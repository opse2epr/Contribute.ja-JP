---
title: ドキュメントを記述するための Markdown の使用方法
description: この記事では、docs.microsoft.com の記事を記述するために使用される Markdown の基礎と参照情報について説明します。
ms.date: 01/29/2019
ms.openlocfilehash: 5235189d11c8c20ac20c91572d8bafcf525fb7c0
ms.sourcegitcommit: fbdd61ae4fb3761aec072732eefcbf2c2dca8011
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/07/2019
ms.locfileid: "55887300"
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="4a552-103">ドキュメントを記述するための Markdown の使用方法</span><span class="sxs-lookup"><span data-stu-id="4a552-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="4a552-104">[docs.microsoft.com](http://docs.microsoft.com) の記事は [Markdown](https://daringfireball.net/projects/markdown/) という読みやすく、しかも簡単に学べる軽量マークアップ言語で記述されます。</span><span class="sxs-lookup"><span data-stu-id="4a552-104">[Docs.microsoft.com](http://docs.microsoft.com) articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="4a552-105">そのため、これは急速に業界標準になりました。</span><span class="sxs-lookup"><span data-stu-id="4a552-105">Because of this, it has quickly become an industry standard.</span></span>

<span data-ttu-id="4a552-106">docs.microsoft.com サイトのバックエンドでは、Open Publishing Services (OPS) が使われています。これは、[Markdig](https://github.com/lunet-io/markdig) を使って解析される [CommonMark](https://commonmark.org/) 準拠のマークダウンをサポートし、また [DocFX Flavored Markdown (DFM)](https://dotnet.github.io/docfx/) もサポートしています。</span><span class="sxs-lookup"><span data-stu-id="4a552-106">The docs.microsoft.com site backend uses Open Publishing Services (OPS) which supports [CommonMark](https://commonmark.org/) compliant markdown parsed through [Markdig](https://github.com/lunet-io/markdig) and also supports [DocFX Flavored Markdown (DFM)](https://dotnet.github.io/docfx/).</span></span> <span data-ttu-id="4a552-107">ほとんどのドキュメントが GitHub に格納され、そこで編集可能であるように、これらのマークダウンの種類のほとんどは [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/) と互換性があります。</span><span class="sxs-lookup"><span data-stu-id="4a552-107">These markdown flavors are mostly compatible with [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), as most docs are stored in GitHub and can be edited there.</span></span> <span data-ttu-id="4a552-108">Markdown の拡張機能を通じて、その他の機能が追加されています。</span><span class="sxs-lookup"><span data-stu-id="4a552-108">Additional functionality is added through Markdown extensions.</span></span>

## <a name="markdown-basics"></a><span data-ttu-id="4a552-109">Markdown の基本</span><span class="sxs-lookup"><span data-stu-id="4a552-109">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="4a552-110">見出し</span><span class="sxs-lookup"><span data-stu-id="4a552-110">Headings</span></span>

<span data-ttu-id="4a552-111">見出しを作成するには、ハッシュ記号 (#) を次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="4a552-111">To create a heading, you use a hash mark (#), as follows:</span></span>

```markdown
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

<span data-ttu-id="4a552-112">見出しは atx 形式で作成してください。つまり、行の先頭で 1 つから 6 つまでのハッシュ文字 (#) を使用して見出しを示し、H1 から H6 までの HTML 見出しレベルに対応させます。</span><span class="sxs-lookup"><span data-stu-id="4a552-112">Headings should be done using atx-style, that is, use 1-6 hash characters (#) at the start of the line to indicate a heading, corresponding to HTML headings levels H1 through H6.</span></span> <span data-ttu-id="4a552-113">上の例では第 1 - 第 4 レベルのヘッダーが使用されています。</span><span class="sxs-lookup"><span data-stu-id="4a552-113">Examples of first- through fourth-level headers are used above.</span></span>

<span data-ttu-id="4a552-114">トピックの第 1 レベルの見出し (H1) は 1 つだけにする**必要があります**。これはページ上のタイトルとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="4a552-114">There **must** be only one first-level heading (H1) in your topic, which will be displayed as the on-page title.</span></span>

<span data-ttu-id="4a552-115">見出しが `#` 文字で終わる場合、タイトルが正しくレンダリングされるように終わりに `#` 文字を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4a552-115">If your heading finishes with a `#` character, you need to add an extra `#` character in the end in order for the title to render correctly.</span></span> <span data-ttu-id="4a552-116">たとえば、`# Async Programming in F# #` のようにします。</span><span class="sxs-lookup"><span data-stu-id="4a552-116">For example, `# Async Programming in F# #`.</span></span>

<span data-ttu-id="4a552-117">第 2 レベルの見出しによってページ上の TOC が生成されます。これはページ上のタイトルの下にある "この記事の内容" セクションに表示されます。</span><span class="sxs-lookup"><span data-stu-id="4a552-117">Second-level headings will generate the on-page TOC that appears in the "In this article" section underneath the on-page title.</span></span>

### <a name="bold-and-italic-text"></a><span data-ttu-id="4a552-118">太字や斜体のテキスト</span><span class="sxs-lookup"><span data-stu-id="4a552-118">Bold and italic text</span></span>

<span data-ttu-id="4a552-119">テキストの書式を**太字**に設定するには、テキストを二重のアスタリスクで囲みます。</span><span class="sxs-lookup"><span data-stu-id="4a552-119">To format text as **bold**, you enclose it in two asterisks:</span></span>

```markdown
This text is **bold**.
```

<span data-ttu-id="4a552-120">テキストの書式を*斜体*に設定するには、テキストを一重のアスタリスクで囲みます。</span><span class="sxs-lookup"><span data-stu-id="4a552-120">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```markdown
This text is *italic*.
```

<span data-ttu-id="4a552-121">テキストの書式を***太字と斜体***の両方に設定するには、テキストを三重のアスタリスクで囲みます。</span><span class="sxs-lookup"><span data-stu-id="4a552-121">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```markdown
This is text is both ***bold and italic***.
```

### <a name="blockquotes"></a><span data-ttu-id="4a552-122">ブロック引用</span><span class="sxs-lookup"><span data-stu-id="4a552-122">Blockquotes</span></span>

<span data-ttu-id="4a552-123">ブロック引用は `>` 文字で作成されます。</span><span class="sxs-lookup"><span data-stu-id="4a552-123">Blockquotes are created using the `>` character:</span></span>

```markdown
> The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended. Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight. In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.
```

<span data-ttu-id="4a552-124">先の例は次のようにレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="4a552-124">The preceding example renders as follows:</span></span>

> <span data-ttu-id="4a552-125">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span><span class="sxs-lookup"><span data-stu-id="4a552-125">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span></span> <span data-ttu-id="4a552-126">Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight.</span><span class="sxs-lookup"><span data-stu-id="4a552-126">Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight.</span></span> <span data-ttu-id="4a552-127">In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.</span><span class="sxs-lookup"><span data-stu-id="4a552-127">In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.</span></span>

### <a name="lists"></a><span data-ttu-id="4a552-128">リスト</span><span class="sxs-lookup"><span data-stu-id="4a552-128">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="4a552-129">記号付きリスト</span><span class="sxs-lookup"><span data-stu-id="4a552-129">Unordered list</span></span>

<span data-ttu-id="4a552-130">記号付きリスト/箇条書きリストの書式を設定するには、アスタリスクまたはダッシュを使用できます。</span><span class="sxs-lookup"><span data-stu-id="4a552-130">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="4a552-131">たとえば、次の Markdown 書式は</span><span class="sxs-lookup"><span data-stu-id="4a552-131">For example, the following Markdown:</span></span>

```markdown
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="4a552-132">次のようにレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="4a552-132">will be rendered as:</span></span>

- <span data-ttu-id="4a552-133">List item 1</span><span class="sxs-lookup"><span data-stu-id="4a552-133">List item 1</span></span>
- <span data-ttu-id="4a552-134">List item 2</span><span class="sxs-lookup"><span data-stu-id="4a552-134">List item 2</span></span>
- <span data-ttu-id="4a552-135">List item 3</span><span class="sxs-lookup"><span data-stu-id="4a552-135">List item 3</span></span>

<span data-ttu-id="4a552-136">リストを別のリスト内にネストするには、子リスト アイテムをインデントします。</span><span class="sxs-lookup"><span data-stu-id="4a552-136">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="4a552-137">たとえば、次の Markdown 書式は</span><span class="sxs-lookup"><span data-stu-id="4a552-137">For example, the following Markdown:</span></span>

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="4a552-138">次のようにレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="4a552-138">will be rendered as:</span></span>

- <span data-ttu-id="4a552-139">List item 1</span><span class="sxs-lookup"><span data-stu-id="4a552-139">List item 1</span></span>
  - <span data-ttu-id="4a552-140">List item A</span><span class="sxs-lookup"><span data-stu-id="4a552-140">List item A</span></span>
  - <span data-ttu-id="4a552-141">List item B</span><span class="sxs-lookup"><span data-stu-id="4a552-141">List item B</span></span>
- <span data-ttu-id="4a552-142">List item 2</span><span class="sxs-lookup"><span data-stu-id="4a552-142">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="4a552-143">番号付きリスト</span><span class="sxs-lookup"><span data-stu-id="4a552-143">Ordered list</span></span>

<span data-ttu-id="4a552-144">番号付きリスト/段階的リストの書式を設定するには、対応する番号を使用します。</span><span class="sxs-lookup"><span data-stu-id="4a552-144">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="4a552-145">たとえば、次の Markdown 書式は</span><span class="sxs-lookup"><span data-stu-id="4a552-145">For example, the following Markdown:</span></span>

```markdown
1. First instruction
1. Second instruction
1. Third instruction
```

<span data-ttu-id="4a552-146">次のようにレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="4a552-146">will be rendered as:</span></span>

1. <span data-ttu-id="4a552-147">第 1 手順</span><span class="sxs-lookup"><span data-stu-id="4a552-147">First instruction</span></span>
2. <span data-ttu-id="4a552-148">第 2 手順</span><span class="sxs-lookup"><span data-stu-id="4a552-148">Second instruction</span></span>
3. <span data-ttu-id="4a552-149">第 3 手順</span><span class="sxs-lookup"><span data-stu-id="4a552-149">Third instruction</span></span>

<span data-ttu-id="4a552-150">リストを別のリスト内にネストするには、子リスト アイテムをインデントします。</span><span class="sxs-lookup"><span data-stu-id="4a552-150">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="4a552-151">たとえば、次の Markdown 書式は</span><span class="sxs-lookup"><span data-stu-id="4a552-151">For example, the following Markdown:</span></span>

```markdown
1. First instruction
   1. Sub-instruction
   1. Sub-instruction
1. Second instruction
```

<span data-ttu-id="4a552-152">次のようにレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="4a552-152">will be rendered as:</span></span>

1. <span data-ttu-id="4a552-153">第 1 手順</span><span class="sxs-lookup"><span data-stu-id="4a552-153">First instruction</span></span>
   1. <span data-ttu-id="4a552-154">下位手順</span><span class="sxs-lookup"><span data-stu-id="4a552-154">Sub-instruction</span></span>
   2. <span data-ttu-id="4a552-155">下位手順</span><span class="sxs-lookup"><span data-stu-id="4a552-155">Sub-instruction</span></span>
2. <span data-ttu-id="4a552-156">第 2 手順</span><span class="sxs-lookup"><span data-stu-id="4a552-156">Second instruction</span></span>

<span data-ttu-id="4a552-157">すべてのエントリに対して '1.' を</span><span class="sxs-lookup"><span data-stu-id="4a552-157">Note that we use '1.'</span></span> <span data-ttu-id="4a552-158">使用していることに注目してください。</span><span class="sxs-lookup"><span data-stu-id="4a552-158">for all entries.</span></span> <span data-ttu-id="4a552-159">後の更新で新しい手順が追加されるときや既存の手順が削除されるとき、見直しが簡単になります。</span><span class="sxs-lookup"><span data-stu-id="4a552-159">It makes diffs easier to review when later updates include new steps or remove existing steps.</span></span>

### <a name="tables"></a><span data-ttu-id="4a552-160">表</span><span class="sxs-lookup"><span data-stu-id="4a552-160">Tables</span></span>

<span data-ttu-id="4a552-161">Markdown の基本仕様には表が含まれていませんが、GFM が表をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="4a552-161">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="4a552-162">パイプ (|) 記号とハイフン記号 (-) を使用して表を作成できます。</span><span class="sxs-lookup"><span data-stu-id="4a552-162">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="4a552-163">ハイフンは各列のヘッダーを作成し、パイプは各列を区切ります。</span><span class="sxs-lookup"><span data-stu-id="4a552-163">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="4a552-164">表が正しくレンダリングされるように、表の前に空の行を 1 つ挿入してください。</span><span class="sxs-lookup"><span data-stu-id="4a552-164">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="4a552-165">たとえば、次の Markdown 書式は</span><span class="sxs-lookup"><span data-stu-id="4a552-165">For example, the following Markdown:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="4a552-166">次のようにレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="4a552-166">will be rendered as:</span></span>

| <span data-ttu-id="4a552-167">Fun</span><span class="sxs-lookup"><span data-stu-id="4a552-167">Fun</span></span>                  | <span data-ttu-id="4a552-168">With</span><span class="sxs-lookup"><span data-stu-id="4a552-168">With</span></span>                 | <span data-ttu-id="4a552-169">表</span><span class="sxs-lookup"><span data-stu-id="4a552-169">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="4a552-170">left-aligned column</span><span class="sxs-lookup"><span data-stu-id="4a552-170">left-aligned column</span></span>  | <span data-ttu-id="4a552-171">right-aligned column</span><span class="sxs-lookup"><span data-stu-id="4a552-171">right-aligned column</span></span> | <span data-ttu-id="4a552-172">centered column</span><span class="sxs-lookup"><span data-stu-id="4a552-172">centered column</span></span> |
| <span data-ttu-id="4a552-173">$100</span><span class="sxs-lookup"><span data-stu-id="4a552-173">$100</span></span>                 | <span data-ttu-id="4a552-174">$100</span><span class="sxs-lookup"><span data-stu-id="4a552-174">$100</span></span>                 | <span data-ttu-id="4a552-175">$100</span><span class="sxs-lookup"><span data-stu-id="4a552-175">$100</span></span>            |
| <span data-ttu-id="4a552-176">$10</span><span class="sxs-lookup"><span data-stu-id="4a552-176">$10</span></span>                  | <span data-ttu-id="4a552-177">$10</span><span class="sxs-lookup"><span data-stu-id="4a552-177">$10</span></span>                  | <span data-ttu-id="4a552-178">$10</span><span class="sxs-lookup"><span data-stu-id="4a552-178">$10</span></span>             |
| <span data-ttu-id="4a552-179">$1</span><span class="sxs-lookup"><span data-stu-id="4a552-179">$1</span></span>                   | <span data-ttu-id="4a552-180">$1</span><span class="sxs-lookup"><span data-stu-id="4a552-180">$1</span></span>                   | <span data-ttu-id="4a552-181">$1</span><span class="sxs-lookup"><span data-stu-id="4a552-181">$1</span></span>              |

<span data-ttu-id="4a552-182">表作成の詳細については、以下の情報源をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="4a552-182">For more information on creating tables, see:</span></span>

- <span data-ttu-id="4a552-183">横に長い表の書式設定に役立つ、Markdig の「[表を折り返す機能](#table-wrapping)」。</span><span class="sxs-lookup"><span data-stu-id="4a552-183">The Markdig [table wrapping feature](#table-wrapping), which can help with formatting of wide tables.</span></span>
- <span data-ttu-id="4a552-184">GitHub の「[Organizing information with tables (表を使用した情報の整理)](https://help.github.com/articles/organizing-information-with-tables/)」。</span><span class="sxs-lookup"><span data-stu-id="4a552-184">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/).</span></span>
- <span data-ttu-id="4a552-185">[Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) Web アプリ。</span><span class="sxs-lookup"><span data-stu-id="4a552-185">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app.</span></span>
- <span data-ttu-id="4a552-186">Adam Pritchard 氏の「[Markdown Cheatsheet (Markdown に関する簡易参照ガイド)](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables)」。</span><span class="sxs-lookup"><span data-stu-id="4a552-186">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span></span>
- <span data-ttu-id="4a552-187">Michel Fortin 氏の [Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table) に関するページ。</span><span class="sxs-lookup"><span data-stu-id="4a552-187">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table).</span></span>
- <span data-ttu-id="4a552-188">[HTML テーブルからマークダウンへの変換](https://jmalarcon.github.io/markdowntables/)。</span><span class="sxs-lookup"><span data-stu-id="4a552-188">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/).</span></span>

### <a name="links"></a><span data-ttu-id="4a552-189">リンク</span><span class="sxs-lookup"><span data-stu-id="4a552-189">Links</span></span>

<span data-ttu-id="4a552-190">インライン リンクの Markdown 構文では、ハイパーリンクされるテキスト部分 `[link text]` の後に、リンク先 URL またはファイル名の部分 `(file-name.md)` が続きます。</span><span class="sxs-lookup"><span data-stu-id="4a552-190">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="4a552-191">リンクの詳細については、以下の情報源をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="4a552-191">For more information on linking, see:</span></span>

- <span data-ttu-id="4a552-192">Markdown のリンクの基本的なサポートについては、[Markdown の構文](https://daringfireball.net/projects/markdown/syntax#link)に関するセクション。</span><span class="sxs-lookup"><span data-stu-id="4a552-192">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="4a552-193">Markdig で提供されるその他のリンク構文の詳細については、このガイドの[リンク](how-to-write-links.md)に関するセクション。</span><span class="sxs-lookup"><span data-stu-id="4a552-193">The [Links](how-to-write-links.md) section of this guide for details on the additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="4a552-194">コード スニペット</span><span class="sxs-lookup"><span data-stu-id="4a552-194">Code snippets</span></span>

<span data-ttu-id="4a552-195">Markdown では、コード スニペットの配置方法として、文中へのインライン配置と、文と文の間への "フェンスされた" 個別ブロックとしての配置の両方がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="4a552-195">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="4a552-196">詳細については、以下の情報源をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="4a552-196">For details, see:</span></span>

- <span data-ttu-id="4a552-197">[Markdown のコード ブロックのネイティブ サポート](https://daringfireball.net/projects/markdown/syntax#precode)に関するセクション</span><span class="sxs-lookup"><span data-stu-id="4a552-197">[Markdown's native support for code blocks](https://daringfireball.net/projects/markdown/syntax#precode)</span></span>
- <span data-ttu-id="4a552-198">[GFM のコード フェンスと構文強調表示のサポート](https://help.github.com/articles/creating-and-highlighting-code-blocks/)に関するページ</span><span class="sxs-lookup"><span data-stu-id="4a552-198">[GFM support for code fencing and syntax highlighting](https://help.github.com/articles/creating-and-highlighting-code-blocks/)</span></span>

<span data-ttu-id="4a552-199">コード ブロックをフェンスすることで、コード スニペットの構文を強調表示することができます。</span><span class="sxs-lookup"><span data-stu-id="4a552-199">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="4a552-200">フェンスされたコード ブロックの一般的な書式は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="4a552-200">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="4a552-201">冒頭の 3 つのバッククォート (\`) 記号に続くエイリアスは、使用される構文強調表示を定義します。</span><span class="sxs-lookup"><span data-stu-id="4a552-201">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="4a552-202">以下は Docs コンテンツで一般的に使用されるプログラミング言語と、対応するラベルのリストです。</span><span class="sxs-lookup"><span data-stu-id="4a552-202">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="4a552-203">これらの言語は、フレンドリ名をサポートし、ほとんどに言語の強調表示機能があります。</span><span class="sxs-lookup"><span data-stu-id="4a552-203">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="4a552-204">名前</span><span class="sxs-lookup"><span data-stu-id="4a552-204">Name</span></span>|<span data-ttu-id="4a552-205">Markdown ラベル</span><span class="sxs-lookup"><span data-stu-id="4a552-205">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="4a552-206">.NET コンソール</span><span class="sxs-lookup"><span data-stu-id="4a552-206">.NET Console</span></span>|<span data-ttu-id="4a552-207">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="4a552-207">dotnetcli</span></span>|
|<span data-ttu-id="4a552-208">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="4a552-208">ASP.NET (C#)</span></span>|<span data-ttu-id="4a552-209">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="4a552-209">aspx-csharp</span></span>|
|<span data-ttu-id="4a552-210">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="4a552-210">ASP.NET (VB)</span></span>|<span data-ttu-id="4a552-211">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="4a552-211">aspx-vb</span></span>|
|<span data-ttu-id="4a552-212">AzCopy</span><span class="sxs-lookup"><span data-stu-id="4a552-212">AzCopy</span></span>|<span data-ttu-id="4a552-213">azcopy</span><span class="sxs-lookup"><span data-stu-id="4a552-213">azcopy</span></span>|
|<span data-ttu-id="4a552-214">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="4a552-214">Azure CLI</span></span>|<span data-ttu-id="4a552-215">azurecli</span><span class="sxs-lookup"><span data-stu-id="4a552-215">azurecli</span></span>|
|<span data-ttu-id="4a552-216">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="4a552-216">Azure PowerShell</span></span>|<span data-ttu-id="4a552-217">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="4a552-217">azurepowershell</span></span>|
|<span data-ttu-id="4a552-218">C++</span><span class="sxs-lookup"><span data-stu-id="4a552-218">C++</span></span>|<span data-ttu-id="4a552-219">cpp</span><span class="sxs-lookup"><span data-stu-id="4a552-219">cpp</span></span>|
|<span data-ttu-id="4a552-220">C++/CX</span><span class="sxs-lookup"><span data-stu-id="4a552-220">C++/CX</span></span>|<span data-ttu-id="4a552-221">cppcx</span><span class="sxs-lookup"><span data-stu-id="4a552-221">cppcx</span></span>|
|<span data-ttu-id="4a552-222">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="4a552-222">C++/WinRT</span></span>|<span data-ttu-id="4a552-223">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="4a552-223">cppwinrt</span></span>|
|<span data-ttu-id="4a552-224">C#</span><span class="sxs-lookup"><span data-stu-id="4a552-224">C#</span></span>|<span data-ttu-id="4a552-225">csharp</span><span class="sxs-lookup"><span data-stu-id="4a552-225">csharp</span></span>|
|<span data-ttu-id="4a552-226">ブラウザーの C#</span><span class="sxs-lookup"><span data-stu-id="4a552-226">C# in browser</span></span>|<span data-ttu-id="4a552-227">csharp-interactive</span><span class="sxs-lookup"><span data-stu-id="4a552-227">csharp-interactive</span></span>|
|<span data-ttu-id="4a552-228">コンソール</span><span class="sxs-lookup"><span data-stu-id="4a552-228">Console</span></span>|<span data-ttu-id="4a552-229">console</span><span class="sxs-lookup"><span data-stu-id="4a552-229">console</span></span>|
|<span data-ttu-id="4a552-230">CSHTML</span><span class="sxs-lookup"><span data-stu-id="4a552-230">CSHTML</span></span>|<span data-ttu-id="4a552-231">cshtml</span><span class="sxs-lookup"><span data-stu-id="4a552-231">cshtml</span></span>|
|<span data-ttu-id="4a552-232">DAX</span><span class="sxs-lookup"><span data-stu-id="4a552-232">DAX</span></span>|<span data-ttu-id="4a552-233">dax</span><span class="sxs-lookup"><span data-stu-id="4a552-233">dax</span></span>|
|<span data-ttu-id="4a552-234">Docker</span><span class="sxs-lookup"><span data-stu-id="4a552-234">Docker</span></span>|<span data-ttu-id="4a552-235">dockerfile</span><span class="sxs-lookup"><span data-stu-id="4a552-235">dockerfile</span></span>|
|<span data-ttu-id="4a552-236">F#</span><span class="sxs-lookup"><span data-stu-id="4a552-236">F#</span></span>|<span data-ttu-id="4a552-237">fsharp</span><span class="sxs-lookup"><span data-stu-id="4a552-237">fsharp</span></span>|
|<span data-ttu-id="4a552-238">Go</span><span class="sxs-lookup"><span data-stu-id="4a552-238">Go</span></span>|<span data-ttu-id="4a552-239">go</span><span class="sxs-lookup"><span data-stu-id="4a552-239">go</span></span>|
|<span data-ttu-id="4a552-240">HTML</span><span class="sxs-lookup"><span data-stu-id="4a552-240">HTML</span></span>|<span data-ttu-id="4a552-241">html</span><span class="sxs-lookup"><span data-stu-id="4a552-241">html</span></span>|
|<span data-ttu-id="4a552-242">HTTP</span><span class="sxs-lookup"><span data-stu-id="4a552-242">HTTP</span></span>|<span data-ttu-id="4a552-243">http</span><span class="sxs-lookup"><span data-stu-id="4a552-243">http</span></span>|
|<span data-ttu-id="4a552-244">Java</span><span class="sxs-lookup"><span data-stu-id="4a552-244">Java</span></span>|<span data-ttu-id="4a552-245">java</span><span class="sxs-lookup"><span data-stu-id="4a552-245">java</span></span>|
|<span data-ttu-id="4a552-246">JavaScript</span><span class="sxs-lookup"><span data-stu-id="4a552-246">JavaScript</span></span>|<span data-ttu-id="4a552-247">javascript</span><span class="sxs-lookup"><span data-stu-id="4a552-247">javascript</span></span>|
|<span data-ttu-id="4a552-248">JSON</span><span class="sxs-lookup"><span data-stu-id="4a552-248">JSON</span></span>|<span data-ttu-id="4a552-249">json</span><span class="sxs-lookup"><span data-stu-id="4a552-249">json</span></span>|
|<span data-ttu-id="4a552-250">Kusto Query Language</span><span class="sxs-lookup"><span data-stu-id="4a552-250">Kusto Query Language</span></span>|<span data-ttu-id="4a552-251">kusto</span><span class="sxs-lookup"><span data-stu-id="4a552-251">kusto</span></span>|
|<span data-ttu-id="4a552-252">Markdown</span><span class="sxs-lookup"><span data-stu-id="4a552-252">Markdown</span></span>|<span data-ttu-id="4a552-253">md</span><span class="sxs-lookup"><span data-stu-id="4a552-253">md</span></span>|
|<span data-ttu-id="4a552-254">Objective-C</span><span class="sxs-lookup"><span data-stu-id="4a552-254">Objective-C</span></span>|<span data-ttu-id="4a552-255">objc</span><span class="sxs-lookup"><span data-stu-id="4a552-255">objc</span></span>|
|<span data-ttu-id="4a552-256">OData</span><span class="sxs-lookup"><span data-stu-id="4a552-256">OData</span></span>|<span data-ttu-id="4a552-257">odata</span><span class="sxs-lookup"><span data-stu-id="4a552-257">odata</span></span>|
|<span data-ttu-id="4a552-258">PHP</span><span class="sxs-lookup"><span data-stu-id="4a552-258">PHP</span></span>|<span data-ttu-id="4a552-259">php</span><span class="sxs-lookup"><span data-stu-id="4a552-259">php</span></span>|
|<span data-ttu-id="4a552-260">PowerApps (ドット小数点区切り記号)</span><span class="sxs-lookup"><span data-stu-id="4a552-260">PowerApps (dot decimal separator)</span></span>|<span data-ttu-id="4a552-261">powerapps-dot</span><span class="sxs-lookup"><span data-stu-id="4a552-261">powerapps-dot</span></span>|
|<span data-ttu-id="4a552-262">PowerApps (コンマ小数点区切り記号)</span><span class="sxs-lookup"><span data-stu-id="4a552-262">PowerApps (comma decimal separator)</span></span>|<span data-ttu-id="4a552-263">powerapps-comma</span><span class="sxs-lookup"><span data-stu-id="4a552-263">powerapps-comma</span></span>|
|<span data-ttu-id="4a552-264">PowerShell</span><span class="sxs-lookup"><span data-stu-id="4a552-264">PowerShell</span></span>|<span data-ttu-id="4a552-265">powershell</span><span class="sxs-lookup"><span data-stu-id="4a552-265">powershell</span></span>|
|<span data-ttu-id="4a552-266">Python</span><span class="sxs-lookup"><span data-stu-id="4a552-266">Python</span></span>|<span data-ttu-id="4a552-267">python</span><span class="sxs-lookup"><span data-stu-id="4a552-267">python</span></span>|
|<span data-ttu-id="4a552-268">Q#</span><span class="sxs-lookup"><span data-stu-id="4a552-268">Q#</span></span>|<span data-ttu-id="4a552-269">qsharp</span><span class="sxs-lookup"><span data-stu-id="4a552-269">qsharp</span></span>|
|<span data-ttu-id="4a552-270">R</span><span class="sxs-lookup"><span data-stu-id="4a552-270">R</span></span>|<span data-ttu-id="4a552-271">r</span><span class="sxs-lookup"><span data-stu-id="4a552-271">r</span></span>|
|<span data-ttu-id="4a552-272">Ruby</span><span class="sxs-lookup"><span data-stu-id="4a552-272">Ruby</span></span>|<span data-ttu-id="4a552-273">ruby</span><span class="sxs-lookup"><span data-stu-id="4a552-273">ruby</span></span>|
|<span data-ttu-id="4a552-274">SQL</span><span class="sxs-lookup"><span data-stu-id="4a552-274">SQL</span></span>|<span data-ttu-id="4a552-275">sql</span><span class="sxs-lookup"><span data-stu-id="4a552-275">sql</span></span>|
|<span data-ttu-id="4a552-276">Swift</span><span class="sxs-lookup"><span data-stu-id="4a552-276">Swift</span></span>|<span data-ttu-id="4a552-277">swift</span><span class="sxs-lookup"><span data-stu-id="4a552-277">swift</span></span>|
|<span data-ttu-id="4a552-278">TypeScript</span><span class="sxs-lookup"><span data-stu-id="4a552-278">TypeScript</span></span>|<span data-ttu-id="4a552-279">typescript</span><span class="sxs-lookup"><span data-stu-id="4a552-279">typescript</span></span>|
|<span data-ttu-id="4a552-280">VB</span><span class="sxs-lookup"><span data-stu-id="4a552-280">VB</span></span>|<span data-ttu-id="4a552-281">vb</span><span class="sxs-lookup"><span data-stu-id="4a552-281">vb</span></span>|
|<span data-ttu-id="4a552-282">XAML</span><span class="sxs-lookup"><span data-stu-id="4a552-282">XAML</span></span>|<span data-ttu-id="4a552-283">xaml</span><span class="sxs-lookup"><span data-stu-id="4a552-283">xaml</span></span>|
|<span data-ttu-id="4a552-284">XML</span><span class="sxs-lookup"><span data-stu-id="4a552-284">XML</span></span>|<span data-ttu-id="4a552-285">xml</span><span class="sxs-lookup"><span data-stu-id="4a552-285">xml</span></span>|

<span data-ttu-id="4a552-286">`csharp-interactive` 名によって C# 言語と、ブラウザーからサンプルを実行する機能が指定されます。</span><span class="sxs-lookup"><span data-stu-id="4a552-286">The `csharp-interactive` name specifies the C# language, and the ability to run the samples from the browser.</span></span> <span data-ttu-id="4a552-287">このようなスニペットは Docker コンテナーでコンパイルされ、実行されます。そのプログラム実行の結果はユーザーのブラウザー ウィンドウに表示されます。</span><span class="sxs-lookup"><span data-stu-id="4a552-287">These snippets are compiled and executed in a Docker container, and the results of that program execution are displayed in the user's browser window.</span></span>

#### <a name="example-c"></a><span data-ttu-id="4a552-288">例:C\#</span><span class="sxs-lookup"><span data-stu-id="4a552-288">Example: C\#</span></span>

<span data-ttu-id="4a552-289">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="4a552-289">__Markdown__</span></span>

    ```csharp
    // Hello1.cs
    public class Hello1
    {
        public static void Main()
        {
            System.Console.WriteLine("Hello, World!");
        }
    }
    ```

<span data-ttu-id="4a552-290">__レンダー__</span><span class="sxs-lookup"><span data-stu-id="4a552-290">__Render__</span></span>

```csharp
// Hello1.cs
public class Hello1
{
    public static void Main()
    {
        System.Console.WriteLine("Hello, World!");
    }
}
```

#### <a name="example-sql"></a><span data-ttu-id="4a552-291">例:SQL</span><span class="sxs-lookup"><span data-stu-id="4a552-291">Example: SQL</span></span>

<span data-ttu-id="4a552-292">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="4a552-292">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="4a552-293">__レンダー__</span><span class="sxs-lookup"><span data-stu-id="4a552-293">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a><span data-ttu-id="4a552-294">OPS による Markdown のカスタム拡張機能</span><span class="sxs-lookup"><span data-stu-id="4a552-294">OPS custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="4a552-295">Open Publishing Services (OPS) は GitHub Flavored Markdown (GFM) との互換性が非常に高い Markdown パーサー Markdig を実装しています。</span><span class="sxs-lookup"><span data-stu-id="4a552-295">Open Publishing Services (OPS) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="4a552-296">Markdig は Markdown 拡張機能を介していくつかの機能を追加しています。</span><span class="sxs-lookup"><span data-stu-id="4a552-296">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="4a552-297">そのため、完全版の「OPS Authoring Guide」 (OPS オーサリング ガイド) の一部の記事は、参考のためにこのガイドに含まれています </span><span class="sxs-lookup"><span data-stu-id="4a552-297">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="4a552-298">(たとえば、目次の「Markdig and Markdown extensions」(Markdig と Markdown の拡張機能) と「Code snippets」(コード スニペット) をご覧ください)。</span><span class="sxs-lookup"><span data-stu-id="4a552-298">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="4a552-299">Docs 記事では、段落、リンク、リスト、見出しなど、ほとんどの書式設定に GFM が使用されます。</span><span class="sxs-lookup"><span data-stu-id="4a552-299">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="4a552-300">記事の高度な書式設定には、次のような Markdig 機能を使用できます。</span><span class="sxs-lookup"><span data-stu-id="4a552-300">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="4a552-301">注ブロック</span><span class="sxs-lookup"><span data-stu-id="4a552-301">Note blocks</span></span>
- <span data-ttu-id="4a552-302">インクルード ファイル</span><span class="sxs-lookup"><span data-stu-id="4a552-302">Include files</span></span>
- <span data-ttu-id="4a552-303">セレクター</span><span class="sxs-lookup"><span data-stu-id="4a552-303">Selectors</span></span>
- <span data-ttu-id="4a552-304">埋め込みビデオ</span><span class="sxs-lookup"><span data-stu-id="4a552-304">Embedded videos</span></span>
- <span data-ttu-id="4a552-305">コード スニペット/サンプル</span><span class="sxs-lookup"><span data-stu-id="4a552-305">Code snippets/samples</span></span>

<span data-ttu-id="4a552-306">完全なリストについては、目次の「Markdig and Markdown extensions」(Markdig と Markdown の拡張機能) と「Code snippets」(コード スニペット) をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="4a552-306">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="4a552-307">注ブロック</span><span class="sxs-lookup"><span data-stu-id="4a552-307">Note blocks</span></span>

<span data-ttu-id="4a552-308">特定の内容に注目を集めるには、4 つのタイプの注ブロックから選択できます。</span><span class="sxs-lookup"><span data-stu-id="4a552-308">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="4a552-309">NOTE (注意)</span><span class="sxs-lookup"><span data-stu-id="4a552-309">NOTE</span></span>
- <span data-ttu-id="4a552-310">WARNING (警告)</span><span class="sxs-lookup"><span data-stu-id="4a552-310">WARNING</span></span>
- <span data-ttu-id="4a552-311">TIP (ヒント)</span><span class="sxs-lookup"><span data-stu-id="4a552-311">TIP</span></span>
- <span data-ttu-id="4a552-312">IMPORTANT (重要)</span><span class="sxs-lookup"><span data-stu-id="4a552-312">IMPORTANT</span></span>

<span data-ttu-id="4a552-313">注ブロックによって文章がわかりにくくなることがあるので、概して注ブロックは控えめに使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4a552-313">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="4a552-314">注ブロックでもコード ブロック、イメージ、リスト、およびリンクがサポートされますが、注ブロックを簡潔でわかりやすくするように心掛けてください。</span><span class="sxs-lookup"><span data-stu-id="4a552-314">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

<span data-ttu-id="4a552-315">例:</span><span class="sxs-lookup"><span data-stu-id="4a552-315">Examples:</span></span>

```markdown
> [!NOTE]
> This is a NOTE

> [!WARNING]
> This is a WARNING

> [!TIP]
> This is a TIP

> [!IMPORTANT]
> This is IMPORTANT
```

<span data-ttu-id="4a552-316">これは次のようにレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="4a552-316">These render as follows:</span></span>

> [!NOTE]
> <span data-ttu-id="4a552-317">This is a NOTE</span><span class="sxs-lookup"><span data-stu-id="4a552-317">This is a NOTE</span></span>

> [!WARNING]
> <span data-ttu-id="4a552-318">This is a WARNING</span><span class="sxs-lookup"><span data-stu-id="4a552-318">This is a WARNING</span></span>

> [!TIP]
> <span data-ttu-id="4a552-319">This is a TIP</span><span class="sxs-lookup"><span data-stu-id="4a552-319">This is a TIP</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4a552-320">This is IMPORTANT</span><span class="sxs-lookup"><span data-stu-id="4a552-320">This is IMPORTANT</span></span>

### <a name="include-files"></a><span data-ttu-id="4a552-321">インクルード ファイル</span><span class="sxs-lookup"><span data-stu-id="4a552-321">Include files</span></span>

<span data-ttu-id="4a552-322">再利用可能なテキスト ファイルまたはイメージ ファイルを記事ファイルにインクルードする必要がある場合は、Markdig のファイル インクルード機能を使用して "インクルード" ファイルを参照できます。</span><span class="sxs-lookup"><span data-stu-id="4a552-322">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="4a552-323">この機能は、ビルド時に特定のファイルを記事ファイルにインクルードするように OPS に指示します。これにより、その指定されたファイルは公開記事に含まれるようになります。</span><span class="sxs-lookup"><span data-stu-id="4a552-323">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="4a552-324">コンテンツの再利用に役立つインクルード参照には、次の 3 種類があります。</span><span class="sxs-lookup"><span data-stu-id="4a552-324">Three types of include references are available to help you reuse content:</span></span>

- <span data-ttu-id="4a552-325">インライン: 一般的なテキスト スニペットを別の文中にインラインで再利用できます。</span><span class="sxs-lookup"><span data-stu-id="4a552-325">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="4a552-326">ブロック: Markdown ファイル全体をブロックとして再利用し、記事のセクション内にネストできます。</span><span class="sxs-lookup"><span data-stu-id="4a552-326">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="4a552-327">イメージ: これは Docs に実装されている標準的なイメージ インクルードの方法です。</span><span class="sxs-lookup"><span data-stu-id="4a552-327">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="4a552-328">インラインまたはブロックによるインクルード ファイルはシンプルな Markdown (.md) ファイルにすぎません。</span><span class="sxs-lookup"><span data-stu-id="4a552-328">An inline or block include file is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="4a552-329">これにはあらゆる有効な Markdown を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="4a552-329">It can contain any valid Markdown.</span></span> <span data-ttu-id="4a552-330">すべてのインクルード Markdown ファイルは、リポジトリのルートにある[共通の `/includes` サブディレクトリ](git-github-fundamentals.md#includes-subdirectory)に配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4a552-330">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="4a552-331">記事が公開されると、インクルードされたファイルはその記事にシームレスに統合されます。</span><span class="sxs-lookup"><span data-stu-id="4a552-331">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="4a552-332">インクルード ファイルに関する要件と考慮事項を次に示します。</span><span class="sxs-lookup"><span data-stu-id="4a552-332">Here are requirements and considerations for include files:</span></span>

- <span data-ttu-id="4a552-333">複数の記事に同じテキストを表示する必要があるときは必ず、インクルード ファイルを使用してください。</span><span class="sxs-lookup"><span data-stu-id="4a552-333">Use an include file whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="4a552-334">ブロックによるインクルード参照は、1 つまたは 2 つの段落、共通の手順、共通のセクションといった分量の多いコンテンツに使用してください。</span><span class="sxs-lookup"><span data-stu-id="4a552-334">Use a block include reference for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="4a552-335">1 つの文よりも小さい場合には、使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="4a552-335">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="4a552-336">インクルード参照は Markdig 拡張機能に依存するため、GitHub でレンダリングされた記事内でインクルード参照はレンダリングされません。</span><span class="sxs-lookup"><span data-stu-id="4a552-336">Include references won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="4a552-337">公開後にのみレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="4a552-337">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="4a552-338">インクルード ファイル内のすべてのテキストが、インクルード ファイルを参照する記事内の先行テキストまたは後続テキストに依存しない完全な文または語句で記述されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4a552-338">Ensure that all the text in an include file is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include file.</span></span> <span data-ttu-id="4a552-339">このガイダンスを無視すると、ローカライズされたエクスペリエンスを乱す翻訳不可能な文字列が記事内に発生します。</span><span class="sxs-lookup"><span data-stu-id="4a552-339">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="4a552-340">インクルード参照をほかのインクルード ファイル内に埋め込まないでください。</span><span class="sxs-lookup"><span data-stu-id="4a552-340">Don't embed include references within other include files.</span></span> <span data-ttu-id="4a552-341">それはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="4a552-341">They are not supported.</span></span>
- <span data-ttu-id="4a552-342">メディア ファイルは、インクルードのサブディレクトリ内にあるメディア フォルダーに配置する必要があります。たとえば、`<repo>`/includes/media フォルダーです。</span><span class="sxs-lookup"><span data-stu-id="4a552-342">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="4a552-343">メディア ディレクトリのルートにはイメージを配置しないでください。</span><span class="sxs-lookup"><span data-stu-id="4a552-343">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="4a552-344">インクルード ファイルにイメージが含まれていない場合、対応するメディア ディレクトリは不要です。</span><span class="sxs-lookup"><span data-stu-id="4a552-344">If the include file does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="4a552-345">通常の記事と同様に、インクルード ファイル間でメディアを共有しないでください。</span><span class="sxs-lookup"><span data-stu-id="4a552-345">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="4a552-346">インクルード ファイルおよび記事ごとに、一意の名前を持つ個別ファイルを使用してください。</span><span class="sxs-lookup"><span data-stu-id="4a552-346">Use a separate file with a unique name for each include file and article.</span></span> <span data-ttu-id="4a552-347">メディア ファイルは、インクルード ファイルに関連付けられたメディア フォルダーに格納してください。</span><span class="sxs-lookup"><span data-stu-id="4a552-347">Store the media file in the media folder that's associated with the include file.</span></span>
- <span data-ttu-id="4a552-348">記事の唯一のコンテンツとしてインクルード ファイルを使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="4a552-348">Don't use an include file as the only content of an article.</span></span>  <span data-ttu-id="4a552-349">インクルード ファイルの目的は、記事の残りの部分にあるコンテンツを補完することです。</span><span class="sxs-lookup"><span data-stu-id="4a552-349">Include files are meant to be supplemental to the content in the rest of the article.</span></span>

<span data-ttu-id="4a552-350">例:</span><span class="sxs-lookup"><span data-stu-id="4a552-350">Example:</span></span>

```markdown
[!INCLUDE[sample include file](../includes/sampleinclude.md)]
```

### <a name="selectors"></a><span data-ttu-id="4a552-351">セレクター</span><span class="sxs-lookup"><span data-stu-id="4a552-351">Selectors</span></span>

<span data-ttu-id="4a552-352">同じ技術記事の複数のバージョンを記述するときには、複数のテクノロジまたはプラットフォームの実装の違いに対応するために、セレクターを使用します。</span><span class="sxs-lookup"><span data-stu-id="4a552-352">Use selectors in technical articles when you author multiple flavors of the same article, to  address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="4a552-353">通常、これが最も当てはまるのは、Microsoft の開発者向けのモバイル プラットフォームのコンテンツです。</span><span class="sxs-lookup"><span data-stu-id="4a552-353">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="4a552-354">現在 Markdig にはシングル セレクターとマルチ セレクターという 2 つのタイプのセレクターがあります。</span><span class="sxs-lookup"><span data-stu-id="4a552-354">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="4a552-355">選択範囲内の各記事に配置されるセレクター Markdown は同じであるため、ご自分の記事に対するセレクターをインクルード ファイルに配置することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="4a552-355">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include file.</span></span> <span data-ttu-id="4a552-356">その上で、同じセレクターを使用するご自分のすべての記事内で、そのインクルード ファイルを参照できます。</span><span class="sxs-lookup"><span data-stu-id="4a552-356">Then you can reference that include file in all your articles that use the same selector.</span></span>

<span data-ttu-id="4a552-357">次にセレクターの例を示します。</span><span class="sxs-lookup"><span data-stu-id="4a552-357">The following shows an example selector:</span></span>

```markdown
> [!div class="op_single_selector"]
- [macOS](../docs/core/tutorials/using-on-macos.md)
- [Windows](../docs/core/tutorials/with-visual-studio.md)
```

<span data-ttu-id="4a552-358">[Azure ドキュメント](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic)で、実際に使われているセレクターの例を確認できます。</span><span class="sxs-lookup"><span data-stu-id="4a552-358">You can see an example of selectors in action at the [Azure docs](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span></span>

### <a name="code-include-references"></a><span data-ttu-id="4a552-359">コードのインクルード参照</span><span class="sxs-lookup"><span data-stu-id="4a552-359">Code include references</span></span>

<span data-ttu-id="4a552-360">Markdig では、コード スニペット拡張機能を使用した記事へのコードの高度なインクルードがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="4a552-360">Markdig supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="4a552-361">プログラミング言語の選択や構文の色分けといった GFM 機能に基づく高度なレンダリングに加えて、次のような便利な機能を使用できます。</span><span class="sxs-lookup"><span data-stu-id="4a552-361">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="4a552-362">外部リポジトリから集められたコード サンプル/スニペットのインクルード。</span><span class="sxs-lookup"><span data-stu-id="4a552-362">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="4a552-363">さまざまな言語でのさまざまなバージョンのコード サンプルをタブに表示する UI。</span><span class="sxs-lookup"><span data-stu-id="4a552-363">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="4a552-364">問題の発見 + トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="4a552-364">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="4a552-365">alt テキスト</span><span class="sxs-lookup"><span data-stu-id="4a552-365">Alt text</span></span>

<span data-ttu-id="4a552-366">アンダー スコアを含む alt テキストは正しくレンダリングされません。</span><span class="sxs-lookup"><span data-stu-id="4a552-366">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="4a552-367">たとえば、次のテキストを使用するのではなく、</span><span class="sxs-lookup"><span data-stu-id="4a552-367">For example, instead of using this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="4a552-368">次のようにアンダー スコアをエスケープします。</span><span class="sxs-lookup"><span data-stu-id="4a552-368">Escape the underscores like this:</span></span>

```markdown
![ADextension\_2FA\_Configure\_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="4a552-369">アポストロフィと引用符</span><span class="sxs-lookup"><span data-stu-id="4a552-369">Apostrophes and quotation marks</span></span>

<span data-ttu-id="4a552-370">Word から Markdown エディターにコピーしたテキストに、"スマート" (カールした) アポストロフィまたは引用符が含まれていることがあります。</span><span class="sxs-lookup"><span data-stu-id="4a552-370">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="4a552-371">これらを標準的なアポストロフィや引用符にエンコードまたは変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4a552-371">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="4a552-372">そうしないと、ファイルが公開されたときに次のように表示されます: Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="4a552-372">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="4a552-373">これらの "スマート" バージョンの記述記号のエンコーディングは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="4a552-373">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="4a552-374">左 (始め) 二重引用符: `&#8220;`</span><span class="sxs-lookup"><span data-stu-id="4a552-374">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="4a552-375">右 (終わり) 二重引用符: `&#8221;`</span><span class="sxs-lookup"><span data-stu-id="4a552-375">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="4a552-376">右 (終わり) 一重引用符またはアポストロフィ: `&#8217;`</span><span class="sxs-lookup"><span data-stu-id="4a552-376">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="4a552-377">左 (始め) 一重引用符 (あまり使用されません): `&#8216;`</span><span class="sxs-lookup"><span data-stu-id="4a552-377">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="4a552-378">山かっこ</span><span class="sxs-lookup"><span data-stu-id="4a552-378">Angle brackets</span></span>

<span data-ttu-id="4a552-379">プレースホルダーを示す目的では一般的に山括弧が使用されます。</span><span class="sxs-lookup"><span data-stu-id="4a552-379">It is common to use angle brackets to denote a placeholder.</span></span> <span data-ttu-id="4a552-380">これを (コードではなく) テキストで行うときは、山括弧で囲む必要があります。</span><span class="sxs-lookup"><span data-stu-id="4a552-380">When you do this in text (not code), you must encode the angle brackets.</span></span> <span data-ttu-id="4a552-381">そうしないと、それらのテキストは Markdown によって HTML タグとして認識されます。</span><span class="sxs-lookup"><span data-stu-id="4a552-381">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="4a552-382">たとえば、`<script name>` を `&lt;script name&gt;` にエンコードしてください。</span><span class="sxs-lookup"><span data-stu-id="4a552-382">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="see-also"></a><span data-ttu-id="4a552-383">関連項目:</span><span class="sxs-lookup"><span data-stu-id="4a552-383">See also:</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="4a552-384">Markdown に関するリソース</span><span class="sxs-lookup"><span data-stu-id="4a552-384">Markdown resources</span></span>

- [<span data-ttu-id="4a552-385">Markdown 入門</span><span class="sxs-lookup"><span data-stu-id="4a552-385">Introduction to Markdown</span></span>](https://daringfireball.net/projects/markdown/syntax)
- [<span data-ttu-id="4a552-386">Docs の Markdown に関する簡易参照ガイド</span><span class="sxs-lookup"><span data-stu-id="4a552-386">Docs Markdown cheat sheet</span></span>](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [<span data-ttu-id="4a552-387">GitHub の Markdown の基本</span><span class="sxs-lookup"><span data-stu-id="4a552-387">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
- [<span data-ttu-id="4a552-388">Markdown ガイド</span><span class="sxs-lookup"><span data-stu-id="4a552-388">The Markdown Guide</span></span>](https://www.markdownguide.org/)
