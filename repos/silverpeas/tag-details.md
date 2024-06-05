<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `silverpeas`

-	[`silverpeas:6.3.5`](#silverpeas635)
-	[`silverpeas:latest`](#silverpeaslatest)

## `silverpeas:6.3.5`

```console
$ docker pull silverpeas@sha256:7b8e5c03079a1b2e8a4d6bb45bba2af7fdc7fcfcb922e0b773c83aabf17737f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `silverpeas:6.3.5` - linux; amd64

```console
$ docker pull silverpeas@sha256:16e87532ff17f224ab0ecabb3a8b5ad9a067a1bdba47125c9830e7ab25541e64
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1777196611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22b396df20749b65ffb6254842e04ba93e00c718e3517c8775e08972d0540c00`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:03:40 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Wed, 05 Jun 2024 05:03:40 GMT
ENV TERM=xterm
# Wed, 05 Jun 2024 05:10:48 GMT
RUN apt-get update   && apt-get install -y tzdata   && apt-get install -y     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Wed, 05 Jun 2024 05:10:54 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Wed, 05 Jun 2024 05:10:57 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Wed, 05 Jun 2024 05:10:58 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Wed, 05 Jun 2024 05:11:37 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Wed, 05 Jun 2024 05:11:38 GMT
ENV LANG=en_US.UTF-8
# Wed, 05 Jun 2024 05:11:38 GMT
ENV LANGUAGE=en_US.UTF-8
# Wed, 05 Jun 2024 05:11:38 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 05 Jun 2024 05:11:38 GMT
ENV PING_ON=1
# Wed, 05 Jun 2024 05:11:38 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 05 Jun 2024 05:11:39 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 05 Jun 2024 05:11:39 GMT
ENV JAVA_HOME=/docker-java-home
# Wed, 05 Jun 2024 05:11:39 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Wed, 05 Jun 2024 05:11:39 GMT
ENV JBOSS_HOME=/opt/wildfly
# Wed, 05 Jun 2024 05:11:39 GMT
ENV SILVERPEAS_VERSION=6.3.5
# Wed, 05 Jun 2024 05:11:40 GMT
ENV WILDFLY_VERSION=26.1.1
# Wed, 05 Jun 2024 05:11:40 GMT
LABEL name=Silverpeas 6.3.5 description=Image to install and to run Silverpeas 6.3.5 vendor=Silverpeas version=6.3.5 build=1
# Wed, 05 Jun 2024 05:12:03 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Wed, 05 Jun 2024 05:12:03 GMT
COPY file:bdea684cbb56f9ec67736214361c476c97d0a0e06ec936f53a7da778776f533b in /root/.m2/ 
# Wed, 05 Jun 2024 05:12:04 GMT
COPY file:473bf75b335a39b6b4b39c64cd151bd8ed3d3e33da73b8124e537a5db1fad3d6 in /opt/silverpeas/bin/ 
# Wed, 05 Jun 2024 05:12:04 GMT
WORKDIR /opt/silverpeas/bin
# Wed, 05 Jun 2024 05:12:04 GMT
COPY file:d0f4d653b188d4ae9abc4034eaa253a720b62e15e65856fa78a99c4a4a58ad67 in /opt/ 
# Wed, 05 Jun 2024 05:12:04 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Wed, 05 Jun 2024 05:13:38 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle   && ./silverpeas construct   && rm ../log/build-*   && touch .install
# Wed, 05 Jun 2024 05:13:41 GMT
EXPOSE 8000 9990
# Wed, 05 Jun 2024 05:13:41 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Wed, 05 Jun 2024 05:13:41 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:933f629bd874cbb2a472b9b610f4b3175c0ddc13b0050adb804e6541a2eef740`  
		Last Modified: Wed, 05 Jun 2024 05:15:21 GMT  
		Size: 762.5 MB (762493745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c96cd7e4d3db5be39f1c0f3bad42f0db1cc5cafa5fc85ccc953e10f457b0b37b`  
		Last Modified: Wed, 05 Jun 2024 05:14:00 GMT  
		Size: 4.0 MB (3994028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f44bbd5f2d4dfdbe3e3875ecfd167de3e4cf15567d4b59579ed86e4c272f486`  
		Last Modified: Wed, 05 Jun 2024 05:14:00 GMT  
		Size: 7.1 MB (7146606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d118d458b83be3f3433e2123c2884b0f362d4c2de6821d07572d7729f6257b3`  
		Last Modified: Wed, 05 Jun 2024 05:13:58 GMT  
		Size: 2.5 MB (2534358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101b0fdc9d44501a119e05adadd02ff4f6977b4cc7b715eca34485d286112e09`  
		Last Modified: Wed, 05 Jun 2024 05:13:57 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228b4fddb660a941ebc5bdaf2c8a3e7515e1dabcf3d1069654ac87ce46114edb`  
		Last Modified: Wed, 05 Jun 2024 05:13:57 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ccf9affdbd18c99603542039df462f773dd02538a34b124e59a2d46db4f84b4`  
		Last Modified: Wed, 05 Jun 2024 05:14:09 GMT  
		Size: 217.8 MB (217842621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e589b057985a28fef6441152ea4e8ab4603745d26b8adfcb93618258349a02`  
		Last Modified: Wed, 05 Jun 2024 05:13:55 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1db6ea3776f8e9d716fce1d3195fb32a2a27c1efe91829679cbd3ef5dc6984a7`  
		Last Modified: Wed, 05 Jun 2024 05:13:55 GMT  
		Size: 662.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446662c2cbba0fab911e1dbe35e580be648c2de02c1e416659c39f955cdd3727`  
		Last Modified: Wed, 05 Jun 2024 05:13:56 GMT  
		Size: 922.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3427ac70af1c6dbcfd1407777fc4f733791de786dbc14623539eafe6377158e2`  
		Last Modified: Wed, 05 Jun 2024 05:13:55 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77150facf177085dfb4f621c9751dacbe11aca03caee3b92a21e84026286c136`  
		Last Modified: Wed, 05 Jun 2024 05:14:31 GMT  
		Size: 754.6 MB (754598284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `silverpeas:latest`

```console
$ docker pull silverpeas@sha256:7b8e5c03079a1b2e8a4d6bb45bba2af7fdc7fcfcb922e0b773c83aabf17737f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `silverpeas:latest` - linux; amd64

```console
$ docker pull silverpeas@sha256:16e87532ff17f224ab0ecabb3a8b5ad9a067a1bdba47125c9830e7ab25541e64
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1777196611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22b396df20749b65ffb6254842e04ba93e00c718e3517c8775e08972d0540c00`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:03:40 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Wed, 05 Jun 2024 05:03:40 GMT
ENV TERM=xterm
# Wed, 05 Jun 2024 05:10:48 GMT
RUN apt-get update   && apt-get install -y tzdata   && apt-get install -y     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Wed, 05 Jun 2024 05:10:54 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Wed, 05 Jun 2024 05:10:57 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Wed, 05 Jun 2024 05:10:58 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Wed, 05 Jun 2024 05:11:37 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Wed, 05 Jun 2024 05:11:38 GMT
ENV LANG=en_US.UTF-8
# Wed, 05 Jun 2024 05:11:38 GMT
ENV LANGUAGE=en_US.UTF-8
# Wed, 05 Jun 2024 05:11:38 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 05 Jun 2024 05:11:38 GMT
ENV PING_ON=1
# Wed, 05 Jun 2024 05:11:38 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 05 Jun 2024 05:11:39 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 05 Jun 2024 05:11:39 GMT
ENV JAVA_HOME=/docker-java-home
# Wed, 05 Jun 2024 05:11:39 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Wed, 05 Jun 2024 05:11:39 GMT
ENV JBOSS_HOME=/opt/wildfly
# Wed, 05 Jun 2024 05:11:39 GMT
ENV SILVERPEAS_VERSION=6.3.5
# Wed, 05 Jun 2024 05:11:40 GMT
ENV WILDFLY_VERSION=26.1.1
# Wed, 05 Jun 2024 05:11:40 GMT
LABEL name=Silverpeas 6.3.5 description=Image to install and to run Silverpeas 6.3.5 vendor=Silverpeas version=6.3.5 build=1
# Wed, 05 Jun 2024 05:12:03 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Wed, 05 Jun 2024 05:12:03 GMT
COPY file:bdea684cbb56f9ec67736214361c476c97d0a0e06ec936f53a7da778776f533b in /root/.m2/ 
# Wed, 05 Jun 2024 05:12:04 GMT
COPY file:473bf75b335a39b6b4b39c64cd151bd8ed3d3e33da73b8124e537a5db1fad3d6 in /opt/silverpeas/bin/ 
# Wed, 05 Jun 2024 05:12:04 GMT
WORKDIR /opt/silverpeas/bin
# Wed, 05 Jun 2024 05:12:04 GMT
COPY file:d0f4d653b188d4ae9abc4034eaa253a720b62e15e65856fa78a99c4a4a58ad67 in /opt/ 
# Wed, 05 Jun 2024 05:12:04 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Wed, 05 Jun 2024 05:13:38 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle   && ./silverpeas construct   && rm ../log/build-*   && touch .install
# Wed, 05 Jun 2024 05:13:41 GMT
EXPOSE 8000 9990
# Wed, 05 Jun 2024 05:13:41 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Wed, 05 Jun 2024 05:13:41 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:933f629bd874cbb2a472b9b610f4b3175c0ddc13b0050adb804e6541a2eef740`  
		Last Modified: Wed, 05 Jun 2024 05:15:21 GMT  
		Size: 762.5 MB (762493745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c96cd7e4d3db5be39f1c0f3bad42f0db1cc5cafa5fc85ccc953e10f457b0b37b`  
		Last Modified: Wed, 05 Jun 2024 05:14:00 GMT  
		Size: 4.0 MB (3994028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f44bbd5f2d4dfdbe3e3875ecfd167de3e4cf15567d4b59579ed86e4c272f486`  
		Last Modified: Wed, 05 Jun 2024 05:14:00 GMT  
		Size: 7.1 MB (7146606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d118d458b83be3f3433e2123c2884b0f362d4c2de6821d07572d7729f6257b3`  
		Last Modified: Wed, 05 Jun 2024 05:13:58 GMT  
		Size: 2.5 MB (2534358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101b0fdc9d44501a119e05adadd02ff4f6977b4cc7b715eca34485d286112e09`  
		Last Modified: Wed, 05 Jun 2024 05:13:57 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228b4fddb660a941ebc5bdaf2c8a3e7515e1dabcf3d1069654ac87ce46114edb`  
		Last Modified: Wed, 05 Jun 2024 05:13:57 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ccf9affdbd18c99603542039df462f773dd02538a34b124e59a2d46db4f84b4`  
		Last Modified: Wed, 05 Jun 2024 05:14:09 GMT  
		Size: 217.8 MB (217842621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e589b057985a28fef6441152ea4e8ab4603745d26b8adfcb93618258349a02`  
		Last Modified: Wed, 05 Jun 2024 05:13:55 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1db6ea3776f8e9d716fce1d3195fb32a2a27c1efe91829679cbd3ef5dc6984a7`  
		Last Modified: Wed, 05 Jun 2024 05:13:55 GMT  
		Size: 662.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446662c2cbba0fab911e1dbe35e580be648c2de02c1e416659c39f955cdd3727`  
		Last Modified: Wed, 05 Jun 2024 05:13:56 GMT  
		Size: 922.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3427ac70af1c6dbcfd1407777fc4f733791de786dbc14623539eafe6377158e2`  
		Last Modified: Wed, 05 Jun 2024 05:13:55 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77150facf177085dfb4f621c9751dacbe11aca03caee3b92a21e84026286c136`  
		Last Modified: Wed, 05 Jun 2024 05:14:31 GMT  
		Size: 754.6 MB (754598284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
