---
title: ms-prod-service-mismatch
description: Docs のビルドの問題 ms-prod-service-mismatch に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: a8d1698a4842ace0e5dd07db170f40a310c666a6
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636795"
---
# <a name="ms-prod-service-mismatch"></a><span data-ttu-id="293a3-103">ms-prod-service-mismatch</span><span class="sxs-lookup"><span data-stu-id="293a3-103">ms-prod-service-mismatch</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="293a3-104">提案</span><span class="sxs-lookup"><span data-stu-id="293a3-104">Suggestion</span></span>

`Invalid attribute pair: ms.prod and ms.subservice. You can only pair ms.prod with ms.technology.`

`Invalid attribute pair: ms.service and ms.technology. You can only pair ms.service with ms.subservice.`

<span data-ttu-id="293a3-105">オンプレミスの製品を指定する場合は `ms.prod` を、クラウド サービスの場合は `ms.service` を使います。</span><span class="sxs-lookup"><span data-stu-id="293a3-105">Use `ms.prod` to specify on-premises products; `ms.service` for cloud services.</span></span> <span data-ttu-id="293a3-106">`ms.prod` に関する詳細情報を指定する場合は、必要に応じて `ms.technology` を指定できます。</span><span class="sxs-lookup"><span data-stu-id="293a3-106">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`.</span></span> <span data-ttu-id="293a3-107">`ms.service` に関する詳細情報を指定する場合は、`ms.subservice` を指定できます。</span><span class="sxs-lookup"><span data-stu-id="293a3-107">To specify more detailed information about `ms.service`, you can specify `ms.subservice`.</span></span> <span data-ttu-id="293a3-108">`ms.prod` と `ms.subservice`、または `ms.service` と `ms.technology` は併用できません。</span><span class="sxs-lookup"><span data-stu-id="293a3-108">You can't use `ms.prod` with `ms.subservice` or `ms.service` with `ms.technology`.</span></span>

## <a name="resolution"></a><span data-ttu-id="293a3-109">解決方法</span><span class="sxs-lookup"><span data-stu-id="293a3-109">Resolution</span></span>

<span data-ttu-id="293a3-110">まず、ご自分の記事に対して適切な親属性 (`ms.prod` または `ms.service`) を選択したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="293a3-110">First, verify that you have selected the correct parent attribute (`ms.prod` or `ms.service`) for your article.</span></span> <span data-ttu-id="293a3-111">次に、適切な子のフィールドを、有効なペアの値と共に追加します。</span><span class="sxs-lookup"><span data-stu-id="293a3-111">Then, add the appropriate child field with a valid paired value.</span></span> <span data-ttu-id="293a3-112">余分なフィールドはすべて削除します。</span><span class="sxs-lookup"><span data-stu-id="293a3-112">Remove any extra fields.</span></span>

<span data-ttu-id="293a3-113">有効な値は、[こちらの Microsoft 内部サイト](https://docsmetadatatool.azurewebsites.net/allowlists)にあります。</span><span class="sxs-lookup"><span data-stu-id="293a3-113">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
