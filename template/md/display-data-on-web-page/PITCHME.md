---?color=#3A8FB7
@snap[breadcrumbs-wrap bluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [9. 抽出データのWebページ表示](#/)
@olend
@snapend

@snap[west headline]
## 抽出データの<br>Webページ表示
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [9. 抽出データのWebページ表示](#/)
@olend
@snapend

### @css[slide-title](抽出データのWebページ表示)

@snap[slide-contents]

@box[rounded box-style](外部データを取得し必要なデータを抽出して、<br>Web上に表示します。)

@ol[numberlist numberlist-color2](false)
- [HTMLファイルのオープン](#/)
- [HTMLファイルの変更](#/)
- [テスト](#/)
- [HTMLファイルの実装（プログラム）](#/)
- [HTMLファイルの実装（表示）](#/)
- [テスト](#/)
@olend

@snapend

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [9. 抽出データのWebページ表示](#/)
- [1. HTMLファイルのオープン](#/)
@olend
@snapend

@snap[west headline]
## @color[white](HTMLファイルの<br>オープン)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [9. 抽出データのWebページ表示](#/)
- [1. HTMLファイルのオープン](#/)
@olend
@snapend

### @css[slide-title](HTMLファイルのオープン)

@snap[slide-contents]

@box[rounded box-style]( **CUI** を使って、<br>Visual Studio Code で HTMLファイルを開きます。)

@ol[numberlist numberlist-color4](true)
- **lib/aedmap_web/templates/page/index.html.eex** を開きます。
- 画面上部のメニューから「**View**」 > 「**Explorer**」 をクリックします。
- 画面の左側に「**EXPLORER**」という枠が開きます。
- 「EXPLORER」の中から「**lib/aedmap_web/templates/page/index.html.eex**」を捜してクリックします。
@olend

@snapend

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [9. 抽出データのWebページ表示](#/)
- [2. HTMLファイルの変更](#/)
@olend
@snapend

@snap[west headline]
## @color[white](HTMLファイルの<br>変更)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [9. 抽出データのWebページ表示](#/)
- [2. HTMLファイルの変更](#/)
@olend
@snapend

### @css[slide-title](HTMLファイルの変更)

@snap[slide-contents]

@box[rounded box-style]( **Visual Studio Code** を使って、HTMLファイル（index.html.eex）に変更を加え保存します。)

@snap[left-column]
@ol[numberlist numberlist-color4](true)
- ファイルの中に書かれている記述を全て削除します。
- Windowsの場合、「**Ctrl + S**」で保存します。
- Macの場合、「**command + S**」で保存します。
@olend
@snapend

@snap[right-column]
@img[goal-image to-center](template/img/display-data-on-web-page/clear-html.png)
@snapend

@snapend


---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [9. 抽出データのWebページ表示](#/)
- [3. テスト](#/)
@olend
@snapend

@snap[west headline]
## @color[white](テスト)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [9. 抽出データのWebページ表示](#/)
- [3. テスト](#/)
@olend
@snapend

### @css[slide-title](テスト)

@snap[slide-contents]

@box[rounded box-style]( **Webブラウザー** を使って、HTMLファイルの変更が<br>Webページに反映されていることを確認します。)

@ol[numberlist numberlist-color4](false)
- アプリケーションが終了している場合は、<br>[CUIでアプリケーションを起動](#/)します。
- <span class="not-selectable">Webブラウザーで</span><u>http://localhost:4000/</u><span class="not-selectable">にアクセスします。</span>
- ヘッダーだけが表示されていることを確認します。
@olend

@snapend

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [9. 抽出データのWebページ表示](#/)
- [4. HTMLファイルの実装（プログラム）](#/)
@olend
@snapend

@snap[west headline]
## @color[white](HTMLファイルの<br>実装（プログラム）)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [9. 抽出データのWebページ表示](#/)
- [4. HTMLファイルの実装（プログラム）](#/)
@olend
@snapend

### @css[slide-title smaller-font](HTMLファイルの実装（プログラム）)

@snap[slide-contents]

@box[rounded box-style]( **Visual Studio Code** を使って、オープンしている<br>index.html.eexファイルにプログラムを加えます。)



@snap[gist-box half-gist-box]

@gist[html zoom-09](https://gist.github.com/yuki-thewaggle/515cac053200d75a6791bc448e61402e)

@[1-5](全てをコピーして、index.html.eexファイルに貼り付けて保存します。)
@[1](外部データを取得しています。)
@[2](latitude に "Latitude"（緯度） の値を保存しています。)
@[3](longitude に "Longitude"（経度） の値を保存しています。)
@[4](locationName に "LocationName"（ロケーションの名称） の値を保存しています。)

@snapend


@snapend

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [9. 抽出データのWebページ表示](#/)
- [5. HTMLファイルの実装（表示）](#/)
@olend
@snapend

@snap[west headline]
## @color[white](HTMLファイルの<br>実装（表示）)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [9. 抽出データのWebページ表示](#/)
- [5. HTMLファイルの実装（表示）](#/)
@olend
@snapend

### @css[slide-title smaller-font](HTMLファイルの実装（表示）)

@snap[slide-contents]

@box[rounded box-style]( **Visual Studio Code** を使って、オープンしている<br>index.html.eexファイルに表示を加えます。)

@snap[gist-box half-gist-box]


@gist[html zoom-09](https://gist.github.com/yuki-thewaggle/c14b0eea4ee96e4b872685efff0ebbe7)

@[0](全てをコピーして、先程の続きに貼り付けます。)
@[0](表示するには、<%= %> タグを利用します。)
@[1](緯度の値を表示します。)
@[2](経度の値を表示します。)
@[3](ロケーションの名称を表示します。)

@snapend

@snapend

---?color=#77B6D4
@snap[breadcrumbs-wrap lightbluescale]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [9. 抽出データのWebページ表示](#/)
- [6. テスト](#/)
@olend
@snapend

@snap[west headline]
## @color[white](テスト)
@snapend

---
@snap[breadcrumbs-wrap]
@ol[breadcrumbs](false)
- [ハンズオン講習会の流れ](#/2)
- [9. 抽出データのWebページ表示](#/)
- [6. テスト](#/)
@olend
@snapend

### @css[slide-title](テスト)

@snap[slide-contents]

@box[rounded box-style]( **Webブラウザー** を使って、HTMLファイルの変更が<br>Webページに反映されていることを確認します。)

@snap[left-column]

@ol[numberlist numberlist-color4](false)
- アプリケーションが終了している場合は、[アプリケーションを起動](#/)します。
- <span class="not-selectable">Webブラウザーで</span><u>[localhost:4000](http://localhost:4000/)</u><span class="not-selectable">にアクセスします。</span>
- データが表示されていることを確認します。
@olend

@snapend

@snap[right-column]
@img[goal-image to-center](template/img/display-data-on-web-page/display-data.png)
@snapend

@snapend


