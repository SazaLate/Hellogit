# gitの使い方

## GitHubにリポジトリを作る（リモートリポジトリ）

## ローカル環境にリポジトリを作る（ローカルリポジトリ）

$ mkdir github 
$ cd github 
$ mkdir gittest 
$ cd gittest 
$ git init 

## GitHubにデータを送信する（リモートリポジトリにデータをプッシュする）

### 1）ローカルリポジトリを作成する
$ git init

### 2）ローカルリポジトリにファイルの変更点を追加（インデックスに追加）
$ git add ファイル名

### 3）ローカルリポジトリにインデックスに追加したファイルを登録
$ git commit -m "変更点などのコメント"

### 4）追加したインデックス（ファイルの変更点など）をGitHubに作成
$ git remote add origin リポジトリのURI

### 5）ローカルリポジトリのファイルをGitHubのリポジトリに送信
$ git push origin master

## プッシュしたデータを変更・更新してみる

### 1）変更をインデックスに追加
$ git add test.txt

### 2）ファイルを登録（コミット）
$ git commit -m "変更してみたよ"

### 3）データの送信
$ git push origin master

## ブランチ（枝）とは？

### 用語説明
#### マージ
「結合する」という意味．
複数に分岐させた物をつなぎます

#### ブランチ
その名の通り「枝」．
一気にバージョンを上げる時などに，失敗した時用にコピーを作っておくイメージ

## 実際にブランチを作ってみる

### 1）新しいブランチを作る
$ git branch ブランチ名

### 2）今あるブランチを確認する
$ git branch

### 3）ブランチを移動する
$ git checkout ブランチ名

### 4）ブランチを結合（マージ）する
※$ git checkoutで，結合したいブランチに移動して…
$ git merge 取り込むブランチ名