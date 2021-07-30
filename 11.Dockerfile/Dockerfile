FROM ubuntu:20.04

RUN apt-get update -qq && DEBIAN_FRONTEND=noninteractive apt-get install -qqy --no-install-recommends \
        gnupg2 \
        software-properties-common \
        wget; \
    add-apt-repository "deb http://apt.llvm.org/focal/ llvm-toolchain-focal-11 main"; \
    add-apt-repository "deb-src http://apt.llvm.org/focal/ llvm-toolchain-focal-11 main"; \
    wget -O - https://apt.llvm.org/llvm-snapshot.gpg.key | apt-key add -;
RUN apt-get update -qq && DEBIAN_FRONTEND=noninteractive apt-get install -qqy --no-install-recommends \
        clang-11 \
        clang-tidy-11 \
        clang-format-11 \
        cmake \
        git \
        libc++-11-dev \
        llvm-11 \
        make \
        python3-pip
RUN python3 -m pip install gcovr

RUN ln -s /usr/bin/clang-tidy-11 /usr/bin/clang-tidy
RUN ln -s /usr/bin/clang-format-11 /usr/bin/clang-format
RUN ln -s /usr/lib/llvm-11/lib/libc++abi.so.1.0 /usr/local/lib/libc++abi.so

ENV CC /usr/bin/clang-11
ENV CXX /usr/bin/clang++-11
