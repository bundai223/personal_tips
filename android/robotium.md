# RobotiumのTips

### Fragmentはtag指定で待機することしかできない。  
    →Fragmentのtagはクラス名などで固定したい（無理な場合もなるだけSuffixなどで対処）
    調べるのがかなり面倒なため。

### 画面遷移待ちがめんどうかも。  
    なんらかのViewを対象にwaitForViewすればいいっぽい。
    アニメーション待ちとか？

### UIの操作（TextView::setTextなど）がめんどう。  
    robotiumのThreadから操作するとExceptionが吐かれてしまう。runToUiThread(Runnable)関数を介して実行する必要がある。

### Intentで別のアプリを呼びだす箇所は対処を考える必要あり。
    Intentでアプリのリストを表示している箇所の処理は自動でテストする手段がわからない。

### UIを直接操作する関数がSolo（robotiumで主に使用する便利機能まとめたクラス）にあるが、viewを指定する方法に違和感がある。
    ViewをIndex、Stringで指定して操作する。
    同じIDのViewを複数生成できるためだと思うが、どっちにしろ不都合がある気がする。
    ID指定でも問題ないケースが多いと思うので欲しい。



