FROM ruby:2.3
RUN echo 'deb http://mirrors.163.com/debian jessie main' > /etc/apt/sources.list    
RUN gem sources --add https://gems.ruby-china.org/ --remove https://rubygems.org/
RUN bundle config mirror.https://rubygems.org https://gems.ruby-china.org
ENV GEM_HOME /cache/bundle
ENV BUNDLE_PATH /cache/bundle
RUN mkdir /root/.ssh

RUN apt-get update && \
    apt-get install -y --no-install-recommends \
    build-essential \
    libmysqlclient-dev

RUN curl -sL https://deb.nodesource.com/setup_7.x | bash - &&\
    apt-get install -y \
    nodejs

RUN rm -rf /var/lib/apt/lists/*
