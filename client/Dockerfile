FROM node:16.15.1-alpine3.16

ARG NODE_ENV="development"

RUN apk add --no-cache python3 make g++

RUN mkdir -p ./client

WORKDIR /client

COPY package*.json ./

COPY . .

EXPOSE 3000

RUN npm install

RUN chown -R node:node /client/node_modules

CMD npm start
