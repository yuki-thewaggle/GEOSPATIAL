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

@box[rounded box-style](<u>[leaflet.js](https://leafletjs.com/)</u> は、<u>[JavaScript](https://ja.wikipedia.org/wiki/JavaScript)</u>のマップ用<u>[ライブラリ](https://ja.wikipedia.org/wiki/ライブラリ)</u>です。 )


@snap[left-column]
@ul[itemlist](false)
- [インタラクティブ](http://e-words.jp/w/インタラクティブ.html)なマップ
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

@box[rounded box-style](作業の内容と目的,使用するソフトウェア)

@snap[left-column]
@ul[itemlist](false)
- 条件１
- 条件１
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

@box[rounded box-style](Firefoxは、高速かつ軽量なWebブラウザーです。<br>拡張機能が豊富であるという特徴があります。)

@ol[numberlist numberlist-color4](true)
- <u>[Firefoxのダウンロードページ](https://www.mozilla.org/ja/firefox/new/)</u>にアクセスします。
- 「今すぐダウンロード」ボタンをクリックします。
- ダウンロードしたファイルをクリックして起動します。
- Windows
- Mac
- インストールされます。
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
