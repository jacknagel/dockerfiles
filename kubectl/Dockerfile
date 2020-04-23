FROM amazon/aws-cli:latest
ARG KUBERNETES_VERSION
RUN wget -q -O /usr/local/bin/kubectl https://dl.k8s.io/${KUBERNETES_VERSION}/bin/linux/amd64/kubectl \
  && chmod +x /usr/local/bin/kubectl
ENTRYPOINT ["kubectl"]
