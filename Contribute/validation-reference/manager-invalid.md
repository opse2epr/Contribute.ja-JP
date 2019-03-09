---
title: manager-invalid
description: Docs のビルドの問題 manager-invalid に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 3/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 7eac188b16b402767bbec551a6dec8b5877680af
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427651"
---
# <a name="manager-invalid"></a><span data-ttu-id="cedeb-103">manager-invalid</span><span class="sxs-lookup"><span data-stu-id="cedeb-103">manager-invalid</span></span>

<span data-ttu-id="cedeb-104">**準備中**</span><span class="sxs-lookup"><span data-stu-id="cedeb-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="cedeb-105">提案</span><span class="sxs-lookup"><span data-stu-id="cedeb-105">Suggestion</span></span>

`Invalid value for manager: '{value}' is not a valid Microsoft alias.`

<span data-ttu-id="cedeb-106">一部のコンテンツ グループには、作成者のマネージャーを識別するための `manager` 属性が必要です。</span><span class="sxs-lookup"><span data-stu-id="cedeb-106">Some content groups require the `manager` attribute to identify the author's manager.</span></span>

## <a name="resolution"></a><span data-ttu-id="cedeb-107">解決方法</span><span class="sxs-lookup"><span data-stu-id="cedeb-107">Resolution</span></span>

<span data-ttu-id="cedeb-108">個々の Microsoft 社員について `manager` の値を有効なエイリアスとする必要があります。</span><span class="sxs-lookup"><span data-stu-id="cedeb-108">The value of `manager` must be a valid alias for an individual Microsoft employee.</span></span> <span data-ttu-id="cedeb-109">作成者のマネージャーのエイリアスを確認し、その値を更新します。</span><span class="sxs-lookup"><span data-stu-id="cedeb-109">Verify the author's manager's alias and update the value.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
