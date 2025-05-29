FROM debian:bookworm-slim

ARG KUBERNETES_VERSION

RUN DEBIAN_FRONTEND=noninteractive apt-get update \
       && apt-get install -y apt-transport-https ca-certificates curl gpg \
       && curl -fsSL https://pkgs.k8s.io/core:/stable:/v$KUBERNETES_VERSION/deb/Release.key | gpg --dearmor -o /etc/apt/keyrings/kubernetes-apt-keyring.gpg \
       && echo "deb [signed-by=/etc/apt/keyrings/kubernetes-apt-keyring.gpg] https://pkgs.k8s.io/core:/stable:/v$KUBERNETES_VERSION/deb/ /" | tee /etc/apt/sources.list.d/kubernetes.list \
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
	netcat-openbsd \
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
