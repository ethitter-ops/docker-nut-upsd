FROM debian:buster-slim

LABEL maintainer="ethitter"
LABEL version="1.0"

RUN echo "deb http://security.debian.org/ buster/updates main" >> /etc/apt/sources.list

RUN apt-get update \
    && apt-get -y --no-install-recommends install \
        nut=2.7 \
    && apt-get autoremove -y \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

EXPOSE 3493

COPY entrypoint /usr/local/bin/
ENTRYPOINT ["entrypoint"]
