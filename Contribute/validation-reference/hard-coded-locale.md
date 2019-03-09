---
title: hard-coded-locale
description: Docs のビルドの問題 hard-coded-locale に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 12/12/2018
ms.prod: non-product-specific
ms.openlocfilehash: 1862014076fa4cbff18535095b244e8f94a17b0f
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427671"
---
# <a name="hard-coded-locale"></a><span data-ttu-id="400d1-103">hard-coded-locale</span><span class="sxs-lookup"><span data-stu-id="400d1-103">hard-coded-locale</span></span>

## <a name="warning"></a><span data-ttu-id="400d1-104">警告</span><span class="sxs-lookup"><span data-stu-id="400d1-104">Warning</span></span>

`Link {URL} contains locale code {code}. For localizability, remove {code} from links to Microsoft sites.`

<span data-ttu-id="400d1-105">特定の Microsoft サイトへのリンクにロケールのコード (`en-us` など) を含めるべきではありません。</span><span class="sxs-lookup"><span data-stu-id="400d1-105">Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites.</span></span> <span data-ttu-id="400d1-106">英語のコンテンツ内のリンクにロケールのコードを含めた場合、それはローカライズされたリンクにも含まれることになり、ローカライズのエクスペリエンスが損なわれます。</span><span class="sxs-lookup"><span data-stu-id="400d1-106">If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience.</span></span> <span data-ttu-id="400d1-107">たとえば、ドイツ語にローカライズされたコンテンツ内のリンクが `en-us` を含んでいた場合、ドイツ語を使用するお客様が、ドイツ語の記事があるにもかかわらず英語の記事にリンクされることになります。</span><span class="sxs-lookup"><span data-stu-id="400d1-107">For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.</span></span>

<span data-ttu-id="400d1-108">以下のサイトはこの検証の対象に含まれます。</span><span class="sxs-lookup"><span data-stu-id="400d1-108">The following sites are in scope for this validation:</span></span>

- <span data-ttu-id="400d1-109">azure.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="400d1-109">azure.microsoft.com</span></span>
- <span data-ttu-id="400d1-110">docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="400d1-110">docs.microsoft.com</span></span>
- <span data-ttu-id="400d1-111">msdn.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="400d1-111">msdn.microsoft.com</span></span>
- <span data-ttu-id="400d1-112">technet.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="400d1-112">technet.microsoft.com</span></span>

## <a name="resolution"></a><span data-ttu-id="400d1-113">解決方法</span><span class="sxs-lookup"><span data-stu-id="400d1-113">Resolution</span></span>

<span data-ttu-id="400d1-114">Microsoft のサイトへのリンクからロケールのコードを削除してください。</span><span class="sxs-lookup"><span data-stu-id="400d1-114">Remove locale codes from links to Microsoft sites.</span></span> <span data-ttu-id="400d1-115">例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="400d1-115">The following is an example.</span></span>

<span data-ttu-id="400d1-116">変更前:</span><span class="sxs-lookup"><span data-stu-id="400d1-116">Before:</span></span>

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="400d1-117">変更後:</span><span class="sxs-lookup"><span data-stu-id="400d1-117">After:</span></span>

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]