FROM tanmer/ubuntu:trusty
MAINTAINER Xiaohui <xiaohui@tanmer.com>

RUN gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3
RUN \curl -sSL https://get.rvm.io | bash -s stable
RUN /bin/bash -l -c 'source /etc/profile.d/rvm.sh'
RUN /bin/bash -l -c 'echo "ruby_url=https://cache.ruby-china.org/pub/ruby" > /usr/local/rvm/user/db'
RUN /bin/bash -l -c 'rvm requirements'
