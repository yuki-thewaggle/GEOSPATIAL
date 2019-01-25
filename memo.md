# 構成

[A1] テンプレートA1
[A2] テンプレートA2
[B] テンプレートB
[C] テンプレートC
[D] テンプレートD
[E] テンプレートE
[F] テンプレートF
[G] テンプレートG
[H] テンプレートH

<a> : 索引からリンクで飛んでこれるようにする単語
<link> : <a>にリンクさせる単語

[A1]基礎知識	-	Webの仕組みやプログラミングに必要な知識を学ぶ
	[B]Webの仕組み
		https://developer.mozilla.org/ja/docs/Learn/Common_questions/Pages_sites_servers_and_search_engines
		https://developer.mozilla.org/ja/docs/Learn/Getting_started_with_the_web/How_the_Web_works
		* 説明１
		* 説明２
	[B]用語解説
		<a>クライアント
		<a>Webブラウザ
		<a>サーバ
		<a>データベース
		<a>リクエストとレスポンス
		<a>インターネット接続
		<a>ウェブページ
			ウェブブラウザに表示可能なドキュメント
	[B]HTMLとは
		https://developer.mozilla.org/ja/docs/Web/HTML
		* HTML（HyperText Markup Language　- ハイパーテキスト マークアップ ランゲージ）
		* ウェブのもっとも基本的な構成要素
		* ウェブページの基本レイアウトに従ってウェブページのコンテンツを記述し定義するもの
	[B]用語解説
		<a>HTML
		<a>ハイパーテキスト
			- ウェブページから別なページに接続するリンク
			- ウェブサイト内でもウェブサイト間でも
			- ウェブの基礎的な特徴
		<a>マークアップ
			- たくさんの特殊な「要素」を用いる
			- <a>タグを利用
				HTML のタグは、大文字と小文字の区別はありません。つまり、大文字でも、小文字でも、混在して書いても構いません。例えば、 <title> タグは <Title> や <TITLE> やその他の方法で書くことができます
	[B]CSSとは
		https://developer.mozilla.org/ja/docs/Web/CSS
		* 体裁や見栄えを表現するために用いられる
		<a>CSS
	[B]JavaScriptとは
		https://developer.mozilla.org/ja/docs/Web/JavaScript
		* プログラミング言語
		* Web ページでよく使用される
		* Webページに動作を付ける
		* 非ブラウザ環境においても多く使用されている
		<a>JavaScript
	[B]Elixirとは
		https://www.ossnews.jp/oss_info/Elixir
		https://ja.m.wikipedia.org/wiki/Elixir_(プログラミング言語)
		* プログラミング言語
		* 短く書ける
		* メンテナンスしやすい
		* １つのマシンで数十万の処理を並行して行える
			- 処理が早い
		* 予想通りに物事が進まなくなった場合の対応を思い通りに保証できる
	[B]用語解説
		<a>Elixir
		<a>プログラミング言語
	[B]型とは
		https://ja.m.wikipedia.org/wiki/データ型
		* データ（値）の種類に関する分類
			- 0, 1, 2, -42 といったような値は整数型
			- "foo", "Hello" といったような値は文字列型
		<a>型
	[B]Elixirの主な型
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
[A1]環境構築	-	地図アプリを作るために必要な設定をする
	[A2]CUI
		* 作業の内容と目的
		* 起動方法
			[D] Windows
				* コマンドプロント
					起動方法
			[D] MacOS
				* ターミナル
				* 起動方法
	[B]CUIとは
		https://ja.m.wikipedia.org/wiki/キャラクタユーザインタフェース
		* ユーザインタフェース
			機械と人間との伝達を行うもの
		* 文字列が表示されるウィンドウに出力する
		* キーボード等から文字列を入力する
		<a>CUI
	[G]確認
	[A2]Firefox
		* 作業の内容と目的
		* 手順
			[D]
			[D]
			[D]
	[B]Firefoxとは
		* 説明
		<link>Webブラウザ
	[G]確認
	[A2]RESTClient
		* 作業の内容と目的
		* 手順
			[D]
			[D]
			[D]
	[B]RESTClientとは
	[G]確認
	[A2]テキストエディタ
		* 作業の内容と目的
			お好みのものがあればそれをお使いください
			Visual Studio Codeをお薦めします
			※Windows
				$ cd フォルダ
				shell のパス設定いらない（インストール時に行う）
		* 手順
			[D]
			[D]
			[D]
	[B]テキストエディタとは
	[G]確認
	[A2]Elixir
		* 作業の内容と目的
			<link>Elixirとは
		* 手順
			[D]
			[D]
			[D]
	[G]確認
	[A2]node.js
		* 作業の内容と目的
		* 手順
			[D]
			[D]
			[D]
	[B]node.jsとは
	[G]確認
	[A2]PostgreSQL
		* 作業の内容と目的
		* 手順
			[D]
			[D]
			[D]
	[B]PostgreSQLとは
	[G]確認
	[A2]Phoenixframework
		* 作業の内容と目的
		* 手順
			[D]
			[D]
			[D]
	[B]Phoenixframeworkとは
	[G]確認
