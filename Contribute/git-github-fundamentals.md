---
title: Git および GitHub のドキュメントの基礎
description: この記事では、Git、GitHub リポジトリの概要、コンテンツの編成、docs.microsoft.com で使用される命名規則について説明します。
ms.date: 06/30/2017
ms.openlocfilehash: 05c758845007f859382014166e88fd9614cdb873
ms.sourcegitcommit: d3c7b49dc854dae8da9cd49da8ac4035789a5010
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/23/2018
ms.locfileid: "49805702"
---
# <a name="git-and-github-essentials-for-docs"></a><span data-ttu-id="b5f22-103">Git および GitHub のドキュメントの基礎</span><span class="sxs-lookup"><span data-stu-id="b5f22-103">Git and GitHub essentials for Docs</span></span>

## <a name="overview"></a><span data-ttu-id="b5f22-104">概要</span><span class="sxs-lookup"><span data-stu-id="b5f22-104">Overview</span></span>

<span data-ttu-id="b5f22-105">Docs コンテンツの共同作成者は、複数のツールやプロセスを操作します。</span><span class="sxs-lookup"><span data-stu-id="b5f22-105">As a contributor to Docs content, you will interact with multiple tools and processes.</span></span> <span data-ttu-id="b5f22-106">同じプロジェクトで他の共同作成者と並行して作業を行います。まったく同じコンテンツで同時に作業を行う場合もあります。</span><span class="sxs-lookup"><span data-stu-id="b5f22-106">You'll work in parallel with other contributors on the same project, potentially the exact same content, even at the same time.</span></span> <span data-ttu-id="b5f22-107">これらのすべては Git と GitHub ソフトウェアによって実現します。</span><span class="sxs-lookup"><span data-stu-id="b5f22-107">This is all enabled through Git and GitHub software.</span></span>

<span data-ttu-id="b5f22-108">Git はオープン ソースのバージョン管理システムです。</span><span class="sxs-lookup"><span data-stu-id="b5f22-108">Git is an open-source version control system.</span></span> <span data-ttu-id="b5f22-109">*リポジトリ* に存在するファイルの*分散型バージョン管理* により、この種のプロジェクト コラボレーションを容易にします。</span><span class="sxs-lookup"><span data-stu-id="b5f22-109">It facilitates this type of project collaboration through *distributed version control* of files that live in *repositories*.</span></span> <span data-ttu-id="b5f22-110">要するに、Git を利用することで、特定のリポジトリを対象に複数の共同作成者によって長期間にわたって行われる一連の作業を統合できます。</span><span class="sxs-lookup"><span data-stu-id="b5f22-110">In essence, Git makes it possible to integrate streams of work done by multiple contributors over time, for a given repository.</span></span>

