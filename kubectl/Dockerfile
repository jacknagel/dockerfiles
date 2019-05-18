FROM alpine:latest

RUN apk --no-cache add ca-certificates curl \
  && KUBERNETES_VERSION=$(curl -sSL https://storage.googleapis.com/kubernetes-release/release/stable.txt) \
  && curl -L https://storage.googleapis.com/kubernetes-release/release/${KUBERNETES_VERSION}/bin/linux/amd64/kubectl -o /usr/local/bin/kubectl \
  && chmod +x /usr/local/bin/kubectl \
  && apk del --purge curl

ENTRYPOINT ["kubectl"]
