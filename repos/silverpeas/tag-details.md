<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `silverpeas`

-	[`silverpeas:6.0.2`](#silverpeas602)
-	[`silverpeas:6.1.3`](#silverpeas613)
-	[`silverpeas:6.2.2`](#silverpeas622)
-	[`silverpeas:latest`](#silverpeaslatest)

## `silverpeas:6.0.2`

```console
$ docker pull silverpeas@sha256:b5c9b1df7911d96406247d7fafc0fedda2244be799e6009cfc621ad7be63b0d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `silverpeas:6.0.2` - linux; amd64

```console
$ docker pull silverpeas@sha256:0a267954f687c0500c46dfdb31408a6ce073f519d6d94b7d46feb8f752bd7cb1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1014925313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d7219f80b96ae15c804beee33c3e2580723de1295e7a534c385361754e37073`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Tue, 31 Aug 2021 01:21:27 GMT
ADD file:11b425d4c08e81a3e0cb2e0345d27cd5fc844dd83f1096af4cc05f635824ff5d in / 
# Tue, 31 Aug 2021 01:21:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 31 Aug 2021 01:21:29 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 01:21:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 31 Aug 2021 01:21:30 GMT
CMD ["/bin/bash"]
# Tue, 31 Aug 2021 02:03:39 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Tue, 31 Aug 2021 02:03:39 GMT
ENV TERM=xterm
# Tue, 31 Aug 2021 02:07:33 GMT
RUN apt-get update && apt-get install -y     wget     locales     procps     net-tools     zip     unzip     openjdk-8-jdk     ffmpeg     imagemagick     ghostscript     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Tue, 31 Aug 2021 02:07:39 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Tue, 31 Aug 2021 02:07:45 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Tue, 31 Aug 2021 02:07:45 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Tue, 31 Aug 2021 02:07:48 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Tue, 31 Aug 2021 02:07:48 GMT
ENV LANG=en_US.UTF-8
# Tue, 31 Aug 2021 02:07:48 GMT
ENV LANGUAGE=en_US.UTF-8
# Tue, 31 Aug 2021 02:07:48 GMT
ENV LC_ALL=en_US.UTF-8
# Tue, 31 Aug 2021 02:07:49 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 31 Aug 2021 02:07:50 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 31 Aug 2021 02:07:50 GMT
ENV JAVA_HOME=/docker-java-home
# Tue, 31 Aug 2021 02:07:50 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Tue, 31 Aug 2021 02:07:51 GMT
ENV JBOSS_HOME=/opt/wildfly
# Tue, 31 Aug 2021 02:07:51 GMT
ENV SILVERPEAS_VERSION=6.0.2
# Tue, 31 Aug 2021 02:07:51 GMT
ENV WILDFLY_VERSION=10.1.0
# Tue, 31 Aug 2021 02:07:51 GMT
LABEL name=Silverpeas 6 description=Image to install and to run Silverpeas 6 vendor=Silverpeas version=6.0.2 build=1
# Tue, 31 Aug 2021 02:08:09 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc http://download.jboss.org/wildfly/${WILDFLY_VERSION}.Final/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Tue, 31 Aug 2021 02:08:10 GMT
COPY file:d12fb4c8fc28235c5621533a9ae0d98ba26e3adf1ffc690da4a6118aa71d8190 in /root/.m2/ 
# Tue, 31 Aug 2021 02:08:10 GMT
WORKDIR /opt/silverpeas/bin
# Tue, 31 Aug 2021 02:08:10 GMT
COPY file:31e3db287bacfa9fb086f2ae49169410b9f0fdf4178bf47d0ebe93621aa996e4 in /opt/ 
# Tue, 31 Aug 2021 02:08:10 GMT
COPY file:5d883339e9add47c37406a038c7747cafede9f81436843206bab5bde7da6e2f6 in /opt/silverpeas/configuration/silverpeas/ 
# Tue, 31 Aug 2021 02:15:29 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ./silverpeas assemble   && rm ../log/build-*   && touch .install
# Tue, 31 Aug 2021 02:15:32 GMT
EXPOSE 8000 9990
# Tue, 31 Aug 2021 02:15:32 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/xmlcomponents/workflows]
# Tue, 31 Aug 2021 02:15:32 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:58690f9b18fca6469a14da4e212c96849469f9b1be6661d2342a4bf01774aa50`  
		Last Modified: Thu, 05 Aug 2021 00:25:05 GMT  
		Size: 46.5 MB (46497548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51569e7c50720acf6860327847fe342a1afbe148d24c529fb81df105e3eed01`  
		Last Modified: Tue, 31 Aug 2021 01:23:09 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8ef40b9ecabc2679fe2419957220c0272a965c5cf7e0269fa1aeeb8c56f2e1`  
		Last Modified: Tue, 31 Aug 2021 01:23:08 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb15d46c38dcd1ea0b1990006c3366ecd10c79d374f341687eb2cb23a2c8672e`  
		Last Modified: Tue, 31 Aug 2021 01:23:08 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75bab7b2978c6f447f4f11629d5abb18105da46a467b3e7fdad602da38a099a`  
		Last Modified: Tue, 31 Aug 2021 02:19:47 GMT  
		Size: 207.5 MB (207457617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae7ad3fb77baf164e811362e174b7f55078faddfb5419581e02ee8be4e22c8cb`  
		Last Modified: Tue, 31 Aug 2021 02:19:19 GMT  
		Size: 4.0 MB (3994087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa21a02eb15eabcb08194dc549f6d2633401a9f02b70a28c42acfb982a2c0892`  
		Last Modified: Tue, 31 Aug 2021 02:19:19 GMT  
		Size: 7.1 MB (7146644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957309a7c22133ea5da921a9e1c440e5db36c1ef29767922a96d0715144a7f3c`  
		Last Modified: Tue, 31 Aug 2021 02:19:15 GMT  
		Size: 845.4 KB (845399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f504f19b2261f336d5fb8ed204508a177d4672a306b41a359f41940d39c67f`  
		Last Modified: Tue, 31 Aug 2021 02:19:15 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07658715bda815de3e29d8e151f013b1b5ef7fc70e9b567fc532bb8bd19e2c04`  
		Last Modified: Tue, 31 Aug 2021 02:19:15 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f600e097c39adc1a81b28bad70ec252868df7c4824d28038502d09de60f0e340`  
		Last Modified: Tue, 31 Aug 2021 02:19:21 GMT  
		Size: 144.3 MB (144284714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa2533c95124d7f6f1f71e873889eb02fb290464f44877ab8db60dc9c58931f`  
		Last Modified: Tue, 31 Aug 2021 02:19:13 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a055b4aee299167cc171b4c496a6fa722dc1cafaffba88430008c4671edfd5d6`  
		Last Modified: Tue, 31 Aug 2021 02:19:12 GMT  
		Size: 809.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f3514ac10d9002bc266d0d7d3916e143b49a339e7cc5249b412b4699987d38`  
		Last Modified: Tue, 31 Aug 2021 02:19:12 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af73964675c4218dd30a52c94723697d58cf2d0cd23cf4a61cb6da0396cf0aa`  
		Last Modified: Tue, 31 Aug 2021 02:19:44 GMT  
		Size: 604.7 MB (604695778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `silverpeas:6.1.3`

```console
$ docker pull silverpeas@sha256:63cae3cb61513bc84ef1e2b5d9b475556a5a048921b19e7315fbedf78db6f7f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `silverpeas:6.1.3` - linux; amd64

```console
$ docker pull silverpeas@sha256:82181611fd9d86f17f34a241b3d56c9d2fcb9d39c581336d7857cc0b2eaacae4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 GB (1426650201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f6c3de89da553188de3bd552e6b5df22947eea5e76d4bfe69f8c9cd3ad9a5fa`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:42 GMT
ADD file:8a4ddbd462c1dd2016c64bd71ea6b5dba2ac4934bfd235a04d55b364666b67d1 in / 
# Tue, 05 Apr 2022 22:20:43 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 03:05:01 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Wed, 06 Apr 2022 03:05:01 GMT
ENV TERM=xterm
# Wed, 06 Apr 2022 03:10:58 GMT
RUN apt-get update && apt-get install -y     wget     locales     procps     net-tools     zip     unzip     openjdk-8-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Wed, 06 Apr 2022 03:11:07 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Wed, 06 Apr 2022 03:11:10 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Wed, 06 Apr 2022 03:11:10 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Wed, 06 Apr 2022 03:11:13 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Wed, 06 Apr 2022 03:11:13 GMT
ENV LANG=en_US.UTF-8
# Wed, 06 Apr 2022 03:11:13 GMT
ENV LANGUAGE=en_US.UTF-8
# Wed, 06 Apr 2022 03:11:13 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 06 Apr 2022 03:11:14 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 06 Apr 2022 03:11:14 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 06 Apr 2022 03:11:14 GMT
ENV JAVA_HOME=/docker-java-home
# Wed, 06 Apr 2022 03:11:14 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Wed, 06 Apr 2022 03:11:14 GMT
ENV JBOSS_HOME=/opt/wildfly
# Wed, 06 Apr 2022 03:11:15 GMT
ENV SILVERPEAS_VERSION=6.1.3
# Wed, 06 Apr 2022 03:11:15 GMT
ENV WILDFLY_VERSION=18.0.1
# Wed, 06 Apr 2022 03:11:15 GMT
LABEL name=Silverpeas 6 description=Image to install and to run Silverpeas 6 vendor=Silverpeas version=6.1.3 build=1
# Wed, 06 Apr 2022 03:12:51 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc http://download.jboss.org/wildfly/${WILDFLY_VERSION}.Final/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Wed, 06 Apr 2022 03:12:51 GMT
COPY file:4d0e637a3e1ce0b8143795fd5df1997a7ee18fba27382849ed23e9ecb8142009 in /root/.m2/ 
# Wed, 06 Apr 2022 03:12:51 GMT
WORKDIR /opt/silverpeas/bin
# Wed, 06 Apr 2022 03:12:52 GMT
COPY file:bd0a4d5e9017df7c7d4b9ba1011c737b2e2fcbe0966662e3315fabb5498b8aa3 in /opt/ 
# Wed, 06 Apr 2022 03:12:52 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Wed, 06 Apr 2022 03:15:48 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ./silverpeas construct   && rm ../log/build-*   && touch .install
# Wed, 06 Apr 2022 03:15:51 GMT
EXPOSE 8000 9990
# Wed, 06 Apr 2022 03:15:51 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Wed, 06 Apr 2022 03:15:52 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:08a6abff89437fab99b52abbefed82ea907f12845c30eeb94f6b93c69be93166`  
		Last Modified: Tue, 05 Apr 2022 13:10:59 GMT  
		Size: 26.7 MB (26708938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2f6aa2dbc0bff6bd0821aead4f1d44e35e2e511cbca90c65a2e4deda8628a1`  
		Last Modified: Wed, 06 Apr 2022 03:19:05 GMT  
		Size: 481.6 MB (481552714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bf8d2356b98575e43c83cf86e742230cedfc830dd57ef192c71639ffe194fb`  
		Last Modified: Wed, 06 Apr 2022 03:18:00 GMT  
		Size: 4.0 MB (3994090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3109f13b8c7dca512db5487073761a16901dd75fe82f204ab592b767cb3b4453`  
		Last Modified: Wed, 06 Apr 2022 03:18:00 GMT  
		Size: 7.1 MB (7146660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23f139355647233dbd2bb824607bec1d74f659e544707d46b4e78ebba47ad82`  
		Last Modified: Wed, 06 Apr 2022 03:17:56 GMT  
		Size: 490.7 KB (490691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:043cfbcb38cad9a6e44135f1f6c1cf422cc83544ce301e0a67eef7179b6c58fc`  
		Last Modified: Wed, 06 Apr 2022 03:17:56 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb5d892269dc8ee43a0172ae467dd4758cbd66f86f71aeb23df1a54ddcbf121d`  
		Last Modified: Wed, 06 Apr 2022 03:17:56 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1837316a5e5b8726a4ad8ba884800cffedb8cac411a269092063bb343dd414`  
		Last Modified: Wed, 06 Apr 2022 03:18:06 GMT  
		Size: 190.5 MB (190469451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3474c8ff223b0cc02d4de47c9a433bc5a6c90175d972081d6bef00d76a7284fa`  
		Last Modified: Wed, 06 Apr 2022 03:17:54 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362520a272b8944aa926281f356b9d2f7afb6a460fdc98467bda66a9b72b71ea`  
		Last Modified: Wed, 06 Apr 2022 03:17:54 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6abc0deda3a640f437bfd05253c06dd77b8b28408393d22c5758f6238068d48`  
		Last Modified: Wed, 06 Apr 2022 03:17:54 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a203d744eaa5f9f9da37841b736d9583930d87e8b3cd877a249c17a6b69bc6e3`  
		Last Modified: Wed, 06 Apr 2022 03:18:30 GMT  
		Size: 716.3 MB (716285731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `silverpeas:6.2.2`

```console
$ docker pull silverpeas@sha256:1d259d8f5ccf04d4f6907a5134463d0f167bb0328d1310d13cb66f153a990320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `silverpeas:6.2.2` - linux; amd64

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
