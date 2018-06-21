---
title: コンテンツ オーサリング ツールのインストール
description: この記事は、Git、および Markdown ファイルの編集に必要なクライアント ツールのダウンロードとインストールに役立ちます。
author: jasonwhowell
ms.author: jasonh
manager: kfile
ms.date: 04/30/2018
ms.openlocfilehash: 00631485f1f4eed9e0de2f6df98d973a819dfe4d
ms.sourcegitcommit: 92aef5ea8bdd692c5c393d5c8f99b9e4f672ef2b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/19/2018
ms.locfileid: "36238922"
---
# <a name="install-content-authoring-tools"></a><span data-ttu-id="fd31c-103">コンテンツ オーサリング ツールのインストール</span><span class="sxs-lookup"><span data-stu-id="fd31c-103">Install content authoring tools</span></span>

<span data-ttu-id="fd31c-104">この記事では、Git クライアント ツールと Visual Studio Code を対話形式でインストールする手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="fd31c-104">This article describes the steps to interactively install Git client tools and Visual Studio Code.</span></span>
> [!div class="checklist"]
> * <span data-ttu-id="fd31c-105">[Git for Windows](https://git-scm.com/download/win) をインストールする</span><span class="sxs-lookup"><span data-stu-id="fd31c-105">Install [Git for Windows](https://git-scm.com/download/win)</span></span>
> * <span data-ttu-id="fd31c-106">[Visual Studio Code](https://code.visualstudio.com/) をインストールする</span><span class="sxs-lookup"><span data-stu-id="fd31c-106">Install [Visual Studio Code](https://code.visualstudio.com/)</span></span>
> * <span data-ttu-id="fd31c-107">[Docs Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) をインストールする</span><span class="sxs-lookup"><span data-stu-id="fd31c-107">Install [Docs Authoring Pack](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)</span></span>

>[!IMPORTANT]
> <span data-ttu-id="fd31c-108">記事に軽微な変更しか加えていない場合は、この記事の手順を実行する必要は*ない*ため、直接[簡易な変更のワークフロー](index.md#quick-edits-to-existing-documents)に進めます。</span><span class="sxs-lookup"><span data-stu-id="fd31c-108">If you're making only minor changes to an article, you *do not* need to complete the steps in this article and can continue directly to the [quick changes workflow](index.md#quick-edits-to-existing-documents).</span></span>
>
> <span data-ttu-id="fd31c-109">大規模な変更を行う共同作成者は、これらの手順を実行することをお勧めします。そうすることで、[大規模/長期間の変更のワークフロー](how-to-write-workflows-major.md)を使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="fd31c-109">Major contributors are encouraged to complete these steps, which enable you to use the [major/long-running changes workflow](how-to-write-workflows-major.md).</span></span> <span data-ttu-id="fd31c-110">メイン リポジトリで書き込みアクセス許可を持っている場合でも、"*リポジトリのフォークと複製を行うことを強くお勧めします (本ガイドでもそれを前提としています)*"。それにより、予定している変更をフォークに保存するための読み取り/書き込み権限が付与されます。</span><span class="sxs-lookup"><span data-stu-id="fd31c-110">Even if you have write permissions in the main repository, *we highly recommend (and this guide assumes) that you fork and clone the repository*, so that you have read/write permissions to store your proposed changes in your fork.</span></span>

## <a name="install-git-client-tools-on-windows"></a><span data-ttu-id="fd31c-111">Git クライアント ツールを Windows にインストールする</span><span class="sxs-lookup"><span data-stu-id="fd31c-111">Install Git client tools on Windows</span></span>

 <span data-ttu-id="fd31c-112">[Software Freedom Conservancy の Git クライアント ツール](https://git-scm.com/download/)の最新バージョンをインストールします。</span><span class="sxs-lookup"><span data-stu-id="fd31c-112">Install the latest version of [Software Freedom Conservancy's Git client tools](https://git-scm.com/download/).</span></span> <span data-ttu-id="fd31c-113">インストールには、Git バージョン管理システムや、ローカル Git リポジトリとの対話で使用するコマンドライン アプリである Git Bash が含まれます。</span><span class="sxs-lookup"><span data-stu-id="fd31c-113">The install includes the Git version control system and Git Bash, the command-line app that you use to interact with your local Git repository.</span></span>

<span data-ttu-id="fd31c-114">コマンド ライン インターフェイス (CLI) ではなくグラフィカル ユーザー インターフェイス (GUI) を使用する場合は、[Software Freedom Conservancy の使用可能な GUI クライアントに関するページ](https://git-scm.com/downloads/guis)、[GitHub の GitHub デスクトップ](https://desktop.github.com/)に関するページ、[Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx) のページで、一部の一般的なオプションを確認してください。</span><span class="sxs-lookup"><span data-stu-id="fd31c-114">If you prefer a graphical user interface (GUI) over a command-line interface (CLI), see [Software Freedom Conservancy's available GUI Clients page](https://git-scm.com/downloads/guis), [GitHub's GitHub Desktop](https://desktop.github.com/), or [Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx) for some popular options.</span></span>

<span data-ttu-id="fd31c-115">選択したクライアントについてインストールと構成の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="fd31c-115">Follow the instructions for your chosen client for installation and configuration.</span></span>

<span data-ttu-id="fd31c-116">次の記事では、[ローカル Git リポジトリを設定](get-started-setup-local.md)します。</span><span class="sxs-lookup"><span data-stu-id="fd31c-116">In the next article, you will [Set up a local Git repository](get-started-setup-local.md).</span></span>

   <span data-ttu-id="fd31c-117">Git の追加のリソースは、[Git 用語集](https://help.github.com/articles/github-glossary) | [Git の基礎](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics) | [Git および GitHub の学習](https://help.github.com/articles/good-resources-for-learning-git-and-github/)にあります</span><span class="sxs-lookup"><span data-stu-id="fd31c-117">Additional Git resources are available here: [Git terminology](https://help.github.com/articles/github-glossary) | [Git basics](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics) | [Learning Git and GitHub](https://help.github.com/articles/good-resources-for-learning-git-and-github/)</span></span>

## <a name="understand-markdown-editors"></a><span data-ttu-id="fd31c-118">Markdown エディターについて</span><span class="sxs-lookup"><span data-stu-id="fd31c-118">Understand Markdown editors</span></span>

<span data-ttu-id="fd31c-119">Markdown は、読みやすく、かつ習得しやすい軽量のマークアップ言語です。</span><span class="sxs-lookup"><span data-stu-id="fd31c-119">Markdown is a lightweight markup language that is both easy to read and easy to learn.</span></span> <span data-ttu-id="fd31c-120">そのため、急速に業界標準になりました。</span><span class="sxs-lookup"><span data-stu-id="fd31c-120">Therefore, it has rapidly become an industry standard.</span></span> <span data-ttu-id="fd31c-121">Markdown で記事を書くには、まず、Markdown エディターをダウンロードしてインストールすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="fd31c-121">To write articles in Markdown, we recommend that you first download and install a Markdown editor.</span></span>  <span data-ttu-id="fd31c-122">[Visual Studio Code](https://code.visualstudio.com/) は、Markdown を編集するために Microsoft が推奨しているツールです。</span><span class="sxs-lookup"><span data-stu-id="fd31c-122">[Visual Studio Code](https://code.visualstudio.com/) is the preferred tool for editing Markdown at Microsoft.</span></span> <span data-ttu-id="fd31c-123">[Atom](https://atom.io) も、Markdown を編集するための一般的なツールです。</span><span class="sxs-lookup"><span data-stu-id="fd31c-123">[Atom](https://atom.io) is another popular tool for editing Markdown.</span></span>

<span data-ttu-id="fd31c-124">Markdown テキストは、.md 拡張子の付いたファイルに保存されます。</span><span class="sxs-lookup"><span data-stu-id="fd31c-124">Markdown text is saved into files with .md extension.</span></span>

<span data-ttu-id="fd31c-125">Markdown の基本と OPS による Markdown のカスタム拡張機能でサポートされる機能を含む、Markdown での記述方法の詳細については、後述の「[Markdown の使用方法](how-to-write-use-markdown.md)」の記事で説明します。</span><span class="sxs-lookup"><span data-stu-id="fd31c-125">Additional details on how to write with Markdown, including Markdown basics and the features supported by OPS custom Markdown extensions, are covered later in the [How to use Markdown](how-to-write-use-markdown.md) article.</span></span>

## <a name="visual-studio-code"></a><span data-ttu-id="fd31c-126">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="fd31c-126">Visual Studio Code</span></span>

<span data-ttu-id="fd31c-127">[Visual Studio Code](https://code.visualstudio.com/) は Windows、Linux、Mac で動作する軽量のエディターで、VS Code とも呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="fd31c-127">[Visual Studio Code](https://code.visualstudio.com/), also known as VS Code, is a lightweight editor that works on Windows, Linux, and Mac.</span></span> <span data-ttu-id="fd31c-128">これには、git 統合と拡張機能のサポートが含まれています。</span><span class="sxs-lookup"><span data-stu-id="fd31c-128">It includes git integration, and support for extensions.</span></span>

<span data-ttu-id="fd31c-129">[VS Code](https://code.visualstudio.com/) をダウンロードしてインストールします。</span><span class="sxs-lookup"><span data-stu-id="fd31c-129">Download and install [VS Code](https://code.visualstudio.com/).</span></span> <span data-ttu-id="fd31c-130">VS Code のホーム ページでは、オペレーティング システムが正しく検出されます。</span><span class="sxs-lookup"><span data-stu-id="fd31c-130">The VS Code home page should detect your operating system correctly.</span></span>

- [<span data-ttu-id="fd31c-131">Windows</span><span class="sxs-lookup"><span data-stu-id="fd31c-131">Windows</span></span>](https://code.visualstudio.com/docs/setup/windows)
- [<span data-ttu-id="fd31c-132">Mac</span><span class="sxs-lookup"><span data-stu-id="fd31c-132">Mac</span></span>](https://code.visualstudio.com/docs/setup/mac)
- [<span data-ttu-id="fd31c-133">Linux</span><span class="sxs-lookup"><span data-stu-id="fd31c-133">Linux</span></span>](https://code.visualstudio.com/docs/setup/linux)

> [!TIP]
> <span data-ttu-id="fd31c-134">VS Code を起動し、現在のフォルダーを開き、コマンド ラインまたは bash シェルで `code .` コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="fd31c-134">To launch VS Code and open the current folder, run the command `code .` in the command line or bash shell.</span></span> <span data-ttu-id="fd31c-135">現在のフォルダーがローカル git リポジトリの一部である場合は、github 統合が Visual Studio Code に自動的に表示されます。</span><span class="sxs-lookup"><span data-stu-id="fd31c-135">If the current folder is part of a local git repo, the github integration appears in Visual Studio Code automatically.</span></span>

## <a name="docs-authoring-pack"></a><span data-ttu-id="fd31c-136">Docs Authoring Pack</span><span class="sxs-lookup"><span data-stu-id="fd31c-136">Docs Authoring Pack</span></span>
<span data-ttu-id="fd31c-137">Visual Studio Code 用に Docs Authoring Pack をインストールします。</span><span class="sxs-lookup"><span data-stu-id="fd31c-137">Install the Docs Authoring Pack for Visual Studio Code.</span></span> <span data-ttu-id="fd31c-138">この一連の拡張機能には、Markdown の記述に役立つ基本的な作成サポートやプレビュー機能が含まれているため、docs.microsoft.com サイトのスタイルで Markdown がどのように表示されるかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="fd31c-138">This set of extensions includes basic authoring assistance for help when writing Markdown, and a preview feature, so that you can see what the Markdown looks like in the style of the docs.microsoft.com site.</span></span>

   <span data-ttu-id="fd31c-139">この [Marketplace ページ](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)にアクセスして **[インストール]** を選択するか、VS Code ウィンドウの拡張機能の一覧で `docsmsft.docs-authoring-pack` を検索します。</span><span class="sxs-lookup"><span data-stu-id="fd31c-139">Visit this [marketplace page](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) and select **Install**, or search for `docsmsft.docs-authoring-pack` in your extensions list in the VS Code window.</span></span> 

   <span data-ttu-id="fd31c-140">Docs Authoring Pack にアクセスするには、VS Code 内で Alt+M を押します。</span><span class="sxs-lookup"><span data-stu-id="fd31c-140">The Docs Authoring Pack is accessible by pressing Alt+M inside of VS Code.</span></span> <span data-ttu-id="fd31c-141">ツール バーは既定で非表示ですが、表示できます。</span><span class="sxs-lookup"><span data-stu-id="fd31c-141">The toolbar is hidden by default but can be shown.</span></span> <span data-ttu-id="fd31c-142">VS Code の設定を編集し (Ctrl+コンマ)、ユーザー設定 `"markdown.showToolbar": true` を追加して、ツール バーを表示します。</span><span class="sxs-lookup"><span data-stu-id="fd31c-142">Edit the VS Code settings (Control+comma) and adding user setting `"markdown.showToolbar": true` to show the toolbar.</span></span>

   <span data-ttu-id="fd31c-143">詳しくは、[Docs Authoring Pack](how-to-write-docs-auth-pack.md) に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="fd31c-143">For more information, see the [Docs Authoring Pack](how-to-write-docs-auth-pack.md) page.</span></span>


## <a name="next-steps"></a><span data-ttu-id="fd31c-144">次のステップ</span><span class="sxs-lookup"><span data-stu-id="fd31c-144">Next steps</span></span>

<span data-ttu-id="fd31c-145">これで、[ローカル Git リポジトリを設定](get-started-setup-local.md)する準備が整いました。</span><span class="sxs-lookup"><span data-stu-id="fd31c-145">Now you are ready to [Set up a local Git repository](get-started-setup-local.md).</span></span>
