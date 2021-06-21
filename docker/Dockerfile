FROM node:16.3.0-alpine3.11


WORKDIR /api

COPY api/package*.json .
COPY api/yarn*.lock .

RUN yarn

CMD ["yarn", "start"]