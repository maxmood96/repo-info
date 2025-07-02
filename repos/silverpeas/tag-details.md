<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `silverpeas`

-	[`silverpeas:6.3.6`](#silverpeas636)
-	[`silverpeas:6.4.3`](#silverpeas643)
-	[`silverpeas:latest`](#silverpeaslatest)

## `silverpeas:6.3.6`

```console
$ docker pull silverpeas@sha256:fd45078184d97696ba802540a10984ee0f33811768d9b91ed127ae33cb62d4f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `silverpeas:6.3.6` - linux; amd64

```console
$ docker pull silverpeas@sha256:e7a04cad16471c8d8613e4f8b25fbd153c6a247d9b75dfb4fcca6acc8cb6b187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1776301272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b766de7acc9aac8e10a20ef903e6712e1e08627f9c1f2d1ec883185cd1b8070`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Fri, 07 Feb 2025 13:19:10 GMT
ARG RELEASE
# Fri, 07 Feb 2025 13:19:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Feb 2025 13:19:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Feb 2025 13:19:10 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 07 Feb 2025 13:19:10 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Fri, 07 Feb 2025 13:19:10 GMT
CMD ["/bin/bash"]
# Fri, 07 Feb 2025 13:19:10 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Fri, 07 Feb 2025 13:19:10 GMT
ENV TERM=xterm
# Fri, 07 Feb 2025 13:19:10 GMT
RUN apt-get update   && apt-get install -y tzdata   && apt-get install -y     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f # buildkit
# Fri, 07 Feb 2025 13:19:10 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip # buildkit
# Fri, 07 Feb 2025 13:19:10 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip # buildkit
# Fri, 07 Feb 2025 13:19:10 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Fri, 07 Feb 2025 13:19:10 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE} # buildkit
# Fri, 07 Feb 2025 13:19:10 GMT
ENV LANG=en_US.UTF-8
# Fri, 07 Feb 2025 13:19:10 GMT
ENV LANGUAGE=en_US.UTF-8
# Fri, 07 Feb 2025 13:19:10 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 07 Feb 2025 13:19:10 GMT
ENV PING_ON=1
# Fri, 07 Feb 2025 13:19:10 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home # buildkit
# Fri, 07 Feb 2025 13:19:10 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home # buildkit
# Fri, 07 Feb 2025 13:19:10 GMT
ENV JAVA_HOME=/docker-java-home
# Fri, 07 Feb 2025 13:19:10 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Fri, 07 Feb 2025 13:19:10 GMT
ENV JBOSS_HOME=/opt/wildfly
# Fri, 07 Feb 2025 13:19:10 GMT
ENV SILVERPEAS_VERSION=6.3.6
# Fri, 07 Feb 2025 13:19:10 GMT
ENV WILDFLY_VERSION=26.1.1
# Fri, 07 Feb 2025 13:19:10 GMT
LABEL name=Silverpeas 6.3.6 description=Image to install and to run Silverpeas 6.3.6 vendor=Silverpeas version=6.3.6 build=1
# Fri, 07 Feb 2025 13:19:10 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2 # buildkit
# Fri, 07 Feb 2025 13:19:10 GMT
COPY src/settings.xml /root/.m2/ # buildkit
# Fri, 07 Feb 2025 13:19:10 GMT
COPY src/silverpeas.gradle /opt/silverpeas/bin/ # buildkit
# Fri, 07 Feb 2025 13:19:10 GMT
WORKDIR /opt/silverpeas/bin
# Fri, 07 Feb 2025 13:19:10 GMT
COPY src/run.sh /opt/ # buildkit
# Fri, 07 Feb 2025 13:19:10 GMT
COPY src/converter.groovy /opt/silverpeas/configuration/silverpeas/ # buildkit
# Fri, 07 Feb 2025 13:19:10 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle   && ./silverpeas construct   && rm ../log/build-*   && touch .install # buildkit
# Fri, 07 Feb 2025 13:19:10 GMT
EXPOSE map[8000/tcp:{} 9990/tcp:{}]
# Fri, 07 Feb 2025 13:19:10 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Fri, 07 Feb 2025 13:19:10 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e9d292ebf7d7c8cc8d916ae591cc751e95bd0687d30dd7f0eea47fd6041f5e`  
		Last Modified: Sat, 17 May 2025 16:51:45 GMT  
		Size: 762.6 MB (762649442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8cd56b849084c23ce23abbe3580033492dc42c22e5bf517d1b38987fd4a7657`  
		Last Modified: Sat, 17 May 2025 16:51:36 GMT  
		Size: 4.0 MB (3994011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd98c7412b53373ca88561f2bf76bc58954699af6b45782635f05fe319605b9`  
		Last Modified: Sat, 17 May 2025 16:51:36 GMT  
		Size: 7.1 MB (7146628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844a5f3aeb3268f18f674a6b18504342a2d89cd7cade4fd9f1240c0c95b20e16`  
		Last Modified: Sat, 17 May 2025 16:51:37 GMT  
		Size: 2.5 MB (2534359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87df7b140611c5d1cfe8079fac5709cf41acdbb712fabf1baa2d50411b5615be`  
		Last Modified: Sat, 17 May 2025 16:51:38 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e489e89ad46a882374d347f7e4f0010061795382bc08ca2f13fc4e23b4e2ca`  
		Last Modified: Sat, 17 May 2025 16:51:38 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302f3e1794e044a114aec8980fdd8871ddf3294a2dc1cf925016082c1a9df6cf`  
		Last Modified: Sat, 17 May 2025 16:51:55 GMT  
		Size: 217.8 MB (217843308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b4b9338e2b65e0c770919df1c4a4dab6737a93bfcc6ef66f75048ff05a5803`  
		Last Modified: Sat, 17 May 2025 16:51:39 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770fde9ba44a2910c06b8a2038f1fb9a47db9bd28d9d1bab88ac188636a41346`  
		Last Modified: Sat, 17 May 2025 16:51:40 GMT  
		Size: 661.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bb8081ae57930ececc71b2172534a9f6987e082aa7718d6ec10cfab89b516b`  
		Last Modified: Sat, 17 May 2025 16:51:41 GMT  
		Size: 921.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79609d21a65916615a6a87834278155ab53a9f275cedc52cb8f8bc08617bb28b`  
		Last Modified: Sat, 17 May 2025 16:51:41 GMT  
		Size: 385.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a0fea8d28c71e93be2754405385abe66b692767fe832bd3868340829bdcdf6`  
		Last Modified: Sat, 17 May 2025 16:51:52 GMT  
		Size: 754.6 MB (754620360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `silverpeas:6.3.6` - unknown; unknown

```console
$ docker pull silverpeas@sha256:0f8837349af75ff3cf15728640721965008a8e9b572366f0354bd7b1128ba2aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.8 MB (27780373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b46640cdd9950a6e500571667b7695956337dab06d3caa7527faacecd0267d9a`

```dockerfile
```

-	Layers:
	-	`sha256:0c89231b91ab0ff439cabf53bf437864083f8b8fe28f78915bd542bda8d6f24d`  
		Last Modified: Tue, 17 Jun 2025 13:57:36 GMT  
		Size: 27.7 MB (27739630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee73558331b89d201c25c0c24dc2f133f6c43954ae0bbe042f085be6d9c1bddd`  
		Last Modified: Tue, 17 Jun 2025 13:57:38 GMT  
		Size: 40.7 KB (40743 bytes)  
		MIME: application/vnd.in-toto+json

## `silverpeas:6.4.3`

```console
$ docker pull silverpeas@sha256:9bd8be24e9a295e3b8f94bf7e879a42e82d5e395f0f98560242e5dbddaa14ab8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `silverpeas:6.4.3` - linux; amd64

```console
$ docker pull silverpeas@sha256:5afaa28acd3339ab89cac40b77e351604eaf5fd6027595a86e3ca6f9388f10d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1817861943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff5ff53b4ba00b7f9c0209a25006d1ae5dd9f7df1ae3034ee9da8ec10763b04f`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Fri, 11 Apr 2025 14:37:01 GMT
ARG RELEASE
# Fri, 11 Apr 2025 14:37:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Apr 2025 14:37:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Apr 2025 14:37:01 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 11 Apr 2025 14:37:01 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 11 Apr 2025 14:37:01 GMT
CMD ["/bin/bash"]
# Fri, 11 Apr 2025 14:37:01 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Fri, 11 Apr 2025 14:37:01 GMT
ENV TERM=xterm
# Fri, 11 Apr 2025 14:37:01 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends tzdata   && apt-get install -y --no-install-recommends     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 swftools-bin-0.9.2.zip' | sha256sum -c --status -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 pdf2json-bin-0.68.zip' | sha256sum -c --status -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Fri, 11 Apr 2025 14:37:01 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE} # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
ENV LANG=en_US.UTF-8
# Fri, 11 Apr 2025 14:37:01 GMT
ENV LANGUAGE=en_US.UTF-8
# Fri, 11 Apr 2025 14:37:01 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 11 Apr 2025 14:37:01 GMT
ENV PING_ON=1
# Fri, 11 Apr 2025 14:37:01 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
ENV JAVA_HOME=/docker-java-home
# Fri, 11 Apr 2025 14:37:01 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Fri, 11 Apr 2025 14:37:01 GMT
ENV JBOSS_HOME=/opt/wildfly
# Fri, 11 Apr 2025 14:37:01 GMT
ENV SILVERPEAS_VERSION=6.4.3
# Fri, 11 Apr 2025 14:37:01 GMT
ENV WILDFLY_VERSION=26.1.3
# Fri, 11 Apr 2025 14:37:01 GMT
LABEL name=Silverpeas 6.4.3 description=Image to install and to run Silverpeas 6.4.3 vendor=Silverpeas version=6.4.3 build=1
# Fri, 11 Apr 2025 14:37:01 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && wget -nc https://www.silverpeas.org/files/oak-migrate.zip   && echo '87009e55520e74b5d2a386f4ebc843ee43cd1f25ca5138f342a94a31add3cfbd oak-migrate.zip' | sha256sum -c --status -   && mkdir -p /opt/oak-migration   && unzip oak-migrate.zip -d /opt/oak-migration/   && chmod +x /opt/oak-migration/oak-migrate.sh   && rm *.zip   && mkdir -p /root/.m2 # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
COPY src/settings.xml /root/.m2/ # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
COPY src/silverpeas.gradle /opt/silverpeas/bin/ # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
WORKDIR /opt/silverpeas/bin
# Fri, 11 Apr 2025 14:37:01 GMT
COPY src/run.sh /opt/ # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
COPY src/converter.groovy /opt/silverpeas/configuration/silverpeas/ # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN set -eux;   sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle;   echo "Construct Silverpeas ${SILVERPEAS_VERSION}";   ./silverpeas assemble || (cat ../log/build-* && exit 1);   rm ../log/build-*;   touch .install; # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
EXPOSE map[8000/tcp:{} 9990/tcp:{}]
# Fri, 11 Apr 2025 14:37:01 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Fri, 11 Apr 2025 14:37:01 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62d6f0745606032c8b790868c0aa698e5eed8feba72deb8c37030903989c02e`  
		Last Modified: Wed, 02 Jul 2025 08:55:31 GMT  
		Size: 494.8 MB (494757559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74eeab2003b6035f590af1f80a2af50cccbd0d3899ca3a9c2fbd75b743435b6`  
		Last Modified: Wed, 02 Jul 2025 03:19:17 GMT  
		Size: 4.0 MB (3994014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687a893569f11ffb58714724de18087d5d302e4dbb38f49ba63aa95630d6e75e`  
		Last Modified: Wed, 02 Jul 2025 03:19:17 GMT  
		Size: 7.1 MB (7146610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d0c08db250b1e6054de1512695e81d38288b86aed137f555855abdc39ee4ac`  
		Last Modified: Wed, 02 Jul 2025 03:19:18 GMT  
		Size: 2.5 MB (2538610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb03fc25bb52a9d8dba2841676c74befb17d3f63e574e3ab6fd88a6759adb5c6`  
		Last Modified: Wed, 02 Jul 2025 03:19:16 GMT  
		Size: 236.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:722957af25c51acbbe377e084b71d9c77c0dd642b355e2a2853d3501f6cd29cd`  
		Last Modified: Wed, 02 Jul 2025 03:19:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87cba23d7048447b34732f084f6e398c15a2a40d363dc7fe1deb633f48fe9153`  
		Last Modified: Wed, 02 Jul 2025 08:55:24 GMT  
		Size: 269.1 MB (269106191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca86c7da813c8e34887c56c89a0944a838456e1ee48ba429ebbff710bea381f`  
		Last Modified: Wed, 02 Jul 2025 03:19:16 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa9cb8285179d1d1110566ca82d134174382be339dfa404f6904503af850184`  
		Last Modified: Wed, 02 Jul 2025 03:19:16 GMT  
		Size: 659.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2960f2081b96090aab5f41593364ad7c896542296d24a6f7c755204e26c078bf`  
		Last Modified: Wed, 02 Jul 2025 03:19:17 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e93ec2196d61e0cb3cc32bdd14a7079d23eb1dcad752ba67f1b97dea80e19d`  
		Last Modified: Wed, 02 Jul 2025 03:19:16 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ba3f269f3a9d946a798fbdc015024ddf55c3ccd3f36b1ff53f2c8258e01da2`  
		Last Modified: Wed, 02 Jul 2025 08:55:31 GMT  
		Size: 1.0 GB (1010779981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `silverpeas:6.4.3` - unknown; unknown

```console
$ docker pull silverpeas@sha256:bef958d8161d1d232323800def8aac0ea4a04e61a1da92bfef3b99e191197965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16648660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d8d226fdc1e2151649c2b075845d8880cdd8c8776a7a54d9b035395e417ec4f`

```dockerfile
```

-	Layers:
	-	`sha256:a4381b6bd7d06288003370abbcdcc85ebe0a268b7ebd0220b98660dcaec169d7`  
		Last Modified: Wed, 02 Jul 2025 07:09:20 GMT  
		Size: 16.6 MB (16606111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:267d26c4fb2cede74d516ec3871911476036b62bd6c7d2f7c6ccb753f001d4ff`  
		Last Modified: Wed, 02 Jul 2025 07:09:21 GMT  
		Size: 42.5 KB (42549 bytes)  
		MIME: application/vnd.in-toto+json

## `silverpeas:latest`

```console
$ docker pull silverpeas@sha256:9bd8be24e9a295e3b8f94bf7e879a42e82d5e395f0f98560242e5dbddaa14ab8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `silverpeas:latest` - linux; amd64

```console
$ docker pull silverpeas@sha256:5afaa28acd3339ab89cac40b77e351604eaf5fd6027595a86e3ca6f9388f10d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1817861943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff5ff53b4ba00b7f9c0209a25006d1ae5dd9f7df1ae3034ee9da8ec10763b04f`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Fri, 11 Apr 2025 14:37:01 GMT
ARG RELEASE
# Fri, 11 Apr 2025 14:37:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Apr 2025 14:37:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Apr 2025 14:37:01 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 11 Apr 2025 14:37:01 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 11 Apr 2025 14:37:01 GMT
CMD ["/bin/bash"]
# Fri, 11 Apr 2025 14:37:01 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Fri, 11 Apr 2025 14:37:01 GMT
ENV TERM=xterm
# Fri, 11 Apr 2025 14:37:01 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends tzdata   && apt-get install -y --no-install-recommends     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 swftools-bin-0.9.2.zip' | sha256sum -c --status -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 pdf2json-bin-0.68.zip' | sha256sum -c --status -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Fri, 11 Apr 2025 14:37:01 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE} # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
ENV LANG=en_US.UTF-8
# Fri, 11 Apr 2025 14:37:01 GMT
ENV LANGUAGE=en_US.UTF-8
# Fri, 11 Apr 2025 14:37:01 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 11 Apr 2025 14:37:01 GMT
ENV PING_ON=1
# Fri, 11 Apr 2025 14:37:01 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
ENV JAVA_HOME=/docker-java-home
# Fri, 11 Apr 2025 14:37:01 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Fri, 11 Apr 2025 14:37:01 GMT
ENV JBOSS_HOME=/opt/wildfly
# Fri, 11 Apr 2025 14:37:01 GMT
ENV SILVERPEAS_VERSION=6.4.3
# Fri, 11 Apr 2025 14:37:01 GMT
ENV WILDFLY_VERSION=26.1.3
# Fri, 11 Apr 2025 14:37:01 GMT
LABEL name=Silverpeas 6.4.3 description=Image to install and to run Silverpeas 6.4.3 vendor=Silverpeas version=6.4.3 build=1
# Fri, 11 Apr 2025 14:37:01 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && wget -nc https://www.silverpeas.org/files/oak-migrate.zip   && echo '87009e55520e74b5d2a386f4ebc843ee43cd1f25ca5138f342a94a31add3cfbd oak-migrate.zip' | sha256sum -c --status -   && mkdir -p /opt/oak-migration   && unzip oak-migrate.zip -d /opt/oak-migration/   && chmod +x /opt/oak-migration/oak-migrate.sh   && rm *.zip   && mkdir -p /root/.m2 # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
COPY src/settings.xml /root/.m2/ # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
COPY src/silverpeas.gradle /opt/silverpeas/bin/ # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
WORKDIR /opt/silverpeas/bin
# Fri, 11 Apr 2025 14:37:01 GMT
COPY src/run.sh /opt/ # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
COPY src/converter.groovy /opt/silverpeas/configuration/silverpeas/ # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN set -eux;   sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle;   echo "Construct Silverpeas ${SILVERPEAS_VERSION}";   ./silverpeas assemble || (cat ../log/build-* && exit 1);   rm ../log/build-*;   touch .install; # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
EXPOSE map[8000/tcp:{} 9990/tcp:{}]
# Fri, 11 Apr 2025 14:37:01 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Fri, 11 Apr 2025 14:37:01 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62d6f0745606032c8b790868c0aa698e5eed8feba72deb8c37030903989c02e`  
		Last Modified: Wed, 02 Jul 2025 08:55:31 GMT  
		Size: 494.8 MB (494757559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74eeab2003b6035f590af1f80a2af50cccbd0d3899ca3a9c2fbd75b743435b6`  
		Last Modified: Wed, 02 Jul 2025 03:19:17 GMT  
		Size: 4.0 MB (3994014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687a893569f11ffb58714724de18087d5d302e4dbb38f49ba63aa95630d6e75e`  
		Last Modified: Wed, 02 Jul 2025 03:19:17 GMT  
		Size: 7.1 MB (7146610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d0c08db250b1e6054de1512695e81d38288b86aed137f555855abdc39ee4ac`  
		Last Modified: Wed, 02 Jul 2025 03:19:18 GMT  
		Size: 2.5 MB (2538610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb03fc25bb52a9d8dba2841676c74befb17d3f63e574e3ab6fd88a6759adb5c6`  
		Last Modified: Wed, 02 Jul 2025 03:19:16 GMT  
		Size: 236.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:722957af25c51acbbe377e084b71d9c77c0dd642b355e2a2853d3501f6cd29cd`  
		Last Modified: Wed, 02 Jul 2025 03:19:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87cba23d7048447b34732f084f6e398c15a2a40d363dc7fe1deb633f48fe9153`  
		Last Modified: Wed, 02 Jul 2025 08:55:24 GMT  
		Size: 269.1 MB (269106191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca86c7da813c8e34887c56c89a0944a838456e1ee48ba429ebbff710bea381f`  
		Last Modified: Wed, 02 Jul 2025 03:19:16 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa9cb8285179d1d1110566ca82d134174382be339dfa404f6904503af850184`  
		Last Modified: Wed, 02 Jul 2025 03:19:16 GMT  
		Size: 659.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2960f2081b96090aab5f41593364ad7c896542296d24a6f7c755204e26c078bf`  
		Last Modified: Wed, 02 Jul 2025 03:19:17 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e93ec2196d61e0cb3cc32bdd14a7079d23eb1dcad752ba67f1b97dea80e19d`  
		Last Modified: Wed, 02 Jul 2025 03:19:16 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ba3f269f3a9d946a798fbdc015024ddf55c3ccd3f36b1ff53f2c8258e01da2`  
		Last Modified: Wed, 02 Jul 2025 08:55:31 GMT  
		Size: 1.0 GB (1010779981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `silverpeas:latest` - unknown; unknown

```console
$ docker pull silverpeas@sha256:bef958d8161d1d232323800def8aac0ea4a04e61a1da92bfef3b99e191197965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16648660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d8d226fdc1e2151649c2b075845d8880cdd8c8776a7a54d9b035395e417ec4f`

```dockerfile
```

-	Layers:
	-	`sha256:a4381b6bd7d06288003370abbcdcc85ebe0a268b7ebd0220b98660dcaec169d7`  
		Last Modified: Wed, 02 Jul 2025 07:09:20 GMT  
		Size: 16.6 MB (16606111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:267d26c4fb2cede74d516ec3871911476036b62bd6c7d2f7c6ccb753f001d4ff`  
		Last Modified: Wed, 02 Jul 2025 07:09:21 GMT  
		Size: 42.5 KB (42549 bytes)  
		MIME: application/vnd.in-toto+json
