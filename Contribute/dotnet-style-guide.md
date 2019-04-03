---
title: .NET 記事のテンプレートとチートシート
description: この記事には、.NET ドキュメント リポジトリ用の新しい記事を作成するときに使用できる便利なテンプレートが含まれています
ms.date: 11/07/2018
ms.openlocfilehash: 9b57abd96093940c96f90a4a01b9f81eae063ffb
ms.sourcegitcommit: af37d44eb67daa2841959817cd205ec95db18cec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/29/2019
ms.locfileid: "58653622"
---
# <a name="metadata-and-markdown-template-for-net-docs"></a><span data-ttu-id="7ace6-103">.NET ドキュメントのメタデータと Markdown テンプレート</span><span class="sxs-lookup"><span data-stu-id="7ace6-103">Metadata and Markdown template for .NET docs</span></span>

<span data-ttu-id="7ace6-104">この dotnet/docs テンプレートには、Markdown 構文の例とメタデータの設定方法が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7ace6-104">This dotnet/docs template contains examples of Markdown syntax, as well as guidance on setting the metadata.</span></span>

<span data-ttu-id="7ace6-105">Markdown ファイルを作成するとき、付属のテンプレートを新しいファイルにコピーし、下のようにメタデータに入力し、上の H1 見出しを記事のタイトルに設定してください。</span><span class="sxs-lookup"><span data-stu-id="7ace6-105">When creating a Markdown file, you should copy the included template to a new file, fill out the metadata as specified below, and set the H1 heading above to the title of the article.</span></span>

## <a name="metadata"></a><span data-ttu-id="7ace6-106">メタデータ</span><span class="sxs-lookup"><span data-stu-id="7ace6-106">Metadata</span></span>

<span data-ttu-id="7ace6-107">必須のメタデータ ブロックは次のサンプル メタデータ ブロックにあります。</span><span class="sxs-lookup"><span data-stu-id="7ace6-107">The required metadata block is in the following sample metadata block:</span></span>

```markdown
---
title: [ARTICLE TITLE]
description: [usually a summary of your first paragraph. It gets displayed in search results, and can help drive the correct traffic if well written.]
author: [GITHUB USERNAME]
ms.date: [CREATION/UPDATE DATE - mm/dd/yyyy]
---
# The H1 should not be the same as the title, but should describe the article contents
```

- <span data-ttu-id="7ace6-108">コロン (:) とメタデータ要素の値の間にはスペースを入れる**必要があります**。</span><span class="sxs-lookup"><span data-stu-id="7ace6-108">You **must** have a space between the colon (:) and the value for a metadata element.</span></span>
- <span data-ttu-id="7ace6-109">値 (タイトルなど) 内のコロンによってメタデータ パーサーが中断されます。</span><span class="sxs-lookup"><span data-stu-id="7ace6-109">Colons in a value (for example, a title) break the metadata parser.</span></span> <span data-ttu-id="7ace6-110">その場合、タイトルを二重引用符で囲みます (例: `title: "Writing .NET Core console apps: An advanced step-by-step guide"`)。</span><span class="sxs-lookup"><span data-stu-id="7ace6-110">In this case, surround the title with double quotes (for example, `title: "Writing .NET Core console apps: An advanced step-by-step guide"`).</span></span>
- <span data-ttu-id="7ace6-111">**title**: 検索エンジンの結果に表示されます。</span><span class="sxs-lookup"><span data-stu-id="7ace6-111">**title**: Appears in search engine results.</span></span> <span data-ttu-id="7ace6-112">タイトルは H1 見出しのタイトルと同じにしないでください。また、60 文字以下にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7ace6-112">The title shouldn't be identical to the title in your H1 heading, and it should contain 60 characters or less.</span></span>
- <span data-ttu-id="7ace6-113">**説明**: 記事の内容をまとめます。</span><span class="sxs-lookup"><span data-stu-id="7ace6-113">**description**: Summarizes the content of the article.</span></span> <span data-ttu-id="7ace6-114">通常、検索結果ページに表示されますが、検索ランキングには使用されません。</span><span class="sxs-lookup"><span data-stu-id="7ace6-114">It's usually shown in the search results page, but it isn't used for search ranking.</span></span> <span data-ttu-id="7ace6-115">その長さはスペースを含めて 115-145 文字にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7ace6-115">Its length should be 115-145 characters including spaces.</span></span>
- <span data-ttu-id="7ace6-116">**author**: author フィールドには、作成者の **GitHub ユーザー名**を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="7ace6-116">**author**: The author field should contain the **GitHub username** of the author.</span></span>
- <span data-ttu-id="7ace6-117">**ms.date**: 前回の大きな更新の日付です。</span><span class="sxs-lookup"><span data-stu-id="7ace6-117">**ms.date**: The date of the last significant update.</span></span> <span data-ttu-id="7ace6-118">記事全体を見直し、更新している場合、既存の記事でこれを更新します。</span><span class="sxs-lookup"><span data-stu-id="7ace6-118">Update this on existing articles if you reviewed and updated the entire article.</span></span> <span data-ttu-id="7ace6-119">誤植など、小さな修正の場合、更新されるとは限りません。</span><span class="sxs-lookup"><span data-stu-id="7ace6-119">Small fixes, such as typos or similar do not warrant an update.</span></span>

