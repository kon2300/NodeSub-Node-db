# NodeSub-Node-db

- 勉強用の課題です

## Description

- **[Docker](https://www.docker.com/products/docker-desktop)** を使用し **[Node.js](https://nodejs.org/ja/)** と **[Mysql](https://www.mysql.com/jp/)** を接続しています

## Requirement

- [Docker](https://www.docker.com/products/docker-desktop)/docker-compose 3.8

## Usage

1. `.env` ファイル を作成します

   ```sh
   $ cp .env.example .env
   ```

1. イメージを構築するため [Docker](https://www.docker.com/products/docker-desktop) をインストールし `docker-compose.yml` のある場所で下記のコマンドを実行します

   ```sh
   $ docker-compose build
   ```

1. コンテナを起動するため `docker-compose.yml` のある場所で下記のコマンドを実行します

   ```sh
   $ docker-compose up
   ```

## Author

- kon
