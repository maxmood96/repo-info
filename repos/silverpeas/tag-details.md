<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `silverpeas`

-	[`silverpeas:6.3.6`](#silverpeas636)
-	[`silverpeas:6.4.6`](#silverpeas646)
-	[`silverpeas:latest`](#silverpeaslatest)

## `silverpeas:6.3.6`

```console
$ docker pull silverpeas@sha256:287a1b2cb804a710f36da1958a4505efb8dfbcae7949af358bd00917b4cce9e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `silverpeas:6.3.6` - linux; amd64

```console
$ docker pull silverpeas@sha256:16a95648c40c192852a03c1d8b887440966649cb17166d1967c14e7bca0ca1b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1887530304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:152c6ba0ad326b84ad0a78023248d18fef78627961d3a4de761b2c39503ea88e`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:23:54 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Fri, 15 May 2026 21:23:54 GMT
ENV TERM=xterm
# Fri, 15 May 2026 21:23:54 GMT
RUN apt-get update   && apt-get install -y tzdata   && apt-get install -y     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f # buildkit
# Fri, 15 May 2026 21:23:56 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip # buildkit
# Fri, 15 May 2026 21:23:58 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip # buildkit
# Fri, 15 May 2026 21:23:58 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Fri, 15 May 2026 21:24:22 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE} # buildkit
# Fri, 15 May 2026 21:24:22 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:24:22 GMT
ENV LANGUAGE=en_US.UTF-8
# Fri, 15 May 2026 21:24:22 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 15 May 2026 21:24:22 GMT
ENV PING_ON=1
# Fri, 15 May 2026 21:24:22 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home # buildkit
# Fri, 15 May 2026 21:24:22 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home # buildkit
# Fri, 15 May 2026 21:24:22 GMT
ENV JAVA_HOME=/docker-java-home
# Fri, 15 May 2026 21:24:22 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Fri, 15 May 2026 21:24:22 GMT
ENV JBOSS_HOME=/opt/wildfly
# Fri, 15 May 2026 21:24:22 GMT
ENV SILVERPEAS_VERSION=6.3.6
# Fri, 15 May 2026 21:24:22 GMT
ENV WILDFLY_VERSION=26.1.1
# Fri, 15 May 2026 21:24:22 GMT
LABEL name=Silverpeas 6.3.6 description=Image to install and to run Silverpeas 6.3.6 vendor=Silverpeas version=6.3.6 build=2
# Fri, 15 May 2026 21:24:50 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2 # buildkit
# Fri, 15 May 2026 21:24:50 GMT
COPY src/settings.xml /root/.m2/ # buildkit
# Fri, 15 May 2026 21:24:50 GMT
COPY src/silverpeas.gradle /opt/silverpeas/bin/ # buildkit
# Fri, 15 May 2026 21:24:50 GMT
WORKDIR /opt/silverpeas/bin
# Fri, 15 May 2026 21:24:50 GMT
COPY src/run.sh /opt/ # buildkit
# Fri, 15 May 2026 21:24:50 GMT
COPY src/converter.groovy /opt/silverpeas/configuration/silverpeas/ # buildkit
# Fri, 15 May 2026 21:26:02 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle   && ./silverpeas construct   && rm ../log/build-*   && touch .install # buildkit
# Fri, 15 May 2026 21:26:02 GMT
EXPOSE map[8000/tcp:{} 9990/tcp:{}]
# Fri, 15 May 2026 21:26:02 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Fri, 15 May 2026 21:26:02 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea92e74b8a3734863448c9a0d1cd523046d8d5579f02b6e8e717ad4590f9cd95`  
		Last Modified: Fri, 15 May 2026 21:28:49 GMT  
		Size: 871.7 MB (871662544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a730454f6dbb5ffc5df525d9a624efb6b10a95c4a29455b303d8b317494fcb1a`  
		Last Modified: Fri, 15 May 2026 21:28:08 GMT  
		Size: 4.0 MB (3994010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dcbecc6126bb548ea15f1cdd5647648da9319f4cd31ffa6a61c49e7ac154bd2`  
		Last Modified: Fri, 15 May 2026 21:28:08 GMT  
		Size: 7.1 MB (7146601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe0ae1b6a40e0137963dc8e5df32c4cb676663e3d69805a32c5ced722a1ee4d`  
		Last Modified: Fri, 15 May 2026 21:28:08 GMT  
		Size: 2.5 MB (2538621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cfcfdbea570a6a2289ebf846378c824b64a2e76a344100fc1a08e74f894c17e`  
		Last Modified: Fri, 15 May 2026 21:28:09 GMT  
		Size: 237.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6a094de725c0e71723bfcfe4b6ac037b4820cec2dcf4817a60c15b3ddcc8b0`  
		Last Modified: Fri, 15 May 2026 21:28:09 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b1e2045a50f00d20e64f4a1c554c8b2e7e9c3a0a6ba3adb689371deee07ea9`  
		Last Modified: Fri, 15 May 2026 21:28:26 GMT  
		Size: 217.8 MB (217843268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4eff500584226bd2194677cf653e2a692f24c92d9634fe392afb5e52b4f257`  
		Last Modified: Fri, 15 May 2026 21:28:11 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3093908d2435ec88d7a4c34d5559a30bc0070dad49ee25b3cf7d1e23d11284c5`  
		Last Modified: Fri, 15 May 2026 21:28:11 GMT  
		Size: 662.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc00bf3e2ec4bab76b5ff316c0d6454661ce8d545a8eeeb961df698102f63e5`  
		Last Modified: Fri, 15 May 2026 21:28:13 GMT  
		Size: 922.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d60de70395fe5ee905a6df0b8d3f2d177940edff68908f2a6852fe1854bfa2`  
		Last Modified: Fri, 15 May 2026 21:28:13 GMT  
		Size: 385.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0cdb06324ed000bec482bf04be6a9a395645d920c15fdc28035d95affc5a16`  
		Last Modified: Fri, 15 May 2026 21:28:50 GMT  
		Size: 754.6 MB (754605804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `silverpeas:6.3.6` - unknown; unknown

```console
$ docker pull silverpeas@sha256:af5166f97ad92e3a8893668f37af354f58c2a8ac3b9857d198f42be5be356d8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26867432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a973177e49e1b6302dad87dc1d375b3fb32094e39ce9ccd1727661fd06d43634`

```dockerfile
```

-	Layers:
	-	`sha256:aa424559cf8e92da4085fe928eeef63a35c793297f2efdc6313922ce86238010`  
		Last Modified: Fri, 15 May 2026 21:28:09 GMT  
		Size: 26.8 MB (26826730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:194312fee6bed0315e2fca29054e3aa45104ecf5fe3b8910e915e16803921bd0`  
		Last Modified: Fri, 15 May 2026 21:28:07 GMT  
		Size: 40.7 KB (40702 bytes)  
		MIME: application/vnd.in-toto+json

## `silverpeas:6.4.6`

```console
$ docker pull silverpeas@sha256:482ff63f1ba9c9f1c1f6b9c4a4ca298c25797523e8456bc52426a1a14a28f38a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `silverpeas:6.4.6` - linux; amd64

```console
$ docker pull silverpeas@sha256:43cfa0da236b8a3699b6fa93bed7b30262d0c2ea2945cc51d85849567db24c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818266910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beafe32f10e177b077e919f4ea9211f03401fde1e37aee4bec7c04c551df88cf`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:23:06 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Fri, 15 May 2026 21:23:06 GMT
ENV TERM=xterm
# Fri, 15 May 2026 21:23:06 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends tzdata   && apt-get install -y --no-install-recommends     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f # buildkit
# Fri, 15 May 2026 21:23:08 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 swftools-bin-0.9.2.zip' | sha256sum -c --status -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip # buildkit
# Fri, 15 May 2026 21:23:11 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 pdf2json-bin-0.68.zip' | sha256sum -c --status -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip # buildkit
# Fri, 15 May 2026 21:23:11 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Fri, 15 May 2026 21:23:32 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE} # buildkit
# Fri, 15 May 2026 21:23:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:23:32 GMT
ENV LANGUAGE=en_US.UTF-8
# Fri, 15 May 2026 21:23:32 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 15 May 2026 21:23:32 GMT
ENV PING_ON=1
# Fri, 15 May 2026 21:23:32 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home # buildkit
# Fri, 15 May 2026 21:23:32 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home # buildkit
# Fri, 15 May 2026 21:23:32 GMT
ENV JAVA_HOME=/docker-java-home
# Fri, 15 May 2026 21:23:32 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Fri, 15 May 2026 21:23:32 GMT
ENV JBOSS_HOME=/opt/wildfly
# Fri, 15 May 2026 21:23:32 GMT
ENV SILVERPEAS_VERSION=6.4.6
# Fri, 15 May 2026 21:23:32 GMT
ENV WILDFLY_VERSION=26.1.3
# Fri, 15 May 2026 21:23:32 GMT
LABEL name=Silverpeas 6.4.6 description=Image to install and to run Silverpeas 6.4.6 vendor=Silverpeas version=6.4.6 build=1
# Fri, 15 May 2026 21:24:07 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && wget -nc https://www.silverpeas.org/files/oak-migrate.zip   && echo '87009e55520e74b5d2a386f4ebc843ee43cd1f25ca5138f342a94a31add3cfbd oak-migrate.zip' | sha256sum -c --status -   && mkdir -p /opt/oak-migration   && unzip oak-migrate.zip -d /opt/oak-migration/   && chmod +x /opt/oak-migration/oak-migrate.sh   && rm *.zip   && mkdir -p /root/.m2 # buildkit
# Fri, 15 May 2026 21:24:07 GMT
COPY src/settings.xml /root/.m2/ # buildkit
# Fri, 15 May 2026 21:24:07 GMT
COPY src/silverpeas.gradle /opt/silverpeas/bin/ # buildkit
# Fri, 15 May 2026 21:24:07 GMT
WORKDIR /opt/silverpeas/bin
# Fri, 15 May 2026 21:24:08 GMT
COPY src/run.sh /opt/ # buildkit
# Fri, 15 May 2026 21:24:08 GMT
COPY src/converter.groovy /opt/silverpeas/configuration/silverpeas/ # buildkit
# Fri, 15 May 2026 21:25:29 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN set -eux;   sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle;   echo "Construct Silverpeas ${SILVERPEAS_VERSION}";   ./silverpeas assemble || (cat ../log/build-* && exit 1);   rm ../log/build-*;   touch .install; # buildkit
# Fri, 15 May 2026 21:25:29 GMT
EXPOSE map[8000/tcp:{} 9990/tcp:{}]
# Fri, 15 May 2026 21:25:29 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Fri, 15 May 2026 21:25:29 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42928dbb4e250c4b9f6147317581ff821e9490c7bbd5d1ca24d422363499697`  
		Last Modified: Fri, 15 May 2026 21:27:10 GMT  
		Size: 494.9 MB (494877982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3e97ee7ac0603ee4674b81b65cec8db013c100db21484c9255846846dc8f3b`  
		Last Modified: Fri, 15 May 2026 21:26:51 GMT  
		Size: 4.0 MB (3994008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a181f5fface8e6f09bf68b8ed36d14929381eb83fd5b663b64276edfff8051`  
		Last Modified: Fri, 15 May 2026 21:26:51 GMT  
		Size: 7.1 MB (7146604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ea1ca777abf1c92ea755d1e1c52efa582609f9aa38b2f22400b2faf002cbff`  
		Last Modified: Fri, 15 May 2026 21:26:51 GMT  
		Size: 2.5 MB (2538614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a01880586753b114a1adb5ca94797db30d10e7e40b5f30d8431cb8634b9cb2`  
		Last Modified: Fri, 15 May 2026 21:26:52 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e400aa576d1141da09820e15a1c7aaea3f5290f31c6e83a8f86ea8ddd9ab8263`  
		Last Modified: Fri, 15 May 2026 21:26:53 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ddc7c5286e660cb2213e5e0aab70a64597f26b92f134d4c58d788f8e0500e84`  
		Last Modified: Fri, 15 May 2026 21:27:05 GMT  
		Size: 269.1 MB (269106215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:804e8b53615a4b9c8108cc15c0b7a5caf4a17a278ebf0c454ee4a9cec8008a7b`  
		Last Modified: Fri, 15 May 2026 21:26:54 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd6e53f240b90a9aa8d9167849e1e99cdf6b6fddde4dd3895711afe63dc0f90`  
		Last Modified: Fri, 15 May 2026 21:26:54 GMT  
		Size: 664.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5d75841a2c0b83d0bacfcc747e404c4bea6f99f31c1855dcafcfc0cc66b11e`  
		Last Modified: Fri, 15 May 2026 21:26:55 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6eb5480ed3a8df70f1abd82f6435370e61e9a27177f12a91f88b611f0427a61`  
		Last Modified: Fri, 15 May 2026 21:26:56 GMT  
		Size: 384.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ccba862e439fef52aba62112d0073488ddd9d0f47117d30c6f9a610c240bfb`  
		Last Modified: Fri, 15 May 2026 21:27:25 GMT  
		Size: 1.0 GB (1010863506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `silverpeas:6.4.6` - unknown; unknown

```console
$ docker pull silverpeas@sha256:84bba96fb9eeef5ef85b24a60d8fe0bb7ef319ad6f3ce176f16f8090326cebda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16648843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd80a89e996fbd389b6c5ec22d6fb07cbd4ae5af59404b08d93511e7e507bbcb`

```dockerfile
```

-	Layers:
	-	`sha256:c76c0e15afadd77e9509d822a1c44457e6d9e91d740cac8f4a95fccc57c451a4`  
		Last Modified: Fri, 15 May 2026 21:26:51 GMT  
		Size: 16.6 MB (16606338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:456abc95bfcf9ede9f41ccab1d2110484bb44c4cfe0d387d3672dc17569770c7`  
		Last Modified: Fri, 15 May 2026 21:26:50 GMT  
		Size: 42.5 KB (42505 bytes)  
		MIME: application/vnd.in-toto+json

## `silverpeas:latest`

```console
$ docker pull silverpeas@sha256:482ff63f1ba9c9f1c1f6b9c4a4ca298c25797523e8456bc52426a1a14a28f38a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `silverpeas:latest` - linux; amd64

```console
$ docker pull silverpeas@sha256:43cfa0da236b8a3699b6fa93bed7b30262d0c2ea2945cc51d85849567db24c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818266910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beafe32f10e177b077e919f4ea9211f03401fde1e37aee4bec7c04c551df88cf`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:23:06 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Fri, 15 May 2026 21:23:06 GMT
ENV TERM=xterm
# Fri, 15 May 2026 21:23:06 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends tzdata   && apt-get install -y --no-install-recommends     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f # buildkit
# Fri, 15 May 2026 21:23:08 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 swftools-bin-0.9.2.zip' | sha256sum -c --status -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip # buildkit
# Fri, 15 May 2026 21:23:11 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 pdf2json-bin-0.68.zip' | sha256sum -c --status -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip # buildkit
# Fri, 15 May 2026 21:23:11 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Fri, 15 May 2026 21:23:32 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE} # buildkit
# Fri, 15 May 2026 21:23:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:23:32 GMT
ENV LANGUAGE=en_US.UTF-8
# Fri, 15 May 2026 21:23:32 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 15 May 2026 21:23:32 GMT
ENV PING_ON=1
# Fri, 15 May 2026 21:23:32 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home # buildkit
# Fri, 15 May 2026 21:23:32 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home # buildkit
# Fri, 15 May 2026 21:23:32 GMT
ENV JAVA_HOME=/docker-java-home
# Fri, 15 May 2026 21:23:32 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Fri, 15 May 2026 21:23:32 GMT
ENV JBOSS_HOME=/opt/wildfly
# Fri, 15 May 2026 21:23:32 GMT
ENV SILVERPEAS_VERSION=6.4.6
# Fri, 15 May 2026 21:23:32 GMT
ENV WILDFLY_VERSION=26.1.3
# Fri, 15 May 2026 21:23:32 GMT
LABEL name=Silverpeas 6.4.6 description=Image to install and to run Silverpeas 6.4.6 vendor=Silverpeas version=6.4.6 build=1
# Fri, 15 May 2026 21:24:07 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && wget -nc https://www.silverpeas.org/files/oak-migrate.zip   && echo '87009e55520e74b5d2a386f4ebc843ee43cd1f25ca5138f342a94a31add3cfbd oak-migrate.zip' | sha256sum -c --status -   && mkdir -p /opt/oak-migration   && unzip oak-migrate.zip -d /opt/oak-migration/   && chmod +x /opt/oak-migration/oak-migrate.sh   && rm *.zip   && mkdir -p /root/.m2 # buildkit
# Fri, 15 May 2026 21:24:07 GMT
COPY src/settings.xml /root/.m2/ # buildkit
# Fri, 15 May 2026 21:24:07 GMT
COPY src/silverpeas.gradle /opt/silverpeas/bin/ # buildkit
# Fri, 15 May 2026 21:24:07 GMT
WORKDIR /opt/silverpeas/bin
# Fri, 15 May 2026 21:24:08 GMT
COPY src/run.sh /opt/ # buildkit
# Fri, 15 May 2026 21:24:08 GMT
COPY src/converter.groovy /opt/silverpeas/configuration/silverpeas/ # buildkit
# Fri, 15 May 2026 21:25:29 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN set -eux;   sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle;   echo "Construct Silverpeas ${SILVERPEAS_VERSION}";   ./silverpeas assemble || (cat ../log/build-* && exit 1);   rm ../log/build-*;   touch .install; # buildkit
# Fri, 15 May 2026 21:25:29 GMT
EXPOSE map[8000/tcp:{} 9990/tcp:{}]
# Fri, 15 May 2026 21:25:29 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Fri, 15 May 2026 21:25:29 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42928dbb4e250c4b9f6147317581ff821e9490c7bbd5d1ca24d422363499697`  
		Last Modified: Fri, 15 May 2026 21:27:10 GMT  
		Size: 494.9 MB (494877982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3e97ee7ac0603ee4674b81b65cec8db013c100db21484c9255846846dc8f3b`  
		Last Modified: Fri, 15 May 2026 21:26:51 GMT  
		Size: 4.0 MB (3994008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a181f5fface8e6f09bf68b8ed36d14929381eb83fd5b663b64276edfff8051`  
		Last Modified: Fri, 15 May 2026 21:26:51 GMT  
		Size: 7.1 MB (7146604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ea1ca777abf1c92ea755d1e1c52efa582609f9aa38b2f22400b2faf002cbff`  
		Last Modified: Fri, 15 May 2026 21:26:51 GMT  
		Size: 2.5 MB (2538614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a01880586753b114a1adb5ca94797db30d10e7e40b5f30d8431cb8634b9cb2`  
		Last Modified: Fri, 15 May 2026 21:26:52 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e400aa576d1141da09820e15a1c7aaea3f5290f31c6e83a8f86ea8ddd9ab8263`  
		Last Modified: Fri, 15 May 2026 21:26:53 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ddc7c5286e660cb2213e5e0aab70a64597f26b92f134d4c58d788f8e0500e84`  
		Last Modified: Fri, 15 May 2026 21:27:05 GMT  
		Size: 269.1 MB (269106215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:804e8b53615a4b9c8108cc15c0b7a5caf4a17a278ebf0c454ee4a9cec8008a7b`  
		Last Modified: Fri, 15 May 2026 21:26:54 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd6e53f240b90a9aa8d9167849e1e99cdf6b6fddde4dd3895711afe63dc0f90`  
		Last Modified: Fri, 15 May 2026 21:26:54 GMT  
		Size: 664.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5d75841a2c0b83d0bacfcc747e404c4bea6f99f31c1855dcafcfc0cc66b11e`  
		Last Modified: Fri, 15 May 2026 21:26:55 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6eb5480ed3a8df70f1abd82f6435370e61e9a27177f12a91f88b611f0427a61`  
		Last Modified: Fri, 15 May 2026 21:26:56 GMT  
		Size: 384.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ccba862e439fef52aba62112d0073488ddd9d0f47117d30c6f9a610c240bfb`  
		Last Modified: Fri, 15 May 2026 21:27:25 GMT  
		Size: 1.0 GB (1010863506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `silverpeas:latest` - unknown; unknown

```console
$ docker pull silverpeas@sha256:84bba96fb9eeef5ef85b24a60d8fe0bb7ef319ad6f3ce176f16f8090326cebda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16648843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd80a89e996fbd389b6c5ec22d6fb07cbd4ae5af59404b08d93511e7e507bbcb`

```dockerfile
```

-	Layers:
	-	`sha256:c76c0e15afadd77e9509d822a1c44457e6d9e91d740cac8f4a95fccc57c451a4`  
		Last Modified: Fri, 15 May 2026 21:26:51 GMT  
		Size: 16.6 MB (16606338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:456abc95bfcf9ede9f41ccab1d2110484bb44c4cfe0d387d3672dc17569770c7`  
		Last Modified: Fri, 15 May 2026 21:26:50 GMT  
		Size: 42.5 KB (42505 bytes)  
		MIME: application/vnd.in-toto+json
