---?color=#3A8FB7
@snap[breadcrumbs-wrap bluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [3. APIサーバーの構築]()
@olend
@snapend

@snap[west headline]
## APIサーバーの構築
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [3. APIサーバーの構築]()
@olend
@snapend

### @css[slide-title](APIサーバーの構築)

@snap[slide-contents]

@box[rounded box-style](地図アプリを提供するためのシステムを作ります。)

@snap[left-column]
@ol[numberlist numberlist-color2 width-60](false)
- プロジェクトの作成
- Webサーバーの確認
- サーバーの起動
- サーバーの終了方法
- フォルダ移動
- DBの作成
@olend
@snapend


@snap[right-column]
@ol[numberlist numberlist-color2 start-7](false)
- JSONデータの作成
- Router.ex の設定
- マイグレーション
- RESTClient の設定
- RESTClientで GET
- RESTClientで POST
@olend
@snapend

@snapend

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [3. APIサーバーの構築]()
- [1. プロジェクトの作成]()
@olend
@snapend

@snap[west headline]
## @color[white](プロジェクトの作成)
@snapend

---

@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [3. APIサーバーの構築]()
- [1. プロジェクトの作成]()
@olend
@snapend

### @css[slide-title](プロジェクトの作成)

@snap[slide-contents]

@box[rounded box-style](作業の内容と目的,使用するソフトウェア)

@snap[left-column]
@ol[numberlist numberlist-color3](false)
- プロジェクトの作成
- パッケージの取り込み
- モジュールバンドラの導入
- フォルダの移動
- DBの作成
- サーバーの起動
@olend
@snapend


@snap[right-column]
@snap[goal-image]
@img[](template/img/Building-APIServer/1-ctr-c.png)
@snapend
@snapend

@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [3. APIサーバーの構築]()
- [1. プロジェクトの作成]()
- [k. 手順]()
@olend
@snapend

### @css[slide-title](手順)

@snap[slide-contents]

@box[rounded box-style](作業の内容と目的,使用するソフトウェア)

@snap[left-column]
@ol[numberlist numberlist-color3](false)
- mix phx.new gismap
- Y
@olend
@snapend


@snap[right-column]
@snap[gist-box half-gist-box]

@gist[zoom-09](yuki-thewaggle/82bf9f1de5b6963bcb47f02e7b1c5d09)

@[1](プロジェクトを「gismap」という名前で作成します)
@[2](関連するファイルをインストールをします)

@snapend
@snapend

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [3. APIサーバーの構築]()
- [2. Webサーバーの確認]()
@olend
@snapend

@snap[west headline]
## @color[white](Webサーバーの確認)
@snapend

---

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [3. APIサーバーの構築]()
- [3. サーバーの起動]()
@olend
@snapend

@snap[west headline]
## @color[white](サーバーの起動)
@snapend

---

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [3. APIサーバーの構築]()
- [4. サーバーの終了方法]()
@olend
@snapend

@snap[west headline]
## @color[white](サーバーの終了方法)
@snapend

---

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [3. APIサーバーの構築]()
- [5. フォルダ移動]()
@olend
@snapend

@snap[west headline]
## @color[white](フォルダ移動)
@snapend

---

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [3. APIサーバーの構築]()
- [6. DBの作成]()
@olend
@snapend

@snap[west headline]
## @color[white](DBの作成)
@snapend

---

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [3. APIサーバーの構築]()
- [7. JSONデータの作成]()
@olend
@snapend

@snap[west headline]
## @color[white](JSONデータの作成)
@snapend

---

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [3. APIサーバーの構築]()
- [8. Router.ex の設定]()
@olend
@snapend

@snap[west headline]
## @color[white](Router.ex の設定)
@snapend

---

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [3. APIサーバーの構築]()
- [9. マイグレーション]()
@olend
@snapend

@snap[west headline]
## @color[white](マイグレーション)
@snapend

---

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [3. APIサーバーの構築]()
- [10. RESTClient の設定]()
@olend
@snapend

@snap[west headline]
## @color[white](RESTClient の設定)
@snapend

---

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [3. APIサーバーの構築]()
- [11. RESTClientで GET]()
@olend
@snapend

@snap[west headline]
## @color[white](RESTClientで GET)
@snapend

---

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [3. APIサーバーの構築]()
- [12. RESTClientで POST]()
@olend
@snapend

@snap[west headline]
## @color[white](RESTClientで POST)
@snapend

---

---

---?color=#EFBB24
# @css[headline](APIServerの構築)

---
@snap[midopoint north-west text-06]
### プロジェクトファイルの生成
@snapend

@snap[midpoint]
@gist[zoom-06](Yoosuke/a3b22fb6c27ef03d978d37bc80e88618)

@[1](gismapという名前でプロジェクトを作成します)
@[3](Yを入力します)
@[7](gismapのディレクトリに移動します)
@[11](DBを作成します)
@[15](サーバーを起動します)

@snapend

---
@snap[north-west text-06]
### WebServerの確認
@snapend

@snap[text-05]
ブラウザで「`http://localhost:4000`」にアクセス。<br>
Phoenixで作られたデフォルトのWebページが表示される事を確認しましょう。<br>
無事に見られたら、成功です。<br>

@img[span-60](template/img/environment/localhost4000.png)

@snapend

---
@snap[north-west text-06]
### サーバーの終了方法
@snapend


@img[span-60](template/img/Building-APIServer/1-ctr-c.png)

@snap[sorth text-10]
Ctrl+C を2回打つ
@snapend


---
@snap[north-west text-06]
### JSONデータを作る
@snapend

@snap[text-05]
ターミナルで以下を打つ<br>
緯度と経度と名称を入れるためのJSONを作る<br><br>

@color[#6F3381](mix phx.gen.json コンテキスト名 スキーマ名 スキーマ名の複数形　データ名：データ型)<br><br>

@gist[elixir midpoint zoom-15](Yoosuke/e18deaff49fd420a220bb338602160fc)

<br><br>このコマンドは、JSONリソースのcontroller, views, contextを生成します。<br><br>

詳しくは、[こちら](https://hexdocs.pm/phoenix/Mix.Tasks.Phx.Gen.Json.html)のライブラリに記載されています。
@snapend

---
@snap[north-west text-06]
### Router.exを設定する
@snapend


@gist[elixir midpoint zoom-07](Yoosuke/426e9d127ab84f72e0493874b7ddac77)

@[3](ファイルに追加するのでコピーしておきます。)

---?terminal=template/sessions/start-up-code.json&color=#7FDBFF&font=small&title=VSCODEでファイルを開く

---

![Video](https://player.vimeo.com/video/311145345)

---?color=#1E1F21
@code[elixir zoom-4](template/src/elixir/router.ex)

@[8](コメントアウトする)
@[20](ここに先ほどコピーした内容をペーストします)

---?color=#000000
@snap[north-west text-06]
### マイグレーションする
@snapend

@code[elixir midpoint zoom-10](template/src/elixir/migrate.ex)

---?color=#000000
@snap[north-west text-06]
### サーバー立ち上げる
@snapend

@code[elixir zoom-4 midpoint](template/src/elixir/start.ex)

@snap[south text-06]
Phoenixを起動します
@snapend

---?terminal=template/sessions/start-server.json

---
@snap[north-west text-06]
### ブラウザで確認
@snapend

@img[span-60](template/img/Building-APIServer/5-localhost.png)

@snap[south text-06]
localhost:4000で表示されていれば成功
@snapend

---
@snap[north-west text-06]
### RESTClientでGet,Postの動作確認
@snapend

![Video](https://player.vimeo.com/video/311154615)

---?color=#333333
@snap[north-west text-06]
### RESTClientの設定
@snapend

@snap[midpoint text-05]

RESTClientの「Headers」メニューで、<br>
「Custom Header」を選択<br>

Nameに　``` Content-Type ```<br><br>

Attribute Valueには　``` application/json ```<br><br>

を入力します。

@snapend

---
@snap[north-west text-06]
### データの確認
@snapend

@snap[midpoint text-05]
まだ、データは何も入っていないので、次のような状態になります。

```

{"data":[]}

```
@snapend

---
@snap[north-west text-06]
### RESTClientを使ってデータをPOSTする
@snapend

@snap[text-05]
Methodの所を「POST」に変更します。
Bodyに<br>
@color[#6F3381]({ "location": { "lat": 35.70822, "lng": 131.463398, "pointname": "test" } })<br>
を入力してSENDします。<br>

@img[span-50](template/img/Building-APIServer/2-rest-post.png)

@snapend


