FROM alpine:3.4
MAINTAINER Theo Chamley <theo.ch@mley.fr>

RUN apk add --no-cache \
    git \
    py-pip && \
    git clone https://github.com/oliver006/elasticsearch-test-data.git && \
    pip install -r elasticsearch-test-data/requirements.txt && \
    rm -rf /elasticsearch-test-data/.git && \
    apk del git

ENTRYPOINT [ "/elasticsearch-test-data/es_test_data.py" ]
