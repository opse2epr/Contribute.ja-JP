---
title: validation-timeout
description: Docs のビルドに関するイシュー validation-timeout の説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 6/5/2019
ms.prod: non-product-specific
ms.openlocfilehash: 018634b1c5fba0848fb36a70d81c46be9acf2ecd
ms.sourcegitcommit: 1e53d17639277bebd89b2e7cabeb45bdad526354
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/12/2019
ms.locfileid: "67024212"
---
# <a name="validation-timeout"></a><span data-ttu-id="fef08-103">validation-timeout</span><span class="sxs-lookup"><span data-stu-id="fef08-103">validation-timeout</span></span>

## <a name="warning"></a><span data-ttu-id="fef08-104">警告</span><span class="sxs-lookup"><span data-stu-id="fef08-104">Warning</span></span>

`The call to the validation service timed out and validation was not completed. This happens when there's an issue with the service and continuing to retry the call could cause build delays. You might have content issues that were not reported. To retry validation, close and open your PR. If you continue to see this message, file an issue via https://SiteHelp.`

<span data-ttu-id="fef08-105">サーバーが正常な状態ではない場合など、検証サービスの一時的なイシューによって、Docs のビルドによりそのサービスを正常に呼び出せない場合があります。</span><span class="sxs-lookup"><span data-stu-id="fef08-105">Sometimes transient issues in the validation service, such as a server in a bad state, prevent Docs Build from successfully calling the service.</span></span> <span data-ttu-id="fef08-106">ビルドの遅延やビルド パイプラインの渋滞を回避するために、3 回の試行の後、呼び出しはタイムアウトになり、検証はキャンセルされます。</span><span class="sxs-lookup"><span data-stu-id="fef08-106">After three tries, the call times out and validation is canceled to avoid build delays and clogging the build pipeline.</span></span>

## <a name="resolution"></a><span data-ttu-id="fef08-107">解決方法</span><span class="sxs-lookup"><span data-stu-id="fef08-107">Resolution</span></span>

<span data-ttu-id="fef08-108">PR を閉じてからもう一度開いてみます。または手動ビルドを再実行します (リポジトリ管理者のみ)。</span><span class="sxs-lookup"><span data-stu-id="fef08-108">Try closing and reopening your PR, or re-running a manual build (repo admins only).</span></span> <span data-ttu-id="fef08-109">多くの場合、最初の再試行後に、サービスのイシューは自動的にクリアされます。</span><span class="sxs-lookup"><span data-stu-id="fef08-109">Often service issues clear themselves up after the initial retry.</span></span> <span data-ttu-id="fef08-110">引き続きメッセージが表示される場合、お客様が Microsoft の従業員である場合は、[https://SiteHelp](https://SiteHelp) 経由でイシューをご提出ください。お客様が外部の共同作成者である場合は、ご自分の PR 内で記事の作成者を @ で言及し、サポートをご依頼ください。</span><span class="sxs-lookup"><span data-stu-id="fef08-110">If you continue to get the message, file an issue via [https://SiteHelp](https://SiteHelp) if you're a Microsoft employee, or @ mention the author of an article in your PR for assistance if you're an external contributor.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
