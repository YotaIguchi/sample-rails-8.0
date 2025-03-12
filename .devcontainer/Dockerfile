# syntax=docker/dockerfile:1
FROM ruby:3.3.4

# 必要なパッケージをインストール
RUN apt-get update -qq && apt-get install -y \
  nodejs \
  yarn \
  build-essential \
  libpq-dev

# bundler のインストール（必要な場合）
RUN gem install bundler

# Rails 8.0 をインストール（必要に応じてバージョン指定）
RUN gem install rails -v 8.0.0

# 作業ディレクトリを作成し、設定
WORKDIR /workspace

# コンテナ内で Rails サーバーのデフォルトポート3000を公開
EXPOSE 3000

# コンテナ起動時は bash を起動
CMD [ "bash" ]
