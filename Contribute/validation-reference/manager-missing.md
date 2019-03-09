---
title: manager-missing
description: Docs のビルドの問題 manager-missing に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 3/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 16da241a21d400d5a5dfb101e247e55d95567485
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427828"
---
# <a name="manager-missing"></a><span data-ttu-id="09601-103">manager-missing</span><span class="sxs-lookup"><span data-stu-id="09601-103">manager-missing</span></span>

<span data-ttu-id="09601-104">**準備中**</span><span class="sxs-lookup"><span data-stu-id="09601-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="09601-105">提案</span><span class="sxs-lookup"><span data-stu-id="09601-105">Suggestion</span></span>

`Missing attribute: manager. Add a valid Microsoft alias for the author's manager.`

<span data-ttu-id="09601-106">一部のコンテンツ グループには、作成者のマネージャーを識別するための `manager` 属性が必要です。</span><span class="sxs-lookup"><span data-stu-id="09601-106">Some content groups require the `manager` attribute to identify the author's manager.</span></span>

## <a name="resolution"></a><span data-ttu-id="09601-107">解決方法</span><span class="sxs-lookup"><span data-stu-id="09601-107">Resolution</span></span>

<span data-ttu-id="09601-108">`manager` に対して有効な Microsoft のエイリアスを追加します。</span><span class="sxs-lookup"><span data-stu-id="09601-108">Add a valid Microsoft alias for `manager`:</span></span>

```yml
---
ms.author: mbradley
manager: jemash
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
