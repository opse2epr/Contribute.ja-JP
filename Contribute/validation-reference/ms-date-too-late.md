---
title: ms-date-too-late
description: Docs のビルドの問題 ms-date-too-late に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 863b13e55c2aaa2057920e3bd77ec75ab5945277
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713110"
---
# <a name="ms-date-too-late"></a><span data-ttu-id="189c7-103">ms-date-too-late</span><span class="sxs-lookup"><span data-stu-id="189c7-103">ms-date-too-late</span></span>

<span data-ttu-id="189c7-104">**準備中**</span><span class="sxs-lookup"><span data-stu-id="189c7-104">**Coming soon!**</span></span>

## <a name="warning"></a><span data-ttu-id="189c7-105">警告</span><span class="sxs-lookup"><span data-stu-id="189c7-105">Warning</span></span>

`Invalid value for ms.date. The freshness date can't be more than five days in the future.`

<span data-ttu-id="189c7-106">`ms.date` 属性は "鮮度" を示すために使われます。つまり、記事の関連性、正確性、スクリーン ショットの適切さ、リンクの動作が、最後にいつ確認されたのかを示します。</span><span class="sxs-lookup"><span data-stu-id="189c7-106">The `ms.date` attribute is used to indicate "freshness" - that is, when the article was last reviewed for relevance, accuracy, correct screen shots, and working links.</span></span> <span data-ttu-id="189c7-107">そのため、これを未来に設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="189c7-107">Therefore, it can't be in the future!</span></span> <span data-ttu-id="189c7-108">メジャー イベントに向けた準備として QA のためにコンテンツを凍結する場合など、リリース時期を考慮するために 5 日間が許容されています。</span><span class="sxs-lookup"><span data-stu-id="189c7-108">Five days are allowed to account for release time, such as when content is frozen for QA in preparation for a major event.</span></span>

## <a name="resolution"></a><span data-ttu-id="189c7-109">解決方法</span><span class="sxs-lookup"><span data-stu-id="189c7-109">Resolution</span></span>

<span data-ttu-id="189c7-110">今日から 5 日以内の `ms.date` を、MM/DD/YYYY の形式で指定します。</span><span class="sxs-lookup"><span data-stu-id="189c7-110">Specify an `ms.date` no more than five days from today, in format MM/DD/YYYY.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
