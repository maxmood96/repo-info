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
