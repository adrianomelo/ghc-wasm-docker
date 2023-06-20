from debian:12

WORKDIR /build

RUN apt update && apt install curl git jq unzip build-essential -y

# RUN curl --proto '=https' --tlsv1.2 -sSf -L https://install.determinate.systems/nix > /build/nix-installer \
#     && /build/nix-installer install linux --init none --extra-conf "filter-syscalls = false" \
#     && . /nix/var/nix/profiles/default/etc/profile.d/nix-daemon.sh

RUN git clone https://gitlab.haskell.org/ghc/ghc-wasm-meta.git \
    && cd ghc-wasm-meta \
    && PREFIX=/usr/local/bin ./setup.sh

CMD ["/usr/local/bin/env"]
