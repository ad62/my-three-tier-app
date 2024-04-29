FROM node:14

ENV INSTANA_AUTO_PROFILE true

EXPOSE 8080

WORKDIR /opt/server

COPY package.json /opt/server/
COPY server.js /opt/server/

RUN npm install newrelic --save
RUN npm install

COPY server.js /opt/server/

CMD ["node", "server.js"]

