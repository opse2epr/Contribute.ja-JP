---
title: validation-timeout
description: Docs のビルドに関するイシュー validation-timeout の説明と解決方法
author: meganbradley
ms.author: mbradley
ms.topic: error-reference
ms.date: 6/5/2019
ms.prod: non-product-specific
ms.openlocfilehash: 00461768491c25b9bafaff6b117a356d9e291e22
ms.sourcegitcommit: 412ce4ab23e758d41947043f1463e96595ba3bfe
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/12/2019
ms.locfileid: "67033299"
---
# <a name="validation-timeout"></a><span data-ttu-id="1141d-103">validation-timeout</span><span class="sxs-lookup"><span data-stu-id="1141d-103">validation-timeout</span></span>

## <a name="warning"></a><span data-ttu-id="1141d-104">警告</span><span class="sxs-lookup"><span data-stu-id="1141d-104">Warning</span></span>

`The call to the validation service timed out and validation was not completed. This happens when there's an issue with the service and continuing to retry the call could cause build delays. You might have content issues that were not reported. To retry validation, close and re-open your PR, or rebuild your branch via Docs Portal (requires admin permissions). If you need admin help or  If you continue to see this message, file an issue via https://SiteHelp.`

<span data-ttu-id="1141d-105">サーバーが正常な状態ではない場合など、検証サービスの一時的なイシューによって、Docs のビルドによりそのサービスを正常に呼び出せない場合があります。</span><span class="sxs-lookup"><span data-stu-id="1141d-105">Sometimes transient issues in the validation service, such as a server in a bad state, prevent Docs Build from successfully calling the service.</span></span> <span data-ttu-id="1141d-106">ビルドの遅延やビルド パイプラインの渋滞を回避するために、数回の試行の後、呼び出しはタイムアウトになり、検証はキャンセルされます。</span><span class="sxs-lookup"><span data-stu-id="1141d-106">After several tries, the call times out and validation is canceled to avoid build delays and clogging the build pipeline.</span></span>

## <a name="resolution"></a><span data-ttu-id="1141d-107">解決方法</span><span class="sxs-lookup"><span data-stu-id="1141d-107">Resolution</span></span>

<span data-ttu-id="1141d-108">PR を閉じてからもう一度開いてみます。または Docs ポータルを使用して手動ビルドを再実行します (リポジトリ管理者のみ)。</span><span class="sxs-lookup"><span data-stu-id="1141d-108">Try closing and re-opening your PR, or re-running a manual build via Docs Portal (repo admins only).</span></span> <span data-ttu-id="1141d-109">多くの場合、最初の再試行後に、サービスのイシューは自動的にクリアされます。</span><span class="sxs-lookup"><span data-stu-id="1141d-109">Often service issues clear themselves up after the initial retry.</span></span> <span data-ttu-id="1141d-110">管理者のヘルプが必要、または引き続きメッセージが表示される場合、お客様が Microsoft の従業員である場合は、[https://SiteHelp](https://SiteHelp) 経由でイシューをご提出ください。お客様が外部の共同作成者である場合は、ご自分の PR 内で記事の作成者を @ で言及し、サポートをご依頼ください。</span><span class="sxs-lookup"><span data-stu-id="1141d-110">If you need help from an admin or if you continue to get this message, file an issue via [https://SiteHelp](https://SiteHelp) if you're a Microsoft employee, or @ mention the author of an article in your PR for assistance if you're an external contributor.</span></span>

<!--make sure to add this file to your includes folder and verify the path-->
[!INCLUDE [validation-reference-help](includes/validation-reference-help.md)]
