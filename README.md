# 03_javascript-basic

2023 年 後期 「JavaScript 基礎」授業課題

##　授業内コード

1. 10 月 5 日（木）はじめの一歩
2. 10 月 5 日（木）git 側から入力

##10 月 19 日

addEventListener でイベント
setAttribute で属性、値の操作

<html lang="ja">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>イベントハンドラを登録演習 ②</title>
    <style>
      .redText {
        color: red;
      }
      .bigText {
        font-size: 25px;
      }
    </style>
  </head>
  <body>
    <p>
      <span>JavaScript</span
      >（ジャバスクリプト）とは、プログラミング言語のひとつである。
    </p>
    <button class="redder">赤くなる</button>
    <button class="bigger">大きくなる</button>

    <script>
      const btnRed = document.querySelector(".redder");
      const btnBig = document.querySelector(".bigger");

      const jsText = document.querySelector("p span");

      //クラスを付与してスタイルの適用
      btnRed.addEventListener("click", function () {
        jsText.setAttribute("class", "redText");
      });

      btnBig.addEventListener("click", function () {
        jsText.setAttribute("class", "bigText");
      });
    </script>

  </body>
</html>

## 10 月 19 日

for 文と配列を使ってリストに要素を追加する

    <script>
      for (let i = 0; i < 4; i++) {
        console.log(i);
      }

      const name_list = ["松田", "田中", "中山", "山本", "本田"];

      for (let i = 0; i < name_list.length; i++) {
        console.log(i + 1 + "人目は" + name_list[i]);
      }
    </script>

  </body>
</html>

    <h1>人気フルーツ一覧</h1>
    <ul id="fruitslist" class="listbox__list"></ul>
    <script>
      const fruits = ["りんご", "もも", "バナナ"];
      const elment = document.querySelector("#fruitslist");
      console.log(fruits);
      console.log(elment);

      for (let i = 0; i < fruits.length; i++) {
        const lilast = document.createElement("li");
        lilast.innerHTML = fruits[i];
        elment.appendChild(lilast);
      }
    </script>

## 10 月 12 日

1.文字列の結合

      console.log("トライ\nデント"); //文字列リテラル　\nで改行
      console.log(123); //数値リテラル
      console.log(123.4);
      console.log(`トライデントコンピュータ専門学校
      Webデザイン学科`);

      console.log("ABC" + "DEF"); //文字列の結合
      console.log("円周率は" + 3.14 + "です。"); //文字列 + 数値

      console.log("計算結果" + 123 + 456); //文字列　+　数値の計算
      console.log(123 + 456 + "となりました。"); //数値の計算 + 文字列
      console.log("計算結果：" + (123 + 456));
      console.log("2" - 1); //文字列 - 数値
      console.log(2 * "5");
      console.log(3 ** "4");
      console.log("13" % 4);

2.変数

      //変数の宣言,代入
      let a; //変数宣言
      a = 10; //値の代入
      console.log(a);
      a = "Hello";
      console.log(a);

      let b = "world";
      console.log(b);

      const pi = 3.14;
      console.log(pi);
      // pi = 314; constで宣言されると再代入できない

      //複合演算子
      let n = 5;
      n = n + 2;
      console.log(n);

      let m = 5;
      m += 2; //m = m + 2 と同じ
      console.log(m);

      //インクリメント
      m++; // m = m +1 と同じ
      console.log(m);

3.html の操作

  <body>
    <h1>果物の種類</h1>
    <ul id="fruitslist" class="listbox__list">
      <li>りんご</li>
      <li>みかん</li>
      <li>バナナ</li>
    </ul>
    <!--リストを操作するDOM操作のスクリプト-->
    <script>
      //メロンを追加

      //ulタグの取得
      const element = document.querySelector("ul");
      console.log(element);

      //idやclassで取得
      const element2 = document.querySelector("#fruitslist");
      console.log(element2);

      const element3 = document.querySelector(".listbox__list");
      console.log(element3);

      //新しくliタグの要素を追加
      const liLast = document.createElement("li");
      console.dir(liLast);
      liLast.textContent = "メロン";
      console.log(liLast);

      //リストの最後の子要素として追加
      element.appendChild(liLast);

      //スタイルの変更
      liLast.style.color = "green";
      console.log(liLast.style.color);
    </script>

  </body>

## 10 月 5 日

- インターネットの基本について理解する。
- Web の基本的な仕組みを理解する。
- Web サーバーの役割について理解する。
- 開発環境の構築
- JavaScript を書く場所

### JavaScript を書く場所

1. HTML ファイルの中
1. 外部 JS ファイルの中
1. ブラウザのコンソール

基本は、外部 JS ファイルを読み込むが、HTML 内に各場合は、`</body>`の上に書く。

```html
<!doctype html>
<html lang=ja>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>演習</title>
</head>
<body>
</script>
</body>
</html>
```

### フロントエンドロードマップ

フロントエンドエンジニアに必要なスキルの[ロードマップ](https://roadmap.sh/frontend)がある。
