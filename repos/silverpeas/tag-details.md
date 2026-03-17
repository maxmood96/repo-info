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

```console
$ docker pull silverpeas@sha256:4288f455d4aac3bfb4e362c258224bbdba09f375f79886a5eab82b7940cdc82e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `silverpeas:6.4.6` - linux; amd64

```console
$ docker pull silverpeas@sha256:b66e3c28ced24850261506d05aea66f0b15e788abb2285bf7187234ddf6b5f87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1819209808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f83a8e6c32d2f39e8caa3a92ebcebf1edc927a1afbd6d161c17df4f55e746c09`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:27:47 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Tue, 17 Mar 2026 02:27:47 GMT
ENV TERM=xterm
# Tue, 17 Mar 2026 02:27:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends tzdata   && apt-get install -y --no-install-recommends     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f # buildkit
# Tue, 17 Mar 2026 02:27:49 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 swftools-bin-0.9.2.zip' | sha256sum -c --status -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip # buildkit
# Tue, 17 Mar 2026 02:27:51 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 pdf2json-bin-0.68.zip' | sha256sum -c --status -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip # buildkit
# Tue, 17 Mar 2026 02:27:51 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Tue, 17 Mar 2026 02:28:13 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE} # buildkit
# Tue, 17 Mar 2026 02:28:13 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 02:28:13 GMT
ENV LANGUAGE=en_US.UTF-8
# Tue, 17 Mar 2026 02:28:13 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 02:28:13 GMT
ENV PING_ON=1
# Tue, 17 Mar 2026 02:28:13 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home # buildkit
# Tue, 17 Mar 2026 02:28:13 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home # buildkit
# Tue, 17 Mar 2026 02:28:13 GMT
ENV JAVA_HOME=/docker-java-home
# Tue, 17 Mar 2026 02:28:13 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Tue, 17 Mar 2026 02:28:13 GMT
ENV JBOSS_HOME=/opt/wildfly
# Tue, 17 Mar 2026 02:28:13 GMT
ENV SILVERPEAS_VERSION=6.4.6
# Tue, 17 Mar 2026 02:28:13 GMT
ENV WILDFLY_VERSION=26.1.3
# Tue, 17 Mar 2026 02:28:13 GMT
LABEL name=Silverpeas 6.4.6 description=Image to install and to run Silverpeas 6.4.6 vendor=Silverpeas version=6.4.6 build=1
# Tue, 17 Mar 2026 02:28:36 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && wget -nc https://www.silverpeas.org/files/oak-migrate.zip   && echo '87009e55520e74b5d2a386f4ebc843ee43cd1f25ca5138f342a94a31add3cfbd oak-migrate.zip' | sha256sum -c --status -   && mkdir -p /opt/oak-migration   && unzip oak-migrate.zip -d /opt/oak-migration/   && chmod +x /opt/oak-migration/oak-migrate.sh   && rm *.zip   && mkdir -p /root/.m2 # buildkit
# Tue, 17 Mar 2026 02:28:36 GMT
COPY src/settings.xml /root/.m2/ # buildkit
# Tue, 17 Mar 2026 02:28:36 GMT
COPY src/silverpeas.gradle /opt/silverpeas/bin/ # buildkit
# Tue, 17 Mar 2026 02:28:36 GMT
WORKDIR /opt/silverpeas/bin
# Tue, 17 Mar 2026 02:28:36 GMT
COPY src/run.sh /opt/ # buildkit
# Tue, 17 Mar 2026 02:28:36 GMT
COPY src/converter.groovy /opt/silverpeas/configuration/silverpeas/ # buildkit
# Tue, 17 Mar 2026 02:30:03 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN set -eux;   sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle;   echo "Construct Silverpeas ${SILVERPEAS_VERSION}";   ./silverpeas assemble || (cat ../log/build-* && exit 1);   rm ../log/build-*;   touch .install; # buildkit
# Tue, 17 Mar 2026 02:30:03 GMT
EXPOSE map[8000/tcp:{} 9990/tcp:{}]
# Tue, 17 Mar 2026 02:30:03 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Tue, 17 Mar 2026 02:30:03 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20b01d9bb94fdba779513f21daa66165f5fdd6bc72c9b61a295d8bbd0d30acd`  
		Last Modified: Tue, 17 Mar 2026 02:31:45 GMT  
		Size: 496.0 MB (496015210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120fe3a9f1fe97513fee68b0f78149607b4b2c48fec10b7431d51ca2507c0a3a`  
		Last Modified: Tue, 17 Mar 2026 02:31:27 GMT  
		Size: 4.0 MB (3994006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8fb4193022325cf1270cf8bcba61e429b3eff472d4ef073db353136c1f73f1a`  
		Last Modified: Tue, 17 Mar 2026 02:31:27 GMT  
		Size: 7.1 MB (7146617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd33bf264fd6f4f61dd8761c568118c418789172d433f6d917b098dab827406`  
		Last Modified: Tue, 17 Mar 2026 02:31:27 GMT  
		Size: 2.5 MB (2538616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd95e9bf51f198b4f4d73fec53838fa660f7cd4f855af3e18016e16d1e78a71`  
		Last Modified: Tue, 17 Mar 2026 02:31:28 GMT  
		Size: 236.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d9e529e5df0e9aa06953cec5e8f294aa404dc4f53286e458fc88e38fd547c7`  
		Last Modified: Tue, 17 Mar 2026 02:31:29 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f014621ef2bcc1b732e5624f651c40b94f4a891a1b1bcbb5631f255c69d21c4c`  
		Last Modified: Tue, 17 Mar 2026 02:31:39 GMT  
		Size: 269.1 MB (269106247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9513bce4846d35bd7e0913aa63e70f249b6005706b8b6f61e325e2339250a188`  
		Last Modified: Tue, 17 Mar 2026 02:31:30 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a995bcdf6da6a020bb3454596df4f510c8abc0cbfa24d435eed2f44d7f98c17`  
		Last Modified: Tue, 17 Mar 2026 02:31:30 GMT  
		Size: 663.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b7bcb256d3003e7b2195aea568209cc1e187a4d43fa4a57e0bdbd2d8796ebd`  
		Last Modified: Tue, 17 Mar 2026 02:31:31 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e02ba07171ccf935cbf9ac96292af3be532d10f955d10b3e989a8e43d2c81a9`  
		Last Modified: Tue, 17 Mar 2026 02:31:31 GMT  
		Size: 384.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956a0502038748a2abaa1d231603830afaf7b05e44b036ed646f1e266cd81162`  
		Last Modified: Tue, 17 Mar 2026 02:31:57 GMT  
		Size: 1.0 GB (1010867293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `silverpeas:6.4.6` - unknown; unknown

```console
$ docker pull silverpeas@sha256:4d37303b84d552d9ecd4cf5107d7c121a581ccacf0cd78bc6b7fa8012ea5d969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16648816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b542f9004b15737671a1d8a5b14ea0fe3c217756c9753c4643d7cbb501eff51`

```dockerfile
```

-	Layers:
	-	`sha256:2cde4b7d2b40dafb9d68d3ddccb494a815496e2d39764bb5d53f0f0308e9cfab`  
		Last Modified: Tue, 17 Mar 2026 02:31:29 GMT  
		Size: 16.6 MB (16606310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:472b4154ef3d15445eed24bc3eb681e5fc08fe2c73561d738824715e54e21c09`  
		Last Modified: Tue, 17 Mar 2026 02:31:27 GMT  
		Size: 42.5 KB (42506 bytes)  
		MIME: application/vnd.in-toto+json

## `silverpeas:latest`

```console
$ docker pull silverpeas@sha256:4288f455d4aac3bfb4e362c258224bbdba09f375f79886a5eab82b7940cdc82e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `silverpeas:latest` - linux; amd64

```console
$ docker pull silverpeas@sha256:b66e3c28ced24850261506d05aea66f0b15e788abb2285bf7187234ddf6b5f87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1819209808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f83a8e6c32d2f39e8caa3a92ebcebf1edc927a1afbd6d161c17df4f55e746c09`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:27:47 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Tue, 17 Mar 2026 02:27:47 GMT
ENV TERM=xterm
# Tue, 17 Mar 2026 02:27:47 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends tzdata   && apt-get install -y --no-install-recommends     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f # buildkit
# Tue, 17 Mar 2026 02:27:49 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 swftools-bin-0.9.2.zip' | sha256sum -c --status -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip # buildkit
# Tue, 17 Mar 2026 02:27:51 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 pdf2json-bin-0.68.zip' | sha256sum -c --status -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip # buildkit
# Tue, 17 Mar 2026 02:27:51 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Tue, 17 Mar 2026 02:28:13 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE} # buildkit
# Tue, 17 Mar 2026 02:28:13 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 02:28:13 GMT
ENV LANGUAGE=en_US.UTF-8
# Tue, 17 Mar 2026 02:28:13 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 17 Mar 2026 02:28:13 GMT
ENV PING_ON=1
# Tue, 17 Mar 2026 02:28:13 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home # buildkit
# Tue, 17 Mar 2026 02:28:13 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home # buildkit
# Tue, 17 Mar 2026 02:28:13 GMT
ENV JAVA_HOME=/docker-java-home
# Tue, 17 Mar 2026 02:28:13 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Tue, 17 Mar 2026 02:28:13 GMT
ENV JBOSS_HOME=/opt/wildfly
# Tue, 17 Mar 2026 02:28:13 GMT
ENV SILVERPEAS_VERSION=6.4.6
# Tue, 17 Mar 2026 02:28:13 GMT
ENV WILDFLY_VERSION=26.1.3
# Tue, 17 Mar 2026 02:28:13 GMT
LABEL name=Silverpeas 6.4.6 description=Image to install and to run Silverpeas 6.4.6 vendor=Silverpeas version=6.4.6 build=1
# Tue, 17 Mar 2026 02:28:36 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && wget -nc https://www.silverpeas.org/files/oak-migrate.zip   && echo '87009e55520e74b5d2a386f4ebc843ee43cd1f25ca5138f342a94a31add3cfbd oak-migrate.zip' | sha256sum -c --status -   && mkdir -p /opt/oak-migration   && unzip oak-migrate.zip -d /opt/oak-migration/   && chmod +x /opt/oak-migration/oak-migrate.sh   && rm *.zip   && mkdir -p /root/.m2 # buildkit
# Tue, 17 Mar 2026 02:28:36 GMT
COPY src/settings.xml /root/.m2/ # buildkit
# Tue, 17 Mar 2026 02:28:36 GMT
COPY src/silverpeas.gradle /opt/silverpeas/bin/ # buildkit
# Tue, 17 Mar 2026 02:28:36 GMT
WORKDIR /opt/silverpeas/bin
# Tue, 17 Mar 2026 02:28:36 GMT
COPY src/run.sh /opt/ # buildkit
# Tue, 17 Mar 2026 02:28:36 GMT
COPY src/converter.groovy /opt/silverpeas/configuration/silverpeas/ # buildkit
# Tue, 17 Mar 2026 02:30:03 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN set -eux;   sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle;   echo "Construct Silverpeas ${SILVERPEAS_VERSION}";   ./silverpeas assemble || (cat ../log/build-* && exit 1);   rm ../log/build-*;   touch .install; # buildkit
# Tue, 17 Mar 2026 02:30:03 GMT
EXPOSE map[8000/tcp:{} 9990/tcp:{}]
# Tue, 17 Mar 2026 02:30:03 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Tue, 17 Mar 2026 02:30:03 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20b01d9bb94fdba779513f21daa66165f5fdd6bc72c9b61a295d8bbd0d30acd`  
		Last Modified: Tue, 17 Mar 2026 02:31:45 GMT  
		Size: 496.0 MB (496015210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120fe3a9f1fe97513fee68b0f78149607b4b2c48fec10b7431d51ca2507c0a3a`  
		Last Modified: Tue, 17 Mar 2026 02:31:27 GMT  
		Size: 4.0 MB (3994006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8fb4193022325cf1270cf8bcba61e429b3eff472d4ef073db353136c1f73f1a`  
		Last Modified: Tue, 17 Mar 2026 02:31:27 GMT  
		Size: 7.1 MB (7146617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd33bf264fd6f4f61dd8761c568118c418789172d433f6d917b098dab827406`  
		Last Modified: Tue, 17 Mar 2026 02:31:27 GMT  
		Size: 2.5 MB (2538616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd95e9bf51f198b4f4d73fec53838fa660f7cd4f855af3e18016e16d1e78a71`  
		Last Modified: Tue, 17 Mar 2026 02:31:28 GMT  
		Size: 236.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d9e529e5df0e9aa06953cec5e8f294aa404dc4f53286e458fc88e38fd547c7`  
		Last Modified: Tue, 17 Mar 2026 02:31:29 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f014621ef2bcc1b732e5624f651c40b94f4a891a1b1bcbb5631f255c69d21c4c`  
		Last Modified: Tue, 17 Mar 2026 02:31:39 GMT  
		Size: 269.1 MB (269106247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9513bce4846d35bd7e0913aa63e70f249b6005706b8b6f61e325e2339250a188`  
		Last Modified: Tue, 17 Mar 2026 02:31:30 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a995bcdf6da6a020bb3454596df4f510c8abc0cbfa24d435eed2f44d7f98c17`  
		Last Modified: Tue, 17 Mar 2026 02:31:30 GMT  
		Size: 663.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b7bcb256d3003e7b2195aea568209cc1e187a4d43fa4a57e0bdbd2d8796ebd`  
		Last Modified: Tue, 17 Mar 2026 02:31:31 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e02ba07171ccf935cbf9ac96292af3be532d10f955d10b3e989a8e43d2c81a9`  
		Last Modified: Tue, 17 Mar 2026 02:31:31 GMT  
		Size: 384.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956a0502038748a2abaa1d231603830afaf7b05e44b036ed646f1e266cd81162`  
		Last Modified: Tue, 17 Mar 2026 02:31:57 GMT  
		Size: 1.0 GB (1010867293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `silverpeas:latest` - unknown; unknown

```console
$ docker pull silverpeas@sha256:4d37303b84d552d9ecd4cf5107d7c121a581ccacf0cd78bc6b7fa8012ea5d969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16648816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b542f9004b15737671a1d8a5b14ea0fe3c217756c9753c4643d7cbb501eff51`

```dockerfile
```

-	Layers:
	-	`sha256:2cde4b7d2b40dafb9d68d3ddccb494a815496e2d39764bb5d53f0f0308e9cfab`  
		Last Modified: Tue, 17 Mar 2026 02:31:29 GMT  
		Size: 16.6 MB (16606310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:472b4154ef3d15445eed24bc3eb681e5fc08fe2c73561d738824715e54e21c09`  
		Last Modified: Tue, 17 Mar 2026 02:31:27 GMT  
		Size: 42.5 KB (42506 bytes)  
		MIME: application/vnd.in-toto+json
