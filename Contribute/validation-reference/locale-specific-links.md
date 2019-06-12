---
author: meganbradley
ms.author: mbradley
ms.date: 03/29/2019
title: ロケール固有のリンク
ms.openlocfilehash: f42a26da45b48972bfc595cb26c67ab0acfe8603
ms.sourcegitcommit: 1e53d17639277bebd89b2e7cabeb45bdad526354
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/12/2019
ms.locfileid: "66841252"
---
# <a name="locale-specific-links"></a><span data-ttu-id="6f7d4-102">ロケール固有のリンク</span><span class="sxs-lookup"><span data-stu-id="6f7d4-102">Locale-specific links</span></span>

<span data-ttu-id="6f7d4-103">特定の Microsoft サイトへのリンクにロケールのコード (`en-us` など) を含めるべきではありません。</span><span class="sxs-lookup"><span data-stu-id="6f7d4-103">Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites.</span></span> <span data-ttu-id="6f7d4-104">英語のコンテンツ内のリンクにロケールのコードを含めた場合、それはローカライズされたリンクにも含まれることになり、ローカライズのエクスペリエンスが損なわれます。</span><span class="sxs-lookup"><span data-stu-id="6f7d4-104">If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience.</span></span> <span data-ttu-id="6f7d4-105">たとえば、ドイツ語にローカライズされたコンテンツ内のリンクが `en-us` を含んでいた場合、ドイツ語を使用するお客様が、ドイツ語の記事があるにもかかわらず英語の記事にリンクされることになります。</span><span class="sxs-lookup"><span data-stu-id="6f7d4-105">For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.</span></span>

<span data-ttu-id="6f7d4-106">Microsoft のサイトへのリンクからロケールのコードを削除してください。</span><span class="sxs-lookup"><span data-stu-id="6f7d4-106">Remove locale codes from links to Microsoft sites.</span></span> <span data-ttu-id="6f7d4-107">例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="6f7d4-107">The following is an example.</span></span>

<span data-ttu-id="6f7d4-108">変更前:</span><span class="sxs-lookup"><span data-stu-id="6f7d4-108">Before:</span></span>

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="6f7d4-109">変更後:</span><span class="sxs-lookup"><span data-stu-id="6f7d4-109">After:</span></span>

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

<span data-ttu-id="6f7d4-110">以下のサイトはこの検証の対象に含まれます。</span><span class="sxs-lookup"><span data-stu-id="6f7d4-110">The following sites are in scope for this validation:</span></span>

- <span data-ttu-id="6f7d4-111">azure.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="6f7d4-111">azure.microsoft.com</span></span>
- <span data-ttu-id="6f7d4-112">docs.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="6f7d4-112">docs.microsoft.com</span></span>
- <span data-ttu-id="6f7d4-113">msdn.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="6f7d4-113">msdn.microsoft.com</span></span>
- <span data-ttu-id="6f7d4-114">technet.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="6f7d4-114">technet.microsoft.com</span></span>