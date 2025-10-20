FROM ubuntu:22.04

RUN apt-get update && apt-get install -y \
    ninja-build \
    xorg-dev \
    libglu1-mesa-dev \
    libxrandr-dev \
    libxi-dev \
    libxinerama-dev \
    libxcursor-dev \
    libxxf86vm-dev \
    cmake \
    build-essential \
    git \
    wget

RUN cd /usr/local && \
    wget https://github.com/mstorsjo/llvm-mingw/releases/download/20230614/llvm-mingw-20230614-ucrt-ubuntu-20.04-x86_64.tar.xz && \
    tar xf llvm-mingw-20230614-ucrt-ubuntu-20.04-x86_64.tar.xz --strip-components=1 && \
    rm llvm-mingw-20230614-ucrt-ubuntu-20.04-x86_64.tar.xz

ENV PATH="/usr/local/bin:$PATH"
