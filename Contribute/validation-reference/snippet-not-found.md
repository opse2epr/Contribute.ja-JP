---
title: snippet-not-found
description: Docs のビルドの問題 snippet-not-found に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: 82fc2926f5bc2ec01577670b066b88fb59d7ea11
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459098"
---
# <a name="snippet-not-found"></a><span data-ttu-id="21c56-103">snippet-not-found</span><span class="sxs-lookup"><span data-stu-id="21c56-103">snippet-not-found</span></span>

## <a name="warning"></a><span data-ttu-id="21c56-104">警告</span><span class="sxs-lookup"><span data-stu-id="21c56-104">Warning</span></span>

`Code snippet '{snippet path}' not found.`

<span data-ttu-id="21c56-105">指定したパスにコード スニペットの参照が存在していないか、またはそのパスを現在のファイルから使用できません。</span><span class="sxs-lookup"><span data-stu-id="21c56-105">The code snippet references doesn't exist at the specified path, or the path isn't available from the current file.</span></span>

## <a name="resolution"></a><span data-ttu-id="21c56-106">解決方法</span><span class="sxs-lookup"><span data-stu-id="21c56-106">Resolution</span></span>

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

<span data-ttu-id="21c56-107">ご利用のスニペット パスが正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="21c56-107">Ensure that your snippet path is correct.</span></span> <span data-ttu-id="21c56-108">スニペットが現在のリポジトリの外に格納されている場合は、リポジトリを必ず依存リポジトリとして構成します。</span><span class="sxs-lookup"><span data-stu-id="21c56-108">If the snippet is stored outside the current repo, make sure the repo is configured ase a dependent repo.</span></span> <span data-ttu-id="21c56-109">詳細については、Microsoft 内部向けの[コード スニペットに関する記事](https://review.docs.microsoft.com/en-us/help/contribute/code-in-docs?branch=master)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="21c56-109">For more information, see the Microsoft-internal [code snippet article](https://review.docs.microsoft.com/en-us/help/contribute/code-in-docs?branch=master).</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
