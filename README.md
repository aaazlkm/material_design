# 8/29 Gestures

- Provide realistic responses
  - dont use animation when drag
- Indicate gestures
  -  elements look and behave should indicate if gestures can be performed on them
    - Animate elements before the user interacts with them to suggest a gesture.
    - Elevated surfaces, like cards, suggest that they can be moved independently.
- Show what gestures do
  - as user performs a gesture, elements sholud move in a way that demonstrates the gestures
  - Gestures that execute actions should use graphics that communicate what the gesture will do.

# 8/28 Customization

- Elevation
  - by shrink background content when foreground container transforming, it makes more dramatic appearance between fore and back ground
    - これは面白いな、より動きが出ていいね
- Stagger
  - creates a stylized cascade effect that focuses attention very briefly on each item in a group
    - short delay before they fade in, creating a cascading effect.
    - a FAB can stand out by finishing its entrance after all other animations have stopped.

# 8/24 Customization

- motion can be customized to express your brand's style
- Applying customizations
  - apply customizatoin each app brand
- Speed
  - speed can be adjusted by changing a transitions duration and easing
- Motion paths
  -  the path that they follow can be linear or arced
  -  Linear motion paths have a simple and functional style, while arc motion paths create a more emphasized and dramatic style.
  -  アニメーションする軌跡を指定することができる
-  Oscillation　振動
  -  When oscillation is added, the transition path overshoots its endpoint at least once and then reverses course to return to the endpoint.
  -  animation like a bounding
- Transition patterns
  - can use shared axis transition animation instead of container transformation

# 8/16 Choreography

- Transitions with animated containers
  - when animate like a card ordivider, use container transforms
- Transitions without animated containers
  - when an element group is not contained by difined borders, use shared transformation
    - icons with fab can rotate
- Focal elements
  - Focal：商店
  - focal element in a transition is a persistent element that is significant to the overall hierarchy of elements in a transition
    - like header image
- Focal element conflicts
  - Some transitions will place a focal element in the path of other elements. In these cases, avoid using a focal element and apply a fade instead.

# 8/5 Choreography

- peak velocity
  - peak velocity refers to the fastest moment in a transition
- Transformation
  -  changing size, position, and opacity are types of transformation
  -  undergo　経験する　経る
  -  Complex layout changes use a shared transformation to create smooth transitions
  -  Don’t animate multiple elements simultaneously in relation to each other.
    - 別に良さげに見えるけどな....
  - Don’t move multiple elements independently.
    - it must avoid
- Transitions with animated containers

# 8/4 Choreography

- Choreography
  - transistion chioreography is a coordinated motion sequence
  - Sequencing
    - refers to the. order in which the different parts of an animation occur
    - a good sequence helps users understand what has changed on a screen
    - element types
      - outgoing
      - incoming
      - persistent
    - Fade types
      - fade
        - one element fading
      - cross-fade
        - A cross-fade transitions two elements simultaneously:
      - fade through
        - an outgoing element fading out entirely before an incoming element fades in.
        - 先に消えてから、表示される
        - minimize overlapping partially transparent elements

# 8/3 speed

- speed
  - Emphasized easing
    - In comparison to 　比べれば
    - draws extra attention at the end of an animation
    - used with longer durations
    - they speed up quickly and slow down very gradually, placing emphasis on the end of the transition
  - Decelerated easing
    - incoming elements are animated using decelerated easing
  - Accelerated easing
    - outgoing elements are animated using accelerated easing

# 8/2 Speed

- duration
  - the right combination of duration and easing produces smooth and clear transitions
  - exits and closing
    - use shorter duration when transitions thanclose dismiss or collapse
    - exit transitions mayy be faster because they require less attention
    - when drawer open 250ms close 200ms
  - transition area
    - 遷移先で大きくなるほど、duration は大きくなる
- easing
  - adjust an animations's rate of change
  - make elements move as though natural forces
  - types
    - standard easing
      - brings attention to the end of an animation by taking more time to decelerate than accelerate
        - こんなのもあるんだ

# 7/29 The motion system & Speed

- Fade
  - used when screen or dialog
  - i hava no idea about diffrence between face and fade through
    - fade does not have outgoing view.
