---
title: ms-prod-and-service
description: Docs のビルドの問題 ms-prod-and-service に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 77c0dd71cf526ee837799bcd01e21290ce7d6058
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636749"
---
# <a name="ms-prod-and-service"></a>ms-prod-and-service

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>提案

`Both ms.prod and ms.service can't be specified. Use ms.prod for on-premise products, or ms.service for cloud services.`

## <a name="resolution"></a>解決方法

`ms.prod`、`ms.service` のどちらかが必要であり、両方を使うことはできません。オンプレミスの製品に対しては `ms.prod` を使い、クラウド サービスに対しては `ms.service` を使います。 ご自分の記事に対してどちらが適切か判断し、値が適切であることを確認して、その他のフィールドを削除します。

有効な値は、[こちらの Microsoft 内部サイト](https://docsmetadatatool.azurewebsites.net/allowlists)にあります。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
