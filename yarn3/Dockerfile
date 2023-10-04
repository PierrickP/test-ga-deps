# App build

FROM node:18-alpine as build-stage

RUN corepack enable

WORKDIR /app

ARG MODE=production

ENV MODE=${MODE}

ENV NODE_OPTIONS="--max_old_space_size=4096"
COPY package.json .
COPY yarn.lock .

RUN corepack yarn@3.6.4 install --immutable
