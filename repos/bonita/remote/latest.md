## `bonita:latest`

```console
$ docker pull bonita@sha256:1d9b7cb3f296e18dcc2e45222a30dd4255c21eb699b68466ebac5d22b3c09964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:latest` - linux; amd64

```console
$ docker pull bonita@sha256:6c198d50123572fe10e314fea73e800dfc74e9b71ba8de3fb8fa1251f57b9c2d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.1 MB (227091253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f82bb7ab24d4761ea134eafa8e198e4f389d473c226b670d9f52432a4a722601`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 24 Apr 2020 01:07:00 GMT
ADD file:c3e6bb316dfa6b81dd4478aaa310df532883b1c0a14edeec3f63d641980c1789 in / 
# Fri, 24 Apr 2020 01:07:02 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 01:07:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 01:07:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 01:07:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 19:25:29 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Fri, 24 Apr 2020 19:26:25 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 19:26:26 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 24 Apr 2020 19:26:27 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 24 Apr 2020 19:26:29 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 24 Apr 2020 19:26:29 GMT
ARG BONITA_VERSION
# Fri, 24 Apr 2020 19:26:29 GMT
ARG BONITA_SHA256
# Fri, 24 Apr 2020 19:26:46 GMT
ARG BASE_URL
# Fri, 24 Apr 2020 19:26:46 GMT
ARG BONITA_URL
# Fri, 24 Apr 2020 19:26:46 GMT
ENV BONITA_VERSION=7.10.4
# Fri, 24 Apr 2020 19:26:46 GMT
ENV BONITA_SHA256=dfc3d6d43a6fda7e0e57a60238e63c754d1a948f3c3e36f460f9c7867bf25d6d
# Fri, 24 Apr 2020 19:26:46 GMT
ENV BASE_URL=https://release.ow2.org/bonita
# Fri, 24 Apr 2020 19:26:46 GMT
ENV BONITA_URL=https://release.ow2.org/bonita/BonitaCommunity-7.10.4.zip
# Fri, 24 Apr 2020 19:26:47 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Fri, 24 Apr 2020 19:26:54 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 24 Apr 2020 19:26:55 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 24 Apr 2020 19:26:58 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Fri, 24 Apr 2020 19:26:58 GMT
VOLUME [/opt/bonita]
# Fri, 24 Apr 2020 19:26:59 GMT
COPY dir:6d2b12bd97418487ddd1a174f34d85d11b3e6487e01e6d3f80d99fffcff78e82 in /opt/files 
# Fri, 24 Apr 2020 19:26:59 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Fri, 24 Apr 2020 19:26:59 GMT
EXPOSE 8080
# Fri, 24 Apr 2020 19:26:59 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:23884877105a7ff84a910895cd044061a4561385ff6c36480ee080b76ec0e771`  
		Last Modified: Sat, 04 Apr 2020 12:21:10 GMT  
		Size: 26.7 MB (26689802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc38caa0f5b94141276220daaf428892096e4afd24b05668cd188311e00a635f`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 35.4 KB (35367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2910811b6c4227c2f42aaea9a3dd5f53b1d469f67e2cf7e601f631b119b61ff7`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36505266dcc64eeb1010bd2112e6f73981e1a8246e4f6d4e287763b57f101b0b`  
		Last Modified: Fri, 24 Apr 2020 01:09:01 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4748d542eda84f306cc6eb9f3f51be6b5412ec5d0d67f1ab602d6557a6843280`  
		Last Modified: Fri, 24 Apr 2020 19:27:25 GMT  
		Size: 101.9 MB (101887135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:965bcbac7979a0c071d6ca1fb66bd0ac6879c1d6fa3ad6ccc8d0cea03e1d8579`  
		Last Modified: Fri, 24 Apr 2020 19:27:09 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5b730e2c806c3ca4c3bbc61db27511d4c145e3053704923d002870ec5945d6`  
		Last Modified: Fri, 24 Apr 2020 19:27:08 GMT  
		Size: 1.9 KB (1911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32d26769757fa92716d732b7ca3cd9dee3360084cb8dc372af00ab32aab2413`  
		Last Modified: Fri, 24 Apr 2020 19:27:08 GMT  
		Size: 572.4 KB (572381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bc307610171d9b974f1b24b72a59edbc014a345e5ad2ca10bb251c8d8c3c2a4`  
		Last Modified: Fri, 24 Apr 2020 19:27:37 GMT  
		Size: 97.9 MB (97894308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:732124ac9af354031c85fcc18ee0457d43aba188a34ff0b2d252f15fe0966de1`  
		Last Modified: Fri, 24 Apr 2020 19:27:31 GMT  
		Size: 7.6 KB (7594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6891723654081f2439b344cf392b0a28427ade0ac6e8d211b04ffece4568056`  
		Last Modified: Fri, 24 Apr 2020 19:27:30 GMT  
		Size: 1.6 KB (1625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:5cce3f8e49539011d82f8bbedb4e6b9969d26536c07f5b0ca68e29fc38922714
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.2 MB (215159921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75bb57298ce381c9294214b3b0b1550f18e082840ce2e7e63c01fe7205a67c33`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 24 Apr 2020 00:16:45 GMT
ADD file:bd5b3470601aa4a28132ec60a8b1c33516d09a1391864fe1dbf82a4030397fd1 in / 
# Fri, 24 Apr 2020 00:16:54 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Apr 2020 00:16:58 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 00:17:03 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 00:17:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 14:49:47 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Fri, 24 Apr 2020 14:50:43 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 14:50:46 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 24 Apr 2020 14:50:48 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 24 Apr 2020 14:50:51 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 24 Apr 2020 14:50:52 GMT
ARG BONITA_VERSION
# Fri, 24 Apr 2020 14:50:53 GMT
ARG BONITA_SHA256
# Fri, 24 Apr 2020 14:51:21 GMT
ARG BASE_URL
# Fri, 24 Apr 2020 14:51:22 GMT
ARG BONITA_URL
# Thu, 11 Jun 2020 20:36:56 GMT
ENV BONITA_VERSION=7.10.5
# Thu, 11 Jun 2020 20:36:56 GMT
ENV BONITA_SHA256=bc2bb1048df1b9d8a293635924fd1e7eb2cf0652f65d3fd64c0f1bc22e435dff
# Thu, 11 Jun 2020 20:36:57 GMT
ENV BASE_URL=https://release.ow2.org/bonita
# Thu, 11 Jun 2020 20:36:58 GMT
ENV BONITA_URL=https://release.ow2.org/bonita/BonitaCommunity-7.10.5.zip
# Thu, 11 Jun 2020 20:37:04 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Thu, 11 Jun 2020 20:37:23 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Thu, 11 Jun 2020 20:37:26 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Thu, 11 Jun 2020 20:37:29 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Thu, 11 Jun 2020 20:37:30 GMT
VOLUME [/opt/bonita]
# Thu, 11 Jun 2020 20:37:30 GMT
COPY dir:6d2b12bd97418487ddd1a174f34d85d11b3e6487e01e6d3f80d99fffcff78e82 in /opt/files 
# Thu, 11 Jun 2020 20:37:31 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Thu, 11 Jun 2020 20:37:32 GMT
EXPOSE 8080
# Thu, 11 Jun 2020 20:37:33 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:c2cd007b69f7e5f37c851aa689e0e617fbaa3fe3e470f714337a03e569b7f434`  
		Last Modified: Sun, 05 Apr 2020 20:25:25 GMT  
		Size: 23.7 MB (23720401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c087f8bf83d28baa9c53fc5cfb0dfc79d5062cfad77563076553b04259e822f`  
		Last Modified: Fri, 24 Apr 2020 00:21:16 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474b5c43e9a24e1958763941a17a7cac60b13460a47f2ae9067ec03ceadab33a`  
		Last Modified: Fri, 24 Apr 2020 00:21:15 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7083e6591d76b9a6c13497a6a89bfbae3e7eb2eb31bec366bec3884c8e4517ce`  
		Last Modified: Fri, 24 Apr 2020 00:21:15 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d2210822f61f96d7e745e40df9f543663e11257e30e222922939e493ce84391`  
		Last Modified: Fri, 24 Apr 2020 14:52:17 GMT  
		Size: 92.9 MB (92894148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da78a5d628eeced4dbcd79fa0e31b79eb98b03653ca4aac6cf5ec07f3bd1adbb`  
		Last Modified: Fri, 24 Apr 2020 14:51:54 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d5ac45fda3ff93dd1c8425e8142db093d713781507c31944c2272e36f41d63`  
		Last Modified: Fri, 24 Apr 2020 14:51:52 GMT  
		Size: 1.9 KB (1920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4dc691455a24b37b3a825b3af8453c60a3bd369c126ed132efa3c93ddd45ec`  
		Last Modified: Fri, 24 Apr 2020 14:51:52 GMT  
		Size: 541.8 KB (541813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2cc6e1e78a6bcf2d971f44859eff8bcc9e8211058055858707e8eeb2432180`  
		Last Modified: Thu, 11 Jun 2020 20:37:59 GMT  
		Size: 98.0 MB (97955969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891e38cf7ceded7640d84fd9fb18bbeec8b82e41233400f02d8fcc75de727955`  
		Last Modified: Thu, 11 Jun 2020 20:37:48 GMT  
		Size: 7.6 KB (7622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6e61b89e2cad740721f947939badbbee49b1c89246067b9a02fab942e944262`  
		Last Modified: Thu, 11 Jun 2020 20:37:48 GMT  
		Size: 1.7 KB (1658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; ppc64le

```console
$ docker pull bonita@sha256:7c32385effd35f026f4264c530280cf83a84f6920b3adf64a13cc73edd7c8a4f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.8 MB (223761201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:949920ba72aac0913ccff0e0e4005a0f353df3c00c00d5530acf3c30232c1850`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 23 Apr 2020 20:42:30 GMT
ADD file:726a32203fbcaae787c10740754e38dcb186778893e6d078db3cba0f49ee6b3c in / 
# Thu, 23 Apr 2020 20:42:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 20:42:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 20:42:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 20:42:50 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 11:12:14 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Fri, 24 Apr 2020 11:16:15 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 11:16:28 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 24 Apr 2020 11:16:38 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 24 Apr 2020 11:16:47 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 24 Apr 2020 11:16:50 GMT
ARG BONITA_VERSION
# Fri, 24 Apr 2020 11:16:54 GMT
ARG BONITA_SHA256
# Fri, 24 Apr 2020 11:18:40 GMT
ARG BASE_URL
# Fri, 24 Apr 2020 11:18:43 GMT
ARG BONITA_URL
# Fri, 24 Apr 2020 11:18:47 GMT
ENV BONITA_VERSION=7.10.4
# Fri, 24 Apr 2020 11:18:51 GMT
ENV BONITA_SHA256=dfc3d6d43a6fda7e0e57a60238e63c754d1a948f3c3e36f460f9c7867bf25d6d
# Fri, 24 Apr 2020 11:18:53 GMT
ENV BASE_URL=https://release.ow2.org/bonita
# Fri, 24 Apr 2020 11:18:56 GMT
ENV BONITA_URL=https://release.ow2.org/bonita/BonitaCommunity-7.10.4.zip
# Fri, 24 Apr 2020 11:19:02 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Fri, 24 Apr 2020 11:19:59 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 24 Apr 2020 11:20:10 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 24 Apr 2020 11:20:17 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Fri, 24 Apr 2020 11:20:19 GMT
VOLUME [/opt/bonita]
# Fri, 24 Apr 2020 11:20:21 GMT
COPY dir:6d2b12bd97418487ddd1a174f34d85d11b3e6487e01e6d3f80d99fffcff78e82 in /opt/files 
# Fri, 24 Apr 2020 11:20:23 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Fri, 24 Apr 2020 11:20:25 GMT
EXPOSE 8080
# Fri, 24 Apr 2020 11:20:29 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:beed3bd0a281cacead564771f079ed9ee8b272a2ed0e28f533e188f3d21fee6e`  
		Last Modified: Mon, 06 Apr 2020 15:40:20 GMT  
		Size: 30.4 MB (30400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae14d2411b83450b8afe92058b998540c56ec42f1ddd7581e8e9fe629c442f89`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 35.2 KB (35198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82678240be3a5c783512ff7336f2b10837ae126958bc6bd1b476a8d039c08771`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7307ad4f24078fd763b41ec7c1772f2fd5238fed1bae36c5d42d28ec9adbffb9`  
		Last Modified: Thu, 23 Apr 2020 20:48:44 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d96de0feba41ae36c2f30772848962f761fa86bea2d5b169395a3bc3c7132e49`  
		Last Modified: Fri, 24 Apr 2020 11:21:16 GMT  
		Size: 94.9 MB (94877414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303b05a46843da9faa969b2426e50688c52e4265f8d3a8d36e56295bafc2ef6d`  
		Last Modified: Fri, 24 Apr 2020 11:20:58 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60cb31d4b93a32f72177ac1374e4fa0804d31b6ac40854dd644fbd53a4a6512e`  
		Last Modified: Fri, 24 Apr 2020 11:20:54 GMT  
		Size: 1.9 KB (1920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b95753237ab572b5fc1131a7c1680219f4a1946af444435a1aff47d35e5eef`  
		Last Modified: Fri, 24 Apr 2020 11:20:54 GMT  
		Size: 541.6 KB (541554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8828b620936bffe307201eada6d468ac9b080f513f12937c5bbf4c0f5a79f14`  
		Last Modified: Fri, 24 Apr 2020 11:21:36 GMT  
		Size: 97.9 MB (97894347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00099f3eb606359b7a2365add166dfb5e6d395de29ca02390c32f24c9a0a977e`  
		Last Modified: Fri, 24 Apr 2020 11:21:29 GMT  
		Size: 7.6 KB (7623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d127f5d545caa1e2928e4980c55cf550ad7fec5e131ed9475f0bd698a72ec9c6`  
		Last Modified: Fri, 24 Apr 2020 11:21:29 GMT  
		Size: 1.7 KB (1652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
