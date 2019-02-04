# アジェンダ項目再編
1. 環境構築(environment)
2. 基礎知識(basic-knowledge-webgis)
3. Phoenix プロジェクト（create-a-new-project, add-modules, how-to-test-Elixir-project）
4. 外部データの利用(external-API, use-RESTClient, external-API-data, display-data-on-web-page, display-map-on-web-page)
5. DBの操作：DBへの追加、DBからの呼び出し、表示()
6. ページの追加()
7. 自分の位置情報の取得と表示()
8. その他の便利なツール紹介()


---
1. 基礎知識
2. 環境構築
3. Phoenix プロジェクトの作成	template/md/create-a-new-project
	1. プロジェクトの作成
        - mix phx.new aedmap
        - Y
	1. フォルダの移動
        - cd aedmap
	1. データベースの作成
        - mix ecto.create
	1. アプリケーションの起動
        - mix phx.server
	1. Webサイトの確認
        - ブラウザで http://localhost:4000 を確認
	1. アプリケーションの終了
        - Ctr + C を２回でサーバーをシャットダウン
4. Elixir モジュールの追加	template/md/add-modules
	1. モジュールとは
	1. Visual Studio Code の起動
        - ターミナル上で、 code . でVscodeを起動する
	1. モジュールの追加方法
        - mix.exs ファイルを開いて、 defp deps do の中に 追加のモジュールを書き込むと案内する
        - 追加のモジュールについては、Elixirは hex というパッケージマネージャを利用する
	1. mix.exs のオープン
	1. smallex の追加
        - hex から　smallex　という　APIを取得するのに便利なモジュールを追加
        - {:smallex, "~> 0.2.3"}, を defp deps do の中に追加して、保存する
	1. 確認
        - コンソール画面で、 mix deps.get をして、smallexがインストールされている事をコンソールに出力される結果から確認する
	1. smallex の使い方
        - hex の smallex　から、Online documentation のリンク先に飛んで、Json.getの使い方を説明
	1. CUIで文字化けが起こるとき
		- chcp 65001
5. プロジェクトのテスト方法		template/md/how-to-test-Elixir-project
	1. Elixir のテスト
        - iex -S mix phx.severでサーバーを立ち上げると、iexが起動しているのでコンソール上で、Elixirをテストできるようになる
		https://elixirschool.com/ja/lessons/basics/iex-helpers/
6. APIの利用	template/md/external-API
	1. APIとは
	1. AEDオープンデータプラットフォーム
	1. AEDオープンデータプラットフォームとは
        - APIは、今回はAEDオープンデータプラットフォームのAPIを利用する。http://hatsunejournal.jp/w8/AEDOpendata/
	1. 直近AED位置情報取得API
        - 直近AED位置情報取得API　を利用する、例に乗っているURLをhttps://aed.azure-mobile.net/api/NearAED?lat=35.96&lng=136.185
	1. 確認
        - 利用するとデータが取得できる事を確認する。
7. RESTClient の操作	template/md/use-RESTClient
	1. RESTClient の起動
	1. URLの設定
        - Firefoxのブラウザから、RESTClientを起動し、URLに　https://aed.azure-mobile.net/api/NearAED?lat=35.96&lng=136.185 を入力する
	1. Methodの設定
        - MethodはGetで、send すると、 ステータスコード　200 OKで JSONデータが取得されている事を確認する
	1. Requestの送信
	1. ステータスコードを確認
		- 無事に確認が取れたら、このような機能をElixirに実装していくと説明する
8. 外部データの取得と抽出	template/md/external-API-data
	1. 外部データの取得
        - まず、コンソール上で、Json.get("https://aed.azure-mobile.net", "/api/NearAED?lat=35.96&lng=136.185")をするとデータが取得できる事を確認する。
	1. Elixir の特徴
        - Elixirには、整数、浮動小数、真理値、atom、文字列、リスト、タプル、キーワードリスト、マップという書き方がある
        - 256 132.1123 true, false, :atom, "Hello", [1,:ok,"text"], {:ok, "text"}, [foo: "hello", bar: "world"], %{key = "value"}
        - それぞれの形の詳しい説明は、ここに乗っています。https://elixir-lang.org/getting-started/basic-types.html
	1. 取得したデータの観察
        - 先ほど、取得したデータを見てみると、 [ %{ dataの中身 } ] という形です。 []リストの中に %{} マップ型のデータ構造が入っています。
        - これを取得しやすくする為に、Map型のデータ構造だけ抜き取りたいと思います。
	1. 取得したデータの抽出（マップ型）
        - ここで、Elixirの特徴として、=は代入演算子では無く、　＝　はパターンマッチング　です。それを利用して、
        - マップ型のデータだけを抜き出して見ます。
        - [ result ] = Json.get("https://aed.azure-mobile.net", "/api/NearAED?lat=35.96&lng=136.185")
        - これで、result　の中は、%{ } マップ型のデータのみが束縛されています。
        - result　の中は、%{ ... "Latitude" => 35.959898 ... } のような形になっています。
	1. 抽出したデータの確認（マップ型）
	1. 取得したデータの抽出（"Latitude"）
        - ここから、Map.getを利用して、"Latitude" のデータを取得したいと思います。
        - latitude = Map.get( result, "Latitude" )
        - これで、latitudeには、35.959898　のデータが取得できました。
