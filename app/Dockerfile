FROM node:lts-alpine

RUN npm install -g http-server 

COPY ./dist /dist

RUN apk add curl jq

ENV NEW_RELIC_NO_CONFIG_FILE=true

ENV NEW_RELIC_BROWSER_MONITOR_ENABLE=true

EXPOSE 8080
ENTRYPOINT [ "http-server", "/dist"]
