FROM crsmithdev/ubuntu:latest

WORKDIR /tmp
RUN wget http://download.redis.io/releases/redis-stable.tar.gz 2>/dev/null
RUN tar xvf redis-stable.tar.gz
RUN cd redis-stable && make && make install
RUN mkdir -p /etc/redis
RUN cp redis-stable/redis.conf /etc/redis
RUN rm -rf redis-stable

RUN mkdir -p /data
WORKDIR /data
VOLUME ["/data"]
EXPOSE 6379

CMD ["redis-server", "/etc/redis/redis.conf"]
