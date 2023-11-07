# 環境の立ち上げ方

## projectフォルダに移動する
~~~
cd project
~~~

## イメージの作成
~~~
docker-compose build
~~~

## コンテナの作成

~~~
docker-compose up -d
~~~

## Wordpressの初期設定を行う

webブラウザで下記URLを入力して検索を行う
~~~
http://localhost:80
~~~

参考文献:<br>
[docker-compose を使って WordPress テーマ開発環境を構築しよう](https://blog.recruit.co.jp/rmp/infrastructure/post-11266/)<br>
[Docker-composeでWEB・DBのDockerfileよりwordpressを構築する](https://qiita.com/kasihko/items/4ebfee91f674f2ec04fa)
