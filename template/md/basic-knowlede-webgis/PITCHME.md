---?color=#3A8FB7
@snap[breadcrumbs-wrap bluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [1. 基礎知識](#/0)
@olend
@snapend

@snap[west headline]
## 基礎知識
@snapend


---

@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [1. 基礎知識](#/0)
@olend
@snapend

### @css[slide-title](基礎知識)

@snap[slide-contents]

@box[rounded box-style](Webの仕組みやプログラミングに必要な知識を学びます。)

@snap[left-column]
@ol[numberlist numberlist-color2](false)
- [Webとは](#/5)
- [Webページとは](#/6)
- HTMLとは
- 小項目
- 小項目
- 小項目
@olend
@snapend


@snap[right-column]
@ol[numberlist numberlist-color2](false)
- アジェンダ項目内の小項目
- 小項目
- 小項目
- 小項目
- 小項目
- 小項目
@olend
@snapend

@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [1. 基礎知識](#/0)
- [1. Webとは]()
@olend
@snapend

### @css[slide-title](Webとは)

@snap[slide-contents]
@snap[quote-wrap]

@quote[<ul><li>World Wide **Web**（WWW、ワールド・ワイド・ウェブ）</li><li>Web（ウェブ）とも呼ばれる</li><li>「**インターネット**」という表現が<br>ワールド・ワイド・ウェブを指す場合もある</li><li>**世界中に張り巡らしたような、文書間のつながり**</li></ul>](https://ja.wikipedia.org/wiki/World_Wide_Web)

@quote[Webにおける情報の基礎的な単位は**ページ**<br>（Webページ、ウェブページ）](http://e-words.jp/w/Web.html)

@snapend
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [1. 基礎知識](#/0)
- [2. Webページとは]()
@olend
@snapend

### @css[slide-title](Webページとは)

@snap[slide-contents]
@snap[quote-wrap]

@quote[<ul><li>ウェブ上にあり、ウェブブラウザで閲覧可能なページ単位の文書</li><li>**HTML**（またはXHTML）と **スタイルシート**、画像データで構成</li><li>ウェブブラウザを使用して閲覧されることが一般的</li><li>**JavaScript** などのスクリプト言語を使って<br>ウェブページに動作をもたる場合がある</li></ul>](https://ja.wikipedia.org/wiki/ウェブページ)

@snapend
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [1. 基礎知識](#/0)
- [3. HTMLとは]()
@olend
@snapend

### @css[slide-title](HTMLとは)

@snap[slide-contents]
@snap[quote-wrap]

@quote[**H**yper **T**ext **M**arkup **L**anguage（ハイパーテキスト マークアップ ランゲージ、HTML（エイチティーエムエル））](https://ja.wikipedia.org/wiki/HyperText_Markup_Language)

@quote[**ハイパーテキスト**：<br>複数の文書（テキスト）を相互に関連付け、結び付ける仕組み](https://ja.wikipedia.org/wiki/ハイパーテキスト)


@quote[**マークアップ言語**：<br>視覚表現や文章構造などを記述するための形式言語](https://ja.wikipedia.org/wiki/マークアップ言語)

@snapend
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [1. 基礎知識](#/0)
- [4. HTMLの書き方]()
@olend
@snapend

### @css[slide-title](HTMLの書き方)

@snap[slide-contents]
@snap[code-contents]

```
<html>
    <head>
        （文書のタイトルや、CSSやJavaScriptへのリンク、）
        （メタデータ（データの説明データ）などを記述します。）
        （Webブラウザーには表示されません。）   
    </head>
    <body>
        （文章や画像などを記述します。）
    </body>
</html>
```
@[0](「&lt;html&gt;」「&lt;head&gt;」などを タグ と呼びます。)
@[0](タグを利用して文書の構造や意味などを記述（マークアップ）していきます。)
@[0](&lt;body&gt;内容&lt;/body&gt; のように、タグで囲んで内容を記述をしていきます。)

@snapend
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [1. 基礎知識](#/0)
- [5. CSSとは]()
@olend
@snapend

### @css[slide-title](CSSとは)

@snap[slide-contents]
@snap[quote-wrap]

@quote[<ul><li>**C**ascading **S**tyle **S**heets（CSS、<br>カスケーディング・スタイル・シート）</li><li>HTMLの要素をどのように修飾（表示）するかを指示する</li><li>文書の構造と体裁を分離させる<br>という理念を実現する為に提唱された**スタイルシート**の一つ</li></ul>](https://ja.wikipedia.org/wiki/Cascading_Style_Sheets)

@quote[**スタイルシート**：<br>構造化文書などにおける表示形式を制御するしくみ](https://ja.wikipedia.org/wiki/スタイルシート)

@snapend
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [1. 基礎知識](#/0)
- [6. CSSの書き方]()
@olend
@snapend

### @css[slide-title](CSSの書き方)

@snap[slide-contents]
@snap[code-contents]

```
div {
    width: 300px;
    height: 500px;
    color: red;
}
```

@[0](（適応する対象を指定します）{<br><span></span>（スタイルの種類を選びます）:（値を設定します）;<br>})

@snapend
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [1. 基礎知識](#/0)
- [7. JavaScriptとは]()
@olend
@snapend

### @css[slide-title](JavaScriptとは)

@snap[slide-contents]
@snap[quote-wrap]

@quote[<ul><li>JavaScript（ジャバスクリプト）</li><li>主にWebページに組み込まれたプログラムを<br>Webブラウザ上で実行するために用いられる**プログラミング言語**</li><li>HTMLファイル内に埋め込まれて記述</li></ul>](https://ja.wikipedia.org/wiki/JavaScript)

@snapend
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [1. 基礎知識](#/0)
- [8. JavaScriptの書き方]()
@olend
@snapend

### @css[slide-title](JavaScriptの書き方)

@snap[slide-contents]
@snap[code-contents]


```
var myHeading = document.querySelector('h1');
```

@[0](「h1」という要素を「myHeading」という名前で操作できるようにします。)

```
myHeading.textContent = "Hello World";
```

@[0](「myHeading」のテキスト内容（textContent）を「Hello World」に設定します。)
@[0](この結果、Webページのh1タグが「Hello World」という言葉になって表示されます。)
@snapend
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [1. 基礎知識](#/0)
- [9. Webの仕組み]()
@olend
@snapend

### @css[slide-title](Webの仕組み)

@snap[slide-contents]
@snap[quote-wrap]

@quote[<ul><li>ウェブページのコピーが<br>**サーバー** から **クライアント** にダウンロードされ、<br>ユーザーのウェブブラウザーに表示されます</li><li>**サーバー**：<br>ウェブページ、サイト、アプリを保存しているコンピューター</li><li>**クライアント**：<br>インターネットに接続された<br>コンピューターやスマートフォンなどのデバイス</li></ul>](https://developer.mozilla.org/ja/docs/Learn/Getting_started_with_the_web/How_the_Web_works)

@snapend
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [1. 基礎知識](#/0)
- [10. Elixirとは]()
@olend
@snapend

### @css[slide-title](Elixirとは)

@snap[slide-contents]
@snap[quote-wrap]

@quote[<ul><li>Elixir（エリクサー）</li><li>プログラミング言語</li><li>高い基本性能、書きやすい高生産性</li><li>１つのマシン内で数十万のプロセスが同時に動作</li><li>コードを短く/速く/メンテナンスしやすくするスタイル</li><li>開発用ツールセットが用意されています<ul><li>ビルドツール「 **mix（ミックス）**」</li></ul></li><li>Web<a href="#/">**フレームワーク**</a>「 **Phoenix（フェニックス）**」が人気</li></ul>](https://www.ossnews.jp/oss_info/Elixir)

@snapend
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [1. 基礎知識](#/0)
- [11. フレームワークとは]()
@olend
@snapend

### @css[slide-title](フレームワークとは)

@snap[slide-contents]
@snap[quote-wrap]

@quote[<ul><li>汎用的な機能や基本的な制御構造をまとめた**半完成品**</li><li>開発者がコードを記述して機能を追加、拡張する</li></ul>](http://e-words.jp/w/フレームワーク.html)

@snapend
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [1. 基礎知識](#/0)
- [12. 型とは]()
@olend
@snapend

### @css[slide-title](型とは)

@snap[slide-contents]
@snap[quote-wrap]

@quote[<ul><li>データ（値）の種類に関する分類<ul><li>0, 1, 2, -42 といったような値は整数型</li><li>"foo", "Hello" といったような値は文字列型</li></ul></li></ul>](https://ja.m.wikipedia.org/wiki/データ型)

@snapend
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [1. 基礎知識](#/0)
- [13. Elixirの主な型]()
@olend
@snapend

### @css[slide-title](Elixirの主な型)

@snap[slide-contents]

@snap[left-column]
<table>
<thead>
<tr>
	<th>型</th>
	<th>表記例</th>
</tr>
</thead>
<tbody>
<tr>
	<th>整数</th>
	<td>1</td>
</tr>
<tr>
	<th>整数(16進数)</th>
	<td>0x1F</td>
</tr>
<tr>
	<th>小数</th>
	<td>1.0</td>
</tr>
<tr>
	<th>論理値</th>
	<td>true</td>
</tr>
<tr>
	<th><u>[アトム](https://elixirschool.com/ja/lessons/basics/basics/#アトム)</u></th>
	<td>:atom</td>
</tr>
</tbody>
</table>
@snapend

@snap[right-column]
<table>
<thead>
<tr>
	<th>型</th>
	<th>表記例</th>
</tr>
</thead>
<tbody>
<tr>
	<th>文字列</th>
	<td>"elixir"</td>
</tr>
<tr>
	<th><u>[リスト](https://elixirschool.com/ja/lessons/basics/collections/#リスト)</u></th>
	<td>[1, 2, 3]</td>
</tr>
<tr>
	<th><u>[タプル](https://elixirschool.com/ja/lessons/basics/collections/#タプル)</u></th>
	<td>{1, 2, 3}</td>
</tr>
<tr>
	<th><u>[キーワードリスト](https://elixirschool.com/ja/lessons/basics/collections/#キーワードリスト)</u></th>
	<td>@size[0.85em](&#91;foo: "hello", bar: "world"&#93;)</td>
</tr>
<tr>
	<th><u>[マップ](https://elixirschool.com/ja/lessons/basics/collections/#マップ)</u></th>
	<td>%{key = "value"}</td>
</tr></tbody>
</table>
@snapend

@snapend


