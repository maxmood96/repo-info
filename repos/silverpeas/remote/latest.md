## `silverpeas:latest`

```console
$ docker pull silverpeas@sha256:8e39ec2d27a8386f1cf9a397bf09eb1992f0c8ac2240ffd678cf8b67643283a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `silverpeas:latest` - linux; amd64

```console
$ docker pull silverpeas@sha256:06a0e6d2ae97d0c3f9df96cb23fe0feb107e12544568f8b41298fbea7513d40c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1817986085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:140f8a0479c70a3da04edf27c244c5db90d4c5a73cae96eba3c1bea6990b56e2`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Thu, 07 Aug 2025 14:33:54 GMT
ARG RELEASE
# Thu, 07 Aug 2025 14:33:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 07 Aug 2025 14:33:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 07 Aug 2025 14:33:54 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 07 Aug 2025 14:33:54 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Thu, 07 Aug 2025 14:33:54 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 14:33:54 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Thu, 07 Aug 2025 14:33:54 GMT
ENV TERM=xterm
# Thu, 07 Aug 2025 14:33:54 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends tzdata   && apt-get install -y --no-install-recommends     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f # buildkit
# Thu, 07 Aug 2025 14:33:54 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 swftools-bin-0.9.2.zip' | sha256sum -c --status -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip # buildkit
# Thu, 07 Aug 2025 14:33:54 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 pdf2json-bin-0.68.zip' | sha256sum -c --status -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip # buildkit
# Thu, 07 Aug 2025 14:33:54 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Thu, 07 Aug 2025 14:33:54 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE} # buildkit
# Thu, 07 Aug 2025 14:33:54 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 14:33:54 GMT
ENV LANGUAGE=en_US.UTF-8
# Thu, 07 Aug 2025 14:33:54 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 07 Aug 2025 14:33:54 GMT
ENV PING_ON=1
# Thu, 07 Aug 2025 14:33:54 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home # buildkit
# Thu, 07 Aug 2025 14:33:54 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home # buildkit
# Thu, 07 Aug 2025 14:33:54 GMT
ENV JAVA_HOME=/docker-java-home
# Thu, 07 Aug 2025 14:33:54 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Thu, 07 Aug 2025 14:33:54 GMT
ENV JBOSS_HOME=/opt/wildfly
# Thu, 07 Aug 2025 14:33:54 GMT
ENV SILVERPEAS_VERSION=6.4.4
# Thu, 07 Aug 2025 14:33:54 GMT
ENV WILDFLY_VERSION=26.1.3
# Thu, 07 Aug 2025 14:33:54 GMT
LABEL name=Silverpeas 6.4.4 description=Image to install and to run Silverpeas 6.4.4 vendor=Silverpeas version=6.4.4 build=1
# Thu, 07 Aug 2025 14:33:54 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && wget -nc https://www.silverpeas.org/files/oak-migrate.zip   && echo '87009e55520e74b5d2a386f4ebc843ee43cd1f25ca5138f342a94a31add3cfbd oak-migrate.zip' | sha256sum -c --status -   && mkdir -p /opt/oak-migration   && unzip oak-migrate.zip -d /opt/oak-migration/   && chmod +x /opt/oak-migration/oak-migrate.sh   && rm *.zip   && mkdir -p /root/.m2 # buildkit
# Thu, 07 Aug 2025 14:33:54 GMT
COPY src/settings.xml /root/.m2/ # buildkit
# Thu, 07 Aug 2025 14:33:54 GMT
COPY src/silverpeas.gradle /opt/silverpeas/bin/ # buildkit
# Thu, 07 Aug 2025 14:33:54 GMT
WORKDIR /opt/silverpeas/bin
# Thu, 07 Aug 2025 14:33:54 GMT
COPY src/run.sh /opt/ # buildkit
# Thu, 07 Aug 2025 14:33:54 GMT
COPY src/converter.groovy /opt/silverpeas/configuration/silverpeas/ # buildkit
# Thu, 07 Aug 2025 14:33:54 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN set -eux;   sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle;   echo "Construct Silverpeas ${SILVERPEAS_VERSION}";   ./silverpeas assemble || (cat ../log/build-* && exit 1);   rm ../log/build-*;   touch .install; # buildkit
# Thu, 07 Aug 2025 14:33:54 GMT
EXPOSE map[8000/tcp:{} 9990/tcp:{}]
# Thu, 07 Aug 2025 14:33:54 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Thu, 07 Aug 2025 14:33:54 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7009282f7fdad0b6312f451d8cbe5e02a5517da079e9fd57a806ee7fcba422bf`  
		Last Modified: Thu, 02 Oct 2025 07:09:48 GMT  
		Size: 494.8 MB (494796613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef7d4f0716ffb43a90cd8c29fc52fb0f221d0113feaebe86200c04b7ded66af`  
		Last Modified: Thu, 02 Oct 2025 05:26:18 GMT  
		Size: 4.0 MB (3994015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862361a07976b25ccd65366584d533c6a000045a6ca407341adf6377c89e1e98`  
		Last Modified: Thu, 02 Oct 2025 05:26:19 GMT  
		Size: 7.1 MB (7146623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95dfa5bc60824d7623ac622479babca24b34b863d7be433c4dcfc531cd8dcc00`  
		Last Modified: Thu, 02 Oct 2025 05:26:20 GMT  
		Size: 2.5 MB (2538616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c1b9b4d85453a603431359c4d65a69775a6eb93c4f5d7b68d508dd1513df9a`  
		Last Modified: Thu, 02 Oct 2025 05:26:18 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e72a6a8170b3e45dc14c2ab4899140b889d6ab4ce10a5b7baefce9bf6ca253`  
		Last Modified: Thu, 02 Oct 2025 05:26:18 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f60eede6d2bb3a5459b6ce2660c324efb68261946d527bd6f414e65a1821fb`  
		Last Modified: Thu, 02 Oct 2025 07:09:49 GMT  
		Size: 269.1 MB (269106246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72604fe0fdf03439de5c139cd40b372d909ea1e2d542f75cec85f97a203f5bd4`  
		Last Modified: Thu, 02 Oct 2025 05:26:19 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14a78569d5fc74b68fb1a63503f4e920ba8b6af509150738ad1708210c565be`  
		Last Modified: Thu, 02 Oct 2025 05:26:18 GMT  
		Size: 664.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aab4f3b579286c01d0456e1423e7b0fbf004dd2377aacae947b4715c233dc20`  
		Last Modified: Thu, 02 Oct 2025 05:26:18 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd172e88144f75059d76fcdbce279b2e90965d34f7cd32a6e05f86d7da3e6ff`  
		Last Modified: Thu, 02 Oct 2025 05:26:18 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbfca043a12bdd5a1d83887356a2571d02ae62e9661ee16e6252b8316324bfa`  
		Last Modified: Thu, 02 Oct 2025 05:26:12 GMT  
		Size: 1.0 GB (1010863855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `silverpeas:latest` - unknown; unknown

```console
$ docker pull silverpeas@sha256:9fa1ce061c3351763c7368640d30d36bd09cdb58620061de39166b771c8eb023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16648746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d5216ee0db1d52a5bf34e9d9915116225b3995ea63a999d019aa5e6cebf16e`

```dockerfile
```

-	Layers:
	-	`sha256:7b244a416a163b6f7a018966679883c5fd63d43d42b456d0e903369e9be9409c`  
		Last Modified: Thu, 02 Oct 2025 07:09:28 GMT  
		Size: 16.6 MB (16606197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29eb04c7485a96fc43dddafa37b5d27aa251f783c58a9cb753e97fe7fb28b813`  
		Last Modified: Thu, 02 Oct 2025 07:09:29 GMT  
		Size: 42.5 KB (42549 bytes)  
		MIME: application/vnd.in-toto+json
