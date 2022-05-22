## 5/22 Navigation transitions Search Color

- navigation をアニメーションさせることで、画面同士の関係を表現することができる
  - 言葉を使わずとも、View の動きでその関係を表現できるって冷静にすごいことだよな
- Search
  - Persistent search
    - サーチがアプリのメインアクションの時に使用する
    - map アプリの上部に表示されてる検索のやつ
  - Expandable search
    - サーチがアプリのメインアクションではない時に使う
      - 通常はサーチは隠れてて、タップすることで初めて表示されえる
- The color system
  - Principles
    - Hierarchical
    - Legible
    - Expressive
- 

## 5/21 Understanding navigation

- バックキーと upward を押下した時の挙動は別々で定義されてるんだな
- 画面遷移しても、リストのスクロールポジションを保持するようにする
- navigation transitions の種類
  - Hierarchical transitions
    - 親子関係が存在する
  - Peer transitions
    - 同じレベルで画面遷移が起きること
  - Top-level transitions
    - bottom navigation bar で変化するような場合
    - 各画面は互いに関係ない機能が入ってる

## 5/20 Applying density | Understanding navigation

- line height を調整することで、情報密度を調整することができる
- web だけ density サポートがなされてる
- ナビゲーションには以下の 3 つの種類がある
  - lateral 横
  - forward 前
  - back 後ろ
- アプリのトップレベルから、複数の画面への遷移が存在する場合は、トップレベルの画面からそれぞれの画面への遷移をできるようにしないといけない
  - ナビゲーションだったり、下部のナビゲーションだったり

## 5/19 component behavior Applying density

- Component behavior では ScreenSize が変化したときの View の挙動について説明してる
- Applying density
  - 大量の情報を表示するときは、情報密度を高くして表示した方がユーザビリティは上がる
  - 情報密度の高いコンポーネントがあるときは、マージンなどをちゃんととる
  - 情報密度と余白の話をしてる
- Density scale
  - 0,-1,-2,-3 でスケールを変化させることができる
  - View の大きさを変えること自体が、desity を変えることになるのか
    - 情報をただ詰め込むことが密度を上げることではなく、View の大きさを変更するという考えもある
  - density 変更のために View の大きさを変えても、タッチターゲットの 48 は守らないといけない

## 5/18 component behavior

- 横長のカードは、大きい画面になったらより正方形のカードに変形させたほうが読みやすい
- 画面のサイズによって、使うコンポーネントを変更することができる
  - 小さい画面では、bottomNav を使用し
  - 大きい画面では、ナビゲーションドロワーを使用する
  - 小さい画面では、フルスクリーンダイアログを使用し
  - 大きい画面では、シンプルなダイアログを使用する
- 画面サイズが変わることにより、レイアウト内のコンポーネントも変化する
  - 表示される
    - 大きい画面では、ドロワーが表示される
    - 大きい画面では、ツールバーに action のアイコンが並ぶ

## 5/17 component behavior

- ボタンを何も考えず View の幅を合わせてしまうと、画面サイズが大きくなった時に、大きくなり過ぎてしまうため、注意が必要
  - 強調され過ぎてしまうために良くない
  - https://material.io/design/layout/component-behavior.html#component-adaptation
