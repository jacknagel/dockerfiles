FROM alpine:latest
RUN KUBERNETES_VERSION=$(wget -q -O - https://storage.googleapis.com/kubernetes-release/release/stable.txt) \
  && wget -q -O /usr/local/bin/kubectl https://storage.googleapis.com/kubernetes-release/release/${KUBERNETES_VERSION}/bin/linux/amd64/kubectl \
  && chmod +x /usr/local/bin/kubectl
ENTRYPOINT ["kubectl"]
