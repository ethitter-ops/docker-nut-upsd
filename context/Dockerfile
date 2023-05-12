FROM debian:bookworm-slim

LABEL maintainer="ethitter"
LABEL version="1.1"

RUN apt-get update \
    && apt-get -y --no-install-recommends install \
    nut \
    && apt-get autoremove -y \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

EXPOSE 3493

COPY entrypoint /usr/local/bin/
ENTRYPOINT ["entrypoint"]
