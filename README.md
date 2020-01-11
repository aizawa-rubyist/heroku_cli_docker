# Heroku CLI on docker

## 準備
```sh
cp .env.sample .env
vi .env # APIキーを設定(HerokuのAccount Settings画面で確認可能)
docker-compose build
```

## コマンド例
### DB接続
```sh
docker-compose run --rm heroku heroku psql
```
もしくはアプリ名が必要な場合は以下
```sh
docker-compose run --rm heroku heroku psql -a app_name
```

### Railsコンソール
```sh
docker-compose run --rm heroku heroku run rails c
```
もしくはアプリ名が必要な場合は以下
```sh
docker-compose run --rm heroku heroku run rails c -a app_name
```
