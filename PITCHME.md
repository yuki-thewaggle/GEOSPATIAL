---?color=#3A8FB7

@snap[west top-left]

@snap[byline headline-detail color4]
@size[0.75em](GEOSPATIAL Hackers Program Hands-on)
@snapend

@snap[headline]
# オープンデータを<br>利用して<br>地図アプリを作ろう!
@snapend
@snapend

---
### @css[slide-title](本日のゴールイメージ)

@snap[slide-contents]
@img[goal-image to-center](template/img/finish.png)
@snapend

---
### @css[slide-title](ハンズオン講習会の流れ)

@snap[slide-contents]

@ol[numberlist numberlist-color1](false)
- 基礎知識			@css[detail-comment](Webの仕組みやプログラミングに必要な知識を学ぶ)
- 環境構築			@css[detail-comment](地図アプリを作るために必要なPCの設定をする)
- APIサーバの構築	@css[detail-comment](地図アプリを提供するためのシステムを作る)
- 地図の表示		@css[detail-comment](まずは地図を表示してみる)
- 外部APIの呼び出し		@css[detail-comment](公開されている地図システムを利用する)
- DBの操作			@css[detail-comment](使いたいデータを登録する)
- 内部APIの呼び出し		@css[detail-comment](ツールを使って地図アプリを配信する)
- 地図へのポイント追加	@css[detail-comment](説明文説明文説明文説明文説明文)
- 自分の緯度経度の取得	@css[detail-comment](説明文説明文説明文説明文説明文)
- CSSデータの読み込み	@css[detail-comment](説明文説明文説明文説明文説明文)
- デプロイ				@css[detail-comment](説明文説明文説明文説明文説明文)
- 最後に全項目にページ内リンクを貼る				@css[detail-comment](説明文説明文説明文説明文説明文)
@olend

@snapend

---?include=template/md/basic-knowlede-webgis/PITCHME.md
---?include=template/md/environment/PITCHME.md
---?include=template/md/create-a-new-project/PITCHME.md
---?include=template/md/add-modules/PITCHME.md
---?include=template/md/how-to-test-Elixir-project/PITCHME.md
---?include=template/md/external-API/PITCHME.md
---?include=template/md/use-RESTClient/PITCHME.md
---?include=template/md/external-API-data/PITCHME.md
---?include=template/md/display-data-on-web-page/PITCHME.md
---?include=template/md/display-map-on-web-page/PITCHME.md
---?include=template/md/add-location-data/PITCHME.md


