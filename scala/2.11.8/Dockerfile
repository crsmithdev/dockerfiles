FROM crsmithdev/ubuntu:14.04

ENV SCALA_VERSION 2.11.8
ENV SBT_VERSION 0.13.11

RUN \
    sudo apt-get install -y openjdk-6-jre

RUN \
    sudo apt-get remove scala-library scala && \
    wget http://www.scala-lang.org/files/archive/scala-$SCALA_VERSION.deb && \
    sudo dpkg -i scala-$SCALA_VERSION.deb && \
    sudo apt-get update && \
    sudo apt-get install scala

RUN \
    wget http://dl.bintray.com/sbt/debian/sbt-$SBT_VERSION.deb && \
    sudo dpkg -i sbt-$SBT_VERSION.deb && \
    sudo apt-get update && \
    sudo apt-get install sbt && \
    sbt about

