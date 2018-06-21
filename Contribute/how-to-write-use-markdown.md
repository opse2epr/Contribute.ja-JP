---
title: ドキュメントを記述するための Markdown の使用方法
description: この記事では、docs.microsoft.com の記事を記述するために使用される Markdown の基礎と参照情報について説明します。
ms.date: 07/13/2017
ms.openlocfilehash: dca1ccba2ae4ebd08b6039f5d780e7a7ac92e79f
ms.sourcegitcommit: 92aef5ea8bdd692c5c393d5c8f99b9e4f672ef2b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/19/2018
ms.locfileid: "36238968"
---
# <a name="how-to-use-markdown-for-writing-docs"></a>ドキュメントを記述するための Markdown の使用方法

docs.microsoft.com の記事は [Markdown](https://daringfireball.net/projects/markdown/) という読みやすく、しかも簡単に学べる軽量マークアップ言語で記述されます。 そのため、これは急速に業界標準になりました。

Docs のコンテンツは GitHub に格納されるので、[GitHub Flavored Markdown (GFM)](https://help.github.com/categories/writing-on-github/) と呼ばれる Markdown の上位セットを使用できます。GFM は一般的な書式要件のための追加機能を提供します。 さらに、Open Publishing Services (OPS) は Markdown パーサー Markdig を実装しています。 Markdig は GitHub Flavored Markdown (GFM) との互換性が高く、Docs 固有の機能を実現するための機能を提供します。

* Markdig は高速で、強力で、CommonMark に準拠した、.NET 向けの拡張可能なマークダウン プロセッサーです。
* https://github.com/lunet-io/markdig
* 優れたコミュニティ サポート
* 優れた標準サポート

## <a name="markdown-basics"></a>Markdown の基本

### <a name="headings"></a>見出し

見出しを作成するには、ハッシュ記号 (#) を次のように使用します。

```markdown
    # This is heading 1
    ## This is heading 2
    ### This is heading 3
    #### This is heading 4
```

### <a name="bold-and-italic-text"></a>太字や斜体のテキスト

テキストの書式を**太字**に設定するには、テキストを二重のアスタリスクで囲みます。

```markdown
    This text is **bold**.
```

テキストの書式を*斜体*に設定するには、テキストを一重のアスタリスクで囲みます。

```markdown
    This text is *italic*.
```

テキストの書式を***太字と斜体***の両方に設定するには、テキストを三重のアスタリスクで囲みます。

```markdown
    This is text is both ***bold and italic***.
```

### <a name="lists"></a>リスト

#### <a name="unordered-list"></a>記号付きリスト

記号付きリスト/箇条書きリストの書式を設定するには、アスタリスクまたはダッシュを使用できます。 たとえば、次の Markdown 書式は

```markdown
- List item 1
- List item 2
- List item 3
```

次のようにレンダリングされます。

- List item 1
- List item 2
- List item 3

リストを別のリスト内にネストするには、子リスト アイテムをインデントします。 たとえば、次の Markdown 書式は

```markdown
- List item 1
  - List item A
  - List item B
- List item 2
```

次のようにレンダリングされます。

- List item 1
  - List item A
  - List item B
- List item 2

#### <a name="ordered-list"></a>番号付きリスト

番号付きリスト/段階的リストの書式を設定するには、対応する番号を使用します。 たとえば、次の Markdown 書式は

```markdown
1. First instruction
2. Second instruction
3. Third instruction
```

次のようにレンダリングされます。

1. 第 1 手順
2. 第 2 手順
3. 第 3 手順

リストを別のリスト内にネストするには、子リスト アイテムをインデントします。 たとえば、次の Markdown 書式は

```markdown
1. First instruction
    1. Sub-instruction
    2. Sub-instruction
2. Second instruction
```

次のようにレンダリングされます。

1. 第 1 手順
    1. 下位手順
    2. 下位手順
2. 第 2 手順

### <a name="tables"></a>表

Markdown の基本仕様には表が含まれていませんが、GFM が表をサポートしています。 パイプ (|) 記号とハイフン記号 (-) を使用して表を作成できます。 ハイフンは各列のヘッダーを作成し、パイプは各列を区切ります。 表が正しくレンダリングされるように、表の前に空の行を 1 つ挿入してください。

たとえば、次の Markdown 書式は

```markdown
| Fun                  | With                 | Tables          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |
```

次のようにレンダリングされます。

| Fun                  | With                 | 表          |
| :------------------- | -------------------: |:---------------:|
| left-aligned column  | right-aligned column | centered column |
| $100                 | $100                 | $100            |
| $10                  | $10                  | $10             |
| $1                   | $1                   | $1              |

表作成の詳細については、以下の情報源をご覧ください。

- 横に長い表の書式設定に役立つ、Markdig の「[表を折り返す機能](#table-wrapping)」
- GitHub の「[Organizing information with tables (表を使用した情報の整理)](https://help.github.com/articles/organizing-information-with-tables/)」
- [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) Web アプリ
- Adam Pritchard 氏の「[Markdown Cheatsheet (Markdown に関する簡易参照ガイド)](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#wiki-tables)」
- Michel Fortin 氏の [Markdown Extra](https://michelf.ca/projects/php-markdown/extra/#table) に関するページ
- [HTML テーブルからマークダウンへの変換](https://jmalarcon.github.io/markdowntables/)

### <a name="links"></a>リンク

インライン リンクの Markdown 構文では、ハイパーリンクされるテキスト部分 `[link text]` の後に、リンク先 URL またはファイル名の部分 `(file-name.md)` が続きます。

 `[link text](file-name.md)`

リンクの詳細については、以下の情報源をご覧ください。

- Markdown のリンクの基本的なサポートについては、[Markdown の構文](https://daringfireball.net/projects/markdown/syntax#link)に関するセクション。
- Markdig で提供されるその他のリンク構文の詳細については、このガイドの[リンク](how-to-write-links.md)に関するセクション。

### <a name="code-snippets"></a>コード スニペット

Markdown では、コード スニペットの配置方法として、文中へのインライン配置と、文と文の間への "フェンスされた" 個別ブロックとしての配置の両方がサポートされます。 詳細については、以下の情報源をご覧ください。

- [Markdown のコード ブロックのネイティブ サポート](https://daringfireball.net/projects/markdown/syntax#precode)に関するセクション
- [GFM のコード フェンスと構文強調表示のサポート](https://help.github.com/articles/creating-and-highlighting-code-blocks/)に関するページ

コード ブロックをフェンスすることで、コード スニペットの構文を強調表示することができます。 フェンスされたコード ブロックの一般的な書式は次のようになります。

    ```alias
    ...
    your code goes in here
    ...
    ```

冒頭の 3 つのバッククォート (`) 記号に続くエイリアスは、使用される構文強調表示を定義します。 以下は Docs コンテンツで一般的に使用されるプログラミング言語と、対応するラベルのリストです。

これらの言語は、フレンドリ名をサポートし、ほとんどに言語の強調表示機能があります。

|名前|Markdown ラベル|
|-----|-------|
|.NET コンソール|dotnetcli|
|ASP.NET (C#)|aspx-csharp|
|ASP.NET (VB)|aspx-vb|
|AzCopy|azcopy|
|Azure CLI|azurecli|
|Azure PowerShell|azurepowershell|
|C++|cpp|
|C++/CX|cppcx|
|C++/WinRT|cppwinrt|
|C#|csharp|
|CSHTML|cshtml|
|DAX|dax|
|F#|fsharp|
|Go|go|
|HTML|html|
|HTTP|http|
|Java|java|
|JavaScript|javascript|
|JSON|json|
|Markdown|md|
|NodeJS|nodejs|
|Objective-C|objc|
|OData|odata|
|PHP|php|
|Power Apps Formula|powerappsfl|
|PowerShell|powershell|
|Python|python|
|Q#|qsharp|
|Ruby|ruby|
|SQL|sql|
|Swift|swift|
|TypeScript|typescript|
|VB|vb|
|VSTS CLI|vstscli|
|XAML|xaml|
|XML|xml|

#### <a name="example-c"></a>例: C\#

__Markdown__

    ```csharp
    // Hello1.cs
    public class Hello1
    {
        public static void Main()
        {
            System.Console.WriteLine("Hello, World!");
        }
    }
    ```

__レンダー__

```csharp
// Hello1.cs
public class Hello1
{
    public static void Main()
    {
        System.Console.WriteLine("Hello, World!");
    }
}
```

#### <a name="example-sql"></a>例: SQL

__Markdown__

    ```sql
    CREATE TABLE T1 (
      c1 int PRIMARY KEY,
      c2 varchar(50) SPARSE NULL
    );
    ```

__レンダー__

```sql
CREATE TABLE T1 (
  c1 int PRIMARY KEY,
  c2 varchar(50) SPARSE NULL
);
```

## <a name="ops-custom-markdown-extensions"></a>OPS による Markdown のカスタム拡張機能

> [!NOTE]
> Open Publishing Services (OPS) は GitHub Flavored Markdown (GFM) との互換性が非常に高い Markdown パーサー Markdig を実装しています。 Markdig は Markdown 拡張機能を介していくつかの機能を追加しています。 そのため、完全版の「OPS Authoring Guide」 (OPS オーサリング ガイド) の一部の記事は、参考のためにこのガイドに含まれています  (たとえば、目次の「Markdig and Markdown extensions」(Markdig と Markdown の拡張機能) と「Code snippets」(コード スニペット) をご覧ください)。

Docs 記事では、段落、リンク、リスト、見出しなど、ほとんどの書式設定に GFM が使用されます。 記事の高度な書式設定には、次のような Markdig 機能を使用できます。

- 注ブロック
- インクルード
- セレクター
- 埋め込みビデオ
- コード スニペット/サンプル

完全なリストについては、目次の「Markdig and Markdown extensions」(Markdig と Markdown の拡張機能) と「Code snippets」(コード スニペット) をご覧ください。

### <a name="note-blocks"></a>注ブロック

特定の内容に注目を集めるには、4 つのタイプの注ブロックから選択できます。

- NOTE (注意)
- WARNING (警告)
- TIP (ヒント)
- IMPORTANT (重要)

注ブロックによって文章がわかりにくくなることがあるので、概して注ブロックは控えめに使用する必要があります。 注ブロックでもコード ブロック、イメージ、リスト、およびリンクがサポートされますが、注ブロックを簡潔でわかりやすくするように心掛けてください。

### <a name="includes"></a>インクルード

再利用可能なテキスト ファイルまたはイメージ ファイルを記事ファイルにインクルードする必要がある場合は、Markdig のファイル インクルード機能を使用して "インクルード" ファイルを参照できます。 この機能は、ビルド時に特定のファイルを記事ファイルにインクルードするように OPS に指示します。これにより、その指定されたファイルは公開記事に含まれるようになります。 コンテンツの再利用に役立つ 3 つのタイプのインクルードがあります。

- インライン: 一般的なテキスト スニペットを別の文中にインラインで再利用できます。
- ブロック: Markdown ファイル全体をブロックとして再利用し、記事のセクション内にネストできます。
- イメージ: これは Docs に実装されている標準的なイメージ インクルードの方法です。

インラインまたはブロックによるインクルードは簡易な Markdown (.md) ファイルにすぎません。 これにはあらゆる有効な Markdown を含めることができます。 すべてのインクルード Markdown ファイルは、リポジトリのルートにある[共通の `/includes` サブディレクトリ](git-github-fundamentals.md#includes-subdirectory)に配置する必要があります。 記事が公開されると、インクルードされたファイルはその記事にシームレスに統合されます。

インクルードに関する要件と考慮事項を次に示します。

- 複数の記事に同じテキストを表示する必要があるときには、インクルードを使用してください。
- ブロックによるインクルードは、1 つまたは 2 つの段落、共通の手順、共通のセクションといった分量の多いコンテンツに使用してください。 1 つの文よりも小さい場合には、使用しないでください。
- インクルードは Markdig 拡張機能に依存するため、GitHub がレンダリングした記事にインクルードはレンダリングされません。 公開後にのみレンダリングされます。
- インクルード内のすべてのテキストの記述には、インクルードを参照する記事内の先行テキストや後続テキストに依存しない完全な文または語句を使用してください。 このガイダンスを無視すると、ローカライズされたエクスペリエンスを乱す翻訳不可能な文字列が記事内に発生します。
- インクルードをほかのインクルード内に埋め込まないでください。 それはサポートされていません。
- メディア ファイルは、インクルードのサブディレクトリ内にあるメディア フォルダーに配置する必要があります。たとえば、`<repo>`/includes/media フォルダーです。 メディア ディレクトリのルートにはイメージを配置しないでください。 イメージがないインクルードの場合は、対応するメディア ディレクトリは不要です。
- 通常の記事と同様に、インクルード ファイル間でメディアを共有しないでください。 インクルードおよび記事ごとに、一意の名前を持つ個別ファイルを使用してください。 インクルードに関連するメディア フォルダー内にメディア ファイルを格納してください。
- 記事の唯一のコンテンツとしてインクルードを使用しないでください。  インクルードの目的は、記事内のほかのコンテンツを補完することです。

### <a name="selectors"></a>セレクター

同じ技術記事の複数のバージョンを記述するときには、複数のテクノロジまたはプラットフォームの実装の違いに対応するために、セレクターを使用します。 通常、これが最も当てはまるのは、Microsoft の開発者向けのモバイル プラットフォームのコンテンツです。 現在 Markdig にはシングル セレクターとマルチ セレクターという 2 つのタイプのセレクターがあります。

選択範囲内の各記事に配置されるセレクター Markdown は同じであるため、記事のセレクターをインクルードに配置することをお勧めします。 そのうえで、同じセレクターを使用するすべての記事でそのインクルードを参照できます。

### <a name="code-snippets"></a>コード スニペット

Markdig では、コード スニペット拡張機能を使用した記事へのコードの高度なインクルードがサポートされます。 プログラミング言語の選択や構文の色分けといった GFM 機能に基づく高度なレンダリングに加えて、次のような便利な機能を使用できます。

- 外部リポジトリから集められたコード サンプル/スニペットのインクルード。
- さまざまな言語でのさまざまなバージョンのコード サンプルをタブに表示する UI。

## <a name="gotchas-and-troubleshooting"></a>問題の発見 + トラブルシューティング

### <a name="alt-text"></a>alt テキスト

アンダー スコアを含む alt テキストは正しくレンダリングされません。 たとえば、次のテキストを使用するのではなく、

```markdown
![ADextension_2FA_Configure_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

次のようにアンダー スコアをエスケープします。

```markdown
![ADextension\_2FA\_Configure\_Step4] (./media/bogusfilename/ADextension_2FA_Configure_Step4.PNG)
```

### <a name="apostrophes-and-quotation-marks"></a>アポストロフィと引用符

Word から Markdown エディターにコピーしたテキストに、"スマート" (カールした) アポストロフィまたは引用符が含まれていることがあります。 これらを標準的なアポストロフィや引用符にエンコードまたは変更する必要があります。 そうしないと、ファイルが公開されたときに Itâ€™s のように表示されます

これらの "スマート" バージョンの記述記号のエンコーディングは次のとおりです。

- 左 (始め) 二重引用符: `&#8220;`
- 右 (終わり) 二重引用符: `&#8221;`
- 右 (終わり) 一重引用符またはアポストロフィ: `&#8217;`
- 左 (始め) 一重引用符 (あまり使用されません): `&#8216;`

### <a name="angle-brackets"></a>山かっこ

プレースホルダーを示すためなどに、ファイル内の (コードではなく) テキストに山かっこを使用する場合は、山かっこを手動でエンコードする必要があります。 そうしないと、それらのテキストは Markdown によって HTML タグとして認識されます。

たとえば、`<script name>` を `&lt;script name&gt;` にエンコードしてください。

## <a name="see-also"></a>関連項目

### <a name="markdown-resources"></a>Markdown に関するリソース

- [Markdown 入門](https://daringfireball.net/projects/markdown/syntax)
- [Docs の Markdown に関する簡易参照ガイド](./media/documents/markdown-cheatsheet.pdf?raw=true)
- [GitHub の Markdown の基本](https://help.github.com/articles/markdown-basics/)