- Speed
  - speed adjustments make transitions smooth and responsive
  - two properties
    - duration
    - easing

# 7/28 The motion system

- Shared axis
  - use fade when shared azis transition creates an unwanted flashing effect
- Fade through
  - used for transitions between ui elements that do not have a strong relationship to each other
  - fade through does not mislead users to think they can swipe horizontally between destinations

# 7/27 The motion system

- Container transform
  - seamlessly transforming one element into another, the relationship of the two elements is reinforced
  - can use when occupy only part of screen
- Shared axis
  - using when transitions between ui elements that have a spatial or navigational relationship

# 7/26 Motion

- use education
  - motion helps users understand how to perform action
    - like swipe to unlock
- transition patterns
  - container transform
  - shared axis
    - applied to ui elements with a spatial or navigational relationship
  - fade through
    - applied to ui elements without a strong relationship to each other
  - fade
    - entering or exiting elements

# 7/25 Understanding motion

- principle
  - informative
  - focused
  - expressive
- Hierarchy
  - motion reflects the hierarchy between a parent and child
- Brand expression
  - motion is used to express a brand personality and style
  - Icons and illustrations
    - polish 　磨く
    - animation in icons can add polish and playfulness to the user experience
    - motion can be used emphasize key points in a user journey
- feedback and status
  - motion provides timely feedback and indicates the status of user or system actions

# 7/24 Applying shape to UI

- Use a set of similar, related shapes across your product's components as a basis for developing a consistent hierarchy and brand expression.
- overuse of shape to express brand can lead to brand dilution
- Transformations
  - components can use shape changes to indicate state changes
  - shape used to indicate state should be distinct from the components typical shape
  - intrude 侵入
- Baseline shape values
  - the recommended range of values for each shape family are listed in the following table

# 7/23 Applying shape to UI

- overrides
  - when a component requires different shape than the one defined by a category, it can use an override to its shape family size or both.
- Picking shapes
  - we can use shape as brand
  - mixing shapes can make it hard to distinguish brand style
- Hierarchy
  - component with unique shapes stand out
    - can be used to draw use attention
  - like fab

# 7/22 Applying shape to UI

- component symmetry
  - components can apply corner shapes in either a symmetrical or asymmetrical way
  - when rtl layouts, we need mirror design
- Categories and overrides

# 7/21 Applying shape to UI

- Shape attributes
  - category attributes
    - shape family
    - shape size
    - symmetry
  - shape family
    - components can apply one of two styles to the shapes of their corners
      - rounded corner
      - cut corner
  - shape size
    - shape size is defined by absolute or percentage
    - absolute
      - ex. 2dp, 40dp...
    - percentage
      - small component s can set the size of theire corner shape using a percentage of the absolute height
      - this means the corner shape will change as the component height changes
        - this only use when changing shape is small component
        - beacause dynamically changing height will lead to rounded corner to circle

# 7/20 Shape and motion Applying shape to UI

- Default shape
  - vice versa
    - 逆もまた同様に
  - backdrop の例がいい感じだ、こんなアプリを作りたいんだよな
- Applying shape to UI
  - material shape system によってシステマチックにコンポーネントにユニークな形を適用できる
  - components are grouped into shape catgrories based on their size
  - shape categories include
    - small components
      - button, chip
    - medium components
      - card, dialog
    - large components
      - backdrop, data table

# 7/15 Shape and motion

- dimension 寸法、広がり、容積
- surface can change its size
  - Stretching
  - shrinking
- avoid distorting shapes when stretching or shrinking a surface
- shape can transform into a different shape
- all content o a surface shoul be visible while the surface morphs, without clipping content
  - 内容が見えるように、surface の大きさが変わるようにする

# 7/14 　 Shape and motion

- Shape overuse
  - 特殊な shape の使いすぎは、意味をなくしてしまう。特殊が普通になってしまうから
  - 普通になると　 leaa noticiable になる
- Shape and motion
  - shape はコンテントの変化やユーザインタラクションによって、変化する

# 7/13 Shape as expression

