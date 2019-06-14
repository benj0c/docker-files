FROM node:8.11.3-alpine

RUN apk -v --update add \
        bash \
        git \
        openssh \
        curl \
        python \
        py-pip \
        groff \
        less \
        mailcap \
        && \
    pip install --upgrade awscli==1.14.5 s3cmd==2.0.1 python-magic && \
    apk -v --purge del py-pip && \
    npm i npm@latest -g && \
    rm /var/cache/apk/*
