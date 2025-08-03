FROM ubuntu:22.04

ENV DEBIAN_FRONTEND=noninteractive

# Install dependencies
RUN apt update && \
    apt install -y curl git cmake build-essential clang python3-pip pkg-config libssl-dev libgmp-dev zlib1g-dev liblz4-dev libsodium-dev && \
    apt clean && \
    rm -rf /var/lib/apt/lists/*

# Install TON tools (func, fift) by building from source
RUN git clone --recursive https://github.com/ton-blockchain/ton.git /ton && \
    cd /ton && \
    mkdir build && cd build && \
    cmake -DCMAKE_BUILD_TYPE=Release .. && \
    make -j4 func fift && \
    cp func/fift /usr/local/bin/fift && \
    cp func/func /usr/local/bin/func && \
    chmod +x /usr/local/bin/func /usr/local/bin/fift && \
    cd / && rm -rf /ton

# Create workspace directory and set up vscode user
RUN mkdir -p /workspace && \
    useradd -m -s /bin/bash vscode && \
    chown -R vscode:vscode /workspace

USER vscode

WORKDIR /workspace