---?color=#3A8FB7
@snap[breadcrumbs-wrap bluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [n. アジェンダ項目名]()
@olend
@snapend

@snap[west headline]
## アジェンダ項目名
@snapend

---

@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [n. アジェンダ項目名]()
@olend
@snapend

### @css[slide-title](テンプレートA1 - 大項目)

@snap[slide-contents]

@box[rounded box-style](アジェンダ項目（大項目）用の、テンプレートです。<br>項目の概要を、説明します。)

@snap[left-column]
@ol[numberlist numberlist-color2](false)
- アジェンダ項目内の小項目
- 小項目
- 小項目
- 小項目
- 体言止め
- a
@olend
@snapend


@snap[right-column]
@ol[numberlist numberlist-color2 start-7](false)
- アジェンダ項目内の小項目
- 小項目
- 小項目
- 小項目
- 体言止め
- ここまで
@olend
@snapend

@snapend

---

@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [n. アジェンダ項目名]()
- [m. 中項目名]()
@olend
@snapend

### @css[slide-title](テンプレートA2 - 中項目)

@snap[slide-contents]

@box[rounded box-style](中項目用の、テンプレートです。<br>項目の概要を、説明します。)

@snap[left-column]
@ol[numberlist numberlist-color3](false)
- アジェンダ項目内の小項目
- 小項目
- 小項目
- 小項目
- 体言止め
- a
@olend
@snapend


@snap[right-column]
@ol[numberlist numberlist-color3](false)
- アジェンダ項目内の小項目
- 小項目
- 小項目
- 小項目
- 体言止め
- ここまで
@olend
@snapend

@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [n. アジェンダ項目名]()
- [m. 小項目名]()
- [k. ここまで]()
@olend
@snapend

### @css[slide-title](テンプレートB - 言葉・概念の意味)

@snap[slide-contents]

@snap[quote-wrap]
@quote[<ul><li>ユーザインタフェース<ul><li>ユーザインタフェース1</li><li>ユーザインタフェース2</li></ul></li><li>文字列が表示されるウィンドウに出力</li><li>キーボード等から文字列を入力</li></ul>](https://ja.m.wikipedia.org/wiki/キャラクタユーザインタフェース)
@quote[キーボード等から文字列を入力](https://ja.m.wikipedia.org/wiki/キャラクタユーザインタフェース)
@snapend

@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [n. アジェンダ項目名]()
- [m. 小項目名]()
- [k. ここまで]()
@olend
@snapend

### @css[slide-title](テンプレートC - Bのテーブル版)

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
- [ハンズオン講習会の流れ](#/2)
- [n. アジェンダ項目名]()
- [m. 小項目名]()
- [k. ここまで]()
@olend
@snapend

### @css[slide-title](テンプレートD - 作業説明)

@snap[slide-contents]

@snap[left-column]
@ol[numberlist numberlist-color3](false)
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

@snap[right-column]
@ol[numberlist  numberlist-color3 start-11](false)
- Web基礎知識
- 環境構築
- APIServerの構築
- 地図の表示
- 外部API呼び出し
- DB操作
- 内部API呼び出し
- 地図へのポイント追加
- 自分の緯度経度の取得
- ここまで
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

### @css[slide-title](テンプレートE - 手順詳細)

@snap[slide-contents]

@box[rounded box-style](手順詳細用の、テンプレートです。<br>この作業の目的を、ここに書きます。)

@snap[left-column]
@ol[numberlist numberlist-color4](true)
- 手順１や、
- 手順２など、
- ここに、書いていきます。
- 書いていきます<br>書いていきます書いていきます。
@olend
@snapend

@snap[right-column]
@ol[numberlist numberlist-color4 start-6](true)
- 手順6なら`start-6`と書き、
- 書いていきます。
- 手順詳細の、
- 番号の色をかえようかな。
- ここまで
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

### @css[slide-title](テンプレートE0 - 手順詳細ワイド)

@snap[slide-contents]

@box[rounded box-style](手順詳細用の、テンプレートです。<br>この作業の目的を、ここに書きます。)

@ol[numberlist numberlist-color4](true)
- 手順１や、
- 手順２など、
- ここに、書いていきます。
- 書いていきます書いていきます書いていきます。
@olend

@snapend


---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [9. 抽出データのWebページ表示](#/)
- [4. HTMLファイルの実装（プログラム）](#/)
@olend
@snapend

### @css[slide-title smaller-font](テンプレートE1 - 手順詳細コード)

@snap[slide-contents]

@box[rounded box-style]( **Visual Studio Code** を使って、オープンしている<br>index.html.eexファイルに変更を加えます。)

```elixir
<% [ result ] = Json.get("https://aed.azure-mobile.net", "/api/NearAED?lat=35.96&lng=136.185")
  latitude = Map.get(result,"Latitude")
  longitude = Map.get(result,"Longitude")
  locationName = Map.get(result,"LocationName")
%>
```

@[1-5](全てをコピーして、index.html.eexファイルに貼り付けます。)


@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [n. アジェンダ項目名]()
- [m. 小項目名]()
- [k. ここまで]()
@olend
@snapend

### @css[slide-title](テンプレートE2 - 手順詳細&コード)

@snap[slide-contents]

@box[rounded box-style](作業の内容と目的,使用するソフトウェア)

@snap[left-column]
@ol[numberlist numberlist-color3](false)
- 手順
- 手順
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

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [n. アジェンダ項目名]()
- [m. 小項目名]()
- [k. ここまで]()
@olend
@snapend

### @css[slide-title](テンプレートE3 - 手順詳細&画像)

@snap[slide-contents]

@box[rounded box-style](作業の内容と目的,使用するソフトウェア)

@snap[left-column]
@ol[numberlist numberlist-color3](true)
- 手順
- 手順
@olend
@snapend

@snap[right-column]
@img[goal-image to-center](template/img/environment/postgresql.png)
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

### @css[slide-title](テンプレートF - 手順ゴール画像)

@snap[slide-contents]

@img[goal-image to-center](template/img/environment/postgresql.png)

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

### @css[slide-title](テンプレートG1 - 手順ゴール条件)

@snap[slide-contents margin-left1]

@ul[itemlist](false)
- 条件１
- 条件２
- 条件３
@ulend

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

### @css[slide-title](テンプレートG2 - ゴール条件&画像)

@snap[slide-contents]

@snap[left-column]
@ul[itemlist](false)
- 条件１
- 条件２
- 条件３
@ulend
@snapend

@snap[right-column]
@img[goal-image to-center](template/img/environment/postgresql.png)
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

### @css[slide-title](テンプレートH - ソースコード)

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
