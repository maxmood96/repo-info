<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `bonita`

-	[`bonita:2021.1`](#bonita20211)
-	[`bonita:7.10`](#bonita710)
-	[`bonita:7.10.6`](#bonita7106)
-	[`bonita:7.11`](#bonita711)
-	[`bonita:7.11.4`](#bonita7114)
-	[`bonita:7.12`](#bonita712)
-	[`bonita:7.12.1`](#bonita7121)
-	[`bonita:latest`](#bonitalatest)

## `bonita:2021.1`

```console
$ docker pull bonita@sha256:32cfa6689575e7983e6a17f1afc8b096aa12369d64b17e357769b45c4d83dc74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2021.1` - linux; amd64

```console
$ docker pull bonita@sha256:b5916584fa8b0223d4f5110fb38f5c7e1d50507c9c06ae7517ff791be50ac988
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237231421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92810c0e9ab24901233e4e22bb664a65b8406726965dddc531f2f5962ac3d59a`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:30 GMT
ADD file:e729fb032bd2f7cde20fb343da0cd358447e8b23028422c123944e8d0be660fa in / 
# Mon, 26 Jul 2021 21:21:31 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:55:51 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 26 Jul 2021 22:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:56:38 GMT
RUN mkdir /opt/custom-init.d/
# Mon, 26 Jul 2021 22:56:40 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Mon, 26 Jul 2021 22:56:43 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Mon, 26 Jul 2021 22:56:43 GMT
ARG BONITA_VERSION
# Mon, 26 Jul 2021 22:57:03 GMT
ARG BRANDING_VERSION
# Mon, 26 Jul 2021 22:57:03 GMT
ARG BONITA_SHA256
# Mon, 26 Jul 2021 22:57:03 GMT
ARG BASE_URL
# Mon, 26 Jul 2021 22:57:03 GMT
ARG BONITA_URL
# Mon, 26 Jul 2021 22:57:03 GMT
ENV BONITA_VERSION=7.12.1
# Mon, 26 Jul 2021 22:57:04 GMT
ENV BRANDING_VERSION=2021.1
# Mon, 26 Jul 2021 22:57:04 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Mon, 26 Jul 2021 22:57:04 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Mon, 26 Jul 2021 22:57:04 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 26 Jul 2021 22:57:05 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Mon, 26 Jul 2021 22:57:05 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Mon, 26 Jul 2021 22:57:06 GMT
RUN mkdir /opt/files
# Mon, 26 Jul 2021 22:57:06 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Mon, 26 Jul 2021 22:57:10 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Mon, 26 Jul 2021 22:57:12 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Mon, 26 Jul 2021 22:57:13 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Mon, 26 Jul 2021 22:57:14 GMT
VOLUME [/opt/bonita]
# Mon, 26 Jul 2021 22:57:14 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Mon, 26 Jul 2021 22:57:14 GMT
EXPOSE 8080
# Mon, 26 Jul 2021 22:57:14 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:feac5306138255e28a9862d3f3d29025d0a4d0648855afe1acd6131af07138ac`  
		Last Modified: Mon, 26 Jul 2021 21:22:52 GMT  
		Size: 26.7 MB (26709039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41fbee9f4b324cc20d8988fa7cab5d9c491c1a9a380342d8846040fa5afe01a`  
		Last Modified: Mon, 26 Jul 2021 22:58:25 GMT  
		Size: 93.5 MB (93519201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ca53056372700c6fbe41da9cb2df900b3b73e9cf784ebadd79e20b3b8080d1`  
		Last Modified: Mon, 26 Jul 2021 22:58:08 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9905bd9bc78f4e660b093c94972b9bfe153be1450b65d1d94a39a66265e9f809`  
		Last Modified: Mon, 26 Jul 2021 22:58:08 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6437ef6648258db0d319ca67287e68abd9d59fd9a13cef685fcf0001eefd77`  
		Last Modified: Mon, 26 Jul 2021 22:58:05 GMT  
		Size: 576.9 KB (576937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6eb19591747c3e652808ab538441ba4b47dc4e60835c762225b47c427ec90aa`  
		Last Modified: Mon, 26 Jul 2021 22:58:38 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb19116d4d9d99e7693af7fd0f393d5a6b46eb766cacef6db42839311df87df`  
		Last Modified: Mon, 26 Jul 2021 22:58:38 GMT  
		Size: 6.9 KB (6942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee45552874f5dc095ab9338e4c91bb15548e9e55d077e57a156c058c4f5b45e`  
		Last Modified: Mon, 26 Jul 2021 22:58:46 GMT  
		Size: 116.4 MB (116415405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e8604ffcc7b25e1d701643f189b9df43053595d0435c1406ab10d73233c0e0`  
		Last Modified: Mon, 26 Jul 2021 22:58:38 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:6fef41ea5e1c154704edff635aa96d95e0f51631f6d0b337dd0502d3028e8953
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226336563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abfa77e4bfcd83636fefc618a3f25a8bec1e977a73c1393b20e51974930f5ecd`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:49 GMT
ADD file:e87e065765ef99e8db25307f469c7481ab480ac5fe6353ae4caf402766f14045 in / 
# Mon, 26 Jul 2021 21:48:50 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:47:04 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 26 Jul 2021 22:47:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:47:27 GMT
RUN mkdir /opt/custom-init.d/
# Mon, 26 Jul 2021 22:47:27 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Mon, 26 Jul 2021 22:47:35 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Mon, 26 Jul 2021 22:47:35 GMT
ARG BONITA_VERSION
# Mon, 26 Jul 2021 22:47:56 GMT
ARG BRANDING_VERSION
# Mon, 26 Jul 2021 22:47:56 GMT
ARG BONITA_SHA256
# Mon, 26 Jul 2021 22:47:56 GMT
ARG BASE_URL
# Mon, 26 Jul 2021 22:47:57 GMT
ARG BONITA_URL
# Mon, 26 Jul 2021 22:47:57 GMT
ENV BONITA_VERSION=7.12.1
# Mon, 26 Jul 2021 22:47:57 GMT
ENV BRANDING_VERSION=2021.1
# Mon, 26 Jul 2021 22:47:57 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Mon, 26 Jul 2021 22:47:57 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Mon, 26 Jul 2021 22:47:57 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 26 Jul 2021 22:47:58 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Mon, 26 Jul 2021 22:47:58 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Mon, 26 Jul 2021 22:47:59 GMT
RUN mkdir /opt/files
# Mon, 26 Jul 2021 22:47:59 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Mon, 26 Jul 2021 22:48:03 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Mon, 26 Jul 2021 22:48:04 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Mon, 26 Jul 2021 22:48:06 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Mon, 26 Jul 2021 22:48:06 GMT
VOLUME [/opt/bonita]
# Mon, 26 Jul 2021 22:48:06 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Mon, 26 Jul 2021 22:48:06 GMT
EXPOSE 8080
# Mon, 26 Jul 2021 22:48:06 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:fda1cca7a3cc2b66c161597f27e151a9b1cab79d73c7c0c2706606813a3e58cf`  
		Last Modified: Mon, 26 Jul 2021 21:50:37 GMT  
		Size: 23.7 MB (23731597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a32c2e693656a5434b587ae1cfac238a95021569769a39d83ef10e89e26121b`  
		Last Modified: Mon, 26 Jul 2021 22:49:21 GMT  
		Size: 85.6 MB (85631763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad214e302609f03f40484c257c896f8ebd558d57ec6c206420d30d631d5372b`  
		Last Modified: Mon, 26 Jul 2021 22:49:09 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9502bfb487c7c8ec156a40e2377f90db8fc718caf311aeded083744517a000a`  
		Last Modified: Mon, 26 Jul 2021 22:49:09 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73e0be58132932de21617b671fbcca74b337f211536ce134caa69deef3762c3`  
		Last Modified: Mon, 26 Jul 2021 22:49:06 GMT  
		Size: 547.0 KB (546952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:604f2973b7d58cdc5ad9de258e3218026fa60cf7e48847f5fdf4534944228b84`  
		Last Modified: Mon, 26 Jul 2021 22:49:34 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd7ba0494738d76004485770de8cffcdedc3552d7b998f873599958d62afd69e`  
		Last Modified: Mon, 26 Jul 2021 22:49:34 GMT  
		Size: 6.9 KB (6941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:057f372f60b20617b2723316908952d57f231b410306e9f1214070e115749ad5`  
		Last Modified: Mon, 26 Jul 2021 22:49:41 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02530942f83aa65323b363a48328cae8256da20797efaee35e8d380d07d5e90f`  
		Last Modified: Mon, 26 Jul 2021 22:49:34 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:6d42098255d7f0cc80c2f0ffb70c5c76e99739651e6aac3c2716d1e8c9ab3bad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233796336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efda9e0b763ba1558488a71d85829892d6d9dcf7a7549ca1cb1052667717c9dc`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 13 Jul 2021 23:21:55 GMT
ADD file:45b627081344651e16f78f7bbb0da81c1dcc0300835ab0f4bdd6dd93621e461d in / 
# Tue, 13 Jul 2021 23:22:00 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 04:23:21 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 14 Jul 2021 04:28:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:28:27 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 14 Jul 2021 04:28:56 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 14 Jul 2021 04:29:11 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 14 Jul 2021 04:29:17 GMT
ARG BONITA_VERSION
# Wed, 14 Jul 2021 04:32:59 GMT
ARG BRANDING_VERSION
# Wed, 14 Jul 2021 04:33:01 GMT
ARG BONITA_SHA256
# Wed, 14 Jul 2021 04:33:08 GMT
ARG BASE_URL
# Wed, 14 Jul 2021 04:33:17 GMT
ARG BONITA_URL
# Wed, 14 Jul 2021 04:33:21 GMT
ENV BONITA_VERSION=7.12.1
# Wed, 14 Jul 2021 04:33:24 GMT
ENV BRANDING_VERSION=2021.1
# Wed, 14 Jul 2021 04:33:39 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Wed, 14 Jul 2021 04:33:45 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Wed, 14 Jul 2021 04:33:52 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 14 Jul 2021 04:33:58 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Wed, 14 Jul 2021 04:34:09 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Wed, 14 Jul 2021 04:34:21 GMT
RUN mkdir /opt/files
# Wed, 14 Jul 2021 04:34:26 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Wed, 14 Jul 2021 04:34:44 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Wed, 14 Jul 2021 04:34:56 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Wed, 14 Jul 2021 04:35:04 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Wed, 14 Jul 2021 04:35:08 GMT
VOLUME [/opt/bonita]
# Wed, 14 Jul 2021 04:35:11 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 14 Jul 2021 04:35:15 GMT
EXPOSE 8080
# Wed, 14 Jul 2021 04:35:21 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:b4e702a7ed6378fce702bcf7ca7d37185cd6d8387370cd090b9dc4bf5844f47c`  
		Last Modified: Tue, 13 Jul 2021 23:27:12 GMT  
		Size: 30.4 MB (30427987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea6d20994673343d11028ac1ac0bcc098d0f1ac3b04655623d2d2cafa4bee8d`  
		Last Modified: Wed, 14 Jul 2021 04:37:02 GMT  
		Size: 86.4 MB (86395354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7a025e3dd302981f640be07c88365b3ddfa8c7d2a818971b050001fa255123`  
		Last Modified: Wed, 14 Jul 2021 04:36:46 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c867ae2580be2a8356c180288cecbeca16488f530908d5ebb203c0c5bf0a99`  
		Last Modified: Wed, 14 Jul 2021 04:36:44 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7732888c6ddf76b2f60aa2ce9638a1b17b4a33dc96c7a969b6b0a3401b8c8568`  
		Last Modified: Wed, 14 Jul 2021 04:36:41 GMT  
		Size: 546.7 KB (546731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01503d0bfb3e8749a1da3e2fe6cbf5e5208d577a78b429c339ba548a3e20f3aa`  
		Last Modified: Wed, 14 Jul 2021 04:37:15 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91434b0d6bc799538f5ccea05a983777aa3db998cee240f7e841f059c8982d1`  
		Last Modified: Wed, 14 Jul 2021 04:37:16 GMT  
		Size: 6.9 KB (6944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ceb99ecfc3b3526d131f1a01116aaaf5821a5a16c59e76ea0e83d14b7c0b5f`  
		Last Modified: Wed, 14 Jul 2021 04:37:26 GMT  
		Size: 116.4 MB (116415405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b028984ead8def425d58ddd729fc1448e107673994a53e44d976baf1ae7ad0`  
		Last Modified: Wed, 14 Jul 2021 04:37:15 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.10`

```console
$ docker pull bonita@sha256:e1d57a765b5dfc4643849c8336c3e6678f7aeda3d8a7c005fdd5f6a461a6ca4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.10` - linux; amd64

```console
$ docker pull bonita@sha256:19110484206360b38152356f2a8869beaa404d141f296d4b90b07620520a4e48
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242333069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf6fe8558cb5bbce5446bcbdd31137f8b97984e5e201773b99b20fd9f6565c54`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:30 GMT
ADD file:e729fb032bd2f7cde20fb343da0cd358447e8b23028422c123944e8d0be660fa in / 
# Mon, 26 Jul 2021 21:21:31 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:53:40 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Mon, 26 Jul 2021 22:55:10 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:55:12 GMT
RUN mkdir /opt/custom-init.d/
# Mon, 26 Jul 2021 22:55:13 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Mon, 26 Jul 2021 22:55:17 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Mon, 26 Jul 2021 22:55:17 GMT
ARG BONITA_VERSION
# Mon, 26 Jul 2021 22:55:18 GMT
ARG BONITA_SHA256
# Mon, 26 Jul 2021 22:55:18 GMT
ARG BASE_URL
# Mon, 26 Jul 2021 22:55:18 GMT
ARG BONITA_URL
# Mon, 26 Jul 2021 22:55:18 GMT
ENV BONITA_VERSION=7.10.6
# Mon, 26 Jul 2021 22:55:19 GMT
ENV BONITA_SHA256=aaf61a044e7a8d9ec95d2b5d0c315a6d01d9c93ba01d753fcb008e2cfbbb725f
# Mon, 26 Jul 2021 22:55:19 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 26 Jul 2021 22:55:19 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.10.6/BonitaCommunity-7.10.6.zip
# Mon, 26 Jul 2021 22:55:21 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Mon, 26 Jul 2021 22:55:26 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Mon, 26 Jul 2021 22:55:28 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Mon, 26 Jul 2021 22:55:31 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Mon, 26 Jul 2021 22:55:31 GMT
VOLUME [/opt/bonita]
# Mon, 26 Jul 2021 22:55:32 GMT
COPY dir:46816633cc37ba9fd23af260c8c2384c15f3b4385b5752d6b42577967959f7f0 in /opt/files 
# Mon, 26 Jul 2021 22:55:32 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Mon, 26 Jul 2021 22:55:33 GMT
EXPOSE 8080
# Mon, 26 Jul 2021 22:55:33 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:feac5306138255e28a9862d3f3d29025d0a4d0648855afe1acd6131af07138ac`  
		Last Modified: Mon, 26 Jul 2021 21:22:52 GMT  
		Size: 26.7 MB (26709039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2ff35a682b5aab2f1833cfe9338d2f1645e92b8b58e6f7bd22ec6698dcf1f2`  
		Last Modified: Mon, 26 Jul 2021 22:57:53 GMT  
		Size: 117.1 MB (117061778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84f5909808e2c4b62d70841dc844b47f71efa83b8bef60f1a24b2d74b2a6c67`  
		Last Modified: Mon, 26 Jul 2021 22:57:33 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce766ab4989dc161342b781f894b1dd679c9ffb46b63dda2f8b179cbdd66d1fa`  
		Last Modified: Mon, 26 Jul 2021 22:57:31 GMT  
		Size: 1.9 KB (1911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d84a5be9ab9155852f8850f6ca351278d05f03262d24b1a685b68d32bfe27b7`  
		Last Modified: Mon, 26 Jul 2021 22:57:31 GMT  
		Size: 576.9 KB (576939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d3f521bc9064d4650d56f6440a5ab56c7b0770a1a93924e474fb0b36297409`  
		Last Modified: Mon, 26 Jul 2021 22:57:36 GMT  
		Size: 98.0 MB (97973942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ae44adc9d2679418c010ab9244525f0e73cdbce76c925dfe68f15ee63ed41c`  
		Last Modified: Mon, 26 Jul 2021 22:57:31 GMT  
		Size: 7.7 KB (7651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d71d7f219eec652eeb9d030d33b6984212dd13ae109d720ffaf61170a352d1e8`  
		Last Modified: Mon, 26 Jul 2021 22:57:31 GMT  
		Size: 1.7 KB (1653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.10` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:db36ecba4b322a9461a743f2c12643cde8c8255d8857ac4fd92c5cca208d4fd6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (231036115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a7d7fe59da110fd1017e66aa5fe23f91d1b14cabed9b20195082baca9ab9be`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:49 GMT
ADD file:e87e065765ef99e8db25307f469c7481ab480ac5fe6353ae4caf402766f14045 in / 
# Mon, 26 Jul 2021 21:48:50 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:46:13 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Mon, 26 Jul 2021 22:46:42 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:46:43 GMT
RUN mkdir /opt/custom-init.d/
# Mon, 26 Jul 2021 22:46:44 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Mon, 26 Jul 2021 22:46:46 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Mon, 26 Jul 2021 22:46:47 GMT
ARG BONITA_VERSION
# Mon, 26 Jul 2021 22:46:47 GMT
ARG BONITA_SHA256
# Mon, 26 Jul 2021 22:46:47 GMT
ARG BASE_URL
# Mon, 26 Jul 2021 22:46:47 GMT
ARG BONITA_URL
# Mon, 26 Jul 2021 22:46:47 GMT
ENV BONITA_VERSION=7.10.6
# Mon, 26 Jul 2021 22:46:48 GMT
ENV BONITA_SHA256=aaf61a044e7a8d9ec95d2b5d0c315a6d01d9c93ba01d753fcb008e2cfbbb725f
# Mon, 26 Jul 2021 22:46:48 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 26 Jul 2021 22:46:48 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.10.6/BonitaCommunity-7.10.6.zip
# Mon, 26 Jul 2021 22:46:49 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Mon, 26 Jul 2021 22:46:52 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Mon, 26 Jul 2021 22:46:53 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Mon, 26 Jul 2021 22:46:54 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Mon, 26 Jul 2021 22:46:55 GMT
VOLUME [/opt/bonita]
# Mon, 26 Jul 2021 22:46:55 GMT
COPY dir:46816633cc37ba9fd23af260c8c2384c15f3b4385b5752d6b42577967959f7f0 in /opt/files 
# Mon, 26 Jul 2021 22:46:55 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Mon, 26 Jul 2021 22:46:55 GMT
EXPOSE 8080
# Mon, 26 Jul 2021 22:46:55 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:fda1cca7a3cc2b66c161597f27e151a9b1cab79d73c7c0c2706606813a3e58cf`  
		Last Modified: Mon, 26 Jul 2021 21:50:37 GMT  
		Size: 23.7 MB (23731597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084547179427f3987e0c5e00994444644fca6aa50be01046504c401d9c3de151`  
		Last Modified: Mon, 26 Jul 2021 22:48:52 GMT  
		Size: 108.8 MB (108774220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9ffb1948cec0ddad1716e2690e2c6aff0b747f20c3d145e1247360da291c6b`  
		Last Modified: Mon, 26 Jul 2021 22:48:36 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140bf1aa1582e43154f47f6fc9ce67ac7026cf4b333dc8bb818fa92d4418dd22`  
		Last Modified: Mon, 26 Jul 2021 22:48:34 GMT  
		Size: 1.9 KB (1911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5a83915a885a6058f42811e56bb1992589f1f4a8b23b2540a7cdf256e53a07`  
		Last Modified: Mon, 26 Jul 2021 22:48:34 GMT  
		Size: 545.0 KB (544987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4359ceb1b1b73a2383db954a7bc0122e5f3d8f2e9a2275d10e6ef34930fc421`  
		Last Modified: Mon, 26 Jul 2021 22:48:40 GMT  
		Size: 98.0 MB (97973946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa71dc46c7003bcc657af068ee6cbf80da0295b72e3b5b988411de8a83c03f3d`  
		Last Modified: Mon, 26 Jul 2021 22:48:34 GMT  
		Size: 7.7 KB (7650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9de8548507afb50a0cab1af79a703f283f06ecc15b599d0ecd0a0d9965e873`  
		Last Modified: Mon, 26 Jul 2021 22:48:33 GMT  
		Size: 1.6 KB (1650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.10` - linux; ppc64le

```console
$ docker pull bonita@sha256:20332bc4ee4a8a974c2b32ad4745dfdc968508cea96a30d3db2aa20e3baea6de
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240271367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77234d27352ad11f8224312ff3ad45419019199c47f3f7ba19de7eb6f4f96f2b`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 13 Jul 2021 23:21:55 GMT
ADD file:45b627081344651e16f78f7bbb0da81c1dcc0300835ab0f4bdd6dd93621e461d in / 
# Tue, 13 Jul 2021 23:22:00 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 04:08:13 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Wed, 14 Jul 2021 04:19:12 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:19:28 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 14 Jul 2021 04:19:54 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 14 Jul 2021 04:20:13 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 14 Jul 2021 04:20:22 GMT
ARG BONITA_VERSION
# Wed, 14 Jul 2021 04:20:40 GMT
ARG BONITA_SHA256
# Wed, 14 Jul 2021 04:20:49 GMT
ARG BASE_URL
# Wed, 14 Jul 2021 04:20:55 GMT
ARG BONITA_URL
# Wed, 14 Jul 2021 04:21:00 GMT
ENV BONITA_VERSION=7.10.6
# Wed, 14 Jul 2021 04:21:03 GMT
ENV BONITA_SHA256=aaf61a044e7a8d9ec95d2b5d0c315a6d01d9c93ba01d753fcb008e2cfbbb725f
# Wed, 14 Jul 2021 04:21:09 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 14 Jul 2021 04:21:15 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.10.6/BonitaCommunity-7.10.6.zip
# Wed, 14 Jul 2021 04:21:31 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Wed, 14 Jul 2021 04:21:52 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Wed, 14 Jul 2021 04:22:06 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Wed, 14 Jul 2021 04:22:24 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Wed, 14 Jul 2021 04:22:29 GMT
VOLUME [/opt/bonita]
# Wed, 14 Jul 2021 04:22:32 GMT
COPY dir:46816633cc37ba9fd23af260c8c2384c15f3b4385b5752d6b42577967959f7f0 in /opt/files 
# Wed, 14 Jul 2021 04:22:37 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Wed, 14 Jul 2021 04:22:43 GMT
EXPOSE 8080
# Wed, 14 Jul 2021 04:22:55 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:b4e702a7ed6378fce702bcf7ca7d37185cd6d8387370cd090b9dc4bf5844f47c`  
		Last Modified: Tue, 13 Jul 2021 23:27:12 GMT  
		Size: 30.4 MB (30427987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2553da853866173ce9729df14e099165262b630df5f2072bbdb6947ac4f95b80`  
		Last Modified: Wed, 14 Jul 2021 04:36:23 GMT  
		Size: 111.3 MB (111311300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788967d9c19b9b7dd0c8ee83597d3b05172d86a419ca589a8e8368b2ac77cb7b`  
		Last Modified: Wed, 14 Jul 2021 04:36:02 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437884138b6c53d6a43c99e8dd16a8d76b4eb153676b68d3f2d69ba95439a902`  
		Last Modified: Wed, 14 Jul 2021 04:35:58 GMT  
		Size: 1.9 KB (1919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5463917c53c3914b5f613e2a27ff62925e7995c8812a6c0a064547b9e691a49`  
		Last Modified: Wed, 14 Jul 2021 04:35:58 GMT  
		Size: 546.7 KB (546735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbdeaae0326f56e4805363bcdfa6732a6c89fa953e841597e0da8c2f6d7b979`  
		Last Modified: Wed, 14 Jul 2021 04:36:06 GMT  
		Size: 98.0 MB (97973963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1217386105f4000a8a625d18b342c35a333d072132b16f6cdb7699bc43ffa4a2`  
		Last Modified: Wed, 14 Jul 2021 04:35:58 GMT  
		Size: 7.7 KB (7653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21eb31509ac553404bedddbf106a2136791cbea246c5c78309c40033273795c8`  
		Last Modified: Wed, 14 Jul 2021 04:35:58 GMT  
		Size: 1.7 KB (1654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.10.6`

```console
$ docker pull bonita@sha256:e1d57a765b5dfc4643849c8336c3e6678f7aeda3d8a7c005fdd5f6a461a6ca4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.10.6` - linux; amd64

```console
$ docker pull bonita@sha256:19110484206360b38152356f2a8869beaa404d141f296d4b90b07620520a4e48
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242333069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf6fe8558cb5bbce5446bcbdd31137f8b97984e5e201773b99b20fd9f6565c54`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:30 GMT
ADD file:e729fb032bd2f7cde20fb343da0cd358447e8b23028422c123944e8d0be660fa in / 
# Mon, 26 Jul 2021 21:21:31 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:53:40 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Mon, 26 Jul 2021 22:55:10 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:55:12 GMT
RUN mkdir /opt/custom-init.d/
# Mon, 26 Jul 2021 22:55:13 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Mon, 26 Jul 2021 22:55:17 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Mon, 26 Jul 2021 22:55:17 GMT
ARG BONITA_VERSION
# Mon, 26 Jul 2021 22:55:18 GMT
ARG BONITA_SHA256
# Mon, 26 Jul 2021 22:55:18 GMT
ARG BASE_URL
# Mon, 26 Jul 2021 22:55:18 GMT
ARG BONITA_URL
# Mon, 26 Jul 2021 22:55:18 GMT
ENV BONITA_VERSION=7.10.6
# Mon, 26 Jul 2021 22:55:19 GMT
ENV BONITA_SHA256=aaf61a044e7a8d9ec95d2b5d0c315a6d01d9c93ba01d753fcb008e2cfbbb725f
# Mon, 26 Jul 2021 22:55:19 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 26 Jul 2021 22:55:19 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.10.6/BonitaCommunity-7.10.6.zip
# Mon, 26 Jul 2021 22:55:21 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Mon, 26 Jul 2021 22:55:26 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Mon, 26 Jul 2021 22:55:28 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Mon, 26 Jul 2021 22:55:31 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Mon, 26 Jul 2021 22:55:31 GMT
VOLUME [/opt/bonita]
# Mon, 26 Jul 2021 22:55:32 GMT
COPY dir:46816633cc37ba9fd23af260c8c2384c15f3b4385b5752d6b42577967959f7f0 in /opt/files 
# Mon, 26 Jul 2021 22:55:32 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Mon, 26 Jul 2021 22:55:33 GMT
EXPOSE 8080
# Mon, 26 Jul 2021 22:55:33 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:feac5306138255e28a9862d3f3d29025d0a4d0648855afe1acd6131af07138ac`  
		Last Modified: Mon, 26 Jul 2021 21:22:52 GMT  
		Size: 26.7 MB (26709039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2ff35a682b5aab2f1833cfe9338d2f1645e92b8b58e6f7bd22ec6698dcf1f2`  
		Last Modified: Mon, 26 Jul 2021 22:57:53 GMT  
		Size: 117.1 MB (117061778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84f5909808e2c4b62d70841dc844b47f71efa83b8bef60f1a24b2d74b2a6c67`  
		Last Modified: Mon, 26 Jul 2021 22:57:33 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce766ab4989dc161342b781f894b1dd679c9ffb46b63dda2f8b179cbdd66d1fa`  
		Last Modified: Mon, 26 Jul 2021 22:57:31 GMT  
		Size: 1.9 KB (1911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d84a5be9ab9155852f8850f6ca351278d05f03262d24b1a685b68d32bfe27b7`  
		Last Modified: Mon, 26 Jul 2021 22:57:31 GMT  
		Size: 576.9 KB (576939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d3f521bc9064d4650d56f6440a5ab56c7b0770a1a93924e474fb0b36297409`  
		Last Modified: Mon, 26 Jul 2021 22:57:36 GMT  
		Size: 98.0 MB (97973942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ae44adc9d2679418c010ab9244525f0e73cdbce76c925dfe68f15ee63ed41c`  
		Last Modified: Mon, 26 Jul 2021 22:57:31 GMT  
		Size: 7.7 KB (7651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d71d7f219eec652eeb9d030d33b6984212dd13ae109d720ffaf61170a352d1e8`  
		Last Modified: Mon, 26 Jul 2021 22:57:31 GMT  
		Size: 1.7 KB (1653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.10.6` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:db36ecba4b322a9461a743f2c12643cde8c8255d8857ac4fd92c5cca208d4fd6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (231036115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a7d7fe59da110fd1017e66aa5fe23f91d1b14cabed9b20195082baca9ab9be`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:49 GMT
ADD file:e87e065765ef99e8db25307f469c7481ab480ac5fe6353ae4caf402766f14045 in / 
# Mon, 26 Jul 2021 21:48:50 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:46:13 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Mon, 26 Jul 2021 22:46:42 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:46:43 GMT
RUN mkdir /opt/custom-init.d/
# Mon, 26 Jul 2021 22:46:44 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Mon, 26 Jul 2021 22:46:46 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Mon, 26 Jul 2021 22:46:47 GMT
ARG BONITA_VERSION
# Mon, 26 Jul 2021 22:46:47 GMT
ARG BONITA_SHA256
# Mon, 26 Jul 2021 22:46:47 GMT
ARG BASE_URL
# Mon, 26 Jul 2021 22:46:47 GMT
ARG BONITA_URL
# Mon, 26 Jul 2021 22:46:47 GMT
ENV BONITA_VERSION=7.10.6
# Mon, 26 Jul 2021 22:46:48 GMT
ENV BONITA_SHA256=aaf61a044e7a8d9ec95d2b5d0c315a6d01d9c93ba01d753fcb008e2cfbbb725f
# Mon, 26 Jul 2021 22:46:48 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 26 Jul 2021 22:46:48 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.10.6/BonitaCommunity-7.10.6.zip
# Mon, 26 Jul 2021 22:46:49 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Mon, 26 Jul 2021 22:46:52 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Mon, 26 Jul 2021 22:46:53 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Mon, 26 Jul 2021 22:46:54 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Mon, 26 Jul 2021 22:46:55 GMT
VOLUME [/opt/bonita]
# Mon, 26 Jul 2021 22:46:55 GMT
COPY dir:46816633cc37ba9fd23af260c8c2384c15f3b4385b5752d6b42577967959f7f0 in /opt/files 
# Mon, 26 Jul 2021 22:46:55 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Mon, 26 Jul 2021 22:46:55 GMT
EXPOSE 8080
# Mon, 26 Jul 2021 22:46:55 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:fda1cca7a3cc2b66c161597f27e151a9b1cab79d73c7c0c2706606813a3e58cf`  
		Last Modified: Mon, 26 Jul 2021 21:50:37 GMT  
		Size: 23.7 MB (23731597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084547179427f3987e0c5e00994444644fca6aa50be01046504c401d9c3de151`  
		Last Modified: Mon, 26 Jul 2021 22:48:52 GMT  
		Size: 108.8 MB (108774220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9ffb1948cec0ddad1716e2690e2c6aff0b747f20c3d145e1247360da291c6b`  
		Last Modified: Mon, 26 Jul 2021 22:48:36 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140bf1aa1582e43154f47f6fc9ce67ac7026cf4b333dc8bb818fa92d4418dd22`  
		Last Modified: Mon, 26 Jul 2021 22:48:34 GMT  
		Size: 1.9 KB (1911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5a83915a885a6058f42811e56bb1992589f1f4a8b23b2540a7cdf256e53a07`  
		Last Modified: Mon, 26 Jul 2021 22:48:34 GMT  
		Size: 545.0 KB (544987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4359ceb1b1b73a2383db954a7bc0122e5f3d8f2e9a2275d10e6ef34930fc421`  
		Last Modified: Mon, 26 Jul 2021 22:48:40 GMT  
		Size: 98.0 MB (97973946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa71dc46c7003bcc657af068ee6cbf80da0295b72e3b5b988411de8a83c03f3d`  
		Last Modified: Mon, 26 Jul 2021 22:48:34 GMT  
		Size: 7.7 KB (7650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9de8548507afb50a0cab1af79a703f283f06ecc15b599d0ecd0a0d9965e873`  
		Last Modified: Mon, 26 Jul 2021 22:48:33 GMT  
		Size: 1.6 KB (1650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.10.6` - linux; ppc64le

```console
$ docker pull bonita@sha256:20332bc4ee4a8a974c2b32ad4745dfdc968508cea96a30d3db2aa20e3baea6de
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240271367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77234d27352ad11f8224312ff3ad45419019199c47f3f7ba19de7eb6f4f96f2b`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 13 Jul 2021 23:21:55 GMT
ADD file:45b627081344651e16f78f7bbb0da81c1dcc0300835ab0f4bdd6dd93621e461d in / 
# Tue, 13 Jul 2021 23:22:00 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 04:08:13 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Wed, 14 Jul 2021 04:19:12 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:19:28 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 14 Jul 2021 04:19:54 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 14 Jul 2021 04:20:13 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 14 Jul 2021 04:20:22 GMT
ARG BONITA_VERSION
# Wed, 14 Jul 2021 04:20:40 GMT
ARG BONITA_SHA256
# Wed, 14 Jul 2021 04:20:49 GMT
ARG BASE_URL
# Wed, 14 Jul 2021 04:20:55 GMT
ARG BONITA_URL
# Wed, 14 Jul 2021 04:21:00 GMT
ENV BONITA_VERSION=7.10.6
# Wed, 14 Jul 2021 04:21:03 GMT
ENV BONITA_SHA256=aaf61a044e7a8d9ec95d2b5d0c315a6d01d9c93ba01d753fcb008e2cfbbb725f
# Wed, 14 Jul 2021 04:21:09 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 14 Jul 2021 04:21:15 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.10.6/BonitaCommunity-7.10.6.zip
# Wed, 14 Jul 2021 04:21:31 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Wed, 14 Jul 2021 04:21:52 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Wed, 14 Jul 2021 04:22:06 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Wed, 14 Jul 2021 04:22:24 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Wed, 14 Jul 2021 04:22:29 GMT
VOLUME [/opt/bonita]
# Wed, 14 Jul 2021 04:22:32 GMT
COPY dir:46816633cc37ba9fd23af260c8c2384c15f3b4385b5752d6b42577967959f7f0 in /opt/files 
# Wed, 14 Jul 2021 04:22:37 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Wed, 14 Jul 2021 04:22:43 GMT
EXPOSE 8080
# Wed, 14 Jul 2021 04:22:55 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:b4e702a7ed6378fce702bcf7ca7d37185cd6d8387370cd090b9dc4bf5844f47c`  
		Last Modified: Tue, 13 Jul 2021 23:27:12 GMT  
		Size: 30.4 MB (30427987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2553da853866173ce9729df14e099165262b630df5f2072bbdb6947ac4f95b80`  
		Last Modified: Wed, 14 Jul 2021 04:36:23 GMT  
		Size: 111.3 MB (111311300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788967d9c19b9b7dd0c8ee83597d3b05172d86a419ca589a8e8368b2ac77cb7b`  
		Last Modified: Wed, 14 Jul 2021 04:36:02 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437884138b6c53d6a43c99e8dd16a8d76b4eb153676b68d3f2d69ba95439a902`  
		Last Modified: Wed, 14 Jul 2021 04:35:58 GMT  
		Size: 1.9 KB (1919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5463917c53c3914b5f613e2a27ff62925e7995c8812a6c0a064547b9e691a49`  
		Last Modified: Wed, 14 Jul 2021 04:35:58 GMT  
		Size: 546.7 KB (546735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbdeaae0326f56e4805363bcdfa6732a6c89fa953e841597e0da8c2f6d7b979`  
		Last Modified: Wed, 14 Jul 2021 04:36:06 GMT  
		Size: 98.0 MB (97973963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1217386105f4000a8a625d18b342c35a333d072132b16f6cdb7699bc43ffa4a2`  
		Last Modified: Wed, 14 Jul 2021 04:35:58 GMT  
		Size: 7.7 KB (7653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21eb31509ac553404bedddbf106a2136791cbea246c5c78309c40033273795c8`  
		Last Modified: Wed, 14 Jul 2021 04:35:58 GMT  
		Size: 1.7 KB (1654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.11`

```console
$ docker pull bonita@sha256:1667e52fe4de2e4bd779dae37f4fc753731c3d8f9e6ababbaafd8859444d5fbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.11` - linux; amd64

```console
$ docker pull bonita@sha256:6e1c0d8516dcff0b729a41f0e33940ee24ea903a731edc7c5e2dfe01a295b8cd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234163801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe0c59eaf4dad2da11b9059ada3fd3358442951e820eb93fefafee346117fae`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:30 GMT
ADD file:e729fb032bd2f7cde20fb343da0cd358447e8b23028422c123944e8d0be660fa in / 
# Mon, 26 Jul 2021 21:21:31 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:55:51 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 26 Jul 2021 22:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:56:38 GMT
RUN mkdir /opt/custom-init.d/
# Mon, 26 Jul 2021 22:56:40 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Mon, 26 Jul 2021 22:56:43 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Mon, 26 Jul 2021 22:56:43 GMT
ARG BONITA_VERSION
# Mon, 26 Jul 2021 22:56:43 GMT
ARG BONITA_SHA256
# Mon, 26 Jul 2021 22:56:44 GMT
ARG BASE_URL
# Mon, 26 Jul 2021 22:56:44 GMT
ARG BONITA_URL
# Mon, 26 Jul 2021 22:56:44 GMT
ENV BONITA_VERSION=7.11.4
# Mon, 26 Jul 2021 22:56:45 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Mon, 26 Jul 2021 22:56:45 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Mon, 26 Jul 2021 22:56:45 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 26 Jul 2021 22:56:45 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Mon, 26 Jul 2021 22:56:47 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Mon, 26 Jul 2021 22:56:48 GMT
RUN mkdir /opt/files
# Mon, 26 Jul 2021 22:56:48 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Mon, 26 Jul 2021 22:56:52 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Mon, 26 Jul 2021 22:56:55 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Mon, 26 Jul 2021 22:56:57 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Mon, 26 Jul 2021 22:56:57 GMT
VOLUME [/opt/bonita]
# Mon, 26 Jul 2021 22:56:57 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Mon, 26 Jul 2021 22:56:58 GMT
EXPOSE 8080
# Mon, 26 Jul 2021 22:56:58 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:feac5306138255e28a9862d3f3d29025d0a4d0648855afe1acd6131af07138ac`  
		Last Modified: Mon, 26 Jul 2021 21:22:52 GMT  
		Size: 26.7 MB (26709039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41fbee9f4b324cc20d8988fa7cab5d9c491c1a9a380342d8846040fa5afe01a`  
		Last Modified: Mon, 26 Jul 2021 22:58:25 GMT  
		Size: 93.5 MB (93519201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ca53056372700c6fbe41da9cb2df900b3b73e9cf784ebadd79e20b3b8080d1`  
		Last Modified: Mon, 26 Jul 2021 22:58:08 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9905bd9bc78f4e660b093c94972b9bfe153be1450b65d1d94a39a66265e9f809`  
		Last Modified: Mon, 26 Jul 2021 22:58:08 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6437ef6648258db0d319ca67287e68abd9d59fd9a13cef685fcf0001eefd77`  
		Last Modified: Mon, 26 Jul 2021 22:58:05 GMT  
		Size: 576.9 KB (576937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b3c478298f17e6e9f4db37ad05b1f59a7703e3dc2531ef60ae6bcf40eb3980`  
		Last Modified: Mon, 26 Jul 2021 22:58:05 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267372339509897e191e9231726b872c73d431dd64d3f611b5651cbca33b7d99`  
		Last Modified: Mon, 26 Jul 2021 22:58:06 GMT  
		Size: 6.9 KB (6895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9ea6d36359e73c26d555fbe289c2d77236b012558f9e776595e8ec0824cd062`  
		Last Modified: Mon, 26 Jul 2021 22:58:14 GMT  
		Size: 113.3 MB (113347830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada58b922dd91bb509a951f2851cb01740378cebd84c37b56c7fcd52b17a2d5e`  
		Last Modified: Mon, 26 Jul 2021 22:58:05 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:f510b7bdf7f4882b25b71d2f58b4360272c4249edac135741f1af3d9dd794e3f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.3 MB (223268930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fb6ac38a1a8ac16cc4a73a30a7db42a729fd7b7ee0f879ea911b637434af9c8`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:49 GMT
ADD file:e87e065765ef99e8db25307f469c7481ab480ac5fe6353ae4caf402766f14045 in / 
# Mon, 26 Jul 2021 21:48:50 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:47:04 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 26 Jul 2021 22:47:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:47:27 GMT
RUN mkdir /opt/custom-init.d/
# Mon, 26 Jul 2021 22:47:27 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Mon, 26 Jul 2021 22:47:35 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Mon, 26 Jul 2021 22:47:35 GMT
ARG BONITA_VERSION
# Mon, 26 Jul 2021 22:47:35 GMT
ARG BONITA_SHA256
# Mon, 26 Jul 2021 22:47:35 GMT
ARG BASE_URL
# Mon, 26 Jul 2021 22:47:36 GMT
ARG BONITA_URL
# Mon, 26 Jul 2021 22:47:36 GMT
ENV BONITA_VERSION=7.11.4
# Mon, 26 Jul 2021 22:47:36 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Mon, 26 Jul 2021 22:47:36 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Mon, 26 Jul 2021 22:47:36 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 26 Jul 2021 22:47:37 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Mon, 26 Jul 2021 22:47:37 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Mon, 26 Jul 2021 22:47:38 GMT
RUN mkdir /opt/files
# Mon, 26 Jul 2021 22:47:38 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Mon, 26 Jul 2021 22:47:42 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Mon, 26 Jul 2021 22:47:43 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Mon, 26 Jul 2021 22:47:45 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Mon, 26 Jul 2021 22:47:45 GMT
VOLUME [/opt/bonita]
# Mon, 26 Jul 2021 22:47:45 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Mon, 26 Jul 2021 22:47:45 GMT
EXPOSE 8080
# Mon, 26 Jul 2021 22:47:45 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:fda1cca7a3cc2b66c161597f27e151a9b1cab79d73c7c0c2706606813a3e58cf`  
		Last Modified: Mon, 26 Jul 2021 21:50:37 GMT  
		Size: 23.7 MB (23731597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a32c2e693656a5434b587ae1cfac238a95021569769a39d83ef10e89e26121b`  
		Last Modified: Mon, 26 Jul 2021 22:49:21 GMT  
		Size: 85.6 MB (85631763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad214e302609f03f40484c257c896f8ebd558d57ec6c206420d30d631d5372b`  
		Last Modified: Mon, 26 Jul 2021 22:49:09 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9502bfb487c7c8ec156a40e2377f90db8fc718caf311aeded083744517a000a`  
		Last Modified: Mon, 26 Jul 2021 22:49:09 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73e0be58132932de21617b671fbcca74b337f211536ce134caa69deef3762c3`  
		Last Modified: Mon, 26 Jul 2021 22:49:06 GMT  
		Size: 547.0 KB (546952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21c5dfa333f8f4d4051d5c551de2eb67d4d7a15798c9197e563e39c2382d89a`  
		Last Modified: Mon, 26 Jul 2021 22:49:06 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41400161f7b912e450a9dbe9a7afdcf654243b1ffdd0780021f9e792ba246e1e`  
		Last Modified: Mon, 26 Jul 2021 22:49:06 GMT  
		Size: 6.9 KB (6890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe40c2b70105262f8bafea210d05401def29390ee6b40e838ee8d6475ffb9cf9`  
		Last Modified: Mon, 26 Jul 2021 22:49:13 GMT  
		Size: 113.3 MB (113347828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b44d48c17eb07fb93fb6fecd8f22911ca1625f1708e4429f98f67026117bd8b`  
		Last Modified: Mon, 26 Jul 2021 22:49:06 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11` - linux; ppc64le

```console
$ docker pull bonita@sha256:2958d6a5bde9958b077c93f38afb6c34dc2004592c5d4a8f185a82fc3ca7ab20
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.7 MB (230728713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6462a293d0d2870577a6ef14785e95017141fd3cd1414c8cd1ece04817071118`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 13 Jul 2021 23:21:55 GMT
ADD file:45b627081344651e16f78f7bbb0da81c1dcc0300835ab0f4bdd6dd93621e461d in / 
# Tue, 13 Jul 2021 23:22:00 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 04:23:21 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 14 Jul 2021 04:28:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:28:27 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 14 Jul 2021 04:28:56 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 14 Jul 2021 04:29:11 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 14 Jul 2021 04:29:17 GMT
ARG BONITA_VERSION
# Wed, 14 Jul 2021 04:29:25 GMT
ARG BONITA_SHA256
# Wed, 14 Jul 2021 04:29:32 GMT
ARG BASE_URL
# Wed, 14 Jul 2021 04:29:36 GMT
ARG BONITA_URL
# Wed, 14 Jul 2021 04:29:40 GMT
ENV BONITA_VERSION=7.11.4
# Wed, 14 Jul 2021 04:29:50 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Wed, 14 Jul 2021 04:29:58 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Wed, 14 Jul 2021 04:30:05 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 14 Jul 2021 04:30:17 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Wed, 14 Jul 2021 04:30:32 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Wed, 14 Jul 2021 04:30:51 GMT
RUN mkdir /opt/files
# Wed, 14 Jul 2021 04:30:54 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Wed, 14 Jul 2021 04:31:19 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Wed, 14 Jul 2021 04:31:55 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Wed, 14 Jul 2021 04:32:13 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Wed, 14 Jul 2021 04:32:21 GMT
VOLUME [/opt/bonita]
# Wed, 14 Jul 2021 04:32:24 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 14 Jul 2021 04:32:38 GMT
EXPOSE 8080
# Wed, 14 Jul 2021 04:32:45 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:b4e702a7ed6378fce702bcf7ca7d37185cd6d8387370cd090b9dc4bf5844f47c`  
		Last Modified: Tue, 13 Jul 2021 23:27:12 GMT  
		Size: 30.4 MB (30427987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea6d20994673343d11028ac1ac0bcc098d0f1ac3b04655623d2d2cafa4bee8d`  
		Last Modified: Wed, 14 Jul 2021 04:37:02 GMT  
		Size: 86.4 MB (86395354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7a025e3dd302981f640be07c88365b3ddfa8c7d2a818971b050001fa255123`  
		Last Modified: Wed, 14 Jul 2021 04:36:46 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c867ae2580be2a8356c180288cecbeca16488f530908d5ebb203c0c5bf0a99`  
		Last Modified: Wed, 14 Jul 2021 04:36:44 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7732888c6ddf76b2f60aa2ce9638a1b17b4a33dc96c7a969b6b0a3401b8c8568`  
		Last Modified: Wed, 14 Jul 2021 04:36:41 GMT  
		Size: 546.7 KB (546731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084fe2e4073223b4d7fbdedc2545b34d8174239157725e6c0a24fbd28d9a8d19`  
		Last Modified: Wed, 14 Jul 2021 04:36:41 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3547178d7d78c1496b84942e11d81ef65cfa3b32a5f6c7839a06493e4eecf0d`  
		Last Modified: Wed, 14 Jul 2021 04:36:41 GMT  
		Size: 6.9 KB (6895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6540b82f34eeb6be88b346855d91ef64c48e76e0c63aa603f951375d98c145a`  
		Last Modified: Wed, 14 Jul 2021 04:36:50 GMT  
		Size: 113.3 MB (113347830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159e285cbe267e213a16b7de6a44e260147a70600c5e397e47802a7301768d81`  
		Last Modified: Wed, 14 Jul 2021 04:36:41 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.11.4`

```console
$ docker pull bonita@sha256:1667e52fe4de2e4bd779dae37f4fc753731c3d8f9e6ababbaafd8859444d5fbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.11.4` - linux; amd64

```console
$ docker pull bonita@sha256:6e1c0d8516dcff0b729a41f0e33940ee24ea903a731edc7c5e2dfe01a295b8cd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234163801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe0c59eaf4dad2da11b9059ada3fd3358442951e820eb93fefafee346117fae`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:30 GMT
ADD file:e729fb032bd2f7cde20fb343da0cd358447e8b23028422c123944e8d0be660fa in / 
# Mon, 26 Jul 2021 21:21:31 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:55:51 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 26 Jul 2021 22:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:56:38 GMT
RUN mkdir /opt/custom-init.d/
# Mon, 26 Jul 2021 22:56:40 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Mon, 26 Jul 2021 22:56:43 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Mon, 26 Jul 2021 22:56:43 GMT
ARG BONITA_VERSION
# Mon, 26 Jul 2021 22:56:43 GMT
ARG BONITA_SHA256
# Mon, 26 Jul 2021 22:56:44 GMT
ARG BASE_URL
# Mon, 26 Jul 2021 22:56:44 GMT
ARG BONITA_URL
# Mon, 26 Jul 2021 22:56:44 GMT
ENV BONITA_VERSION=7.11.4
# Mon, 26 Jul 2021 22:56:45 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Mon, 26 Jul 2021 22:56:45 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Mon, 26 Jul 2021 22:56:45 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 26 Jul 2021 22:56:45 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Mon, 26 Jul 2021 22:56:47 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Mon, 26 Jul 2021 22:56:48 GMT
RUN mkdir /opt/files
# Mon, 26 Jul 2021 22:56:48 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Mon, 26 Jul 2021 22:56:52 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Mon, 26 Jul 2021 22:56:55 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Mon, 26 Jul 2021 22:56:57 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Mon, 26 Jul 2021 22:56:57 GMT
VOLUME [/opt/bonita]
# Mon, 26 Jul 2021 22:56:57 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Mon, 26 Jul 2021 22:56:58 GMT
EXPOSE 8080
# Mon, 26 Jul 2021 22:56:58 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:feac5306138255e28a9862d3f3d29025d0a4d0648855afe1acd6131af07138ac`  
		Last Modified: Mon, 26 Jul 2021 21:22:52 GMT  
		Size: 26.7 MB (26709039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41fbee9f4b324cc20d8988fa7cab5d9c491c1a9a380342d8846040fa5afe01a`  
		Last Modified: Mon, 26 Jul 2021 22:58:25 GMT  
		Size: 93.5 MB (93519201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ca53056372700c6fbe41da9cb2df900b3b73e9cf784ebadd79e20b3b8080d1`  
		Last Modified: Mon, 26 Jul 2021 22:58:08 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9905bd9bc78f4e660b093c94972b9bfe153be1450b65d1d94a39a66265e9f809`  
		Last Modified: Mon, 26 Jul 2021 22:58:08 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6437ef6648258db0d319ca67287e68abd9d59fd9a13cef685fcf0001eefd77`  
		Last Modified: Mon, 26 Jul 2021 22:58:05 GMT  
		Size: 576.9 KB (576937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b3c478298f17e6e9f4db37ad05b1f59a7703e3dc2531ef60ae6bcf40eb3980`  
		Last Modified: Mon, 26 Jul 2021 22:58:05 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267372339509897e191e9231726b872c73d431dd64d3f611b5651cbca33b7d99`  
		Last Modified: Mon, 26 Jul 2021 22:58:06 GMT  
		Size: 6.9 KB (6895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9ea6d36359e73c26d555fbe289c2d77236b012558f9e776595e8ec0824cd062`  
		Last Modified: Mon, 26 Jul 2021 22:58:14 GMT  
		Size: 113.3 MB (113347830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada58b922dd91bb509a951f2851cb01740378cebd84c37b56c7fcd52b17a2d5e`  
		Last Modified: Mon, 26 Jul 2021 22:58:05 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11.4` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:f510b7bdf7f4882b25b71d2f58b4360272c4249edac135741f1af3d9dd794e3f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.3 MB (223268930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fb6ac38a1a8ac16cc4a73a30a7db42a729fd7b7ee0f879ea911b637434af9c8`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:49 GMT
ADD file:e87e065765ef99e8db25307f469c7481ab480ac5fe6353ae4caf402766f14045 in / 
# Mon, 26 Jul 2021 21:48:50 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:47:04 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 26 Jul 2021 22:47:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:47:27 GMT
RUN mkdir /opt/custom-init.d/
# Mon, 26 Jul 2021 22:47:27 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Mon, 26 Jul 2021 22:47:35 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Mon, 26 Jul 2021 22:47:35 GMT
ARG BONITA_VERSION
# Mon, 26 Jul 2021 22:47:35 GMT
ARG BONITA_SHA256
# Mon, 26 Jul 2021 22:47:35 GMT
ARG BASE_URL
# Mon, 26 Jul 2021 22:47:36 GMT
ARG BONITA_URL
# Mon, 26 Jul 2021 22:47:36 GMT
ENV BONITA_VERSION=7.11.4
# Mon, 26 Jul 2021 22:47:36 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Mon, 26 Jul 2021 22:47:36 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Mon, 26 Jul 2021 22:47:36 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 26 Jul 2021 22:47:37 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Mon, 26 Jul 2021 22:47:37 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Mon, 26 Jul 2021 22:47:38 GMT
RUN mkdir /opt/files
# Mon, 26 Jul 2021 22:47:38 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Mon, 26 Jul 2021 22:47:42 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Mon, 26 Jul 2021 22:47:43 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Mon, 26 Jul 2021 22:47:45 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Mon, 26 Jul 2021 22:47:45 GMT
VOLUME [/opt/bonita]
# Mon, 26 Jul 2021 22:47:45 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Mon, 26 Jul 2021 22:47:45 GMT
EXPOSE 8080
# Mon, 26 Jul 2021 22:47:45 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:fda1cca7a3cc2b66c161597f27e151a9b1cab79d73c7c0c2706606813a3e58cf`  
		Last Modified: Mon, 26 Jul 2021 21:50:37 GMT  
		Size: 23.7 MB (23731597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a32c2e693656a5434b587ae1cfac238a95021569769a39d83ef10e89e26121b`  
		Last Modified: Mon, 26 Jul 2021 22:49:21 GMT  
		Size: 85.6 MB (85631763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad214e302609f03f40484c257c896f8ebd558d57ec6c206420d30d631d5372b`  
		Last Modified: Mon, 26 Jul 2021 22:49:09 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9502bfb487c7c8ec156a40e2377f90db8fc718caf311aeded083744517a000a`  
		Last Modified: Mon, 26 Jul 2021 22:49:09 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73e0be58132932de21617b671fbcca74b337f211536ce134caa69deef3762c3`  
		Last Modified: Mon, 26 Jul 2021 22:49:06 GMT  
		Size: 547.0 KB (546952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21c5dfa333f8f4d4051d5c551de2eb67d4d7a15798c9197e563e39c2382d89a`  
		Last Modified: Mon, 26 Jul 2021 22:49:06 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41400161f7b912e450a9dbe9a7afdcf654243b1ffdd0780021f9e792ba246e1e`  
		Last Modified: Mon, 26 Jul 2021 22:49:06 GMT  
		Size: 6.9 KB (6890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe40c2b70105262f8bafea210d05401def29390ee6b40e838ee8d6475ffb9cf9`  
		Last Modified: Mon, 26 Jul 2021 22:49:13 GMT  
		Size: 113.3 MB (113347828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b44d48c17eb07fb93fb6fecd8f22911ca1625f1708e4429f98f67026117bd8b`  
		Last Modified: Mon, 26 Jul 2021 22:49:06 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11.4` - linux; ppc64le

```console
$ docker pull bonita@sha256:2958d6a5bde9958b077c93f38afb6c34dc2004592c5d4a8f185a82fc3ca7ab20
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.7 MB (230728713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6462a293d0d2870577a6ef14785e95017141fd3cd1414c8cd1ece04817071118`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 13 Jul 2021 23:21:55 GMT
ADD file:45b627081344651e16f78f7bbb0da81c1dcc0300835ab0f4bdd6dd93621e461d in / 
# Tue, 13 Jul 2021 23:22:00 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 04:23:21 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 14 Jul 2021 04:28:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:28:27 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 14 Jul 2021 04:28:56 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 14 Jul 2021 04:29:11 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 14 Jul 2021 04:29:17 GMT
ARG BONITA_VERSION
# Wed, 14 Jul 2021 04:29:25 GMT
ARG BONITA_SHA256
# Wed, 14 Jul 2021 04:29:32 GMT
ARG BASE_URL
# Wed, 14 Jul 2021 04:29:36 GMT
ARG BONITA_URL
# Wed, 14 Jul 2021 04:29:40 GMT
ENV BONITA_VERSION=7.11.4
# Wed, 14 Jul 2021 04:29:50 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Wed, 14 Jul 2021 04:29:58 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Wed, 14 Jul 2021 04:30:05 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 14 Jul 2021 04:30:17 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Wed, 14 Jul 2021 04:30:32 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Wed, 14 Jul 2021 04:30:51 GMT
RUN mkdir /opt/files
# Wed, 14 Jul 2021 04:30:54 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Wed, 14 Jul 2021 04:31:19 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Wed, 14 Jul 2021 04:31:55 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Wed, 14 Jul 2021 04:32:13 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Wed, 14 Jul 2021 04:32:21 GMT
VOLUME [/opt/bonita]
# Wed, 14 Jul 2021 04:32:24 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 14 Jul 2021 04:32:38 GMT
EXPOSE 8080
# Wed, 14 Jul 2021 04:32:45 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:b4e702a7ed6378fce702bcf7ca7d37185cd6d8387370cd090b9dc4bf5844f47c`  
		Last Modified: Tue, 13 Jul 2021 23:27:12 GMT  
		Size: 30.4 MB (30427987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea6d20994673343d11028ac1ac0bcc098d0f1ac3b04655623d2d2cafa4bee8d`  
		Last Modified: Wed, 14 Jul 2021 04:37:02 GMT  
		Size: 86.4 MB (86395354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7a025e3dd302981f640be07c88365b3ddfa8c7d2a818971b050001fa255123`  
		Last Modified: Wed, 14 Jul 2021 04:36:46 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c867ae2580be2a8356c180288cecbeca16488f530908d5ebb203c0c5bf0a99`  
		Last Modified: Wed, 14 Jul 2021 04:36:44 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7732888c6ddf76b2f60aa2ce9638a1b17b4a33dc96c7a969b6b0a3401b8c8568`  
		Last Modified: Wed, 14 Jul 2021 04:36:41 GMT  
		Size: 546.7 KB (546731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084fe2e4073223b4d7fbdedc2545b34d8174239157725e6c0a24fbd28d9a8d19`  
		Last Modified: Wed, 14 Jul 2021 04:36:41 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3547178d7d78c1496b84942e11d81ef65cfa3b32a5f6c7839a06493e4eecf0d`  
		Last Modified: Wed, 14 Jul 2021 04:36:41 GMT  
		Size: 6.9 KB (6895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6540b82f34eeb6be88b346855d91ef64c48e76e0c63aa603f951375d98c145a`  
		Last Modified: Wed, 14 Jul 2021 04:36:50 GMT  
		Size: 113.3 MB (113347830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159e285cbe267e213a16b7de6a44e260147a70600c5e397e47802a7301768d81`  
		Last Modified: Wed, 14 Jul 2021 04:36:41 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.12`

```console
$ docker pull bonita@sha256:32cfa6689575e7983e6a17f1afc8b096aa12369d64b17e357769b45c4d83dc74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.12` - linux; amd64

```console
$ docker pull bonita@sha256:b5916584fa8b0223d4f5110fb38f5c7e1d50507c9c06ae7517ff791be50ac988
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237231421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92810c0e9ab24901233e4e22bb664a65b8406726965dddc531f2f5962ac3d59a`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:30 GMT
ADD file:e729fb032bd2f7cde20fb343da0cd358447e8b23028422c123944e8d0be660fa in / 
# Mon, 26 Jul 2021 21:21:31 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:55:51 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 26 Jul 2021 22:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:56:38 GMT
RUN mkdir /opt/custom-init.d/
# Mon, 26 Jul 2021 22:56:40 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Mon, 26 Jul 2021 22:56:43 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Mon, 26 Jul 2021 22:56:43 GMT
ARG BONITA_VERSION
# Mon, 26 Jul 2021 22:57:03 GMT
ARG BRANDING_VERSION
# Mon, 26 Jul 2021 22:57:03 GMT
ARG BONITA_SHA256
# Mon, 26 Jul 2021 22:57:03 GMT
ARG BASE_URL
# Mon, 26 Jul 2021 22:57:03 GMT
ARG BONITA_URL
# Mon, 26 Jul 2021 22:57:03 GMT
ENV BONITA_VERSION=7.12.1
# Mon, 26 Jul 2021 22:57:04 GMT
ENV BRANDING_VERSION=2021.1
# Mon, 26 Jul 2021 22:57:04 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Mon, 26 Jul 2021 22:57:04 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Mon, 26 Jul 2021 22:57:04 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 26 Jul 2021 22:57:05 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Mon, 26 Jul 2021 22:57:05 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Mon, 26 Jul 2021 22:57:06 GMT
RUN mkdir /opt/files
# Mon, 26 Jul 2021 22:57:06 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Mon, 26 Jul 2021 22:57:10 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Mon, 26 Jul 2021 22:57:12 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Mon, 26 Jul 2021 22:57:13 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Mon, 26 Jul 2021 22:57:14 GMT
VOLUME [/opt/bonita]
# Mon, 26 Jul 2021 22:57:14 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Mon, 26 Jul 2021 22:57:14 GMT
EXPOSE 8080
# Mon, 26 Jul 2021 22:57:14 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:feac5306138255e28a9862d3f3d29025d0a4d0648855afe1acd6131af07138ac`  
		Last Modified: Mon, 26 Jul 2021 21:22:52 GMT  
		Size: 26.7 MB (26709039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41fbee9f4b324cc20d8988fa7cab5d9c491c1a9a380342d8846040fa5afe01a`  
		Last Modified: Mon, 26 Jul 2021 22:58:25 GMT  
		Size: 93.5 MB (93519201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ca53056372700c6fbe41da9cb2df900b3b73e9cf784ebadd79e20b3b8080d1`  
		Last Modified: Mon, 26 Jul 2021 22:58:08 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9905bd9bc78f4e660b093c94972b9bfe153be1450b65d1d94a39a66265e9f809`  
		Last Modified: Mon, 26 Jul 2021 22:58:08 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6437ef6648258db0d319ca67287e68abd9d59fd9a13cef685fcf0001eefd77`  
		Last Modified: Mon, 26 Jul 2021 22:58:05 GMT  
		Size: 576.9 KB (576937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6eb19591747c3e652808ab538441ba4b47dc4e60835c762225b47c427ec90aa`  
		Last Modified: Mon, 26 Jul 2021 22:58:38 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb19116d4d9d99e7693af7fd0f393d5a6b46eb766cacef6db42839311df87df`  
		Last Modified: Mon, 26 Jul 2021 22:58:38 GMT  
		Size: 6.9 KB (6942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee45552874f5dc095ab9338e4c91bb15548e9e55d077e57a156c058c4f5b45e`  
		Last Modified: Mon, 26 Jul 2021 22:58:46 GMT  
		Size: 116.4 MB (116415405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e8604ffcc7b25e1d701643f189b9df43053595d0435c1406ab10d73233c0e0`  
		Last Modified: Mon, 26 Jul 2021 22:58:38 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:6fef41ea5e1c154704edff635aa96d95e0f51631f6d0b337dd0502d3028e8953
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226336563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abfa77e4bfcd83636fefc618a3f25a8bec1e977a73c1393b20e51974930f5ecd`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:49 GMT
ADD file:e87e065765ef99e8db25307f469c7481ab480ac5fe6353ae4caf402766f14045 in / 
# Mon, 26 Jul 2021 21:48:50 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:47:04 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 26 Jul 2021 22:47:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:47:27 GMT
RUN mkdir /opt/custom-init.d/
# Mon, 26 Jul 2021 22:47:27 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Mon, 26 Jul 2021 22:47:35 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Mon, 26 Jul 2021 22:47:35 GMT
ARG BONITA_VERSION
# Mon, 26 Jul 2021 22:47:56 GMT
ARG BRANDING_VERSION
# Mon, 26 Jul 2021 22:47:56 GMT
ARG BONITA_SHA256
# Mon, 26 Jul 2021 22:47:56 GMT
ARG BASE_URL
# Mon, 26 Jul 2021 22:47:57 GMT
ARG BONITA_URL
# Mon, 26 Jul 2021 22:47:57 GMT
ENV BONITA_VERSION=7.12.1
# Mon, 26 Jul 2021 22:47:57 GMT
ENV BRANDING_VERSION=2021.1
# Mon, 26 Jul 2021 22:47:57 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Mon, 26 Jul 2021 22:47:57 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Mon, 26 Jul 2021 22:47:57 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 26 Jul 2021 22:47:58 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Mon, 26 Jul 2021 22:47:58 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Mon, 26 Jul 2021 22:47:59 GMT
RUN mkdir /opt/files
# Mon, 26 Jul 2021 22:47:59 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Mon, 26 Jul 2021 22:48:03 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Mon, 26 Jul 2021 22:48:04 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Mon, 26 Jul 2021 22:48:06 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Mon, 26 Jul 2021 22:48:06 GMT
VOLUME [/opt/bonita]
# Mon, 26 Jul 2021 22:48:06 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Mon, 26 Jul 2021 22:48:06 GMT
EXPOSE 8080
# Mon, 26 Jul 2021 22:48:06 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:fda1cca7a3cc2b66c161597f27e151a9b1cab79d73c7c0c2706606813a3e58cf`  
		Last Modified: Mon, 26 Jul 2021 21:50:37 GMT  
		Size: 23.7 MB (23731597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a32c2e693656a5434b587ae1cfac238a95021569769a39d83ef10e89e26121b`  
		Last Modified: Mon, 26 Jul 2021 22:49:21 GMT  
		Size: 85.6 MB (85631763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad214e302609f03f40484c257c896f8ebd558d57ec6c206420d30d631d5372b`  
		Last Modified: Mon, 26 Jul 2021 22:49:09 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9502bfb487c7c8ec156a40e2377f90db8fc718caf311aeded083744517a000a`  
		Last Modified: Mon, 26 Jul 2021 22:49:09 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73e0be58132932de21617b671fbcca74b337f211536ce134caa69deef3762c3`  
		Last Modified: Mon, 26 Jul 2021 22:49:06 GMT  
		Size: 547.0 KB (546952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:604f2973b7d58cdc5ad9de258e3218026fa60cf7e48847f5fdf4534944228b84`  
		Last Modified: Mon, 26 Jul 2021 22:49:34 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd7ba0494738d76004485770de8cffcdedc3552d7b998f873599958d62afd69e`  
		Last Modified: Mon, 26 Jul 2021 22:49:34 GMT  
		Size: 6.9 KB (6941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:057f372f60b20617b2723316908952d57f231b410306e9f1214070e115749ad5`  
		Last Modified: Mon, 26 Jul 2021 22:49:41 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02530942f83aa65323b363a48328cae8256da20797efaee35e8d380d07d5e90f`  
		Last Modified: Mon, 26 Jul 2021 22:49:34 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12` - linux; ppc64le

```console
$ docker pull bonita@sha256:6d42098255d7f0cc80c2f0ffb70c5c76e99739651e6aac3c2716d1e8c9ab3bad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233796336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efda9e0b763ba1558488a71d85829892d6d9dcf7a7549ca1cb1052667717c9dc`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 13 Jul 2021 23:21:55 GMT
ADD file:45b627081344651e16f78f7bbb0da81c1dcc0300835ab0f4bdd6dd93621e461d in / 
# Tue, 13 Jul 2021 23:22:00 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 04:23:21 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 14 Jul 2021 04:28:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:28:27 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 14 Jul 2021 04:28:56 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 14 Jul 2021 04:29:11 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 14 Jul 2021 04:29:17 GMT
ARG BONITA_VERSION
# Wed, 14 Jul 2021 04:32:59 GMT
ARG BRANDING_VERSION
# Wed, 14 Jul 2021 04:33:01 GMT
ARG BONITA_SHA256
# Wed, 14 Jul 2021 04:33:08 GMT
ARG BASE_URL
# Wed, 14 Jul 2021 04:33:17 GMT
ARG BONITA_URL
# Wed, 14 Jul 2021 04:33:21 GMT
ENV BONITA_VERSION=7.12.1
# Wed, 14 Jul 2021 04:33:24 GMT
ENV BRANDING_VERSION=2021.1
# Wed, 14 Jul 2021 04:33:39 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Wed, 14 Jul 2021 04:33:45 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Wed, 14 Jul 2021 04:33:52 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 14 Jul 2021 04:33:58 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Wed, 14 Jul 2021 04:34:09 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Wed, 14 Jul 2021 04:34:21 GMT
RUN mkdir /opt/files
# Wed, 14 Jul 2021 04:34:26 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Wed, 14 Jul 2021 04:34:44 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Wed, 14 Jul 2021 04:34:56 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Wed, 14 Jul 2021 04:35:04 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Wed, 14 Jul 2021 04:35:08 GMT
VOLUME [/opt/bonita]
# Wed, 14 Jul 2021 04:35:11 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 14 Jul 2021 04:35:15 GMT
EXPOSE 8080
# Wed, 14 Jul 2021 04:35:21 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:b4e702a7ed6378fce702bcf7ca7d37185cd6d8387370cd090b9dc4bf5844f47c`  
		Last Modified: Tue, 13 Jul 2021 23:27:12 GMT  
		Size: 30.4 MB (30427987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea6d20994673343d11028ac1ac0bcc098d0f1ac3b04655623d2d2cafa4bee8d`  
		Last Modified: Wed, 14 Jul 2021 04:37:02 GMT  
		Size: 86.4 MB (86395354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7a025e3dd302981f640be07c88365b3ddfa8c7d2a818971b050001fa255123`  
		Last Modified: Wed, 14 Jul 2021 04:36:46 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c867ae2580be2a8356c180288cecbeca16488f530908d5ebb203c0c5bf0a99`  
		Last Modified: Wed, 14 Jul 2021 04:36:44 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7732888c6ddf76b2f60aa2ce9638a1b17b4a33dc96c7a969b6b0a3401b8c8568`  
		Last Modified: Wed, 14 Jul 2021 04:36:41 GMT  
		Size: 546.7 KB (546731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01503d0bfb3e8749a1da3e2fe6cbf5e5208d577a78b429c339ba548a3e20f3aa`  
		Last Modified: Wed, 14 Jul 2021 04:37:15 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91434b0d6bc799538f5ccea05a983777aa3db998cee240f7e841f059c8982d1`  
		Last Modified: Wed, 14 Jul 2021 04:37:16 GMT  
		Size: 6.9 KB (6944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ceb99ecfc3b3526d131f1a01116aaaf5821a5a16c59e76ea0e83d14b7c0b5f`  
		Last Modified: Wed, 14 Jul 2021 04:37:26 GMT  
		Size: 116.4 MB (116415405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b028984ead8def425d58ddd729fc1448e107673994a53e44d976baf1ae7ad0`  
		Last Modified: Wed, 14 Jul 2021 04:37:15 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.12.1`

```console
$ docker pull bonita@sha256:32cfa6689575e7983e6a17f1afc8b096aa12369d64b17e357769b45c4d83dc74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.12.1` - linux; amd64

```console
$ docker pull bonita@sha256:b5916584fa8b0223d4f5110fb38f5c7e1d50507c9c06ae7517ff791be50ac988
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237231421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92810c0e9ab24901233e4e22bb664a65b8406726965dddc531f2f5962ac3d59a`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:30 GMT
ADD file:e729fb032bd2f7cde20fb343da0cd358447e8b23028422c123944e8d0be660fa in / 
# Mon, 26 Jul 2021 21:21:31 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:55:51 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 26 Jul 2021 22:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:56:38 GMT
RUN mkdir /opt/custom-init.d/
# Mon, 26 Jul 2021 22:56:40 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Mon, 26 Jul 2021 22:56:43 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Mon, 26 Jul 2021 22:56:43 GMT
ARG BONITA_VERSION
# Mon, 26 Jul 2021 22:57:03 GMT
ARG BRANDING_VERSION
# Mon, 26 Jul 2021 22:57:03 GMT
ARG BONITA_SHA256
# Mon, 26 Jul 2021 22:57:03 GMT
ARG BASE_URL
# Mon, 26 Jul 2021 22:57:03 GMT
ARG BONITA_URL
# Mon, 26 Jul 2021 22:57:03 GMT
ENV BONITA_VERSION=7.12.1
# Mon, 26 Jul 2021 22:57:04 GMT
ENV BRANDING_VERSION=2021.1
# Mon, 26 Jul 2021 22:57:04 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Mon, 26 Jul 2021 22:57:04 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Mon, 26 Jul 2021 22:57:04 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 26 Jul 2021 22:57:05 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Mon, 26 Jul 2021 22:57:05 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Mon, 26 Jul 2021 22:57:06 GMT
RUN mkdir /opt/files
# Mon, 26 Jul 2021 22:57:06 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Mon, 26 Jul 2021 22:57:10 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Mon, 26 Jul 2021 22:57:12 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Mon, 26 Jul 2021 22:57:13 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Mon, 26 Jul 2021 22:57:14 GMT
VOLUME [/opt/bonita]
# Mon, 26 Jul 2021 22:57:14 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Mon, 26 Jul 2021 22:57:14 GMT
EXPOSE 8080
# Mon, 26 Jul 2021 22:57:14 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:feac5306138255e28a9862d3f3d29025d0a4d0648855afe1acd6131af07138ac`  
		Last Modified: Mon, 26 Jul 2021 21:22:52 GMT  
		Size: 26.7 MB (26709039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41fbee9f4b324cc20d8988fa7cab5d9c491c1a9a380342d8846040fa5afe01a`  
		Last Modified: Mon, 26 Jul 2021 22:58:25 GMT  
		Size: 93.5 MB (93519201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ca53056372700c6fbe41da9cb2df900b3b73e9cf784ebadd79e20b3b8080d1`  
		Last Modified: Mon, 26 Jul 2021 22:58:08 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9905bd9bc78f4e660b093c94972b9bfe153be1450b65d1d94a39a66265e9f809`  
		Last Modified: Mon, 26 Jul 2021 22:58:08 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6437ef6648258db0d319ca67287e68abd9d59fd9a13cef685fcf0001eefd77`  
		Last Modified: Mon, 26 Jul 2021 22:58:05 GMT  
		Size: 576.9 KB (576937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6eb19591747c3e652808ab538441ba4b47dc4e60835c762225b47c427ec90aa`  
		Last Modified: Mon, 26 Jul 2021 22:58:38 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb19116d4d9d99e7693af7fd0f393d5a6b46eb766cacef6db42839311df87df`  
		Last Modified: Mon, 26 Jul 2021 22:58:38 GMT  
		Size: 6.9 KB (6942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee45552874f5dc095ab9338e4c91bb15548e9e55d077e57a156c058c4f5b45e`  
		Last Modified: Mon, 26 Jul 2021 22:58:46 GMT  
		Size: 116.4 MB (116415405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e8604ffcc7b25e1d701643f189b9df43053595d0435c1406ab10d73233c0e0`  
		Last Modified: Mon, 26 Jul 2021 22:58:38 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:6fef41ea5e1c154704edff635aa96d95e0f51631f6d0b337dd0502d3028e8953
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226336563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abfa77e4bfcd83636fefc618a3f25a8bec1e977a73c1393b20e51974930f5ecd`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:49 GMT
ADD file:e87e065765ef99e8db25307f469c7481ab480ac5fe6353ae4caf402766f14045 in / 
# Mon, 26 Jul 2021 21:48:50 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:47:04 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 26 Jul 2021 22:47:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:47:27 GMT
RUN mkdir /opt/custom-init.d/
# Mon, 26 Jul 2021 22:47:27 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Mon, 26 Jul 2021 22:47:35 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Mon, 26 Jul 2021 22:47:35 GMT
ARG BONITA_VERSION
# Mon, 26 Jul 2021 22:47:56 GMT
ARG BRANDING_VERSION
# Mon, 26 Jul 2021 22:47:56 GMT
ARG BONITA_SHA256
# Mon, 26 Jul 2021 22:47:56 GMT
ARG BASE_URL
# Mon, 26 Jul 2021 22:47:57 GMT
ARG BONITA_URL
# Mon, 26 Jul 2021 22:47:57 GMT
ENV BONITA_VERSION=7.12.1
# Mon, 26 Jul 2021 22:47:57 GMT
ENV BRANDING_VERSION=2021.1
# Mon, 26 Jul 2021 22:47:57 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Mon, 26 Jul 2021 22:47:57 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Mon, 26 Jul 2021 22:47:57 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 26 Jul 2021 22:47:58 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Mon, 26 Jul 2021 22:47:58 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Mon, 26 Jul 2021 22:47:59 GMT
RUN mkdir /opt/files
# Mon, 26 Jul 2021 22:47:59 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Mon, 26 Jul 2021 22:48:03 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Mon, 26 Jul 2021 22:48:04 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Mon, 26 Jul 2021 22:48:06 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Mon, 26 Jul 2021 22:48:06 GMT
VOLUME [/opt/bonita]
# Mon, 26 Jul 2021 22:48:06 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Mon, 26 Jul 2021 22:48:06 GMT
EXPOSE 8080
# Mon, 26 Jul 2021 22:48:06 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:fda1cca7a3cc2b66c161597f27e151a9b1cab79d73c7c0c2706606813a3e58cf`  
		Last Modified: Mon, 26 Jul 2021 21:50:37 GMT  
		Size: 23.7 MB (23731597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a32c2e693656a5434b587ae1cfac238a95021569769a39d83ef10e89e26121b`  
		Last Modified: Mon, 26 Jul 2021 22:49:21 GMT  
		Size: 85.6 MB (85631763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad214e302609f03f40484c257c896f8ebd558d57ec6c206420d30d631d5372b`  
		Last Modified: Mon, 26 Jul 2021 22:49:09 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9502bfb487c7c8ec156a40e2377f90db8fc718caf311aeded083744517a000a`  
		Last Modified: Mon, 26 Jul 2021 22:49:09 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73e0be58132932de21617b671fbcca74b337f211536ce134caa69deef3762c3`  
		Last Modified: Mon, 26 Jul 2021 22:49:06 GMT  
		Size: 547.0 KB (546952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:604f2973b7d58cdc5ad9de258e3218026fa60cf7e48847f5fdf4534944228b84`  
		Last Modified: Mon, 26 Jul 2021 22:49:34 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd7ba0494738d76004485770de8cffcdedc3552d7b998f873599958d62afd69e`  
		Last Modified: Mon, 26 Jul 2021 22:49:34 GMT  
		Size: 6.9 KB (6941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:057f372f60b20617b2723316908952d57f231b410306e9f1214070e115749ad5`  
		Last Modified: Mon, 26 Jul 2021 22:49:41 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02530942f83aa65323b363a48328cae8256da20797efaee35e8d380d07d5e90f`  
		Last Modified: Mon, 26 Jul 2021 22:49:34 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:6d42098255d7f0cc80c2f0ffb70c5c76e99739651e6aac3c2716d1e8c9ab3bad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233796336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efda9e0b763ba1558488a71d85829892d6d9dcf7a7549ca1cb1052667717c9dc`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 13 Jul 2021 23:21:55 GMT
ADD file:45b627081344651e16f78f7bbb0da81c1dcc0300835ab0f4bdd6dd93621e461d in / 
# Tue, 13 Jul 2021 23:22:00 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 04:23:21 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 14 Jul 2021 04:28:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:28:27 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 14 Jul 2021 04:28:56 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 14 Jul 2021 04:29:11 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 14 Jul 2021 04:29:17 GMT
ARG BONITA_VERSION
# Wed, 14 Jul 2021 04:32:59 GMT
ARG BRANDING_VERSION
# Wed, 14 Jul 2021 04:33:01 GMT
ARG BONITA_SHA256
# Wed, 14 Jul 2021 04:33:08 GMT
ARG BASE_URL
# Wed, 14 Jul 2021 04:33:17 GMT
ARG BONITA_URL
# Wed, 14 Jul 2021 04:33:21 GMT
ENV BONITA_VERSION=7.12.1
# Wed, 14 Jul 2021 04:33:24 GMT
ENV BRANDING_VERSION=2021.1
# Wed, 14 Jul 2021 04:33:39 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Wed, 14 Jul 2021 04:33:45 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Wed, 14 Jul 2021 04:33:52 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 14 Jul 2021 04:33:58 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Wed, 14 Jul 2021 04:34:09 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Wed, 14 Jul 2021 04:34:21 GMT
RUN mkdir /opt/files
# Wed, 14 Jul 2021 04:34:26 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Wed, 14 Jul 2021 04:34:44 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Wed, 14 Jul 2021 04:34:56 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Wed, 14 Jul 2021 04:35:04 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Wed, 14 Jul 2021 04:35:08 GMT
VOLUME [/opt/bonita]
# Wed, 14 Jul 2021 04:35:11 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 14 Jul 2021 04:35:15 GMT
EXPOSE 8080
# Wed, 14 Jul 2021 04:35:21 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:b4e702a7ed6378fce702bcf7ca7d37185cd6d8387370cd090b9dc4bf5844f47c`  
		Last Modified: Tue, 13 Jul 2021 23:27:12 GMT  
		Size: 30.4 MB (30427987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea6d20994673343d11028ac1ac0bcc098d0f1ac3b04655623d2d2cafa4bee8d`  
		Last Modified: Wed, 14 Jul 2021 04:37:02 GMT  
		Size: 86.4 MB (86395354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7a025e3dd302981f640be07c88365b3ddfa8c7d2a818971b050001fa255123`  
		Last Modified: Wed, 14 Jul 2021 04:36:46 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c867ae2580be2a8356c180288cecbeca16488f530908d5ebb203c0c5bf0a99`  
		Last Modified: Wed, 14 Jul 2021 04:36:44 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7732888c6ddf76b2f60aa2ce9638a1b17b4a33dc96c7a969b6b0a3401b8c8568`  
		Last Modified: Wed, 14 Jul 2021 04:36:41 GMT  
		Size: 546.7 KB (546731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01503d0bfb3e8749a1da3e2fe6cbf5e5208d577a78b429c339ba548a3e20f3aa`  
		Last Modified: Wed, 14 Jul 2021 04:37:15 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91434b0d6bc799538f5ccea05a983777aa3db998cee240f7e841f059c8982d1`  
		Last Modified: Wed, 14 Jul 2021 04:37:16 GMT  
		Size: 6.9 KB (6944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ceb99ecfc3b3526d131f1a01116aaaf5821a5a16c59e76ea0e83d14b7c0b5f`  
		Last Modified: Wed, 14 Jul 2021 04:37:26 GMT  
		Size: 116.4 MB (116415405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b028984ead8def425d58ddd729fc1448e107673994a53e44d976baf1ae7ad0`  
		Last Modified: Wed, 14 Jul 2021 04:37:15 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:latest`

```console
$ docker pull bonita@sha256:32cfa6689575e7983e6a17f1afc8b096aa12369d64b17e357769b45c4d83dc74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:latest` - linux; amd64

```console
$ docker pull bonita@sha256:b5916584fa8b0223d4f5110fb38f5c7e1d50507c9c06ae7517ff791be50ac988
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237231421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92810c0e9ab24901233e4e22bb664a65b8406726965dddc531f2f5962ac3d59a`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:30 GMT
ADD file:e729fb032bd2f7cde20fb343da0cd358447e8b23028422c123944e8d0be660fa in / 
# Mon, 26 Jul 2021 21:21:31 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:55:51 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 26 Jul 2021 22:56:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:56:38 GMT
RUN mkdir /opt/custom-init.d/
# Mon, 26 Jul 2021 22:56:40 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Mon, 26 Jul 2021 22:56:43 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Mon, 26 Jul 2021 22:56:43 GMT
ARG BONITA_VERSION
# Mon, 26 Jul 2021 22:57:03 GMT
ARG BRANDING_VERSION
# Mon, 26 Jul 2021 22:57:03 GMT
ARG BONITA_SHA256
# Mon, 26 Jul 2021 22:57:03 GMT
ARG BASE_URL
# Mon, 26 Jul 2021 22:57:03 GMT
ARG BONITA_URL
# Mon, 26 Jul 2021 22:57:03 GMT
ENV BONITA_VERSION=7.12.1
# Mon, 26 Jul 2021 22:57:04 GMT
ENV BRANDING_VERSION=2021.1
# Mon, 26 Jul 2021 22:57:04 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Mon, 26 Jul 2021 22:57:04 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Mon, 26 Jul 2021 22:57:04 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 26 Jul 2021 22:57:05 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Mon, 26 Jul 2021 22:57:05 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Mon, 26 Jul 2021 22:57:06 GMT
RUN mkdir /opt/files
# Mon, 26 Jul 2021 22:57:06 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Mon, 26 Jul 2021 22:57:10 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Mon, 26 Jul 2021 22:57:12 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Mon, 26 Jul 2021 22:57:13 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Mon, 26 Jul 2021 22:57:14 GMT
VOLUME [/opt/bonita]
# Mon, 26 Jul 2021 22:57:14 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Mon, 26 Jul 2021 22:57:14 GMT
EXPOSE 8080
# Mon, 26 Jul 2021 22:57:14 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:feac5306138255e28a9862d3f3d29025d0a4d0648855afe1acd6131af07138ac`  
		Last Modified: Mon, 26 Jul 2021 21:22:52 GMT  
		Size: 26.7 MB (26709039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41fbee9f4b324cc20d8988fa7cab5d9c491c1a9a380342d8846040fa5afe01a`  
		Last Modified: Mon, 26 Jul 2021 22:58:25 GMT  
		Size: 93.5 MB (93519201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ca53056372700c6fbe41da9cb2df900b3b73e9cf784ebadd79e20b3b8080d1`  
		Last Modified: Mon, 26 Jul 2021 22:58:08 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9905bd9bc78f4e660b093c94972b9bfe153be1450b65d1d94a39a66265e9f809`  
		Last Modified: Mon, 26 Jul 2021 22:58:08 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6437ef6648258db0d319ca67287e68abd9d59fd9a13cef685fcf0001eefd77`  
		Last Modified: Mon, 26 Jul 2021 22:58:05 GMT  
		Size: 576.9 KB (576937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6eb19591747c3e652808ab538441ba4b47dc4e60835c762225b47c427ec90aa`  
		Last Modified: Mon, 26 Jul 2021 22:58:38 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb19116d4d9d99e7693af7fd0f393d5a6b46eb766cacef6db42839311df87df`  
		Last Modified: Mon, 26 Jul 2021 22:58:38 GMT  
		Size: 6.9 KB (6942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee45552874f5dc095ab9338e4c91bb15548e9e55d077e57a156c058c4f5b45e`  
		Last Modified: Mon, 26 Jul 2021 22:58:46 GMT  
		Size: 116.4 MB (116415405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e8604ffcc7b25e1d701643f189b9df43053595d0435c1406ab10d73233c0e0`  
		Last Modified: Mon, 26 Jul 2021 22:58:38 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:6fef41ea5e1c154704edff635aa96d95e0f51631f6d0b337dd0502d3028e8953
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226336563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abfa77e4bfcd83636fefc618a3f25a8bec1e977a73c1393b20e51974930f5ecd`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:49 GMT
ADD file:e87e065765ef99e8db25307f469c7481ab480ac5fe6353ae4caf402766f14045 in / 
# Mon, 26 Jul 2021 21:48:50 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:47:04 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 26 Jul 2021 22:47:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:47:27 GMT
RUN mkdir /opt/custom-init.d/
# Mon, 26 Jul 2021 22:47:27 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Mon, 26 Jul 2021 22:47:35 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Mon, 26 Jul 2021 22:47:35 GMT
ARG BONITA_VERSION
# Mon, 26 Jul 2021 22:47:56 GMT
ARG BRANDING_VERSION
# Mon, 26 Jul 2021 22:47:56 GMT
ARG BONITA_SHA256
# Mon, 26 Jul 2021 22:47:56 GMT
ARG BASE_URL
# Mon, 26 Jul 2021 22:47:57 GMT
ARG BONITA_URL
# Mon, 26 Jul 2021 22:47:57 GMT
ENV BONITA_VERSION=7.12.1
# Mon, 26 Jul 2021 22:47:57 GMT
ENV BRANDING_VERSION=2021.1
# Mon, 26 Jul 2021 22:47:57 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Mon, 26 Jul 2021 22:47:57 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Mon, 26 Jul 2021 22:47:57 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 26 Jul 2021 22:47:58 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Mon, 26 Jul 2021 22:47:58 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Mon, 26 Jul 2021 22:47:59 GMT
RUN mkdir /opt/files
# Mon, 26 Jul 2021 22:47:59 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Mon, 26 Jul 2021 22:48:03 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Mon, 26 Jul 2021 22:48:04 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Mon, 26 Jul 2021 22:48:06 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Mon, 26 Jul 2021 22:48:06 GMT
VOLUME [/opt/bonita]
# Mon, 26 Jul 2021 22:48:06 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Mon, 26 Jul 2021 22:48:06 GMT
EXPOSE 8080
# Mon, 26 Jul 2021 22:48:06 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:fda1cca7a3cc2b66c161597f27e151a9b1cab79d73c7c0c2706606813a3e58cf`  
		Last Modified: Mon, 26 Jul 2021 21:50:37 GMT  
		Size: 23.7 MB (23731597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a32c2e693656a5434b587ae1cfac238a95021569769a39d83ef10e89e26121b`  
		Last Modified: Mon, 26 Jul 2021 22:49:21 GMT  
		Size: 85.6 MB (85631763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad214e302609f03f40484c257c896f8ebd558d57ec6c206420d30d631d5372b`  
		Last Modified: Mon, 26 Jul 2021 22:49:09 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9502bfb487c7c8ec156a40e2377f90db8fc718caf311aeded083744517a000a`  
		Last Modified: Mon, 26 Jul 2021 22:49:09 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73e0be58132932de21617b671fbcca74b337f211536ce134caa69deef3762c3`  
		Last Modified: Mon, 26 Jul 2021 22:49:06 GMT  
		Size: 547.0 KB (546952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:604f2973b7d58cdc5ad9de258e3218026fa60cf7e48847f5fdf4534944228b84`  
		Last Modified: Mon, 26 Jul 2021 22:49:34 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd7ba0494738d76004485770de8cffcdedc3552d7b998f873599958d62afd69e`  
		Last Modified: Mon, 26 Jul 2021 22:49:34 GMT  
		Size: 6.9 KB (6941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:057f372f60b20617b2723316908952d57f231b410306e9f1214070e115749ad5`  
		Last Modified: Mon, 26 Jul 2021 22:49:41 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02530942f83aa65323b363a48328cae8256da20797efaee35e8d380d07d5e90f`  
		Last Modified: Mon, 26 Jul 2021 22:49:34 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; ppc64le

```console
$ docker pull bonita@sha256:6d42098255d7f0cc80c2f0ffb70c5c76e99739651e6aac3c2716d1e8c9ab3bad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233796336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efda9e0b763ba1558488a71d85829892d6d9dcf7a7549ca1cb1052667717c9dc`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 13 Jul 2021 23:21:55 GMT
ADD file:45b627081344651e16f78f7bbb0da81c1dcc0300835ab0f4bdd6dd93621e461d in / 
# Tue, 13 Jul 2021 23:22:00 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 04:23:21 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 14 Jul 2021 04:28:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:28:27 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 14 Jul 2021 04:28:56 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 14 Jul 2021 04:29:11 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 14 Jul 2021 04:29:17 GMT
ARG BONITA_VERSION
# Wed, 14 Jul 2021 04:32:59 GMT
ARG BRANDING_VERSION
# Wed, 14 Jul 2021 04:33:01 GMT
ARG BONITA_SHA256
# Wed, 14 Jul 2021 04:33:08 GMT
ARG BASE_URL
# Wed, 14 Jul 2021 04:33:17 GMT
ARG BONITA_URL
# Wed, 14 Jul 2021 04:33:21 GMT
ENV BONITA_VERSION=7.12.1
# Wed, 14 Jul 2021 04:33:24 GMT
ENV BRANDING_VERSION=2021.1
# Wed, 14 Jul 2021 04:33:39 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Wed, 14 Jul 2021 04:33:45 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Wed, 14 Jul 2021 04:33:52 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 14 Jul 2021 04:33:58 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Wed, 14 Jul 2021 04:34:09 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Wed, 14 Jul 2021 04:34:21 GMT
RUN mkdir /opt/files
# Wed, 14 Jul 2021 04:34:26 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Wed, 14 Jul 2021 04:34:44 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Wed, 14 Jul 2021 04:34:56 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Wed, 14 Jul 2021 04:35:04 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Wed, 14 Jul 2021 04:35:08 GMT
VOLUME [/opt/bonita]
# Wed, 14 Jul 2021 04:35:11 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 14 Jul 2021 04:35:15 GMT
EXPOSE 8080
# Wed, 14 Jul 2021 04:35:21 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:b4e702a7ed6378fce702bcf7ca7d37185cd6d8387370cd090b9dc4bf5844f47c`  
		Last Modified: Tue, 13 Jul 2021 23:27:12 GMT  
		Size: 30.4 MB (30427987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea6d20994673343d11028ac1ac0bcc098d0f1ac3b04655623d2d2cafa4bee8d`  
		Last Modified: Wed, 14 Jul 2021 04:37:02 GMT  
		Size: 86.4 MB (86395354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7a025e3dd302981f640be07c88365b3ddfa8c7d2a818971b050001fa255123`  
		Last Modified: Wed, 14 Jul 2021 04:36:46 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c867ae2580be2a8356c180288cecbeca16488f530908d5ebb203c0c5bf0a99`  
		Last Modified: Wed, 14 Jul 2021 04:36:44 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7732888c6ddf76b2f60aa2ce9638a1b17b4a33dc96c7a969b6b0a3401b8c8568`  
		Last Modified: Wed, 14 Jul 2021 04:36:41 GMT  
		Size: 546.7 KB (546731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01503d0bfb3e8749a1da3e2fe6cbf5e5208d577a78b429c339ba548a3e20f3aa`  
		Last Modified: Wed, 14 Jul 2021 04:37:15 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91434b0d6bc799538f5ccea05a983777aa3db998cee240f7e841f059c8982d1`  
		Last Modified: Wed, 14 Jul 2021 04:37:16 GMT  
		Size: 6.9 KB (6944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ceb99ecfc3b3526d131f1a01116aaaf5821a5a16c59e76ea0e83d14b7c0b5f`  
		Last Modified: Wed, 14 Jul 2021 04:37:26 GMT  
		Size: 116.4 MB (116415405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b028984ead8def425d58ddd729fc1448e107673994a53e44d976baf1ae7ad0`  
		Last Modified: Wed, 14 Jul 2021 04:37:15 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
