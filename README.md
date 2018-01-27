# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...

## 導入まで

```sh
$ git clone <プロジェクトURL>
$ cd fasch
$ bundle
$ cp config/database.yml.sample config/database.yml
# 自分の環境に合わせて書き換えてください
$ bin/rails s
```

### トラブルシューティング

#### gem 'pg' のインストールに失敗する

`pg_config` を設定してみてください。

1. pg_configのファイルがどこにあるか探す (以下、仮に `/usr/pgsql-10/bin/pg_config` とする)
2. `bundle config build.pg --with-pg-config=/usr/pgsql-10/bin/pg_config`
3. bundle

#### DBが作成できない


```FATAL: Peer authentication failed for user ""```
このエラーが発生する場合は、Peer認証が有効になっています。

ユーザ名とUnixユーザ名を一致させるか、認証方法を変更してください。
認証変更は `pg_hba.conf` のファイルを編集することで行なえます。