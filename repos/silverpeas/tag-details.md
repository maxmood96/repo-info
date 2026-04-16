<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `silverpeas`

-	[`silverpeas:6.3.6`](#silverpeas636)
-	[`silverpeas:6.4.6`](#silverpeas646)
-	[`silverpeas:latest`](#silverpeaslatest)

## `silverpeas:6.3.6`

```console
$ docker pull silverpeas@sha256:fb88c9e267e655067265e42764b67fb587880dd362a3f65a33b3f8165ae99cef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `silverpeas:6.3.6` - linux; amd64

```console
$ docker pull silverpeas@sha256:c20e5e5e94833ca409797617888265c17664e80ffba8130c0bd8bed2c43bddd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1887525137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:303b13bfd6d6112bc73dd7f6571929cfa8b6be70eed88a801113b7c2e5caeb02`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:02:48 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Wed, 15 Apr 2026 21:02:48 GMT
ENV TERM=xterm
# Wed, 15 Apr 2026 21:02:48 GMT
RUN apt-get update   && apt-get install -y tzdata   && apt-get install -y     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f # buildkit
# Wed, 15 Apr 2026 21:02:50 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip # buildkit
# Wed, 15 Apr 2026 21:02:52 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip # buildkit
# Wed, 15 Apr 2026 21:02:52 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Wed, 15 Apr 2026 21:03:13 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE} # buildkit
# Wed, 15 Apr 2026 21:03:13 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 21:03:13 GMT
ENV LANGUAGE=en_US.UTF-8
# Wed, 15 Apr 2026 21:03:13 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 21:03:13 GMT
ENV PING_ON=1
# Wed, 15 Apr 2026 21:03:13 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home # buildkit
# Wed, 15 Apr 2026 21:03:13 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home # buildkit
# Wed, 15 Apr 2026 21:03:13 GMT
ENV JAVA_HOME=/docker-java-home
# Wed, 15 Apr 2026 21:03:13 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Wed, 15 Apr 2026 21:03:13 GMT
ENV JBOSS_HOME=/opt/wildfly
# Wed, 15 Apr 2026 21:03:13 GMT
ENV SILVERPEAS_VERSION=6.3.6
# Wed, 15 Apr 2026 21:03:13 GMT
ENV WILDFLY_VERSION=26.1.1
# Wed, 15 Apr 2026 21:03:13 GMT
LABEL name=Silverpeas 6.3.6 description=Image to install and to run Silverpeas 6.3.6 vendor=Silverpeas version=6.3.6 build=2
# Wed, 15 Apr 2026 21:03:32 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2 # buildkit
# Wed, 15 Apr 2026 21:03:32 GMT
COPY src/settings.xml /root/.m2/ # buildkit
# Wed, 15 Apr 2026 21:03:32 GMT
COPY src/silverpeas.gradle /opt/silverpeas/bin/ # buildkit
# Wed, 15 Apr 2026 21:03:32 GMT
WORKDIR /opt/silverpeas/bin
# Wed, 15 Apr 2026 21:03:32 GMT
COPY src/run.sh /opt/ # buildkit
# Wed, 15 Apr 2026 21:03:32 GMT
COPY src/converter.groovy /opt/silverpeas/configuration/silverpeas/ # buildkit
# Wed, 15 Apr 2026 21:04:47 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle   && ./silverpeas construct   && rm ../log/build-*   && touch .install # buildkit
# Wed, 15 Apr 2026 21:04:47 GMT
EXPOSE map[8000/tcp:{} 9990/tcp:{}]
# Wed, 15 Apr 2026 21:04:47 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Wed, 15 Apr 2026 21:04:47 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969b367177eb7275e9be37f704cab8366a144dafbb746db3ad2137615a96631b`  
		Last Modified: Wed, 15 Apr 2026 21:07:11 GMT  
		Size: 871.7 MB (871656103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3bbaf534e696ce3df8ac560672254ed155747867b4eda92594f4e3c2e71111e`  
		Last Modified: Wed, 15 Apr 2026 21:06:39 GMT  
		Size: 4.0 MB (3994014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac34061bdd7b9ee18298cf9948e77b88d7fc20a816ede9357637d6555f8d1d5`  
		Last Modified: Wed, 15 Apr 2026 21:06:39 GMT  
		Size: 7.1 MB (7146619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3087a463085da0abb210ba0ca9549ab2bef366f033fac813a3c7f3ca966b914c`  
		Last Modified: Wed, 15 Apr 2026 21:06:39 GMT  
		Size: 2.5 MB (2538613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b96fc636000d61e00147162ad245e40519536cf857cb4a97135447551dad71`  
		Last Modified: Wed, 15 Apr 2026 21:06:41 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd828b9541e21541be069d8a0adbe2f7720b3afa9ceb2a8b158a837a7014ff3e`  
		Last Modified: Wed, 15 Apr 2026 21:06:41 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ed87ed98d63896b2ef4405175faa98bd98523f48c06ddbee1508a782d259cd`  
		Last Modified: Wed, 15 Apr 2026 21:06:52 GMT  
		Size: 217.8 MB (217843269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f75d18784f0ba7fdf98c173eb1d3a7d13b61b52383faa238cf34579c4fd482`  
		Last Modified: Wed, 15 Apr 2026 21:06:42 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44f0c247212efd4761906081d06edb0f65f48f4797acce20d2a88cdb02b3149`  
		Last Modified: Wed, 15 Apr 2026 21:06:42 GMT  
		Size: 664.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66991d6eb84a84898b784f5d00264617b63fec9dcfcfd24c0f4ce2f6bef60a8e`  
		Last Modified: Wed, 15 Apr 2026 21:06:43 GMT  
		Size: 921.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948a225d7aba12b58add6842169a660dacb10cb9ca6395558a976837368da888`  
		Last Modified: Wed, 15 Apr 2026 21:06:44 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699a8e6e215a438e00f5a830dd308739f236f25d2d020ee5a63a32c755af775f`  
		Last Modified: Wed, 15 Apr 2026 21:07:13 GMT  
		Size: 754.6 MB (754607247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `silverpeas:6.3.6` - unknown; unknown

```console
$ docker pull silverpeas@sha256:51ee69c1ee51d1aea73bece47629368e1c9121abe60320bc76ec55d9caaade99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26867408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804fee0d2998aadce0dea41a8477957908554fb795cf1f7d3185ae8b0f2237da`

```dockerfile
```

-	Layers:
	-	`sha256:5ead7984cd332c87bcb0489e07eb503ec64c42d639bd7324d14535ac177e540c`  
		Last Modified: Wed, 15 Apr 2026 21:06:40 GMT  
		Size: 26.8 MB (26826706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c38fd33ceb45f914238f36852c24b699fe20461e56d37d021e1f1a672f43546`  
		Last Modified: Wed, 15 Apr 2026 21:06:39 GMT  
		Size: 40.7 KB (40702 bytes)  
		MIME: application/vnd.in-toto+json

## `silverpeas:6.4.6`

```console
$ docker pull silverpeas@sha256:a72b07c10d0045dca69fb0f088c46c4ace622cf2432a5c0f8cef14fda2529349
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `silverpeas:6.4.6` - linux; amd64

```console
$ docker pull silverpeas@sha256:d3f2feb3792902a315e7b4179ca2ed2dffa82a463815517b54868438d16b96e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818271531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed829afe4c8c10612bc140892217fd0b878155e28855b61bc8d650621d468cd0`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:02:03 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Wed, 15 Apr 2026 21:02:03 GMT
ENV TERM=xterm
# Wed, 15 Apr 2026 21:02:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends tzdata   && apt-get install -y --no-install-recommends     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f # buildkit
# Wed, 15 Apr 2026 21:02:05 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 swftools-bin-0.9.2.zip' | sha256sum -c --status -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip # buildkit
# Wed, 15 Apr 2026 21:02:07 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 pdf2json-bin-0.68.zip' | sha256sum -c --status -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip # buildkit
# Wed, 15 Apr 2026 21:02:07 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Wed, 15 Apr 2026 21:02:30 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE} # buildkit
# Wed, 15 Apr 2026 21:02:30 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 21:02:30 GMT
ENV LANGUAGE=en_US.UTF-8
# Wed, 15 Apr 2026 21:02:30 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 21:02:30 GMT
ENV PING_ON=1
# Wed, 15 Apr 2026 21:02:30 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home # buildkit
# Wed, 15 Apr 2026 21:02:30 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home # buildkit
# Wed, 15 Apr 2026 21:02:30 GMT
ENV JAVA_HOME=/docker-java-home
# Wed, 15 Apr 2026 21:02:30 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Wed, 15 Apr 2026 21:02:30 GMT
ENV JBOSS_HOME=/opt/wildfly
# Wed, 15 Apr 2026 21:02:30 GMT
ENV SILVERPEAS_VERSION=6.4.6
# Wed, 15 Apr 2026 21:02:30 GMT
ENV WILDFLY_VERSION=26.1.3
# Wed, 15 Apr 2026 21:02:30 GMT
LABEL name=Silverpeas 6.4.6 description=Image to install and to run Silverpeas 6.4.6 vendor=Silverpeas version=6.4.6 build=1
# Wed, 15 Apr 2026 21:02:53 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && wget -nc https://www.silverpeas.org/files/oak-migrate.zip   && echo '87009e55520e74b5d2a386f4ebc843ee43cd1f25ca5138f342a94a31add3cfbd oak-migrate.zip' | sha256sum -c --status -   && mkdir -p /opt/oak-migration   && unzip oak-migrate.zip -d /opt/oak-migration/   && chmod +x /opt/oak-migration/oak-migrate.sh   && rm *.zip   && mkdir -p /root/.m2 # buildkit
# Wed, 15 Apr 2026 21:02:53 GMT
COPY src/settings.xml /root/.m2/ # buildkit
# Wed, 15 Apr 2026 21:02:53 GMT
COPY src/silverpeas.gradle /opt/silverpeas/bin/ # buildkit
# Wed, 15 Apr 2026 21:02:53 GMT
WORKDIR /opt/silverpeas/bin
# Wed, 15 Apr 2026 21:02:53 GMT
COPY src/run.sh /opt/ # buildkit
# Wed, 15 Apr 2026 21:02:53 GMT
COPY src/converter.groovy /opt/silverpeas/configuration/silverpeas/ # buildkit
# Wed, 15 Apr 2026 21:04:19 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN set -eux;   sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle;   echo "Construct Silverpeas ${SILVERPEAS_VERSION}";   ./silverpeas assemble || (cat ../log/build-* && exit 1);   rm ../log/build-*;   touch .install; # buildkit
# Wed, 15 Apr 2026 21:04:19 GMT
EXPOSE map[8000/tcp:{} 9990/tcp:{}]
# Wed, 15 Apr 2026 21:04:19 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Wed, 15 Apr 2026 21:04:19 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a194293a6471517b2675170757aa88edd563a996900254585d312ea8faef6e1a`  
		Last Modified: Wed, 15 Apr 2026 21:06:03 GMT  
		Size: 494.9 MB (494877018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2a875b319fe116c764ee5c9b4ea6f9ab451039b79880937284912b027ed30c`  
		Last Modified: Wed, 15 Apr 2026 21:05:44 GMT  
		Size: 4.0 MB (3994015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362dc26901c42707d1626c4fab2a85850f4d951663983a8a1a35fdb15a03e60b`  
		Last Modified: Wed, 15 Apr 2026 21:05:44 GMT  
		Size: 7.1 MB (7146625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b730b6d15a51dec73ec7c35f146ea85b88c25af002217215c6f4790f69d5f55`  
		Last Modified: Wed, 15 Apr 2026 21:05:44 GMT  
		Size: 2.5 MB (2538614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fcffd6f458db412cb1d3407cd81309f98e89d4f6655b7569624bad398a2fe0`  
		Last Modified: Wed, 15 Apr 2026 21:05:45 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a761c0c8ee2a5e60206fcda8d891f7b9c316ba05b9fd4ed67836e8875a532c`  
		Last Modified: Wed, 15 Apr 2026 21:05:45 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa387acc3cb1a6d895cac6c5b5c89d85918a9537cd2d804f3e14252ac75ccfd`  
		Last Modified: Wed, 15 Apr 2026 21:05:59 GMT  
		Size: 269.1 MB (269106251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3c32218eb0976fe3b5630daf30342f6392091f459e8de07206f8c9a5af61bc`  
		Last Modified: Wed, 15 Apr 2026 21:05:47 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f0a3e3fc3262a2e32a6c7c4a1de8dc7dd20b013bff0d05eb8dc238ba3da768`  
		Last Modified: Wed, 15 Apr 2026 21:05:47 GMT  
		Size: 660.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b9daa7c8f95ff8a5625bb9b0f964775a8f6e72ecfa78fbba8297829cb17bc97`  
		Last Modified: Wed, 15 Apr 2026 21:05:48 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2115e2a4260b8e60b2ffc59c32d5d4c9119ecb225803445fa4c23d1889ceca`  
		Last Modified: Wed, 15 Apr 2026 21:05:48 GMT  
		Size: 383.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e27347b222499481ea125f82670e49cccb3bf8b5e9ffcc9d78424afe4af8e4`  
		Last Modified: Wed, 15 Apr 2026 21:06:19 GMT  
		Size: 1.0 GB (1010869219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `silverpeas:6.4.6` - unknown; unknown

```console
$ docker pull silverpeas@sha256:bfb0446ff6cb7a72a4e7e00a90233c104b1a6ed775569349c9631045fb7fa439
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16648828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5975db589ef0389fc2163d352488688de1093e12fec9544cde0369c810a1aa7c`

```dockerfile
```

-	Layers:
	-	`sha256:6eb4f8662df88145a012f50f5a22a9d29d1c78ce7c041d4e745cb0100c2917ee`  
		Last Modified: Wed, 15 Apr 2026 21:05:45 GMT  
		Size: 16.6 MB (16606322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3b5beabe988e46f3f5183af614ceb94057eb76317c4791cd01a182c81654699`  
		Last Modified: Wed, 15 Apr 2026 21:05:44 GMT  
		Size: 42.5 KB (42506 bytes)  
		MIME: application/vnd.in-toto+json

## `silverpeas:latest`

```console
$ docker pull silverpeas@sha256:a72b07c10d0045dca69fb0f088c46c4ace622cf2432a5c0f8cef14fda2529349
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `silverpeas:latest` - linux; amd64

```console
$ docker pull silverpeas@sha256:d3f2feb3792902a315e7b4179ca2ed2dffa82a463815517b54868438d16b96e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818271531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed829afe4c8c10612bc140892217fd0b878155e28855b61bc8d650621d468cd0`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:02:03 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Wed, 15 Apr 2026 21:02:03 GMT
ENV TERM=xterm
# Wed, 15 Apr 2026 21:02:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends tzdata   && apt-get install -y --no-install-recommends     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f # buildkit
# Wed, 15 Apr 2026 21:02:05 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 swftools-bin-0.9.2.zip' | sha256sum -c --status -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip # buildkit
# Wed, 15 Apr 2026 21:02:07 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 pdf2json-bin-0.68.zip' | sha256sum -c --status -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip # buildkit
# Wed, 15 Apr 2026 21:02:07 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Wed, 15 Apr 2026 21:02:30 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE} # buildkit
# Wed, 15 Apr 2026 21:02:30 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 21:02:30 GMT
ENV LANGUAGE=en_US.UTF-8
# Wed, 15 Apr 2026 21:02:30 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 15 Apr 2026 21:02:30 GMT
ENV PING_ON=1
# Wed, 15 Apr 2026 21:02:30 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home # buildkit
# Wed, 15 Apr 2026 21:02:30 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home # buildkit
# Wed, 15 Apr 2026 21:02:30 GMT
ENV JAVA_HOME=/docker-java-home
# Wed, 15 Apr 2026 21:02:30 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Wed, 15 Apr 2026 21:02:30 GMT
ENV JBOSS_HOME=/opt/wildfly
# Wed, 15 Apr 2026 21:02:30 GMT
ENV SILVERPEAS_VERSION=6.4.6
# Wed, 15 Apr 2026 21:02:30 GMT
ENV WILDFLY_VERSION=26.1.3
# Wed, 15 Apr 2026 21:02:30 GMT
LABEL name=Silverpeas 6.4.6 description=Image to install and to run Silverpeas 6.4.6 vendor=Silverpeas version=6.4.6 build=1
# Wed, 15 Apr 2026 21:02:53 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && wget -nc https://www.silverpeas.org/files/oak-migrate.zip   && echo '87009e55520e74b5d2a386f4ebc843ee43cd1f25ca5138f342a94a31add3cfbd oak-migrate.zip' | sha256sum -c --status -   && mkdir -p /opt/oak-migration   && unzip oak-migrate.zip -d /opt/oak-migration/   && chmod +x /opt/oak-migration/oak-migrate.sh   && rm *.zip   && mkdir -p /root/.m2 # buildkit
# Wed, 15 Apr 2026 21:02:53 GMT
COPY src/settings.xml /root/.m2/ # buildkit
# Wed, 15 Apr 2026 21:02:53 GMT
COPY src/silverpeas.gradle /opt/silverpeas/bin/ # buildkit
# Wed, 15 Apr 2026 21:02:53 GMT
WORKDIR /opt/silverpeas/bin
# Wed, 15 Apr 2026 21:02:53 GMT
COPY src/run.sh /opt/ # buildkit
# Wed, 15 Apr 2026 21:02:53 GMT
COPY src/converter.groovy /opt/silverpeas/configuration/silverpeas/ # buildkit
# Wed, 15 Apr 2026 21:04:19 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN set -eux;   sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle;   echo "Construct Silverpeas ${SILVERPEAS_VERSION}";   ./silverpeas assemble || (cat ../log/build-* && exit 1);   rm ../log/build-*;   touch .install; # buildkit
# Wed, 15 Apr 2026 21:04:19 GMT
EXPOSE map[8000/tcp:{} 9990/tcp:{}]
# Wed, 15 Apr 2026 21:04:19 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Wed, 15 Apr 2026 21:04:19 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a194293a6471517b2675170757aa88edd563a996900254585d312ea8faef6e1a`  
		Last Modified: Wed, 15 Apr 2026 21:06:03 GMT  
		Size: 494.9 MB (494877018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2a875b319fe116c764ee5c9b4ea6f9ab451039b79880937284912b027ed30c`  
		Last Modified: Wed, 15 Apr 2026 21:05:44 GMT  
		Size: 4.0 MB (3994015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362dc26901c42707d1626c4fab2a85850f4d951663983a8a1a35fdb15a03e60b`  
		Last Modified: Wed, 15 Apr 2026 21:05:44 GMT  
		Size: 7.1 MB (7146625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b730b6d15a51dec73ec7c35f146ea85b88c25af002217215c6f4790f69d5f55`  
		Last Modified: Wed, 15 Apr 2026 21:05:44 GMT  
		Size: 2.5 MB (2538614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fcffd6f458db412cb1d3407cd81309f98e89d4f6655b7569624bad398a2fe0`  
		Last Modified: Wed, 15 Apr 2026 21:05:45 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a761c0c8ee2a5e60206fcda8d891f7b9c316ba05b9fd4ed67836e8875a532c`  
		Last Modified: Wed, 15 Apr 2026 21:05:45 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa387acc3cb1a6d895cac6c5b5c89d85918a9537cd2d804f3e14252ac75ccfd`  
		Last Modified: Wed, 15 Apr 2026 21:05:59 GMT  
		Size: 269.1 MB (269106251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3c32218eb0976fe3b5630daf30342f6392091f459e8de07206f8c9a5af61bc`  
		Last Modified: Wed, 15 Apr 2026 21:05:47 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f0a3e3fc3262a2e32a6c7c4a1de8dc7dd20b013bff0d05eb8dc238ba3da768`  
		Last Modified: Wed, 15 Apr 2026 21:05:47 GMT  
		Size: 660.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b9daa7c8f95ff8a5625bb9b0f964775a8f6e72ecfa78fbba8297829cb17bc97`  
		Last Modified: Wed, 15 Apr 2026 21:05:48 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2115e2a4260b8e60b2ffc59c32d5d4c9119ecb225803445fa4c23d1889ceca`  
		Last Modified: Wed, 15 Apr 2026 21:05:48 GMT  
		Size: 383.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e27347b222499481ea125f82670e49cccb3bf8b5e9ffcc9d78424afe4af8e4`  
		Last Modified: Wed, 15 Apr 2026 21:06:19 GMT  
		Size: 1.0 GB (1010869219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `silverpeas:latest` - unknown; unknown

```console
$ docker pull silverpeas@sha256:bfb0446ff6cb7a72a4e7e00a90233c104b1a6ed775569349c9631045fb7fa439
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16648828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5975db589ef0389fc2163d352488688de1093e12fec9544cde0369c810a1aa7c`

```dockerfile
```

-	Layers:
	-	`sha256:6eb4f8662df88145a012f50f5a22a9d29d1c78ce7c041d4e745cb0100c2917ee`  
		Last Modified: Wed, 15 Apr 2026 21:05:45 GMT  
		Size: 16.6 MB (16606322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3b5beabe988e46f3f5183af614ceb94057eb76317c4791cd01a182c81654699`  
		Last Modified: Wed, 15 Apr 2026 21:05:44 GMT  
		Size: 42.5 KB (42506 bytes)  
		MIME: application/vnd.in-toto+json
