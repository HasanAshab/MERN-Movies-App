FROM node:20-alpine

WORKDIR /app

COPY package*.json .

RUN npm install

copy . .

EXPOSE 5000

CMD ["nodemon","index.js"]
