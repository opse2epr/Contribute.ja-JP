---
title: ms-prod-or-service-missing
description: Docs のビルドの問題 ms-prod-or-service-missing に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/20/2018
ms.prod: non-product-specific
ms.openlocfilehash: f4d5bc7537ec851ce7ac1de3be2208fd74cbe37f
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713547"
---
# <a name="ms-prod-or-service-missing"></a><span data-ttu-id="b4b60-103">ms-prod-or-service-missing</span><span class="sxs-lookup"><span data-stu-id="b4b60-103">ms-prod-or-service-missing</span></span>

<span data-ttu-id="b4b60-104">**準備中**</span><span class="sxs-lookup"><span data-stu-id="b4b60-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="b4b60-105">提案</span><span class="sxs-lookup"><span data-stu-id="b4b60-105">Suggestion</span></span>

`Missing attribute: either ms.prod or ms.service is required. Use ms.prod for on-premise products, or ms.service for cloud services.`

## <a name="resolution"></a><span data-ttu-id="b4b60-106">解決方法</span><span class="sxs-lookup"><span data-stu-id="b4b60-106">Resolution</span></span>

<span data-ttu-id="b4b60-107">`ms.prod`、`ms.service` のどちらかが必要であり、両方を使うことはできません。オンプレミスの製品に対しては `ms.prod` を使い、クラウド サービスに対しては `ms.service` を使います。</span><span class="sxs-lookup"><span data-stu-id="b4b60-107">Either `ms.prod` or `ms.service` is required, and they can't both be present: `ms.prod` is used for on-premises products; `ms.service` is used for cloud services.</span></span> <span data-ttu-id="b4b60-108">ご自分の記事に対してどちらが適切か判断し、値が適切であることを確認して、その他のフィールドを削除します。</span><span class="sxs-lookup"><span data-stu-id="b4b60-108">Determine which is appropriate for your article, verify that the value is correct, and remove the other field.</span></span>

<span data-ttu-id="b4b60-109">有効な値は、[こちらの Microsoft 内部サイト](https://docsmetadatatool.azurewebsites.net/whitelists)にあります。</span><span class="sxs-lookup"><span data-stu-id="b4b60-109">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]