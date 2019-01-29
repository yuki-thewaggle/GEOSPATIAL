1. Phoenix プロジェクトの作成
	1. プロジェクトの作成
            - mix phx.new aedmap
            - Y
	1. データベースの作成
            - cd aedmap
            - mix ecto.create
	1. サーバーの起動
            - mix phx.server
	1. Webサイトの確認
            - ブラウザで http://localhost:4000 を確認
	1. サーバーの終了
            - Ctr + C を２回でサーバーをシャットダウン
1. Elixir モジュールの追加
	1. モジュールとは
	1. Visual Studio Code の起動
            - ターミナル上で、 code . でVscodeを起動する
	1. モジュールの追加方法
            - mix.exs ファイルを開いて、 defp deps do の中に 追加のモジュールを書き込むと案内する
            - 追加のモジュールについては、Elixirは hex というパッケージマネージャを利用する
	1. smallex の追加
            - hex から　smallex　という　APIを取得するのに便利なモジュールを追加
            - {:smallex, "~> 0.2.3"}, を defp deps do の中に追加して、保存する
	1. 確認
            - コンソール画面で、 mix deps.get をして、smallexがインストールされている事をコンソールに出力される結果から確認する
	1. smallex の使い方
            - hex の smallex　から、Online documentation のリンク先に飛んで、Json.getの使い方を説明
1. プロジェクトのテスト方法
	1. Elixir のテスト
            - iex -S mix phx.severでサーバーを立ち上げると、iexが起動しているのでコンソール上で、Elixirをテストできるようになる
			https://elixirschool.com/ja/lessons/basics/iex-helpers/
1. APIの利用
	1. APIとは
	1. AEDオープンデータプラットフォーム
            - APIは、今回はAEDオープンデータプラットフォームのAPIを利用する。http://hatsunejournal.jp/w8/AEDOpendata/
	1. 直近AED位置情報取得API
            - 直近AED位置情報取得API　を利用する、例に乗っているURLをhttps://aed.azure-mobile.net/api/NearAED?lat=35.96&lng=136.185
	1. 確認
            - 利用するとデータが取得できる事を確認する。
1. RestClient の操作
	1. RestClient での確認
            - Firefoxのブラウザから、RestClientを起動し、URLに　https://aed.azure-mobile.net/api/NearAED?lat=35.96&lng=136.185
			を入力する
            - MethodはGetで、send すると、 ステータスコード　200 OKで JSONデータが取得されている事を確認する
			- 無事に確認が取れたら、このような機能をElixirに実装していくと説明する
1. 外部データの取得と抽出
	1. 外部データの取得
            - まず、コンソール上で、Json.get("https://aed.azure-mobile.net", "/api/NearAED?lat=35.96&lng=136.185")をするとデータが取得できる事を確認する。
	1. Elixir の特徴
            - Elixirには、整数、浮動小数、真理値、atom、文字列、リスト、タプル、キーワードリスト、マップという書き方がある
            - 256 132.1123 true, false, :atom, "Hello", [1,:ok,"text"], {:ok, "text"}, [foo: "hello", bar: "world"], %{key = "value"}
            - それぞれの形の詳しい説明は、ここに乗っています。https://elixir-lang.org/getting-started/basic-types.html
	1. 取得したデータの抽出（%{ } マップ型のデータ）
            - 先ほど、取得したデータを見てみると、 [ %{ dataの中身 } ] という形です。 []リストの中に %{} マップ型のデータ構造が入っています。
            - これを取得しやすくする為に、Map型のデータ構造だけ抜き取りたいと思います。
            - ここで、Elixirの特徴として、=は代入演算子では無く、　＝　はパターンマッチング　です。それを利用して、
            - マップ型のデータだけを抜き出して見ます。
            - [ result ] = Json.get("https://aed.azure-mobile.net", "/api/NearAED?lat=35.96&lng=136.185")
            - これで、result　の中は、%{ } マップ型のデータのみが束縛されています。
            - result　の中は、%{ ... "Latitude" => 35.959898 ... } のような形になっています。
	1. 取得したデータの抽出（"Latitude" のデータ）
            - ここから、Map.getを利用して、"Latitude" のデータを取得したいと思います。
            - latitude = Map.get( result, "Latitude" )
            - これで、latitudeには、35.959898　のデータが取得できました。
