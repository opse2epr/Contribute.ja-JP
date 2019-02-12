---
title: ms-prod-service-mismatch
description: Docs のビルドの問題 ms-prod-service-mismatch に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4a3cf8bc5435972f0442ca1d41d4147e1ea00d78
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713179"
---
# <a name="ms-prod-service-mismatch"></a><span data-ttu-id="115a5-103">ms-prod-service-mismatch</span><span class="sxs-lookup"><span data-stu-id="115a5-103">ms-prod-service-mismatch</span></span>

<span data-ttu-id="115a5-104">**準備中**</span><span class="sxs-lookup"><span data-stu-id="115a5-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="115a5-105">提案</span><span class="sxs-lookup"><span data-stu-id="115a5-105">Suggestion</span></span>

`Invalid attribute pair: ms.prod and ms.subservice. You can only pair ms.prod with ms.technology.`

`Invalid attribute pair: ms.service and ms.technology. You can only pair ms.service with ms.subservice.`

<span data-ttu-id="115a5-106">オンプレミスの製品を指定する場合は `ms.prod` を、クラウド サービスの場合は `ms.service` を使います。</span><span class="sxs-lookup"><span data-stu-id="115a5-106">Use `ms.prod` to specify on-premises products; `ms.service` for cloud services.</span></span> <span data-ttu-id="115a5-107">`ms.prod` に関する詳細情報を指定する場合は、必要に応じて `ms.technology` を指定できます。</span><span class="sxs-lookup"><span data-stu-id="115a5-107">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`.</span></span> <span data-ttu-id="115a5-108">`ms.service` に関する詳細情報を指定する場合は、`ms.subservice` を指定できます。</span><span class="sxs-lookup"><span data-stu-id="115a5-108">To specify more detailed information about `ms.service`, you can specify `ms.subservice`.</span></span> <span data-ttu-id="115a5-109">`ms.prod` と `ms.subservice`、または `ms.service` と `ms.technology` は併用できません。</span><span class="sxs-lookup"><span data-stu-id="115a5-109">You can't use `ms.prod` with `ms.subservice` or `ms.service` with `ms.technology`.</span></span>

## <a name="resolution"></a><span data-ttu-id="115a5-110">解決方法</span><span class="sxs-lookup"><span data-stu-id="115a5-110">Resolution</span></span>

<span data-ttu-id="115a5-111">まず、ご自分の記事に対して適切な親属性 (`ms.prod` または `ms.service`) を選択したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="115a5-111">First, verify that you have selected the correct parent attribute (`ms.prod` or `ms.service`) for your article.</span></span> <span data-ttu-id="115a5-112">次に、適切な子のフィールドを、有効なペアの値と共に追加します。</span><span class="sxs-lookup"><span data-stu-id="115a5-112">Then, add the appropriate child field with a valid paired value.</span></span> <span data-ttu-id="115a5-113">余分なフィールドはすべて削除します。</span><span class="sxs-lookup"><span data-stu-id="115a5-113">Remove any extra fields.</span></span>

<span data-ttu-id="115a5-114">有効な値は、[こちらの Microsoft 内部サイト](https://docsmetadatatool.azurewebsites.net/whitelists)にあります。</span><span class="sxs-lookup"><span data-stu-id="115a5-114">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
