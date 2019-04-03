---
author: meganbradley
ms.author: mbradley
ms.date: 03/29/2019
ms.openlocfilehash: a3b383021046412620c616882b19cb06f4dc59f8
ms.sourcegitcommit: af37d44eb67daa2841959817cd205ec95db18cec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/29/2019
ms.locfileid: "58653553"
---
# <a name="locale-specific-links"></a><span data-ttu-id="9a7bd-101">ロケール固有のリンク</span><span class="sxs-lookup"><span data-stu-id="9a7bd-101">Locale-specific links</span></span>

<span data-ttu-id="9a7bd-102">特定の Microsoft サイトへのリンクにロケールのコード (`en-us` など) を含めるべきではありません。</span><span class="sxs-lookup"><span data-stu-id="9a7bd-102">Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites.</span></span> <span data-ttu-id="9a7bd-103">英語のコンテンツ内のリンクにロケールのコードを含めた場合、それはローカライズされたリンクにも含まれることになり、ローカライズのエクスペリエンスが損なわれます。</span><span class="sxs-lookup"><span data-stu-id="9a7bd-103">If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience.</span></span> <span data-ttu-id="9a7bd-104">たとえば、ドイツ語にローカライズされたコンテンツ内のリンクが `en-us` を含んでいた場合、ドイツ語を使用するお客様が、ドイツ語の記事があるにもかかわらず英語の記事にリンクされることになります。</span><span class="sxs-lookup"><span data-stu-id="9a7bd-104">For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.</span></span>

<span data-ttu-id="9a7bd-105">Microsoft のサイトへのリンクからロケールのコードを削除してください。</span><span class="sxs-lookup"><span data-stu-id="9a7bd-105">Remove locale codes from links to Microsoft sites.</span></span> <span data-ttu-id="9a7bd-106">例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="9a7bd-106">The following is an example.</span></span>

<span data-ttu-id="9a7bd-107">変更前:</span><span class="sxs-lookup"><span data-stu-id="9a7bd-107">Before:</span></span>

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="9a7bd-108">変更後:</span><span class="sxs-lookup"><span data-stu-id="9a7bd-108">After:</span></span>

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="9a7bd-109">以下のサイトはこの検証の対象に含まれます。</span><span class="sxs-lookup"><span data-stu-id="9a7bd-109">The following sites are in scope for this validation:</span></span>

- <span data-ttu-id="9a7bd-110">azure.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="9a7bd-110">azure.microsoft.com</span></span>
- <span data-ttu-id="9a7bd-111">docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="9a7bd-111">docs.microsoft.com</span></span>
- <span data-ttu-id="9a7bd-112">msdn.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="9a7bd-112">msdn.microsoft.com</span></span>
- <span data-ttu-id="9a7bd-113">technet.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="9a7bd-113">technet.microsoft.com</span></span>