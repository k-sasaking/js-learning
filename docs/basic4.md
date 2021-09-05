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
  <a class="box_left" href="basic3.html">
    <button class="btn bg-info">前の講義へ</button>
  </a>
  <a class="box_right" href="basic5.html">
    <button class="btn bg-info">次の講義へ</button>
  </a>
</div>


## 第4章: 型と演算

### 型
プログラム上、データには型があります。

例えば、文字の型、数字の型...

<br/>

型を調べるには以下のコードで調べることができます。

typeof(型を調べる値)
実際にやってみよう。

```
var moji = "私は文字です。"
console.log(moji)
console.log(typeof(moji))
```

他にもいろいろな型があります。

以下の変数の方を調べてみよう。

```
var moji = "私は文字です。"
var number = 1
var bool = true
var array = [1,2,3]

console.log(typeof(moji))
console.log(typeof(number))
console.log(typeof(bool))
console.log(typeof(array))
```

#### 主な型
- number: 数字
- string: 文字
- boolean: 論理（true/false)
- object: オブジェクト型
- undefined: 型がない

※オブジェクト型は、あるデータ構造を持った特殊な型です。

オブジェクト型以外の型をプリミティブ型と呼びます。


<br/>


#### 動的型付けと静的型付け
Javascriptの言語は、型を自動で判別してくれます。このような仕組みを「動的型付け」と言います。

しかし、プログラミング言語の中には、Javaのように、どの型の変数かを宣言しないとつかえない言語もあります。 このような仕組みを「静的型付け」と言います。

この場合、例えば文字の型に数字を入れるとエラーになります。

<br/>

以下のプログラムを実行してみましょう。

```
var hensu = "私の型は何？"
console.log(typeof(hensu))
hensu = 1
console.log(typeof(hensu))
```



### 演算
プログラムは、算数同様に演算をすることができます。

いろいろな演算方法を学びましょう。

以下のプログラム実行しましょう。

```
var a = 10
var b = 5

console.log(a + b)
console.log(a - b)
console.log(a * b)
console.log(a / b)
console.log(a % b)
console.log(a ** b)
```


#### 主な演算子
- 足し算: +
- 引き算: -
- 掛け算: *
- 割り算: /
- 剰余: %
- べき乗: **




#### その他の演算方法
演算の書き方もいろいろな書き方があります。

以下のプログラムを実行してみましょう。

```
var num = 10
num += 5
console.log(num)
```

以下の２つのコードは同じ処理をします。

```
num = num + 5

num += 5
```



以下のプログラムを実行しましょう。

```
var num = 10
num++
console.log(num)
```

以下の２つのコードは同じ処理をします。

```
num = num + 1

num++
```

この++のことを**インクリメント**といいます。






#### 文字列の演算

文字も＋の演算のみ使うことができます。

```
var moji = "私の名前は"
var name = "Tom"
var moji2 = "です。"

console.log(moji + name +moji2)
```



#### 文字と数値の足し算はどうなる？
以下のプログラムを実行してみましょう。

```
var moji = "10"
var num = 5

console.log(num + moji)
```

この結果から分かる通り、文字列と数値の足し算は、文字列になります。

演習
```
var num1 = 100
var num2 = 3
var moji3 = "7"
var moji4 = "5"


console.log(/*ここに処理を追加*/)
console.log(/*ここに処理を追加*/)
console.log(/*ここに処理を追加*/)
console.log(/*ここに処理を追加*/)
console.log(/*ここに処理を追加*/)
console.log(/*ここに処理を追加*/)
console.log(/*ここに処理を追加*/)
```

結果

```
103
97
300
1
57
777
37
```


<div class="box mt mb">
  <a class="box_left" href="basic3.html">
    <button class="btn bg-info">前の講義へ</button>
  </a>
  <a class="box_right" href="basic5.html">
    <button class="btn bg-info">次の講義へ</button>
  </a>
</div>

<footer>
    <small>© 2021 k-sasaking.net</small>
</footer>
