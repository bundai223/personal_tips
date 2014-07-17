# EspressoのTips

### ユーザー目線でのテスト
    Activityがなんだ・Fragmentの状態が…などではなく、どういうViewが画面にでているか？どのViewをタップするか？など
    画面の見た目に基づくテストを記述する感じ。

### 画面遷移ではなく、単画面・単Activity・単FragmentでのUIの単体テスト的に使用するツール？
    ？？？

### APIは独特だが一定のルールで書いていけるのできれいだと思う。
    Espresso.onView(ViewMatchers.withId(R.id.viewId)).perform(ViewAction.click());
    Espresso.onView(ViewMatchers.withId(R.id.viewId)).check(ViewAssertions.matches(ViewMatchers.isDisplayed()));

### 画面を跨ぐテスト用ではなさそう。
    APIから推測するにActivityの遷移を考慮したAPIではない。（Activity・FragmentをチェックするAPIはない）
    一応、それぞれで固有な表示のViewを確認することでチェックできるけれどidの被りなどを考えると不確実。

### すべて逐次処理されていくのでUIのアニメーション待ち、通信を待ってUI表示などがやり辛い。
    APIにアニメーション・通信などを待つ処理がない。
    実装するとすればThread.sleep(millisec)・別スレッドで待機する処理を自作するしかないよう。
    アニメーションは、端末の設定でOffにできるが通信待ちは待機処理を入れる必要がある。
    これは結構厳しいと思う。
