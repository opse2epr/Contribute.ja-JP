---
title: ms-date-missing
description: Docs のビルドの問題 ms-date-missing に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: d7697c8449e451879c137d9d6cdf42327e597be6
ms.sourcegitcommit: f374ad2607360f46d88982b4b7ecc63d3ab08235
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/20/2019
ms.locfileid: "56431463"
---
# <a name="ms-date-missing"></a><span data-ttu-id="83188-103">ms-date-missing</span><span class="sxs-lookup"><span data-stu-id="83188-103">ms-date-missing</span></span>

<span data-ttu-id="83188-104">**準備中**</span><span class="sxs-lookup"><span data-stu-id="83188-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="83188-105">提案</span><span class="sxs-lookup"><span data-stu-id="83188-105">Suggestion</span></span>

`Missing attribute: ms.date. A freshness date is required for this content. Add a date in format MM/DD/YYYY.`

<span data-ttu-id="83188-106">この日付は "鮮度" を示すために使われます。つまり、記事の関連性、正確性、スクリーン ショットの適切さ、リンクの動作が、最後にいつ確認されたのかを示します。</span><span class="sxs-lookup"><span data-stu-id="83188-106">This date is used to indicate "freshness" - that is, when the article was last reviewed for relevance, accuracy, correct screen shots, and working links.</span></span> <span data-ttu-id="83188-107">これは、記事が "*公開*" された最後の日付とは異なります。それは `ms.date` を明示的に指定しなくてもページ上に表示されます。</span><span class="sxs-lookup"><span data-stu-id="83188-107">This is not the same as the last date the article was *published*, which will show on the page if `ms.date` is not explicitly specified.</span></span>

## <a name="resolution"></a><span data-ttu-id="83188-108">解決方法</span><span class="sxs-lookup"><span data-stu-id="83188-108">Resolution</span></span>

<span data-ttu-id="83188-109">記事が最新で、壊れたコンテンツがないことを確認した後、有効な日付を MM/DD/YYYY の形式で追加します。</span><span class="sxs-lookup"><span data-stu-id="83188-109">Confirm that the article is up-to-date with no broken content, then add a valid date in the format MM/DD/YYYY:</span></span>

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
