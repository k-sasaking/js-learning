
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
  <a class="box_left" href="game1.html">
    <button class="btn bg-info">前の講義へ</button>
  </a>
  <a class="box_right" href="game3.html">
    <button class="btn bg-info">次の講義へ</button>
  </a>
</div>

## クイズゲームを作ろう

① 元となるhtmlファイルを作成しましょう。

```

<html>
<head>
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.0/css/bootstrap.min.css" integrity="sha384-9aIt2nRpC12Uk9gS9baDl411NQApFmC26EwAOH8WgZl5MYYxFfc+NcPb1dKGj7Sk" crossorigin="anonymous">
    <script src="https://code.jquery.com/jquery-3.5.1.slim.min.js" integrity="sha384-DfXdz2htPH0lsSSs5nCTpuj/zy4C+OGpamoFVy38MVBnE+IbbVYUew+OrCXaRkfj" crossorigin="anonymous"></script>
    <script src="https://cdn.jsdelivr.net/npm/popper.js@1.16.0/dist/umd/popper.min.js" integrity="sha384-Q6E9RHvbIyZFJoft+2mJbHaEWldlvI9IOYy5n3zV9zzTtmI3UksdQRVvoxMfooAo" crossorigin="anonymous"></script>
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.0/js/bootstrap.min.js" integrity="sha384-OgVRvuATP1z7JjHLkuOU7Xw704+h835Lr+6QL9UvYjZE3Ipu6Tp75j7Bh/kR0JKI" crossorigin="anonymous"></script>
    <style type="text/css">
        body {
            background-color: #CEF;
        }
    </style>   
</head>
<body>
    <div class="text-center p-5">
        <div class="quiz">
            <h1>クラーククイズ</h1>
            <img src="clark.jpeg" height="320px"/>
            <div class="question m-5">
                <h2>問1</h2>
                <p>クラーク博士はどこの国の人？</p>
                <div class="answer">
                    <select id="q1">
                        <option value="1">イギリス</option>
                        <option value="2">アメリカ</option>
                        <option value="3">フランス</option>
                    </select>
                </div>
            </div>
            <div class="question m-5">
                <h2>問2</h2>
                <p>クラーク博士が開講した大学は？（現在の名前）</p>
                <div class="answer">
                    <select id="q2">
                        <option value="1">東北大学</option>
                        <option value="2">環太平洋大学</option>
                        <option value="3">北海道大学</option>
                    </select>
                </div>
            </div>
            <div class="question m-5">
                <h2>問3</h2>
                <p>クラーク博士のフルネームは？</p>
                <div class="answer">
                    <select id="q3">
                        <option value="1">ポール・スミス・クラーク</option>
                        <option value="2">アダム・スミス・クラーク</option>
                        <option value="3">ウィリアム・スミス・クラーク</option>
                    </select>
                </div>
            </div>
            <input class="form-control btn btn-primary" type="button" value="結果を見る" onclick="quiz()" />
        </div>
        <hr/>
        <div class="text-center">
            <p>結果</p>
            <h2 id="result"></h2>
        </div>
    </div>
</body>
<script>
function quiz(){

}
</script>
</html>
```

② 結果を見るボタンが押された時、コンソールにidがq1のvalueを出力しなさい。

③ ②と同様にidがq2とidがq3のvalueもそれぞれ出力しなさい。

④ ②と③で取得した値と答えがあっているかを判定し、正解数を計算しなさい。また正解数をコンソールに出力しなさい。

⑤ idがresultのところに正解数を表示しなさい。

２問正解でした。



<div class="box mt mb">
  <a class="box_left" href="game1.html">
    <button class="btn bg-info">前の講義へ</button>
  </a>
  <a class="box_right" href="game3.html">
    <button class="btn bg-info">次の講義へ</button>
  </a>
</div>

<footer>
    <small>© 2021 k-sasaking.net</small>
</footer>
