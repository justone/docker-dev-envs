FROM nate/basedev

RUN apt-get update && apt-get install -y \
    ca-certificates \
    libsasl2-modules \
    lynx \
    elinks \
    mutt-dbg \
    mutt-patched \
    --no-install-recommends \
    && rm -rf /var/lib/apt/lists/*

ENV BROWSER lynx
