---
title: deprecated-attribute
description: Docs のビルドの問題 deprecated-attribute に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 113ca759af1765a2a51cadc721fa59743b699475
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636887"
---
# <a name="deprecated-attribute"></a><span data-ttu-id="2d193-103">deprecated-attribute</span><span class="sxs-lookup"><span data-stu-id="2d193-103">deprecated-attribute</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="2d193-104">提案</span><span class="sxs-lookup"><span data-stu-id="2d193-104">Suggestion</span></span>

`Deprecated attribute: ms.component. Use ms.subservice instead.`

<span data-ttu-id="2d193-105">`ms.service` を使ってクラウド サービスを指定します。</span><span class="sxs-lookup"><span data-stu-id="2d193-105">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="2d193-106">`ms.service` に関する詳細情報を指定する場合は、必要に応じて `ms.subservice` を指定できます。</span><span class="sxs-lookup"><span data-stu-id="2d193-106">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="2d193-107">`ms.component` は使用しないでください。このコンテンツでは非推奨です。</span><span class="sxs-lookup"><span data-stu-id="2d193-107">Don't use `ms.component`; it's deprecated for this content.</span></span>

## <a name="resolution"></a><span data-ttu-id="2d193-108">解決方法</span><span class="sxs-lookup"><span data-stu-id="2d193-108">Resolution</span></span>

<span data-ttu-id="2d193-109">`ms.service` の値がご自分の記事に対して適切であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="2d193-109">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="2d193-110">次に、有効な `ms.subservice` の値を選びます。</span><span class="sxs-lookup"><span data-stu-id="2d193-110">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="2d193-111">有効な値は、[こちらの Microsoft 内部サイト](https://docsmetadatatool.azurewebsites.net/allowlists)にあります。</span><span class="sxs-lookup"><span data-stu-id="2d193-111">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
