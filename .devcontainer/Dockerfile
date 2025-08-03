FROM ubuntu:22.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt update && \
    apt install -y curl git cmake build-essential clang python3-pip pkg-config libssl-dev libgmp-dev zlib1g-dev

# Install toncli
RUN pip3 install toncli

WORKDIR /workspace

