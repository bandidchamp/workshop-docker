FROM node:17-buster-slim

WORKDIR /usr/src/app
COPY ./package.json .
COPY ./server.js .

RUN ls /usr/src/app

RUN yarn

COPY . /usr/src/app

RUN set -x && apt-get update

CMD ["node", "./server.js", "&"]