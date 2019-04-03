---
title: ms-prod-service-mismatch
description: Docs のビルドの問題 ms-prod-service-mismatch に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: a8d1698a4842ace0e5dd07db170f40a310c666a6
ms.sourcegitcommit: 8e897e90268a8a87dc4b97d7c28d22ed5950c8d9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/29/2019
ms.locfileid: "58636795"
---
# <a name="ms-prod-service-mismatch"></a>ms-prod-service-mismatch

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>提案

`Invalid attribute pair: ms.prod and ms.subservice. You can only pair ms.prod with ms.technology.`

`Invalid attribute pair: ms.service and ms.technology. You can only pair ms.service with ms.subservice.`

オンプレミスの製品を指定する場合は `ms.prod` を、クラウド サービスの場合は `ms.service` を使います。 `ms.prod` に関する詳細情報を指定する場合は、必要に応じて `ms.technology` を指定できます。 `ms.service` に関する詳細情報を指定する場合は、`ms.subservice` を指定できます。 `ms.prod` と `ms.subservice`、または `ms.service` と `ms.technology` は併用できません。

## <a name="resolution"></a>解決方法

まず、ご自分の記事に対して適切な親属性 (`ms.prod` または `ms.service`) を選択したことを確認します。 次に、適切な子のフィールドを、有効なペアの値と共に追加します。 余分なフィールドはすべて削除します。

有効な値は、[こちらの Microsoft 内部サイト](https://docsmetadatatool.azurewebsites.net/allowlists)にあります。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
