FROM node:16

RUN apt-get update && apt-get upgrade -y
RUN apt-get install -y postgresql-client

WORKDIR /usr/src/app

RUN npm init -y
RUN npm install
RUN npm install nest
RUN npm install glob rimraf

EXPOSE 3000

RUN npm i -g @nestjs/cli
RUN nest new backend -p npm

WORKDIR /usr/src/app/backend

RUN npm run build

CMD ["node", "dist/main.js"]
