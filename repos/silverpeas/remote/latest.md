## `silverpeas:latest`

```console
$ docker pull silverpeas@sha256:1d259d8f5ccf04d4f6907a5134463d0f167bb0328d1310d13cb66f153a990320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `silverpeas:latest` - linux; amd64

```console
$ docker pull silverpeas@sha256:5033c394031b90ce0b7c349ee9ec8465f21c0552f93802613bd65c92a04b111e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1899990075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b385ec591d229d8494e8adf3622a3cfad5acd60671e06e45cfeb11489d8a4c9`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 02:52:23 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Wed, 06 Apr 2022 02:52:23 GMT
ENV TERM=xterm
# Wed, 06 Apr 2022 02:58:09 GMT
RUN apt-get update   && apt-get install -y tzdata   && apt-get install -y     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Wed, 06 Apr 2022 02:58:22 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Wed, 06 Apr 2022 02:58:33 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Wed, 06 Apr 2022 02:58:33 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Wed, 06 Apr 2022 02:59:11 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Wed, 06 Apr 2022 02:59:11 GMT
ENV LANG=en_US.UTF-8
# Wed, 06 Apr 2022 02:59:11 GMT
ENV LANGUAGE=en_US.UTF-8
# Wed, 06 Apr 2022 02:59:12 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 06 Apr 2022 02:59:12 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 06 Apr 2022 02:59:13 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 06 Apr 2022 02:59:13 GMT
ENV JAVA_HOME=/docker-java-home
# Wed, 06 Apr 2022 02:59:13 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Wed, 06 Apr 2022 02:59:13 GMT
ENV JBOSS_HOME=/opt/wildfly
# Wed, 06 Apr 2022 02:59:13 GMT
ENV SILVERPEAS_VERSION=6.2.2
# Wed, 06 Apr 2022 02:59:13 GMT
ENV WILDFLY_VERSION=20.0.1
# Wed, 06 Apr 2022 02:59:13 GMT
LABEL name=Silverpeas 6.2.2 description=Image to install and to run Silverpeas 6.2.2 vendor=Silverpeas version=6.2.2 build=1
# Wed, 06 Apr 2022 03:00:57 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc http://download.jboss.org/wildfly/${WILDFLY_VERSION}.Final/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Wed, 06 Apr 2022 03:00:57 GMT
COPY file:4d0e637a3e1ce0b8143795fd5df1997a7ee18fba27382849ed23e9ecb8142009 in /root/.m2/ 
# Wed, 06 Apr 2022 03:00:57 GMT
COPY file:473bf75b335a39b6b4b39c64cd151bd8ed3d3e33da73b8124e537a5db1fad3d6 in /opt/silverpeas/bin/ 
# Wed, 06 Apr 2022 03:00:58 GMT
WORKDIR /opt/silverpeas/bin
# Wed, 06 Apr 2022 03:00:58 GMT
COPY file:b54156953ecf6c3259f3b3d2885a784847c0996fd145c0f7ccef25182725511f in /opt/ 
# Wed, 06 Apr 2022 03:00:58 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Wed, 06 Apr 2022 03:04:47 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle   && ./silverpeas construct   && rm ../log/build-*   && touch .install
# Wed, 06 Apr 2022 03:04:50 GMT
EXPOSE 8000 9990
# Wed, 06 Apr 2022 03:04:50 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Wed, 06 Apr 2022 03:04:50 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b05a90dc189177dca73a70569e0bdaec9c261e84d64c7abc39e2f91f2499b92`  
		Last Modified: Wed, 06 Apr 2022 03:17:44 GMT  
		Size: 912.9 MB (912949900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8354bab153b2388c09027b651c8d8fa0d16c33638a92800ee051db98815c50db`  
		Last Modified: Wed, 06 Apr 2022 03:16:10 GMT  
		Size: 4.0 MB (3994077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae2a83e218d0b0c8229bbed27b4c39102645feff1c60b21226e0a828b0774c8`  
		Last Modified: Wed, 06 Apr 2022 03:16:10 GMT  
		Size: 7.1 MB (7146661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065c4ddf20bd08031d52aa973e3294483effd66844bcd5f8b16d1e32d6bf70fb`  
		Last Modified: Wed, 06 Apr 2022 03:16:07 GMT  
		Size: 2.5 MB (2534352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa348fd95d1e5baf1877c1bde52449bb4d0461545d3afdd01140d8345f24c754`  
		Last Modified: Wed, 06 Apr 2022 03:16:06 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed975ca4856eb6275b35a1be17c437371bf39d3922be9d9d56e46ef22e2a9be2`  
		Last Modified: Wed, 06 Apr 2022 03:16:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1603bd035f6893e965431eaf80f70b1cda33cd7962254259f44dc07e471e9088`  
		Last Modified: Wed, 06 Apr 2022 03:16:19 GMT  
		Size: 196.8 MB (196774061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:169a0f325c0e8f0764b805d218aea05aa87f0b4e6d134ba800b22723f55e8529`  
		Last Modified: Wed, 06 Apr 2022 03:16:04 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:923414ab849db89215e0c32af13a8b8fad56622136066125b376961b4cc1267a`  
		Last Modified: Wed, 06 Apr 2022 03:16:04 GMT  
		Size: 661.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8267afaef4746a9bf0891823a14384a241d9faa041be34bba3a9dfb52a87e081`  
		Last Modified: Wed, 06 Apr 2022 03:16:04 GMT  
		Size: 876.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a6eb0b84115d6f199ad7318ea5453e2fead096d9ee6e2a52c14b6ae19f5891f`  
		Last Modified: Wed, 06 Apr 2022 03:16:04 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b8a5a9746c97a38d21c51737b90b0cfd68e486f0064e0465d6692197f94e61`  
		Last Modified: Wed, 06 Apr 2022 03:16:42 GMT  
		Size: 748.0 MB (748022036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
