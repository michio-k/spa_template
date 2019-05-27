# SPA

## overview
django（API）＋vuejs（フロント）＋nginx＋postgres（DB）の
SPAのサイトを作るための雛形。

## environment
Dockerとdocker-compose。
- Docker version 18.09.2, build 6247962
- docker-compose version 1.23.2, build 1110ad01

## コンテナ
以下4つのコンテナで構成。
 - vuejs
 - postgres
 - nginx
 - django

## アプリ
django: djangoproject
vue: vueproject

### コンテナをバックグランドで起動する
`docker-compose up -d`

### コンテナを停止する
`docker-compose stop`

### コンテナを削除する
`docker-compose down`

### django開発サーバを起動する
`docker container exec -it spa_django djangoproject/manage.py runserver 0.0.0.0:8000`

### npm install
`docker container exec -it spa_vue npm install`

### webpack dev serverを起動する
`docker container exec -it spa_vue npm run dev`

#### vueのbuild
`docker container exec -it spa_vue npm run build`

### コンテナに入る
`docker container exec -it spa_django bash`
`docker container exec -it spa_nginx bash`
`docker container exec -it spa_vue sh`

### 動作確認
バックエンド：http://0.0.0.0:8000/
フロントエンド：http://0.0.0.0:8080/
webサーバ：http://0.0.0.0:9000/
