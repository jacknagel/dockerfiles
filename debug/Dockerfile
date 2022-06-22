FROM debian:bullseye-slim

RUN DEBIAN_FRONTEND=noninteractive apt-get update \
       && apt-get install -y apt-transport-https ca-certificates curl \
       && curl -fsSLo /usr/share/keyrings/kubernetes-archive-keyring.gpg https://packages.cloud.google.com/apt/doc/apt-key.gpg \
       && echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/kubernetes-archive-keyring.gpg] https://apt.kubernetes.io/ kubernetes-xenial main" | tee /etc/apt/sources.list.d/kubernetes.list \
       && echo "wireshark-common wireshark-common/install-setuid boolean true" | debconf-set-selections \
       && apt-get update -y \
       && apt-get install -y --no-install-recommends --no-install-suggests \
	bash \
	bash-completion \
	blktrace \
	dnsutils \
	ethtool \
	file \
	findutils \
	git \
	iotop \
	iperf3 \
	iproute2 \
	iptables \
	iputils-ping \
	jq \
	kubectl \
	less \
	linux-cpupower \
	linux-perf \
	lsof \
	moreutils \
	mtr \
	net-tools \
	netcat \
	netsniff-ng \
	nftables \
	ngrep \
	nmap \
	procps \
	psmisc \
	strace \
	sysstat \
	tcpdump \
	tcptrace \
	tcptraceroute \
	tshark \
	vim-tiny \
	&& apt-get purge -y --auto-remove \
	&& rm -rf /var/lib/apt/lists/*

CMD ["bash"]
