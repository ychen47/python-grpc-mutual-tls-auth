FROM amr-registry.caas.intel.com/rvm/rvm_pyhub_base:latest

VOLUME [ "/grpc-test" ]
VOLUME [ "/grpc-dev" ]

RUN export http_proxy=http://proxy-chain.intel.com:911  \
    && export https_proxy=http://proxy-chain.intel.com:911 \
    && pip3 install invoke \
    && apt-get install nano


COPY . /grpc-test/.

WORKDIR /grpc-test

CMD ["invoke", "server.run"]