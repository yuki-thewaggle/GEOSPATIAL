<nav>
@ol[roman breadcrumb](false)
- Home
- Category
- Sub Category
- Sub Category
- Contents
@olend
</nav>

---?color=#3A8FB7

@snap[west]
# @css[headline top-left specified-font](GEOSPATIAL<br>Hackers Program<br>Hands-on)
@snapend

---?color=#3A8FB7

@snap[west]
# @css[sub-headline specified-font](オープンデータを<br>利用して<br>地図アプリを作ろう!)
@snapend

---
# @css[slide-title blue specified-font](ハンズオン講習会の流れ)

@css[space-0]()

@ul[roman](false)
- Web基礎知識
- 環境構築
- APIServerの構築
- 地図の表示
- 外部API呼び出し
- DB操作
- 内部API呼び出し
- 地図へのポイント追加
- 自分の緯度経度の取得
@ulend

---?color=#3A8FB7
@css[page-number blue]([2] 環境構築)
# @css[slide-title specified-font](（例）環境構築)

@snap[west slide-contents]

@box[rounded box-style](今回の開発に必要なシステムやソフトウェアを、<br>自分のPCで使えるように準備します。)

@ol[roman](false)
- Firefox
- RestClient
- テキストエディタ
- Elixir
- node.js
- PostgreSQL
- Phoenixframework
@olend

@snapend

---

# @css[slide-title blue specified-font](（例）Firefoxのダウンロード)

@snap[south-east]
@img[span-60 height-50 margin-right-0](template/img/environment/postgresql.png)
@snapend

@snap[west slide-contents]

<u>[Firefox](https://www.mozilla.org/ja/firefox/new/)</u>を<br>
ダウンロードします。

@snapend

---
@css[page-number lightblue](ハンズオン講習会の流れ[2] ＞ 環境構築[1] Firefox)
# @css[slide-title blue specified-font](（例）ソースコード)

@css[space-0]()

@gist[html zoom-05](Yoosuke/4b171606c9390418467b961085894915)

@[1](sample1)
@[2,4](sample2)
@[6-8](sample3)

---
@css[page-number lightblue](ハンズオン講習会の流れ[2] ＞ 環境構築[1] Firefox)
# @css[slide-title blue specified-font](（例）Webページを埋め込む)

<iframe class="iframe-style" src="http://nipponcolors.com/#chigusa"></iframe>

---
1. Webの仕組み
2. HTML
3. CSS
4. JavaScript
5. Elixir
6. 型
7. Elixirの型
---

---?color=#3a8fb7

@snap[north-west]
## The Agenda
@snapend

@snap[south-west list-content-concise span-80]
@ol[list-bullets-black](true)
- Web基礎知識
- 環境構築
- APIServerの構築
- 地図の表示
- 外部API呼び出し
- DB操作
- 内部API呼び出し
- 地図へのポイント追加
- 自分の緯度経度の取得
@olend
@snapend

---?include=template/md/basic-knowlede-webgis/PITCHME.md
---?include=template/md/environment/PITCHME.md
---?include=template/md/Building-APIServer/PITCHME.md
---?include=template/md/Show-map/PITCHME.md
---?include=template/md/External-API-call/PITCHME.md
---?include=template/md/DB-operation/PITCHME.md
---?include=template/md/Internal-API-call/PITCHME.md
---?include=template/md/points-to-the-map/PITCHME.md
---?include=template/md/own-latitude-longitude/PITCHME.md

---
利用サービス
* [leafletjs](https://leafletjs.com)
* [国土地理院](https://maps.gsi.go.jp)
* [TURF](http://turfjs.org/getting-started/)
* [Firefox「RESTClient」](https://addons.mozilla.org/ja/firefox/addon/restclient/)

---
利用技術の紹介
* [Elixir](https://elixir-lang.org/)
* [Phoenix](https://phoenixframework.org/)
* [PostgreSQL](https://www.postgresql.org/)
* [Vue.js](https://jp.vuejs.org/index.html)

---
オープンデータ

---
参考情報
* [OpenStreetMap](https://openstreetmap.jp)
* [CART](https://carto.com/)
* [SPARQL](https://www.slideshare.net/uedayou/web-apisparql)
* [QGIS](https://www.qgis.org/)
* [地図tile](https://wiki.openstreetmap.org/wiki/JA:%E3%82%BF%E3%82%A4%E3%83%AB)

---?survey=https://docs.google.com/forms/d/e/1FAIpQLSdabsWuQXStcoocJffMSv535a6KyZ_1VL6PSNISr4nuaPYdDQ/viewform?vc=0&c=0&w=1&usp=mail_form_link&color=#B481BB
