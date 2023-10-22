FROM node:21-alpine

ENV VERSION=0.1.1-3
ENV PROJECT=fake-metrics-generator
ENV FILENAME=$PROJECT-$VERSION.zip

WORKDIR /app

ADD https://github.com/grafana/$PROJECT/releases/download/v$VERSION/$FILENAME .

RUN unzip "$FILENAME" && rm "$FILENAME"

EXPOSE 5000

ENTRYPOINT ["node"]
CMD ["/app/dist/main.node.js"]
