FROM debian:bullseye-slim
RUN apt update && apt install -y build-essential binutils-arm-none-eabi git libpng-dev \
    && rm -rf /var/lib/apt/lists/*

WORKDIR /workspaces
RUN git clone https://github.com/pret/agbcc && \
    cd agbcc && \
    ./build.sh
