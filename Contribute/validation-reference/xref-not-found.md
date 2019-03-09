---
title: xref-not-found
description: Docs のビルドの問題 xref-not-found に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: d51eace291bfac179be2701463d113c06627f92f
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427873"
---
# <a name="xref-not-found"></a><span data-ttu-id="db7d3-103">xref-not-found</span><span class="sxs-lookup"><span data-stu-id="db7d3-103">xref-not-found</span></span>

## <a name="warning"></a><span data-ttu-id="db7d3-104">警告</span><span class="sxs-lookup"><span data-stu-id="db7d3-104">Warning</span></span>

`Cross reference not found: '<xref: {uid}>'.`

`Cross reference not found: '@{uid}'.`

<span data-ttu-id="db7d3-105">リンク先の UID が存在していないか、またはご利用のリポジトリでは使用できません。</span><span class="sxs-lookup"><span data-stu-id="db7d3-105">The UID you linked to doesn't exist, or isn't available to your repo.</span></span>

## <a name="resolution"></a><span data-ttu-id="db7d3-106">解決方法</span><span class="sxs-lookup"><span data-stu-id="db7d3-106">Resolution</span></span>

<span data-ttu-id="db7d3-107">Microsoft 内部向けの [Xref Service](https://review.docs.microsoft.com/en-us/help/onboard/admin/xref-service?branch=master) に関するドキュメントの説明に従って、UID が正しいこと、およびご利用のリポジトリ上で Xref Service が適切に構成されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="db7d3-107">Confirm that the UID is correct and that the Xref Service is properly configured on your repo, as described in the Microsoft-internal [Xref Service](https://review.docs.microsoft.com/en-us/help/onboard/admin/xref-service?branch=master) documentation.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
