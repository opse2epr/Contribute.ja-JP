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
# <a name="no-space-in-h1"></a>no-space-in-h1

## <a name="warning"></a>警告

`A space is required after the hash (#) in H1.`

H1 はマークダウン ファイル内の最初の見出しを参照します。 docs.microsoft.com に公開すると、H1 はページの上部に大きなフォントで表示されます。 H1 を作成するには、行を 1 つのハッシュ (#) とスペースで開始して、その後に見出しのテキストを続けます。 ハッシュの後にスペースがない場合、Docs によって H1 は認識されません。

## <a name="resolution"></a>解決方法

このエラーを修正するには、ご利用の H1 内でハッシュの後にスペースを追加します。

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]