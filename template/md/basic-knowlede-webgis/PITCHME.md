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