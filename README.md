# 03_javascript-basic

2023 年 後期 「JavaScript 基礎」授業課題

##　授業内コード

1. 10 月 5 日（木）はじめの一歩
2. 10 月 5 日（木）git 側から入力

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
