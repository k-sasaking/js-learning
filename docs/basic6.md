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

### ループ処理
ループ処理とは、繰り返し同じことをする処理を言います。 ループ処理は、while文とfor文を使います。




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
for(var count=1; count<10; count++) {
    console.log(count)
}
```

処理の内容は先ほどのwhile文と同じで、表記の仕方が違うだけです。

for文は以下のように記述します。

```
for(/*初期処理*/; /*条件式*/ ;/*繰り返し処理*/){
  /*ループする処理*/
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


③0から30までの偶数を出力しなさい。

```
0
2
4
6
8
10
12
14
16
18
20
22
24
26
28
30
```


④10から0までの数値を出力しなさい。

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


### continueとbreak
繰り返し処理をする時、ある特定の条件だけスキップすることができます。

#### break
例えば、以下のプログラムを実行しましょう。

```
for(var count=1; count<10; count++) {
    if(count == 5)
       break; 
    console.log(count)
}
```

countが5の時強制的に繰り返し処理をストップします。



#### continue
例えば、以下のプログラムを実行しましょう。

```
for(var count=1; count<10; count++) {
    if(count == 5)
       continue; 
    console.log(count)
}
```

countが5の時だけ、スキップすることができます。

breakやcontinueはif文と合わせて使うと、このように、いろいろなことができます。



<br/>

### 演習
① 0から30の値を出力しなさい。ただし、奇数のみ出力する。

② ①のプログラムを強制的に21まで出力したら止めるようにしてください。（21は出力する)





#### 応用演習問題

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
