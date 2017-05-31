FROM openjdk:8-jre

MAINTAINER Bas Passon <docker@bliep.net>

RUN apt-get update && apt-get install -y wget

ENV DOCKERIZE_VERSION v0.4.0
RUN wget https://github.com/jwilder/dockerize/releases/download/$DOCKERIZE_VERSION/dockerize-linux-amd64-$DOCKERIZE_VERSION.tar.gz \
    && tar -C /usr/local/bin -xzvf dockerize-linux-amd64-$DOCKERIZE_VERSION.tar.gz \
    && rm dockerize-linux-amd64-$DOCKERIZE_VERSION.tar.gz

VOLUME [ "/app" ]
WORKDIR /app

EXPOSE 8080

COPY ./docker-entry.sh /
ENTRYPOINT [ "/docker-entry.sh" ]

CMD ["-?"]
