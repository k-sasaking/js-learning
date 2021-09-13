# Javascript講座 DOM編

## 第2章: Webの仕組みとDOM


### HTMLにJavascriptを埋め込む
ここからは、実際にHTMLファイルにJavascriptを埋め込んで、実行します。

javascriptのコードは一般的には、bodyタグの下に、scriptタグを設けて、コードを書くことができます。

実際に、追加をしてみましょう。

```
<html>
<head>
  <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">

  <title>タイトル</title>
  <style>
  </style>
</head>
<body>
  <div class="m-5">
    <h1 id="hello">Hello HTML!!</h1>
    <p id="test">idを指定した段落です。</p>
    <div class="m-5">
        <input id="textbox1" class="textbox form-control" type="text" value="テキストボックス1"/>
        <input class="textbox form-control" type="text" value="テキストボックス2"/>
        <input class="textbox form-control" type="text" value="テキストボックス3"/>
        <input id="button1" class="btn btn-primary form-control" type="button" value="クリックしてね！" />
        <input id="button2" class="btn btn-danger form-control" type="button" value="クリックしてね！" />
    </div>
  </div>
<script>
  console.log("hello world!!")
  console.log("hello world!!")
  console.log("hello world!!")
</script>
<script src="https://code.jquery.com/jquery-3.3.1.slim.min.js" integrity="sha384-q8i/X+965DzO0rT7abK41JStQIAqVgRVzpbzo5smXKp4YfRvH+8abtTE1Pi6jizo" crossorigin="anonymous"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.7/umd/popper.min.js" integrity="sha384-UO2eT0CpHqdSJQ6hJty5KVphtPhzWj9WO1clHTMGa3JDZwrnQq4sF86dIHNDz0W1" crossorigin="anonymous"></script>
<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/js/bootstrap.min.js" integrity="sha384-JjSmVgyd0p3pXB1rRibZUAYoIIy6OrQ6VrjIEaFf/nJGzIxFDsf4x0xIM+B07jRM" crossorigin="anonymous"></script>
</body>
</html>
```

### コンソールの文字の確認方法
コンソールの文字をブラウザで確認します。

- 右クリックを押して、「検証」
- consoleタブをクリック
- hello world!!と3回表示されていたら大丈夫です。

## DOMの取得
scriptタグ内を以下のように変更しましょう。

```
<script>
console.dir(document)
</script>
```

実行すると、最初にやったdocumentのモデルが表示されます。

## idのノードを取得
ここからは、DOMからpタグの情報を取得します。

scriptタグを以下のように変更しましょう。

```
<script>
var p = document.getElementById("test")
console.dir(p)
</script>
```

するとコンソールにp#testという情報が表示されます。

この情報をノードと言います。

idがtestのノードを開くといろいろな情報が記載されているのが確認できます。


<br/>


## ノードからpタグのテキストを取得
上記のコードでpタグのノードが取得できました。

ここからは、pタグのテキスト情報をjavascriptで取得します。

pタグのノードの中にinnerTextの値がテキストの情報になります。

よって、以下のようにコードを書くことで、コンソールに出力します。

```
var p = document.getElementById("test")
console.dir(p)
console.dir(p.innerText)
```

このように、pタグのinnerTextを取得したい場合は、

```
p.innerText
```

と指定することで取得することができます。


<br/>


## 演習
①h1タグのテキスト情報を コンソールに出力しなさい。


<br/>


## ノードの書き換え
上記で取得したpタグinnerTextの値をjavascriptのコードを使って変更します。

```
var p = document.getElementById("test")
console.dir(p)

p.innerText = "pタグを変更しました。"
```

<br/>


## 演習
① h1タグのテキストを"h1タグの要素を変えました"と変更しなさい。

② idがtextbox1のノードを取得してコンソールに出力しなさい。

③ idがtextbox1のテキストボックスの文字をコンソールに出力しなさい。

④ idがtextbox1のテキストボックスの文字を"textboxの文字を変えました。"とjavascriptで書き換えなさい。



