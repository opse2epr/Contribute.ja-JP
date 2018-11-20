---
title: OPS と docs.microsoft.com の Markdown
description: Markdown および DocFX Flavored Markdown (DFM) 拡張機能の OPS プラットフォーム ガイド。
author: meganbradley
ms.author: mbradley
manager: jemash
ms.date: 05/18/2018
ms.topic: contributor-guide
ms.prod: non-product-specific
audience: internal,external
ms.openlocfilehash: 64921bacf48e638221048db4b24e1a941f1d2777
ms.sourcegitcommit: 44eb4f5ee65c1848d7f36fca107b296eb7687397
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/13/2018
ms.locfileid: "51609547"
---
# <a name="markdown-reference-for-ops"></a><span data-ttu-id="05312-103">OPS の Markdown 参照</span><span class="sxs-lookup"><span data-stu-id="05312-103">Markdown Reference for OPS</span></span>

<span data-ttu-id="05312-104">Markdown は、プレーン テキスト形式の構文を使用する軽量のマークアップ言語です。</span><span class="sxs-lookup"><span data-stu-id="05312-104">Markdown is a lightweight markup language with plain text formatting syntax.</span></span> <span data-ttu-id="05312-105">Open Publishing Services (OPS) では、Markdown の CommonMark 標準がサポートされており、また、docs.microsoft.com で豊富なコンテンツを提供する目的で設計されたカスタム Markdown 拡張を一部サポートしています。</span><span class="sxs-lookup"><span data-stu-id="05312-105">Open Publishing Services (OPS) supports the CommonMark standard for Markdown, plus some custom Markdown extensions designed to provide richer content on docs.microsoft.com.</span></span> <span data-ttu-id="05312-106">この記事では、docs.microsoft.com 向けに OPS の Markdown のアルファベット順参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="05312-106">This article provides an alphabetical reference for using Markdown in OPS for docs.microsoft.com.</span></span>

