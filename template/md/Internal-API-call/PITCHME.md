---?color=#DB4D6D
# @css[headline](内部APIの取得)

---
@snap[midopoint north-west text-06]
### Vue.jsとaxiosを使ってAPIを呼出す
@snapend

CDN（Content Delivery Network）を使用して読み込む

[Vue.js](https://jp.vuejs.org/index.html)

[axios](https://github.com/axios/axios#axios)

---
@snap[midopoint north-west text-06]
### CDNを使用する為のタグを追加する
@snapend

```js
<script src="https://cdnjs.cloudflare.com/ajax/libs/vue/2.5.17/vue.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/axios/0.18.0/axios.min.js"></script>
```

`<head></head>`内に追記する

---
@snap[midopoint north-west text-06]
### 表示
@snapend

@gist[html zoom-05](Yoosuke/04c2374ec84b1248cc7a5d12d67725e4)

@[14-28](Vue側を作成し、axiosでデータ取得をします)
@[3-10](テーブルの中にinputフォームを作ります)
@[5-7](v-modelを使ってelのデータに入ってる内容を取得します)

---
@snap[midopoint north-west text-06]
### 更新
@snapend

@gist[html zoom-05](Yoosuke/05fe11928f2da1c59e257a70ab687b02)

@[11](v-on:click="onUpdate"を追加します)

---
@snap[midopoint north-west text-06]
### 更新
@snapend

@gist[js zoom-05](Yoosuke/47427ee583a24edcaaeb934e20ffbf22)

@[3]( asyncは同期処理をする為に追加します )
@[5]( forEach->第1引数に配列の要素、第2引数に配列の要素の添字)
@[7]( axios.put -> axios.putの第1引数であるURLには、更新対象となるデータのidを指定します)
@[9](第２引数には、オブジェクトリテラルで書く)
@[11-13]()

---
@snap[midopoint north-west text-06]
### 削除
@snapend

@gist[html zoom-05](Yoosuke/f3c6a68dd8625d879f9856c6b584bc2e)

@[9](削除ボタンを追加します)
---
@snap[midopoint north-west text-06]
### 削除
@snapend

@[45-51](削除の処理を追加します。awaitは、削除完了前に読み取られないように同期処理するために記述します)
---
@snap[midopoint north-west text-06]
### 追加
@snapend

@gist[js zoom-07](Yoosuke/736ca3d9b93cceb22f6b2754b9eaec0f)

@[11-16](追加するエリアを追加します)
@[28-30](新しくデータを取得するdata部分を追加します)
@[61-78](追加の処理を記述します)

