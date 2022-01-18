
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
  <a class="box_left" href="game2.html">
    <button class="btn bg-info">前の講義へ</button>
  </a>
  <a class="box_right" href="game4.html">
    <button class="btn bg-info">次の講義へ</button>
  </a>
</div>

## ジャンケンゲームを作ろう
ジャンケンゲーム

「グー」「チョキ」「パー」のボタンを押したら、ジャンケンの結果を表示する。

成果物イメージ

難易度: ★★★★☆

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
        body {background-color: #CFC;}
    </style>   
</head>
<body>
    <div class="p-5 text-center">
        <h1>ジャンケンゲーム</h1>
        <p>ジャンケンをしましょう</p>
        <img src="janken.jpeg" height="320px"/>
        <div class="p-5">
            <select id="hand" class="form-control">
                <option value="0">グー</option>
                <option value="1">チョキ</option>
                <option value="2">パー</option>
            </select>
            <input class="btn btn-primary form-control mt-5" type="button" value="ジャンケンをする" onclick="janken()"/>
        </div>
        <hr/>
        <p>結果</p>
        <div>
            <p id="cp"></p>
            <h2 id="result"></p>
        </div>
    </div>
</body>
<script>
function janken(){
    
}
</script>
</html>
```

② 「グー」「チョキ」「パー」の配列を作りなさい。また、ジャンケンをするボタンが押された時、「グー」を表示しなさい。

③ ジャンケンをするボタンが押された時、ランダムで「グー」「チョキ」「パー」を表示しなさい。

④ ジャンケンをするボタンが押された時、select boxの値を取得し、コンソールに表示しなさい。

⑤ ジャンケンをするボタンが押された時、id="cp"のタグに、CPの手（ランダムにグー、チョキ、パーのどれか）を表示しなさい。

「CPの手はチョキです。」

⑥ ジャンケンの勝敗を計算し、idがresultのところに結果を表示しなさい。

「あなたの勝ち」



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
