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

# Javascript講座 DOM編

<div class="box mb">
  <a class="box_left" href="dom2.html">
    <button class="btn bg-info">前の講義へ</button>
  </a>
  <a class="box_right" href="game1.html">
    <button class="btn bg-info">次の講義へ</button>
  </a>
</div>

# Javascript講座 DOM編

## 第3章: イベントと機能

本章ではJavascriptでかける様々なイベントや機能について紹介します。

## alert機能
まずは、以下のjavascriptをscriptタグに記載しましょう。

```
alert('ページが読み込まれました')
```


ページの再読み込みを押すと、アラートが表示されます。


## confirm機能
まずは、以下のjavascriptをscriptタグに記載しましょう。

```
confirm('ページを読み込みますか？')
```

すると、「キャンセル」と「OK」ボタンが出てきました。

　<br/>

「OK」を押されたときに、alertを実行したい場合は、以下のようなプログラムで実行できます。

```
if(confirm('ページを読み込みますか？')){
    alert('OKが押されました！')
}
```

confirmで**OKを押すと、confirm関数が"true"**を返します。

よって、if文の条件式にconfirmを入れることで、OKが押された時の処理をすることができます。

**キャンセルを押したときは、"false"**を返します。

<br/>

## クリックイベントの定義
まずは、alert機能を実行する関数を定義してみましょう。

```
function buttonClick(){
    alert('クリックされました')
}

buttonClick();
```

上記の関数は、buttonClickという関数が実行されたときに、alertを表示します。

<br/>

それでは、上記のjavascriptのコードを以下のように変更して、実行しましょう。

```
function buttonClick(){
    alert('クリックされました')
}

var button1 = document.getElementById('button1')

// クリックイベントを追加
button1.addEventListener('click', buttonClick)
```

これは、button1の情報に**addEventListener**によって、イベントを追加しています。


<br/>

## addEventListenerの使い方
以下のように指定することができます。

```
ノード.addEventListener('イベント名', 関数名)
```

下記のコードでは、

```
button1.addEventListener('click', buttonClick)
```

button1がclickされた際、buttonClick関数を実行するという意味になります。


## 他のイベント
イベントはclick以外にも以下のようなイベントもあります。

- mousemove: マウスカーソルが要素に移動した時
- keypress: キーが押された時
- change: 要素が変更された時
- focus: フォーカスが要素に移動した時




##  演習
① button2のvalueをコンソールに出力しなさい。

② alertで"button2がクリックされました"と表示する関数を定義しなさい。（関数名は、button2Click）

③ button2がクリックされた時、button2Click関数を呼びなさい。

④ button2クリックが押された時、alertの文字を"pタグの文字"に変更しなさい。

⑤ button2がクリックされた時、alertの文字をpタグ(idがtest)のテキスト情報が出るようにしなさい。

⑥ button2がクリックされた時、pタグのテキストを"ボタンが押されました！"に変更しなさい。

⑦ button2がクリックされた時、textbox1のテキストを取得し、alertに表示しなさい。

⑧ button2がクリックされた時、textbox1のテキストをpタグの値に書き換えなさい。


<div class="box mt mb">
  <a class="box_left" href="dom2.html">
    <button class="btn bg-info">前の講義へ</button>
  </a>
  <a class="box_right" href="game1.html">
    <button class="btn bg-info">次の講義へ</button>
  </a>
</div>

<footer>
    <small>© 2021 k-sasaking.net</small>
</footer>
