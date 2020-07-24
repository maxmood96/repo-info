<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `silverpeas`

-	[`silverpeas:6.0.2`](#silverpeas602)
-	[`silverpeas:6.1`](#silverpeas61)
-	[`silverpeas:latest`](#silverpeaslatest)

## `silverpeas:6.0.2`

```console
$ docker pull silverpeas@sha256:c99f1472dddafedfabf5ca1f8761cd3172dc3a125629591bb603b9fddd38158e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `silverpeas:6.0.2` - linux; amd64

```console
$ docker pull silverpeas@sha256:23361a46e4486da586b40d7416802ad99ab6d055ff43dbf5225c7004152a583d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1011652818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8d594fb8468244888a542e9a10884c78ff708054cfc662457ce6ee59c1cc0cb`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Fri, 24 Jul 2020 14:39:06 GMT
ADD file:513ae777bc4042f8446c0454f8cffc9a94f8429de963651d9a6dab95d4502007 in / 
# Fri, 24 Jul 2020 14:39:07 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 14:39:07 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:39:08 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:39:08 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 17:15:27 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Fri, 24 Jul 2020 17:15:27 GMT
ENV TERM=xterm
# Fri, 24 Jul 2020 17:17:32 GMT
RUN apt-get update && apt-get install -y     wget     locales     procps     net-tools     zip     unzip     openjdk-8-jdk     ffmpeg     imagemagick     ghostscript     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Fri, 24 Jul 2020 17:17:34 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Fri, 24 Jul 2020 17:17:36 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Fri, 24 Jul 2020 17:17:36 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Fri, 24 Jul 2020 17:17:39 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Fri, 24 Jul 2020 17:17:39 GMT
ENV LANG=en_US.UTF-8
# Fri, 24 Jul 2020 17:17:39 GMT
ENV LANGUAGE=en_US.UTF-8
# Fri, 24 Jul 2020 17:17:40 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 24 Jul 2020 17:17:40 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 24 Jul 2020 17:17:41 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 24 Jul 2020 17:17:41 GMT
ENV JAVA_HOME=/docker-java-home
# Fri, 24 Jul 2020 17:17:41 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Fri, 24 Jul 2020 17:17:42 GMT
ENV JBOSS_HOME=/opt/wildfly
# Fri, 24 Jul 2020 17:17:42 GMT
ENV SILVERPEAS_VERSION=6.0.2
# Fri, 24 Jul 2020 17:17:42 GMT
ENV WILDFLY_VERSION=10.1.0
# Fri, 24 Jul 2020 17:17:42 GMT
LABEL name=Silverpeas 6 description=Image to install and to run Silverpeas 6 vendor=Silverpeas version=6.0.2 build=1
# Fri, 24 Jul 2020 17:18:09 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc http://download.jboss.org/wildfly/${WILDFLY_VERSION}.Final/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Fri, 24 Jul 2020 17:18:09 GMT
COPY file:d12fb4c8fc28235c5621533a9ae0d98ba26e3adf1ffc690da4a6118aa71d8190 in /root/.m2/ 
# Fri, 24 Jul 2020 17:18:09 GMT
WORKDIR /opt/silverpeas/bin
# Fri, 24 Jul 2020 17:18:09 GMT
COPY file:31e3db287bacfa9fb086f2ae49169410b9f0fdf4178bf47d0ebe93621aa996e4 in /opt/ 
# Fri, 24 Jul 2020 17:18:10 GMT
COPY file:5d883339e9add47c37406a038c7747cafede9f81436843206bab5bde7da6e2f6 in /opt/silverpeas/configuration/silverpeas/ 
# Fri, 24 Jul 2020 17:21:09 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ./silverpeas assemble   && rm ../log/build-*   && touch .install
# Fri, 24 Jul 2020 17:21:09 GMT
EXPOSE 8000 9990
# Fri, 24 Jul 2020 17:21:10 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/xmlcomponents/workflows]
# Fri, 24 Jul 2020 17:21:10 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:7b378fa0f9085667ced1c76c9919cde8663becf2218e8d20e2df8d0824311531`  
		Last Modified: Tue, 07 Jul 2020 13:19:56 GMT  
		Size: 44.4 MB (44401021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d77b1b29f2e9b6f141b9d8f74b601f40eb998544783f4a0a3cdc384873c1a4e`  
		Last Modified: Fri, 24 Jul 2020 14:39:50 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c793be88baee3f3204444e4d4e49c4e44c1709d40182c131cd5681c94e17227`  
		Last Modified: Fri, 24 Jul 2020 14:39:50 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc05c8a19c0cf83f2f44263c967c3fe81fffc4b41b592ad088fb1534c206e70`  
		Last Modified: Fri, 24 Jul 2020 14:39:49 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b860ace0228b3f06bd67c20e42d46e03e9948d13505087b34023b42298e2d2`  
		Last Modified: Fri, 24 Jul 2020 17:23:39 GMT  
		Size: 206.3 MB (206281750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a45caa50f0d90e5025c9b19821daf66889b49d127501f75a7b9552bd7a3f015b`  
		Last Modified: Fri, 24 Jul 2020 17:23:02 GMT  
		Size: 4.0 MB (3994026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888eb15f3886ed74674369c0c86531b592d111fd0a57824f05b97d53bb652f8f`  
		Last Modified: Fri, 24 Jul 2020 17:23:02 GMT  
		Size: 7.1 MB (7146615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f0fb0b6883e22fabc8066813c71c6c49a40f4859432ede1c9092500295469f`  
		Last Modified: Fri, 24 Jul 2020 17:23:00 GMT  
		Size: 845.4 KB (845395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef75a7a7e8d22159c01b6cdb68b82050fe12bfeae0b25ea2bda15463bde3e45`  
		Last Modified: Fri, 24 Jul 2020 17:22:59 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5329a9fcc9d228dd2b3a2215c36fc0d6f647df91b382b01a23dc4a87b7d232e1`  
		Last Modified: Fri, 24 Jul 2020 17:22:59 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89aae662a54ed767dbb983185046ec146c2f96cc8fa6858210d18ea7e28a7fbb`  
		Last Modified: Fri, 24 Jul 2020 17:23:10 GMT  
		Size: 144.3 MB (144284462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e373986e807e0da177ece7012084ee74d1ee6b95dabd5eed6d568f71cf959c2`  
		Last Modified: Fri, 24 Jul 2020 17:22:58 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01f8e02b1b7a5e017f000caf1649b904d1a46c3ce16ae5f1a189dc70eed7b235`  
		Last Modified: Fri, 24 Jul 2020 17:22:58 GMT  
		Size: 808.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a6774561ba0fc3a84ab7abafb9d868fc6952187c1bb58ff21c1a6094212cedd`  
		Last Modified: Fri, 24 Jul 2020 17:22:58 GMT  
		Size: 378.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e2d95a3c29e4938aef2022952baa186b33522d9c2cb7da1d0d4af0b66df796`  
		Last Modified: Fri, 24 Jul 2020 17:23:40 GMT  
		Size: 604.7 MB (604696045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `silverpeas:6.1`

```console
$ docker pull silverpeas@sha256:321a007b1100df56b705292b67bb19244394d3ff134d7502681a8685fa3f1dc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `silverpeas:6.1` - linux; amd64

```console
$ docker pull silverpeas@sha256:2e435049ab3c10eb77bf172fbf1ef90417717bf8c6fbeb42313e291a996045dc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 GB (1439733919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb66a1d2de8f2df09890dec02b84b31051d2d60a021e032424a0df6295dd02bd`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Fri, 24 Jul 2020 14:38:19 GMT
ADD file:7d9bbf45a5b2510d44d3206a028cf6502757884d49e46d3d2e6356c3a92c4309 in / 
# Fri, 24 Jul 2020 14:38:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:38:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:38:22 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 17:09:05 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Fri, 24 Jul 2020 17:09:06 GMT
ENV TERM=xterm
# Fri, 24 Jul 2020 17:13:24 GMT
RUN apt-get update && apt-get install -y     wget     vim     locales     procps     net-tools     zip     unzip     openjdk-8-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Fri, 24 Jul 2020 17:13:26 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Fri, 24 Jul 2020 17:13:29 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Fri, 24 Jul 2020 17:13:29 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Fri, 24 Jul 2020 17:13:32 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Fri, 24 Jul 2020 17:13:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 24 Jul 2020 17:13:32 GMT
ENV LANGUAGE=en_US.UTF-8
# Fri, 24 Jul 2020 17:13:32 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 24 Jul 2020 17:13:33 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 24 Jul 2020 17:13:34 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 24 Jul 2020 17:13:34 GMT
ENV JAVA_HOME=/docker-java-home
# Fri, 24 Jul 2020 17:13:34 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Fri, 24 Jul 2020 17:13:35 GMT
ENV JBOSS_HOME=/opt/wildfly
# Fri, 24 Jul 2020 17:13:35 GMT
ENV SILVERPEAS_VERSION=6.1
# Fri, 24 Jul 2020 17:13:35 GMT
ENV WILDFLY_VERSION=18.0.1
# Fri, 24 Jul 2020 17:13:35 GMT
LABEL name=Silverpeas 6 description=Image to install and to run Silverpeas 6 vendor=Silverpeas version=6.1 build=2
# Fri, 24 Jul 2020 17:13:44 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc http://download.jboss.org/wildfly/${WILDFLY_VERSION}.Final/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Fri, 24 Jul 2020 17:13:45 GMT
COPY file:4d0e637a3e1ce0b8143795fd5df1997a7ee18fba27382849ed23e9ecb8142009 in /root/.m2/ 
# Fri, 24 Jul 2020 17:13:45 GMT
COPY file:473bf75b335a39b6b4b39c64cd151bd8ed3d3e33da73b8124e537a5db1fad3d6 in /opt/silverpeas/bin/ 
# Fri, 24 Jul 2020 17:13:45 GMT
WORKDIR /opt/silverpeas/bin
# Fri, 24 Jul 2020 17:13:45 GMT
COPY file:b54156953ecf6c3259f3b3d2885a784847c0996fd145c0f7ccef25182725511f in /opt/ 
# Fri, 24 Jul 2020 17:13:46 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Fri, 24 Jul 2020 17:15:19 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle   && ./silverpeas construct   && mv ../migrations/db/h2/busCore/up040/alter-table.sql ../migrations/db/h2/busCore/up040/alter_table.sql   && rm ../log/build-*   && touch .install
# Fri, 24 Jul 2020 17:15:20 GMT
EXPOSE 8000 9990
# Fri, 24 Jul 2020 17:15:20 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Fri, 24 Jul 2020 17:15:20 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:7595c8c21622ea8a8b9778972e26dbbe063f7a1c4b0a28a80a34ebb3d343b586`  
		Last Modified: Mon, 13 Jul 2020 15:46:50 GMT  
		Size: 26.7 MB (26697127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13af8ca898f36af68711cb67c345f65046a78ccd802453f4b129adf9205b1f8`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 35.4 KB (35364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70799171ddba93a611490ba3557d782714b3f4da8963d49ac8726786ba8274a5`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c12202c5ef07dc9eb8f9d9e71407064684ed70f8c4040b62679b7d30200840`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7564b024498d80200e283f6a6b1fc19c95efbaae98f4e02e3c7a7331534facc5`  
		Last Modified: Fri, 24 Jul 2020 17:22:53 GMT  
		Size: 491.3 MB (491317367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6875490b53741ba3a5ed5a7280c480529d27870530ad7aa9ff71866e6a2d51b`  
		Last Modified: Fri, 24 Jul 2020 17:21:25 GMT  
		Size: 4.0 MB (3994021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd1006265dfb80de28918479f7f15d22ad9422d74dbc5186844f33d37a35530`  
		Last Modified: Fri, 24 Jul 2020 17:21:25 GMT  
		Size: 7.1 MB (7146632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a36d7783ebd9868cdaef5325e478a453c896d1433800c19df9be265cb244258`  
		Last Modified: Fri, 24 Jul 2020 17:21:23 GMT  
		Size: 490.7 KB (490692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b4afe11c37ac07c4545df4fd7d50f99ee07708273753686faa6387dcbf01d4`  
		Last Modified: Fri, 24 Jul 2020 17:21:23 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85bc2fe25508dee8736b91488503d03a20db2c891d0325c2b15dad23ddcba01f`  
		Last Modified: Fri, 24 Jul 2020 17:21:23 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d64b1d0d7c896d07f932d9e3df3803926b02af1e323ab0bd15c1706d11eccaf`  
		Last Modified: Fri, 24 Jul 2020 17:21:38 GMT  
		Size: 190.5 MB (190469477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16d5fbab7bbee411171e75a6ae4bfb04d1b1e66541bce7f777db4d6c2143a1d`  
		Last Modified: Fri, 24 Jul 2020 17:21:22 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1e744d3dfd9986f4b08b8d053b8b289414a7ade9946a2a4ffc7bb5cf197fed`  
		Last Modified: Fri, 24 Jul 2020 17:21:21 GMT  
		Size: 663.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e16dc504e012fb2e8139eb3fd4d3d9df1a75325c1754fd1d6f1a1988f935f2f`  
		Last Modified: Fri, 24 Jul 2020 17:21:21 GMT  
		Size: 877.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79407ab7afdb562b5f37e55dbaa5fbd3c5017562342b74602964da7de87225c4`  
		Last Modified: Fri, 24 Jul 2020 17:21:22 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50c1cac2c939ddfcd6d55cfb23f24e40f106169cff83fcb8fe4f057c310b43f`  
		Last Modified: Fri, 24 Jul 2020 17:22:06 GMT  
		Size: 719.6 MB (719579525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `silverpeas:latest`

```console
$ docker pull silverpeas@sha256:321a007b1100df56b705292b67bb19244394d3ff134d7502681a8685fa3f1dc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `silverpeas:latest` - linux; amd64

```console
$ docker pull silverpeas@sha256:2e435049ab3c10eb77bf172fbf1ef90417717bf8c6fbeb42313e291a996045dc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 GB (1439733919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb66a1d2de8f2df09890dec02b84b31051d2d60a021e032424a0df6295dd02bd`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Fri, 24 Jul 2020 14:38:19 GMT
ADD file:7d9bbf45a5b2510d44d3206a028cf6502757884d49e46d3d2e6356c3a92c4309 in / 
# Fri, 24 Jul 2020 14:38:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:38:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:38:22 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 17:09:05 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Fri, 24 Jul 2020 17:09:06 GMT
ENV TERM=xterm
# Fri, 24 Jul 2020 17:13:24 GMT
RUN apt-get update && apt-get install -y     wget     vim     locales     procps     net-tools     zip     unzip     openjdk-8-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Fri, 24 Jul 2020 17:13:26 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Fri, 24 Jul 2020 17:13:29 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Fri, 24 Jul 2020 17:13:29 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Fri, 24 Jul 2020 17:13:32 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Fri, 24 Jul 2020 17:13:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 24 Jul 2020 17:13:32 GMT
ENV LANGUAGE=en_US.UTF-8
# Fri, 24 Jul 2020 17:13:32 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 24 Jul 2020 17:13:33 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 24 Jul 2020 17:13:34 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 24 Jul 2020 17:13:34 GMT
ENV JAVA_HOME=/docker-java-home
# Fri, 24 Jul 2020 17:13:34 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Fri, 24 Jul 2020 17:13:35 GMT
ENV JBOSS_HOME=/opt/wildfly
# Fri, 24 Jul 2020 17:13:35 GMT
ENV SILVERPEAS_VERSION=6.1
# Fri, 24 Jul 2020 17:13:35 GMT
ENV WILDFLY_VERSION=18.0.1
# Fri, 24 Jul 2020 17:13:35 GMT
LABEL name=Silverpeas 6 description=Image to install and to run Silverpeas 6 vendor=Silverpeas version=6.1 build=2
# Fri, 24 Jul 2020 17:13:44 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc http://download.jboss.org/wildfly/${WILDFLY_VERSION}.Final/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Fri, 24 Jul 2020 17:13:45 GMT
COPY file:4d0e637a3e1ce0b8143795fd5df1997a7ee18fba27382849ed23e9ecb8142009 in /root/.m2/ 
# Fri, 24 Jul 2020 17:13:45 GMT
COPY file:473bf75b335a39b6b4b39c64cd151bd8ed3d3e33da73b8124e537a5db1fad3d6 in /opt/silverpeas/bin/ 
# Fri, 24 Jul 2020 17:13:45 GMT
WORKDIR /opt/silverpeas/bin
# Fri, 24 Jul 2020 17:13:45 GMT
COPY file:b54156953ecf6c3259f3b3d2885a784847c0996fd145c0f7ccef25182725511f in /opt/ 
# Fri, 24 Jul 2020 17:13:46 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Fri, 24 Jul 2020 17:15:19 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle   && ./silverpeas construct   && mv ../migrations/db/h2/busCore/up040/alter-table.sql ../migrations/db/h2/busCore/up040/alter_table.sql   && rm ../log/build-*   && touch .install
# Fri, 24 Jul 2020 17:15:20 GMT
EXPOSE 8000 9990
# Fri, 24 Jul 2020 17:15:20 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Fri, 24 Jul 2020 17:15:20 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:7595c8c21622ea8a8b9778972e26dbbe063f7a1c4b0a28a80a34ebb3d343b586`  
		Last Modified: Mon, 13 Jul 2020 15:46:50 GMT  
		Size: 26.7 MB (26697127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13af8ca898f36af68711cb67c345f65046a78ccd802453f4b129adf9205b1f8`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 35.4 KB (35364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70799171ddba93a611490ba3557d782714b3f4da8963d49ac8726786ba8274a5`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c12202c5ef07dc9eb8f9d9e71407064684ed70f8c4040b62679b7d30200840`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7564b024498d80200e283f6a6b1fc19c95efbaae98f4e02e3c7a7331534facc5`  
		Last Modified: Fri, 24 Jul 2020 17:22:53 GMT  
		Size: 491.3 MB (491317367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6875490b53741ba3a5ed5a7280c480529d27870530ad7aa9ff71866e6a2d51b`  
		Last Modified: Fri, 24 Jul 2020 17:21:25 GMT  
		Size: 4.0 MB (3994021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd1006265dfb80de28918479f7f15d22ad9422d74dbc5186844f33d37a35530`  
		Last Modified: Fri, 24 Jul 2020 17:21:25 GMT  
		Size: 7.1 MB (7146632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a36d7783ebd9868cdaef5325e478a453c896d1433800c19df9be265cb244258`  
		Last Modified: Fri, 24 Jul 2020 17:21:23 GMT  
		Size: 490.7 KB (490692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b4afe11c37ac07c4545df4fd7d50f99ee07708273753686faa6387dcbf01d4`  
		Last Modified: Fri, 24 Jul 2020 17:21:23 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85bc2fe25508dee8736b91488503d03a20db2c891d0325c2b15dad23ddcba01f`  
		Last Modified: Fri, 24 Jul 2020 17:21:23 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d64b1d0d7c896d07f932d9e3df3803926b02af1e323ab0bd15c1706d11eccaf`  
		Last Modified: Fri, 24 Jul 2020 17:21:38 GMT  
		Size: 190.5 MB (190469477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16d5fbab7bbee411171e75a6ae4bfb04d1b1e66541bce7f777db4d6c2143a1d`  
		Last Modified: Fri, 24 Jul 2020 17:21:22 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1e744d3dfd9986f4b08b8d053b8b289414a7ade9946a2a4ffc7bb5cf197fed`  
		Last Modified: Fri, 24 Jul 2020 17:21:21 GMT  
		Size: 663.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e16dc504e012fb2e8139eb3fd4d3d9df1a75325c1754fd1d6f1a1988f935f2f`  
		Last Modified: Fri, 24 Jul 2020 17:21:21 GMT  
		Size: 877.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79407ab7afdb562b5f37e55dbaa5fbd3c5017562342b74602964da7de87225c4`  
		Last Modified: Fri, 24 Jul 2020 17:21:22 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50c1cac2c939ddfcd6d55cfb23f24e40f106169cff83fcb8fe4f057c310b43f`  
		Last Modified: Fri, 24 Jul 2020 17:22:06 GMT  
		Size: 719.6 MB (719579525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
