<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `bonita`

-	[`bonita:2021.1`](#bonita20211)
-	[`bonita:2021.2`](#bonita20212)
-	[`bonita:2021.2-u0`](#bonita20212-u0)
-	[`bonita:2022.1`](#bonita20221)
-	[`bonita:2022.1-u0`](#bonita20221-u0)
-	[`bonita:7.11`](#bonita711)
-	[`bonita:7.11.4`](#bonita7114)
-	[`bonita:7.12`](#bonita712)
-	[`bonita:7.12.1`](#bonita7121)
-	[`bonita:7.13`](#bonita713)
-	[`bonita:7.13.0`](#bonita7130)
-	[`bonita:7.14`](#bonita714)
-	[`bonita:7.14.0`](#bonita7140)
-	[`bonita:latest`](#bonitalatest)

## `bonita:2021.1`

```console
$ docker pull bonita@sha256:54c83670f10d0228b43b8429181d0daf3f424e0318ceca3d590e5ab7790cef74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2021.1` - linux; amd64

```console
$ docker pull bonita@sha256:80466a4dccd68109457f43a0e767da10aeb8b583df0d041613865b9bbdb22789
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235158820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:700188edbce5d6a5318a88159ccb7ed86ace381a376089f945abb59004e60b6a`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:18 GMT
ADD file:8b379a8fd96e76d10db6f9ae4e9675de33d227db0431ca2a7ca799119e905e8f in / 
# Thu, 01 Sep 2022 23:46:18 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 02:14:29 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 02 Sep 2022 02:15:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 02:15:40 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 02 Sep 2022 02:15:40 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 02 Sep 2022 02:15:43 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 02 Sep 2022 02:15:43 GMT
ARG BONITA_VERSION
# Fri, 02 Sep 2022 02:15:59 GMT
ARG BRANDING_VERSION
# Fri, 02 Sep 2022 02:15:59 GMT
ARG BONITA_SHA256
# Fri, 02 Sep 2022 02:16:00 GMT
ARG BASE_URL
# Fri, 02 Sep 2022 02:16:00 GMT
ARG BONITA_URL
# Fri, 02 Sep 2022 02:16:00 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 02 Sep 2022 02:16:00 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 02 Sep 2022 02:16:00 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 02 Sep 2022 02:16:00 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 02 Sep 2022 02:16:00 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 02 Sep 2022 02:16:00 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 02 Sep 2022 02:16:01 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 02 Sep 2022 02:16:01 GMT
RUN mkdir /opt/files
# Fri, 02 Sep 2022 02:16:01 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 02 Sep 2022 02:16:09 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 02 Sep 2022 02:16:10 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 02 Sep 2022 02:16:11 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 02 Sep 2022 02:16:11 GMT
VOLUME [/opt/bonita]
# Fri, 02 Sep 2022 02:16:11 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 02 Sep 2022 02:16:12 GMT
EXPOSE 8080
# Fri, 02 Sep 2022 02:16:12 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:dad0f37c70a668d101c86b5c769d452ff29c6d51f811891384cc7da00fce192f`  
		Last Modified: Wed, 31 Aug 2022 06:57:55 GMT  
		Size: 26.7 MB (26710085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750275bcb7bb4912342f140375c1ce92e98b2f9e57412c3cad45f187338866a0`  
		Last Modified: Fri, 02 Sep 2022 02:17:29 GMT  
		Size: 91.5 MB (91516145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df88e187d33eaa5fad41d9def2804b163fb2e585812bacaf52692a53f374f63a`  
		Last Modified: Fri, 02 Sep 2022 02:17:17 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba7ae4fc2b53ab1ed2e277d595661f6603221a735892d88d3a91289786af5e5`  
		Last Modified: Fri, 02 Sep 2022 02:17:17 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e92680bf21b31965cdbc63cba205e2d6d3e3556305e8363212fa92c453ed90fc`  
		Last Modified: Fri, 02 Sep 2022 02:17:15 GMT  
		Size: 506.3 KB (506345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40102bfc49242ccad811ceb6454c2505dded5b8bf2df2b8a30e3daa0d96aeb95`  
		Last Modified: Fri, 02 Sep 2022 02:17:39 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751ee84a8ead9a50e1c4ea24a22bfee22c9f3d86d74a4120f023056e8e35b835`  
		Last Modified: Fri, 02 Sep 2022 02:17:39 GMT  
		Size: 6.9 KB (6943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af39de63888c60952ef624561ab47e86d3dac80a61ce77fd0580719fef3811d3`  
		Last Modified: Fri, 02 Sep 2022 02:17:44 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab9f40f4f42e87e7e1d785aa1d88f94cd5f2612ad526ee7c819545e3f14f5a9`  
		Last Modified: Fri, 02 Sep 2022 02:17:38 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:7ab361015ccf742c9808e14ce5c2ab028dbfb1bad421c6795bcb5fdae34952d5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226598269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c30a614d1db72283c5a882db79ce17c54eb505b86100630ee7af353c98f25c4a`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:43 GMT
ADD file:7002810c3cfdef12d2e13c49037e759257e42f5972f300411294e0239f3bdfe9 in / 
# Tue, 02 Aug 2022 01:18:44 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 17:40:46 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 02 Aug 2022 17:41:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 17:41:12 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 02 Aug 2022 17:41:13 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 02 Aug 2022 17:41:17 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 02 Aug 2022 17:41:17 GMT
ARG BONITA_VERSION
# Tue, 02 Aug 2022 17:41:47 GMT
ARG BRANDING_VERSION
# Tue, 02 Aug 2022 17:41:48 GMT
ARG BONITA_SHA256
# Tue, 02 Aug 2022 17:41:49 GMT
ARG BASE_URL
# Tue, 02 Aug 2022 17:41:50 GMT
ARG BONITA_URL
# Tue, 02 Aug 2022 17:41:51 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 02 Aug 2022 17:41:52 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 02 Aug 2022 17:41:53 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 02 Aug 2022 17:41:54 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 02 Aug 2022 17:41:55 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 02 Aug 2022 17:41:56 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 02 Aug 2022 17:41:57 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 02 Aug 2022 17:41:58 GMT
RUN mkdir /opt/files
# Tue, 02 Aug 2022 17:42:00 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 02 Aug 2022 17:42:05 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 02 Aug 2022 17:42:06 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 02 Aug 2022 17:42:08 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 02 Aug 2022 17:42:08 GMT
VOLUME [/opt/bonita]
# Tue, 02 Aug 2022 17:42:10 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 02 Aug 2022 17:42:10 GMT
EXPOSE 8080
# Tue, 02 Aug 2022 17:42:11 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:d2f2687beb6dd5f04849c57d6d83cabdfa44ec5cc5062369416bff4844045533`  
		Last Modified: Tue, 02 Aug 2022 01:20:09 GMT  
		Size: 23.7 MB (23734714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439589d8fce29b6ddaeaa0d2c2fb68eb16c9f8135829466ddf899922c2c78488`  
		Last Modified: Tue, 02 Aug 2022 17:44:08 GMT  
		Size: 86.0 MB (85961696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca434dad4975c4402f953151563ec4581df90bd8b9f4e3bd670e8fd614ff4b4`  
		Last Modified: Tue, 02 Aug 2022 17:43:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643a53a5b66d93db8abb050b7d143e86ef10bae890206b1365d673172628f9e1`  
		Last Modified: Tue, 02 Aug 2022 17:43:56 GMT  
		Size: 1.9 KB (1858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df8d82da748df549da0b2ede71952a9099c9ee290d5c22dc38ba1e76b34d2b0`  
		Last Modified: Tue, 02 Aug 2022 17:43:54 GMT  
		Size: 475.8 KB (475760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:817f5e764b86512346f24b36dc95ba83759a1899e2a9b045ee3ec06489ba8f86`  
		Last Modified: Tue, 02 Aug 2022 17:44:20 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a0280f786f1176a696f1de7847cb62d4bc218e1f5af961737ccf4f5d1d8b1b`  
		Last Modified: Tue, 02 Aug 2022 17:44:20 GMT  
		Size: 6.9 KB (6917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a6cdcd42d0bf3bf3ef933054227953a11e8579bdad50c64499c65b79a8a5f3c`  
		Last Modified: Tue, 02 Aug 2022 17:44:27 GMT  
		Size: 116.4 MB (116415405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1677b323555e6b1285259ac735523908155d92868b55464a79dd6d0f5489056`  
		Last Modified: Tue, 02 Aug 2022 17:44:20 GMT  
		Size: 1.7 KB (1683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:72a3a370139595ad5b1cfee4ca4000b37e0c7e8cb350cd3e684c12a6f81c7d28
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 MB (234121611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c40efc11de084ca8788a328441d252d10b173c6fc4a6f66f12e6c84b4ad6fde3`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 01 Sep 2022 23:49:38 GMT
ADD file:57b462f3139cb98a97a7020f0d1be33f5beb6500115500a9bfd7aaec39854e35 in / 
# Thu, 01 Sep 2022 23:49:40 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:20:24 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 02 Sep 2022 03:21:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 03:21:59 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 02 Sep 2022 03:22:00 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 02 Sep 2022 03:22:03 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 02 Sep 2022 03:22:04 GMT
ARG BONITA_VERSION
# Fri, 02 Sep 2022 03:22:34 GMT
ARG BRANDING_VERSION
# Fri, 02 Sep 2022 03:22:34 GMT
ARG BONITA_SHA256
# Fri, 02 Sep 2022 03:22:35 GMT
ARG BASE_URL
# Fri, 02 Sep 2022 03:22:35 GMT
ARG BONITA_URL
# Fri, 02 Sep 2022 03:22:35 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 02 Sep 2022 03:22:36 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 02 Sep 2022 03:22:36 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 02 Sep 2022 03:22:36 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 02 Sep 2022 03:22:37 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 02 Sep 2022 03:22:37 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 02 Sep 2022 03:22:38 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 02 Sep 2022 03:22:39 GMT
RUN mkdir /opt/files
# Fri, 02 Sep 2022 03:22:40 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 02 Sep 2022 03:22:47 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 02 Sep 2022 03:22:50 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 02 Sep 2022 03:22:52 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 02 Sep 2022 03:22:52 GMT
VOLUME [/opt/bonita]
# Fri, 02 Sep 2022 03:22:53 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 02 Sep 2022 03:22:53 GMT
EXPOSE 8080
# Fri, 02 Sep 2022 03:22:53 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:c48fbbfad89e07e20864186f593c37c87089700f93ddb1b88e1912f891bf3ae2`  
		Last Modified: Thu, 01 Sep 2022 23:51:47 GMT  
		Size: 30.4 MB (30441333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ce4fcdd76768dd18048cc9949e2796034de05cb93b96eb8572c335d32ba5220`  
		Last Modified: Fri, 02 Sep 2022 03:25:38 GMT  
		Size: 86.8 MB (86778682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb409beb41a1bd79a56853b54c0ad28a5898abf3d56039f8dfdb854210605c1b`  
		Last Modified: Fri, 02 Sep 2022 03:25:19 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd49f3a3257a814e50c93343e18132140cb48901a0f943ceb6faa346598f4eb6`  
		Last Modified: Fri, 02 Sep 2022 03:25:19 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92e1d0a3ef0d8e84a002e7cf01ae2749aad5d62c61cc9506814729de58b184c`  
		Last Modified: Fri, 02 Sep 2022 03:25:17 GMT  
		Size: 475.3 KB (475349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d06067abeddbf2ece6713abd2f2892b8b8e965296c97b65c5057953e6a6b0a`  
		Last Modified: Fri, 02 Sep 2022 03:25:53 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df74992fb091e618086a86c86c3c8dd57b6a7eff06b86b3ce3e8b1f50e71242d`  
		Last Modified: Fri, 02 Sep 2022 03:25:53 GMT  
		Size: 6.9 KB (6943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b0d9f2a6396e8308d1d2f25a67bda00a49eba5fef6b1be8a6594163c1581739`  
		Last Modified: Fri, 02 Sep 2022 03:26:02 GMT  
		Size: 116.4 MB (116415406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2927f5bde3e75489bc62c80a0feb7b9af086898c24c2bf55b5bbc34ccdf9b50`  
		Last Modified: Fri, 02 Sep 2022 03:25:54 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2021.2`

```console
$ docker pull bonita@sha256:5dc6083141bf700ff138405a8574d26e8e3fc46a6f507e5df7cbfe78174528f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2021.2` - linux; amd64

```console
$ docker pull bonita@sha256:0fcaedc7cd7d2d449e1521daae0719061bc544182f86e19801010a58b9b22083
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232890125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ed8d795b04f4b515baf26214386238c18686a6133c4889586e280b36574454e`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:18 GMT
ADD file:8b379a8fd96e76d10db6f9ae4e9675de33d227db0431ca2a7ca799119e905e8f in / 
# Thu, 01 Sep 2022 23:46:18 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 02:14:29 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 02 Sep 2022 02:16:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 02:16:37 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 02 Sep 2022 02:16:38 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 02 Sep 2022 02:16:40 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 02 Sep 2022 02:16:40 GMT
ARG BONITA_VERSION
# Fri, 02 Sep 2022 02:16:40 GMT
ARG BRANDING_VERSION
# Fri, 02 Sep 2022 02:16:40 GMT
ARG BONITA_SHA256
# Fri, 02 Sep 2022 02:16:41 GMT
ARG BASE_URL
# Fri, 02 Sep 2022 02:16:41 GMT
ARG BONITA_URL
# Fri, 02 Sep 2022 02:16:41 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 02 Sep 2022 02:16:41 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 02 Sep 2022 02:16:41 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 02 Sep 2022 02:16:41 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 02 Sep 2022 02:16:41 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 02 Sep 2022 02:16:41 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 02 Sep 2022 02:16:42 GMT
RUN mkdir /opt/files
# Fri, 02 Sep 2022 02:16:42 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 02 Sep 2022 02:16:50 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 02 Sep 2022 02:16:50 GMT
ENV HTTP_API=false
# Fri, 02 Sep 2022 02:16:51 GMT
VOLUME [/opt/bonita]
# Fri, 02 Sep 2022 02:16:51 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 02 Sep 2022 02:16:52 GMT
EXPOSE 8080
# Fri, 02 Sep 2022 02:16:52 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:dad0f37c70a668d101c86b5c769d452ff29c6d51f811891384cc7da00fce192f`  
		Last Modified: Wed, 31 Aug 2022 06:57:55 GMT  
		Size: 26.7 MB (26710085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9445ef9b3d9ad52a0b5a4e858b2e1d94d80bebfec7114bc1adf6346ded1e38`  
		Last Modified: Fri, 02 Sep 2022 02:18:15 GMT  
		Size: 91.5 MB (91514447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dea0b3ab44d01a38452357fdd6077f037b9a1a210877fce8212df9e473fd16a`  
		Last Modified: Fri, 02 Sep 2022 02:18:03 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b704d05598c9451af6b6a27ede5b234ce2e92c4f4c62451c64ce2475fded168`  
		Last Modified: Fri, 02 Sep 2022 02:18:03 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f418ed2c2f8afd7574989781b402f2b0861672417ffe0312f54e7674feac016`  
		Last Modified: Fri, 02 Sep 2022 02:18:01 GMT  
		Size: 930.5 KB (930480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc14393a90491498a80f8d9458f0125e279d1bf05a01d5532004f8e6c340321`  
		Last Modified: Fri, 02 Sep 2022 02:18:01 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec5869629895813d7fbbba7bbe46c767935dac320b3064c0c5afb5901b0f9b2`  
		Last Modified: Fri, 02 Sep 2022 02:18:01 GMT  
		Size: 3.3 KB (3304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98d9b939876d4ac38df1b0365894325f22d98cbc1aa0696984e40852d3583a3`  
		Last Modified: Fri, 02 Sep 2022 02:18:07 GMT  
		Size: 113.7 MB (113727916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:424330bc5909186cdbd05250aa5f010218aa7b4fae540baf4f12c07f0d8f764b`  
		Last Modified: Fri, 02 Sep 2022 02:18:01 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:c5a0992056eef2b9aeb7b9023169b6561f41058f415ed1c9aaaf0de603e18f40
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.3 MB (224290844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01446a7647207db9dcef3a6a688fe82790586b7738d010034ee50b9368c9f7ed`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:43 GMT
ADD file:7002810c3cfdef12d2e13c49037e759257e42f5972f300411294e0239f3bdfe9 in / 
# Tue, 02 Aug 2022 01:18:44 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 17:40:46 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 02 Aug 2022 17:42:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 17:42:42 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 02 Aug 2022 17:42:43 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 02 Aug 2022 17:42:46 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 02 Aug 2022 17:42:47 GMT
ARG BONITA_VERSION
# Tue, 02 Aug 2022 17:42:48 GMT
ARG BRANDING_VERSION
# Tue, 02 Aug 2022 17:42:49 GMT
ARG BONITA_SHA256
# Tue, 02 Aug 2022 17:42:50 GMT
ARG BASE_URL
# Tue, 02 Aug 2022 17:42:51 GMT
ARG BONITA_URL
# Tue, 02 Aug 2022 17:42:52 GMT
ENV BONITA_VERSION=7.13.0
# Tue, 02 Aug 2022 17:42:53 GMT
ENV BRANDING_VERSION=2021.2-u0
# Tue, 02 Aug 2022 17:42:54 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Tue, 02 Aug 2022 17:42:55 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Tue, 02 Aug 2022 17:42:56 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 02 Aug 2022 17:42:57 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Tue, 02 Aug 2022 17:42:58 GMT
RUN mkdir /opt/files
# Tue, 02 Aug 2022 17:43:00 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Tue, 02 Aug 2022 17:43:09 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Tue, 02 Aug 2022 17:43:09 GMT
ENV HTTP_API=false
# Tue, 02 Aug 2022 17:43:11 GMT
VOLUME [/opt/bonita]
# Tue, 02 Aug 2022 17:43:12 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 02 Aug 2022 17:43:12 GMT
EXPOSE 8080
# Tue, 02 Aug 2022 17:43:13 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:d2f2687beb6dd5f04849c57d6d83cabdfa44ec5cc5062369416bff4844045533`  
		Last Modified: Tue, 02 Aug 2022 01:20:09 GMT  
		Size: 23.7 MB (23734714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a1ca2ca8943857085e06d4b425c045a8b3ee3a3d7fe89ac23f84d180773b96`  
		Last Modified: Tue, 02 Aug 2022 17:44:56 GMT  
		Size: 86.0 MB (85961602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a55de22dada9082ec7a3a593b8cd232748af4efcbc59db840905b831b28bf54`  
		Last Modified: Tue, 02 Aug 2022 17:44:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ab2e3ad9bf163d68612b159389317d504561ce353dbbf27cccbad037d50594`  
		Last Modified: Tue, 02 Aug 2022 17:44:45 GMT  
		Size: 1.9 KB (1858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d78327ccb2861bccf31add43c64cff76a765bf0b997b06e3738bb08eef2ef9`  
		Last Modified: Tue, 02 Aug 2022 17:44:43 GMT  
		Size: 859.5 KB (859533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc204ca899ea0a81ff2df00810e1f2367f4473436fb8901e4dde42c4f225aff0`  
		Last Modified: Tue, 02 Aug 2022 17:44:42 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f2f83eeba8861334e02971316a51f87680e6783a18bcd1faa9e88640330733`  
		Last Modified: Tue, 02 Aug 2022 17:44:42 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8bf6c9a5ae30c1986b673c3e50d9b39a0f3971a7e1c2d01efc816afb4149fd0`  
		Last Modified: Tue, 02 Aug 2022 17:45:02 GMT  
		Size: 113.7 MB (113727907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496e82ba59853989856478c938a72a23dce5951e98090ebf251385616cd463fb`  
		Last Modified: Tue, 02 Aug 2022 17:44:42 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2` - linux; ppc64le

```console
$ docker pull bonita@sha256:92909e43f6a5fd7e5cf7739a2763905a127f12b8af5c9871728480b084dd781c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231786962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47e37ee9882ab47d345c5c82d579d84a18a1f752b02f23abee526dc6730443eb`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 01 Sep 2022 23:49:38 GMT
ADD file:57b462f3139cb98a97a7020f0d1be33f5beb6500115500a9bfd7aaec39854e35 in / 
# Thu, 01 Sep 2022 23:49:40 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:20:24 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 02 Sep 2022 03:23:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 03:23:48 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 02 Sep 2022 03:23:50 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 02 Sep 2022 03:23:54 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 02 Sep 2022 03:23:54 GMT
ARG BONITA_VERSION
# Fri, 02 Sep 2022 03:23:55 GMT
ARG BRANDING_VERSION
# Fri, 02 Sep 2022 03:23:56 GMT
ARG BONITA_SHA256
# Fri, 02 Sep 2022 03:23:56 GMT
ARG BASE_URL
# Fri, 02 Sep 2022 03:23:57 GMT
ARG BONITA_URL
# Fri, 02 Sep 2022 03:23:57 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 02 Sep 2022 03:23:57 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 02 Sep 2022 03:23:58 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 02 Sep 2022 03:23:58 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 02 Sep 2022 03:23:58 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 02 Sep 2022 03:23:59 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 02 Sep 2022 03:24:00 GMT
RUN mkdir /opt/files
# Fri, 02 Sep 2022 03:24:00 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 02 Sep 2022 03:24:15 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 02 Sep 2022 03:24:16 GMT
ENV HTTP_API=false
# Fri, 02 Sep 2022 03:24:18 GMT
VOLUME [/opt/bonita]
# Fri, 02 Sep 2022 03:24:18 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 02 Sep 2022 03:24:20 GMT
EXPOSE 8080
# Fri, 02 Sep 2022 03:24:22 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:c48fbbfad89e07e20864186f593c37c87089700f93ddb1b88e1912f891bf3ae2`  
		Last Modified: Thu, 01 Sep 2022 23:51:47 GMT  
		Size: 30.4 MB (30441333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289cd5e43ef82b3c3c3c9b8798aa65297828459a2471b9b72731689fb9f9624a`  
		Last Modified: Fri, 02 Sep 2022 03:26:39 GMT  
		Size: 86.8 MB (86778897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c29dd0edffe90985520d45b1ddb05d088cd4dcacbeae1582f1a2305ea005932c`  
		Last Modified: Fri, 02 Sep 2022 03:26:20 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d34f499c617fc5de08cd30aad45074b5d3ac5aabfb6768085aa357e24414c5`  
		Last Modified: Fri, 02 Sep 2022 03:26:20 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a3072de02ca6ae273b41a6644fcd51761da50caf58489fac1e5360b01c36c7`  
		Last Modified: Fri, 02 Sep 2022 03:26:18 GMT  
		Size: 831.6 KB (831581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee3d9bf0fb81e627ad0ff8325b961526d2ca1430ce7a284d414c521b1ca0aac`  
		Last Modified: Fri, 02 Sep 2022 03:26:17 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e65ff53421a1c28d975c2789a7d0ad6d1a64571285fd736c1c69ce4bb4833514`  
		Last Modified: Fri, 02 Sep 2022 03:26:17 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2322b6dfd2ae67c8d3ad50b82bac21fc0111129094ad3dbfddb0495d223438d`  
		Last Modified: Fri, 02 Sep 2022 03:26:28 GMT  
		Size: 113.7 MB (113727949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8150b5e8c399d031e811be41caf7c0497319e14af8fb501da514ba95d9ca8734`  
		Last Modified: Fri, 02 Sep 2022 03:26:18 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2021.2-u0`

```console
$ docker pull bonita@sha256:5dc6083141bf700ff138405a8574d26e8e3fc46a6f507e5df7cbfe78174528f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2021.2-u0` - linux; amd64

```console
$ docker pull bonita@sha256:0fcaedc7cd7d2d449e1521daae0719061bc544182f86e19801010a58b9b22083
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232890125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ed8d795b04f4b515baf26214386238c18686a6133c4889586e280b36574454e`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:18 GMT
ADD file:8b379a8fd96e76d10db6f9ae4e9675de33d227db0431ca2a7ca799119e905e8f in / 
# Thu, 01 Sep 2022 23:46:18 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 02:14:29 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 02 Sep 2022 02:16:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 02:16:37 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 02 Sep 2022 02:16:38 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 02 Sep 2022 02:16:40 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 02 Sep 2022 02:16:40 GMT
ARG BONITA_VERSION
# Fri, 02 Sep 2022 02:16:40 GMT
ARG BRANDING_VERSION
# Fri, 02 Sep 2022 02:16:40 GMT
ARG BONITA_SHA256
# Fri, 02 Sep 2022 02:16:41 GMT
ARG BASE_URL
# Fri, 02 Sep 2022 02:16:41 GMT
ARG BONITA_URL
# Fri, 02 Sep 2022 02:16:41 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 02 Sep 2022 02:16:41 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 02 Sep 2022 02:16:41 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 02 Sep 2022 02:16:41 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 02 Sep 2022 02:16:41 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 02 Sep 2022 02:16:41 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 02 Sep 2022 02:16:42 GMT
RUN mkdir /opt/files
# Fri, 02 Sep 2022 02:16:42 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 02 Sep 2022 02:16:50 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 02 Sep 2022 02:16:50 GMT
ENV HTTP_API=false
# Fri, 02 Sep 2022 02:16:51 GMT
VOLUME [/opt/bonita]
# Fri, 02 Sep 2022 02:16:51 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 02 Sep 2022 02:16:52 GMT
EXPOSE 8080
# Fri, 02 Sep 2022 02:16:52 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:dad0f37c70a668d101c86b5c769d452ff29c6d51f811891384cc7da00fce192f`  
		Last Modified: Wed, 31 Aug 2022 06:57:55 GMT  
		Size: 26.7 MB (26710085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9445ef9b3d9ad52a0b5a4e858b2e1d94d80bebfec7114bc1adf6346ded1e38`  
		Last Modified: Fri, 02 Sep 2022 02:18:15 GMT  
		Size: 91.5 MB (91514447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dea0b3ab44d01a38452357fdd6077f037b9a1a210877fce8212df9e473fd16a`  
		Last Modified: Fri, 02 Sep 2022 02:18:03 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b704d05598c9451af6b6a27ede5b234ce2e92c4f4c62451c64ce2475fded168`  
		Last Modified: Fri, 02 Sep 2022 02:18:03 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f418ed2c2f8afd7574989781b402f2b0861672417ffe0312f54e7674feac016`  
		Last Modified: Fri, 02 Sep 2022 02:18:01 GMT  
		Size: 930.5 KB (930480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc14393a90491498a80f8d9458f0125e279d1bf05a01d5532004f8e6c340321`  
		Last Modified: Fri, 02 Sep 2022 02:18:01 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec5869629895813d7fbbba7bbe46c767935dac320b3064c0c5afb5901b0f9b2`  
		Last Modified: Fri, 02 Sep 2022 02:18:01 GMT  
		Size: 3.3 KB (3304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98d9b939876d4ac38df1b0365894325f22d98cbc1aa0696984e40852d3583a3`  
		Last Modified: Fri, 02 Sep 2022 02:18:07 GMT  
		Size: 113.7 MB (113727916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:424330bc5909186cdbd05250aa5f010218aa7b4fae540baf4f12c07f0d8f764b`  
		Last Modified: Fri, 02 Sep 2022 02:18:01 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2-u0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:c5a0992056eef2b9aeb7b9023169b6561f41058f415ed1c9aaaf0de603e18f40
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.3 MB (224290844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01446a7647207db9dcef3a6a688fe82790586b7738d010034ee50b9368c9f7ed`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:43 GMT
ADD file:7002810c3cfdef12d2e13c49037e759257e42f5972f300411294e0239f3bdfe9 in / 
# Tue, 02 Aug 2022 01:18:44 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 17:40:46 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 02 Aug 2022 17:42:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 17:42:42 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 02 Aug 2022 17:42:43 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 02 Aug 2022 17:42:46 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 02 Aug 2022 17:42:47 GMT
ARG BONITA_VERSION
# Tue, 02 Aug 2022 17:42:48 GMT
ARG BRANDING_VERSION
# Tue, 02 Aug 2022 17:42:49 GMT
ARG BONITA_SHA256
# Tue, 02 Aug 2022 17:42:50 GMT
ARG BASE_URL
# Tue, 02 Aug 2022 17:42:51 GMT
ARG BONITA_URL
# Tue, 02 Aug 2022 17:42:52 GMT
ENV BONITA_VERSION=7.13.0
# Tue, 02 Aug 2022 17:42:53 GMT
ENV BRANDING_VERSION=2021.2-u0
# Tue, 02 Aug 2022 17:42:54 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Tue, 02 Aug 2022 17:42:55 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Tue, 02 Aug 2022 17:42:56 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 02 Aug 2022 17:42:57 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Tue, 02 Aug 2022 17:42:58 GMT
RUN mkdir /opt/files
# Tue, 02 Aug 2022 17:43:00 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Tue, 02 Aug 2022 17:43:09 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Tue, 02 Aug 2022 17:43:09 GMT
ENV HTTP_API=false
# Tue, 02 Aug 2022 17:43:11 GMT
VOLUME [/opt/bonita]
# Tue, 02 Aug 2022 17:43:12 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 02 Aug 2022 17:43:12 GMT
EXPOSE 8080
# Tue, 02 Aug 2022 17:43:13 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:d2f2687beb6dd5f04849c57d6d83cabdfa44ec5cc5062369416bff4844045533`  
		Last Modified: Tue, 02 Aug 2022 01:20:09 GMT  
		Size: 23.7 MB (23734714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a1ca2ca8943857085e06d4b425c045a8b3ee3a3d7fe89ac23f84d180773b96`  
		Last Modified: Tue, 02 Aug 2022 17:44:56 GMT  
		Size: 86.0 MB (85961602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a55de22dada9082ec7a3a593b8cd232748af4efcbc59db840905b831b28bf54`  
		Last Modified: Tue, 02 Aug 2022 17:44:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ab2e3ad9bf163d68612b159389317d504561ce353dbbf27cccbad037d50594`  
		Last Modified: Tue, 02 Aug 2022 17:44:45 GMT  
		Size: 1.9 KB (1858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d78327ccb2861bccf31add43c64cff76a765bf0b997b06e3738bb08eef2ef9`  
		Last Modified: Tue, 02 Aug 2022 17:44:43 GMT  
		Size: 859.5 KB (859533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc204ca899ea0a81ff2df00810e1f2367f4473436fb8901e4dde42c4f225aff0`  
		Last Modified: Tue, 02 Aug 2022 17:44:42 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f2f83eeba8861334e02971316a51f87680e6783a18bcd1faa9e88640330733`  
		Last Modified: Tue, 02 Aug 2022 17:44:42 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8bf6c9a5ae30c1986b673c3e50d9b39a0f3971a7e1c2d01efc816afb4149fd0`  
		Last Modified: Tue, 02 Aug 2022 17:45:02 GMT  
		Size: 113.7 MB (113727907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496e82ba59853989856478c938a72a23dce5951e98090ebf251385616cd463fb`  
		Last Modified: Tue, 02 Aug 2022 17:44:42 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2-u0` - linux; ppc64le

```console
$ docker pull bonita@sha256:92909e43f6a5fd7e5cf7739a2763905a127f12b8af5c9871728480b084dd781c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231786962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47e37ee9882ab47d345c5c82d579d84a18a1f752b02f23abee526dc6730443eb`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 01 Sep 2022 23:49:38 GMT
ADD file:57b462f3139cb98a97a7020f0d1be33f5beb6500115500a9bfd7aaec39854e35 in / 
# Thu, 01 Sep 2022 23:49:40 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:20:24 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 02 Sep 2022 03:23:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 03:23:48 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 02 Sep 2022 03:23:50 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 02 Sep 2022 03:23:54 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 02 Sep 2022 03:23:54 GMT
ARG BONITA_VERSION
# Fri, 02 Sep 2022 03:23:55 GMT
ARG BRANDING_VERSION
# Fri, 02 Sep 2022 03:23:56 GMT
ARG BONITA_SHA256
# Fri, 02 Sep 2022 03:23:56 GMT
ARG BASE_URL
# Fri, 02 Sep 2022 03:23:57 GMT
ARG BONITA_URL
# Fri, 02 Sep 2022 03:23:57 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 02 Sep 2022 03:23:57 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 02 Sep 2022 03:23:58 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 02 Sep 2022 03:23:58 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 02 Sep 2022 03:23:58 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 02 Sep 2022 03:23:59 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 02 Sep 2022 03:24:00 GMT
RUN mkdir /opt/files
# Fri, 02 Sep 2022 03:24:00 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 02 Sep 2022 03:24:15 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 02 Sep 2022 03:24:16 GMT
ENV HTTP_API=false
# Fri, 02 Sep 2022 03:24:18 GMT
VOLUME [/opt/bonita]
# Fri, 02 Sep 2022 03:24:18 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 02 Sep 2022 03:24:20 GMT
EXPOSE 8080
# Fri, 02 Sep 2022 03:24:22 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:c48fbbfad89e07e20864186f593c37c87089700f93ddb1b88e1912f891bf3ae2`  
		Last Modified: Thu, 01 Sep 2022 23:51:47 GMT  
		Size: 30.4 MB (30441333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289cd5e43ef82b3c3c3c9b8798aa65297828459a2471b9b72731689fb9f9624a`  
		Last Modified: Fri, 02 Sep 2022 03:26:39 GMT  
		Size: 86.8 MB (86778897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c29dd0edffe90985520d45b1ddb05d088cd4dcacbeae1582f1a2305ea005932c`  
		Last Modified: Fri, 02 Sep 2022 03:26:20 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d34f499c617fc5de08cd30aad45074b5d3ac5aabfb6768085aa357e24414c5`  
		Last Modified: Fri, 02 Sep 2022 03:26:20 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a3072de02ca6ae273b41a6644fcd51761da50caf58489fac1e5360b01c36c7`  
		Last Modified: Fri, 02 Sep 2022 03:26:18 GMT  
		Size: 831.6 KB (831581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee3d9bf0fb81e627ad0ff8325b961526d2ca1430ce7a284d414c521b1ca0aac`  
		Last Modified: Fri, 02 Sep 2022 03:26:17 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e65ff53421a1c28d975c2789a7d0ad6d1a64571285fd736c1c69ce4bb4833514`  
		Last Modified: Fri, 02 Sep 2022 03:26:17 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2322b6dfd2ae67c8d3ad50b82bac21fc0111129094ad3dbfddb0495d223438d`  
		Last Modified: Fri, 02 Sep 2022 03:26:28 GMT  
		Size: 113.7 MB (113727949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8150b5e8c399d031e811be41caf7c0497319e14af8fb501da514ba95d9ca8734`  
		Last Modified: Fri, 02 Sep 2022 03:26:18 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2022.1`

```console
$ docker pull bonita@sha256:977f4e8862be31d76a5a463b0238a58fcd4af483ea1c6d6cb1ed75a1447c0d23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2022.1` - linux; amd64

```console
$ docker pull bonita@sha256:08cde8fece645d8b60bc13cf85691f0a092238a270c1a95554fc71714cd25237
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180333152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83b7a73741c772da78e05b71140aeaa6e2838bcfef7277b7af94e3813db00ebb`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:15:43 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 09 Aug 2022 18:15:47 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 09 Aug 2022 18:15:47 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 09 Aug 2022 18:15:48 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BONITA_VERSION
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BRANDING_VERSION
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BONITA_SHA256
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BASE_URL
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BONITA_URL
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 09 Aug 2022 18:15:49 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 09 Aug 2022 18:15:50 GMT
RUN mkdir /opt/files
# Tue, 09 Aug 2022 18:15:50 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 09 Aug 2022 18:16:01 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 09 Aug 2022 18:16:02 GMT
ENV HTTP_API=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 09 Aug 2022 18:16:02 GMT
ENV HTTP_API_PASSWORD=
# Tue, 09 Aug 2022 18:16:02 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 09 Aug 2022 18:16:02 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 09 Aug 2022 18:16:02 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 09 Aug 2022 18:16:03 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 09 Aug 2022 18:16:03 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 09 Aug 2022 18:16:03 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 09 Aug 2022 18:16:03 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 09 Aug 2022 18:16:03 GMT
EXPOSE 8080 9000
# Tue, 09 Aug 2022 18:16:03 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 09 Aug 2022 18:16:03 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e40e66c88000cdcf6a5f303ff471b71908973b42e6d2c853ebafc528c1f58d`  
		Last Modified: Tue, 09 Aug 2022 18:16:38 GMT  
		Size: 60.8 MB (60808791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8517b429307545f8abc13fc0b37faa4607093e758af1d721cd166a9c9d59ec60`  
		Last Modified: Tue, 09 Aug 2022 18:16:29 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a90d8fa310d2a6ea37f38a5d6783134999b8e41a9a6cea96f56c35fef2514e`  
		Last Modified: Tue, 09 Aug 2022 18:16:27 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7082e206c7455f0f4b81da210af350e50379ccb7f4d413868083cb6bd93fb7`  
		Last Modified: Tue, 09 Aug 2022 18:16:27 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1afa20c272a36d9fffe827f8ce399a488ef133030401d5e3892cb8f30b9ab2c7`  
		Last Modified: Tue, 09 Aug 2022 18:16:27 GMT  
		Size: 3.0 KB (3034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9086b05d70c72cfe77142c9829855c34c099504b88df663d5d954537502aef`  
		Last Modified: Tue, 09 Aug 2022 18:16:34 GMT  
		Size: 116.7 MB (116690829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153200db9a09f679584a791a878014d3dcdf52d99869e37107b43db18c4d9cc3`  
		Last Modified: Tue, 09 Aug 2022 18:16:27 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:9659f7730d354083e732097fd3656a47ab26b8c4f2010683fc2fbe6358cd9dad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179546604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30779f62863399675fedee53f8a02f2a0fea94360bde10754580989873e9ef13`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:18:32 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 09 Aug 2022 18:18:36 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 09 Aug 2022 18:18:36 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 09 Aug 2022 18:18:37 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 09 Aug 2022 18:18:38 GMT
ARG BONITA_VERSION
# Tue, 09 Aug 2022 18:18:39 GMT
ARG BRANDING_VERSION
# Tue, 09 Aug 2022 18:18:40 GMT
ARG BONITA_SHA256
# Tue, 09 Aug 2022 18:18:41 GMT
ARG BASE_URL
# Tue, 09 Aug 2022 18:18:42 GMT
ARG BONITA_URL
# Tue, 09 Aug 2022 18:18:43 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 09 Aug 2022 18:18:44 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 09 Aug 2022 18:18:45 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 09 Aug 2022 18:18:46 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 09 Aug 2022 18:18:47 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 09 Aug 2022 18:18:48 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 09 Aug 2022 18:18:49 GMT
RUN mkdir /opt/files
# Tue, 09 Aug 2022 18:18:51 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 09 Aug 2022 18:19:04 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 09 Aug 2022 18:19:05 GMT
ENV HTTP_API=false
# Tue, 09 Aug 2022 18:19:06 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 09 Aug 2022 18:19:07 GMT
ENV HTTP_API_PASSWORD=
# Tue, 09 Aug 2022 18:19:08 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 09 Aug 2022 18:19:09 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 09 Aug 2022 18:19:10 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 09 Aug 2022 18:19:11 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 09 Aug 2022 18:19:12 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 09 Aug 2022 18:19:13 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 09 Aug 2022 18:19:14 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 09 Aug 2022 18:19:15 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 09 Aug 2022 18:19:16 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 09 Aug 2022 18:19:17 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 09 Aug 2022 18:19:19 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 09 Aug 2022 18:19:19 GMT
EXPOSE 8080 9000
# Tue, 09 Aug 2022 18:19:20 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 09 Aug 2022 18:19:21 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc88915541d6f4421b66a886f25f68b9655dc1dee732760c3086d5e8b3304a4a`  
		Last Modified: Tue, 09 Aug 2022 18:20:24 GMT  
		Size: 60.1 MB (60129514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319bc8304739386ec9aab2a1dcd52eb85ca85059ce787cc536f24934bb6907c1`  
		Last Modified: Tue, 09 Aug 2022 18:20:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f5f51932f11b34b80147eec1268be25c87b241a595d18adb836b09480ebee6`  
		Last Modified: Tue, 09 Aug 2022 18:20:13 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec51c34c596f0fcdf1cc75e2c3154642dc1e041ed2d502ad3468cbf5ee7633a`  
		Last Modified: Tue, 09 Aug 2022 18:20:13 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ccaa414eaa82b83c723b3217df9302e719890e1ceacda1452c141980ae6f5d`  
		Last Modified: Tue, 09 Aug 2022 18:20:13 GMT  
		Size: 3.0 KB (3002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:334448ededff63c05c8efe4578487e4b1ad071d95373c4c39515f1c33472d788`  
		Last Modified: Tue, 09 Aug 2022 18:20:17 GMT  
		Size: 116.7 MB (116688789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b61a4040e3817598cff22a8fae45d9f16a5d5f8703e2acef71454e5df2d9889`  
		Last Modified: Tue, 09 Aug 2022 18:20:13 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:905376aad5c6b1828a693ea6913e13ee18e890176d32e306d9f9d015ddd0b228
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176142222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34f7c95b1e8662e1c67b791b144f27360f33bf8c5a12aa9beb134ef618268006`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 09 Aug 2022 17:17:20 GMT
ADD file:be31abb0aba89ed5ff9200736a1c46091abc3845d0e332efd5e5c874ef2c99d1 in / 
# Tue, 09 Aug 2022 17:17:21 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 02:57:05 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 10 Aug 2022 02:57:14 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Wed, 10 Aug 2022 02:57:16 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 10 Aug 2022 02:57:18 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Wed, 10 Aug 2022 02:57:19 GMT
ARG BONITA_VERSION
# Wed, 10 Aug 2022 02:57:19 GMT
ARG BRANDING_VERSION
# Wed, 10 Aug 2022 02:57:19 GMT
ARG BONITA_SHA256
# Wed, 10 Aug 2022 02:57:19 GMT
ARG BASE_URL
# Wed, 10 Aug 2022 02:57:20 GMT
ARG BONITA_URL
# Wed, 10 Aug 2022 02:57:20 GMT
ENV BONITA_VERSION=7.14.0
# Wed, 10 Aug 2022 02:57:20 GMT
ENV BRANDING_VERSION=2022.1-u0
# Wed, 10 Aug 2022 02:57:21 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Wed, 10 Aug 2022 02:57:21 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Wed, 10 Aug 2022 02:57:21 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 10 Aug 2022 02:57:21 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Wed, 10 Aug 2022 02:57:23 GMT
RUN mkdir /opt/files
# Wed, 10 Aug 2022 02:57:23 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Wed, 10 Aug 2022 02:57:37 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Wed, 10 Aug 2022 02:57:39 GMT
ENV HTTP_API=false
# Wed, 10 Aug 2022 02:57:39 GMT
ENV HTTP_API_USERNAME=http-api
# Wed, 10 Aug 2022 02:57:40 GMT
ENV HTTP_API_PASSWORD=
# Wed, 10 Aug 2022 02:57:40 GMT
ENV MONITORING_USERNAME=monitoring
# Wed, 10 Aug 2022 02:57:40 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Wed, 10 Aug 2022 02:57:41 GMT
ENV JMX_REMOTE_ACCESS=false
# Wed, 10 Aug 2022 02:57:41 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Wed, 10 Aug 2022 02:57:42 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Wed, 10 Aug 2022 02:57:42 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Wed, 10 Aug 2022 02:57:42 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Wed, 10 Aug 2022 02:57:43 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Wed, 10 Aug 2022 02:57:43 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Wed, 10 Aug 2022 02:57:44 GMT
ENV HTTP_MAX_THREADS=20
# Wed, 10 Aug 2022 02:57:44 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Wed, 10 Aug 2022 02:57:44 GMT
EXPOSE 8080 9000
# Wed, 10 Aug 2022 02:57:45 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Wed, 10 Aug 2022 02:57:45 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:deb7065b3304c3a9834f31b8a53e8d6089060e9c6522668abd22f1f4d9f52ca7`  
		Last Modified: Tue, 09 Aug 2022 17:18:45 GMT  
		Size: 2.8 MB (2812989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20bd0e6368901462206ecfbedd1db3517fe94f68bc7b57918c328df47fbdbbf3`  
		Last Modified: Wed, 10 Aug 2022 02:58:51 GMT  
		Size: 56.6 MB (56628364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2f41beebf7247171a5b275e0598e9ed16be2ad6ffa16ad4c9c8f036f8800f1`  
		Last Modified: Wed, 10 Aug 2022 02:58:38 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d583bf09d162033ea6a52f524d3142e51ab87f5ce8e1c17c918e8c47527016c`  
		Last Modified: Wed, 10 Aug 2022 02:58:36 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593fae9e149af994c09345a3dcb015f0959fed2dd20e229f5fafea90d08f429b`  
		Last Modified: Wed, 10 Aug 2022 02:58:36 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96057fb9286d4d93de5c991d820e3b03be1923bec7ea58592b8417b9f69368bc`  
		Last Modified: Wed, 10 Aug 2022 02:58:36 GMT  
		Size: 3.0 KB (3032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e77133cc538711ede4f9dda1c5d44ea027f26326760bb0136c00411045f62d0d`  
		Last Modified: Wed, 10 Aug 2022 02:58:47 GMT  
		Size: 116.7 MB (116690853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:933c622a69b13e9df15b3809c6323b98b3a6e697a0ce37025afde53920527a41`  
		Last Modified: Wed, 10 Aug 2022 02:58:36 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2022.1-u0`

```console
$ docker pull bonita@sha256:977f4e8862be31d76a5a463b0238a58fcd4af483ea1c6d6cb1ed75a1447c0d23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2022.1-u0` - linux; amd64

```console
$ docker pull bonita@sha256:08cde8fece645d8b60bc13cf85691f0a092238a270c1a95554fc71714cd25237
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180333152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83b7a73741c772da78e05b71140aeaa6e2838bcfef7277b7af94e3813db00ebb`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:15:43 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 09 Aug 2022 18:15:47 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 09 Aug 2022 18:15:47 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 09 Aug 2022 18:15:48 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BONITA_VERSION
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BRANDING_VERSION
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BONITA_SHA256
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BASE_URL
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BONITA_URL
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 09 Aug 2022 18:15:49 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 09 Aug 2022 18:15:50 GMT
RUN mkdir /opt/files
# Tue, 09 Aug 2022 18:15:50 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 09 Aug 2022 18:16:01 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 09 Aug 2022 18:16:02 GMT
ENV HTTP_API=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 09 Aug 2022 18:16:02 GMT
ENV HTTP_API_PASSWORD=
# Tue, 09 Aug 2022 18:16:02 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 09 Aug 2022 18:16:02 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 09 Aug 2022 18:16:02 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 09 Aug 2022 18:16:03 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 09 Aug 2022 18:16:03 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 09 Aug 2022 18:16:03 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 09 Aug 2022 18:16:03 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 09 Aug 2022 18:16:03 GMT
EXPOSE 8080 9000
# Tue, 09 Aug 2022 18:16:03 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 09 Aug 2022 18:16:03 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e40e66c88000cdcf6a5f303ff471b71908973b42e6d2c853ebafc528c1f58d`  
		Last Modified: Tue, 09 Aug 2022 18:16:38 GMT  
		Size: 60.8 MB (60808791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8517b429307545f8abc13fc0b37faa4607093e758af1d721cd166a9c9d59ec60`  
		Last Modified: Tue, 09 Aug 2022 18:16:29 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a90d8fa310d2a6ea37f38a5d6783134999b8e41a9a6cea96f56c35fef2514e`  
		Last Modified: Tue, 09 Aug 2022 18:16:27 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7082e206c7455f0f4b81da210af350e50379ccb7f4d413868083cb6bd93fb7`  
		Last Modified: Tue, 09 Aug 2022 18:16:27 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1afa20c272a36d9fffe827f8ce399a488ef133030401d5e3892cb8f30b9ab2c7`  
		Last Modified: Tue, 09 Aug 2022 18:16:27 GMT  
		Size: 3.0 KB (3034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9086b05d70c72cfe77142c9829855c34c099504b88df663d5d954537502aef`  
		Last Modified: Tue, 09 Aug 2022 18:16:34 GMT  
		Size: 116.7 MB (116690829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153200db9a09f679584a791a878014d3dcdf52d99869e37107b43db18c4d9cc3`  
		Last Modified: Tue, 09 Aug 2022 18:16:27 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.1-u0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:9659f7730d354083e732097fd3656a47ab26b8c4f2010683fc2fbe6358cd9dad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179546604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30779f62863399675fedee53f8a02f2a0fea94360bde10754580989873e9ef13`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:18:32 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 09 Aug 2022 18:18:36 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 09 Aug 2022 18:18:36 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 09 Aug 2022 18:18:37 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 09 Aug 2022 18:18:38 GMT
ARG BONITA_VERSION
# Tue, 09 Aug 2022 18:18:39 GMT
ARG BRANDING_VERSION
# Tue, 09 Aug 2022 18:18:40 GMT
ARG BONITA_SHA256
# Tue, 09 Aug 2022 18:18:41 GMT
ARG BASE_URL
# Tue, 09 Aug 2022 18:18:42 GMT
ARG BONITA_URL
# Tue, 09 Aug 2022 18:18:43 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 09 Aug 2022 18:18:44 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 09 Aug 2022 18:18:45 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 09 Aug 2022 18:18:46 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 09 Aug 2022 18:18:47 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 09 Aug 2022 18:18:48 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 09 Aug 2022 18:18:49 GMT
RUN mkdir /opt/files
# Tue, 09 Aug 2022 18:18:51 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 09 Aug 2022 18:19:04 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 09 Aug 2022 18:19:05 GMT
ENV HTTP_API=false
# Tue, 09 Aug 2022 18:19:06 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 09 Aug 2022 18:19:07 GMT
ENV HTTP_API_PASSWORD=
# Tue, 09 Aug 2022 18:19:08 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 09 Aug 2022 18:19:09 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 09 Aug 2022 18:19:10 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 09 Aug 2022 18:19:11 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 09 Aug 2022 18:19:12 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 09 Aug 2022 18:19:13 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 09 Aug 2022 18:19:14 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 09 Aug 2022 18:19:15 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 09 Aug 2022 18:19:16 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 09 Aug 2022 18:19:17 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 09 Aug 2022 18:19:19 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 09 Aug 2022 18:19:19 GMT
EXPOSE 8080 9000
# Tue, 09 Aug 2022 18:19:20 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 09 Aug 2022 18:19:21 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc88915541d6f4421b66a886f25f68b9655dc1dee732760c3086d5e8b3304a4a`  
		Last Modified: Tue, 09 Aug 2022 18:20:24 GMT  
		Size: 60.1 MB (60129514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319bc8304739386ec9aab2a1dcd52eb85ca85059ce787cc536f24934bb6907c1`  
		Last Modified: Tue, 09 Aug 2022 18:20:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f5f51932f11b34b80147eec1268be25c87b241a595d18adb836b09480ebee6`  
		Last Modified: Tue, 09 Aug 2022 18:20:13 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec51c34c596f0fcdf1cc75e2c3154642dc1e041ed2d502ad3468cbf5ee7633a`  
		Last Modified: Tue, 09 Aug 2022 18:20:13 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ccaa414eaa82b83c723b3217df9302e719890e1ceacda1452c141980ae6f5d`  
		Last Modified: Tue, 09 Aug 2022 18:20:13 GMT  
		Size: 3.0 KB (3002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:334448ededff63c05c8efe4578487e4b1ad071d95373c4c39515f1c33472d788`  
		Last Modified: Tue, 09 Aug 2022 18:20:17 GMT  
		Size: 116.7 MB (116688789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b61a4040e3817598cff22a8fae45d9f16a5d5f8703e2acef71454e5df2d9889`  
		Last Modified: Tue, 09 Aug 2022 18:20:13 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.1-u0` - linux; ppc64le

```console
$ docker pull bonita@sha256:905376aad5c6b1828a693ea6913e13ee18e890176d32e306d9f9d015ddd0b228
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176142222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34f7c95b1e8662e1c67b791b144f27360f33bf8c5a12aa9beb134ef618268006`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 09 Aug 2022 17:17:20 GMT
ADD file:be31abb0aba89ed5ff9200736a1c46091abc3845d0e332efd5e5c874ef2c99d1 in / 
# Tue, 09 Aug 2022 17:17:21 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 02:57:05 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 10 Aug 2022 02:57:14 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Wed, 10 Aug 2022 02:57:16 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 10 Aug 2022 02:57:18 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Wed, 10 Aug 2022 02:57:19 GMT
ARG BONITA_VERSION
# Wed, 10 Aug 2022 02:57:19 GMT
ARG BRANDING_VERSION
# Wed, 10 Aug 2022 02:57:19 GMT
ARG BONITA_SHA256
# Wed, 10 Aug 2022 02:57:19 GMT
ARG BASE_URL
# Wed, 10 Aug 2022 02:57:20 GMT
ARG BONITA_URL
# Wed, 10 Aug 2022 02:57:20 GMT
ENV BONITA_VERSION=7.14.0
# Wed, 10 Aug 2022 02:57:20 GMT
ENV BRANDING_VERSION=2022.1-u0
# Wed, 10 Aug 2022 02:57:21 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Wed, 10 Aug 2022 02:57:21 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Wed, 10 Aug 2022 02:57:21 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 10 Aug 2022 02:57:21 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Wed, 10 Aug 2022 02:57:23 GMT
RUN mkdir /opt/files
# Wed, 10 Aug 2022 02:57:23 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Wed, 10 Aug 2022 02:57:37 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Wed, 10 Aug 2022 02:57:39 GMT
ENV HTTP_API=false
# Wed, 10 Aug 2022 02:57:39 GMT
ENV HTTP_API_USERNAME=http-api
# Wed, 10 Aug 2022 02:57:40 GMT
ENV HTTP_API_PASSWORD=
# Wed, 10 Aug 2022 02:57:40 GMT
ENV MONITORING_USERNAME=monitoring
# Wed, 10 Aug 2022 02:57:40 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Wed, 10 Aug 2022 02:57:41 GMT
ENV JMX_REMOTE_ACCESS=false
# Wed, 10 Aug 2022 02:57:41 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Wed, 10 Aug 2022 02:57:42 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Wed, 10 Aug 2022 02:57:42 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Wed, 10 Aug 2022 02:57:42 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Wed, 10 Aug 2022 02:57:43 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Wed, 10 Aug 2022 02:57:43 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Wed, 10 Aug 2022 02:57:44 GMT
ENV HTTP_MAX_THREADS=20
# Wed, 10 Aug 2022 02:57:44 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Wed, 10 Aug 2022 02:57:44 GMT
EXPOSE 8080 9000
# Wed, 10 Aug 2022 02:57:45 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Wed, 10 Aug 2022 02:57:45 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:deb7065b3304c3a9834f31b8a53e8d6089060e9c6522668abd22f1f4d9f52ca7`  
		Last Modified: Tue, 09 Aug 2022 17:18:45 GMT  
		Size: 2.8 MB (2812989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20bd0e6368901462206ecfbedd1db3517fe94f68bc7b57918c328df47fbdbbf3`  
		Last Modified: Wed, 10 Aug 2022 02:58:51 GMT  
		Size: 56.6 MB (56628364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2f41beebf7247171a5b275e0598e9ed16be2ad6ffa16ad4c9c8f036f8800f1`  
		Last Modified: Wed, 10 Aug 2022 02:58:38 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d583bf09d162033ea6a52f524d3142e51ab87f5ce8e1c17c918e8c47527016c`  
		Last Modified: Wed, 10 Aug 2022 02:58:36 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593fae9e149af994c09345a3dcb015f0959fed2dd20e229f5fafea90d08f429b`  
		Last Modified: Wed, 10 Aug 2022 02:58:36 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96057fb9286d4d93de5c991d820e3b03be1923bec7ea58592b8417b9f69368bc`  
		Last Modified: Wed, 10 Aug 2022 02:58:36 GMT  
		Size: 3.0 KB (3032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e77133cc538711ede4f9dda1c5d44ea027f26326760bb0136c00411045f62d0d`  
		Last Modified: Wed, 10 Aug 2022 02:58:47 GMT  
		Size: 116.7 MB (116690853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:933c622a69b13e9df15b3809c6323b98b3a6e697a0ce37025afde53920527a41`  
		Last Modified: Wed, 10 Aug 2022 02:58:36 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.11`

```console
$ docker pull bonita@sha256:8b7e5b01c2499bdd78e847dbee075e0869ed859f6dbe14f59b49c031eeaa432d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.11` - linux; amd64

```console
$ docker pull bonita@sha256:9ab7f66305befdd537c14c80a13f05cc5fb4b2f89747ecfc0a1a61a115421fa3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232091195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f56006ad244e189f5c0ba684aad89a49c63f565209eff325896a160221f0b06`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:18 GMT
ADD file:8b379a8fd96e76d10db6f9ae4e9675de33d227db0431ca2a7ca799119e905e8f in / 
# Thu, 01 Sep 2022 23:46:18 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 02:14:29 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 02 Sep 2022 02:15:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 02:15:40 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 02 Sep 2022 02:15:40 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 02 Sep 2022 02:15:43 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 02 Sep 2022 02:15:43 GMT
ARG BONITA_VERSION
# Fri, 02 Sep 2022 02:15:43 GMT
ARG BONITA_SHA256
# Fri, 02 Sep 2022 02:15:43 GMT
ARG BASE_URL
# Fri, 02 Sep 2022 02:15:43 GMT
ARG BONITA_URL
# Fri, 02 Sep 2022 02:15:43 GMT
ENV BONITA_VERSION=7.11.4
# Fri, 02 Sep 2022 02:15:43 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Fri, 02 Sep 2022 02:15:43 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Fri, 02 Sep 2022 02:15:43 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 02 Sep 2022 02:15:44 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Fri, 02 Sep 2022 02:15:44 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 02 Sep 2022 02:15:45 GMT
RUN mkdir /opt/files
# Fri, 02 Sep 2022 02:15:45 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Fri, 02 Sep 2022 02:15:50 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Fri, 02 Sep 2022 02:15:51 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 02 Sep 2022 02:15:53 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 02 Sep 2022 02:15:53 GMT
VOLUME [/opt/bonita]
# Fri, 02 Sep 2022 02:15:53 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 02 Sep 2022 02:15:53 GMT
EXPOSE 8080
# Fri, 02 Sep 2022 02:15:53 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:dad0f37c70a668d101c86b5c769d452ff29c6d51f811891384cc7da00fce192f`  
		Last Modified: Wed, 31 Aug 2022 06:57:55 GMT  
		Size: 26.7 MB (26710085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750275bcb7bb4912342f140375c1ce92e98b2f9e57412c3cad45f187338866a0`  
		Last Modified: Fri, 02 Sep 2022 02:17:29 GMT  
		Size: 91.5 MB (91516145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df88e187d33eaa5fad41d9def2804b163fb2e585812bacaf52692a53f374f63a`  
		Last Modified: Fri, 02 Sep 2022 02:17:17 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba7ae4fc2b53ab1ed2e277d595661f6603221a735892d88d3a91289786af5e5`  
		Last Modified: Fri, 02 Sep 2022 02:17:17 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e92680bf21b31965cdbc63cba205e2d6d3e3556305e8363212fa92c453ed90fc`  
		Last Modified: Fri, 02 Sep 2022 02:17:15 GMT  
		Size: 506.3 KB (506345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a07182a504af2946ede7d68e3620e89fae21afd8c29503dc4c9fa4896469e1c`  
		Last Modified: Fri, 02 Sep 2022 02:17:15 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46baa877a1fb6b95e6a3af854f215b97898ec9c1ad7843cdf25d62cc866e1612`  
		Last Modified: Fri, 02 Sep 2022 02:17:15 GMT  
		Size: 6.9 KB (6897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aecb8824597accfd961ed6b48887db329cce4299aa513291c9f769efb79635f`  
		Last Modified: Fri, 02 Sep 2022 02:17:20 GMT  
		Size: 113.3 MB (113347828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ee456ab2c916ef8e09a301bbfd21903e791c094846305831b0d0c628fa1eeaf`  
		Last Modified: Fri, 02 Sep 2022 02:17:15 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:e8a118dff4de791d93f6c11e94b08c9a1164d7181f64c797acf2d91de067a090
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.5 MB (223530644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646571e35ae1a4d11e8d547c9a5860e82aefbca8adddfea403ef44603cbac11c`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:43 GMT
ADD file:7002810c3cfdef12d2e13c49037e759257e42f5972f300411294e0239f3bdfe9 in / 
# Tue, 02 Aug 2022 01:18:44 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 17:40:46 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 02 Aug 2022 17:41:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 17:41:12 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 02 Aug 2022 17:41:13 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 02 Aug 2022 17:41:17 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 02 Aug 2022 17:41:17 GMT
ARG BONITA_VERSION
# Tue, 02 Aug 2022 17:41:18 GMT
ARG BONITA_SHA256
# Tue, 02 Aug 2022 17:41:19 GMT
ARG BASE_URL
# Tue, 02 Aug 2022 17:41:20 GMT
ARG BONITA_URL
# Tue, 02 Aug 2022 17:41:21 GMT
ENV BONITA_VERSION=7.11.4
# Tue, 02 Aug 2022 17:41:22 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Tue, 02 Aug 2022 17:41:23 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Tue, 02 Aug 2022 17:41:24 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 02 Aug 2022 17:41:25 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Tue, 02 Aug 2022 17:41:26 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 02 Aug 2022 17:41:27 GMT
RUN mkdir /opt/files
# Tue, 02 Aug 2022 17:41:29 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Tue, 02 Aug 2022 17:41:33 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Tue, 02 Aug 2022 17:41:35 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 02 Aug 2022 17:41:36 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 02 Aug 2022 17:41:36 GMT
VOLUME [/opt/bonita]
# Tue, 02 Aug 2022 17:41:38 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 02 Aug 2022 17:41:38 GMT
EXPOSE 8080
# Tue, 02 Aug 2022 17:41:39 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:d2f2687beb6dd5f04849c57d6d83cabdfa44ec5cc5062369416bff4844045533`  
		Last Modified: Tue, 02 Aug 2022 01:20:09 GMT  
		Size: 23.7 MB (23734714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439589d8fce29b6ddaeaa0d2c2fb68eb16c9f8135829466ddf899922c2c78488`  
		Last Modified: Tue, 02 Aug 2022 17:44:08 GMT  
		Size: 86.0 MB (85961696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca434dad4975c4402f953151563ec4581df90bd8b9f4e3bd670e8fd614ff4b4`  
		Last Modified: Tue, 02 Aug 2022 17:43:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643a53a5b66d93db8abb050b7d143e86ef10bae890206b1365d673172628f9e1`  
		Last Modified: Tue, 02 Aug 2022 17:43:56 GMT  
		Size: 1.9 KB (1858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df8d82da748df549da0b2ede71952a9099c9ee290d5c22dc38ba1e76b34d2b0`  
		Last Modified: Tue, 02 Aug 2022 17:43:54 GMT  
		Size: 475.8 KB (475760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad50631eb49c8f19312feae82197b8c84c7acda252a4d27c2ee52deb5531d3cc`  
		Last Modified: Tue, 02 Aug 2022 17:43:54 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03f352bba50f5659567c93213547f0571de628a75a84ffd8ff6d7cc7806fd98`  
		Last Modified: Tue, 02 Aug 2022 17:43:53 GMT  
		Size: 6.9 KB (6867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6320208c13dc7f0655e4ee6d692280f7cabac4e50f1edb8f7243d23813baaf6`  
		Last Modified: Tue, 02 Aug 2022 17:44:00 GMT  
		Size: 113.3 MB (113347829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82cde75c267c8cce58f6c22396d464208efe6533f6ffe92f17cfe14954b72b00`  
		Last Modified: Tue, 02 Aug 2022 17:43:53 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11` - linux; ppc64le

```console
$ docker pull bonita@sha256:ffeee3f5b41708ba2798f68f694e214eea0f14896aa67ee984b62b02798ffca3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.1 MB (231053984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d36fd8e8fcfe5e91bc486fa51710da694a83681909ca108f7a466ad54799bd84`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 01 Sep 2022 23:49:38 GMT
ADD file:57b462f3139cb98a97a7020f0d1be33f5beb6500115500a9bfd7aaec39854e35 in / 
# Thu, 01 Sep 2022 23:49:40 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:20:24 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 02 Sep 2022 03:21:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 03:21:59 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 02 Sep 2022 03:22:00 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 02 Sep 2022 03:22:03 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 02 Sep 2022 03:22:04 GMT
ARG BONITA_VERSION
# Fri, 02 Sep 2022 03:22:04 GMT
ARG BONITA_SHA256
# Fri, 02 Sep 2022 03:22:04 GMT
ARG BASE_URL
# Fri, 02 Sep 2022 03:22:04 GMT
ARG BONITA_URL
# Fri, 02 Sep 2022 03:22:05 GMT
ENV BONITA_VERSION=7.11.4
# Fri, 02 Sep 2022 03:22:05 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Fri, 02 Sep 2022 03:22:05 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Fri, 02 Sep 2022 03:22:05 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 02 Sep 2022 03:22:06 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Fri, 02 Sep 2022 03:22:07 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 02 Sep 2022 03:22:08 GMT
RUN mkdir /opt/files
# Fri, 02 Sep 2022 03:22:08 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Fri, 02 Sep 2022 03:22:21 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Fri, 02 Sep 2022 03:22:24 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 02 Sep 2022 03:22:26 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 02 Sep 2022 03:22:26 GMT
VOLUME [/opt/bonita]
# Fri, 02 Sep 2022 03:22:27 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 02 Sep 2022 03:22:27 GMT
EXPOSE 8080
# Fri, 02 Sep 2022 03:22:27 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:c48fbbfad89e07e20864186f593c37c87089700f93ddb1b88e1912f891bf3ae2`  
		Last Modified: Thu, 01 Sep 2022 23:51:47 GMT  
		Size: 30.4 MB (30441333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ce4fcdd76768dd18048cc9949e2796034de05cb93b96eb8572c335d32ba5220`  
		Last Modified: Fri, 02 Sep 2022 03:25:38 GMT  
		Size: 86.8 MB (86778682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb409beb41a1bd79a56853b54c0ad28a5898abf3d56039f8dfdb854210605c1b`  
		Last Modified: Fri, 02 Sep 2022 03:25:19 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd49f3a3257a814e50c93343e18132140cb48901a0f943ceb6faa346598f4eb6`  
		Last Modified: Fri, 02 Sep 2022 03:25:19 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92e1d0a3ef0d8e84a002e7cf01ae2749aad5d62c61cc9506814729de58b184c`  
		Last Modified: Fri, 02 Sep 2022 03:25:17 GMT  
		Size: 475.3 KB (475349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1fde273c1cc5f6ee003883aeee9b965062ecff0b55e355b842ff0c7cca5839`  
		Last Modified: Fri, 02 Sep 2022 03:25:17 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079b6a9f499c02b73e76c25123439d1f4207629f2b2652d0207a2a9209ebca19`  
		Last Modified: Fri, 02 Sep 2022 03:25:17 GMT  
		Size: 6.9 KB (6892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d59432fef91fb9f934480a2aeb01df127404d3fb2ee5921dbcd345644e6f0dc8`  
		Last Modified: Fri, 02 Sep 2022 03:25:24 GMT  
		Size: 113.3 MB (113347830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9e3abefe84f83c44f044fa3d377a822de41fe376d25e9ec814d406ccafdb16`  
		Last Modified: Fri, 02 Sep 2022 03:25:17 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.11.4`

```console
$ docker pull bonita@sha256:8b7e5b01c2499bdd78e847dbee075e0869ed859f6dbe14f59b49c031eeaa432d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.11.4` - linux; amd64

```console
$ docker pull bonita@sha256:9ab7f66305befdd537c14c80a13f05cc5fb4b2f89747ecfc0a1a61a115421fa3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232091195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f56006ad244e189f5c0ba684aad89a49c63f565209eff325896a160221f0b06`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:18 GMT
ADD file:8b379a8fd96e76d10db6f9ae4e9675de33d227db0431ca2a7ca799119e905e8f in / 
# Thu, 01 Sep 2022 23:46:18 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 02:14:29 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 02 Sep 2022 02:15:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 02:15:40 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 02 Sep 2022 02:15:40 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 02 Sep 2022 02:15:43 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 02 Sep 2022 02:15:43 GMT
ARG BONITA_VERSION
# Fri, 02 Sep 2022 02:15:43 GMT
ARG BONITA_SHA256
# Fri, 02 Sep 2022 02:15:43 GMT
ARG BASE_URL
# Fri, 02 Sep 2022 02:15:43 GMT
ARG BONITA_URL
# Fri, 02 Sep 2022 02:15:43 GMT
ENV BONITA_VERSION=7.11.4
# Fri, 02 Sep 2022 02:15:43 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Fri, 02 Sep 2022 02:15:43 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Fri, 02 Sep 2022 02:15:43 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 02 Sep 2022 02:15:44 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Fri, 02 Sep 2022 02:15:44 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 02 Sep 2022 02:15:45 GMT
RUN mkdir /opt/files
# Fri, 02 Sep 2022 02:15:45 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Fri, 02 Sep 2022 02:15:50 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Fri, 02 Sep 2022 02:15:51 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 02 Sep 2022 02:15:53 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 02 Sep 2022 02:15:53 GMT
VOLUME [/opt/bonita]
# Fri, 02 Sep 2022 02:15:53 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 02 Sep 2022 02:15:53 GMT
EXPOSE 8080
# Fri, 02 Sep 2022 02:15:53 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:dad0f37c70a668d101c86b5c769d452ff29c6d51f811891384cc7da00fce192f`  
		Last Modified: Wed, 31 Aug 2022 06:57:55 GMT  
		Size: 26.7 MB (26710085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750275bcb7bb4912342f140375c1ce92e98b2f9e57412c3cad45f187338866a0`  
		Last Modified: Fri, 02 Sep 2022 02:17:29 GMT  
		Size: 91.5 MB (91516145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df88e187d33eaa5fad41d9def2804b163fb2e585812bacaf52692a53f374f63a`  
		Last Modified: Fri, 02 Sep 2022 02:17:17 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba7ae4fc2b53ab1ed2e277d595661f6603221a735892d88d3a91289786af5e5`  
		Last Modified: Fri, 02 Sep 2022 02:17:17 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e92680bf21b31965cdbc63cba205e2d6d3e3556305e8363212fa92c453ed90fc`  
		Last Modified: Fri, 02 Sep 2022 02:17:15 GMT  
		Size: 506.3 KB (506345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a07182a504af2946ede7d68e3620e89fae21afd8c29503dc4c9fa4896469e1c`  
		Last Modified: Fri, 02 Sep 2022 02:17:15 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46baa877a1fb6b95e6a3af854f215b97898ec9c1ad7843cdf25d62cc866e1612`  
		Last Modified: Fri, 02 Sep 2022 02:17:15 GMT  
		Size: 6.9 KB (6897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aecb8824597accfd961ed6b48887db329cce4299aa513291c9f769efb79635f`  
		Last Modified: Fri, 02 Sep 2022 02:17:20 GMT  
		Size: 113.3 MB (113347828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ee456ab2c916ef8e09a301bbfd21903e791c094846305831b0d0c628fa1eeaf`  
		Last Modified: Fri, 02 Sep 2022 02:17:15 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11.4` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:e8a118dff4de791d93f6c11e94b08c9a1164d7181f64c797acf2d91de067a090
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.5 MB (223530644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646571e35ae1a4d11e8d547c9a5860e82aefbca8adddfea403ef44603cbac11c`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:43 GMT
ADD file:7002810c3cfdef12d2e13c49037e759257e42f5972f300411294e0239f3bdfe9 in / 
# Tue, 02 Aug 2022 01:18:44 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 17:40:46 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 02 Aug 2022 17:41:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 17:41:12 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 02 Aug 2022 17:41:13 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 02 Aug 2022 17:41:17 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 02 Aug 2022 17:41:17 GMT
ARG BONITA_VERSION
# Tue, 02 Aug 2022 17:41:18 GMT
ARG BONITA_SHA256
# Tue, 02 Aug 2022 17:41:19 GMT
ARG BASE_URL
# Tue, 02 Aug 2022 17:41:20 GMT
ARG BONITA_URL
# Tue, 02 Aug 2022 17:41:21 GMT
ENV BONITA_VERSION=7.11.4
# Tue, 02 Aug 2022 17:41:22 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Tue, 02 Aug 2022 17:41:23 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Tue, 02 Aug 2022 17:41:24 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 02 Aug 2022 17:41:25 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Tue, 02 Aug 2022 17:41:26 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 02 Aug 2022 17:41:27 GMT
RUN mkdir /opt/files
# Tue, 02 Aug 2022 17:41:29 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Tue, 02 Aug 2022 17:41:33 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Tue, 02 Aug 2022 17:41:35 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 02 Aug 2022 17:41:36 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 02 Aug 2022 17:41:36 GMT
VOLUME [/opt/bonita]
# Tue, 02 Aug 2022 17:41:38 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 02 Aug 2022 17:41:38 GMT
EXPOSE 8080
# Tue, 02 Aug 2022 17:41:39 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:d2f2687beb6dd5f04849c57d6d83cabdfa44ec5cc5062369416bff4844045533`  
		Last Modified: Tue, 02 Aug 2022 01:20:09 GMT  
		Size: 23.7 MB (23734714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439589d8fce29b6ddaeaa0d2c2fb68eb16c9f8135829466ddf899922c2c78488`  
		Last Modified: Tue, 02 Aug 2022 17:44:08 GMT  
		Size: 86.0 MB (85961696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca434dad4975c4402f953151563ec4581df90bd8b9f4e3bd670e8fd614ff4b4`  
		Last Modified: Tue, 02 Aug 2022 17:43:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643a53a5b66d93db8abb050b7d143e86ef10bae890206b1365d673172628f9e1`  
		Last Modified: Tue, 02 Aug 2022 17:43:56 GMT  
		Size: 1.9 KB (1858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df8d82da748df549da0b2ede71952a9099c9ee290d5c22dc38ba1e76b34d2b0`  
		Last Modified: Tue, 02 Aug 2022 17:43:54 GMT  
		Size: 475.8 KB (475760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad50631eb49c8f19312feae82197b8c84c7acda252a4d27c2ee52deb5531d3cc`  
		Last Modified: Tue, 02 Aug 2022 17:43:54 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03f352bba50f5659567c93213547f0571de628a75a84ffd8ff6d7cc7806fd98`  
		Last Modified: Tue, 02 Aug 2022 17:43:53 GMT  
		Size: 6.9 KB (6867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6320208c13dc7f0655e4ee6d692280f7cabac4e50f1edb8f7243d23813baaf6`  
		Last Modified: Tue, 02 Aug 2022 17:44:00 GMT  
		Size: 113.3 MB (113347829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82cde75c267c8cce58f6c22396d464208efe6533f6ffe92f17cfe14954b72b00`  
		Last Modified: Tue, 02 Aug 2022 17:43:53 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11.4` - linux; ppc64le

```console
$ docker pull bonita@sha256:ffeee3f5b41708ba2798f68f694e214eea0f14896aa67ee984b62b02798ffca3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.1 MB (231053984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d36fd8e8fcfe5e91bc486fa51710da694a83681909ca108f7a466ad54799bd84`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 01 Sep 2022 23:49:38 GMT
ADD file:57b462f3139cb98a97a7020f0d1be33f5beb6500115500a9bfd7aaec39854e35 in / 
# Thu, 01 Sep 2022 23:49:40 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:20:24 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 02 Sep 2022 03:21:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 03:21:59 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 02 Sep 2022 03:22:00 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 02 Sep 2022 03:22:03 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 02 Sep 2022 03:22:04 GMT
ARG BONITA_VERSION
# Fri, 02 Sep 2022 03:22:04 GMT
ARG BONITA_SHA256
# Fri, 02 Sep 2022 03:22:04 GMT
ARG BASE_URL
# Fri, 02 Sep 2022 03:22:04 GMT
ARG BONITA_URL
# Fri, 02 Sep 2022 03:22:05 GMT
ENV BONITA_VERSION=7.11.4
# Fri, 02 Sep 2022 03:22:05 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Fri, 02 Sep 2022 03:22:05 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Fri, 02 Sep 2022 03:22:05 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 02 Sep 2022 03:22:06 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Fri, 02 Sep 2022 03:22:07 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 02 Sep 2022 03:22:08 GMT
RUN mkdir /opt/files
# Fri, 02 Sep 2022 03:22:08 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Fri, 02 Sep 2022 03:22:21 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Fri, 02 Sep 2022 03:22:24 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 02 Sep 2022 03:22:26 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 02 Sep 2022 03:22:26 GMT
VOLUME [/opt/bonita]
# Fri, 02 Sep 2022 03:22:27 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 02 Sep 2022 03:22:27 GMT
EXPOSE 8080
# Fri, 02 Sep 2022 03:22:27 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:c48fbbfad89e07e20864186f593c37c87089700f93ddb1b88e1912f891bf3ae2`  
		Last Modified: Thu, 01 Sep 2022 23:51:47 GMT  
		Size: 30.4 MB (30441333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ce4fcdd76768dd18048cc9949e2796034de05cb93b96eb8572c335d32ba5220`  
		Last Modified: Fri, 02 Sep 2022 03:25:38 GMT  
		Size: 86.8 MB (86778682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb409beb41a1bd79a56853b54c0ad28a5898abf3d56039f8dfdb854210605c1b`  
		Last Modified: Fri, 02 Sep 2022 03:25:19 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd49f3a3257a814e50c93343e18132140cb48901a0f943ceb6faa346598f4eb6`  
		Last Modified: Fri, 02 Sep 2022 03:25:19 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92e1d0a3ef0d8e84a002e7cf01ae2749aad5d62c61cc9506814729de58b184c`  
		Last Modified: Fri, 02 Sep 2022 03:25:17 GMT  
		Size: 475.3 KB (475349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1fde273c1cc5f6ee003883aeee9b965062ecff0b55e355b842ff0c7cca5839`  
		Last Modified: Fri, 02 Sep 2022 03:25:17 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079b6a9f499c02b73e76c25123439d1f4207629f2b2652d0207a2a9209ebca19`  
		Last Modified: Fri, 02 Sep 2022 03:25:17 GMT  
		Size: 6.9 KB (6892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d59432fef91fb9f934480a2aeb01df127404d3fb2ee5921dbcd345644e6f0dc8`  
		Last Modified: Fri, 02 Sep 2022 03:25:24 GMT  
		Size: 113.3 MB (113347830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9e3abefe84f83c44f044fa3d377a822de41fe376d25e9ec814d406ccafdb16`  
		Last Modified: Fri, 02 Sep 2022 03:25:17 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.12`

```console
$ docker pull bonita@sha256:54c83670f10d0228b43b8429181d0daf3f424e0318ceca3d590e5ab7790cef74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.12` - linux; amd64

```console
$ docker pull bonita@sha256:80466a4dccd68109457f43a0e767da10aeb8b583df0d041613865b9bbdb22789
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235158820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:700188edbce5d6a5318a88159ccb7ed86ace381a376089f945abb59004e60b6a`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:18 GMT
ADD file:8b379a8fd96e76d10db6f9ae4e9675de33d227db0431ca2a7ca799119e905e8f in / 
# Thu, 01 Sep 2022 23:46:18 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 02:14:29 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 02 Sep 2022 02:15:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 02:15:40 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 02 Sep 2022 02:15:40 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 02 Sep 2022 02:15:43 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 02 Sep 2022 02:15:43 GMT
ARG BONITA_VERSION
# Fri, 02 Sep 2022 02:15:59 GMT
ARG BRANDING_VERSION
# Fri, 02 Sep 2022 02:15:59 GMT
ARG BONITA_SHA256
# Fri, 02 Sep 2022 02:16:00 GMT
ARG BASE_URL
# Fri, 02 Sep 2022 02:16:00 GMT
ARG BONITA_URL
# Fri, 02 Sep 2022 02:16:00 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 02 Sep 2022 02:16:00 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 02 Sep 2022 02:16:00 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 02 Sep 2022 02:16:00 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 02 Sep 2022 02:16:00 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 02 Sep 2022 02:16:00 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 02 Sep 2022 02:16:01 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 02 Sep 2022 02:16:01 GMT
RUN mkdir /opt/files
# Fri, 02 Sep 2022 02:16:01 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 02 Sep 2022 02:16:09 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 02 Sep 2022 02:16:10 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 02 Sep 2022 02:16:11 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 02 Sep 2022 02:16:11 GMT
VOLUME [/opt/bonita]
# Fri, 02 Sep 2022 02:16:11 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 02 Sep 2022 02:16:12 GMT
EXPOSE 8080
# Fri, 02 Sep 2022 02:16:12 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:dad0f37c70a668d101c86b5c769d452ff29c6d51f811891384cc7da00fce192f`  
		Last Modified: Wed, 31 Aug 2022 06:57:55 GMT  
		Size: 26.7 MB (26710085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750275bcb7bb4912342f140375c1ce92e98b2f9e57412c3cad45f187338866a0`  
		Last Modified: Fri, 02 Sep 2022 02:17:29 GMT  
		Size: 91.5 MB (91516145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df88e187d33eaa5fad41d9def2804b163fb2e585812bacaf52692a53f374f63a`  
		Last Modified: Fri, 02 Sep 2022 02:17:17 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba7ae4fc2b53ab1ed2e277d595661f6603221a735892d88d3a91289786af5e5`  
		Last Modified: Fri, 02 Sep 2022 02:17:17 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e92680bf21b31965cdbc63cba205e2d6d3e3556305e8363212fa92c453ed90fc`  
		Last Modified: Fri, 02 Sep 2022 02:17:15 GMT  
		Size: 506.3 KB (506345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40102bfc49242ccad811ceb6454c2505dded5b8bf2df2b8a30e3daa0d96aeb95`  
		Last Modified: Fri, 02 Sep 2022 02:17:39 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751ee84a8ead9a50e1c4ea24a22bfee22c9f3d86d74a4120f023056e8e35b835`  
		Last Modified: Fri, 02 Sep 2022 02:17:39 GMT  
		Size: 6.9 KB (6943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af39de63888c60952ef624561ab47e86d3dac80a61ce77fd0580719fef3811d3`  
		Last Modified: Fri, 02 Sep 2022 02:17:44 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab9f40f4f42e87e7e1d785aa1d88f94cd5f2612ad526ee7c819545e3f14f5a9`  
		Last Modified: Fri, 02 Sep 2022 02:17:38 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:7ab361015ccf742c9808e14ce5c2ab028dbfb1bad421c6795bcb5fdae34952d5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226598269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c30a614d1db72283c5a882db79ce17c54eb505b86100630ee7af353c98f25c4a`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:43 GMT
ADD file:7002810c3cfdef12d2e13c49037e759257e42f5972f300411294e0239f3bdfe9 in / 
# Tue, 02 Aug 2022 01:18:44 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 17:40:46 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 02 Aug 2022 17:41:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 17:41:12 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 02 Aug 2022 17:41:13 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 02 Aug 2022 17:41:17 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 02 Aug 2022 17:41:17 GMT
ARG BONITA_VERSION
# Tue, 02 Aug 2022 17:41:47 GMT
ARG BRANDING_VERSION
# Tue, 02 Aug 2022 17:41:48 GMT
ARG BONITA_SHA256
# Tue, 02 Aug 2022 17:41:49 GMT
ARG BASE_URL
# Tue, 02 Aug 2022 17:41:50 GMT
ARG BONITA_URL
# Tue, 02 Aug 2022 17:41:51 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 02 Aug 2022 17:41:52 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 02 Aug 2022 17:41:53 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 02 Aug 2022 17:41:54 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 02 Aug 2022 17:41:55 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 02 Aug 2022 17:41:56 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 02 Aug 2022 17:41:57 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 02 Aug 2022 17:41:58 GMT
RUN mkdir /opt/files
# Tue, 02 Aug 2022 17:42:00 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 02 Aug 2022 17:42:05 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 02 Aug 2022 17:42:06 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 02 Aug 2022 17:42:08 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 02 Aug 2022 17:42:08 GMT
VOLUME [/opt/bonita]
# Tue, 02 Aug 2022 17:42:10 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 02 Aug 2022 17:42:10 GMT
EXPOSE 8080
# Tue, 02 Aug 2022 17:42:11 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:d2f2687beb6dd5f04849c57d6d83cabdfa44ec5cc5062369416bff4844045533`  
		Last Modified: Tue, 02 Aug 2022 01:20:09 GMT  
		Size: 23.7 MB (23734714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439589d8fce29b6ddaeaa0d2c2fb68eb16c9f8135829466ddf899922c2c78488`  
		Last Modified: Tue, 02 Aug 2022 17:44:08 GMT  
		Size: 86.0 MB (85961696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca434dad4975c4402f953151563ec4581df90bd8b9f4e3bd670e8fd614ff4b4`  
		Last Modified: Tue, 02 Aug 2022 17:43:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643a53a5b66d93db8abb050b7d143e86ef10bae890206b1365d673172628f9e1`  
		Last Modified: Tue, 02 Aug 2022 17:43:56 GMT  
		Size: 1.9 KB (1858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df8d82da748df549da0b2ede71952a9099c9ee290d5c22dc38ba1e76b34d2b0`  
		Last Modified: Tue, 02 Aug 2022 17:43:54 GMT  
		Size: 475.8 KB (475760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:817f5e764b86512346f24b36dc95ba83759a1899e2a9b045ee3ec06489ba8f86`  
		Last Modified: Tue, 02 Aug 2022 17:44:20 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a0280f786f1176a696f1de7847cb62d4bc218e1f5af961737ccf4f5d1d8b1b`  
		Last Modified: Tue, 02 Aug 2022 17:44:20 GMT  
		Size: 6.9 KB (6917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a6cdcd42d0bf3bf3ef933054227953a11e8579bdad50c64499c65b79a8a5f3c`  
		Last Modified: Tue, 02 Aug 2022 17:44:27 GMT  
		Size: 116.4 MB (116415405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1677b323555e6b1285259ac735523908155d92868b55464a79dd6d0f5489056`  
		Last Modified: Tue, 02 Aug 2022 17:44:20 GMT  
		Size: 1.7 KB (1683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12` - linux; ppc64le

```console
$ docker pull bonita@sha256:72a3a370139595ad5b1cfee4ca4000b37e0c7e8cb350cd3e684c12a6f81c7d28
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 MB (234121611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c40efc11de084ca8788a328441d252d10b173c6fc4a6f66f12e6c84b4ad6fde3`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 01 Sep 2022 23:49:38 GMT
ADD file:57b462f3139cb98a97a7020f0d1be33f5beb6500115500a9bfd7aaec39854e35 in / 
# Thu, 01 Sep 2022 23:49:40 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:20:24 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 02 Sep 2022 03:21:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 03:21:59 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 02 Sep 2022 03:22:00 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 02 Sep 2022 03:22:03 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 02 Sep 2022 03:22:04 GMT
ARG BONITA_VERSION
# Fri, 02 Sep 2022 03:22:34 GMT
ARG BRANDING_VERSION
# Fri, 02 Sep 2022 03:22:34 GMT
ARG BONITA_SHA256
# Fri, 02 Sep 2022 03:22:35 GMT
ARG BASE_URL
# Fri, 02 Sep 2022 03:22:35 GMT
ARG BONITA_URL
# Fri, 02 Sep 2022 03:22:35 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 02 Sep 2022 03:22:36 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 02 Sep 2022 03:22:36 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 02 Sep 2022 03:22:36 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 02 Sep 2022 03:22:37 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 02 Sep 2022 03:22:37 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 02 Sep 2022 03:22:38 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 02 Sep 2022 03:22:39 GMT
RUN mkdir /opt/files
# Fri, 02 Sep 2022 03:22:40 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 02 Sep 2022 03:22:47 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 02 Sep 2022 03:22:50 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 02 Sep 2022 03:22:52 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 02 Sep 2022 03:22:52 GMT
VOLUME [/opt/bonita]
# Fri, 02 Sep 2022 03:22:53 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 02 Sep 2022 03:22:53 GMT
EXPOSE 8080
# Fri, 02 Sep 2022 03:22:53 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:c48fbbfad89e07e20864186f593c37c87089700f93ddb1b88e1912f891bf3ae2`  
		Last Modified: Thu, 01 Sep 2022 23:51:47 GMT  
		Size: 30.4 MB (30441333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ce4fcdd76768dd18048cc9949e2796034de05cb93b96eb8572c335d32ba5220`  
		Last Modified: Fri, 02 Sep 2022 03:25:38 GMT  
		Size: 86.8 MB (86778682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb409beb41a1bd79a56853b54c0ad28a5898abf3d56039f8dfdb854210605c1b`  
		Last Modified: Fri, 02 Sep 2022 03:25:19 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd49f3a3257a814e50c93343e18132140cb48901a0f943ceb6faa346598f4eb6`  
		Last Modified: Fri, 02 Sep 2022 03:25:19 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92e1d0a3ef0d8e84a002e7cf01ae2749aad5d62c61cc9506814729de58b184c`  
		Last Modified: Fri, 02 Sep 2022 03:25:17 GMT  
		Size: 475.3 KB (475349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d06067abeddbf2ece6713abd2f2892b8b8e965296c97b65c5057953e6a6b0a`  
		Last Modified: Fri, 02 Sep 2022 03:25:53 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df74992fb091e618086a86c86c3c8dd57b6a7eff06b86b3ce3e8b1f50e71242d`  
		Last Modified: Fri, 02 Sep 2022 03:25:53 GMT  
		Size: 6.9 KB (6943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b0d9f2a6396e8308d1d2f25a67bda00a49eba5fef6b1be8a6594163c1581739`  
		Last Modified: Fri, 02 Sep 2022 03:26:02 GMT  
		Size: 116.4 MB (116415406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2927f5bde3e75489bc62c80a0feb7b9af086898c24c2bf55b5bbc34ccdf9b50`  
		Last Modified: Fri, 02 Sep 2022 03:25:54 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.12.1`

```console
$ docker pull bonita@sha256:54c83670f10d0228b43b8429181d0daf3f424e0318ceca3d590e5ab7790cef74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.12.1` - linux; amd64

```console
$ docker pull bonita@sha256:80466a4dccd68109457f43a0e767da10aeb8b583df0d041613865b9bbdb22789
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235158820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:700188edbce5d6a5318a88159ccb7ed86ace381a376089f945abb59004e60b6a`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:18 GMT
ADD file:8b379a8fd96e76d10db6f9ae4e9675de33d227db0431ca2a7ca799119e905e8f in / 
# Thu, 01 Sep 2022 23:46:18 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 02:14:29 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 02 Sep 2022 02:15:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 02:15:40 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 02 Sep 2022 02:15:40 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 02 Sep 2022 02:15:43 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 02 Sep 2022 02:15:43 GMT
ARG BONITA_VERSION
# Fri, 02 Sep 2022 02:15:59 GMT
ARG BRANDING_VERSION
# Fri, 02 Sep 2022 02:15:59 GMT
ARG BONITA_SHA256
# Fri, 02 Sep 2022 02:16:00 GMT
ARG BASE_URL
# Fri, 02 Sep 2022 02:16:00 GMT
ARG BONITA_URL
# Fri, 02 Sep 2022 02:16:00 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 02 Sep 2022 02:16:00 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 02 Sep 2022 02:16:00 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 02 Sep 2022 02:16:00 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 02 Sep 2022 02:16:00 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 02 Sep 2022 02:16:00 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 02 Sep 2022 02:16:01 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 02 Sep 2022 02:16:01 GMT
RUN mkdir /opt/files
# Fri, 02 Sep 2022 02:16:01 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 02 Sep 2022 02:16:09 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 02 Sep 2022 02:16:10 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 02 Sep 2022 02:16:11 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 02 Sep 2022 02:16:11 GMT
VOLUME [/opt/bonita]
# Fri, 02 Sep 2022 02:16:11 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 02 Sep 2022 02:16:12 GMT
EXPOSE 8080
# Fri, 02 Sep 2022 02:16:12 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:dad0f37c70a668d101c86b5c769d452ff29c6d51f811891384cc7da00fce192f`  
		Last Modified: Wed, 31 Aug 2022 06:57:55 GMT  
		Size: 26.7 MB (26710085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750275bcb7bb4912342f140375c1ce92e98b2f9e57412c3cad45f187338866a0`  
		Last Modified: Fri, 02 Sep 2022 02:17:29 GMT  
		Size: 91.5 MB (91516145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df88e187d33eaa5fad41d9def2804b163fb2e585812bacaf52692a53f374f63a`  
		Last Modified: Fri, 02 Sep 2022 02:17:17 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba7ae4fc2b53ab1ed2e277d595661f6603221a735892d88d3a91289786af5e5`  
		Last Modified: Fri, 02 Sep 2022 02:17:17 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e92680bf21b31965cdbc63cba205e2d6d3e3556305e8363212fa92c453ed90fc`  
		Last Modified: Fri, 02 Sep 2022 02:17:15 GMT  
		Size: 506.3 KB (506345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40102bfc49242ccad811ceb6454c2505dded5b8bf2df2b8a30e3daa0d96aeb95`  
		Last Modified: Fri, 02 Sep 2022 02:17:39 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751ee84a8ead9a50e1c4ea24a22bfee22c9f3d86d74a4120f023056e8e35b835`  
		Last Modified: Fri, 02 Sep 2022 02:17:39 GMT  
		Size: 6.9 KB (6943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af39de63888c60952ef624561ab47e86d3dac80a61ce77fd0580719fef3811d3`  
		Last Modified: Fri, 02 Sep 2022 02:17:44 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab9f40f4f42e87e7e1d785aa1d88f94cd5f2612ad526ee7c819545e3f14f5a9`  
		Last Modified: Fri, 02 Sep 2022 02:17:38 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:7ab361015ccf742c9808e14ce5c2ab028dbfb1bad421c6795bcb5fdae34952d5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226598269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c30a614d1db72283c5a882db79ce17c54eb505b86100630ee7af353c98f25c4a`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:43 GMT
ADD file:7002810c3cfdef12d2e13c49037e759257e42f5972f300411294e0239f3bdfe9 in / 
# Tue, 02 Aug 2022 01:18:44 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 17:40:46 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 02 Aug 2022 17:41:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 17:41:12 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 02 Aug 2022 17:41:13 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 02 Aug 2022 17:41:17 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 02 Aug 2022 17:41:17 GMT
ARG BONITA_VERSION
# Tue, 02 Aug 2022 17:41:47 GMT
ARG BRANDING_VERSION
# Tue, 02 Aug 2022 17:41:48 GMT
ARG BONITA_SHA256
# Tue, 02 Aug 2022 17:41:49 GMT
ARG BASE_URL
# Tue, 02 Aug 2022 17:41:50 GMT
ARG BONITA_URL
# Tue, 02 Aug 2022 17:41:51 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 02 Aug 2022 17:41:52 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 02 Aug 2022 17:41:53 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 02 Aug 2022 17:41:54 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 02 Aug 2022 17:41:55 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 02 Aug 2022 17:41:56 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 02 Aug 2022 17:41:57 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 02 Aug 2022 17:41:58 GMT
RUN mkdir /opt/files
# Tue, 02 Aug 2022 17:42:00 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 02 Aug 2022 17:42:05 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 02 Aug 2022 17:42:06 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 02 Aug 2022 17:42:08 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 02 Aug 2022 17:42:08 GMT
VOLUME [/opt/bonita]
# Tue, 02 Aug 2022 17:42:10 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 02 Aug 2022 17:42:10 GMT
EXPOSE 8080
# Tue, 02 Aug 2022 17:42:11 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:d2f2687beb6dd5f04849c57d6d83cabdfa44ec5cc5062369416bff4844045533`  
		Last Modified: Tue, 02 Aug 2022 01:20:09 GMT  
		Size: 23.7 MB (23734714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439589d8fce29b6ddaeaa0d2c2fb68eb16c9f8135829466ddf899922c2c78488`  
		Last Modified: Tue, 02 Aug 2022 17:44:08 GMT  
		Size: 86.0 MB (85961696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca434dad4975c4402f953151563ec4581df90bd8b9f4e3bd670e8fd614ff4b4`  
		Last Modified: Tue, 02 Aug 2022 17:43:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643a53a5b66d93db8abb050b7d143e86ef10bae890206b1365d673172628f9e1`  
		Last Modified: Tue, 02 Aug 2022 17:43:56 GMT  
		Size: 1.9 KB (1858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df8d82da748df549da0b2ede71952a9099c9ee290d5c22dc38ba1e76b34d2b0`  
		Last Modified: Tue, 02 Aug 2022 17:43:54 GMT  
		Size: 475.8 KB (475760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:817f5e764b86512346f24b36dc95ba83759a1899e2a9b045ee3ec06489ba8f86`  
		Last Modified: Tue, 02 Aug 2022 17:44:20 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a0280f786f1176a696f1de7847cb62d4bc218e1f5af961737ccf4f5d1d8b1b`  
		Last Modified: Tue, 02 Aug 2022 17:44:20 GMT  
		Size: 6.9 KB (6917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a6cdcd42d0bf3bf3ef933054227953a11e8579bdad50c64499c65b79a8a5f3c`  
		Last Modified: Tue, 02 Aug 2022 17:44:27 GMT  
		Size: 116.4 MB (116415405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1677b323555e6b1285259ac735523908155d92868b55464a79dd6d0f5489056`  
		Last Modified: Tue, 02 Aug 2022 17:44:20 GMT  
		Size: 1.7 KB (1683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:72a3a370139595ad5b1cfee4ca4000b37e0c7e8cb350cd3e684c12a6f81c7d28
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 MB (234121611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c40efc11de084ca8788a328441d252d10b173c6fc4a6f66f12e6c84b4ad6fde3`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 01 Sep 2022 23:49:38 GMT
ADD file:57b462f3139cb98a97a7020f0d1be33f5beb6500115500a9bfd7aaec39854e35 in / 
# Thu, 01 Sep 2022 23:49:40 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:20:24 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 02 Sep 2022 03:21:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 03:21:59 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 02 Sep 2022 03:22:00 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 02 Sep 2022 03:22:03 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 02 Sep 2022 03:22:04 GMT
ARG BONITA_VERSION
# Fri, 02 Sep 2022 03:22:34 GMT
ARG BRANDING_VERSION
# Fri, 02 Sep 2022 03:22:34 GMT
ARG BONITA_SHA256
# Fri, 02 Sep 2022 03:22:35 GMT
ARG BASE_URL
# Fri, 02 Sep 2022 03:22:35 GMT
ARG BONITA_URL
# Fri, 02 Sep 2022 03:22:35 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 02 Sep 2022 03:22:36 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 02 Sep 2022 03:22:36 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 02 Sep 2022 03:22:36 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 02 Sep 2022 03:22:37 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 02 Sep 2022 03:22:37 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 02 Sep 2022 03:22:38 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 02 Sep 2022 03:22:39 GMT
RUN mkdir /opt/files
# Fri, 02 Sep 2022 03:22:40 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 02 Sep 2022 03:22:47 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 02 Sep 2022 03:22:50 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 02 Sep 2022 03:22:52 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 02 Sep 2022 03:22:52 GMT
VOLUME [/opt/bonita]
# Fri, 02 Sep 2022 03:22:53 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 02 Sep 2022 03:22:53 GMT
EXPOSE 8080
# Fri, 02 Sep 2022 03:22:53 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:c48fbbfad89e07e20864186f593c37c87089700f93ddb1b88e1912f891bf3ae2`  
		Last Modified: Thu, 01 Sep 2022 23:51:47 GMT  
		Size: 30.4 MB (30441333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ce4fcdd76768dd18048cc9949e2796034de05cb93b96eb8572c335d32ba5220`  
		Last Modified: Fri, 02 Sep 2022 03:25:38 GMT  
		Size: 86.8 MB (86778682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb409beb41a1bd79a56853b54c0ad28a5898abf3d56039f8dfdb854210605c1b`  
		Last Modified: Fri, 02 Sep 2022 03:25:19 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd49f3a3257a814e50c93343e18132140cb48901a0f943ceb6faa346598f4eb6`  
		Last Modified: Fri, 02 Sep 2022 03:25:19 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92e1d0a3ef0d8e84a002e7cf01ae2749aad5d62c61cc9506814729de58b184c`  
		Last Modified: Fri, 02 Sep 2022 03:25:17 GMT  
		Size: 475.3 KB (475349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d06067abeddbf2ece6713abd2f2892b8b8e965296c97b65c5057953e6a6b0a`  
		Last Modified: Fri, 02 Sep 2022 03:25:53 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df74992fb091e618086a86c86c3c8dd57b6a7eff06b86b3ce3e8b1f50e71242d`  
		Last Modified: Fri, 02 Sep 2022 03:25:53 GMT  
		Size: 6.9 KB (6943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b0d9f2a6396e8308d1d2f25a67bda00a49eba5fef6b1be8a6594163c1581739`  
		Last Modified: Fri, 02 Sep 2022 03:26:02 GMT  
		Size: 116.4 MB (116415406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2927f5bde3e75489bc62c80a0feb7b9af086898c24c2bf55b5bbc34ccdf9b50`  
		Last Modified: Fri, 02 Sep 2022 03:25:54 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.13`

```console
$ docker pull bonita@sha256:5dc6083141bf700ff138405a8574d26e8e3fc46a6f507e5df7cbfe78174528f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.13` - linux; amd64

```console
$ docker pull bonita@sha256:0fcaedc7cd7d2d449e1521daae0719061bc544182f86e19801010a58b9b22083
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232890125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ed8d795b04f4b515baf26214386238c18686a6133c4889586e280b36574454e`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:18 GMT
ADD file:8b379a8fd96e76d10db6f9ae4e9675de33d227db0431ca2a7ca799119e905e8f in / 
# Thu, 01 Sep 2022 23:46:18 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 02:14:29 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 02 Sep 2022 02:16:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 02:16:37 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 02 Sep 2022 02:16:38 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 02 Sep 2022 02:16:40 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 02 Sep 2022 02:16:40 GMT
ARG BONITA_VERSION
# Fri, 02 Sep 2022 02:16:40 GMT
ARG BRANDING_VERSION
# Fri, 02 Sep 2022 02:16:40 GMT
ARG BONITA_SHA256
# Fri, 02 Sep 2022 02:16:41 GMT
ARG BASE_URL
# Fri, 02 Sep 2022 02:16:41 GMT
ARG BONITA_URL
# Fri, 02 Sep 2022 02:16:41 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 02 Sep 2022 02:16:41 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 02 Sep 2022 02:16:41 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 02 Sep 2022 02:16:41 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 02 Sep 2022 02:16:41 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 02 Sep 2022 02:16:41 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 02 Sep 2022 02:16:42 GMT
RUN mkdir /opt/files
# Fri, 02 Sep 2022 02:16:42 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 02 Sep 2022 02:16:50 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 02 Sep 2022 02:16:50 GMT
ENV HTTP_API=false
# Fri, 02 Sep 2022 02:16:51 GMT
VOLUME [/opt/bonita]
# Fri, 02 Sep 2022 02:16:51 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 02 Sep 2022 02:16:52 GMT
EXPOSE 8080
# Fri, 02 Sep 2022 02:16:52 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:dad0f37c70a668d101c86b5c769d452ff29c6d51f811891384cc7da00fce192f`  
		Last Modified: Wed, 31 Aug 2022 06:57:55 GMT  
		Size: 26.7 MB (26710085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9445ef9b3d9ad52a0b5a4e858b2e1d94d80bebfec7114bc1adf6346ded1e38`  
		Last Modified: Fri, 02 Sep 2022 02:18:15 GMT  
		Size: 91.5 MB (91514447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dea0b3ab44d01a38452357fdd6077f037b9a1a210877fce8212df9e473fd16a`  
		Last Modified: Fri, 02 Sep 2022 02:18:03 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b704d05598c9451af6b6a27ede5b234ce2e92c4f4c62451c64ce2475fded168`  
		Last Modified: Fri, 02 Sep 2022 02:18:03 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f418ed2c2f8afd7574989781b402f2b0861672417ffe0312f54e7674feac016`  
		Last Modified: Fri, 02 Sep 2022 02:18:01 GMT  
		Size: 930.5 KB (930480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc14393a90491498a80f8d9458f0125e279d1bf05a01d5532004f8e6c340321`  
		Last Modified: Fri, 02 Sep 2022 02:18:01 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec5869629895813d7fbbba7bbe46c767935dac320b3064c0c5afb5901b0f9b2`  
		Last Modified: Fri, 02 Sep 2022 02:18:01 GMT  
		Size: 3.3 KB (3304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98d9b939876d4ac38df1b0365894325f22d98cbc1aa0696984e40852d3583a3`  
		Last Modified: Fri, 02 Sep 2022 02:18:07 GMT  
		Size: 113.7 MB (113727916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:424330bc5909186cdbd05250aa5f010218aa7b4fae540baf4f12c07f0d8f764b`  
		Last Modified: Fri, 02 Sep 2022 02:18:01 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:c5a0992056eef2b9aeb7b9023169b6561f41058f415ed1c9aaaf0de603e18f40
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.3 MB (224290844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01446a7647207db9dcef3a6a688fe82790586b7738d010034ee50b9368c9f7ed`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:43 GMT
ADD file:7002810c3cfdef12d2e13c49037e759257e42f5972f300411294e0239f3bdfe9 in / 
# Tue, 02 Aug 2022 01:18:44 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 17:40:46 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 02 Aug 2022 17:42:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 17:42:42 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 02 Aug 2022 17:42:43 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 02 Aug 2022 17:42:46 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 02 Aug 2022 17:42:47 GMT
ARG BONITA_VERSION
# Tue, 02 Aug 2022 17:42:48 GMT
ARG BRANDING_VERSION
# Tue, 02 Aug 2022 17:42:49 GMT
ARG BONITA_SHA256
# Tue, 02 Aug 2022 17:42:50 GMT
ARG BASE_URL
# Tue, 02 Aug 2022 17:42:51 GMT
ARG BONITA_URL
# Tue, 02 Aug 2022 17:42:52 GMT
ENV BONITA_VERSION=7.13.0
# Tue, 02 Aug 2022 17:42:53 GMT
ENV BRANDING_VERSION=2021.2-u0
# Tue, 02 Aug 2022 17:42:54 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Tue, 02 Aug 2022 17:42:55 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Tue, 02 Aug 2022 17:42:56 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 02 Aug 2022 17:42:57 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Tue, 02 Aug 2022 17:42:58 GMT
RUN mkdir /opt/files
# Tue, 02 Aug 2022 17:43:00 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Tue, 02 Aug 2022 17:43:09 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Tue, 02 Aug 2022 17:43:09 GMT
ENV HTTP_API=false
# Tue, 02 Aug 2022 17:43:11 GMT
VOLUME [/opt/bonita]
# Tue, 02 Aug 2022 17:43:12 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 02 Aug 2022 17:43:12 GMT
EXPOSE 8080
# Tue, 02 Aug 2022 17:43:13 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:d2f2687beb6dd5f04849c57d6d83cabdfa44ec5cc5062369416bff4844045533`  
		Last Modified: Tue, 02 Aug 2022 01:20:09 GMT  
		Size: 23.7 MB (23734714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a1ca2ca8943857085e06d4b425c045a8b3ee3a3d7fe89ac23f84d180773b96`  
		Last Modified: Tue, 02 Aug 2022 17:44:56 GMT  
		Size: 86.0 MB (85961602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a55de22dada9082ec7a3a593b8cd232748af4efcbc59db840905b831b28bf54`  
		Last Modified: Tue, 02 Aug 2022 17:44:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ab2e3ad9bf163d68612b159389317d504561ce353dbbf27cccbad037d50594`  
		Last Modified: Tue, 02 Aug 2022 17:44:45 GMT  
		Size: 1.9 KB (1858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d78327ccb2861bccf31add43c64cff76a765bf0b997b06e3738bb08eef2ef9`  
		Last Modified: Tue, 02 Aug 2022 17:44:43 GMT  
		Size: 859.5 KB (859533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc204ca899ea0a81ff2df00810e1f2367f4473436fb8901e4dde42c4f225aff0`  
		Last Modified: Tue, 02 Aug 2022 17:44:42 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f2f83eeba8861334e02971316a51f87680e6783a18bcd1faa9e88640330733`  
		Last Modified: Tue, 02 Aug 2022 17:44:42 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8bf6c9a5ae30c1986b673c3e50d9b39a0f3971a7e1c2d01efc816afb4149fd0`  
		Last Modified: Tue, 02 Aug 2022 17:45:02 GMT  
		Size: 113.7 MB (113727907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496e82ba59853989856478c938a72a23dce5951e98090ebf251385616cd463fb`  
		Last Modified: Tue, 02 Aug 2022 17:44:42 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13` - linux; ppc64le

```console
$ docker pull bonita@sha256:92909e43f6a5fd7e5cf7739a2763905a127f12b8af5c9871728480b084dd781c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231786962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47e37ee9882ab47d345c5c82d579d84a18a1f752b02f23abee526dc6730443eb`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 01 Sep 2022 23:49:38 GMT
ADD file:57b462f3139cb98a97a7020f0d1be33f5beb6500115500a9bfd7aaec39854e35 in / 
# Thu, 01 Sep 2022 23:49:40 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:20:24 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 02 Sep 2022 03:23:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 03:23:48 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 02 Sep 2022 03:23:50 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 02 Sep 2022 03:23:54 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 02 Sep 2022 03:23:54 GMT
ARG BONITA_VERSION
# Fri, 02 Sep 2022 03:23:55 GMT
ARG BRANDING_VERSION
# Fri, 02 Sep 2022 03:23:56 GMT
ARG BONITA_SHA256
# Fri, 02 Sep 2022 03:23:56 GMT
ARG BASE_URL
# Fri, 02 Sep 2022 03:23:57 GMT
ARG BONITA_URL
# Fri, 02 Sep 2022 03:23:57 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 02 Sep 2022 03:23:57 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 02 Sep 2022 03:23:58 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 02 Sep 2022 03:23:58 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 02 Sep 2022 03:23:58 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 02 Sep 2022 03:23:59 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 02 Sep 2022 03:24:00 GMT
RUN mkdir /opt/files
# Fri, 02 Sep 2022 03:24:00 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 02 Sep 2022 03:24:15 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 02 Sep 2022 03:24:16 GMT
ENV HTTP_API=false
# Fri, 02 Sep 2022 03:24:18 GMT
VOLUME [/opt/bonita]
# Fri, 02 Sep 2022 03:24:18 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 02 Sep 2022 03:24:20 GMT
EXPOSE 8080
# Fri, 02 Sep 2022 03:24:22 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:c48fbbfad89e07e20864186f593c37c87089700f93ddb1b88e1912f891bf3ae2`  
		Last Modified: Thu, 01 Sep 2022 23:51:47 GMT  
		Size: 30.4 MB (30441333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289cd5e43ef82b3c3c3c9b8798aa65297828459a2471b9b72731689fb9f9624a`  
		Last Modified: Fri, 02 Sep 2022 03:26:39 GMT  
		Size: 86.8 MB (86778897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c29dd0edffe90985520d45b1ddb05d088cd4dcacbeae1582f1a2305ea005932c`  
		Last Modified: Fri, 02 Sep 2022 03:26:20 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d34f499c617fc5de08cd30aad45074b5d3ac5aabfb6768085aa357e24414c5`  
		Last Modified: Fri, 02 Sep 2022 03:26:20 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a3072de02ca6ae273b41a6644fcd51761da50caf58489fac1e5360b01c36c7`  
		Last Modified: Fri, 02 Sep 2022 03:26:18 GMT  
		Size: 831.6 KB (831581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee3d9bf0fb81e627ad0ff8325b961526d2ca1430ce7a284d414c521b1ca0aac`  
		Last Modified: Fri, 02 Sep 2022 03:26:17 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e65ff53421a1c28d975c2789a7d0ad6d1a64571285fd736c1c69ce4bb4833514`  
		Last Modified: Fri, 02 Sep 2022 03:26:17 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2322b6dfd2ae67c8d3ad50b82bac21fc0111129094ad3dbfddb0495d223438d`  
		Last Modified: Fri, 02 Sep 2022 03:26:28 GMT  
		Size: 113.7 MB (113727949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8150b5e8c399d031e811be41caf7c0497319e14af8fb501da514ba95d9ca8734`  
		Last Modified: Fri, 02 Sep 2022 03:26:18 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.13.0`

```console
$ docker pull bonita@sha256:5dc6083141bf700ff138405a8574d26e8e3fc46a6f507e5df7cbfe78174528f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.13.0` - linux; amd64

```console
$ docker pull bonita@sha256:0fcaedc7cd7d2d449e1521daae0719061bc544182f86e19801010a58b9b22083
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232890125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ed8d795b04f4b515baf26214386238c18686a6133c4889586e280b36574454e`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:18 GMT
ADD file:8b379a8fd96e76d10db6f9ae4e9675de33d227db0431ca2a7ca799119e905e8f in / 
# Thu, 01 Sep 2022 23:46:18 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 02:14:29 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 02 Sep 2022 02:16:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 02:16:37 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 02 Sep 2022 02:16:38 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 02 Sep 2022 02:16:40 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 02 Sep 2022 02:16:40 GMT
ARG BONITA_VERSION
# Fri, 02 Sep 2022 02:16:40 GMT
ARG BRANDING_VERSION
# Fri, 02 Sep 2022 02:16:40 GMT
ARG BONITA_SHA256
# Fri, 02 Sep 2022 02:16:41 GMT
ARG BASE_URL
# Fri, 02 Sep 2022 02:16:41 GMT
ARG BONITA_URL
# Fri, 02 Sep 2022 02:16:41 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 02 Sep 2022 02:16:41 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 02 Sep 2022 02:16:41 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 02 Sep 2022 02:16:41 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 02 Sep 2022 02:16:41 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 02 Sep 2022 02:16:41 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 02 Sep 2022 02:16:42 GMT
RUN mkdir /opt/files
# Fri, 02 Sep 2022 02:16:42 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 02 Sep 2022 02:16:50 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 02 Sep 2022 02:16:50 GMT
ENV HTTP_API=false
# Fri, 02 Sep 2022 02:16:51 GMT
VOLUME [/opt/bonita]
# Fri, 02 Sep 2022 02:16:51 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 02 Sep 2022 02:16:52 GMT
EXPOSE 8080
# Fri, 02 Sep 2022 02:16:52 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:dad0f37c70a668d101c86b5c769d452ff29c6d51f811891384cc7da00fce192f`  
		Last Modified: Wed, 31 Aug 2022 06:57:55 GMT  
		Size: 26.7 MB (26710085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9445ef9b3d9ad52a0b5a4e858b2e1d94d80bebfec7114bc1adf6346ded1e38`  
		Last Modified: Fri, 02 Sep 2022 02:18:15 GMT  
		Size: 91.5 MB (91514447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dea0b3ab44d01a38452357fdd6077f037b9a1a210877fce8212df9e473fd16a`  
		Last Modified: Fri, 02 Sep 2022 02:18:03 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b704d05598c9451af6b6a27ede5b234ce2e92c4f4c62451c64ce2475fded168`  
		Last Modified: Fri, 02 Sep 2022 02:18:03 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f418ed2c2f8afd7574989781b402f2b0861672417ffe0312f54e7674feac016`  
		Last Modified: Fri, 02 Sep 2022 02:18:01 GMT  
		Size: 930.5 KB (930480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc14393a90491498a80f8d9458f0125e279d1bf05a01d5532004f8e6c340321`  
		Last Modified: Fri, 02 Sep 2022 02:18:01 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec5869629895813d7fbbba7bbe46c767935dac320b3064c0c5afb5901b0f9b2`  
		Last Modified: Fri, 02 Sep 2022 02:18:01 GMT  
		Size: 3.3 KB (3304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98d9b939876d4ac38df1b0365894325f22d98cbc1aa0696984e40852d3583a3`  
		Last Modified: Fri, 02 Sep 2022 02:18:07 GMT  
		Size: 113.7 MB (113727916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:424330bc5909186cdbd05250aa5f010218aa7b4fae540baf4f12c07f0d8f764b`  
		Last Modified: Fri, 02 Sep 2022 02:18:01 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:c5a0992056eef2b9aeb7b9023169b6561f41058f415ed1c9aaaf0de603e18f40
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.3 MB (224290844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01446a7647207db9dcef3a6a688fe82790586b7738d010034ee50b9368c9f7ed`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:43 GMT
ADD file:7002810c3cfdef12d2e13c49037e759257e42f5972f300411294e0239f3bdfe9 in / 
# Tue, 02 Aug 2022 01:18:44 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 17:40:46 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 02 Aug 2022 17:42:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 17:42:42 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 02 Aug 2022 17:42:43 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 02 Aug 2022 17:42:46 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 02 Aug 2022 17:42:47 GMT
ARG BONITA_VERSION
# Tue, 02 Aug 2022 17:42:48 GMT
ARG BRANDING_VERSION
# Tue, 02 Aug 2022 17:42:49 GMT
ARG BONITA_SHA256
# Tue, 02 Aug 2022 17:42:50 GMT
ARG BASE_URL
# Tue, 02 Aug 2022 17:42:51 GMT
ARG BONITA_URL
# Tue, 02 Aug 2022 17:42:52 GMT
ENV BONITA_VERSION=7.13.0
# Tue, 02 Aug 2022 17:42:53 GMT
ENV BRANDING_VERSION=2021.2-u0
# Tue, 02 Aug 2022 17:42:54 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Tue, 02 Aug 2022 17:42:55 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Tue, 02 Aug 2022 17:42:56 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 02 Aug 2022 17:42:57 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Tue, 02 Aug 2022 17:42:58 GMT
RUN mkdir /opt/files
# Tue, 02 Aug 2022 17:43:00 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Tue, 02 Aug 2022 17:43:09 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Tue, 02 Aug 2022 17:43:09 GMT
ENV HTTP_API=false
# Tue, 02 Aug 2022 17:43:11 GMT
VOLUME [/opt/bonita]
# Tue, 02 Aug 2022 17:43:12 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 02 Aug 2022 17:43:12 GMT
EXPOSE 8080
# Tue, 02 Aug 2022 17:43:13 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:d2f2687beb6dd5f04849c57d6d83cabdfa44ec5cc5062369416bff4844045533`  
		Last Modified: Tue, 02 Aug 2022 01:20:09 GMT  
		Size: 23.7 MB (23734714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a1ca2ca8943857085e06d4b425c045a8b3ee3a3d7fe89ac23f84d180773b96`  
		Last Modified: Tue, 02 Aug 2022 17:44:56 GMT  
		Size: 86.0 MB (85961602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a55de22dada9082ec7a3a593b8cd232748af4efcbc59db840905b831b28bf54`  
		Last Modified: Tue, 02 Aug 2022 17:44:45 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ab2e3ad9bf163d68612b159389317d504561ce353dbbf27cccbad037d50594`  
		Last Modified: Tue, 02 Aug 2022 17:44:45 GMT  
		Size: 1.9 KB (1858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d78327ccb2861bccf31add43c64cff76a765bf0b997b06e3738bb08eef2ef9`  
		Last Modified: Tue, 02 Aug 2022 17:44:43 GMT  
		Size: 859.5 KB (859533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc204ca899ea0a81ff2df00810e1f2367f4473436fb8901e4dde42c4f225aff0`  
		Last Modified: Tue, 02 Aug 2022 17:44:42 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f2f83eeba8861334e02971316a51f87680e6783a18bcd1faa9e88640330733`  
		Last Modified: Tue, 02 Aug 2022 17:44:42 GMT  
		Size: 3.3 KB (3310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8bf6c9a5ae30c1986b673c3e50d9b39a0f3971a7e1c2d01efc816afb4149fd0`  
		Last Modified: Tue, 02 Aug 2022 17:45:02 GMT  
		Size: 113.7 MB (113727907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496e82ba59853989856478c938a72a23dce5951e98090ebf251385616cd463fb`  
		Last Modified: Tue, 02 Aug 2022 17:44:42 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:92909e43f6a5fd7e5cf7739a2763905a127f12b8af5c9871728480b084dd781c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231786962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47e37ee9882ab47d345c5c82d579d84a18a1f752b02f23abee526dc6730443eb`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 01 Sep 2022 23:49:38 GMT
ADD file:57b462f3139cb98a97a7020f0d1be33f5beb6500115500a9bfd7aaec39854e35 in / 
# Thu, 01 Sep 2022 23:49:40 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:20:24 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 02 Sep 2022 03:23:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 03:23:48 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 02 Sep 2022 03:23:50 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 02 Sep 2022 03:23:54 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 02 Sep 2022 03:23:54 GMT
ARG BONITA_VERSION
# Fri, 02 Sep 2022 03:23:55 GMT
ARG BRANDING_VERSION
# Fri, 02 Sep 2022 03:23:56 GMT
ARG BONITA_SHA256
# Fri, 02 Sep 2022 03:23:56 GMT
ARG BASE_URL
# Fri, 02 Sep 2022 03:23:57 GMT
ARG BONITA_URL
# Fri, 02 Sep 2022 03:23:57 GMT
ENV BONITA_VERSION=7.13.0
# Fri, 02 Sep 2022 03:23:57 GMT
ENV BRANDING_VERSION=2021.2-u0
# Fri, 02 Sep 2022 03:23:58 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Fri, 02 Sep 2022 03:23:58 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Fri, 02 Sep 2022 03:23:58 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 02 Sep 2022 03:23:59 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Fri, 02 Sep 2022 03:24:00 GMT
RUN mkdir /opt/files
# Fri, 02 Sep 2022 03:24:00 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Fri, 02 Sep 2022 03:24:15 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Fri, 02 Sep 2022 03:24:16 GMT
ENV HTTP_API=false
# Fri, 02 Sep 2022 03:24:18 GMT
VOLUME [/opt/bonita]
# Fri, 02 Sep 2022 03:24:18 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 02 Sep 2022 03:24:20 GMT
EXPOSE 8080
# Fri, 02 Sep 2022 03:24:22 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:c48fbbfad89e07e20864186f593c37c87089700f93ddb1b88e1912f891bf3ae2`  
		Last Modified: Thu, 01 Sep 2022 23:51:47 GMT  
		Size: 30.4 MB (30441333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289cd5e43ef82b3c3c3c9b8798aa65297828459a2471b9b72731689fb9f9624a`  
		Last Modified: Fri, 02 Sep 2022 03:26:39 GMT  
		Size: 86.8 MB (86778897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c29dd0edffe90985520d45b1ddb05d088cd4dcacbeae1582f1a2305ea005932c`  
		Last Modified: Fri, 02 Sep 2022 03:26:20 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d34f499c617fc5de08cd30aad45074b5d3ac5aabfb6768085aa357e24414c5`  
		Last Modified: Fri, 02 Sep 2022 03:26:20 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a3072de02ca6ae273b41a6644fcd51761da50caf58489fac1e5360b01c36c7`  
		Last Modified: Fri, 02 Sep 2022 03:26:18 GMT  
		Size: 831.6 KB (831581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee3d9bf0fb81e627ad0ff8325b961526d2ca1430ce7a284d414c521b1ca0aac`  
		Last Modified: Fri, 02 Sep 2022 03:26:17 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e65ff53421a1c28d975c2789a7d0ad6d1a64571285fd736c1c69ce4bb4833514`  
		Last Modified: Fri, 02 Sep 2022 03:26:17 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2322b6dfd2ae67c8d3ad50b82bac21fc0111129094ad3dbfddb0495d223438d`  
		Last Modified: Fri, 02 Sep 2022 03:26:28 GMT  
		Size: 113.7 MB (113727949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8150b5e8c399d031e811be41caf7c0497319e14af8fb501da514ba95d9ca8734`  
		Last Modified: Fri, 02 Sep 2022 03:26:18 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.14`

```console
$ docker pull bonita@sha256:977f4e8862be31d76a5a463b0238a58fcd4af483ea1c6d6cb1ed75a1447c0d23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.14` - linux; amd64

```console
$ docker pull bonita@sha256:08cde8fece645d8b60bc13cf85691f0a092238a270c1a95554fc71714cd25237
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180333152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83b7a73741c772da78e05b71140aeaa6e2838bcfef7277b7af94e3813db00ebb`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:15:43 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 09 Aug 2022 18:15:47 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 09 Aug 2022 18:15:47 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 09 Aug 2022 18:15:48 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BONITA_VERSION
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BRANDING_VERSION
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BONITA_SHA256
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BASE_URL
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BONITA_URL
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 09 Aug 2022 18:15:49 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 09 Aug 2022 18:15:50 GMT
RUN mkdir /opt/files
# Tue, 09 Aug 2022 18:15:50 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 09 Aug 2022 18:16:01 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 09 Aug 2022 18:16:02 GMT
ENV HTTP_API=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 09 Aug 2022 18:16:02 GMT
ENV HTTP_API_PASSWORD=
# Tue, 09 Aug 2022 18:16:02 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 09 Aug 2022 18:16:02 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 09 Aug 2022 18:16:02 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 09 Aug 2022 18:16:03 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 09 Aug 2022 18:16:03 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 09 Aug 2022 18:16:03 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 09 Aug 2022 18:16:03 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 09 Aug 2022 18:16:03 GMT
EXPOSE 8080 9000
# Tue, 09 Aug 2022 18:16:03 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 09 Aug 2022 18:16:03 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e40e66c88000cdcf6a5f303ff471b71908973b42e6d2c853ebafc528c1f58d`  
		Last Modified: Tue, 09 Aug 2022 18:16:38 GMT  
		Size: 60.8 MB (60808791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8517b429307545f8abc13fc0b37faa4607093e758af1d721cd166a9c9d59ec60`  
		Last Modified: Tue, 09 Aug 2022 18:16:29 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a90d8fa310d2a6ea37f38a5d6783134999b8e41a9a6cea96f56c35fef2514e`  
		Last Modified: Tue, 09 Aug 2022 18:16:27 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7082e206c7455f0f4b81da210af350e50379ccb7f4d413868083cb6bd93fb7`  
		Last Modified: Tue, 09 Aug 2022 18:16:27 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1afa20c272a36d9fffe827f8ce399a488ef133030401d5e3892cb8f30b9ab2c7`  
		Last Modified: Tue, 09 Aug 2022 18:16:27 GMT  
		Size: 3.0 KB (3034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9086b05d70c72cfe77142c9829855c34c099504b88df663d5d954537502aef`  
		Last Modified: Tue, 09 Aug 2022 18:16:34 GMT  
		Size: 116.7 MB (116690829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153200db9a09f679584a791a878014d3dcdf52d99869e37107b43db18c4d9cc3`  
		Last Modified: Tue, 09 Aug 2022 18:16:27 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.14` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:9659f7730d354083e732097fd3656a47ab26b8c4f2010683fc2fbe6358cd9dad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179546604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30779f62863399675fedee53f8a02f2a0fea94360bde10754580989873e9ef13`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:18:32 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 09 Aug 2022 18:18:36 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 09 Aug 2022 18:18:36 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 09 Aug 2022 18:18:37 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 09 Aug 2022 18:18:38 GMT
ARG BONITA_VERSION
# Tue, 09 Aug 2022 18:18:39 GMT
ARG BRANDING_VERSION
# Tue, 09 Aug 2022 18:18:40 GMT
ARG BONITA_SHA256
# Tue, 09 Aug 2022 18:18:41 GMT
ARG BASE_URL
# Tue, 09 Aug 2022 18:18:42 GMT
ARG BONITA_URL
# Tue, 09 Aug 2022 18:18:43 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 09 Aug 2022 18:18:44 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 09 Aug 2022 18:18:45 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 09 Aug 2022 18:18:46 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 09 Aug 2022 18:18:47 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 09 Aug 2022 18:18:48 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 09 Aug 2022 18:18:49 GMT
RUN mkdir /opt/files
# Tue, 09 Aug 2022 18:18:51 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 09 Aug 2022 18:19:04 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 09 Aug 2022 18:19:05 GMT
ENV HTTP_API=false
# Tue, 09 Aug 2022 18:19:06 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 09 Aug 2022 18:19:07 GMT
ENV HTTP_API_PASSWORD=
# Tue, 09 Aug 2022 18:19:08 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 09 Aug 2022 18:19:09 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 09 Aug 2022 18:19:10 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 09 Aug 2022 18:19:11 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 09 Aug 2022 18:19:12 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 09 Aug 2022 18:19:13 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 09 Aug 2022 18:19:14 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 09 Aug 2022 18:19:15 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 09 Aug 2022 18:19:16 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 09 Aug 2022 18:19:17 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 09 Aug 2022 18:19:19 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 09 Aug 2022 18:19:19 GMT
EXPOSE 8080 9000
# Tue, 09 Aug 2022 18:19:20 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 09 Aug 2022 18:19:21 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc88915541d6f4421b66a886f25f68b9655dc1dee732760c3086d5e8b3304a4a`  
		Last Modified: Tue, 09 Aug 2022 18:20:24 GMT  
		Size: 60.1 MB (60129514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319bc8304739386ec9aab2a1dcd52eb85ca85059ce787cc536f24934bb6907c1`  
		Last Modified: Tue, 09 Aug 2022 18:20:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f5f51932f11b34b80147eec1268be25c87b241a595d18adb836b09480ebee6`  
		Last Modified: Tue, 09 Aug 2022 18:20:13 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec51c34c596f0fcdf1cc75e2c3154642dc1e041ed2d502ad3468cbf5ee7633a`  
		Last Modified: Tue, 09 Aug 2022 18:20:13 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ccaa414eaa82b83c723b3217df9302e719890e1ceacda1452c141980ae6f5d`  
		Last Modified: Tue, 09 Aug 2022 18:20:13 GMT  
		Size: 3.0 KB (3002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:334448ededff63c05c8efe4578487e4b1ad071d95373c4c39515f1c33472d788`  
		Last Modified: Tue, 09 Aug 2022 18:20:17 GMT  
		Size: 116.7 MB (116688789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b61a4040e3817598cff22a8fae45d9f16a5d5f8703e2acef71454e5df2d9889`  
		Last Modified: Tue, 09 Aug 2022 18:20:13 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.14` - linux; ppc64le

```console
$ docker pull bonita@sha256:905376aad5c6b1828a693ea6913e13ee18e890176d32e306d9f9d015ddd0b228
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176142222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34f7c95b1e8662e1c67b791b144f27360f33bf8c5a12aa9beb134ef618268006`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 09 Aug 2022 17:17:20 GMT
ADD file:be31abb0aba89ed5ff9200736a1c46091abc3845d0e332efd5e5c874ef2c99d1 in / 
# Tue, 09 Aug 2022 17:17:21 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 02:57:05 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 10 Aug 2022 02:57:14 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Wed, 10 Aug 2022 02:57:16 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 10 Aug 2022 02:57:18 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Wed, 10 Aug 2022 02:57:19 GMT
ARG BONITA_VERSION
# Wed, 10 Aug 2022 02:57:19 GMT
ARG BRANDING_VERSION
# Wed, 10 Aug 2022 02:57:19 GMT
ARG BONITA_SHA256
# Wed, 10 Aug 2022 02:57:19 GMT
ARG BASE_URL
# Wed, 10 Aug 2022 02:57:20 GMT
ARG BONITA_URL
# Wed, 10 Aug 2022 02:57:20 GMT
ENV BONITA_VERSION=7.14.0
# Wed, 10 Aug 2022 02:57:20 GMT
ENV BRANDING_VERSION=2022.1-u0
# Wed, 10 Aug 2022 02:57:21 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Wed, 10 Aug 2022 02:57:21 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Wed, 10 Aug 2022 02:57:21 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 10 Aug 2022 02:57:21 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Wed, 10 Aug 2022 02:57:23 GMT
RUN mkdir /opt/files
# Wed, 10 Aug 2022 02:57:23 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Wed, 10 Aug 2022 02:57:37 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Wed, 10 Aug 2022 02:57:39 GMT
ENV HTTP_API=false
# Wed, 10 Aug 2022 02:57:39 GMT
ENV HTTP_API_USERNAME=http-api
# Wed, 10 Aug 2022 02:57:40 GMT
ENV HTTP_API_PASSWORD=
# Wed, 10 Aug 2022 02:57:40 GMT
ENV MONITORING_USERNAME=monitoring
# Wed, 10 Aug 2022 02:57:40 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Wed, 10 Aug 2022 02:57:41 GMT
ENV JMX_REMOTE_ACCESS=false
# Wed, 10 Aug 2022 02:57:41 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Wed, 10 Aug 2022 02:57:42 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Wed, 10 Aug 2022 02:57:42 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Wed, 10 Aug 2022 02:57:42 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Wed, 10 Aug 2022 02:57:43 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Wed, 10 Aug 2022 02:57:43 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Wed, 10 Aug 2022 02:57:44 GMT
ENV HTTP_MAX_THREADS=20
# Wed, 10 Aug 2022 02:57:44 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Wed, 10 Aug 2022 02:57:44 GMT
EXPOSE 8080 9000
# Wed, 10 Aug 2022 02:57:45 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Wed, 10 Aug 2022 02:57:45 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:deb7065b3304c3a9834f31b8a53e8d6089060e9c6522668abd22f1f4d9f52ca7`  
		Last Modified: Tue, 09 Aug 2022 17:18:45 GMT  
		Size: 2.8 MB (2812989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20bd0e6368901462206ecfbedd1db3517fe94f68bc7b57918c328df47fbdbbf3`  
		Last Modified: Wed, 10 Aug 2022 02:58:51 GMT  
		Size: 56.6 MB (56628364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2f41beebf7247171a5b275e0598e9ed16be2ad6ffa16ad4c9c8f036f8800f1`  
		Last Modified: Wed, 10 Aug 2022 02:58:38 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d583bf09d162033ea6a52f524d3142e51ab87f5ce8e1c17c918e8c47527016c`  
		Last Modified: Wed, 10 Aug 2022 02:58:36 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593fae9e149af994c09345a3dcb015f0959fed2dd20e229f5fafea90d08f429b`  
		Last Modified: Wed, 10 Aug 2022 02:58:36 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96057fb9286d4d93de5c991d820e3b03be1923bec7ea58592b8417b9f69368bc`  
		Last Modified: Wed, 10 Aug 2022 02:58:36 GMT  
		Size: 3.0 KB (3032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e77133cc538711ede4f9dda1c5d44ea027f26326760bb0136c00411045f62d0d`  
		Last Modified: Wed, 10 Aug 2022 02:58:47 GMT  
		Size: 116.7 MB (116690853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:933c622a69b13e9df15b3809c6323b98b3a6e697a0ce37025afde53920527a41`  
		Last Modified: Wed, 10 Aug 2022 02:58:36 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.14.0`

```console
$ docker pull bonita@sha256:977f4e8862be31d76a5a463b0238a58fcd4af483ea1c6d6cb1ed75a1447c0d23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.14.0` - linux; amd64

```console
$ docker pull bonita@sha256:08cde8fece645d8b60bc13cf85691f0a092238a270c1a95554fc71714cd25237
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180333152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83b7a73741c772da78e05b71140aeaa6e2838bcfef7277b7af94e3813db00ebb`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:15:43 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 09 Aug 2022 18:15:47 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 09 Aug 2022 18:15:47 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 09 Aug 2022 18:15:48 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BONITA_VERSION
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BRANDING_VERSION
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BONITA_SHA256
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BASE_URL
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BONITA_URL
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 09 Aug 2022 18:15:49 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 09 Aug 2022 18:15:50 GMT
RUN mkdir /opt/files
# Tue, 09 Aug 2022 18:15:50 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 09 Aug 2022 18:16:01 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 09 Aug 2022 18:16:02 GMT
ENV HTTP_API=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 09 Aug 2022 18:16:02 GMT
ENV HTTP_API_PASSWORD=
# Tue, 09 Aug 2022 18:16:02 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 09 Aug 2022 18:16:02 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 09 Aug 2022 18:16:02 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 09 Aug 2022 18:16:03 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 09 Aug 2022 18:16:03 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 09 Aug 2022 18:16:03 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 09 Aug 2022 18:16:03 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 09 Aug 2022 18:16:03 GMT
EXPOSE 8080 9000
# Tue, 09 Aug 2022 18:16:03 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 09 Aug 2022 18:16:03 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e40e66c88000cdcf6a5f303ff471b71908973b42e6d2c853ebafc528c1f58d`  
		Last Modified: Tue, 09 Aug 2022 18:16:38 GMT  
		Size: 60.8 MB (60808791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8517b429307545f8abc13fc0b37faa4607093e758af1d721cd166a9c9d59ec60`  
		Last Modified: Tue, 09 Aug 2022 18:16:29 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a90d8fa310d2a6ea37f38a5d6783134999b8e41a9a6cea96f56c35fef2514e`  
		Last Modified: Tue, 09 Aug 2022 18:16:27 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7082e206c7455f0f4b81da210af350e50379ccb7f4d413868083cb6bd93fb7`  
		Last Modified: Tue, 09 Aug 2022 18:16:27 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1afa20c272a36d9fffe827f8ce399a488ef133030401d5e3892cb8f30b9ab2c7`  
		Last Modified: Tue, 09 Aug 2022 18:16:27 GMT  
		Size: 3.0 KB (3034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9086b05d70c72cfe77142c9829855c34c099504b88df663d5d954537502aef`  
		Last Modified: Tue, 09 Aug 2022 18:16:34 GMT  
		Size: 116.7 MB (116690829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153200db9a09f679584a791a878014d3dcdf52d99869e37107b43db18c4d9cc3`  
		Last Modified: Tue, 09 Aug 2022 18:16:27 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.14.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:9659f7730d354083e732097fd3656a47ab26b8c4f2010683fc2fbe6358cd9dad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179546604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30779f62863399675fedee53f8a02f2a0fea94360bde10754580989873e9ef13`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:18:32 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 09 Aug 2022 18:18:36 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 09 Aug 2022 18:18:36 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 09 Aug 2022 18:18:37 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 09 Aug 2022 18:18:38 GMT
ARG BONITA_VERSION
# Tue, 09 Aug 2022 18:18:39 GMT
ARG BRANDING_VERSION
# Tue, 09 Aug 2022 18:18:40 GMT
ARG BONITA_SHA256
# Tue, 09 Aug 2022 18:18:41 GMT
ARG BASE_URL
# Tue, 09 Aug 2022 18:18:42 GMT
ARG BONITA_URL
# Tue, 09 Aug 2022 18:18:43 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 09 Aug 2022 18:18:44 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 09 Aug 2022 18:18:45 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 09 Aug 2022 18:18:46 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 09 Aug 2022 18:18:47 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 09 Aug 2022 18:18:48 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 09 Aug 2022 18:18:49 GMT
RUN mkdir /opt/files
# Tue, 09 Aug 2022 18:18:51 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 09 Aug 2022 18:19:04 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 09 Aug 2022 18:19:05 GMT
ENV HTTP_API=false
# Tue, 09 Aug 2022 18:19:06 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 09 Aug 2022 18:19:07 GMT
ENV HTTP_API_PASSWORD=
# Tue, 09 Aug 2022 18:19:08 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 09 Aug 2022 18:19:09 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 09 Aug 2022 18:19:10 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 09 Aug 2022 18:19:11 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 09 Aug 2022 18:19:12 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 09 Aug 2022 18:19:13 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 09 Aug 2022 18:19:14 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 09 Aug 2022 18:19:15 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 09 Aug 2022 18:19:16 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 09 Aug 2022 18:19:17 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 09 Aug 2022 18:19:19 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 09 Aug 2022 18:19:19 GMT
EXPOSE 8080 9000
# Tue, 09 Aug 2022 18:19:20 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 09 Aug 2022 18:19:21 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc88915541d6f4421b66a886f25f68b9655dc1dee732760c3086d5e8b3304a4a`  
		Last Modified: Tue, 09 Aug 2022 18:20:24 GMT  
		Size: 60.1 MB (60129514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319bc8304739386ec9aab2a1dcd52eb85ca85059ce787cc536f24934bb6907c1`  
		Last Modified: Tue, 09 Aug 2022 18:20:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f5f51932f11b34b80147eec1268be25c87b241a595d18adb836b09480ebee6`  
		Last Modified: Tue, 09 Aug 2022 18:20:13 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec51c34c596f0fcdf1cc75e2c3154642dc1e041ed2d502ad3468cbf5ee7633a`  
		Last Modified: Tue, 09 Aug 2022 18:20:13 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ccaa414eaa82b83c723b3217df9302e719890e1ceacda1452c141980ae6f5d`  
		Last Modified: Tue, 09 Aug 2022 18:20:13 GMT  
		Size: 3.0 KB (3002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:334448ededff63c05c8efe4578487e4b1ad071d95373c4c39515f1c33472d788`  
		Last Modified: Tue, 09 Aug 2022 18:20:17 GMT  
		Size: 116.7 MB (116688789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b61a4040e3817598cff22a8fae45d9f16a5d5f8703e2acef71454e5df2d9889`  
		Last Modified: Tue, 09 Aug 2022 18:20:13 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.14.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:905376aad5c6b1828a693ea6913e13ee18e890176d32e306d9f9d015ddd0b228
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176142222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34f7c95b1e8662e1c67b791b144f27360f33bf8c5a12aa9beb134ef618268006`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 09 Aug 2022 17:17:20 GMT
ADD file:be31abb0aba89ed5ff9200736a1c46091abc3845d0e332efd5e5c874ef2c99d1 in / 
# Tue, 09 Aug 2022 17:17:21 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 02:57:05 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 10 Aug 2022 02:57:14 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Wed, 10 Aug 2022 02:57:16 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 10 Aug 2022 02:57:18 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Wed, 10 Aug 2022 02:57:19 GMT
ARG BONITA_VERSION
# Wed, 10 Aug 2022 02:57:19 GMT
ARG BRANDING_VERSION
# Wed, 10 Aug 2022 02:57:19 GMT
ARG BONITA_SHA256
# Wed, 10 Aug 2022 02:57:19 GMT
ARG BASE_URL
# Wed, 10 Aug 2022 02:57:20 GMT
ARG BONITA_URL
# Wed, 10 Aug 2022 02:57:20 GMT
ENV BONITA_VERSION=7.14.0
# Wed, 10 Aug 2022 02:57:20 GMT
ENV BRANDING_VERSION=2022.1-u0
# Wed, 10 Aug 2022 02:57:21 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Wed, 10 Aug 2022 02:57:21 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Wed, 10 Aug 2022 02:57:21 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 10 Aug 2022 02:57:21 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Wed, 10 Aug 2022 02:57:23 GMT
RUN mkdir /opt/files
# Wed, 10 Aug 2022 02:57:23 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Wed, 10 Aug 2022 02:57:37 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Wed, 10 Aug 2022 02:57:39 GMT
ENV HTTP_API=false
# Wed, 10 Aug 2022 02:57:39 GMT
ENV HTTP_API_USERNAME=http-api
# Wed, 10 Aug 2022 02:57:40 GMT
ENV HTTP_API_PASSWORD=
# Wed, 10 Aug 2022 02:57:40 GMT
ENV MONITORING_USERNAME=monitoring
# Wed, 10 Aug 2022 02:57:40 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Wed, 10 Aug 2022 02:57:41 GMT
ENV JMX_REMOTE_ACCESS=false
# Wed, 10 Aug 2022 02:57:41 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Wed, 10 Aug 2022 02:57:42 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Wed, 10 Aug 2022 02:57:42 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Wed, 10 Aug 2022 02:57:42 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Wed, 10 Aug 2022 02:57:43 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Wed, 10 Aug 2022 02:57:43 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Wed, 10 Aug 2022 02:57:44 GMT
ENV HTTP_MAX_THREADS=20
# Wed, 10 Aug 2022 02:57:44 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Wed, 10 Aug 2022 02:57:44 GMT
EXPOSE 8080 9000
# Wed, 10 Aug 2022 02:57:45 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Wed, 10 Aug 2022 02:57:45 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:deb7065b3304c3a9834f31b8a53e8d6089060e9c6522668abd22f1f4d9f52ca7`  
		Last Modified: Tue, 09 Aug 2022 17:18:45 GMT  
		Size: 2.8 MB (2812989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20bd0e6368901462206ecfbedd1db3517fe94f68bc7b57918c328df47fbdbbf3`  
		Last Modified: Wed, 10 Aug 2022 02:58:51 GMT  
		Size: 56.6 MB (56628364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2f41beebf7247171a5b275e0598e9ed16be2ad6ffa16ad4c9c8f036f8800f1`  
		Last Modified: Wed, 10 Aug 2022 02:58:38 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d583bf09d162033ea6a52f524d3142e51ab87f5ce8e1c17c918e8c47527016c`  
		Last Modified: Wed, 10 Aug 2022 02:58:36 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593fae9e149af994c09345a3dcb015f0959fed2dd20e229f5fafea90d08f429b`  
		Last Modified: Wed, 10 Aug 2022 02:58:36 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96057fb9286d4d93de5c991d820e3b03be1923bec7ea58592b8417b9f69368bc`  
		Last Modified: Wed, 10 Aug 2022 02:58:36 GMT  
		Size: 3.0 KB (3032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e77133cc538711ede4f9dda1c5d44ea027f26326760bb0136c00411045f62d0d`  
		Last Modified: Wed, 10 Aug 2022 02:58:47 GMT  
		Size: 116.7 MB (116690853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:933c622a69b13e9df15b3809c6323b98b3a6e697a0ce37025afde53920527a41`  
		Last Modified: Wed, 10 Aug 2022 02:58:36 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:latest`

```console
$ docker pull bonita@sha256:977f4e8862be31d76a5a463b0238a58fcd4af483ea1c6d6cb1ed75a1447c0d23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:latest` - linux; amd64

```console
$ docker pull bonita@sha256:08cde8fece645d8b60bc13cf85691f0a092238a270c1a95554fc71714cd25237
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180333152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83b7a73741c772da78e05b71140aeaa6e2838bcfef7277b7af94e3813db00ebb`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:15:43 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 09 Aug 2022 18:15:47 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 09 Aug 2022 18:15:47 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 09 Aug 2022 18:15:48 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BONITA_VERSION
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BRANDING_VERSION
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BONITA_SHA256
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BASE_URL
# Tue, 09 Aug 2022 18:15:48 GMT
ARG BONITA_URL
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 09 Aug 2022 18:15:49 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 09 Aug 2022 18:15:49 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 09 Aug 2022 18:15:50 GMT
RUN mkdir /opt/files
# Tue, 09 Aug 2022 18:15:50 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 09 Aug 2022 18:16:01 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 09 Aug 2022 18:16:02 GMT
ENV HTTP_API=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 09 Aug 2022 18:16:02 GMT
ENV HTTP_API_PASSWORD=
# Tue, 09 Aug 2022 18:16:02 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 09 Aug 2022 18:16:02 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 09 Aug 2022 18:16:02 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 09 Aug 2022 18:16:02 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 09 Aug 2022 18:16:03 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 09 Aug 2022 18:16:03 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 09 Aug 2022 18:16:03 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 09 Aug 2022 18:16:03 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 09 Aug 2022 18:16:03 GMT
EXPOSE 8080 9000
# Tue, 09 Aug 2022 18:16:03 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 09 Aug 2022 18:16:03 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e40e66c88000cdcf6a5f303ff471b71908973b42e6d2c853ebafc528c1f58d`  
		Last Modified: Tue, 09 Aug 2022 18:16:38 GMT  
		Size: 60.8 MB (60808791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8517b429307545f8abc13fc0b37faa4607093e758af1d721cd166a9c9d59ec60`  
		Last Modified: Tue, 09 Aug 2022 18:16:29 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a90d8fa310d2a6ea37f38a5d6783134999b8e41a9a6cea96f56c35fef2514e`  
		Last Modified: Tue, 09 Aug 2022 18:16:27 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7082e206c7455f0f4b81da210af350e50379ccb7f4d413868083cb6bd93fb7`  
		Last Modified: Tue, 09 Aug 2022 18:16:27 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1afa20c272a36d9fffe827f8ce399a488ef133030401d5e3892cb8f30b9ab2c7`  
		Last Modified: Tue, 09 Aug 2022 18:16:27 GMT  
		Size: 3.0 KB (3034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9086b05d70c72cfe77142c9829855c34c099504b88df663d5d954537502aef`  
		Last Modified: Tue, 09 Aug 2022 18:16:34 GMT  
		Size: 116.7 MB (116690829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153200db9a09f679584a791a878014d3dcdf52d99869e37107b43db18c4d9cc3`  
		Last Modified: Tue, 09 Aug 2022 18:16:27 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:9659f7730d354083e732097fd3656a47ab26b8c4f2010683fc2fbe6358cd9dad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179546604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30779f62863399675fedee53f8a02f2a0fea94360bde10754580989873e9ef13`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:18:32 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 09 Aug 2022 18:18:36 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Tue, 09 Aug 2022 18:18:36 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 09 Aug 2022 18:18:37 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Tue, 09 Aug 2022 18:18:38 GMT
ARG BONITA_VERSION
# Tue, 09 Aug 2022 18:18:39 GMT
ARG BRANDING_VERSION
# Tue, 09 Aug 2022 18:18:40 GMT
ARG BONITA_SHA256
# Tue, 09 Aug 2022 18:18:41 GMT
ARG BASE_URL
# Tue, 09 Aug 2022 18:18:42 GMT
ARG BONITA_URL
# Tue, 09 Aug 2022 18:18:43 GMT
ENV BONITA_VERSION=7.14.0
# Tue, 09 Aug 2022 18:18:44 GMT
ENV BRANDING_VERSION=2022.1-u0
# Tue, 09 Aug 2022 18:18:45 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Tue, 09 Aug 2022 18:18:46 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Tue, 09 Aug 2022 18:18:47 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 09 Aug 2022 18:18:48 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Tue, 09 Aug 2022 18:18:49 GMT
RUN mkdir /opt/files
# Tue, 09 Aug 2022 18:18:51 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Tue, 09 Aug 2022 18:19:04 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Tue, 09 Aug 2022 18:19:05 GMT
ENV HTTP_API=false
# Tue, 09 Aug 2022 18:19:06 GMT
ENV HTTP_API_USERNAME=http-api
# Tue, 09 Aug 2022 18:19:07 GMT
ENV HTTP_API_PASSWORD=
# Tue, 09 Aug 2022 18:19:08 GMT
ENV MONITORING_USERNAME=monitoring
# Tue, 09 Aug 2022 18:19:09 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Tue, 09 Aug 2022 18:19:10 GMT
ENV JMX_REMOTE_ACCESS=false
# Tue, 09 Aug 2022 18:19:11 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Tue, 09 Aug 2022 18:19:12 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Tue, 09 Aug 2022 18:19:13 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Tue, 09 Aug 2022 18:19:14 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Tue, 09 Aug 2022 18:19:15 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Tue, 09 Aug 2022 18:19:16 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Tue, 09 Aug 2022 18:19:17 GMT
ENV HTTP_MAX_THREADS=20
# Tue, 09 Aug 2022 18:19:19 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Tue, 09 Aug 2022 18:19:19 GMT
EXPOSE 8080 9000
# Tue, 09 Aug 2022 18:19:20 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Tue, 09 Aug 2022 18:19:21 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc88915541d6f4421b66a886f25f68b9655dc1dee732760c3086d5e8b3304a4a`  
		Last Modified: Tue, 09 Aug 2022 18:20:24 GMT  
		Size: 60.1 MB (60129514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319bc8304739386ec9aab2a1dcd52eb85ca85059ce787cc536f24934bb6907c1`  
		Last Modified: Tue, 09 Aug 2022 18:20:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f5f51932f11b34b80147eec1268be25c87b241a595d18adb836b09480ebee6`  
		Last Modified: Tue, 09 Aug 2022 18:20:13 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec51c34c596f0fcdf1cc75e2c3154642dc1e041ed2d502ad3468cbf5ee7633a`  
		Last Modified: Tue, 09 Aug 2022 18:20:13 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ccaa414eaa82b83c723b3217df9302e719890e1ceacda1452c141980ae6f5d`  
		Last Modified: Tue, 09 Aug 2022 18:20:13 GMT  
		Size: 3.0 KB (3002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:334448ededff63c05c8efe4578487e4b1ad071d95373c4c39515f1c33472d788`  
		Last Modified: Tue, 09 Aug 2022 18:20:17 GMT  
		Size: 116.7 MB (116688789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b61a4040e3817598cff22a8fae45d9f16a5d5f8703e2acef71454e5df2d9889`  
		Last Modified: Tue, 09 Aug 2022 18:20:13 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; ppc64le

```console
$ docker pull bonita@sha256:905376aad5c6b1828a693ea6913e13ee18e890176d32e306d9f9d015ddd0b228
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176142222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34f7c95b1e8662e1c67b791b144f27360f33bf8c5a12aa9beb134ef618268006`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 09 Aug 2022 17:17:20 GMT
ADD file:be31abb0aba89ed5ff9200736a1c46091abc3845d0e332efd5e5c874ef2c99d1 in / 
# Tue, 09 Aug 2022 17:17:21 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 02:57:05 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 10 Aug 2022 02:57:14 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Wed, 10 Aug 2022 02:57:16 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 10 Aug 2022 02:57:18 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Wed, 10 Aug 2022 02:57:19 GMT
ARG BONITA_VERSION
# Wed, 10 Aug 2022 02:57:19 GMT
ARG BRANDING_VERSION
# Wed, 10 Aug 2022 02:57:19 GMT
ARG BONITA_SHA256
# Wed, 10 Aug 2022 02:57:19 GMT
ARG BASE_URL
# Wed, 10 Aug 2022 02:57:20 GMT
ARG BONITA_URL
# Wed, 10 Aug 2022 02:57:20 GMT
ENV BONITA_VERSION=7.14.0
# Wed, 10 Aug 2022 02:57:20 GMT
ENV BRANDING_VERSION=2022.1-u0
# Wed, 10 Aug 2022 02:57:21 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Wed, 10 Aug 2022 02:57:21 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Wed, 10 Aug 2022 02:57:21 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 10 Aug 2022 02:57:21 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Wed, 10 Aug 2022 02:57:23 GMT
RUN mkdir /opt/files
# Wed, 10 Aug 2022 02:57:23 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Wed, 10 Aug 2022 02:57:37 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Wed, 10 Aug 2022 02:57:39 GMT
ENV HTTP_API=false
# Wed, 10 Aug 2022 02:57:39 GMT
ENV HTTP_API_USERNAME=http-api
# Wed, 10 Aug 2022 02:57:40 GMT
ENV HTTP_API_PASSWORD=
# Wed, 10 Aug 2022 02:57:40 GMT
ENV MONITORING_USERNAME=monitoring
# Wed, 10 Aug 2022 02:57:40 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Wed, 10 Aug 2022 02:57:41 GMT
ENV JMX_REMOTE_ACCESS=false
# Wed, 10 Aug 2022 02:57:41 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Wed, 10 Aug 2022 02:57:42 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Wed, 10 Aug 2022 02:57:42 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Wed, 10 Aug 2022 02:57:42 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Wed, 10 Aug 2022 02:57:43 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Wed, 10 Aug 2022 02:57:43 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Wed, 10 Aug 2022 02:57:44 GMT
ENV HTTP_MAX_THREADS=20
# Wed, 10 Aug 2022 02:57:44 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Wed, 10 Aug 2022 02:57:44 GMT
EXPOSE 8080 9000
# Wed, 10 Aug 2022 02:57:45 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Wed, 10 Aug 2022 02:57:45 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:deb7065b3304c3a9834f31b8a53e8d6089060e9c6522668abd22f1f4d9f52ca7`  
		Last Modified: Tue, 09 Aug 2022 17:18:45 GMT  
		Size: 2.8 MB (2812989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20bd0e6368901462206ecfbedd1db3517fe94f68bc7b57918c328df47fbdbbf3`  
		Last Modified: Wed, 10 Aug 2022 02:58:51 GMT  
		Size: 56.6 MB (56628364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2f41beebf7247171a5b275e0598e9ed16be2ad6ffa16ad4c9c8f036f8800f1`  
		Last Modified: Wed, 10 Aug 2022 02:58:38 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d583bf09d162033ea6a52f524d3142e51ab87f5ce8e1c17c918e8c47527016c`  
		Last Modified: Wed, 10 Aug 2022 02:58:36 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593fae9e149af994c09345a3dcb015f0959fed2dd20e229f5fafea90d08f429b`  
		Last Modified: Wed, 10 Aug 2022 02:58:36 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96057fb9286d4d93de5c991d820e3b03be1923bec7ea58592b8417b9f69368bc`  
		Last Modified: Wed, 10 Aug 2022 02:58:36 GMT  
		Size: 3.0 KB (3032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e77133cc538711ede4f9dda1c5d44ea027f26326760bb0136c00411045f62d0d`  
		Last Modified: Wed, 10 Aug 2022 02:58:47 GMT  
		Size: 116.7 MB (116690853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:933c622a69b13e9df15b3809c6323b98b3a6e697a0ce37025afde53920527a41`  
		Last Modified: Wed, 10 Aug 2022 02:58:36 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
