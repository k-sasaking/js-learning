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
  <a class="box_left" href="basic6.html">
    <button class="btn bg-info">前の講義へ</button>
  </a>
  <a class="box_right" href="dom1.html">
    <button class="btn bg-info">次の講義へ</button>
  </a>
</div>

## 第7章: 関数

## 解説動画
<iframe width="560" height="315" src="https://www.youtube.com/embed/s0CCJYDQkpA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### 関数
関数は、ある処理をまとめる時に使用します。

例えば、以下のプログラムを実行してみましょう。

```
// 関数の定義
function greeting(){
    console.log("おはよう")
    console.log("今日も一日頑張ろう！")
}

// 関数の呼び出し
greeting()
greeting()
greeting()
```

このように、関数は、複数の処理をfunctionで１つにまとめる（定義する）ことで、何回も呼び出して使うことができます。

<br/>

関数を定義する時は、好きな関数名をつけることができます。

```
function /*関数名*/ (){
   /*まとめる処理*/
}
```

関数を呼び出す際は、関数名に()をつけることで関数を実行します。

```
関数名()
```

<br/>

### 引数
関数はとても便利で、例えば、計算をする際、以下のように同じような処理をします。

```
var apple = 100
var orange = 200

//りんごを1個買った代金
console.log(apple+"円です")

//オレンジを1個買った代金
console.log(orange+"円です")

//りんごを20個買った代金
console.log(apple*20+"円です")
```

その場合、引数を使うことでより汎用的な関数を作ることができます。

上記のプログラムを関数を使って表すと以下のようになります。

```
function  printTotal(total) {
    console.log(total+"円です")
}

var apple = 100
var orange = 200

printTotal(apple)
printTotal(orange)
printTotal(apple*10)
```

引数を使うことで、関数に値を渡すことができます。

呼び出し側は、()内に渡す値を入れます。

```
printTotal(100)
```
すると、functionの()の変数にその値が代入されます。

```
function printTotal(total){  //←totalが100になる

}
```


### 演習
上記のプログラムに、以下の変数を追加し、banana３本の合計金額を出力しなさい。

```
var banana = 300
```


### 複数の引数
引数は、複数定義することも可能です。

以下のようにプログラムを実行してみましょう。

```
function  printTotal(price, amount) {
    console.log(price*amount+"円です")
}

var apple = 100
var orange = 200

printTotal(apple, 1)
printTotal(orange, 1)
printTotal(apple, 10)
```



### 戻り値
関数は、処理した値の結果を返す戻り値という機能があります。

以下の関数を実行してみましょう。

```
function greeting (){
   return "おはよう"
}

var g =  greeting()
console.log(g)
```
greetingの関数のreturnに書かれている文字が、変数gに入っていることがわかります。

このように、関数内にreturnを書くことで、戻り値を設定できます。



引数と戻り値を使うと以下のような関数も作ることができます。

```
function add(a,b){
   return a+b
}

var result = add(10,5)
console.log(result)
```



### 演習
① 入力値の２倍の値を返す関数calcを作りなさい。

```
function calc(num){
/* ここに記載する*/

}

var val1 = calc(5);
var val2 = calc(100);
console.log(val1);
console.log(val2);
```
結果

```
10
200
```


② ２つの値を平均する関数aveを作りなさい。

```
/* ここに関数を定義 */

var result = ave(100, 300)
console.log(result)
```

結果

```
200
```


③ 入力値をtimeとして、

- timeが8から10の時は「おはよう」
- timeが10から17の時は「こんにちは」
- timeが18から23の時は「こんばんは」
- それ以外の時は「...」 と出力する関数greetingを作りなさい。

```
/* ここに関数を定義 */

console.log(greeting(10))
```

④ ２つの値の間の数値を連続出力する関数rangeを作りなさい。

```
/* ここに関数を定義 */

range(0,10)
```

結果

```
0
1
2
3
4
5
6
7
8
9
10
```


<div class="box mt mb">
  <a class="box_left" href="basic6.html">
    <button class="btn bg-info">前の講義へ</button>
  </a>
  <a class="box_right" href="dom1.html">
    <button class="btn bg-info">次の講義へ</button>
  </a>
</div>

<footer>
    <small>© 2021 k-sasaking.net</small>
</footer>
