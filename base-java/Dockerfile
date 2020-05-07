ARG JITSI_REPO=jitsi
FROM ${JITSI_REPO}/base

RUN	\
	mkdir -p /usr/share/man/man1 && \
	sed -re "s/deb\s*http/deb [arch=arm64] http/g" /etc/apt/sources.list && \
	LC_ALL=C DEBIAN_FRONTEND=noninteractive apt-get update && \
	LC_ALL=C DEBIAN_FRONTEND=noninteractive apt-get install -t stretch-backports -y openjdk-11-jre && \
	apt-cleanup

