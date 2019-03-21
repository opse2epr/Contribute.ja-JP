---
title: ms-service-missing
description: Docs のビルドの問題 ms-service-missing に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 7c5860d9ef50598ad5b3e9546100af0ba436e69f
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987723"
---
# <a name="ms-service-missing"></a><span data-ttu-id="20898-103">ms-service-missing</span><span class="sxs-lookup"><span data-stu-id="20898-103">ms-service-missing</span></span>

<span data-ttu-id="20898-104">**準備中**</span><span class="sxs-lookup"><span data-stu-id="20898-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="20898-105">提案</span><span class="sxs-lookup"><span data-stu-id="20898-105">Suggestion</span></span>

`Missing attribute: ms.service. If you specify ms.subservice, you must also specify ms.service.`

<span data-ttu-id="20898-106">`ms.service` を使ってクラウド サービスを指定します。</span><span class="sxs-lookup"><span data-stu-id="20898-106">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="20898-107">`ms.service` に関する詳細情報を指定する場合は、必要に応じて `ms.subservice` を指定できます。ただし、`ms.subservice` を指定する場合は、`ms.service` も指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="20898-107">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`, but if you specify `ms.subservice`, you must also specify `ms.service`.</span></span> <span data-ttu-id="20898-108">`ms.service` と `ms.subservice` に対する値は有効なペアである必要があります。</span><span class="sxs-lookup"><span data-stu-id="20898-108">The values for `ms.service` and `ms.subservice` must be a valid pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="20898-109">解決方法</span><span class="sxs-lookup"><span data-stu-id="20898-109">Resolution</span></span>

<span data-ttu-id="20898-110">指定した `ms.subservice` の値がご自分の記事に対して適切かどうか確認します。</span><span class="sxs-lookup"><span data-stu-id="20898-110">Confirm that the `ms.subservice` value you've specified is correct for your article.</span></span> <span data-ttu-id="20898-111">次に、`ms.subservice` の有効な親となる、適切な `ms.service` の値を追加します。</span><span class="sxs-lookup"><span data-stu-id="20898-111">Then add the appropriate `ms.service` value that is a valid parent for the `ms.subservice`.</span></span>

<span data-ttu-id="20898-112">有効な値は、[こちらの Microsoft 内部サイト](https://docsmetadatatool.azurewebsites.net/allowlists)にあります。</span><span class="sxs-lookup"><span data-stu-id="20898-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
