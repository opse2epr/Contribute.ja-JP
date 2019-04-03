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
# <a name="ms-prod-and-service"></a><span data-ttu-id="9c8a3-103">ms-prod-and-service</span><span class="sxs-lookup"><span data-stu-id="9c8a3-103">ms-prod-and-service</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="9c8a3-104">提案</span><span class="sxs-lookup"><span data-stu-id="9c8a3-104">Suggestion</span></span>

`Both ms.prod and ms.service can't be specified. Use ms.prod for on-premise products, or ms.service for cloud services.`

## <a name="resolution"></a><span data-ttu-id="9c8a3-105">解決方法</span><span class="sxs-lookup"><span data-stu-id="9c8a3-105">Resolution</span></span>

<span data-ttu-id="9c8a3-106">`ms.prod`、`ms.service` のどちらかが必要であり、両方を使うことはできません。オンプレミスの製品に対しては `ms.prod` を使い、クラウド サービスに対しては `ms.service` を使います。</span><span class="sxs-lookup"><span data-stu-id="9c8a3-106">Either `ms.prod` or `ms.service` is required, and they can't both be present: `ms.prod` is used for on-premises products; `ms.service` is used for cloud services.</span></span> <span data-ttu-id="9c8a3-107">ご自分の記事に対してどちらが適切か判断し、値が適切であることを確認して、その他のフィールドを削除します。</span><span class="sxs-lookup"><span data-stu-id="9c8a3-107">Determine which is appropriate for your article, verify that the value is correct, and remove the other field.</span></span>

<span data-ttu-id="9c8a3-108">有効な値は、[こちらの Microsoft 内部サイト](https://docsmetadatatool.azurewebsites.net/allowlists)にあります。</span><span class="sxs-lookup"><span data-stu-id="9c8a3-108">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
