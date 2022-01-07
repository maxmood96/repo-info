## `silverpeas:latest`

```console
$ docker pull silverpeas@sha256:fe1b57f43953648ea95a4824442e03f7557e394523e4c339dc61260f174ac663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `silverpeas:latest` - linux; amd64

```console
$ docker pull silverpeas@sha256:3b148babf8ac4cec90ae8643b9aaa58d6b3024ccc805dfba755c741ee92e72cc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1896916998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af77cb15fd6025fcce4295d50fd7b24f1d020c6ee51e9e22e75461294fea2bb1`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:29 GMT
ADD file:122ad323412c2e70b3138d8eb62648c4692989de91be1ffb6b4bf086c8311b62 in / 
# Fri, 07 Jan 2022 02:25:30 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 05:38:02 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Fri, 07 Jan 2022 05:38:02 GMT
ENV TERM=xterm
# Fri, 07 Jan 2022 05:45:01 GMT
RUN apt-get update   && apt-get install -y tzdata   && apt-get install -y     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Fri, 07 Jan 2022 05:45:08 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Fri, 07 Jan 2022 05:45:11 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Fri, 07 Jan 2022 05:45:12 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Fri, 07 Jan 2022 05:45:50 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Fri, 07 Jan 2022 05:45:50 GMT
ENV LANG=en_US.UTF-8
# Fri, 07 Jan 2022 05:45:50 GMT
ENV LANGUAGE=en_US.UTF-8
# Fri, 07 Jan 2022 05:45:51 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 07 Jan 2022 05:45:51 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 07 Jan 2022 05:45:52 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 07 Jan 2022 05:45:52 GMT
ENV JAVA_HOME=/docker-java-home
# Fri, 07 Jan 2022 05:45:53 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Fri, 07 Jan 2022 05:45:53 GMT
ENV JBOSS_HOME=/opt/wildfly
# Fri, 07 Jan 2022 05:45:53 GMT
ENV SILVERPEAS_VERSION=6.2.2
# Fri, 07 Jan 2022 05:45:53 GMT
ENV WILDFLY_VERSION=20.0.1
# Fri, 07 Jan 2022 05:45:53 GMT
LABEL name=Silverpeas 6.2.2 description=Image to install and to run Silverpeas 6.2.2 vendor=Silverpeas version=6.2.2 build=1
# Fri, 07 Jan 2022 05:46:09 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc http://download.jboss.org/wildfly/${WILDFLY_VERSION}.Final/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Fri, 07 Jan 2022 05:46:10 GMT
COPY file:4d0e637a3e1ce0b8143795fd5df1997a7ee18fba27382849ed23e9ecb8142009 in /root/.m2/ 
# Fri, 07 Jan 2022 05:46:10 GMT
COPY file:473bf75b335a39b6b4b39c64cd151bd8ed3d3e33da73b8124e537a5db1fad3d6 in /opt/silverpeas/bin/ 
# Fri, 07 Jan 2022 05:46:10 GMT
WORKDIR /opt/silverpeas/bin
# Fri, 07 Jan 2022 05:46:11 GMT
COPY file:b54156953ecf6c3259f3b3d2885a784847c0996fd145c0f7ccef25182725511f in /opt/ 
# Fri, 07 Jan 2022 05:46:11 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Fri, 07 Jan 2022 05:48:01 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle   && ./silverpeas construct   && rm ../log/build-*   && touch .install
# Fri, 07 Jan 2022 05:48:04 GMT
EXPOSE 8000 9990
# Fri, 07 Jan 2022 05:48:04 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Fri, 07 Jan 2022 05:48:05 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:ea362f368469f909a95f9a6e54ebe0121ce0a8e3c30583dd9c5fb35b14544dec`  
		Last Modified: Thu, 06 Jan 2022 15:07:12 GMT  
		Size: 28.6 MB (28566425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67c40d122f8f6e0112bb277f221d325bc3d2f835931a72d342734bea9e45c401`  
		Last Modified: Fri, 07 Jan 2022 06:00:05 GMT  
		Size: 909.9 MB (909876872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:004e34c38a7c5a63ef85a0355e2dddca97591863d363b570ef25cb1e2c6e944d`  
		Last Modified: Fri, 07 Jan 2022 05:58:32 GMT  
		Size: 4.0 MB (3994068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d01a19868298feafea1fa658c5a42b3b3020819f998fcacff034a852fc5296`  
		Last Modified: Fri, 07 Jan 2022 05:58:32 GMT  
		Size: 7.1 MB (7146648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592c400ad9b8a1e7e0cfd95c6468c48616e76bffd545ee3fae5362799eef8be2`  
		Last Modified: Fri, 07 Jan 2022 05:58:29 GMT  
		Size: 2.5 MB (2534366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb6e910563c17ef74e04b44dd915a06b2e47762aa429670b1a2135596aa7d50`  
		Last Modified: Fri, 07 Jan 2022 05:58:28 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86da6030d71c2ce2030ce2e7230b6e25292d479dcd722074caf806343315c4cf`  
		Last Modified: Fri, 07 Jan 2022 05:58:28 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e148401445c2a86a86ed4c62aaea25c575d4d0c93d0e46c688aaad73bc436fdf`  
		Last Modified: Fri, 07 Jan 2022 05:58:41 GMT  
		Size: 196.8 MB (196774067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5bfa761dcb05231237d90ffe88b48708cf5c76c791fad0ff9eb710e7a7a9737`  
		Last Modified: Fri, 07 Jan 2022 05:58:26 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b60dec9603e5d4ce3e001721327448e11f71e44eb19a9239866b21fc34280f`  
		Last Modified: Fri, 07 Jan 2022 05:58:26 GMT  
		Size: 666.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb18f89eba3cd5ac7848d223d57f9e424e7c919ecf4dc5fa211e6ecead6fd7d3`  
		Last Modified: Fri, 07 Jan 2022 05:58:26 GMT  
		Size: 877.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0a855f632b5184ce221f206a1340c2a2d0352242eb3eaaaea7e57983c9d527`  
		Last Modified: Fri, 07 Jan 2022 05:58:26 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35efde809c2f5a4d7323abcda584af8196e21d2a54555e068fd42da088f4f5cb`  
		Last Modified: Fri, 07 Jan 2022 05:59:05 GMT  
		Size: 748.0 MB (748021846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
