<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `silverpeas`

-	[`silverpeas:6.3.5`](#silverpeas635)
-	[`silverpeas:6.4.1`](#silverpeas641)
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

## `silverpeas:6.4.1`

```console
$ docker pull silverpeas@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `silverpeas:latest`

```console
$ docker pull silverpeas@sha256:4d74472cfb2069b720131a166b0196b1bfa27e0066cd363614d847cc12dcf630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `silverpeas:latest` - linux; amd64

```console
$ docker pull silverpeas@sha256:e6c1d0c861f07ed70e6dbe90819d063b7e65ae662b32097a6997deac6afeb4f7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1805432885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30994531debd1ced645d71db2652bbed0e61e733d027995d63f11a81011ddcd9`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Mon, 24 Jun 2024 23:20:35 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Mon, 24 Jun 2024 23:20:35 GMT
ENV TERM=xterm
# Mon, 24 Jun 2024 23:25:33 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends tzdata   && apt-get install -y --no-install-recommends     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Mon, 24 Jun 2024 23:25:40 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 swftools-bin-0.9.2.zip' | sha256sum -c --status -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Mon, 24 Jun 2024 23:25:44 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 pdf2json-bin-0.68.zip' | sha256sum -c --status -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Mon, 24 Jun 2024 23:25:44 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Mon, 24 Jun 2024 23:26:25 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Mon, 24 Jun 2024 23:26:25 GMT
ENV LANG=en_US.UTF-8
# Mon, 24 Jun 2024 23:26:25 GMT
ENV LANGUAGE=en_US.UTF-8
# Mon, 24 Jun 2024 23:26:25 GMT
ENV LC_ALL=en_US.UTF-8
# Mon, 24 Jun 2024 23:26:25 GMT
ENV PING_ON=1
# Mon, 24 Jun 2024 23:26:26 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Mon, 24 Jun 2024 23:26:26 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Mon, 24 Jun 2024 23:26:26 GMT
ENV JAVA_HOME=/docker-java-home
# Mon, 24 Jun 2024 23:26:27 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Mon, 24 Jun 2024 23:26:27 GMT
ENV JBOSS_HOME=/opt/wildfly
# Mon, 24 Jun 2024 23:26:27 GMT
ENV SILVERPEAS_VERSION=6.4
# Mon, 24 Jun 2024 23:26:27 GMT
ENV WILDFLY_VERSION=26.1.3
# Mon, 24 Jun 2024 23:26:27 GMT
LABEL name=Silverpeas 6.4 description=Image to install and to run Silverpeas 6.4 vendor=Silverpeas version=6.4 build=1
# Mon, 24 Jun 2024 23:28:02 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && wget -nc https://www.silverpeas.org/files/oak-migrate.zip   && echo '02d21f69004f2d9e634e82ec062d94521bd6bc0385d7c0ddf9af261cb63afdbb oak-migrate.zip' | sha256sum -c --status -   && mkdir -p /opt/oak-migration   && unzip oak-migrate.zip -d /opt/oak-migration/   && chmod +x /opt/oak-migration/oak-migrate.sh   && rm *.zip   && mkdir -p /root/.m2
# Mon, 24 Jun 2024 23:28:03 GMT
COPY file:bdea684cbb56f9ec67736214361c476c97d0a0e06ec936f53a7da778776f533b in /root/.m2/ 
# Mon, 24 Jun 2024 23:28:03 GMT
COPY file:473bf75b335a39b6b4b39c64cd151bd8ed3d3e33da73b8124e537a5db1fad3d6 in /opt/silverpeas/bin/ 
# Mon, 24 Jun 2024 23:28:03 GMT
WORKDIR /opt/silverpeas/bin
# Mon, 24 Jun 2024 23:28:03 GMT
COPY file:39b5296ac06d483424dc84ebab1183a21a787142115d7243720e010eb696d296 in /opt/ 
# Mon, 24 Jun 2024 23:28:03 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Mon, 24 Jun 2024 23:29:46 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN set -eux;   sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle;   echo "Construct Silverpeas ${SILVERPEAS_VERSION}";   ./silverpeas assemble || (cat ../log/build-* && exit 1);   rm ../log/build-*;   touch .install;
# Mon, 24 Jun 2024 23:29:51 GMT
EXPOSE 8000 9990
# Mon, 24 Jun 2024 23:29:51 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Mon, 24 Jun 2024 23:29:51 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d197a946d6993801aed554996da8580dc87a21f3714d2aa44ba65cb7c77bddac`  
		Last Modified: Mon, 24 Jun 2024 23:31:08 GMT  
		Size: 494.6 MB (494632993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d222bf6236654b25c0aa52449c441540f9743bb6bfca6635a30a7f253fe3582`  
		Last Modified: Mon, 24 Jun 2024 23:30:11 GMT  
		Size: 4.0 MB (3994018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38aff74284c1f81c367412391c1bb1bda03cf5517e3f740d58306b2fcae98547`  
		Last Modified: Mon, 24 Jun 2024 23:30:12 GMT  
		Size: 7.1 MB (7146630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a5abe18a77a2ae4e782119767491481b95cf2227bac6a533a1c9e33b68896d9`  
		Last Modified: Mon, 24 Jun 2024 23:30:09 GMT  
		Size: 2.5 MB (2538607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4008e9bc952c50d44e190fc329b0dbe5ce85e789dab5a04d6946e76429d1b6a`  
		Last Modified: Mon, 24 Jun 2024 23:30:08 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc75f05005e2792a0730969bafb045ed74d00e36302bc036404e097dfecf4842`  
		Last Modified: Mon, 24 Jun 2024 23:30:08 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3afda38506fc98760d9a30f66492f28a194a843e7480099945857ad0bc4f5cf7`  
		Last Modified: Mon, 24 Jun 2024 23:30:22 GMT  
		Size: 267.1 MB (267147065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f5679fb2377650aa5e1694a20a7eb7535267af87da0a00c7f802d7a9e74645`  
		Last Modified: Mon, 24 Jun 2024 23:30:06 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8884d76f529c232c52b54d09618f803187641241e52e5f81983471a28ccfbb69`  
		Last Modified: Mon, 24 Jun 2024 23:30:06 GMT  
		Size: 663.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9e70331faa3bbc75c59bbbcfeeb0c3575203f3a4f32b3f2567ce8d88fc73a7`  
		Last Modified: Mon, 24 Jun 2024 23:30:06 GMT  
		Size: 1.4 KB (1450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f94ca034f53fce85bb27f8b8987dc46c73342a692daffb78b2b4b3a89483fc`  
		Last Modified: Mon, 24 Jun 2024 23:30:07 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:104a9a7be186f3d2f5c5f2135ba6d01c04543b55627bd27c1ee16db6c0ac0e76`  
		Last Modified: Mon, 24 Jun 2024 23:30:52 GMT  
		Size: 999.5 MB (999531018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
