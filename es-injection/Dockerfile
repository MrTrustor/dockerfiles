FROM python:2.7
MAINTAINER Theo Chamley <theo.ch@mley.fr>

RUN git clone https://github.com/oliver006/elasticsearch-test-data.git && \
    pip install -r elasticsearch-test-data/requirements.txt && \
    ln -s /usr/local/bin/python /usr/bin/python

ENTRYPOINT [ "/elasticsearch-test-data/es_test_data.py" ]
