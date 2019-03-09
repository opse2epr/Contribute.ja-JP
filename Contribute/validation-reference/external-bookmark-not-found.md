---
title: external-bookmark-not-found
description: Docs のビルドの問題 external-bookmark-not-found に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: b533a463ac38d6445ab84c74bf14b2065a0a63f3
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427771"
---
# <a name="external-bookmark-not-found"></a><span data-ttu-id="449a6-103">external-bookmark-not-found</span><span class="sxs-lookup"><span data-stu-id="449a6-103">external-bookmark-not-found</span></span>

## <a name="warning"></a><span data-ttu-id="449a6-104">警告</span><span class="sxs-lookup"><span data-stu-id="449a6-104">Warning</span></span>

`File '{file name}' doesn't contain a bookmark named '{bookmark text}'.`

<span data-ttu-id="449a6-105">存在しない別のファイル内の見出しにリンクしようとしています。</span><span class="sxs-lookup"><span data-stu-id="449a6-105">You're trying to link to a heading in another file that doesn't exist.</span></span>

## <a name="resolution"></a><span data-ttu-id="449a6-106">解決方法</span><span class="sxs-lookup"><span data-stu-id="449a6-106">Resolution</span></span>

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

<span data-ttu-id="449a6-107">リンク先のファイルを確認し、そのファイル内の有効なセクションを指すブックマーク リンクを更新します。</span><span class="sxs-lookup"><span data-stu-id="449a6-107">Review the file you're linking to and update your bookmark link to point to a valid section in the file.</span></span>

<span data-ttu-id="449a6-108">別の記事にあるセクション見出しにリンクするには、ファイル相対リンクまたはサイト相対リンクに加えてハッシュ記号使用し、その後に見出し語を続けます。</span><span class="sxs-lookup"><span data-stu-id="449a6-108">To link to a section heading in another article, use the file-relative or site-relative link plus a hash symbol, followed by the words of the heading.</span></span> <span data-ttu-id="449a6-109">見出しから句読点を削除し、スペースをダッシュに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="449a6-109">Remove punctuation from the heading and replace spaces with dashes.</span></span> <span data-ttu-id="449a6-110">例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="449a6-110">The following is an example:</span></span>

```markdown
[Managed Disks](../../linux/overview.md#managed-disks)
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
