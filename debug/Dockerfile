FROM debian:bullseye-slim

RUN apt-get update -y \
       && apt-get install -y apt-transport-https ca-certificates curl \
       && curl -fsSLo /usr/share/keyrings/kubernetes-archive-keyring.gpg https://packages.cloud.google.com/apt/doc/apt-key.gpg \
       && echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/kubernetes-archive-keyring.gpg] https://apt.kubernetes.io/ kubernetes-xenial main" | tee /etc/apt/sources.list.d/kubernetes.list \
       && apt-get update -y \
       && apt-get install -y --no-install-recommends --no-install-suggests \
	bash \
	bash-completion \
	dnsutils \
	file \
	findutils \
	git \
	iputils-ping \
	kubectl \
	less \
	moreutils \
	net-tools \
	netcat \
	netsniff-ng \
	procps \
	psmisc \
	strace \
	sysstat \
	tcpdump \
	tcptrace \
	tcptraceroute \
	vim-tiny \
	&& apt-get purge -y --auto-remove \
	&& rm -rf /var/lib/apt/lists/*

CMD ["/bin/bash"]
