## `silverpeas:latest`

```console
$ docker pull silverpeas@sha256:741ef04147bd70056ed8099d8b389726561a9036c739c8b295ead258c338f71e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `silverpeas:latest` - linux; amd64

```console
$ docker pull silverpeas@sha256:1bb3eaff634a89bf9f6a93fff8158cc0af6df9dd63b39f2d6112cc3189a904b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818021186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64664721a2c575511fd1cffaf469f67bd76bdff69fc79c1bad1f3f2fe4f79929`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Mon, 08 Dec 2025 19:23:50 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Mon, 08 Dec 2025 19:23:50 GMT
ENV TERM=xterm
# Mon, 08 Dec 2025 19:23:50 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends tzdata   && apt-get install -y --no-install-recommends     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f # buildkit
# Mon, 08 Dec 2025 19:23:52 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 swftools-bin-0.9.2.zip' | sha256sum -c --status -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip # buildkit
# Mon, 08 Dec 2025 19:23:54 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 pdf2json-bin-0.68.zip' | sha256sum -c --status -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip # buildkit
# Mon, 08 Dec 2025 19:23:54 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Mon, 08 Dec 2025 19:24:18 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE} # buildkit
# Mon, 08 Dec 2025 19:24:18 GMT
ENV LANG=en_US.UTF-8
# Mon, 08 Dec 2025 19:24:18 GMT
ENV LANGUAGE=en_US.UTF-8
# Mon, 08 Dec 2025 19:24:18 GMT
ENV LC_ALL=en_US.UTF-8
# Mon, 08 Dec 2025 19:24:18 GMT
ENV PING_ON=1
# Mon, 08 Dec 2025 19:24:18 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home # buildkit
# Mon, 08 Dec 2025 19:24:18 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home # buildkit
# Mon, 08 Dec 2025 19:24:18 GMT
ENV JAVA_HOME=/docker-java-home
# Mon, 08 Dec 2025 19:24:18 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Mon, 08 Dec 2025 19:24:18 GMT
ENV JBOSS_HOME=/opt/wildfly
# Mon, 08 Dec 2025 19:24:18 GMT
ENV SILVERPEAS_VERSION=6.4.5
# Mon, 08 Dec 2025 19:24:18 GMT
ENV WILDFLY_VERSION=26.1.3
# Mon, 08 Dec 2025 19:24:18 GMT
LABEL name=Silverpeas 6.4.5 description=Image to install and to run Silverpeas 6.4.5 vendor=Silverpeas version=6.4.5 build=1
# Mon, 08 Dec 2025 19:24:41 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && wget -nc https://www.silverpeas.org/files/oak-migrate.zip   && echo '87009e55520e74b5d2a386f4ebc843ee43cd1f25ca5138f342a94a31add3cfbd oak-migrate.zip' | sha256sum -c --status -   && mkdir -p /opt/oak-migration   && unzip oak-migrate.zip -d /opt/oak-migration/   && chmod +x /opt/oak-migration/oak-migrate.sh   && rm *.zip   && mkdir -p /root/.m2 # buildkit
# Mon, 08 Dec 2025 19:24:41 GMT
COPY src/settings.xml /root/.m2/ # buildkit
# Mon, 08 Dec 2025 19:24:41 GMT
COPY src/silverpeas.gradle /opt/silverpeas/bin/ # buildkit
# Mon, 08 Dec 2025 19:24:41 GMT
WORKDIR /opt/silverpeas/bin
# Mon, 08 Dec 2025 19:24:41 GMT
COPY src/run.sh /opt/ # buildkit
# Mon, 08 Dec 2025 19:24:41 GMT
COPY src/converter.groovy /opt/silverpeas/configuration/silverpeas/ # buildkit
# Mon, 08 Dec 2025 19:25:56 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN set -eux;   sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle;   echo "Construct Silverpeas ${SILVERPEAS_VERSION}";   ./silverpeas assemble || (cat ../log/build-* && exit 1);   rm ../log/build-*;   touch .install; # buildkit
# Mon, 08 Dec 2025 19:25:56 GMT
EXPOSE map[8000/tcp:{} 9990/tcp:{}]
# Mon, 08 Dec 2025 19:25:56 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Mon, 08 Dec 2025 19:25:56 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f54fdb6e92b37b584c0028be76feacfcdf6b76eb7c53495dd4eee1dc2e8c923`  
		Last Modified: Mon, 08 Dec 2025 20:04:07 GMT  
		Size: 494.8 MB (494826907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a45c63453d8fe50c39b83bbd0e130a880d753858e47c849a4e18a5cdcb01723`  
		Last Modified: Mon, 08 Dec 2025 20:02:35 GMT  
		Size: 4.0 MB (3994007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7603ea3ed846026ecfef1d47076f4576fd515bdcfaebecaa65e7593221c61d37`  
		Last Modified: Mon, 08 Dec 2025 20:02:35 GMT  
		Size: 7.1 MB (7146599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156272c2950fbfc533c1ed8ae0fd2dd8b39e6b9f2bfac9cba33df0b4c304d141`  
		Last Modified: Mon, 08 Dec 2025 20:02:35 GMT  
		Size: 2.5 MB (2538620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81049ed12467ea0048d53b238836a2699ab7daa586b662121749c0e326b614c8`  
		Last Modified: Mon, 08 Dec 2025 20:02:34 GMT  
		Size: 237.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a7d560e7914cf30929b36714e6801be188381bc183258c5d84707252e01ebe`  
		Last Modified: Mon, 08 Dec 2025 20:02:34 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76fcb4307acb5b24b8781f694d233a7a81e761de302fbf4b6dc743ee74410060`  
		Last Modified: Mon, 08 Dec 2025 20:04:20 GMT  
		Size: 269.1 MB (269106197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7926b97b7ec878e70b27a5598dc5e4c98d08276a67d76474ce486708e12f213b`  
		Last Modified: Mon, 08 Dec 2025 20:02:34 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109db5c069076e58a475bc6ac5c1efe0456d9466567b3f34440b7ae04e6646f6`  
		Last Modified: Mon, 08 Dec 2025 20:02:34 GMT  
		Size: 661.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a9bdb8fe2fe08176a0a1c36a1f01923456b26d6039cd80903a81209b171378`  
		Last Modified: Mon, 08 Dec 2025 20:02:34 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9aff068f136286e57b5471d87c46004a040a4bc27330069890256eb2e34a4d`  
		Last Modified: Mon, 08 Dec 2025 20:02:35 GMT  
		Size: 383.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45e04c24569ddfcb14a38adbf62c5ffd4a0375b03abf2224c22ed5143b0d97b4`  
		Last Modified: Mon, 08 Dec 2025 20:04:24 GMT  
		Size: 1.0 GB (1010868762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `silverpeas:latest` - unknown; unknown

```console
$ docker pull silverpeas@sha256:a0db9e836b7071f5e2ccc38f39bdd292a889aa669ec67ac3263b4a11d06b372e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16648731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d58c00688ff0ab1b1adb5dd1774bcfc0768e29c8bc8ce7c09fab1d3455afcfa`

```dockerfile
```

-	Layers:
	-	`sha256:52acdc01312f0f5565c433c26e3ce92fc5ac9be1e11ec3dbfdb8f70ff46ec22d`  
		Last Modified: Mon, 08 Dec 2025 20:09:22 GMT  
		Size: 16.6 MB (16606225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0a462a5708698afbab9c4dc55d86340ef4db43acb1f9403fe64a51b27cf3a2b`  
		Last Modified: Mon, 08 Dec 2025 20:09:23 GMT  
		Size: 42.5 KB (42506 bytes)  
		MIME: application/vnd.in-toto+json
