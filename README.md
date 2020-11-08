# github-pagesのサンプル

## 作成された GitHub Pages(静的ページ)

[ReactチュートリアルをGitHub Pagesで公開](https://yuki-arch.github.io/github-pages/)

## 参考にさせて頂いたURL

[10分でできる！GitHub Pagesで静的サイトを公開する方法](https://tadaken3.hatenablog.jp/entry/github-pages)

## メモランダム

### reactチュートリアルを作成する

[チュートリアル：React の導入](https://ja.reactjs.org/tutorial/tutorial.html)

```bash
$ npx create-react-app my-app
$ cd my-app
$ cd src
$ rm -f *
$ cd ..
```

### アプリの作成

- チュートリアルに従ってReacアプリを作成する
- .gitignoreを修正
    - GitHub Pagesの公開に利用するdocs/を追加
- package.jsonを修正

```json
{
    ... snipped ...
    "scripts": {
    "start": "react-scripts start",
    "build": "react-scripts build && rm -rf docs && mv build docs",
    ... snipped ...
  },
  "homepage": "https://yuki-arch.github.io/github-pages/"
}
```

- github setttingでGitHub Pagesの設定を実施
    - develop（またはmaster)ブランチのdocsフォルダを公開するように設定
- reactのコマンド
    - npm start
    - npm run develop
- GitHub Pagesで公開するためのgitコマンド
    - git add .
    - git commit -m "コメント"
    - git push
