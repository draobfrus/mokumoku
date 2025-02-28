# README

## 環境構築
```
$ bundle install
$ bin/rails db:setup
$ yarn install
$ bin/rails s
```

## 事業をエンジニアリングしよう提案編の回答は以下に記述してください


### ■選択した事業側の課題
サービス登録者数の内、男性60%に対して、女性は40%。一方で、サービス内のもくもく会に参加した人の比率は、男性90%：女性10%と大きな差が出ている。もっと女性が使いやすいようなサービス設計にする必要があるのではないか？

### ■提案内容
ユーザープロフィール等を公開する。
現状、各もくもく会から主催者のプロフィールにアクセスできない他、参加者情報も公開されていないため、実際に集まるまでどんな人が主催・参加するのか分からない状態になっている。見知らぬ人と会うことへの心理的抵抗がユーザー（特に女性）の参加を阻んでいると考えられるため、参加表明前にある程度もくもく会に集まるユーザーの情報を把握できるようにする。

### ■実装方針
- 各ユーザーのプロフィール欄を充実させる。現在はアバター、メールアドレス、名前しか登録項目がないため、性別('gender'), 自己紹介文('introduce')の入力項目を追加する。
- 各ユーザーのプロフィールは公開を前提とし、ログインユーザーであれば誰もが閲覧できるようにする（但し他人の編集や削除はできないように制限を設ける）。
- もくもく会詳細ページを開いた時に、「主催者名」の項目をクリックすると、主催者のプロフィール及び過去に主催したもくもく会一覧が表示されるようにする。
- もくもく会詳細ページに「参加者情報」の項目を設け、現在の参加者数と、男女内訳を公開する。更に「参加者情報」の項目をクリックすると、参加表明したユーザーの名前・アバターが一覧表示され、各ユーザー名のリンクからプロフィールや過去に主催したもくもく会の情報が取得できるようにする。
