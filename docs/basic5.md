<style>
.mb {
  margin-bottom: 90px;
}
.mt {
  margin-top: 90px;
}
.box {
  position: relative;
}
.box .box_left {
  position: absolute;
  left: 0;
}
.box .box_right {
  position: absolute;
  right: 0;
}
.btn {
  padding: 6px 12px;
  border-radius: 7em;
  border: solid 1px #ccc;
}
.bg-info {
  background-color: #00a651;
  color: #ffffff;
}
footer {
    text-align: center;
    margin-top: 120px;
    padding: 30px;
}
</style>


# [Javascript講座 基礎編](basic.html)

<div class="box mb">
  <a class="box_left" href="basic4.html">
    <button class="btn bg-info">前の講義へ</button>
  </a>
  <a class="box_right" href="basic6.html">
    <button class="btn bg-info">次の講義へ</button>
  </a>
</div>

## 第5章: 条件分岐

## 解説動画
<iframe width="560" height="315" src="https://www.youtube.com/embed/wW3x7zS32pQ?start=4391" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### 条件分岐

条件分岐とは、例えば、ジャンケンで「勝ち」「負け」の時にそれぞれ違う処理をするなど、
ある条件によって処理が分岐することを言います。

<br/>

**条件分岐**は、**if文**を使って書くことができます。

### if文の使い方
以下のプログラムを実行してみましょう。

```
var age = 10


if(age == 10){
   console.log("あなたは10才です。")
}
```

実行すると、以下のような結果が得られました。

```
あなたは10才です。
```

続いて、ageの値を20に変えて実行してみましょう。

すると、何も表示されません。

```

```

<br/>

以下のようにif文を使うことである特定の条件を満たした時のみ処理をすることができます。

```
if (/* 条件式 */) {

 /* 処理 */
}
```

<br/>

### 条件式
条件式は、その条件が○か×かを判断する式です。

○の時をtrue,×の時をfalseといいます。

<table>
<tr><th>演算子</th><th>意味</th></tr>
<tr><td>a==b</td><td>aとbの値が同じの時true</td></tr>
<tr><td>a&lt;b</td><td>aがbより小さい時true</td></tr>
<tr><td>a&gt;b</td><td>aがbより大きい時true</td></tr>
<tr><td>a&lt;=b</td><td>aがb以下の時true</td></tr>
<tr><td>a&gt;=b</td><td>aがbより以上の時true</td></tr>
<tr><td>a!=b</td><td>aとbが異なる値の時true</td></tr>
</table>

<br/>

### if-else文
if文は条件式がtrueの時に処理をしました。

条件式がfalseの時に処理をする場合は、else文を使います。

以下のプログラムを実行してみましょう。

```
var age = 30

if(age < 20){
   console.log("あなたは未成年です")
}
else {
   console.log("あなたは大人です")
}
```
実行すると、以下のような結果が得られました。

```
あなたは大人です
```

ageの値を10にして実行してみましょう。

```
あなたは未成年です
```

このように、ifの条件以外の場合、処理を行います。

```
if (/* 条件式 */) {

 /* trueの時の処理 */
}
else {
 /* falseの時の処理 */
}
```

<br/>

### ３つ以上の分岐
例えば、上記のプログラムを以下のようにしたい場合、

- ageが20未満の時は、未成年
- ageが20の時は、成人
- それ以外の時は、大人

と表示する。

以下のように書くことができます。

```
var age = 20

if(age< 20){
   console.log("あなたは未成年です")
}
else if(age == 20){
   console.log("あなたは成人です")
}
else {
   console.log("あなたは大人です")
}
```

実行すると以下のような結果が出ます。

```
あなたは成人です。
```

ageの値を変えて実行してみよう。

- ageが10の時
```
あなたは未成年です
```

- ageが30の時

```
あなたは大人です
```


<br/>

このようにelse ifを使えば、３つ以上の分岐処理もすることができます。

```
if (/* 条件式A */) {

 /* 条件式Aがtrueの時の処理 */
}
else if (/* 条件式B */) {

 /* 条件式Bがtrueの時の処理 */
}
else if (/* 条件式C */) {

 /* 条件式Cがtrueの時の処理 */
}
else {
 /* 条件に当てはまらなかった時の処理 */
}
```

※else ifは何個も加えることができます。


#### else ifの注意点
以下のプログラムを実行してみましょう。

```
var age = 25

if(age >= 10){
   console.log("あなたは10代です")
}
else if(age >=20){
   console.log("あなたは20代です")
}
```

結果は、以下のようになりました。

```
あなたは10代です
```

これは、「age >= 10」「age >= 20」の両方を満たしますが、
最初のif文が実行されていることがわかります。

このように、複数の条件式を作るときは、上のものが優先されるので、条件を書く順番には気を付けましょう。


<br/>

### 複数の条件式の組み合わせ
条件式は組み合わせて使うことができます。

<table>
<tr><th>演算子</th><th>意味</th></tr>
<tr><td>条件式A && 条件式B</td><td>条件式Aと条件式Bが両方trueの時、true</td></tr>
<tr><td>条件式A || 条件式B</td><td>条件式Aか条件式Bのどちらかがtrueの時、true</td></tr>
<tr><td>!(条件式A)</td><td>条件式Aを満たさない時、true</td></tr>
</table>

以下のプログラムを実行しましょう。

```
var age = 21

if(age < 20 || age >= 30){
   console.log("あなたは20歳未満もしくは30才以上です")
}
else if(age >=20 && age < 30){
   console.log("あなたは20代です")
}

if (!(age == 20)){
   console.log("あなたは20才ではありません")
}
```

ageの値を変えてプログラムを動かしてみよう。


<br/>


### 演習
①以下のプログラムを作成しなさい。

- dayが0の時、"日曜日"
- dayが1の時、"土曜日"
- dayが６以下の時、"平日"
- それ以外、"不明"

```
var day =  3

/* ここにプログラムを記載 */

```


② 以下のプログラムを作成しなさい。

- xが偶数の場合、偶数です。
- xが奇数の場合、奇数です。

```
var x = 6

/* ここにプログラムを記載 */

```


③ 以下のプログラムを作成しなさい。

- (a)xが0未満かつyが0未満の場合、"掛け算をしたら正になります。"と表示する
- (b)xかyどちらか0未満の場合は、掛け算をしたら負になります。"と表示する
- (c)それ以外の時は、"掛け算をしたら正になります。"と表示する

```
var x = 10
var y = -10

/*ここに処理を記載*/

```


<div class="box mt mb">
  <a class="box_left" href="basic4.html">
    <button class="btn bg-info">前の講義へ</button>
  </a>
  <a class="box_right" href="basic6.html">
    <button class="btn bg-info">次の講義へ</button>
  </a>
</div>

<footer>
    <small>© 2021 k-sasaking.net</small>
</footer>
