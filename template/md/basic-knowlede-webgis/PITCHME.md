---?color=#3A8FB7
@snap[breadcrumbs-wrap bluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/1)
- [1. 基礎知識](#/12)
@olend
@snapend

@snap[west headline]
## 基礎知識
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/1)
- [1. 基礎知識](#/12)
- [1. Web（World Wide Web）とは]()
@olend
@snapend

### @css[slide-title](Web（World Wide Web）とは)

@snap[slide-contents]
@snap[quote-wrap]

@quote[<ul><li>World Wide <span class="orange">Web</span>（WWW、ワールド・ワイド・ウェブ）</li><li>Web（ウェブ）とも呼ばれる</li><li>「<span class="orange">インターネット</span>」という表現が<br>ワールド・ワイド・ウェブを指す場合もある</li><li><span class="orange">世界中に張り巡らしたような、文書間のつながり</span></li></ul>](https://ja.wikipedia.org/wiki/World_Wide_Web)

@quote[Webにおける<span class="orange">情報の基礎的な単位</span>はページ<br>（<span class="orange">Webページ</span>、ウェブページ）](http://e-words.jp/w/Web.html)

@snapend
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/1)
- [1. 基礎知識](#/12)
- [2. Webページとは]()
@olend
@snapend

### @css[slide-title](Webページとは)

@snap[slide-contents]
@snap[quote-wrap]

@quote[<ul><li>ウェブ上にあり、ウェブブラウザで閲覧可能なページ単位の文書</li><li><span class="orange">HTML</span>（またはXHTML）と <span class="orange">スタイルシート</span>、画像データで構成</li><li>ウェブブラウザを使用して閲覧されることが一般的</li><li><span class="orange">JavaScript</span> などのスクリプト言語を使って<br>ウェブページに動作をもたる場合がある</li></ul>](https://ja.wikipedia.org/wiki/%E3%82%A6%E3%82%A7%E3%83%96%E3%83%9A%E3%83%BC%E3%82%B8)

@snapend

* 文章の構造を定義する　<a href="#/6">@css[orange](HTML)</a>
* レイアウトなど装飾するのが　<a href="#/">@css[orange](スタイルシート（CSS）)</a>
* 機能をつけるのが <a href="#/">@css[orange](JavaScript)</a>

@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/1)
- [1. 基礎知識](#/12)
- [3. HTMLとは]()
@olend
@snapend

### @css[slide-title](HTMLとは)

@snap[slide-contents]
@snap[quote-wrap]

@quote[<span class="orange">H</span>yper<span class="orange">T</span>ext <span class="orange">M</span>arkup <span class="orange">L</span>anguage（ハイパーテキスト マークアップ ランゲージ、HTML（エイチティーエムエル））](https://ja.wikipedia.org/wiki/HyperText_Markup_Language)

@quote[<span class="orange">ハイパーテキスト</span>：<br>複数の文書（テキスト）を相互に関連付け、結び付ける仕組み](https://ja.wikipedia.org/wiki/%E3%83%8F%E3%82%A4%E3%83%91%E3%83%BC%E3%83%86%E3%82%AD%E3%82%B9%E3%83%88)


@quote[<span class="orange">マークアップ言語</span>：<br>視覚表現や文章構造などを記述するための形式言語](https://ja.wikipedia.org/wiki/%E3%83%9E%E3%83%BC%E3%82%AF%E3%82%A2%E3%83%83%E3%83%97%E8%A8%80%E8%AA%9E)

@snapend
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/1)
- [1. 基礎知識](#/12)
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
@[0](タグで文書の構造や意味などを指定します。)
@[0](&lt;html&gt;指定したい部分&lt;/html&gt; のように囲みます。)

@snapend
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/1)
- [1. 基礎知識](#/12)
- [5. CSSとは]()
@olend
@snapend

### @css[slide-title](CSSとは)

@snap[slide-contents]
@snap[quote-wrap]

@quote[<ul><li><span class="orange">C</span>ascading <span class="orange">S</span>tyle <span class="orange">S</span>heets（CSS、<br>カスケーディング・スタイル・シート、<br>カスケード・スタイル・シート）</li><li>HTMLの要素をどのように修飾（表示）するかを指示する</li><li>文書の構造と体裁を分離させる<br>という理念を実現する為に提唱された<span class="orange">スタイルシート</span>の一つ</li></ul>](https://ja.wikipedia.org/wiki/Cascading_Style_Sheets)

@quote[<span class="orange">スタイルシート</span>：<br>構造化文書などにおける表示形式を制御するしくみ](https://ja.wikipedia.org/wiki/%E3%82%B9%E3%82%BF%E3%82%A4%E3%83%AB%E3%82%B7%E3%83%BC%E3%83%88)

@snapend
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/1)
- [1. 基礎知識](#/12)
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
- [ハンズオン講習会の流れ](#/1)
- [1. 基礎知識](#/12)
- [7. JavaScriptとは]()
@olend
@snapend

### @css[slide-title](JavaScriptとは)

@snap[slide-contents]
@snap[quote-wrap]

@quote[<ul><li>JavaScript（ジャバスクリプト）</li><li>主にWebページに組み込まれたプログラムを<br>Webブラウザ上で実行するために用いられる<span class="orange">プログラミング言語</span></li><li>HTMLファイル内に埋め込まれて記述</li></ul>](https://ja.wikipedia.org/wiki/JavaScript)

@snapend
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/1)
- [1. 基礎知識](#/12)
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
- [ハンズオン講習会の流れ](#/1)
- [1. 基礎知識](#/12)
- [9. Webの仕組み]()
@olend
@snapend

### @css[slide-title](Webの仕組み)

@snap[slide-contents]
@snap[quote-wrap]

@quote[<ul><li>ウェブページのコピーが<br><span class="orange">サーバー</span> から <span class="orange">クライアント</span> にダウンロードされ、<br>ユーザーのウェブブラウザーに表示されます</li><li><span class="orange">サーバー</span>：<br>ウェブページ、サイト、アプリを保存しているコンピューター</li><li><span class="orange">クライアント</span>：<br>インターネットに接続された<br>コンピューターやスマートフォンなどのデバイス</li></ul>](https://developer.mozilla.org/ja/docs/Learn/Getting_started_with_the_web/How_the_Web_works)

@snapend
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/1)
- [1. 基礎知識](#/12)
- [10. Elixirとは]()
@olend
@snapend

### @css[slide-title](Elixirとは)

@snap[slide-contents]
@snap[quote-wrap]

@quote[<ul><li>Elixir（エリクサー）</li><li>プログラミング言語</li><li>高い基本性能、書きやすい高生産性</li><li>１つのマシン内で数十万のプロセスが同時に動作</li><li>コードを短く/速く/メンテナンスしやすくするスタイル</li><li>開発用ツールセットが用意されています<ul><li>ビルドツール「 <span class="orange">mix（ミックス）<span>」</li></ul></li><li>Webフレームワーク「 <span class="orange">Phoenix（フェニックス）</span>」が人気</li></ul>](https://www.ossnews.jp/oss_info/Elixir)

@snapend
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/1)
- [1. 基礎知識](#/12)
- [11. Elixirの主な型]()
@olend
@snapend

### @css[slide-title](Elixirの主な型)

@snap[slide-contents]

@snap[left-column]
<table>
<tr>
	<th width="45%">型</th>
	<th>表記例</th>
</tr>
<tr>
	<td style="background-color:rgba(0,0,0,0.1);">整数</td>
	<td>1</td>
</tr>
<tr>
	<td style="background-color:rgba(0,0,0,0.1);">整数(16進数)</td>
	<td>0x1F</td>
</tr>
<tr>
	<td style="background-color:rgba(0,0,0,0.1);">小数</td>
	<td>1.0</td>
</tr>
<tr>
	<td style="background-color:rgba(0,0,0,0.1);">論理値</td>
	<td>true</td>
</tr>
</table>
@snapend

@snap[right-column]
<table>
<tr>
	<th width="45%">型</th>
	<th>表記例</th>
</tr>
<tr>
	<td style="background-color:rgba(0,0,0,0.1);"><u>[アトム](https://elixirschool.com/ja/lessons/basics/basics/#%E3%82%A2%E3%83%88%E3%83%A0)</u></td>
	<td>:atom</td>
</tr>
<tr>
	<td style="background-color:rgba(0,0,0,0.1);">文字列</td>
	<td>"elixir"</td>
</tr>
<tr>
	<td style="background-color:rgba(0,0,0,0.1);"><u>[リスト](https://elixirschool.com/ja/lessons/basics/collections/#%E3%83%AA%E3%82%B9%E3%83%88)</u></td>
	<td>[1, 2, 3]</td>
</tr>
<tr>
	<td style="background-color:rgba(0,0,0,0.1);"><u>[タプル](https://elixirschool.com/ja/lessons/basics/collections/#%E3%82%BF%E3%83%97%E3%83%AB)</u></td>
	<td>{1, 2, 3}</td>
</tr>
</table>
@snapend

@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/1)
- [1. 基礎知識](#/12)
- [12. 型とは]()
@olend
@snapend

### @css[slide-title](型とは)

@snap[slide-contents]
@snap[quote-wrap]

@quote[<ul><li>データ（値）の種類に関する分類<ul><li>0, 1, 2, -42 といったような値は整数型</li><li>"foo", "Hello" といったような値は文字列型</li></ul></li></ul>](https://ja.m.wikipedia.org/wiki/データ型)

@snapend
@snapend
