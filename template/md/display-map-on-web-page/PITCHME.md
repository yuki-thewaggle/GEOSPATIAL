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

@box[rounded box-style](leaflet.js を使って地図を作成します。)

@snap[left-column]
@ol[numberlist numberlist-color2](false)
- [leaflet.js とは](#/)
- [モジュールとは](#/)
- [leaflet.js の導入方法](#/)
- [CDNでの追加](#/)
- [サンプルの追加](#/)
- [プログラムの追加](#/)
@olend
@snapend

@snap[right-column]
@ol[numberlist numberlist-color2 start-7](false)
- [スタイルの追加](#/)
- [プログラム部分の解説](#/)
- [国土地理院のタイルの利用例](#/)
@olend
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

@ol[numberlist numberlist-color4](true)
- <u>[こちら](https://leafletjs.com/download.html#using-a-hosted-version-of-leaflet)</u> に記載されている、以下のコード二行を右クリックしてコピーします。
- ```<link rel="stylesheet" href="https://unpkg.com/leaflet@1.4.0/dist/leaflet.css" />```
- ```<script src="https://unpkg.com/leaflet@1.4.0/dist/leaflet.js"></script>```

@olend

@snapend

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [10. 地図のWebページ表示](#/)
- [4. CDNでの追加](#/)
@olend
@snapend

@snap[west headline]
## @color[white](CDNでの追加)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [10. 地図のWebページ表示](#/)
- [4. CDNでの追加](#/)
@olend
@snapend

### @css[slide-title](CDNでの追加)

@snap[slide-contents]

@box[rounded box-style](**Visual Studio Code** を使って、**app.html.eex**に、先ほどコピーしたCDNを追加します。)

@ol[numberlist numberlist-color4](true)
- VScodeのサイドバーにあるEXPLORERより、```lib/aedmap_web/templates/layout/app.html.eex```を開きます。
- ```<head>``` タグと ```</head>```の終了タグの間（どこでも可）に先ほどコピーしたタグをペーストします。
@olend

@snapend

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [10. 地図のWebページ表示](#/)
- [5. サンプルの追加](#/)
@olend
@snapend

@snap[west headline]
## @color[white](サンプルの追加)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [10. 地図のWebページ表示](#/)
- [5. サンプルの追加](#/)
@olend
@snapend

### @css[slide-title smaller-font](サンプルの追加)

@snap[slide-contents]

@box[rounded box-style](**ブラウザ**を使います。先ほど開いてある```leafletjs.com```のサイトのOverviewにあるサンプルコードを利用します。)

@ol[numberlist numberlist-color4](false)
- ```https://leafletjs.com/```の[Overview](https://leafletjs.com/index.html)にあるスクリプトをコピーします。
@olend

@snap[gist-box]

@gist[js zoom-06](Yoosuke/48b765d1ddb12d08831f0748c9e6cdb9)

@snapend

@snapend

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [10. 地図のWebページ表示](#/)
- [6. プログラムの追加](#/)
@olend
@snapend

@snap[west headline]
## @color[white](プログラムの追加)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [10. 地図のWebページ表示](#/)
- [6. プログラムの追加](#/)
@olend
@snapend

### @css[slide-title smaller-font](プログラムの追加)

@snap[slide-contents]

@box[rounded box-style]( **Visual Studio Code** を使って、**index.html.eex**ファイルにプログラムを加えます。)

@ol[numberlist numberlist-color4](false)
- ``` lib/aedmap_web/templates/page/index.html.eex ```を開きます。

- ページに先ほどコピーしたスクリプトをペーストします。
- 追加したコードは、JavaScriptなので、```<script>先ほどコピーしたスクリプト</script>```で囲みます。
- ```<div id="map"></div>``` タグを先ほどの```<script>```タグより上に追記します。
@olend


@snapend

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [10. 地図のWebページ表示](#/)
- [7. スタイルの追加](#/)
@olend
@snapend

@snap[west headline]
## @color[white](スタイルの追加)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [10. 地図のWebページ表示](#/)
- [7. スタイルの追加](#/)
@olend
@snapend

### @css[slide-title smaller-font](スタイルの追加)

@snap[slide-contents]

@box[rounded box-style]( **Visual Studio Code** を使って、**app.html.eex**ファイルにスタイルを加えます。)

@ol[numberlist numberlist-color4](false)
- ``` lib/aedmap_web/templates/layout/app.html.eex ```を開きます。

- ```</head>```の終了タグの上に、以下のタグを追記します。
@olend

@snap[gist-box]
    @gist[css zoom-06](Yoosuke/a2917fdd1b7279a40b0a63351a84195c)
@snapend

@snapend

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [10. 地図のWebページ表示](#/)
- [7. プログラム部分の解説](#/)
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
- [7. プログラム部分の解説](#/)
@olend
@snapend

### @css[slide-title](プログラム部分の解説)

@snap[slide-contents]
@snap[gist-box]

@fa[external-link]
<u>https://gist.github.com/Yoosuke/48b765d1ddb12d08831f0748c9e6cdb9</u>

@gist[zoom-09](Yoosuke/f91e402b4a465a91a7637c79209fa976)

@[1](変数mapに地図の初期表示の緯度経度、地図の縮尺を設定しています。)
@[3](地図タイルのリンクを変更する事で、色々な種類の地図を利用できます。)
@[4](利用した地図タイルの提供元の名前とライセンスについてのURLを設定します。)
@[7-9](地図にマーカーをつける場合に、緯度経度とポップアップに入れる内容を設定します。)

@snapend
@snapend

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [10. 地図のWebページ表示](#/)
- [8. 国土地理院の地図タイル利用例](#/)
@olend
@snapend

@snap[west headline]
## @color[white](国土地理院の <br> 地図タイル利用例)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [10. 地図のWebページ表示](#/)
- [8. 国土地理院の地図タイル利用例](#/)
@olend
@snapend

### @css[slide-title](国土地理院の地図タイル利用例)

@snap[slide-contents]
@snap[gist-box]

@fa[external-link]
<u>https://gist.github.com/Yoosuke/34b74c792a0bf40f1875f22da9bc2b46</u>

@gist[js zoom-09](Yoosuke/34b74c792a0bf40f1875f22da9bc2b46)

@[1](東京タワーの緯度経度に変更しています。)
@[3](```https://maps.gsi.go.jp/development/ichiran.html#std```より、写真のタイルを利用します。)
@[4](国土地理院の名前とリンク先を追加します。)
@[7-9](東京タワーと緯度経度を追加しています。)

@snapend
@snapend