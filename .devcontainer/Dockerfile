FROM node:lts-alpine3.17

RUN apk update && \
    apk --no-cache add git openssh && \
    apk --no-cache add --upgrade grep
RUN npm install -g zenn-cli@latest \
    textlint \
    textlint-rule-preset-ja-spacing \
    textlint-rule-preset-ja-technical-writing \
    textlint-rule-spellcheck-tech-word

# copy all files to cache packages
COPY . .

USER node

WORKDIR /workspaces/zenn-content

