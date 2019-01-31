---?color=#3A8FB7
@snap[breadcrumbs-wrap bluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [3. Phoenix プロジェクトの作成](#/)
@olend
@snapend

@snap[west headline]
## Phoenix<br>プロジェクトの作成
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [3. Phoenix プロジェクトの作成](#/)
@olend
@snapend

### @css[slide-title](Phoenix プロジェクトの作成)

@snap[slide-contents]

@box[rounded box-style](Phoenix を使ってWebプロジェクトを作成します。)

@snap[left-column]
@ol[numberlist numberlist-color2](false)
- [プロジェクトの作成](#/)
- [フォルダの移動](#/)
- [データベースの作成](#/)
- [アプリケーションの起動](#/)
- [Webサイトの確認](#/)
- [サーバーの終了](#/)
@olend
@snapend

@snapend

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [3. Phoenix プロジェクトの作成](#/)
- [1. プロジェクトの作成](#/)
@olend
@snapend

@snap[west headline]
## @color[white](プロジェクトの作成)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [3. Phoenix プロジェクトの作成](#/)
- [1. プロジェクトの作成](#/)
@olend
@snapend

### @css[slide-title](プロジェクトの作成)

@snap[slide-contents]

@box[rounded box-style](プロジェクトのフォルダ構成と<br>必要なソースコードを生成します。)

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
- [3. Phoenix プロジェクトの作成](#/)
- [2. フォルダの移動](#/)
@olend
@snapend

@snap[west headline]
## @color[white](フォルダの移動)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [3. Phoenix プロジェクトの作成](#/)
- [2. フォルダの移動](#/)
@olend
@snapend

### @css[slide-title](フォルダの移動)

@snap[slide-contents]

@box[rounded box-style](プロジェクトのフォルダに移動します。)

@snap[left-column]
@ol[numberlist numberlist-color4](false)
- cd aedmap
@olend
@snapend

@snap[right-column]
@snap[gist-box half-gist-box]

@gist[zoom-09](yuki-thewaggle/82bf9f1de5b6963bcb47f02e7b1c5d09)

@[1](説明)

@snapend
@snapend

@snapend


---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [3. Phoenix プロジェクトの作成](#/)
- [3. データベースの作成](#/)
@olend
@snapend

@snap[west headline]
## @color[white](データベースの作成)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [3. Phoenix プロジェクトの作成](#/)
- [3. データベースの作成](#/)
@olend
@snapend

### @css[slide-title](データベースの作成)

@snap[slide-contents]

@box[rounded box-style](データを保存するための機能を作成します。)

@snap[left-column]
@ol[numberlist numberlist-color4](false)
- mix ecto.create
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
- [3. Phoenix プロジェクトの作成](#/)
- [4. アプリケーションの起動](#/)
@olend
@snapend

@snap[west headline]
## @color[white](アプリケーションの起動)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [3. Phoenix プロジェクトの作成](#/)
- [4. アプリケーションの起動](#/)
@olend
@snapend

### @css[slide-title](アプリケーションの起動)

@snap[slide-contents]

@box[rounded box-style](サーバーを実行してアプリケーションを起動します。)

@snap[left-column]
@ol[numberlist numberlist-color4](false)
- mix phx.server
@olend
@snapend

@snap[right-column]
@snap[gist-box half-gist-box]

@gist[zoom-09](yuki-thewaggle/82bf9f1de5b6963bcb47f02e7b1c5d09)

@[1](説明)

@snapend
@snapend

@snapend

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [3. Phoenix プロジェクトの作成](#/)
- [5. Webサイトの確認](#/)
@olend
@snapend

@snap[west headline]
## @color[white](Webサイトの確認)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [3. Phoenix プロジェクトの作成](#/)
- [5. Webサイトの確認](#/)
@olend
@snapend

### @css[slide-title](Webサイトの確認)

@snap[slide-contents]

@box[rounded box-style](アプリケーションが起動して<br>Webサイトが見られるようになったことを確認します。)

@snap[left-column]
@ol[numberlist numberlist-color4](true)
- Firefox を立ち上げます。
- <span class="not-selectable">URLに</span><br><u>http://localhost:4000</u><br><span class="not-selectable">を貼り付けて開きます。</span>
- 画像のようなページが表示されます。
@olend
@snapend

@snap[right-column]
@snap[imagebox]
@img[](template/img/finish.png)
@snapend
@snapend

@snapend

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [3. Phoenix プロジェクトの作成](#/)
- [6. サーバーの終了](#/)
@olend
@snapend

@snap[west headline]
## @color[white](サーバーの終了)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [3. Phoenix プロジェクトの作成](#/)
- [6. サーバーの終了](#/)
@olend
@snapend

### @css[slide-title](サーバーの終了)

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
