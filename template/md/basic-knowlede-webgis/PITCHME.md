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

@quote[<ul><li>World Wide Web（ワールド・ワイド・ウェブ、略名：WWW）は、Web（ウェブ）とも呼ばれる</li><li>「インターネット」という表現がワールド・ワイド・ウェブを指す場合もある</li><li>世界中に張り巡らしたような、文書間のつながり</li><li>HTMLやXHTMLといったハイパーテキストの記述言語が使用される</li></ul>](https://ja.wikipedia.org/wiki/World_Wide_Web)

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

@quote[ウェブ上にあり、ウェブブラウザで閲覧可能な、ページ単位の文書](https://ja.wikipedia.org/wiki/%E3%82%A6%E3%82%A7%E3%83%96%E3%83%9A%E3%83%BC%E3%82%B8)

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/1)
- [1. 基礎知識](#/12)
- [2. Webの仕組み]()
@olend
@snapend

### @css[slide-title](Webの仕組み)

@snap[slide-contents]

@snap[quote-wrap]

@quote[<ul><li>Webにおける情報の基礎的な単位はページ（Webページ、ウェブページ）](http://e-words.jp/w/Web.html)

@quote[<ul><li>ウェブページのコピーが<strong>サーバー</strong>から<strong>クライアント</strong>にダウンロードされ、ユーザーのウェブブラウザーに表示されます。<ul><li>クライアント：<br>インターネットに接続されたコンピューターやスマートフォンなど</li><li>サーバー：<br>ウェブページ、サイト、アプリを保存しているコンピューター</li></ul></li></ul>](https://developer.mozilla.org/ja/docs/Learn/Getting_started_with_the_web/How_the_Web_works)

@snapend

---?color=#9F79F7
# @css[headline](Webの)
# @css[headline](基礎知識)
# @css[headline](ちょっとだけ)

---
@snap[midopoint north-west text-06]
### 本日のゴールイメージ
@snapend

@img[span-60](template/img/finish.png)

---
@snap[midopoint north-west text-06]
### Webの仕組み
@snapend

ブラウザに表示するのに使う技術は３種類

* 文章の構造を定義する　HTML
* レイアウト等、装飾するのが　CSS
* 機能をつけるのが JavaScript
---
@snap[midopoint north-west text-06]
### HTML
@snapend

```html
<html>
    <head>属性情報などを記述する</head>
    <body>ブラウザに表示される</body>
</html>
```
---
@snap[midopoint north-west text-06]
### CSS
@snapend

```css
div {
    Width: 300px;
    height: 500px;
    color: red;
}
```
---
@snap[midopoint north-west text-06]
### JavaScript
@snapend

```js

var myHeading = document.querySelector('h1');
myHeading.textContent = "Hello World";  

```
---
@snap[midopoint north-west text-06]
### Elixirの型
@snapend

* 基本的な型	値の例
* 整数	1
* 整数(16進数)	0x1F
* 小数	1.0
* 論理値	true
* アトム	:atom
* 文字列	"elixir"
* リスト	[1, 2, 3]
* タプル	{1, 2, 3}