---
title: 軽微な変更や低頻度の変更の GitHub 共同作成ワークフロー
description: この記事では、"軽微な" 共同作成者向けのワークフローを利用して docs.microsoft.com の記事を作成する方法について説明します。
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 10/06/2017
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 8bde44d502e1942b0870df9dd546a97705c2bb4f
ms.sourcegitcommit: de6e6b6ca641fdd5b30eb46deee9ac3a500089ef
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2018
---
# <a name="github-contribution-workflow-for-minor-or-infrequent-changes"></a>軽微な変更や低頻度の変更の GitHub 共同作成ワークフロー

> [!IMPORTANT]
> docs.microsoft.com に公開されるすべてのリポジトリには、「[Microsoft Open Source Code of Conduct (Microsoft オープンソース倫理規定)](https://opensource.microsoft.com/codeofconduct/)」または「[.NET Foundation Code of Conduct (.NET Foundation 倫理規定)](https://dotnetfoundation.org/code-of-conduct)」が適用されています。 詳細については、「[Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/)」 (倫理規定に関する FAQ) を参照してください。 または、ご質問やコメントがある場合は、[opencode@microsoft.com](mailto:opencode@microsoft.com) または [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org) までご連絡ください。<br>
>
> パブリック リポジトリ内にあるドキュメントおよびコード例の軽微な修正や補足は、「[docs.microsoft.com - 使用条件](https://docs.microsoft.com/legal/termsofuse)」の対象になります。 Microsoft の従業員ではない共同作成者が新規または大幅な変更を行うと、オンライン貢献者使用許諾契約書 (CLA) の提出をお願いするコメントがプル要求内に生成されます。 プル要求が正しく受理されるように、オンライン フォームへのご記入をお願いいたします。

## <a name="overview"></a>概要

このワークフローは、GitHub の Web ベースの Markdown エディターを使用しており、軽微な変更や低頻度の変更を行う場合に適しています。 GitHub エディターは、UI が一部の Git 操作および作成シナリオをサポートしていないため、実行できることに関して制限があります。 大規模な共同作成を行う必要がある場合、または Git の高度な機能 (ブランチ管理や高度なマージの競合の解決など) に対するサポートが必要な場合は、[大規模な変更や長期にわたる変更のワークフロー](full-workflow.md)に関する記事をご覧ください。

## <a name="procedure-for-using-the-github-editor-to-propose-your-changes"></a>GitHub エディターを使用した変更の提案の手順

1. 記事に対応する GitHub リポジトリと Markdown ファイルを参照します。 次のいずれかの方法を使用できます。

   - 関連する GitHub リポジトリで Markdown ファイルを参照して、記事を探します。
   - [docs.microsoft.com/](https://docs.microsoft.com/) の記事にアクセスし、ページ右上隅の **[編集]** を選択します。

     ![[編集] リンクの場所](./media/light-workflow/contributetogit.png)

2. **[このファイルの編集]** 鉛筆アイコンを選択して、編集モードにします。

    ![鉛筆アイコンの場所](./media/light-workflow/editicon.png)

3. **[ファイルの編集]** タブで Markdown を使用して変更を行い、**[変更のプレビュー]** タブで変更をプレビューします。エディターの使用方法は非常にわかりやすいものですが、サポートが必要な場合は、次のガイドをご覧ください。

   - [Markdown の使用方法](how-to-write-use-markdown.md)
   - [Creating files on GitHub (GitHub でファイルを作成する)](https://github.com/blog/1327-creating-files-on-github)
   - [Upload files to your repositories (リポジトリにファイルをアップロードする)](https://github.com/blog/2105-upload-files-to-your-repositories)

4. 次のいずれかが表示されるまで、ページ下部にスクロールします。

   - **[Propose file change]\(ファイル変更の提案\)**: [他のユーザーのリポジトリのファイルの編集](https://help.github.com/articles/editing-files-in-another-user-s-repository/)など、リポジトリへの読み取り専用アクセスを持つ場合に表示されます。 この場合、GitHub によって、リポジトリのフォークに "パッチ" ブランチが作成されます (また、フォークが存在しない場合は自動的に作成されます)。 **[Propose file change ]\(ファイル変更の提案\)** を選択すると、**[Comparing changes]\(変更の比較\)** ページが表示され、変更を確認できます。 その後、[[プル要求の作成]](#pull-request-processing) を選択してプル要求キューに変更を送信し、**次のセクション**に進みます。

   - **[変更の確定]**: [独自のリポジトリのファイルの編集](https://help.github.com/articles/editing-files-in-your-repository/)など、リポジトリへの書き込みのアクセス許可を持つ場合に表示されます。 この場合、GitHub によって、変更を保存するための 2 つのオプションが示されます。

     - **`<branch-name>` ブランチに直接コミット**します。ここで、`<branch-name>` は **[編集]** ボタンを選択したときの現在のブランチの名前です。 これにより、プル要求を使用せずに、ブランチに直接変更が適用されます。 これで完了です。

     - **このコミットに対して新しいブランチを作成してプル要求を開始**します。この場合、既定の名前とともに、新しいブランチを作成するためのプロンプトが表示されます。 **[Propose file change ]\(ファイル変更の提案\)** を選択すると、**[Comparing changes]\(変更の比較\)** ページが表示され、変更を確認できます。 その後、[[プル要求の作成]](#pull-request-processing) を選択してプル要求キューに変更を送信し、**次のセクション**に進みます。

[!INCLUDE[contribute-how-to-write-workflows-pull-request-processing](includes/contribute-how-to-write-workflows-pull-request-processing.md)]

## <a name="next-steps"></a>次のステップ

- Markdown や Markdown 拡張構文などについての知識を深めるには、「Writing essentials」 (書き方の要点) の記事に進んでください。
