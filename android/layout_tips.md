andeoid Layoutのtips
============

## PreferenceActivityのレイアウト指定
 1. extends PreferenceActivityしたクラスを用意。（今ならPreferenceFragment）
 2. setContentViewでカスタムLayoutを指定する。
     @Override
     public void onCreate(){ setContentView(testResId); }
 3. この時setContentViewするレイアウトの中に  
    android:id="@android:id/list"属性を持つListViewが必要
