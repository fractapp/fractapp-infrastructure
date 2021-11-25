FROM golang:1.16.2-buster

WORKDIR /app

RUN mkdir /app/build
COPY ./fractapp-server /app/build
COPY ./fractapp-server /app/build
COPY config-server.json /app/config-docker.json
COPY ./fractapp-server/firebase.json /app/firebase.json

RUN cd /app/build/cmd/scheduler && go build -o /app/scheduler && cd /app/build
RUN rm -rf /app/build

ENTRYPOINT ["./scheduler", "--config=config-docker.json"]
