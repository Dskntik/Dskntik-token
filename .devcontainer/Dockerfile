FROM ubuntu:22.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt update && \
    apt install -y curl git cmake build-essential clang python3-pip pkg-config libssl-dev libgmp-dev zlib1g-dev && \
    apt clean && rm -rf /var/lib/apt/lists/*

# Install func & fift
RUN git clone https://github.com/ton-blockchain/ton.git /opt/ton && \
    cd /opt/ton && \
    git submodule update --init --recursive && \
    cmake . && \
    make -j$(nproc)

ENV PATH="/opt/ton/build:/opt/ton/bin:$PATH"

WORKDIR /workspace
