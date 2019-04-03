---
title: ms-date-invalid
description: Docs のビルドの問題 ms-date-invalid に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 22b903c2a670124c272fc5b1e26088c516ded306
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637416"
---
# <a name="ms-date-invalid"></a><span data-ttu-id="2104b-103">ms-date-invalid</span><span class="sxs-lookup"><span data-stu-id="2104b-103">ms-date-invalid</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="2104b-104">提案</span><span class="sxs-lookup"><span data-stu-id="2104b-104">Suggestion</span></span>

`Invalid value for ms.date: '{value}'. Must be a date in format MM/DD/YYYY.`

## <a name="resolution"></a><span data-ttu-id="2104b-105">解決方法</span><span class="sxs-lookup"><span data-stu-id="2104b-105">Resolution</span></span>

<span data-ttu-id="2104b-106">記事が最新で、壊れたコンテンツがないことを確認した後、有効な日付を MM/DD/YYYY の形式で追加します。</span><span class="sxs-lookup"><span data-stu-id="2104b-106">Confirm that the article is up-to-date with no broken content, then add a valid date in the format MM/DD/YYYY:</span></span>

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
