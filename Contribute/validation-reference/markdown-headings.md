---
title: マークダウン見出し
description: マークダウン見出しの要件について説明します。
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 05/03/2017
ms.openlocfilehash: 18beb815fdf7caad3e8e675e8d79853d8a5688f2
ms.sourcegitcommit: 6f1997864c000a9cd25fb9171a8f8fdb8b5b5ece
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/11/2018
ms.locfileid: "49084492"
---
# <a name="markdown-headings"></a>マークダウン見出し

OPS マークダウン ファイルの見出しには、次の検証要件が適用されます。

## <a name="h1"></a>H1

`H1` は、マークダウン ファイルの最初の見出しを参照します。 docs.microsoft.com に公開すると、H1 はページの上部に大きなフォントで表示されます。

H1 を作成するには、行を 1 つのハッシュ (`#`) とスペースで開始して、その後に見出しのテキストを続けます。 たとえば、この記事の H1 は次のようになります。

```md
# Markdown headings
```

H1 見出しには、次の規則が適用されます。

- ファイルには H1 を含める必要があります。
- H1 は 1 つだけ含めることができます。
- H1 には内容が必要です。

  ```markdown
  # 
  This is not allowed.
  ```
- `#` と H1 の内容の間にスペースが必要です。 H1 にスペースがなかった場合、公開されたページで見出しとして表示されません。

  ```markdown
  #This looks bad on the site.
  ```
- H1 は、YML メタデータ ヘッダーの後に来る、ファイルの最初のコンテンツにする必要があります。 YML ヘッダーの終端と H1 の間にコンテンツ (テキストやイメージなど) を置くことはできません。

  ```markdown
  ---
  ... YML would go here
  ---
  ![cheerful image](not-allowed.jpg)
  # This cheer is not allowed
  ```
- 最上位見出し向けの HTML 要素 (`<h1>`) は使用できません。 マークダウンの構文 (`# `) を使用します。
- H1 は 100 文字以内にする必要があります。 これはスタイルのガイドラインです。

## <a name="h2---h6"></a>H2 - H6

OPS では H2 (`## `) から H6 (`###### `) までを使用できます。 HTML (`<h2>` - `<h6>`) ではなくマークダウン ヘッダーを使用して、見出しを作成します。
