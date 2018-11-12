# HTML入門
dotinstallを用いた言語学習  
最初は[HTML入門](https://dotinstall.com/lessons/basic_html_v4)から  

HTMLはテキスト平文でも表示されるが、適切にタグで**マークアップ**することで、意味をもたせたり、CSSでデザインをする等できる。  
【マークアップ】タグによってブラウザが識別できるよう、意味づけすること。  

## 主な書き方、要素
### 要素
`<!DOCTYPE html>` html5で作成されてあるという宣言  
`<head>` html文書のヘッダ要素を記入していく  
`<meta>` メタタグ 文字コードやhtml文書の説明などに用いる  
`<body>` 実際にブラウザに表示される領域  
`<header>` タイトル見出しやナビバーなど、ヘッダに当たる部分を示す  
`<nav>` ナビバー部分を示す  
`<section>` 文書の区切りを示す  
`<h1>` 見出し(1〜7)  
`<p>` 平文(パラグラフ)  
`<a>` アンカータグ 主にリンクで使用される  
`<img>` 画像タグ  
`<ol>, <ul>, <li>` リストタグ(詳しくは下記の「リスト」項で)
`<!-- ここに書く -->` コメント ※ブラウザでは表示されないが、ソースコードとしては見えてしまうので注意。  

### alt属性
【属性】タグの中で指定するもの  
ex) imgタグ  
`<img src="./file/path.jpg" width="140" height="140" alt="タイトル画像">`  
- imgタグの**alt属性**は意味のないもの以外は**必ず指定**し、端的でわかりやすいものにする。  
  - 意味のない画像にも`alt=""`と記述する。  
  - 検索エンジンに画像の詳細を把握させる意味あり  
  - 画像が表示できない際に代替としてテキストが表示される
  - 画像からリンクを張る際に、

### head と header
`<head>`と`<header>`タグがあるが、  
headはhtml文書全体の情報を記述するところ、  
headerはブラウザで見えている範囲でヘッダー的な要素が入る。  

### リスト
`<ol>` Orderd List 連番リスト  
`<ul>` Unorderd List 非連番(箇条書き)リスト  
このどちらかで囲った中に、  
`<li>` List Item  
をほしい分だけ入れる。  
ex)
```html
<ol>
  <li><img src="なんや" alt="かんや"></li>
  <li><img src="なんでん" alt="かんでん"></li>
  <li><img src="hoge" alt="piyo"></li>
</ol>
```
※上記のように、リスト状に要素を並べる際にはliで囲って使ったりもする。  

また、`<dl>, <dt>, <dd>` を使い、情報をひとまとまりにする「定義リスト」も作れる。  
ex)  
```html
<dl>
  <dt>
    項目(description term)
  </dt>
  <dd>
    内容or説明(discription, definition)
  </dd>
</dl>
```

### リンク
`<a href="./open/your/link">` アンカータグを用いてリンクを作成できる。  
他要素を囲ってまるごとリンクにできたりする。  
ex) `<a href=""><li>リストまるごと</li></a>`  
- メールリンク  
メールもaタグでリンクを張る。  
ex) `<a href="mailto:example@mail.address">`
- 電話番号のリンク  
`href="tel:電話番号をいれる"` tel:に続けて電話番号でリンクを張れる  
- target属性  
`target="_blank"` 新規タブで開く  

## マークアップの基本構成(HTML5)
```html
<!DOCTYPE html>
<html lang="ja"><!-- langで言語を宣言 -->
  <head><!-- headタグでhtmlについて各種宣言 -->
    <meta charset="utf-8"><!-- 文字コードの設定。特に何もなければutf-8、指定でs-jis等ある場合注意 -->
    <title>ページ名 | サイト名</title><!-- ページタイトル -->
    <link rel="icon" href="./fabicon.ico"><!-- ファビコンの指定 -->
    <meta name="description" content="竹中の練習サイトです"><!-- このhtmlについての説明 -->
  </head>
  <body><!-- 文章はbodyタグに -->
    <header>
      <nav><!-- ナビゲーション部分 -->
        <!-- ul, li などでリストを入れたりする -->
      </nav>
    </header>
    
    <section><!-- 内容のひとまとまりをsectionで区切る -->
      <img src="./img/path.jpg" alt="画像説明">
      <h1>見出し</h1>
      <p>文章</p>
    </section>
    
    <footer>
      <p>著作権表示など</p>
    </footer>
  </body>
</html>
```
- 適切なインデント(スペースではなくハードタブ)で見やすくすること
  弊社ではタブ幅は4に指定のこと。
- divを使用した場合
  弊社では閉じタグに右のようにメモをつける`<!-- /class名,/id名 -->`

## HTMLの仕様
[MDN (Mozilla Developer Network)](https://developer.mozilla.org/ja/)  
こちらを参照のこと。仕様については、  
1. 会社のコーディング規約
1. MDN  
で確認しながらマークアップする。  

---

HTML入門 終了
