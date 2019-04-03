---
title: ms-prod-and-technology-invalid
description: Docs のビルドの問題 ms-prod-and-technology-invalid に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 8c6f12629cf4b8cf7fd2471ef4d1287562435696
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636841"
---
# <a name="ms-prod-and-technology-invalid"></a><span data-ttu-id="53061-103">ms-prod-and-technology-invalid</span><span class="sxs-lookup"><span data-stu-id="53061-103">ms-prod-and-technology-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="53061-104">警告</span><span class="sxs-lookup"><span data-stu-id="53061-104">Warning</span></span>

`Invalid value for ms.prod: '{value}'.`

`Invalid value for ms.technology: '{value}' is not valid with ms.prod value '{value}'.`

<span data-ttu-id="53061-105">オンプレミスの製品を指定する場合は `ms.prod` を使います。</span><span class="sxs-lookup"><span data-stu-id="53061-105">Use `ms.prod` to specify on-premises products.</span></span> <span data-ttu-id="53061-106">`ms.prod` に関する詳細情報を指定する場合は、必要に応じて `ms.technology` を指定できます。</span><span class="sxs-lookup"><span data-stu-id="53061-106">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`.</span></span> <span data-ttu-id="53061-107">`ms.prod` と `ms.technology` に対する値は有効なペアである必要があります。</span><span class="sxs-lookup"><span data-stu-id="53061-107">The values for `ms.prod` and `ms.technology` must be a valid pair.</span></span> <span data-ttu-id="53061-108">`ms.prod` の値が無効であるか、`ms.technology` の値が `ms.prod` と有効なペアになっていないかのどちらかです。</span><span class="sxs-lookup"><span data-stu-id="53061-108">Either your `ms.prod` value is invalid, or your `ms.technology` value is not a valid pair with your `ms.prod`.</span></span>

## <a name="resolution"></a><span data-ttu-id="53061-109">解決方法</span><span class="sxs-lookup"><span data-stu-id="53061-109">Resolution</span></span>

<span data-ttu-id="53061-110">`ms.prod` の値がご自分の記事に対して適切であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="53061-110">Confirm that your `ms.prod` value is correct for your article.</span></span> <span data-ttu-id="53061-111">次に、有効な `ms.technology` の値を選びます。</span><span class="sxs-lookup"><span data-stu-id="53061-111">Then choose a valid `ms.technology` value.</span></span>

<span data-ttu-id="53061-112">有効な値は、[こちらの Microsoft 内部サイト](https://docsmetadatatool.azurewebsites.net/allowlists)にあります。</span><span class="sxs-lookup"><span data-stu-id="53061-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
