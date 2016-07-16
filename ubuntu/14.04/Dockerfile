FROM ubuntu:14.04

RUN DEBIAN_FRONTEND=noninteractive apt-get -q update && apt-get -yq install \
    apt-transport-https \
    ca-certificates \
    build-essential \
    curl \
    wget

CMD ["/bin/bash"]
