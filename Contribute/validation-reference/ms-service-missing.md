---
title: ms-service-missing
description: Docs のビルドの問題 ms-service-missing に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 2bc425726f82840565978072b2efdf13a1284ec0
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713087"
---
# <a name="ms-service-missing"></a><span data-ttu-id="fe3a6-103">ms-service-missing</span><span class="sxs-lookup"><span data-stu-id="fe3a6-103">ms-service-missing</span></span>

<span data-ttu-id="fe3a6-104">**準備中**</span><span class="sxs-lookup"><span data-stu-id="fe3a6-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="fe3a6-105">提案</span><span class="sxs-lookup"><span data-stu-id="fe3a6-105">Suggestion</span></span>

`Missing attribute: ms.service. If you specify ms.subservice, you must also specify ms.service.`

<span data-ttu-id="fe3a6-106">`ms.service` を使ってクラウド サービスを指定します。</span><span class="sxs-lookup"><span data-stu-id="fe3a6-106">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="fe3a6-107">`ms.service` に関する詳細情報を指定する場合は、必要に応じて `ms.subservice` を指定できます。ただし、`ms.subservice` を指定する場合は、`ms.service` も指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fe3a6-107">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`, but if you specify `ms.subservice`, you must also specify `ms.service`.</span></span> <span data-ttu-id="fe3a6-108">`ms.service` と `ms.subservice` に対する値は有効なペアである必要があります。</span><span class="sxs-lookup"><span data-stu-id="fe3a6-108">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="fe3a6-109">解決方法</span><span class="sxs-lookup"><span data-stu-id="fe3a6-109">Resolution</span></span>

<span data-ttu-id="fe3a6-110">指定した `ms.subservice` の値がご自分の記事に対して適切かどうか確認します。</span><span class="sxs-lookup"><span data-stu-id="fe3a6-110">Confirm that the `ms.subservice` value you've specified is correct for your article.</span></span> <span data-ttu-id="fe3a6-111">次に、`ms.subservice` の有効な親となる、適切な `ms.service` の値を追加します。</span><span class="sxs-lookup"><span data-stu-id="fe3a6-111">Then add the appropriate `ms.service` value that is a valid parent for the `ms.subservice`.</span></span>

<span data-ttu-id="fe3a6-112">有効な値は、[こちらの Microsoft 内部サイト](https://docsmetadatatool.azurewebsites.net/whitelists)にあります。</span><span class="sxs-lookup"><span data-stu-id="fe3a6-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