<span data-ttu-id="b5f22-111">GitHub は、[docs.microsoft.com](https://docs.microsoft.com) コンテンツの格納に使用しているような Git リポジトリの、Web ベースのホスティング サービスです。</span><span class="sxs-lookup"><span data-stu-id="b5f22-111">GitHub is a web-based hosting service for Git repositories, such as those used to store [docs.microsoft.com](https://docs.microsoft.com) content.</span></span> <span data-ttu-id="b5f22-112">GitHub は任意のプロジェクトのメイン リポジトリをホストします。共同作成者はこのメイン リポジトリから独自の作業用のコピーを作成できます </span><span class="sxs-lookup"><span data-stu-id="b5f22-112">For any project, GitHub hosts the main repository, from which contributors can make copies for their own work.</span></span>

## <a name="git"></a><span data-ttu-id="b5f22-113">Git</span><span class="sxs-lookup"><span data-stu-id="b5f22-113">Git</span></span>

<span data-ttu-id="b5f22-114">集中型バージョン管理システム (Team Foundation Server、SharePoint、Visual SourceSafe など) を使い慣れている場合、Git に分散型モデルをサポートする固有の共同作成ワークフローと用語があることに気付かれるでしょう。</span><span class="sxs-lookup"><span data-stu-id="b5f22-114">If you're familiar with centralized version control systems (such as Team Foundation Server, SharePoint, or Visual SourceSafe), you will notice that Git has a unique contribution workflow and terminology to support its distributed model.</span></span> <span data-ttu-id="b5f22-115">たとえば、通常はチェックアウト/チェックイン操作と関連するファイル ロックはありません。</span><span class="sxs-lookup"><span data-stu-id="b5f22-115">For instance, there is no file locking that is normally associated with check-out/check-in operations.</span></span> <span data-ttu-id="b5f22-116">実際のところ、Git では最小レベルの変更でさえも考慮されており、ファイルはバイト単位で比較されます。</span><span class="sxs-lookup"><span data-stu-id="b5f22-116">As a matter of fact, Git is concerned about changes at an even finer level, comparing files byte by byte.</span></span>

<span data-ttu-id="b5f22-117">また、Git では階層化された構造を使用して、プロジェクトのコンテンツを格納および管理します。</span><span class="sxs-lookup"><span data-stu-id="b5f22-117">Git also uses a tiered structure to store and manage content for a project:</span></span>

- <span data-ttu-id="b5f22-118">"*リポジトリ*" : これは"*リポ*" とも呼ばれる最上位の記憶域単位です。</span><span class="sxs-lookup"><span data-stu-id="b5f22-118">*Repository*: Also known as a *repo*, this is the highest unit of storage.</span></span> <span data-ttu-id="b5f22-119">リポジトリには 1 つまたは複数のブランチが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b5f22-119">A repository contains one or more branches.</span></span>
- <span data-ttu-id="b5f22-120">"*ブランチ*" : プロジェクトのコンテンツ セットを構成するファイルとフォルダーを含む記憶域単位。</span><span class="sxs-lookup"><span data-stu-id="b5f22-120">*Branch*: A unit of storage that contains the files and  folders that make up a project's content set.</span></span> <span data-ttu-id="b5f22-121">ブランチは作業ストリームを分離します (通常はバージョンと呼ばれる)。</span><span class="sxs-lookup"><span data-stu-id="b5f22-121">Branches separate streams of work (typically referred to as versions).</span></span> <span data-ttu-id="b5f22-122">共同作成の範囲は必ず特定のブランチに設定されます。</span><span class="sxs-lookup"><span data-stu-id="b5f22-122">Contributions are always made and scoped to a specific branch.</span></span> <span data-ttu-id="b5f22-123">すべてのリポジトリには、既定のブランチ (通常の名前は "マスター") と、マスター ブランチにマージされることになるブランチが 1 つまたは複数含まれます。</span><span class="sxs-lookup"><span data-stu-id="b5f22-123">All repositories contain a default branch (typically named "master") and one or more branches that are destined to be merged back into the master branch.</span></span> <span data-ttu-id="b5f22-124">マスター ブランチは、プロジェクトの現在のバージョンおよび "信頼できる唯一の情報源" となります。</span><span class="sxs-lookup"><span data-stu-id="b5f22-124">The master branch serves as the current version and "single source of truth" for the project.</span></span> <span data-ttu-id="b5f22-125">これは、そのリポジトリ内の他のすべてのブランチの作成元となる親です。</span><span class="sxs-lookup"><span data-stu-id="b5f22-125">It's the parent from which all other branches in the repository are created.</span></span>

<span data-ttu-id="b5f22-126">共同作成者は以下の方法で Git と対話して、ローカル レベルと GitHub レベルの両方でリポジトリを更新および処理します。</span><span class="sxs-lookup"><span data-stu-id="b5f22-126">Contributors interact with Git to update and manipulate repositories at both the local and GitHub levels:</span></span>

- <span data-ttu-id="b5f22-127">ローカルでは、ローカル リポジトリの管理や GitHub リポジトリとの通信のための Git のコマンドをサポートするツール (Git Bash コンソールなど) を利用します。</span><span class="sxs-lookup"><span data-stu-id="b5f22-127">Locally through tools such as the Git Bash console, which supports Git commands for managing local repositories and communicating with GitHub repositories.</span></span>
- <span data-ttu-id="b5f22-128">Git を統合する [www.github.com](https://www.github.com) を利用して、メイン リポジトリに戻される共同作成の整合を管理します。</span><span class="sxs-lookup"><span data-stu-id="b5f22-128">Via [www.github.com](https://www.github.com), which integrates Git to manage the reconciliation of contributions that flow back into the main repository.</span></span>

## <a name="github"></a><span data-ttu-id="b5f22-129">GitHub</span><span class="sxs-lookup"><span data-stu-id="b5f22-129">GitHub</span></span>

> [!NOTE]
> <span data-ttu-id="b5f22-130">Docs のガイダンスは GitHub の使用を前提としていますが、チームによっては Visual Studio Team Services を利用して Git リポジトリをホスティングします。</span><span class="sxs-lookup"><span data-stu-id="b5f22-130">Although Docs guidance is based on using GitHub, some teams use Visual Studio Team Services to host Git repositories.</span></span> <span data-ttu-id="b5f22-131">Visual Studio Team Explorer クライアントでは、コマンド ラインで Git コマンドを使用する代わりに、GUI を利用して Team Services リポジトリと対話できます。</span><span class="sxs-lookup"><span data-stu-id="b5f22-131">The Visual Studio Team Explorer client provides a GUI for interacting with Team Services repositories, as an alternative to using Git commands through a command line.</span></span>
> </br>
> <span data-ttu-id="b5f22-132">また、後述のガイドラインの多くは、GitHub で Azure サービスのコンテンツをホストしてきた長年の経験からのベスト プラクティスとして開発されました。</span><span class="sxs-lookup"><span data-stu-id="b5f22-132">Also, many of the following guidelines were developed as best practices from years of experience in hosting Azure service content in GitHub.</span></span> <span data-ttu-id="b5f22-133">一部の Docs リポジトリでは必須である可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b5f22-133">They might be required in some Docs repositories.</span></span>

<span data-ttu-id="b5f22-134">すべてのワークフローは任意の Docs プロジェクトのメイン リポジトリが格納されている GitHub レベルで始まり、GitHub レベルで終わります。</span><span class="sxs-lookup"><span data-stu-id="b5f22-134">All workflows begin and end at the GitHub level, where the main repository for any Docs project is stored.</span></span> <span data-ttu-id="b5f22-135">共同作成者が自分で使用するために作成するコピーは、複数のコンピューターに配信されます。</span><span class="sxs-lookup"><span data-stu-id="b5f22-135">The copies that contributors create for their own use are distributed across multiple computers.</span></span> <span data-ttu-id="b5f22-136">これらのコピーは最終的に、プロジェクトのメイン GitHub リポジトリに戻されて整合されます。</span><span class="sxs-lookup"><span data-stu-id="b5f22-136">These copies are eventually reconciled back into the project's main GitHub repository.</span></span>

### <a name="directory-organization"></a><span data-ttu-id="b5f22-137">ディレクトリの構成</span><span class="sxs-lookup"><span data-stu-id="b5f22-137">Directory organization</span></span>

<span data-ttu-id="b5f22-138">前述のとおり、プロジェクトの既定/マスター ブランチは、プロジェクト コンテンツの最新バージョンとして機能します。</span><span class="sxs-lookup"><span data-stu-id="b5f22-138">As mentioned earlier, a project's default/master branch serves as the current version of content for the project.</span></span> <span data-ttu-id="b5f22-139">マスター ブランチ (およびマスター ブランチから作成されたブランチ) のコンテンツは、対応する Docs ページの記事の組織と大まかに一致します。</span><span class="sxs-lookup"><span data-stu-id="b5f22-139">The content in the master branch--and branches created from it--is loosely aligned with the organization of the articles on the corresponding Docs pages.</span></span> <span data-ttu-id="b5f22-140">お気に入りコンテンツ (サービスなど)、メディア コンテンツ (イメージ ファイルなど)、および "インクルード" ファイル (コンテンツの再利用を可能にする) を分離するために、サブディレクトリが使用されます。</span><span class="sxs-lookup"><span data-stu-id="b5f22-140">Subdirectories are used for separation of like content (such as services), media content (such as image files), and "include" files (which enable reuse of content).</span></span>

<span data-ttu-id="b5f22-141">通常、メイン `articles` ディレクトリはリポジトリのルートの直下にあります。</span><span class="sxs-lookup"><span data-stu-id="b5f22-141">You can typically find a main `articles` directory off the root of the repository.</span></span> <span data-ttu-id="b5f22-142">記事のディレクトリには一連のサブディレクトリが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b5f22-142">The articles directory contains a set of subdirectories.</span></span> <span data-ttu-id="b5f22-143">サブディレクトリ内の記事は、*.md* 拡張子を使用する Markdown ファイルとして書式設定されます。</span><span class="sxs-lookup"><span data-stu-id="b5f22-143">Articles in the subdirectories are formatted as Markdown files that use an *.md* extension.</span></span> <span data-ttu-id="b5f22-144">複数のサービスをサポートするリポジトリでは、共通の `/articles` サブディレクトリが使用されることがあります。たとえば、[Azure-Docs](https://github.com/MicrosoftDocs/Azure-Docs) リポジトリです。</span><span class="sxs-lookup"><span data-stu-id="b5f22-144">Some repositories that support multiple services use a generic `/articles` subdirectory, such as the [Azure-Docs](https://github.com/MicrosoftDocs/Azure-Docs) repository.</span></span> <span data-ttu-id="b5f22-145">サービス固有の名前が使用される場合もあります。たとえば、[IntuneDocs](https://github.com/MicrosoftDocs/IntuneDocs) リポジトリでは `/IntuneDocs` が使用されます。</span><span class="sxs-lookup"><span data-stu-id="b5f22-145">Others might use a service-specific name, such as the [IntuneDocs](https://github.com/MicrosoftDocs/IntuneDocs) repository, which uses `/IntuneDocs`.</span></span>

<span data-ttu-id="b5f22-146">このディレクトリのルートには、サービスまたは製品全体に関する記事全般があります。</span><span class="sxs-lookup"><span data-stu-id="b5f22-146">Within the root of this directory, you can find general articles that relate to the overall service or product.</span></span> <span data-ttu-id="b5f22-147">通常ではその他に、機能/サービスまたは共通のシナリオに対応する一連のサブディレクトリがあります。</span><span class="sxs-lookup"><span data-stu-id="b5f22-147">And typically, you can then find another series of subdirectories that match the features/services or common scenarios.</span></span> <span data-ttu-id="b5f22-148">たとえば、Azure の "仮想マシン" に関する記事はサブディレクトリ `/virtual-machines` にあり、Intune の "理解と探索" に関する記事はサブディレクトリ `/understand-explore` にあります。</span><span class="sxs-lookup"><span data-stu-id="b5f22-148">For instance, Azure "virtual machine" articles are in the `/virtual-machines` subdirectory, and Intune "understand and explore" articles are in the `/understand-explore` subdirectory.</span></span>

### <a name="media-subdirectory"></a><span data-ttu-id="b5f22-149">メディアのサブディレクトリ</span><span class="sxs-lookup"><span data-stu-id="b5f22-149">Media subdirectory</span></span>

<span data-ttu-id="b5f22-150">各記事のディレクトリには、対応するメディア ファイルの `/media` サブディレクトリが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b5f22-150">Each article directory contains a `/media` subdirectory for corresponding media files.</span></span> <span data-ttu-id="b5f22-151">メディア ファイルには、イメージ参照がある記事で使用されるイメージが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b5f22-151">Media files contain images used by articles that have image references.</span></span>

### <a name="includes-subdirectory"></a><span data-ttu-id="b5f22-152">インクルード サブディレクトリ</span><span class="sxs-lookup"><span data-stu-id="b5f22-152">Includes subdirectory</span></span>

<span data-ttu-id="b5f22-153">2 つ以上の記事で共有される再利用可能なコンテンツがある場合は常に、メイン `articles` ディレクトリの直下にあるサブディレクトリ `/includes` に配置されます。</span><span class="sxs-lookup"><span data-stu-id="b5f22-153">Whenever we have reusable content that is shared across two or more articles, it is placed in an `/includes` subdirectory off the main `articles` directory.</span></span> <span data-ttu-id="b5f22-154">インクルード ファイルを使用する Markdown ファイルでは、インクルード ファイルが参照される必要がある場所に、対応する "include" Markdown の拡張機能が配置されます。</span><span class="sxs-lookup"><span data-stu-id="b5f22-154">In a Markdown file that uses the include file, a corresponding "include" Markdown extension is placed in the location where the include file needs to be referenced.</span></span>

<span data-ttu-id="b5f22-155">その他のガイダンスについては、[「Markdown の使用方法」の「インクルード」セクション](how-to-write-use-markdown.md#includes)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b5f22-155">See [How to use Markdown: Includes](how-to-write-use-markdown.md#includes) for additional guidance.</span></span>

### <a name="markdown-file-template"></a><span data-ttu-id="b5f22-156">Markdown ファイルのテンプレート</span><span class="sxs-lookup"><span data-stu-id="b5f22-156">Markdown file template</span></span>

<span data-ttu-id="b5f22-157">便宜上、各リポジトリのルート ディレクトリには通常、`template.md` という名前の Markdown テンプレート ファイルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b5f22-157">For convenience, the root directory of each repository typically contains a Markdown template file named `template.md`.</span></span> <span data-ttu-id="b5f22-158">新しい記事を作成してリポジトリに送信する必要がある場合は、このテンプレート ファイルを "開始ファイル" として使用できます。</span><span class="sxs-lookup"><span data-stu-id="b5f22-158">You can use this template file as a "starter file" if you need to create a new article for submission to the repository.</span></span> <span data-ttu-id="b5f22-159">ファイルには、次のものが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b5f22-159">The file contains:</span></span>

- <span data-ttu-id="b5f22-160">ファイルの冒頭にある**メタデータ ヘッダー**。3 つのハイフンで構成される 2 本の線で区切られます。</span><span class="sxs-lookup"><span data-stu-id="b5f22-160">A **metadata header** at the top of the file, delineated by two, 3-hyphen lines.</span></span> <span data-ttu-id="b5f22-161">記事に関連する情報の追跡に使用される各種タグが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b5f22-161">It contains the various tags used for tracking information related to the article.</span></span> <span data-ttu-id="b5f22-162">記事のメタデータでは、作成者の属性、共同作成者の属性、階層リンク、および記事の説明など、特定の機能を使用できます。</span><span class="sxs-lookup"><span data-stu-id="b5f22-162">Article metadata enables certain functionality, such as author attribution, contributor attribution, breadcrumbs, and article descriptions.</span></span> <span data-ttu-id="b5f22-163">これには、Microsoft がコンテンツのパフォーマンス評価に使用する SEO の最適化やレポート プロセスも含まれます。</span><span class="sxs-lookup"><span data-stu-id="b5f22-163">It also includes SEO optimizations and reporting processes that Microsoft uses to evaluate the performance of the content.</span></span> <span data-ttu-id="b5f22-164">したがって、メタデータは重要です。</span><span class="sxs-lookup"><span data-stu-id="b5f22-164">So the metadata is important!</span></span>
- <span data-ttu-id="b5f22-165">メタデータのさまざまなタグや値を説明する**メタデータ セクション**。</span><span class="sxs-lookup"><span data-stu-id="b5f22-165">A **metadata section** that describes the various metadata tags and values.</span></span> <span data-ttu-id="b5f22-166"> メタデータ セクションで使用する値がわからない場合、空白のままにするか、先頭にハッシュタグ (#) を付けたコメントを残すことができます。これらはリポジトリの pull request レビュー担当者によってレビュー/完了されます。</span><span class="sxs-lookup"><span data-stu-id="b5f22-166">If you're unsure of the values to use for the metadata section, you can leave them blank or comment them with a leading hashtag (#), and they will be reviewed/completed by the pull request reviewer for the repository.</span></span>
- <span data-ttu-id="b5f22-167">記事の要素の書式を設定するさまざまな **Markdown の使用例**。</span><span class="sxs-lookup"><span data-stu-id="b5f22-167">Various **examples of using Markdown** to format the elements of an article.</span></span>
- <span data-ttu-id="b5f22-168">**Markdown 拡張機能の使用に関する説明**全般。これはさまざまな種類のアラートに使用できます。</span><span class="sxs-lookup"><span data-stu-id="b5f22-168">General **instructions on the use of Markdown extensions**, which you can use for various types of alerts.</span></span>
- <span data-ttu-id="b5f22-169">iframe を使用した**ビデオ埋め込み**の例。</span><span class="sxs-lookup"><span data-stu-id="b5f22-169">Examples of **embedding video** by using an iframe.</span></span>
- <span data-ttu-id="b5f22-170">**docs.microsoft.com 拡張機能の使用に関する説明**全般。これはボタンやセレクターなどの特殊なコントロールに使用できます。</span><span class="sxs-lookup"><span data-stu-id="b5f22-170">General **instructions on the use of docs.microsoft.com extensions**, which you can use for special controls such as buttons and selectors.</span></span>

## <a name="pull-requests"></a><span data-ttu-id="b5f22-171">Pull request</span><span class="sxs-lookup"><span data-stu-id="b5f22-171">Pull requests</span></span>

<span data-ttu-id="b5f22-172">*pull request* は、共同作成者が既定のブランチに適用される一連の変更内容を提案できる便利な手段です。</span><span class="sxs-lookup"><span data-stu-id="b5f22-172">A *pull request* provides a convenient way for a contributor to propose a set of changes that will be applied to the default branch.</span></span> <span data-ttu-id="b5f22-173">変更内容 (*コミット* ともいう) は共同作成者のブランチに格納されるため、GitHub は既定のブランチに変更内容を*マージする* 影響をあらかじめモデル化することができます。</span><span class="sxs-lookup"><span data-stu-id="b5f22-173">The changes (also known as *commits*) are stored in a contributor's branch, so GitHub can first model the impact of *merging* them into the default branch.</span></span> <span data-ttu-id="b5f22-174">Pull request は、変更内容が既定のブランチにマージされる前に潜在的な問題や疑問を解消するために、ビルド/検証プロセスや pull request のレビュー担当者からのフィードバックを共同作成者に提供するメカニズムとしても機能します。</span><span class="sxs-lookup"><span data-stu-id="b5f22-174">A pull request also serves as a mechanism to provide the contributor with feedback from a build/validation process, the pull request reviewer, to resolve potential issues or questions before the changes are merged into the default branch.</span></span>

<span data-ttu-id="b5f22-175">提案する変更内容のサイズに応じて、pull request で共同作成を行う方法が 2 つあります。</span><span class="sxs-lookup"><span data-stu-id="b5f22-175">There are two ways to contribute by pull request, depending on the size of changes that you want to propose.</span></span> <span data-ttu-id="b5f22-176">これについては、このガイドで後述する [GitHub のワークフロー](how-to-write-workflows-major.md)に関するセクションで詳しく説明します。</span><span class="sxs-lookup"><span data-stu-id="b5f22-176">We will cover this in detail later, in the [GitHub workflow](how-to-write-workflows-major.md) section of this guide.</span></span>

<!---- Reference links for Docs landing pages, associated GitHub repositories, and related Forums matrix. ------------------>
<!---- PLEASE INSERT URLS IN ASCENDING SORT ORDER, AND REMOVE LOCALE SEGMENT FROM URLS (that is, en-us) FOR LOCALIZED FORUMS! -->
<!---- NOTE: these links are saved for future use in another/new article; no longer used above in this article --->
[Visual-Studio-Page]:(https://docs.microsoft.com/en-us/visualstudio/index)
[Visual-Studio-Repo-Internal]:(https://github.com/Microsoft/vsdocs)
[Visual-Studio-Repo-External]:(https://github.com/Microsoft/visualstudio-docs)
[Visual-Studio-SO]: (https://stackoverflow.com/search?q=Visual+Studio+2017)
[Dotnet-Page]: https://docs.microsoft.com/dotnet
[Dotnet-Core-Page]: https://docs.microsoft.com/dotnet/articles/welcome
[Dotnet-Core-Repo]: https://github.com/dotnet/docs
[EM-ATA-Land]: https://docs.microsoft.com/advanced-threat-analytics/
[EM-ATA-Repo]: https://github.com/Microsoft/ATADocs
[EM-AzureAD-Land]: https://docs.microsoft.com/active-directory/
[EM-AzureAD-Repo]: https://github.com/Azure/azure-content/tree/master/articles/active-directory/
[EM-AzureRMS-Land]: https://docs.microsoft.com/rights-management/
[EM-AzureRMS-Repo]: https://github.com/Microsoft/Azure-RMSDocs
[EM-Intune-Land]: https://docs.microsoft.com/intune/
[EM-Intune-Repo]: https://github.com/microsoft/intuneDocs
[EM-Land-Page]: https://docs.microsoft.com/enterprise-mobility/
[EM-Land-Repo]: https://github.com/Microsoft/EMDocs/
[EM-MFA-Land]: https://docs.microsoft.com/multi-factor-authentication/
[EM-MFA-Repo]: https://github.com/Azure/azure-content/tree/master/articles/multi-factor-authentication
[EM-MIM-Land]: https://docs.microsoft.com/microsoft-identity-manager/
[EM-MIM-Repo]: https://github.com/Microsoft/MIMDocs
[EM-RemoteApp-Land]: https://docs.microsoft.com/en-us/remoteapp/
[EM-RemoteApp-Repo]: https://github.com/Azure/azure-content/tree/master/articles/remoteapp
[Forum-MSDN-ATA]: https://social.technet.microsoft.com/Forums/en-US/home?forum=mata
[Forum-MSDN-AzureAD]: https://social.msdn.microsoft.com/Forums/en-US/home?forum=WindowsAzureAD
[Forum-MSDN-AzureRMS]: https://social.technet.microsoft.com/Forums/en-US/home?forum=rmsapps%2Crmscloud&filter=alltypes&sort=lastpostdesc
[Forum-MSDN-EM]: https://social.technet.microsoft.com/Forums/en-US/home?sort=relevancedesc&brandIgnore=True&searchTerm=Enterprise+Mobility
[Forum-MSDN-Intune]: https://social.technet.microsoft.com/Forums/en-us/home?category=microsoftintune
[Forum-MSDN-Main]: https://social.msdn.microsoft.com/Forums/home
[Forum-MSDN-MFA]: https://social.msdn.microsoft.com/Forums/en-US/home?forum=windowsazureactiveauthentication
[Forum-MSDN-MIM]: https://social.technet.microsoft.com/Forums/en-US/home?category=identitymanagement
[Forum-MSDN-RemoteApp]: https://social.technet.microsoft.com/Forums/en-US/home?filter=alltypes&brandIgnore=True&sort=relevancedesc&searchTerm=Azure+Remote+or+RemoteApp
[Forum-SO-AzureAD]: https://stackoverflow.com/questions/tagged/azure-active-directory
[Forum-SO-AzureRMS]: https://stackoverflow.com/questions/tagged/rights-management
[Forum-SO-Dotnet]: https://stackoverflow.com/questions/tagged/.net
[Forum-SO-Dotnet-Core]: https://stackoverflow.com/questions/tagged/.net-core
[Forum-SO-Main]: https://stackoverflow.com/tags
[Forum-SO-Intune]: https://stackoverflow.com/questions/tagged/intune
[Forum-SO-MFA]: https://stackoverflow.com/search?q=%5Bazure%5D+multi-factor
[Forum-SO-MIM]: https://stackoverflow.com/search?q=Microsoft+Identity+Manager
[Forum-SO-RemoteApp]: https://stackoverflow.com/questions/tagged/remoteapp
[Forum-TechNet-Main]: https://social.technet.microsoft.com/Forums/home
[Forum-Yammer-AzureRMS]: https://www.yammer.com/AskIPTeam
[Forum-Yammer-Main]: https://www.yammer.com/