1. 抽出データのWebページ表示
	1. 抽出したデータの実装
            - では、Json.getで取得したデータを取り出すまでできたので、Web上にそのデータを表示する事を実装していきましょう。
	1. HTMLファイルの変更方法
	        - lib/aedmap_web/templates/page/index.html.eex　ファイルを開きます。
            - 中に書かれている<タグ>を全て削除します。
	1. テスト
            - 全て削除すると、localhost:4000の表示されているブラウザの内容が消えて、ヘッダー情報だけが表示される状態になります。
	1.  HTMLファイルの実装（プログラム部分）
            - 続いて、index.html.eex の中に先ほどコンソール上で試したプログラムを書いていきます。
            - その際、何も記述しないと、ブラウザに書いたまま表示されます。そこで、Elixirの言語を書いているとわかるように
            - <% %>タグで囲います。
		    - <% [ result ] = Json.get("https://aed.azure-mobile.net", "/api/NearAED?lat=35.96&lng=136.185")
            -     latitude = Map.get(result,"Latitude")
            -     longitude = Map.get(result,"Longitude")
            -     locationName = Map.get(result,"LocationName")
            - %>
            - これで、それぞれ、latitude, longitude, locationName　に 緯度、経度、ロケーションの名称が取得できました。
	1.  HTMLファイルの実装（表示部分）
            - では、Webの方に表示して見ましょう。表示するには、<%= %> タグを利用します。
            - <%= latitude %><br> 
            - <%= longitude %><br>
            - <%= locationName　%><br>
	1. テスト
            - これで、ブラウザに、無事にAPIで取得したデータの緯度経度、ロケーションの名称を表示する事ができました。
1. 地図のWebページ表示
            - 続いて、このデータを利用して地図に表示できるようにしたいと思います。
	1. leaflet.js とは
            - 地図を利用するのに、今回は簡単に使える leafletjs というJSのモジュールを使います。https://leafletjs.com/
	1. モジュールとは
	1. leaflet.js の導入方法
            - leafletjsを使う準備として、色々ありますが、今回は簡単に、CDNを利用して使えるようにします。
            - https://leafletjs.com/download.html　より、Using a Hosted Version of Leaflet　に記載あるリンクをコピーします
            - <link rel="stylesheet" href="https://unpkg.com/leaflet@1.4.0/dist/leaflet.css" />
            - <script src="https://unpkg.com/leaflet@1.4.0/dist/leaflet.js"></script>
            - コピーしたら、lib/aedmap_web/templates/layout/app.html.eex ファイルの<head>タグの中の一番最下部にペーストします。
            - これで、leafletjsのモジュールを使えるようになりました。
	1. leaflet.js での実装（プログラム部分）
            - 早速、https://leafletjs.com/index.html　の OverView　にあるサンプルをコピーして ib/aedmap_web/templates/page/index.html.eex
            - のファイルの中にペーストします。
            - ペーストしたら、今回は、Javascriptだという事がわかるように<script></script>タグで囲みます。
            - <script>
            - var map = L.map('map').setView([51.505, -0.09], 13);
			- 
            - L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
            -     attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
            - }).addTo(map);
			- 
            - L.marker([51.5, -0.09]).addTo(map)
            -     .bindPopup('A pretty CSS3 popup.<br> Easily customizable.')
            -     .openPopup();
            - </scirpt>
	1. leaflet.js での実装（表示部分）
            - `<script>` で地図を作る機能を実装したので、次いでJavascriptが機能する場所を追加しましょう。
            - htmlの中で、divタグを利用します。<div id="map"></div> タグを追加します。
            - まだ、表示されません。それは、機能はある、構造もある、けど見せ方がまだ未定義でしたので、見せ方を定義します。
            - 見せ方はCSSで定義するので、CSSだとわかるように<style></style>タグで囲みます。
            - 今回は、lib/aedmap_web/templates/layout/app.html.eex のファイルの<head>タグの中に書くようにします。
            - div#map{ width: 100%; heigth: 500px; }
            - これで、表示されました。
	1. leaflet.jsプログラム部分の解説
            - では、このMapのポイントをAPIで取得したデータに従って表示されるようにしましょう。
			- 
            - その為に、leafletjsの<script>の中を解説していきます。
			- 
            - こちらですが、　var map = L.map('map').setView([51.505, -0.09], 13);
			- 
            - 地図が最初に表示される際の中心位置と 地図のズームレベルを定義します。
            - var map = L.map('map').setView([緯度, 経度], ズームレベル);
			- 
            - 続いて、マーカーをつけている箇所は次のようになります。
            - L.marker([緯度, 経度]).addTo(map)
            -     .bindPopup('ポップアップに表示する内容')
            -     .openPopup();
			- 
            - そして、ここは何をしているかというと、
            - L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
            -     attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
            - }).addTo(map);
			- 
            - https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.pngは、表示したい地図タイルのURLを指定しています。
	1. 地図タイルの変更
            - この例では、Openstreetmapの地図タイルを利用していますが、国土地理院のタイルを利用する場合はここを

            - https://maps.gsi.go.jp/development/ichiran.html　にある、https://cyberjapandata.gsi.go.jp/xyz/std/{z}/{x}/{y}.png
            - に変更する事で、地図を変更する事が可能です。

            - また、その際には、attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a>の部分を
            - 国土地理院の記載に変更する必要があります。URLは国土地理院のページに、

            - 地理院タイル一覧ページ（https://maps.gsi.go.jp/development/ichiran.html）へのリンクを付けてください。

            - と書いてあるので、次のように変更します。
            - attribution: '&copy; <a href="https://maps.gsi.go.jp/development/ichiran.html">国土地理院</a>

            - このように地図タイルを変更する事も簡単にできます。

            - 今回は、オープンストリートマップのタイルで進めます。
