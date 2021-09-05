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
  <a class="box_left" href="basic1.html">
    <button class="btn bg-info">前の講義へ</button>
  </a>
  <a class="box_right" href="basic3.html">
    <button class="btn bg-info">次の講義へ</button>
  </a>
</div>

## 第2章: コンソール表示とコメント

### コンソール表示

以下のコードを実行してみよう。

```
console.log("Hello Javascript!!")
```

<br/>

すると画面に以下のように出力されます。

```
Hello Javascript!!
```

<br/>

このように、文字を出力したい場合は、

```
console.log("表示したい文字")
```

を利用します。

<br/>

実務では、エラーが起きたときにメッセージを表示したり、処理の途中経過を実行されているか確認するために出力します。


<br/>


### コメントの表示
以下のプログラムを実行しましょう。

```
console.log("Hello Javascript1")

//console.log("Hello Javascript2")

console.log("Hello Javascript3")

/*
console.log("Hello Javascript4")
console.log("Hello Javascript5")
*/
```

<br/>

実行してみると、以下のような結果が出力されます。

```
Hello Javascript1
Hello Javascript3
```

<br/>

コメントで記載された場所は、表示されていないことがわかります。

<br/>

このようにコメントは、以下の２つの書き方があります。

- １行のコメント //
- 複数行のコメント /* */

<br/>

実務では、コードを説明するときや不要になったコードを一時的に読み込ませないようにするときに使用します。


### 演習
「自分の名前」を出力してみましょう。

```
〇〇 〇〇
```



<div class="box mt mb">
  <a class="box_left" href="basic1.html">
    <button class="btn bg-info">前の講義へ</button>
  </a>
  <a class="box_right" href="basic3.html">
    <button class="btn bg-info">次の講義へ</button>
  </a>
</div>

<footer>
    <small>© 2021 k-sasaking.net</small>
</footer>
