FROM node

ENV network="Polkadot"
ENV defaultHeight="7647081"

WORKDIR /app

COPY ./scanner /app
COPY .env-scanner /app/.env

RUN yarn install && yarn build

CMD ["sh", "-c", "node ./bin/src/cmd/notifier.js ${network} ${defaultHeight}"]
