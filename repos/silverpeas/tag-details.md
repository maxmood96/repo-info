<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `silverpeas`

-	[`silverpeas:6.3.5`](#silverpeas635)
-	[`silverpeas:6.4.2`](#silverpeas642)
-	[`silverpeas:latest`](#silverpeaslatest)

## `silverpeas:6.3.5`

```console
$ docker pull silverpeas@sha256:41d2fcc6d6fd1fb137cb18787ab1f191e5ba561441664fb5c3fc06c7aacbba6c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `silverpeas:6.3.5` - linux; amd64

```console
$ docker pull silverpeas@sha256:88f69207fd6f5cf20335a8ba9c81c8898a7f945ec1d9504971988507078c070a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1776184712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2ded0d1ebd1c9efe00d0b87b7e75b52491ff29c28b0c9d4ae23af17caaee420`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Tue, 28 May 2024 07:33:18 GMT
ARG RELEASE
# Tue, 28 May 2024 07:33:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 May 2024 07:33:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 May 2024 07:33:18 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 28 May 2024 07:33:18 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Tue, 28 May 2024 07:33:18 GMT
CMD ["/bin/bash"]
# Tue, 28 May 2024 07:33:18 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Tue, 28 May 2024 07:33:18 GMT
ENV TERM=xterm
# Tue, 28 May 2024 07:33:18 GMT
RUN apt-get update   && apt-get install -y tzdata   && apt-get install -y     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f # buildkit
# Tue, 28 May 2024 07:33:18 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip # buildkit
# Tue, 28 May 2024 07:33:18 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip # buildkit
# Tue, 28 May 2024 07:33:18 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Tue, 28 May 2024 07:33:18 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE} # buildkit
# Tue, 28 May 2024 07:33:18 GMT
ENV LANG=en_US.UTF-8
# Tue, 28 May 2024 07:33:18 GMT
ENV LANGUAGE=en_US.UTF-8
# Tue, 28 May 2024 07:33:18 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 28 May 2024 07:33:18 GMT
ENV PING_ON=1
# Tue, 28 May 2024 07:33:18 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home # buildkit
# Tue, 28 May 2024 07:33:18 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home # buildkit
# Tue, 28 May 2024 07:33:18 GMT
ENV JAVA_HOME=/docker-java-home
# Tue, 28 May 2024 07:33:18 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Tue, 28 May 2024 07:33:18 GMT
ENV JBOSS_HOME=/opt/wildfly
# Tue, 28 May 2024 07:33:18 GMT
ENV SILVERPEAS_VERSION=6.3.5
# Tue, 28 May 2024 07:33:18 GMT
ENV WILDFLY_VERSION=26.1.1
# Tue, 28 May 2024 07:33:18 GMT
LABEL name=Silverpeas 6.3.5 description=Image to install and to run Silverpeas 6.3.5 vendor=Silverpeas version=6.3.5 build=1
# Tue, 28 May 2024 07:33:18 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2 # buildkit
# Tue, 28 May 2024 07:33:18 GMT
COPY src/settings.xml /root/.m2/ # buildkit
# Tue, 28 May 2024 07:33:18 GMT
COPY src/silverpeas.gradle /opt/silverpeas/bin/ # buildkit
# Tue, 28 May 2024 07:33:18 GMT
WORKDIR /opt/silverpeas/bin
# Tue, 28 May 2024 07:33:18 GMT
COPY src/run.sh /opt/ # buildkit
# Tue, 28 May 2024 07:33:18 GMT
COPY src/converter.groovy /opt/silverpeas/configuration/silverpeas/ # buildkit
# Tue, 28 May 2024 07:33:18 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle   && ./silverpeas construct   && rm ../log/build-*   && touch .install # buildkit
# Tue, 28 May 2024 07:33:18 GMT
EXPOSE map[8000/tcp:{} 9990/tcp:{}]
# Tue, 28 May 2024 07:33:18 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Tue, 28 May 2024 07:33:18 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 13 Dec 2024 13:08:34 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591db78ce1339018ea3bbcf310157b9f7e1fe6757906e5173b73291f1701c68e`  
		Last Modified: Tue, 07 Jan 2025 03:55:43 GMT  
		Size: 762.6 MB (762557289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3b6f4fce89b6a112d5a4be574efb4b822140914fd0e4d6872c0765f7f355ca`  
		Last Modified: Mon, 06 Jan 2025 18:03:17 GMT  
		Size: 4.0 MB (3994017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f789a0de6954641b9dc75bfdd90e275d79c184a15a7c8bbe6568e9c6e02778d2`  
		Last Modified: Tue, 07 Jan 2025 01:01:46 GMT  
		Size: 7.1 MB (7146602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493a7cc60281649899722e95a35d7a815f887e688220fe5b5d9bcc764d8d63bf`  
		Last Modified: Wed, 08 Jan 2025 03:56:31 GMT  
		Size: 2.5 MB (2534369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2275153831ef74056cfe492e220e37d6cde06d87f8d65a0fe65870c3bd6c192c`  
		Last Modified: Mon, 06 Jan 2025 23:04:38 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673b20165884fb640a0a2972939d3a7fd9e86ffe3f7c8e03a3a4a2b83472eece`  
		Last Modified: Mon, 06 Jan 2025 18:03:18 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ef4a8632125bf90670f1dd7b2812017a7f2d41b27f4b32ab515be819a9868b`  
		Last Modified: Mon, 06 Jan 2025 20:06:55 GMT  
		Size: 217.8 MB (217843300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:507c18988c03f7399ccb77ce02f8bb16276afc863cbb4f478c87d805cab6ed39`  
		Last Modified: Mon, 06 Jan 2025 23:04:39 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8ac9f5552bc7450d6581855c94158dd37f2a453807b6704ef87865f52127c5`  
		Last Modified: Tue, 07 Jan 2025 02:57:26 GMT  
		Size: 660.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ded2d570306e08f4c673909ef4ccadf03463032481979336d46fe659e988e2`  
		Last Modified: Tue, 07 Jan 2025 06:52:39 GMT  
		Size: 921.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f300fbf46a33d2335fa852f886a489fc63a5bc36c072c33fb9584732fe796639`  
		Last Modified: Mon, 06 Jan 2025 20:06:47 GMT  
		Size: 384.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ccd4814c6ac5c9cf7b05d6280011b1a53fa1d62f043bd84dd7d887416d895e`  
		Last Modified: Sat, 19 Oct 2024 02:17:35 GMT  
		Size: 754.6 MB (754595307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `silverpeas:6.3.5` - unknown; unknown

```console
$ docker pull silverpeas@sha256:732097e849a0ca210f98aee224b294987759ad294575867328d754de6c1c74a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.8 MB (27820802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a28f2d368e49744331ca2f6a553a3446638c9a59a83edb6431c9aa1d34a59b43`

```dockerfile
```

-	Layers:
	-	`sha256:870bd78caebc99bfd1f2913dd585031155b9b5f5d55f91f5dc518aea274b4c15`  
		Last Modified: Tue, 07 Jan 2025 21:00:51 GMT  
		Size: 27.8 MB (27780060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caad95269c98c29ca14395dd36abc5176c7de132a14b2dd0990dd176f0e19e7f`  
		Last Modified: Mon, 06 Jan 2025 23:04:41 GMT  
		Size: 40.7 KB (40742 bytes)  
		MIME: application/vnd.in-toto+json

## `silverpeas:6.4.2`

```console
$ docker pull silverpeas@sha256:fe8bb912175dd366342995e7da1594f4aa1d05be44432d36927f80ffce4b849f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `silverpeas:6.4.2` - linux; amd64

```console
$ docker pull silverpeas@sha256:deebabc927fd2cdde90dd45eb277d30458c0d9932cb769b40e8ce8914c4da5f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1798652075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff004f06ab4716f57e11f1568bd886b7d0da001bb23e9e8ed34d319a50402ca`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Thu, 12 Dec 2024 09:44:16 GMT
ARG RELEASE
# Thu, 12 Dec 2024 09:44:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 12 Dec 2024 09:44:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 12 Dec 2024 09:44:16 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 12 Dec 2024 09:44:16 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Thu, 12 Dec 2024 09:44:16 GMT
CMD ["/bin/bash"]
# Thu, 12 Dec 2024 09:44:16 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Thu, 12 Dec 2024 09:44:16 GMT
ENV TERM=xterm
# Thu, 12 Dec 2024 09:44:16 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends tzdata   && apt-get install -y --no-install-recommends     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f # buildkit
# Thu, 12 Dec 2024 09:44:16 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 swftools-bin-0.9.2.zip' | sha256sum -c --status -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip # buildkit
# Thu, 12 Dec 2024 09:44:16 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 pdf2json-bin-0.68.zip' | sha256sum -c --status -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip # buildkit
# Thu, 12 Dec 2024 09:44:16 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Thu, 12 Dec 2024 09:44:16 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE} # buildkit
# Thu, 12 Dec 2024 09:44:16 GMT
ENV LANG=en_US.UTF-8
# Thu, 12 Dec 2024 09:44:16 GMT
ENV LANGUAGE=en_US.UTF-8
# Thu, 12 Dec 2024 09:44:16 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 12 Dec 2024 09:44:16 GMT
ENV PING_ON=1
# Thu, 12 Dec 2024 09:44:16 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home # buildkit
# Thu, 12 Dec 2024 09:44:16 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home # buildkit
# Thu, 12 Dec 2024 09:44:16 GMT
ENV JAVA_HOME=/docker-java-home
# Thu, 12 Dec 2024 09:44:16 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Thu, 12 Dec 2024 09:44:16 GMT
ENV JBOSS_HOME=/opt/wildfly
# Thu, 12 Dec 2024 09:44:16 GMT
ENV SILVERPEAS_VERSION=6.4.2
# Thu, 12 Dec 2024 09:44:16 GMT
ENV WILDFLY_VERSION=26.1.3
# Thu, 12 Dec 2024 09:44:16 GMT
LABEL name=Silverpeas 6.4.2 description=Image to install and to run Silverpeas 6.4.2 vendor=Silverpeas version=6.4.2 build=1
# Thu, 12 Dec 2024 09:44:16 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && wget -nc https://www.silverpeas.org/files/oak-migrate.zip   && echo '87009e55520e74b5d2a386f4ebc843ee43cd1f25ca5138f342a94a31add3cfbd oak-migrate.zip' | sha256sum -c --status -   && mkdir -p /opt/oak-migration   && unzip oak-migrate.zip -d /opt/oak-migration/   && chmod +x /opt/oak-migration/oak-migrate.sh   && rm *.zip   && mkdir -p /root/.m2 # buildkit
# Thu, 12 Dec 2024 09:44:16 GMT
COPY src/settings.xml /root/.m2/ # buildkit
# Thu, 12 Dec 2024 09:44:16 GMT
COPY src/silverpeas.gradle /opt/silverpeas/bin/ # buildkit
# Thu, 12 Dec 2024 09:44:16 GMT
WORKDIR /opt/silverpeas/bin
# Thu, 12 Dec 2024 09:44:16 GMT
COPY src/run.sh /opt/ # buildkit
# Thu, 12 Dec 2024 09:44:16 GMT
COPY src/converter.groovy /opt/silverpeas/configuration/silverpeas/ # buildkit
# Thu, 12 Dec 2024 09:44:16 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN set -eux;   sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle;   echo "Construct Silverpeas ${SILVERPEAS_VERSION}";   ./silverpeas assemble || (cat ../log/build-* && exit 1);   rm ../log/build-*;   touch .install; # buildkit
# Thu, 12 Dec 2024 09:44:16 GMT
EXPOSE map[8000/tcp:{} 9990/tcp:{}]
# Thu, 12 Dec 2024 09:44:16 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Thu, 12 Dec 2024 09:44:16 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc9ed91f74449fa0290f7e9d642ea142eb1226b965254e99f0461afdecfaec6`  
		Last Modified: Wed, 05 Feb 2025 03:12:48 GMT  
		Size: 495.0 MB (494955226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f44bc2bbae2e96aa81a75c76b1a75b631e3385bb4c23a19c44fad3a9592a4e7`  
		Last Modified: Wed, 05 Feb 2025 18:10:35 GMT  
		Size: 4.0 MB (3994012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df61e8858c56239bdfccd8bc1f92beadb17bde2b87fc085a37f1bb4dcb342c5`  
		Last Modified: Fri, 07 Feb 2025 15:23:17 GMT  
		Size: 7.1 MB (7146623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96f0938379fac27d9fd0b2e888a7cff87185f078c45ca485593a5f32fa3ac3a`  
		Last Modified: Tue, 04 Feb 2025 16:17:47 GMT  
		Size: 2.5 MB (2538616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a59da64f4f1e85f316a3e752714d6db202947944426d56ffa009d48e79cd30`  
		Last Modified: Fri, 07 Feb 2025 17:55:02 GMT  
		Size: 236.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af52e85ddbedfbc4f410b2b7829a7f3a46be6716253ddbad862af76873adafa5`  
		Last Modified: Wed, 05 Feb 2025 18:10:39 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57770674239d6c2d99423ee776dd3854e39de62774ea656702bde6296cf6436a`  
		Last Modified: Wed, 05 Feb 2025 18:11:01 GMT  
		Size: 269.1 MB (269106231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1d348d999728c54cdd7e84f9eb7c2d882ec0cf92441de1b1a0eb6e4beabf74`  
		Last Modified: Fri, 07 Feb 2025 18:14:31 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6b75ad1dd45cf8e1d2a963a396a26c85ec9040cd0e4d7a0687bb62ce94524d`  
		Last Modified: Wed, 05 Feb 2025 03:12:35 GMT  
		Size: 664.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a59219dadd75db9ae61f85b5c3bda99316d23a15fbe51a72ac9bf4c77cbf06`  
		Last Modified: Fri, 07 Feb 2025 15:23:23 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f55bd20299332160273e411f11965766ac9e61ee5d1dd7916e5459d28459445`  
		Last Modified: Wed, 05 Feb 2025 18:10:40 GMT  
		Size: 385.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51dc44d95438403c0c2757e005383685e48289c243ab8b1045459ebabfb7cb5`  
		Last Modified: Sat, 08 Feb 2025 22:05:57 GMT  
		Size: 991.4 MB (991372132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `silverpeas:6.4.2` - unknown; unknown

```console
$ docker pull silverpeas@sha256:4009e2a90a4bd95a0c6b08bc46332516a6cd930961d1bc12c007f9cc9882b6fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15711366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f3aa4eb4ccd134ac4a90e3cbb1f953780bc74c29e86009b4ec2f2653e0e7a3`

```dockerfile
```

-	Layers:
	-	`sha256:d7f07185d038b7401f87837e09203ca91d4e1044d47c7a9be3166ce145120688`  
		Last Modified: Mon, 10 Feb 2025 19:18:07 GMT  
		Size: 15.7 MB (15668818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bcf6e56cbbb28b19a694d96e63a356c191de21a566ad1a83926a36499638b7a`  
		Last Modified: Fri, 21 Feb 2025 18:30:14 GMT  
		Size: 42.5 KB (42548 bytes)  
		MIME: application/vnd.in-toto+json

## `silverpeas:latest`

```console
$ docker pull silverpeas@sha256:fe8bb912175dd366342995e7da1594f4aa1d05be44432d36927f80ffce4b849f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `silverpeas:latest` - linux; amd64

```console
$ docker pull silverpeas@sha256:deebabc927fd2cdde90dd45eb277d30458c0d9932cb769b40e8ce8914c4da5f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1798652075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff004f06ab4716f57e11f1568bd886b7d0da001bb23e9e8ed34d319a50402ca`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Thu, 12 Dec 2024 09:44:16 GMT
ARG RELEASE
# Thu, 12 Dec 2024 09:44:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 12 Dec 2024 09:44:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 12 Dec 2024 09:44:16 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 12 Dec 2024 09:44:16 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Thu, 12 Dec 2024 09:44:16 GMT
CMD ["/bin/bash"]
# Thu, 12 Dec 2024 09:44:16 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Thu, 12 Dec 2024 09:44:16 GMT
ENV TERM=xterm
# Thu, 12 Dec 2024 09:44:16 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends tzdata   && apt-get install -y --no-install-recommends     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f # buildkit
# Thu, 12 Dec 2024 09:44:16 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 swftools-bin-0.9.2.zip' | sha256sum -c --status -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip # buildkit
# Thu, 12 Dec 2024 09:44:16 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 pdf2json-bin-0.68.zip' | sha256sum -c --status -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip # buildkit
# Thu, 12 Dec 2024 09:44:16 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Thu, 12 Dec 2024 09:44:16 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE} # buildkit
# Thu, 12 Dec 2024 09:44:16 GMT
ENV LANG=en_US.UTF-8
# Thu, 12 Dec 2024 09:44:16 GMT
ENV LANGUAGE=en_US.UTF-8
# Thu, 12 Dec 2024 09:44:16 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 12 Dec 2024 09:44:16 GMT
ENV PING_ON=1
# Thu, 12 Dec 2024 09:44:16 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home # buildkit
# Thu, 12 Dec 2024 09:44:16 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home # buildkit
# Thu, 12 Dec 2024 09:44:16 GMT
ENV JAVA_HOME=/docker-java-home
# Thu, 12 Dec 2024 09:44:16 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Thu, 12 Dec 2024 09:44:16 GMT
ENV JBOSS_HOME=/opt/wildfly
# Thu, 12 Dec 2024 09:44:16 GMT
ENV SILVERPEAS_VERSION=6.4.2
# Thu, 12 Dec 2024 09:44:16 GMT
ENV WILDFLY_VERSION=26.1.3
# Thu, 12 Dec 2024 09:44:16 GMT
LABEL name=Silverpeas 6.4.2 description=Image to install and to run Silverpeas 6.4.2 vendor=Silverpeas version=6.4.2 build=1
# Thu, 12 Dec 2024 09:44:16 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && wget -nc https://www.silverpeas.org/files/oak-migrate.zip   && echo '87009e55520e74b5d2a386f4ebc843ee43cd1f25ca5138f342a94a31add3cfbd oak-migrate.zip' | sha256sum -c --status -   && mkdir -p /opt/oak-migration   && unzip oak-migrate.zip -d /opt/oak-migration/   && chmod +x /opt/oak-migration/oak-migrate.sh   && rm *.zip   && mkdir -p /root/.m2 # buildkit
# Thu, 12 Dec 2024 09:44:16 GMT
COPY src/settings.xml /root/.m2/ # buildkit
# Thu, 12 Dec 2024 09:44:16 GMT
COPY src/silverpeas.gradle /opt/silverpeas/bin/ # buildkit
# Thu, 12 Dec 2024 09:44:16 GMT
WORKDIR /opt/silverpeas/bin
# Thu, 12 Dec 2024 09:44:16 GMT
COPY src/run.sh /opt/ # buildkit
# Thu, 12 Dec 2024 09:44:16 GMT
COPY src/converter.groovy /opt/silverpeas/configuration/silverpeas/ # buildkit
# Thu, 12 Dec 2024 09:44:16 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN set -eux;   sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle;   echo "Construct Silverpeas ${SILVERPEAS_VERSION}";   ./silverpeas assemble || (cat ../log/build-* && exit 1);   rm ../log/build-*;   touch .install; # buildkit
# Thu, 12 Dec 2024 09:44:16 GMT
EXPOSE map[8000/tcp:{} 9990/tcp:{}]
# Thu, 12 Dec 2024 09:44:16 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Thu, 12 Dec 2024 09:44:16 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc9ed91f74449fa0290f7e9d642ea142eb1226b965254e99f0461afdecfaec6`  
		Last Modified: Wed, 05 Feb 2025 03:12:48 GMT  
		Size: 495.0 MB (494955226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f44bc2bbae2e96aa81a75c76b1a75b631e3385bb4c23a19c44fad3a9592a4e7`  
		Last Modified: Wed, 05 Feb 2025 18:10:35 GMT  
		Size: 4.0 MB (3994012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df61e8858c56239bdfccd8bc1f92beadb17bde2b87fc085a37f1bb4dcb342c5`  
		Last Modified: Fri, 07 Feb 2025 15:23:17 GMT  
		Size: 7.1 MB (7146623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96f0938379fac27d9fd0b2e888a7cff87185f078c45ca485593a5f32fa3ac3a`  
		Last Modified: Tue, 04 Feb 2025 16:17:47 GMT  
		Size: 2.5 MB (2538616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a59da64f4f1e85f316a3e752714d6db202947944426d56ffa009d48e79cd30`  
		Last Modified: Fri, 07 Feb 2025 17:55:02 GMT  
		Size: 236.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af52e85ddbedfbc4f410b2b7829a7f3a46be6716253ddbad862af76873adafa5`  
		Last Modified: Wed, 05 Feb 2025 18:10:39 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57770674239d6c2d99423ee776dd3854e39de62774ea656702bde6296cf6436a`  
		Last Modified: Wed, 05 Feb 2025 18:11:01 GMT  
		Size: 269.1 MB (269106231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1d348d999728c54cdd7e84f9eb7c2d882ec0cf92441de1b1a0eb6e4beabf74`  
		Last Modified: Fri, 07 Feb 2025 18:14:31 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6b75ad1dd45cf8e1d2a963a396a26c85ec9040cd0e4d7a0687bb62ce94524d`  
		Last Modified: Wed, 05 Feb 2025 03:12:35 GMT  
		Size: 664.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a59219dadd75db9ae61f85b5c3bda99316d23a15fbe51a72ac9bf4c77cbf06`  
		Last Modified: Fri, 07 Feb 2025 15:23:23 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f55bd20299332160273e411f11965766ac9e61ee5d1dd7916e5459d28459445`  
		Last Modified: Wed, 05 Feb 2025 18:10:40 GMT  
		Size: 385.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51dc44d95438403c0c2757e005383685e48289c243ab8b1045459ebabfb7cb5`  
		Last Modified: Sat, 08 Feb 2025 22:05:57 GMT  
		Size: 991.4 MB (991372132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `silverpeas:latest` - unknown; unknown

```console
$ docker pull silverpeas@sha256:4009e2a90a4bd95a0c6b08bc46332516a6cd930961d1bc12c007f9cc9882b6fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15711366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f3aa4eb4ccd134ac4a90e3cbb1f953780bc74c29e86009b4ec2f2653e0e7a3`

```dockerfile
```

-	Layers:
	-	`sha256:d7f07185d038b7401f87837e09203ca91d4e1044d47c7a9be3166ce145120688`  
		Last Modified: Mon, 10 Feb 2025 19:18:07 GMT  
		Size: 15.7 MB (15668818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bcf6e56cbbb28b19a694d96e63a356c191de21a566ad1a83926a36499638b7a`  
		Last Modified: Fri, 21 Feb 2025 18:30:14 GMT  
		Size: 42.5 KB (42548 bytes)  
		MIME: application/vnd.in-toto+json
