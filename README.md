# Modern clang docker containers

[![docker](https://img.shields.io/docker/pulls/cbachhuber/clang.svg)](https://hub.docker.com/r/cbachhuber/clang/)

A docker container with modern cmake and clang. The cmake version provided by [silkeh/clang](https://github.com/silkeh/docker-clang) is too old for me, so I created this container.

Tags and corresponding docker files:

- `11`: [11.Dockerfile/](https://github.com/cbachhuber/clang/blob/master/11.Dockerfile/Dockerfile) contains
  - clang-11
  - clang-tidy-11
  - clang-format-11
  - cmake 3.16.3
  - gcovr 4.2
  - libc++-11-dev
  - llvm-tools-11
- `12`: [12.Dockerfile/](https://github.com/cbachhuber/clang/blob/master/12.Dockerfile/Dockerfile) contains
  - clang-12
  - clang-tidy-12
  - clang-format-12
  - cmake 3.16.3
  - gcovr 4.2
  - libc++-12-dev
  - llvm-tools-12
- `latest` links to [12.Dockerfile/](https://github.com/cbachhuber/clang/blob/master/12.Dockerfile/Dockerfile).
