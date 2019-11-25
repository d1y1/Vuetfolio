# コンセプト CONCEPT
かんたんに作れて更新の手間も抑えられるような
ポートフォリオテンプレートを目指して作成しております。
I wish creating and editing easy portfolio site.
この経歴書はテンプレートはVue.jsで作成しており、
dataとimageを用意するだけでいい感じのポートフォリオができます。
This template made Vue.js.
So, You only edit data and take images.
また、なるべく1つのファイルで完結することを目指しています。
これは多くレイヤーの方に使ってもらいたいからです。
And, It is one file.
Because, I wish to use many people.
公開はgithub pagesを使用すると手軽かと思います。
I recommend to use github pages.
github pageでの公開手順はここをみるとよいと思います。
Check about how to upload github pages.
https://ferret-plus.com/5875
(わかりにくい部分があれば気軽にissueなどでお知らせください。すぐに対応します。)
(英語が間違ってたら気軽にissueとかでおしえてもらえるとありがたいです。。。)
※ 個人情報の公開は危険であり、また外部向けのサービスではないプロジェクトをグローバルに公開すること禁止している場合があります。
※ そのような場合は、auth機能を有効にする。もしくは記載を避けてください。
※ auth機能に関しても簡易的な認証なので公開する場合は自己責任でお願いいたします。
# サンプル SAMPLE
このrepositoryはgithub pagesで公開しているので
以下のurlで表示を確認いただけます。
https://d1y1.github.io/Vuetfolio/
# 使い方 HOT TO USE
index.html内のdata.displayItemsを
自分の経歴に書き換えてご利用ください。
以下で各ディレクティブの書き換え方法を紹介してます。
## 各ディレクティブについて
使用しないディレクティブは削除せず、
文字のときは、空文字。
配列のときは、空配列。
オブジェクトnoneを入力してください。
あと、dataはオブジェクト型なので最後「,」をつけるのを忘れないでくださいー。
### header
```
  header: {
    title: "myPortfolio",
    messageUrl: "https://docs.google.com/forms/d/xxx"
  },
```
headerに表示する内容を記述します。
#### title
headerに表示するこのportfolioのタイトルを入力してください。
#### messageUrl
portfolioを見た方からメッセージを受け取るときに使用します。
google formを作成し、urlを貼るのがよいかとおもいます。
直接メーラーが起動するようにしたい場合は、"mailto:"を指定しましょう。
```
messageUrl: "https://docs.google.com/forms/d/xxx",
```
もしくは
```
messageUrl: "mailto:name@email.com",
```
### mainVisual
メインビジュアルとして使用する画像を指定します。
```
  mainVisual: {
    logoImageSrc: "images/mainVisual.png",
    backgroundImageSrc: "xxx"
  },
```
#### logoImageSrc
ページのロゴのurlを指定します。
local srcとしたい場合は、imagesディレクトリに画像を配置し、images/xxxx.pngとしてください。
#### backgroundImageSrc
背景に使用する画像を指定します。
自分の撮ったお気に入りの写真をlocal srcしてもいいですし、
以下のサイトから画像urlをコピーしてきて指定してもよいかと思います。
https://unsplash.com/
### about
```
  about: {
    textCatchCopy1: "キャッチコピーを記述します。",
    textCatchCopy2: "2行目のキャッチコピーを記述します。",
    textDescription: "キャッチコピーについて長めに書くといいかもしれません。(※改行には対応してません。)",
    imageSrc: "images/about.png",
    personalInfo: {
      name: "",
      birthday: "",
      address: "",
      tel: "",
      mail: ""
    }
  },
```
#### textCatchCopy1
自分を表すキャッチコピーを記述してください。
#### textCatchCopy2
二行目のキャッチコピーを記述してください。
#### textDescription
自分についての説明や、キャッチコピーの意図をちょっと長めに記述すると良いかもしれません。
(※たぶん改行には対応しておりません。)
#### imageSrc
自分の顔写真やアイコン画像のurlを記述してください。
#### personalInfo
自分自信の紹介文を記述します。
(※個人情報となる部分はauth機能を有効にして使用することをおすすめします。)
(※まだ未実装。乗せるべきなのか検討中)
### history
学歴、資格取得歴、職歴、受賞歴の順番に記述していきます。
```
history: {
    academic: [
      {
        startDate: "20xx.x",
        endDate: "20xx.x",
        title: "AAA高校",
        description: "aaa科に所属"
      },
      {
        startDate: "20xx.x",
        endDate: "20xx.x",
        title: "BBB大学",
        description: "bbb科に所属"
      },
    ],
    qualification: [
      {
        startDate: "20xx.x",
        endDate: "",
        title: "CCC資格",
        description: ""
      },
    ],
    career: [
      {
        startDate: "20xx.x",
        endDate: "20xx.x",
        title: "株式会社DDD",
        description: "デザイナーとして所属。dddアプリケーションの構築、運用。"
      },
      {
        startDate: "20xx.xx",
        endDate: "",
        title: "EEE有限会社",
        description: "エンジニアとして所属。フロントエンドエンジニア、サーバサイドエンジニアを経験。"
      }
    ],
    award: [
      {
        startDate: "20xx.x",
        endDate: "",
        title: "賞の名前",
        description": "佳作を受賞。"
      }
    ]
  },
```
学歴、資格、職歴、受賞歴の各項目は
配列となっているので必要な分コピーして使用してください。
ない場合は、空配列としてください。
```
award: []
```
各項目の中身は以下のような構成となっています。
```
{
   startDate: "20xx.x",
   endDate: "",
   title: "賞の名前",
   description": "佳作を受賞。"
}
```
#### startDate
始めた日を記入してください。
#### endDate
終えた日を記入してください。
#### title
学校名や会社名など各項目にあった名称を記入してください。
#### description
何科に所属していたかやどのような役目で携わっていたかを記入してください。
### works
```
"works": [
    {
      "title": "プロジェクト名",
      "summary": "プロジェクトの概要などをちょっと長めに書くといい感じだと思います。",
      "tags": ["B2C", "C2C", "Wordpress",],
      "favoriteWorks": [
        {
          "title": "お気に入りの箇所",
          "imageSrc": "images/works1_1.png",
          "description": "そのお気に入りの箇所のことをちょっと長めに書くといいと思います。",
          "linkUrl": "https://関連ページのurl"
        }
      ],
      "skills": [
        {
          "title": "MacOS",
          "iconName": "fab fa-apple",
          "color": "red",
          "point": "8"
        },
        {
          "title": "CentOS6",
          "iconName": "fab fa-linux",
          "color": "red",
          "point": "1"
        },
      ]
    },
 }
```
各仕事の内容を掘り下げて記述します。
プロジェクト単位で記述するといいかもしれないです。
(※B2B向けサービスなどの外部に向けたサービスではない場合、グローバルに公開することを禁止しているプロジェクトの場合は、authを有効にして公開することをおすすめします。)
また、そのプロジェクト内でも気に入ってる点やうまくいった部分を記述できます。
そのプロジェクトから得たスキルを記述しましょう！
#### title
プロジェクト名を記述してください。
#### summary
そのプロジェクトの内容をちょっと長めに書くといい感じです。
(※多分改行はできません。)
#### tags
そのプロジェクトに関連する技術的な単語やツール名などを羅列します。
単語単位で多めに書くとよいかと思います。
#### favoriteWorks
プロジェクトの中でも気に入ってる部分を記述しましょう！
配列で記述できるので複数ある場合は、お気に入りの分追加しましょう！
#### skills
このプロジェクトで得たスキルを羅列します。
詳細は以下で説明します。
##### title
スキル名を記述します。
##### iconName
スキルにあったアイコン名を
fontawesomeから探し記述します。
https://fontawesome.com/icons?d=gallery&m=free
> fab fa-linux
のようにアイコンタイプとアイコン名が必要です。
##### color
スキルに合う色を以下の中から指定しましょう。
- red
- blue
- orange
- green
おすすめは
- red    は開発環境やOS
- blue   は言語やフレームワーク、ライブラリーなど
- orange は開発ツールやアプリケーション
- green  はリーダ経験やテストなどのフェーズの記述、またはその他
にすると良いと思います。
##### point
このプロジェクトでどのくらいレペルアップしたのかの数値として
「1」から「10」の間で記述します。
# 認証について ABOUT AUTH
※md5の生成やjson apiの知識が必要です。
※個人情報を記載する場合や、外部向けではないプロジェクトの内容を記載する場合は使用を推奨します。
本portfolioテンプレートは簡易的なパスコード認証で閲覧を制御することもできます。
data.auth.enableをtrueにして、
任意のmd5でハッシュ化されたパスコードをdata.auth.tureCodeに記入します。
data.auth.apiUrlにdata.displayItemsと同等のjsonを返すapiのurlを記入します。
github pagesで公開されている場合は、
repositoryをprivateにして、github pagesを有効し、(※有料です)
displayItems.jsonというファイルを配置し、
そのファイルの公開されているurlを指定すると手軽にapiとして認識してくれます。
## auth
```
auth: {
  enable: true,
  jsonUrl: "https://{{自分のgithub名}}/{{repository名}}/displayItems.json",
  trueCode: "ttt",
  code: "",
},
```
### enable
auth機能の有効、無効を切り替えます。
有効の場合は、auth画面を表示し、パスコードが正しいことが
確認できた時点で、apiでjson情報を取得し、
data内のdisplayItemsを書き換えます。
無効の場合は、auth画面は表示されず、
data内のdisplayItemsを参照します。
### jsonUrl
認証後にデータ取得するapiの接続先を指定します。
github pagesにて公開している場合は、jsonファイルを配置するのみでも機能します。
> jsonUrl: "https://{{自分のgithub名}}/{{repository名}}/displayItems.json",
※コードを見れると認証の意味がないのでかならず、private リポジトリにて公開してください。
※有料版のみprivate repositoryでgithub pagesを有効にすることができます。