<span data-ttu-id="7ace6-120">その他のメタデータは各記事に付け加えられますが、通常、ほとんどのメタデータ値は **docfx.json** に指定されているフォルダー レベルで適用されます。</span><span class="sxs-lookup"><span data-stu-id="7ace6-120">Other metadata is attached to each article, but we typically apply most metadata values at the folder level, specified in **docfx.json**.</span></span>

## <a name="basic-markdown-gfm-and-special-characters"></a><span data-ttu-id="7ace6-121">基本的 Markdown、GFM、特殊文字</span><span class="sxs-lookup"><span data-stu-id="7ace6-121">Basic Markdown, GFM, and special characters</span></span>

<span data-ttu-id="7ace6-122">Markdown、GitHub Flavored Markdown (GFM)、OPS 固有の拡張機能の基本については [Markdown](how-to-write-use-markdown.md) と [Markdown リファレンス](markdown-reference.md)に関する全般記事で学習できます。</span><span class="sxs-lookup"><span data-stu-id="7ace6-122">You can learn the basics of Markdown, GitHub Flavored Markdown (GFM), and OPS specific extensions in the general articles on [Markdown](how-to-write-use-markdown.md) and [Markdown reference](markdown-reference.md).</span></span>

<span data-ttu-id="7ace6-123">Markdown では、書式設定に \*、\`、\# のような特殊文字が使用されます。</span><span class="sxs-lookup"><span data-stu-id="7ace6-123">Markdown uses special characters such as \*, \`, and \# for formatting.</span></span> <span data-ttu-id="7ace6-124">このような文字をコンテンツに含める場合、次の 2 つのいずれかを行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="7ace6-124">If you wish to include one of these characters in your content, you must do one of two things:</span></span>

- <span data-ttu-id="7ace6-125">特殊文字の前にバックスラッシュを置いて "エスケープ処理" します (たとえば、\* の場合、`\*`)。</span><span class="sxs-lookup"><span data-stu-id="7ace6-125">Put a backslash before the special character to "escape" it (for example, `\*` for a \*)</span></span>
- <span data-ttu-id="7ace6-126">その文字の [HTML エンティティ コード](http://www.ascii.cl/htmlcodes.htm)を使用します (たとえば、&#42; の場合、`&#42;`)。</span><span class="sxs-lookup"><span data-stu-id="7ace6-126">Use the [HTML entity code](http://www.ascii.cl/htmlcodes.htm) for the character (for example, `&#42;` for a &#42;).</span></span>

## <a name="file-names"></a><span data-ttu-id="7ace6-127">ファイル名</span><span class="sxs-lookup"><span data-stu-id="7ace6-127">File names</span></span>

<span data-ttu-id="7ace6-128">ファイル名では次の規則が使用されます。</span><span class="sxs-lookup"><span data-stu-id="7ace6-128">File names use the following rules:</span></span>

* <span data-ttu-id="7ace6-129">小文字、数字、ハイフンのみを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="7ace6-129">Contain only lowercase letters, numbers, and hyphens.</span></span>
* <span data-ttu-id="7ace6-130">空白や句読点は使用できません。</span><span class="sxs-lookup"><span data-stu-id="7ace6-130">No spaces or punctuation characters.</span></span> <span data-ttu-id="7ace6-131">ファイル名の単語と数値はハイフンを使用して区切ります。</span><span class="sxs-lookup"><span data-stu-id="7ace6-131">Use the hyphens to separate words and numbers in the file name.</span></span>
* <span data-ttu-id="7ace6-132">動作を示す固有の動詞を使用します。develop、buy、build、troubleshoot などです。</span><span class="sxs-lookup"><span data-stu-id="7ace6-132">Use action verbs that are specific, such as develop, buy, build, troubleshoot.</span></span> <span data-ttu-id="7ace6-133">進行形は使用しません。</span><span class="sxs-lookup"><span data-stu-id="7ace6-133">No -ing words.</span></span>
* <span data-ttu-id="7ace6-134">スモール ワード (a、and、the、in、or など) を含めてはなりません。</span><span class="sxs-lookup"><span data-stu-id="7ace6-134">No small words - don't include a, and, the, in, or, etc.</span></span>
* <span data-ttu-id="7ace6-135">Markdown フォーマットで、.md ファイル拡張子を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7ace6-135">Must be in Markdown and use the .md file extension.</span></span>
* <span data-ttu-id="7ace6-136">ファイル名は無理のない範囲で短くします。</span><span class="sxs-lookup"><span data-stu-id="7ace6-136">Keep file names reasonably short.</span></span> <span data-ttu-id="7ace6-137">ファイル名は記事の URL の一部になります。</span><span class="sxs-lookup"><span data-stu-id="7ace6-137">They are part of the URL for your articles.</span></span>

## <a name="headings"></a><span data-ttu-id="7ace6-138">見出し</span><span class="sxs-lookup"><span data-stu-id="7ace6-138">Headings</span></span>

<span data-ttu-id="7ace6-139">文章スタイルで大文字と小文字を使い分けます。</span><span class="sxs-lookup"><span data-stu-id="7ace6-139">Use sentence-style capitalization.</span></span> <span data-ttu-id="7ace6-140">見出しの最初の文字は必ず大文字にします。</span><span class="sxs-lookup"><span data-stu-id="7ace6-140">Always capitalize the first word of a heading.</span></span>

## <a name="text-styling"></a><span data-ttu-id="7ace6-141">テキストのスタイル設定</span><span class="sxs-lookup"><span data-stu-id="7ace6-141">Text styling</span></span>

