---?color=#3A8FB7
@snap[breadcrumbs-wrap bluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [4. Elixir モジュールの追加](#/)
@olend
@snapend

@snap[west headline]
## Elixir モジュール<br>の追加
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [4. Elixir モジュールの追加](#/)
@olend
@snapend

### @css[slide-title](Elixir モジュールの追加)

@snap[slide-contents]

@box[rounded box-style](Phoenix を使ってWebプロジェクトを作成します。)

@snap[left-column]
@ol[numberlist numberlist-color2](false)
- [モジュールとは](#/)
- [Visual Studio Code の起動](#/)
- [モジュールの追加方法](#/)
- [mix.exs のオープン](#/)
- [smallex の追加](#/)
- [確認](#/)
@olend
@snapend

@snap[right-column]
@ol[numberlist numberlist-color2](false)
- [smallex の使い方](#/)
- [CUIで文字化けが起こるとき](#/)
@olend
@snapend

@snapend

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [4. Phoenix Elixir モジュールの追加](#/)
- [1. モジュールとは](#/)
@olend
@snapend

@snap[west headline]
## @color[white](モジュールとは)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [4. Phoenix Elixir モジュールの追加](#/)
- [1. モジュールとは](#/)
@olend
@snapend

### @css[slide-title](モジュールとは)

@snap[slide-contents]

@snap[quote-wrap]
@quote[<ul><li>システムの一部を構成するひとまとまりの<span class="orange">機能を持った部品</span><li>容易に追加や交換ができる</li></ul>](http://e-words.jp/w/モジュール.html)
@snapend

@snapend

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [4. Phoenix Elixir モジュールの追加](#/)
- [2. Visual Studio Code の起動](#/)
@olend
@snapend

@snap[west headline]
## @color[white](Visual Studio Code<br>の起動)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [4. Phoenix Elixir モジュールの追加](#/)
- [2. Visual Studio Code の起動](#/)
@olend
@snapend

### @css[slide-title](Visual Studio Code の起動)

@snap[slide-contents]

@box[rounded box-style](<span class="orange">CUI</span>を使って、<br>Visual Studio Codeを起動します。)

@snap[left-column]
@ol[numberlist numberlist-color4](false)
- code .
@olend
@snapend

@snap[right-column]
@snap[imagebox]
@img[](template/img/environment/postgresql.png)
@snapend
@snapend

@snapend

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [4. Phoenix Elixir モジュールの追加](#/)
- [3. モジュールの追加方法](#/)
@olend
@snapend

@snap[west headline]
## @color[white](モジュールの<br>追加方法)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [4. Phoenix Elixir モジュールの追加](#/)
- [3. モジュールの追加方法](#/)
@olend
@snapend

### @css[slide-title](モジュールの追加方法)

@snap[slide-contents]

@box[rounded box-style](<span class="orange">Visual Studio Code</span>を使って、<br>mix.exs ファイルを編集してモジュールを追加します。)

@ol[numberlist numberlist-color4](false)
- mix.exs という名前のファイルを編集して、<br>追加のモジュールを書き込んでいきます。
- Elixir でモジュールを管理するためには、<br><u>[hex](https://hex.pm/)</u> という<u>[パッケージマネージャー](https://www.weblio.jp/content/パッケージ管理システム)</u>を利用します。
@olend
@snapend

@snapend

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [4. Phoenix Elixir モジュールの追加](#/)
- [4. mix.exs のオープン](#/)
@olend
@snapend

@snap[west headline]
## @color[white](mix.exs のオープン)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [4. Phoenix Elixir モジュールの追加](#/)
- [4. mix.exs のオープン](#/)
@olend
@snapend

### @css[slide-title](mix.exs のオープン)

@snap[slide-contents]

@box[rounded box-style](<span class="orange">Visual Studio Code</span>を使って、<br>mix.exs というファイルを開きます。)

@ol[numberlist numberlist-color4](false)
- 画面上部のメニューから「<span class="orange">View</span>」 > 「<span class="orange">Explorer</span>」 をクリックします。
- 画面の左側に「<span class="orange">EXPLORER</span>」という枠が開きます。
- 「EXPLORER」から「<span class="orange">deps</span>」> 「<span class="orange">phoenix</span>」>「<span class="orange">mix.exs</span>」を捜してクリックします。
@olend

@snapend

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [4. Phoenix Elixir モジュールの追加](#/)
- [5. smallex の追加](#/)
@olend
@snapend

@snap[west headline]
## @color[white](smallex の追加)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [4. Phoenix Elixir モジュールの追加](#/)
- [5. smallex の追加](#/)
@olend
@snapend

### @css[slide-title](smallex の追加)

@snap[slide-contents]

@box[rounded box-style](<span class="orange">Visual Studio Code</span>を使って、<br>smallex というAPIを取得するのに便利なモジュールを実際に追加します。)

@snap[left-column]
@ol[numberlist numberlist-color4](false)
- {:smallex, "~> 0.2.3"},
@olend
@snapend

@snap[right-column]
@snap[gist-box half-gist-box]

@gist[zoom-09](yuki-thewaggle/82bf9f1de5b6963bcb47f02e7b1c5d09)

@[1-5](（defp deps doのブロックをハイライト）この区分の中に加筆します。)
@[2](この行に `{:smallex, "~> 0.2.3"},` と記入します。)

@snapend
@snapend

@snapend

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [4. Phoenix Elixir モジュールの追加](#/)
- [6. 確認](#/)
@olend
@snapend

@snap[west headline]
## @color[white](確認)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [4. Phoenix Elixir モジュールの追加](#/)
- [6. 確認](#/)
@olend
@snapend

### @css[slide-title](確認)

@snap[slide-contents]

@box[rounded box-style](<span class="orange">CUI</span>を使って、<br>smallexがインストールされていることを確認します。Windowsでの確認方法を確立する！！！)

@snap[left-column]
@ol[numberlist numberlist-color4](false)
- mix deps.get
@olend
@snapend

@snap[right-column]
@snap[gist-box half-gist-box]

@gist[zoom-09](yuki-thewaggle/6225d47bfe950aa8255afb72b2a26718)

@[1](説明)
@[2](説明)

@snapend
@snapend

@snapend

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [4. Phoenix Elixir モジュールの追加](#/)
- [7. smallex の使い方](#/)
@olend
@snapend

@snap[west headline]
## @color[white](smallex の使い方)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [4. Phoenix Elixir モジュールの追加](#/)
- [7. smallex の使い方](#/)
@olend
@snapend

### @css[slide-title](smallex の使い方)

@snap[slide-contents]

@snap[quote-wrap]
@quote[<ul><li>Json.get（ドメイン, パス）</li><ul><li>Json.get（"https://api.github.com", "/rate_limit" ）</li><li>https://api.github.com/rate_limit のJSON APIを取得</li></ul></li></ul>](https://hexdocs.pm/smallex/Json.html#get/3)
@snapend

@snap[left-column]
@ol[numberlist numberlist-color4](false)
- result = Json.get("https://aed.azure-mobile.net","/api/NearAED?lat=35.96&lng=136.185")
@olend
@snapend

@snap[right-column]
@snap[gist-box half-gist-box]

@gist[zoom-09](yuki-thewaggle/82bf9f1de5b6963bcb47f02e7b1c5d09)

@[1-5](（説明します。)

@snapend
@snapend

@snapend

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [4. Phoenix Elixir モジュールの追加](#/)
- [8. CUIで文字化けが起こるとき](#/)
@olend
@snapend

@snap[west headline]
## @color[white](CUIで文字化けが起こるとき)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [4. Phoenix Elixir モジュールの追加](#/)
- [8. CUIで文字化けが起こるとき](#/)
@olend
@snapend

### @css[slide-title](CUIで文字化けが起こるとき)

@snap[slide-contents]

@box[rounded box-style](Windowsの場合、文字が別の文字で表示されてしまうときは、以下のコマンドを入力してください。)

@snap[left-column]
@ol[numberlist numberlist-color4](false)
- chcp 65001
@olend
@snapend

@snap[right-column]
@snap[gist-box half-gist-box]

@gist[zoom-09](yuki-thewaggle/82bf9f1de5b6963bcb47f02e7b1c5d09)

@[1-5](（説明します。)

@snapend
@snapend

@snapend