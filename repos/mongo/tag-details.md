<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mongo`

-	[`mongo:3`](#mongo3)
-	[`mongo:3.6`](#mongo36)
-	[`mongo:3.6.17`](#mongo3617)
-	[`mongo:3.6.17-windowsservercore`](#mongo3617-windowsservercore)
-	[`mongo:3.6.17-windowsservercore-1809`](#mongo3617-windowsservercore-1809)
-	[`mongo:3.6.17-windowsservercore-ltsc2016`](#mongo3617-windowsservercore-ltsc2016)
-	[`mongo:3.6.17-xenial`](#mongo3617-xenial)
-	[`mongo:3.6-windowsservercore`](#mongo36-windowsservercore)
-	[`mongo:3.6-windowsservercore-1809`](#mongo36-windowsservercore-1809)
-	[`mongo:3.6-windowsservercore-ltsc2016`](#mongo36-windowsservercore-ltsc2016)
-	[`mongo:3.6-xenial`](#mongo36-xenial)
-	[`mongo:3-windowsservercore`](#mongo3-windowsservercore)
-	[`mongo:3-windowsservercore-1809`](#mongo3-windowsservercore-1809)
-	[`mongo:3-windowsservercore-ltsc2016`](#mongo3-windowsservercore-ltsc2016)
-	[`mongo:3-xenial`](#mongo3-xenial)
-	[`mongo:4`](#mongo4)
-	[`mongo:4.0`](#mongo40)
-	[`mongo:4.0.18`](#mongo4018)
-	[`mongo:4.0.18-windowsservercore`](#mongo4018-windowsservercore)
-	[`mongo:4.0.18-windowsservercore-1809`](#mongo4018-windowsservercore-1809)
-	[`mongo:4.0.18-windowsservercore-ltsc2016`](#mongo4018-windowsservercore-ltsc2016)
-	[`mongo:4.0.18-xenial`](#mongo4018-xenial)
-	[`mongo:4.0-windowsservercore`](#mongo40-windowsservercore)
-	[`mongo:4.0-windowsservercore-1809`](#mongo40-windowsservercore-1809)
-	[`mongo:4.0-windowsservercore-ltsc2016`](#mongo40-windowsservercore-ltsc2016)
-	[`mongo:4.0-xenial`](#mongo40-xenial)
-	[`mongo:4.2`](#mongo42)
-	[`mongo:4.2.6`](#mongo426)
-	[`mongo:4.2.6-bionic`](#mongo426-bionic)
-	[`mongo:4.2.6-windowsservercore`](#mongo426-windowsservercore)
-	[`mongo:4.2.6-windowsservercore-1809`](#mongo426-windowsservercore-1809)
-	[`mongo:4.2.6-windowsservercore-ltsc2016`](#mongo426-windowsservercore-ltsc2016)
-	[`mongo:4.2-bionic`](#mongo42-bionic)
-	[`mongo:4.2-windowsservercore`](#mongo42-windowsservercore)
-	[`mongo:4.2-windowsservercore-1809`](#mongo42-windowsservercore-1809)
-	[`mongo:4.2-windowsservercore-ltsc2016`](#mongo42-windowsservercore-ltsc2016)
-	[`mongo:4-bionic`](#mongo4-bionic)
-	[`mongo:4-windowsservercore`](#mongo4-windowsservercore)
-	[`mongo:4-windowsservercore-1809`](#mongo4-windowsservercore-1809)
-	[`mongo:4-windowsservercore-ltsc2016`](#mongo4-windowsservercore-ltsc2016)
-	[`mongo:bionic`](#mongobionic)
-	[`mongo:latest`](#mongolatest)
-	[`mongo:windowsservercore`](#mongowindowsservercore)
-	[`mongo:windowsservercore-1809`](#mongowindowsservercore-1809)
-	[`mongo:windowsservercore-ltsc2016`](#mongowindowsservercore-ltsc2016)

## `mongo:3`

```console
$ docker pull mongo@sha256:5dfee95028afb74cf34341a36f1b5f349bb877e0b824427c8e601a91a89f2fb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.14393.3630; amd64
	-	windows version 10.0.17763.1158; amd64

### `mongo:3` - linux; amd64