<span data-ttu-id="05312-107">あらゆるテキスト エディターを使用して Markdown を作成できます。</span><span class="sxs-lookup"><span data-stu-id="05312-107">You can use any text editor to author Markdown.</span></span> <span data-ttu-id="05312-108">Markdown 構文とカスタム OPS 拡張の両方を簡単に挿入できるエディターとして、[Docs Authoring Pack](https://aka.ms/DocsAuthoringPack) をインストールした [VS Code](https://code.visualstudio.com/) をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="05312-108">For an editor that facilitates inserting both standard Markdown syntax and custom OPS extensions, we recommend [VS Code](https://code.visualstudio.com/) with the [Docs Authoring Pack](https://aka.ms/DocsAuthoringPack) installed.</span></span>

<span data-ttu-id="05312-109">OPS は、すべての新しいリポジトリについて、Markdig を標準としており、古いリポジトリは Markdig に移行されています。</span><span class="sxs-lookup"><span data-stu-id="05312-109">OPS has standardized on Markdig for all new repos, and older repos are migrating to Markdig.</span></span> <span data-ttu-id="05312-110">[https://babelmark.github.io/](https://babelmark.github.io/) では、Markdown のレンダリングを Markdig と他のエンジンで比較テストできます。</span><span class="sxs-lookup"><span data-stu-id="05312-110">You can test the rendering of Markdown in Markdig vs. other engines at [https://babelmark.github.io/](https://babelmark.github.io/).</span></span>

## <a name="alerts-note-tip-important-caution-warning"></a><span data-ttu-id="05312-111">アラート (注記、ヒント、重要、注意、警告)</span><span class="sxs-lookup"><span data-stu-id="05312-111">Alerts (Note, Tip, Important, Caution, Warning)</span></span>

<span data-ttu-id="05312-112">アラートは、docs.microsoft.com 上でレンダリングされるブロック引用を作成するための OPS 固有の Markdown 拡張です。その色とアイコンでコンテンツの重要性を示します。</span><span class="sxs-lookup"><span data-stu-id="05312-112">Alerts is an OPS-specific Markdown extension to create block quotes that render on docs.microsoft.com with colors and icons that indicate the significance of the content.</span></span> <span data-ttu-id="05312-113">次の種類のアラートがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="05312-113">The following alert types are supported:</span></span>

```markdown
> [!NOTE]
> Information the user should notice even if skimming.

> [!TIP]
> Optional information to help a user be more successful.

> [!IMPORTANT]
> Essential information required for user success.

> [!CAUTION]
> Negative potential consequences of an action.

> [!WARNING]
> Dangerous certain consequences of an action.
```

<span data-ttu-id="05312-114">これらのアラートは docs.microsoft.com 上で次のように表示されます。</span><span class="sxs-lookup"><span data-stu-id="05312-114">These alerts look like this on docs.microsoft.com:</span></span>

> [!NOTE]
> <span data-ttu-id="05312-115">Information the user should notice even if skimming. (ざっと読む場合でも、ユーザーは注意するべき情報。)</span><span class="sxs-lookup"><span data-stu-id="05312-115">Information the user should notice even if skimming.</span></span>

> [!TIP]
> <span data-ttu-id="05312-116">Optional information to help a user be more successful. (ユーザーにさらなる好結果を与える任意の情報。)</span><span class="sxs-lookup"><span data-stu-id="05312-116">Optional information to help a user be more successful.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="05312-117">Essential information required for user success. (ユーザーが好結果を得るために必須となる情報。)</span><span class="sxs-lookup"><span data-stu-id="05312-117">Essential information required for user success.</span></span>

> [!CAUTION]
> <span data-ttu-id="05312-118">Negative potential consequences of an action. (ある行動で起こりえる良くない結果。)</span><span class="sxs-lookup"><span data-stu-id="05312-118">Negative potential consequences of an action.</span></span>

> [!WARNING]
> <span data-ttu-id="05312-119">Dangerous certain consequences of an action. (ある行動で起こるいくつかの危険な結果。)</span><span class="sxs-lookup"><span data-stu-id="05312-119">Dangerous certain consequences of an action.</span></span>

## <a name="code-snippets"></a><span data-ttu-id="05312-120">コード スニペット</span><span class="sxs-lookup"><span data-stu-id="05312-120">Code snippets</span></span>

<span data-ttu-id="05312-121">Markdown ファイルにはコード スニペットを埋め込むことができます。</span><span class="sxs-lookup"><span data-stu-id="05312-121">You can embed code snippets in your Markdown files:</span></span>

```markdown
[!code-<language>[<name>](<codepath><queryoption><queryoptionvalue> "<title>")]
```

## <a name="headings"></a><span data-ttu-id="05312-122">見出し</span><span class="sxs-lookup"><span data-stu-id="05312-122">Headings</span></span>

<span data-ttu-id="05312-123">OPS では、6 つのレベルの Markdown 見出しがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="05312-123">OPS supports six levels of Markdown headings:</span></span>

```markdown
# This is a first level heading (H1)

## This is a second level heading (H2)

...

###### This is a sixth level heading (H6)
```

- <span data-ttu-id="05312-124">最後の `#` と見出しテキストの間にスペースを入れる必要があります。</span><span class="sxs-lookup"><span data-stu-id="05312-124">There must be a space between the last `#` and heading text.</span></span>
- <span data-ttu-id="05312-125">Markdown ファイルごとに与える H1 は 1 つだけにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="05312-125">Each Markdown file must have one and only one H1.</span></span>
- <span data-ttu-id="05312-126">H1 は YML メタデータ ブロックの後ろに来る、ファイルで最初のコンテンツにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="05312-126">The H1 must be the first content in the file after the YML metadata block.</span></span>
- <span data-ttu-id="05312-127">H2 は右側に自動的に表示され、発行されたファイルのメニューのナビゲーションとなります。</span><span class="sxs-lookup"><span data-stu-id="05312-127">H2s automatically appear in the right-hand navigating menu of the published file.</span></span> <span data-ttu-id="05312-128">これより下のレベルの見出しは表示されません。そのため、閲覧者がコンテンツを移動する支えになるように H2 を戦略的に利用してください。</span><span class="sxs-lookup"><span data-stu-id="05312-128">Lower-level headings do not, so use H2s strategically to help readers navigate your content.</span></span>
- <span data-ttu-id="05312-129">`<h1>` など、HMTL 見出しは推奨されません。場合によっては、ビルド警告を発生させます。</span><span class="sxs-lookup"><span data-stu-id="05312-129">HMTL headings, such as `<h1>`, are not recommended and in some cases will cause build warnings.</span></span>
- <span data-ttu-id="05312-130">[ブックマーク](#bookmark-links)を利用し、ファイル内で個別の見出しにリンクできます。</span><span class="sxs-lookup"><span data-stu-id="05312-130">You can link to individual headings in a file via [bookmarks](#bookmark-links).</span></span>

## <a name="html"></a><span data-ttu-id="05312-131">HTML</span><span class="sxs-lookup"><span data-stu-id="05312-131">HTML</span></span>

<span data-ttu-id="05312-132">Markdown ではインライン HTML がサポートされていますが、OPS 経由の公開には HTML は推奨されません。値の一覧が限られていない限り、ビルドのエラーまたは警告を発生させます。</span><span class="sxs-lookup"><span data-stu-id="05312-132">Although Markdown supports inline HTML, HTML is not recommended for publishing via OPS, and except for a limited list of values will cause build errors or warnings.</span></span> <!--For more information, see HTML Whitelist. // do we want to add the whitelist? -->

## <a name="images"></a><span data-ttu-id="05312-133">イメージ</span><span class="sxs-lookup"><span data-stu-id="05312-133">Images</span></span>

<span data-ttu-id="05312-134">イメージをインクルードするための構文は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="05312-134">The syntax to include an image is:</span></span>

```markdown
![[alt text]](<folderPath>)

Example:
![alt text for image](../images/Introduction.png)
```

<span data-ttu-id="05312-135">`alt text` はイメージの簡単な説明であり、`<folder path>` はイメージの相対パスです。</span><span class="sxs-lookup"><span data-stu-id="05312-135">Where `alt text` is a brief description of the image and `<folder path>` is a relative path to the image.</span></span> <span data-ttu-id="05312-136">目が不自由な人のためにスクリーン リーダー用の代替テキストが必要になります。</span><span class="sxs-lookup"><span data-stu-id="05312-136">Alternate text is required for screen readers for the visually impaired.</span></span> <span data-ttu-id="05312-137">イメージをレンダリングできないサイト バグがある場合にも役立ちます。</span><span class="sxs-lookup"><span data-stu-id="05312-137">It is also useful if there is a site bug where the image cannot render.</span></span>

<span data-ttu-id="05312-138">イメージはドキュメント セット内の `/media` フォルダーに格納してください。</span><span class="sxs-lookup"><span data-stu-id="05312-138">Images should be stored in a `/media` folder within your doc set.</span></span> <span data-ttu-id="05312-139">イメージには既定で次の種類のファイルがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="05312-139">The following file types are supported by default for images:</span></span>

- <span data-ttu-id="05312-140">.jpg</span><span class="sxs-lookup"><span data-stu-id="05312-140">.jpg</span></span>
- <span data-ttu-id="05312-141">.png</span><span class="sxs-lookup"><span data-stu-id="05312-141">.png</span></span>

<span data-ttu-id="05312-142">ドキュメント セットの docfx.json ファイル<!--add link to reference when available--> にリソースとして追加することで、他の種類のイメージのサポートを追加できます。</span><span class="sxs-lookup"><span data-stu-id="05312-142">You can add support for other image types by adding them as resources to the docfx.json file<!--add link to reference when available--> for your doc set.</span></span>

## <a name="links"></a><span data-ttu-id="05312-143">リンク</span><span class="sxs-lookup"><span data-stu-id="05312-143">Links</span></span>

<span data-ttu-id="05312-144">多くの場合、OPS では、他のファイルやリンクへの標準 Markdown リンクが使用されます。</span><span class="sxs-lookup"><span data-stu-id="05312-144">In most cases, OPS uses standard Markdown links to other files and pages.</span></span> <span data-ttu-id="05312-145">リンクの種類については、下のセクションに説明があります。</span><span class="sxs-lookup"><span data-stu-id="05312-145">The types of links are described in subsections below.</span></span>

> [!TIP]
> <span data-ttu-id="05312-146">Docs Authoring Pack for VS Code を利用すれば、パスを理解する面倒な作業なく、相対的なリンクとブックマークを正しく挿入できます。</span><span class="sxs-lookup"><span data-stu-id="05312-146">The Docs Authoring Pack for VS Code can help insert relative links and bookmarks correctly without the tedium of figuring out the paths!</span></span>

> [!IMPORTANT]
> <span data-ttu-id="05312-147">Microsoft サイトへのリンクに en-us のようなロケール コードを含めないでください。</span><span class="sxs-lookup"><span data-stu-id="05312-147">Do not include locale codes, such as en-us, in your links to Microsoft sites.</span></span> <span data-ttu-id="05312-148">ハードコーディングされたロケール コードはローカライズされたコンテンツのレンダリングを妨げます。他のロケールのお客様に不自由を与えることになり、また、大きなローカライズ コストを発生させます。</span><span class="sxs-lookup"><span data-stu-id="05312-148">Hard-coded locale codes prevent localized content from rendering, which is a bad customer experience for users in other locales and incurs significant localization costs.</span></span> <span data-ttu-id="05312-149">ブラウザーから URL をコピーすると、既定ではロケール コードが含まれます。そのため、リンクを作成するとき、手動で削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="05312-149">When you copy a URL from a browser, the locale code is included by default, so you need to manually delete it when you create your link.</span></span> <span data-ttu-id="05312-150">たとえば、次のような URL を使用します。</span><span class="sxs-lookup"><span data-stu-id="05312-150">For example, use:</span></span>
>
> `[Microsoft](https://www.microsoft.com)`
>
> <span data-ttu-id="05312-151">次のような URL は使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="05312-151">Not:</span></span>
>
> `[Microsoft](https://www.microsoft.com/en-us/)`

### <a name="relative-links-to-files-in-the-same-doc-set"></a><span data-ttu-id="05312-152">同じドキュメント セットのファイルの相対リンク</span><span class="sxs-lookup"><span data-stu-id="05312-152">Relative links to files in the same doc set</span></span>

<span data-ttu-id="05312-153">相対パスとは、現在のファイルから見た目的のファイルまでのパスです。</span><span class="sxs-lookup"><span data-stu-id="05312-153">A relative path is the path to the target file relative to the current file.</span></span> <span data-ttu-id="05312-154">OPS の場合、同じドキュメント セット内で別のファイルへのリンクの相対パスを利用できます。</span><span class="sxs-lookup"><span data-stu-id="05312-154">In OPS, you can use a relative path to link to another file within the same doc set.</span></span> <span data-ttu-id="05312-155">相対パスの構文は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="05312-155">The syntax for a relative path is as follows:</span></span>

```markdown
[link text](../../folder/filename.md)
```

<span data-ttu-id="05312-156">`../` は階層で 1 つ上を示します。</span><span class="sxs-lookup"><span data-stu-id="05312-156">Where `../` indicates one level above in the hierarchy.</span></span>

- <span data-ttu-id="05312-157">相対パスはビルド中に解決されますが、その中で .md 拡張が削除されます。</span><span class="sxs-lookup"><span data-stu-id="05312-157">The relative path will be resolved during the build, including removal of the .md extension.</span></span>
- <span data-ttu-id="05312-158">"../" を使用して親フォルダー内のファイルにリンクできますが、そのファイルは同じドキュメント セット内に置かれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="05312-158">You can use "../" to link to a file in the parent folder, but that file has to be in the same doc set.</span></span> <span data-ttu-id="05312-159">"../" を使用して別のドキュメント セット フォルダー内のファイルにリンクすることはできません。</span><span class="sxs-lookup"><span data-stu-id="05312-159">You cannot use "../" to link to a file in another doc set folder.</span></span>
- <span data-ttu-id="05312-160">OPS は、"~" で始まる特殊な形式の相対パスもサポートされています (~/foo/bar.md など)。</span><span class="sxs-lookup"><span data-stu-id="05312-160">OPS also supports a special form of relative path that starts with "~" (for example, ~/foo/bar.md).</span></span> <span data-ttu-id="05312-161">この構文は、ドキュメント セットのルート フォルダーから相対的に見たファイルを示しています。</span><span class="sxs-lookup"><span data-stu-id="05312-161">This syntax indicates a file relative to the root folder of a doc set.</span></span> <span data-ttu-id="05312-162">この種類のパスも、ビルド中に検証および解決されます。</span><span class="sxs-lookup"><span data-stu-id="05312-162">This kind of path is also validated and resolved during the build.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="05312-163">相対パスにファイル拡張子を含めてください。</span><span class="sxs-lookup"><span data-stu-id="05312-163">Include the file extension in the relative path.</span></span> <span data-ttu-id="05312-164">その相対パスの目的ファイルの存在がビルドで検証されます。</span><span class="sxs-lookup"><span data-stu-id="05312-164">Build validates the existence of the target file of that relative path.</span></span> <span data-ttu-id="05312-165">相対パスにファイル拡張子が含まれない場合、ビルドにより、リンクが壊れていると警告されます。</span><span class="sxs-lookup"><span data-stu-id="05312-165">If relative path does not include file extension, it is likely build will report a warning of broken link.</span></span> <span data-ttu-id="05312-166">たとえば、次のような URL を使用します。</span><span class="sxs-lookup"><span data-stu-id="05312-166">For example, use:</span></span>
>
> `[link text](../../folder/filename.md)`
>
> <span data-ttu-id="05312-167">次のような URL は使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="05312-167">Not:</span></span>
>
> `[link text](../../folder/filename)`

### <a name="absolute-links-to-other-files-in-ops"></a><span data-ttu-id="05312-168">OPS の他のファイルへの絶対リンク</span><span class="sxs-lookup"><span data-stu-id="05312-168">Absolute links to other files in OPS</span></span>

```markdown
[Azure and Linux](/articles/virtual-machines/linux/overview)
```

<span data-ttu-id="05312-169">ファイル拡張子 (.md) を含めません。</span><span class="sxs-lookup"><span data-stu-id="05312-169">Do not include the file extension (.md).</span></span> <span data-ttu-id="05312-170">Azure "articles" ドキュメント セットの外から Linux 概要ファイルにリンクされています。</span><span class="sxs-lookup"><span data-stu-id="05312-170">This links to the Linux overview file from outside the Azure "articles" doc set.</span></span>

### <a name="links-to-external-sites"></a><span data-ttu-id="05312-171">外部サイトへのリンク</span><span class="sxs-lookup"><span data-stu-id="05312-171">Links to external sites</span></span>

```markdown
[Microsoft](https://www.microsoft.com)
```

<span data-ttu-id="05312-172">別の Web ページへの URL ベースのリンク (https:// を含める必要があります)。</span><span class="sxs-lookup"><span data-stu-id="05312-172">URL-based link to another web page (must include https://).</span></span>

### <a name="bookmark-links"></a><span data-ttu-id="05312-173">ブックマーク リンク</span><span class="sxs-lookup"><span data-stu-id="05312-173">Bookmark links</span></span>

<span data-ttu-id="05312-174">同じリポジトリにおける別ファイルの見出しへのブックマーク リンクは次のようになります。</span><span class="sxs-lookup"><span data-stu-id="05312-174">Bookmark link to a heading in another file in the same repo:</span></span>

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

<span data-ttu-id="05312-175">現在のファイルにある見出しへのブックマーク リンクは次のようになります。</span><span class="sxs-lookup"><span data-stu-id="05312-175">Bookmark link to a heading in the current file:</span></span>

```markdown
[Managed Disks](#managed-disks)
```

<span data-ttu-id="05312-176">ハッシュ タグの後ろに句読点を取り除いた見出し語を続けます。スペースはダッシュに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="05312-176">Use a hash tag followed by the words of the heading with punctuation removed and spaces replaced with dashes.</span></span>

### <a name="explicit-anchor-links"></a><span data-ttu-id="05312-177">明示的なアンカー リンク</span><span class="sxs-lookup"><span data-stu-id="05312-177">Explicit anchor links</span></span>

<span data-ttu-id="05312-178">`<a>` HTML タグを使用する明示的なアンカー リンクは、ハブ ページと待ち受けページを除き、**必須ではないか、推奨されません**。</span><span class="sxs-lookup"><span data-stu-id="05312-178">Explicit anchor links using the `<a>` HTML tag are **not required or recommended** except in hub and landing pages.</span></span> <span data-ttu-id="05312-179">一般的な Markdown ファイルでは、前述のブックマークを使用してください。</span><span class="sxs-lookup"><span data-stu-id="05312-179">Use bookmarks as described above in general Markdown files.</span></span> <span data-ttu-id="05312-180">ハブ ページと待ち受けページについては、アンカーを次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="05312-180">For hub and landing pages, use anchors as follows:</span></span>

<span data-ttu-id="05312-181">`## <a id="AnchorText"> </a>Header text` または `## <a name="AnchorText"> </a>Header text`</span><span class="sxs-lookup"><span data-stu-id="05312-181">`## <a id="AnchorText"> </a>Header text` or `## <a name="AnchorText"> </a>Header text`</span></span>

<span data-ttu-id="05312-182">明示的なアンカーにリンクするには、次の構文を使用します。</span><span class="sxs-lookup"><span data-stu-id="05312-182">To link to explicit anchors, use the following syntax:</span></span>

```markdown
To go to a section on the same page:
[text](#AnchorText)

To go to a section on another page.
[text](FileName.md#AnchorText)
```

### <a name="xref-cross-reference-links"></a><span data-ttu-id="05312-183">XREF (相互参照) リンク</span><span class="sxs-lookup"><span data-stu-id="05312-183">XREF (cross reference) links</span></span>

<span data-ttu-id="05312-184">現在のドキュメント セットまたは他のドキュメント セットにある自動生成 API 参照ページにリンクするには、一意の ID (UID) を持つ XREF リンクを使用します。</span><span class="sxs-lookup"><span data-stu-id="05312-184">To link to auto-generated API references pages in the current doc set or other doc sets, use XREF links with the unique ID (UID).</span></span>

> [!NOTE]
> <span data-ttu-id="05312-185">他のドキュメント セットにある API 参照ページを参照するには、`docfx.json` ファイルで `xrefService` 構成を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="05312-185">To reference API reference pages in other doc sets, you need to add `xrefService` configuration in `docfx.json` file.</span></span>
> ```
> "build": {
>   ...
>   "xrefService": [ "https://xref.docs.microsoft.com/query?uid={uid}" ]
> }
> ```

<span data-ttu-id="05312-186">UID は、クラスとメンバーの完全修飾名に相当します。</span><span class="sxs-lookup"><span data-stu-id="05312-186">The UID equates to the fully qualified class and member name.</span></span> <span data-ttu-id="05312-187">UID の後ろに \* を追加すると、リンクは固有の API ではなく、オーバーロードのページを表すようになります。</span><span class="sxs-lookup"><span data-stu-id="05312-187">If you add a \* after the UID, the link then represents the overload page and not a specific API.</span></span> <span data-ttu-id="05312-188">たとえば、`List<T>.BinarySearch*` を使用すると、`List<T>.BinarySearch(T, IComparer<T>)` のような固有のオーバーロードにリンクする代わりに BinarySearch Method ページにリンクします。</span><span class="sxs-lookup"><span data-stu-id="05312-188">For example, use `List<T>.BinarySearch*` to link to the BinarySearch Method page instead of linking to a specific overload such as `List<T>.BinarySearch(T, IComparer<T>)`.</span></span>

<span data-ttu-id="05312-189">次のいずれかの構文を使用できます。</span><span class="sxs-lookup"><span data-stu-id="05312-189">You can use one of the following syntaxes:</span></span>

- <span data-ttu-id="05312-190">自動リンク: `<xref:UID> or <xref:UID?displayProperty=nameWithType>`</span><span class="sxs-lookup"><span data-stu-id="05312-190">Auto-link: `<xref:UID> or <xref:UID?displayProperty=nameWithType>`</span></span>

  <span data-ttu-id="05312-191">任意の `displayProperty` クエリ パラメーターにより、完全修飾のリンク テキストが生成されます。</span><span class="sxs-lookup"><span data-stu-id="05312-191">The optional `displayProperty` query parameter produces a fully qualified link text.</span></span> <span data-ttu-id="05312-192">既定では、リンク テキストに表示されるのはメンバー名または型名のみです。</span><span class="sxs-lookup"><span data-stu-id="05312-192">By default, link text shows only the member or type name.</span></span>

- <span data-ttu-id="05312-193">マークダウン リンク: `[link text](xref:UID)`</span><span class="sxs-lookup"><span data-stu-id="05312-193">Markdown link: `[link text](xref:UID)`</span></span>
  
  <span data-ttu-id="05312-194">表示されるリンク テキストをカスタマイズする場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="05312-194">Use when you want to customize the link text displayed.</span></span>

<span data-ttu-id="05312-195">例:</span><span class="sxs-lookup"><span data-stu-id="05312-195">Examples:</span></span>

- <span data-ttu-id="05312-196">`<xref:System.String>` は "String" としてレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="05312-196">`<xref:System.String>` renders as "String".</span></span>
- <span data-ttu-id="05312-197">`<xref:System.String?displayProperty=nameWithType>` は "System.String" としてレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="05312-197">`<xref:System.String?displayProperty=nameWithType>` renders as "System.String".</span></span>
- <span data-ttu-id="05312-198">`[String class](xref:System.String)` は "String class" としてレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="05312-198">`[String class](xref:System.String)` renders as "String class".</span></span>

<span data-ttu-id="05312-199">現在、UID を検索する簡単な方法はありません。</span><span class="sxs-lookup"><span data-stu-id="05312-199">Right now, there is no easy way to find the UIDs.</span></span> <span data-ttu-id="05312-200"><!-- ? -->API の UID を検索する最善の方法は、リンクする API のページのソースを表示し、ms.assetid という値を検索することです。</span><span class="sxs-lookup"><span data-stu-id="05312-200"><!-- ? -->The best way to find the UID for an API is to view the source for the API page you want to link to and find the ms.assetid value.</span></span> <span data-ttu-id="05312-201">個別のオーバーロードの値は、ソースには表示されません。</span><span class="sxs-lookup"><span data-stu-id="05312-201">Individual overload values are not shown in the source.</span></span> <span data-ttu-id="05312-202">将来的に、より優れたシステムを提供できるように取り組んでいます。</span><span class="sxs-lookup"><span data-stu-id="05312-202">We're working on having a better system in the future.</span></span>

<span data-ttu-id="05312-203">UID に特殊文字 \`、\#、\* が含まれている場合、UID の値は、それぞれ `%60`、`%23`、`%2A` のように HTML エンコードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="05312-203">When the UID contains the special characters \`, \#, or \*, the UID value needs to be HTML encoded as `%60`, `%23`, and `%2A`, respectively.</span></span> <span data-ttu-id="05312-204">かっこがエンコードされている場合もありますが、これは必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="05312-204">You'll sometimes see parentheses encoded but it's not a requirement.</span></span>

<span data-ttu-id="05312-205">例:</span><span class="sxs-lookup"><span data-stu-id="05312-205">Examples:</span></span>

- <span data-ttu-id="05312-206">System.Threading.Tasks.Task\`1 は、`System.Threading.Tasks.Task%601` になります</span><span class="sxs-lookup"><span data-stu-id="05312-206">System.Threading.Tasks.Task\`1 becomes `System.Threading.Tasks.Task%601`</span></span>
- <span data-ttu-id="05312-207">System.Exception.\#ctor は、`System.Exception.%23ctor` になります</span><span class="sxs-lookup"><span data-stu-id="05312-207">System.Exception.\#ctor becomes `System.Exception.%23ctor`</span></span>
- <span data-ttu-id="05312-208">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) は、`System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29` になります</span><span class="sxs-lookup"><span data-stu-id="05312-208">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) becomes  `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span></span>

<!-- leave out of Contributor Guide for now
Using XREF may require some configuration. For more information, see XREF Service.
-->

## <a name="lists-numbered-bulleted-checklist"></a><span data-ttu-id="05312-209">リスト (番号付き、箇条書き、チェックリスト)</span><span class="sxs-lookup"><span data-stu-id="05312-209">Lists (Numbered, Bulleted, Checklist)</span></span>

### <a name="numbered-list"></a><span data-ttu-id="05312-210">番号付きリスト</span><span class="sxs-lookup"><span data-stu-id="05312-210">Numbered list</span></span>

<span data-ttu-id="05312-211">番号付きリストを作成するには、すべての 1 を使用できます。これは公開されると、連続する一覧としてレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="05312-211">To create a numbered list, you can use all 1s, which are rendered as a sequential list when published.</span></span> <span data-ttu-id="05312-212">ソースを読みやすくするために、リストをインクリメントできます。</span><span class="sxs-lookup"><span data-stu-id="05312-212">For increased source readability, you can increment your lists.</span></span>

<span data-ttu-id="05312-213">入れ子になっているリストなど、リストには文字を使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="05312-213">Do not use letters in lists, including nested lists.</span></span> <span data-ttu-id="05312-214">OPS 経由で公開するとき、正しくレンダリングされません。</span><span class="sxs-lookup"><span data-stu-id="05312-214">They do not render correctly when published via OPS.</span></span> <span data-ttu-id="05312-215">番号を使用する入れ子リストは、公開されると、小文字としてレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="05312-215">Nested lists using numbers will render as lowercase letters when published.</span></span> <span data-ttu-id="05312-216">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="05312-216">For example:</span></span>

```markdown
1. This is
1. a parent numbered list
   1. and this is
   1. a nested numbered list
1. (fin)
```

<span data-ttu-id="05312-217">これは次のようにレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="05312-217">This renders as follows:</span></span>

1. <span data-ttu-id="05312-218">This is</span><span class="sxs-lookup"><span data-stu-id="05312-218">This is</span></span>
1. <span data-ttu-id="05312-219">a parent numbered list</span><span class="sxs-lookup"><span data-stu-id="05312-219">a parent numbered list</span></span>
   1. <span data-ttu-id="05312-220">and this is</span><span class="sxs-lookup"><span data-stu-id="05312-220">and this is</span></span>
   1. <span data-ttu-id="05312-221">a nested numbered list</span><span class="sxs-lookup"><span data-stu-id="05312-221">a nested numbered list</span></span>
1. <span data-ttu-id="05312-222">(fin)</span><span class="sxs-lookup"><span data-stu-id="05312-222">(fin)</span></span>

### <a name="bulleted-list"></a><span data-ttu-id="05312-223">箇条書き</span><span class="sxs-lookup"><span data-stu-id="05312-223">Bulleted list</span></span>

<span data-ttu-id="05312-224">箇条書きを作成するには、`-` の後ろにスペースを入れてから各行を続けます。</span><span class="sxs-lookup"><span data-stu-id="05312-224">To create a bulleted list, use `-` followed by a space at the beginning of each line:</span></span>

```markdown
- This is
- a parent bulleted list
  - and this is
  - a nested bulleted list
- All done!
```

<span data-ttu-id="05312-225">これは次のようにレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="05312-225">This renders as follows:</span></span>

- <span data-ttu-id="05312-226">This is</span><span class="sxs-lookup"><span data-stu-id="05312-226">This is</span></span>
- <span data-ttu-id="05312-227">a parent bulleted list</span><span class="sxs-lookup"><span data-stu-id="05312-227">a parent bulleted list</span></span>
  - <span data-ttu-id="05312-228">and this is</span><span class="sxs-lookup"><span data-stu-id="05312-228">and this is</span></span>
  - <span data-ttu-id="05312-229">a nested bulleted list</span><span class="sxs-lookup"><span data-stu-id="05312-229">a nested bulleted list</span></span>
- <span data-ttu-id="05312-230">All done!</span><span class="sxs-lookup"><span data-stu-id="05312-230">All done!</span></span>

### <a name="checklist"></a><span data-ttu-id="05312-231">チェックリスト</span><span class="sxs-lookup"><span data-stu-id="05312-231">Checklist</span></span>

<span data-ttu-id="05312-232">チェックリストは、カスタム Markdown 拡張経由で docs.microsoft.com (のみ) で使用する場合に利用できます。</span><span class="sxs-lookup"><span data-stu-id="05312-232">Checklists are available for use on docs.microsoft.com (only) via a custom Markdown extension:</span></span>

```markdown
> [!div class="checklist"]
> * List item 1
> * List item 2
> * List item 3
```

<span data-ttu-id="05312-233">このサンプルは docs.microsoft.com で次のようにレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="05312-233">This example renders on docs.microsoft.com like this:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="05312-234">List item 1</span><span class="sxs-lookup"><span data-stu-id="05312-234">List item 1</span></span>
> * <span data-ttu-id="05312-235">List item 2</span><span class="sxs-lookup"><span data-stu-id="05312-235">List item 2</span></span>
> * <span data-ttu-id="05312-236">List item 3</span><span class="sxs-lookup"><span data-stu-id="05312-236">List item 3</span></span>

<span data-ttu-id="05312-237">"これから学習する内容" や "今回学習した内容" をまとめる目的で、記事の冒頭や最後でチェックリストを使用します。</span><span class="sxs-lookup"><span data-stu-id="05312-237">Use checklists at the beginning or end of an article to summarize "What will you learn" or "What have you learned" content.</span></span> <span data-ttu-id="05312-238">記事全体でランダムなチェックリストを追加しないでください。</span><span class="sxs-lookup"><span data-stu-id="05312-238">Do not add random checklists throughout your articles.</span></span>
<!-- is this guidance still accurate? -->

## <a name="next-step-action"></a><span data-ttu-id="05312-239">次のステップ アクション</span><span class="sxs-lookup"><span data-stu-id="05312-239">Next step action</span></span>

<span data-ttu-id="05312-240">カスタム拡張を使用し、次のステップ アクション ボタンを docs.microsoft.com (のみ) のページに追加できます。</span><span class="sxs-lookup"><span data-stu-id="05312-240">You can use a custom extension to add a next step action button to pages on docs.microsoft.com (only).</span></span>

<span data-ttu-id="05312-241">構文は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="05312-241">The syntax is as follows:</span></span>

```markdown
> [!div class="nextstepaction"]
> [button text](link to topic)
```

<span data-ttu-id="05312-242">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="05312-242">For example:</span></span>

```markdown
> [!div class="nextstepaction"]
> [Learn about basic style](style-quick-start.md)
```

<span data-ttu-id="05312-243">これは次のようにレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="05312-243">This renders as follows:</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="05312-244">Learn about basic style</span><span class="sxs-lookup"><span data-stu-id="05312-244">Learn about basic style</span></span>](style-quick-start.md)

<span data-ttu-id="05312-245">別の Web ページへの Markdown リンクを含め、次のステップ アクションでは、サポートされているあらゆるリンクを使用できます。</span><span class="sxs-lookup"><span data-stu-id="05312-245">You can use any supported link in a next step action, including a Markdown link to another web page.</span></span> <span data-ttu-id="05312-246">ほとんどの場合、次のアクション リンクは同じドキュメント セット内の別のファイルへの相対リンクになります。</span><span class="sxs-lookup"><span data-stu-id="05312-246">In most cases, the next action link will be a relative link to another file in the same doc set.</span></span>

## <a name="section-definition"></a><span data-ttu-id="05312-247">セクション定義</span><span class="sxs-lookup"><span data-stu-id="05312-247">Section definition</span></span>

<span data-ttu-id="05312-248"><!-- more info about this would be helpful! --> 場合によっては、セクションを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="05312-248"><!-- more info about this would be helpful! --> You might need to define a section.</span></span> <span data-ttu-id="05312-249">この構文は多くの場合、コード表に使用されます。</span><span class="sxs-lookup"><span data-stu-id="05312-249">This syntax is mostly used for code tables.</span></span>
<span data-ttu-id="05312-250">次の例を参照してください。</span><span class="sxs-lookup"><span data-stu-id="05312-250">See the following example:</span></span>

````
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```
````

<span data-ttu-id="05312-251">前述のブロック引用 Markdown テキストは、次のように表示されます。</span><span class="sxs-lookup"><span data-stu-id="05312-251">The preceding blockquote Markdown text will be rendered as:</span></span>
> [!div class="tabbedCodeSnippets" data-resources="OutlookServices.Calendar"]
> ```cs
> <cs code text>
> ```
> ```javascript
> <js code text>
> ```

## <a name="selectors"></a><span data-ttu-id="05312-252">セレクター</span><span class="sxs-lookup"><span data-stu-id="05312-252">Selectors</span></span>

<span data-ttu-id="05312-253"><!-- could be more clear! --> 同じ記事に対してさまざまなページをつなげるなら、セレクターを使用できます。</span><span class="sxs-lookup"><span data-stu-id="05312-253"><!-- could be more clear! --> You can use a selector when you want to connect different pages for the same article.</span></span> <span data-ttu-id="05312-254">閲覧者はページを切り替えることができます。</span><span class="sxs-lookup"><span data-stu-id="05312-254">Readers can then switch between those pages.</span></span>

> [!NOTE]
> <span data-ttu-id="05312-255">この拡張機能は、docs.microsoft.com と MSDN で機能が異なります。</span><span class="sxs-lookup"><span data-stu-id="05312-255">This extension works differently between docs.microsoft.com and MSDN.</span></span> <!-- should we keep info about MSDN? If so say how they differ?-->

### <a name="single-selector"></a><span data-ttu-id="05312-256">単一セレクター</span><span class="sxs-lookup"><span data-stu-id="05312-256">Single selector</span></span>

```
> [!div class="op_single_selector"]
> - [Universal Windows](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [Baidu](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)
```

<span data-ttu-id="05312-257">これは次のようにレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="05312-257">... will be rendered like this:</span></span>

> [!div class="op_single_selector"]
> - [Universal Windows](how-to-write-use-markdown.md)
> - [Windows Phone](how-to-write-use-markdown.md)
> - [iOS](how-to-write-use-markdown.md)
> - [Android](how-to-write-use-markdown.md)
> - [Kindle](how-to-write-use-markdown.md)
> - [Baidu](how-to-write-use-markdown.md)
> - [Xamarin.iOS](how-to-write-use-markdown.md)
> - [Xamarin.Android](how-to-write-use-markdown.md)

### <a name="multi-selector"></a><span data-ttu-id="05312-266">複数のセレクター</span><span class="sxs-lookup"><span data-stu-id="05312-266">Multi-selector</span></span>

```
> [!div class="op_multi_selector" title1="Platform" title2="Backend"]
> - [(iOS | .NET)](how-to-write-workflows-major.md)
> - [(iOS | JavaScript)](how-to-write-workflows-major.md)
> - [(Windows universal C# | .NET)](how-to-write-workflows-major.md)
> - [(Windows universal C# | Javascript)](how-to-write-workflows-major.md)
> - [(Windows Phone | .NET)](how-to-write-workflows-major.md)
> - [(Windows Phone | Javascript)](how-to-write-workflows-major.md)
> - [(Android | .NET)](how-to-write-workflows-major.md)
> - [(Android | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin iOS | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin Android | Javascript)](how-to-write-workflows-major.md)
```

<span data-ttu-id="05312-267">これは次のようにレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="05312-267">... will be rendered like this:</span></span>

> [!div class="op_multi_selector" title1="Platform" title2="Backend"]
> - [(iOS | .NET)](how-to-write-workflows-major.md)
> - [(iOS | JavaScript)](how-to-write-workflows-major.md)
> - [(Windows universal C# | .NET)](how-to-write-workflows-major.md)
> - [(Windows universal C# | Javascript)](how-to-write-workflows-major.md)
> - [(Windows Phone | .NET)](how-to-write-workflows-major.md)
> - [(Windows Phone | Javascript)](how-to-write-workflows-major.md)
> - [(Android | .NET)](how-to-write-workflows-major.md)
> - [(Android | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin iOS | Javascript)](how-to-write-workflows-major.md)
> - [(Xamarin Android | Javascript)](how-to-write-workflows-major.md)

<!-- uncomment and link when Cory's topic is live
## Tabbed content

Tabs are a Markdown extension for docs.microsoft.com that allow us to present different versions of content, such as procedural steps to accomplish the same task on different platforms, in a tabbed format.

Because the syntax and requirements for tabbed content are fairly complex, they are documented separately in Tabbed Content.
-->

## <a name="tables"></a><span data-ttu-id="05312-278">表</span><span class="sxs-lookup"><span data-stu-id="05312-278">Tables</span></span>

<span data-ttu-id="05312-279">Markdow で表を作成する最も簡単な方法は、パイプと行を使用することです。</span><span class="sxs-lookup"><span data-stu-id="05312-279">The simplest way to create a table in Markdown is to use pipes and lines.</span></span> <span data-ttu-id="05312-280">ヘッダー付きの標準的な表を作成するには、最初の行の後に点線を続けます。</span><span class="sxs-lookup"><span data-stu-id="05312-280">To create a standard table with a header, follow the first line with dashed line:</span></span>

```markdown
|This is   |a simple   |table header|
|----------|-----------|------------|
|table     |data       |here        |
|it doesn't|actually   |have to line up nicely!|
```

<span data-ttu-id="05312-281">これは次のようにレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="05312-281">This renders as follows:</span></span>

|<span data-ttu-id="05312-282">This is</span><span class="sxs-lookup"><span data-stu-id="05312-282">This is</span></span>   |<span data-ttu-id="05312-283">a simple</span><span class="sxs-lookup"><span data-stu-id="05312-283">a simple</span></span>   |<span data-ttu-id="05312-284">table header</span><span class="sxs-lookup"><span data-stu-id="05312-284">table header</span></span>|
|----------|-----------|------------|
|<span data-ttu-id="05312-285">table</span><span class="sxs-lookup"><span data-stu-id="05312-285">table</span></span>     |<span data-ttu-id="05312-286">data</span><span class="sxs-lookup"><span data-stu-id="05312-286">data</span></span>       |<span data-ttu-id="05312-287">here</span><span class="sxs-lookup"><span data-stu-id="05312-287">here</span></span>        |
|<span data-ttu-id="05312-288">it doesn't</span><span class="sxs-lookup"><span data-stu-id="05312-288">it doesn't</span></span>|<span data-ttu-id="05312-289">actually</span><span class="sxs-lookup"><span data-stu-id="05312-289">actually</span></span>   |<span data-ttu-id="05312-290">have to line up nicely!</span><span class="sxs-lookup"><span data-stu-id="05312-290">have to line up nicely!</span></span>||

<span data-ttu-id="05312-291">ヘッダーなしで表を作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="05312-291">You can also create a table without a header.</span></span> <span data-ttu-id="05312-292">たとえば、複数列のリストを作成するには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="05312-292">For example, to create a multiple-column list:</span></span>

```markdown
|   |   |
| - | - |
| This | table |
| has no | header |
```

<span data-ttu-id="05312-293">これは次のようにレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="05312-293">This renders like this:</span></span>

|   |   |
| - | - |
| <span data-ttu-id="05312-294">This</span><span class="sxs-lookup"><span data-stu-id="05312-294">This</span></span> | <span data-ttu-id="05312-295">table</span><span class="sxs-lookup"><span data-stu-id="05312-295">table</span></span> |
| <span data-ttu-id="05312-296">has no</span><span class="sxs-lookup"><span data-stu-id="05312-296">has no</span></span> | <span data-ttu-id="05312-297">header</span><span class="sxs-lookup"><span data-stu-id="05312-297">header</span></span> |

<span data-ttu-id="05312-298">コロンを使用して、列を整列することができます。</span><span class="sxs-lookup"><span data-stu-id="05312-298">You can align the columns by using colons:</span></span>

```markdown
|                  |
|------------------|
|    right aligned:|
|:left aligned     |
|:centered        :|
```

<span data-ttu-id="05312-299">これは次のようにレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="05312-299">Renders as follows:</span></span>

|                  |
|------------------|
|    <span data-ttu-id="05312-300">right aligned:</span><span class="sxs-lookup"><span data-stu-id="05312-300">right aligned:</span></span>|
|<span data-ttu-id="05312-301">:left aligned</span><span class="sxs-lookup"><span data-stu-id="05312-301">:left aligned</span></span>     |
|<span data-ttu-id="05312-302">:centered        :</span><span class="sxs-lookup"><span data-stu-id="05312-302">:centered        :</span></span>|

> [!TIP]
> Docs Authoring Extension for VS Code では、基本的な Markdown 表を簡単に追加できます。
>
> [オンラインの表生成機能](http://www.tablesgenerator.com/markdown_tables)を使用することもできます。

### <a name="mx-tdbreakall"></a><span data-ttu-id="05312-305">mx-tdBreakAll</span><span class="sxs-lookup"><span data-stu-id="05312-305">mx-tdBreakAll</span></span>

> [!IMPORTANT]
> これは docs.microsoft.com サイトでのみ機能します。

<span data-ttu-id="05312-307">Markdown で表を作成すると、表が右側のナビゲーションまで広がって、表が読めなくなることがあります。</span><span class="sxs-lookup"><span data-stu-id="05312-307">If you create a table in Markdown, the table might expand to the right navigation and become unreadable.</span></span> <span data-ttu-id="05312-308">これは、必要に応じて、Docs のレンダリングで表内の改行を許可することで解決できます。</span><span class="sxs-lookup"><span data-stu-id="05312-308">You can solve that by allowing Docs rendering to break the table when needed.</span></span> <span data-ttu-id="05312-309">カスタム クラス `[!div class="mx-tdBreakAll"]` を使用して表を折り返すだけです。</span><span class="sxs-lookup"><span data-stu-id="05312-309">Just wrap up the table with the custom class `[!div class="mx-tdBreakAll"]`.</span></span>

<span data-ttu-id="05312-310">クラス名が `mx-tdBreakAll` の `div` で折り返される 3 行の表の Markdown サンプルを次に示します。</span><span class="sxs-lookup"><span data-stu-id="05312-310">Here is a Markdown sample of a table with three rows that will be wrapped by a `div` with the class name `mx-tdBreakAll`.</span></span>

```markdown
> [!div class="mx-tdBreakAll"]
> |Name|Syntax|Mandatory for silent installation?|Description|
> |-------------|----------|---------|---------|
> |Quiet|/quiet|Yes|Runs the installer, displaying no UI and no prompts.|
> |NoRestart|/norestart|No|Suppresses any attempts to restart. By default, the UI will prompt before restart.|
> |Help|/help|No|Provides help and quick reference. Displays the correct use of the setup command, including a list of all options and behaviors.|
```

<span data-ttu-id="05312-311">これは次のようにレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="05312-311">It will be rendered like this:</span></span>

> [!div class="mx-tdBreakAll"]
> |<span data-ttu-id="05312-312">名前</span><span class="sxs-lookup"><span data-stu-id="05312-312">Name</span></span>|<span data-ttu-id="05312-313">Syntax</span><span class="sxs-lookup"><span data-stu-id="05312-313">Syntax</span></span>|<span data-ttu-id="05312-314">Mandatory for silent installation?</span><span class="sxs-lookup"><span data-stu-id="05312-314">Mandatory for silent installation?</span></span>|<span data-ttu-id="05312-315">Description</span><span class="sxs-lookup"><span data-stu-id="05312-315">Description</span></span>|
> |-------------|----------|---------|---------|
> |<span data-ttu-id="05312-316">Quiet</span><span class="sxs-lookup"><span data-stu-id="05312-316">Quiet</span></span>|<span data-ttu-id="05312-317">/quiet</span><span class="sxs-lookup"><span data-stu-id="05312-317">/quiet</span></span>|<span data-ttu-id="05312-318">Yes</span><span class="sxs-lookup"><span data-stu-id="05312-318">Yes</span></span>|<span data-ttu-id="05312-319">Runs the installer, displaying no UI and no prompts.</span><span class="sxs-lookup"><span data-stu-id="05312-319">Runs the installer, displaying no UI and no prompts.</span></span>|
> |<span data-ttu-id="05312-320">NoRestart</span><span class="sxs-lookup"><span data-stu-id="05312-320">NoRestart</span></span>|<span data-ttu-id="05312-321">/norestart</span><span class="sxs-lookup"><span data-stu-id="05312-321">/norestart</span></span>|<span data-ttu-id="05312-322">No</span><span class="sxs-lookup"><span data-stu-id="05312-322">No</span></span>|<span data-ttu-id="05312-323">Suppresses any attempts to restart.</span><span class="sxs-lookup"><span data-stu-id="05312-323">Suppresses any attempts to restart.</span></span> <span data-ttu-id="05312-324">By default, the UI will prompt before restart.</span><span class="sxs-lookup"><span data-stu-id="05312-324">By default, the UI will prompt before restart.</span></span>|
> |<span data-ttu-id="05312-325">Help</span><span class="sxs-lookup"><span data-stu-id="05312-325">Help</span></span>|<span data-ttu-id="05312-326">/help</span><span class="sxs-lookup"><span data-stu-id="05312-326">/help</span></span>|<span data-ttu-id="05312-327">No</span><span class="sxs-lookup"><span data-stu-id="05312-327">No</span></span>|<span data-ttu-id="05312-328">Provides help and quick reference.</span><span class="sxs-lookup"><span data-stu-id="05312-328">Provides help and quick reference.</span></span> <span data-ttu-id="05312-329">Displays the correct use of the setup command, including a list of all options and behaviors.</span><span class="sxs-lookup"><span data-stu-id="05312-329">Displays the correct use of the setup command, including a list of all options and behaviors.</span></span>|

### <a name="mx-tdcol2breakall"></a><span data-ttu-id="05312-330">mx-tdCol2BreakAll</span><span class="sxs-lookup"><span data-stu-id="05312-330">mx-tdCol2BreakAll</span></span>

> [!IMPORTANT]
> <span data-ttu-id="05312-331">これは docs.microsoft.com サイトでのみ機能します。</span><span class="sxs-lookup"><span data-stu-id="05312-331">This only works on the docs.microsoft.com site.</span></span>

<span data-ttu-id="05312-332">ときどき、表の 2 番目の列に非常に長い単語がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="05312-332">From time to time, you might have very long words in the second column of a table.</span></span> <span data-ttu-id="05312-333">そのような単語を適切に分割するために、前述のような `div` ラッパー構文を使用して `mx-tdCol2BreakAll` クラスを適用できます。</span><span class="sxs-lookup"><span data-stu-id="05312-333">To ensure they are broken apart nicely, you can apply the class `mx-tdCol2BreakAll` by using the `div` wrapper syntax as shown earlier.</span></span>

### <a name="html-tables"></a><span data-ttu-id="05312-334">HTML テーブル</span><span class="sxs-lookup"><span data-stu-id="05312-334">HTML Tables</span></span>

<span data-ttu-id="05312-335">docs.microsoft.com の場合、HTML テーブルは推奨されません。</span><span class="sxs-lookup"><span data-stu-id="05312-335">HTML tables are not recommended for docs.microsoft.com.</span></span> <span data-ttu-id="05312-336">ソースでは人間が読めないようになっています。このことは Markdown の重要な原則の 1 つです。</span><span class="sxs-lookup"><span data-stu-id="05312-336">They are not human readable in the source - which is a key principle of Markdown.</span></span>

<!--If you use HTML tables and your Markdown is not being rendered between the two tables, you need to add a closing `br` tag after the closing `table` tag.

![break HTML tables](media/break-tables.png)
-->

## <a name="videos"></a><span data-ttu-id="05312-337">動画</span><span class="sxs-lookup"><span data-stu-id="05312-337">Videos</span></span>

### <a name="embedding-videos-into-a-markdown-page"></a><span data-ttu-id="05312-338">Markdown ページに動画を埋め込む</span><span class="sxs-lookup"><span data-stu-id="05312-338">Embedding videos into a Markdown page</span></span>

<span data-ttu-id="05312-339">現在のところ、OPS では、次の 3 つの場所に公開された動画がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="05312-339">Currently, OPS can support videos published to one of three locations:</span></span>

- <span data-ttu-id="05312-340">YouTube</span><span class="sxs-lookup"><span data-stu-id="05312-340">YouTube</span></span>
- <span data-ttu-id="05312-341">Channel 9</span><span class="sxs-lookup"><span data-stu-id="05312-341">Channel 9</span></span>
- <span data-ttu-id="05312-342">Microsoft 独自の 'One Player' システム</span><span class="sxs-lookup"><span data-stu-id="05312-342">Microsoft's own 'One Player' system</span></span>

<span data-ttu-id="05312-343">次の構文を使用してビデオを埋め込むと、OPS でこれがレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="05312-343">You can embed a video with the following syntax, and OPS will render it.</span></span>

```markdown
> [!VIDEO <embedded_video_link>]
```

<span data-ttu-id="05312-344">例:</span><span class="sxs-lookup"><span data-stu-id="05312-344">Example:</span></span>

```markdown
> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
```

<span data-ttu-id="05312-345">これは次のようにレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="05312-345">... will be rendered as:</span></span>

```html
<iframe src="https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>

<iframe src="https://www.youtube-nocookie.com/embed/iAtwVM-Z7rY" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
<iframe src="https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS" width="640" height="320" allowFullScreen="true" frameBorder="0"></iframe>
```

<span data-ttu-id="05312-346">公開されたページでは、次のように表示されます。</span><span class="sxs-lookup"><span data-stu-id="05312-346">And it will be displayed like this on published pages:</span></span>

> [!VIDEO https://channel9.msdn.com/Series/Youve-Got-Key-Values-A-Redis-Jump-Start/03/player]

> [!VIDEO https://www.youtube.com/embed/iAtwVM-Z7rY]

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]

> [!IMPORTANT]
> <span data-ttu-id="05312-347">CH9 ビデオの URL は `https` で始まり、`/player` で終わる必要があります。</span><span class="sxs-lookup"><span data-stu-id="05312-347">The CH9 video URL should start with `https` and end with `/player`.</span></span> <span data-ttu-id="05312-348">そうしないと、ビデオだけでなくページ全体が埋め込まれます。</span><span class="sxs-lookup"><span data-stu-id="05312-348">Otherwise, it will embed the whole page instead of the video only.</span></span>

### <a name="uploading-new-videos"></a><span data-ttu-id="05312-349">新しい動画をアップロードする</span><span class="sxs-lookup"><span data-stu-id="05312-349">Uploading new videos</span></span>

<span data-ttu-id="05312-350">新しい動画は次のプロセスでアップロードしてください。</span><span class="sxs-lookup"><span data-stu-id="05312-350">Any new videos should be uploaded using the following process:</span></span>

1. <span data-ttu-id="05312-351">IDWEB で **docs_video_users** グループに参加します。</span><span class="sxs-lookup"><span data-stu-id="05312-351">Join the **docs_video_users** group on IDWEB.</span></span>
1. <span data-ttu-id="05312-352">https://aka.ms/VideoUploadRequest に移動し、動画の詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="05312-352">Go to https://aka.ms/VideoUploadRequest and fill in the details for your video.</span></span> <span data-ttu-id="05312-353">次の項目が必要になります (いずれも公開されません)。</span><span class="sxs-lookup"><span data-stu-id="05312-353">You will need (note that none of these items will be visible to the public):</span></span>
    1. <span data-ttu-id="05312-354">動画のタイトル。</span><span class="sxs-lookup"><span data-stu-id="05312-354">A title for your video.</span></span>
    1. <span data-ttu-id="05312-355">動画が関連する製品/サービスの一覧。</span><span class="sxs-lookup"><span data-stu-id="05312-355">A list of products/services that your video is related to.</span></span>
    1. <span data-ttu-id="05312-356">動画がホストされる対象ページまたは (ページをまだ用意していない場合) ドキュメント セット。</span><span class="sxs-lookup"><span data-stu-id="05312-356">The target page or (if you don’t have the page yet) doc set that your video will be hosted on.</span></span>
    1. <span data-ttu-id="05312-357">動画の MP4 ファイルへのリンク (ファイルを置く場所を用意していない場合、`\\scratch2\scratch\apex` に一時的に置くことができます)。</span><span class="sxs-lookup"><span data-stu-id="05312-357">A link to the MP4 file for your video (if you don’t have a location to put the file, you can put it here temporarily:   `\\scratch2\scratch\apex`).</span></span> <span data-ttu-id="05312-358">MP4 ファイルは 720p 以上にしてください。</span><span class="sxs-lookup"><span data-stu-id="05312-358">MP4 files should be 720p or higher.</span></span>
    1. <span data-ttu-id="05312-359">動画の説明。</span><span class="sxs-lookup"><span data-stu-id="05312-359">A description of the video.</span></span>
1. <span data-ttu-id="05312-360">項目を送信 (保存) します。</span><span class="sxs-lookup"><span data-stu-id="05312-360">Submit (save) that item.</span></span>
1. <span data-ttu-id="05312-361">2 営業日以内に動画がアップロードされます。</span><span class="sxs-lookup"><span data-stu-id="05312-361">Within two business days, the video will get uploaded.</span></span> <span data-ttu-id="05312-362">埋め込みに必要なリンクは作業項目に配置されます。解決されて*戻されます*。</span><span class="sxs-lookup"><span data-stu-id="05312-362">The link you need for embedding will be placed into the work item, and it will be resolved *back to you*.</span></span>
1. <span data-ttu-id="05312-363">動画リンクを取得したら、作業項目を閉じます。</span><span class="sxs-lookup"><span data-stu-id="05312-363">Once you have grabbed the video link, close the work item.</span></span>
1. <span data-ttu-id="05312-364">その後、次の構文を利用し、動画リンクを投稿に追加できます。</span><span class="sxs-lookup"><span data-stu-id="05312-364">The video link can then be added to your post, using this syntax:</span></span>

   ```markdown
   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE1XVQS]
   ```