- Expressing brand
  - 形と色やテキストを組み合わせることで、ブランドの視覚言語を開発することができる
  - shape family
    - アプリ内で使用する shape をまとめて定義しておく
  - 異なる shape style を混ぜちゃうと、ブランドと shape が結びつかなくなるのでやめたほうがいい

# 7/12 Shape as expression

- in tandem with と並行して
- initiated 　開始して
- morph 変形して
- shape change はユーザの操作に紐づけるべき ssion

# 7/11 shape & Shape and hierarchy

- component は以下の三つに分けれられる
  - small
    - button, chip
  - medium
    - card
  - large
    - drawer
- Shape and hierarchy
  - unique shape get user attention
  - 周りの要素が四角の中丸の fab は stand out
- related surfaces
  - 一つの場所だけ角にすることで、他の surface に関連することを表現することができる

# 7/10 animated icons & shape

- identity
  - コンポーネントを識別する方法を提供する
- state
  - by using shape, you can express elements change of state
- branding
  - tandem 　二つの何かが縦に並んで
- Displaying shape
  - 背景色に対して十分なコントラストを持ってると、shape はよく見える
  - シャドウを使ったり、色や opacity を使ってコントラストを持たせるようにする
- Communicating meaning
  - シェイプは特定の目的や意味を持たせるために使用する
  - 一つだけ各丸じゃないのは、つながりを表現できる

# 7/9 animated icons & shape

- animation の種類
  - transitions
    - アイコン A からアイコン B への変化
    - simple
      - そこまで重要ではない変化
      - 単純なアニメーション(fading, scaling rotating)でもいい感じに変化してるように見える
      - ツールバーのアイコンなどに使用される
    - complex
      - 重要な変化
      - アイコン自体が変化するようなアニメーション
      - 注意を引くしいい感じ
      - lottie らへんを使わないといけないんだろうな
      - music の操作のアイコンなどに使われる
  - Duration
    - 複雑なアニメーションの場合は duration を長めにとる
    - simple: 100ms
    - average: 200ms
    - complext: 500ms
  - stagger
    - left to right にアニメーションを適用することで、進行中のような意味を持たせることができる
  - States
    - animation represent they have changed state
  - Theming
- shape
  - 色々な形を設定することができる
- Usage
  - emphasis
    - unique shapes stands out, they can direct attention to different parts of screen

# 7/6 animated icons & shape

- animation の種類
  - transitions
    - アイコン A からアイコン B への変化
    - simple
      - そこまで重要ではない変化
      - 単純なアニメーション(fading, scaling rotating)でもいい感じに変化してるように見える
      - ツールバーのアイコンなどに使用される
    - complex
      - 重要な変化
      - アイコン自体が変化するようなアニメーション
      - 注意を引くしいい感じ
      - lottie らへんを使わないといけないんだろうな
      - music の操作のアイコンなどに使われる
  - Duration
    - 複雑なアニメーションの場合は duration を長めにとる
    - simple: 100ms
    - average: 200ms
    - complext: 500ms
  - stagger
    - left to right にアニメーションを適用することで、進行中のような意味を持たせることができる
  - States
    - animation represent they have changed state
  - Theming
- shape
  - 色々な形を設定することができる
- Usage
  - emphasis
    - unique shapes stands out, they can direct attention to different parts of screen

# 7/5 system icons & animated icons

- 太さと fill と corner radius と color をいじってカスタムアイコンを作成することができる
- recomennded corner radius values are between 0dp and 4dp
- icon theme
  - outlined icon
  - two-tone icons
  - sharp and rounded icons
    - enables the use of multiple brand colors
    - improve legibility
- animated icon
  - polish and delight. 磨きと喜び

# 7/4 System icons

- icon の stroke は 2dp じゃないといけない
  - だからマテリアルデザインのアイコンはちょっと太めなんだな
- icon の　 stoke は均一じゃないといけない
  - けど、複雑な形状のアイコンの場合は、読みやすさ的に調整して、違う太さになることもある
- icon の touch target は 48dp 確保しないといけない
  - ios では 40dp ですね
  - keyboard やマウスが主なインプット要素だったら、40dp でもいいらしい

# 6/28 Product icons System icons

- fold
  - 折りたたんだような表現もできる
- Accordion
  - アコーディオンのように折りたたんだ表現できる
