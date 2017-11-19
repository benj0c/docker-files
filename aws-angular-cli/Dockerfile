FROM teracy/angular-cli

RUN apt-get update \
  && apt-get install -y python-dev \
  && cd /tmp \
  && curl -O https://bootstrap.pypa.io/get-pip.py \
  && python get-pip.py \
  && pip install awscli --upgrade --user \
  && echo 'alias aws="~/../root/.local/bin/aws"' >> ~/.bashrc \
  && apt-get clean \
  && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
