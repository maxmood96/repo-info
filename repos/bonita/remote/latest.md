## `bonita:latest`

```console
$ docker pull bonita@sha256:27444e37f1e5be76f1dcf6715205e64c0a0873532eb59ad12357adc2f73dfa92
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
$ docker pull bonita@sha256:32151d03fbba1f4b824753c7fd82e9d51f37b5cceb435d01d9f4d8fb4d1b4d33
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.2 MB (239211716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a3d890fd2857568c063a6dc6f532f3fd140040f0f0c7129a95e48ef33c96d1c`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Wed, 16 Sep 2020 23:54:24 GMT
ADD file:8f9c69dc1466e3fa3f47ef42daa366ad93d6a34e816768fb8dd35e541e61b9af in / 
# Wed, 16 Sep 2020 23:54:44 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 23:54:54 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 16 Sep 2020 23:55:02 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 23:55:04 GMT
CMD ["/bin/bash"]
# Thu, 17 Sep 2020 01:50:56 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Thu, 17 Sep 2020 02:05:34 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 02:05:55 GMT
RUN mkdir /opt/custom-init.d/
# Thu, 17 Sep 2020 02:06:25 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Thu, 17 Sep 2020 02:06:44 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Thu, 17 Sep 2020 02:06:49 GMT
ARG BONITA_VERSION
# Thu, 17 Sep 2020 02:06:55 GMT
ARG BONITA_SHA256
# Thu, 17 Sep 2020 02:09:36 GMT
ARG BASE_URL
# Thu, 17 Sep 2020 02:09:41 GMT
ARG BONITA_URL
# Thu, 17 Sep 2020 02:12:50 GMT
ENV BONITA_VERSION=7.11.1
# Thu, 17 Sep 2020 02:12:57 GMT
ENV BONITA_SHA256=d2874ada41c0549a6620ef8095c6eb7480e45d8b8143af5f983a06df62a7243d
# Thu, 17 Sep 2020 02:13:05 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Thu, 17 Sep 2020 02:13:09 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.1/BonitaCommunity-7.11.1.zip
# Thu, 17 Sep 2020 02:13:25 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Thu, 17 Sep 2020 02:13:48 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Thu, 17 Sep 2020 02:14:13 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Thu, 17 Sep 2020 02:14:28 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Thu, 17 Sep 2020 02:14:35 GMT
VOLUME [/opt/bonita]
# Thu, 17 Sep 2020 02:14:38 GMT
COPY dir:6c801c025cd750ee96a4e29676afb9ba394d4bc647bb82010816896eefc044ed in /opt/files 
# Thu, 17 Sep 2020 02:14:41 GMT
COPY dir:173a816fed2c2b9f191c45b4238f2062102518ab7cf02e5e7c4ca6bd9caeb849 in /opt/templates 
# Thu, 17 Sep 2020 02:14:47 GMT
EXPOSE 8080
# Thu, 17 Sep 2020 02:14:53 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:cab4317aedcc40ff2a2f72b253d06e717095a7e3cf1c28ab1ede6b2ee2113c28`  
		Last Modified: Mon, 07 Sep 2020 15:50:42 GMT  
		Size: 30.4 MB (30407200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c62ab144e14fcd18dc307805290e556f638df374f6647d94816e4aa11f2c014a`  
		Last Modified: Thu, 17 Sep 2020 00:01:25 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ab01c61d5c7930829a28ce67f84f50f322fbb587f8c867af94413ae163e19c`  
		Last Modified: Thu, 17 Sep 2020 00:01:25 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b8d53975254c7495ad6bc50e035c9c18d0e281eb86901b49fc1ef67139e24f4`  
		Last Modified: Thu, 17 Sep 2020 02:16:09 GMT  
		Size: 95.0 MB (95017172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed7e5a8516c5d5d730faab7e6f2211cde6b56d96ad2af55a21a99ba037c845a9`  
		Last Modified: Thu, 17 Sep 2020 02:15:39 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65632cdc9b876d868d1e3ad3776ce1fbe94a3c1bc6db75f37487d8bf7db2fd42`  
		Last Modified: Thu, 17 Sep 2020 02:15:33 GMT  
		Size: 1.9 KB (1933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668f5236399dcc9ed4b0fd872ff6fe2bd95d09faf1275bd27e1082505dcdbffe`  
		Last Modified: Thu, 17 Sep 2020 02:15:33 GMT  
		Size: 541.6 KB (541557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0edfdaf3dd6a8c411ba52f34741ff920fb442769ec2e6cad345c58dcf465496`  
		Last Modified: Thu, 17 Sep 2020 02:17:09 GMT  
		Size: 113.2 MB (113233290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b23e009f1e9ee016496e3e434b48436fb04e35fb1aff7a7cf4a4a32b7a953d6`  
		Last Modified: Thu, 17 Sep 2020 02:16:54 GMT  
		Size: 7.7 KB (7659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edb1183649e643a376e8ce1143b37932d62de0176530a0ab8421b8ee0d504a9d`  
		Last Modified: Thu, 17 Sep 2020 02:16:55 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
