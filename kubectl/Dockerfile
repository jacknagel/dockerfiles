FROM alpine:latest AS build
ARG KUBERNETES_VERSION
RUN wget -q -O /kubectl https://dl.k8s.io/v${KUBERNETES_VERSION}/bin/linux/amd64/kubectl && chmod +x /kubectl

FROM amazon/aws-cli:latest
COPY --from=build /kubectl /usr/local/bin/
ENTRYPOINT ["kubectl"]
