# STEP1 初動の手順
リポジトリの複製 or 新規作成が始まり大抵は複製が良いかも

## リポジトリ用のディレクトリ作成
`mkdir ~/git/vim`
`cd ~/git/vim`

## リモートリポジトリを複製する
`git clone [URL]`  
master の / がカレントに入る  
指定したディレクトリのみ複製する  
  → 要研究。少なくとも階層は短縮不可。  
  → kaggle環境はシンボリックリンクで解決した

## ローカルリポジトリを作成する (.git作成)
`git init`

## ローカルリポジトリを削除する
rm -rf ./.git があるディレクトリ  
特にgitコマンド使わず、削除してOK

## ユーザ情報を登録する
これが完了しないとgit commitできない  
ただし、git clone した場合は不要

`git config --global user.email "yuyuyu@aa"`
`git config --global user.name "yuyuyu"`

## SSH公開鍵登録
gitユーザーでssh認証しないとNG (ハマった)

# STEP2 リモートリポジトリの準備
git clone すると、originで自動登録される  
ローカルとリモートは同じディレクトリ構成にする

## リモートリポジトリを登録する
`git remote add vim https://github.com/yuyuyu0706/vim.git`

## リモートリポジトリを削除する
`git remote rm vim`

## リモートリポジトリを確認する
`git remote -v`

## リモートリポジトリ名を変更する
`git remote rename origin kaggle`

## リモートリポジトリ設定を変更する
`git remote set-url kaggle git@github.com:ID/リポ名`  
HTTPでcloneしたリポジトリをSSHに変更した  
別リポジトリに切り替える場合も同じ

# STEP3 コミット手順
.git を持つディレクトリで実行すること  
.git を持つパス配下がリポジトリ管理されている

## ローカルリポジトリのステージングに登録する
`git add hello.html`

## ローカルリポジトリのステージングを全消し
`git reset HEAD`

## ローカルリポジトリにステータスを確認する
`git status`

## ローカルリポジトリでコミットする
`git commit -am "Update"`  
  -a 変更ファイル全てコミット  
  -m コメントをつける

## リモートリポジトリに変更を反映する
（branch名=masterの場合)  
`git push vim master`

## リモートリポジトリの変更を確認する
`git fetch vim`
`git diff vim/master`

## リモートリポジトリの変更を取り込む
（branch名=master)
`git pull vim master`


# その他
## コミット履歴を参照する  
`git log -n 10`

[参考]
https://techacademy.jp/magazine/6235

# WEB操作手順
## ディレクトリ作成
http://maeokaka.hatenablog.jp/entry/2016/07/07/001441

## ファイルアップロード
https://qiita.com/yoichiro6642/items/727a581486af281853e7


```python

```
