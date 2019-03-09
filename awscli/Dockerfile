FROM alpine:latest

LABEL maintainer "Jack Nagel <jack@jacknagel.dev>"

RUN apk --no-cache add ca-certificates groff less python py2-pip \
  && pip install awscli

ENTRYPOINT ["aws"]
