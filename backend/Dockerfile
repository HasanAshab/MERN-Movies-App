FROM node:20 AS base

WORKDIR /app

COPY package*.json .

RUN npm ci

copy . .

FROM node:20-alpine

WORKDIR /app

COPY --from=base /app /app

EXPOSE 3000

CMD ["node","index.js"]
