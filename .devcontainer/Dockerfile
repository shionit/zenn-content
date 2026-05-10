# Pinned to a specific digest so Renovate can track and update it automatically.
# The digest ensures reproducible builds even if the tag is re-pushed upstream.
FROM node:lts-alpine3.22@sha256:f587a14b20e59fa6706b0bd82ef3ee330fd4c49f6372e37ed4920d0b6874e4ec

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

