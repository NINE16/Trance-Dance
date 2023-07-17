FROM node:14

WORKDIR /usr/src/app

EXPOSE 3000

RUN npx create-react-app .
COPY /node/src/App.js /usr/src/app/src/App.js
COPY /node/src/cow.svg /usr/src/app/src/
COPY /node/src/App.css /usr/src/app/src/App.css


RUN npm ci
RUN npm run build

CMD [ "npx", "serve", "build" ]


