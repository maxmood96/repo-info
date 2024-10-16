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
$ docker pull silverpeas@sha256:0cb172a6e740ca9bbc3bba981c5ca5ac81736ac7b763bfbc749d4103f3a9d9ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `silverpeas:6.4.1` - linux; amd64

```console
$ docker pull silverpeas@sha256:2fe89bd62dba5823d8c9d6b814c7c25928703d6175523f1c7d7ce3772db042f6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1805441233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:979f38a471110fedab8b072de0965d3350816816a082e7c407f02136f0fa4332`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Mon, 24 Jun 2024 23:20:35 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Mon, 24 Jun 2024 23:20:35 GMT
ENV TERM=xterm
# Mon, 24 Jun 2024 23:25:33 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends tzdata   && apt-get install -y --no-install-recommends     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Mon, 24 Jun 2024 23:25:40 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 swftools-bin-0.9.2.zip' | sha256sum -c --status -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Mon, 24 Jun 2024 23:25:44 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 pdf2json-bin-0.68.zip' | sha256sum -c --status -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Mon, 24 Jun 2024 23:25:44 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Mon, 24 Jun 2024 23:26:25 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Mon, 24 Jun 2024 23:26:25 GMT
ENV LANG=en_US.UTF-8
# Mon, 24 Jun 2024 23:26:25 GMT
ENV LANGUAGE=en_US.UTF-8
# Mon, 24 Jun 2024 23:26:25 GMT
ENV LC_ALL=en_US.UTF-8
# Mon, 24 Jun 2024 23:26:25 GMT
ENV PING_ON=1
# Mon, 24 Jun 2024 23:26:26 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Mon, 24 Jun 2024 23:26:26 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Mon, 24 Jun 2024 23:26:26 GMT
ENV JAVA_HOME=/docker-java-home
# Mon, 24 Jun 2024 23:26:27 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Mon, 24 Jun 2024 23:26:27 GMT
ENV JBOSS_HOME=/opt/wildfly
# Wed, 26 Jun 2024 19:39:52 GMT
ENV SILVERPEAS_VERSION=6.4.1
# Wed, 26 Jun 2024 19:39:52 GMT
ENV WILDFLY_VERSION=26.1.3
# Wed, 26 Jun 2024 19:39:52 GMT
LABEL name=Silverpeas 6.4.1 description=Image to install and to run Silverpeas 6.4.1 vendor=Silverpeas version=6.4.1 build=1
# Wed, 26 Jun 2024 19:40:20 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && wget -nc https://www.silverpeas.org/files/oak-migrate.zip   && echo '02d21f69004f2d9e634e82ec062d94521bd6bc0385d7c0ddf9af261cb63afdbb oak-migrate.zip' | sha256sum -c --status -   && mkdir -p /opt/oak-migration   && unzip oak-migrate.zip -d /opt/oak-migration/   && chmod +x /opt/oak-migration/oak-migrate.sh   && rm *.zip   && mkdir -p /root/.m2
# Wed, 26 Jun 2024 19:40:21 GMT
COPY file:bdea684cbb56f9ec67736214361c476c97d0a0e06ec936f53a7da778776f533b in /root/.m2/ 
# Wed, 26 Jun 2024 19:40:21 GMT
COPY file:473bf75b335a39b6b4b39c64cd151bd8ed3d3e33da73b8124e537a5db1fad3d6 in /opt/silverpeas/bin/ 
# Wed, 26 Jun 2024 19:40:22 GMT
WORKDIR /opt/silverpeas/bin
# Wed, 26 Jun 2024 19:40:22 GMT
COPY file:39b5296ac06d483424dc84ebab1183a21a787142115d7243720e010eb696d296 in /opt/ 
# Wed, 26 Jun 2024 19:40:22 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Wed, 26 Jun 2024 19:42:03 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN set -eux;   sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle;   echo "Construct Silverpeas ${SILVERPEAS_VERSION}";   ./silverpeas assemble || (cat ../log/build-* && exit 1);   rm ../log/build-*;   touch .install;
# Wed, 26 Jun 2024 19:42:07 GMT
EXPOSE 8000 9990
# Wed, 26 Jun 2024 19:42:07 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Wed, 26 Jun 2024 19:42:08 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d197a946d6993801aed554996da8580dc87a21f3714d2aa44ba65cb7c77bddac`  
		Last Modified: Mon, 24 Jun 2024 23:31:08 GMT  
		Size: 494.6 MB (494632993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d222bf6236654b25c0aa52449c441540f9743bb6bfca6635a30a7f253fe3582`  
		Last Modified: Mon, 24 Jun 2024 23:30:11 GMT  
		Size: 4.0 MB (3994018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38aff74284c1f81c367412391c1bb1bda03cf5517e3f740d58306b2fcae98547`  
		Last Modified: Mon, 24 Jun 2024 23:30:12 GMT  
		Size: 7.1 MB (7146630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a5abe18a77a2ae4e782119767491481b95cf2227bac6a533a1c9e33b68896d9`  
		Last Modified: Mon, 24 Jun 2024 23:30:09 GMT  
		Size: 2.5 MB (2538607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4008e9bc952c50d44e190fc329b0dbe5ce85e789dab5a04d6946e76429d1b6a`  
		Last Modified: Mon, 24 Jun 2024 23:30:08 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc75f05005e2792a0730969bafb045ed74d00e36302bc036404e097dfecf4842`  
		Last Modified: Mon, 24 Jun 2024 23:30:08 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc81cf5d95d8b5ecd659ee3fd6f32a6ab693a448dd28af873a39f2a1741859d`  
		Last Modified: Wed, 26 Jun 2024 19:42:39 GMT  
		Size: 267.1 MB (267147193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db04f4bad9f63d17ae08776d5524832a390f4d43267141703bf4722f3af409f3`  
		Last Modified: Wed, 26 Jun 2024 19:42:24 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b54f083ebc080fe862aabdae4d886828d7fb4b0c294637e9afce86a01b18501`  
		Last Modified: Wed, 26 Jun 2024 19:42:25 GMT  
		Size: 659.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48763f4f9cf30f1630634c379c571ecda02568d45783cc60071c0c9c2a2c63b0`  
		Last Modified: Wed, 26 Jun 2024 19:42:25 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d9d69fc13ba8f6f9d3ec7ca13ce6062d3967119ffd3aaabb596d1d50e7f5d3`  
		Last Modified: Wed, 26 Jun 2024 19:42:25 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c22f742ca52055107e7f7afbe3c552d165a195ff3faca875b949ed2609319b`  
		Last Modified: Wed, 26 Jun 2024 19:43:07 GMT  
		Size: 999.5 MB (999539247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `silverpeas:latest`

```console
$ docker pull silverpeas@sha256:0cb172a6e740ca9bbc3bba981c5ca5ac81736ac7b763bfbc749d4103f3a9d9ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `silverpeas:latest` - linux; amd64

```console
$ docker pull silverpeas@sha256:2fe89bd62dba5823d8c9d6b814c7c25928703d6175523f1c7d7ce3772db042f6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1805441233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:979f38a471110fedab8b072de0965d3350816816a082e7c407f02136f0fa4332`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Mon, 24 Jun 2024 23:20:35 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Mon, 24 Jun 2024 23:20:35 GMT
ENV TERM=xterm
# Mon, 24 Jun 2024 23:25:33 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends tzdata   && apt-get install -y --no-install-recommends     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Mon, 24 Jun 2024 23:25:40 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 swftools-bin-0.9.2.zip' | sha256sum -c --status -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Mon, 24 Jun 2024 23:25:44 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 pdf2json-bin-0.68.zip' | sha256sum -c --status -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Mon, 24 Jun 2024 23:25:44 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Mon, 24 Jun 2024 23:26:25 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Mon, 24 Jun 2024 23:26:25 GMT
ENV LANG=en_US.UTF-8
# Mon, 24 Jun 2024 23:26:25 GMT
ENV LANGUAGE=en_US.UTF-8
# Mon, 24 Jun 2024 23:26:25 GMT
ENV LC_ALL=en_US.UTF-8
# Mon, 24 Jun 2024 23:26:25 GMT
ENV PING_ON=1
# Mon, 24 Jun 2024 23:26:26 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Mon, 24 Jun 2024 23:26:26 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Mon, 24 Jun 2024 23:26:26 GMT
ENV JAVA_HOME=/docker-java-home
# Mon, 24 Jun 2024 23:26:27 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Mon, 24 Jun 2024 23:26:27 GMT
ENV JBOSS_HOME=/opt/wildfly
# Wed, 26 Jun 2024 19:39:52 GMT
ENV SILVERPEAS_VERSION=6.4.1
# Wed, 26 Jun 2024 19:39:52 GMT
ENV WILDFLY_VERSION=26.1.3
# Wed, 26 Jun 2024 19:39:52 GMT
LABEL name=Silverpeas 6.4.1 description=Image to install and to run Silverpeas 6.4.1 vendor=Silverpeas version=6.4.1 build=1
# Wed, 26 Jun 2024 19:40:20 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && wget -nc https://www.silverpeas.org/files/oak-migrate.zip   && echo '02d21f69004f2d9e634e82ec062d94521bd6bc0385d7c0ddf9af261cb63afdbb oak-migrate.zip' | sha256sum -c --status -   && mkdir -p /opt/oak-migration   && unzip oak-migrate.zip -d /opt/oak-migration/   && chmod +x /opt/oak-migration/oak-migrate.sh   && rm *.zip   && mkdir -p /root/.m2
# Wed, 26 Jun 2024 19:40:21 GMT
COPY file:bdea684cbb56f9ec67736214361c476c97d0a0e06ec936f53a7da778776f533b in /root/.m2/ 
# Wed, 26 Jun 2024 19:40:21 GMT
COPY file:473bf75b335a39b6b4b39c64cd151bd8ed3d3e33da73b8124e537a5db1fad3d6 in /opt/silverpeas/bin/ 
# Wed, 26 Jun 2024 19:40:22 GMT
WORKDIR /opt/silverpeas/bin
# Wed, 26 Jun 2024 19:40:22 GMT
COPY file:39b5296ac06d483424dc84ebab1183a21a787142115d7243720e010eb696d296 in /opt/ 
# Wed, 26 Jun 2024 19:40:22 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Wed, 26 Jun 2024 19:42:03 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN set -eux;   sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle;   echo "Construct Silverpeas ${SILVERPEAS_VERSION}";   ./silverpeas assemble || (cat ../log/build-* && exit 1);   rm ../log/build-*;   touch .install;
# Wed, 26 Jun 2024 19:42:07 GMT
EXPOSE 8000 9990
# Wed, 26 Jun 2024 19:42:07 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Wed, 26 Jun 2024 19:42:08 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d197a946d6993801aed554996da8580dc87a21f3714d2aa44ba65cb7c77bddac`  
		Last Modified: Mon, 24 Jun 2024 23:31:08 GMT  
		Size: 494.6 MB (494632993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d222bf6236654b25c0aa52449c441540f9743bb6bfca6635a30a7f253fe3582`  
		Last Modified: Mon, 24 Jun 2024 23:30:11 GMT  
		Size: 4.0 MB (3994018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38aff74284c1f81c367412391c1bb1bda03cf5517e3f740d58306b2fcae98547`  
		Last Modified: Mon, 24 Jun 2024 23:30:12 GMT  
		Size: 7.1 MB (7146630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a5abe18a77a2ae4e782119767491481b95cf2227bac6a533a1c9e33b68896d9`  
		Last Modified: Mon, 24 Jun 2024 23:30:09 GMT  
		Size: 2.5 MB (2538607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4008e9bc952c50d44e190fc329b0dbe5ce85e789dab5a04d6946e76429d1b6a`  
		Last Modified: Mon, 24 Jun 2024 23:30:08 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc75f05005e2792a0730969bafb045ed74d00e36302bc036404e097dfecf4842`  
		Last Modified: Mon, 24 Jun 2024 23:30:08 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc81cf5d95d8b5ecd659ee3fd6f32a6ab693a448dd28af873a39f2a1741859d`  
		Last Modified: Wed, 26 Jun 2024 19:42:39 GMT  
		Size: 267.1 MB (267147193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db04f4bad9f63d17ae08776d5524832a390f4d43267141703bf4722f3af409f3`  
		Last Modified: Wed, 26 Jun 2024 19:42:24 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b54f083ebc080fe862aabdae4d886828d7fb4b0c294637e9afce86a01b18501`  
		Last Modified: Wed, 26 Jun 2024 19:42:25 GMT  
		Size: 659.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48763f4f9cf30f1630634c379c571ecda02568d45783cc60071c0c9c2a2c63b0`  
		Last Modified: Wed, 26 Jun 2024 19:42:25 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49d9d69fc13ba8f6f9d3ec7ca13ce6062d3967119ffd3aaabb596d1d50e7f5d3`  
		Last Modified: Wed, 26 Jun 2024 19:42:25 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c22f742ca52055107e7f7afbe3c552d165a195ff3faca875b949ed2609319b`  
		Last Modified: Wed, 26 Jun 2024 19:43:07 GMT  
		Size: 999.5 MB (999539247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
