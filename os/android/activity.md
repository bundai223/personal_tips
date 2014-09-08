# ActivityへのTips
###startActivityForResult を使うなら、以下の条件をすべて満たす必要がある。
* 起動元のアクティビティの luanchMode は standard、singleTop、singleTask のいずれか。
* 起動先のアクティビティの launchMode は standard、singleTop のどちらか。
* 起動時のインテントに Intent.FLAG_ACTIVITY_NEW_TASK フラグを付けない。

###アプリに終了処理を組込むには
    ルートActivity が決まっている場合、 Intent.FLAG_ACTIVITY_CLEAR_TOP フラグをつけ、その Activity を開始する。
    Extras に exitキー を true で追加するなどで終了する旨を表現し、ルートActivity ではその値を見て finish() を実行する。
