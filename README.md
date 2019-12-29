# nut-upsd

[![pipeline status](https://git.ethitter.com/docker/nut-upsd/badges/master/pipeline.svg)](https://git.ethitter.com/docker/nut-upsd/commits/master)

Fully-customizable `nut` instance in a container. Many images exist, but they are
feature-limited due to how `nut`'s configuration is handled. This image aims to
provide all `nut` options without making too many compromises.

## Usage

1. Create necessary configurations in `./config`; `.conf`, `.html`, and `.users`
files are supported. **`./config` includes sample configurations.**
1. `docker-compose up -d`
1. If `MODE` is set to `netserver`, `nut` will be available on the container's 
port `3493`. Confirm using `telnet`:
    ```bash
    $ telnet [CONTAINER IP] 3493
    Trying [CONTAINER IP]...
    Connected to [CONTAINER IP].
    Escape character is '^]'.
    
    $ LIST UPS
    BEGIN LIST UPS
    UPS test "Back-UPS XS 1500 Test"
    END LIST UPS
    ```
