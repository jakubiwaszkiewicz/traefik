FROM node:20-alpine3.16

RUN mkdir -p /home/node/app/node_modules && chown -R node:node /home/node/app

WORKDIR /home/node/app

COPY package*.json ./

USER node

COPY --chown=node:node . .

RUN npm install

EXPOSE 5001

CMD [ "node", "app.js" ]