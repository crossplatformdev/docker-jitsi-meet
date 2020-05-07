ARG JITSI_REPO=jitsi
FROM ${JITSI_REPO}/base-java

ENV GOOGLE_APPLICATION_CREDENTIALS /config/key.json

RUN \
	LC_ALL=C DEBIAN_FRONTEND=noninteractive apt-get update && \
	LC_ALL=C DEBIAN_FRONTEND=noninteractive apt-get install -y jigasi jq && \
	apt-cleanup

COPY rootfs/ /

VOLUME ["/config", "/tmp/transcripts"]
