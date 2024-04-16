## `silverpeas:latest`

```console
$ docker pull silverpeas@sha256:3277e6c8be87f0d7d396703b9a0c39f3978c698e3cec4120c49336e295c9fa38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `silverpeas:latest` - linux; amd64

```console
$ docker pull silverpeas@sha256:d3cef8f7c8ebebef744b78ffeef64d105f84452516be6c9b595cc7d4e4567c78
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1777170306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4033a5acff7936549a36e629906c6b6d90e3903b5d8691a1cc00b090434639d6`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Wed, 10 Apr 2024 18:50:35 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:50:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:50:35 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 10 Apr 2024 18:50:37 GMT
ADD file:ea2128e23dce0162557abadd80656bd5ae047d573095d1d4323eb4154490dfdc in / 
# Wed, 10 Apr 2024 18:50:37 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 05:33:09 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Tue, 16 Apr 2024 05:33:09 GMT
ENV TERM=xterm
# Tue, 16 Apr 2024 05:39:17 GMT
RUN apt-get update   && apt-get install -y tzdata   && apt-get install -y     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Tue, 16 Apr 2024 05:39:24 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Tue, 16 Apr 2024 05:39:27 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Tue, 16 Apr 2024 05:39:27 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Tue, 16 Apr 2024 05:40:07 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Tue, 16 Apr 2024 05:40:07 GMT
ENV LANG=en_US.UTF-8
# Tue, 16 Apr 2024 05:40:08 GMT
ENV LANGUAGE=en_US.UTF-8
# Tue, 16 Apr 2024 05:40:08 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 16 Apr 2024 05:40:08 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 16 Apr 2024 05:40:09 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 16 Apr 2024 05:40:09 GMT
ENV JAVA_HOME=/docker-java-home
# Tue, 16 Apr 2024 05:40:09 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Tue, 16 Apr 2024 05:40:09 GMT
ENV JBOSS_HOME=/opt/wildfly
# Tue, 16 Apr 2024 05:40:09 GMT
ENV SILVERPEAS_VERSION=6.3.4
# Tue, 16 Apr 2024 05:40:09 GMT
ENV WILDFLY_VERSION=26.1.1
# Tue, 16 Apr 2024 05:40:09 GMT
LABEL name=Silverpeas 6.3.4 description=Image to install and to run Silverpeas 6.3.4 vendor=Silverpeas version=6.3.4 build=1
# Tue, 16 Apr 2024 05:40:42 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Tue, 16 Apr 2024 05:40:43 GMT
COPY file:4d0e637a3e1ce0b8143795fd5df1997a7ee18fba27382849ed23e9ecb8142009 in /root/.m2/ 
# Tue, 16 Apr 2024 05:40:43 GMT
COPY file:473bf75b335a39b6b4b39c64cd151bd8ed3d3e33da73b8124e537a5db1fad3d6 in /opt/silverpeas/bin/ 
# Tue, 16 Apr 2024 05:40:43 GMT
WORKDIR /opt/silverpeas/bin
# Tue, 16 Apr 2024 05:40:43 GMT
COPY file:53a5e8023ae593585b413b14c995a55c412d5a4dff0ebcb7db632f2c22c39da6 in /opt/ 
# Tue, 16 Apr 2024 05:40:43 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Tue, 16 Apr 2024 05:43:05 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle   && ./silverpeas construct   && rm ../log/build-*   && touch .install
# Tue, 16 Apr 2024 05:43:08 GMT
EXPOSE 8000 9990
# Tue, 16 Apr 2024 05:43:08 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Tue, 16 Apr 2024 05:43:09 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:80888bc6716fcbb8874e75ac88898d3e38e6f1bc55678f0e97ca9d706b7f3733`  
		Last Modified: Fri, 12 Apr 2024 07:27:49 GMT  
		Size: 28.6 MB (28584506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d13f2b1d0a304fbb18d8a5cdbf0f5ca08ebb2c82f9ee808d8036b4e3234231`  
		Last Modified: Tue, 16 Apr 2024 05:44:51 GMT  
		Size: 762.5 MB (762502233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c40509f4f2d1786d4fdbadd252cb3dd903565fe816644af6ae777dbd0e2be8d`  
		Last Modified: Tue, 16 Apr 2024 05:43:28 GMT  
		Size: 4.0 MB (3994078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab94a8653f23ad132917a6eb1c913efaa9c61d3dc416c2856a9578019fd79890`  
		Last Modified: Tue, 16 Apr 2024 05:43:29 GMT  
		Size: 7.1 MB (7146635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21f2fdb13cadc8f9edfa2cd70e864d008893453323a65060d60c395a2e91f38`  
		Last Modified: Tue, 16 Apr 2024 05:43:26 GMT  
		Size: 2.5 MB (2534362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a94880c3d39ff93e7b7395f2dc02af7137d3e3cfca47c0fa52307e5dca65e4`  
		Last Modified: Tue, 16 Apr 2024 05:43:25 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d85f8682597f0156537a1ea503f0ed9bc6cd6787d8969a2b29bcfe6d6a76fa`  
		Last Modified: Tue, 16 Apr 2024 05:43:25 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071e3fc0675154eb7f82d562fcd96a0ea1ac771671a9423e18492c85effbc4d3`  
		Last Modified: Tue, 16 Apr 2024 05:43:37 GMT  
		Size: 217.8 MB (217842734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d4a02a4e50f0b8964c8c81f64efd26be2df4e6b1d09961cde46fa7c73847e6`  
		Last Modified: Tue, 16 Apr 2024 05:43:23 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae63fb3c28ba884c1159c982d93e5c546027537d100e75ab99f2d75835c8c25`  
		Last Modified: Tue, 16 Apr 2024 05:43:24 GMT  
		Size: 663.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9539217d5988b1753381350694c9da0d05a1eba28016eef0582587cc9265f138`  
		Last Modified: Tue, 16 Apr 2024 05:43:23 GMT  
		Size: 908.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b1c297c0809c48933a348ac62722fcc4e64bb0f94af0e6292177e748da53079`  
		Last Modified: Tue, 16 Apr 2024 05:43:23 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0d5cf0f244f361a93ad12df8246c2de32cba30d9bd352dfd0b9619358db066`  
		Last Modified: Tue, 16 Apr 2024 05:43:59 GMT  
		Size: 754.6 MB (754563026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
