---
title: h1-empty
description: Docs のビルドの問題 h1-empty に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: bb07235f7cd1ba6d45418c48a4190255bdd9a428
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427688"
---
# <a name="h1-empty"></a><span data-ttu-id="67892-103">h1-empty</span><span class="sxs-lookup"><span data-stu-id="67892-103">h1-empty</span></span>

## <a name="warning"></a><span data-ttu-id="67892-104">警告</span><span class="sxs-lookup"><span data-stu-id="67892-104">Warning</span></span>

`H1 is required. Add content to your top-level heading.`

<span data-ttu-id="67892-105">H1 はマークダウン ファイル内の最初の見出しを参照します。</span><span class="sxs-lookup"><span data-stu-id="67892-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="67892-106">docs.microsoft.com に公開すると、H1 はページの上部に大きなフォントで表示されます。</span><span class="sxs-lookup"><span data-stu-id="67892-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="67892-107">H1 を作成するには、行を 1 つのハッシュ (#) とスペースで開始して、その後に見出しのテキストを続けます。</span><span class="sxs-lookup"><span data-stu-id="67892-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span>

## <a name="resolution"></a><span data-ttu-id="67892-108">解決方法</span><span class="sxs-lookup"><span data-stu-id="67892-108">Resolution</span></span>

<span data-ttu-id="67892-109">この問題を解決するには、ご利用の H1 に、ハッシュだけでなくコンテンツも必ず含めます。</span><span class="sxs-lookup"><span data-stu-id="67892-109">To fix this issue, make sure your H1 includes content, not just a hash.</span></span>

<span data-ttu-id="67892-110">悪い: </span><span class="sxs-lookup"><span data-stu-id="67892-110">Bad:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
#
This is not an H1
```

<span data-ttu-id="67892-111">良い: </span><span class="sxs-lookup"><span data-stu-id="67892-111">Good:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]