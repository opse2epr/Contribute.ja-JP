---
title: ローカルでの Git リポジトリの設定
description: この記事では、フォークや複製のプロセスなど、ローカル Git リポジトリの作成およびドキュメントへの投稿方法に関するガイダンスを示します。
author: jasonwhowell
ms.author: jasonh
manager: kfile
ms.date: 01/18/2018
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: f702d0d29ee7dc9c69cb26b79bf6283d91b6b6bc
ms.sourcegitcommit: 3ec397fab57ea582edb03a59609f62d886410ee8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2018
---
# <a name="set-up-git-repository-locally-for-documentation"></a><span data-ttu-id="92532-103">ドキュメントの Git リポジトリをローカルに設定する</span><span class="sxs-lookup"><span data-stu-id="92532-103">Set up Git repository locally for documentation</span></span>

<span data-ttu-id="92532-104">この記事では、Microsoft のドキュメントに投稿することを目的として、ローカル コンピューターに git リポジトリを設定する手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="92532-104">This article describes the steps to set up a git repository on your local machine, with the intent to contribute to Microsoft documentation.</span></span> <span data-ttu-id="92532-105">共同作成者は、ローカルに複製されたリポジトリを使用して、新規記事の追加、既存の記事の大幅な編集、またはアートワークの変更を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="92532-105">Contributors may use a locally cloned repository to add new articles, do major edits on existing articles, or change artwork.</span></span>

<span data-ttu-id="92532-106">投稿を開始するには、次の 1 回限りのセットアップ アクティビティを実行します。</span><span class="sxs-lookup"><span data-stu-id="92532-106">You run these one-time setup activities to get started contributing:</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="92532-107">適切なリポジトリを決定する</span><span class="sxs-lookup"><span data-stu-id="92532-107">Determine the appropriate repository</span></span>
> * <span data-ttu-id="92532-108">GitHub アカウントにリポジトリをフォークする</span><span class="sxs-lookup"><span data-stu-id="92532-108">Fork the repository to your GitHub account</span></span>
> * <span data-ttu-id="92532-109">複製されたファイルのローカル フォルダーを選択する</span><span class="sxs-lookup"><span data-stu-id="92532-109">Choose a local folder for the cloned files</span></span>
> * <span data-ttu-id="92532-110">ローカル コンピューターにリポジトリを複製する</span><span class="sxs-lookup"><span data-stu-id="92532-110">Clone the repository to your local machine</span></span>
> * <span data-ttu-id="92532-111">アップストリームのリモート値を構成する</span><span class="sxs-lookup"><span data-stu-id="92532-111">Configure the upstream remote value</span></span>

> [!IMPORTANT]
> <span data-ttu-id="92532-112">記事に軽微な変更しか加えていない場合は、この記事の手順を完了する必要*はありません*。</span><span class="sxs-lookup"><span data-stu-id="92532-112">If you're making only minor changes to an article, you *do not* need to complete the steps in this article.</span></span> <span data-ttu-id="92532-113">[簡易的な変更のワークフロー](index.md#quick-edits-to-existing-documents)に直接進むことができます。</span><span class="sxs-lookup"><span data-stu-id="92532-113">You can continue directly to the [quick changes workflow](index.md#quick-edits-to-existing-documents).</span></span>
>

## <a name="overview"></a><span data-ttu-id="92532-114">概要</span><span class="sxs-lookup"><span data-stu-id="92532-114">Overview</span></span>

<span data-ttu-id="92532-115">Microsoft のドキュメント サイトに投稿するには、対応するドキュメント リポジトリを複製して、マークダウン ファイルをローカルで作成および編集します。</span><span class="sxs-lookup"><span data-stu-id="92532-115">To contribute to Microsoft's documentation site, you can make and edit Markdown files locally by cloning the corresponding documentation repository.</span></span> <span data-ttu-id="92532-116">Microsoft では、github アカウントに適切なリポジトリをフォークすることを要求しています。それにより、予定している変更を保存するための読み取り/書き込み権限が付与されます。</span><span class="sxs-lookup"><span data-stu-id="92532-116">Microsoft requires you to fork the appropriate repository into your own github account, so that you have read/write permissions there to store your proposed changes.</span></span> <span data-ttu-id="92532-117">その後、プル要求を使用して、変更を読み取り専用の一元的な共有リポジトリにマージします。</span><span class="sxs-lookup"><span data-stu-id="92532-117">Then you use pull requests to merge changes into the read-only central shared repository.</span></span>

