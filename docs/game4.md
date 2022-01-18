
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

# Javascript講座 GAME編

<div class="box mb">
  <a class="box_left" href="game3.html">
    <button class="btn bg-info">前の講義へ</button>
  </a>
</div>

## ハングマンゲームを作ろう
ハングマンゲーム

三つのアルファベットの単語を当てるゲーム。

A〜Zのアルファベットのどの文字が含まれているかを当てます。

6回間違えるとゲームオーバー。6回以内に当てられればクリア。


難易度: ★★★★★



作り方
① 元となるhtmlファイルを作成しましょう。

```

<html>
<head>
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.0/css/bootstrap.min.css" integrity="sha384-9aIt2nRpC12Uk9gS9baDl411NQApFmC26EwAOH8WgZl5MYYxFfc+NcPb1dKGj7Sk" crossorigin="anonymous">
    <script src="https://code.jquery.com/jquery-3.5.1.slim.min.js" integrity="sha384-DfXdz2htPH0lsSSs5nCTpuj/zy4C+OGpamoFVy38MVBnE+IbbVYUew+OrCXaRkfj" crossorigin="anonymous"></script>
    <script src="https://cdn.jsdelivr.net/npm/popper.js@1.16.0/dist/umd/popper.min.js" integrity="sha384-Q6E9RHvbIyZFJoft+2mJbHaEWldlvI9IOYy5n3zV9zzTtmI3UksdQRVvoxMfooAo" crossorigin="anonymous"></script>
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.0/js/bootstrap.min.js" integrity="sha384-OgVRvuATP1z7JjHLkuOU7Xw704+h835Lr+6QL9UvYjZE3Ipu6Tp75j7Bh/kR0JKI" crossorigin="anonymous"></script>
    <style type="text/css">
        body {background-color: #FEC;}
    </style>   
</head>
<body>
<div  class="text-center">
    <div class="uranai-question">
        <h1>ハングマンゲーム</h1>
        <img src="img/hangman.png" height="320px"/>
        <h2 id="display">_ _ _</h2>
        <p id="turn">残り6回ミスしても良い</p>
        <input type="button" value="A" onclick="btnClick('A')">
        <input type="button" value="B" onclick="btnClick('B')">
        <input type="button" value="C" onclick="btnClick('C')">
        <input type="button" value="D" onclick="btnClick('D')">
        <input type="button" value="E" onclick="btnClick('E')">
        <input type="button" value="F" onclick="btnClick('F')">
        <input type="button" value="G" onclick="btnClick('G')">
        <input type="button" value="H" onclick="btnClick('H')">
        <input type="button" value="I" onclick="btnClick('I')">
        <input type="button" value="J" onclick="btnClick('J')">
        <input type="button" value="K" onclick="btnClick('K')">
        <input type="button" value="L" onclick="btnClick('L')">
        <input type="button" value="M" onclick="btnClick('M')">
        <input type="button" value="N" onclick="btnClick('N')">
        <input type="button" value="O" onclick="btnClick('O')">
        <input type="button" value="P" onclick="btnClick('P')">
        <input type="button" value="Q" onclick="btnClick('Q')">
        <input type="button" value="R" onclick="btnClick('R')">
        <input type="button" value="S" onclick="btnClick('S')">
        <input type="button" value="T" onclick="btnClick('T')">
        <input type="button" value="U" onclick="btnClick('U')">
        <input type="button" value="V" onclick="btnClick('V')">
        <input type="button" value="W" onclick="btnClick('W')">
        <input type="button" value="X" onclick="btnClick('X')">
        <input type="button" value="Y" onclick="btnClick('Y')">
        <input type="button" value="Z" onclick="btnClick('Z')">
        </div>
    </div>
    <script>
        var word = "CAT"; // 答えの単語
        var answer = "_ _ _"; // 問題文（虫食い）
        var faildCount = 0; // 失敗の数をカウント
        function btnClick(char) {
          
            if(char == "C"){
                answer = "C" + answer.slice(1, 6);
            }
            else if(char == "A"){
                answer = answer.slice(0, 2) + "A" + answer.slice(3, 6);
            }
            else if(char == "T"){
                answer = answer.slice(0, 4) + "T";
            }
            else {
                faildCount++;
            }
            document.getElementById("turn").innerHTML = "残り" + (6 - faildCount) + "回ミスしても良い";
            document.getElementById("display").innerHTML = answer;
            if(answer == "C A T"){
                alert("クリア！！")
            }
            if(faildCount >= 6){
                alert("ゲームオーバー");
            }
        }
    </script>
</body>
</html>
```

② Cがクリックされた時、「Cがクリックされました」とalertを出す。

③ ②と同様に、A,Tがクリックされた時、alertを出す。

④ C,A,T以外が押された時、faildCountを+1する。

⑤ 残り何回ミスをしても良いかをid=turnの要素を取得し、表示する。

⑥ Cがクリックされた時以下のコードを追加する。

```
answer = "C" + answer.slice(1, 6);
```

⑦ Aがクリックされた時、以下のコードを追加する。

```

```

⑧ Tがクリックされた時、以下のコードを追加する。

```

```

⑨ 全部のアルファベットが当たった時、「クリア」とalertを表示する。

⑩ 失敗が6回以上の場合は、「ゲームオーバー」とalertを表示する。

その他追加機能

- 問題を複数用意してランダムに表示する

- 一度押されたボタンは押されましたと表示する




<div class="box mt mb">
  <a class="box_left" href="game2.html">
    <button class="btn bg-info">前の講義へ</button>
  </a>
  <a class="box_right" href="game4.html">
    <button class="btn bg-info">次の講義へ</button>
  </a>
</div>

<footer>
    <small>© 2021 k-sasaking.net</small>
</footer>