<span data-ttu-id="7ace6-142">*斜体* ファイル、フォルダー、パス (長い項目の場合、分割してそれだけの行にします)、新しい用語に使用します。</span><span class="sxs-lookup"><span data-stu-id="7ace6-142">*Italics* Use for files, folders, paths (for long items, split onto their own line), new terms.</span></span>

<span data-ttu-id="7ace6-143">**太字** UI 要素に使用します。</span><span class="sxs-lookup"><span data-stu-id="7ace6-143">**Bold** Use for UI elements.</span></span>

<span data-ttu-id="7ace6-144">`Code` インライン コード、言語キーワード、NuGet パッケージ名、コマンドライン コマンド、データベース テーブル、列名、クリック可能にしない URL に使用します。</span><span class="sxs-lookup"><span data-stu-id="7ace6-144">`Code` Use for inline code, language keywords, NuGet package names, command-line commands, database table and column names, and URLs that you don't want to be clickable.</span></span>

## <a name="links"></a><span data-ttu-id="7ace6-145">リンク</span><span class="sxs-lookup"><span data-stu-id="7ace6-145">Links</span></span>

<span data-ttu-id="7ace6-146">アンカー、内部リンク、他のドキュメントのリンク、コード インクルード、外部リンクに関する詳細については、[リンク](how-to-write-links.md)に関する全般記事をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="7ace6-146">See the general article on [Links](how-to-write-links.md) for information about anchors, internal links, links to other documents, code includes, and external links.</span></span>

<span data-ttu-id="7ace6-147">.NET ドキュメント チームでは次の規則に従っています。</span><span class="sxs-lookup"><span data-stu-id="7ace6-147">The .NET docs team uses the following conventions:</span></span>

- <span data-ttu-id="7ace6-148">ほとんどの場合、相対リンクを使用し、リンクに `~/` を使用することは奨励していません。相対リンクは GitHub のソースで解決されるためです。</span><span class="sxs-lookup"><span data-stu-id="7ace6-148">In most cases, we use the relative links and discourage the use of `~/` in links because relative links resolve in the source on GitHub.</span></span> <span data-ttu-id="7ace6-149">ただし、依存レポジトリのファイルにリンクするときは必ず `~/` 文字を使用してパスを指定します。</span><span class="sxs-lookup"><span data-stu-id="7ace6-149">However, whenever we link to a file in a dependent repo, we'll use the `~/` character to provide the path.</span></span> <span data-ttu-id="7ace6-150">依存レポジトリのファイルは GitHub の別の場所にあるため、記述方法に関係なく、相対リンクでは正しく解決されません。</span><span class="sxs-lookup"><span data-stu-id="7ace6-150">Because the files in the dependent repo are in a different location in GitHub the links won't resolve correctly with relative links regardless of how they were written.</span></span>
- <span data-ttu-id="7ace6-151">C# 言語仕様と Visual Basic 言語仕様は、言語リポジトリからソースを含めることにより .NET ドキュメントに含められます。</span><span class="sxs-lookup"><span data-stu-id="7ace6-151">The C# language specification and the Visual Basic language specification are included in the .NET docs by including the source from the language repositories.</span></span> <span data-ttu-id="7ace6-152">Markdown ソースは [csharplang](https://github.com/dotnet/csharplang) リポジトリと [vblang](https://github.com/dotnet/vblang) リポジトリで管理されます。</span><span class="sxs-lookup"><span data-stu-id="7ace6-152">The markdown sources are managed in the [csharplang](https://github.com/dotnet/csharplang) and [vblang](https://github.com/dotnet/vblang) repositories.</span></span>

<span data-ttu-id="7ace6-153">仕様のリンクは、その仕様が含まれるソース ディレクトリを指す必要があります。</span><span class="sxs-lookup"><span data-stu-id="7ace6-153">Links to the spec must point to the source directories where those specs are included.</span></span> <span data-ttu-id="7ace6-154">以下の例にあるとおり、C# の場合は **~/_csharplang/spec** であり、VB の場合は **~/_vblang/spec** です。</span><span class="sxs-lookup"><span data-stu-id="7ace6-154">For C#, it's **~/_csharplang/spec** and for VB, it's **~/_vblang/spec**, as in the following example:</span></span>

```markdown
[C# Query Expressions](~/_csharplang/spec/expressions.md#query-expressions)
```

### <a name="links-to-apis"></a><span data-ttu-id="7ace6-155">API のリンク</span><span class="sxs-lookup"><span data-stu-id="7ace6-155">Links to APIs</span></span>

<span data-ttu-id="7ace6-156">このビルド システムには、外部リンクを使用しなくても .NET API にリンクできる拡張機能があります。</span><span class="sxs-lookup"><span data-stu-id="7ace6-156">The build system has some extensions that allow us to link to .NET APIs without having to use external links.</span></span> <span data-ttu-id="7ace6-157">次のいずれかの構文を使用します。</span><span class="sxs-lookup"><span data-stu-id="7ace6-157">You use one of the following syntax:</span></span>

1. <span data-ttu-id="7ace6-158">自動リンク: `<xref:UID>` または `<xref:UID?displayProperty=nameWithType>`</span><span class="sxs-lookup"><span data-stu-id="7ace6-158">Auto-link: `<xref:UID>` or `<xref:UID?displayProperty=nameWithType>`</span></span>

   <span data-ttu-id="7ace6-159">`displayProperty` クエリ パラメーターは、完全修飾のリンク テキストを生成します。</span><span class="sxs-lookup"><span data-stu-id="7ace6-159">The `displayProperty` query parameter produces a fully qualified link text.</span></span> <span data-ttu-id="7ace6-160">既定では、リンク テキストに表示されるのはメンバー名または型名のみです。</span><span class="sxs-lookup"><span data-stu-id="7ace6-160">By default, link text shows only the member or type name.</span></span>

