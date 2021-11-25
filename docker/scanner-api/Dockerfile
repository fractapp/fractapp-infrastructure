FROM node

WORKDIR /app

COPY ./scanner /app
COPY .env-scanner /app/.env

RUN yarn install && yarn build

ENTRYPOINT ["yarn", "run", "api"]
