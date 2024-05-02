<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `silverpeas`

-	[`silverpeas:6.3.4`](#silverpeas634)
-	[`silverpeas:latest`](#silverpeaslatest)

## `silverpeas:6.3.4`

```console
$ docker pull silverpeas@sha256:a9a4a8f2cd241c5cfcd1ec44c5d32ba636b154bbc490d2e8117381bedf31b483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `silverpeas:6.3.4` - linux; amd64

```console
$ docker pull silverpeas@sha256:d2d59793bd0da5879cb918edc6946fb6b9eb23e050946aabcfa7618e0bd36a29
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1777168108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d35eb92c9d9711dd0bcc6cb6818450f52278a2fb9924a48228e680313ee3ba`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Sat, 27 Apr 2024 14:03:39 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:03:41 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Sat, 27 Apr 2024 14:03:41 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 03:29:10 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Thu, 02 May 2024 03:29:10 GMT
ENV TERM=xterm
# Thu, 02 May 2024 03:35:21 GMT
RUN apt-get update   && apt-get install -y tzdata   && apt-get install -y     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Thu, 02 May 2024 03:35:28 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Thu, 02 May 2024 03:35:31 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Thu, 02 May 2024 03:35:31 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Thu, 02 May 2024 03:36:11 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Thu, 02 May 2024 03:36:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 02 May 2024 03:36:11 GMT
ENV LANGUAGE=en_US.UTF-8
# Thu, 02 May 2024 03:36:11 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 02 May 2024 03:36:12 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 02 May 2024 03:36:12 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Thu, 02 May 2024 03:36:12 GMT
ENV JAVA_HOME=/docker-java-home
# Thu, 02 May 2024 03:36:12 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Thu, 02 May 2024 03:36:12 GMT
ENV JBOSS_HOME=/opt/wildfly
# Thu, 02 May 2024 03:36:13 GMT
ENV SILVERPEAS_VERSION=6.3.4
# Thu, 02 May 2024 03:36:13 GMT
ENV WILDFLY_VERSION=26.1.1
# Thu, 02 May 2024 03:36:13 GMT
LABEL name=Silverpeas 6.3.4 description=Image to install and to run Silverpeas 6.3.4 vendor=Silverpeas version=6.3.4 build=1
# Thu, 02 May 2024 03:38:38 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Thu, 02 May 2024 03:38:39 GMT
COPY file:4d0e637a3e1ce0b8143795fd5df1997a7ee18fba27382849ed23e9ecb8142009 in /root/.m2/ 
# Thu, 02 May 2024 03:38:39 GMT
COPY file:473bf75b335a39b6b4b39c64cd151bd8ed3d3e33da73b8124e537a5db1fad3d6 in /opt/silverpeas/bin/ 
# Thu, 02 May 2024 03:38:39 GMT
WORKDIR /opt/silverpeas/bin
# Thu, 02 May 2024 03:38:39 GMT
COPY file:53a5e8023ae593585b413b14c995a55c412d5a4dff0ebcb7db632f2c22c39da6 in /opt/ 
# Thu, 02 May 2024 03:38:39 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Thu, 02 May 2024 03:40:56 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle   && ./silverpeas construct   && rm ../log/build-*   && touch .install
# Thu, 02 May 2024 03:40:59 GMT
EXPOSE 8000 9990
# Thu, 02 May 2024 03:40:59 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Thu, 02 May 2024 03:40:59 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:c83baea2d576c50e5cabbc3c34a47fbbbbd18a9230362ba713d603c9686181fb`  
		Last Modified: Sat, 27 Apr 2024 19:03:26 GMT  
		Size: 28.6 MB (28584299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:645064fb8cf6388b0a6f4bf6bb1c0dfdd016afecd0046fdeeabe9f8cae49c2fb`  
		Last Modified: Thu, 02 May 2024 03:42:37 GMT  
		Size: 762.5 MB (762500578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:539031f0affe0bed54d9b585f02a1a11eb3200c10d6d7897c1334aa1bdc8361b`  
		Last Modified: Thu, 02 May 2024 03:41:15 GMT  
		Size: 4.0 MB (3994066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f33f911a3dce78090ee6311dc1f1529d711d1dc0dd7dc7b993d65ebf07f22c`  
		Last Modified: Thu, 02 May 2024 03:41:15 GMT  
		Size: 7.1 MB (7146638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4f678a1462e69fc1768522e60d5356b82a0b0189009b8223e8f6a8c4b18e87c`  
		Last Modified: Thu, 02 May 2024 03:41:13 GMT  
		Size: 2.5 MB (2534372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb27bf2079e0f918455579034b845e1136f89249387e185ce64bab1235ceef3`  
		Last Modified: Thu, 02 May 2024 03:41:12 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fcdc53afa4b8fbba0a0e60f19c35dc056bfd186d66697a3660ea655982784dc`  
		Last Modified: Thu, 02 May 2024 03:41:12 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443606924b050b87b854803d95efd3366f3b94af134fde866a12db32b7d51073`  
		Last Modified: Thu, 02 May 2024 03:41:23 GMT  
		Size: 217.8 MB (217842687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66969e44c211a79af872bf4f318b246ac94d8221037276b05aac0190686017d7`  
		Last Modified: Thu, 02 May 2024 03:41:10 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57433da06cfee84247de79cdc2737b59857cd952a92132afc7b338510c541865`  
		Last Modified: Thu, 02 May 2024 03:41:10 GMT  
		Size: 664.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ba347f9bbc081269eb01271a07747300246a741d1ed8d4086756a1ad37c727`  
		Last Modified: Thu, 02 May 2024 03:41:10 GMT  
		Size: 911.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c2f5bfb2b88d486d8a3e0d5a4b0c8900ceba65d03edec49400e0c5c4b77fe1`  
		Last Modified: Thu, 02 May 2024 03:41:10 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc96857f1f08d3d241e7d8325add91f592a221d07c5955a9d9e63be501887da6`  
		Last Modified: Thu, 02 May 2024 03:41:45 GMT  
		Size: 754.6 MB (754562730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `silverpeas:latest`

```console
$ docker pull silverpeas@sha256:a9a4a8f2cd241c5cfcd1ec44c5d32ba636b154bbc490d2e8117381bedf31b483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `silverpeas:latest` - linux; amd64

```console
$ docker pull silverpeas@sha256:d2d59793bd0da5879cb918edc6946fb6b9eb23e050946aabcfa7618e0bd36a29
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1777168108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d35eb92c9d9711dd0bcc6cb6818450f52278a2fb9924a48228e680313ee3ba`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Sat, 27 Apr 2024 14:03:39 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:03:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:03:39 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 27 Apr 2024 14:03:41 GMT
ADD file:e5742fae181dc02a419e48d202fdd6a561b79ccbe7d3415e15e3d2c12e444a2a in / 
# Sat, 27 Apr 2024 14:03:41 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 03:29:10 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Thu, 02 May 2024 03:29:10 GMT
ENV TERM=xterm
# Thu, 02 May 2024 03:35:21 GMT
RUN apt-get update   && apt-get install -y tzdata   && apt-get install -y     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Thu, 02 May 2024 03:35:28 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Thu, 02 May 2024 03:35:31 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Thu, 02 May 2024 03:35:31 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Thu, 02 May 2024 03:36:11 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Thu, 02 May 2024 03:36:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 02 May 2024 03:36:11 GMT
ENV LANGUAGE=en_US.UTF-8
# Thu, 02 May 2024 03:36:11 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 02 May 2024 03:36:12 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 02 May 2024 03:36:12 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Thu, 02 May 2024 03:36:12 GMT
ENV JAVA_HOME=/docker-java-home
# Thu, 02 May 2024 03:36:12 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Thu, 02 May 2024 03:36:12 GMT
ENV JBOSS_HOME=/opt/wildfly
# Thu, 02 May 2024 03:36:13 GMT
ENV SILVERPEAS_VERSION=6.3.4
# Thu, 02 May 2024 03:36:13 GMT
ENV WILDFLY_VERSION=26.1.1
# Thu, 02 May 2024 03:36:13 GMT
LABEL name=Silverpeas 6.3.4 description=Image to install and to run Silverpeas 6.3.4 vendor=Silverpeas version=6.3.4 build=1
# Thu, 02 May 2024 03:38:38 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Thu, 02 May 2024 03:38:39 GMT
COPY file:4d0e637a3e1ce0b8143795fd5df1997a7ee18fba27382849ed23e9ecb8142009 in /root/.m2/ 
# Thu, 02 May 2024 03:38:39 GMT
COPY file:473bf75b335a39b6b4b39c64cd151bd8ed3d3e33da73b8124e537a5db1fad3d6 in /opt/silverpeas/bin/ 
# Thu, 02 May 2024 03:38:39 GMT
WORKDIR /opt/silverpeas/bin
# Thu, 02 May 2024 03:38:39 GMT
COPY file:53a5e8023ae593585b413b14c995a55c412d5a4dff0ebcb7db632f2c22c39da6 in /opt/ 
# Thu, 02 May 2024 03:38:39 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Thu, 02 May 2024 03:40:56 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle   && ./silverpeas construct   && rm ../log/build-*   && touch .install
# Thu, 02 May 2024 03:40:59 GMT
EXPOSE 8000 9990
# Thu, 02 May 2024 03:40:59 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Thu, 02 May 2024 03:40:59 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:c83baea2d576c50e5cabbc3c34a47fbbbbd18a9230362ba713d603c9686181fb`  
		Last Modified: Sat, 27 Apr 2024 19:03:26 GMT  
		Size: 28.6 MB (28584299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:645064fb8cf6388b0a6f4bf6bb1c0dfdd016afecd0046fdeeabe9f8cae49c2fb`  
		Last Modified: Thu, 02 May 2024 03:42:37 GMT  
		Size: 762.5 MB (762500578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:539031f0affe0bed54d9b585f02a1a11eb3200c10d6d7897c1334aa1bdc8361b`  
		Last Modified: Thu, 02 May 2024 03:41:15 GMT  
		Size: 4.0 MB (3994066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f33f911a3dce78090ee6311dc1f1529d711d1dc0dd7dc7b993d65ebf07f22c`  
		Last Modified: Thu, 02 May 2024 03:41:15 GMT  
		Size: 7.1 MB (7146638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4f678a1462e69fc1768522e60d5356b82a0b0189009b8223e8f6a8c4b18e87c`  
		Last Modified: Thu, 02 May 2024 03:41:13 GMT  
		Size: 2.5 MB (2534372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb27bf2079e0f918455579034b845e1136f89249387e185ce64bab1235ceef3`  
		Last Modified: Thu, 02 May 2024 03:41:12 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fcdc53afa4b8fbba0a0e60f19c35dc056bfd186d66697a3660ea655982784dc`  
		Last Modified: Thu, 02 May 2024 03:41:12 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443606924b050b87b854803d95efd3366f3b94af134fde866a12db32b7d51073`  
		Last Modified: Thu, 02 May 2024 03:41:23 GMT  
		Size: 217.8 MB (217842687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66969e44c211a79af872bf4f318b246ac94d8221037276b05aac0190686017d7`  
		Last Modified: Thu, 02 May 2024 03:41:10 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57433da06cfee84247de79cdc2737b59857cd952a92132afc7b338510c541865`  
		Last Modified: Thu, 02 May 2024 03:41:10 GMT  
		Size: 664.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ba347f9bbc081269eb01271a07747300246a741d1ed8d4086756a1ad37c727`  
		Last Modified: Thu, 02 May 2024 03:41:10 GMT  
		Size: 911.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c2f5bfb2b88d486d8a3e0d5a4b0c8900ceba65d03edec49400e0c5c4b77fe1`  
		Last Modified: Thu, 02 May 2024 03:41:10 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc96857f1f08d3d241e7d8325add91f592a221d07c5955a9d9e63be501887da6`  
		Last Modified: Thu, 02 May 2024 03:41:45 GMT  
		Size: 754.6 MB (754562730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
