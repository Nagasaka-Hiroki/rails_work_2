# Bookmark_list
　railsの練習と学習の記録。

## 製作背景
　ブラウザにはブックマーク機能が備わっており、ブックマークすることでブラウザからの再アクセスを容易にすることができる。頻繁にアクセスするサイトについては利用者もブックマークの位置を覚えていたり、わかりやすい位置に置くなどの工夫をすることで操作量を減らすことができる。しかし過去にブックマークしたページが増えてブックマーク内で検索することが困難になることがある。もちろんブックマーク自体もディレクトリ構造があり、わかりやすく保存することで検索時間を削減することができると考えられる。しかし使用する上では少し不便を感じることがある。

　ディレクトリ構造的なブックマークの保存は階層的な属性を付与することに相当する。しかし、必ずしも属性が階層的な状態が適切とは限らない。場合によっては階層的でなく水平的に、すなわち単純に複数の属性を持つ方がユーザとしては都合がいいことがある。そこでディレクトリ的ではなくリレーショナルデータベースによるブックマークの保存とすれば、複数の属性を一つのブックマークに付与することが可能になり、検索性を向上することができると考えた。そこでデータベースを使用した簡単なブックマーク管理アプリを作ることを考えた。

## 前提
　ローカル上で動き、利用者は一人。そのため認証などのセキュリティ面の作り込みはしない。  
使用するフレームワークはRuby on Railsとする。単純なアプリにRailsは大きすぎるかもしれないがこの点は問題としない。  

動作環境はDockerとし、以前に作った[Dockerfile](https://github.com/Nagasaka-Hiroki/rails_container)を使ってイメージを作る。  
~~(しかしこのファイルは別の開発途中で不足分が明らかになったり、HTTPサーバ化する際に必要なツールのインストールに未対応などの問題点がある。希望的観測であるがこの点についてこのアプリを作る過程で解決できないかと考えている。)~~

## バージョンなど
使用する言語などのバージョンや種類についてメモする。

|言語など|内容|
|-|-|
|言語|Ruby 3.1.2|
|Webフレームワーク|Ruby on Rails 7.0.4|
|データベース|SQLite(単純にaptでインストール)|
|ブラウザ|Chrome or Firefox|
