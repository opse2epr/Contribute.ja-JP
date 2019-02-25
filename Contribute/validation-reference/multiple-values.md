---
title: multiple-values
description: Docs のビルドの問題 multiple-values に関する説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 2/19/2019
ms.prod: non-product-specific
ms.openlocfilehash: 8cee25b07e5bd1e019f8d270888eff73292d8e7c
ms.sourcegitcommit: ae71ca811c143deb6214147c7eea8704444a6093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/21/2019
ms.locfileid: "56465118"
---
# <a name="multiple-values"></a><span data-ttu-id="b5311-103">multiple-values</span><span class="sxs-lookup"><span data-stu-id="b5311-103">multiple-values</span></span>

<span data-ttu-id="b5311-104">**準備中**</span><span class="sxs-lookup"><span data-stu-id="b5311-104">**Coming soon!**</span></span>

[!INCLUDE [suggestion-note](includes/suggestion-note.md)]

## <a name="suggestion"></a><span data-ttu-id="b5311-105">提案</span><span class="sxs-lookup"><span data-stu-id="b5311-105">Suggestion</span></span>

`Single-valued attribute {attribute} has multiple values. Remove additional values.`

<span data-ttu-id="b5311-106">単一の値しか許可されていない属性に対して、複数の値を指定しました。</span><span class="sxs-lookup"><span data-stu-id="b5311-106">You specified more than one value for an attribute that is ony allowed one value.</span></span>

`Single-valued attribute {attribute} is in multi-valued array format. Change to scalar format.`

<span data-ttu-id="b5311-107">複数の値を持つことが許可されていない属性は、単一値 (スカラー) の YML 形式で指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5311-107">Attributes that aren't allowed to have more than one value must be specified in the single-valued (scalar) YML format.</span></span>

## <a name="resolution"></a><span data-ttu-id="b5311-108">解決方法</span><span class="sxs-lookup"><span data-stu-id="b5311-108">Resolution</span></span>

<span data-ttu-id="b5311-109">複数値の配列を単一値の属性に対して使った場合、配列内に複数の値、単一の値のどちらが含まれていても、必ずこの提案が発生します。</span><span class="sxs-lookup"><span data-stu-id="b5311-109">You get this Suggestion any time a multi-valued array is used for a single-valued attribute, either with multiple values or a single value in the array.</span></span>

<span data-ttu-id="b5311-110">YML では、`ms.custom` などの複数値の属性に対して、次の配列形式がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="b5311-110">YML supports the following array formats for multi-valued attributes, such as `ms.custom`:</span></span>

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

<span data-ttu-id="b5311-111">これらの形式は、`author` などの単一値の属性に対しては有効ではありません。</span><span class="sxs-lookup"><span data-stu-id="b5311-111">These formats aren't valid for single-valued attributes, such as `author`.</span></span>

<span data-ttu-id="b5311-112">複数の値を指定した場合は、指定した値を確認していずれが正しいのか判断します。</span><span class="sxs-lookup"><span data-stu-id="b5311-112">If you specified multiple values, review the specified values and determine which is correct.</span></span> <span data-ttu-id="b5311-113">次のように、他の値を削除し、同じ行に属性としてブラケットを含まない単一の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="b5311-113">Remove other values and specify the single value on the same line as the attribute with no brackets, as follows:</span></span>

```yml
---
author: meganbradley
---
```

<span data-ttu-id="b5311-114">単一値の配列がある場合は、それを上のスカラー形式に変更します。</span><span class="sxs-lookup"><span data-stu-id="b5311-114">If you have a single-valued array, change it to the scalar format above.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
