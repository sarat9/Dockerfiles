FROM alpine/git as repo
MAINTAINER sarat.e99@gmail.com Sarat Chandra E
# Dockerfile to run NodeJs 8 or ExpressJS app

WORKDIR /app

RUN git clone https://github.com/jatins/express-hello-world

FROM node:8

WORKDIR /app

COPY --from=repo /app/express-hello-world /app 

RUN npm install express

RUN npm install

EXPOSE 3000

#Give your server.js path location
CMD ["node", "server.js"]
