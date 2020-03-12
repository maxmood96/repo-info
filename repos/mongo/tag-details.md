<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mongo`

-	[`mongo:3`](#mongo3)
-	[`mongo:3.6`](#mongo36)
-	[`mongo:3.6.17`](#mongo3617)
-	[`mongo:3.6.17-windowsservercore`](#mongo3617-windowsservercore)
-	[`mongo:3.6.17-windowsservercore-ltsc2016`](#mongo3617-windowsservercore-ltsc2016)
-	[`mongo:3.6.17-xenial`](#mongo3617-xenial)
-	[`mongo:3.6-windowsservercore`](#mongo36-windowsservercore)
-	[`mongo:3.6-windowsservercore-ltsc2016`](#mongo36-windowsservercore-ltsc2016)
-	[`mongo:3.6-xenial`](#mongo36-xenial)
-	[`mongo:3-windowsservercore`](#mongo3-windowsservercore)
-	[`mongo:3-windowsservercore-ltsc2016`](#mongo3-windowsservercore-ltsc2016)
-	[`mongo:3-xenial`](#mongo3-xenial)
-	[`mongo:4`](#mongo4)
-	[`mongo:4.0`](#mongo40)
-	[`mongo:4.0.16`](#mongo4016)
-	[`mongo:4.0.16-windowsservercore`](#mongo4016-windowsservercore)
-	[`mongo:4.0.16-windowsservercore-1809`](#mongo4016-windowsservercore-1809)
-	[`mongo:4.0.16-windowsservercore-ltsc2016`](#mongo4016-windowsservercore-ltsc2016)
-	[`mongo:4.0.16-xenial`](#mongo4016-xenial)
-	[`mongo:4.0-windowsservercore`](#mongo40-windowsservercore)
-	[`mongo:4.0-windowsservercore-1809`](#mongo40-windowsservercore-1809)
-	[`mongo:4.0-windowsservercore-ltsc2016`](#mongo40-windowsservercore-ltsc2016)
-	[`mongo:4.0-xenial`](#mongo40-xenial)
-	[`mongo:4.2`](#mongo42)
-	[`mongo:4.2.3`](#mongo423)
-	[`mongo:4.2.3-bionic`](#mongo423-bionic)
-	[`mongo:4.2.3-windowsservercore`](#mongo423-windowsservercore)
-	[`mongo:4.2.3-windowsservercore-1809`](#mongo423-windowsservercore-1809)
-	[`mongo:4.2.3-windowsservercore-ltsc2016`](#mongo423-windowsservercore-ltsc2016)
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
$ docker pull mongo@sha256:f1ff4f9fd92c45e545c8a9d726123fc1410e2c53c82e99288edf57da98be4e81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.14393.3506; amd64

### `mongo:3` - linux; amd64

```console
$ docker pull mongo@sha256:557aaf306c611bf9cd04e69fc3174757e2ce25ecc073a88fe28dbc889f5dae9a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.6 MB (165644020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3fdbdf0f17b70466eda08d155b2f1c72bc3450d23b8a752a4a841a83d6eb76f`
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
# Sat, 22 Feb 2020 01:08:24 GMT
ENV GOSU_VERSION=1.11
# Sat, 22 Feb 2020 01:08:24 GMT
ENV JSYAML_VERSION=3.13.0
# Sat, 22 Feb 2020 01:08:40 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 22 Feb 2020 01:08:40 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 22 Feb 2020 01:08:41 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Sat, 22 Feb 2020 01:08:41 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Sat, 22 Feb 2020 01:08:42 GMT
ARG MONGO_PACKAGE=mongodb-org
# Sat, 22 Feb 2020 01:08:42 GMT
ARG MONGO_REPO=repo.mongodb.org
# Sat, 22 Feb 2020 01:08:42 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Sat, 22 Feb 2020 01:08:42 GMT
ENV MONGO_MAJOR=3.6
# Sat, 22 Feb 2020 01:08:42 GMT
ENV MONGO_VERSION=3.6.17
# Sat, 22 Feb 2020 01:08:43 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Sat, 22 Feb 2020 01:09:04 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Sat, 22 Feb 2020 01:09:05 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Sat, 22 Feb 2020 01:09:05 GMT
VOLUME [/data/db /data/configdb]
# Sat, 22 Feb 2020 01:09:05 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Sat, 22 Feb 2020 01:09:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 22 Feb 2020 01:09:06 GMT
EXPOSE 27017
# Sat, 22 Feb 2020 01:09:06 GMT
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
	-	`sha256:7f706fb8c773a1773b04049e2fc1aa9f63e9f8b1ecbaae99fcf970f69c417f18`  
		Last Modified: Sat, 22 Feb 2020 01:11:01 GMT  
		Size: 1.2 MB (1243833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f137797464445cc1df1f6510d063791f41c4be58a91cbde2d7c9e9d5985cab6d`  
		Last Modified: Sat, 22 Feb 2020 01:11:01 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a03380f32ca06a89bb8bbb6437140f7feaa8cbc73656efd413066485af7bed9`  
		Last Modified: Sat, 22 Feb 2020 01:11:00 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a38c136f14bc4cc8e7c8b75a1b58fbd13ee66ab4018835cce5deafd77e34629`  
		Last Modified: Sat, 22 Feb 2020 01:11:00 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0e875b59ceec4323d6455ddef1a97e267ed64e723a3785961db869da21e662`  
		Last Modified: Sat, 22 Feb 2020 01:11:19 GMT  
		Size: 117.3 MB (117252414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f55b4999cd606166300c3bcc0c29bbdb69f9e442f652f9e2a1b037ff63069d`  
		Last Modified: Sat, 22 Feb 2020 01:11:00 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc92ef8de8b080701461ef5a44e3df6e2b20f0e5d0502bc9c2f58fb0c18884c`  
		Last Modified: Sat, 22 Feb 2020 01:11:00 GMT  
		Size: 4.0 KB (3953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:8d00f2129c233839b0192bc63ad1b38d732559eb063a8c7fb6afd9b14000dfe9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155054951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:904d1cc8fa66fbab1604f0f278d0125cf824c48dde0e06e2de53f80f21123a3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 21 Feb 2020 21:55:42 GMT
ADD file:61b91c95a686740a57740470b7a1fe64d2479c56c36c69ca1222d870e78d44cc in / 
# Fri, 21 Feb 2020 21:55:46 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 21:55:48 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:55:50 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:55:50 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:48:01 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 21 Feb 2020 22:48:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:48:17 GMT
ENV GOSU_VERSION=1.11
# Fri, 21 Feb 2020 22:48:19 GMT
ENV JSYAML_VERSION=3.13.0
# Fri, 21 Feb 2020 22:48:47 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 21 Feb 2020 22:48:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:48:51 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Fri, 21 Feb 2020 22:48:53 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:48:54 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 21 Feb 2020 22:48:54 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:48:55 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:48:56 GMT
ENV MONGO_MAJOR=3.6
# Fri, 21 Feb 2020 22:48:57 GMT
ENV MONGO_VERSION=3.6.17
# Fri, 21 Feb 2020 22:48:59 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 21 Feb 2020 22:49:21 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 21 Feb 2020 22:49:23 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 21 Feb 2020 22:49:24 GMT
VOLUME [/data/db /data/configdb]
# Fri, 21 Feb 2020 22:49:24 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:49:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:49:26 GMT
EXPOSE 27017
# Fri, 21 Feb 2020 22:49:27 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a7bab9946de3c22ecccd832a0910adc2ffa82eea53f83c600d5ebce9e5422ad0`  
		Last Modified: Mon, 17 Feb 2020 15:45:27 GMT  
		Size: 39.9 MB (39940373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38630c4d9093f5b60806171ca7fa47a70d7ab28eeed25edfad43fb91d5f9f825`  
		Last Modified: Fri, 21 Feb 2020 21:56:39 GMT  
		Size: 467.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef678cbe74d844c6a114c1158a8c8868b412b7c5ed3a4c159831975a4915db9`  
		Last Modified: Fri, 21 Feb 2020 21:56:39 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78928743b0e778df64b15ac919705702ee0a080c2586f43c4349b35180de3c36`  
		Last Modified: Fri, 21 Feb 2020 21:56:40 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b98e127168243d033826ae375801cd9bde48991cd8c3f70195b2393e612fdd`  
		Last Modified: Fri, 21 Feb 2020 22:52:35 GMT  
		Size: 2.0 KB (1989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd8b81c3e37e64b559f25587bfdcb850b0f99e789d079c3a5e23aedc76a5b133`  
		Last Modified: Fri, 21 Feb 2020 22:52:35 GMT  
		Size: 2.5 MB (2474933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5133614dc076c55be0b03423a8f81053612df19fc888c3a5e65cf096386ca61a`  
		Last Modified: Fri, 21 Feb 2020 22:52:35 GMT  
		Size: 1.2 MB (1170004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa274bfc4efdade7b87ff58757777040775bd689e0478b13c0325ace270c75b`  
		Last Modified: Fri, 21 Feb 2020 22:52:35 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c551726d412935a665a5faa37ba35c6b578c9b4b9a04e15fbb8141e18c469f4`  
		Last Modified: Fri, 21 Feb 2020 22:52:33 GMT  
		Size: 2.0 KB (1995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690416c5e0de4a88eb11a3f888d668dffc71c64ce9928810382a5f989ea0d6d8`  
		Last Modified: Fri, 21 Feb 2020 22:52:33 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466edf90a60ac36b2e4ef9846aac45cf6dcbf6603561ff365607d6ec8e1d4333`  
		Last Modified: Fri, 21 Feb 2020 22:53:01 GMT  
		Size: 111.5 MB (111459661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a78ae9c5bd995e33cabe28ea21119ec5a46c4ecd1c7a5b80beedf81e226048`  
		Last Modified: Fri, 21 Feb 2020 22:52:33 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddfad788e158cc0e6900c305454fae286feb8c8e9807a24c9e4a962a22727dfc`  
		Last Modified: Fri, 21 Feb 2020 22:52:33 GMT  
		Size: 4.0 KB (3953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3` - windows version 10.0.14393.3506; amd64

```console
$ docker pull mongo@sha256:6763381f4a67ddb7df259a4187887006e19ee9253e592ff2bb60c1059bfcdf31
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5820567995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a26b0054534cef77b808f6755003209a9fd4a5056f058edad907cc6c50409ffd`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 05:12:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 20 Feb 2020 05:19:42 GMT
ENV MONGO_VERSION=3.6.17
# Wed, 11 Mar 2020 22:15:37 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.17-signed.msi
# Wed, 11 Mar 2020 22:15:39 GMT
ENV MONGO_DOWNLOAD_SHA256=b20b72d5366a7a00cb85245ebedd01b665bbac4f918dd5fac7a7c5eb68477c26
# Wed, 11 Mar 2020 22:28:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Mar 2020 22:28:24 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Mar 2020 22:28:25 GMT
EXPOSE 27017
# Wed, 11 Mar 2020 22:28:27 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:846a2223e9e7a88a2a07d706553f144d380483d72fb9f0697c4fcd71773a8693`  
		Size: 1.7 GB (1657079102 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0961c48658cd7865bcf6c05285dfbe8ad89cd52059088d7f4eed6fde1bb2b385`  
		Last Modified: Thu, 20 Feb 2020 05:18:25 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4863e5701bfa2388492681880718703eecf4360e943021e702f897bc078de68e`  
		Last Modified: Thu, 20 Feb 2020 05:40:40 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8875ee76ce08286dab2e650f9808e785bc0f79acb4c15382048735765497b07`  
		Last Modified: Wed, 11 Mar 2020 23:38:14 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dffa284f8065be9eb03e643bb9dd50a603c5b6e8813bb0d4ddb7e75987fc5b4d`  
		Last Modified: Wed, 11 Mar 2020 23:38:09 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae68ba460a8f3dc989becee8ef2d59e650742bc77ba74a98d0c8e12ace493d19`  
		Last Modified: Wed, 11 Mar 2020 23:38:54 GMT  
		Size: 93.5 MB (93494538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead5918efa91f150d4991d381d85158e23cdab0f832fd73a318fb4af300348d1`  
		Last Modified: Wed, 11 Mar 2020 23:38:09 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b8dc5e80e6329a94b954cc8673d91fa2222d35ee9569178e1e0502c6ed2d14`  
		Last Modified: Wed, 11 Mar 2020 23:38:10 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a47d981e96991c1baf1c50d2090a8accbe1a377c893fd4d7aa22e580bb24e35`  
		Last Modified: Wed, 11 Mar 2020 23:38:09 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.6`

```console
$ docker pull mongo@sha256:f1ff4f9fd92c45e545c8a9d726123fc1410e2c53c82e99288edf57da98be4e81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.14393.3506; amd64

### `mongo:3.6` - linux; amd64

```console
$ docker pull mongo@sha256:557aaf306c611bf9cd04e69fc3174757e2ce25ecc073a88fe28dbc889f5dae9a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.6 MB (165644020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3fdbdf0f17b70466eda08d155b2f1c72bc3450d23b8a752a4a841a83d6eb76f`
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
# Sat, 22 Feb 2020 01:08:24 GMT
ENV GOSU_VERSION=1.11
# Sat, 22 Feb 2020 01:08:24 GMT
ENV JSYAML_VERSION=3.13.0
# Sat, 22 Feb 2020 01:08:40 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 22 Feb 2020 01:08:40 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 22 Feb 2020 01:08:41 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Sat, 22 Feb 2020 01:08:41 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Sat, 22 Feb 2020 01:08:42 GMT
ARG MONGO_PACKAGE=mongodb-org
# Sat, 22 Feb 2020 01:08:42 GMT
ARG MONGO_REPO=repo.mongodb.org
# Sat, 22 Feb 2020 01:08:42 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Sat, 22 Feb 2020 01:08:42 GMT
ENV MONGO_MAJOR=3.6
# Sat, 22 Feb 2020 01:08:42 GMT
ENV MONGO_VERSION=3.6.17
# Sat, 22 Feb 2020 01:08:43 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Sat, 22 Feb 2020 01:09:04 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Sat, 22 Feb 2020 01:09:05 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Sat, 22 Feb 2020 01:09:05 GMT
VOLUME [/data/db /data/configdb]
# Sat, 22 Feb 2020 01:09:05 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Sat, 22 Feb 2020 01:09:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 22 Feb 2020 01:09:06 GMT
EXPOSE 27017
# Sat, 22 Feb 2020 01:09:06 GMT
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
	-	`sha256:7f706fb8c773a1773b04049e2fc1aa9f63e9f8b1ecbaae99fcf970f69c417f18`  
		Last Modified: Sat, 22 Feb 2020 01:11:01 GMT  
		Size: 1.2 MB (1243833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f137797464445cc1df1f6510d063791f41c4be58a91cbde2d7c9e9d5985cab6d`  
		Last Modified: Sat, 22 Feb 2020 01:11:01 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a03380f32ca06a89bb8bbb6437140f7feaa8cbc73656efd413066485af7bed9`  
		Last Modified: Sat, 22 Feb 2020 01:11:00 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a38c136f14bc4cc8e7c8b75a1b58fbd13ee66ab4018835cce5deafd77e34629`  
		Last Modified: Sat, 22 Feb 2020 01:11:00 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0e875b59ceec4323d6455ddef1a97e267ed64e723a3785961db869da21e662`  
		Last Modified: Sat, 22 Feb 2020 01:11:19 GMT  
		Size: 117.3 MB (117252414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f55b4999cd606166300c3bcc0c29bbdb69f9e442f652f9e2a1b037ff63069d`  
		Last Modified: Sat, 22 Feb 2020 01:11:00 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc92ef8de8b080701461ef5a44e3df6e2b20f0e5d0502bc9c2f58fb0c18884c`  
		Last Modified: Sat, 22 Feb 2020 01:11:00 GMT  
		Size: 4.0 KB (3953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3.6` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:8d00f2129c233839b0192bc63ad1b38d732559eb063a8c7fb6afd9b14000dfe9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155054951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:904d1cc8fa66fbab1604f0f278d0125cf824c48dde0e06e2de53f80f21123a3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 21 Feb 2020 21:55:42 GMT
ADD file:61b91c95a686740a57740470b7a1fe64d2479c56c36c69ca1222d870e78d44cc in / 
# Fri, 21 Feb 2020 21:55:46 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 21:55:48 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:55:50 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:55:50 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:48:01 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 21 Feb 2020 22:48:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:48:17 GMT
ENV GOSU_VERSION=1.11
# Fri, 21 Feb 2020 22:48:19 GMT
ENV JSYAML_VERSION=3.13.0
# Fri, 21 Feb 2020 22:48:47 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 21 Feb 2020 22:48:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:48:51 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Fri, 21 Feb 2020 22:48:53 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:48:54 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 21 Feb 2020 22:48:54 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:48:55 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:48:56 GMT
ENV MONGO_MAJOR=3.6
# Fri, 21 Feb 2020 22:48:57 GMT
ENV MONGO_VERSION=3.6.17
# Fri, 21 Feb 2020 22:48:59 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 21 Feb 2020 22:49:21 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 21 Feb 2020 22:49:23 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 21 Feb 2020 22:49:24 GMT
VOLUME [/data/db /data/configdb]
# Fri, 21 Feb 2020 22:49:24 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:49:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:49:26 GMT
EXPOSE 27017
# Fri, 21 Feb 2020 22:49:27 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a7bab9946de3c22ecccd832a0910adc2ffa82eea53f83c600d5ebce9e5422ad0`  
		Last Modified: Mon, 17 Feb 2020 15:45:27 GMT  
		Size: 39.9 MB (39940373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38630c4d9093f5b60806171ca7fa47a70d7ab28eeed25edfad43fb91d5f9f825`  
		Last Modified: Fri, 21 Feb 2020 21:56:39 GMT  
		Size: 467.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef678cbe74d844c6a114c1158a8c8868b412b7c5ed3a4c159831975a4915db9`  
		Last Modified: Fri, 21 Feb 2020 21:56:39 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78928743b0e778df64b15ac919705702ee0a080c2586f43c4349b35180de3c36`  
		Last Modified: Fri, 21 Feb 2020 21:56:40 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b98e127168243d033826ae375801cd9bde48991cd8c3f70195b2393e612fdd`  
		Last Modified: Fri, 21 Feb 2020 22:52:35 GMT  
		Size: 2.0 KB (1989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd8b81c3e37e64b559f25587bfdcb850b0f99e789d079c3a5e23aedc76a5b133`  
		Last Modified: Fri, 21 Feb 2020 22:52:35 GMT  
		Size: 2.5 MB (2474933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5133614dc076c55be0b03423a8f81053612df19fc888c3a5e65cf096386ca61a`  
		Last Modified: Fri, 21 Feb 2020 22:52:35 GMT  
		Size: 1.2 MB (1170004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa274bfc4efdade7b87ff58757777040775bd689e0478b13c0325ace270c75b`  
		Last Modified: Fri, 21 Feb 2020 22:52:35 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c551726d412935a665a5faa37ba35c6b578c9b4b9a04e15fbb8141e18c469f4`  
		Last Modified: Fri, 21 Feb 2020 22:52:33 GMT  
		Size: 2.0 KB (1995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690416c5e0de4a88eb11a3f888d668dffc71c64ce9928810382a5f989ea0d6d8`  
		Last Modified: Fri, 21 Feb 2020 22:52:33 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466edf90a60ac36b2e4ef9846aac45cf6dcbf6603561ff365607d6ec8e1d4333`  
		Last Modified: Fri, 21 Feb 2020 22:53:01 GMT  
		Size: 111.5 MB (111459661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a78ae9c5bd995e33cabe28ea21119ec5a46c4ecd1c7a5b80beedf81e226048`  
		Last Modified: Fri, 21 Feb 2020 22:52:33 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddfad788e158cc0e6900c305454fae286feb8c8e9807a24c9e4a962a22727dfc`  
		Last Modified: Fri, 21 Feb 2020 22:52:33 GMT  
		Size: 4.0 KB (3953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3.6` - windows version 10.0.14393.3506; amd64

```console
$ docker pull mongo@sha256:6763381f4a67ddb7df259a4187887006e19ee9253e592ff2bb60c1059bfcdf31
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5820567995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a26b0054534cef77b808f6755003209a9fd4a5056f058edad907cc6c50409ffd`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 05:12:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 20 Feb 2020 05:19:42 GMT
ENV MONGO_VERSION=3.6.17
# Wed, 11 Mar 2020 22:15:37 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.17-signed.msi
# Wed, 11 Mar 2020 22:15:39 GMT
ENV MONGO_DOWNLOAD_SHA256=b20b72d5366a7a00cb85245ebedd01b665bbac4f918dd5fac7a7c5eb68477c26
# Wed, 11 Mar 2020 22:28:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Mar 2020 22:28:24 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Mar 2020 22:28:25 GMT
EXPOSE 27017
# Wed, 11 Mar 2020 22:28:27 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:846a2223e9e7a88a2a07d706553f144d380483d72fb9f0697c4fcd71773a8693`  
		Size: 1.7 GB (1657079102 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0961c48658cd7865bcf6c05285dfbe8ad89cd52059088d7f4eed6fde1bb2b385`  
		Last Modified: Thu, 20 Feb 2020 05:18:25 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4863e5701bfa2388492681880718703eecf4360e943021e702f897bc078de68e`  
		Last Modified: Thu, 20 Feb 2020 05:40:40 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8875ee76ce08286dab2e650f9808e785bc0f79acb4c15382048735765497b07`  
		Last Modified: Wed, 11 Mar 2020 23:38:14 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dffa284f8065be9eb03e643bb9dd50a603c5b6e8813bb0d4ddb7e75987fc5b4d`  
		Last Modified: Wed, 11 Mar 2020 23:38:09 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae68ba460a8f3dc989becee8ef2d59e650742bc77ba74a98d0c8e12ace493d19`  
		Last Modified: Wed, 11 Mar 2020 23:38:54 GMT  
		Size: 93.5 MB (93494538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead5918efa91f150d4991d381d85158e23cdab0f832fd73a318fb4af300348d1`  
		Last Modified: Wed, 11 Mar 2020 23:38:09 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b8dc5e80e6329a94b954cc8673d91fa2222d35ee9569178e1e0502c6ed2d14`  
		Last Modified: Wed, 11 Mar 2020 23:38:10 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a47d981e96991c1baf1c50d2090a8accbe1a377c893fd4d7aa22e580bb24e35`  
		Last Modified: Wed, 11 Mar 2020 23:38:09 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.6.17`

```console
$ docker pull mongo@sha256:f1ff4f9fd92c45e545c8a9d726123fc1410e2c53c82e99288edf57da98be4e81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.14393.3506; amd64

### `mongo:3.6.17` - linux; amd64

```console
$ docker pull mongo@sha256:557aaf306c611bf9cd04e69fc3174757e2ce25ecc073a88fe28dbc889f5dae9a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.6 MB (165644020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3fdbdf0f17b70466eda08d155b2f1c72bc3450d23b8a752a4a841a83d6eb76f`
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
# Sat, 22 Feb 2020 01:08:24 GMT
ENV GOSU_VERSION=1.11
# Sat, 22 Feb 2020 01:08:24 GMT
ENV JSYAML_VERSION=3.13.0
# Sat, 22 Feb 2020 01:08:40 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 22 Feb 2020 01:08:40 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 22 Feb 2020 01:08:41 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Sat, 22 Feb 2020 01:08:41 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Sat, 22 Feb 2020 01:08:42 GMT
ARG MONGO_PACKAGE=mongodb-org
# Sat, 22 Feb 2020 01:08:42 GMT
ARG MONGO_REPO=repo.mongodb.org
# Sat, 22 Feb 2020 01:08:42 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Sat, 22 Feb 2020 01:08:42 GMT
ENV MONGO_MAJOR=3.6
# Sat, 22 Feb 2020 01:08:42 GMT
ENV MONGO_VERSION=3.6.17
# Sat, 22 Feb 2020 01:08:43 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Sat, 22 Feb 2020 01:09:04 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Sat, 22 Feb 2020 01:09:05 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Sat, 22 Feb 2020 01:09:05 GMT
VOLUME [/data/db /data/configdb]
# Sat, 22 Feb 2020 01:09:05 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Sat, 22 Feb 2020 01:09:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 22 Feb 2020 01:09:06 GMT
EXPOSE 27017
# Sat, 22 Feb 2020 01:09:06 GMT
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
	-	`sha256:7f706fb8c773a1773b04049e2fc1aa9f63e9f8b1ecbaae99fcf970f69c417f18`  
		Last Modified: Sat, 22 Feb 2020 01:11:01 GMT  
		Size: 1.2 MB (1243833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f137797464445cc1df1f6510d063791f41c4be58a91cbde2d7c9e9d5985cab6d`  
		Last Modified: Sat, 22 Feb 2020 01:11:01 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a03380f32ca06a89bb8bbb6437140f7feaa8cbc73656efd413066485af7bed9`  
		Last Modified: Sat, 22 Feb 2020 01:11:00 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a38c136f14bc4cc8e7c8b75a1b58fbd13ee66ab4018835cce5deafd77e34629`  
		Last Modified: Sat, 22 Feb 2020 01:11:00 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0e875b59ceec4323d6455ddef1a97e267ed64e723a3785961db869da21e662`  
		Last Modified: Sat, 22 Feb 2020 01:11:19 GMT  
		Size: 117.3 MB (117252414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f55b4999cd606166300c3bcc0c29bbdb69f9e442f652f9e2a1b037ff63069d`  
		Last Modified: Sat, 22 Feb 2020 01:11:00 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc92ef8de8b080701461ef5a44e3df6e2b20f0e5d0502bc9c2f58fb0c18884c`  
		Last Modified: Sat, 22 Feb 2020 01:11:00 GMT  
		Size: 4.0 KB (3953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3.6.17` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:8d00f2129c233839b0192bc63ad1b38d732559eb063a8c7fb6afd9b14000dfe9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155054951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:904d1cc8fa66fbab1604f0f278d0125cf824c48dde0e06e2de53f80f21123a3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 21 Feb 2020 21:55:42 GMT
ADD file:61b91c95a686740a57740470b7a1fe64d2479c56c36c69ca1222d870e78d44cc in / 
# Fri, 21 Feb 2020 21:55:46 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 21:55:48 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:55:50 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:55:50 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:48:01 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 21 Feb 2020 22:48:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:48:17 GMT
ENV GOSU_VERSION=1.11
# Fri, 21 Feb 2020 22:48:19 GMT
ENV JSYAML_VERSION=3.13.0
# Fri, 21 Feb 2020 22:48:47 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 21 Feb 2020 22:48:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:48:51 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Fri, 21 Feb 2020 22:48:53 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:48:54 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 21 Feb 2020 22:48:54 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:48:55 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:48:56 GMT
ENV MONGO_MAJOR=3.6
# Fri, 21 Feb 2020 22:48:57 GMT
ENV MONGO_VERSION=3.6.17
# Fri, 21 Feb 2020 22:48:59 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 21 Feb 2020 22:49:21 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 21 Feb 2020 22:49:23 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 21 Feb 2020 22:49:24 GMT
VOLUME [/data/db /data/configdb]
# Fri, 21 Feb 2020 22:49:24 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:49:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:49:26 GMT
EXPOSE 27017
# Fri, 21 Feb 2020 22:49:27 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a7bab9946de3c22ecccd832a0910adc2ffa82eea53f83c600d5ebce9e5422ad0`  
		Last Modified: Mon, 17 Feb 2020 15:45:27 GMT  
		Size: 39.9 MB (39940373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38630c4d9093f5b60806171ca7fa47a70d7ab28eeed25edfad43fb91d5f9f825`  
		Last Modified: Fri, 21 Feb 2020 21:56:39 GMT  
		Size: 467.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef678cbe74d844c6a114c1158a8c8868b412b7c5ed3a4c159831975a4915db9`  
		Last Modified: Fri, 21 Feb 2020 21:56:39 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78928743b0e778df64b15ac919705702ee0a080c2586f43c4349b35180de3c36`  
		Last Modified: Fri, 21 Feb 2020 21:56:40 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b98e127168243d033826ae375801cd9bde48991cd8c3f70195b2393e612fdd`  
		Last Modified: Fri, 21 Feb 2020 22:52:35 GMT  
		Size: 2.0 KB (1989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd8b81c3e37e64b559f25587bfdcb850b0f99e789d079c3a5e23aedc76a5b133`  
		Last Modified: Fri, 21 Feb 2020 22:52:35 GMT  
		Size: 2.5 MB (2474933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5133614dc076c55be0b03423a8f81053612df19fc888c3a5e65cf096386ca61a`  
		Last Modified: Fri, 21 Feb 2020 22:52:35 GMT  
		Size: 1.2 MB (1170004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa274bfc4efdade7b87ff58757777040775bd689e0478b13c0325ace270c75b`  
		Last Modified: Fri, 21 Feb 2020 22:52:35 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c551726d412935a665a5faa37ba35c6b578c9b4b9a04e15fbb8141e18c469f4`  
		Last Modified: Fri, 21 Feb 2020 22:52:33 GMT  
		Size: 2.0 KB (1995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690416c5e0de4a88eb11a3f888d668dffc71c64ce9928810382a5f989ea0d6d8`  
		Last Modified: Fri, 21 Feb 2020 22:52:33 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466edf90a60ac36b2e4ef9846aac45cf6dcbf6603561ff365607d6ec8e1d4333`  
		Last Modified: Fri, 21 Feb 2020 22:53:01 GMT  
		Size: 111.5 MB (111459661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a78ae9c5bd995e33cabe28ea21119ec5a46c4ecd1c7a5b80beedf81e226048`  
		Last Modified: Fri, 21 Feb 2020 22:52:33 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddfad788e158cc0e6900c305454fae286feb8c8e9807a24c9e4a962a22727dfc`  
		Last Modified: Fri, 21 Feb 2020 22:52:33 GMT  
		Size: 4.0 KB (3953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3.6.17` - windows version 10.0.14393.3506; amd64

```console
$ docker pull mongo@sha256:6763381f4a67ddb7df259a4187887006e19ee9253e592ff2bb60c1059bfcdf31
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5820567995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a26b0054534cef77b808f6755003209a9fd4a5056f058edad907cc6c50409ffd`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 05:12:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 20 Feb 2020 05:19:42 GMT
ENV MONGO_VERSION=3.6.17
# Wed, 11 Mar 2020 22:15:37 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.17-signed.msi
# Wed, 11 Mar 2020 22:15:39 GMT
ENV MONGO_DOWNLOAD_SHA256=b20b72d5366a7a00cb85245ebedd01b665bbac4f918dd5fac7a7c5eb68477c26
# Wed, 11 Mar 2020 22:28:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Mar 2020 22:28:24 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Mar 2020 22:28:25 GMT
EXPOSE 27017
# Wed, 11 Mar 2020 22:28:27 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:846a2223e9e7a88a2a07d706553f144d380483d72fb9f0697c4fcd71773a8693`  
		Size: 1.7 GB (1657079102 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0961c48658cd7865bcf6c05285dfbe8ad89cd52059088d7f4eed6fde1bb2b385`  
		Last Modified: Thu, 20 Feb 2020 05:18:25 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4863e5701bfa2388492681880718703eecf4360e943021e702f897bc078de68e`  
		Last Modified: Thu, 20 Feb 2020 05:40:40 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8875ee76ce08286dab2e650f9808e785bc0f79acb4c15382048735765497b07`  
		Last Modified: Wed, 11 Mar 2020 23:38:14 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dffa284f8065be9eb03e643bb9dd50a603c5b6e8813bb0d4ddb7e75987fc5b4d`  
		Last Modified: Wed, 11 Mar 2020 23:38:09 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae68ba460a8f3dc989becee8ef2d59e650742bc77ba74a98d0c8e12ace493d19`  
		Last Modified: Wed, 11 Mar 2020 23:38:54 GMT  
		Size: 93.5 MB (93494538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead5918efa91f150d4991d381d85158e23cdab0f832fd73a318fb4af300348d1`  
		Last Modified: Wed, 11 Mar 2020 23:38:09 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b8dc5e80e6329a94b954cc8673d91fa2222d35ee9569178e1e0502c6ed2d14`  
		Last Modified: Wed, 11 Mar 2020 23:38:10 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a47d981e96991c1baf1c50d2090a8accbe1a377c893fd4d7aa22e580bb24e35`  
		Last Modified: Wed, 11 Mar 2020 23:38:09 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.6.17-windowsservercore`

```console
$ docker pull mongo@sha256:119864376569cbeccbb83d4eec939c7439dd733f57d970246b3998b5dc9dce7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3506; amd64

### `mongo:3.6.17-windowsservercore` - windows version 10.0.14393.3506; amd64

```console
$ docker pull mongo@sha256:6763381f4a67ddb7df259a4187887006e19ee9253e592ff2bb60c1059bfcdf31
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5820567995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a26b0054534cef77b808f6755003209a9fd4a5056f058edad907cc6c50409ffd`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 05:12:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 20 Feb 2020 05:19:42 GMT
ENV MONGO_VERSION=3.6.17
# Wed, 11 Mar 2020 22:15:37 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.17-signed.msi
# Wed, 11 Mar 2020 22:15:39 GMT
ENV MONGO_DOWNLOAD_SHA256=b20b72d5366a7a00cb85245ebedd01b665bbac4f918dd5fac7a7c5eb68477c26
# Wed, 11 Mar 2020 22:28:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Mar 2020 22:28:24 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Mar 2020 22:28:25 GMT
EXPOSE 27017
# Wed, 11 Mar 2020 22:28:27 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:846a2223e9e7a88a2a07d706553f144d380483d72fb9f0697c4fcd71773a8693`  
		Size: 1.7 GB (1657079102 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0961c48658cd7865bcf6c05285dfbe8ad89cd52059088d7f4eed6fde1bb2b385`  
		Last Modified: Thu, 20 Feb 2020 05:18:25 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4863e5701bfa2388492681880718703eecf4360e943021e702f897bc078de68e`  
		Last Modified: Thu, 20 Feb 2020 05:40:40 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8875ee76ce08286dab2e650f9808e785bc0f79acb4c15382048735765497b07`  
		Last Modified: Wed, 11 Mar 2020 23:38:14 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dffa284f8065be9eb03e643bb9dd50a603c5b6e8813bb0d4ddb7e75987fc5b4d`  
		Last Modified: Wed, 11 Mar 2020 23:38:09 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae68ba460a8f3dc989becee8ef2d59e650742bc77ba74a98d0c8e12ace493d19`  
		Last Modified: Wed, 11 Mar 2020 23:38:54 GMT  
		Size: 93.5 MB (93494538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead5918efa91f150d4991d381d85158e23cdab0f832fd73a318fb4af300348d1`  
		Last Modified: Wed, 11 Mar 2020 23:38:09 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b8dc5e80e6329a94b954cc8673d91fa2222d35ee9569178e1e0502c6ed2d14`  
		Last Modified: Wed, 11 Mar 2020 23:38:10 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a47d981e96991c1baf1c50d2090a8accbe1a377c893fd4d7aa22e580bb24e35`  
		Last Modified: Wed, 11 Mar 2020 23:38:09 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.6.17-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:119864376569cbeccbb83d4eec939c7439dd733f57d970246b3998b5dc9dce7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3506; amd64

### `mongo:3.6.17-windowsservercore-ltsc2016` - windows version 10.0.14393.3506; amd64

```console
$ docker pull mongo@sha256:6763381f4a67ddb7df259a4187887006e19ee9253e592ff2bb60c1059bfcdf31
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5820567995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a26b0054534cef77b808f6755003209a9fd4a5056f058edad907cc6c50409ffd`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 05:12:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 20 Feb 2020 05:19:42 GMT
ENV MONGO_VERSION=3.6.17
# Wed, 11 Mar 2020 22:15:37 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.17-signed.msi
# Wed, 11 Mar 2020 22:15:39 GMT
ENV MONGO_DOWNLOAD_SHA256=b20b72d5366a7a00cb85245ebedd01b665bbac4f918dd5fac7a7c5eb68477c26
# Wed, 11 Mar 2020 22:28:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Mar 2020 22:28:24 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Mar 2020 22:28:25 GMT
EXPOSE 27017
# Wed, 11 Mar 2020 22:28:27 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:846a2223e9e7a88a2a07d706553f144d380483d72fb9f0697c4fcd71773a8693`  
		Size: 1.7 GB (1657079102 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0961c48658cd7865bcf6c05285dfbe8ad89cd52059088d7f4eed6fde1bb2b385`  
		Last Modified: Thu, 20 Feb 2020 05:18:25 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4863e5701bfa2388492681880718703eecf4360e943021e702f897bc078de68e`  
		Last Modified: Thu, 20 Feb 2020 05:40:40 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8875ee76ce08286dab2e650f9808e785bc0f79acb4c15382048735765497b07`  
		Last Modified: Wed, 11 Mar 2020 23:38:14 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dffa284f8065be9eb03e643bb9dd50a603c5b6e8813bb0d4ddb7e75987fc5b4d`  
		Last Modified: Wed, 11 Mar 2020 23:38:09 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae68ba460a8f3dc989becee8ef2d59e650742bc77ba74a98d0c8e12ace493d19`  
		Last Modified: Wed, 11 Mar 2020 23:38:54 GMT  
		Size: 93.5 MB (93494538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead5918efa91f150d4991d381d85158e23cdab0f832fd73a318fb4af300348d1`  
		Last Modified: Wed, 11 Mar 2020 23:38:09 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b8dc5e80e6329a94b954cc8673d91fa2222d35ee9569178e1e0502c6ed2d14`  
		Last Modified: Wed, 11 Mar 2020 23:38:10 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a47d981e96991c1baf1c50d2090a8accbe1a377c893fd4d7aa22e580bb24e35`  
		Last Modified: Wed, 11 Mar 2020 23:38:09 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.6.17-xenial`

```console
$ docker pull mongo@sha256:dbdd944e50ed4f45174aae05205e284b76166e3ac9801b6f15856b79fb3f595b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:3.6.17-xenial` - linux; amd64

```console
$ docker pull mongo@sha256:557aaf306c611bf9cd04e69fc3174757e2ce25ecc073a88fe28dbc889f5dae9a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.6 MB (165644020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3fdbdf0f17b70466eda08d155b2f1c72bc3450d23b8a752a4a841a83d6eb76f`
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
# Sat, 22 Feb 2020 01:08:24 GMT
ENV GOSU_VERSION=1.11
# Sat, 22 Feb 2020 01:08:24 GMT
ENV JSYAML_VERSION=3.13.0
# Sat, 22 Feb 2020 01:08:40 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 22 Feb 2020 01:08:40 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 22 Feb 2020 01:08:41 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Sat, 22 Feb 2020 01:08:41 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Sat, 22 Feb 2020 01:08:42 GMT
ARG MONGO_PACKAGE=mongodb-org
# Sat, 22 Feb 2020 01:08:42 GMT
ARG MONGO_REPO=repo.mongodb.org
# Sat, 22 Feb 2020 01:08:42 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Sat, 22 Feb 2020 01:08:42 GMT
ENV MONGO_MAJOR=3.6
# Sat, 22 Feb 2020 01:08:42 GMT
ENV MONGO_VERSION=3.6.17
# Sat, 22 Feb 2020 01:08:43 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Sat, 22 Feb 2020 01:09:04 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Sat, 22 Feb 2020 01:09:05 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Sat, 22 Feb 2020 01:09:05 GMT
VOLUME [/data/db /data/configdb]
# Sat, 22 Feb 2020 01:09:05 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Sat, 22 Feb 2020 01:09:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 22 Feb 2020 01:09:06 GMT
EXPOSE 27017
# Sat, 22 Feb 2020 01:09:06 GMT
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
	-	`sha256:7f706fb8c773a1773b04049e2fc1aa9f63e9f8b1ecbaae99fcf970f69c417f18`  
		Last Modified: Sat, 22 Feb 2020 01:11:01 GMT  
		Size: 1.2 MB (1243833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f137797464445cc1df1f6510d063791f41c4be58a91cbde2d7c9e9d5985cab6d`  
		Last Modified: Sat, 22 Feb 2020 01:11:01 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a03380f32ca06a89bb8bbb6437140f7feaa8cbc73656efd413066485af7bed9`  
		Last Modified: Sat, 22 Feb 2020 01:11:00 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a38c136f14bc4cc8e7c8b75a1b58fbd13ee66ab4018835cce5deafd77e34629`  
		Last Modified: Sat, 22 Feb 2020 01:11:00 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0e875b59ceec4323d6455ddef1a97e267ed64e723a3785961db869da21e662`  
		Last Modified: Sat, 22 Feb 2020 01:11:19 GMT  
		Size: 117.3 MB (117252414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f55b4999cd606166300c3bcc0c29bbdb69f9e442f652f9e2a1b037ff63069d`  
		Last Modified: Sat, 22 Feb 2020 01:11:00 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc92ef8de8b080701461ef5a44e3df6e2b20f0e5d0502bc9c2f58fb0c18884c`  
		Last Modified: Sat, 22 Feb 2020 01:11:00 GMT  
		Size: 4.0 KB (3953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3.6.17-xenial` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:8d00f2129c233839b0192bc63ad1b38d732559eb063a8c7fb6afd9b14000dfe9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155054951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:904d1cc8fa66fbab1604f0f278d0125cf824c48dde0e06e2de53f80f21123a3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 21 Feb 2020 21:55:42 GMT
ADD file:61b91c95a686740a57740470b7a1fe64d2479c56c36c69ca1222d870e78d44cc in / 
# Fri, 21 Feb 2020 21:55:46 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 21:55:48 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:55:50 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:55:50 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:48:01 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 21 Feb 2020 22:48:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:48:17 GMT
ENV GOSU_VERSION=1.11
# Fri, 21 Feb 2020 22:48:19 GMT
ENV JSYAML_VERSION=3.13.0
# Fri, 21 Feb 2020 22:48:47 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 21 Feb 2020 22:48:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:48:51 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Fri, 21 Feb 2020 22:48:53 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:48:54 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 21 Feb 2020 22:48:54 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:48:55 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:48:56 GMT
ENV MONGO_MAJOR=3.6
# Fri, 21 Feb 2020 22:48:57 GMT
ENV MONGO_VERSION=3.6.17
# Fri, 21 Feb 2020 22:48:59 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 21 Feb 2020 22:49:21 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 21 Feb 2020 22:49:23 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 21 Feb 2020 22:49:24 GMT
VOLUME [/data/db /data/configdb]
# Fri, 21 Feb 2020 22:49:24 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:49:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:49:26 GMT
EXPOSE 27017
# Fri, 21 Feb 2020 22:49:27 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a7bab9946de3c22ecccd832a0910adc2ffa82eea53f83c600d5ebce9e5422ad0`  
		Last Modified: Mon, 17 Feb 2020 15:45:27 GMT  
		Size: 39.9 MB (39940373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38630c4d9093f5b60806171ca7fa47a70d7ab28eeed25edfad43fb91d5f9f825`  
		Last Modified: Fri, 21 Feb 2020 21:56:39 GMT  
		Size: 467.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef678cbe74d844c6a114c1158a8c8868b412b7c5ed3a4c159831975a4915db9`  
		Last Modified: Fri, 21 Feb 2020 21:56:39 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78928743b0e778df64b15ac919705702ee0a080c2586f43c4349b35180de3c36`  
		Last Modified: Fri, 21 Feb 2020 21:56:40 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b98e127168243d033826ae375801cd9bde48991cd8c3f70195b2393e612fdd`  
		Last Modified: Fri, 21 Feb 2020 22:52:35 GMT  
		Size: 2.0 KB (1989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd8b81c3e37e64b559f25587bfdcb850b0f99e789d079c3a5e23aedc76a5b133`  
		Last Modified: Fri, 21 Feb 2020 22:52:35 GMT  
		Size: 2.5 MB (2474933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5133614dc076c55be0b03423a8f81053612df19fc888c3a5e65cf096386ca61a`  
		Last Modified: Fri, 21 Feb 2020 22:52:35 GMT  
		Size: 1.2 MB (1170004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa274bfc4efdade7b87ff58757777040775bd689e0478b13c0325ace270c75b`  
		Last Modified: Fri, 21 Feb 2020 22:52:35 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c551726d412935a665a5faa37ba35c6b578c9b4b9a04e15fbb8141e18c469f4`  
		Last Modified: Fri, 21 Feb 2020 22:52:33 GMT  
		Size: 2.0 KB (1995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690416c5e0de4a88eb11a3f888d668dffc71c64ce9928810382a5f989ea0d6d8`  
		Last Modified: Fri, 21 Feb 2020 22:52:33 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466edf90a60ac36b2e4ef9846aac45cf6dcbf6603561ff365607d6ec8e1d4333`  
		Last Modified: Fri, 21 Feb 2020 22:53:01 GMT  
		Size: 111.5 MB (111459661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a78ae9c5bd995e33cabe28ea21119ec5a46c4ecd1c7a5b80beedf81e226048`  
		Last Modified: Fri, 21 Feb 2020 22:52:33 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddfad788e158cc0e6900c305454fae286feb8c8e9807a24c9e4a962a22727dfc`  
		Last Modified: Fri, 21 Feb 2020 22:52:33 GMT  
		Size: 4.0 KB (3953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.6-windowsservercore`

```console
$ docker pull mongo@sha256:119864376569cbeccbb83d4eec939c7439dd733f57d970246b3998b5dc9dce7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3506; amd64

### `mongo:3.6-windowsservercore` - windows version 10.0.14393.3506; amd64

```console
$ docker pull mongo@sha256:6763381f4a67ddb7df259a4187887006e19ee9253e592ff2bb60c1059bfcdf31
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5820567995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a26b0054534cef77b808f6755003209a9fd4a5056f058edad907cc6c50409ffd`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 05:12:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 20 Feb 2020 05:19:42 GMT
ENV MONGO_VERSION=3.6.17
# Wed, 11 Mar 2020 22:15:37 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.17-signed.msi
# Wed, 11 Mar 2020 22:15:39 GMT
ENV MONGO_DOWNLOAD_SHA256=b20b72d5366a7a00cb85245ebedd01b665bbac4f918dd5fac7a7c5eb68477c26
# Wed, 11 Mar 2020 22:28:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Mar 2020 22:28:24 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Mar 2020 22:28:25 GMT
EXPOSE 27017
# Wed, 11 Mar 2020 22:28:27 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:846a2223e9e7a88a2a07d706553f144d380483d72fb9f0697c4fcd71773a8693`  
		Size: 1.7 GB (1657079102 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0961c48658cd7865bcf6c05285dfbe8ad89cd52059088d7f4eed6fde1bb2b385`  
		Last Modified: Thu, 20 Feb 2020 05:18:25 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4863e5701bfa2388492681880718703eecf4360e943021e702f897bc078de68e`  
		Last Modified: Thu, 20 Feb 2020 05:40:40 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8875ee76ce08286dab2e650f9808e785bc0f79acb4c15382048735765497b07`  
		Last Modified: Wed, 11 Mar 2020 23:38:14 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dffa284f8065be9eb03e643bb9dd50a603c5b6e8813bb0d4ddb7e75987fc5b4d`  
		Last Modified: Wed, 11 Mar 2020 23:38:09 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae68ba460a8f3dc989becee8ef2d59e650742bc77ba74a98d0c8e12ace493d19`  
		Last Modified: Wed, 11 Mar 2020 23:38:54 GMT  
		Size: 93.5 MB (93494538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead5918efa91f150d4991d381d85158e23cdab0f832fd73a318fb4af300348d1`  
		Last Modified: Wed, 11 Mar 2020 23:38:09 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b8dc5e80e6329a94b954cc8673d91fa2222d35ee9569178e1e0502c6ed2d14`  
		Last Modified: Wed, 11 Mar 2020 23:38:10 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a47d981e96991c1baf1c50d2090a8accbe1a377c893fd4d7aa22e580bb24e35`  
		Last Modified: Wed, 11 Mar 2020 23:38:09 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.6-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:119864376569cbeccbb83d4eec939c7439dd733f57d970246b3998b5dc9dce7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3506; amd64

### `mongo:3.6-windowsservercore-ltsc2016` - windows version 10.0.14393.3506; amd64

```console
$ docker pull mongo@sha256:6763381f4a67ddb7df259a4187887006e19ee9253e592ff2bb60c1059bfcdf31
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5820567995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a26b0054534cef77b808f6755003209a9fd4a5056f058edad907cc6c50409ffd`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 05:12:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 20 Feb 2020 05:19:42 GMT
ENV MONGO_VERSION=3.6.17
# Wed, 11 Mar 2020 22:15:37 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.17-signed.msi
# Wed, 11 Mar 2020 22:15:39 GMT
ENV MONGO_DOWNLOAD_SHA256=b20b72d5366a7a00cb85245ebedd01b665bbac4f918dd5fac7a7c5eb68477c26
# Wed, 11 Mar 2020 22:28:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Mar 2020 22:28:24 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Mar 2020 22:28:25 GMT
EXPOSE 27017
# Wed, 11 Mar 2020 22:28:27 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:846a2223e9e7a88a2a07d706553f144d380483d72fb9f0697c4fcd71773a8693`  
		Size: 1.7 GB (1657079102 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0961c48658cd7865bcf6c05285dfbe8ad89cd52059088d7f4eed6fde1bb2b385`  
		Last Modified: Thu, 20 Feb 2020 05:18:25 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4863e5701bfa2388492681880718703eecf4360e943021e702f897bc078de68e`  
		Last Modified: Thu, 20 Feb 2020 05:40:40 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8875ee76ce08286dab2e650f9808e785bc0f79acb4c15382048735765497b07`  
		Last Modified: Wed, 11 Mar 2020 23:38:14 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dffa284f8065be9eb03e643bb9dd50a603c5b6e8813bb0d4ddb7e75987fc5b4d`  
		Last Modified: Wed, 11 Mar 2020 23:38:09 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae68ba460a8f3dc989becee8ef2d59e650742bc77ba74a98d0c8e12ace493d19`  
		Last Modified: Wed, 11 Mar 2020 23:38:54 GMT  
		Size: 93.5 MB (93494538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead5918efa91f150d4991d381d85158e23cdab0f832fd73a318fb4af300348d1`  
		Last Modified: Wed, 11 Mar 2020 23:38:09 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b8dc5e80e6329a94b954cc8673d91fa2222d35ee9569178e1e0502c6ed2d14`  
		Last Modified: Wed, 11 Mar 2020 23:38:10 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a47d981e96991c1baf1c50d2090a8accbe1a377c893fd4d7aa22e580bb24e35`  
		Last Modified: Wed, 11 Mar 2020 23:38:09 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.6-xenial`

```console
$ docker pull mongo@sha256:dbdd944e50ed4f45174aae05205e284b76166e3ac9801b6f15856b79fb3f595b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:3.6-xenial` - linux; amd64

```console
$ docker pull mongo@sha256:557aaf306c611bf9cd04e69fc3174757e2ce25ecc073a88fe28dbc889f5dae9a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.6 MB (165644020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3fdbdf0f17b70466eda08d155b2f1c72bc3450d23b8a752a4a841a83d6eb76f`
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
# Sat, 22 Feb 2020 01:08:24 GMT
ENV GOSU_VERSION=1.11
# Sat, 22 Feb 2020 01:08:24 GMT
ENV JSYAML_VERSION=3.13.0
# Sat, 22 Feb 2020 01:08:40 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 22 Feb 2020 01:08:40 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 22 Feb 2020 01:08:41 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Sat, 22 Feb 2020 01:08:41 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Sat, 22 Feb 2020 01:08:42 GMT
ARG MONGO_PACKAGE=mongodb-org
# Sat, 22 Feb 2020 01:08:42 GMT
ARG MONGO_REPO=repo.mongodb.org
# Sat, 22 Feb 2020 01:08:42 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Sat, 22 Feb 2020 01:08:42 GMT
ENV MONGO_MAJOR=3.6
# Sat, 22 Feb 2020 01:08:42 GMT
ENV MONGO_VERSION=3.6.17
# Sat, 22 Feb 2020 01:08:43 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Sat, 22 Feb 2020 01:09:04 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Sat, 22 Feb 2020 01:09:05 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Sat, 22 Feb 2020 01:09:05 GMT
VOLUME [/data/db /data/configdb]
# Sat, 22 Feb 2020 01:09:05 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Sat, 22 Feb 2020 01:09:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 22 Feb 2020 01:09:06 GMT
EXPOSE 27017
# Sat, 22 Feb 2020 01:09:06 GMT
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
	-	`sha256:7f706fb8c773a1773b04049e2fc1aa9f63e9f8b1ecbaae99fcf970f69c417f18`  
		Last Modified: Sat, 22 Feb 2020 01:11:01 GMT  
		Size: 1.2 MB (1243833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f137797464445cc1df1f6510d063791f41c4be58a91cbde2d7c9e9d5985cab6d`  
		Last Modified: Sat, 22 Feb 2020 01:11:01 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a03380f32ca06a89bb8bbb6437140f7feaa8cbc73656efd413066485af7bed9`  
		Last Modified: Sat, 22 Feb 2020 01:11:00 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a38c136f14bc4cc8e7c8b75a1b58fbd13ee66ab4018835cce5deafd77e34629`  
		Last Modified: Sat, 22 Feb 2020 01:11:00 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0e875b59ceec4323d6455ddef1a97e267ed64e723a3785961db869da21e662`  
		Last Modified: Sat, 22 Feb 2020 01:11:19 GMT  
		Size: 117.3 MB (117252414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f55b4999cd606166300c3bcc0c29bbdb69f9e442f652f9e2a1b037ff63069d`  
		Last Modified: Sat, 22 Feb 2020 01:11:00 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc92ef8de8b080701461ef5a44e3df6e2b20f0e5d0502bc9c2f58fb0c18884c`  
		Last Modified: Sat, 22 Feb 2020 01:11:00 GMT  
		Size: 4.0 KB (3953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3.6-xenial` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:8d00f2129c233839b0192bc63ad1b38d732559eb063a8c7fb6afd9b14000dfe9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155054951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:904d1cc8fa66fbab1604f0f278d0125cf824c48dde0e06e2de53f80f21123a3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 21 Feb 2020 21:55:42 GMT
ADD file:61b91c95a686740a57740470b7a1fe64d2479c56c36c69ca1222d870e78d44cc in / 
# Fri, 21 Feb 2020 21:55:46 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 21:55:48 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:55:50 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:55:50 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:48:01 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 21 Feb 2020 22:48:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:48:17 GMT
ENV GOSU_VERSION=1.11
# Fri, 21 Feb 2020 22:48:19 GMT
ENV JSYAML_VERSION=3.13.0
# Fri, 21 Feb 2020 22:48:47 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 21 Feb 2020 22:48:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:48:51 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Fri, 21 Feb 2020 22:48:53 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:48:54 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 21 Feb 2020 22:48:54 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:48:55 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:48:56 GMT
ENV MONGO_MAJOR=3.6
# Fri, 21 Feb 2020 22:48:57 GMT
ENV MONGO_VERSION=3.6.17
# Fri, 21 Feb 2020 22:48:59 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 21 Feb 2020 22:49:21 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 21 Feb 2020 22:49:23 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 21 Feb 2020 22:49:24 GMT
VOLUME [/data/db /data/configdb]
# Fri, 21 Feb 2020 22:49:24 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:49:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:49:26 GMT
EXPOSE 27017
# Fri, 21 Feb 2020 22:49:27 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a7bab9946de3c22ecccd832a0910adc2ffa82eea53f83c600d5ebce9e5422ad0`  
		Last Modified: Mon, 17 Feb 2020 15:45:27 GMT  
		Size: 39.9 MB (39940373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38630c4d9093f5b60806171ca7fa47a70d7ab28eeed25edfad43fb91d5f9f825`  
		Last Modified: Fri, 21 Feb 2020 21:56:39 GMT  
		Size: 467.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef678cbe74d844c6a114c1158a8c8868b412b7c5ed3a4c159831975a4915db9`  
		Last Modified: Fri, 21 Feb 2020 21:56:39 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78928743b0e778df64b15ac919705702ee0a080c2586f43c4349b35180de3c36`  
		Last Modified: Fri, 21 Feb 2020 21:56:40 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b98e127168243d033826ae375801cd9bde48991cd8c3f70195b2393e612fdd`  
		Last Modified: Fri, 21 Feb 2020 22:52:35 GMT  
		Size: 2.0 KB (1989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd8b81c3e37e64b559f25587bfdcb850b0f99e789d079c3a5e23aedc76a5b133`  
		Last Modified: Fri, 21 Feb 2020 22:52:35 GMT  
		Size: 2.5 MB (2474933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5133614dc076c55be0b03423a8f81053612df19fc888c3a5e65cf096386ca61a`  
		Last Modified: Fri, 21 Feb 2020 22:52:35 GMT  
		Size: 1.2 MB (1170004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa274bfc4efdade7b87ff58757777040775bd689e0478b13c0325ace270c75b`  
		Last Modified: Fri, 21 Feb 2020 22:52:35 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c551726d412935a665a5faa37ba35c6b578c9b4b9a04e15fbb8141e18c469f4`  
		Last Modified: Fri, 21 Feb 2020 22:52:33 GMT  
		Size: 2.0 KB (1995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690416c5e0de4a88eb11a3f888d668dffc71c64ce9928810382a5f989ea0d6d8`  
		Last Modified: Fri, 21 Feb 2020 22:52:33 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466edf90a60ac36b2e4ef9846aac45cf6dcbf6603561ff365607d6ec8e1d4333`  
		Last Modified: Fri, 21 Feb 2020 22:53:01 GMT  
		Size: 111.5 MB (111459661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a78ae9c5bd995e33cabe28ea21119ec5a46c4ecd1c7a5b80beedf81e226048`  
		Last Modified: Fri, 21 Feb 2020 22:52:33 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddfad788e158cc0e6900c305454fae286feb8c8e9807a24c9e4a962a22727dfc`  
		Last Modified: Fri, 21 Feb 2020 22:52:33 GMT  
		Size: 4.0 KB (3953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3-windowsservercore`

```console
$ docker pull mongo@sha256:119864376569cbeccbb83d4eec939c7439dd733f57d970246b3998b5dc9dce7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3506; amd64

### `mongo:3-windowsservercore` - windows version 10.0.14393.3506; amd64

```console
$ docker pull mongo@sha256:6763381f4a67ddb7df259a4187887006e19ee9253e592ff2bb60c1059bfcdf31
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5820567995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a26b0054534cef77b808f6755003209a9fd4a5056f058edad907cc6c50409ffd`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 05:12:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 20 Feb 2020 05:19:42 GMT
ENV MONGO_VERSION=3.6.17
# Wed, 11 Mar 2020 22:15:37 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.17-signed.msi
# Wed, 11 Mar 2020 22:15:39 GMT
ENV MONGO_DOWNLOAD_SHA256=b20b72d5366a7a00cb85245ebedd01b665bbac4f918dd5fac7a7c5eb68477c26
# Wed, 11 Mar 2020 22:28:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Mar 2020 22:28:24 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Mar 2020 22:28:25 GMT
EXPOSE 27017
# Wed, 11 Mar 2020 22:28:27 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:846a2223e9e7a88a2a07d706553f144d380483d72fb9f0697c4fcd71773a8693`  
		Size: 1.7 GB (1657079102 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0961c48658cd7865bcf6c05285dfbe8ad89cd52059088d7f4eed6fde1bb2b385`  
		Last Modified: Thu, 20 Feb 2020 05:18:25 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4863e5701bfa2388492681880718703eecf4360e943021e702f897bc078de68e`  
		Last Modified: Thu, 20 Feb 2020 05:40:40 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8875ee76ce08286dab2e650f9808e785bc0f79acb4c15382048735765497b07`  
		Last Modified: Wed, 11 Mar 2020 23:38:14 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dffa284f8065be9eb03e643bb9dd50a603c5b6e8813bb0d4ddb7e75987fc5b4d`  
		Last Modified: Wed, 11 Mar 2020 23:38:09 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae68ba460a8f3dc989becee8ef2d59e650742bc77ba74a98d0c8e12ace493d19`  
		Last Modified: Wed, 11 Mar 2020 23:38:54 GMT  
		Size: 93.5 MB (93494538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead5918efa91f150d4991d381d85158e23cdab0f832fd73a318fb4af300348d1`  
		Last Modified: Wed, 11 Mar 2020 23:38:09 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b8dc5e80e6329a94b954cc8673d91fa2222d35ee9569178e1e0502c6ed2d14`  
		Last Modified: Wed, 11 Mar 2020 23:38:10 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a47d981e96991c1baf1c50d2090a8accbe1a377c893fd4d7aa22e580bb24e35`  
		Last Modified: Wed, 11 Mar 2020 23:38:09 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:119864376569cbeccbb83d4eec939c7439dd733f57d970246b3998b5dc9dce7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3506; amd64

### `mongo:3-windowsservercore-ltsc2016` - windows version 10.0.14393.3506; amd64

```console
$ docker pull mongo@sha256:6763381f4a67ddb7df259a4187887006e19ee9253e592ff2bb60c1059bfcdf31
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5820567995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a26b0054534cef77b808f6755003209a9fd4a5056f058edad907cc6c50409ffd`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 05:12:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 20 Feb 2020 05:19:42 GMT
ENV MONGO_VERSION=3.6.17
# Wed, 11 Mar 2020 22:15:37 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.17-signed.msi
# Wed, 11 Mar 2020 22:15:39 GMT
ENV MONGO_DOWNLOAD_SHA256=b20b72d5366a7a00cb85245ebedd01b665bbac4f918dd5fac7a7c5eb68477c26
# Wed, 11 Mar 2020 22:28:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Mar 2020 22:28:24 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Mar 2020 22:28:25 GMT
EXPOSE 27017
# Wed, 11 Mar 2020 22:28:27 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:846a2223e9e7a88a2a07d706553f144d380483d72fb9f0697c4fcd71773a8693`  
		Size: 1.7 GB (1657079102 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0961c48658cd7865bcf6c05285dfbe8ad89cd52059088d7f4eed6fde1bb2b385`  
		Last Modified: Thu, 20 Feb 2020 05:18:25 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4863e5701bfa2388492681880718703eecf4360e943021e702f897bc078de68e`  
		Last Modified: Thu, 20 Feb 2020 05:40:40 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8875ee76ce08286dab2e650f9808e785bc0f79acb4c15382048735765497b07`  
		Last Modified: Wed, 11 Mar 2020 23:38:14 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dffa284f8065be9eb03e643bb9dd50a603c5b6e8813bb0d4ddb7e75987fc5b4d`  
		Last Modified: Wed, 11 Mar 2020 23:38:09 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae68ba460a8f3dc989becee8ef2d59e650742bc77ba74a98d0c8e12ace493d19`  
		Last Modified: Wed, 11 Mar 2020 23:38:54 GMT  
		Size: 93.5 MB (93494538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead5918efa91f150d4991d381d85158e23cdab0f832fd73a318fb4af300348d1`  
		Last Modified: Wed, 11 Mar 2020 23:38:09 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b8dc5e80e6329a94b954cc8673d91fa2222d35ee9569178e1e0502c6ed2d14`  
		Last Modified: Wed, 11 Mar 2020 23:38:10 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a47d981e96991c1baf1c50d2090a8accbe1a377c893fd4d7aa22e580bb24e35`  
		Last Modified: Wed, 11 Mar 2020 23:38:09 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3-xenial`

```console
$ docker pull mongo@sha256:dbdd944e50ed4f45174aae05205e284b76166e3ac9801b6f15856b79fb3f595b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:3-xenial` - linux; amd64

```console
$ docker pull mongo@sha256:557aaf306c611bf9cd04e69fc3174757e2ce25ecc073a88fe28dbc889f5dae9a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.6 MB (165644020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3fdbdf0f17b70466eda08d155b2f1c72bc3450d23b8a752a4a841a83d6eb76f`
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
# Sat, 22 Feb 2020 01:08:24 GMT
ENV GOSU_VERSION=1.11
# Sat, 22 Feb 2020 01:08:24 GMT
ENV JSYAML_VERSION=3.13.0
# Sat, 22 Feb 2020 01:08:40 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 22 Feb 2020 01:08:40 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 22 Feb 2020 01:08:41 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Sat, 22 Feb 2020 01:08:41 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Sat, 22 Feb 2020 01:08:42 GMT
ARG MONGO_PACKAGE=mongodb-org
# Sat, 22 Feb 2020 01:08:42 GMT
ARG MONGO_REPO=repo.mongodb.org
# Sat, 22 Feb 2020 01:08:42 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Sat, 22 Feb 2020 01:08:42 GMT
ENV MONGO_MAJOR=3.6
# Sat, 22 Feb 2020 01:08:42 GMT
ENV MONGO_VERSION=3.6.17
# Sat, 22 Feb 2020 01:08:43 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Sat, 22 Feb 2020 01:09:04 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Sat, 22 Feb 2020 01:09:05 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Sat, 22 Feb 2020 01:09:05 GMT
VOLUME [/data/db /data/configdb]
# Sat, 22 Feb 2020 01:09:05 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Sat, 22 Feb 2020 01:09:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 22 Feb 2020 01:09:06 GMT
EXPOSE 27017
# Sat, 22 Feb 2020 01:09:06 GMT
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
	-	`sha256:7f706fb8c773a1773b04049e2fc1aa9f63e9f8b1ecbaae99fcf970f69c417f18`  
		Last Modified: Sat, 22 Feb 2020 01:11:01 GMT  
		Size: 1.2 MB (1243833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f137797464445cc1df1f6510d063791f41c4be58a91cbde2d7c9e9d5985cab6d`  
		Last Modified: Sat, 22 Feb 2020 01:11:01 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a03380f32ca06a89bb8bbb6437140f7feaa8cbc73656efd413066485af7bed9`  
		Last Modified: Sat, 22 Feb 2020 01:11:00 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a38c136f14bc4cc8e7c8b75a1b58fbd13ee66ab4018835cce5deafd77e34629`  
		Last Modified: Sat, 22 Feb 2020 01:11:00 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0e875b59ceec4323d6455ddef1a97e267ed64e723a3785961db869da21e662`  
		Last Modified: Sat, 22 Feb 2020 01:11:19 GMT  
		Size: 117.3 MB (117252414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f55b4999cd606166300c3bcc0c29bbdb69f9e442f652f9e2a1b037ff63069d`  
		Last Modified: Sat, 22 Feb 2020 01:11:00 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc92ef8de8b080701461ef5a44e3df6e2b20f0e5d0502bc9c2f58fb0c18884c`  
		Last Modified: Sat, 22 Feb 2020 01:11:00 GMT  
		Size: 4.0 KB (3953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3-xenial` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:8d00f2129c233839b0192bc63ad1b38d732559eb063a8c7fb6afd9b14000dfe9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155054951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:904d1cc8fa66fbab1604f0f278d0125cf824c48dde0e06e2de53f80f21123a3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 21 Feb 2020 21:55:42 GMT
ADD file:61b91c95a686740a57740470b7a1fe64d2479c56c36c69ca1222d870e78d44cc in / 
# Fri, 21 Feb 2020 21:55:46 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 21:55:48 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:55:50 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:55:50 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:48:01 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 21 Feb 2020 22:48:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:48:17 GMT
ENV GOSU_VERSION=1.11
# Fri, 21 Feb 2020 22:48:19 GMT
ENV JSYAML_VERSION=3.13.0
# Fri, 21 Feb 2020 22:48:47 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 21 Feb 2020 22:48:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:48:51 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Fri, 21 Feb 2020 22:48:53 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:48:54 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 21 Feb 2020 22:48:54 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:48:55 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:48:56 GMT
ENV MONGO_MAJOR=3.6
# Fri, 21 Feb 2020 22:48:57 GMT
ENV MONGO_VERSION=3.6.17
# Fri, 21 Feb 2020 22:48:59 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 21 Feb 2020 22:49:21 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 21 Feb 2020 22:49:23 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 21 Feb 2020 22:49:24 GMT
VOLUME [/data/db /data/configdb]
# Fri, 21 Feb 2020 22:49:24 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:49:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:49:26 GMT
EXPOSE 27017
# Fri, 21 Feb 2020 22:49:27 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a7bab9946de3c22ecccd832a0910adc2ffa82eea53f83c600d5ebce9e5422ad0`  
		Last Modified: Mon, 17 Feb 2020 15:45:27 GMT  
		Size: 39.9 MB (39940373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38630c4d9093f5b60806171ca7fa47a70d7ab28eeed25edfad43fb91d5f9f825`  
		Last Modified: Fri, 21 Feb 2020 21:56:39 GMT  
		Size: 467.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef678cbe74d844c6a114c1158a8c8868b412b7c5ed3a4c159831975a4915db9`  
		Last Modified: Fri, 21 Feb 2020 21:56:39 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78928743b0e778df64b15ac919705702ee0a080c2586f43c4349b35180de3c36`  
		Last Modified: Fri, 21 Feb 2020 21:56:40 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b98e127168243d033826ae375801cd9bde48991cd8c3f70195b2393e612fdd`  
		Last Modified: Fri, 21 Feb 2020 22:52:35 GMT  
		Size: 2.0 KB (1989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd8b81c3e37e64b559f25587bfdcb850b0f99e789d079c3a5e23aedc76a5b133`  
		Last Modified: Fri, 21 Feb 2020 22:52:35 GMT  
		Size: 2.5 MB (2474933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5133614dc076c55be0b03423a8f81053612df19fc888c3a5e65cf096386ca61a`  
		Last Modified: Fri, 21 Feb 2020 22:52:35 GMT  
		Size: 1.2 MB (1170004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa274bfc4efdade7b87ff58757777040775bd689e0478b13c0325ace270c75b`  
		Last Modified: Fri, 21 Feb 2020 22:52:35 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c551726d412935a665a5faa37ba35c6b578c9b4b9a04e15fbb8141e18c469f4`  
		Last Modified: Fri, 21 Feb 2020 22:52:33 GMT  
		Size: 2.0 KB (1995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690416c5e0de4a88eb11a3f888d668dffc71c64ce9928810382a5f989ea0d6d8`  
		Last Modified: Fri, 21 Feb 2020 22:52:33 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466edf90a60ac36b2e4ef9846aac45cf6dcbf6603561ff365607d6ec8e1d4333`  
		Last Modified: Fri, 21 Feb 2020 22:53:01 GMT  
		Size: 111.5 MB (111459661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a78ae9c5bd995e33cabe28ea21119ec5a46c4ecd1c7a5b80beedf81e226048`  
		Last Modified: Fri, 21 Feb 2020 22:52:33 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddfad788e158cc0e6900c305454fae286feb8c8e9807a24c9e4a962a22727dfc`  
		Last Modified: Fri, 21 Feb 2020 22:52:33 GMT  
		Size: 4.0 KB (3953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4`

```console
$ docker pull mongo@sha256:a1f116a08f48359302d7b567bdccc8b047bb0e534044de91be908c39eb796707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x
	-	windows version 10.0.14393.3506; amd64
	-	windows version 10.0.17763.1098; amd64

### `mongo:4` - linux; amd64

```console
$ docker pull mongo@sha256:c6e1710fc73d5a878ebc8b98c28d8897d5a4bbbb0e5d7ad758264d913e21ee71
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (163996273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcef5fd2979dbcbf76e46139680bf71c35925e344afa4703de43bdc44c6c526a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 21 Feb 2020 22:20:39 GMT
ADD file:91a750fb184711fde03c9172f41e8a907ccbb1bfb904c2c3f4ef595fcddbc3a9 in / 
# Fri, 21 Feb 2020 22:20:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:20:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:20:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:20:44 GMT
CMD ["/bin/bash"]
# Sat, 22 Feb 2020 01:09:51 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Sat, 22 Feb 2020 01:10:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 01:10:01 GMT
ENV GOSU_VERSION=1.11
# Sat, 22 Feb 2020 01:10:01 GMT
ENV JSYAML_VERSION=3.13.0
# Sat, 22 Feb 2020 01:10:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 22 Feb 2020 01:10:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 22 Feb 2020 01:10:19 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Sat, 22 Feb 2020 01:10:20 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Sat, 22 Feb 2020 01:10:20 GMT
ARG MONGO_PACKAGE=mongodb-org
# Sat, 22 Feb 2020 01:10:20 GMT
ARG MONGO_REPO=repo.mongodb.org
# Sat, 22 Feb 2020 01:10:20 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Sat, 22 Feb 2020 01:10:21 GMT
ENV MONGO_MAJOR=4.2
# Sat, 22 Feb 2020 01:10:21 GMT
ENV MONGO_VERSION=4.2.3
# Sat, 22 Feb 2020 01:10:21 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Sat, 22 Feb 2020 01:10:39 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Sat, 22 Feb 2020 01:10:40 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Sat, 22 Feb 2020 01:10:40 GMT
VOLUME [/data/db /data/configdb]
# Sat, 22 Feb 2020 01:10:40 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Sat, 22 Feb 2020 01:10:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 22 Feb 2020 01:10:41 GMT
EXPOSE 27017
# Sat, 22 Feb 2020 01:10:41 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:423ae2b273f4c17ceee9e8482fa8d071d90c7d052ae208e1fe4963fceb3d6954`  
		Last Modified: Wed, 19 Feb 2020 13:21:21 GMT  
		Size: 26.7 MB (26692096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de83a2304fa1f7c4a13708a0d15b9704f5945c2be5cbb2b3ed9b2ccb718d0b3d`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a83bce3af0648efaa60b9bb28225b09136d2d35d0bed25ac764297076dec1b`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b53be908de2c0c78070fff0a9f04835211b3156c4e73785747af365e71a0d7`  
		Last Modified: Fri, 21 Feb 2020 22:22:50 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cc2fb4f0eb1b8b82496ad1e17ec728355d84d889f8fd43ac357de9c6daaae6`  
		Last Modified: Sat, 22 Feb 2020 01:11:46 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f552d845039c0b94c06de56dc454b604142c32a69268bbc374a05470cc888431`  
		Last Modified: Sat, 22 Feb 2020 01:11:47 GMT  
		Size: 3.0 MB (2982680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6e166a9814b17b9c5dc683a8a35855eea3d9a898f77c0ee310f2038f29fce6`  
		Last Modified: Sat, 22 Feb 2020 01:11:47 GMT  
		Size: 5.8 MB (5764092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2ba5bee263bb3922f6c6a693b088d8d4753d4d90c05edd7534c2d80fc66358`  
		Last Modified: Sat, 22 Feb 2020 01:11:46 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828a1244f9760b1f6ff171f61f81c4fb01be2128e86e070c53e5b90658c40c8f`  
		Last Modified: Sat, 22 Feb 2020 01:11:45 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63a86989a84986d2b7e0e4ba20e65cdf25b2785771363571320bcd39f1d3494`  
		Last Modified: Sat, 22 Feb 2020 01:11:45 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc2ee27e8bbd1744066620810df67cf8b783b2b658f3edc0c852d75bfae74ca`  
		Last Modified: Sat, 22 Feb 2020 01:12:03 GMT  
		Size: 128.5 MB (128513279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a06e64657c7706873ecc5363ca322af486258b0e2a7c26fab7f46343ba622e`  
		Last Modified: Sat, 22 Feb 2020 01:11:45 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca7a59243040eff21e5c6d08a9e1b6b3be459f869ac615b51ec2a4949948128`  
		Last Modified: Sat, 22 Feb 2020 01:11:45 GMT  
		Size: 4.0 KB (3954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:d06ed06348a9b1815c5bc265d58f3706762f8a10fd9d7b4f1b9b7bb83f1673c9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (154023756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91cd6dddcfbe299cfe0222a6a9bc21d01f7b4561a6cb63efce4975d09b957c26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 21 Feb 2020 21:54:16 GMT
ADD file:d827a0b8f08011678a718254c1220408c7e6c7ab03ae4259b415542309f18578 in / 
# Fri, 21 Feb 2020 21:54:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:54:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:54:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:54:25 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:50:43 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 21 Feb 2020 22:51:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:51:02 GMT
ENV GOSU_VERSION=1.11
# Fri, 21 Feb 2020 22:51:03 GMT
ENV JSYAML_VERSION=3.13.0
# Fri, 21 Feb 2020 22:51:30 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 21 Feb 2020 22:51:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:51:33 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 21 Feb 2020 22:51:35 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:51:35 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 21 Feb 2020 22:51:37 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:51:37 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:51:38 GMT
ENV MONGO_MAJOR=4.2
# Fri, 21 Feb 2020 22:51:39 GMT
ENV MONGO_VERSION=4.2.3
# Fri, 21 Feb 2020 22:51:41 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 21 Feb 2020 22:52:11 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 21 Feb 2020 22:52:13 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 21 Feb 2020 22:52:14 GMT
VOLUME [/data/db /data/configdb]
# Fri, 21 Feb 2020 22:52:14 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:52:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:52:16 GMT
EXPOSE 27017
# Fri, 21 Feb 2020 22:52:16 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:6695dc10aaa5cd71c433dfb366e84804eb5fbee91eab1e113442040d6ef4c9e0`  
		Last Modified: Fri, 21 Feb 2020 21:56:13 GMT  
		Size: 23.7 MB (23721143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72aab8f928deff72c9b5867c93524a60e3f8cf1b7401c88b0ede8dc3c595e828`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e83b6447acdea2afff1a10052ebc551d15bfd1d2a93a202699f7a458c612c07`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6a91485a919c412d218b6441c339f691079ff88e6d28734b1cc3d5938cf58d`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce30eb24f9ee36f81283e24d44464d289f8925925dd29948021da9875c68ada`  
		Last Modified: Fri, 21 Feb 2020 22:53:51 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40c1d7ad1d1ea72814e10a3a2a7a82e998ae6f374122d24456bbda9bf38e068`  
		Last Modified: Fri, 21 Feb 2020 22:53:51 GMT  
		Size: 2.7 MB (2676051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c7fbc92b61b056c0d3a8e0b548ffe9f5d488c6ea126c0a27d97efbb4f4befad`  
		Last Modified: Fri, 21 Feb 2020 22:53:51 GMT  
		Size: 5.3 MB (5283262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31687588808d10bf423bf6473235a0ba3c81ee24391fcb307a550ef4f12161e`  
		Last Modified: Fri, 21 Feb 2020 22:53:50 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd05cdedee7f57674a001111e63e8d59a002bf511c3878b74313795359de0d7`  
		Last Modified: Fri, 21 Feb 2020 22:53:47 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af7b837ad38bf29cafd860d9a45a0ac68d398991d2c18660806e4d9bd570ba2e`  
		Last Modified: Fri, 21 Feb 2020 22:53:48 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1886e577ef072dc81cbc19ec5cb5da2cd43a40a0b8bfd5cc1f649630a8e350c`  
		Last Modified: Fri, 21 Feb 2020 22:54:13 GMT  
		Size: 122.3 MB (122299237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c2758fd66f09bc1675a0459df7ac7f51a7226772ca6f84430622c6f74fe6cb`  
		Last Modified: Fri, 21 Feb 2020 22:53:47 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf80da1fa0a60da920fc9b9f3f655290968ebb2335db548ad307c952fd6d933`  
		Last Modified: Fri, 21 Feb 2020 22:53:48 GMT  
		Size: 4.0 KB (3952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4` - linux; s390x

```console
$ docker pull mongo@sha256:f680daf0de2259244447be2895d266431defeebea01fba22433c12ffec9bdb01
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.9 MB (159948448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1d6d571c4e0118b833c5aad42620aa5ec5f67c8d3f1f4f9d65e677e88e4b4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 21 Feb 2020 21:57:46 GMT
ADD file:7925c9b35ffa1870e7d336ddcdd6c3434715178c7d08ff2ce9796b651302c347 in / 
# Fri, 21 Feb 2020 21:57:50 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:57:51 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:57:53 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:57:53 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:35:53 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 21 Feb 2020 22:36:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:36:07 GMT
ENV GOSU_VERSION=1.11
# Fri, 21 Feb 2020 22:36:08 GMT
ENV JSYAML_VERSION=3.13.0
# Fri, 21 Feb 2020 22:36:32 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 21 Feb 2020 22:36:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:36:35 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 21 Feb 2020 22:36:37 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:36:38 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 21 Feb 2020 22:36:38 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:36:39 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:36:40 GMT
ENV MONGO_MAJOR=4.2
# Fri, 21 Feb 2020 22:36:40 GMT
ENV MONGO_VERSION=4.2.3
# Fri, 21 Feb 2020 22:36:42 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 21 Feb 2020 22:37:22 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 21 Feb 2020 22:37:34 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 21 Feb 2020 22:37:35 GMT
VOLUME [/data/db /data/configdb]
# Fri, 21 Feb 2020 22:37:35 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:37:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:37:36 GMT
EXPOSE 27017
# Fri, 21 Feb 2020 22:37:37 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:b84fcb37dc33cf7416e0f1cf1219e16a15ab0d1c3aa4638d362f19c2679451de`  
		Last Modified: Fri, 21 Feb 2020 21:59:09 GMT  
		Size: 25.4 MB (25365672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9594931f903b7b3c4f5cb63196d29d715c50b567c128a5572131c12a25f04139`  
		Last Modified: Fri, 21 Feb 2020 21:59:06 GMT  
		Size: 36.2 KB (36186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66af13675c2330803d61d2198bb4f69c36bb7eed2d2b2bc3660fed8e873dce59`  
		Last Modified: Fri, 21 Feb 2020 21:59:11 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae0fb7b2ee5c5bc387374bdd08f53541bdfcf678d9b9f83489c3923af65fed0`  
		Last Modified: Fri, 21 Feb 2020 21:59:21 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20167b6352cf148caf092b98ebcd5a57b9008a2bc70e24c6a1aa4b6d54597e4`  
		Last Modified: Fri, 21 Feb 2020 22:38:04 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2c5aee18e04f08b2d2246738dd9239c3fc17fbc5629693a785574101ac5259`  
		Last Modified: Fri, 21 Feb 2020 22:38:03 GMT  
		Size: 2.7 MB (2714796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:679a24e64e261a1b368092a0ac88f8c4caf2a56ddbeb080a0b8d40e8892e07d5`  
		Last Modified: Fri, 21 Feb 2020 22:38:02 GMT  
		Size: 5.7 MB (5686031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a3aec4f6061abbba88c3ade7fef1e34e6fd70dbe30c3a9b5f0fbc64d2958e8`  
		Last Modified: Fri, 21 Feb 2020 22:38:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd8c5c1c54681c13c0b8c3a2bc57867973e945d847f5d9eadddbe4368c77540`  
		Last Modified: Fri, 21 Feb 2020 22:37:59 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f7fb2198b888d79b72c745d2130adc19213398ae3fac9631e98c6a8f6f128f`  
		Last Modified: Fri, 21 Feb 2020 22:37:59 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f630485b2c56c8706faa0a45bb123c968dc150a878e45eba0014ce3ca4d235`  
		Last Modified: Fri, 21 Feb 2020 22:38:19 GMT  
		Size: 126.1 MB (126136898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64555c5c853ffac8525a186c8038b7e67d4fbcc02d07f8e129e6ae70e5ca668f`  
		Last Modified: Fri, 21 Feb 2020 22:38:05 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d128c4bb10ec54ee27fce624769033a0191750dbc6b46a63a576aed005f086f`  
		Last Modified: Fri, 21 Feb 2020 22:38:04 GMT  
		Size: 4.0 KB (3952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4` - windows version 10.0.14393.3506; amd64

```console
$ docker pull mongo@sha256:ffcd7945296fd6bf2d492a8fbd2d76b87b4d700b617a3dbc3113ad3609dc1e99
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5823379228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b1841c6da45b9f09da659b319ee3ec76161c255d3a0299c744e58541cf1d5f`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 05:12:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 20 Feb 2020 05:31:28 GMT
ENV MONGO_VERSION=4.2.3
# Wed, 11 Mar 2020 22:59:46 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.3-signed.msi
# Wed, 11 Mar 2020 22:59:47 GMT
ENV MONGO_DOWNLOAD_SHA256=234f6abf9c4947df94428f6ce648905dbf6b1269f48cc3239ebd4990bde1ca2a
# Wed, 11 Mar 2020 23:17:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Mar 2020 23:17:16 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Mar 2020 23:17:18 GMT
EXPOSE 27017
# Wed, 11 Mar 2020 23:17:19 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:846a2223e9e7a88a2a07d706553f144d380483d72fb9f0697c4fcd71773a8693`  
		Size: 1.7 GB (1657079102 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0961c48658cd7865bcf6c05285dfbe8ad89cd52059088d7f4eed6fde1bb2b385`  
		Last Modified: Thu, 20 Feb 2020 05:18:25 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53763da721aa3ae58cd704805589abe169e1d3d28218280db0ed4045881d52cc`  
		Last Modified: Thu, 20 Feb 2020 05:44:18 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28575cbb1dce05be3e8ec069dac86a4ae8b751008d4f0c9654ea8a5adb6a05d`  
		Last Modified: Wed, 11 Mar 2020 23:40:27 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b0fd752a2977b6c56e9008cdf13c5221932c0fa7d04c8b82af7b1e365d7dcb`  
		Last Modified: Wed, 11 Mar 2020 23:40:24 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a599774a11cf582afd1c631f47ee898b2d7b7bd6c85e6a169f55999aebaf3f`  
		Last Modified: Wed, 11 Mar 2020 23:40:50 GMT  
		Size: 96.3 MB (96305864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158acd728c1a7f81dc5ab0e6ab015b47dbfe43d906b6935e6b3fb5af9ac717c9`  
		Last Modified: Wed, 11 Mar 2020 23:40:25 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1207ac339b253e1f2d5d984071f0cd6b1c14321de6258b95f05756828577ef`  
		Last Modified: Wed, 11 Mar 2020 23:40:24 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7bafe8e7fe89107a1cc111971c17ff5bfed4f23c13b7e8351d50dfedc51894`  
		Last Modified: Wed, 11 Mar 2020 23:40:24 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4` - windows version 10.0.17763.1098; amd64

```console
$ docker pull mongo@sha256:aac754de81af2f5d162c77a945382332cffd5575897c7601ef472343cb844896
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2720597037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d0aaebe9da6481c2ac37ceef6336551122a88bb8c6e0f0273b2b1408c89f3a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Tue, 10 Mar 2020 23:23:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Mar 2020 23:17:35 GMT
ENV MONGO_VERSION=4.2.3
# Wed, 11 Mar 2020 23:17:36 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.3-signed.msi
# Wed, 11 Mar 2020 23:17:37 GMT
ENV MONGO_DOWNLOAD_SHA256=234f6abf9c4947df94428f6ce648905dbf6b1269f48cc3239ebd4990bde1ca2a
# Wed, 11 Mar 2020 23:37:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Mar 2020 23:37:05 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Mar 2020 23:37:08 GMT
EXPOSE 27017
# Wed, 11 Mar 2020 23:37:09 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb49f89affc2d69b541463d095fdfbe61fa62e02b0aa5fa6d26bc134fb66bf35`  
		Last Modified: Wed, 11 Mar 2020 00:30:48 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a556cdd1dac3043338300637cf3645822f875ee02355952ab1cd7751e1b68bc`  
		Last Modified: Wed, 11 Mar 2020 23:41:10 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcc51a0e27cfe040ead7b64a7c6a800c4c738b534689744bc5736c486935beb`  
		Last Modified: Wed, 11 Mar 2020 23:41:10 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f7203b7c8fc0a4e01010792bc0a916bb1d80725bd8a4e8f11428ee3160d35f`  
		Last Modified: Wed, 11 Mar 2020 23:41:07 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22af9a292df27880e2bdab8b6325e55b0ca496959f7b3cbc864addc1d08d102d`  
		Last Modified: Wed, 11 Mar 2020 23:42:15 GMT  
		Size: 455.3 MB (455252292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb17de172b016b72e14b1ad1dc7b0d91f65115cd25a7268d5758b93956a3298f`  
		Last Modified: Wed, 11 Mar 2020 23:41:07 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a4339164f7d75bf46ec45b216b30960178423acd470a8d3f7fa23bcadb1e05`  
		Last Modified: Wed, 11 Mar 2020 23:41:07 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf29d93e6248494f3397e2328ebfe14d053d0679135d2853daa7460ecf197df7`  
		Last Modified: Wed, 11 Mar 2020 23:41:08 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.0`

```console
$ docker pull mongo@sha256:3bb5fbd6047f7ab2d2a72643c12aaefaa8633ac67d2882ec0db4e54430a06490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.14393.3506; amd64
	-	windows version 10.0.17763.1098; amd64

### `mongo:4.0` - linux; amd64

```console
$ docker pull mongo@sha256:1405a8f6e31677ff4b3294194dcd06e146dc0bad2a630eb284788e94231127a5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.5 MB (153507849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ca2473194af6f177c878788bbbec0464f9f3a1cbb747b2851005461e0a602a8`
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
# Sat, 22 Feb 2020 01:08:24 GMT
ENV GOSU_VERSION=1.11
# Sat, 22 Feb 2020 01:08:24 GMT
ENV JSYAML_VERSION=3.13.0
# Sat, 22 Feb 2020 01:08:40 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 22 Feb 2020 01:08:40 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 22 Feb 2020 01:09:18 GMT
ENV GPG_KEYS=9DA31620334BD75D9DCB49F368818C72E52529D4
# Sat, 22 Feb 2020 01:09:19 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Sat, 22 Feb 2020 01:09:19 GMT
ARG MONGO_PACKAGE=mongodb-org
# Sat, 22 Feb 2020 01:09:19 GMT
ARG MONGO_REPO=repo.mongodb.org
# Sat, 22 Feb 2020 01:09:20 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Sat, 22 Feb 2020 01:09:20 GMT
ENV MONGO_MAJOR=4.0
# Sat, 22 Feb 2020 01:09:20 GMT
ENV MONGO_VERSION=4.0.16
# Sat, 22 Feb 2020 01:09:21 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Sat, 22 Feb 2020 01:09:42 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Sat, 22 Feb 2020 01:09:43 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Sat, 22 Feb 2020 01:09:43 GMT
VOLUME [/data/db /data/configdb]
# Sat, 22 Feb 2020 01:09:44 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Sat, 22 Feb 2020 01:09:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 22 Feb 2020 01:09:44 GMT
EXPOSE 27017
# Sat, 22 Feb 2020 01:09:44 GMT
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
	-	`sha256:7f706fb8c773a1773b04049e2fc1aa9f63e9f8b1ecbaae99fcf970f69c417f18`  
		Last Modified: Sat, 22 Feb 2020 01:11:01 GMT  
		Size: 1.2 MB (1243833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f137797464445cc1df1f6510d063791f41c4be58a91cbde2d7c9e9d5985cab6d`  
		Last Modified: Sat, 22 Feb 2020 01:11:01 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba1898ebd41f26efc884bea6eb4a7ee3ef6ce3b48ed6be03ab56b4d6621921b`  
		Last Modified: Sat, 22 Feb 2020 01:11:24 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98214b9220d1755014dadb1062ca0353c17a9a1e27fa7f98ab774a3620e765a`  
		Last Modified: Sat, 22 Feb 2020 01:11:24 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b1d18aff5c75efc72089efe20c56e3f17fd0bd26810c852970943c90e0630d`  
		Last Modified: Sat, 22 Feb 2020 01:11:40 GMT  
		Size: 105.1 MB (105116807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b06bee133e4751d624d692f0465deba7e7caa19ec110cf7ed2be9a2677763d9`  
		Last Modified: Sat, 22 Feb 2020 01:11:24 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd9b651222ae34454628d7df9170651dbc190b288174cc079128130d2fe7659`  
		Last Modified: Sat, 22 Feb 2020 01:11:24 GMT  
		Size: 4.0 KB (3954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:bee1429bdd24d4ea23d22e00c2443443cda977011ad7342962b1af23d37b0f43
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143151410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:371eda185f2d3aaae409703639ec4f24171f49527e4df518ce35401cf6d12c68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 21 Feb 2020 21:55:42 GMT
ADD file:61b91c95a686740a57740470b7a1fe64d2479c56c36c69ca1222d870e78d44cc in / 
# Fri, 21 Feb 2020 21:55:46 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 21:55:48 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:55:50 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:55:50 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:48:01 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 21 Feb 2020 22:48:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:48:17 GMT
ENV GOSU_VERSION=1.11
# Fri, 21 Feb 2020 22:48:19 GMT
ENV JSYAML_VERSION=3.13.0
# Fri, 21 Feb 2020 22:48:47 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 21 Feb 2020 22:48:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:49:43 GMT
ENV GPG_KEYS=9DA31620334BD75D9DCB49F368818C72E52529D4
# Fri, 21 Feb 2020 22:49:45 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:49:46 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 21 Feb 2020 22:49:47 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:49:47 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:49:48 GMT
ENV MONGO_MAJOR=4.0
# Fri, 21 Feb 2020 22:49:48 GMT
ENV MONGO_VERSION=4.0.16
# Fri, 21 Feb 2020 22:49:51 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 21 Feb 2020 22:50:21 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 21 Feb 2020 22:50:26 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 21 Feb 2020 22:50:27 GMT
VOLUME [/data/db /data/configdb]
# Fri, 21 Feb 2020 22:50:28 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:50:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:50:30 GMT
EXPOSE 27017
# Fri, 21 Feb 2020 22:50:31 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a7bab9946de3c22ecccd832a0910adc2ffa82eea53f83c600d5ebce9e5422ad0`  
		Last Modified: Mon, 17 Feb 2020 15:45:27 GMT  
		Size: 39.9 MB (39940373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38630c4d9093f5b60806171ca7fa47a70d7ab28eeed25edfad43fb91d5f9f825`  
		Last Modified: Fri, 21 Feb 2020 21:56:39 GMT  
		Size: 467.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef678cbe74d844c6a114c1158a8c8868b412b7c5ed3a4c159831975a4915db9`  
		Last Modified: Fri, 21 Feb 2020 21:56:39 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78928743b0e778df64b15ac919705702ee0a080c2586f43c4349b35180de3c36`  
		Last Modified: Fri, 21 Feb 2020 21:56:40 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b98e127168243d033826ae375801cd9bde48991cd8c3f70195b2393e612fdd`  
		Last Modified: Fri, 21 Feb 2020 22:52:35 GMT  
		Size: 2.0 KB (1989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd8b81c3e37e64b559f25587bfdcb850b0f99e789d079c3a5e23aedc76a5b133`  
		Last Modified: Fri, 21 Feb 2020 22:52:35 GMT  
		Size: 2.5 MB (2474933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5133614dc076c55be0b03423a8f81053612df19fc888c3a5e65cf096386ca61a`  
		Last Modified: Fri, 21 Feb 2020 22:52:35 GMT  
		Size: 1.2 MB (1170004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa274bfc4efdade7b87ff58757777040775bd689e0478b13c0325ace270c75b`  
		Last Modified: Fri, 21 Feb 2020 22:52:35 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb69e090ce7c1babcfff2b727157954d5d146b17548d8bb27049c97f915f5cea`  
		Last Modified: Fri, 21 Feb 2020 22:53:11 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7a9e90c489535d54e2e10e06c7b9af4bbc05b31b7cc2a3d35c14504cf74583`  
		Last Modified: Fri, 21 Feb 2020 22:53:10 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c5b6cb9cca3e4e988a406ebfb0fe73313988d8dfa82d88b290d8ca22fedace`  
		Last Modified: Fri, 21 Feb 2020 22:53:36 GMT  
		Size: 99.6 MB (99556685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba940fc12ab744cc237dbe74ff0eade5fd77afadde1c293944ff3d7364d9a05`  
		Last Modified: Fri, 21 Feb 2020 22:53:11 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ca1d218e0af74a4dbc4e2db95d6461988ee1ba31f49d5b7e61e45bbd555333`  
		Last Modified: Fri, 21 Feb 2020 22:53:11 GMT  
		Size: 4.0 KB (3954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0` - windows version 10.0.14393.3506; amd64

```console
$ docker pull mongo@sha256:74305d6a0eaf1089e8ac7203997efdbbe4d9c929b5d3c1b829d1c5f7019d70bb
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5813768790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba36e25199332dcf2b256d38677f467e12d190d7ef2354958dd21ed2341093d6`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 05:12:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 20 Feb 2020 05:23:32 GMT
ENV MONGO_VERSION=4.0.16
# Wed, 11 Mar 2020 22:28:39 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.16-signed.msi
# Wed, 11 Mar 2020 22:28:40 GMT
ENV MONGO_DOWNLOAD_SHA256=d871d52110ed3c6600273d44e557ab63fc4104aa84b6115ad4dc0b68f90c062d
# Wed, 11 Mar 2020 22:43:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Mar 2020 22:43:40 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Mar 2020 22:43:41 GMT
EXPOSE 27017
# Wed, 11 Mar 2020 22:43:42 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:846a2223e9e7a88a2a07d706553f144d380483d72fb9f0697c4fcd71773a8693`  
		Size: 1.7 GB (1657079102 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0961c48658cd7865bcf6c05285dfbe8ad89cd52059088d7f4eed6fde1bb2b385`  
		Last Modified: Thu, 20 Feb 2020 05:18:25 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b95eaa46f6dc274081bb617c326301e6db7eafe7025fbca86204b56386d5e4`  
		Last Modified: Thu, 20 Feb 2020 05:41:39 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9125b6c8e897838ea7a35f82cf6aca35e5e680367fa6d57c8041103ddcab811f`  
		Last Modified: Wed, 11 Mar 2020 23:39:11 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb4788e0c8c73e11b8f5224f59735b530b9739bbbd635a841e5d0b55f74be95`  
		Last Modified: Wed, 11 Mar 2020 23:39:09 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d7d77ced793c11fbcc96d46ee7ad769b9b9396c7708defd235e63aa65e0fa6`  
		Last Modified: Wed, 11 Mar 2020 23:39:37 GMT  
		Size: 86.7 MB (86695418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a870095f969440cd5c45ac9070f7feb895ab88b2e81bf9001d43154c26ca1780`  
		Last Modified: Wed, 11 Mar 2020 23:39:08 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3659b02cfc5d56e87dae7010fa7250547c5130aaa5eda3ad3c969c2517ff193e`  
		Last Modified: Wed, 11 Mar 2020 23:39:08 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd685dcbcd4362c893d98232d13d1b9d37c929701a06412d09d0ae9c79dfb19e`  
		Last Modified: Wed, 11 Mar 2020 23:39:08 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0` - windows version 10.0.17763.1098; amd64

```console
$ docker pull mongo@sha256:d572896df16d388fdd2c996fbe0000478c28addd99a3125df445f846d4c370e2
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2351177202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bcd11758fd33911df7c1ebf8588f0c0f3e719faa59e7c543d0779e3424f019a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Tue, 10 Mar 2020 23:23:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 10 Mar 2020 23:23:23 GMT
ENV MONGO_VERSION=4.0.16
# Wed, 11 Mar 2020 22:43:57 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.16-signed.msi
# Wed, 11 Mar 2020 22:43:58 GMT
ENV MONGO_DOWNLOAD_SHA256=d871d52110ed3c6600273d44e557ab63fc4104aa84b6115ad4dc0b68f90c062d
# Wed, 11 Mar 2020 22:59:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Mar 2020 22:59:26 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Mar 2020 22:59:29 GMT
EXPOSE 27017
# Wed, 11 Mar 2020 22:59:31 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb49f89affc2d69b541463d095fdfbe61fa62e02b0aa5fa6d26bc134fb66bf35`  
		Last Modified: Wed, 11 Mar 2020 00:30:48 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672d2344ef682ac901927ee26dde837d8edafb029d3889536fd885d149a60b98`  
		Last Modified: Wed, 11 Mar 2020 00:30:47 GMT  
		Size: 1.2 KB (1215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36cb64b0c869a5e7853c6b68f41924f002596d4910d6f10270a0720a3cf4eff2`  
		Last Modified: Wed, 11 Mar 2020 23:39:50 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695030bb83bb861be142bd3fd66b9891af9fe0411d44040366f5475f377dc390`  
		Last Modified: Wed, 11 Mar 2020 23:39:48 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39cee58b67c5b7e0e1a1ab2da864494fccf18612ca2c4e257d524ad6c30f185e`  
		Last Modified: Wed, 11 Mar 2020 23:40:13 GMT  
		Size: 85.8 MB (85832453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49414bd8bac7bd6c2f4b567a69b29f7c43561d8d881544f3b5956b9516f94843`  
		Last Modified: Wed, 11 Mar 2020 23:39:48 GMT  
		Size: 1.2 KB (1199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cfb786fc61b3d0a6725c78fe526aa00cd0a1e2b7289ca6d32dc074c8823e018`  
		Last Modified: Wed, 11 Mar 2020 23:39:48 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820c433db6a551c20e48ece7ad3c6b97fc7a91564887e40b4de9752452c04c5e`  
		Last Modified: Wed, 11 Mar 2020 23:39:48 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.0.16`

```console
$ docker pull mongo@sha256:3bb5fbd6047f7ab2d2a72643c12aaefaa8633ac67d2882ec0db4e54430a06490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.14393.3506; amd64
	-	windows version 10.0.17763.1098; amd64

### `mongo:4.0.16` - linux; amd64

```console
$ docker pull mongo@sha256:1405a8f6e31677ff4b3294194dcd06e146dc0bad2a630eb284788e94231127a5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.5 MB (153507849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ca2473194af6f177c878788bbbec0464f9f3a1cbb747b2851005461e0a602a8`
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
# Sat, 22 Feb 2020 01:08:24 GMT
ENV GOSU_VERSION=1.11
# Sat, 22 Feb 2020 01:08:24 GMT
ENV JSYAML_VERSION=3.13.0
# Sat, 22 Feb 2020 01:08:40 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 22 Feb 2020 01:08:40 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 22 Feb 2020 01:09:18 GMT
ENV GPG_KEYS=9DA31620334BD75D9DCB49F368818C72E52529D4
# Sat, 22 Feb 2020 01:09:19 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Sat, 22 Feb 2020 01:09:19 GMT
ARG MONGO_PACKAGE=mongodb-org
# Sat, 22 Feb 2020 01:09:19 GMT
ARG MONGO_REPO=repo.mongodb.org
# Sat, 22 Feb 2020 01:09:20 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Sat, 22 Feb 2020 01:09:20 GMT
ENV MONGO_MAJOR=4.0
# Sat, 22 Feb 2020 01:09:20 GMT
ENV MONGO_VERSION=4.0.16
# Sat, 22 Feb 2020 01:09:21 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Sat, 22 Feb 2020 01:09:42 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Sat, 22 Feb 2020 01:09:43 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Sat, 22 Feb 2020 01:09:43 GMT
VOLUME [/data/db /data/configdb]
# Sat, 22 Feb 2020 01:09:44 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Sat, 22 Feb 2020 01:09:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 22 Feb 2020 01:09:44 GMT
EXPOSE 27017
# Sat, 22 Feb 2020 01:09:44 GMT
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
	-	`sha256:7f706fb8c773a1773b04049e2fc1aa9f63e9f8b1ecbaae99fcf970f69c417f18`  
		Last Modified: Sat, 22 Feb 2020 01:11:01 GMT  
		Size: 1.2 MB (1243833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f137797464445cc1df1f6510d063791f41c4be58a91cbde2d7c9e9d5985cab6d`  
		Last Modified: Sat, 22 Feb 2020 01:11:01 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba1898ebd41f26efc884bea6eb4a7ee3ef6ce3b48ed6be03ab56b4d6621921b`  
		Last Modified: Sat, 22 Feb 2020 01:11:24 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98214b9220d1755014dadb1062ca0353c17a9a1e27fa7f98ab774a3620e765a`  
		Last Modified: Sat, 22 Feb 2020 01:11:24 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b1d18aff5c75efc72089efe20c56e3f17fd0bd26810c852970943c90e0630d`  
		Last Modified: Sat, 22 Feb 2020 01:11:40 GMT  
		Size: 105.1 MB (105116807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b06bee133e4751d624d692f0465deba7e7caa19ec110cf7ed2be9a2677763d9`  
		Last Modified: Sat, 22 Feb 2020 01:11:24 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd9b651222ae34454628d7df9170651dbc190b288174cc079128130d2fe7659`  
		Last Modified: Sat, 22 Feb 2020 01:11:24 GMT  
		Size: 4.0 KB (3954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0.16` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:bee1429bdd24d4ea23d22e00c2443443cda977011ad7342962b1af23d37b0f43
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143151410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:371eda185f2d3aaae409703639ec4f24171f49527e4df518ce35401cf6d12c68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 21 Feb 2020 21:55:42 GMT
ADD file:61b91c95a686740a57740470b7a1fe64d2479c56c36c69ca1222d870e78d44cc in / 
# Fri, 21 Feb 2020 21:55:46 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 21:55:48 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:55:50 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:55:50 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:48:01 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 21 Feb 2020 22:48:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:48:17 GMT
ENV GOSU_VERSION=1.11
# Fri, 21 Feb 2020 22:48:19 GMT
ENV JSYAML_VERSION=3.13.0
# Fri, 21 Feb 2020 22:48:47 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 21 Feb 2020 22:48:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:49:43 GMT
ENV GPG_KEYS=9DA31620334BD75D9DCB49F368818C72E52529D4
# Fri, 21 Feb 2020 22:49:45 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:49:46 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 21 Feb 2020 22:49:47 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:49:47 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:49:48 GMT
ENV MONGO_MAJOR=4.0
# Fri, 21 Feb 2020 22:49:48 GMT
ENV MONGO_VERSION=4.0.16
# Fri, 21 Feb 2020 22:49:51 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 21 Feb 2020 22:50:21 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 21 Feb 2020 22:50:26 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 21 Feb 2020 22:50:27 GMT
VOLUME [/data/db /data/configdb]
# Fri, 21 Feb 2020 22:50:28 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:50:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:50:30 GMT
EXPOSE 27017
# Fri, 21 Feb 2020 22:50:31 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a7bab9946de3c22ecccd832a0910adc2ffa82eea53f83c600d5ebce9e5422ad0`  
		Last Modified: Mon, 17 Feb 2020 15:45:27 GMT  
		Size: 39.9 MB (39940373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38630c4d9093f5b60806171ca7fa47a70d7ab28eeed25edfad43fb91d5f9f825`  
		Last Modified: Fri, 21 Feb 2020 21:56:39 GMT  
		Size: 467.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef678cbe74d844c6a114c1158a8c8868b412b7c5ed3a4c159831975a4915db9`  
		Last Modified: Fri, 21 Feb 2020 21:56:39 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78928743b0e778df64b15ac919705702ee0a080c2586f43c4349b35180de3c36`  
		Last Modified: Fri, 21 Feb 2020 21:56:40 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b98e127168243d033826ae375801cd9bde48991cd8c3f70195b2393e612fdd`  
		Last Modified: Fri, 21 Feb 2020 22:52:35 GMT  
		Size: 2.0 KB (1989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd8b81c3e37e64b559f25587bfdcb850b0f99e789d079c3a5e23aedc76a5b133`  
		Last Modified: Fri, 21 Feb 2020 22:52:35 GMT  
		Size: 2.5 MB (2474933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5133614dc076c55be0b03423a8f81053612df19fc888c3a5e65cf096386ca61a`  
		Last Modified: Fri, 21 Feb 2020 22:52:35 GMT  
		Size: 1.2 MB (1170004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa274bfc4efdade7b87ff58757777040775bd689e0478b13c0325ace270c75b`  
		Last Modified: Fri, 21 Feb 2020 22:52:35 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb69e090ce7c1babcfff2b727157954d5d146b17548d8bb27049c97f915f5cea`  
		Last Modified: Fri, 21 Feb 2020 22:53:11 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7a9e90c489535d54e2e10e06c7b9af4bbc05b31b7cc2a3d35c14504cf74583`  
		Last Modified: Fri, 21 Feb 2020 22:53:10 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c5b6cb9cca3e4e988a406ebfb0fe73313988d8dfa82d88b290d8ca22fedace`  
		Last Modified: Fri, 21 Feb 2020 22:53:36 GMT  
		Size: 99.6 MB (99556685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba940fc12ab744cc237dbe74ff0eade5fd77afadde1c293944ff3d7364d9a05`  
		Last Modified: Fri, 21 Feb 2020 22:53:11 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ca1d218e0af74a4dbc4e2db95d6461988ee1ba31f49d5b7e61e45bbd555333`  
		Last Modified: Fri, 21 Feb 2020 22:53:11 GMT  
		Size: 4.0 KB (3954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0.16` - windows version 10.0.14393.3506; amd64

```console
$ docker pull mongo@sha256:74305d6a0eaf1089e8ac7203997efdbbe4d9c929b5d3c1b829d1c5f7019d70bb
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5813768790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba36e25199332dcf2b256d38677f467e12d190d7ef2354958dd21ed2341093d6`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 05:12:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 20 Feb 2020 05:23:32 GMT
ENV MONGO_VERSION=4.0.16
# Wed, 11 Mar 2020 22:28:39 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.16-signed.msi
# Wed, 11 Mar 2020 22:28:40 GMT
ENV MONGO_DOWNLOAD_SHA256=d871d52110ed3c6600273d44e557ab63fc4104aa84b6115ad4dc0b68f90c062d
# Wed, 11 Mar 2020 22:43:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Mar 2020 22:43:40 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Mar 2020 22:43:41 GMT
EXPOSE 27017
# Wed, 11 Mar 2020 22:43:42 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:846a2223e9e7a88a2a07d706553f144d380483d72fb9f0697c4fcd71773a8693`  
		Size: 1.7 GB (1657079102 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0961c48658cd7865bcf6c05285dfbe8ad89cd52059088d7f4eed6fde1bb2b385`  
		Last Modified: Thu, 20 Feb 2020 05:18:25 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b95eaa46f6dc274081bb617c326301e6db7eafe7025fbca86204b56386d5e4`  
		Last Modified: Thu, 20 Feb 2020 05:41:39 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9125b6c8e897838ea7a35f82cf6aca35e5e680367fa6d57c8041103ddcab811f`  
		Last Modified: Wed, 11 Mar 2020 23:39:11 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb4788e0c8c73e11b8f5224f59735b530b9739bbbd635a841e5d0b55f74be95`  
		Last Modified: Wed, 11 Mar 2020 23:39:09 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d7d77ced793c11fbcc96d46ee7ad769b9b9396c7708defd235e63aa65e0fa6`  
		Last Modified: Wed, 11 Mar 2020 23:39:37 GMT  
		Size: 86.7 MB (86695418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a870095f969440cd5c45ac9070f7feb895ab88b2e81bf9001d43154c26ca1780`  
		Last Modified: Wed, 11 Mar 2020 23:39:08 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3659b02cfc5d56e87dae7010fa7250547c5130aaa5eda3ad3c969c2517ff193e`  
		Last Modified: Wed, 11 Mar 2020 23:39:08 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd685dcbcd4362c893d98232d13d1b9d37c929701a06412d09d0ae9c79dfb19e`  
		Last Modified: Wed, 11 Mar 2020 23:39:08 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0.16` - windows version 10.0.17763.1098; amd64

```console
$ docker pull mongo@sha256:d572896df16d388fdd2c996fbe0000478c28addd99a3125df445f846d4c370e2
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2351177202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bcd11758fd33911df7c1ebf8588f0c0f3e719faa59e7c543d0779e3424f019a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Tue, 10 Mar 2020 23:23:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 10 Mar 2020 23:23:23 GMT
ENV MONGO_VERSION=4.0.16
# Wed, 11 Mar 2020 22:43:57 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.16-signed.msi
# Wed, 11 Mar 2020 22:43:58 GMT
ENV MONGO_DOWNLOAD_SHA256=d871d52110ed3c6600273d44e557ab63fc4104aa84b6115ad4dc0b68f90c062d
# Wed, 11 Mar 2020 22:59:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Mar 2020 22:59:26 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Mar 2020 22:59:29 GMT
EXPOSE 27017
# Wed, 11 Mar 2020 22:59:31 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb49f89affc2d69b541463d095fdfbe61fa62e02b0aa5fa6d26bc134fb66bf35`  
		Last Modified: Wed, 11 Mar 2020 00:30:48 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672d2344ef682ac901927ee26dde837d8edafb029d3889536fd885d149a60b98`  
		Last Modified: Wed, 11 Mar 2020 00:30:47 GMT  
		Size: 1.2 KB (1215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36cb64b0c869a5e7853c6b68f41924f002596d4910d6f10270a0720a3cf4eff2`  
		Last Modified: Wed, 11 Mar 2020 23:39:50 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695030bb83bb861be142bd3fd66b9891af9fe0411d44040366f5475f377dc390`  
		Last Modified: Wed, 11 Mar 2020 23:39:48 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39cee58b67c5b7e0e1a1ab2da864494fccf18612ca2c4e257d524ad6c30f185e`  
		Last Modified: Wed, 11 Mar 2020 23:40:13 GMT  
		Size: 85.8 MB (85832453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49414bd8bac7bd6c2f4b567a69b29f7c43561d8d881544f3b5956b9516f94843`  
		Last Modified: Wed, 11 Mar 2020 23:39:48 GMT  
		Size: 1.2 KB (1199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cfb786fc61b3d0a6725c78fe526aa00cd0a1e2b7289ca6d32dc074c8823e018`  
		Last Modified: Wed, 11 Mar 2020 23:39:48 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820c433db6a551c20e48ece7ad3c6b97fc7a91564887e40b4de9752452c04c5e`  
		Last Modified: Wed, 11 Mar 2020 23:39:48 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.0.16-windowsservercore`

```console
$ docker pull mongo@sha256:a87718b58c7d124ea2046738e40259ceeab00f01197c000816b49e579b108741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3506; amd64
	-	windows version 10.0.17763.1098; amd64

### `mongo:4.0.16-windowsservercore` - windows version 10.0.14393.3506; amd64

```console
$ docker pull mongo@sha256:74305d6a0eaf1089e8ac7203997efdbbe4d9c929b5d3c1b829d1c5f7019d70bb
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5813768790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba36e25199332dcf2b256d38677f467e12d190d7ef2354958dd21ed2341093d6`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 05:12:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 20 Feb 2020 05:23:32 GMT
ENV MONGO_VERSION=4.0.16
# Wed, 11 Mar 2020 22:28:39 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.16-signed.msi
# Wed, 11 Mar 2020 22:28:40 GMT
ENV MONGO_DOWNLOAD_SHA256=d871d52110ed3c6600273d44e557ab63fc4104aa84b6115ad4dc0b68f90c062d
# Wed, 11 Mar 2020 22:43:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Mar 2020 22:43:40 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Mar 2020 22:43:41 GMT
EXPOSE 27017
# Wed, 11 Mar 2020 22:43:42 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:846a2223e9e7a88a2a07d706553f144d380483d72fb9f0697c4fcd71773a8693`  
		Size: 1.7 GB (1657079102 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0961c48658cd7865bcf6c05285dfbe8ad89cd52059088d7f4eed6fde1bb2b385`  
		Last Modified: Thu, 20 Feb 2020 05:18:25 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b95eaa46f6dc274081bb617c326301e6db7eafe7025fbca86204b56386d5e4`  
		Last Modified: Thu, 20 Feb 2020 05:41:39 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9125b6c8e897838ea7a35f82cf6aca35e5e680367fa6d57c8041103ddcab811f`  
		Last Modified: Wed, 11 Mar 2020 23:39:11 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb4788e0c8c73e11b8f5224f59735b530b9739bbbd635a841e5d0b55f74be95`  
		Last Modified: Wed, 11 Mar 2020 23:39:09 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d7d77ced793c11fbcc96d46ee7ad769b9b9396c7708defd235e63aa65e0fa6`  
		Last Modified: Wed, 11 Mar 2020 23:39:37 GMT  
		Size: 86.7 MB (86695418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a870095f969440cd5c45ac9070f7feb895ab88b2e81bf9001d43154c26ca1780`  
		Last Modified: Wed, 11 Mar 2020 23:39:08 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3659b02cfc5d56e87dae7010fa7250547c5130aaa5eda3ad3c969c2517ff193e`  
		Last Modified: Wed, 11 Mar 2020 23:39:08 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd685dcbcd4362c893d98232d13d1b9d37c929701a06412d09d0ae9c79dfb19e`  
		Last Modified: Wed, 11 Mar 2020 23:39:08 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0.16-windowsservercore` - windows version 10.0.17763.1098; amd64

```console
$ docker pull mongo@sha256:d572896df16d388fdd2c996fbe0000478c28addd99a3125df445f846d4c370e2
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2351177202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bcd11758fd33911df7c1ebf8588f0c0f3e719faa59e7c543d0779e3424f019a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Tue, 10 Mar 2020 23:23:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 10 Mar 2020 23:23:23 GMT
ENV MONGO_VERSION=4.0.16
# Wed, 11 Mar 2020 22:43:57 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.16-signed.msi
# Wed, 11 Mar 2020 22:43:58 GMT
ENV MONGO_DOWNLOAD_SHA256=d871d52110ed3c6600273d44e557ab63fc4104aa84b6115ad4dc0b68f90c062d
# Wed, 11 Mar 2020 22:59:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Mar 2020 22:59:26 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Mar 2020 22:59:29 GMT
EXPOSE 27017
# Wed, 11 Mar 2020 22:59:31 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb49f89affc2d69b541463d095fdfbe61fa62e02b0aa5fa6d26bc134fb66bf35`  
		Last Modified: Wed, 11 Mar 2020 00:30:48 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672d2344ef682ac901927ee26dde837d8edafb029d3889536fd885d149a60b98`  
		Last Modified: Wed, 11 Mar 2020 00:30:47 GMT  
		Size: 1.2 KB (1215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36cb64b0c869a5e7853c6b68f41924f002596d4910d6f10270a0720a3cf4eff2`  
		Last Modified: Wed, 11 Mar 2020 23:39:50 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695030bb83bb861be142bd3fd66b9891af9fe0411d44040366f5475f377dc390`  
		Last Modified: Wed, 11 Mar 2020 23:39:48 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39cee58b67c5b7e0e1a1ab2da864494fccf18612ca2c4e257d524ad6c30f185e`  
		Last Modified: Wed, 11 Mar 2020 23:40:13 GMT  
		Size: 85.8 MB (85832453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49414bd8bac7bd6c2f4b567a69b29f7c43561d8d881544f3b5956b9516f94843`  
		Last Modified: Wed, 11 Mar 2020 23:39:48 GMT  
		Size: 1.2 KB (1199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cfb786fc61b3d0a6725c78fe526aa00cd0a1e2b7289ca6d32dc074c8823e018`  
		Last Modified: Wed, 11 Mar 2020 23:39:48 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820c433db6a551c20e48ece7ad3c6b97fc7a91564887e40b4de9752452c04c5e`  
		Last Modified: Wed, 11 Mar 2020 23:39:48 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.0.16-windowsservercore-1809`

```console
$ docker pull mongo@sha256:98c93a3db5e82b248de2b5c14d7d5229edb09d20b2088d27c7c2cb036c20ba21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `mongo:4.0.16-windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull mongo@sha256:d572896df16d388fdd2c996fbe0000478c28addd99a3125df445f846d4c370e2
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2351177202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bcd11758fd33911df7c1ebf8588f0c0f3e719faa59e7c543d0779e3424f019a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Tue, 10 Mar 2020 23:23:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 10 Mar 2020 23:23:23 GMT
ENV MONGO_VERSION=4.0.16
# Wed, 11 Mar 2020 22:43:57 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.16-signed.msi
# Wed, 11 Mar 2020 22:43:58 GMT
ENV MONGO_DOWNLOAD_SHA256=d871d52110ed3c6600273d44e557ab63fc4104aa84b6115ad4dc0b68f90c062d
# Wed, 11 Mar 2020 22:59:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Mar 2020 22:59:26 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Mar 2020 22:59:29 GMT
EXPOSE 27017
# Wed, 11 Mar 2020 22:59:31 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb49f89affc2d69b541463d095fdfbe61fa62e02b0aa5fa6d26bc134fb66bf35`  
		Last Modified: Wed, 11 Mar 2020 00:30:48 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672d2344ef682ac901927ee26dde837d8edafb029d3889536fd885d149a60b98`  
		Last Modified: Wed, 11 Mar 2020 00:30:47 GMT  
		Size: 1.2 KB (1215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36cb64b0c869a5e7853c6b68f41924f002596d4910d6f10270a0720a3cf4eff2`  
		Last Modified: Wed, 11 Mar 2020 23:39:50 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695030bb83bb861be142bd3fd66b9891af9fe0411d44040366f5475f377dc390`  
		Last Modified: Wed, 11 Mar 2020 23:39:48 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39cee58b67c5b7e0e1a1ab2da864494fccf18612ca2c4e257d524ad6c30f185e`  
		Last Modified: Wed, 11 Mar 2020 23:40:13 GMT  
		Size: 85.8 MB (85832453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49414bd8bac7bd6c2f4b567a69b29f7c43561d8d881544f3b5956b9516f94843`  
		Last Modified: Wed, 11 Mar 2020 23:39:48 GMT  
		Size: 1.2 KB (1199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cfb786fc61b3d0a6725c78fe526aa00cd0a1e2b7289ca6d32dc074c8823e018`  
		Last Modified: Wed, 11 Mar 2020 23:39:48 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820c433db6a551c20e48ece7ad3c6b97fc7a91564887e40b4de9752452c04c5e`  
		Last Modified: Wed, 11 Mar 2020 23:39:48 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.0.16-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:4502eaf87cfa21f5c509f6f388027c1332304c06e6fd34da5ed1a6a4aad63241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3506; amd64

### `mongo:4.0.16-windowsservercore-ltsc2016` - windows version 10.0.14393.3506; amd64

```console
$ docker pull mongo@sha256:74305d6a0eaf1089e8ac7203997efdbbe4d9c929b5d3c1b829d1c5f7019d70bb
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5813768790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba36e25199332dcf2b256d38677f467e12d190d7ef2354958dd21ed2341093d6`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 05:12:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 20 Feb 2020 05:23:32 GMT
ENV MONGO_VERSION=4.0.16
# Wed, 11 Mar 2020 22:28:39 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.16-signed.msi
# Wed, 11 Mar 2020 22:28:40 GMT
ENV MONGO_DOWNLOAD_SHA256=d871d52110ed3c6600273d44e557ab63fc4104aa84b6115ad4dc0b68f90c062d
# Wed, 11 Mar 2020 22:43:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Mar 2020 22:43:40 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Mar 2020 22:43:41 GMT
EXPOSE 27017
# Wed, 11 Mar 2020 22:43:42 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:846a2223e9e7a88a2a07d706553f144d380483d72fb9f0697c4fcd71773a8693`  
		Size: 1.7 GB (1657079102 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0961c48658cd7865bcf6c05285dfbe8ad89cd52059088d7f4eed6fde1bb2b385`  
		Last Modified: Thu, 20 Feb 2020 05:18:25 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b95eaa46f6dc274081bb617c326301e6db7eafe7025fbca86204b56386d5e4`  
		Last Modified: Thu, 20 Feb 2020 05:41:39 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9125b6c8e897838ea7a35f82cf6aca35e5e680367fa6d57c8041103ddcab811f`  
		Last Modified: Wed, 11 Mar 2020 23:39:11 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb4788e0c8c73e11b8f5224f59735b530b9739bbbd635a841e5d0b55f74be95`  
		Last Modified: Wed, 11 Mar 2020 23:39:09 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d7d77ced793c11fbcc96d46ee7ad769b9b9396c7708defd235e63aa65e0fa6`  
		Last Modified: Wed, 11 Mar 2020 23:39:37 GMT  
		Size: 86.7 MB (86695418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a870095f969440cd5c45ac9070f7feb895ab88b2e81bf9001d43154c26ca1780`  
		Last Modified: Wed, 11 Mar 2020 23:39:08 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3659b02cfc5d56e87dae7010fa7250547c5130aaa5eda3ad3c969c2517ff193e`  
		Last Modified: Wed, 11 Mar 2020 23:39:08 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd685dcbcd4362c893d98232d13d1b9d37c929701a06412d09d0ae9c79dfb19e`  
		Last Modified: Wed, 11 Mar 2020 23:39:08 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.0.16-xenial`

```console
$ docker pull mongo@sha256:419735b40840fb9fa69f30d78db7973e3040dff5e19cbcf11129f67ecd530ce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:4.0.16-xenial` - linux; amd64

```console
$ docker pull mongo@sha256:1405a8f6e31677ff4b3294194dcd06e146dc0bad2a630eb284788e94231127a5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.5 MB (153507849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ca2473194af6f177c878788bbbec0464f9f3a1cbb747b2851005461e0a602a8`
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
# Sat, 22 Feb 2020 01:08:24 GMT
ENV GOSU_VERSION=1.11
# Sat, 22 Feb 2020 01:08:24 GMT
ENV JSYAML_VERSION=3.13.0
# Sat, 22 Feb 2020 01:08:40 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 22 Feb 2020 01:08:40 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 22 Feb 2020 01:09:18 GMT
ENV GPG_KEYS=9DA31620334BD75D9DCB49F368818C72E52529D4
# Sat, 22 Feb 2020 01:09:19 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Sat, 22 Feb 2020 01:09:19 GMT
ARG MONGO_PACKAGE=mongodb-org
# Sat, 22 Feb 2020 01:09:19 GMT
ARG MONGO_REPO=repo.mongodb.org
# Sat, 22 Feb 2020 01:09:20 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Sat, 22 Feb 2020 01:09:20 GMT
ENV MONGO_MAJOR=4.0
# Sat, 22 Feb 2020 01:09:20 GMT
ENV MONGO_VERSION=4.0.16
# Sat, 22 Feb 2020 01:09:21 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Sat, 22 Feb 2020 01:09:42 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Sat, 22 Feb 2020 01:09:43 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Sat, 22 Feb 2020 01:09:43 GMT
VOLUME [/data/db /data/configdb]
# Sat, 22 Feb 2020 01:09:44 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Sat, 22 Feb 2020 01:09:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 22 Feb 2020 01:09:44 GMT
EXPOSE 27017
# Sat, 22 Feb 2020 01:09:44 GMT
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
	-	`sha256:7f706fb8c773a1773b04049e2fc1aa9f63e9f8b1ecbaae99fcf970f69c417f18`  
		Last Modified: Sat, 22 Feb 2020 01:11:01 GMT  
		Size: 1.2 MB (1243833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f137797464445cc1df1f6510d063791f41c4be58a91cbde2d7c9e9d5985cab6d`  
		Last Modified: Sat, 22 Feb 2020 01:11:01 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba1898ebd41f26efc884bea6eb4a7ee3ef6ce3b48ed6be03ab56b4d6621921b`  
		Last Modified: Sat, 22 Feb 2020 01:11:24 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98214b9220d1755014dadb1062ca0353c17a9a1e27fa7f98ab774a3620e765a`  
		Last Modified: Sat, 22 Feb 2020 01:11:24 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b1d18aff5c75efc72089efe20c56e3f17fd0bd26810c852970943c90e0630d`  
		Last Modified: Sat, 22 Feb 2020 01:11:40 GMT  
		Size: 105.1 MB (105116807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b06bee133e4751d624d692f0465deba7e7caa19ec110cf7ed2be9a2677763d9`  
		Last Modified: Sat, 22 Feb 2020 01:11:24 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd9b651222ae34454628d7df9170651dbc190b288174cc079128130d2fe7659`  
		Last Modified: Sat, 22 Feb 2020 01:11:24 GMT  
		Size: 4.0 KB (3954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0.16-xenial` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:bee1429bdd24d4ea23d22e00c2443443cda977011ad7342962b1af23d37b0f43
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143151410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:371eda185f2d3aaae409703639ec4f24171f49527e4df518ce35401cf6d12c68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 21 Feb 2020 21:55:42 GMT
ADD file:61b91c95a686740a57740470b7a1fe64d2479c56c36c69ca1222d870e78d44cc in / 
# Fri, 21 Feb 2020 21:55:46 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 21:55:48 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:55:50 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:55:50 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:48:01 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 21 Feb 2020 22:48:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:48:17 GMT
ENV GOSU_VERSION=1.11
# Fri, 21 Feb 2020 22:48:19 GMT
ENV JSYAML_VERSION=3.13.0
# Fri, 21 Feb 2020 22:48:47 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 21 Feb 2020 22:48:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:49:43 GMT
ENV GPG_KEYS=9DA31620334BD75D9DCB49F368818C72E52529D4
# Fri, 21 Feb 2020 22:49:45 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:49:46 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 21 Feb 2020 22:49:47 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:49:47 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:49:48 GMT
ENV MONGO_MAJOR=4.0
# Fri, 21 Feb 2020 22:49:48 GMT
ENV MONGO_VERSION=4.0.16
# Fri, 21 Feb 2020 22:49:51 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 21 Feb 2020 22:50:21 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 21 Feb 2020 22:50:26 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 21 Feb 2020 22:50:27 GMT
VOLUME [/data/db /data/configdb]
# Fri, 21 Feb 2020 22:50:28 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:50:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:50:30 GMT
EXPOSE 27017
# Fri, 21 Feb 2020 22:50:31 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a7bab9946de3c22ecccd832a0910adc2ffa82eea53f83c600d5ebce9e5422ad0`  
		Last Modified: Mon, 17 Feb 2020 15:45:27 GMT  
		Size: 39.9 MB (39940373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38630c4d9093f5b60806171ca7fa47a70d7ab28eeed25edfad43fb91d5f9f825`  
		Last Modified: Fri, 21 Feb 2020 21:56:39 GMT  
		Size: 467.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef678cbe74d844c6a114c1158a8c8868b412b7c5ed3a4c159831975a4915db9`  
		Last Modified: Fri, 21 Feb 2020 21:56:39 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78928743b0e778df64b15ac919705702ee0a080c2586f43c4349b35180de3c36`  
		Last Modified: Fri, 21 Feb 2020 21:56:40 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b98e127168243d033826ae375801cd9bde48991cd8c3f70195b2393e612fdd`  
		Last Modified: Fri, 21 Feb 2020 22:52:35 GMT  
		Size: 2.0 KB (1989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd8b81c3e37e64b559f25587bfdcb850b0f99e789d079c3a5e23aedc76a5b133`  
		Last Modified: Fri, 21 Feb 2020 22:52:35 GMT  
		Size: 2.5 MB (2474933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5133614dc076c55be0b03423a8f81053612df19fc888c3a5e65cf096386ca61a`  
		Last Modified: Fri, 21 Feb 2020 22:52:35 GMT  
		Size: 1.2 MB (1170004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa274bfc4efdade7b87ff58757777040775bd689e0478b13c0325ace270c75b`  
		Last Modified: Fri, 21 Feb 2020 22:52:35 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb69e090ce7c1babcfff2b727157954d5d146b17548d8bb27049c97f915f5cea`  
		Last Modified: Fri, 21 Feb 2020 22:53:11 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7a9e90c489535d54e2e10e06c7b9af4bbc05b31b7cc2a3d35c14504cf74583`  
		Last Modified: Fri, 21 Feb 2020 22:53:10 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c5b6cb9cca3e4e988a406ebfb0fe73313988d8dfa82d88b290d8ca22fedace`  
		Last Modified: Fri, 21 Feb 2020 22:53:36 GMT  
		Size: 99.6 MB (99556685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba940fc12ab744cc237dbe74ff0eade5fd77afadde1c293944ff3d7364d9a05`  
		Last Modified: Fri, 21 Feb 2020 22:53:11 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ca1d218e0af74a4dbc4e2db95d6461988ee1ba31f49d5b7e61e45bbd555333`  
		Last Modified: Fri, 21 Feb 2020 22:53:11 GMT  
		Size: 4.0 KB (3954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.0-windowsservercore`

```console
$ docker pull mongo@sha256:a87718b58c7d124ea2046738e40259ceeab00f01197c000816b49e579b108741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3506; amd64
	-	windows version 10.0.17763.1098; amd64

### `mongo:4.0-windowsservercore` - windows version 10.0.14393.3506; amd64

```console
$ docker pull mongo@sha256:74305d6a0eaf1089e8ac7203997efdbbe4d9c929b5d3c1b829d1c5f7019d70bb
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5813768790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba36e25199332dcf2b256d38677f467e12d190d7ef2354958dd21ed2341093d6`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 05:12:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 20 Feb 2020 05:23:32 GMT
ENV MONGO_VERSION=4.0.16
# Wed, 11 Mar 2020 22:28:39 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.16-signed.msi
# Wed, 11 Mar 2020 22:28:40 GMT
ENV MONGO_DOWNLOAD_SHA256=d871d52110ed3c6600273d44e557ab63fc4104aa84b6115ad4dc0b68f90c062d
# Wed, 11 Mar 2020 22:43:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Mar 2020 22:43:40 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Mar 2020 22:43:41 GMT
EXPOSE 27017
# Wed, 11 Mar 2020 22:43:42 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:846a2223e9e7a88a2a07d706553f144d380483d72fb9f0697c4fcd71773a8693`  
		Size: 1.7 GB (1657079102 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0961c48658cd7865bcf6c05285dfbe8ad89cd52059088d7f4eed6fde1bb2b385`  
		Last Modified: Thu, 20 Feb 2020 05:18:25 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b95eaa46f6dc274081bb617c326301e6db7eafe7025fbca86204b56386d5e4`  
		Last Modified: Thu, 20 Feb 2020 05:41:39 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9125b6c8e897838ea7a35f82cf6aca35e5e680367fa6d57c8041103ddcab811f`  
		Last Modified: Wed, 11 Mar 2020 23:39:11 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb4788e0c8c73e11b8f5224f59735b530b9739bbbd635a841e5d0b55f74be95`  
		Last Modified: Wed, 11 Mar 2020 23:39:09 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d7d77ced793c11fbcc96d46ee7ad769b9b9396c7708defd235e63aa65e0fa6`  
		Last Modified: Wed, 11 Mar 2020 23:39:37 GMT  
		Size: 86.7 MB (86695418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a870095f969440cd5c45ac9070f7feb895ab88b2e81bf9001d43154c26ca1780`  
		Last Modified: Wed, 11 Mar 2020 23:39:08 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3659b02cfc5d56e87dae7010fa7250547c5130aaa5eda3ad3c969c2517ff193e`  
		Last Modified: Wed, 11 Mar 2020 23:39:08 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd685dcbcd4362c893d98232d13d1b9d37c929701a06412d09d0ae9c79dfb19e`  
		Last Modified: Wed, 11 Mar 2020 23:39:08 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0-windowsservercore` - windows version 10.0.17763.1098; amd64

```console
$ docker pull mongo@sha256:d572896df16d388fdd2c996fbe0000478c28addd99a3125df445f846d4c370e2
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2351177202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bcd11758fd33911df7c1ebf8588f0c0f3e719faa59e7c543d0779e3424f019a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Tue, 10 Mar 2020 23:23:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 10 Mar 2020 23:23:23 GMT
ENV MONGO_VERSION=4.0.16
# Wed, 11 Mar 2020 22:43:57 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.16-signed.msi
# Wed, 11 Mar 2020 22:43:58 GMT
ENV MONGO_DOWNLOAD_SHA256=d871d52110ed3c6600273d44e557ab63fc4104aa84b6115ad4dc0b68f90c062d
# Wed, 11 Mar 2020 22:59:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Mar 2020 22:59:26 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Mar 2020 22:59:29 GMT
EXPOSE 27017
# Wed, 11 Mar 2020 22:59:31 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb49f89affc2d69b541463d095fdfbe61fa62e02b0aa5fa6d26bc134fb66bf35`  
		Last Modified: Wed, 11 Mar 2020 00:30:48 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672d2344ef682ac901927ee26dde837d8edafb029d3889536fd885d149a60b98`  
		Last Modified: Wed, 11 Mar 2020 00:30:47 GMT  
		Size: 1.2 KB (1215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36cb64b0c869a5e7853c6b68f41924f002596d4910d6f10270a0720a3cf4eff2`  
		Last Modified: Wed, 11 Mar 2020 23:39:50 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695030bb83bb861be142bd3fd66b9891af9fe0411d44040366f5475f377dc390`  
		Last Modified: Wed, 11 Mar 2020 23:39:48 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39cee58b67c5b7e0e1a1ab2da864494fccf18612ca2c4e257d524ad6c30f185e`  
		Last Modified: Wed, 11 Mar 2020 23:40:13 GMT  
		Size: 85.8 MB (85832453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49414bd8bac7bd6c2f4b567a69b29f7c43561d8d881544f3b5956b9516f94843`  
		Last Modified: Wed, 11 Mar 2020 23:39:48 GMT  
		Size: 1.2 KB (1199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cfb786fc61b3d0a6725c78fe526aa00cd0a1e2b7289ca6d32dc074c8823e018`  
		Last Modified: Wed, 11 Mar 2020 23:39:48 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820c433db6a551c20e48ece7ad3c6b97fc7a91564887e40b4de9752452c04c5e`  
		Last Modified: Wed, 11 Mar 2020 23:39:48 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.0-windowsservercore-1809`

```console
$ docker pull mongo@sha256:98c93a3db5e82b248de2b5c14d7d5229edb09d20b2088d27c7c2cb036c20ba21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `mongo:4.0-windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull mongo@sha256:d572896df16d388fdd2c996fbe0000478c28addd99a3125df445f846d4c370e2
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2351177202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bcd11758fd33911df7c1ebf8588f0c0f3e719faa59e7c543d0779e3424f019a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Tue, 10 Mar 2020 23:23:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 10 Mar 2020 23:23:23 GMT
ENV MONGO_VERSION=4.0.16
# Wed, 11 Mar 2020 22:43:57 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.16-signed.msi
# Wed, 11 Mar 2020 22:43:58 GMT
ENV MONGO_DOWNLOAD_SHA256=d871d52110ed3c6600273d44e557ab63fc4104aa84b6115ad4dc0b68f90c062d
# Wed, 11 Mar 2020 22:59:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Mar 2020 22:59:26 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Mar 2020 22:59:29 GMT
EXPOSE 27017
# Wed, 11 Mar 2020 22:59:31 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb49f89affc2d69b541463d095fdfbe61fa62e02b0aa5fa6d26bc134fb66bf35`  
		Last Modified: Wed, 11 Mar 2020 00:30:48 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672d2344ef682ac901927ee26dde837d8edafb029d3889536fd885d149a60b98`  
		Last Modified: Wed, 11 Mar 2020 00:30:47 GMT  
		Size: 1.2 KB (1215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36cb64b0c869a5e7853c6b68f41924f002596d4910d6f10270a0720a3cf4eff2`  
		Last Modified: Wed, 11 Mar 2020 23:39:50 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:695030bb83bb861be142bd3fd66b9891af9fe0411d44040366f5475f377dc390`  
		Last Modified: Wed, 11 Mar 2020 23:39:48 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39cee58b67c5b7e0e1a1ab2da864494fccf18612ca2c4e257d524ad6c30f185e`  
		Last Modified: Wed, 11 Mar 2020 23:40:13 GMT  
		Size: 85.8 MB (85832453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49414bd8bac7bd6c2f4b567a69b29f7c43561d8d881544f3b5956b9516f94843`  
		Last Modified: Wed, 11 Mar 2020 23:39:48 GMT  
		Size: 1.2 KB (1199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cfb786fc61b3d0a6725c78fe526aa00cd0a1e2b7289ca6d32dc074c8823e018`  
		Last Modified: Wed, 11 Mar 2020 23:39:48 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820c433db6a551c20e48ece7ad3c6b97fc7a91564887e40b4de9752452c04c5e`  
		Last Modified: Wed, 11 Mar 2020 23:39:48 GMT  
		Size: 1.2 KB (1222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.0-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:4502eaf87cfa21f5c509f6f388027c1332304c06e6fd34da5ed1a6a4aad63241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3506; amd64

### `mongo:4.0-windowsservercore-ltsc2016` - windows version 10.0.14393.3506; amd64

```console
$ docker pull mongo@sha256:74305d6a0eaf1089e8ac7203997efdbbe4d9c929b5d3c1b829d1c5f7019d70bb
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5813768790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba36e25199332dcf2b256d38677f467e12d190d7ef2354958dd21ed2341093d6`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 05:12:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 20 Feb 2020 05:23:32 GMT
ENV MONGO_VERSION=4.0.16
# Wed, 11 Mar 2020 22:28:39 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.16-signed.msi
# Wed, 11 Mar 2020 22:28:40 GMT
ENV MONGO_DOWNLOAD_SHA256=d871d52110ed3c6600273d44e557ab63fc4104aa84b6115ad4dc0b68f90c062d
# Wed, 11 Mar 2020 22:43:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Mar 2020 22:43:40 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Mar 2020 22:43:41 GMT
EXPOSE 27017
# Wed, 11 Mar 2020 22:43:42 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:846a2223e9e7a88a2a07d706553f144d380483d72fb9f0697c4fcd71773a8693`  
		Size: 1.7 GB (1657079102 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0961c48658cd7865bcf6c05285dfbe8ad89cd52059088d7f4eed6fde1bb2b385`  
		Last Modified: Thu, 20 Feb 2020 05:18:25 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b95eaa46f6dc274081bb617c326301e6db7eafe7025fbca86204b56386d5e4`  
		Last Modified: Thu, 20 Feb 2020 05:41:39 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9125b6c8e897838ea7a35f82cf6aca35e5e680367fa6d57c8041103ddcab811f`  
		Last Modified: Wed, 11 Mar 2020 23:39:11 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb4788e0c8c73e11b8f5224f59735b530b9739bbbd635a841e5d0b55f74be95`  
		Last Modified: Wed, 11 Mar 2020 23:39:09 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06d7d77ced793c11fbcc96d46ee7ad769b9b9396c7708defd235e63aa65e0fa6`  
		Last Modified: Wed, 11 Mar 2020 23:39:37 GMT  
		Size: 86.7 MB (86695418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a870095f969440cd5c45ac9070f7feb895ab88b2e81bf9001d43154c26ca1780`  
		Last Modified: Wed, 11 Mar 2020 23:39:08 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3659b02cfc5d56e87dae7010fa7250547c5130aaa5eda3ad3c969c2517ff193e`  
		Last Modified: Wed, 11 Mar 2020 23:39:08 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd685dcbcd4362c893d98232d13d1b9d37c929701a06412d09d0ae9c79dfb19e`  
		Last Modified: Wed, 11 Mar 2020 23:39:08 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.0-xenial`

```console
$ docker pull mongo@sha256:419735b40840fb9fa69f30d78db7973e3040dff5e19cbcf11129f67ecd530ce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:4.0-xenial` - linux; amd64

```console
$ docker pull mongo@sha256:1405a8f6e31677ff4b3294194dcd06e146dc0bad2a630eb284788e94231127a5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.5 MB (153507849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ca2473194af6f177c878788bbbec0464f9f3a1cbb747b2851005461e0a602a8`
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
# Sat, 22 Feb 2020 01:08:24 GMT
ENV GOSU_VERSION=1.11
# Sat, 22 Feb 2020 01:08:24 GMT
ENV JSYAML_VERSION=3.13.0
# Sat, 22 Feb 2020 01:08:40 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 22 Feb 2020 01:08:40 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 22 Feb 2020 01:09:18 GMT
ENV GPG_KEYS=9DA31620334BD75D9DCB49F368818C72E52529D4
# Sat, 22 Feb 2020 01:09:19 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Sat, 22 Feb 2020 01:09:19 GMT
ARG MONGO_PACKAGE=mongodb-org
# Sat, 22 Feb 2020 01:09:19 GMT
ARG MONGO_REPO=repo.mongodb.org
# Sat, 22 Feb 2020 01:09:20 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Sat, 22 Feb 2020 01:09:20 GMT
ENV MONGO_MAJOR=4.0
# Sat, 22 Feb 2020 01:09:20 GMT
ENV MONGO_VERSION=4.0.16
# Sat, 22 Feb 2020 01:09:21 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Sat, 22 Feb 2020 01:09:42 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Sat, 22 Feb 2020 01:09:43 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Sat, 22 Feb 2020 01:09:43 GMT
VOLUME [/data/db /data/configdb]
# Sat, 22 Feb 2020 01:09:44 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Sat, 22 Feb 2020 01:09:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 22 Feb 2020 01:09:44 GMT
EXPOSE 27017
# Sat, 22 Feb 2020 01:09:44 GMT
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
	-	`sha256:7f706fb8c773a1773b04049e2fc1aa9f63e9f8b1ecbaae99fcf970f69c417f18`  
		Last Modified: Sat, 22 Feb 2020 01:11:01 GMT  
		Size: 1.2 MB (1243833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f137797464445cc1df1f6510d063791f41c4be58a91cbde2d7c9e9d5985cab6d`  
		Last Modified: Sat, 22 Feb 2020 01:11:01 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba1898ebd41f26efc884bea6eb4a7ee3ef6ce3b48ed6be03ab56b4d6621921b`  
		Last Modified: Sat, 22 Feb 2020 01:11:24 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98214b9220d1755014dadb1062ca0353c17a9a1e27fa7f98ab774a3620e765a`  
		Last Modified: Sat, 22 Feb 2020 01:11:24 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b1d18aff5c75efc72089efe20c56e3f17fd0bd26810c852970943c90e0630d`  
		Last Modified: Sat, 22 Feb 2020 01:11:40 GMT  
		Size: 105.1 MB (105116807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b06bee133e4751d624d692f0465deba7e7caa19ec110cf7ed2be9a2677763d9`  
		Last Modified: Sat, 22 Feb 2020 01:11:24 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd9b651222ae34454628d7df9170651dbc190b288174cc079128130d2fe7659`  
		Last Modified: Sat, 22 Feb 2020 01:11:24 GMT  
		Size: 4.0 KB (3954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0-xenial` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:bee1429bdd24d4ea23d22e00c2443443cda977011ad7342962b1af23d37b0f43
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143151410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:371eda185f2d3aaae409703639ec4f24171f49527e4df518ce35401cf6d12c68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 21 Feb 2020 21:55:42 GMT
ADD file:61b91c95a686740a57740470b7a1fe64d2479c56c36c69ca1222d870e78d44cc in / 
# Fri, 21 Feb 2020 21:55:46 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 21:55:48 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:55:50 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:55:50 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:48:01 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 21 Feb 2020 22:48:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:48:17 GMT
ENV GOSU_VERSION=1.11
# Fri, 21 Feb 2020 22:48:19 GMT
ENV JSYAML_VERSION=3.13.0
# Fri, 21 Feb 2020 22:48:47 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 21 Feb 2020 22:48:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:49:43 GMT
ENV GPG_KEYS=9DA31620334BD75D9DCB49F368818C72E52529D4
# Fri, 21 Feb 2020 22:49:45 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:49:46 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 21 Feb 2020 22:49:47 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:49:47 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:49:48 GMT
ENV MONGO_MAJOR=4.0
# Fri, 21 Feb 2020 22:49:48 GMT
ENV MONGO_VERSION=4.0.16
# Fri, 21 Feb 2020 22:49:51 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 21 Feb 2020 22:50:21 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 21 Feb 2020 22:50:26 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 21 Feb 2020 22:50:27 GMT
VOLUME [/data/db /data/configdb]
# Fri, 21 Feb 2020 22:50:28 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:50:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:50:30 GMT
EXPOSE 27017
# Fri, 21 Feb 2020 22:50:31 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a7bab9946de3c22ecccd832a0910adc2ffa82eea53f83c600d5ebce9e5422ad0`  
		Last Modified: Mon, 17 Feb 2020 15:45:27 GMT  
		Size: 39.9 MB (39940373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38630c4d9093f5b60806171ca7fa47a70d7ab28eeed25edfad43fb91d5f9f825`  
		Last Modified: Fri, 21 Feb 2020 21:56:39 GMT  
		Size: 467.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef678cbe74d844c6a114c1158a8c8868b412b7c5ed3a4c159831975a4915db9`  
		Last Modified: Fri, 21 Feb 2020 21:56:39 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78928743b0e778df64b15ac919705702ee0a080c2586f43c4349b35180de3c36`  
		Last Modified: Fri, 21 Feb 2020 21:56:40 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b98e127168243d033826ae375801cd9bde48991cd8c3f70195b2393e612fdd`  
		Last Modified: Fri, 21 Feb 2020 22:52:35 GMT  
		Size: 2.0 KB (1989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd8b81c3e37e64b559f25587bfdcb850b0f99e789d079c3a5e23aedc76a5b133`  
		Last Modified: Fri, 21 Feb 2020 22:52:35 GMT  
		Size: 2.5 MB (2474933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5133614dc076c55be0b03423a8f81053612df19fc888c3a5e65cf096386ca61a`  
		Last Modified: Fri, 21 Feb 2020 22:52:35 GMT  
		Size: 1.2 MB (1170004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa274bfc4efdade7b87ff58757777040775bd689e0478b13c0325ace270c75b`  
		Last Modified: Fri, 21 Feb 2020 22:52:35 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb69e090ce7c1babcfff2b727157954d5d146b17548d8bb27049c97f915f5cea`  
		Last Modified: Fri, 21 Feb 2020 22:53:11 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7a9e90c489535d54e2e10e06c7b9af4bbc05b31b7cc2a3d35c14504cf74583`  
		Last Modified: Fri, 21 Feb 2020 22:53:10 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c5b6cb9cca3e4e988a406ebfb0fe73313988d8dfa82d88b290d8ca22fedace`  
		Last Modified: Fri, 21 Feb 2020 22:53:36 GMT  
		Size: 99.6 MB (99556685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba940fc12ab744cc237dbe74ff0eade5fd77afadde1c293944ff3d7364d9a05`  
		Last Modified: Fri, 21 Feb 2020 22:53:11 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ca1d218e0af74a4dbc4e2db95d6461988ee1ba31f49d5b7e61e45bbd555333`  
		Last Modified: Fri, 21 Feb 2020 22:53:11 GMT  
		Size: 4.0 KB (3954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.2`

```console
$ docker pull mongo@sha256:a1f116a08f48359302d7b567bdccc8b047bb0e534044de91be908c39eb796707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x
	-	windows version 10.0.14393.3506; amd64
	-	windows version 10.0.17763.1098; amd64

### `mongo:4.2` - linux; amd64

```console
$ docker pull mongo@sha256:c6e1710fc73d5a878ebc8b98c28d8897d5a4bbbb0e5d7ad758264d913e21ee71
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (163996273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcef5fd2979dbcbf76e46139680bf71c35925e344afa4703de43bdc44c6c526a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 21 Feb 2020 22:20:39 GMT
ADD file:91a750fb184711fde03c9172f41e8a907ccbb1bfb904c2c3f4ef595fcddbc3a9 in / 
# Fri, 21 Feb 2020 22:20:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:20:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:20:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:20:44 GMT
CMD ["/bin/bash"]
# Sat, 22 Feb 2020 01:09:51 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Sat, 22 Feb 2020 01:10:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 01:10:01 GMT
ENV GOSU_VERSION=1.11
# Sat, 22 Feb 2020 01:10:01 GMT
ENV JSYAML_VERSION=3.13.0
# Sat, 22 Feb 2020 01:10:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 22 Feb 2020 01:10:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 22 Feb 2020 01:10:19 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Sat, 22 Feb 2020 01:10:20 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Sat, 22 Feb 2020 01:10:20 GMT
ARG MONGO_PACKAGE=mongodb-org
# Sat, 22 Feb 2020 01:10:20 GMT
ARG MONGO_REPO=repo.mongodb.org
# Sat, 22 Feb 2020 01:10:20 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Sat, 22 Feb 2020 01:10:21 GMT
ENV MONGO_MAJOR=4.2
# Sat, 22 Feb 2020 01:10:21 GMT
ENV MONGO_VERSION=4.2.3
# Sat, 22 Feb 2020 01:10:21 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Sat, 22 Feb 2020 01:10:39 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Sat, 22 Feb 2020 01:10:40 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Sat, 22 Feb 2020 01:10:40 GMT
VOLUME [/data/db /data/configdb]
# Sat, 22 Feb 2020 01:10:40 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Sat, 22 Feb 2020 01:10:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 22 Feb 2020 01:10:41 GMT
EXPOSE 27017
# Sat, 22 Feb 2020 01:10:41 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:423ae2b273f4c17ceee9e8482fa8d071d90c7d052ae208e1fe4963fceb3d6954`  
		Last Modified: Wed, 19 Feb 2020 13:21:21 GMT  
		Size: 26.7 MB (26692096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de83a2304fa1f7c4a13708a0d15b9704f5945c2be5cbb2b3ed9b2ccb718d0b3d`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a83bce3af0648efaa60b9bb28225b09136d2d35d0bed25ac764297076dec1b`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b53be908de2c0c78070fff0a9f04835211b3156c4e73785747af365e71a0d7`  
		Last Modified: Fri, 21 Feb 2020 22:22:50 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cc2fb4f0eb1b8b82496ad1e17ec728355d84d889f8fd43ac357de9c6daaae6`  
		Last Modified: Sat, 22 Feb 2020 01:11:46 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f552d845039c0b94c06de56dc454b604142c32a69268bbc374a05470cc888431`  
		Last Modified: Sat, 22 Feb 2020 01:11:47 GMT  
		Size: 3.0 MB (2982680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6e166a9814b17b9c5dc683a8a35855eea3d9a898f77c0ee310f2038f29fce6`  
		Last Modified: Sat, 22 Feb 2020 01:11:47 GMT  
		Size: 5.8 MB (5764092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2ba5bee263bb3922f6c6a693b088d8d4753d4d90c05edd7534c2d80fc66358`  
		Last Modified: Sat, 22 Feb 2020 01:11:46 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828a1244f9760b1f6ff171f61f81c4fb01be2128e86e070c53e5b90658c40c8f`  
		Last Modified: Sat, 22 Feb 2020 01:11:45 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63a86989a84986d2b7e0e4ba20e65cdf25b2785771363571320bcd39f1d3494`  
		Last Modified: Sat, 22 Feb 2020 01:11:45 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc2ee27e8bbd1744066620810df67cf8b783b2b658f3edc0c852d75bfae74ca`  
		Last Modified: Sat, 22 Feb 2020 01:12:03 GMT  
		Size: 128.5 MB (128513279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a06e64657c7706873ecc5363ca322af486258b0e2a7c26fab7f46343ba622e`  
		Last Modified: Sat, 22 Feb 2020 01:11:45 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca7a59243040eff21e5c6d08a9e1b6b3be459f869ac615b51ec2a4949948128`  
		Last Modified: Sat, 22 Feb 2020 01:11:45 GMT  
		Size: 4.0 KB (3954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:d06ed06348a9b1815c5bc265d58f3706762f8a10fd9d7b4f1b9b7bb83f1673c9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (154023756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91cd6dddcfbe299cfe0222a6a9bc21d01f7b4561a6cb63efce4975d09b957c26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 21 Feb 2020 21:54:16 GMT
ADD file:d827a0b8f08011678a718254c1220408c7e6c7ab03ae4259b415542309f18578 in / 
# Fri, 21 Feb 2020 21:54:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:54:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:54:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:54:25 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:50:43 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 21 Feb 2020 22:51:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:51:02 GMT
ENV GOSU_VERSION=1.11
# Fri, 21 Feb 2020 22:51:03 GMT
ENV JSYAML_VERSION=3.13.0
# Fri, 21 Feb 2020 22:51:30 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 21 Feb 2020 22:51:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:51:33 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 21 Feb 2020 22:51:35 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:51:35 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 21 Feb 2020 22:51:37 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:51:37 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:51:38 GMT
ENV MONGO_MAJOR=4.2
# Fri, 21 Feb 2020 22:51:39 GMT
ENV MONGO_VERSION=4.2.3
# Fri, 21 Feb 2020 22:51:41 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 21 Feb 2020 22:52:11 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 21 Feb 2020 22:52:13 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 21 Feb 2020 22:52:14 GMT
VOLUME [/data/db /data/configdb]
# Fri, 21 Feb 2020 22:52:14 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:52:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:52:16 GMT
EXPOSE 27017
# Fri, 21 Feb 2020 22:52:16 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:6695dc10aaa5cd71c433dfb366e84804eb5fbee91eab1e113442040d6ef4c9e0`  
		Last Modified: Fri, 21 Feb 2020 21:56:13 GMT  
		Size: 23.7 MB (23721143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72aab8f928deff72c9b5867c93524a60e3f8cf1b7401c88b0ede8dc3c595e828`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e83b6447acdea2afff1a10052ebc551d15bfd1d2a93a202699f7a458c612c07`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6a91485a919c412d218b6441c339f691079ff88e6d28734b1cc3d5938cf58d`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce30eb24f9ee36f81283e24d44464d289f8925925dd29948021da9875c68ada`  
		Last Modified: Fri, 21 Feb 2020 22:53:51 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40c1d7ad1d1ea72814e10a3a2a7a82e998ae6f374122d24456bbda9bf38e068`  
		Last Modified: Fri, 21 Feb 2020 22:53:51 GMT  
		Size: 2.7 MB (2676051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c7fbc92b61b056c0d3a8e0b548ffe9f5d488c6ea126c0a27d97efbb4f4befad`  
		Last Modified: Fri, 21 Feb 2020 22:53:51 GMT  
		Size: 5.3 MB (5283262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31687588808d10bf423bf6473235a0ba3c81ee24391fcb307a550ef4f12161e`  
		Last Modified: Fri, 21 Feb 2020 22:53:50 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd05cdedee7f57674a001111e63e8d59a002bf511c3878b74313795359de0d7`  
		Last Modified: Fri, 21 Feb 2020 22:53:47 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af7b837ad38bf29cafd860d9a45a0ac68d398991d2c18660806e4d9bd570ba2e`  
		Last Modified: Fri, 21 Feb 2020 22:53:48 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1886e577ef072dc81cbc19ec5cb5da2cd43a40a0b8bfd5cc1f649630a8e350c`  
		Last Modified: Fri, 21 Feb 2020 22:54:13 GMT  
		Size: 122.3 MB (122299237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c2758fd66f09bc1675a0459df7ac7f51a7226772ca6f84430622c6f74fe6cb`  
		Last Modified: Fri, 21 Feb 2020 22:53:47 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf80da1fa0a60da920fc9b9f3f655290968ebb2335db548ad307c952fd6d933`  
		Last Modified: Fri, 21 Feb 2020 22:53:48 GMT  
		Size: 4.0 KB (3952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2` - linux; s390x

```console
$ docker pull mongo@sha256:f680daf0de2259244447be2895d266431defeebea01fba22433c12ffec9bdb01
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.9 MB (159948448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1d6d571c4e0118b833c5aad42620aa5ec5f67c8d3f1f4f9d65e677e88e4b4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 21 Feb 2020 21:57:46 GMT
ADD file:7925c9b35ffa1870e7d336ddcdd6c3434715178c7d08ff2ce9796b651302c347 in / 
# Fri, 21 Feb 2020 21:57:50 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:57:51 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:57:53 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:57:53 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:35:53 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 21 Feb 2020 22:36:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:36:07 GMT
ENV GOSU_VERSION=1.11
# Fri, 21 Feb 2020 22:36:08 GMT
ENV JSYAML_VERSION=3.13.0
# Fri, 21 Feb 2020 22:36:32 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 21 Feb 2020 22:36:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:36:35 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 21 Feb 2020 22:36:37 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:36:38 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 21 Feb 2020 22:36:38 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:36:39 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:36:40 GMT
ENV MONGO_MAJOR=4.2
# Fri, 21 Feb 2020 22:36:40 GMT
ENV MONGO_VERSION=4.2.3
# Fri, 21 Feb 2020 22:36:42 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 21 Feb 2020 22:37:22 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 21 Feb 2020 22:37:34 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 21 Feb 2020 22:37:35 GMT
VOLUME [/data/db /data/configdb]
# Fri, 21 Feb 2020 22:37:35 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:37:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:37:36 GMT
EXPOSE 27017
# Fri, 21 Feb 2020 22:37:37 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:b84fcb37dc33cf7416e0f1cf1219e16a15ab0d1c3aa4638d362f19c2679451de`  
		Last Modified: Fri, 21 Feb 2020 21:59:09 GMT  
		Size: 25.4 MB (25365672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9594931f903b7b3c4f5cb63196d29d715c50b567c128a5572131c12a25f04139`  
		Last Modified: Fri, 21 Feb 2020 21:59:06 GMT  
		Size: 36.2 KB (36186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66af13675c2330803d61d2198bb4f69c36bb7eed2d2b2bc3660fed8e873dce59`  
		Last Modified: Fri, 21 Feb 2020 21:59:11 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae0fb7b2ee5c5bc387374bdd08f53541bdfcf678d9b9f83489c3923af65fed0`  
		Last Modified: Fri, 21 Feb 2020 21:59:21 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20167b6352cf148caf092b98ebcd5a57b9008a2bc70e24c6a1aa4b6d54597e4`  
		Last Modified: Fri, 21 Feb 2020 22:38:04 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2c5aee18e04f08b2d2246738dd9239c3fc17fbc5629693a785574101ac5259`  
		Last Modified: Fri, 21 Feb 2020 22:38:03 GMT  
		Size: 2.7 MB (2714796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:679a24e64e261a1b368092a0ac88f8c4caf2a56ddbeb080a0b8d40e8892e07d5`  
		Last Modified: Fri, 21 Feb 2020 22:38:02 GMT  
		Size: 5.7 MB (5686031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a3aec4f6061abbba88c3ade7fef1e34e6fd70dbe30c3a9b5f0fbc64d2958e8`  
		Last Modified: Fri, 21 Feb 2020 22:38:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd8c5c1c54681c13c0b8c3a2bc57867973e945d847f5d9eadddbe4368c77540`  
		Last Modified: Fri, 21 Feb 2020 22:37:59 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f7fb2198b888d79b72c745d2130adc19213398ae3fac9631e98c6a8f6f128f`  
		Last Modified: Fri, 21 Feb 2020 22:37:59 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f630485b2c56c8706faa0a45bb123c968dc150a878e45eba0014ce3ca4d235`  
		Last Modified: Fri, 21 Feb 2020 22:38:19 GMT  
		Size: 126.1 MB (126136898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64555c5c853ffac8525a186c8038b7e67d4fbcc02d07f8e129e6ae70e5ca668f`  
		Last Modified: Fri, 21 Feb 2020 22:38:05 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d128c4bb10ec54ee27fce624769033a0191750dbc6b46a63a576aed005f086f`  
		Last Modified: Fri, 21 Feb 2020 22:38:04 GMT  
		Size: 4.0 KB (3952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2` - windows version 10.0.14393.3506; amd64

```console
$ docker pull mongo@sha256:ffcd7945296fd6bf2d492a8fbd2d76b87b4d700b617a3dbc3113ad3609dc1e99
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5823379228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b1841c6da45b9f09da659b319ee3ec76161c255d3a0299c744e58541cf1d5f`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 05:12:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 20 Feb 2020 05:31:28 GMT
ENV MONGO_VERSION=4.2.3
# Wed, 11 Mar 2020 22:59:46 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.3-signed.msi
# Wed, 11 Mar 2020 22:59:47 GMT
ENV MONGO_DOWNLOAD_SHA256=234f6abf9c4947df94428f6ce648905dbf6b1269f48cc3239ebd4990bde1ca2a
# Wed, 11 Mar 2020 23:17:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Mar 2020 23:17:16 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Mar 2020 23:17:18 GMT
EXPOSE 27017
# Wed, 11 Mar 2020 23:17:19 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:846a2223e9e7a88a2a07d706553f144d380483d72fb9f0697c4fcd71773a8693`  
		Size: 1.7 GB (1657079102 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0961c48658cd7865bcf6c05285dfbe8ad89cd52059088d7f4eed6fde1bb2b385`  
		Last Modified: Thu, 20 Feb 2020 05:18:25 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53763da721aa3ae58cd704805589abe169e1d3d28218280db0ed4045881d52cc`  
		Last Modified: Thu, 20 Feb 2020 05:44:18 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28575cbb1dce05be3e8ec069dac86a4ae8b751008d4f0c9654ea8a5adb6a05d`  
		Last Modified: Wed, 11 Mar 2020 23:40:27 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b0fd752a2977b6c56e9008cdf13c5221932c0fa7d04c8b82af7b1e365d7dcb`  
		Last Modified: Wed, 11 Mar 2020 23:40:24 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a599774a11cf582afd1c631f47ee898b2d7b7bd6c85e6a169f55999aebaf3f`  
		Last Modified: Wed, 11 Mar 2020 23:40:50 GMT  
		Size: 96.3 MB (96305864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158acd728c1a7f81dc5ab0e6ab015b47dbfe43d906b6935e6b3fb5af9ac717c9`  
		Last Modified: Wed, 11 Mar 2020 23:40:25 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1207ac339b253e1f2d5d984071f0cd6b1c14321de6258b95f05756828577ef`  
		Last Modified: Wed, 11 Mar 2020 23:40:24 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7bafe8e7fe89107a1cc111971c17ff5bfed4f23c13b7e8351d50dfedc51894`  
		Last Modified: Wed, 11 Mar 2020 23:40:24 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2` - windows version 10.0.17763.1098; amd64

```console
$ docker pull mongo@sha256:aac754de81af2f5d162c77a945382332cffd5575897c7601ef472343cb844896
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2720597037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d0aaebe9da6481c2ac37ceef6336551122a88bb8c6e0f0273b2b1408c89f3a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Tue, 10 Mar 2020 23:23:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Mar 2020 23:17:35 GMT
ENV MONGO_VERSION=4.2.3
# Wed, 11 Mar 2020 23:17:36 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.3-signed.msi
# Wed, 11 Mar 2020 23:17:37 GMT
ENV MONGO_DOWNLOAD_SHA256=234f6abf9c4947df94428f6ce648905dbf6b1269f48cc3239ebd4990bde1ca2a
# Wed, 11 Mar 2020 23:37:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Mar 2020 23:37:05 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Mar 2020 23:37:08 GMT
EXPOSE 27017
# Wed, 11 Mar 2020 23:37:09 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb49f89affc2d69b541463d095fdfbe61fa62e02b0aa5fa6d26bc134fb66bf35`  
		Last Modified: Wed, 11 Mar 2020 00:30:48 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a556cdd1dac3043338300637cf3645822f875ee02355952ab1cd7751e1b68bc`  
		Last Modified: Wed, 11 Mar 2020 23:41:10 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcc51a0e27cfe040ead7b64a7c6a800c4c738b534689744bc5736c486935beb`  
		Last Modified: Wed, 11 Mar 2020 23:41:10 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f7203b7c8fc0a4e01010792bc0a916bb1d80725bd8a4e8f11428ee3160d35f`  
		Last Modified: Wed, 11 Mar 2020 23:41:07 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22af9a292df27880e2bdab8b6325e55b0ca496959f7b3cbc864addc1d08d102d`  
		Last Modified: Wed, 11 Mar 2020 23:42:15 GMT  
		Size: 455.3 MB (455252292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb17de172b016b72e14b1ad1dc7b0d91f65115cd25a7268d5758b93956a3298f`  
		Last Modified: Wed, 11 Mar 2020 23:41:07 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a4339164f7d75bf46ec45b216b30960178423acd470a8d3f7fa23bcadb1e05`  
		Last Modified: Wed, 11 Mar 2020 23:41:07 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf29d93e6248494f3397e2328ebfe14d053d0679135d2853daa7460ecf197df7`  
		Last Modified: Wed, 11 Mar 2020 23:41:08 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.2.3`

```console
$ docker pull mongo@sha256:a1f116a08f48359302d7b567bdccc8b047bb0e534044de91be908c39eb796707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x
	-	windows version 10.0.14393.3506; amd64
	-	windows version 10.0.17763.1098; amd64

### `mongo:4.2.3` - linux; amd64

```console
$ docker pull mongo@sha256:c6e1710fc73d5a878ebc8b98c28d8897d5a4bbbb0e5d7ad758264d913e21ee71
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (163996273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcef5fd2979dbcbf76e46139680bf71c35925e344afa4703de43bdc44c6c526a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 21 Feb 2020 22:20:39 GMT
ADD file:91a750fb184711fde03c9172f41e8a907ccbb1bfb904c2c3f4ef595fcddbc3a9 in / 
# Fri, 21 Feb 2020 22:20:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:20:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:20:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:20:44 GMT
CMD ["/bin/bash"]
# Sat, 22 Feb 2020 01:09:51 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Sat, 22 Feb 2020 01:10:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 01:10:01 GMT
ENV GOSU_VERSION=1.11
# Sat, 22 Feb 2020 01:10:01 GMT
ENV JSYAML_VERSION=3.13.0
# Sat, 22 Feb 2020 01:10:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 22 Feb 2020 01:10:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 22 Feb 2020 01:10:19 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Sat, 22 Feb 2020 01:10:20 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Sat, 22 Feb 2020 01:10:20 GMT
ARG MONGO_PACKAGE=mongodb-org
# Sat, 22 Feb 2020 01:10:20 GMT
ARG MONGO_REPO=repo.mongodb.org
# Sat, 22 Feb 2020 01:10:20 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Sat, 22 Feb 2020 01:10:21 GMT
ENV MONGO_MAJOR=4.2
# Sat, 22 Feb 2020 01:10:21 GMT
ENV MONGO_VERSION=4.2.3
# Sat, 22 Feb 2020 01:10:21 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Sat, 22 Feb 2020 01:10:39 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Sat, 22 Feb 2020 01:10:40 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Sat, 22 Feb 2020 01:10:40 GMT
VOLUME [/data/db /data/configdb]
# Sat, 22 Feb 2020 01:10:40 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Sat, 22 Feb 2020 01:10:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 22 Feb 2020 01:10:41 GMT
EXPOSE 27017
# Sat, 22 Feb 2020 01:10:41 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:423ae2b273f4c17ceee9e8482fa8d071d90c7d052ae208e1fe4963fceb3d6954`  
		Last Modified: Wed, 19 Feb 2020 13:21:21 GMT  
		Size: 26.7 MB (26692096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de83a2304fa1f7c4a13708a0d15b9704f5945c2be5cbb2b3ed9b2ccb718d0b3d`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a83bce3af0648efaa60b9bb28225b09136d2d35d0bed25ac764297076dec1b`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b53be908de2c0c78070fff0a9f04835211b3156c4e73785747af365e71a0d7`  
		Last Modified: Fri, 21 Feb 2020 22:22:50 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cc2fb4f0eb1b8b82496ad1e17ec728355d84d889f8fd43ac357de9c6daaae6`  
		Last Modified: Sat, 22 Feb 2020 01:11:46 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f552d845039c0b94c06de56dc454b604142c32a69268bbc374a05470cc888431`  
		Last Modified: Sat, 22 Feb 2020 01:11:47 GMT  
		Size: 3.0 MB (2982680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6e166a9814b17b9c5dc683a8a35855eea3d9a898f77c0ee310f2038f29fce6`  
		Last Modified: Sat, 22 Feb 2020 01:11:47 GMT  
		Size: 5.8 MB (5764092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2ba5bee263bb3922f6c6a693b088d8d4753d4d90c05edd7534c2d80fc66358`  
		Last Modified: Sat, 22 Feb 2020 01:11:46 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828a1244f9760b1f6ff171f61f81c4fb01be2128e86e070c53e5b90658c40c8f`  
		Last Modified: Sat, 22 Feb 2020 01:11:45 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63a86989a84986d2b7e0e4ba20e65cdf25b2785771363571320bcd39f1d3494`  
		Last Modified: Sat, 22 Feb 2020 01:11:45 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc2ee27e8bbd1744066620810df67cf8b783b2b658f3edc0c852d75bfae74ca`  
		Last Modified: Sat, 22 Feb 2020 01:12:03 GMT  
		Size: 128.5 MB (128513279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a06e64657c7706873ecc5363ca322af486258b0e2a7c26fab7f46343ba622e`  
		Last Modified: Sat, 22 Feb 2020 01:11:45 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca7a59243040eff21e5c6d08a9e1b6b3be459f869ac615b51ec2a4949948128`  
		Last Modified: Sat, 22 Feb 2020 01:11:45 GMT  
		Size: 4.0 KB (3954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2.3` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:d06ed06348a9b1815c5bc265d58f3706762f8a10fd9d7b4f1b9b7bb83f1673c9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (154023756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91cd6dddcfbe299cfe0222a6a9bc21d01f7b4561a6cb63efce4975d09b957c26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 21 Feb 2020 21:54:16 GMT
ADD file:d827a0b8f08011678a718254c1220408c7e6c7ab03ae4259b415542309f18578 in / 
# Fri, 21 Feb 2020 21:54:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:54:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:54:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:54:25 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:50:43 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 21 Feb 2020 22:51:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:51:02 GMT
ENV GOSU_VERSION=1.11
# Fri, 21 Feb 2020 22:51:03 GMT
ENV JSYAML_VERSION=3.13.0
# Fri, 21 Feb 2020 22:51:30 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 21 Feb 2020 22:51:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:51:33 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 21 Feb 2020 22:51:35 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:51:35 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 21 Feb 2020 22:51:37 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:51:37 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:51:38 GMT
ENV MONGO_MAJOR=4.2
# Fri, 21 Feb 2020 22:51:39 GMT
ENV MONGO_VERSION=4.2.3
# Fri, 21 Feb 2020 22:51:41 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 21 Feb 2020 22:52:11 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 21 Feb 2020 22:52:13 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 21 Feb 2020 22:52:14 GMT
VOLUME [/data/db /data/configdb]
# Fri, 21 Feb 2020 22:52:14 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:52:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:52:16 GMT
EXPOSE 27017
# Fri, 21 Feb 2020 22:52:16 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:6695dc10aaa5cd71c433dfb366e84804eb5fbee91eab1e113442040d6ef4c9e0`  
		Last Modified: Fri, 21 Feb 2020 21:56:13 GMT  
		Size: 23.7 MB (23721143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72aab8f928deff72c9b5867c93524a60e3f8cf1b7401c88b0ede8dc3c595e828`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e83b6447acdea2afff1a10052ebc551d15bfd1d2a93a202699f7a458c612c07`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6a91485a919c412d218b6441c339f691079ff88e6d28734b1cc3d5938cf58d`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce30eb24f9ee36f81283e24d44464d289f8925925dd29948021da9875c68ada`  
		Last Modified: Fri, 21 Feb 2020 22:53:51 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40c1d7ad1d1ea72814e10a3a2a7a82e998ae6f374122d24456bbda9bf38e068`  
		Last Modified: Fri, 21 Feb 2020 22:53:51 GMT  
		Size: 2.7 MB (2676051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c7fbc92b61b056c0d3a8e0b548ffe9f5d488c6ea126c0a27d97efbb4f4befad`  
		Last Modified: Fri, 21 Feb 2020 22:53:51 GMT  
		Size: 5.3 MB (5283262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31687588808d10bf423bf6473235a0ba3c81ee24391fcb307a550ef4f12161e`  
		Last Modified: Fri, 21 Feb 2020 22:53:50 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd05cdedee7f57674a001111e63e8d59a002bf511c3878b74313795359de0d7`  
		Last Modified: Fri, 21 Feb 2020 22:53:47 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af7b837ad38bf29cafd860d9a45a0ac68d398991d2c18660806e4d9bd570ba2e`  
		Last Modified: Fri, 21 Feb 2020 22:53:48 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1886e577ef072dc81cbc19ec5cb5da2cd43a40a0b8bfd5cc1f649630a8e350c`  
		Last Modified: Fri, 21 Feb 2020 22:54:13 GMT  
		Size: 122.3 MB (122299237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c2758fd66f09bc1675a0459df7ac7f51a7226772ca6f84430622c6f74fe6cb`  
		Last Modified: Fri, 21 Feb 2020 22:53:47 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf80da1fa0a60da920fc9b9f3f655290968ebb2335db548ad307c952fd6d933`  
		Last Modified: Fri, 21 Feb 2020 22:53:48 GMT  
		Size: 4.0 KB (3952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2.3` - linux; s390x

```console
$ docker pull mongo@sha256:f680daf0de2259244447be2895d266431defeebea01fba22433c12ffec9bdb01
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.9 MB (159948448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1d6d571c4e0118b833c5aad42620aa5ec5f67c8d3f1f4f9d65e677e88e4b4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 21 Feb 2020 21:57:46 GMT
ADD file:7925c9b35ffa1870e7d336ddcdd6c3434715178c7d08ff2ce9796b651302c347 in / 
# Fri, 21 Feb 2020 21:57:50 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:57:51 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:57:53 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:57:53 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:35:53 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 21 Feb 2020 22:36:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:36:07 GMT
ENV GOSU_VERSION=1.11
# Fri, 21 Feb 2020 22:36:08 GMT
ENV JSYAML_VERSION=3.13.0
# Fri, 21 Feb 2020 22:36:32 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 21 Feb 2020 22:36:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:36:35 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 21 Feb 2020 22:36:37 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:36:38 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 21 Feb 2020 22:36:38 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:36:39 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:36:40 GMT
ENV MONGO_MAJOR=4.2
# Fri, 21 Feb 2020 22:36:40 GMT
ENV MONGO_VERSION=4.2.3
# Fri, 21 Feb 2020 22:36:42 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 21 Feb 2020 22:37:22 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 21 Feb 2020 22:37:34 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 21 Feb 2020 22:37:35 GMT
VOLUME [/data/db /data/configdb]
# Fri, 21 Feb 2020 22:37:35 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:37:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:37:36 GMT
EXPOSE 27017
# Fri, 21 Feb 2020 22:37:37 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:b84fcb37dc33cf7416e0f1cf1219e16a15ab0d1c3aa4638d362f19c2679451de`  
		Last Modified: Fri, 21 Feb 2020 21:59:09 GMT  
		Size: 25.4 MB (25365672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9594931f903b7b3c4f5cb63196d29d715c50b567c128a5572131c12a25f04139`  
		Last Modified: Fri, 21 Feb 2020 21:59:06 GMT  
		Size: 36.2 KB (36186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66af13675c2330803d61d2198bb4f69c36bb7eed2d2b2bc3660fed8e873dce59`  
		Last Modified: Fri, 21 Feb 2020 21:59:11 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae0fb7b2ee5c5bc387374bdd08f53541bdfcf678d9b9f83489c3923af65fed0`  
		Last Modified: Fri, 21 Feb 2020 21:59:21 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20167b6352cf148caf092b98ebcd5a57b9008a2bc70e24c6a1aa4b6d54597e4`  
		Last Modified: Fri, 21 Feb 2020 22:38:04 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2c5aee18e04f08b2d2246738dd9239c3fc17fbc5629693a785574101ac5259`  
		Last Modified: Fri, 21 Feb 2020 22:38:03 GMT  
		Size: 2.7 MB (2714796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:679a24e64e261a1b368092a0ac88f8c4caf2a56ddbeb080a0b8d40e8892e07d5`  
		Last Modified: Fri, 21 Feb 2020 22:38:02 GMT  
		Size: 5.7 MB (5686031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a3aec4f6061abbba88c3ade7fef1e34e6fd70dbe30c3a9b5f0fbc64d2958e8`  
		Last Modified: Fri, 21 Feb 2020 22:38:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd8c5c1c54681c13c0b8c3a2bc57867973e945d847f5d9eadddbe4368c77540`  
		Last Modified: Fri, 21 Feb 2020 22:37:59 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f7fb2198b888d79b72c745d2130adc19213398ae3fac9631e98c6a8f6f128f`  
		Last Modified: Fri, 21 Feb 2020 22:37:59 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f630485b2c56c8706faa0a45bb123c968dc150a878e45eba0014ce3ca4d235`  
		Last Modified: Fri, 21 Feb 2020 22:38:19 GMT  
		Size: 126.1 MB (126136898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64555c5c853ffac8525a186c8038b7e67d4fbcc02d07f8e129e6ae70e5ca668f`  
		Last Modified: Fri, 21 Feb 2020 22:38:05 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d128c4bb10ec54ee27fce624769033a0191750dbc6b46a63a576aed005f086f`  
		Last Modified: Fri, 21 Feb 2020 22:38:04 GMT  
		Size: 4.0 KB (3952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2.3` - windows version 10.0.14393.3506; amd64

```console
$ docker pull mongo@sha256:ffcd7945296fd6bf2d492a8fbd2d76b87b4d700b617a3dbc3113ad3609dc1e99
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5823379228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b1841c6da45b9f09da659b319ee3ec76161c255d3a0299c744e58541cf1d5f`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 05:12:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 20 Feb 2020 05:31:28 GMT
ENV MONGO_VERSION=4.2.3
# Wed, 11 Mar 2020 22:59:46 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.3-signed.msi
# Wed, 11 Mar 2020 22:59:47 GMT
ENV MONGO_DOWNLOAD_SHA256=234f6abf9c4947df94428f6ce648905dbf6b1269f48cc3239ebd4990bde1ca2a
# Wed, 11 Mar 2020 23:17:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Mar 2020 23:17:16 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Mar 2020 23:17:18 GMT
EXPOSE 27017
# Wed, 11 Mar 2020 23:17:19 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:846a2223e9e7a88a2a07d706553f144d380483d72fb9f0697c4fcd71773a8693`  
		Size: 1.7 GB (1657079102 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0961c48658cd7865bcf6c05285dfbe8ad89cd52059088d7f4eed6fde1bb2b385`  
		Last Modified: Thu, 20 Feb 2020 05:18:25 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53763da721aa3ae58cd704805589abe169e1d3d28218280db0ed4045881d52cc`  
		Last Modified: Thu, 20 Feb 2020 05:44:18 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28575cbb1dce05be3e8ec069dac86a4ae8b751008d4f0c9654ea8a5adb6a05d`  
		Last Modified: Wed, 11 Mar 2020 23:40:27 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b0fd752a2977b6c56e9008cdf13c5221932c0fa7d04c8b82af7b1e365d7dcb`  
		Last Modified: Wed, 11 Mar 2020 23:40:24 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a599774a11cf582afd1c631f47ee898b2d7b7bd6c85e6a169f55999aebaf3f`  
		Last Modified: Wed, 11 Mar 2020 23:40:50 GMT  
		Size: 96.3 MB (96305864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158acd728c1a7f81dc5ab0e6ab015b47dbfe43d906b6935e6b3fb5af9ac717c9`  
		Last Modified: Wed, 11 Mar 2020 23:40:25 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1207ac339b253e1f2d5d984071f0cd6b1c14321de6258b95f05756828577ef`  
		Last Modified: Wed, 11 Mar 2020 23:40:24 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7bafe8e7fe89107a1cc111971c17ff5bfed4f23c13b7e8351d50dfedc51894`  
		Last Modified: Wed, 11 Mar 2020 23:40:24 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2.3` - windows version 10.0.17763.1098; amd64

```console
$ docker pull mongo@sha256:aac754de81af2f5d162c77a945382332cffd5575897c7601ef472343cb844896
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2720597037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d0aaebe9da6481c2ac37ceef6336551122a88bb8c6e0f0273b2b1408c89f3a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Tue, 10 Mar 2020 23:23:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Mar 2020 23:17:35 GMT
ENV MONGO_VERSION=4.2.3
# Wed, 11 Mar 2020 23:17:36 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.3-signed.msi
# Wed, 11 Mar 2020 23:17:37 GMT
ENV MONGO_DOWNLOAD_SHA256=234f6abf9c4947df94428f6ce648905dbf6b1269f48cc3239ebd4990bde1ca2a
# Wed, 11 Mar 2020 23:37:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Mar 2020 23:37:05 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Mar 2020 23:37:08 GMT
EXPOSE 27017
# Wed, 11 Mar 2020 23:37:09 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb49f89affc2d69b541463d095fdfbe61fa62e02b0aa5fa6d26bc134fb66bf35`  
		Last Modified: Wed, 11 Mar 2020 00:30:48 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a556cdd1dac3043338300637cf3645822f875ee02355952ab1cd7751e1b68bc`  
		Last Modified: Wed, 11 Mar 2020 23:41:10 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcc51a0e27cfe040ead7b64a7c6a800c4c738b534689744bc5736c486935beb`  
		Last Modified: Wed, 11 Mar 2020 23:41:10 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f7203b7c8fc0a4e01010792bc0a916bb1d80725bd8a4e8f11428ee3160d35f`  
		Last Modified: Wed, 11 Mar 2020 23:41:07 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22af9a292df27880e2bdab8b6325e55b0ca496959f7b3cbc864addc1d08d102d`  
		Last Modified: Wed, 11 Mar 2020 23:42:15 GMT  
		Size: 455.3 MB (455252292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb17de172b016b72e14b1ad1dc7b0d91f65115cd25a7268d5758b93956a3298f`  
		Last Modified: Wed, 11 Mar 2020 23:41:07 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a4339164f7d75bf46ec45b216b30960178423acd470a8d3f7fa23bcadb1e05`  
		Last Modified: Wed, 11 Mar 2020 23:41:07 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf29d93e6248494f3397e2328ebfe14d053d0679135d2853daa7460ecf197df7`  
		Last Modified: Wed, 11 Mar 2020 23:41:08 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.2.3-bionic`

```console
$ docker pull mongo@sha256:e74f06447431bb0afe8ab0e260e22c664e5714a301b9ac2d92805f0da2a83be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `mongo:4.2.3-bionic` - linux; amd64

```console
$ docker pull mongo@sha256:c6e1710fc73d5a878ebc8b98c28d8897d5a4bbbb0e5d7ad758264d913e21ee71
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (163996273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcef5fd2979dbcbf76e46139680bf71c35925e344afa4703de43bdc44c6c526a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 21 Feb 2020 22:20:39 GMT
ADD file:91a750fb184711fde03c9172f41e8a907ccbb1bfb904c2c3f4ef595fcddbc3a9 in / 
# Fri, 21 Feb 2020 22:20:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:20:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:20:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:20:44 GMT
CMD ["/bin/bash"]
# Sat, 22 Feb 2020 01:09:51 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Sat, 22 Feb 2020 01:10:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 01:10:01 GMT
ENV GOSU_VERSION=1.11
# Sat, 22 Feb 2020 01:10:01 GMT
ENV JSYAML_VERSION=3.13.0
# Sat, 22 Feb 2020 01:10:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 22 Feb 2020 01:10:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 22 Feb 2020 01:10:19 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Sat, 22 Feb 2020 01:10:20 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Sat, 22 Feb 2020 01:10:20 GMT
ARG MONGO_PACKAGE=mongodb-org
# Sat, 22 Feb 2020 01:10:20 GMT
ARG MONGO_REPO=repo.mongodb.org
# Sat, 22 Feb 2020 01:10:20 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Sat, 22 Feb 2020 01:10:21 GMT
ENV MONGO_MAJOR=4.2
# Sat, 22 Feb 2020 01:10:21 GMT
ENV MONGO_VERSION=4.2.3
# Sat, 22 Feb 2020 01:10:21 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Sat, 22 Feb 2020 01:10:39 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Sat, 22 Feb 2020 01:10:40 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Sat, 22 Feb 2020 01:10:40 GMT
VOLUME [/data/db /data/configdb]
# Sat, 22 Feb 2020 01:10:40 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Sat, 22 Feb 2020 01:10:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 22 Feb 2020 01:10:41 GMT
EXPOSE 27017
# Sat, 22 Feb 2020 01:10:41 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:423ae2b273f4c17ceee9e8482fa8d071d90c7d052ae208e1fe4963fceb3d6954`  
		Last Modified: Wed, 19 Feb 2020 13:21:21 GMT  
		Size: 26.7 MB (26692096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de83a2304fa1f7c4a13708a0d15b9704f5945c2be5cbb2b3ed9b2ccb718d0b3d`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a83bce3af0648efaa60b9bb28225b09136d2d35d0bed25ac764297076dec1b`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b53be908de2c0c78070fff0a9f04835211b3156c4e73785747af365e71a0d7`  
		Last Modified: Fri, 21 Feb 2020 22:22:50 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cc2fb4f0eb1b8b82496ad1e17ec728355d84d889f8fd43ac357de9c6daaae6`  
		Last Modified: Sat, 22 Feb 2020 01:11:46 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f552d845039c0b94c06de56dc454b604142c32a69268bbc374a05470cc888431`  
		Last Modified: Sat, 22 Feb 2020 01:11:47 GMT  
		Size: 3.0 MB (2982680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6e166a9814b17b9c5dc683a8a35855eea3d9a898f77c0ee310f2038f29fce6`  
		Last Modified: Sat, 22 Feb 2020 01:11:47 GMT  
		Size: 5.8 MB (5764092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2ba5bee263bb3922f6c6a693b088d8d4753d4d90c05edd7534c2d80fc66358`  
		Last Modified: Sat, 22 Feb 2020 01:11:46 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828a1244f9760b1f6ff171f61f81c4fb01be2128e86e070c53e5b90658c40c8f`  
		Last Modified: Sat, 22 Feb 2020 01:11:45 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63a86989a84986d2b7e0e4ba20e65cdf25b2785771363571320bcd39f1d3494`  
		Last Modified: Sat, 22 Feb 2020 01:11:45 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc2ee27e8bbd1744066620810df67cf8b783b2b658f3edc0c852d75bfae74ca`  
		Last Modified: Sat, 22 Feb 2020 01:12:03 GMT  
		Size: 128.5 MB (128513279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a06e64657c7706873ecc5363ca322af486258b0e2a7c26fab7f46343ba622e`  
		Last Modified: Sat, 22 Feb 2020 01:11:45 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca7a59243040eff21e5c6d08a9e1b6b3be459f869ac615b51ec2a4949948128`  
		Last Modified: Sat, 22 Feb 2020 01:11:45 GMT  
		Size: 4.0 KB (3954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2.3-bionic` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:d06ed06348a9b1815c5bc265d58f3706762f8a10fd9d7b4f1b9b7bb83f1673c9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (154023756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91cd6dddcfbe299cfe0222a6a9bc21d01f7b4561a6cb63efce4975d09b957c26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 21 Feb 2020 21:54:16 GMT
ADD file:d827a0b8f08011678a718254c1220408c7e6c7ab03ae4259b415542309f18578 in / 
# Fri, 21 Feb 2020 21:54:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:54:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:54:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:54:25 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:50:43 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 21 Feb 2020 22:51:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:51:02 GMT
ENV GOSU_VERSION=1.11
# Fri, 21 Feb 2020 22:51:03 GMT
ENV JSYAML_VERSION=3.13.0
# Fri, 21 Feb 2020 22:51:30 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 21 Feb 2020 22:51:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:51:33 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 21 Feb 2020 22:51:35 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:51:35 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 21 Feb 2020 22:51:37 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:51:37 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:51:38 GMT
ENV MONGO_MAJOR=4.2
# Fri, 21 Feb 2020 22:51:39 GMT
ENV MONGO_VERSION=4.2.3
# Fri, 21 Feb 2020 22:51:41 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 21 Feb 2020 22:52:11 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 21 Feb 2020 22:52:13 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 21 Feb 2020 22:52:14 GMT
VOLUME [/data/db /data/configdb]
# Fri, 21 Feb 2020 22:52:14 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:52:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:52:16 GMT
EXPOSE 27017
# Fri, 21 Feb 2020 22:52:16 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:6695dc10aaa5cd71c433dfb366e84804eb5fbee91eab1e113442040d6ef4c9e0`  
		Last Modified: Fri, 21 Feb 2020 21:56:13 GMT  
		Size: 23.7 MB (23721143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72aab8f928deff72c9b5867c93524a60e3f8cf1b7401c88b0ede8dc3c595e828`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e83b6447acdea2afff1a10052ebc551d15bfd1d2a93a202699f7a458c612c07`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6a91485a919c412d218b6441c339f691079ff88e6d28734b1cc3d5938cf58d`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce30eb24f9ee36f81283e24d44464d289f8925925dd29948021da9875c68ada`  
		Last Modified: Fri, 21 Feb 2020 22:53:51 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40c1d7ad1d1ea72814e10a3a2a7a82e998ae6f374122d24456bbda9bf38e068`  
		Last Modified: Fri, 21 Feb 2020 22:53:51 GMT  
		Size: 2.7 MB (2676051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c7fbc92b61b056c0d3a8e0b548ffe9f5d488c6ea126c0a27d97efbb4f4befad`  
		Last Modified: Fri, 21 Feb 2020 22:53:51 GMT  
		Size: 5.3 MB (5283262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31687588808d10bf423bf6473235a0ba3c81ee24391fcb307a550ef4f12161e`  
		Last Modified: Fri, 21 Feb 2020 22:53:50 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd05cdedee7f57674a001111e63e8d59a002bf511c3878b74313795359de0d7`  
		Last Modified: Fri, 21 Feb 2020 22:53:47 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af7b837ad38bf29cafd860d9a45a0ac68d398991d2c18660806e4d9bd570ba2e`  
		Last Modified: Fri, 21 Feb 2020 22:53:48 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1886e577ef072dc81cbc19ec5cb5da2cd43a40a0b8bfd5cc1f649630a8e350c`  
		Last Modified: Fri, 21 Feb 2020 22:54:13 GMT  
		Size: 122.3 MB (122299237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c2758fd66f09bc1675a0459df7ac7f51a7226772ca6f84430622c6f74fe6cb`  
		Last Modified: Fri, 21 Feb 2020 22:53:47 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf80da1fa0a60da920fc9b9f3f655290968ebb2335db548ad307c952fd6d933`  
		Last Modified: Fri, 21 Feb 2020 22:53:48 GMT  
		Size: 4.0 KB (3952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2.3-bionic` - linux; s390x

```console
$ docker pull mongo@sha256:f680daf0de2259244447be2895d266431defeebea01fba22433c12ffec9bdb01
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.9 MB (159948448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1d6d571c4e0118b833c5aad42620aa5ec5f67c8d3f1f4f9d65e677e88e4b4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 21 Feb 2020 21:57:46 GMT
ADD file:7925c9b35ffa1870e7d336ddcdd6c3434715178c7d08ff2ce9796b651302c347 in / 
# Fri, 21 Feb 2020 21:57:50 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:57:51 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:57:53 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:57:53 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:35:53 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 21 Feb 2020 22:36:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:36:07 GMT
ENV GOSU_VERSION=1.11
# Fri, 21 Feb 2020 22:36:08 GMT
ENV JSYAML_VERSION=3.13.0
# Fri, 21 Feb 2020 22:36:32 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 21 Feb 2020 22:36:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:36:35 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 21 Feb 2020 22:36:37 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:36:38 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 21 Feb 2020 22:36:38 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:36:39 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:36:40 GMT
ENV MONGO_MAJOR=4.2
# Fri, 21 Feb 2020 22:36:40 GMT
ENV MONGO_VERSION=4.2.3
# Fri, 21 Feb 2020 22:36:42 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 21 Feb 2020 22:37:22 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 21 Feb 2020 22:37:34 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 21 Feb 2020 22:37:35 GMT
VOLUME [/data/db /data/configdb]
# Fri, 21 Feb 2020 22:37:35 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:37:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:37:36 GMT
EXPOSE 27017
# Fri, 21 Feb 2020 22:37:37 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:b84fcb37dc33cf7416e0f1cf1219e16a15ab0d1c3aa4638d362f19c2679451de`  
		Last Modified: Fri, 21 Feb 2020 21:59:09 GMT  
		Size: 25.4 MB (25365672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9594931f903b7b3c4f5cb63196d29d715c50b567c128a5572131c12a25f04139`  
		Last Modified: Fri, 21 Feb 2020 21:59:06 GMT  
		Size: 36.2 KB (36186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66af13675c2330803d61d2198bb4f69c36bb7eed2d2b2bc3660fed8e873dce59`  
		Last Modified: Fri, 21 Feb 2020 21:59:11 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae0fb7b2ee5c5bc387374bdd08f53541bdfcf678d9b9f83489c3923af65fed0`  
		Last Modified: Fri, 21 Feb 2020 21:59:21 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20167b6352cf148caf092b98ebcd5a57b9008a2bc70e24c6a1aa4b6d54597e4`  
		Last Modified: Fri, 21 Feb 2020 22:38:04 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2c5aee18e04f08b2d2246738dd9239c3fc17fbc5629693a785574101ac5259`  
		Last Modified: Fri, 21 Feb 2020 22:38:03 GMT  
		Size: 2.7 MB (2714796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:679a24e64e261a1b368092a0ac88f8c4caf2a56ddbeb080a0b8d40e8892e07d5`  
		Last Modified: Fri, 21 Feb 2020 22:38:02 GMT  
		Size: 5.7 MB (5686031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a3aec4f6061abbba88c3ade7fef1e34e6fd70dbe30c3a9b5f0fbc64d2958e8`  
		Last Modified: Fri, 21 Feb 2020 22:38:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd8c5c1c54681c13c0b8c3a2bc57867973e945d847f5d9eadddbe4368c77540`  
		Last Modified: Fri, 21 Feb 2020 22:37:59 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f7fb2198b888d79b72c745d2130adc19213398ae3fac9631e98c6a8f6f128f`  
		Last Modified: Fri, 21 Feb 2020 22:37:59 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f630485b2c56c8706faa0a45bb123c968dc150a878e45eba0014ce3ca4d235`  
		Last Modified: Fri, 21 Feb 2020 22:38:19 GMT  
		Size: 126.1 MB (126136898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64555c5c853ffac8525a186c8038b7e67d4fbcc02d07f8e129e6ae70e5ca668f`  
		Last Modified: Fri, 21 Feb 2020 22:38:05 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d128c4bb10ec54ee27fce624769033a0191750dbc6b46a63a576aed005f086f`  
		Last Modified: Fri, 21 Feb 2020 22:38:04 GMT  
		Size: 4.0 KB (3952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.2.3-windowsservercore`

```console
$ docker pull mongo@sha256:a6f3b2e274f112882de6bfb127033534f068a11fdbd123fb549104b79f50860f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3506; amd64
	-	windows version 10.0.17763.1098; amd64

### `mongo:4.2.3-windowsservercore` - windows version 10.0.14393.3506; amd64

```console
$ docker pull mongo@sha256:ffcd7945296fd6bf2d492a8fbd2d76b87b4d700b617a3dbc3113ad3609dc1e99
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5823379228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b1841c6da45b9f09da659b319ee3ec76161c255d3a0299c744e58541cf1d5f`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 05:12:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 20 Feb 2020 05:31:28 GMT
ENV MONGO_VERSION=4.2.3
# Wed, 11 Mar 2020 22:59:46 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.3-signed.msi
# Wed, 11 Mar 2020 22:59:47 GMT
ENV MONGO_DOWNLOAD_SHA256=234f6abf9c4947df94428f6ce648905dbf6b1269f48cc3239ebd4990bde1ca2a
# Wed, 11 Mar 2020 23:17:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Mar 2020 23:17:16 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Mar 2020 23:17:18 GMT
EXPOSE 27017
# Wed, 11 Mar 2020 23:17:19 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:846a2223e9e7a88a2a07d706553f144d380483d72fb9f0697c4fcd71773a8693`  
		Size: 1.7 GB (1657079102 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0961c48658cd7865bcf6c05285dfbe8ad89cd52059088d7f4eed6fde1bb2b385`  
		Last Modified: Thu, 20 Feb 2020 05:18:25 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53763da721aa3ae58cd704805589abe169e1d3d28218280db0ed4045881d52cc`  
		Last Modified: Thu, 20 Feb 2020 05:44:18 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28575cbb1dce05be3e8ec069dac86a4ae8b751008d4f0c9654ea8a5adb6a05d`  
		Last Modified: Wed, 11 Mar 2020 23:40:27 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b0fd752a2977b6c56e9008cdf13c5221932c0fa7d04c8b82af7b1e365d7dcb`  
		Last Modified: Wed, 11 Mar 2020 23:40:24 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a599774a11cf582afd1c631f47ee898b2d7b7bd6c85e6a169f55999aebaf3f`  
		Last Modified: Wed, 11 Mar 2020 23:40:50 GMT  
		Size: 96.3 MB (96305864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158acd728c1a7f81dc5ab0e6ab015b47dbfe43d906b6935e6b3fb5af9ac717c9`  
		Last Modified: Wed, 11 Mar 2020 23:40:25 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1207ac339b253e1f2d5d984071f0cd6b1c14321de6258b95f05756828577ef`  
		Last Modified: Wed, 11 Mar 2020 23:40:24 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7bafe8e7fe89107a1cc111971c17ff5bfed4f23c13b7e8351d50dfedc51894`  
		Last Modified: Wed, 11 Mar 2020 23:40:24 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2.3-windowsservercore` - windows version 10.0.17763.1098; amd64

```console
$ docker pull mongo@sha256:aac754de81af2f5d162c77a945382332cffd5575897c7601ef472343cb844896
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2720597037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d0aaebe9da6481c2ac37ceef6336551122a88bb8c6e0f0273b2b1408c89f3a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Tue, 10 Mar 2020 23:23:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Mar 2020 23:17:35 GMT
ENV MONGO_VERSION=4.2.3
# Wed, 11 Mar 2020 23:17:36 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.3-signed.msi
# Wed, 11 Mar 2020 23:17:37 GMT
ENV MONGO_DOWNLOAD_SHA256=234f6abf9c4947df94428f6ce648905dbf6b1269f48cc3239ebd4990bde1ca2a
# Wed, 11 Mar 2020 23:37:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Mar 2020 23:37:05 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Mar 2020 23:37:08 GMT
EXPOSE 27017
# Wed, 11 Mar 2020 23:37:09 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb49f89affc2d69b541463d095fdfbe61fa62e02b0aa5fa6d26bc134fb66bf35`  
		Last Modified: Wed, 11 Mar 2020 00:30:48 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a556cdd1dac3043338300637cf3645822f875ee02355952ab1cd7751e1b68bc`  
		Last Modified: Wed, 11 Mar 2020 23:41:10 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcc51a0e27cfe040ead7b64a7c6a800c4c738b534689744bc5736c486935beb`  
		Last Modified: Wed, 11 Mar 2020 23:41:10 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f7203b7c8fc0a4e01010792bc0a916bb1d80725bd8a4e8f11428ee3160d35f`  
		Last Modified: Wed, 11 Mar 2020 23:41:07 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22af9a292df27880e2bdab8b6325e55b0ca496959f7b3cbc864addc1d08d102d`  
		Last Modified: Wed, 11 Mar 2020 23:42:15 GMT  
		Size: 455.3 MB (455252292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb17de172b016b72e14b1ad1dc7b0d91f65115cd25a7268d5758b93956a3298f`  
		Last Modified: Wed, 11 Mar 2020 23:41:07 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a4339164f7d75bf46ec45b216b30960178423acd470a8d3f7fa23bcadb1e05`  
		Last Modified: Wed, 11 Mar 2020 23:41:07 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf29d93e6248494f3397e2328ebfe14d053d0679135d2853daa7460ecf197df7`  
		Last Modified: Wed, 11 Mar 2020 23:41:08 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.2.3-windowsservercore-1809`

```console
$ docker pull mongo@sha256:d934c0075f6a09fef6cba2d002d7f37e28f70e2007cacaa1bff067a56a097e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `mongo:4.2.3-windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull mongo@sha256:aac754de81af2f5d162c77a945382332cffd5575897c7601ef472343cb844896
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2720597037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d0aaebe9da6481c2ac37ceef6336551122a88bb8c6e0f0273b2b1408c89f3a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Tue, 10 Mar 2020 23:23:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Mar 2020 23:17:35 GMT
ENV MONGO_VERSION=4.2.3
# Wed, 11 Mar 2020 23:17:36 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.3-signed.msi
# Wed, 11 Mar 2020 23:17:37 GMT
ENV MONGO_DOWNLOAD_SHA256=234f6abf9c4947df94428f6ce648905dbf6b1269f48cc3239ebd4990bde1ca2a
# Wed, 11 Mar 2020 23:37:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Mar 2020 23:37:05 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Mar 2020 23:37:08 GMT
EXPOSE 27017
# Wed, 11 Mar 2020 23:37:09 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb49f89affc2d69b541463d095fdfbe61fa62e02b0aa5fa6d26bc134fb66bf35`  
		Last Modified: Wed, 11 Mar 2020 00:30:48 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a556cdd1dac3043338300637cf3645822f875ee02355952ab1cd7751e1b68bc`  
		Last Modified: Wed, 11 Mar 2020 23:41:10 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcc51a0e27cfe040ead7b64a7c6a800c4c738b534689744bc5736c486935beb`  
		Last Modified: Wed, 11 Mar 2020 23:41:10 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f7203b7c8fc0a4e01010792bc0a916bb1d80725bd8a4e8f11428ee3160d35f`  
		Last Modified: Wed, 11 Mar 2020 23:41:07 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22af9a292df27880e2bdab8b6325e55b0ca496959f7b3cbc864addc1d08d102d`  
		Last Modified: Wed, 11 Mar 2020 23:42:15 GMT  
		Size: 455.3 MB (455252292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb17de172b016b72e14b1ad1dc7b0d91f65115cd25a7268d5758b93956a3298f`  
		Last Modified: Wed, 11 Mar 2020 23:41:07 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a4339164f7d75bf46ec45b216b30960178423acd470a8d3f7fa23bcadb1e05`  
		Last Modified: Wed, 11 Mar 2020 23:41:07 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf29d93e6248494f3397e2328ebfe14d053d0679135d2853daa7460ecf197df7`  
		Last Modified: Wed, 11 Mar 2020 23:41:08 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.2.3-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:252d9092a44cb76ce1978defc409db903e14ffa2b022b7a58293c4583db38a47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3506; amd64

### `mongo:4.2.3-windowsservercore-ltsc2016` - windows version 10.0.14393.3506; amd64

```console
$ docker pull mongo@sha256:ffcd7945296fd6bf2d492a8fbd2d76b87b4d700b617a3dbc3113ad3609dc1e99
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5823379228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b1841c6da45b9f09da659b319ee3ec76161c255d3a0299c744e58541cf1d5f`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 05:12:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 20 Feb 2020 05:31:28 GMT
ENV MONGO_VERSION=4.2.3
# Wed, 11 Mar 2020 22:59:46 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.3-signed.msi
# Wed, 11 Mar 2020 22:59:47 GMT
ENV MONGO_DOWNLOAD_SHA256=234f6abf9c4947df94428f6ce648905dbf6b1269f48cc3239ebd4990bde1ca2a
# Wed, 11 Mar 2020 23:17:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Mar 2020 23:17:16 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Mar 2020 23:17:18 GMT
EXPOSE 27017
# Wed, 11 Mar 2020 23:17:19 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:846a2223e9e7a88a2a07d706553f144d380483d72fb9f0697c4fcd71773a8693`  
		Size: 1.7 GB (1657079102 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0961c48658cd7865bcf6c05285dfbe8ad89cd52059088d7f4eed6fde1bb2b385`  
		Last Modified: Thu, 20 Feb 2020 05:18:25 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53763da721aa3ae58cd704805589abe169e1d3d28218280db0ed4045881d52cc`  
		Last Modified: Thu, 20 Feb 2020 05:44:18 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28575cbb1dce05be3e8ec069dac86a4ae8b751008d4f0c9654ea8a5adb6a05d`  
		Last Modified: Wed, 11 Mar 2020 23:40:27 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b0fd752a2977b6c56e9008cdf13c5221932c0fa7d04c8b82af7b1e365d7dcb`  
		Last Modified: Wed, 11 Mar 2020 23:40:24 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a599774a11cf582afd1c631f47ee898b2d7b7bd6c85e6a169f55999aebaf3f`  
		Last Modified: Wed, 11 Mar 2020 23:40:50 GMT  
		Size: 96.3 MB (96305864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158acd728c1a7f81dc5ab0e6ab015b47dbfe43d906b6935e6b3fb5af9ac717c9`  
		Last Modified: Wed, 11 Mar 2020 23:40:25 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1207ac339b253e1f2d5d984071f0cd6b1c14321de6258b95f05756828577ef`  
		Last Modified: Wed, 11 Mar 2020 23:40:24 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7bafe8e7fe89107a1cc111971c17ff5bfed4f23c13b7e8351d50dfedc51894`  
		Last Modified: Wed, 11 Mar 2020 23:40:24 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.2-bionic`

```console
$ docker pull mongo@sha256:e74f06447431bb0afe8ab0e260e22c664e5714a301b9ac2d92805f0da2a83be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `mongo:4.2-bionic` - linux; amd64

```console
$ docker pull mongo@sha256:c6e1710fc73d5a878ebc8b98c28d8897d5a4bbbb0e5d7ad758264d913e21ee71
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (163996273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcef5fd2979dbcbf76e46139680bf71c35925e344afa4703de43bdc44c6c526a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 21 Feb 2020 22:20:39 GMT
ADD file:91a750fb184711fde03c9172f41e8a907ccbb1bfb904c2c3f4ef595fcddbc3a9 in / 
# Fri, 21 Feb 2020 22:20:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:20:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:20:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:20:44 GMT
CMD ["/bin/bash"]
# Sat, 22 Feb 2020 01:09:51 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Sat, 22 Feb 2020 01:10:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 01:10:01 GMT
ENV GOSU_VERSION=1.11
# Sat, 22 Feb 2020 01:10:01 GMT
ENV JSYAML_VERSION=3.13.0
# Sat, 22 Feb 2020 01:10:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 22 Feb 2020 01:10:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 22 Feb 2020 01:10:19 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Sat, 22 Feb 2020 01:10:20 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Sat, 22 Feb 2020 01:10:20 GMT
ARG MONGO_PACKAGE=mongodb-org
# Sat, 22 Feb 2020 01:10:20 GMT
ARG MONGO_REPO=repo.mongodb.org
# Sat, 22 Feb 2020 01:10:20 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Sat, 22 Feb 2020 01:10:21 GMT
ENV MONGO_MAJOR=4.2
# Sat, 22 Feb 2020 01:10:21 GMT
ENV MONGO_VERSION=4.2.3
# Sat, 22 Feb 2020 01:10:21 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Sat, 22 Feb 2020 01:10:39 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Sat, 22 Feb 2020 01:10:40 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Sat, 22 Feb 2020 01:10:40 GMT
VOLUME [/data/db /data/configdb]
# Sat, 22 Feb 2020 01:10:40 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Sat, 22 Feb 2020 01:10:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 22 Feb 2020 01:10:41 GMT
EXPOSE 27017
# Sat, 22 Feb 2020 01:10:41 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:423ae2b273f4c17ceee9e8482fa8d071d90c7d052ae208e1fe4963fceb3d6954`  
		Last Modified: Wed, 19 Feb 2020 13:21:21 GMT  
		Size: 26.7 MB (26692096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de83a2304fa1f7c4a13708a0d15b9704f5945c2be5cbb2b3ed9b2ccb718d0b3d`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a83bce3af0648efaa60b9bb28225b09136d2d35d0bed25ac764297076dec1b`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b53be908de2c0c78070fff0a9f04835211b3156c4e73785747af365e71a0d7`  
		Last Modified: Fri, 21 Feb 2020 22:22:50 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cc2fb4f0eb1b8b82496ad1e17ec728355d84d889f8fd43ac357de9c6daaae6`  
		Last Modified: Sat, 22 Feb 2020 01:11:46 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f552d845039c0b94c06de56dc454b604142c32a69268bbc374a05470cc888431`  
		Last Modified: Sat, 22 Feb 2020 01:11:47 GMT  
		Size: 3.0 MB (2982680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6e166a9814b17b9c5dc683a8a35855eea3d9a898f77c0ee310f2038f29fce6`  
		Last Modified: Sat, 22 Feb 2020 01:11:47 GMT  
		Size: 5.8 MB (5764092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2ba5bee263bb3922f6c6a693b088d8d4753d4d90c05edd7534c2d80fc66358`  
		Last Modified: Sat, 22 Feb 2020 01:11:46 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828a1244f9760b1f6ff171f61f81c4fb01be2128e86e070c53e5b90658c40c8f`  
		Last Modified: Sat, 22 Feb 2020 01:11:45 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63a86989a84986d2b7e0e4ba20e65cdf25b2785771363571320bcd39f1d3494`  
		Last Modified: Sat, 22 Feb 2020 01:11:45 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc2ee27e8bbd1744066620810df67cf8b783b2b658f3edc0c852d75bfae74ca`  
		Last Modified: Sat, 22 Feb 2020 01:12:03 GMT  
		Size: 128.5 MB (128513279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a06e64657c7706873ecc5363ca322af486258b0e2a7c26fab7f46343ba622e`  
		Last Modified: Sat, 22 Feb 2020 01:11:45 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca7a59243040eff21e5c6d08a9e1b6b3be459f869ac615b51ec2a4949948128`  
		Last Modified: Sat, 22 Feb 2020 01:11:45 GMT  
		Size: 4.0 KB (3954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2-bionic` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:d06ed06348a9b1815c5bc265d58f3706762f8a10fd9d7b4f1b9b7bb83f1673c9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (154023756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91cd6dddcfbe299cfe0222a6a9bc21d01f7b4561a6cb63efce4975d09b957c26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 21 Feb 2020 21:54:16 GMT
ADD file:d827a0b8f08011678a718254c1220408c7e6c7ab03ae4259b415542309f18578 in / 
# Fri, 21 Feb 2020 21:54:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:54:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:54:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:54:25 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:50:43 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 21 Feb 2020 22:51:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:51:02 GMT
ENV GOSU_VERSION=1.11
# Fri, 21 Feb 2020 22:51:03 GMT
ENV JSYAML_VERSION=3.13.0
# Fri, 21 Feb 2020 22:51:30 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 21 Feb 2020 22:51:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:51:33 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 21 Feb 2020 22:51:35 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:51:35 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 21 Feb 2020 22:51:37 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:51:37 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:51:38 GMT
ENV MONGO_MAJOR=4.2
# Fri, 21 Feb 2020 22:51:39 GMT
ENV MONGO_VERSION=4.2.3
# Fri, 21 Feb 2020 22:51:41 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 21 Feb 2020 22:52:11 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 21 Feb 2020 22:52:13 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 21 Feb 2020 22:52:14 GMT
VOLUME [/data/db /data/configdb]
# Fri, 21 Feb 2020 22:52:14 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:52:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:52:16 GMT
EXPOSE 27017
# Fri, 21 Feb 2020 22:52:16 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:6695dc10aaa5cd71c433dfb366e84804eb5fbee91eab1e113442040d6ef4c9e0`  
		Last Modified: Fri, 21 Feb 2020 21:56:13 GMT  
		Size: 23.7 MB (23721143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72aab8f928deff72c9b5867c93524a60e3f8cf1b7401c88b0ede8dc3c595e828`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e83b6447acdea2afff1a10052ebc551d15bfd1d2a93a202699f7a458c612c07`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6a91485a919c412d218b6441c339f691079ff88e6d28734b1cc3d5938cf58d`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce30eb24f9ee36f81283e24d44464d289f8925925dd29948021da9875c68ada`  
		Last Modified: Fri, 21 Feb 2020 22:53:51 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40c1d7ad1d1ea72814e10a3a2a7a82e998ae6f374122d24456bbda9bf38e068`  
		Last Modified: Fri, 21 Feb 2020 22:53:51 GMT  
		Size: 2.7 MB (2676051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c7fbc92b61b056c0d3a8e0b548ffe9f5d488c6ea126c0a27d97efbb4f4befad`  
		Last Modified: Fri, 21 Feb 2020 22:53:51 GMT  
		Size: 5.3 MB (5283262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31687588808d10bf423bf6473235a0ba3c81ee24391fcb307a550ef4f12161e`  
		Last Modified: Fri, 21 Feb 2020 22:53:50 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd05cdedee7f57674a001111e63e8d59a002bf511c3878b74313795359de0d7`  
		Last Modified: Fri, 21 Feb 2020 22:53:47 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af7b837ad38bf29cafd860d9a45a0ac68d398991d2c18660806e4d9bd570ba2e`  
		Last Modified: Fri, 21 Feb 2020 22:53:48 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1886e577ef072dc81cbc19ec5cb5da2cd43a40a0b8bfd5cc1f649630a8e350c`  
		Last Modified: Fri, 21 Feb 2020 22:54:13 GMT  
		Size: 122.3 MB (122299237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c2758fd66f09bc1675a0459df7ac7f51a7226772ca6f84430622c6f74fe6cb`  
		Last Modified: Fri, 21 Feb 2020 22:53:47 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf80da1fa0a60da920fc9b9f3f655290968ebb2335db548ad307c952fd6d933`  
		Last Modified: Fri, 21 Feb 2020 22:53:48 GMT  
		Size: 4.0 KB (3952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2-bionic` - linux; s390x

```console
$ docker pull mongo@sha256:f680daf0de2259244447be2895d266431defeebea01fba22433c12ffec9bdb01
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.9 MB (159948448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1d6d571c4e0118b833c5aad42620aa5ec5f67c8d3f1f4f9d65e677e88e4b4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 21 Feb 2020 21:57:46 GMT
ADD file:7925c9b35ffa1870e7d336ddcdd6c3434715178c7d08ff2ce9796b651302c347 in / 
# Fri, 21 Feb 2020 21:57:50 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:57:51 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:57:53 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:57:53 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:35:53 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 21 Feb 2020 22:36:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:36:07 GMT
ENV GOSU_VERSION=1.11
# Fri, 21 Feb 2020 22:36:08 GMT
ENV JSYAML_VERSION=3.13.0
# Fri, 21 Feb 2020 22:36:32 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 21 Feb 2020 22:36:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:36:35 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 21 Feb 2020 22:36:37 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:36:38 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 21 Feb 2020 22:36:38 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:36:39 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:36:40 GMT
ENV MONGO_MAJOR=4.2
# Fri, 21 Feb 2020 22:36:40 GMT
ENV MONGO_VERSION=4.2.3
# Fri, 21 Feb 2020 22:36:42 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 21 Feb 2020 22:37:22 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 21 Feb 2020 22:37:34 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 21 Feb 2020 22:37:35 GMT
VOLUME [/data/db /data/configdb]
# Fri, 21 Feb 2020 22:37:35 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:37:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:37:36 GMT
EXPOSE 27017
# Fri, 21 Feb 2020 22:37:37 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:b84fcb37dc33cf7416e0f1cf1219e16a15ab0d1c3aa4638d362f19c2679451de`  
		Last Modified: Fri, 21 Feb 2020 21:59:09 GMT  
		Size: 25.4 MB (25365672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9594931f903b7b3c4f5cb63196d29d715c50b567c128a5572131c12a25f04139`  
		Last Modified: Fri, 21 Feb 2020 21:59:06 GMT  
		Size: 36.2 KB (36186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66af13675c2330803d61d2198bb4f69c36bb7eed2d2b2bc3660fed8e873dce59`  
		Last Modified: Fri, 21 Feb 2020 21:59:11 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae0fb7b2ee5c5bc387374bdd08f53541bdfcf678d9b9f83489c3923af65fed0`  
		Last Modified: Fri, 21 Feb 2020 21:59:21 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20167b6352cf148caf092b98ebcd5a57b9008a2bc70e24c6a1aa4b6d54597e4`  
		Last Modified: Fri, 21 Feb 2020 22:38:04 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2c5aee18e04f08b2d2246738dd9239c3fc17fbc5629693a785574101ac5259`  
		Last Modified: Fri, 21 Feb 2020 22:38:03 GMT  
		Size: 2.7 MB (2714796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:679a24e64e261a1b368092a0ac88f8c4caf2a56ddbeb080a0b8d40e8892e07d5`  
		Last Modified: Fri, 21 Feb 2020 22:38:02 GMT  
		Size: 5.7 MB (5686031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a3aec4f6061abbba88c3ade7fef1e34e6fd70dbe30c3a9b5f0fbc64d2958e8`  
		Last Modified: Fri, 21 Feb 2020 22:38:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd8c5c1c54681c13c0b8c3a2bc57867973e945d847f5d9eadddbe4368c77540`  
		Last Modified: Fri, 21 Feb 2020 22:37:59 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f7fb2198b888d79b72c745d2130adc19213398ae3fac9631e98c6a8f6f128f`  
		Last Modified: Fri, 21 Feb 2020 22:37:59 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f630485b2c56c8706faa0a45bb123c968dc150a878e45eba0014ce3ca4d235`  
		Last Modified: Fri, 21 Feb 2020 22:38:19 GMT  
		Size: 126.1 MB (126136898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64555c5c853ffac8525a186c8038b7e67d4fbcc02d07f8e129e6ae70e5ca668f`  
		Last Modified: Fri, 21 Feb 2020 22:38:05 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d128c4bb10ec54ee27fce624769033a0191750dbc6b46a63a576aed005f086f`  
		Last Modified: Fri, 21 Feb 2020 22:38:04 GMT  
		Size: 4.0 KB (3952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.2-windowsservercore`

```console
$ docker pull mongo@sha256:a6f3b2e274f112882de6bfb127033534f068a11fdbd123fb549104b79f50860f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3506; amd64
	-	windows version 10.0.17763.1098; amd64

### `mongo:4.2-windowsservercore` - windows version 10.0.14393.3506; amd64

```console
$ docker pull mongo@sha256:ffcd7945296fd6bf2d492a8fbd2d76b87b4d700b617a3dbc3113ad3609dc1e99
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5823379228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b1841c6da45b9f09da659b319ee3ec76161c255d3a0299c744e58541cf1d5f`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 05:12:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 20 Feb 2020 05:31:28 GMT
ENV MONGO_VERSION=4.2.3
# Wed, 11 Mar 2020 22:59:46 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.3-signed.msi
# Wed, 11 Mar 2020 22:59:47 GMT
ENV MONGO_DOWNLOAD_SHA256=234f6abf9c4947df94428f6ce648905dbf6b1269f48cc3239ebd4990bde1ca2a
# Wed, 11 Mar 2020 23:17:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Mar 2020 23:17:16 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Mar 2020 23:17:18 GMT
EXPOSE 27017
# Wed, 11 Mar 2020 23:17:19 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:846a2223e9e7a88a2a07d706553f144d380483d72fb9f0697c4fcd71773a8693`  
		Size: 1.7 GB (1657079102 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0961c48658cd7865bcf6c05285dfbe8ad89cd52059088d7f4eed6fde1bb2b385`  
		Last Modified: Thu, 20 Feb 2020 05:18:25 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53763da721aa3ae58cd704805589abe169e1d3d28218280db0ed4045881d52cc`  
		Last Modified: Thu, 20 Feb 2020 05:44:18 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28575cbb1dce05be3e8ec069dac86a4ae8b751008d4f0c9654ea8a5adb6a05d`  
		Last Modified: Wed, 11 Mar 2020 23:40:27 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b0fd752a2977b6c56e9008cdf13c5221932c0fa7d04c8b82af7b1e365d7dcb`  
		Last Modified: Wed, 11 Mar 2020 23:40:24 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a599774a11cf582afd1c631f47ee898b2d7b7bd6c85e6a169f55999aebaf3f`  
		Last Modified: Wed, 11 Mar 2020 23:40:50 GMT  
		Size: 96.3 MB (96305864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158acd728c1a7f81dc5ab0e6ab015b47dbfe43d906b6935e6b3fb5af9ac717c9`  
		Last Modified: Wed, 11 Mar 2020 23:40:25 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1207ac339b253e1f2d5d984071f0cd6b1c14321de6258b95f05756828577ef`  
		Last Modified: Wed, 11 Mar 2020 23:40:24 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7bafe8e7fe89107a1cc111971c17ff5bfed4f23c13b7e8351d50dfedc51894`  
		Last Modified: Wed, 11 Mar 2020 23:40:24 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2-windowsservercore` - windows version 10.0.17763.1098; amd64

```console
$ docker pull mongo@sha256:aac754de81af2f5d162c77a945382332cffd5575897c7601ef472343cb844896
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2720597037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d0aaebe9da6481c2ac37ceef6336551122a88bb8c6e0f0273b2b1408c89f3a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Tue, 10 Mar 2020 23:23:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Mar 2020 23:17:35 GMT
ENV MONGO_VERSION=4.2.3
# Wed, 11 Mar 2020 23:17:36 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.3-signed.msi
# Wed, 11 Mar 2020 23:17:37 GMT
ENV MONGO_DOWNLOAD_SHA256=234f6abf9c4947df94428f6ce648905dbf6b1269f48cc3239ebd4990bde1ca2a
# Wed, 11 Mar 2020 23:37:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Mar 2020 23:37:05 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Mar 2020 23:37:08 GMT
EXPOSE 27017
# Wed, 11 Mar 2020 23:37:09 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb49f89affc2d69b541463d095fdfbe61fa62e02b0aa5fa6d26bc134fb66bf35`  
		Last Modified: Wed, 11 Mar 2020 00:30:48 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a556cdd1dac3043338300637cf3645822f875ee02355952ab1cd7751e1b68bc`  
		Last Modified: Wed, 11 Mar 2020 23:41:10 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcc51a0e27cfe040ead7b64a7c6a800c4c738b534689744bc5736c486935beb`  
		Last Modified: Wed, 11 Mar 2020 23:41:10 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f7203b7c8fc0a4e01010792bc0a916bb1d80725bd8a4e8f11428ee3160d35f`  
		Last Modified: Wed, 11 Mar 2020 23:41:07 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22af9a292df27880e2bdab8b6325e55b0ca496959f7b3cbc864addc1d08d102d`  
		Last Modified: Wed, 11 Mar 2020 23:42:15 GMT  
		Size: 455.3 MB (455252292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb17de172b016b72e14b1ad1dc7b0d91f65115cd25a7268d5758b93956a3298f`  
		Last Modified: Wed, 11 Mar 2020 23:41:07 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a4339164f7d75bf46ec45b216b30960178423acd470a8d3f7fa23bcadb1e05`  
		Last Modified: Wed, 11 Mar 2020 23:41:07 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf29d93e6248494f3397e2328ebfe14d053d0679135d2853daa7460ecf197df7`  
		Last Modified: Wed, 11 Mar 2020 23:41:08 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.2-windowsservercore-1809`

```console
$ docker pull mongo@sha256:d934c0075f6a09fef6cba2d002d7f37e28f70e2007cacaa1bff067a56a097e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `mongo:4.2-windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull mongo@sha256:aac754de81af2f5d162c77a945382332cffd5575897c7601ef472343cb844896
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2720597037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d0aaebe9da6481c2ac37ceef6336551122a88bb8c6e0f0273b2b1408c89f3a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Tue, 10 Mar 2020 23:23:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Mar 2020 23:17:35 GMT
ENV MONGO_VERSION=4.2.3
# Wed, 11 Mar 2020 23:17:36 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.3-signed.msi
# Wed, 11 Mar 2020 23:17:37 GMT
ENV MONGO_DOWNLOAD_SHA256=234f6abf9c4947df94428f6ce648905dbf6b1269f48cc3239ebd4990bde1ca2a
# Wed, 11 Mar 2020 23:37:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Mar 2020 23:37:05 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Mar 2020 23:37:08 GMT
EXPOSE 27017
# Wed, 11 Mar 2020 23:37:09 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb49f89affc2d69b541463d095fdfbe61fa62e02b0aa5fa6d26bc134fb66bf35`  
		Last Modified: Wed, 11 Mar 2020 00:30:48 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a556cdd1dac3043338300637cf3645822f875ee02355952ab1cd7751e1b68bc`  
		Last Modified: Wed, 11 Mar 2020 23:41:10 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcc51a0e27cfe040ead7b64a7c6a800c4c738b534689744bc5736c486935beb`  
		Last Modified: Wed, 11 Mar 2020 23:41:10 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f7203b7c8fc0a4e01010792bc0a916bb1d80725bd8a4e8f11428ee3160d35f`  
		Last Modified: Wed, 11 Mar 2020 23:41:07 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22af9a292df27880e2bdab8b6325e55b0ca496959f7b3cbc864addc1d08d102d`  
		Last Modified: Wed, 11 Mar 2020 23:42:15 GMT  
		Size: 455.3 MB (455252292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb17de172b016b72e14b1ad1dc7b0d91f65115cd25a7268d5758b93956a3298f`  
		Last Modified: Wed, 11 Mar 2020 23:41:07 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a4339164f7d75bf46ec45b216b30960178423acd470a8d3f7fa23bcadb1e05`  
		Last Modified: Wed, 11 Mar 2020 23:41:07 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf29d93e6248494f3397e2328ebfe14d053d0679135d2853daa7460ecf197df7`  
		Last Modified: Wed, 11 Mar 2020 23:41:08 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.2-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:252d9092a44cb76ce1978defc409db903e14ffa2b022b7a58293c4583db38a47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3506; amd64

### `mongo:4.2-windowsservercore-ltsc2016` - windows version 10.0.14393.3506; amd64

```console
$ docker pull mongo@sha256:ffcd7945296fd6bf2d492a8fbd2d76b87b4d700b617a3dbc3113ad3609dc1e99
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5823379228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b1841c6da45b9f09da659b319ee3ec76161c255d3a0299c744e58541cf1d5f`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 05:12:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 20 Feb 2020 05:31:28 GMT
ENV MONGO_VERSION=4.2.3
# Wed, 11 Mar 2020 22:59:46 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.3-signed.msi
# Wed, 11 Mar 2020 22:59:47 GMT
ENV MONGO_DOWNLOAD_SHA256=234f6abf9c4947df94428f6ce648905dbf6b1269f48cc3239ebd4990bde1ca2a
# Wed, 11 Mar 2020 23:17:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Mar 2020 23:17:16 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Mar 2020 23:17:18 GMT
EXPOSE 27017
# Wed, 11 Mar 2020 23:17:19 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:846a2223e9e7a88a2a07d706553f144d380483d72fb9f0697c4fcd71773a8693`  
		Size: 1.7 GB (1657079102 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0961c48658cd7865bcf6c05285dfbe8ad89cd52059088d7f4eed6fde1bb2b385`  
		Last Modified: Thu, 20 Feb 2020 05:18:25 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53763da721aa3ae58cd704805589abe169e1d3d28218280db0ed4045881d52cc`  
		Last Modified: Thu, 20 Feb 2020 05:44:18 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28575cbb1dce05be3e8ec069dac86a4ae8b751008d4f0c9654ea8a5adb6a05d`  
		Last Modified: Wed, 11 Mar 2020 23:40:27 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b0fd752a2977b6c56e9008cdf13c5221932c0fa7d04c8b82af7b1e365d7dcb`  
		Last Modified: Wed, 11 Mar 2020 23:40:24 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a599774a11cf582afd1c631f47ee898b2d7b7bd6c85e6a169f55999aebaf3f`  
		Last Modified: Wed, 11 Mar 2020 23:40:50 GMT  
		Size: 96.3 MB (96305864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158acd728c1a7f81dc5ab0e6ab015b47dbfe43d906b6935e6b3fb5af9ac717c9`  
		Last Modified: Wed, 11 Mar 2020 23:40:25 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1207ac339b253e1f2d5d984071f0cd6b1c14321de6258b95f05756828577ef`  
		Last Modified: Wed, 11 Mar 2020 23:40:24 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7bafe8e7fe89107a1cc111971c17ff5bfed4f23c13b7e8351d50dfedc51894`  
		Last Modified: Wed, 11 Mar 2020 23:40:24 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4-bionic`

```console
$ docker pull mongo@sha256:e74f06447431bb0afe8ab0e260e22c664e5714a301b9ac2d92805f0da2a83be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `mongo:4-bionic` - linux; amd64

```console
$ docker pull mongo@sha256:c6e1710fc73d5a878ebc8b98c28d8897d5a4bbbb0e5d7ad758264d913e21ee71
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (163996273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcef5fd2979dbcbf76e46139680bf71c35925e344afa4703de43bdc44c6c526a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 21 Feb 2020 22:20:39 GMT
ADD file:91a750fb184711fde03c9172f41e8a907ccbb1bfb904c2c3f4ef595fcddbc3a9 in / 
# Fri, 21 Feb 2020 22:20:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:20:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:20:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:20:44 GMT
CMD ["/bin/bash"]
# Sat, 22 Feb 2020 01:09:51 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Sat, 22 Feb 2020 01:10:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 01:10:01 GMT
ENV GOSU_VERSION=1.11
# Sat, 22 Feb 2020 01:10:01 GMT
ENV JSYAML_VERSION=3.13.0
# Sat, 22 Feb 2020 01:10:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 22 Feb 2020 01:10:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 22 Feb 2020 01:10:19 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Sat, 22 Feb 2020 01:10:20 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Sat, 22 Feb 2020 01:10:20 GMT
ARG MONGO_PACKAGE=mongodb-org
# Sat, 22 Feb 2020 01:10:20 GMT
ARG MONGO_REPO=repo.mongodb.org
# Sat, 22 Feb 2020 01:10:20 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Sat, 22 Feb 2020 01:10:21 GMT
ENV MONGO_MAJOR=4.2
# Sat, 22 Feb 2020 01:10:21 GMT
ENV MONGO_VERSION=4.2.3
# Sat, 22 Feb 2020 01:10:21 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Sat, 22 Feb 2020 01:10:39 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Sat, 22 Feb 2020 01:10:40 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Sat, 22 Feb 2020 01:10:40 GMT
VOLUME [/data/db /data/configdb]
# Sat, 22 Feb 2020 01:10:40 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Sat, 22 Feb 2020 01:10:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 22 Feb 2020 01:10:41 GMT
EXPOSE 27017
# Sat, 22 Feb 2020 01:10:41 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:423ae2b273f4c17ceee9e8482fa8d071d90c7d052ae208e1fe4963fceb3d6954`  
		Last Modified: Wed, 19 Feb 2020 13:21:21 GMT  
		Size: 26.7 MB (26692096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de83a2304fa1f7c4a13708a0d15b9704f5945c2be5cbb2b3ed9b2ccb718d0b3d`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a83bce3af0648efaa60b9bb28225b09136d2d35d0bed25ac764297076dec1b`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b53be908de2c0c78070fff0a9f04835211b3156c4e73785747af365e71a0d7`  
		Last Modified: Fri, 21 Feb 2020 22:22:50 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cc2fb4f0eb1b8b82496ad1e17ec728355d84d889f8fd43ac357de9c6daaae6`  
		Last Modified: Sat, 22 Feb 2020 01:11:46 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f552d845039c0b94c06de56dc454b604142c32a69268bbc374a05470cc888431`  
		Last Modified: Sat, 22 Feb 2020 01:11:47 GMT  
		Size: 3.0 MB (2982680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6e166a9814b17b9c5dc683a8a35855eea3d9a898f77c0ee310f2038f29fce6`  
		Last Modified: Sat, 22 Feb 2020 01:11:47 GMT  
		Size: 5.8 MB (5764092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2ba5bee263bb3922f6c6a693b088d8d4753d4d90c05edd7534c2d80fc66358`  
		Last Modified: Sat, 22 Feb 2020 01:11:46 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828a1244f9760b1f6ff171f61f81c4fb01be2128e86e070c53e5b90658c40c8f`  
		Last Modified: Sat, 22 Feb 2020 01:11:45 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63a86989a84986d2b7e0e4ba20e65cdf25b2785771363571320bcd39f1d3494`  
		Last Modified: Sat, 22 Feb 2020 01:11:45 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc2ee27e8bbd1744066620810df67cf8b783b2b658f3edc0c852d75bfae74ca`  
		Last Modified: Sat, 22 Feb 2020 01:12:03 GMT  
		Size: 128.5 MB (128513279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a06e64657c7706873ecc5363ca322af486258b0e2a7c26fab7f46343ba622e`  
		Last Modified: Sat, 22 Feb 2020 01:11:45 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca7a59243040eff21e5c6d08a9e1b6b3be459f869ac615b51ec2a4949948128`  
		Last Modified: Sat, 22 Feb 2020 01:11:45 GMT  
		Size: 4.0 KB (3954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-bionic` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:d06ed06348a9b1815c5bc265d58f3706762f8a10fd9d7b4f1b9b7bb83f1673c9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (154023756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91cd6dddcfbe299cfe0222a6a9bc21d01f7b4561a6cb63efce4975d09b957c26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 21 Feb 2020 21:54:16 GMT
ADD file:d827a0b8f08011678a718254c1220408c7e6c7ab03ae4259b415542309f18578 in / 
# Fri, 21 Feb 2020 21:54:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:54:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:54:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:54:25 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:50:43 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 21 Feb 2020 22:51:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:51:02 GMT
ENV GOSU_VERSION=1.11
# Fri, 21 Feb 2020 22:51:03 GMT
ENV JSYAML_VERSION=3.13.0
# Fri, 21 Feb 2020 22:51:30 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 21 Feb 2020 22:51:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:51:33 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 21 Feb 2020 22:51:35 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:51:35 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 21 Feb 2020 22:51:37 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:51:37 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:51:38 GMT
ENV MONGO_MAJOR=4.2
# Fri, 21 Feb 2020 22:51:39 GMT
ENV MONGO_VERSION=4.2.3
# Fri, 21 Feb 2020 22:51:41 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 21 Feb 2020 22:52:11 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 21 Feb 2020 22:52:13 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 21 Feb 2020 22:52:14 GMT
VOLUME [/data/db /data/configdb]
# Fri, 21 Feb 2020 22:52:14 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:52:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:52:16 GMT
EXPOSE 27017
# Fri, 21 Feb 2020 22:52:16 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:6695dc10aaa5cd71c433dfb366e84804eb5fbee91eab1e113442040d6ef4c9e0`  
		Last Modified: Fri, 21 Feb 2020 21:56:13 GMT  
		Size: 23.7 MB (23721143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72aab8f928deff72c9b5867c93524a60e3f8cf1b7401c88b0ede8dc3c595e828`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e83b6447acdea2afff1a10052ebc551d15bfd1d2a93a202699f7a458c612c07`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6a91485a919c412d218b6441c339f691079ff88e6d28734b1cc3d5938cf58d`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce30eb24f9ee36f81283e24d44464d289f8925925dd29948021da9875c68ada`  
		Last Modified: Fri, 21 Feb 2020 22:53:51 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40c1d7ad1d1ea72814e10a3a2a7a82e998ae6f374122d24456bbda9bf38e068`  
		Last Modified: Fri, 21 Feb 2020 22:53:51 GMT  
		Size: 2.7 MB (2676051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c7fbc92b61b056c0d3a8e0b548ffe9f5d488c6ea126c0a27d97efbb4f4befad`  
		Last Modified: Fri, 21 Feb 2020 22:53:51 GMT  
		Size: 5.3 MB (5283262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31687588808d10bf423bf6473235a0ba3c81ee24391fcb307a550ef4f12161e`  
		Last Modified: Fri, 21 Feb 2020 22:53:50 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd05cdedee7f57674a001111e63e8d59a002bf511c3878b74313795359de0d7`  
		Last Modified: Fri, 21 Feb 2020 22:53:47 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af7b837ad38bf29cafd860d9a45a0ac68d398991d2c18660806e4d9bd570ba2e`  
		Last Modified: Fri, 21 Feb 2020 22:53:48 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1886e577ef072dc81cbc19ec5cb5da2cd43a40a0b8bfd5cc1f649630a8e350c`  
		Last Modified: Fri, 21 Feb 2020 22:54:13 GMT  
		Size: 122.3 MB (122299237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c2758fd66f09bc1675a0459df7ac7f51a7226772ca6f84430622c6f74fe6cb`  
		Last Modified: Fri, 21 Feb 2020 22:53:47 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf80da1fa0a60da920fc9b9f3f655290968ebb2335db548ad307c952fd6d933`  
		Last Modified: Fri, 21 Feb 2020 22:53:48 GMT  
		Size: 4.0 KB (3952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-bionic` - linux; s390x

```console
$ docker pull mongo@sha256:f680daf0de2259244447be2895d266431defeebea01fba22433c12ffec9bdb01
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.9 MB (159948448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1d6d571c4e0118b833c5aad42620aa5ec5f67c8d3f1f4f9d65e677e88e4b4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 21 Feb 2020 21:57:46 GMT
ADD file:7925c9b35ffa1870e7d336ddcdd6c3434715178c7d08ff2ce9796b651302c347 in / 
# Fri, 21 Feb 2020 21:57:50 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:57:51 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:57:53 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:57:53 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:35:53 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 21 Feb 2020 22:36:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:36:07 GMT
ENV GOSU_VERSION=1.11
# Fri, 21 Feb 2020 22:36:08 GMT
ENV JSYAML_VERSION=3.13.0
# Fri, 21 Feb 2020 22:36:32 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 21 Feb 2020 22:36:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:36:35 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 21 Feb 2020 22:36:37 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:36:38 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 21 Feb 2020 22:36:38 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:36:39 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:36:40 GMT
ENV MONGO_MAJOR=4.2
# Fri, 21 Feb 2020 22:36:40 GMT
ENV MONGO_VERSION=4.2.3
# Fri, 21 Feb 2020 22:36:42 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 21 Feb 2020 22:37:22 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 21 Feb 2020 22:37:34 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 21 Feb 2020 22:37:35 GMT
VOLUME [/data/db /data/configdb]
# Fri, 21 Feb 2020 22:37:35 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:37:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:37:36 GMT
EXPOSE 27017
# Fri, 21 Feb 2020 22:37:37 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:b84fcb37dc33cf7416e0f1cf1219e16a15ab0d1c3aa4638d362f19c2679451de`  
		Last Modified: Fri, 21 Feb 2020 21:59:09 GMT  
		Size: 25.4 MB (25365672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9594931f903b7b3c4f5cb63196d29d715c50b567c128a5572131c12a25f04139`  
		Last Modified: Fri, 21 Feb 2020 21:59:06 GMT  
		Size: 36.2 KB (36186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66af13675c2330803d61d2198bb4f69c36bb7eed2d2b2bc3660fed8e873dce59`  
		Last Modified: Fri, 21 Feb 2020 21:59:11 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae0fb7b2ee5c5bc387374bdd08f53541bdfcf678d9b9f83489c3923af65fed0`  
		Last Modified: Fri, 21 Feb 2020 21:59:21 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20167b6352cf148caf092b98ebcd5a57b9008a2bc70e24c6a1aa4b6d54597e4`  
		Last Modified: Fri, 21 Feb 2020 22:38:04 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2c5aee18e04f08b2d2246738dd9239c3fc17fbc5629693a785574101ac5259`  
		Last Modified: Fri, 21 Feb 2020 22:38:03 GMT  
		Size: 2.7 MB (2714796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:679a24e64e261a1b368092a0ac88f8c4caf2a56ddbeb080a0b8d40e8892e07d5`  
		Last Modified: Fri, 21 Feb 2020 22:38:02 GMT  
		Size: 5.7 MB (5686031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a3aec4f6061abbba88c3ade7fef1e34e6fd70dbe30c3a9b5f0fbc64d2958e8`  
		Last Modified: Fri, 21 Feb 2020 22:38:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd8c5c1c54681c13c0b8c3a2bc57867973e945d847f5d9eadddbe4368c77540`  
		Last Modified: Fri, 21 Feb 2020 22:37:59 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f7fb2198b888d79b72c745d2130adc19213398ae3fac9631e98c6a8f6f128f`  
		Last Modified: Fri, 21 Feb 2020 22:37:59 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f630485b2c56c8706faa0a45bb123c968dc150a878e45eba0014ce3ca4d235`  
		Last Modified: Fri, 21 Feb 2020 22:38:19 GMT  
		Size: 126.1 MB (126136898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64555c5c853ffac8525a186c8038b7e67d4fbcc02d07f8e129e6ae70e5ca668f`  
		Last Modified: Fri, 21 Feb 2020 22:38:05 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d128c4bb10ec54ee27fce624769033a0191750dbc6b46a63a576aed005f086f`  
		Last Modified: Fri, 21 Feb 2020 22:38:04 GMT  
		Size: 4.0 KB (3952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4-windowsservercore`

```console
$ docker pull mongo@sha256:a6f3b2e274f112882de6bfb127033534f068a11fdbd123fb549104b79f50860f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3506; amd64
	-	windows version 10.0.17763.1098; amd64

### `mongo:4-windowsservercore` - windows version 10.0.14393.3506; amd64

```console
$ docker pull mongo@sha256:ffcd7945296fd6bf2d492a8fbd2d76b87b4d700b617a3dbc3113ad3609dc1e99
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5823379228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b1841c6da45b9f09da659b319ee3ec76161c255d3a0299c744e58541cf1d5f`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 05:12:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 20 Feb 2020 05:31:28 GMT
ENV MONGO_VERSION=4.2.3
# Wed, 11 Mar 2020 22:59:46 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.3-signed.msi
# Wed, 11 Mar 2020 22:59:47 GMT
ENV MONGO_DOWNLOAD_SHA256=234f6abf9c4947df94428f6ce648905dbf6b1269f48cc3239ebd4990bde1ca2a
# Wed, 11 Mar 2020 23:17:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Mar 2020 23:17:16 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Mar 2020 23:17:18 GMT
EXPOSE 27017
# Wed, 11 Mar 2020 23:17:19 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:846a2223e9e7a88a2a07d706553f144d380483d72fb9f0697c4fcd71773a8693`  
		Size: 1.7 GB (1657079102 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0961c48658cd7865bcf6c05285dfbe8ad89cd52059088d7f4eed6fde1bb2b385`  
		Last Modified: Thu, 20 Feb 2020 05:18:25 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53763da721aa3ae58cd704805589abe169e1d3d28218280db0ed4045881d52cc`  
		Last Modified: Thu, 20 Feb 2020 05:44:18 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28575cbb1dce05be3e8ec069dac86a4ae8b751008d4f0c9654ea8a5adb6a05d`  
		Last Modified: Wed, 11 Mar 2020 23:40:27 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b0fd752a2977b6c56e9008cdf13c5221932c0fa7d04c8b82af7b1e365d7dcb`  
		Last Modified: Wed, 11 Mar 2020 23:40:24 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a599774a11cf582afd1c631f47ee898b2d7b7bd6c85e6a169f55999aebaf3f`  
		Last Modified: Wed, 11 Mar 2020 23:40:50 GMT  
		Size: 96.3 MB (96305864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158acd728c1a7f81dc5ab0e6ab015b47dbfe43d906b6935e6b3fb5af9ac717c9`  
		Last Modified: Wed, 11 Mar 2020 23:40:25 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1207ac339b253e1f2d5d984071f0cd6b1c14321de6258b95f05756828577ef`  
		Last Modified: Wed, 11 Mar 2020 23:40:24 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7bafe8e7fe89107a1cc111971c17ff5bfed4f23c13b7e8351d50dfedc51894`  
		Last Modified: Wed, 11 Mar 2020 23:40:24 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-windowsservercore` - windows version 10.0.17763.1098; amd64

```console
$ docker pull mongo@sha256:aac754de81af2f5d162c77a945382332cffd5575897c7601ef472343cb844896
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2720597037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d0aaebe9da6481c2ac37ceef6336551122a88bb8c6e0f0273b2b1408c89f3a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Tue, 10 Mar 2020 23:23:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Mar 2020 23:17:35 GMT
ENV MONGO_VERSION=4.2.3
# Wed, 11 Mar 2020 23:17:36 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.3-signed.msi
# Wed, 11 Mar 2020 23:17:37 GMT
ENV MONGO_DOWNLOAD_SHA256=234f6abf9c4947df94428f6ce648905dbf6b1269f48cc3239ebd4990bde1ca2a
# Wed, 11 Mar 2020 23:37:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Mar 2020 23:37:05 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Mar 2020 23:37:08 GMT
EXPOSE 27017
# Wed, 11 Mar 2020 23:37:09 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb49f89affc2d69b541463d095fdfbe61fa62e02b0aa5fa6d26bc134fb66bf35`  
		Last Modified: Wed, 11 Mar 2020 00:30:48 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a556cdd1dac3043338300637cf3645822f875ee02355952ab1cd7751e1b68bc`  
		Last Modified: Wed, 11 Mar 2020 23:41:10 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcc51a0e27cfe040ead7b64a7c6a800c4c738b534689744bc5736c486935beb`  
		Last Modified: Wed, 11 Mar 2020 23:41:10 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f7203b7c8fc0a4e01010792bc0a916bb1d80725bd8a4e8f11428ee3160d35f`  
		Last Modified: Wed, 11 Mar 2020 23:41:07 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22af9a292df27880e2bdab8b6325e55b0ca496959f7b3cbc864addc1d08d102d`  
		Last Modified: Wed, 11 Mar 2020 23:42:15 GMT  
		Size: 455.3 MB (455252292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb17de172b016b72e14b1ad1dc7b0d91f65115cd25a7268d5758b93956a3298f`  
		Last Modified: Wed, 11 Mar 2020 23:41:07 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a4339164f7d75bf46ec45b216b30960178423acd470a8d3f7fa23bcadb1e05`  
		Last Modified: Wed, 11 Mar 2020 23:41:07 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf29d93e6248494f3397e2328ebfe14d053d0679135d2853daa7460ecf197df7`  
		Last Modified: Wed, 11 Mar 2020 23:41:08 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4-windowsservercore-1809`

```console
$ docker pull mongo@sha256:d934c0075f6a09fef6cba2d002d7f37e28f70e2007cacaa1bff067a56a097e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `mongo:4-windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull mongo@sha256:aac754de81af2f5d162c77a945382332cffd5575897c7601ef472343cb844896
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2720597037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d0aaebe9da6481c2ac37ceef6336551122a88bb8c6e0f0273b2b1408c89f3a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Tue, 10 Mar 2020 23:23:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Mar 2020 23:17:35 GMT
ENV MONGO_VERSION=4.2.3
# Wed, 11 Mar 2020 23:17:36 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.3-signed.msi
# Wed, 11 Mar 2020 23:17:37 GMT
ENV MONGO_DOWNLOAD_SHA256=234f6abf9c4947df94428f6ce648905dbf6b1269f48cc3239ebd4990bde1ca2a
# Wed, 11 Mar 2020 23:37:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Mar 2020 23:37:05 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Mar 2020 23:37:08 GMT
EXPOSE 27017
# Wed, 11 Mar 2020 23:37:09 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb49f89affc2d69b541463d095fdfbe61fa62e02b0aa5fa6d26bc134fb66bf35`  
		Last Modified: Wed, 11 Mar 2020 00:30:48 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a556cdd1dac3043338300637cf3645822f875ee02355952ab1cd7751e1b68bc`  
		Last Modified: Wed, 11 Mar 2020 23:41:10 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcc51a0e27cfe040ead7b64a7c6a800c4c738b534689744bc5736c486935beb`  
		Last Modified: Wed, 11 Mar 2020 23:41:10 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f7203b7c8fc0a4e01010792bc0a916bb1d80725bd8a4e8f11428ee3160d35f`  
		Last Modified: Wed, 11 Mar 2020 23:41:07 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22af9a292df27880e2bdab8b6325e55b0ca496959f7b3cbc864addc1d08d102d`  
		Last Modified: Wed, 11 Mar 2020 23:42:15 GMT  
		Size: 455.3 MB (455252292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb17de172b016b72e14b1ad1dc7b0d91f65115cd25a7268d5758b93956a3298f`  
		Last Modified: Wed, 11 Mar 2020 23:41:07 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a4339164f7d75bf46ec45b216b30960178423acd470a8d3f7fa23bcadb1e05`  
		Last Modified: Wed, 11 Mar 2020 23:41:07 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf29d93e6248494f3397e2328ebfe14d053d0679135d2853daa7460ecf197df7`  
		Last Modified: Wed, 11 Mar 2020 23:41:08 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:252d9092a44cb76ce1978defc409db903e14ffa2b022b7a58293c4583db38a47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3506; amd64

### `mongo:4-windowsservercore-ltsc2016` - windows version 10.0.14393.3506; amd64

```console
$ docker pull mongo@sha256:ffcd7945296fd6bf2d492a8fbd2d76b87b4d700b617a3dbc3113ad3609dc1e99
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5823379228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b1841c6da45b9f09da659b319ee3ec76161c255d3a0299c744e58541cf1d5f`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 05:12:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 20 Feb 2020 05:31:28 GMT
ENV MONGO_VERSION=4.2.3
# Wed, 11 Mar 2020 22:59:46 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.3-signed.msi
# Wed, 11 Mar 2020 22:59:47 GMT
ENV MONGO_DOWNLOAD_SHA256=234f6abf9c4947df94428f6ce648905dbf6b1269f48cc3239ebd4990bde1ca2a
# Wed, 11 Mar 2020 23:17:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Mar 2020 23:17:16 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Mar 2020 23:17:18 GMT
EXPOSE 27017
# Wed, 11 Mar 2020 23:17:19 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:846a2223e9e7a88a2a07d706553f144d380483d72fb9f0697c4fcd71773a8693`  
		Size: 1.7 GB (1657079102 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0961c48658cd7865bcf6c05285dfbe8ad89cd52059088d7f4eed6fde1bb2b385`  
		Last Modified: Thu, 20 Feb 2020 05:18:25 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53763da721aa3ae58cd704805589abe169e1d3d28218280db0ed4045881d52cc`  
		Last Modified: Thu, 20 Feb 2020 05:44:18 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28575cbb1dce05be3e8ec069dac86a4ae8b751008d4f0c9654ea8a5adb6a05d`  
		Last Modified: Wed, 11 Mar 2020 23:40:27 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b0fd752a2977b6c56e9008cdf13c5221932c0fa7d04c8b82af7b1e365d7dcb`  
		Last Modified: Wed, 11 Mar 2020 23:40:24 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a599774a11cf582afd1c631f47ee898b2d7b7bd6c85e6a169f55999aebaf3f`  
		Last Modified: Wed, 11 Mar 2020 23:40:50 GMT  
		Size: 96.3 MB (96305864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158acd728c1a7f81dc5ab0e6ab015b47dbfe43d906b6935e6b3fb5af9ac717c9`  
		Last Modified: Wed, 11 Mar 2020 23:40:25 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1207ac339b253e1f2d5d984071f0cd6b1c14321de6258b95f05756828577ef`  
		Last Modified: Wed, 11 Mar 2020 23:40:24 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7bafe8e7fe89107a1cc111971c17ff5bfed4f23c13b7e8351d50dfedc51894`  
		Last Modified: Wed, 11 Mar 2020 23:40:24 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:bionic`

```console
$ docker pull mongo@sha256:e74f06447431bb0afe8ab0e260e22c664e5714a301b9ac2d92805f0da2a83be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `mongo:bionic` - linux; amd64

```console
$ docker pull mongo@sha256:c6e1710fc73d5a878ebc8b98c28d8897d5a4bbbb0e5d7ad758264d913e21ee71
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (163996273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcef5fd2979dbcbf76e46139680bf71c35925e344afa4703de43bdc44c6c526a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 21 Feb 2020 22:20:39 GMT
ADD file:91a750fb184711fde03c9172f41e8a907ccbb1bfb904c2c3f4ef595fcddbc3a9 in / 
# Fri, 21 Feb 2020 22:20:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:20:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:20:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:20:44 GMT
CMD ["/bin/bash"]
# Sat, 22 Feb 2020 01:09:51 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Sat, 22 Feb 2020 01:10:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 01:10:01 GMT
ENV GOSU_VERSION=1.11
# Sat, 22 Feb 2020 01:10:01 GMT
ENV JSYAML_VERSION=3.13.0
# Sat, 22 Feb 2020 01:10:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 22 Feb 2020 01:10:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 22 Feb 2020 01:10:19 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Sat, 22 Feb 2020 01:10:20 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Sat, 22 Feb 2020 01:10:20 GMT
ARG MONGO_PACKAGE=mongodb-org
# Sat, 22 Feb 2020 01:10:20 GMT
ARG MONGO_REPO=repo.mongodb.org
# Sat, 22 Feb 2020 01:10:20 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Sat, 22 Feb 2020 01:10:21 GMT
ENV MONGO_MAJOR=4.2
# Sat, 22 Feb 2020 01:10:21 GMT
ENV MONGO_VERSION=4.2.3
# Sat, 22 Feb 2020 01:10:21 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Sat, 22 Feb 2020 01:10:39 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Sat, 22 Feb 2020 01:10:40 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Sat, 22 Feb 2020 01:10:40 GMT
VOLUME [/data/db /data/configdb]
# Sat, 22 Feb 2020 01:10:40 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Sat, 22 Feb 2020 01:10:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 22 Feb 2020 01:10:41 GMT
EXPOSE 27017
# Sat, 22 Feb 2020 01:10:41 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:423ae2b273f4c17ceee9e8482fa8d071d90c7d052ae208e1fe4963fceb3d6954`  
		Last Modified: Wed, 19 Feb 2020 13:21:21 GMT  
		Size: 26.7 MB (26692096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de83a2304fa1f7c4a13708a0d15b9704f5945c2be5cbb2b3ed9b2ccb718d0b3d`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a83bce3af0648efaa60b9bb28225b09136d2d35d0bed25ac764297076dec1b`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b53be908de2c0c78070fff0a9f04835211b3156c4e73785747af365e71a0d7`  
		Last Modified: Fri, 21 Feb 2020 22:22:50 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cc2fb4f0eb1b8b82496ad1e17ec728355d84d889f8fd43ac357de9c6daaae6`  
		Last Modified: Sat, 22 Feb 2020 01:11:46 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f552d845039c0b94c06de56dc454b604142c32a69268bbc374a05470cc888431`  
		Last Modified: Sat, 22 Feb 2020 01:11:47 GMT  
		Size: 3.0 MB (2982680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6e166a9814b17b9c5dc683a8a35855eea3d9a898f77c0ee310f2038f29fce6`  
		Last Modified: Sat, 22 Feb 2020 01:11:47 GMT  
		Size: 5.8 MB (5764092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2ba5bee263bb3922f6c6a693b088d8d4753d4d90c05edd7534c2d80fc66358`  
		Last Modified: Sat, 22 Feb 2020 01:11:46 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828a1244f9760b1f6ff171f61f81c4fb01be2128e86e070c53e5b90658c40c8f`  
		Last Modified: Sat, 22 Feb 2020 01:11:45 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63a86989a84986d2b7e0e4ba20e65cdf25b2785771363571320bcd39f1d3494`  
		Last Modified: Sat, 22 Feb 2020 01:11:45 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc2ee27e8bbd1744066620810df67cf8b783b2b658f3edc0c852d75bfae74ca`  
		Last Modified: Sat, 22 Feb 2020 01:12:03 GMT  
		Size: 128.5 MB (128513279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a06e64657c7706873ecc5363ca322af486258b0e2a7c26fab7f46343ba622e`  
		Last Modified: Sat, 22 Feb 2020 01:11:45 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca7a59243040eff21e5c6d08a9e1b6b3be459f869ac615b51ec2a4949948128`  
		Last Modified: Sat, 22 Feb 2020 01:11:45 GMT  
		Size: 4.0 KB (3954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:bionic` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:d06ed06348a9b1815c5bc265d58f3706762f8a10fd9d7b4f1b9b7bb83f1673c9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (154023756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91cd6dddcfbe299cfe0222a6a9bc21d01f7b4561a6cb63efce4975d09b957c26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 21 Feb 2020 21:54:16 GMT
ADD file:d827a0b8f08011678a718254c1220408c7e6c7ab03ae4259b415542309f18578 in / 
# Fri, 21 Feb 2020 21:54:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:54:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:54:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:54:25 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:50:43 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 21 Feb 2020 22:51:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:51:02 GMT
ENV GOSU_VERSION=1.11
# Fri, 21 Feb 2020 22:51:03 GMT
ENV JSYAML_VERSION=3.13.0
# Fri, 21 Feb 2020 22:51:30 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 21 Feb 2020 22:51:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:51:33 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 21 Feb 2020 22:51:35 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:51:35 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 21 Feb 2020 22:51:37 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:51:37 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:51:38 GMT
ENV MONGO_MAJOR=4.2
# Fri, 21 Feb 2020 22:51:39 GMT
ENV MONGO_VERSION=4.2.3
# Fri, 21 Feb 2020 22:51:41 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 21 Feb 2020 22:52:11 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 21 Feb 2020 22:52:13 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 21 Feb 2020 22:52:14 GMT
VOLUME [/data/db /data/configdb]
# Fri, 21 Feb 2020 22:52:14 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:52:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:52:16 GMT
EXPOSE 27017
# Fri, 21 Feb 2020 22:52:16 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:6695dc10aaa5cd71c433dfb366e84804eb5fbee91eab1e113442040d6ef4c9e0`  
		Last Modified: Fri, 21 Feb 2020 21:56:13 GMT  
		Size: 23.7 MB (23721143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72aab8f928deff72c9b5867c93524a60e3f8cf1b7401c88b0ede8dc3c595e828`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e83b6447acdea2afff1a10052ebc551d15bfd1d2a93a202699f7a458c612c07`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6a91485a919c412d218b6441c339f691079ff88e6d28734b1cc3d5938cf58d`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce30eb24f9ee36f81283e24d44464d289f8925925dd29948021da9875c68ada`  
		Last Modified: Fri, 21 Feb 2020 22:53:51 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40c1d7ad1d1ea72814e10a3a2a7a82e998ae6f374122d24456bbda9bf38e068`  
		Last Modified: Fri, 21 Feb 2020 22:53:51 GMT  
		Size: 2.7 MB (2676051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c7fbc92b61b056c0d3a8e0b548ffe9f5d488c6ea126c0a27d97efbb4f4befad`  
		Last Modified: Fri, 21 Feb 2020 22:53:51 GMT  
		Size: 5.3 MB (5283262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31687588808d10bf423bf6473235a0ba3c81ee24391fcb307a550ef4f12161e`  
		Last Modified: Fri, 21 Feb 2020 22:53:50 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd05cdedee7f57674a001111e63e8d59a002bf511c3878b74313795359de0d7`  
		Last Modified: Fri, 21 Feb 2020 22:53:47 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af7b837ad38bf29cafd860d9a45a0ac68d398991d2c18660806e4d9bd570ba2e`  
		Last Modified: Fri, 21 Feb 2020 22:53:48 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1886e577ef072dc81cbc19ec5cb5da2cd43a40a0b8bfd5cc1f649630a8e350c`  
		Last Modified: Fri, 21 Feb 2020 22:54:13 GMT  
		Size: 122.3 MB (122299237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c2758fd66f09bc1675a0459df7ac7f51a7226772ca6f84430622c6f74fe6cb`  
		Last Modified: Fri, 21 Feb 2020 22:53:47 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf80da1fa0a60da920fc9b9f3f655290968ebb2335db548ad307c952fd6d933`  
		Last Modified: Fri, 21 Feb 2020 22:53:48 GMT  
		Size: 4.0 KB (3952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:bionic` - linux; s390x

```console
$ docker pull mongo@sha256:f680daf0de2259244447be2895d266431defeebea01fba22433c12ffec9bdb01
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.9 MB (159948448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1d6d571c4e0118b833c5aad42620aa5ec5f67c8d3f1f4f9d65e677e88e4b4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 21 Feb 2020 21:57:46 GMT
ADD file:7925c9b35ffa1870e7d336ddcdd6c3434715178c7d08ff2ce9796b651302c347 in / 
# Fri, 21 Feb 2020 21:57:50 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:57:51 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:57:53 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:57:53 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:35:53 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 21 Feb 2020 22:36:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:36:07 GMT
ENV GOSU_VERSION=1.11
# Fri, 21 Feb 2020 22:36:08 GMT
ENV JSYAML_VERSION=3.13.0
# Fri, 21 Feb 2020 22:36:32 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 21 Feb 2020 22:36:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:36:35 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 21 Feb 2020 22:36:37 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:36:38 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 21 Feb 2020 22:36:38 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:36:39 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:36:40 GMT
ENV MONGO_MAJOR=4.2
# Fri, 21 Feb 2020 22:36:40 GMT
ENV MONGO_VERSION=4.2.3
# Fri, 21 Feb 2020 22:36:42 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 21 Feb 2020 22:37:22 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 21 Feb 2020 22:37:34 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 21 Feb 2020 22:37:35 GMT
VOLUME [/data/db /data/configdb]
# Fri, 21 Feb 2020 22:37:35 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:37:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:37:36 GMT
EXPOSE 27017
# Fri, 21 Feb 2020 22:37:37 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:b84fcb37dc33cf7416e0f1cf1219e16a15ab0d1c3aa4638d362f19c2679451de`  
		Last Modified: Fri, 21 Feb 2020 21:59:09 GMT  
		Size: 25.4 MB (25365672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9594931f903b7b3c4f5cb63196d29d715c50b567c128a5572131c12a25f04139`  
		Last Modified: Fri, 21 Feb 2020 21:59:06 GMT  
		Size: 36.2 KB (36186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66af13675c2330803d61d2198bb4f69c36bb7eed2d2b2bc3660fed8e873dce59`  
		Last Modified: Fri, 21 Feb 2020 21:59:11 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae0fb7b2ee5c5bc387374bdd08f53541bdfcf678d9b9f83489c3923af65fed0`  
		Last Modified: Fri, 21 Feb 2020 21:59:21 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20167b6352cf148caf092b98ebcd5a57b9008a2bc70e24c6a1aa4b6d54597e4`  
		Last Modified: Fri, 21 Feb 2020 22:38:04 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2c5aee18e04f08b2d2246738dd9239c3fc17fbc5629693a785574101ac5259`  
		Last Modified: Fri, 21 Feb 2020 22:38:03 GMT  
		Size: 2.7 MB (2714796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:679a24e64e261a1b368092a0ac88f8c4caf2a56ddbeb080a0b8d40e8892e07d5`  
		Last Modified: Fri, 21 Feb 2020 22:38:02 GMT  
		Size: 5.7 MB (5686031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a3aec4f6061abbba88c3ade7fef1e34e6fd70dbe30c3a9b5f0fbc64d2958e8`  
		Last Modified: Fri, 21 Feb 2020 22:38:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd8c5c1c54681c13c0b8c3a2bc57867973e945d847f5d9eadddbe4368c77540`  
		Last Modified: Fri, 21 Feb 2020 22:37:59 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f7fb2198b888d79b72c745d2130adc19213398ae3fac9631e98c6a8f6f128f`  
		Last Modified: Fri, 21 Feb 2020 22:37:59 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f630485b2c56c8706faa0a45bb123c968dc150a878e45eba0014ce3ca4d235`  
		Last Modified: Fri, 21 Feb 2020 22:38:19 GMT  
		Size: 126.1 MB (126136898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64555c5c853ffac8525a186c8038b7e67d4fbcc02d07f8e129e6ae70e5ca668f`  
		Last Modified: Fri, 21 Feb 2020 22:38:05 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d128c4bb10ec54ee27fce624769033a0191750dbc6b46a63a576aed005f086f`  
		Last Modified: Fri, 21 Feb 2020 22:38:04 GMT  
		Size: 4.0 KB (3952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:latest`

```console
$ docker pull mongo@sha256:a1f116a08f48359302d7b567bdccc8b047bb0e534044de91be908c39eb796707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x
	-	windows version 10.0.14393.3506; amd64
	-	windows version 10.0.17763.1098; amd64

### `mongo:latest` - linux; amd64

```console
$ docker pull mongo@sha256:c6e1710fc73d5a878ebc8b98c28d8897d5a4bbbb0e5d7ad758264d913e21ee71
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (163996273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcef5fd2979dbcbf76e46139680bf71c35925e344afa4703de43bdc44c6c526a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 21 Feb 2020 22:20:39 GMT
ADD file:91a750fb184711fde03c9172f41e8a907ccbb1bfb904c2c3f4ef595fcddbc3a9 in / 
# Fri, 21 Feb 2020 22:20:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 22:20:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 22:20:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 22:20:44 GMT
CMD ["/bin/bash"]
# Sat, 22 Feb 2020 01:09:51 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Sat, 22 Feb 2020 01:10:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 22 Feb 2020 01:10:01 GMT
ENV GOSU_VERSION=1.11
# Sat, 22 Feb 2020 01:10:01 GMT
ENV JSYAML_VERSION=3.13.0
# Sat, 22 Feb 2020 01:10:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 22 Feb 2020 01:10:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 22 Feb 2020 01:10:19 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Sat, 22 Feb 2020 01:10:20 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Sat, 22 Feb 2020 01:10:20 GMT
ARG MONGO_PACKAGE=mongodb-org
# Sat, 22 Feb 2020 01:10:20 GMT
ARG MONGO_REPO=repo.mongodb.org
# Sat, 22 Feb 2020 01:10:20 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Sat, 22 Feb 2020 01:10:21 GMT
ENV MONGO_MAJOR=4.2
# Sat, 22 Feb 2020 01:10:21 GMT
ENV MONGO_VERSION=4.2.3
# Sat, 22 Feb 2020 01:10:21 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Sat, 22 Feb 2020 01:10:39 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Sat, 22 Feb 2020 01:10:40 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Sat, 22 Feb 2020 01:10:40 GMT
VOLUME [/data/db /data/configdb]
# Sat, 22 Feb 2020 01:10:40 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Sat, 22 Feb 2020 01:10:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 22 Feb 2020 01:10:41 GMT
EXPOSE 27017
# Sat, 22 Feb 2020 01:10:41 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:423ae2b273f4c17ceee9e8482fa8d071d90c7d052ae208e1fe4963fceb3d6954`  
		Last Modified: Wed, 19 Feb 2020 13:21:21 GMT  
		Size: 26.7 MB (26692096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de83a2304fa1f7c4a13708a0d15b9704f5945c2be5cbb2b3ed9b2ccb718d0b3d`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a83bce3af0648efaa60b9bb28225b09136d2d35d0bed25ac764297076dec1b`  
		Last Modified: Fri, 21 Feb 2020 22:22:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b53be908de2c0c78070fff0a9f04835211b3156c4e73785747af365e71a0d7`  
		Last Modified: Fri, 21 Feb 2020 22:22:50 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3cc2fb4f0eb1b8b82496ad1e17ec728355d84d889f8fd43ac357de9c6daaae6`  
		Last Modified: Sat, 22 Feb 2020 01:11:46 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f552d845039c0b94c06de56dc454b604142c32a69268bbc374a05470cc888431`  
		Last Modified: Sat, 22 Feb 2020 01:11:47 GMT  
		Size: 3.0 MB (2982680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6e166a9814b17b9c5dc683a8a35855eea3d9a898f77c0ee310f2038f29fce6`  
		Last Modified: Sat, 22 Feb 2020 01:11:47 GMT  
		Size: 5.8 MB (5764092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2ba5bee263bb3922f6c6a693b088d8d4753d4d90c05edd7534c2d80fc66358`  
		Last Modified: Sat, 22 Feb 2020 01:11:46 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828a1244f9760b1f6ff171f61f81c4fb01be2128e86e070c53e5b90658c40c8f`  
		Last Modified: Sat, 22 Feb 2020 01:11:45 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63a86989a84986d2b7e0e4ba20e65cdf25b2785771363571320bcd39f1d3494`  
		Last Modified: Sat, 22 Feb 2020 01:11:45 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc2ee27e8bbd1744066620810df67cf8b783b2b658f3edc0c852d75bfae74ca`  
		Last Modified: Sat, 22 Feb 2020 01:12:03 GMT  
		Size: 128.5 MB (128513279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a06e64657c7706873ecc5363ca322af486258b0e2a7c26fab7f46343ba622e`  
		Last Modified: Sat, 22 Feb 2020 01:11:45 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca7a59243040eff21e5c6d08a9e1b6b3be459f869ac615b51ec2a4949948128`  
		Last Modified: Sat, 22 Feb 2020 01:11:45 GMT  
		Size: 4.0 KB (3954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:d06ed06348a9b1815c5bc265d58f3706762f8a10fd9d7b4f1b9b7bb83f1673c9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (154023756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91cd6dddcfbe299cfe0222a6a9bc21d01f7b4561a6cb63efce4975d09b957c26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 21 Feb 2020 21:54:16 GMT
ADD file:d827a0b8f08011678a718254c1220408c7e6c7ab03ae4259b415542309f18578 in / 
# Fri, 21 Feb 2020 21:54:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:54:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:54:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:54:25 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:50:43 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 21 Feb 2020 22:51:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:51:02 GMT
ENV GOSU_VERSION=1.11
# Fri, 21 Feb 2020 22:51:03 GMT
ENV JSYAML_VERSION=3.13.0
# Fri, 21 Feb 2020 22:51:30 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 21 Feb 2020 22:51:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:51:33 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 21 Feb 2020 22:51:35 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:51:35 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 21 Feb 2020 22:51:37 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:51:37 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:51:38 GMT
ENV MONGO_MAJOR=4.2
# Fri, 21 Feb 2020 22:51:39 GMT
ENV MONGO_VERSION=4.2.3
# Fri, 21 Feb 2020 22:51:41 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 21 Feb 2020 22:52:11 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 21 Feb 2020 22:52:13 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 21 Feb 2020 22:52:14 GMT
VOLUME [/data/db /data/configdb]
# Fri, 21 Feb 2020 22:52:14 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:52:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:52:16 GMT
EXPOSE 27017
# Fri, 21 Feb 2020 22:52:16 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:6695dc10aaa5cd71c433dfb366e84804eb5fbee91eab1e113442040d6ef4c9e0`  
		Last Modified: Fri, 21 Feb 2020 21:56:13 GMT  
		Size: 23.7 MB (23721143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72aab8f928deff72c9b5867c93524a60e3f8cf1b7401c88b0ede8dc3c595e828`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e83b6447acdea2afff1a10052ebc551d15bfd1d2a93a202699f7a458c612c07`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6a91485a919c412d218b6441c339f691079ff88e6d28734b1cc3d5938cf58d`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce30eb24f9ee36f81283e24d44464d289f8925925dd29948021da9875c68ada`  
		Last Modified: Fri, 21 Feb 2020 22:53:51 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40c1d7ad1d1ea72814e10a3a2a7a82e998ae6f374122d24456bbda9bf38e068`  
		Last Modified: Fri, 21 Feb 2020 22:53:51 GMT  
		Size: 2.7 MB (2676051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c7fbc92b61b056c0d3a8e0b548ffe9f5d488c6ea126c0a27d97efbb4f4befad`  
		Last Modified: Fri, 21 Feb 2020 22:53:51 GMT  
		Size: 5.3 MB (5283262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31687588808d10bf423bf6473235a0ba3c81ee24391fcb307a550ef4f12161e`  
		Last Modified: Fri, 21 Feb 2020 22:53:50 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd05cdedee7f57674a001111e63e8d59a002bf511c3878b74313795359de0d7`  
		Last Modified: Fri, 21 Feb 2020 22:53:47 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af7b837ad38bf29cafd860d9a45a0ac68d398991d2c18660806e4d9bd570ba2e`  
		Last Modified: Fri, 21 Feb 2020 22:53:48 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1886e577ef072dc81cbc19ec5cb5da2cd43a40a0b8bfd5cc1f649630a8e350c`  
		Last Modified: Fri, 21 Feb 2020 22:54:13 GMT  
		Size: 122.3 MB (122299237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c2758fd66f09bc1675a0459df7ac7f51a7226772ca6f84430622c6f74fe6cb`  
		Last Modified: Fri, 21 Feb 2020 22:53:47 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf80da1fa0a60da920fc9b9f3f655290968ebb2335db548ad307c952fd6d933`  
		Last Modified: Fri, 21 Feb 2020 22:53:48 GMT  
		Size: 4.0 KB (3952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - linux; s390x

```console
$ docker pull mongo@sha256:f680daf0de2259244447be2895d266431defeebea01fba22433c12ffec9bdb01
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.9 MB (159948448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1d6d571c4e0118b833c5aad42620aa5ec5f67c8d3f1f4f9d65e677e88e4b4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 21 Feb 2020 21:57:46 GMT
ADD file:7925c9b35ffa1870e7d336ddcdd6c3434715178c7d08ff2ce9796b651302c347 in / 
# Fri, 21 Feb 2020 21:57:50 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:57:51 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:57:53 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:57:53 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:35:53 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 21 Feb 2020 22:36:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 21 Feb 2020 22:36:07 GMT
ENV GOSU_VERSION=1.11
# Fri, 21 Feb 2020 22:36:08 GMT
ENV JSYAML_VERSION=3.13.0
# Fri, 21 Feb 2020 22:36:32 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 21 Feb 2020 22:36:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 21 Feb 2020 22:36:35 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 21 Feb 2020 22:36:37 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 21 Feb 2020 22:36:38 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 21 Feb 2020 22:36:38 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:36:39 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 21 Feb 2020 22:36:40 GMT
ENV MONGO_MAJOR=4.2
# Fri, 21 Feb 2020 22:36:40 GMT
ENV MONGO_VERSION=4.2.3
# Fri, 21 Feb 2020 22:36:42 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 21 Feb 2020 22:37:22 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 21 Feb 2020 22:37:34 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 21 Feb 2020 22:37:35 GMT
VOLUME [/data/db /data/configdb]
# Fri, 21 Feb 2020 22:37:35 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Fri, 21 Feb 2020 22:37:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Feb 2020 22:37:36 GMT
EXPOSE 27017
# Fri, 21 Feb 2020 22:37:37 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:b84fcb37dc33cf7416e0f1cf1219e16a15ab0d1c3aa4638d362f19c2679451de`  
		Last Modified: Fri, 21 Feb 2020 21:59:09 GMT  
		Size: 25.4 MB (25365672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9594931f903b7b3c4f5cb63196d29d715c50b567c128a5572131c12a25f04139`  
		Last Modified: Fri, 21 Feb 2020 21:59:06 GMT  
		Size: 36.2 KB (36186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66af13675c2330803d61d2198bb4f69c36bb7eed2d2b2bc3660fed8e873dce59`  
		Last Modified: Fri, 21 Feb 2020 21:59:11 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae0fb7b2ee5c5bc387374bdd08f53541bdfcf678d9b9f83489c3923af65fed0`  
		Last Modified: Fri, 21 Feb 2020 21:59:21 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20167b6352cf148caf092b98ebcd5a57b9008a2bc70e24c6a1aa4b6d54597e4`  
		Last Modified: Fri, 21 Feb 2020 22:38:04 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2c5aee18e04f08b2d2246738dd9239c3fc17fbc5629693a785574101ac5259`  
		Last Modified: Fri, 21 Feb 2020 22:38:03 GMT  
		Size: 2.7 MB (2714796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:679a24e64e261a1b368092a0ac88f8c4caf2a56ddbeb080a0b8d40e8892e07d5`  
		Last Modified: Fri, 21 Feb 2020 22:38:02 GMT  
		Size: 5.7 MB (5686031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a3aec4f6061abbba88c3ade7fef1e34e6fd70dbe30c3a9b5f0fbc64d2958e8`  
		Last Modified: Fri, 21 Feb 2020 22:38:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd8c5c1c54681c13c0b8c3a2bc57867973e945d847f5d9eadddbe4368c77540`  
		Last Modified: Fri, 21 Feb 2020 22:37:59 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f7fb2198b888d79b72c745d2130adc19213398ae3fac9631e98c6a8f6f128f`  
		Last Modified: Fri, 21 Feb 2020 22:37:59 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f630485b2c56c8706faa0a45bb123c968dc150a878e45eba0014ce3ca4d235`  
		Last Modified: Fri, 21 Feb 2020 22:38:19 GMT  
		Size: 126.1 MB (126136898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64555c5c853ffac8525a186c8038b7e67d4fbcc02d07f8e129e6ae70e5ca668f`  
		Last Modified: Fri, 21 Feb 2020 22:38:05 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d128c4bb10ec54ee27fce624769033a0191750dbc6b46a63a576aed005f086f`  
		Last Modified: Fri, 21 Feb 2020 22:38:04 GMT  
		Size: 4.0 KB (3952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.14393.3506; amd64

```console
$ docker pull mongo@sha256:ffcd7945296fd6bf2d492a8fbd2d76b87b4d700b617a3dbc3113ad3609dc1e99
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5823379228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b1841c6da45b9f09da659b319ee3ec76161c255d3a0299c744e58541cf1d5f`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 05:12:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 20 Feb 2020 05:31:28 GMT
ENV MONGO_VERSION=4.2.3
# Wed, 11 Mar 2020 22:59:46 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.3-signed.msi
# Wed, 11 Mar 2020 22:59:47 GMT
ENV MONGO_DOWNLOAD_SHA256=234f6abf9c4947df94428f6ce648905dbf6b1269f48cc3239ebd4990bde1ca2a
# Wed, 11 Mar 2020 23:17:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Mar 2020 23:17:16 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Mar 2020 23:17:18 GMT
EXPOSE 27017
# Wed, 11 Mar 2020 23:17:19 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:846a2223e9e7a88a2a07d706553f144d380483d72fb9f0697c4fcd71773a8693`  
		Size: 1.7 GB (1657079102 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0961c48658cd7865bcf6c05285dfbe8ad89cd52059088d7f4eed6fde1bb2b385`  
		Last Modified: Thu, 20 Feb 2020 05:18:25 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53763da721aa3ae58cd704805589abe169e1d3d28218280db0ed4045881d52cc`  
		Last Modified: Thu, 20 Feb 2020 05:44:18 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28575cbb1dce05be3e8ec069dac86a4ae8b751008d4f0c9654ea8a5adb6a05d`  
		Last Modified: Wed, 11 Mar 2020 23:40:27 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b0fd752a2977b6c56e9008cdf13c5221932c0fa7d04c8b82af7b1e365d7dcb`  
		Last Modified: Wed, 11 Mar 2020 23:40:24 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a599774a11cf582afd1c631f47ee898b2d7b7bd6c85e6a169f55999aebaf3f`  
		Last Modified: Wed, 11 Mar 2020 23:40:50 GMT  
		Size: 96.3 MB (96305864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158acd728c1a7f81dc5ab0e6ab015b47dbfe43d906b6935e6b3fb5af9ac717c9`  
		Last Modified: Wed, 11 Mar 2020 23:40:25 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1207ac339b253e1f2d5d984071f0cd6b1c14321de6258b95f05756828577ef`  
		Last Modified: Wed, 11 Mar 2020 23:40:24 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7bafe8e7fe89107a1cc111971c17ff5bfed4f23c13b7e8351d50dfedc51894`  
		Last Modified: Wed, 11 Mar 2020 23:40:24 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.17763.1098; amd64

```console
$ docker pull mongo@sha256:aac754de81af2f5d162c77a945382332cffd5575897c7601ef472343cb844896
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2720597037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d0aaebe9da6481c2ac37ceef6336551122a88bb8c6e0f0273b2b1408c89f3a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Tue, 10 Mar 2020 23:23:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Mar 2020 23:17:35 GMT
ENV MONGO_VERSION=4.2.3
# Wed, 11 Mar 2020 23:17:36 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.3-signed.msi
# Wed, 11 Mar 2020 23:17:37 GMT
ENV MONGO_DOWNLOAD_SHA256=234f6abf9c4947df94428f6ce648905dbf6b1269f48cc3239ebd4990bde1ca2a
# Wed, 11 Mar 2020 23:37:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Mar 2020 23:37:05 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Mar 2020 23:37:08 GMT
EXPOSE 27017
# Wed, 11 Mar 2020 23:37:09 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb49f89affc2d69b541463d095fdfbe61fa62e02b0aa5fa6d26bc134fb66bf35`  
		Last Modified: Wed, 11 Mar 2020 00:30:48 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a556cdd1dac3043338300637cf3645822f875ee02355952ab1cd7751e1b68bc`  
		Last Modified: Wed, 11 Mar 2020 23:41:10 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcc51a0e27cfe040ead7b64a7c6a800c4c738b534689744bc5736c486935beb`  
		Last Modified: Wed, 11 Mar 2020 23:41:10 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f7203b7c8fc0a4e01010792bc0a916bb1d80725bd8a4e8f11428ee3160d35f`  
		Last Modified: Wed, 11 Mar 2020 23:41:07 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22af9a292df27880e2bdab8b6325e55b0ca496959f7b3cbc864addc1d08d102d`  
		Last Modified: Wed, 11 Mar 2020 23:42:15 GMT  
		Size: 455.3 MB (455252292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb17de172b016b72e14b1ad1dc7b0d91f65115cd25a7268d5758b93956a3298f`  
		Last Modified: Wed, 11 Mar 2020 23:41:07 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a4339164f7d75bf46ec45b216b30960178423acd470a8d3f7fa23bcadb1e05`  
		Last Modified: Wed, 11 Mar 2020 23:41:07 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf29d93e6248494f3397e2328ebfe14d053d0679135d2853daa7460ecf197df7`  
		Last Modified: Wed, 11 Mar 2020 23:41:08 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:windowsservercore`

```console
$ docker pull mongo@sha256:a6f3b2e274f112882de6bfb127033534f068a11fdbd123fb549104b79f50860f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3506; amd64
	-	windows version 10.0.17763.1098; amd64

### `mongo:windowsservercore` - windows version 10.0.14393.3506; amd64

```console
$ docker pull mongo@sha256:ffcd7945296fd6bf2d492a8fbd2d76b87b4d700b617a3dbc3113ad3609dc1e99
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5823379228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b1841c6da45b9f09da659b319ee3ec76161c255d3a0299c744e58541cf1d5f`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 05:12:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 20 Feb 2020 05:31:28 GMT
ENV MONGO_VERSION=4.2.3
# Wed, 11 Mar 2020 22:59:46 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.3-signed.msi
# Wed, 11 Mar 2020 22:59:47 GMT
ENV MONGO_DOWNLOAD_SHA256=234f6abf9c4947df94428f6ce648905dbf6b1269f48cc3239ebd4990bde1ca2a
# Wed, 11 Mar 2020 23:17:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Mar 2020 23:17:16 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Mar 2020 23:17:18 GMT
EXPOSE 27017
# Wed, 11 Mar 2020 23:17:19 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:846a2223e9e7a88a2a07d706553f144d380483d72fb9f0697c4fcd71773a8693`  
		Size: 1.7 GB (1657079102 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0961c48658cd7865bcf6c05285dfbe8ad89cd52059088d7f4eed6fde1bb2b385`  
		Last Modified: Thu, 20 Feb 2020 05:18:25 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53763da721aa3ae58cd704805589abe169e1d3d28218280db0ed4045881d52cc`  
		Last Modified: Thu, 20 Feb 2020 05:44:18 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28575cbb1dce05be3e8ec069dac86a4ae8b751008d4f0c9654ea8a5adb6a05d`  
		Last Modified: Wed, 11 Mar 2020 23:40:27 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b0fd752a2977b6c56e9008cdf13c5221932c0fa7d04c8b82af7b1e365d7dcb`  
		Last Modified: Wed, 11 Mar 2020 23:40:24 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a599774a11cf582afd1c631f47ee898b2d7b7bd6c85e6a169f55999aebaf3f`  
		Last Modified: Wed, 11 Mar 2020 23:40:50 GMT  
		Size: 96.3 MB (96305864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158acd728c1a7f81dc5ab0e6ab015b47dbfe43d906b6935e6b3fb5af9ac717c9`  
		Last Modified: Wed, 11 Mar 2020 23:40:25 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1207ac339b253e1f2d5d984071f0cd6b1c14321de6258b95f05756828577ef`  
		Last Modified: Wed, 11 Mar 2020 23:40:24 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7bafe8e7fe89107a1cc111971c17ff5bfed4f23c13b7e8351d50dfedc51894`  
		Last Modified: Wed, 11 Mar 2020 23:40:24 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:windowsservercore` - windows version 10.0.17763.1098; amd64

```console
$ docker pull mongo@sha256:aac754de81af2f5d162c77a945382332cffd5575897c7601ef472343cb844896
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2720597037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d0aaebe9da6481c2ac37ceef6336551122a88bb8c6e0f0273b2b1408c89f3a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Tue, 10 Mar 2020 23:23:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Mar 2020 23:17:35 GMT
ENV MONGO_VERSION=4.2.3
# Wed, 11 Mar 2020 23:17:36 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.3-signed.msi
# Wed, 11 Mar 2020 23:17:37 GMT
ENV MONGO_DOWNLOAD_SHA256=234f6abf9c4947df94428f6ce648905dbf6b1269f48cc3239ebd4990bde1ca2a
# Wed, 11 Mar 2020 23:37:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Mar 2020 23:37:05 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Mar 2020 23:37:08 GMT
EXPOSE 27017
# Wed, 11 Mar 2020 23:37:09 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb49f89affc2d69b541463d095fdfbe61fa62e02b0aa5fa6d26bc134fb66bf35`  
		Last Modified: Wed, 11 Mar 2020 00:30:48 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a556cdd1dac3043338300637cf3645822f875ee02355952ab1cd7751e1b68bc`  
		Last Modified: Wed, 11 Mar 2020 23:41:10 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcc51a0e27cfe040ead7b64a7c6a800c4c738b534689744bc5736c486935beb`  
		Last Modified: Wed, 11 Mar 2020 23:41:10 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f7203b7c8fc0a4e01010792bc0a916bb1d80725bd8a4e8f11428ee3160d35f`  
		Last Modified: Wed, 11 Mar 2020 23:41:07 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22af9a292df27880e2bdab8b6325e55b0ca496959f7b3cbc864addc1d08d102d`  
		Last Modified: Wed, 11 Mar 2020 23:42:15 GMT  
		Size: 455.3 MB (455252292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb17de172b016b72e14b1ad1dc7b0d91f65115cd25a7268d5758b93956a3298f`  
		Last Modified: Wed, 11 Mar 2020 23:41:07 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a4339164f7d75bf46ec45b216b30960178423acd470a8d3f7fa23bcadb1e05`  
		Last Modified: Wed, 11 Mar 2020 23:41:07 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf29d93e6248494f3397e2328ebfe14d053d0679135d2853daa7460ecf197df7`  
		Last Modified: Wed, 11 Mar 2020 23:41:08 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:windowsservercore-1809`

```console
$ docker pull mongo@sha256:d934c0075f6a09fef6cba2d002d7f37e28f70e2007cacaa1bff067a56a097e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `mongo:windowsservercore-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull mongo@sha256:aac754de81af2f5d162c77a945382332cffd5575897c7601ef472343cb844896
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2720597037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d0aaebe9da6481c2ac37ceef6336551122a88bb8c6e0f0273b2b1408c89f3a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Tue, 10 Mar 2020 23:23:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Mar 2020 23:17:35 GMT
ENV MONGO_VERSION=4.2.3
# Wed, 11 Mar 2020 23:17:36 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.3-signed.msi
# Wed, 11 Mar 2020 23:17:37 GMT
ENV MONGO_DOWNLOAD_SHA256=234f6abf9c4947df94428f6ce648905dbf6b1269f48cc3239ebd4990bde1ca2a
# Wed, 11 Mar 2020 23:37:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Mar 2020 23:37:05 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Mar 2020 23:37:08 GMT
EXPOSE 27017
# Wed, 11 Mar 2020 23:37:09 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb49f89affc2d69b541463d095fdfbe61fa62e02b0aa5fa6d26bc134fb66bf35`  
		Last Modified: Wed, 11 Mar 2020 00:30:48 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a556cdd1dac3043338300637cf3645822f875ee02355952ab1cd7751e1b68bc`  
		Last Modified: Wed, 11 Mar 2020 23:41:10 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcc51a0e27cfe040ead7b64a7c6a800c4c738b534689744bc5736c486935beb`  
		Last Modified: Wed, 11 Mar 2020 23:41:10 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f7203b7c8fc0a4e01010792bc0a916bb1d80725bd8a4e8f11428ee3160d35f`  
		Last Modified: Wed, 11 Mar 2020 23:41:07 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22af9a292df27880e2bdab8b6325e55b0ca496959f7b3cbc864addc1d08d102d`  
		Last Modified: Wed, 11 Mar 2020 23:42:15 GMT  
		Size: 455.3 MB (455252292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb17de172b016b72e14b1ad1dc7b0d91f65115cd25a7268d5758b93956a3298f`  
		Last Modified: Wed, 11 Mar 2020 23:41:07 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a4339164f7d75bf46ec45b216b30960178423acd470a8d3f7fa23bcadb1e05`  
		Last Modified: Wed, 11 Mar 2020 23:41:07 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf29d93e6248494f3397e2328ebfe14d053d0679135d2853daa7460ecf197df7`  
		Last Modified: Wed, 11 Mar 2020 23:41:08 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:252d9092a44cb76ce1978defc409db903e14ffa2b022b7a58293c4583db38a47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3506; amd64

### `mongo:windowsservercore-ltsc2016` - windows version 10.0.14393.3506; amd64

```console
$ docker pull mongo@sha256:ffcd7945296fd6bf2d492a8fbd2d76b87b4d700b617a3dbc3113ad3609dc1e99
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5823379228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b1841c6da45b9f09da659b319ee3ec76161c255d3a0299c744e58541cf1d5f`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 05:12:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 20 Feb 2020 05:31:28 GMT
ENV MONGO_VERSION=4.2.3
# Wed, 11 Mar 2020 22:59:46 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.3-signed.msi
# Wed, 11 Mar 2020 22:59:47 GMT
ENV MONGO_DOWNLOAD_SHA256=234f6abf9c4947df94428f6ce648905dbf6b1269f48cc3239ebd4990bde1ca2a
# Wed, 11 Mar 2020 23:17:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Mar 2020 23:17:16 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Mar 2020 23:17:18 GMT
EXPOSE 27017
# Wed, 11 Mar 2020 23:17:19 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:846a2223e9e7a88a2a07d706553f144d380483d72fb9f0697c4fcd71773a8693`  
		Size: 1.7 GB (1657079102 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0961c48658cd7865bcf6c05285dfbe8ad89cd52059088d7f4eed6fde1bb2b385`  
		Last Modified: Thu, 20 Feb 2020 05:18:25 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53763da721aa3ae58cd704805589abe169e1d3d28218280db0ed4045881d52cc`  
		Last Modified: Thu, 20 Feb 2020 05:44:18 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28575cbb1dce05be3e8ec069dac86a4ae8b751008d4f0c9654ea8a5adb6a05d`  
		Last Modified: Wed, 11 Mar 2020 23:40:27 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b0fd752a2977b6c56e9008cdf13c5221932c0fa7d04c8b82af7b1e365d7dcb`  
		Last Modified: Wed, 11 Mar 2020 23:40:24 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a599774a11cf582afd1c631f47ee898b2d7b7bd6c85e6a169f55999aebaf3f`  
		Last Modified: Wed, 11 Mar 2020 23:40:50 GMT  
		Size: 96.3 MB (96305864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158acd728c1a7f81dc5ab0e6ab015b47dbfe43d906b6935e6b3fb5af9ac717c9`  
		Last Modified: Wed, 11 Mar 2020 23:40:25 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1207ac339b253e1f2d5d984071f0cd6b1c14321de6258b95f05756828577ef`  
		Last Modified: Wed, 11 Mar 2020 23:40:24 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7bafe8e7fe89107a1cc111971c17ff5bfed4f23c13b7e8351d50dfedc51894`  
		Last Modified: Wed, 11 Mar 2020 23:40:24 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
