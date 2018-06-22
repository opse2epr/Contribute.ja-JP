---
title: ドキュメントでのリンクの使用方法
description: この記事では、docs.microsoft.com 内でのコンテンツへのリンクの作成に関するガイドを提供します。
ms.date: 06/29/2017
ms.openlocfilehash: a66e2fb4febf1947afe01919b96b1c10873cf57d
ms.sourcegitcommit: 92aef5ea8bdd692c5c393d5c8f99b9e4f672ef2b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/19/2018
ms.locfileid: "36239728"
---
# <a name="using-links-in-documentation"></a><span data-ttu-id="0bf6a-103">ドキュメントでリンクを使用する</span><span class="sxs-lookup"><span data-stu-id="0bf6a-103">Using links in documentation</span></span>
<span data-ttu-id="0bf6a-104">この記事では、docs.microsoft.com でホストされたページからハイパーリンクを使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-104">This article describes how to use hyperlinks from pages hosted at docs.microsoft.com.</span></span> <span data-ttu-id="0bf6a-105">いくつかの規則が変更されていますが、リンクは Markdown に簡単に追加できます。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-105">Links are easy to add into markdown with a few varying conventions.</span></span> <span data-ttu-id="0bf6a-106">リンクは、同じページ内のコンテンツをポイントするか、他の近くにあるページ内をポイントするか、外部のサイトや URL をポイントすることができます。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-106">Links point users to content in the same page, point off into other neighboring pages, or point to external sites and URLs.</span></span>

<span data-ttu-id="0bf6a-107">docs.microsoft.com サイトは、DocFX Flavored Markdown (DFM) を実装する Open Publishing Services (OPS) をバックエンドで使用します。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-107">The docs.microsoft.com site backend uses Open Publishing Services (OPS) which implements DocFX Flavored Markdown (DFM).</span></span> <span data-ttu-id="0bf6a-108">DFM は、GitHub Flavored Markdown (GFM) と高い互換性があり、DFM は Markdown 拡張機能を介して機能を追加します。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-108">DFM is highly compatible with GitHub Flavored Markdown (GFM), and DFM adds additional functionality through Markdown extensions.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0bf6a-109">ターゲットでサポートされている場合 (このケースが大半) は必ず、すべてのリンクをセキュリティで保護する必要があります (`http` ではなく `https`)。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-109">All links must be secure (`https` vs `http`) whenever the target supports it (which the vast majority should).</span></span>

## <a name="link-text"></a><span data-ttu-id="0bf6a-110">リンク テキスト</span><span class="sxs-lookup"><span data-stu-id="0bf6a-110">Link text</span></span>

<span data-ttu-id="0bf6a-111">リンク テキストに含める単語はわかりやすくすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-111">The words that you include in link text should be friendly.</span></span> <span data-ttu-id="0bf6a-112">つまり、通常の英単語にするか、リンク先のページのタイトルにします。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-112">In other words, they should be normal English words or the title of the page that you're linking to.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0bf6a-113">「ここをクリック」は使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-113">Do not use "click here."</span></span> <span data-ttu-id="0bf6a-114">これは SEO (検索エンジン最適化) としても悪く、また、リンク先の説明も的確にされていません。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-114">It's bad for SEO and doesn't adequately describe the target.</span></span>

<span data-ttu-id="0bf6a-115">**正確:**</span><span class="sxs-lookup"><span data-stu-id="0bf6a-115">**Correct:**</span></span>

