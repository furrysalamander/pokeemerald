FROM debian:bullseye-slim
RUN apt update && apt install -y build-essential binutils-arm-none-eabi git libpng-dev \
    && rm -rf /var/lib/apt/lists/*

WORKDIR /tmp
RUN git clone https://github.com/furrysalamander/agbcc && \
    cd agbcc && \
    ./build.sh && \
    ./install.sh && \
    cd .. && rm -rf agbcc

ENV AGBCC=/opt/pret/agbcc
WORKDIR /usr/src

