ARG JITSI_REPO=jitsi
FROM ${JITSI_REPO}/base-java

RUN \
	LC_ALL=C DEBIAN_FRONTEND=noninteractive apt-get update && \
	LC_ALL=C DEBIAN_FRONTEND=noninteractive apt-get install -y jicofo && \
	apt-cleanup

COPY rootfs/ /

VOLUME /config

