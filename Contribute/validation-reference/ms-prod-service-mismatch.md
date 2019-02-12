---
title: ms-prod-service-mismatch
description: Docs のビルドの問題 ms-prod-service-mismatch に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 1/15/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4a3cf8bc5435972f0442ca1d41d4147e1ea00d78
ms.sourcegitcommit: 203ca15fda2d217f082c74ec648c1f1db323f9f1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/04/2019
ms.locfileid: "55713179"
---
# <a name="ms-prod-service-mismatch"></a>ms-prod-service-mismatch

**準備中**

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a>提案

`Invalid attribute pair: ms.prod and ms.subservice. You can only pair ms.prod with ms.technology.`

`Invalid attribute pair: ms.service and ms.technology. You can only pair ms.service with ms.subservice.`

オンプレミスの製品を指定する場合は `ms.prod` を、クラウド サービスの場合は `ms.service` を使います。 `ms.prod` に関する詳細情報を指定する場合は、必要に応じて `ms.technology` を指定できます。 `ms.service` に関する詳細情報を指定する場合は、`ms.subservice` を指定できます。 `ms.prod` と `ms.subservice`、または `ms.service` と `ms.technology` は併用できません。

## <a name="resolution"></a>解決方法

まず、ご自分の記事に対して適切な親属性 (`ms.prod` または `ms.service`) を選択したことを確認します。 次に、適切な子のフィールドを、有効なペアの値と共に追加します。 余分なフィールドはすべて削除します。

有効な値は、[こちらの Microsoft 内部サイト](https://docsmetadatatool.azurewebsites.net/whitelists)にあります。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
