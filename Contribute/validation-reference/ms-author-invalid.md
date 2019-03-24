---
title: ms-author-invalid
description: Docs のビルドの問題 ms-author-invalid に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 5d4cc6a08c6e70824ee3f7117d58be9c75aa7fa4
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987769"
---
# <a name="ms-author-invalid"></a><span data-ttu-id="ebc4c-103">ms-author-invalid</span><span class="sxs-lookup"><span data-stu-id="ebc4c-103">ms-author-invalid</span></span>

<span data-ttu-id="ebc4c-104">**準備中**</span><span class="sxs-lookup"><span data-stu-id="ebc4c-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="ebc4c-105">提案</span><span class="sxs-lookup"><span data-stu-id="ebc4c-105">Suggestion</span></span>

`Invalid value for ms.author: '{value}' is not a valid Microsoft alias, or is not an allowed distribution list.`

## <a name="resolution"></a><span data-ttu-id="ebc4c-106">解決方法</span><span class="sxs-lookup"><span data-stu-id="ebc4c-106">Resolution</span></span>

<span data-ttu-id="ebc4c-107">`ms.author` の値が有効な Microsoft のエイリアスであるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="ebc4c-107">Verify that the `ms.author` value is a valid Microsoft alias.</span></span> <span data-ttu-id="ebc4c-108">エイリアスが配布リストである場合は、許可リストに含まれている必要もあります。</span><span class="sxs-lookup"><span data-stu-id="ebc4c-108">If the alias is a distribution list, it must also be on the allow list.</span></span>

<span data-ttu-id="ebc4c-109">DL に有効な値は、[こちらの Microsoft 内部サイト](https://docsmetadatatool.azurewebsites.net/allowlists)にあります。</span><span class="sxs-lookup"><span data-stu-id="ebc4c-109">Valid values for DLs can be found on [this Microsoft-internal site](https://docsmetadatatool.azurewebsites.net/allowlists).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
