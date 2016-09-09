#jeklly runtime util
FROM ruby:2.2-slim

MAINTAINER hualee215@gmail.com

RUN sed -i s/httpredir.debian.org/mirrors.aliyun.com/g /etc/apt/sources.list

RUN apt-get -y update  \
    && apt-get -y install ruby-dev build-essential

RUN gem source -r https://rubygems.org/ \
    && gem source -a https://gems.ruby-china.org \
    && gem install jekyll jekyll-paginate redcarpet kramdown  rouge jekyll-watch

#&& bundle config mirror.https://rubygems.org https://gems.ruby-china.org

WORKDIR /opt/site-src

# RUN bunlder to install gem packages

CMD jekyll build -s . -d /opt/site
