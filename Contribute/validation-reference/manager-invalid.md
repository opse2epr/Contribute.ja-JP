---
title: manager-invalid
description: Docs のビルドの問題 manager-invalid に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 3/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 44174bde29b63bffe709596f9c2d6be994f252a3
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637232"
---
# <a name="manager-invalid"></a><span data-ttu-id="06cd7-103">manager-invalid</span><span class="sxs-lookup"><span data-stu-id="06cd7-103">manager-invalid</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="06cd7-104">提案</span><span class="sxs-lookup"><span data-stu-id="06cd7-104">Suggestion</span></span>

`Invalid value for manager: '{value}' is not a valid Microsoft alias.`

<span data-ttu-id="06cd7-105">一部のコンテンツ グループには、作成者のマネージャーを識別するための `manager` 属性が必要です。</span><span class="sxs-lookup"><span data-stu-id="06cd7-105">Some content groups require the `manager` attribute to identify the author's manager.</span></span>

## <a name="resolution"></a><span data-ttu-id="06cd7-106">解決方法</span><span class="sxs-lookup"><span data-stu-id="06cd7-106">Resolution</span></span>

<span data-ttu-id="06cd7-107">個々の Microsoft 社員について `manager` の値を有効なエイリアスとする必要があります。</span><span class="sxs-lookup"><span data-stu-id="06cd7-107">The value of `manager` must be a valid alias for an individual Microsoft employee.</span></span> <span data-ttu-id="06cd7-108">作成者のマネージャーのエイリアスを確認し、その値を更新します。</span><span class="sxs-lookup"><span data-stu-id="06cd7-108">Verify the author's manager's alias and update the value.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
