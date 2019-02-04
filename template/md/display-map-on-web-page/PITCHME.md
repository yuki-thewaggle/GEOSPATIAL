---?color=#3A8FB7
@snap[breadcrumbs-wrap bluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [10. 地図のWebページ表示](#/)
@olend
@snapend

@snap[west headline]
## 地図の<br>Webページ表示
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [10. 地図のWebページ表示](#/)
@olend
@snapend

### @css[slide-title](地図のWebページ表示)

@snap[slide-contents]

@box[rounded box-style](Phoenix を使ってWebプロジェクトを作成します。)

@snap[left-column]
@ol[numberlist numberlist-color2](false)
- [leaflet.js とは](#/)
- [モジュールとは](#/)
- [leaflet.js の導入方法](#/)
- [HTMLファイルのオープン](#/)
- [leaflet.js での実装（プロ<br>グラム）](#/)
- [leaflet.js での実装（表示）](#/)
- [プログラム部分の解説](#/)
@olend
@snapend

@snap[right-column]
@img[goal-image to-center](template/img/environment/CUI-windows.png)
@snapend

@snapend

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [10. 地図のWebページ表示](#/)
- [1. leaflet.js とは](#/)
@olend
@snapend

@snap[west headline]
## @color[white](leaflet.js とは)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [10. 地図のWebページ表示](#/)
- [1. leaflet.js とは](#/)
@olend
@snapend

### @css[slide-title](leaflet.js とは)

@snap[slide-contents]

@box[rounded box-style](<u>[leaflet.js](https://leafletjs.com/)</u> は、<u>[JavaScript](https://ja.wikipedia.org/wiki/JavaScript)</u>のマップ用**モジュール**です。)


@snap[left-column]
@ul[itemlist](false)
- <u>[インタラクティブ](http://e-words.jp/w/インタラクティブ.html)</u>なマップ
- モバイル対応
- 軽量
- ほとんどのマッピング機能
@ulend
@snapend

@snap[right-column]
@img[goal-image to-center](template/img/environment/postgresql.png)

@snapend

@snapend


---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [10. 地図のWebページ表示](#/)
- [2. モジュールとは](#/)
@olend
@snapend

@snap[west headline]
## @color[white](モジュールとは)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [10. 地図のWebページ表示](#/)
- [2. モジュールとは](#/)
@olend
@snapend

### @css[slide-title](モジュールとは)

@snap[slide-contents]
@snap[quote-wrap]

@quote[<ul><li>機能単位、**交換可能な構成部分**という意味の英単語</li><li>システムの一部を構成する**ひとまとまりの機能を持った部品**</li><li>規格化・標準化されていて、容易に追加や交換ができる</li></ul>]((http://e-words.jp/w/モジュール.html)

@snapend
@snapend

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [10. 地図のWebページ表示](#/)
- [3. leaflet.js の導入方法](#/)
@olend
@snapend

@snap[west headline]
## @color[white](leaflet.js の<br>導入方法)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [10. 地図のWebページ表示](#/)
- [3. leaflet.js の導入方法](#/)
@olend
@snapend

### @css[slide-title](leaflet.js の導入方法)

@snap[slide-contents]

@box[rounded box-style](**Visual Studio Code** を使って、leaflet.jsを導入します。<br>今回は<u>[CDN](http://e-words.jp/w/CDN.html)</u>を利用します。)

@snap[fragment]
@ol[]
- <u>[こちら](https://leafletjs.com/download.html#using-a-hosted-version-of-leaflet)</u> に記載されている、以下のコードを右クリックしてコピーします。
@snapend

```html
<link rel="stylesheet" href="https://unpkg.com/leaflet@1.4.0/dist/leaflet.css" />
<script src="https://unpkg.com/leaflet@1.4.0/dist/leaflet.js"></script>
```

@snapend

@snapend

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [10. 地図のWebページ表示](#/)
- [4. HTMLファイルのオープン](#/)
@olend
@snapend

@snap[west headline]
## @color[white](HTMLファイルの<br>オープン)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [10. 地図のWebページ表示](#/)
- [4. HTMLファイルのオープン](#/)
@olend
@snapend

### @css[slide-title](HTMLファイルのオープン)

@snap[slide-contents]

@box[rounded box-style]( **CUI** を使って、<br>Visual Studio Code で HTMLファイルを開きます。)

@ol[numberlist numberlist-color4](true)
- 以下のコマンドを貼り付けます。
- code -r lib/aedmap_web/templates/page/index.html.eex
@olend

@snapend

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [10. 地図のWebページ表示](#/)
- [4. leaflet.js での実装（プログラム）](#/)
@olend
@snapend

@snap[west headline]
## @color[white](leaflet.js での<br>実装（プログラム）)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [10. 地図のWebページ表示](#/)
- [4. leaflet.js での実装（プログラム）](#/)
@olend
@snapend

### @css[slide-title smaller-font](leaflet.js での実装（プログラム）)

@snap[slide-contents]

@box[rounded box-style](作業の内容と目的)

@snap[left-column]
@ol[numberlist numberlist-color4](false)
- mix phx.new aedmap
- Y
@olend
@snapend

@snap[right-column]
@snap[gist-box half-gist-box]

@gist[zoom-09](yuki-thewaggle/82bf9f1de5b6963bcb47f02e7b1c5d09)

@[1](説明)
@[2](説明)

@snapend
@snapend

@snapend



---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [10. 地図のWebページ表示](#/)
- [5. leaflet.js での実装（表示）](#/)
@olend
@snapend

@snap[west headline]
## @color[white](leaflet.js での<br>実装（表示）)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [10. 地図のWebページ表示](#/)
- [5. leaflet.js での実装（表示）](#/)
@olend
@snapend

### @css[slide-title smaller-font](leaflet.js での実装（表示）)

@snap[slide-contents]

@box[rounded box-style](作業の内容と目的)

@snap[left-column]
@ol[numberlist numberlist-color4](false)
- mix phx.new aedmap
- Y
@olend
@snapend

@snap[right-column]
@snap[gist-box half-gist-box]

@gist[zoom-09](yuki-thewaggle/82bf9f1de5b6963bcb47f02e7b1c5d09)

@[1](説明)
@[2](説明)

@snapend
@snapend

@snapend



---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [10. 地図のWebページ表示](#/)
- [6. プログラム部分の解説](#/)
@olend
@snapend

@snap[west headline]
## @color[white](プログラム部分の<br>解説)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [10. 地図のWebページ表示](#/)
- [6. プログラム部分の解説](#/)
@olend
@snapend

### @css[slide-title](プログラム部分の解説)

@snap[slide-contents]
@snap[gist-box]

@fa[external-link]
<u>https://gist.github.com/yuki-thewaggle/82bf9f1de5b6963bcb47f02e7b1c5d09</u>

@gist[zoom-09](yuki-thewaggle/82bf9f1de5b6963bcb47f02e7b1c5d09)

@[1](1)
@[2,4](2,4)
@[6-8](6-8)
@[17-19](17-19)
@[32](32)

@snapend
@snapend
