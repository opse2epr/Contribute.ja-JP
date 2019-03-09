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
# <a name="hard-coded-locale"></a>hard-coded-locale

## <a name="warning"></a>警告

`Link {URL} contains locale code {code}. For localizability, remove {code} from links to Microsoft sites.`

特定の Microsoft サイトへのリンクにロケールのコード (`en-us` など) を含めるべきではありません。 英語のコンテンツ内のリンクにロケールのコードを含めた場合、それはローカライズされたリンクにも含まれることになり、ローカライズのエクスペリエンスが損なわれます。 たとえば、ドイツ語にローカライズされたコンテンツ内のリンクが `en-us` を含んでいた場合、ドイツ語を使用するお客様が、ドイツ語の記事があるにもかかわらず英語の記事にリンクされることになります。

以下のサイトはこの検証の対象に含まれます。

- azure.microsoft.com
- docs.microsoft.com
- msdn.microsoft.com
- technet.microsoft.com

## <a name="resolution"></a>解決方法

Microsoft のサイトへのリンクからロケールのコードを削除してください。 例を次に示します。

変更前:

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

変更後:

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]