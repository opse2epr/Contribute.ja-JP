---
title: deprecated-attribute
description: Docs のビルドの問題 deprecated-attribute に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4f9ddc611d401bc7003e1b7d378517d5e374da87
ms.sourcegitcommit: a2c8317ccf8b56371773c84f4960a44787ce8666
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2019
ms.locfileid: "56322685"
---
# <a name="deprecated-attribute"></a><span data-ttu-id="0d93b-103">deprecated-attribute</span><span class="sxs-lookup"><span data-stu-id="0d93b-103">deprecated-attribute</span></span>

<span data-ttu-id="0d93b-104">**準備中**</span><span class="sxs-lookup"><span data-stu-id="0d93b-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="0d93b-105">提案</span><span class="sxs-lookup"><span data-stu-id="0d93b-105">Suggestion</span></span>

`Deprecated attribute: ms.component. Use ms.subservice instead.`

<span data-ttu-id="0d93b-106">`ms.service` を使ってクラウド サービスを指定します。</span><span class="sxs-lookup"><span data-stu-id="0d93b-106">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="0d93b-107">`ms.service` に関する詳細情報を指定する場合は、必要に応じて `ms.subservice` を指定できます。</span><span class="sxs-lookup"><span data-stu-id="0d93b-107">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="0d93b-108">`ms.component` は使用しないでください。このコンテンツでは非推奨です。</span><span class="sxs-lookup"><span data-stu-id="0d93b-108">Don't use `ms.component`; it's deprecated for this content.</span></span>

## <a name="resolution"></a><span data-ttu-id="0d93b-109">解決方法</span><span class="sxs-lookup"><span data-stu-id="0d93b-109">Resolution</span></span>

<span data-ttu-id="0d93b-110">`ms.service` の値がご自分の記事に対して適切であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="0d93b-110">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="0d93b-111">次に、有効な `ms.subservice` の値を選びます。</span><span class="sxs-lookup"><span data-stu-id="0d93b-111">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="0d93b-112">有効な値は、[こちらの Microsoft 内部サイト](https://docsmetadatatool.azurewebsites.net/whitelists)にあります。</span><span class="sxs-lookup"><span data-stu-id="0d93b-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