9. 抽出データのWebページ表示	template/md/display-data-on-web-page
	1. HTMLファイルのオープン
        - では、Json.getで取得したデータを取り出すまでできたので、Web上にそのデータを表示する事を実装していきましょう。
	    - lib/aedmap_web/templates/page/index.html.eex　ファイルを開きます。
    1. HTMLファイルの変更
	    - 中に書かれている<タグ>を全て削除します。
	1. テスト
        - 全て削除すると、localhost:4000の表示されているブラウザの内容が消えて、ヘッダー情報だけが表示される状態になります。
	1.  HTMLファイルの実装（プログラム）
        - 続いて、index.html.eex の中に先ほどコンソール上で試したプログラムを書いていきます。
        - その際、何も記述しないと、ブラウザに書いたまま表示されます。そこで、Elixirの言語を書いているとわかるように
        - <% %>タグで囲います。
	    - <% [ result ] = Json.get("https://aed.azure-mobile.net", "/api/NearAED?lat=35.96&lng=136.185")
        -     latitude = Map.get(result,"Latitude")
        -     longitude = Map.get(result,"Longitude")
        -     locationName = Map.get(result,"LocationName")
        - %>
        - これで、それぞれ、latitude, longitude, locationName　に 緯度、経度、ロケーションの名称が取得できました。
	1.  HTMLファイルの実装（表示）
        - では、Webの方に表示して見ましょう。表示するには、<%= %> タグを利用します。
        - <%= latitude %><br> 
        - <%= longitude %><br>
        - <%= locationName　%><br>
	1. テスト
        - これで、ブラウザに、無事にAPIで取得したデータの緯度経度、ロケーションの名称を表示する事ができました。
10. 地図のWebページ表示	template/md/display-map-on-web-page
        - 続いて、このデータを利用して地図に表示できるようにしたいと思います。
	1. leaflet.js とは
        - 地図を利用するのに、今回は簡単に使える leafletjs というJSのモジュールを使います。https://leafletjs.com/
	1. モジュールとは
	1. leaflet.js の導入方法
        - leafletjsを使う準備として、色々ありますが、今回は簡単に、CDNを利用して使えるようにします。
        - https://leafletjs.com/download.html　より、Using a Hosted Version of Leaflet　に記載あるリンクをコピーします
        - <link rel="stylesheet" href="https://unpkg.com/leaflet@1.4.0/dist/leaflet.css" />
        - <script src="https://unpkg.com/leaflet@1.4.0/dist/leaflet.js"></script>
        1. HTMLファイルのオープン
        - コピーしたら、lib/aedmap_web/templates/layout/app.html.eex ファイルの<head>タグの中の一番最下部にペーストします。
        - これで、leafletjsのモジュールを使えるようになりました。
	1. leaflet.js での実装（プログラム）
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
	1. leaflet.js での実装（表示）
        - `<script>` で地図を作る機能を実装したので、次いでJavascriptが機能する場所を追加しましょう。
        - htmlの中で、divタグを利用します。<div id="map"></div> タグを追加します。
    	- まだ、表示されません。それは、機能はある、構造もある、けど見せ方がまだ未定義でしたので、見せ方を定義します。
        - 見せ方はCSSで定義するので、CSSだとわかるように<style></style>タグで囲みます。
        - 今回は、lib/aedmap_web/templates/layout/app.html.eex のファイルの<head>タグの中に書くようにします。
        - div#map{ width: 100%; heigth: 500px; }
        - これで、表示されました。
	1. プログラム部分の解説
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
1. 地点データの追加		template/md/add-location-data
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
        - ブラウザから、http://localhost:4000/locations　でページが表示される事を確認します。		
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
	- もう一件追加して見ましょう。　礫川地域活動センター, 35.711938、 139.750418、で入力します。
        - それでは、入力したDBからデータを取得して、地図にマップするのを追加して見ましょう。

lib/aedmap_web/templates/location/index.html.eex
というファイルが作られています。ここに地図を追加して行きましょう。
lib/aedmap_web/templates/page/index.html.eex のファイルに書いた、コードを全てコピーします。
lib/aedmap_web/templates/location/index.html.eex　のページの一番下の行に書いてある
<span><%= link "New Location", to: Routes.location_path(@conn, :new) %></span>
より下に、先ほどコピーした内容を全て貼り付けます。
そうすると、AEDオープンデータプラットフォームから出した内容が表示された地図がブラウザに表示されます。

