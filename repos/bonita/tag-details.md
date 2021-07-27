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
$ docker pull bonita@sha256:c437992c1cc00db5f552cbfa1dfdad6f0daa6939e597f966a63b632881d786d1
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
$ docker pull bonita@sha256:32b0d47166ca68736fe0797ac6908cb1aa17970d8c4c28c5374e65c894a47775
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233848935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edded5279ca8e8bd58eea6c07ee43a8ce9fde41439b2e28411445343ce7e6fd6`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Mon, 26 Jul 2021 23:12:31 GMT
ADD file:2e6f05bbffb47b3ea8e5e4127452e80debc89fb9e22af2dc5c735ea579adad64 in / 
# Mon, 26 Jul 2021 23:12:34 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:48:05 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 27 Jul 2021 01:49:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:50:07 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 27 Jul 2021 01:50:15 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 27 Jul 2021 01:50:23 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 27 Jul 2021 01:50:25 GMT
ARG BONITA_VERSION
# Tue, 27 Jul 2021 01:51:49 GMT
ARG BRANDING_VERSION
# Tue, 27 Jul 2021 01:51:51 GMT
ARG BONITA_SHA256
# Tue, 27 Jul 2021 01:51:53 GMT
ARG BASE_URL
# Tue, 27 Jul 2021 01:51:58 GMT
ARG BONITA_URL
# Tue, 27 Jul 2021 01:52:00 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 27 Jul 2021 01:52:02 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 27 Jul 2021 01:52:06 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 27 Jul 2021 01:52:09 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 27 Jul 2021 01:52:12 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 27 Jul 2021 01:52:13 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 27 Jul 2021 01:52:16 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 27 Jul 2021 01:52:20 GMT
RUN mkdir /opt/files
# Tue, 27 Jul 2021 01:52:21 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 27 Jul 2021 01:52:31 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 27 Jul 2021 01:52:41 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 27 Jul 2021 01:52:50 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 27 Jul 2021 01:52:53 GMT
VOLUME [/opt/bonita]
# Tue, 27 Jul 2021 01:52:56 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 27 Jul 2021 01:53:03 GMT
EXPOSE 8080
# Tue, 27 Jul 2021 01:53:10 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:3c742a0b2a0025420dcf1bc91d81de2ffb292328fad483ce715521d725503b66`  
		Last Modified: Mon, 26 Jul 2021 23:15:30 GMT  
		Size: 30.4 MB (30437958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122e38cf8ca67c15cafbfb79b10cc63db576f58b99dc6263f8f559ece480fc98`  
		Last Modified: Tue, 27 Jul 2021 01:54:51 GMT  
		Size: 86.4 MB (86437995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0a3a3c9c04402a88e8ea2b6d49b056fcf131a881d2edadaace8b0210815457`  
		Last Modified: Tue, 27 Jul 2021 01:54:32 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fefdc9fcd6ac38c5ffba630155d3fe6932b659a42bf83468548e79583d7537b`  
		Last Modified: Tue, 27 Jul 2021 01:54:32 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a7810bc793a156fe6f7ab91a2bda750971a3a25fc51b31bede2b04fcac68f7`  
		Last Modified: Tue, 27 Jul 2021 01:54:29 GMT  
		Size: 546.7 KB (546729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562af50260f536c102631c3e00af1641a5ef89b02d7eeb8b4f175ac07047b7b0`  
		Last Modified: Tue, 27 Jul 2021 01:55:03 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4549b34b465cf2aa005e75cd1344237ede2babc3e6c848ce3a94d85cb7aec0`  
		Last Modified: Tue, 27 Jul 2021 01:55:03 GMT  
		Size: 6.9 KB (6949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d1515dc066d8f53657c19bdf13096ba8d63b29f80bb948a9e9584ed676ceea5`  
		Last Modified: Tue, 27 Jul 2021 01:55:11 GMT  
		Size: 116.4 MB (116415406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f22fe0852be4639aef4dddb02e14e1edce7a98c01793e260a099ec9455b957`  
		Last Modified: Tue, 27 Jul 2021 01:55:03 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.10`

```console
$ docker pull bonita@sha256:4cd6ba6ebb9128d834d42a91c583b7b73b5130e05679b86738d3fdb90f8a4658
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
$ docker pull bonita@sha256:7435337c5b03201e08d6c5480f979dda62a5ab7a3476445b8dd29f98f7324ba8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240327363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ea392201ab7d7e95ba4100cd9cda81f9c7c264c03221dad7b9da413817b785`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Mon, 26 Jul 2021 23:12:31 GMT
ADD file:2e6f05bbffb47b3ea8e5e4127452e80debc89fb9e22af2dc5c735ea579adad64 in / 
# Mon, 26 Jul 2021 23:12:34 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:40:40 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Tue, 27 Jul 2021 01:46:05 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:46:17 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 27 Jul 2021 01:46:26 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 27 Jul 2021 01:46:36 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 27 Jul 2021 01:46:40 GMT
ARG BONITA_VERSION
# Tue, 27 Jul 2021 01:46:42 GMT
ARG BONITA_SHA256
# Tue, 27 Jul 2021 01:46:43 GMT
ARG BASE_URL
# Tue, 27 Jul 2021 01:46:45 GMT
ARG BONITA_URL
# Tue, 27 Jul 2021 01:46:49 GMT
ENV BONITA_VERSION=7.10.6
# Tue, 27 Jul 2021 01:46:53 GMT
ENV BONITA_SHA256=aaf61a044e7a8d9ec95d2b5d0c315a6d01d9c93ba01d753fcb008e2cfbbb725f
# Tue, 27 Jul 2021 01:46:54 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 27 Jul 2021 01:46:56 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.10.6/BonitaCommunity-7.10.6.zip
# Tue, 27 Jul 2021 01:47:06 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Tue, 27 Jul 2021 01:47:18 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Tue, 27 Jul 2021 01:47:34 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Tue, 27 Jul 2021 01:47:44 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Tue, 27 Jul 2021 01:47:46 GMT
VOLUME [/opt/bonita]
# Tue, 27 Jul 2021 01:47:47 GMT
COPY dir:46816633cc37ba9fd23af260c8c2384c15f3b4385b5752d6b42577967959f7f0 in /opt/files 
# Tue, 27 Jul 2021 01:47:48 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Tue, 27 Jul 2021 01:47:50 GMT
EXPOSE 8080
# Tue, 27 Jul 2021 01:47:52 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:3c742a0b2a0025420dcf1bc91d81de2ffb292328fad483ce715521d725503b66`  
		Last Modified: Mon, 26 Jul 2021 23:15:30 GMT  
		Size: 30.4 MB (30437958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0524c28c2164d9b09796ddd2f83322f39ef57ffb02016ebbab0f892718ed6f3c`  
		Last Modified: Tue, 27 Jul 2021 01:54:16 GMT  
		Size: 111.4 MB (111357324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c297c471637309e3e9fde7207a7fc74cd183cf576f4c0e5b76e3f773b6477d0`  
		Last Modified: Tue, 27 Jul 2021 01:53:56 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c51ff6961145bafb2cbf5f9fd74b019531a479ce3f5ba8be9e5cded0f0cd466`  
		Last Modified: Tue, 27 Jul 2021 01:53:54 GMT  
		Size: 1.9 KB (1924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac381df1a0a13c356b1bc75f7bd3734a4f73d7d18f31502868dfe1dea35a9fe4`  
		Last Modified: Tue, 27 Jul 2021 01:53:54 GMT  
		Size: 546.7 KB (546735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44111302069faf8885ad262753b2cc3d01e90ef24c63aed05e824d857e7f3ffb`  
		Last Modified: Tue, 27 Jul 2021 01:54:03 GMT  
		Size: 98.0 MB (97973960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fc58828439256fab66ae7073d00350a28abd601e4148e168545faac8ff5e29`  
		Last Modified: Tue, 27 Jul 2021 01:53:54 GMT  
		Size: 7.7 KB (7653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d835501ba5de751fcfea8da4da19c29d17731a0cb81fc0b0110c3fbee5cdc863`  
		Last Modified: Tue, 27 Jul 2021 01:53:54 GMT  
		Size: 1.7 KB (1653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.10.6`

```console
$ docker pull bonita@sha256:4cd6ba6ebb9128d834d42a91c583b7b73b5130e05679b86738d3fdb90f8a4658
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
$ docker pull bonita@sha256:7435337c5b03201e08d6c5480f979dda62a5ab7a3476445b8dd29f98f7324ba8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240327363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ea392201ab7d7e95ba4100cd9cda81f9c7c264c03221dad7b9da413817b785`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Mon, 26 Jul 2021 23:12:31 GMT
ADD file:2e6f05bbffb47b3ea8e5e4127452e80debc89fb9e22af2dc5c735ea579adad64 in / 
# Mon, 26 Jul 2021 23:12:34 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:40:40 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Tue, 27 Jul 2021 01:46:05 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:46:17 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 27 Jul 2021 01:46:26 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 27 Jul 2021 01:46:36 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 27 Jul 2021 01:46:40 GMT
ARG BONITA_VERSION
# Tue, 27 Jul 2021 01:46:42 GMT
ARG BONITA_SHA256
# Tue, 27 Jul 2021 01:46:43 GMT
ARG BASE_URL
# Tue, 27 Jul 2021 01:46:45 GMT
ARG BONITA_URL
# Tue, 27 Jul 2021 01:46:49 GMT
ENV BONITA_VERSION=7.10.6
# Tue, 27 Jul 2021 01:46:53 GMT
ENV BONITA_SHA256=aaf61a044e7a8d9ec95d2b5d0c315a6d01d9c93ba01d753fcb008e2cfbbb725f
# Tue, 27 Jul 2021 01:46:54 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 27 Jul 2021 01:46:56 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.10.6/BonitaCommunity-7.10.6.zip
# Tue, 27 Jul 2021 01:47:06 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Tue, 27 Jul 2021 01:47:18 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Tue, 27 Jul 2021 01:47:34 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Tue, 27 Jul 2021 01:47:44 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Tue, 27 Jul 2021 01:47:46 GMT
VOLUME [/opt/bonita]
# Tue, 27 Jul 2021 01:47:47 GMT
COPY dir:46816633cc37ba9fd23af260c8c2384c15f3b4385b5752d6b42577967959f7f0 in /opt/files 
# Tue, 27 Jul 2021 01:47:48 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Tue, 27 Jul 2021 01:47:50 GMT
EXPOSE 8080
# Tue, 27 Jul 2021 01:47:52 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:3c742a0b2a0025420dcf1bc91d81de2ffb292328fad483ce715521d725503b66`  
		Last Modified: Mon, 26 Jul 2021 23:15:30 GMT  
		Size: 30.4 MB (30437958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0524c28c2164d9b09796ddd2f83322f39ef57ffb02016ebbab0f892718ed6f3c`  
		Last Modified: Tue, 27 Jul 2021 01:54:16 GMT  
		Size: 111.4 MB (111357324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c297c471637309e3e9fde7207a7fc74cd183cf576f4c0e5b76e3f773b6477d0`  
		Last Modified: Tue, 27 Jul 2021 01:53:56 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c51ff6961145bafb2cbf5f9fd74b019531a479ce3f5ba8be9e5cded0f0cd466`  
		Last Modified: Tue, 27 Jul 2021 01:53:54 GMT  
		Size: 1.9 KB (1924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac381df1a0a13c356b1bc75f7bd3734a4f73d7d18f31502868dfe1dea35a9fe4`  
		Last Modified: Tue, 27 Jul 2021 01:53:54 GMT  
		Size: 546.7 KB (546735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44111302069faf8885ad262753b2cc3d01e90ef24c63aed05e824d857e7f3ffb`  
		Last Modified: Tue, 27 Jul 2021 01:54:03 GMT  
		Size: 98.0 MB (97973960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fc58828439256fab66ae7073d00350a28abd601e4148e168545faac8ff5e29`  
		Last Modified: Tue, 27 Jul 2021 01:53:54 GMT  
		Size: 7.7 KB (7653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d835501ba5de751fcfea8da4da19c29d17731a0cb81fc0b0110c3fbee5cdc863`  
		Last Modified: Tue, 27 Jul 2021 01:53:54 GMT  
		Size: 1.7 KB (1653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.11`

```console
$ docker pull bonita@sha256:9b2444a5a1ba806af3d8b0b88012dfefdfdd49e83ba381569d1d0c7b23032b8e
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
$ docker pull bonita@sha256:7ce17467fcbb85e33497e8b0b03596ebb76ff0f5f1377054265f062c13990c93
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230781303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39ca1e3f339e3988174dde935282fbeb3c2ba5254c92a68512c469fd4c938b69`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Mon, 26 Jul 2021 23:12:31 GMT
ADD file:2e6f05bbffb47b3ea8e5e4127452e80debc89fb9e22af2dc5c735ea579adad64 in / 
# Mon, 26 Jul 2021 23:12:34 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:48:05 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 27 Jul 2021 01:49:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:50:07 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 27 Jul 2021 01:50:15 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 27 Jul 2021 01:50:23 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 27 Jul 2021 01:50:25 GMT
ARG BONITA_VERSION
# Tue, 27 Jul 2021 01:50:27 GMT
ARG BONITA_SHA256
# Tue, 27 Jul 2021 01:50:28 GMT
ARG BASE_URL
# Tue, 27 Jul 2021 01:50:30 GMT
ARG BONITA_URL
# Tue, 27 Jul 2021 01:50:31 GMT
ENV BONITA_VERSION=7.11.4
# Tue, 27 Jul 2021 01:50:32 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Tue, 27 Jul 2021 01:50:34 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Tue, 27 Jul 2021 01:50:36 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 27 Jul 2021 01:50:38 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Tue, 27 Jul 2021 01:50:42 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 27 Jul 2021 01:50:48 GMT
RUN mkdir /opt/files
# Tue, 27 Jul 2021 01:50:52 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Tue, 27 Jul 2021 01:51:04 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Tue, 27 Jul 2021 01:51:13 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 27 Jul 2021 01:51:20 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 27 Jul 2021 01:51:23 GMT
VOLUME [/opt/bonita]
# Tue, 27 Jul 2021 01:51:25 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 27 Jul 2021 01:51:29 GMT
EXPOSE 8080
# Tue, 27 Jul 2021 01:51:33 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:3c742a0b2a0025420dcf1bc91d81de2ffb292328fad483ce715521d725503b66`  
		Last Modified: Mon, 26 Jul 2021 23:15:30 GMT  
		Size: 30.4 MB (30437958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122e38cf8ca67c15cafbfb79b10cc63db576f58b99dc6263f8f559ece480fc98`  
		Last Modified: Tue, 27 Jul 2021 01:54:51 GMT  
		Size: 86.4 MB (86437995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0a3a3c9c04402a88e8ea2b6d49b056fcf131a881d2edadaace8b0210815457`  
		Last Modified: Tue, 27 Jul 2021 01:54:32 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fefdc9fcd6ac38c5ffba630155d3fe6932b659a42bf83468548e79583d7537b`  
		Last Modified: Tue, 27 Jul 2021 01:54:32 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a7810bc793a156fe6f7ab91a2bda750971a3a25fc51b31bede2b04fcac68f7`  
		Last Modified: Tue, 27 Jul 2021 01:54:29 GMT  
		Size: 546.7 KB (546729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96569f8db6fc0c27d54e0b17ce10f27fa4a146eb7d3c36daee069c1544245025`  
		Last Modified: Tue, 27 Jul 2021 01:54:28 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c17b3820e9395f8fcca7f3e8a32db1158c904bdefb6a5521a404960cfe579ad`  
		Last Modified: Tue, 27 Jul 2021 01:54:28 GMT  
		Size: 6.9 KB (6895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e6865a3e5096e25d9be57177db42f935a66f9fa09f1be3e1631dec3afd5d82`  
		Last Modified: Tue, 27 Jul 2021 01:54:38 GMT  
		Size: 113.3 MB (113347832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c67662f3856a170290f7ab939a737d1ea97d30b90fea5a8e88468683fb53159`  
		Last Modified: Tue, 27 Jul 2021 01:54:28 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.11.4`

```console
$ docker pull bonita@sha256:9b2444a5a1ba806af3d8b0b88012dfefdfdd49e83ba381569d1d0c7b23032b8e
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
$ docker pull bonita@sha256:7ce17467fcbb85e33497e8b0b03596ebb76ff0f5f1377054265f062c13990c93
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230781303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39ca1e3f339e3988174dde935282fbeb3c2ba5254c92a68512c469fd4c938b69`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Mon, 26 Jul 2021 23:12:31 GMT
ADD file:2e6f05bbffb47b3ea8e5e4127452e80debc89fb9e22af2dc5c735ea579adad64 in / 
# Mon, 26 Jul 2021 23:12:34 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:48:05 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 27 Jul 2021 01:49:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:50:07 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 27 Jul 2021 01:50:15 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 27 Jul 2021 01:50:23 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 27 Jul 2021 01:50:25 GMT
ARG BONITA_VERSION
# Tue, 27 Jul 2021 01:50:27 GMT
ARG BONITA_SHA256
# Tue, 27 Jul 2021 01:50:28 GMT
ARG BASE_URL
# Tue, 27 Jul 2021 01:50:30 GMT
ARG BONITA_URL
# Tue, 27 Jul 2021 01:50:31 GMT
ENV BONITA_VERSION=7.11.4
# Tue, 27 Jul 2021 01:50:32 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Tue, 27 Jul 2021 01:50:34 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Tue, 27 Jul 2021 01:50:36 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 27 Jul 2021 01:50:38 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Tue, 27 Jul 2021 01:50:42 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 27 Jul 2021 01:50:48 GMT
RUN mkdir /opt/files
# Tue, 27 Jul 2021 01:50:52 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Tue, 27 Jul 2021 01:51:04 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Tue, 27 Jul 2021 01:51:13 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 27 Jul 2021 01:51:20 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 27 Jul 2021 01:51:23 GMT
VOLUME [/opt/bonita]
# Tue, 27 Jul 2021 01:51:25 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 27 Jul 2021 01:51:29 GMT
EXPOSE 8080
# Tue, 27 Jul 2021 01:51:33 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:3c742a0b2a0025420dcf1bc91d81de2ffb292328fad483ce715521d725503b66`  
		Last Modified: Mon, 26 Jul 2021 23:15:30 GMT  
		Size: 30.4 MB (30437958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122e38cf8ca67c15cafbfb79b10cc63db576f58b99dc6263f8f559ece480fc98`  
		Last Modified: Tue, 27 Jul 2021 01:54:51 GMT  
		Size: 86.4 MB (86437995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0a3a3c9c04402a88e8ea2b6d49b056fcf131a881d2edadaace8b0210815457`  
		Last Modified: Tue, 27 Jul 2021 01:54:32 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fefdc9fcd6ac38c5ffba630155d3fe6932b659a42bf83468548e79583d7537b`  
		Last Modified: Tue, 27 Jul 2021 01:54:32 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a7810bc793a156fe6f7ab91a2bda750971a3a25fc51b31bede2b04fcac68f7`  
		Last Modified: Tue, 27 Jul 2021 01:54:29 GMT  
		Size: 546.7 KB (546729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96569f8db6fc0c27d54e0b17ce10f27fa4a146eb7d3c36daee069c1544245025`  
		Last Modified: Tue, 27 Jul 2021 01:54:28 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c17b3820e9395f8fcca7f3e8a32db1158c904bdefb6a5521a404960cfe579ad`  
		Last Modified: Tue, 27 Jul 2021 01:54:28 GMT  
		Size: 6.9 KB (6895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e6865a3e5096e25d9be57177db42f935a66f9fa09f1be3e1631dec3afd5d82`  
		Last Modified: Tue, 27 Jul 2021 01:54:38 GMT  
		Size: 113.3 MB (113347832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c67662f3856a170290f7ab939a737d1ea97d30b90fea5a8e88468683fb53159`  
		Last Modified: Tue, 27 Jul 2021 01:54:28 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.12`

```console
$ docker pull bonita@sha256:c437992c1cc00db5f552cbfa1dfdad6f0daa6939e597f966a63b632881d786d1
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
$ docker pull bonita@sha256:32b0d47166ca68736fe0797ac6908cb1aa17970d8c4c28c5374e65c894a47775
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233848935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edded5279ca8e8bd58eea6c07ee43a8ce9fde41439b2e28411445343ce7e6fd6`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Mon, 26 Jul 2021 23:12:31 GMT
ADD file:2e6f05bbffb47b3ea8e5e4127452e80debc89fb9e22af2dc5c735ea579adad64 in / 
# Mon, 26 Jul 2021 23:12:34 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:48:05 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 27 Jul 2021 01:49:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:50:07 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 27 Jul 2021 01:50:15 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 27 Jul 2021 01:50:23 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 27 Jul 2021 01:50:25 GMT
ARG BONITA_VERSION
# Tue, 27 Jul 2021 01:51:49 GMT
ARG BRANDING_VERSION
# Tue, 27 Jul 2021 01:51:51 GMT
ARG BONITA_SHA256
# Tue, 27 Jul 2021 01:51:53 GMT
ARG BASE_URL
# Tue, 27 Jul 2021 01:51:58 GMT
ARG BONITA_URL
# Tue, 27 Jul 2021 01:52:00 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 27 Jul 2021 01:52:02 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 27 Jul 2021 01:52:06 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 27 Jul 2021 01:52:09 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 27 Jul 2021 01:52:12 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 27 Jul 2021 01:52:13 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 27 Jul 2021 01:52:16 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 27 Jul 2021 01:52:20 GMT
RUN mkdir /opt/files
# Tue, 27 Jul 2021 01:52:21 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 27 Jul 2021 01:52:31 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 27 Jul 2021 01:52:41 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 27 Jul 2021 01:52:50 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 27 Jul 2021 01:52:53 GMT
VOLUME [/opt/bonita]
# Tue, 27 Jul 2021 01:52:56 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 27 Jul 2021 01:53:03 GMT
EXPOSE 8080
# Tue, 27 Jul 2021 01:53:10 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:3c742a0b2a0025420dcf1bc91d81de2ffb292328fad483ce715521d725503b66`  
		Last Modified: Mon, 26 Jul 2021 23:15:30 GMT  
		Size: 30.4 MB (30437958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122e38cf8ca67c15cafbfb79b10cc63db576f58b99dc6263f8f559ece480fc98`  
		Last Modified: Tue, 27 Jul 2021 01:54:51 GMT  
		Size: 86.4 MB (86437995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0a3a3c9c04402a88e8ea2b6d49b056fcf131a881d2edadaace8b0210815457`  
		Last Modified: Tue, 27 Jul 2021 01:54:32 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fefdc9fcd6ac38c5ffba630155d3fe6932b659a42bf83468548e79583d7537b`  
		Last Modified: Tue, 27 Jul 2021 01:54:32 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a7810bc793a156fe6f7ab91a2bda750971a3a25fc51b31bede2b04fcac68f7`  
		Last Modified: Tue, 27 Jul 2021 01:54:29 GMT  
		Size: 546.7 KB (546729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562af50260f536c102631c3e00af1641a5ef89b02d7eeb8b4f175ac07047b7b0`  
		Last Modified: Tue, 27 Jul 2021 01:55:03 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4549b34b465cf2aa005e75cd1344237ede2babc3e6c848ce3a94d85cb7aec0`  
		Last Modified: Tue, 27 Jul 2021 01:55:03 GMT  
		Size: 6.9 KB (6949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d1515dc066d8f53657c19bdf13096ba8d63b29f80bb948a9e9584ed676ceea5`  
		Last Modified: Tue, 27 Jul 2021 01:55:11 GMT  
		Size: 116.4 MB (116415406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f22fe0852be4639aef4dddb02e14e1edce7a98c01793e260a099ec9455b957`  
		Last Modified: Tue, 27 Jul 2021 01:55:03 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.12.1`

```console
$ docker pull bonita@sha256:c437992c1cc00db5f552cbfa1dfdad6f0daa6939e597f966a63b632881d786d1
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
$ docker pull bonita@sha256:32b0d47166ca68736fe0797ac6908cb1aa17970d8c4c28c5374e65c894a47775
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233848935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edded5279ca8e8bd58eea6c07ee43a8ce9fde41439b2e28411445343ce7e6fd6`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Mon, 26 Jul 2021 23:12:31 GMT
ADD file:2e6f05bbffb47b3ea8e5e4127452e80debc89fb9e22af2dc5c735ea579adad64 in / 
# Mon, 26 Jul 2021 23:12:34 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:48:05 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 27 Jul 2021 01:49:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:50:07 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 27 Jul 2021 01:50:15 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 27 Jul 2021 01:50:23 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 27 Jul 2021 01:50:25 GMT
ARG BONITA_VERSION
# Tue, 27 Jul 2021 01:51:49 GMT
ARG BRANDING_VERSION
# Tue, 27 Jul 2021 01:51:51 GMT
ARG BONITA_SHA256
# Tue, 27 Jul 2021 01:51:53 GMT
ARG BASE_URL
# Tue, 27 Jul 2021 01:51:58 GMT
ARG BONITA_URL
# Tue, 27 Jul 2021 01:52:00 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 27 Jul 2021 01:52:02 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 27 Jul 2021 01:52:06 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 27 Jul 2021 01:52:09 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 27 Jul 2021 01:52:12 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 27 Jul 2021 01:52:13 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 27 Jul 2021 01:52:16 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 27 Jul 2021 01:52:20 GMT
RUN mkdir /opt/files
# Tue, 27 Jul 2021 01:52:21 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 27 Jul 2021 01:52:31 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 27 Jul 2021 01:52:41 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 27 Jul 2021 01:52:50 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 27 Jul 2021 01:52:53 GMT
VOLUME [/opt/bonita]
# Tue, 27 Jul 2021 01:52:56 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 27 Jul 2021 01:53:03 GMT
EXPOSE 8080
# Tue, 27 Jul 2021 01:53:10 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:3c742a0b2a0025420dcf1bc91d81de2ffb292328fad483ce715521d725503b66`  
		Last Modified: Mon, 26 Jul 2021 23:15:30 GMT  
		Size: 30.4 MB (30437958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122e38cf8ca67c15cafbfb79b10cc63db576f58b99dc6263f8f559ece480fc98`  
		Last Modified: Tue, 27 Jul 2021 01:54:51 GMT  
		Size: 86.4 MB (86437995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0a3a3c9c04402a88e8ea2b6d49b056fcf131a881d2edadaace8b0210815457`  
		Last Modified: Tue, 27 Jul 2021 01:54:32 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fefdc9fcd6ac38c5ffba630155d3fe6932b659a42bf83468548e79583d7537b`  
		Last Modified: Tue, 27 Jul 2021 01:54:32 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a7810bc793a156fe6f7ab91a2bda750971a3a25fc51b31bede2b04fcac68f7`  
		Last Modified: Tue, 27 Jul 2021 01:54:29 GMT  
		Size: 546.7 KB (546729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562af50260f536c102631c3e00af1641a5ef89b02d7eeb8b4f175ac07047b7b0`  
		Last Modified: Tue, 27 Jul 2021 01:55:03 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4549b34b465cf2aa005e75cd1344237ede2babc3e6c848ce3a94d85cb7aec0`  
		Last Modified: Tue, 27 Jul 2021 01:55:03 GMT  
		Size: 6.9 KB (6949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d1515dc066d8f53657c19bdf13096ba8d63b29f80bb948a9e9584ed676ceea5`  
		Last Modified: Tue, 27 Jul 2021 01:55:11 GMT  
		Size: 116.4 MB (116415406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f22fe0852be4639aef4dddb02e14e1edce7a98c01793e260a099ec9455b957`  
		Last Modified: Tue, 27 Jul 2021 01:55:03 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:latest`

```console
$ docker pull bonita@sha256:c437992c1cc00db5f552cbfa1dfdad6f0daa6939e597f966a63b632881d786d1
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
$ docker pull bonita@sha256:32b0d47166ca68736fe0797ac6908cb1aa17970d8c4c28c5374e65c894a47775
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233848935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edded5279ca8e8bd58eea6c07ee43a8ce9fde41439b2e28411445343ce7e6fd6`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Mon, 26 Jul 2021 23:12:31 GMT
ADD file:2e6f05bbffb47b3ea8e5e4127452e80debc89fb9e22af2dc5c735ea579adad64 in / 
# Mon, 26 Jul 2021 23:12:34 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:48:05 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 27 Jul 2021 01:49:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:50:07 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 27 Jul 2021 01:50:15 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 27 Jul 2021 01:50:23 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 27 Jul 2021 01:50:25 GMT
ARG BONITA_VERSION
# Tue, 27 Jul 2021 01:51:49 GMT
ARG BRANDING_VERSION
# Tue, 27 Jul 2021 01:51:51 GMT
ARG BONITA_SHA256
# Tue, 27 Jul 2021 01:51:53 GMT
ARG BASE_URL
# Tue, 27 Jul 2021 01:51:58 GMT
ARG BONITA_URL
# Tue, 27 Jul 2021 01:52:00 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 27 Jul 2021 01:52:02 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 27 Jul 2021 01:52:06 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 27 Jul 2021 01:52:09 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 27 Jul 2021 01:52:12 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 27 Jul 2021 01:52:13 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 27 Jul 2021 01:52:16 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 27 Jul 2021 01:52:20 GMT
RUN mkdir /opt/files
# Tue, 27 Jul 2021 01:52:21 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 27 Jul 2021 01:52:31 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 27 Jul 2021 01:52:41 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 27 Jul 2021 01:52:50 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 27 Jul 2021 01:52:53 GMT
VOLUME [/opt/bonita]
# Tue, 27 Jul 2021 01:52:56 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 27 Jul 2021 01:53:03 GMT
EXPOSE 8080
# Tue, 27 Jul 2021 01:53:10 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:3c742a0b2a0025420dcf1bc91d81de2ffb292328fad483ce715521d725503b66`  
		Last Modified: Mon, 26 Jul 2021 23:15:30 GMT  
		Size: 30.4 MB (30437958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122e38cf8ca67c15cafbfb79b10cc63db576f58b99dc6263f8f559ece480fc98`  
		Last Modified: Tue, 27 Jul 2021 01:54:51 GMT  
		Size: 86.4 MB (86437995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0a3a3c9c04402a88e8ea2b6d49b056fcf131a881d2edadaace8b0210815457`  
		Last Modified: Tue, 27 Jul 2021 01:54:32 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fefdc9fcd6ac38c5ffba630155d3fe6932b659a42bf83468548e79583d7537b`  
		Last Modified: Tue, 27 Jul 2021 01:54:32 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a7810bc793a156fe6f7ab91a2bda750971a3a25fc51b31bede2b04fcac68f7`  
		Last Modified: Tue, 27 Jul 2021 01:54:29 GMT  
		Size: 546.7 KB (546729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562af50260f536c102631c3e00af1641a5ef89b02d7eeb8b4f175ac07047b7b0`  
		Last Modified: Tue, 27 Jul 2021 01:55:03 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4549b34b465cf2aa005e75cd1344237ede2babc3e6c848ce3a94d85cb7aec0`  
		Last Modified: Tue, 27 Jul 2021 01:55:03 GMT  
		Size: 6.9 KB (6949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d1515dc066d8f53657c19bdf13096ba8d63b29f80bb948a9e9584ed676ceea5`  
		Last Modified: Tue, 27 Jul 2021 01:55:11 GMT  
		Size: 116.4 MB (116415406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f22fe0852be4639aef4dddb02e14e1edce7a98c01793e260a099ec9455b957`  
		Last Modified: Tue, 27 Jul 2021 01:55:03 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
