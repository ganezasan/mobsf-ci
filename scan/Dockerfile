FROM ruby:2.5-alpine

WORKDIR /app

COPY Gemfile Gemfile.lock /app/

RUN bundle && apk add --update bash

COPY . .

RUN ls -la /app/

CMD ./wait-for-it.sh mobsf:8000 -- ruby scan.rb
