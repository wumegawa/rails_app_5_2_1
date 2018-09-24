# README

## 事前準備
- gitとdockerをインストールしてください
- ソースをクローンしてください

## 新規railsプロジェクト作成(新規のみ)
1. 初期フォルダー作成

  `cp -r rails_app_5_2_1/ [プロジェクトフォルダ名]/`

2. プロジェクトフォルダへ移動

  `cd [プロジェクトフォルダ名]`

## rails app初期作成(新規のみ)
1. app作成

  `docker-compose run web rails new . --force --database=mysql`

2. docekerイメージ再ビルド

  `docker-compose build`

3. コンテナ起動

  `docker-compose up -d`

4. rails server起動

  `docker-compose run web rake db:create`

5. コンテナ停止

  `docker-compose down`

## app開発時用
- コンテナ起動

  `docker-compose up -d`

- コンテナ停止

  `docker-compose down`

## コンテナへ入りたい時用
- appコンテナへ

  `docker-compose exec web bash`

- dbコンテナへ

  `docker-compose exec db bash`

## 参考
- [Rails] DockerでRails + MySQLの開発環境をつくる手順

  https://qiita.com/jshimazu/items/ba13ce87dfdb11e2d1d9
