---
title: 'クイック スタート: Azure Key Vault でのシークレットの設定と取得 | Microsoft Docs'
description: 'クイック スタート: Azure Key Vault でのシークレットの設定と取得'
services: key-vault
author: syntaxc4
manager: erifkin
ms.date: 07/24/2018
ms.author: cfowler
zone_pivot_groups: keyvault-languages
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: 497631fe46ac4e2c9c495a609547753a84d662bf
ms.sourcegitcommit: d3c7b49dc854dae8da9cd49da8ac4035789a5010
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/23/2018
ms.locfileid: "49805748"
---
# <a name="quickstart-set-and-retrieve-a-secret-from-azure-key-vault"></a>クイック スタート: Azure Key Vault でのシークレットの設定と取得

このクイック スタートでは、Web アプリを使って Key Vault にシークレットを格納する方法とシークレットを取得する方法について説明します。 シークレット値を確認するには、Azure でこれを実行する必要があります。 このクイック スタートでは Node.js とマネージド サービス ID (MSI) を使用します。

> [!div class="checklist"]
> * キー コンテナーを作成します。
> * キー コンテナーにシークレットを格納します。
> * キー コンテナーからシークレットを取得します。
> * Azure AD Web アプリケーションを作成します。
> * [マネージド サービス ID を有効にします](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview)。
> * Web アプリケーションに必要なアクセス許可を付与して、キー コンテナーからデータを読み取ります。

