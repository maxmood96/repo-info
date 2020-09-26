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
$ docker pull bonita@sha256:62382fa45074718ba200b4dd38d5d14fa266eb12f629a27d9ae7aeb0efe51bbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.10` - linux; amd64

```console
$ docker pull bonita@sha256:20019759ca31c4294caceb5e4b9d5d396ea89221ac601a49b9fb36243fd90564
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.2 MB (227240346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72e1ad30a6c727066b879b30ad21824fe2a9a71b60f77b04ed73830ab64f9a93`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 25 Sep 2020 22:33:49 GMT
ADD file:4974bb5483c392fb54a35f3799802d623d14632747493dce5feb4d435634b4ac in / 
# Fri, 25 Sep 2020 22:33:50 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:33:51 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:33:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:33:52 GMT
CMD ["/bin/bash"]
# Fri, 25 Sep 2020 23:41:10 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Fri, 25 Sep 2020 23:41:47 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 25 Sep 2020 23:41:48 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 25 Sep 2020 23:41:49 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 25 Sep 2020 23:41:50 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 25 Sep 2020 23:41:50 GMT
ARG BONITA_VERSION
# Fri, 25 Sep 2020 23:41:51 GMT
ARG BONITA_SHA256
# Fri, 25 Sep 2020 23:42:15 GMT
ARG BASE_URL
# Fri, 25 Sep 2020 23:42:15 GMT
ARG BONITA_URL
# Fri, 25 Sep 2020 23:42:16 GMT
ENV BONITA_VERSION=7.10.5
# Fri, 25 Sep 2020 23:42:16 GMT
ENV BONITA_SHA256=bc2bb1048df1b9d8a293635924fd1e7eb2cf0652f65d3fd64c0f1bc22e435dff
# Fri, 25 Sep 2020 23:42:16 GMT
ENV BASE_URL=https://release.ow2.org/bonita
# Fri, 25 Sep 2020 23:42:16 GMT
ENV BONITA_URL=https://release.ow2.org/bonita/BonitaCommunity-7.10.5.zip
# Fri, 25 Sep 2020 23:42:17 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Fri, 25 Sep 2020 23:42:24 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 25 Sep 2020 23:42:25 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 25 Sep 2020 23:42:27 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Fri, 25 Sep 2020 23:42:27 GMT
VOLUME [/opt/bonita]
# Fri, 25 Sep 2020 23:42:27 GMT
COPY dir:6d2b12bd97418487ddd1a174f34d85d11b3e6487e01e6d3f80d99fffcff78e82 in /opt/files 
# Fri, 25 Sep 2020 23:42:27 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Fri, 25 Sep 2020 23:42:27 GMT
EXPOSE 8080
# Fri, 25 Sep 2020 23:42:28 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:171857c49d0f5e2ebf623e6cb36a8bcad585ed0c2aa99c87a055df034c1e5848`  
		Last Modified: Tue, 22 Sep 2020 12:21:27 GMT  
		Size: 26.7 MB (26701612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419640447d267f068d2f84a093cb13a56ce77e130877f5b8bdb4294f4a90a84f`  
		Last Modified: Fri, 25 Sep 2020 22:36:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e52f862619ab016d3bcfbd78e5c7aaaa1989b4c295e6dbcacddd2d7b93e1f5`  
		Last Modified: Fri, 25 Sep 2020 22:36:49 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16b26225e2399009e0af570eebb768bfcbe84cb6c29b1904acdde559aa23f5ea`  
		Last Modified: Fri, 25 Sep 2020 23:43:07 GMT  
		Size: 102.0 MB (101998153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a756bb5a69747c3a85260b46c657b99989e66e321215246e71037a10243f35`  
		Last Modified: Fri, 25 Sep 2020 23:42:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2a72327f28ef87b1a7d940367fe2bd4bde9b327a8efe0d35fd44b7d5c19ab6`  
		Last Modified: Fri, 25 Sep 2020 23:42:49 GMT  
		Size: 1.9 KB (1913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf8ca91d922430c6fecd7439843b96ee71b8d1116fcf27a619ef4ff6b5b5f8e`  
		Last Modified: Fri, 25 Sep 2020 23:42:50 GMT  
		Size: 572.4 KB (572374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7250200ef15d13bc23204bf661f7e0cec29ddecc673ababe4036bd000195f2fe`  
		Last Modified: Fri, 25 Sep 2020 23:43:17 GMT  
		Size: 98.0 MB (97955938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4af656064e96245a0e8f267ec95e5276d4bf2124e8ee9e64f1c7c14ab7156f1`  
		Last Modified: Fri, 25 Sep 2020 23:43:12 GMT  
		Size: 7.6 KB (7595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89aa2c68c1af7f02e8647ee3d1025f9af90874b2eee82b5d659a5e223e1f2fdd`  
		Last Modified: Fri, 25 Sep 2020 23:43:12 GMT  
		Size: 1.6 KB (1625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.10` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:ebf244daa7b9ea1e52356a091e27858ce8979ef69ac80da9d46ea3dd3e577aa2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.3 MB (215250014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd84f280df0e5227c4a4220211a0b69ca75ed5b7b7f6429b339a9ea30fe88dca`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 25 Sep 2020 22:47:32 GMT
ADD file:d2c57bfbb29f6de3b29050a2c50c3806e0c8caa26f6d8dea47f479c923d72e3e in / 
# Fri, 25 Sep 2020 22:47:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:47:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:47:38 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:47:39 GMT
CMD ["/bin/bash"]
# Fri, 25 Sep 2020 23:14:35 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Fri, 25 Sep 2020 23:15:32 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 25 Sep 2020 23:15:36 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 25 Sep 2020 23:15:38 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 25 Sep 2020 23:15:41 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 25 Sep 2020 23:15:41 GMT
ARG BONITA_VERSION
# Fri, 25 Sep 2020 23:15:42 GMT
ARG BONITA_SHA256
# Fri, 25 Sep 2020 23:16:09 GMT
ARG BASE_URL
# Fri, 25 Sep 2020 23:16:09 GMT
ARG BONITA_URL
# Fri, 25 Sep 2020 23:16:10 GMT
ENV BONITA_VERSION=7.10.5
# Fri, 25 Sep 2020 23:16:11 GMT
ENV BONITA_SHA256=bc2bb1048df1b9d8a293635924fd1e7eb2cf0652f65d3fd64c0f1bc22e435dff
# Fri, 25 Sep 2020 23:16:11 GMT
ENV BASE_URL=https://release.ow2.org/bonita
# Fri, 25 Sep 2020 23:16:12 GMT
ENV BONITA_URL=https://release.ow2.org/bonita/BonitaCommunity-7.10.5.zip
# Fri, 25 Sep 2020 23:16:14 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Fri, 25 Sep 2020 23:16:21 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 25 Sep 2020 23:16:24 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 25 Sep 2020 23:16:26 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Fri, 25 Sep 2020 23:16:27 GMT
VOLUME [/opt/bonita]
# Fri, 25 Sep 2020 23:16:28 GMT
COPY dir:6d2b12bd97418487ddd1a174f34d85d11b3e6487e01e6d3f80d99fffcff78e82 in /opt/files 
# Fri, 25 Sep 2020 23:16:28 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Fri, 25 Sep 2020 23:16:29 GMT
EXPOSE 8080
# Fri, 25 Sep 2020 23:16:30 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:296c9ad75beec603486f1373addae8e2c509e94c4adda44c1289792c91624acc`  
		Last Modified: Tue, 22 Sep 2020 00:25:11 GMT  
		Size: 23.7 MB (23722853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0533d1393025aa8c38e0823a6546a0d4e5dec6b8b670758c25494c35783668d`  
		Last Modified: Fri, 25 Sep 2020 22:49:19 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c11bb34abc87247c6a70c928b7a5ef4cd48093642eb0c4b8121a674d3e278c6`  
		Last Modified: Fri, 25 Sep 2020 22:49:19 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa1dfd15710a6e16b3f5fed6c59c0bdb0a7ba405f5ba3f7ff792b76ad7d3350`  
		Last Modified: Fri, 25 Sep 2020 23:17:31 GMT  
		Size: 93.0 MB (93016994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62720c7fb3413709158ccd43c2ca056a10127529b175f1117dd4ca5a750a776`  
		Last Modified: Fri, 25 Sep 2020 23:17:06 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c12fdedbbeedcbc7e7bb2d253a8d5ddddc45dba884ced5beda6368436be77a`  
		Last Modified: Fri, 25 Sep 2020 23:17:04 GMT  
		Size: 1.9 KB (1918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4504a1dcb9b969292970b3d7cb79bbb573c83ff79706fa346afae5e2e8996f3d`  
		Last Modified: Fri, 25 Sep 2020 23:17:04 GMT  
		Size: 541.8 KB (541812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6bf3b0dd3da3a02dca79aa7825de49309c355db59cc33651d2af2fe24ca6f32`  
		Last Modified: Fri, 25 Sep 2020 23:17:46 GMT  
		Size: 98.0 MB (97955967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f9c26c59229a2bb64897fbf2182d2bce86727eac2fc3ef031417054de69a1b`  
		Last Modified: Fri, 25 Sep 2020 23:17:38 GMT  
		Size: 7.6 KB (7624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148d703c877b5cf301ef109f53dae4cf52a608e00380deb1a1a0a0961eadcfa7`  
		Last Modified: Fri, 25 Sep 2020 23:17:38 GMT  
		Size: 1.7 KB (1651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.10` - linux; ppc64le

```console
$ docker pull bonita@sha256:51d6e397d904439a18ba42ee41dd857f19084dce73158471f9b7dd50bd53e80c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.9 MB (223936455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccca660753f6f9a3668fb657318e5b28ea7ab5596105b7366a424801ac2b89a5`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 25 Sep 2020 23:47:27 GMT
ADD file:0275f43eb5902c3fb3fe4f7e8dbd20c02f6be138627bbc6770bb74283f9e35fa in / 
# Fri, 25 Sep 2020 23:47:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 23:48:12 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 23:48:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 23:48:35 GMT
CMD ["/bin/bash"]
# Sat, 26 Sep 2020 03:25:11 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Sat, 26 Sep 2020 03:29:47 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 03:30:04 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 26 Sep 2020 03:30:20 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Sat, 26 Sep 2020 03:30:33 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Sat, 26 Sep 2020 03:30:41 GMT
ARG BONITA_VERSION
# Sat, 26 Sep 2020 03:30:48 GMT
ARG BONITA_SHA256
# Sat, 26 Sep 2020 03:32:40 GMT
ARG BASE_URL
# Sat, 26 Sep 2020 03:32:44 GMT
ARG BONITA_URL
# Sat, 26 Sep 2020 03:32:50 GMT
ENV BONITA_VERSION=7.10.5
# Sat, 26 Sep 2020 03:32:52 GMT
ENV BONITA_SHA256=bc2bb1048df1b9d8a293635924fd1e7eb2cf0652f65d3fd64c0f1bc22e435dff
# Sat, 26 Sep 2020 03:32:56 GMT
ENV BASE_URL=https://release.ow2.org/bonita
# Sat, 26 Sep 2020 03:32:58 GMT
ENV BONITA_URL=https://release.ow2.org/bonita/BonitaCommunity-7.10.5.zip
# Sat, 26 Sep 2020 03:33:07 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Sat, 26 Sep 2020 03:33:28 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Sat, 26 Sep 2020 03:33:40 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Sat, 26 Sep 2020 03:33:53 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Sat, 26 Sep 2020 03:33:58 GMT
VOLUME [/opt/bonita]
# Sat, 26 Sep 2020 03:34:00 GMT
COPY dir:6d2b12bd97418487ddd1a174f34d85d11b3e6487e01e6d3f80d99fffcff78e82 in /opt/files 
# Sat, 26 Sep 2020 03:34:03 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Sat, 26 Sep 2020 03:34:06 GMT
EXPOSE 8080
# Sat, 26 Sep 2020 03:34:12 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:597e66b6a06b9db7e6c7b74196c96587c89c928a0f1bea6a5c816ed0364acca2`  
		Last Modified: Sat, 26 Sep 2020 00:05:59 GMT  
		Size: 30.4 MB (30408489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fe1993d655960561e2b7d98a72bf4167cb6bb3a934b1095c2bd170bce1b0d0`  
		Last Modified: Sat, 26 Sep 2020 00:05:07 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a85181f68a0b81866e1ec4d1fc2f161d8d57137447d2ff1d6d61bcac1974773`  
		Last Modified: Sat, 26 Sep 2020 00:05:06 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36f615abc241aa46a9f641088be9733489aa54ecdd7656aabbebc59e8babff4`  
		Last Modified: Sat, 26 Sep 2020 03:36:32 GMT  
		Size: 95.0 MB (95018057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7815598247ab5a7495520c70706e93222c19f009b14fa035185abb72878b65fb`  
		Last Modified: Sat, 26 Sep 2020 03:36:15 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b957f0e55214fe990421d5d9157a1e2b99678772069be9e9b93204567ce98e8`  
		Last Modified: Sat, 26 Sep 2020 03:36:09 GMT  
		Size: 1.9 KB (1919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d55cf6fc034ce3ae81db3086f9f903bad18df306e4078a9c4a542cf09dcf0773`  
		Last Modified: Sat, 26 Sep 2020 03:36:10 GMT  
		Size: 541.5 KB (541548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d19508b0aca15676672bddc1af8fe2e7f167d8796486c0cad01e65b70c1b6bd`  
		Last Modified: Sat, 26 Sep 2020 03:36:51 GMT  
		Size: 98.0 MB (97955971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e23b4d61123002cd0f526af79867fba561646fc3ec11f6892706857cd8d22ca`  
		Last Modified: Sat, 26 Sep 2020 03:36:44 GMT  
		Size: 7.6 KB (7621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d58575fd90b74f5f792fad2341243f772394b8c17fd8524bf1fc723a22d037`  
		Last Modified: Sat, 26 Sep 2020 03:36:44 GMT  
		Size: 1.7 KB (1652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.10.5`

```console
$ docker pull bonita@sha256:62382fa45074718ba200b4dd38d5d14fa266eb12f629a27d9ae7aeb0efe51bbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.10.5` - linux; amd64

```console
$ docker pull bonita@sha256:20019759ca31c4294caceb5e4b9d5d396ea89221ac601a49b9fb36243fd90564
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.2 MB (227240346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72e1ad30a6c727066b879b30ad21824fe2a9a71b60f77b04ed73830ab64f9a93`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 25 Sep 2020 22:33:49 GMT
ADD file:4974bb5483c392fb54a35f3799802d623d14632747493dce5feb4d435634b4ac in / 
# Fri, 25 Sep 2020 22:33:50 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:33:51 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:33:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:33:52 GMT
CMD ["/bin/bash"]
# Fri, 25 Sep 2020 23:41:10 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Fri, 25 Sep 2020 23:41:47 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 25 Sep 2020 23:41:48 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 25 Sep 2020 23:41:49 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 25 Sep 2020 23:41:50 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 25 Sep 2020 23:41:50 GMT
ARG BONITA_VERSION
# Fri, 25 Sep 2020 23:41:51 GMT
ARG BONITA_SHA256
# Fri, 25 Sep 2020 23:42:15 GMT
ARG BASE_URL
# Fri, 25 Sep 2020 23:42:15 GMT
ARG BONITA_URL
# Fri, 25 Sep 2020 23:42:16 GMT
ENV BONITA_VERSION=7.10.5
# Fri, 25 Sep 2020 23:42:16 GMT
ENV BONITA_SHA256=bc2bb1048df1b9d8a293635924fd1e7eb2cf0652f65d3fd64c0f1bc22e435dff
# Fri, 25 Sep 2020 23:42:16 GMT
ENV BASE_URL=https://release.ow2.org/bonita
# Fri, 25 Sep 2020 23:42:16 GMT
ENV BONITA_URL=https://release.ow2.org/bonita/BonitaCommunity-7.10.5.zip
# Fri, 25 Sep 2020 23:42:17 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Fri, 25 Sep 2020 23:42:24 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 25 Sep 2020 23:42:25 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 25 Sep 2020 23:42:27 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Fri, 25 Sep 2020 23:42:27 GMT
VOLUME [/opt/bonita]
# Fri, 25 Sep 2020 23:42:27 GMT
COPY dir:6d2b12bd97418487ddd1a174f34d85d11b3e6487e01e6d3f80d99fffcff78e82 in /opt/files 
# Fri, 25 Sep 2020 23:42:27 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Fri, 25 Sep 2020 23:42:27 GMT
EXPOSE 8080
# Fri, 25 Sep 2020 23:42:28 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:171857c49d0f5e2ebf623e6cb36a8bcad585ed0c2aa99c87a055df034c1e5848`  
		Last Modified: Tue, 22 Sep 2020 12:21:27 GMT  
		Size: 26.7 MB (26701612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419640447d267f068d2f84a093cb13a56ce77e130877f5b8bdb4294f4a90a84f`  
		Last Modified: Fri, 25 Sep 2020 22:36:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e52f862619ab016d3bcfbd78e5c7aaaa1989b4c295e6dbcacddd2d7b93e1f5`  
		Last Modified: Fri, 25 Sep 2020 22:36:49 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16b26225e2399009e0af570eebb768bfcbe84cb6c29b1904acdde559aa23f5ea`  
		Last Modified: Fri, 25 Sep 2020 23:43:07 GMT  
		Size: 102.0 MB (101998153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a756bb5a69747c3a85260b46c657b99989e66e321215246e71037a10243f35`  
		Last Modified: Fri, 25 Sep 2020 23:42:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2a72327f28ef87b1a7d940367fe2bd4bde9b327a8efe0d35fd44b7d5c19ab6`  
		Last Modified: Fri, 25 Sep 2020 23:42:49 GMT  
		Size: 1.9 KB (1913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf8ca91d922430c6fecd7439843b96ee71b8d1116fcf27a619ef4ff6b5b5f8e`  
		Last Modified: Fri, 25 Sep 2020 23:42:50 GMT  
		Size: 572.4 KB (572374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7250200ef15d13bc23204bf661f7e0cec29ddecc673ababe4036bd000195f2fe`  
		Last Modified: Fri, 25 Sep 2020 23:43:17 GMT  
		Size: 98.0 MB (97955938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4af656064e96245a0e8f267ec95e5276d4bf2124e8ee9e64f1c7c14ab7156f1`  
		Last Modified: Fri, 25 Sep 2020 23:43:12 GMT  
		Size: 7.6 KB (7595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89aa2c68c1af7f02e8647ee3d1025f9af90874b2eee82b5d659a5e223e1f2fdd`  
		Last Modified: Fri, 25 Sep 2020 23:43:12 GMT  
		Size: 1.6 KB (1625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.10.5` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:ebf244daa7b9ea1e52356a091e27858ce8979ef69ac80da9d46ea3dd3e577aa2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.3 MB (215250014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd84f280df0e5227c4a4220211a0b69ca75ed5b7b7f6429b339a9ea30fe88dca`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 25 Sep 2020 22:47:32 GMT
ADD file:d2c57bfbb29f6de3b29050a2c50c3806e0c8caa26f6d8dea47f479c923d72e3e in / 
# Fri, 25 Sep 2020 22:47:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:47:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:47:38 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:47:39 GMT
CMD ["/bin/bash"]
# Fri, 25 Sep 2020 23:14:35 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Fri, 25 Sep 2020 23:15:32 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 25 Sep 2020 23:15:36 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 25 Sep 2020 23:15:38 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 25 Sep 2020 23:15:41 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 25 Sep 2020 23:15:41 GMT
ARG BONITA_VERSION
# Fri, 25 Sep 2020 23:15:42 GMT
ARG BONITA_SHA256
# Fri, 25 Sep 2020 23:16:09 GMT
ARG BASE_URL
# Fri, 25 Sep 2020 23:16:09 GMT
ARG BONITA_URL
# Fri, 25 Sep 2020 23:16:10 GMT
ENV BONITA_VERSION=7.10.5
# Fri, 25 Sep 2020 23:16:11 GMT
ENV BONITA_SHA256=bc2bb1048df1b9d8a293635924fd1e7eb2cf0652f65d3fd64c0f1bc22e435dff
# Fri, 25 Sep 2020 23:16:11 GMT
ENV BASE_URL=https://release.ow2.org/bonita
# Fri, 25 Sep 2020 23:16:12 GMT
ENV BONITA_URL=https://release.ow2.org/bonita/BonitaCommunity-7.10.5.zip
# Fri, 25 Sep 2020 23:16:14 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Fri, 25 Sep 2020 23:16:21 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 25 Sep 2020 23:16:24 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 25 Sep 2020 23:16:26 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Fri, 25 Sep 2020 23:16:27 GMT
VOLUME [/opt/bonita]
# Fri, 25 Sep 2020 23:16:28 GMT
COPY dir:6d2b12bd97418487ddd1a174f34d85d11b3e6487e01e6d3f80d99fffcff78e82 in /opt/files 
# Fri, 25 Sep 2020 23:16:28 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Fri, 25 Sep 2020 23:16:29 GMT
EXPOSE 8080
# Fri, 25 Sep 2020 23:16:30 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:296c9ad75beec603486f1373addae8e2c509e94c4adda44c1289792c91624acc`  
		Last Modified: Tue, 22 Sep 2020 00:25:11 GMT  
		Size: 23.7 MB (23722853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0533d1393025aa8c38e0823a6546a0d4e5dec6b8b670758c25494c35783668d`  
		Last Modified: Fri, 25 Sep 2020 22:49:19 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c11bb34abc87247c6a70c928b7a5ef4cd48093642eb0c4b8121a674d3e278c6`  
		Last Modified: Fri, 25 Sep 2020 22:49:19 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa1dfd15710a6e16b3f5fed6c59c0bdb0a7ba405f5ba3f7ff792b76ad7d3350`  
		Last Modified: Fri, 25 Sep 2020 23:17:31 GMT  
		Size: 93.0 MB (93016994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62720c7fb3413709158ccd43c2ca056a10127529b175f1117dd4ca5a750a776`  
		Last Modified: Fri, 25 Sep 2020 23:17:06 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c12fdedbbeedcbc7e7bb2d253a8d5ddddc45dba884ced5beda6368436be77a`  
		Last Modified: Fri, 25 Sep 2020 23:17:04 GMT  
		Size: 1.9 KB (1918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4504a1dcb9b969292970b3d7cb79bbb573c83ff79706fa346afae5e2e8996f3d`  
		Last Modified: Fri, 25 Sep 2020 23:17:04 GMT  
		Size: 541.8 KB (541812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6bf3b0dd3da3a02dca79aa7825de49309c355db59cc33651d2af2fe24ca6f32`  
		Last Modified: Fri, 25 Sep 2020 23:17:46 GMT  
		Size: 98.0 MB (97955967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f9c26c59229a2bb64897fbf2182d2bce86727eac2fc3ef031417054de69a1b`  
		Last Modified: Fri, 25 Sep 2020 23:17:38 GMT  
		Size: 7.6 KB (7624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148d703c877b5cf301ef109f53dae4cf52a608e00380deb1a1a0a0961eadcfa7`  
		Last Modified: Fri, 25 Sep 2020 23:17:38 GMT  
		Size: 1.7 KB (1651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.10.5` - linux; ppc64le

```console
$ docker pull bonita@sha256:51d6e397d904439a18ba42ee41dd857f19084dce73158471f9b7dd50bd53e80c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.9 MB (223936455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccca660753f6f9a3668fb657318e5b28ea7ab5596105b7366a424801ac2b89a5`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 25 Sep 2020 23:47:27 GMT
ADD file:0275f43eb5902c3fb3fe4f7e8dbd20c02f6be138627bbc6770bb74283f9e35fa in / 
# Fri, 25 Sep 2020 23:47:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 23:48:12 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 23:48:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 23:48:35 GMT
CMD ["/bin/bash"]
# Sat, 26 Sep 2020 03:25:11 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Sat, 26 Sep 2020 03:29:47 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 03:30:04 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 26 Sep 2020 03:30:20 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Sat, 26 Sep 2020 03:30:33 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Sat, 26 Sep 2020 03:30:41 GMT
ARG BONITA_VERSION
# Sat, 26 Sep 2020 03:30:48 GMT
ARG BONITA_SHA256
# Sat, 26 Sep 2020 03:32:40 GMT
ARG BASE_URL
# Sat, 26 Sep 2020 03:32:44 GMT
ARG BONITA_URL
# Sat, 26 Sep 2020 03:32:50 GMT
ENV BONITA_VERSION=7.10.5
# Sat, 26 Sep 2020 03:32:52 GMT
ENV BONITA_SHA256=bc2bb1048df1b9d8a293635924fd1e7eb2cf0652f65d3fd64c0f1bc22e435dff
# Sat, 26 Sep 2020 03:32:56 GMT
ENV BASE_URL=https://release.ow2.org/bonita
# Sat, 26 Sep 2020 03:32:58 GMT
ENV BONITA_URL=https://release.ow2.org/bonita/BonitaCommunity-7.10.5.zip
# Sat, 26 Sep 2020 03:33:07 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Sat, 26 Sep 2020 03:33:28 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Sat, 26 Sep 2020 03:33:40 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Sat, 26 Sep 2020 03:33:53 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Sat, 26 Sep 2020 03:33:58 GMT
VOLUME [/opt/bonita]
# Sat, 26 Sep 2020 03:34:00 GMT
COPY dir:6d2b12bd97418487ddd1a174f34d85d11b3e6487e01e6d3f80d99fffcff78e82 in /opt/files 
# Sat, 26 Sep 2020 03:34:03 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Sat, 26 Sep 2020 03:34:06 GMT
EXPOSE 8080
# Sat, 26 Sep 2020 03:34:12 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:597e66b6a06b9db7e6c7b74196c96587c89c928a0f1bea6a5c816ed0364acca2`  
		Last Modified: Sat, 26 Sep 2020 00:05:59 GMT  
		Size: 30.4 MB (30408489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fe1993d655960561e2b7d98a72bf4167cb6bb3a934b1095c2bd170bce1b0d0`  
		Last Modified: Sat, 26 Sep 2020 00:05:07 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a85181f68a0b81866e1ec4d1fc2f161d8d57137447d2ff1d6d61bcac1974773`  
		Last Modified: Sat, 26 Sep 2020 00:05:06 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36f615abc241aa46a9f641088be9733489aa54ecdd7656aabbebc59e8babff4`  
		Last Modified: Sat, 26 Sep 2020 03:36:32 GMT  
		Size: 95.0 MB (95018057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7815598247ab5a7495520c70706e93222c19f009b14fa035185abb72878b65fb`  
		Last Modified: Sat, 26 Sep 2020 03:36:15 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b957f0e55214fe990421d5d9157a1e2b99678772069be9e9b93204567ce98e8`  
		Last Modified: Sat, 26 Sep 2020 03:36:09 GMT  
		Size: 1.9 KB (1919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d55cf6fc034ce3ae81db3086f9f903bad18df306e4078a9c4a542cf09dcf0773`  
		Last Modified: Sat, 26 Sep 2020 03:36:10 GMT  
		Size: 541.5 KB (541548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d19508b0aca15676672bddc1af8fe2e7f167d8796486c0cad01e65b70c1b6bd`  
		Last Modified: Sat, 26 Sep 2020 03:36:51 GMT  
		Size: 98.0 MB (97955971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e23b4d61123002cd0f526af79867fba561646fc3ec11f6892706857cd8d22ca`  
		Last Modified: Sat, 26 Sep 2020 03:36:44 GMT  
		Size: 7.6 KB (7621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d58575fd90b74f5f792fad2341243f772394b8c17fd8524bf1fc723a22d037`  
		Last Modified: Sat, 26 Sep 2020 03:36:44 GMT  
		Size: 1.7 KB (1652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.11`

```console
$ docker pull bonita@sha256:1f5f3fa2bf07396eea591d75b6172bb94e33c5940ac135217288bd7651731cda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.11` - linux; amd64

```console
$ docker pull bonita@sha256:6fb6ab9a679a3d2f3db9b798778bed62c98d768729a0accdad8e86a39f6afeac
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.5 MB (242517755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce4b71d10d9830f1ba285af9668f58b515be3b6dbdb276b7bd21ed5c1186298c`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 25 Sep 2020 22:33:49 GMT
ADD file:4974bb5483c392fb54a35f3799802d623d14632747493dce5feb4d435634b4ac in / 
# Fri, 25 Sep 2020 22:33:50 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:33:51 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:33:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:33:52 GMT
CMD ["/bin/bash"]
# Fri, 25 Sep 2020 23:41:10 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Fri, 25 Sep 2020 23:41:47 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 25 Sep 2020 23:41:48 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 25 Sep 2020 23:41:49 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 25 Sep 2020 23:41:50 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 25 Sep 2020 23:41:50 GMT
ARG BONITA_VERSION
# Fri, 25 Sep 2020 23:41:51 GMT
ARG BONITA_SHA256
# Fri, 25 Sep 2020 23:42:15 GMT
ARG BASE_URL
# Fri, 25 Sep 2020 23:42:15 GMT
ARG BONITA_URL
# Fri, 25 Sep 2020 23:42:32 GMT
ENV BONITA_VERSION=7.11.1
# Fri, 25 Sep 2020 23:42:32 GMT
ENV BONITA_SHA256=d2874ada41c0549a6620ef8095c6eb7480e45d8b8143af5f983a06df62a7243d
# Fri, 25 Sep 2020 23:42:32 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 25 Sep 2020 23:42:32 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.1/BonitaCommunity-7.11.1.zip
# Fri, 25 Sep 2020 23:42:33 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Fri, 25 Sep 2020 23:42:36 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 25 Sep 2020 23:42:38 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 25 Sep 2020 23:42:39 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Fri, 25 Sep 2020 23:42:39 GMT
VOLUME [/opt/bonita]
# Fri, 25 Sep 2020 23:42:40 GMT
COPY dir:6c801c025cd750ee96a4e29676afb9ba394d4bc647bb82010816896eefc044ed in /opt/files 
# Fri, 25 Sep 2020 23:42:40 GMT
COPY dir:173a816fed2c2b9f191c45b4238f2062102518ab7cf02e5e7c4ca6bd9caeb849 in /opt/templates 
# Fri, 25 Sep 2020 23:42:40 GMT
EXPOSE 8080
# Fri, 25 Sep 2020 23:42:40 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:171857c49d0f5e2ebf623e6cb36a8bcad585ed0c2aa99c87a055df034c1e5848`  
		Last Modified: Tue, 22 Sep 2020 12:21:27 GMT  
		Size: 26.7 MB (26701612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419640447d267f068d2f84a093cb13a56ce77e130877f5b8bdb4294f4a90a84f`  
		Last Modified: Fri, 25 Sep 2020 22:36:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e52f862619ab016d3bcfbd78e5c7aaaa1989b4c295e6dbcacddd2d7b93e1f5`  
		Last Modified: Fri, 25 Sep 2020 22:36:49 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16b26225e2399009e0af570eebb768bfcbe84cb6c29b1904acdde559aa23f5ea`  
		Last Modified: Fri, 25 Sep 2020 23:43:07 GMT  
		Size: 102.0 MB (101998153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a756bb5a69747c3a85260b46c657b99989e66e321215246e71037a10243f35`  
		Last Modified: Fri, 25 Sep 2020 23:42:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2a72327f28ef87b1a7d940367fe2bd4bde9b327a8efe0d35fd44b7d5c19ab6`  
		Last Modified: Fri, 25 Sep 2020 23:42:49 GMT  
		Size: 1.9 KB (1913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf8ca91d922430c6fecd7439843b96ee71b8d1116fcf27a619ef4ff6b5b5f8e`  
		Last Modified: Fri, 25 Sep 2020 23:42:50 GMT  
		Size: 572.4 KB (572374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14dc88aae09debc09e9c65bd505454e070b470bdc4e4678bb6a5783040b9a8e2`  
		Last Modified: Fri, 25 Sep 2020 23:43:46 GMT  
		Size: 113.2 MB (113233257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a607aa1c2a3ee7b8ce047eea9f8735289630b4af41664a5be44d033e9f5e7d`  
		Last Modified: Fri, 25 Sep 2020 23:43:22 GMT  
		Size: 7.6 KB (7632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee7861914989fd2dbf64e0f951ff8c10790c7f01dc494a587c1ef50f7c6364d5`  
		Last Modified: Fri, 25 Sep 2020 23:43:22 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:c1f456dcf7a4f2479fbfdab8758d5129c32737d0c929c347d990fc4a259cf889
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230527423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f05d1a1bf3a63e16214337af1049fef3641ed860234e11a7bbf2352266e397a1`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 25 Sep 2020 22:47:32 GMT
ADD file:d2c57bfbb29f6de3b29050a2c50c3806e0c8caa26f6d8dea47f479c923d72e3e in / 
# Fri, 25 Sep 2020 22:47:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:47:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:47:38 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:47:39 GMT
CMD ["/bin/bash"]
# Fri, 25 Sep 2020 23:14:35 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Fri, 25 Sep 2020 23:15:32 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 25 Sep 2020 23:15:36 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 25 Sep 2020 23:15:38 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 25 Sep 2020 23:15:41 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 25 Sep 2020 23:15:41 GMT
ARG BONITA_VERSION
# Fri, 25 Sep 2020 23:15:42 GMT
ARG BONITA_SHA256
# Fri, 25 Sep 2020 23:16:09 GMT
ARG BASE_URL
# Fri, 25 Sep 2020 23:16:09 GMT
ARG BONITA_URL
# Fri, 25 Sep 2020 23:16:36 GMT
ENV BONITA_VERSION=7.11.1
# Fri, 25 Sep 2020 23:16:36 GMT
ENV BONITA_SHA256=d2874ada41c0549a6620ef8095c6eb7480e45d8b8143af5f983a06df62a7243d
# Fri, 25 Sep 2020 23:16:37 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 25 Sep 2020 23:16:37 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.1/BonitaCommunity-7.11.1.zip
# Fri, 25 Sep 2020 23:16:39 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Fri, 25 Sep 2020 23:16:44 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 25 Sep 2020 23:16:46 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 25 Sep 2020 23:16:49 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Fri, 25 Sep 2020 23:16:49 GMT
VOLUME [/opt/bonita]
# Fri, 25 Sep 2020 23:16:50 GMT
COPY dir:6c801c025cd750ee96a4e29676afb9ba394d4bc647bb82010816896eefc044ed in /opt/files 
# Fri, 25 Sep 2020 23:16:51 GMT
COPY dir:173a816fed2c2b9f191c45b4238f2062102518ab7cf02e5e7c4ca6bd9caeb849 in /opt/templates 
# Fri, 25 Sep 2020 23:16:51 GMT
EXPOSE 8080
# Fri, 25 Sep 2020 23:16:52 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:296c9ad75beec603486f1373addae8e2c509e94c4adda44c1289792c91624acc`  
		Last Modified: Tue, 22 Sep 2020 00:25:11 GMT  
		Size: 23.7 MB (23722853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0533d1393025aa8c38e0823a6546a0d4e5dec6b8b670758c25494c35783668d`  
		Last Modified: Fri, 25 Sep 2020 22:49:19 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c11bb34abc87247c6a70c928b7a5ef4cd48093642eb0c4b8121a674d3e278c6`  
		Last Modified: Fri, 25 Sep 2020 22:49:19 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa1dfd15710a6e16b3f5fed6c59c0bdb0a7ba405f5ba3f7ff792b76ad7d3350`  
		Last Modified: Fri, 25 Sep 2020 23:17:31 GMT  
		Size: 93.0 MB (93016994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62720c7fb3413709158ccd43c2ca056a10127529b175f1117dd4ca5a750a776`  
		Last Modified: Fri, 25 Sep 2020 23:17:06 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c12fdedbbeedcbc7e7bb2d253a8d5ddddc45dba884ced5beda6368436be77a`  
		Last Modified: Fri, 25 Sep 2020 23:17:04 GMT  
		Size: 1.9 KB (1918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4504a1dcb9b969292970b3d7cb79bbb573c83ff79706fa346afae5e2e8996f3d`  
		Last Modified: Fri, 25 Sep 2020 23:17:04 GMT  
		Size: 541.8 KB (541812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d1203e913bc92867ce63558fd1546b825a77046054efcd9471fe9df22ea6f2`  
		Last Modified: Fri, 25 Sep 2020 23:18:05 GMT  
		Size: 113.2 MB (113233287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff67ab494944bd7fa82c77f75b4dd8a9b62d9d37509c63d5afa02bd706f2ab90`  
		Last Modified: Fri, 25 Sep 2020 23:17:55 GMT  
		Size: 7.7 KB (7659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:249bd67642b856c035b371fab214898d39e220468d7eaabc3f5fde8500104e7f`  
		Last Modified: Fri, 25 Sep 2020 23:17:55 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11` - linux; ppc64le

```console
$ docker pull bonita@sha256:66d46edd1bc0688a2411b56302eedd764b76a749a4969ddeb35969b1f205dbe1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.2 MB (239213864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35db2627251a61b3854bef40fa8b233e802938ef0e2458fd3bfae567f329e768`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 25 Sep 2020 23:47:27 GMT
ADD file:0275f43eb5902c3fb3fe4f7e8dbd20c02f6be138627bbc6770bb74283f9e35fa in / 
# Fri, 25 Sep 2020 23:47:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 23:48:12 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 23:48:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 23:48:35 GMT
CMD ["/bin/bash"]
# Sat, 26 Sep 2020 03:25:11 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Sat, 26 Sep 2020 03:29:47 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 03:30:04 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 26 Sep 2020 03:30:20 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Sat, 26 Sep 2020 03:30:33 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Sat, 26 Sep 2020 03:30:41 GMT
ARG BONITA_VERSION
# Sat, 26 Sep 2020 03:30:48 GMT
ARG BONITA_SHA256
# Sat, 26 Sep 2020 03:32:40 GMT
ARG BASE_URL
# Sat, 26 Sep 2020 03:32:44 GMT
ARG BONITA_URL
# Sat, 26 Sep 2020 03:34:18 GMT
ENV BONITA_VERSION=7.11.1
# Sat, 26 Sep 2020 03:34:21 GMT
ENV BONITA_SHA256=d2874ada41c0549a6620ef8095c6eb7480e45d8b8143af5f983a06df62a7243d
# Sat, 26 Sep 2020 03:34:24 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 26 Sep 2020 03:34:28 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.1/BonitaCommunity-7.11.1.zip
# Sat, 26 Sep 2020 03:34:39 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Sat, 26 Sep 2020 03:34:55 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Sat, 26 Sep 2020 03:35:11 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Sat, 26 Sep 2020 03:35:22 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Sat, 26 Sep 2020 03:35:32 GMT
VOLUME [/opt/bonita]
# Sat, 26 Sep 2020 03:35:40 GMT
COPY dir:6c801c025cd750ee96a4e29676afb9ba394d4bc647bb82010816896eefc044ed in /opt/files 
# Sat, 26 Sep 2020 03:35:44 GMT
COPY dir:173a816fed2c2b9f191c45b4238f2062102518ab7cf02e5e7c4ca6bd9caeb849 in /opt/templates 
# Sat, 26 Sep 2020 03:35:50 GMT
EXPOSE 8080
# Sat, 26 Sep 2020 03:35:52 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:597e66b6a06b9db7e6c7b74196c96587c89c928a0f1bea6a5c816ed0364acca2`  
		Last Modified: Sat, 26 Sep 2020 00:05:59 GMT  
		Size: 30.4 MB (30408489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fe1993d655960561e2b7d98a72bf4167cb6bb3a934b1095c2bd170bce1b0d0`  
		Last Modified: Sat, 26 Sep 2020 00:05:07 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a85181f68a0b81866e1ec4d1fc2f161d8d57137447d2ff1d6d61bcac1974773`  
		Last Modified: Sat, 26 Sep 2020 00:05:06 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36f615abc241aa46a9f641088be9733489aa54ecdd7656aabbebc59e8babff4`  
		Last Modified: Sat, 26 Sep 2020 03:36:32 GMT  
		Size: 95.0 MB (95018057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7815598247ab5a7495520c70706e93222c19f009b14fa035185abb72878b65fb`  
		Last Modified: Sat, 26 Sep 2020 03:36:15 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b957f0e55214fe990421d5d9157a1e2b99678772069be9e9b93204567ce98e8`  
		Last Modified: Sat, 26 Sep 2020 03:36:09 GMT  
		Size: 1.9 KB (1919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d55cf6fc034ce3ae81db3086f9f903bad18df306e4078a9c4a542cf09dcf0773`  
		Last Modified: Sat, 26 Sep 2020 03:36:10 GMT  
		Size: 541.5 KB (541548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3012798154cb9b4c4bd141f31561f8162243a967bde1ffa5ce1cb0cae5579027`  
		Last Modified: Sat, 26 Sep 2020 03:37:10 GMT  
		Size: 113.2 MB (113233290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c05916e1d4fe6cb9a1aff534b9c7b4b8a4f7afc77bdaa32cc53be01d3c4d1d9c`  
		Last Modified: Sat, 26 Sep 2020 03:37:02 GMT  
		Size: 7.7 KB (7660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7655426f75a9f769944586081509a83f95cd1a2f5d66d35eaf73fbf98c47451c`  
		Last Modified: Sat, 26 Sep 2020 03:37:03 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.11.1`

```console
$ docker pull bonita@sha256:1f5f3fa2bf07396eea591d75b6172bb94e33c5940ac135217288bd7651731cda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.11.1` - linux; amd64

```console
$ docker pull bonita@sha256:6fb6ab9a679a3d2f3db9b798778bed62c98d768729a0accdad8e86a39f6afeac
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.5 MB (242517755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce4b71d10d9830f1ba285af9668f58b515be3b6dbdb276b7bd21ed5c1186298c`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 25 Sep 2020 22:33:49 GMT
ADD file:4974bb5483c392fb54a35f3799802d623d14632747493dce5feb4d435634b4ac in / 
# Fri, 25 Sep 2020 22:33:50 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:33:51 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:33:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:33:52 GMT
CMD ["/bin/bash"]
# Fri, 25 Sep 2020 23:41:10 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Fri, 25 Sep 2020 23:41:47 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 25 Sep 2020 23:41:48 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 25 Sep 2020 23:41:49 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 25 Sep 2020 23:41:50 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 25 Sep 2020 23:41:50 GMT
ARG BONITA_VERSION
# Fri, 25 Sep 2020 23:41:51 GMT
ARG BONITA_SHA256
# Fri, 25 Sep 2020 23:42:15 GMT
ARG BASE_URL
# Fri, 25 Sep 2020 23:42:15 GMT
ARG BONITA_URL
# Fri, 25 Sep 2020 23:42:32 GMT
ENV BONITA_VERSION=7.11.1
# Fri, 25 Sep 2020 23:42:32 GMT
ENV BONITA_SHA256=d2874ada41c0549a6620ef8095c6eb7480e45d8b8143af5f983a06df62a7243d
# Fri, 25 Sep 2020 23:42:32 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 25 Sep 2020 23:42:32 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.1/BonitaCommunity-7.11.1.zip
# Fri, 25 Sep 2020 23:42:33 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Fri, 25 Sep 2020 23:42:36 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 25 Sep 2020 23:42:38 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 25 Sep 2020 23:42:39 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Fri, 25 Sep 2020 23:42:39 GMT
VOLUME [/opt/bonita]
# Fri, 25 Sep 2020 23:42:40 GMT
COPY dir:6c801c025cd750ee96a4e29676afb9ba394d4bc647bb82010816896eefc044ed in /opt/files 
# Fri, 25 Sep 2020 23:42:40 GMT
COPY dir:173a816fed2c2b9f191c45b4238f2062102518ab7cf02e5e7c4ca6bd9caeb849 in /opt/templates 
# Fri, 25 Sep 2020 23:42:40 GMT
EXPOSE 8080
# Fri, 25 Sep 2020 23:42:40 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:171857c49d0f5e2ebf623e6cb36a8bcad585ed0c2aa99c87a055df034c1e5848`  
		Last Modified: Tue, 22 Sep 2020 12:21:27 GMT  
		Size: 26.7 MB (26701612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419640447d267f068d2f84a093cb13a56ce77e130877f5b8bdb4294f4a90a84f`  
		Last Modified: Fri, 25 Sep 2020 22:36:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e52f862619ab016d3bcfbd78e5c7aaaa1989b4c295e6dbcacddd2d7b93e1f5`  
		Last Modified: Fri, 25 Sep 2020 22:36:49 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16b26225e2399009e0af570eebb768bfcbe84cb6c29b1904acdde559aa23f5ea`  
		Last Modified: Fri, 25 Sep 2020 23:43:07 GMT  
		Size: 102.0 MB (101998153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a756bb5a69747c3a85260b46c657b99989e66e321215246e71037a10243f35`  
		Last Modified: Fri, 25 Sep 2020 23:42:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2a72327f28ef87b1a7d940367fe2bd4bde9b327a8efe0d35fd44b7d5c19ab6`  
		Last Modified: Fri, 25 Sep 2020 23:42:49 GMT  
		Size: 1.9 KB (1913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf8ca91d922430c6fecd7439843b96ee71b8d1116fcf27a619ef4ff6b5b5f8e`  
		Last Modified: Fri, 25 Sep 2020 23:42:50 GMT  
		Size: 572.4 KB (572374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14dc88aae09debc09e9c65bd505454e070b470bdc4e4678bb6a5783040b9a8e2`  
		Last Modified: Fri, 25 Sep 2020 23:43:46 GMT  
		Size: 113.2 MB (113233257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a607aa1c2a3ee7b8ce047eea9f8735289630b4af41664a5be44d033e9f5e7d`  
		Last Modified: Fri, 25 Sep 2020 23:43:22 GMT  
		Size: 7.6 KB (7632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee7861914989fd2dbf64e0f951ff8c10790c7f01dc494a587c1ef50f7c6364d5`  
		Last Modified: Fri, 25 Sep 2020 23:43:22 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:c1f456dcf7a4f2479fbfdab8758d5129c32737d0c929c347d990fc4a259cf889
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230527423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f05d1a1bf3a63e16214337af1049fef3641ed860234e11a7bbf2352266e397a1`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 25 Sep 2020 22:47:32 GMT
ADD file:d2c57bfbb29f6de3b29050a2c50c3806e0c8caa26f6d8dea47f479c923d72e3e in / 
# Fri, 25 Sep 2020 22:47:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:47:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:47:38 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:47:39 GMT
CMD ["/bin/bash"]
# Fri, 25 Sep 2020 23:14:35 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Fri, 25 Sep 2020 23:15:32 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 25 Sep 2020 23:15:36 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 25 Sep 2020 23:15:38 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 25 Sep 2020 23:15:41 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 25 Sep 2020 23:15:41 GMT
ARG BONITA_VERSION
# Fri, 25 Sep 2020 23:15:42 GMT
ARG BONITA_SHA256
# Fri, 25 Sep 2020 23:16:09 GMT
ARG BASE_URL
# Fri, 25 Sep 2020 23:16:09 GMT
ARG BONITA_URL
# Fri, 25 Sep 2020 23:16:36 GMT
ENV BONITA_VERSION=7.11.1
# Fri, 25 Sep 2020 23:16:36 GMT
ENV BONITA_SHA256=d2874ada41c0549a6620ef8095c6eb7480e45d8b8143af5f983a06df62a7243d
# Fri, 25 Sep 2020 23:16:37 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 25 Sep 2020 23:16:37 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.1/BonitaCommunity-7.11.1.zip
# Fri, 25 Sep 2020 23:16:39 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Fri, 25 Sep 2020 23:16:44 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 25 Sep 2020 23:16:46 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 25 Sep 2020 23:16:49 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Fri, 25 Sep 2020 23:16:49 GMT
VOLUME [/opt/bonita]
# Fri, 25 Sep 2020 23:16:50 GMT
COPY dir:6c801c025cd750ee96a4e29676afb9ba394d4bc647bb82010816896eefc044ed in /opt/files 
# Fri, 25 Sep 2020 23:16:51 GMT
COPY dir:173a816fed2c2b9f191c45b4238f2062102518ab7cf02e5e7c4ca6bd9caeb849 in /opt/templates 
# Fri, 25 Sep 2020 23:16:51 GMT
EXPOSE 8080
# Fri, 25 Sep 2020 23:16:52 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:296c9ad75beec603486f1373addae8e2c509e94c4adda44c1289792c91624acc`  
		Last Modified: Tue, 22 Sep 2020 00:25:11 GMT  
		Size: 23.7 MB (23722853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0533d1393025aa8c38e0823a6546a0d4e5dec6b8b670758c25494c35783668d`  
		Last Modified: Fri, 25 Sep 2020 22:49:19 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c11bb34abc87247c6a70c928b7a5ef4cd48093642eb0c4b8121a674d3e278c6`  
		Last Modified: Fri, 25 Sep 2020 22:49:19 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa1dfd15710a6e16b3f5fed6c59c0bdb0a7ba405f5ba3f7ff792b76ad7d3350`  
		Last Modified: Fri, 25 Sep 2020 23:17:31 GMT  
		Size: 93.0 MB (93016994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62720c7fb3413709158ccd43c2ca056a10127529b175f1117dd4ca5a750a776`  
		Last Modified: Fri, 25 Sep 2020 23:17:06 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c12fdedbbeedcbc7e7bb2d253a8d5ddddc45dba884ced5beda6368436be77a`  
		Last Modified: Fri, 25 Sep 2020 23:17:04 GMT  
		Size: 1.9 KB (1918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4504a1dcb9b969292970b3d7cb79bbb573c83ff79706fa346afae5e2e8996f3d`  
		Last Modified: Fri, 25 Sep 2020 23:17:04 GMT  
		Size: 541.8 KB (541812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d1203e913bc92867ce63558fd1546b825a77046054efcd9471fe9df22ea6f2`  
		Last Modified: Fri, 25 Sep 2020 23:18:05 GMT  
		Size: 113.2 MB (113233287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff67ab494944bd7fa82c77f75b4dd8a9b62d9d37509c63d5afa02bd706f2ab90`  
		Last Modified: Fri, 25 Sep 2020 23:17:55 GMT  
		Size: 7.7 KB (7659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:249bd67642b856c035b371fab214898d39e220468d7eaabc3f5fde8500104e7f`  
		Last Modified: Fri, 25 Sep 2020 23:17:55 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:66d46edd1bc0688a2411b56302eedd764b76a749a4969ddeb35969b1f205dbe1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.2 MB (239213864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35db2627251a61b3854bef40fa8b233e802938ef0e2458fd3bfae567f329e768`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 25 Sep 2020 23:47:27 GMT
ADD file:0275f43eb5902c3fb3fe4f7e8dbd20c02f6be138627bbc6770bb74283f9e35fa in / 
# Fri, 25 Sep 2020 23:47:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 23:48:12 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 23:48:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 23:48:35 GMT
CMD ["/bin/bash"]
# Sat, 26 Sep 2020 03:25:11 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Sat, 26 Sep 2020 03:29:47 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 03:30:04 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 26 Sep 2020 03:30:20 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Sat, 26 Sep 2020 03:30:33 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Sat, 26 Sep 2020 03:30:41 GMT
ARG BONITA_VERSION
# Sat, 26 Sep 2020 03:30:48 GMT
ARG BONITA_SHA256
# Sat, 26 Sep 2020 03:32:40 GMT
ARG BASE_URL
# Sat, 26 Sep 2020 03:32:44 GMT
ARG BONITA_URL
# Sat, 26 Sep 2020 03:34:18 GMT
ENV BONITA_VERSION=7.11.1
# Sat, 26 Sep 2020 03:34:21 GMT
ENV BONITA_SHA256=d2874ada41c0549a6620ef8095c6eb7480e45d8b8143af5f983a06df62a7243d
# Sat, 26 Sep 2020 03:34:24 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 26 Sep 2020 03:34:28 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.1/BonitaCommunity-7.11.1.zip
# Sat, 26 Sep 2020 03:34:39 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Sat, 26 Sep 2020 03:34:55 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Sat, 26 Sep 2020 03:35:11 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Sat, 26 Sep 2020 03:35:22 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Sat, 26 Sep 2020 03:35:32 GMT
VOLUME [/opt/bonita]
# Sat, 26 Sep 2020 03:35:40 GMT
COPY dir:6c801c025cd750ee96a4e29676afb9ba394d4bc647bb82010816896eefc044ed in /opt/files 
# Sat, 26 Sep 2020 03:35:44 GMT
COPY dir:173a816fed2c2b9f191c45b4238f2062102518ab7cf02e5e7c4ca6bd9caeb849 in /opt/templates 
# Sat, 26 Sep 2020 03:35:50 GMT
EXPOSE 8080
# Sat, 26 Sep 2020 03:35:52 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:597e66b6a06b9db7e6c7b74196c96587c89c928a0f1bea6a5c816ed0364acca2`  
		Last Modified: Sat, 26 Sep 2020 00:05:59 GMT  
		Size: 30.4 MB (30408489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fe1993d655960561e2b7d98a72bf4167cb6bb3a934b1095c2bd170bce1b0d0`  
		Last Modified: Sat, 26 Sep 2020 00:05:07 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a85181f68a0b81866e1ec4d1fc2f161d8d57137447d2ff1d6d61bcac1974773`  
		Last Modified: Sat, 26 Sep 2020 00:05:06 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36f615abc241aa46a9f641088be9733489aa54ecdd7656aabbebc59e8babff4`  
		Last Modified: Sat, 26 Sep 2020 03:36:32 GMT  
		Size: 95.0 MB (95018057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7815598247ab5a7495520c70706e93222c19f009b14fa035185abb72878b65fb`  
		Last Modified: Sat, 26 Sep 2020 03:36:15 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b957f0e55214fe990421d5d9157a1e2b99678772069be9e9b93204567ce98e8`  
		Last Modified: Sat, 26 Sep 2020 03:36:09 GMT  
		Size: 1.9 KB (1919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d55cf6fc034ce3ae81db3086f9f903bad18df306e4078a9c4a542cf09dcf0773`  
		Last Modified: Sat, 26 Sep 2020 03:36:10 GMT  
		Size: 541.5 KB (541548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3012798154cb9b4c4bd141f31561f8162243a967bde1ffa5ce1cb0cae5579027`  
		Last Modified: Sat, 26 Sep 2020 03:37:10 GMT  
		Size: 113.2 MB (113233290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c05916e1d4fe6cb9a1aff534b9c7b4b8a4f7afc77bdaa32cc53be01d3c4d1d9c`  
		Last Modified: Sat, 26 Sep 2020 03:37:02 GMT  
		Size: 7.7 KB (7660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7655426f75a9f769944586081509a83f95cd1a2f5d66d35eaf73fbf98c47451c`  
		Last Modified: Sat, 26 Sep 2020 03:37:03 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.9`

```console
$ docker pull bonita@sha256:0267697a2f6faacd7e8cf4059dc49a9ac48676b643e98ee95d41d87e66001d20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.9` - linux; amd64

```console
$ docker pull bonita@sha256:6dd7434048c6ce0d7cf65765c2ef6536533574903972e74aaacaa548913d924a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.3 MB (229309326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ba5fb2960dd0440f3128c99af425d16d930666ab8d578eb2e7dd17518bc77c`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 25 Sep 2020 22:33:49 GMT
ADD file:4974bb5483c392fb54a35f3799802d623d14632747493dce5feb4d435634b4ac in / 
# Fri, 25 Sep 2020 22:33:50 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:33:51 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:33:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:33:52 GMT
CMD ["/bin/bash"]
# Fri, 25 Sep 2020 23:41:10 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Fri, 25 Sep 2020 23:41:47 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 25 Sep 2020 23:41:48 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 25 Sep 2020 23:41:49 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 25 Sep 2020 23:41:50 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 25 Sep 2020 23:41:50 GMT
ARG BONITA_VERSION
# Fri, 25 Sep 2020 23:41:51 GMT
ARG BONITA_SHA256
# Fri, 25 Sep 2020 23:41:51 GMT
ARG BONITA_URL
# Fri, 25 Sep 2020 23:41:51 GMT
ENV BONITA_VERSION=7.9.5
# Fri, 25 Sep 2020 23:41:51 GMT
ENV BONITA_SHA256=49620e505f072a4f20ebb936c9391e8665d441df9f650749a61a19a5c52e2932
# Fri, 25 Sep 2020 23:41:51 GMT
ENV BONITA_URL=https://release.ow2.org/bonita/BonitaCommunity-7.9.5-tomcat.zip
# Fri, 25 Sep 2020 23:42:01 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip
# Fri, 25 Sep 2020 23:42:02 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip
# Fri, 25 Sep 2020 23:42:04 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip | sha256sum -c -
# Fri, 25 Sep 2020 23:42:04 GMT
VOLUME [/opt/bonita]
# Fri, 25 Sep 2020 23:42:04 GMT
COPY dir:ef58daa6df201fe2eac6b87ad183ec81a5dbb212d47f61a3244b65faca8cb3c6 in /opt/files 
# Fri, 25 Sep 2020 23:42:04 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Fri, 25 Sep 2020 23:42:04 GMT
EXPOSE 8080
# Fri, 25 Sep 2020 23:42:05 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:171857c49d0f5e2ebf623e6cb36a8bcad585ed0c2aa99c87a055df034c1e5848`  
		Last Modified: Tue, 22 Sep 2020 12:21:27 GMT  
		Size: 26.7 MB (26701612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419640447d267f068d2f84a093cb13a56ce77e130877f5b8bdb4294f4a90a84f`  
		Last Modified: Fri, 25 Sep 2020 22:36:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e52f862619ab016d3bcfbd78e5c7aaaa1989b4c295e6dbcacddd2d7b93e1f5`  
		Last Modified: Fri, 25 Sep 2020 22:36:49 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16b26225e2399009e0af570eebb768bfcbe84cb6c29b1904acdde559aa23f5ea`  
		Last Modified: Fri, 25 Sep 2020 23:43:07 GMT  
		Size: 102.0 MB (101998153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a756bb5a69747c3a85260b46c657b99989e66e321215246e71037a10243f35`  
		Last Modified: Fri, 25 Sep 2020 23:42:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2a72327f28ef87b1a7d940367fe2bd4bde9b327a8efe0d35fd44b7d5c19ab6`  
		Last Modified: Fri, 25 Sep 2020 23:42:49 GMT  
		Size: 1.9 KB (1913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf8ca91d922430c6fecd7439843b96ee71b8d1116fcf27a619ef4ff6b5b5f8e`  
		Last Modified: Fri, 25 Sep 2020 23:42:50 GMT  
		Size: 572.4 KB (572374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76df12a7f39d6849f5acbf70ea4ca165fc6b0f07477eddf53ae0b1207ab03245`  
		Last Modified: Fri, 25 Sep 2020 23:42:56 GMT  
		Size: 100.0 MB (100024954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e92a2e89fe94010b0cdad922da1433fbeb2b714f1ea82d598a6bf82bec2b28`  
		Last Modified: Fri, 25 Sep 2020 23:42:50 GMT  
		Size: 7.6 KB (7557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf3e10066052f2a8c3180843296f3faecef55cce051176c6ab2194862c974f7`  
		Last Modified: Fri, 25 Sep 2020 23:42:50 GMT  
		Size: 1.6 KB (1627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.9` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:2b2b8fed33fbef0d3d8bdae8e9aad890ccb2035cbc00937d0eae544d125ea744
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 MB (217319007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c6f7d0f9f98b33412ff678787befd2b209860cf88c9779620078fecf18bb728`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 25 Sep 2020 22:47:32 GMT
ADD file:d2c57bfbb29f6de3b29050a2c50c3806e0c8caa26f6d8dea47f479c923d72e3e in / 
# Fri, 25 Sep 2020 22:47:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:47:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:47:38 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:47:39 GMT
CMD ["/bin/bash"]
# Fri, 25 Sep 2020 23:14:35 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Fri, 25 Sep 2020 23:15:32 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 25 Sep 2020 23:15:36 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 25 Sep 2020 23:15:38 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 25 Sep 2020 23:15:41 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 25 Sep 2020 23:15:41 GMT
ARG BONITA_VERSION
# Fri, 25 Sep 2020 23:15:42 GMT
ARG BONITA_SHA256
# Fri, 25 Sep 2020 23:15:43 GMT
ARG BONITA_URL
# Fri, 25 Sep 2020 23:15:43 GMT
ENV BONITA_VERSION=7.9.5
# Fri, 25 Sep 2020 23:15:44 GMT
ENV BONITA_SHA256=49620e505f072a4f20ebb936c9391e8665d441df9f650749a61a19a5c52e2932
# Fri, 25 Sep 2020 23:15:44 GMT
ENV BONITA_URL=https://release.ow2.org/bonita/BonitaCommunity-7.9.5-tomcat.zip
# Fri, 25 Sep 2020 23:15:54 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip
# Fri, 25 Sep 2020 23:15:57 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip
# Fri, 25 Sep 2020 23:15:59 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip | sha256sum -c -
# Fri, 25 Sep 2020 23:16:00 GMT
VOLUME [/opt/bonita]
# Fri, 25 Sep 2020 23:16:01 GMT
COPY dir:ef58daa6df201fe2eac6b87ad183ec81a5dbb212d47f61a3244b65faca8cb3c6 in /opt/files 
# Fri, 25 Sep 2020 23:16:01 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Fri, 25 Sep 2020 23:16:02 GMT
EXPOSE 8080
# Fri, 25 Sep 2020 23:16:03 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:296c9ad75beec603486f1373addae8e2c509e94c4adda44c1289792c91624acc`  
		Last Modified: Tue, 22 Sep 2020 00:25:11 GMT  
		Size: 23.7 MB (23722853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0533d1393025aa8c38e0823a6546a0d4e5dec6b8b670758c25494c35783668d`  
		Last Modified: Fri, 25 Sep 2020 22:49:19 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c11bb34abc87247c6a70c928b7a5ef4cd48093642eb0c4b8121a674d3e278c6`  
		Last Modified: Fri, 25 Sep 2020 22:49:19 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa1dfd15710a6e16b3f5fed6c59c0bdb0a7ba405f5ba3f7ff792b76ad7d3350`  
		Last Modified: Fri, 25 Sep 2020 23:17:31 GMT  
		Size: 93.0 MB (93016994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62720c7fb3413709158ccd43c2ca056a10127529b175f1117dd4ca5a750a776`  
		Last Modified: Fri, 25 Sep 2020 23:17:06 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c12fdedbbeedcbc7e7bb2d253a8d5ddddc45dba884ced5beda6368436be77a`  
		Last Modified: Fri, 25 Sep 2020 23:17:04 GMT  
		Size: 1.9 KB (1918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4504a1dcb9b969292970b3d7cb79bbb573c83ff79706fa346afae5e2e8996f3d`  
		Last Modified: Fri, 25 Sep 2020 23:17:04 GMT  
		Size: 541.8 KB (541812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba78f1892dd49488cd1e0379d04df4d330dd840a0e6a72c6d641b72056261850`  
		Last Modified: Fri, 25 Sep 2020 23:17:15 GMT  
		Size: 100.0 MB (100024998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928e8923f26cf76d52e539b56af1306b4c9ad8196e6c644b8ca542953e81cebf`  
		Last Modified: Fri, 25 Sep 2020 23:17:05 GMT  
		Size: 7.6 KB (7585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5359086d34b0cdae532bb4c1b02984b1dd86c710f69956c7bcbfa17bdcb6af9a`  
		Last Modified: Fri, 25 Sep 2020 23:17:05 GMT  
		Size: 1.7 KB (1652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.9` - linux; ppc64le

```console
$ docker pull bonita@sha256:fb96dcdef70970a0c3e0ab5901cf885c9ba983a23e7568e0e71098c23b2463dc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.0 MB (226005453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41738009cf190898409332797a8509227b6a5983c82c0d73f8068b054f6b0449`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 25 Sep 2020 23:47:27 GMT
ADD file:0275f43eb5902c3fb3fe4f7e8dbd20c02f6be138627bbc6770bb74283f9e35fa in / 
# Fri, 25 Sep 2020 23:47:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 23:48:12 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 23:48:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 23:48:35 GMT
CMD ["/bin/bash"]
# Sat, 26 Sep 2020 03:25:11 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Sat, 26 Sep 2020 03:29:47 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 03:30:04 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 26 Sep 2020 03:30:20 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Sat, 26 Sep 2020 03:30:33 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Sat, 26 Sep 2020 03:30:41 GMT
ARG BONITA_VERSION
# Sat, 26 Sep 2020 03:30:48 GMT
ARG BONITA_SHA256
# Sat, 26 Sep 2020 03:30:56 GMT
ARG BONITA_URL
# Sat, 26 Sep 2020 03:31:03 GMT
ENV BONITA_VERSION=7.9.5
# Sat, 26 Sep 2020 03:31:08 GMT
ENV BONITA_SHA256=49620e505f072a4f20ebb936c9391e8665d441df9f650749a61a19a5c52e2932
# Sat, 26 Sep 2020 03:31:14 GMT
ENV BONITA_URL=https://release.ow2.org/bonita/BonitaCommunity-7.9.5-tomcat.zip
# Sat, 26 Sep 2020 03:31:45 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip
# Sat, 26 Sep 2020 03:31:55 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip
# Sat, 26 Sep 2020 03:32:03 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip | sha256sum -c -
# Sat, 26 Sep 2020 03:32:07 GMT
VOLUME [/opt/bonita]
# Sat, 26 Sep 2020 03:32:08 GMT
COPY dir:ef58daa6df201fe2eac6b87ad183ec81a5dbb212d47f61a3244b65faca8cb3c6 in /opt/files 
# Sat, 26 Sep 2020 03:32:09 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Sat, 26 Sep 2020 03:32:12 GMT
EXPOSE 8080
# Sat, 26 Sep 2020 03:32:18 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:597e66b6a06b9db7e6c7b74196c96587c89c928a0f1bea6a5c816ed0364acca2`  
		Last Modified: Sat, 26 Sep 2020 00:05:59 GMT  
		Size: 30.4 MB (30408489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fe1993d655960561e2b7d98a72bf4167cb6bb3a934b1095c2bd170bce1b0d0`  
		Last Modified: Sat, 26 Sep 2020 00:05:07 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a85181f68a0b81866e1ec4d1fc2f161d8d57137447d2ff1d6d61bcac1974773`  
		Last Modified: Sat, 26 Sep 2020 00:05:06 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36f615abc241aa46a9f641088be9733489aa54ecdd7656aabbebc59e8babff4`  
		Last Modified: Sat, 26 Sep 2020 03:36:32 GMT  
		Size: 95.0 MB (95018057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7815598247ab5a7495520c70706e93222c19f009b14fa035185abb72878b65fb`  
		Last Modified: Sat, 26 Sep 2020 03:36:15 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b957f0e55214fe990421d5d9157a1e2b99678772069be9e9b93204567ce98e8`  
		Last Modified: Sat, 26 Sep 2020 03:36:09 GMT  
		Size: 1.9 KB (1919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d55cf6fc034ce3ae81db3086f9f903bad18df306e4078a9c4a542cf09dcf0773`  
		Last Modified: Sat, 26 Sep 2020 03:36:10 GMT  
		Size: 541.5 KB (541548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f13d3f9382602b6be6714234d241fc55503d84bd44510f2079b3780d407f12`  
		Last Modified: Sat, 26 Sep 2020 03:36:18 GMT  
		Size: 100.0 MB (100025000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e37c9bee6801e902a0424a33961cfa7f9a3d831242d28de47136f492f26f8d`  
		Last Modified: Sat, 26 Sep 2020 03:36:10 GMT  
		Size: 7.6 KB (7588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9afe094faae2bb36b5cf8883854120c3003a2059e9fbe5401cd6de59fbbf2df4`  
		Last Modified: Sat, 26 Sep 2020 03:36:09 GMT  
		Size: 1.7 KB (1654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.9.5`

```console
$ docker pull bonita@sha256:0267697a2f6faacd7e8cf4059dc49a9ac48676b643e98ee95d41d87e66001d20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.9.5` - linux; amd64

```console
$ docker pull bonita@sha256:6dd7434048c6ce0d7cf65765c2ef6536533574903972e74aaacaa548913d924a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.3 MB (229309326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ba5fb2960dd0440f3128c99af425d16d930666ab8d578eb2e7dd17518bc77c`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 25 Sep 2020 22:33:49 GMT
ADD file:4974bb5483c392fb54a35f3799802d623d14632747493dce5feb4d435634b4ac in / 
# Fri, 25 Sep 2020 22:33:50 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:33:51 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:33:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:33:52 GMT
CMD ["/bin/bash"]
# Fri, 25 Sep 2020 23:41:10 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Fri, 25 Sep 2020 23:41:47 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 25 Sep 2020 23:41:48 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 25 Sep 2020 23:41:49 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 25 Sep 2020 23:41:50 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 25 Sep 2020 23:41:50 GMT
ARG BONITA_VERSION
# Fri, 25 Sep 2020 23:41:51 GMT
ARG BONITA_SHA256
# Fri, 25 Sep 2020 23:41:51 GMT
ARG BONITA_URL
# Fri, 25 Sep 2020 23:41:51 GMT
ENV BONITA_VERSION=7.9.5
# Fri, 25 Sep 2020 23:41:51 GMT
ENV BONITA_SHA256=49620e505f072a4f20ebb936c9391e8665d441df9f650749a61a19a5c52e2932
# Fri, 25 Sep 2020 23:41:51 GMT
ENV BONITA_URL=https://release.ow2.org/bonita/BonitaCommunity-7.9.5-tomcat.zip
# Fri, 25 Sep 2020 23:42:01 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip
# Fri, 25 Sep 2020 23:42:02 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip
# Fri, 25 Sep 2020 23:42:04 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip | sha256sum -c -
# Fri, 25 Sep 2020 23:42:04 GMT
VOLUME [/opt/bonita]
# Fri, 25 Sep 2020 23:42:04 GMT
COPY dir:ef58daa6df201fe2eac6b87ad183ec81a5dbb212d47f61a3244b65faca8cb3c6 in /opt/files 
# Fri, 25 Sep 2020 23:42:04 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Fri, 25 Sep 2020 23:42:04 GMT
EXPOSE 8080
# Fri, 25 Sep 2020 23:42:05 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:171857c49d0f5e2ebf623e6cb36a8bcad585ed0c2aa99c87a055df034c1e5848`  
		Last Modified: Tue, 22 Sep 2020 12:21:27 GMT  
		Size: 26.7 MB (26701612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419640447d267f068d2f84a093cb13a56ce77e130877f5b8bdb4294f4a90a84f`  
		Last Modified: Fri, 25 Sep 2020 22:36:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e52f862619ab016d3bcfbd78e5c7aaaa1989b4c295e6dbcacddd2d7b93e1f5`  
		Last Modified: Fri, 25 Sep 2020 22:36:49 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16b26225e2399009e0af570eebb768bfcbe84cb6c29b1904acdde559aa23f5ea`  
		Last Modified: Fri, 25 Sep 2020 23:43:07 GMT  
		Size: 102.0 MB (101998153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a756bb5a69747c3a85260b46c657b99989e66e321215246e71037a10243f35`  
		Last Modified: Fri, 25 Sep 2020 23:42:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2a72327f28ef87b1a7d940367fe2bd4bde9b327a8efe0d35fd44b7d5c19ab6`  
		Last Modified: Fri, 25 Sep 2020 23:42:49 GMT  
		Size: 1.9 KB (1913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf8ca91d922430c6fecd7439843b96ee71b8d1116fcf27a619ef4ff6b5b5f8e`  
		Last Modified: Fri, 25 Sep 2020 23:42:50 GMT  
		Size: 572.4 KB (572374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76df12a7f39d6849f5acbf70ea4ca165fc6b0f07477eddf53ae0b1207ab03245`  
		Last Modified: Fri, 25 Sep 2020 23:42:56 GMT  
		Size: 100.0 MB (100024954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e92a2e89fe94010b0cdad922da1433fbeb2b714f1ea82d598a6bf82bec2b28`  
		Last Modified: Fri, 25 Sep 2020 23:42:50 GMT  
		Size: 7.6 KB (7557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf3e10066052f2a8c3180843296f3faecef55cce051176c6ab2194862c974f7`  
		Last Modified: Fri, 25 Sep 2020 23:42:50 GMT  
		Size: 1.6 KB (1627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.9.5` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:2b2b8fed33fbef0d3d8bdae8e9aad890ccb2035cbc00937d0eae544d125ea744
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 MB (217319007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c6f7d0f9f98b33412ff678787befd2b209860cf88c9779620078fecf18bb728`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 25 Sep 2020 22:47:32 GMT
ADD file:d2c57bfbb29f6de3b29050a2c50c3806e0c8caa26f6d8dea47f479c923d72e3e in / 
# Fri, 25 Sep 2020 22:47:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:47:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:47:38 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:47:39 GMT
CMD ["/bin/bash"]
# Fri, 25 Sep 2020 23:14:35 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Fri, 25 Sep 2020 23:15:32 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 25 Sep 2020 23:15:36 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 25 Sep 2020 23:15:38 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 25 Sep 2020 23:15:41 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 25 Sep 2020 23:15:41 GMT
ARG BONITA_VERSION
# Fri, 25 Sep 2020 23:15:42 GMT
ARG BONITA_SHA256
# Fri, 25 Sep 2020 23:15:43 GMT
ARG BONITA_URL
# Fri, 25 Sep 2020 23:15:43 GMT
ENV BONITA_VERSION=7.9.5
# Fri, 25 Sep 2020 23:15:44 GMT
ENV BONITA_SHA256=49620e505f072a4f20ebb936c9391e8665d441df9f650749a61a19a5c52e2932
# Fri, 25 Sep 2020 23:15:44 GMT
ENV BONITA_URL=https://release.ow2.org/bonita/BonitaCommunity-7.9.5-tomcat.zip
# Fri, 25 Sep 2020 23:15:54 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip
# Fri, 25 Sep 2020 23:15:57 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip
# Fri, 25 Sep 2020 23:15:59 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip | sha256sum -c -
# Fri, 25 Sep 2020 23:16:00 GMT
VOLUME [/opt/bonita]
# Fri, 25 Sep 2020 23:16:01 GMT
COPY dir:ef58daa6df201fe2eac6b87ad183ec81a5dbb212d47f61a3244b65faca8cb3c6 in /opt/files 
# Fri, 25 Sep 2020 23:16:01 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Fri, 25 Sep 2020 23:16:02 GMT
EXPOSE 8080
# Fri, 25 Sep 2020 23:16:03 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:296c9ad75beec603486f1373addae8e2c509e94c4adda44c1289792c91624acc`  
		Last Modified: Tue, 22 Sep 2020 00:25:11 GMT  
		Size: 23.7 MB (23722853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0533d1393025aa8c38e0823a6546a0d4e5dec6b8b670758c25494c35783668d`  
		Last Modified: Fri, 25 Sep 2020 22:49:19 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c11bb34abc87247c6a70c928b7a5ef4cd48093642eb0c4b8121a674d3e278c6`  
		Last Modified: Fri, 25 Sep 2020 22:49:19 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa1dfd15710a6e16b3f5fed6c59c0bdb0a7ba405f5ba3f7ff792b76ad7d3350`  
		Last Modified: Fri, 25 Sep 2020 23:17:31 GMT  
		Size: 93.0 MB (93016994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62720c7fb3413709158ccd43c2ca056a10127529b175f1117dd4ca5a750a776`  
		Last Modified: Fri, 25 Sep 2020 23:17:06 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c12fdedbbeedcbc7e7bb2d253a8d5ddddc45dba884ced5beda6368436be77a`  
		Last Modified: Fri, 25 Sep 2020 23:17:04 GMT  
		Size: 1.9 KB (1918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4504a1dcb9b969292970b3d7cb79bbb573c83ff79706fa346afae5e2e8996f3d`  
		Last Modified: Fri, 25 Sep 2020 23:17:04 GMT  
		Size: 541.8 KB (541812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba78f1892dd49488cd1e0379d04df4d330dd840a0e6a72c6d641b72056261850`  
		Last Modified: Fri, 25 Sep 2020 23:17:15 GMT  
		Size: 100.0 MB (100024998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928e8923f26cf76d52e539b56af1306b4c9ad8196e6c644b8ca542953e81cebf`  
		Last Modified: Fri, 25 Sep 2020 23:17:05 GMT  
		Size: 7.6 KB (7585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5359086d34b0cdae532bb4c1b02984b1dd86c710f69956c7bcbfa17bdcb6af9a`  
		Last Modified: Fri, 25 Sep 2020 23:17:05 GMT  
		Size: 1.7 KB (1652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.9.5` - linux; ppc64le

```console
$ docker pull bonita@sha256:fb96dcdef70970a0c3e0ab5901cf885c9ba983a23e7568e0e71098c23b2463dc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.0 MB (226005453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41738009cf190898409332797a8509227b6a5983c82c0d73f8068b054f6b0449`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 25 Sep 2020 23:47:27 GMT
ADD file:0275f43eb5902c3fb3fe4f7e8dbd20c02f6be138627bbc6770bb74283f9e35fa in / 
# Fri, 25 Sep 2020 23:47:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 23:48:12 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 23:48:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 23:48:35 GMT
CMD ["/bin/bash"]
# Sat, 26 Sep 2020 03:25:11 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Sat, 26 Sep 2020 03:29:47 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 03:30:04 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 26 Sep 2020 03:30:20 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Sat, 26 Sep 2020 03:30:33 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Sat, 26 Sep 2020 03:30:41 GMT
ARG BONITA_VERSION
# Sat, 26 Sep 2020 03:30:48 GMT
ARG BONITA_SHA256
# Sat, 26 Sep 2020 03:30:56 GMT
ARG BONITA_URL
# Sat, 26 Sep 2020 03:31:03 GMT
ENV BONITA_VERSION=7.9.5
# Sat, 26 Sep 2020 03:31:08 GMT
ENV BONITA_SHA256=49620e505f072a4f20ebb936c9391e8665d441df9f650749a61a19a5c52e2932
# Sat, 26 Sep 2020 03:31:14 GMT
ENV BONITA_URL=https://release.ow2.org/bonita/BonitaCommunity-7.9.5-tomcat.zip
# Sat, 26 Sep 2020 03:31:45 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip
# Sat, 26 Sep 2020 03:31:55 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip
# Sat, 26 Sep 2020 03:32:03 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}-tomcat.zip | sha256sum -c -
# Sat, 26 Sep 2020 03:32:07 GMT
VOLUME [/opt/bonita]
# Sat, 26 Sep 2020 03:32:08 GMT
COPY dir:ef58daa6df201fe2eac6b87ad183ec81a5dbb212d47f61a3244b65faca8cb3c6 in /opt/files 
# Sat, 26 Sep 2020 03:32:09 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Sat, 26 Sep 2020 03:32:12 GMT
EXPOSE 8080
# Sat, 26 Sep 2020 03:32:18 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:597e66b6a06b9db7e6c7b74196c96587c89c928a0f1bea6a5c816ed0364acca2`  
		Last Modified: Sat, 26 Sep 2020 00:05:59 GMT  
		Size: 30.4 MB (30408489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fe1993d655960561e2b7d98a72bf4167cb6bb3a934b1095c2bd170bce1b0d0`  
		Last Modified: Sat, 26 Sep 2020 00:05:07 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a85181f68a0b81866e1ec4d1fc2f161d8d57137447d2ff1d6d61bcac1974773`  
		Last Modified: Sat, 26 Sep 2020 00:05:06 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36f615abc241aa46a9f641088be9733489aa54ecdd7656aabbebc59e8babff4`  
		Last Modified: Sat, 26 Sep 2020 03:36:32 GMT  
		Size: 95.0 MB (95018057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7815598247ab5a7495520c70706e93222c19f009b14fa035185abb72878b65fb`  
		Last Modified: Sat, 26 Sep 2020 03:36:15 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b957f0e55214fe990421d5d9157a1e2b99678772069be9e9b93204567ce98e8`  
		Last Modified: Sat, 26 Sep 2020 03:36:09 GMT  
		Size: 1.9 KB (1919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d55cf6fc034ce3ae81db3086f9f903bad18df306e4078a9c4a542cf09dcf0773`  
		Last Modified: Sat, 26 Sep 2020 03:36:10 GMT  
		Size: 541.5 KB (541548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f13d3f9382602b6be6714234d241fc55503d84bd44510f2079b3780d407f12`  
		Last Modified: Sat, 26 Sep 2020 03:36:18 GMT  
		Size: 100.0 MB (100025000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e37c9bee6801e902a0424a33961cfa7f9a3d831242d28de47136f492f26f8d`  
		Last Modified: Sat, 26 Sep 2020 03:36:10 GMT  
		Size: 7.6 KB (7588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9afe094faae2bb36b5cf8883854120c3003a2059e9fbe5401cd6de59fbbf2df4`  
		Last Modified: Sat, 26 Sep 2020 03:36:09 GMT  
		Size: 1.7 KB (1654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:latest`

```console
$ docker pull bonita@sha256:1f5f3fa2bf07396eea591d75b6172bb94e33c5940ac135217288bd7651731cda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:latest` - linux; amd64

```console
$ docker pull bonita@sha256:6fb6ab9a679a3d2f3db9b798778bed62c98d768729a0accdad8e86a39f6afeac
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.5 MB (242517755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce4b71d10d9830f1ba285af9668f58b515be3b6dbdb276b7bd21ed5c1186298c`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 25 Sep 2020 22:33:49 GMT
ADD file:4974bb5483c392fb54a35f3799802d623d14632747493dce5feb4d435634b4ac in / 
# Fri, 25 Sep 2020 22:33:50 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:33:51 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:33:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:33:52 GMT
CMD ["/bin/bash"]
# Fri, 25 Sep 2020 23:41:10 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Fri, 25 Sep 2020 23:41:47 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 25 Sep 2020 23:41:48 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 25 Sep 2020 23:41:49 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 25 Sep 2020 23:41:50 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 25 Sep 2020 23:41:50 GMT
ARG BONITA_VERSION
# Fri, 25 Sep 2020 23:41:51 GMT
ARG BONITA_SHA256
# Fri, 25 Sep 2020 23:42:15 GMT
ARG BASE_URL
# Fri, 25 Sep 2020 23:42:15 GMT
ARG BONITA_URL
# Fri, 25 Sep 2020 23:42:32 GMT
ENV BONITA_VERSION=7.11.1
# Fri, 25 Sep 2020 23:42:32 GMT
ENV BONITA_SHA256=d2874ada41c0549a6620ef8095c6eb7480e45d8b8143af5f983a06df62a7243d
# Fri, 25 Sep 2020 23:42:32 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 25 Sep 2020 23:42:32 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.1/BonitaCommunity-7.11.1.zip
# Fri, 25 Sep 2020 23:42:33 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Fri, 25 Sep 2020 23:42:36 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 25 Sep 2020 23:42:38 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 25 Sep 2020 23:42:39 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Fri, 25 Sep 2020 23:42:39 GMT
VOLUME [/opt/bonita]
# Fri, 25 Sep 2020 23:42:40 GMT
COPY dir:6c801c025cd750ee96a4e29676afb9ba394d4bc647bb82010816896eefc044ed in /opt/files 
# Fri, 25 Sep 2020 23:42:40 GMT
COPY dir:173a816fed2c2b9f191c45b4238f2062102518ab7cf02e5e7c4ca6bd9caeb849 in /opt/templates 
# Fri, 25 Sep 2020 23:42:40 GMT
EXPOSE 8080
# Fri, 25 Sep 2020 23:42:40 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:171857c49d0f5e2ebf623e6cb36a8bcad585ed0c2aa99c87a055df034c1e5848`  
		Last Modified: Tue, 22 Sep 2020 12:21:27 GMT  
		Size: 26.7 MB (26701612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419640447d267f068d2f84a093cb13a56ce77e130877f5b8bdb4294f4a90a84f`  
		Last Modified: Fri, 25 Sep 2020 22:36:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e52f862619ab016d3bcfbd78e5c7aaaa1989b4c295e6dbcacddd2d7b93e1f5`  
		Last Modified: Fri, 25 Sep 2020 22:36:49 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16b26225e2399009e0af570eebb768bfcbe84cb6c29b1904acdde559aa23f5ea`  
		Last Modified: Fri, 25 Sep 2020 23:43:07 GMT  
		Size: 102.0 MB (101998153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a756bb5a69747c3a85260b46c657b99989e66e321215246e71037a10243f35`  
		Last Modified: Fri, 25 Sep 2020 23:42:50 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2a72327f28ef87b1a7d940367fe2bd4bde9b327a8efe0d35fd44b7d5c19ab6`  
		Last Modified: Fri, 25 Sep 2020 23:42:49 GMT  
		Size: 1.9 KB (1913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf8ca91d922430c6fecd7439843b96ee71b8d1116fcf27a619ef4ff6b5b5f8e`  
		Last Modified: Fri, 25 Sep 2020 23:42:50 GMT  
		Size: 572.4 KB (572374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14dc88aae09debc09e9c65bd505454e070b470bdc4e4678bb6a5783040b9a8e2`  
		Last Modified: Fri, 25 Sep 2020 23:43:46 GMT  
		Size: 113.2 MB (113233257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a607aa1c2a3ee7b8ce047eea9f8735289630b4af41664a5be44d033e9f5e7d`  
		Last Modified: Fri, 25 Sep 2020 23:43:22 GMT  
		Size: 7.6 KB (7632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee7861914989fd2dbf64e0f951ff8c10790c7f01dc494a587c1ef50f7c6364d5`  
		Last Modified: Fri, 25 Sep 2020 23:43:22 GMT  
		Size: 1.7 KB (1678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:c1f456dcf7a4f2479fbfdab8758d5129c32737d0c929c347d990fc4a259cf889
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230527423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f05d1a1bf3a63e16214337af1049fef3641ed860234e11a7bbf2352266e397a1`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 25 Sep 2020 22:47:32 GMT
ADD file:d2c57bfbb29f6de3b29050a2c50c3806e0c8caa26f6d8dea47f479c923d72e3e in / 
# Fri, 25 Sep 2020 22:47:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:47:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:47:38 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:47:39 GMT
CMD ["/bin/bash"]
# Fri, 25 Sep 2020 23:14:35 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Fri, 25 Sep 2020 23:15:32 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 25 Sep 2020 23:15:36 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 25 Sep 2020 23:15:38 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 25 Sep 2020 23:15:41 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 25 Sep 2020 23:15:41 GMT
ARG BONITA_VERSION
# Fri, 25 Sep 2020 23:15:42 GMT
ARG BONITA_SHA256
# Fri, 25 Sep 2020 23:16:09 GMT
ARG BASE_URL
# Fri, 25 Sep 2020 23:16:09 GMT
ARG BONITA_URL
# Fri, 25 Sep 2020 23:16:36 GMT
ENV BONITA_VERSION=7.11.1
# Fri, 25 Sep 2020 23:16:36 GMT
ENV BONITA_SHA256=d2874ada41c0549a6620ef8095c6eb7480e45d8b8143af5f983a06df62a7243d
# Fri, 25 Sep 2020 23:16:37 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 25 Sep 2020 23:16:37 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.1/BonitaCommunity-7.11.1.zip
# Fri, 25 Sep 2020 23:16:39 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Fri, 25 Sep 2020 23:16:44 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 25 Sep 2020 23:16:46 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 25 Sep 2020 23:16:49 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Fri, 25 Sep 2020 23:16:49 GMT
VOLUME [/opt/bonita]
# Fri, 25 Sep 2020 23:16:50 GMT
COPY dir:6c801c025cd750ee96a4e29676afb9ba394d4bc647bb82010816896eefc044ed in /opt/files 
# Fri, 25 Sep 2020 23:16:51 GMT
COPY dir:173a816fed2c2b9f191c45b4238f2062102518ab7cf02e5e7c4ca6bd9caeb849 in /opt/templates 
# Fri, 25 Sep 2020 23:16:51 GMT
EXPOSE 8080
# Fri, 25 Sep 2020 23:16:52 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:296c9ad75beec603486f1373addae8e2c509e94c4adda44c1289792c91624acc`  
		Last Modified: Tue, 22 Sep 2020 00:25:11 GMT  
		Size: 23.7 MB (23722853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0533d1393025aa8c38e0823a6546a0d4e5dec6b8b670758c25494c35783668d`  
		Last Modified: Fri, 25 Sep 2020 22:49:19 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c11bb34abc87247c6a70c928b7a5ef4cd48093642eb0c4b8121a674d3e278c6`  
		Last Modified: Fri, 25 Sep 2020 22:49:19 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa1dfd15710a6e16b3f5fed6c59c0bdb0a7ba405f5ba3f7ff792b76ad7d3350`  
		Last Modified: Fri, 25 Sep 2020 23:17:31 GMT  
		Size: 93.0 MB (93016994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62720c7fb3413709158ccd43c2ca056a10127529b175f1117dd4ca5a750a776`  
		Last Modified: Fri, 25 Sep 2020 23:17:06 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c12fdedbbeedcbc7e7bb2d253a8d5ddddc45dba884ced5beda6368436be77a`  
		Last Modified: Fri, 25 Sep 2020 23:17:04 GMT  
		Size: 1.9 KB (1918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4504a1dcb9b969292970b3d7cb79bbb573c83ff79706fa346afae5e2e8996f3d`  
		Last Modified: Fri, 25 Sep 2020 23:17:04 GMT  
		Size: 541.8 KB (541812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d1203e913bc92867ce63558fd1546b825a77046054efcd9471fe9df22ea6f2`  
		Last Modified: Fri, 25 Sep 2020 23:18:05 GMT  
		Size: 113.2 MB (113233287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff67ab494944bd7fa82c77f75b4dd8a9b62d9d37509c63d5afa02bd706f2ab90`  
		Last Modified: Fri, 25 Sep 2020 23:17:55 GMT  
		Size: 7.7 KB (7659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:249bd67642b856c035b371fab214898d39e220468d7eaabc3f5fde8500104e7f`  
		Last Modified: Fri, 25 Sep 2020 23:17:55 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; ppc64le

```console
$ docker pull bonita@sha256:66d46edd1bc0688a2411b56302eedd764b76a749a4969ddeb35969b1f205dbe1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.2 MB (239213864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35db2627251a61b3854bef40fa8b233e802938ef0e2458fd3bfae567f329e768`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 25 Sep 2020 23:47:27 GMT
ADD file:0275f43eb5902c3fb3fe4f7e8dbd20c02f6be138627bbc6770bb74283f9e35fa in / 
# Fri, 25 Sep 2020 23:47:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 23:48:12 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 23:48:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 23:48:35 GMT
CMD ["/bin/bash"]
# Sat, 26 Sep 2020 03:25:11 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Sat, 26 Sep 2020 03:29:47 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Sat, 26 Sep 2020 03:30:04 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 26 Sep 2020 03:30:20 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Sat, 26 Sep 2020 03:30:33 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Sat, 26 Sep 2020 03:30:41 GMT
ARG BONITA_VERSION
# Sat, 26 Sep 2020 03:30:48 GMT
ARG BONITA_SHA256
# Sat, 26 Sep 2020 03:32:40 GMT
ARG BASE_URL
# Sat, 26 Sep 2020 03:32:44 GMT
ARG BONITA_URL
# Sat, 26 Sep 2020 03:34:18 GMT
ENV BONITA_VERSION=7.11.1
# Sat, 26 Sep 2020 03:34:21 GMT
ENV BONITA_SHA256=d2874ada41c0549a6620ef8095c6eb7480e45d8b8143af5f983a06df62a7243d
# Sat, 26 Sep 2020 03:34:24 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 26 Sep 2020 03:34:28 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.1/BonitaCommunity-7.11.1.zip
# Sat, 26 Sep 2020 03:34:39 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Sat, 26 Sep 2020 03:34:55 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Sat, 26 Sep 2020 03:35:11 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Sat, 26 Sep 2020 03:35:22 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Sat, 26 Sep 2020 03:35:32 GMT
VOLUME [/opt/bonita]
# Sat, 26 Sep 2020 03:35:40 GMT
COPY dir:6c801c025cd750ee96a4e29676afb9ba394d4bc647bb82010816896eefc044ed in /opt/files 
# Sat, 26 Sep 2020 03:35:44 GMT
COPY dir:173a816fed2c2b9f191c45b4238f2062102518ab7cf02e5e7c4ca6bd9caeb849 in /opt/templates 
# Sat, 26 Sep 2020 03:35:50 GMT
EXPOSE 8080
# Sat, 26 Sep 2020 03:35:52 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:597e66b6a06b9db7e6c7b74196c96587c89c928a0f1bea6a5c816ed0364acca2`  
		Last Modified: Sat, 26 Sep 2020 00:05:59 GMT  
		Size: 30.4 MB (30408489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fe1993d655960561e2b7d98a72bf4167cb6bb3a934b1095c2bd170bce1b0d0`  
		Last Modified: Sat, 26 Sep 2020 00:05:07 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a85181f68a0b81866e1ec4d1fc2f161d8d57137447d2ff1d6d61bcac1974773`  
		Last Modified: Sat, 26 Sep 2020 00:05:06 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36f615abc241aa46a9f641088be9733489aa54ecdd7656aabbebc59e8babff4`  
		Last Modified: Sat, 26 Sep 2020 03:36:32 GMT  
		Size: 95.0 MB (95018057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7815598247ab5a7495520c70706e93222c19f009b14fa035185abb72878b65fb`  
		Last Modified: Sat, 26 Sep 2020 03:36:15 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b957f0e55214fe990421d5d9157a1e2b99678772069be9e9b93204567ce98e8`  
		Last Modified: Sat, 26 Sep 2020 03:36:09 GMT  
		Size: 1.9 KB (1919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d55cf6fc034ce3ae81db3086f9f903bad18df306e4078a9c4a542cf09dcf0773`  
		Last Modified: Sat, 26 Sep 2020 03:36:10 GMT  
		Size: 541.5 KB (541548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3012798154cb9b4c4bd141f31561f8162243a967bde1ffa5ce1cb0cae5579027`  
		Last Modified: Sat, 26 Sep 2020 03:37:10 GMT  
		Size: 113.2 MB (113233290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c05916e1d4fe6cb9a1aff534b9c7b4b8a4f7afc77bdaa32cc53be01d3c4d1d9c`  
		Last Modified: Sat, 26 Sep 2020 03:37:02 GMT  
		Size: 7.7 KB (7660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7655426f75a9f769944586081509a83f95cd1a2f5d66d35eaf73fbf98c47451c`  
		Last Modified: Sat, 26 Sep 2020 03:37:03 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
