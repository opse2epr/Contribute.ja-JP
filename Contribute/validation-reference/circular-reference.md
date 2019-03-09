---
title: circular-reference
description: Docs のビルドの問題 circular-reference に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: 4600465cf940efa82c61bcbac4a1d912c16e6903
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459213"
---
# <a name="circular-reference"></a>circular-reference

## <a name="error"></a>エラー

`Files '{file name 1}' and '{file name 2}' reference each other.`

たとえば、これは現在のファイルにリンクされているインクルード ファイルである可能性もあれば、現在のファイルにリダイレクトされたファイルへのリンクである可能性もあります。

## <a name="resolution"></a>解決方法

ファイル内のリンクを確認し、ファイルがそれ自体にリンクしないように、またはファイルにそれ自体が含まれないように必要な編集を行います。

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
