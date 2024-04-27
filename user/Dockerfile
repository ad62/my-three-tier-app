FROM node:14

# Set the New Relic license key as an environment variable
ENV NEW_RELIC_LICENSE_KEY=d27bd10be363ab7b7d243f2e8415d9b5FFFFNRAL
ENV NEW_RELIC_APP_NAME=user
ENV INSTANA_AUTO_PROFILE true

EXPOSE 8080

WORKDIR /opt/server

COPY package.json /opt/server/

RUN npm install newrelic --save \
    && npm install

COPY server.js /opt/server/

# Start your application with the New Relic agent
CMD ["node", "node_modules/newrelic/bin/newrelic.js", "server.js"]
