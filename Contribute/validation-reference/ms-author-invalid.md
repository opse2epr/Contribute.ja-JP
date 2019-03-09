---
title: ms-author-invalid
description: Docs のビルドの問題 ms-author-invalid に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 210ff6a18bd12585c81f461a87238aa8d20c0530
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427851"
---
# <a name="ms-author-invalid"></a><span data-ttu-id="2be76-103">ms-author-invalid</span><span class="sxs-lookup"><span data-stu-id="2be76-103">ms-author-invalid</span></span>

<span data-ttu-id="2be76-104">**準備中**</span><span class="sxs-lookup"><span data-stu-id="2be76-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="2be76-105">提案</span><span class="sxs-lookup"><span data-stu-id="2be76-105">Suggestion</span></span>

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not a whitelisted distribution list.`

## <a name="resolution"></a><span data-ttu-id="2be76-106">解決方法</span><span class="sxs-lookup"><span data-stu-id="2be76-106">Resolution</span></span>

<span data-ttu-id="2be76-107">`ms.author` の値が有効な Microsoft のエイリアスであるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="2be76-107">Verify that the `ms.author` value is a valid Microsoft alias.</span></span> <span data-ttu-id="2be76-108">エイリアスが配布リストである場合は、ホワイト リストへの登録も必要です。</span><span class="sxs-lookup"><span data-stu-id="2be76-108">If the alias is a distribution list, it must also be whitelisted.</span></span>

<span data-ttu-id="2be76-109">有効な値は、[こちらの Microsoft 内部サイト](https://docsmetadatatool.azurewebsites.net/whitelists)にあります。</span><span class="sxs-lookup"><span data-stu-id="2be76-109">Valid values can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/whitelists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
