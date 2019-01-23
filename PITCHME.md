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

@snap[slide-contents]

@ol[numberlist](false)
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

---?color=#3A8FB7
@snap[breadcrumbs-wrap bluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](5)
- [n. アジェンダ項目名]()
@olend
@snapend

# @css[slide-title specified-font](テンプレートA - 大項目)

@snap[slide-contents]

@box[rounded box-style-blue](アジェンダ項目（大項目）用の、テンプレートです。<br>項目の概要を、説明します。)

@ol[numberlist](false)
- アジェンダ項目内の小項目
- 小項目
- 小項目
- 小項目
- 体言止め
- a
- a
@olend

@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](5)
- [n. アジェンダ項目名]()
- [m. 小項目名]()
- [k. ここまで]()
@olend
@snapend

# @css[slide-title blue specified-font](テンプレートB - 言葉・概念の意味)

@snap[slide-contents]

@snap[quote-wrap]
@quote[<ul><li>ユーザインタフェース<ul><li>ユーザインタフェース1</li><li>ユーザインタフェース2</li></ul></li><li>文字列が表示されるウィンドウに出力</li><li>キーボード等から文字列を入力</li></ul>](https://ja.m.wikipedia.org/wiki/キャラクタユーザインタフェース)
@quote[キーボード等から文字列を入力](https://ja.m.wikipedia.org/wiki/キャラクタユーザインタフェース)
@snapend

@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](5)
- [n. アジェンダ項目名]()
- [m. 小項目名]()
- [k. ここまで]()
@olend
@snapend

# @css[slide-title blue specified-font](テンプレートC - Bのテーブル版)

@snap[slide-contents]

<table>
<tr>
	<th width="30%"/*適宜変更*/>型</th>
	<th>表記例</td>
</tr>
<tr>
	<td>整数</th>
	<td>1</td>
</tr><tr>
	<td>整数(16進数)</th>
	<td>0x1F</td>
</tr>
<tr>
	<td>小数</th>
	<td>1.0</td>
</tr>
<tr>
	<td>論理値</th>
	<td>true</td>
</tr>
<tr>
	<td>アトム</th>
	<td>:atom</td>
</tr>
<tr>
	<td>文字列</th>
	<td>"elixir"</td>
</tr>
<tr>
	<td>リスト</th>
	<td>[1, 2, 3]</td>
</tr>
<tr>
	<td>タプル</th>
	<td>{1, 2, 3}</td>
</tr>
</table>

@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](5)
- [n. アジェンダ項目名]()
- [m. 小項目名]()
- [k. ここまで]()
@olend
@snapend

# @css[slide-title blue specified-font](テンプレートD - 作業手順)

@snap[slide-contents]

@ol[numberlist](false)
- Web基礎知識
- 環境構築
- APIServerの構築
- 地図の表示
- 外部API呼び出し
- DB操作
- 内部API呼び出し
- 地図へのポイント追加
- 自分の緯度経度の取得
- 自分の緯度経度の取得
- 自分の緯度経度の取得
@olend

@snapend


---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](5)
- [n. アジェンダ項目名]()
- [m. 小項目名]()
- [k. ここまで]()
@olend
@snapend

# @css[slide-title blue specified-font](テンプレートE - 手順詳細)

@snap[slide-contents]

@box[rounded box-style](手順詳細用の、テンプレートです。<br>この作業の目的を、ここに書きます。)

@snap[left-column]
@ol[numberlist](true)
- 手順１や、
- 手順２など、
- ここに、書いていきます。
- 書いていきます<br>書いていきます書いていきます。
- a
@olend
@snapend

@snap[right-column]
@ol[numberlist start-6](true)
- 手順5なら `start-6` と書き、
- 書いていきます。
- 書いていきます。
- 書いていきます。
- a
- a
@olend
@snapend

@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](5)
- [n. アジェンダ項目名]()
- [m. 小項目名]()
- [k. ここまで]()
@olend
@snapend

# @css[slide-title blue specified-font](テンプレートF - 手順ゴール)

@snap[slide-contents]

@img[goal-image](template/img/environment/postgresql.png)

@snapend
---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](5)
- [n. アジェンダ項目名]()
- [m. 小項目名]()
- [k. ここまで]()
@olend
@snapend

# @css[slide-title blue specified-font](テンプレートG - ソースコード)

@snap[slide-contents]
@snap[gist-box]

@fa[external-link]
<u>https://gist.github.com/Yoosuke/4b171606c9390418467b961085894915</u>

@gist[html zoom-07](Yoosuke/4b171606c9390418467b961085894915)

@[1](sample1)
@[2,4](sample2)
@[6-8](sample3)
@[21](sample6)

@snapend
@snapend

---?color=#3A8FB7
@snap[breadcrumbs-wrap bluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](5)
- [2. 環境構築]()
- 
@olend
@snapend

# @css[slide-title specified-font](（例）環境構築)

@snap[west slide-contents]

@box[rounded box-style](今回の開発に必要なシステムやソフトウェアを、<br>自分のPCで使えるように準備します。)

@ol[numberlist](false)
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
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](5)
- [1. Web基礎知識]()
- [3. テキストエディタ]()
- [1. 概要]()
@olend
@snapend

# @css[slide-title blue specified-font](（例）Firefoxのダウンロード)

@snap[south-east]
@img[span-60 height-50 margin-right-0](template/img/environment/postgresql.png)
@snapend

@snap[west slide-contents]

<u>[Firefox](https://www.mozilla.org/ja/firefox/new/)</u>を<br>
ダウンロードします。

@snapend

---
@css[page-number lightblue](（レイアウト変更します）ハンズオン講習会の流れ[2] ＞ 環境構築[1] Firefox)
# @css[slide-title blue specified-font](（例）ソースコード)

@gist[html zoom-05](Yoosuke/4b171606c9390418467b961085894915)

@[1](sample1)
@[2,4](sample2)
@[6-8](sample3)

---
@css[page-number lightblue](（レイアウト変更します）ハンズオン講習会の流れ[2] ＞ 環境構築[1] Firefox)
# @css[slide-title blue specified-font](（例）Webページを埋め込む)

<iframe class="iframe-style" src="http://nipponcolors.com/#chigusa"></iframe>

---
@css[page-number lightblue](（レイアウト変更します）ハンズオン講習会の流れ[2] ＞ 環境構築[1] Firefox)
# @css[slide-title specified-font](（例）Webの仕組み)

@snap[west slide-contents]

> https://developer.mozilla.org/ja/docs/Learn/Common_questions/Pages_sites_servers_and_search_engines
> https://developer.mozilla.org/ja/docs/Learn/Getting_started_with_the_web/How_the_Web_works
	
* クライアント
	Webブラウザ
* サーバ
* リクエストとレスポンス
* インターネット接続
* ウェブページ
	ウェブブラウザに表示可能なドキュメント

@snapend

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
@ol[numberlist](true)
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
