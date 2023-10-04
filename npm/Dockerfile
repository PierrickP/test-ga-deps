# App build

FROM node:18-alpine as build-stage

WORKDIR /app

ARG MODE=production

ENV MODE=${MODE}

ENV NODE_OPTIONS="--max_old_space_size=4096"
COPY package.json .
COPY package-lock.json .

RUN npm ci
