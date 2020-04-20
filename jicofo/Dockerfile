ARG JITSI_REPO=jitsi
FROM mansab/jitsi-base-java

RUN \
	apt-dpkg-wrap apt-get update && \
	apt-dpkg-wrap apt-get install -y jicofo && \
	apt-cleanup

COPY rootfs/ /

RUN /fix-permissions.sh

VOLUME /config

USER 1001
