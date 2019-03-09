---
title: no-space-in-h1
description: Docs のビルドの問題 no-space-in-h1 に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 8c719a89e6373fb960f216a5b4ec01c6d1739a28
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427848"
---
# <a name="no-space-in-h1"></a><span data-ttu-id="48b23-103">no-space-in-h1</span><span class="sxs-lookup"><span data-stu-id="48b23-103">no-space-in-h1</span></span>

## <a name="warning"></a><span data-ttu-id="48b23-104">警告</span><span class="sxs-lookup"><span data-stu-id="48b23-104">Warning</span></span>

`A space is required after the hash (#) in H1.`

<span data-ttu-id="48b23-105">H1 はマークダウン ファイル内の最初の見出しを参照します。</span><span class="sxs-lookup"><span data-stu-id="48b23-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="48b23-106">docs.microsoft.com に公開すると、H1 はページの上部に大きなフォントで表示されます。</span><span class="sxs-lookup"><span data-stu-id="48b23-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="48b23-107">H1 を作成するには、行を 1 つのハッシュ (#) とスペースで開始して、その後に見出しのテキストを続けます。</span><span class="sxs-lookup"><span data-stu-id="48b23-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span> <span data-ttu-id="48b23-108">ハッシュの後にスペースがない場合、Docs によって H1 は認識されません。</span><span class="sxs-lookup"><span data-stu-id="48b23-108">Without the space after the hash, Docs will not recognize an H1.</span></span>

## <a name="resolution"></a><span data-ttu-id="48b23-109">解決方法</span><span class="sxs-lookup"><span data-stu-id="48b23-109">Resolution</span></span>

<span data-ttu-id="48b23-110">このエラーを修正するには、ご利用の H1 内でハッシュの後にスペースを追加します。</span><span class="sxs-lookup"><span data-stu-id="48b23-110">To fix this error, add a space after the hash in your H1.</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]