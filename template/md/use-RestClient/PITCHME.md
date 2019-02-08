---?color=#3A8FB7
@snap[breadcrumbs-wrap bluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [7. RESTClient の操作](#/)
@olend
@snapend

@snap[west headline]
## RESTClient の操作
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [7. RESTClient の操作](#/)
@olend
@snapend

### @css[slide-title](RESTClient の操作)

@snap[slide-contents]

@box[rounded box-style](Phoenix を使ってWebプロジェクトを作成します。)

@snap[left-column]
@ol[numberlist numberlist-color2](false)
- [RESTClient の起動](#/)
- [URLの設定](#/)
- [Methodの設定](#/)
- [Requestの送信](#/)
- [ステータスコードを確認](#/)
@olend
@snapend

@snapend

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [7. RESTClient の操作](#/)
- [1. RESTClient の起動](#/)
@olend
@snapend

@snap[west headline]
## @color[white](RESTClient の起動)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [7. RESTClient の操作](#/)
- [1. RESTClient の起動](#/)
@olend
@snapend

### @css[slide-title](RESTClient の起動)

@snap[slide-contents]

@box[rounded box-style]( **Firefox** を使って、RESTClient を起動します。)

@snap[left-column]
@ol[numberlist numberlist-color4](true)
- Firefoxを起動します。
- 右上にある**RESTClientのアイコン**をクリックします。
- Migrate from RESTClient 2 というウィンドウを&#215;ボタンで閉じます。
- RESTClient が起動します。
@olend
@snapend

@snap[right-column]
@img[goal-image to-center](template/img/use-RESTClient/RESTClient.png)
@snapend

@snapend

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [7. RESTClient の操作](#/)
- [2. URLの設定](#/)
@olend
@snapend

@snap[west headline]
## @color[white](URLの設定)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [7. RESTClient の操作](#/)
- [2. URLの設定](#/)
@olend
@snapend

### @css[slide-title](URLの設定)

@snap[slide-contents]

@box[rounded box-style]( **RESTClient** を使って、取得したいページのURLの設定します。)

@snap[left-column]
@ol[numberlist numberlist-color4](true)
- **Request** の **URL** の入力部分をクリックします。
- @css[orange not-linkable](https://aed.azure-mobile.net/api/NearAED?lat=35.96&lng=136.185)<span class="not-selectable"> を貼り付けます。</span>
- これは、<u>[直近AED位置情報取得API](http://hatsunejournal.jp/w8/AEDOpendata/)</u>のURLです。
@olend
@snapend

@snap[right-column]
@img[goal-image to-center](template/img/use-RESTClient/set-url.png)
@snapend

@snapend

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [7. RESTClient の操作](#/)
- [3. Methodの設定](#/)
@olend
@snapend

@snap[west headline]
## @color[white](Methodの設定)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [7. RESTClient の操作](#/)
- [3. Methodの設定](#/)
@olend
@snapend

### @css[slide-title](Methodの設定)

@snap[slide-contents]

@box[rounded box-style]( **RESTClient** を使って、ページに対する要求（Request）を設定します。)

@snap[left-column]
@ol[numberlist numberlist-color4](true)
- **Request** の **Method** の部分を開きます。

- **GET** をクリックします。
- これで<u>[リクエストメソッド](https://developer.mozilla.org/ja/docs/Web/HTTP/Methods)</u>が設定できました。
@olend
@snapend

@snap[right-column]
@img[goal-image to-center](template/img/use-RESTClient/set-method.png)
@snapend

@snapend

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [7. RESTClient の操作](#/)
- [4. Requestの送信](#/)
@olend
@snapend

@snap[west headline]
## @color[white](Requestの送信)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [7. RESTClient の操作](#/)
- [4. Requestの送信](#/)
@olend
@snapend

### @css[slide-title](Requestの送信)

@snap[slide-contents]

@box[rounded box-style]( **RESTClient** を使って、ページにRequestを送信します。)

@snap[left-column]
@ol[numberlist numberlist-color4](true)
- **Request** の **SEND** ボタンをクリックします。
- Requestが送信され、画面が更新されます。
@olend
@snapend

@snap[right-column]
@img[goal-image to-center fragment](template/img/use-RESTClient/request-send.png)
@snapend

@snapend


---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [7. RESTClient の操作](#/)
- [5. ステータスコードを確認](#/)
@olend
@snapend

@snap[west headline]
## @color[white](ステータスコードを<br>確認)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [7. RESTClient の操作](#/)
- [5. ステータスコードを確認](#/)
@olend
@snapend

### @css[slide-title](ステータスコードを確認)

@snap[slide-contents]

@box[rounded box-style]( **RESTClient** を使って、<br>ページに対するRequestが正常に完了したかを確認します。)

@snap[left-column]
@ol[numberlist numberlist-color4](true)
- **Request** の **Status Code** に **200 OK** と表示されていることを確認します。
- これは、ページの情報を取得する<u>[リクエスト](https://developer.mozilla.org/ja/docs/Web/HTTP/Methods)</u>が**成功**したときに返される<u>[ステータスコード](https://developer.mozilla.org/ja/docs/Web/HTTP/Status)</u>です。
@olend
@snapend

@snap[right-column]
@img[goal-image to-center](template/img/use-RESTClient/responce-200ok.png)
@snapend

@snapend

