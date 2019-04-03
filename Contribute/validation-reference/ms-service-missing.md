---
title: ms-service-missing
description: Docs のビルドの問題 ms-service-missing に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 17e2e272e3a21e14e038e27ff68866afe28bee60
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636703"
---
# <a name="ms-service-missing"></a><span data-ttu-id="e7645-103">ms-service-missing</span><span class="sxs-lookup"><span data-stu-id="e7645-103">ms-service-missing</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="e7645-104">提案</span><span class="sxs-lookup"><span data-stu-id="e7645-104">Suggestion</span></span>

`Missing attribute: ms.service. If you specify ms.subservice, you must also specify ms.service.`

<span data-ttu-id="e7645-105">`ms.service` を使ってクラウド サービスを指定します。</span><span class="sxs-lookup"><span data-stu-id="e7645-105">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="e7645-106">`ms.service` に関する詳細情報を指定する場合は、必要に応じて `ms.subservice` を指定できます。ただし、`ms.subservice` を指定する場合は、`ms.service` も指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e7645-106">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`, but if you specify `ms.subservice`, you must also specify `ms.service`.</span></span> <span data-ttu-id="e7645-107">`ms.service` と `ms.subservice` に対する値は有効なペアである必要があります。</span><span class="sxs-lookup"><span data-stu-id="e7645-107">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="e7645-108">解決方法</span><span class="sxs-lookup"><span data-stu-id="e7645-108">Resolution</span></span>

<span data-ttu-id="e7645-109">指定した `ms.subservice` の値がご自分の記事に対して適切かどうか確認します。</span><span class="sxs-lookup"><span data-stu-id="e7645-109">Confirm that the `ms.subservice` value you've specified is correct for your article.</span></span> <span data-ttu-id="e7645-110">次に、`ms.subservice` の有効な親となる、適切な `ms.service` の値を追加します。</span><span class="sxs-lookup"><span data-stu-id="e7645-110">Then add the appropriate `ms.service` value that is a valid parent for the `ms.subservice`.</span></span>

<span data-ttu-id="e7645-111">有効な値は、[こちらの Microsoft 内部サイト](https://docsmetadatatool.azurewebsites.net/allowlists)にあります。</span><span class="sxs-lookup"><span data-stu-id="e7645-111">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