2. <span data-ttu-id="7ace6-161">マークダウン リンク: `[link text](xref:UID)`</span><span class="sxs-lookup"><span data-stu-id="7ace6-161">Markdown link: `[link text](xref:UID)`</span></span>

   <span data-ttu-id="7ace6-162">表示されるリンク テキストをカスタマイズする場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="7ace6-162">Use when you want to customize the link text displayed.</span></span>

<span data-ttu-id="7ace6-163">例:</span><span class="sxs-lookup"><span data-stu-id="7ace6-163">Examples:</span></span>

- <span data-ttu-id="7ace6-164">`<xref:System.String>` は [String](https://docs.microsoft.com/dotnet/api/system.string) としてレンダリングされます</span><span class="sxs-lookup"><span data-stu-id="7ace6-164">`<xref:System.String>` renders as [String](https://docs.microsoft.com/dotnet/api/system.string)</span></span>
- <span data-ttu-id="7ace6-165">`<xref:System.String?displayProperty=nameWithType>` は [System.String](https://docs.microsoft.com/dotnet/api/system.string) としてレンダリングされます</span><span class="sxs-lookup"><span data-stu-id="7ace6-165">`<xref:System.String?displayProperty=nameWithType>` renders as [System.String](https://docs.microsoft.com/dotnet/api/system.string)</span></span>
- <span data-ttu-id="7ace6-166">`[String class](xref:System.String)` は [String class](https://docs.microsoft.com/dotnet/api/system.string) としてレンダリングされます</span><span class="sxs-lookup"><span data-stu-id="7ace6-166">`[String class](xref:System.String)` renders as [String class](https://docs.microsoft.com/dotnet/api/system.string)</span></span>

<span data-ttu-id="7ace6-167">この表記の使用について詳しくは、「[Using cross reference](https://dotnet.github.io/docfx/tutorial/links_and_cross_references.html#using-cross-reference)」(相互参照の使用) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7ace6-167">For more information about using this notation, see [Using cross reference](https://dotnet.github.io/docfx/tutorial/links_and_cross_references.html#using-cross-reference).</span></span>

<span data-ttu-id="7ace6-168">一部の UID には特殊文字 \`、\#、\* が含まれています。UID の値は、それぞれ `%60`、`%23`、`%2A` のように HTML エンコードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7ace6-168">Some UIDs contain the special characters \`, \# or \*, the UID value needs to be HTML encoded as `%60`, `%23` and `%2A` respectively.</span></span> <span data-ttu-id="7ace6-169">かっこがエンコードされている場合もありますが、これは必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="7ace6-169">You'll sometimes see parentheses encoded but it's not a requirement.</span></span>

<span data-ttu-id="7ace6-170">例:</span><span class="sxs-lookup"><span data-stu-id="7ace6-170">Examples:</span></span>

- <span data-ttu-id="7ace6-171">System.Threading.Tasks.Task\`1 は、`System.Threading.Tasks.Task%601` になります</span><span class="sxs-lookup"><span data-stu-id="7ace6-171">System.Threading.Tasks.Task\`1 becomes `System.Threading.Tasks.Task%601`</span></span>
- <span data-ttu-id="7ace6-172">System.Exception.\#ctor は、`System.Exception.%23ctor` になります</span><span class="sxs-lookup"><span data-stu-id="7ace6-172">System.Exception.\#ctor becomes `System.Exception.%23ctor`</span></span>
- <span data-ttu-id="7ace6-173">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) は、`System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29` になります</span><span class="sxs-lookup"><span data-stu-id="7ace6-173">System.Lazy\`1.\#ctor(System.Threading.LazyThreadSafetyMode) becomes  `System.Lazy%601.%23ctor%28System.Threading.LazyThreadSafetyMode%29`</span></span>

<span data-ttu-id="7ace6-174">型の UID、メンバー オーバーロード、特定のオーバーロードされたメンバーを `https://xref.docs.microsoft.com/autocomplete` から見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="7ace6-174">You can find the UIDs of types, a member overload list, or a particular overloaded member from `https://xref.docs.microsoft.com/autocomplete`.</span></span> <span data-ttu-id="7ace6-175">クエリ文字列 `?text=*\<type-member-name>*` では、UID を確認する型またはメンバーが特定されます。</span><span class="sxs-lookup"><span data-stu-id="7ace6-175">The query string `?text=*\<type-member-name>*` identifies the type or member whose UIDs you'd like to see.</span></span> <span data-ttu-id="7ace6-176">たとえば、`https://xref.docs.microsoft.com/autocomplete?text=string.format` の場合、[String.Format](https://docs.microsoft.com/dotnet/api/system.string.format) オーバーロードが取得されます。</span><span class="sxs-lookup"><span data-stu-id="7ace6-176">For example, `https://xref.docs.microsoft.com/autocomplete?text=string.format` retrieves the [String.Format](https://docs.microsoft.com/dotnet/api/system.string.format) overloads.</span></span> <span data-ttu-id="7ace6-177">このツールでは、指定された `text` クエリ パラメーターが UID のあらゆる部分で検索されます。</span><span class="sxs-lookup"><span data-stu-id="7ace6-177">The tool searches for the provided `text` query parameter in any part of the UID.</span></span> <span data-ttu-id="7ace6-178">たとえば、メンバー名 (ToString)、部分的なメンバー名 (ToStri)、型とメンバーの名前 (Double.ToString) などを検索できます。</span><span class="sxs-lookup"><span data-stu-id="7ace6-178">For example, you can search for member name (ToString), partial member name (ToStri), type and member name (Double.ToString), etc.</span></span>

<span data-ttu-id="7ace6-179">UID の後ろに \* (または `%2A`) を追加すると、リンクは固有の API ではなく、オーバーロードのページを表すようになります。</span><span class="sxs-lookup"><span data-stu-id="7ace6-179">If you add a \* (or `%2A`) after the UID, the link then represents the overload page and not a specific API.</span></span> <span data-ttu-id="7ace6-180">これはたとえば、[List\<T>.BinarySearch(T, IComparer\<T>)](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch#System_Collections_Generic_List_1_BinarySearch__0_) のような固有のオーバーロードではなく、[List\<T>.BinarySearch Method](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch) ページに汎用的な方法でリンクする必要がある場合に使用できます。</span><span class="sxs-lookup"><span data-stu-id="7ace6-180">For example, you can use that when you want to link to the [List\<T>.BinarySearch Method](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch) page in a generic way instead of a specific overload such as [List\<T>.BinarySearch(T, IComparer\<T>)](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1.binarysearch#System_Collections_Generic_List_1_BinarySearch__0_).</span></span> <span data-ttu-id="7ace6-181">メンバーがオーバーロードされていないとき、\* を使用してメンバー ページにリンクすることもできます。それにより、UID にパラメーターの一覧を含める必要がなくなります。</span><span class="sxs-lookup"><span data-stu-id="7ace6-181">You can also use \* to link to a member page when the member is not overloaded; this saves you from having to include the parameter list in the UID.</span></span>

<span data-ttu-id="7ace6-182">特定のメソッド オーバーロードにリンクするには、メソッドの各パラメーターの完全修飾型名を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="7ace6-182">To link to a specific method overload, you must include the fully qualified type name of each of the method's parameters.</span></span> <span data-ttu-id="7ace6-183">たとえば、\<xref:System.DateTime.ToString> はパラメーターなしの [DateTime.ToString](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString) メソッドにリンクされますが、\<xref:System.DateTime.ToString(System.String,System.IFormatProvider)> は [DateTime.ToString(String,IFormatProvider)](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString_System_String_System_IFormatProvider_) メソッドにリンクされます。</span><span class="sxs-lookup"><span data-stu-id="7ace6-183">For example, \<xref:System.DateTime.ToString> links to the parameterless [DateTime.ToString](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString) method, while \<xref:System.DateTime.ToString(System.String,System.IFormatProvider)> links to the  [DateTime.ToString(String,IFormatProvider)](https://docs.microsoft.com/dotnet/api/system.datetime.tostring#System_DateTime_ToString_System_String_System_IFormatProvider_) method.</span></span>

<span data-ttu-id="7ace6-184">[System.Collections.Generic.List\<T>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1) など、ジェネリック型にリンクするには、\` (`%60`) 文字にジェネリック型パラメーターの番号を続けます。</span><span class="sxs-lookup"><span data-stu-id="7ace6-184">To link to a generic type, such as [System.Collections.Generic.List\<T>](https://docs.microsoft.com/dotnet/api/system.collections.generic.list-1), you use the \` (`%60`) character followed by the number of generic type parameters.</span></span> <span data-ttu-id="7ace6-185">たとえば、`<xref:System.Nullable%601>` は [System.Nullable\<T>](https://docs.microsoft.com/dotnet/api/system.nullable-1) 型にリンクされますが、`<xref:System.Func%602>` [System.Func\<T,TResult>](https://docs.microsoft.com/dotnet/api/system.func-2) デリゲートにリンクされます。</span><span class="sxs-lookup"><span data-stu-id="7ace6-185">For example, `<xref:System.Nullable%601>` links to the [System.Nullable\<T>](https://docs.microsoft.com/dotnet/api/system.nullable-1) type, while `<xref:System.Func%602>` links to the [System.Func\<T,TResult>](https://docs.microsoft.com/dotnet/api/system.func-2) delegate.</span></span>

## <a name="code"></a><span data-ttu-id="7ace6-186">コード</span><span class="sxs-lookup"><span data-stu-id="7ace6-186">Code</span></span>

<span data-ttu-id="7ace6-187">コードを含める最良の方法は、動作するサンプルからの抜粋を含めることです。</span><span class="sxs-lookup"><span data-stu-id="7ace6-187">The best way to include code is to include snippets from a working sample.</span></span> <span data-ttu-id="7ace6-188">[.NET に協力する](dotnet-contribute-process.md#contributing-to-samples)方法に関する記事の指示に従い、サンプルを作成します。</span><span class="sxs-lookup"><span data-stu-id="7ace6-188">Create your sample following the instructions in the [contributing to .NET](dotnet-contribute-process.md#contributing-to-samples) article.</span></span> <span data-ttu-id="7ace6-189">コードを含める基本的規則は、[コード](how-to-write-use-markdown.md#code-snippets)の一般的なガイダンスにあります。</span><span class="sxs-lookup"><span data-stu-id="7ace6-189">The basic rules for including code are located in the general guidance on [code](how-to-write-use-markdown.md#code-snippets).</span></span>

<span data-ttu-id="7ace6-190">次の構文でコードを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="7ace6-190">You can include the code using the following syntax:</span></span>

```markdown
[!code-<language>[<name>](<pathToFile><queryoption><queryoptionvalue>)]
```

* <span data-ttu-id="7ace6-191">`-<language>` (*省略可能*ですが、実施することを*お勧めします*)</span><span class="sxs-lookup"><span data-stu-id="7ace6-191">`-<language>` (*optional* but *recommended*)</span></span>
  * <span data-ttu-id="7ace6-192">参照されているコード スニペットの言語。</span><span class="sxs-lookup"><span data-stu-id="7ace6-192">Language of the code snippet being referenced.</span></span>

* <span data-ttu-id="7ace6-193">`<name>` (*省略可能*)</span><span class="sxs-lookup"><span data-stu-id="7ace6-193">`<name>` (*optional*)</span></span>
  * <span data-ttu-id="7ace6-194">コード スニペットの名前。</span><span class="sxs-lookup"><span data-stu-id="7ace6-194">Name for the code snippet.</span></span> <span data-ttu-id="7ace6-195">出力 HTML には影響はありませんが、これを使用して Markdown ソースの読みやすさを向上させることができます。</span><span class="sxs-lookup"><span data-stu-id="7ace6-195">It doesn’t have any impact on the output HTML, but you can use it to improve the readability of your Markdown source.</span></span>

* <span data-ttu-id="7ace6-196">`<pathToFile>` (*必須*)</span><span class="sxs-lookup"><span data-stu-id="7ace6-196">`<pathToFile>` (*mandatory*)</span></span>
  * <span data-ttu-id="7ace6-197">参照するコード スニペット ファイルを示すファイル システムの相対パス。</span><span class="sxs-lookup"><span data-stu-id="7ace6-197">Relative path in the file system that indicates the code snippet file to reference.</span></span> <span data-ttu-id="7ace6-198">これは .NET ドキュメント セットを構成するさまざまなレポジトリによって複雑になることがあります。</span><span class="sxs-lookup"><span data-stu-id="7ace6-198">This can be complicated by the different repos that make up the .NET doc set.</span></span> <span data-ttu-id="7ace6-199">.NET サンプルは dotnet/samples レポジトリにあります。</span><span class="sxs-lookup"><span data-stu-id="7ace6-199">The .NET samples are in the dotnet/samples repo.</span></span> <span data-ttu-id="7ace6-200">すべてのスニペット パスは `~/samples` から始まり、パスの残りの部分はそのリポジトリのルートからソースまでのパスとなります。</span><span class="sxs-lookup"><span data-stu-id="7ace6-200">All snippet paths would start with `~/samples`, the rest of the path being the path to the source from the root of that repo.</span></span>

* <span data-ttu-id="7ace6-201">`<queryoption>` (*省略可能*)</span><span class="sxs-lookup"><span data-stu-id="7ace6-201">`<queryoption>` (*optional*)</span></span>
  * <span data-ttu-id="7ace6-202">ファイルからコードを取得する方法を指定するために使用。</span><span class="sxs-lookup"><span data-stu-id="7ace6-202">Used to specify how the code should be retrieved from the file:</span></span>
    * <span data-ttu-id="7ace6-203">`#`: `#{tagname}` (タグ名) *または* `#L{startlinenumber}-L{endlinenumber}` (行の範囲)。</span><span class="sxs-lookup"><span data-stu-id="7ace6-203">`#`:  `#{tagname}` (tag name) *or* `#L{startlinenumber}-L{endlinenumber}` (line range).</span></span>
    <span data-ttu-id="7ace6-204">行番号は非常に崩れやすいため、使用はお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="7ace6-204">We discourage the use of line numbers because they are very brittle.</span></span> <span data-ttu-id="7ace6-205">コード スニペットを参照する方法としてはタグ名をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="7ace6-205">Tag name is the preferred way of referencing code snippets.</span></span> <span data-ttu-id="7ace6-206">タグ名には意味のある名前を使用します。</span><span class="sxs-lookup"><span data-stu-id="7ace6-206">Use meaningful tag names.</span></span> <span data-ttu-id="7ace6-207">(スニペットの多くは前のプラットフォームから移行されており、タグには `Snippet1` や `Snippet2` のような名前が付けられています。この方法では保守管理が難しくなります。)</span><span class="sxs-lookup"><span data-stu-id="7ace6-207">(Many snippets were migrated from a previous platform and the tags have names such as `Snippet1`, `Snippet2` etc. That practice is much harder to maintain.)</span></span>
    * <span data-ttu-id="7ace6-208">`range`:　`?range=1,3-5` 行の範囲です。</span><span class="sxs-lookup"><span data-stu-id="7ace6-208">`range`: `?range=1,3-5` A range of lines.</span></span> <span data-ttu-id="7ace6-209">この例には、1、3、4、5 行が含まれます。</span><span class="sxs-lookup"><span data-stu-id="7ace6-209">This example includes lines 1, 3, 4, and 5.</span></span>

<span data-ttu-id="7ace6-210">可能な限り、タグ名を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="7ace6-210">We recommend using the tag name option whenever possible.</span></span> <span data-ttu-id="7ace6-211">タグ名はリージョンまたはコード コメントの名前であり、ソース コードでは `Snippettagname` の形式で確認できます。</span><span class="sxs-lookup"><span data-stu-id="7ace6-211">The tag name is the name of a region or of a code comment in the format of `Snippettagname` present in the source code.</span></span> <span data-ttu-id="7ace6-212">次の例は、タグ名 `BasicThrow` を参照する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="7ace6-212">The following example shows how to refer to the tag name `BasicThrow`:</span></span>

```markdown
[!code-csharp[csrefKeyword#1](~/samples/snippets/snippets/csharp/language-reference/operators/ConditionalExamples.csConditionalRef)]
```

<span data-ttu-id="7ace6-213">**dotnet/samples** レポジトリのソースの相対パスは `~/samples` パスに従います。</span><span class="sxs-lookup"><span data-stu-id="7ace6-213">The relative path to the source in the **dotnet/samples** repo follows the `~/samples` path.</span></span>

<span data-ttu-id="7ace6-214">また、[このソース ファイル](https://github.com/dotnet/samples/blob/master/snippets/csharp/language-reference/operators/ConditionalExamples.cs)でスニペット タグの構造を確認できます。</span><span class="sxs-lookup"><span data-stu-id="7ace6-214">And you can see how the snippet tags are structured in [this source file](https://github.com/dotnet/samples/blob/master/snippets/csharp/language-reference/operators/ConditionalExamples.cs).</span></span> <span data-ttu-id="7ace6-215">言語別のコード スニペット ソース ファイルでのタグ名表現の詳細については、[DocFX ガイドライン](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#tag-name-representation-in-code-snippet-source-file)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7ace6-215">For details about tag name representation in code snippet source files by language, see the [DocFX guidelines](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#tag-name-representation-in-code-snippet-source-file).</span></span>

<span data-ttu-id="7ace6-216">次の例は、3 つすべての .NET 言語に含まれるコードを示しています。</span><span class="sxs-lookup"><span data-stu-id="7ace6-216">The following example shows code included in all three .NET languages:</span></span>

```markdown
[!code-fsharp[ToPigLatin](../../../samples/snippets/fsharp/getting-started/pig-latin.fs#L1-L14)]
 [!code-csharp[ADCreateDomain#2](../../../samples/snippets/csharp/VS_Snippets_CLR/ADCreateDomain/CS/source2.cs#2)]
 [!code-vb[ADCreateDomain#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR/ADCreateDomain/VB/source2.vb#2)]  
```

<span data-ttu-id="7ace6-217">完全なプログラムからのスニペットを含めることで、すべてのコードが Microsoft の継続的インテグレーション (CI) システムで実行されます。</span><span class="sxs-lookup"><span data-stu-id="7ace6-217">Including snippets from full programs ensures that all code runs through our Continuous Integration (CI) system.</span></span> <span data-ttu-id="7ace6-218">ただし、コンパイル タイム エラーまたはランタイム エラーの原因を表示する必要がある場合、インライン コード ブロックを使用できます。</span><span class="sxs-lookup"><span data-stu-id="7ace6-218">However, if you need to show something that causes compile time or runtime errors, you can use inline code blocks.</span></span>

## <a name="images"></a><span data-ttu-id="7ace6-219">イメージ</span><span class="sxs-lookup"><span data-stu-id="7ace6-219">Images</span></span>

### <a name="static-image-or-animated-gif"></a><span data-ttu-id="7ace6-220">静止画像またはアニメーション GIF</span><span class="sxs-lookup"><span data-stu-id="7ace6-220">Static image or animated GIF</span></span>

```markdown
![this is the alt text](../images/Logo_DotNet.png)
```

### <a name="linked-image"></a><span data-ttu-id="7ace6-221">リンク画像</span><span class="sxs-lookup"><span data-stu-id="7ace6-221">Linked image</span></span>

```markdown
[![alt text for linked image](../images/Logo_DotNet.png)](https://dot.net)
```

## <a name="videos"></a><span data-ttu-id="7ace6-222">動画</span><span class="sxs-lookup"><span data-stu-id="7ace6-222">Videos</span></span>

<span data-ttu-id="7ace6-223">現在のところ、Channel 9 動画と YouTube 動画をいずれも次の構文で埋め込むことができます。</span><span class="sxs-lookup"><span data-stu-id="7ace6-223">Currently, you can embed both Channel 9 and YouTube videos with the following syntax:</span></span>

### <a name="channel-9"></a><span data-ttu-id="7ace6-224">Channel 9</span><span class="sxs-lookup"><span data-stu-id="7ace6-224">Channel 9</span></span>

```markdown
> [!VIDEO <channel9_video_link>]
```

<span data-ttu-id="7ace6-225">動画の正しい URL を取得するには、動画フレームの下にある **[埋め込む]** タグを選択し、`<iframe>` 要素から URL をコピーします。</span><span class="sxs-lookup"><span data-stu-id="7ace6-225">To get the video's correct URL, select the **Embed** tab below the video frame, and copy the URL from the `<iframe>` element.</span></span> <span data-ttu-id="7ace6-226">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="7ace6-226">For example:</span></span>

```markdown
> [!VIDEO https://channel9.msdn.com/Blogs/dotnet/NET-Core-20-Released/player]
```

### <a name="youtube"></a><span data-ttu-id="7ace6-227">YouTube</span><span class="sxs-lookup"><span data-stu-id="7ace6-227">YouTube</span></span>

<span data-ttu-id="7ace6-228">動画の正しい URL を取得するには、動画を右クリックし、**[埋め込みコードのコピー]** を選択し、`<iframe>` 要素から URL をコピーします。</span><span class="sxs-lookup"><span data-stu-id="7ace6-228">To get the video's correct URL, right-click on the video, select **Copy Embed Code**, and copy the URL from the `<iframe>` element.</span></span>

```markdown
> [!VIDEO <youtube_video_link>]
```

<span data-ttu-id="7ace6-229">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="7ace6-229">For example:</span></span>

```markdown
> [!VIDEO https://www.youtube.com/embed/Q2mMbjw6cLA]
```

## <a name="docsmicrosoft-extensions"></a><span data-ttu-id="7ace6-230">docs.microsoft 拡張機能</span><span class="sxs-lookup"><span data-stu-id="7ace6-230">docs.microsoft extensions</span></span>

<span data-ttu-id="7ace6-231">docs.microsoft では、GitHub Flavored Markdown の追加拡張機能をいくつか用意しています。</span><span class="sxs-lookup"><span data-stu-id="7ace6-231">docs.microsoft provides a few additional extensions to GitHub Flavored Markdown.</span></span>

### <a name="checked-lists"></a><span data-ttu-id="7ace6-232">チェック済みリスト</span><span class="sxs-lookup"><span data-stu-id="7ace6-232">Checked lists</span></span>

<span data-ttu-id="7ace6-233">カスタム スタイルはリストに使用できます。</span><span class="sxs-lookup"><span data-stu-id="7ace6-233">A custom style is available for lists.</span></span> <span data-ttu-id="7ace6-234">緑のチェック マークを付けたリストをレンダリングできます。</span><span class="sxs-lookup"><span data-stu-id="7ace6-234">You can render lists with green check marks.</span></span>

```markdown
> [!div class="checklist"]
> * How to create a .NET Core app
> * How to add a reference to the Microsoft.XmlSerializer.Generator package
> * How to edit your MyApp.csproj to add dependencies
> * How to add a class and an XmlSerializer
> * How to build and run the application
```

<span data-ttu-id="7ace6-235">これは次のようにレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="7ace6-235">This renders as:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="7ace6-236">NET Core アプリの作成方法</span><span class="sxs-lookup"><span data-stu-id="7ace6-236">How to create a .NET Core app</span></span>
> * <span data-ttu-id="7ace6-237">Microsoft.XmlSerializer.Generator パッケージへの参照を追加する方法</span><span class="sxs-lookup"><span data-stu-id="7ace6-237">How to add a reference to the Microsoft.XmlSerializer.Generator package</span></span>
> * <span data-ttu-id="7ace6-238">MyApp.csproj を編集して依存関係を追加する方法</span><span class="sxs-lookup"><span data-stu-id="7ace6-238">How to edit your MyApp.csproj to add dependencies</span></span>
> * <span data-ttu-id="7ace6-239">クラスと XmlSerializer を追加する方法</span><span class="sxs-lookup"><span data-stu-id="7ace6-239">How to add a class and an XmlSerializer</span></span>
> * <span data-ttu-id="7ace6-240">アプリケーションをビルドして実行する方法</span><span class="sxs-lookup"><span data-stu-id="7ace6-240">How to build and run the application</span></span>

<span data-ttu-id="7ace6-241">[.NET Core ドキュメント](https://docs.microsoft.com/dotnet/core/additional-tools/xml-serializer-generator)で、実際に使われているチェック済みリストの例を確認できます。</span><span class="sxs-lookup"><span data-stu-id="7ace6-241">You can see an example of checked lists in action in the [.NET Core docs](https://docs.microsoft.com/dotnet/core/additional-tools/xml-serializer-generator).</span></span>

### <a name="buttons"></a><span data-ttu-id="7ace6-242">ボタン</span><span class="sxs-lookup"><span data-stu-id="7ace6-242">Buttons</span></span>

<span data-ttu-id="7ace6-243">ボタン リンク:</span><span class="sxs-lookup"><span data-stu-id="7ace6-243">Button links:</span></span>

```markdown
> [!div class="button"]
> [button links](dotnet-contribute.md)
```

<span data-ttu-id="7ace6-244">これは次のようにレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="7ace6-244">This renders as:</span></span>

> [!div class="button"]
> [<span data-ttu-id="7ace6-245">ボタン リンク</span><span class="sxs-lookup"><span data-stu-id="7ace6-245">button links</span></span>](dotnet-contribute.md)

<span data-ttu-id="7ace6-246">[Visual Studio ドキュメント](https://docs.microsoft.com/visualstudio/install/install-visual-studio#step-2---download-visual-studio)で、実際に使われているボタンの例を確認できます。</span><span class="sxs-lookup"><span data-stu-id="7ace6-246">You can see an example of buttons in action in the [Visual Studio docs](https://docs.microsoft.com/visualstudio/install/install-visual-studio#step-2---download-visual-studio).</span></span>

### <a name="step-by-steps"></a><span data-ttu-id="7ace6-247">段階的手順</span><span class="sxs-lookup"><span data-stu-id="7ace6-247">Step-by-steps</span></span>

```markdown
>[!div class="step-by-step"]
> [Pre](../docs/csharp/expression-trees-interpreting.md)
> [Next](../docs/csharp/expression-trees-translating.md)
```

<span data-ttu-id="7ace6-248">[C# ガイド](https://docs.microsoft.com/dotnet/csharp/tour-of-csharp/program-structure)で、実際に使われている段階的手順の例を確認できます。</span><span class="sxs-lookup"><span data-stu-id="7ace6-248">You can see an example of step-by-steps in action at the [C# Guide](https://docs.microsoft.com/dotnet/csharp/tour-of-csharp/program-structure).</span></span>
