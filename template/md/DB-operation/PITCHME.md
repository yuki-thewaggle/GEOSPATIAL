---?color=#3A8FB7
@snap[breadcrumbs-wrap bluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [12. DBからのData取得](#/)
@olend
@snapend

@snap[west headline]
## DBからのData取得
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [12. DBからのData取得](#/)
@olend
@snapend

### @css[slide-title](DBからのData取得)

@snap[slide-contents]

@box[rounded box-style](Ectoを利用してDBからDataを取得します。)

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
- [12. DBからのData取得](#/)
- [1. Ectoを利用したDataの取得](#/)
@olend
@snapend

@snap[west headline]
## @color[white](Ectoを利用した<br>Dataの取得)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [12. DBからのData取得](#/)
- [1. Ectoを利用したDataの取得](#/)
@olend
@snapend

### @css[slide-title](Ectoを利用したDataの取得)

@snap[slide-contents]

@box[rounded box-style](**CUI** を利用します。Ecto.Adapters.SQL.queryを利用してDataを取得します。)

@fa[external-link]
[Ecto.Adapters.SQL](https://hexdocs.pm/ecto/2.2.8/Ecto.Adapters.SQL.html#query/4)

@ol[numberlist numberlist-color2](false)
- ```Ecto.Adapters.SQL.query( Aedmap.Repo  ,"SELECT * FROM locations", [])```
- 上記のコマンドをコピーしてCUIにペーストします。
- ```{ status, struct }```というタプル型のデータが返ってきます。
@olend

@snapend


---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [12. DBからのData取得](#/)
- [2. 取得されたDataの確認](#/)
@olend
@snapend

@snap[west headline]
## @color[white](取得された<br>Dataの確認)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [12. DBからのData取得](#/)
- [2. 取得されたDataの確認](#/)
@olend
@snapend

### @css[slide-title](取得されたDataの確認)

@snap[slide-contents]

@box[rounded box-style](**CUI** を利用します。取得したDataの構造体を確認します。)

@snap[gist-box]
@gist[js zoom-08](Yoosuke/32b8b3d1d4cb5ffba23c93fffd1219d6)
@snapend

@[1](```:ok```というステータスが返ってきています。)
@[2](```%Postgrex.Result```という構造体の形式でDataが取得されています。)
@[3](```columns:```には、テーブルのカラムに関するデータが入っています。)
@[9-14](```rows:```には、テーブルのロウに関するデータがリスト型で入っています。)

@snapend

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [12. DBからのData取得](#/)
- [3. DB取得のモジュール開発](#/)
@olend
@snapend

@snap[west headline]
## @color[white](DB取得の<br>モジュール開発)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [12. DBからのData取得](#/)
- [3. DB取得のモジュール開発](#/)
@olend
@snapend

### @css[slide-title](DB取得のモジュール開発)

@snap[slide-contents]

@box[rounded box-style](**Visual Studio Code** を利用します。lib/util/db.exを作ります。)

@snap[left-column]

@ul[itemlist](false)
- ```lib/```直下に```util/```の作成
- ```util/```直下に```db.ex```ファイルの作成
@ulend

@snapend

@snap[right-column]
@img[goal-image to-center](template/img/DB-operation/Visual_Studio_Code.png)
@snapend

@snapend