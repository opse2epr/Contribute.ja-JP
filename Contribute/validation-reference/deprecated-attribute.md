---
title: deprecated-attribute
description: Docs のビルドの問題 deprecated-attribute に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 564bd35c418fb9def6bf20240fca64265a477f46
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987792"
---
# <a name="deprecated-attribute"></a>deprecated-attribute

**準備中**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>提案

`Deprecated attribute: ms.component. Use ms.subservice instead.`

`ms.service` を使ってクラウド サービスを指定します。 `ms.service` に関する詳細情報を指定する場合は、必要に応じて `ms.subservice` を指定できます。 `ms.component` は使用しないでください。このコンテンツでは非推奨です。

## <a name="resolution"></a>解決方法

`ms.service` の値がご自分の記事に対して適切であることを確認します。 次に、有効な `ms.subservice` の値を選びます。

有効な値は、[こちらの Microsoft 内部サイト](https://docsmetadatatool.azurewebsites.net/allowlists)にあります。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