- アイコンを歪めたり、変形させたりしてはいけない
- System icons
  - アイコンに対して、細かい装飾は止める
    - 細い線なども表現

# 6/27 Product icons

- Anatomy
  - 解剖学、構造
- マテリアルデザインでは、仮想の光が要素を照らすので、それを反映して車道などを設定しないといけない
- Contact shadow
  - 要素を真上から照らすことによって生じる影
- Edge tint and shade
  - 要素の top と bottom の端に色を与えることで、深さを表現することができる
    - top には明るい色を
    - bottom には暗い色を
  - height は 1dp くらい
- Finish
  - 45angle で照らす光
- 色自体に車道やエッジの表現を適用してはいけない
- レイヤーを追加しすぎてはいけない
- スコアリングは、アイコンを半分に分ける行為
  - これにより、深さを与えることができる
  - 中心に据えないといけない

# 6/26 Sound choreography Product icons

- file formats
  - ファイルの圧縮をしすぎてノイズを含まないようにする
  - でも、圧縮はちゃんとする
- material design の haptic sound を置いとい手くれてる
  - https://material.io/design/sound/sound-resources.html#
- Product icons
  - 実際に髪からプロトタイプを作り、光の当たり方などを見る
  - keyline shapes
    - 以下の四つの基本的な形がある
      - square circle vertiacal rectangle horizontal regtangle

# 6/25 Sound choreography

- sound にも priority という概念あるんだな
  - priority ってあんま使わないものだと思ったけど、意外とあるのかもしれない
- 音を設定するときは、現実世界のいろいろな場所でテストして、音をオーディションした方がいい
- イコライゼーション
  - 特定の周波数を強化または削減する効果
  - 全然違いがわからない

# 6/24 Sound choreography

- Expressing sound relationships
  - motifs を使用して on off は互いに関係してる音を出す
- Repeated sounds
  - よく発生する音は、現実世界の音を真似たり、音に僅かな変化を与える
    - **同じ UI でも押下する場所によって、音を変えてる！！！**
  - スクロールやスワイプやタイプなど
- Mixing sound
  - 複数の音源を混ぜること

# 6/22 Sound choreography

- Effects
  - 音に空間と奥行きを与える
  - Reverb
    - サウンドに存在感を与える
    - 確かに音が広がっていくような感覚を覚える
  - Delay
    - 元のサウンドをのエコーをそのサウンドにブレンドする
- Sound choreography
  - 互いに続く音には関連性が必要
  - Key signatures が tonal サウンドの特徴を決定する

# 6/21 Sound attributes

- dynamics
  - volume または、ラウンドネスを変化させる
  - ダイナミックなサウンドにより、自然でリアルに感じられる
- Envelope
  - 時間の経過に伴うサウンドの振幅の変化を指します。
  - attacke
    - softer と shaper の表現方法がある
  - Decay
    - アタック後にサウンドの振幅が減少する量と速度を差す
    - decay が大きいほど、音が大きくゆっくり感じられる

# 6/15 Sound attributes

- Tonality
  - 調性、色調
  - Tonal sounds
    - 音楽的な音
    - simple
      - 短くリズミカルな音
    - Common motifs
      - 音が大きくなる
        - はじまったこと、ポジティブなことを意味する
      - 音が小さくなる
        - 終わったこと、閉じたことを示す
      - 音が繰り返す
        - 考えや待つことを意味する
    - 音のパターンで意味することが異なるので面白いな
      - デザインと同じでここも奥が深そうな感じだな
  - Atonal sounds
    - 日常の音やノイズに似た音
    - ハプティックフィードバックやボタンの押下の音などに向いてる
    - Skeuomorphic sound
      - 現実に存在するものと同じ音に使う
      - カメラのシャッター音など
      - キーボードの音など

# 6/14 Sound attributes

- warrants 必要な場所
- 音を視覚化する方法について書いてる
  - あまり嬉しくないような？？
  - 方法
    - 横じく time
    - 横じく frequency
    - 横じく Timbre(音色)
      - 音色を横軸にできるのか
