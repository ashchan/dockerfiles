FROM ubuntu:14.04
MAINTAINER James Chen <ashchan@gmail.com> (@ashchan)

RUN locale-gen --no-purge en_US.UTF-8
ENV LC_ALL en_US.UTF-8

ENV DEBIAN_FRONTEND noninteractive
RUN apt-get update
RUN apt-get upgrade -y

RUN apt-get install -y wget curl git git-core build-essential \
    libmysqlclient-dev libpq-dev \
    zlib1g-dev libssl-dev libreadline-dev libyaml-dev libsqlite3-dev sqlite3 libxml2-dev libxslt1-dev

RUN wget -O ruby-2.1.5.tar.gz http://ftp.ruby-lang.org/pub/ruby/2.1/ruby-2.1.5.tar.gz
RUN tar -xzf ruby-2.1.5.tar.gz
RUN cd ruby-2.1.5/ && ./configure && make && make install

RUN echo "gem: --no-ri --no-rdoc" > ~/.gemrc
RUN gem install bundler
