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
