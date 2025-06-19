FROM arm64v8/node:16-alpine3.16
#created directory
WORKDIR /home/node/app
RUN mkdir -p /home/node/app/node_modules && chown -R node:node /home/node/app
COPY package*.json package-lock.json .env ./
#use user node user
USER node
COPY --chown=node:node . .
RUN npm install --ignore-scripts --production
EXPOSE 15002
CMD [ "npm", "start" ]