### DBの操作

この地図の内容をDBから取得した内容に変更していきます。
DBの操作には、Ectoのモジュールを利用する事でできます。
コンソールで、次のように書いてください。
```elixir
Ecto.Adapters.SQL.query( Aedmap.Repo  ,"SELECT * FROM locations", [])
{:ok,
%Postgrex.Result{
  columns: ["id", "latitude", "longitude", "locationName", "inserted_at",
   "updated_at"],
  command: :select,
  connection_id: 44500,
  messages: [],
  num_rows: 2,
  rows: [
    [1, 35.707895, 139.752286, "文教シビックセンター",
     ~N[2019-01-28 09:52:10.000000], ~N[2019-01-28 09:52:10.000000]],
    [2, 35.711938, 139.750418, "礫川地域活動センター",
     ~N[2019-01-29 03:55:12.000000], ~N[2019-01-29 03:55:12.000000]]
  ]
}}
```
 結果が表示されます。
結果をみると、statusと、構造体のタプル形式でデータを持っているのがわかります。
{ status, struct }のタプルで結果が取得されるので、構造体だけ取得できるように、あらかじめ、モジュール化しておきます。
lib/util/db.ex libフォルダ直下に、utilフォルダを作成し、db.exファイルを作ります。
```elixir
defmodule Db do
  def query(sql) do
    case Ecto.Adapters.SQL.query( Aedmap.Repo  ,sql, []) do
      {:ok, result } -> result
      {:error, _result } -> "sql error"
    end
  end
end
```
コンソールで利用できるか確かめます。コンソールに戻ったら、recompile　と入力してください。
:ok が表示されたら、無事にコンパイルされています。
それでは、無事にモジュールが利用できるか確認して見ましょう。
data = Db.query("SELECT * FROM locations;")
これで、dataに構造体のデータが紐づけられました。
構造体のデータは、.key名でデータを取得できます。
data.columns をコンソールで表示して見ます。
["id", "latitude", "longitude", "locationName", "inserted_at", "updated_at"]
続いて、data.rows をコンソールで表示して見ます。
[
  [1, 35.707895, 139.752286, "文教シビックセンター",
   ~N[2019-01-28 09:52:10.000000], ~N[2019-01-28 09:52:10.000000]],
  [2, 35.711938, 139.750418, "礫川地域活動センター",
   ~N[2019-01-29 03:55:12.000000], ~N[2019-01-29 03:55:12.000000]]
]
このままだと、columnsとrowsが対のデータになっていないので、columnsとrowsのタプル形式に変換します。
そこで、List.zip　を使います。
List.zip([[1,2],[3,4]])の形の引数を渡すと　[{1, 3}, {2, 4}] のようなタプルを保持したリストを返してくれます。
List.zip([data.columns, data,rows])とすれば良さそうです。しかし、data.rowsの形は[]リストの中に[]リストを持つ
データなので、一つのリストだけ取得して使いたいです。
そこで、ここでは試しに、先頭のリストだけ取得する方法を利用します。
[head | tail ] = data.rows
これで、headに一つめのリストだけが入るので、List.zipで利用して見ます。
List.zip([data.columns, head])
[
  {"id", 1},
  {"latitude", 35.707895},
  {"longitude", 139.752286},
  {"locationName", "文教シビックセンター"},
  {"inserted_at", ~N[2019-01-28 09:52:10.000000]},
  {"updated_at", ~N[2019-01-28 09:52:10.000000]}
]
無事に、columnsとrowの対のタプルを保持したリストができました。
今度は、このデータをMap.getで利用できるようにマップ型に変換したいと思います。
Map型にするには、Enum.intoを利用します。第一引数に、リスト、第２引数に %{} を入れる事で、Map型に変換した値が返ってきます。
Enum.into(List.zip([data.columns, head]), %{})
%{
  "id" => 1,
  "inserted_at" => ~N[2019-01-28 09:52:10.000000],
  "latitude" => 35.707895,
  "locationName" => "文教シビックセンター",
  "longitude" => 139.752286,
  "updated_at" => ~N[2019-01-28 09:52:10.000000]
}
これで、Map.getで値を取得しやすい形に変形できました。
次に、問題なのは、data.rowsはリストの中に入れ子でリストが入っているデータ形式です。
リストの中の一つ一つのリストをMap型に変換したい為、繰り返し処理させたいです。
そのような時に便利なのが、Enum.mapというものがあります。
Enum.map(リスト、処理) 第１引数にリストを入れ、第二引数に処理を書きます。
すると、リストの１つの値毎に処理を実行してくれます。
例えば、Enum.map([1,2,3], fn x -> x * 2 end ) と書きます。
そうすると、リストの中身が２倍された値が返ってきます。
[2, 4, 6]
これを利用して、第１引数に、data.rowsを、第２引数に先ほど、書いた、Enum.into(List.zip([data.columns, head]), %{})を
入れます。その際に、第二引数は無名関数と呼ばれる形式で、fn x -> 処理 end という形で入れます。xは第１引数で入れたリストの1つ
1つの値が入ってくると考えてください。
Enum.map(data.rows, fn row -> Enum.into(List.zip([data.columns, row]), %{}) end )
[
  %{
    "id" => 1,
    "inserted_at" => ~N[2019-01-28 09:52:10.000000],
    "latitude" => 35.707895,
    "locationName" => "文教シビックセンター",
    "longitude" => 139.752286,
    "updated_at" => ~N[2019-01-28 09:52:10.000000]
  },
  %{
    "id" => 2,
    "inserted_at" => ~N[2019-01-29 03:55:12.000000],
    "latitude" => 35.711938,
    "locationName" => "礫川地域活動センター",
    "longitude" => 139.750418,
    "updated_at" => ~N[2019-01-29 03:55:12.000000]
  }
]
これで、やりたい事ができたので、Dbモジュールの中に追加しましょう。
lib/util/db.ex
わかりやすくする為に、パイプで繋げる書き方に変えて見ます。
defp get(column, row) do
    List.zip([ column, row ])
    |> Enum.into(%{})
