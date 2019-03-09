---
title: yaml-header-invalid
description: Docs のビルドの問題 yaml-header-invalid に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/26/2019
ms.prod: non-product-specific
ms.openlocfilehash: 62b3b2c2aa47525cae5dd5c0955eb88463124359
ms.sourcegitcommit: 89eb357721b26710e00d9b8fdab3e7628c34bdb6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/06/2019
ms.locfileid: "57459029"
---
# <a name="yaml-header-invalid"></a><span data-ttu-id="27f86-103">yaml-header-invalid</span><span class="sxs-lookup"><span data-stu-id="27f86-103">yaml-header-invalid</span></span>

## <a name="warning"></a><span data-ttu-id="27f86-104">警告</span><span class="sxs-lookup"><span data-stu-id="27f86-104">Warning</span></span>

`Invalid YAML header: Improper use of a colon in a metadata entry.`

<span data-ttu-id="27f86-105">通常、これは、YAML ヘッダー内の引用符なしのメタデータ値にコロンまたは別の特殊文字が含まれていることを意味します。</span><span class="sxs-lookup"><span data-stu-id="27f86-105">Usually this means an unquoted metadata value in a YAML header includes a colon or another special character.</span></span> <span data-ttu-id="27f86-106">また、キーと値のペア内のコロンの後にスペースが欠落していることを意味している場合もあります。</span><span class="sxs-lookup"><span data-stu-id="27f86-106">It can also mean that a space is missing after the colon in a key/value pair.</span></span>

## <a name="resolution"></a><span data-ttu-id="27f86-107">解決方法</span><span class="sxs-lookup"><span data-stu-id="27f86-107">Resolution</span></span>

<span data-ttu-id="27f86-108">ご利用の YAML ヘッダーを確認します。</span><span class="sxs-lookup"><span data-stu-id="27f86-108">Review your YAML header.</span></span> <span data-ttu-id="27f86-109">次の間違いを探します。</span><span class="sxs-lookup"><span data-stu-id="27f86-109">Look for the following mistakes.</span></span>

<span data-ttu-id="27f86-110">引用符なしの値内のコロン: </span><span class="sxs-lookup"><span data-stu-id="27f86-110">Colon in unquoted value:</span></span>

```yml
---
title: Common mistake: I included a colon in my unquoted value.
---
```

<span data-ttu-id="27f86-111">次の内容に変更: </span><span class="sxs-lookup"><span data-stu-id="27f86-111">Change to:</span></span>

```yml
---
title: 'Common mistake: I included a colon in my unquoted value.'
---
```

<span data-ttu-id="27f86-112">キーと値のペア内のコロンの後にスペースがない: </span><span class="sxs-lookup"><span data-stu-id="27f86-112">No space after colon in key/value pair:</span></span>

```yml
---
title:I omitted a space.
---
```

<span data-ttu-id="27f86-113">次の内容に変更: </span><span class="sxs-lookup"><span data-stu-id="27f86-113">Change to:</span></span>

```yml
---
title: I omitted a space.
---
```

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
