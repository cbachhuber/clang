FROM ubuntu:20.04

RUN apt-get update -qq; \
    apt-get install -qqy --no-install-recommends \
        gnupg2 \
        software-properties-common \
        wget; \
    add-apt-repository "deb http://apt.llvm.org/focal/ llvm-toolchain-focal-11 main"; \
    add-apt-repository "deb-src http://apt.llvm.org/focal/ llvm-toolchain-focal-11 main"; \
    wget -O - https://apt.llvm.org/llvm-snapshot.gpg.key | apt-key add -; \
    apt-get update -qq; \
    apt-get install -qqy --no-install-recommends \
        clang-11 \
        clang-tidy-11 \
        clang-format-11 \
        cmake \
        git \
        make

ENV CC /usr/bin/clang-11
ENV CXX /usr/bin/clang++-11