end
defにpをつけて、defpにする事で、モジュール外から利用できなくする事ができます。この関数はこのモジュールの中で使うものとして、defpにしておきます。
続いて、Enum.mapを追加します。
  def map(result) do
     Enum.map(result.rows, fn row -> get(result.columns, row) end )
  end
これで、Db　モジュールが完成です。以下のようになって入ればOKです。
defmodule Db do
  def query(sql) do
    case Ecto.Adapters.SQL.query( Aedmap.Repo  ,sql, []) do
      {:ok, result } -> result
      {:error, _result } -> "sql error"
    end
  end
  # Enum.mapをして、result.rowsの[[a],[b],[c]...]のようなリストを一つずつ、columnをkeyにするMap型に変換している
  def map(result) do
     Enum.map(result.rows, fn row -> get(result.columns, row) end )
  end
  # List.zipで[[1,2],[3,4]] => [ {1,3}, {2, 4} ]のタプルにする。Enum.intoで [ %{1 => 3}, %{2 => 4} ]のマップ型にする
  defp get(column, row) do
    List.zip([ column, row ])
    |> Enum.into(%{})
  end
end
書き終えたら、,コンソールから、recompileしましょう。
無事に動くかテストします。次のコマンドを打ってください。
data = Db.query("SELECT * FROM locations;")
results = Db.map(data)
それでは、lib/aedmap_web/templates/location/index.html.eex の中身を書き換えて行きましょう。
Json.getから取得してきていた箇所を削除し、Dbから取得する形にします。
コンソールで実行したコマンドを書きます。
<%
data = Db.query("SELECT * FROM locations;")
results = Db.map(data)
%>
次に、js　のmapの中心位置を決める緯度と経度にデータを入れたいと思います。今回は、最初のデータに入っている緯度と経度を
反映させるようにしたいと思います。
Elixir部分に以下を追加
[ head | tail ] = results 
latitude = Map.get(head,"latitude")
longitude = Map.get(head,"longitude")
jsに以下を追加
var map = L.map('map').setView([<%= latitude %>, <%= longitude %>], 13);
続いて、mapに追加するマーカーを複数表示する為に、
以下のように記述します。
<%= for result <- results do %>
L.marker([<%= Map.get(result,"latitude") %>, <%= Map.get(result,"longitude") %>]).addTo(map)
    .bindPopup('<%= Map.get(result,"locationName") %>')
    .openPopup();
<%= end %>


---

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
 - ページタイトル



---

# Windowsメモ

<!-->
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

-->
---

@quote[Macは、ターミナルと呼ぶ](https://developer.apple.com/library/archive/technotes/tn2002/tn2071.html#//apple_ref/doc/uid/DTS10003098)

@quote[Windowsは、コマンドプロンプトと呼ぶ](https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/windows-commands)


---

カットしたインクルード
---?include=template/md/basic-knowlede-webgis/PITCHME.md
---?include=template/md/environment/PITCHME.md
---?include=template/md/Building-APIServer/PITCHME.md
---?include=template/md/Show-map/PITCHME.md
---?include=template/md/External-API-call/PITCHME.md
---?include=template/md/DB-operation/PITCHME.md
---?include=template/md/Internal-API-call/PITCHME.md
---?include=template/md/points-to-the-map/PITCHME.md
---?include=template/md/own-latitude-longitude/PITCHME.md
