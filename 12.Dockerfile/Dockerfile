FROM ubuntu:20.04

RUN apt-get update -qq && DEBIAN_FRONTENT=noninteractive apt-get install -qqy --no-install-recommends \
        gnupg2 \
        software-properties-common \
        wget; \
    add-apt-repository "deb http://apt.llvm.org/focal/ llvm-toolchain-focal-12 main"; \
    add-apt-repository "deb-src http://apt.llvm.org/focal/ llvm-toolchain-focal-12 main"; \
    wget -O - https://apt.llvm.org/llvm-snapshot.gpg.key | apt-key add -;
RUN apt-get update -qq && DEBIAN_FRONTENT=noninteractive apt-get install -qqy --no-install-recommends \
        clang-12 \
        clang-tidy-12 \
        clang-format-12 \
        cmake \
        git \
        libc++-12-dev \
        llvm-12 \
        make \
        python3-pip
RUN python3 -m pip install gcovr

RUN ln -s /usr/bin/clang-tidy-12 /usr/bin/clang-tidy
RUN ln -s /usr/bin/clang-format-12 /usr/bin/clang-format
RUN ln -s /usr/lib/llvm-12/lib/libc++abi.so.1.0 /usr/local/lib/libc++abi.so

ENV CC /usr/bin/clang-12
ENV CXX /usr/bin/clang++-12
