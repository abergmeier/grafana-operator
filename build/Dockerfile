FROM alpine:3.10

RUN apk upgrade --update --no-cache

USER nobody

ADD build/_output/bin/grafana-operator /usr/local/bin/grafana-operator
