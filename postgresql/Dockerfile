FROM crsmithdev/ubuntu:latest

RUN DEBIAN_FRONTEND=noninteractive apt-get update && apt-get install -yq \
    postgresql-9.4 \
    postgresql-contrib-9.4 \
    postgresql-client-9.4

RUN mkdir -p /data
RUN chown postgres:postgres /data

ADD postgresql.conf /etc/postgresql/9.4/main/postgresql.conf
ADD pg_hba.conf /etc/postgresql/9.4/main/pg_hba.conf
ADD start /start

VOLUME ["/data"]
EXPOSE 5432
CMD ["./start"]

