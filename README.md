# wordpress_docker_apache_mysql

## 概要

WordPressを立ち上げるDocker Compose構成です。

## 起動

### 1. .envの設定を適宜編集する

- `COMPOSE_PROJECT_NAME`を編集し、Dockerコンテナ名のprefixを適宜編集する。
- `MYSQL_****`を編集し、MySQLの設定を適宜編集する。

### 2. Dockerコンテナを起動する

```bash
docker-compose up
```

以下のようなログが出力され、ログが落ち着いたら起動完了。

```bash
    :
db_1   | 2022-02-09T08:33:41.056378Z 0 [Note] mysqld: ready for connections.
db_1   | Version: '5.7.36'  socket: '/var/run/mysqld/mysqld.sock'  port: 3306  MySQL Community Server (GPL)
    :
app_1  | [Wed Feb 09 08:33:41.073296 2022] [mpm_prefork:notice] [pid 1] AH00163: Apache/2.4.52 (Debian) PHP/7.4.27 configured -- resuming normal operations
app_1  | [Wed Feb 09 08:33:41.073322 2022] [core:notice] [pid 1] AH00094: Command line: 'apache2 -D FOREGROUND'
```

### 3. WordPressの初期セットアップを行う

ブラウザで`localhost:8080`にアクセスし、WordPressの初期設定・ログインを行う。
