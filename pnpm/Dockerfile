# App build

FROM node:18-alpine as build-stage

RUN corepack enable

WORKDIR /app

ARG MODE=production

ENV MODE=${MODE}

ENV NODE_OPTIONS="--max_old_space_size=4096"
COPY package.json .
COPY pnpm-lock.yaml .

RUN corepack pnpm@8.8.0 install --frozen-lockfile
