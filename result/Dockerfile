FROM node:12-alpine
LABEL author="Lucas Hauszler"

RUN mkdir -p /app

COPY . /app/
WORKDIR /app

RUN npm install

EXPOSE 80

CMD [ "node", "server.js" ]
