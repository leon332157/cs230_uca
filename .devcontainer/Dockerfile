FROM --platform=linux/amd64 mcr.microsoft.com/devcontainers/base:jammy

RUN ln -fs /usr/share/zoneinfo/America/New_York /etc/localtime

RUN apt-get update && yes | unminimize

RUN apt-get update && apt-get install -y build-essential python3 python3-setuptools python3-dev python3-pip zip libgtest-dev cmake curl g++-11 libc6-dbg gdb valgrind git man-db manpages-posix

RUN apt-get update && cd /usr/src/gtest && cmake CMakeLists.txt && make && cp lib/*.a /usr/lib ; :

