---
title: ms-prod-or-service-missing
description: Docs のビルドの問題 ms-prod-or-service-missing に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/20/2018
ms.prod: non-product-specific
ms.openlocfilehash: 6eeb4a95e4d4aeba527b1078bc646fcbc56898a2
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987562"
---
# <a name="ms-prod-or-service-missing"></a>ms-prod-or-service-missing

**準備中**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>提案

`Missing attribute: either ms.prod or ms.service is required. Use ms.prod for on-premise products, or ms.service for cloud services.`

## <a name="resolution"></a>解決方法

`ms.prod`、`ms.service` のどちらかが必要であり、両方を使うことはできません。オンプレミスの製品に対しては `ms.prod` を使い、クラウド サービスに対しては `ms.service` を使います。 ご自分の記事に対してどちらが適切か判断し、値が適切であることを確認して、その他のフィールドを削除します。

有効な値は、[こちらの Microsoft 内部サイト](https://docsmetadatatool.azurewebsites.net/allowlists)にあります。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]