![GitHub の三角形](./media/git-and-github-initial-setup.png)

<span data-ttu-id="92532-119">GitHub を初めて使用する場合は、次のビデオを視聴して、フォークと複製のプロセスの概念について概要を確認します。</span><span class="sxs-lookup"><span data-stu-id="92532-119">If you're new to GitHub, watch the following video for a conceptual overview of the forking and cloning process:</span></span>

>[!VIDEO https://channel9.msdn.com/Blogs/CoolMoose/Git-Repository-Setup/player]

## <a name="determine-the-repository"></a><span data-ttu-id="92532-120">リポジトリを決定する</span><span class="sxs-lookup"><span data-stu-id="92532-120">Determine the repository</span></span>

<span data-ttu-id="92532-121">[docs.microsoft.com](https://docs.microsoft.com) にホストされているドキュメントは、[github.com](https://www.github.com) のいくつかの異なるリポジトリに存在します。</span><span class="sxs-lookup"><span data-stu-id="92532-121">Documentation hosted at [docs.microsoft.com](https://docs.microsoft.com) resides in several different repositories at [github.com](https://www.github.com).</span></span>

1. <span data-ttu-id="92532-122">使用するリポジトリが不明な場合は、Web ブラウザーを使用して docs.microsoft.com 上の記事にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="92532-122">If you are unsure of which repository to use, then visit the article on docs.microsoft.com using your web browser.</span></span> <span data-ttu-id="92532-123">記事の右上にある **[編集]** リンク (鉛筆のアイコン) を選択します。</span><span class="sxs-lookup"><span data-stu-id="92532-123">Select the **Edit** link (pencil icon) on the upper right of the article.</span></span>

   ![[編集] をクリックしてリポジトリとファイルの場所を特定します。](media/index/edit-article.png)

2. <span data-ttu-id="92532-125">このリンクでは、適切なリポジトリ内の対応するマークダウン ファイルがある github.com の場所に移動します。</span><span class="sxs-lookup"><span data-stu-id="92532-125">That link takes you to github.com location for the corresponding Markdown file in the appropriate repository.</span></span> <span data-ttu-id="92532-126">リポジトリ名を表示するための URL にご注意ください。</span><span class="sxs-lookup"><span data-stu-id="92532-126">Note the URL to view the repository name.</span></span>

   ![リポジトリの場所を特定する URL にご注意ください。](media/public-repo.png)

   <span data-ttu-id="92532-128">たとえば、よく使用される次のリポジトリは公開投稿に使用できます。</span><span class="sxs-lookup"><span data-stu-id="92532-128">For example, these popular repositories are available for public contributions:</span></span>
   - <span data-ttu-id="92532-129">Azure ドキュメント[https://github.com/MicrosoftDocs/azure-docs](https://github.com/MicrosoftDocs/azure-docs)</span><span class="sxs-lookup"><span data-stu-id="92532-129">Azure documentation [https://github.com/MicrosoftDocs/azure-docs](https://github.com/MicrosoftDocs/azure-docs)</span></span>
   - <span data-ttu-id="92532-130">SQL Server ドキュメント[https://github.com/MicrosoftDocs/sql-docs](https://github.com/MicrosoftDocs/sql-docs)</span><span class="sxs-lookup"><span data-stu-id="92532-130">SQL Server documentation [https://github.com/MicrosoftDocs/sql-docs](https://github.com/MicrosoftDocs/sql-docs)</span></span>
   - <span data-ttu-id="92532-131">Visual Studio ドキュメント[https://github.com/MicrosoftDocs/visualstudio-docs](https://github.com/MicrosoftDocs/visualstudio-docs)</span><span class="sxs-lookup"><span data-stu-id="92532-131">Visual Studio documentation [https://github.com/MicrosoftDocs/visualstudio-docs](https://github.com/MicrosoftDocs/visualstudio-docs)</span></span>
   - <span data-ttu-id="92532-132">.NET ドキュメント[https://github.com/dotnet/docs](https://github.com/dotnet/docs)</span><span class="sxs-lookup"><span data-stu-id="92532-132">.NET Documentation [https://github.com/dotnet/docs](https://github.com/dotnet/docs)</span></span>
   - <span data-ttu-id="92532-133">Azure .NET SDK ドキュメント[https://github.com/azure/azure-docs-sdk-dotnet](https://github.com/azure/azure-docs-sdk-dotnet)</span><span class="sxs-lookup"><span data-stu-id="92532-133">Azure .Net SDK documentation [https://github.com/azure/azure-docs-sdk-dotnet](https://github.com/azure/azure-docs-sdk-dotnet)</span></span>

## <a name="fork-the-repository"></a><span data-ttu-id="92532-134">リポジトリのフォーク</span><span class="sxs-lookup"><span data-stu-id="92532-134">Fork the repository</span></span>
<span data-ttu-id="92532-135">適切なリポジトリを使用し、GitHub Web サイトで GitHub アカウントにリポジトリのフォークを作成します。</span><span class="sxs-lookup"><span data-stu-id="92532-135">Using the appropriate repository, create a fork of the repository into your own GitHub account by using the GitHub website.</span></span>

<span data-ttu-id="92532-136">すべてのメイン ドキュメント リポジトリでは、読み取り専用アクセスが提供され、つまり、リポジトリのコンテンツを直接変更することはできないので、個人用のフォークが必要です。</span><span class="sxs-lookup"><span data-stu-id="92532-136">A personal fork is required since all main documentation repositories provide read-only access, which means you cannot make changes directly on content in the repositories.</span></span> <span data-ttu-id="92532-137">変更するには、自分のフォークからメイン リポジトリに[プル要求](git-github-fundamentals.md#pull-requests)を送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="92532-137">To make changes, you must submit a [pull request](git-github-fundamentals.md#pull-requests) from your fork into the main repository.</span></span> <span data-ttu-id="92532-138">このプロセスを容易にするには、まずリポジトリの独自のコピーが必要になります。このコピーでは、書き込みアクセス権を持ちます。</span><span class="sxs-lookup"><span data-stu-id="92532-138">To facilitate this process, you first need your own copy of the repository, in which you have write access.</span></span> <span data-ttu-id="92532-139">GitHub の "*fork*" はその目的にかなっています。</span><span class="sxs-lookup"><span data-stu-id="92532-139">A GitHub *fork* serves that purpose.</span></span>

1. <span data-ttu-id="92532-140">メイン リポジトリの GitHub ページに移動して、右上の **[フォーク]** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="92532-140">Go to the main repository's GitHub page and click the **Fork** button on the upper right.</span></span>

   ![GitHub プロファイルの例](./media/contribute-get-started-setup-local/fork.png)

2. <span data-ttu-id="92532-142">メッセージが表示されたら、フォークの作成先として、GitHub アカウント タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="92532-142">If you are prompted, select your GitHub account tile as the destination where the fork should be created.</span></span> <span data-ttu-id="92532-143">これにより、GitHub アカウント内にフォークと呼ばれるリポジトリのコピーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="92532-143">This prompt creates a copy of the repository within your GitHub account, known as a fork.</span></span>

## <a name="choose-a-local-folder"></a><span data-ttu-id="92532-144">ローカル フォルダーを選択する</span><span class="sxs-lookup"><span data-stu-id="92532-144">Choose a local folder</span></span>
<span data-ttu-id="92532-145">リポジトリのコピーをローカルで保持するためのローカル フォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="92532-145">Make a local folder to hold a copy of the repository locally.</span></span> <span data-ttu-id="92532-146">一部のリポジトリは大きくなることがあります。たとえば、azure-docs は最大で 5 GB になります。</span><span class="sxs-lookup"><span data-stu-id="92532-146">Some of the repositories can be large; up to 5 GB for azure-docs for example.</span></span> <span data-ttu-id="92532-147">利用可能なディスク領域がある場所を選択します。</span><span class="sxs-lookup"><span data-stu-id="92532-147">Choose a location with available disk space.</span></span>

1. <span data-ttu-id="92532-148">覚えやすく入力しやすいフォルダー名を選択します。</span><span class="sxs-lookup"><span data-stu-id="92532-148">Choose a folder name should be easy for you to remember and type.</span></span> <span data-ttu-id="92532-149">たとえば、ルート フォルダー `C:\docs\` を使用するか、ユーザー プロファイル ディレクトリ `~/Documents/docs/` にフォルダーを作成することを検討してください</span><span class="sxs-lookup"><span data-stu-id="92532-149">For example, consider a root folder `C:\docs\` or make a folder in your user profile directory `~/Documents/docs/`</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="92532-150">別の Git リポジトリ フォルダーの場所内に入れ子になっているローカル フォルダーの場所を選択しないてください。</span><span class="sxs-lookup"><span data-stu-id="92532-150">Avoid choosing a local folder path that is nested inside of another git repository folder location.</span></span> <span data-ttu-id="92532-151">相互に隣接された Git 複製フォルダーを格納することは可能ですが、相互の Git フォルダー内に Git フォルダーを入れ子にすると、ファイルの追跡でエラーが発生する原因になります。</span><span class="sxs-lookup"><span data-stu-id="92532-151">While it is acceptable to store the git cloned folders adjacent to each other, nesting git folders inside one another causes errors for the file tracking.</span></span>

2. <span data-ttu-id="92532-152">Git Bash を起動する</span><span class="sxs-lookup"><span data-stu-id="92532-152">Launch Git Bash</span></span>

   ![Git Bash を起動します。](./media/contribute-get-started-setup-local/gitbash-start.png)

   <span data-ttu-id="92532-154">Git Bash を起動する既定の場所は、Windows では一般的にホーム ディレクトリ (~) または `/c/users/<Windows-user-account>/` です。</span><span class="sxs-lookup"><span data-stu-id="92532-154">The default location that Git Bash starts in is typically the home directory (~) or `/c/users/<Windows-user-account>/` on Windows OS.</span></span>

   <span data-ttu-id="92532-155">現在のディレクトリを確認するには、$ プロンプトで「`pwd`」と入力します。</span><span class="sxs-lookup"><span data-stu-id="92532-155">To determine the current directory, type `pwd` at the $ prompt.</span></span> 

3. <span data-ttu-id="92532-156">レポジトリをローカルでホストするために作成したフォルダー内にディレクトリを変更します (cd)。</span><span class="sxs-lookup"><span data-stu-id="92532-156">Change directory (cd) into the folder that you created for hosting the repository locally.</span></span> <span data-ttu-id="92532-157">Git Bash では、フォルダー パスにバックスラッシュの代わりに Linux 規則であるフォワード スラッシュを使用します。</span><span class="sxs-lookup"><span data-stu-id="92532-157">Note that Git Bash uses Linux convention of forward-slashes instead of back-slashes for folder paths.</span></span>

   <span data-ttu-id="92532-158">たとえば、`cd /c/docs/ ` や `cd ~/Documents/docs/` のようにします。</span><span class="sxs-lookup"><span data-stu-id="92532-158">For example, `cd /c/docs/ ` or `cd ~/Documents/docs/`</span></span>

## <a name="create-a-local-clone"></a><span data-ttu-id="92532-159">ローカル複製を作成する</span><span class="sxs-lookup"><span data-stu-id="92532-159">Create a local clone</span></span>

<span data-ttu-id="92532-160">Git Bash を使用し、**clone** コマンドを実行してデバイスの現在のディレクトリにリポジトリのコピー (自分のフォーク) をプルすることを準備します。</span><span class="sxs-lookup"><span data-stu-id="92532-160">Using Git Bash, prepare to run the **clone** command to pull a copy of a repository (your fork) down to your device on the current directory.</span></span> 

### <a name="authenticate-by-using-git-credential-manager"></a><span data-ttu-id="92532-161">Git Credential Manager を使用した認証</span><span class="sxs-lookup"><span data-stu-id="92532-161">Authenticate by using Git Credential Manager</span></span>
<span data-ttu-id="92532-162">最新バージョンの Git for Windows をインストールして、既定のインストールを受け入れた場合、Git Credential Manager は既定で有効になります。</span><span class="sxs-lookup"><span data-stu-id="92532-162">If you installed the latest version of Git for Windows and accepted the default installation, Git Credential Manager is enabled by default.</span></span> <span data-ttu-id="92532-163">Git Credential Manager を使用すると、GitHub との認証済み接続およびリモートを再確立するときに、個人用アクセス トークンをあらためて呼び出す必要がなくなるため、認証が大幅に簡単になります。</span><span class="sxs-lookup"><span data-stu-id="92532-163">Git Credential Manager makes authentication much easier, because you don't need to recall your personal access token when re-establishing authenticated connections and remotes with GitHub.</span></span>

1. <span data-ttu-id="92532-164">リポジトリ名を指定して **clone** コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="92532-164">Run the **clone** command, by providing the repository name.</span></span> <span data-ttu-id="92532-165">複製によって、フォークされたリポジトリがローカル コンピューターにダウンロード (複製) されます。</span><span class="sxs-lookup"><span data-stu-id="92532-165">Cloning downloads (clone) the forked repository on your local computer.</span></span> 

    > [!Tip]
    > <span data-ttu-id="92532-166">GitHub UI の **[Clone or download]\(複製またはダウンロード\)** から、clone コマンド用のフォークの GitHub URL を取得できます。</span><span class="sxs-lookup"><span data-stu-id="92532-166">You can get your fork's GitHub URL for the clone command from the **Clone or download** button in the GitHub UI:</span></span>
    >
    > ![[Clone or download]\(複製またはダウンロード\)](./media/contribute-get-started-setup-local/clone-or-download.png)

    <span data-ttu-id="92532-168">複製処理中に、フォークの作成元のメイン リポジトリではなく、*フォーク*のパスを指定します。</span><span class="sxs-lookup"><span data-stu-id="92532-168">Be sure to specify the path to *your fork* during the cloning process, not the main repository from which you created the fork.</span></span> <span data-ttu-id="92532-169">そのようにしないと、変更に協力できません。</span><span class="sxs-lookup"><span data-stu-id="92532-169">Otherwise, you cannot contribute changes.</span></span> <span data-ttu-id="92532-170">フォークは、個人用の GitHub ユーザー アカウント (`github.com/<github-username>/<repo>` など) を通じて参照されます。</span><span class="sxs-lookup"><span data-stu-id="92532-170">Your fork is referenced through your personal GitHub user account, such as `github.com/<github-username>/<repo>`.</span></span>

    ```bash
    git clone https://github.com/<github-username>/<repo>.git
    ```

    <span data-ttu-id="92532-171">clone コマンドは次の例のようになります。</span><span class="sxs-lookup"><span data-stu-id="92532-171">Your clone command should look similar to this example:</span></span>

    ```bash
    git clone https://github.com/smithj/azure-docs.git
    ```

2. <span data-ttu-id="92532-172">メッセージが表示されたら、GitHub 資格情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="92532-172">When you're prompted, enter your GitHub credentials.</span></span>

    ![GitHub ログイン](./media/contribute-get-started-setup-local/github-login.png)

3. <span data-ttu-id="92532-174">メッセージが表示されたら、2 要素認証コードを入力します。</span><span class="sxs-lookup"><span data-stu-id="92532-174">When you're prompted, enter your two-factor authentication code.</span></span>

    ![GitHub 2 要素認証](./media/contribute-get-started-setup-local/github-2fa.png)

    > [!Note]
    > <span data-ttu-id="92532-176">資格情報は保存されて、今後の GitHub 要求の認証に使用されます。</span><span class="sxs-lookup"><span data-stu-id="92532-176">Your credentials will be saved and used to authenticate future GitHub requests.</span></span> <span data-ttu-id="92532-177">コンピューターごとに 1 回だけこの認証を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="92532-177">You only need to do this authentication once per computer.</span></span> 

4. <span data-ttu-id="92532-178">clone コマンドを実行すると、リポジトリ ファイルのコピーをフォークからローカル ディスク上の新しいフォルダーにダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="92532-178">The clone command runs and downloads a copy of the repository files from your fork into a new folder on the local disk.</span></span> <span data-ttu-id="92532-179">新しいフォルダーは現在のフォルダー内に作成されます。</span><span class="sxs-lookup"><span data-stu-id="92532-179">A new folder is made within the current folder.</span></span> <span data-ttu-id="92532-180">リポジトリのサイズによっては数分かかることがあります。</span><span class="sxs-lookup"><span data-stu-id="92532-180">It may take a few minutes, depending on the repository size.</span></span> <span data-ttu-id="92532-181">処理が終了したらフォルダーを調べて構造を確認することができます。</span><span class="sxs-lookup"><span data-stu-id="92532-181">You can explore the folder to see the structure once it is finished.</span></span>

## <a name="configure-remote-upstream"></a><span data-ttu-id="92532-182">リモート アップストリームを構成する</span><span class="sxs-lookup"><span data-stu-id="92532-182">Configure remote upstream</span></span>
<span data-ttu-id="92532-183">レポジトリを複製した後に、**upstream** という名前のメイン リポジトリへの読み取り専用のリモート接続をセットアップします。</span><span class="sxs-lookup"><span data-stu-id="92532-183">After cloning the repository, set up a read-only remote connection to the main repository named **upstream**.</span></span> <span data-ttu-id="92532-184">upstream URL を使用して、他のユーザーが行った最新の変更と、ローカル リポジトリを常に同期しておくことができます。</span><span class="sxs-lookup"><span data-stu-id="92532-184">You use the upstream URL to keep your local repository in sync with the latest changes made by others.</span></span> <span data-ttu-id="92532-185">**git remote** コマンドは、構成値を設定するために使用します。</span><span class="sxs-lookup"><span data-stu-id="92532-185">The **git remote** command is used to set the configuration value.</span></span> <span data-ttu-id="92532-186">**fetch** コマンドを使用して upstream リポジトリからブランチの情報を更新します。</span><span class="sxs-lookup"><span data-stu-id="92532-186">You use the **fetch** command to refresh the branch info from the upstream repository.</span></span>

1. <span data-ttu-id="92532-187">**Git Credential Manager** を使用している場合は、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="92532-187">If you're using **Git Credential Manager**, use the following commands.</span></span> <span data-ttu-id="92532-188">\<repo\> および \<organization\> プレースホルダーを置き換えます。</span><span class="sxs-lookup"><span data-stu-id="92532-188">Replace the \<repo\> and \<organization\> placeholders.</span></span>
   ```bash
   cd <repo>
   git remote add upstream https://github.com/<organization>/<repo>.git
   git fetch upstream
   ```

2. <span data-ttu-id="92532-189">構成された値を表示し、URL が正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="92532-189">View the configured values and confirm the URLs are correct.</span></span> <span data-ttu-id="92532-190">**origin** URL が個人用フォームを指していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="92532-190">Ensure the **origin** URLs point to your personal fork.</span></span> <span data-ttu-id="92532-191">**upstream** URL が MicrosoftDocs や Azure などのメイン リポジトリを指していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="92532-191">Ensure the **upstream** URLs point to the main repository, such as MicrosoftDocs or Azure.</span></span> 
   ```bash
   git remote -v 
   ```

   <span data-ttu-id="92532-192">リモート出力の例を示します。</span><span class="sxs-lookup"><span data-stu-id="92532-192">Example remote output is shown.</span></span> <span data-ttu-id="92532-193">リポジトリ azure-docs にアクセスするための個人用アクセス トークンを使用して MyGitAccount という名前の架空の Git アカウントが構成されます。</span><span class="sxs-lookup"><span data-stu-id="92532-193">A fictitious git account named MyGitAccount is configured with a personal access token to access the repo azure-docs:</span></span>
   ```output
   origin  https://github.com/MyGitAccount/azure-docs.git (fetch)
   origin  https://github.com/MyGitAccount/azure-docs.git(push)
   upstream        https://github.com/MicrosoftDocs/azure-docs.git (fetch)
   upstream        https://github.com/MicrosoftDocs/azure-docs.git (push)
   ```

3. <span data-ttu-id="92532-194">誤りがある場合は、リモート値を削除することができます。</span><span class="sxs-lookup"><span data-stu-id="92532-194">If you made a mistake, you can remove the remote value.</span></span> <span data-ttu-id="92532-195">upstream 値を削除するには、`git remote remove upstream` コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="92532-195">To remove the upstream value, run the command `git remote remove upstream`.</span></span>

## <a name="next-steps"></a><span data-ttu-id="92532-196">次のステップ</span><span class="sxs-lookup"><span data-stu-id="92532-196">Next steps</span></span>
- <span data-ttu-id="92532-197">コンテンツの追加と更新の詳細については、[GitHub 共同作成ワークフロー](how-to-write-workflows-major.md)に関するページに進んでください。</span><span class="sxs-lookup"><span data-stu-id="92532-197">To learn more about adding and updating content, continue to the [GitHub contribution workflow](how-to-write-workflows-major.md).</span></span>