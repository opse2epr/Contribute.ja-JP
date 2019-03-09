---
title: internal-bookmark-not-found
description: Docs のビルドの問題 internal-bookmark-not-found に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/28/2019
ms.prod: non-product-specific
ms.openlocfilehash: 9073603d4e745db2f49b57a8901e00a03d8f570f
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427831"
---
# <a name="internal-bookmark-not-found"></a><span data-ttu-id="df775-103">internal-bookmark-not-found</span><span class="sxs-lookup"><span data-stu-id="df775-103">internal-bookmark-not-found</span></span>

<span data-ttu-id="df775-104">**準備中**</span><span class="sxs-lookup"><span data-stu-id="df775-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="df775-105">提案</span><span class="sxs-lookup"><span data-stu-id="df775-105">Suggestion</span></span>

`Current file doesn't contain a bookmark named '{bookmark}'.`

<span data-ttu-id="df775-106">存在しない現在のファイル内の見出しにリンクしようとしています。</span><span class="sxs-lookup"><span data-stu-id="df775-106">You're trying to link to a heading in the current file that doesn't exist.</span></span>

## <a name="resolution"></a><span data-ttu-id="df775-107">解決方法</span><span class="sxs-lookup"><span data-stu-id="df775-107">Resolution</span></span>

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

<span data-ttu-id="df775-108">リンクする先の見出しを確認し、リンクを更新します。</span><span class="sxs-lookup"><span data-stu-id="df775-108">Verify the heading you want to link to and update the link.</span></span>

<span data-ttu-id="df775-109">現在の記事にあるセクションにリンクするには、ハッシュ記号を使用し、その後に見出し語を続けます。</span><span class="sxs-lookup"><span data-stu-id="df775-109">To link to a section in the current article, use a hash symbol, followed by the words of the heading.</span></span> <span data-ttu-id="df775-110">見出しから句読点を削除し、スペースをダッシュに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="df775-110">Remove punctuation from the heading and replace spaces with dashes.</span></span> <span data-ttu-id="df775-111">例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="df775-111">The following is an example:</span></span>

```markdown
[Managed Disks](#managed-disks)
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
