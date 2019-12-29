# nut-upsd

Fully-customizable `nut` instance in a container. Many images exist, but they are
feature-limited due to how `nut`'s configuration is handled. This image aims to
provide all `nut` options without making too many compromises.

## Usage

1. Copy any of the `./config/*.conf.sample` files to `./config/[FILENAME].conf`
and modify as needed.
1. `docker-compose up -d`
1. `nut` will be available on the container's port `3493`.
