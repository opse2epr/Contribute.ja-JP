---
title: author-missing
description: Docs のビルドの問題 author-missing に関する説明と解決方法。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 89725dcfbd4ec266071c45a003748021b480bbc2
ms.sourcegitcommit: f374ad2607360f46d88982b4b7ecc63d3ab08235
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/20/2019
ms.locfileid: "56431532"
---
# <a name="author-missing"></a><span data-ttu-id="7046a-103">author-missing</span><span class="sxs-lookup"><span data-stu-id="7046a-103">author-missing</span></span>

<span data-ttu-id="7046a-104">**準備中**</span><span class="sxs-lookup"><span data-stu-id="7046a-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="7046a-105">提案</span><span class="sxs-lookup"><span data-stu-id="7046a-105">Suggestion</span></span>

`Missing attribute: author. Add a valid GitHub ID.`

<span data-ttu-id="7046a-106">`author` 属性は、GitHub ID によって記事の作成者を識別します。</span><span class="sxs-lookup"><span data-stu-id="7046a-106">The `author` attribute identifies the author of the article by GitHub ID.</span></span> 

## <a name="resolution"></a><span data-ttu-id="7046a-107">解決方法</span><span class="sxs-lookup"><span data-stu-id="7046a-107">Resolution</span></span>

<span data-ttu-id="7046a-108">作成者の GitHub ID を YML ヘッダーに追加します。</span><span class="sxs-lookup"><span data-stu-id="7046a-108">Add the author's GitHub ID to the YML header:</span></span>

```yml
---
author: meganbradley
ms.author: mbradley
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]