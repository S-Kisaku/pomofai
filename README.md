# プロジェクトの開始方法
ターミナルでdockerディレクトリにて以下のコマンドを打つ 
```
make init
```
<br>
他にも便利なショートカットがあるので docker/makefile の参照を推奨

---
# GitHub 規約
## branchについて<br>
main - このリポジトリは本番にデプロイするよう <br>
feature - ここのリポジトリで開発する<br>
enviroment - 初期の環境を保存する<br>
<br>

## commitについて
コメントの頭にコミットの分類を記載する<br>
<br>
例
```
add: ToDo機能を追加した

ToDoのCRUD機能を追加した。
UIを凝ってないので今後アップデートが必要
```
詳細の分類（他の分類を追加したい時は一声かけてくれる嬉しい）<br>
```
add:機能の追加
fix:機能の修正
delete:機能の削除
update:機能のアップデート
```
---
# 構成
- typescript : 安全性を保つためのjsの拡張言語
- next : ベースのフレームワーク
    * react-redux : react内でのstateを管理するライブラリ
        - redux-logger
        - redux-toolkit
        - redux-persist : リダイレクトしてもstateを維持するため
- material-ui : メインのcssフレームワーク
    * material-ui/core
    * material-ui/styles 
    * material-ui/icon
    * material-ui-popup-state : popupのstateを簡単に管理
- prettier : コードを綺麗に保つためのライブラリ
- eslint : コードを綺麗に保つためのライブラリ
    * eslint-config-next
    * eslint-config-prettie
---
# ディレクトリ構造

- app/src：基本的にここで作業する
    * components　: 再利用するUIをここに置く<br>
　　　　　　　  componentsディレクトリ配下の詳細は設計[Atoms design](https://qiita.com/seya/items/8814e905693f00cdade2)を参照

    * contaiers 　　 : reduxのdispatchを含むUIを個々に置く

    * firebase　　　 : firebaseのライブラリの設定などをここに置く

    * public 　　　　: iconなどの画像を置く

    * styles　　　　  : cssを個々に置く

    * utils 　　　　　: 他のディレクトリに分類されないファイルをこっこに置く

    * reducks　　　 : redux関連のファイルをここにおく<br>
                　　　　　　　　詳細は[re-ducks pattern](https://noah.plus/blog/021/)と[フォルダの作り方](https://www.slideshare.net/ayatas0623/reduxstate-129830690)を参照<br>
　　　　　　　　分かりやすいページは参考から

- app/functions：ここはfirebaseのfunctionを開発する所基本的に触らない
- docker/*

---
## 参考
---
redux <br>
- [re-ducks パターン分かりやすいやつ](https://tech.playground.style/javascript/re-ducks/)<br>
- [reduxとfirebasの連携の参考](https://qiita.com/ddpmntcpbr/items/c6e7503e0c88e363d56d)<br>
- [reduxのstate設計の参考](https://www.slideshare.net/ayatas0623/reduxstate-129830690)<br>