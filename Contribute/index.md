---
title: Microsoft Docs 共同作成者ガイド概要
description: このガイドでは、Microsoft ドキュメント サイト docs.microsoft.com で協力する方法について説明します。
author: billwagner
ms.author: wiwagn
ms.date: 02/19/2019
ms.openlocfilehash: 9b091f864f5191c9f7a00900ec11a4a1cffdb698
ms.sourcegitcommit: af37d44eb67daa2841959817cd205ec95db18cec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/29/2019
ms.locfileid: "58653507"
---
# <a name="microsoft-docs-contributor-guide-overview"></a>Microsoft Docs 共同作成者ガイド概要

[docs.microsoft.com](https://docs.microsoft.com) (Docs) 共同作成者ガイドへようこそ。

Microsoft のドキュメント セットには、オープン ソースで GitHub 上でホストされているのものがいくつかあります。 すべてのドキュメント セットが完全にオープン ソースであるわけではありませんが、多くには一般公開用のリポジトリが備わっていて、そこで pull request を使って提案された変更を加えることができます。 このようなオープン ソースのアプローチにより、製品エンジニア、コンテンツ チーム、およびお客様との間のコミュニケーションが合理化され、改善されます。また、その他の利点があります。

- オープン ソースのリポジトリにより "_一般公開された状態で計画を行う_" ことで、最も必要とされているドキュメントがどれであるかについてのフィードバックを得る。
- オープン ソースのリポジトリにより "_一般公開された状態でレビューを行う_" ことで、最も役に立つコンテンツを最初のリリースで公開する。
- オープン ソースのリポジトリにより "_一般公開された状態で更新を行う_" ことで、コンテンツの継続的な改善を容易にする。

[docs.microsoft.com](https://docs.microsoft.com) のユーザー エクスペリエンスには [GitHub](https://github.com) のワークフローが直接統合され、さらに簡単になっています。 まずは[表示しているドキュメントを編集](#quick-edits-to-existing-documents)してみましょう。 または、[新しいトピックをレビュー](#review-open-prs)して支援するか、[品質に関するイシューを作成します](#create-quality-issues)。

> [!IMPORTANT]
> docs.microsoft.com に公開されるすべてのリポジトリには、「[Microsoft Open Source Code of Conduct (Microsoft オープン ソース倫理規定)](https://opensource.microsoft.com/codeofconduct/)」または「[.NET Foundation Code of Conduct (.NET Foundation 倫理規定)](https://dotnetfoundation.org/code-of-conduct)」が適用されています。 詳細については、[倫理規定に関する FAQ](https://opensource.microsoft.com/codeofconduct/faq/) のページを参照してください。 または、ご質問やコメントがある場合は、[opencode@microsoft.com](mailto:opencode@microsoft.com) または [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org) までご連絡ください。<br>
>
> パブリック リポジトリにあるドキュメントおよびコード例に対する軽微な修正や明確化は、「[docs.microsoft.com - 使用条件](https://docs.microsoft.com/legal/termsofuse)」の対象になります。 Microsoft の従業員ではない場合、新規または大幅な変更を加えると、オンライン貢献者使用許諾契約書 (CLA) の提出を求めるコメントが pull request 内に生成されます。 ご自身の pull request に対するレビューや承認を可能にするには、オンライン フォームに入力する必要があります。

## <a name="quick-edits-to-existing-documents"></a>既存のドキュメントに対するクイック編集

クイック編集により、ドキュメント内の小さなエラーや省略を報告および修正するプロセスが合理化されます。 さまざまな努力を重ねても、公開されたドキュメントには文法やスペルに関する小さな誤りが "_必ず_" 入り込みます。 イシューを作成して間違いを報告することもできますが、利用可能な場合は、pull request (PR) を作成して問題を修正するオプションの方が速くて簡単です。

1. 一部のドキュメント ページでは、ブラウザー内でコンテンツを直接編集できます。 その場合、以下に示すような **[編集]** ボタンが表示されます。 **[編集]** (または同等にローカライズされた) ボタンをクリックすると、GitHub 上のソース ファイルに移動します。 **[編集]** ボタン (テキストなしの鉛筆アイコン) がない場合は、そのドキュメント ページを変更することはできません。

   ![[編集] リンクの場所](./media/index/edit-article.png)

2. 次に、鉛筆アイコンをクリックして、以下のように記事を編集します。 鉛筆アイコンが灰色表示されている場合は、自分の GitHub アカウントにログインするか、新しいアカウントを作成する必要があります。 

   ![鉛筆アイコンの場所](./media/index/edit-icon.png)


3. Web エディターで変更を加えます。 **[変更のプレビュー]** タブをクリックして、自分の変更の書式設定を確認します。

4. 変更を加えたら、ページの一番下までスクロールします。 次の図に示すように、自分の変更にタイトルと説明を入力して、 **[Propose file change]\(ファイル変更の提案\)** をクリックします。

   ![ファイル変更の提案](./media/index/submit-pull-request.png)

5. これで変更を提案したので、リポジトリの所有者に、変更をそのリポジトリに「pull」するように要求する必要があります。 これを完了するには、「pull request」と呼ばれる作業を実行します。 上の図の **[Propose file change ]\(ファイル変更の提案\)** をクリックした場合、次の図のような新しいページに移動しているはずです。

   ![pull request の作成](media/index/create-pull-request.png)

   **[Create pull request]\(pull request の作成)** をクリックし、pull request のタイトル (および必要に応じて説明) を入力した後、もう一度 **[Create pull request]\(pull request の作成)** をクリックします。 (GitHub を初めてお使いの場合、詳細については「[About Pull Requests (pull request について)](https://help.github.com/en/articles/about-pull-requests)」を参照してください。)

6. これで終了です。 コンテンツ チームのメンバーが、ご自分の PR をレビューしてマージします。 大規模な変更を加えた場合、変更を求めるフィードバックを受け取る可能性があります。

GitHub の編集用 UI は、リポジトリに対する自分のアクセス許可に対応しています。 上の図が正確になるのは、対象のリポジトリに対する書き込みアクセス許可がない共同作成者の場合です。 GitHub により、対象のリポジトリのフォークが自分のアカウント内に自動的に作成されます。 対象のリポジトリへの書き込みアクセス権がある場合は、GitHub により対象のリポジトリに新しいブランチが作成されます。 ブランチ名は **\<GitHubId\>-patch-n** という形式になり、ご自身の GitHub ID と、パッチのブランチ用の数値識別子が使われます。

書き込みアクセス権がある共同作成者の場合も、すべての変更に対して pull request が使われます。 更新が必ず pull request として提出されるように、ほとんどのリポジトリでは `master` ブランチが保護されています。

ブラウザー内の編集操作は、軽微または頻度の低い変更を行う場合に最適です。 大規模な共同作成を行う場合、または Git の高度な機能 (ブランチ管理や高度なマージ競合の解決など) を使用する場合は、[リポジトリをフォークしてローカルで作業する](how-to-write-workflows-major.md)必要があります。

> [!NOTE]
> 有効な場合、**任意の言語**で記事を編集できます。また、編集の種類に基づいて、次のことが起こります。
> 1. 承認された言語の変更は、Microsoft の機械翻訳エンジンの改善にも役立てられます
> 2. 編集によって記事のコンテンツを大幅に変更する場合、それは内部的に処理され、承認された場合はすべての言語でローカライズされるように、同じ記事の英語版に変更が送信されます。
> したがって、ご自分が提案した改善は、ご自身の言語だけでなく、利用可能なすべての言語の記事に良い影響を与えます。

## <a name="review-open-prs"></a>開いている PR をレビューする

現在開いている PR を確認することで、新しいトピックを公開前に読むことができます。 レビューは [GitHub フロー](https://guides.github.com/introduction/flow/)のプロセスに従います。 パブリック リポジトリにある提案された更新や新しい記事を閲覧できます。 それらをレビューしてコメントを追加します。 任意のドキュメント リポジトリを参照して、関心のある領域の開いている pull requests (PR) を確認してください。 提案された更新に対するコミュニティのフィードバックは、コミュニティ全体の役に立ちます。

## <a name="create-quality-issues"></a>品質に関するイシューを作成する

Microsoft のドキュメントは、進行中の継続的な作業です。 適切なイシューは、コミュニティの最優先事項に注力するために役立ちます。 提供する情報が詳細なほど、イシューは役立つものになります。 求めていた情報を教えてください。 使用した検索語句を教えてください。 使ったことがないテクノロジの探索を開始できない場合は、どのように開始したいかをお聞かせください。

Microsoft のドキュメント ページの多くには、ページの下部に**フィードバック** セクションがあります。ここでは、 **[製品のフィードバック]** または **[コンテンツに関するフィードバック]** をクリックしてそれらを残し、その記事に固有の問題を追跡することができます。

イシューによって、必要なことに関する会話が開始されます。 コンテンツ チームでは、追加できる内容のアイデアと共にこのようなイシューに対応し、ご意見を伺います。 ドラフトが作成されると、お客様に [PR のレビュー](#review-open-prs)が依頼されます。

## <a name="get-more-involved"></a>深く関わる

その他のトピックは、Microsoft Docs に対する共同作成を生産的に開始するのに役立ちます。これらでは、Microsoft Docs プラットフォームで使用される GitHub リポジトリ、Markdown ツール、および拡張機能の操作について説明しています。
