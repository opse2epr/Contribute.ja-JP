---
title: ms-service-missing
description: Docs のビルドの問題 ms-service-missing に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/2/2019
ms.prod: non-product-specific
ms.openlocfilehash: 7c5860d9ef50598ad5b3e9546100af0ba436e69f
ms.sourcegitcommit: 42e5a6ae071826afc2a32a9b7150ca113b39afdf
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/19/2019
ms.locfileid: "57987723"
---
# <a name="ms-service-missing"></a>ms-service-missing

**準備中**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>提案

`Missing attribute: ms.service. If you specify ms.subservice, you must also specify ms.service.`

`ms.service` を使ってクラウド サービスを指定します。 `ms.service` に関する詳細情報を指定する場合は、必要に応じて `ms.subservice` を指定できます。ただし、`ms.subservice` を指定する場合は、`ms.service` も指定する必要があります。 `ms.service` と `ms.subservice` に対する値は有効なペアである必要があります。

## <a name="resolution"></a>解決方法

指定した `ms.subservice` の値がご自分の記事に対して適切かどうか確認します。 次に、`ms.subservice` の有効な親となる、適切な `ms.service` の値を追加します。

有効な値は、[こちらの Microsoft 内部サイト](https://docsmetadatatool.azurewebsites.net/allowlists)にあります。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
