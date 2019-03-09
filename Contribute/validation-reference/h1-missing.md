---
title: h1-missing
description: Docs のビルドの問題 h1-missing に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: c920cc0f12a9fac41b640957d45452a7958d4b07
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459121"
---
# <a name="h1-missing"></a>h1-missing

## <a name="warning"></a>警告

`H1 is required. Use a single hash (#) followed by a space to create your top-level heading.`

H1 はマークダウン ファイル内の最初の見出しを参照します。 docs.microsoft.com に公開すると、H1 はページの上部に大きなフォントで表示されます。 H1 を作成するには、行を 1 つのハッシュ (#) とスペースで開始して、その後に見出しのテキストを続けます。

## <a name="resolution"></a>解決方法

この問題を解決するには、ご利用のファイル内の YML メタデータ ブロックの後に、H1 を最初のコンテンツとして追加します。

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

> [!NOTE]
> このルールはインクルード ファイルには適用されません。 インクルード ファイルに対して H1 の警告が表示された場合、大抵はインクルード ファイルを `includes` フォルダーに移動する必要があります。 `includes` フォルダーは、ファイル パス内の任意のレベルに置くことができます。 パスに基づいて Docs のビルドではファイルがインクルード ファイルとして認識され、H1 の検証は実行されません。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]