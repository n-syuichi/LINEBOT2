# LINEBOT2
昔書いたLINEBOTをNodeで書き直しています。

# 環境設定
- `git clone https://github.com/n-syuichi/LINEBOT2.git`でプロジェクトをクローンしてください。
- `touch .env`で.envを作成します
- .env内を以下のようにします
```
CHANNEL_SEACRET= ...
CHANNEL_ACCESS_TOKEN= ...
LINE_UID= ... 
```
LINE MessageAPIのチャンネルシークレット、アクセストークンを確認してください。
LINE_UIDは、送信先のid(userid, groupid)を入力してください。
(自分のUIDを設定する場合は、Message APIの管理画面に表示されています)

Message APIの設定方法については以下を参照してください。
https://first-contact.jp/blog/article/linebot/

# パッケージ管理
Yarnでパッケージ管理をしています。
`yarn install`で指定パッケージをインストールしてください。
(package.jsonで指定されているので、yarn install時に自動でインストールされます)

また、LINE Developer SDKを使用しています。

# JavaScript
TypeScriptを使っています。
ts-nodeを使って、distファイルにjavascriptへトランスパイルしたものを出力しています。

# build
`yarn dev`で実行できます
`yarn dev:watch`で更新すると自動でトランスパイルされます。
`yarn build`でビルドできます。
`yarn start`で実行できます

# Heroku
process.env.PORTはHerokuの環境変数です。指定しない限りポートは3000になります
そのまま、Herokuにアップロードすることもできます。

Herokuに関しては、以下を参照してください。
https://qiita.com/DogK0625/items/12178fdc3dd607088ff0




