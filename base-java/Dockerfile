ARG JITSI_REPO=jitsi
FROM ${JITSI_REPO}/base

RUN	\
	mkdir -p /usr/share/man/man1 && \
	LC_ALL=C DEBIAN_FRONTEND=noninteractive apt-get update && \
	LC_ALL=C DEBIAN_FRONTEND=noninteractive apt-get install -t stretch-backports -y openjdk-8-jre-headless && \
	apt-cleanup

