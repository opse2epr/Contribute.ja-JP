---
title: ms-prod-and-technology-invalid
description: Docs のビルドの問題 ms-prod-and-technology-invalid に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 92e8b17c3b5c96d544d12d394534a494ada3b901
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713271"
---
# <a name="ms-prod-and-technology-invalid"></a><span data-ttu-id="81c3a-103">ms-prod-and-technology-invalid</span><span class="sxs-lookup"><span data-stu-id="81c3a-103">ms-prod-and-technology-invalid</span></span>

<span data-ttu-id="81c3a-104">**準備中**</span><span class="sxs-lookup"><span data-stu-id="81c3a-104">**Coming soon!**</span></span>

## <a name="warning"></a><span data-ttu-id="81c3a-105">警告</span><span class="sxs-lookup"><span data-stu-id="81c3a-105">Warning</span></span>

`Invalid value for ms.prod: '{value}'.`

`Invalid value for ms.technology: '{value}' is not valid with ms.prod value '{value}'.`

<span data-ttu-id="81c3a-106">オンプレミスの製品を指定する場合は `ms.prod` を使います。</span><span class="sxs-lookup"><span data-stu-id="81c3a-106">Use `ms.prod` to specify on-premises products.</span></span> <span data-ttu-id="81c3a-107">`ms.prod` に関する詳細情報を指定する場合は、必要に応じて `ms.technology` を指定できます。</span><span class="sxs-lookup"><span data-stu-id="81c3a-107">To specify more detailed information about `ms.prod`, you can optionally specify `ms.technology`.</span></span> <span data-ttu-id="81c3a-108">`ms.prod` と `ms.technology` に対する値は有効なペアである必要があります。</span><span class="sxs-lookup"><span data-stu-id="81c3a-108">The values for `ms.prod` and `ms.technology` must be a valid pair.</span></span> <span data-ttu-id="81c3a-109">`ms.prod` の値が無効であるか、`ms.technology` の値が `ms.prod` と有効なペアになっていないかのどちらかです。</span><span class="sxs-lookup"><span data-stu-id="81c3a-109">Either your `ms.prod` value is invalid, or your `ms.technology` value is not a valid pair with your `ms.prod`.</span></span>

## <a name="resolution"></a><span data-ttu-id="81c3a-110">解決方法</span><span class="sxs-lookup"><span data-stu-id="81c3a-110">Resolution</span></span>

<span data-ttu-id="81c3a-111">`ms.prod` の値がご自分の記事に対して適切であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="81c3a-111">Confirm that your `ms.prod` value is correct for your article.</span></span> <span data-ttu-id="81c3a-112">次に、有効な `ms.technology` の値を選びます。</span><span class="sxs-lookup"><span data-stu-id="81c3a-112">Then choose a valid `ms.technology` value.</span></span>

<span data-ttu-id="81c3a-113">有効な値は、[こちらの Microsoft 内部サイト](https://docsmetadatatool.azurewebsites.net/whitelists)にあります。</span><span class="sxs-lookup"><span data-stu-id="81c3a-113">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!-- Can we link to whitelist externally? -->

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
