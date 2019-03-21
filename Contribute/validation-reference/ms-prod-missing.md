---
title: ms-prod-missing
description: Docs のビルドの問題 ms-prod-missing に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 2578ab47dab315a446529d24357e9489d7fd0bad
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987700"
---
# <a name="ms-prod-missing"></a><span data-ttu-id="e2a67-103">ms-prod-missing</span><span class="sxs-lookup"><span data-stu-id="e2a67-103">ms-prod-missing</span></span>

<span data-ttu-id="e2a67-104">**準備中**</span><span class="sxs-lookup"><span data-stu-id="e2a67-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="e2a67-105">提案</span><span class="sxs-lookup"><span data-stu-id="e2a67-105">Suggestion</span></span>

`Missing attribute: ms.prod. If you specify ms.technology, you must also specify ms.prod.`

<span data-ttu-id="e2a67-106">オンプレミスの製品を指定する場合は `ms.prod` を使います。</span><span class="sxs-lookup"><span data-stu-id="e2a67-106">Use `ms.prod` to specify on-premises products.</span></span> <span data-ttu-id="e2a67-107">`ms.prod` に関する詳細情報を指定する場合は、必要に応じて `ms.technology` を指定できます。ただし、`ms.technology` を指定する場合は、`ms.prod` も指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e2a67-107">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`, but if you specify `ms.technology`, you must also specify `ms.prod`.</span></span> <span data-ttu-id="e2a67-108">`ms.prod` と `ms.technology` に対する値は有効なペアである必要があります。</span><span class="sxs-lookup"><span data-stu-id="e2a67-108">The values for `ms.prod` and `ms.technology` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="e2a67-109">解決方法</span><span class="sxs-lookup"><span data-stu-id="e2a67-109">Resolution</span></span>

<span data-ttu-id="e2a67-110">指定した `ms.technology` の値がご自分の記事に対して適切かどうか確認します。</span><span class="sxs-lookup"><span data-stu-id="e2a67-110">Confirm that the `ms.technology` value you've specified is correct for your article.</span></span> <span data-ttu-id="e2a67-111">次に、`ms.technology` の有効な親となる、適切な `ms.prod` の値を追加します。</span><span class="sxs-lookup"><span data-stu-id="e2a67-111">Then add the appropriate `ms.prod` value that is a valid parent for the `ms.technology`.</span></span>

<span data-ttu-id="e2a67-112">有効な値は、[こちらの Microsoft 内部サイト](https://docsmetadatatool.azurewebsites.net/allowlists)にあります。</span><span class="sxs-lookup"><span data-stu-id="e2a67-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
