<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `silverpeas`

-	[`silverpeas:6.3.5`](#silverpeas635)
-	[`silverpeas:6.4.2`](#silverpeas642)
-	[`silverpeas:latest`](#silverpeaslatest)

## `silverpeas:6.3.5`

```console
$ docker pull silverpeas@sha256:44f7dd0c2f533aae92a3a8efe2514755ebdda29bd5a77aa20fe4c87c39741fb8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `silverpeas:6.3.5` - linux; amd64

```console
$ docker pull silverpeas@sha256:8f1c11f3ff6ccc66fa7a9bc311d511237d95a3bcd1795a12c7113aeb1ba0f3f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1776283483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8e7c4aaccae4ebbc9d2fdaf4a41f607c10dfc9995f6fb38a111d9a78f9a25fb`
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
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
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
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bad73964efc16cb51a48d87293a267e715b5e1010665a1e65d86615b8bec5a0`  
		Last Modified: Wed, 09 Apr 2025 01:28:55 GMT  
		Size: 762.6 MB (762648167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08245978d6e1d945b91b10c359415cc5c0a68a620e52a9d3278a25d3008163a2`  
		Last Modified: Wed, 09 Apr 2025 01:28:36 GMT  
		Size: 4.0 MB (3994011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6668f3b30fea667ec860fcf5b3eea4bd39e35f3c7955e1a13fc2db93593147`  
		Last Modified: Wed, 09 Apr 2025 01:28:36 GMT  
		Size: 7.1 MB (7146622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2728234f576b93b3168c2cc527dab85af813b27897b0f27851eff956387d50dc`  
		Last Modified: Wed, 09 Apr 2025 01:28:36 GMT  
		Size: 2.5 MB (2534369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a206050e8ea1a3e8debbe59447dc923d2566347d1573e53f6ead22c8c134c91b`  
		Last Modified: Wed, 09 Apr 2025 01:28:38 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37723d51955c7bfdd86dd00398d20243bc0c21650776cb6bd60b2375a125efcc`  
		Last Modified: Wed, 09 Apr 2025 01:28:38 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592c97e1373ef0fe127ec0cef2f74a1a5e0315a2a50827351390575d5991e946`  
		Last Modified: Wed, 09 Apr 2025 01:28:43 GMT  
		Size: 217.8 MB (217843236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca32f8c1d513287ed611296cebcf9e5f17a575930f58586a59339d7afd58698f`  
		Last Modified: Wed, 09 Apr 2025 01:28:39 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ada503c44304823da79a77796297fe79956b48db0525fbb4e1d50aaca2111b`  
		Last Modified: Wed, 09 Apr 2025 01:28:39 GMT  
		Size: 661.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b73747c1a3918fd83f131f34937b3782f5dfda7b79c343057aa4533bc5c8c2df`  
		Last Modified: Wed, 09 Apr 2025 01:28:40 GMT  
		Size: 922.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b104f65456df29eba47029a6ef022e83c1981360e50824d3f8ddcbd423c98c`  
		Last Modified: Wed, 09 Apr 2025 01:28:40 GMT  
		Size: 383.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ab1eff1a02b1cd39a3b132f7162acc9ab1749b5b3c0cb51aecd55d31fa1630`  
		Last Modified: Wed, 09 Apr 2025 01:29:02 GMT  
		Size: 754.6 MB (754603914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `silverpeas:6.3.5` - unknown; unknown

```console
$ docker pull silverpeas@sha256:ad4cb1e7bc2b4c5bc07169c88c3f6e551af9ed6a4c38786062a2b9423cccc854
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.8 MB (27780882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae9ad858efae94e0b317944e09b2fbb8e79a4a16ad9710b0d436704dc89acffe`

```dockerfile
```

-	Layers:
	-	`sha256:d0f31e104cfa536d3f725e36f373c587eaec055cd050d958436bc1aceb81de9d`  
		Last Modified: Wed, 09 Apr 2025 01:28:37 GMT  
		Size: 27.7 MB (27740138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0b45e65309f5242388fc31e872f02706cc55a565254eb0cad460b323e503d59`  
		Last Modified: Wed, 09 Apr 2025 01:28:36 GMT  
		Size: 40.7 KB (40744 bytes)  
		MIME: application/vnd.in-toto+json

## `silverpeas:6.4.2`

```console
$ docker pull silverpeas@sha256:f00a1a4a1dbffcb046074e0a4faacb5a291c1b551868b35e6a0e1846210fe113
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `silverpeas:6.4.2` - linux; amd64

```console
$ docker pull silverpeas@sha256:a6fc619cf100d3fb419fd4424ef4b08cbb354aa9669d6065a44801e8af552bb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1798409171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2926376090c6d3eda48ac73916e313d305d07b9b532de7564aa3b13ff9f7b0dc`
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
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69892df9335f50005361ed235a5737cd80a2765c090b627a7e4ba78e152514a`  
		Last Modified: Wed, 09 Apr 2025 01:28:24 GMT  
		Size: 494.7 MB (494713695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de0e0c160f426077eda111529829a272da3f6d7a4e774ee8ad987b113d4d927`  
		Last Modified: Wed, 09 Apr 2025 01:28:10 GMT  
		Size: 4.0 MB (3994011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4882bf4d6c1aee1c343951aa6653a2d1c38bfd251ae97ebd39ff2fe18c5673d7`  
		Last Modified: Wed, 09 Apr 2025 01:28:10 GMT  
		Size: 7.1 MB (7146616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0867385fb639ae06fb0eebd8689b76feffb4a315b594a064b5fd70637cd18d3`  
		Last Modified: Wed, 09 Apr 2025 01:28:10 GMT  
		Size: 2.5 MB (2538615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619eac8c35b50aa71d131896ff15767e93e7aac5dae7b5894530638c6098f629`  
		Last Modified: Wed, 09 Apr 2025 01:28:11 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1219235dd4327fe6669728d5ad9c4b1277cbf8159a3b95c5a3cb309b0c5922a6`  
		Last Modified: Wed, 09 Apr 2025 01:28:11 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4985a2dcffd837d5215bbe7edb743cdb3df9e6230d51598f124e2d71bab17ae7`  
		Last Modified: Wed, 09 Apr 2025 01:28:18 GMT  
		Size: 269.1 MB (269106221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11f1e2f8e8003876768582ace81e08821868c5a45c552bd5d68b40e5b4ec7b6`  
		Last Modified: Wed, 09 Apr 2025 01:28:12 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836cb3299bd42b940a5beadb01cf3fd46d38776bff0bcb8ee4dabeb1a630bf35`  
		Last Modified: Wed, 09 Apr 2025 01:28:12 GMT  
		Size: 664.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f4052f236300064d6c8260931f3c758428845c92e96efd45f8f31292c8e5c3`  
		Last Modified: Wed, 09 Apr 2025 01:28:13 GMT  
		Size: 1.4 KB (1450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36941b364f8e9cfcc0876976d093a17641ad06eddbd685749a8fd4793c9137e2`  
		Last Modified: Wed, 09 Apr 2025 01:28:14 GMT  
		Size: 384.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05cca22a1f19eeb1b73efa2be48c142e0ccaa76fb105196b36624316a16eb9c5`  
		Last Modified: Wed, 09 Apr 2025 01:28:41 GMT  
		Size: 991.4 MB (991374348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `silverpeas:6.4.2` - unknown; unknown

```console
$ docker pull silverpeas@sha256:88161579dd526aa4e1b5a70685a58c6687e8a2e5cdb07af18b7d73d67538575c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15714245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0286863b4ec537d101938bef1f1e4ff5512c5c9cf8dda0a5ff5b376336e63f72`

```dockerfile
```

-	Layers:
	-	`sha256:299287ec3a8ed7dd28bc4e84e4453e27a9a5143b26b0c26c54c0b29c8e0c8233`  
		Last Modified: Wed, 09 Apr 2025 01:28:11 GMT  
		Size: 15.7 MB (15671698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d7c5703b08ec2cc4a8760bbf67a2666f1e53676d3e166a7d05d4070a81961ba`  
		Last Modified: Wed, 09 Apr 2025 01:28:10 GMT  
		Size: 42.5 KB (42547 bytes)  
		MIME: application/vnd.in-toto+json

## `silverpeas:latest`

```console
$ docker pull silverpeas@sha256:f00a1a4a1dbffcb046074e0a4faacb5a291c1b551868b35e6a0e1846210fe113
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `silverpeas:latest` - linux; amd64

```console
$ docker pull silverpeas@sha256:a6fc619cf100d3fb419fd4424ef4b08cbb354aa9669d6065a44801e8af552bb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1798409171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2926376090c6d3eda48ac73916e313d305d07b9b532de7564aa3b13ff9f7b0dc`
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
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69892df9335f50005361ed235a5737cd80a2765c090b627a7e4ba78e152514a`  
		Last Modified: Wed, 09 Apr 2025 01:28:24 GMT  
		Size: 494.7 MB (494713695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de0e0c160f426077eda111529829a272da3f6d7a4e774ee8ad987b113d4d927`  
		Last Modified: Wed, 09 Apr 2025 01:28:10 GMT  
		Size: 4.0 MB (3994011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4882bf4d6c1aee1c343951aa6653a2d1c38bfd251ae97ebd39ff2fe18c5673d7`  
		Last Modified: Wed, 09 Apr 2025 01:28:10 GMT  
		Size: 7.1 MB (7146616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0867385fb639ae06fb0eebd8689b76feffb4a315b594a064b5fd70637cd18d3`  
		Last Modified: Wed, 09 Apr 2025 01:28:10 GMT  
		Size: 2.5 MB (2538615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619eac8c35b50aa71d131896ff15767e93e7aac5dae7b5894530638c6098f629`  
		Last Modified: Wed, 09 Apr 2025 01:28:11 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1219235dd4327fe6669728d5ad9c4b1277cbf8159a3b95c5a3cb309b0c5922a6`  
		Last Modified: Wed, 09 Apr 2025 01:28:11 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4985a2dcffd837d5215bbe7edb743cdb3df9e6230d51598f124e2d71bab17ae7`  
		Last Modified: Wed, 09 Apr 2025 01:28:18 GMT  
		Size: 269.1 MB (269106221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11f1e2f8e8003876768582ace81e08821868c5a45c552bd5d68b40e5b4ec7b6`  
		Last Modified: Wed, 09 Apr 2025 01:28:12 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836cb3299bd42b940a5beadb01cf3fd46d38776bff0bcb8ee4dabeb1a630bf35`  
		Last Modified: Wed, 09 Apr 2025 01:28:12 GMT  
		Size: 664.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f4052f236300064d6c8260931f3c758428845c92e96efd45f8f31292c8e5c3`  
		Last Modified: Wed, 09 Apr 2025 01:28:13 GMT  
		Size: 1.4 KB (1450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36941b364f8e9cfcc0876976d093a17641ad06eddbd685749a8fd4793c9137e2`  
		Last Modified: Wed, 09 Apr 2025 01:28:14 GMT  
		Size: 384.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05cca22a1f19eeb1b73efa2be48c142e0ccaa76fb105196b36624316a16eb9c5`  
		Last Modified: Wed, 09 Apr 2025 01:28:41 GMT  
		Size: 991.4 MB (991374348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `silverpeas:latest` - unknown; unknown

```console
$ docker pull silverpeas@sha256:88161579dd526aa4e1b5a70685a58c6687e8a2e5cdb07af18b7d73d67538575c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15714245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0286863b4ec537d101938bef1f1e4ff5512c5c9cf8dda0a5ff5b376336e63f72`

```dockerfile
```

-	Layers:
	-	`sha256:299287ec3a8ed7dd28bc4e84e4453e27a9a5143b26b0c26c54c0b29c8e0c8233`  
		Last Modified: Wed, 09 Apr 2025 01:28:11 GMT  
		Size: 15.7 MB (15671698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d7c5703b08ec2cc4a8760bbf67a2666f1e53676d3e166a7d05d4070a81961ba`  
		Last Modified: Wed, 09 Apr 2025 01:28:10 GMT  
		Size: 42.5 KB (42547 bytes)  
		MIME: application/vnd.in-toto+json
