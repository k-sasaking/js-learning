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
  <a class="box_left" href="basic2.html">
    <button class="btn bg-info">前の講義へ</button>
  </a>
  <a class="box_right" href="basic4.html">
    <button class="btn bg-info">次の講義へ</button>
  </a>
</div>

## 第3章: 変数

### 変数

#### 変数の特徴１
まずは、以下のプログラムを実行してみましょう。

```
var hensu = "私は変数です。"
console.log(hensu)
```

このように変数は、値を保持することができます。

使い方は以下の通りです。

```
var 変数名 = 値
```

<br/>

#### 変数の特徴２
続いて、以下のプログラムを実行してみましょう。

```
var hensu = "私は変数です。"
hensu = "私は本当に変数ですよ！"
console.log(hensu)
```

値を変更することができます。


<br/>


#### 変数の特徴３
変数に変数の値を入れることができる。

```
var name1 = "私はTomです。"
var name2 = "私はAnnです。"
var name3 = name1

console.log(name1)
console.log(name2)
console.log(name3)
```

<br/>

#### 演習問題
① 以下のプログラムを変更し、結果と同じになるように処理を追加しなさい。

```
var name1 = "私はTomです。"
var name2 = "私はAnnです。"
var whoAmI = "私は誰？"

/* ここに処理を1行追加 */

console.log(whoAmI)

/* ここに処理を1行追加 */

console.log(whoAmI)
```

結果

```
私はTomです。
私はAnnです。
```

<br/>

② 以下のプログラムを変更し、結果と同じになるように処理を追加しなさい。

```
var name1 = "私はTomです。"
var name2 = "私はAnnです。"

/* ここに処理を3行追加 */

console.log(name1)
console.log(name2)
```

結果

```
私はAnnです。
私はTomです。
```



### 変数の新しい記法
Javascriptでは、変数の書き方が２つあります。

- varを使うやり方
- letを使うやり方

簡単に言うと、varを使うやり方は古いです。

letを使うやり方は新しいです。

#### letの使い方
varと同様に使うことができます。

```
let hensu = "私は変数です。"
hensu = "私は本当に変数ですよ！"
console.log(hensu)
```

### 変数と定数
なぜ、varからletに変わったのか？ それは、「変数」と「定数」を区別するためです。

- 変数は、値がコロコロ変えることができます。
- 定数は、値を変えることができません。

varを使う時代は、変数と定数の区別がなかった。

letは、let(変数)とconst(定数)を区別して使う必要があります。

### 定数
なぜ、変数と定数を区別する必要があるか？

それは、大きく３つのメリットがあります。

- メモリの消費を抑える
- バグを減らす
- 可読性

定数を変えるとどうなる？

```
const teisu = "私は定数です。"
teisu = "定数を変えます"
console.log(teisu)
```

以下のようなエラーが起きたらOK

```
TypeError: Assignment to constant variable.
```

実務での使いどころ。

絶対に変えて欲しくない値を定数にすることが多いです。

例えば、消費税の税率、制限文字数など...


<div class="box mt mb">
  <a class="box_left" href="basic2.html">
    <button class="btn bg-info">前の講義へ</button>
  </a>
  <a class="box_right" href="basic4.html">
    <button class="btn bg-info">次の講義へ</button>
  </a>
</div>

<footer>
    <small>© 2021 k-sasaking.net</small>
</footer>
