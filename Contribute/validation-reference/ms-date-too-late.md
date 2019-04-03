---
title: ms-date-too-late
description: Docs のビルドの問題 ms-date-too-late に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4cb5da1da2fee59302791e729e5fcfb8e84170e5
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637393"
---
# <a name="ms-date-too-late"></a><span data-ttu-id="e663b-103">ms-date-too-late</span><span class="sxs-lookup"><span data-stu-id="e663b-103">ms-date-too-late</span></span>

## <a name="warning"></a><span data-ttu-id="e663b-104">警告</span><span class="sxs-lookup"><span data-stu-id="e663b-104">Warning</span></span>

`Invalid value for ms.date. The freshness date can't be more than five days in the future.`

<span data-ttu-id="e663b-105">`ms.date` 属性は "鮮度" を示すために使われます。つまり、記事の関連性、正確性、スクリーン ショットの適切さ、リンクの動作が、最後にいつ確認されたのかを示します。</span><span class="sxs-lookup"><span data-stu-id="e663b-105">The `ms.date` attribute is used to indicate "freshness" - that is, when the article was last reviewed for relevance, accuracy, correct screen shots, and working links.</span></span> <span data-ttu-id="e663b-106">そのため、これを未来に設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="e663b-106">Therefore, it can't be in the future!</span></span> <span data-ttu-id="e663b-107">メジャー イベントに向けた準備として QA のためにコンテンツを凍結する場合など、リリース時期を考慮するために 5 日間が許容されています。</span><span class="sxs-lookup"><span data-stu-id="e663b-107">Five days are allowed to account for release time, such as when content is frozen for QA in preparation for a major event.</span></span>

## <a name="resolution"></a><span data-ttu-id="e663b-108">解決方法</span><span class="sxs-lookup"><span data-stu-id="e663b-108">Resolution</span></span>

<span data-ttu-id="e663b-109">今日から 5 日以内の `ms.date` を、MM/DD/YYYY の形式で指定します。</span><span class="sxs-lookup"><span data-stu-id="e663b-109">Specify an `ms.date` no more than five days from today, in format MM/DD/YYYY:</span></span>

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
