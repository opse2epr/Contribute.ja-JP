---
title: xref-not-found
description: Docs のビルドの問題 xref-not-found に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: d51eace291bfac179be2701463d113c06627f92f
ms.sourcegitcommit: 4053577bd0478d711257a283ee661d618b49c2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/05/2019
ms.locfileid: "57427873"
---
# <a name="xref-not-found"></a>xref-not-found

## <a name="warning"></a>警告

`Cross reference not found: '<xref: {uid}>'.`

`Cross reference not found: '@{uid}'.`

リンク先の UID が存在していないか、またはご利用のリポジトリでは使用できません。

## <a name="resolution"></a>解決方法

Microsoft 内部向けの [Xref Service](https://review.docs.microsoft.com/en-us/help/onboard/admin/xref-service?branch=master) に関するドキュメントの説明に従って、UID が正しいこと、およびご利用のリポジトリ上で Xref Service が適切に構成されていることを確認します。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
