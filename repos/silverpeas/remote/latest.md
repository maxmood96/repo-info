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
