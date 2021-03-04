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
$ docker pull bonita@sha256:92023653b15e0dde13c5a796f799122c47fc02865749ac63473626bacb658239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2021.1` - linux; amd64

```console
$ docker pull bonita@sha256:acb5236fefd92ff819cccce8ff039bfcee49d3ffd8b8408ec9eb86e1e044034d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.9 MB (238892145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:187e939000b59a7d68f188b581df9d3cae03e73cb682657a582674e0c8c29fc2`
-	Default Command: `["\/opt\/files\/startup.sh"]`

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
# Thu, 04 Mar 2021 03:38:30 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 04 Mar 2021 03:38:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 03:38:56 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 04 Mar 2021 03:38:57 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 04 Mar 2021 03:38:58 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 04 Mar 2021 03:38:59 GMT
ARG BONITA_VERSION
# Thu, 04 Mar 2021 03:39:17 GMT
ARG BRANDING_VERSION
# Thu, 04 Mar 2021 03:39:17 GMT
ARG BONITA_SHA256
# Thu, 04 Mar 2021 03:39:17 GMT
ARG BASE_URL
# Thu, 04 Mar 2021 03:39:17 GMT
ARG BONITA_URL
# Thu, 04 Mar 2021 03:39:18 GMT
ENV BONITA_VERSION=7.12.1
# Thu, 04 Mar 2021 03:39:18 GMT
ENV BRANDING_VERSION=2021.1
# Thu, 04 Mar 2021 03:39:18 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Thu, 04 Mar 2021 03:39:18 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Thu, 04 Mar 2021 03:39:18 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 04 Mar 2021 03:39:19 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Thu, 04 Mar 2021 03:39:20 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Thu, 04 Mar 2021 03:39:21 GMT
RUN mkdir /opt/files
# Thu, 04 Mar 2021 03:39:21 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Thu, 04 Mar 2021 03:39:26 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Thu, 04 Mar 2021 03:39:29 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Thu, 04 Mar 2021 03:39:31 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Thu, 04 Mar 2021 03:39:31 GMT
VOLUME [/opt/bonita]
# Thu, 04 Mar 2021 03:39:32 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 04 Mar 2021 03:39:32 GMT
EXPOSE 8080
# Thu, 04 Mar 2021 03:39:32 GMT
CMD ["/opt/files/startup.sh"]
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
	-	`sha256:0b013a5e6d745d8ddf229fc1b6efe515531408d68a38ccdfd19fe2734a796e20`  
		Last Modified: Thu, 04 Mar 2021 03:40:39 GMT  
		Size: 95.2 MB (95182489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43c3d83e550e3c03dbf7d5be4813516f132b770f495793ae7ec767850a867c0`  
		Last Modified: Thu, 04 Mar 2021 03:40:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e491464ad3b52ebf5550aee453151a66f342c6fae6fd17dddaa8ecfd52de0eb`  
		Last Modified: Thu, 04 Mar 2021 03:40:19 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ac5a46d0b9f41259cbbd28b965b962ac61af24a85d5940ac903bd1e53ec4a1`  
		Last Modified: Thu, 04 Mar 2021 03:40:19 GMT  
		Size: 572.4 KB (572376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d472c4128821436fa9d86e73569e07fc23ad4f59a21e2fccfcd1ee9e9c020b85`  
		Last Modified: Thu, 04 Mar 2021 03:40:45 GMT  
		Size: 112.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a35d3dfa6026e7fa52e17e9e231a17fbd844b63b8d7f0272216e59cd56bff4`  
		Last Modified: Thu, 04 Mar 2021 03:40:45 GMT  
		Size: 6.9 KB (6916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeed78bcae57a07524cd258132b6af9e23f9ecc6785be1f5f694755051ecf8be`  
		Last Modified: Thu, 04 Mar 2021 03:40:51 GMT  
		Size: 116.4 MB (116415402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c3e90c609477ff5a3252818b53a8e93c79ce128be2829b763ed5019a1c5688`  
		Last Modified: Thu, 04 Mar 2021 03:40:45 GMT  
		Size: 1.7 KB (1683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:042b27c155776c49fa827a611e68600e3ab7616ae5be3bbe45c57e5f8c41a4d8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.0 MB (225999606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1473c8d2979e05f1c6fe37e1c2ef0c1c3f0d01b1d9b043222c585bd2f204ea03`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 21 Jan 2021 03:49:23 GMT
ADD file:7d9bc01cf1f3757bf5fa308213a77aeb128883cc13616ff46b3da5b0e65b92f2 in / 
# Thu, 21 Jan 2021 03:49:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:49:29 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:49:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:49:32 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 05:28:20 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 21 Jan 2021 05:29:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 05:29:09 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 21 Jan 2021 05:29:11 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 21 Jan 2021 05:29:13 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 21 Jan 2021 05:29:14 GMT
ARG BONITA_VERSION
# Sat, 30 Jan 2021 00:53:50 GMT
ARG BRANDING_VERSION
# Sat, 30 Jan 2021 00:53:50 GMT
ARG BONITA_SHA256
# Sat, 30 Jan 2021 00:53:51 GMT
ARG BASE_URL
# Sat, 30 Jan 2021 00:53:51 GMT
ARG BONITA_URL
# Sat, 30 Jan 2021 00:53:52 GMT
ENV BONITA_VERSION=7.12.1
# Sat, 30 Jan 2021 00:53:53 GMT
ENV BRANDING_VERSION=2021.1
# Sat, 30 Jan 2021 00:53:53 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Sat, 30 Jan 2021 00:53:54 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Sat, 30 Jan 2021 00:53:54 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 30 Jan 2021 00:53:55 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Sat, 30 Jan 2021 00:53:57 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Sat, 30 Jan 2021 00:53:59 GMT
RUN mkdir /opt/files
# Sat, 30 Jan 2021 00:54:00 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Sat, 30 Jan 2021 00:54:06 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Sat, 30 Jan 2021 00:54:08 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Sat, 30 Jan 2021 00:54:11 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Sat, 30 Jan 2021 00:54:12 GMT
VOLUME [/opt/bonita]
# Sat, 30 Jan 2021 00:54:12 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Sat, 30 Jan 2021 00:54:13 GMT
EXPOSE 8080
# Sat, 30 Jan 2021 00:54:14 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:64e3fba066352e44a4c1eeb6caedc87c29b46f0a7b31e21a58183fc8370005bd`  
		Last Modified: Tue, 19 Jan 2021 00:25:17 GMT  
		Size: 23.7 MB (23732640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dbb433f451339aab734bb52e3df5b34cdea477f3f8e3aa32f7ac060bd852de2`  
		Last Modified: Thu, 21 Jan 2021 03:51:55 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3042a0d94b83caeb29bc20734c197130f58e14e86e8e6cdad8b768052bb563c`  
		Last Modified: Thu, 21 Jan 2021 03:51:54 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8df92044c4b506076de6abc24afe1d5eac83a9e6cc5fb97a725daea7b5fb742`  
		Last Modified: Thu, 21 Jan 2021 05:31:28 GMT  
		Size: 85.3 MB (85297873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1abc3fcd55457d935f9da38456f79f5f4c394ff39f5f0bf92deb550a9c5d5a8`  
		Last Modified: Thu, 21 Jan 2021 05:31:05 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb17a62d1dc9db97a189188b6263b79601d869b5f3813597d9c9990e9b1e67b0`  
		Last Modified: Thu, 21 Jan 2021 05:31:04 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af2268a1d88611b9add2dc44af567d1d121e316d036e49cbd1b3f54717c4019`  
		Last Modified: Thu, 21 Jan 2021 05:31:03 GMT  
		Size: 541.8 KB (541813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a6d9f507c165d2c3713ddc71f40686f7efab71e36563b00a38df6544f734a9`  
		Last Modified: Sat, 30 Jan 2021 00:54:31 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e96b3ed213aa787365c4954d6c9d9f0f6339011bb25c1da83b930936e897408f`  
		Last Modified: Sat, 30 Jan 2021 00:54:31 GMT  
		Size: 6.9 KB (6946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d407eacd2633e2d566bbdbc12ca4a0bfb1598bc401e81b0c7b2ac5789018614c`  
		Last Modified: Sat, 30 Jan 2021 00:54:41 GMT  
		Size: 116.4 MB (116415398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8263bbe0ad9c06ee5e05b8540e8b539f69ce8f36cd16c611f40d2a27977da5`  
		Last Modified: Sat, 30 Jan 2021 00:54:31 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:7cbc79ac9276eeb9ed45b37e7460eb8b82cd17ee65bf79366743255784a8fed5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.3 MB (233308791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2deb92cacf66527c2fdde8cdd3931695079b54e53a5882fc939be196f3fc36c`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 21 Jan 2021 03:49:03 GMT
ADD file:f6214eb5991df55aa5198d84442d6ddd28b67d4043d1832afba8b30e0249dcf5 in / 
# Thu, 21 Jan 2021 03:49:39 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:49:50 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:50:04 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:50:09 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 04:23:39 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 21 Jan 2021 04:27:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 04:28:04 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 21 Jan 2021 04:28:10 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 21 Jan 2021 04:28:18 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 21 Jan 2021 04:28:22 GMT
ARG BONITA_VERSION
# Sat, 30 Jan 2021 01:47:09 GMT
ARG BRANDING_VERSION
# Sat, 30 Jan 2021 01:47:17 GMT
ARG BONITA_SHA256
# Sat, 30 Jan 2021 01:47:23 GMT
ARG BASE_URL
# Sat, 30 Jan 2021 01:47:32 GMT
ARG BONITA_URL
# Sat, 30 Jan 2021 01:47:38 GMT
ENV BONITA_VERSION=7.12.1
# Sat, 30 Jan 2021 01:47:46 GMT
ENV BRANDING_VERSION=2021.1
# Sat, 30 Jan 2021 01:48:02 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Sat, 30 Jan 2021 01:48:07 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Sat, 30 Jan 2021 01:48:11 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 30 Jan 2021 01:48:13 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Sat, 30 Jan 2021 01:48:30 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Sat, 30 Jan 2021 01:48:55 GMT
RUN mkdir /opt/files
# Sat, 30 Jan 2021 01:48:59 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Sat, 30 Jan 2021 01:49:27 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Sat, 30 Jan 2021 01:49:41 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Sat, 30 Jan 2021 01:49:52 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Sat, 30 Jan 2021 01:49:57 GMT
VOLUME [/opt/bonita]
# Sat, 30 Jan 2021 01:50:00 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Sat, 30 Jan 2021 01:50:08 GMT
EXPOSE 8080
# Sat, 30 Jan 2021 01:50:13 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:e07786faec2ce77c08f20befe52a3eac52d983b0dfae9cb8d58dfa0ede0648e1`  
		Last Modified: Thu, 21 Jan 2021 03:54:37 GMT  
		Size: 30.4 MB (30422854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a41aaf71d5cf82fa1f9e11d2d352906ae135d0b216c665ed76ad9a8e1ce046`  
		Last Modified: Thu, 21 Jan 2021 03:54:30 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae0c92402f48f37a5d3bf1b351e5c6cbed6cec502dc9138f974a2e114c29ce4`  
		Last Modified: Thu, 21 Jan 2021 03:52:10 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b13b45af58aa295d275be3fb2ee2cdae02906032f23429acfe6e350037d8ab93`  
		Last Modified: Thu, 21 Jan 2021 04:31:44 GMT  
		Size: 85.9 MB (85917102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85b382bfd13fccaece5a5a9972badb85c89b4e5d49d62b01a5c56586d69dff55`  
		Last Modified: Thu, 21 Jan 2021 04:31:24 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b765dbe8b65a01b5e7a6c6bcf266a3f252f9ecab42044078374cd592222b75c1`  
		Last Modified: Thu, 21 Jan 2021 04:31:25 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9bc546cf88c8886a652c41a34d2b48be1bdf5a74182087aea7df14653843a8`  
		Last Modified: Thu, 21 Jan 2021 04:31:21 GMT  
		Size: 541.5 KB (541539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3328d3e249051dfe4783d885b91ec5874d8d654b2c198cc6e62b5eee230942bf`  
		Last Modified: Sat, 30 Jan 2021 01:50:42 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0341326e395d84e7152c652f6370e970564a985e74835fe94d52123709c5ae13`  
		Last Modified: Sat, 30 Jan 2021 01:50:42 GMT  
		Size: 7.0 KB (6950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b610564454d7cbfa5e7c6d19b44df37a3ff995fc38607f6154903eb2fde0914`  
		Last Modified: Sat, 30 Jan 2021 01:50:52 GMT  
		Size: 116.4 MB (116415407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06136d8ff274d12b9e1962bd89095c8930d5f735cb50f3942ae371b5128ff1af`  
		Last Modified: Sat, 30 Jan 2021 01:50:43 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.10`

```console
$ docker pull bonita@sha256:6ea3e56e6c525da95921d14525e7637fb1ccc8daec972696656a51d1c119d085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.10` - linux; amd64

```console
$ docker pull bonita@sha256:0a154b80d33af0abac0d3142da30765c96ab95be34e8e8c6da7848ce3c18342b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.0 MB (243978671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d57209e61995d778e22e5fbe0672dbaa5b9aa9eac3e989a85a8a6fd6cf57b31`
-	Default Command: `["\/opt\/files\/startup.sh"]`

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
# Thu, 04 Mar 2021 03:37:13 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Thu, 04 Mar 2021 03:38:03 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 03:38:05 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 04 Mar 2021 03:38:06 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 04 Mar 2021 03:38:08 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 04 Mar 2021 03:38:08 GMT
ARG BONITA_VERSION
# Thu, 04 Mar 2021 03:38:08 GMT
ARG BONITA_SHA256
# Thu, 04 Mar 2021 03:38:08 GMT
ARG BASE_URL
# Thu, 04 Mar 2021 03:38:08 GMT
ARG BONITA_URL
# Thu, 04 Mar 2021 03:38:09 GMT
ENV BONITA_VERSION=7.10.6
# Thu, 04 Mar 2021 03:38:09 GMT
ENV BONITA_SHA256=aaf61a044e7a8d9ec95d2b5d0c315a6d01d9c93ba01d753fcb008e2cfbbb725f
# Thu, 04 Mar 2021 03:38:09 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 04 Mar 2021 03:38:09 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.10.6/BonitaCommunity-7.10.6.zip
# Thu, 04 Mar 2021 03:38:10 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Thu, 04 Mar 2021 03:38:14 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Thu, 04 Mar 2021 03:38:16 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Thu, 04 Mar 2021 03:38:17 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Thu, 04 Mar 2021 03:38:17 GMT
VOLUME [/opt/bonita]
# Thu, 04 Mar 2021 03:38:18 GMT
COPY dir:46816633cc37ba9fd23af260c8c2384c15f3b4385b5752d6b42577967959f7f0 in /opt/files 
# Thu, 04 Mar 2021 03:38:18 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Thu, 04 Mar 2021 03:38:18 GMT
EXPOSE 8080
# Thu, 04 Mar 2021 03:38:18 GMT
CMD ["/opt/files/startup.sh"]
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
	-	`sha256:434195674b944c7b26c9fac11ba8af5effb5d5df21c92f0acb661f52acfc19c3`  
		Last Modified: Thu, 04 Mar 2021 03:40:09 GMT  
		Size: 118.7 MB (118709940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4718803d801e9af254f6577f1d42bb5c03dbd5fc2e52507a9d3aa6b90932223c`  
		Last Modified: Thu, 04 Mar 2021 03:39:48 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbbeba20b0c723911b9025634ab5278680111bee7cfa3a4791b6895b81a21ff3`  
		Last Modified: Thu, 04 Mar 2021 03:39:47 GMT  
		Size: 1.9 KB (1912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cd42a066bb8ea4fccdf5391d3ef7f13652718c06b2a466e5a12019537fc74`  
		Last Modified: Thu, 04 Mar 2021 03:39:47 GMT  
		Size: 572.4 KB (572375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5847de73dde7005b9b0e2df701ae4b09a815af48447f29f5eb58d6dbf6f4c0a5`  
		Last Modified: Thu, 04 Mar 2021 03:39:53 GMT  
		Size: 98.0 MB (97973911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa0477e7a6d5149e0e209d722efebed2d27cd8e2ed879df850dfda85929c84a`  
		Last Modified: Thu, 04 Mar 2021 03:39:48 GMT  
		Size: 7.6 KB (7626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19d2d4183d7bd50e6f85bd6e0d8a60eb5724c6a59ff4c2ecc359ad0b0a919e7`  
		Last Modified: Thu, 04 Mar 2021 03:39:47 GMT  
		Size: 1.6 KB (1626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.10` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:40332cdc79c1f2a8e5187f413b5b31b6bf9285de6cf3d4565ea1f0034714111a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.8 MB (215803468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f2fc251d722cfd66c393c630ad4075f49a6da4595f2530549d9656e2a9551c0`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 21 Jan 2021 03:49:23 GMT
ADD file:7d9bc01cf1f3757bf5fa308213a77aeb128883cc13616ff46b3da5b0e65b92f2 in / 
# Thu, 21 Jan 2021 03:49:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:49:29 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:49:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:49:32 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 05:25:47 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Thu, 21 Jan 2021 05:26:50 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 05:26:55 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 21 Jan 2021 05:26:58 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 21 Jan 2021 05:27:02 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 21 Jan 2021 05:27:02 GMT
ARG BONITA_VERSION
# Thu, 21 Jan 2021 05:27:03 GMT
ARG BONITA_SHA256
# Thu, 21 Jan 2021 05:27:53 GMT
ARG BASE_URL
# Thu, 21 Jan 2021 05:27:53 GMT
ARG BONITA_URL
# Thu, 21 Jan 2021 05:27:54 GMT
ENV BONITA_VERSION=7.10.6
# Thu, 21 Jan 2021 05:27:55 GMT
ENV BONITA_SHA256=aaf61a044e7a8d9ec95d2b5d0c315a6d01d9c93ba01d753fcb008e2cfbbb725f
# Thu, 21 Jan 2021 05:27:56 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 21 Jan 2021 05:27:56 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.10.6/BonitaCommunity-7.10.6.zip
# Thu, 21 Jan 2021 05:27:58 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Thu, 21 Jan 2021 05:28:02 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Thu, 21 Jan 2021 05:28:05 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Thu, 21 Jan 2021 05:28:08 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Thu, 21 Jan 2021 05:28:10 GMT
VOLUME [/opt/bonita]
# Thu, 21 Jan 2021 05:28:11 GMT
COPY dir:46816633cc37ba9fd23af260c8c2384c15f3b4385b5752d6b42577967959f7f0 in /opt/files 
# Thu, 21 Jan 2021 05:28:12 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Thu, 21 Jan 2021 05:28:12 GMT
EXPOSE 8080
# Thu, 21 Jan 2021 05:28:13 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:64e3fba066352e44a4c1eeb6caedc87c29b46f0a7b31e21a58183fc8370005bd`  
		Last Modified: Tue, 19 Jan 2021 00:25:17 GMT  
		Size: 23.7 MB (23732640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dbb433f451339aab734bb52e3df5b34cdea477f3f8e3aa32f7ac060bd852de2`  
		Last Modified: Thu, 21 Jan 2021 03:51:55 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3042a0d94b83caeb29bc20734c197130f58e14e86e8e6cdad8b768052bb563c`  
		Last Modified: Thu, 21 Jan 2021 03:51:54 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24336a54672e821e94fa257760b5e413b70629939ef726f3bb2eeab9c0601edd`  
		Last Modified: Thu, 21 Jan 2021 05:30:31 GMT  
		Size: 93.5 MB (93542646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:552fdcf45b6eb86bd7d48ed1e77374970ba298ec65a68788f8acd4f04c890222`  
		Last Modified: Thu, 21 Jan 2021 05:30:09 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50bd7f50264ee42d6837fbee45fe7973e89ddb3b535df67a436953fb351b725e`  
		Last Modified: Thu, 21 Jan 2021 05:30:07 GMT  
		Size: 1.9 KB (1914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df34d15f6edd642a516be0ee0bca1199f4e6b25fb8bd67bb12933531f2fb9e0a`  
		Last Modified: Thu, 21 Jan 2021 05:30:07 GMT  
		Size: 541.8 KB (541810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486b97b8751e5407605c4e2db22b52b00b3b348e354abe58a82a5ba2c3f77b8c`  
		Last Modified: Thu, 21 Jan 2021 05:30:50 GMT  
		Size: 98.0 MB (97973962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e947cc90fd2185eebfd07a00ef5f294d3c49192a1cb89062fa7a411b5f3a1c5`  
		Last Modified: Thu, 21 Jan 2021 05:30:44 GMT  
		Size: 7.7 KB (7650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d578899624ad3033f7d8488f9e8cf0653579ae3cb9fea080434e925710d1bc2a`  
		Last Modified: Thu, 21 Jan 2021 05:30:44 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.10` - linux; ppc64le

```console
$ docker pull bonita@sha256:9478c7d1bda23a0c277dffe5a490afe0da07f607d944222984301c50f4c4f072
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.2 MB (224208346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5166b23bd2a925c05ea0e69315c5b3d1a7f2fa327eb8afbb3229f21cd45c5974`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 21 Jan 2021 03:49:03 GMT
ADD file:f6214eb5991df55aa5198d84442d6ddd28b67d4043d1832afba8b30e0249dcf5 in / 
# Thu, 21 Jan 2021 03:49:39 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:49:50 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:50:04 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:50:09 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 04:12:01 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Thu, 21 Jan 2021 04:17:06 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 04:17:22 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 21 Jan 2021 04:17:46 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 21 Jan 2021 04:18:01 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 21 Jan 2021 04:18:12 GMT
ARG BONITA_VERSION
# Thu, 21 Jan 2021 04:18:24 GMT
ARG BONITA_SHA256
# Thu, 21 Jan 2021 04:21:37 GMT
ARG BASE_URL
# Thu, 21 Jan 2021 04:21:45 GMT
ARG BONITA_URL
# Thu, 21 Jan 2021 04:21:50 GMT
ENV BONITA_VERSION=7.10.6
# Thu, 21 Jan 2021 04:21:57 GMT
ENV BONITA_SHA256=aaf61a044e7a8d9ec95d2b5d0c315a6d01d9c93ba01d753fcb008e2cfbbb725f
# Thu, 21 Jan 2021 04:22:07 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 21 Jan 2021 04:22:15 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.10.6/BonitaCommunity-7.10.6.zip
# Thu, 21 Jan 2021 04:22:24 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Thu, 21 Jan 2021 04:22:39 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Thu, 21 Jan 2021 04:22:50 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Thu, 21 Jan 2021 04:22:59 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Thu, 21 Jan 2021 04:23:04 GMT
VOLUME [/opt/bonita]
# Thu, 21 Jan 2021 04:23:06 GMT
COPY dir:46816633cc37ba9fd23af260c8c2384c15f3b4385b5752d6b42577967959f7f0 in /opt/files 
# Thu, 21 Jan 2021 04:23:08 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Thu, 21 Jan 2021 04:23:11 GMT
EXPOSE 8080
# Thu, 21 Jan 2021 04:23:20 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:e07786faec2ce77c08f20befe52a3eac52d983b0dfae9cb8d58dfa0ede0648e1`  
		Last Modified: Thu, 21 Jan 2021 03:54:37 GMT  
		Size: 30.4 MB (30422854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a41aaf71d5cf82fa1f9e11d2d352906ae135d0b216c665ed76ad9a8e1ce046`  
		Last Modified: Thu, 21 Jan 2021 03:54:30 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae0c92402f48f37a5d3bf1b351e5c6cbed6cec502dc9138f974a2e114c29ce4`  
		Last Modified: Thu, 21 Jan 2021 03:52:10 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8645f25ff36389214f3b0d20071cb514aa4decfad8510bbc0931a4dba6ddb02a`  
		Last Modified: Thu, 21 Jan 2021 04:30:43 GMT  
		Size: 95.3 MB (95257543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89068eb35b7bad5e3efa6b9f484a4d1958aeb9ddf3ef56a7458c7a9a7e233252`  
		Last Modified: Thu, 21 Jan 2021 04:30:24 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ea54e4343379e00e2cd0769514c3f76c70ab8c6d6a3ca67a8af0942c757503`  
		Last Modified: Thu, 21 Jan 2021 04:30:19 GMT  
		Size: 1.9 KB (1933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1766eadb2f05f4cff36ad426b71940f7c2b4e16578c604ec12e3f9eff547185c`  
		Last Modified: Thu, 21 Jan 2021 04:30:20 GMT  
		Size: 541.6 KB (541552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90a8d0f991d16fe5681a7754a0f0f18dab11987324470044b7cadf50673289b`  
		Last Modified: Thu, 21 Jan 2021 04:31:07 GMT  
		Size: 98.0 MB (97973962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3dc9e6fd1cfca24bd4766aeaaaeb99734a7b0f4b018c34d8ca1b0a6a98e2d58`  
		Last Modified: Thu, 21 Jan 2021 04:30:59 GMT  
		Size: 7.7 KB (7651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c79a199864b72a2a1b997b6d9aa41b6c6d6c56320e803c0bf192a92566f37b8`  
		Last Modified: Thu, 21 Jan 2021 04:31:00 GMT  
		Size: 1.7 KB (1652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.10.6`

```console
$ docker pull bonita@sha256:6ea3e56e6c525da95921d14525e7637fb1ccc8daec972696656a51d1c119d085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.10.6` - linux; amd64

```console
$ docker pull bonita@sha256:0a154b80d33af0abac0d3142da30765c96ab95be34e8e8c6da7848ce3c18342b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.0 MB (243978671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d57209e61995d778e22e5fbe0672dbaa5b9aa9eac3e989a85a8a6fd6cf57b31`
-	Default Command: `["\/opt\/files\/startup.sh"]`

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
# Thu, 04 Mar 2021 03:37:13 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Thu, 04 Mar 2021 03:38:03 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 03:38:05 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 04 Mar 2021 03:38:06 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 04 Mar 2021 03:38:08 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 04 Mar 2021 03:38:08 GMT
ARG BONITA_VERSION
# Thu, 04 Mar 2021 03:38:08 GMT
ARG BONITA_SHA256
# Thu, 04 Mar 2021 03:38:08 GMT
ARG BASE_URL
# Thu, 04 Mar 2021 03:38:08 GMT
ARG BONITA_URL
# Thu, 04 Mar 2021 03:38:09 GMT
ENV BONITA_VERSION=7.10.6
# Thu, 04 Mar 2021 03:38:09 GMT
ENV BONITA_SHA256=aaf61a044e7a8d9ec95d2b5d0c315a6d01d9c93ba01d753fcb008e2cfbbb725f
# Thu, 04 Mar 2021 03:38:09 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 04 Mar 2021 03:38:09 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.10.6/BonitaCommunity-7.10.6.zip
# Thu, 04 Mar 2021 03:38:10 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Thu, 04 Mar 2021 03:38:14 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Thu, 04 Mar 2021 03:38:16 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Thu, 04 Mar 2021 03:38:17 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Thu, 04 Mar 2021 03:38:17 GMT
VOLUME [/opt/bonita]
# Thu, 04 Mar 2021 03:38:18 GMT
COPY dir:46816633cc37ba9fd23af260c8c2384c15f3b4385b5752d6b42577967959f7f0 in /opt/files 
# Thu, 04 Mar 2021 03:38:18 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Thu, 04 Mar 2021 03:38:18 GMT
EXPOSE 8080
# Thu, 04 Mar 2021 03:38:18 GMT
CMD ["/opt/files/startup.sh"]
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
	-	`sha256:434195674b944c7b26c9fac11ba8af5effb5d5df21c92f0acb661f52acfc19c3`  
		Last Modified: Thu, 04 Mar 2021 03:40:09 GMT  
		Size: 118.7 MB (118709940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4718803d801e9af254f6577f1d42bb5c03dbd5fc2e52507a9d3aa6b90932223c`  
		Last Modified: Thu, 04 Mar 2021 03:39:48 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbbeba20b0c723911b9025634ab5278680111bee7cfa3a4791b6895b81a21ff3`  
		Last Modified: Thu, 04 Mar 2021 03:39:47 GMT  
		Size: 1.9 KB (1912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cd42a066bb8ea4fccdf5391d3ef7f13652718c06b2a466e5a12019537fc74`  
		Last Modified: Thu, 04 Mar 2021 03:39:47 GMT  
		Size: 572.4 KB (572375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5847de73dde7005b9b0e2df701ae4b09a815af48447f29f5eb58d6dbf6f4c0a5`  
		Last Modified: Thu, 04 Mar 2021 03:39:53 GMT  
		Size: 98.0 MB (97973911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa0477e7a6d5149e0e209d722efebed2d27cd8e2ed879df850dfda85929c84a`  
		Last Modified: Thu, 04 Mar 2021 03:39:48 GMT  
		Size: 7.6 KB (7626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19d2d4183d7bd50e6f85bd6e0d8a60eb5724c6a59ff4c2ecc359ad0b0a919e7`  
		Last Modified: Thu, 04 Mar 2021 03:39:47 GMT  
		Size: 1.6 KB (1626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.10.6` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:40332cdc79c1f2a8e5187f413b5b31b6bf9285de6cf3d4565ea1f0034714111a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.8 MB (215803468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f2fc251d722cfd66c393c630ad4075f49a6da4595f2530549d9656e2a9551c0`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 21 Jan 2021 03:49:23 GMT
ADD file:7d9bc01cf1f3757bf5fa308213a77aeb128883cc13616ff46b3da5b0e65b92f2 in / 
# Thu, 21 Jan 2021 03:49:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:49:29 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:49:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:49:32 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 05:25:47 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Thu, 21 Jan 2021 05:26:50 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 05:26:55 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 21 Jan 2021 05:26:58 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 21 Jan 2021 05:27:02 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 21 Jan 2021 05:27:02 GMT
ARG BONITA_VERSION
# Thu, 21 Jan 2021 05:27:03 GMT
ARG BONITA_SHA256
# Thu, 21 Jan 2021 05:27:53 GMT
ARG BASE_URL
# Thu, 21 Jan 2021 05:27:53 GMT
ARG BONITA_URL
# Thu, 21 Jan 2021 05:27:54 GMT
ENV BONITA_VERSION=7.10.6
# Thu, 21 Jan 2021 05:27:55 GMT
ENV BONITA_SHA256=aaf61a044e7a8d9ec95d2b5d0c315a6d01d9c93ba01d753fcb008e2cfbbb725f
# Thu, 21 Jan 2021 05:27:56 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 21 Jan 2021 05:27:56 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.10.6/BonitaCommunity-7.10.6.zip
# Thu, 21 Jan 2021 05:27:58 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Thu, 21 Jan 2021 05:28:02 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Thu, 21 Jan 2021 05:28:05 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Thu, 21 Jan 2021 05:28:08 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Thu, 21 Jan 2021 05:28:10 GMT
VOLUME [/opt/bonita]
# Thu, 21 Jan 2021 05:28:11 GMT
COPY dir:46816633cc37ba9fd23af260c8c2384c15f3b4385b5752d6b42577967959f7f0 in /opt/files 
# Thu, 21 Jan 2021 05:28:12 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Thu, 21 Jan 2021 05:28:12 GMT
EXPOSE 8080
# Thu, 21 Jan 2021 05:28:13 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:64e3fba066352e44a4c1eeb6caedc87c29b46f0a7b31e21a58183fc8370005bd`  
		Last Modified: Tue, 19 Jan 2021 00:25:17 GMT  
		Size: 23.7 MB (23732640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dbb433f451339aab734bb52e3df5b34cdea477f3f8e3aa32f7ac060bd852de2`  
		Last Modified: Thu, 21 Jan 2021 03:51:55 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3042a0d94b83caeb29bc20734c197130f58e14e86e8e6cdad8b768052bb563c`  
		Last Modified: Thu, 21 Jan 2021 03:51:54 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24336a54672e821e94fa257760b5e413b70629939ef726f3bb2eeab9c0601edd`  
		Last Modified: Thu, 21 Jan 2021 05:30:31 GMT  
		Size: 93.5 MB (93542646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:552fdcf45b6eb86bd7d48ed1e77374970ba298ec65a68788f8acd4f04c890222`  
		Last Modified: Thu, 21 Jan 2021 05:30:09 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50bd7f50264ee42d6837fbee45fe7973e89ddb3b535df67a436953fb351b725e`  
		Last Modified: Thu, 21 Jan 2021 05:30:07 GMT  
		Size: 1.9 KB (1914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df34d15f6edd642a516be0ee0bca1199f4e6b25fb8bd67bb12933531f2fb9e0a`  
		Last Modified: Thu, 21 Jan 2021 05:30:07 GMT  
		Size: 541.8 KB (541810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486b97b8751e5407605c4e2db22b52b00b3b348e354abe58a82a5ba2c3f77b8c`  
		Last Modified: Thu, 21 Jan 2021 05:30:50 GMT  
		Size: 98.0 MB (97973962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e947cc90fd2185eebfd07a00ef5f294d3c49192a1cb89062fa7a411b5f3a1c5`  
		Last Modified: Thu, 21 Jan 2021 05:30:44 GMT  
		Size: 7.7 KB (7650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d578899624ad3033f7d8488f9e8cf0653579ae3cb9fea080434e925710d1bc2a`  
		Last Modified: Thu, 21 Jan 2021 05:30:44 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.10.6` - linux; ppc64le

```console
$ docker pull bonita@sha256:9478c7d1bda23a0c277dffe5a490afe0da07f607d944222984301c50f4c4f072
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.2 MB (224208346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5166b23bd2a925c05ea0e69315c5b3d1a7f2fa327eb8afbb3229f21cd45c5974`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 21 Jan 2021 03:49:03 GMT
ADD file:f6214eb5991df55aa5198d84442d6ddd28b67d4043d1832afba8b30e0249dcf5 in / 
# Thu, 21 Jan 2021 03:49:39 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:49:50 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:50:04 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:50:09 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 04:12:01 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Thu, 21 Jan 2021 04:17:06 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 04:17:22 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 21 Jan 2021 04:17:46 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 21 Jan 2021 04:18:01 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 21 Jan 2021 04:18:12 GMT
ARG BONITA_VERSION
# Thu, 21 Jan 2021 04:18:24 GMT
ARG BONITA_SHA256
# Thu, 21 Jan 2021 04:21:37 GMT
ARG BASE_URL
# Thu, 21 Jan 2021 04:21:45 GMT
ARG BONITA_URL
# Thu, 21 Jan 2021 04:21:50 GMT
ENV BONITA_VERSION=7.10.6
# Thu, 21 Jan 2021 04:21:57 GMT
ENV BONITA_SHA256=aaf61a044e7a8d9ec95d2b5d0c315a6d01d9c93ba01d753fcb008e2cfbbb725f
# Thu, 21 Jan 2021 04:22:07 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 21 Jan 2021 04:22:15 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.10.6/BonitaCommunity-7.10.6.zip
# Thu, 21 Jan 2021 04:22:24 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Thu, 21 Jan 2021 04:22:39 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Thu, 21 Jan 2021 04:22:50 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Thu, 21 Jan 2021 04:22:59 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Thu, 21 Jan 2021 04:23:04 GMT
VOLUME [/opt/bonita]
# Thu, 21 Jan 2021 04:23:06 GMT
COPY dir:46816633cc37ba9fd23af260c8c2384c15f3b4385b5752d6b42577967959f7f0 in /opt/files 
# Thu, 21 Jan 2021 04:23:08 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Thu, 21 Jan 2021 04:23:11 GMT
EXPOSE 8080
# Thu, 21 Jan 2021 04:23:20 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:e07786faec2ce77c08f20befe52a3eac52d983b0dfae9cb8d58dfa0ede0648e1`  
		Last Modified: Thu, 21 Jan 2021 03:54:37 GMT  
		Size: 30.4 MB (30422854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a41aaf71d5cf82fa1f9e11d2d352906ae135d0b216c665ed76ad9a8e1ce046`  
		Last Modified: Thu, 21 Jan 2021 03:54:30 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae0c92402f48f37a5d3bf1b351e5c6cbed6cec502dc9138f974a2e114c29ce4`  
		Last Modified: Thu, 21 Jan 2021 03:52:10 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8645f25ff36389214f3b0d20071cb514aa4decfad8510bbc0931a4dba6ddb02a`  
		Last Modified: Thu, 21 Jan 2021 04:30:43 GMT  
		Size: 95.3 MB (95257543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89068eb35b7bad5e3efa6b9f484a4d1958aeb9ddf3ef56a7458c7a9a7e233252`  
		Last Modified: Thu, 21 Jan 2021 04:30:24 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ea54e4343379e00e2cd0769514c3f76c70ab8c6d6a3ca67a8af0942c757503`  
		Last Modified: Thu, 21 Jan 2021 04:30:19 GMT  
		Size: 1.9 KB (1933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1766eadb2f05f4cff36ad426b71940f7c2b4e16578c604ec12e3f9eff547185c`  
		Last Modified: Thu, 21 Jan 2021 04:30:20 GMT  
		Size: 541.6 KB (541552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90a8d0f991d16fe5681a7754a0f0f18dab11987324470044b7cadf50673289b`  
		Last Modified: Thu, 21 Jan 2021 04:31:07 GMT  
		Size: 98.0 MB (97973962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3dc9e6fd1cfca24bd4766aeaaaeb99734a7b0f4b018c34d8ca1b0a6a98e2d58`  
		Last Modified: Thu, 21 Jan 2021 04:30:59 GMT  
		Size: 7.7 KB (7651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c79a199864b72a2a1b997b6d9aa41b6c6d6c56320e803c0bf192a92566f37b8`  
		Last Modified: Thu, 21 Jan 2021 04:31:00 GMT  
		Size: 1.7 KB (1652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.11`

```console
$ docker pull bonita@sha256:86439c3a35bad2fd5748bf58ac2e75ac701c56801e4a9132e32e32fe0564c80b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.11` - linux; amd64

```console
$ docker pull bonita@sha256:37d60f9edc294825817f9b59e9fd20840a4d2c14118e4005f52a3d8bd9149715
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235824524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64c5080e92ae8d3762f043be32d9ea396ed1c917899318a904fd9ff5501f2aa0`
-	Default Command: `["\/opt\/files\/startup.sh"]`

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
# Thu, 04 Mar 2021 03:38:30 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 04 Mar 2021 03:38:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 03:38:56 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 04 Mar 2021 03:38:57 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 04 Mar 2021 03:38:58 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 04 Mar 2021 03:38:59 GMT
ARG BONITA_VERSION
# Thu, 04 Mar 2021 03:38:59 GMT
ARG BONITA_SHA256
# Thu, 04 Mar 2021 03:38:59 GMT
ARG BASE_URL
# Thu, 04 Mar 2021 03:38:59 GMT
ARG BONITA_URL
# Thu, 04 Mar 2021 03:38:59 GMT
ENV BONITA_VERSION=7.11.4
# Thu, 04 Mar 2021 03:39:00 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Thu, 04 Mar 2021 03:39:00 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Thu, 04 Mar 2021 03:39:00 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 04 Mar 2021 03:39:00 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Thu, 04 Mar 2021 03:39:01 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Thu, 04 Mar 2021 03:39:02 GMT
RUN mkdir /opt/files
# Thu, 04 Mar 2021 03:39:03 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Thu, 04 Mar 2021 03:39:07 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Thu, 04 Mar 2021 03:39:08 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Thu, 04 Mar 2021 03:39:10 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Thu, 04 Mar 2021 03:39:10 GMT
VOLUME [/opt/bonita]
# Thu, 04 Mar 2021 03:39:11 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 04 Mar 2021 03:39:11 GMT
EXPOSE 8080
# Thu, 04 Mar 2021 03:39:11 GMT
CMD ["/opt/files/startup.sh"]
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
	-	`sha256:0b013a5e6d745d8ddf229fc1b6efe515531408d68a38ccdfd19fe2734a796e20`  
		Last Modified: Thu, 04 Mar 2021 03:40:39 GMT  
		Size: 95.2 MB (95182489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43c3d83e550e3c03dbf7d5be4813516f132b770f495793ae7ec767850a867c0`  
		Last Modified: Thu, 04 Mar 2021 03:40:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e491464ad3b52ebf5550aee453151a66f342c6fae6fd17dddaa8ecfd52de0eb`  
		Last Modified: Thu, 04 Mar 2021 03:40:19 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ac5a46d0b9f41259cbbd28b965b962ac61af24a85d5940ac903bd1e53ec4a1`  
		Last Modified: Thu, 04 Mar 2021 03:40:19 GMT  
		Size: 572.4 KB (572376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493c7f5a5149ae08be5a29d0ce0d4be54d0b005a06a6252507e940c453e2d338`  
		Last Modified: Thu, 04 Mar 2021 03:40:18 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291ba264f2c139f812d770234286bcbe7090083d9fc0e14a978c67b3d857e845`  
		Last Modified: Thu, 04 Mar 2021 03:40:18 GMT  
		Size: 6.9 KB (6862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62cd0e364923c8af12121d0a201f09c308715cd96682ea734faca351fd9ae05`  
		Last Modified: Thu, 04 Mar 2021 03:40:25 GMT  
		Size: 113.3 MB (113347830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34417d1ab78ffb701465821fef5ae18a0a9b19441b60990995013d03cdd892d`  
		Last Modified: Thu, 04 Mar 2021 03:40:19 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:6e57ebde9af7ab516053917af2b604d205385e92d2664c472bddd4188d8eaef8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222931988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29629cffca39c180f123375454535422e423b29d3304a2ff49799d494568d3ad`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 21 Jan 2021 03:49:23 GMT
ADD file:7d9bc01cf1f3757bf5fa308213a77aeb128883cc13616ff46b3da5b0e65b92f2 in / 
# Thu, 21 Jan 2021 03:49:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:49:29 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:49:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:49:32 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 05:28:20 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 21 Jan 2021 05:29:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 05:29:09 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 21 Jan 2021 05:29:11 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 21 Jan 2021 05:29:13 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 21 Jan 2021 05:29:14 GMT
ARG BONITA_VERSION
# Thu, 21 Jan 2021 05:29:15 GMT
ARG BONITA_SHA256
# Thu, 21 Jan 2021 05:29:16 GMT
ARG BASE_URL
# Thu, 21 Jan 2021 05:29:16 GMT
ARG BONITA_URL
# Thu, 21 Jan 2021 05:29:17 GMT
ENV BONITA_VERSION=7.11.4
# Thu, 21 Jan 2021 05:29:18 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Thu, 21 Jan 2021 05:29:18 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Thu, 21 Jan 2021 05:29:19 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 21 Jan 2021 05:29:20 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Thu, 21 Jan 2021 05:29:21 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Thu, 21 Jan 2021 05:29:24 GMT
RUN mkdir /opt/files
# Thu, 21 Jan 2021 05:29:25 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Thu, 21 Jan 2021 05:29:29 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Thu, 21 Jan 2021 05:29:32 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Thu, 21 Jan 2021 05:29:35 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Thu, 21 Jan 2021 05:29:39 GMT
VOLUME [/opt/bonita]
# Thu, 21 Jan 2021 05:29:40 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 21 Jan 2021 05:29:41 GMT
EXPOSE 8080
# Thu, 21 Jan 2021 05:29:41 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:64e3fba066352e44a4c1eeb6caedc87c29b46f0a7b31e21a58183fc8370005bd`  
		Last Modified: Tue, 19 Jan 2021 00:25:17 GMT  
		Size: 23.7 MB (23732640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dbb433f451339aab734bb52e3df5b34cdea477f3f8e3aa32f7ac060bd852de2`  
		Last Modified: Thu, 21 Jan 2021 03:51:55 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3042a0d94b83caeb29bc20734c197130f58e14e86e8e6cdad8b768052bb563c`  
		Last Modified: Thu, 21 Jan 2021 03:51:54 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8df92044c4b506076de6abc24afe1d5eac83a9e6cc5fb97a725daea7b5fb742`  
		Last Modified: Thu, 21 Jan 2021 05:31:28 GMT  
		Size: 85.3 MB (85297873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1abc3fcd55457d935f9da38456f79f5f4c394ff39f5f0bf92deb550a9c5d5a8`  
		Last Modified: Thu, 21 Jan 2021 05:31:05 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb17a62d1dc9db97a189188b6263b79601d869b5f3813597d9c9990e9b1e67b0`  
		Last Modified: Thu, 21 Jan 2021 05:31:04 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af2268a1d88611b9add2dc44af567d1d121e316d036e49cbd1b3f54717c4019`  
		Last Modified: Thu, 21 Jan 2021 05:31:03 GMT  
		Size: 541.8 KB (541813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7011bc1e3e2385dd497f2541b214c8e259921b44a3bbe11ae2f8454ff5c2f05`  
		Last Modified: Thu, 21 Jan 2021 05:31:02 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc233ea535576f5c2dd12a795b89a08cb205eb4c2c8b22c598cc7807ed768fc`  
		Last Modified: Thu, 21 Jan 2021 05:31:03 GMT  
		Size: 6.9 KB (6888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a3e84fbef1056c060b4c5c04da16a9d663008e1caa29d4bebc0c0e04089d866`  
		Last Modified: Thu, 21 Jan 2021 05:31:24 GMT  
		Size: 113.3 MB (113347830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ced7ae2e5ea92f0a4d7e0884dd740f3a3714133ab4b497e1b4d49b7c0adec34`  
		Last Modified: Thu, 21 Jan 2021 05:31:03 GMT  
		Size: 1.7 KB (1713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11` - linux; ppc64le

```console
$ docker pull bonita@sha256:1775b31bd091990c8ee76d8008a159f6c4fdfffa75e296fcc182e834a21544d1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230241157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5fe55d84a7f19877b8d13a999ae20f712b89fc2e506fa927710ba8b61013d12`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 21 Jan 2021 03:49:03 GMT
ADD file:f6214eb5991df55aa5198d84442d6ddd28b67d4043d1832afba8b30e0249dcf5 in / 
# Thu, 21 Jan 2021 03:49:39 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:49:50 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:50:04 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:50:09 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 04:23:39 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 21 Jan 2021 04:27:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 04:28:04 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 21 Jan 2021 04:28:10 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 21 Jan 2021 04:28:18 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 21 Jan 2021 04:28:22 GMT
ARG BONITA_VERSION
# Thu, 21 Jan 2021 04:28:26 GMT
ARG BONITA_SHA256
# Thu, 21 Jan 2021 04:28:30 GMT
ARG BASE_URL
# Thu, 21 Jan 2021 04:28:32 GMT
ARG BONITA_URL
# Thu, 21 Jan 2021 04:28:37 GMT
ENV BONITA_VERSION=7.11.4
# Thu, 21 Jan 2021 04:28:41 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Thu, 21 Jan 2021 04:28:44 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Thu, 21 Jan 2021 04:28:47 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 21 Jan 2021 04:28:49 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Thu, 21 Jan 2021 04:28:55 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Thu, 21 Jan 2021 04:29:05 GMT
RUN mkdir /opt/files
# Thu, 21 Jan 2021 04:29:07 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Thu, 21 Jan 2021 04:29:23 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Thu, 21 Jan 2021 04:29:30 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Thu, 21 Jan 2021 04:29:40 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Thu, 21 Jan 2021 04:29:43 GMT
VOLUME [/opt/bonita]
# Thu, 21 Jan 2021 04:29:51 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 21 Jan 2021 04:29:55 GMT
EXPOSE 8080
# Thu, 21 Jan 2021 04:29:58 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:e07786faec2ce77c08f20befe52a3eac52d983b0dfae9cb8d58dfa0ede0648e1`  
		Last Modified: Thu, 21 Jan 2021 03:54:37 GMT  
		Size: 30.4 MB (30422854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a41aaf71d5cf82fa1f9e11d2d352906ae135d0b216c665ed76ad9a8e1ce046`  
		Last Modified: Thu, 21 Jan 2021 03:54:30 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae0c92402f48f37a5d3bf1b351e5c6cbed6cec502dc9138f974a2e114c29ce4`  
		Last Modified: Thu, 21 Jan 2021 03:52:10 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b13b45af58aa295d275be3fb2ee2cdae02906032f23429acfe6e350037d8ab93`  
		Last Modified: Thu, 21 Jan 2021 04:31:44 GMT  
		Size: 85.9 MB (85917102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85b382bfd13fccaece5a5a9972badb85c89b4e5d49d62b01a5c56586d69dff55`  
		Last Modified: Thu, 21 Jan 2021 04:31:24 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b765dbe8b65a01b5e7a6c6bcf266a3f252f9ecab42044078374cd592222b75c1`  
		Last Modified: Thu, 21 Jan 2021 04:31:25 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9bc546cf88c8886a652c41a34d2b48be1bdf5a74182087aea7df14653843a8`  
		Last Modified: Thu, 21 Jan 2021 04:31:21 GMT  
		Size: 541.5 KB (541539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c93abec29ddc090408885bdbc819a7f8683da1f890a9715fb57444c54a13d7`  
		Last Modified: Thu, 21 Jan 2021 04:31:21 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58af7537f4df108a07f0bee0e14a66013e96015a9c6a6158c3781fe7b67b8370`  
		Last Modified: Thu, 21 Jan 2021 04:31:21 GMT  
		Size: 6.9 KB (6894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:247670b29b11f8ee3a4863d091ecc7144ccbd59c145ea12b2a9a276df91e24a7`  
		Last Modified: Thu, 21 Jan 2021 04:31:30 GMT  
		Size: 113.3 MB (113347828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:645d94b6347d9ee25f4b3df7bdef0a0864af5427b7fd61aaf5dad4c479fc54d3`  
		Last Modified: Thu, 21 Jan 2021 04:31:20 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.11.4`

```console
$ docker pull bonita@sha256:86439c3a35bad2fd5748bf58ac2e75ac701c56801e4a9132e32e32fe0564c80b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.11.4` - linux; amd64

```console
$ docker pull bonita@sha256:37d60f9edc294825817f9b59e9fd20840a4d2c14118e4005f52a3d8bd9149715
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235824524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64c5080e92ae8d3762f043be32d9ea396ed1c917899318a904fd9ff5501f2aa0`
-	Default Command: `["\/opt\/files\/startup.sh"]`

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
# Thu, 04 Mar 2021 03:38:30 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 04 Mar 2021 03:38:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 03:38:56 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 04 Mar 2021 03:38:57 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 04 Mar 2021 03:38:58 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 04 Mar 2021 03:38:59 GMT
ARG BONITA_VERSION
# Thu, 04 Mar 2021 03:38:59 GMT
ARG BONITA_SHA256
# Thu, 04 Mar 2021 03:38:59 GMT
ARG BASE_URL
# Thu, 04 Mar 2021 03:38:59 GMT
ARG BONITA_URL
# Thu, 04 Mar 2021 03:38:59 GMT
ENV BONITA_VERSION=7.11.4
# Thu, 04 Mar 2021 03:39:00 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Thu, 04 Mar 2021 03:39:00 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Thu, 04 Mar 2021 03:39:00 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 04 Mar 2021 03:39:00 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Thu, 04 Mar 2021 03:39:01 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Thu, 04 Mar 2021 03:39:02 GMT
RUN mkdir /opt/files
# Thu, 04 Mar 2021 03:39:03 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Thu, 04 Mar 2021 03:39:07 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Thu, 04 Mar 2021 03:39:08 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Thu, 04 Mar 2021 03:39:10 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Thu, 04 Mar 2021 03:39:10 GMT
VOLUME [/opt/bonita]
# Thu, 04 Mar 2021 03:39:11 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 04 Mar 2021 03:39:11 GMT
EXPOSE 8080
# Thu, 04 Mar 2021 03:39:11 GMT
CMD ["/opt/files/startup.sh"]
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
	-	`sha256:0b013a5e6d745d8ddf229fc1b6efe515531408d68a38ccdfd19fe2734a796e20`  
		Last Modified: Thu, 04 Mar 2021 03:40:39 GMT  
		Size: 95.2 MB (95182489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43c3d83e550e3c03dbf7d5be4813516f132b770f495793ae7ec767850a867c0`  
		Last Modified: Thu, 04 Mar 2021 03:40:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e491464ad3b52ebf5550aee453151a66f342c6fae6fd17dddaa8ecfd52de0eb`  
		Last Modified: Thu, 04 Mar 2021 03:40:19 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ac5a46d0b9f41259cbbd28b965b962ac61af24a85d5940ac903bd1e53ec4a1`  
		Last Modified: Thu, 04 Mar 2021 03:40:19 GMT  
		Size: 572.4 KB (572376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493c7f5a5149ae08be5a29d0ce0d4be54d0b005a06a6252507e940c453e2d338`  
		Last Modified: Thu, 04 Mar 2021 03:40:18 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291ba264f2c139f812d770234286bcbe7090083d9fc0e14a978c67b3d857e845`  
		Last Modified: Thu, 04 Mar 2021 03:40:18 GMT  
		Size: 6.9 KB (6862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62cd0e364923c8af12121d0a201f09c308715cd96682ea734faca351fd9ae05`  
		Last Modified: Thu, 04 Mar 2021 03:40:25 GMT  
		Size: 113.3 MB (113347830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34417d1ab78ffb701465821fef5ae18a0a9b19441b60990995013d03cdd892d`  
		Last Modified: Thu, 04 Mar 2021 03:40:19 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11.4` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:6e57ebde9af7ab516053917af2b604d205385e92d2664c472bddd4188d8eaef8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222931988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29629cffca39c180f123375454535422e423b29d3304a2ff49799d494568d3ad`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 21 Jan 2021 03:49:23 GMT
ADD file:7d9bc01cf1f3757bf5fa308213a77aeb128883cc13616ff46b3da5b0e65b92f2 in / 
# Thu, 21 Jan 2021 03:49:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:49:29 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:49:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:49:32 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 05:28:20 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 21 Jan 2021 05:29:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 05:29:09 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 21 Jan 2021 05:29:11 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 21 Jan 2021 05:29:13 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 21 Jan 2021 05:29:14 GMT
ARG BONITA_VERSION
# Thu, 21 Jan 2021 05:29:15 GMT
ARG BONITA_SHA256
# Thu, 21 Jan 2021 05:29:16 GMT
ARG BASE_URL
# Thu, 21 Jan 2021 05:29:16 GMT
ARG BONITA_URL
# Thu, 21 Jan 2021 05:29:17 GMT
ENV BONITA_VERSION=7.11.4
# Thu, 21 Jan 2021 05:29:18 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Thu, 21 Jan 2021 05:29:18 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Thu, 21 Jan 2021 05:29:19 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 21 Jan 2021 05:29:20 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Thu, 21 Jan 2021 05:29:21 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Thu, 21 Jan 2021 05:29:24 GMT
RUN mkdir /opt/files
# Thu, 21 Jan 2021 05:29:25 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Thu, 21 Jan 2021 05:29:29 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Thu, 21 Jan 2021 05:29:32 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Thu, 21 Jan 2021 05:29:35 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Thu, 21 Jan 2021 05:29:39 GMT
VOLUME [/opt/bonita]
# Thu, 21 Jan 2021 05:29:40 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 21 Jan 2021 05:29:41 GMT
EXPOSE 8080
# Thu, 21 Jan 2021 05:29:41 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:64e3fba066352e44a4c1eeb6caedc87c29b46f0a7b31e21a58183fc8370005bd`  
		Last Modified: Tue, 19 Jan 2021 00:25:17 GMT  
		Size: 23.7 MB (23732640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dbb433f451339aab734bb52e3df5b34cdea477f3f8e3aa32f7ac060bd852de2`  
		Last Modified: Thu, 21 Jan 2021 03:51:55 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3042a0d94b83caeb29bc20734c197130f58e14e86e8e6cdad8b768052bb563c`  
		Last Modified: Thu, 21 Jan 2021 03:51:54 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8df92044c4b506076de6abc24afe1d5eac83a9e6cc5fb97a725daea7b5fb742`  
		Last Modified: Thu, 21 Jan 2021 05:31:28 GMT  
		Size: 85.3 MB (85297873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1abc3fcd55457d935f9da38456f79f5f4c394ff39f5f0bf92deb550a9c5d5a8`  
		Last Modified: Thu, 21 Jan 2021 05:31:05 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb17a62d1dc9db97a189188b6263b79601d869b5f3813597d9c9990e9b1e67b0`  
		Last Modified: Thu, 21 Jan 2021 05:31:04 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af2268a1d88611b9add2dc44af567d1d121e316d036e49cbd1b3f54717c4019`  
		Last Modified: Thu, 21 Jan 2021 05:31:03 GMT  
		Size: 541.8 KB (541813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7011bc1e3e2385dd497f2541b214c8e259921b44a3bbe11ae2f8454ff5c2f05`  
		Last Modified: Thu, 21 Jan 2021 05:31:02 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc233ea535576f5c2dd12a795b89a08cb205eb4c2c8b22c598cc7807ed768fc`  
		Last Modified: Thu, 21 Jan 2021 05:31:03 GMT  
		Size: 6.9 KB (6888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a3e84fbef1056c060b4c5c04da16a9d663008e1caa29d4bebc0c0e04089d866`  
		Last Modified: Thu, 21 Jan 2021 05:31:24 GMT  
		Size: 113.3 MB (113347830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ced7ae2e5ea92f0a4d7e0884dd740f3a3714133ab4b497e1b4d49b7c0adec34`  
		Last Modified: Thu, 21 Jan 2021 05:31:03 GMT  
		Size: 1.7 KB (1713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11.4` - linux; ppc64le

```console
$ docker pull bonita@sha256:1775b31bd091990c8ee76d8008a159f6c4fdfffa75e296fcc182e834a21544d1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230241157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5fe55d84a7f19877b8d13a999ae20f712b89fc2e506fa927710ba8b61013d12`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 21 Jan 2021 03:49:03 GMT
ADD file:f6214eb5991df55aa5198d84442d6ddd28b67d4043d1832afba8b30e0249dcf5 in / 
# Thu, 21 Jan 2021 03:49:39 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:49:50 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:50:04 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:50:09 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 04:23:39 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 21 Jan 2021 04:27:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 04:28:04 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 21 Jan 2021 04:28:10 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 21 Jan 2021 04:28:18 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 21 Jan 2021 04:28:22 GMT
ARG BONITA_VERSION
# Thu, 21 Jan 2021 04:28:26 GMT
ARG BONITA_SHA256
# Thu, 21 Jan 2021 04:28:30 GMT
ARG BASE_URL
# Thu, 21 Jan 2021 04:28:32 GMT
ARG BONITA_URL
# Thu, 21 Jan 2021 04:28:37 GMT
ENV BONITA_VERSION=7.11.4
# Thu, 21 Jan 2021 04:28:41 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Thu, 21 Jan 2021 04:28:44 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Thu, 21 Jan 2021 04:28:47 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 21 Jan 2021 04:28:49 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Thu, 21 Jan 2021 04:28:55 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Thu, 21 Jan 2021 04:29:05 GMT
RUN mkdir /opt/files
# Thu, 21 Jan 2021 04:29:07 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Thu, 21 Jan 2021 04:29:23 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Thu, 21 Jan 2021 04:29:30 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Thu, 21 Jan 2021 04:29:40 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Thu, 21 Jan 2021 04:29:43 GMT
VOLUME [/opt/bonita]
# Thu, 21 Jan 2021 04:29:51 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 21 Jan 2021 04:29:55 GMT
EXPOSE 8080
# Thu, 21 Jan 2021 04:29:58 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:e07786faec2ce77c08f20befe52a3eac52d983b0dfae9cb8d58dfa0ede0648e1`  
		Last Modified: Thu, 21 Jan 2021 03:54:37 GMT  
		Size: 30.4 MB (30422854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a41aaf71d5cf82fa1f9e11d2d352906ae135d0b216c665ed76ad9a8e1ce046`  
		Last Modified: Thu, 21 Jan 2021 03:54:30 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae0c92402f48f37a5d3bf1b351e5c6cbed6cec502dc9138f974a2e114c29ce4`  
		Last Modified: Thu, 21 Jan 2021 03:52:10 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b13b45af58aa295d275be3fb2ee2cdae02906032f23429acfe6e350037d8ab93`  
		Last Modified: Thu, 21 Jan 2021 04:31:44 GMT  
		Size: 85.9 MB (85917102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85b382bfd13fccaece5a5a9972badb85c89b4e5d49d62b01a5c56586d69dff55`  
		Last Modified: Thu, 21 Jan 2021 04:31:24 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b765dbe8b65a01b5e7a6c6bcf266a3f252f9ecab42044078374cd592222b75c1`  
		Last Modified: Thu, 21 Jan 2021 04:31:25 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9bc546cf88c8886a652c41a34d2b48be1bdf5a74182087aea7df14653843a8`  
		Last Modified: Thu, 21 Jan 2021 04:31:21 GMT  
		Size: 541.5 KB (541539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c93abec29ddc090408885bdbc819a7f8683da1f890a9715fb57444c54a13d7`  
		Last Modified: Thu, 21 Jan 2021 04:31:21 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58af7537f4df108a07f0bee0e14a66013e96015a9c6a6158c3781fe7b67b8370`  
		Last Modified: Thu, 21 Jan 2021 04:31:21 GMT  
		Size: 6.9 KB (6894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:247670b29b11f8ee3a4863d091ecc7144ccbd59c145ea12b2a9a276df91e24a7`  
		Last Modified: Thu, 21 Jan 2021 04:31:30 GMT  
		Size: 113.3 MB (113347828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:645d94b6347d9ee25f4b3df7bdef0a0864af5427b7fd61aaf5dad4c479fc54d3`  
		Last Modified: Thu, 21 Jan 2021 04:31:20 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.12`

```console
$ docker pull bonita@sha256:92023653b15e0dde13c5a796f799122c47fc02865749ac63473626bacb658239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.12` - linux; amd64

```console
$ docker pull bonita@sha256:acb5236fefd92ff819cccce8ff039bfcee49d3ffd8b8408ec9eb86e1e044034d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.9 MB (238892145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:187e939000b59a7d68f188b581df9d3cae03e73cb682657a582674e0c8c29fc2`
-	Default Command: `["\/opt\/files\/startup.sh"]`

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
# Thu, 04 Mar 2021 03:38:30 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 04 Mar 2021 03:38:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 03:38:56 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 04 Mar 2021 03:38:57 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 04 Mar 2021 03:38:58 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 04 Mar 2021 03:38:59 GMT
ARG BONITA_VERSION
# Thu, 04 Mar 2021 03:39:17 GMT
ARG BRANDING_VERSION
# Thu, 04 Mar 2021 03:39:17 GMT
ARG BONITA_SHA256
# Thu, 04 Mar 2021 03:39:17 GMT
ARG BASE_URL
# Thu, 04 Mar 2021 03:39:17 GMT
ARG BONITA_URL
# Thu, 04 Mar 2021 03:39:18 GMT
ENV BONITA_VERSION=7.12.1
# Thu, 04 Mar 2021 03:39:18 GMT
ENV BRANDING_VERSION=2021.1
# Thu, 04 Mar 2021 03:39:18 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Thu, 04 Mar 2021 03:39:18 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Thu, 04 Mar 2021 03:39:18 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 04 Mar 2021 03:39:19 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Thu, 04 Mar 2021 03:39:20 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Thu, 04 Mar 2021 03:39:21 GMT
RUN mkdir /opt/files
# Thu, 04 Mar 2021 03:39:21 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Thu, 04 Mar 2021 03:39:26 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Thu, 04 Mar 2021 03:39:29 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Thu, 04 Mar 2021 03:39:31 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Thu, 04 Mar 2021 03:39:31 GMT
VOLUME [/opt/bonita]
# Thu, 04 Mar 2021 03:39:32 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 04 Mar 2021 03:39:32 GMT
EXPOSE 8080
# Thu, 04 Mar 2021 03:39:32 GMT
CMD ["/opt/files/startup.sh"]
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
	-	`sha256:0b013a5e6d745d8ddf229fc1b6efe515531408d68a38ccdfd19fe2734a796e20`  
		Last Modified: Thu, 04 Mar 2021 03:40:39 GMT  
		Size: 95.2 MB (95182489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43c3d83e550e3c03dbf7d5be4813516f132b770f495793ae7ec767850a867c0`  
		Last Modified: Thu, 04 Mar 2021 03:40:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e491464ad3b52ebf5550aee453151a66f342c6fae6fd17dddaa8ecfd52de0eb`  
		Last Modified: Thu, 04 Mar 2021 03:40:19 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ac5a46d0b9f41259cbbd28b965b962ac61af24a85d5940ac903bd1e53ec4a1`  
		Last Modified: Thu, 04 Mar 2021 03:40:19 GMT  
		Size: 572.4 KB (572376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d472c4128821436fa9d86e73569e07fc23ad4f59a21e2fccfcd1ee9e9c020b85`  
		Last Modified: Thu, 04 Mar 2021 03:40:45 GMT  
		Size: 112.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a35d3dfa6026e7fa52e17e9e231a17fbd844b63b8d7f0272216e59cd56bff4`  
		Last Modified: Thu, 04 Mar 2021 03:40:45 GMT  
		Size: 6.9 KB (6916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeed78bcae57a07524cd258132b6af9e23f9ecc6785be1f5f694755051ecf8be`  
		Last Modified: Thu, 04 Mar 2021 03:40:51 GMT  
		Size: 116.4 MB (116415402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c3e90c609477ff5a3252818b53a8e93c79ce128be2829b763ed5019a1c5688`  
		Last Modified: Thu, 04 Mar 2021 03:40:45 GMT  
		Size: 1.7 KB (1683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:042b27c155776c49fa827a611e68600e3ab7616ae5be3bbe45c57e5f8c41a4d8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.0 MB (225999606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1473c8d2979e05f1c6fe37e1c2ef0c1c3f0d01b1d9b043222c585bd2f204ea03`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 21 Jan 2021 03:49:23 GMT
ADD file:7d9bc01cf1f3757bf5fa308213a77aeb128883cc13616ff46b3da5b0e65b92f2 in / 
# Thu, 21 Jan 2021 03:49:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:49:29 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:49:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:49:32 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 05:28:20 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 21 Jan 2021 05:29:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 05:29:09 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 21 Jan 2021 05:29:11 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 21 Jan 2021 05:29:13 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 21 Jan 2021 05:29:14 GMT
ARG BONITA_VERSION
# Sat, 30 Jan 2021 00:53:50 GMT
ARG BRANDING_VERSION
# Sat, 30 Jan 2021 00:53:50 GMT
ARG BONITA_SHA256
# Sat, 30 Jan 2021 00:53:51 GMT
ARG BASE_URL
# Sat, 30 Jan 2021 00:53:51 GMT
ARG BONITA_URL
# Sat, 30 Jan 2021 00:53:52 GMT
ENV BONITA_VERSION=7.12.1
# Sat, 30 Jan 2021 00:53:53 GMT
ENV BRANDING_VERSION=2021.1
# Sat, 30 Jan 2021 00:53:53 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Sat, 30 Jan 2021 00:53:54 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Sat, 30 Jan 2021 00:53:54 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 30 Jan 2021 00:53:55 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Sat, 30 Jan 2021 00:53:57 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Sat, 30 Jan 2021 00:53:59 GMT
RUN mkdir /opt/files
# Sat, 30 Jan 2021 00:54:00 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Sat, 30 Jan 2021 00:54:06 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Sat, 30 Jan 2021 00:54:08 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Sat, 30 Jan 2021 00:54:11 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Sat, 30 Jan 2021 00:54:12 GMT
VOLUME [/opt/bonita]
# Sat, 30 Jan 2021 00:54:12 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Sat, 30 Jan 2021 00:54:13 GMT
EXPOSE 8080
# Sat, 30 Jan 2021 00:54:14 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:64e3fba066352e44a4c1eeb6caedc87c29b46f0a7b31e21a58183fc8370005bd`  
		Last Modified: Tue, 19 Jan 2021 00:25:17 GMT  
		Size: 23.7 MB (23732640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dbb433f451339aab734bb52e3df5b34cdea477f3f8e3aa32f7ac060bd852de2`  
		Last Modified: Thu, 21 Jan 2021 03:51:55 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3042a0d94b83caeb29bc20734c197130f58e14e86e8e6cdad8b768052bb563c`  
		Last Modified: Thu, 21 Jan 2021 03:51:54 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8df92044c4b506076de6abc24afe1d5eac83a9e6cc5fb97a725daea7b5fb742`  
		Last Modified: Thu, 21 Jan 2021 05:31:28 GMT  
		Size: 85.3 MB (85297873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1abc3fcd55457d935f9da38456f79f5f4c394ff39f5f0bf92deb550a9c5d5a8`  
		Last Modified: Thu, 21 Jan 2021 05:31:05 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb17a62d1dc9db97a189188b6263b79601d869b5f3813597d9c9990e9b1e67b0`  
		Last Modified: Thu, 21 Jan 2021 05:31:04 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af2268a1d88611b9add2dc44af567d1d121e316d036e49cbd1b3f54717c4019`  
		Last Modified: Thu, 21 Jan 2021 05:31:03 GMT  
		Size: 541.8 KB (541813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a6d9f507c165d2c3713ddc71f40686f7efab71e36563b00a38df6544f734a9`  
		Last Modified: Sat, 30 Jan 2021 00:54:31 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e96b3ed213aa787365c4954d6c9d9f0f6339011bb25c1da83b930936e897408f`  
		Last Modified: Sat, 30 Jan 2021 00:54:31 GMT  
		Size: 6.9 KB (6946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d407eacd2633e2d566bbdbc12ca4a0bfb1598bc401e81b0c7b2ac5789018614c`  
		Last Modified: Sat, 30 Jan 2021 00:54:41 GMT  
		Size: 116.4 MB (116415398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8263bbe0ad9c06ee5e05b8540e8b539f69ce8f36cd16c611f40d2a27977da5`  
		Last Modified: Sat, 30 Jan 2021 00:54:31 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12` - linux; ppc64le

```console
$ docker pull bonita@sha256:7cbc79ac9276eeb9ed45b37e7460eb8b82cd17ee65bf79366743255784a8fed5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.3 MB (233308791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2deb92cacf66527c2fdde8cdd3931695079b54e53a5882fc939be196f3fc36c`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 21 Jan 2021 03:49:03 GMT
ADD file:f6214eb5991df55aa5198d84442d6ddd28b67d4043d1832afba8b30e0249dcf5 in / 
# Thu, 21 Jan 2021 03:49:39 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:49:50 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:50:04 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:50:09 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 04:23:39 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 21 Jan 2021 04:27:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 04:28:04 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 21 Jan 2021 04:28:10 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 21 Jan 2021 04:28:18 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 21 Jan 2021 04:28:22 GMT
ARG BONITA_VERSION
# Sat, 30 Jan 2021 01:47:09 GMT
ARG BRANDING_VERSION
# Sat, 30 Jan 2021 01:47:17 GMT
ARG BONITA_SHA256
# Sat, 30 Jan 2021 01:47:23 GMT
ARG BASE_URL
# Sat, 30 Jan 2021 01:47:32 GMT
ARG BONITA_URL
# Sat, 30 Jan 2021 01:47:38 GMT
ENV BONITA_VERSION=7.12.1
# Sat, 30 Jan 2021 01:47:46 GMT
ENV BRANDING_VERSION=2021.1
# Sat, 30 Jan 2021 01:48:02 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Sat, 30 Jan 2021 01:48:07 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Sat, 30 Jan 2021 01:48:11 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 30 Jan 2021 01:48:13 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Sat, 30 Jan 2021 01:48:30 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Sat, 30 Jan 2021 01:48:55 GMT
RUN mkdir /opt/files
# Sat, 30 Jan 2021 01:48:59 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Sat, 30 Jan 2021 01:49:27 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Sat, 30 Jan 2021 01:49:41 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Sat, 30 Jan 2021 01:49:52 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Sat, 30 Jan 2021 01:49:57 GMT
VOLUME [/opt/bonita]
# Sat, 30 Jan 2021 01:50:00 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Sat, 30 Jan 2021 01:50:08 GMT
EXPOSE 8080
# Sat, 30 Jan 2021 01:50:13 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:e07786faec2ce77c08f20befe52a3eac52d983b0dfae9cb8d58dfa0ede0648e1`  
		Last Modified: Thu, 21 Jan 2021 03:54:37 GMT  
		Size: 30.4 MB (30422854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a41aaf71d5cf82fa1f9e11d2d352906ae135d0b216c665ed76ad9a8e1ce046`  
		Last Modified: Thu, 21 Jan 2021 03:54:30 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae0c92402f48f37a5d3bf1b351e5c6cbed6cec502dc9138f974a2e114c29ce4`  
		Last Modified: Thu, 21 Jan 2021 03:52:10 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b13b45af58aa295d275be3fb2ee2cdae02906032f23429acfe6e350037d8ab93`  
		Last Modified: Thu, 21 Jan 2021 04:31:44 GMT  
		Size: 85.9 MB (85917102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85b382bfd13fccaece5a5a9972badb85c89b4e5d49d62b01a5c56586d69dff55`  
		Last Modified: Thu, 21 Jan 2021 04:31:24 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b765dbe8b65a01b5e7a6c6bcf266a3f252f9ecab42044078374cd592222b75c1`  
		Last Modified: Thu, 21 Jan 2021 04:31:25 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9bc546cf88c8886a652c41a34d2b48be1bdf5a74182087aea7df14653843a8`  
		Last Modified: Thu, 21 Jan 2021 04:31:21 GMT  
		Size: 541.5 KB (541539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3328d3e249051dfe4783d885b91ec5874d8d654b2c198cc6e62b5eee230942bf`  
		Last Modified: Sat, 30 Jan 2021 01:50:42 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0341326e395d84e7152c652f6370e970564a985e74835fe94d52123709c5ae13`  
		Last Modified: Sat, 30 Jan 2021 01:50:42 GMT  
		Size: 7.0 KB (6950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b610564454d7cbfa5e7c6d19b44df37a3ff995fc38607f6154903eb2fde0914`  
		Last Modified: Sat, 30 Jan 2021 01:50:52 GMT  
		Size: 116.4 MB (116415407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06136d8ff274d12b9e1962bd89095c8930d5f735cb50f3942ae371b5128ff1af`  
		Last Modified: Sat, 30 Jan 2021 01:50:43 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.12.1`

```console
$ docker pull bonita@sha256:92023653b15e0dde13c5a796f799122c47fc02865749ac63473626bacb658239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.12.1` - linux; amd64

```console
$ docker pull bonita@sha256:acb5236fefd92ff819cccce8ff039bfcee49d3ffd8b8408ec9eb86e1e044034d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.9 MB (238892145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:187e939000b59a7d68f188b581df9d3cae03e73cb682657a582674e0c8c29fc2`
-	Default Command: `["\/opt\/files\/startup.sh"]`

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
# Thu, 04 Mar 2021 03:38:30 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 04 Mar 2021 03:38:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 03:38:56 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 04 Mar 2021 03:38:57 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 04 Mar 2021 03:38:58 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 04 Mar 2021 03:38:59 GMT
ARG BONITA_VERSION
# Thu, 04 Mar 2021 03:39:17 GMT
ARG BRANDING_VERSION
# Thu, 04 Mar 2021 03:39:17 GMT
ARG BONITA_SHA256
# Thu, 04 Mar 2021 03:39:17 GMT
ARG BASE_URL
# Thu, 04 Mar 2021 03:39:17 GMT
ARG BONITA_URL
# Thu, 04 Mar 2021 03:39:18 GMT
ENV BONITA_VERSION=7.12.1
# Thu, 04 Mar 2021 03:39:18 GMT
ENV BRANDING_VERSION=2021.1
# Thu, 04 Mar 2021 03:39:18 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Thu, 04 Mar 2021 03:39:18 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Thu, 04 Mar 2021 03:39:18 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 04 Mar 2021 03:39:19 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Thu, 04 Mar 2021 03:39:20 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Thu, 04 Mar 2021 03:39:21 GMT
RUN mkdir /opt/files
# Thu, 04 Mar 2021 03:39:21 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Thu, 04 Mar 2021 03:39:26 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Thu, 04 Mar 2021 03:39:29 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Thu, 04 Mar 2021 03:39:31 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Thu, 04 Mar 2021 03:39:31 GMT
VOLUME [/opt/bonita]
# Thu, 04 Mar 2021 03:39:32 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 04 Mar 2021 03:39:32 GMT
EXPOSE 8080
# Thu, 04 Mar 2021 03:39:32 GMT
CMD ["/opt/files/startup.sh"]
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
	-	`sha256:0b013a5e6d745d8ddf229fc1b6efe515531408d68a38ccdfd19fe2734a796e20`  
		Last Modified: Thu, 04 Mar 2021 03:40:39 GMT  
		Size: 95.2 MB (95182489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43c3d83e550e3c03dbf7d5be4813516f132b770f495793ae7ec767850a867c0`  
		Last Modified: Thu, 04 Mar 2021 03:40:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e491464ad3b52ebf5550aee453151a66f342c6fae6fd17dddaa8ecfd52de0eb`  
		Last Modified: Thu, 04 Mar 2021 03:40:19 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ac5a46d0b9f41259cbbd28b965b962ac61af24a85d5940ac903bd1e53ec4a1`  
		Last Modified: Thu, 04 Mar 2021 03:40:19 GMT  
		Size: 572.4 KB (572376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d472c4128821436fa9d86e73569e07fc23ad4f59a21e2fccfcd1ee9e9c020b85`  
		Last Modified: Thu, 04 Mar 2021 03:40:45 GMT  
		Size: 112.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a35d3dfa6026e7fa52e17e9e231a17fbd844b63b8d7f0272216e59cd56bff4`  
		Last Modified: Thu, 04 Mar 2021 03:40:45 GMT  
		Size: 6.9 KB (6916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeed78bcae57a07524cd258132b6af9e23f9ecc6785be1f5f694755051ecf8be`  
		Last Modified: Thu, 04 Mar 2021 03:40:51 GMT  
		Size: 116.4 MB (116415402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c3e90c609477ff5a3252818b53a8e93c79ce128be2829b763ed5019a1c5688`  
		Last Modified: Thu, 04 Mar 2021 03:40:45 GMT  
		Size: 1.7 KB (1683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:042b27c155776c49fa827a611e68600e3ab7616ae5be3bbe45c57e5f8c41a4d8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.0 MB (225999606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1473c8d2979e05f1c6fe37e1c2ef0c1c3f0d01b1d9b043222c585bd2f204ea03`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 21 Jan 2021 03:49:23 GMT
ADD file:7d9bc01cf1f3757bf5fa308213a77aeb128883cc13616ff46b3da5b0e65b92f2 in / 
# Thu, 21 Jan 2021 03:49:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:49:29 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:49:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:49:32 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 05:28:20 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 21 Jan 2021 05:29:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 05:29:09 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 21 Jan 2021 05:29:11 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 21 Jan 2021 05:29:13 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 21 Jan 2021 05:29:14 GMT
ARG BONITA_VERSION
# Sat, 30 Jan 2021 00:53:50 GMT
ARG BRANDING_VERSION
# Sat, 30 Jan 2021 00:53:50 GMT
ARG BONITA_SHA256
# Sat, 30 Jan 2021 00:53:51 GMT
ARG BASE_URL
# Sat, 30 Jan 2021 00:53:51 GMT
ARG BONITA_URL
# Sat, 30 Jan 2021 00:53:52 GMT
ENV BONITA_VERSION=7.12.1
# Sat, 30 Jan 2021 00:53:53 GMT
ENV BRANDING_VERSION=2021.1
# Sat, 30 Jan 2021 00:53:53 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Sat, 30 Jan 2021 00:53:54 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Sat, 30 Jan 2021 00:53:54 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 30 Jan 2021 00:53:55 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Sat, 30 Jan 2021 00:53:57 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Sat, 30 Jan 2021 00:53:59 GMT
RUN mkdir /opt/files
# Sat, 30 Jan 2021 00:54:00 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Sat, 30 Jan 2021 00:54:06 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Sat, 30 Jan 2021 00:54:08 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Sat, 30 Jan 2021 00:54:11 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Sat, 30 Jan 2021 00:54:12 GMT
VOLUME [/opt/bonita]
# Sat, 30 Jan 2021 00:54:12 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Sat, 30 Jan 2021 00:54:13 GMT
EXPOSE 8080
# Sat, 30 Jan 2021 00:54:14 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:64e3fba066352e44a4c1eeb6caedc87c29b46f0a7b31e21a58183fc8370005bd`  
		Last Modified: Tue, 19 Jan 2021 00:25:17 GMT  
		Size: 23.7 MB (23732640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dbb433f451339aab734bb52e3df5b34cdea477f3f8e3aa32f7ac060bd852de2`  
		Last Modified: Thu, 21 Jan 2021 03:51:55 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3042a0d94b83caeb29bc20734c197130f58e14e86e8e6cdad8b768052bb563c`  
		Last Modified: Thu, 21 Jan 2021 03:51:54 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8df92044c4b506076de6abc24afe1d5eac83a9e6cc5fb97a725daea7b5fb742`  
		Last Modified: Thu, 21 Jan 2021 05:31:28 GMT  
		Size: 85.3 MB (85297873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1abc3fcd55457d935f9da38456f79f5f4c394ff39f5f0bf92deb550a9c5d5a8`  
		Last Modified: Thu, 21 Jan 2021 05:31:05 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb17a62d1dc9db97a189188b6263b79601d869b5f3813597d9c9990e9b1e67b0`  
		Last Modified: Thu, 21 Jan 2021 05:31:04 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af2268a1d88611b9add2dc44af567d1d121e316d036e49cbd1b3f54717c4019`  
		Last Modified: Thu, 21 Jan 2021 05:31:03 GMT  
		Size: 541.8 KB (541813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a6d9f507c165d2c3713ddc71f40686f7efab71e36563b00a38df6544f734a9`  
		Last Modified: Sat, 30 Jan 2021 00:54:31 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e96b3ed213aa787365c4954d6c9d9f0f6339011bb25c1da83b930936e897408f`  
		Last Modified: Sat, 30 Jan 2021 00:54:31 GMT  
		Size: 6.9 KB (6946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d407eacd2633e2d566bbdbc12ca4a0bfb1598bc401e81b0c7b2ac5789018614c`  
		Last Modified: Sat, 30 Jan 2021 00:54:41 GMT  
		Size: 116.4 MB (116415398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8263bbe0ad9c06ee5e05b8540e8b539f69ce8f36cd16c611f40d2a27977da5`  
		Last Modified: Sat, 30 Jan 2021 00:54:31 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:7cbc79ac9276eeb9ed45b37e7460eb8b82cd17ee65bf79366743255784a8fed5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.3 MB (233308791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2deb92cacf66527c2fdde8cdd3931695079b54e53a5882fc939be196f3fc36c`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 21 Jan 2021 03:49:03 GMT
ADD file:f6214eb5991df55aa5198d84442d6ddd28b67d4043d1832afba8b30e0249dcf5 in / 
# Thu, 21 Jan 2021 03:49:39 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:49:50 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:50:04 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:50:09 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 04:23:39 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 21 Jan 2021 04:27:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 04:28:04 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 21 Jan 2021 04:28:10 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 21 Jan 2021 04:28:18 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 21 Jan 2021 04:28:22 GMT
ARG BONITA_VERSION
# Sat, 30 Jan 2021 01:47:09 GMT
ARG BRANDING_VERSION
# Sat, 30 Jan 2021 01:47:17 GMT
ARG BONITA_SHA256
# Sat, 30 Jan 2021 01:47:23 GMT
ARG BASE_URL
# Sat, 30 Jan 2021 01:47:32 GMT
ARG BONITA_URL
# Sat, 30 Jan 2021 01:47:38 GMT
ENV BONITA_VERSION=7.12.1
# Sat, 30 Jan 2021 01:47:46 GMT
ENV BRANDING_VERSION=2021.1
# Sat, 30 Jan 2021 01:48:02 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Sat, 30 Jan 2021 01:48:07 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Sat, 30 Jan 2021 01:48:11 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 30 Jan 2021 01:48:13 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Sat, 30 Jan 2021 01:48:30 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Sat, 30 Jan 2021 01:48:55 GMT
RUN mkdir /opt/files
# Sat, 30 Jan 2021 01:48:59 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Sat, 30 Jan 2021 01:49:27 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Sat, 30 Jan 2021 01:49:41 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Sat, 30 Jan 2021 01:49:52 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Sat, 30 Jan 2021 01:49:57 GMT
VOLUME [/opt/bonita]
# Sat, 30 Jan 2021 01:50:00 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Sat, 30 Jan 2021 01:50:08 GMT
EXPOSE 8080
# Sat, 30 Jan 2021 01:50:13 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:e07786faec2ce77c08f20befe52a3eac52d983b0dfae9cb8d58dfa0ede0648e1`  
		Last Modified: Thu, 21 Jan 2021 03:54:37 GMT  
		Size: 30.4 MB (30422854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a41aaf71d5cf82fa1f9e11d2d352906ae135d0b216c665ed76ad9a8e1ce046`  
		Last Modified: Thu, 21 Jan 2021 03:54:30 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae0c92402f48f37a5d3bf1b351e5c6cbed6cec502dc9138f974a2e114c29ce4`  
		Last Modified: Thu, 21 Jan 2021 03:52:10 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b13b45af58aa295d275be3fb2ee2cdae02906032f23429acfe6e350037d8ab93`  
		Last Modified: Thu, 21 Jan 2021 04:31:44 GMT  
		Size: 85.9 MB (85917102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85b382bfd13fccaece5a5a9972badb85c89b4e5d49d62b01a5c56586d69dff55`  
		Last Modified: Thu, 21 Jan 2021 04:31:24 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b765dbe8b65a01b5e7a6c6bcf266a3f252f9ecab42044078374cd592222b75c1`  
		Last Modified: Thu, 21 Jan 2021 04:31:25 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9bc546cf88c8886a652c41a34d2b48be1bdf5a74182087aea7df14653843a8`  
		Last Modified: Thu, 21 Jan 2021 04:31:21 GMT  
		Size: 541.5 KB (541539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3328d3e249051dfe4783d885b91ec5874d8d654b2c198cc6e62b5eee230942bf`  
		Last Modified: Sat, 30 Jan 2021 01:50:42 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0341326e395d84e7152c652f6370e970564a985e74835fe94d52123709c5ae13`  
		Last Modified: Sat, 30 Jan 2021 01:50:42 GMT  
		Size: 7.0 KB (6950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b610564454d7cbfa5e7c6d19b44df37a3ff995fc38607f6154903eb2fde0914`  
		Last Modified: Sat, 30 Jan 2021 01:50:52 GMT  
		Size: 116.4 MB (116415407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06136d8ff274d12b9e1962bd89095c8930d5f735cb50f3942ae371b5128ff1af`  
		Last Modified: Sat, 30 Jan 2021 01:50:43 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:latest`

```console
$ docker pull bonita@sha256:92023653b15e0dde13c5a796f799122c47fc02865749ac63473626bacb658239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:latest` - linux; amd64

```console
$ docker pull bonita@sha256:acb5236fefd92ff819cccce8ff039bfcee49d3ffd8b8408ec9eb86e1e044034d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.9 MB (238892145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:187e939000b59a7d68f188b581df9d3cae03e73cb682657a582674e0c8c29fc2`
-	Default Command: `["\/opt\/files\/startup.sh"]`

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
# Thu, 04 Mar 2021 03:38:30 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 04 Mar 2021 03:38:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 04 Mar 2021 03:38:56 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 04 Mar 2021 03:38:57 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 04 Mar 2021 03:38:58 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 04 Mar 2021 03:38:59 GMT
ARG BONITA_VERSION
# Thu, 04 Mar 2021 03:39:17 GMT
ARG BRANDING_VERSION
# Thu, 04 Mar 2021 03:39:17 GMT
ARG BONITA_SHA256
# Thu, 04 Mar 2021 03:39:17 GMT
ARG BASE_URL
# Thu, 04 Mar 2021 03:39:17 GMT
ARG BONITA_URL
# Thu, 04 Mar 2021 03:39:18 GMT
ENV BONITA_VERSION=7.12.1
# Thu, 04 Mar 2021 03:39:18 GMT
ENV BRANDING_VERSION=2021.1
# Thu, 04 Mar 2021 03:39:18 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Thu, 04 Mar 2021 03:39:18 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Thu, 04 Mar 2021 03:39:18 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 04 Mar 2021 03:39:19 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Thu, 04 Mar 2021 03:39:20 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Thu, 04 Mar 2021 03:39:21 GMT
RUN mkdir /opt/files
# Thu, 04 Mar 2021 03:39:21 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Thu, 04 Mar 2021 03:39:26 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Thu, 04 Mar 2021 03:39:29 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Thu, 04 Mar 2021 03:39:31 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Thu, 04 Mar 2021 03:39:31 GMT
VOLUME [/opt/bonita]
# Thu, 04 Mar 2021 03:39:32 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Thu, 04 Mar 2021 03:39:32 GMT
EXPOSE 8080
# Thu, 04 Mar 2021 03:39:32 GMT
CMD ["/opt/files/startup.sh"]
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
	-	`sha256:0b013a5e6d745d8ddf229fc1b6efe515531408d68a38ccdfd19fe2734a796e20`  
		Last Modified: Thu, 04 Mar 2021 03:40:39 GMT  
		Size: 95.2 MB (95182489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43c3d83e550e3c03dbf7d5be4813516f132b770f495793ae7ec767850a867c0`  
		Last Modified: Thu, 04 Mar 2021 03:40:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e491464ad3b52ebf5550aee453151a66f342c6fae6fd17dddaa8ecfd52de0eb`  
		Last Modified: Thu, 04 Mar 2021 03:40:19 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ac5a46d0b9f41259cbbd28b965b962ac61af24a85d5940ac903bd1e53ec4a1`  
		Last Modified: Thu, 04 Mar 2021 03:40:19 GMT  
		Size: 572.4 KB (572376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d472c4128821436fa9d86e73569e07fc23ad4f59a21e2fccfcd1ee9e9c020b85`  
		Last Modified: Thu, 04 Mar 2021 03:40:45 GMT  
		Size: 112.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a35d3dfa6026e7fa52e17e9e231a17fbd844b63b8d7f0272216e59cd56bff4`  
		Last Modified: Thu, 04 Mar 2021 03:40:45 GMT  
		Size: 6.9 KB (6916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeed78bcae57a07524cd258132b6af9e23f9ecc6785be1f5f694755051ecf8be`  
		Last Modified: Thu, 04 Mar 2021 03:40:51 GMT  
		Size: 116.4 MB (116415402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c3e90c609477ff5a3252818b53a8e93c79ce128be2829b763ed5019a1c5688`  
		Last Modified: Thu, 04 Mar 2021 03:40:45 GMT  
		Size: 1.7 KB (1683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:042b27c155776c49fa827a611e68600e3ab7616ae5be3bbe45c57e5f8c41a4d8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.0 MB (225999606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1473c8d2979e05f1c6fe37e1c2ef0c1c3f0d01b1d9b043222c585bd2f204ea03`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 21 Jan 2021 03:49:23 GMT
ADD file:7d9bc01cf1f3757bf5fa308213a77aeb128883cc13616ff46b3da5b0e65b92f2 in / 
# Thu, 21 Jan 2021 03:49:27 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:49:29 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:49:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:49:32 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 05:28:20 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 21 Jan 2021 05:29:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 05:29:09 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 21 Jan 2021 05:29:11 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 21 Jan 2021 05:29:13 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 21 Jan 2021 05:29:14 GMT
ARG BONITA_VERSION
# Sat, 30 Jan 2021 00:53:50 GMT
ARG BRANDING_VERSION
# Sat, 30 Jan 2021 00:53:50 GMT
ARG BONITA_SHA256
# Sat, 30 Jan 2021 00:53:51 GMT
ARG BASE_URL
# Sat, 30 Jan 2021 00:53:51 GMT
ARG BONITA_URL
# Sat, 30 Jan 2021 00:53:52 GMT
ENV BONITA_VERSION=7.12.1
# Sat, 30 Jan 2021 00:53:53 GMT
ENV BRANDING_VERSION=2021.1
# Sat, 30 Jan 2021 00:53:53 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Sat, 30 Jan 2021 00:53:54 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Sat, 30 Jan 2021 00:53:54 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 30 Jan 2021 00:53:55 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Sat, 30 Jan 2021 00:53:57 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Sat, 30 Jan 2021 00:53:59 GMT
RUN mkdir /opt/files
# Sat, 30 Jan 2021 00:54:00 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Sat, 30 Jan 2021 00:54:06 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Sat, 30 Jan 2021 00:54:08 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Sat, 30 Jan 2021 00:54:11 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Sat, 30 Jan 2021 00:54:12 GMT
VOLUME [/opt/bonita]
# Sat, 30 Jan 2021 00:54:12 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Sat, 30 Jan 2021 00:54:13 GMT
EXPOSE 8080
# Sat, 30 Jan 2021 00:54:14 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:64e3fba066352e44a4c1eeb6caedc87c29b46f0a7b31e21a58183fc8370005bd`  
		Last Modified: Tue, 19 Jan 2021 00:25:17 GMT  
		Size: 23.7 MB (23732640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dbb433f451339aab734bb52e3df5b34cdea477f3f8e3aa32f7ac060bd852de2`  
		Last Modified: Thu, 21 Jan 2021 03:51:55 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3042a0d94b83caeb29bc20734c197130f58e14e86e8e6cdad8b768052bb563c`  
		Last Modified: Thu, 21 Jan 2021 03:51:54 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8df92044c4b506076de6abc24afe1d5eac83a9e6cc5fb97a725daea7b5fb742`  
		Last Modified: Thu, 21 Jan 2021 05:31:28 GMT  
		Size: 85.3 MB (85297873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1abc3fcd55457d935f9da38456f79f5f4c394ff39f5f0bf92deb550a9c5d5a8`  
		Last Modified: Thu, 21 Jan 2021 05:31:05 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb17a62d1dc9db97a189188b6263b79601d869b5f3813597d9c9990e9b1e67b0`  
		Last Modified: Thu, 21 Jan 2021 05:31:04 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af2268a1d88611b9add2dc44af567d1d121e316d036e49cbd1b3f54717c4019`  
		Last Modified: Thu, 21 Jan 2021 05:31:03 GMT  
		Size: 541.8 KB (541813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a6d9f507c165d2c3713ddc71f40686f7efab71e36563b00a38df6544f734a9`  
		Last Modified: Sat, 30 Jan 2021 00:54:31 GMT  
		Size: 145.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e96b3ed213aa787365c4954d6c9d9f0f6339011bb25c1da83b930936e897408f`  
		Last Modified: Sat, 30 Jan 2021 00:54:31 GMT  
		Size: 6.9 KB (6946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d407eacd2633e2d566bbdbc12ca4a0bfb1598bc401e81b0c7b2ac5789018614c`  
		Last Modified: Sat, 30 Jan 2021 00:54:41 GMT  
		Size: 116.4 MB (116415398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8263bbe0ad9c06ee5e05b8540e8b539f69ce8f36cd16c611f40d2a27977da5`  
		Last Modified: Sat, 30 Jan 2021 00:54:31 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; ppc64le

```console
$ docker pull bonita@sha256:7cbc79ac9276eeb9ed45b37e7460eb8b82cd17ee65bf79366743255784a8fed5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.3 MB (233308791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2deb92cacf66527c2fdde8cdd3931695079b54e53a5882fc939be196f3fc36c`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 21 Jan 2021 03:49:03 GMT
ADD file:f6214eb5991df55aa5198d84442d6ddd28b67d4043d1832afba8b30e0249dcf5 in / 
# Thu, 21 Jan 2021 03:49:39 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:49:50 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:50:04 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:50:09 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 04:23:39 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Thu, 21 Jan 2021 04:27:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 04:28:04 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 21 Jan 2021 04:28:10 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 21 Jan 2021 04:28:18 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 21 Jan 2021 04:28:22 GMT
ARG BONITA_VERSION
# Sat, 30 Jan 2021 01:47:09 GMT
ARG BRANDING_VERSION
# Sat, 30 Jan 2021 01:47:17 GMT
ARG BONITA_SHA256
# Sat, 30 Jan 2021 01:47:23 GMT
ARG BASE_URL
# Sat, 30 Jan 2021 01:47:32 GMT
ARG BONITA_URL
# Sat, 30 Jan 2021 01:47:38 GMT
ENV BONITA_VERSION=7.12.1
# Sat, 30 Jan 2021 01:47:46 GMT
ENV BRANDING_VERSION=2021.1
# Sat, 30 Jan 2021 01:48:02 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Sat, 30 Jan 2021 01:48:07 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Sat, 30 Jan 2021 01:48:11 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 30 Jan 2021 01:48:13 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Sat, 30 Jan 2021 01:48:30 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Sat, 30 Jan 2021 01:48:55 GMT
RUN mkdir /opt/files
# Sat, 30 Jan 2021 01:48:59 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Sat, 30 Jan 2021 01:49:27 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Sat, 30 Jan 2021 01:49:41 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Sat, 30 Jan 2021 01:49:52 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Sat, 30 Jan 2021 01:49:57 GMT
VOLUME [/opt/bonita]
# Sat, 30 Jan 2021 01:50:00 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Sat, 30 Jan 2021 01:50:08 GMT
EXPOSE 8080
# Sat, 30 Jan 2021 01:50:13 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:e07786faec2ce77c08f20befe52a3eac52d983b0dfae9cb8d58dfa0ede0648e1`  
		Last Modified: Thu, 21 Jan 2021 03:54:37 GMT  
		Size: 30.4 MB (30422854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a41aaf71d5cf82fa1f9e11d2d352906ae135d0b216c665ed76ad9a8e1ce046`  
		Last Modified: Thu, 21 Jan 2021 03:54:30 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae0c92402f48f37a5d3bf1b351e5c6cbed6cec502dc9138f974a2e114c29ce4`  
		Last Modified: Thu, 21 Jan 2021 03:52:10 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b13b45af58aa295d275be3fb2ee2cdae02906032f23429acfe6e350037d8ab93`  
		Last Modified: Thu, 21 Jan 2021 04:31:44 GMT  
		Size: 85.9 MB (85917102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85b382bfd13fccaece5a5a9972badb85c89b4e5d49d62b01a5c56586d69dff55`  
		Last Modified: Thu, 21 Jan 2021 04:31:24 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b765dbe8b65a01b5e7a6c6bcf266a3f252f9ecab42044078374cd592222b75c1`  
		Last Modified: Thu, 21 Jan 2021 04:31:25 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9bc546cf88c8886a652c41a34d2b48be1bdf5a74182087aea7df14653843a8`  
		Last Modified: Thu, 21 Jan 2021 04:31:21 GMT  
		Size: 541.5 KB (541539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3328d3e249051dfe4783d885b91ec5874d8d654b2c198cc6e62b5eee230942bf`  
		Last Modified: Sat, 30 Jan 2021 01:50:42 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0341326e395d84e7152c652f6370e970564a985e74835fe94d52123709c5ae13`  
		Last Modified: Sat, 30 Jan 2021 01:50:42 GMT  
		Size: 7.0 KB (6950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b610564454d7cbfa5e7c6d19b44df37a3ff995fc38607f6154903eb2fde0914`  
		Last Modified: Sat, 30 Jan 2021 01:50:52 GMT  
		Size: 116.4 MB (116415407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06136d8ff274d12b9e1962bd89095c8930d5f735cb50f3942ae371b5128ff1af`  
		Last Modified: Sat, 30 Jan 2021 01:50:43 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
