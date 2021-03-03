FROM alpine/git as repo
MAINTAINER sarat.e99@gmail.com Sarat Chandra E
#Docker file to run Angular app in Dev Mode

WORKDIR /app

RUN git clone https://github.com/didinj/angular-4-sample-app.git

FROM node:8

WORKDIR /app

COPY --from=repo /app/angular-4-sample-app /app 

RUN npm install -g @angular/cli

RUN npm install

EXPOSE 4202

#Give your server.js path location - dist/ or build/ or so if u have node server file
#CMD ["node", "build/server.js"]
# OR
#Running in Dev Mode
#CMD ["ng", "serve", "--host", "0.0.0.0", "--port", "4202"]
CMD ["npm", "start"]
