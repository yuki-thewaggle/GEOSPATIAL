---?color=#3A8FB7
@snap[breadcrumbs-wrap bluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [11. 地点データの追加](#/)
@olend
@snapend

@snap[west headline]
## 地点データの追加
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [11. 地点データの追加](#/)
@olend
@snapend

### @css[slide-title](地点データの追加)

@snap[slide-contents]

@box[rounded box-style](Phoenix を使ってDBとの連携をします。)

@snap[left-column]
@ol[numberlist numberlist-color2](false)
- [外部データからの追加](#/)
- [DBとは](#/)
- [SQLとは](#/)
- [Tableの設計](#/)
- [ルートの設定](#/)
- [テーブルの生成](#/)
@olend
@snapend

@snap[right-column]
@ol[numberlist numberlist-color2 start-7](false)
- [表示の確認](#/)
- [緯度・経度を調べる](#/)
- [DBへの入力](#/)
- [入力・修正・削除](#/)
@olend
@snapend

@snapend


---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [11. 地点データの追加](#/)
- [1. 外部データからの追加](#/)
@olend
@snapend

@snap[west headline]
## @color[white](外部データからの<br>追加)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [11. 地点データの追加](#/)
- [1. 外部データからの追加](#/)
@olend
@snapend

### @css[slide-title](外部データからの追加)

@snap[slide-contents]
@snap[gist-box]

@fa[external-link]
<u>https://gist.github.com/Yoosuke/ec1b601b0f7bad26fc15629634c86d1b</u>

@gist[js zoom-08](Yoosuke/ec1b601b0f7bad26fc15629634c86d1b)

@[1](緯度経度を記載する箇所を<%= latitude >、<%= longitude %>に変更します。)
@[7-8](<%= latitude %>、<%= longitude %>、<%= locationName　%>を変更します。)

@snapend
@snapend


---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [11. 地点データの追加](#/)
- [2. DBとは](#/)
@olend
@snapend

@snap[west headline]
## @color[white](DBとは)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [11. 地点データの追加](#/)
- [2. DBとは](#/)
@olend
@snapend

### @css[slide-title](DBとは)

@snap[slide-contents]

@box[rounded box-style](DB 「Data Base」とは、特定の条件によって、まとめられたデータの集合です。よく利用されているDBの一つにRDB「Relational Data Base」というものがあります。RDBでは、Tableと呼ばれる表形式のようなデータ構造を利用します。)

@snapend


---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [11. 地点データの追加](#/)
- [3. SQLとは](#/)
@olend
@snapend

@snap[west headline]
## @color[white](SQLとは)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [11. 地点データの追加](#/)
- [3. SQLとは](#/)
@olend
@snapend

### @css[slide-title](SQLとは)

@snap[slide-contents]

@box[rounded box-style](SQL(Structured Query Language)とは、RDBで、データベースのオブジェクトに対して、定義や変更、データの操作などを行う言語です。)

SQLは大きく３つの体系から分類できます。
@ol[numberlist numberlist-color2](false)
- データ操作 (SELECT, INSERT, UPDATA, DELETE)
- データ定義 (CREATE TABLE, DROP TABLE...)
- データ制御 (START TRANSACTION...)
@olend

@snapend


---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [11. 地点データの追加](#/)
- [4. Tableの設計](#/)
@olend
@snapend

@snap[west headline]
## @color[white](Tableの設計)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [11. 地点データの追加](#/)
- [4. Tableの設計](#/)
@olend
@snapend

### @css[slide-title](Tableの設計)

@snap[slide-contents]

@box[rounded box-style](**CUI** を利用して、Tableの設計します。)

@ol[numberlist numberlist-color2](false)
- [```mix phx.gen.html AED Location locations latitude:float longitude:float locationName:string```](#/)
- [上記のコマンドを貼り付けます。](#/)
- [コマンドが実行されると、次のような内容が表示されます。](#/)
- [```resources "/locations", LocationController```](#/)
- [上記のコマンドをコピーします。](#/)
@olend

@snapend


---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [11. 地点データの追加](#/)
- [5. ルートの設定](#/)
@olend
@snapend

@snap[west headline]
## @color[white](ルートの設定)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [11. 地点データの追加](#/)
- [5. ルートの設定](#/)
@olend
@snapend

### @css[slide-title](ルートの設定)

@snap[slide-contents]

@box[rounded box-style](**Visual Studio Code** を利用します。```router.ex```のファイルを開きます。)

@ol[numberlist numberlist-color2](false)
- [```lib/aedmap_web/router.ex```を開きます。](#/)
- [```scope "/", AedmapWeb do pipe_through :browser```と書かれている箇所を探します](#/)
- [```get "/", PageController, :index```の直下に以下をペーストします。](#/)
- [```resources "/locations", LocationController```](#/)
@olend

@snapend


---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [11. 地点データの追加](#/)
- [6. テーブルの生成](#/)
@olend
@snapend

@snap[west headline]
## @color[white](テーブルの生成)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [11. 地点データの追加](#/)
- [6. テーブルの生成](#/)
@olend
@snapend

### @css[slide-title](テーブルの生成)

@snap[slide-contents]

@box[rounded box-style](**CUI** を利用します。コマンドを利用して設計したテーブルを生成します。)

@ol[numberlist numberlist-color2](false)
- [```mix ecto.migrate```](#/)
- [上記のコマンドをCUIにペーストします。](#/)
- [errorが表示されなければ成功です。](#/)
- [```iex -S mix phx.server ```](#/)
- [上記のコマンドをペーストして、サーバーを起動します。](#/)
@olend

@snapend


---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [11. 地点データの追加](#/)
- [7. 表示の確認](#/)
@olend
@snapend

@snap[west headline]
## @color[white](表示の確認)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [11. 地点データの追加](#/)
- [7. 表示の確認](#/)
@olend
@snapend

### @css[slide-title](表示の確認)

@snap[slide-contents]

@box[rounded box-style](**ブラウザ** を利用します。URL：```http://localhost:4000/locations```から追加したページが表示される事を確認します。)

@snap[left-column]
@ol[numberlist numberlist-color2](false)
- [URLに```/locations```を追記する](#/)
@olend
@snapend

@snap[right-column]
@img[goal-image to-center](template/img/add-location-data/locations.png)

@snapend

@snapend


---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [11. 地点データの追加](#/)
- [8. 緯度・経度を調べる](#/)
@olend
@snapend

@snap[west headline]
## @color[white](緯度・経度<br>を調べる)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [11. 地点データの追加](#/)
- [8. 緯度・経度を調べる](#/)
@olend
@snapend

### @css[slide-title](緯度・経度を調べる)

@snap[slide-contents]

@fa[external-link]
[AED設置施設](https://www.city.bunkyo.lg.jp/bosai/bosai/bousai/snota/aed/settikasho.html)ページの、
[AED設置施設一覧表](https://www.city.bunkyo.lg.jp/var/rev0/0110/3859/2016510114959.pdf)を開きます。<br>

@box[rounded box-style](**ブラウザ**を利用します。文京シビックセンター等のセンター名称のみ記載されているデータから、緯度経度を調べてDBに入力します。)


@ol[numberlist numberlist-color2](false)
- [Yahoo!地図で緯度・経度を調べる **<-クリック** ](https://user.numazu-ct.ac.jp/~tsato/webmap/sphere/coordinates/yahoo_olp/)
- 検索に「文京シビックセンター」で検索します
- 検索結果に２件ほど表示されます１つをクリックします。
- 緯度と経度をコピーします。

@olend
@snapend


---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [11. 地点データの追加](#/)
- [9. DBへの入力](#/)
@olend
@snapend

@snap[west headline]
## @color[white](DBへの入力)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [11. 地点データの追加](#/)
- [9. DBへの入力](#/)
@olend
@snapend

### @css[slide-title](DBへの入力)

@snap[slide-contents]

@box[rounded box-style](**ブラウザ**を利用します。```http://localhost:4000/locations```)

@snap[left-column]

@ol[numberlist numberlist-color2](false)
- [New Locationをクリック](http://localhost:4000/locations/new)
- 緯度経度や名前を入力
- SAVEをクリック
@olend

@snapend

@snap[right-column]

@img[goal-image to-center](template/img/add-location-data/newlocation.png)

@snapend

@snapend


---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [11. 地点データの追加](#/)
- [10. 入力・修正・削除](#/)
@olend
@snapend

@snap[west headline]
## @color[white](入力・修正・削除)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [11. 地点データの追加](#/)
- [10. 入力・修正・削除](#/)
@olend
@snapend

### @css[slide-title](入力・修正・削除)

@snap[slide-contents]

@box[rounded box-style](**ブラウザ**を利用します。```http://localhost:4000/locations```のページから、それぞれ入力・修正・削除ができます。)

@ol[numberlist numberlist-color2](false)
- [もう１件データを追加します](#/)
- 礫川地域活動センター, 35.711938、 139.750418
@olend


@snapend
