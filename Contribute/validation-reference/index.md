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
# <a name="docs-pr-validation-service"></a><span data-ttu-id="7525e-101">Docs PR 検証サービス</span><span class="sxs-lookup"><span data-stu-id="7525e-101">Docs PR validation service</span></span>

<span data-ttu-id="7525e-102">Docs PR 検証サービスは、PR 内のファイルに検証ルールを適用する GitHub アプリです。</span><span class="sxs-lookup"><span data-stu-id="7525e-102">The Docs PR validation service is a GitHub app that runs validation rules on the files in a PR.</span></span>

<span data-ttu-id="7525e-103">リポジトリ上で検証サービスを有効にすると、次のように動作します。</span><span class="sxs-lookup"><span data-stu-id="7525e-103">When the validation service is enabled on a repo, you'll see the following behavior:</span></span>

1. <span data-ttu-id="7525e-104">PR を送信します。</span><span class="sxs-lookup"><span data-stu-id="7525e-104">You submit a PR.</span></span>
1. <span data-ttu-id="7525e-105">PR の状態を示す GitHub コメント内で、"checks" (チェック) の状態が有効になっているのをリポジトリで確認できます。</span><span class="sxs-lookup"><span data-stu-id="7525e-105">In the GitHub comment that indicates the status of your PR, you'll see the status of "checks" enabled on the repo.</span></span> <span data-ttu-id="7525e-106">この例では、2 つのチェック "Commit Validation" (コミットの検証) と "OpenPublishing.Build" が有効になっていることに注意します。</span><span class="sxs-lookup"><span data-stu-id="7525e-106">Note that in this example, there are two checks enabled, "Commit Validation" and "OpenPublishing.Build":</span></span>

   ![一部のチェックが失敗](media/validation-failed.png)

   <span data-ttu-id="7525e-108">コミットの検証に失敗した場合でも、ビルドを通すことができます。</span><span class="sxs-lookup"><span data-stu-id="7525e-108">Build can pass even if commit validation fails.</span></span>

1. <span data-ttu-id="7525e-109">**[Details]\(詳細\)** をクリックして詳細情報を確認します。</span><span class="sxs-lookup"><span data-stu-id="7525e-109">Click **Details** for more information.</span></span>
1. <span data-ttu-id="7525e-110">[Details]\(詳細\) ページには、失敗したすべての検証のチェックと、その問題を修正する方法に関する情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="7525e-110">On the Details page, you'll see all the validation checks that failed, with information about how to fix the issues:</span></span>

   ![検証メッセージ](media/validation-details.png)

<span data-ttu-id="7525e-112">現在サービスで利用できる検証の一覧については、この記事の左側にある目次をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="7525e-112">See the left-hand TOC of this article for the list of validations currently in the service.</span></span>