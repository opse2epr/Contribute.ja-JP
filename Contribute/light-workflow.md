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
# <a name="github-contribution-workflow-for-minor-or-infrequent-changes"></a><span data-ttu-id="ff594-103">軽微な変更や低頻度の変更の GitHub 共同作成ワークフロー</span><span class="sxs-lookup"><span data-stu-id="ff594-103">GitHub contribution workflow for minor or infrequent changes</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ff594-104">docs.microsoft.com に公開されるすべてのリポジトリには、「[Microsoft Open Source Code of Conduct (Microsoft オープンソース倫理規定)](https://opensource.microsoft.com/codeofconduct/)」または「[.NET Foundation Code of Conduct (.NET Foundation 倫理規定)](https://dotnetfoundation.org/code-of-conduct)」が適用されています。</span><span class="sxs-lookup"><span data-stu-id="ff594-104">All repositories that publish to docs.microsoft.com have adopted either the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/) or the [.NET Foundation Code of Conduct](https://dotnetfoundation.org/code-of-conduct).</span></span> <span data-ttu-id="ff594-105">詳細については、「[Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/)」 (倫理規定に関する FAQ) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ff594-105">For more information, see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/).</span></span> <span data-ttu-id="ff594-106">または、ご質問やコメントがある場合は、[opencode@microsoft.com](mailto:opencode@microsoft.com) または [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org) までご連絡ください。</span><span class="sxs-lookup"><span data-stu-id="ff594-106">Or contact [opencode@microsoft.com](mailto:opencode@microsoft.com), or [conduct@dotnetfoundation.org](mailto:conduct@dotnetfoundation.org) with any questions or comments.</span></span><br>
>
> <span data-ttu-id="ff594-107">パブリック リポジトリ内にあるドキュメントおよびコード例の軽微な修正や補足は、「[docs.microsoft.com - 使用条件](https://docs.microsoft.com/legal/termsofuse)」の対象になります。</span><span class="sxs-lookup"><span data-stu-id="ff594-107">Minor corrections or clarifications to documentation and code examples in public repositories are covered by the [docs.microsoft.com Terms of Use](https://docs.microsoft.com/legal/termsofuse).</span></span> <span data-ttu-id="ff594-108">Microsoft の従業員ではない共同作成者が新規または大幅な変更を行うと、オンライン貢献者使用許諾契約書 (CLA) の提出をお願いするコメントがプル要求内に生成されます。</span><span class="sxs-lookup"><span data-stu-id="ff594-108">New or significant changes will generate a comment in the pull request, asking you to submit an online Contribution License Agreement (CLA) if you are not an employee of Microsoft.</span></span> <span data-ttu-id="ff594-109">プル要求が正しく受理されるように、オンライン フォームへのご記入をお願いいたします。</span><span class="sxs-lookup"><span data-stu-id="ff594-109">We need you to complete the online form before we can accept your pull request.</span></span>

## <a name="overview"></a><span data-ttu-id="ff594-110">概要</span><span class="sxs-lookup"><span data-stu-id="ff594-110">Overview</span></span>

<span data-ttu-id="ff594-111">このワークフローは、GitHub の Web ベースの Markdown エディターを使用しており、軽微な変更や低頻度の変更を行う場合に適しています。</span><span class="sxs-lookup"><span data-stu-id="ff594-111">This workflow is suitable for making minor or infrequent changes, by using GitHub's web-based Markdown editor.</span></span> <span data-ttu-id="ff594-112">GitHub エディターは、UI が一部の Git 操作および作成シナリオをサポートしていないため、実行できることに関して制限があります。</span><span class="sxs-lookup"><span data-stu-id="ff594-112">The GitHub editor is limited in terms of what you can do, because the UI does not support all Git operations and authoring scenarios.</span></span> <span data-ttu-id="ff594-113">大規模な共同作成を行う必要がある場合、または Git の高度な機能 (ブランチ管理や高度なマージの競合の解決など) に対するサポートが必要な場合は、[大規模な変更や長期にわたる変更のワークフロー](full-workflow.md)に関する記事をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="ff594-113">If you need to make large contributions, or you need support for advanced Git features (such as branch management or advanced merge conflict resolution), refer to the [major or long-running changes workflow](full-workflow.md).</span></span>

## <a name="procedure-for-using-the-github-editor-to-propose-your-changes"></a><span data-ttu-id="ff594-114">GitHub エディターを使用した変更の提案の手順</span><span class="sxs-lookup"><span data-stu-id="ff594-114">Procedure for using the GitHub editor to propose your changes</span></span>

1. <span data-ttu-id="ff594-115">記事に対応する GitHub リポジトリと Markdown ファイルを参照します。</span><span class="sxs-lookup"><span data-stu-id="ff594-115">Browse to the article's corresponding GitHub repository and Markdown file.</span></span> <span data-ttu-id="ff594-116">次のいずれかの方法を使用できます。</span><span class="sxs-lookup"><span data-stu-id="ff594-116">You can use either of the following methods:</span></span>

   - <span data-ttu-id="ff594-117">関連する GitHub リポジトリで Markdown ファイルを参照して、記事を探します。</span><span class="sxs-lookup"><span data-stu-id="ff594-117">Find the article by browsing through the Markdown files in the related GitHub repository.</span></span>
   - <span data-ttu-id="ff594-118">[docs.microsoft.com/](https://docs.microsoft.com/) の記事にアクセスし、ページ右上隅の **[編集]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ff594-118">Go to the article on [docs.microsoft.com](https://docs.microsoft.com/) and select the **Edit** link in the upper-right corner of the page.</span></span>

     ![[編集] リンクの場所](./media/light-workflow/contributetogit.png)

2. <span data-ttu-id="ff594-120">**[このファイルの編集]** 鉛筆アイコンを選択して、編集モードにします。</span><span class="sxs-lookup"><span data-stu-id="ff594-120">Select the **Edit this file** pencil icon to go into edit mode:</span></span>

    ![鉛筆アイコンの場所](./media/light-workflow/editicon.png)

3. <span data-ttu-id="ff594-122">**[ファイルの編集]** タブで Markdown を使用して変更を行い、**[変更のプレビュー]** タブで変更をプレビューします。エディターの使用方法は非常にわかりやすいものですが、サポートが必要な場合は、次のガイドをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="ff594-122">Make changes by using Markdown on the **Edit file** tab, and preview your changes on the **Preview changes** tab. Using the editor is fairly straightforward, but if you need assistance, see the following guides:</span></span>

   - [<span data-ttu-id="ff594-123">Markdown の使用方法</span><span class="sxs-lookup"><span data-stu-id="ff594-123">How to use Markdown</span></span>](how-to-write-use-markdown.md)
   - [<span data-ttu-id="ff594-124">Creating files on GitHub (GitHub でファイルを作成する)</span><span class="sxs-lookup"><span data-stu-id="ff594-124">Creating files on GitHub</span></span>](https://github.com/blog/1327-creating-files-on-github)
   - [<span data-ttu-id="ff594-125">Upload files to your repositories (リポジトリにファイルをアップロードする)</span><span class="sxs-lookup"><span data-stu-id="ff594-125">Upload files to your repositories</span></span>](https://github.com/blog/2105-upload-files-to-your-repositories)

4. <span data-ttu-id="ff594-126">次のいずれかが表示されるまで、ページ下部にスクロールします。</span><span class="sxs-lookup"><span data-stu-id="ff594-126">Scroll to the bottom of the page, where you see one of the following:</span></span>

   - <span data-ttu-id="ff594-127">**[Propose file change]\(ファイル変更の提案\)**: [他のユーザーのリポジトリのファイルの編集](https://help.github.com/articles/editing-files-in-another-user-s-repository/)など、リポジトリへの読み取り専用アクセスを持つ場合に表示されます。</span><span class="sxs-lookup"><span data-stu-id="ff594-127">**Propose file change**: Appears when you have read-only access to the repository, such as [editing files in another user's repository](https://help.github.com/articles/editing-files-in-another-user-s-repository/).</span></span> <span data-ttu-id="ff594-128">この場合、GitHub によって、リポジトリのフォークに "パッチ" ブランチが作成されます (また、フォークが存在しない場合は自動的に作成されます)。</span><span class="sxs-lookup"><span data-stu-id="ff594-128">In this case, GitHub will create a "patch" branch in your fork of the repository (and automatically create a fork if it doesn't exist).</span></span> <span data-ttu-id="ff594-129">**[Propose file change ]\(ファイル変更の提案\)** を選択すると、**[Comparing changes]\(変更の比較\)** ページが表示され、変更を確認できます。</span><span class="sxs-lookup"><span data-stu-id="ff594-129">After you select **Propose file change**, a **Comparing changes** page appears so you can verify your changes.</span></span> <span data-ttu-id="ff594-130">その後、[[プル要求の作成]](#pull-request-processing) を選択してプル要求キューに変更を送信し、**次のセクション**に進みます。</span><span class="sxs-lookup"><span data-stu-id="ff594-130">Then select the **Create pull request** button to submit your changes to the pull request queue, and proceed to the [next section](#pull-request-processing).</span></span>

   - <span data-ttu-id="ff594-131">**[変更の確定]**: [独自のリポジトリのファイルの編集](https://help.github.com/articles/editing-files-in-your-repository/)など、リポジトリへの書き込みのアクセス許可を持つ場合に表示されます。</span><span class="sxs-lookup"><span data-stu-id="ff594-131">**Commit changes**: Appears when you have write permissions to a repository, such as [editing files in your own repository](https://help.github.com/articles/editing-files-in-your-repository/).</span></span> <span data-ttu-id="ff594-132">この場合、GitHub によって、変更を保存するための 2 つのオプションが示されます。</span><span class="sxs-lookup"><span data-stu-id="ff594-132">In this case, GitHub gives you two options for saving your changes:</span></span>

     - <span data-ttu-id="ff594-133">**`<branch-name>` ブランチに直接コミット**します。ここで、`<branch-name>` は **[編集]** ボタンを選択したときの現在のブランチの名前です。</span><span class="sxs-lookup"><span data-stu-id="ff594-133">**Commit directly to the `<branch-name>` branch**, where `<branch-name>` is the name of the branch that you were on when you selected the **Edit** button.</span></span> <span data-ttu-id="ff594-134">これにより、プル要求を使用せずに、ブランチに直接変更が適用されます。</span><span class="sxs-lookup"><span data-stu-id="ff594-134">This applies your changes directly to the branch instead of using a pull request.</span></span> <span data-ttu-id="ff594-135">これで完了です。</span><span class="sxs-lookup"><span data-stu-id="ff594-135">At this point, you're finished!</span></span>

     - <span data-ttu-id="ff594-136">**このコミットに対して新しいブランチを作成してプル要求を開始**します。この場合、既定の名前とともに、新しいブランチを作成するためのプロンプトが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ff594-136">**Create a new branch for this commit and start a pull request**, which prompts you with a default name to create a new branch.</span></span> <span data-ttu-id="ff594-137">**[Propose file change ]\(ファイル変更の提案\)** を選択すると、**[Comparing changes]\(変更の比較\)** ページが表示され、変更を確認できます。</span><span class="sxs-lookup"><span data-stu-id="ff594-137">After you select **Propose file change**, a **Comparing changes** page appears so you can verify your changes.</span></span> <span data-ttu-id="ff594-138">その後、[[プル要求の作成]](#pull-request-processing) を選択してプル要求キューに変更を送信し、**次のセクション**に進みます。</span><span class="sxs-lookup"><span data-stu-id="ff594-138">Then select the **Create pull request** button to submit your changes to the pull request queue, and proceed to the [next section](#pull-request-processing).</span></span>

[!INCLUDE[contribute-how-to-write-workflows-pull-request-processing](includes/contribute-how-to-write-workflows-pull-request-processing.md)]

## <a name="next-steps"></a><span data-ttu-id="ff594-139">次のステップ</span><span class="sxs-lookup"><span data-stu-id="ff594-139">Next steps</span></span>

- <span data-ttu-id="ff594-140">Markdown や Markdown 拡張構文などについての知識を深めるには、「Writing essentials」 (書き方の要点) の記事に進んでください。</span><span class="sxs-lookup"><span data-stu-id="ff594-140">Continue to the "Writing essentials" articles to learn more about Markdown, Markdown extensions syntax, and more.</span></span>
