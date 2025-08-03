FROM ubuntu:22.04

ENV DEBIAN_FRONTEND=noninteractive

# Install dependencies
RUN apt update && \
    apt install -y curl git cmake build-essential clang python3-pip pkg-config libssl-dev libgmp-dev zlib1g-dev && \
    apt clean && \
    rm -rf /var/lib/apt/lists/*

# Install toncli
RUN pip3 install toncli

# Create vscode user and set up home directory
RUN useradd -m -s /bin/bash vscode && \
    chown -R vscode:vscode /workspace

USER vscode

WORKDIR /workspace
