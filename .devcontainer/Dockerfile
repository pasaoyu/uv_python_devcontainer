FROM python:3.12-slim

RUN apt-get update && \
    apt-get install -y --no-install-recommends \
    git && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* /var/cache/apt/* && \
    pip install --no-cache-dir --upgrade pip uv