---
title: コンテンツ オーサリング ツールのインストール
description: この記事は、Git、および Markdown ファイルの編集に必要なクライアント ツールのダウンロードとインストールに役立ちます。
author: bryanla
ms.author: bryanla
manager: mbaldwin
ms.date: 01/04/2018
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: external-contributor-guide
ms.openlocfilehash: 62c4b234f23b470ffea33cacdfc469fbd7e526bd
ms.sourcegitcommit: dd1b4e915f4996ac029d2a0704ced785438d3484
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2018
---
# <a name="install-content-authoring-tools"></a>コンテンツ オーサリング ツールのインストール

この記事では、Git クライアント ツールと Visual Studio Code を対話形式でインストールする手順について説明します。
> [!div class="checklist"]
> * [Git for Windows](https://git-scm.com/download/win) をインストールする
> * [Visual Studio Code](https://code.visualstudio.com/) をインストールする

>[!IMPORTANT]
> 記事に軽微な変更しか加えていない場合は、この記事の手順を実行する必要は*ない*ため、直接[軽微な/低頻度の変更のワークフロー](light-workflow.md)に進めます。
>
> 大規模な変更を行う共同作成者は、これらの手順を実行することをお勧めします。そうすることで、[大規模/長期間の変更のワークフロー](full-workflow.md)を使用できるようになります。 メイン リポジトリで書き込みアクセス許可を持っている場合でも、"*リポジトリのフォークと複製を行うことを強くお勧めします (本ガイドでもそれを前提としています)*"。それにより、予定している変更をフォークに保存するための読み取り/書き込み権限が付与されます。

## <a name="install-git-client-tools-on-windows"></a>Git クライアント ツールを Windows にインストールする

 [Software Freedom Conservancy の Git クライアント ツール](https://git-scm.com/download/)の最新バージョンをインストールします。 インストールには、Git バージョン管理システムや、ローカル Git リポジトリとの対話で使用するコマンドライン アプリである Git Bash が含まれます。

コマンド ライン インターフェイス (CLI) ではなくグラフィカル ユーザー インターフェイス (GUI) を使用する場合は、[Software Freedom Conservancy の使用可能な GUI クライアントに関するページ](https://git-scm.com/downloads/guis)、[GitHub の GitHub デスクトップ](https://desktop.github.com/)に関するページ、[Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx) のページで、一部の一般的なオプションを確認してください。

選択したクライアントについてインストールと構成の手順に従います。

次の記事では、[ローカル Git リポジトリを設定](get-started-setup-local.md)します。

   Git の追加のリソースは、[Git 用語集](https://help.github.com/articles/github-glossary) | [Git の基礎](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics) | [Git および GitHub の学習](https://help.github.com/articles/good-resources-for-learning-git-and-github/)にあります

## <a name="understand-markdown-editors"></a>Markdown エディターについて

Markdown は、読みやすく、かつ習得しやすい軽量のマークアップ言語です。 そのため、急速に業界標準になりました。 Markdown で記事を書くには、まず、Markdown エディターをダウンロードしてインストールすることをお勧めします。  [Visual Studio Code](https://code.visualstudio.com/) は、Markdown を編集するために Microsoft が推奨しているツールです。 [Atom](https://atom.io) も、Markdown を編集するための一般的なツールです。

Markdown テキストは、.md 拡張子の付いたファイルに保存されます。

Markdown の基本と OPS による Markdown のカスタム拡張機能でサポートされる機能を含む、Markdown での記述方法の詳細については、後述の「[Markdown の使用方法](how-to-write-use-markdown.md)」の記事で説明します。

## <a name="visual-studio-code"></a>Visual Studio Code

[Visual Studio Code](https://code.visualstudio.com/) は Windows、Linux、Mac で動作する軽量のエディターで、VS Code とも呼ばれます。 これには、git 統合と拡張機能のサポートが含まれています。

[VS Code](https://code.visualstudio.com/) をダウンロードしてインストールします。 VS Code のホーム ページでは、オペレーティング システムが正しく検出されます。

- [Windows](https://code.visualstudio.com/docs/setup/windows)
- [Mac](https://code.visualstudio.com/docs/setup/mac)
- [Linux](https://code.visualstudio.com/docs/setup/linux)

> [!TIP]
> VS Code を起動し、現在のフォルダーを開き、コマンド ラインまたは bash シェルで `code .` コマンドを実行します。 現在のフォルダーがローカル git リポジトリの一部である場合は、github 統合が Visual Studio Code に自動的に表示されます。

## <a name="next-steps"></a>次のステップ

これで、[ローカル Git リポジトリを設定](get-started-setup-local.md)する準備が整いました。
