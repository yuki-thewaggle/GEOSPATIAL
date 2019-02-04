---?color=#3A8FB7
@snap[breadcrumbs-wrap bluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [0. 環境構築](#/)
@olend
@snapend

@snap[west headline]
## 環境構築
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [0. 環境構築](#/)
@olend
@snapend

### @css[slide-title](環境構築)

@snap[slide-contents]

@box[rounded box-style](地図アプリを作るために必要なPCの設定をします。)

@snap[left-column]
@ol[numberlist numberlist-color2](false)
- CUI
- Firefox
- RESTClient
- テキストエディタ
- Elixir
- node.js
@olend
@snapend


@snap[right-column]
@ol[numberlist numberlist-color2 start-7](false)
- PostgreSQL
- Phoenixframework
- リンクつけるのを忘れない
@olend
@snapend

@snapend

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [0. 環境構築](#/)
- [1. CUI](#/20)
@olend
@snapend

@snap[west headline]
## @color[white](CUI)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [0. 環境構築](#/)
- [1. CUI](#/20)
@olend
@snapend

### @css[slide-title](CUI)

@snap[slide-contents]
@img[goal-image to-center](template/img/environment/postgresql.png)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [0. 環境構築](#/)
- [1. CUI](#/20)
- [0. CUIの起動](#/20)
@olend
@snapend

### @css[slide-title](CUIの起動)

@snap[slide-contents]

@box[rounded box-style](CUIの起動方法を確認します。)

@ol[numberlist numberlist-color4](false)
- CUIとは
- 起動方法（Windowsの場合）
- 起動方法（Macの場合）
- 確認
- リンクつけるのを忘れない
@olend

@snapend

---

@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [0. 環境構築](#/)
- [1. CUI](#/20)
- [0. CUIとは]()
@olend
@snapend

### @css[slide-title](CUIとは)

@snap[slide-contents]

@snap[quote-wrap]
@quote[<ul><li>**C**haracter **U**ser **I**nterface（キャラクタユーザインタフェース）</li><li><a href="#/">**ユーザインタフェース**</a>の様式</li><li>キーボード等からの文字列を<a href="#/">**入力**</a>とする</li><li>文字列が表示されるウィンドウを<a href="#/">**出力**</a>とする</li></ul>](https://ja.wikipedia.org/wiki/キャラクタユーザインタフェース)
@snapend

- Macは「**ターミナル**」
- Windowsは「**コマンドプロンプト**」

@snapend

---

@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [0. 環境構築](#/)
- [1. CUI](#/20)
- [0. ユーザインタフェースとは]()
@olend
@snapend

### @css[slide-title](ユーザインタフェースとは)

@snap[slide-contents]
@snap[quote-wrap]

@quote[<ul><li>コンピュータと人間の間での情報をやりとりする</li><li>ユーザインタフェースは以下の手段を提供する<ul><li>**入力**：<br>ユーザーがシステムを操作する手段</li><li>**出力**：<br>ユーザーが操作した結果システムが生成したものを提示する手段</li></ul></li></ul>](https://ja.wikipedia.org/wiki/ユーザインタフェース)

@snapend
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [0. 環境構築](#/)
- [1. CUI](#/20)
- [k. 起動方法（Windowsの場合）]()
@olend
@snapend

### @css[slide-title](起動方法（Windowsの場合）)

@snap[slide-contents]

@snap[left-column]
@ol[numberlist numberlist-color4](true)
- <span class="not-selectable">検索ボックスに<br>「</span>**コマンドプロンプト**<span class="not-selectable">」<br>と記入します。</span>
- 「**コマンドプロンプト<br>デスクトップアプリ**」<br>をクリックします。
- コマンドプロンプトが起動します。
@olend
@snapend

@snap[right-column]
@img[goal-image to-center](template/img/environment/CUI-windows.png)
@snapend

@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [0. 環境構築](#/)
- [1. CUI](#/20)
- [k. 起動方法（Macの場合）]()
@olend
@snapend

### @css[slide-title](起動方法（Macの場合）)

@snap[slide-contents]

@snap[left-column]
@ol[numberlist numberlist-color4](true)
- 画面端にあるメニューバー <u>**[Dock](https://support.apple.com/ja-jp/guide/mac-help/mh35859/mac)**</u> から <u>**[Launchpad](https://support.apple.com/ja-jp/HT202635)**</u>をクリックします。
- <span class="not-selectable">検索ボックスに「</span> **ターミナル** <span class="not-selectable">」と入力して検索します。</span>
- **ターミナル** をクリックします。
- ターミナルが起動します。
@olend
@snapend

@snap[right-column]
@img[goal-image to-center](template/img/environment/CUI-terminal.png)
@snapend
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [0. 環境構築](#/)
- [1. CUI](#/20)
- [k. 確認]()
@olend
@snapend

### @css[slide-title](確認)

@snap[slide-contents]

@snap[left-column]
@ul[itemlist](false)
- このように、CUIが起動したことを確認します。
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
- [0. 環境構築](#/)
- [m. Firefox]()
@olend
@snapend

@snap[west headline]
## @color[white](Firefox)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [0. 環境構築](#/)
- [m. Firefox]()
- [k. Firefox]()
@olend
@snapend

### @css[slide-title](Firefox)

@snap[slide-contents]
@img[goal-image to-center](template/img/environment/Firefox.png)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [0. 環境構築](#/)
- [m. Firefox]()
- [k. Firefoxのインストール]()
@olend
@snapend

### @css[slide-title](Firefoxのインストール)

@snap[slide-contents]

@box[rounded box-style](Firefoxは、高速かつ軽量なWebブラウザーです。<br>拡張機能が豊富であるという特徴があります。)

@ol[numberlist numberlist-color4](true)
- <u>[Firefoxのダウンロードページ](https://www.mozilla.org/ja/firefox/new/)</u>にアクセスします。
- 「**今すぐダウンロード**」ボタンをクリックします。
- ダウンロードしたファイルをクリックして起動します。
- Windowsの場合、インストールを許可します。
- Macの場合、アイコンをフォルダにドラッグします。
- インストールされます。
@olend

@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [0. 環境構築](#/)
- [m. Firefox]()
- [k. 確認]()
@olend
@snapend

### @css[slide-title](確認)

@snap[slide-contents]

@snap[left-column]
@ul[itemlist](false)
- PC上に<br>Firefox のアイコンがある
- アイコンから<br>Firefox が起動する
- Firefox で<br>Webサイトなどが閲覧できる
@ulend
@snapend

@snap[right-column]
@snap[imagebox]
@img[](template/img/environment/Firefox-installed_windows.png)
@snapend
@snapend

@snapend

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [0. 環境構築](#/)
- [m. RESTClient]()
@olend
@snapend

@snap[west headline]
## @color[white](RESTClient)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [0. 環境構築](#/)
- [m. RESTClient]()
- [k. RESTClient]()
@olend
@snapend

### @css[slide-title](RESTClient)

@snap[slide-contents]
@img[goal-image to-center](template/img/environment/postgresql.png)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [0. 環境構築](#/)
- [m. RESTClient]()
- [k. RESTClientのインストール]()
@olend
@snapend

### @css[slide-title](RESTClientのインストール)

@snap[slide-contents]

@box[rounded box-style](何をするものか)

@snap[left-column]
@ol[numberlist numberlist-color4](true)
- 手順
- 手順
- 手順
- 手順
- 手順
- 手順
@olend
@snapend


@snap[right-column]
@ol[numberlist numberlist-color4 start-6](true)
- 手順
- 手順
- 手順
- 手順
- 手順
- 手順
@olend
@snapend

@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [0. 環境構築](#/)
- [m. RESTClient]()
- [k. 確認]()
@olend
@snapend

### @css[slide-title](確認)


---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [0. 環境構築](#/)
- [m. テキストエディタ]()
@olend
@snapend

@snap[west headline]
## @color[white](テキストエディタ)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [0. 環境構築](#/)
- [m. テキストエディタ]()
- [k. テキストエディタ]()
@olend
@snapend

### @css[slide-title](テキストエディタ)

@snap[slide-contents]
@img[goal-image to-center](template/img/environment/postgresql.png)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [0. 環境構築](#/)
- [m. テキストエディタ]()
- [k. テキストエディタのインストール]()
@olend
@snapend

### @css[slide-title](テキストエディタのインストール)

@snap[slide-contents]

@box[rounded box-style](中項目用の、テンプレートです。<br>項目の概要を、説明します。)

@snap[left-column]
@ol[numberlist numberlist-color4](true)
- アジェンダ項目内の小項目
- 小項目
- 小項目
- 小項目
- 体言止め
- a
@olend
@snapend


@snap[right-column]
@ol[numberlist numberlist-color4 start-6](true)
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
- [0. 環境構築](#/)
- [m. テキストエディタ]()
- [k. 確認]()
@olend
@snapend

### @css[slide-title](確認)

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [0. 環境構築](#/)
- [m. Elixir]()
@olend
@snapend

### @css[slide-title](Elixir)

@snap[slide-contents]
@img[goal-image to-center](template/img/environment/postgresql.png)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [0. 環境構築](#/)
- [m. Elixir]()
- [k. Elixirのインストール]()
@olend
@snapend

### @css[slide-title](Elixirのインストール)

@snap[slide-contents]

@box[rounded box-style](中項目用の、テンプレートです。<br>項目の概要を、説明します。)

@snap[left-column]
@ol[numberlist numberlist-color4](true)
- アジェンダ項目内の小項目
- 小項目
- 小項目
- 小項目
- 体言止め
@olend
@snapend

@snap[right-column]
@ol[numberlist numberlist-color4 start-6](true)
- アジェンダ項目内の小項目
- 小項目
- 小項目
- 小項目
- 体言止め
- ここまで
@olend
@snapend

@snapend
---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [0. 環境構築](#/)
- [m. node.js]()
@olend
@snapend

@snap[west headline]
## @color[white](node.js)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [0. 環境構築](#/)
- [m. node.js]()
- [k. node.js]()
@olend
@snapend

### @css[slide-title](node.js)

@snap[slide-contents]
@img[goal-image to-center](template/img/environment/postgresql.png)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [0. 環境構築](#/)
- [m. node.js]()
- [k. node.jsのインストール]()
@olend
@snapend

### @css[slide-title](node.jsのインストール)

@snap[slide-contents]

@box[rounded box-style](中項目用の、テンプレートです。<br>項目の概要を、説明します。)

@snap[left-column]
@ol[numberlist numberlist-color4](true)
- アジェンダ項目内の小項目
- 小項目
- 小項目
- 小項目
- 体言止め
- a
@olend
@snapend


@snap[right-column]
@ol[numberlist numberlist-color4 start-6](true)
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
- [0. 環境構築](#/)
- [m. node.js]()
- [k. 確認]()
@olend
@snapend

### @css[slide-title](確認)

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [0. 環境構築](#/)
- [m. PostgreSQL]()
@olend
@snapend

@snap[west headline]
## @color[white](PostgreSQL)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [0. 環境構築](#/)
- [m. PostgreSQL]()
- [k. PostgreSQL]()
@olend
@snapend

### @css[slide-title](PostgreSQL)

@snap[slide-contents]
@img[goal-image to-center](template/img/environment/postgresql.png)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [0. 環境構築](#/)
- [m. PostgreSQL]()
- [k. PostgreSQLのインストール]()
@olend
@snapend

### @css[slide-title](PostgreSQLのインストール)

@snap[slide-contents]

@box[rounded box-style](中項目用の、テンプレートです。<br>項目の概要を、説明します。)

@snap[left-column]
@ol[numberlist numberlist-color4](true)
- アジェンダ項目内の小項目
- 小項目
- 小項目
- 小項目
- 体言止め
- a
@olend
@snapend


@snap[right-column]
@ol[numberlist numberlist-color4 start-6](true)
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
- [0. 環境構築](#/)
- [m. PostgreSQL]()
- [k. 確認]()
@olend
@snapend

### @css[slide-title](確認)

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [0. 環境構築](#/)
- [m. Phoenixframework]()
@olend
@snapend

@snap[west headline]
## @color[white](Phoenixframework)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [0. 環境構築](#/)
- [m. Phoenixframework]()
- [k. Phoenixframework]()
@olend
@snapend

### @css[slide-title](Phoenixframework)

@snap[slide-contents]
@img[goal-image to-center](template/img/environment/postgresql.png)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [0. 環境構築](#/)
- [m. Phoenixframework]()
- [k. Phoenixframeworkのインストール]()
@olend
@snapend

### @css[slide-title](Phoenixframeworkのインストール)

@snap[slide-contents]

@box[rounded box-style](中項目用の、テンプレートです。<br>項目の概要を、説明します。)

@snap[left-column]
@ol[numberlist numberlist-color4](true)
- アジェンダ項目内の小項目
- 小項目
- 小項目
- 小項目
- 体言止め
@olend
@snapend

@snap[right-column]
@ol[numberlist numberlist-color4 start-6](true)
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
- [0. 環境構築](#/)
- [m. Phoenixframework]()
- [k. 確認]()
@olend
@snapend

### @css[slide-title](確認)










---?color=#F39F39
# @css[headline](環境構築)

---
@snap[midopoint north-west text-06]
### インストール
@snapend

1. firefox & RESTClient
2. テキストエディタ
3. Elixir
4. node.js
5. PostgreSQL
6. Phoenixframework

---
@snap[north-west text-06]
### Rest APIクライアントの準備
@snapend

@snap[midopoint text-05]
今回は、[Firefox](https://www.mozilla.org/ja/firefox/new/?utm_campaign=non-fx-button&utm_content=rta%3Ae2FkMGQ5MjVkLTg4ZjgtNDdmMS04NWVhLTg0NjM1NjllNzU2ZX0&utm_medium=referral&utm_source=addons.mozilla.org)「[RESTClient](https://addons.mozilla.org/ja/firefox/addon/restclient/)」を利用します。

ダウンロードしてインストールしください。
@img[span-70](template/img/environment/RESTClient-add.png)
@snapend
---
@snap[north-west text-06]
### エディタのインストール
@snapend

@snap[midopoint text-05]
テキストエディタ、普段ご利用のものをお使いください。<br>

入ってない方は、この講座では以下を利用しています。<br>

[VSCODE](https://code.visualstudio.com/)<br/>

@img[span-70](template/img/environment/vscode.png)

@snapend

---
@snap[north-west text-06]
### vscode-elixirの追加
@snapend

@snap[midopoint text-05]
VSCODEにElixirのアドインを追加します。

[MarketplaceよりElixirのアドイン追加](https://marketplace.visualstudio.com/items?itemName=mjmcloug.vscode-elixir) 

@img[span-70](template/img/environment/vscode-elixir.png)
@snapend

---
@snap[north-west text-06]
### ターミナルからエディタを起動するための準備
@snapend

@snap[midopoint text-05]
VSCODEを開いた状態で

Command + Shift + P で検索窓を開きます。

@img[span-70](template/img/environment/vscode-adin.png)
@snapend
---
@snap[north-west text-06]
### Shell Command install
@snapend

@snap[text-05]
「Shell Command: install 'code' command in PATH」を選択します。
@img[span-90](template/img/environment/vscode-shell.png)
@snapend

---
@snap[north-west text-06]
### ターミナル
@snapend

@snap[text-05]
ターミナルとは:コマンドベースの入力インターフェイス(略称：CUI）<br>
WindowsとMacでは利用するアプリ名と、利用するコマンドも若干異なります。<br>
* Windows->コマンドプロンプト
* Mac->ターミナル
@img[span-60](template/img/environment/terminal.png)
@snapend

---?color=#000000
@snap[north-west text-06 text-white]
### ターミナルの使い方
@snapend


@snap[midpoint text-06]

現在のディレクトリ内にある内容の確認

@gist[terminal](Yoosuke/ef45e8a06367c20cff7b4a46714fbd12)

@snapend

---?color=#000000

@snap[north-west text-06 text-white]
### ターミナルからエディタを起動する方法
@snapend

@snap[midpoint]
VSCODEが起動すればOK<br><br>

@gist[zoom-10](Yoosuke/6d2cfefcc23d71cf0911074a99787e88)

@[2](VScodeを立ち上げる)

@snapend


---
@snap[north-west text-06]
### Elixirのインストール
@snapend

@snap[text-05]
今回は、Elixirという言語を利用しますので

お使いの環境に合わせて、インストールしてください。<br>
elixirに必要なパッケージ類も一緒にインストールされます。

@img[span-60](template/img/environment/elixir-hp.png)<br>
[Elixir インストール](https://elixir-lang.org/install.html)

@snapend
---
@snap[north-west text-06]
### HomeBrewのインストール
@snapend

@snap[midpint text-07]
homebrewを使用すると便利です。<br>
@img[span-60](template/img/environment/elixir-install-mac.png)<br>
[homebrewのインストール方法](https://brew.sh/index_ja)

@snapend

---?color=#000000
@snap[north-west text-06]
### Elixirのインストール for Mac
@snapend

@snap[midpoint]

@gist[elixir zoom-10](Yoosuke/0abcd22f59dc8cc7c0db4509aa358253)


@[1](HomebrewのUpdateをします)
@[2](Elixirをインストールします)

@snapend
---
@snap[north-west text-06]
### Elixirのインストール for Windows
@snapend

@snap[midpoint text-06]
@img[span-90](template/img/environment/elixir-install-win.png)<br>

[Elixirのインストール方法](https://elixir-lang.org/install.html)<br>
 Windowsの「Download the installer」よりインストール。
@snapend
---
@snap[north-west text-06]
### node.jsのインストール
@snapend

@snap[text-05]
@img[span-70](template/img/environment/nodejs.png)<br>

[nodejs ダウンロード](https://nodejs.org/en/download/)
@snapend

---
@snap[north-west text-06]
### PostgreSQLのインストール
@snapend

@snap[text-05]
今回は、version 11.1 をダウンロードします。<br>
* パスワードはpostgresを設定します。<br>
[PostgreSQL インストール](https://www.enterprisedb.com/downloads/postgres-postgresql-downloads)<br>
@img[span-60](template/img/environment/postgresql.png)
@snapend
---
@snap[north-west text-06]
### Phoenixframeworkのインストール
@snapend

@snap[text-05]
Webのフレームワークとして、Phoenixを利用します<br>
[Phoenix](https://hexdocs.pm/phoenix/installation.html)<br/>
@img[span-70](template/img/environment/phoenix.png)

@snapend

---?color=#000000
@snap[north-west text-06 text-white]
### Phoenix v1.4のインストール
@snapend

@gist[elixir midpoint zoom-16](Yoosuke/02ec19b92d74e666fd6e47e7095dfd9c)

@snap[south text-04]
ターミナルからコマンドを入力してインストールします。
@snapend

---?color=#000000
@snap[north-west text-06 text-white]
### Phoenix プロジェクトの作成
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



