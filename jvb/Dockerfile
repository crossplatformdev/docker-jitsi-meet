ARG JITSI_REPO=jitsi
FROM ${JITSI_REPO}/base-java

RUN \
	LC_ALL=C DEBIAN_FRONTEND=noninteractive apt-get update && \
	LC_ALL=C DEBIAN_FRONTEND=noninteractive apt-get install -y jitsi-videobridge2 jq curl && \
	apt-cleanup

COPY rootfs/ /

#Place libjniwrapper in project's root directory
COPY ./jnilib-1.0-SNAPSHOT.jar  /usr/share/jitsi-videobridge/lib/jnilib-1.0-SNAPSHOT.jar
VOOLUME /config
