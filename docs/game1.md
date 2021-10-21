
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
  <a class="box_left" href="dom3.html">
    <button class="btn bg-info">前の講義へ</button>
  </a>
  <a class="box_right" href="game2.html">
    <button class="btn bg-info">次の講義へ</button>
  </a>
</div>

## 占いゲーム

ボタンを押したら、「大吉」「中吉」「小吉」「吉」「末吉」「凶」「大凶」のいずれかの結果が出てくる。

成果物イメージ

難易度: ★☆☆☆☆

### 作り方
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
            <h1>⭐︎占い⭐︎</h1>
            <img src="uranai.jpeg" height="320px"/>
            <p>今日の運勢を占いましょう</p>
            <input type="button" value="占う" onclick="uranai()"/>
        </div>
        <hr/>
        <div class="uranai-result">
            <p>結果</p>
            <h2 id="result"></h2>
            <p id="message"></p>
        </div>
    </div>
</body>
<script>
function uranai(){

}
</script>
</html>
```

② 占い結果を配列で定義しましょう。

③ 0から6のいずれかが出る乱数を作りましょう。

④ 占うボタンが押された時、コンソールに、ランダムで占い結果を表示しよう。

⑥ idがresultのh2タグに占い結果を表示しましょう。

⑦ ⑥のやり方で、占いの結果に対するメッセージを持つ配列を追加し、占い結果と同時にidがmessageのpタグにメッセージを表示しましょう。

大吉なら => おめでとう！！

大凶なら => 残念...

<div class="box mt mb">
  <a class="box_left" href="dom3.html">
    <button class="btn bg-info">前の講義へ</button>
  </a>
  <a class="box_right" href="game2.html">
    <button class="btn bg-info">次の講義へ</button>
  </a>
</div>

<footer>
    <small>© 2021 k-sasaking.net</small>
</footer>

