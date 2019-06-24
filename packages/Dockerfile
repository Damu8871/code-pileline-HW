FROM debian:jessie

MAINTAINER test@dockertest.com

RUN apt-get update

RUN apt-get install -y software-properties-common

RUN add-apt-repository "deb http://ppa.launchpad.net/webupd8team/java/ubuntu xenial main"

RUN apt-get update

RUN echo debconf shared/accepted-oracle-license-v1-1 select true |  debconf-set-selections
RUN echo debconf shared/accepted-oracle-license-v1-1 seen true |  debconf-set-selections

RUN apt-get install -y oracle-java8-installer

RUN javac -version
