Gitの使い方
===========


## 新規にローカルリポジトリ作成する
    git init  
    
## 管理するファイルを追加する
    git add ファイル  
    
## ファイルを削除
    git rm ファイル  
    
## 変更など、現在の状態を確認する
    git status  
    
## 管理するファイルを追加する
    git commit -m "[Prefix]コメント"  
    
#### Prefix簡易版
Prefix  | 概要
------------- | -------------
add  | 追加
fix  | バグを修正
update  | （バグではない）変更、更新  
remove  | 削除  




## GitHubにてリモートリポジトリを作成する
    Create a New Repository 

## リモート名「origin」とリモートURLを関連付ける
    git remote add origin https://github.com/aoisan/hello-world.git  
    
## 設定を確認する
    git remote -v  
    
## プッシュして、ローカルリポジトリをリモートリポジトリ「master」に反映
    git push origin master  
    
### 注意
リモートリポジトリを後に作成すると、リモートとローカルが関連のない別々のものとなるため、  
マージがデフォルトでエラーとなる。  
その場合、`--allow-unrelated-histories`オプションを指定する。  
    git merge --allow-unrelated-histories master  

## 変更など、現在の状態を確認する
    git status  
    
## リモートリポジトリから複製して開発する
    git clone https://github.com/aoisan/hello-world.git  
    
## 確認のため、ブランチ一覧を表示する
    git branch
    
## 開発用ブランチを作成する
    git branch develop  
    
## 開発用ブランチへ移動する
    git checkout develop  
    
## ファイルを編集し、コミットする

## add後、最新コミットとの差分を確認する
    git diff --cached
    
## リモートリポジトリを確認
    git remote -v  

## フェッチして、リモートリポジトリが変更されていないか確認する
#### まだローカルには反映されない。
    git fetch https://github.com/aoisan/hello-world.git  
    
    
## プルして最新のリモートリポジトリ「master」をローカルリポジトリ「master」に反映させる
    git pull origin master  
    
## ローカル内の開発用ブランチをメインブランチへマージする
#### まず、メインへ移動  
    git checkout master  
    
#### メインへ移動後、開発用ブランチをメインへマージ   
    git merge develop  

## プッシュして、ローカル「master」の変更をリモートリポジトリに反映する
    git push origin master  
    
    
## 不必要なブランチを削除する
    git branch -d develop  


