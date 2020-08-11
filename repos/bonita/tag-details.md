<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `bonita`

-	[`bonita:7.10`](#bonita710)
-	[`bonita:7.10.5`](#bonita7105)
-	[`bonita:7.11`](#bonita711)
-	[`bonita:7.11.1`](#bonita7111)
-	[`bonita:7.9`](#bonita79)
-	[`bonita:7.9.5`](#bonita795)
-	[`bonita:latest`](#bonitalatest)

## `bonita:7.10`

```console
$ docker pull bonita@sha256:1beb86e7c908cff590f690f001a63eb7b64b5abb96fc3b2d262dbf36f284cfb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.10` - linux; amd64

```console
$ docker pull bonita@sha256:5e5d94bb6bacdfcd68b0ccdc949c55599a2a15ab3d4cc47dfe552924a074e0a3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.2 MB (227179088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb08e1df4eb37fc6b87746b5325cfb0581d4e1a642559953cf29018f3bc4dadb`
-	Default Command: `["\/opt\/files\/startup.sh"]`

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
# Fri, 24 Jul 2020 15:12:55 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Fri, 24 Jul 2020 15:14:04 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 15:14:05 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 24 Jul 2020 15:14:06 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 24 Jul 2020 15:14:07 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 24 Jul 2020 15:14:07 GMT
ARG BONITA_VERSION
# Fri, 24 Jul 2020 15:14:08 GMT
ARG BONITA_SHA256
# Fri, 24 Jul 2020 15:14:27 GMT
ARG BASE_URL
# Fri, 24 Jul 2020 15:14:27 GMT
ARG BONITA_URL
# Fri, 24 Jul 2020 15:14:28 GMT
ENV BONITA_VERSION=7.10.5
# Fri, 24 Jul 2020 15:14:28 GMT
ENV BONITA_SHA256=bc2bb1048df1b9d8a293635924fd1e7eb2cf0652f65d3fd64c0f1bc22e435dff
# Fri, 24 Jul 2020 15:14:28 GMT
ENV BASE_URL=https://release.ow2.org/bonita
# Fri, 24 Jul 2020 15:14:29 GMT
ENV BONITA_URL=https://release.ow2.org/bonita/BonitaCommunity-7.10.5.zip
# Fri, 24 Jul 2020 15:14:30 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Fri, 24 Jul 2020 15:14:39 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 24 Jul 2020 15:14:42 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 24 Jul 2020 15:14:45 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Fri, 24 Jul 2020 15:14:45 GMT
VOLUME [/opt/bonita]
# Fri, 24 Jul 2020 15:14:45 GMT
COPY dir:6d2b12bd97418487ddd1a174f34d85d11b3e6487e01e6d3f80d99fffcff78e82 in /opt/files 
# Fri, 24 Jul 2020 15:14:46 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Fri, 24 Jul 2020 15:14:46 GMT
EXPOSE 8080
# Fri, 24 Jul 2020 15:14:47 GMT
CMD ["/opt/files/startup.sh"]
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
	-	`sha256:5ce09050ccb37a91848a2410e6cf24a9d4056cc29a002e0e3043b6e4769ce8d3`  
		Last Modified: Fri, 24 Jul 2020 15:15:54 GMT  
		Size: 101.9 MB (101906023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4478375ad1eb033b8219364f99edb05051f4adf2d66cf389f563e3f74810338`  
		Last Modified: Fri, 24 Jul 2020 15:15:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b82b669ffdbcf417e0cfbfb18f9748ff31a265e93e909bf79a5b83848d3b77c`  
		Last Modified: Fri, 24 Jul 2020 15:15:28 GMT  
		Size: 1.9 KB (1911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6828d86a7b44b30f246e15579d27ddd831a9a5e95c23822353a3e1bb4ad870a7`  
		Last Modified: Fri, 24 Jul 2020 15:15:28 GMT  
		Size: 572.4 KB (572378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0d45ed7129e7381f16cfeb7e822f9047060ab59381e6b88d0c5ad69e679e86`  
		Last Modified: Fri, 24 Jul 2020 15:16:04 GMT  
		Size: 98.0 MB (97955934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841673564a4c9b5984d3c0f81e994cd4eb1ac54aabafe8ccf8bcb0bd0d823856`  
		Last Modified: Fri, 24 Jul 2020 15:15:58 GMT  
		Size: 7.6 KB (7596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710f84969b2e9122a21b9e5c825d370d4218e3ed921eb22f58b3dd5aae95a573`  
		Last Modified: Fri, 24 Jul 2020 15:15:58 GMT  
		Size: 1.6 KB (1624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.10` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:5747d88bd63623d7ac115a4a821988fabd30367471b1057075685ddd161a50eb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.2 MB (215177534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:186123517dee901ee750a7cf4b0389d355eea74dc749debe363cffdf2348ed42`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 24 Jul 2020 16:21:15 GMT
ADD file:146b4b3953060bbe623c06f374b3b3798872e4e1ddfef76071c7c4b69a834622 in / 
# Fri, 24 Jul 2020 16:21:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 16:21:51 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 16:23:26 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 16:23:50 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 18:34:44 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Fri, 24 Jul 2020 18:36:01 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 18:36:06 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 24 Jul 2020 18:36:08 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 24 Jul 2020 18:36:11 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 24 Jul 2020 18:36:12 GMT
ARG BONITA_VERSION
# Fri, 24 Jul 2020 18:36:13 GMT
ARG BONITA_SHA256
# Fri, 24 Jul 2020 18:36:45 GMT
ARG BASE_URL
# Fri, 24 Jul 2020 18:36:46 GMT
ARG BONITA_URL
# Fri, 24 Jul 2020 18:36:48 GMT
ENV BONITA_VERSION=7.10.5
# Fri, 24 Jul 2020 18:36:49 GMT
ENV BONITA_SHA256=bc2bb1048df1b9d8a293635924fd1e7eb2cf0652f65d3fd64c0f1bc22e435dff
# Fri, 24 Jul 2020 18:36:50 GMT
ENV BASE_URL=https://release.ow2.org/bonita
# Fri, 24 Jul 2020 18:36:50 GMT
ENV BONITA_URL=https://release.ow2.org/bonita/BonitaCommunity-7.10.5.zip
# Fri, 24 Jul 2020 18:36:52 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Fri, 24 Jul 2020 18:37:00 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 24 Jul 2020 18:37:02 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 24 Jul 2020 18:37:05 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Fri, 24 Jul 2020 18:37:08 GMT
VOLUME [/opt/bonita]
# Fri, 24 Jul 2020 18:37:09 GMT
COPY dir:6d2b12bd97418487ddd1a174f34d85d11b3e6487e01e6d3f80d99fffcff78e82 in /opt/files 
# Fri, 24 Jul 2020 18:37:10 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Fri, 24 Jul 2020 18:37:10 GMT
EXPOSE 8080
# Fri, 24 Jul 2020 18:37:11 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:a114936b480795ec46632c29c96e126744c314983ee0d83354804dc39d1afb46`  
		Last Modified: Mon, 13 Jul 2020 15:47:08 GMT  
		Size: 23.7 MB (23721122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27ecf0d2a869e5d188121e6b38473e481b66599a26d8df24d22c9170f50bfa9`  
		Last Modified: Fri, 24 Jul 2020 16:27:00 GMT  
		Size: 35.2 KB (35205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4eb48eb870f62ec1a7a4a2d753bf2b92dff62a6dbedaeff6db6e41cb33196bc`  
		Last Modified: Fri, 24 Jul 2020 16:27:00 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f912b9bb20d998fd0f1a2526d5539f35d34a476da71c783d0041b25b78c0af5`  
		Last Modified: Fri, 24 Jul 2020 16:27:00 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c7aace3625d8fa13cf8b7d77fe57408818354300e46353244fef2776362c56`  
		Last Modified: Fri, 24 Jul 2020 18:38:22 GMT  
		Size: 92.9 MB (92911044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9983df6425d8cd839e1b2ae6052ea46e5ddfd942e2e822f08b65fd37b92eb2a`  
		Last Modified: Fri, 24 Jul 2020 18:37:54 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97944ca16225583c86f445ec7811306935d93a1ac397d4c6853f2322b87ce0a4`  
		Last Modified: Fri, 24 Jul 2020 18:37:52 GMT  
		Size: 1.9 KB (1918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f054d458bdf6ba532ab669977ad7f78bdddc9716ae73fde3b5f150fe598daf`  
		Last Modified: Fri, 24 Jul 2020 18:37:53 GMT  
		Size: 541.8 KB (541811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03c7d6cdcb9829488e4673feffe614800d319d47a1188c48be80e76f5bcfd2a0`  
		Last Modified: Fri, 24 Jul 2020 18:38:38 GMT  
		Size: 98.0 MB (97955971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd8c1ac0b5238830ed33fe4608b28bf530720425622e7b4ca2bee9859dd70a3`  
		Last Modified: Fri, 24 Jul 2020 18:38:29 GMT  
		Size: 7.6 KB (7620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:361b3feb3deef5236f296237726425c6c5bf96653713d7aea60af3636277b27e`  
		Last Modified: Fri, 24 Jul 2020 18:38:29 GMT  
		Size: 1.7 KB (1651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.10` - linux; ppc64le

```console
$ docker pull bonita@sha256:06295dbf11481d69f32b7d15f2dba20b31127271eab35ed5447310cf638a76e6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.8 MB (223838363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45c9a1157fe2702c26783e376d61df025b4beae65d11f76a541becc39342b74`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 24 Jul 2020 14:33:42 GMT
ADD file:d8c73324b090ba968a3efc4afc8af7d913766bd7787fc4cd6e4436895a4e564a in / 
# Fri, 24 Jul 2020 14:34:10 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:34:45 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:35:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:35:08 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 15:02:57 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Fri, 24 Jul 2020 15:15:53 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 15:18:17 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 24 Jul 2020 15:18:41 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 24 Jul 2020 15:19:19 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 24 Jul 2020 15:20:18 GMT
ARG BONITA_VERSION
# Fri, 24 Jul 2020 15:21:14 GMT
ARG BONITA_SHA256
# Fri, 24 Jul 2020 15:29:35 GMT
ARG BASE_URL
# Fri, 24 Jul 2020 15:29:45 GMT
ARG BONITA_URL
# Fri, 24 Jul 2020 15:29:58 GMT
ENV BONITA_VERSION=7.10.5
# Fri, 24 Jul 2020 15:30:18 GMT
ENV BONITA_SHA256=bc2bb1048df1b9d8a293635924fd1e7eb2cf0652f65d3fd64c0f1bc22e435dff
# Fri, 24 Jul 2020 15:30:37 GMT
ENV BASE_URL=https://release.ow2.org/bonita
# Fri, 24 Jul 2020 15:30:56 GMT
ENV BONITA_URL=https://release.ow2.org/bonita/BonitaCommunity-7.10.5.zip
# Fri, 24 Jul 2020 15:31:14 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Fri, 24 Jul 2020 15:32:12 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 24 Jul 2020 15:32:31 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 24 Jul 2020 15:32:45 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Fri, 24 Jul 2020 15:32:51 GMT
VOLUME [/opt/bonita]
# Fri, 24 Jul 2020 15:32:57 GMT
COPY dir:6d2b12bd97418487ddd1a174f34d85d11b3e6487e01e6d3f80d99fffcff78e82 in /opt/files 
# Fri, 24 Jul 2020 15:33:00 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Fri, 24 Jul 2020 15:33:09 GMT
EXPOSE 8080
# Fri, 24 Jul 2020 15:33:15 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:453712c8810fcce792c21167e028047a35328679a3bd4429b8837301315e9103`  
		Last Modified: Mon, 13 Jul 2020 15:47:10 GMT  
		Size: 30.4 MB (30404926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecbb4638d99213e93a32d6945492539426ee3616d7ba413462a8b936268a56af`  
		Last Modified: Fri, 24 Jul 2020 14:41:32 GMT  
		Size: 35.2 KB (35224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b0bd277b733224c67d835643aa13dd8a9b86bcc10023a393302b3861e9a7b8`  
		Last Modified: Fri, 24 Jul 2020 14:41:32 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270c2b729d72bf4931bb8d6ccbd100e124e01bac9628380f36c2d0f13bdcc109`  
		Last Modified: Fri, 24 Jul 2020 14:41:31 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4dc874fe32813212edae7830ebd9554906d3a9802e744a6530ed9a511570f21`  
		Last Modified: Fri, 24 Jul 2020 15:36:20 GMT  
		Size: 94.9 MB (94888298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05eb40fa041d55b9cd41e2e2f1a15e457175cc3a2811e496e29307a862ec43d9`  
		Last Modified: Fri, 24 Jul 2020 15:35:57 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c80b30a08e97cf721509bb59ba0408d673fed65d3ed71f5db8036232c7504f`  
		Last Modified: Fri, 24 Jul 2020 15:35:52 GMT  
		Size: 1.9 KB (1928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a203b158d8938914a6fe005c69beb448eb02aeecdf3e4966988855eda91435`  
		Last Modified: Fri, 24 Jul 2020 15:35:52 GMT  
		Size: 541.5 KB (541549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca2098aa6b882e16efea4df2aeb18a3b068dbcc097daa5b34c557b99145c3f7`  
		Last Modified: Fri, 24 Jul 2020 15:36:48 GMT  
		Size: 98.0 MB (97955971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:615fe22f80a63eb8288a3c882d487381a5fda7d6a752e7008cef15082de832e7`  
		Last Modified: Fri, 24 Jul 2020 15:36:41 GMT  
		Size: 7.6 KB (7618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e339a306b67bc7fd74f4303f47c4d461b3240cb050045a4abd0d491a34bc5dd8`  
		Last Modified: Fri, 24 Jul 2020 15:36:41 GMT  
		Size: 1.7 KB (1653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.10.5`

```console
$ docker pull bonita@sha256:1beb86e7c908cff590f690f001a63eb7b64b5abb96fc3b2d262dbf36f284cfb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.10.5` - linux; amd64

```console
$ docker pull bonita@sha256:5e5d94bb6bacdfcd68b0ccdc949c55599a2a15ab3d4cc47dfe552924a074e0a3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.2 MB (227179088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb08e1df4eb37fc6b87746b5325cfb0581d4e1a642559953cf29018f3bc4dadb`
-	Default Command: `["\/opt\/files\/startup.sh"]`

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
# Fri, 24 Jul 2020 15:12:55 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Fri, 24 Jul 2020 15:14:04 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 15:14:05 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 24 Jul 2020 15:14:06 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 24 Jul 2020 15:14:07 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 24 Jul 2020 15:14:07 GMT
ARG BONITA_VERSION
# Fri, 24 Jul 2020 15:14:08 GMT
ARG BONITA_SHA256
# Fri, 24 Jul 2020 15:14:27 GMT
ARG BASE_URL
# Fri, 24 Jul 2020 15:14:27 GMT
ARG BONITA_URL
# Fri, 24 Jul 2020 15:14:28 GMT
ENV BONITA_VERSION=7.10.5
# Fri, 24 Jul 2020 15:14:28 GMT
ENV BONITA_SHA256=bc2bb1048df1b9d8a293635924fd1e7eb2cf0652f65d3fd64c0f1bc22e435dff
# Fri, 24 Jul 2020 15:14:28 GMT
ENV BASE_URL=https://release.ow2.org/bonita
# Fri, 24 Jul 2020 15:14:29 GMT
ENV BONITA_URL=https://release.ow2.org/bonita/BonitaCommunity-7.10.5.zip
# Fri, 24 Jul 2020 15:14:30 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Fri, 24 Jul 2020 15:14:39 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 24 Jul 2020 15:14:42 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 24 Jul 2020 15:14:45 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Fri, 24 Jul 2020 15:14:45 GMT
VOLUME [/opt/bonita]
# Fri, 24 Jul 2020 15:14:45 GMT
COPY dir:6d2b12bd97418487ddd1a174f34d85d11b3e6487e01e6d3f80d99fffcff78e82 in /opt/files 
# Fri, 24 Jul 2020 15:14:46 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Fri, 24 Jul 2020 15:14:46 GMT
EXPOSE 8080
# Fri, 24 Jul 2020 15:14:47 GMT
CMD ["/opt/files/startup.sh"]
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
	-	`sha256:5ce09050ccb37a91848a2410e6cf24a9d4056cc29a002e0e3043b6e4769ce8d3`  
		Last Modified: Fri, 24 Jul 2020 15:15:54 GMT  
		Size: 101.9 MB (101906023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4478375ad1eb033b8219364f99edb05051f4adf2d66cf389f563e3f74810338`  
		Last Modified: Fri, 24 Jul 2020 15:15:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b82b669ffdbcf417e0cfbfb18f9748ff31a265e93e909bf79a5b83848d3b77c`  
		Last Modified: Fri, 24 Jul 2020 15:15:28 GMT  
		Size: 1.9 KB (1911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6828d86a7b44b30f246e15579d27ddd831a9a5e95c23822353a3e1bb4ad870a7`  
		Last Modified: Fri, 24 Jul 2020 15:15:28 GMT  
		Size: 572.4 KB (572378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0d45ed7129e7381f16cfeb7e822f9047060ab59381e6b88d0c5ad69e679e86`  
		Last Modified: Fri, 24 Jul 2020 15:16:04 GMT  
		Size: 98.0 MB (97955934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841673564a4c9b5984d3c0f81e994cd4eb1ac54aabafe8ccf8bcb0bd0d823856`  
		Last Modified: Fri, 24 Jul 2020 15:15:58 GMT  
		Size: 7.6 KB (7596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710f84969b2e9122a21b9e5c825d370d4218e3ed921eb22f58b3dd5aae95a573`  
		Last Modified: Fri, 24 Jul 2020 15:15:58 GMT  
		Size: 1.6 KB (1624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.10.5` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:5747d88bd63623d7ac115a4a821988fabd30367471b1057075685ddd161a50eb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.2 MB (215177534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:186123517dee901ee750a7cf4b0389d355eea74dc749debe363cffdf2348ed42`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 24 Jul 2020 16:21:15 GMT
ADD file:146b4b3953060bbe623c06f374b3b3798872e4e1ddfef76071c7c4b69a834622 in / 
# Fri, 24 Jul 2020 16:21:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 16:21:51 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 16:23:26 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 16:23:50 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 18:34:44 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Fri, 24 Jul 2020 18:36:01 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 18:36:06 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 24 Jul 2020 18:36:08 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 24 Jul 2020 18:36:11 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 24 Jul 2020 18:36:12 GMT
ARG BONITA_VERSION
# Fri, 24 Jul 2020 18:36:13 GMT
ARG BONITA_SHA256
# Fri, 24 Jul 2020 18:36:45 GMT
ARG BASE_URL
# Fri, 24 Jul 2020 18:36:46 GMT
ARG BONITA_URL
# Fri, 24 Jul 2020 18:36:48 GMT
ENV BONITA_VERSION=7.10.5
# Fri, 24 Jul 2020 18:36:49 GMT
ENV BONITA_SHA256=bc2bb1048df1b9d8a293635924fd1e7eb2cf0652f65d3fd64c0f1bc22e435dff
# Fri, 24 Jul 2020 18:36:50 GMT
ENV BASE_URL=https://release.ow2.org/bonita
# Fri, 24 Jul 2020 18:36:50 GMT
ENV BONITA_URL=https://release.ow2.org/bonita/BonitaCommunity-7.10.5.zip
# Fri, 24 Jul 2020 18:36:52 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Fri, 24 Jul 2020 18:37:00 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 24 Jul 2020 18:37:02 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 24 Jul 2020 18:37:05 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Fri, 24 Jul 2020 18:37:08 GMT
VOLUME [/opt/bonita]
# Fri, 24 Jul 2020 18:37:09 GMT
COPY dir:6d2b12bd97418487ddd1a174f34d85d11b3e6487e01e6d3f80d99fffcff78e82 in /opt/files 
# Fri, 24 Jul 2020 18:37:10 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Fri, 24 Jul 2020 18:37:10 GMT
EXPOSE 8080
# Fri, 24 Jul 2020 18:37:11 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:a114936b480795ec46632c29c96e126744c314983ee0d83354804dc39d1afb46`  
		Last Modified: Mon, 13 Jul 2020 15:47:08 GMT  
		Size: 23.7 MB (23721122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27ecf0d2a869e5d188121e6b38473e481b66599a26d8df24d22c9170f50bfa9`  
		Last Modified: Fri, 24 Jul 2020 16:27:00 GMT  
		Size: 35.2 KB (35205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4eb48eb870f62ec1a7a4a2d753bf2b92dff62a6dbedaeff6db6e41cb33196bc`  
		Last Modified: Fri, 24 Jul 2020 16:27:00 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f912b9bb20d998fd0f1a2526d5539f35d34a476da71c783d0041b25b78c0af5`  
		Last Modified: Fri, 24 Jul 2020 16:27:00 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c7aace3625d8fa13cf8b7d77fe57408818354300e46353244fef2776362c56`  
		Last Modified: Fri, 24 Jul 2020 18:38:22 GMT  
		Size: 92.9 MB (92911044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9983df6425d8cd839e1b2ae6052ea46e5ddfd942e2e822f08b65fd37b92eb2a`  
		Last Modified: Fri, 24 Jul 2020 18:37:54 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97944ca16225583c86f445ec7811306935d93a1ac397d4c6853f2322b87ce0a4`  
		Last Modified: Fri, 24 Jul 2020 18:37:52 GMT  
		Size: 1.9 KB (1918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f054d458bdf6ba532ab669977ad7f78bdddc9716ae73fde3b5f150fe598daf`  
		Last Modified: Fri, 24 Jul 2020 18:37:53 GMT  
		Size: 541.8 KB (541811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03c7d6cdcb9829488e4673feffe614800d319d47a1188c48be80e76f5bcfd2a0`  
		Last Modified: Fri, 24 Jul 2020 18:38:38 GMT  
		Size: 98.0 MB (97955971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd8c1ac0b5238830ed33fe4608b28bf530720425622e7b4ca2bee9859dd70a3`  
		Last Modified: Fri, 24 Jul 2020 18:38:29 GMT  
		Size: 7.6 KB (7620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:361b3feb3deef5236f296237726425c6c5bf96653713d7aea60af3636277b27e`  
		Last Modified: Fri, 24 Jul 2020 18:38:29 GMT  
		Size: 1.7 KB (1651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.10.5` - linux; ppc64le

```console
$ docker pull bonita@sha256:06295dbf11481d69f32b7d15f2dba20b31127271eab35ed5447310cf638a76e6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.8 MB (223838363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45c9a1157fe2702c26783e376d61df025b4beae65d11f76a541becc39342b74`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 24 Jul 2020 14:33:42 GMT
ADD file:d8c73324b090ba968a3efc4afc8af7d913766bd7787fc4cd6e4436895a4e564a in / 
# Fri, 24 Jul 2020 14:34:10 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:34:45 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:35:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:35:08 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 15:02:57 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Fri, 24 Jul 2020 15:15:53 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 15:18:17 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 24 Jul 2020 15:18:41 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 24 Jul 2020 15:19:19 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 24 Jul 2020 15:20:18 GMT
ARG BONITA_VERSION
# Fri, 24 Jul 2020 15:21:14 GMT
ARG BONITA_SHA256
# Fri, 24 Jul 2020 15:29:35 GMT
ARG BASE_URL
# Fri, 24 Jul 2020 15:29:45 GMT
ARG BONITA_URL
# Fri, 24 Jul 2020 15:29:58 GMT
ENV BONITA_VERSION=7.10.5
# Fri, 24 Jul 2020 15:30:18 GMT
ENV BONITA_SHA256=bc2bb1048df1b9d8a293635924fd1e7eb2cf0652f65d3fd64c0f1bc22e435dff
# Fri, 24 Jul 2020 15:30:37 GMT
ENV BASE_URL=https://release.ow2.org/bonita
# Fri, 24 Jul 2020 15:30:56 GMT
ENV BONITA_URL=https://release.ow2.org/bonita/BonitaCommunity-7.10.5.zip
# Fri, 24 Jul 2020 15:31:14 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Fri, 24 Jul 2020 15:32:12 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 24 Jul 2020 15:32:31 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 24 Jul 2020 15:32:45 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Fri, 24 Jul 2020 15:32:51 GMT
VOLUME [/opt/bonita]
# Fri, 24 Jul 2020 15:32:57 GMT
COPY dir:6d2b12bd97418487ddd1a174f34d85d11b3e6487e01e6d3f80d99fffcff78e82 in /opt/files 
# Fri, 24 Jul 2020 15:33:00 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Fri, 24 Jul 2020 15:33:09 GMT
EXPOSE 8080
# Fri, 24 Jul 2020 15:33:15 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:453712c8810fcce792c21167e028047a35328679a3bd4429b8837301315e9103`  
		Last Modified: Mon, 13 Jul 2020 15:47:10 GMT  
		Size: 30.4 MB (30404926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecbb4638d99213e93a32d6945492539426ee3616d7ba413462a8b936268a56af`  
		Last Modified: Fri, 24 Jul 2020 14:41:32 GMT  
		Size: 35.2 KB (35224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b0bd277b733224c67d835643aa13dd8a9b86bcc10023a393302b3861e9a7b8`  
		Last Modified: Fri, 24 Jul 2020 14:41:32 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270c2b729d72bf4931bb8d6ccbd100e124e01bac9628380f36c2d0f13bdcc109`  
		Last Modified: Fri, 24 Jul 2020 14:41:31 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4dc874fe32813212edae7830ebd9554906d3a9802e744a6530ed9a511570f21`  
		Last Modified: Fri, 24 Jul 2020 15:36:20 GMT  
		Size: 94.9 MB (94888298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05eb40fa041d55b9cd41e2e2f1a15e457175cc3a2811e496e29307a862ec43d9`  
		Last Modified: Fri, 24 Jul 2020 15:35:57 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c80b30a08e97cf721509bb59ba0408d673fed65d3ed71f5db8036232c7504f`  
		Last Modified: Fri, 24 Jul 2020 15:35:52 GMT  
		Size: 1.9 KB (1928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a203b158d8938914a6fe005c69beb448eb02aeecdf3e4966988855eda91435`  
		Last Modified: Fri, 24 Jul 2020 15:35:52 GMT  
		Size: 541.5 KB (541549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca2098aa6b882e16efea4df2aeb18a3b068dbcc097daa5b34c557b99145c3f7`  
		Last Modified: Fri, 24 Jul 2020 15:36:48 GMT  
		Size: 98.0 MB (97955971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:615fe22f80a63eb8288a3c882d487381a5fda7d6a752e7008cef15082de832e7`  
		Last Modified: Fri, 24 Jul 2020 15:36:41 GMT  
		Size: 7.6 KB (7618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e339a306b67bc7fd74f4303f47c4d461b3240cb050045a4abd0d491a34bc5dd8`  
		Last Modified: Fri, 24 Jul 2020 15:36:41 GMT  
		Size: 1.7 KB (1653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.11`

```console
$ docker pull bonita@sha256:95b0b8db7899dcd91711cff86795f0833e6e35e378661af21439c499d4bbfcbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.11` - linux; amd64

```console
$ docker pull bonita@sha256:46c91d9a5183e12efb3f8d355e2aba11ccdbcb73f6c8e038d6d87ed8f73ef1c8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.5 MB (242456504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f08fa01271425cc02c855e17e1d3972a08e9bb21924bee7b8e1de8c237ac9177`
-	Default Command: `["\/opt\/files\/startup.sh"]`

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
# Fri, 24 Jul 2020 15:12:55 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Fri, 24 Jul 2020 15:14:04 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 15:14:05 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 24 Jul 2020 15:14:06 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 24 Jul 2020 15:14:07 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 24 Jul 2020 15:14:07 GMT
ARG BONITA_VERSION
# Fri, 24 Jul 2020 15:14:08 GMT
ARG BONITA_SHA256
# Fri, 24 Jul 2020 15:14:27 GMT
ARG BASE_URL
# Fri, 24 Jul 2020 15:14:27 GMT
ARG BONITA_URL
# Tue, 11 Aug 2020 20:21:46 GMT
ENV BONITA_VERSION=7.11.1
# Tue, 11 Aug 2020 20:21:46 GMT
ENV BONITA_SHA256=d2874ada41c0549a6620ef8095c6eb7480e45d8b8143af5f983a06df62a7243d
# Tue, 11 Aug 2020 20:21:47 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 11 Aug 2020 20:21:47 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.1/BonitaCommunity-7.11.1.zip
# Tue, 11 Aug 2020 20:21:48 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Tue, 11 Aug 2020 20:21:53 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Tue, 11 Aug 2020 20:21:55 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Tue, 11 Aug 2020 20:21:56 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Tue, 11 Aug 2020 20:21:57 GMT
VOLUME [/opt/bonita]
# Tue, 11 Aug 2020 20:21:57 GMT
COPY dir:6c801c025cd750ee96a4e29676afb9ba394d4bc647bb82010816896eefc044ed in /opt/files 
# Tue, 11 Aug 2020 20:21:57 GMT
COPY dir:173a816fed2c2b9f191c45b4238f2062102518ab7cf02e5e7c4ca6bd9caeb849 in /opt/templates 
# Tue, 11 Aug 2020 20:21:57 GMT
EXPOSE 8080
# Tue, 11 Aug 2020 20:21:57 GMT
CMD ["/opt/files/startup.sh"]
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
	-	`sha256:5ce09050ccb37a91848a2410e6cf24a9d4056cc29a002e0e3043b6e4769ce8d3`  
		Last Modified: Fri, 24 Jul 2020 15:15:54 GMT  
		Size: 101.9 MB (101906023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4478375ad1eb033b8219364f99edb05051f4adf2d66cf389f563e3f74810338`  
		Last Modified: Fri, 24 Jul 2020 15:15:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b82b669ffdbcf417e0cfbfb18f9748ff31a265e93e909bf79a5b83848d3b77c`  
		Last Modified: Fri, 24 Jul 2020 15:15:28 GMT  
		Size: 1.9 KB (1911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6828d86a7b44b30f246e15579d27ddd831a9a5e95c23822353a3e1bb4ad870a7`  
		Last Modified: Fri, 24 Jul 2020 15:15:28 GMT  
		Size: 572.4 KB (572378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba427e87d977f1d635964ca96e266aa00591aea7ebfdc2e05f36b697b1efc651`  
		Last Modified: Tue, 11 Aug 2020 20:22:25 GMT  
		Size: 113.2 MB (113233259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d2ba96a9cf2e076ea398b37ed0e9060ff9df570080291281d69e86934af0da`  
		Last Modified: Tue, 11 Aug 2020 20:22:06 GMT  
		Size: 7.6 KB (7632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae962f4f19e3a055bacdfde2a5f8c1e9caa78dea98eccce0f4f3beced547b10`  
		Last Modified: Tue, 11 Aug 2020 20:22:07 GMT  
		Size: 1.7 KB (1679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:8c01dad6734f26028c6b140de76f1a60afdcf66c3a79f08909f8180fdf158a7f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230454939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e01cc05832e6b7f271cb611727d26e9ef6ba626f5a832e14b98de2e33138867`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 24 Jul 2020 16:21:15 GMT
ADD file:146b4b3953060bbe623c06f374b3b3798872e4e1ddfef76071c7c4b69a834622 in / 
# Fri, 24 Jul 2020 16:21:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 16:21:51 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 16:23:26 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 16:23:50 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 18:34:44 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Fri, 24 Jul 2020 18:36:01 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 18:36:06 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 24 Jul 2020 18:36:08 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 24 Jul 2020 18:36:11 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 24 Jul 2020 18:36:12 GMT
ARG BONITA_VERSION
# Fri, 24 Jul 2020 18:36:13 GMT
ARG BONITA_SHA256
# Fri, 24 Jul 2020 18:36:45 GMT
ARG BASE_URL
# Fri, 24 Jul 2020 18:36:46 GMT
ARG BONITA_URL
# Tue, 11 Aug 2020 19:43:27 GMT
ENV BONITA_VERSION=7.11.1
# Tue, 11 Aug 2020 19:43:28 GMT
ENV BONITA_SHA256=d2874ada41c0549a6620ef8095c6eb7480e45d8b8143af5f983a06df62a7243d
# Tue, 11 Aug 2020 19:43:28 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 11 Aug 2020 19:43:29 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.1/BonitaCommunity-7.11.1.zip
# Tue, 11 Aug 2020 19:43:31 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Tue, 11 Aug 2020 19:43:41 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Tue, 11 Aug 2020 19:43:44 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Tue, 11 Aug 2020 19:43:46 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Tue, 11 Aug 2020 19:43:47 GMT
VOLUME [/opt/bonita]
# Tue, 11 Aug 2020 19:43:48 GMT
COPY dir:6c801c025cd750ee96a4e29676afb9ba394d4bc647bb82010816896eefc044ed in /opt/files 
# Tue, 11 Aug 2020 19:43:48 GMT
COPY dir:173a816fed2c2b9f191c45b4238f2062102518ab7cf02e5e7c4ca6bd9caeb849 in /opt/templates 
# Tue, 11 Aug 2020 19:43:49 GMT
EXPOSE 8080
# Tue, 11 Aug 2020 19:43:50 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:a114936b480795ec46632c29c96e126744c314983ee0d83354804dc39d1afb46`  
		Last Modified: Mon, 13 Jul 2020 15:47:08 GMT  
		Size: 23.7 MB (23721122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27ecf0d2a869e5d188121e6b38473e481b66599a26d8df24d22c9170f50bfa9`  
		Last Modified: Fri, 24 Jul 2020 16:27:00 GMT  
		Size: 35.2 KB (35205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4eb48eb870f62ec1a7a4a2d753bf2b92dff62a6dbedaeff6db6e41cb33196bc`  
		Last Modified: Fri, 24 Jul 2020 16:27:00 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f912b9bb20d998fd0f1a2526d5539f35d34a476da71c783d0041b25b78c0af5`  
		Last Modified: Fri, 24 Jul 2020 16:27:00 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c7aace3625d8fa13cf8b7d77fe57408818354300e46353244fef2776362c56`  
		Last Modified: Fri, 24 Jul 2020 18:38:22 GMT  
		Size: 92.9 MB (92911044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9983df6425d8cd839e1b2ae6052ea46e5ddfd942e2e822f08b65fd37b92eb2a`  
		Last Modified: Fri, 24 Jul 2020 18:37:54 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97944ca16225583c86f445ec7811306935d93a1ac397d4c6853f2322b87ce0a4`  
		Last Modified: Fri, 24 Jul 2020 18:37:52 GMT  
		Size: 1.9 KB (1918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f054d458bdf6ba532ab669977ad7f78bdddc9716ae73fde3b5f150fe598daf`  
		Last Modified: Fri, 24 Jul 2020 18:37:53 GMT  
		Size: 541.8 KB (541811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba1a71e36dea7995351642f9e6283360224eec43f3edaa20c69293bcb667b226`  
		Last Modified: Tue, 11 Aug 2020 19:44:22 GMT  
		Size: 113.2 MB (113233287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdcb9af7d9e74359515b021c960417ed4a43553d71f813ad12cf975e99217767`  
		Last Modified: Tue, 11 Aug 2020 19:44:03 GMT  
		Size: 7.7 KB (7659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db876ac2189dad6a40f9b71205d91c32a1f939cddf325f5d8ed5b7588b814a62`  
		Last Modified: Tue, 11 Aug 2020 19:44:04 GMT  
		Size: 1.7 KB (1701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11` - linux; ppc64le

```console
$ docker pull bonita@sha256:46a12d62583064b20dc5dc5e464f855bae992df10570f9c8df1f94be43646d78
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.1 MB (239115773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aed8256341d30f9f3fc82988c1bff8c667d9db5ebfa2d70769b19e54d272664d`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 24 Jul 2020 14:33:42 GMT
ADD file:d8c73324b090ba968a3efc4afc8af7d913766bd7787fc4cd6e4436895a4e564a in / 
# Fri, 24 Jul 2020 14:34:10 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:34:45 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:35:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:35:08 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 15:02:57 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Fri, 24 Jul 2020 15:15:53 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 15:18:17 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 24 Jul 2020 15:18:41 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 24 Jul 2020 15:19:19 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 24 Jul 2020 15:20:18 GMT
ARG BONITA_VERSION
# Fri, 24 Jul 2020 15:21:14 GMT
ARG BONITA_SHA256
# Fri, 24 Jul 2020 15:29:35 GMT
ARG BASE_URL
# Fri, 24 Jul 2020 15:29:45 GMT
ARG BONITA_URL
# Tue, 11 Aug 2020 20:32:59 GMT
ENV BONITA_VERSION=7.11.1
# Tue, 11 Aug 2020 20:33:12 GMT
ENV BONITA_SHA256=d2874ada41c0549a6620ef8095c6eb7480e45d8b8143af5f983a06df62a7243d
# Tue, 11 Aug 2020 20:33:21 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 11 Aug 2020 20:33:26 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.1/BonitaCommunity-7.11.1.zip
# Tue, 11 Aug 2020 20:33:52 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Tue, 11 Aug 2020 20:34:21 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Tue, 11 Aug 2020 20:34:35 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Tue, 11 Aug 2020 20:34:50 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Tue, 11 Aug 2020 20:34:59 GMT
VOLUME [/opt/bonita]
# Tue, 11 Aug 2020 20:35:02 GMT
COPY dir:6c801c025cd750ee96a4e29676afb9ba394d4bc647bb82010816896eefc044ed in /opt/files 
# Tue, 11 Aug 2020 20:35:05 GMT
COPY dir:173a816fed2c2b9f191c45b4238f2062102518ab7cf02e5e7c4ca6bd9caeb849 in /opt/templates 
# Tue, 11 Aug 2020 20:35:13 GMT
EXPOSE 8080
# Tue, 11 Aug 2020 20:35:17 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:453712c8810fcce792c21167e028047a35328679a3bd4429b8837301315e9103`  
		Last Modified: Mon, 13 Jul 2020 15:47:10 GMT  
		Size: 30.4 MB (30404926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecbb4638d99213e93a32d6945492539426ee3616d7ba413462a8b936268a56af`  
		Last Modified: Fri, 24 Jul 2020 14:41:32 GMT  
		Size: 35.2 KB (35224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b0bd277b733224c67d835643aa13dd8a9b86bcc10023a393302b3861e9a7b8`  
		Last Modified: Fri, 24 Jul 2020 14:41:32 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270c2b729d72bf4931bb8d6ccbd100e124e01bac9628380f36c2d0f13bdcc109`  
		Last Modified: Fri, 24 Jul 2020 14:41:31 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4dc874fe32813212edae7830ebd9554906d3a9802e744a6530ed9a511570f21`  
		Last Modified: Fri, 24 Jul 2020 15:36:20 GMT  
		Size: 94.9 MB (94888298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05eb40fa041d55b9cd41e2e2f1a15e457175cc3a2811e496e29307a862ec43d9`  
		Last Modified: Fri, 24 Jul 2020 15:35:57 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c80b30a08e97cf721509bb59ba0408d673fed65d3ed71f5db8036232c7504f`  
		Last Modified: Fri, 24 Jul 2020 15:35:52 GMT  
		Size: 1.9 KB (1928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a203b158d8938914a6fe005c69beb448eb02aeecdf3e4966988855eda91435`  
		Last Modified: Fri, 24 Jul 2020 15:35:52 GMT  
		Size: 541.5 KB (541549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be42801dd677c8b8b03e2272fd48e918c74558f615368d64515e5253282277c`  
		Last Modified: Tue, 11 Aug 2020 20:35:53 GMT  
		Size: 113.2 MB (113233289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf0a66d388f71754edfc41324b75df7ce8f8b57b462c023adce8efbf933c036`  
		Last Modified: Tue, 11 Aug 2020 20:35:45 GMT  
		Size: 7.7 KB (7660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6afb022459ebd3e03885dc35798a8b27ea5348111b3e99cf2292f40a249e57bf`  
		Last Modified: Tue, 11 Aug 2020 20:35:45 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.11.1`

```console
$ docker pull bonita@sha256:95b0b8db7899dcd91711cff86795f0833e6e35e378661af21439c499d4bbfcbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.11.1` - linux; amd64

```console
$ docker pull bonita@sha256:46c91d9a5183e12efb3f8d355e2aba11ccdbcb73f6c8e038d6d87ed8f73ef1c8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.5 MB (242456504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f08fa01271425cc02c855e17e1d3972a08e9bb21924bee7b8e1de8c237ac9177`
-	Default Command: `["\/opt\/files\/startup.sh"]`

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
# Fri, 24 Jul 2020 15:12:55 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Fri, 24 Jul 2020 15:14:04 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 15:14:05 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 24 Jul 2020 15:14:06 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 24 Jul 2020 15:14:07 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 24 Jul 2020 15:14:07 GMT
ARG BONITA_VERSION
# Fri, 24 Jul 2020 15:14:08 GMT
ARG BONITA_SHA256
# Fri, 24 Jul 2020 15:14:27 GMT
ARG BASE_URL
# Fri, 24 Jul 2020 15:14:27 GMT
ARG BONITA_URL
# Tue, 11 Aug 2020 20:21:46 GMT
ENV BONITA_VERSION=7.11.1
# Tue, 11 Aug 2020 20:21:46 GMT
ENV BONITA_SHA256=d2874ada41c0549a6620ef8095c6eb7480e45d8b8143af5f983a06df62a7243d
# Tue, 11 Aug 2020 20:21:47 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 11 Aug 2020 20:21:47 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.1/BonitaCommunity-7.11.1.zip
# Tue, 11 Aug 2020 20:21:48 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Tue, 11 Aug 2020 20:21:53 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Tue, 11 Aug 2020 20:21:55 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Tue, 11 Aug 2020 20:21:56 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Tue, 11 Aug 2020 20:21:57 GMT
VOLUME [/opt/bonita]
# Tue, 11 Aug 2020 20:21:57 GMT
COPY dir:6c801c025cd750ee96a4e29676afb9ba394d4bc647bb82010816896eefc044ed in /opt/files 
# Tue, 11 Aug 2020 20:21:57 GMT
COPY dir:173a816fed2c2b9f191c45b4238f2062102518ab7cf02e5e7c4ca6bd9caeb849 in /opt/templates 
# Tue, 11 Aug 2020 20:21:57 GMT
EXPOSE 8080
# Tue, 11 Aug 2020 20:21:57 GMT
CMD ["/opt/files/startup.sh"]
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
	-	`sha256:5ce09050ccb37a91848a2410e6cf24a9d4056cc29a002e0e3043b6e4769ce8d3`  
		Last Modified: Fri, 24 Jul 2020 15:15:54 GMT  
		Size: 101.9 MB (101906023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4478375ad1eb033b8219364f99edb05051f4adf2d66cf389f563e3f74810338`  
		Last Modified: Fri, 24 Jul 2020 15:15:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b82b669ffdbcf417e0cfbfb18f9748ff31a265e93e909bf79a5b83848d3b77c`  
		Last Modified: Fri, 24 Jul 2020 15:15:28 GMT  
		Size: 1.9 KB (1911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6828d86a7b44b30f246e15579d27ddd831a9a5e95c23822353a3e1bb4ad870a7`  
		Last Modified: Fri, 24 Jul 2020 15:15:28 GMT  
		Size: 572.4 KB (572378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba427e87d977f1d635964ca96e266aa00591aea7ebfdc2e05f36b697b1efc651`  
		Last Modified: Tue, 11 Aug 2020 20:22:25 GMT  
		Size: 113.2 MB (113233259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d2ba96a9cf2e076ea398b37ed0e9060ff9df570080291281d69e86934af0da`  
		Last Modified: Tue, 11 Aug 2020 20:22:06 GMT  
		Size: 7.6 KB (7632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae962f4f19e3a055bacdfde2a5f8c1e9caa78dea98eccce0f4f3beced547b10`  
		Last Modified: Tue, 11 Aug 2020 20:22:07 GMT  
		Size: 1.7 KB (1679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:8c01dad6734f26028c6b140de76f1a60afdcf66c3a79f08909f8180fdf158a7f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230454939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e01cc05832e6b7f271cb611727d26e9ef6ba626f5a832e14b98de2e33138867`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 24 Jul 2020 16:21:15 GMT
ADD file:146b4b3953060bbe623c06f374b3b3798872e4e1ddfef76071c7c4b69a834622 in / 
# Fri, 24 Jul 2020 16:21:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 16:21:51 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 16:23:26 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 16:23:50 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 18:34:44 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Fri, 24 Jul 2020 18:36:01 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 18:36:06 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 24 Jul 2020 18:36:08 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 24 Jul 2020 18:36:11 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 24 Jul 2020 18:36:12 GMT
ARG BONITA_VERSION
# Fri, 24 Jul 2020 18:36:13 GMT
ARG BONITA_SHA256
# Fri, 24 Jul 2020 18:36:45 GMT
ARG BASE_URL
# Fri, 24 Jul 2020 18:36:46 GMT
ARG BONITA_URL
# Tue, 11 Aug 2020 19:43:27 GMT
ENV BONITA_VERSION=7.11.1
# Tue, 11 Aug 2020 19:43:28 GMT
ENV BONITA_SHA256=d2874ada41c0549a6620ef8095c6eb7480e45d8b8143af5f983a06df62a7243d
# Tue, 11 Aug 2020 19:43:28 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 11 Aug 2020 19:43:29 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.1/BonitaCommunity-7.11.1.zip
# Tue, 11 Aug 2020 19:43:31 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Tue, 11 Aug 2020 19:43:41 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Tue, 11 Aug 2020 19:43:44 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Tue, 11 Aug 2020 19:43:46 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Tue, 11 Aug 2020 19:43:47 GMT
VOLUME [/opt/bonita]
# Tue, 11 Aug 2020 19:43:48 GMT
COPY dir:6c801c025cd750ee96a4e29676afb9ba394d4bc647bb82010816896eefc044ed in /opt/files 
# Tue, 11 Aug 2020 19:43:48 GMT
COPY dir:173a816fed2c2b9f191c45b4238f2062102518ab7cf02e5e7c4ca6bd9caeb849 in /opt/templates 
# Tue, 11 Aug 2020 19:43:49 GMT
EXPOSE 8080
# Tue, 11 Aug 2020 19:43:50 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:a114936b480795ec46632c29c96e126744c314983ee0d83354804dc39d1afb46`  
		Last Modified: Mon, 13 Jul 2020 15:47:08 GMT  
		Size: 23.7 MB (23721122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27ecf0d2a869e5d188121e6b38473e481b66599a26d8df24d22c9170f50bfa9`  
		Last Modified: Fri, 24 Jul 2020 16:27:00 GMT  
		Size: 35.2 KB (35205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4eb48eb870f62ec1a7a4a2d753bf2b92dff62a6dbedaeff6db6e41cb33196bc`  
		Last Modified: Fri, 24 Jul 2020 16:27:00 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f912b9bb20d998fd0f1a2526d5539f35d34a476da71c783d0041b25b78c0af5`  
		Last Modified: Fri, 24 Jul 2020 16:27:00 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c7aace3625d8fa13cf8b7d77fe57408818354300e46353244fef2776362c56`  
		Last Modified: Fri, 24 Jul 2020 18:38:22 GMT  
		Size: 92.9 MB (92911044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9983df6425d8cd839e1b2ae6052ea46e5ddfd942e2e822f08b65fd37b92eb2a`  
		Last Modified: Fri, 24 Jul 2020 18:37:54 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97944ca16225583c86f445ec7811306935d93a1ac397d4c6853f2322b87ce0a4`  
		Last Modified: Fri, 24 Jul 2020 18:37:52 GMT  
		Size: 1.9 KB (1918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f054d458bdf6ba532ab669977ad7f78bdddc9716ae73fde3b5f150fe598daf`  
		Last Modified: Fri, 24 Jul 2020 18:37:53 GMT  
		Size: 541.8 KB (541811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba1a71e36dea7995351642f9e6283360224eec43f3edaa20c69293bcb667b226`  
		Last Modified: Tue, 11 Aug 2020 19:44:22 GMT  
		Size: 113.2 MB (113233287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdcb9af7d9e74359515b021c960417ed4a43553d71f813ad12cf975e99217767`  
		Last Modified: Tue, 11 Aug 2020 19:44:03 GMT  
		Size: 7.7 KB (7659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db876ac2189dad6a40f9b71205d91c32a1f939cddf325f5d8ed5b7588b814a62`  
		Last Modified: Tue, 11 Aug 2020 19:44:04 GMT  
		Size: 1.7 KB (1701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:46a12d62583064b20dc5dc5e464f855bae992df10570f9c8df1f94be43646d78
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.1 MB (239115773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aed8256341d30f9f3fc82988c1bff8c667d9db5ebfa2d70769b19e54d272664d`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 24 Jul 2020 14:33:42 GMT
ADD file:d8c73324b090ba968a3efc4afc8af7d913766bd7787fc4cd6e4436895a4e564a in / 
# Fri, 24 Jul 2020 14:34:10 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:34:45 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:35:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:35:08 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 15:02:57 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Fri, 24 Jul 2020 15:15:53 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 15:18:17 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 24 Jul 2020 15:18:41 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 24 Jul 2020 15:19:19 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 24 Jul 2020 15:20:18 GMT
ARG BONITA_VERSION
# Fri, 24 Jul 2020 15:21:14 GMT
ARG BONITA_SHA256
# Fri, 24 Jul 2020 15:29:35 GMT
ARG BASE_URL
# Fri, 24 Jul 2020 15:29:45 GMT
ARG BONITA_URL
# Tue, 11 Aug 2020 20:32:59 GMT
ENV BONITA_VERSION=7.11.1
# Tue, 11 Aug 2020 20:33:12 GMT
ENV BONITA_SHA256=d2874ada41c0549a6620ef8095c6eb7480e45d8b8143af5f983a06df62a7243d
# Tue, 11 Aug 2020 20:33:21 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 11 Aug 2020 20:33:26 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.1/BonitaCommunity-7.11.1.zip
# Tue, 11 Aug 2020 20:33:52 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Tue, 11 Aug 2020 20:34:21 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Tue, 11 Aug 2020 20:34:35 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Tue, 11 Aug 2020 20:34:50 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Tue, 11 Aug 2020 20:34:59 GMT
VOLUME [/opt/bonita]
# Tue, 11 Aug 2020 20:35:02 GMT
COPY dir:6c801c025cd750ee96a4e29676afb9ba394d4bc647bb82010816896eefc044ed in /opt/files 
# Tue, 11 Aug 2020 20:35:05 GMT
COPY dir:173a816fed2c2b9f191c45b4238f2062102518ab7cf02e5e7c4ca6bd9caeb849 in /opt/templates 
# Tue, 11 Aug 2020 20:35:13 GMT
EXPOSE 8080
# Tue, 11 Aug 2020 20:35:17 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:453712c8810fcce792c21167e028047a35328679a3bd4429b8837301315e9103`  
		Last Modified: Mon, 13 Jul 2020 15:47:10 GMT  
		Size: 30.4 MB (30404926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecbb4638d99213e93a32d6945492539426ee3616d7ba413462a8b936268a56af`  
		Last Modified: Fri, 24 Jul 2020 14:41:32 GMT  
		Size: 35.2 KB (35224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b0bd277b733224c67d835643aa13dd8a9b86bcc10023a393302b3861e9a7b8`  
		Last Modified: Fri, 24 Jul 2020 14:41:32 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270c2b729d72bf4931bb8d6ccbd100e124e01bac9628380f36c2d0f13bdcc109`  
		Last Modified: Fri, 24 Jul 2020 14:41:31 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4dc874fe32813212edae7830ebd9554906d3a9802e744a6530ed9a511570f21`  
		Last Modified: Fri, 24 Jul 2020 15:36:20 GMT  
		Size: 94.9 MB (94888298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05eb40fa041d55b9cd41e2e2f1a15e457175cc3a2811e496e29307a862ec43d9`  
		Last Modified: Fri, 24 Jul 2020 15:35:57 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c80b30a08e97cf721509bb59ba0408d673fed65d3ed71f5db8036232c7504f`  
		Last Modified: Fri, 24 Jul 2020 15:35:52 GMT  
		Size: 1.9 KB (1928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a203b158d8938914a6fe005c69beb448eb02aeecdf3e4966988855eda91435`  
		Last Modified: Fri, 24 Jul 2020 15:35:52 GMT  
		Size: 541.5 KB (541549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be42801dd677c8b8b03e2272fd48e918c74558f615368d64515e5253282277c`  
		Last Modified: Tue, 11 Aug 2020 20:35:53 GMT  
		Size: 113.2 MB (113233289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf0a66d388f71754edfc41324b75df7ce8f8b57b462c023adce8efbf933c036`  
		Last Modified: Tue, 11 Aug 2020 20:35:45 GMT  
		Size: 7.7 KB (7660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6afb022459ebd3e03885dc35798a8b27ea5348111b3e99cf2292f40a249e57bf`  
		Last Modified: Tue, 11 Aug 2020 20:35:45 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.9`

```console
$ docker pull bonita@sha256:eeef3942a2f069a92e8c48c2181e881dc7242d26259fd85f1d0e3c7e56cd8a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.9` - linux; amd64

```console
$ docker pull bonita@sha256:cd3698012161087ad95bc9b4b9d9dcb1a34f64cedc4d47ab942a0a310d264994
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229248074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087af6b121177d537feede6d9c49b75587407931d98fe8902cab6913935e606c`
-	Default Command: `["\/opt\/files\/startup.sh"]`

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
# Fri, 24 Jul 2020 15:12:55 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Fri, 24 Jul 2020 15:14:04 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 15:14:05 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 24 Jul 2020 15:14:06 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 24 Jul 2020 15:14:07 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 24 Jul 2020 15:14:07 GMT
ARG BONITA_VERSION
# Fri, 24 Jul 2020 15:14:08 GMT
ARG BONITA_SHA256
# Fri, 24 Jul 2020 15:14:08 GMT
ARG BONITA_URL
# Fri, 24 Jul 2020 15:14:08 GMT
ENV BONITA_VERSION=7.9.5
# Fri, 24 Jul 2020 15:14:08 GMT
ENV BONITA_SHA256=49620e505f072a4f20ebb936c9391e8665d441df9f650749a61a19a5c52e2932
# Fri, 24 Jul 2020 15:14:08 GMT
ENV BONITA_URL=https://release.ow2.org/bonita/BonitaCommunity-7.9.5-tomcat.zip
# Fri, 24 Jul 2020 15:14:16 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip
# Fri, 24 Jul 2020 15:14:18 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip
# Fri, 24 Jul 2020 15:14:19 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip | sha256sum -c -
# Fri, 24 Jul 2020 15:14:19 GMT
VOLUME [/opt/bonita]
# Fri, 24 Jul 2020 15:14:19 GMT
COPY dir:ef58daa6df201fe2eac6b87ad183ec81a5dbb212d47f61a3244b65faca8cb3c6 in /opt/files 
# Fri, 24 Jul 2020 15:14:20 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Fri, 24 Jul 2020 15:14:20 GMT
EXPOSE 8080
# Fri, 24 Jul 2020 15:14:20 GMT
CMD ["/opt/files/startup.sh"]
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
	-	`sha256:5ce09050ccb37a91848a2410e6cf24a9d4056cc29a002e0e3043b6e4769ce8d3`  
		Last Modified: Fri, 24 Jul 2020 15:15:54 GMT  
		Size: 101.9 MB (101906023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4478375ad1eb033b8219364f99edb05051f4adf2d66cf389f563e3f74810338`  
		Last Modified: Fri, 24 Jul 2020 15:15:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b82b669ffdbcf417e0cfbfb18f9748ff31a265e93e909bf79a5b83848d3b77c`  
		Last Modified: Fri, 24 Jul 2020 15:15:28 GMT  
		Size: 1.9 KB (1911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6828d86a7b44b30f246e15579d27ddd831a9a5e95c23822353a3e1bb4ad870a7`  
		Last Modified: Fri, 24 Jul 2020 15:15:28 GMT  
		Size: 572.4 KB (572378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72316a6c2235f09e451d63a39c30a9f4aedb930e37ec4361df963d4f20c60649`  
		Last Modified: Fri, 24 Jul 2020 15:15:38 GMT  
		Size: 100.0 MB (100024958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ee97736a6624dd58105ae7c51361b5458c640ee5fbcf94b4de3ce5df92f815`  
		Last Modified: Fri, 24 Jul 2020 15:15:27 GMT  
		Size: 7.6 KB (7557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e8836bce126064a7a60fc6c01c3f6ec40cf1eaaf6f39827065291e28d3ae8e`  
		Last Modified: Fri, 24 Jul 2020 15:15:28 GMT  
		Size: 1.6 KB (1625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.9` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:ff7e9b8880ad74aefa8dd8233a06a22672446404dc00ef4b8ea794569f89a6b7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.2 MB (217246533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87705f262e956438013c2bc2a7a60e71d490228ea42a5120754eba6ca607ac12`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 24 Jul 2020 16:21:15 GMT
ADD file:146b4b3953060bbe623c06f374b3b3798872e4e1ddfef76071c7c4b69a834622 in / 
# Fri, 24 Jul 2020 16:21:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 16:21:51 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 16:23:26 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 16:23:50 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 18:34:44 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Fri, 24 Jul 2020 18:36:01 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 18:36:06 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 24 Jul 2020 18:36:08 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 24 Jul 2020 18:36:11 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 24 Jul 2020 18:36:12 GMT
ARG BONITA_VERSION
# Fri, 24 Jul 2020 18:36:13 GMT
ARG BONITA_SHA256
# Fri, 24 Jul 2020 18:36:14 GMT
ARG BONITA_URL
# Fri, 24 Jul 2020 18:36:15 GMT
ENV BONITA_VERSION=7.9.5
# Fri, 24 Jul 2020 18:36:16 GMT
ENV BONITA_SHA256=49620e505f072a4f20ebb936c9391e8665d441df9f650749a61a19a5c52e2932
# Fri, 24 Jul 2020 18:36:17 GMT
ENV BONITA_URL=https://release.ow2.org/bonita/BonitaCommunity-7.9.5-tomcat.zip
# Fri, 24 Jul 2020 18:36:26 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip
# Fri, 24 Jul 2020 18:36:29 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip
# Fri, 24 Jul 2020 18:36:32 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip | sha256sum -c -
# Fri, 24 Jul 2020 18:36:33 GMT
VOLUME [/opt/bonita]
# Fri, 24 Jul 2020 18:36:33 GMT
COPY dir:ef58daa6df201fe2eac6b87ad183ec81a5dbb212d47f61a3244b65faca8cb3c6 in /opt/files 
# Fri, 24 Jul 2020 18:36:34 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Fri, 24 Jul 2020 18:36:35 GMT
EXPOSE 8080
# Fri, 24 Jul 2020 18:36:36 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:a114936b480795ec46632c29c96e126744c314983ee0d83354804dc39d1afb46`  
		Last Modified: Mon, 13 Jul 2020 15:47:08 GMT  
		Size: 23.7 MB (23721122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27ecf0d2a869e5d188121e6b38473e481b66599a26d8df24d22c9170f50bfa9`  
		Last Modified: Fri, 24 Jul 2020 16:27:00 GMT  
		Size: 35.2 KB (35205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4eb48eb870f62ec1a7a4a2d753bf2b92dff62a6dbedaeff6db6e41cb33196bc`  
		Last Modified: Fri, 24 Jul 2020 16:27:00 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f912b9bb20d998fd0f1a2526d5539f35d34a476da71c783d0041b25b78c0af5`  
		Last Modified: Fri, 24 Jul 2020 16:27:00 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c7aace3625d8fa13cf8b7d77fe57408818354300e46353244fef2776362c56`  
		Last Modified: Fri, 24 Jul 2020 18:38:22 GMT  
		Size: 92.9 MB (92911044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9983df6425d8cd839e1b2ae6052ea46e5ddfd942e2e822f08b65fd37b92eb2a`  
		Last Modified: Fri, 24 Jul 2020 18:37:54 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97944ca16225583c86f445ec7811306935d93a1ac397d4c6853f2322b87ce0a4`  
		Last Modified: Fri, 24 Jul 2020 18:37:52 GMT  
		Size: 1.9 KB (1918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f054d458bdf6ba532ab669977ad7f78bdddc9716ae73fde3b5f150fe598daf`  
		Last Modified: Fri, 24 Jul 2020 18:37:53 GMT  
		Size: 541.8 KB (541811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afbcc9627255aba055f8e008354c24d8974770b38127357375cd45741cfdd367`  
		Last Modified: Fri, 24 Jul 2020 18:38:01 GMT  
		Size: 100.0 MB (100024999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c89fd24dd1f90fed68bdcdfb6ed67af828cfeb61351103e7185412df1c2edb0c`  
		Last Modified: Fri, 24 Jul 2020 18:37:52 GMT  
		Size: 7.6 KB (7588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91ed069328443be9a7db1dad5de04b1b4691738742ec6cf2459791a7b2a3217`  
		Last Modified: Fri, 24 Jul 2020 18:37:53 GMT  
		Size: 1.7 KB (1654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.9` - linux; ppc64le

```console
$ docker pull bonita@sha256:70f404034dc99d4b0ffcb9196d9a79c33c87a63203a79de80603f89d4a55e8be
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.9 MB (225907359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de581d98d5ebb7e96ffad56fe393b81a5862d16ddda0e6a8aa62444710f757a6`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 24 Jul 2020 14:33:42 GMT
ADD file:d8c73324b090ba968a3efc4afc8af7d913766bd7787fc4cd6e4436895a4e564a in / 
# Fri, 24 Jul 2020 14:34:10 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:34:45 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:35:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:35:08 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 15:02:57 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Fri, 24 Jul 2020 15:15:53 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 15:18:17 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 24 Jul 2020 15:18:41 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 24 Jul 2020 15:19:19 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 24 Jul 2020 15:20:18 GMT
ARG BONITA_VERSION
# Fri, 24 Jul 2020 15:21:14 GMT
ARG BONITA_SHA256
# Fri, 24 Jul 2020 15:21:43 GMT
ARG BONITA_URL
# Fri, 24 Jul 2020 15:22:38 GMT
ENV BONITA_VERSION=7.9.5
# Fri, 24 Jul 2020 15:24:13 GMT
ENV BONITA_SHA256=49620e505f072a4f20ebb936c9391e8665d441df9f650749a61a19a5c52e2932
# Fri, 24 Jul 2020 15:24:33 GMT
ENV BONITA_URL=https://release.ow2.org/bonita/BonitaCommunity-7.9.5-tomcat.zip
# Fri, 24 Jul 2020 15:26:07 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip
# Fri, 24 Jul 2020 15:26:37 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip
# Fri, 24 Jul 2020 15:27:21 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip | sha256sum -c -
# Fri, 24 Jul 2020 15:27:39 GMT
VOLUME [/opt/bonita]
# Fri, 24 Jul 2020 15:27:56 GMT
COPY dir:ef58daa6df201fe2eac6b87ad183ec81a5dbb212d47f61a3244b65faca8cb3c6 in /opt/files 
# Fri, 24 Jul 2020 15:28:07 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Fri, 24 Jul 2020 15:28:49 GMT
EXPOSE 8080
# Fri, 24 Jul 2020 15:29:00 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:453712c8810fcce792c21167e028047a35328679a3bd4429b8837301315e9103`  
		Last Modified: Mon, 13 Jul 2020 15:47:10 GMT  
		Size: 30.4 MB (30404926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecbb4638d99213e93a32d6945492539426ee3616d7ba413462a8b936268a56af`  
		Last Modified: Fri, 24 Jul 2020 14:41:32 GMT  
		Size: 35.2 KB (35224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b0bd277b733224c67d835643aa13dd8a9b86bcc10023a393302b3861e9a7b8`  
		Last Modified: Fri, 24 Jul 2020 14:41:32 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270c2b729d72bf4931bb8d6ccbd100e124e01bac9628380f36c2d0f13bdcc109`  
		Last Modified: Fri, 24 Jul 2020 14:41:31 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4dc874fe32813212edae7830ebd9554906d3a9802e744a6530ed9a511570f21`  
		Last Modified: Fri, 24 Jul 2020 15:36:20 GMT  
		Size: 94.9 MB (94888298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05eb40fa041d55b9cd41e2e2f1a15e457175cc3a2811e496e29307a862ec43d9`  
		Last Modified: Fri, 24 Jul 2020 15:35:57 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c80b30a08e97cf721509bb59ba0408d673fed65d3ed71f5db8036232c7504f`  
		Last Modified: Fri, 24 Jul 2020 15:35:52 GMT  
		Size: 1.9 KB (1928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a203b158d8938914a6fe005c69beb448eb02aeecdf3e4966988855eda91435`  
		Last Modified: Fri, 24 Jul 2020 15:35:52 GMT  
		Size: 541.5 KB (541549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66c206c26a5d5560aa39e8751f0b9214cfec83b55ba77e486056f7dbcb2ad89`  
		Last Modified: Fri, 24 Jul 2020 15:35:59 GMT  
		Size: 100.0 MB (100024999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d427418fe29ed17ce10fad53ea5a532d577fcc7c3f6682e2edae074e8030608`  
		Last Modified: Fri, 24 Jul 2020 15:35:52 GMT  
		Size: 7.6 KB (7587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f5cd9afe65492761d758d82c92bb11ea3e453f94b6ae985edf8bae6266d4f6`  
		Last Modified: Fri, 24 Jul 2020 15:35:52 GMT  
		Size: 1.7 KB (1652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.9.5`

```console
$ docker pull bonita@sha256:eeef3942a2f069a92e8c48c2181e881dc7242d26259fd85f1d0e3c7e56cd8a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.9.5` - linux; amd64

```console
$ docker pull bonita@sha256:cd3698012161087ad95bc9b4b9d9dcb1a34f64cedc4d47ab942a0a310d264994
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229248074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087af6b121177d537feede6d9c49b75587407931d98fe8902cab6913935e606c`
-	Default Command: `["\/opt\/files\/startup.sh"]`

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
# Fri, 24 Jul 2020 15:12:55 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Fri, 24 Jul 2020 15:14:04 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 15:14:05 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 24 Jul 2020 15:14:06 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 24 Jul 2020 15:14:07 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 24 Jul 2020 15:14:07 GMT
ARG BONITA_VERSION
# Fri, 24 Jul 2020 15:14:08 GMT
ARG BONITA_SHA256
# Fri, 24 Jul 2020 15:14:08 GMT
ARG BONITA_URL
# Fri, 24 Jul 2020 15:14:08 GMT
ENV BONITA_VERSION=7.9.5
# Fri, 24 Jul 2020 15:14:08 GMT
ENV BONITA_SHA256=49620e505f072a4f20ebb936c9391e8665d441df9f650749a61a19a5c52e2932
# Fri, 24 Jul 2020 15:14:08 GMT
ENV BONITA_URL=https://release.ow2.org/bonita/BonitaCommunity-7.9.5-tomcat.zip
# Fri, 24 Jul 2020 15:14:16 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip
# Fri, 24 Jul 2020 15:14:18 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip
# Fri, 24 Jul 2020 15:14:19 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip | sha256sum -c -
# Fri, 24 Jul 2020 15:14:19 GMT
VOLUME [/opt/bonita]
# Fri, 24 Jul 2020 15:14:19 GMT
COPY dir:ef58daa6df201fe2eac6b87ad183ec81a5dbb212d47f61a3244b65faca8cb3c6 in /opt/files 
# Fri, 24 Jul 2020 15:14:20 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Fri, 24 Jul 2020 15:14:20 GMT
EXPOSE 8080
# Fri, 24 Jul 2020 15:14:20 GMT
CMD ["/opt/files/startup.sh"]
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
	-	`sha256:5ce09050ccb37a91848a2410e6cf24a9d4056cc29a002e0e3043b6e4769ce8d3`  
		Last Modified: Fri, 24 Jul 2020 15:15:54 GMT  
		Size: 101.9 MB (101906023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4478375ad1eb033b8219364f99edb05051f4adf2d66cf389f563e3f74810338`  
		Last Modified: Fri, 24 Jul 2020 15:15:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b82b669ffdbcf417e0cfbfb18f9748ff31a265e93e909bf79a5b83848d3b77c`  
		Last Modified: Fri, 24 Jul 2020 15:15:28 GMT  
		Size: 1.9 KB (1911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6828d86a7b44b30f246e15579d27ddd831a9a5e95c23822353a3e1bb4ad870a7`  
		Last Modified: Fri, 24 Jul 2020 15:15:28 GMT  
		Size: 572.4 KB (572378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72316a6c2235f09e451d63a39c30a9f4aedb930e37ec4361df963d4f20c60649`  
		Last Modified: Fri, 24 Jul 2020 15:15:38 GMT  
		Size: 100.0 MB (100024958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34ee97736a6624dd58105ae7c51361b5458c640ee5fbcf94b4de3ce5df92f815`  
		Last Modified: Fri, 24 Jul 2020 15:15:27 GMT  
		Size: 7.6 KB (7557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e8836bce126064a7a60fc6c01c3f6ec40cf1eaaf6f39827065291e28d3ae8e`  
		Last Modified: Fri, 24 Jul 2020 15:15:28 GMT  
		Size: 1.6 KB (1625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.9.5` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:ff7e9b8880ad74aefa8dd8233a06a22672446404dc00ef4b8ea794569f89a6b7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.2 MB (217246533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87705f262e956438013c2bc2a7a60e71d490228ea42a5120754eba6ca607ac12`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 24 Jul 2020 16:21:15 GMT
ADD file:146b4b3953060bbe623c06f374b3b3798872e4e1ddfef76071c7c4b69a834622 in / 
# Fri, 24 Jul 2020 16:21:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 16:21:51 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 16:23:26 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 16:23:50 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 18:34:44 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Fri, 24 Jul 2020 18:36:01 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 18:36:06 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 24 Jul 2020 18:36:08 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 24 Jul 2020 18:36:11 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 24 Jul 2020 18:36:12 GMT
ARG BONITA_VERSION
# Fri, 24 Jul 2020 18:36:13 GMT
ARG BONITA_SHA256
# Fri, 24 Jul 2020 18:36:14 GMT
ARG BONITA_URL
# Fri, 24 Jul 2020 18:36:15 GMT
ENV BONITA_VERSION=7.9.5
# Fri, 24 Jul 2020 18:36:16 GMT
ENV BONITA_SHA256=49620e505f072a4f20ebb936c9391e8665d441df9f650749a61a19a5c52e2932
# Fri, 24 Jul 2020 18:36:17 GMT
ENV BONITA_URL=https://release.ow2.org/bonita/BonitaCommunity-7.9.5-tomcat.zip
# Fri, 24 Jul 2020 18:36:26 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip
# Fri, 24 Jul 2020 18:36:29 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip
# Fri, 24 Jul 2020 18:36:32 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip | sha256sum -c -
# Fri, 24 Jul 2020 18:36:33 GMT
VOLUME [/opt/bonita]
# Fri, 24 Jul 2020 18:36:33 GMT
COPY dir:ef58daa6df201fe2eac6b87ad183ec81a5dbb212d47f61a3244b65faca8cb3c6 in /opt/files 
# Fri, 24 Jul 2020 18:36:34 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Fri, 24 Jul 2020 18:36:35 GMT
EXPOSE 8080
# Fri, 24 Jul 2020 18:36:36 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:a114936b480795ec46632c29c96e126744c314983ee0d83354804dc39d1afb46`  
		Last Modified: Mon, 13 Jul 2020 15:47:08 GMT  
		Size: 23.7 MB (23721122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27ecf0d2a869e5d188121e6b38473e481b66599a26d8df24d22c9170f50bfa9`  
		Last Modified: Fri, 24 Jul 2020 16:27:00 GMT  
		Size: 35.2 KB (35205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4eb48eb870f62ec1a7a4a2d753bf2b92dff62a6dbedaeff6db6e41cb33196bc`  
		Last Modified: Fri, 24 Jul 2020 16:27:00 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f912b9bb20d998fd0f1a2526d5539f35d34a476da71c783d0041b25b78c0af5`  
		Last Modified: Fri, 24 Jul 2020 16:27:00 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c7aace3625d8fa13cf8b7d77fe57408818354300e46353244fef2776362c56`  
		Last Modified: Fri, 24 Jul 2020 18:38:22 GMT  
		Size: 92.9 MB (92911044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9983df6425d8cd839e1b2ae6052ea46e5ddfd942e2e822f08b65fd37b92eb2a`  
		Last Modified: Fri, 24 Jul 2020 18:37:54 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97944ca16225583c86f445ec7811306935d93a1ac397d4c6853f2322b87ce0a4`  
		Last Modified: Fri, 24 Jul 2020 18:37:52 GMT  
		Size: 1.9 KB (1918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f054d458bdf6ba532ab669977ad7f78bdddc9716ae73fde3b5f150fe598daf`  
		Last Modified: Fri, 24 Jul 2020 18:37:53 GMT  
		Size: 541.8 KB (541811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afbcc9627255aba055f8e008354c24d8974770b38127357375cd45741cfdd367`  
		Last Modified: Fri, 24 Jul 2020 18:38:01 GMT  
		Size: 100.0 MB (100024999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c89fd24dd1f90fed68bdcdfb6ed67af828cfeb61351103e7185412df1c2edb0c`  
		Last Modified: Fri, 24 Jul 2020 18:37:52 GMT  
		Size: 7.6 KB (7588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91ed069328443be9a7db1dad5de04b1b4691738742ec6cf2459791a7b2a3217`  
		Last Modified: Fri, 24 Jul 2020 18:37:53 GMT  
		Size: 1.7 KB (1654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.9.5` - linux; ppc64le

```console
$ docker pull bonita@sha256:70f404034dc99d4b0ffcb9196d9a79c33c87a63203a79de80603f89d4a55e8be
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.9 MB (225907359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de581d98d5ebb7e96ffad56fe393b81a5862d16ddda0e6a8aa62444710f757a6`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 24 Jul 2020 14:33:42 GMT
ADD file:d8c73324b090ba968a3efc4afc8af7d913766bd7787fc4cd6e4436895a4e564a in / 
# Fri, 24 Jul 2020 14:34:10 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:34:45 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:35:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:35:08 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 15:02:57 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Fri, 24 Jul 2020 15:15:53 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 15:18:17 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 24 Jul 2020 15:18:41 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 24 Jul 2020 15:19:19 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 24 Jul 2020 15:20:18 GMT
ARG BONITA_VERSION
# Fri, 24 Jul 2020 15:21:14 GMT
ARG BONITA_SHA256
# Fri, 24 Jul 2020 15:21:43 GMT
ARG BONITA_URL
# Fri, 24 Jul 2020 15:22:38 GMT
ENV BONITA_VERSION=7.9.5
# Fri, 24 Jul 2020 15:24:13 GMT
ENV BONITA_SHA256=49620e505f072a4f20ebb936c9391e8665d441df9f650749a61a19a5c52e2932
# Fri, 24 Jul 2020 15:24:33 GMT
ENV BONITA_URL=https://release.ow2.org/bonita/BonitaCommunity-7.9.5-tomcat.zip
# Fri, 24 Jul 2020 15:26:07 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip
# Fri, 24 Jul 2020 15:26:37 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip
# Fri, 24 Jul 2020 15:27:21 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip | sha256sum -c -
# Fri, 24 Jul 2020 15:27:39 GMT
VOLUME [/opt/bonita]
# Fri, 24 Jul 2020 15:27:56 GMT
COPY dir:ef58daa6df201fe2eac6b87ad183ec81a5dbb212d47f61a3244b65faca8cb3c6 in /opt/files 
# Fri, 24 Jul 2020 15:28:07 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Fri, 24 Jul 2020 15:28:49 GMT
EXPOSE 8080
# Fri, 24 Jul 2020 15:29:00 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:453712c8810fcce792c21167e028047a35328679a3bd4429b8837301315e9103`  
		Last Modified: Mon, 13 Jul 2020 15:47:10 GMT  
		Size: 30.4 MB (30404926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecbb4638d99213e93a32d6945492539426ee3616d7ba413462a8b936268a56af`  
		Last Modified: Fri, 24 Jul 2020 14:41:32 GMT  
		Size: 35.2 KB (35224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b0bd277b733224c67d835643aa13dd8a9b86bcc10023a393302b3861e9a7b8`  
		Last Modified: Fri, 24 Jul 2020 14:41:32 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270c2b729d72bf4931bb8d6ccbd100e124e01bac9628380f36c2d0f13bdcc109`  
		Last Modified: Fri, 24 Jul 2020 14:41:31 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4dc874fe32813212edae7830ebd9554906d3a9802e744a6530ed9a511570f21`  
		Last Modified: Fri, 24 Jul 2020 15:36:20 GMT  
		Size: 94.9 MB (94888298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05eb40fa041d55b9cd41e2e2f1a15e457175cc3a2811e496e29307a862ec43d9`  
		Last Modified: Fri, 24 Jul 2020 15:35:57 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c80b30a08e97cf721509bb59ba0408d673fed65d3ed71f5db8036232c7504f`  
		Last Modified: Fri, 24 Jul 2020 15:35:52 GMT  
		Size: 1.9 KB (1928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a203b158d8938914a6fe005c69beb448eb02aeecdf3e4966988855eda91435`  
		Last Modified: Fri, 24 Jul 2020 15:35:52 GMT  
		Size: 541.5 KB (541549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66c206c26a5d5560aa39e8751f0b9214cfec83b55ba77e486056f7dbcb2ad89`  
		Last Modified: Fri, 24 Jul 2020 15:35:59 GMT  
		Size: 100.0 MB (100024999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d427418fe29ed17ce10fad53ea5a532d577fcc7c3f6682e2edae074e8030608`  
		Last Modified: Fri, 24 Jul 2020 15:35:52 GMT  
		Size: 7.6 KB (7587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f5cd9afe65492761d758d82c92bb11ea3e453f94b6ae985edf8bae6266d4f6`  
		Last Modified: Fri, 24 Jul 2020 15:35:52 GMT  
		Size: 1.7 KB (1652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:latest`

```console
$ docker pull bonita@sha256:95b0b8db7899dcd91711cff86795f0833e6e35e378661af21439c499d4bbfcbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:latest` - linux; amd64

```console
$ docker pull bonita@sha256:46c91d9a5183e12efb3f8d355e2aba11ccdbcb73f6c8e038d6d87ed8f73ef1c8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.5 MB (242456504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f08fa01271425cc02c855e17e1d3972a08e9bb21924bee7b8e1de8c237ac9177`
-	Default Command: `["\/opt\/files\/startup.sh"]`

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
# Fri, 24 Jul 2020 15:12:55 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Fri, 24 Jul 2020 15:14:04 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 15:14:05 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 24 Jul 2020 15:14:06 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 24 Jul 2020 15:14:07 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 24 Jul 2020 15:14:07 GMT
ARG BONITA_VERSION
# Fri, 24 Jul 2020 15:14:08 GMT
ARG BONITA_SHA256
# Fri, 24 Jul 2020 15:14:27 GMT
ARG BASE_URL
# Fri, 24 Jul 2020 15:14:27 GMT
ARG BONITA_URL
# Tue, 11 Aug 2020 20:21:46 GMT
ENV BONITA_VERSION=7.11.1
# Tue, 11 Aug 2020 20:21:46 GMT
ENV BONITA_SHA256=d2874ada41c0549a6620ef8095c6eb7480e45d8b8143af5f983a06df62a7243d
# Tue, 11 Aug 2020 20:21:47 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 11 Aug 2020 20:21:47 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.1/BonitaCommunity-7.11.1.zip
# Tue, 11 Aug 2020 20:21:48 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Tue, 11 Aug 2020 20:21:53 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Tue, 11 Aug 2020 20:21:55 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Tue, 11 Aug 2020 20:21:56 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Tue, 11 Aug 2020 20:21:57 GMT
VOLUME [/opt/bonita]
# Tue, 11 Aug 2020 20:21:57 GMT
COPY dir:6c801c025cd750ee96a4e29676afb9ba394d4bc647bb82010816896eefc044ed in /opt/files 
# Tue, 11 Aug 2020 20:21:57 GMT
COPY dir:173a816fed2c2b9f191c45b4238f2062102518ab7cf02e5e7c4ca6bd9caeb849 in /opt/templates 
# Tue, 11 Aug 2020 20:21:57 GMT
EXPOSE 8080
# Tue, 11 Aug 2020 20:21:57 GMT
CMD ["/opt/files/startup.sh"]
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
	-	`sha256:5ce09050ccb37a91848a2410e6cf24a9d4056cc29a002e0e3043b6e4769ce8d3`  
		Last Modified: Fri, 24 Jul 2020 15:15:54 GMT  
		Size: 101.9 MB (101906023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4478375ad1eb033b8219364f99edb05051f4adf2d66cf389f563e3f74810338`  
		Last Modified: Fri, 24 Jul 2020 15:15:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b82b669ffdbcf417e0cfbfb18f9748ff31a265e93e909bf79a5b83848d3b77c`  
		Last Modified: Fri, 24 Jul 2020 15:15:28 GMT  
		Size: 1.9 KB (1911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6828d86a7b44b30f246e15579d27ddd831a9a5e95c23822353a3e1bb4ad870a7`  
		Last Modified: Fri, 24 Jul 2020 15:15:28 GMT  
		Size: 572.4 KB (572378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba427e87d977f1d635964ca96e266aa00591aea7ebfdc2e05f36b697b1efc651`  
		Last Modified: Tue, 11 Aug 2020 20:22:25 GMT  
		Size: 113.2 MB (113233259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d2ba96a9cf2e076ea398b37ed0e9060ff9df570080291281d69e86934af0da`  
		Last Modified: Tue, 11 Aug 2020 20:22:06 GMT  
		Size: 7.6 KB (7632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae962f4f19e3a055bacdfde2a5f8c1e9caa78dea98eccce0f4f3beced547b10`  
		Last Modified: Tue, 11 Aug 2020 20:22:07 GMT  
		Size: 1.7 KB (1679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:8c01dad6734f26028c6b140de76f1a60afdcf66c3a79f08909f8180fdf158a7f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230454939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e01cc05832e6b7f271cb611727d26e9ef6ba626f5a832e14b98de2e33138867`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 24 Jul 2020 16:21:15 GMT
ADD file:146b4b3953060bbe623c06f374b3b3798872e4e1ddfef76071c7c4b69a834622 in / 
# Fri, 24 Jul 2020 16:21:35 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 16:21:51 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 16:23:26 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 16:23:50 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 18:34:44 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Fri, 24 Jul 2020 18:36:01 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 18:36:06 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 24 Jul 2020 18:36:08 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 24 Jul 2020 18:36:11 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 24 Jul 2020 18:36:12 GMT
ARG BONITA_VERSION
# Fri, 24 Jul 2020 18:36:13 GMT
ARG BONITA_SHA256
# Fri, 24 Jul 2020 18:36:45 GMT
ARG BASE_URL
# Fri, 24 Jul 2020 18:36:46 GMT
ARG BONITA_URL
# Tue, 11 Aug 2020 19:43:27 GMT
ENV BONITA_VERSION=7.11.1
# Tue, 11 Aug 2020 19:43:28 GMT
ENV BONITA_SHA256=d2874ada41c0549a6620ef8095c6eb7480e45d8b8143af5f983a06df62a7243d
# Tue, 11 Aug 2020 19:43:28 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 11 Aug 2020 19:43:29 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.1/BonitaCommunity-7.11.1.zip
# Tue, 11 Aug 2020 19:43:31 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Tue, 11 Aug 2020 19:43:41 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Tue, 11 Aug 2020 19:43:44 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Tue, 11 Aug 2020 19:43:46 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Tue, 11 Aug 2020 19:43:47 GMT
VOLUME [/opt/bonita]
# Tue, 11 Aug 2020 19:43:48 GMT
COPY dir:6c801c025cd750ee96a4e29676afb9ba394d4bc647bb82010816896eefc044ed in /opt/files 
# Tue, 11 Aug 2020 19:43:48 GMT
COPY dir:173a816fed2c2b9f191c45b4238f2062102518ab7cf02e5e7c4ca6bd9caeb849 in /opt/templates 
# Tue, 11 Aug 2020 19:43:49 GMT
EXPOSE 8080
# Tue, 11 Aug 2020 19:43:50 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:a114936b480795ec46632c29c96e126744c314983ee0d83354804dc39d1afb46`  
		Last Modified: Mon, 13 Jul 2020 15:47:08 GMT  
		Size: 23.7 MB (23721122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27ecf0d2a869e5d188121e6b38473e481b66599a26d8df24d22c9170f50bfa9`  
		Last Modified: Fri, 24 Jul 2020 16:27:00 GMT  
		Size: 35.2 KB (35205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4eb48eb870f62ec1a7a4a2d753bf2b92dff62a6dbedaeff6db6e41cb33196bc`  
		Last Modified: Fri, 24 Jul 2020 16:27:00 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f912b9bb20d998fd0f1a2526d5539f35d34a476da71c783d0041b25b78c0af5`  
		Last Modified: Fri, 24 Jul 2020 16:27:00 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c7aace3625d8fa13cf8b7d77fe57408818354300e46353244fef2776362c56`  
		Last Modified: Fri, 24 Jul 2020 18:38:22 GMT  
		Size: 92.9 MB (92911044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9983df6425d8cd839e1b2ae6052ea46e5ddfd942e2e822f08b65fd37b92eb2a`  
		Last Modified: Fri, 24 Jul 2020 18:37:54 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97944ca16225583c86f445ec7811306935d93a1ac397d4c6853f2322b87ce0a4`  
		Last Modified: Fri, 24 Jul 2020 18:37:52 GMT  
		Size: 1.9 KB (1918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f054d458bdf6ba532ab669977ad7f78bdddc9716ae73fde3b5f150fe598daf`  
		Last Modified: Fri, 24 Jul 2020 18:37:53 GMT  
		Size: 541.8 KB (541811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba1a71e36dea7995351642f9e6283360224eec43f3edaa20c69293bcb667b226`  
		Last Modified: Tue, 11 Aug 2020 19:44:22 GMT  
		Size: 113.2 MB (113233287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdcb9af7d9e74359515b021c960417ed4a43553d71f813ad12cf975e99217767`  
		Last Modified: Tue, 11 Aug 2020 19:44:03 GMT  
		Size: 7.7 KB (7659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db876ac2189dad6a40f9b71205d91c32a1f939cddf325f5d8ed5b7588b814a62`  
		Last Modified: Tue, 11 Aug 2020 19:44:04 GMT  
		Size: 1.7 KB (1701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; ppc64le

```console
$ docker pull bonita@sha256:46a12d62583064b20dc5dc5e464f855bae992df10570f9c8df1f94be43646d78
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.1 MB (239115773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aed8256341d30f9f3fc82988c1bff8c667d9db5ebfa2d70769b19e54d272664d`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 24 Jul 2020 14:33:42 GMT
ADD file:d8c73324b090ba968a3efc4afc8af7d913766bd7787fc4cd6e4436895a4e564a in / 
# Fri, 24 Jul 2020 14:34:10 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:34:45 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:35:00 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:35:08 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 15:02:57 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Fri, 24 Jul 2020 15:15:53 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 15:18:17 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 24 Jul 2020 15:18:41 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 24 Jul 2020 15:19:19 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 24 Jul 2020 15:20:18 GMT
ARG BONITA_VERSION
# Fri, 24 Jul 2020 15:21:14 GMT
ARG BONITA_SHA256
# Fri, 24 Jul 2020 15:29:35 GMT
ARG BASE_URL
# Fri, 24 Jul 2020 15:29:45 GMT
ARG BONITA_URL
# Tue, 11 Aug 2020 20:32:59 GMT
ENV BONITA_VERSION=7.11.1
# Tue, 11 Aug 2020 20:33:12 GMT
ENV BONITA_SHA256=d2874ada41c0549a6620ef8095c6eb7480e45d8b8143af5f983a06df62a7243d
# Tue, 11 Aug 2020 20:33:21 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 11 Aug 2020 20:33:26 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.1/BonitaCommunity-7.11.1.zip
# Tue, 11 Aug 2020 20:33:52 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Tue, 11 Aug 2020 20:34:21 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Tue, 11 Aug 2020 20:34:35 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Tue, 11 Aug 2020 20:34:50 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Tue, 11 Aug 2020 20:34:59 GMT
VOLUME [/opt/bonita]
# Tue, 11 Aug 2020 20:35:02 GMT
COPY dir:6c801c025cd750ee96a4e29676afb9ba394d4bc647bb82010816896eefc044ed in /opt/files 
# Tue, 11 Aug 2020 20:35:05 GMT
COPY dir:173a816fed2c2b9f191c45b4238f2062102518ab7cf02e5e7c4ca6bd9caeb849 in /opt/templates 
# Tue, 11 Aug 2020 20:35:13 GMT
EXPOSE 8080
# Tue, 11 Aug 2020 20:35:17 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:453712c8810fcce792c21167e028047a35328679a3bd4429b8837301315e9103`  
		Last Modified: Mon, 13 Jul 2020 15:47:10 GMT  
		Size: 30.4 MB (30404926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecbb4638d99213e93a32d6945492539426ee3616d7ba413462a8b936268a56af`  
		Last Modified: Fri, 24 Jul 2020 14:41:32 GMT  
		Size: 35.2 KB (35224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b0bd277b733224c67d835643aa13dd8a9b86bcc10023a393302b3861e9a7b8`  
		Last Modified: Fri, 24 Jul 2020 14:41:32 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270c2b729d72bf4931bb8d6ccbd100e124e01bac9628380f36c2d0f13bdcc109`  
		Last Modified: Fri, 24 Jul 2020 14:41:31 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4dc874fe32813212edae7830ebd9554906d3a9802e744a6530ed9a511570f21`  
		Last Modified: Fri, 24 Jul 2020 15:36:20 GMT  
		Size: 94.9 MB (94888298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05eb40fa041d55b9cd41e2e2f1a15e457175cc3a2811e496e29307a862ec43d9`  
		Last Modified: Fri, 24 Jul 2020 15:35:57 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c80b30a08e97cf721509bb59ba0408d673fed65d3ed71f5db8036232c7504f`  
		Last Modified: Fri, 24 Jul 2020 15:35:52 GMT  
		Size: 1.9 KB (1928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a203b158d8938914a6fe005c69beb448eb02aeecdf3e4966988855eda91435`  
		Last Modified: Fri, 24 Jul 2020 15:35:52 GMT  
		Size: 541.5 KB (541549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be42801dd677c8b8b03e2272fd48e918c74558f615368d64515e5253282277c`  
		Last Modified: Tue, 11 Aug 2020 20:35:53 GMT  
		Size: 113.2 MB (113233289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf0a66d388f71754edfc41324b75df7ce8f8b57b462c023adce8efbf933c036`  
		Last Modified: Tue, 11 Aug 2020 20:35:45 GMT  
		Size: 7.7 KB (7660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6afb022459ebd3e03885dc35798a8b27ea5348111b3e99cf2292f40a249e57bf`  
		Last Modified: Tue, 11 Aug 2020 20:35:45 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
