FROM alpine:3.4

ENV HUGO_VERSION 0.26

RUN apk add --update curl \
    python \
    py-pip \
    && pip install Pygments

RUN curl -L https://github.com/gohugoio/hugo/releases/download/v${HUGO_VERSION}/hugo_${HUGO_VERSION}_Linux-64bit.tar.gz | tar xvz -C /tmp && \
    mv /tmp/hugo /usr/local/bin/hugo && \
    rm -rf /tmp/* && \
    chmod 777 /tmp

WORKDIR /var/tmp/site

ENTRYPOINT ["hugo"]
