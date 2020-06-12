FROM gitlab/gitlab-runner:alpine

RUN apk add --no-cache \
    docker=18.09.8-r0 \
    curl \
    python \
    python2-dev \
    musl-dev \
    libffi-dev \
    openssl-dev \
    gcc \
    make

RUN python -m ensurepip && \
    rm -r /usr/lib/python*/ensurepip && \
    pip install --upgrade pip setuptools && \
    pip install docker-compose && \
    rm -r /root/.cache

RUN adduser gitlab-runner docker
RUN adduser gitlab-runner ping