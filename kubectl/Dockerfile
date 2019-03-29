FROM alpine:latest

RUN apk --no-cache add ca-certificates curl \
  && KUBERNETES_VERSION=$(curl -sSL https://storage.googleapis.com/kubernetes-release/release/stable.txt) \
  && curl -L https://storage.googleapis.com/kubernetes-release/release/${KUBERNETES_VERSION}/bin/linux/amd64/kubectl -o /usr/local/bin/kubectl \
  && curl -L https://amazon-eks.s3-us-west-2.amazonaws.com/1.12.7/2019-03-27/bin/linux/amd64/aws-iam-authenticator -o /usr/local/bin/aws-iam-authenticator \
  && chmod +x /usr/local/bin/kubectl /usr/local/bin/aws-iam-authenticator \
  && apk del --purge curl

ENTRYPOINT ["kubectl"]
