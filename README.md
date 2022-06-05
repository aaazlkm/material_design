# 6/6 Understanding typography

- Ascenders and descenders
  - cap height よりも高い d などが該当する
  - base line よりも下に伸びるやつ y など
- weidget
  - 太さ
- Monospace
  - 全ての幅が同じ
  - さんセリフは一応幅違うんだな、一緒かと思ってた
- 識字力は、フォントに影響
- 読みやすさは、書体のスタイルに影響される単語やテキストのブロックを読みやすくすることを意味する

# 6/5 The type system Understanding typography

- button のテキストは典型的に all caps sans serif
  - ボタンのフォントってマテリアルデザインでは、サンセリフ使う縛りがあるの？？
  - 文章のテキストの場合は、セリフもありえるらしい
- ボタンに厳ついフォントは使ってはいけない
  - 確かに、スクリプト帯のボタンなんて見たことないな
- テキストは、階層とブランドの存在を表現する
- テキストは、4dp ごとに並ぶ
  - ラインハイトは 4dp ごとの指定にする
- Cap height
  - ベースラインから測定した書体のフラットな大文字（M や I など）の高さ
  - S や A などの丸くて先のとがった大文字は、キャップの高さより少し上にオーバーシュートして描画することで、同じサイズに見える
- X-height
  - 書体の小文字の x の高さを指す
  - x height が高いと、各文字内の空白が読みやすいため、小さいフォントサイズで読みやすくなる

# 6/4 The type system

- a range of さまざまな
- type の大きさは、13 のスタイによって表現される
- android では文字間の間隔は em の単位を使用する？
  - 何これ？
- headline
  - 1 - 6 段階ある
  - 短く、攻めてるフォントを使える
- Subtitles
  - 中間的な表現に使用される、短いテキスト
  - 攻めてるフォントは使わないようにする
- Body
  - 1-2
  - 長い文章に使用される
  - 攻めたフォントは使用しない
- Caption and overline
  - 最も小さいサイズのテキスト
  - 注釈の時などに使用される
  - overline 初めて聞いた
    - overline に使用されるらしい、overline とは？
      - 見出しの上の補足文らしい
    - caption は？
      - 画像の下に説明文などで使用される

# 6/3 Dark theme

- 状態を表現するのに、オーバーレイを使用する
  - surfaceContainer と primaryContainer が存在する
  - surfaceContainer
    - テキストやアイコンと同じ色のオーバーレイを載せる
  - primaryContainer
    - 背景色が primary を使用してるもの
    - オーバーレイは white
  - ここのらへんの処理は自分でやるというよりかは、ライブラリ側で自動でやってくれてる部分だよな

# 6/2 Dark theme

- ダークテーマの時は、エラーに色に white の opacity 載せてる
- ダークテーマの中でも目立つように、snackbar の色は白色でもいい

# 6/1 Dark theme

- text の色と背景色はちゃんとコントラストをとること
  - primaryColor を overlay させる場合もあるらしい
  - 面白いな
    - そうすれば、surface でもブレンドカラーを表現でき、アプリ全体の統一感を守ることができるのか
- desaturated な色を使用する、背景色とのコントラストを保つために
- ブランドカラーを控えめに使用するこにより、要素は階層内で目立つようになる
  - 目立つかどうかは他の用途の兼ね合いで決まる

# 5/30 Dark theme

- dark theme はブラックではなく、ダークグレイを使用する
  - ブラックだと完全にシャドウが見えなくなってしまうため
- 影ではなく、表面の色の明るさで、深さを表す
  - これは onSurface カラーを overlay で薄く表示することで実現する
    - でも light の時これやるのか？
    - もしかしてここで条件判定入れないといけないのか？面倒じゃね？
    - elevation の値ごとに、overlay どれくらい載せるかが決まってる
      - 1dp -> ovelay 5%など
    - この考えは、primary, secondary を使用した view には適用されない
      - overlay を表示しない

# 5/28 Text legibility and Dark theme

- 相変わらずテキストの opacity を下げる意味がわからない
  - opacity つけないとコントラスト強すぎるから、それを防ぐ意味で opacity をつけるのかな？
  - これはデザイナーの人に確認をしたいな
- material tool を使用することで、テキストと背景色のコントラストが十分か確認することができる
- 色の opacity を変更することで、active 状態を表現したり、読みやすさを調整できる
- dark theme
  - 目の疲れを顕現し、照明条件に合わせて明るさを調整し、暗い環境でも画面を使用できるようにする
  - 人間工学的に素晴らしい
- dark theme で決まってること
  - 深さは影ではなく、surface の明るさで表現する

## 5/27 Color usage and Text legibility

- placeholder, state change, prgogress などでブランドカラーを使うことで、そのブランドカラーの存在を維持できる
- 色によって意味を与えることができる
  - 混んでたら赤 空いてたら緑表示 など
- 色はアプリ内で一貫性のある使い方をしないといけない
  - ブランドカラーが赤だった場合、エラーで赤を使用してはいけない
- テキストの読みやすさは The Web Content Accessibility Guidelines に定義されてる
  - 4.5:1 の比率で背景とコントラストをつけないといけない
- テキストの不透明度を変更する
  - これにより、読みやすさが向上する？
  - なんで不透明度を調整すると、読みやすさが変わるんだ？

## 5/26 UI Color usage

- 色は、階層やブランドの存在、View の状態を示す
- どの element が重要か示す方法は、たくさんある
  - Color Theme はアプリによって異なるので
  - 色は他との要素との関係で意味が変わってくる
- 色だけではなく、形も変えることで、選択したことを強調することができる
- gray を使うことで、写真やテキストが目立つ
- launch screen は色を大胆に使う最適なタイミング

## 5/25 Applying color to UI Color usage

- modal sheet 系に primary color を使用していいんだ
- drawer の scrim の黒じゃなくていいのか
  - シャドウは黒のイメージがあったけど、白表示でもいいのか
- 画像の上にテキストを表示すると読みにくくなるので、primary color をテキストとアイコンの下に敷いて読みやすさを担保する
- 色によって、重要性や他のテキストとの関係性を表現することができる
- 重要なテキストには、primary secondary を使用する
- 画像の上にテキストを表示する場合は、薄い色のシートの上にテキストを表示する
  - これにより読みやすさが担保される

## 5/24 Applying color to UI

- material design で決まってる color theme 以外にも追加でアプリの色を定義することができる
- app bar に primary color を使用する system bar には primary color dart or light を適用する
- アプリの構造よりもアプリのコンテンツを強調したい時に、app bar と backgourd の色を揃える
  - app bar と content の色を分けることは、コンテンツの構造を伝えるのに役に立っていたんだな
  - 同じ色にしてもスクロー時に shadow を適用することで、同化しないようにしてる
- 背景の色が強いと、各要素が目立たなくなり、コンテンツ全体が目立つようになる
- 下部シート、ドロワー、メニュー、ダイアログ、カードなどのベースラインは白だが、他のものと区別するために色を与えることができる
  - 例では primary color を設定してる

## 5/23 color system

- color types
  - primary Color
    - アプリの画面、コンポーネント全体を通して最も頻度高く表示される色
  - secondary color
    - アクセントや区別するために使用される色
      - fab, selection controls highlight selected text
  - surface color
  - background collor
  - error color
  - onCOlors
    - XXXColor の上に表示されるテキストやアイコンなどの色を指定する
- Alternative colors
  - テーマの話
  - 同じアプリないでも機能によってテーマを変える考えがあるらしい

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
