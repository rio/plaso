FROM python:3

ARG UID=1000

RUN useradd -m --uid ${UID} vscode && \
    apt-get update -y && \
    export DEBIAN_FRONTEND=noninteractive && \
    apt-get install -y --no-install-recommends sudo

RUN /bin/bash -c "cat > /etc/sudoers.d/10-vscode <<<'vscode ALL=(ALL:ALL) NOPASSWD:ALL'"
