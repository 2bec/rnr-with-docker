FROM ruby:2.5

# install dependencies
RUN apt-get update && apt-get install -y build-essential libpq-dev nodejs

# lets work
RUN mkdir /opt/app
WORKDIR /opt/app

# copy files and initiate
COPY Gemfile /opt/app/Gemfile
COPY Gemfile.lock /opt/app/Gemfile.lock

RUN bundle install

COPY . /opt/app