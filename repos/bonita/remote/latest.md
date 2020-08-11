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
