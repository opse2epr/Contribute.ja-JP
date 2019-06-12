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
# <a name="locale-specific-links"></a>ロケール固有のリンク

特定の Microsoft サイトへのリンクにロケールのコード (`en-us` など) を含めるべきではありません。 英語のコンテンツ内のリンクにロケールのコードを含めた場合、それはローカライズされたリンクにも含まれることになり、ローカライズのエクスペリエンスが損なわれます。 たとえば、ドイツ語にローカライズされたコンテンツ内のリンクが `en-us` を含んでいた場合、ドイツ語を使用するお客様が、ドイツ語の記事があるにもかかわらず英語の記事にリンクされることになります。

Microsoft のサイトへのリンクからロケールのコードを削除してください。 例を次に示します。

変更前:

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

変更後:

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

以下のサイトはこの検証の対象に含まれます。

- azure.microsoft.com
- docs.microsoft.com
- msdn.microsoft.com
- technet.microsoft.com