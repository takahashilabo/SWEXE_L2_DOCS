# ソフトウェア開発演習　第２回 説明資料

## L2ディレクトリを作成して、以下を作成する

```
index.html（空ファイル）
css/style.css（空ファイル）
img/a.png（以下の画像を保存）
```
<img src="a.png">

## index.html にhtmlの基本構造を入力する

```html
<!DOCTYPE html>
<html lang="ja">
  <head>
    <meta charset="utf-8">
  </head>
  <body>
  </body>
</html>
```

## 講義資料からテキストをコピペして<body>部に流し込む

```html
ソフトウェア開発演習

授業概要
少人数の開発チームを作りWebアプリケーション開発を行う。具体的には、ソフトウェア開発のライフサイクルである要件定義、設計、実装、テストを一通り演習する。また、チーム開発に必要な開発計画、目標設定、分担決め、仕様打合せ、進捗管理などプロジェクト管理を演習する。本学科で学習してきたソフトウェア開発関連の技術を総合的に活用し、その知識をより深める機会とする。 
学習・教育目標
基本的なソフトウェア開発（要求分析・設計・プログラミング・テスト）を行うことができる。
ソフトウェア開発に必要な基本的なドキュメントを作成することができる。
チームメンバーと協調してソフトウェア開発作業を進めることができる。
基本的なプレゼンテーションの方法及び要点を知っている。
参考資料
repl.it
Ruby on Rails（本家）
Riding Rails（最新情報）
```

## <h1><h2><p>を使って装飾する

```html
<h1>ソフトウェア開発演習</h1>
<h2>授業概要</h2>
<p>少人数の開発チームを作りWebアプリケーション開発を行う。具体的には、ソフトウェア開発のライフサイクルである要件定義、設計、実装、テストを一通り演習する。また、チーム開発に必要な開発計画、目標設定、分担決め、仕様打合せ、進捗管理などプロジェクト管理を演習する。本学科で学習してきたソフトウェア開発関連の技術を総合的に活用し、その知識をより深める機会とする。</p>

<h2>学習・教育目標</h2>
<ul>
<li>基本的なソフトウェア開発（要求分析・設計・プログラミング・テスト）を行うことができる。</li>
<li>ソフトウェア開発に必要な基本的なドキュメントを作成することができる。</li>
<li>チームメンバーと協調してソフトウェア開発作業を進めることができる。</li>
<li>基本的なプレゼンテーションの方法及び要点を知っている。</li>
</ul>

<h2>参考資料</h2>
<ul>
<li>repl.it</li>
<li>Ruby on Rails（本家）</li>
<li>Riding Rails（最新情報）</li>
</ul>
```

## git add&commit

コミットメッセージは各自で考える。

## いまどきのサイトは中央寄せです

Headに以下を追記する
```html
<link href="css/style.css" rel="stylesheet">
```

全体にdivタグを追加する
```html
<div id="page></div>
```

style.cssに以下を追記する
```css
#page {
  width: 980px;
  margin: 0 auto;
}
```

## h2タグを少しそれっぽくする

style.cssに以下を追加する
```css
h2 {background-color: #FFFFCC; border-bottom: dashed 3px #555555}
```

## ２カラムにする

index.htmlに以下を追加する
```html
<div id="pageBody"></div>
<div id="pageSub"></div>
```

style.cssに以下を追加する
```css
#pageBody {
  width: 720px; float: left;
}

#pageSub {
  width: 220px; float: right;
}
```

## Footerをつける

index.htmlに以下を追加する
```html
<footer id="pageFooter"> <p id="copyright">Copyright&copy;Kindai University 2025 All rights Reserved.</p>
</footer>
```

表示がおかしいので、style.cssに以下を追加する
```css
#pageFooter {
  border-top: solid 1px #CCCCCC; text-align: center;
  clear: both;
}
```

## イメージを追加してみる（授業概要の本文のした）

```html
<img src="img/a.png">
```


## イメージを本文の右に配置したい

```html
<img src="img/a.png" class="img-right">
```

```css
.img-right { float: right; }
```

## おかしいので、<img>を本文の上に移動する

## git add&commit

コミットメッセージは各自で考える。

## ナビゲーションバーをつける。header&navを追加

```html
<header>
<nav>
<h1>ソフトウェア開発演習</h1>
<ul>
  <li><a href=".">メニュー１</a></li>
  <li><a href=".">メニュー２</a></li>
  <li><a href=".">メニュー３</a></li>
  <li><a href=".">ログイン</a></li>
</ul>
</nav>
</header>
```

## CSSを追加する

```css
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}
```

## 箇条書きが全部変わるので制限をつける

```css
nav ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}
```

## メニュー項目を横にしたい

```css
nav li {
  display: inline;
}
```

## ハイパーリンクが邪魔なので消す
```css
nav li a {
  text-decoration: none; //下線消す
}
```

## メニュー項目ごとにちょっと隙間開けようか？
```css
nav li a {
  text-decoration: none; //下線消す
  padding: 8px;
  background-color: #dddddd;
  color: #000
}
```
## ボタンらしくマウスカーソルをあてたら色変化させる
```css
nav li a:hover {
  background-color: #555;
  color: white;
}
```

## ログインボタンを右端にもっていく
```html
<li style="float:right"><a href=".">ログイン</a></li>
```

## git add&commit

コミットメッセージは各自で考える。







