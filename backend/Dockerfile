FROM node:20

WORKDIR ./app

RUN npm install express cookieParser dotenv path

COPY . .

EXPOSE 3000

CMD ["node","index.js"]