1. 地点データの追加
	1. 外部データからの追加
            - それでは、地図を描画している箇所を理解した所で、APIのデータを追加できるようにしましょう。
			- 
            - <script>
            - var map = L.map('map').setView([<%= latitude %>, <%= longitude %>], 13);
			- 
            - L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
            -     attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
            - }).addTo(map);
			- 
            - L.marker([<%= latitude %>, <%= longitude %>]).addTo(map)
            -     .bindPopup('<%= locationName　%>')
            -     .openPopup();
            - </scirpt>
	1. DBへの追加
		1. DBとは
		1. DBへの入力
            - では、続いて DBへの入力を追加します。コンソール画面から次のコマンドを打ちます。
			- 
            - mix phx.gen.html AED Location locations latitude:float longitude:float locationName:string
            - lib/aedmap_web/router.ex　のscope　の中に　resources "/locations", LocationController　を追記します。
            - scope "/", AedmapWeb do
            -     pipe_through :browser
			- 
            -     get "/", PageController, :index
            -     resources "/locations", LocationController
            - end
            - 期日をしたら、保存し、コンソールから次のコマンドを打ちます。
			- mix ecto.migrate
		1. 表示の確認
            - 追加できたら、iex -S mix phx.server でサーバーを立ち上げて、ブラウザで確認します。
            - ブラウザから、http://localhost:4000/locations　でページが表示される事を確認します。1. WebページからDBへの追加

	1. Webページからのデータ追加
            - New Location をクリックして、Latitude、Longitude、Locationname にデータを入れて見ましょう。
            - 例えば、文京区のAEDのオープンデータを確認して見ます。
            - https://www.city.bunkyo.lg.jp/bosai/bosai/bousai/snota/aed/settikasho.html
            - PDFで配置の施設一覧が確認できます。この施設名から緯度経度を探して、登録して見たいと思います。
            - 施設名から緯度経度を調べられるサイトを探すといくつかありますが、今回はこちらを利用して見ます。
            - https://user.numazu-ct.ac.jp/~tsato/webmap/sphere/coordinates/yahoo_olp/
            - 文教シビックセンターで検索すると、35.707895	139.752286 が取得できました。
            - 早速、DBに入力して見ます。各入力欄にデータを入力して、Saveを押すと、Show Locationに画面が切り替わり、
            - DBに入った事が確認できます。
            - Editを押すと、修正する事も可能です。
            - それでは、入力したDBからデータを取得して、地図にマップするのを追加して見ましょう。
---

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

