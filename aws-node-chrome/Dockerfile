FROM node:14.17.6-alpine

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
    pip install --upgrade pip && \
    pip install --upgrade awscli==1.14.5 s3cmd==2.0.1 python-magic && \
    npm i npm@7 -g && \
    apk -v --purge del py-pip && \
    rm /var/cache/apk/*

RUN apk --no-cache upgrade && apk add --no-cache \
    udev \
    ttf-freefont \
    chromium

RUN curl -sL https://sentry.io/get-cli/ | bash

ENV CHROME_BIN /usr/bin/chromium-browser
ENV LIGHTHOUSE_CHROMIUM_PATH /usr/bin/chromium-browser
ENV NODE_OPTIONS --max-old-space-size=8192
