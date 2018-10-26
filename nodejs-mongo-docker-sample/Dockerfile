FROM node:8.12.0-alpine

WORKDIR /usr/src/app

COPY ./package.json /usr/src/app

RUN ls -la

RUN npm install

RUN npm install pm2 -g

COPY . /usr/src/app

RUN ls -la

EXPOSE 3000

CMD ["pm2-docker", "start", "process.json"]
