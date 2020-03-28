FROM golang:1.14.0-alpine

ARG SERVICE_NAME

WORKDIR /go/src/github.com/Pashio84/${SERVICE_NAME}

COPY ${SERVICE_NAME} /go/src/github.com/Pashio84/${SERVICE_NAME}

RUN pwd && apk update && \
  apk add --no-cache git tzdata && \
  cp /usr/share/zoneinfo/Asia/Tokyo /etc/localtime && \
  go build && \
  go get github.com/oxequa/realize