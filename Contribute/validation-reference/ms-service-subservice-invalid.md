---
title: ms-service-and-subservice-invalid
description: Docs のビルドの問題 ms-service-and-subservice-invalid に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 6a2efc5cee04d7721e7a8fe1602ca24dc09ca7fd
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713133"
---
# <a name="ms-service-and-subservice-invalid"></a><span data-ttu-id="48ba2-103">ms-service-and-subservice-invalid</span><span class="sxs-lookup"><span data-stu-id="48ba2-103">ms-service-and-subservice-invalid</span></span>

<span data-ttu-id="48ba2-104">**準備中**</span><span class="sxs-lookup"><span data-stu-id="48ba2-104">**Coming soon!**</span></span>

## <a name="warning"></a><span data-ttu-id="48ba2-105">警告</span><span class="sxs-lookup"><span data-stu-id="48ba2-105">Warning</span></span>

`Invalid value for ms.service: '{value}'.`

`Invalid value for ms.subservice: '{value}' is not valid with ms.service value '{value}'.`

<span data-ttu-id="48ba2-106">`ms.service` を使ってクラウド サービスを指定します。</span><span class="sxs-lookup"><span data-stu-id="48ba2-106">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="48ba2-107">`ms.service` に関する詳細情報を指定する場合は、必要に応じて `ms.subservice` を指定できます。</span><span class="sxs-lookup"><span data-stu-id="48ba2-107">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="48ba2-108">`ms.service` と `ms.subservice` に対する値は有効なペアである必要があります。</span><span class="sxs-lookup"><span data-stu-id="48ba2-108">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span> <span data-ttu-id="48ba2-109">`ms.service` の値が無効であるか、`ms.subservice` の値が `ms.service` と有効なペアになっていないかのどちらかです。</span><span class="sxs-lookup"><span data-stu-id="48ba2-109">Either your `ms.service` value is invalid, or your `ms.subservice` value is not a valid pair with your `ms.service`.</span></span>

## <a name="resolution"></a><span data-ttu-id="48ba2-110">解決方法</span><span class="sxs-lookup"><span data-stu-id="48ba2-110">Resolution</span></span>

<span data-ttu-id="48ba2-111">`ms.service` の値がご自分の記事に対して適切であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="48ba2-111">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="48ba2-112">次に、有効な `ms.subservice` の値を選びます。</span><span class="sxs-lookup"><span data-stu-id="48ba2-112">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="48ba2-113">有効な値は、[こちらの Microsoft 内部サイト](https://docsmetadatatool.azurewebsites.net/whitelists)にあります。</span><span class="sxs-lookup"><span data-stu-id="48ba2-113">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
