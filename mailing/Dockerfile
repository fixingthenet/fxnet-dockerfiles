FROM debian:jessie


RUN apt-get update -y && \
    apt-get install -y \
    build-essential \
    pkg-config \
    libncurses5-dev \
    libsieve2-dev \
    libglib2.0-dev \
    libgmime-2.6-dev \
    libldap2-dev \
    libzdb-dev \
    libmhash-dev \
    libevent-dev \
    libmysqlclient-dev \
    libpq-dev \
    libssl-dev \
    curl && \
    cd /usr/src && \
    curl -s http://dbmail.org/download/3.2/dbmail-3.2.3.tar.gz > dbmail.tar.gz && \
    tar -xzf dbmail.tar.gz

RUN cd /usr/src/dbmail-3.2.3 && \
    ./configure --with-lda --with-sieve && \
    make install

CMD /bin/bash

