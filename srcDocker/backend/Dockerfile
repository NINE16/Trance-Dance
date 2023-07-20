FROM node:16

RUN apt-get update && apt-get upgrade -y
RUN apt-get install -y postgresql-client

WORKDIR /usr/src/app

RUN npm init -y
RUN npm install
RUN npm install nest
RUN npm install glob rimraf


EXPOSE 3001

RUN npm i -g @nestjs/cli
# RUN npm install @nestjs/typeorm typeorm
RUN npm install pg
COPY backnest/ /usr/src/app/backend

# RUN nest new backend -p npm
# RUN nest generate module database


WORKDIR /usr/src/app/backend

RUN npm run build

CMD ["node", "dist/main.js"]