1. [A1]基礎知識	-	Webの仕組みやプログラミングに必要な知識を学ぶ
<!--	1. [B]Web（World Wide Web）とは
		https://developer.mozilla.org/ja/docs/Learn/Common_questions/Pages_sites_servers_and_search_engines
		https://developer.mozilla.org/ja/docs/Learn/Getting_started_with_the_web/How_the_Web_works
		* 説明１
		* 説明２
	1. [B]Webページとは
	0. [B]HTMLとは
		https://developer.mozilla.org/ja/docs/Web/HTML
		* HTML（HyperText Markup Language　- ハイパーテキスト マークアップ ランゲージ）
		* ウェブのもっとも基本的な構成要素
		* ウェブページの基本レイアウトに従ってウェブページのコンテンツを記述し定義するもの
	0. [B]CSSとは
	1. [B]JavaScriptとは
	0. [B]Webの仕組み
		https://developer.mozilla.org/ja/docs/Learn/Common_questions/Pages_sites_servers_and_search_engines
		https://developer.mozilla.org/ja/docs/Learn/Getting_started_with_the_web/How_the_Web_works
		* 説明１
		* 説明２
	0. [B]用語解説
		<a>クライアント
		<a>Webブラウザ
		<a>サーバー
		<a>データベース
		<a>リクエストとレスポンス
		<a>インターネット接続
		<a>ウェブページ
			ウェブブラウザに表示可能なドキュメント
	0. [B]用語解説
		<a>HTML
		<a>ハイパーテキスト
			- ウェブページから別なページに接続するリンク
			- ウェブサイト内でもウェブサイト間でも
			- ウェブの基礎的な特徴
		<a>マークアップ
			- たくさんの特殊な「要素」を用いる
			- <a>タグを利用
				HTML のタグは、大文字と小文字の区別はありません。つまり、大文字でも、小文字でも、混在して書いても構いません。例えば、 <title> タグは <Title> や <TITLE> やその他の方法で書くことができます
	0. [B]CSS（スタイルシート）とは
		https://developer.mozilla.org/ja/docs/Web/CSS
		* 体裁や見栄えを表現するために用いられる
		<a>CSS
	0. [B]JavaScriptとは
		https://developer.mozilla.org/ja/docs/Web/JavaScript
		* プログラミング言語
		* Web ページでよく使用される
		* Webページに動作を付ける
		* 非ブラウザ環境においても多く使用されている
		<a>JavaScript
	0. [B]Elixirとは
		https://www.ossnews.jp/oss_info/Elixir
		https://ja.m.wikipedia.org/wiki/Elixir_(プログラミング言語)
		* プログラミング言語
		* 短く書ける
		* メンテナンスしやすい
		* １つのマシンで数十万の処理を並行して行える
			- 処理が早い
		* 予想通りに物事が進まなくなった場合の対応を思い通りに保証できる
	0. [B]型とは
		https://ja.m.wikipedia.org/wiki/データ型
		* データ（値）の種類に関する分類
			- 0, 1, 2, -42 といったような値は整数型
			- "foo", "Hello" といったような値は文字列型
		<a>型
	00. [B]Elixirの主な型
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
-->
2. [A1]環境構築	-	地図アプリを作るために必要な設定をする
	1. [A2]CUI
		* 作業の内容と目的
		* 起動方法
			1. [D] Windows
				* コマンドプロント
					起動方法
			2. [D] MacOS
				* ターミナル
				* 起動方法
	2. [B]CUIとは
		https://ja.m.wikipedia.org/wiki/キャラクタユーザインタフェース
		* ユーザインタフェース
			機械と人間との伝達を行うもの
		* 文字列が表示されるウィンドウに出力する
		* キーボード等から文字列を入力する
		<a>CUI
	3. [G]確認
	4. [A2]Firefox
		* 作業の内容と目的
		* 手順
			1. [D]
			2. [D]
			3. [D]
	5. [B]Firefoxとは
		* 説明
		<link>Webブラウザ
	6. [G]確認
	7. [A2]RESTClient
		* 作業の内容と目的
		* 手順
			[D]
			[D]
			[D]
	8. [B]RESTClientとは
	9. [G]確認
	10. [A2]テキストエディタ
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
	11. [B]テキストエディタとは
	12. [G]確認
	13. [A2]Elixir
		* 作業の内容と目的
			<link>Elixirとは
		* 手順
			[D]
			[D]
			[D]
	14. [G]確認
	15. [A2]node.js
		* 作業の内容と目的
		* 手順
			[D]
			[D]
			[D]
	16. [B]node.jsとは
	17. [G]確認
	18. [A2]PostgreSQL
		* 作業の内容と目的
		* 手順
			[D]
			[D]
			[D]
	19. [B]PostgreSQLとは
	20. [G]確認
	21. [A2]Phoenixframework
		* 作業の内容と目的
		* 手順
			[D]
			[D]
			[D]
	22. [B]Phoenixframeworkとは
	23. [G]確認
