---
title: circular-reference
description: Docs のビルドの問題 circular-reference に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4600465cf940efa82c61bcbac4a1d912c16e6903
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459213"
---
# <a name="circular-reference"></a><span data-ttu-id="0cf76-103">circular-reference</span><span class="sxs-lookup"><span data-stu-id="0cf76-103">circular-reference</span></span>

## <a name="error"></a><span data-ttu-id="0cf76-104">エラー</span><span class="sxs-lookup"><span data-stu-id="0cf76-104">Error</span></span>

`Files '{file name 1}' and '{file name 2}' reference each other.`

<span data-ttu-id="0cf76-105">たとえば、これは現在のファイルにリンクされているインクルード ファイルである可能性もあれば、現在のファイルにリダイレクトされたファイルへのリンクである可能性もあります。</span><span class="sxs-lookup"><span data-stu-id="0cf76-105">For example, this might be an included file that links to the current file, or a link to a file that's been redirected to the current file.</span></span>

## <a name="resolution"></a><span data-ttu-id="0cf76-106">解決方法</span><span class="sxs-lookup"><span data-stu-id="0cf76-106">Resolution</span></span>

<span data-ttu-id="0cf76-107">ファイル内のリンクを確認し、ファイルがそれ自体にリンクしないように、またはファイルにそれ自体が含まれないように必要な編集を行います。</span><span class="sxs-lookup"><span data-stu-id="0cf76-107">Review the links in the files and make necessary edits so no file links to or includes itself.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
