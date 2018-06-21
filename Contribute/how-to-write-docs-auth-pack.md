---
title: VS Code 用 Docs Authoring Pack
description: この記事では、docs.microsoft.com の Markdown の作成を促進する VS Code 拡張パックについて説明します。
author: meganbradley
ms.author: mbradley
manager: jemash
ms.date: 04/06/2018
ms.openlocfilehash: 0a6a793f568771347efce5d7b2d347210f9e5c70
ms.sourcegitcommit: 92aef5ea8bdd692c5c393d5c8f99b9e4f672ef2b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/19/2018
ms.locfileid: "36238899"
---
# <a name="docs-authoring-pack-for-vs-code"></a>VS Code 用 Docs Authoring Pack

Docs Authoring Pack は、docs.microsoft.com の Markdown の作成を支援する VS Code 拡張機能の集まりです。 このパックは、[VS Code Marketplace で入手可能であり](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)、次の拡張機能を含んでいます。

- **DocFx:** docs.microsoft.com 固有の Markdown のプレビューを含んでいます。 詳細については、[DocFx](https://marketplace.visualstudio.com/items?itemName=ms-docfx.DocFX) を参照してください。
- **markdownlint:** David Anson 氏による人気のある Markdown リンターで、ベスト プラクティスに従った Markdown を作成するために役立ちます。 詳細については、[markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint) を参照してください。
- **Docs Markdown:** Open Publishing System (OPS) での docs.microsoft.com コンテンツの Markdown 作成サポートを提供します。OPS での基本的な Markdown のサポートとカスタム Markdown 構文のサポートが含まれます。 このトピックの残りの部分では、Docs Markdown の拡張機能について説明します。

## <a name="prerequisites-and-assumptions"></a>前提条件

Docs Markdown 拡張機能を使用して、相対リンク、画像、その他の埋め込みコンテンツを正確に挿入するには、複製された OPS リポジトリのルートを対象範囲とした VS Code ワークスペースを持っている必要があります。

アラートやスニペットなどの拡張機能でサポートされる一部の構文は、OPS のカスタム Markdown であり、OPS を介して公開されない限り正しくレンダリングされません。

## <a name="how-to-use-the-docs-markdown-extension"></a>Docs Markdown 拡張機能の使用方法

Docs Markdown のメニューにアクセスするには、「`ALT+M`」と入力します。 上下の矢印をクリックまたは使用して、必要な機能を選択するか、フィルターの入力して開始し、メニューで必要な機能が強調表示されたら `ENTER` キーを押します。 次の機能を使用できます:

|機能     |コマンド             |説明           |
|-------------|--------------------|----------------------|
|太字         |`formatBold`        |テキストを**太字**に書式設定します。|
|斜体       |`formatItalic`      |テキストを*斜体*に書式設定します。|
|コード         |`formatCode`        |1 つ以下の線が選択されているときに、テキストを `inline code` として書式設定します。<br><br>複数の線が選択されている場合、それらをフェンスされたコードのブロックとして書式設定します。オプションで OPS でサポートされているプログラミング言語を選択できます。|
|アラート        |`insertAlert`       |メモ、重要、警告、またはヒントを挿入します。<br><br>メニューからアラートを選択し、アラートの種類を選択します。 以前にテキストを選択している場合は、選択したアラートの構文でテキストが囲まれます。 テキストを選択していない場合は、プレースホルダーのテキストと共にアラートが追加されます。|
|番号付きリスト|`insertNumberedList` |新しい番号付きリストを挿入します。<br><br> 複数の行が選択されている場合は、各行がリスト項目になります。 Markdown 内の番号付きリストはすべて 1 として表示されますが、docs.microsoft.com では連番、または入れ子になったリストでは文字としてレンダリングされます。 入れ子になった番号付きリストを作成するには、親リスト内からタブを指定します。|
|箇条書き|`insertBulletedList` |新しい箇条書きを挿入します。|
|テーブル        |`insertTable`        |Markdown のテーブル構造を挿入します。<br><br>テーブル コマンドを選択した後で、3:4 のように列:行の形式で列と行の数を指定します。 この式で指定できる列の最大数は 5 です。読みやすくするためにこの最大数が推奨されます。|
|リンク         |`selectLinkType`      |リンクを挿入します。 このコマンドを選択すると、次のサブメニューが表示されます。<br><br>`External`: URI で Web ページにリンクします。 "http" または "https" を含める必要があります。<br>`Internal`: 同じリポジトリ内の別のファイルへの相対リンクを挿入します。 このオプションを選択した後で、コマンド ウィンドウに入力し、名前でフィルター処理し、必要なファイルを選択します。 <br>`Bookmark in this file`: 現在のファイルの見出しの一覧から選択し、適切に書式設定されたブックマークを挿入します。<br>`Bookmark in another file`: 最初に、ファイル名でフィルター処理して、リンク先のファイルを選択し、次に選択したファイル内の適切な見出しを選択します。|
|イメージ        |`insertImage`     |代替テキスト (アクセシビリティのために必要) を入力してそれを選択し、このコマンドを実行してリポジトリ内のサポートされる画像ファイルのリストをフィルター処理し、必要なファイルを選択します。 このコマンドを呼び出したときに代替テキストを選択していない場合、画像ファイルを選択する前に代替テキストを選択するように指示されます。|
|含める      |`insertInclude`   |現在のファイル内に埋め込むファイルを見つけます。|
|スニペット      |`insertSnippet`   |現在のファイル内に埋め込むリポジトリ内のコード スニペットを見つけます。|
|ビデオ        |`insertVideo`     |埋め込みビデオを追加します。|
|プレビュー      |`previewTopic`    |DocFX 拡張機能を使用し、左右に並べたウィンドウにアクティブなトピックのプレビューを表示します。  DocFX 拡張機能がインストールされていない場合またはインストールされていても無効になっている場合、トピックはレンダリングされません。


## <a name="how-to-assign-keyboard-shortcuts"></a>キーボード ショートカットの割り当て方法

1. 「`CTRL+K`」と入力し、「`CTRL+S`」と入力してキーボード ショートカットの一覧を開きます。
1. カスタム キーバインドを作成するコマンド (`formatBold` など) を検索します。
1. マウス ポインターを行の上に置いたときにコマンド名の近くに表示されるプラス記号をクリックします。
1. 新しい入力ボックスが表示されたら、特定のコマンドにバインドするキーボード ショートカットを入力します。 たとえば、太字の共通のショートカットを使用するには、「`ctrl+b`」と入力します。
1. Markdown 以外のファイルで使用できないようにするために、`when` 句をキーバインドに含めることをお勧めします。 これを行うには、*keybindings.json* を開き、コマンド名の下に次の行を挿入します (必ず行の間にコマンドを追加してください)。
   
    `"when": "editorTextFocus && editorLangId == 'markdown'"`

    keybindings.json 内の完成したキーバインドは次のようになります。

    ```json
    // Place your key bindings in this file to overwrite the defaults
    [
        {
            "key": "ctrl+b",
            "command": "formatBold",
            "when": "editorTextFocus && editorLangId == 'markdown'"
        }
    ]
    ```

1. keybindings.json を保存します。

詳細については、VS Code のドキュメントの[キーバインド](https://code.visualstudio.com/docs/getstarted/keybindings)を参照してください。

## <a name="how-to-show-the-legacy-gauntlet-toolbar"></a>レガシーの "Gauntlet" ツールバーの表示方法

"Gauntlet" という名前の拡張コードの以前のユーザーは、Docs Markdown 拡張機能がインストールされたときに VS Code ウィンドウの下部にオーサリング ツールバーが表示されなくなったことに気付くでしょう。 これは、ツールバーが VS Code ステータス バー上で多くの領域を使用し、拡張機能のユーザー エクスペリエンスのベスト プラクティスに従っていなかったために新しい拡張機能で非推奨になったためです。 しかし、オプションで VS Code の settings.json ファイルを次のように更新することでツールバーを表示できます。

1. VS Code で、[ファイル]、[基本設定]、[設定]、 (`CTRL+Comma`) の順に選択します。
1. [ユーザー設定] を選択してすべての VS Code ワークスペースの設定を変更するか、[ワークスペースの設定] を選択して、現在のワークスペースのみの設定を変更します。
1. [既定の設定] ウィンドウで、[Docs Authoring Extension Configuration]\(Docs Authoring 拡張機能の構成\) を見つけ、目的の設定の横にある鉛筆アイコンを選択します。 次に、`true` または `false` を選択するように指示されます。 選択すると、VS Code によって settings.json ファイルに自動的に値が追加され、変更を有効にするためにウィンドウを再び読み込むように指示されます。

## <a name="known-issues"></a>既知の問題

- DocFX Preview: MacOS および Linux: DocFX Preview でプレビューが正しく起動しない (これらのプラットフォームではプレビューは既定で VS Code Markdown プレビューになります)。
- DocFx Preview: すべてのプラットフォームで API への xref (相互参照) リンクなどの一部の構文が、プレビューで正しくレンダリングされない。場合によってはコンテンツ ページが閉じる。
- 外部ブックマーク: Linux でファイル リストが表示されるが、見出しが表示されない。
- 含む: Linux でファイル リストが表示されるが、選択を行った後でリンクが追加されない。
