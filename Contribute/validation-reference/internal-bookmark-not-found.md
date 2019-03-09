---
title: internal-bookmark-not-found
description: Docs のビルドの問題 internal-bookmark-not-found に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 9073603d4e745db2f49b57a8901e00a03d8f570f
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427831"
---
# <a name="internal-bookmark-not-found"></a>internal-bookmark-not-found

**準備中**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>提案

`Current file doesn't contain a bookmark named '{bookmark}'.`

存在しない現在のファイル内の見出しにリンクしようとしています。

## <a name="resolution"></a>解決方法

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

リンクする先の見出しを確認し、リンクを更新します。

現在の記事にあるセクションにリンクするには、ハッシュ記号を使用し、その後に見出し語を続けます。 見出しから句読点を削除し、スペースをダッシュに置き換えます。 例を次に示します。

```markdown
[Managed Disks](#managed-disks)
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
