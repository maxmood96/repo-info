<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `silverpeas`

-	[`silverpeas:6.3.6`](#silverpeas636)
-	[`silverpeas:6.4.6`](#silverpeas646)
-	[`silverpeas:latest`](#silverpeaslatest)

## `silverpeas:6.3.6`

```console
$ docker pull silverpeas@sha256:959e67fc320946e772b19789fca4cd6e15b02131b74869735882e457032d37fa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `silverpeas:6.3.6` - linux; amd64

```console
$ docker pull silverpeas@sha256:30e55d365c742dc00996636c4eb8425969ba4b8d48c612ebf60f9d552cb912d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1887338487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e772c37b63ea7c16f8b65c5dd6ac8c5ff8bb19bf31c1408c8a6dda0ab63ccf57`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:38:35 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Tue, 17 Feb 2026 20:38:35 GMT
ENV TERM=xterm
# Tue, 17 Feb 2026 20:38:35 GMT
RUN apt-get update   && apt-get install -y tzdata   && apt-get install -y     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f # buildkit
# Tue, 17 Feb 2026 20:38:37 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip # buildkit
# Tue, 17 Feb 2026 20:38:40 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip # buildkit
# Tue, 17 Feb 2026 20:38:40 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Tue, 17 Feb 2026 20:39:01 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE} # buildkit
# Tue, 17 Feb 2026 20:39:01 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:39:01 GMT
ENV LANGUAGE=en_US.UTF-8
# Tue, 17 Feb 2026 20:39:01 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:39:01 GMT
ENV PING_ON=1
# Tue, 17 Feb 2026 20:39:01 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home # buildkit
# Tue, 17 Feb 2026 20:39:01 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home # buildkit
# Tue, 17 Feb 2026 20:39:01 GMT
ENV JAVA_HOME=/docker-java-home
# Tue, 17 Feb 2026 20:39:01 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Tue, 17 Feb 2026 20:39:01 GMT
ENV JBOSS_HOME=/opt/wildfly
# Tue, 17 Feb 2026 20:39:01 GMT
ENV SILVERPEAS_VERSION=6.3.6
# Tue, 17 Feb 2026 20:39:01 GMT
ENV WILDFLY_VERSION=26.1.1
# Tue, 17 Feb 2026 20:39:01 GMT
LABEL name=Silverpeas 6.3.6 description=Image to install and to run Silverpeas 6.3.6 vendor=Silverpeas version=6.3.6 build=2
# Tue, 17 Feb 2026 20:39:19 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2 # buildkit
# Tue, 17 Feb 2026 20:39:20 GMT
COPY src/settings.xml /root/.m2/ # buildkit
# Tue, 17 Feb 2026 20:39:20 GMT
COPY src/silverpeas.gradle /opt/silverpeas/bin/ # buildkit
# Tue, 17 Feb 2026 20:39:20 GMT
WORKDIR /opt/silverpeas/bin
# Tue, 17 Feb 2026 20:39:20 GMT
COPY src/run.sh /opt/ # buildkit
# Tue, 17 Feb 2026 20:39:20 GMT
COPY src/converter.groovy /opt/silverpeas/configuration/silverpeas/ # buildkit
# Tue, 17 Feb 2026 20:40:48 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle   && ./silverpeas construct   && rm ../log/build-*   && touch .install # buildkit
# Tue, 17 Feb 2026 20:40:48 GMT
EXPOSE map[8000/tcp:{} 9990/tcp:{}]
# Tue, 17 Feb 2026 20:40:48 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Tue, 17 Feb 2026 20:40:48 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e946a56642028cef7544a29e0041fcaaf6ec84bb87eefac75b1c35fb480134`  
		Last Modified: Tue, 17 Feb 2026 20:43:08 GMT  
		Size: 871.7 MB (871661395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de4ee5df5b68feeb2f137727b2d059f14c95c393ddf77697f625a2a159b8061`  
		Last Modified: Tue, 17 Feb 2026 20:42:41 GMT  
		Size: 4.0 MB (3994011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723ed96912da3925ca8db09f50399defa760b60a449293746eb6041f97f47afc`  
		Last Modified: Tue, 17 Feb 2026 20:42:41 GMT  
		Size: 7.1 MB (7146619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7c0c713fe80ea3c468579312e5997a03e03992bc9617f556863f6721567922`  
		Last Modified: Tue, 17 Feb 2026 20:42:41 GMT  
		Size: 2.5 MB (2538620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c306278d9f99e329a6cbbff4881ee304bc1c6a1c74fde52a24e3e5fb4dffde3d`  
		Last Modified: Tue, 17 Feb 2026 20:42:42 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9adc881f08d4d1997f47c4fc35835b7895f6c17af0044b24031ad51485b3a468`  
		Last Modified: Tue, 17 Feb 2026 20:42:42 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b3a61692a30582cb15f07dba0a98b32a8eba3c5a8483524b85e6efd3c75c4e`  
		Last Modified: Tue, 17 Feb 2026 20:42:51 GMT  
		Size: 217.8 MB (217843285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919e9e71514ba721da88d1cf43a9fe38d041b557438ec62b05ab95245b8db7d9`  
		Last Modified: Tue, 17 Feb 2026 20:42:43 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee863e2716d2df9f9285752d2fca3114347800374cf7c957a45bf1d62bf24a2`  
		Last Modified: Tue, 17 Feb 2026 20:42:43 GMT  
		Size: 663.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bd84aad29d2cb280fbfd2b49530bd1c9f1e001321ccb2dbfc75e728261e9f8`  
		Last Modified: Tue, 17 Feb 2026 20:42:45 GMT  
		Size: 919.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc85405ddb94ed5f205250c95bf4a58858eec344a6d3ea9577bd342f6db3ed7`  
		Last Modified: Tue, 17 Feb 2026 20:42:45 GMT  
		Size: 383.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75bbd886f9c8473585844bbb19ba9346479e399af8d94a298c77034fd8c1734`  
		Last Modified: Tue, 17 Feb 2026 20:43:09 GMT  
		Size: 754.6 MB (754614425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `silverpeas:6.3.6` - unknown; unknown

```console
$ docker pull silverpeas@sha256:edb1771e0451ef6d55d2ba1f881803012557c266b4efee58e16472b8dc770c0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26867390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f605964cf74adced8339161e68071acd1694df820cbc329497c4820765aa1942`

```dockerfile
```

-	Layers:
	-	`sha256:3b8a073c2e65da0f448a12d66ac76d60f544479ddf87a34045c51f482bd9fe94`  
		Last Modified: Tue, 17 Feb 2026 20:42:42 GMT  
		Size: 26.8 MB (26826688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e2202c90a268c3cb6751e45ed8bab6fec6ff7a6bb6cf2cb39327225ec9a7653`  
		Last Modified: Tue, 17 Feb 2026 20:42:41 GMT  
		Size: 40.7 KB (40702 bytes)  
		MIME: application/vnd.in-toto+json

## `silverpeas:6.4.6`

**does not exist** (yet?)

## `silverpeas:latest`

```console
$ docker pull silverpeas@sha256:5a51b0b5814dc5177b9cdd0e87f5465ba63d4ae693a18c3f1eebbcdff772f39a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `silverpeas:latest` - linux; amd64

```console
$ docker pull silverpeas@sha256:98899ab81c6ecab04a8d5a3ae99d913aa07850874d51473a67dd98723320402c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818086931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6946270ed7a6950df793c34820d5526188cc57bb2d3dd9f6f65e149caedbf920`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:37:49 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Tue, 17 Feb 2026 20:37:49 GMT
ENV TERM=xterm
# Tue, 17 Feb 2026 20:37:49 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends tzdata   && apt-get install -y --no-install-recommends     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f # buildkit
# Tue, 17 Feb 2026 20:37:51 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 swftools-bin-0.9.2.zip' | sha256sum -c --status -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip # buildkit
# Tue, 17 Feb 2026 20:37:53 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 pdf2json-bin-0.68.zip' | sha256sum -c --status -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip # buildkit
# Tue, 17 Feb 2026 20:37:53 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Tue, 17 Feb 2026 20:38:19 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE} # buildkit
# Tue, 17 Feb 2026 20:38:19 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:38:19 GMT
ENV LANGUAGE=en_US.UTF-8
# Tue, 17 Feb 2026 20:38:19 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 17 Feb 2026 20:38:19 GMT
ENV PING_ON=1
# Tue, 17 Feb 2026 20:38:19 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home # buildkit
# Tue, 17 Feb 2026 20:38:19 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home # buildkit
# Tue, 17 Feb 2026 20:38:19 GMT
ENV JAVA_HOME=/docker-java-home
# Tue, 17 Feb 2026 20:38:19 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Tue, 17 Feb 2026 20:38:19 GMT
ENV JBOSS_HOME=/opt/wildfly
# Tue, 17 Feb 2026 20:38:19 GMT
ENV SILVERPEAS_VERSION=6.4.5
# Tue, 17 Feb 2026 20:38:19 GMT
ENV WILDFLY_VERSION=26.1.3
# Tue, 17 Feb 2026 20:38:19 GMT
LABEL name=Silverpeas 6.4.5 description=Image to install and to run Silverpeas 6.4.5 vendor=Silverpeas version=6.4.5 build=1
# Tue, 17 Feb 2026 20:38:42 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && wget -nc https://www.silverpeas.org/files/oak-migrate.zip   && echo '87009e55520e74b5d2a386f4ebc843ee43cd1f25ca5138f342a94a31add3cfbd oak-migrate.zip' | sha256sum -c --status -   && mkdir -p /opt/oak-migration   && unzip oak-migrate.zip -d /opt/oak-migration/   && chmod +x /opt/oak-migration/oak-migrate.sh   && rm *.zip   && mkdir -p /root/.m2 # buildkit
# Tue, 17 Feb 2026 20:38:43 GMT
COPY src/settings.xml /root/.m2/ # buildkit
# Tue, 17 Feb 2026 20:38:43 GMT
COPY src/silverpeas.gradle /opt/silverpeas/bin/ # buildkit
# Tue, 17 Feb 2026 20:38:43 GMT
WORKDIR /opt/silverpeas/bin
# Tue, 17 Feb 2026 20:38:43 GMT
COPY src/run.sh /opt/ # buildkit
# Tue, 17 Feb 2026 20:38:43 GMT
COPY src/converter.groovy /opt/silverpeas/configuration/silverpeas/ # buildkit
# Tue, 17 Feb 2026 20:40:07 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN set -eux;   sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle;   echo "Construct Silverpeas ${SILVERPEAS_VERSION}";   ./silverpeas assemble || (cat ../log/build-* && exit 1);   rm ../log/build-*;   touch .install; # buildkit
# Tue, 17 Feb 2026 20:40:07 GMT
EXPOSE map[8000/tcp:{} 9990/tcp:{}]
# Tue, 17 Feb 2026 20:40:07 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Tue, 17 Feb 2026 20:40:07 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04389590c2b551acbc132d6be662836be8e54530e11e30cb484736bb4c55c501`  
		Last Modified: Tue, 17 Feb 2026 20:42:01 GMT  
		Size: 494.9 MB (494891643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb93ef0792e603dafbdae7627cdcf185459b226a635c0cd28482282c42a77a3`  
		Last Modified: Tue, 17 Feb 2026 20:41:40 GMT  
		Size: 4.0 MB (3994011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d853083a3b5518719773836b15cd2b23ff520cc88b7cc2b15257843bd9cb233`  
		Last Modified: Tue, 17 Feb 2026 20:41:40 GMT  
		Size: 7.1 MB (7146619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ffdbce641090acd54f3fd3d327d56c7c572790fe9185ac540555a89db2c327`  
		Last Modified: Tue, 17 Feb 2026 20:41:39 GMT  
		Size: 2.5 MB (2538614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3c14db9e6ce87b02e63cd6e74bf2eeb88b67dc95b84e5d5f7b85873c19946e`  
		Last Modified: Tue, 17 Feb 2026 20:41:41 GMT  
		Size: 236.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f277e65a47951b35f7f7c2ffd33a52cec963d16a1ddd6b224f0153dbe0fd02`  
		Last Modified: Tue, 17 Feb 2026 20:41:41 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c67362930872302024edb284404622ba763773ad842342e986c862a73fd829a`  
		Last Modified: Tue, 17 Feb 2026 20:41:55 GMT  
		Size: 269.1 MB (269106265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee099066d7f2221a79515c25772791cfc1287d81bdf3a0d30851e1334908fe15`  
		Last Modified: Tue, 17 Feb 2026 20:41:42 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa0e1b3b9ae0dff40f5c3375d711a1236ccab4cd7f03dd0db7d680a91482d58`  
		Last Modified: Tue, 17 Feb 2026 20:41:42 GMT  
		Size: 661.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3e664cf9e031b088a6d8d7cfc305fa9b92e73ba9a3bab6f3f8d37a288ff5ab`  
		Last Modified: Tue, 17 Feb 2026 20:41:44 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3954feaf258bbfd81159e7dd95c38d297c3b83986ee3352156bbe0bcfff2e52a`  
		Last Modified: Tue, 17 Feb 2026 20:41:44 GMT  
		Size: 384.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163f133fb9dd9a41cfb895deb5b3ce0787c10f94118f1b8990f91a20764dd6aa`  
		Last Modified: Tue, 17 Feb 2026 20:42:20 GMT  
		Size: 1.0 GB (1010869119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `silverpeas:latest` - unknown; unknown

```console
$ docker pull silverpeas@sha256:367524ef1394d5ae4cc3033bac40cec9bcf6eb4d4f886cba3740f92d05b16f0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16648249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbd58fcebe3391b7ece07abe1c530e05a1bbc936b86281ee68f78c603e67b623`

```dockerfile
```

-	Layers:
	-	`sha256:de853e71cfc2eb4ae67128732ae56e67920e175ef84256dde36ca88b82d21358`  
		Last Modified: Tue, 17 Feb 2026 20:41:40 GMT  
		Size: 16.6 MB (16605743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ff7aef5fc954b805610cb5c32047994a9281b8a2d815aca7081b93f7dbd1346`  
		Last Modified: Tue, 17 Feb 2026 20:41:39 GMT  
		Size: 42.5 KB (42506 bytes)  
		MIME: application/vnd.in-toto+json
