---
title: author-missing
description: Docs のビルドの問題 author-missing に関する説明と解決方法。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 89725dcfbd4ec266071c45a003748021b480bbc2
ms.sourcegitcommit: f374ad2607360f46d88982b4b7ecc63d3ab08235
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/20/2019
ms.locfileid: "56431532"
---
# <a name="author-missing"></a>author-missing

**準備中**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>提案

`Missing attribute: author. Add a valid GitHub ID.`

`author` 属性は、GitHub ID によって記事の作成者を識別します。 

## <a name="resolution"></a>解決方法

作成者の GitHub ID を YML ヘッダーに追加します。

```yml
---
author: meganbradley
ms.author: mbradley
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]