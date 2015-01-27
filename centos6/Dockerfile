FROM centos:6
ENV PATH /ruby-2.2/bin:$PATH
RUN cd $HOME && \
yum -y install git tar gcc libffi-devel make zlib-devel openssl-devel gcc-c++ libevent-devel autoconf && \
git clone https://github.com/tagomoris/xbuild.git && \
./xbuild/ruby-install 2.2.0 /ruby-2.2 && \
gem install bundler omnibus berkshelf test-kitchen --no-ri --no-rdoc
