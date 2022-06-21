FROM debian:bullseye-slim

RUN apt-get update -y \
	&& apt-get install -y --no-install-recommends --no-install-suggests bash curl dnsutils git \
	&& apt-get purge -y --auto-remove \
	&& rm -rf /var/lib/apt/lists/*

CMD ["/bin/bash"]
