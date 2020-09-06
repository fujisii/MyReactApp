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
