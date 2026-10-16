FROM mcr.microsoft.com/devcontainers/base:bookworm

RUN apt-get update && apt-get install -y --no-install-recommends bash grep sed coreutils util-linux procps tar gzip nano && rm -rf /var/lib/apt/lists/*

ENV LANG=C.UTF-8
