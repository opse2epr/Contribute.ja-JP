---
author: meganbradley
ms.author: mbradley
ms.openlocfilehash: fa048980afcf3c50f7d990f9c88064df6ee5ebb5
ms.sourcegitcommit: 6f1997864c000a9cd25fb9171a8f8fdb8b5b5ece
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/11/2018
ms.locfileid: "49084630"
---
# <a name="docs-pr-validation-service"></a>Docs PR 検証サービス

Docs PR 検証サービスは、PR 内のファイルに検証ルールを適用する GitHub アプリです。

リポジトリ上で検証サービスを有効にすると、次のように動作します。

1. PR を送信します。
1. PR の状態を示す GitHub コメント内で、"checks" (チェック) の状態が有効になっているのをリポジトリで確認できます。 この例では、2 つのチェック "Commit Validation" (コミットの検証) と "OpenPublishing.Build" が有効になっていることに注意します。

   ![一部のチェックが失敗](media/validation-failed.png)

   コミットの検証に失敗した場合でも、ビルドを通すことができます。

1. **[Details]\(詳細\)** をクリックして詳細情報を確認します。
1. [Details]\(詳細\) ページには、失敗したすべての検証のチェックと、その問題を修正する方法に関する情報が表示されます。

   ![検証メッセージ](media/validation-details.png)

現在サービスで利用できる検証の一覧については、この記事の左側にある目次をご覧ください。