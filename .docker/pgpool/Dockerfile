FROM debian:bullseye

RUN apt-get update && \
    apt-get -y install lsb-release nano procps wget gnupg2 && \
    sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt $(lsb_release -cs)-pgdg main" > /etc/apt/sources.list.d/pgdg.list' && \
    wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | apt-key add - && \
    apt-get update && \
    apt-get -y install pgpool2 libpgpool2 postgresql-16-pgpool2

EXPOSE 5432