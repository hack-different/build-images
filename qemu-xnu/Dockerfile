FROM ubuntu:latest

RUN apt update && apt upgrade -y && apt install -y apt-utils
RUN TZ=Etc/UTC ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
RUN DEBIAN_FRONTEND=noninteractive TZ=Etc/UTC apt-get -y install tzdata

RUN apt install -y git libglib2.0-dev libfdt-dev libpixman-1-dev zlib1g-dev libtasn1-dev ninja-build build-essential cmake

RUN git clone https://github.com/lzfse/lzfse /opt/lzfse
RUN cd /opt/lzfse && mkdir build && cd build && cmake .. && make && make install
