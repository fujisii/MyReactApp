# [ドットインストール]React入門

## #01 Reactを使ってみよう

## #02 開発の準備を整えよう

### ローカル開発環境の構築

1. Chromeの拡張機能である「[React Developer Tools](https://chrome.google.com/webstore/detail/react-developer-tools/fmkadmapgofadopljbjfkapdkoienihi/related?ctx=DEblog20052011&hl=ja)」をインストールする
1. React Developer Tools > 右クリック > 拡張機能を管理 をクリックする
1. 「ファイルのURLヘのアクセスを許可する」をONにする
1. 準備OK

### Reactのスクリプトを読み込む

1. [公式サイト > Docs > Try React > Online Playgrounds](https://reactjs.org/docs/getting-started.html#online-playgrounds)にアクセスする
1. 「download this HTML file」をクリックする
1. 以下のスクリプトをコピーしてファイルに貼り付ける

```html
    <script src="https://unpkg.com/react@16/umd/react.development.js"></script>
    <script src="https://unpkg.com/react-dom@16/umd/react-dom.development.js"></script>

    <!-- Don't use this in production: -->
    <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
```

## #03 はじめてのReact

## #04 JSXを使ってみよう

- JSXで渡せる要素は1つだけであることに注意する
- 複数の要素を渡したい場合は、配列にしてあげるか、もしくは親要素を作ればOK

  ```html
  <div>
    <p>Hello</p>
    <p>World</p>
  </div>
  ```

- それから閉じタグがないようなタグには注意が必要
  - 例：hrタグ
  - JSXはXMLが元になっているので、閉じタグがないタブの場合は、最後に必ず「/」でタグを閉じる必要あり

  ```html
  <hr/>
  ```

## #05 属性やイベントを扱ってみよう

- JSXではHTMLの属性も使うことができるが、属性によっては注意が必要
- classは新しいJavaScriptでは予約後なのでclassNameとしないといけない

  ```html
  <div className="box"></div>
  ```

- style属性で指定することもできる
- style属性にはオブジェクト形式で渡す必要がある
- 一旦波括弧をつけたあとにその中にオブジェクトなので...二重波括弧のようなかたちになる
- プロパティのpxは省略できる
- 属性はcamelCaseで書く必要がある

  ```html
  <div style={{width:100, height:100, backgroundColor:'tomato'}}></div>
  ```

- 関数は波括弧だけで書いてあげる必要がある

  ```html
  <div style={{width:100, height:100, backgroundColor:'tomato'}} onClick={showMessage}></div>
  ```

## #06 Componentを作ってみよう

- Componentの名前の1文字目は必ず大文字にすること

  ```html
  <Counter/>
  ```

- Componentの内容はほとんど同じだけど少しだけ変えたいという場合には、Componentに属性をつけてあげればOK

  ```html
  <div>
    <Counter color="tomato"/>
    <Counter color="skyblue"/>
    <Counter color="limegreen"/>
  </div>
  ```

- Componentで値を受け取るには、引数を指定してあげればOK
- ちなみに以下のpropsは、読み取り専用の値という点に注意する

  ```javascript
  function Counter(props) {
    return <div>0 {props.color}</div>
  }
  ```

## #07 Propsを使ってみよう

## #08 スタイルを整えよう

## #09 イベントの仕組みを理解しよう

- 関数に引数を渡したい場合は、無名関数を onClick に渡してあげる必要がある
