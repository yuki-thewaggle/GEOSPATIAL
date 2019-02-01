---?color=#3A8FB7
@snap[breadcrumbs-wrap bluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [8. 外部データの取得と抽出](#/)
@olend
@snapend

@snap[west headline]
## 外部データの取得と抽出
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

@box[rounded box-style](外部データを取得し、そのデータの中から必要な部分のみを抽出します。)

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

@gist[json zoom-09](https://gist.github.com/yuki-thewaggle/8d5c582ba46e0350acc6fcba0d66439c)

@[0](このようなデータが取得できます。)

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
<tr>
	<th width="45%">型</th>
	<th>表記例</th>
</tr>
<tr>
	<td style="background-color:rgba(0,0,0,0.1);">整数</td>
	<td>1</td>
</tr>
<tr>
	<td style="background-color:rgba(0,0,0,0.1);">整数(16進数)</td>
	<td>0x1F</td>
</tr>
<tr>
	<td style="background-color:rgba(0,0,0,0.1);">小数</td>
	<td>1.0</td>
</tr>
<tr>
	<td style="background-color:rgba(0,0,0,0.1);">論理値</td>
	<td>true</td>
</tr>
<tr>
	<td style="background-color:rgba(0,0,0,0.1);"><u>[アトム](https://elixirschool.com/ja/lessons/basics/basics/#%E3%82%A2%E3%83%88%E3%83%A0)</u></td>
	<td>:atom</td>
</tr>
</table>
@snapend

@snap[right-column]
<table>
<tr>
	<th width="45%">型</th>
	<th>表記例</th>
</tr>
<tr>
	<td style="background-color:rgba(0,0,0,0.1);">文字列</td>
	<td>"elixir"</td>
</tr>
<tr>
	<td style="background-color:rgba(0,0,0,0.1);"><u>[リスト](https://elixirschool.com/ja/lessons/basics/collections/#%E3%83%AA%E3%82%B9%E3%83%88)</u></td>
	<td>[1, 2, 3]</td>
</tr>
<tr>
	<td style="background-color:rgba(0,0,0,0.1);"><u>[タプル](https://elixirschool.com/ja/lessons/basics/collections/#%E3%82%BF%E3%83%97%E3%83%AB)</u></td>
	<td>{1, 2, 3}</td>
</tr>
<tr>
	<td style="background-color:rgba(0,0,0,0.1);"><u>[キーワードリスト](https://elixirschool.com/ja/lessons/basics/collections/#キーワードリスト)</u></td>
	<td>[foo: "hello", bar: "world"]</td>
</tr>
<tr>
	<td style="background-color:rgba(0,0,0,0.1);"><u>[マップ](https://elixirschool.com/ja/lessons/basics/collections/#マップ)</u></td>
	<td>%{key = "value"}</td>
</tr>
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

@[0](これで result の中は、)
@[0](%{}（マップ型）のデータのみが束縛されています。)

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
