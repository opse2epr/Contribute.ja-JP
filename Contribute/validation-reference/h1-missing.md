---
title: h1-missing
description: Docs のビルドの問題 h1-missing に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: c920cc0f12a9fac41b640957d45452a7958d4b07
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459121"
---
# <a name="h1-missing"></a><span data-ttu-id="a0a26-103">h1-missing</span><span class="sxs-lookup"><span data-stu-id="a0a26-103">h1-missing</span></span>

## <a name="warning"></a><span data-ttu-id="a0a26-104">警告</span><span class="sxs-lookup"><span data-stu-id="a0a26-104">Warning</span></span>

`H1 is required. Use a single hash (#) followed by a space to create your top-level heading.`

<span data-ttu-id="a0a26-105">H1 はマークダウン ファイル内の最初の見出しを参照します。</span><span class="sxs-lookup"><span data-stu-id="a0a26-105">H1 refers to the first heading in a Markdown file.</span></span> <span data-ttu-id="a0a26-106">docs.microsoft.com に公開すると、H1 はページの上部に大きなフォントで表示されます。</span><span class="sxs-lookup"><span data-stu-id="a0a26-106">When published to docs.microsoft.com, the H1 shows at the top of the page in a large font.</span></span> <span data-ttu-id="a0a26-107">H1 を作成するには、行を 1 つのハッシュ (#) とスペースで開始して、その後に見出しのテキストを続けます。</span><span class="sxs-lookup"><span data-stu-id="a0a26-107">An H1 is created by beginning a line with a single hash (#) followed by a space, then the heading text.</span></span>

## <a name="resolution"></a><span data-ttu-id="a0a26-108">解決方法</span><span class="sxs-lookup"><span data-stu-id="a0a26-108">Resolution</span></span>

<span data-ttu-id="a0a26-109">この問題を解決するには、ご利用のファイル内の YML メタデータ ブロックの後に、H1 を最初のコンテンツとして追加します。</span><span class="sxs-lookup"><span data-stu-id="a0a26-109">To fix this issue, add an H1 as the first content after the YML metadata block in your file:</span></span>

```markdown
---
author: meganbradley
ms.author: mbradley
---
# This is an H1
```

> [!NOTE]
> <span data-ttu-id="a0a26-110">このルールはインクルード ファイルには適用されません。</span><span class="sxs-lookup"><span data-stu-id="a0a26-110">This rule does not apply to included files.</span></span> <span data-ttu-id="a0a26-111">インクルード ファイルに対して H1 の警告が表示された場合、大抵はインクルード ファイルを `includes` フォルダーに移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0a26-111">If you get H1 warnings on included files, you most likely need to move your included files into an `includes` folder.</span></span> <span data-ttu-id="a0a26-112">`includes` フォルダーは、ファイル パス内の任意のレベルに置くことができます。</span><span class="sxs-lookup"><span data-stu-id="a0a26-112">The `includes` folder can be at any level in the file path.</span></span> <span data-ttu-id="a0a26-113">パスに基づいて Docs のビルドではファイルがインクルード ファイルとして認識され、H1 の検証は実行されません。</span><span class="sxs-lookup"><span data-stu-id="a0a26-113">Based on the path, Docs build will recognize the file as an included file and H1 validations won't run.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]