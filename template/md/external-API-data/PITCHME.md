---?color=#3A8FB7
@snap[breadcrumbs-wrap bluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [8. 外部データの取得と抽出](#/)
@olend
@snapend

@snap[west headline]
## 外部データの<br>取得と抽出
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [8. 外部データの取得と抽出](#/)
@olend
@snapend

### @css[slide-title](外部データの取得と抽出)

@snap[slide-contents]

@box[rounded box-style](外部データを取得し、そのデータの中から<br>必要な部分のみを抽出します。)

@ol[numberlist numberlist-color2](false)
- [外部データの取得](#/)
- [Elixir の特徴](#/)
- [取得したデータの観察](#/)
- [取得したデータの抽出（マップ型）](#/)
- [抽出したデータの確認（マップ型）](#/)
- [取得したデータの抽出（"Latitude"）](#/)
@olend

@snapend

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [8. 外部データの取得と抽出](#/)
- [1. 外部データの取得](#/)
@olend
@snapend

@snap[west headline]
## @color[white](外部データの取得)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [8. 外部データの取得と抽出](#/)
- [1. 外部データの取得](#/)
@olend
@snapend

### @css[slide-title](外部データの取得)

@snap[slide-contents]

@box[rounded box-style]( **CUI** を使って、外部APIからデータを取得します。)

@snap[left-column]
@ol[numberlist numberlist-color4](true)
- iex -S mix phx.server
- Json.get("https://aed.azure-mobile.net", "/api/NearAED?lat=35.96&lng=136.185")
@olend
@snapend

@snap[right-column]
@snap[gist-box half-gist-box]

@gist[json zoom-09](https://gist.github.com/yuki-thewaggle/d1cf3c8d2d4bcc2b61853f68559d56c9)

@[1](サーバーを起動します。)
@[6](外部APIからデータを取得します。)
@[7-44](このようなデータが取得できます。)

@snapend
@snapend

@snapend

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [8. 外部データの取得と抽出](#/)
- [2. Elixir の特徴](#/)
@olend
@snapend

@snap[west headline]
## @color[white](Elixir の特徴)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [8. 外部データの取得と抽出](#/)
- [2. Elixir の特徴](#/)
@olend
@snapend

### @css[slide-title](Elixir の特徴)

@snap[slide-contents]

@box[rounded box-style](Elixir で扱う<u>[データ型](https://ja.m.wikipedia.org/wiki/データ型)</u>には以下のようなものがあります。<br>詳しくは<u>[公式サイトの記載](https://elixir-lang.org/getting-started/basic-types.html)</u>を確認してください。)

@snap[left-column]
<table>
<thead>
<tr>
	<th>型</th>
	<th>表記例</th>
</tr>
</thead>
<tbody>
<tr>
	<th>整数</th>
	<td>1</td>
</tr>
<tr>
	<th>整数(16進数)</th>
	<td>0x1F</td>
</tr>
<tr>
	<th>小数</th>
	<td>1.0</td>
</tr>
<tr>
	<th>論理値</th>
	<td>true</td>
</tr>
<tr>
	<th><u>[アトム](https://elixirschool.com/ja/lessons/basics/basics/#アトム)</u></th>
	<td>:atom</td>
</tr>
</tbody>
</table>
@snapend

@snap[right-column]
<table>
<thead>
<tr>
	<th>型</th>
	<th>表記例</th>
</tr>
</thead>
<tbody>
<tr>
	<th>文字列</th>
	<td>"elixir"</td>
</tr>
<tr>
	<th><u>[リスト](https://elixirschool.com/ja/lessons/basics/collections/#リスト)</u></th>
	<td>[1, 2, 3]</td>
</tr>
<tr>
	<th><u>[タプル](https://elixirschool.com/ja/lessons/basics/collections/#タプル)</u></th>
	<td>{1, 2, 3}</td>
</tr>
<tr>
	<th><u>[キーワードリスト](https://elixirschool.com/ja/lessons/basics/collections/#キーワードリスト)</u></th>
	<td>@size[0.85em](&#91;foo: "hello", bar: "world"&#93;)</td>
</tr>
<tr>
	<th><u>[マップ](https://elixirschool.com/ja/lessons/basics/collections/#マップ)</u></th>
	<td>%{key = "value"}</td>
</tr></tbody>
</table>
@snapend

@snapend

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [8. 外部データの取得と抽出](#/)
- [3. 取得したデータの観察](#/)
@olend
@snapend

@snap[west headline]
## @color[white](取得したデータの<br>観察)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [8. 外部データの取得と抽出](#/)
- [3. 取得したデータの観察](#/)
@olend
@snapend

### @css[slide-title smaller-font](取得したデータの観察)

@snap[slide-contents]
@snap[gist-box]

@fa[external-link]
<u>https://gist.github.com/yuki-thewaggle/8d5c582ba46e0350acc6fcba0d66439c</u>

@gist[json zoom-09](https://gist.github.com/yuki-thewaggle/8d5c582ba46e0350acc6fcba0d66439c)

@[1]([]（リスト型） に囲まれています。)
@[2](その中に %{}（マップ型） があります。)
@[3-36](さらにその中にデータの中身があります。)
@[20](今回必要なデータだけを取り出しやすくしていきます。)

@snapend
@snapend

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [8. 外部データの取得と抽出](#/)
- [4. 取得したデータの抽出（マップ型）](#/)
@olend
@snapend

@snap[west headline]
## @color[white](取得したデータの<br>抽出（マップ型）)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [8. 外部データの取得と抽出](#/)
- [4. 取得したデータの抽出（マップ型）](#/)
@olend
@snapend

### @css[slide-title smaller-font](取得したデータの抽出（マップ型）)

@snap[slide-contents]

@box[rounded box-style]( **CUI** を使って、取得したデータの中からマップ型のデータを抜き出します。)

@snap[left-column]
@ol[numberlist numberlist-color4](false)
- [ result ] = Json.get("https://aed.azure-mobile.net", "/api/NearAED?lat=35.96&lng=136.185")
@olend
@snapend

@snap[right-column]
@snap[gist-box half-gist-box]

@gist[json zoom-08](https://gist.github.com/yuki-thewaggle/1f7029888a37f0df49d65ec95f549b7b)

@[1](これで result の中は、)
@[1](%{}（マップ型）のデータのみが束縛されています。)

@snapend
@snapend

@snapend

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [8. 外部データの取得と抽出](#/)
- [5. 抽出したデータの確認（マップ型）](#/)
@olend
@snapend

@snap[west headline]
## @color[white](抽出したデータの<br>確認（マップ型）)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [8. 外部データの取得と抽出](#/)
- [5.  抽出したデータの確認（マップ型）](#/)
@olend
@snapend

### @css[slide-title smaller-font](抽出したデータの確認（マップ型）)

@snap[slide-contents]

@box[rounded box-style]( **CUI** を使って、result の中身が<br>マップ型であることを確認します。)

@snap[left-column]
@ol[numberlist numberlist-color4](false)
- result
@olend
@snapend

@snap[right-column]
@snap[gist-box half-gist-box]

@gist[elixir zoom-08](https://gist.github.com/yuki-thewaggle/295c0a9d45b220e2f4a20f1232f319ab)

@[1](result の中身を表示します。)
@[2]([]（リスト型）を表す記号がなくなり)
@[37](%{}（マップ型）のデータが抜き取れています。)

@snapend
@snapend

@snapend

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [8. 外部データの取得と抽出](#/)
- [5. 取得したデータの抽出（"Latitude"）](#/)
@olend
@snapend

@snap[west headline]
## @color[white](取得したデータの<br>抽出（"Latitude"）)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [8. 外部データの取得と抽出](#/)
- [5. 取得したデータの抽出（"Latitude"）](#/)
@olend
@snapend

### @css[slide-title smaller-font](取得したデータの抽出（"Latitude"）)

@snap[slide-contents]

@box[rounded box-style]( **CUI** を使って、result の中身から<br>"Latitude" のデータを取得します。)

@snap[left-column]
@ol[numberlist numberlist-color4](false)
- latitude = Map.get( result, "Latitude" )
@olend
@snapend

@snap[right-column]
@snap[gist-box half-gist-box]

@gist[elixir zoom-08](yuki-thewaggle/10abb0cba3a44ef8cb7fce0df35d3ece)

@[1](result から "Latitude" を latitude に取得します。)
@[2](値が取得できています。)

@snapend
@snapend

@snapend
