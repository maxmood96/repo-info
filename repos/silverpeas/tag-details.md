<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `silverpeas`

-	[`silverpeas:6.0.2`](#silverpeas602)
-	[`silverpeas:6.1.2`](#silverpeas612)
-	[`silverpeas:6.2`](#silverpeas62)
-	[`silverpeas:latest`](#silverpeaslatest)

## `silverpeas:6.0.2`

```console
$ docker pull silverpeas@sha256:958ec57365c19a0aa4cd779fc209a529d5dcbcf631c415265391471b1826f2c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `silverpeas:6.0.2` - linux; amd64

```console
$ docker pull silverpeas@sha256:418139f1b60235429e59466553b9c650fd3fd23ec6e9767efcab4cd03e3782f3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1014322051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f35f44045b83564556ad9e5b051a6b988f0c8d7151a21b80cfe39d95fe3e804`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Thu, 21 Jan 2021 03:39:31 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 21 Jan 2021 03:39:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:39:34 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:39:35 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:39:36 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 10:41:19 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Thu, 21 Jan 2021 10:41:19 GMT
ENV TERM=xterm
# Thu, 21 Jan 2021 10:43:24 GMT
RUN apt-get update && apt-get install -y     wget     locales     procps     net-tools     zip     unzip     openjdk-8-jdk     ffmpeg     imagemagick     ghostscript     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Thu, 21 Jan 2021 10:43:27 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Thu, 21 Jan 2021 10:43:30 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Thu, 21 Jan 2021 10:43:31 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Thu, 21 Jan 2021 10:43:34 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Thu, 21 Jan 2021 10:43:34 GMT
ENV LANG=en_US.UTF-8
# Thu, 21 Jan 2021 10:43:34 GMT
ENV LANGUAGE=en_US.UTF-8
# Thu, 21 Jan 2021 10:43:34 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 21 Jan 2021 10:43:35 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 21 Jan 2021 10:43:36 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Thu, 21 Jan 2021 10:43:36 GMT
ENV JAVA_HOME=/docker-java-home
# Thu, 21 Jan 2021 10:43:36 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Thu, 21 Jan 2021 10:43:37 GMT
ENV JBOSS_HOME=/opt/wildfly
# Thu, 21 Jan 2021 10:43:37 GMT
ENV SILVERPEAS_VERSION=6.0.2
# Thu, 21 Jan 2021 10:43:37 GMT
ENV WILDFLY_VERSION=10.1.0
# Thu, 21 Jan 2021 10:43:37 GMT
LABEL name=Silverpeas 6 description=Image to install and to run Silverpeas 6 vendor=Silverpeas version=6.0.2 build=1
# Thu, 21 Jan 2021 10:43:46 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc http://download.jboss.org/wildfly/${WILDFLY_VERSION}.Final/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Thu, 21 Jan 2021 10:43:46 GMT
COPY file:d12fb4c8fc28235c5621533a9ae0d98ba26e3adf1ffc690da4a6118aa71d8190 in /root/.m2/ 
# Thu, 21 Jan 2021 10:43:46 GMT
WORKDIR /opt/silverpeas/bin
# Thu, 21 Jan 2021 10:43:46 GMT
COPY file:31e3db287bacfa9fb086f2ae49169410b9f0fdf4178bf47d0ebe93621aa996e4 in /opt/ 
# Thu, 21 Jan 2021 10:43:47 GMT
COPY file:5d883339e9add47c37406a038c7747cafede9f81436843206bab5bde7da6e2f6 in /opt/silverpeas/configuration/silverpeas/ 
# Thu, 21 Jan 2021 10:48:22 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ./silverpeas assemble   && rm ../log/build-*   && touch .install
# Thu, 21 Jan 2021 10:48:23 GMT
EXPOSE 8000 9990
# Thu, 21 Jan 2021 10:48:23 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/xmlcomponents/workflows]
# Thu, 21 Jan 2021 10:48:24 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfa26c6b9c9d1ccbcb1eaa65befa376805d9324174ac580ca76fdedc3575f54`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba7bf18aa406cb7dc372ac732de222b04d1c824ff1705d8900831c3d1361ff5`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6ec688ebe374ea7d89ce967576d221a177ebd2c02ca9f053197f954102e30b`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485d6cc6deeb0e6aaff53d82980aff7608d697d87a1ffe69cf09996f7ad9c2e1`  
		Last Modified: Thu, 21 Jan 2021 10:51:16 GMT  
		Size: 207.4 MB (207389840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d65be3921226b9d9a5408d2e7dea1fd6503f1fc97e312facffd7b06bfd41226`  
		Last Modified: Thu, 21 Jan 2021 10:50:39 GMT  
		Size: 4.0 MB (3994034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d9ff6825183c27656c9e2ae60ced8a2cf7df094b0824992f45538b77dd8545`  
		Last Modified: Thu, 21 Jan 2021 10:50:39 GMT  
		Size: 7.1 MB (7146616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d2f0e81b1afd6c80f57f3f9ed6d71cadf0da0046715948bff62ddbfc4e6828`  
		Last Modified: Thu, 21 Jan 2021 10:50:38 GMT  
		Size: 845.4 KB (845413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea9fe0e5091cf32faddec0d40906e6768f651680e42ef718d92478067935571`  
		Last Modified: Thu, 21 Jan 2021 10:50:35 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d69ab684f108a7e4a189f9bd219dcff77294a7f6e9593b2beee6f43b17d423`  
		Last Modified: Thu, 21 Jan 2021 10:50:35 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991b03265f7d07e4af469c173551d9fb53287a53a77a08821e6159a0e98df63f`  
		Last Modified: Thu, 21 Jan 2021 10:50:46 GMT  
		Size: 144.3 MB (144284541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a5baa6ccc140c0d7705472ecddd0a4db73f6c4c994e0ea08f25b57e077dd36`  
		Last Modified: Thu, 21 Jan 2021 10:50:34 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2293c265ff151f607fc523cc2e490378ad978a3f436c51e77b558da5bf8cfce`  
		Last Modified: Thu, 21 Jan 2021 10:50:34 GMT  
		Size: 808.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3091881f974323e6093ac70761f000f0ff7892e05df79448bc29791848086f3`  
		Last Modified: Thu, 21 Jan 2021 10:50:34 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9079e76782c1dafcd2f9294150fab265a8e7c2f44b2cd61844586190fade8686`  
		Last Modified: Thu, 21 Jan 2021 10:51:13 GMT  
		Size: 604.7 MB (604695746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `silverpeas:6.1.2`

```console
$ docker pull silverpeas@sha256:f47a0d674c1edbddede67f199fc9a3f475f049e061d52fbc9a1127a2cf5da72b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `silverpeas:6.1.2` - linux; amd64

```console
$ docker pull silverpeas@sha256:9033bc635ddaa69b4b6d4aa1b5021e9b9107b2716f30a1f514eb00307bff011d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 GB (1426642202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173a0b3ec001e863a171575bc2a29a6f6aa80a99ca159fb2f2fae77a8a982a90`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:26 GMT
ADD file:d65963eb4f4b3a8c8e57119725a91036e8932a3e8f604e7edc21ff9665472da9 in / 
# Thu, 04 Mar 2021 02:24:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:28 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:29 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 04:52:22 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Thu, 04 Mar 2021 04:52:22 GMT
ENV TERM=xterm
# Thu, 04 Mar 2021 04:57:01 GMT
RUN apt-get update && apt-get install -y     wget     locales     procps     net-tools     zip     unzip     openjdk-8-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Thu, 04 Mar 2021 04:57:06 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Thu, 04 Mar 2021 04:57:11 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Thu, 04 Mar 2021 04:57:13 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Thu, 04 Mar 2021 04:57:17 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Thu, 04 Mar 2021 04:57:17 GMT
ENV LANG=en_US.UTF-8
# Thu, 04 Mar 2021 04:57:18 GMT
ENV LANGUAGE=en_US.UTF-8
# Thu, 04 Mar 2021 04:57:18 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 04 Mar 2021 04:57:19 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 04 Mar 2021 04:57:20 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Thu, 04 Mar 2021 04:57:20 GMT
ENV JAVA_HOME=/docker-java-home
# Thu, 04 Mar 2021 04:57:20 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Thu, 04 Mar 2021 04:57:20 GMT
ENV JBOSS_HOME=/opt/wildfly
# Thu, 04 Mar 2021 04:57:20 GMT
ENV SILVERPEAS_VERSION=6.1.2
# Thu, 04 Mar 2021 04:57:21 GMT
ENV WILDFLY_VERSION=18.0.1
# Thu, 04 Mar 2021 04:57:21 GMT
LABEL name=Silverpeas 6 description=Image to install and to run Silverpeas 6 vendor=Silverpeas version=6.1.2 build=1
# Thu, 04 Mar 2021 04:59:00 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc http://download.jboss.org/wildfly/${WILDFLY_VERSION}.Final/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Thu, 04 Mar 2021 04:59:01 GMT
COPY file:4d0e637a3e1ce0b8143795fd5df1997a7ee18fba27382849ed23e9ecb8142009 in /root/.m2/ 
# Thu, 04 Mar 2021 04:59:01 GMT
WORKDIR /opt/silverpeas/bin
# Thu, 04 Mar 2021 04:59:01 GMT
COPY file:bd0a4d5e9017df7c7d4b9ba1011c737b2e2fcbe0966662e3315fabb5498b8aa3 in /opt/ 
# Thu, 04 Mar 2021 04:59:01 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Thu, 04 Mar 2021 05:00:29 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ./silverpeas construct   && rm ../log/build-*   && touch .install
# Thu, 04 Mar 2021 05:00:30 GMT
EXPOSE 8000 9990
# Thu, 04 Mar 2021 05:00:30 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Thu, 04 Mar 2021 05:00:30 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:92dc2a97ff99354714f17180401813eb3073e4f62a67643d66b461505a604cbe`  
		Last Modified: Mon, 01 Mar 2021 16:09:46 GMT  
		Size: 26.7 MB (26710147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be13a9d27eb82db7e9c7f3a76f70919a2d690e34e78cda8cae60161b0f5e9137`  
		Last Modified: Thu, 04 Mar 2021 02:25:42 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8299583700ab4cc65a0126f99ca6f2b836a097dedcc64270094bea59b8b4306`  
		Last Modified: Thu, 04 Mar 2021 02:25:41 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2d28560a4dfaf3b7b95272c3d48e9fcd25788fa947ce55a01aa80062d6b4a6`  
		Last Modified: Thu, 04 Mar 2021 05:04:30 GMT  
		Size: 481.6 MB (481557214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:862e998872c4e850fa59e4e109420df69d2af93d7d0309f2a3a6f38b36eb173d`  
		Last Modified: Thu, 04 Mar 2021 05:03:11 GMT  
		Size: 4.0 MB (3994017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c30f907c0398d8a8bd107ffd51a5fe5e3c9d499e3ff9bb4d4e57f961ac959d`  
		Last Modified: Thu, 04 Mar 2021 05:03:11 GMT  
		Size: 7.1 MB (7146627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae101afe5a4307b28fbbdd65ca8a603e6d2382e997950b6336c8c1321a818a0`  
		Last Modified: Thu, 04 Mar 2021 05:03:09 GMT  
		Size: 490.7 KB (490690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed51da3991527088d7b83a25ba2ca3266f73825b4b61390001850578ac99525`  
		Last Modified: Thu, 04 Mar 2021 05:03:09 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14622575e40c8fa71bd4c7f263cdc050ceafceb67f6965396f3a539cec30f171`  
		Last Modified: Thu, 04 Mar 2021 05:03:08 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46856f04ec621f854ef082fc8e8ed3f838d65b6f9b3aa74e9fad73bad0e50b26`  
		Last Modified: Thu, 04 Mar 2021 05:03:23 GMT  
		Size: 190.5 MB (190469472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d85ef704664bec6d7e3c1fb1fb71ded6ae9ac174c74fdb35a768d25f34d30859`  
		Last Modified: Thu, 04 Mar 2021 05:03:07 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5afcefffc1044f0ca1255af0a2380e8d7fd3235e74443ef93d3d9994cdf46d`  
		Last Modified: Thu, 04 Mar 2021 05:03:07 GMT  
		Size: 761.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c86289b7d7db365c669928397908509871c5c44ed962c55442a2ec2c8b3579d`  
		Last Modified: Thu, 04 Mar 2021 05:03:07 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64c7cf48c7a09b0a94b8be1ca31255a93274c6d114cf8e5dc0b18d8d31362c01`  
		Last Modified: Thu, 04 Mar 2021 05:03:54 GMT  
		Size: 716.3 MB (716271103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `silverpeas:6.2`

```console
$ docker pull silverpeas@sha256:649d44ba4791b7c28c1d71b9a71a5dee0eb9a7568ffc8ec20a45138203fe37d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `silverpeas:6.2` - linux; amd64

```console
$ docker pull silverpeas@sha256:52c6ba290593f1d7172cb148c886cef9948b9051c33e58d3fe9c7aeb209bc52b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1865873708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee3509afef300112fce81d12dbce368c99a63078adfabe83d4a12cd1ed52fa7`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:39 GMT
ADD file:c77338d21e6d1587df92d76a2b0a5c36f0e026ac1640b5cddefb1bf8db8a1204 in / 
# Thu, 04 Mar 2021 02:24:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:42 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:42 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 04:42:43 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Thu, 04 Mar 2021 04:42:43 GMT
ENV TERM=xterm
# Thu, 04 Mar 2021 04:47:42 GMT
RUN apt-get update   && apt-get install -y tzdata   && apt-get install -y     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Thu, 04 Mar 2021 04:47:47 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Thu, 04 Mar 2021 04:47:50 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Thu, 04 Mar 2021 04:47:50 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Thu, 04 Mar 2021 04:48:35 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Thu, 04 Mar 2021 04:48:35 GMT
ENV LANG=en_US.UTF-8
# Thu, 04 Mar 2021 04:48:36 GMT
ENV LANGUAGE=en_US.UTF-8
# Thu, 04 Mar 2021 04:48:36 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 04 Mar 2021 04:48:37 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 04 Mar 2021 04:48:38 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Thu, 04 Mar 2021 04:48:38 GMT
ENV JAVA_HOME=/docker-java-home
# Thu, 04 Mar 2021 04:48:38 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Thu, 04 Mar 2021 04:48:38 GMT
ENV JBOSS_HOME=/opt/wildfly
# Thu, 04 Mar 2021 04:48:38 GMT
ENV SILVERPEAS_VERSION=6.2
# Thu, 04 Mar 2021 04:48:39 GMT
ENV WILDFLY_VERSION=20.0.1
# Thu, 04 Mar 2021 04:48:39 GMT
LABEL name=Silverpeas 6.2 description=Image to install and to run Silverpeas 6.2 vendor=Silverpeas version=6.2 build=1
# Thu, 04 Mar 2021 04:50:21 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc http://download.jboss.org/wildfly/${WILDFLY_VERSION}.Final/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Thu, 04 Mar 2021 04:50:22 GMT
COPY file:4d0e637a3e1ce0b8143795fd5df1997a7ee18fba27382849ed23e9ecb8142009 in /root/.m2/ 
# Thu, 04 Mar 2021 04:50:22 GMT
COPY file:473bf75b335a39b6b4b39c64cd151bd8ed3d3e33da73b8124e537a5db1fad3d6 in /opt/silverpeas/bin/ 
# Thu, 04 Mar 2021 04:50:22 GMT
WORKDIR /opt/silverpeas/bin
# Thu, 04 Mar 2021 04:50:22 GMT
COPY file:b54156953ecf6c3259f3b3d2885a784847c0996fd145c0f7ccef25182725511f in /opt/ 
# Thu, 04 Mar 2021 04:50:23 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Thu, 04 Mar 2021 04:52:02 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle   && ./silverpeas construct   && rm ../log/build-*   && touch .install
# Thu, 04 Mar 2021 04:52:03 GMT
EXPOSE 8000 9990
# Thu, 04 Mar 2021 04:52:03 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Thu, 04 Mar 2021 04:52:03 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:5d3b2c2d21bba59850dac063bcbb574fddcb6aefb444ffcc63843355d878d54f`  
		Last Modified: Mon, 22 Feb 2021 16:09:51 GMT  
		Size: 28.6 MB (28567785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc2062ea6672189447be7510fb7d5bc2ef2fda234a04b457d9dda4bba5cc635`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75adf526d75b82eb4f9981cce0b23608ebe6ab85c3e1ab2441f29b302d2f9aa8`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de244dbd20fd6497b027902ddc16101a67726c3275e8fd58257be7afc42a7306`  
		Last Modified: Thu, 04 Mar 2021 05:02:57 GMT  
		Size: 904.9 MB (904902160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfdfea2ce8b1839ddadcde4e1f365a88b0fac835b027c1914cc5a7804a65e4f1`  
		Last Modified: Thu, 04 Mar 2021 05:01:00 GMT  
		Size: 4.0 MB (3994013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd2f4461ba4700bc81bd56be65f5409dfea1a82f2277c6f269ac3f2135cf6ee`  
		Last Modified: Thu, 04 Mar 2021 05:01:01 GMT  
		Size: 7.1 MB (7146630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d215b8b3d294ea157fb140040217e3fd76a738a9c3c424fb160d70e8a1748d`  
		Last Modified: Thu, 04 Mar 2021 05:00:58 GMT  
		Size: 2.5 MB (2534369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852e91cbacf1268c647f0b7ef96a653334c3b5aab91bae75fcb8c96642646a1a`  
		Last Modified: Thu, 04 Mar 2021 05:00:57 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d2210cfba25064c64c1b5bc53c047599a3d207b3a134671016ba05a74257b1d`  
		Last Modified: Thu, 04 Mar 2021 05:00:57 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23af7f98ac790361171919b526488beeec10e42175af3aababc3b781e550b407`  
		Last Modified: Thu, 04 Mar 2021 05:01:13 GMT  
		Size: 196.8 MB (196773976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4792cba046144abea515c5f9d403263bc5630eb8122584cb03dedbc3bc30ad68`  
		Last Modified: Thu, 04 Mar 2021 05:00:55 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4467bc854f2009c7e7a29c9d0bbd2ea2824463900245c2392f7518b33fcfd040`  
		Last Modified: Thu, 04 Mar 2021 05:00:55 GMT  
		Size: 658.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:221884a449612b91f1aca6a9b6a15248ce97cb5fed3d50f19e9d50c56e0602f0`  
		Last Modified: Thu, 04 Mar 2021 05:00:56 GMT  
		Size: 876.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e88ecad371a0d6b2be8856f2dcbff16acabe6c78050282e45c313654d585326`  
		Last Modified: Thu, 04 Mar 2021 05:00:55 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df7a30538379fe4ada35ac6bb08cfcffb4819158df590bb619876198d2b8139`  
		Last Modified: Thu, 04 Mar 2021 05:01:42 GMT  
		Size: 722.0 MB (721951066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `silverpeas:latest`

```console
$ docker pull silverpeas@sha256:649d44ba4791b7c28c1d71b9a71a5dee0eb9a7568ffc8ec20a45138203fe37d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `silverpeas:latest` - linux; amd64

```console
$ docker pull silverpeas@sha256:52c6ba290593f1d7172cb148c886cef9948b9051c33e58d3fe9c7aeb209bc52b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1865873708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee3509afef300112fce81d12dbce368c99a63078adfabe83d4a12cd1ed52fa7`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Thu, 04 Mar 2021 02:24:39 GMT
ADD file:c77338d21e6d1587df92d76a2b0a5c36f0e026ac1640b5cddefb1bf8db8a1204 in / 
# Thu, 04 Mar 2021 02:24:40 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 04 Mar 2021 02:24:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 04 Mar 2021 02:24:42 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 04 Mar 2021 02:24:42 GMT
CMD ["/bin/bash"]
# Thu, 04 Mar 2021 04:42:43 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Thu, 04 Mar 2021 04:42:43 GMT
ENV TERM=xterm
# Thu, 04 Mar 2021 04:47:42 GMT
RUN apt-get update   && apt-get install -y tzdata   && apt-get install -y     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Thu, 04 Mar 2021 04:47:47 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Thu, 04 Mar 2021 04:47:50 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Thu, 04 Mar 2021 04:47:50 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Thu, 04 Mar 2021 04:48:35 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Thu, 04 Mar 2021 04:48:35 GMT
ENV LANG=en_US.UTF-8
# Thu, 04 Mar 2021 04:48:36 GMT
ENV LANGUAGE=en_US.UTF-8
# Thu, 04 Mar 2021 04:48:36 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 04 Mar 2021 04:48:37 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 04 Mar 2021 04:48:38 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Thu, 04 Mar 2021 04:48:38 GMT
ENV JAVA_HOME=/docker-java-home
# Thu, 04 Mar 2021 04:48:38 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Thu, 04 Mar 2021 04:48:38 GMT
ENV JBOSS_HOME=/opt/wildfly
# Thu, 04 Mar 2021 04:48:38 GMT
ENV SILVERPEAS_VERSION=6.2
# Thu, 04 Mar 2021 04:48:39 GMT
ENV WILDFLY_VERSION=20.0.1
# Thu, 04 Mar 2021 04:48:39 GMT
LABEL name=Silverpeas 6.2 description=Image to install and to run Silverpeas 6.2 vendor=Silverpeas version=6.2 build=1
# Thu, 04 Mar 2021 04:50:21 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc http://download.jboss.org/wildfly/${WILDFLY_VERSION}.Final/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Thu, 04 Mar 2021 04:50:22 GMT
COPY file:4d0e637a3e1ce0b8143795fd5df1997a7ee18fba27382849ed23e9ecb8142009 in /root/.m2/ 
# Thu, 04 Mar 2021 04:50:22 GMT
COPY file:473bf75b335a39b6b4b39c64cd151bd8ed3d3e33da73b8124e537a5db1fad3d6 in /opt/silverpeas/bin/ 
# Thu, 04 Mar 2021 04:50:22 GMT
WORKDIR /opt/silverpeas/bin
# Thu, 04 Mar 2021 04:50:22 GMT
COPY file:b54156953ecf6c3259f3b3d2885a784847c0996fd145c0f7ccef25182725511f in /opt/ 
# Thu, 04 Mar 2021 04:50:23 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Thu, 04 Mar 2021 04:52:02 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle   && ./silverpeas construct   && rm ../log/build-*   && touch .install
# Thu, 04 Mar 2021 04:52:03 GMT
EXPOSE 8000 9990
# Thu, 04 Mar 2021 04:52:03 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Thu, 04 Mar 2021 04:52:03 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:5d3b2c2d21bba59850dac063bcbb574fddcb6aefb444ffcc63843355d878d54f`  
		Last Modified: Mon, 22 Feb 2021 16:09:51 GMT  
		Size: 28.6 MB (28567785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc2062ea6672189447be7510fb7d5bc2ef2fda234a04b457d9dda4bba5cc635`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75adf526d75b82eb4f9981cce0b23608ebe6ab85c3e1ab2441f29b302d2f9aa8`  
		Last Modified: Thu, 04 Mar 2021 02:25:50 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de244dbd20fd6497b027902ddc16101a67726c3275e8fd58257be7afc42a7306`  
		Last Modified: Thu, 04 Mar 2021 05:02:57 GMT  
		Size: 904.9 MB (904902160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfdfea2ce8b1839ddadcde4e1f365a88b0fac835b027c1914cc5a7804a65e4f1`  
		Last Modified: Thu, 04 Mar 2021 05:01:00 GMT  
		Size: 4.0 MB (3994013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd2f4461ba4700bc81bd56be65f5409dfea1a82f2277c6f269ac3f2135cf6ee`  
		Last Modified: Thu, 04 Mar 2021 05:01:01 GMT  
		Size: 7.1 MB (7146630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d215b8b3d294ea157fb140040217e3fd76a738a9c3c424fb160d70e8a1748d`  
		Last Modified: Thu, 04 Mar 2021 05:00:58 GMT  
		Size: 2.5 MB (2534369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852e91cbacf1268c647f0b7ef96a653334c3b5aab91bae75fcb8c96642646a1a`  
		Last Modified: Thu, 04 Mar 2021 05:00:57 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d2210cfba25064c64c1b5bc53c047599a3d207b3a134671016ba05a74257b1d`  
		Last Modified: Thu, 04 Mar 2021 05:00:57 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23af7f98ac790361171919b526488beeec10e42175af3aababc3b781e550b407`  
		Last Modified: Thu, 04 Mar 2021 05:01:13 GMT  
		Size: 196.8 MB (196773976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4792cba046144abea515c5f9d403263bc5630eb8122584cb03dedbc3bc30ad68`  
		Last Modified: Thu, 04 Mar 2021 05:00:55 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4467bc854f2009c7e7a29c9d0bbd2ea2824463900245c2392f7518b33fcfd040`  
		Last Modified: Thu, 04 Mar 2021 05:00:55 GMT  
		Size: 658.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:221884a449612b91f1aca6a9b6a15248ce97cb5fed3d50f19e9d50c56e0602f0`  
		Last Modified: Thu, 04 Mar 2021 05:00:56 GMT  
		Size: 876.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e88ecad371a0d6b2be8856f2dcbff16acabe6c78050282e45c313654d585326`  
		Last Modified: Thu, 04 Mar 2021 05:00:55 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df7a30538379fe4ada35ac6bb08cfcffb4819158df590bb619876198d2b8139`  
		Last Modified: Thu, 04 Mar 2021 05:01:42 GMT  
		Size: 722.0 MB (721951066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
