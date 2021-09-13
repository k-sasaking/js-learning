# Javascript講座 DOM編

## 第3章: クリックイベント

## クリックイベント
ボタンがクリックされた時の動作について学びます。

## alert機能
まずは、以下のjavascriptをscriptタグに記載しましょう。

```
function buttonClick(){
    alert('クリックされました')
}

buttonClick()
```

ページの再読み込みを押すと、アラートが表示されます。

これは、buttonClick関数を実行した際に、以下のコードで呼び出されています。

```
    alert('クリックされました')
```


<br/>

## クリックイベントの定義
それでは、上記のjavascriptのコードを以下のように変更して、実行しましょう。

```
function buttonClick(){
    alert('クリックされました')
}

var button1 = document.getElementById('button1')
console.dir(button1)

// クリックイベントを追加
button1.addEventListener('click', buttonClick)
```

これは、button1の情報にaddEventListenerによって、イベントを追加しています。


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
