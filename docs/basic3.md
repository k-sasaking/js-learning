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
  <a class="box_left" href="basic2.html">
    <button class="btn bg-info">前の講義へ</button>
  </a>
  <a class="box_right" href="basic4.html">
    <button class="btn bg-info">次の講義へ</button>
  </a>
</div>

## 第3章: 変数

### 変数

## 解説動画

<iframe width="560" height="315" src="https://www.youtube.com/embed/wW3x7zS32pQ?start=1707" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

#### 変数の特徴１
まずは、以下のプログラムを実行してみましょう。

```
var x = "私は変数です。"
console.log(x)
```

<br/>

上記のコードは、変数xに「私は変数です。」という値を**代入**しています。

「=」の記号は、右の値を左に「**代入する**」という意味です。

<br/>

さらに、x（変数）を出力すると、xの中に入っている値が出力されます。

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
<br/>

### 演習問題
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

<br/>

※ヒント：以下のコードから3つのコードを選んで実行しましょう。

```
name1 = name2
name2 = name1
var name3 = name1
var name3 = name2
name1 = name3
name2 = name3
```


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
