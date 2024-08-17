<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `silverpeas`

-	[`silverpeas:6.3.5`](#silverpeas635)
-	[`silverpeas:6.4.1`](#silverpeas641)
-	[`silverpeas:latest`](#silverpeaslatest)

## `silverpeas:6.3.5`

```console
$ docker pull silverpeas@sha256:b4a156a717ad602f076beece54f59a4d209d3cee4007c83b1c9ad7b289fced99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `silverpeas:6.3.5` - linux; amd64

```console
$ docker pull silverpeas@sha256:19a4db4f229eecc60e2a0814370295066fb4212466e06e886475452eeb82415e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1777304497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43054a7167f6488d82547bcadd4d6107476e3d034d0a051061c4dc439e432c8b`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Tue, 13 Aug 2024 09:26:46 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:26:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:26:48 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Tue, 13 Aug 2024 09:26:48 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 01:58:11 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Sat, 17 Aug 2024 01:58:11 GMT
ENV TERM=xterm
# Sat, 17 Aug 2024 02:05:35 GMT
RUN apt-get update   && apt-get install -y tzdata   && apt-get install -y     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Sat, 17 Aug 2024 02:05:44 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Sat, 17 Aug 2024 02:05:47 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Sat, 17 Aug 2024 02:05:47 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Sat, 17 Aug 2024 02:06:25 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Sat, 17 Aug 2024 02:06:25 GMT
ENV LANG=en_US.UTF-8
# Sat, 17 Aug 2024 02:06:25 GMT
ENV LANGUAGE=en_US.UTF-8
# Sat, 17 Aug 2024 02:06:26 GMT
ENV LC_ALL=en_US.UTF-8
# Sat, 17 Aug 2024 02:06:26 GMT
ENV PING_ON=1
# Sat, 17 Aug 2024 02:06:26 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Sat, 17 Aug 2024 02:06:27 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Sat, 17 Aug 2024 02:06:27 GMT
ENV JAVA_HOME=/docker-java-home
# Sat, 17 Aug 2024 02:06:27 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Sat, 17 Aug 2024 02:06:27 GMT
ENV JBOSS_HOME=/opt/wildfly
# Sat, 17 Aug 2024 02:06:27 GMT
ENV SILVERPEAS_VERSION=6.3.5
# Sat, 17 Aug 2024 02:06:27 GMT
ENV WILDFLY_VERSION=26.1.1
# Sat, 17 Aug 2024 02:06:27 GMT
LABEL name=Silverpeas 6.3.5 description=Image to install and to run Silverpeas 6.3.5 vendor=Silverpeas version=6.3.5 build=1
# Sat, 17 Aug 2024 02:06:49 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Sat, 17 Aug 2024 02:06:49 GMT
COPY file:bdea684cbb56f9ec67736214361c476c97d0a0e06ec936f53a7da778776f533b in /root/.m2/ 
# Sat, 17 Aug 2024 02:06:49 GMT
COPY file:473bf75b335a39b6b4b39c64cd151bd8ed3d3e33da73b8124e537a5db1fad3d6 in /opt/silverpeas/bin/ 
# Sat, 17 Aug 2024 02:06:50 GMT
WORKDIR /opt/silverpeas/bin
# Sat, 17 Aug 2024 02:06:50 GMT
COPY file:d0f4d653b188d4ae9abc4034eaa253a720b62e15e65856fa78a99c4a4a58ad67 in /opt/ 
# Sat, 17 Aug 2024 02:06:50 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Sat, 17 Aug 2024 02:08:25 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle   && ./silverpeas construct   && rm ../log/build-*   && touch .install
# Sat, 17 Aug 2024 02:08:28 GMT
EXPOSE 8000 9990
# Sat, 17 Aug 2024 02:08:28 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Sat, 17 Aug 2024 02:08:29 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804c9775db37fcd412324c69fbc97461bcfc510def8e96d3859665d0a35355ed`  
		Last Modified: Sat, 17 Aug 2024 02:10:05 GMT  
		Size: 762.6 MB (762602744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07aa50089b4ff004f317ab84e647c776ed5c05e5e67d6d33a50a6ffa6f3461a`  
		Last Modified: Sat, 17 Aug 2024 02:08:45 GMT  
		Size: 4.0 MB (3994014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d439f48df55a52b1a943a8f3e885c1f9dfe7e7380f78ff5874acc416d00a245`  
		Last Modified: Sat, 17 Aug 2024 02:08:45 GMT  
		Size: 7.1 MB (7146603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5b16a0e05978f091749caca33ff1a1152966f5721745af1cbe97fc158da84f`  
		Last Modified: Sat, 17 Aug 2024 02:08:42 GMT  
		Size: 2.5 MB (2534354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e51fa8ac6698f1e33a10047ec707d8df89695bd036c9c2dd4d7a3b9fbda22f7`  
		Last Modified: Sat, 17 Aug 2024 02:08:42 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dafce072dcd8f349aaf1ec43d064f06513ffc525d69869f208d058615d744df`  
		Last Modified: Sat, 17 Aug 2024 02:08:42 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb38175cd6674824d4e5957af68c8d7228fa7edb04e6d18ca66db60dae71caf`  
		Last Modified: Sat, 17 Aug 2024 02:08:53 GMT  
		Size: 217.8 MB (217842620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d57aac1c9a166660c68dd06c398575361252ceb62bb93b486d89335f3e9d9112`  
		Last Modified: Sat, 17 Aug 2024 02:08:40 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d843011bae04647d7d633cb6b039010365b7eb07ccb01aa80f34eccea25c7e`  
		Last Modified: Sat, 17 Aug 2024 02:08:40 GMT  
		Size: 663.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648164feb5cf7d1b007c64fb15298cc1266b8befbd0cc006a840428640b52cdf`  
		Last Modified: Sat, 17 Aug 2024 02:08:40 GMT  
		Size: 925.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0cadde56c0b612bf713fe22cb8da6f220a3928a7160e1ec0238602aac7053da`  
		Last Modified: Sat, 17 Aug 2024 02:08:40 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e70972b3a5730d15c6164beffb4863428ce7e5a84d27368c1d7be4a10e756309`  
		Last Modified: Sat, 17 Aug 2024 02:09:14 GMT  
		Size: 754.6 MB (754597189 bytes)  
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
