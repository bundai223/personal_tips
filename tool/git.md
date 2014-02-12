Gitのtips
========================================

#gitブランチ
ローカル：git branch
リモート：git branch -r

# ブランチ削除
ローカルブランチ：git branch -D <branch_name>
リモートブランチ：git push <remote> :<branch_name>

#git pushしていないコミットの差分
masterの場合 : git log origin/master..master

#git logに変更したファイルも表示
http://yuroyoro.hatenablog.com/entry/20101008/1286531851
・git log --stat
・git whatchanged




