# NodeSub-Node-db

- 勉強用の課題です

## Description

- **[Docker](https://www.docker.com/products/docker-desktop)** を使用し **[Node.js](https://nodejs.org/ja/)** と **[Mysql](https://www.mysql.com/jp/)** を接続しています

## Requirement

- [Docker](https://www.docker.com/products/docker-desktop)/docker-compose 3.8

## Usage

1. `.env` ファイル を作成する(???は適当なものを入力してください)

   ```.env
   MYSQL_ROOT_PASSWORD=???
   MYSQL_USERNAME=???
   MYSQL_PASSWORD=???
   MYSQL_DATABASE=db_mysql
   MYSQL_HOST=db
   ```

1. **[Docker](https://www.docker.com/products/docker-desktop)** をインストールし **docker-compose.yml** のある場所で下記のコマンドを実行します

   ```sh
   $ docker-compose up -d
   ```

1. コンテナの中に入るには下記のコマンドを実行します

   ```sh
   $ docker exec -ti api_node sh
   ```

1. コンテナの中で環境を構築するには下記のコマンドを実行します(環境構築後に docker-compose.yml 内の'command'部分のコメントアウトを外してください)

   ```sh
   yarn init
   npx express-generator --view=ejs
   ```

1. Mysql のコンテナに入るためには API コンテナから出て下記のコマンドを実行します

   ```sh
   $ docker exec -ti db_musql sh
   ```

1. Mysql に接続するにはコンテナ内で下記のコマンドを実行します(USEWNAME,PASSWORD は.env ファイルと同じものを記述してください)

   ```sh
   mysql -u {USERNAME} -p
   {PASSWORDを入力}
   ```

## Author

- kon