先に進む前に、[基本的な概念](https://docs.microsoft.com/azure/key-vault/key-vault-whatis#basic-concepts)を理解しておいてください。

> [!NOTE]
> 下記のチュートリアルがベスト プラクティスである理由を理解するには、いくつかの概念を理解する必要があります。 Key Vault は、プログラムでシークレットを格納できる中央リポジトリです。 しかしこれを実行するには、アプリケーション/ユーザーが最初に Key Vault に対する認証を行う (シークレットを提示する) 必要があります。 セキュリティのベスト プラクティスに従うために、最初のシークレットのローテーションが定期的に行われる必要もあります。 しかしながら、Azure で実行される[マネージド サービス ID](https://docs.microsoft.com/azure/active-directory/managed-service-identity/overview) アプリケーションでは、Azure によって自動で管理される ID が提供されます。 これにより、**シークレット導入問題**が解決されます。ユーザー/アプリケーションはベスト プラクティスに従うことができ、最初のシークレットのローテーションについて心配する必要がありません

## <a name="prerequisites"></a>前提条件

::: zone pivot="nodejs"
* [Node JS](https://nodejs.org/en/)
::: zone-end
::: zone pivot="dotnet"
* 次のワークロードでは [Visual Studio 2017 バージョン 15.7.3 以降](https://www.microsoft.com/net/download/windows)。
  * ASP.NET および Web の開発
  * .NET Core クロスプラットフォームの開発
* [.NET Core 2.1 SDK 以降](https://www.microsoft.com/net/download/windows)
::: zone-end
* Git ([ダウンロード](https://git-scm.com/downloads))。
* Azure サブスクリプション。 Azure サブスクリプションをお持ちでない場合は、開始する前に[無料アカウント](https://azure.microsoft.com/free/?WT.mc_id=A261C142F)を作成してください。
* [Azure CLI](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest) バージョン 2.0.4 以降。 これは、Windows、Mac、Linux に対応しています。

## <a name="login-to-azure"></a>Azure にログインする

CLI を使用して Azure にログインするには、次のように入力します。

```azurecli
az login
```

## <a name="create-resource-group"></a>リソース グループを作成する

[az group create](/cli/azure/group#az-group-create) コマンドでリソース グループを作成します。 Azure リソース グループとは、Azure リソースのデプロイと管理に使用する論理コンテナーです。

リソース グループ名を選択し、プレース ホルダーを入力してください。
次の例では、*<YourResourceGroupName>* という名前のリソース グループを *eastus* の場所に作成します。

```azurecli
# To list locations: az account list-locations --output table
az group create --name "<YourResourceGroupName>" --location "East US"
```

作成したリソース グループは、このチュートリアルの全体を通して使用します。

## <a name="create-an-azure-key-vault"></a>Azure Key Vault を作成する

次に、前の手順で作成したリソース グループを使って Key Vault を作成します。 この記事全体で Key Vault の名前として "ContosoKeyVault" を使用していますが、一意の名前を使用する必要があります。 次の情報を指定します。

* Key Vault 名 - **こちらで Key Vault 名を選択してください**。
* リソース グループ名 -**こちらでリソース グループ名を選択してください**。
* 場所: **米国東部**。

```azurecli
az keyvault create --name "<YourKeyVaultName>" --resource-group "<YourResourceGroupName>" --location "East US"
```

この時点で、自分の Azure アカウントが唯一、この新しいコンテナーで任意の操作を実行することを許可されています。

## <a name="add-a-secret-to-key-vault"></a>キー コンテナーにシークレットを追加する

シークレットのしくみをよく理解できるように、シークレットを追加します。 SQL 接続文字列やその他の情報を機密として保持する必要があるのに、アプリケーションで使用可能になるように保管している場合があります。 このチュートリアルでは、パスワードを **AppSecret** と呼び、このパスワード内に **MySecret** という値を格納します。

次のコマンドを入力して、値 **MySecret** を保存する **AppSecret** というシークレットをキー コンテナーに作成します。

```azurecli
az keyvault secret set --vault-name "<YourKeyVaultName>" --name "AppSecret" --value "MySecret"
```

シークレットに格納されている値をプレーンテキストとして表示するには:

```azurecli
az keyvault secret show --name "AppSecret" --vault-name "<YourKeyVaultName>"
```

このコマンドは、URI を含むシークレットの情報を表示します。 これらの手順を完了すると、Azure Key Vault のシークレットへの URI がわかります。 この情報を書き留めておいてください。 後の手順で必要になります。

## <a name="clone-the-repo"></a>リポジトリを複製する

次のコマンドを実行してリポジトリを複製し、ソースを編集するためのローカル コピーを作成します。

```bash
git clone https://github.com/Azure-Samples/key-vault-node-quickstart.git
```

::: zone pivot="nodejs"

## <a name="install-dependencies"></a>依存関係をインストールする

ここで依存関係をインストールします。 次のコマンドを実行します。

    cd key-vault-node-quickstart
    npm install

このプロジェクトでは、次の 2 つのノード モジュールを使用しました。

* [ms-rest-azure](https://www.npmjs.com/package/ms-rest-azure) 
* [azure-keyvault](https://www.npmjs.com/package/azure-keyvault)

## <a name="publish-the-web-application-to-azure"></a>Azure に Web アプリケーションを発行する

アプリケーションを Azure に発行するために必要な手順は次のようになります。

* 1 つ目の手順は、[Azure App Service](https://azure.microsoft.com/services/app-service/) プランの作成です。 このプランには複数の Web アプリを格納することができます。

    ```azurecli
    az appservice plan create --name myAppServicePlan --resource-group myResourceGroup
    ```
* 次に、Web アプリを作成します。 次の例では、<app_name> をグローバルに一意のアプリ名に置き換えてください (有効な文字は a-z、0-9、-)。 ランタイムは NODE|6.9 に設定されています。 サポートされているすべてのランタイムを確認するには、`az webapp list-runtimes` を実行します。

    ```azurecli
    az webapp create --resource-group myResourceGroup --plan myAppServicePlan --name <app_name> --runtime "NODE|6.9" --deployment-local-git
    ```

    Web アプリが作成されると、Azure CLI によって次の例のような出力が表示されます。

    ```json
    {
      "availabilityState": "Normal",
      "clientAffinityEnabled": true,
      "clientCertEnabled": false,
      "cloningInfo": null,
      "containerSize": 0,
      "dailyMemoryTimeQuota": 0,
      "defaultHostName": "<app_name>.azurewebsites.net",
      "enabled": true,
      "deploymentLocalGitUrl": "https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git"
      < JSON data removed for brevity. >
    }
    ```
    新しく作成された Web アプリに移動すると、Web アプリが稼働していることがわかります。 <app_name> は、アプリの一意の名前に置き換えてください。

    ```text
    http://<app name>.azurewebsites.net
    ```
    また、上のコマンドを実行すると、ローカル Git から Azure にデプロイすることができる Git 対応のアプリが作成されます。 
    ローカル Git は、"https://<username>@<app_name>.scm.azurewebsites.net/<app_name>.git" という URL を使って構成されています。

* デプロイ ユーザーを作成します。前のコマンドが完了したら、ローカル Git リポジトリに Azure リモートを追加できます。 <url> を、「アプリの Git を有効にする」で取得した Git リモートの URL で置き換えます。

    ```bash
    git remote add azure <url>
    ```
    
::: zone-end

::: zone pivot="dotnet"
## <a name="open-and-edit-the-solution"></a>ソリューションを開いて編集する

program.cs ファイルを編集し、特定のキー コンテナー名でサンプルを実行します。

1. フォルダー key-vault-dotnet-core-quickstart を参照します。
2. Visual Studio 2017 で、key-vault-dotnet-core-quickstart.sln ファイルを開きます。
3. Program.cs ファイルを開き、プレースホルダー *YourKeyVaultName* を先ほど作成したキー コンテナーの名前に更新します。

このソリューションでは、[AppAuthentication](https://www.nuget.org/packages/Microsoft.Azure.Services.AppAuthentication) ライブラリと [KeyVault](https://www.nuget.org/packages/Microsoft.Azure.KeyVault) NuGet ライブラリが使用されます。

## <a name="run-the-app"></a>アプリを実行する

Visual Studio 2017 のメイン メニューで、**[デバッグ]** > **[デバッグなしで開始]** と選択します。 ブラウザーが表示されたら、**[バージョン情報]** ページに移動します。 **AppSecret** の値が表示されます。

## <a name="publish-the-web-application-to-azure"></a>Azure に Web アプリケーションを発行する

このアプリを Azure に発行し、Web アプリとしてライブであることと、シークレット値を取得することを確認します。

1. Visual Studio で、**key-vault-dotnet-core-quickstart** プロジェクトを選択します。
2. **[発行]** > **[開始]** の順に選択します。
3. 新しい **App Service** を作成し、**[発行]** を選択します。
4. アプリ名を **keyvaultdotnetcorequickstart** に変更します。
5. **[作成]** を選択します。

>[!VIDEO https://sec.ch9.ms/ch9/e93d/a6ac417f-2e63-4125-a37a-8f34bf0fe93d/KeyVault_high.mp4]
::: zone-end

## <a name="enable-managed-service-identities"></a>マネージド サービス ID を有効にする

Azure Key Vault は、資格情報およびその他のキーやシークレットを安全に保管する方法を提供しますが、コードは Azure Key Vault に認証してそれらを取得する必要があります。 マネージド サービス ID は、Azure Active Directory (Azure AD) で自動的に管理されている ID を Azure サービスに付与することで、これを簡単にします。 この ID を使用して、コードに資格情報が含まれていなくても、Key Vault を含む Azure AD の認証をサポートする任意のサービスに認証することができます。

1. Azure CLI に戻ります。
2. assign-identity コマンドを実行して、このアプリケーションの ID を作成します。

   ```azurecli
   az webapp identity assign --name "keyvaultdotnetcorequickstart" --resource-group "<YourResourceGroupName>"
   ```

>[!NOTE]
>このプロシージャのコマンドは、ポータルに移動して、Web アプリケーション プロパティの **[マネージド サービス ID]** を **[オン]** に切り替えることと同等です。

## <a name="assign-permissions-to-your-application-to-read-secrets-from-key-vault"></a>アプリケーションにアクセス許可を割り当ててキー コンテナーからシークレットを読み取る

アプリケーションを Azure に発行するときの出力をメモします。 次の形式にする必要があります。

```json
        {
          "principalId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "tenantId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
          "type": "SystemAssigned"
        }
```

次に、キー コンテナーの名前と **PrincipalId** の値を使用してこのコマンドを実行します。

```azurecli
az keyvault set-policy --name '<YourKeyVaultName>' --object-id <PrincipalId> --secret-permissions get
```

::: zone pivot="nodejs"
## <a name="deploy-the-node-app-to-azure-and-retrieve-the-secret-value"></a>Node アプリを Azure にデプロイしてシークレット値を取得する

以上で準備は完了です。 次のコマンドを実行してアプリを Azure にデプロイします。

```bash
git push azure master
```

その後ブラウザーで https://<app_name>.azurewebsites.net にアクセスすると、シークレット値が確認できます。
<YourKeyVaultName> という名前を実際のコンテナー名に置き換えたことを確認してください

::: zone-end

::: zone pivot="dotnet"
これで、アプリケーションを実行すると、取得されたシークレットの値が表示されます。
::: zone-end

## <a name="next-steps"></a>次のステップ

::: zone pivot="nodejs"
* [Azure Key Vault のホーム ページ](https://azure.microsoft.com/services/key-vault/)
* [Azure Key Vault のドキュメント](https://docs.microsoft.com/azure/key-vault/)
* [Azure SDK For Node](https://docs.microsoft.com/javascript/api/overview/azure/key-vault)
* [Azure REST API リファレンス](https://docs.microsoft.com/rest/api/keyvault/)
::: zone-end

::: zone pivot="dotnet"
* [Azure Key Vault のホーム ページ](https://azure.microsoft.com/services/key-vault/)
* [Azure Key Vault のドキュメント](https://docs.microsoft.com/azure/key-vault/)
* [Azure SDK for .NET](https://github.com/Azure/azure-sdk-for-net)
* [Azure REST API リファレンス](https://docs.microsoft.com/rest/api/keyvault/)
::: zone-end