[A1]APIServerの構築	-	地図アプリを提供するためのシステムを作る
	[A2]プロジェクトファイルの生成
		* 作業の内容と目的
			- 使用するソフトウェア
		* 手順
			[D]
			[D]
			[D]
	[A2]Webサーバの確認
		* 作業の内容と目的
			- 使用するソフトウェア
		* 手順
			[D]
			[D]
			[D]
	[A2]サーバの起動
		* 作業の内容と目的
			- 使用するソフトウェア
		* 手順
			[D]
			[D]
			[D]
	[A2]サーバの終了方法
		* 作業の内容と目的
			- 使用するソフトウェア
		* 手順
			[D]
			[D]
			[D]
	[A2]フォルダ移動
		* 作業の内容と目的
			- 使用するソフトウェア
		[A2]作業内容
	[A2]DBの作成
		* 作業の内容と目的
			- 使用するソフトウェア
		* 手順
			[D]
			[D]
			[D]
	[A2]JSONデータの作成
		* 作業の内容と目的
			- 使用するソフトウェア
		* 手順
			[D]
			[D]
			[D]
	[A2]Router.exの設定
		* 作業の内容と目的
			- 使用するソフトウェア
		* 手順
			[D]
			[D]
			[D]
	[A2]マイグレーション
		* 作業の内容と目的
			- 使用するソフトウェア
		* 手順
			[D]
			[D]サーバの立ち上げ
			[D]ブラウザで確認
	[A2]RESTClient の設定
	[A2]RESTClientでGET
		* 作業の内容と目的
			- 使用するソフトウェア
		* 手順
			[D]
			[D]
			[D]
	1. RESTClientでPOST
		* 作業の内容と目的
			- 使用するソフトウェア
		* 手順
			[D]
			[D]
			[D]
[A1]地図の表示	-	まずは地図を表示してみる
	[A2]leaflet.js
		* 作業の内容と目的
		* 手順
			[D]
			[D]
			[D]
	[A2]Mapの設定
		* 作業の内容と目的
		* 手順
			[D]
			[D]
			[D]
	[B]leaflet.jsの仕様
	[F]表示の確認
	[G]確認
[A1]外部API呼び出し	-	公開されている地図システムを利用する
	[A2]APIを扱うパッケージの追加
[A1]DB操作	-	データ群を扱う
	[A2]DB操作の追加
[A1]内部API呼び出し	-	ツールを使って地図アプリを配信する
	[A2]Vue.jsとaxiosを使ってAPIを呼出す
	[B]フレームワークとは
	[A2]CDNを使用する為のタグを追加する
	[A2]表示
	[A2]更新
	[A2]削除
	[A2]追加
[A1]地図へのポイント追加
	[A2]繰り返し
[A1]自分の緯度経度の取得
	[A2]現在地取得
	[A2]Terf.js CDN追加
	[A2]GeoJsonに入れる
[A1]CSSデータを読み込む
[A1]デプロイ					

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
