## `silverpeas:latest`

```console
$ docker pull silverpeas@sha256:3640b1c74966bdbd770a27582ef10aeb59cd56c92395506bcdfc8b4af2323588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `silverpeas:latest` - linux; amd64

```console
$ docker pull silverpeas@sha256:3ef6a76941d756cd71331b0b1efeef31f95a5a7b682e3e58186e5df1742a3c55
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1779863391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5be4d15a3ededf2b50d08da617400c41683d010aa25b80953ddaabb58156cd0d`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Mon, 05 Jun 2023 17:08:57 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:08:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:08:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:08:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 05 Jun 2023 17:08:58 GMT
ADD file:655d373cb551d0dd5d7867f88a4f98908dc3f16190986f693e88c423e6f21b8d in / 
# Mon, 05 Jun 2023 17:08:58 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 04:14:23 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Fri, 16 Jun 2023 04:14:23 GMT
ENV TERM=xterm
# Fri, 16 Jun 2023 04:22:01 GMT
RUN apt-get update   && apt-get install -y tzdata   && apt-get install -y     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Fri, 16 Jun 2023 04:22:08 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Fri, 16 Jun 2023 04:22:11 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Fri, 16 Jun 2023 04:22:12 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Fri, 16 Jun 2023 04:22:50 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Fri, 16 Jun 2023 04:22:50 GMT
ENV LANG=en_US.UTF-8
# Fri, 16 Jun 2023 04:22:50 GMT
ENV LANGUAGE=en_US.UTF-8
# Fri, 16 Jun 2023 04:22:51 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 04:22:51 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 16 Jun 2023 04:22:52 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 16 Jun 2023 04:22:52 GMT
ENV JAVA_HOME=/docker-java-home
# Fri, 16 Jun 2023 04:22:52 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Fri, 16 Jun 2023 04:22:52 GMT
ENV JBOSS_HOME=/opt/wildfly
# Fri, 16 Jun 2023 04:22:52 GMT
ENV SILVERPEAS_VERSION=6.3
# Fri, 16 Jun 2023 04:22:52 GMT
ENV WILDFLY_VERSION=26.1.1
# Fri, 16 Jun 2023 04:22:52 GMT
LABEL name=Silverpeas 6.3 description=Image to install and to run Silverpeas 6.3 vendor=Silverpeas version=6.3 build=1
# Fri, 16 Jun 2023 04:23:34 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Fri, 16 Jun 2023 04:23:35 GMT
COPY file:4d0e637a3e1ce0b8143795fd5df1997a7ee18fba27382849ed23e9ecb8142009 in /root/.m2/ 
# Fri, 16 Jun 2023 04:23:35 GMT
COPY file:473bf75b335a39b6b4b39c64cd151bd8ed3d3e33da73b8124e537a5db1fad3d6 in /opt/silverpeas/bin/ 
# Fri, 16 Jun 2023 04:23:35 GMT
WORKDIR /opt/silverpeas/bin
# Fri, 16 Jun 2023 04:23:35 GMT
COPY file:b54156953ecf6c3259f3b3d2885a784847c0996fd145c0f7ccef25182725511f in /opt/ 
# Fri, 16 Jun 2023 04:23:35 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Fri, 16 Jun 2023 04:25:20 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle   && ./silverpeas construct   && rm ../log/build-*   && touch .install
# Fri, 16 Jun 2023 04:25:23 GMT
EXPOSE 8000 9990
# Fri, 16 Jun 2023 04:25:23 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Fri, 16 Jun 2023 04:25:23 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:f0412dfb1aaea4892c13dab6f771bcd79641a4bdcb521ce881f5dcfc0df9a7a5`  
		Last Modified: Tue, 06 Jun 2023 09:20:27 GMT  
		Size: 28.6 MB (28580519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b0a1380d6a7d7d8b874d96689b1af575d0d6a3fdeaa305add95009b98d210d`  
		Last Modified: Fri, 16 Jun 2023 04:29:26 GMT  
		Size: 762.5 MB (762545872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25d681bb85b49486c74804bdc158add33040409da2c1039db7ad42b840fe2d59`  
		Last Modified: Fri, 16 Jun 2023 04:28:06 GMT  
		Size: 4.0 MB (3994072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b95609b17c560dda436c5f6f57713cd7bd36d8506863a0ce9da7c2290bf2d38`  
		Last Modified: Fri, 16 Jun 2023 04:28:06 GMT  
		Size: 7.1 MB (7146649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b40311651f4d671650c532b5efd94a2bb1477cd6eb72bece6186cff8e1f6b29`  
		Last Modified: Fri, 16 Jun 2023 04:28:04 GMT  
		Size: 2.5 MB (2534358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d161275f8db97c30a8a3631e588f709fdbbf7b4ef232a0e28846b16ff07e1b`  
		Last Modified: Fri, 16 Jun 2023 04:28:03 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d2e8f3f2d66d55a33e485d9e8c6df41bdb60331d90351f808a81f8aee9ed540`  
		Last Modified: Fri, 16 Jun 2023 04:28:03 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03671d3f4604aba7614b95a57e8da98ea3207b71c315af4ab46f40e5d46bcd03`  
		Last Modified: Fri, 16 Jun 2023 04:28:14 GMT  
		Size: 217.8 MB (217842804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e8c16c649f2b29bb9a6f404fe6de6b5d966d51fc171bf9930cd6451eb804647`  
		Last Modified: Fri, 16 Jun 2023 04:28:01 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a20616e4517414fa8fba5f07e01812ad1e3349bc38570327c3853eefa8fb476`  
		Last Modified: Fri, 16 Jun 2023 04:28:01 GMT  
		Size: 663.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b983feac237071e6ef7cf4f408ead9501d3a0c6fa6b16bb3dfea35217b1bb5`  
		Last Modified: Fri, 16 Jun 2023 04:28:01 GMT  
		Size: 876.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fccdc0817dfb8c0fa1a1e080a97cd708a1daea487076c9c59da154a1df5c907`  
		Last Modified: Fri, 16 Jun 2023 04:28:01 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e9b1210dc743cdb4a8f5b83513f348cd2b0012969fad395f05408ce931221c`  
		Last Modified: Fri, 16 Jun 2023 04:28:36 GMT  
		Size: 757.2 MB (757216414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
