---
title: ドキュメントを記述するための Markdown の使用方法
description: この記事では、docs.microsoft.com の記事を記述するために使用される Markdown の基礎と参照情報について説明します。
ms.date: 07/13/2017
ms.openlocfilehash: 8613d525afc11caf9ec760c4f15ea44010781634
ms.sourcegitcommit: 21c9ac71e1abff946466cddf17a1ee97bc349ec5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/11/2018
ms.locfileid: "53245897"
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="2b4c0-103">ドキュメントを記述するための Markdown の使用方法</span><span class="sxs-lookup"><span data-stu-id="2b4c0-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="2b4c0-104">[docs.microsoft.com](http://docs.microsoft.com) の記事は [Markdown](https://daringfireball.net/projects/markdown/) という読みやすく、しかも簡単に学べる軽量マークアップ言語で記述されます。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-104">[Docs.microsoft.com](http://docs.microsoft.com) articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="2b4c0-105">そのため、これは急速に業界標準になりました。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-105">Because of this, it has quickly become an industry standard.</span></span>

<span data-ttu-id="2b4c0-106">Docs のコンテンツは GitHub に格納されるので、[GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/) と呼ばれる Markdown の上位セットを使用できます。GFM は一般的な書式要件のための追加機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-106">Since Docs content is stored in GitHub, it can use a superset of Markdown called [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), which provides additional functionality for common formatting needs.</span></span> <span data-ttu-id="2b4c0-107">さらに、Open Publishing Services (OPS) は Markdown パーサー Markdig を実装しています。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-107">Additionally, Open Publishing Services (OPS) implements Markdig Markdown Parser.</span></span> <span data-ttu-id="2b4c0-108">Markdig は GFM との互換性が高く、Docs 固有の機能を実現するための機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-108">Markdig is highly compatible with GFM, adding functionality to enable Docs-specific features.</span></span>

* <span data-ttu-id="2b4c0-109">Markdig は高速で、強力で、CommonMark に準拠した、.NET 向けの拡張可能なマークダウン プロセッサーです。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-109">Markdig is a fast, powerful, CommonMark compliant, extensible Markdown processor for .NET.</span></span>
* https://github.com/lunet-io/markdig
* <span data-ttu-id="2b4c0-110">優れたコミュニティ サポート</span><span class="sxs-lookup"><span data-stu-id="2b4c0-110">Better community support</span></span>
* <span data-ttu-id="2b4c0-111">優れた標準サポート</span><span class="sxs-lookup"><span data-stu-id="2b4c0-111">Better standards support</span></span>

## <a name="markdown-basics"></a><span data-ttu-id="2b4c0-112">Markdown の基本</span><span class="sxs-lookup"><span data-stu-id="2b4c0-112">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="2b4c0-113">見出し</span><span class="sxs-lookup"><span data-stu-id="2b4c0-113">Headings</span></span>

<span data-ttu-id="2b4c0-114">見出しを作成するには、ハッシュ記号 (#) を次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-114">To create a heading, you use a hash mark (#), as follows:</span></span>

```markdown
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

<span data-ttu-id="2b4c0-115">見出しは atx 形式で作成してください。つまり、行の先頭で 1 つから 6 つまでのハッシュ文字 (#) を使用して見出しを示し、H1 から H6 までの HTML 見出しレベルに対応させます。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-115">Headings should be done using atx-style, that is, use 1-6 hash characters (#) at the start of the line to indicate a heading, corresponding to HTML headings levels H1 through H6.</span></span> <span data-ttu-id="2b4c0-116">上の例では第 1 - 第 4 レベルのヘッダーが使用されています。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-116">Examples of first- through fourth-level headers are used above.</span></span>

<span data-ttu-id="2b4c0-117">トピックの第 1 レベルの見出し (H1) は 1 つだけにする**必要があります**。これはページ上のタイトルとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-117">There **must** be only one first-level heading (H1) in your topic, which will be displayed as the on-page title.</span></span>

<span data-ttu-id="2b4c0-118">見出しが `#` 文字で終わる場合、タイトルが正しくレンダリングされるように終わりに `#` 文字を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-118">If your heading finishes with a `#` character, you need to add an extra `#` character in the end in order for the title to render correctly.</span></span> <span data-ttu-id="2b4c0-119">たとえば、`# Async Programming in F# #` のようにします。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-119">For example, `# Async Programming in F# #`.</span></span>

<span data-ttu-id="2b4c0-120">第 2 レベルの見出しによってページ上の TOC が生成されます。これはページ上のタイトルの下にある "この記事の内容" セクションに表示されます。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-120">Second-level headings will generate the on-page TOC that appears in the "In this article" section underneath the on-page title.</span></span>

### <a name="bold-and-italic-text"></a><span data-ttu-id="2b4c0-121">太字や斜体のテキスト</span><span class="sxs-lookup"><span data-stu-id="2b4c0-121">Bold and italic text</span></span>

<span data-ttu-id="2b4c0-122">テキストの書式を**太字**に設定するには、テキストを二重のアスタリスクで囲みます。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-122">To format text as **bold**, you enclose it in two asterisks:</span></span>

```markdown
This text is **bold**.
```

<span data-ttu-id="2b4c0-123">テキストの書式を*斜体*に設定するには、テキストを一重のアスタリスクで囲みます。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-123">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```markdown
This text is *italic*.
```

<span data-ttu-id="2b4c0-124">テキストの書式を***太字と斜体***の両方に設定するには、テキストを三重のアスタリスクで囲みます。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-124">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```markdown
This is text is both ***bold and italic***.
```

### <a name="blockquotes"></a><span data-ttu-id="2b4c0-125">ブロック引用</span><span class="sxs-lookup"><span data-stu-id="2b4c0-125">Blockquotes</span></span>

<span data-ttu-id="2b4c0-126">ブロック引用は `>` 文字で作成されます。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-126">Blockquotes are created using the `>` character:</span></span>

```markdown
> The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended. Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight. In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.
```

<span data-ttu-id="2b4c0-127">先の例は次のようにレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-127">The preceding example renders as follows:</span></span>

> <span data-ttu-id="2b4c0-128">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span><span class="sxs-lookup"><span data-stu-id="2b4c0-128">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span></span> <span data-ttu-id="2b4c0-129">Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight.</span><span class="sxs-lookup"><span data-stu-id="2b4c0-129">Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight.</span></span> <span data-ttu-id="2b4c0-130">In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.</span><span class="sxs-lookup"><span data-stu-id="2b4c0-130">In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.</span></span>

### <a name="lists"></a><span data-ttu-id="2b4c0-131">リスト</span><span class="sxs-lookup"><span data-stu-id="2b4c0-131">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="2b4c0-132">記号付きリスト</span><span class="sxs-lookup"><span data-stu-id="2b4c0-132">Unordered list</span></span>

<span data-ttu-id="2b4c0-133">記号付きリスト/箇条書きリストの書式を設定するには、アスタリスクまたはダッシュを使用できます。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-133">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="2b4c0-134">たとえば、次の Markdown 書式は</span><span class="sxs-lookup"><span data-stu-id="2b4c0-134">For example, the following Markdown:</span></span>

```markdown
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="2b4c0-135">次のようにレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-135">will be rendered as:</span></span>

- <span data-ttu-id="2b4c0-136">List item 1</span><span class="sxs-lookup"><span data-stu-id="2b4c0-136">List item 1</span></span>
- <span data-ttu-id="2b4c0-137">List item 2</span><span class="sxs-lookup"><span data-stu-id="2b4c0-137">List item 2</span></span>
- <span data-ttu-id="2b4c0-138">List item 3</span><span class="sxs-lookup"><span data-stu-id="2b4c0-138">List item 3</span></span>

<span data-ttu-id="2b4c0-139">リストを別のリスト内にネストするには、子リスト アイテムをインデントします。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-139">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="2b4c0-140">たとえば、次の Markdown 書式は</span><span class="sxs-lookup"><span data-stu-id="2b4c0-140">For example, the following Markdown:</span></span>

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="2b4c0-141">次のようにレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-141">will be rendered as:</span></span>

- <span data-ttu-id="2b4c0-142">List item 1</span><span class="sxs-lookup"><span data-stu-id="2b4c0-142">List item 1</span></span>
  - <span data-ttu-id="2b4c0-143">List item A</span><span class="sxs-lookup"><span data-stu-id="2b4c0-143">List item A</span></span>
  - <span data-ttu-id="2b4c0-144">List item B</span><span class="sxs-lookup"><span data-stu-id="2b4c0-144">List item B</span></span>
- <span data-ttu-id="2b4c0-145">List item 2</span><span class="sxs-lookup"><span data-stu-id="2b4c0-145">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="2b4c0-146">番号付きリスト</span><span class="sxs-lookup"><span data-stu-id="2b4c0-146">Ordered list</span></span>

<span data-ttu-id="2b4c0-147">番号付きリスト/段階的リストの書式を設定するには、対応する番号を使用します。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-147">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="2b4c0-148">たとえば、次の Markdown 書式は</span><span class="sxs-lookup"><span data-stu-id="2b4c0-148">For example, the following Markdown:</span></span>

```markdown
1. First instruction
1. Second instruction
1. Third instruction
```

<span data-ttu-id="2b4c0-149">次のようにレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-149">will be rendered as:</span></span>

1. <span data-ttu-id="2b4c0-150">第 1 手順</span><span class="sxs-lookup"><span data-stu-id="2b4c0-150">First instruction</span></span>
2. <span data-ttu-id="2b4c0-151">第 2 手順</span><span class="sxs-lookup"><span data-stu-id="2b4c0-151">Second instruction</span></span>
3. <span data-ttu-id="2b4c0-152">第 3 手順</span><span class="sxs-lookup"><span data-stu-id="2b4c0-152">Third instruction</span></span>

<span data-ttu-id="2b4c0-153">リストを別のリスト内にネストするには、子リスト アイテムをインデントします。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-153">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="2b4c0-154">たとえば、次の Markdown 書式は</span><span class="sxs-lookup"><span data-stu-id="2b4c0-154">For example, the following Markdown:</span></span>

```markdown
1. First instruction
   1. Sub-instruction
   1. Sub-instruction
1. Second instruction
```

<span data-ttu-id="2b4c0-155">次のようにレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-155">will be rendered as:</span></span>

1. <span data-ttu-id="2b4c0-156">第 1 手順</span><span class="sxs-lookup"><span data-stu-id="2b4c0-156">First instruction</span></span>
   1. <span data-ttu-id="2b4c0-157">下位手順</span><span class="sxs-lookup"><span data-stu-id="2b4c0-157">Sub-instruction</span></span>
   2. <span data-ttu-id="2b4c0-158">下位手順</span><span class="sxs-lookup"><span data-stu-id="2b4c0-158">Sub-instruction</span></span>
2. <span data-ttu-id="2b4c0-159">第 2 手順</span><span class="sxs-lookup"><span data-stu-id="2b4c0-159">Second instruction</span></span>

<span data-ttu-id="2b4c0-160">すべてのエントリに対して '1.' を</span><span class="sxs-lookup"><span data-stu-id="2b4c0-160">Note that we use '1.'</span></span> <span data-ttu-id="2b4c0-161">使用していることに注目してください。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-161">for all entries.</span></span> <span data-ttu-id="2b4c0-162">後の更新で新しい手順が追加されるときや既存の手順が削除されるとき、見直しが簡単になります。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-162">It makes diffs easier to review when later updates include new steps or remove existing steps.</span></span>

### <a name="tables"></a><span data-ttu-id="2b4c0-163">表</span><span class="sxs-lookup"><span data-stu-id="2b4c0-163">Tables</span></span>

<span data-ttu-id="2b4c0-164">Markdown の基本仕様には表が含まれていませんが、GFM が表をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-164">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="2b4c0-165">パイプ (|) 記号とハイフン記号 (-) を使用して表を作成できます。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-165">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="2b4c0-166">ハイフンは各列のヘッダーを作成し、パイプは各列を区切ります。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-166">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="2b4c0-167">表が正しくレンダリングされるように、表の前に空の行を 1 つ挿入してください。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-167">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="2b4c0-168">たとえば、次の Markdown 書式は</span><span class="sxs-lookup"><span data-stu-id="2b4c0-168">For example, the following Markdown:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="2b4c0-169">次のようにレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-169">will be rendered as:</span></span>

| <span data-ttu-id="2b4c0-170">Fun</span><span class="sxs-lookup"><span data-stu-id="2b4c0-170">Fun</span></span>                  | <span data-ttu-id="2b4c0-171">With</span><span class="sxs-lookup"><span data-stu-id="2b4c0-171">With</span></span>                 | <span data-ttu-id="2b4c0-172">表</span><span class="sxs-lookup"><span data-stu-id="2b4c0-172">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="2b4c0-173">left-aligned column</span><span class="sxs-lookup"><span data-stu-id="2b4c0-173">left-aligned column</span></span>  | <span data-ttu-id="2b4c0-174">right-aligned column</span><span class="sxs-lookup"><span data-stu-id="2b4c0-174">right-aligned column</span></span> | <span data-ttu-id="2b4c0-175">centered column</span><span class="sxs-lookup"><span data-stu-id="2b4c0-175">centered column</span></span> |
| <span data-ttu-id="2b4c0-176">$100</span><span class="sxs-lookup"><span data-stu-id="2b4c0-176">$100</span></span>                 | <span data-ttu-id="2b4c0-177">$100</span><span class="sxs-lookup"><span data-stu-id="2b4c0-177">$100</span></span>                 | <span data-ttu-id="2b4c0-178">$100</span><span class="sxs-lookup"><span data-stu-id="2b4c0-178">$100</span></span>            |
| <span data-ttu-id="2b4c0-179">$10</span><span class="sxs-lookup"><span data-stu-id="2b4c0-179">$10</span></span>                  | <span data-ttu-id="2b4c0-180">$10</span><span class="sxs-lookup"><span data-stu-id="2b4c0-180">$10</span></span>                  | <span data-ttu-id="2b4c0-181">$10</span><span class="sxs-lookup"><span data-stu-id="2b4c0-181">$10</span></span>             |
| <span data-ttu-id="2b4c0-182">$1</span><span class="sxs-lookup"><span data-stu-id="2b4c0-182">$1</span></span>                   | <span data-ttu-id="2b4c0-183">$1</span><span class="sxs-lookup"><span data-stu-id="2b4c0-183">$1</span></span>                   | <span data-ttu-id="2b4c0-184">$1</span><span class="sxs-lookup"><span data-stu-id="2b4c0-184">$1</span></span>              |

<span data-ttu-id="2b4c0-185">表作成の詳細については、以下の情報源をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-185">For more information on creating tables, see:</span></span>

- <span data-ttu-id="2b4c0-186">横に長い表の書式設定に役立つ、Markdig の「[表を折り返す機能](#table-wrapping)」。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-186">The Markdig [table wrapping feature](#table-wrapping), which can help with formatting of wide tables.</span></span>
- <span data-ttu-id="2b4c0-187">GitHub の「[Organizing information with tables (表を使用した情報の整理)](https://help.github.com/articles/organizing-information-with-tables/)」。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-187">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/).</span></span>
- <span data-ttu-id="2b4c0-188">[Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) Web アプリ。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-188">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app.</span></span>
- <span data-ttu-id="2b4c0-189">Adam Pritchard 氏の「[Markdown Cheatsheet (Markdown に関する簡易参照ガイド)](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables)」。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-189">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span></span>
- <span data-ttu-id="2b4c0-190">Michel Fortin 氏の [Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table) に関するページ。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-190">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table).</span></span>
- <span data-ttu-id="2b4c0-191">[HTML テーブルからマークダウンへの変換](https://jmalarcon.github.io/markdowntables/)。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-191">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/).</span></span>

### <a name="links"></a><span data-ttu-id="2b4c0-192">リンク</span><span class="sxs-lookup"><span data-stu-id="2b4c0-192">Links</span></span>

<span data-ttu-id="2b4c0-193">インライン リンクの Markdown 構文では、ハイパーリンクされるテキスト部分 `[link text]` の後に、リンク先 URL またはファイル名の部分 `(file-name.md)` が続きます。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-193">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="2b4c0-194">リンクの詳細については、以下の情報源をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-194">For more information on linking, see:</span></span>

- <span data-ttu-id="2b4c0-195">Markdown のリンクの基本的なサポートについては、[Markdown の構文](https://daringfireball.net/projects/markdown/syntax#link)に関するセクション。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-195">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="2b4c0-196">Markdig で提供されるその他のリンク構文の詳細については、このガイドの[リンク](how-to-write-links.md)に関するセクション。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-196">The [Links](how-to-write-links.md) section of this guide for details on the additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="2b4c0-197">コード スニペット</span><span class="sxs-lookup"><span data-stu-id="2b4c0-197">Code snippets</span></span>

<span data-ttu-id="2b4c0-198">Markdown では、コード スニペットの配置方法として、文中へのインライン配置と、文と文の間への "フェンスされた" 個別ブロックとしての配置の両方がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-198">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="2b4c0-199">詳細については、以下の情報源をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-199">For details, see:</span></span>

- <span data-ttu-id="2b4c0-200">[Markdown のコード ブロックのネイティブ サポート](https://daringfireball.net/projects/markdown/syntax#precode)に関するセクション</span><span class="sxs-lookup"><span data-stu-id="2b4c0-200">[Markdown's native support for code blocks](https://daringfireball.net/projects/markdown/syntax#precode)</span></span>
- <span data-ttu-id="2b4c0-201">[GFM のコード フェンスと構文強調表示のサポート](https://help.github.com/articles/creating-and-highlighting-code-blocks/)に関するページ</span><span class="sxs-lookup"><span data-stu-id="2b4c0-201">[GFM support for code fencing and syntax highlighting](https://help.github.com/articles/creating-and-highlighting-code-blocks/)</span></span>

<span data-ttu-id="2b4c0-202">コード ブロックをフェンスすることで、コード スニペットの構文を強調表示することができます。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-202">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="2b4c0-203">フェンスされたコード ブロックの一般的な書式は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-203">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="2b4c0-204">冒頭の 3 つのバッククォート (\`) 記号に続くエイリアスは、使用される構文強調表示を定義します。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-204">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="2b4c0-205">以下は Docs コンテンツで一般的に使用されるプログラミング言語と、対応するラベルのリストです。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-205">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="2b4c0-206">これらの言語は、フレンドリ名をサポートし、ほとんどに言語の強調表示機能があります。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-206">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="2b4c0-207">名前</span><span class="sxs-lookup"><span data-stu-id="2b4c0-207">Name</span></span>|<span data-ttu-id="2b4c0-208">Markdown ラベル</span><span class="sxs-lookup"><span data-stu-id="2b4c0-208">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="2b4c0-209">.NET コンソール</span><span class="sxs-lookup"><span data-stu-id="2b4c0-209">.NET Console</span></span>|<span data-ttu-id="2b4c0-210">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="2b4c0-210">dotnetcli</span></span>|
|<span data-ttu-id="2b4c0-211">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="2b4c0-211">ASP.NET (C#)</span></span>|<span data-ttu-id="2b4c0-212">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="2b4c0-212">aspx-csharp</span></span>|
|<span data-ttu-id="2b4c0-213">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="2b4c0-213">ASP.NET (VB)</span></span>|<span data-ttu-id="2b4c0-214">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="2b4c0-214">aspx-vb</span></span>|
|<span data-ttu-id="2b4c0-215">AzCopy</span><span class="sxs-lookup"><span data-stu-id="2b4c0-215">AzCopy</span></span>|<span data-ttu-id="2b4c0-216">azcopy</span><span class="sxs-lookup"><span data-stu-id="2b4c0-216">azcopy</span></span>|
|<span data-ttu-id="2b4c0-217">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="2b4c0-217">Azure CLI</span></span>|<span data-ttu-id="2b4c0-218">azurecli</span><span class="sxs-lookup"><span data-stu-id="2b4c0-218">azurecli</span></span>|
|<span data-ttu-id="2b4c0-219">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="2b4c0-219">Azure PowerShell</span></span>|<span data-ttu-id="2b4c0-220">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="2b4c0-220">azurepowershell</span></span>|
|<span data-ttu-id="2b4c0-221">C++</span><span class="sxs-lookup"><span data-stu-id="2b4c0-221">C++</span></span>|<span data-ttu-id="2b4c0-222">cpp</span><span class="sxs-lookup"><span data-stu-id="2b4c0-222">cpp</span></span>|
|<span data-ttu-id="2b4c0-223">C++/CX</span><span class="sxs-lookup"><span data-stu-id="2b4c0-223">C++/CX</span></span>|<span data-ttu-id="2b4c0-224">cppcx</span><span class="sxs-lookup"><span data-stu-id="2b4c0-224">cppcx</span></span>|
|<span data-ttu-id="2b4c0-225">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="2b4c0-225">C++/WinRT</span></span>|<span data-ttu-id="2b4c0-226">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="2b4c0-226">cppwinrt</span></span>|
|<span data-ttu-id="2b4c0-227">C#</span><span class="sxs-lookup"><span data-stu-id="2b4c0-227">C#</span></span>|<span data-ttu-id="2b4c0-228">csharp</span><span class="sxs-lookup"><span data-stu-id="2b4c0-228">csharp</span></span>|
|<span data-ttu-id="2b4c0-229">ブラウザーの C#</span><span class="sxs-lookup"><span data-stu-id="2b4c0-229">C# in browser</span></span>|<span data-ttu-id="2b4c0-230">csharp-interactive</span><span class="sxs-lookup"><span data-stu-id="2b4c0-230">csharp-interactive</span></span>|
|<span data-ttu-id="2b4c0-231">コンソール</span><span class="sxs-lookup"><span data-stu-id="2b4c0-231">Console</span></span>|<span data-ttu-id="2b4c0-232">console</span><span class="sxs-lookup"><span data-stu-id="2b4c0-232">console</span></span>|
|<span data-ttu-id="2b4c0-233">CSHTML</span><span class="sxs-lookup"><span data-stu-id="2b4c0-233">CSHTML</span></span>|<span data-ttu-id="2b4c0-234">cshtml</span><span class="sxs-lookup"><span data-stu-id="2b4c0-234">cshtml</span></span>|
|<span data-ttu-id="2b4c0-235">DAX</span><span class="sxs-lookup"><span data-stu-id="2b4c0-235">DAX</span></span>|<span data-ttu-id="2b4c0-236">dax</span><span class="sxs-lookup"><span data-stu-id="2b4c0-236">dax</span></span>|
|<span data-ttu-id="2b4c0-237">F#</span><span class="sxs-lookup"><span data-stu-id="2b4c0-237">F#</span></span>|<span data-ttu-id="2b4c0-238">fsharp</span><span class="sxs-lookup"><span data-stu-id="2b4c0-238">fsharp</span></span>|
|<span data-ttu-id="2b4c0-239">Go</span><span class="sxs-lookup"><span data-stu-id="2b4c0-239">Go</span></span>|<span data-ttu-id="2b4c0-240">go</span><span class="sxs-lookup"><span data-stu-id="2b4c0-240">go</span></span>|
|<span data-ttu-id="2b4c0-241">HTML</span><span class="sxs-lookup"><span data-stu-id="2b4c0-241">HTML</span></span>|<span data-ttu-id="2b4c0-242">html</span><span class="sxs-lookup"><span data-stu-id="2b4c0-242">html</span></span>|
|<span data-ttu-id="2b4c0-243">HTTP</span><span class="sxs-lookup"><span data-stu-id="2b4c0-243">HTTP</span></span>|<span data-ttu-id="2b4c0-244">http</span><span class="sxs-lookup"><span data-stu-id="2b4c0-244">http</span></span>|
|<span data-ttu-id="2b4c0-245">Java</span><span class="sxs-lookup"><span data-stu-id="2b4c0-245">Java</span></span>|<span data-ttu-id="2b4c0-246">java</span><span class="sxs-lookup"><span data-stu-id="2b4c0-246">java</span></span>|
|<span data-ttu-id="2b4c0-247">JavaScript</span><span class="sxs-lookup"><span data-stu-id="2b4c0-247">JavaScript</span></span>|<span data-ttu-id="2b4c0-248">javascript</span><span class="sxs-lookup"><span data-stu-id="2b4c0-248">javascript</span></span>|
|<span data-ttu-id="2b4c0-249">JSON</span><span class="sxs-lookup"><span data-stu-id="2b4c0-249">JSON</span></span>|<span data-ttu-id="2b4c0-250">json</span><span class="sxs-lookup"><span data-stu-id="2b4c0-250">json</span></span>|
|<span data-ttu-id="2b4c0-251">Markdown</span><span class="sxs-lookup"><span data-stu-id="2b4c0-251">Markdown</span></span>|<span data-ttu-id="2b4c0-252">md</span><span class="sxs-lookup"><span data-stu-id="2b4c0-252">md</span></span>|
|<span data-ttu-id="2b4c0-253">NodeJS</span><span class="sxs-lookup"><span data-stu-id="2b4c0-253">NodeJS</span></span>|<span data-ttu-id="2b4c0-254">nodejs</span><span class="sxs-lookup"><span data-stu-id="2b4c0-254">nodejs</span></span>|
|<span data-ttu-id="2b4c0-255">Objective-C</span><span class="sxs-lookup"><span data-stu-id="2b4c0-255">Objective-C</span></span>|<span data-ttu-id="2b4c0-256">objc</span><span class="sxs-lookup"><span data-stu-id="2b4c0-256">objc</span></span>|
|<span data-ttu-id="2b4c0-257">OData</span><span class="sxs-lookup"><span data-stu-id="2b4c0-257">OData</span></span>|<span data-ttu-id="2b4c0-258">odata</span><span class="sxs-lookup"><span data-stu-id="2b4c0-258">odata</span></span>|
|<span data-ttu-id="2b4c0-259">PHP</span><span class="sxs-lookup"><span data-stu-id="2b4c0-259">PHP</span></span>|<span data-ttu-id="2b4c0-260">php</span><span class="sxs-lookup"><span data-stu-id="2b4c0-260">php</span></span>|
|<span data-ttu-id="2b4c0-261">Power Apps Formula</span><span class="sxs-lookup"><span data-stu-id="2b4c0-261">Power Apps Formula</span></span>|<span data-ttu-id="2b4c0-262">powerappsfl</span><span class="sxs-lookup"><span data-stu-id="2b4c0-262">powerappsfl</span></span>|
|<span data-ttu-id="2b4c0-263">PowerShell</span><span class="sxs-lookup"><span data-stu-id="2b4c0-263">PowerShell</span></span>|<span data-ttu-id="2b4c0-264">powershell</span><span class="sxs-lookup"><span data-stu-id="2b4c0-264">powershell</span></span>|
|<span data-ttu-id="2b4c0-265">Python</span><span class="sxs-lookup"><span data-stu-id="2b4c0-265">Python</span></span>|<span data-ttu-id="2b4c0-266">python</span><span class="sxs-lookup"><span data-stu-id="2b4c0-266">python</span></span>|
|<span data-ttu-id="2b4c0-267">Q#</span><span class="sxs-lookup"><span data-stu-id="2b4c0-267">Q#</span></span>|<span data-ttu-id="2b4c0-268">qsharp</span><span class="sxs-lookup"><span data-stu-id="2b4c0-268">qsharp</span></span>|
|<span data-ttu-id="2b4c0-269">R</span><span class="sxs-lookup"><span data-stu-id="2b4c0-269">R</span></span>|<span data-ttu-id="2b4c0-270">r</span><span class="sxs-lookup"><span data-stu-id="2b4c0-270">r</span></span>|
|<span data-ttu-id="2b4c0-271">Ruby</span><span class="sxs-lookup"><span data-stu-id="2b4c0-271">Ruby</span></span>|<span data-ttu-id="2b4c0-272">ruby</span><span class="sxs-lookup"><span data-stu-id="2b4c0-272">ruby</span></span>|
|<span data-ttu-id="2b4c0-273">SQL</span><span class="sxs-lookup"><span data-stu-id="2b4c0-273">SQL</span></span>|<span data-ttu-id="2b4c0-274">sql</span><span class="sxs-lookup"><span data-stu-id="2b4c0-274">sql</span></span>|
|<span data-ttu-id="2b4c0-275">Swift</span><span class="sxs-lookup"><span data-stu-id="2b4c0-275">Swift</span></span>|<span data-ttu-id="2b4c0-276">swift</span><span class="sxs-lookup"><span data-stu-id="2b4c0-276">swift</span></span>|
|<span data-ttu-id="2b4c0-277">TypeScript</span><span class="sxs-lookup"><span data-stu-id="2b4c0-277">TypeScript</span></span>|<span data-ttu-id="2b4c0-278">typescript</span><span class="sxs-lookup"><span data-stu-id="2b4c0-278">typescript</span></span>|
|<span data-ttu-id="2b4c0-279">VB</span><span class="sxs-lookup"><span data-stu-id="2b4c0-279">VB</span></span>|<span data-ttu-id="2b4c0-280">vb</span><span class="sxs-lookup"><span data-stu-id="2b4c0-280">vb</span></span>|
|<span data-ttu-id="2b4c0-281">VSTS CLI</span><span class="sxs-lookup"><span data-stu-id="2b4c0-281">VSTS CLI</span></span>|<span data-ttu-id="2b4c0-282">vstscli</span><span class="sxs-lookup"><span data-stu-id="2b4c0-282">vstscli</span></span>|
|<span data-ttu-id="2b4c0-283">XAML</span><span class="sxs-lookup"><span data-stu-id="2b4c0-283">XAML</span></span>|<span data-ttu-id="2b4c0-284">xaml</span><span class="sxs-lookup"><span data-stu-id="2b4c0-284">xaml</span></span>|
|<span data-ttu-id="2b4c0-285">XML</span><span class="sxs-lookup"><span data-stu-id="2b4c0-285">XML</span></span>|<span data-ttu-id="2b4c0-286">xml</span><span class="sxs-lookup"><span data-stu-id="2b4c0-286">xml</span></span>|

<span data-ttu-id="2b4c0-287">`csharp-interactive` 名によって C# 言語と、ブラウザーからサンプルを実行する機能が指定されます。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-287">The `csharp-interactive` name specifies the C# language, and the ability to run the samples from the browser.</span></span> <span data-ttu-id="2b4c0-288">このようなスニペットは Docker コンテナーでコンパイルされ、実行されます。そのプログラム実行の結果はユーザーのブラウザー ウィンドウに表示されます。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-288">These snippets are compiled and executed in a Docker container, and the results of that program execution are displayed in the user's browser window.</span></span>

#### <a name="example-c"></a><span data-ttu-id="2b4c0-289">例:C\#</span><span class="sxs-lookup"><span data-stu-id="2b4c0-289">Example: C\#</span></span>

<span data-ttu-id="2b4c0-290">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="2b4c0-290">__Markdown__</span></span>

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

<span data-ttu-id="2b4c0-291">__レンダー__</span><span class="sxs-lookup"><span data-stu-id="2b4c0-291">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="2b4c0-292">例:SQL</span><span class="sxs-lookup"><span data-stu-id="2b4c0-292">Example: SQL</span></span>

<span data-ttu-id="2b4c0-293">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="2b4c0-293">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="2b4c0-294">__レンダー__</span><span class="sxs-lookup"><span data-stu-id="2b4c0-294">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a><span data-ttu-id="2b4c0-295">OPS による Markdown のカスタム拡張機能</span><span class="sxs-lookup"><span data-stu-id="2b4c0-295">OPS custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="2b4c0-296">Open Publishing Services (OPS) は GitHub Flavored Markdown (GFM) との互換性が非常に高い Markdown パーサー Markdig を実装しています。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-296">Open Publishing Services (OPS) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="2b4c0-297">Markdig は Markdown 拡張機能を介していくつかの機能を追加しています。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-297">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="2b4c0-298">そのため、完全版の「OPS Authoring Guide」 (OPS オーサリング ガイド) の一部の記事は、参考のためにこのガイドに含まれています </span><span class="sxs-lookup"><span data-stu-id="2b4c0-298">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="2b4c0-299">(たとえば、目次の「Markdig and Markdown extensions」(Markdig と Markdown の拡張機能) と「Code snippets」(コード スニペット) をご覧ください)。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-299">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="2b4c0-300">Docs 記事では、段落、リンク、リスト、見出しなど、ほとんどの書式設定に GFM が使用されます。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-300">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="2b4c0-301">記事の高度な書式設定には、次のような Markdig 機能を使用できます。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-301">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="2b4c0-302">注ブロック</span><span class="sxs-lookup"><span data-stu-id="2b4c0-302">Note blocks</span></span>
- <span data-ttu-id="2b4c0-303">インクルード ファイル</span><span class="sxs-lookup"><span data-stu-id="2b4c0-303">Include files</span></span>
- <span data-ttu-id="2b4c0-304">セレクター</span><span class="sxs-lookup"><span data-stu-id="2b4c0-304">Selectors</span></span>
- <span data-ttu-id="2b4c0-305">埋め込みビデオ</span><span class="sxs-lookup"><span data-stu-id="2b4c0-305">Embedded videos</span></span>
- <span data-ttu-id="2b4c0-306">コード スニペット/サンプル</span><span class="sxs-lookup"><span data-stu-id="2b4c0-306">Code snippets/samples</span></span>

<span data-ttu-id="2b4c0-307">完全なリストについては、目次の「Markdig and Markdown extensions」(Markdig と Markdown の拡張機能) と「Code snippets」(コード スニペット) をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-307">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="2b4c0-308">注ブロック</span><span class="sxs-lookup"><span data-stu-id="2b4c0-308">Note blocks</span></span>

<span data-ttu-id="2b4c0-309">特定の内容に注目を集めるには、4 つのタイプの注ブロックから選択できます。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-309">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="2b4c0-310">NOTE (注意)</span><span class="sxs-lookup"><span data-stu-id="2b4c0-310">NOTE</span></span>
- <span data-ttu-id="2b4c0-311">WARNING (警告)</span><span class="sxs-lookup"><span data-stu-id="2b4c0-311">WARNING</span></span>
- <span data-ttu-id="2b4c0-312">TIP (ヒント)</span><span class="sxs-lookup"><span data-stu-id="2b4c0-312">TIP</span></span>
- <span data-ttu-id="2b4c0-313">IMPORTANT (重要)</span><span class="sxs-lookup"><span data-stu-id="2b4c0-313">IMPORTANT</span></span>

<span data-ttu-id="2b4c0-314">注ブロックによって文章がわかりにくくなることがあるので、概して注ブロックは控えめに使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-314">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="2b4c0-315">注ブロックでもコード ブロック、イメージ、リスト、およびリンクがサポートされますが、注ブロックを簡潔でわかりやすくするように心掛けてください。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-315">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

<span data-ttu-id="2b4c0-316">例:</span><span class="sxs-lookup"><span data-stu-id="2b4c0-316">Examples:</span></span>

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

<span data-ttu-id="2b4c0-317">これは次のようにレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-317">These render as follows:</span></span>

> [!NOTE]
> <span data-ttu-id="2b4c0-318">This is a NOTE</span><span class="sxs-lookup"><span data-stu-id="2b4c0-318">This is a NOTE</span></span>

> [!WARNING]
> <span data-ttu-id="2b4c0-319">This is a WARNING</span><span class="sxs-lookup"><span data-stu-id="2b4c0-319">This is a WARNING</span></span>

> [!TIP]
> <span data-ttu-id="2b4c0-320">This is a TIP</span><span class="sxs-lookup"><span data-stu-id="2b4c0-320">This is a TIP</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2b4c0-321">This is IMPORTANT</span><span class="sxs-lookup"><span data-stu-id="2b4c0-321">This is IMPORTANT</span></span>

### <a name="include-files"></a><span data-ttu-id="2b4c0-322">インクルード ファイル</span><span class="sxs-lookup"><span data-stu-id="2b4c0-322">Include files</span></span>

<span data-ttu-id="2b4c0-323">再利用可能なテキスト ファイルまたはイメージ ファイルを記事ファイルにインクルードする必要がある場合は、Markdig のファイル インクルード機能を使用して "インクルード" ファイルを参照できます。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-323">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="2b4c0-324">この機能は、ビルド時に特定のファイルを記事ファイルにインクルードするように OPS に指示します。これにより、その指定されたファイルは公開記事に含まれるようになります。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-324">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="2b4c0-325">コンテンツの再利用に役立つインクルード参照には、次の 3 種類があります。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-325">Three types of include references are available to help you reuse content:</span></span>

- <span data-ttu-id="2b4c0-326">インライン: 一般的なテキスト スニペットを別の文中にインラインで再利用できます。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-326">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="2b4c0-327">ブロック: Markdown ファイル全体をブロックとして再利用し、記事のセクション内にネストできます。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-327">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="2b4c0-328">イメージ: これは Docs に実装されている標準的なイメージ インクルードの方法です。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-328">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="2b4c0-329">インラインまたはブロックによるインクルード ファイルはシンプルな Markdown (.md) ファイルにすぎません。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-329">An inline or block include file is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="2b4c0-330">これにはあらゆる有効な Markdown を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-330">It can contain any valid Markdown.</span></span> <span data-ttu-id="2b4c0-331">すべてのインクルード Markdown ファイルは、リポジトリのルートにある[共通の `/includes` サブディレクトリ](git-github-fundamentals.md#includes-subdirectory)に配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-331">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="2b4c0-332">記事が公開されると、インクルードされたファイルはその記事にシームレスに統合されます。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-332">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="2b4c0-333">インクルード ファイルに関する要件と考慮事項を次に示します。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-333">Here are requirements and considerations for include files:</span></span>

- <span data-ttu-id="2b4c0-334">複数の記事に同じテキストを表示する必要があるときは必ず、インクルード ファイルを使用してください。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-334">Use an include file whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="2b4c0-335">ブロックによるインクルード参照は、1 つまたは 2 つの段落、共通の手順、共通のセクションといった分量の多いコンテンツに使用してください。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-335">Use a block include reference for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="2b4c0-336">1 つの文よりも小さい場合には、使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-336">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="2b4c0-337">インクルード参照は Markdig 拡張機能に依存するため、GitHub でレンダリングされた記事内でインクルード参照はレンダリングされません。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-337">Include references won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="2b4c0-338">公開後にのみレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-338">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="2b4c0-339">インクルード ファイル内のすべてのテキストが、インクルード ファイルを参照する記事内の先行テキストまたは後続テキストに依存しない完全な文または語句で記述されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-339">Ensure that all the text in an include file is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include file.</span></span> <span data-ttu-id="2b4c0-340">このガイダンスを無視すると、ローカライズされたエクスペリエンスを乱す翻訳不可能な文字列が記事内に発生します。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-340">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="2b4c0-341">インクルード参照をほかのインクルード ファイル内に埋め込まないでください。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-341">Don't embed include references within other include files.</span></span> <span data-ttu-id="2b4c0-342">それはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-342">They are not supported.</span></span>
- <span data-ttu-id="2b4c0-343">メディア ファイルは、インクルードのサブディレクトリ内にあるメディア フォルダーに配置する必要があります。たとえば、`<repo>`/includes/media フォルダーです。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-343">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="2b4c0-344">メディア ディレクトリのルートにはイメージを配置しないでください。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-344">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="2b4c0-345">インクルード ファイルにイメージが含まれていない場合、対応するメディア ディレクトリは不要です。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-345">If the include file does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="2b4c0-346">通常の記事と同様に、インクルード ファイル間でメディアを共有しないでください。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-346">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="2b4c0-347">インクルード ファイルおよび記事ごとに、一意の名前を持つ個別ファイルを使用してください。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-347">Use a separate file with a unique name for each include file and article.</span></span> <span data-ttu-id="2b4c0-348">メディア ファイルは、インクルード ファイルに関連付けられたメディア フォルダーに格納してください。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-348">Store the media file in the media folder that's associated with the include file.</span></span>
- <span data-ttu-id="2b4c0-349">記事の唯一のコンテンツとしてインクルード ファイルを使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-349">Don't use an include file as the only content of an article.</span></span>  <span data-ttu-id="2b4c0-350">インクルード ファイルの目的は、記事の残りの部分にあるコンテンツを補完することです。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-350">Include files are meant to be supplemental to the content in the rest of the article.</span></span>

<span data-ttu-id="2b4c0-351">例:</span><span class="sxs-lookup"><span data-stu-id="2b4c0-351">Example:</span></span>

```markdown
[!INCLUDE[sample include file](../includes/sampleinclude.md)]
```

### <a name="selectors"></a><span data-ttu-id="2b4c0-352">セレクター</span><span class="sxs-lookup"><span data-stu-id="2b4c0-352">Selectors</span></span>

<span data-ttu-id="2b4c0-353">同じ技術記事の複数のバージョンを記述するときには、複数のテクノロジまたはプラットフォームの実装の違いに対応するために、セレクターを使用します。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-353">Use selectors in technical articles when you author multiple flavors of the same article, to  address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="2b4c0-354">通常、これが最も当てはまるのは、Microsoft の開発者向けのモバイル プラットフォームのコンテンツです。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-354">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="2b4c0-355">現在 Markdig にはシングル セレクターとマルチ セレクターという 2 つのタイプのセレクターがあります。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-355">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="2b4c0-356">選択範囲内の各記事に配置されるセレクター Markdown は同じであるため、ご自分の記事に対するセレクターをインクルード ファイルに配置することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-356">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include file.</span></span> <span data-ttu-id="2b4c0-357">その上で、同じセレクターを使用するご自分のすべての記事内で、そのインクルード ファイルを参照できます。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-357">Then you can reference that include file in all your articles that use the same selector.</span></span>

<span data-ttu-id="2b4c0-358">次にセレクターの例を示します。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-358">The following shows an example selector:</span></span>

```markdown
> [!div class="op_single_selector"]
- [macOS](../docs/core/tutorials/using-on-macos.md)
- [Windows](../docs/core/tutorials/with-visual-studio.md)
```

<span data-ttu-id="2b4c0-359">[Azure ドキュメント](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic)で、実際に使われているセレクターの例を確認できます。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-359">You can see an example of selectors in action at the [Azure docs](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span></span>

### <a name="code-include-references"></a><span data-ttu-id="2b4c0-360">コードのインクルード参照</span><span class="sxs-lookup"><span data-stu-id="2b4c0-360">Code include references</span></span>

<span data-ttu-id="2b4c0-361">Markdig では、コード スニペット拡張機能を使用した記事へのコードの高度なインクルードがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-361">Markdig supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="2b4c0-362">プログラミング言語の選択や構文の色分けといった GFM 機能に基づく高度なレンダリングに加えて、次のような便利な機能を使用できます。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-362">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="2b4c0-363">外部リポジトリから集められたコード サンプル/スニペットのインクルード。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-363">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="2b4c0-364">さまざまな言語でのさまざまなバージョンのコード サンプルをタブに表示する UI。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-364">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="2b4c0-365">問題の発見 + トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="2b4c0-365">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="2b4c0-366">alt テキスト</span><span class="sxs-lookup"><span data-stu-id="2b4c0-366">Alt text</span></span>

<span data-ttu-id="2b4c0-367">アンダー スコアを含む alt テキストは正しくレンダリングされません。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-367">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="2b4c0-368">たとえば、次のテキストを使用するのではなく、</span><span class="sxs-lookup"><span data-stu-id="2b4c0-368">For example, instead of using this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="2b4c0-369">次のようにアンダー スコアをエスケープします。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-369">Escape the underscores like this:</span></span>

```markdown
![ADextension\_2FA\_Configure\_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="2b4c0-370">アポストロフィと引用符</span><span class="sxs-lookup"><span data-stu-id="2b4c0-370">Apostrophes and quotation marks</span></span>

<span data-ttu-id="2b4c0-371">Word から Markdown エディターにコピーしたテキストに、"スマート" (カールした) アポストロフィまたは引用符が含まれていることがあります。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-371">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="2b4c0-372">これらを標準的なアポストロフィや引用符にエンコードまたは変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-372">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="2b4c0-373">そうしないと、ファイルが公開されたときに次のように表示されます: Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="2b4c0-373">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="2b4c0-374">これらの "スマート" バージョンの記述記号のエンコーディングは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-374">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="2b4c0-375">左 (始め) 二重引用符: `&#8220;`</span><span class="sxs-lookup"><span data-stu-id="2b4c0-375">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="2b4c0-376">右 (終わり) 二重引用符: `&#8221;`</span><span class="sxs-lookup"><span data-stu-id="2b4c0-376">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="2b4c0-377">右 (終わり) 一重引用符またはアポストロフィ: `&#8217;`</span><span class="sxs-lookup"><span data-stu-id="2b4c0-377">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="2b4c0-378">左 (始め) 一重引用符 (あまり使用されません): `&#8216;`</span><span class="sxs-lookup"><span data-stu-id="2b4c0-378">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="2b4c0-379">山かっこ</span><span class="sxs-lookup"><span data-stu-id="2b4c0-379">Angle brackets</span></span>

<span data-ttu-id="2b4c0-380">プレースホルダーを示す目的では一般的に山括弧が使用されます。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-380">It is common to use angle brackets to denote a placeholder.</span></span> <span data-ttu-id="2b4c0-381">これを (コードではなく) テキストで行うときは、山括弧で囲む必要があります。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-381">When you do this in text (not code), you must encode the angle brackets.</span></span> <span data-ttu-id="2b4c0-382">そうしないと、それらのテキストは Markdown によって HTML タグとして認識されます。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-382">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="2b4c0-383">たとえば、`<script name>` を `&lt;script name&gt;` にエンコードしてください。</span><span class="sxs-lookup"><span data-stu-id="2b4c0-383">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="see-also"></a><span data-ttu-id="2b4c0-384">関連項目:</span><span class="sxs-lookup"><span data-stu-id="2b4c0-384">See also:</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="2b4c0-385">Markdown に関するリソース</span><span class="sxs-lookup"><span data-stu-id="2b4c0-385">Markdown resources</span></span>

- [<span data-ttu-id="2b4c0-386">Markdown 入門</span><span class="sxs-lookup"><span data-stu-id="2b4c0-386">Introduction to Markdown</span></span>](https://daringfireball.net/projects/markdown/syntax)
- [<span data-ttu-id="2b4c0-387">Docs の Markdown に関する簡易参照ガイド</span><span class="sxs-lookup"><span data-stu-id="2b4c0-387">Docs Markdown cheat sheet</span></span>](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [<span data-ttu-id="2b4c0-388">GitHub の Markdown の基本</span><span class="sxs-lookup"><span data-stu-id="2b4c0-388">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
- [<span data-ttu-id="2b4c0-389">Markdown ガイド</span><span class="sxs-lookup"><span data-stu-id="2b4c0-389">The Markdown Guide</span></span>](https://www.markdownguide.org/)