3. [A1]APIサーバーの構築	-	地図アプリを提供するためのシステムを作る
	1. [A2]プロジェクトの作成
		* 作業の内容と目的
			- 使用するソフトウェア
		* 手順
			[D]
			[D]
			[D]
	2. [A2]Webサーバーの確認
		* 作業の内容と目的
			- 使用するソフトウェア
		* 手順
			[D]
			[D]
			[D]
	3. [A2]サーバーの起動
		* 作業の内容と目的
			- 使用するソフトウェア
		* 手順
			[D]
			[D]
			[D]
	4. [A2]サーバーの終了方法
		* 作業の内容と目的
			- 使用するソフトウェア
		* 手順
			[D]
			[D]
			[D]
	5. [A2]フォルダ移動
		* 作業の内容と目的
			- 使用するソフトウェア
		[A2]作業内容
	6. [A2]DBの作成
		* 作業の内容と目的
			- 使用するソフトウェア
		* 手順
			[D]
			[D]
			[D]
	7. [A2]JSONデータの作成
		* 作業の内容と目的
			- 使用するソフトウェア
		* 手順
			[D]
			[D]
			[D]
	8. [A2]Router.exの設定
		* 作業の内容と目的
			- 使用するソフトウェア
		* 手順
			[D]
			[D]
			[D]
	9. [A2]マイグレーション
		* 作業の内容と目的
			- 使用するソフトウェア
		* 手順
			[D]
			[D]サーバーの立ち上げ
			[D]ブラウザで確認
	10. [A2]RESTClient の設定
	11. [A2]RESTClientでGET
		* 作業の内容と目的
			- 使用するソフトウェア
		* 手順
			[D]
			[D]
			[D]
	12. RESTClientでPOST
		* 作業の内容と目的
			- 使用するソフトウェア
		* 手順
			[D]
			[D]
			[D]
4. [A1]地図の表示	-	まずは地図を表示してみる
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
5. [A1]外部APIの呼び出し	-	公開されている地図システムを利用する
	[A2]APIを扱うパッケージの追加
6. [A1]DBの操作	-	データ群を扱う
	[A2]DB操作の追加
7. [A1]内部APIの呼び出し	-	ツールを使って地図アプリを配信する
	[A2]Vue.jsとaxiosを使ってAPIを呼出す
	[B]フレームワークとは
	[A2]CDNを使用する為のタグを追加する
	[A2]表示
	[A2]更新
	[A2]削除
	[A2]追加
8. [A1]地図へのポイント追加
	[A2]繰り返し
9. [A1]自分の緯度経度の取得
	[A2]現在地取得
	[A2]Terf.js CDN追加
	[A2]GeoJsonに入れる
10. [A1]CSSデータの読み込み
11. [A1]デプロイ					

---

#メモ
  - 今、何やっているか？の進捗が確認できる事 (作業に連番を振る)
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

 #最終確認事項
 - 項目の採番
 - 採番されている要素には全てページ内リンク
 - 外部リンク先（青文字、下線）
 - ページ内リンク（色普通、下線なし）
 - 名称の大文字小文字、誤字脱字
 - 文章中のページ内リンクは<a href="#/">で検索


---

# Windowsメモ


We are almost there! The following steps are missing:

    $ cd gismap
    $ mix deps.get
    $ cd assets && npm install && node node_modules/webpack/bin/webpack.js --mode development

Then configure your database in config/dev.exs and run:

    ($ cd ../)
    $ mix ecto.create

Start your Phoenix app with:

    $ mix phx.server

You can also run your app inside IEx (Interactive Elixir) as:

    $ iex -S mix phx.server


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

---

### コマンド
`explorer （表示したいフォルダ）`  エクスプローラーでフォルダを開く
`dir` 現在のフォルダの中身を表示する
`cd （移動したいフォルダ）`  フォルダを移動する
`cd`  現在のフォルダの位置（パス）を表示する


---

@quote[Macは、ターミナルと呼ぶ](https://developer.apple.com/library/archive/technotes/tn2002/tn2071.html#//apple_ref/doc/uid/DTS10003098)

@quote[Windowsは、コマンドプロンプトと呼ぶ](https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/windows-commands)
