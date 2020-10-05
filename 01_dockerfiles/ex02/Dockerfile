FROM ruby:2.6.5
MAINTAINER Ndaniell School 21
RUN apt-get update
RUN apt-get install -y build-essential libpq-dev nodejs sqlite3
ONBUILD COPY app /opt/app
ONBUILD WORKDIR /opt/app
ONBUILD EXPOSE 3000
ONBUILD RUN gem install bundler:1.16.3
ONBUILD RUN gem install execjs
ONBUILD RUN bundle install
ONBUILD RUN rake db:migrate
ONBUILD RUN rake db:seed
# docker run --rm -it -p 3000:3000 ex02
