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
    margin-top: 90px;
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

### 条件分岐
条件分岐とは、例えばスイッチがONの時とOFFの時で違う処理をするときに使います。



条件分岐は、if文を使います。

if文の使い方
以下のプログラムを実行してみましょう。

```
var age = 10

console.log("年齢を確認します。")

if(age == 10){
   console.log("あなたは10才です。")
}
```

続いて、ageの値を20に変えて実行してみましょう。


<br/>

以下のようにif文を使うことである特定の条件を満たした時のみ処理をすることができます。

```
if (/* 条件式 */) {

 /* 処理 */
}
```


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


### if-else文
if文は条件式がtrueの時に処理をしました。

条件式がfalseの時に処理をする場合は、else文を使います。

以下のプログラムを実行してみましょう。

```
var age = 30


if(age< 20){
   console.log("あなたは子供です")
}
else {
   console.log("あなたは大人です")
}
```

ageの値を10にして実行してみましょう。

このように、ifの条件以外の場合、処理を行います。

```
if (/* 条件式 */) {

 /* trueの時の処理 */
}
else {
 /* falseの時の処理 */
}
```



### ３つ以上の分岐
例えば、上記のプログラムを以下のようにしたい場合、

- ageが20未満の時は、子供
- ageが20の時は、成人
- それ以外の時は、大人

と表示する。

以下のように書くことができます。

```
var age = 20


if(age< 20){
   console.log("あなたは子供です")
}
else if(age == 20){
   console.log("あなたは成人です")
}
else {
   console.log("あなたは大人です")
}
```

ageの値を変えて実行してみよう。

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




#### else ifの注意点
以下のプログラムはどちらが表示される？

```
var age = 21


if(age >= 10){
   console.log("あなたは10代です")
}
else if(age >=20){
   console.log("あなたは20代です")
}
```

実行してもらうと分かる通り、 どちらの条件にも当てはまる場合は、上の条件式が優先されます。

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


if(age < 10 || age >= 30){
   console.log("あなたは10代もしくは30才以上です")
}
else if(age >=20 && age < 30){
   console.log("あなたは20代です")
}

if (!(age == 20)){
   console.log("あなたは20才ではありません")
}
```

ageの値を変えてプログラムを動かしてみよう。





### 演習
①以下のプログラムを作成しなさい。

- dayが0の時、"日曜日"
- dayが1の時、"月曜日"
- dayが2の時、"火曜日"
- dayが3の時、"水曜日"
- dayが4の時、"木曜日"
- dayが5の時、"金曜日"
- dayが6の時、"土曜日"
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

④ ③のプログラムのaとcの条件式を１つにまとめなさい。


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
