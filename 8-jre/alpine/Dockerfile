FROM openjdk:8-jre-alpine

MAINTAINER Bas Passon <docker@bliep.net>

RUN apk add --no-cache openssl

ENV DOCKERIZE_OPTS ""
ENV DOCKERIZE_VERSION v0.4.0
RUN wget https://github.com/jwilder/dockerize/releases/download/$DOCKERIZE_VERSION/dockerize-alpine-linux-amd64-$DOCKERIZE_VERSION.tar.gz \
    && tar -C /usr/local/bin -xzvf dockerize-alpine-linux-amd64-$DOCKERIZE_VERSION.tar.gz \
    && rm dockerize-alpine-linux-amd64-$DOCKERIZE_VERSION.tar.gz

VOLUME [ "/app" ]
WORKDIR /app

EXPOSE 8080

COPY ../../docker-entry.sh /
ENTRYPOINT [ "/docker-entry.sh" ]

CMD ["-?"]
