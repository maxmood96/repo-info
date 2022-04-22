## `silverpeas:latest`

```console
$ docker pull silverpeas@sha256:5e7734d554a4376ceb521ee625b7be960a2f1eeccae1cda3d7760cc5dea6496b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `silverpeas:latest` - linux; amd64

```console
$ docker pull silverpeas@sha256:a68df697858c498ccc7118624c1e47d27e75cbe917703518f01fce367b126041
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1900054775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc7ce49919442da33dd428f6a681ef80cfe0278187f11d1a2d4e1b2b9e7b1dd`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 04:06:11 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Fri, 22 Apr 2022 04:06:11 GMT
ENV TERM=xterm
# Fri, 22 Apr 2022 04:11:59 GMT
RUN apt-get update   && apt-get install -y tzdata   && apt-get install -y     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Fri, 22 Apr 2022 04:12:15 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Fri, 22 Apr 2022 04:12:33 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Fri, 22 Apr 2022 04:12:33 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Fri, 22 Apr 2022 04:13:13 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Fri, 22 Apr 2022 04:13:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 22 Apr 2022 04:13:13 GMT
ENV LANGUAGE=en_US.UTF-8
# Fri, 22 Apr 2022 04:13:13 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 22 Apr 2022 04:13:14 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 22 Apr 2022 04:13:14 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 22 Apr 2022 04:13:14 GMT
ENV JAVA_HOME=/docker-java-home
# Fri, 22 Apr 2022 04:13:14 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Fri, 22 Apr 2022 04:13:14 GMT
ENV JBOSS_HOME=/opt/wildfly
# Fri, 22 Apr 2022 04:13:15 GMT
ENV SILVERPEAS_VERSION=6.2.3
# Fri, 22 Apr 2022 04:13:15 GMT
ENV WILDFLY_VERSION=20.0.1
# Fri, 22 Apr 2022 04:13:15 GMT
LABEL name=Silverpeas 6.2.3 description=Image to install and to run Silverpeas 6.2.3 vendor=Silverpeas version=6.2.3 build=1
# Fri, 22 Apr 2022 04:13:54 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc http://download.jboss.org/wildfly/${WILDFLY_VERSION}.Final/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Fri, 22 Apr 2022 04:13:55 GMT
COPY file:4d0e637a3e1ce0b8143795fd5df1997a7ee18fba27382849ed23e9ecb8142009 in /root/.m2/ 
# Fri, 22 Apr 2022 04:13:55 GMT
COPY file:473bf75b335a39b6b4b39c64cd151bd8ed3d3e33da73b8124e537a5db1fad3d6 in /opt/silverpeas/bin/ 
# Fri, 22 Apr 2022 04:13:55 GMT
WORKDIR /opt/silverpeas/bin
# Fri, 22 Apr 2022 04:13:55 GMT
COPY file:b54156953ecf6c3259f3b3d2885a784847c0996fd145c0f7ccef25182725511f in /opt/ 
# Fri, 22 Apr 2022 04:13:55 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Fri, 22 Apr 2022 04:19:43 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle   && ./silverpeas construct   && rm ../log/build-*   && touch .install
# Fri, 22 Apr 2022 04:19:46 GMT
EXPOSE 8000 9990
# Fri, 22 Apr 2022 04:19:46 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Fri, 22 Apr 2022 04:19:47 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c461063983ebe63eaefaebaf3ed0ba3e0fc81b49bd6a19d5ef9b6560dc6f7162`  
		Last Modified: Fri, 22 Apr 2022 04:21:34 GMT  
		Size: 913.0 MB (912962709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de54e84a5bc45507aea28633e05aa2c1cb1959088a19e123688dc3b577d6d48`  
		Last Modified: Fri, 22 Apr 2022 04:20:00 GMT  
		Size: 4.0 MB (3994070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20dfbdc863300473d6165d3055548bb1be61a4951c7a61c0d27b2358714924db`  
		Last Modified: Fri, 22 Apr 2022 04:20:01 GMT  
		Size: 7.1 MB (7146667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4e62a5e7b001477cea38010ad0d663cc065eb5fbd67123d6e2404cd807f2af`  
		Last Modified: Fri, 22 Apr 2022 04:19:58 GMT  
		Size: 2.5 MB (2534366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da35a7d5cdd8926dfa140ff42360bcfd368f6733f1e86569e9524ea791ec359`  
		Last Modified: Fri, 22 Apr 2022 04:19:57 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0615126b1d554c3de18a88fe697bbcc011853ba8307fb37dfe54f793c002492`  
		Last Modified: Fri, 22 Apr 2022 04:19:57 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87acb1ad1acb53cecefabb3d7aeb53b8d57c13fafdd04f2400d9a30ce29b5711`  
		Last Modified: Fri, 22 Apr 2022 04:20:09 GMT  
		Size: 196.8 MB (196774084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3125b7791bd61b993465128ec1d95200eb61960b4c641fcdcf0cb9bad2db59d7`  
		Last Modified: Fri, 22 Apr 2022 04:19:55 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95dc2e008aedef779f03301231c61ce4fca38420168ed21d9c9499674054f49a`  
		Last Modified: Fri, 22 Apr 2022 04:19:54 GMT  
		Size: 661.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e933302d51109ed335e299b7d276e6699c7a4bb3ab277c834de40796938394e`  
		Last Modified: Fri, 22 Apr 2022 04:19:55 GMT  
		Size: 875.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:205f7470a657414419b2de3fa599cd7541b347c079997f949153a301bca17736`  
		Last Modified: Fri, 22 Apr 2022 04:19:55 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a20346176c9df109a54718ee460222f1feae9a26b3edcaf55cf45a00f124076`  
		Last Modified: Fri, 22 Apr 2022 04:20:31 GMT  
		Size: 748.1 MB (748074178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
