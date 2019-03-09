---
title: external-bookmark-not-found
description: Docs のビルドの問題 external-bookmark-not-found に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: b533a463ac38d6445ab84c74bf14b2065a0a63f3
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427771"
---
# <a name="external-bookmark-not-found"></a>external-bookmark-not-found

## <a name="warning"></a>警告

`File '{file name}' doesn't contain a bookmark named '{bookmark text}'.`

存在しない別のファイル内の見出しにリンクしようとしています。

## <a name="resolution"></a>解決方法

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

リンク先のファイルを確認し、そのファイル内の有効なセクションを指すブックマーク リンクを更新します。

別の記事にあるセクション見出しにリンクするには、ファイル相対リンクまたはサイト相対リンクに加えてハッシュ記号使用し、その後に見出し語を続けます。 見出しから句読点を削除し、スペースをダッシュに置き換えます。 例を次に示します。

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
