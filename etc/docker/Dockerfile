#fpco/stack-run:lts-5
FROM fpco/stack-run@sha256:4b170ac899755a89c0295b7726c5530015211055125f6e3f6c5b902cb3e9b74b

RUN export DEBIAN_FRONTEND=noninteractive && \
    apt-get update && \
    wget -qO- https://get.haskellstack.org/ | sh -x && \
    unset DEBIAN_FRONTEND

RUN mkdir --parents /app/db
COPY _artifacts/casa-curator /usr/local/bin/casa-curator
COPY _artifacts/curator /usr/local/bin/curator
