FROM node:22-slim

# Install only essential dependencies for node-gyp + Chromium
RUN apt-get update && apt-get install -y --no-install-recommends \
    python3 \
    python3-setuptools \
    make \
    g++ \
    git \
    openssh-client \
    curl \
    awscli \
    groff-base \
    less \
    mailcap \
    udev \
    fonts-freefont-ttf \
    chromium \
    ca-certificates \
  && apt-get clean \
  && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

# Install Sentry CLI
RUN curl -sL https://sentry.io/get-cli/ | bash

# Environment variables for Chromium & Node
ENV CHROME_BIN=/usr/bin/chromium
ENV LIGHTHOUSE_CHROMIUM_PATH=/usr/bin/chromium
ENV NODE_OPTIONS=--max-old-space-size=8192
ENV PYTHON=/usr/bin/python3
