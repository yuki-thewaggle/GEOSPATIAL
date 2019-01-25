# 構成

[A1] テンプレートA
[A2]
[B] テンプレートB
[C] テンプレートC
[D] テンプレートD
[E] テンプレートE
[F] テンプレートF
[G] テンプレートG
[H] テンプレートH

<a> : 索引からリンクで飛んでこれるようにする単語
<link> : <a>にリンクさせる単語

# 基礎知識	-	Webの仕組みやプログラミングに必要な知識を学ぶ
	## Webの仕組み
		https://developer.mozilla.org/ja/docs/Learn/Common_questions/Pages_sites_servers_and_search_engines
		https://developer.mozilla.org/ja/docs/Learn/Getting_started_with_the_web/How_the_Web_works
		* 説明１
		* 説明２
	## 用語解説
		<a>クライアント
		<a>Webブラウザ
		<a>サーバ
		<a>データベース
		<a>リクエストとレスポンス
		<a>インターネット接続
		<a>ウェブページ
			ウェブブラウザに表示可能なドキュメント
	## HTMLとは
		https://developer.mozilla.org/ja/docs/Web/HTML
		* HTML（HyperText Markup Language　- ハイパーテキスト マークアップ ランゲージ）
		* ウェブのもっとも基本的な構成要素
		* ウェブページの基本レイアウトに従ってウェブページのコンテンツを記述し定義するもの
	## 用語解説
		<a>HTML
		<a>ハイパーテキスト
			- ウェブページから別なページに接続するリンク
			- ウェブサイト内でもウェブサイト間でも
			- ウェブの基礎的な特徴
		<a>マークアップ
			- たくさんの特殊な「要素」を用いる
			- <a>タグを利用
				HTML のタグは、大文字と小文字の区別はありません。つまり、大文字でも、小文字でも、混在して書いても構いません。例えば、 <title> タグは <Title> や <TITLE> やその他の方法で書くことができます
	## CSSとは
		https://developer.mozilla.org/ja/docs/Web/CSS
		* 体裁や見栄えを表現するために用いられる
		<a>CSS
	## JavaScriptとは
		https://developer.mozilla.org/ja/docs/Web/JavaScript
		* プログラミング言語
		* Web ページでよく使用される
		* Webページに動作を付ける
		* 非ブラウザ環境においても多く使用されている
		<a>JavaScript
	## Elixirとは
		https://www.ossnews.jp/oss_info/Elixir
		https://ja.m.wikipedia.org/wiki/Elixir_(プログラミング言語)
		* プログラミング言語
		* 短く書ける
		* メンテナンスしやすい
		* １つのマシンで数十万の処理を並行して行える
			- 処理が早い
		* 予想通りに物事が進まなくなった場合の対応を思い通りに保証できる
	## 用語解説
		<a>Elixir
		<a>プログラミング言語
	## 型とは
		https://ja.m.wikipedia.org/wiki/データ型
		* データ（値）の種類に関する分類
			- 0, 1, 2, -42 といったような値は整数型
			- "foo", "Hello" といったような値は文字列型
		<a>型
	## Elixirの主な型
		https://elixirschool.com/ja/lessons/basics/basics/#%E3%82%A2%E3%83%88%E3%83%A0
		https://elixirschool.com/ja/lessons/basics/collections/#タプル
		* 整数 1
		* 整数(16進数) 0x1F
		* 小数 1.0
		* 論理値 true
		* アトム :atom
		* 文字列 "elixir"
		* リスト [1, 2, 3]
		* タプル {1, 2, 3}
		<a>Elixirの主な型
# 環境構築	-	地図アプリを作るために必要な設定をする
	## CUI
		## 概要
			* 作業の内容と目的
			* 起動方法
				- Windows
					* コマンドプロント
						起動方法
				- MacOS
					* ターミナル
					* 起動方法
		## CUIとは
			https://ja.m.wikipedia.org/wiki/キャラクタユーザインタフェース
			- ユーザインタフェース
				機械と人間との伝達を行うもの
			- 文字列が表示されるウィンドウに出力する
			- キーボード等から文字列を入力する
			<a>CUI
	1. Firefox
		##### ダウンロードとインストール
			* 作業の内容と目的
			* 手順
		## Firefoxとは
			<link>Webブラウザ
	1. RESTClient
		##### ダウンロードとインストール
			* 作業の内容と目的
			* 手順
	## RESTClientとは
	1. テキストエディタ
		##### ダウンロードとインストール
			* 作業の内容と目的
			* 手順
			お好みのものがあればそれをお使いください
			Visual Studio Codeをお薦めします
			※Windows
				$ cd フォルダ
				shell のパス設定いらない（インストール時に行う）
		## テキストエディタとは
	1. Elixir
		##### ダウンロードとインストール
			* 作業の内容と目的
		## Elixirとは
			<link>Elixirとは
		1. ダウンロードとインストール
	1. node.js
		##### ダウンロードとインストール
			* 作業の内容と目的
		## node.jsとは
		1. 
	1. PostgreSQL
		##### ダウンロードとインストール
			* 作業の内容と目的
		## PostgreSQLとは
		1. ダウンロードとインストール
	1. Phoenixframework
		##### ダウンロードとインストール
			* 作業の内容と目的
		## Phoenixframeworkとは
		1. ダウンロードとインストール
