---
title: included-file-redirected
description: Docs のビルドの問題 included-file-redirected に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 3/1/2019
ms.prod: non-product-specific
ms.openlocfilehash: 8a40f04fe1a7e7f19ab9ee7ce684684184aa4dc7
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459075"
---
# <a name="included-file-redirected"></a>included-file-redirected

## <a name="warning"></a>警告

`Included file '{include path}' is redirected to '{target file path}'. Only include files that are not redirected and that are located in an includes folder.`

## <a name="resolution"></a>解決方法

リダイレクトされたファイルが含まれないようにご自分のコンテンツを再構築します。 たとえば、新しいファイルを作成してリンクへの参照またはリンクを含めるか、含まれているリンクへの参照またはリンクを削除するか、コンテンツをインラインで作成します。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
