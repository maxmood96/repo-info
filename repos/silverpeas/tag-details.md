<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `silverpeas`

-	[`silverpeas:6.3.5`](#silverpeas635)
-	[`silverpeas:6.4.1`](#silverpeas641)
-	[`silverpeas:latest`](#silverpeaslatest)

## `silverpeas:6.3.5`

```console
$ docker pull silverpeas@sha256:007a4a244b48b242ebf8d1eb1278665b195cb3e0d62b4d27d1d3387ca0fd12cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `silverpeas:6.3.5` - linux; amd64

```console
$ docker pull silverpeas@sha256:dfaa62f650eeb2027717f9c20ebda5d2c3e959b62773d57e8d253d32889e4e3f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1777274000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49dd4207eb91c83bdb10f8bf717f2df4742372b48a9c5e3580be7b4fd5baa39e`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 01:45:44 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Wed, 16 Oct 2024 01:45:44 GMT
ENV TERM=xterm
# Wed, 16 Oct 2024 01:53:54 GMT
RUN apt-get update   && apt-get install -y tzdata   && apt-get install -y     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Wed, 16 Oct 2024 01:54:04 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Wed, 16 Oct 2024 01:54:07 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Wed, 16 Oct 2024 01:54:07 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Wed, 16 Oct 2024 01:54:47 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Wed, 16 Oct 2024 01:54:47 GMT
ENV LANG=en_US.UTF-8
# Wed, 16 Oct 2024 01:54:47 GMT
ENV LANGUAGE=en_US.UTF-8
# Wed, 16 Oct 2024 01:54:47 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 16 Oct 2024 01:54:47 GMT
ENV PING_ON=1
# Wed, 16 Oct 2024 01:54:48 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 16 Oct 2024 01:54:48 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 16 Oct 2024 01:54:48 GMT
ENV JAVA_HOME=/docker-java-home
# Wed, 16 Oct 2024 01:54:49 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Wed, 16 Oct 2024 01:54:49 GMT
ENV JBOSS_HOME=/opt/wildfly
# Wed, 16 Oct 2024 01:54:49 GMT
ENV SILVERPEAS_VERSION=6.3.5
# Wed, 16 Oct 2024 01:54:49 GMT
ENV WILDFLY_VERSION=26.1.1
# Wed, 16 Oct 2024 01:54:49 GMT
LABEL name=Silverpeas 6.3.5 description=Image to install and to run Silverpeas 6.3.5 vendor=Silverpeas version=6.3.5 build=1
# Wed, 16 Oct 2024 01:55:11 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Wed, 16 Oct 2024 01:55:11 GMT
COPY file:bdea684cbb56f9ec67736214361c476c97d0a0e06ec936f53a7da778776f533b in /root/.m2/ 
# Wed, 16 Oct 2024 01:55:11 GMT
COPY file:473bf75b335a39b6b4b39c64cd151bd8ed3d3e33da73b8124e537a5db1fad3d6 in /opt/silverpeas/bin/ 
# Wed, 16 Oct 2024 01:55:11 GMT
WORKDIR /opt/silverpeas/bin
# Wed, 16 Oct 2024 01:55:12 GMT
COPY file:d0f4d653b188d4ae9abc4034eaa253a720b62e15e65856fa78a99c4a4a58ad67 in /opt/ 
# Wed, 16 Oct 2024 01:55:12 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Wed, 16 Oct 2024 01:56:46 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle   && ./silverpeas construct   && rm ../log/build-*   && touch .install
# Wed, 16 Oct 2024 01:56:49 GMT
EXPOSE 8000 9990
# Wed, 16 Oct 2024 01:56:49 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Wed, 16 Oct 2024 01:56:49 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:86e5016c269355b382c9cabab4f6646d56d75914f20d545289970436dae431b1`  
		Last Modified: Fri, 11 Oct 2024 08:12:19 GMT  
		Size: 28.6 MB (28583948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01636e6b7b19a1acbd7cf43e5f63a38f4ed32f32667583d98f89ddbf0faa6925`  
		Last Modified: Wed, 16 Oct 2024 01:58:23 GMT  
		Size: 762.6 MB (762573442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30dbba552b07181c2d628a16831ead83e7d162c74b5da661493e6383b1a2b65c`  
		Last Modified: Wed, 16 Oct 2024 01:57:01 GMT  
		Size: 4.0 MB (3994005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a99f39985845ed37d1e82c82806d987518c3734259a9a5cf1b8a82d9b0071f`  
		Last Modified: Wed, 16 Oct 2024 01:57:02 GMT  
		Size: 7.1 MB (7146612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3016422d6c7b4bc5c14038fc7d674a47b22c6bddb242827f9fef9c26f0a318`  
		Last Modified: Wed, 16 Oct 2024 01:56:59 GMT  
		Size: 2.5 MB (2534353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5398dc2c9ae1d650232978daadd3c16dc447f005c6f15113d9b97def66aafcc6`  
		Last Modified: Wed, 16 Oct 2024 01:56:59 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a45ba846476e03ab8916ea56119e25a5bd7034e123f35331361c9dce0b066069`  
		Last Modified: Wed, 16 Oct 2024 01:56:59 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007c2475a7710dde73940acc010e90942c48487b6aff0a5a4b83c1ae291aedea`  
		Last Modified: Wed, 16 Oct 2024 01:57:10 GMT  
		Size: 217.8 MB (217842622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50938d33a3cf8857bcea99f1eb7278be5f4bbd32b2b5eb4fef647fc3baed4d2a`  
		Last Modified: Wed, 16 Oct 2024 01:56:57 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea64cd0cd7b2f050e8278ada44a25eaef744298554c13a797b774a2841ea7586`  
		Last Modified: Wed, 16 Oct 2024 01:56:57 GMT  
		Size: 664.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5109cfe546b25d3e3e50ed11983b5d5722bd86920a7c4814d8627101fb65138c`  
		Last Modified: Wed, 16 Oct 2024 01:56:57 GMT  
		Size: 922.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73990e5419da7918441a89a241a0e6c6394618fe18b72ee4cedd5c3401d7cdc`  
		Last Modified: Wed, 16 Oct 2024 01:56:57 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f9beda50fd95818a6961c2238ccdcedb5dd39123f5ed84d370c90f50640b143`  
		Last Modified: Wed, 16 Oct 2024 01:57:32 GMT  
		Size: 754.6 MB (754596265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `silverpeas:6.4.1`

```console
$ docker pull silverpeas@sha256:d27031cb56c1130912e716680c03444ced7e6f41eb46ab54b781cd8cb9af2e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `silverpeas:6.4.1` - linux; amd64

```console
$ docker pull silverpeas@sha256:8ce4860fe654fe5814baf97e29b2c6acb4341611df7088cd3efce53e1ba7bf04
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1807407746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d8d26a14616c0e1f82b8fc634961349a7ecdc4b6d013aa7a2a0f652401664c4`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Fri, 18 Oct 2024 19:59:19 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Fri, 18 Oct 2024 19:59:19 GMT
ENV TERM=xterm
# Fri, 18 Oct 2024 20:05:00 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends tzdata   && apt-get install -y --no-install-recommends     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Fri, 18 Oct 2024 20:05:07 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 swftools-bin-0.9.2.zip' | sha256sum -c --status -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Fri, 18 Oct 2024 20:05:10 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 pdf2json-bin-0.68.zip' | sha256sum -c --status -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Fri, 18 Oct 2024 20:05:10 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Fri, 18 Oct 2024 20:05:51 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Fri, 18 Oct 2024 20:05:51 GMT
ENV LANG=en_US.UTF-8
# Fri, 18 Oct 2024 20:05:51 GMT
ENV LANGUAGE=en_US.UTF-8
# Fri, 18 Oct 2024 20:05:51 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 18 Oct 2024 20:05:51 GMT
ENV PING_ON=1
# Fri, 18 Oct 2024 20:05:52 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 18 Oct 2024 20:05:52 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 18 Oct 2024 20:05:52 GMT
ENV JAVA_HOME=/docker-java-home
# Fri, 18 Oct 2024 20:05:53 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Fri, 18 Oct 2024 20:05:53 GMT
ENV JBOSS_HOME=/opt/wildfly
# Fri, 18 Oct 2024 20:05:53 GMT
ENV SILVERPEAS_VERSION=6.4.1
# Fri, 18 Oct 2024 20:05:53 GMT
ENV WILDFLY_VERSION=26.1.3
# Fri, 18 Oct 2024 20:05:53 GMT
LABEL name=Silverpeas 6.4.1 description=Image to install and to run Silverpeas 6.4.1 vendor=Silverpeas version=6.4.1 build=2
# Fri, 18 Oct 2024 20:06:22 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && wget -nc https://www.silverpeas.org/files/oak-migrate.zip   && echo '87009e55520e74b5d2a386f4ebc843ee43cd1f25ca5138f342a94a31add3cfbd oak-migrate.zip' | sha256sum -c --status -   && mkdir -p /opt/oak-migration   && unzip oak-migrate.zip -d /opt/oak-migration/   && chmod +x /opt/oak-migration/oak-migrate.sh   && rm *.zip   && mkdir -p /root/.m2
# Fri, 18 Oct 2024 20:06:22 GMT
COPY file:bdea684cbb56f9ec67736214361c476c97d0a0e06ec936f53a7da778776f533b in /root/.m2/ 
# Fri, 18 Oct 2024 20:06:23 GMT
COPY file:473bf75b335a39b6b4b39c64cd151bd8ed3d3e33da73b8124e537a5db1fad3d6 in /opt/silverpeas/bin/ 
# Fri, 18 Oct 2024 20:06:23 GMT
WORKDIR /opt/silverpeas/bin
# Fri, 18 Oct 2024 20:06:23 GMT
COPY file:39b5296ac06d483424dc84ebab1183a21a787142115d7243720e010eb696d296 in /opt/ 
# Fri, 18 Oct 2024 20:06:23 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Fri, 18 Oct 2024 20:07:54 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN set -eux;   sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle;   echo "Construct Silverpeas ${SILVERPEAS_VERSION}";   ./silverpeas assemble || (cat ../log/build-* && exit 1);   rm ../log/build-*;   touch .install;
# Fri, 18 Oct 2024 20:07:59 GMT
EXPOSE 8000 9990
# Fri, 18 Oct 2024 20:07:59 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Fri, 18 Oct 2024 20:07:59 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3486afb2275f50c531e6dd7cf5269390807bfcafa8204b5663ed5cd8649facdc`  
		Last Modified: Fri, 18 Oct 2024 20:09:21 GMT  
		Size: 494.6 MB (494645785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be6bf08e77e29cb2aa14a054bdcbb5ab9a6d3683ba5d928e4e184e4b635007c`  
		Last Modified: Fri, 18 Oct 2024 20:08:25 GMT  
		Size: 4.0 MB (3994012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f034f4713a1e08403394d21296cac9d44db477410018fcb7011dc4d644936295`  
		Last Modified: Fri, 18 Oct 2024 20:08:25 GMT  
		Size: 7.1 MB (7146627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d9273b3707d5c56d4ba45c2f737340a3bb3df3f06fb6da8176123d106dfaf3b`  
		Last Modified: Fri, 18 Oct 2024 20:08:23 GMT  
		Size: 2.5 MB (2538614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0eb6fef2198bff80b8fc15b76d581b91d763198cf57bb56e2579cf804d94c94`  
		Last Modified: Fri, 18 Oct 2024 20:08:22 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ef4263d81de7cf864de750249df23c9bb85d8250b5386b2749f39bf72d55ad`  
		Last Modified: Fri, 18 Oct 2024 20:08:22 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf92047eb4712ff576357fc80d08d2f52dab3cb2086fc4f5b353cd5d44da764`  
		Last Modified: Fri, 18 Oct 2024 20:08:36 GMT  
		Size: 269.1 MB (269105533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d303d5f1acf87483bf5b5f4a584a33a669ce2e62b3598e9ee56ba000435397`  
		Last Modified: Fri, 18 Oct 2024 20:08:20 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1618743bad82c8d65d415015b8c2b800076447e4fecb00cd1c1410130f23ee09`  
		Last Modified: Fri, 18 Oct 2024 20:08:20 GMT  
		Size: 665.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40133226d2832a94597ac6ad020f57514ff9af887a76107b51013d82dae868f`  
		Last Modified: Fri, 18 Oct 2024 20:08:20 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ece2c1e70cef441bd496acb9b5d0fabdbc9994d871e87846f458176dd874dfcb`  
		Last Modified: Fri, 18 Oct 2024 20:08:20 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75a3f8935e5c822d3eca0a612425aa5cc0c5b90dab997ae362a67887728eae4`  
		Last Modified: Fri, 18 Oct 2024 20:09:05 GMT  
		Size: 999.5 MB (999533966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `silverpeas:latest`

```console
$ docker pull silverpeas@sha256:d27031cb56c1130912e716680c03444ced7e6f41eb46ab54b781cd8cb9af2e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `silverpeas:latest` - linux; amd64

```console
$ docker pull silverpeas@sha256:8ce4860fe654fe5814baf97e29b2c6acb4341611df7088cd3efce53e1ba7bf04
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1807407746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d8d26a14616c0e1f82b8fc634961349a7ecdc4b6d013aa7a2a0f652401664c4`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Fri, 18 Oct 2024 19:59:19 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Fri, 18 Oct 2024 19:59:19 GMT
ENV TERM=xterm
# Fri, 18 Oct 2024 20:05:00 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends tzdata   && apt-get install -y --no-install-recommends     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Fri, 18 Oct 2024 20:05:07 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 swftools-bin-0.9.2.zip' | sha256sum -c --status -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Fri, 18 Oct 2024 20:05:10 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 pdf2json-bin-0.68.zip' | sha256sum -c --status -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Fri, 18 Oct 2024 20:05:10 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Fri, 18 Oct 2024 20:05:51 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Fri, 18 Oct 2024 20:05:51 GMT
ENV LANG=en_US.UTF-8
# Fri, 18 Oct 2024 20:05:51 GMT
ENV LANGUAGE=en_US.UTF-8
# Fri, 18 Oct 2024 20:05:51 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 18 Oct 2024 20:05:51 GMT
ENV PING_ON=1
# Fri, 18 Oct 2024 20:05:52 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 18 Oct 2024 20:05:52 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 18 Oct 2024 20:05:52 GMT
ENV JAVA_HOME=/docker-java-home
# Fri, 18 Oct 2024 20:05:53 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Fri, 18 Oct 2024 20:05:53 GMT
ENV JBOSS_HOME=/opt/wildfly
# Fri, 18 Oct 2024 20:05:53 GMT
ENV SILVERPEAS_VERSION=6.4.1
# Fri, 18 Oct 2024 20:05:53 GMT
ENV WILDFLY_VERSION=26.1.3
# Fri, 18 Oct 2024 20:05:53 GMT
LABEL name=Silverpeas 6.4.1 description=Image to install and to run Silverpeas 6.4.1 vendor=Silverpeas version=6.4.1 build=2
# Fri, 18 Oct 2024 20:06:22 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && wget -nc https://www.silverpeas.org/files/oak-migrate.zip   && echo '87009e55520e74b5d2a386f4ebc843ee43cd1f25ca5138f342a94a31add3cfbd oak-migrate.zip' | sha256sum -c --status -   && mkdir -p /opt/oak-migration   && unzip oak-migrate.zip -d /opt/oak-migration/   && chmod +x /opt/oak-migration/oak-migrate.sh   && rm *.zip   && mkdir -p /root/.m2
# Fri, 18 Oct 2024 20:06:22 GMT
COPY file:bdea684cbb56f9ec67736214361c476c97d0a0e06ec936f53a7da778776f533b in /root/.m2/ 
# Fri, 18 Oct 2024 20:06:23 GMT
COPY file:473bf75b335a39b6b4b39c64cd151bd8ed3d3e33da73b8124e537a5db1fad3d6 in /opt/silverpeas/bin/ 
# Fri, 18 Oct 2024 20:06:23 GMT
WORKDIR /opt/silverpeas/bin
# Fri, 18 Oct 2024 20:06:23 GMT
COPY file:39b5296ac06d483424dc84ebab1183a21a787142115d7243720e010eb696d296 in /opt/ 
# Fri, 18 Oct 2024 20:06:23 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Fri, 18 Oct 2024 20:07:54 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN set -eux;   sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle;   echo "Construct Silverpeas ${SILVERPEAS_VERSION}";   ./silverpeas assemble || (cat ../log/build-* && exit 1);   rm ../log/build-*;   touch .install;
# Fri, 18 Oct 2024 20:07:59 GMT
EXPOSE 8000 9990
# Fri, 18 Oct 2024 20:07:59 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Fri, 18 Oct 2024 20:07:59 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:7478e0ac0f23f94b2f27848fbcdf804a670fbf8d4bab26df842d40a10cd33059`  
		Last Modified: Wed, 11 Sep 2024 21:27:10 GMT  
		Size: 30.4 MB (30439933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3486afb2275f50c531e6dd7cf5269390807bfcafa8204b5663ed5cd8649facdc`  
		Last Modified: Fri, 18 Oct 2024 20:09:21 GMT  
		Size: 494.6 MB (494645785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be6bf08e77e29cb2aa14a054bdcbb5ab9a6d3683ba5d928e4e184e4b635007c`  
		Last Modified: Fri, 18 Oct 2024 20:08:25 GMT  
		Size: 4.0 MB (3994012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f034f4713a1e08403394d21296cac9d44db477410018fcb7011dc4d644936295`  
		Last Modified: Fri, 18 Oct 2024 20:08:25 GMT  
		Size: 7.1 MB (7146627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d9273b3707d5c56d4ba45c2f737340a3bb3df3f06fb6da8176123d106dfaf3b`  
		Last Modified: Fri, 18 Oct 2024 20:08:23 GMT  
		Size: 2.5 MB (2538614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0eb6fef2198bff80b8fc15b76d581b91d763198cf57bb56e2579cf804d94c94`  
		Last Modified: Fri, 18 Oct 2024 20:08:22 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ef4263d81de7cf864de750249df23c9bb85d8250b5386b2749f39bf72d55ad`  
		Last Modified: Fri, 18 Oct 2024 20:08:22 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf92047eb4712ff576357fc80d08d2f52dab3cb2086fc4f5b353cd5d44da764`  
		Last Modified: Fri, 18 Oct 2024 20:08:36 GMT  
		Size: 269.1 MB (269105533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d303d5f1acf87483bf5b5f4a584a33a669ce2e62b3598e9ee56ba000435397`  
		Last Modified: Fri, 18 Oct 2024 20:08:20 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1618743bad82c8d65d415015b8c2b800076447e4fecb00cd1c1410130f23ee09`  
		Last Modified: Fri, 18 Oct 2024 20:08:20 GMT  
		Size: 665.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40133226d2832a94597ac6ad020f57514ff9af887a76107b51013d82dae868f`  
		Last Modified: Fri, 18 Oct 2024 20:08:20 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ece2c1e70cef441bd496acb9b5d0fabdbc9994d871e87846f458176dd874dfcb`  
		Last Modified: Fri, 18 Oct 2024 20:08:20 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75a3f8935e5c822d3eca0a612425aa5cc0c5b90dab997ae362a67887728eae4`  
		Last Modified: Fri, 18 Oct 2024 20:09:05 GMT  
		Size: 999.5 MB (999533966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
