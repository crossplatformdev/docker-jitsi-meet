ARG JITSI_REPO=jitsi
FROM ${JITSI_REPO}/base-java

RUN \
	sed -re "s/deb\s*http/deb [arch=arm64] http/g" /etc/apt/sources.list && \
	LC_ALL=C DEBIAN_FRONTEND=noninteractive apt-get update && \
	LC_ALL=C DEBIAN_FRONTEND=noninteractive apt-get install -y jicofo && \
	apt-cleanup

COPY rootfs/ /

VOLUME /config

