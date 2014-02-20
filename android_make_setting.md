Androidのプロダクトをビルドするためのantの設定
==============================

0. 各プロジェクトに build.xml を置く。それぞれ規定のものを未編集のままでOK
1. 環境変数で ANDROID_HOME をandroid-sdk のパスに設定する。  
    windows: ユーザー環境変数に設定。  
    mac: ログイン時に以下を実行するようにする。  
        /bin/launchctl setenv ANDROID_HOME /path/to/android-sdk
    ログイン時にshellスクリプトを実行するのは、Automator でシェルスクリプトを実行するアプリケーションを作成し、  
    一度dockに登録、オプション→ログイン時に実行にチェックを付ける。(チェックしたあとはドックから削除してもOK)

2. コマンドラインから ant release しても、eclipse から build.xml を実行してもどちらでも OK

