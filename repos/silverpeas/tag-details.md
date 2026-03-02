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
$ docker pull silverpeas@sha256:6d0056d6730b9c26ada884cb572d4f7efed881162803d5e0a4115ca06a15e983
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `silverpeas:6.4.6` - linux; amd64

```console
$ docker pull silverpeas@sha256:51e5b6c302680fef30305effd543dc8e4748e1be65b0713890aca36038111735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1819219255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45b2040d9b6e3a214c2cfdee3723240eef6deb39563dc8dc565456ba10000cf`
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
# Mon, 02 Mar 2026 19:51:10 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Mon, 02 Mar 2026 19:51:10 GMT
ENV TERM=xterm
# Mon, 02 Mar 2026 19:51:10 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends tzdata   && apt-get install -y --no-install-recommends     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f # buildkit
# Mon, 02 Mar 2026 19:51:12 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 swftools-bin-0.9.2.zip' | sha256sum -c --status -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip # buildkit
# Mon, 02 Mar 2026 19:51:15 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 pdf2json-bin-0.68.zip' | sha256sum -c --status -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip # buildkit
# Mon, 02 Mar 2026 19:51:15 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Mon, 02 Mar 2026 19:51:38 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE} # buildkit
# Mon, 02 Mar 2026 19:51:38 GMT
ENV LANG=en_US.UTF-8
# Mon, 02 Mar 2026 19:51:38 GMT
ENV LANGUAGE=en_US.UTF-8
# Mon, 02 Mar 2026 19:51:38 GMT
ENV LC_ALL=en_US.UTF-8
# Mon, 02 Mar 2026 19:51:38 GMT
ENV PING_ON=1
# Mon, 02 Mar 2026 19:51:38 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home # buildkit
# Mon, 02 Mar 2026 19:51:38 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home # buildkit
# Mon, 02 Mar 2026 19:51:38 GMT
ENV JAVA_HOME=/docker-java-home
# Mon, 02 Mar 2026 19:51:38 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Mon, 02 Mar 2026 19:51:38 GMT
ENV JBOSS_HOME=/opt/wildfly
# Mon, 02 Mar 2026 19:51:38 GMT
ENV SILVERPEAS_VERSION=6.4.6
# Mon, 02 Mar 2026 19:51:38 GMT
ENV WILDFLY_VERSION=26.1.3
# Mon, 02 Mar 2026 19:51:38 GMT
LABEL name=Silverpeas 6.4.6 description=Image to install and to run Silverpeas 6.4.6 vendor=Silverpeas version=6.4.6 build=1
# Mon, 02 Mar 2026 19:52:01 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && wget -nc https://www.silverpeas.org/files/oak-migrate.zip   && echo '87009e55520e74b5d2a386f4ebc843ee43cd1f25ca5138f342a94a31add3cfbd oak-migrate.zip' | sha256sum -c --status -   && mkdir -p /opt/oak-migration   && unzip oak-migrate.zip -d /opt/oak-migration/   && chmod +x /opt/oak-migration/oak-migrate.sh   && rm *.zip   && mkdir -p /root/.m2 # buildkit
# Mon, 02 Mar 2026 19:52:01 GMT
COPY src/settings.xml /root/.m2/ # buildkit
# Mon, 02 Mar 2026 19:52:01 GMT
COPY src/silverpeas.gradle /opt/silverpeas/bin/ # buildkit
# Mon, 02 Mar 2026 19:52:01 GMT
WORKDIR /opt/silverpeas/bin
# Mon, 02 Mar 2026 19:52:01 GMT
COPY src/run.sh /opt/ # buildkit
# Mon, 02 Mar 2026 19:52:01 GMT
COPY src/converter.groovy /opt/silverpeas/configuration/silverpeas/ # buildkit
# Mon, 02 Mar 2026 19:53:18 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN set -eux;   sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle;   echo "Construct Silverpeas ${SILVERPEAS_VERSION}";   ./silverpeas assemble || (cat ../log/build-* && exit 1);   rm ../log/build-*;   touch .install; # buildkit
# Mon, 02 Mar 2026 19:53:18 GMT
EXPOSE map[8000/tcp:{} 9990/tcp:{}]
# Mon, 02 Mar 2026 19:53:18 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Mon, 02 Mar 2026 19:53:18 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0adb5934f9d3a6d318c76848166f11c54811440732d30cb955e9e0c7b99fd89c`  
		Last Modified: Mon, 02 Mar 2026 19:55:21 GMT  
		Size: 496.0 MB (496018471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c132d61885d39cde96a9ada3f4ce5648d4be151974d1bf2f0c109c4c5f7c0d7`  
		Last Modified: Mon, 02 Mar 2026 19:54:47 GMT  
		Size: 4.0 MB (3994007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32df9177cf5030733a75a0ba9076a752994a41d113068c97d4defcb9cd78a72`  
		Last Modified: Mon, 02 Mar 2026 19:54:47 GMT  
		Size: 7.1 MB (7146615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65380e613350ca3a2c0ad3587e7a21f1708d747593b9ecdad6fe4ebcd101218e`  
		Last Modified: Mon, 02 Mar 2026 19:54:47 GMT  
		Size: 2.5 MB (2538619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f8dfe222eaff83405a35b137a90e25f7137f311f4c488c87264f14cdbf12a2`  
		Last Modified: Mon, 02 Mar 2026 19:54:48 GMT  
		Size: 236.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17c90550c1c4437400b0b8f1834716b72e30fe3f5b19dcb72c8088856ee6923`  
		Last Modified: Mon, 02 Mar 2026 19:54:48 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c7e3ae94cf7240d3c3eb2b2ec211c2688e5f5519812f55d15ffd99574c900e`  
		Last Modified: Mon, 02 Mar 2026 19:55:11 GMT  
		Size: 269.1 MB (269106250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356826f145122dc3e96c165adf0a12a8c19e0c7ab547930f645b5d9eb7e4e383`  
		Last Modified: Mon, 02 Mar 2026 19:54:49 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c52d385edd64605446627e40fe4e8390d4026d2c7f5fe61dd555b10b635408d`  
		Last Modified: Mon, 02 Mar 2026 19:54:50 GMT  
		Size: 663.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e32af3c1b202279ec413b4a65c4817beee6424d8701fa197b97488fe3fa2968`  
		Last Modified: Mon, 02 Mar 2026 19:54:51 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3118e792fd717f9b763db1aa46569848d63055421d6c572dd8a3ad63547c0acc`  
		Last Modified: Mon, 02 Mar 2026 19:54:51 GMT  
		Size: 384.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818765d25ea070460351f4cc7bb685781703155b297367f80db4ec7556319271`  
		Last Modified: Mon, 02 Mar 2026 19:55:37 GMT  
		Size: 1.0 GB (1010874631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `silverpeas:6.4.6` - unknown; unknown

```console
$ docker pull silverpeas@sha256:6b407d7b5133125ccd31f88511acdf970da98cbe53f43aa1a7ad5030f49934ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16648816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eebdefabf273b22edbe3298019f8ac8ee943b247b130349bc448733cfe26f33e`

```dockerfile
```

-	Layers:
	-	`sha256:c261d4065684284b8cd9cdc99de2e736a708af35d421bf65f3b9f4b67d5809b8`  
		Last Modified: Mon, 02 Mar 2026 19:54:48 GMT  
		Size: 16.6 MB (16606310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:876c7174b02e68e1dc06cd9253ac2c8baa94f66438a42f78e741382fb14e4f6d`  
		Last Modified: Mon, 02 Mar 2026 19:54:46 GMT  
		Size: 42.5 KB (42506 bytes)  
		MIME: application/vnd.in-toto+json

## `silverpeas:latest`

```console
$ docker pull silverpeas@sha256:6d0056d6730b9c26ada884cb572d4f7efed881162803d5e0a4115ca06a15e983
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `silverpeas:latest` - linux; amd64

```console
$ docker pull silverpeas@sha256:51e5b6c302680fef30305effd543dc8e4748e1be65b0713890aca36038111735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1819219255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45b2040d9b6e3a214c2cfdee3723240eef6deb39563dc8dc565456ba10000cf`
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
# Mon, 02 Mar 2026 19:51:10 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Mon, 02 Mar 2026 19:51:10 GMT
ENV TERM=xterm
# Mon, 02 Mar 2026 19:51:10 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends tzdata   && apt-get install -y --no-install-recommends     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f # buildkit
# Mon, 02 Mar 2026 19:51:12 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 swftools-bin-0.9.2.zip' | sha256sum -c --status -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip # buildkit
# Mon, 02 Mar 2026 19:51:15 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 pdf2json-bin-0.68.zip' | sha256sum -c --status -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip # buildkit
# Mon, 02 Mar 2026 19:51:15 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Mon, 02 Mar 2026 19:51:38 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE} # buildkit
# Mon, 02 Mar 2026 19:51:38 GMT
ENV LANG=en_US.UTF-8
# Mon, 02 Mar 2026 19:51:38 GMT
ENV LANGUAGE=en_US.UTF-8
# Mon, 02 Mar 2026 19:51:38 GMT
ENV LC_ALL=en_US.UTF-8
# Mon, 02 Mar 2026 19:51:38 GMT
ENV PING_ON=1
# Mon, 02 Mar 2026 19:51:38 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home # buildkit
# Mon, 02 Mar 2026 19:51:38 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home # buildkit
# Mon, 02 Mar 2026 19:51:38 GMT
ENV JAVA_HOME=/docker-java-home
# Mon, 02 Mar 2026 19:51:38 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Mon, 02 Mar 2026 19:51:38 GMT
ENV JBOSS_HOME=/opt/wildfly
# Mon, 02 Mar 2026 19:51:38 GMT
ENV SILVERPEAS_VERSION=6.4.6
# Mon, 02 Mar 2026 19:51:38 GMT
ENV WILDFLY_VERSION=26.1.3
# Mon, 02 Mar 2026 19:51:38 GMT
LABEL name=Silverpeas 6.4.6 description=Image to install and to run Silverpeas 6.4.6 vendor=Silverpeas version=6.4.6 build=1
# Mon, 02 Mar 2026 19:52:01 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && wget -nc https://www.silverpeas.org/files/oak-migrate.zip   && echo '87009e55520e74b5d2a386f4ebc843ee43cd1f25ca5138f342a94a31add3cfbd oak-migrate.zip' | sha256sum -c --status -   && mkdir -p /opt/oak-migration   && unzip oak-migrate.zip -d /opt/oak-migration/   && chmod +x /opt/oak-migration/oak-migrate.sh   && rm *.zip   && mkdir -p /root/.m2 # buildkit
# Mon, 02 Mar 2026 19:52:01 GMT
COPY src/settings.xml /root/.m2/ # buildkit
# Mon, 02 Mar 2026 19:52:01 GMT
COPY src/silverpeas.gradle /opt/silverpeas/bin/ # buildkit
# Mon, 02 Mar 2026 19:52:01 GMT
WORKDIR /opt/silverpeas/bin
# Mon, 02 Mar 2026 19:52:01 GMT
COPY src/run.sh /opt/ # buildkit
# Mon, 02 Mar 2026 19:52:01 GMT
COPY src/converter.groovy /opt/silverpeas/configuration/silverpeas/ # buildkit
# Mon, 02 Mar 2026 19:53:18 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN set -eux;   sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle;   echo "Construct Silverpeas ${SILVERPEAS_VERSION}";   ./silverpeas assemble || (cat ../log/build-* && exit 1);   rm ../log/build-*;   touch .install; # buildkit
# Mon, 02 Mar 2026 19:53:18 GMT
EXPOSE map[8000/tcp:{} 9990/tcp:{}]
# Mon, 02 Mar 2026 19:53:18 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Mon, 02 Mar 2026 19:53:18 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0adb5934f9d3a6d318c76848166f11c54811440732d30cb955e9e0c7b99fd89c`  
		Last Modified: Mon, 02 Mar 2026 19:55:21 GMT  
		Size: 496.0 MB (496018471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c132d61885d39cde96a9ada3f4ce5648d4be151974d1bf2f0c109c4c5f7c0d7`  
		Last Modified: Mon, 02 Mar 2026 19:54:47 GMT  
		Size: 4.0 MB (3994007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32df9177cf5030733a75a0ba9076a752994a41d113068c97d4defcb9cd78a72`  
		Last Modified: Mon, 02 Mar 2026 19:54:47 GMT  
		Size: 7.1 MB (7146615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65380e613350ca3a2c0ad3587e7a21f1708d747593b9ecdad6fe4ebcd101218e`  
		Last Modified: Mon, 02 Mar 2026 19:54:47 GMT  
		Size: 2.5 MB (2538619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f8dfe222eaff83405a35b137a90e25f7137f311f4c488c87264f14cdbf12a2`  
		Last Modified: Mon, 02 Mar 2026 19:54:48 GMT  
		Size: 236.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17c90550c1c4437400b0b8f1834716b72e30fe3f5b19dcb72c8088856ee6923`  
		Last Modified: Mon, 02 Mar 2026 19:54:48 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c7e3ae94cf7240d3c3eb2b2ec211c2688e5f5519812f55d15ffd99574c900e`  
		Last Modified: Mon, 02 Mar 2026 19:55:11 GMT  
		Size: 269.1 MB (269106250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356826f145122dc3e96c165adf0a12a8c19e0c7ab547930f645b5d9eb7e4e383`  
		Last Modified: Mon, 02 Mar 2026 19:54:49 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c52d385edd64605446627e40fe4e8390d4026d2c7f5fe61dd555b10b635408d`  
		Last Modified: Mon, 02 Mar 2026 19:54:50 GMT  
		Size: 663.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e32af3c1b202279ec413b4a65c4817beee6424d8701fa197b97488fe3fa2968`  
		Last Modified: Mon, 02 Mar 2026 19:54:51 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3118e792fd717f9b763db1aa46569848d63055421d6c572dd8a3ad63547c0acc`  
		Last Modified: Mon, 02 Mar 2026 19:54:51 GMT  
		Size: 384.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818765d25ea070460351f4cc7bb685781703155b297367f80db4ec7556319271`  
		Last Modified: Mon, 02 Mar 2026 19:55:37 GMT  
		Size: 1.0 GB (1010874631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `silverpeas:latest` - unknown; unknown

```console
$ docker pull silverpeas@sha256:6b407d7b5133125ccd31f88511acdf970da98cbe53f43aa1a7ad5030f49934ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16648816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eebdefabf273b22edbe3298019f8ac8ee943b247b130349bc448733cfe26f33e`

```dockerfile
```

-	Layers:
	-	`sha256:c261d4065684284b8cd9cdc99de2e736a708af35d421bf65f3b9f4b67d5809b8`  
		Last Modified: Mon, 02 Mar 2026 19:54:48 GMT  
		Size: 16.6 MB (16606310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:876c7174b02e68e1dc06cd9253ac2c8baa94f66438a42f78e741382fb14e4f6d`  
		Last Modified: Mon, 02 Mar 2026 19:54:46 GMT  
		Size: 42.5 KB (42506 bytes)  
		MIME: application/vnd.in-toto+json
