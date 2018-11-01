---
title: マークダウン見出し
description: マークダウン見出しの要件について説明します。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 05/03/2017
ms.openlocfilehash: 18beb815fdf7caad3e8e675e8d79853d8a5688f2
ms.sourcegitcommit: 6f1997864c000a9cd25fb9171a8f8fdb8b5b5ece
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/11/2018
ms.locfileid: "49084492"
---
# <a name="markdown-headings"></a><span data-ttu-id="a4128-103">マークダウン見出し</span><span class="sxs-lookup"><span data-stu-id="a4128-103">Markdown headings</span></span>

<span data-ttu-id="a4128-104">OPS マークダウン ファイルの見出しには、次の検証要件が適用されます。</span><span class="sxs-lookup"><span data-stu-id="a4128-104">The following validation requirements apply to headings in OPS Markdown files.</span></span>

## <a name="h1"></a><span data-ttu-id="a4128-105">H1</span><span class="sxs-lookup"><span data-stu-id="a4128-105">H1</span></span>

<span data-ttu-id="a4128-106">`H1` は、マークダウン ファイルの最初の見出しを参照します。</span><span class="sxs-lookup"><span data-stu-id="a4128-106">`H1` refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="a4128-107">docs.microsoft.com に公開すると、H1 はページの上部に大きなフォントで表示されます。</span><span class="sxs-lookup"><span data-stu-id="a4128-107">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span>

<span data-ttu-id="a4128-108">H1 を作成するには、行を 1 つのハッシュ (`#`) とスペースで開始して、その後に見出しのテキストを続けます。</span><span class="sxs-lookup"><span data-stu-id="a4128-108">An H1 is created by beginning a line with a single hash (`#`) followed by a space, then the heading text.</span></span> <span data-ttu-id="a4128-109">たとえば、この記事の H1 は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="a4128-109">For example, the H1 of this article is:</span></span>

```md
# Markdown headings
```

<span data-ttu-id="a4128-110">H1 見出しには、次の規則が適用されます。</span><span class="sxs-lookup"><span data-stu-id="a4128-110">The following rules apply to H1 headings:</span></span>

- <span data-ttu-id="a4128-111">ファイルには H1 を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="a4128-111">An H1 must be present in the file.</span></span>
- <span data-ttu-id="a4128-112">H1 は 1 つだけ含めることができます。</span><span class="sxs-lookup"><span data-stu-id="a4128-112">There can only be one H1.</span></span>
- <span data-ttu-id="a4128-113">H1 には内容が必要です。</span><span class="sxs-lookup"><span data-stu-id="a4128-113">The H1 must have content.</span></span>

  ```markdown
  # 
  This is not allowed.
  ```
- <span data-ttu-id="a4128-114">`#` と H1 の内容の間にスペースが必要です。</span><span class="sxs-lookup"><span data-stu-id="a4128-114">There must be a space between the `#` and the H1 content.</span></span> <span data-ttu-id="a4128-115">H1 にスペースがなかった場合、公開されたページで見出しとして表示されません。</span><span class="sxs-lookup"><span data-stu-id="a4128-115">An H1 with no space doesn't render as a heading on the published page.</span></span>

  ```markdown
  #This looks bad on the site.
  ```
- <span data-ttu-id="a4128-116">H1 は、YML メタデータ ヘッダーの後に来る、ファイルの最初のコンテンツにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a4128-116">The H1 must be the first content in the file after the YML metadata header.</span></span> <span data-ttu-id="a4128-117">YML ヘッダーの終端と H1 の間にコンテンツ (テキストやイメージなど) を置くことはできません。</span><span class="sxs-lookup"><span data-stu-id="a4128-117">No content, such as text or images, is allowed between the end of the YML header and the H1.</span></span>

  ```markdown
  ---
  ... YML would go here
  ---
  ![cheerful image](not-allowed.jpg)
  # This cheer is not allowed
  ```
- <span data-ttu-id="a4128-118">最上位見出し向けの HTML 要素 (`<h1>`) は使用できません。</span><span class="sxs-lookup"><span data-stu-id="a4128-118">The HTML element for first-level headings, `<h1>`, should not be used.</span></span> <span data-ttu-id="a4128-119">マークダウンの構文 (`# `) を使用します。</span><span class="sxs-lookup"><span data-stu-id="a4128-119">Use the Markdown syntax (`# `).</span></span>
- <span data-ttu-id="a4128-120">H1 は 100 文字以内にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a4128-120">The H1 should be no more than 100 characters long.</span></span> <span data-ttu-id="a4128-121">これはスタイルのガイドラインです。</span><span class="sxs-lookup"><span data-stu-id="a4128-121">This is a style guideline.</span></span>

## <a name="h2---h6"></a><span data-ttu-id="a4128-122">H2 - H6</span><span class="sxs-lookup"><span data-stu-id="a4128-122">H2 - H6</span></span>

<span data-ttu-id="a4128-123">OPS では H2 (`## `) から H6 (`###### `) までを使用できます。</span><span class="sxs-lookup"><span data-stu-id="a4128-123">H2 (`## `) through H6 (`###### `) are allowed in OPS.</span></span> <span data-ttu-id="a4128-124">HTML (`<h2>` - `<h6>`) ではなくマークダウン ヘッダーを使用して、見出しを作成します。</span><span class="sxs-lookup"><span data-stu-id="a4128-124">Use the Markdown headers, not the HTML (`<h2>` - `<h6>`), to create headings.</span></span>
