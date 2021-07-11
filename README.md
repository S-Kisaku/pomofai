# MenStack.ts

## 構成

### パッケージ
- typescript : 安全性を保つためのjsの拡張言語
- next : ベースのフレームワーク
    * next-firebase-auth [githubレポジトリ](https://github.com/gladly-team/next-firebase-auth)
    * react-redux : react内でのstateを管理するライブラリ
        - redux-logger
        - redux-toolkit
- material-ui : メインのcssフレームワーク
    * material-ui/core
    * material-ui/styles 
    * material-ui/icon
    * material-ui-popup-state：popupのstateを簡単に管理
- prettier : コードを綺麗に保つためのライブラリ
- eslint : コードを綺麗に保つためのライブラリ
    * eslint-config-next
    * eslint-config-prettie

### ディレクトリ構造
- componentsは[Atoms design](https://qiita.com/seya/items/8814e905693f00cdade2)を適用
- reduxは[re-ducks](https://noah.plus/blog/021/)を適用

### 設計
- reduxのstate設計の[参考](https://www.slideshare.net/ayatas0623/reduxstate-129830690)

### 参考

- [re-ducks pattern](https://qiita.com/ddpmntcpbr/items/c6e7503e0c88e363d56d)
- [createAsyncの参考](https://qiita.com/puku0x/items/4217ca9f98fad82bc998)
- [datepicker](https://material-ui-pickers.dev/demo/datepicker)