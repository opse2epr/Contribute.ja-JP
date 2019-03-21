---
title: ms-prod-service-mismatch
description: Docs のビルドの問題 ms-prod-service-mismatch に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: a7de44e9930def2d2582194f28695e3ef3940541
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987617"
---
# <a name="ms-prod-service-mismatch"></a><span data-ttu-id="47ca8-103">ms-prod-service-mismatch</span><span class="sxs-lookup"><span data-stu-id="47ca8-103">ms-prod-service-mismatch</span></span>

<span data-ttu-id="47ca8-104">**準備中**</span><span class="sxs-lookup"><span data-stu-id="47ca8-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="47ca8-105">提案</span><span class="sxs-lookup"><span data-stu-id="47ca8-105">Suggestion</span></span>

`Invalid attribute pair: ms.prod and ms.subservice. You can only pair ms.prod with ms.technology.`

`Invalid attribute pair: ms.service and ms.technology. You can only pair ms.service with ms.subservice.`

<span data-ttu-id="47ca8-106">オンプレミスの製品を指定する場合は `ms.prod` を、クラウド サービスの場合は `ms.service` を使います。</span><span class="sxs-lookup"><span data-stu-id="47ca8-106">Use `ms.prod` to specify on-premises products; `ms.service` for cloud services.</span></span> <span data-ttu-id="47ca8-107">`ms.prod` に関する詳細情報を指定する場合は、必要に応じて `ms.technology` を指定できます。</span><span class="sxs-lookup"><span data-stu-id="47ca8-107">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`.</span></span> <span data-ttu-id="47ca8-108">`ms.service` に関する詳細情報を指定する場合は、`ms.subservice` を指定できます。</span><span class="sxs-lookup"><span data-stu-id="47ca8-108">To specify more detailed information about `ms.service`, you can specify `ms.subservice`.</span></span> <span data-ttu-id="47ca8-109">`ms.prod` と `ms.subservice`、または `ms.service` と `ms.technology` は併用できません。</span><span class="sxs-lookup"><span data-stu-id="47ca8-109">You can't use `ms.prod` with `ms.subservice` or `ms.service` with `ms.technology`.</span></span>

## <a name="resolution"></a><span data-ttu-id="47ca8-110">解決方法</span><span class="sxs-lookup"><span data-stu-id="47ca8-110">Resolution</span></span>

<span data-ttu-id="47ca8-111">まず、ご自分の記事に対して適切な親属性 (`ms.prod` または `ms.service`) を選択したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="47ca8-111">First, verify that you have selected the correct parent attribute (`ms.prod` or `ms.service`) for your article.</span></span> <span data-ttu-id="47ca8-112">次に、適切な子のフィールドを、有効なペアの値と共に追加します。</span><span class="sxs-lookup"><span data-stu-id="47ca8-112">Then, add the appropriate child field with a valid paired value.</span></span> <span data-ttu-id="47ca8-113">余分なフィールドはすべて削除します。</span><span class="sxs-lookup"><span data-stu-id="47ca8-113">Remove any extra fields.</span></span>

<span data-ttu-id="47ca8-114">有効な値は、[こちらの Microsoft 内部サイト](https://docsmetadatatool.azurewebsites.net/allowlists)にあります。</span><span class="sxs-lookup"><span data-stu-id="47ca8-114">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
