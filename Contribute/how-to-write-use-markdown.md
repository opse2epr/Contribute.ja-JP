---
title: ドキュメントを記述するための Markdown の使用方法
description: この記事では、docs.microsoft.com の記事を記述するために使用される Markdown の基礎と参照情報について説明します。
ms.date: 07/13/2017
ms.openlocfilehash: ef75ffd59b75db5757822642f651d863906cf14c
ms.sourcegitcommit: 18c271ebec920bb976a4bc901f4ab8c1d36b02fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/19/2018
ms.locfileid: "53615837"
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="d26c7-103">ドキュメントを記述するための Markdown の使用方法</span><span class="sxs-lookup"><span data-stu-id="d26c7-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="d26c7-104">[docs.microsoft.com](http://docs.microsoft.com) の記事は [Markdown](https://daringfireball.net/projects/markdown/) という読みやすく、しかも簡単に学べる軽量マークアップ言語で記述されます。</span><span class="sxs-lookup"><span data-stu-id="d26c7-104">[Docs.microsoft.com](http://docs.microsoft.com) articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="d26c7-105">そのため、これは急速に業界標準になりました。</span><span class="sxs-lookup"><span data-stu-id="d26c7-105">Because of this, it has quickly become an industry standard.</span></span>

<span data-ttu-id="d26c7-106">Docs のコンテンツは GitHub に格納されるので、[GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/) と呼ばれる Markdown の上位セットを使用できます。GFM は一般的な書式要件のための追加機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="d26c7-106">Since Docs content is stored in GitHub, it can use a superset of Markdown called [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), which provides additional functionality for common formatting needs.</span></span> <span data-ttu-id="d26c7-107">さらに、Open Publishing Services (OPS) は Markdown パーサー Markdig を実装しています。</span><span class="sxs-lookup"><span data-stu-id="d26c7-107">Additionally, Open Publishing Services (OPS) implements Markdig Markdown Parser.</span></span> <span data-ttu-id="d26c7-108">Markdig は GFM との互換性が高く、Docs 固有の機能を実現するための機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="d26c7-108">Markdig is highly compatible with GFM, adding functionality to enable Docs-specific features.</span></span>

* <span data-ttu-id="d26c7-109">Markdig は高速で、強力で、CommonMark に準拠した、.NET 向けの拡張可能なマークダウン プロセッサーです。</span><span class="sxs-lookup"><span data-stu-id="d26c7-109">Markdig is a fast, powerful, CommonMark compliant, extensible Markdown processor for .NET.</span></span>
* https://github.com/lunet-io/markdig
* <span data-ttu-id="d26c7-110">優れたコミュニティ サポート</span><span class="sxs-lookup"><span data-stu-id="d26c7-110">Better community support</span></span>
* <span data-ttu-id="d26c7-111">優れた標準サポート</span><span class="sxs-lookup"><span data-stu-id="d26c7-111">Better standards support</span></span>

## <a name="markdown-basics"></a><span data-ttu-id="d26c7-112">Markdown の基本</span><span class="sxs-lookup"><span data-stu-id="d26c7-112">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="d26c7-113">見出し</span><span class="sxs-lookup"><span data-stu-id="d26c7-113">Headings</span></span>

