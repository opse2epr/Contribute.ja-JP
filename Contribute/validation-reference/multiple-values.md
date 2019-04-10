---
title: multiple-values
description: Docs のビルドの問題 multiple-values に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/19/2019
ms.prod: non-product-specific
ms.openlocfilehash: 479472abfb771ae5b4dc77cab2bf94633f3ead5c
ms.sourcegitcommit: fdaff82fec769f4ce9153ff1e0f968d3ea97a76d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/03/2019
ms.locfileid: "58899661"
---
# <a name="multiple-values"></a><span data-ttu-id="26471-103">multiple-values</span><span class="sxs-lookup"><span data-stu-id="26471-103">multiple-values</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="26471-104">提案</span><span class="sxs-lookup"><span data-stu-id="26471-104">Suggestion</span></span>

`Single-valued attribute {attribute} has multiple values. Remove additional values.`

<span data-ttu-id="26471-105">単一の値しか許可されていない属性に対して、複数の値を指定しました。</span><span class="sxs-lookup"><span data-stu-id="26471-105">You specified more than one value for an attribute that is ony allowed one value.</span></span>

`Single-valued attribute {attribute} is in multi-valued array format. Change to scalar format.`

<span data-ttu-id="26471-106">複数の値を持つことが許可されていない属性は、単一値 (スカラー) の YML 形式で指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="26471-106">Attributes that aren't allowed to have more than one value must be specified in the single-valued (scalar) YML format.</span></span>

## <a name="resolution"></a><span data-ttu-id="26471-107">解決方法</span><span class="sxs-lookup"><span data-stu-id="26471-107">Resolution</span></span>

<span data-ttu-id="26471-108">複数値の配列を単一値の属性に対して使った場合、配列内に複数の値、単一の値のどちらが含まれていても、必ずこの提案が発生します。</span><span class="sxs-lookup"><span data-stu-id="26471-108">You get this Suggestion any time a multi-valued array is used for a single-valued attribute, either with multiple values or a single value in the array.</span></span>

<span data-ttu-id="26471-109">YML では、`ms.custom` などの複数値の属性に対して、次の配列形式がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="26471-109">YML supports the following array formats for multi-valued attributes, such as `ms.custom`:</span></span>

```yml
---
# comma-separated bracketed list:
ms.custom: [WIP, generated-via-CI]

# each value on its own line:
ms.custom:
  - WIP
  - generated-via-CI
---
```

<span data-ttu-id="26471-110">これらの形式は、`author` などの単一値の属性に対しては有効ではありません。</span><span class="sxs-lookup"><span data-stu-id="26471-110">These formats aren't valid for single-valued attributes, such as `author`.</span></span>

<span data-ttu-id="26471-111">複数の値を指定した場合は、指定した値を確認していずれが正しいのか判断します。</span><span class="sxs-lookup"><span data-stu-id="26471-111">If you specified multiple values, review the specified values and determine which is correct.</span></span> <span data-ttu-id="26471-112">次のように、他の値を削除し、同じ行に属性としてブラケットを含まない単一の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="26471-112">Remove other values and specify the single value on the same line as the attribute with no brackets, as follows:</span></span>

```yml
---
author: meganbradley
---
```

<span data-ttu-id="26471-113">単一値の配列がある場合は、それを上のスカラー形式に変更します。</span><span class="sxs-lookup"><span data-stu-id="26471-113">If you have a single-valued array, change it to the scalar format above.</span></span>

## <a name="attributes-in-scope"></a><span data-ttu-id="26471-114">スコープ内の属性</span><span class="sxs-lookup"><span data-stu-id="26471-114">Attributes in scope</span></span>

<span data-ttu-id="26471-115">次の属性は単一値である必要があります。</span><span class="sxs-lookup"><span data-stu-id="26471-115">The following attributes are required to be single-valued:</span></span>

- `author`
- `ms.author`
- `ms.date`
- `ms.prod`
- `ms.service`
- `ms.subservice`
- `ms.technology`
- `ms.topic`
- `title`

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