- `For more information, see the [contributor guide index](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

- `For more details, see the [SET TRANSACTION ISOLATION LEVEL](https://msdn.microsoft.com/library/ms173763.aspx) reference.`

<span data-ttu-id="0bf6a-116">**不正確:**</span><span class="sxs-lookup"><span data-stu-id="0bf6a-116">**Incorrect:**</span></span>

- `For more details, see [https://msdn.microsoft.com/library/ms173763.aspx](https://msdn.microsoft.com/library/ms173763.aspx).`

- `For more information, click [here](https://github.com/Azure/azure-content/blob/master/contributor-guide/contributor-guide-index.md).`

## <a name="links-from-one-article-to-another"></a><span data-ttu-id="0bf6a-117">1 つの記事から別の記事へのリンク</span><span class="sxs-lookup"><span data-stu-id="0bf6a-117">Links from one article to another</span></span>

<span data-ttu-id="0bf6a-118">同じ docset 内で 1 つの Docs 技術情報記事から別の Docs 技術情報記事へのインライン リンクを作成するには、次のリンク構文を使用します。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-118">To create an inline link from a Docs technical article to another Docs technical article within the same docset, use the following link syntax:</span></span>

- <span data-ttu-id="0bf6a-119">ディレクトリの記事を、同じディレクトリの別の記事にリンクする場合</span><span class="sxs-lookup"><span data-stu-id="0bf6a-119">An article in a directory links to another article in the same directory:</span></span>

  `[link text](article-name.md)`

- <span data-ttu-id="0bf6a-120">サブディレクトリの記事を、ルート ディレクトリの記事にリンクする場合</span><span class="sxs-lookup"><span data-stu-id="0bf6a-120">An article links from a subdirectory to an article in the root directory:</span></span>

  `[link text](../article-name.md)`

- <span data-ttu-id="0bf6a-121">ルート ディレクトリの記事を、サブディレクトリの記事にリンクする場合</span><span class="sxs-lookup"><span data-stu-id="0bf6a-121">An article in the root directory links to an article in a subdirectory:</span></span>

  `[link text](./directory/article-name.md)`

- <span data-ttu-id="0bf6a-122">サブディレクトリの記事を、別のサブディレクトリの記事にリンクする場合</span><span class="sxs-lookup"><span data-stu-id="0bf6a-122">An article in a subdirectory links to an article in another subdirectory:</span></span>

  `[link text](../directory/article-name.md)`

- <span data-ttu-id="0bf6a-123">docset 間の記事のリンク (同じリポジトリ内の場合でも): `[link text](./directory/article-name)`</span><span class="sxs-lookup"><span data-stu-id="0bf6a-123">An article linking across docsets (even if in the same repository): `[link text](./directory/article-name)`</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0bf6a-124">上記の例で `~/` をリンクの一部としているのはありません。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-124">None of the above examples use the `~/` as part of the link.</span></span> <span data-ttu-id="0bf6a-125">リポジトリのルートにあるパスにリンクするには、`/` から始めます。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-125">If you are linking to a path at the root of the repository, start with the `/`.</span></span> <span data-ttu-id="0bf6a-126">GitHub のソース リポジトリを移動するときに `~/` が生成する無効なリンクを含みます。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-126">Including the `~/` produces invalid links when navigating the source repositories on GitHub.</span></span> <span data-ttu-id="0bf6a-127">`/` が正しく解決するパスから始めます。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-127">Starting the path with `/` resolves correctly.</span></span>

## <a name="links-to-anchors"></a><span data-ttu-id="0bf6a-128">アンカーへのリンク</span><span class="sxs-lookup"><span data-stu-id="0bf6a-128">Links to anchors</span></span>

<span data-ttu-id="0bf6a-129">アンカーを作成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-129">You do not have to create anchors.</span></span> <span data-ttu-id="0bf6a-130">アンカーは、公開時に、すべての H2 見出しについて自動的に生成されます。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-130">They're automatically generated at publishing time for all H2 headings.</span></span> <span data-ttu-id="0bf6a-131">唯一行う必要がある処理は、H2 セクションへのリンクを作成することです。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-131">The only thing you have to do is create links to the H2 sections.</span></span>

- <span data-ttu-id="0bf6a-132">同じ記事内の見出しにリンクする場合</span><span class="sxs-lookup"><span data-stu-id="0bf6a-132">To link to a heading within the same article:</span></span>

  `[link](#the-text-of-the-H2-section-separated-by-hyphens)`
  `[Create cache](#create-cache)`

- <span data-ttu-id="0bf6a-133">同じサブディレクトリの別の記事のアンカーにリンクする場合</span><span class="sxs-lookup"><span data-stu-id="0bf6a-133">To link to an anchor in another article in the same subdirectory:</span></span>

  `[link text](article-name.md#anchor-name)`
  `[Configure your profile](media-services-create-account.md#configure-your-profile)`

- <span data-ttu-id="0bf6a-134">別のサービスのサブディレクトリのアンカーにリンクする場合</span><span class="sxs-lookup"><span data-stu-id="0bf6a-134">To link to an anchor in another service subdirectory:</span></span>

  `[link text](../directory/article-name.md#anchor-name)`
  `[Configure your profile](../directory/media-services-create-account.md#configure-your-profile)`

## <a name="links-from-includes"></a><span data-ttu-id="0bf6a-135">インクルードからのリンク</span><span class="sxs-lookup"><span data-stu-id="0bf6a-135">Links from includes</span></span>

<span data-ttu-id="0bf6a-136">インクルード ファイルは別のディレクトリにあるため、より長い相対パスを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-136">Because include files are located in another directory, you must use longer relative paths.</span></span> <span data-ttu-id="0bf6a-137">インクルード ファイルから記事にリンクするには、次のフォーマットを使用します。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-137">To link to an article from an include file, use this format:</span></span>

    [link text](../articles/folder/article-name.md)

## <a name="links-in-selectors"></a><span data-ttu-id="0bf6a-138">セレクターのリンク</span><span class="sxs-lookup"><span data-stu-id="0bf6a-138">Links in selectors</span></span>

<span data-ttu-id="0bf6a-139">インクルードに埋め込まれたセレクターがある場合は、Azure ドキュメント チームが行っているように次のリンク構造を使用します。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-139">If you have selectors that are embedded in an include--as does the Azure documentation team--use the following link structure:</span></span>

    > <span data-ttu-id="0bf6a-140">[AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]</span><span class="sxs-lookup"><span data-stu-id="0bf6a-140">[AZURE.SELECTOR-LIST (Dropdown1 | Dropdown2 )]</span></span>
    - [<span data-ttu-id="0bf6a-141">(Text1 | Example1 )</span><span class="sxs-lookup"><span data-stu-id="0bf6a-141">(Text1 | Example1 )</span></span>](../articles/folder/article-name1.md)
    - [<span data-ttu-id="0bf6a-142">(Text1 | Example2 )</span><span class="sxs-lookup"><span data-stu-id="0bf6a-142">(Text1 | Example2 )</span></span>](../articles/folder/article-name2.md)
    - [<span data-ttu-id="0bf6a-143">(Text2 | Example3 )</span><span class="sxs-lookup"><span data-stu-id="0bf6a-143">(Text2 | Example3 )</span></span>](../articles/folder/article-name3.md)
    - <span data-ttu-id="0bf6a-144">[(Text2 | Example4 )](../articles/folder/article-name4.md) --></span><span class="sxs-lookup"><span data-stu-id="0bf6a-144">[(Text2 | Example4 )](../articles/folder/article-name4.md) --></span></span>

## <a name="reference-style-links"></a><span data-ttu-id="0bf6a-145">参照形式のリンク</span><span class="sxs-lookup"><span data-stu-id="0bf6a-145">Reference-style links</span></span>

<span data-ttu-id="0bf6a-146">参照形式のリンクを使用することで、ソース コンテンツをさらに読みやすくすることができます。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-146">You can use reference-style links to make your source content easier to read.</span></span> <span data-ttu-id="0bf6a-147">参照形式のリンクを使用すると、インライン リンク構文を、簡素化された構文で置き換えることができます。この構文によって、長い URL を記事の最後に移動することができます。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-147">Reference-style links replace inline link syntax with simplified syntax that allows you to move the long URLs to the end of the article.</span></span> <span data-ttu-id="0bf6a-148">[Daring Fireball](https://daringfireball.net/projects/markdown/) の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-148">Here's [Daring Fireball](https://daringfireball.net/projects/markdown/) 's example:</span></span>

<span data-ttu-id="0bf6a-149">インライン テキスト:</span><span class="sxs-lookup"><span data-stu-id="0bf6a-149">Inline text:</span></span>

    I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].

<span data-ttu-id="0bf6a-150">記事の最後のリンク参照:</span><span class="sxs-lookup"><span data-stu-id="0bf6a-150">Link references at the end of the article:</span></span>

    <!--Reference links in article-->
    [1]: http://google.com/
    [2]: http://search.yahoo.com/
    [3]: http://search.msn.com/

<span data-ttu-id="0bf6a-151">コロンの後、リンクの前に必ずスペースを入れます。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-151">Make sure that you include the space after the colon, before the link.</span></span> <span data-ttu-id="0bf6a-152">他の技術情報記事にリンクする際に、スペースを入れ忘れてしまった場合、リンクが破損した状態で記事が公開されます。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-152">When you link to other technical articles, if you forget to include the space, the link will be broken in the published article.</span></span>

## <a name="links-to-pages-that-are-not-part-of-the-technical-documentation-set"></a><span data-ttu-id="0bf6a-153">技術ドキュメント セットではないページへのリンク</span><span class="sxs-lookup"><span data-stu-id="0bf6a-153">Links to pages that are not part of the technical documentation set</span></span>

<span data-ttu-id="0bf6a-154">別の Microsoft 資産のページ (価格のページ、SLA のページ、その他ドキュメントの記事ではないもの) にリンクする場合は、絶対 URL を使用しますが、ロケールは省略します。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-154">To link to a page on another Microsoft property (such as a pricing page, SLA page, or anything else that is not a documentation article), use an absolute URL, but omit the locale.</span></span> <span data-ttu-id="0bf6a-155">ここでの目的は、リンクが GitHub と次に示すサイトで作動することです。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-155">The goal here is that links work in GitHub and on the rendered site:</span></span>

    [link text](https://azure.microsoft.com/pricing/details/virtual-machines/)

## <a name="links-to-third-party-sites"></a><span data-ttu-id="0bf6a-156">サード パーティのサイトへのリンク</span><span class="sxs-lookup"><span data-stu-id="0bf6a-156">Links to third-party sites</span></span>

<span data-ttu-id="0bf6a-157">最高のユーザー体験は、別サイトへのユーザーの誘導を最小限に抑えます。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-157">The best user experience minimizes sending users to another site.</span></span> <span data-ttu-id="0bf6a-158">そのため、サード パーティのサイトにリンクする必要がある場合は、次の情報に基づいて行ってください。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-158">So base any links to third-party sites, which we do sometimes need, on this info:</span></span>

- <span data-ttu-id="0bf6a-159">**アカウンタビリティ**: 共有する情報がサード パーティの情報である場合に、サード パーティのコンテンツにリンクする。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-159">**Accountability**: Link to third-party content when it's the third-party's information to share.</span></span> <span data-ttu-id="0bf6a-160">たとえば、Microsoft のサイトで Android Developer Tools の使用方法の説明はしません。これは、Google が説明するべきことです。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-160">For example, it's not Microsoft's place to tell people how to use Android developer tools--that is Google's story to tell.</span></span> <span data-ttu-id="0bf6a-161">必要であれば、Azure *で* Android 開発者用ツールを使用する方法を説明することはできますが、Google のツールの使用方法は、Google が説明することです。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-161">If we need to, we can explain how to use Android developer tools *with* Azure, but Google should tell the story of how to use their tools.</span></span>
- <span data-ttu-id="0bf6a-162">**PM サインオフ**: サードパーティ コンテンツの Microsoft サインオフを要求する。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-162">**PM signoff**: Request that Microsoft sign off on third-party content.</span></span> <span data-ttu-id="0bf6a-163">サード パーティのコンテンツにリンクすることは、Microsoft がそのコンテンツを信頼していること、またユーザーがその指示に従った場合の Microsoft の責任を意味することになります</span><span class="sxs-lookup"><span data-stu-id="0bf6a-163">By linking to it, we are saying something about our trust in it and our obligation if people follow the instructions.</span></span>
- <span data-ttu-id="0bf6a-164">**情報の鮮度のレビュー**: サード パーティの情報がまだ最新で、間違いがなく、関連していること、そしてリンクが変更していないことを確認する。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-164">**Freshness reviews**: Make sure that the third-party info is still current, correct, and relevant, and that the link hasn’t changed.</span></span>
- <span data-ttu-id="0bf6a-165">**オフサイト**: 別のサイトに移動していることをユーザーが認識できるようにする。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-165">**Offsite**: Make users aware that they are going to another site.</span></span> <span data-ttu-id="0bf6a-166">それが明確でない状況の場合は、適切なフレーズを追加します。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-166">If the context does not make that clear, add a qualifying phrase.</span></span> <span data-ttu-id="0bf6a-167">たとえば、"必要条件に Android Developer Tools が含まれます。このツールは Android Studio サイトでダウンロードできます" などです。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-167">For example: “Prerequisites include the Android Developer Tools, which you can download on the Android Studio site.”</span></span>
- <span data-ttu-id="0bf6a-168">**次のステップ:** 「次のステップ」セクションに、MVP のブログなどへのリンクを追加しても構いません。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-168">**Next steps**: It’s fine to add a link to, say, an MVP blog in a "Next steps" section.</span></span> <span data-ttu-id="0bf6a-169">この場合も、サイトを離れることをユーザーが必ず認識できるようにしてください</span><span class="sxs-lookup"><span data-stu-id="0bf6a-169">Again, just make sure that users understand they’ll be leaving the site.</span></span>
- <span data-ttu-id="0bf6a-170">**合法**: Microsoft は、各 ms.com ページにある「**利用条件**」のフッターの **「サード パーティのサイト」へのリンク**で、合法的に保護されています</span><span class="sxs-lookup"><span data-stu-id="0bf6a-170">**Legal**: We are covered legally under **Links to Third Party Sites** in the **Terms of Use** footer on every ms.com page.</span></span>

## <a name="links-to-msdn-or-technet"></a><span data-ttu-id="0bf6a-171">MSDN または TechNet へのリンク</span><span class="sxs-lookup"><span data-stu-id="0bf6a-171">Links to MSDN or TechNet</span></span>

<span data-ttu-id="0bf6a-172">MSDN または TechNet へのリンクが必要な場合は、そのトピックへのフル リンクを使用し、そのリンクから "en-us" の言語ロケールを削除します。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-172">When you need to link to MSDN or TechNet, use the full link to the topic, and remove the "en-us" language locale from the link.</span></span>

## <a name="links-to-azure-powershell-reference-content"></a><span data-ttu-id="0bf6a-173">Azure PowerShell 関連コンテンツへのリンク</span><span class="sxs-lookup"><span data-stu-id="0bf6a-173">Links to Azure PowerShell reference content</span></span>

<span data-ttu-id="0bf6a-174">Azure PowerShell 関連のコンテンツは、2016 年 11 月以来、数回の変更を重ねています。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-174">The Azure PowerShell reference content has been through several changes since November 2016.</span></span> <span data-ttu-id="0bf6a-175">docs.microsoft.com の他の記事からこのコンテンツにリンクする場合は、次のガイドラインを使用してください。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-175">Use the following guidelines for linking to this content from other articles on docs.microsoft.com.</span></span>

<span data-ttu-id="0bf6a-176">URL の構造:</span><span class="sxs-lookup"><span data-stu-id="0bf6a-176">Structure of the URL:</span></span>

* <span data-ttu-id="0bf6a-177">コマンドレットの場合:</span><span class="sxs-lookup"><span data-stu-id="0bf6a-177">For cmdlets:</span></span>
  - `/powershell/module/<module-name>/<cmdlet-name>[?view=<moniker-name>]`
* <span data-ttu-id="0bf6a-178">概念についてのトピックの場合:</span><span class="sxs-lookup"><span data-stu-id="0bf6a-178">For conceptual topics:</span></span>
  - `/powershell/azure/<topic-file-name>[?view=<moniker-name>]`
  - `/powershell/azure/<service-name>/<topic-file-name>[?view=<moniker-name>]`

<span data-ttu-id="0bf6a-179">&lt;moniker-name&gt; (モニカー名) の部分は省略可能です。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-179">The &lt;moniker-name&gt; portion is optional.</span></span> <span data-ttu-id="0bf6a-180">省略した場合は、コンテンツの最新バージョンに移動します。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-180">If it's omitted, you will be directed to the latest version of the content.</span></span> <span data-ttu-id="0bf6a-181">&lt;service-name&gt; 部分は、次のベース URL に示す例のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-181">The &lt;service-name&gt; portion is one of the examples shown in the following base URLs:</span></span>

- <span data-ttu-id="0bf6a-182">Azure PowerShell (AzureRM) のコンテンツ: https://docs.microsoft.com/powershell/azure/</span><span class="sxs-lookup"><span data-stu-id="0bf6a-182">Azure PowerShell (AzureRM) content: https://docs.microsoft.com/powershell/azure/</span></span>
- <span data-ttu-id="0bf6a-183">Azure PowerShell (ASM) のコンテンツ: https://docs.microsoft.com/powershell/azure/_servicemanagement_</span><span class="sxs-lookup"><span data-stu-id="0bf6a-183">Azure PowerShell (ASM) content: https://docs.microsoft.com/powershell/azure/_servicemanagement_</span></span>
- <span data-ttu-id="0bf6a-184">Azure Active Directory (AzureAD) PowerShell のコンテンツ: https://docs.microsoft.com/powershell/azure/_active-directory_</span><span class="sxs-lookup"><span data-stu-id="0bf6a-184">Azure Active Directory (AzureAD) PowerShell content: https://docs.microsoft.com/powershell/azure/_active-directory_</span></span>
- <span data-ttu-id="0bf6a-185">Azure Service Fabric PowerShell: https://docs.microsoft.com/powershell/azure/_service-fabric_</span><span class="sxs-lookup"><span data-stu-id="0bf6a-185">Azure Service Fabric PowerShell: https://docs.microsoft.com/powershell/azure/_service-fabric_</span></span>
- <span data-ttu-id="0bf6a-186">Azure Information Protection PowerShell: https://docs.microsoft.com/powershell/azure/_aip_</span><span class="sxs-lookup"><span data-stu-id="0bf6a-186">Azure Information Protection PowerShell: https://docs.microsoft.com/powershell/azure/_aip_</span></span>
- <span data-ttu-id="0bf6a-187">Azure Elastic DB Jobs PowerShell: https://docs.microsoft.com/powershell/azure/_elasticdbjobs_</span><span class="sxs-lookup"><span data-stu-id="0bf6a-187">Azure Elastic DB Jobs PowerShell: https://docs.microsoft.com/powershell/azure/_elasticdbjobs_</span></span>

<span data-ttu-id="0bf6a-188">これらの URL を使用すると、コンテンツの最新バージョンにリダイレクトされます。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-188">When you use these URLs, you will be redirected to the latest version of the content.</span></span> <span data-ttu-id="0bf6a-189">この方法を使うと、バージョン モニカーを指定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-189">This way, you don't have to specify a version moniker.</span></span> <span data-ttu-id="0bf6a-190">また、バージョンが変わったときに更新する必要がある概念的コンテンツへのリンクも保持しません。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-190">And you won't have links to conceptual content that must be updated when the version changes.</span></span>

<span data-ttu-id="0bf6a-191">正確なリンクを作成するには、リンクするページを自分のブラウザーで検索して、その URL をコピーします。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-191">To create the correct link, find the page that you want to link to in your browser, and copy the URL.</span></span>
<span data-ttu-id="0bf6a-192">次に、"https://docs.microsoft.com" とロケール情報を削除します。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-192">Then, remove "https://docs.microsoft.com" and the locale info.</span></span>

<span data-ttu-id="0bf6a-193">目次からリンクするときは、フル URL からロケール情報を削除したものを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0bf6a-193">When you're linking from a TOC, you must use the full URL without the locale information.</span></span>

<span data-ttu-id="0bf6a-194">Markdown の例</span><span class="sxs-lookup"><span data-stu-id="0bf6a-194">Example markdown:</span></span>

```markdown
[Get-AzureRmResourceGroup](/powershell/module/azurerm.resources/get-azurermresourcegroup)
[Get-AzureRmResourceGroup](/powershell/module/azurerm.resources/get-azurermresourcegroup?view=azurermps-4.1.0)
[New-AzureVM](/powershell/module/azure/new-azurevm?view=azuresmps-4.0.0)
[New-AzureRmVM](/powershell/module/azurerm.compute/new-azurermvm)
[Install Azure PowerShell for Service Management](/powershell/azure/servicemanagement/install-azurerm-ps)
[Install Azure PowerShell](/powershell/azure/install-azurerm-ps)
```
