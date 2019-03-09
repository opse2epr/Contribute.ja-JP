---
title: manager-missing
description: Docs のビルドの問題 manager-missing に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 3/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 16da241a21d400d5a5dfb101e247e55d95567485
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427828"
---
# <a name="manager-missing"></a>manager-missing

**準備中**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>提案

`Missing attribute: manager. Add a valid Microsoft alias for the author's manager.`

一部のコンテンツ グループには、作成者のマネージャーを識別するための `manager` 属性が必要です。

## <a name="resolution"></a>解決方法

`manager` に対して有効な Microsoft のエイリアスを追加します。

```yml
---
ms.author: mbradley
manager: jemash
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
