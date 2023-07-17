FROM node:fermium-alpine

WORKDIR /usr/src/app
COPY package*.json ./

RUN npm install

RUN npm install glob rimraf

RUN npm run build
