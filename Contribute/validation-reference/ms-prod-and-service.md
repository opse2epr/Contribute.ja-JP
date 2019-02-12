---
title: ms-prod-and-service
description: Docs のビルドの問題 ms-prod-and-service に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 42e6f063c8b3d97386b2655b49a19a3e103d6b3b
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713202"
---
# <a name="ms-prod-and-service"></a>ms-prod-and-service

**準備中**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>提案

`Both ms.prod and ms.service can't be specified. Use ms.prod for on-premise products, or ms.service for cloud services.`

## <a name="resolution"></a>解決方法

`ms.prod`、`ms.service` のどちらかが必要であり、両方を使うことはできません。オンプレミスの製品に対しては `ms.prod` を使い、クラウド サービスに対しては `ms.service` を使います。 ご自分の記事に対してどちらが適切か判断し、値が適切であることを確認して、その他のフィールドを削除します。

有効な値は、[こちらの Microsoft 内部サイト](https://docsmetadatatool.azurewebsites.net/whitelists)にあります。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
