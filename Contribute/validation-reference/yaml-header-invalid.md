---
title: yaml-header-invalid
description: Docs のビルドの問題 yaml-header-invalid に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: 62b3b2c2aa47525cae5dd5c0955eb88463124359
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459029"
---
# <a name="yaml-header-invalid"></a>yaml-header-invalid

## <a name="warning"></a>警告

`Invalid YAML header: Improper use of a colon in a metadata entry.`

通常、これは、YAML ヘッダー内の引用符なしのメタデータ値にコロンまたは別の特殊文字が含まれていることを意味します。 また、キーと値のペア内のコロンの後にスペースが欠落していることを意味している場合もあります。

## <a name="resolution"></a>解決方法

ご利用の YAML ヘッダーを確認します。 次の間違いを探します。

引用符なしの値内のコロン: 

```yml
---
title: Common mistake: I included a colon in my unquoted value.
---
```

次の内容に変更: 

```yml
---
title: 'Common mistake: I included a colon in my unquoted value.'
---
```

キーと値のペア内のコロンの後にスペースがない: 

```yml
---
title:I omitted a space.
---
```

次の内容に変更: 

```yml
---
title: I omitted a space.
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
