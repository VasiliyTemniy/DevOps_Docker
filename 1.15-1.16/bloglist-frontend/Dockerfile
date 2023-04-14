FROM node:16.17.0-bullseye-slim AS base

WORKDIR /usr/src/app

COPY package.json package.json
COPY package-lock.json package-lock.json

RUN npm install -g serve


FROM base AS build-stage
ENV NODE_ENV=production REACT_APP_BACKEND_URL=http://localhost:8080

COPY . .

RUN npm ci

RUN npm run build

CMD serve -s -l 3000 build