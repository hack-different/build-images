FROM ubuntu:latest

ARG DEBIAN_FRONTEND=noninteractive

RUN apt update && apt upgrade -y
RUN apt install -y git libglib2.0-dev libfdt-dev libpixman-1-dev zlib1g-dev libtasn1-dev ninja-build build-essential cmake

RUN git clone https://github.com/lzfse/lzfse /opt/lzfse
RUN cd /opt/lzfse && mkdir build && cd build && cmake .. && make && make install
