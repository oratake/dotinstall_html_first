# HTML入門
dotinstallを用いた言語学習  
最初は[HTML入門](https://dotinstall.com/lessons/basic_html_v4)から  

HTMLはテキスト平文でも表示されるが、適切にタグで**マークアップ**することで、意味をもたせたり、CSSでデザインをする等できる。  
【マークアップ】タグによってブラウザが識別できるよう、意味づけすること。  

## 主なタグ
`<h1></h1>` 見出し(1〜7)  
`<p></p>` 平文(パラグラフ)  
`<img>` 画像タグ  

【属性】タグの中で指定するもの  
例：imgタグ  
`<img src="./file/path.jpg" width="140" height="140" alt="タイトル画像">`  
imgタグの**alt属性**は自動読み上げ等で読まれるので、意味のないもの以外は**必ず指定**し、端的でわかりやすいものにする。  

## マークアップの基本構成(HTML5)
```html
<!DOCTYPE html><!-- html5である宣言 -->
<html lang="ja"><!-- langで言語を宣言 -->
  <head><!-- headタグでhtmlについて各種宣言 -->
    <meta charset="utf-8"><!-- 文字コードの設定。特に何もなければutf-8、指定でs-jis等ある場合注意 -->
    <title>ページ名 | サイト名</title><!-- ページタイトル -->
    <link rel="icon" href="./fabicon.ico"><!-- ファビコンの指定 -->
    <meta name="description" content="竹中の練習サイトです"><!-- このhtmlについての説明 -->
  </head>
  <body><!-- 文章はbodyタグに -->
    <img src="./img/path.jpg" alt="画像説明">
    <h1>見出し</h1>
    <p>文章</p>
  </body>
</html>
```
※適切なインデント(スペースではなくハードタブ)で見やすくする。

---

学習中
