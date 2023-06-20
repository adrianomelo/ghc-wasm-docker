from debian:12

WORKDIR /build

RUN apt update && apt install curl jq unzip gcc make xz-utils -y

RUN curl --proto '=https' --tlsv1.2 -sSf -L https://gitlab.haskell.org/ghc/ghc-wasm-meta/-/archive/master/ghc-wasm-meta-master.tar.gz | tar xz

RUN cd ghc-wasm-meta-master && PREFIX=/usr/local/bin ./setup.sh
