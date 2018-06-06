---
title: Microsoft Docs 共同作成者ガイド概要
description: このガイドでは、Microsoft ドキュメント サイト docs.microsoft.com で協力する方法について説明します。
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 04/17/2018
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 1cda40c890e5b30e6e1e10f3bcee0278f8004653
ms.sourcegitcommit: 782b689882cce3ce07f5613763322989f2d0d63f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/05/2018
ms.locfileid: "34469442"
---
# <a name="microsoft-docs-contributor-guide-overview"></a>Microsoft Docs 共同作成者ガイド概要

[docs.microsoft.com](https://docs.microsoft.com) (Docs) 共同作成者ガイドへようこそ。

Microsoft のドキュメント セットには、GitHub でホストされているオープン ソースのものがあります。 多くのチームが頻繁にこのモデルを採用しています。 プル要求を作成するために招待された場合、完全にオープン ソースでないドキュメント セットでも一般公開用のリポジトリがあります。 これを使用すると、製品エンジニア、コンテンツ チーム、顧客との間のコミュニケーションが効率化され改善されます。 オープン環境で作業すると、次のようないくつかの利点があります。

- 最も必要なドキュメントに関するフィードバックを取得するために、開かれたオープン ソースのリポジトリのプラン。
- 最初のリリースで最も役立つコンテンツを公開するために、開かれたオープン ソースのリポジトリのレビュー。
- コンテンツを継続して改善しやすくするために、開かれたオープン ソースのリポジトリの更新。

[docs.microsoft.com](https://docs.microsoft.com) のユーザー エクスペリエンスは、より操作しやすいように、[GitHub](https://github.com) のワークフローに直接統合されています。 [表示しているドキュメントを編集](#quick-edits-to-existing-documents)して開始します。 または、[新しいトピックをレビュー](#review-open-prs)して支援するか、[品質の Issue を作成します](#create-quality-issues)。

> [!IMPORTANT]
> docs.microsoft.com に公開されるすべてのリポジトリには、「[Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/)」 (Microsoft オープン ソース倫理規定) または「[.NET Foundation Code of Conduct](https://dotnetfoundation.org/code-of-conduct)」 (.NET Foundation 倫理規定) が適用されています。 詳細については、「[Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/)」 (倫理規定に関する FAQ) を参照してください。 または、ご質問やコメントがある場合は、[opencode@microsoft.com](mailto:opencode@microsoft.com) または [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org) までご連絡ください。<br>
>
> パブリック リポジトリ内にあるドキュメントおよびコード例の軽微な修正や補足は、「[docs.microsoft.com - 使用条件](https://docs.microsoft.com/legal/termsofuse)」の対象になります。 Microsoft の従業員ではない共同作成者が新規または大幅な変更を加えた場合、オンライン貢献者使用許諾契約書 (CLA) の提出を要求するコメントがプル要求内に生成されます。 プル要求をレビューまたは承認できるように、オンライン フォームへのご記入をお願いいたします。

## <a name="quick-edits-to-existing-documents"></a>既存のドキュメントへのクイック編集

クイック編集はプロセスを効率化し、ドキュメント内の小さなエラーや省略を報告および修正します。 さまざまな努力を重ねても、文章校正やスペルチェックの小さなエラーは公開されたドキュメントに入り込みます。 Issue (問題) を作成してミスを報告できますが、プル要求 (PR) を作成して Issue を修正する方が速くて簡単です。 次の図のように編集ボタンが、ほとんどすべての記事に表示されます。 **[編集]** ボタンをクリックすると、GitHub 上のソース ファイルに移動します。

![[編集] リンクの場所](./media/index/edit-article.png)

次に、次の図に示されているように鉛筆アイコンをクリックして、記事を編集します。

> [!NOTE]
> 鉛筆アイコンが灰色表示されている場合は、GitHub アカウントにログインするか、新しいアカウントを作成する必要があります。 Web エディターで変更を加えます。 **[変更のプレビュー]** タブをクリックして、変更の書式設定を確認できます。

![鉛筆アイコンの場所](./media/index/editicon.png)

変更を加えたら、ページの一番下へスクロールします。 次の図のように、自分の PR にタイトルと説明を入力して、**[Propose file change]** をクリックします。

![ファイルの変更を提案する](./media/index/submit-pull-request.png)

これで終了です。 コンテンツ チームのメンバーが、PR をレビューしてマージします。 大規模な変更を加えた場合、変更を要求するフィードバックを受け取る可能性があります。

GitHub の UI の編集は、リポジトリ上の自分のアクセス許可に対応しています。 前の図は、ターゲットのリポジトリへの書き込みアクセス許可がない共同作成者に対して正確な図です。 GitHub では、お使いのアカウントにターゲットのリポジトリのフォークが自動的に作成されます。 ターゲットのリポジトリへの書き込みアクセス権がある場合、GitHub ではターゲットのリポジトリに新しいブランチが作成されます。 ブランチ名には、GitHub ID、およびパッチのブランチに対する数値識別子を使用する、フォーム **\<GitHubId\>-patch-n** が含まれます。

Microsoft ではすべての変更だけでなく、書き込みアクセス権がある共同作成者に対しても PR を使用します。 ほとんどのリポジトリに保護された `master` ブランチがあるため、更新プログラムを PR として提出する必要があります。

ブラウザー内の編集操作は、マイナー変更や頻度の低い変更に最適です。 大規模な共同作成を行う場合、または Git の高度な機能 (ブランチ管理や高度なマージの競合の解決など) を使用する場合は、[リポジトリをフォークしてローカルで作業する](how-to-write-workflows-major.md)必要があります。

## <a name="review-open-prs"></a>開いている PR をレビューする

現在、開いている PR を確認して公開する前に、新しいトピックを確認することができます。 レビューは [GitHub のフロー](https://guides.github.com/introduction/flow/) プロセスに従います。 パブリック リポジトリにある提案された更新や新しい記事を確認できます。 それらをレビューしてコメントを追加します。 ドキュメント リポジトリのいずれかを参照し、関心のあるエリアの開いているプル要求 (PR) を確認します。 提案された更新のコミュニティ フィードバックは、コミュニティ全体の役に立ちます。

## <a name="create-quality-issues"></a>品質の Issue を作成する

Microsoft のドキュメントは、引き続き進行中の内容です。 適切な Issue は、Microsoft がコミュニティにとって優先度の高い内容に注力するために役立ちます。 詳細を提供すればするほど、Issue の役に立ちます。 探索した情報を教えてください。 使用した検索語句を教えてください。 使用を開始できない場合は、慣れていないテクノロジの探索をどのように始めたいかをお聞かせください。

Issue により、必要な内容についての会話が始まります。 コンテンツ チームは、追加できる内容のアイデアを用いて、これらの Issue に対応し、ご意見を伺います。 Microsoft でドラフトを作成した場合、お客様に [PR のレビュー](#review-open-prs)を依頼します。

## <a name="get-more-involved"></a>深く関わる

その他のトピックは、Microsoft Docs で生産的に投稿を開始するのに役立ちます。これらのトピックでは、Microsoft Docs プラットフォームで使用される GitHub リポジトリ、Markdown ツール、拡張機能の使い方について説明します。