- Timbre 音の明るさ（高周波音の量）によって使い分ける
  - 明るいと、存在感が大きくなる
    - 電卓などのボタンにこれを使用しない
  - 落ち着いてると、重くて深刻な感じ
    - 周りがうるさい環境だと聞こえない
    - 電卓のボタンなどに使用

# 6/13 Applying sound to UI

- hero sounds を使うタイミングは以下
  - 祝う
  - ユーザが新しくアプリを使うとき
  - プロダクトの主要な動作を終えた時
- 確かに、TODO アプリで全ての TODO を終えた時に、このサウンドとアニメーションがあるのはいい感じな気がするよな
  - 家計簿でも一回入力したら音出るようにしたら、ちょっと嬉しいのかも。まあこれはなりすぎて微妙な場合もあるけど
- Notifications
  - ダイアログに対しても使用できる
  - 他の UI よりも頻繁に起きるため、ヒーローサウンドよりは短く、複数回再生するのに適した方法がいいらしい
  - 通知をカスタマイズできるようにした方がいいらしい
  - 音ってどこまでやるか悩むよな
- ここら辺はスイッチがめちゃ参考になる気がするな
  - よく音が出てるイメージがある
- ぷるれフレッシュなど、自分が本当にその作業を完了してるのか分かりづらい場合に、音を出すといいのかもしれないな
  - disable のボタンもそうだな、押下できてるのかわからない時に、音を出す
    - この考えで言ったら、haptic 動作とか disable でやるべきなのかな？？
    - ちょっと微妙な気もする

# 6/11 About sound

- 音楽や動きと組み合わせると、音楽は製品の感情を高めることができる
- 会話の音声を使うことで、複雑な情報を伝えられる
- 音は以下のタイミングで適用できる イアコンと呼ばれる
  - 動作
  - 状態の変化
- 音は、相互作用の意味と製品の美的感覚、感情、個性の両方を強化する
- 音の種類
  - 実物の音を真似たもの Skeuomorphic sounds
  - 抽象的な音 Abstract sounds
- 音の使い過ぎには注意する
  - 音は基本的に必要ないもの
  - ユーザの注意を快適さを損なう
  - デザインの余白と同じで、余白があるからこそ、注意を惹きつける

# 6/10 Language support About sound

- 言語によってテキストの大きさ変えるの大変だと思ったけど、これはアプリ側でテキストのサイズを変更できる設定を設ければ解決だな
- google が各言語の以下のタイプに分類している
  - English-like
  - Tall typefaces
  - Dense typefaces
- アプリに sound effect 取り入れたいいいいな
- sound は次の目的で使用される
  - UI を特定のサウンドに関連付ける
  - 感情や性格を表現する
  - 相互作用を特定の音に関連づけることにより、階層構造を伝達
  - 感覚フィードバックを提供する
    - ユーザにアクションが終了したことを明確に伝えることができる

# 6/9

会社でデザイン会があったのでお休み

# 6/8 Understanding typography Language support

- lineheight 指定した状態で、sp 変えるとどうなるんだろう？
  - どちらが優先されるんだろうな？
- 右揃えテキストは、短い要素にはいい感んじ、再度に表示されるノートとか
- システムフォントはいろいろな場所で使用されるため、目立ちづらい
- Language support
  - 言語によって、サイズやスタイルを変えた方がいいかも。。
  - 言語によって平均の単語の長さや高さが違うので、UI の表示のされ方も異なってしまうため
    - サイズも異なることがある
  - 種類
    - English-like
      - 英語に似てる
    - Tall typefaces
      - アラビックとかタイなどの言語
      - bold は使ってはいけないらしい、あまりにも太くなってしまうため
      - ラテン語系の言語よりテキストが少し大きい
    - Dense typefaces
      - 中国日本韓国
      - ラテン語系の言語よりテキストが少し大きい

# 6/7 Understanding typography

- Letter-spacing
  - 文字間のスペースを均一に調整すること
  - 見出しなどの大きなタイプのテキストは、文字間を狭くするらしい
  - 小さい文字は、文字間隔広めにとるらしい
- 表などの数字は、固定幅のフォントを使用する
  - カンマの位置を揃えるため
- line は
  - body は 40-60 がベスト
  - short line は 20-40

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
