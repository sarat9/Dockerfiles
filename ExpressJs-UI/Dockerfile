FROM alpine/git as repo
MAINTAINER sarat.e99@gmail.com Sarat Chandra E
# Dockerfile to host static UI in expressjs server

WORKDIR /app

RUN git clone https://github.com/didinj/angular-4-sample-app.git

FROM node:8

WORKDIR /app

COPY --from=repo /app/angular-4-sample-app /app 

RUN npm install express

RUN npm install

EXPOSE 4202

RUN ["npm", "run", "build"]

#Give your server.js path location
CMD ["node", "dist/server.js"]