<span data-ttu-id="d26c7-114">見出しを作成するには、ハッシュ記号 (#) を次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="d26c7-114">To create a heading, you use a hash mark (#), as follows:</span></span>

```markdown
# This is heading 1
## This is heading 2
### This is heading 3
#### This is heading 4
```

<span data-ttu-id="d26c7-115">見出しは atx 形式で作成してください。つまり、行の先頭で 1 つから 6 つまでのハッシュ文字 (#) を使用して見出しを示し、H1 から H6 までの HTML 見出しレベルに対応させます。</span><span class="sxs-lookup"><span data-stu-id="d26c7-115">Headings should be done using atx-style, that is, use 1-6 hash characters (#) at the start of the line to indicate a heading, corresponding to HTML headings levels H1 through H6.</span></span> <span data-ttu-id="d26c7-116">上の例では第 1 - 第 4 レベルのヘッダーが使用されています。</span><span class="sxs-lookup"><span data-stu-id="d26c7-116">Examples of first- through fourth-level headers are used above.</span></span>

<span data-ttu-id="d26c7-117">トピックの第 1 レベルの見出し (H1) は 1 つだけにする**必要があります**。これはページ上のタイトルとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="d26c7-117">There **must** be only one first-level heading (H1) in your topic, which will be displayed as the on-page title.</span></span>

<span data-ttu-id="d26c7-118">見出しが `#` 文字で終わる場合、タイトルが正しくレンダリングされるように終わりに `#` 文字を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d26c7-118">If your heading finishes with a `#` character, you need to add an extra `#` character in the end in order for the title to render correctly.</span></span> <span data-ttu-id="d26c7-119">たとえば、`# Async Programming in F# #` のようにします。</span><span class="sxs-lookup"><span data-stu-id="d26c7-119">For example, `# Async Programming in F# #`.</span></span>

<span data-ttu-id="d26c7-120">第 2 レベルの見出しによってページ上の TOC が生成されます。これはページ上のタイトルの下にある "この記事の内容" セクションに表示されます。</span><span class="sxs-lookup"><span data-stu-id="d26c7-120">Second-level headings will generate the on-page TOC that appears in the "In this article" section underneath the on-page title.</span></span>

### <a name="bold-and-italic-text"></a><span data-ttu-id="d26c7-121">太字や斜体のテキスト</span><span class="sxs-lookup"><span data-stu-id="d26c7-121">Bold and italic text</span></span>

<span data-ttu-id="d26c7-122">テキストの書式を**太字**に設定するには、テキストを二重のアスタリスクで囲みます。</span><span class="sxs-lookup"><span data-stu-id="d26c7-122">To format text as **bold**, you enclose it in two asterisks:</span></span>

```markdown
This text is **bold**.
```

<span data-ttu-id="d26c7-123">テキストの書式を*斜体*に設定するには、テキストを一重のアスタリスクで囲みます。</span><span class="sxs-lookup"><span data-stu-id="d26c7-123">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```markdown
This text is *italic*.
```

<span data-ttu-id="d26c7-124">テキストの書式を***太字と斜体***の両方に設定するには、テキストを三重のアスタリスクで囲みます。</span><span class="sxs-lookup"><span data-stu-id="d26c7-124">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```markdown
This is text is both ***bold and italic***.
```

### <a name="blockquotes"></a><span data-ttu-id="d26c7-125">ブロック引用</span><span class="sxs-lookup"><span data-stu-id="d26c7-125">Blockquotes</span></span>

<span data-ttu-id="d26c7-126">ブロック引用は `>` 文字で作成されます。</span><span class="sxs-lookup"><span data-stu-id="d26c7-126">Blockquotes are created using the `>` character:</span></span>

```markdown
> The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended. Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight. In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.
```

<span data-ttu-id="d26c7-127">先の例は次のようにレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="d26c7-127">The preceding example renders as follows:</span></span>

> <span data-ttu-id="d26c7-128">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span><span class="sxs-lookup"><span data-stu-id="d26c7-128">The drought had lasted now for ten million years, and the reign of the terrible lizards had long since ended.</span></span> <span data-ttu-id="d26c7-129">Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight.</span><span class="sxs-lookup"><span data-stu-id="d26c7-129">Here on the Equator, in the continent which would one day be known as Africa, the battle for existence had reached a new climax of ferocity, and the victor was not yet in sight.</span></span> <span data-ttu-id="d26c7-130">In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.</span><span class="sxs-lookup"><span data-stu-id="d26c7-130">In this barren and desiccated land, only the small or the swift or the fierce could flourish, or even hope to survive.</span></span>

### <a name="lists"></a><span data-ttu-id="d26c7-131">リスト</span><span class="sxs-lookup"><span data-stu-id="d26c7-131">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="d26c7-132">記号付きリスト</span><span class="sxs-lookup"><span data-stu-id="d26c7-132">Unordered list</span></span>

<span data-ttu-id="d26c7-133">記号付きリスト/箇条書きリストの書式を設定するには、アスタリスクまたはダッシュを使用できます。</span><span class="sxs-lookup"><span data-stu-id="d26c7-133">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="d26c7-134">たとえば、次の Markdown 書式は</span><span class="sxs-lookup"><span data-stu-id="d26c7-134">For example, the following Markdown:</span></span>

```markdown
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="d26c7-135">次のようにレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="d26c7-135">will be rendered as:</span></span>

- <span data-ttu-id="d26c7-136">List item 1</span><span class="sxs-lookup"><span data-stu-id="d26c7-136">List item 1</span></span>
- <span data-ttu-id="d26c7-137">List item 2</span><span class="sxs-lookup"><span data-stu-id="d26c7-137">List item 2</span></span>
- <span data-ttu-id="d26c7-138">List item 3</span><span class="sxs-lookup"><span data-stu-id="d26c7-138">List item 3</span></span>

<span data-ttu-id="d26c7-139">リストを別のリスト内にネストするには、子リスト アイテムをインデントします。</span><span class="sxs-lookup"><span data-stu-id="d26c7-139">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="d26c7-140">たとえば、次の Markdown 書式は</span><span class="sxs-lookup"><span data-stu-id="d26c7-140">For example, the following Markdown:</span></span>

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="d26c7-141">次のようにレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="d26c7-141">will be rendered as:</span></span>

- <span data-ttu-id="d26c7-142">List item 1</span><span class="sxs-lookup"><span data-stu-id="d26c7-142">List item 1</span></span>
  - <span data-ttu-id="d26c7-143">List item A</span><span class="sxs-lookup"><span data-stu-id="d26c7-143">List item A</span></span>
  - <span data-ttu-id="d26c7-144">List item B</span><span class="sxs-lookup"><span data-stu-id="d26c7-144">List item B</span></span>
- <span data-ttu-id="d26c7-145">List item 2</span><span class="sxs-lookup"><span data-stu-id="d26c7-145">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="d26c7-146">番号付きリスト</span><span class="sxs-lookup"><span data-stu-id="d26c7-146">Ordered list</span></span>

<span data-ttu-id="d26c7-147">番号付きリスト/段階的リストの書式を設定するには、対応する番号を使用します。</span><span class="sxs-lookup"><span data-stu-id="d26c7-147">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="d26c7-148">たとえば、次の Markdown 書式は</span><span class="sxs-lookup"><span data-stu-id="d26c7-148">For example, the following Markdown:</span></span>

```markdown
1. First instruction
1. Second instruction
1. Third instruction
```

<span data-ttu-id="d26c7-149">次のようにレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="d26c7-149">will be rendered as:</span></span>

1. <span data-ttu-id="d26c7-150">第 1 手順</span><span class="sxs-lookup"><span data-stu-id="d26c7-150">First instruction</span></span>
2. <span data-ttu-id="d26c7-151">第 2 手順</span><span class="sxs-lookup"><span data-stu-id="d26c7-151">Second instruction</span></span>
3. <span data-ttu-id="d26c7-152">第 3 手順</span><span class="sxs-lookup"><span data-stu-id="d26c7-152">Third instruction</span></span>

<span data-ttu-id="d26c7-153">リストを別のリスト内にネストするには、子リスト アイテムをインデントします。</span><span class="sxs-lookup"><span data-stu-id="d26c7-153">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="d26c7-154">たとえば、次の Markdown 書式は</span><span class="sxs-lookup"><span data-stu-id="d26c7-154">For example, the following Markdown:</span></span>

```markdown
1. First instruction
   1. Sub-instruction
   1. Sub-instruction
1. Second instruction
```

<span data-ttu-id="d26c7-155">次のようにレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="d26c7-155">will be rendered as:</span></span>

1. <span data-ttu-id="d26c7-156">第 1 手順</span><span class="sxs-lookup"><span data-stu-id="d26c7-156">First instruction</span></span>
   1. <span data-ttu-id="d26c7-157">下位手順</span><span class="sxs-lookup"><span data-stu-id="d26c7-157">Sub-instruction</span></span>
   2. <span data-ttu-id="d26c7-158">下位手順</span><span class="sxs-lookup"><span data-stu-id="d26c7-158">Sub-instruction</span></span>
2. <span data-ttu-id="d26c7-159">第 2 手順</span><span class="sxs-lookup"><span data-stu-id="d26c7-159">Second instruction</span></span>

<span data-ttu-id="d26c7-160">すべてのエントリに対して '1.' を</span><span class="sxs-lookup"><span data-stu-id="d26c7-160">Note that we use '1.'</span></span> <span data-ttu-id="d26c7-161">使用していることに注目してください。</span><span class="sxs-lookup"><span data-stu-id="d26c7-161">for all entries.</span></span> <span data-ttu-id="d26c7-162">後の更新で新しい手順が追加されるときや既存の手順が削除されるとき、見直しが簡単になります。</span><span class="sxs-lookup"><span data-stu-id="d26c7-162">It makes diffs easier to review when later updates include new steps or remove existing steps.</span></span>

### <a name="tables"></a><span data-ttu-id="d26c7-163">表</span><span class="sxs-lookup"><span data-stu-id="d26c7-163">Tables</span></span>

<span data-ttu-id="d26c7-164">Markdown の基本仕様には表が含まれていませんが、GFM が表をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="d26c7-164">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="d26c7-165">パイプ (|) 記号とハイフン記号 (-) を使用して表を作成できます。</span><span class="sxs-lookup"><span data-stu-id="d26c7-165">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="d26c7-166">ハイフンは各列のヘッダーを作成し、パイプは各列を区切ります。</span><span class="sxs-lookup"><span data-stu-id="d26c7-166">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="d26c7-167">表が正しくレンダリングされるように、表の前に空の行を 1 つ挿入してください。</span><span class="sxs-lookup"><span data-stu-id="d26c7-167">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="d26c7-168">たとえば、次の Markdown 書式は</span><span class="sxs-lookup"><span data-stu-id="d26c7-168">For example, the following Markdown:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="d26c7-169">次のようにレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="d26c7-169">will be rendered as:</span></span>

| <span data-ttu-id="d26c7-170">Fun</span><span class="sxs-lookup"><span data-stu-id="d26c7-170">Fun</span></span>                  | <span data-ttu-id="d26c7-171">With</span><span class="sxs-lookup"><span data-stu-id="d26c7-171">With</span></span>                 | <span data-ttu-id="d26c7-172">表</span><span class="sxs-lookup"><span data-stu-id="d26c7-172">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="d26c7-173">left-aligned column</span><span class="sxs-lookup"><span data-stu-id="d26c7-173">left-aligned column</span></span>  | <span data-ttu-id="d26c7-174">right-aligned column</span><span class="sxs-lookup"><span data-stu-id="d26c7-174">right-aligned column</span></span> | <span data-ttu-id="d26c7-175">centered column</span><span class="sxs-lookup"><span data-stu-id="d26c7-175">centered column</span></span> |
| <span data-ttu-id="d26c7-176">$100</span><span class="sxs-lookup"><span data-stu-id="d26c7-176">$100</span></span>                 | <span data-ttu-id="d26c7-177">$100</span><span class="sxs-lookup"><span data-stu-id="d26c7-177">$100</span></span>                 | <span data-ttu-id="d26c7-178">$100</span><span class="sxs-lookup"><span data-stu-id="d26c7-178">$100</span></span>            |
| <span data-ttu-id="d26c7-179">$10</span><span class="sxs-lookup"><span data-stu-id="d26c7-179">$10</span></span>                  | <span data-ttu-id="d26c7-180">$10</span><span class="sxs-lookup"><span data-stu-id="d26c7-180">$10</span></span>                  | <span data-ttu-id="d26c7-181">$10</span><span class="sxs-lookup"><span data-stu-id="d26c7-181">$10</span></span>             |
| <span data-ttu-id="d26c7-182">$1</span><span class="sxs-lookup"><span data-stu-id="d26c7-182">$1</span></span>                   | <span data-ttu-id="d26c7-183">$1</span><span class="sxs-lookup"><span data-stu-id="d26c7-183">$1</span></span>                   | <span data-ttu-id="d26c7-184">$1</span><span class="sxs-lookup"><span data-stu-id="d26c7-184">$1</span></span>              |

<span data-ttu-id="d26c7-185">表作成の詳細については、以下の情報源をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="d26c7-185">For more information on creating tables, see:</span></span>

- <span data-ttu-id="d26c7-186">横に長い表の書式設定に役立つ、Markdig の「[表を折り返す機能](#table-wrapping)」。</span><span class="sxs-lookup"><span data-stu-id="d26c7-186">The Markdig [table wrapping feature](#table-wrapping), which can help with formatting of wide tables.</span></span>
- <span data-ttu-id="d26c7-187">GitHub の「[Organizing information with tables (表を使用した情報の整理)](https://help.github.com/articles/organizing-information-with-tables/)」。</span><span class="sxs-lookup"><span data-stu-id="d26c7-187">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/).</span></span>
- <span data-ttu-id="d26c7-188">[Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) Web アプリ。</span><span class="sxs-lookup"><span data-stu-id="d26c7-188">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app.</span></span>
- <span data-ttu-id="d26c7-189">Adam Pritchard 氏の「[Markdown Cheatsheet (Markdown に関する簡易参照ガイド)](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables)」。</span><span class="sxs-lookup"><span data-stu-id="d26c7-189">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables).</span></span>
- <span data-ttu-id="d26c7-190">Michel Fortin 氏の [Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table) に関するページ。</span><span class="sxs-lookup"><span data-stu-id="d26c7-190">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table).</span></span>
- <span data-ttu-id="d26c7-191">[HTML テーブルからマークダウンへの変換](https://jmalarcon.github.io/markdowntables/)。</span><span class="sxs-lookup"><span data-stu-id="d26c7-191">[Convert HTML tables to Markdown](https://jmalarcon.github.io/markdowntables/).</span></span>

### <a name="links"></a><span data-ttu-id="d26c7-192">リンク</span><span class="sxs-lookup"><span data-stu-id="d26c7-192">Links</span></span>

<span data-ttu-id="d26c7-193">インライン リンクの Markdown 構文では、ハイパーリンクされるテキスト部分 `[link text]` の後に、リンク先 URL またはファイル名の部分 `(file-name.md)` が続きます。</span><span class="sxs-lookup"><span data-stu-id="d26c7-193">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="d26c7-194">リンクの詳細については、以下の情報源をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="d26c7-194">For more information on linking, see:</span></span>

- <span data-ttu-id="d26c7-195">Markdown のリンクの基本的なサポートについては、[Markdown の構文](https://daringfireball.net/projects/markdown/syntax#link)に関するセクション。</span><span class="sxs-lookup"><span data-stu-id="d26c7-195">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="d26c7-196">Markdig で提供されるその他のリンク構文の詳細については、このガイドの[リンク](how-to-write-links.md)に関するセクション。</span><span class="sxs-lookup"><span data-stu-id="d26c7-196">The [Links](how-to-write-links.md) section of this guide for details on the additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="d26c7-197">コード スニペット</span><span class="sxs-lookup"><span data-stu-id="d26c7-197">Code snippets</span></span>

<span data-ttu-id="d26c7-198">Markdown では、コード スニペットの配置方法として、文中へのインライン配置と、文と文の間への "フェンスされた" 個別ブロックとしての配置の両方がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="d26c7-198">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="d26c7-199">詳細については、以下の情報源をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="d26c7-199">For details, see:</span></span>

- <span data-ttu-id="d26c7-200">[Markdown のコード ブロックのネイティブ サポート](https://daringfireball.net/projects/markdown/syntax#precode)に関するセクション</span><span class="sxs-lookup"><span data-stu-id="d26c7-200">[Markdown's native support for code blocks](https://daringfireball.net/projects/markdown/syntax#precode)</span></span>
- <span data-ttu-id="d26c7-201">[GFM のコード フェンスと構文強調表示のサポート](https://help.github.com/articles/creating-and-highlighting-code-blocks/)に関するページ</span><span class="sxs-lookup"><span data-stu-id="d26c7-201">[GFM support for code fencing and syntax highlighting](https://help.github.com/articles/creating-and-highlighting-code-blocks/)</span></span>

<span data-ttu-id="d26c7-202">コード ブロックをフェンスすることで、コード スニペットの構文を強調表示することができます。</span><span class="sxs-lookup"><span data-stu-id="d26c7-202">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="d26c7-203">フェンスされたコード ブロックの一般的な書式は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="d26c7-203">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="d26c7-204">冒頭の 3 つのバッククォート (\`) 記号に続くエイリアスは、使用される構文強調表示を定義します。</span><span class="sxs-lookup"><span data-stu-id="d26c7-204">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="d26c7-205">以下は Docs コンテンツで一般的に使用されるプログラミング言語と、対応するラベルのリストです。</span><span class="sxs-lookup"><span data-stu-id="d26c7-205">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="d26c7-206">これらの言語は、フレンドリ名をサポートし、ほとんどに言語の強調表示機能があります。</span><span class="sxs-lookup"><span data-stu-id="d26c7-206">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="d26c7-207">名前</span><span class="sxs-lookup"><span data-stu-id="d26c7-207">Name</span></span>|<span data-ttu-id="d26c7-208">Markdown ラベル</span><span class="sxs-lookup"><span data-stu-id="d26c7-208">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="d26c7-209">.NET コンソール</span><span class="sxs-lookup"><span data-stu-id="d26c7-209">.NET Console</span></span>|<span data-ttu-id="d26c7-210">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="d26c7-210">dotnetcli</span></span>|
|<span data-ttu-id="d26c7-211">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="d26c7-211">ASP.NET (C#)</span></span>|<span data-ttu-id="d26c7-212">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="d26c7-212">aspx-csharp</span></span>|
|<span data-ttu-id="d26c7-213">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="d26c7-213">ASP.NET (VB)</span></span>|<span data-ttu-id="d26c7-214">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="d26c7-214">aspx-vb</span></span>|
|<span data-ttu-id="d26c7-215">AzCopy</span><span class="sxs-lookup"><span data-stu-id="d26c7-215">AzCopy</span></span>|<span data-ttu-id="d26c7-216">azcopy</span><span class="sxs-lookup"><span data-stu-id="d26c7-216">azcopy</span></span>|
|<span data-ttu-id="d26c7-217">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="d26c7-217">Azure CLI</span></span>|<span data-ttu-id="d26c7-218">azurecli</span><span class="sxs-lookup"><span data-stu-id="d26c7-218">azurecli</span></span>|
|<span data-ttu-id="d26c7-219">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="d26c7-219">Azure PowerShell</span></span>|<span data-ttu-id="d26c7-220">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="d26c7-220">azurepowershell</span></span>|
|<span data-ttu-id="d26c7-221">C++</span><span class="sxs-lookup"><span data-stu-id="d26c7-221">C++</span></span>|<span data-ttu-id="d26c7-222">cpp</span><span class="sxs-lookup"><span data-stu-id="d26c7-222">cpp</span></span>|
|<span data-ttu-id="d26c7-223">C++/CX</span><span class="sxs-lookup"><span data-stu-id="d26c7-223">C++/CX</span></span>|<span data-ttu-id="d26c7-224">cppcx</span><span class="sxs-lookup"><span data-stu-id="d26c7-224">cppcx</span></span>|
|<span data-ttu-id="d26c7-225">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="d26c7-225">C++/WinRT</span></span>|<span data-ttu-id="d26c7-226">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="d26c7-226">cppwinrt</span></span>|
|<span data-ttu-id="d26c7-227">C#</span><span class="sxs-lookup"><span data-stu-id="d26c7-227">C#</span></span>|<span data-ttu-id="d26c7-228">csharp</span><span class="sxs-lookup"><span data-stu-id="d26c7-228">csharp</span></span>|
|<span data-ttu-id="d26c7-229">ブラウザーの C#</span><span class="sxs-lookup"><span data-stu-id="d26c7-229">C# in browser</span></span>|<span data-ttu-id="d26c7-230">csharp-interactive</span><span class="sxs-lookup"><span data-stu-id="d26c7-230">csharp-interactive</span></span>|
|<span data-ttu-id="d26c7-231">コンソール</span><span class="sxs-lookup"><span data-stu-id="d26c7-231">Console</span></span>|<span data-ttu-id="d26c7-232">console</span><span class="sxs-lookup"><span data-stu-id="d26c7-232">console</span></span>|
|<span data-ttu-id="d26c7-233">CSHTML</span><span class="sxs-lookup"><span data-stu-id="d26c7-233">CSHTML</span></span>|<span data-ttu-id="d26c7-234">cshtml</span><span class="sxs-lookup"><span data-stu-id="d26c7-234">cshtml</span></span>|
|<span data-ttu-id="d26c7-235">DAX</span><span class="sxs-lookup"><span data-stu-id="d26c7-235">DAX</span></span>|<span data-ttu-id="d26c7-236">dax</span><span class="sxs-lookup"><span data-stu-id="d26c7-236">dax</span></span>|
|<span data-ttu-id="d26c7-237">F#</span><span class="sxs-lookup"><span data-stu-id="d26c7-237">F#</span></span>|<span data-ttu-id="d26c7-238">fsharp</span><span class="sxs-lookup"><span data-stu-id="d26c7-238">fsharp</span></span>|
|<span data-ttu-id="d26c7-239">Go</span><span class="sxs-lookup"><span data-stu-id="d26c7-239">Go</span></span>|<span data-ttu-id="d26c7-240">go</span><span class="sxs-lookup"><span data-stu-id="d26c7-240">go</span></span>|
|<span data-ttu-id="d26c7-241">HTML</span><span class="sxs-lookup"><span data-stu-id="d26c7-241">HTML</span></span>|<span data-ttu-id="d26c7-242">html</span><span class="sxs-lookup"><span data-stu-id="d26c7-242">html</span></span>|
|<span data-ttu-id="d26c7-243">HTTP</span><span class="sxs-lookup"><span data-stu-id="d26c7-243">HTTP</span></span>|<span data-ttu-id="d26c7-244">http</span><span class="sxs-lookup"><span data-stu-id="d26c7-244">http</span></span>|
|<span data-ttu-id="d26c7-245">Java</span><span class="sxs-lookup"><span data-stu-id="d26c7-245">Java</span></span>|<span data-ttu-id="d26c7-246">java</span><span class="sxs-lookup"><span data-stu-id="d26c7-246">java</span></span>|
|<span data-ttu-id="d26c7-247">JavaScript</span><span class="sxs-lookup"><span data-stu-id="d26c7-247">JavaScript</span></span>|<span data-ttu-id="d26c7-248">javascript</span><span class="sxs-lookup"><span data-stu-id="d26c7-248">javascript</span></span>|
|<span data-ttu-id="d26c7-249">JSON</span><span class="sxs-lookup"><span data-stu-id="d26c7-249">JSON</span></span>|<span data-ttu-id="d26c7-250">json</span><span class="sxs-lookup"><span data-stu-id="d26c7-250">json</span></span>|
|<span data-ttu-id="d26c7-251">Markdown</span><span class="sxs-lookup"><span data-stu-id="d26c7-251">Markdown</span></span>|<span data-ttu-id="d26c7-252">md</span><span class="sxs-lookup"><span data-stu-id="d26c7-252">md</span></span>|
|<span data-ttu-id="d26c7-253">NodeJS</span><span class="sxs-lookup"><span data-stu-id="d26c7-253">NodeJS</span></span>|<span data-ttu-id="d26c7-254">nodejs</span><span class="sxs-lookup"><span data-stu-id="d26c7-254">nodejs</span></span>|
|<span data-ttu-id="d26c7-255">Objective-C</span><span class="sxs-lookup"><span data-stu-id="d26c7-255">Objective-C</span></span>|<span data-ttu-id="d26c7-256">objc</span><span class="sxs-lookup"><span data-stu-id="d26c7-256">objc</span></span>|
|<span data-ttu-id="d26c7-257">OData</span><span class="sxs-lookup"><span data-stu-id="d26c7-257">OData</span></span>|<span data-ttu-id="d26c7-258">odata</span><span class="sxs-lookup"><span data-stu-id="d26c7-258">odata</span></span>|
|<span data-ttu-id="d26c7-259">PHP</span><span class="sxs-lookup"><span data-stu-id="d26c7-259">PHP</span></span>|<span data-ttu-id="d26c7-260">php</span><span class="sxs-lookup"><span data-stu-id="d26c7-260">php</span></span>|
|<span data-ttu-id="d26c7-261">PowerApps (ドット小数点区切り記号)</span><span class="sxs-lookup"><span data-stu-id="d26c7-261">PowerApps (dot decimal separator)</span></span>|<span data-ttu-id="d26c7-262">powerapps-dot</span><span class="sxs-lookup"><span data-stu-id="d26c7-262">powerapps-dot</span></span>|
|<span data-ttu-id="d26c7-263">PowerApps (コンマ小数点区切り記号)</span><span class="sxs-lookup"><span data-stu-id="d26c7-263">PowerApps (comma decimal separator)</span></span>|<span data-ttu-id="d26c7-264">powerapps-comma</span><span class="sxs-lookup"><span data-stu-id="d26c7-264">powerapps-comma</span></span>|
|<span data-ttu-id="d26c7-265">PowerShell</span><span class="sxs-lookup"><span data-stu-id="d26c7-265">PowerShell</span></span>|<span data-ttu-id="d26c7-266">powershell</span><span class="sxs-lookup"><span data-stu-id="d26c7-266">powershell</span></span>|
|<span data-ttu-id="d26c7-267">Python</span><span class="sxs-lookup"><span data-stu-id="d26c7-267">Python</span></span>|<span data-ttu-id="d26c7-268">python</span><span class="sxs-lookup"><span data-stu-id="d26c7-268">python</span></span>|
|<span data-ttu-id="d26c7-269">Q#</span><span class="sxs-lookup"><span data-stu-id="d26c7-269">Q#</span></span>|<span data-ttu-id="d26c7-270">qsharp</span><span class="sxs-lookup"><span data-stu-id="d26c7-270">qsharp</span></span>|
|<span data-ttu-id="d26c7-271">R</span><span class="sxs-lookup"><span data-stu-id="d26c7-271">R</span></span>|<span data-ttu-id="d26c7-272">r</span><span class="sxs-lookup"><span data-stu-id="d26c7-272">r</span></span>|
|<span data-ttu-id="d26c7-273">Ruby</span><span class="sxs-lookup"><span data-stu-id="d26c7-273">Ruby</span></span>|<span data-ttu-id="d26c7-274">ruby</span><span class="sxs-lookup"><span data-stu-id="d26c7-274">ruby</span></span>|
|<span data-ttu-id="d26c7-275">SQL</span><span class="sxs-lookup"><span data-stu-id="d26c7-275">SQL</span></span>|<span data-ttu-id="d26c7-276">sql</span><span class="sxs-lookup"><span data-stu-id="d26c7-276">sql</span></span>|
|<span data-ttu-id="d26c7-277">Swift</span><span class="sxs-lookup"><span data-stu-id="d26c7-277">Swift</span></span>|<span data-ttu-id="d26c7-278">swift</span><span class="sxs-lookup"><span data-stu-id="d26c7-278">swift</span></span>|
|<span data-ttu-id="d26c7-279">TypeScript</span><span class="sxs-lookup"><span data-stu-id="d26c7-279">TypeScript</span></span>|<span data-ttu-id="d26c7-280">typescript</span><span class="sxs-lookup"><span data-stu-id="d26c7-280">typescript</span></span>|
|<span data-ttu-id="d26c7-281">VB</span><span class="sxs-lookup"><span data-stu-id="d26c7-281">VB</span></span>|<span data-ttu-id="d26c7-282">vb</span><span class="sxs-lookup"><span data-stu-id="d26c7-282">vb</span></span>|
|<span data-ttu-id="d26c7-283">VSTS CLI</span><span class="sxs-lookup"><span data-stu-id="d26c7-283">VSTS CLI</span></span>|<span data-ttu-id="d26c7-284">vstscli</span><span class="sxs-lookup"><span data-stu-id="d26c7-284">vstscli</span></span>|
|<span data-ttu-id="d26c7-285">XAML</span><span class="sxs-lookup"><span data-stu-id="d26c7-285">XAML</span></span>|<span data-ttu-id="d26c7-286">xaml</span><span class="sxs-lookup"><span data-stu-id="d26c7-286">xaml</span></span>|
|<span data-ttu-id="d26c7-287">XML</span><span class="sxs-lookup"><span data-stu-id="d26c7-287">XML</span></span>|<span data-ttu-id="d26c7-288">xml</span><span class="sxs-lookup"><span data-stu-id="d26c7-288">xml</span></span>|

<span data-ttu-id="d26c7-289">`csharp-interactive` 名によって C# 言語と、ブラウザーからサンプルを実行する機能が指定されます。</span><span class="sxs-lookup"><span data-stu-id="d26c7-289">The `csharp-interactive` name specifies the C# language, and the ability to run the samples from the browser.</span></span> <span data-ttu-id="d26c7-290">このようなスニペットは Docker コンテナーでコンパイルされ、実行されます。そのプログラム実行の結果はユーザーのブラウザー ウィンドウに表示されます。</span><span class="sxs-lookup"><span data-stu-id="d26c7-290">These snippets are compiled and executed in a Docker container, and the results of that program execution are displayed in the user's browser window.</span></span>

#### <a name="example-c"></a><span data-ttu-id="d26c7-291">例:C\#</span><span class="sxs-lookup"><span data-stu-id="d26c7-291">Example: C\#</span></span>

<span data-ttu-id="d26c7-292">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="d26c7-292">__Markdown__</span></span>

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

<span data-ttu-id="d26c7-293">__レンダー__</span><span class="sxs-lookup"><span data-stu-id="d26c7-293">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="d26c7-294">例:SQL</span><span class="sxs-lookup"><span data-stu-id="d26c7-294">Example: SQL</span></span>

<span data-ttu-id="d26c7-295">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="d26c7-295">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="d26c7-296">__レンダー__</span><span class="sxs-lookup"><span data-stu-id="d26c7-296">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a><span data-ttu-id="d26c7-297">OPS による Markdown のカスタム拡張機能</span><span class="sxs-lookup"><span data-stu-id="d26c7-297">OPS custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="d26c7-298">Open Publishing Services (OPS) は GitHub Flavored Markdown (GFM) との互換性が非常に高い Markdown パーサー Markdig を実装しています。</span><span class="sxs-lookup"><span data-stu-id="d26c7-298">Open Publishing Services (OPS) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="d26c7-299">Markdig は Markdown 拡張機能を介していくつかの機能を追加しています。</span><span class="sxs-lookup"><span data-stu-id="d26c7-299">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="d26c7-300">そのため、完全版の「OPS Authoring Guide」 (OPS オーサリング ガイド) の一部の記事は、参考のためにこのガイドに含まれています </span><span class="sxs-lookup"><span data-stu-id="d26c7-300">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="d26c7-301">(たとえば、目次の「Markdig and Markdown extensions」(Markdig と Markdown の拡張機能) と「Code snippets」(コード スニペット) をご覧ください)。</span><span class="sxs-lookup"><span data-stu-id="d26c7-301">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="d26c7-302">Docs 記事では、段落、リンク、リスト、見出しなど、ほとんどの書式設定に GFM が使用されます。</span><span class="sxs-lookup"><span data-stu-id="d26c7-302">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="d26c7-303">記事の高度な書式設定には、次のような Markdig 機能を使用できます。</span><span class="sxs-lookup"><span data-stu-id="d26c7-303">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="d26c7-304">注ブロック</span><span class="sxs-lookup"><span data-stu-id="d26c7-304">Note blocks</span></span>
- <span data-ttu-id="d26c7-305">インクルード ファイル</span><span class="sxs-lookup"><span data-stu-id="d26c7-305">Include files</span></span>
- <span data-ttu-id="d26c7-306">セレクター</span><span class="sxs-lookup"><span data-stu-id="d26c7-306">Selectors</span></span>
- <span data-ttu-id="d26c7-307">埋め込みビデオ</span><span class="sxs-lookup"><span data-stu-id="d26c7-307">Embedded videos</span></span>
- <span data-ttu-id="d26c7-308">コード スニペット/サンプル</span><span class="sxs-lookup"><span data-stu-id="d26c7-308">Code snippets/samples</span></span>

<span data-ttu-id="d26c7-309">完全なリストについては、目次の「Markdig and Markdown extensions」(Markdig と Markdown の拡張機能) と「Code snippets」(コード スニペット) をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="d26c7-309">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="d26c7-310">注ブロック</span><span class="sxs-lookup"><span data-stu-id="d26c7-310">Note blocks</span></span>

<span data-ttu-id="d26c7-311">特定の内容に注目を集めるには、4 つのタイプの注ブロックから選択できます。</span><span class="sxs-lookup"><span data-stu-id="d26c7-311">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="d26c7-312">NOTE (注意)</span><span class="sxs-lookup"><span data-stu-id="d26c7-312">NOTE</span></span>
- <span data-ttu-id="d26c7-313">WARNING (警告)</span><span class="sxs-lookup"><span data-stu-id="d26c7-313">WARNING</span></span>
- <span data-ttu-id="d26c7-314">TIP (ヒント)</span><span class="sxs-lookup"><span data-stu-id="d26c7-314">TIP</span></span>
- <span data-ttu-id="d26c7-315">IMPORTANT (重要)</span><span class="sxs-lookup"><span data-stu-id="d26c7-315">IMPORTANT</span></span>

<span data-ttu-id="d26c7-316">注ブロックによって文章がわかりにくくなることがあるので、概して注ブロックは控えめに使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d26c7-316">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="d26c7-317">注ブロックでもコード ブロック、イメージ、リスト、およびリンクがサポートされますが、注ブロックを簡潔でわかりやすくするように心掛けてください。</span><span class="sxs-lookup"><span data-stu-id="d26c7-317">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

<span data-ttu-id="d26c7-318">例:</span><span class="sxs-lookup"><span data-stu-id="d26c7-318">Examples:</span></span>

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

<span data-ttu-id="d26c7-319">これは次のようにレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="d26c7-319">These render as follows:</span></span>

> [!NOTE]
> <span data-ttu-id="d26c7-320">This is a NOTE</span><span class="sxs-lookup"><span data-stu-id="d26c7-320">This is a NOTE</span></span>

> [!WARNING]
> <span data-ttu-id="d26c7-321">This is a WARNING</span><span class="sxs-lookup"><span data-stu-id="d26c7-321">This is a WARNING</span></span>

> [!TIP]
> <span data-ttu-id="d26c7-322">This is a TIP</span><span class="sxs-lookup"><span data-stu-id="d26c7-322">This is a TIP</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d26c7-323">This is IMPORTANT</span><span class="sxs-lookup"><span data-stu-id="d26c7-323">This is IMPORTANT</span></span>

### <a name="include-files"></a><span data-ttu-id="d26c7-324">インクルード ファイル</span><span class="sxs-lookup"><span data-stu-id="d26c7-324">Include files</span></span>

<span data-ttu-id="d26c7-325">再利用可能なテキスト ファイルまたはイメージ ファイルを記事ファイルにインクルードする必要がある場合は、Markdig のファイル インクルード機能を使用して "インクルード" ファイルを参照できます。</span><span class="sxs-lookup"><span data-stu-id="d26c7-325">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="d26c7-326">この機能は、ビルド時に特定のファイルを記事ファイルにインクルードするように OPS に指示します。これにより、その指定されたファイルは公開記事に含まれるようになります。</span><span class="sxs-lookup"><span data-stu-id="d26c7-326">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="d26c7-327">コンテンツの再利用に役立つインクルード参照には、次の 3 種類があります。</span><span class="sxs-lookup"><span data-stu-id="d26c7-327">Three types of include references are available to help you reuse content:</span></span>

- <span data-ttu-id="d26c7-328">インライン: 一般的なテキスト スニペットを別の文中にインラインで再利用できます。</span><span class="sxs-lookup"><span data-stu-id="d26c7-328">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="d26c7-329">ブロック: Markdown ファイル全体をブロックとして再利用し、記事のセクション内にネストできます。</span><span class="sxs-lookup"><span data-stu-id="d26c7-329">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="d26c7-330">イメージ: これは Docs に実装されている標準的なイメージ インクルードの方法です。</span><span class="sxs-lookup"><span data-stu-id="d26c7-330">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="d26c7-331">インラインまたはブロックによるインクルード ファイルはシンプルな Markdown (.md) ファイルにすぎません。</span><span class="sxs-lookup"><span data-stu-id="d26c7-331">An inline or block include file is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="d26c7-332">これにはあらゆる有効な Markdown を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="d26c7-332">It can contain any valid Markdown.</span></span> <span data-ttu-id="d26c7-333">すべてのインクルード Markdown ファイルは、リポジトリのルートにある[共通の `/includes` サブディレクトリ](git-github-fundamentals.md#includes-subdirectory)に配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d26c7-333">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="d26c7-334">記事が公開されると、インクルードされたファイルはその記事にシームレスに統合されます。</span><span class="sxs-lookup"><span data-stu-id="d26c7-334">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="d26c7-335">インクルード ファイルに関する要件と考慮事項を次に示します。</span><span class="sxs-lookup"><span data-stu-id="d26c7-335">Here are requirements and considerations for include files:</span></span>

- <span data-ttu-id="d26c7-336">複数の記事に同じテキストを表示する必要があるときは必ず、インクルード ファイルを使用してください。</span><span class="sxs-lookup"><span data-stu-id="d26c7-336">Use an include file whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="d26c7-337">ブロックによるインクルード参照は、1 つまたは 2 つの段落、共通の手順、共通のセクションといった分量の多いコンテンツに使用してください。</span><span class="sxs-lookup"><span data-stu-id="d26c7-337">Use a block include reference for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="d26c7-338">1 つの文よりも小さい場合には、使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="d26c7-338">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="d26c7-339">インクルード参照は Markdig 拡張機能に依存するため、GitHub でレンダリングされた記事内でインクルード参照はレンダリングされません。</span><span class="sxs-lookup"><span data-stu-id="d26c7-339">Include references won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="d26c7-340">公開後にのみレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="d26c7-340">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="d26c7-341">インクルード ファイル内のすべてのテキストが、インクルード ファイルを参照する記事内の先行テキストまたは後続テキストに依存しない完全な文または語句で記述されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d26c7-341">Ensure that all the text in an include file is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include file.</span></span> <span data-ttu-id="d26c7-342">このガイダンスを無視すると、ローカライズされたエクスペリエンスを乱す翻訳不可能な文字列が記事内に発生します。</span><span class="sxs-lookup"><span data-stu-id="d26c7-342">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="d26c7-343">インクルード参照をほかのインクルード ファイル内に埋め込まないでください。</span><span class="sxs-lookup"><span data-stu-id="d26c7-343">Don't embed include references within other include files.</span></span> <span data-ttu-id="d26c7-344">それはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="d26c7-344">They are not supported.</span></span>
- <span data-ttu-id="d26c7-345">メディア ファイルは、インクルードのサブディレクトリ内にあるメディア フォルダーに配置する必要があります。たとえば、`<repo>`/includes/media フォルダーです。</span><span class="sxs-lookup"><span data-stu-id="d26c7-345">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="d26c7-346">メディア ディレクトリのルートにはイメージを配置しないでください。</span><span class="sxs-lookup"><span data-stu-id="d26c7-346">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="d26c7-347">インクルード ファイルにイメージが含まれていない場合、対応するメディア ディレクトリは不要です。</span><span class="sxs-lookup"><span data-stu-id="d26c7-347">If the include file does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="d26c7-348">通常の記事と同様に、インクルード ファイル間でメディアを共有しないでください。</span><span class="sxs-lookup"><span data-stu-id="d26c7-348">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="d26c7-349">インクルード ファイルおよび記事ごとに、一意の名前を持つ個別ファイルを使用してください。</span><span class="sxs-lookup"><span data-stu-id="d26c7-349">Use a separate file with a unique name for each include file and article.</span></span> <span data-ttu-id="d26c7-350">メディア ファイルは、インクルード ファイルに関連付けられたメディア フォルダーに格納してください。</span><span class="sxs-lookup"><span data-stu-id="d26c7-350">Store the media file in the media folder that's associated with the include file.</span></span>
- <span data-ttu-id="d26c7-351">記事の唯一のコンテンツとしてインクルード ファイルを使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="d26c7-351">Don't use an include file as the only content of an article.</span></span>  <span data-ttu-id="d26c7-352">インクルード ファイルの目的は、記事の残りの部分にあるコンテンツを補完することです。</span><span class="sxs-lookup"><span data-stu-id="d26c7-352">Include files are meant to be supplemental to the content in the rest of the article.</span></span>

<span data-ttu-id="d26c7-353">例:</span><span class="sxs-lookup"><span data-stu-id="d26c7-353">Example:</span></span>

```markdown
[!INCLUDE[sample include file](../includes/sampleinclude.md)]
```

### <a name="selectors"></a><span data-ttu-id="d26c7-354">セレクター</span><span class="sxs-lookup"><span data-stu-id="d26c7-354">Selectors</span></span>

<span data-ttu-id="d26c7-355">同じ技術記事の複数のバージョンを記述するときには、複数のテクノロジまたはプラットフォームの実装の違いに対応するために、セレクターを使用します。</span><span class="sxs-lookup"><span data-stu-id="d26c7-355">Use selectors in technical articles when you author multiple flavors of the same article, to  address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="d26c7-356">通常、これが最も当てはまるのは、Microsoft の開発者向けのモバイル プラットフォームのコンテンツです。</span><span class="sxs-lookup"><span data-stu-id="d26c7-356">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="d26c7-357">現在 Markdig にはシングル セレクターとマルチ セレクターという 2 つのタイプのセレクターがあります。</span><span class="sxs-lookup"><span data-stu-id="d26c7-357">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="d26c7-358">選択範囲内の各記事に配置されるセレクター Markdown は同じであるため、ご自分の記事に対するセレクターをインクルード ファイルに配置することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="d26c7-358">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include file.</span></span> <span data-ttu-id="d26c7-359">その上で、同じセレクターを使用するご自分のすべての記事内で、そのインクルード ファイルを参照できます。</span><span class="sxs-lookup"><span data-stu-id="d26c7-359">Then you can reference that include file in all your articles that use the same selector.</span></span>

<span data-ttu-id="d26c7-360">次にセレクターの例を示します。</span><span class="sxs-lookup"><span data-stu-id="d26c7-360">The following shows an example selector:</span></span>

```markdown
> [!div class="op_single_selector"]
- [macOS](../docs/core/tutorials/using-on-macos.md)
- [Windows](../docs/core/tutorials/with-visual-studio.md)
```

<span data-ttu-id="d26c7-361">[Azure ドキュメント](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic)で、実際に使われているセレクターの例を確認できます。</span><span class="sxs-lookup"><span data-stu-id="d26c7-361">You can see an example of selectors in action at the [Azure docs](https://docs.microsoft.com/azure/expressroute/expressroute-howto-circuit-classic).</span></span>

### <a name="code-include-references"></a><span data-ttu-id="d26c7-362">コードのインクルード参照</span><span class="sxs-lookup"><span data-stu-id="d26c7-362">Code include references</span></span>

<span data-ttu-id="d26c7-363">Markdig では、コード スニペット拡張機能を使用した記事へのコードの高度なインクルードがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="d26c7-363">Markdig supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="d26c7-364">プログラミング言語の選択や構文の色分けといった GFM 機能に基づく高度なレンダリングに加えて、次のような便利な機能を使用できます。</span><span class="sxs-lookup"><span data-stu-id="d26c7-364">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="d26c7-365">外部リポジトリから集められたコード サンプル/スニペットのインクルード。</span><span class="sxs-lookup"><span data-stu-id="d26c7-365">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="d26c7-366">さまざまな言語でのさまざまなバージョンのコード サンプルをタブに表示する UI。</span><span class="sxs-lookup"><span data-stu-id="d26c7-366">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="d26c7-367">問題の発見 + トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="d26c7-367">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="d26c7-368">alt テキスト</span><span class="sxs-lookup"><span data-stu-id="d26c7-368">Alt text</span></span>

<span data-ttu-id="d26c7-369">アンダー スコアを含む alt テキストは正しくレンダリングされません。</span><span class="sxs-lookup"><span data-stu-id="d26c7-369">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="d26c7-370">たとえば、次のテキストを使用するのではなく、</span><span class="sxs-lookup"><span data-stu-id="d26c7-370">For example, instead of using this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="d26c7-371">次のようにアンダー スコアをエスケープします。</span><span class="sxs-lookup"><span data-stu-id="d26c7-371">Escape the underscores like this:</span></span>

```markdown
![ADextension\_2FA\_Configure\_Step4](./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="d26c7-372">アポストロフィと引用符</span><span class="sxs-lookup"><span data-stu-id="d26c7-372">Apostrophes and quotation marks</span></span>

<span data-ttu-id="d26c7-373">Word から Markdown エディターにコピーしたテキストに、"スマート" (カールした) アポストロフィまたは引用符が含まれていることがあります。</span><span class="sxs-lookup"><span data-stu-id="d26c7-373">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="d26c7-374">これらを標準的なアポストロフィや引用符にエンコードまたは変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d26c7-374">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="d26c7-375">そうしないと、ファイルが公開されたときに次のように表示されます: Itâ€™s</span><span class="sxs-lookup"><span data-stu-id="d26c7-375">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="d26c7-376">これらの "スマート" バージョンの記述記号のエンコーディングは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="d26c7-376">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="d26c7-377">左 (始め) 二重引用符: `&#8220;`</span><span class="sxs-lookup"><span data-stu-id="d26c7-377">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="d26c7-378">右 (終わり) 二重引用符: `&#8221;`</span><span class="sxs-lookup"><span data-stu-id="d26c7-378">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="d26c7-379">右 (終わり) 一重引用符またはアポストロフィ: `&#8217;`</span><span class="sxs-lookup"><span data-stu-id="d26c7-379">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="d26c7-380">左 (始め) 一重引用符 (あまり使用されません): `&#8216;`</span><span class="sxs-lookup"><span data-stu-id="d26c7-380">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="d26c7-381">山かっこ</span><span class="sxs-lookup"><span data-stu-id="d26c7-381">Angle brackets</span></span>

<span data-ttu-id="d26c7-382">プレースホルダーを示す目的では一般的に山括弧が使用されます。</span><span class="sxs-lookup"><span data-stu-id="d26c7-382">It is common to use angle brackets to denote a placeholder.</span></span> <span data-ttu-id="d26c7-383">これを (コードではなく) テキストで行うときは、山括弧で囲む必要があります。</span><span class="sxs-lookup"><span data-stu-id="d26c7-383">When you do this in text (not code), you must encode the angle brackets.</span></span> <span data-ttu-id="d26c7-384">そうしないと、それらのテキストは Markdown によって HTML タグとして認識されます。</span><span class="sxs-lookup"><span data-stu-id="d26c7-384">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="d26c7-385">たとえば、`<script name>` を `&lt;script name&gt;` にエンコードしてください。</span><span class="sxs-lookup"><span data-stu-id="d26c7-385">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="see-also"></a><span data-ttu-id="d26c7-386">関連項目:</span><span class="sxs-lookup"><span data-stu-id="d26c7-386">See also:</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="d26c7-387">Markdown に関するリソース</span><span class="sxs-lookup"><span data-stu-id="d26c7-387">Markdown resources</span></span>

- [<span data-ttu-id="d26c7-388">Markdown 入門</span><span class="sxs-lookup"><span data-stu-id="d26c7-388">Introduction to Markdown</span></span>](https://daringfireball.net/projects/markdown/syntax)
- [<span data-ttu-id="d26c7-389">Docs の Markdown に関する簡易参照ガイド</span><span class="sxs-lookup"><span data-stu-id="d26c7-389">Docs Markdown cheat sheet</span></span>](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [<span data-ttu-id="d26c7-390">GitHub の Markdown の基本</span><span class="sxs-lookup"><span data-stu-id="d26c7-390">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
- [<span data-ttu-id="d26c7-391">Markdown ガイド</span><span class="sxs-lookup"><span data-stu-id="d26c7-391">The Markdown Guide</span></span>](https://www.markdownguide.org/)
