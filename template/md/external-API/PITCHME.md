---?color=#3A8FB7
@snap[breadcrumbs-wrap bluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [6. APIの利用](#/)
@olend
@snapend

@snap[west headline]
## APIの利用
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [6. APIの利用](#/)
@olend
@snapend

### @css[slide-title](APIの利用)

@snap[slide-contents]

@box[rounded box-style](Phoenix を使ってWebプロジェクトを作成します。)

@ol[numberlist numberlist-color2](false)
- [APIとは](#/)
- [AEDオープンデータプラットフォーム](#/)
- [AAEDオープンデータプラットフォームとは](#/)
- [直近AED位置情報取得API](#/)
- [確認](#/)
@olend

@snapend

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [6. APIの利用](#/)
- [1. APIとは](#/)
@olend
@snapend

@snap[west headline]
## @color[white](APIとは)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [6. APIの利用](#/)
- [1. APIとは](#/)
@olend
@snapend

### @css[slide-title](APIとは)

@snap[slide-contents]
@snap[quote-wrap]

@quote[<ul><li>プログラミング言語から提供される構造<li>開発者が**複雑な機能をより簡単に**作成できる</li><li>複雑なコードにかわる**簡潔な構文**を提供</li></ul>](https://developer.mozilla.org/ja/docs/Learn/JavaScript/Client-side_web_APIs/Introduction)

@snapend
@snapend

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [6. APIの利用](#/)
- [2. AEDオープンデータプラットフォーム](#/)
@olend
@snapend

@snap[west headline]
## @color[white](AEDオープンデータプラットフォーム)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [6. APIの利用](#/)
- [2. AEDオープンデータプラットフォーム](#/)
@olend
@snapend

### @css[slide-title smaller-font](AEDオープンデータプラットフォーム)

@snap[slide-contents]
@img[goal-image to-center](template/img/external-API/aed-opendata-platform.png)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [6. APIの利用](#/)
- [3. AEDオープンデータプラットフォームとは](#/)
@olend
@snapend

### @css[slide-title smallest-font](AEDオープンデータプラットフォームとは)

@snap[slide-contents]

@box[rounded box-style](今回は<u>[AEDオープンデータプラットフォーム](http://hatsunejournal.jp/w8/AEDOpendata/)</u>を利用します。<br>これは、AEDの設置箇所に関する情報を取得できるAPIです。)

@ol[numberlist numberlist-color4](false)
- Webブラウザーを使って、<u>http://hatsunejournal.jp/w8/AEDOpendata/</u>にアクセスします。
- 画面上部のメニューから **API** をクリックします。
- 利用できるAPIを確認します。
@olend

@snapend

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [6. APIの利用](#/)
- [3. 直近AED位置情報取得API](#/)
@olend
@snapend

@snap[west headline]
## @color[white](直近AED位置情報<br>取得API)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [6. APIの利用](#/)
- [3. 直近AED位置情報取得API](#/)
@olend
@snapend

### @css[slide-title](直近AED位置情報取得API)

@snap[slide-contents]

@box[rounded box-style](**Webブラウザー** を使って、<br>ある地点から直近のAED位置情報を取得してみます。)

@ol[numberlist numberlist-color4](true)
- <u>https://aed.azure-mobile.net/api/NearAED?lat=35.96&lng=136.185</u> にアクセスします。
- これは、**北緯（lat）35.96** 、 **東経（lng）136.185** の地点から最も近いAEDの情報です。
@olend

@snapend

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [6. APIの利用](#/)
- [4. 確認](#/)
@olend
@snapend

@snap[west headline]
## @color[white](確認)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [6. APIの利用](#/)
- [4. 確認](#/)
@olend
@snapend

### @css[slide-title](確認)

@snap[slide-contents]

@box[rounded box-style](**Webブラウザー** を使って、<br>任意の地点から直近のAED情報を取得してみます。)

@snap[left-column]
@ol[numberlist numberlist-color4](false)
- 例えば、東京駅の<br>**北緯（lat）35.68**<br>**東経（lng）139.767** だと<br><u>@size[0.7em](https://aed.azure-mobile.net/api/NearAED?lat=35.68&lng=139.767)</u>です。
@olend
@snapend

@snap[right-column]
@snap[gist-box half-gist-box]

@gist[json zoom-06](yuki-thewaggle/8d5c582ba46e0350acc6fcba0d66439c)

@[0](上記（先程）とは別データを取得したことを確認します。)

@snapend
@snapend

@snapend

