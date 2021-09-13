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
  <a class="box_left" href="basic5.html">
    <button class="btn bg-info">前の講義へ</button>
  </a>
  <a class="box_right" href="basic7.html">
    <button class="btn bg-info">次の講義へ</button>
  </a>
</div>

## 第6章: ループ処理

## 解説動画


### ループ処理
ループ処理とは、繰り返し同じことをする処理を言います。 ループ処理は、while文とfor文を使います。


<br/>

### while文の使い方
以下のプログラムを実行してみよう。

```
var count = 1

while(count < 10) {
    console.log(count)
    count++
}
```

以下のように条件式がtrueの場合は、繰り返し処理をします。

```
while(/*条件式*/){
  /*ループする処理*/
}
```

※条件式がずっとtrueになる場合は、無限ループになりPCがクラッシュする原因になるので気を付けましょう。


<br/>

### for文の使い方
以下のプログラムを実行してみよう。

```
for(var i=0; i<10; i++) {
    console.log(i)
}
```

処理の内容は先ほどのwhile文と同じで、表記の仕方が違うだけです。

for文は以下のように記述します。

```
for(/*初期処理*/; /*条件式*/ ;/*繰り返し処理*/){
  /*ループする処理*/
}
```

難しい場合は、以下のように覚えてしまっても大丈夫です。

```
for(var i=最初の値 ; i<最後の値 ; i++){
    console.log(i)
}
```



### 演習
①1から10までの数値を出力しなさい。

```
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


②0から10までの数値を出力しなさい。

```
0
1
2
3
4
5
6
8
9
10
```

③10から0までの数値を出力しなさい。

```
10
9
8
7
6
5
4
3
2
1
0
```

<br/>

### continueとbreak
繰り返し処理をする時、ある特定の条件だけスキップすることができます。

#### break
例えば、以下のプログラムを実行しましょう。

```
for(var i=0; i<10; i++) {
    if(i == 5)
       break; 
    console.log(i)
}
```

実行結果を見てみましょう。

```
0
1
2
3
4
```

iが5の時強制的に繰り返し処理をストップします。



#### continue
例えば、以下のプログラムを実行しましょう。

```
for(var i=0; i<10; i++) {
    if(i == 5)
       cotinue; 
    console.log(i)
```
実行結果を見てみましょう。

```
0
1
2
3
4
6
7
8
9
```

iが5の時だけ、スキップされていることがわかります。


このように、**break**や**continue**はif文と合わせて使うと、イレギュラーな処理をすることができます。


<br/>

### 演習
① 0から30の値を出力しなさい。※ただし、奇数のみ出力する（偶数の値はスキップする）。

② ①のプログラムを強制的に21まで出力したら止めるようにしてください。（21は出力する)


<br/>


#### 実践問題

世界のナベアツになろう！ 以下のプログラムを作成しなさい。


① 0から30までの数値を数える

② 3の倍数の時、「ほげ」と出力する

③ 5の倍数の時、「ふにゃ」と出力する

④ 3の倍数かつ5の倍数の時、「ほげふにゃ」と出力する


<div class="box mt mb">
  <a class="box_left" href="basic5.html">
    <button class="btn bg-info">前の講義へ</button>
  </a>
  <a class="box_right" href="basic7.html">
    <button class="btn bg-info">次の講義へ</button>
  </a>
</div>

<footer>
    <small>© 2021 k-sasaking.net</small>
</footer>
