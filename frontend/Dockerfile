FROM node:20 AS builder

WORKDIR /app

COPY package*.json .

RUN npm ci

COPY . .

RUN npm run build


FROM node:20-alpine

WORKDIR /app

COPY --from=builder /app /app

RUN npm install -g serve

EXPOSE 3000

CMD ["serve","-s",".","-l","3000"]