```console
$ docker pull mongo@sha256:72605ac8f0e09e7d8e6d69b9d0d3dde9ed5e84cd5deb137e5d3837f38bfcde49
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.7 MB (165705537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf42dda7e6bc6222f7de7237406270b2f52108e259310d7f02325defa09d0622`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 21 Feb 2020 22:22:27 GMT
ADD file:1f70668251e2e58cee0ff0c22ee805f8a269ac6f8934c07f7e89dca6cc1de3aa in / 
# Fri, 21 Feb 2020 22:22:27 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:22:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:22:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:22:30 GMT
CMD ["/bin/bash"]
# Sat, 22 Feb 2020 01:08:16 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Sat, 22 Feb 2020 01:08:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 16:52:33 GMT
ENV GOSU_VERSION=1.12
# Fri, 17 Apr 2020 16:52:33 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 17 Apr 2020 16:53:00 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 17 Apr 2020 16:53:00 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 17 Apr 2020 16:53:01 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Fri, 17 Apr 2020 16:53:02 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 17 Apr 2020 16:53:02 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 17 Apr 2020 16:53:02 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 17 Apr 2020 16:53:02 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 17 Apr 2020 16:53:02 GMT
ENV MONGO_MAJOR=3.6
# Fri, 17 Apr 2020 16:53:02 GMT
ENV MONGO_VERSION=3.6.17
# Fri, 17 Apr 2020 16:53:03 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 17 Apr 2020 16:53:20 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 17 Apr 2020 16:53:21 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 17 Apr 2020 16:53:21 GMT
VOLUME [/data/db /data/configdb]
# Fri, 17 Apr 2020 16:53:21 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 17 Apr 2020 16:53:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2020 16:53:21 GMT
EXPOSE 27017
# Fri, 17 Apr 2020 16:53:22 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:fe703b657a32e0046dce0ad2cb17172cbec8ba302edf370f5f28962bdb6216a9`  
		Last Modified: Thu, 13 Feb 2020 00:25:54 GMT  
		Size: 44.2 MB (44191726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9df1fafd224fae3ba34a68dfc401f75bf6bc0c016fe36c61661ca5c7ad729ee`  
		Last Modified: Fri, 21 Feb 2020 22:23:12 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a645a4b887f9613f80fae43432e46423f196a9952d11bb620bef2add7c4ed4ee`  
		Last Modified: Fri, 21 Feb 2020 22:23:12 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57db7fe0b522b7a6069e769606e5ed0913a64e1e0d0030382a922ccf9449211e`  
		Last Modified: Fri, 21 Feb 2020 22:23:13 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f659f7c5a8a29b7c2592bc12a6afb9babe94617501a765bab59df899dfa98ac`  
		Last Modified: Sat, 22 Feb 2020 01:11:01 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b7ff548bb868b716a6e1ffbc5281d3f298fa1f2d6bac7843ef09901a0ee5c0`  
		Last Modified: Sat, 22 Feb 2020 01:11:02 GMT  
		Size: 2.9 MB (2946077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67a4fc8b9ac596e924ec523f4f913cec4c02bf316c82fab3b22c51e25d54d638`  
		Last Modified: Fri, 17 Apr 2020 16:54:56 GMT  
		Size: 1.3 MB (1305292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2afe62084c30f7e3e50835c0b6462b1f995eb96ec333987aaf1d2ee4db6157`  
		Last Modified: Fri, 17 Apr 2020 16:54:55 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7c01deb0621cbc504ab4cd9a51f5cfd311c99c6283f34c785e34c27bfa9752`  
		Last Modified: Fri, 17 Apr 2020 16:54:54 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e9a4da5d56fae7ffdc2014b07002f0b83c6faf6956e5eff6e52eabd1a62fea`  
		Last Modified: Fri, 17 Apr 2020 16:54:54 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc013520249edbb1f93602cd7c0f85f27646a70eff47a785afaa3112bed02a09`  
		Last Modified: Fri, 17 Apr 2020 16:55:13 GMT  
		Size: 117.3 MB (117252470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73dc6946a91f0e64b73ad829cb40e9f18b747fee8e3919d203e5aa500386c46`  
		Last Modified: Fri, 17 Apr 2020 16:54:54 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3565d572e9e93f03d67971f15464511edfeb4802e68bd02a9175086684e8c74d`  
		Last Modified: Fri, 17 Apr 2020 16:54:54 GMT  
		Size: 4.0 KB (3953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:2ecee2069cc04242d99e0ee6048d70d14ae5ff0543ba298655d2fa6955c0461e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155145801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44f9d7fc261f5187d7b975386607362ed5ad38bbdf26a0a7ded700cf8a9094b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 24 Apr 2020 00:20:42 GMT
ADD file:24038b6c5a9bab991785fab56202fc43de85e0749e57fcfc361de8aeff302309 in / 
# Fri, 24 Apr 2020 00:20:48 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 00:20:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 00:20:56 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 00:20:58 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 16:16:27 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Apr 2020 16:16:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 16:16:43 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 16:16:43 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Apr 2020 16:17:08 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 16:17:10 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 16:17:10 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Fri, 24 Apr 2020 16:17:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 16:17:13 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Apr 2020 16:17:14 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 16:17:14 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 16:17:15 GMT
ENV MONGO_MAJOR=3.6
# Fri, 24 Apr 2020 16:17:15 GMT
ENV MONGO_VERSION=3.6.17
# Fri, 24 Apr 2020 16:17:17 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Apr 2020 16:17:41 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Apr 2020 16:17:43 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Apr 2020 16:17:44 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Apr 2020 16:17:45 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Apr 2020 16:17:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 16:17:46 GMT
EXPOSE 27017
# Fri, 24 Apr 2020 16:17:47 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:ca96533948cdaf1fc84922a44248fcf915a3f526b46555bb96090bed658b00d7`  
		Last Modified: Mon, 30 Mar 2020 15:49:17 GMT  
		Size: 40.0 MB (39968791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c72780e1c95403020a1883a1054d9d48b7a5ad2d940ba2d57ae211369a19685`  
		Last Modified: Fri, 24 Apr 2020 00:22:16 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d962f0171bca79269769ac242507e3f65f2dcbb86de35ecaf164d37b8a89c9d`  
		Last Modified: Fri, 24 Apr 2020 00:22:16 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179f057dc5a95fd6368cf61fa48d9e2d85af21b750813b8dd17b7ad44752c342`  
		Last Modified: Fri, 24 Apr 2020 00:22:17 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0a8e99e85782df175a29b1bde536a79db756966637facaf915cc8e16f38691`  
		Last Modified: Fri, 24 Apr 2020 16:20:35 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a46d993ee733e416b83e56bc49a2736148b105b73cc7553c80fc2aaa7df313b1`  
		Last Modified: Fri, 24 Apr 2020 16:20:35 GMT  
		Size: 2.5 MB (2475001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b49e909411104c2ebb353f5cd8c52434864e5d144971b58f81c3780a4cd037`  
		Last Modified: Fri, 24 Apr 2020 16:20:35 GMT  
		Size: 1.2 MB (1232274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd9944fff526a6c05418546fe52dfcdcf7b391b22af046c09426b603f2e7154`  
		Last Modified: Fri, 24 Apr 2020 16:20:35 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b2027de0f6b664ea891ed435841a0d444186df6e88b5b5f2946927698336d6`  
		Last Modified: Fri, 24 Apr 2020 16:20:33 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ab895b5b6b70154da05847062e72d9a1032923b2342443cec884eaf030d888`  
		Last Modified: Fri, 24 Apr 2020 16:20:33 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f4372c45199d48239f882cd33086a7480f6645e6652b886e2558c1b60e68f9b`  
		Last Modified: Fri, 24 Apr 2020 16:21:01 GMT  
		Size: 111.5 MB (111459734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:587f076de92d09903fc17a662bebb324abd1afa13dd10e89f23ff056ae0e3ead`  
		Last Modified: Fri, 24 Apr 2020 16:20:33 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc10f27dd2024e92ff7f713da1de35c2fb0928ebe9405088ee2e73fa12bfa7cb`  
		Last Modified: Fri, 24 Apr 2020 16:20:33 GMT  
		Size: 4.0 KB (3956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3` - windows version 10.0.14393.3630; amd64

```console
$ docker pull mongo@sha256:2ad038b8029f42ac88220c0d3c6797b0809c950a4004236f9673b200be31cbc0
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5821606870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590a4c61c6bc30e3ed45446f0dcbe013069705ae7b56c8d5077bd028a915d099`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Apr 2020 17:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Apr 2020 12:52:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Apr 2020 19:36:32 GMT
ENV MONGO_VERSION=3.6.17
# Wed, 15 Apr 2020 19:36:33 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.17-signed.msi
# Wed, 15 Apr 2020 19:36:33 GMT
ENV MONGO_DOWNLOAD_SHA256=b20b72d5366a7a00cb85245ebedd01b665bbac4f918dd5fac7a7c5eb68477c26
# Wed, 15 Apr 2020 19:49:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Apr 2020 19:49:07 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Apr 2020 19:49:09 GMT
EXPOSE 27017
# Wed, 15 Apr 2020 19:49:10 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d0099407ec8ccaf0472e55152e38b262bdf0b2cf8dfd2e8afcc89d728ba3f5a0`  
		Size: 1.7 GB (1658081673 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5171ed01a0687a59b2bdf59e2df29a8932abe0ee22a4a6ff6368f8a8295a97d1`  
		Last Modified: Wed, 15 Apr 2020 15:29:42 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8e9fa0da56ade24c3e568bf7596673f57639c7ed6cbd088c0ed192fde3668c`  
		Last Modified: Wed, 15 Apr 2020 21:11:32 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e27b8aa174553c5d6b83ed9c1f3829422e0730424c12945debd87be96177d6f`  
		Last Modified: Wed, 15 Apr 2020 21:11:31 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ae114b0c74597963b9945618fdcce5d27a13e90eb02a392f336e769e662910`  
		Last Modified: Wed, 15 Apr 2020 21:11:29 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7bc5318f6c07b8cb2f32c160d64179040f98f5c51bb63b437e2f4488137cb85`  
		Last Modified: Wed, 15 Apr 2020 21:11:50 GMT  
		Size: 93.5 MB (93531367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb123bc7931ecaa846ab9b9466beee498abb2472e7cb91d73ae9258f955afb67`  
		Last Modified: Wed, 15 Apr 2020 21:11:29 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216514753240f2ef45953d11052bf0936dd93b2fe2648f4be49903b9390eb35f`  
		Last Modified: Wed, 15 Apr 2020 21:11:29 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d670e752b94e4007002fde91c4f19432ea9f989c1201d858d92f738dc8dd55e`  
		Last Modified: Wed, 15 Apr 2020 21:11:29 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3` - windows version 10.0.17763.1158; amd64

```console
$ docker pull mongo@sha256:a064905482e8ea379e7f18b4904b8f88f8d4d1d40edeb39c9931ebe4778abd67
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2363529840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b2f3a2adf42a0ef0b335a00a0a01d258f3c67063d0b1c0f57dbfcc502701d7`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Wed, 15 Apr 2020 12:44:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Apr 2020 19:49:17 GMT
ENV MONGO_VERSION=3.6.17
# Wed, 15 Apr 2020 19:49:18 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.17-signed.msi
# Wed, 15 Apr 2020 19:49:19 GMT
ENV MONGO_DOWNLOAD_SHA256=b20b72d5366a7a00cb85245ebedd01b665bbac4f918dd5fac7a7c5eb68477c26
# Wed, 15 Apr 2020 20:02:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Apr 2020 20:02:57 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Apr 2020 20:02:58 GMT
EXPOSE 27017
# Wed, 15 Apr 2020 20:03:00 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:442da5a04696895ce6580924a45188bbec9a9db9f81cb7dcef41fc1d4b119130`  
		Last Modified: Wed, 15 Apr 2020 15:29:13 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a32eaddbbf64e167a8d76b71c66899143004c2fbe5f4766f4426ea84e713d0ca`  
		Last Modified: Wed, 15 Apr 2020 21:12:07 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c57468d4b7999565099de1a9c9f9cdb9161aae34989b35a90f9dc12817974e`  
		Last Modified: Wed, 15 Apr 2020 21:12:07 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6507fbba7468665907ecbbf5780b006ad495da6e41c2af8ee7e0875bdf8f4d0`  
		Last Modified: Wed, 15 Apr 2020 21:12:04 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb6a89713dfdcb39ef8f35065173480d59ee8642e8a88eff0126e4a50c5640e5`  
		Last Modified: Wed, 15 Apr 2020 21:12:23 GMT  
		Size: 92.8 MB (92814634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e151825f282187bab3b65866fc4de82ddf85961391875c26f0ef432d2f98e2`  
		Last Modified: Wed, 15 Apr 2020 21:12:04 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9d8eec224ec973fdbdb527993fca4283fd10cd10658ec4a031ae91a53bba1f`  
		Last Modified: Wed, 15 Apr 2020 21:12:04 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c341b33407da3598f93102cc41ca103e249854a941436bac2f2a741faf0cb578`  
		Last Modified: Wed, 15 Apr 2020 21:12:04 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.6`

```console
$ docker pull mongo@sha256:5dfee95028afb74cf34341a36f1b5f349bb877e0b824427c8e601a91a89f2fb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.14393.3630; amd64
	-	windows version 10.0.17763.1158; amd64

### `mongo:3.6` - linux; amd64

```console
$ docker pull mongo@sha256:72605ac8f0e09e7d8e6d69b9d0d3dde9ed5e84cd5deb137e5d3837f38bfcde49
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.7 MB (165705537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf42dda7e6bc6222f7de7237406270b2f52108e259310d7f02325defa09d0622`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 21 Feb 2020 22:22:27 GMT
ADD file:1f70668251e2e58cee0ff0c22ee805f8a269ac6f8934c07f7e89dca6cc1de3aa in / 
# Fri, 21 Feb 2020 22:22:27 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:22:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:22:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:22:30 GMT
CMD ["/bin/bash"]
# Sat, 22 Feb 2020 01:08:16 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Sat, 22 Feb 2020 01:08:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 16:52:33 GMT
ENV GOSU_VERSION=1.12
# Fri, 17 Apr 2020 16:52:33 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 17 Apr 2020 16:53:00 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 17 Apr 2020 16:53:00 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 17 Apr 2020 16:53:01 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Fri, 17 Apr 2020 16:53:02 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 17 Apr 2020 16:53:02 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 17 Apr 2020 16:53:02 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 17 Apr 2020 16:53:02 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 17 Apr 2020 16:53:02 GMT
ENV MONGO_MAJOR=3.6
# Fri, 17 Apr 2020 16:53:02 GMT
ENV MONGO_VERSION=3.6.17
# Fri, 17 Apr 2020 16:53:03 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 17 Apr 2020 16:53:20 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 17 Apr 2020 16:53:21 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 17 Apr 2020 16:53:21 GMT
VOLUME [/data/db /data/configdb]
# Fri, 17 Apr 2020 16:53:21 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 17 Apr 2020 16:53:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2020 16:53:21 GMT
EXPOSE 27017
# Fri, 17 Apr 2020 16:53:22 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:fe703b657a32e0046dce0ad2cb17172cbec8ba302edf370f5f28962bdb6216a9`  
		Last Modified: Thu, 13 Feb 2020 00:25:54 GMT  
		Size: 44.2 MB (44191726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9df1fafd224fae3ba34a68dfc401f75bf6bc0c016fe36c61661ca5c7ad729ee`  
		Last Modified: Fri, 21 Feb 2020 22:23:12 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a645a4b887f9613f80fae43432e46423f196a9952d11bb620bef2add7c4ed4ee`  
		Last Modified: Fri, 21 Feb 2020 22:23:12 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57db7fe0b522b7a6069e769606e5ed0913a64e1e0d0030382a922ccf9449211e`  
		Last Modified: Fri, 21 Feb 2020 22:23:13 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f659f7c5a8a29b7c2592bc12a6afb9babe94617501a765bab59df899dfa98ac`  
		Last Modified: Sat, 22 Feb 2020 01:11:01 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b7ff548bb868b716a6e1ffbc5281d3f298fa1f2d6bac7843ef09901a0ee5c0`  
		Last Modified: Sat, 22 Feb 2020 01:11:02 GMT  
		Size: 2.9 MB (2946077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67a4fc8b9ac596e924ec523f4f913cec4c02bf316c82fab3b22c51e25d54d638`  
		Last Modified: Fri, 17 Apr 2020 16:54:56 GMT  
		Size: 1.3 MB (1305292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2afe62084c30f7e3e50835c0b6462b1f995eb96ec333987aaf1d2ee4db6157`  
		Last Modified: Fri, 17 Apr 2020 16:54:55 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7c01deb0621cbc504ab4cd9a51f5cfd311c99c6283f34c785e34c27bfa9752`  
		Last Modified: Fri, 17 Apr 2020 16:54:54 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e9a4da5d56fae7ffdc2014b07002f0b83c6faf6956e5eff6e52eabd1a62fea`  
		Last Modified: Fri, 17 Apr 2020 16:54:54 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc013520249edbb1f93602cd7c0f85f27646a70eff47a785afaa3112bed02a09`  
		Last Modified: Fri, 17 Apr 2020 16:55:13 GMT  
		Size: 117.3 MB (117252470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73dc6946a91f0e64b73ad829cb40e9f18b747fee8e3919d203e5aa500386c46`  
		Last Modified: Fri, 17 Apr 2020 16:54:54 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3565d572e9e93f03d67971f15464511edfeb4802e68bd02a9175086684e8c74d`  
		Last Modified: Fri, 17 Apr 2020 16:54:54 GMT  
		Size: 4.0 KB (3953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3.6` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:2ecee2069cc04242d99e0ee6048d70d14ae5ff0543ba298655d2fa6955c0461e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155145801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44f9d7fc261f5187d7b975386607362ed5ad38bbdf26a0a7ded700cf8a9094b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 24 Apr 2020 00:20:42 GMT
ADD file:24038b6c5a9bab991785fab56202fc43de85e0749e57fcfc361de8aeff302309 in / 
# Fri, 24 Apr 2020 00:20:48 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 00:20:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 00:20:56 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 00:20:58 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 16:16:27 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Apr 2020 16:16:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 16:16:43 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 16:16:43 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Apr 2020 16:17:08 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 16:17:10 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 16:17:10 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Fri, 24 Apr 2020 16:17:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 16:17:13 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Apr 2020 16:17:14 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 16:17:14 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 16:17:15 GMT
ENV MONGO_MAJOR=3.6
# Fri, 24 Apr 2020 16:17:15 GMT
ENV MONGO_VERSION=3.6.17
# Fri, 24 Apr 2020 16:17:17 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Apr 2020 16:17:41 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Apr 2020 16:17:43 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Apr 2020 16:17:44 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Apr 2020 16:17:45 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Apr 2020 16:17:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 16:17:46 GMT
EXPOSE 27017
# Fri, 24 Apr 2020 16:17:47 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:ca96533948cdaf1fc84922a44248fcf915a3f526b46555bb96090bed658b00d7`  
		Last Modified: Mon, 30 Mar 2020 15:49:17 GMT  
		Size: 40.0 MB (39968791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c72780e1c95403020a1883a1054d9d48b7a5ad2d940ba2d57ae211369a19685`  
		Last Modified: Fri, 24 Apr 2020 00:22:16 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d962f0171bca79269769ac242507e3f65f2dcbb86de35ecaf164d37b8a89c9d`  
		Last Modified: Fri, 24 Apr 2020 00:22:16 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179f057dc5a95fd6368cf61fa48d9e2d85af21b750813b8dd17b7ad44752c342`  
		Last Modified: Fri, 24 Apr 2020 00:22:17 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0a8e99e85782df175a29b1bde536a79db756966637facaf915cc8e16f38691`  
		Last Modified: Fri, 24 Apr 2020 16:20:35 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a46d993ee733e416b83e56bc49a2736148b105b73cc7553c80fc2aaa7df313b1`  
		Last Modified: Fri, 24 Apr 2020 16:20:35 GMT  
		Size: 2.5 MB (2475001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b49e909411104c2ebb353f5cd8c52434864e5d144971b58f81c3780a4cd037`  
		Last Modified: Fri, 24 Apr 2020 16:20:35 GMT  
		Size: 1.2 MB (1232274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd9944fff526a6c05418546fe52dfcdcf7b391b22af046c09426b603f2e7154`  
		Last Modified: Fri, 24 Apr 2020 16:20:35 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b2027de0f6b664ea891ed435841a0d444186df6e88b5b5f2946927698336d6`  
		Last Modified: Fri, 24 Apr 2020 16:20:33 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ab895b5b6b70154da05847062e72d9a1032923b2342443cec884eaf030d888`  
		Last Modified: Fri, 24 Apr 2020 16:20:33 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f4372c45199d48239f882cd33086a7480f6645e6652b886e2558c1b60e68f9b`  
		Last Modified: Fri, 24 Apr 2020 16:21:01 GMT  
		Size: 111.5 MB (111459734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:587f076de92d09903fc17a662bebb324abd1afa13dd10e89f23ff056ae0e3ead`  
		Last Modified: Fri, 24 Apr 2020 16:20:33 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc10f27dd2024e92ff7f713da1de35c2fb0928ebe9405088ee2e73fa12bfa7cb`  
		Last Modified: Fri, 24 Apr 2020 16:20:33 GMT  
		Size: 4.0 KB (3956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3.6` - windows version 10.0.14393.3630; amd64

```console
$ docker pull mongo@sha256:2ad038b8029f42ac88220c0d3c6797b0809c950a4004236f9673b200be31cbc0
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5821606870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590a4c61c6bc30e3ed45446f0dcbe013069705ae7b56c8d5077bd028a915d099`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Apr 2020 17:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Apr 2020 12:52:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Apr 2020 19:36:32 GMT
ENV MONGO_VERSION=3.6.17
# Wed, 15 Apr 2020 19:36:33 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.17-signed.msi
# Wed, 15 Apr 2020 19:36:33 GMT
ENV MONGO_DOWNLOAD_SHA256=b20b72d5366a7a00cb85245ebedd01b665bbac4f918dd5fac7a7c5eb68477c26
# Wed, 15 Apr 2020 19:49:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Apr 2020 19:49:07 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Apr 2020 19:49:09 GMT
EXPOSE 27017
# Wed, 15 Apr 2020 19:49:10 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d0099407ec8ccaf0472e55152e38b262bdf0b2cf8dfd2e8afcc89d728ba3f5a0`  
		Size: 1.7 GB (1658081673 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5171ed01a0687a59b2bdf59e2df29a8932abe0ee22a4a6ff6368f8a8295a97d1`  
		Last Modified: Wed, 15 Apr 2020 15:29:42 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8e9fa0da56ade24c3e568bf7596673f57639c7ed6cbd088c0ed192fde3668c`  
		Last Modified: Wed, 15 Apr 2020 21:11:32 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e27b8aa174553c5d6b83ed9c1f3829422e0730424c12945debd87be96177d6f`  
		Last Modified: Wed, 15 Apr 2020 21:11:31 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ae114b0c74597963b9945618fdcce5d27a13e90eb02a392f336e769e662910`  
		Last Modified: Wed, 15 Apr 2020 21:11:29 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7bc5318f6c07b8cb2f32c160d64179040f98f5c51bb63b437e2f4488137cb85`  
		Last Modified: Wed, 15 Apr 2020 21:11:50 GMT  
		Size: 93.5 MB (93531367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb123bc7931ecaa846ab9b9466beee498abb2472e7cb91d73ae9258f955afb67`  
		Last Modified: Wed, 15 Apr 2020 21:11:29 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216514753240f2ef45953d11052bf0936dd93b2fe2648f4be49903b9390eb35f`  
		Last Modified: Wed, 15 Apr 2020 21:11:29 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d670e752b94e4007002fde91c4f19432ea9f989c1201d858d92f738dc8dd55e`  
		Last Modified: Wed, 15 Apr 2020 21:11:29 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3.6` - windows version 10.0.17763.1158; amd64

```console
$ docker pull mongo@sha256:a064905482e8ea379e7f18b4904b8f88f8d4d1d40edeb39c9931ebe4778abd67
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2363529840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b2f3a2adf42a0ef0b335a00a0a01d258f3c67063d0b1c0f57dbfcc502701d7`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Wed, 15 Apr 2020 12:44:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Apr 2020 19:49:17 GMT
ENV MONGO_VERSION=3.6.17
# Wed, 15 Apr 2020 19:49:18 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.17-signed.msi
# Wed, 15 Apr 2020 19:49:19 GMT
ENV MONGO_DOWNLOAD_SHA256=b20b72d5366a7a00cb85245ebedd01b665bbac4f918dd5fac7a7c5eb68477c26
# Wed, 15 Apr 2020 20:02:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Apr 2020 20:02:57 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Apr 2020 20:02:58 GMT
EXPOSE 27017
# Wed, 15 Apr 2020 20:03:00 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:442da5a04696895ce6580924a45188bbec9a9db9f81cb7dcef41fc1d4b119130`  
		Last Modified: Wed, 15 Apr 2020 15:29:13 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a32eaddbbf64e167a8d76b71c66899143004c2fbe5f4766f4426ea84e713d0ca`  
		Last Modified: Wed, 15 Apr 2020 21:12:07 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c57468d4b7999565099de1a9c9f9cdb9161aae34989b35a90f9dc12817974e`  
		Last Modified: Wed, 15 Apr 2020 21:12:07 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6507fbba7468665907ecbbf5780b006ad495da6e41c2af8ee7e0875bdf8f4d0`  
		Last Modified: Wed, 15 Apr 2020 21:12:04 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb6a89713dfdcb39ef8f35065173480d59ee8642e8a88eff0126e4a50c5640e5`  
		Last Modified: Wed, 15 Apr 2020 21:12:23 GMT  
		Size: 92.8 MB (92814634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e151825f282187bab3b65866fc4de82ddf85961391875c26f0ef432d2f98e2`  
		Last Modified: Wed, 15 Apr 2020 21:12:04 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9d8eec224ec973fdbdb527993fca4283fd10cd10658ec4a031ae91a53bba1f`  
		Last Modified: Wed, 15 Apr 2020 21:12:04 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c341b33407da3598f93102cc41ca103e249854a941436bac2f2a741faf0cb578`  
		Last Modified: Wed, 15 Apr 2020 21:12:04 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.6.17`

```console
$ docker pull mongo@sha256:5dfee95028afb74cf34341a36f1b5f349bb877e0b824427c8e601a91a89f2fb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.14393.3630; amd64
	-	windows version 10.0.17763.1158; amd64

### `mongo:3.6.17` - linux; amd64

```console
$ docker pull mongo@sha256:72605ac8f0e09e7d8e6d69b9d0d3dde9ed5e84cd5deb137e5d3837f38bfcde49
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.7 MB (165705537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf42dda7e6bc6222f7de7237406270b2f52108e259310d7f02325defa09d0622`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 21 Feb 2020 22:22:27 GMT
ADD file:1f70668251e2e58cee0ff0c22ee805f8a269ac6f8934c07f7e89dca6cc1de3aa in / 
# Fri, 21 Feb 2020 22:22:27 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:22:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:22:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:22:30 GMT
CMD ["/bin/bash"]
# Sat, 22 Feb 2020 01:08:16 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Sat, 22 Feb 2020 01:08:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 16:52:33 GMT
ENV GOSU_VERSION=1.12
# Fri, 17 Apr 2020 16:52:33 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 17 Apr 2020 16:53:00 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 17 Apr 2020 16:53:00 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 17 Apr 2020 16:53:01 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Fri, 17 Apr 2020 16:53:02 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 17 Apr 2020 16:53:02 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 17 Apr 2020 16:53:02 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 17 Apr 2020 16:53:02 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 17 Apr 2020 16:53:02 GMT
ENV MONGO_MAJOR=3.6
# Fri, 17 Apr 2020 16:53:02 GMT
ENV MONGO_VERSION=3.6.17
# Fri, 17 Apr 2020 16:53:03 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 17 Apr 2020 16:53:20 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 17 Apr 2020 16:53:21 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 17 Apr 2020 16:53:21 GMT
VOLUME [/data/db /data/configdb]
# Fri, 17 Apr 2020 16:53:21 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 17 Apr 2020 16:53:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2020 16:53:21 GMT
EXPOSE 27017
# Fri, 17 Apr 2020 16:53:22 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:fe703b657a32e0046dce0ad2cb17172cbec8ba302edf370f5f28962bdb6216a9`  
		Last Modified: Thu, 13 Feb 2020 00:25:54 GMT  
		Size: 44.2 MB (44191726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9df1fafd224fae3ba34a68dfc401f75bf6bc0c016fe36c61661ca5c7ad729ee`  
		Last Modified: Fri, 21 Feb 2020 22:23:12 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a645a4b887f9613f80fae43432e46423f196a9952d11bb620bef2add7c4ed4ee`  
		Last Modified: Fri, 21 Feb 2020 22:23:12 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57db7fe0b522b7a6069e769606e5ed0913a64e1e0d0030382a922ccf9449211e`  
		Last Modified: Fri, 21 Feb 2020 22:23:13 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f659f7c5a8a29b7c2592bc12a6afb9babe94617501a765bab59df899dfa98ac`  
		Last Modified: Sat, 22 Feb 2020 01:11:01 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b7ff548bb868b716a6e1ffbc5281d3f298fa1f2d6bac7843ef09901a0ee5c0`  
		Last Modified: Sat, 22 Feb 2020 01:11:02 GMT  
		Size: 2.9 MB (2946077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67a4fc8b9ac596e924ec523f4f913cec4c02bf316c82fab3b22c51e25d54d638`  
		Last Modified: Fri, 17 Apr 2020 16:54:56 GMT  
		Size: 1.3 MB (1305292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2afe62084c30f7e3e50835c0b6462b1f995eb96ec333987aaf1d2ee4db6157`  
		Last Modified: Fri, 17 Apr 2020 16:54:55 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7c01deb0621cbc504ab4cd9a51f5cfd311c99c6283f34c785e34c27bfa9752`  
		Last Modified: Fri, 17 Apr 2020 16:54:54 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e9a4da5d56fae7ffdc2014b07002f0b83c6faf6956e5eff6e52eabd1a62fea`  
		Last Modified: Fri, 17 Apr 2020 16:54:54 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc013520249edbb1f93602cd7c0f85f27646a70eff47a785afaa3112bed02a09`  
		Last Modified: Fri, 17 Apr 2020 16:55:13 GMT  
		Size: 117.3 MB (117252470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73dc6946a91f0e64b73ad829cb40e9f18b747fee8e3919d203e5aa500386c46`  
		Last Modified: Fri, 17 Apr 2020 16:54:54 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3565d572e9e93f03d67971f15464511edfeb4802e68bd02a9175086684e8c74d`  
		Last Modified: Fri, 17 Apr 2020 16:54:54 GMT  
		Size: 4.0 KB (3953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3.6.17` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:2ecee2069cc04242d99e0ee6048d70d14ae5ff0543ba298655d2fa6955c0461e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155145801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44f9d7fc261f5187d7b975386607362ed5ad38bbdf26a0a7ded700cf8a9094b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 24 Apr 2020 00:20:42 GMT
ADD file:24038b6c5a9bab991785fab56202fc43de85e0749e57fcfc361de8aeff302309 in / 
# Fri, 24 Apr 2020 00:20:48 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 00:20:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 00:20:56 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 00:20:58 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 16:16:27 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Apr 2020 16:16:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 16:16:43 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 16:16:43 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Apr 2020 16:17:08 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 16:17:10 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 16:17:10 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Fri, 24 Apr 2020 16:17:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 16:17:13 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Apr 2020 16:17:14 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 16:17:14 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 16:17:15 GMT
ENV MONGO_MAJOR=3.6
# Fri, 24 Apr 2020 16:17:15 GMT
ENV MONGO_VERSION=3.6.17
# Fri, 24 Apr 2020 16:17:17 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Apr 2020 16:17:41 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Apr 2020 16:17:43 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Apr 2020 16:17:44 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Apr 2020 16:17:45 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Apr 2020 16:17:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 16:17:46 GMT
EXPOSE 27017
# Fri, 24 Apr 2020 16:17:47 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:ca96533948cdaf1fc84922a44248fcf915a3f526b46555bb96090bed658b00d7`  
		Last Modified: Mon, 30 Mar 2020 15:49:17 GMT  
		Size: 40.0 MB (39968791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c72780e1c95403020a1883a1054d9d48b7a5ad2d940ba2d57ae211369a19685`  
		Last Modified: Fri, 24 Apr 2020 00:22:16 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d962f0171bca79269769ac242507e3f65f2dcbb86de35ecaf164d37b8a89c9d`  
		Last Modified: Fri, 24 Apr 2020 00:22:16 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179f057dc5a95fd6368cf61fa48d9e2d85af21b750813b8dd17b7ad44752c342`  
		Last Modified: Fri, 24 Apr 2020 00:22:17 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0a8e99e85782df175a29b1bde536a79db756966637facaf915cc8e16f38691`  
		Last Modified: Fri, 24 Apr 2020 16:20:35 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a46d993ee733e416b83e56bc49a2736148b105b73cc7553c80fc2aaa7df313b1`  
		Last Modified: Fri, 24 Apr 2020 16:20:35 GMT  
		Size: 2.5 MB (2475001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b49e909411104c2ebb353f5cd8c52434864e5d144971b58f81c3780a4cd037`  
		Last Modified: Fri, 24 Apr 2020 16:20:35 GMT  
		Size: 1.2 MB (1232274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd9944fff526a6c05418546fe52dfcdcf7b391b22af046c09426b603f2e7154`  
		Last Modified: Fri, 24 Apr 2020 16:20:35 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b2027de0f6b664ea891ed435841a0d444186df6e88b5b5f2946927698336d6`  
		Last Modified: Fri, 24 Apr 2020 16:20:33 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ab895b5b6b70154da05847062e72d9a1032923b2342443cec884eaf030d888`  
		Last Modified: Fri, 24 Apr 2020 16:20:33 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f4372c45199d48239f882cd33086a7480f6645e6652b886e2558c1b60e68f9b`  
		Last Modified: Fri, 24 Apr 2020 16:21:01 GMT  
		Size: 111.5 MB (111459734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:587f076de92d09903fc17a662bebb324abd1afa13dd10e89f23ff056ae0e3ead`  
		Last Modified: Fri, 24 Apr 2020 16:20:33 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc10f27dd2024e92ff7f713da1de35c2fb0928ebe9405088ee2e73fa12bfa7cb`  
		Last Modified: Fri, 24 Apr 2020 16:20:33 GMT  
		Size: 4.0 KB (3956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3.6.17` - windows version 10.0.14393.3630; amd64

```console
$ docker pull mongo@sha256:2ad038b8029f42ac88220c0d3c6797b0809c950a4004236f9673b200be31cbc0
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5821606870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590a4c61c6bc30e3ed45446f0dcbe013069705ae7b56c8d5077bd028a915d099`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Apr 2020 17:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Apr 2020 12:52:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Apr 2020 19:36:32 GMT
ENV MONGO_VERSION=3.6.17
# Wed, 15 Apr 2020 19:36:33 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.17-signed.msi
# Wed, 15 Apr 2020 19:36:33 GMT
ENV MONGO_DOWNLOAD_SHA256=b20b72d5366a7a00cb85245ebedd01b665bbac4f918dd5fac7a7c5eb68477c26
# Wed, 15 Apr 2020 19:49:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Apr 2020 19:49:07 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Apr 2020 19:49:09 GMT
EXPOSE 27017
# Wed, 15 Apr 2020 19:49:10 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d0099407ec8ccaf0472e55152e38b262bdf0b2cf8dfd2e8afcc89d728ba3f5a0`  
		Size: 1.7 GB (1658081673 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5171ed01a0687a59b2bdf59e2df29a8932abe0ee22a4a6ff6368f8a8295a97d1`  
		Last Modified: Wed, 15 Apr 2020 15:29:42 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8e9fa0da56ade24c3e568bf7596673f57639c7ed6cbd088c0ed192fde3668c`  
		Last Modified: Wed, 15 Apr 2020 21:11:32 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e27b8aa174553c5d6b83ed9c1f3829422e0730424c12945debd87be96177d6f`  
		Last Modified: Wed, 15 Apr 2020 21:11:31 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ae114b0c74597963b9945618fdcce5d27a13e90eb02a392f336e769e662910`  
		Last Modified: Wed, 15 Apr 2020 21:11:29 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7bc5318f6c07b8cb2f32c160d64179040f98f5c51bb63b437e2f4488137cb85`  
		Last Modified: Wed, 15 Apr 2020 21:11:50 GMT  
		Size: 93.5 MB (93531367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb123bc7931ecaa846ab9b9466beee498abb2472e7cb91d73ae9258f955afb67`  
		Last Modified: Wed, 15 Apr 2020 21:11:29 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216514753240f2ef45953d11052bf0936dd93b2fe2648f4be49903b9390eb35f`  
		Last Modified: Wed, 15 Apr 2020 21:11:29 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d670e752b94e4007002fde91c4f19432ea9f989c1201d858d92f738dc8dd55e`  
		Last Modified: Wed, 15 Apr 2020 21:11:29 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3.6.17` - windows version 10.0.17763.1158; amd64

```console
$ docker pull mongo@sha256:a064905482e8ea379e7f18b4904b8f88f8d4d1d40edeb39c9931ebe4778abd67
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2363529840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b2f3a2adf42a0ef0b335a00a0a01d258f3c67063d0b1c0f57dbfcc502701d7`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Wed, 15 Apr 2020 12:44:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Apr 2020 19:49:17 GMT
ENV MONGO_VERSION=3.6.17
# Wed, 15 Apr 2020 19:49:18 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.17-signed.msi
# Wed, 15 Apr 2020 19:49:19 GMT
ENV MONGO_DOWNLOAD_SHA256=b20b72d5366a7a00cb85245ebedd01b665bbac4f918dd5fac7a7c5eb68477c26
# Wed, 15 Apr 2020 20:02:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Apr 2020 20:02:57 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Apr 2020 20:02:58 GMT
EXPOSE 27017
# Wed, 15 Apr 2020 20:03:00 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:442da5a04696895ce6580924a45188bbec9a9db9f81cb7dcef41fc1d4b119130`  
		Last Modified: Wed, 15 Apr 2020 15:29:13 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a32eaddbbf64e167a8d76b71c66899143004c2fbe5f4766f4426ea84e713d0ca`  
		Last Modified: Wed, 15 Apr 2020 21:12:07 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c57468d4b7999565099de1a9c9f9cdb9161aae34989b35a90f9dc12817974e`  
		Last Modified: Wed, 15 Apr 2020 21:12:07 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6507fbba7468665907ecbbf5780b006ad495da6e41c2af8ee7e0875bdf8f4d0`  
		Last Modified: Wed, 15 Apr 2020 21:12:04 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb6a89713dfdcb39ef8f35065173480d59ee8642e8a88eff0126e4a50c5640e5`  
		Last Modified: Wed, 15 Apr 2020 21:12:23 GMT  
		Size: 92.8 MB (92814634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e151825f282187bab3b65866fc4de82ddf85961391875c26f0ef432d2f98e2`  
		Last Modified: Wed, 15 Apr 2020 21:12:04 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9d8eec224ec973fdbdb527993fca4283fd10cd10658ec4a031ae91a53bba1f`  
		Last Modified: Wed, 15 Apr 2020 21:12:04 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c341b33407da3598f93102cc41ca103e249854a941436bac2f2a741faf0cb578`  
		Last Modified: Wed, 15 Apr 2020 21:12:04 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.6.17-windowsservercore`

```console
$ docker pull mongo@sha256:cc192d5019217acb5b5d9782f46a0341abe17c7d8bfa58df28b16e95cf8ff4f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3630; amd64
	-	windows version 10.0.17763.1158; amd64

### `mongo:3.6.17-windowsservercore` - windows version 10.0.14393.3630; amd64

```console
$ docker pull mongo@sha256:2ad038b8029f42ac88220c0d3c6797b0809c950a4004236f9673b200be31cbc0
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5821606870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590a4c61c6bc30e3ed45446f0dcbe013069705ae7b56c8d5077bd028a915d099`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Apr 2020 17:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Apr 2020 12:52:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Apr 2020 19:36:32 GMT
ENV MONGO_VERSION=3.6.17
# Wed, 15 Apr 2020 19:36:33 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.17-signed.msi
# Wed, 15 Apr 2020 19:36:33 GMT
ENV MONGO_DOWNLOAD_SHA256=b20b72d5366a7a00cb85245ebedd01b665bbac4f918dd5fac7a7c5eb68477c26
# Wed, 15 Apr 2020 19:49:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Apr 2020 19:49:07 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Apr 2020 19:49:09 GMT
EXPOSE 27017
# Wed, 15 Apr 2020 19:49:10 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d0099407ec8ccaf0472e55152e38b262bdf0b2cf8dfd2e8afcc89d728ba3f5a0`  
		Size: 1.7 GB (1658081673 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5171ed01a0687a59b2bdf59e2df29a8932abe0ee22a4a6ff6368f8a8295a97d1`  
		Last Modified: Wed, 15 Apr 2020 15:29:42 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8e9fa0da56ade24c3e568bf7596673f57639c7ed6cbd088c0ed192fde3668c`  
		Last Modified: Wed, 15 Apr 2020 21:11:32 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e27b8aa174553c5d6b83ed9c1f3829422e0730424c12945debd87be96177d6f`  
		Last Modified: Wed, 15 Apr 2020 21:11:31 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ae114b0c74597963b9945618fdcce5d27a13e90eb02a392f336e769e662910`  
		Last Modified: Wed, 15 Apr 2020 21:11:29 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7bc5318f6c07b8cb2f32c160d64179040f98f5c51bb63b437e2f4488137cb85`  
		Last Modified: Wed, 15 Apr 2020 21:11:50 GMT  
		Size: 93.5 MB (93531367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb123bc7931ecaa846ab9b9466beee498abb2472e7cb91d73ae9258f955afb67`  
		Last Modified: Wed, 15 Apr 2020 21:11:29 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216514753240f2ef45953d11052bf0936dd93b2fe2648f4be49903b9390eb35f`  
		Last Modified: Wed, 15 Apr 2020 21:11:29 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d670e752b94e4007002fde91c4f19432ea9f989c1201d858d92f738dc8dd55e`  
		Last Modified: Wed, 15 Apr 2020 21:11:29 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3.6.17-windowsservercore` - windows version 10.0.17763.1158; amd64

```console
$ docker pull mongo@sha256:a064905482e8ea379e7f18b4904b8f88f8d4d1d40edeb39c9931ebe4778abd67
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2363529840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b2f3a2adf42a0ef0b335a00a0a01d258f3c67063d0b1c0f57dbfcc502701d7`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Wed, 15 Apr 2020 12:44:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Apr 2020 19:49:17 GMT
ENV MONGO_VERSION=3.6.17
# Wed, 15 Apr 2020 19:49:18 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.17-signed.msi
# Wed, 15 Apr 2020 19:49:19 GMT
ENV MONGO_DOWNLOAD_SHA256=b20b72d5366a7a00cb85245ebedd01b665bbac4f918dd5fac7a7c5eb68477c26
# Wed, 15 Apr 2020 20:02:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Apr 2020 20:02:57 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Apr 2020 20:02:58 GMT
EXPOSE 27017
# Wed, 15 Apr 2020 20:03:00 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:442da5a04696895ce6580924a45188bbec9a9db9f81cb7dcef41fc1d4b119130`  
		Last Modified: Wed, 15 Apr 2020 15:29:13 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a32eaddbbf64e167a8d76b71c66899143004c2fbe5f4766f4426ea84e713d0ca`  
		Last Modified: Wed, 15 Apr 2020 21:12:07 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c57468d4b7999565099de1a9c9f9cdb9161aae34989b35a90f9dc12817974e`  
		Last Modified: Wed, 15 Apr 2020 21:12:07 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6507fbba7468665907ecbbf5780b006ad495da6e41c2af8ee7e0875bdf8f4d0`  
		Last Modified: Wed, 15 Apr 2020 21:12:04 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb6a89713dfdcb39ef8f35065173480d59ee8642e8a88eff0126e4a50c5640e5`  
		Last Modified: Wed, 15 Apr 2020 21:12:23 GMT  
		Size: 92.8 MB (92814634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e151825f282187bab3b65866fc4de82ddf85961391875c26f0ef432d2f98e2`  
		Last Modified: Wed, 15 Apr 2020 21:12:04 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9d8eec224ec973fdbdb527993fca4283fd10cd10658ec4a031ae91a53bba1f`  
		Last Modified: Wed, 15 Apr 2020 21:12:04 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c341b33407da3598f93102cc41ca103e249854a941436bac2f2a741faf0cb578`  
		Last Modified: Wed, 15 Apr 2020 21:12:04 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.6.17-windowsservercore-1809`

```console
$ docker pull mongo@sha256:6a86515bb0970d7b80e2ab33ee2cb21e5f63a231d47a0eaf708dfe13b491127b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1158; amd64

### `mongo:3.6.17-windowsservercore-1809` - windows version 10.0.17763.1158; amd64

```console
$ docker pull mongo@sha256:a064905482e8ea379e7f18b4904b8f88f8d4d1d40edeb39c9931ebe4778abd67
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2363529840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b2f3a2adf42a0ef0b335a00a0a01d258f3c67063d0b1c0f57dbfcc502701d7`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Wed, 15 Apr 2020 12:44:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Apr 2020 19:49:17 GMT
ENV MONGO_VERSION=3.6.17
# Wed, 15 Apr 2020 19:49:18 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.17-signed.msi
# Wed, 15 Apr 2020 19:49:19 GMT
ENV MONGO_DOWNLOAD_SHA256=b20b72d5366a7a00cb85245ebedd01b665bbac4f918dd5fac7a7c5eb68477c26
# Wed, 15 Apr 2020 20:02:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Apr 2020 20:02:57 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Apr 2020 20:02:58 GMT
EXPOSE 27017
# Wed, 15 Apr 2020 20:03:00 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:442da5a04696895ce6580924a45188bbec9a9db9f81cb7dcef41fc1d4b119130`  
		Last Modified: Wed, 15 Apr 2020 15:29:13 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a32eaddbbf64e167a8d76b71c66899143004c2fbe5f4766f4426ea84e713d0ca`  
		Last Modified: Wed, 15 Apr 2020 21:12:07 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c57468d4b7999565099de1a9c9f9cdb9161aae34989b35a90f9dc12817974e`  
		Last Modified: Wed, 15 Apr 2020 21:12:07 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6507fbba7468665907ecbbf5780b006ad495da6e41c2af8ee7e0875bdf8f4d0`  
		Last Modified: Wed, 15 Apr 2020 21:12:04 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb6a89713dfdcb39ef8f35065173480d59ee8642e8a88eff0126e4a50c5640e5`  
		Last Modified: Wed, 15 Apr 2020 21:12:23 GMT  
		Size: 92.8 MB (92814634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e151825f282187bab3b65866fc4de82ddf85961391875c26f0ef432d2f98e2`  
		Last Modified: Wed, 15 Apr 2020 21:12:04 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9d8eec224ec973fdbdb527993fca4283fd10cd10658ec4a031ae91a53bba1f`  
		Last Modified: Wed, 15 Apr 2020 21:12:04 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c341b33407da3598f93102cc41ca103e249854a941436bac2f2a741faf0cb578`  
		Last Modified: Wed, 15 Apr 2020 21:12:04 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.6.17-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:cf14c686fbf2088bfd778e806b278dc4a24aac8ad56f6156ff609677a7c883a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3630; amd64

### `mongo:3.6.17-windowsservercore-ltsc2016` - windows version 10.0.14393.3630; amd64

```console
$ docker pull mongo@sha256:2ad038b8029f42ac88220c0d3c6797b0809c950a4004236f9673b200be31cbc0
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5821606870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590a4c61c6bc30e3ed45446f0dcbe013069705ae7b56c8d5077bd028a915d099`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Apr 2020 17:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Apr 2020 12:52:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Apr 2020 19:36:32 GMT
ENV MONGO_VERSION=3.6.17
# Wed, 15 Apr 2020 19:36:33 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.17-signed.msi
# Wed, 15 Apr 2020 19:36:33 GMT
ENV MONGO_DOWNLOAD_SHA256=b20b72d5366a7a00cb85245ebedd01b665bbac4f918dd5fac7a7c5eb68477c26
# Wed, 15 Apr 2020 19:49:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Apr 2020 19:49:07 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Apr 2020 19:49:09 GMT
EXPOSE 27017
# Wed, 15 Apr 2020 19:49:10 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d0099407ec8ccaf0472e55152e38b262bdf0b2cf8dfd2e8afcc89d728ba3f5a0`  
		Size: 1.7 GB (1658081673 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5171ed01a0687a59b2bdf59e2df29a8932abe0ee22a4a6ff6368f8a8295a97d1`  
		Last Modified: Wed, 15 Apr 2020 15:29:42 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8e9fa0da56ade24c3e568bf7596673f57639c7ed6cbd088c0ed192fde3668c`  
		Last Modified: Wed, 15 Apr 2020 21:11:32 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e27b8aa174553c5d6b83ed9c1f3829422e0730424c12945debd87be96177d6f`  
		Last Modified: Wed, 15 Apr 2020 21:11:31 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ae114b0c74597963b9945618fdcce5d27a13e90eb02a392f336e769e662910`  
		Last Modified: Wed, 15 Apr 2020 21:11:29 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7bc5318f6c07b8cb2f32c160d64179040f98f5c51bb63b437e2f4488137cb85`  
		Last Modified: Wed, 15 Apr 2020 21:11:50 GMT  
		Size: 93.5 MB (93531367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb123bc7931ecaa846ab9b9466beee498abb2472e7cb91d73ae9258f955afb67`  
		Last Modified: Wed, 15 Apr 2020 21:11:29 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216514753240f2ef45953d11052bf0936dd93b2fe2648f4be49903b9390eb35f`  
		Last Modified: Wed, 15 Apr 2020 21:11:29 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d670e752b94e4007002fde91c4f19432ea9f989c1201d858d92f738dc8dd55e`  
		Last Modified: Wed, 15 Apr 2020 21:11:29 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.6.17-xenial`

```console
$ docker pull mongo@sha256:1cbbf25222ab3274a388c779615cb9fe77273b0b6f57c34d61f23eb57a37b80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:3.6.17-xenial` - linux; amd64

```console
$ docker pull mongo@sha256:72605ac8f0e09e7d8e6d69b9d0d3dde9ed5e84cd5deb137e5d3837f38bfcde49
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.7 MB (165705537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf42dda7e6bc6222f7de7237406270b2f52108e259310d7f02325defa09d0622`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 21 Feb 2020 22:22:27 GMT
ADD file:1f70668251e2e58cee0ff0c22ee805f8a269ac6f8934c07f7e89dca6cc1de3aa in / 
# Fri, 21 Feb 2020 22:22:27 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:22:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:22:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:22:30 GMT
CMD ["/bin/bash"]
# Sat, 22 Feb 2020 01:08:16 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Sat, 22 Feb 2020 01:08:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 16:52:33 GMT
ENV GOSU_VERSION=1.12
# Fri, 17 Apr 2020 16:52:33 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 17 Apr 2020 16:53:00 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 17 Apr 2020 16:53:00 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 17 Apr 2020 16:53:01 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Fri, 17 Apr 2020 16:53:02 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 17 Apr 2020 16:53:02 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 17 Apr 2020 16:53:02 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 17 Apr 2020 16:53:02 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 17 Apr 2020 16:53:02 GMT
ENV MONGO_MAJOR=3.6
# Fri, 17 Apr 2020 16:53:02 GMT
ENV MONGO_VERSION=3.6.17
# Fri, 17 Apr 2020 16:53:03 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 17 Apr 2020 16:53:20 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 17 Apr 2020 16:53:21 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 17 Apr 2020 16:53:21 GMT
VOLUME [/data/db /data/configdb]
# Fri, 17 Apr 2020 16:53:21 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 17 Apr 2020 16:53:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2020 16:53:21 GMT
EXPOSE 27017
# Fri, 17 Apr 2020 16:53:22 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:fe703b657a32e0046dce0ad2cb17172cbec8ba302edf370f5f28962bdb6216a9`  
		Last Modified: Thu, 13 Feb 2020 00:25:54 GMT  
		Size: 44.2 MB (44191726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9df1fafd224fae3ba34a68dfc401f75bf6bc0c016fe36c61661ca5c7ad729ee`  
		Last Modified: Fri, 21 Feb 2020 22:23:12 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a645a4b887f9613f80fae43432e46423f196a9952d11bb620bef2add7c4ed4ee`  
		Last Modified: Fri, 21 Feb 2020 22:23:12 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57db7fe0b522b7a6069e769606e5ed0913a64e1e0d0030382a922ccf9449211e`  
		Last Modified: Fri, 21 Feb 2020 22:23:13 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f659f7c5a8a29b7c2592bc12a6afb9babe94617501a765bab59df899dfa98ac`  
		Last Modified: Sat, 22 Feb 2020 01:11:01 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b7ff548bb868b716a6e1ffbc5281d3f298fa1f2d6bac7843ef09901a0ee5c0`  
		Last Modified: Sat, 22 Feb 2020 01:11:02 GMT  
		Size: 2.9 MB (2946077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67a4fc8b9ac596e924ec523f4f913cec4c02bf316c82fab3b22c51e25d54d638`  
		Last Modified: Fri, 17 Apr 2020 16:54:56 GMT  
		Size: 1.3 MB (1305292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2afe62084c30f7e3e50835c0b6462b1f995eb96ec333987aaf1d2ee4db6157`  
		Last Modified: Fri, 17 Apr 2020 16:54:55 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7c01deb0621cbc504ab4cd9a51f5cfd311c99c6283f34c785e34c27bfa9752`  
		Last Modified: Fri, 17 Apr 2020 16:54:54 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e9a4da5d56fae7ffdc2014b07002f0b83c6faf6956e5eff6e52eabd1a62fea`  
		Last Modified: Fri, 17 Apr 2020 16:54:54 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc013520249edbb1f93602cd7c0f85f27646a70eff47a785afaa3112bed02a09`  
		Last Modified: Fri, 17 Apr 2020 16:55:13 GMT  
		Size: 117.3 MB (117252470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73dc6946a91f0e64b73ad829cb40e9f18b747fee8e3919d203e5aa500386c46`  
		Last Modified: Fri, 17 Apr 2020 16:54:54 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3565d572e9e93f03d67971f15464511edfeb4802e68bd02a9175086684e8c74d`  
		Last Modified: Fri, 17 Apr 2020 16:54:54 GMT  
		Size: 4.0 KB (3953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3.6.17-xenial` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:2ecee2069cc04242d99e0ee6048d70d14ae5ff0543ba298655d2fa6955c0461e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155145801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44f9d7fc261f5187d7b975386607362ed5ad38bbdf26a0a7ded700cf8a9094b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 24 Apr 2020 00:20:42 GMT
ADD file:24038b6c5a9bab991785fab56202fc43de85e0749e57fcfc361de8aeff302309 in / 
# Fri, 24 Apr 2020 00:20:48 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 00:20:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 00:20:56 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 00:20:58 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 16:16:27 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Apr 2020 16:16:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 16:16:43 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 16:16:43 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Apr 2020 16:17:08 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 16:17:10 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 16:17:10 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Fri, 24 Apr 2020 16:17:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 16:17:13 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Apr 2020 16:17:14 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 16:17:14 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 16:17:15 GMT
ENV MONGO_MAJOR=3.6
# Fri, 24 Apr 2020 16:17:15 GMT
ENV MONGO_VERSION=3.6.17
# Fri, 24 Apr 2020 16:17:17 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Apr 2020 16:17:41 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Apr 2020 16:17:43 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Apr 2020 16:17:44 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Apr 2020 16:17:45 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Apr 2020 16:17:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 16:17:46 GMT
EXPOSE 27017
# Fri, 24 Apr 2020 16:17:47 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:ca96533948cdaf1fc84922a44248fcf915a3f526b46555bb96090bed658b00d7`  
		Last Modified: Mon, 30 Mar 2020 15:49:17 GMT  
		Size: 40.0 MB (39968791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c72780e1c95403020a1883a1054d9d48b7a5ad2d940ba2d57ae211369a19685`  
		Last Modified: Fri, 24 Apr 2020 00:22:16 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d962f0171bca79269769ac242507e3f65f2dcbb86de35ecaf164d37b8a89c9d`  
		Last Modified: Fri, 24 Apr 2020 00:22:16 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179f057dc5a95fd6368cf61fa48d9e2d85af21b750813b8dd17b7ad44752c342`  
		Last Modified: Fri, 24 Apr 2020 00:22:17 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0a8e99e85782df175a29b1bde536a79db756966637facaf915cc8e16f38691`  
		Last Modified: Fri, 24 Apr 2020 16:20:35 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a46d993ee733e416b83e56bc49a2736148b105b73cc7553c80fc2aaa7df313b1`  
		Last Modified: Fri, 24 Apr 2020 16:20:35 GMT  
		Size: 2.5 MB (2475001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b49e909411104c2ebb353f5cd8c52434864e5d144971b58f81c3780a4cd037`  
		Last Modified: Fri, 24 Apr 2020 16:20:35 GMT  
		Size: 1.2 MB (1232274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd9944fff526a6c05418546fe52dfcdcf7b391b22af046c09426b603f2e7154`  
		Last Modified: Fri, 24 Apr 2020 16:20:35 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b2027de0f6b664ea891ed435841a0d444186df6e88b5b5f2946927698336d6`  
		Last Modified: Fri, 24 Apr 2020 16:20:33 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ab895b5b6b70154da05847062e72d9a1032923b2342443cec884eaf030d888`  
		Last Modified: Fri, 24 Apr 2020 16:20:33 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f4372c45199d48239f882cd33086a7480f6645e6652b886e2558c1b60e68f9b`  
		Last Modified: Fri, 24 Apr 2020 16:21:01 GMT  
		Size: 111.5 MB (111459734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:587f076de92d09903fc17a662bebb324abd1afa13dd10e89f23ff056ae0e3ead`  
		Last Modified: Fri, 24 Apr 2020 16:20:33 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc10f27dd2024e92ff7f713da1de35c2fb0928ebe9405088ee2e73fa12bfa7cb`  
		Last Modified: Fri, 24 Apr 2020 16:20:33 GMT  
		Size: 4.0 KB (3956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.6-windowsservercore`

```console
$ docker pull mongo@sha256:cc192d5019217acb5b5d9782f46a0341abe17c7d8bfa58df28b16e95cf8ff4f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3630; amd64
	-	windows version 10.0.17763.1158; amd64

### `mongo:3.6-windowsservercore` - windows version 10.0.14393.3630; amd64

```console
$ docker pull mongo@sha256:2ad038b8029f42ac88220c0d3c6797b0809c950a4004236f9673b200be31cbc0
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5821606870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590a4c61c6bc30e3ed45446f0dcbe013069705ae7b56c8d5077bd028a915d099`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Apr 2020 17:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Apr 2020 12:52:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Apr 2020 19:36:32 GMT
ENV MONGO_VERSION=3.6.17
# Wed, 15 Apr 2020 19:36:33 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.17-signed.msi
# Wed, 15 Apr 2020 19:36:33 GMT
ENV MONGO_DOWNLOAD_SHA256=b20b72d5366a7a00cb85245ebedd01b665bbac4f918dd5fac7a7c5eb68477c26
# Wed, 15 Apr 2020 19:49:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Apr 2020 19:49:07 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Apr 2020 19:49:09 GMT
EXPOSE 27017
# Wed, 15 Apr 2020 19:49:10 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d0099407ec8ccaf0472e55152e38b262bdf0b2cf8dfd2e8afcc89d728ba3f5a0`  
		Size: 1.7 GB (1658081673 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5171ed01a0687a59b2bdf59e2df29a8932abe0ee22a4a6ff6368f8a8295a97d1`  
		Last Modified: Wed, 15 Apr 2020 15:29:42 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8e9fa0da56ade24c3e568bf7596673f57639c7ed6cbd088c0ed192fde3668c`  
		Last Modified: Wed, 15 Apr 2020 21:11:32 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e27b8aa174553c5d6b83ed9c1f3829422e0730424c12945debd87be96177d6f`  
		Last Modified: Wed, 15 Apr 2020 21:11:31 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ae114b0c74597963b9945618fdcce5d27a13e90eb02a392f336e769e662910`  
		Last Modified: Wed, 15 Apr 2020 21:11:29 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7bc5318f6c07b8cb2f32c160d64179040f98f5c51bb63b437e2f4488137cb85`  
		Last Modified: Wed, 15 Apr 2020 21:11:50 GMT  
		Size: 93.5 MB (93531367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb123bc7931ecaa846ab9b9466beee498abb2472e7cb91d73ae9258f955afb67`  
		Last Modified: Wed, 15 Apr 2020 21:11:29 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216514753240f2ef45953d11052bf0936dd93b2fe2648f4be49903b9390eb35f`  
		Last Modified: Wed, 15 Apr 2020 21:11:29 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d670e752b94e4007002fde91c4f19432ea9f989c1201d858d92f738dc8dd55e`  
		Last Modified: Wed, 15 Apr 2020 21:11:29 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3.6-windowsservercore` - windows version 10.0.17763.1158; amd64

```console
$ docker pull mongo@sha256:a064905482e8ea379e7f18b4904b8f88f8d4d1d40edeb39c9931ebe4778abd67
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2363529840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b2f3a2adf42a0ef0b335a00a0a01d258f3c67063d0b1c0f57dbfcc502701d7`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Wed, 15 Apr 2020 12:44:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Apr 2020 19:49:17 GMT
ENV MONGO_VERSION=3.6.17
# Wed, 15 Apr 2020 19:49:18 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.17-signed.msi
# Wed, 15 Apr 2020 19:49:19 GMT
ENV MONGO_DOWNLOAD_SHA256=b20b72d5366a7a00cb85245ebedd01b665bbac4f918dd5fac7a7c5eb68477c26
# Wed, 15 Apr 2020 20:02:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Apr 2020 20:02:57 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Apr 2020 20:02:58 GMT
EXPOSE 27017
# Wed, 15 Apr 2020 20:03:00 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:442da5a04696895ce6580924a45188bbec9a9db9f81cb7dcef41fc1d4b119130`  
		Last Modified: Wed, 15 Apr 2020 15:29:13 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a32eaddbbf64e167a8d76b71c66899143004c2fbe5f4766f4426ea84e713d0ca`  
		Last Modified: Wed, 15 Apr 2020 21:12:07 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c57468d4b7999565099de1a9c9f9cdb9161aae34989b35a90f9dc12817974e`  
		Last Modified: Wed, 15 Apr 2020 21:12:07 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6507fbba7468665907ecbbf5780b006ad495da6e41c2af8ee7e0875bdf8f4d0`  
		Last Modified: Wed, 15 Apr 2020 21:12:04 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb6a89713dfdcb39ef8f35065173480d59ee8642e8a88eff0126e4a50c5640e5`  
		Last Modified: Wed, 15 Apr 2020 21:12:23 GMT  
		Size: 92.8 MB (92814634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e151825f282187bab3b65866fc4de82ddf85961391875c26f0ef432d2f98e2`  
		Last Modified: Wed, 15 Apr 2020 21:12:04 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9d8eec224ec973fdbdb527993fca4283fd10cd10658ec4a031ae91a53bba1f`  
		Last Modified: Wed, 15 Apr 2020 21:12:04 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c341b33407da3598f93102cc41ca103e249854a941436bac2f2a741faf0cb578`  
		Last Modified: Wed, 15 Apr 2020 21:12:04 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.6-windowsservercore-1809`

```console
$ docker pull mongo@sha256:6a86515bb0970d7b80e2ab33ee2cb21e5f63a231d47a0eaf708dfe13b491127b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1158; amd64

### `mongo:3.6-windowsservercore-1809` - windows version 10.0.17763.1158; amd64

```console
$ docker pull mongo@sha256:a064905482e8ea379e7f18b4904b8f88f8d4d1d40edeb39c9931ebe4778abd67
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2363529840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b2f3a2adf42a0ef0b335a00a0a01d258f3c67063d0b1c0f57dbfcc502701d7`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Wed, 15 Apr 2020 12:44:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Apr 2020 19:49:17 GMT
ENV MONGO_VERSION=3.6.17
# Wed, 15 Apr 2020 19:49:18 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.17-signed.msi
# Wed, 15 Apr 2020 19:49:19 GMT
ENV MONGO_DOWNLOAD_SHA256=b20b72d5366a7a00cb85245ebedd01b665bbac4f918dd5fac7a7c5eb68477c26
# Wed, 15 Apr 2020 20:02:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Apr 2020 20:02:57 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Apr 2020 20:02:58 GMT
EXPOSE 27017
# Wed, 15 Apr 2020 20:03:00 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:442da5a04696895ce6580924a45188bbec9a9db9f81cb7dcef41fc1d4b119130`  
		Last Modified: Wed, 15 Apr 2020 15:29:13 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a32eaddbbf64e167a8d76b71c66899143004c2fbe5f4766f4426ea84e713d0ca`  
		Last Modified: Wed, 15 Apr 2020 21:12:07 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c57468d4b7999565099de1a9c9f9cdb9161aae34989b35a90f9dc12817974e`  
		Last Modified: Wed, 15 Apr 2020 21:12:07 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6507fbba7468665907ecbbf5780b006ad495da6e41c2af8ee7e0875bdf8f4d0`  
		Last Modified: Wed, 15 Apr 2020 21:12:04 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb6a89713dfdcb39ef8f35065173480d59ee8642e8a88eff0126e4a50c5640e5`  
		Last Modified: Wed, 15 Apr 2020 21:12:23 GMT  
		Size: 92.8 MB (92814634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e151825f282187bab3b65866fc4de82ddf85961391875c26f0ef432d2f98e2`  
		Last Modified: Wed, 15 Apr 2020 21:12:04 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9d8eec224ec973fdbdb527993fca4283fd10cd10658ec4a031ae91a53bba1f`  
		Last Modified: Wed, 15 Apr 2020 21:12:04 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c341b33407da3598f93102cc41ca103e249854a941436bac2f2a741faf0cb578`  
		Last Modified: Wed, 15 Apr 2020 21:12:04 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.6-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:cf14c686fbf2088bfd778e806b278dc4a24aac8ad56f6156ff609677a7c883a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3630; amd64

### `mongo:3.6-windowsservercore-ltsc2016` - windows version 10.0.14393.3630; amd64

```console
$ docker pull mongo@sha256:2ad038b8029f42ac88220c0d3c6797b0809c950a4004236f9673b200be31cbc0
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5821606870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590a4c61c6bc30e3ed45446f0dcbe013069705ae7b56c8d5077bd028a915d099`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Apr 2020 17:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Apr 2020 12:52:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Apr 2020 19:36:32 GMT
ENV MONGO_VERSION=3.6.17
# Wed, 15 Apr 2020 19:36:33 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.17-signed.msi
# Wed, 15 Apr 2020 19:36:33 GMT
ENV MONGO_DOWNLOAD_SHA256=b20b72d5366a7a00cb85245ebedd01b665bbac4f918dd5fac7a7c5eb68477c26
# Wed, 15 Apr 2020 19:49:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Apr 2020 19:49:07 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Apr 2020 19:49:09 GMT
EXPOSE 27017
# Wed, 15 Apr 2020 19:49:10 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d0099407ec8ccaf0472e55152e38b262bdf0b2cf8dfd2e8afcc89d728ba3f5a0`  
		Size: 1.7 GB (1658081673 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5171ed01a0687a59b2bdf59e2df29a8932abe0ee22a4a6ff6368f8a8295a97d1`  
		Last Modified: Wed, 15 Apr 2020 15:29:42 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8e9fa0da56ade24c3e568bf7596673f57639c7ed6cbd088c0ed192fde3668c`  
		Last Modified: Wed, 15 Apr 2020 21:11:32 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e27b8aa174553c5d6b83ed9c1f3829422e0730424c12945debd87be96177d6f`  
		Last Modified: Wed, 15 Apr 2020 21:11:31 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ae114b0c74597963b9945618fdcce5d27a13e90eb02a392f336e769e662910`  
		Last Modified: Wed, 15 Apr 2020 21:11:29 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7bc5318f6c07b8cb2f32c160d64179040f98f5c51bb63b437e2f4488137cb85`  
		Last Modified: Wed, 15 Apr 2020 21:11:50 GMT  
		Size: 93.5 MB (93531367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb123bc7931ecaa846ab9b9466beee498abb2472e7cb91d73ae9258f955afb67`  
		Last Modified: Wed, 15 Apr 2020 21:11:29 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216514753240f2ef45953d11052bf0936dd93b2fe2648f4be49903b9390eb35f`  
		Last Modified: Wed, 15 Apr 2020 21:11:29 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d670e752b94e4007002fde91c4f19432ea9f989c1201d858d92f738dc8dd55e`  
		Last Modified: Wed, 15 Apr 2020 21:11:29 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.6-xenial`

```console
$ docker pull mongo@sha256:1cbbf25222ab3274a388c779615cb9fe77273b0b6f57c34d61f23eb57a37b80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:3.6-xenial` - linux; amd64

```console
$ docker pull mongo@sha256:72605ac8f0e09e7d8e6d69b9d0d3dde9ed5e84cd5deb137e5d3837f38bfcde49
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.7 MB (165705537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf42dda7e6bc6222f7de7237406270b2f52108e259310d7f02325defa09d0622`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 21 Feb 2020 22:22:27 GMT
ADD file:1f70668251e2e58cee0ff0c22ee805f8a269ac6f8934c07f7e89dca6cc1de3aa in / 
# Fri, 21 Feb 2020 22:22:27 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:22:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:22:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:22:30 GMT
CMD ["/bin/bash"]
# Sat, 22 Feb 2020 01:08:16 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Sat, 22 Feb 2020 01:08:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 16:52:33 GMT
ENV GOSU_VERSION=1.12
# Fri, 17 Apr 2020 16:52:33 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 17 Apr 2020 16:53:00 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 17 Apr 2020 16:53:00 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 17 Apr 2020 16:53:01 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Fri, 17 Apr 2020 16:53:02 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 17 Apr 2020 16:53:02 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 17 Apr 2020 16:53:02 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 17 Apr 2020 16:53:02 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 17 Apr 2020 16:53:02 GMT
ENV MONGO_MAJOR=3.6
# Fri, 17 Apr 2020 16:53:02 GMT
ENV MONGO_VERSION=3.6.17
# Fri, 17 Apr 2020 16:53:03 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 17 Apr 2020 16:53:20 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 17 Apr 2020 16:53:21 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 17 Apr 2020 16:53:21 GMT
VOLUME [/data/db /data/configdb]
# Fri, 17 Apr 2020 16:53:21 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 17 Apr 2020 16:53:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2020 16:53:21 GMT
EXPOSE 27017
# Fri, 17 Apr 2020 16:53:22 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:fe703b657a32e0046dce0ad2cb17172cbec8ba302edf370f5f28962bdb6216a9`  
		Last Modified: Thu, 13 Feb 2020 00:25:54 GMT  
		Size: 44.2 MB (44191726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9df1fafd224fae3ba34a68dfc401f75bf6bc0c016fe36c61661ca5c7ad729ee`  
		Last Modified: Fri, 21 Feb 2020 22:23:12 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a645a4b887f9613f80fae43432e46423f196a9952d11bb620bef2add7c4ed4ee`  
		Last Modified: Fri, 21 Feb 2020 22:23:12 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57db7fe0b522b7a6069e769606e5ed0913a64e1e0d0030382a922ccf9449211e`  
		Last Modified: Fri, 21 Feb 2020 22:23:13 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f659f7c5a8a29b7c2592bc12a6afb9babe94617501a765bab59df899dfa98ac`  
		Last Modified: Sat, 22 Feb 2020 01:11:01 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b7ff548bb868b716a6e1ffbc5281d3f298fa1f2d6bac7843ef09901a0ee5c0`  
		Last Modified: Sat, 22 Feb 2020 01:11:02 GMT  
		Size: 2.9 MB (2946077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67a4fc8b9ac596e924ec523f4f913cec4c02bf316c82fab3b22c51e25d54d638`  
		Last Modified: Fri, 17 Apr 2020 16:54:56 GMT  
		Size: 1.3 MB (1305292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2afe62084c30f7e3e50835c0b6462b1f995eb96ec333987aaf1d2ee4db6157`  
		Last Modified: Fri, 17 Apr 2020 16:54:55 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7c01deb0621cbc504ab4cd9a51f5cfd311c99c6283f34c785e34c27bfa9752`  
		Last Modified: Fri, 17 Apr 2020 16:54:54 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e9a4da5d56fae7ffdc2014b07002f0b83c6faf6956e5eff6e52eabd1a62fea`  
		Last Modified: Fri, 17 Apr 2020 16:54:54 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc013520249edbb1f93602cd7c0f85f27646a70eff47a785afaa3112bed02a09`  
		Last Modified: Fri, 17 Apr 2020 16:55:13 GMT  
		Size: 117.3 MB (117252470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73dc6946a91f0e64b73ad829cb40e9f18b747fee8e3919d203e5aa500386c46`  
		Last Modified: Fri, 17 Apr 2020 16:54:54 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3565d572e9e93f03d67971f15464511edfeb4802e68bd02a9175086684e8c74d`  
		Last Modified: Fri, 17 Apr 2020 16:54:54 GMT  
		Size: 4.0 KB (3953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3.6-xenial` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:2ecee2069cc04242d99e0ee6048d70d14ae5ff0543ba298655d2fa6955c0461e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155145801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44f9d7fc261f5187d7b975386607362ed5ad38bbdf26a0a7ded700cf8a9094b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 24 Apr 2020 00:20:42 GMT
ADD file:24038b6c5a9bab991785fab56202fc43de85e0749e57fcfc361de8aeff302309 in / 
# Fri, 24 Apr 2020 00:20:48 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 00:20:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 00:20:56 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 00:20:58 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 16:16:27 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Apr 2020 16:16:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 16:16:43 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 16:16:43 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Apr 2020 16:17:08 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 16:17:10 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 16:17:10 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Fri, 24 Apr 2020 16:17:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 16:17:13 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Apr 2020 16:17:14 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 16:17:14 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 16:17:15 GMT
ENV MONGO_MAJOR=3.6
# Fri, 24 Apr 2020 16:17:15 GMT
ENV MONGO_VERSION=3.6.17
# Fri, 24 Apr 2020 16:17:17 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Apr 2020 16:17:41 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Apr 2020 16:17:43 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Apr 2020 16:17:44 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Apr 2020 16:17:45 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Apr 2020 16:17:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 16:17:46 GMT
EXPOSE 27017
# Fri, 24 Apr 2020 16:17:47 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:ca96533948cdaf1fc84922a44248fcf915a3f526b46555bb96090bed658b00d7`  
		Last Modified: Mon, 30 Mar 2020 15:49:17 GMT  
		Size: 40.0 MB (39968791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c72780e1c95403020a1883a1054d9d48b7a5ad2d940ba2d57ae211369a19685`  
		Last Modified: Fri, 24 Apr 2020 00:22:16 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d962f0171bca79269769ac242507e3f65f2dcbb86de35ecaf164d37b8a89c9d`  
		Last Modified: Fri, 24 Apr 2020 00:22:16 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179f057dc5a95fd6368cf61fa48d9e2d85af21b750813b8dd17b7ad44752c342`  
		Last Modified: Fri, 24 Apr 2020 00:22:17 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0a8e99e85782df175a29b1bde536a79db756966637facaf915cc8e16f38691`  
		Last Modified: Fri, 24 Apr 2020 16:20:35 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a46d993ee733e416b83e56bc49a2736148b105b73cc7553c80fc2aaa7df313b1`  
		Last Modified: Fri, 24 Apr 2020 16:20:35 GMT  
		Size: 2.5 MB (2475001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b49e909411104c2ebb353f5cd8c52434864e5d144971b58f81c3780a4cd037`  
		Last Modified: Fri, 24 Apr 2020 16:20:35 GMT  
		Size: 1.2 MB (1232274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd9944fff526a6c05418546fe52dfcdcf7b391b22af046c09426b603f2e7154`  
		Last Modified: Fri, 24 Apr 2020 16:20:35 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b2027de0f6b664ea891ed435841a0d444186df6e88b5b5f2946927698336d6`  
		Last Modified: Fri, 24 Apr 2020 16:20:33 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ab895b5b6b70154da05847062e72d9a1032923b2342443cec884eaf030d888`  
		Last Modified: Fri, 24 Apr 2020 16:20:33 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f4372c45199d48239f882cd33086a7480f6645e6652b886e2558c1b60e68f9b`  
		Last Modified: Fri, 24 Apr 2020 16:21:01 GMT  
		Size: 111.5 MB (111459734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:587f076de92d09903fc17a662bebb324abd1afa13dd10e89f23ff056ae0e3ead`  
		Last Modified: Fri, 24 Apr 2020 16:20:33 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc10f27dd2024e92ff7f713da1de35c2fb0928ebe9405088ee2e73fa12bfa7cb`  
		Last Modified: Fri, 24 Apr 2020 16:20:33 GMT  
		Size: 4.0 KB (3956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3-windowsservercore`

```console
$ docker pull mongo@sha256:cc192d5019217acb5b5d9782f46a0341abe17c7d8bfa58df28b16e95cf8ff4f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3630; amd64
	-	windows version 10.0.17763.1158; amd64

### `mongo:3-windowsservercore` - windows version 10.0.14393.3630; amd64

```console
$ docker pull mongo@sha256:2ad038b8029f42ac88220c0d3c6797b0809c950a4004236f9673b200be31cbc0
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5821606870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590a4c61c6bc30e3ed45446f0dcbe013069705ae7b56c8d5077bd028a915d099`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Apr 2020 17:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Apr 2020 12:52:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Apr 2020 19:36:32 GMT
ENV MONGO_VERSION=3.6.17
# Wed, 15 Apr 2020 19:36:33 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.17-signed.msi
# Wed, 15 Apr 2020 19:36:33 GMT
ENV MONGO_DOWNLOAD_SHA256=b20b72d5366a7a00cb85245ebedd01b665bbac4f918dd5fac7a7c5eb68477c26
# Wed, 15 Apr 2020 19:49:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Apr 2020 19:49:07 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Apr 2020 19:49:09 GMT
EXPOSE 27017
# Wed, 15 Apr 2020 19:49:10 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d0099407ec8ccaf0472e55152e38b262bdf0b2cf8dfd2e8afcc89d728ba3f5a0`  
		Size: 1.7 GB (1658081673 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5171ed01a0687a59b2bdf59e2df29a8932abe0ee22a4a6ff6368f8a8295a97d1`  
		Last Modified: Wed, 15 Apr 2020 15:29:42 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8e9fa0da56ade24c3e568bf7596673f57639c7ed6cbd088c0ed192fde3668c`  
		Last Modified: Wed, 15 Apr 2020 21:11:32 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e27b8aa174553c5d6b83ed9c1f3829422e0730424c12945debd87be96177d6f`  
		Last Modified: Wed, 15 Apr 2020 21:11:31 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ae114b0c74597963b9945618fdcce5d27a13e90eb02a392f336e769e662910`  
		Last Modified: Wed, 15 Apr 2020 21:11:29 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7bc5318f6c07b8cb2f32c160d64179040f98f5c51bb63b437e2f4488137cb85`  
		Last Modified: Wed, 15 Apr 2020 21:11:50 GMT  
		Size: 93.5 MB (93531367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb123bc7931ecaa846ab9b9466beee498abb2472e7cb91d73ae9258f955afb67`  
		Last Modified: Wed, 15 Apr 2020 21:11:29 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216514753240f2ef45953d11052bf0936dd93b2fe2648f4be49903b9390eb35f`  
		Last Modified: Wed, 15 Apr 2020 21:11:29 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d670e752b94e4007002fde91c4f19432ea9f989c1201d858d92f738dc8dd55e`  
		Last Modified: Wed, 15 Apr 2020 21:11:29 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3-windowsservercore` - windows version 10.0.17763.1158; amd64

```console
$ docker pull mongo@sha256:a064905482e8ea379e7f18b4904b8f88f8d4d1d40edeb39c9931ebe4778abd67
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2363529840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b2f3a2adf42a0ef0b335a00a0a01d258f3c67063d0b1c0f57dbfcc502701d7`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Wed, 15 Apr 2020 12:44:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Apr 2020 19:49:17 GMT
ENV MONGO_VERSION=3.6.17
# Wed, 15 Apr 2020 19:49:18 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.17-signed.msi
# Wed, 15 Apr 2020 19:49:19 GMT
ENV MONGO_DOWNLOAD_SHA256=b20b72d5366a7a00cb85245ebedd01b665bbac4f918dd5fac7a7c5eb68477c26
# Wed, 15 Apr 2020 20:02:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Apr 2020 20:02:57 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Apr 2020 20:02:58 GMT
EXPOSE 27017
# Wed, 15 Apr 2020 20:03:00 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:442da5a04696895ce6580924a45188bbec9a9db9f81cb7dcef41fc1d4b119130`  
		Last Modified: Wed, 15 Apr 2020 15:29:13 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a32eaddbbf64e167a8d76b71c66899143004c2fbe5f4766f4426ea84e713d0ca`  
		Last Modified: Wed, 15 Apr 2020 21:12:07 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c57468d4b7999565099de1a9c9f9cdb9161aae34989b35a90f9dc12817974e`  
		Last Modified: Wed, 15 Apr 2020 21:12:07 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6507fbba7468665907ecbbf5780b006ad495da6e41c2af8ee7e0875bdf8f4d0`  
		Last Modified: Wed, 15 Apr 2020 21:12:04 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb6a89713dfdcb39ef8f35065173480d59ee8642e8a88eff0126e4a50c5640e5`  
		Last Modified: Wed, 15 Apr 2020 21:12:23 GMT  
		Size: 92.8 MB (92814634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e151825f282187bab3b65866fc4de82ddf85961391875c26f0ef432d2f98e2`  
		Last Modified: Wed, 15 Apr 2020 21:12:04 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9d8eec224ec973fdbdb527993fca4283fd10cd10658ec4a031ae91a53bba1f`  
		Last Modified: Wed, 15 Apr 2020 21:12:04 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c341b33407da3598f93102cc41ca103e249854a941436bac2f2a741faf0cb578`  
		Last Modified: Wed, 15 Apr 2020 21:12:04 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3-windowsservercore-1809`

```console
$ docker pull mongo@sha256:6a86515bb0970d7b80e2ab33ee2cb21e5f63a231d47a0eaf708dfe13b491127b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1158; amd64

### `mongo:3-windowsservercore-1809` - windows version 10.0.17763.1158; amd64

```console
$ docker pull mongo@sha256:a064905482e8ea379e7f18b4904b8f88f8d4d1d40edeb39c9931ebe4778abd67
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2363529840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b2f3a2adf42a0ef0b335a00a0a01d258f3c67063d0b1c0f57dbfcc502701d7`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Wed, 15 Apr 2020 12:44:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Apr 2020 19:49:17 GMT
ENV MONGO_VERSION=3.6.17
# Wed, 15 Apr 2020 19:49:18 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.17-signed.msi
# Wed, 15 Apr 2020 19:49:19 GMT
ENV MONGO_DOWNLOAD_SHA256=b20b72d5366a7a00cb85245ebedd01b665bbac4f918dd5fac7a7c5eb68477c26
# Wed, 15 Apr 2020 20:02:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Apr 2020 20:02:57 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Apr 2020 20:02:58 GMT
EXPOSE 27017
# Wed, 15 Apr 2020 20:03:00 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:442da5a04696895ce6580924a45188bbec9a9db9f81cb7dcef41fc1d4b119130`  
		Last Modified: Wed, 15 Apr 2020 15:29:13 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a32eaddbbf64e167a8d76b71c66899143004c2fbe5f4766f4426ea84e713d0ca`  
		Last Modified: Wed, 15 Apr 2020 21:12:07 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c57468d4b7999565099de1a9c9f9cdb9161aae34989b35a90f9dc12817974e`  
		Last Modified: Wed, 15 Apr 2020 21:12:07 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6507fbba7468665907ecbbf5780b006ad495da6e41c2af8ee7e0875bdf8f4d0`  
		Last Modified: Wed, 15 Apr 2020 21:12:04 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb6a89713dfdcb39ef8f35065173480d59ee8642e8a88eff0126e4a50c5640e5`  
		Last Modified: Wed, 15 Apr 2020 21:12:23 GMT  
		Size: 92.8 MB (92814634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e151825f282187bab3b65866fc4de82ddf85961391875c26f0ef432d2f98e2`  
		Last Modified: Wed, 15 Apr 2020 21:12:04 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9d8eec224ec973fdbdb527993fca4283fd10cd10658ec4a031ae91a53bba1f`  
		Last Modified: Wed, 15 Apr 2020 21:12:04 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c341b33407da3598f93102cc41ca103e249854a941436bac2f2a741faf0cb578`  
		Last Modified: Wed, 15 Apr 2020 21:12:04 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:cf14c686fbf2088bfd778e806b278dc4a24aac8ad56f6156ff609677a7c883a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3630; amd64

### `mongo:3-windowsservercore-ltsc2016` - windows version 10.0.14393.3630; amd64

```console
$ docker pull mongo@sha256:2ad038b8029f42ac88220c0d3c6797b0809c950a4004236f9673b200be31cbc0
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5821606870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590a4c61c6bc30e3ed45446f0dcbe013069705ae7b56c8d5077bd028a915d099`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Apr 2020 17:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Apr 2020 12:52:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 Apr 2020 19:36:32 GMT
ENV MONGO_VERSION=3.6.17
# Wed, 15 Apr 2020 19:36:33 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.17-signed.msi
# Wed, 15 Apr 2020 19:36:33 GMT
ENV MONGO_DOWNLOAD_SHA256=b20b72d5366a7a00cb85245ebedd01b665bbac4f918dd5fac7a7c5eb68477c26
# Wed, 15 Apr 2020 19:49:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 Apr 2020 19:49:07 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Apr 2020 19:49:09 GMT
EXPOSE 27017
# Wed, 15 Apr 2020 19:49:10 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d0099407ec8ccaf0472e55152e38b262bdf0b2cf8dfd2e8afcc89d728ba3f5a0`  
		Size: 1.7 GB (1658081673 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5171ed01a0687a59b2bdf59e2df29a8932abe0ee22a4a6ff6368f8a8295a97d1`  
		Last Modified: Wed, 15 Apr 2020 15:29:42 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8e9fa0da56ade24c3e568bf7596673f57639c7ed6cbd088c0ed192fde3668c`  
		Last Modified: Wed, 15 Apr 2020 21:11:32 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e27b8aa174553c5d6b83ed9c1f3829422e0730424c12945debd87be96177d6f`  
		Last Modified: Wed, 15 Apr 2020 21:11:31 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ae114b0c74597963b9945618fdcce5d27a13e90eb02a392f336e769e662910`  
		Last Modified: Wed, 15 Apr 2020 21:11:29 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7bc5318f6c07b8cb2f32c160d64179040f98f5c51bb63b437e2f4488137cb85`  
		Last Modified: Wed, 15 Apr 2020 21:11:50 GMT  
		Size: 93.5 MB (93531367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb123bc7931ecaa846ab9b9466beee498abb2472e7cb91d73ae9258f955afb67`  
		Last Modified: Wed, 15 Apr 2020 21:11:29 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216514753240f2ef45953d11052bf0936dd93b2fe2648f4be49903b9390eb35f`  
		Last Modified: Wed, 15 Apr 2020 21:11:29 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d670e752b94e4007002fde91c4f19432ea9f989c1201d858d92f738dc8dd55e`  
		Last Modified: Wed, 15 Apr 2020 21:11:29 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3-xenial`

```console
$ docker pull mongo@sha256:1cbbf25222ab3274a388c779615cb9fe77273b0b6f57c34d61f23eb57a37b80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:3-xenial` - linux; amd64

```console
$ docker pull mongo@sha256:72605ac8f0e09e7d8e6d69b9d0d3dde9ed5e84cd5deb137e5d3837f38bfcde49
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.7 MB (165705537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf42dda7e6bc6222f7de7237406270b2f52108e259310d7f02325defa09d0622`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 21 Feb 2020 22:22:27 GMT
ADD file:1f70668251e2e58cee0ff0c22ee805f8a269ac6f8934c07f7e89dca6cc1de3aa in / 
# Fri, 21 Feb 2020 22:22:27 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:22:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:22:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:22:30 GMT
CMD ["/bin/bash"]
# Sat, 22 Feb 2020 01:08:16 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Sat, 22 Feb 2020 01:08:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 16:52:33 GMT
ENV GOSU_VERSION=1.12
# Fri, 17 Apr 2020 16:52:33 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 17 Apr 2020 16:53:00 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 17 Apr 2020 16:53:00 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 17 Apr 2020 16:53:01 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Fri, 17 Apr 2020 16:53:02 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 17 Apr 2020 16:53:02 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 17 Apr 2020 16:53:02 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 17 Apr 2020 16:53:02 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 17 Apr 2020 16:53:02 GMT
ENV MONGO_MAJOR=3.6
# Fri, 17 Apr 2020 16:53:02 GMT
ENV MONGO_VERSION=3.6.17
# Fri, 17 Apr 2020 16:53:03 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 17 Apr 2020 16:53:20 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 17 Apr 2020 16:53:21 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 17 Apr 2020 16:53:21 GMT
VOLUME [/data/db /data/configdb]
# Fri, 17 Apr 2020 16:53:21 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 17 Apr 2020 16:53:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2020 16:53:21 GMT
EXPOSE 27017
# Fri, 17 Apr 2020 16:53:22 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:fe703b657a32e0046dce0ad2cb17172cbec8ba302edf370f5f28962bdb6216a9`  
		Last Modified: Thu, 13 Feb 2020 00:25:54 GMT  
		Size: 44.2 MB (44191726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9df1fafd224fae3ba34a68dfc401f75bf6bc0c016fe36c61661ca5c7ad729ee`  
		Last Modified: Fri, 21 Feb 2020 22:23:12 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a645a4b887f9613f80fae43432e46423f196a9952d11bb620bef2add7c4ed4ee`  
		Last Modified: Fri, 21 Feb 2020 22:23:12 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57db7fe0b522b7a6069e769606e5ed0913a64e1e0d0030382a922ccf9449211e`  
		Last Modified: Fri, 21 Feb 2020 22:23:13 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f659f7c5a8a29b7c2592bc12a6afb9babe94617501a765bab59df899dfa98ac`  
		Last Modified: Sat, 22 Feb 2020 01:11:01 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b7ff548bb868b716a6e1ffbc5281d3f298fa1f2d6bac7843ef09901a0ee5c0`  
		Last Modified: Sat, 22 Feb 2020 01:11:02 GMT  
		Size: 2.9 MB (2946077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67a4fc8b9ac596e924ec523f4f913cec4c02bf316c82fab3b22c51e25d54d638`  
		Last Modified: Fri, 17 Apr 2020 16:54:56 GMT  
		Size: 1.3 MB (1305292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2afe62084c30f7e3e50835c0b6462b1f995eb96ec333987aaf1d2ee4db6157`  
		Last Modified: Fri, 17 Apr 2020 16:54:55 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7c01deb0621cbc504ab4cd9a51f5cfd311c99c6283f34c785e34c27bfa9752`  
		Last Modified: Fri, 17 Apr 2020 16:54:54 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e9a4da5d56fae7ffdc2014b07002f0b83c6faf6956e5eff6e52eabd1a62fea`  
		Last Modified: Fri, 17 Apr 2020 16:54:54 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc013520249edbb1f93602cd7c0f85f27646a70eff47a785afaa3112bed02a09`  
		Last Modified: Fri, 17 Apr 2020 16:55:13 GMT  
		Size: 117.3 MB (117252470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73dc6946a91f0e64b73ad829cb40e9f18b747fee8e3919d203e5aa500386c46`  
		Last Modified: Fri, 17 Apr 2020 16:54:54 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3565d572e9e93f03d67971f15464511edfeb4802e68bd02a9175086684e8c74d`  
		Last Modified: Fri, 17 Apr 2020 16:54:54 GMT  
		Size: 4.0 KB (3953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3-xenial` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:2ecee2069cc04242d99e0ee6048d70d14ae5ff0543ba298655d2fa6955c0461e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155145801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44f9d7fc261f5187d7b975386607362ed5ad38bbdf26a0a7ded700cf8a9094b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 24 Apr 2020 00:20:42 GMT
ADD file:24038b6c5a9bab991785fab56202fc43de85e0749e57fcfc361de8aeff302309 in / 
# Fri, 24 Apr 2020 00:20:48 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 00:20:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 00:20:56 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 00:20:58 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 16:16:27 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Apr 2020 16:16:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 16:16:43 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 16:16:43 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Apr 2020 16:17:08 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 16:17:10 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 16:17:10 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Fri, 24 Apr 2020 16:17:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 16:17:13 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Apr 2020 16:17:14 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 16:17:14 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 16:17:15 GMT
ENV MONGO_MAJOR=3.6
# Fri, 24 Apr 2020 16:17:15 GMT
ENV MONGO_VERSION=3.6.17
# Fri, 24 Apr 2020 16:17:17 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Apr 2020 16:17:41 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Apr 2020 16:17:43 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Apr 2020 16:17:44 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Apr 2020 16:17:45 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Apr 2020 16:17:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 16:17:46 GMT
EXPOSE 27017
# Fri, 24 Apr 2020 16:17:47 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:ca96533948cdaf1fc84922a44248fcf915a3f526b46555bb96090bed658b00d7`  
		Last Modified: Mon, 30 Mar 2020 15:49:17 GMT  
		Size: 40.0 MB (39968791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c72780e1c95403020a1883a1054d9d48b7a5ad2d940ba2d57ae211369a19685`  
		Last Modified: Fri, 24 Apr 2020 00:22:16 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d962f0171bca79269769ac242507e3f65f2dcbb86de35ecaf164d37b8a89c9d`  
		Last Modified: Fri, 24 Apr 2020 00:22:16 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179f057dc5a95fd6368cf61fa48d9e2d85af21b750813b8dd17b7ad44752c342`  
		Last Modified: Fri, 24 Apr 2020 00:22:17 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0a8e99e85782df175a29b1bde536a79db756966637facaf915cc8e16f38691`  
		Last Modified: Fri, 24 Apr 2020 16:20:35 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a46d993ee733e416b83e56bc49a2736148b105b73cc7553c80fc2aaa7df313b1`  
		Last Modified: Fri, 24 Apr 2020 16:20:35 GMT  
		Size: 2.5 MB (2475001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b49e909411104c2ebb353f5cd8c52434864e5d144971b58f81c3780a4cd037`  
		Last Modified: Fri, 24 Apr 2020 16:20:35 GMT  
		Size: 1.2 MB (1232274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd9944fff526a6c05418546fe52dfcdcf7b391b22af046c09426b603f2e7154`  
		Last Modified: Fri, 24 Apr 2020 16:20:35 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b2027de0f6b664ea891ed435841a0d444186df6e88b5b5f2946927698336d6`  
		Last Modified: Fri, 24 Apr 2020 16:20:33 GMT  
		Size: 2.0 KB (2000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ab895b5b6b70154da05847062e72d9a1032923b2342443cec884eaf030d888`  
		Last Modified: Fri, 24 Apr 2020 16:20:33 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f4372c45199d48239f882cd33086a7480f6645e6652b886e2558c1b60e68f9b`  
		Last Modified: Fri, 24 Apr 2020 16:21:01 GMT  
		Size: 111.5 MB (111459734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:587f076de92d09903fc17a662bebb324abd1afa13dd10e89f23ff056ae0e3ead`  
		Last Modified: Fri, 24 Apr 2020 16:20:33 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc10f27dd2024e92ff7f713da1de35c2fb0928ebe9405088ee2e73fa12bfa7cb`  
		Last Modified: Fri, 24 Apr 2020 16:20:33 GMT  
		Size: 4.0 KB (3956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4`

```console
$ docker pull mongo@sha256:7663173f07cf97589989d0c9e15015737cf328618cc4d466fc6c9eddd838ac72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x
	-	windows version 10.0.14393.3630; amd64
	-	windows version 10.0.17763.1158; amd64

### `mongo:4` - linux; amd64

```console
$ docker pull mongo@sha256:18f7e39575cd12e9177017ddaa4bcb6c3bae1f6468f3922dc1ecd0662e10281c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164652772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e9495ea1bc639197bc40aef2beedf931078003d8933fb38240f3a1a63c90119`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 20 Mar 2020 19:20:20 GMT
ADD file:594fa35cf803361e69d817fc867b6a4069c064ffd20ed50caf42ad9bb11ca999 in / 
# Fri, 20 Mar 2020 19:20:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 20 Mar 2020 19:20:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 20 Mar 2020 19:20:22 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 20 Mar 2020 19:20:22 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2020 20:49:50 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 20 Mar 2020 20:49:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 16:53:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 17 Apr 2020 16:53:54 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 17 Apr 2020 16:54:10 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 17 Apr 2020 16:54:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 17 Apr 2020 16:54:11 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 17 Apr 2020 16:54:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 17 Apr 2020 16:54:12 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 17 Apr 2020 16:54:13 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 17 Apr 2020 16:54:13 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 17 Apr 2020 16:54:13 GMT
ENV MONGO_MAJOR=4.2
# Mon, 20 Apr 2020 17:44:11 GMT
ENV MONGO_VERSION=4.2.6
# Mon, 20 Apr 2020 17:44:12 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Mon, 20 Apr 2020 17:44:40 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Mon, 20 Apr 2020 17:44:41 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Mon, 20 Apr 2020 17:44:41 GMT
VOLUME [/data/db /data/configdb]
# Mon, 20 Apr 2020 17:44:41 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Mon, 20 Apr 2020 17:44:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2020 17:44:42 GMT
EXPOSE 27017
# Mon, 20 Apr 2020 17:44:42 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:5bed26d33875e6da1d9ff9a1054c5fef3bbeb22ee979e14b72acf72528de007b`  
		Last Modified: Thu, 12 Mar 2020 13:21:29 GMT  
		Size: 26.7 MB (26690587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f11b29a9c7306674a9479158c1b4259938af11b97359d9ac02030cc1095e9ed1`  
		Last Modified: Fri, 20 Mar 2020 19:21:18 GMT  
		Size: 35.4 KB (35372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:930bda195c84cf132344bf38edcad255317382f910503fef234a9ce3bff0f4dd`  
		Last Modified: Fri, 20 Mar 2020 19:21:18 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78bf9a5ad49e4ae42a83f4995ade4efc096f78fd38299cf05bc041e8cdda2a36`  
		Last Modified: Fri, 20 Mar 2020 19:21:18 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7fb3809884c8771103b4475a778eb0a14b736d5f2008d7ef534950c9b6b77d`  
		Last Modified: Fri, 20 Mar 2020 20:50:51 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7237292ff8a2ff64ff0898dc8792b23e5abe90bf32d14f0d4d9eb6ab9e956dd`  
		Last Modified: Fri, 20 Mar 2020 20:50:50 GMT  
		Size: 3.0 MB (2982755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cdf1eb96f71308e6f5be52c3f5278ff6de496b971e1a94d6adb60fc52b2835f`  
		Last Modified: Fri, 17 Apr 2020 16:55:51 GMT  
		Size: 5.8 MB (5824593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39c254c62945d89e0d0e07c721ca9da0ee5848ace6fd9ce95f719a6b721c2be`  
		Last Modified: Fri, 17 Apr 2020 16:55:49 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:110f77aab367a0f38f766fa5d307186a68fdd7483177e20a62c2eee431fb244d`  
		Last Modified: Fri, 17 Apr 2020 16:55:48 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6bec5ffc4eadbe0fa6b84373fe7eaed47c67d2a505a1c640f7cc79c84b5278`  
		Last Modified: Mon, 20 Apr 2020 17:45:00 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d994803edb5bbd3b979490f3ccbe46fc0977dc6fb469fab88fccc9115d0675`  
		Last Modified: Mon, 20 Apr 2020 17:45:27 GMT  
		Size: 129.1 MB (129110699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4266b1dcdabb8fe88172e362ae653d5564293bcd065b45dba2a8e765b4902ab9`  
		Last Modified: Mon, 20 Apr 2020 17:45:00 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3143b095bd39dff0535f074d233459b67c33b68bf2bd7f6d69220bae208a8cac`  
		Last Modified: Mon, 20 Apr 2020 17:45:00 GMT  
		Size: 4.0 KB (3952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:25821e16c7c401986caa09fba3be08b103203a1599edaba8cd34366903b4b3e6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154693716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c06ecd9c0f139339bf92dbef6e630dca8acc4265b72752f7d7b37e16786ed8d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

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
# Fri, 24 Apr 2020 16:18:50 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Apr 2020 16:19:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 16:19:09 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 16:19:09 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Apr 2020 16:19:31 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 16:19:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 16:19:33 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 24 Apr 2020 16:19:35 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 16:19:36 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Apr 2020 16:19:37 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 16:19:37 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 16:19:38 GMT
ENV MONGO_MAJOR=4.2
# Fri, 24 Apr 2020 16:19:38 GMT
ENV MONGO_VERSION=4.2.6
# Fri, 24 Apr 2020 16:19:40 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Apr 2020 16:20:06 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Apr 2020 16:20:09 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Apr 2020 16:20:10 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Apr 2020 16:20:10 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Apr 2020 16:20:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 16:20:11 GMT
EXPOSE 27017
# Fri, 24 Apr 2020 16:20:12 GMT
CMD ["mongod"]
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
	-	`sha256:d1a8d1af89634c78002ec70ef345dd88801eff1bbca938f85fc7472acf873b32`  
		Last Modified: Fri, 24 Apr 2020 16:21:43 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c03832d333b77fecdaaf76768c24a0c6797373a576bd7fb9abc41f3e3e5e2e4`  
		Last Modified: Fri, 24 Apr 2020 16:21:43 GMT  
		Size: 2.7 MB (2675928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544b6736a2d19b775007ab26e1c72ee2e84911c375eec60ec697fe5e8deca69f`  
		Last Modified: Fri, 24 Apr 2020 16:21:44 GMT  
		Size: 5.3 MB (5345352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920aac5b0c675d956885986db6ac84f954ff2f6a98df26a133ae89ae619cd5be`  
		Last Modified: Fri, 24 Apr 2020 16:21:42 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d53bf51618735c85e240ace69cf43a38a4077593fb9b4633fc1d85d2e655016`  
		Last Modified: Fri, 24 Apr 2020 16:21:41 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5296ff1757ed119711f3cc049cb72f1f77178850e6ba2efc6cb0d1e9e1687bdf`  
		Last Modified: Fri, 24 Apr 2020 16:21:41 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7697b84404da018afccd718c3454ed04a6ee05110f0d573a5d73e25a5c5cd75c`  
		Last Modified: Fri, 24 Apr 2020 16:22:09 GMT  
		Size: 122.9 MB (122907968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458af224982cf3028e9a2a89e362caa3e795382c0448adc60b4ab96bedbcc1ef`  
		Last Modified: Fri, 24 Apr 2020 16:21:41 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7506dcffce0af812ecd82776f582f438856fd75e7f948fa2a689a841eaf272e0`  
		Last Modified: Fri, 24 Apr 2020 16:21:41 GMT  
		Size: 4.0 KB (3955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4` - linux; s390x

```console
$ docker pull mongo@sha256:9a853858232155d691db93ab8ab614ad4636f9465aaab10dad522c6ffdbb6fd5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160626574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb6080841c0f9e130ab30d755a2610d8101b8b45a55cfbce1852edce8e90e15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 23 Apr 2020 17:52:20 GMT
ADD file:ea66ef2a01c547f771866bfa221969f8a30489c28d2a81be8dde7f40e73da33b in / 
# Thu, 23 Apr 2020 17:52:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 17:52:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 17:52:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 17:52:31 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 07:34:44 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Apr 2020 07:34:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 07:34:51 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 07:34:51 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Apr 2020 07:35:02 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 07:35:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 07:35:03 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 24 Apr 2020 07:35:09 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 07:35:10 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Apr 2020 07:35:10 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 07:35:10 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 07:35:11 GMT
ENV MONGO_MAJOR=4.2
# Fri, 24 Apr 2020 07:35:11 GMT
ENV MONGO_VERSION=4.2.6
# Fri, 24 Apr 2020 07:35:12 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Apr 2020 07:35:33 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Apr 2020 07:35:38 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Apr 2020 07:35:38 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Apr 2020 07:35:38 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Apr 2020 07:35:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 07:35:39 GMT
EXPOSE 27017
# Fri, 24 Apr 2020 07:35:39 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:13b4c2e4bb97a2a80bb0e557eeba41e4adea0f5e18352e359bca3f847193899c`  
		Last Modified: Mon, 06 Apr 2020 15:41:16 GMT  
		Size: 25.4 MB (25365338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:471a80e39fb485b86610de915eaaad3d867cc97e460b6da3bb656e03520e8a63`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 36.2 KB (36171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb0c128ddabc6a980ec71426ade04fc9bba2e1afcdc243e2d09c316b635f814`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678052ac148ee123df2f0773eb3a0f5f90490ada8b9a5705363b18a2f45fbe88`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c464d6728e9ac439c8d2dc10a88d64a54c34ac50926c66cb7b6d12e37b15d6`  
		Last Modified: Fri, 24 Apr 2020 07:36:04 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd364a38efacff4956ad8e4082d7fa9593aa0a036757fdfbe97487eb26ea2c9`  
		Last Modified: Fri, 24 Apr 2020 07:36:03 GMT  
		Size: 2.7 MB (2714610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e788a62ef53016c8add2417fa25e2141e1b7293acd648f26ed2ddffd54e605b`  
		Last Modified: Fri, 24 Apr 2020 07:36:02 GMT  
		Size: 5.7 MB (5744825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e103dac172d8152c577b2075cc90e6b674188775064cccfbbbc84d93979b3e56`  
		Last Modified: Fri, 24 Apr 2020 07:36:00 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:259fb52c1ef634a5a074adebdaa3f4fc95e636e570c5719c5d662babed85392e`  
		Last Modified: Fri, 24 Apr 2020 07:35:59 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f95c28bb62ddcdbb79cc6870d5cd9701c912a6307bde4c657e1d0c619430fab`  
		Last Modified: Fri, 24 Apr 2020 07:35:58 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05cea8c1238e8ec47654f290d7a566d006d9302762e741316cd236b909d4577d`  
		Last Modified: Fri, 24 Apr 2020 07:36:18 GMT  
		Size: 126.8 MB (126756767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a873535c8ae6f6827fe3d880ab25b1cc404dc3b74898d2ca9bff17136b83caba`  
		Last Modified: Fri, 24 Apr 2020 07:36:04 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d64c0289b5d5c3ee9e04955ed738543e81fdae4e1a43328fd4d88be18d402b`  
		Last Modified: Fri, 24 Apr 2020 07:36:30 GMT  
		Size: 4.0 KB (3954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4` - windows version 10.0.14393.3630; amd64

```console
$ docker pull mongo@sha256:dd6d940f7a8469cd7ff4d01cf767e861e05ea91c4e01707ea74ed2b633b56f20
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6184565858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fe805e4e3cf7852986e9f6716f85f270946e78bb6585812cc72368454753b47`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Apr 2020 17:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Apr 2020 12:52:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 20 Apr 2020 18:34:28 GMT
ENV MONGO_VERSION=4.2.6
# Mon, 20 Apr 2020 18:34:29 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.6-signed.msi
# Mon, 20 Apr 2020 18:34:30 GMT
ENV MONGO_DOWNLOAD_SHA256=401ebc0c087058cd98194046bbd4fbee243592cf9397f36a1fafa208de4ac21e
# Mon, 20 Apr 2020 18:52:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 20 Apr 2020 18:52:25 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 20 Apr 2020 18:52:26 GMT
EXPOSE 27017
# Mon, 20 Apr 2020 18:52:27 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d0099407ec8ccaf0472e55152e38b262bdf0b2cf8dfd2e8afcc89d728ba3f5a0`  
		Size: 1.7 GB (1658081673 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5171ed01a0687a59b2bdf59e2df29a8932abe0ee22a4a6ff6368f8a8295a97d1`  
		Last Modified: Wed, 15 Apr 2020 15:29:42 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a316c4dbc306f67b8ac735d957f87c1afbef1afde59d7b13febb4777781f6eb`  
		Last Modified: Mon, 20 Apr 2020 19:17:03 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e05862ade99bc32c017752427f4eb4ac19437b38181c6900cfed1d6a99d6510`  
		Last Modified: Mon, 20 Apr 2020 19:17:02 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7bdc8ea0d500490783e39f9355fa0349a2d9c32cd29ac8cbdd9a06e848cccda`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f30ae2c8c647fe5e41e956e8cb45d970e0761b0d144aa2a1a1c991f5627caa78`  
		Last Modified: Mon, 20 Apr 2020 19:18:45 GMT  
		Size: 456.5 MB (456490346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2069620de21f9e09ee89665e7488732e9804b4ebabb671846dcc5a2efad828f`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9793d6d47e628c898abbf674bad2cd450299481e89b30f575aac87fc2d186496`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b962b3b43034bdc9d37b9b1a386a2abcdb5b6c8a648d35aa3b46bd884a3c439`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4` - windows version 10.0.17763.1158; amd64

```console
$ docker pull mongo@sha256:98dc02185399f9a980eeac228255f8e42451f535d99c12f71015f176dacbce2f
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2726301729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98407fec53691f82e5cd2eb3a2bda7d93127266f2f6a5f4b7fc5d15a33987224`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Wed, 15 Apr 2020 12:44:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 20 Apr 2020 18:52:33 GMT
ENV MONGO_VERSION=4.2.6
# Mon, 20 Apr 2020 18:52:34 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.6-signed.msi
# Mon, 20 Apr 2020 18:52:35 GMT
ENV MONGO_DOWNLOAD_SHA256=401ebc0c087058cd98194046bbd4fbee243592cf9397f36a1fafa208de4ac21e
# Mon, 20 Apr 2020 19:16:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 20 Apr 2020 19:16:07 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 20 Apr 2020 19:16:08 GMT
EXPOSE 27017
# Mon, 20 Apr 2020 19:16:10 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:442da5a04696895ce6580924a45188bbec9a9db9f81cb7dcef41fc1d4b119130`  
		Last Modified: Wed, 15 Apr 2020 15:29:13 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd1d4721643d80e780c8f74ccda6db920cd5d6702e3a02cecc0a28dc3df2b90`  
		Last Modified: Mon, 20 Apr 2020 19:19:18 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f67966d3a477caf485aaf4080d27615f90dfeed53dd3ba0fd149e65a6b97531`  
		Last Modified: Mon, 20 Apr 2020 19:19:18 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3f18459245d1b377a5dd3fc17087c4c9f225ae47f7e5293f1bd6fca26b0879`  
		Last Modified: Mon, 20 Apr 2020 19:19:15 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff28a577006caf2972aa81e377a6ddbc80a4f337df7c3fc877bc22c875d70b30`  
		Last Modified: Mon, 20 Apr 2020 19:20:11 GMT  
		Size: 455.6 MB (455586654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88cd1efbb2ca082ab8c0e84173075d04be6d252eea7a7f18d961f40e12ac4a0`  
		Last Modified: Mon, 20 Apr 2020 19:19:15 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1eb8768e3e39daa6fe8c5e1c37f5928b6bf0a79e6f13ec87956b42d9e01756d`  
		Last Modified: Mon, 20 Apr 2020 19:19:16 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdc5f1e7a5e65ad06c77f10ba2410b9c07f078d86c597960e5760ad0e398a9d2`  
		Last Modified: Mon, 20 Apr 2020 19:19:15 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.0`

```console
$ docker pull mongo@sha256:87f603aa65ae0faaae359c2b96125f3aedd2a6953924333c8b32b6b1cac6848a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.14393.3630; amd64
	-	windows version 10.0.17763.1158; amd64

### `mongo:4.0` - linux; amd64

```console
$ docker pull mongo@sha256:5ff4514ff351575aa37842896ea330dc14ea026f0baabddc7d7988eeda72bd3d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.7 MB (153661651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d82b5301d74ec719432a0521d65e6a7e4ff4e5e54a4acc789cb4e895e9f16c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 21 Feb 2020 22:22:27 GMT
ADD file:1f70668251e2e58cee0ff0c22ee805f8a269ac6f8934c07f7e89dca6cc1de3aa in / 
# Fri, 21 Feb 2020 22:22:27 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:22:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:22:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:22:30 GMT
CMD ["/bin/bash"]
# Sat, 22 Feb 2020 01:08:16 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Sat, 22 Feb 2020 01:08:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 16:52:33 GMT
ENV GOSU_VERSION=1.12
# Fri, 17 Apr 2020 16:52:33 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 17 Apr 2020 16:53:00 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 17 Apr 2020 16:53:00 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 17 Apr 2020 16:53:28 GMT
ENV GPG_KEYS=9DA31620334BD75D9DCB49F368818C72E52529D4
# Fri, 17 Apr 2020 16:53:29 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 17 Apr 2020 16:53:29 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 17 Apr 2020 16:53:29 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 17 Apr 2020 16:53:29 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 17 Apr 2020 16:53:29 GMT
ENV MONGO_MAJOR=4.0
# Fri, 17 Apr 2020 16:53:30 GMT
ENV MONGO_VERSION=4.0.18
# Fri, 17 Apr 2020 16:53:30 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 17 Apr 2020 16:53:47 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 17 Apr 2020 16:53:48 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 17 Apr 2020 16:53:48 GMT
VOLUME [/data/db /data/configdb]
# Fri, 17 Apr 2020 16:53:48 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 17 Apr 2020 16:53:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2020 16:53:49 GMT
EXPOSE 27017
# Fri, 17 Apr 2020 16:53:49 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:fe703b657a32e0046dce0ad2cb17172cbec8ba302edf370f5f28962bdb6216a9`  
		Last Modified: Thu, 13 Feb 2020 00:25:54 GMT  
		Size: 44.2 MB (44191726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9df1fafd224fae3ba34a68dfc401f75bf6bc0c016fe36c61661ca5c7ad729ee`  
		Last Modified: Fri, 21 Feb 2020 22:23:12 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a645a4b887f9613f80fae43432e46423f196a9952d11bb620bef2add7c4ed4ee`  
		Last Modified: Fri, 21 Feb 2020 22:23:12 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57db7fe0b522b7a6069e769606e5ed0913a64e1e0d0030382a922ccf9449211e`  
		Last Modified: Fri, 21 Feb 2020 22:23:13 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f659f7c5a8a29b7c2592bc12a6afb9babe94617501a765bab59df899dfa98ac`  
		Last Modified: Sat, 22 Feb 2020 01:11:01 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b7ff548bb868b716a6e1ffbc5281d3f298fa1f2d6bac7843ef09901a0ee5c0`  
		Last Modified: Sat, 22 Feb 2020 01:11:02 GMT  
		Size: 2.9 MB (2946077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67a4fc8b9ac596e924ec523f4f913cec4c02bf316c82fab3b22c51e25d54d638`  
		Last Modified: Fri, 17 Apr 2020 16:54:56 GMT  
		Size: 1.3 MB (1305292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2afe62084c30f7e3e50835c0b6462b1f995eb96ec333987aaf1d2ee4db6157`  
		Last Modified: Fri, 17 Apr 2020 16:54:55 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:665eda6efe5a2ca89da71b3ec6c8008d061966135b267f56d91cb89160a709aa`  
		Last Modified: Fri, 17 Apr 2020 16:55:24 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f249afb8789ebd2cd3fa3191b4cf216f2762efa63a931238da6e4d0f8be691`  
		Last Modified: Fri, 17 Apr 2020 16:55:23 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9817b982630eb9b50d91d1fb8d3421347d0e3689ced1362228a59220a12883`  
		Last Modified: Fri, 17 Apr 2020 16:55:43 GMT  
		Size: 105.2 MB (105209155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d52bfe96ec699c4207b7a1cbbabb525e7d2c0522c43715f911f89427ffc17e48`  
		Last Modified: Fri, 17 Apr 2020 16:55:24 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f87759b290cbd65a430b16abe35549620c225a0644191b793a7cab038c4e25a`  
		Last Modified: Fri, 17 Apr 2020 16:55:24 GMT  
		Size: 4.0 KB (3954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:2f2453d105ecfe52f2978b8461d4a4a6a756a329eae7adf18f08e6a6fb294fdb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.3 MB (143329420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0f9f050c13891b73d379f80d79a2a59c001147bc100c01f46470510c75a191d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 24 Apr 2020 00:20:42 GMT
ADD file:24038b6c5a9bab991785fab56202fc43de85e0749e57fcfc361de8aeff302309 in / 
# Fri, 24 Apr 2020 00:20:48 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 00:20:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 00:20:56 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 00:20:58 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 16:16:27 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Apr 2020 16:16:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 16:16:43 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 16:16:43 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Apr 2020 16:17:08 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 16:17:10 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 16:17:59 GMT
ENV GPG_KEYS=9DA31620334BD75D9DCB49F368818C72E52529D4
# Fri, 24 Apr 2020 16:18:00 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 16:18:01 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Apr 2020 16:18:02 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 16:18:02 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 16:18:03 GMT
ENV MONGO_MAJOR=4.0
# Fri, 24 Apr 2020 16:18:04 GMT
ENV MONGO_VERSION=4.0.18
# Fri, 24 Apr 2020 16:18:05 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Apr 2020 16:18:31 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Apr 2020 16:18:34 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Apr 2020 16:18:34 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Apr 2020 16:18:35 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Apr 2020 16:18:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 16:18:36 GMT
EXPOSE 27017
# Fri, 24 Apr 2020 16:18:37 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:ca96533948cdaf1fc84922a44248fcf915a3f526b46555bb96090bed658b00d7`  
		Last Modified: Mon, 30 Mar 2020 15:49:17 GMT  
		Size: 40.0 MB (39968791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c72780e1c95403020a1883a1054d9d48b7a5ad2d940ba2d57ae211369a19685`  
		Last Modified: Fri, 24 Apr 2020 00:22:16 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d962f0171bca79269769ac242507e3f65f2dcbb86de35ecaf164d37b8a89c9d`  
		Last Modified: Fri, 24 Apr 2020 00:22:16 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179f057dc5a95fd6368cf61fa48d9e2d85af21b750813b8dd17b7ad44752c342`  
		Last Modified: Fri, 24 Apr 2020 00:22:17 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0a8e99e85782df175a29b1bde536a79db756966637facaf915cc8e16f38691`  
		Last Modified: Fri, 24 Apr 2020 16:20:35 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a46d993ee733e416b83e56bc49a2736148b105b73cc7553c80fc2aaa7df313b1`  
		Last Modified: Fri, 24 Apr 2020 16:20:35 GMT  
		Size: 2.5 MB (2475001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b49e909411104c2ebb353f5cd8c52434864e5d144971b58f81c3780a4cd037`  
		Last Modified: Fri, 24 Apr 2020 16:20:35 GMT  
		Size: 1.2 MB (1232274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd9944fff526a6c05418546fe52dfcdcf7b391b22af046c09426b603f2e7154`  
		Last Modified: Fri, 24 Apr 2020 16:20:35 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c9cfbc7523eafd818f49310c0660145f99ef417b5e33fc14dde1a4e9c691e89`  
		Last Modified: Fri, 24 Apr 2020 16:21:09 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176c609d312b2670f8da9e72294f1c225dafe5c5bacf1d01b76370affcf3a0ad`  
		Last Modified: Fri, 24 Apr 2020 16:21:09 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ebf85bcab66a237a422958c4176d323878d5a01f16373925994a14b03decbc`  
		Last Modified: Fri, 24 Apr 2020 16:21:34 GMT  
		Size: 99.6 MB (99643925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8e46255fbd40183c4b284dbe92b867b802541e61f0457464eb134faae1f4e8`  
		Last Modified: Fri, 24 Apr 2020 16:21:09 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc8fcc8a0a1a416a06738f37c1af475d21581ce7f1d91a46f67b033ca21ea39`  
		Last Modified: Fri, 24 Apr 2020 16:21:09 GMT  
		Size: 4.0 KB (3956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0` - windows version 10.0.14393.3630; amd64

```console
$ docker pull mongo@sha256:b6e7d94f10b514a0034e43613a7231c9205b851edcd434a220366754980e3d16
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6174608935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9204ac12d78304d62efc38d691baec06bb99ffd71ef6b6c0c7dfb33bd48abd04`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Apr 2020 17:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Apr 2020 12:52:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 16 Apr 2020 00:15:31 GMT
ENV MONGO_VERSION=4.0.18
# Thu, 16 Apr 2020 00:15:32 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.18-signed.msi
# Thu, 16 Apr 2020 00:15:33 GMT
ENV MONGO_DOWNLOAD_SHA256=8f326aff375480941e48852314fbfd4e4e186de6556d753cf09b890ab9241ecf
# Thu, 16 Apr 2020 00:33:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 16 Apr 2020 00:33:42 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 16 Apr 2020 00:33:44 GMT
EXPOSE 27017
# Thu, 16 Apr 2020 00:33:45 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d0099407ec8ccaf0472e55152e38b262bdf0b2cf8dfd2e8afcc89d728ba3f5a0`  
		Size: 1.7 GB (1658081673 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5171ed01a0687a59b2bdf59e2df29a8932abe0ee22a4a6ff6368f8a8295a97d1`  
		Last Modified: Wed, 15 Apr 2020 15:29:42 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a6cd4c1ece17777a2c32dd239a8ba395e23c44f29e0233e281af26c9d2857d`  
		Last Modified: Thu, 16 Apr 2020 00:48:37 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf8b4dd88b18a52ca34aea2c9d21fc28a99db5737a9abd526f97ea9af1f38b2`  
		Last Modified: Thu, 16 Apr 2020 00:48:37 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd28aa952c4558acafcc059815a66472bb0f5eb7ef0cd1d0f851b3354301b140`  
		Last Modified: Thu, 16 Apr 2020 00:48:34 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad3765d0be3c9c109c970bfd4e310c53d3d2d8b1006b87ec93fd9240c577fa2`  
		Last Modified: Thu, 16 Apr 2020 00:50:01 GMT  
		Size: 446.5 MB (446533412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df155fc8098cf06f4508cb44bde84bfe1d4fb867ade29aa374cd0861de8161e4`  
		Last Modified: Thu, 16 Apr 2020 00:48:34 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bad101aceee320e60f5dd9bba9839a069ef5d4a0ead6ad6c29b833328d2b5396`  
		Last Modified: Thu, 16 Apr 2020 00:48:34 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3415fe8d1273fa9bd484bc97b45f1dc83defdc87330120c128494d264022d5b5`  
		Last Modified: Thu, 16 Apr 2020 00:48:34 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0` - windows version 10.0.17763.1158; amd64

```console
$ docker pull mongo@sha256:ccd97bd444338973ac143a22753e6b73a3e707a6a3edd512311a418a3e432cdb
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2356541115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c9945d9fe9ca658fb0b08de9eac6736f7f9f6f6132782ad2f1a33419787310`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Wed, 15 Apr 2020 12:44:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 16 Apr 2020 00:33:51 GMT
ENV MONGO_VERSION=4.0.18
# Thu, 16 Apr 2020 00:33:52 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.18-signed.msi
# Thu, 16 Apr 2020 00:33:53 GMT
ENV MONGO_DOWNLOAD_SHA256=8f326aff375480941e48852314fbfd4e4e186de6556d753cf09b890ab9241ecf
# Thu, 16 Apr 2020 00:47:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 16 Apr 2020 00:47:20 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 16 Apr 2020 00:47:21 GMT
EXPOSE 27017
# Thu, 16 Apr 2020 00:47:23 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:442da5a04696895ce6580924a45188bbec9a9db9f81cb7dcef41fc1d4b119130`  
		Last Modified: Wed, 15 Apr 2020 15:29:13 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d06c5b7d240f934d1a803e7c0affb983bb556079edf76645f5ea89f3eb6ca0`  
		Last Modified: Thu, 16 Apr 2020 00:50:27 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1c8999ac54863eceb53a9253dd6ce7446db0ce0b49f75110116faea049b988`  
		Last Modified: Thu, 16 Apr 2020 00:50:27 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c62229a21e021c6afa0a2d47c9da44bed4152a29f163402db1c46226598c62`  
		Last Modified: Thu, 16 Apr 2020 00:50:24 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b6a77bfcdf682061579dbfd42fb85c94f50e2772f0492635662a42b568d11f`  
		Last Modified: Thu, 16 Apr 2020 00:50:58 GMT  
		Size: 85.8 MB (85825866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376560267143c527c9e648c8674aa8d68445b9af83e1c126daab2c89e4333d12`  
		Last Modified: Thu, 16 Apr 2020 00:50:24 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be795de606456ac97d7b3b1bb6f04c78dc3623e093cc10f27ee1c445974c76bb`  
		Last Modified: Thu, 16 Apr 2020 00:50:24 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c07d006bdcb6ede32d05a301be6b76d939a6d859a5149d7d7d766627e66a218`  
		Last Modified: Thu, 16 Apr 2020 00:50:24 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.0.18`

```console
$ docker pull mongo@sha256:87f603aa65ae0faaae359c2b96125f3aedd2a6953924333c8b32b6b1cac6848a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.14393.3630; amd64
	-	windows version 10.0.17763.1158; amd64

### `mongo:4.0.18` - linux; amd64

```console
$ docker pull mongo@sha256:5ff4514ff351575aa37842896ea330dc14ea026f0baabddc7d7988eeda72bd3d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.7 MB (153661651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d82b5301d74ec719432a0521d65e6a7e4ff4e5e54a4acc789cb4e895e9f16c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 21 Feb 2020 22:22:27 GMT
ADD file:1f70668251e2e58cee0ff0c22ee805f8a269ac6f8934c07f7e89dca6cc1de3aa in / 
# Fri, 21 Feb 2020 22:22:27 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:22:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:22:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:22:30 GMT
CMD ["/bin/bash"]
# Sat, 22 Feb 2020 01:08:16 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Sat, 22 Feb 2020 01:08:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 16:52:33 GMT
ENV GOSU_VERSION=1.12
# Fri, 17 Apr 2020 16:52:33 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 17 Apr 2020 16:53:00 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 17 Apr 2020 16:53:00 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 17 Apr 2020 16:53:28 GMT
ENV GPG_KEYS=9DA31620334BD75D9DCB49F368818C72E52529D4
# Fri, 17 Apr 2020 16:53:29 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 17 Apr 2020 16:53:29 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 17 Apr 2020 16:53:29 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 17 Apr 2020 16:53:29 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 17 Apr 2020 16:53:29 GMT
ENV MONGO_MAJOR=4.0
# Fri, 17 Apr 2020 16:53:30 GMT
ENV MONGO_VERSION=4.0.18
# Fri, 17 Apr 2020 16:53:30 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 17 Apr 2020 16:53:47 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 17 Apr 2020 16:53:48 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 17 Apr 2020 16:53:48 GMT
VOLUME [/data/db /data/configdb]
# Fri, 17 Apr 2020 16:53:48 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 17 Apr 2020 16:53:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2020 16:53:49 GMT
EXPOSE 27017
# Fri, 17 Apr 2020 16:53:49 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:fe703b657a32e0046dce0ad2cb17172cbec8ba302edf370f5f28962bdb6216a9`  
		Last Modified: Thu, 13 Feb 2020 00:25:54 GMT  
		Size: 44.2 MB (44191726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9df1fafd224fae3ba34a68dfc401f75bf6bc0c016fe36c61661ca5c7ad729ee`  
		Last Modified: Fri, 21 Feb 2020 22:23:12 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a645a4b887f9613f80fae43432e46423f196a9952d11bb620bef2add7c4ed4ee`  
		Last Modified: Fri, 21 Feb 2020 22:23:12 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57db7fe0b522b7a6069e769606e5ed0913a64e1e0d0030382a922ccf9449211e`  
		Last Modified: Fri, 21 Feb 2020 22:23:13 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f659f7c5a8a29b7c2592bc12a6afb9babe94617501a765bab59df899dfa98ac`  
		Last Modified: Sat, 22 Feb 2020 01:11:01 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b7ff548bb868b716a6e1ffbc5281d3f298fa1f2d6bac7843ef09901a0ee5c0`  
		Last Modified: Sat, 22 Feb 2020 01:11:02 GMT  
		Size: 2.9 MB (2946077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67a4fc8b9ac596e924ec523f4f913cec4c02bf316c82fab3b22c51e25d54d638`  
		Last Modified: Fri, 17 Apr 2020 16:54:56 GMT  
		Size: 1.3 MB (1305292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2afe62084c30f7e3e50835c0b6462b1f995eb96ec333987aaf1d2ee4db6157`  
		Last Modified: Fri, 17 Apr 2020 16:54:55 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:665eda6efe5a2ca89da71b3ec6c8008d061966135b267f56d91cb89160a709aa`  
		Last Modified: Fri, 17 Apr 2020 16:55:24 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f249afb8789ebd2cd3fa3191b4cf216f2762efa63a931238da6e4d0f8be691`  
		Last Modified: Fri, 17 Apr 2020 16:55:23 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9817b982630eb9b50d91d1fb8d3421347d0e3689ced1362228a59220a12883`  
		Last Modified: Fri, 17 Apr 2020 16:55:43 GMT  
		Size: 105.2 MB (105209155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d52bfe96ec699c4207b7a1cbbabb525e7d2c0522c43715f911f89427ffc17e48`  
		Last Modified: Fri, 17 Apr 2020 16:55:24 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f87759b290cbd65a430b16abe35549620c225a0644191b793a7cab038c4e25a`  
		Last Modified: Fri, 17 Apr 2020 16:55:24 GMT  
		Size: 4.0 KB (3954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0.18` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:2f2453d105ecfe52f2978b8461d4a4a6a756a329eae7adf18f08e6a6fb294fdb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.3 MB (143329420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0f9f050c13891b73d379f80d79a2a59c001147bc100c01f46470510c75a191d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 24 Apr 2020 00:20:42 GMT
ADD file:24038b6c5a9bab991785fab56202fc43de85e0749e57fcfc361de8aeff302309 in / 
# Fri, 24 Apr 2020 00:20:48 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 00:20:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 00:20:56 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 00:20:58 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 16:16:27 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Apr 2020 16:16:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 16:16:43 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 16:16:43 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Apr 2020 16:17:08 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 16:17:10 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 16:17:59 GMT
ENV GPG_KEYS=9DA31620334BD75D9DCB49F368818C72E52529D4
# Fri, 24 Apr 2020 16:18:00 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 16:18:01 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Apr 2020 16:18:02 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 16:18:02 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 16:18:03 GMT
ENV MONGO_MAJOR=4.0
# Fri, 24 Apr 2020 16:18:04 GMT
ENV MONGO_VERSION=4.0.18
# Fri, 24 Apr 2020 16:18:05 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Apr 2020 16:18:31 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Apr 2020 16:18:34 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Apr 2020 16:18:34 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Apr 2020 16:18:35 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Apr 2020 16:18:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 16:18:36 GMT
EXPOSE 27017
# Fri, 24 Apr 2020 16:18:37 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:ca96533948cdaf1fc84922a44248fcf915a3f526b46555bb96090bed658b00d7`  
		Last Modified: Mon, 30 Mar 2020 15:49:17 GMT  
		Size: 40.0 MB (39968791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c72780e1c95403020a1883a1054d9d48b7a5ad2d940ba2d57ae211369a19685`  
		Last Modified: Fri, 24 Apr 2020 00:22:16 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d962f0171bca79269769ac242507e3f65f2dcbb86de35ecaf164d37b8a89c9d`  
		Last Modified: Fri, 24 Apr 2020 00:22:16 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179f057dc5a95fd6368cf61fa48d9e2d85af21b750813b8dd17b7ad44752c342`  
		Last Modified: Fri, 24 Apr 2020 00:22:17 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0a8e99e85782df175a29b1bde536a79db756966637facaf915cc8e16f38691`  
		Last Modified: Fri, 24 Apr 2020 16:20:35 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a46d993ee733e416b83e56bc49a2736148b105b73cc7553c80fc2aaa7df313b1`  
		Last Modified: Fri, 24 Apr 2020 16:20:35 GMT  
		Size: 2.5 MB (2475001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b49e909411104c2ebb353f5cd8c52434864e5d144971b58f81c3780a4cd037`  
		Last Modified: Fri, 24 Apr 2020 16:20:35 GMT  
		Size: 1.2 MB (1232274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd9944fff526a6c05418546fe52dfcdcf7b391b22af046c09426b603f2e7154`  
		Last Modified: Fri, 24 Apr 2020 16:20:35 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c9cfbc7523eafd818f49310c0660145f99ef417b5e33fc14dde1a4e9c691e89`  
		Last Modified: Fri, 24 Apr 2020 16:21:09 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176c609d312b2670f8da9e72294f1c225dafe5c5bacf1d01b76370affcf3a0ad`  
		Last Modified: Fri, 24 Apr 2020 16:21:09 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ebf85bcab66a237a422958c4176d323878d5a01f16373925994a14b03decbc`  
		Last Modified: Fri, 24 Apr 2020 16:21:34 GMT  
		Size: 99.6 MB (99643925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8e46255fbd40183c4b284dbe92b867b802541e61f0457464eb134faae1f4e8`  
		Last Modified: Fri, 24 Apr 2020 16:21:09 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc8fcc8a0a1a416a06738f37c1af475d21581ce7f1d91a46f67b033ca21ea39`  
		Last Modified: Fri, 24 Apr 2020 16:21:09 GMT  
		Size: 4.0 KB (3956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0.18` - windows version 10.0.14393.3630; amd64

```console
$ docker pull mongo@sha256:b6e7d94f10b514a0034e43613a7231c9205b851edcd434a220366754980e3d16
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6174608935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9204ac12d78304d62efc38d691baec06bb99ffd71ef6b6c0c7dfb33bd48abd04`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Apr 2020 17:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Apr 2020 12:52:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 16 Apr 2020 00:15:31 GMT
ENV MONGO_VERSION=4.0.18
# Thu, 16 Apr 2020 00:15:32 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.18-signed.msi
# Thu, 16 Apr 2020 00:15:33 GMT
ENV MONGO_DOWNLOAD_SHA256=8f326aff375480941e48852314fbfd4e4e186de6556d753cf09b890ab9241ecf
# Thu, 16 Apr 2020 00:33:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 16 Apr 2020 00:33:42 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 16 Apr 2020 00:33:44 GMT
EXPOSE 27017
# Thu, 16 Apr 2020 00:33:45 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d0099407ec8ccaf0472e55152e38b262bdf0b2cf8dfd2e8afcc89d728ba3f5a0`  
		Size: 1.7 GB (1658081673 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5171ed01a0687a59b2bdf59e2df29a8932abe0ee22a4a6ff6368f8a8295a97d1`  
		Last Modified: Wed, 15 Apr 2020 15:29:42 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a6cd4c1ece17777a2c32dd239a8ba395e23c44f29e0233e281af26c9d2857d`  
		Last Modified: Thu, 16 Apr 2020 00:48:37 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf8b4dd88b18a52ca34aea2c9d21fc28a99db5737a9abd526f97ea9af1f38b2`  
		Last Modified: Thu, 16 Apr 2020 00:48:37 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd28aa952c4558acafcc059815a66472bb0f5eb7ef0cd1d0f851b3354301b140`  
		Last Modified: Thu, 16 Apr 2020 00:48:34 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad3765d0be3c9c109c970bfd4e310c53d3d2d8b1006b87ec93fd9240c577fa2`  
		Last Modified: Thu, 16 Apr 2020 00:50:01 GMT  
		Size: 446.5 MB (446533412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df155fc8098cf06f4508cb44bde84bfe1d4fb867ade29aa374cd0861de8161e4`  
		Last Modified: Thu, 16 Apr 2020 00:48:34 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bad101aceee320e60f5dd9bba9839a069ef5d4a0ead6ad6c29b833328d2b5396`  
		Last Modified: Thu, 16 Apr 2020 00:48:34 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3415fe8d1273fa9bd484bc97b45f1dc83defdc87330120c128494d264022d5b5`  
		Last Modified: Thu, 16 Apr 2020 00:48:34 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0.18` - windows version 10.0.17763.1158; amd64

```console
$ docker pull mongo@sha256:ccd97bd444338973ac143a22753e6b73a3e707a6a3edd512311a418a3e432cdb
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2356541115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c9945d9fe9ca658fb0b08de9eac6736f7f9f6f6132782ad2f1a33419787310`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Wed, 15 Apr 2020 12:44:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 16 Apr 2020 00:33:51 GMT
ENV MONGO_VERSION=4.0.18
# Thu, 16 Apr 2020 00:33:52 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.18-signed.msi
# Thu, 16 Apr 2020 00:33:53 GMT
ENV MONGO_DOWNLOAD_SHA256=8f326aff375480941e48852314fbfd4e4e186de6556d753cf09b890ab9241ecf
# Thu, 16 Apr 2020 00:47:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 16 Apr 2020 00:47:20 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 16 Apr 2020 00:47:21 GMT
EXPOSE 27017
# Thu, 16 Apr 2020 00:47:23 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:442da5a04696895ce6580924a45188bbec9a9db9f81cb7dcef41fc1d4b119130`  
		Last Modified: Wed, 15 Apr 2020 15:29:13 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d06c5b7d240f934d1a803e7c0affb983bb556079edf76645f5ea89f3eb6ca0`  
		Last Modified: Thu, 16 Apr 2020 00:50:27 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1c8999ac54863eceb53a9253dd6ce7446db0ce0b49f75110116faea049b988`  
		Last Modified: Thu, 16 Apr 2020 00:50:27 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c62229a21e021c6afa0a2d47c9da44bed4152a29f163402db1c46226598c62`  
		Last Modified: Thu, 16 Apr 2020 00:50:24 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b6a77bfcdf682061579dbfd42fb85c94f50e2772f0492635662a42b568d11f`  
		Last Modified: Thu, 16 Apr 2020 00:50:58 GMT  
		Size: 85.8 MB (85825866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376560267143c527c9e648c8674aa8d68445b9af83e1c126daab2c89e4333d12`  
		Last Modified: Thu, 16 Apr 2020 00:50:24 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be795de606456ac97d7b3b1bb6f04c78dc3623e093cc10f27ee1c445974c76bb`  
		Last Modified: Thu, 16 Apr 2020 00:50:24 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c07d006bdcb6ede32d05a301be6b76d939a6d859a5149d7d7d766627e66a218`  
		Last Modified: Thu, 16 Apr 2020 00:50:24 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.0.18-windowsservercore`

```console
$ docker pull mongo@sha256:9ff147feebb98918c160ec6bc52c5cb7d2a6d1a2484f9509409a9caad28a9219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3630; amd64
	-	windows version 10.0.17763.1158; amd64

### `mongo:4.0.18-windowsservercore` - windows version 10.0.14393.3630; amd64

```console
$ docker pull mongo@sha256:b6e7d94f10b514a0034e43613a7231c9205b851edcd434a220366754980e3d16
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6174608935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9204ac12d78304d62efc38d691baec06bb99ffd71ef6b6c0c7dfb33bd48abd04`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Apr 2020 17:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Apr 2020 12:52:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 16 Apr 2020 00:15:31 GMT
ENV MONGO_VERSION=4.0.18
# Thu, 16 Apr 2020 00:15:32 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.18-signed.msi
# Thu, 16 Apr 2020 00:15:33 GMT
ENV MONGO_DOWNLOAD_SHA256=8f326aff375480941e48852314fbfd4e4e186de6556d753cf09b890ab9241ecf
# Thu, 16 Apr 2020 00:33:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 16 Apr 2020 00:33:42 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 16 Apr 2020 00:33:44 GMT
EXPOSE 27017
# Thu, 16 Apr 2020 00:33:45 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d0099407ec8ccaf0472e55152e38b262bdf0b2cf8dfd2e8afcc89d728ba3f5a0`  
		Size: 1.7 GB (1658081673 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5171ed01a0687a59b2bdf59e2df29a8932abe0ee22a4a6ff6368f8a8295a97d1`  
		Last Modified: Wed, 15 Apr 2020 15:29:42 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a6cd4c1ece17777a2c32dd239a8ba395e23c44f29e0233e281af26c9d2857d`  
		Last Modified: Thu, 16 Apr 2020 00:48:37 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf8b4dd88b18a52ca34aea2c9d21fc28a99db5737a9abd526f97ea9af1f38b2`  
		Last Modified: Thu, 16 Apr 2020 00:48:37 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd28aa952c4558acafcc059815a66472bb0f5eb7ef0cd1d0f851b3354301b140`  
		Last Modified: Thu, 16 Apr 2020 00:48:34 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad3765d0be3c9c109c970bfd4e310c53d3d2d8b1006b87ec93fd9240c577fa2`  
		Last Modified: Thu, 16 Apr 2020 00:50:01 GMT  
		Size: 446.5 MB (446533412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df155fc8098cf06f4508cb44bde84bfe1d4fb867ade29aa374cd0861de8161e4`  
		Last Modified: Thu, 16 Apr 2020 00:48:34 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bad101aceee320e60f5dd9bba9839a069ef5d4a0ead6ad6c29b833328d2b5396`  
		Last Modified: Thu, 16 Apr 2020 00:48:34 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3415fe8d1273fa9bd484bc97b45f1dc83defdc87330120c128494d264022d5b5`  
		Last Modified: Thu, 16 Apr 2020 00:48:34 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0.18-windowsservercore` - windows version 10.0.17763.1158; amd64

```console
$ docker pull mongo@sha256:ccd97bd444338973ac143a22753e6b73a3e707a6a3edd512311a418a3e432cdb
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2356541115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c9945d9fe9ca658fb0b08de9eac6736f7f9f6f6132782ad2f1a33419787310`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Wed, 15 Apr 2020 12:44:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 16 Apr 2020 00:33:51 GMT
ENV MONGO_VERSION=4.0.18
# Thu, 16 Apr 2020 00:33:52 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.18-signed.msi
# Thu, 16 Apr 2020 00:33:53 GMT
ENV MONGO_DOWNLOAD_SHA256=8f326aff375480941e48852314fbfd4e4e186de6556d753cf09b890ab9241ecf
# Thu, 16 Apr 2020 00:47:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 16 Apr 2020 00:47:20 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 16 Apr 2020 00:47:21 GMT
EXPOSE 27017
# Thu, 16 Apr 2020 00:47:23 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:442da5a04696895ce6580924a45188bbec9a9db9f81cb7dcef41fc1d4b119130`  
		Last Modified: Wed, 15 Apr 2020 15:29:13 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d06c5b7d240f934d1a803e7c0affb983bb556079edf76645f5ea89f3eb6ca0`  
		Last Modified: Thu, 16 Apr 2020 00:50:27 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1c8999ac54863eceb53a9253dd6ce7446db0ce0b49f75110116faea049b988`  
		Last Modified: Thu, 16 Apr 2020 00:50:27 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c62229a21e021c6afa0a2d47c9da44bed4152a29f163402db1c46226598c62`  
		Last Modified: Thu, 16 Apr 2020 00:50:24 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b6a77bfcdf682061579dbfd42fb85c94f50e2772f0492635662a42b568d11f`  
		Last Modified: Thu, 16 Apr 2020 00:50:58 GMT  
		Size: 85.8 MB (85825866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376560267143c527c9e648c8674aa8d68445b9af83e1c126daab2c89e4333d12`  
		Last Modified: Thu, 16 Apr 2020 00:50:24 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be795de606456ac97d7b3b1bb6f04c78dc3623e093cc10f27ee1c445974c76bb`  
		Last Modified: Thu, 16 Apr 2020 00:50:24 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c07d006bdcb6ede32d05a301be6b76d939a6d859a5149d7d7d766627e66a218`  
		Last Modified: Thu, 16 Apr 2020 00:50:24 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.0.18-windowsservercore-1809`

```console
$ docker pull mongo@sha256:a9b083f53dd089dd440cf5ed74930321789f2aa0dd617106f147df77fedcf731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1158; amd64

### `mongo:4.0.18-windowsservercore-1809` - windows version 10.0.17763.1158; amd64

```console
$ docker pull mongo@sha256:ccd97bd444338973ac143a22753e6b73a3e707a6a3edd512311a418a3e432cdb
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2356541115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c9945d9fe9ca658fb0b08de9eac6736f7f9f6f6132782ad2f1a33419787310`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Wed, 15 Apr 2020 12:44:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 16 Apr 2020 00:33:51 GMT
ENV MONGO_VERSION=4.0.18
# Thu, 16 Apr 2020 00:33:52 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.18-signed.msi
# Thu, 16 Apr 2020 00:33:53 GMT
ENV MONGO_DOWNLOAD_SHA256=8f326aff375480941e48852314fbfd4e4e186de6556d753cf09b890ab9241ecf
# Thu, 16 Apr 2020 00:47:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 16 Apr 2020 00:47:20 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 16 Apr 2020 00:47:21 GMT
EXPOSE 27017
# Thu, 16 Apr 2020 00:47:23 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:442da5a04696895ce6580924a45188bbec9a9db9f81cb7dcef41fc1d4b119130`  
		Last Modified: Wed, 15 Apr 2020 15:29:13 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d06c5b7d240f934d1a803e7c0affb983bb556079edf76645f5ea89f3eb6ca0`  
		Last Modified: Thu, 16 Apr 2020 00:50:27 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1c8999ac54863eceb53a9253dd6ce7446db0ce0b49f75110116faea049b988`  
		Last Modified: Thu, 16 Apr 2020 00:50:27 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c62229a21e021c6afa0a2d47c9da44bed4152a29f163402db1c46226598c62`  
		Last Modified: Thu, 16 Apr 2020 00:50:24 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b6a77bfcdf682061579dbfd42fb85c94f50e2772f0492635662a42b568d11f`  
		Last Modified: Thu, 16 Apr 2020 00:50:58 GMT  
		Size: 85.8 MB (85825866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376560267143c527c9e648c8674aa8d68445b9af83e1c126daab2c89e4333d12`  
		Last Modified: Thu, 16 Apr 2020 00:50:24 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be795de606456ac97d7b3b1bb6f04c78dc3623e093cc10f27ee1c445974c76bb`  
		Last Modified: Thu, 16 Apr 2020 00:50:24 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c07d006bdcb6ede32d05a301be6b76d939a6d859a5149d7d7d766627e66a218`  
		Last Modified: Thu, 16 Apr 2020 00:50:24 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.0.18-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:a869c2a880cc57c5c93e56a9dc5ea6950b4d905471b65ecacd94c8107e225470
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3630; amd64

### `mongo:4.0.18-windowsservercore-ltsc2016` - windows version 10.0.14393.3630; amd64

```console
$ docker pull mongo@sha256:b6e7d94f10b514a0034e43613a7231c9205b851edcd434a220366754980e3d16
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6174608935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9204ac12d78304d62efc38d691baec06bb99ffd71ef6b6c0c7dfb33bd48abd04`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Apr 2020 17:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Apr 2020 12:52:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 16 Apr 2020 00:15:31 GMT
ENV MONGO_VERSION=4.0.18
# Thu, 16 Apr 2020 00:15:32 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.18-signed.msi
# Thu, 16 Apr 2020 00:15:33 GMT
ENV MONGO_DOWNLOAD_SHA256=8f326aff375480941e48852314fbfd4e4e186de6556d753cf09b890ab9241ecf
# Thu, 16 Apr 2020 00:33:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 16 Apr 2020 00:33:42 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 16 Apr 2020 00:33:44 GMT
EXPOSE 27017
# Thu, 16 Apr 2020 00:33:45 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d0099407ec8ccaf0472e55152e38b262bdf0b2cf8dfd2e8afcc89d728ba3f5a0`  
		Size: 1.7 GB (1658081673 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5171ed01a0687a59b2bdf59e2df29a8932abe0ee22a4a6ff6368f8a8295a97d1`  
		Last Modified: Wed, 15 Apr 2020 15:29:42 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a6cd4c1ece17777a2c32dd239a8ba395e23c44f29e0233e281af26c9d2857d`  
		Last Modified: Thu, 16 Apr 2020 00:48:37 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf8b4dd88b18a52ca34aea2c9d21fc28a99db5737a9abd526f97ea9af1f38b2`  
		Last Modified: Thu, 16 Apr 2020 00:48:37 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd28aa952c4558acafcc059815a66472bb0f5eb7ef0cd1d0f851b3354301b140`  
		Last Modified: Thu, 16 Apr 2020 00:48:34 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad3765d0be3c9c109c970bfd4e310c53d3d2d8b1006b87ec93fd9240c577fa2`  
		Last Modified: Thu, 16 Apr 2020 00:50:01 GMT  
		Size: 446.5 MB (446533412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df155fc8098cf06f4508cb44bde84bfe1d4fb867ade29aa374cd0861de8161e4`  
		Last Modified: Thu, 16 Apr 2020 00:48:34 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bad101aceee320e60f5dd9bba9839a069ef5d4a0ead6ad6c29b833328d2b5396`  
		Last Modified: Thu, 16 Apr 2020 00:48:34 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3415fe8d1273fa9bd484bc97b45f1dc83defdc87330120c128494d264022d5b5`  
		Last Modified: Thu, 16 Apr 2020 00:48:34 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.0.18-xenial`

```console
$ docker pull mongo@sha256:88627ec198bd62e7a5e7f1fa2e7f130a8e161b0bdb392f3076c654d6ddb289a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:4.0.18-xenial` - linux; amd64

```console
$ docker pull mongo@sha256:5ff4514ff351575aa37842896ea330dc14ea026f0baabddc7d7988eeda72bd3d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.7 MB (153661651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d82b5301d74ec719432a0521d65e6a7e4ff4e5e54a4acc789cb4e895e9f16c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 21 Feb 2020 22:22:27 GMT
ADD file:1f70668251e2e58cee0ff0c22ee805f8a269ac6f8934c07f7e89dca6cc1de3aa in / 
# Fri, 21 Feb 2020 22:22:27 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:22:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:22:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:22:30 GMT
CMD ["/bin/bash"]
# Sat, 22 Feb 2020 01:08:16 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Sat, 22 Feb 2020 01:08:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 16:52:33 GMT
ENV GOSU_VERSION=1.12
# Fri, 17 Apr 2020 16:52:33 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 17 Apr 2020 16:53:00 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 17 Apr 2020 16:53:00 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 17 Apr 2020 16:53:28 GMT
ENV GPG_KEYS=9DA31620334BD75D9DCB49F368818C72E52529D4
# Fri, 17 Apr 2020 16:53:29 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 17 Apr 2020 16:53:29 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 17 Apr 2020 16:53:29 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 17 Apr 2020 16:53:29 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 17 Apr 2020 16:53:29 GMT
ENV MONGO_MAJOR=4.0
# Fri, 17 Apr 2020 16:53:30 GMT
ENV MONGO_VERSION=4.0.18
# Fri, 17 Apr 2020 16:53:30 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 17 Apr 2020 16:53:47 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 17 Apr 2020 16:53:48 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 17 Apr 2020 16:53:48 GMT
VOLUME [/data/db /data/configdb]
# Fri, 17 Apr 2020 16:53:48 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 17 Apr 2020 16:53:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2020 16:53:49 GMT
EXPOSE 27017
# Fri, 17 Apr 2020 16:53:49 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:fe703b657a32e0046dce0ad2cb17172cbec8ba302edf370f5f28962bdb6216a9`  
		Last Modified: Thu, 13 Feb 2020 00:25:54 GMT  
		Size: 44.2 MB (44191726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9df1fafd224fae3ba34a68dfc401f75bf6bc0c016fe36c61661ca5c7ad729ee`  
		Last Modified: Fri, 21 Feb 2020 22:23:12 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a645a4b887f9613f80fae43432e46423f196a9952d11bb620bef2add7c4ed4ee`  
		Last Modified: Fri, 21 Feb 2020 22:23:12 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57db7fe0b522b7a6069e769606e5ed0913a64e1e0d0030382a922ccf9449211e`  
		Last Modified: Fri, 21 Feb 2020 22:23:13 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f659f7c5a8a29b7c2592bc12a6afb9babe94617501a765bab59df899dfa98ac`  
		Last Modified: Sat, 22 Feb 2020 01:11:01 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b7ff548bb868b716a6e1ffbc5281d3f298fa1f2d6bac7843ef09901a0ee5c0`  
		Last Modified: Sat, 22 Feb 2020 01:11:02 GMT  
		Size: 2.9 MB (2946077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67a4fc8b9ac596e924ec523f4f913cec4c02bf316c82fab3b22c51e25d54d638`  
		Last Modified: Fri, 17 Apr 2020 16:54:56 GMT  
		Size: 1.3 MB (1305292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2afe62084c30f7e3e50835c0b6462b1f995eb96ec333987aaf1d2ee4db6157`  
		Last Modified: Fri, 17 Apr 2020 16:54:55 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:665eda6efe5a2ca89da71b3ec6c8008d061966135b267f56d91cb89160a709aa`  
		Last Modified: Fri, 17 Apr 2020 16:55:24 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f249afb8789ebd2cd3fa3191b4cf216f2762efa63a931238da6e4d0f8be691`  
		Last Modified: Fri, 17 Apr 2020 16:55:23 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9817b982630eb9b50d91d1fb8d3421347d0e3689ced1362228a59220a12883`  
		Last Modified: Fri, 17 Apr 2020 16:55:43 GMT  
		Size: 105.2 MB (105209155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d52bfe96ec699c4207b7a1cbbabb525e7d2c0522c43715f911f89427ffc17e48`  
		Last Modified: Fri, 17 Apr 2020 16:55:24 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f87759b290cbd65a430b16abe35549620c225a0644191b793a7cab038c4e25a`  
		Last Modified: Fri, 17 Apr 2020 16:55:24 GMT  
		Size: 4.0 KB (3954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0.18-xenial` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:2f2453d105ecfe52f2978b8461d4a4a6a756a329eae7adf18f08e6a6fb294fdb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.3 MB (143329420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0f9f050c13891b73d379f80d79a2a59c001147bc100c01f46470510c75a191d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 24 Apr 2020 00:20:42 GMT
ADD file:24038b6c5a9bab991785fab56202fc43de85e0749e57fcfc361de8aeff302309 in / 
# Fri, 24 Apr 2020 00:20:48 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 00:20:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 00:20:56 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 00:20:58 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 16:16:27 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Apr 2020 16:16:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 16:16:43 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 16:16:43 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Apr 2020 16:17:08 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 16:17:10 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 16:17:59 GMT
ENV GPG_KEYS=9DA31620334BD75D9DCB49F368818C72E52529D4
# Fri, 24 Apr 2020 16:18:00 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 16:18:01 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Apr 2020 16:18:02 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 16:18:02 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 16:18:03 GMT
ENV MONGO_MAJOR=4.0
# Fri, 24 Apr 2020 16:18:04 GMT
ENV MONGO_VERSION=4.0.18
# Fri, 24 Apr 2020 16:18:05 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Apr 2020 16:18:31 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Apr 2020 16:18:34 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Apr 2020 16:18:34 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Apr 2020 16:18:35 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Apr 2020 16:18:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 16:18:36 GMT
EXPOSE 27017
# Fri, 24 Apr 2020 16:18:37 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:ca96533948cdaf1fc84922a44248fcf915a3f526b46555bb96090bed658b00d7`  
		Last Modified: Mon, 30 Mar 2020 15:49:17 GMT  
		Size: 40.0 MB (39968791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c72780e1c95403020a1883a1054d9d48b7a5ad2d940ba2d57ae211369a19685`  
		Last Modified: Fri, 24 Apr 2020 00:22:16 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d962f0171bca79269769ac242507e3f65f2dcbb86de35ecaf164d37b8a89c9d`  
		Last Modified: Fri, 24 Apr 2020 00:22:16 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179f057dc5a95fd6368cf61fa48d9e2d85af21b750813b8dd17b7ad44752c342`  
		Last Modified: Fri, 24 Apr 2020 00:22:17 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0a8e99e85782df175a29b1bde536a79db756966637facaf915cc8e16f38691`  
		Last Modified: Fri, 24 Apr 2020 16:20:35 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a46d993ee733e416b83e56bc49a2736148b105b73cc7553c80fc2aaa7df313b1`  
		Last Modified: Fri, 24 Apr 2020 16:20:35 GMT  
		Size: 2.5 MB (2475001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b49e909411104c2ebb353f5cd8c52434864e5d144971b58f81c3780a4cd037`  
		Last Modified: Fri, 24 Apr 2020 16:20:35 GMT  
		Size: 1.2 MB (1232274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd9944fff526a6c05418546fe52dfcdcf7b391b22af046c09426b603f2e7154`  
		Last Modified: Fri, 24 Apr 2020 16:20:35 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c9cfbc7523eafd818f49310c0660145f99ef417b5e33fc14dde1a4e9c691e89`  
		Last Modified: Fri, 24 Apr 2020 16:21:09 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176c609d312b2670f8da9e72294f1c225dafe5c5bacf1d01b76370affcf3a0ad`  
		Last Modified: Fri, 24 Apr 2020 16:21:09 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ebf85bcab66a237a422958c4176d323878d5a01f16373925994a14b03decbc`  
		Last Modified: Fri, 24 Apr 2020 16:21:34 GMT  
		Size: 99.6 MB (99643925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8e46255fbd40183c4b284dbe92b867b802541e61f0457464eb134faae1f4e8`  
		Last Modified: Fri, 24 Apr 2020 16:21:09 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc8fcc8a0a1a416a06738f37c1af475d21581ce7f1d91a46f67b033ca21ea39`  
		Last Modified: Fri, 24 Apr 2020 16:21:09 GMT  
		Size: 4.0 KB (3956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.0-windowsservercore`

```console
$ docker pull mongo@sha256:9ff147feebb98918c160ec6bc52c5cb7d2a6d1a2484f9509409a9caad28a9219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3630; amd64
	-	windows version 10.0.17763.1158; amd64

### `mongo:4.0-windowsservercore` - windows version 10.0.14393.3630; amd64

```console
$ docker pull mongo@sha256:b6e7d94f10b514a0034e43613a7231c9205b851edcd434a220366754980e3d16
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6174608935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9204ac12d78304d62efc38d691baec06bb99ffd71ef6b6c0c7dfb33bd48abd04`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Apr 2020 17:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Apr 2020 12:52:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 16 Apr 2020 00:15:31 GMT
ENV MONGO_VERSION=4.0.18
# Thu, 16 Apr 2020 00:15:32 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.18-signed.msi
# Thu, 16 Apr 2020 00:15:33 GMT
ENV MONGO_DOWNLOAD_SHA256=8f326aff375480941e48852314fbfd4e4e186de6556d753cf09b890ab9241ecf
# Thu, 16 Apr 2020 00:33:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 16 Apr 2020 00:33:42 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 16 Apr 2020 00:33:44 GMT
EXPOSE 27017
# Thu, 16 Apr 2020 00:33:45 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d0099407ec8ccaf0472e55152e38b262bdf0b2cf8dfd2e8afcc89d728ba3f5a0`  
		Size: 1.7 GB (1658081673 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5171ed01a0687a59b2bdf59e2df29a8932abe0ee22a4a6ff6368f8a8295a97d1`  
		Last Modified: Wed, 15 Apr 2020 15:29:42 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a6cd4c1ece17777a2c32dd239a8ba395e23c44f29e0233e281af26c9d2857d`  
		Last Modified: Thu, 16 Apr 2020 00:48:37 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf8b4dd88b18a52ca34aea2c9d21fc28a99db5737a9abd526f97ea9af1f38b2`  
		Last Modified: Thu, 16 Apr 2020 00:48:37 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd28aa952c4558acafcc059815a66472bb0f5eb7ef0cd1d0f851b3354301b140`  
		Last Modified: Thu, 16 Apr 2020 00:48:34 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad3765d0be3c9c109c970bfd4e310c53d3d2d8b1006b87ec93fd9240c577fa2`  
		Last Modified: Thu, 16 Apr 2020 00:50:01 GMT  
		Size: 446.5 MB (446533412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df155fc8098cf06f4508cb44bde84bfe1d4fb867ade29aa374cd0861de8161e4`  
		Last Modified: Thu, 16 Apr 2020 00:48:34 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bad101aceee320e60f5dd9bba9839a069ef5d4a0ead6ad6c29b833328d2b5396`  
		Last Modified: Thu, 16 Apr 2020 00:48:34 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3415fe8d1273fa9bd484bc97b45f1dc83defdc87330120c128494d264022d5b5`  
		Last Modified: Thu, 16 Apr 2020 00:48:34 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0-windowsservercore` - windows version 10.0.17763.1158; amd64

```console
$ docker pull mongo@sha256:ccd97bd444338973ac143a22753e6b73a3e707a6a3edd512311a418a3e432cdb
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2356541115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c9945d9fe9ca658fb0b08de9eac6736f7f9f6f6132782ad2f1a33419787310`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Wed, 15 Apr 2020 12:44:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 16 Apr 2020 00:33:51 GMT
ENV MONGO_VERSION=4.0.18
# Thu, 16 Apr 2020 00:33:52 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.18-signed.msi
# Thu, 16 Apr 2020 00:33:53 GMT
ENV MONGO_DOWNLOAD_SHA256=8f326aff375480941e48852314fbfd4e4e186de6556d753cf09b890ab9241ecf
# Thu, 16 Apr 2020 00:47:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 16 Apr 2020 00:47:20 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 16 Apr 2020 00:47:21 GMT
EXPOSE 27017
# Thu, 16 Apr 2020 00:47:23 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:442da5a04696895ce6580924a45188bbec9a9db9f81cb7dcef41fc1d4b119130`  
		Last Modified: Wed, 15 Apr 2020 15:29:13 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d06c5b7d240f934d1a803e7c0affb983bb556079edf76645f5ea89f3eb6ca0`  
		Last Modified: Thu, 16 Apr 2020 00:50:27 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1c8999ac54863eceb53a9253dd6ce7446db0ce0b49f75110116faea049b988`  
		Last Modified: Thu, 16 Apr 2020 00:50:27 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c62229a21e021c6afa0a2d47c9da44bed4152a29f163402db1c46226598c62`  
		Last Modified: Thu, 16 Apr 2020 00:50:24 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b6a77bfcdf682061579dbfd42fb85c94f50e2772f0492635662a42b568d11f`  
		Last Modified: Thu, 16 Apr 2020 00:50:58 GMT  
		Size: 85.8 MB (85825866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376560267143c527c9e648c8674aa8d68445b9af83e1c126daab2c89e4333d12`  
		Last Modified: Thu, 16 Apr 2020 00:50:24 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be795de606456ac97d7b3b1bb6f04c78dc3623e093cc10f27ee1c445974c76bb`  
		Last Modified: Thu, 16 Apr 2020 00:50:24 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c07d006bdcb6ede32d05a301be6b76d939a6d859a5149d7d7d766627e66a218`  
		Last Modified: Thu, 16 Apr 2020 00:50:24 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.0-windowsservercore-1809`

```console
$ docker pull mongo@sha256:a9b083f53dd089dd440cf5ed74930321789f2aa0dd617106f147df77fedcf731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1158; amd64

### `mongo:4.0-windowsservercore-1809` - windows version 10.0.17763.1158; amd64

```console
$ docker pull mongo@sha256:ccd97bd444338973ac143a22753e6b73a3e707a6a3edd512311a418a3e432cdb
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2356541115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c9945d9fe9ca658fb0b08de9eac6736f7f9f6f6132782ad2f1a33419787310`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Wed, 15 Apr 2020 12:44:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 16 Apr 2020 00:33:51 GMT
ENV MONGO_VERSION=4.0.18
# Thu, 16 Apr 2020 00:33:52 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.18-signed.msi
# Thu, 16 Apr 2020 00:33:53 GMT
ENV MONGO_DOWNLOAD_SHA256=8f326aff375480941e48852314fbfd4e4e186de6556d753cf09b890ab9241ecf
# Thu, 16 Apr 2020 00:47:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 16 Apr 2020 00:47:20 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 16 Apr 2020 00:47:21 GMT
EXPOSE 27017
# Thu, 16 Apr 2020 00:47:23 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:442da5a04696895ce6580924a45188bbec9a9db9f81cb7dcef41fc1d4b119130`  
		Last Modified: Wed, 15 Apr 2020 15:29:13 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d06c5b7d240f934d1a803e7c0affb983bb556079edf76645f5ea89f3eb6ca0`  
		Last Modified: Thu, 16 Apr 2020 00:50:27 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1c8999ac54863eceb53a9253dd6ce7446db0ce0b49f75110116faea049b988`  
		Last Modified: Thu, 16 Apr 2020 00:50:27 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c62229a21e021c6afa0a2d47c9da44bed4152a29f163402db1c46226598c62`  
		Last Modified: Thu, 16 Apr 2020 00:50:24 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b6a77bfcdf682061579dbfd42fb85c94f50e2772f0492635662a42b568d11f`  
		Last Modified: Thu, 16 Apr 2020 00:50:58 GMT  
		Size: 85.8 MB (85825866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376560267143c527c9e648c8674aa8d68445b9af83e1c126daab2c89e4333d12`  
		Last Modified: Thu, 16 Apr 2020 00:50:24 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be795de606456ac97d7b3b1bb6f04c78dc3623e093cc10f27ee1c445974c76bb`  
		Last Modified: Thu, 16 Apr 2020 00:50:24 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c07d006bdcb6ede32d05a301be6b76d939a6d859a5149d7d7d766627e66a218`  
		Last Modified: Thu, 16 Apr 2020 00:50:24 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.0-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:a869c2a880cc57c5c93e56a9dc5ea6950b4d905471b65ecacd94c8107e225470
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3630; amd64

### `mongo:4.0-windowsservercore-ltsc2016` - windows version 10.0.14393.3630; amd64

```console
$ docker pull mongo@sha256:b6e7d94f10b514a0034e43613a7231c9205b851edcd434a220366754980e3d16
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6174608935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9204ac12d78304d62efc38d691baec06bb99ffd71ef6b6c0c7dfb33bd48abd04`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Apr 2020 17:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Apr 2020 12:52:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 16 Apr 2020 00:15:31 GMT
ENV MONGO_VERSION=4.0.18
# Thu, 16 Apr 2020 00:15:32 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.18-signed.msi
# Thu, 16 Apr 2020 00:15:33 GMT
ENV MONGO_DOWNLOAD_SHA256=8f326aff375480941e48852314fbfd4e4e186de6556d753cf09b890ab9241ecf
# Thu, 16 Apr 2020 00:33:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 16 Apr 2020 00:33:42 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 16 Apr 2020 00:33:44 GMT
EXPOSE 27017
# Thu, 16 Apr 2020 00:33:45 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d0099407ec8ccaf0472e55152e38b262bdf0b2cf8dfd2e8afcc89d728ba3f5a0`  
		Size: 1.7 GB (1658081673 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5171ed01a0687a59b2bdf59e2df29a8932abe0ee22a4a6ff6368f8a8295a97d1`  
		Last Modified: Wed, 15 Apr 2020 15:29:42 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a6cd4c1ece17777a2c32dd239a8ba395e23c44f29e0233e281af26c9d2857d`  
		Last Modified: Thu, 16 Apr 2020 00:48:37 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf8b4dd88b18a52ca34aea2c9d21fc28a99db5737a9abd526f97ea9af1f38b2`  
		Last Modified: Thu, 16 Apr 2020 00:48:37 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd28aa952c4558acafcc059815a66472bb0f5eb7ef0cd1d0f851b3354301b140`  
		Last Modified: Thu, 16 Apr 2020 00:48:34 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad3765d0be3c9c109c970bfd4e310c53d3d2d8b1006b87ec93fd9240c577fa2`  
		Last Modified: Thu, 16 Apr 2020 00:50:01 GMT  
		Size: 446.5 MB (446533412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df155fc8098cf06f4508cb44bde84bfe1d4fb867ade29aa374cd0861de8161e4`  
		Last Modified: Thu, 16 Apr 2020 00:48:34 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bad101aceee320e60f5dd9bba9839a069ef5d4a0ead6ad6c29b833328d2b5396`  
		Last Modified: Thu, 16 Apr 2020 00:48:34 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3415fe8d1273fa9bd484bc97b45f1dc83defdc87330120c128494d264022d5b5`  
		Last Modified: Thu, 16 Apr 2020 00:48:34 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.0-xenial`

```console
$ docker pull mongo@sha256:88627ec198bd62e7a5e7f1fa2e7f130a8e161b0bdb392f3076c654d6ddb289a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:4.0-xenial` - linux; amd64

```console
$ docker pull mongo@sha256:5ff4514ff351575aa37842896ea330dc14ea026f0baabddc7d7988eeda72bd3d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.7 MB (153661651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d82b5301d74ec719432a0521d65e6a7e4ff4e5e54a4acc789cb4e895e9f16c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 21 Feb 2020 22:22:27 GMT
ADD file:1f70668251e2e58cee0ff0c22ee805f8a269ac6f8934c07f7e89dca6cc1de3aa in / 
# Fri, 21 Feb 2020 22:22:27 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:22:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:22:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:22:30 GMT
CMD ["/bin/bash"]
# Sat, 22 Feb 2020 01:08:16 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Sat, 22 Feb 2020 01:08:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 16:52:33 GMT
ENV GOSU_VERSION=1.12
# Fri, 17 Apr 2020 16:52:33 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 17 Apr 2020 16:53:00 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 17 Apr 2020 16:53:00 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 17 Apr 2020 16:53:28 GMT
ENV GPG_KEYS=9DA31620334BD75D9DCB49F368818C72E52529D4
# Fri, 17 Apr 2020 16:53:29 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 17 Apr 2020 16:53:29 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 17 Apr 2020 16:53:29 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 17 Apr 2020 16:53:29 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 17 Apr 2020 16:53:29 GMT
ENV MONGO_MAJOR=4.0
# Fri, 17 Apr 2020 16:53:30 GMT
ENV MONGO_VERSION=4.0.18
# Fri, 17 Apr 2020 16:53:30 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 17 Apr 2020 16:53:47 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 17 Apr 2020 16:53:48 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 17 Apr 2020 16:53:48 GMT
VOLUME [/data/db /data/configdb]
# Fri, 17 Apr 2020 16:53:48 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 17 Apr 2020 16:53:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2020 16:53:49 GMT
EXPOSE 27017
# Fri, 17 Apr 2020 16:53:49 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:fe703b657a32e0046dce0ad2cb17172cbec8ba302edf370f5f28962bdb6216a9`  
		Last Modified: Thu, 13 Feb 2020 00:25:54 GMT  
		Size: 44.2 MB (44191726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9df1fafd224fae3ba34a68dfc401f75bf6bc0c016fe36c61661ca5c7ad729ee`  
		Last Modified: Fri, 21 Feb 2020 22:23:12 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a645a4b887f9613f80fae43432e46423f196a9952d11bb620bef2add7c4ed4ee`  
		Last Modified: Fri, 21 Feb 2020 22:23:12 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57db7fe0b522b7a6069e769606e5ed0913a64e1e0d0030382a922ccf9449211e`  
		Last Modified: Fri, 21 Feb 2020 22:23:13 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f659f7c5a8a29b7c2592bc12a6afb9babe94617501a765bab59df899dfa98ac`  
		Last Modified: Sat, 22 Feb 2020 01:11:01 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b7ff548bb868b716a6e1ffbc5281d3f298fa1f2d6bac7843ef09901a0ee5c0`  
		Last Modified: Sat, 22 Feb 2020 01:11:02 GMT  
		Size: 2.9 MB (2946077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67a4fc8b9ac596e924ec523f4f913cec4c02bf316c82fab3b22c51e25d54d638`  
		Last Modified: Fri, 17 Apr 2020 16:54:56 GMT  
		Size: 1.3 MB (1305292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2afe62084c30f7e3e50835c0b6462b1f995eb96ec333987aaf1d2ee4db6157`  
		Last Modified: Fri, 17 Apr 2020 16:54:55 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:665eda6efe5a2ca89da71b3ec6c8008d061966135b267f56d91cb89160a709aa`  
		Last Modified: Fri, 17 Apr 2020 16:55:24 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f249afb8789ebd2cd3fa3191b4cf216f2762efa63a931238da6e4d0f8be691`  
		Last Modified: Fri, 17 Apr 2020 16:55:23 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9817b982630eb9b50d91d1fb8d3421347d0e3689ced1362228a59220a12883`  
		Last Modified: Fri, 17 Apr 2020 16:55:43 GMT  
		Size: 105.2 MB (105209155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d52bfe96ec699c4207b7a1cbbabb525e7d2c0522c43715f911f89427ffc17e48`  
		Last Modified: Fri, 17 Apr 2020 16:55:24 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f87759b290cbd65a430b16abe35549620c225a0644191b793a7cab038c4e25a`  
		Last Modified: Fri, 17 Apr 2020 16:55:24 GMT  
		Size: 4.0 KB (3954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0-xenial` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:2f2453d105ecfe52f2978b8461d4a4a6a756a329eae7adf18f08e6a6fb294fdb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.3 MB (143329420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0f9f050c13891b73d379f80d79a2a59c001147bc100c01f46470510c75a191d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 24 Apr 2020 00:20:42 GMT
ADD file:24038b6c5a9bab991785fab56202fc43de85e0749e57fcfc361de8aeff302309 in / 
# Fri, 24 Apr 2020 00:20:48 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 00:20:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Apr 2020 00:20:56 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Apr 2020 00:20:58 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 16:16:27 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Apr 2020 16:16:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 16:16:43 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 16:16:43 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Apr 2020 16:17:08 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 16:17:10 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 16:17:59 GMT
ENV GPG_KEYS=9DA31620334BD75D9DCB49F368818C72E52529D4
# Fri, 24 Apr 2020 16:18:00 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 16:18:01 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Apr 2020 16:18:02 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 16:18:02 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 16:18:03 GMT
ENV MONGO_MAJOR=4.0
# Fri, 24 Apr 2020 16:18:04 GMT
ENV MONGO_VERSION=4.0.18
# Fri, 24 Apr 2020 16:18:05 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Apr 2020 16:18:31 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Apr 2020 16:18:34 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Apr 2020 16:18:34 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Apr 2020 16:18:35 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Apr 2020 16:18:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 16:18:36 GMT
EXPOSE 27017
# Fri, 24 Apr 2020 16:18:37 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:ca96533948cdaf1fc84922a44248fcf915a3f526b46555bb96090bed658b00d7`  
		Last Modified: Mon, 30 Mar 2020 15:49:17 GMT  
		Size: 40.0 MB (39968791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c72780e1c95403020a1883a1054d9d48b7a5ad2d940ba2d57ae211369a19685`  
		Last Modified: Fri, 24 Apr 2020 00:22:16 GMT  
		Size: 472.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d962f0171bca79269769ac242507e3f65f2dcbb86de35ecaf164d37b8a89c9d`  
		Last Modified: Fri, 24 Apr 2020 00:22:16 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179f057dc5a95fd6368cf61fa48d9e2d85af21b750813b8dd17b7ad44752c342`  
		Last Modified: Fri, 24 Apr 2020 00:22:17 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0a8e99e85782df175a29b1bde536a79db756966637facaf915cc8e16f38691`  
		Last Modified: Fri, 24 Apr 2020 16:20:35 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a46d993ee733e416b83e56bc49a2736148b105b73cc7553c80fc2aaa7df313b1`  
		Last Modified: Fri, 24 Apr 2020 16:20:35 GMT  
		Size: 2.5 MB (2475001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b49e909411104c2ebb353f5cd8c52434864e5d144971b58f81c3780a4cd037`  
		Last Modified: Fri, 24 Apr 2020 16:20:35 GMT  
		Size: 1.2 MB (1232274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd9944fff526a6c05418546fe52dfcdcf7b391b22af046c09426b603f2e7154`  
		Last Modified: Fri, 24 Apr 2020 16:20:35 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c9cfbc7523eafd818f49310c0660145f99ef417b5e33fc14dde1a4e9c691e89`  
		Last Modified: Fri, 24 Apr 2020 16:21:09 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176c609d312b2670f8da9e72294f1c225dafe5c5bacf1d01b76370affcf3a0ad`  
		Last Modified: Fri, 24 Apr 2020 16:21:09 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ebf85bcab66a237a422958c4176d323878d5a01f16373925994a14b03decbc`  
		Last Modified: Fri, 24 Apr 2020 16:21:34 GMT  
		Size: 99.6 MB (99643925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8e46255fbd40183c4b284dbe92b867b802541e61f0457464eb134faae1f4e8`  
		Last Modified: Fri, 24 Apr 2020 16:21:09 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc8fcc8a0a1a416a06738f37c1af475d21581ce7f1d91a46f67b033ca21ea39`  
		Last Modified: Fri, 24 Apr 2020 16:21:09 GMT  
		Size: 4.0 KB (3956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.2`

```console
$ docker pull mongo@sha256:7663173f07cf97589989d0c9e15015737cf328618cc4d466fc6c9eddd838ac72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x
	-	windows version 10.0.14393.3630; amd64
	-	windows version 10.0.17763.1158; amd64

### `mongo:4.2` - linux; amd64

```console
$ docker pull mongo@sha256:18f7e39575cd12e9177017ddaa4bcb6c3bae1f6468f3922dc1ecd0662e10281c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164652772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e9495ea1bc639197bc40aef2beedf931078003d8933fb38240f3a1a63c90119`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 20 Mar 2020 19:20:20 GMT
ADD file:594fa35cf803361e69d817fc867b6a4069c064ffd20ed50caf42ad9bb11ca999 in / 
# Fri, 20 Mar 2020 19:20:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 20 Mar 2020 19:20:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 20 Mar 2020 19:20:22 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 20 Mar 2020 19:20:22 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2020 20:49:50 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 20 Mar 2020 20:49:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 16:53:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 17 Apr 2020 16:53:54 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 17 Apr 2020 16:54:10 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 17 Apr 2020 16:54:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 17 Apr 2020 16:54:11 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 17 Apr 2020 16:54:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 17 Apr 2020 16:54:12 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 17 Apr 2020 16:54:13 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 17 Apr 2020 16:54:13 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 17 Apr 2020 16:54:13 GMT
ENV MONGO_MAJOR=4.2
# Mon, 20 Apr 2020 17:44:11 GMT
ENV MONGO_VERSION=4.2.6
# Mon, 20 Apr 2020 17:44:12 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Mon, 20 Apr 2020 17:44:40 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Mon, 20 Apr 2020 17:44:41 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Mon, 20 Apr 2020 17:44:41 GMT
VOLUME [/data/db /data/configdb]
# Mon, 20 Apr 2020 17:44:41 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Mon, 20 Apr 2020 17:44:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2020 17:44:42 GMT
EXPOSE 27017
# Mon, 20 Apr 2020 17:44:42 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:5bed26d33875e6da1d9ff9a1054c5fef3bbeb22ee979e14b72acf72528de007b`  
		Last Modified: Thu, 12 Mar 2020 13:21:29 GMT  
		Size: 26.7 MB (26690587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f11b29a9c7306674a9479158c1b4259938af11b97359d9ac02030cc1095e9ed1`  
		Last Modified: Fri, 20 Mar 2020 19:21:18 GMT  
		Size: 35.4 KB (35372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:930bda195c84cf132344bf38edcad255317382f910503fef234a9ce3bff0f4dd`  
		Last Modified: Fri, 20 Mar 2020 19:21:18 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78bf9a5ad49e4ae42a83f4995ade4efc096f78fd38299cf05bc041e8cdda2a36`  
		Last Modified: Fri, 20 Mar 2020 19:21:18 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7fb3809884c8771103b4475a778eb0a14b736d5f2008d7ef534950c9b6b77d`  
		Last Modified: Fri, 20 Mar 2020 20:50:51 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7237292ff8a2ff64ff0898dc8792b23e5abe90bf32d14f0d4d9eb6ab9e956dd`  
		Last Modified: Fri, 20 Mar 2020 20:50:50 GMT  
		Size: 3.0 MB (2982755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cdf1eb96f71308e6f5be52c3f5278ff6de496b971e1a94d6adb60fc52b2835f`  
		Last Modified: Fri, 17 Apr 2020 16:55:51 GMT  
		Size: 5.8 MB (5824593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39c254c62945d89e0d0e07c721ca9da0ee5848ace6fd9ce95f719a6b721c2be`  
		Last Modified: Fri, 17 Apr 2020 16:55:49 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:110f77aab367a0f38f766fa5d307186a68fdd7483177e20a62c2eee431fb244d`  
		Last Modified: Fri, 17 Apr 2020 16:55:48 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6bec5ffc4eadbe0fa6b84373fe7eaed47c67d2a505a1c640f7cc79c84b5278`  
		Last Modified: Mon, 20 Apr 2020 17:45:00 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d994803edb5bbd3b979490f3ccbe46fc0977dc6fb469fab88fccc9115d0675`  
		Last Modified: Mon, 20 Apr 2020 17:45:27 GMT  
		Size: 129.1 MB (129110699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4266b1dcdabb8fe88172e362ae653d5564293bcd065b45dba2a8e765b4902ab9`  
		Last Modified: Mon, 20 Apr 2020 17:45:00 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3143b095bd39dff0535f074d233459b67c33b68bf2bd7f6d69220bae208a8cac`  
		Last Modified: Mon, 20 Apr 2020 17:45:00 GMT  
		Size: 4.0 KB (3952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:25821e16c7c401986caa09fba3be08b103203a1599edaba8cd34366903b4b3e6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154693716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c06ecd9c0f139339bf92dbef6e630dca8acc4265b72752f7d7b37e16786ed8d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

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
# Fri, 24 Apr 2020 16:18:50 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Apr 2020 16:19:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 16:19:09 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 16:19:09 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Apr 2020 16:19:31 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 16:19:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 16:19:33 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 24 Apr 2020 16:19:35 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 16:19:36 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Apr 2020 16:19:37 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 16:19:37 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 16:19:38 GMT
ENV MONGO_MAJOR=4.2
# Fri, 24 Apr 2020 16:19:38 GMT
ENV MONGO_VERSION=4.2.6
# Fri, 24 Apr 2020 16:19:40 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Apr 2020 16:20:06 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Apr 2020 16:20:09 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Apr 2020 16:20:10 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Apr 2020 16:20:10 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Apr 2020 16:20:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 16:20:11 GMT
EXPOSE 27017
# Fri, 24 Apr 2020 16:20:12 GMT
CMD ["mongod"]
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
	-	`sha256:d1a8d1af89634c78002ec70ef345dd88801eff1bbca938f85fc7472acf873b32`  
		Last Modified: Fri, 24 Apr 2020 16:21:43 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c03832d333b77fecdaaf76768c24a0c6797373a576bd7fb9abc41f3e3e5e2e4`  
		Last Modified: Fri, 24 Apr 2020 16:21:43 GMT  
		Size: 2.7 MB (2675928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544b6736a2d19b775007ab26e1c72ee2e84911c375eec60ec697fe5e8deca69f`  
		Last Modified: Fri, 24 Apr 2020 16:21:44 GMT  
		Size: 5.3 MB (5345352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920aac5b0c675d956885986db6ac84f954ff2f6a98df26a133ae89ae619cd5be`  
		Last Modified: Fri, 24 Apr 2020 16:21:42 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d53bf51618735c85e240ace69cf43a38a4077593fb9b4633fc1d85d2e655016`  
		Last Modified: Fri, 24 Apr 2020 16:21:41 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5296ff1757ed119711f3cc049cb72f1f77178850e6ba2efc6cb0d1e9e1687bdf`  
		Last Modified: Fri, 24 Apr 2020 16:21:41 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7697b84404da018afccd718c3454ed04a6ee05110f0d573a5d73e25a5c5cd75c`  
		Last Modified: Fri, 24 Apr 2020 16:22:09 GMT  
		Size: 122.9 MB (122907968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458af224982cf3028e9a2a89e362caa3e795382c0448adc60b4ab96bedbcc1ef`  
		Last Modified: Fri, 24 Apr 2020 16:21:41 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7506dcffce0af812ecd82776f582f438856fd75e7f948fa2a689a841eaf272e0`  
		Last Modified: Fri, 24 Apr 2020 16:21:41 GMT  
		Size: 4.0 KB (3955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2` - linux; s390x

```console
$ docker pull mongo@sha256:9a853858232155d691db93ab8ab614ad4636f9465aaab10dad522c6ffdbb6fd5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160626574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb6080841c0f9e130ab30d755a2610d8101b8b45a55cfbce1852edce8e90e15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 23 Apr 2020 17:52:20 GMT
ADD file:ea66ef2a01c547f771866bfa221969f8a30489c28d2a81be8dde7f40e73da33b in / 
# Thu, 23 Apr 2020 17:52:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 17:52:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 17:52:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 17:52:31 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 07:34:44 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Apr 2020 07:34:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 07:34:51 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 07:34:51 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Apr 2020 07:35:02 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 07:35:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 07:35:03 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 24 Apr 2020 07:35:09 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 07:35:10 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Apr 2020 07:35:10 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 07:35:10 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 07:35:11 GMT
ENV MONGO_MAJOR=4.2
# Fri, 24 Apr 2020 07:35:11 GMT
ENV MONGO_VERSION=4.2.6
# Fri, 24 Apr 2020 07:35:12 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Apr 2020 07:35:33 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Apr 2020 07:35:38 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Apr 2020 07:35:38 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Apr 2020 07:35:38 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Apr 2020 07:35:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 07:35:39 GMT
EXPOSE 27017
# Fri, 24 Apr 2020 07:35:39 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:13b4c2e4bb97a2a80bb0e557eeba41e4adea0f5e18352e359bca3f847193899c`  
		Last Modified: Mon, 06 Apr 2020 15:41:16 GMT  
		Size: 25.4 MB (25365338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:471a80e39fb485b86610de915eaaad3d867cc97e460b6da3bb656e03520e8a63`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 36.2 KB (36171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb0c128ddabc6a980ec71426ade04fc9bba2e1afcdc243e2d09c316b635f814`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678052ac148ee123df2f0773eb3a0f5f90490ada8b9a5705363b18a2f45fbe88`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c464d6728e9ac439c8d2dc10a88d64a54c34ac50926c66cb7b6d12e37b15d6`  
		Last Modified: Fri, 24 Apr 2020 07:36:04 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd364a38efacff4956ad8e4082d7fa9593aa0a036757fdfbe97487eb26ea2c9`  
		Last Modified: Fri, 24 Apr 2020 07:36:03 GMT  
		Size: 2.7 MB (2714610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e788a62ef53016c8add2417fa25e2141e1b7293acd648f26ed2ddffd54e605b`  
		Last Modified: Fri, 24 Apr 2020 07:36:02 GMT  
		Size: 5.7 MB (5744825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e103dac172d8152c577b2075cc90e6b674188775064cccfbbbc84d93979b3e56`  
		Last Modified: Fri, 24 Apr 2020 07:36:00 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:259fb52c1ef634a5a074adebdaa3f4fc95e636e570c5719c5d662babed85392e`  
		Last Modified: Fri, 24 Apr 2020 07:35:59 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f95c28bb62ddcdbb79cc6870d5cd9701c912a6307bde4c657e1d0c619430fab`  
		Last Modified: Fri, 24 Apr 2020 07:35:58 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05cea8c1238e8ec47654f290d7a566d006d9302762e741316cd236b909d4577d`  
		Last Modified: Fri, 24 Apr 2020 07:36:18 GMT  
		Size: 126.8 MB (126756767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a873535c8ae6f6827fe3d880ab25b1cc404dc3b74898d2ca9bff17136b83caba`  
		Last Modified: Fri, 24 Apr 2020 07:36:04 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d64c0289b5d5c3ee9e04955ed738543e81fdae4e1a43328fd4d88be18d402b`  
		Last Modified: Fri, 24 Apr 2020 07:36:30 GMT  
		Size: 4.0 KB (3954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2` - windows version 10.0.14393.3630; amd64

```console
$ docker pull mongo@sha256:dd6d940f7a8469cd7ff4d01cf767e861e05ea91c4e01707ea74ed2b633b56f20
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6184565858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fe805e4e3cf7852986e9f6716f85f270946e78bb6585812cc72368454753b47`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Apr 2020 17:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Apr 2020 12:52:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 20 Apr 2020 18:34:28 GMT
ENV MONGO_VERSION=4.2.6
# Mon, 20 Apr 2020 18:34:29 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.6-signed.msi
# Mon, 20 Apr 2020 18:34:30 GMT
ENV MONGO_DOWNLOAD_SHA256=401ebc0c087058cd98194046bbd4fbee243592cf9397f36a1fafa208de4ac21e
# Mon, 20 Apr 2020 18:52:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 20 Apr 2020 18:52:25 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 20 Apr 2020 18:52:26 GMT
EXPOSE 27017
# Mon, 20 Apr 2020 18:52:27 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d0099407ec8ccaf0472e55152e38b262bdf0b2cf8dfd2e8afcc89d728ba3f5a0`  
		Size: 1.7 GB (1658081673 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5171ed01a0687a59b2bdf59e2df29a8932abe0ee22a4a6ff6368f8a8295a97d1`  
		Last Modified: Wed, 15 Apr 2020 15:29:42 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a316c4dbc306f67b8ac735d957f87c1afbef1afde59d7b13febb4777781f6eb`  
		Last Modified: Mon, 20 Apr 2020 19:17:03 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e05862ade99bc32c017752427f4eb4ac19437b38181c6900cfed1d6a99d6510`  
		Last Modified: Mon, 20 Apr 2020 19:17:02 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7bdc8ea0d500490783e39f9355fa0349a2d9c32cd29ac8cbdd9a06e848cccda`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f30ae2c8c647fe5e41e956e8cb45d970e0761b0d144aa2a1a1c991f5627caa78`  
		Last Modified: Mon, 20 Apr 2020 19:18:45 GMT  
		Size: 456.5 MB (456490346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2069620de21f9e09ee89665e7488732e9804b4ebabb671846dcc5a2efad828f`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9793d6d47e628c898abbf674bad2cd450299481e89b30f575aac87fc2d186496`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b962b3b43034bdc9d37b9b1a386a2abcdb5b6c8a648d35aa3b46bd884a3c439`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2` - windows version 10.0.17763.1158; amd64

```console
$ docker pull mongo@sha256:98dc02185399f9a980eeac228255f8e42451f535d99c12f71015f176dacbce2f
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2726301729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98407fec53691f82e5cd2eb3a2bda7d93127266f2f6a5f4b7fc5d15a33987224`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Wed, 15 Apr 2020 12:44:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 20 Apr 2020 18:52:33 GMT
ENV MONGO_VERSION=4.2.6
# Mon, 20 Apr 2020 18:52:34 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.6-signed.msi
# Mon, 20 Apr 2020 18:52:35 GMT
ENV MONGO_DOWNLOAD_SHA256=401ebc0c087058cd98194046bbd4fbee243592cf9397f36a1fafa208de4ac21e
# Mon, 20 Apr 2020 19:16:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 20 Apr 2020 19:16:07 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 20 Apr 2020 19:16:08 GMT
EXPOSE 27017
# Mon, 20 Apr 2020 19:16:10 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:442da5a04696895ce6580924a45188bbec9a9db9f81cb7dcef41fc1d4b119130`  
		Last Modified: Wed, 15 Apr 2020 15:29:13 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd1d4721643d80e780c8f74ccda6db920cd5d6702e3a02cecc0a28dc3df2b90`  
		Last Modified: Mon, 20 Apr 2020 19:19:18 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f67966d3a477caf485aaf4080d27615f90dfeed53dd3ba0fd149e65a6b97531`  
		Last Modified: Mon, 20 Apr 2020 19:19:18 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3f18459245d1b377a5dd3fc17087c4c9f225ae47f7e5293f1bd6fca26b0879`  
		Last Modified: Mon, 20 Apr 2020 19:19:15 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff28a577006caf2972aa81e377a6ddbc80a4f337df7c3fc877bc22c875d70b30`  
		Last Modified: Mon, 20 Apr 2020 19:20:11 GMT  
		Size: 455.6 MB (455586654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88cd1efbb2ca082ab8c0e84173075d04be6d252eea7a7f18d961f40e12ac4a0`  
		Last Modified: Mon, 20 Apr 2020 19:19:15 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1eb8768e3e39daa6fe8c5e1c37f5928b6bf0a79e6f13ec87956b42d9e01756d`  
		Last Modified: Mon, 20 Apr 2020 19:19:16 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdc5f1e7a5e65ad06c77f10ba2410b9c07f078d86c597960e5760ad0e398a9d2`  
		Last Modified: Mon, 20 Apr 2020 19:19:15 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.2.6`

```console
$ docker pull mongo@sha256:7663173f07cf97589989d0c9e15015737cf328618cc4d466fc6c9eddd838ac72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x
	-	windows version 10.0.14393.3630; amd64
	-	windows version 10.0.17763.1158; amd64

### `mongo:4.2.6` - linux; amd64

```console
$ docker pull mongo@sha256:18f7e39575cd12e9177017ddaa4bcb6c3bae1f6468f3922dc1ecd0662e10281c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164652772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e9495ea1bc639197bc40aef2beedf931078003d8933fb38240f3a1a63c90119`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 20 Mar 2020 19:20:20 GMT
ADD file:594fa35cf803361e69d817fc867b6a4069c064ffd20ed50caf42ad9bb11ca999 in / 
# Fri, 20 Mar 2020 19:20:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 20 Mar 2020 19:20:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 20 Mar 2020 19:20:22 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 20 Mar 2020 19:20:22 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2020 20:49:50 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 20 Mar 2020 20:49:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 16:53:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 17 Apr 2020 16:53:54 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 17 Apr 2020 16:54:10 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 17 Apr 2020 16:54:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 17 Apr 2020 16:54:11 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 17 Apr 2020 16:54:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 17 Apr 2020 16:54:12 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 17 Apr 2020 16:54:13 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 17 Apr 2020 16:54:13 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 17 Apr 2020 16:54:13 GMT
ENV MONGO_MAJOR=4.2
# Mon, 20 Apr 2020 17:44:11 GMT
ENV MONGO_VERSION=4.2.6
# Mon, 20 Apr 2020 17:44:12 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Mon, 20 Apr 2020 17:44:40 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Mon, 20 Apr 2020 17:44:41 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Mon, 20 Apr 2020 17:44:41 GMT
VOLUME [/data/db /data/configdb]
# Mon, 20 Apr 2020 17:44:41 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Mon, 20 Apr 2020 17:44:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2020 17:44:42 GMT
EXPOSE 27017
# Mon, 20 Apr 2020 17:44:42 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:5bed26d33875e6da1d9ff9a1054c5fef3bbeb22ee979e14b72acf72528de007b`  
		Last Modified: Thu, 12 Mar 2020 13:21:29 GMT  
		Size: 26.7 MB (26690587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f11b29a9c7306674a9479158c1b4259938af11b97359d9ac02030cc1095e9ed1`  
		Last Modified: Fri, 20 Mar 2020 19:21:18 GMT  
		Size: 35.4 KB (35372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:930bda195c84cf132344bf38edcad255317382f910503fef234a9ce3bff0f4dd`  
		Last Modified: Fri, 20 Mar 2020 19:21:18 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78bf9a5ad49e4ae42a83f4995ade4efc096f78fd38299cf05bc041e8cdda2a36`  
		Last Modified: Fri, 20 Mar 2020 19:21:18 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7fb3809884c8771103b4475a778eb0a14b736d5f2008d7ef534950c9b6b77d`  
		Last Modified: Fri, 20 Mar 2020 20:50:51 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7237292ff8a2ff64ff0898dc8792b23e5abe90bf32d14f0d4d9eb6ab9e956dd`  
		Last Modified: Fri, 20 Mar 2020 20:50:50 GMT  
		Size: 3.0 MB (2982755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cdf1eb96f71308e6f5be52c3f5278ff6de496b971e1a94d6adb60fc52b2835f`  
		Last Modified: Fri, 17 Apr 2020 16:55:51 GMT  
		Size: 5.8 MB (5824593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39c254c62945d89e0d0e07c721ca9da0ee5848ace6fd9ce95f719a6b721c2be`  
		Last Modified: Fri, 17 Apr 2020 16:55:49 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:110f77aab367a0f38f766fa5d307186a68fdd7483177e20a62c2eee431fb244d`  
		Last Modified: Fri, 17 Apr 2020 16:55:48 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6bec5ffc4eadbe0fa6b84373fe7eaed47c67d2a505a1c640f7cc79c84b5278`  
		Last Modified: Mon, 20 Apr 2020 17:45:00 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d994803edb5bbd3b979490f3ccbe46fc0977dc6fb469fab88fccc9115d0675`  
		Last Modified: Mon, 20 Apr 2020 17:45:27 GMT  
		Size: 129.1 MB (129110699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4266b1dcdabb8fe88172e362ae653d5564293bcd065b45dba2a8e765b4902ab9`  
		Last Modified: Mon, 20 Apr 2020 17:45:00 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3143b095bd39dff0535f074d233459b67c33b68bf2bd7f6d69220bae208a8cac`  
		Last Modified: Mon, 20 Apr 2020 17:45:00 GMT  
		Size: 4.0 KB (3952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2.6` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:25821e16c7c401986caa09fba3be08b103203a1599edaba8cd34366903b4b3e6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154693716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c06ecd9c0f139339bf92dbef6e630dca8acc4265b72752f7d7b37e16786ed8d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

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
# Fri, 24 Apr 2020 16:18:50 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Apr 2020 16:19:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 16:19:09 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 16:19:09 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Apr 2020 16:19:31 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 16:19:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 16:19:33 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 24 Apr 2020 16:19:35 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 16:19:36 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Apr 2020 16:19:37 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 16:19:37 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 16:19:38 GMT
ENV MONGO_MAJOR=4.2
# Fri, 24 Apr 2020 16:19:38 GMT
ENV MONGO_VERSION=4.2.6
# Fri, 24 Apr 2020 16:19:40 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Apr 2020 16:20:06 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Apr 2020 16:20:09 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Apr 2020 16:20:10 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Apr 2020 16:20:10 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Apr 2020 16:20:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 16:20:11 GMT
EXPOSE 27017
# Fri, 24 Apr 2020 16:20:12 GMT
CMD ["mongod"]
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
	-	`sha256:d1a8d1af89634c78002ec70ef345dd88801eff1bbca938f85fc7472acf873b32`  
		Last Modified: Fri, 24 Apr 2020 16:21:43 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c03832d333b77fecdaaf76768c24a0c6797373a576bd7fb9abc41f3e3e5e2e4`  
		Last Modified: Fri, 24 Apr 2020 16:21:43 GMT  
		Size: 2.7 MB (2675928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544b6736a2d19b775007ab26e1c72ee2e84911c375eec60ec697fe5e8deca69f`  
		Last Modified: Fri, 24 Apr 2020 16:21:44 GMT  
		Size: 5.3 MB (5345352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920aac5b0c675d956885986db6ac84f954ff2f6a98df26a133ae89ae619cd5be`  
		Last Modified: Fri, 24 Apr 2020 16:21:42 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d53bf51618735c85e240ace69cf43a38a4077593fb9b4633fc1d85d2e655016`  
		Last Modified: Fri, 24 Apr 2020 16:21:41 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5296ff1757ed119711f3cc049cb72f1f77178850e6ba2efc6cb0d1e9e1687bdf`  
		Last Modified: Fri, 24 Apr 2020 16:21:41 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7697b84404da018afccd718c3454ed04a6ee05110f0d573a5d73e25a5c5cd75c`  
		Last Modified: Fri, 24 Apr 2020 16:22:09 GMT  
		Size: 122.9 MB (122907968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458af224982cf3028e9a2a89e362caa3e795382c0448adc60b4ab96bedbcc1ef`  
		Last Modified: Fri, 24 Apr 2020 16:21:41 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7506dcffce0af812ecd82776f582f438856fd75e7f948fa2a689a841eaf272e0`  
		Last Modified: Fri, 24 Apr 2020 16:21:41 GMT  
		Size: 4.0 KB (3955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2.6` - linux; s390x

```console
$ docker pull mongo@sha256:9a853858232155d691db93ab8ab614ad4636f9465aaab10dad522c6ffdbb6fd5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160626574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb6080841c0f9e130ab30d755a2610d8101b8b45a55cfbce1852edce8e90e15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 23 Apr 2020 17:52:20 GMT
ADD file:ea66ef2a01c547f771866bfa221969f8a30489c28d2a81be8dde7f40e73da33b in / 
# Thu, 23 Apr 2020 17:52:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 17:52:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 17:52:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 17:52:31 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 07:34:44 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Apr 2020 07:34:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 07:34:51 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 07:34:51 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Apr 2020 07:35:02 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 07:35:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 07:35:03 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 24 Apr 2020 07:35:09 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 07:35:10 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Apr 2020 07:35:10 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 07:35:10 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 07:35:11 GMT
ENV MONGO_MAJOR=4.2
# Fri, 24 Apr 2020 07:35:11 GMT
ENV MONGO_VERSION=4.2.6
# Fri, 24 Apr 2020 07:35:12 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Apr 2020 07:35:33 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Apr 2020 07:35:38 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Apr 2020 07:35:38 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Apr 2020 07:35:38 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Apr 2020 07:35:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 07:35:39 GMT
EXPOSE 27017
# Fri, 24 Apr 2020 07:35:39 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:13b4c2e4bb97a2a80bb0e557eeba41e4adea0f5e18352e359bca3f847193899c`  
		Last Modified: Mon, 06 Apr 2020 15:41:16 GMT  
		Size: 25.4 MB (25365338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:471a80e39fb485b86610de915eaaad3d867cc97e460b6da3bb656e03520e8a63`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 36.2 KB (36171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb0c128ddabc6a980ec71426ade04fc9bba2e1afcdc243e2d09c316b635f814`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678052ac148ee123df2f0773eb3a0f5f90490ada8b9a5705363b18a2f45fbe88`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c464d6728e9ac439c8d2dc10a88d64a54c34ac50926c66cb7b6d12e37b15d6`  
		Last Modified: Fri, 24 Apr 2020 07:36:04 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd364a38efacff4956ad8e4082d7fa9593aa0a036757fdfbe97487eb26ea2c9`  
		Last Modified: Fri, 24 Apr 2020 07:36:03 GMT  
		Size: 2.7 MB (2714610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e788a62ef53016c8add2417fa25e2141e1b7293acd648f26ed2ddffd54e605b`  
		Last Modified: Fri, 24 Apr 2020 07:36:02 GMT  
		Size: 5.7 MB (5744825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e103dac172d8152c577b2075cc90e6b674188775064cccfbbbc84d93979b3e56`  
		Last Modified: Fri, 24 Apr 2020 07:36:00 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:259fb52c1ef634a5a074adebdaa3f4fc95e636e570c5719c5d662babed85392e`  
		Last Modified: Fri, 24 Apr 2020 07:35:59 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f95c28bb62ddcdbb79cc6870d5cd9701c912a6307bde4c657e1d0c619430fab`  
		Last Modified: Fri, 24 Apr 2020 07:35:58 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05cea8c1238e8ec47654f290d7a566d006d9302762e741316cd236b909d4577d`  
		Last Modified: Fri, 24 Apr 2020 07:36:18 GMT  
		Size: 126.8 MB (126756767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a873535c8ae6f6827fe3d880ab25b1cc404dc3b74898d2ca9bff17136b83caba`  
		Last Modified: Fri, 24 Apr 2020 07:36:04 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d64c0289b5d5c3ee9e04955ed738543e81fdae4e1a43328fd4d88be18d402b`  
		Last Modified: Fri, 24 Apr 2020 07:36:30 GMT  
		Size: 4.0 KB (3954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2.6` - windows version 10.0.14393.3630; amd64

```console
$ docker pull mongo@sha256:dd6d940f7a8469cd7ff4d01cf767e861e05ea91c4e01707ea74ed2b633b56f20
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6184565858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fe805e4e3cf7852986e9f6716f85f270946e78bb6585812cc72368454753b47`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Apr 2020 17:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Apr 2020 12:52:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 20 Apr 2020 18:34:28 GMT
ENV MONGO_VERSION=4.2.6
# Mon, 20 Apr 2020 18:34:29 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.6-signed.msi
# Mon, 20 Apr 2020 18:34:30 GMT
ENV MONGO_DOWNLOAD_SHA256=401ebc0c087058cd98194046bbd4fbee243592cf9397f36a1fafa208de4ac21e
# Mon, 20 Apr 2020 18:52:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 20 Apr 2020 18:52:25 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 20 Apr 2020 18:52:26 GMT
EXPOSE 27017
# Mon, 20 Apr 2020 18:52:27 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d0099407ec8ccaf0472e55152e38b262bdf0b2cf8dfd2e8afcc89d728ba3f5a0`  
		Size: 1.7 GB (1658081673 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5171ed01a0687a59b2bdf59e2df29a8932abe0ee22a4a6ff6368f8a8295a97d1`  
		Last Modified: Wed, 15 Apr 2020 15:29:42 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a316c4dbc306f67b8ac735d957f87c1afbef1afde59d7b13febb4777781f6eb`  
		Last Modified: Mon, 20 Apr 2020 19:17:03 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e05862ade99bc32c017752427f4eb4ac19437b38181c6900cfed1d6a99d6510`  
		Last Modified: Mon, 20 Apr 2020 19:17:02 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7bdc8ea0d500490783e39f9355fa0349a2d9c32cd29ac8cbdd9a06e848cccda`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f30ae2c8c647fe5e41e956e8cb45d970e0761b0d144aa2a1a1c991f5627caa78`  
		Last Modified: Mon, 20 Apr 2020 19:18:45 GMT  
		Size: 456.5 MB (456490346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2069620de21f9e09ee89665e7488732e9804b4ebabb671846dcc5a2efad828f`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9793d6d47e628c898abbf674bad2cd450299481e89b30f575aac87fc2d186496`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b962b3b43034bdc9d37b9b1a386a2abcdb5b6c8a648d35aa3b46bd884a3c439`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2.6` - windows version 10.0.17763.1158; amd64

```console
$ docker pull mongo@sha256:98dc02185399f9a980eeac228255f8e42451f535d99c12f71015f176dacbce2f
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2726301729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98407fec53691f82e5cd2eb3a2bda7d93127266f2f6a5f4b7fc5d15a33987224`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Wed, 15 Apr 2020 12:44:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 20 Apr 2020 18:52:33 GMT
ENV MONGO_VERSION=4.2.6
# Mon, 20 Apr 2020 18:52:34 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.6-signed.msi
# Mon, 20 Apr 2020 18:52:35 GMT
ENV MONGO_DOWNLOAD_SHA256=401ebc0c087058cd98194046bbd4fbee243592cf9397f36a1fafa208de4ac21e
# Mon, 20 Apr 2020 19:16:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 20 Apr 2020 19:16:07 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 20 Apr 2020 19:16:08 GMT
EXPOSE 27017
# Mon, 20 Apr 2020 19:16:10 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:442da5a04696895ce6580924a45188bbec9a9db9f81cb7dcef41fc1d4b119130`  
		Last Modified: Wed, 15 Apr 2020 15:29:13 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd1d4721643d80e780c8f74ccda6db920cd5d6702e3a02cecc0a28dc3df2b90`  
		Last Modified: Mon, 20 Apr 2020 19:19:18 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f67966d3a477caf485aaf4080d27615f90dfeed53dd3ba0fd149e65a6b97531`  
		Last Modified: Mon, 20 Apr 2020 19:19:18 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3f18459245d1b377a5dd3fc17087c4c9f225ae47f7e5293f1bd6fca26b0879`  
		Last Modified: Mon, 20 Apr 2020 19:19:15 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff28a577006caf2972aa81e377a6ddbc80a4f337df7c3fc877bc22c875d70b30`  
		Last Modified: Mon, 20 Apr 2020 19:20:11 GMT  
		Size: 455.6 MB (455586654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88cd1efbb2ca082ab8c0e84173075d04be6d252eea7a7f18d961f40e12ac4a0`  
		Last Modified: Mon, 20 Apr 2020 19:19:15 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1eb8768e3e39daa6fe8c5e1c37f5928b6bf0a79e6f13ec87956b42d9e01756d`  
		Last Modified: Mon, 20 Apr 2020 19:19:16 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdc5f1e7a5e65ad06c77f10ba2410b9c07f078d86c597960e5760ad0e398a9d2`  
		Last Modified: Mon, 20 Apr 2020 19:19:15 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.2.6-bionic`

```console
$ docker pull mongo@sha256:e4abccb1677a976b66d2c726586fc40a073aa3ce4fc5ef6bbc18267e3394d19c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `mongo:4.2.6-bionic` - linux; amd64

```console
$ docker pull mongo@sha256:18f7e39575cd12e9177017ddaa4bcb6c3bae1f6468f3922dc1ecd0662e10281c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164652772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e9495ea1bc639197bc40aef2beedf931078003d8933fb38240f3a1a63c90119`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 20 Mar 2020 19:20:20 GMT
ADD file:594fa35cf803361e69d817fc867b6a4069c064ffd20ed50caf42ad9bb11ca999 in / 
# Fri, 20 Mar 2020 19:20:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 20 Mar 2020 19:20:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 20 Mar 2020 19:20:22 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 20 Mar 2020 19:20:22 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2020 20:49:50 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 20 Mar 2020 20:49:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 16:53:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 17 Apr 2020 16:53:54 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 17 Apr 2020 16:54:10 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 17 Apr 2020 16:54:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 17 Apr 2020 16:54:11 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 17 Apr 2020 16:54:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 17 Apr 2020 16:54:12 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 17 Apr 2020 16:54:13 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 17 Apr 2020 16:54:13 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 17 Apr 2020 16:54:13 GMT
ENV MONGO_MAJOR=4.2
# Mon, 20 Apr 2020 17:44:11 GMT
ENV MONGO_VERSION=4.2.6
# Mon, 20 Apr 2020 17:44:12 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Mon, 20 Apr 2020 17:44:40 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Mon, 20 Apr 2020 17:44:41 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Mon, 20 Apr 2020 17:44:41 GMT
VOLUME [/data/db /data/configdb]
# Mon, 20 Apr 2020 17:44:41 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Mon, 20 Apr 2020 17:44:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2020 17:44:42 GMT
EXPOSE 27017
# Mon, 20 Apr 2020 17:44:42 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:5bed26d33875e6da1d9ff9a1054c5fef3bbeb22ee979e14b72acf72528de007b`  
		Last Modified: Thu, 12 Mar 2020 13:21:29 GMT  
		Size: 26.7 MB (26690587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f11b29a9c7306674a9479158c1b4259938af11b97359d9ac02030cc1095e9ed1`  
		Last Modified: Fri, 20 Mar 2020 19:21:18 GMT  
		Size: 35.4 KB (35372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:930bda195c84cf132344bf38edcad255317382f910503fef234a9ce3bff0f4dd`  
		Last Modified: Fri, 20 Mar 2020 19:21:18 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78bf9a5ad49e4ae42a83f4995ade4efc096f78fd38299cf05bc041e8cdda2a36`  
		Last Modified: Fri, 20 Mar 2020 19:21:18 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7fb3809884c8771103b4475a778eb0a14b736d5f2008d7ef534950c9b6b77d`  
		Last Modified: Fri, 20 Mar 2020 20:50:51 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7237292ff8a2ff64ff0898dc8792b23e5abe90bf32d14f0d4d9eb6ab9e956dd`  
		Last Modified: Fri, 20 Mar 2020 20:50:50 GMT  
		Size: 3.0 MB (2982755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cdf1eb96f71308e6f5be52c3f5278ff6de496b971e1a94d6adb60fc52b2835f`  
		Last Modified: Fri, 17 Apr 2020 16:55:51 GMT  
		Size: 5.8 MB (5824593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39c254c62945d89e0d0e07c721ca9da0ee5848ace6fd9ce95f719a6b721c2be`  
		Last Modified: Fri, 17 Apr 2020 16:55:49 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:110f77aab367a0f38f766fa5d307186a68fdd7483177e20a62c2eee431fb244d`  
		Last Modified: Fri, 17 Apr 2020 16:55:48 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6bec5ffc4eadbe0fa6b84373fe7eaed47c67d2a505a1c640f7cc79c84b5278`  
		Last Modified: Mon, 20 Apr 2020 17:45:00 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d994803edb5bbd3b979490f3ccbe46fc0977dc6fb469fab88fccc9115d0675`  
		Last Modified: Mon, 20 Apr 2020 17:45:27 GMT  
		Size: 129.1 MB (129110699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4266b1dcdabb8fe88172e362ae653d5564293bcd065b45dba2a8e765b4902ab9`  
		Last Modified: Mon, 20 Apr 2020 17:45:00 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3143b095bd39dff0535f074d233459b67c33b68bf2bd7f6d69220bae208a8cac`  
		Last Modified: Mon, 20 Apr 2020 17:45:00 GMT  
		Size: 4.0 KB (3952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2.6-bionic` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:25821e16c7c401986caa09fba3be08b103203a1599edaba8cd34366903b4b3e6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154693716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c06ecd9c0f139339bf92dbef6e630dca8acc4265b72752f7d7b37e16786ed8d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

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
# Fri, 24 Apr 2020 16:18:50 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Apr 2020 16:19:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 16:19:09 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 16:19:09 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Apr 2020 16:19:31 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 16:19:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 16:19:33 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 24 Apr 2020 16:19:35 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 16:19:36 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Apr 2020 16:19:37 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 16:19:37 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 16:19:38 GMT
ENV MONGO_MAJOR=4.2
# Fri, 24 Apr 2020 16:19:38 GMT
ENV MONGO_VERSION=4.2.6
# Fri, 24 Apr 2020 16:19:40 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Apr 2020 16:20:06 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Apr 2020 16:20:09 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Apr 2020 16:20:10 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Apr 2020 16:20:10 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Apr 2020 16:20:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 16:20:11 GMT
EXPOSE 27017
# Fri, 24 Apr 2020 16:20:12 GMT
CMD ["mongod"]
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
	-	`sha256:d1a8d1af89634c78002ec70ef345dd88801eff1bbca938f85fc7472acf873b32`  
		Last Modified: Fri, 24 Apr 2020 16:21:43 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c03832d333b77fecdaaf76768c24a0c6797373a576bd7fb9abc41f3e3e5e2e4`  
		Last Modified: Fri, 24 Apr 2020 16:21:43 GMT  
		Size: 2.7 MB (2675928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544b6736a2d19b775007ab26e1c72ee2e84911c375eec60ec697fe5e8deca69f`  
		Last Modified: Fri, 24 Apr 2020 16:21:44 GMT  
		Size: 5.3 MB (5345352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920aac5b0c675d956885986db6ac84f954ff2f6a98df26a133ae89ae619cd5be`  
		Last Modified: Fri, 24 Apr 2020 16:21:42 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d53bf51618735c85e240ace69cf43a38a4077593fb9b4633fc1d85d2e655016`  
		Last Modified: Fri, 24 Apr 2020 16:21:41 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5296ff1757ed119711f3cc049cb72f1f77178850e6ba2efc6cb0d1e9e1687bdf`  
		Last Modified: Fri, 24 Apr 2020 16:21:41 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7697b84404da018afccd718c3454ed04a6ee05110f0d573a5d73e25a5c5cd75c`  
		Last Modified: Fri, 24 Apr 2020 16:22:09 GMT  
		Size: 122.9 MB (122907968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458af224982cf3028e9a2a89e362caa3e795382c0448adc60b4ab96bedbcc1ef`  
		Last Modified: Fri, 24 Apr 2020 16:21:41 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7506dcffce0af812ecd82776f582f438856fd75e7f948fa2a689a841eaf272e0`  
		Last Modified: Fri, 24 Apr 2020 16:21:41 GMT  
		Size: 4.0 KB (3955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2.6-bionic` - linux; s390x

```console
$ docker pull mongo@sha256:9a853858232155d691db93ab8ab614ad4636f9465aaab10dad522c6ffdbb6fd5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160626574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb6080841c0f9e130ab30d755a2610d8101b8b45a55cfbce1852edce8e90e15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 23 Apr 2020 17:52:20 GMT
ADD file:ea66ef2a01c547f771866bfa221969f8a30489c28d2a81be8dde7f40e73da33b in / 
# Thu, 23 Apr 2020 17:52:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 17:52:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 17:52:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 17:52:31 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 07:34:44 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Apr 2020 07:34:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 07:34:51 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 07:34:51 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Apr 2020 07:35:02 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 07:35:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 07:35:03 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 24 Apr 2020 07:35:09 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 07:35:10 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Apr 2020 07:35:10 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 07:35:10 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 07:35:11 GMT
ENV MONGO_MAJOR=4.2
# Fri, 24 Apr 2020 07:35:11 GMT
ENV MONGO_VERSION=4.2.6
# Fri, 24 Apr 2020 07:35:12 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Apr 2020 07:35:33 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Apr 2020 07:35:38 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Apr 2020 07:35:38 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Apr 2020 07:35:38 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Apr 2020 07:35:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 07:35:39 GMT
EXPOSE 27017
# Fri, 24 Apr 2020 07:35:39 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:13b4c2e4bb97a2a80bb0e557eeba41e4adea0f5e18352e359bca3f847193899c`  
		Last Modified: Mon, 06 Apr 2020 15:41:16 GMT  
		Size: 25.4 MB (25365338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:471a80e39fb485b86610de915eaaad3d867cc97e460b6da3bb656e03520e8a63`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 36.2 KB (36171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb0c128ddabc6a980ec71426ade04fc9bba2e1afcdc243e2d09c316b635f814`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678052ac148ee123df2f0773eb3a0f5f90490ada8b9a5705363b18a2f45fbe88`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c464d6728e9ac439c8d2dc10a88d64a54c34ac50926c66cb7b6d12e37b15d6`  
		Last Modified: Fri, 24 Apr 2020 07:36:04 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd364a38efacff4956ad8e4082d7fa9593aa0a036757fdfbe97487eb26ea2c9`  
		Last Modified: Fri, 24 Apr 2020 07:36:03 GMT  
		Size: 2.7 MB (2714610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e788a62ef53016c8add2417fa25e2141e1b7293acd648f26ed2ddffd54e605b`  
		Last Modified: Fri, 24 Apr 2020 07:36:02 GMT  
		Size: 5.7 MB (5744825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e103dac172d8152c577b2075cc90e6b674188775064cccfbbbc84d93979b3e56`  
		Last Modified: Fri, 24 Apr 2020 07:36:00 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:259fb52c1ef634a5a074adebdaa3f4fc95e636e570c5719c5d662babed85392e`  
		Last Modified: Fri, 24 Apr 2020 07:35:59 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f95c28bb62ddcdbb79cc6870d5cd9701c912a6307bde4c657e1d0c619430fab`  
		Last Modified: Fri, 24 Apr 2020 07:35:58 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05cea8c1238e8ec47654f290d7a566d006d9302762e741316cd236b909d4577d`  
		Last Modified: Fri, 24 Apr 2020 07:36:18 GMT  
		Size: 126.8 MB (126756767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a873535c8ae6f6827fe3d880ab25b1cc404dc3b74898d2ca9bff17136b83caba`  
		Last Modified: Fri, 24 Apr 2020 07:36:04 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d64c0289b5d5c3ee9e04955ed738543e81fdae4e1a43328fd4d88be18d402b`  
		Last Modified: Fri, 24 Apr 2020 07:36:30 GMT  
		Size: 4.0 KB (3954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.2.6-windowsservercore`

```console
$ docker pull mongo@sha256:29ca3bea646a83d01e3e25e0046a5c18fe594e2ee511c7dc50a489e282582d80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3630; amd64
	-	windows version 10.0.17763.1158; amd64

### `mongo:4.2.6-windowsservercore` - windows version 10.0.14393.3630; amd64

```console
$ docker pull mongo@sha256:dd6d940f7a8469cd7ff4d01cf767e861e05ea91c4e01707ea74ed2b633b56f20
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6184565858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fe805e4e3cf7852986e9f6716f85f270946e78bb6585812cc72368454753b47`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Apr 2020 17:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Apr 2020 12:52:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 20 Apr 2020 18:34:28 GMT
ENV MONGO_VERSION=4.2.6
# Mon, 20 Apr 2020 18:34:29 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.6-signed.msi
# Mon, 20 Apr 2020 18:34:30 GMT
ENV MONGO_DOWNLOAD_SHA256=401ebc0c087058cd98194046bbd4fbee243592cf9397f36a1fafa208de4ac21e
# Mon, 20 Apr 2020 18:52:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 20 Apr 2020 18:52:25 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 20 Apr 2020 18:52:26 GMT
EXPOSE 27017
# Mon, 20 Apr 2020 18:52:27 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d0099407ec8ccaf0472e55152e38b262bdf0b2cf8dfd2e8afcc89d728ba3f5a0`  
		Size: 1.7 GB (1658081673 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5171ed01a0687a59b2bdf59e2df29a8932abe0ee22a4a6ff6368f8a8295a97d1`  
		Last Modified: Wed, 15 Apr 2020 15:29:42 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a316c4dbc306f67b8ac735d957f87c1afbef1afde59d7b13febb4777781f6eb`  
		Last Modified: Mon, 20 Apr 2020 19:17:03 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e05862ade99bc32c017752427f4eb4ac19437b38181c6900cfed1d6a99d6510`  
		Last Modified: Mon, 20 Apr 2020 19:17:02 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7bdc8ea0d500490783e39f9355fa0349a2d9c32cd29ac8cbdd9a06e848cccda`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f30ae2c8c647fe5e41e956e8cb45d970e0761b0d144aa2a1a1c991f5627caa78`  
		Last Modified: Mon, 20 Apr 2020 19:18:45 GMT  
		Size: 456.5 MB (456490346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2069620de21f9e09ee89665e7488732e9804b4ebabb671846dcc5a2efad828f`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9793d6d47e628c898abbf674bad2cd450299481e89b30f575aac87fc2d186496`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b962b3b43034bdc9d37b9b1a386a2abcdb5b6c8a648d35aa3b46bd884a3c439`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2.6-windowsservercore` - windows version 10.0.17763.1158; amd64

```console
$ docker pull mongo@sha256:98dc02185399f9a980eeac228255f8e42451f535d99c12f71015f176dacbce2f
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2726301729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98407fec53691f82e5cd2eb3a2bda7d93127266f2f6a5f4b7fc5d15a33987224`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Wed, 15 Apr 2020 12:44:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 20 Apr 2020 18:52:33 GMT
ENV MONGO_VERSION=4.2.6
# Mon, 20 Apr 2020 18:52:34 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.6-signed.msi
# Mon, 20 Apr 2020 18:52:35 GMT
ENV MONGO_DOWNLOAD_SHA256=401ebc0c087058cd98194046bbd4fbee243592cf9397f36a1fafa208de4ac21e
# Mon, 20 Apr 2020 19:16:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 20 Apr 2020 19:16:07 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 20 Apr 2020 19:16:08 GMT
EXPOSE 27017
# Mon, 20 Apr 2020 19:16:10 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:442da5a04696895ce6580924a45188bbec9a9db9f81cb7dcef41fc1d4b119130`  
		Last Modified: Wed, 15 Apr 2020 15:29:13 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd1d4721643d80e780c8f74ccda6db920cd5d6702e3a02cecc0a28dc3df2b90`  
		Last Modified: Mon, 20 Apr 2020 19:19:18 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f67966d3a477caf485aaf4080d27615f90dfeed53dd3ba0fd149e65a6b97531`  
		Last Modified: Mon, 20 Apr 2020 19:19:18 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3f18459245d1b377a5dd3fc17087c4c9f225ae47f7e5293f1bd6fca26b0879`  
		Last Modified: Mon, 20 Apr 2020 19:19:15 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff28a577006caf2972aa81e377a6ddbc80a4f337df7c3fc877bc22c875d70b30`  
		Last Modified: Mon, 20 Apr 2020 19:20:11 GMT  
		Size: 455.6 MB (455586654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88cd1efbb2ca082ab8c0e84173075d04be6d252eea7a7f18d961f40e12ac4a0`  
		Last Modified: Mon, 20 Apr 2020 19:19:15 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1eb8768e3e39daa6fe8c5e1c37f5928b6bf0a79e6f13ec87956b42d9e01756d`  
		Last Modified: Mon, 20 Apr 2020 19:19:16 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdc5f1e7a5e65ad06c77f10ba2410b9c07f078d86c597960e5760ad0e398a9d2`  
		Last Modified: Mon, 20 Apr 2020 19:19:15 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.2.6-windowsservercore-1809`

```console
$ docker pull mongo@sha256:a14620e311ff3a231892aeb35aa5b8ec88c6ab01ffda9a0941c4159344f999e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1158; amd64

### `mongo:4.2.6-windowsservercore-1809` - windows version 10.0.17763.1158; amd64

```console
$ docker pull mongo@sha256:98dc02185399f9a980eeac228255f8e42451f535d99c12f71015f176dacbce2f
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2726301729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98407fec53691f82e5cd2eb3a2bda7d93127266f2f6a5f4b7fc5d15a33987224`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Wed, 15 Apr 2020 12:44:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 20 Apr 2020 18:52:33 GMT
ENV MONGO_VERSION=4.2.6
# Mon, 20 Apr 2020 18:52:34 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.6-signed.msi
# Mon, 20 Apr 2020 18:52:35 GMT
ENV MONGO_DOWNLOAD_SHA256=401ebc0c087058cd98194046bbd4fbee243592cf9397f36a1fafa208de4ac21e
# Mon, 20 Apr 2020 19:16:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 20 Apr 2020 19:16:07 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 20 Apr 2020 19:16:08 GMT
EXPOSE 27017
# Mon, 20 Apr 2020 19:16:10 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:442da5a04696895ce6580924a45188bbec9a9db9f81cb7dcef41fc1d4b119130`  
		Last Modified: Wed, 15 Apr 2020 15:29:13 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd1d4721643d80e780c8f74ccda6db920cd5d6702e3a02cecc0a28dc3df2b90`  
		Last Modified: Mon, 20 Apr 2020 19:19:18 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f67966d3a477caf485aaf4080d27615f90dfeed53dd3ba0fd149e65a6b97531`  
		Last Modified: Mon, 20 Apr 2020 19:19:18 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3f18459245d1b377a5dd3fc17087c4c9f225ae47f7e5293f1bd6fca26b0879`  
		Last Modified: Mon, 20 Apr 2020 19:19:15 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff28a577006caf2972aa81e377a6ddbc80a4f337df7c3fc877bc22c875d70b30`  
		Last Modified: Mon, 20 Apr 2020 19:20:11 GMT  
		Size: 455.6 MB (455586654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88cd1efbb2ca082ab8c0e84173075d04be6d252eea7a7f18d961f40e12ac4a0`  
		Last Modified: Mon, 20 Apr 2020 19:19:15 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1eb8768e3e39daa6fe8c5e1c37f5928b6bf0a79e6f13ec87956b42d9e01756d`  
		Last Modified: Mon, 20 Apr 2020 19:19:16 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdc5f1e7a5e65ad06c77f10ba2410b9c07f078d86c597960e5760ad0e398a9d2`  
		Last Modified: Mon, 20 Apr 2020 19:19:15 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.2.6-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:05c800b1878e2a6e157c15ac110f83316f73f52e94e5b204c8f1f89acee4477b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3630; amd64

### `mongo:4.2.6-windowsservercore-ltsc2016` - windows version 10.0.14393.3630; amd64

```console
$ docker pull mongo@sha256:dd6d940f7a8469cd7ff4d01cf767e861e05ea91c4e01707ea74ed2b633b56f20
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6184565858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fe805e4e3cf7852986e9f6716f85f270946e78bb6585812cc72368454753b47`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Apr 2020 17:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Apr 2020 12:52:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 20 Apr 2020 18:34:28 GMT
ENV MONGO_VERSION=4.2.6
# Mon, 20 Apr 2020 18:34:29 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.6-signed.msi
# Mon, 20 Apr 2020 18:34:30 GMT
ENV MONGO_DOWNLOAD_SHA256=401ebc0c087058cd98194046bbd4fbee243592cf9397f36a1fafa208de4ac21e
# Mon, 20 Apr 2020 18:52:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 20 Apr 2020 18:52:25 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 20 Apr 2020 18:52:26 GMT
EXPOSE 27017
# Mon, 20 Apr 2020 18:52:27 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d0099407ec8ccaf0472e55152e38b262bdf0b2cf8dfd2e8afcc89d728ba3f5a0`  
		Size: 1.7 GB (1658081673 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5171ed01a0687a59b2bdf59e2df29a8932abe0ee22a4a6ff6368f8a8295a97d1`  
		Last Modified: Wed, 15 Apr 2020 15:29:42 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a316c4dbc306f67b8ac735d957f87c1afbef1afde59d7b13febb4777781f6eb`  
		Last Modified: Mon, 20 Apr 2020 19:17:03 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e05862ade99bc32c017752427f4eb4ac19437b38181c6900cfed1d6a99d6510`  
		Last Modified: Mon, 20 Apr 2020 19:17:02 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7bdc8ea0d500490783e39f9355fa0349a2d9c32cd29ac8cbdd9a06e848cccda`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f30ae2c8c647fe5e41e956e8cb45d970e0761b0d144aa2a1a1c991f5627caa78`  
		Last Modified: Mon, 20 Apr 2020 19:18:45 GMT  
		Size: 456.5 MB (456490346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2069620de21f9e09ee89665e7488732e9804b4ebabb671846dcc5a2efad828f`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9793d6d47e628c898abbf674bad2cd450299481e89b30f575aac87fc2d186496`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b962b3b43034bdc9d37b9b1a386a2abcdb5b6c8a648d35aa3b46bd884a3c439`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.2-bionic`

```console
$ docker pull mongo@sha256:e4abccb1677a976b66d2c726586fc40a073aa3ce4fc5ef6bbc18267e3394d19c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `mongo:4.2-bionic` - linux; amd64

```console
$ docker pull mongo@sha256:18f7e39575cd12e9177017ddaa4bcb6c3bae1f6468f3922dc1ecd0662e10281c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164652772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e9495ea1bc639197bc40aef2beedf931078003d8933fb38240f3a1a63c90119`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 20 Mar 2020 19:20:20 GMT
ADD file:594fa35cf803361e69d817fc867b6a4069c064ffd20ed50caf42ad9bb11ca999 in / 
# Fri, 20 Mar 2020 19:20:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 20 Mar 2020 19:20:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 20 Mar 2020 19:20:22 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 20 Mar 2020 19:20:22 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2020 20:49:50 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 20 Mar 2020 20:49:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 16:53:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 17 Apr 2020 16:53:54 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 17 Apr 2020 16:54:10 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 17 Apr 2020 16:54:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 17 Apr 2020 16:54:11 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 17 Apr 2020 16:54:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 17 Apr 2020 16:54:12 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 17 Apr 2020 16:54:13 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 17 Apr 2020 16:54:13 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 17 Apr 2020 16:54:13 GMT
ENV MONGO_MAJOR=4.2
# Mon, 20 Apr 2020 17:44:11 GMT
ENV MONGO_VERSION=4.2.6
# Mon, 20 Apr 2020 17:44:12 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Mon, 20 Apr 2020 17:44:40 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Mon, 20 Apr 2020 17:44:41 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Mon, 20 Apr 2020 17:44:41 GMT
VOLUME [/data/db /data/configdb]
# Mon, 20 Apr 2020 17:44:41 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Mon, 20 Apr 2020 17:44:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2020 17:44:42 GMT
EXPOSE 27017
# Mon, 20 Apr 2020 17:44:42 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:5bed26d33875e6da1d9ff9a1054c5fef3bbeb22ee979e14b72acf72528de007b`  
		Last Modified: Thu, 12 Mar 2020 13:21:29 GMT  
		Size: 26.7 MB (26690587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f11b29a9c7306674a9479158c1b4259938af11b97359d9ac02030cc1095e9ed1`  
		Last Modified: Fri, 20 Mar 2020 19:21:18 GMT  
		Size: 35.4 KB (35372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:930bda195c84cf132344bf38edcad255317382f910503fef234a9ce3bff0f4dd`  
		Last Modified: Fri, 20 Mar 2020 19:21:18 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78bf9a5ad49e4ae42a83f4995ade4efc096f78fd38299cf05bc041e8cdda2a36`  
		Last Modified: Fri, 20 Mar 2020 19:21:18 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7fb3809884c8771103b4475a778eb0a14b736d5f2008d7ef534950c9b6b77d`  
		Last Modified: Fri, 20 Mar 2020 20:50:51 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7237292ff8a2ff64ff0898dc8792b23e5abe90bf32d14f0d4d9eb6ab9e956dd`  
		Last Modified: Fri, 20 Mar 2020 20:50:50 GMT  
		Size: 3.0 MB (2982755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cdf1eb96f71308e6f5be52c3f5278ff6de496b971e1a94d6adb60fc52b2835f`  
		Last Modified: Fri, 17 Apr 2020 16:55:51 GMT  
		Size: 5.8 MB (5824593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39c254c62945d89e0d0e07c721ca9da0ee5848ace6fd9ce95f719a6b721c2be`  
		Last Modified: Fri, 17 Apr 2020 16:55:49 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:110f77aab367a0f38f766fa5d307186a68fdd7483177e20a62c2eee431fb244d`  
		Last Modified: Fri, 17 Apr 2020 16:55:48 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6bec5ffc4eadbe0fa6b84373fe7eaed47c67d2a505a1c640f7cc79c84b5278`  
		Last Modified: Mon, 20 Apr 2020 17:45:00 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d994803edb5bbd3b979490f3ccbe46fc0977dc6fb469fab88fccc9115d0675`  
		Last Modified: Mon, 20 Apr 2020 17:45:27 GMT  
		Size: 129.1 MB (129110699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4266b1dcdabb8fe88172e362ae653d5564293bcd065b45dba2a8e765b4902ab9`  
		Last Modified: Mon, 20 Apr 2020 17:45:00 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3143b095bd39dff0535f074d233459b67c33b68bf2bd7f6d69220bae208a8cac`  
		Last Modified: Mon, 20 Apr 2020 17:45:00 GMT  
		Size: 4.0 KB (3952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2-bionic` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:25821e16c7c401986caa09fba3be08b103203a1599edaba8cd34366903b4b3e6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154693716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c06ecd9c0f139339bf92dbef6e630dca8acc4265b72752f7d7b37e16786ed8d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

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
# Fri, 24 Apr 2020 16:18:50 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Apr 2020 16:19:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 16:19:09 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 16:19:09 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Apr 2020 16:19:31 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 16:19:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 16:19:33 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 24 Apr 2020 16:19:35 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 16:19:36 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Apr 2020 16:19:37 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 16:19:37 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 16:19:38 GMT
ENV MONGO_MAJOR=4.2
# Fri, 24 Apr 2020 16:19:38 GMT
ENV MONGO_VERSION=4.2.6
# Fri, 24 Apr 2020 16:19:40 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Apr 2020 16:20:06 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Apr 2020 16:20:09 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Apr 2020 16:20:10 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Apr 2020 16:20:10 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Apr 2020 16:20:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 16:20:11 GMT
EXPOSE 27017
# Fri, 24 Apr 2020 16:20:12 GMT
CMD ["mongod"]
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
	-	`sha256:d1a8d1af89634c78002ec70ef345dd88801eff1bbca938f85fc7472acf873b32`  
		Last Modified: Fri, 24 Apr 2020 16:21:43 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c03832d333b77fecdaaf76768c24a0c6797373a576bd7fb9abc41f3e3e5e2e4`  
		Last Modified: Fri, 24 Apr 2020 16:21:43 GMT  
		Size: 2.7 MB (2675928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544b6736a2d19b775007ab26e1c72ee2e84911c375eec60ec697fe5e8deca69f`  
		Last Modified: Fri, 24 Apr 2020 16:21:44 GMT  
		Size: 5.3 MB (5345352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920aac5b0c675d956885986db6ac84f954ff2f6a98df26a133ae89ae619cd5be`  
		Last Modified: Fri, 24 Apr 2020 16:21:42 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d53bf51618735c85e240ace69cf43a38a4077593fb9b4633fc1d85d2e655016`  
		Last Modified: Fri, 24 Apr 2020 16:21:41 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5296ff1757ed119711f3cc049cb72f1f77178850e6ba2efc6cb0d1e9e1687bdf`  
		Last Modified: Fri, 24 Apr 2020 16:21:41 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7697b84404da018afccd718c3454ed04a6ee05110f0d573a5d73e25a5c5cd75c`  
		Last Modified: Fri, 24 Apr 2020 16:22:09 GMT  
		Size: 122.9 MB (122907968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458af224982cf3028e9a2a89e362caa3e795382c0448adc60b4ab96bedbcc1ef`  
		Last Modified: Fri, 24 Apr 2020 16:21:41 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7506dcffce0af812ecd82776f582f438856fd75e7f948fa2a689a841eaf272e0`  
		Last Modified: Fri, 24 Apr 2020 16:21:41 GMT  
		Size: 4.0 KB (3955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2-bionic` - linux; s390x

```console
$ docker pull mongo@sha256:9a853858232155d691db93ab8ab614ad4636f9465aaab10dad522c6ffdbb6fd5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160626574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb6080841c0f9e130ab30d755a2610d8101b8b45a55cfbce1852edce8e90e15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 23 Apr 2020 17:52:20 GMT
ADD file:ea66ef2a01c547f771866bfa221969f8a30489c28d2a81be8dde7f40e73da33b in / 
# Thu, 23 Apr 2020 17:52:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 17:52:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 17:52:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 17:52:31 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 07:34:44 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Apr 2020 07:34:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 07:34:51 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 07:34:51 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Apr 2020 07:35:02 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 07:35:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 07:35:03 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 24 Apr 2020 07:35:09 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 07:35:10 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Apr 2020 07:35:10 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 07:35:10 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 07:35:11 GMT
ENV MONGO_MAJOR=4.2
# Fri, 24 Apr 2020 07:35:11 GMT
ENV MONGO_VERSION=4.2.6
# Fri, 24 Apr 2020 07:35:12 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Apr 2020 07:35:33 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Apr 2020 07:35:38 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Apr 2020 07:35:38 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Apr 2020 07:35:38 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Apr 2020 07:35:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 07:35:39 GMT
EXPOSE 27017
# Fri, 24 Apr 2020 07:35:39 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:13b4c2e4bb97a2a80bb0e557eeba41e4adea0f5e18352e359bca3f847193899c`  
		Last Modified: Mon, 06 Apr 2020 15:41:16 GMT  
		Size: 25.4 MB (25365338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:471a80e39fb485b86610de915eaaad3d867cc97e460b6da3bb656e03520e8a63`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 36.2 KB (36171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb0c128ddabc6a980ec71426ade04fc9bba2e1afcdc243e2d09c316b635f814`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678052ac148ee123df2f0773eb3a0f5f90490ada8b9a5705363b18a2f45fbe88`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c464d6728e9ac439c8d2dc10a88d64a54c34ac50926c66cb7b6d12e37b15d6`  
		Last Modified: Fri, 24 Apr 2020 07:36:04 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd364a38efacff4956ad8e4082d7fa9593aa0a036757fdfbe97487eb26ea2c9`  
		Last Modified: Fri, 24 Apr 2020 07:36:03 GMT  
		Size: 2.7 MB (2714610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e788a62ef53016c8add2417fa25e2141e1b7293acd648f26ed2ddffd54e605b`  
		Last Modified: Fri, 24 Apr 2020 07:36:02 GMT  
		Size: 5.7 MB (5744825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e103dac172d8152c577b2075cc90e6b674188775064cccfbbbc84d93979b3e56`  
		Last Modified: Fri, 24 Apr 2020 07:36:00 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:259fb52c1ef634a5a074adebdaa3f4fc95e636e570c5719c5d662babed85392e`  
		Last Modified: Fri, 24 Apr 2020 07:35:59 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f95c28bb62ddcdbb79cc6870d5cd9701c912a6307bde4c657e1d0c619430fab`  
		Last Modified: Fri, 24 Apr 2020 07:35:58 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05cea8c1238e8ec47654f290d7a566d006d9302762e741316cd236b909d4577d`  
		Last Modified: Fri, 24 Apr 2020 07:36:18 GMT  
		Size: 126.8 MB (126756767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a873535c8ae6f6827fe3d880ab25b1cc404dc3b74898d2ca9bff17136b83caba`  
		Last Modified: Fri, 24 Apr 2020 07:36:04 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d64c0289b5d5c3ee9e04955ed738543e81fdae4e1a43328fd4d88be18d402b`  
		Last Modified: Fri, 24 Apr 2020 07:36:30 GMT  
		Size: 4.0 KB (3954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.2-windowsservercore`

```console
$ docker pull mongo@sha256:29ca3bea646a83d01e3e25e0046a5c18fe594e2ee511c7dc50a489e282582d80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3630; amd64
	-	windows version 10.0.17763.1158; amd64

### `mongo:4.2-windowsservercore` - windows version 10.0.14393.3630; amd64

```console
$ docker pull mongo@sha256:dd6d940f7a8469cd7ff4d01cf767e861e05ea91c4e01707ea74ed2b633b56f20
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6184565858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fe805e4e3cf7852986e9f6716f85f270946e78bb6585812cc72368454753b47`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Apr 2020 17:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Apr 2020 12:52:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 20 Apr 2020 18:34:28 GMT
ENV MONGO_VERSION=4.2.6
# Mon, 20 Apr 2020 18:34:29 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.6-signed.msi
# Mon, 20 Apr 2020 18:34:30 GMT
ENV MONGO_DOWNLOAD_SHA256=401ebc0c087058cd98194046bbd4fbee243592cf9397f36a1fafa208de4ac21e
# Mon, 20 Apr 2020 18:52:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 20 Apr 2020 18:52:25 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 20 Apr 2020 18:52:26 GMT
EXPOSE 27017
# Mon, 20 Apr 2020 18:52:27 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d0099407ec8ccaf0472e55152e38b262bdf0b2cf8dfd2e8afcc89d728ba3f5a0`  
		Size: 1.7 GB (1658081673 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5171ed01a0687a59b2bdf59e2df29a8932abe0ee22a4a6ff6368f8a8295a97d1`  
		Last Modified: Wed, 15 Apr 2020 15:29:42 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a316c4dbc306f67b8ac735d957f87c1afbef1afde59d7b13febb4777781f6eb`  
		Last Modified: Mon, 20 Apr 2020 19:17:03 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e05862ade99bc32c017752427f4eb4ac19437b38181c6900cfed1d6a99d6510`  
		Last Modified: Mon, 20 Apr 2020 19:17:02 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7bdc8ea0d500490783e39f9355fa0349a2d9c32cd29ac8cbdd9a06e848cccda`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f30ae2c8c647fe5e41e956e8cb45d970e0761b0d144aa2a1a1c991f5627caa78`  
		Last Modified: Mon, 20 Apr 2020 19:18:45 GMT  
		Size: 456.5 MB (456490346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2069620de21f9e09ee89665e7488732e9804b4ebabb671846dcc5a2efad828f`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9793d6d47e628c898abbf674bad2cd450299481e89b30f575aac87fc2d186496`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b962b3b43034bdc9d37b9b1a386a2abcdb5b6c8a648d35aa3b46bd884a3c439`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2-windowsservercore` - windows version 10.0.17763.1158; amd64

```console
$ docker pull mongo@sha256:98dc02185399f9a980eeac228255f8e42451f535d99c12f71015f176dacbce2f
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2726301729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98407fec53691f82e5cd2eb3a2bda7d93127266f2f6a5f4b7fc5d15a33987224`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Wed, 15 Apr 2020 12:44:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 20 Apr 2020 18:52:33 GMT
ENV MONGO_VERSION=4.2.6
# Mon, 20 Apr 2020 18:52:34 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.6-signed.msi
# Mon, 20 Apr 2020 18:52:35 GMT
ENV MONGO_DOWNLOAD_SHA256=401ebc0c087058cd98194046bbd4fbee243592cf9397f36a1fafa208de4ac21e
# Mon, 20 Apr 2020 19:16:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 20 Apr 2020 19:16:07 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 20 Apr 2020 19:16:08 GMT
EXPOSE 27017
# Mon, 20 Apr 2020 19:16:10 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:442da5a04696895ce6580924a45188bbec9a9db9f81cb7dcef41fc1d4b119130`  
		Last Modified: Wed, 15 Apr 2020 15:29:13 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd1d4721643d80e780c8f74ccda6db920cd5d6702e3a02cecc0a28dc3df2b90`  
		Last Modified: Mon, 20 Apr 2020 19:19:18 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f67966d3a477caf485aaf4080d27615f90dfeed53dd3ba0fd149e65a6b97531`  
		Last Modified: Mon, 20 Apr 2020 19:19:18 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3f18459245d1b377a5dd3fc17087c4c9f225ae47f7e5293f1bd6fca26b0879`  
		Last Modified: Mon, 20 Apr 2020 19:19:15 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff28a577006caf2972aa81e377a6ddbc80a4f337df7c3fc877bc22c875d70b30`  
		Last Modified: Mon, 20 Apr 2020 19:20:11 GMT  
		Size: 455.6 MB (455586654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88cd1efbb2ca082ab8c0e84173075d04be6d252eea7a7f18d961f40e12ac4a0`  
		Last Modified: Mon, 20 Apr 2020 19:19:15 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1eb8768e3e39daa6fe8c5e1c37f5928b6bf0a79e6f13ec87956b42d9e01756d`  
		Last Modified: Mon, 20 Apr 2020 19:19:16 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdc5f1e7a5e65ad06c77f10ba2410b9c07f078d86c597960e5760ad0e398a9d2`  
		Last Modified: Mon, 20 Apr 2020 19:19:15 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.2-windowsservercore-1809`

```console
$ docker pull mongo@sha256:a14620e311ff3a231892aeb35aa5b8ec88c6ab01ffda9a0941c4159344f999e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1158; amd64

### `mongo:4.2-windowsservercore-1809` - windows version 10.0.17763.1158; amd64

```console
$ docker pull mongo@sha256:98dc02185399f9a980eeac228255f8e42451f535d99c12f71015f176dacbce2f
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2726301729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98407fec53691f82e5cd2eb3a2bda7d93127266f2f6a5f4b7fc5d15a33987224`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Wed, 15 Apr 2020 12:44:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 20 Apr 2020 18:52:33 GMT
ENV MONGO_VERSION=4.2.6
# Mon, 20 Apr 2020 18:52:34 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.6-signed.msi
# Mon, 20 Apr 2020 18:52:35 GMT
ENV MONGO_DOWNLOAD_SHA256=401ebc0c087058cd98194046bbd4fbee243592cf9397f36a1fafa208de4ac21e
# Mon, 20 Apr 2020 19:16:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 20 Apr 2020 19:16:07 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 20 Apr 2020 19:16:08 GMT
EXPOSE 27017
# Mon, 20 Apr 2020 19:16:10 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:442da5a04696895ce6580924a45188bbec9a9db9f81cb7dcef41fc1d4b119130`  
		Last Modified: Wed, 15 Apr 2020 15:29:13 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd1d4721643d80e780c8f74ccda6db920cd5d6702e3a02cecc0a28dc3df2b90`  
		Last Modified: Mon, 20 Apr 2020 19:19:18 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f67966d3a477caf485aaf4080d27615f90dfeed53dd3ba0fd149e65a6b97531`  
		Last Modified: Mon, 20 Apr 2020 19:19:18 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3f18459245d1b377a5dd3fc17087c4c9f225ae47f7e5293f1bd6fca26b0879`  
		Last Modified: Mon, 20 Apr 2020 19:19:15 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff28a577006caf2972aa81e377a6ddbc80a4f337df7c3fc877bc22c875d70b30`  
		Last Modified: Mon, 20 Apr 2020 19:20:11 GMT  
		Size: 455.6 MB (455586654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88cd1efbb2ca082ab8c0e84173075d04be6d252eea7a7f18d961f40e12ac4a0`  
		Last Modified: Mon, 20 Apr 2020 19:19:15 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1eb8768e3e39daa6fe8c5e1c37f5928b6bf0a79e6f13ec87956b42d9e01756d`  
		Last Modified: Mon, 20 Apr 2020 19:19:16 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdc5f1e7a5e65ad06c77f10ba2410b9c07f078d86c597960e5760ad0e398a9d2`  
		Last Modified: Mon, 20 Apr 2020 19:19:15 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.2-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:05c800b1878e2a6e157c15ac110f83316f73f52e94e5b204c8f1f89acee4477b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3630; amd64

### `mongo:4.2-windowsservercore-ltsc2016` - windows version 10.0.14393.3630; amd64

```console
$ docker pull mongo@sha256:dd6d940f7a8469cd7ff4d01cf767e861e05ea91c4e01707ea74ed2b633b56f20
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6184565858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fe805e4e3cf7852986e9f6716f85f270946e78bb6585812cc72368454753b47`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Apr 2020 17:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Apr 2020 12:52:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 20 Apr 2020 18:34:28 GMT
ENV MONGO_VERSION=4.2.6
# Mon, 20 Apr 2020 18:34:29 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.6-signed.msi
# Mon, 20 Apr 2020 18:34:30 GMT
ENV MONGO_DOWNLOAD_SHA256=401ebc0c087058cd98194046bbd4fbee243592cf9397f36a1fafa208de4ac21e
# Mon, 20 Apr 2020 18:52:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 20 Apr 2020 18:52:25 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 20 Apr 2020 18:52:26 GMT
EXPOSE 27017
# Mon, 20 Apr 2020 18:52:27 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d0099407ec8ccaf0472e55152e38b262bdf0b2cf8dfd2e8afcc89d728ba3f5a0`  
		Size: 1.7 GB (1658081673 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5171ed01a0687a59b2bdf59e2df29a8932abe0ee22a4a6ff6368f8a8295a97d1`  
		Last Modified: Wed, 15 Apr 2020 15:29:42 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a316c4dbc306f67b8ac735d957f87c1afbef1afde59d7b13febb4777781f6eb`  
		Last Modified: Mon, 20 Apr 2020 19:17:03 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e05862ade99bc32c017752427f4eb4ac19437b38181c6900cfed1d6a99d6510`  
		Last Modified: Mon, 20 Apr 2020 19:17:02 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7bdc8ea0d500490783e39f9355fa0349a2d9c32cd29ac8cbdd9a06e848cccda`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f30ae2c8c647fe5e41e956e8cb45d970e0761b0d144aa2a1a1c991f5627caa78`  
		Last Modified: Mon, 20 Apr 2020 19:18:45 GMT  
		Size: 456.5 MB (456490346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2069620de21f9e09ee89665e7488732e9804b4ebabb671846dcc5a2efad828f`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9793d6d47e628c898abbf674bad2cd450299481e89b30f575aac87fc2d186496`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b962b3b43034bdc9d37b9b1a386a2abcdb5b6c8a648d35aa3b46bd884a3c439`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4-bionic`

```console
$ docker pull mongo@sha256:e4abccb1677a976b66d2c726586fc40a073aa3ce4fc5ef6bbc18267e3394d19c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `mongo:4-bionic` - linux; amd64

```console
$ docker pull mongo@sha256:18f7e39575cd12e9177017ddaa4bcb6c3bae1f6468f3922dc1ecd0662e10281c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164652772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e9495ea1bc639197bc40aef2beedf931078003d8933fb38240f3a1a63c90119`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 20 Mar 2020 19:20:20 GMT
ADD file:594fa35cf803361e69d817fc867b6a4069c064ffd20ed50caf42ad9bb11ca999 in / 
# Fri, 20 Mar 2020 19:20:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 20 Mar 2020 19:20:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 20 Mar 2020 19:20:22 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 20 Mar 2020 19:20:22 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2020 20:49:50 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 20 Mar 2020 20:49:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 16:53:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 17 Apr 2020 16:53:54 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 17 Apr 2020 16:54:10 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 17 Apr 2020 16:54:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 17 Apr 2020 16:54:11 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 17 Apr 2020 16:54:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 17 Apr 2020 16:54:12 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 17 Apr 2020 16:54:13 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 17 Apr 2020 16:54:13 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 17 Apr 2020 16:54:13 GMT
ENV MONGO_MAJOR=4.2
# Mon, 20 Apr 2020 17:44:11 GMT
ENV MONGO_VERSION=4.2.6
# Mon, 20 Apr 2020 17:44:12 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Mon, 20 Apr 2020 17:44:40 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Mon, 20 Apr 2020 17:44:41 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Mon, 20 Apr 2020 17:44:41 GMT
VOLUME [/data/db /data/configdb]
# Mon, 20 Apr 2020 17:44:41 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Mon, 20 Apr 2020 17:44:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2020 17:44:42 GMT
EXPOSE 27017
# Mon, 20 Apr 2020 17:44:42 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:5bed26d33875e6da1d9ff9a1054c5fef3bbeb22ee979e14b72acf72528de007b`  
		Last Modified: Thu, 12 Mar 2020 13:21:29 GMT  
		Size: 26.7 MB (26690587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f11b29a9c7306674a9479158c1b4259938af11b97359d9ac02030cc1095e9ed1`  
		Last Modified: Fri, 20 Mar 2020 19:21:18 GMT  
		Size: 35.4 KB (35372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:930bda195c84cf132344bf38edcad255317382f910503fef234a9ce3bff0f4dd`  
		Last Modified: Fri, 20 Mar 2020 19:21:18 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78bf9a5ad49e4ae42a83f4995ade4efc096f78fd38299cf05bc041e8cdda2a36`  
		Last Modified: Fri, 20 Mar 2020 19:21:18 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7fb3809884c8771103b4475a778eb0a14b736d5f2008d7ef534950c9b6b77d`  
		Last Modified: Fri, 20 Mar 2020 20:50:51 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7237292ff8a2ff64ff0898dc8792b23e5abe90bf32d14f0d4d9eb6ab9e956dd`  
		Last Modified: Fri, 20 Mar 2020 20:50:50 GMT  
		Size: 3.0 MB (2982755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cdf1eb96f71308e6f5be52c3f5278ff6de496b971e1a94d6adb60fc52b2835f`  
		Last Modified: Fri, 17 Apr 2020 16:55:51 GMT  
		Size: 5.8 MB (5824593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39c254c62945d89e0d0e07c721ca9da0ee5848ace6fd9ce95f719a6b721c2be`  
		Last Modified: Fri, 17 Apr 2020 16:55:49 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:110f77aab367a0f38f766fa5d307186a68fdd7483177e20a62c2eee431fb244d`  
		Last Modified: Fri, 17 Apr 2020 16:55:48 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6bec5ffc4eadbe0fa6b84373fe7eaed47c67d2a505a1c640f7cc79c84b5278`  
		Last Modified: Mon, 20 Apr 2020 17:45:00 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d994803edb5bbd3b979490f3ccbe46fc0977dc6fb469fab88fccc9115d0675`  
		Last Modified: Mon, 20 Apr 2020 17:45:27 GMT  
		Size: 129.1 MB (129110699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4266b1dcdabb8fe88172e362ae653d5564293bcd065b45dba2a8e765b4902ab9`  
		Last Modified: Mon, 20 Apr 2020 17:45:00 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3143b095bd39dff0535f074d233459b67c33b68bf2bd7f6d69220bae208a8cac`  
		Last Modified: Mon, 20 Apr 2020 17:45:00 GMT  
		Size: 4.0 KB (3952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-bionic` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:25821e16c7c401986caa09fba3be08b103203a1599edaba8cd34366903b4b3e6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154693716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c06ecd9c0f139339bf92dbef6e630dca8acc4265b72752f7d7b37e16786ed8d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

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
# Fri, 24 Apr 2020 16:18:50 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Apr 2020 16:19:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 16:19:09 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 16:19:09 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Apr 2020 16:19:31 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 16:19:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 16:19:33 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 24 Apr 2020 16:19:35 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 16:19:36 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Apr 2020 16:19:37 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 16:19:37 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 16:19:38 GMT
ENV MONGO_MAJOR=4.2
# Fri, 24 Apr 2020 16:19:38 GMT
ENV MONGO_VERSION=4.2.6
# Fri, 24 Apr 2020 16:19:40 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Apr 2020 16:20:06 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Apr 2020 16:20:09 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Apr 2020 16:20:10 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Apr 2020 16:20:10 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Apr 2020 16:20:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 16:20:11 GMT
EXPOSE 27017
# Fri, 24 Apr 2020 16:20:12 GMT
CMD ["mongod"]
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
	-	`sha256:d1a8d1af89634c78002ec70ef345dd88801eff1bbca938f85fc7472acf873b32`  
		Last Modified: Fri, 24 Apr 2020 16:21:43 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c03832d333b77fecdaaf76768c24a0c6797373a576bd7fb9abc41f3e3e5e2e4`  
		Last Modified: Fri, 24 Apr 2020 16:21:43 GMT  
		Size: 2.7 MB (2675928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544b6736a2d19b775007ab26e1c72ee2e84911c375eec60ec697fe5e8deca69f`  
		Last Modified: Fri, 24 Apr 2020 16:21:44 GMT  
		Size: 5.3 MB (5345352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920aac5b0c675d956885986db6ac84f954ff2f6a98df26a133ae89ae619cd5be`  
		Last Modified: Fri, 24 Apr 2020 16:21:42 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d53bf51618735c85e240ace69cf43a38a4077593fb9b4633fc1d85d2e655016`  
		Last Modified: Fri, 24 Apr 2020 16:21:41 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5296ff1757ed119711f3cc049cb72f1f77178850e6ba2efc6cb0d1e9e1687bdf`  
		Last Modified: Fri, 24 Apr 2020 16:21:41 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7697b84404da018afccd718c3454ed04a6ee05110f0d573a5d73e25a5c5cd75c`  
		Last Modified: Fri, 24 Apr 2020 16:22:09 GMT  
		Size: 122.9 MB (122907968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458af224982cf3028e9a2a89e362caa3e795382c0448adc60b4ab96bedbcc1ef`  
		Last Modified: Fri, 24 Apr 2020 16:21:41 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7506dcffce0af812ecd82776f582f438856fd75e7f948fa2a689a841eaf272e0`  
		Last Modified: Fri, 24 Apr 2020 16:21:41 GMT  
		Size: 4.0 KB (3955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-bionic` - linux; s390x

```console
$ docker pull mongo@sha256:9a853858232155d691db93ab8ab614ad4636f9465aaab10dad522c6ffdbb6fd5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160626574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb6080841c0f9e130ab30d755a2610d8101b8b45a55cfbce1852edce8e90e15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 23 Apr 2020 17:52:20 GMT
ADD file:ea66ef2a01c547f771866bfa221969f8a30489c28d2a81be8dde7f40e73da33b in / 
# Thu, 23 Apr 2020 17:52:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 17:52:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 17:52:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 17:52:31 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 07:34:44 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Apr 2020 07:34:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 07:34:51 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 07:34:51 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Apr 2020 07:35:02 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 07:35:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 07:35:03 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 24 Apr 2020 07:35:09 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 07:35:10 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Apr 2020 07:35:10 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 07:35:10 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 07:35:11 GMT
ENV MONGO_MAJOR=4.2
# Fri, 24 Apr 2020 07:35:11 GMT
ENV MONGO_VERSION=4.2.6
# Fri, 24 Apr 2020 07:35:12 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Apr 2020 07:35:33 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Apr 2020 07:35:38 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Apr 2020 07:35:38 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Apr 2020 07:35:38 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Apr 2020 07:35:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 07:35:39 GMT
EXPOSE 27017
# Fri, 24 Apr 2020 07:35:39 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:13b4c2e4bb97a2a80bb0e557eeba41e4adea0f5e18352e359bca3f847193899c`  
		Last Modified: Mon, 06 Apr 2020 15:41:16 GMT  
		Size: 25.4 MB (25365338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:471a80e39fb485b86610de915eaaad3d867cc97e460b6da3bb656e03520e8a63`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 36.2 KB (36171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb0c128ddabc6a980ec71426ade04fc9bba2e1afcdc243e2d09c316b635f814`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678052ac148ee123df2f0773eb3a0f5f90490ada8b9a5705363b18a2f45fbe88`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c464d6728e9ac439c8d2dc10a88d64a54c34ac50926c66cb7b6d12e37b15d6`  
		Last Modified: Fri, 24 Apr 2020 07:36:04 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd364a38efacff4956ad8e4082d7fa9593aa0a036757fdfbe97487eb26ea2c9`  
		Last Modified: Fri, 24 Apr 2020 07:36:03 GMT  
		Size: 2.7 MB (2714610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e788a62ef53016c8add2417fa25e2141e1b7293acd648f26ed2ddffd54e605b`  
		Last Modified: Fri, 24 Apr 2020 07:36:02 GMT  
		Size: 5.7 MB (5744825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e103dac172d8152c577b2075cc90e6b674188775064cccfbbbc84d93979b3e56`  
		Last Modified: Fri, 24 Apr 2020 07:36:00 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:259fb52c1ef634a5a074adebdaa3f4fc95e636e570c5719c5d662babed85392e`  
		Last Modified: Fri, 24 Apr 2020 07:35:59 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f95c28bb62ddcdbb79cc6870d5cd9701c912a6307bde4c657e1d0c619430fab`  
		Last Modified: Fri, 24 Apr 2020 07:35:58 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05cea8c1238e8ec47654f290d7a566d006d9302762e741316cd236b909d4577d`  
		Last Modified: Fri, 24 Apr 2020 07:36:18 GMT  
		Size: 126.8 MB (126756767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a873535c8ae6f6827fe3d880ab25b1cc404dc3b74898d2ca9bff17136b83caba`  
		Last Modified: Fri, 24 Apr 2020 07:36:04 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d64c0289b5d5c3ee9e04955ed738543e81fdae4e1a43328fd4d88be18d402b`  
		Last Modified: Fri, 24 Apr 2020 07:36:30 GMT  
		Size: 4.0 KB (3954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4-windowsservercore`

```console
$ docker pull mongo@sha256:29ca3bea646a83d01e3e25e0046a5c18fe594e2ee511c7dc50a489e282582d80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3630; amd64
	-	windows version 10.0.17763.1158; amd64

### `mongo:4-windowsservercore` - windows version 10.0.14393.3630; amd64

```console
$ docker pull mongo@sha256:dd6d940f7a8469cd7ff4d01cf767e861e05ea91c4e01707ea74ed2b633b56f20
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6184565858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fe805e4e3cf7852986e9f6716f85f270946e78bb6585812cc72368454753b47`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Apr 2020 17:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Apr 2020 12:52:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 20 Apr 2020 18:34:28 GMT
ENV MONGO_VERSION=4.2.6
# Mon, 20 Apr 2020 18:34:29 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.6-signed.msi
# Mon, 20 Apr 2020 18:34:30 GMT
ENV MONGO_DOWNLOAD_SHA256=401ebc0c087058cd98194046bbd4fbee243592cf9397f36a1fafa208de4ac21e
# Mon, 20 Apr 2020 18:52:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 20 Apr 2020 18:52:25 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 20 Apr 2020 18:52:26 GMT
EXPOSE 27017
# Mon, 20 Apr 2020 18:52:27 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d0099407ec8ccaf0472e55152e38b262bdf0b2cf8dfd2e8afcc89d728ba3f5a0`  
		Size: 1.7 GB (1658081673 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5171ed01a0687a59b2bdf59e2df29a8932abe0ee22a4a6ff6368f8a8295a97d1`  
		Last Modified: Wed, 15 Apr 2020 15:29:42 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a316c4dbc306f67b8ac735d957f87c1afbef1afde59d7b13febb4777781f6eb`  
		Last Modified: Mon, 20 Apr 2020 19:17:03 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e05862ade99bc32c017752427f4eb4ac19437b38181c6900cfed1d6a99d6510`  
		Last Modified: Mon, 20 Apr 2020 19:17:02 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7bdc8ea0d500490783e39f9355fa0349a2d9c32cd29ac8cbdd9a06e848cccda`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f30ae2c8c647fe5e41e956e8cb45d970e0761b0d144aa2a1a1c991f5627caa78`  
		Last Modified: Mon, 20 Apr 2020 19:18:45 GMT  
		Size: 456.5 MB (456490346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2069620de21f9e09ee89665e7488732e9804b4ebabb671846dcc5a2efad828f`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9793d6d47e628c898abbf674bad2cd450299481e89b30f575aac87fc2d186496`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b962b3b43034bdc9d37b9b1a386a2abcdb5b6c8a648d35aa3b46bd884a3c439`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-windowsservercore` - windows version 10.0.17763.1158; amd64

```console
$ docker pull mongo@sha256:98dc02185399f9a980eeac228255f8e42451f535d99c12f71015f176dacbce2f
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2726301729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98407fec53691f82e5cd2eb3a2bda7d93127266f2f6a5f4b7fc5d15a33987224`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Wed, 15 Apr 2020 12:44:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 20 Apr 2020 18:52:33 GMT
ENV MONGO_VERSION=4.2.6
# Mon, 20 Apr 2020 18:52:34 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.6-signed.msi
# Mon, 20 Apr 2020 18:52:35 GMT
ENV MONGO_DOWNLOAD_SHA256=401ebc0c087058cd98194046bbd4fbee243592cf9397f36a1fafa208de4ac21e
# Mon, 20 Apr 2020 19:16:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 20 Apr 2020 19:16:07 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 20 Apr 2020 19:16:08 GMT
EXPOSE 27017
# Mon, 20 Apr 2020 19:16:10 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:442da5a04696895ce6580924a45188bbec9a9db9f81cb7dcef41fc1d4b119130`  
		Last Modified: Wed, 15 Apr 2020 15:29:13 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd1d4721643d80e780c8f74ccda6db920cd5d6702e3a02cecc0a28dc3df2b90`  
		Last Modified: Mon, 20 Apr 2020 19:19:18 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f67966d3a477caf485aaf4080d27615f90dfeed53dd3ba0fd149e65a6b97531`  
		Last Modified: Mon, 20 Apr 2020 19:19:18 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3f18459245d1b377a5dd3fc17087c4c9f225ae47f7e5293f1bd6fca26b0879`  
		Last Modified: Mon, 20 Apr 2020 19:19:15 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff28a577006caf2972aa81e377a6ddbc80a4f337df7c3fc877bc22c875d70b30`  
		Last Modified: Mon, 20 Apr 2020 19:20:11 GMT  
		Size: 455.6 MB (455586654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88cd1efbb2ca082ab8c0e84173075d04be6d252eea7a7f18d961f40e12ac4a0`  
		Last Modified: Mon, 20 Apr 2020 19:19:15 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1eb8768e3e39daa6fe8c5e1c37f5928b6bf0a79e6f13ec87956b42d9e01756d`  
		Last Modified: Mon, 20 Apr 2020 19:19:16 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdc5f1e7a5e65ad06c77f10ba2410b9c07f078d86c597960e5760ad0e398a9d2`  
		Last Modified: Mon, 20 Apr 2020 19:19:15 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4-windowsservercore-1809`

```console
$ docker pull mongo@sha256:a14620e311ff3a231892aeb35aa5b8ec88c6ab01ffda9a0941c4159344f999e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1158; amd64

### `mongo:4-windowsservercore-1809` - windows version 10.0.17763.1158; amd64

```console
$ docker pull mongo@sha256:98dc02185399f9a980eeac228255f8e42451f535d99c12f71015f176dacbce2f
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2726301729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98407fec53691f82e5cd2eb3a2bda7d93127266f2f6a5f4b7fc5d15a33987224`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Wed, 15 Apr 2020 12:44:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 20 Apr 2020 18:52:33 GMT
ENV MONGO_VERSION=4.2.6
# Mon, 20 Apr 2020 18:52:34 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.6-signed.msi
# Mon, 20 Apr 2020 18:52:35 GMT
ENV MONGO_DOWNLOAD_SHA256=401ebc0c087058cd98194046bbd4fbee243592cf9397f36a1fafa208de4ac21e
# Mon, 20 Apr 2020 19:16:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 20 Apr 2020 19:16:07 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 20 Apr 2020 19:16:08 GMT
EXPOSE 27017
# Mon, 20 Apr 2020 19:16:10 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:442da5a04696895ce6580924a45188bbec9a9db9f81cb7dcef41fc1d4b119130`  
		Last Modified: Wed, 15 Apr 2020 15:29:13 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd1d4721643d80e780c8f74ccda6db920cd5d6702e3a02cecc0a28dc3df2b90`  
		Last Modified: Mon, 20 Apr 2020 19:19:18 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f67966d3a477caf485aaf4080d27615f90dfeed53dd3ba0fd149e65a6b97531`  
		Last Modified: Mon, 20 Apr 2020 19:19:18 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3f18459245d1b377a5dd3fc17087c4c9f225ae47f7e5293f1bd6fca26b0879`  
		Last Modified: Mon, 20 Apr 2020 19:19:15 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff28a577006caf2972aa81e377a6ddbc80a4f337df7c3fc877bc22c875d70b30`  
		Last Modified: Mon, 20 Apr 2020 19:20:11 GMT  
		Size: 455.6 MB (455586654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88cd1efbb2ca082ab8c0e84173075d04be6d252eea7a7f18d961f40e12ac4a0`  
		Last Modified: Mon, 20 Apr 2020 19:19:15 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1eb8768e3e39daa6fe8c5e1c37f5928b6bf0a79e6f13ec87956b42d9e01756d`  
		Last Modified: Mon, 20 Apr 2020 19:19:16 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdc5f1e7a5e65ad06c77f10ba2410b9c07f078d86c597960e5760ad0e398a9d2`  
		Last Modified: Mon, 20 Apr 2020 19:19:15 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:05c800b1878e2a6e157c15ac110f83316f73f52e94e5b204c8f1f89acee4477b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3630; amd64

### `mongo:4-windowsservercore-ltsc2016` - windows version 10.0.14393.3630; amd64

```console
$ docker pull mongo@sha256:dd6d940f7a8469cd7ff4d01cf767e861e05ea91c4e01707ea74ed2b633b56f20
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6184565858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fe805e4e3cf7852986e9f6716f85f270946e78bb6585812cc72368454753b47`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Apr 2020 17:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Apr 2020 12:52:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 20 Apr 2020 18:34:28 GMT
ENV MONGO_VERSION=4.2.6
# Mon, 20 Apr 2020 18:34:29 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.6-signed.msi
# Mon, 20 Apr 2020 18:34:30 GMT
ENV MONGO_DOWNLOAD_SHA256=401ebc0c087058cd98194046bbd4fbee243592cf9397f36a1fafa208de4ac21e
# Mon, 20 Apr 2020 18:52:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 20 Apr 2020 18:52:25 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 20 Apr 2020 18:52:26 GMT
EXPOSE 27017
# Mon, 20 Apr 2020 18:52:27 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d0099407ec8ccaf0472e55152e38b262bdf0b2cf8dfd2e8afcc89d728ba3f5a0`  
		Size: 1.7 GB (1658081673 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5171ed01a0687a59b2bdf59e2df29a8932abe0ee22a4a6ff6368f8a8295a97d1`  
		Last Modified: Wed, 15 Apr 2020 15:29:42 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a316c4dbc306f67b8ac735d957f87c1afbef1afde59d7b13febb4777781f6eb`  
		Last Modified: Mon, 20 Apr 2020 19:17:03 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e05862ade99bc32c017752427f4eb4ac19437b38181c6900cfed1d6a99d6510`  
		Last Modified: Mon, 20 Apr 2020 19:17:02 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7bdc8ea0d500490783e39f9355fa0349a2d9c32cd29ac8cbdd9a06e848cccda`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f30ae2c8c647fe5e41e956e8cb45d970e0761b0d144aa2a1a1c991f5627caa78`  
		Last Modified: Mon, 20 Apr 2020 19:18:45 GMT  
		Size: 456.5 MB (456490346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2069620de21f9e09ee89665e7488732e9804b4ebabb671846dcc5a2efad828f`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9793d6d47e628c898abbf674bad2cd450299481e89b30f575aac87fc2d186496`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b962b3b43034bdc9d37b9b1a386a2abcdb5b6c8a648d35aa3b46bd884a3c439`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:bionic`

```console
$ docker pull mongo@sha256:e4abccb1677a976b66d2c726586fc40a073aa3ce4fc5ef6bbc18267e3394d19c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `mongo:bionic` - linux; amd64

```console
$ docker pull mongo@sha256:18f7e39575cd12e9177017ddaa4bcb6c3bae1f6468f3922dc1ecd0662e10281c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164652772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e9495ea1bc639197bc40aef2beedf931078003d8933fb38240f3a1a63c90119`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 20 Mar 2020 19:20:20 GMT
ADD file:594fa35cf803361e69d817fc867b6a4069c064ffd20ed50caf42ad9bb11ca999 in / 
# Fri, 20 Mar 2020 19:20:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 20 Mar 2020 19:20:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 20 Mar 2020 19:20:22 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 20 Mar 2020 19:20:22 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2020 20:49:50 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 20 Mar 2020 20:49:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 16:53:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 17 Apr 2020 16:53:54 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 17 Apr 2020 16:54:10 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 17 Apr 2020 16:54:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 17 Apr 2020 16:54:11 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 17 Apr 2020 16:54:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 17 Apr 2020 16:54:12 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 17 Apr 2020 16:54:13 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 17 Apr 2020 16:54:13 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 17 Apr 2020 16:54:13 GMT
ENV MONGO_MAJOR=4.2
# Mon, 20 Apr 2020 17:44:11 GMT
ENV MONGO_VERSION=4.2.6
# Mon, 20 Apr 2020 17:44:12 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Mon, 20 Apr 2020 17:44:40 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Mon, 20 Apr 2020 17:44:41 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Mon, 20 Apr 2020 17:44:41 GMT
VOLUME [/data/db /data/configdb]
# Mon, 20 Apr 2020 17:44:41 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Mon, 20 Apr 2020 17:44:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2020 17:44:42 GMT
EXPOSE 27017
# Mon, 20 Apr 2020 17:44:42 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:5bed26d33875e6da1d9ff9a1054c5fef3bbeb22ee979e14b72acf72528de007b`  
		Last Modified: Thu, 12 Mar 2020 13:21:29 GMT  
		Size: 26.7 MB (26690587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f11b29a9c7306674a9479158c1b4259938af11b97359d9ac02030cc1095e9ed1`  
		Last Modified: Fri, 20 Mar 2020 19:21:18 GMT  
		Size: 35.4 KB (35372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:930bda195c84cf132344bf38edcad255317382f910503fef234a9ce3bff0f4dd`  
		Last Modified: Fri, 20 Mar 2020 19:21:18 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78bf9a5ad49e4ae42a83f4995ade4efc096f78fd38299cf05bc041e8cdda2a36`  
		Last Modified: Fri, 20 Mar 2020 19:21:18 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7fb3809884c8771103b4475a778eb0a14b736d5f2008d7ef534950c9b6b77d`  
		Last Modified: Fri, 20 Mar 2020 20:50:51 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7237292ff8a2ff64ff0898dc8792b23e5abe90bf32d14f0d4d9eb6ab9e956dd`  
		Last Modified: Fri, 20 Mar 2020 20:50:50 GMT  
		Size: 3.0 MB (2982755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cdf1eb96f71308e6f5be52c3f5278ff6de496b971e1a94d6adb60fc52b2835f`  
		Last Modified: Fri, 17 Apr 2020 16:55:51 GMT  
		Size: 5.8 MB (5824593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39c254c62945d89e0d0e07c721ca9da0ee5848ace6fd9ce95f719a6b721c2be`  
		Last Modified: Fri, 17 Apr 2020 16:55:49 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:110f77aab367a0f38f766fa5d307186a68fdd7483177e20a62c2eee431fb244d`  
		Last Modified: Fri, 17 Apr 2020 16:55:48 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6bec5ffc4eadbe0fa6b84373fe7eaed47c67d2a505a1c640f7cc79c84b5278`  
		Last Modified: Mon, 20 Apr 2020 17:45:00 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d994803edb5bbd3b979490f3ccbe46fc0977dc6fb469fab88fccc9115d0675`  
		Last Modified: Mon, 20 Apr 2020 17:45:27 GMT  
		Size: 129.1 MB (129110699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4266b1dcdabb8fe88172e362ae653d5564293bcd065b45dba2a8e765b4902ab9`  
		Last Modified: Mon, 20 Apr 2020 17:45:00 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3143b095bd39dff0535f074d233459b67c33b68bf2bd7f6d69220bae208a8cac`  
		Last Modified: Mon, 20 Apr 2020 17:45:00 GMT  
		Size: 4.0 KB (3952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:bionic` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:25821e16c7c401986caa09fba3be08b103203a1599edaba8cd34366903b4b3e6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154693716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c06ecd9c0f139339bf92dbef6e630dca8acc4265b72752f7d7b37e16786ed8d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

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
# Fri, 24 Apr 2020 16:18:50 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Apr 2020 16:19:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 16:19:09 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 16:19:09 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Apr 2020 16:19:31 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 16:19:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 16:19:33 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 24 Apr 2020 16:19:35 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 16:19:36 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Apr 2020 16:19:37 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 16:19:37 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 16:19:38 GMT
ENV MONGO_MAJOR=4.2
# Fri, 24 Apr 2020 16:19:38 GMT
ENV MONGO_VERSION=4.2.6
# Fri, 24 Apr 2020 16:19:40 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Apr 2020 16:20:06 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Apr 2020 16:20:09 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Apr 2020 16:20:10 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Apr 2020 16:20:10 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Apr 2020 16:20:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 16:20:11 GMT
EXPOSE 27017
# Fri, 24 Apr 2020 16:20:12 GMT
CMD ["mongod"]
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
	-	`sha256:d1a8d1af89634c78002ec70ef345dd88801eff1bbca938f85fc7472acf873b32`  
		Last Modified: Fri, 24 Apr 2020 16:21:43 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c03832d333b77fecdaaf76768c24a0c6797373a576bd7fb9abc41f3e3e5e2e4`  
		Last Modified: Fri, 24 Apr 2020 16:21:43 GMT  
		Size: 2.7 MB (2675928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544b6736a2d19b775007ab26e1c72ee2e84911c375eec60ec697fe5e8deca69f`  
		Last Modified: Fri, 24 Apr 2020 16:21:44 GMT  
		Size: 5.3 MB (5345352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920aac5b0c675d956885986db6ac84f954ff2f6a98df26a133ae89ae619cd5be`  
		Last Modified: Fri, 24 Apr 2020 16:21:42 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d53bf51618735c85e240ace69cf43a38a4077593fb9b4633fc1d85d2e655016`  
		Last Modified: Fri, 24 Apr 2020 16:21:41 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5296ff1757ed119711f3cc049cb72f1f77178850e6ba2efc6cb0d1e9e1687bdf`  
		Last Modified: Fri, 24 Apr 2020 16:21:41 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7697b84404da018afccd718c3454ed04a6ee05110f0d573a5d73e25a5c5cd75c`  
		Last Modified: Fri, 24 Apr 2020 16:22:09 GMT  
		Size: 122.9 MB (122907968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458af224982cf3028e9a2a89e362caa3e795382c0448adc60b4ab96bedbcc1ef`  
		Last Modified: Fri, 24 Apr 2020 16:21:41 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7506dcffce0af812ecd82776f582f438856fd75e7f948fa2a689a841eaf272e0`  
		Last Modified: Fri, 24 Apr 2020 16:21:41 GMT  
		Size: 4.0 KB (3955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:bionic` - linux; s390x

```console
$ docker pull mongo@sha256:9a853858232155d691db93ab8ab614ad4636f9465aaab10dad522c6ffdbb6fd5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160626574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb6080841c0f9e130ab30d755a2610d8101b8b45a55cfbce1852edce8e90e15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 23 Apr 2020 17:52:20 GMT
ADD file:ea66ef2a01c547f771866bfa221969f8a30489c28d2a81be8dde7f40e73da33b in / 
# Thu, 23 Apr 2020 17:52:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 17:52:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 17:52:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 17:52:31 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 07:34:44 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Apr 2020 07:34:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 07:34:51 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 07:34:51 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Apr 2020 07:35:02 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 07:35:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 07:35:03 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 24 Apr 2020 07:35:09 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 07:35:10 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Apr 2020 07:35:10 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 07:35:10 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 07:35:11 GMT
ENV MONGO_MAJOR=4.2
# Fri, 24 Apr 2020 07:35:11 GMT
ENV MONGO_VERSION=4.2.6
# Fri, 24 Apr 2020 07:35:12 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Apr 2020 07:35:33 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Apr 2020 07:35:38 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Apr 2020 07:35:38 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Apr 2020 07:35:38 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Apr 2020 07:35:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 07:35:39 GMT
EXPOSE 27017
# Fri, 24 Apr 2020 07:35:39 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:13b4c2e4bb97a2a80bb0e557eeba41e4adea0f5e18352e359bca3f847193899c`  
		Last Modified: Mon, 06 Apr 2020 15:41:16 GMT  
		Size: 25.4 MB (25365338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:471a80e39fb485b86610de915eaaad3d867cc97e460b6da3bb656e03520e8a63`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 36.2 KB (36171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb0c128ddabc6a980ec71426ade04fc9bba2e1afcdc243e2d09c316b635f814`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678052ac148ee123df2f0773eb3a0f5f90490ada8b9a5705363b18a2f45fbe88`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c464d6728e9ac439c8d2dc10a88d64a54c34ac50926c66cb7b6d12e37b15d6`  
		Last Modified: Fri, 24 Apr 2020 07:36:04 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd364a38efacff4956ad8e4082d7fa9593aa0a036757fdfbe97487eb26ea2c9`  
		Last Modified: Fri, 24 Apr 2020 07:36:03 GMT  
		Size: 2.7 MB (2714610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e788a62ef53016c8add2417fa25e2141e1b7293acd648f26ed2ddffd54e605b`  
		Last Modified: Fri, 24 Apr 2020 07:36:02 GMT  
		Size: 5.7 MB (5744825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e103dac172d8152c577b2075cc90e6b674188775064cccfbbbc84d93979b3e56`  
		Last Modified: Fri, 24 Apr 2020 07:36:00 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:259fb52c1ef634a5a074adebdaa3f4fc95e636e570c5719c5d662babed85392e`  
		Last Modified: Fri, 24 Apr 2020 07:35:59 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f95c28bb62ddcdbb79cc6870d5cd9701c912a6307bde4c657e1d0c619430fab`  
		Last Modified: Fri, 24 Apr 2020 07:35:58 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05cea8c1238e8ec47654f290d7a566d006d9302762e741316cd236b909d4577d`  
		Last Modified: Fri, 24 Apr 2020 07:36:18 GMT  
		Size: 126.8 MB (126756767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a873535c8ae6f6827fe3d880ab25b1cc404dc3b74898d2ca9bff17136b83caba`  
		Last Modified: Fri, 24 Apr 2020 07:36:04 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d64c0289b5d5c3ee9e04955ed738543e81fdae4e1a43328fd4d88be18d402b`  
		Last Modified: Fri, 24 Apr 2020 07:36:30 GMT  
		Size: 4.0 KB (3954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:latest`

```console
$ docker pull mongo@sha256:7663173f07cf97589989d0c9e15015737cf328618cc4d466fc6c9eddd838ac72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x
	-	windows version 10.0.14393.3630; amd64
	-	windows version 10.0.17763.1158; amd64

### `mongo:latest` - linux; amd64

```console
$ docker pull mongo@sha256:18f7e39575cd12e9177017ddaa4bcb6c3bae1f6468f3922dc1ecd0662e10281c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164652772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e9495ea1bc639197bc40aef2beedf931078003d8933fb38240f3a1a63c90119`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 20 Mar 2020 19:20:20 GMT
ADD file:594fa35cf803361e69d817fc867b6a4069c064ffd20ed50caf42ad9bb11ca999 in / 
# Fri, 20 Mar 2020 19:20:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 20 Mar 2020 19:20:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 20 Mar 2020 19:20:22 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 20 Mar 2020 19:20:22 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2020 20:49:50 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 20 Mar 2020 20:49:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 17 Apr 2020 16:53:54 GMT
ENV GOSU_VERSION=1.12
# Fri, 17 Apr 2020 16:53:54 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 17 Apr 2020 16:54:10 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 17 Apr 2020 16:54:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 17 Apr 2020 16:54:11 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 17 Apr 2020 16:54:12 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 17 Apr 2020 16:54:12 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 17 Apr 2020 16:54:13 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 17 Apr 2020 16:54:13 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 17 Apr 2020 16:54:13 GMT
ENV MONGO_MAJOR=4.2
# Mon, 20 Apr 2020 17:44:11 GMT
ENV MONGO_VERSION=4.2.6
# Mon, 20 Apr 2020 17:44:12 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Mon, 20 Apr 2020 17:44:40 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Mon, 20 Apr 2020 17:44:41 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Mon, 20 Apr 2020 17:44:41 GMT
VOLUME [/data/db /data/configdb]
# Mon, 20 Apr 2020 17:44:41 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Mon, 20 Apr 2020 17:44:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 20 Apr 2020 17:44:42 GMT
EXPOSE 27017
# Mon, 20 Apr 2020 17:44:42 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:5bed26d33875e6da1d9ff9a1054c5fef3bbeb22ee979e14b72acf72528de007b`  
		Last Modified: Thu, 12 Mar 2020 13:21:29 GMT  
		Size: 26.7 MB (26690587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f11b29a9c7306674a9479158c1b4259938af11b97359d9ac02030cc1095e9ed1`  
		Last Modified: Fri, 20 Mar 2020 19:21:18 GMT  
		Size: 35.4 KB (35372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:930bda195c84cf132344bf38edcad255317382f910503fef234a9ce3bff0f4dd`  
		Last Modified: Fri, 20 Mar 2020 19:21:18 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78bf9a5ad49e4ae42a83f4995ade4efc096f78fd38299cf05bc041e8cdda2a36`  
		Last Modified: Fri, 20 Mar 2020 19:21:18 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7fb3809884c8771103b4475a778eb0a14b736d5f2008d7ef534950c9b6b77d`  
		Last Modified: Fri, 20 Mar 2020 20:50:51 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7237292ff8a2ff64ff0898dc8792b23e5abe90bf32d14f0d4d9eb6ab9e956dd`  
		Last Modified: Fri, 20 Mar 2020 20:50:50 GMT  
		Size: 3.0 MB (2982755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cdf1eb96f71308e6f5be52c3f5278ff6de496b971e1a94d6adb60fc52b2835f`  
		Last Modified: Fri, 17 Apr 2020 16:55:51 GMT  
		Size: 5.8 MB (5824593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39c254c62945d89e0d0e07c721ca9da0ee5848ace6fd9ce95f719a6b721c2be`  
		Last Modified: Fri, 17 Apr 2020 16:55:49 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:110f77aab367a0f38f766fa5d307186a68fdd7483177e20a62c2eee431fb244d`  
		Last Modified: Fri, 17 Apr 2020 16:55:48 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6bec5ffc4eadbe0fa6b84373fe7eaed47c67d2a505a1c640f7cc79c84b5278`  
		Last Modified: Mon, 20 Apr 2020 17:45:00 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d994803edb5bbd3b979490f3ccbe46fc0977dc6fb469fab88fccc9115d0675`  
		Last Modified: Mon, 20 Apr 2020 17:45:27 GMT  
		Size: 129.1 MB (129110699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4266b1dcdabb8fe88172e362ae653d5564293bcd065b45dba2a8e765b4902ab9`  
		Last Modified: Mon, 20 Apr 2020 17:45:00 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3143b095bd39dff0535f074d233459b67c33b68bf2bd7f6d69220bae208a8cac`  
		Last Modified: Mon, 20 Apr 2020 17:45:00 GMT  
		Size: 4.0 KB (3952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:25821e16c7c401986caa09fba3be08b103203a1599edaba8cd34366903b4b3e6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154693716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c06ecd9c0f139339bf92dbef6e630dca8acc4265b72752f7d7b37e16786ed8d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

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
# Fri, 24 Apr 2020 16:18:50 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Apr 2020 16:19:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 16:19:09 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 16:19:09 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Apr 2020 16:19:31 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 16:19:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 16:19:33 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 24 Apr 2020 16:19:35 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 16:19:36 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Apr 2020 16:19:37 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 16:19:37 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 16:19:38 GMT
ENV MONGO_MAJOR=4.2
# Fri, 24 Apr 2020 16:19:38 GMT
ENV MONGO_VERSION=4.2.6
# Fri, 24 Apr 2020 16:19:40 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Apr 2020 16:20:06 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Apr 2020 16:20:09 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Apr 2020 16:20:10 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Apr 2020 16:20:10 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Apr 2020 16:20:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 16:20:11 GMT
EXPOSE 27017
# Fri, 24 Apr 2020 16:20:12 GMT
CMD ["mongod"]
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
	-	`sha256:d1a8d1af89634c78002ec70ef345dd88801eff1bbca938f85fc7472acf873b32`  
		Last Modified: Fri, 24 Apr 2020 16:21:43 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c03832d333b77fecdaaf76768c24a0c6797373a576bd7fb9abc41f3e3e5e2e4`  
		Last Modified: Fri, 24 Apr 2020 16:21:43 GMT  
		Size: 2.7 MB (2675928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544b6736a2d19b775007ab26e1c72ee2e84911c375eec60ec697fe5e8deca69f`  
		Last Modified: Fri, 24 Apr 2020 16:21:44 GMT  
		Size: 5.3 MB (5345352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920aac5b0c675d956885986db6ac84f954ff2f6a98df26a133ae89ae619cd5be`  
		Last Modified: Fri, 24 Apr 2020 16:21:42 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d53bf51618735c85e240ace69cf43a38a4077593fb9b4633fc1d85d2e655016`  
		Last Modified: Fri, 24 Apr 2020 16:21:41 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5296ff1757ed119711f3cc049cb72f1f77178850e6ba2efc6cb0d1e9e1687bdf`  
		Last Modified: Fri, 24 Apr 2020 16:21:41 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7697b84404da018afccd718c3454ed04a6ee05110f0d573a5d73e25a5c5cd75c`  
		Last Modified: Fri, 24 Apr 2020 16:22:09 GMT  
		Size: 122.9 MB (122907968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458af224982cf3028e9a2a89e362caa3e795382c0448adc60b4ab96bedbcc1ef`  
		Last Modified: Fri, 24 Apr 2020 16:21:41 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7506dcffce0af812ecd82776f582f438856fd75e7f948fa2a689a841eaf272e0`  
		Last Modified: Fri, 24 Apr 2020 16:21:41 GMT  
		Size: 4.0 KB (3955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - linux; s390x

```console
$ docker pull mongo@sha256:9a853858232155d691db93ab8ab614ad4636f9465aaab10dad522c6ffdbb6fd5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160626574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb6080841c0f9e130ab30d755a2610d8101b8b45a55cfbce1852edce8e90e15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 23 Apr 2020 17:52:20 GMT
ADD file:ea66ef2a01c547f771866bfa221969f8a30489c28d2a81be8dde7f40e73da33b in / 
# Thu, 23 Apr 2020 17:52:26 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 23 Apr 2020 17:52:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 23 Apr 2020 17:52:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 23 Apr 2020 17:52:31 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2020 07:34:44 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 24 Apr 2020 07:34:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 07:34:51 GMT
ENV GOSU_VERSION=1.12
# Fri, 24 Apr 2020 07:34:51 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 24 Apr 2020 07:35:02 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 24 Apr 2020 07:35:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 24 Apr 2020 07:35:03 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 24 Apr 2020 07:35:09 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 24 Apr 2020 07:35:10 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 24 Apr 2020 07:35:10 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 07:35:10 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 24 Apr 2020 07:35:11 GMT
ENV MONGO_MAJOR=4.2
# Fri, 24 Apr 2020 07:35:11 GMT
ENV MONGO_VERSION=4.2.6
# Fri, 24 Apr 2020 07:35:12 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 24 Apr 2020 07:35:33 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 24 Apr 2020 07:35:38 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 24 Apr 2020 07:35:38 GMT
VOLUME [/data/db /data/configdb]
# Fri, 24 Apr 2020 07:35:38 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 24 Apr 2020 07:35:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Apr 2020 07:35:39 GMT
EXPOSE 27017
# Fri, 24 Apr 2020 07:35:39 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:13b4c2e4bb97a2a80bb0e557eeba41e4adea0f5e18352e359bca3f847193899c`  
		Last Modified: Mon, 06 Apr 2020 15:41:16 GMT  
		Size: 25.4 MB (25365338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:471a80e39fb485b86610de915eaaad3d867cc97e460b6da3bb656e03520e8a63`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 36.2 KB (36171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb0c128ddabc6a980ec71426ade04fc9bba2e1afcdc243e2d09c316b635f814`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678052ac148ee123df2f0773eb3a0f5f90490ada8b9a5705363b18a2f45fbe88`  
		Last Modified: Thu, 23 Apr 2020 17:54:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c464d6728e9ac439c8d2dc10a88d64a54c34ac50926c66cb7b6d12e37b15d6`  
		Last Modified: Fri, 24 Apr 2020 07:36:04 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd364a38efacff4956ad8e4082d7fa9593aa0a036757fdfbe97487eb26ea2c9`  
		Last Modified: Fri, 24 Apr 2020 07:36:03 GMT  
		Size: 2.7 MB (2714610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e788a62ef53016c8add2417fa25e2141e1b7293acd648f26ed2ddffd54e605b`  
		Last Modified: Fri, 24 Apr 2020 07:36:02 GMT  
		Size: 5.7 MB (5744825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e103dac172d8152c577b2075cc90e6b674188775064cccfbbbc84d93979b3e56`  
		Last Modified: Fri, 24 Apr 2020 07:36:00 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:259fb52c1ef634a5a074adebdaa3f4fc95e636e570c5719c5d662babed85392e`  
		Last Modified: Fri, 24 Apr 2020 07:35:59 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f95c28bb62ddcdbb79cc6870d5cd9701c912a6307bde4c657e1d0c619430fab`  
		Last Modified: Fri, 24 Apr 2020 07:35:58 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05cea8c1238e8ec47654f290d7a566d006d9302762e741316cd236b909d4577d`  
		Last Modified: Fri, 24 Apr 2020 07:36:18 GMT  
		Size: 126.8 MB (126756767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a873535c8ae6f6827fe3d880ab25b1cc404dc3b74898d2ca9bff17136b83caba`  
		Last Modified: Fri, 24 Apr 2020 07:36:04 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d64c0289b5d5c3ee9e04955ed738543e81fdae4e1a43328fd4d88be18d402b`  
		Last Modified: Fri, 24 Apr 2020 07:36:30 GMT  
		Size: 4.0 KB (3954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.14393.3630; amd64

```console
$ docker pull mongo@sha256:dd6d940f7a8469cd7ff4d01cf767e861e05ea91c4e01707ea74ed2b633b56f20
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6184565858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fe805e4e3cf7852986e9f6716f85f270946e78bb6585812cc72368454753b47`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Apr 2020 17:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Apr 2020 12:52:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 20 Apr 2020 18:34:28 GMT
ENV MONGO_VERSION=4.2.6
# Mon, 20 Apr 2020 18:34:29 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.6-signed.msi
# Mon, 20 Apr 2020 18:34:30 GMT
ENV MONGO_DOWNLOAD_SHA256=401ebc0c087058cd98194046bbd4fbee243592cf9397f36a1fafa208de4ac21e
# Mon, 20 Apr 2020 18:52:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 20 Apr 2020 18:52:25 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 20 Apr 2020 18:52:26 GMT
EXPOSE 27017
# Mon, 20 Apr 2020 18:52:27 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d0099407ec8ccaf0472e55152e38b262bdf0b2cf8dfd2e8afcc89d728ba3f5a0`  
		Size: 1.7 GB (1658081673 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5171ed01a0687a59b2bdf59e2df29a8932abe0ee22a4a6ff6368f8a8295a97d1`  
		Last Modified: Wed, 15 Apr 2020 15:29:42 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a316c4dbc306f67b8ac735d957f87c1afbef1afde59d7b13febb4777781f6eb`  
		Last Modified: Mon, 20 Apr 2020 19:17:03 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e05862ade99bc32c017752427f4eb4ac19437b38181c6900cfed1d6a99d6510`  
		Last Modified: Mon, 20 Apr 2020 19:17:02 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7bdc8ea0d500490783e39f9355fa0349a2d9c32cd29ac8cbdd9a06e848cccda`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f30ae2c8c647fe5e41e956e8cb45d970e0761b0d144aa2a1a1c991f5627caa78`  
		Last Modified: Mon, 20 Apr 2020 19:18:45 GMT  
		Size: 456.5 MB (456490346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2069620de21f9e09ee89665e7488732e9804b4ebabb671846dcc5a2efad828f`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9793d6d47e628c898abbf674bad2cd450299481e89b30f575aac87fc2d186496`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b962b3b43034bdc9d37b9b1a386a2abcdb5b6c8a648d35aa3b46bd884a3c439`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.17763.1158; amd64

```console
$ docker pull mongo@sha256:98dc02185399f9a980eeac228255f8e42451f535d99c12f71015f176dacbce2f
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2726301729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98407fec53691f82e5cd2eb3a2bda7d93127266f2f6a5f4b7fc5d15a33987224`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Wed, 15 Apr 2020 12:44:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 20 Apr 2020 18:52:33 GMT
ENV MONGO_VERSION=4.2.6
# Mon, 20 Apr 2020 18:52:34 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.6-signed.msi
# Mon, 20 Apr 2020 18:52:35 GMT
ENV MONGO_DOWNLOAD_SHA256=401ebc0c087058cd98194046bbd4fbee243592cf9397f36a1fafa208de4ac21e
# Mon, 20 Apr 2020 19:16:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 20 Apr 2020 19:16:07 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 20 Apr 2020 19:16:08 GMT
EXPOSE 27017
# Mon, 20 Apr 2020 19:16:10 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:442da5a04696895ce6580924a45188bbec9a9db9f81cb7dcef41fc1d4b119130`  
		Last Modified: Wed, 15 Apr 2020 15:29:13 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd1d4721643d80e780c8f74ccda6db920cd5d6702e3a02cecc0a28dc3df2b90`  
		Last Modified: Mon, 20 Apr 2020 19:19:18 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f67966d3a477caf485aaf4080d27615f90dfeed53dd3ba0fd149e65a6b97531`  
		Last Modified: Mon, 20 Apr 2020 19:19:18 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3f18459245d1b377a5dd3fc17087c4c9f225ae47f7e5293f1bd6fca26b0879`  
		Last Modified: Mon, 20 Apr 2020 19:19:15 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff28a577006caf2972aa81e377a6ddbc80a4f337df7c3fc877bc22c875d70b30`  
		Last Modified: Mon, 20 Apr 2020 19:20:11 GMT  
		Size: 455.6 MB (455586654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88cd1efbb2ca082ab8c0e84173075d04be6d252eea7a7f18d961f40e12ac4a0`  
		Last Modified: Mon, 20 Apr 2020 19:19:15 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1eb8768e3e39daa6fe8c5e1c37f5928b6bf0a79e6f13ec87956b42d9e01756d`  
		Last Modified: Mon, 20 Apr 2020 19:19:16 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdc5f1e7a5e65ad06c77f10ba2410b9c07f078d86c597960e5760ad0e398a9d2`  
		Last Modified: Mon, 20 Apr 2020 19:19:15 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:windowsservercore`

```console
$ docker pull mongo@sha256:29ca3bea646a83d01e3e25e0046a5c18fe594e2ee511c7dc50a489e282582d80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3630; amd64
	-	windows version 10.0.17763.1158; amd64

### `mongo:windowsservercore` - windows version 10.0.14393.3630; amd64

```console
$ docker pull mongo@sha256:dd6d940f7a8469cd7ff4d01cf767e861e05ea91c4e01707ea74ed2b633b56f20
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6184565858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fe805e4e3cf7852986e9f6716f85f270946e78bb6585812cc72368454753b47`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Apr 2020 17:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Apr 2020 12:52:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 20 Apr 2020 18:34:28 GMT
ENV MONGO_VERSION=4.2.6
# Mon, 20 Apr 2020 18:34:29 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.6-signed.msi
# Mon, 20 Apr 2020 18:34:30 GMT
ENV MONGO_DOWNLOAD_SHA256=401ebc0c087058cd98194046bbd4fbee243592cf9397f36a1fafa208de4ac21e
# Mon, 20 Apr 2020 18:52:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 20 Apr 2020 18:52:25 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 20 Apr 2020 18:52:26 GMT
EXPOSE 27017
# Mon, 20 Apr 2020 18:52:27 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d0099407ec8ccaf0472e55152e38b262bdf0b2cf8dfd2e8afcc89d728ba3f5a0`  
		Size: 1.7 GB (1658081673 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5171ed01a0687a59b2bdf59e2df29a8932abe0ee22a4a6ff6368f8a8295a97d1`  
		Last Modified: Wed, 15 Apr 2020 15:29:42 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a316c4dbc306f67b8ac735d957f87c1afbef1afde59d7b13febb4777781f6eb`  
		Last Modified: Mon, 20 Apr 2020 19:17:03 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e05862ade99bc32c017752427f4eb4ac19437b38181c6900cfed1d6a99d6510`  
		Last Modified: Mon, 20 Apr 2020 19:17:02 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7bdc8ea0d500490783e39f9355fa0349a2d9c32cd29ac8cbdd9a06e848cccda`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f30ae2c8c647fe5e41e956e8cb45d970e0761b0d144aa2a1a1c991f5627caa78`  
		Last Modified: Mon, 20 Apr 2020 19:18:45 GMT  
		Size: 456.5 MB (456490346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2069620de21f9e09ee89665e7488732e9804b4ebabb671846dcc5a2efad828f`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9793d6d47e628c898abbf674bad2cd450299481e89b30f575aac87fc2d186496`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b962b3b43034bdc9d37b9b1a386a2abcdb5b6c8a648d35aa3b46bd884a3c439`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:windowsservercore` - windows version 10.0.17763.1158; amd64

```console
$ docker pull mongo@sha256:98dc02185399f9a980eeac228255f8e42451f535d99c12f71015f176dacbce2f
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2726301729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98407fec53691f82e5cd2eb3a2bda7d93127266f2f6a5f4b7fc5d15a33987224`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Wed, 15 Apr 2020 12:44:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 20 Apr 2020 18:52:33 GMT
ENV MONGO_VERSION=4.2.6
# Mon, 20 Apr 2020 18:52:34 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.6-signed.msi
# Mon, 20 Apr 2020 18:52:35 GMT
ENV MONGO_DOWNLOAD_SHA256=401ebc0c087058cd98194046bbd4fbee243592cf9397f36a1fafa208de4ac21e
# Mon, 20 Apr 2020 19:16:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 20 Apr 2020 19:16:07 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 20 Apr 2020 19:16:08 GMT
EXPOSE 27017
# Mon, 20 Apr 2020 19:16:10 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:442da5a04696895ce6580924a45188bbec9a9db9f81cb7dcef41fc1d4b119130`  
		Last Modified: Wed, 15 Apr 2020 15:29:13 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd1d4721643d80e780c8f74ccda6db920cd5d6702e3a02cecc0a28dc3df2b90`  
		Last Modified: Mon, 20 Apr 2020 19:19:18 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f67966d3a477caf485aaf4080d27615f90dfeed53dd3ba0fd149e65a6b97531`  
		Last Modified: Mon, 20 Apr 2020 19:19:18 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3f18459245d1b377a5dd3fc17087c4c9f225ae47f7e5293f1bd6fca26b0879`  
		Last Modified: Mon, 20 Apr 2020 19:19:15 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff28a577006caf2972aa81e377a6ddbc80a4f337df7c3fc877bc22c875d70b30`  
		Last Modified: Mon, 20 Apr 2020 19:20:11 GMT  
		Size: 455.6 MB (455586654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88cd1efbb2ca082ab8c0e84173075d04be6d252eea7a7f18d961f40e12ac4a0`  
		Last Modified: Mon, 20 Apr 2020 19:19:15 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1eb8768e3e39daa6fe8c5e1c37f5928b6bf0a79e6f13ec87956b42d9e01756d`  
		Last Modified: Mon, 20 Apr 2020 19:19:16 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdc5f1e7a5e65ad06c77f10ba2410b9c07f078d86c597960e5760ad0e398a9d2`  
		Last Modified: Mon, 20 Apr 2020 19:19:15 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:windowsservercore-1809`

```console
$ docker pull mongo@sha256:a14620e311ff3a231892aeb35aa5b8ec88c6ab01ffda9a0941c4159344f999e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1158; amd64

### `mongo:windowsservercore-1809` - windows version 10.0.17763.1158; amd64

```console
$ docker pull mongo@sha256:98dc02185399f9a980eeac228255f8e42451f535d99c12f71015f176dacbce2f
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2726301729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98407fec53691f82e5cd2eb3a2bda7d93127266f2f6a5f4b7fc5d15a33987224`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Apr 2020 03:38:38 GMT
RUN Install update 1809-amd64
# Wed, 15 Apr 2020 12:44:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 20 Apr 2020 18:52:33 GMT
ENV MONGO_VERSION=4.2.6
# Mon, 20 Apr 2020 18:52:34 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.6-signed.msi
# Mon, 20 Apr 2020 18:52:35 GMT
ENV MONGO_DOWNLOAD_SHA256=401ebc0c087058cd98194046bbd4fbee243592cf9397f36a1fafa208de4ac21e
# Mon, 20 Apr 2020 19:16:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 20 Apr 2020 19:16:07 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 20 Apr 2020 19:16:08 GMT
EXPOSE 27017
# Mon, 20 Apr 2020 19:16:10 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:eac6fba788c9781d6f989eb0932cb33bf72c2cce4eb234cc6decdcab89e183bc`  
		Size: 736.0 MB (736021953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:442da5a04696895ce6580924a45188bbec9a9db9f81cb7dcef41fc1d4b119130`  
		Last Modified: Wed, 15 Apr 2020 15:29:13 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd1d4721643d80e780c8f74ccda6db920cd5d6702e3a02cecc0a28dc3df2b90`  
		Last Modified: Mon, 20 Apr 2020 19:19:18 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f67966d3a477caf485aaf4080d27615f90dfeed53dd3ba0fd149e65a6b97531`  
		Last Modified: Mon, 20 Apr 2020 19:19:18 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3f18459245d1b377a5dd3fc17087c4c9f225ae47f7e5293f1bd6fca26b0879`  
		Last Modified: Mon, 20 Apr 2020 19:19:15 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff28a577006caf2972aa81e377a6ddbc80a4f337df7c3fc877bc22c875d70b30`  
		Last Modified: Mon, 20 Apr 2020 19:20:11 GMT  
		Size: 455.6 MB (455586654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88cd1efbb2ca082ab8c0e84173075d04be6d252eea7a7f18d961f40e12ac4a0`  
		Last Modified: Mon, 20 Apr 2020 19:19:15 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1eb8768e3e39daa6fe8c5e1c37f5928b6bf0a79e6f13ec87956b42d9e01756d`  
		Last Modified: Mon, 20 Apr 2020 19:19:16 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdc5f1e7a5e65ad06c77f10ba2410b9c07f078d86c597960e5760ad0e398a9d2`  
		Last Modified: Mon, 20 Apr 2020 19:19:15 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:05c800b1878e2a6e157c15ac110f83316f73f52e94e5b204c8f1f89acee4477b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3630; amd64

### `mongo:windowsservercore-ltsc2016` - windows version 10.0.14393.3630; amd64

```console
$ docker pull mongo@sha256:dd6d940f7a8469cd7ff4d01cf767e861e05ea91c4e01707ea74ed2b633b56f20
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6184565858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fe805e4e3cf7852986e9f6716f85f270946e78bb6585812cc72368454753b47`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Apr 2020 17:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Apr 2020 12:52:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 20 Apr 2020 18:34:28 GMT
ENV MONGO_VERSION=4.2.6
# Mon, 20 Apr 2020 18:34:29 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.6-signed.msi
# Mon, 20 Apr 2020 18:34:30 GMT
ENV MONGO_DOWNLOAD_SHA256=401ebc0c087058cd98194046bbd4fbee243592cf9397f36a1fafa208de4ac21e
# Mon, 20 Apr 2020 18:52:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 20 Apr 2020 18:52:25 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 20 Apr 2020 18:52:26 GMT
EXPOSE 27017
# Mon, 20 Apr 2020 18:52:27 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d0099407ec8ccaf0472e55152e38b262bdf0b2cf8dfd2e8afcc89d728ba3f5a0`  
		Size: 1.7 GB (1658081673 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5171ed01a0687a59b2bdf59e2df29a8932abe0ee22a4a6ff6368f8a8295a97d1`  
		Last Modified: Wed, 15 Apr 2020 15:29:42 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a316c4dbc306f67b8ac735d957f87c1afbef1afde59d7b13febb4777781f6eb`  
		Last Modified: Mon, 20 Apr 2020 19:17:03 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e05862ade99bc32c017752427f4eb4ac19437b38181c6900cfed1d6a99d6510`  
		Last Modified: Mon, 20 Apr 2020 19:17:02 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7bdc8ea0d500490783e39f9355fa0349a2d9c32cd29ac8cbdd9a06e848cccda`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f30ae2c8c647fe5e41e956e8cb45d970e0761b0d144aa2a1a1c991f5627caa78`  
		Last Modified: Mon, 20 Apr 2020 19:18:45 GMT  
		Size: 456.5 MB (456490346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2069620de21f9e09ee89665e7488732e9804b4ebabb671846dcc5a2efad828f`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9793d6d47e628c898abbf674bad2cd450299481e89b30f575aac87fc2d186496`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b962b3b43034bdc9d37b9b1a386a2abcdb5b6c8a648d35aa3b46bd884a3c439`  
		Last Modified: Mon, 20 Apr 2020 19:17:00 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