# APIServerの構築	-	地図アプリを提供するためのシステムを作る
	1. プロジェクトファイルの生成
		1. 概要
		1. 使用するソフトウェア
		1. 作業内容
	1. Webサーバの確認
		1. 概要
		1. 使用するソフトウェア
		1. 作業内容
	1. サーバの起動
		1. 概要
		1. 使用するソフトウェア
		1. 作業内容
	1. サーバの終了方法
		1. 概要
		1. 使用するソフトウェア
		1. 作業内容
	1. フォルダ移動
		1. 概要
		1. 使用するソフトウェア
		1. 作業内容
	1. DBの作成
		1. 概要
		1. 使用するソフトウェア
		1. 作業内容
	1. JSONデータの作成
		1. 概要
		1. 使用するソフトウェア
		1. 作業内容
	1. Router.exの設定
		1. 概要
		1. 使用するソフトウェア
		1. 作業内容
	1. マイグレーション
		1. 概要
		1. 使用するソフトウェア
		1. 作業内容
			- サーバの立ち上げ
			- ブラウザで確認
	1. RESTClient の設定
	1. RESTClientでGET
		1. 概要
		1. 使用するソフトウェア
		1. 作業内容
	1. RESTClientでPOST
		1. 概要
		1. 使用するソフトウェア
		1. 作業内容
# 地図の表示	-	まずは地図を表示してみる
	1. leaflet.js
		1. 概要
		1. 使用するソフトウェア
	1. Mapの設定
	1. leaflet.jsの仕様
	1. 表示の確認
# 外部API呼び出し	-	公開されている地図システムを利用する
	1. APIを扱うパッケージの追加
# DB操作	-	データ群を扱う
	1. DB操作の追加
# 内部API呼び出し	-	ツールを使って地図アプリを配信する
	1. Vue.jsとaxiosを使ってAPIを呼出す
	1. フレームワークとは
	1. CDNを使用する為のタグを追加する
	1. 表示
	1. 更新
	1. 削除
	1. 追加
# 地図へのポイント追加
	1. 繰り返し
# 自分の緯度経度の取得
	1. 現在地取得
	1. Terf.js CDN追加
	1. GeoJsonに入れる
# CSSデータを読み込む
# デプロイ					

---

#メモ
  - 今、何やっているか？の進捗が確認できる事 (作業に連番を降る)
  - 画面の上に出てる
  - 確認の仕方
  - Gistにコピペ用のソースを上げておいて、名前と番号を振り直し
  - これコピペして下さい。で進む。
  - 解説重視
  - G空間に利用できるオープンデータの一覧
  - G空間に役立ちそうなElixirの使えそうなライブラリの一覧
  - 技術選定・学習内容の編集：瑛佑　（映像）
  - ドキュメント編集長：松本
  - 調査・作業：多田

---

# Windowsメモ

### Phoenix v1.4 のインストール
- 管理者権限でコマンドプロンプトを起動する
- 入力するコマンドは同じ `mix archive.install hex phx_new 1.4.0`
```
C:\WINDOWS\system32>mix archive.install hex phx_new 1.4.0
Could not find Hex, which is needed to build dependency :phx_new
Shall I install Hex? (if running non-interactively, use "mix local.hex --force") [Yn] Y
1. creating c:/Users/yukim/.mix/archives/hex-0.19.0
Resolving Hex dependencies...
Dependency resolution completed:
New:
[32m  phx_new 1.4.0[0m
* Getting phx_new (Hex package)
All dependencies are up to date
Compiling 10 files (.ex)
Generated phx_new app
Generated archive "phx_new-1.4.0.ez" with MIX_ENV=prod
Are you sure you want to install "phx_new-1.4.0.ez"? [Yn] Y
* creating c:/Users/yukim/.mix/archives/phx_new-1.4.0
```
---

### Visual Studio Code の使い方
- 管理者権限で Visual Studio Code を起動する
- 入力するコマンドを `code .` から `code . -r` に変える
