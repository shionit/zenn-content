# Pinned to a specific digest so Renovate can track and update it automatically.
# The digest ensures reproducible builds even if the tag is re-pushed upstream.
FROM node:lts-alpine3.22@sha256:191c9f0080fcbbc6547a85dc0ff7988072214a355aabdc1d2ec55a7dae5eea8a

RUN apk update && \
    apk --no-cache add git openssh && \
    apk --no-cache add --upgrade grep
# Versions are pinned so Renovate can open PRs when newer releases are available.
RUN npm install -g \
    zenn-cli@0.4.7 \
    textlint@15.6.0 \
    textlint-rule-preset-ja-spacing@2.4.3 \
    textlint-rule-preset-ja-technical-writing@12.0.2 \
    textlint-rule-spellcheck-tech-word@5.0.0

# copy all files to cache packages
COPY . .

USER node

WORKDIR /workspaces/zenn-content

