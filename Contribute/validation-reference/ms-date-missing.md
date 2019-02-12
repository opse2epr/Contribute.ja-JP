---
title: ms-date-missing
description: Docs のビルドの問題 ms-date-missing に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: f5603dee7efe5c7ce3eaa4fa944031d94a9283d8
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713248"
---
# <a name="ms-date-missing"></a>ms-date-missing

**準備中**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>提案

`Missing attribute: ms.date. A freshness date is required for this content. Add a date in format MM/DD/YYYY.`

この日付は "鮮度" を示すために使われます。つまり、記事の関連性、正確性、スクリーン ショットの適切さ、リンクの動作が、最後にいつ確認されたのかを示します。 これは、記事が "*公開*" された最後の日付とは異なります。それは `ms.date` を明示的に指定しなくてもページ上に表示されます。

## <a name="resolution"></a>解決方法

記事が最新で、壊れたコンテンツがないことを確認した後、有効な日付を MM/DD/YYYY の形式で追加します。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
