<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `silverpeas`

-	[`silverpeas:6.2.3`](#silverpeas623)
-	[`silverpeas:latest`](#silverpeaslatest)

## `silverpeas:6.2.3`

```console
$ docker pull silverpeas@sha256:a67218a3732692d6d5d5afd362d11dbb5caa083c7b992d8c47257eccdc4aabf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `silverpeas:6.2.3` - linux; amd64

```console
$ docker pull silverpeas@sha256:b90fc1fc4683f8c16c535f5df858df70bcc820eff6112b09459ca16bd5c7eb80
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1900042125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:854e8992203d86ac09cbd1c54c6cd7aa8abf706025b0a2f9770956a14e86ce45`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 02:52:23 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Wed, 06 Apr 2022 02:52:23 GMT
ENV TERM=xterm
# Wed, 06 Apr 2022 02:58:09 GMT
RUN apt-get update   && apt-get install -y tzdata   && apt-get install -y     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Wed, 06 Apr 2022 02:58:22 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Wed, 06 Apr 2022 02:58:33 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Wed, 06 Apr 2022 02:58:33 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Wed, 06 Apr 2022 02:59:11 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Wed, 06 Apr 2022 02:59:11 GMT
ENV LANG=en_US.UTF-8
# Wed, 06 Apr 2022 02:59:11 GMT
ENV LANGUAGE=en_US.UTF-8
# Wed, 06 Apr 2022 02:59:12 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 06 Apr 2022 02:59:12 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 06 Apr 2022 02:59:13 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 06 Apr 2022 02:59:13 GMT
ENV JAVA_HOME=/docker-java-home
# Wed, 06 Apr 2022 02:59:13 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Wed, 06 Apr 2022 02:59:13 GMT
ENV JBOSS_HOME=/opt/wildfly
# Fri, 08 Apr 2022 20:46:46 GMT
ENV SILVERPEAS_VERSION=6.2.3
# Fri, 08 Apr 2022 20:46:46 GMT
ENV WILDFLY_VERSION=20.0.1
# Fri, 08 Apr 2022 20:46:46 GMT
LABEL name=Silverpeas 6.2.3 description=Image to install and to run Silverpeas 6.2.3 vendor=Silverpeas version=6.2.3 build=1
# Fri, 08 Apr 2022 20:47:32 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc http://download.jboss.org/wildfly/${WILDFLY_VERSION}.Final/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Fri, 08 Apr 2022 20:47:32 GMT
COPY file:4d0e637a3e1ce0b8143795fd5df1997a7ee18fba27382849ed23e9ecb8142009 in /root/.m2/ 
# Fri, 08 Apr 2022 20:47:32 GMT
COPY file:473bf75b335a39b6b4b39c64cd151bd8ed3d3e33da73b8124e537a5db1fad3d6 in /opt/silverpeas/bin/ 
# Fri, 08 Apr 2022 20:47:32 GMT
WORKDIR /opt/silverpeas/bin
# Fri, 08 Apr 2022 20:47:32 GMT
COPY file:b54156953ecf6c3259f3b3d2885a784847c0996fd145c0f7ccef25182725511f in /opt/ 
# Fri, 08 Apr 2022 20:47:32 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Fri, 08 Apr 2022 20:50:00 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle   && ./silverpeas construct   && rm ../log/build-*   && touch .install
# Fri, 08 Apr 2022 20:50:03 GMT
EXPOSE 8000 9990
# Fri, 08 Apr 2022 20:50:03 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Fri, 08 Apr 2022 20:50:04 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b05a90dc189177dca73a70569e0bdaec9c261e84d64c7abc39e2f91f2499b92`  
		Last Modified: Wed, 06 Apr 2022 03:17:44 GMT  
		Size: 912.9 MB (912949900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8354bab153b2388c09027b651c8d8fa0d16c33638a92800ee051db98815c50db`  
		Last Modified: Wed, 06 Apr 2022 03:16:10 GMT  
		Size: 4.0 MB (3994077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae2a83e218d0b0c8229bbed27b4c39102645feff1c60b21226e0a828b0774c8`  
		Last Modified: Wed, 06 Apr 2022 03:16:10 GMT  
		Size: 7.1 MB (7146661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065c4ddf20bd08031d52aa973e3294483effd66844bcd5f8b16d1e32d6bf70fb`  
		Last Modified: Wed, 06 Apr 2022 03:16:07 GMT  
		Size: 2.5 MB (2534352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa348fd95d1e5baf1877c1bde52449bb4d0461545d3afdd01140d8345f24c754`  
		Last Modified: Wed, 06 Apr 2022 03:16:06 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed975ca4856eb6275b35a1be17c437371bf39d3922be9d9d56e46ef22e2a9be2`  
		Last Modified: Wed, 06 Apr 2022 03:16:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e20f0c732b8c86ca666340a0480d080fad72e3e060c783b4cc7cf75a646173`  
		Last Modified: Fri, 08 Apr 2022 20:50:28 GMT  
		Size: 196.8 MB (196774066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8688d1af4d81476ade6690da8206b9662034ec822689ada5e6dbf045c6ad9288`  
		Last Modified: Fri, 08 Apr 2022 20:50:15 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bba2756e953106a296b11924be4fae39d7c153af00352605854c4f62f2a2599`  
		Last Modified: Fri, 08 Apr 2022 20:50:15 GMT  
		Size: 663.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4972999e3c99dbfe473c1946fa35453aaf6d1f74304687de6558dde3bf006ea6`  
		Last Modified: Fri, 08 Apr 2022 20:50:15 GMT  
		Size: 876.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:537e771935893a5089da2122e49063b3871819c96a68a41a7e4fc599c1d1912d`  
		Last Modified: Fri, 08 Apr 2022 20:50:15 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2324424039a0ad2551820620d9a05cc2a4676555a821d5791639f3cab13112`  
		Last Modified: Fri, 08 Apr 2022 20:50:49 GMT  
		Size: 748.1 MB (748074081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `silverpeas:latest`

```console
$ docker pull silverpeas@sha256:a67218a3732692d6d5d5afd362d11dbb5caa083c7b992d8c47257eccdc4aabf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `silverpeas:latest` - linux; amd64

```console
$ docker pull silverpeas@sha256:b90fc1fc4683f8c16c535f5df858df70bcc820eff6112b09459ca16bd5c7eb80
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1900042125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:854e8992203d86ac09cbd1c54c6cd7aa8abf706025b0a2f9770956a14e86ce45`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 02:52:23 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Wed, 06 Apr 2022 02:52:23 GMT
ENV TERM=xterm
# Wed, 06 Apr 2022 02:58:09 GMT
RUN apt-get update   && apt-get install -y tzdata   && apt-get install -y     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Wed, 06 Apr 2022 02:58:22 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Wed, 06 Apr 2022 02:58:33 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Wed, 06 Apr 2022 02:58:33 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Wed, 06 Apr 2022 02:59:11 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Wed, 06 Apr 2022 02:59:11 GMT
ENV LANG=en_US.UTF-8
# Wed, 06 Apr 2022 02:59:11 GMT
ENV LANGUAGE=en_US.UTF-8
# Wed, 06 Apr 2022 02:59:12 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 06 Apr 2022 02:59:12 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 06 Apr 2022 02:59:13 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 06 Apr 2022 02:59:13 GMT
ENV JAVA_HOME=/docker-java-home
# Wed, 06 Apr 2022 02:59:13 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Wed, 06 Apr 2022 02:59:13 GMT
ENV JBOSS_HOME=/opt/wildfly
# Fri, 08 Apr 2022 20:46:46 GMT
ENV SILVERPEAS_VERSION=6.2.3
# Fri, 08 Apr 2022 20:46:46 GMT
ENV WILDFLY_VERSION=20.0.1
# Fri, 08 Apr 2022 20:46:46 GMT
LABEL name=Silverpeas 6.2.3 description=Image to install and to run Silverpeas 6.2.3 vendor=Silverpeas version=6.2.3 build=1
# Fri, 08 Apr 2022 20:47:32 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc http://download.jboss.org/wildfly/${WILDFLY_VERSION}.Final/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Fri, 08 Apr 2022 20:47:32 GMT
COPY file:4d0e637a3e1ce0b8143795fd5df1997a7ee18fba27382849ed23e9ecb8142009 in /root/.m2/ 
# Fri, 08 Apr 2022 20:47:32 GMT
COPY file:473bf75b335a39b6b4b39c64cd151bd8ed3d3e33da73b8124e537a5db1fad3d6 in /opt/silverpeas/bin/ 
# Fri, 08 Apr 2022 20:47:32 GMT
WORKDIR /opt/silverpeas/bin
# Fri, 08 Apr 2022 20:47:32 GMT
COPY file:b54156953ecf6c3259f3b3d2885a784847c0996fd145c0f7ccef25182725511f in /opt/ 
# Fri, 08 Apr 2022 20:47:32 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Fri, 08 Apr 2022 20:50:00 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle   && ./silverpeas construct   && rm ../log/build-*   && touch .install
# Fri, 08 Apr 2022 20:50:03 GMT
EXPOSE 8000 9990
# Fri, 08 Apr 2022 20:50:03 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Fri, 08 Apr 2022 20:50:04 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b05a90dc189177dca73a70569e0bdaec9c261e84d64c7abc39e2f91f2499b92`  
		Last Modified: Wed, 06 Apr 2022 03:17:44 GMT  
		Size: 912.9 MB (912949900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8354bab153b2388c09027b651c8d8fa0d16c33638a92800ee051db98815c50db`  
		Last Modified: Wed, 06 Apr 2022 03:16:10 GMT  
		Size: 4.0 MB (3994077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae2a83e218d0b0c8229bbed27b4c39102645feff1c60b21226e0a828b0774c8`  
		Last Modified: Wed, 06 Apr 2022 03:16:10 GMT  
		Size: 7.1 MB (7146661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065c4ddf20bd08031d52aa973e3294483effd66844bcd5f8b16d1e32d6bf70fb`  
		Last Modified: Wed, 06 Apr 2022 03:16:07 GMT  
		Size: 2.5 MB (2534352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa348fd95d1e5baf1877c1bde52449bb4d0461545d3afdd01140d8345f24c754`  
		Last Modified: Wed, 06 Apr 2022 03:16:06 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed975ca4856eb6275b35a1be17c437371bf39d3922be9d9d56e46ef22e2a9be2`  
		Last Modified: Wed, 06 Apr 2022 03:16:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e20f0c732b8c86ca666340a0480d080fad72e3e060c783b4cc7cf75a646173`  
		Last Modified: Fri, 08 Apr 2022 20:50:28 GMT  
		Size: 196.8 MB (196774066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8688d1af4d81476ade6690da8206b9662034ec822689ada5e6dbf045c6ad9288`  
		Last Modified: Fri, 08 Apr 2022 20:50:15 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bba2756e953106a296b11924be4fae39d7c153af00352605854c4f62f2a2599`  
		Last Modified: Fri, 08 Apr 2022 20:50:15 GMT  
		Size: 663.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4972999e3c99dbfe473c1946fa35453aaf6d1f74304687de6558dde3bf006ea6`  
		Last Modified: Fri, 08 Apr 2022 20:50:15 GMT  
		Size: 876.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:537e771935893a5089da2122e49063b3871819c96a68a41a7e4fc599c1d1912d`  
		Last Modified: Fri, 08 Apr 2022 20:50:15 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2324424039a0ad2551820620d9a05cc2a4676555a821d5791639f3cab13112`  
		Last Modified: Fri, 08 Apr 2022 20:50:49 GMT  
		Size: 748.1 MB (748074081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
