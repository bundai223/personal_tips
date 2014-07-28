andeoid Layoutのtips
============

## PreferenceActivityのレイアウト指定
 1. extends PreferenceActivityしたクラスを用意。（今ならPreferenceFragment）
 2. setContentViewでカスタムLayoutを指定する。
     @Override
     public void onCreate(){ setContentView(testResId); }
 3. この時setContentViewするレイアウトの中に  
    android:id="@android:id/list"属性を持つListViewが必要

## Preferences用のxmlファイルで文字列型以外の指定の仕方
```xml
    <resources>
        <bool name="mypreference_default">true</bool>
    </resources>
```

Use the value in the preferences.xml  
```xml
    <CheckBoxPreference
        android:defaultValue="@bool/mypreference_default"
        android:key="mypreference"
        android:title="@string/mypreference_title" />
```

```java:test.java
private void Hoge() {
}
```
