FROM nvidia/cuda:11.2.0-runtime-ubuntu18.04

ENV PYTHON_VERSION=3.9.9
ARG CUDNN_FILENAME

# Install cuDNN
COPY ./${CUDNN_FILENAME} .

RUN apt install ./${CUDNN_FILENAME}

# Install Python
RUN apt update && \
    apt install -y build-essential zlib1g-dev libncurses5-dev libgdbm-dev libnss3-dev libssl-dev \
    libreadline-dev libffi-dev libsqlite3-dev wget libbz2-dev

RUN cd /tmp && \
    wget https://www.python.org/ftp/python/${PYTHON_VERSION}/Python-${PYTHON_VERSION}.tgz && \
    tar -xf Python-${PYTHON_VERSION}.tgz

RUN cd /tmp/Python-${PYTHON_VERSION} && \
    ./configure --enable-optimizations && \
    make -j 12 && \
    make install

RUN ln -s /usr/local/bin/python3 /usr/local/bin/python && \
    ln -s /usr/local/bin/pip3 /usr/local/bin/pip

# Clean
RUN rm ./${CUDNN_FILENAME} && \
    apt remove -y build-essential zlib1g-dev libncurses5-dev libgdbm-dev libnss3-dev libssl-dev \
      libreadline-dev libffi-dev libsqlite3-dev wget libbz2-dev && \
    apt clean && \
    rm -rf /tmp/*

CMD /usr/local/bin/python
