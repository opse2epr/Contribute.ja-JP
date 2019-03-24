---
title: Microsoft Docs 共同作成者ガイド概要
description: このガイドでは、Microsoft ドキュメント サイト docs.microsoft.com で協力する方法について説明します。
author: billwagner
ms.author: wiwagn
ms.date: 02/19/2019
---

# <a name="microsoft-docs-contributor-guide-overview"></a>Microsoft Docs 共同作成者ガイド概要

[docs.microsoft.com](https://docs.microsoft.com) (Docs) 共同作成者ガイドへようこそ。

Microsoft のドキュメント セットには、オープン ソースで GitHub 上でホストされているのものがいくつかあります。 一部のドキュメント セットは完全にオープン ソースではありませんが、多くのものは一般公開用のリポジトリを持ち、pull request を作成できます。 これを使用すると、製品エンジニア、コンテンツ チーム、顧客との間のコミュニケーションが効率化され改善されます。 オープン環境で作業すると、次のようないくつかの利点があります。

- 最も必要なドキュメントに関するフィードバックを取得するために、_開かれたオープン ソースのリポジトリのプラン_
- 最初のリリースで最も役立つコンテンツを公開するために、_開かれたオープン ソースのリポジトリのレビュー_
- コンテンツを継続して改善しやすくするために、_開かれたオープン ソースのリポジトリの更新_

[docs.microsoft.com](https://docs.microsoft.com) のユーザー エクスペリエンスは、より操作しやすいように、[GitHub](https://github.com) のワークフローに直接統合されています。 [表示しているドキュメントを編集](#quick-edits-to-existing-documents)して開始します。 または、[新しいトピックをレビュー](#review-open-prs)して支援するか、[品質の Issue を作成します](#create-quality-issues)。

> [!IMPORTANT]
> docs.microsoft.com に公開されるすべてのリポジトリには、「[Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/)」 (Microsoft オープン ソース倫理規定) または「[.NET Foundation Code of Conduct](https://dotnetfoundation.org/code-of-conduct)」 (.NET Foundation 倫理規定) が適用されています。 詳細については、「[Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/)」 (倫理規定に関する FAQ) を参照してください。 または、ご質問やコメントがある場合は、[opencode@microsoft.com](mailto:opencode@microsoft.com) または [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org) までご連絡ください。<br>
>
> パブリック リポジトリ内にあるドキュメントおよびコード例の軽微な修正や補足は、「[docs.microsoft.com - 使用条件](https://docs.microsoft.com/legal/termsofuse)」の対象になります。 Microsoft の従業員ではない共同作成者が新規または大幅な変更を加えた場合、オンライン貢献者使用許諾契約書 (CLA) の提出を要求するコメントが pull request 内に生成されます。 pull request をレビューまたは承認できるように、オンライン フォームへのご記入をお願いいたします。

## <a name="quick-edits-to-existing-documents"></a>既存のドキュメントへのクイック編集

クイック編集はプロセスを効率化し、ドキュメント内の小さなエラーや省略を報告および修正します。 さまざまな努力を重ねても、文章校正やスペルチェックの小さなエラーは公開されたドキュメントに_入り込みます_。 問題を作成して間違いを報告できますが、pull request (PR) を作成して問題を修正する方が速くて簡単です (このオプションを利用できる場合)。

1. 一部のドキュメント ページでは、ブラウザー内でコンテンツを直接編集できます。 その場合、以下に示すような **[編集]** ボタンが表示されます。 **[編集]** (または同等のローカライズされた) ボタンをクリックすると、GitHub 上のソース ファイルに移動します。 **[編集]** ボタン (テキストのない鉛筆アイコン) がない場合は、そのドキュメント ページを変更することはできません。

   ![[編集] リンクの場所](./media/index/edit-article.png)

2. 次に、鉛筆アイコンをクリックして、以下のように記事を編集します。 鉛筆アイコンが灰色表示されている場合は、GitHub アカウントにログインするか、新しいアカウントを作成する必要があります。 

   ![鉛筆アイコンの場所](./media/index/edit-icon.png)


3. Web エディターで変更を加えます。 **[変更のプレビュー]** タブをクリックし、ご自分の変更の書式設定を確認します。

4. 変更を加えたら、ページの一番下へスクロールします。 次の図に示すように、ご自分の変更にタイトルと説明を入力して、**[Propose file change]\(ファイル変更の提案\)** をクリックします。

   ![ファイル変更の提案](./media/index/submit-pull-request.png)

5. これで変更を提案したので、リポジトリの所有者に、変更をそのリポジトリに「pull」するように要求する必要があります。 これを完了するには、「pull request」と呼ばれる作業を実行します。 上の図の **[Propose file change ]\(ファイル変更の提案\)** をクリックしたら、次の図のような新しいページに移動しているはずです。

   ![Pull request の作成](media/index/create-pull-request.png)

   **[Create pull request]\(pull request の作成)** をクリックして pull request のタイトル (および必要に応じて説明) を入力した後、もう一度 **[Create pull request]** をクリックします。 (GitHub を初めてお使いの場合、詳細については、「[About Pull Requests](https://help.github.com/en/articles/about-pull-requests)」 (pull request について) を参照してください。)

6. これで終了です。 コンテンツ チームのメンバーが、PR をレビューしてマージします。 大規模な変更を加えた場合、変更を要求するフィードバックを受け取る可能性があります。

GitHub の UI の編集は、リポジトリ上の自分のアクセス許可に対応しています。 前の図は、ターゲットのリポジトリへの書き込みアクセス許可がない共同作成者に対して正確な図です。 GitHub では、お使いのアカウントに対象のリポジトリのフォークが自動的に作成されます。 対象のリポジトリへの書き込みアクセス権がある場合、GitHub では対象のリポジトリに新しいブランチが作成されます。 ブランチ名には、GitHub ID、およびパッチのブランチに対する数値識別子を使用する、フォーム **\<GitHubId\>-patch-n** が含まれます。

Microsoft では、書き込みアクセス権がある共同作成者も含めて、すべての変更に対して pull request を使用します。 ほとんどのリポジトリに保護された `master` ブランチがあるため、更新を pull request として提出する必要があります。

ブラウザー内の編集操作は、軽微な変更や頻度の低い変更に最適です。 大規模な共同作成を行う場合、または Git の高度な機能 (ブランチ管理や高度なマージの競合の解決など) を使用する場合は、[リポジトリをフォークしてローカルで作業する](how-to-write-workflows-major.md)必要があります。

> [!NOTE]
> 可能であれば、**任意の言語**で記事を編集できます。また、編集の種類に基づいて、次のことが起こります。
> 1. 言語に関する変更が承認されると、機械翻訳エンジンも改善されます。
> 2. 編集が記事のコンテンツを大幅に変更する場合、それは内部で処理されて、同じ記事の英語版に変更が送信されます。このため、承認された場合はすべての言語でローカライズされます。
> したがって、提案された改善は、自身の言語の記事を改善するだけでなく、利用可能なすべての言語に影響を与えます。

## <a name="review-open-prs"></a>開いている PR をレビューする

現在、開いている PR を確認して公開する前に、新しいトピックを確認することができます。 レビューは [GitHub のフロー](https://guides.github.com/introduction/flow/) プロセスに従います。 パブリック リポジトリにある提案された更新や新しい記事を確認できます。 それらをレビューしてコメントを追加します。 ドキュメント リポジトリのいずれかを参照し、関心のあるエリアの開いている pull requests (PR) を確認します。 提案された更新のコミュニティ フィードバックは、コミュニティ全体の役に立ちます。

## <a name="create-quality-issues"></a>品質の Issue を作成する

Microsoft のドキュメントは、引き続き進行中の内容です。 適切な Issue は、Microsoft がコミュニティにとって優先度の高い内容に注力するために役立ちます。 詳細を提供すればするほど、Issue の役に立ちます。 探索した情報を教えてください。 使用した検索語句を教えてください。 始めることができない場合は、慣れ親しんでいないテクノロジの探索をどのように始めたいかを教えてください。

Microsoft のドキュメント ページの多くには、ページの下部に**フィードバック** セクションがあります。ここでは、**[製品のフィードバック]** または **[コンテンツに関するフィードバック]** をクリックしてそれらを残し、その記事に固有の問題を追跡することができます。

Issue により、必要な内容についての会話が始まります。 コンテンツ チームは、追加できる内容のアイデアを用いて、これらの Issue に対応し、ご意見を伺います。 Microsoft でドラフトを作成した場合、お客様に [PR のレビュー](#review-open-PRs)を依頼します。

## <a name="get-more-involved"></a>深く関わる

その他のトピックは、Microsoft Docs で生産的に投稿を開始するのに役立ちます。これらのトピックでは、Microsoft Docs プラットフォームで使用される GitHub リポジトリ、Markdown ツール、拡張機能の使い方について説明します。
