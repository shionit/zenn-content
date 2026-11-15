# Node 26 (LTS) on the current Alpine release, pinned to a digest for reproducible builds.
# Renovate bumps the digest as the tag is rebuilt (new Node 26.x / Alpine) and opens a
# separate PR for the next Node major. Avoid "lts-alpineX.Y": those tags freeze over time.
FROM node:26-alpine@sha256:6bd9ab43c0ec0190ca7b2d193906cb8b7edf6e7f4afa43ddeccd6452710bffb5

RUN apk add --no-cache git openssh && \
    apk add --no-cache --upgrade grep
# zenn-cli and textlint come from package.json / package-lock.json
# (installed by postCreateCommand), so their versions have a single source of truth.

USER node

WORKDIR /workspaces/zenn-content
