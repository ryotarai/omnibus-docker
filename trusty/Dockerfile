FROM ubuntu:14.04
RUN cat /etc/apt/sources.list | sed -e 's|http://[^ ]*|mirror://mirrors.ubuntu.com/mirrors.txt|g' > /tmp/sources.list && mv /tmp/sources.list /etc/apt/sources.list
RUN apt-get update && \
  apt-get install -y software-properties-common git-core build-essential autoconf && \
  apt-add-repository -y ppa:brightbox/ruby-ng && \
  apt-get update && \
  apt-get install -y ruby2.2 ruby2.2-dev
RUN gem install bundler omnibus berkshelf test-kitchen
