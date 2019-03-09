FROM python:3-alpine

LABEL maintainer "Jack Nagel <jack@jacknagel.dev>"

RUN apk --no-cache add ca-certificates groff less && pip install --no-cache-dir awscli

ENTRYPOINT ["aws"]
