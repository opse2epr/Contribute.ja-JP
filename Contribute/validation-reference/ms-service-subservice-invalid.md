---
title: ms-service-and-subservice-invalid
description: Docs のビルドの問題 ms-service-and-subservice-invalid に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 3f165d16eed7e937c7db912a9c5e0ee0809e3031
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637301"
---
# <a name="ms-service-and-subservice-invalid"></a><span data-ttu-id="3caad-103">ms-service-and-subservice-invalid</span><span class="sxs-lookup"><span data-stu-id="3caad-103">ms-service-and-subservice-invalid</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="3caad-104">提案</span><span class="sxs-lookup"><span data-stu-id="3caad-104">Suggestion</span></span>

`Invalid value for ms.service: '{value}'.`

`Invalid value for ms.subservice: '{value}' is not valid with ms.service value '{value}'.`

<span data-ttu-id="3caad-105">`ms.service` を使ってクラウド サービスを指定します。</span><span class="sxs-lookup"><span data-stu-id="3caad-105">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="3caad-106">`ms.service` に関する詳細情報を指定する場合は、必要に応じて `ms.subservice` を指定できます。</span><span class="sxs-lookup"><span data-stu-id="3caad-106">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="3caad-107">`ms.service` と `ms.subservice` に対する値は有効なペアである必要があります。</span><span class="sxs-lookup"><span data-stu-id="3caad-107">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span> <span data-ttu-id="3caad-108">`ms.service` の値が無効であるか、`ms.subservice` の値が `ms.service` と有効なペアになっていないかのどちらかです。</span><span class="sxs-lookup"><span data-stu-id="3caad-108">Either your `ms.service` value is invalid, or your `ms.subservice` value is not a valid pair with your `ms.service`.</span></span>

## <a name="resolution"></a><span data-ttu-id="3caad-109">解決方法</span><span class="sxs-lookup"><span data-stu-id="3caad-109">Resolution</span></span>

<span data-ttu-id="3caad-110">`ms.service` の値がご自分の記事に対して適切であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="3caad-110">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="3caad-111">次に、有効な `ms.subservice` の値を選びます。</span><span class="sxs-lookup"><span data-stu-id="3caad-111">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="3caad-112">有効な値は、[こちらの Microsoft 内部サイト](https://docsmetadatatool.azurewebsites.net/allowlists)にあります。</span><span class="sxs-lookup"><span data-stu-id="3caad-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
