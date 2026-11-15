# Pinned to a specific digest so Renovate can track and update it automatically.
# The digest ensures reproducible builds even if the tag is re-pushed upstream.
FROM node:lts-alpine3.22@sha256:191c9f0080fcbbc6547a85dc0ff7988072214a355aabdc1d2ec55a7dae5eea8a

RUN apk add --no-cache git openssh && \
    apk add --no-cache --upgrade grep
# zenn-cli and textlint come from package.json / package-lock.json
# (installed by postCreateCommand), so their versions have a single source of truth.

USER node

WORKDIR /workspaces/zenn-content
