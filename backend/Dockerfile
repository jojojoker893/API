FROM ruby:3.4.2

WORKDIR /usr/src/app

ENV LANG C.UTF-8
ENV TZ Asia/Tokyo

RUN apt-get update -qq && \
    apt-get install -y --no-install-recommends \
    build-essential \
    git \
    default-mysql-client \
    less \
    vim && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

COPY backend/Gemfile* ./
RUN bundle install

