# Modern clang docker containers

[![docker](https://img.shields.io/docker/pulls/cbachhuber/clang.svg)](https://hub.docker.com/r/cbachhuber/clang/)

A docker container with modern cmake and clang. The cmake version provided by [silkeh/clang](https://github.com/silkeh/docker-clang) is too old for me, so I created this container.

Tags and corresponding docker files:

- `11`: [/11.Dockerfile](https://github.com/cbachhuber/clang/blob/master/11.Dockerfile/Dockerfile) contains
  - clang-11
  - clang-tidy-11
  - clang-format-11
  - cmake 3.16.3
  - llvm-tools-11
  - gcovr 4.2
- `latest`: [/11.Dockerfile](https://github.com/cbachhuber/clang/blob/master/11.Dockerfile/Dockerfile[) contains
  - clang-11
  - clang-tidy-11
  - clang-format-11
  - cmake 3.16.3
  - llvm-tools-11
  - gcovr 4.2
