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
# <a name="ms-date-too-late"></a>ms-date-too-late

## <a name="warning"></a>警告

`Invalid value for ms.date. The freshness date can't be more than five days in the future.`

`ms.date` 属性は "鮮度" を示すために使われます。つまり、記事の関連性、正確性、スクリーン ショットの適切さ、リンクの動作が、最後にいつ確認されたのかを示します。 そのため、これを未来に設定することはできません。 メジャー イベントに向けた準備として QA のためにコンテンツを凍結する場合など、リリース時期を考慮するために 5 日間が許容されています。

## <a name="resolution"></a>解決方法

今日から 5 日以内の `ms.date` を、MM/DD/YYYY の形式で指定します。

```yml
---
ms.date: 02/19/2019
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
