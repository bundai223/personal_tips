Gitのtips
============

## いろいろまとめたサンプル
https://github.com/bundai223/dotfiles/blob/master/.gitconfig 

## ブランチ
### 一覧
+ ローカル
        git branch
+ リモート
        git branch -r

### 作成
+ リモートから取得しつつ作成
        git checkout -b [branch_name] [remote_branch_name]

+ リモートへpush

### 削除
+ ローカル
        git branch -D [branch_name]
+ リモート
        git push [remote_name] :[branch_name]

### 取り消し
+ リモート戻し
        git push -f origin HEAD~:master  
**危険な操作** リモートで他の人が操作している可能性がある。

## tag
### 作成
+ 説明なし
        git tag [tag_name]
+ 説明付き
        git tag -a [tag_name]

### 一覧
+ 名前のみ
        git tag
+ 説明付き
        git tag -n

+ リモート
        git ls-remote --tags [(参考)][remote]

### 削除
    git tag -d [tag_name]

### リモートへタグ追加
    git push origin [tag_namee]

・[tag追記予定](http://at-aka.blogspot.jp/2009/02/git.html)

## pushしていないコミットの差分
    git log [remote_name]/[branch_name]..[branch_name]

## [git logに変更したファイルも表示][log_withfile]
    git log --stat
    git whatchanged

## [指定の関数のみのlog・diffを表示][log_func]
    git log -L :[regex]:[file]

##  リポジトリの情報
###  表示
    git config -l
###  remoteのurl表示
    git remote -v
    git config -l|grep url
###  remoteの追加・変更
    git remote set-url [remote_name] [url(ex: git@git.example.com:foo/bar.git)]

## 一時的な変更の退避・適用
[stash いろいろ便利][stash_exp]

### 一度適用したstashの取り消し
    git stash show stash@{n} -p | git apply -R

## コマンド一覧
### リポジトリの作成およびメンテナンスに利用するコマンド
    git init	リポジトリを作成する
    git clone	既存のリポジトリの複製を作る
    git fsck	リポジトリの正当性チェックを行う
    git gc	リポジトリ内の不要なオブジェクトを削除し、最適化を行う
### 作業ツリーやブランチを操作・管理するコマンド
    git status	変更が加えられたファイルを表示する
    git diff	ファイルに加えられた変更点をdiff形式で表示する
    git add	コミットするファイルを指定する
    git commit	変更点をコミットする
    git log	コミットログを閲覧する
    git reset	直前のコミットを取り消す
    git revert	作業ツリーを指定したコミット時点の状態にまで戻す
    git branch	ブランチ情報の表示およびブランチの作成
    git checkout	ブランチの切り替え
    git show-branch	ブランチの作成/変更/マージ履歴を表示
    git merge	ローカルブランチのマージを行う
    git tag	コミットにタグを付ける
    git stash	現在の作業ツリーの状態を一時的に保管する
    git rebase	ブランチの派生元（上流）を変更する
### ほかのリポジトリとの連携を行うコマンド
    git pull	ほかのリポジトリの変更点をローカルリポジトリにマージする
    git push	公開リポジトリに自分のリポジトリの内容を送信する

<!-- URL -->
[remote]: http://renoiv.com/2012/08/06/git%E3%81%AE%E3%82%BF%E3%82%B0%E6%93%8D%E4%BD%9C%E3%82%B3%E3%83%9E%E3%83%B3%E3%83%89%E3%81%BE%E3%81%A8%E3%82%81/
[log_withfile]: http://yuroyoro.hatenablog.com/entry/20101008/1286531851
[log_func]: http://daretoku-unix.blogspot.jp/2014/02/gitgit-log-l.html?spref=tw
[stash_exp]: http://qiita.com/fukajun/items/41288806e4733cb9c342
