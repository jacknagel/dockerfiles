FROM alpine:latest
ARG SKEEMA_VERSION
RUN wget -q -O skeema.tar.gz https://github.com/skeema/skeema/releases/download/v${SKEEMA_VERSION}/skeema_${SKEEMA_VERSION}_linux_amd64.tar.gz \
	&& tar xvf skeema.tar.gz \
	&& rm skeema.tar.gz \
	&& chmod +x skeema \
	&& mv skeema /usr/local/bin
ENTRYPOINT ["skeema"]
