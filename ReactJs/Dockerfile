FROM alpine/git as repo
MAINTAINER sarat.e99@gmail.com Sarat Chandra E

WORKDIR /app

#Give your Repository
RUN git clone https://github.com/ahfarmer/emoji-search.git

FROM node:8

WORKDIR /app

COPY --from=repo /app/emoji-search /app 

RUN npm install express

RUN npm install

EXPOSE 4202

RUN ["npm", "run", "build"]

#Give your server.js path location - dist/ or build/ or so if u have node server file
#CMD ["node", "build/server.js"]
# OR
#Runs in Development Mode
CMD ["npm", "start"] 
