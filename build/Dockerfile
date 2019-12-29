FROM golang:alpine3.10 AS build

RUN apk add bash build-base --no-cache

ENV GO111MODULE=on

COPY . /workspace

RUN make -C /workspace code/compile


FROM alpine:3.10

RUN apk upgrade --update --no-cache

COPY --from=build /workspace/build/_output/bin/grafana-operator /usr/local/bin/grafana-operator

USER nobody
