FROM node:10
RUN mkdir -p /usr/src/app && chown -R node:node /usr/src/app
COPY index.js /usr/src/app
USER node
RUN npm install
COPY . /usr/src/app
EXPOSE 8080
CMD [ "node", "/usr/src/app/index" ]
