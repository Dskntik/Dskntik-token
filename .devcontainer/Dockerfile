FROM ubuntu:22.04

ENV DEBIAN_FRONTEND=noninteractive

# Install dependencies
RUN apt update && \
    apt install -y curl git cmake build-essential clang python3-pip pkg-config libssl-dev libgmp-dev zlib1g-dev && \
    apt clean && \
    rm -rf /var/lib/apt/lists/*

# Install TON tools (func, fift)
RUN curl -sL https://github.com/ton-blockchain/ton/releases/download/v2023.06/ton-linux-x86_64 -o /usr/local/bin/ton && \
    chmod +x /usr/local/bin/ton

# Create workspace directory and set up vscode user
RUN mkdir -p /workspace && \
    useradd -m -s /bin/bash vscode && \
    chown -R vscode:vscode /workspace

USER vscode

WORKDIR /workspace
