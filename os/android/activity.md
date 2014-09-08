# ActivityへのTips
###startActivityForResult を使うなら、以下の条件をすべて満たす必要がある。
* 起動元のアクティビティの luanchMode は standard、singleTop、singleTask のいずれか。
* 起動先のアクティビティの launchMode は standard、singleTop のどちらか。
* 起動時のインテントに Intent.FLAG_ACTIVITY_NEW_TASK フラグを付けない。
