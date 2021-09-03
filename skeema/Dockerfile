FROM alpine:latest AS build
ARG SKEEMA_VERSION
RUN wget -q -O skeema.tar.gz https://github.com/skeema/skeema/releases/download/v${SKEEMA_VERSION}/skeema_${SKEEMA_VERSION}_linux_amd64.tar.gz \
	&& tar xvf skeema.tar.gz \
	&& rm skeema.tar.gz \
	&& chmod +x skeema

FROM busybox:latest
COPY --from=build /skeema /usr/local/bin/skeema
ENTRYPOINT ["skeema"]
