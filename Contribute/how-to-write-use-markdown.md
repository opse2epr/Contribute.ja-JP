---
title: ドキュメントを記述するための Markdown の使用方法
description: この記事では、docs.microsoft.com の記事を記述するために使用される Markdown の基礎と参照情報について説明します。
ms.date: 07/13/2017
ms.openlocfilehash: dca1ccba2ae4ebd08b6039f5d780e7a7ac92e79f
ms.sourcegitcommit: 92aef5ea8bdd692c5c393d5c8f99b9e4f672ef2b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/19/2018
ms.locfileid: "36238968"
---
# <a name="how-to-use-markdown-for-writing-docs"></a><span data-ttu-id="5d84b-103">ドキュメントを記述するための Markdown の使用方法</span><span class="sxs-lookup"><span data-stu-id="5d84b-103">How to use Markdown for writing Docs</span></span>

<span data-ttu-id="5d84b-104">docs.microsoft.com の記事は [Markdown](https://daringfireball.net/projects/markdown/) という読みやすく、しかも簡単に学べる軽量マークアップ言語で記述されます。</span><span class="sxs-lookup"><span data-stu-id="5d84b-104">Docs.microsoft.com articles are written in a lightweight markup language called [Markdown](https://daringfireball.net/projects/markdown/), which is both easy to read and easy to learn.</span></span> <span data-ttu-id="5d84b-105">そのため、これは急速に業界標準になりました。</span><span class="sxs-lookup"><span data-stu-id="5d84b-105">Because of this, it has quickly become an industry standard.</span></span>

<span data-ttu-id="5d84b-106">Docs のコンテンツは GitHub に格納されるので、[GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/) と呼ばれる Markdown の上位セットを使用できます。GFM は一般的な書式要件のための追加機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="5d84b-106">Because Docs content is stored in GitHub, it can use a superset of Markdown called [GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/), which provides additional functionality for common formatting needs.</span></span> <span data-ttu-id="5d84b-107">さらに、Open Publishing Services (OPS) は Markdown パーサー Markdig を実装しています。</span><span class="sxs-lookup"><span data-stu-id="5d84b-107">Additionally, Open Publishing Services (OPS) implements Markdig Markdown Parser.</span></span> <span data-ttu-id="5d84b-108">Markdig は GitHub Flavored Markdown (GFM) との互換性が高く、Docs 固有の機能を実現するための機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="5d84b-108">Markdig is highly compatible with GitHub Flavored Markdown (GFM), adding functionality to enable Docs-specific features.</span></span>

* <span data-ttu-id="5d84b-109">Markdig は高速で、強力で、CommonMark に準拠した、.NET 向けの拡張可能なマークダウン プロセッサーです。</span><span class="sxs-lookup"><span data-stu-id="5d84b-109">Markdig is a fast, powerful, CommonMark compliant, extensible Markdown processor for .NET.</span></span>
* https://github.com/lunet-io/markdig
* <span data-ttu-id="5d84b-110">優れたコミュニティ サポート</span><span class="sxs-lookup"><span data-stu-id="5d84b-110">Better community support</span></span>
* <span data-ttu-id="5d84b-111">優れた標準サポート</span><span class="sxs-lookup"><span data-stu-id="5d84b-111">Better standards support</span></span>

## <a name="markdown-basics"></a><span data-ttu-id="5d84b-112">Markdown の基本</span><span class="sxs-lookup"><span data-stu-id="5d84b-112">Markdown basics</span></span>

### <a name="headings"></a><span data-ttu-id="5d84b-113">見出し</span><span class="sxs-lookup"><span data-stu-id="5d84b-113">Headings</span></span>

<span data-ttu-id="5d84b-114">見出しを作成するには、ハッシュ記号 (#) を次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="5d84b-114">To create a heading, you use a hash mark (#), as follows:</span></span>

```markdown
    # This is heading 1
    ## This is heading 2
    ### This is heading 3
    #### This is heading 4
```

### <a name="bold-and-italic-text"></a><span data-ttu-id="5d84b-115">太字や斜体のテキスト</span><span class="sxs-lookup"><span data-stu-id="5d84b-115">Bold and italic text</span></span>

<span data-ttu-id="5d84b-116">テキストの書式を**太字**に設定するには、テキストを二重のアスタリスクで囲みます。</span><span class="sxs-lookup"><span data-stu-id="5d84b-116">To format text as **bold**, you enclose it in two asterisks:</span></span>

```markdown
    This text is **bold**.
```

<span data-ttu-id="5d84b-117">テキストの書式を*斜体*に設定するには、テキストを一重のアスタリスクで囲みます。</span><span class="sxs-lookup"><span data-stu-id="5d84b-117">To format text as *italic*, you enclose it in a single asterisk:</span></span>

```markdown
    This text is *italic*.
```

<span data-ttu-id="5d84b-118">テキストの書式を***太字と斜体***の両方に設定するには、テキストを三重のアスタリスクで囲みます。</span><span class="sxs-lookup"><span data-stu-id="5d84b-118">To format text as both ***bold and italic***, you enclose it in three asterisks:</span></span>

```markdown
    This is text is both ***bold and italic***.
```

### <a name="lists"></a><span data-ttu-id="5d84b-119">リスト</span><span class="sxs-lookup"><span data-stu-id="5d84b-119">Lists</span></span>

#### <a name="unordered-list"></a><span data-ttu-id="5d84b-120">記号付きリスト</span><span class="sxs-lookup"><span data-stu-id="5d84b-120">Unordered list</span></span>

<span data-ttu-id="5d84b-121">記号付きリスト/箇条書きリストの書式を設定するには、アスタリスクまたはダッシュを使用できます。</span><span class="sxs-lookup"><span data-stu-id="5d84b-121">To format an unordered/bulleted list, you can use either asterisks or dashes.</span></span> <span data-ttu-id="5d84b-122">たとえば、次の Markdown 書式は</span><span class="sxs-lookup"><span data-stu-id="5d84b-122">For example, the following Markdown:</span></span>

```markdown
- List item 1
- List item 2
- List item 3
```

<span data-ttu-id="5d84b-123">次のようにレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="5d84b-123">will be rendered as:</span></span>

- <span data-ttu-id="5d84b-124">List item 1</span><span class="sxs-lookup"><span data-stu-id="5d84b-124">List item 1</span></span>
- <span data-ttu-id="5d84b-125">List item 2</span><span class="sxs-lookup"><span data-stu-id="5d84b-125">List item 2</span></span>
- <span data-ttu-id="5d84b-126">List item 3</span><span class="sxs-lookup"><span data-stu-id="5d84b-126">List item 3</span></span>

<span data-ttu-id="5d84b-127">リストを別のリスト内にネストするには、子リスト アイテムをインデントします。</span><span class="sxs-lookup"><span data-stu-id="5d84b-127">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="5d84b-128">たとえば、次の Markdown 書式は</span><span class="sxs-lookup"><span data-stu-id="5d84b-128">For example, the following Markdown:</span></span>

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

<span data-ttu-id="5d84b-129">次のようにレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="5d84b-129">will be rendered as:</span></span>

- <span data-ttu-id="5d84b-130">List item 1</span><span class="sxs-lookup"><span data-stu-id="5d84b-130">List item 1</span></span>
  - <span data-ttu-id="5d84b-131">List item A</span><span class="sxs-lookup"><span data-stu-id="5d84b-131">List item A</span></span>
  - <span data-ttu-id="5d84b-132">List item B</span><span class="sxs-lookup"><span data-stu-id="5d84b-132">List item B</span></span>
- <span data-ttu-id="5d84b-133">List item 2</span><span class="sxs-lookup"><span data-stu-id="5d84b-133">List item 2</span></span>

#### <a name="ordered-list"></a><span data-ttu-id="5d84b-134">番号付きリスト</span><span class="sxs-lookup"><span data-stu-id="5d84b-134">Ordered list</span></span>

<span data-ttu-id="5d84b-135">番号付きリスト/段階的リストの書式を設定するには、対応する番号を使用します。</span><span class="sxs-lookup"><span data-stu-id="5d84b-135">To format an ordered/stepwise list, you use corresponding numbers.</span></span> <span data-ttu-id="5d84b-136">たとえば、次の Markdown 書式は</span><span class="sxs-lookup"><span data-stu-id="5d84b-136">For example, the following Markdown:</span></span>

```markdown
1. First instruction
2. Second instruction
3. Third instruction
```

<span data-ttu-id="5d84b-137">次のようにレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="5d84b-137">will be rendered as:</span></span>

1. <span data-ttu-id="5d84b-138">第 1 手順</span><span class="sxs-lookup"><span data-stu-id="5d84b-138">First instruction</span></span>
2. <span data-ttu-id="5d84b-139">第 2 手順</span><span class="sxs-lookup"><span data-stu-id="5d84b-139">Second instruction</span></span>
3. <span data-ttu-id="5d84b-140">第 3 手順</span><span class="sxs-lookup"><span data-stu-id="5d84b-140">Third instruction</span></span>

<span data-ttu-id="5d84b-141">リストを別のリスト内にネストするには、子リスト アイテムをインデントします。</span><span class="sxs-lookup"><span data-stu-id="5d84b-141">To nest a list within another list, indent the child list items.</span></span> <span data-ttu-id="5d84b-142">たとえば、次の Markdown 書式は</span><span class="sxs-lookup"><span data-stu-id="5d84b-142">For example, the following Markdown:</span></span>

```markdown
1. First instruction
    1. Sub-instruction
    2. Sub-instruction
2. Second instruction
```

<span data-ttu-id="5d84b-143">次のようにレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="5d84b-143">will be rendered as:</span></span>

1. <span data-ttu-id="5d84b-144">第 1 手順</span><span class="sxs-lookup"><span data-stu-id="5d84b-144">First instruction</span></span>
    1. <span data-ttu-id="5d84b-145">下位手順</span><span class="sxs-lookup"><span data-stu-id="5d84b-145">Sub-instruction</span></span>
    2. <span data-ttu-id="5d84b-146">下位手順</span><span class="sxs-lookup"><span data-stu-id="5d84b-146">Sub-instruction</span></span>
2. <span data-ttu-id="5d84b-147">第 2 手順</span><span class="sxs-lookup"><span data-stu-id="5d84b-147">Second instruction</span></span>

### <a name="tables"></a><span data-ttu-id="5d84b-148">表</span><span class="sxs-lookup"><span data-stu-id="5d84b-148">Tables</span></span>

<span data-ttu-id="5d84b-149">Markdown の基本仕様には表が含まれていませんが、GFM が表をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="5d84b-149">Tables are not part of the core Markdown specification, but GFM supports them.</span></span> <span data-ttu-id="5d84b-150">パイプ (|) 記号とハイフン記号 (-) を使用して表を作成できます。</span><span class="sxs-lookup"><span data-stu-id="5d84b-150">You can create tables by using the pipe (|) and hyphen (-) characters.</span></span> <span data-ttu-id="5d84b-151">ハイフンは各列のヘッダーを作成し、パイプは各列を区切ります。</span><span class="sxs-lookup"><span data-stu-id="5d84b-151">Hyphens create each column's header, while pipes separate each column.</span></span> <span data-ttu-id="5d84b-152">表が正しくレンダリングされるように、表の前に空の行を 1 つ挿入してください。</span><span class="sxs-lookup"><span data-stu-id="5d84b-152">Include a blank line before your table so it's rendered correctly.</span></span>

<span data-ttu-id="5d84b-153">たとえば、次の Markdown 書式は</span><span class="sxs-lookup"><span data-stu-id="5d84b-153">For example, the following Markdown:</span></span>

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

<span data-ttu-id="5d84b-154">次のようにレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="5d84b-154">will be rendered as:</span></span>

| <span data-ttu-id="5d84b-155">Fun</span><span class="sxs-lookup"><span data-stu-id="5d84b-155">Fun</span></span>                  | <span data-ttu-id="5d84b-156">With</span><span class="sxs-lookup"><span data-stu-id="5d84b-156">With</span></span>                 | <span data-ttu-id="5d84b-157">表</span><span class="sxs-lookup"><span data-stu-id="5d84b-157">Tables</span></span>          |
| :------------------- | -------------------: |:---------------:|
| <span data-ttu-id="5d84b-158">left-aligned column</span><span class="sxs-lookup"><span data-stu-id="5d84b-158">left-aligned column</span></span>  | <span data-ttu-id="5d84b-159">right-aligned column</span><span class="sxs-lookup"><span data-stu-id="5d84b-159">right-aligned column</span></span> | <span data-ttu-id="5d84b-160">centered column</span><span class="sxs-lookup"><span data-stu-id="5d84b-160">centered column</span></span> |
| <span data-ttu-id="5d84b-161">$100</span><span class="sxs-lookup"><span data-stu-id="5d84b-161">$100</span></span>                 | <span data-ttu-id="5d84b-162">$100</span><span class="sxs-lookup"><span data-stu-id="5d84b-162">$100</span></span>                 | <span data-ttu-id="5d84b-163">$100</span><span class="sxs-lookup"><span data-stu-id="5d84b-163">$100</span></span>            |
| <span data-ttu-id="5d84b-164">$10</span><span class="sxs-lookup"><span data-stu-id="5d84b-164">$10</span></span>                  | <span data-ttu-id="5d84b-165">$10</span><span class="sxs-lookup"><span data-stu-id="5d84b-165">$10</span></span>                  | <span data-ttu-id="5d84b-166">$10</span><span class="sxs-lookup"><span data-stu-id="5d84b-166">$10</span></span>             |
| <span data-ttu-id="5d84b-167">$1</span><span class="sxs-lookup"><span data-stu-id="5d84b-167">$1</span></span>                   | <span data-ttu-id="5d84b-168">$1</span><span class="sxs-lookup"><span data-stu-id="5d84b-168">$1</span></span>                   | <span data-ttu-id="5d84b-169">$1</span><span class="sxs-lookup"><span data-stu-id="5d84b-169">$1</span></span>              |

<span data-ttu-id="5d84b-170">表作成の詳細については、以下の情報源をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="5d84b-170">For more information on creating tables, see:</span></span>

- <span data-ttu-id="5d84b-171">横に長い表の書式設定に役立つ、Markdig の「[表を折り返す機能](#table-wrapping)」</span><span class="sxs-lookup"><span data-stu-id="5d84b-171">The Markdig [table wrapping feature](#table-wrapping), which can help with formatting of wide tables</span></span>
- <span data-ttu-id="5d84b-172">GitHub の「[Organizing information with tables (表を使用した情報の整理)](https://help.github.com/articles/organizing-information-with-tables/)」</span><span class="sxs-lookup"><span data-stu-id="5d84b-172">GitHub's [Organizing information with tables](https://help.github.com/articles/organizing-information-with-tables/)</span></span>
- <span data-ttu-id="5d84b-173">[Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) Web アプリ</span><span class="sxs-lookup"><span data-stu-id="5d84b-173">The [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) web app</span></span>
- <span data-ttu-id="5d84b-174">Adam Pritchard 氏の「[Markdown Cheatsheet (Markdown に関する簡易参照ガイド)](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables)」</span><span class="sxs-lookup"><span data-stu-id="5d84b-174">[Adam Pritchard's Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables)</span></span>
- <span data-ttu-id="5d84b-175">Michel Fortin 氏の [Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table) に関するページ</span><span class="sxs-lookup"><span data-stu-id="5d84b-175">[Michel Fortin's Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table)</span></span>
- [<span data-ttu-id="5d84b-176">HTML テーブルからマークダウンへの変換</span><span class="sxs-lookup"><span data-stu-id="5d84b-176">Convert HTML tables to Markdown</span></span>](https://jmalarcon.github.io/markdowntables/)

### <a name="links"></a><span data-ttu-id="5d84b-177">リンク</span><span class="sxs-lookup"><span data-stu-id="5d84b-177">Links</span></span>

<span data-ttu-id="5d84b-178">インライン リンクの Markdown 構文では、ハイパーリンクされるテキスト部分 `[link text]` の後に、リンク先 URL またはファイル名の部分 `(file-name.md)` が続きます。</span><span class="sxs-lookup"><span data-stu-id="5d84b-178">The Markdown syntax for an inline link consists of the `[link text]` portion, which is the text that will be hyperlinked, followed by the `(file-name.md)` portion, which is the URL or file name that's being linked to:</span></span>

 `[link text](file-name.md)`

<span data-ttu-id="5d84b-179">リンクの詳細については、以下の情報源をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="5d84b-179">For more information on linking, see:</span></span>

- <span data-ttu-id="5d84b-180">Markdown のリンクの基本的なサポートについては、[Markdown の構文](https://daringfireball.net/projects/markdown/syntax#link)に関するセクション。</span><span class="sxs-lookup"><span data-stu-id="5d84b-180">The [Markdown syntax guide](https://daringfireball.net/projects/markdown/syntax#link) for details on Markdown's base linking support.</span></span>
- <span data-ttu-id="5d84b-181">Markdig で提供されるその他のリンク構文の詳細については、このガイドの[リンク](how-to-write-links.md)に関するセクション。</span><span class="sxs-lookup"><span data-stu-id="5d84b-181">The [Links](how-to-write-links.md) section of this guide for details on additional linking syntax that Markdig provides.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="5d84b-182">コード スニペット</span><span class="sxs-lookup"><span data-stu-id="5d84b-182">Code snippets</span></span>

<span data-ttu-id="5d84b-183">Markdown では、コード スニペットの配置方法として、文中へのインライン配置と、文と文の間への "フェンスされた" 個別ブロックとしての配置の両方がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="5d84b-183">Markdown supports the placement of code snippets both inline in a sentence and as a separate "fenced" block between sentences.</span></span> <span data-ttu-id="5d84b-184">詳細については、以下の情報源をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="5d84b-184">For details, see:</span></span>

- <span data-ttu-id="5d84b-185">[Markdown のコード ブロックのネイティブ サポート](https://daringfireball.net/projects/markdown/syntax#precode)に関するセクション</span><span class="sxs-lookup"><span data-stu-id="5d84b-185">[Markdown's native support for code blocks](https://daringfireball.net/projects/markdown/syntax#precode)</span></span>
- <span data-ttu-id="5d84b-186">[GFM のコード フェンスと構文強調表示のサポート](https://help.github.com/articles/creating-and-highlighting-code-blocks/)に関するページ</span><span class="sxs-lookup"><span data-stu-id="5d84b-186">[GFM support for code fencing and syntax highlighting](https://help.github.com/articles/creating-and-highlighting-code-blocks/)</span></span>

<span data-ttu-id="5d84b-187">コード ブロックをフェンスすることで、コード スニペットの構文を強調表示することができます。</span><span class="sxs-lookup"><span data-stu-id="5d84b-187">Fenced code blocks are an easy way to enable syntax highlighting for your code snippets.</span></span> <span data-ttu-id="5d84b-188">フェンスされたコード ブロックの一般的な書式は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="5d84b-188">The general format for fenced code blocks is:</span></span>

    ```alias
    ...
    your code goes in here
    ...
    ```

<span data-ttu-id="5d84b-189">冒頭の 3 つのバッククォート (\`) 記号に続くエイリアスは、使用される構文強調表示を定義します。</span><span class="sxs-lookup"><span data-stu-id="5d84b-189">The alias after the initial three backtick (\`) characters defines the syntax highlighting to be used.</span></span> <span data-ttu-id="5d84b-190">以下は Docs コンテンツで一般的に使用されるプログラミング言語と、対応するラベルのリストです。</span><span class="sxs-lookup"><span data-stu-id="5d84b-190">The following is a list of commonly used programming languages in Docs content and the matching label:</span></span>

<span data-ttu-id="5d84b-191">これらの言語は、フレンドリ名をサポートし、ほとんどに言語の強調表示機能があります。</span><span class="sxs-lookup"><span data-stu-id="5d84b-191">These languages have friendly name support and most have language highlighting.</span></span>

|<span data-ttu-id="5d84b-192">名前</span><span class="sxs-lookup"><span data-stu-id="5d84b-192">Name</span></span>|<span data-ttu-id="5d84b-193">Markdown ラベル</span><span class="sxs-lookup"><span data-stu-id="5d84b-193">Markdown Label</span></span>|
|-----|-------|
|<span data-ttu-id="5d84b-194">.NET コンソール</span><span class="sxs-lookup"><span data-stu-id="5d84b-194">.NET Console</span></span>|<span data-ttu-id="5d84b-195">dotnetcli</span><span class="sxs-lookup"><span data-stu-id="5d84b-195">dotnetcli</span></span>|
|<span data-ttu-id="5d84b-196">ASP.NET (C#)</span><span class="sxs-lookup"><span data-stu-id="5d84b-196">ASP.NET (C#)</span></span>|<span data-ttu-id="5d84b-197">aspx-csharp</span><span class="sxs-lookup"><span data-stu-id="5d84b-197">aspx-csharp</span></span>|
|<span data-ttu-id="5d84b-198">ASP.NET (VB)</span><span class="sxs-lookup"><span data-stu-id="5d84b-198">ASP.NET (VB)</span></span>|<span data-ttu-id="5d84b-199">aspx-vb</span><span class="sxs-lookup"><span data-stu-id="5d84b-199">aspx-vb</span></span>|
|<span data-ttu-id="5d84b-200">AzCopy</span><span class="sxs-lookup"><span data-stu-id="5d84b-200">AzCopy</span></span>|<span data-ttu-id="5d84b-201">azcopy</span><span class="sxs-lookup"><span data-stu-id="5d84b-201">azcopy</span></span>|
|<span data-ttu-id="5d84b-202">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="5d84b-202">Azure CLI</span></span>|<span data-ttu-id="5d84b-203">azurecli</span><span class="sxs-lookup"><span data-stu-id="5d84b-203">azurecli</span></span>|
|<span data-ttu-id="5d84b-204">Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="5d84b-204">Azure PowerShell</span></span>|<span data-ttu-id="5d84b-205">azurepowershell</span><span class="sxs-lookup"><span data-stu-id="5d84b-205">azurepowershell</span></span>|
|<span data-ttu-id="5d84b-206">C++</span><span class="sxs-lookup"><span data-stu-id="5d84b-206">C++</span></span>|<span data-ttu-id="5d84b-207">cpp</span><span class="sxs-lookup"><span data-stu-id="5d84b-207">cpp</span></span>|
|<span data-ttu-id="5d84b-208">C++/CX</span><span class="sxs-lookup"><span data-stu-id="5d84b-208">C++/CX</span></span>|<span data-ttu-id="5d84b-209">cppcx</span><span class="sxs-lookup"><span data-stu-id="5d84b-209">cppcx</span></span>|
|<span data-ttu-id="5d84b-210">C++/WinRT</span><span class="sxs-lookup"><span data-stu-id="5d84b-210">C++/WinRT</span></span>|<span data-ttu-id="5d84b-211">cppwinrt</span><span class="sxs-lookup"><span data-stu-id="5d84b-211">cppwinrt</span></span>|
|<span data-ttu-id="5d84b-212">C#</span><span class="sxs-lookup"><span data-stu-id="5d84b-212">C#</span></span>|<span data-ttu-id="5d84b-213">csharp</span><span class="sxs-lookup"><span data-stu-id="5d84b-213">csharp</span></span>|
|<span data-ttu-id="5d84b-214">CSHTML</span><span class="sxs-lookup"><span data-stu-id="5d84b-214">CSHTML</span></span>|<span data-ttu-id="5d84b-215">cshtml</span><span class="sxs-lookup"><span data-stu-id="5d84b-215">cshtml</span></span>|
|<span data-ttu-id="5d84b-216">DAX</span><span class="sxs-lookup"><span data-stu-id="5d84b-216">DAX</span></span>|<span data-ttu-id="5d84b-217">dax</span><span class="sxs-lookup"><span data-stu-id="5d84b-217">dax</span></span>|
|<span data-ttu-id="5d84b-218">F#</span><span class="sxs-lookup"><span data-stu-id="5d84b-218">F#</span></span>|<span data-ttu-id="5d84b-219">fsharp</span><span class="sxs-lookup"><span data-stu-id="5d84b-219">fsharp</span></span>|
|<span data-ttu-id="5d84b-220">Go</span><span class="sxs-lookup"><span data-stu-id="5d84b-220">Go</span></span>|<span data-ttu-id="5d84b-221">go</span><span class="sxs-lookup"><span data-stu-id="5d84b-221">go</span></span>|
|<span data-ttu-id="5d84b-222">HTML</span><span class="sxs-lookup"><span data-stu-id="5d84b-222">HTML</span></span>|<span data-ttu-id="5d84b-223">html</span><span class="sxs-lookup"><span data-stu-id="5d84b-223">html</span></span>|
|<span data-ttu-id="5d84b-224">HTTP</span><span class="sxs-lookup"><span data-stu-id="5d84b-224">HTTP</span></span>|<span data-ttu-id="5d84b-225">http</span><span class="sxs-lookup"><span data-stu-id="5d84b-225">http</span></span>|
|<span data-ttu-id="5d84b-226">Java</span><span class="sxs-lookup"><span data-stu-id="5d84b-226">Java</span></span>|<span data-ttu-id="5d84b-227">java</span><span class="sxs-lookup"><span data-stu-id="5d84b-227">java</span></span>|
|<span data-ttu-id="5d84b-228">JavaScript</span><span class="sxs-lookup"><span data-stu-id="5d84b-228">JavaScript</span></span>|<span data-ttu-id="5d84b-229">javascript</span><span class="sxs-lookup"><span data-stu-id="5d84b-229">javascript</span></span>|
|<span data-ttu-id="5d84b-230">JSON</span><span class="sxs-lookup"><span data-stu-id="5d84b-230">JSON</span></span>|<span data-ttu-id="5d84b-231">json</span><span class="sxs-lookup"><span data-stu-id="5d84b-231">json</span></span>|
|<span data-ttu-id="5d84b-232">Markdown</span><span class="sxs-lookup"><span data-stu-id="5d84b-232">Markdown</span></span>|<span data-ttu-id="5d84b-233">md</span><span class="sxs-lookup"><span data-stu-id="5d84b-233">md</span></span>|
|<span data-ttu-id="5d84b-234">NodeJS</span><span class="sxs-lookup"><span data-stu-id="5d84b-234">NodeJS</span></span>|<span data-ttu-id="5d84b-235">nodejs</span><span class="sxs-lookup"><span data-stu-id="5d84b-235">nodejs</span></span>|
|<span data-ttu-id="5d84b-236">Objective-C</span><span class="sxs-lookup"><span data-stu-id="5d84b-236">Objective-C</span></span>|<span data-ttu-id="5d84b-237">objc</span><span class="sxs-lookup"><span data-stu-id="5d84b-237">objc</span></span>|
|<span data-ttu-id="5d84b-238">OData</span><span class="sxs-lookup"><span data-stu-id="5d84b-238">OData</span></span>|<span data-ttu-id="5d84b-239">odata</span><span class="sxs-lookup"><span data-stu-id="5d84b-239">odata</span></span>|
|<span data-ttu-id="5d84b-240">PHP</span><span class="sxs-lookup"><span data-stu-id="5d84b-240">PHP</span></span>|<span data-ttu-id="5d84b-241">php</span><span class="sxs-lookup"><span data-stu-id="5d84b-241">php</span></span>|
|<span data-ttu-id="5d84b-242">Power Apps Formula</span><span class="sxs-lookup"><span data-stu-id="5d84b-242">Power Apps Formula</span></span>|<span data-ttu-id="5d84b-243">powerappsfl</span><span class="sxs-lookup"><span data-stu-id="5d84b-243">powerappsfl</span></span>|
|<span data-ttu-id="5d84b-244">PowerShell</span><span class="sxs-lookup"><span data-stu-id="5d84b-244">PowerShell</span></span>|<span data-ttu-id="5d84b-245">powershell</span><span class="sxs-lookup"><span data-stu-id="5d84b-245">powershell</span></span>|
|<span data-ttu-id="5d84b-246">Python</span><span class="sxs-lookup"><span data-stu-id="5d84b-246">Python</span></span>|<span data-ttu-id="5d84b-247">python</span><span class="sxs-lookup"><span data-stu-id="5d84b-247">python</span></span>|
|<span data-ttu-id="5d84b-248">Q#</span><span class="sxs-lookup"><span data-stu-id="5d84b-248">Q#</span></span>|<span data-ttu-id="5d84b-249">qsharp</span><span class="sxs-lookup"><span data-stu-id="5d84b-249">qsharp</span></span>|
|<span data-ttu-id="5d84b-250">Ruby</span><span class="sxs-lookup"><span data-stu-id="5d84b-250">Ruby</span></span>|<span data-ttu-id="5d84b-251">ruby</span><span class="sxs-lookup"><span data-stu-id="5d84b-251">ruby</span></span>|
|<span data-ttu-id="5d84b-252">SQL</span><span class="sxs-lookup"><span data-stu-id="5d84b-252">SQL</span></span>|<span data-ttu-id="5d84b-253">sql</span><span class="sxs-lookup"><span data-stu-id="5d84b-253">sql</span></span>|
|<span data-ttu-id="5d84b-254">Swift</span><span class="sxs-lookup"><span data-stu-id="5d84b-254">Swift</span></span>|<span data-ttu-id="5d84b-255">swift</span><span class="sxs-lookup"><span data-stu-id="5d84b-255">swift</span></span>|
|<span data-ttu-id="5d84b-256">TypeScript</span><span class="sxs-lookup"><span data-stu-id="5d84b-256">TypeScript</span></span>|<span data-ttu-id="5d84b-257">typescript</span><span class="sxs-lookup"><span data-stu-id="5d84b-257">typescript</span></span>|
|<span data-ttu-id="5d84b-258">VB</span><span class="sxs-lookup"><span data-stu-id="5d84b-258">VB</span></span>|<span data-ttu-id="5d84b-259">vb</span><span class="sxs-lookup"><span data-stu-id="5d84b-259">vb</span></span>|
|<span data-ttu-id="5d84b-260">VSTS CLI</span><span class="sxs-lookup"><span data-stu-id="5d84b-260">VSTS CLI</span></span>|<span data-ttu-id="5d84b-261">vstscli</span><span class="sxs-lookup"><span data-stu-id="5d84b-261">vstscli</span></span>|
|<span data-ttu-id="5d84b-262">XAML</span><span class="sxs-lookup"><span data-stu-id="5d84b-262">XAML</span></span>|<span data-ttu-id="5d84b-263">xaml</span><span class="sxs-lookup"><span data-stu-id="5d84b-263">xaml</span></span>|
|<span data-ttu-id="5d84b-264">XML</span><span class="sxs-lookup"><span data-stu-id="5d84b-264">XML</span></span>|<span data-ttu-id="5d84b-265">xml</span><span class="sxs-lookup"><span data-stu-id="5d84b-265">xml</span></span>|

#### <a name="example-c"></a><span data-ttu-id="5d84b-266">例: C\#</span><span class="sxs-lookup"><span data-stu-id="5d84b-266">Example: C\#</span></span>

<span data-ttu-id="5d84b-267">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="5d84b-267">__Markdown__</span></span>

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

<span data-ttu-id="5d84b-268">__レンダー__</span><span class="sxs-lookup"><span data-stu-id="5d84b-268">__Render__</span></span>

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

#### <a name="example-sql"></a><span data-ttu-id="5d84b-269">例: SQL</span><span class="sxs-lookup"><span data-stu-id="5d84b-269">Example: SQL</span></span>

<span data-ttu-id="5d84b-270">__Markdown__</span><span class="sxs-lookup"><span data-stu-id="5d84b-270">__Markdown__</span></span>

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

<span data-ttu-id="5d84b-271">__レンダー__</span><span class="sxs-lookup"><span data-stu-id="5d84b-271">__Render__</span></span>

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a><span data-ttu-id="5d84b-272">OPS による Markdown のカスタム拡張機能</span><span class="sxs-lookup"><span data-stu-id="5d84b-272">OPS custom Markdown extensions</span></span>

> [!NOTE]
> <span data-ttu-id="5d84b-273">Open Publishing Services (OPS) は GitHub Flavored Markdown (GFM) との互換性が非常に高い Markdown パーサー Markdig を実装しています。</span><span class="sxs-lookup"><span data-stu-id="5d84b-273">Open Publishing Services (OPS) implements a Markdig Parser for Markdown, which is highly compatible with GitHub Flavored Markdown (GFM).</span></span> <span data-ttu-id="5d84b-274">Markdig は Markdown 拡張機能を介していくつかの機能を追加しています。</span><span class="sxs-lookup"><span data-stu-id="5d84b-274">Markdig adds some functionality through Markdown extensions.</span></span> <span data-ttu-id="5d84b-275">そのため、完全版の「OPS Authoring Guide」 (OPS オーサリング ガイド) の一部の記事は、参考のためにこのガイドに含まれています </span><span class="sxs-lookup"><span data-stu-id="5d84b-275">As such, selected articles from the full OPS Authoring Guide are included in this guide for reference.</span></span> <span data-ttu-id="5d84b-276">(たとえば、目次の「Markdig and Markdown extensions」(Markdig と Markdown の拡張機能) と「Code snippets」(コード スニペット) をご覧ください)。</span><span class="sxs-lookup"><span data-stu-id="5d84b-276">(For example, see "Markdig and Markdown extensions" and "Code snippets" in the table of contents.)</span></span>

<span data-ttu-id="5d84b-277">Docs 記事では、段落、リンク、リスト、見出しなど、ほとんどの書式設定に GFM が使用されます。</span><span class="sxs-lookup"><span data-stu-id="5d84b-277">Docs articles use GFM for most article formatting, such as paragraphs, links, lists, and headings.</span></span> <span data-ttu-id="5d84b-278">記事の高度な書式設定には、次のような Markdig 機能を使用できます。</span><span class="sxs-lookup"><span data-stu-id="5d84b-278">For richer formatting, articles can use Markdig features such as:</span></span>

- <span data-ttu-id="5d84b-279">注ブロック</span><span class="sxs-lookup"><span data-stu-id="5d84b-279">Note blocks</span></span>
- <span data-ttu-id="5d84b-280">インクルード</span><span class="sxs-lookup"><span data-stu-id="5d84b-280">Includes</span></span>
- <span data-ttu-id="5d84b-281">セレクター</span><span class="sxs-lookup"><span data-stu-id="5d84b-281">Selectors</span></span>
- <span data-ttu-id="5d84b-282">埋め込みビデオ</span><span class="sxs-lookup"><span data-stu-id="5d84b-282">Embedded videos</span></span>
- <span data-ttu-id="5d84b-283">コード スニペット/サンプル</span><span class="sxs-lookup"><span data-stu-id="5d84b-283">Code snippets/samples</span></span>

<span data-ttu-id="5d84b-284">完全なリストについては、目次の「Markdig and Markdown extensions」(Markdig と Markdown の拡張機能) と「Code snippets」(コード スニペット) をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="5d84b-284">For the complete list, refer to "Markdig and Markdown extensions" and "Code snippets" in the table of contents.</span></span>

### <a name="note-blocks"></a><span data-ttu-id="5d84b-285">注ブロック</span><span class="sxs-lookup"><span data-stu-id="5d84b-285">Note blocks</span></span>

<span data-ttu-id="5d84b-286">特定の内容に注目を集めるには、4 つのタイプの注ブロックから選択できます。</span><span class="sxs-lookup"><span data-stu-id="5d84b-286">You can choose from four types of note blocks to draw attention to specific content:</span></span>

- <span data-ttu-id="5d84b-287">NOTE (注意)</span><span class="sxs-lookup"><span data-stu-id="5d84b-287">NOTE</span></span>
- <span data-ttu-id="5d84b-288">WARNING (警告)</span><span class="sxs-lookup"><span data-stu-id="5d84b-288">WARNING</span></span>
- <span data-ttu-id="5d84b-289">TIP (ヒント)</span><span class="sxs-lookup"><span data-stu-id="5d84b-289">TIP</span></span>
- <span data-ttu-id="5d84b-290">IMPORTANT (重要)</span><span class="sxs-lookup"><span data-stu-id="5d84b-290">IMPORTANT</span></span>

<span data-ttu-id="5d84b-291">注ブロックによって文章がわかりにくくなることがあるので、概して注ブロックは控えめに使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5d84b-291">In general, note blocks should be used sparingly because they can be disruptive.</span></span> <span data-ttu-id="5d84b-292">注ブロックでもコード ブロック、イメージ、リスト、およびリンクがサポートされますが、注ブロックを簡潔でわかりやすくするように心掛けてください。</span><span class="sxs-lookup"><span data-stu-id="5d84b-292">Although they also support code blocks, images, lists, and links, try to keep your note blocks simple and straightforward.</span></span>

### <a name="includes"></a><span data-ttu-id="5d84b-293">インクルード</span><span class="sxs-lookup"><span data-stu-id="5d84b-293">Includes</span></span>

<span data-ttu-id="5d84b-294">再利用可能なテキスト ファイルまたはイメージ ファイルを記事ファイルにインクルードする必要がある場合は、Markdig のファイル インクルード機能を使用して "インクルード" ファイルを参照できます。</span><span class="sxs-lookup"><span data-stu-id="5d84b-294">When you have reusable text or image files that need to be included in article files, you can use a reference to the "include" file via the Markdig file include feature.</span></span> <span data-ttu-id="5d84b-295">この機能は、ビルド時に特定のファイルを記事ファイルにインクルードするように OPS に指示します。これにより、その指定されたファイルは公開記事に含まれるようになります。</span><span class="sxs-lookup"><span data-stu-id="5d84b-295">This feature instructs OPS to include the file in your article file at build time, making it part of your published article.</span></span> <span data-ttu-id="5d84b-296">コンテンツの再利用に役立つ 3 つのタイプのインクルードがあります。</span><span class="sxs-lookup"><span data-stu-id="5d84b-296">Three types of includes are available to help you reuse content:</span></span>

- <span data-ttu-id="5d84b-297">インライン: 一般的なテキスト スニペットを別の文中にインラインで再利用できます。</span><span class="sxs-lookup"><span data-stu-id="5d84b-297">Inline: Reuse a common text snippet inline with within another sentence.</span></span>
- <span data-ttu-id="5d84b-298">ブロック: Markdown ファイル全体をブロックとして再利用し、記事のセクション内にネストできます。</span><span class="sxs-lookup"><span data-stu-id="5d84b-298">Block: Reuse an entire Markdown file as a block, nested within a section of an article.</span></span>
- <span data-ttu-id="5d84b-299">イメージ: これは Docs に実装されている標準的なイメージ インクルードの方法です。</span><span class="sxs-lookup"><span data-stu-id="5d84b-299">Image: This is how standard image inclusion is implemented in Docs.</span></span>

<span data-ttu-id="5d84b-300">インラインまたはブロックによるインクルードは簡易な Markdown (.md) ファイルにすぎません。</span><span class="sxs-lookup"><span data-stu-id="5d84b-300">An inline or block include is just a simple Markdown (.md) file.</span></span> <span data-ttu-id="5d84b-301">これにはあらゆる有効な Markdown を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="5d84b-301">It can contain any valid Markdown.</span></span> <span data-ttu-id="5d84b-302">すべてのインクルード Markdown ファイルは、リポジトリのルートにある[共通の `/includes` サブディレクトリ](git-github-fundamentals.md#includes-subdirectory)に配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5d84b-302">All include Markdown files should be placed in a [common `/includes` subdirectory](git-github-fundamentals.md#includes-subdirectory), in the root of the repository.</span></span> <span data-ttu-id="5d84b-303">記事が公開されると、インクルードされたファイルはその記事にシームレスに統合されます。</span><span class="sxs-lookup"><span data-stu-id="5d84b-303">When the article is published, the included file is seamlessly integrated into it.</span></span>

<span data-ttu-id="5d84b-304">インクルードに関する要件と考慮事項を次に示します。</span><span class="sxs-lookup"><span data-stu-id="5d84b-304">Here are requirements and considerations for includes:</span></span>

- <span data-ttu-id="5d84b-305">複数の記事に同じテキストを表示する必要があるときには、インクルードを使用してください。</span><span class="sxs-lookup"><span data-stu-id="5d84b-305">Use includes whenever you need the same text to appear in multiple articles.</span></span>
- <span data-ttu-id="5d84b-306">ブロックによるインクルードは、1 つまたは 2 つの段落、共通の手順、共通のセクションといった分量の多いコンテンツに使用してください。</span><span class="sxs-lookup"><span data-stu-id="5d84b-306">Use block includes for significant amounts of content--a paragraph or two, a shared procedure, or a shared section.</span></span> <span data-ttu-id="5d84b-307">1 つの文よりも小さい場合には、使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="5d84b-307">Do not use them for anything smaller than a sentence.</span></span>
- <span data-ttu-id="5d84b-308">インクルードは Markdig 拡張機能に依存するため、GitHub がレンダリングした記事にインクルードはレンダリングされません。</span><span class="sxs-lookup"><span data-stu-id="5d84b-308">Includes won't be rendered in the GitHub rendered view of your article, because they rely on Markdig extensions.</span></span> <span data-ttu-id="5d84b-309">公開後にのみレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="5d84b-309">They'll be rendered only after publication.</span></span>
- <span data-ttu-id="5d84b-310">インクルード内のすべてのテキストの記述には、インクルードを参照する記事内の先行テキストや後続テキストに依存しない完全な文または語句を使用してください。</span><span class="sxs-lookup"><span data-stu-id="5d84b-310">Ensure that all the text in an include is written in complete sentences or phrases that do not depend on preceding text or following text in the article that references the include.</span></span> <span data-ttu-id="5d84b-311">このガイダンスを無視すると、ローカライズされたエクスペリエンスを乱す翻訳不可能な文字列が記事内に発生します。</span><span class="sxs-lookup"><span data-stu-id="5d84b-311">Ignoring this guidance creates an untranslatable string in the article that breaks the localized experience.</span></span>
- <span data-ttu-id="5d84b-312">インクルードをほかのインクルード内に埋め込まないでください。</span><span class="sxs-lookup"><span data-stu-id="5d84b-312">Don't embed includes within other includes.</span></span> <span data-ttu-id="5d84b-313">それはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="5d84b-313">They are not supported.</span></span>
- <span data-ttu-id="5d84b-314">メディア ファイルは、インクルードのサブディレクトリ内にあるメディア フォルダーに配置する必要があります。たとえば、`<repo>`/includes/media フォルダーです。</span><span class="sxs-lookup"><span data-stu-id="5d84b-314">Place media files in a media folder that's specific to the include subdirectory--for instance, the `<repo>`/includes/media folder.</span></span> <span data-ttu-id="5d84b-315">メディア ディレクトリのルートにはイメージを配置しないでください。</span><span class="sxs-lookup"><span data-stu-id="5d84b-315">The media directory should not contain any images in its root.</span></span> <span data-ttu-id="5d84b-316">イメージがないインクルードの場合は、対応するメディア ディレクトリは不要です。</span><span class="sxs-lookup"><span data-stu-id="5d84b-316">If the include does not have images, a corresponding media directory is not required.</span></span>
- <span data-ttu-id="5d84b-317">通常の記事と同様に、インクルード ファイル間でメディアを共有しないでください。</span><span class="sxs-lookup"><span data-stu-id="5d84b-317">As with regular articles, don't share media between include files.</span></span> <span data-ttu-id="5d84b-318">インクルードおよび記事ごとに、一意の名前を持つ個別ファイルを使用してください。</span><span class="sxs-lookup"><span data-stu-id="5d84b-318">Use a separate file with a unique name for each include and article.</span></span> <span data-ttu-id="5d84b-319">インクルードに関連するメディア フォルダー内にメディア ファイルを格納してください。</span><span class="sxs-lookup"><span data-stu-id="5d84b-319">Store the media file in the media folder that's associated with the include.</span></span>
- <span data-ttu-id="5d84b-320">記事の唯一のコンテンツとしてインクルードを使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="5d84b-320">Don't use an include as the only content of an article.</span></span>  <span data-ttu-id="5d84b-321">インクルードの目的は、記事内のほかのコンテンツを補完することです。</span><span class="sxs-lookup"><span data-stu-id="5d84b-321">Includes are meant to be supplemental to the content in the rest of the article.</span></span>

### <a name="selectors"></a><span data-ttu-id="5d84b-322">セレクター</span><span class="sxs-lookup"><span data-stu-id="5d84b-322">Selectors</span></span>

<span data-ttu-id="5d84b-323">同じ技術記事の複数のバージョンを記述するときには、複数のテクノロジまたはプラットフォームの実装の違いに対応するために、セレクターを使用します。</span><span class="sxs-lookup"><span data-stu-id="5d84b-323">Use selectors in technical articles when you author multiple flavors of the same article, to address differences in implementation across technologies or platforms.</span></span> <span data-ttu-id="5d84b-324">通常、これが最も当てはまるのは、Microsoft の開発者向けのモバイル プラットフォームのコンテンツです。</span><span class="sxs-lookup"><span data-stu-id="5d84b-324">This is typically most applicable to our mobile platform content for developers.</span></span> <span data-ttu-id="5d84b-325">現在 Markdig にはシングル セレクターとマルチ セレクターという 2 つのタイプのセレクターがあります。</span><span class="sxs-lookup"><span data-stu-id="5d84b-325">There are currently two different types of selectors in Markdig, a single selector and a multi-selector.</span></span>

<span data-ttu-id="5d84b-326">選択範囲内の各記事に配置されるセレクター Markdown は同じであるため、記事のセレクターをインクルードに配置することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="5d84b-326">Because the same selector Markdown goes in each article in the selection, we recommend placing the selector for your article in an include.</span></span> <span data-ttu-id="5d84b-327">そのうえで、同じセレクターを使用するすべての記事でそのインクルードを参照できます。</span><span class="sxs-lookup"><span data-stu-id="5d84b-327">Then you can reference that include in all your articles that use the same selector.</span></span>

### <a name="code-snippets"></a><span data-ttu-id="5d84b-328">コード スニペット</span><span class="sxs-lookup"><span data-stu-id="5d84b-328">Code snippets</span></span>

<span data-ttu-id="5d84b-329">Markdig では、コード スニペット拡張機能を使用した記事へのコードの高度なインクルードがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="5d84b-329">Markdig supports advanced inclusion of code in an article, via its code snippet extension.</span></span> <span data-ttu-id="5d84b-330">プログラミング言語の選択や構文の色分けといった GFM 機能に基づく高度なレンダリングに加えて、次のような便利な機能を使用できます。</span><span class="sxs-lookup"><span data-stu-id="5d84b-330">It provides advanced rendering that builds on GFM features such as programming language selection and syntax coloring, plus nice features such as:</span></span>

- <span data-ttu-id="5d84b-331">外部リポジトリから集められたコード サンプル/スニペットのインクルード。</span><span class="sxs-lookup"><span data-stu-id="5d84b-331">Inclusion of centralized code samples/snippets from an external repository.</span></span>
- <span data-ttu-id="5d84b-332">さまざまな言語でのさまざまなバージョンのコード サンプルをタブに表示する UI。</span><span class="sxs-lookup"><span data-stu-id="5d84b-332">Tabbed UI to show multiple versions of code samples in different languages.</span></span>

## <a name="gotchas-and-troubleshooting"></a><span data-ttu-id="5d84b-333">問題の発見 + トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="5d84b-333">Gotchas and troubleshooting</span></span>

### <a name="alt-text"></a><span data-ttu-id="5d84b-334">alt テキスト</span><span class="sxs-lookup"><span data-stu-id="5d84b-334">Alt text</span></span>

<span data-ttu-id="5d84b-335">アンダー スコアを含む alt テキストは正しくレンダリングされません。</span><span class="sxs-lookup"><span data-stu-id="5d84b-335">Alt text that contains underscores won't be rendered properly.</span></span> <span data-ttu-id="5d84b-336">たとえば、次のテキストを使用するのではなく、</span><span class="sxs-lookup"><span data-stu-id="5d84b-336">For example, instead of using this:</span></span>

```markdown
![ADextension_2FA_Configure_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

<span data-ttu-id="5d84b-337">次のようにアンダー スコアをエスケープします。</span><span class="sxs-lookup"><span data-stu-id="5d84b-337">Escape the underscores like this:</span></span>

```markdown
![ADextension\_2FA\_Configure\_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a><span data-ttu-id="5d84b-338">アポストロフィと引用符</span><span class="sxs-lookup"><span data-stu-id="5d84b-338">Apostrophes and quotation marks</span></span>

<span data-ttu-id="5d84b-339">Word から Markdown エディターにコピーしたテキストに、"スマート" (カールした) アポストロフィまたは引用符が含まれていることがあります。</span><span class="sxs-lookup"><span data-stu-id="5d84b-339">If you copy from Word into a Markdown editor, the text might contain "smart" (curly) apostrophes or quotation marks.</span></span> <span data-ttu-id="5d84b-340">これらを標準的なアポストロフィや引用符にエンコードまたは変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5d84b-340">These need to be encoded or changed to basic apostrophes or quotation marks.</span></span> <span data-ttu-id="5d84b-341">そうしないと、ファイルが公開されたときに Itâ€™s のように表示されます</span><span class="sxs-lookup"><span data-stu-id="5d84b-341">Otherwise, you end up with things like this when the file is published: Itâ€™s</span></span>

<span data-ttu-id="5d84b-342">これらの "スマート" バージョンの記述記号のエンコーディングは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="5d84b-342">Here are the encodings for the "smart" versions of these punctuation marks:</span></span>

- <span data-ttu-id="5d84b-343">左 (始め) 二重引用符: `&#8220;`</span><span class="sxs-lookup"><span data-stu-id="5d84b-343">Left (opening) quotation mark: `&#8220;`</span></span>
- <span data-ttu-id="5d84b-344">右 (終わり) 二重引用符: `&#8221;`</span><span class="sxs-lookup"><span data-stu-id="5d84b-344">Right (closing) quotation mark: `&#8221;`</span></span>
- <span data-ttu-id="5d84b-345">右 (終わり) 一重引用符またはアポストロフィ: `&#8217;`</span><span class="sxs-lookup"><span data-stu-id="5d84b-345">Right (closing) single quotation mark or apostrophe: `&#8217;`</span></span>
- <span data-ttu-id="5d84b-346">左 (始め) 一重引用符 (あまり使用されません): `&#8216;`</span><span class="sxs-lookup"><span data-stu-id="5d84b-346">Left (opening) single quotation mark (rarely used): `&#8216;`</span></span>

### <a name="angle-brackets"></a><span data-ttu-id="5d84b-347">山かっこ</span><span class="sxs-lookup"><span data-stu-id="5d84b-347">Angle brackets</span></span>

<span data-ttu-id="5d84b-348">プレースホルダーを示すためなどに、ファイル内の (コードではなく) テキストに山かっこを使用する場合は、山かっこを手動でエンコードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5d84b-348">If you use angle brackets in text (not code) in your file--for example, to denote a placeholder--you need to manually encode the angle brackets.</span></span> <span data-ttu-id="5d84b-349">そうしないと、それらのテキストは Markdown によって HTML タグとして認識されます。</span><span class="sxs-lookup"><span data-stu-id="5d84b-349">Otherwise, Markdown thinks that they're intended to be an HTML tag.</span></span>

<span data-ttu-id="5d84b-350">たとえば、`<script name>` を `&lt;script name&gt;` にエンコードしてください。</span><span class="sxs-lookup"><span data-stu-id="5d84b-350">For example, encode `<script name>` as `&lt;script name&gt;`</span></span>

## <a name="see-also"></a><span data-ttu-id="5d84b-351">関連項目</span><span class="sxs-lookup"><span data-stu-id="5d84b-351">See also</span></span>

### <a name="markdown-resources"></a><span data-ttu-id="5d84b-352">Markdown に関するリソース</span><span class="sxs-lookup"><span data-stu-id="5d84b-352">Markdown resources</span></span>

- [<span data-ttu-id="5d84b-353">Markdown 入門</span><span class="sxs-lookup"><span data-stu-id="5d84b-353">Introduction to Markdown</span></span>](https://daringfireball.net/projects/markdown/syntax)
- [<span data-ttu-id="5d84b-354">Docs の Markdown に関する簡易参照ガイド</span><span class="sxs-lookup"><span data-stu-id="5d84b-354">Docs Markdown cheat sheet</span></span>](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [<span data-ttu-id="5d84b-355">GitHub の Markdown の基本</span><span class="sxs-lookup"><span data-stu-id="5d84b-355">GitHub's Markdown Basics</span></span>](https://help.github.com/articles/markdown-basics/)
