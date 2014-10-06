FROM crsmithdev/ubuntu:14.04

ENV GOPATH /go
ENV GOROOT /usr/local/go
ENV PATH $PATH:$GOPATH/bin:$GOROOT/bin

RUN DEBIAN_FRONTEND=noninteractive apt-get update && apt-get install -yq \
    git \
    bzr \
    mercurial

WORKDIR /tmp
RUN wget --quiet https://godeb.s3.amazonaws.com/godeb-amd64.tar.gz
RUN tar xvf godeb-amd64.tar.gz
RUN ./godeb install 1.3.3
RUN rm -rf godeb-amd64.tar.gz godeb

WORKDIR /go
VOLUME ["/go"]

EXPOSE 8080


