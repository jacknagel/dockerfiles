FROM python:3-alpine
RUN apk --no-cache add ca-certificates groff less && pip install --no-cache-dir awscli
ENTRYPOINT ["aws"]
