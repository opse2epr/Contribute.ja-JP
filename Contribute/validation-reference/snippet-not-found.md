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
# <a name="snippet-not-found"></a>snippet-not-found

## <a name="warning"></a>警告

`Code snippet '{snippet path}' not found.`

指定したパスにコード スニペットの参照が存在していないか、またはそのパスを現在のファイルから使用できません。

## <a name="resolution"></a>解決方法

[!INCLUDE [docs-authoring-pack](includes/docs-authoring-pack.md)]

ご利用のスニペット パスが正しいことを確認します。 スニペットが現在のリポジトリの外に格納されている場合は、リポジトリを必ず依存リポジトリとして構成します。 詳細については、Microsoft 内部向けの[コード スニペットに関する記事](https://review.docs.microsoft.com/en-us/help/contribute/code-in-docs?branch=master)を参照してください。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
