#
# Oracle Java 7 
# Fork from dockerfile to support Ubuntu 12.04
#
# https://github.com/dockerfile/java
# https://github.com/chrisduong/java
# https://github.com/dockerfile/java/tree/master/oracle-java7
# https://github.com/chrisduong/java/tree/master/oracle-java7/precise
#

# Pull base image.
FROM chrisduong/ubuntu:dockerfile-12.04
MAINTAINER Chris Duong <chris.duong83@gmail.com>

# Install Java.
RUN \
  echo oracle-java7-installer shared/accepted-oracle-license-v1-1 select true | debconf-set-selections && \
  add-apt-repository -y ppa:webupd8team/java && \
  apt-get update && \
  apt-get install -y oracle-java7-installer && \
  rm -rf /var/lib/apt/lists/* && \
  rm -rf /var/cache/oracle-jdk7-installer

# Define working directory.
WORKDIR /data

# Define commonly used JAVA_HOME variable
ENV JAVA_HOME /usr/lib/jvm/java-7-oracle

# Define default command.
CMD ["bash"]
