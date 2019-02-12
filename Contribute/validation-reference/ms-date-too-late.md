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
# <a name="ms-date-too-late"></a>ms-date-too-late

**準備中**

## <a name="warning"></a>警告

`Invalid value for ms.date. The freshness date can't be more than five days in the future.`

`ms.date` 属性は "鮮度" を示すために使われます。つまり、記事の関連性、正確性、スクリーン ショットの適切さ、リンクの動作が、最後にいつ確認されたのかを示します。 そのため、これを未来に設定することはできません。 メジャー イベントに向けた準備として QA のためにコンテンツを凍結する場合など、リリース時期を考慮するために 5 日間が許容されています。

## <a name="resolution"></a>解決方法

今日から 5 日以内の `ms.date` を、MM/DD/YYYY の形式で指定します。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
