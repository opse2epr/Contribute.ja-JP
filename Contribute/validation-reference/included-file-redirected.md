---
title: included-file-redirected
description: Docs のビルドの問題 included-file-redirected に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 3/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 8a40f04fe1a7e7f19ab9ee7ce684684184aa4dc7
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459075"
---
# <a name="included-file-redirected"></a><span data-ttu-id="23202-103">included-file-redirected</span><span class="sxs-lookup"><span data-stu-id="23202-103">included-file-redirected</span></span>

## <a name="warning"></a><span data-ttu-id="23202-104">警告</span><span class="sxs-lookup"><span data-stu-id="23202-104">Warning</span></span>

`Included file '{include path}' is redirected to '{target file path}'. Only include files that are not redirected and that are located in an includes folder.`

## <a name="resolution"></a><span data-ttu-id="23202-105">解決方法</span><span class="sxs-lookup"><span data-stu-id="23202-105">Resolution</span></span>

<span data-ttu-id="23202-106">リダイレクトされたファイルが含まれないようにご自分のコンテンツを再構築します。</span><span class="sxs-lookup"><span data-stu-id="23202-106">Restructure your content so you aren't including a redirected file.</span></span> <span data-ttu-id="23202-107">たとえば、新しいファイルを作成してリンクへの参照またはリンクを含めるか、含まれているリンクへの参照またはリンクを削除するか、コンテンツをインラインで作成します。</span><span class="sxs-lookup"><span data-stu-id="23202-107">For example, create a new file to include or remove the included reference and link to content or write it inline.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
