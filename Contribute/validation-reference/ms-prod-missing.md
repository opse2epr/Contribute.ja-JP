---
title: ms-prod-missing
description: Docs のビルドの問題 ms-prod-missing に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 9b3f209ca2300735210490ffd58c3ac423c44fef
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636772"
---
# <a name="ms-prod-missing"></a><span data-ttu-id="1ab09-103">ms-prod-missing</span><span class="sxs-lookup"><span data-stu-id="1ab09-103">ms-prod-missing</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="1ab09-104">提案</span><span class="sxs-lookup"><span data-stu-id="1ab09-104">Suggestion</span></span>

`Missing attribute: ms.prod. If you specify ms.technology, you must also specify ms.prod.`

<span data-ttu-id="1ab09-105">オンプレミスの製品を指定する場合は `ms.prod` を使います。</span><span class="sxs-lookup"><span data-stu-id="1ab09-105">Use `ms.prod` to specify on-premises products.</span></span> <span data-ttu-id="1ab09-106">`ms.prod` に関する詳細情報を指定する場合は、必要に応じて `ms.technology` を指定できます。ただし、`ms.technology` を指定する場合は、`ms.prod` も指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1ab09-106">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`, but if you specify `ms.technology`, you must also specify `ms.prod`.</span></span> <span data-ttu-id="1ab09-107">`ms.prod` と `ms.technology` に対する値は有効なペアである必要があります。</span><span class="sxs-lookup"><span data-stu-id="1ab09-107">The values for `ms.prod` and `ms.technology` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="1ab09-108">解決方法</span><span class="sxs-lookup"><span data-stu-id="1ab09-108">Resolution</span></span>

<span data-ttu-id="1ab09-109">指定した `ms.technology` の値がご自分の記事に対して適切かどうか確認します。</span><span class="sxs-lookup"><span data-stu-id="1ab09-109">Confirm that the `ms.technology` value you've specified is correct for your article.</span></span> <span data-ttu-id="1ab09-110">次に、`ms.technology` の有効な親となる、適切な `ms.prod` の値を追加します。</span><span class="sxs-lookup"><span data-stu-id="1ab09-110">Then add the appropriate `ms.prod` value that is a valid parent for the `ms.technology`.</span></span>

<span data-ttu-id="1ab09-111">有効な値は、[こちらの Microsoft 内部サイト](https://docsmetadatatool.azurewebsites.net/allowlists)にあります。</span><span class="sxs-lookup"><span data-stu-id="1ab09-111">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
