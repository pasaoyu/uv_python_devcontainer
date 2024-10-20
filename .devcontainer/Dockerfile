FROM debian:bullseye-slim AS builder

RUN apt-get update && \
    apt-get install -y \
    curl \
    && rm -rf /var/lib/apt/lists/*

# install uv
RUN curl -LsSf https://astral.sh/uv/install.sh | bash

#==================================================
FROM debian:bullseye-slim

RUN apt-get update && \
    apt-get install -y \
    ca-certificates \
    git \
    sudo \
    && rm -rf /var/lib/apt/lists/* && \
    # add vecode user
    useradd -m vscode && \
    # give vscode user sudo privileges
    echo "vscode ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers

# copy uv from builder
COPY --from=builder /root/.cargo/bin/uv /usr/local/bin/uv
COPY --from=builder /root/.cargo/bin/uvx /usr/local/bin/uvx

USER vscode
