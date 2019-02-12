---
title: ms-component-deprecated
description: Docs のビルドの問題 ms-component-deprecated に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4f89571e2d4c50439806fb26b9967a4b7588f4a9
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713156"
---
# <a name="ms-component-deprecated"></a><span data-ttu-id="facc9-103">ms-component-deprecated</span><span class="sxs-lookup"><span data-stu-id="facc9-103">ms-component-deprecated</span></span>

<span data-ttu-id="facc9-104">**準備中**</span><span class="sxs-lookup"><span data-stu-id="facc9-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="facc9-105">提案</span><span class="sxs-lookup"><span data-stu-id="facc9-105">Suggestion</span></span>

`Deprecated attribute: ms.component. Use ms.subservice instead.`

<span data-ttu-id="facc9-106">`ms.service` を使ってクラウド サービスを指定します。</span><span class="sxs-lookup"><span data-stu-id="facc9-106">Use `ms.service` to specify cloud services.</span></span> <span data-ttu-id="facc9-107">`ms.service` に関する詳細情報を指定する場合は、必要に応じて `ms.subservice` を指定できます。</span><span class="sxs-lookup"><span data-stu-id="facc9-107">To specify more detailed information about `ms.service`, you can optionally specify `ms.subservice`.</span></span> <span data-ttu-id="facc9-108">`ms.component` は使用しないでください。このコンテンツでは非推奨です。</span><span class="sxs-lookup"><span data-stu-id="facc9-108">Don't use `ms.component`; it's deprecated for this content.</span></span>

## <a name="resolution"></a><span data-ttu-id="facc9-109">解決方法</span><span class="sxs-lookup"><span data-stu-id="facc9-109">Resolution</span></span>

<span data-ttu-id="facc9-110">`ms.service` の値がご自分の記事に対して適切であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="facc9-110">Confirm that your `ms.service` value is correct for your article.</span></span> <span data-ttu-id="facc9-111">次に、有効な `ms.subservice` の値を選びます。</span><span class="sxs-lookup"><span data-stu-id="facc9-111">Then choose a valid `ms.subservice` value.</span></span>

<span data-ttu-id="facc9-112">有効な値は、[こちらの Microsoft 内部サイト](https://docsmetadatatool.azurewebsites.net/whitelists)にあります。</span><span class="sxs-lookup"><span data-stu-id="facc9-112">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
