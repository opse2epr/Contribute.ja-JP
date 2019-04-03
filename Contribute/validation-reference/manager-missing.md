---
title: manager-missing
description: Docs のビルドの問題 manager-missing に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 3/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: af23f2cab1fd948b4192bc0b598543ad15013ae0
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/29/2019
ms.locfileid: "58637255"
---
# <a name="manager-missing"></a><span data-ttu-id="15c62-103">manager-missing</span><span class="sxs-lookup"><span data-stu-id="15c62-103">manager-missing</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="15c62-104">提案</span><span class="sxs-lookup"><span data-stu-id="15c62-104">Suggestion</span></span>

`Missing attribute: manager. Add a valid Microsoft alias for the author's manager.`

<span data-ttu-id="15c62-105">一部のコンテンツ グループには、作成者のマネージャーを識別するための `manager` 属性が必要です。</span><span class="sxs-lookup"><span data-stu-id="15c62-105">Some content groups require the `manager` attribute to identify the author's manager.</span></span>

## <a name="resolution"></a><span data-ttu-id="15c62-106">解決方法</span><span class="sxs-lookup"><span data-stu-id="15c62-106">Resolution</span></span>

<span data-ttu-id="15c62-107">`manager` に対して有効な Microsoft のエイリアスを追加します。</span><span class="sxs-lookup"><span data-stu-id="15c62-107">Add a valid Microsoft alias for `manager`:</span></span>

```yml
---
ms.author: mbradley
manager: jemash
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
