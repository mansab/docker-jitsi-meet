ARG JITSI_REPO=jitsi
FROM mansab/jitsi-base

ENV JAVA_SYS_PROPS "-Djava.util.prefs.userRoot=/root"

RUN	\
	mkdir -p /usr/share/man/man1 && \
	apt-dpkg-wrap apt-get update && \
	apt-dpkg-wrap apt-get install -y openjdk-8-jre-headless && \
	apt-cleanup
