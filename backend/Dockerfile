FROM ruby:2.6.5

# 必要なパッケージのインストール（基本的に必要になってくるものだと思うので削らないこと）
RUN apt-get update -qq && \
    apt-get install -y build-essential \ 
                       libpq-dev \        
                       nodejs 

ENV APP /usr/src/app
RUN mkdir $APP
WORKDIR $APP

RUN gem install bundler

COPY Gemfile* $APP/
RUN bundle install -j3 --path vendor/bundle

COPY . $APP/

RUN gem install rails
RUN bundle

CMD ["rails", "server", "-p", "3000", "-b", "0.0.0.0"]

