<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mongo`

-	[`mongo:3`](#mongo3)
-	[`mongo:3.4`](#mongo34)
-	[`mongo:3.4.23`](#mongo3423)
-	[`mongo:3.4.23-windowsservercore`](#mongo3423-windowsservercore)
-	[`mongo:3.4.23-windowsservercore-ltsc2016`](#mongo3423-windowsservercore-ltsc2016)
-	[`mongo:3.4.23-xenial`](#mongo3423-xenial)
-	[`mongo:3.4-windowsservercore`](#mongo34-windowsservercore)
-	[`mongo:3.4-windowsservercore-ltsc2016`](#mongo34-windowsservercore-ltsc2016)
-	[`mongo:3.4-xenial`](#mongo34-xenial)
-	[`mongo:3.6`](#mongo36)
-	[`mongo:3.6.16`](#mongo3616)
-	[`mongo:3.6.16-windowsservercore`](#mongo3616-windowsservercore)
-	[`mongo:3.6.16-windowsservercore-ltsc2016`](#mongo3616-windowsservercore-ltsc2016)
-	[`mongo:3.6.16-xenial`](#mongo3616-xenial)
-	[`mongo:3.6-windowsservercore`](#mongo36-windowsservercore)
-	[`mongo:3.6-windowsservercore-ltsc2016`](#mongo36-windowsservercore-ltsc2016)
-	[`mongo:3.6-xenial`](#mongo36-xenial)
-	[`mongo:3-windowsservercore`](#mongo3-windowsservercore)
-	[`mongo:3-windowsservercore-ltsc2016`](#mongo3-windowsservercore-ltsc2016)
-	[`mongo:3-xenial`](#mongo3-xenial)
-	[`mongo:4`](#mongo4)
-	[`mongo:4.0`](#mongo40)
-	[`mongo:4.0.13`](#mongo4013)
-	[`mongo:4.0.13-windowsservercore`](#mongo4013-windowsservercore)
-	[`mongo:4.0.13-windowsservercore-1809`](#mongo4013-windowsservercore-1809)
-	[`mongo:4.0.13-windowsservercore-ltsc2016`](#mongo4013-windowsservercore-ltsc2016)
-	[`mongo:4.0.13-xenial`](#mongo4013-xenial)
-	[`mongo:4.0-windowsservercore`](#mongo40-windowsservercore)
-	[`mongo:4.0-windowsservercore-1809`](#mongo40-windowsservercore-1809)
-	[`mongo:4.0-windowsservercore-ltsc2016`](#mongo40-windowsservercore-ltsc2016)
-	[`mongo:4.0-xenial`](#mongo40-xenial)
-	[`mongo:4.2`](#mongo42)
-	[`mongo:4.2.2`](#mongo422)
-	[`mongo:4.2.2-bionic`](#mongo422-bionic)
-	[`mongo:4.2.2-windowsservercore`](#mongo422-windowsservercore)
-	[`mongo:4.2.2-windowsservercore-1809`](#mongo422-windowsservercore-1809)
-	[`mongo:4.2.2-windowsservercore-ltsc2016`](#mongo422-windowsservercore-ltsc2016)
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
$ docker pull mongo@sha256:7b7404c9c071cab07e3978734baf1fda6c1b83ef01b9c37d101f8f0128a2f611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.14393.3384; amd64

### `mongo:3` - linux; amd64

```console
$ docker pull mongo@sha256:c18f243b3a51049e68ee82847c401222e1dbb45c740e904371a2e2a39f542c9f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.6 MB (165573298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fa64d9ee5add803bcede62a16fdff87c57b7cbc55157480caa44942ecd4a955`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 27 Nov 2019 00:22:54 GMT
ADD file:4eb02fc768cad452a37e8df30bbfcc728f3e6e7ca33af177fd4de06fd07c2098 in / 
# Wed, 27 Nov 2019 00:22:55 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 00:22:56 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 27 Nov 2019 00:22:56 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 27 Nov 2019 00:22:56 GMT
CMD ["/bin/bash"]
# Wed, 27 Nov 2019 02:02:59 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 27 Nov 2019 02:03:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 02:03:08 GMT
ENV GOSU_VERSION=1.11
# Wed, 27 Nov 2019 02:03:08 GMT
ENV JSYAML_VERSION=3.13.0
# Wed, 27 Nov 2019 02:03:19 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 27 Nov 2019 02:03:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 27 Nov 2019 02:03:52 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Wed, 27 Nov 2019 02:03:53 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 27 Nov 2019 02:03:53 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 27 Nov 2019 02:03:53 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 02:03:53 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 02:03:53 GMT
ENV MONGO_MAJOR=3.6
# Tue, 03 Dec 2019 23:26:18 GMT
ENV MONGO_VERSION=3.6.16
# Tue, 03 Dec 2019 23:26:19 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Tue, 03 Dec 2019 23:26:40 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Tue, 03 Dec 2019 23:26:41 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Tue, 03 Dec 2019 23:26:41 GMT
VOLUME [/data/db /data/configdb]
# Tue, 03 Dec 2019 23:26:41 GMT
COPY file:021686a669d0d1d1cbb99d6ca84ff8de10577b78ea985b8cdab9d75b347a3bd0 in /usr/local/bin/ 
# Tue, 03 Dec 2019 23:26:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Dec 2019 23:26:41 GMT
EXPOSE 27017
# Tue, 03 Dec 2019 23:26:42 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:976a760c94fcdd7d105269ae621e8269e7bb25a58c52ae667b4029a6bc7e33cb`  
		Last Modified: Sat, 09 Nov 2019 00:25:10 GMT  
		Size: 44.1 MB (44145376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c58992f3c37bb64aeba18910408cda9a7a63e212fe27e95065a8d54130ca5926`  
		Last Modified: Wed, 27 Nov 2019 00:23:39 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca0e5e7f12e6eb512246aea5579fcb771fe7203bc60944384d5cd7962f87ddb`  
		Last Modified: Wed, 27 Nov 2019 00:23:39 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a274cc00ca5f671b1740c43672dbc96504760cee585e7604029a3fe56854a8`  
		Last Modified: Wed, 27 Nov 2019 00:23:39 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6568107a703bb6b06323a98aa1b0b9269889582ed7bfca9784efda57e0f2e9`  
		Last Modified: Wed, 27 Nov 2019 02:05:02 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08957b2477b2c6d539baf4907363ed231b413902491c5cb985cbebe0c3ffe4dc`  
		Last Modified: Wed, 27 Nov 2019 02:05:01 GMT  
		Size: 2.9 MB (2946123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66dbd57d2a3b26381fcffa09bc1e01a2a010b2ea01432d43920927d44a8b2ac`  
		Last Modified: Wed, 27 Nov 2019 02:05:01 GMT  
		Size: 1.2 MB (1243858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135a9132a8625aee4a48702e5db9ea194db458f6109f490569fd5a85bad53b0c`  
		Last Modified: Wed, 27 Nov 2019 02:05:01 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6412ed86abd20e679cb4e72d098ef56ee0bb8ca029f85ae15d02074aa84919e`  
		Last Modified: Wed, 27 Nov 2019 02:05:22 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20a6504afb84bc25562d6f799c37e80cb6de33594c94610969bc8cabf8a01bb`  
		Last Modified: Tue, 03 Dec 2019 23:27:01 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c35ae8338e5b637ffe1eadf90ac3cf5f0649e30deee265166a258470d6a98d`  
		Last Modified: Tue, 03 Dec 2019 23:27:20 GMT  
		Size: 117.2 MB (117227921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d4094bb54473e0370e72f7720239cf79eeeed4d7101502000898201a91a99f`  
		Last Modified: Tue, 03 Dec 2019 23:27:01 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c0f43ab80060836d54f807cc28fba4e30027b595d0d23dc36ed994c8f7d50e`  
		Last Modified: Tue, 03 Dec 2019 23:27:01 GMT  
		Size: 4.0 KB (4008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:4d6093c2b1e85db9acfffcf152e936a481fac5af3a05a8d679a9fa1f9923b0b7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.0 MB (155040149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68ee79b405e7b46538372c16edc6a1549cd7e1f76907fb7070bef7ddc69937f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 26 Nov 2019 23:51:57 GMT
ADD file:2aa99efceecb520e73ba3c7dc167a4fbe6143ce5e9a6499e85dbc75935b3dfab in / 
# Tue, 26 Nov 2019 23:52:01 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 26 Nov 2019 23:52:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 26 Nov 2019 23:52:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 26 Nov 2019 23:52:06 GMT
CMD ["/bin/bash"]
# Wed, 27 Nov 2019 00:48:07 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 27 Nov 2019 00:48:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 00:48:27 GMT
ENV GOSU_VERSION=1.11
# Wed, 27 Nov 2019 00:48:28 GMT
ENV JSYAML_VERSION=3.13.0
# Wed, 27 Nov 2019 00:48:55 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 27 Nov 2019 00:48:57 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 27 Nov 2019 00:49:52 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Wed, 27 Nov 2019 00:49:55 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 27 Nov 2019 00:49:55 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 27 Nov 2019 00:49:56 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 00:49:57 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 00:49:58 GMT
ENV MONGO_MAJOR=3.6
# Tue, 03 Dec 2019 23:47:18 GMT
ENV MONGO_VERSION=3.6.16
# Tue, 03 Dec 2019 23:47:20 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Tue, 03 Dec 2019 23:47:44 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Tue, 03 Dec 2019 23:47:47 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Tue, 03 Dec 2019 23:47:47 GMT
VOLUME [/data/db /data/configdb]
# Tue, 03 Dec 2019 23:47:48 GMT
COPY file:021686a669d0d1d1cbb99d6ca84ff8de10577b78ea985b8cdab9d75b347a3bd0 in /usr/local/bin/ 
# Tue, 03 Dec 2019 23:47:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Dec 2019 23:47:49 GMT
EXPOSE 27017
# Tue, 03 Dec 2019 23:47:50 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:89276bd3590376dfedf96d27b310423c8a1d8c2fe92e4c5a2630aa704b1bb77f`  
		Last Modified: Mon, 11 Nov 2019 15:38:35 GMT  
		Size: 40.0 MB (39951577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a34d6b85b836a6bc6237d1912834f44592a792ab55d92f9ebe1d74973886c6`  
		Last Modified: Tue, 26 Nov 2019 23:52:51 GMT  
		Size: 470.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1bf847b434f33038cc426678c8640251706a59656ef4b0fec6fe3ba88854ab5`  
		Last Modified: Tue, 26 Nov 2019 23:52:51 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcbc4652a1718a263f7195a62c1ca8bf0117bcced50af01ac046bd164f523e5e`  
		Last Modified: Tue, 26 Nov 2019 23:52:51 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29654a2b453807f2a2ab77da919c90f470b457feb09082017c2db0cb659cbae8`  
		Last Modified: Wed, 27 Nov 2019 00:52:48 GMT  
		Size: 2.0 KB (2005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82801a5d252ba1ad5369119729d06933f6687427ec9b00ed3affee3d7d9e5a5b`  
		Last Modified: Wed, 27 Nov 2019 00:52:46 GMT  
		Size: 2.5 MB (2475016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32596fb594dee26ddc2fff00de483a10c3a1e9d0596d9e175424080fd13f6222`  
		Last Modified: Wed, 27 Nov 2019 00:52:46 GMT  
		Size: 1.2 MB (1170042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8df7b8db38cf122e5d4240be8c6a69443d07d574e37834d27d6a9316782df11`  
		Last Modified: Wed, 27 Nov 2019 00:52:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cebea15061d7e2a3269c663f7ecb0d5b395e1e49c409b8d064dbe5f7d6e72172`  
		Last Modified: Wed, 27 Nov 2019 00:53:25 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa2935a9205e0bef6cd51d522ccd870fe0dc3ffdea544e47c9ac26be8eb3122`  
		Last Modified: Tue, 03 Dec 2019 23:48:20 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf9e65ee1a4b2ed96c6967fb16eb0de7c63da6bce0c47e3ec63d0c9bd5a237a`  
		Last Modified: Tue, 03 Dec 2019 23:48:49 GMT  
		Size: 111.4 MB (111433459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c6a6b8b935e01daa47297ffcd098477b6928da4ffc96f92547c69d47479304f`  
		Last Modified: Tue, 03 Dec 2019 23:48:21 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27528e779b9e619704d2f2e340fa917637a6413c6f864c8864405df4245b2a2a`  
		Last Modified: Tue, 03 Dec 2019 23:48:21 GMT  
		Size: 4.0 KB (4006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3` - windows version 10.0.14393.3384; amd64

```console
$ docker pull mongo@sha256:1bdcfaae6aafbb14428a8892a23124a40f31bd9414e5d2c3b641904db525a5a8
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5816186803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23192a55795afdee48dc3b3724f1c8a7a93396e95bff38c432c3e559fb9ba27c`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 15:47:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 22:57:29 GMT
ENV MONGO_VERSION=3.6.16
# Wed, 11 Dec 2019 22:57:30 GMT
ENV MONGO_DOWNLOAD_URL=https://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.16-signed.msi
# Wed, 11 Dec 2019 22:57:32 GMT
ENV MONGO_DOWNLOAD_SHA256=06d8b235702c6a2a4f1b721bbd4b59efbc67d0b9dcd5b4d31984c75946837a2e
# Wed, 11 Dec 2019 23:06:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Dec 2019 23:06:40 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Dec 2019 23:06:42 GMT
EXPOSE 27017
# Wed, 11 Dec 2019 23:06:44 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d23dffb4f7b6ebd1cceaac955d664d79467da76c4749d2a37d98556996d8bb0a`  
		Last Modified: Wed, 11 Dec 2019 18:01:38 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628896678dbc43683e49f91e61271412aa1d97a90b65a2ed04e74157fa49532b`  
		Last Modified: Thu, 12 Dec 2019 00:05:14 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f2f11a3aaf5933be1369a1954c04a62d6f707a9e9cde397a42e567f5648e768`  
		Last Modified: Thu, 12 Dec 2019 00:05:14 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:836437d81474147d2932b37b6634ea7d129614983deba273248aae15400c3d08`  
		Last Modified: Thu, 12 Dec 2019 00:05:12 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2c1a30da870a0715c3a3c01c9ab82079b1057836d8b6591a358b85f5c6b8339`  
		Last Modified: Thu, 12 Dec 2019 00:05:41 GMT  
		Size: 93.5 MB (93474561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9ece9fda5ed7b5d814b85fdc19ec1154ec7939bc68330c399127bd4e855024`  
		Last Modified: Thu, 12 Dec 2019 00:05:12 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d3ecfc5eca20e232501e1be3e7bcd29af0358074cbe07316e39ff04be2c224`  
		Last Modified: Thu, 12 Dec 2019 00:05:12 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2833f1058a943a474d0b1fb420d65ba0c50b5b30e8edf26032ec538ed6360beb`  
		Last Modified: Thu, 12 Dec 2019 00:05:12 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.4`

```console
$ docker pull mongo@sha256:4c7003e140fc7dce5f12817d510b5a9bd265f2c3bbd6f81d50a60cc11f6395d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.14393.3384; amd64

### `mongo:3.4` - linux; amd64

```console
$ docker pull mongo@sha256:88d46977d6298f69374422a2405000ea34c7f7046b661bc8fe81b4899105835e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.0 MB (168036392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e5bdbd0995dea8998d475d950eb68cbe78db2c23f9c6cd682c87011b1c5d34f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 27 Nov 2019 00:22:54 GMT
ADD file:4eb02fc768cad452a37e8df30bbfcc728f3e6e7ca33af177fd4de06fd07c2098 in / 
# Wed, 27 Nov 2019 00:22:55 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 00:22:56 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 27 Nov 2019 00:22:56 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 27 Nov 2019 00:22:56 GMT
CMD ["/bin/bash"]
# Wed, 27 Nov 2019 02:02:59 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 27 Nov 2019 02:03:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 02:03:08 GMT
ENV GOSU_VERSION=1.11
# Wed, 27 Nov 2019 02:03:08 GMT
ENV JSYAML_VERSION=3.13.0
# Wed, 27 Nov 2019 02:03:19 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 27 Nov 2019 02:03:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 27 Nov 2019 02:03:20 GMT
ENV GPG_KEYS=0C49F3730359A14518585931BC711F9BA15703C6
# Wed, 27 Nov 2019 02:03:21 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 27 Nov 2019 02:03:21 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 27 Nov 2019 02:03:21 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 02:03:21 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 02:03:21 GMT
ENV MONGO_MAJOR=3.4
# Wed, 27 Nov 2019 02:03:22 GMT
ENV MONGO_VERSION=3.4.23
# Wed, 27 Nov 2019 02:03:22 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 27 Nov 2019 02:03:40 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 27 Nov 2019 02:03:41 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 27 Nov 2019 02:03:41 GMT
VOLUME [/data/db /data/configdb]
# Wed, 27 Nov 2019 02:03:41 GMT
COPY file:021686a669d0d1d1cbb99d6ca84ff8de10577b78ea985b8cdab9d75b347a3bd0 in /usr/local/bin/ 
# Wed, 27 Nov 2019 02:03:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat (3.4)
# Wed, 27 Nov 2019 02:03:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2019 02:03:42 GMT
EXPOSE 27017
# Wed, 27 Nov 2019 02:03:42 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:976a760c94fcdd7d105269ae621e8269e7bb25a58c52ae667b4029a6bc7e33cb`  
		Last Modified: Sat, 09 Nov 2019 00:25:10 GMT  
		Size: 44.1 MB (44145376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c58992f3c37bb64aeba18910408cda9a7a63e212fe27e95065a8d54130ca5926`  
		Last Modified: Wed, 27 Nov 2019 00:23:39 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca0e5e7f12e6eb512246aea5579fcb771fe7203bc60944384d5cd7962f87ddb`  
		Last Modified: Wed, 27 Nov 2019 00:23:39 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a274cc00ca5f671b1740c43672dbc96504760cee585e7604029a3fe56854a8`  
		Last Modified: Wed, 27 Nov 2019 00:23:39 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6568107a703bb6b06323a98aa1b0b9269889582ed7bfca9784efda57e0f2e9`  
		Last Modified: Wed, 27 Nov 2019 02:05:02 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08957b2477b2c6d539baf4907363ed231b413902491c5cb985cbebe0c3ffe4dc`  
		Last Modified: Wed, 27 Nov 2019 02:05:01 GMT  
		Size: 2.9 MB (2946123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66dbd57d2a3b26381fcffa09bc1e01a2a010b2ea01432d43920927d44a8b2ac`  
		Last Modified: Wed, 27 Nov 2019 02:05:01 GMT  
		Size: 1.2 MB (1243858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135a9132a8625aee4a48702e5db9ea194db458f6109f490569fd5a85bad53b0c`  
		Last Modified: Wed, 27 Nov 2019 02:05:01 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c45eb8eb6ddee2a5e98dc1c47af2194ace743e316fa0273562a93d6d5efe98`  
		Last Modified: Wed, 27 Nov 2019 02:05:00 GMT  
		Size: 2.0 KB (1989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866ea801830c4c1864c47e410b972112ebb96afad39855b071903fe93b4764ac`  
		Last Modified: Wed, 27 Nov 2019 02:04:59 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782aa32daa2e0ad1b857a6d97b1f6b5509222fc564ea0348d565170dcb81ed39`  
		Last Modified: Wed, 27 Nov 2019 02:05:17 GMT  
		Size: 119.7 MB (119690901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa854ba58c1b2c5369f20306a7882fe7c8afc15bd52163a88ef76ce42f1adf41`  
		Last Modified: Wed, 27 Nov 2019 02:04:59 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38e496ab5a398fef652b4bf8a22bf76be2857c992d4e2bb2e74d7c944a6b02a2`  
		Last Modified: Wed, 27 Nov 2019 02:04:59 GMT  
		Size: 4.0 KB (4006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3757d63ce2b9f7e200d8ff434c45e12777b3d480c2eb603abeff0ffff45b5c77`  
		Last Modified: Wed, 27 Nov 2019 02:05:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3.4` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:fe85914cb2acfa4566f55e84020d0fec0928fe78278028641db565f22cbda373
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156509463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bec8fc74b4cc1dba49eedacd4bbb713ae3bd71d82f5254096bb551bf21c5e6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 26 Nov 2019 23:51:57 GMT
ADD file:2aa99efceecb520e73ba3c7dc167a4fbe6143ce5e9a6499e85dbc75935b3dfab in / 
# Tue, 26 Nov 2019 23:52:01 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 26 Nov 2019 23:52:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 26 Nov 2019 23:52:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 26 Nov 2019 23:52:06 GMT
CMD ["/bin/bash"]
# Wed, 27 Nov 2019 00:48:07 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 27 Nov 2019 00:48:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 00:48:27 GMT
ENV GOSU_VERSION=1.11
# Wed, 27 Nov 2019 00:48:28 GMT
ENV JSYAML_VERSION=3.13.0
# Wed, 27 Nov 2019 00:48:55 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 27 Nov 2019 00:48:57 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 27 Nov 2019 00:48:58 GMT
ENV GPG_KEYS=0C49F3730359A14518585931BC711F9BA15703C6
# Wed, 27 Nov 2019 00:49:00 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 27 Nov 2019 00:49:01 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 27 Nov 2019 00:49:01 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 00:49:02 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 00:49:02 GMT
ENV MONGO_MAJOR=3.4
# Wed, 27 Nov 2019 00:49:03 GMT
ENV MONGO_VERSION=3.4.23
# Wed, 27 Nov 2019 00:49:06 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 27 Nov 2019 00:49:29 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 27 Nov 2019 00:49:33 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 27 Nov 2019 00:49:34 GMT
VOLUME [/data/db /data/configdb]
# Wed, 27 Nov 2019 00:49:36 GMT
COPY file:021686a669d0d1d1cbb99d6ca84ff8de10577b78ea985b8cdab9d75b347a3bd0 in /usr/local/bin/ 
# Wed, 27 Nov 2019 00:49:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat (3.4)
# Wed, 27 Nov 2019 00:49:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2019 00:49:40 GMT
EXPOSE 27017
# Wed, 27 Nov 2019 00:49:41 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:89276bd3590376dfedf96d27b310423c8a1d8c2fe92e4c5a2630aa704b1bb77f`  
		Last Modified: Mon, 11 Nov 2019 15:38:35 GMT  
		Size: 40.0 MB (39951577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a34d6b85b836a6bc6237d1912834f44592a792ab55d92f9ebe1d74973886c6`  
		Last Modified: Tue, 26 Nov 2019 23:52:51 GMT  
		Size: 470.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1bf847b434f33038cc426678c8640251706a59656ef4b0fec6fe3ba88854ab5`  
		Last Modified: Tue, 26 Nov 2019 23:52:51 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcbc4652a1718a263f7195a62c1ca8bf0117bcced50af01ac046bd164f523e5e`  
		Last Modified: Tue, 26 Nov 2019 23:52:51 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29654a2b453807f2a2ab77da919c90f470b457feb09082017c2db0cb659cbae8`  
		Last Modified: Wed, 27 Nov 2019 00:52:48 GMT  
		Size: 2.0 KB (2005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82801a5d252ba1ad5369119729d06933f6687427ec9b00ed3affee3d7d9e5a5b`  
		Last Modified: Wed, 27 Nov 2019 00:52:46 GMT  
		Size: 2.5 MB (2475016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32596fb594dee26ddc2fff00de483a10c3a1e9d0596d9e175424080fd13f6222`  
		Last Modified: Wed, 27 Nov 2019 00:52:46 GMT  
		Size: 1.2 MB (1170042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8df7b8db38cf122e5d4240be8c6a69443d07d574e37834d27d6a9316782df11`  
		Last Modified: Wed, 27 Nov 2019 00:52:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a584ca199e1f752345b7703fa96fc8e508d6a1f9356ff1aa9760b6fe8247a8e`  
		Last Modified: Wed, 27 Nov 2019 00:52:46 GMT  
		Size: 2.0 KB (1998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aacdf9ff19e7305d7121240dfd9d1b49c56446a62c1a13dbc0ff974cf1d2fdb1`  
		Last Modified: Wed, 27 Nov 2019 00:52:44 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66c54bfa417fa777e458b4a690c984d42605c4ba2d9133b5ea4f3ed0f7883939`  
		Last Modified: Wed, 27 Nov 2019 00:53:10 GMT  
		Size: 112.9 MB (112902650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cfb71c955fb087026c7ee53b62e51bf1e734704b8d1ad6cdf23ba533e3090fe`  
		Last Modified: Wed, 27 Nov 2019 00:52:44 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:631fade05419c01f5ca14bff6ecb12a246d75dbbb7358daa79afa37a7f87d878`  
		Last Modified: Wed, 27 Nov 2019 00:52:44 GMT  
		Size: 4.0 KB (4006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20da495cf7cbbe25ed9a76a9f58c07412036412ab9fc9f9b07550cc7a62246b2`  
		Last Modified: Wed, 27 Nov 2019 00:52:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3.4` - windows version 10.0.14393.3384; amd64

```console
$ docker pull mongo@sha256:e16c4d20c606d871234bdb0646a07fed96c7c00c6d611c851990d1f03d998088
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5814790844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c474f0259ca30e23f0af22868e318fd2c390db53bbc09401d894347a029e297`
-	Default Command: `["mongod"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 15:47:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 22:54:10 GMT
ENV MONGO_VERSION=3.4.23
# Wed, 11 Dec 2019 22:54:11 GMT
ENV MONGO_DOWNLOAD_URL=https://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.4.23-signed.msi
# Wed, 11 Dec 2019 22:54:12 GMT
ENV MONGO_DOWNLOAD_SHA256=7b43467dce18599d8f0fff3fe7f4e204e08598e09ecfcaf65fc83c69791792cf
# Wed, 11 Dec 2019 22:57:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Dec 2019 22:57:10 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Dec 2019 22:57:12 GMT
EXPOSE 27017
# Wed, 11 Dec 2019 22:57:14 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d23dffb4f7b6ebd1cceaac955d664d79467da76c4749d2a37d98556996d8bb0a`  
		Last Modified: Wed, 11 Dec 2019 18:01:38 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9523a305809803867a7c8184c661ca8e07d09250d115f76a5afbfcecd86bb2`  
		Last Modified: Thu, 12 Dec 2019 00:04:23 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07a73e133029c5064cd425b52131222d21888abbf5e5f2de7cc8abdd80a1313`  
		Last Modified: Thu, 12 Dec 2019 00:04:22 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5acbd03e1cbfaea390737c6ca0a9907094bbb5877915f9dc273d2e91c7cea6d5`  
		Last Modified: Thu, 12 Dec 2019 00:04:20 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516dfd7d42b8e69b4e11e16ecc131d94667e51aff48da7e02a90d657122d2069`  
		Last Modified: Thu, 12 Dec 2019 00:04:50 GMT  
		Size: 92.1 MB (92078605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a941a3e4603ccf48c3ff03c56e6dedf804bc38b9c3b2f2afa278baeac58a95dd`  
		Last Modified: Thu, 12 Dec 2019 00:04:20 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0568cf846cc19ce9b662894d626cf207ef84597e046927350daa419118e108`  
		Last Modified: Thu, 12 Dec 2019 00:04:20 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0f659f4fe3b4d95be807483b1882efdebb26a2d88608a43b0bdc613e40f4ec`  
		Last Modified: Thu, 12 Dec 2019 00:04:20 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.4.23`

```console
$ docker pull mongo@sha256:4c7003e140fc7dce5f12817d510b5a9bd265f2c3bbd6f81d50a60cc11f6395d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.14393.3384; amd64

### `mongo:3.4.23` - linux; amd64

```console
$ docker pull mongo@sha256:88d46977d6298f69374422a2405000ea34c7f7046b661bc8fe81b4899105835e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.0 MB (168036392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e5bdbd0995dea8998d475d950eb68cbe78db2c23f9c6cd682c87011b1c5d34f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 27 Nov 2019 00:22:54 GMT
ADD file:4eb02fc768cad452a37e8df30bbfcc728f3e6e7ca33af177fd4de06fd07c2098 in / 
# Wed, 27 Nov 2019 00:22:55 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 00:22:56 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 27 Nov 2019 00:22:56 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 27 Nov 2019 00:22:56 GMT
CMD ["/bin/bash"]
# Wed, 27 Nov 2019 02:02:59 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 27 Nov 2019 02:03:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 02:03:08 GMT
ENV GOSU_VERSION=1.11
# Wed, 27 Nov 2019 02:03:08 GMT
ENV JSYAML_VERSION=3.13.0
# Wed, 27 Nov 2019 02:03:19 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 27 Nov 2019 02:03:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 27 Nov 2019 02:03:20 GMT
ENV GPG_KEYS=0C49F3730359A14518585931BC711F9BA15703C6
# Wed, 27 Nov 2019 02:03:21 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 27 Nov 2019 02:03:21 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 27 Nov 2019 02:03:21 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 02:03:21 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 02:03:21 GMT
ENV MONGO_MAJOR=3.4
# Wed, 27 Nov 2019 02:03:22 GMT
ENV MONGO_VERSION=3.4.23
# Wed, 27 Nov 2019 02:03:22 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 27 Nov 2019 02:03:40 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 27 Nov 2019 02:03:41 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 27 Nov 2019 02:03:41 GMT
VOLUME [/data/db /data/configdb]
# Wed, 27 Nov 2019 02:03:41 GMT
COPY file:021686a669d0d1d1cbb99d6ca84ff8de10577b78ea985b8cdab9d75b347a3bd0 in /usr/local/bin/ 
# Wed, 27 Nov 2019 02:03:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat (3.4)
# Wed, 27 Nov 2019 02:03:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2019 02:03:42 GMT
EXPOSE 27017
# Wed, 27 Nov 2019 02:03:42 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:976a760c94fcdd7d105269ae621e8269e7bb25a58c52ae667b4029a6bc7e33cb`  
		Last Modified: Sat, 09 Nov 2019 00:25:10 GMT  
		Size: 44.1 MB (44145376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c58992f3c37bb64aeba18910408cda9a7a63e212fe27e95065a8d54130ca5926`  
		Last Modified: Wed, 27 Nov 2019 00:23:39 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca0e5e7f12e6eb512246aea5579fcb771fe7203bc60944384d5cd7962f87ddb`  
		Last Modified: Wed, 27 Nov 2019 00:23:39 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a274cc00ca5f671b1740c43672dbc96504760cee585e7604029a3fe56854a8`  
		Last Modified: Wed, 27 Nov 2019 00:23:39 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6568107a703bb6b06323a98aa1b0b9269889582ed7bfca9784efda57e0f2e9`  
		Last Modified: Wed, 27 Nov 2019 02:05:02 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08957b2477b2c6d539baf4907363ed231b413902491c5cb985cbebe0c3ffe4dc`  
		Last Modified: Wed, 27 Nov 2019 02:05:01 GMT  
		Size: 2.9 MB (2946123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66dbd57d2a3b26381fcffa09bc1e01a2a010b2ea01432d43920927d44a8b2ac`  
		Last Modified: Wed, 27 Nov 2019 02:05:01 GMT  
		Size: 1.2 MB (1243858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135a9132a8625aee4a48702e5db9ea194db458f6109f490569fd5a85bad53b0c`  
		Last Modified: Wed, 27 Nov 2019 02:05:01 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c45eb8eb6ddee2a5e98dc1c47af2194ace743e316fa0273562a93d6d5efe98`  
		Last Modified: Wed, 27 Nov 2019 02:05:00 GMT  
		Size: 2.0 KB (1989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866ea801830c4c1864c47e410b972112ebb96afad39855b071903fe93b4764ac`  
		Last Modified: Wed, 27 Nov 2019 02:04:59 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782aa32daa2e0ad1b857a6d97b1f6b5509222fc564ea0348d565170dcb81ed39`  
		Last Modified: Wed, 27 Nov 2019 02:05:17 GMT  
		Size: 119.7 MB (119690901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa854ba58c1b2c5369f20306a7882fe7c8afc15bd52163a88ef76ce42f1adf41`  
		Last Modified: Wed, 27 Nov 2019 02:04:59 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38e496ab5a398fef652b4bf8a22bf76be2857c992d4e2bb2e74d7c944a6b02a2`  
		Last Modified: Wed, 27 Nov 2019 02:04:59 GMT  
		Size: 4.0 KB (4006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3757d63ce2b9f7e200d8ff434c45e12777b3d480c2eb603abeff0ffff45b5c77`  
		Last Modified: Wed, 27 Nov 2019 02:05:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3.4.23` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:fe85914cb2acfa4566f55e84020d0fec0928fe78278028641db565f22cbda373
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156509463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bec8fc74b4cc1dba49eedacd4bbb713ae3bd71d82f5254096bb551bf21c5e6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 26 Nov 2019 23:51:57 GMT
ADD file:2aa99efceecb520e73ba3c7dc167a4fbe6143ce5e9a6499e85dbc75935b3dfab in / 
# Tue, 26 Nov 2019 23:52:01 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 26 Nov 2019 23:52:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 26 Nov 2019 23:52:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 26 Nov 2019 23:52:06 GMT
CMD ["/bin/bash"]
# Wed, 27 Nov 2019 00:48:07 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 27 Nov 2019 00:48:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 00:48:27 GMT
ENV GOSU_VERSION=1.11
# Wed, 27 Nov 2019 00:48:28 GMT
ENV JSYAML_VERSION=3.13.0
# Wed, 27 Nov 2019 00:48:55 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 27 Nov 2019 00:48:57 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 27 Nov 2019 00:48:58 GMT
ENV GPG_KEYS=0C49F3730359A14518585931BC711F9BA15703C6
# Wed, 27 Nov 2019 00:49:00 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 27 Nov 2019 00:49:01 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 27 Nov 2019 00:49:01 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 00:49:02 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 00:49:02 GMT
ENV MONGO_MAJOR=3.4
# Wed, 27 Nov 2019 00:49:03 GMT
ENV MONGO_VERSION=3.4.23
# Wed, 27 Nov 2019 00:49:06 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 27 Nov 2019 00:49:29 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 27 Nov 2019 00:49:33 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 27 Nov 2019 00:49:34 GMT
VOLUME [/data/db /data/configdb]
# Wed, 27 Nov 2019 00:49:36 GMT
COPY file:021686a669d0d1d1cbb99d6ca84ff8de10577b78ea985b8cdab9d75b347a3bd0 in /usr/local/bin/ 
# Wed, 27 Nov 2019 00:49:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat (3.4)
# Wed, 27 Nov 2019 00:49:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2019 00:49:40 GMT
EXPOSE 27017
# Wed, 27 Nov 2019 00:49:41 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:89276bd3590376dfedf96d27b310423c8a1d8c2fe92e4c5a2630aa704b1bb77f`  
		Last Modified: Mon, 11 Nov 2019 15:38:35 GMT  
		Size: 40.0 MB (39951577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a34d6b85b836a6bc6237d1912834f44592a792ab55d92f9ebe1d74973886c6`  
		Last Modified: Tue, 26 Nov 2019 23:52:51 GMT  
		Size: 470.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1bf847b434f33038cc426678c8640251706a59656ef4b0fec6fe3ba88854ab5`  
		Last Modified: Tue, 26 Nov 2019 23:52:51 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcbc4652a1718a263f7195a62c1ca8bf0117bcced50af01ac046bd164f523e5e`  
		Last Modified: Tue, 26 Nov 2019 23:52:51 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29654a2b453807f2a2ab77da919c90f470b457feb09082017c2db0cb659cbae8`  
		Last Modified: Wed, 27 Nov 2019 00:52:48 GMT  
		Size: 2.0 KB (2005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82801a5d252ba1ad5369119729d06933f6687427ec9b00ed3affee3d7d9e5a5b`  
		Last Modified: Wed, 27 Nov 2019 00:52:46 GMT  
		Size: 2.5 MB (2475016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32596fb594dee26ddc2fff00de483a10c3a1e9d0596d9e175424080fd13f6222`  
		Last Modified: Wed, 27 Nov 2019 00:52:46 GMT  
		Size: 1.2 MB (1170042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8df7b8db38cf122e5d4240be8c6a69443d07d574e37834d27d6a9316782df11`  
		Last Modified: Wed, 27 Nov 2019 00:52:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a584ca199e1f752345b7703fa96fc8e508d6a1f9356ff1aa9760b6fe8247a8e`  
		Last Modified: Wed, 27 Nov 2019 00:52:46 GMT  
		Size: 2.0 KB (1998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aacdf9ff19e7305d7121240dfd9d1b49c56446a62c1a13dbc0ff974cf1d2fdb1`  
		Last Modified: Wed, 27 Nov 2019 00:52:44 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66c54bfa417fa777e458b4a690c984d42605c4ba2d9133b5ea4f3ed0f7883939`  
		Last Modified: Wed, 27 Nov 2019 00:53:10 GMT  
		Size: 112.9 MB (112902650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cfb71c955fb087026c7ee53b62e51bf1e734704b8d1ad6cdf23ba533e3090fe`  
		Last Modified: Wed, 27 Nov 2019 00:52:44 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:631fade05419c01f5ca14bff6ecb12a246d75dbbb7358daa79afa37a7f87d878`  
		Last Modified: Wed, 27 Nov 2019 00:52:44 GMT  
		Size: 4.0 KB (4006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20da495cf7cbbe25ed9a76a9f58c07412036412ab9fc9f9b07550cc7a62246b2`  
		Last Modified: Wed, 27 Nov 2019 00:52:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3.4.23` - windows version 10.0.14393.3384; amd64

```console
$ docker pull mongo@sha256:e16c4d20c606d871234bdb0646a07fed96c7c00c6d611c851990d1f03d998088
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5814790844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c474f0259ca30e23f0af22868e318fd2c390db53bbc09401d894347a029e297`
-	Default Command: `["mongod"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 15:47:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 22:54:10 GMT
ENV MONGO_VERSION=3.4.23
# Wed, 11 Dec 2019 22:54:11 GMT
ENV MONGO_DOWNLOAD_URL=https://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.4.23-signed.msi
# Wed, 11 Dec 2019 22:54:12 GMT
ENV MONGO_DOWNLOAD_SHA256=7b43467dce18599d8f0fff3fe7f4e204e08598e09ecfcaf65fc83c69791792cf
# Wed, 11 Dec 2019 22:57:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Dec 2019 22:57:10 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Dec 2019 22:57:12 GMT
EXPOSE 27017
# Wed, 11 Dec 2019 22:57:14 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d23dffb4f7b6ebd1cceaac955d664d79467da76c4749d2a37d98556996d8bb0a`  
		Last Modified: Wed, 11 Dec 2019 18:01:38 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9523a305809803867a7c8184c661ca8e07d09250d115f76a5afbfcecd86bb2`  
		Last Modified: Thu, 12 Dec 2019 00:04:23 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07a73e133029c5064cd425b52131222d21888abbf5e5f2de7cc8abdd80a1313`  
		Last Modified: Thu, 12 Dec 2019 00:04:22 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5acbd03e1cbfaea390737c6ca0a9907094bbb5877915f9dc273d2e91c7cea6d5`  
		Last Modified: Thu, 12 Dec 2019 00:04:20 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516dfd7d42b8e69b4e11e16ecc131d94667e51aff48da7e02a90d657122d2069`  
		Last Modified: Thu, 12 Dec 2019 00:04:50 GMT  
		Size: 92.1 MB (92078605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a941a3e4603ccf48c3ff03c56e6dedf804bc38b9c3b2f2afa278baeac58a95dd`  
		Last Modified: Thu, 12 Dec 2019 00:04:20 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0568cf846cc19ce9b662894d626cf207ef84597e046927350daa419118e108`  
		Last Modified: Thu, 12 Dec 2019 00:04:20 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0f659f4fe3b4d95be807483b1882efdebb26a2d88608a43b0bdc613e40f4ec`  
		Last Modified: Thu, 12 Dec 2019 00:04:20 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.4.23-windowsservercore`

```console
$ docker pull mongo@sha256:db0fc781466d6c1630b0207c7a1d72c8c47c7a169c2fdc55dfb5637f078e0c1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3384; amd64

### `mongo:3.4.23-windowsservercore` - windows version 10.0.14393.3384; amd64

```console
$ docker pull mongo@sha256:e16c4d20c606d871234bdb0646a07fed96c7c00c6d611c851990d1f03d998088
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5814790844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c474f0259ca30e23f0af22868e318fd2c390db53bbc09401d894347a029e297`
-	Default Command: `["mongod"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 15:47:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 22:54:10 GMT
ENV MONGO_VERSION=3.4.23
# Wed, 11 Dec 2019 22:54:11 GMT
ENV MONGO_DOWNLOAD_URL=https://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.4.23-signed.msi
# Wed, 11 Dec 2019 22:54:12 GMT
ENV MONGO_DOWNLOAD_SHA256=7b43467dce18599d8f0fff3fe7f4e204e08598e09ecfcaf65fc83c69791792cf
# Wed, 11 Dec 2019 22:57:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Dec 2019 22:57:10 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Dec 2019 22:57:12 GMT
EXPOSE 27017
# Wed, 11 Dec 2019 22:57:14 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d23dffb4f7b6ebd1cceaac955d664d79467da76c4749d2a37d98556996d8bb0a`  
		Last Modified: Wed, 11 Dec 2019 18:01:38 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9523a305809803867a7c8184c661ca8e07d09250d115f76a5afbfcecd86bb2`  
		Last Modified: Thu, 12 Dec 2019 00:04:23 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07a73e133029c5064cd425b52131222d21888abbf5e5f2de7cc8abdd80a1313`  
		Last Modified: Thu, 12 Dec 2019 00:04:22 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5acbd03e1cbfaea390737c6ca0a9907094bbb5877915f9dc273d2e91c7cea6d5`  
		Last Modified: Thu, 12 Dec 2019 00:04:20 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516dfd7d42b8e69b4e11e16ecc131d94667e51aff48da7e02a90d657122d2069`  
		Last Modified: Thu, 12 Dec 2019 00:04:50 GMT  
		Size: 92.1 MB (92078605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a941a3e4603ccf48c3ff03c56e6dedf804bc38b9c3b2f2afa278baeac58a95dd`  
		Last Modified: Thu, 12 Dec 2019 00:04:20 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0568cf846cc19ce9b662894d626cf207ef84597e046927350daa419118e108`  
		Last Modified: Thu, 12 Dec 2019 00:04:20 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0f659f4fe3b4d95be807483b1882efdebb26a2d88608a43b0bdc613e40f4ec`  
		Last Modified: Thu, 12 Dec 2019 00:04:20 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.4.23-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:db0fc781466d6c1630b0207c7a1d72c8c47c7a169c2fdc55dfb5637f078e0c1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3384; amd64

### `mongo:3.4.23-windowsservercore-ltsc2016` - windows version 10.0.14393.3384; amd64

```console
$ docker pull mongo@sha256:e16c4d20c606d871234bdb0646a07fed96c7c00c6d611c851990d1f03d998088
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5814790844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c474f0259ca30e23f0af22868e318fd2c390db53bbc09401d894347a029e297`
-	Default Command: `["mongod"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 15:47:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 22:54:10 GMT
ENV MONGO_VERSION=3.4.23
# Wed, 11 Dec 2019 22:54:11 GMT
ENV MONGO_DOWNLOAD_URL=https://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.4.23-signed.msi
# Wed, 11 Dec 2019 22:54:12 GMT
ENV MONGO_DOWNLOAD_SHA256=7b43467dce18599d8f0fff3fe7f4e204e08598e09ecfcaf65fc83c69791792cf
# Wed, 11 Dec 2019 22:57:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Dec 2019 22:57:10 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Dec 2019 22:57:12 GMT
EXPOSE 27017
# Wed, 11 Dec 2019 22:57:14 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d23dffb4f7b6ebd1cceaac955d664d79467da76c4749d2a37d98556996d8bb0a`  
		Last Modified: Wed, 11 Dec 2019 18:01:38 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9523a305809803867a7c8184c661ca8e07d09250d115f76a5afbfcecd86bb2`  
		Last Modified: Thu, 12 Dec 2019 00:04:23 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07a73e133029c5064cd425b52131222d21888abbf5e5f2de7cc8abdd80a1313`  
		Last Modified: Thu, 12 Dec 2019 00:04:22 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5acbd03e1cbfaea390737c6ca0a9907094bbb5877915f9dc273d2e91c7cea6d5`  
		Last Modified: Thu, 12 Dec 2019 00:04:20 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516dfd7d42b8e69b4e11e16ecc131d94667e51aff48da7e02a90d657122d2069`  
		Last Modified: Thu, 12 Dec 2019 00:04:50 GMT  
		Size: 92.1 MB (92078605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a941a3e4603ccf48c3ff03c56e6dedf804bc38b9c3b2f2afa278baeac58a95dd`  
		Last Modified: Thu, 12 Dec 2019 00:04:20 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0568cf846cc19ce9b662894d626cf207ef84597e046927350daa419118e108`  
		Last Modified: Thu, 12 Dec 2019 00:04:20 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0f659f4fe3b4d95be807483b1882efdebb26a2d88608a43b0bdc613e40f4ec`  
		Last Modified: Thu, 12 Dec 2019 00:04:20 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.4.23-xenial`

```console
$ docker pull mongo@sha256:2fb5ed8995ae8c98a01a2faf4289c35b086a3ed4273d1bef99966868d61a58dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:3.4.23-xenial` - linux; amd64

```console
$ docker pull mongo@sha256:88d46977d6298f69374422a2405000ea34c7f7046b661bc8fe81b4899105835e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.0 MB (168036392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e5bdbd0995dea8998d475d950eb68cbe78db2c23f9c6cd682c87011b1c5d34f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 27 Nov 2019 00:22:54 GMT
ADD file:4eb02fc768cad452a37e8df30bbfcc728f3e6e7ca33af177fd4de06fd07c2098 in / 
# Wed, 27 Nov 2019 00:22:55 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 00:22:56 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 27 Nov 2019 00:22:56 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 27 Nov 2019 00:22:56 GMT
CMD ["/bin/bash"]
# Wed, 27 Nov 2019 02:02:59 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 27 Nov 2019 02:03:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 02:03:08 GMT
ENV GOSU_VERSION=1.11
# Wed, 27 Nov 2019 02:03:08 GMT
ENV JSYAML_VERSION=3.13.0
# Wed, 27 Nov 2019 02:03:19 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 27 Nov 2019 02:03:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 27 Nov 2019 02:03:20 GMT
ENV GPG_KEYS=0C49F3730359A14518585931BC711F9BA15703C6
# Wed, 27 Nov 2019 02:03:21 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 27 Nov 2019 02:03:21 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 27 Nov 2019 02:03:21 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 02:03:21 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 02:03:21 GMT
ENV MONGO_MAJOR=3.4
# Wed, 27 Nov 2019 02:03:22 GMT
ENV MONGO_VERSION=3.4.23
# Wed, 27 Nov 2019 02:03:22 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 27 Nov 2019 02:03:40 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 27 Nov 2019 02:03:41 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 27 Nov 2019 02:03:41 GMT
VOLUME [/data/db /data/configdb]
# Wed, 27 Nov 2019 02:03:41 GMT
COPY file:021686a669d0d1d1cbb99d6ca84ff8de10577b78ea985b8cdab9d75b347a3bd0 in /usr/local/bin/ 
# Wed, 27 Nov 2019 02:03:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat (3.4)
# Wed, 27 Nov 2019 02:03:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2019 02:03:42 GMT
EXPOSE 27017
# Wed, 27 Nov 2019 02:03:42 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:976a760c94fcdd7d105269ae621e8269e7bb25a58c52ae667b4029a6bc7e33cb`  
		Last Modified: Sat, 09 Nov 2019 00:25:10 GMT  
		Size: 44.1 MB (44145376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c58992f3c37bb64aeba18910408cda9a7a63e212fe27e95065a8d54130ca5926`  
		Last Modified: Wed, 27 Nov 2019 00:23:39 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca0e5e7f12e6eb512246aea5579fcb771fe7203bc60944384d5cd7962f87ddb`  
		Last Modified: Wed, 27 Nov 2019 00:23:39 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a274cc00ca5f671b1740c43672dbc96504760cee585e7604029a3fe56854a8`  
		Last Modified: Wed, 27 Nov 2019 00:23:39 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6568107a703bb6b06323a98aa1b0b9269889582ed7bfca9784efda57e0f2e9`  
		Last Modified: Wed, 27 Nov 2019 02:05:02 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08957b2477b2c6d539baf4907363ed231b413902491c5cb985cbebe0c3ffe4dc`  
		Last Modified: Wed, 27 Nov 2019 02:05:01 GMT  
		Size: 2.9 MB (2946123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66dbd57d2a3b26381fcffa09bc1e01a2a010b2ea01432d43920927d44a8b2ac`  
		Last Modified: Wed, 27 Nov 2019 02:05:01 GMT  
		Size: 1.2 MB (1243858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135a9132a8625aee4a48702e5db9ea194db458f6109f490569fd5a85bad53b0c`  
		Last Modified: Wed, 27 Nov 2019 02:05:01 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c45eb8eb6ddee2a5e98dc1c47af2194ace743e316fa0273562a93d6d5efe98`  
		Last Modified: Wed, 27 Nov 2019 02:05:00 GMT  
		Size: 2.0 KB (1989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866ea801830c4c1864c47e410b972112ebb96afad39855b071903fe93b4764ac`  
		Last Modified: Wed, 27 Nov 2019 02:04:59 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782aa32daa2e0ad1b857a6d97b1f6b5509222fc564ea0348d565170dcb81ed39`  
		Last Modified: Wed, 27 Nov 2019 02:05:17 GMT  
		Size: 119.7 MB (119690901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa854ba58c1b2c5369f20306a7882fe7c8afc15bd52163a88ef76ce42f1adf41`  
		Last Modified: Wed, 27 Nov 2019 02:04:59 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38e496ab5a398fef652b4bf8a22bf76be2857c992d4e2bb2e74d7c944a6b02a2`  
		Last Modified: Wed, 27 Nov 2019 02:04:59 GMT  
		Size: 4.0 KB (4006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3757d63ce2b9f7e200d8ff434c45e12777b3d480c2eb603abeff0ffff45b5c77`  
		Last Modified: Wed, 27 Nov 2019 02:05:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3.4.23-xenial` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:fe85914cb2acfa4566f55e84020d0fec0928fe78278028641db565f22cbda373
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156509463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bec8fc74b4cc1dba49eedacd4bbb713ae3bd71d82f5254096bb551bf21c5e6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 26 Nov 2019 23:51:57 GMT
ADD file:2aa99efceecb520e73ba3c7dc167a4fbe6143ce5e9a6499e85dbc75935b3dfab in / 
# Tue, 26 Nov 2019 23:52:01 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 26 Nov 2019 23:52:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 26 Nov 2019 23:52:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 26 Nov 2019 23:52:06 GMT
CMD ["/bin/bash"]
# Wed, 27 Nov 2019 00:48:07 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 27 Nov 2019 00:48:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 00:48:27 GMT
ENV GOSU_VERSION=1.11
# Wed, 27 Nov 2019 00:48:28 GMT
ENV JSYAML_VERSION=3.13.0
# Wed, 27 Nov 2019 00:48:55 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 27 Nov 2019 00:48:57 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 27 Nov 2019 00:48:58 GMT
ENV GPG_KEYS=0C49F3730359A14518585931BC711F9BA15703C6
# Wed, 27 Nov 2019 00:49:00 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 27 Nov 2019 00:49:01 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 27 Nov 2019 00:49:01 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 00:49:02 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 00:49:02 GMT
ENV MONGO_MAJOR=3.4
# Wed, 27 Nov 2019 00:49:03 GMT
ENV MONGO_VERSION=3.4.23
# Wed, 27 Nov 2019 00:49:06 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 27 Nov 2019 00:49:29 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 27 Nov 2019 00:49:33 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 27 Nov 2019 00:49:34 GMT
VOLUME [/data/db /data/configdb]
# Wed, 27 Nov 2019 00:49:36 GMT
COPY file:021686a669d0d1d1cbb99d6ca84ff8de10577b78ea985b8cdab9d75b347a3bd0 in /usr/local/bin/ 
# Wed, 27 Nov 2019 00:49:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat (3.4)
# Wed, 27 Nov 2019 00:49:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2019 00:49:40 GMT
EXPOSE 27017
# Wed, 27 Nov 2019 00:49:41 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:89276bd3590376dfedf96d27b310423c8a1d8c2fe92e4c5a2630aa704b1bb77f`  
		Last Modified: Mon, 11 Nov 2019 15:38:35 GMT  
		Size: 40.0 MB (39951577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a34d6b85b836a6bc6237d1912834f44592a792ab55d92f9ebe1d74973886c6`  
		Last Modified: Tue, 26 Nov 2019 23:52:51 GMT  
		Size: 470.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1bf847b434f33038cc426678c8640251706a59656ef4b0fec6fe3ba88854ab5`  
		Last Modified: Tue, 26 Nov 2019 23:52:51 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcbc4652a1718a263f7195a62c1ca8bf0117bcced50af01ac046bd164f523e5e`  
		Last Modified: Tue, 26 Nov 2019 23:52:51 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29654a2b453807f2a2ab77da919c90f470b457feb09082017c2db0cb659cbae8`  
		Last Modified: Wed, 27 Nov 2019 00:52:48 GMT  
		Size: 2.0 KB (2005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82801a5d252ba1ad5369119729d06933f6687427ec9b00ed3affee3d7d9e5a5b`  
		Last Modified: Wed, 27 Nov 2019 00:52:46 GMT  
		Size: 2.5 MB (2475016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32596fb594dee26ddc2fff00de483a10c3a1e9d0596d9e175424080fd13f6222`  
		Last Modified: Wed, 27 Nov 2019 00:52:46 GMT  
		Size: 1.2 MB (1170042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8df7b8db38cf122e5d4240be8c6a69443d07d574e37834d27d6a9316782df11`  
		Last Modified: Wed, 27 Nov 2019 00:52:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a584ca199e1f752345b7703fa96fc8e508d6a1f9356ff1aa9760b6fe8247a8e`  
		Last Modified: Wed, 27 Nov 2019 00:52:46 GMT  
		Size: 2.0 KB (1998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aacdf9ff19e7305d7121240dfd9d1b49c56446a62c1a13dbc0ff974cf1d2fdb1`  
		Last Modified: Wed, 27 Nov 2019 00:52:44 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66c54bfa417fa777e458b4a690c984d42605c4ba2d9133b5ea4f3ed0f7883939`  
		Last Modified: Wed, 27 Nov 2019 00:53:10 GMT  
		Size: 112.9 MB (112902650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cfb71c955fb087026c7ee53b62e51bf1e734704b8d1ad6cdf23ba533e3090fe`  
		Last Modified: Wed, 27 Nov 2019 00:52:44 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:631fade05419c01f5ca14bff6ecb12a246d75dbbb7358daa79afa37a7f87d878`  
		Last Modified: Wed, 27 Nov 2019 00:52:44 GMT  
		Size: 4.0 KB (4006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20da495cf7cbbe25ed9a76a9f58c07412036412ab9fc9f9b07550cc7a62246b2`  
		Last Modified: Wed, 27 Nov 2019 00:52:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.4-windowsservercore`

```console
$ docker pull mongo@sha256:db0fc781466d6c1630b0207c7a1d72c8c47c7a169c2fdc55dfb5637f078e0c1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3384; amd64

### `mongo:3.4-windowsservercore` - windows version 10.0.14393.3384; amd64

```console
$ docker pull mongo@sha256:e16c4d20c606d871234bdb0646a07fed96c7c00c6d611c851990d1f03d998088
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5814790844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c474f0259ca30e23f0af22868e318fd2c390db53bbc09401d894347a029e297`
-	Default Command: `["mongod"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 15:47:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 22:54:10 GMT
ENV MONGO_VERSION=3.4.23
# Wed, 11 Dec 2019 22:54:11 GMT
ENV MONGO_DOWNLOAD_URL=https://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.4.23-signed.msi
# Wed, 11 Dec 2019 22:54:12 GMT
ENV MONGO_DOWNLOAD_SHA256=7b43467dce18599d8f0fff3fe7f4e204e08598e09ecfcaf65fc83c69791792cf
# Wed, 11 Dec 2019 22:57:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Dec 2019 22:57:10 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Dec 2019 22:57:12 GMT
EXPOSE 27017
# Wed, 11 Dec 2019 22:57:14 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d23dffb4f7b6ebd1cceaac955d664d79467da76c4749d2a37d98556996d8bb0a`  
		Last Modified: Wed, 11 Dec 2019 18:01:38 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9523a305809803867a7c8184c661ca8e07d09250d115f76a5afbfcecd86bb2`  
		Last Modified: Thu, 12 Dec 2019 00:04:23 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07a73e133029c5064cd425b52131222d21888abbf5e5f2de7cc8abdd80a1313`  
		Last Modified: Thu, 12 Dec 2019 00:04:22 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5acbd03e1cbfaea390737c6ca0a9907094bbb5877915f9dc273d2e91c7cea6d5`  
		Last Modified: Thu, 12 Dec 2019 00:04:20 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516dfd7d42b8e69b4e11e16ecc131d94667e51aff48da7e02a90d657122d2069`  
		Last Modified: Thu, 12 Dec 2019 00:04:50 GMT  
		Size: 92.1 MB (92078605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a941a3e4603ccf48c3ff03c56e6dedf804bc38b9c3b2f2afa278baeac58a95dd`  
		Last Modified: Thu, 12 Dec 2019 00:04:20 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0568cf846cc19ce9b662894d626cf207ef84597e046927350daa419118e108`  
		Last Modified: Thu, 12 Dec 2019 00:04:20 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0f659f4fe3b4d95be807483b1882efdebb26a2d88608a43b0bdc613e40f4ec`  
		Last Modified: Thu, 12 Dec 2019 00:04:20 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.4-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:db0fc781466d6c1630b0207c7a1d72c8c47c7a169c2fdc55dfb5637f078e0c1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3384; amd64

### `mongo:3.4-windowsservercore-ltsc2016` - windows version 10.0.14393.3384; amd64

```console
$ docker pull mongo@sha256:e16c4d20c606d871234bdb0646a07fed96c7c00c6d611c851990d1f03d998088
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5814790844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c474f0259ca30e23f0af22868e318fd2c390db53bbc09401d894347a029e297`
-	Default Command: `["mongod"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 15:47:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 22:54:10 GMT
ENV MONGO_VERSION=3.4.23
# Wed, 11 Dec 2019 22:54:11 GMT
ENV MONGO_DOWNLOAD_URL=https://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.4.23-signed.msi
# Wed, 11 Dec 2019 22:54:12 GMT
ENV MONGO_DOWNLOAD_SHA256=7b43467dce18599d8f0fff3fe7f4e204e08598e09ecfcaf65fc83c69791792cf
# Wed, 11 Dec 2019 22:57:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Dec 2019 22:57:10 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Dec 2019 22:57:12 GMT
EXPOSE 27017
# Wed, 11 Dec 2019 22:57:14 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d23dffb4f7b6ebd1cceaac955d664d79467da76c4749d2a37d98556996d8bb0a`  
		Last Modified: Wed, 11 Dec 2019 18:01:38 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9523a305809803867a7c8184c661ca8e07d09250d115f76a5afbfcecd86bb2`  
		Last Modified: Thu, 12 Dec 2019 00:04:23 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07a73e133029c5064cd425b52131222d21888abbf5e5f2de7cc8abdd80a1313`  
		Last Modified: Thu, 12 Dec 2019 00:04:22 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5acbd03e1cbfaea390737c6ca0a9907094bbb5877915f9dc273d2e91c7cea6d5`  
		Last Modified: Thu, 12 Dec 2019 00:04:20 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516dfd7d42b8e69b4e11e16ecc131d94667e51aff48da7e02a90d657122d2069`  
		Last Modified: Thu, 12 Dec 2019 00:04:50 GMT  
		Size: 92.1 MB (92078605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a941a3e4603ccf48c3ff03c56e6dedf804bc38b9c3b2f2afa278baeac58a95dd`  
		Last Modified: Thu, 12 Dec 2019 00:04:20 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0568cf846cc19ce9b662894d626cf207ef84597e046927350daa419118e108`  
		Last Modified: Thu, 12 Dec 2019 00:04:20 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0f659f4fe3b4d95be807483b1882efdebb26a2d88608a43b0bdc613e40f4ec`  
		Last Modified: Thu, 12 Dec 2019 00:04:20 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.4-xenial`

```console
$ docker pull mongo@sha256:2fb5ed8995ae8c98a01a2faf4289c35b086a3ed4273d1bef99966868d61a58dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:3.4-xenial` - linux; amd64

```console
$ docker pull mongo@sha256:88d46977d6298f69374422a2405000ea34c7f7046b661bc8fe81b4899105835e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.0 MB (168036392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e5bdbd0995dea8998d475d950eb68cbe78db2c23f9c6cd682c87011b1c5d34f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 27 Nov 2019 00:22:54 GMT
ADD file:4eb02fc768cad452a37e8df30bbfcc728f3e6e7ca33af177fd4de06fd07c2098 in / 
# Wed, 27 Nov 2019 00:22:55 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 00:22:56 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 27 Nov 2019 00:22:56 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 27 Nov 2019 00:22:56 GMT
CMD ["/bin/bash"]
# Wed, 27 Nov 2019 02:02:59 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 27 Nov 2019 02:03:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 02:03:08 GMT
ENV GOSU_VERSION=1.11
# Wed, 27 Nov 2019 02:03:08 GMT
ENV JSYAML_VERSION=3.13.0
# Wed, 27 Nov 2019 02:03:19 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 27 Nov 2019 02:03:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 27 Nov 2019 02:03:20 GMT
ENV GPG_KEYS=0C49F3730359A14518585931BC711F9BA15703C6
# Wed, 27 Nov 2019 02:03:21 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 27 Nov 2019 02:03:21 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 27 Nov 2019 02:03:21 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 02:03:21 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 02:03:21 GMT
ENV MONGO_MAJOR=3.4
# Wed, 27 Nov 2019 02:03:22 GMT
ENV MONGO_VERSION=3.4.23
# Wed, 27 Nov 2019 02:03:22 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 27 Nov 2019 02:03:40 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 27 Nov 2019 02:03:41 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 27 Nov 2019 02:03:41 GMT
VOLUME [/data/db /data/configdb]
# Wed, 27 Nov 2019 02:03:41 GMT
COPY file:021686a669d0d1d1cbb99d6ca84ff8de10577b78ea985b8cdab9d75b347a3bd0 in /usr/local/bin/ 
# Wed, 27 Nov 2019 02:03:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat (3.4)
# Wed, 27 Nov 2019 02:03:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2019 02:03:42 GMT
EXPOSE 27017
# Wed, 27 Nov 2019 02:03:42 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:976a760c94fcdd7d105269ae621e8269e7bb25a58c52ae667b4029a6bc7e33cb`  
		Last Modified: Sat, 09 Nov 2019 00:25:10 GMT  
		Size: 44.1 MB (44145376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c58992f3c37bb64aeba18910408cda9a7a63e212fe27e95065a8d54130ca5926`  
		Last Modified: Wed, 27 Nov 2019 00:23:39 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca0e5e7f12e6eb512246aea5579fcb771fe7203bc60944384d5cd7962f87ddb`  
		Last Modified: Wed, 27 Nov 2019 00:23:39 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a274cc00ca5f671b1740c43672dbc96504760cee585e7604029a3fe56854a8`  
		Last Modified: Wed, 27 Nov 2019 00:23:39 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6568107a703bb6b06323a98aa1b0b9269889582ed7bfca9784efda57e0f2e9`  
		Last Modified: Wed, 27 Nov 2019 02:05:02 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08957b2477b2c6d539baf4907363ed231b413902491c5cb985cbebe0c3ffe4dc`  
		Last Modified: Wed, 27 Nov 2019 02:05:01 GMT  
		Size: 2.9 MB (2946123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66dbd57d2a3b26381fcffa09bc1e01a2a010b2ea01432d43920927d44a8b2ac`  
		Last Modified: Wed, 27 Nov 2019 02:05:01 GMT  
		Size: 1.2 MB (1243858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135a9132a8625aee4a48702e5db9ea194db458f6109f490569fd5a85bad53b0c`  
		Last Modified: Wed, 27 Nov 2019 02:05:01 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c45eb8eb6ddee2a5e98dc1c47af2194ace743e316fa0273562a93d6d5efe98`  
		Last Modified: Wed, 27 Nov 2019 02:05:00 GMT  
		Size: 2.0 KB (1989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866ea801830c4c1864c47e410b972112ebb96afad39855b071903fe93b4764ac`  
		Last Modified: Wed, 27 Nov 2019 02:04:59 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782aa32daa2e0ad1b857a6d97b1f6b5509222fc564ea0348d565170dcb81ed39`  
		Last Modified: Wed, 27 Nov 2019 02:05:17 GMT  
		Size: 119.7 MB (119690901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa854ba58c1b2c5369f20306a7882fe7c8afc15bd52163a88ef76ce42f1adf41`  
		Last Modified: Wed, 27 Nov 2019 02:04:59 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38e496ab5a398fef652b4bf8a22bf76be2857c992d4e2bb2e74d7c944a6b02a2`  
		Last Modified: Wed, 27 Nov 2019 02:04:59 GMT  
		Size: 4.0 KB (4006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3757d63ce2b9f7e200d8ff434c45e12777b3d480c2eb603abeff0ffff45b5c77`  
		Last Modified: Wed, 27 Nov 2019 02:05:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3.4-xenial` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:fe85914cb2acfa4566f55e84020d0fec0928fe78278028641db565f22cbda373
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156509463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bec8fc74b4cc1dba49eedacd4bbb713ae3bd71d82f5254096bb551bf21c5e6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 26 Nov 2019 23:51:57 GMT
ADD file:2aa99efceecb520e73ba3c7dc167a4fbe6143ce5e9a6499e85dbc75935b3dfab in / 
# Tue, 26 Nov 2019 23:52:01 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 26 Nov 2019 23:52:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 26 Nov 2019 23:52:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 26 Nov 2019 23:52:06 GMT
CMD ["/bin/bash"]
# Wed, 27 Nov 2019 00:48:07 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 27 Nov 2019 00:48:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 00:48:27 GMT
ENV GOSU_VERSION=1.11
# Wed, 27 Nov 2019 00:48:28 GMT
ENV JSYAML_VERSION=3.13.0
# Wed, 27 Nov 2019 00:48:55 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 27 Nov 2019 00:48:57 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 27 Nov 2019 00:48:58 GMT
ENV GPG_KEYS=0C49F3730359A14518585931BC711F9BA15703C6
# Wed, 27 Nov 2019 00:49:00 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 27 Nov 2019 00:49:01 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 27 Nov 2019 00:49:01 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 00:49:02 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 00:49:02 GMT
ENV MONGO_MAJOR=3.4
# Wed, 27 Nov 2019 00:49:03 GMT
ENV MONGO_VERSION=3.4.23
# Wed, 27 Nov 2019 00:49:06 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 27 Nov 2019 00:49:29 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 27 Nov 2019 00:49:33 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 27 Nov 2019 00:49:34 GMT
VOLUME [/data/db /data/configdb]
# Wed, 27 Nov 2019 00:49:36 GMT
COPY file:021686a669d0d1d1cbb99d6ca84ff8de10577b78ea985b8cdab9d75b347a3bd0 in /usr/local/bin/ 
# Wed, 27 Nov 2019 00:49:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat (3.4)
# Wed, 27 Nov 2019 00:49:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2019 00:49:40 GMT
EXPOSE 27017
# Wed, 27 Nov 2019 00:49:41 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:89276bd3590376dfedf96d27b310423c8a1d8c2fe92e4c5a2630aa704b1bb77f`  
		Last Modified: Mon, 11 Nov 2019 15:38:35 GMT  
		Size: 40.0 MB (39951577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a34d6b85b836a6bc6237d1912834f44592a792ab55d92f9ebe1d74973886c6`  
		Last Modified: Tue, 26 Nov 2019 23:52:51 GMT  
		Size: 470.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1bf847b434f33038cc426678c8640251706a59656ef4b0fec6fe3ba88854ab5`  
		Last Modified: Tue, 26 Nov 2019 23:52:51 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcbc4652a1718a263f7195a62c1ca8bf0117bcced50af01ac046bd164f523e5e`  
		Last Modified: Tue, 26 Nov 2019 23:52:51 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29654a2b453807f2a2ab77da919c90f470b457feb09082017c2db0cb659cbae8`  
		Last Modified: Wed, 27 Nov 2019 00:52:48 GMT  
		Size: 2.0 KB (2005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82801a5d252ba1ad5369119729d06933f6687427ec9b00ed3affee3d7d9e5a5b`  
		Last Modified: Wed, 27 Nov 2019 00:52:46 GMT  
		Size: 2.5 MB (2475016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32596fb594dee26ddc2fff00de483a10c3a1e9d0596d9e175424080fd13f6222`  
		Last Modified: Wed, 27 Nov 2019 00:52:46 GMT  
		Size: 1.2 MB (1170042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8df7b8db38cf122e5d4240be8c6a69443d07d574e37834d27d6a9316782df11`  
		Last Modified: Wed, 27 Nov 2019 00:52:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a584ca199e1f752345b7703fa96fc8e508d6a1f9356ff1aa9760b6fe8247a8e`  
		Last Modified: Wed, 27 Nov 2019 00:52:46 GMT  
		Size: 2.0 KB (1998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aacdf9ff19e7305d7121240dfd9d1b49c56446a62c1a13dbc0ff974cf1d2fdb1`  
		Last Modified: Wed, 27 Nov 2019 00:52:44 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66c54bfa417fa777e458b4a690c984d42605c4ba2d9133b5ea4f3ed0f7883939`  
		Last Modified: Wed, 27 Nov 2019 00:53:10 GMT  
		Size: 112.9 MB (112902650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cfb71c955fb087026c7ee53b62e51bf1e734704b8d1ad6cdf23ba533e3090fe`  
		Last Modified: Wed, 27 Nov 2019 00:52:44 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:631fade05419c01f5ca14bff6ecb12a246d75dbbb7358daa79afa37a7f87d878`  
		Last Modified: Wed, 27 Nov 2019 00:52:44 GMT  
		Size: 4.0 KB (4006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20da495cf7cbbe25ed9a76a9f58c07412036412ab9fc9f9b07550cc7a62246b2`  
		Last Modified: Wed, 27 Nov 2019 00:52:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.6`

```console
$ docker pull mongo@sha256:7b7404c9c071cab07e3978734baf1fda6c1b83ef01b9c37d101f8f0128a2f611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.14393.3384; amd64

### `mongo:3.6` - linux; amd64

```console
$ docker pull mongo@sha256:c18f243b3a51049e68ee82847c401222e1dbb45c740e904371a2e2a39f542c9f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.6 MB (165573298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fa64d9ee5add803bcede62a16fdff87c57b7cbc55157480caa44942ecd4a955`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 27 Nov 2019 00:22:54 GMT
ADD file:4eb02fc768cad452a37e8df30bbfcc728f3e6e7ca33af177fd4de06fd07c2098 in / 
# Wed, 27 Nov 2019 00:22:55 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 00:22:56 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 27 Nov 2019 00:22:56 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 27 Nov 2019 00:22:56 GMT
CMD ["/bin/bash"]
# Wed, 27 Nov 2019 02:02:59 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 27 Nov 2019 02:03:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 02:03:08 GMT
ENV GOSU_VERSION=1.11
# Wed, 27 Nov 2019 02:03:08 GMT
ENV JSYAML_VERSION=3.13.0
# Wed, 27 Nov 2019 02:03:19 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 27 Nov 2019 02:03:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 27 Nov 2019 02:03:52 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Wed, 27 Nov 2019 02:03:53 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 27 Nov 2019 02:03:53 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 27 Nov 2019 02:03:53 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 02:03:53 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 02:03:53 GMT
ENV MONGO_MAJOR=3.6
# Tue, 03 Dec 2019 23:26:18 GMT
ENV MONGO_VERSION=3.6.16
# Tue, 03 Dec 2019 23:26:19 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Tue, 03 Dec 2019 23:26:40 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Tue, 03 Dec 2019 23:26:41 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Tue, 03 Dec 2019 23:26:41 GMT
VOLUME [/data/db /data/configdb]
# Tue, 03 Dec 2019 23:26:41 GMT
COPY file:021686a669d0d1d1cbb99d6ca84ff8de10577b78ea985b8cdab9d75b347a3bd0 in /usr/local/bin/ 
# Tue, 03 Dec 2019 23:26:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Dec 2019 23:26:41 GMT
EXPOSE 27017
# Tue, 03 Dec 2019 23:26:42 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:976a760c94fcdd7d105269ae621e8269e7bb25a58c52ae667b4029a6bc7e33cb`  
		Last Modified: Sat, 09 Nov 2019 00:25:10 GMT  
		Size: 44.1 MB (44145376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c58992f3c37bb64aeba18910408cda9a7a63e212fe27e95065a8d54130ca5926`  
		Last Modified: Wed, 27 Nov 2019 00:23:39 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca0e5e7f12e6eb512246aea5579fcb771fe7203bc60944384d5cd7962f87ddb`  
		Last Modified: Wed, 27 Nov 2019 00:23:39 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a274cc00ca5f671b1740c43672dbc96504760cee585e7604029a3fe56854a8`  
		Last Modified: Wed, 27 Nov 2019 00:23:39 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6568107a703bb6b06323a98aa1b0b9269889582ed7bfca9784efda57e0f2e9`  
		Last Modified: Wed, 27 Nov 2019 02:05:02 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08957b2477b2c6d539baf4907363ed231b413902491c5cb985cbebe0c3ffe4dc`  
		Last Modified: Wed, 27 Nov 2019 02:05:01 GMT  
		Size: 2.9 MB (2946123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66dbd57d2a3b26381fcffa09bc1e01a2a010b2ea01432d43920927d44a8b2ac`  
		Last Modified: Wed, 27 Nov 2019 02:05:01 GMT  
		Size: 1.2 MB (1243858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135a9132a8625aee4a48702e5db9ea194db458f6109f490569fd5a85bad53b0c`  
		Last Modified: Wed, 27 Nov 2019 02:05:01 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6412ed86abd20e679cb4e72d098ef56ee0bb8ca029f85ae15d02074aa84919e`  
		Last Modified: Wed, 27 Nov 2019 02:05:22 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20a6504afb84bc25562d6f799c37e80cb6de33594c94610969bc8cabf8a01bb`  
		Last Modified: Tue, 03 Dec 2019 23:27:01 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c35ae8338e5b637ffe1eadf90ac3cf5f0649e30deee265166a258470d6a98d`  
		Last Modified: Tue, 03 Dec 2019 23:27:20 GMT  
		Size: 117.2 MB (117227921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d4094bb54473e0370e72f7720239cf79eeeed4d7101502000898201a91a99f`  
		Last Modified: Tue, 03 Dec 2019 23:27:01 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c0f43ab80060836d54f807cc28fba4e30027b595d0d23dc36ed994c8f7d50e`  
		Last Modified: Tue, 03 Dec 2019 23:27:01 GMT  
		Size: 4.0 KB (4008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3.6` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:4d6093c2b1e85db9acfffcf152e936a481fac5af3a05a8d679a9fa1f9923b0b7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.0 MB (155040149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68ee79b405e7b46538372c16edc6a1549cd7e1f76907fb7070bef7ddc69937f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 26 Nov 2019 23:51:57 GMT
ADD file:2aa99efceecb520e73ba3c7dc167a4fbe6143ce5e9a6499e85dbc75935b3dfab in / 
# Tue, 26 Nov 2019 23:52:01 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 26 Nov 2019 23:52:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 26 Nov 2019 23:52:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 26 Nov 2019 23:52:06 GMT
CMD ["/bin/bash"]
# Wed, 27 Nov 2019 00:48:07 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 27 Nov 2019 00:48:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 00:48:27 GMT
ENV GOSU_VERSION=1.11
# Wed, 27 Nov 2019 00:48:28 GMT
ENV JSYAML_VERSION=3.13.0
# Wed, 27 Nov 2019 00:48:55 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 27 Nov 2019 00:48:57 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 27 Nov 2019 00:49:52 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Wed, 27 Nov 2019 00:49:55 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 27 Nov 2019 00:49:55 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 27 Nov 2019 00:49:56 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 00:49:57 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 00:49:58 GMT
ENV MONGO_MAJOR=3.6
# Tue, 03 Dec 2019 23:47:18 GMT
ENV MONGO_VERSION=3.6.16
# Tue, 03 Dec 2019 23:47:20 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Tue, 03 Dec 2019 23:47:44 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Tue, 03 Dec 2019 23:47:47 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Tue, 03 Dec 2019 23:47:47 GMT
VOLUME [/data/db /data/configdb]
# Tue, 03 Dec 2019 23:47:48 GMT
COPY file:021686a669d0d1d1cbb99d6ca84ff8de10577b78ea985b8cdab9d75b347a3bd0 in /usr/local/bin/ 
# Tue, 03 Dec 2019 23:47:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Dec 2019 23:47:49 GMT
EXPOSE 27017
# Tue, 03 Dec 2019 23:47:50 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:89276bd3590376dfedf96d27b310423c8a1d8c2fe92e4c5a2630aa704b1bb77f`  
		Last Modified: Mon, 11 Nov 2019 15:38:35 GMT  
		Size: 40.0 MB (39951577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a34d6b85b836a6bc6237d1912834f44592a792ab55d92f9ebe1d74973886c6`  
		Last Modified: Tue, 26 Nov 2019 23:52:51 GMT  
		Size: 470.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1bf847b434f33038cc426678c8640251706a59656ef4b0fec6fe3ba88854ab5`  
		Last Modified: Tue, 26 Nov 2019 23:52:51 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcbc4652a1718a263f7195a62c1ca8bf0117bcced50af01ac046bd164f523e5e`  
		Last Modified: Tue, 26 Nov 2019 23:52:51 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29654a2b453807f2a2ab77da919c90f470b457feb09082017c2db0cb659cbae8`  
		Last Modified: Wed, 27 Nov 2019 00:52:48 GMT  
		Size: 2.0 KB (2005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82801a5d252ba1ad5369119729d06933f6687427ec9b00ed3affee3d7d9e5a5b`  
		Last Modified: Wed, 27 Nov 2019 00:52:46 GMT  
		Size: 2.5 MB (2475016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32596fb594dee26ddc2fff00de483a10c3a1e9d0596d9e175424080fd13f6222`  
		Last Modified: Wed, 27 Nov 2019 00:52:46 GMT  
		Size: 1.2 MB (1170042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8df7b8db38cf122e5d4240be8c6a69443d07d574e37834d27d6a9316782df11`  
		Last Modified: Wed, 27 Nov 2019 00:52:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cebea15061d7e2a3269c663f7ecb0d5b395e1e49c409b8d064dbe5f7d6e72172`  
		Last Modified: Wed, 27 Nov 2019 00:53:25 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa2935a9205e0bef6cd51d522ccd870fe0dc3ffdea544e47c9ac26be8eb3122`  
		Last Modified: Tue, 03 Dec 2019 23:48:20 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf9e65ee1a4b2ed96c6967fb16eb0de7c63da6bce0c47e3ec63d0c9bd5a237a`  
		Last Modified: Tue, 03 Dec 2019 23:48:49 GMT  
		Size: 111.4 MB (111433459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c6a6b8b935e01daa47297ffcd098477b6928da4ffc96f92547c69d47479304f`  
		Last Modified: Tue, 03 Dec 2019 23:48:21 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27528e779b9e619704d2f2e340fa917637a6413c6f864c8864405df4245b2a2a`  
		Last Modified: Tue, 03 Dec 2019 23:48:21 GMT  
		Size: 4.0 KB (4006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3.6` - windows version 10.0.14393.3384; amd64

```console
$ docker pull mongo@sha256:1bdcfaae6aafbb14428a8892a23124a40f31bd9414e5d2c3b641904db525a5a8
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5816186803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23192a55795afdee48dc3b3724f1c8a7a93396e95bff38c432c3e559fb9ba27c`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 15:47:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 22:57:29 GMT
ENV MONGO_VERSION=3.6.16
# Wed, 11 Dec 2019 22:57:30 GMT
ENV MONGO_DOWNLOAD_URL=https://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.16-signed.msi
# Wed, 11 Dec 2019 22:57:32 GMT
ENV MONGO_DOWNLOAD_SHA256=06d8b235702c6a2a4f1b721bbd4b59efbc67d0b9dcd5b4d31984c75946837a2e
# Wed, 11 Dec 2019 23:06:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Dec 2019 23:06:40 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Dec 2019 23:06:42 GMT
EXPOSE 27017
# Wed, 11 Dec 2019 23:06:44 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d23dffb4f7b6ebd1cceaac955d664d79467da76c4749d2a37d98556996d8bb0a`  
		Last Modified: Wed, 11 Dec 2019 18:01:38 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628896678dbc43683e49f91e61271412aa1d97a90b65a2ed04e74157fa49532b`  
		Last Modified: Thu, 12 Dec 2019 00:05:14 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f2f11a3aaf5933be1369a1954c04a62d6f707a9e9cde397a42e567f5648e768`  
		Last Modified: Thu, 12 Dec 2019 00:05:14 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:836437d81474147d2932b37b6634ea7d129614983deba273248aae15400c3d08`  
		Last Modified: Thu, 12 Dec 2019 00:05:12 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2c1a30da870a0715c3a3c01c9ab82079b1057836d8b6591a358b85f5c6b8339`  
		Last Modified: Thu, 12 Dec 2019 00:05:41 GMT  
		Size: 93.5 MB (93474561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9ece9fda5ed7b5d814b85fdc19ec1154ec7939bc68330c399127bd4e855024`  
		Last Modified: Thu, 12 Dec 2019 00:05:12 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d3ecfc5eca20e232501e1be3e7bcd29af0358074cbe07316e39ff04be2c224`  
		Last Modified: Thu, 12 Dec 2019 00:05:12 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2833f1058a943a474d0b1fb420d65ba0c50b5b30e8edf26032ec538ed6360beb`  
		Last Modified: Thu, 12 Dec 2019 00:05:12 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.6.16`

```console
$ docker pull mongo@sha256:7b7404c9c071cab07e3978734baf1fda6c1b83ef01b9c37d101f8f0128a2f611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.14393.3384; amd64

### `mongo:3.6.16` - linux; amd64

```console
$ docker pull mongo@sha256:c18f243b3a51049e68ee82847c401222e1dbb45c740e904371a2e2a39f542c9f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.6 MB (165573298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fa64d9ee5add803bcede62a16fdff87c57b7cbc55157480caa44942ecd4a955`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 27 Nov 2019 00:22:54 GMT
ADD file:4eb02fc768cad452a37e8df30bbfcc728f3e6e7ca33af177fd4de06fd07c2098 in / 
# Wed, 27 Nov 2019 00:22:55 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 00:22:56 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 27 Nov 2019 00:22:56 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 27 Nov 2019 00:22:56 GMT
CMD ["/bin/bash"]
# Wed, 27 Nov 2019 02:02:59 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 27 Nov 2019 02:03:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 02:03:08 GMT
ENV GOSU_VERSION=1.11
# Wed, 27 Nov 2019 02:03:08 GMT
ENV JSYAML_VERSION=3.13.0
# Wed, 27 Nov 2019 02:03:19 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 27 Nov 2019 02:03:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 27 Nov 2019 02:03:52 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Wed, 27 Nov 2019 02:03:53 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 27 Nov 2019 02:03:53 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 27 Nov 2019 02:03:53 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 02:03:53 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 02:03:53 GMT
ENV MONGO_MAJOR=3.6
# Tue, 03 Dec 2019 23:26:18 GMT
ENV MONGO_VERSION=3.6.16
# Tue, 03 Dec 2019 23:26:19 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Tue, 03 Dec 2019 23:26:40 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Tue, 03 Dec 2019 23:26:41 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Tue, 03 Dec 2019 23:26:41 GMT
VOLUME [/data/db /data/configdb]
# Tue, 03 Dec 2019 23:26:41 GMT
COPY file:021686a669d0d1d1cbb99d6ca84ff8de10577b78ea985b8cdab9d75b347a3bd0 in /usr/local/bin/ 
# Tue, 03 Dec 2019 23:26:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Dec 2019 23:26:41 GMT
EXPOSE 27017
# Tue, 03 Dec 2019 23:26:42 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:976a760c94fcdd7d105269ae621e8269e7bb25a58c52ae667b4029a6bc7e33cb`  
		Last Modified: Sat, 09 Nov 2019 00:25:10 GMT  
		Size: 44.1 MB (44145376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c58992f3c37bb64aeba18910408cda9a7a63e212fe27e95065a8d54130ca5926`  
		Last Modified: Wed, 27 Nov 2019 00:23:39 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca0e5e7f12e6eb512246aea5579fcb771fe7203bc60944384d5cd7962f87ddb`  
		Last Modified: Wed, 27 Nov 2019 00:23:39 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a274cc00ca5f671b1740c43672dbc96504760cee585e7604029a3fe56854a8`  
		Last Modified: Wed, 27 Nov 2019 00:23:39 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6568107a703bb6b06323a98aa1b0b9269889582ed7bfca9784efda57e0f2e9`  
		Last Modified: Wed, 27 Nov 2019 02:05:02 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08957b2477b2c6d539baf4907363ed231b413902491c5cb985cbebe0c3ffe4dc`  
		Last Modified: Wed, 27 Nov 2019 02:05:01 GMT  
		Size: 2.9 MB (2946123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66dbd57d2a3b26381fcffa09bc1e01a2a010b2ea01432d43920927d44a8b2ac`  
		Last Modified: Wed, 27 Nov 2019 02:05:01 GMT  
		Size: 1.2 MB (1243858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135a9132a8625aee4a48702e5db9ea194db458f6109f490569fd5a85bad53b0c`  
		Last Modified: Wed, 27 Nov 2019 02:05:01 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6412ed86abd20e679cb4e72d098ef56ee0bb8ca029f85ae15d02074aa84919e`  
		Last Modified: Wed, 27 Nov 2019 02:05:22 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20a6504afb84bc25562d6f799c37e80cb6de33594c94610969bc8cabf8a01bb`  
		Last Modified: Tue, 03 Dec 2019 23:27:01 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c35ae8338e5b637ffe1eadf90ac3cf5f0649e30deee265166a258470d6a98d`  
		Last Modified: Tue, 03 Dec 2019 23:27:20 GMT  
		Size: 117.2 MB (117227921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d4094bb54473e0370e72f7720239cf79eeeed4d7101502000898201a91a99f`  
		Last Modified: Tue, 03 Dec 2019 23:27:01 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c0f43ab80060836d54f807cc28fba4e30027b595d0d23dc36ed994c8f7d50e`  
		Last Modified: Tue, 03 Dec 2019 23:27:01 GMT  
		Size: 4.0 KB (4008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3.6.16` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:4d6093c2b1e85db9acfffcf152e936a481fac5af3a05a8d679a9fa1f9923b0b7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.0 MB (155040149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68ee79b405e7b46538372c16edc6a1549cd7e1f76907fb7070bef7ddc69937f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 26 Nov 2019 23:51:57 GMT
ADD file:2aa99efceecb520e73ba3c7dc167a4fbe6143ce5e9a6499e85dbc75935b3dfab in / 
# Tue, 26 Nov 2019 23:52:01 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 26 Nov 2019 23:52:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 26 Nov 2019 23:52:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 26 Nov 2019 23:52:06 GMT
CMD ["/bin/bash"]
# Wed, 27 Nov 2019 00:48:07 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 27 Nov 2019 00:48:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 00:48:27 GMT
ENV GOSU_VERSION=1.11
# Wed, 27 Nov 2019 00:48:28 GMT
ENV JSYAML_VERSION=3.13.0
# Wed, 27 Nov 2019 00:48:55 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 27 Nov 2019 00:48:57 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 27 Nov 2019 00:49:52 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Wed, 27 Nov 2019 00:49:55 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 27 Nov 2019 00:49:55 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 27 Nov 2019 00:49:56 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 00:49:57 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 00:49:58 GMT
ENV MONGO_MAJOR=3.6
# Tue, 03 Dec 2019 23:47:18 GMT
ENV MONGO_VERSION=3.6.16
# Tue, 03 Dec 2019 23:47:20 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Tue, 03 Dec 2019 23:47:44 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Tue, 03 Dec 2019 23:47:47 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Tue, 03 Dec 2019 23:47:47 GMT
VOLUME [/data/db /data/configdb]
# Tue, 03 Dec 2019 23:47:48 GMT
COPY file:021686a669d0d1d1cbb99d6ca84ff8de10577b78ea985b8cdab9d75b347a3bd0 in /usr/local/bin/ 
# Tue, 03 Dec 2019 23:47:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Dec 2019 23:47:49 GMT
EXPOSE 27017
# Tue, 03 Dec 2019 23:47:50 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:89276bd3590376dfedf96d27b310423c8a1d8c2fe92e4c5a2630aa704b1bb77f`  
		Last Modified: Mon, 11 Nov 2019 15:38:35 GMT  
		Size: 40.0 MB (39951577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a34d6b85b836a6bc6237d1912834f44592a792ab55d92f9ebe1d74973886c6`  
		Last Modified: Tue, 26 Nov 2019 23:52:51 GMT  
		Size: 470.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1bf847b434f33038cc426678c8640251706a59656ef4b0fec6fe3ba88854ab5`  
		Last Modified: Tue, 26 Nov 2019 23:52:51 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcbc4652a1718a263f7195a62c1ca8bf0117bcced50af01ac046bd164f523e5e`  
		Last Modified: Tue, 26 Nov 2019 23:52:51 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29654a2b453807f2a2ab77da919c90f470b457feb09082017c2db0cb659cbae8`  
		Last Modified: Wed, 27 Nov 2019 00:52:48 GMT  
		Size: 2.0 KB (2005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82801a5d252ba1ad5369119729d06933f6687427ec9b00ed3affee3d7d9e5a5b`  
		Last Modified: Wed, 27 Nov 2019 00:52:46 GMT  
		Size: 2.5 MB (2475016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32596fb594dee26ddc2fff00de483a10c3a1e9d0596d9e175424080fd13f6222`  
		Last Modified: Wed, 27 Nov 2019 00:52:46 GMT  
		Size: 1.2 MB (1170042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8df7b8db38cf122e5d4240be8c6a69443d07d574e37834d27d6a9316782df11`  
		Last Modified: Wed, 27 Nov 2019 00:52:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cebea15061d7e2a3269c663f7ecb0d5b395e1e49c409b8d064dbe5f7d6e72172`  
		Last Modified: Wed, 27 Nov 2019 00:53:25 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa2935a9205e0bef6cd51d522ccd870fe0dc3ffdea544e47c9ac26be8eb3122`  
		Last Modified: Tue, 03 Dec 2019 23:48:20 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf9e65ee1a4b2ed96c6967fb16eb0de7c63da6bce0c47e3ec63d0c9bd5a237a`  
		Last Modified: Tue, 03 Dec 2019 23:48:49 GMT  
		Size: 111.4 MB (111433459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c6a6b8b935e01daa47297ffcd098477b6928da4ffc96f92547c69d47479304f`  
		Last Modified: Tue, 03 Dec 2019 23:48:21 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27528e779b9e619704d2f2e340fa917637a6413c6f864c8864405df4245b2a2a`  
		Last Modified: Tue, 03 Dec 2019 23:48:21 GMT  
		Size: 4.0 KB (4006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3.6.16` - windows version 10.0.14393.3384; amd64

```console
$ docker pull mongo@sha256:1bdcfaae6aafbb14428a8892a23124a40f31bd9414e5d2c3b641904db525a5a8
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5816186803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23192a55795afdee48dc3b3724f1c8a7a93396e95bff38c432c3e559fb9ba27c`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 15:47:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 22:57:29 GMT
ENV MONGO_VERSION=3.6.16
# Wed, 11 Dec 2019 22:57:30 GMT
ENV MONGO_DOWNLOAD_URL=https://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.16-signed.msi
# Wed, 11 Dec 2019 22:57:32 GMT
ENV MONGO_DOWNLOAD_SHA256=06d8b235702c6a2a4f1b721bbd4b59efbc67d0b9dcd5b4d31984c75946837a2e
# Wed, 11 Dec 2019 23:06:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Dec 2019 23:06:40 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Dec 2019 23:06:42 GMT
EXPOSE 27017
# Wed, 11 Dec 2019 23:06:44 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d23dffb4f7b6ebd1cceaac955d664d79467da76c4749d2a37d98556996d8bb0a`  
		Last Modified: Wed, 11 Dec 2019 18:01:38 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628896678dbc43683e49f91e61271412aa1d97a90b65a2ed04e74157fa49532b`  
		Last Modified: Thu, 12 Dec 2019 00:05:14 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f2f11a3aaf5933be1369a1954c04a62d6f707a9e9cde397a42e567f5648e768`  
		Last Modified: Thu, 12 Dec 2019 00:05:14 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:836437d81474147d2932b37b6634ea7d129614983deba273248aae15400c3d08`  
		Last Modified: Thu, 12 Dec 2019 00:05:12 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2c1a30da870a0715c3a3c01c9ab82079b1057836d8b6591a358b85f5c6b8339`  
		Last Modified: Thu, 12 Dec 2019 00:05:41 GMT  
		Size: 93.5 MB (93474561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9ece9fda5ed7b5d814b85fdc19ec1154ec7939bc68330c399127bd4e855024`  
		Last Modified: Thu, 12 Dec 2019 00:05:12 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d3ecfc5eca20e232501e1be3e7bcd29af0358074cbe07316e39ff04be2c224`  
		Last Modified: Thu, 12 Dec 2019 00:05:12 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2833f1058a943a474d0b1fb420d65ba0c50b5b30e8edf26032ec538ed6360beb`  
		Last Modified: Thu, 12 Dec 2019 00:05:12 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.6.16-windowsservercore`

```console
$ docker pull mongo@sha256:99c034916b7aa0c476e0e2335038220070762cfec62cc661771ce56326b06404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3384; amd64

### `mongo:3.6.16-windowsservercore` - windows version 10.0.14393.3384; amd64

```console
$ docker pull mongo@sha256:1bdcfaae6aafbb14428a8892a23124a40f31bd9414e5d2c3b641904db525a5a8
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5816186803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23192a55795afdee48dc3b3724f1c8a7a93396e95bff38c432c3e559fb9ba27c`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 15:47:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 22:57:29 GMT
ENV MONGO_VERSION=3.6.16
# Wed, 11 Dec 2019 22:57:30 GMT
ENV MONGO_DOWNLOAD_URL=https://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.16-signed.msi
# Wed, 11 Dec 2019 22:57:32 GMT
ENV MONGO_DOWNLOAD_SHA256=06d8b235702c6a2a4f1b721bbd4b59efbc67d0b9dcd5b4d31984c75946837a2e
# Wed, 11 Dec 2019 23:06:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Dec 2019 23:06:40 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Dec 2019 23:06:42 GMT
EXPOSE 27017
# Wed, 11 Dec 2019 23:06:44 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d23dffb4f7b6ebd1cceaac955d664d79467da76c4749d2a37d98556996d8bb0a`  
		Last Modified: Wed, 11 Dec 2019 18:01:38 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628896678dbc43683e49f91e61271412aa1d97a90b65a2ed04e74157fa49532b`  
		Last Modified: Thu, 12 Dec 2019 00:05:14 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f2f11a3aaf5933be1369a1954c04a62d6f707a9e9cde397a42e567f5648e768`  
		Last Modified: Thu, 12 Dec 2019 00:05:14 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:836437d81474147d2932b37b6634ea7d129614983deba273248aae15400c3d08`  
		Last Modified: Thu, 12 Dec 2019 00:05:12 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2c1a30da870a0715c3a3c01c9ab82079b1057836d8b6591a358b85f5c6b8339`  
		Last Modified: Thu, 12 Dec 2019 00:05:41 GMT  
		Size: 93.5 MB (93474561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9ece9fda5ed7b5d814b85fdc19ec1154ec7939bc68330c399127bd4e855024`  
		Last Modified: Thu, 12 Dec 2019 00:05:12 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d3ecfc5eca20e232501e1be3e7bcd29af0358074cbe07316e39ff04be2c224`  
		Last Modified: Thu, 12 Dec 2019 00:05:12 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2833f1058a943a474d0b1fb420d65ba0c50b5b30e8edf26032ec538ed6360beb`  
		Last Modified: Thu, 12 Dec 2019 00:05:12 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.6.16-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:99c034916b7aa0c476e0e2335038220070762cfec62cc661771ce56326b06404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3384; amd64

### `mongo:3.6.16-windowsservercore-ltsc2016` - windows version 10.0.14393.3384; amd64

```console
$ docker pull mongo@sha256:1bdcfaae6aafbb14428a8892a23124a40f31bd9414e5d2c3b641904db525a5a8
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5816186803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23192a55795afdee48dc3b3724f1c8a7a93396e95bff38c432c3e559fb9ba27c`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 15:47:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 22:57:29 GMT
ENV MONGO_VERSION=3.6.16
# Wed, 11 Dec 2019 22:57:30 GMT
ENV MONGO_DOWNLOAD_URL=https://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.16-signed.msi
# Wed, 11 Dec 2019 22:57:32 GMT
ENV MONGO_DOWNLOAD_SHA256=06d8b235702c6a2a4f1b721bbd4b59efbc67d0b9dcd5b4d31984c75946837a2e
# Wed, 11 Dec 2019 23:06:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Dec 2019 23:06:40 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Dec 2019 23:06:42 GMT
EXPOSE 27017
# Wed, 11 Dec 2019 23:06:44 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d23dffb4f7b6ebd1cceaac955d664d79467da76c4749d2a37d98556996d8bb0a`  
		Last Modified: Wed, 11 Dec 2019 18:01:38 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628896678dbc43683e49f91e61271412aa1d97a90b65a2ed04e74157fa49532b`  
		Last Modified: Thu, 12 Dec 2019 00:05:14 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f2f11a3aaf5933be1369a1954c04a62d6f707a9e9cde397a42e567f5648e768`  
		Last Modified: Thu, 12 Dec 2019 00:05:14 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:836437d81474147d2932b37b6634ea7d129614983deba273248aae15400c3d08`  
		Last Modified: Thu, 12 Dec 2019 00:05:12 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2c1a30da870a0715c3a3c01c9ab82079b1057836d8b6591a358b85f5c6b8339`  
		Last Modified: Thu, 12 Dec 2019 00:05:41 GMT  
		Size: 93.5 MB (93474561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9ece9fda5ed7b5d814b85fdc19ec1154ec7939bc68330c399127bd4e855024`  
		Last Modified: Thu, 12 Dec 2019 00:05:12 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d3ecfc5eca20e232501e1be3e7bcd29af0358074cbe07316e39ff04be2c224`  
		Last Modified: Thu, 12 Dec 2019 00:05:12 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2833f1058a943a474d0b1fb420d65ba0c50b5b30e8edf26032ec538ed6360beb`  
		Last Modified: Thu, 12 Dec 2019 00:05:12 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.6.16-xenial`

```console
$ docker pull mongo@sha256:5ff3aff1a99662e052cb66ca70ab474ff08e20a7ef14e9f248639ca31f65f05e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:3.6.16-xenial` - linux; amd64

```console
$ docker pull mongo@sha256:c18f243b3a51049e68ee82847c401222e1dbb45c740e904371a2e2a39f542c9f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.6 MB (165573298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fa64d9ee5add803bcede62a16fdff87c57b7cbc55157480caa44942ecd4a955`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 27 Nov 2019 00:22:54 GMT
ADD file:4eb02fc768cad452a37e8df30bbfcc728f3e6e7ca33af177fd4de06fd07c2098 in / 
# Wed, 27 Nov 2019 00:22:55 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 00:22:56 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 27 Nov 2019 00:22:56 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 27 Nov 2019 00:22:56 GMT
CMD ["/bin/bash"]
# Wed, 27 Nov 2019 02:02:59 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 27 Nov 2019 02:03:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 02:03:08 GMT
ENV GOSU_VERSION=1.11
# Wed, 27 Nov 2019 02:03:08 GMT
ENV JSYAML_VERSION=3.13.0
# Wed, 27 Nov 2019 02:03:19 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 27 Nov 2019 02:03:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 27 Nov 2019 02:03:52 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Wed, 27 Nov 2019 02:03:53 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 27 Nov 2019 02:03:53 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 27 Nov 2019 02:03:53 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 02:03:53 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 02:03:53 GMT
ENV MONGO_MAJOR=3.6
# Tue, 03 Dec 2019 23:26:18 GMT
ENV MONGO_VERSION=3.6.16
# Tue, 03 Dec 2019 23:26:19 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Tue, 03 Dec 2019 23:26:40 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Tue, 03 Dec 2019 23:26:41 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Tue, 03 Dec 2019 23:26:41 GMT
VOLUME [/data/db /data/configdb]
# Tue, 03 Dec 2019 23:26:41 GMT
COPY file:021686a669d0d1d1cbb99d6ca84ff8de10577b78ea985b8cdab9d75b347a3bd0 in /usr/local/bin/ 
# Tue, 03 Dec 2019 23:26:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Dec 2019 23:26:41 GMT
EXPOSE 27017
# Tue, 03 Dec 2019 23:26:42 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:976a760c94fcdd7d105269ae621e8269e7bb25a58c52ae667b4029a6bc7e33cb`  
		Last Modified: Sat, 09 Nov 2019 00:25:10 GMT  
		Size: 44.1 MB (44145376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c58992f3c37bb64aeba18910408cda9a7a63e212fe27e95065a8d54130ca5926`  
		Last Modified: Wed, 27 Nov 2019 00:23:39 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca0e5e7f12e6eb512246aea5579fcb771fe7203bc60944384d5cd7962f87ddb`  
		Last Modified: Wed, 27 Nov 2019 00:23:39 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a274cc00ca5f671b1740c43672dbc96504760cee585e7604029a3fe56854a8`  
		Last Modified: Wed, 27 Nov 2019 00:23:39 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6568107a703bb6b06323a98aa1b0b9269889582ed7bfca9784efda57e0f2e9`  
		Last Modified: Wed, 27 Nov 2019 02:05:02 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08957b2477b2c6d539baf4907363ed231b413902491c5cb985cbebe0c3ffe4dc`  
		Last Modified: Wed, 27 Nov 2019 02:05:01 GMT  
		Size: 2.9 MB (2946123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66dbd57d2a3b26381fcffa09bc1e01a2a010b2ea01432d43920927d44a8b2ac`  
		Last Modified: Wed, 27 Nov 2019 02:05:01 GMT  
		Size: 1.2 MB (1243858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135a9132a8625aee4a48702e5db9ea194db458f6109f490569fd5a85bad53b0c`  
		Last Modified: Wed, 27 Nov 2019 02:05:01 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6412ed86abd20e679cb4e72d098ef56ee0bb8ca029f85ae15d02074aa84919e`  
		Last Modified: Wed, 27 Nov 2019 02:05:22 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20a6504afb84bc25562d6f799c37e80cb6de33594c94610969bc8cabf8a01bb`  
		Last Modified: Tue, 03 Dec 2019 23:27:01 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c35ae8338e5b637ffe1eadf90ac3cf5f0649e30deee265166a258470d6a98d`  
		Last Modified: Tue, 03 Dec 2019 23:27:20 GMT  
		Size: 117.2 MB (117227921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d4094bb54473e0370e72f7720239cf79eeeed4d7101502000898201a91a99f`  
		Last Modified: Tue, 03 Dec 2019 23:27:01 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c0f43ab80060836d54f807cc28fba4e30027b595d0d23dc36ed994c8f7d50e`  
		Last Modified: Tue, 03 Dec 2019 23:27:01 GMT  
		Size: 4.0 KB (4008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3.6.16-xenial` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:4d6093c2b1e85db9acfffcf152e936a481fac5af3a05a8d679a9fa1f9923b0b7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.0 MB (155040149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68ee79b405e7b46538372c16edc6a1549cd7e1f76907fb7070bef7ddc69937f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 26 Nov 2019 23:51:57 GMT
ADD file:2aa99efceecb520e73ba3c7dc167a4fbe6143ce5e9a6499e85dbc75935b3dfab in / 
# Tue, 26 Nov 2019 23:52:01 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 26 Nov 2019 23:52:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 26 Nov 2019 23:52:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 26 Nov 2019 23:52:06 GMT
CMD ["/bin/bash"]
# Wed, 27 Nov 2019 00:48:07 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 27 Nov 2019 00:48:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 00:48:27 GMT
ENV GOSU_VERSION=1.11
# Wed, 27 Nov 2019 00:48:28 GMT
ENV JSYAML_VERSION=3.13.0
# Wed, 27 Nov 2019 00:48:55 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 27 Nov 2019 00:48:57 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 27 Nov 2019 00:49:52 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Wed, 27 Nov 2019 00:49:55 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 27 Nov 2019 00:49:55 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 27 Nov 2019 00:49:56 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 00:49:57 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 00:49:58 GMT
ENV MONGO_MAJOR=3.6
# Tue, 03 Dec 2019 23:47:18 GMT
ENV MONGO_VERSION=3.6.16
# Tue, 03 Dec 2019 23:47:20 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Tue, 03 Dec 2019 23:47:44 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Tue, 03 Dec 2019 23:47:47 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Tue, 03 Dec 2019 23:47:47 GMT
VOLUME [/data/db /data/configdb]
# Tue, 03 Dec 2019 23:47:48 GMT
COPY file:021686a669d0d1d1cbb99d6ca84ff8de10577b78ea985b8cdab9d75b347a3bd0 in /usr/local/bin/ 
# Tue, 03 Dec 2019 23:47:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Dec 2019 23:47:49 GMT
EXPOSE 27017
# Tue, 03 Dec 2019 23:47:50 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:89276bd3590376dfedf96d27b310423c8a1d8c2fe92e4c5a2630aa704b1bb77f`  
		Last Modified: Mon, 11 Nov 2019 15:38:35 GMT  
		Size: 40.0 MB (39951577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a34d6b85b836a6bc6237d1912834f44592a792ab55d92f9ebe1d74973886c6`  
		Last Modified: Tue, 26 Nov 2019 23:52:51 GMT  
		Size: 470.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1bf847b434f33038cc426678c8640251706a59656ef4b0fec6fe3ba88854ab5`  
		Last Modified: Tue, 26 Nov 2019 23:52:51 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcbc4652a1718a263f7195a62c1ca8bf0117bcced50af01ac046bd164f523e5e`  
		Last Modified: Tue, 26 Nov 2019 23:52:51 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29654a2b453807f2a2ab77da919c90f470b457feb09082017c2db0cb659cbae8`  
		Last Modified: Wed, 27 Nov 2019 00:52:48 GMT  
		Size: 2.0 KB (2005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82801a5d252ba1ad5369119729d06933f6687427ec9b00ed3affee3d7d9e5a5b`  
		Last Modified: Wed, 27 Nov 2019 00:52:46 GMT  
		Size: 2.5 MB (2475016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32596fb594dee26ddc2fff00de483a10c3a1e9d0596d9e175424080fd13f6222`  
		Last Modified: Wed, 27 Nov 2019 00:52:46 GMT  
		Size: 1.2 MB (1170042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8df7b8db38cf122e5d4240be8c6a69443d07d574e37834d27d6a9316782df11`  
		Last Modified: Wed, 27 Nov 2019 00:52:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cebea15061d7e2a3269c663f7ecb0d5b395e1e49c409b8d064dbe5f7d6e72172`  
		Last Modified: Wed, 27 Nov 2019 00:53:25 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa2935a9205e0bef6cd51d522ccd870fe0dc3ffdea544e47c9ac26be8eb3122`  
		Last Modified: Tue, 03 Dec 2019 23:48:20 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf9e65ee1a4b2ed96c6967fb16eb0de7c63da6bce0c47e3ec63d0c9bd5a237a`  
		Last Modified: Tue, 03 Dec 2019 23:48:49 GMT  
		Size: 111.4 MB (111433459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c6a6b8b935e01daa47297ffcd098477b6928da4ffc96f92547c69d47479304f`  
		Last Modified: Tue, 03 Dec 2019 23:48:21 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27528e779b9e619704d2f2e340fa917637a6413c6f864c8864405df4245b2a2a`  
		Last Modified: Tue, 03 Dec 2019 23:48:21 GMT  
		Size: 4.0 KB (4006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.6-windowsservercore`

```console
$ docker pull mongo@sha256:99c034916b7aa0c476e0e2335038220070762cfec62cc661771ce56326b06404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3384; amd64

### `mongo:3.6-windowsservercore` - windows version 10.0.14393.3384; amd64

```console
$ docker pull mongo@sha256:1bdcfaae6aafbb14428a8892a23124a40f31bd9414e5d2c3b641904db525a5a8
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5816186803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23192a55795afdee48dc3b3724f1c8a7a93396e95bff38c432c3e559fb9ba27c`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 15:47:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 22:57:29 GMT
ENV MONGO_VERSION=3.6.16
# Wed, 11 Dec 2019 22:57:30 GMT
ENV MONGO_DOWNLOAD_URL=https://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.16-signed.msi
# Wed, 11 Dec 2019 22:57:32 GMT
ENV MONGO_DOWNLOAD_SHA256=06d8b235702c6a2a4f1b721bbd4b59efbc67d0b9dcd5b4d31984c75946837a2e
# Wed, 11 Dec 2019 23:06:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Dec 2019 23:06:40 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Dec 2019 23:06:42 GMT
EXPOSE 27017
# Wed, 11 Dec 2019 23:06:44 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d23dffb4f7b6ebd1cceaac955d664d79467da76c4749d2a37d98556996d8bb0a`  
		Last Modified: Wed, 11 Dec 2019 18:01:38 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628896678dbc43683e49f91e61271412aa1d97a90b65a2ed04e74157fa49532b`  
		Last Modified: Thu, 12 Dec 2019 00:05:14 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f2f11a3aaf5933be1369a1954c04a62d6f707a9e9cde397a42e567f5648e768`  
		Last Modified: Thu, 12 Dec 2019 00:05:14 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:836437d81474147d2932b37b6634ea7d129614983deba273248aae15400c3d08`  
		Last Modified: Thu, 12 Dec 2019 00:05:12 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2c1a30da870a0715c3a3c01c9ab82079b1057836d8b6591a358b85f5c6b8339`  
		Last Modified: Thu, 12 Dec 2019 00:05:41 GMT  
		Size: 93.5 MB (93474561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9ece9fda5ed7b5d814b85fdc19ec1154ec7939bc68330c399127bd4e855024`  
		Last Modified: Thu, 12 Dec 2019 00:05:12 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d3ecfc5eca20e232501e1be3e7bcd29af0358074cbe07316e39ff04be2c224`  
		Last Modified: Thu, 12 Dec 2019 00:05:12 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2833f1058a943a474d0b1fb420d65ba0c50b5b30e8edf26032ec538ed6360beb`  
		Last Modified: Thu, 12 Dec 2019 00:05:12 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.6-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:99c034916b7aa0c476e0e2335038220070762cfec62cc661771ce56326b06404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3384; amd64

### `mongo:3.6-windowsservercore-ltsc2016` - windows version 10.0.14393.3384; amd64

```console
$ docker pull mongo@sha256:1bdcfaae6aafbb14428a8892a23124a40f31bd9414e5d2c3b641904db525a5a8
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5816186803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23192a55795afdee48dc3b3724f1c8a7a93396e95bff38c432c3e559fb9ba27c`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 15:47:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 22:57:29 GMT
ENV MONGO_VERSION=3.6.16
# Wed, 11 Dec 2019 22:57:30 GMT
ENV MONGO_DOWNLOAD_URL=https://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.16-signed.msi
# Wed, 11 Dec 2019 22:57:32 GMT
ENV MONGO_DOWNLOAD_SHA256=06d8b235702c6a2a4f1b721bbd4b59efbc67d0b9dcd5b4d31984c75946837a2e
# Wed, 11 Dec 2019 23:06:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Dec 2019 23:06:40 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Dec 2019 23:06:42 GMT
EXPOSE 27017
# Wed, 11 Dec 2019 23:06:44 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d23dffb4f7b6ebd1cceaac955d664d79467da76c4749d2a37d98556996d8bb0a`  
		Last Modified: Wed, 11 Dec 2019 18:01:38 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628896678dbc43683e49f91e61271412aa1d97a90b65a2ed04e74157fa49532b`  
		Last Modified: Thu, 12 Dec 2019 00:05:14 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f2f11a3aaf5933be1369a1954c04a62d6f707a9e9cde397a42e567f5648e768`  
		Last Modified: Thu, 12 Dec 2019 00:05:14 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:836437d81474147d2932b37b6634ea7d129614983deba273248aae15400c3d08`  
		Last Modified: Thu, 12 Dec 2019 00:05:12 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2c1a30da870a0715c3a3c01c9ab82079b1057836d8b6591a358b85f5c6b8339`  
		Last Modified: Thu, 12 Dec 2019 00:05:41 GMT  
		Size: 93.5 MB (93474561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9ece9fda5ed7b5d814b85fdc19ec1154ec7939bc68330c399127bd4e855024`  
		Last Modified: Thu, 12 Dec 2019 00:05:12 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d3ecfc5eca20e232501e1be3e7bcd29af0358074cbe07316e39ff04be2c224`  
		Last Modified: Thu, 12 Dec 2019 00:05:12 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2833f1058a943a474d0b1fb420d65ba0c50b5b30e8edf26032ec538ed6360beb`  
		Last Modified: Thu, 12 Dec 2019 00:05:12 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.6-xenial`

```console
$ docker pull mongo@sha256:5ff3aff1a99662e052cb66ca70ab474ff08e20a7ef14e9f248639ca31f65f05e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:3.6-xenial` - linux; amd64

```console
$ docker pull mongo@sha256:c18f243b3a51049e68ee82847c401222e1dbb45c740e904371a2e2a39f542c9f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.6 MB (165573298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fa64d9ee5add803bcede62a16fdff87c57b7cbc55157480caa44942ecd4a955`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 27 Nov 2019 00:22:54 GMT
ADD file:4eb02fc768cad452a37e8df30bbfcc728f3e6e7ca33af177fd4de06fd07c2098 in / 
# Wed, 27 Nov 2019 00:22:55 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 00:22:56 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 27 Nov 2019 00:22:56 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 27 Nov 2019 00:22:56 GMT
CMD ["/bin/bash"]
# Wed, 27 Nov 2019 02:02:59 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 27 Nov 2019 02:03:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 02:03:08 GMT
ENV GOSU_VERSION=1.11
# Wed, 27 Nov 2019 02:03:08 GMT
ENV JSYAML_VERSION=3.13.0
# Wed, 27 Nov 2019 02:03:19 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 27 Nov 2019 02:03:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 27 Nov 2019 02:03:52 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Wed, 27 Nov 2019 02:03:53 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 27 Nov 2019 02:03:53 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 27 Nov 2019 02:03:53 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 02:03:53 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 02:03:53 GMT
ENV MONGO_MAJOR=3.6
# Tue, 03 Dec 2019 23:26:18 GMT
ENV MONGO_VERSION=3.6.16
# Tue, 03 Dec 2019 23:26:19 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Tue, 03 Dec 2019 23:26:40 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Tue, 03 Dec 2019 23:26:41 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Tue, 03 Dec 2019 23:26:41 GMT
VOLUME [/data/db /data/configdb]
# Tue, 03 Dec 2019 23:26:41 GMT
COPY file:021686a669d0d1d1cbb99d6ca84ff8de10577b78ea985b8cdab9d75b347a3bd0 in /usr/local/bin/ 
# Tue, 03 Dec 2019 23:26:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Dec 2019 23:26:41 GMT
EXPOSE 27017
# Tue, 03 Dec 2019 23:26:42 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:976a760c94fcdd7d105269ae621e8269e7bb25a58c52ae667b4029a6bc7e33cb`  
		Last Modified: Sat, 09 Nov 2019 00:25:10 GMT  
		Size: 44.1 MB (44145376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c58992f3c37bb64aeba18910408cda9a7a63e212fe27e95065a8d54130ca5926`  
		Last Modified: Wed, 27 Nov 2019 00:23:39 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca0e5e7f12e6eb512246aea5579fcb771fe7203bc60944384d5cd7962f87ddb`  
		Last Modified: Wed, 27 Nov 2019 00:23:39 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a274cc00ca5f671b1740c43672dbc96504760cee585e7604029a3fe56854a8`  
		Last Modified: Wed, 27 Nov 2019 00:23:39 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6568107a703bb6b06323a98aa1b0b9269889582ed7bfca9784efda57e0f2e9`  
		Last Modified: Wed, 27 Nov 2019 02:05:02 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08957b2477b2c6d539baf4907363ed231b413902491c5cb985cbebe0c3ffe4dc`  
		Last Modified: Wed, 27 Nov 2019 02:05:01 GMT  
		Size: 2.9 MB (2946123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66dbd57d2a3b26381fcffa09bc1e01a2a010b2ea01432d43920927d44a8b2ac`  
		Last Modified: Wed, 27 Nov 2019 02:05:01 GMT  
		Size: 1.2 MB (1243858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135a9132a8625aee4a48702e5db9ea194db458f6109f490569fd5a85bad53b0c`  
		Last Modified: Wed, 27 Nov 2019 02:05:01 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6412ed86abd20e679cb4e72d098ef56ee0bb8ca029f85ae15d02074aa84919e`  
		Last Modified: Wed, 27 Nov 2019 02:05:22 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20a6504afb84bc25562d6f799c37e80cb6de33594c94610969bc8cabf8a01bb`  
		Last Modified: Tue, 03 Dec 2019 23:27:01 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c35ae8338e5b637ffe1eadf90ac3cf5f0649e30deee265166a258470d6a98d`  
		Last Modified: Tue, 03 Dec 2019 23:27:20 GMT  
		Size: 117.2 MB (117227921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d4094bb54473e0370e72f7720239cf79eeeed4d7101502000898201a91a99f`  
		Last Modified: Tue, 03 Dec 2019 23:27:01 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c0f43ab80060836d54f807cc28fba4e30027b595d0d23dc36ed994c8f7d50e`  
		Last Modified: Tue, 03 Dec 2019 23:27:01 GMT  
		Size: 4.0 KB (4008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3.6-xenial` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:4d6093c2b1e85db9acfffcf152e936a481fac5af3a05a8d679a9fa1f9923b0b7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.0 MB (155040149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68ee79b405e7b46538372c16edc6a1549cd7e1f76907fb7070bef7ddc69937f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 26 Nov 2019 23:51:57 GMT
ADD file:2aa99efceecb520e73ba3c7dc167a4fbe6143ce5e9a6499e85dbc75935b3dfab in / 
# Tue, 26 Nov 2019 23:52:01 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 26 Nov 2019 23:52:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 26 Nov 2019 23:52:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 26 Nov 2019 23:52:06 GMT
CMD ["/bin/bash"]
# Wed, 27 Nov 2019 00:48:07 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 27 Nov 2019 00:48:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 00:48:27 GMT
ENV GOSU_VERSION=1.11
# Wed, 27 Nov 2019 00:48:28 GMT
ENV JSYAML_VERSION=3.13.0
# Wed, 27 Nov 2019 00:48:55 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 27 Nov 2019 00:48:57 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 27 Nov 2019 00:49:52 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Wed, 27 Nov 2019 00:49:55 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 27 Nov 2019 00:49:55 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 27 Nov 2019 00:49:56 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 00:49:57 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 00:49:58 GMT
ENV MONGO_MAJOR=3.6
# Tue, 03 Dec 2019 23:47:18 GMT
ENV MONGO_VERSION=3.6.16
# Tue, 03 Dec 2019 23:47:20 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Tue, 03 Dec 2019 23:47:44 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Tue, 03 Dec 2019 23:47:47 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Tue, 03 Dec 2019 23:47:47 GMT
VOLUME [/data/db /data/configdb]
# Tue, 03 Dec 2019 23:47:48 GMT
COPY file:021686a669d0d1d1cbb99d6ca84ff8de10577b78ea985b8cdab9d75b347a3bd0 in /usr/local/bin/ 
# Tue, 03 Dec 2019 23:47:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Dec 2019 23:47:49 GMT
EXPOSE 27017
# Tue, 03 Dec 2019 23:47:50 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:89276bd3590376dfedf96d27b310423c8a1d8c2fe92e4c5a2630aa704b1bb77f`  
		Last Modified: Mon, 11 Nov 2019 15:38:35 GMT  
		Size: 40.0 MB (39951577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a34d6b85b836a6bc6237d1912834f44592a792ab55d92f9ebe1d74973886c6`  
		Last Modified: Tue, 26 Nov 2019 23:52:51 GMT  
		Size: 470.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1bf847b434f33038cc426678c8640251706a59656ef4b0fec6fe3ba88854ab5`  
		Last Modified: Tue, 26 Nov 2019 23:52:51 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcbc4652a1718a263f7195a62c1ca8bf0117bcced50af01ac046bd164f523e5e`  
		Last Modified: Tue, 26 Nov 2019 23:52:51 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29654a2b453807f2a2ab77da919c90f470b457feb09082017c2db0cb659cbae8`  
		Last Modified: Wed, 27 Nov 2019 00:52:48 GMT  
		Size: 2.0 KB (2005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82801a5d252ba1ad5369119729d06933f6687427ec9b00ed3affee3d7d9e5a5b`  
		Last Modified: Wed, 27 Nov 2019 00:52:46 GMT  
		Size: 2.5 MB (2475016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32596fb594dee26ddc2fff00de483a10c3a1e9d0596d9e175424080fd13f6222`  
		Last Modified: Wed, 27 Nov 2019 00:52:46 GMT  
		Size: 1.2 MB (1170042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8df7b8db38cf122e5d4240be8c6a69443d07d574e37834d27d6a9316782df11`  
		Last Modified: Wed, 27 Nov 2019 00:52:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cebea15061d7e2a3269c663f7ecb0d5b395e1e49c409b8d064dbe5f7d6e72172`  
		Last Modified: Wed, 27 Nov 2019 00:53:25 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa2935a9205e0bef6cd51d522ccd870fe0dc3ffdea544e47c9ac26be8eb3122`  
		Last Modified: Tue, 03 Dec 2019 23:48:20 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf9e65ee1a4b2ed96c6967fb16eb0de7c63da6bce0c47e3ec63d0c9bd5a237a`  
		Last Modified: Tue, 03 Dec 2019 23:48:49 GMT  
		Size: 111.4 MB (111433459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c6a6b8b935e01daa47297ffcd098477b6928da4ffc96f92547c69d47479304f`  
		Last Modified: Tue, 03 Dec 2019 23:48:21 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27528e779b9e619704d2f2e340fa917637a6413c6f864c8864405df4245b2a2a`  
		Last Modified: Tue, 03 Dec 2019 23:48:21 GMT  
		Size: 4.0 KB (4006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3-windowsservercore`

```console
$ docker pull mongo@sha256:99c034916b7aa0c476e0e2335038220070762cfec62cc661771ce56326b06404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3384; amd64

### `mongo:3-windowsservercore` - windows version 10.0.14393.3384; amd64

```console
$ docker pull mongo@sha256:1bdcfaae6aafbb14428a8892a23124a40f31bd9414e5d2c3b641904db525a5a8
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5816186803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23192a55795afdee48dc3b3724f1c8a7a93396e95bff38c432c3e559fb9ba27c`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 15:47:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 22:57:29 GMT
ENV MONGO_VERSION=3.6.16
# Wed, 11 Dec 2019 22:57:30 GMT
ENV MONGO_DOWNLOAD_URL=https://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.16-signed.msi
# Wed, 11 Dec 2019 22:57:32 GMT
ENV MONGO_DOWNLOAD_SHA256=06d8b235702c6a2a4f1b721bbd4b59efbc67d0b9dcd5b4d31984c75946837a2e
# Wed, 11 Dec 2019 23:06:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Dec 2019 23:06:40 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Dec 2019 23:06:42 GMT
EXPOSE 27017
# Wed, 11 Dec 2019 23:06:44 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d23dffb4f7b6ebd1cceaac955d664d79467da76c4749d2a37d98556996d8bb0a`  
		Last Modified: Wed, 11 Dec 2019 18:01:38 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628896678dbc43683e49f91e61271412aa1d97a90b65a2ed04e74157fa49532b`  
		Last Modified: Thu, 12 Dec 2019 00:05:14 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f2f11a3aaf5933be1369a1954c04a62d6f707a9e9cde397a42e567f5648e768`  
		Last Modified: Thu, 12 Dec 2019 00:05:14 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:836437d81474147d2932b37b6634ea7d129614983deba273248aae15400c3d08`  
		Last Modified: Thu, 12 Dec 2019 00:05:12 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2c1a30da870a0715c3a3c01c9ab82079b1057836d8b6591a358b85f5c6b8339`  
		Last Modified: Thu, 12 Dec 2019 00:05:41 GMT  
		Size: 93.5 MB (93474561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9ece9fda5ed7b5d814b85fdc19ec1154ec7939bc68330c399127bd4e855024`  
		Last Modified: Thu, 12 Dec 2019 00:05:12 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d3ecfc5eca20e232501e1be3e7bcd29af0358074cbe07316e39ff04be2c224`  
		Last Modified: Thu, 12 Dec 2019 00:05:12 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2833f1058a943a474d0b1fb420d65ba0c50b5b30e8edf26032ec538ed6360beb`  
		Last Modified: Thu, 12 Dec 2019 00:05:12 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:99c034916b7aa0c476e0e2335038220070762cfec62cc661771ce56326b06404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3384; amd64

### `mongo:3-windowsservercore-ltsc2016` - windows version 10.0.14393.3384; amd64

```console
$ docker pull mongo@sha256:1bdcfaae6aafbb14428a8892a23124a40f31bd9414e5d2c3b641904db525a5a8
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5816186803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23192a55795afdee48dc3b3724f1c8a7a93396e95bff38c432c3e559fb9ba27c`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 15:47:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 22:57:29 GMT
ENV MONGO_VERSION=3.6.16
# Wed, 11 Dec 2019 22:57:30 GMT
ENV MONGO_DOWNLOAD_URL=https://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.16-signed.msi
# Wed, 11 Dec 2019 22:57:32 GMT
ENV MONGO_DOWNLOAD_SHA256=06d8b235702c6a2a4f1b721bbd4b59efbc67d0b9dcd5b4d31984c75946837a2e
# Wed, 11 Dec 2019 23:06:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Dec 2019 23:06:40 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Dec 2019 23:06:42 GMT
EXPOSE 27017
# Wed, 11 Dec 2019 23:06:44 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d23dffb4f7b6ebd1cceaac955d664d79467da76c4749d2a37d98556996d8bb0a`  
		Last Modified: Wed, 11 Dec 2019 18:01:38 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628896678dbc43683e49f91e61271412aa1d97a90b65a2ed04e74157fa49532b`  
		Last Modified: Thu, 12 Dec 2019 00:05:14 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f2f11a3aaf5933be1369a1954c04a62d6f707a9e9cde397a42e567f5648e768`  
		Last Modified: Thu, 12 Dec 2019 00:05:14 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:836437d81474147d2932b37b6634ea7d129614983deba273248aae15400c3d08`  
		Last Modified: Thu, 12 Dec 2019 00:05:12 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2c1a30da870a0715c3a3c01c9ab82079b1057836d8b6591a358b85f5c6b8339`  
		Last Modified: Thu, 12 Dec 2019 00:05:41 GMT  
		Size: 93.5 MB (93474561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9ece9fda5ed7b5d814b85fdc19ec1154ec7939bc68330c399127bd4e855024`  
		Last Modified: Thu, 12 Dec 2019 00:05:12 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d3ecfc5eca20e232501e1be3e7bcd29af0358074cbe07316e39ff04be2c224`  
		Last Modified: Thu, 12 Dec 2019 00:05:12 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2833f1058a943a474d0b1fb420d65ba0c50b5b30e8edf26032ec538ed6360beb`  
		Last Modified: Thu, 12 Dec 2019 00:05:12 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3-xenial`

```console
$ docker pull mongo@sha256:5ff3aff1a99662e052cb66ca70ab474ff08e20a7ef14e9f248639ca31f65f05e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:3-xenial` - linux; amd64

```console
$ docker pull mongo@sha256:c18f243b3a51049e68ee82847c401222e1dbb45c740e904371a2e2a39f542c9f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.6 MB (165573298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fa64d9ee5add803bcede62a16fdff87c57b7cbc55157480caa44942ecd4a955`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 27 Nov 2019 00:22:54 GMT
ADD file:4eb02fc768cad452a37e8df30bbfcc728f3e6e7ca33af177fd4de06fd07c2098 in / 
# Wed, 27 Nov 2019 00:22:55 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 00:22:56 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 27 Nov 2019 00:22:56 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 27 Nov 2019 00:22:56 GMT
CMD ["/bin/bash"]
# Wed, 27 Nov 2019 02:02:59 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 27 Nov 2019 02:03:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 02:03:08 GMT
ENV GOSU_VERSION=1.11
# Wed, 27 Nov 2019 02:03:08 GMT
ENV JSYAML_VERSION=3.13.0
# Wed, 27 Nov 2019 02:03:19 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 27 Nov 2019 02:03:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 27 Nov 2019 02:03:52 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Wed, 27 Nov 2019 02:03:53 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 27 Nov 2019 02:03:53 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 27 Nov 2019 02:03:53 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 02:03:53 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 02:03:53 GMT
ENV MONGO_MAJOR=3.6
# Tue, 03 Dec 2019 23:26:18 GMT
ENV MONGO_VERSION=3.6.16
# Tue, 03 Dec 2019 23:26:19 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Tue, 03 Dec 2019 23:26:40 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Tue, 03 Dec 2019 23:26:41 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Tue, 03 Dec 2019 23:26:41 GMT
VOLUME [/data/db /data/configdb]
# Tue, 03 Dec 2019 23:26:41 GMT
COPY file:021686a669d0d1d1cbb99d6ca84ff8de10577b78ea985b8cdab9d75b347a3bd0 in /usr/local/bin/ 
# Tue, 03 Dec 2019 23:26:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Dec 2019 23:26:41 GMT
EXPOSE 27017
# Tue, 03 Dec 2019 23:26:42 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:976a760c94fcdd7d105269ae621e8269e7bb25a58c52ae667b4029a6bc7e33cb`  
		Last Modified: Sat, 09 Nov 2019 00:25:10 GMT  
		Size: 44.1 MB (44145376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c58992f3c37bb64aeba18910408cda9a7a63e212fe27e95065a8d54130ca5926`  
		Last Modified: Wed, 27 Nov 2019 00:23:39 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca0e5e7f12e6eb512246aea5579fcb771fe7203bc60944384d5cd7962f87ddb`  
		Last Modified: Wed, 27 Nov 2019 00:23:39 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a274cc00ca5f671b1740c43672dbc96504760cee585e7604029a3fe56854a8`  
		Last Modified: Wed, 27 Nov 2019 00:23:39 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6568107a703bb6b06323a98aa1b0b9269889582ed7bfca9784efda57e0f2e9`  
		Last Modified: Wed, 27 Nov 2019 02:05:02 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08957b2477b2c6d539baf4907363ed231b413902491c5cb985cbebe0c3ffe4dc`  
		Last Modified: Wed, 27 Nov 2019 02:05:01 GMT  
		Size: 2.9 MB (2946123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66dbd57d2a3b26381fcffa09bc1e01a2a010b2ea01432d43920927d44a8b2ac`  
		Last Modified: Wed, 27 Nov 2019 02:05:01 GMT  
		Size: 1.2 MB (1243858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135a9132a8625aee4a48702e5db9ea194db458f6109f490569fd5a85bad53b0c`  
		Last Modified: Wed, 27 Nov 2019 02:05:01 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6412ed86abd20e679cb4e72d098ef56ee0bb8ca029f85ae15d02074aa84919e`  
		Last Modified: Wed, 27 Nov 2019 02:05:22 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20a6504afb84bc25562d6f799c37e80cb6de33594c94610969bc8cabf8a01bb`  
		Last Modified: Tue, 03 Dec 2019 23:27:01 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c35ae8338e5b637ffe1eadf90ac3cf5f0649e30deee265166a258470d6a98d`  
		Last Modified: Tue, 03 Dec 2019 23:27:20 GMT  
		Size: 117.2 MB (117227921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d4094bb54473e0370e72f7720239cf79eeeed4d7101502000898201a91a99f`  
		Last Modified: Tue, 03 Dec 2019 23:27:01 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c0f43ab80060836d54f807cc28fba4e30027b595d0d23dc36ed994c8f7d50e`  
		Last Modified: Tue, 03 Dec 2019 23:27:01 GMT  
		Size: 4.0 KB (4008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3-xenial` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:4d6093c2b1e85db9acfffcf152e936a481fac5af3a05a8d679a9fa1f9923b0b7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.0 MB (155040149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68ee79b405e7b46538372c16edc6a1549cd7e1f76907fb7070bef7ddc69937f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 26 Nov 2019 23:51:57 GMT
ADD file:2aa99efceecb520e73ba3c7dc167a4fbe6143ce5e9a6499e85dbc75935b3dfab in / 
# Tue, 26 Nov 2019 23:52:01 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 26 Nov 2019 23:52:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 26 Nov 2019 23:52:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 26 Nov 2019 23:52:06 GMT
CMD ["/bin/bash"]
# Wed, 27 Nov 2019 00:48:07 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 27 Nov 2019 00:48:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 00:48:27 GMT
ENV GOSU_VERSION=1.11
# Wed, 27 Nov 2019 00:48:28 GMT
ENV JSYAML_VERSION=3.13.0
# Wed, 27 Nov 2019 00:48:55 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 27 Nov 2019 00:48:57 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 27 Nov 2019 00:49:52 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Wed, 27 Nov 2019 00:49:55 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 27 Nov 2019 00:49:55 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 27 Nov 2019 00:49:56 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 00:49:57 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 00:49:58 GMT
ENV MONGO_MAJOR=3.6
# Tue, 03 Dec 2019 23:47:18 GMT
ENV MONGO_VERSION=3.6.16
# Tue, 03 Dec 2019 23:47:20 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Tue, 03 Dec 2019 23:47:44 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Tue, 03 Dec 2019 23:47:47 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Tue, 03 Dec 2019 23:47:47 GMT
VOLUME [/data/db /data/configdb]
# Tue, 03 Dec 2019 23:47:48 GMT
COPY file:021686a669d0d1d1cbb99d6ca84ff8de10577b78ea985b8cdab9d75b347a3bd0 in /usr/local/bin/ 
# Tue, 03 Dec 2019 23:47:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Dec 2019 23:47:49 GMT
EXPOSE 27017
# Tue, 03 Dec 2019 23:47:50 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:89276bd3590376dfedf96d27b310423c8a1d8c2fe92e4c5a2630aa704b1bb77f`  
		Last Modified: Mon, 11 Nov 2019 15:38:35 GMT  
		Size: 40.0 MB (39951577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a34d6b85b836a6bc6237d1912834f44592a792ab55d92f9ebe1d74973886c6`  
		Last Modified: Tue, 26 Nov 2019 23:52:51 GMT  
		Size: 470.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1bf847b434f33038cc426678c8640251706a59656ef4b0fec6fe3ba88854ab5`  
		Last Modified: Tue, 26 Nov 2019 23:52:51 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcbc4652a1718a263f7195a62c1ca8bf0117bcced50af01ac046bd164f523e5e`  
		Last Modified: Tue, 26 Nov 2019 23:52:51 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29654a2b453807f2a2ab77da919c90f470b457feb09082017c2db0cb659cbae8`  
		Last Modified: Wed, 27 Nov 2019 00:52:48 GMT  
		Size: 2.0 KB (2005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82801a5d252ba1ad5369119729d06933f6687427ec9b00ed3affee3d7d9e5a5b`  
		Last Modified: Wed, 27 Nov 2019 00:52:46 GMT  
		Size: 2.5 MB (2475016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32596fb594dee26ddc2fff00de483a10c3a1e9d0596d9e175424080fd13f6222`  
		Last Modified: Wed, 27 Nov 2019 00:52:46 GMT  
		Size: 1.2 MB (1170042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8df7b8db38cf122e5d4240be8c6a69443d07d574e37834d27d6a9316782df11`  
		Last Modified: Wed, 27 Nov 2019 00:52:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cebea15061d7e2a3269c663f7ecb0d5b395e1e49c409b8d064dbe5f7d6e72172`  
		Last Modified: Wed, 27 Nov 2019 00:53:25 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa2935a9205e0bef6cd51d522ccd870fe0dc3ffdea544e47c9ac26be8eb3122`  
		Last Modified: Tue, 03 Dec 2019 23:48:20 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf9e65ee1a4b2ed96c6967fb16eb0de7c63da6bce0c47e3ec63d0c9bd5a237a`  
		Last Modified: Tue, 03 Dec 2019 23:48:49 GMT  
		Size: 111.4 MB (111433459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c6a6b8b935e01daa47297ffcd098477b6928da4ffc96f92547c69d47479304f`  
		Last Modified: Tue, 03 Dec 2019 23:48:21 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27528e779b9e619704d2f2e340fa917637a6413c6f864c8864405df4245b2a2a`  
		Last Modified: Tue, 03 Dec 2019 23:48:21 GMT  
		Size: 4.0 KB (4006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4`

```console
$ docker pull mongo@sha256:6ca49afbcb2b44aedf53f5f27b20c99813f500981b6d62193aa770e8340461cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x
	-	windows version 10.0.14393.3384; amd64
	-	windows version 10.0.17134.1184; amd64

### `mongo:4` - linux; amd64

```console
$ docker pull mongo@sha256:52c3314bee611f91d37b9b1bc0cc2755b1388f2de5b396b441f3fe94bef6c56c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.3 MB (147285849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:965553e202a44592bc26d8c076eafef996a6dfc0de5bb2c1cf1795cd3b3a7373`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 31 Oct 2019 22:20:35 GMT
ADD file:a48a5dc1b9dbfc632f6cf86fe27b770b63f07a115c98c4465dc184e303a4efa1 in / 
# Thu, 31 Oct 2019 22:20:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:20:36 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:20:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:20:37 GMT
CMD ["/bin/bash"]
# Fri, 01 Nov 2019 00:34:46 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 01 Nov 2019 00:34:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Nov 2019 00:34:56 GMT
ENV GOSU_VERSION=1.11
# Fri, 01 Nov 2019 00:34:56 GMT
ENV JSYAML_VERSION=3.13.0
# Fri, 01 Nov 2019 00:35:07 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 01 Nov 2019 00:35:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Nov 2019 00:35:09 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 01 Nov 2019 00:35:10 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 01 Nov 2019 00:35:10 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 01 Nov 2019 00:35:10 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 01 Nov 2019 00:35:10 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 01 Nov 2019 00:35:10 GMT
ENV MONGO_MAJOR=4.2
# Fri, 01 Nov 2019 00:35:11 GMT
ENV MONGO_VERSION=4.2.1
# Fri, 01 Nov 2019 00:35:11 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 01 Nov 2019 00:35:29 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 01 Nov 2019 00:35:29 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 01 Nov 2019 00:35:30 GMT
VOLUME [/data/db /data/configdb]
# Fri, 01 Nov 2019 00:35:30 GMT
COPY file:021686a669d0d1d1cbb99d6ca84ff8de10577b78ea985b8cdab9d75b347a3bd0 in /usr/local/bin/ 
# Fri, 01 Nov 2019 00:35:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Nov 2019 00:35:30 GMT
EXPOSE 27017
# Fri, 01 Nov 2019 00:35:30 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7ddbc47eeb70dc7f08e410a6667948b87ff3883024eb41478b44ef9a81bf400c`  
		Last Modified: Wed, 30 Oct 2019 00:25:34 GMT  
		Size: 26.7 MB (26688847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1bbdc448b7263673926b8fe2e88491e5083a8b4b06ddfabf311f2fc5f27e2ff`  
		Last Modified: Thu, 31 Oct 2019 22:21:39 GMT  
		Size: 35.4 KB (35362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3b70e3904492c753652606df4726430426f42ea56e06ea924d6fea7ae162a1`  
		Last Modified: Thu, 31 Oct 2019 22:21:39 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45d437916d5781043432f2d72608049dcf74ddbd27daa01a25fa63c8f1b9adc4`  
		Last Modified: Thu, 31 Oct 2019 22:21:39 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e119fb0e0a556b13af304b430ee02ab7dae340974ed1c56c071f8b76ba94fce8`  
		Last Modified: Fri, 01 Nov 2019 00:37:26 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f0b9bae1ea1da827453099df499d277582fee378b02632492f5960b3199f45`  
		Last Modified: Fri, 01 Nov 2019 00:37:27 GMT  
		Size: 3.0 MB (2981726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e7c2967f1132938ce99899a660345acb7d81a2722d03be593c501f2d5a0fb5`  
		Last Modified: Fri, 01 Nov 2019 00:37:28 GMT  
		Size: 5.8 MB (5763200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a945568374aab4d5559c42c26f5e91d0077eaa2fc6f4ac2de12681665847c1`  
		Last Modified: Fri, 01 Nov 2019 00:37:25 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93333bc225a750104af3ea7a4dee020f14d95b1f7e9f3d3bbd4629a0d38cbeb8`  
		Last Modified: Fri, 01 Nov 2019 00:37:25 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c10bd6c9bdce8efa69364bade1114e6089a95a8c9b652fad7f4e5e169f882a`  
		Last Modified: Fri, 01 Nov 2019 00:37:24 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4e3538e99cfab06dca9314aa7ee1d77d09973875de8c9505159544571ca423`  
		Last Modified: Fri, 01 Nov 2019 00:37:50 GMT  
		Size: 111.8 MB (111807903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1164b51d180a68eda4b69db7227a8ef9d79924dba229c255fb45a45e7704bdbd`  
		Last Modified: Fri, 01 Nov 2019 00:37:24 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a715a7d71f27cafd081768bdaeddc9538ab8060043ae9d59e20cb067fcf98b5e`  
		Last Modified: Fri, 01 Nov 2019 00:37:25 GMT  
		Size: 4.0 KB (4007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:922dfe530d2a4bad26786c20f5ab9667bf8096c5378615ee1fb3327e1e45ba46
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136338781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f09d4aa5ffaafb22631c9c99c5038d690874b461d69736e308b6d3f5c9bbd57b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 31 Oct 2019 22:40:37 GMT
ADD file:4c6cab77271e86386e8f3d4ecf06c17a3e9339481bea878a706d2c5dc4a0addd in / 
# Thu, 31 Oct 2019 22:40:40 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:40:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:40:43 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:40:44 GMT
CMD ["/bin/bash"]
# Fri, 01 Nov 2019 00:48:13 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 01 Nov 2019 00:48:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Nov 2019 00:48:29 GMT
ENV GOSU_VERSION=1.11
# Fri, 01 Nov 2019 00:48:30 GMT
ENV JSYAML_VERSION=3.13.0
# Fri, 01 Nov 2019 00:48:54 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 01 Nov 2019 00:48:57 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Nov 2019 00:48:57 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 01 Nov 2019 00:49:00 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 01 Nov 2019 00:49:00 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 01 Nov 2019 00:49:01 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 01 Nov 2019 00:49:02 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 01 Nov 2019 00:49:03 GMT
ENV MONGO_MAJOR=4.2
# Fri, 01 Nov 2019 00:49:04 GMT
ENV MONGO_VERSION=4.2.1
# Fri, 01 Nov 2019 00:49:06 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 01 Nov 2019 00:49:30 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 01 Nov 2019 00:49:34 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 01 Nov 2019 00:49:35 GMT
VOLUME [/data/db /data/configdb]
# Fri, 01 Nov 2019 00:49:35 GMT
COPY file:021686a669d0d1d1cbb99d6ca84ff8de10577b78ea985b8cdab9d75b347a3bd0 in /usr/local/bin/ 
# Fri, 01 Nov 2019 00:49:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Nov 2019 00:49:37 GMT
EXPOSE 27017
# Fri, 01 Nov 2019 00:49:39 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:6531af3558948c8839fd7cc7eb7062aa86bfae891870ccaafd554ac65c97971b`  
		Last Modified: Thu, 31 Oct 2019 22:42:23 GMT  
		Size: 23.7 MB (23718403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f7942d2fb7381ee1735a4c972ef45c89b6521902e6eba024d4791dfd069def`  
		Last Modified: Thu, 31 Oct 2019 22:42:16 GMT  
		Size: 35.2 KB (35198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdce94e690d563311eb8b102b49e94a01b2a4c965daa9e33d5e59168dc4327e0`  
		Last Modified: Thu, 31 Oct 2019 22:42:16 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96a89ada1c32e30a1998945a8785c18bcdce55dcfe2b666bb587d432255cb11`  
		Last Modified: Thu, 31 Oct 2019 22:42:16 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441c8b285da3534c6705c81b056f0421dc29aff21e3b8e891572ee58969b23c4`  
		Last Modified: Fri, 01 Nov 2019 00:51:57 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3369e8993485be78046aa93778ceb9f0ac9a9cd1460c56dd0a39b5612a2bf0db`  
		Last Modified: Fri, 01 Nov 2019 00:51:58 GMT  
		Size: 2.7 MB (2675614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aedf06151273427f8c9155f17ce3804e486f188c768a9b1395a8e808091bfa59`  
		Last Modified: Fri, 01 Nov 2019 00:51:58 GMT  
		Size: 5.3 MB (5282727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb0173982fa974e75dbc470008149e563eb935f7027577971b32bf9790721d4`  
		Last Modified: Fri, 01 Nov 2019 00:51:57 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ff79f67ba8dbf80063a12f5296a984d5fe453bf212e7aa4562c6e9b2109d01`  
		Last Modified: Fri, 01 Nov 2019 00:51:55 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6085923db4441f085ae2476ca6fa391e1df060ca33644fb82a401201a757959f`  
		Last Modified: Fri, 01 Nov 2019 00:51:55 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50380edb4431c149b589a7bff3db64481717f9197cc57e99ea9cd2e278dab9b6`  
		Last Modified: Fri, 01 Nov 2019 00:52:21 GMT  
		Size: 104.6 MB (104617931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e667dd7db0918baac9e775b56ad7dbb1ec2806eee8f7415812d13f0dd700ed0`  
		Last Modified: Fri, 01 Nov 2019 00:51:55 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:545348b868a6ab6133facf259e76520240f6e7a6f4cdf4e53b38215cc9929476`  
		Last Modified: Fri, 01 Nov 2019 00:51:55 GMT  
		Size: 4.0 KB (4003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4` - linux; s390x

```console
$ docker pull mongo@sha256:76cdaab6ec75306255226b0ba785dd113c2f264320382e88368ae1157f93ddbc
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.5 MB (143531232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0000651cfa9056c242a341ec396f1b03a548a1d8486b039d3b6fd5d010751ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 31 Oct 2019 22:41:56 GMT
ADD file:6e6c5c69d7791dc0b62c8d03fc0c5051c6291e08dfc4e11abbdc333bc6f44359 in / 
# Thu, 31 Oct 2019 22:41:58 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:41:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:42:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:42:01 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 23:16:28 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Thu, 31 Oct 2019 23:16:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 31 Oct 2019 23:16:46 GMT
ENV GOSU_VERSION=1.11
# Thu, 31 Oct 2019 23:16:46 GMT
ENV JSYAML_VERSION=3.13.0
# Thu, 31 Oct 2019 23:17:14 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 31 Oct 2019 23:17:15 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 31 Oct 2019 23:17:15 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Thu, 31 Oct 2019 23:17:18 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 31 Oct 2019 23:17:18 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 31 Oct 2019 23:17:18 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 31 Oct 2019 23:17:18 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 31 Oct 2019 23:17:19 GMT
ENV MONGO_MAJOR=4.2
# Thu, 31 Oct 2019 23:17:19 GMT
ENV MONGO_VERSION=4.2.1
# Thu, 31 Oct 2019 23:17:21 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Thu, 31 Oct 2019 23:18:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Thu, 31 Oct 2019 23:18:06 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Thu, 31 Oct 2019 23:18:06 GMT
VOLUME [/data/db /data/configdb]
# Thu, 31 Oct 2019 23:18:07 GMT
COPY file:021686a669d0d1d1cbb99d6ca84ff8de10577b78ea985b8cdab9d75b347a3bd0 in /usr/local/bin/ 
# Thu, 31 Oct 2019 23:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 31 Oct 2019 23:18:08 GMT
EXPOSE 27017
# Thu, 31 Oct 2019 23:18:08 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:617b55fd1ba95b3ed68226101c9b2568ed00a9b7c50959230d2124648f3a47d2`  
		Last Modified: Thu, 31 Oct 2019 22:43:47 GMT  
		Size: 25.4 MB (25364650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee6ed80b799b3b7d7d66e31ba7e61be1f8d02732bccb1a22d1f14c65f9cea21`  
		Last Modified: Thu, 31 Oct 2019 22:43:42 GMT  
		Size: 36.2 KB (36173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc71634b6bba51b68da661aedfd0876ba93b197653cc94323ca050369bef0bc`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 841.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e017bfda3869ce68902d01d6dfb0fe74964f8c598ea31bc77825772e58a122b`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43ce05cccebf9f7a410bbace7582d3f6a8a6eb8f969e738365ff52fa41bef56`  
		Last Modified: Thu, 31 Oct 2019 23:18:26 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232ad1433592ae3e49689f9a399155d8cd4cb66e85d3e9a3371f64c5d3767ef5`  
		Last Modified: Thu, 31 Oct 2019 23:18:27 GMT  
		Size: 2.7 MB (2714202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfb83020b47608042582b07eac59bfe53f87d076f429e2030150fce7671fcfc`  
		Last Modified: Thu, 31 Oct 2019 23:18:28 GMT  
		Size: 5.7 MB (5684577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e67294f8ac41b2fbbb98389025f6a2934cd3e85f08b50641d96ce6fd42c5d4`  
		Last Modified: Thu, 31 Oct 2019 23:18:25 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10477e3f19872878bbd97b9b1d529a9cda966b6dab49c609ca17a815f56eaf03`  
		Last Modified: Thu, 31 Oct 2019 23:18:24 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd80e3c144d231663b9fc4f19de43fe431596d85adb3fd80db6e1965f649b99`  
		Last Modified: Thu, 31 Oct 2019 23:18:23 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390cef7a4233b0430f858343c7ffa603238382f6b3d57400fba4bc37dc1fc338`  
		Last Modified: Thu, 31 Oct 2019 23:18:49 GMT  
		Size: 109.7 MB (109722811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ab2a7a00460c93578481306a6e5212441ae6f399678d3a0938105339ff3659`  
		Last Modified: Thu, 31 Oct 2019 23:18:24 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729e6c5603fe8d82346fcc9450f163fdd06d4f77ad73e59fca74447aa971f9ba`  
		Last Modified: Thu, 31 Oct 2019 23:18:23 GMT  
		Size: 4.0 KB (4005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4` - windows version 10.0.14393.3384; amd64

```console
$ docker pull mongo@sha256:37ed0ce402c453d82362c8674a95a84ccdc02c9864bfa4fc8170d49d42584a92
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5816058219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fb916a127f9cd60ef9757a818d2c965590bd5303ed4476b1c5a8445ac0b6e2a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 15:47:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 23:35:26 GMT
ENV MONGO_VERSION=4.2.1
# Wed, 11 Dec 2019 23:35:27 GMT
ENV MONGO_DOWNLOAD_URL=https://downloads.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.1-signed.msi
# Wed, 11 Dec 2019 23:35:28 GMT
ENV MONGO_DOWNLOAD_SHA256=0bd9f5361d21cf358156e8e18aae3f4bc0298e9949b4b988c4b15b52913f91d6
# Wed, 11 Dec 2019 23:44:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Dec 2019 23:44:48 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Dec 2019 23:44:50 GMT
EXPOSE 27017
# Wed, 11 Dec 2019 23:44:52 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d23dffb4f7b6ebd1cceaac955d664d79467da76c4749d2a37d98556996d8bb0a`  
		Last Modified: Wed, 11 Dec 2019 18:01:38 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c30838129c9ab8ebc7cfc1437e4655ad2fcbf99b7c2a4f618f0dadeb02ee9b1`  
		Last Modified: Thu, 12 Dec 2019 00:08:43 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e12474c86cd0cf6cec9ffc98ee72da8f5c5ef236665b487ed4590f3083cb5d`  
		Last Modified: Thu, 12 Dec 2019 00:08:43 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de05e906a577fa8f95e8df9641ed2d7b042e8ab039218c711f9be88e153f43c4`  
		Last Modified: Thu, 12 Dec 2019 00:08:40 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0735cfc26b92c99aa40bf6c1feb6c344f5d7113c006c50441f5304fe92fd8285`  
		Last Modified: Thu, 12 Dec 2019 00:09:03 GMT  
		Size: 93.3 MB (93345990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77636ccac26ca06e73af52744671d5c6ae3db8960b110a60b0e95ed0231a9619`  
		Last Modified: Thu, 12 Dec 2019 00:08:41 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e83b06286df83053a894432b81bf6c78acc9a1000308697438915c8072f4210`  
		Last Modified: Thu, 12 Dec 2019 00:08:40 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262bd20abcdfdee728fa18bff25d7071edeb206e56c11f9b4a4080018ca2db1f`  
		Last Modified: Thu, 12 Dec 2019 00:08:40 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4` - windows version 10.0.17134.1184; amd64

```console
$ docker pull mongo@sha256:672798fb05567fe529909cf3f81422c76d5fe1a2bdbd1974abd9aa238b639f36
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2809636910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:def4de6e07cdaff0556a068451bdd6043d77ee91d167288d24f922343dab649d`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 12 Apr 2018 09:20:54 GMT
RUN Apply image 1803-RTM-amd64
# Wed, 04 Dec 2019 15:21:18 GMT
RUN Install update 1803-amd64
# Wed, 11 Dec 2019 15:36:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 23:45:17 GMT
ENV MONGO_VERSION=4.2.1
# Wed, 11 Dec 2019 23:45:19 GMT
ENV MONGO_DOWNLOAD_URL=https://downloads.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.1-signed.msi
# Wed, 11 Dec 2019 23:45:20 GMT
ENV MONGO_DOWNLOAD_SHA256=0bd9f5361d21cf358156e8e18aae3f4bc0298e9949b4b988c4b15b52913f91d6
# Thu, 12 Dec 2019 00:03:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 12 Dec 2019 00:03:17 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 12 Dec 2019 00:03:18 GMT
EXPOSE 27017
# Thu, 12 Dec 2019 00:03:20 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:d9e8b01179bfc94a5bdb1810fbd76b999aa52016001ace2d3a4c4bc7065a9601`  
		Last Modified: Tue, 18 Sep 2018 22:43:55 GMT  
		Size: 1.7 GB (1659688273 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d117323cd539488e5ef3bef575a41fa714d83119b0da1896607d96ec2a5e3b52`  
		Size: 696.9 MB (696873564 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:70c803815d644f3772896add8df055dfd33f5934921ca0c57efc290d42454abf`  
		Last Modified: Wed, 11 Dec 2019 18:00:43 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48cbbbce208b5a8e143d43012de06b33cd12dc212fae3e3f6cf28b1acd900861`  
		Last Modified: Thu, 12 Dec 2019 00:09:45 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f72bd77f828256b25eb7375c46fdec577565bc53d89a05fa8a100796450f599`  
		Last Modified: Thu, 12 Dec 2019 00:09:45 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d00e37fa3cf44154da5932563d6cfcff58333ffd56b34c2933a9b14f273b96`  
		Last Modified: Thu, 12 Dec 2019 00:09:42 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e5c13eeee73b3c63164fa7984e8859a050bb173cb69c2b162e7d93845778b5f`  
		Last Modified: Thu, 12 Dec 2019 00:10:40 GMT  
		Size: 453.1 MB (453066744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de21f5bd53ce10a88ff8e77419719b9a2283c1a3f88706ebc56116df5d13e82e`  
		Last Modified: Thu, 12 Dec 2019 00:09:42 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aecef79094cae66ab1003365b8a64bce825e973f8fc6fdaac26462fb31363a15`  
		Last Modified: Thu, 12 Dec 2019 00:09:43 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c1b6171741d09ad84e50e1a007624e0807534f6adc039d848e5915d26bcdfa9`  
		Last Modified: Thu, 12 Dec 2019 00:09:43 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.0`

```console
$ docker pull mongo@sha256:1aea2377c5b17dcd5e67d4c33f8f7ee09da62a4dd27ae988958b70efdf3a0a6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.14393.3384; amd64
	-	windows version 10.0.17134.1184; amd64

### `mongo:4.0` - linux; amd64

```console
$ docker pull mongo@sha256:f0397f249d2ced55ce59c7c50a8490ea536ffe4af4db75801f3443a380b7070a
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.3 MB (153327907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0712bd00d695f12ce3deac6f8425af7a782ee6c2bbb4697af7d94ba341c68ae7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 27 Nov 2019 00:22:54 GMT
ADD file:4eb02fc768cad452a37e8df30bbfcc728f3e6e7ca33af177fd4de06fd07c2098 in / 
# Wed, 27 Nov 2019 00:22:55 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 00:22:56 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 27 Nov 2019 00:22:56 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 27 Nov 2019 00:22:56 GMT
CMD ["/bin/bash"]
# Wed, 27 Nov 2019 02:02:59 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 27 Nov 2019 02:03:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 02:03:08 GMT
ENV GOSU_VERSION=1.11
# Wed, 27 Nov 2019 02:03:08 GMT
ENV JSYAML_VERSION=3.13.0
# Wed, 27 Nov 2019 02:03:19 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 27 Nov 2019 02:03:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 27 Nov 2019 02:04:20 GMT
ENV GPG_KEYS=9DA31620334BD75D9DCB49F368818C72E52529D4
# Wed, 27 Nov 2019 02:04:21 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 27 Nov 2019 02:04:21 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 27 Nov 2019 02:04:21 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 02:04:21 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 02:04:21 GMT
ENV MONGO_MAJOR=4.0
# Wed, 27 Nov 2019 02:04:22 GMT
ENV MONGO_VERSION=4.0.13
# Wed, 27 Nov 2019 02:04:22 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 27 Nov 2019 02:04:39 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 27 Nov 2019 02:04:40 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 27 Nov 2019 02:04:40 GMT
VOLUME [/data/db /data/configdb]
# Wed, 27 Nov 2019 02:04:40 GMT
COPY file:021686a669d0d1d1cbb99d6ca84ff8de10577b78ea985b8cdab9d75b347a3bd0 in /usr/local/bin/ 
# Wed, 27 Nov 2019 02:04:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2019 02:04:42 GMT
EXPOSE 27017
# Wed, 27 Nov 2019 02:04:43 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:976a760c94fcdd7d105269ae621e8269e7bb25a58c52ae667b4029a6bc7e33cb`  
		Last Modified: Sat, 09 Nov 2019 00:25:10 GMT  
		Size: 44.1 MB (44145376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c58992f3c37bb64aeba18910408cda9a7a63e212fe27e95065a8d54130ca5926`  
		Last Modified: Wed, 27 Nov 2019 00:23:39 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca0e5e7f12e6eb512246aea5579fcb771fe7203bc60944384d5cd7962f87ddb`  
		Last Modified: Wed, 27 Nov 2019 00:23:39 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a274cc00ca5f671b1740c43672dbc96504760cee585e7604029a3fe56854a8`  
		Last Modified: Wed, 27 Nov 2019 00:23:39 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6568107a703bb6b06323a98aa1b0b9269889582ed7bfca9784efda57e0f2e9`  
		Last Modified: Wed, 27 Nov 2019 02:05:02 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08957b2477b2c6d539baf4907363ed231b413902491c5cb985cbebe0c3ffe4dc`  
		Last Modified: Wed, 27 Nov 2019 02:05:01 GMT  
		Size: 2.9 MB (2946123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66dbd57d2a3b26381fcffa09bc1e01a2a010b2ea01432d43920927d44a8b2ac`  
		Last Modified: Wed, 27 Nov 2019 02:05:01 GMT  
		Size: 1.2 MB (1243858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135a9132a8625aee4a48702e5db9ea194db458f6109f490569fd5a85bad53b0c`  
		Last Modified: Wed, 27 Nov 2019 02:05:01 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b7c17ba1dfd1e6d1e81e53c7ec478aaa252cf71f763fccbf8ad0886f683d99`  
		Last Modified: Wed, 27 Nov 2019 02:05:48 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b595c9e65de00f4ca8af04db11e32dc5a88786cfb786b4b4a84fcec15c16ed9`  
		Last Modified: Wed, 27 Nov 2019 02:05:48 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e74b440cab6657354dc1f10c360db0d95b292793c03edc3c8d0c45e64a9009e`  
		Last Modified: Wed, 27 Nov 2019 02:06:05 GMT  
		Size: 105.0 MB (104983100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c04ed8f6ca08229e3b61f8daa67b49ba118a465c5d411927f726d4baf7437eb`  
		Last Modified: Wed, 27 Nov 2019 02:05:48 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dbe824121e4a60ac8c829dd487c52ce2fac50319e9d90b0dc5ad865e2640390`  
		Last Modified: Wed, 27 Nov 2019 02:05:48 GMT  
		Size: 4.0 KB (4007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:f49ed701bb903cd709218404e56d372dfb9b03b536cd7754c7f80793666070a7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (143029158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dafb85d77371751edcf79ff34b7bebafc75415d082ad7d1369038c38bc71b569`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 26 Nov 2019 23:51:57 GMT
ADD file:2aa99efceecb520e73ba3c7dc167a4fbe6143ce5e9a6499e85dbc75935b3dfab in / 
# Tue, 26 Nov 2019 23:52:01 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 26 Nov 2019 23:52:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 26 Nov 2019 23:52:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 26 Nov 2019 23:52:06 GMT
CMD ["/bin/bash"]
# Wed, 27 Nov 2019 00:48:07 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 27 Nov 2019 00:48:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 00:48:27 GMT
ENV GOSU_VERSION=1.11
# Wed, 27 Nov 2019 00:48:28 GMT
ENV JSYAML_VERSION=3.13.0
# Wed, 27 Nov 2019 00:48:55 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 27 Nov 2019 00:48:57 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 27 Nov 2019 00:50:57 GMT
ENV GPG_KEYS=9DA31620334BD75D9DCB49F368818C72E52529D4
# Wed, 27 Nov 2019 00:51:02 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 27 Nov 2019 00:51:03 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 27 Nov 2019 00:51:04 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 00:51:06 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 00:51:10 GMT
ENV MONGO_MAJOR=4.0
# Wed, 27 Nov 2019 00:51:12 GMT
ENV MONGO_VERSION=4.0.13
# Wed, 27 Nov 2019 00:51:19 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 27 Nov 2019 00:52:07 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 27 Nov 2019 00:52:11 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 27 Nov 2019 00:52:12 GMT
VOLUME [/data/db /data/configdb]
# Wed, 27 Nov 2019 00:52:13 GMT
COPY file:021686a669d0d1d1cbb99d6ca84ff8de10577b78ea985b8cdab9d75b347a3bd0 in /usr/local/bin/ 
# Wed, 27 Nov 2019 00:52:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2019 00:52:15 GMT
EXPOSE 27017
# Wed, 27 Nov 2019 00:52:16 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:89276bd3590376dfedf96d27b310423c8a1d8c2fe92e4c5a2630aa704b1bb77f`  
		Last Modified: Mon, 11 Nov 2019 15:38:35 GMT  
		Size: 40.0 MB (39951577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a34d6b85b836a6bc6237d1912834f44592a792ab55d92f9ebe1d74973886c6`  
		Last Modified: Tue, 26 Nov 2019 23:52:51 GMT  
		Size: 470.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1bf847b434f33038cc426678c8640251706a59656ef4b0fec6fe3ba88854ab5`  
		Last Modified: Tue, 26 Nov 2019 23:52:51 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcbc4652a1718a263f7195a62c1ca8bf0117bcced50af01ac046bd164f523e5e`  
		Last Modified: Tue, 26 Nov 2019 23:52:51 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29654a2b453807f2a2ab77da919c90f470b457feb09082017c2db0cb659cbae8`  
		Last Modified: Wed, 27 Nov 2019 00:52:48 GMT  
		Size: 2.0 KB (2005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82801a5d252ba1ad5369119729d06933f6687427ec9b00ed3affee3d7d9e5a5b`  
		Last Modified: Wed, 27 Nov 2019 00:52:46 GMT  
		Size: 2.5 MB (2475016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32596fb594dee26ddc2fff00de483a10c3a1e9d0596d9e175424080fd13f6222`  
		Last Modified: Wed, 27 Nov 2019 00:52:46 GMT  
		Size: 1.2 MB (1170042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8df7b8db38cf122e5d4240be8c6a69443d07d574e37834d27d6a9316782df11`  
		Last Modified: Wed, 27 Nov 2019 00:52:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70b88de3f1a87007d7bccff5988808f14d2e9742aed390012fcccb4e6c30281`  
		Last Modified: Wed, 27 Nov 2019 00:54:01 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd55f9c2264e49984337fbf81be3647067592db952bc49fb7106b3f1eb40daa`  
		Last Modified: Wed, 27 Nov 2019 00:54:01 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df962447b3ce6cd904afde3cc1c9a3b0995ed98f88a8c1acb923721fdb6110a7`  
		Last Modified: Wed, 27 Nov 2019 00:54:39 GMT  
		Size: 99.4 MB (99423038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cde73bff8f9cd090b08b2b46cc3a82c3b4f1f8270437943a6205927efe3fb87`  
		Last Modified: Wed, 27 Nov 2019 00:54:01 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a678a14e59551b487531e0347ba6ff428a70995ac2acc4ca363b747fed15d19`  
		Last Modified: Wed, 27 Nov 2019 00:54:01 GMT  
		Size: 4.0 KB (4005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0` - windows version 10.0.14393.3384; amd64

```console
$ docker pull mongo@sha256:330ad5ceaa1cd14aa1cb0455805a6deca5443c710c51f84fde39f641f4634a1c
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5809306075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c40c2e38d9e9f82c7ad2cf265f969a244aeef2a1a580329608c987438539357`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 15:47:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 23:07:06 GMT
ENV MONGO_VERSION=4.0.13
# Wed, 11 Dec 2019 23:07:07 GMT
ENV MONGO_DOWNLOAD_URL=https://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.13-signed.msi
# Wed, 11 Dec 2019 23:07:09 GMT
ENV MONGO_DOWNLOAD_SHA256=3d81d6214017e66343be94109aa36147a684be43b2731c37e52dd14518501ec0
# Wed, 11 Dec 2019 23:16:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Dec 2019 23:16:49 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Dec 2019 23:16:51 GMT
EXPOSE 27017
# Wed, 11 Dec 2019 23:16:52 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d23dffb4f7b6ebd1cceaac955d664d79467da76c4749d2a37d98556996d8bb0a`  
		Last Modified: Wed, 11 Dec 2019 18:01:38 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8484c162a97ee6791383e9fca96ce033068872b6112a193254938bab430897d4`  
		Last Modified: Thu, 12 Dec 2019 00:06:14 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b30553bdd94fae0eb4e8e8b3e38ab811bb4c8ac09d7e5b025293213cad0e53`  
		Last Modified: Thu, 12 Dec 2019 00:06:14 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:016b1abe1ab3b5c5c96597b1fe9964732d2c97f069e5fba0a83fb5a1d628f4b0`  
		Last Modified: Thu, 12 Dec 2019 00:06:12 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790eee007f25e4655a64d552a089ab2542b6916e4c115b3e4f589ed7357f07d6`  
		Last Modified: Thu, 12 Dec 2019 00:06:41 GMT  
		Size: 86.6 MB (86593791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96cb717f3e92ad0c4c894b9a76338096035b38cdbf6493d617da34a5f6c4748`  
		Last Modified: Thu, 12 Dec 2019 00:06:12 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:503292fe9ddd5fc1cae87fea71fc233de586e3fa6ce17806e20573c178985744`  
		Last Modified: Thu, 12 Dec 2019 00:06:12 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193ef3868851a73d4b10ef5ed9de6cf04364f1b53e6113f7a0112141d0a2c910`  
		Last Modified: Thu, 12 Dec 2019 00:06:12 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0` - windows version 10.0.17134.1184; amd64

```console
$ docker pull mongo@sha256:46dc0df09207a9e71508f9862d98e9e7fb668ccb4e6c3f28c6b8e925b4563bab
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2802868608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342deb9b0b80a2b6af5fc59ffeec43185124410ea7cda667e7b288f7d334bc03`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 12 Apr 2018 09:20:54 GMT
RUN Apply image 1803-RTM-amd64
# Wed, 04 Dec 2019 15:21:18 GMT
RUN Install update 1803-amd64
# Wed, 11 Dec 2019 15:36:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 23:17:13 GMT
ENV MONGO_VERSION=4.0.13
# Wed, 11 Dec 2019 23:17:14 GMT
ENV MONGO_DOWNLOAD_URL=https://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.13-signed.msi
# Wed, 11 Dec 2019 23:17:15 GMT
ENV MONGO_DOWNLOAD_SHA256=3d81d6214017e66343be94109aa36147a684be43b2731c37e52dd14518501ec0
# Wed, 11 Dec 2019 23:34:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Dec 2019 23:34:54 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Dec 2019 23:34:56 GMT
EXPOSE 27017
# Wed, 11 Dec 2019 23:34:57 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:d9e8b01179bfc94a5bdb1810fbd76b999aa52016001ace2d3a4c4bc7065a9601`  
		Last Modified: Tue, 18 Sep 2018 22:43:55 GMT  
		Size: 1.7 GB (1659688273 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d117323cd539488e5ef3bef575a41fa714d83119b0da1896607d96ec2a5e3b52`  
		Size: 696.9 MB (696873564 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:70c803815d644f3772896add8df055dfd33f5934921ca0c57efc290d42454abf`  
		Last Modified: Wed, 11 Dec 2019 18:00:43 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9cf07de65da1c9645e5c05214e9c4469214e13d07cb0524c52803d3eb38ed9`  
		Last Modified: Thu, 12 Dec 2019 00:07:08 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4548d3d297dcebf4b6aa4174311754dd620ab7008482038cf70c2324295438a`  
		Last Modified: Thu, 12 Dec 2019 00:07:08 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0faef6b4b77f63622a396f3195ac8d0b5b29d77cb69ade3002688710ffe72a8`  
		Last Modified: Thu, 12 Dec 2019 00:07:05 GMT  
		Size: 1.2 KB (1201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b34b2e676b51b294d0fdc43d409b91111ac8b407868908ede496edf2e17640`  
		Last Modified: Thu, 12 Dec 2019 00:08:12 GMT  
		Size: 446.3 MB (446298421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f222910d750b7b04baaf6c47d1909ccb4a4e3f1925314e81ffa55e0cedd7d14a`  
		Last Modified: Thu, 12 Dec 2019 00:07:05 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7e30ae2a2e5e08c7ca50abe1b3c2803557d5ea13a767d17ffe7981b3f588f3`  
		Last Modified: Thu, 12 Dec 2019 00:07:05 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ff2a06b59987f234c12bb12410a7d882e0e2b17a17c30da19d67f9ad52699c`  
		Last Modified: Thu, 12 Dec 2019 00:07:05 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.0.13`

```console
$ docker pull mongo@sha256:1aea2377c5b17dcd5e67d4c33f8f7ee09da62a4dd27ae988958b70efdf3a0a6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.14393.3384; amd64
	-	windows version 10.0.17134.1184; amd64

### `mongo:4.0.13` - linux; amd64

```console
$ docker pull mongo@sha256:f0397f249d2ced55ce59c7c50a8490ea536ffe4af4db75801f3443a380b7070a
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.3 MB (153327907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0712bd00d695f12ce3deac6f8425af7a782ee6c2bbb4697af7d94ba341c68ae7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 27 Nov 2019 00:22:54 GMT
ADD file:4eb02fc768cad452a37e8df30bbfcc728f3e6e7ca33af177fd4de06fd07c2098 in / 
# Wed, 27 Nov 2019 00:22:55 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 00:22:56 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 27 Nov 2019 00:22:56 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 27 Nov 2019 00:22:56 GMT
CMD ["/bin/bash"]
# Wed, 27 Nov 2019 02:02:59 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 27 Nov 2019 02:03:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 02:03:08 GMT
ENV GOSU_VERSION=1.11
# Wed, 27 Nov 2019 02:03:08 GMT
ENV JSYAML_VERSION=3.13.0
# Wed, 27 Nov 2019 02:03:19 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 27 Nov 2019 02:03:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 27 Nov 2019 02:04:20 GMT
ENV GPG_KEYS=9DA31620334BD75D9DCB49F368818C72E52529D4
# Wed, 27 Nov 2019 02:04:21 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 27 Nov 2019 02:04:21 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 27 Nov 2019 02:04:21 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 02:04:21 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 02:04:21 GMT
ENV MONGO_MAJOR=4.0
# Wed, 27 Nov 2019 02:04:22 GMT
ENV MONGO_VERSION=4.0.13
# Wed, 27 Nov 2019 02:04:22 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 27 Nov 2019 02:04:39 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 27 Nov 2019 02:04:40 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 27 Nov 2019 02:04:40 GMT
VOLUME [/data/db /data/configdb]
# Wed, 27 Nov 2019 02:04:40 GMT
COPY file:021686a669d0d1d1cbb99d6ca84ff8de10577b78ea985b8cdab9d75b347a3bd0 in /usr/local/bin/ 
# Wed, 27 Nov 2019 02:04:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2019 02:04:42 GMT
EXPOSE 27017
# Wed, 27 Nov 2019 02:04:43 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:976a760c94fcdd7d105269ae621e8269e7bb25a58c52ae667b4029a6bc7e33cb`  
		Last Modified: Sat, 09 Nov 2019 00:25:10 GMT  
		Size: 44.1 MB (44145376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c58992f3c37bb64aeba18910408cda9a7a63e212fe27e95065a8d54130ca5926`  
		Last Modified: Wed, 27 Nov 2019 00:23:39 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca0e5e7f12e6eb512246aea5579fcb771fe7203bc60944384d5cd7962f87ddb`  
		Last Modified: Wed, 27 Nov 2019 00:23:39 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a274cc00ca5f671b1740c43672dbc96504760cee585e7604029a3fe56854a8`  
		Last Modified: Wed, 27 Nov 2019 00:23:39 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6568107a703bb6b06323a98aa1b0b9269889582ed7bfca9784efda57e0f2e9`  
		Last Modified: Wed, 27 Nov 2019 02:05:02 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08957b2477b2c6d539baf4907363ed231b413902491c5cb985cbebe0c3ffe4dc`  
		Last Modified: Wed, 27 Nov 2019 02:05:01 GMT  
		Size: 2.9 MB (2946123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66dbd57d2a3b26381fcffa09bc1e01a2a010b2ea01432d43920927d44a8b2ac`  
		Last Modified: Wed, 27 Nov 2019 02:05:01 GMT  
		Size: 1.2 MB (1243858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135a9132a8625aee4a48702e5db9ea194db458f6109f490569fd5a85bad53b0c`  
		Last Modified: Wed, 27 Nov 2019 02:05:01 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b7c17ba1dfd1e6d1e81e53c7ec478aaa252cf71f763fccbf8ad0886f683d99`  
		Last Modified: Wed, 27 Nov 2019 02:05:48 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b595c9e65de00f4ca8af04db11e32dc5a88786cfb786b4b4a84fcec15c16ed9`  
		Last Modified: Wed, 27 Nov 2019 02:05:48 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e74b440cab6657354dc1f10c360db0d95b292793c03edc3c8d0c45e64a9009e`  
		Last Modified: Wed, 27 Nov 2019 02:06:05 GMT  
		Size: 105.0 MB (104983100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c04ed8f6ca08229e3b61f8daa67b49ba118a465c5d411927f726d4baf7437eb`  
		Last Modified: Wed, 27 Nov 2019 02:05:48 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dbe824121e4a60ac8c829dd487c52ce2fac50319e9d90b0dc5ad865e2640390`  
		Last Modified: Wed, 27 Nov 2019 02:05:48 GMT  
		Size: 4.0 KB (4007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0.13` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:f49ed701bb903cd709218404e56d372dfb9b03b536cd7754c7f80793666070a7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (143029158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dafb85d77371751edcf79ff34b7bebafc75415d082ad7d1369038c38bc71b569`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 26 Nov 2019 23:51:57 GMT
ADD file:2aa99efceecb520e73ba3c7dc167a4fbe6143ce5e9a6499e85dbc75935b3dfab in / 
# Tue, 26 Nov 2019 23:52:01 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 26 Nov 2019 23:52:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 26 Nov 2019 23:52:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 26 Nov 2019 23:52:06 GMT
CMD ["/bin/bash"]
# Wed, 27 Nov 2019 00:48:07 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 27 Nov 2019 00:48:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 00:48:27 GMT
ENV GOSU_VERSION=1.11
# Wed, 27 Nov 2019 00:48:28 GMT
ENV JSYAML_VERSION=3.13.0
# Wed, 27 Nov 2019 00:48:55 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 27 Nov 2019 00:48:57 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 27 Nov 2019 00:50:57 GMT
ENV GPG_KEYS=9DA31620334BD75D9DCB49F368818C72E52529D4
# Wed, 27 Nov 2019 00:51:02 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 27 Nov 2019 00:51:03 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 27 Nov 2019 00:51:04 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 00:51:06 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 00:51:10 GMT
ENV MONGO_MAJOR=4.0
# Wed, 27 Nov 2019 00:51:12 GMT
ENV MONGO_VERSION=4.0.13
# Wed, 27 Nov 2019 00:51:19 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 27 Nov 2019 00:52:07 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 27 Nov 2019 00:52:11 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 27 Nov 2019 00:52:12 GMT
VOLUME [/data/db /data/configdb]
# Wed, 27 Nov 2019 00:52:13 GMT
COPY file:021686a669d0d1d1cbb99d6ca84ff8de10577b78ea985b8cdab9d75b347a3bd0 in /usr/local/bin/ 
# Wed, 27 Nov 2019 00:52:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2019 00:52:15 GMT
EXPOSE 27017
# Wed, 27 Nov 2019 00:52:16 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:89276bd3590376dfedf96d27b310423c8a1d8c2fe92e4c5a2630aa704b1bb77f`  
		Last Modified: Mon, 11 Nov 2019 15:38:35 GMT  
		Size: 40.0 MB (39951577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a34d6b85b836a6bc6237d1912834f44592a792ab55d92f9ebe1d74973886c6`  
		Last Modified: Tue, 26 Nov 2019 23:52:51 GMT  
		Size: 470.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1bf847b434f33038cc426678c8640251706a59656ef4b0fec6fe3ba88854ab5`  
		Last Modified: Tue, 26 Nov 2019 23:52:51 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcbc4652a1718a263f7195a62c1ca8bf0117bcced50af01ac046bd164f523e5e`  
		Last Modified: Tue, 26 Nov 2019 23:52:51 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29654a2b453807f2a2ab77da919c90f470b457feb09082017c2db0cb659cbae8`  
		Last Modified: Wed, 27 Nov 2019 00:52:48 GMT  
		Size: 2.0 KB (2005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82801a5d252ba1ad5369119729d06933f6687427ec9b00ed3affee3d7d9e5a5b`  
		Last Modified: Wed, 27 Nov 2019 00:52:46 GMT  
		Size: 2.5 MB (2475016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32596fb594dee26ddc2fff00de483a10c3a1e9d0596d9e175424080fd13f6222`  
		Last Modified: Wed, 27 Nov 2019 00:52:46 GMT  
		Size: 1.2 MB (1170042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8df7b8db38cf122e5d4240be8c6a69443d07d574e37834d27d6a9316782df11`  
		Last Modified: Wed, 27 Nov 2019 00:52:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70b88de3f1a87007d7bccff5988808f14d2e9742aed390012fcccb4e6c30281`  
		Last Modified: Wed, 27 Nov 2019 00:54:01 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd55f9c2264e49984337fbf81be3647067592db952bc49fb7106b3f1eb40daa`  
		Last Modified: Wed, 27 Nov 2019 00:54:01 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df962447b3ce6cd904afde3cc1c9a3b0995ed98f88a8c1acb923721fdb6110a7`  
		Last Modified: Wed, 27 Nov 2019 00:54:39 GMT  
		Size: 99.4 MB (99423038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cde73bff8f9cd090b08b2b46cc3a82c3b4f1f8270437943a6205927efe3fb87`  
		Last Modified: Wed, 27 Nov 2019 00:54:01 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a678a14e59551b487531e0347ba6ff428a70995ac2acc4ca363b747fed15d19`  
		Last Modified: Wed, 27 Nov 2019 00:54:01 GMT  
		Size: 4.0 KB (4005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0.13` - windows version 10.0.14393.3384; amd64

```console
$ docker pull mongo@sha256:330ad5ceaa1cd14aa1cb0455805a6deca5443c710c51f84fde39f641f4634a1c
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5809306075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c40c2e38d9e9f82c7ad2cf265f969a244aeef2a1a580329608c987438539357`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 15:47:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 23:07:06 GMT
ENV MONGO_VERSION=4.0.13
# Wed, 11 Dec 2019 23:07:07 GMT
ENV MONGO_DOWNLOAD_URL=https://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.13-signed.msi
# Wed, 11 Dec 2019 23:07:09 GMT
ENV MONGO_DOWNLOAD_SHA256=3d81d6214017e66343be94109aa36147a684be43b2731c37e52dd14518501ec0
# Wed, 11 Dec 2019 23:16:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Dec 2019 23:16:49 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Dec 2019 23:16:51 GMT
EXPOSE 27017
# Wed, 11 Dec 2019 23:16:52 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d23dffb4f7b6ebd1cceaac955d664d79467da76c4749d2a37d98556996d8bb0a`  
		Last Modified: Wed, 11 Dec 2019 18:01:38 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8484c162a97ee6791383e9fca96ce033068872b6112a193254938bab430897d4`  
		Last Modified: Thu, 12 Dec 2019 00:06:14 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b30553bdd94fae0eb4e8e8b3e38ab811bb4c8ac09d7e5b025293213cad0e53`  
		Last Modified: Thu, 12 Dec 2019 00:06:14 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:016b1abe1ab3b5c5c96597b1fe9964732d2c97f069e5fba0a83fb5a1d628f4b0`  
		Last Modified: Thu, 12 Dec 2019 00:06:12 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790eee007f25e4655a64d552a089ab2542b6916e4c115b3e4f589ed7357f07d6`  
		Last Modified: Thu, 12 Dec 2019 00:06:41 GMT  
		Size: 86.6 MB (86593791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96cb717f3e92ad0c4c894b9a76338096035b38cdbf6493d617da34a5f6c4748`  
		Last Modified: Thu, 12 Dec 2019 00:06:12 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:503292fe9ddd5fc1cae87fea71fc233de586e3fa6ce17806e20573c178985744`  
		Last Modified: Thu, 12 Dec 2019 00:06:12 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193ef3868851a73d4b10ef5ed9de6cf04364f1b53e6113f7a0112141d0a2c910`  
		Last Modified: Thu, 12 Dec 2019 00:06:12 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0.13` - windows version 10.0.17134.1184; amd64

```console
$ docker pull mongo@sha256:46dc0df09207a9e71508f9862d98e9e7fb668ccb4e6c3f28c6b8e925b4563bab
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2802868608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342deb9b0b80a2b6af5fc59ffeec43185124410ea7cda667e7b288f7d334bc03`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 12 Apr 2018 09:20:54 GMT
RUN Apply image 1803-RTM-amd64
# Wed, 04 Dec 2019 15:21:18 GMT
RUN Install update 1803-amd64
# Wed, 11 Dec 2019 15:36:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 23:17:13 GMT
ENV MONGO_VERSION=4.0.13
# Wed, 11 Dec 2019 23:17:14 GMT
ENV MONGO_DOWNLOAD_URL=https://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.13-signed.msi
# Wed, 11 Dec 2019 23:17:15 GMT
ENV MONGO_DOWNLOAD_SHA256=3d81d6214017e66343be94109aa36147a684be43b2731c37e52dd14518501ec0
# Wed, 11 Dec 2019 23:34:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Dec 2019 23:34:54 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Dec 2019 23:34:56 GMT
EXPOSE 27017
# Wed, 11 Dec 2019 23:34:57 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:d9e8b01179bfc94a5bdb1810fbd76b999aa52016001ace2d3a4c4bc7065a9601`  
		Last Modified: Tue, 18 Sep 2018 22:43:55 GMT  
		Size: 1.7 GB (1659688273 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d117323cd539488e5ef3bef575a41fa714d83119b0da1896607d96ec2a5e3b52`  
		Size: 696.9 MB (696873564 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:70c803815d644f3772896add8df055dfd33f5934921ca0c57efc290d42454abf`  
		Last Modified: Wed, 11 Dec 2019 18:00:43 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9cf07de65da1c9645e5c05214e9c4469214e13d07cb0524c52803d3eb38ed9`  
		Last Modified: Thu, 12 Dec 2019 00:07:08 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4548d3d297dcebf4b6aa4174311754dd620ab7008482038cf70c2324295438a`  
		Last Modified: Thu, 12 Dec 2019 00:07:08 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0faef6b4b77f63622a396f3195ac8d0b5b29d77cb69ade3002688710ffe72a8`  
		Last Modified: Thu, 12 Dec 2019 00:07:05 GMT  
		Size: 1.2 KB (1201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b34b2e676b51b294d0fdc43d409b91111ac8b407868908ede496edf2e17640`  
		Last Modified: Thu, 12 Dec 2019 00:08:12 GMT  
		Size: 446.3 MB (446298421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f222910d750b7b04baaf6c47d1909ccb4a4e3f1925314e81ffa55e0cedd7d14a`  
		Last Modified: Thu, 12 Dec 2019 00:07:05 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7e30ae2a2e5e08c7ca50abe1b3c2803557d5ea13a767d17ffe7981b3f588f3`  
		Last Modified: Thu, 12 Dec 2019 00:07:05 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ff2a06b59987f234c12bb12410a7d882e0e2b17a17c30da19d67f9ad52699c`  
		Last Modified: Thu, 12 Dec 2019 00:07:05 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.0.13-windowsservercore`

```console
$ docker pull mongo@sha256:25aad1229d02676b1e14e4460925d828b571c12fabe91bba2a450685082c4b5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3384; amd64
	-	windows version 10.0.17134.1184; amd64

### `mongo:4.0.13-windowsservercore` - windows version 10.0.14393.3384; amd64

```console
$ docker pull mongo@sha256:330ad5ceaa1cd14aa1cb0455805a6deca5443c710c51f84fde39f641f4634a1c
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5809306075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c40c2e38d9e9f82c7ad2cf265f969a244aeef2a1a580329608c987438539357`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 15:47:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 23:07:06 GMT
ENV MONGO_VERSION=4.0.13
# Wed, 11 Dec 2019 23:07:07 GMT
ENV MONGO_DOWNLOAD_URL=https://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.13-signed.msi
# Wed, 11 Dec 2019 23:07:09 GMT
ENV MONGO_DOWNLOAD_SHA256=3d81d6214017e66343be94109aa36147a684be43b2731c37e52dd14518501ec0
# Wed, 11 Dec 2019 23:16:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Dec 2019 23:16:49 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Dec 2019 23:16:51 GMT
EXPOSE 27017
# Wed, 11 Dec 2019 23:16:52 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d23dffb4f7b6ebd1cceaac955d664d79467da76c4749d2a37d98556996d8bb0a`  
		Last Modified: Wed, 11 Dec 2019 18:01:38 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8484c162a97ee6791383e9fca96ce033068872b6112a193254938bab430897d4`  
		Last Modified: Thu, 12 Dec 2019 00:06:14 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b30553bdd94fae0eb4e8e8b3e38ab811bb4c8ac09d7e5b025293213cad0e53`  
		Last Modified: Thu, 12 Dec 2019 00:06:14 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:016b1abe1ab3b5c5c96597b1fe9964732d2c97f069e5fba0a83fb5a1d628f4b0`  
		Last Modified: Thu, 12 Dec 2019 00:06:12 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790eee007f25e4655a64d552a089ab2542b6916e4c115b3e4f589ed7357f07d6`  
		Last Modified: Thu, 12 Dec 2019 00:06:41 GMT  
		Size: 86.6 MB (86593791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96cb717f3e92ad0c4c894b9a76338096035b38cdbf6493d617da34a5f6c4748`  
		Last Modified: Thu, 12 Dec 2019 00:06:12 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:503292fe9ddd5fc1cae87fea71fc233de586e3fa6ce17806e20573c178985744`  
		Last Modified: Thu, 12 Dec 2019 00:06:12 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193ef3868851a73d4b10ef5ed9de6cf04364f1b53e6113f7a0112141d0a2c910`  
		Last Modified: Thu, 12 Dec 2019 00:06:12 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0.13-windowsservercore` - windows version 10.0.17134.1184; amd64

```console
$ docker pull mongo@sha256:46dc0df09207a9e71508f9862d98e9e7fb668ccb4e6c3f28c6b8e925b4563bab
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2802868608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342deb9b0b80a2b6af5fc59ffeec43185124410ea7cda667e7b288f7d334bc03`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 12 Apr 2018 09:20:54 GMT
RUN Apply image 1803-RTM-amd64
# Wed, 04 Dec 2019 15:21:18 GMT
RUN Install update 1803-amd64
# Wed, 11 Dec 2019 15:36:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 23:17:13 GMT
ENV MONGO_VERSION=4.0.13
# Wed, 11 Dec 2019 23:17:14 GMT
ENV MONGO_DOWNLOAD_URL=https://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.13-signed.msi
# Wed, 11 Dec 2019 23:17:15 GMT
ENV MONGO_DOWNLOAD_SHA256=3d81d6214017e66343be94109aa36147a684be43b2731c37e52dd14518501ec0
# Wed, 11 Dec 2019 23:34:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Dec 2019 23:34:54 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Dec 2019 23:34:56 GMT
EXPOSE 27017
# Wed, 11 Dec 2019 23:34:57 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:d9e8b01179bfc94a5bdb1810fbd76b999aa52016001ace2d3a4c4bc7065a9601`  
		Last Modified: Tue, 18 Sep 2018 22:43:55 GMT  
		Size: 1.7 GB (1659688273 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d117323cd539488e5ef3bef575a41fa714d83119b0da1896607d96ec2a5e3b52`  
		Size: 696.9 MB (696873564 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:70c803815d644f3772896add8df055dfd33f5934921ca0c57efc290d42454abf`  
		Last Modified: Wed, 11 Dec 2019 18:00:43 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9cf07de65da1c9645e5c05214e9c4469214e13d07cb0524c52803d3eb38ed9`  
		Last Modified: Thu, 12 Dec 2019 00:07:08 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4548d3d297dcebf4b6aa4174311754dd620ab7008482038cf70c2324295438a`  
		Last Modified: Thu, 12 Dec 2019 00:07:08 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0faef6b4b77f63622a396f3195ac8d0b5b29d77cb69ade3002688710ffe72a8`  
		Last Modified: Thu, 12 Dec 2019 00:07:05 GMT  
		Size: 1.2 KB (1201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b34b2e676b51b294d0fdc43d409b91111ac8b407868908ede496edf2e17640`  
		Last Modified: Thu, 12 Dec 2019 00:08:12 GMT  
		Size: 446.3 MB (446298421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f222910d750b7b04baaf6c47d1909ccb4a4e3f1925314e81ffa55e0cedd7d14a`  
		Last Modified: Thu, 12 Dec 2019 00:07:05 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7e30ae2a2e5e08c7ca50abe1b3c2803557d5ea13a767d17ffe7981b3f588f3`  
		Last Modified: Thu, 12 Dec 2019 00:07:05 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ff2a06b59987f234c12bb12410a7d882e0e2b17a17c30da19d67f9ad52699c`  
		Last Modified: Thu, 12 Dec 2019 00:07:05 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.0.13-windowsservercore-1809`

```console
$ docker pull mongo@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:

## `mongo:4.0.13-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:88512bbbcaf78f65528b014cb2cfe3ba289650b1d1313708003898dfb4496226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3384; amd64

### `mongo:4.0.13-windowsservercore-ltsc2016` - windows version 10.0.14393.3384; amd64

```console
$ docker pull mongo@sha256:330ad5ceaa1cd14aa1cb0455805a6deca5443c710c51f84fde39f641f4634a1c
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5809306075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c40c2e38d9e9f82c7ad2cf265f969a244aeef2a1a580329608c987438539357`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 15:47:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 23:07:06 GMT
ENV MONGO_VERSION=4.0.13
# Wed, 11 Dec 2019 23:07:07 GMT
ENV MONGO_DOWNLOAD_URL=https://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.13-signed.msi
# Wed, 11 Dec 2019 23:07:09 GMT
ENV MONGO_DOWNLOAD_SHA256=3d81d6214017e66343be94109aa36147a684be43b2731c37e52dd14518501ec0
# Wed, 11 Dec 2019 23:16:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Dec 2019 23:16:49 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Dec 2019 23:16:51 GMT
EXPOSE 27017
# Wed, 11 Dec 2019 23:16:52 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d23dffb4f7b6ebd1cceaac955d664d79467da76c4749d2a37d98556996d8bb0a`  
		Last Modified: Wed, 11 Dec 2019 18:01:38 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8484c162a97ee6791383e9fca96ce033068872b6112a193254938bab430897d4`  
		Last Modified: Thu, 12 Dec 2019 00:06:14 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b30553bdd94fae0eb4e8e8b3e38ab811bb4c8ac09d7e5b025293213cad0e53`  
		Last Modified: Thu, 12 Dec 2019 00:06:14 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:016b1abe1ab3b5c5c96597b1fe9964732d2c97f069e5fba0a83fb5a1d628f4b0`  
		Last Modified: Thu, 12 Dec 2019 00:06:12 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790eee007f25e4655a64d552a089ab2542b6916e4c115b3e4f589ed7357f07d6`  
		Last Modified: Thu, 12 Dec 2019 00:06:41 GMT  
		Size: 86.6 MB (86593791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96cb717f3e92ad0c4c894b9a76338096035b38cdbf6493d617da34a5f6c4748`  
		Last Modified: Thu, 12 Dec 2019 00:06:12 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:503292fe9ddd5fc1cae87fea71fc233de586e3fa6ce17806e20573c178985744`  
		Last Modified: Thu, 12 Dec 2019 00:06:12 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193ef3868851a73d4b10ef5ed9de6cf04364f1b53e6113f7a0112141d0a2c910`  
		Last Modified: Thu, 12 Dec 2019 00:06:12 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.0.13-xenial`

```console
$ docker pull mongo@sha256:9ef751ff0bf7249b0673a27f90b8d755fbe93693e12188406635821ba760a423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:4.0.13-xenial` - linux; amd64

```console
$ docker pull mongo@sha256:f0397f249d2ced55ce59c7c50a8490ea536ffe4af4db75801f3443a380b7070a
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.3 MB (153327907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0712bd00d695f12ce3deac6f8425af7a782ee6c2bbb4697af7d94ba341c68ae7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 27 Nov 2019 00:22:54 GMT
ADD file:4eb02fc768cad452a37e8df30bbfcc728f3e6e7ca33af177fd4de06fd07c2098 in / 
# Wed, 27 Nov 2019 00:22:55 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 00:22:56 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 27 Nov 2019 00:22:56 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 27 Nov 2019 00:22:56 GMT
CMD ["/bin/bash"]
# Wed, 27 Nov 2019 02:02:59 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 27 Nov 2019 02:03:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 02:03:08 GMT
ENV GOSU_VERSION=1.11
# Wed, 27 Nov 2019 02:03:08 GMT
ENV JSYAML_VERSION=3.13.0
# Wed, 27 Nov 2019 02:03:19 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 27 Nov 2019 02:03:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 27 Nov 2019 02:04:20 GMT
ENV GPG_KEYS=9DA31620334BD75D9DCB49F368818C72E52529D4
# Wed, 27 Nov 2019 02:04:21 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 27 Nov 2019 02:04:21 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 27 Nov 2019 02:04:21 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 02:04:21 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 02:04:21 GMT
ENV MONGO_MAJOR=4.0
# Wed, 27 Nov 2019 02:04:22 GMT
ENV MONGO_VERSION=4.0.13
# Wed, 27 Nov 2019 02:04:22 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 27 Nov 2019 02:04:39 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 27 Nov 2019 02:04:40 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 27 Nov 2019 02:04:40 GMT
VOLUME [/data/db /data/configdb]
# Wed, 27 Nov 2019 02:04:40 GMT
COPY file:021686a669d0d1d1cbb99d6ca84ff8de10577b78ea985b8cdab9d75b347a3bd0 in /usr/local/bin/ 
# Wed, 27 Nov 2019 02:04:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2019 02:04:42 GMT
EXPOSE 27017
# Wed, 27 Nov 2019 02:04:43 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:976a760c94fcdd7d105269ae621e8269e7bb25a58c52ae667b4029a6bc7e33cb`  
		Last Modified: Sat, 09 Nov 2019 00:25:10 GMT  
		Size: 44.1 MB (44145376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c58992f3c37bb64aeba18910408cda9a7a63e212fe27e95065a8d54130ca5926`  
		Last Modified: Wed, 27 Nov 2019 00:23:39 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca0e5e7f12e6eb512246aea5579fcb771fe7203bc60944384d5cd7962f87ddb`  
		Last Modified: Wed, 27 Nov 2019 00:23:39 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a274cc00ca5f671b1740c43672dbc96504760cee585e7604029a3fe56854a8`  
		Last Modified: Wed, 27 Nov 2019 00:23:39 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6568107a703bb6b06323a98aa1b0b9269889582ed7bfca9784efda57e0f2e9`  
		Last Modified: Wed, 27 Nov 2019 02:05:02 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08957b2477b2c6d539baf4907363ed231b413902491c5cb985cbebe0c3ffe4dc`  
		Last Modified: Wed, 27 Nov 2019 02:05:01 GMT  
		Size: 2.9 MB (2946123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66dbd57d2a3b26381fcffa09bc1e01a2a010b2ea01432d43920927d44a8b2ac`  
		Last Modified: Wed, 27 Nov 2019 02:05:01 GMT  
		Size: 1.2 MB (1243858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135a9132a8625aee4a48702e5db9ea194db458f6109f490569fd5a85bad53b0c`  
		Last Modified: Wed, 27 Nov 2019 02:05:01 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b7c17ba1dfd1e6d1e81e53c7ec478aaa252cf71f763fccbf8ad0886f683d99`  
		Last Modified: Wed, 27 Nov 2019 02:05:48 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b595c9e65de00f4ca8af04db11e32dc5a88786cfb786b4b4a84fcec15c16ed9`  
		Last Modified: Wed, 27 Nov 2019 02:05:48 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e74b440cab6657354dc1f10c360db0d95b292793c03edc3c8d0c45e64a9009e`  
		Last Modified: Wed, 27 Nov 2019 02:06:05 GMT  
		Size: 105.0 MB (104983100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c04ed8f6ca08229e3b61f8daa67b49ba118a465c5d411927f726d4baf7437eb`  
		Last Modified: Wed, 27 Nov 2019 02:05:48 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dbe824121e4a60ac8c829dd487c52ce2fac50319e9d90b0dc5ad865e2640390`  
		Last Modified: Wed, 27 Nov 2019 02:05:48 GMT  
		Size: 4.0 KB (4007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0.13-xenial` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:f49ed701bb903cd709218404e56d372dfb9b03b536cd7754c7f80793666070a7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (143029158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dafb85d77371751edcf79ff34b7bebafc75415d082ad7d1369038c38bc71b569`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 26 Nov 2019 23:51:57 GMT
ADD file:2aa99efceecb520e73ba3c7dc167a4fbe6143ce5e9a6499e85dbc75935b3dfab in / 
# Tue, 26 Nov 2019 23:52:01 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 26 Nov 2019 23:52:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 26 Nov 2019 23:52:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 26 Nov 2019 23:52:06 GMT
CMD ["/bin/bash"]
# Wed, 27 Nov 2019 00:48:07 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 27 Nov 2019 00:48:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 00:48:27 GMT
ENV GOSU_VERSION=1.11
# Wed, 27 Nov 2019 00:48:28 GMT
ENV JSYAML_VERSION=3.13.0
# Wed, 27 Nov 2019 00:48:55 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 27 Nov 2019 00:48:57 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 27 Nov 2019 00:50:57 GMT
ENV GPG_KEYS=9DA31620334BD75D9DCB49F368818C72E52529D4
# Wed, 27 Nov 2019 00:51:02 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 27 Nov 2019 00:51:03 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 27 Nov 2019 00:51:04 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 00:51:06 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 00:51:10 GMT
ENV MONGO_MAJOR=4.0
# Wed, 27 Nov 2019 00:51:12 GMT
ENV MONGO_VERSION=4.0.13
# Wed, 27 Nov 2019 00:51:19 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 27 Nov 2019 00:52:07 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 27 Nov 2019 00:52:11 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 27 Nov 2019 00:52:12 GMT
VOLUME [/data/db /data/configdb]
# Wed, 27 Nov 2019 00:52:13 GMT
COPY file:021686a669d0d1d1cbb99d6ca84ff8de10577b78ea985b8cdab9d75b347a3bd0 in /usr/local/bin/ 
# Wed, 27 Nov 2019 00:52:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2019 00:52:15 GMT
EXPOSE 27017
# Wed, 27 Nov 2019 00:52:16 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:89276bd3590376dfedf96d27b310423c8a1d8c2fe92e4c5a2630aa704b1bb77f`  
		Last Modified: Mon, 11 Nov 2019 15:38:35 GMT  
		Size: 40.0 MB (39951577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a34d6b85b836a6bc6237d1912834f44592a792ab55d92f9ebe1d74973886c6`  
		Last Modified: Tue, 26 Nov 2019 23:52:51 GMT  
		Size: 470.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1bf847b434f33038cc426678c8640251706a59656ef4b0fec6fe3ba88854ab5`  
		Last Modified: Tue, 26 Nov 2019 23:52:51 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcbc4652a1718a263f7195a62c1ca8bf0117bcced50af01ac046bd164f523e5e`  
		Last Modified: Tue, 26 Nov 2019 23:52:51 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29654a2b453807f2a2ab77da919c90f470b457feb09082017c2db0cb659cbae8`  
		Last Modified: Wed, 27 Nov 2019 00:52:48 GMT  
		Size: 2.0 KB (2005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82801a5d252ba1ad5369119729d06933f6687427ec9b00ed3affee3d7d9e5a5b`  
		Last Modified: Wed, 27 Nov 2019 00:52:46 GMT  
		Size: 2.5 MB (2475016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32596fb594dee26ddc2fff00de483a10c3a1e9d0596d9e175424080fd13f6222`  
		Last Modified: Wed, 27 Nov 2019 00:52:46 GMT  
		Size: 1.2 MB (1170042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8df7b8db38cf122e5d4240be8c6a69443d07d574e37834d27d6a9316782df11`  
		Last Modified: Wed, 27 Nov 2019 00:52:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70b88de3f1a87007d7bccff5988808f14d2e9742aed390012fcccb4e6c30281`  
		Last Modified: Wed, 27 Nov 2019 00:54:01 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd55f9c2264e49984337fbf81be3647067592db952bc49fb7106b3f1eb40daa`  
		Last Modified: Wed, 27 Nov 2019 00:54:01 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df962447b3ce6cd904afde3cc1c9a3b0995ed98f88a8c1acb923721fdb6110a7`  
		Last Modified: Wed, 27 Nov 2019 00:54:39 GMT  
		Size: 99.4 MB (99423038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cde73bff8f9cd090b08b2b46cc3a82c3b4f1f8270437943a6205927efe3fb87`  
		Last Modified: Wed, 27 Nov 2019 00:54:01 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a678a14e59551b487531e0347ba6ff428a70995ac2acc4ca363b747fed15d19`  
		Last Modified: Wed, 27 Nov 2019 00:54:01 GMT  
		Size: 4.0 KB (4005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.0-windowsservercore`

```console
$ docker pull mongo@sha256:25aad1229d02676b1e14e4460925d828b571c12fabe91bba2a450685082c4b5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3384; amd64
	-	windows version 10.0.17134.1184; amd64

### `mongo:4.0-windowsservercore` - windows version 10.0.14393.3384; amd64

```console
$ docker pull mongo@sha256:330ad5ceaa1cd14aa1cb0455805a6deca5443c710c51f84fde39f641f4634a1c
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5809306075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c40c2e38d9e9f82c7ad2cf265f969a244aeef2a1a580329608c987438539357`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 15:47:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 23:07:06 GMT
ENV MONGO_VERSION=4.0.13
# Wed, 11 Dec 2019 23:07:07 GMT
ENV MONGO_DOWNLOAD_URL=https://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.13-signed.msi
# Wed, 11 Dec 2019 23:07:09 GMT
ENV MONGO_DOWNLOAD_SHA256=3d81d6214017e66343be94109aa36147a684be43b2731c37e52dd14518501ec0
# Wed, 11 Dec 2019 23:16:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Dec 2019 23:16:49 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Dec 2019 23:16:51 GMT
EXPOSE 27017
# Wed, 11 Dec 2019 23:16:52 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d23dffb4f7b6ebd1cceaac955d664d79467da76c4749d2a37d98556996d8bb0a`  
		Last Modified: Wed, 11 Dec 2019 18:01:38 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8484c162a97ee6791383e9fca96ce033068872b6112a193254938bab430897d4`  
		Last Modified: Thu, 12 Dec 2019 00:06:14 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b30553bdd94fae0eb4e8e8b3e38ab811bb4c8ac09d7e5b025293213cad0e53`  
		Last Modified: Thu, 12 Dec 2019 00:06:14 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:016b1abe1ab3b5c5c96597b1fe9964732d2c97f069e5fba0a83fb5a1d628f4b0`  
		Last Modified: Thu, 12 Dec 2019 00:06:12 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790eee007f25e4655a64d552a089ab2542b6916e4c115b3e4f589ed7357f07d6`  
		Last Modified: Thu, 12 Dec 2019 00:06:41 GMT  
		Size: 86.6 MB (86593791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96cb717f3e92ad0c4c894b9a76338096035b38cdbf6493d617da34a5f6c4748`  
		Last Modified: Thu, 12 Dec 2019 00:06:12 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:503292fe9ddd5fc1cae87fea71fc233de586e3fa6ce17806e20573c178985744`  
		Last Modified: Thu, 12 Dec 2019 00:06:12 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193ef3868851a73d4b10ef5ed9de6cf04364f1b53e6113f7a0112141d0a2c910`  
		Last Modified: Thu, 12 Dec 2019 00:06:12 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0-windowsservercore` - windows version 10.0.17134.1184; amd64

```console
$ docker pull mongo@sha256:46dc0df09207a9e71508f9862d98e9e7fb668ccb4e6c3f28c6b8e925b4563bab
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2802868608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342deb9b0b80a2b6af5fc59ffeec43185124410ea7cda667e7b288f7d334bc03`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 12 Apr 2018 09:20:54 GMT
RUN Apply image 1803-RTM-amd64
# Wed, 04 Dec 2019 15:21:18 GMT
RUN Install update 1803-amd64
# Wed, 11 Dec 2019 15:36:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 23:17:13 GMT
ENV MONGO_VERSION=4.0.13
# Wed, 11 Dec 2019 23:17:14 GMT
ENV MONGO_DOWNLOAD_URL=https://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.13-signed.msi
# Wed, 11 Dec 2019 23:17:15 GMT
ENV MONGO_DOWNLOAD_SHA256=3d81d6214017e66343be94109aa36147a684be43b2731c37e52dd14518501ec0
# Wed, 11 Dec 2019 23:34:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Dec 2019 23:34:54 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Dec 2019 23:34:56 GMT
EXPOSE 27017
# Wed, 11 Dec 2019 23:34:57 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:d9e8b01179bfc94a5bdb1810fbd76b999aa52016001ace2d3a4c4bc7065a9601`  
		Last Modified: Tue, 18 Sep 2018 22:43:55 GMT  
		Size: 1.7 GB (1659688273 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d117323cd539488e5ef3bef575a41fa714d83119b0da1896607d96ec2a5e3b52`  
		Size: 696.9 MB (696873564 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:70c803815d644f3772896add8df055dfd33f5934921ca0c57efc290d42454abf`  
		Last Modified: Wed, 11 Dec 2019 18:00:43 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9cf07de65da1c9645e5c05214e9c4469214e13d07cb0524c52803d3eb38ed9`  
		Last Modified: Thu, 12 Dec 2019 00:07:08 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4548d3d297dcebf4b6aa4174311754dd620ab7008482038cf70c2324295438a`  
		Last Modified: Thu, 12 Dec 2019 00:07:08 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0faef6b4b77f63622a396f3195ac8d0b5b29d77cb69ade3002688710ffe72a8`  
		Last Modified: Thu, 12 Dec 2019 00:07:05 GMT  
		Size: 1.2 KB (1201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b34b2e676b51b294d0fdc43d409b91111ac8b407868908ede496edf2e17640`  
		Last Modified: Thu, 12 Dec 2019 00:08:12 GMT  
		Size: 446.3 MB (446298421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f222910d750b7b04baaf6c47d1909ccb4a4e3f1925314e81ffa55e0cedd7d14a`  
		Last Modified: Thu, 12 Dec 2019 00:07:05 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7e30ae2a2e5e08c7ca50abe1b3c2803557d5ea13a767d17ffe7981b3f588f3`  
		Last Modified: Thu, 12 Dec 2019 00:07:05 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ff2a06b59987f234c12bb12410a7d882e0e2b17a17c30da19d67f9ad52699c`  
		Last Modified: Thu, 12 Dec 2019 00:07:05 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.0-windowsservercore-1809`

```console
$ docker pull mongo@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:

## `mongo:4.0-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:88512bbbcaf78f65528b014cb2cfe3ba289650b1d1313708003898dfb4496226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3384; amd64

### `mongo:4.0-windowsservercore-ltsc2016` - windows version 10.0.14393.3384; amd64

```console
$ docker pull mongo@sha256:330ad5ceaa1cd14aa1cb0455805a6deca5443c710c51f84fde39f641f4634a1c
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5809306075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c40c2e38d9e9f82c7ad2cf265f969a244aeef2a1a580329608c987438539357`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 15:47:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 23:07:06 GMT
ENV MONGO_VERSION=4.0.13
# Wed, 11 Dec 2019 23:07:07 GMT
ENV MONGO_DOWNLOAD_URL=https://downloads.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.13-signed.msi
# Wed, 11 Dec 2019 23:07:09 GMT
ENV MONGO_DOWNLOAD_SHA256=3d81d6214017e66343be94109aa36147a684be43b2731c37e52dd14518501ec0
# Wed, 11 Dec 2019 23:16:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Dec 2019 23:16:49 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Dec 2019 23:16:51 GMT
EXPOSE 27017
# Wed, 11 Dec 2019 23:16:52 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d23dffb4f7b6ebd1cceaac955d664d79467da76c4749d2a37d98556996d8bb0a`  
		Last Modified: Wed, 11 Dec 2019 18:01:38 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8484c162a97ee6791383e9fca96ce033068872b6112a193254938bab430897d4`  
		Last Modified: Thu, 12 Dec 2019 00:06:14 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b30553bdd94fae0eb4e8e8b3e38ab811bb4c8ac09d7e5b025293213cad0e53`  
		Last Modified: Thu, 12 Dec 2019 00:06:14 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:016b1abe1ab3b5c5c96597b1fe9964732d2c97f069e5fba0a83fb5a1d628f4b0`  
		Last Modified: Thu, 12 Dec 2019 00:06:12 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790eee007f25e4655a64d552a089ab2542b6916e4c115b3e4f589ed7357f07d6`  
		Last Modified: Thu, 12 Dec 2019 00:06:41 GMT  
		Size: 86.6 MB (86593791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96cb717f3e92ad0c4c894b9a76338096035b38cdbf6493d617da34a5f6c4748`  
		Last Modified: Thu, 12 Dec 2019 00:06:12 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:503292fe9ddd5fc1cae87fea71fc233de586e3fa6ce17806e20573c178985744`  
		Last Modified: Thu, 12 Dec 2019 00:06:12 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193ef3868851a73d4b10ef5ed9de6cf04364f1b53e6113f7a0112141d0a2c910`  
		Last Modified: Thu, 12 Dec 2019 00:06:12 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.0-xenial`

```console
$ docker pull mongo@sha256:9ef751ff0bf7249b0673a27f90b8d755fbe93693e12188406635821ba760a423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:4.0-xenial` - linux; amd64

```console
$ docker pull mongo@sha256:f0397f249d2ced55ce59c7c50a8490ea536ffe4af4db75801f3443a380b7070a
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.3 MB (153327907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0712bd00d695f12ce3deac6f8425af7a782ee6c2bbb4697af7d94ba341c68ae7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 27 Nov 2019 00:22:54 GMT
ADD file:4eb02fc768cad452a37e8df30bbfcc728f3e6e7ca33af177fd4de06fd07c2098 in / 
# Wed, 27 Nov 2019 00:22:55 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 00:22:56 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 27 Nov 2019 00:22:56 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 27 Nov 2019 00:22:56 GMT
CMD ["/bin/bash"]
# Wed, 27 Nov 2019 02:02:59 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 27 Nov 2019 02:03:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 02:03:08 GMT
ENV GOSU_VERSION=1.11
# Wed, 27 Nov 2019 02:03:08 GMT
ENV JSYAML_VERSION=3.13.0
# Wed, 27 Nov 2019 02:03:19 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 27 Nov 2019 02:03:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 27 Nov 2019 02:04:20 GMT
ENV GPG_KEYS=9DA31620334BD75D9DCB49F368818C72E52529D4
# Wed, 27 Nov 2019 02:04:21 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 27 Nov 2019 02:04:21 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 27 Nov 2019 02:04:21 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 02:04:21 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 02:04:21 GMT
ENV MONGO_MAJOR=4.0
# Wed, 27 Nov 2019 02:04:22 GMT
ENV MONGO_VERSION=4.0.13
# Wed, 27 Nov 2019 02:04:22 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 27 Nov 2019 02:04:39 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 27 Nov 2019 02:04:40 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 27 Nov 2019 02:04:40 GMT
VOLUME [/data/db /data/configdb]
# Wed, 27 Nov 2019 02:04:40 GMT
COPY file:021686a669d0d1d1cbb99d6ca84ff8de10577b78ea985b8cdab9d75b347a3bd0 in /usr/local/bin/ 
# Wed, 27 Nov 2019 02:04:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2019 02:04:42 GMT
EXPOSE 27017
# Wed, 27 Nov 2019 02:04:43 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:976a760c94fcdd7d105269ae621e8269e7bb25a58c52ae667b4029a6bc7e33cb`  
		Last Modified: Sat, 09 Nov 2019 00:25:10 GMT  
		Size: 44.1 MB (44145376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c58992f3c37bb64aeba18910408cda9a7a63e212fe27e95065a8d54130ca5926`  
		Last Modified: Wed, 27 Nov 2019 00:23:39 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca0e5e7f12e6eb512246aea5579fcb771fe7203bc60944384d5cd7962f87ddb`  
		Last Modified: Wed, 27 Nov 2019 00:23:39 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a274cc00ca5f671b1740c43672dbc96504760cee585e7604029a3fe56854a8`  
		Last Modified: Wed, 27 Nov 2019 00:23:39 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6568107a703bb6b06323a98aa1b0b9269889582ed7bfca9784efda57e0f2e9`  
		Last Modified: Wed, 27 Nov 2019 02:05:02 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08957b2477b2c6d539baf4907363ed231b413902491c5cb985cbebe0c3ffe4dc`  
		Last Modified: Wed, 27 Nov 2019 02:05:01 GMT  
		Size: 2.9 MB (2946123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66dbd57d2a3b26381fcffa09bc1e01a2a010b2ea01432d43920927d44a8b2ac`  
		Last Modified: Wed, 27 Nov 2019 02:05:01 GMT  
		Size: 1.2 MB (1243858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135a9132a8625aee4a48702e5db9ea194db458f6109f490569fd5a85bad53b0c`  
		Last Modified: Wed, 27 Nov 2019 02:05:01 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b7c17ba1dfd1e6d1e81e53c7ec478aaa252cf71f763fccbf8ad0886f683d99`  
		Last Modified: Wed, 27 Nov 2019 02:05:48 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b595c9e65de00f4ca8af04db11e32dc5a88786cfb786b4b4a84fcec15c16ed9`  
		Last Modified: Wed, 27 Nov 2019 02:05:48 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e74b440cab6657354dc1f10c360db0d95b292793c03edc3c8d0c45e64a9009e`  
		Last Modified: Wed, 27 Nov 2019 02:06:05 GMT  
		Size: 105.0 MB (104983100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c04ed8f6ca08229e3b61f8daa67b49ba118a465c5d411927f726d4baf7437eb`  
		Last Modified: Wed, 27 Nov 2019 02:05:48 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dbe824121e4a60ac8c829dd487c52ce2fac50319e9d90b0dc5ad865e2640390`  
		Last Modified: Wed, 27 Nov 2019 02:05:48 GMT  
		Size: 4.0 KB (4007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0-xenial` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:f49ed701bb903cd709218404e56d372dfb9b03b536cd7754c7f80793666070a7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (143029158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dafb85d77371751edcf79ff34b7bebafc75415d082ad7d1369038c38bc71b569`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 26 Nov 2019 23:51:57 GMT
ADD file:2aa99efceecb520e73ba3c7dc167a4fbe6143ce5e9a6499e85dbc75935b3dfab in / 
# Tue, 26 Nov 2019 23:52:01 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 26 Nov 2019 23:52:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 26 Nov 2019 23:52:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 26 Nov 2019 23:52:06 GMT
CMD ["/bin/bash"]
# Wed, 27 Nov 2019 00:48:07 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 27 Nov 2019 00:48:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 27 Nov 2019 00:48:27 GMT
ENV GOSU_VERSION=1.11
# Wed, 27 Nov 2019 00:48:28 GMT
ENV JSYAML_VERSION=3.13.0
# Wed, 27 Nov 2019 00:48:55 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 27 Nov 2019 00:48:57 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 27 Nov 2019 00:50:57 GMT
ENV GPG_KEYS=9DA31620334BD75D9DCB49F368818C72E52529D4
# Wed, 27 Nov 2019 00:51:02 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 27 Nov 2019 00:51:03 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 27 Nov 2019 00:51:04 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 00:51:06 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 27 Nov 2019 00:51:10 GMT
ENV MONGO_MAJOR=4.0
# Wed, 27 Nov 2019 00:51:12 GMT
ENV MONGO_VERSION=4.0.13
# Wed, 27 Nov 2019 00:51:19 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 27 Nov 2019 00:52:07 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 27 Nov 2019 00:52:11 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 27 Nov 2019 00:52:12 GMT
VOLUME [/data/db /data/configdb]
# Wed, 27 Nov 2019 00:52:13 GMT
COPY file:021686a669d0d1d1cbb99d6ca84ff8de10577b78ea985b8cdab9d75b347a3bd0 in /usr/local/bin/ 
# Wed, 27 Nov 2019 00:52:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2019 00:52:15 GMT
EXPOSE 27017
# Wed, 27 Nov 2019 00:52:16 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:89276bd3590376dfedf96d27b310423c8a1d8c2fe92e4c5a2630aa704b1bb77f`  
		Last Modified: Mon, 11 Nov 2019 15:38:35 GMT  
		Size: 40.0 MB (39951577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a34d6b85b836a6bc6237d1912834f44592a792ab55d92f9ebe1d74973886c6`  
		Last Modified: Tue, 26 Nov 2019 23:52:51 GMT  
		Size: 470.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1bf847b434f33038cc426678c8640251706a59656ef4b0fec6fe3ba88854ab5`  
		Last Modified: Tue, 26 Nov 2019 23:52:51 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcbc4652a1718a263f7195a62c1ca8bf0117bcced50af01ac046bd164f523e5e`  
		Last Modified: Tue, 26 Nov 2019 23:52:51 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29654a2b453807f2a2ab77da919c90f470b457feb09082017c2db0cb659cbae8`  
		Last Modified: Wed, 27 Nov 2019 00:52:48 GMT  
		Size: 2.0 KB (2005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82801a5d252ba1ad5369119729d06933f6687427ec9b00ed3affee3d7d9e5a5b`  
		Last Modified: Wed, 27 Nov 2019 00:52:46 GMT  
		Size: 2.5 MB (2475016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32596fb594dee26ddc2fff00de483a10c3a1e9d0596d9e175424080fd13f6222`  
		Last Modified: Wed, 27 Nov 2019 00:52:46 GMT  
		Size: 1.2 MB (1170042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8df7b8db38cf122e5d4240be8c6a69443d07d574e37834d27d6a9316782df11`  
		Last Modified: Wed, 27 Nov 2019 00:52:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70b88de3f1a87007d7bccff5988808f14d2e9742aed390012fcccb4e6c30281`  
		Last Modified: Wed, 27 Nov 2019 00:54:01 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd55f9c2264e49984337fbf81be3647067592db952bc49fb7106b3f1eb40daa`  
		Last Modified: Wed, 27 Nov 2019 00:54:01 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df962447b3ce6cd904afde3cc1c9a3b0995ed98f88a8c1acb923721fdb6110a7`  
		Last Modified: Wed, 27 Nov 2019 00:54:39 GMT  
		Size: 99.4 MB (99423038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cde73bff8f9cd090b08b2b46cc3a82c3b4f1f8270437943a6205927efe3fb87`  
		Last Modified: Wed, 27 Nov 2019 00:54:01 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a678a14e59551b487531e0347ba6ff428a70995ac2acc4ca363b747fed15d19`  
		Last Modified: Wed, 27 Nov 2019 00:54:01 GMT  
		Size: 4.0 KB (4005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.2`

```console
$ docker pull mongo@sha256:6ca49afbcb2b44aedf53f5f27b20c99813f500981b6d62193aa770e8340461cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x
	-	windows version 10.0.14393.3384; amd64
	-	windows version 10.0.17134.1184; amd64

### `mongo:4.2` - linux; amd64

```console
$ docker pull mongo@sha256:52c3314bee611f91d37b9b1bc0cc2755b1388f2de5b396b441f3fe94bef6c56c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.3 MB (147285849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:965553e202a44592bc26d8c076eafef996a6dfc0de5bb2c1cf1795cd3b3a7373`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 31 Oct 2019 22:20:35 GMT
ADD file:a48a5dc1b9dbfc632f6cf86fe27b770b63f07a115c98c4465dc184e303a4efa1 in / 
# Thu, 31 Oct 2019 22:20:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:20:36 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:20:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:20:37 GMT
CMD ["/bin/bash"]
# Fri, 01 Nov 2019 00:34:46 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 01 Nov 2019 00:34:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Nov 2019 00:34:56 GMT
ENV GOSU_VERSION=1.11
# Fri, 01 Nov 2019 00:34:56 GMT
ENV JSYAML_VERSION=3.13.0
# Fri, 01 Nov 2019 00:35:07 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 01 Nov 2019 00:35:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Nov 2019 00:35:09 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 01 Nov 2019 00:35:10 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 01 Nov 2019 00:35:10 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 01 Nov 2019 00:35:10 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 01 Nov 2019 00:35:10 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 01 Nov 2019 00:35:10 GMT
ENV MONGO_MAJOR=4.2
# Fri, 01 Nov 2019 00:35:11 GMT
ENV MONGO_VERSION=4.2.1
# Fri, 01 Nov 2019 00:35:11 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 01 Nov 2019 00:35:29 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 01 Nov 2019 00:35:29 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 01 Nov 2019 00:35:30 GMT
VOLUME [/data/db /data/configdb]
# Fri, 01 Nov 2019 00:35:30 GMT
COPY file:021686a669d0d1d1cbb99d6ca84ff8de10577b78ea985b8cdab9d75b347a3bd0 in /usr/local/bin/ 
# Fri, 01 Nov 2019 00:35:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Nov 2019 00:35:30 GMT
EXPOSE 27017
# Fri, 01 Nov 2019 00:35:30 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7ddbc47eeb70dc7f08e410a6667948b87ff3883024eb41478b44ef9a81bf400c`  
		Last Modified: Wed, 30 Oct 2019 00:25:34 GMT  
		Size: 26.7 MB (26688847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1bbdc448b7263673926b8fe2e88491e5083a8b4b06ddfabf311f2fc5f27e2ff`  
		Last Modified: Thu, 31 Oct 2019 22:21:39 GMT  
		Size: 35.4 KB (35362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3b70e3904492c753652606df4726430426f42ea56e06ea924d6fea7ae162a1`  
		Last Modified: Thu, 31 Oct 2019 22:21:39 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45d437916d5781043432f2d72608049dcf74ddbd27daa01a25fa63c8f1b9adc4`  
		Last Modified: Thu, 31 Oct 2019 22:21:39 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e119fb0e0a556b13af304b430ee02ab7dae340974ed1c56c071f8b76ba94fce8`  
		Last Modified: Fri, 01 Nov 2019 00:37:26 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f0b9bae1ea1da827453099df499d277582fee378b02632492f5960b3199f45`  
		Last Modified: Fri, 01 Nov 2019 00:37:27 GMT  
		Size: 3.0 MB (2981726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e7c2967f1132938ce99899a660345acb7d81a2722d03be593c501f2d5a0fb5`  
		Last Modified: Fri, 01 Nov 2019 00:37:28 GMT  
		Size: 5.8 MB (5763200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a945568374aab4d5559c42c26f5e91d0077eaa2fc6f4ac2de12681665847c1`  
		Last Modified: Fri, 01 Nov 2019 00:37:25 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93333bc225a750104af3ea7a4dee020f14d95b1f7e9f3d3bbd4629a0d38cbeb8`  
		Last Modified: Fri, 01 Nov 2019 00:37:25 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c10bd6c9bdce8efa69364bade1114e6089a95a8c9b652fad7f4e5e169f882a`  
		Last Modified: Fri, 01 Nov 2019 00:37:24 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4e3538e99cfab06dca9314aa7ee1d77d09973875de8c9505159544571ca423`  
		Last Modified: Fri, 01 Nov 2019 00:37:50 GMT  
		Size: 111.8 MB (111807903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1164b51d180a68eda4b69db7227a8ef9d79924dba229c255fb45a45e7704bdbd`  
		Last Modified: Fri, 01 Nov 2019 00:37:24 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a715a7d71f27cafd081768bdaeddc9538ab8060043ae9d59e20cb067fcf98b5e`  
		Last Modified: Fri, 01 Nov 2019 00:37:25 GMT  
		Size: 4.0 KB (4007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:922dfe530d2a4bad26786c20f5ab9667bf8096c5378615ee1fb3327e1e45ba46
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136338781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f09d4aa5ffaafb22631c9c99c5038d690874b461d69736e308b6d3f5c9bbd57b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 31 Oct 2019 22:40:37 GMT
ADD file:4c6cab77271e86386e8f3d4ecf06c17a3e9339481bea878a706d2c5dc4a0addd in / 
# Thu, 31 Oct 2019 22:40:40 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:40:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:40:43 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:40:44 GMT
CMD ["/bin/bash"]
# Fri, 01 Nov 2019 00:48:13 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 01 Nov 2019 00:48:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Nov 2019 00:48:29 GMT
ENV GOSU_VERSION=1.11
# Fri, 01 Nov 2019 00:48:30 GMT
ENV JSYAML_VERSION=3.13.0
# Fri, 01 Nov 2019 00:48:54 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 01 Nov 2019 00:48:57 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Nov 2019 00:48:57 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 01 Nov 2019 00:49:00 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 01 Nov 2019 00:49:00 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 01 Nov 2019 00:49:01 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 01 Nov 2019 00:49:02 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 01 Nov 2019 00:49:03 GMT
ENV MONGO_MAJOR=4.2
# Fri, 01 Nov 2019 00:49:04 GMT
ENV MONGO_VERSION=4.2.1
# Fri, 01 Nov 2019 00:49:06 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 01 Nov 2019 00:49:30 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 01 Nov 2019 00:49:34 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 01 Nov 2019 00:49:35 GMT
VOLUME [/data/db /data/configdb]
# Fri, 01 Nov 2019 00:49:35 GMT
COPY file:021686a669d0d1d1cbb99d6ca84ff8de10577b78ea985b8cdab9d75b347a3bd0 in /usr/local/bin/ 
# Fri, 01 Nov 2019 00:49:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Nov 2019 00:49:37 GMT
EXPOSE 27017
# Fri, 01 Nov 2019 00:49:39 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:6531af3558948c8839fd7cc7eb7062aa86bfae891870ccaafd554ac65c97971b`  
		Last Modified: Thu, 31 Oct 2019 22:42:23 GMT  
		Size: 23.7 MB (23718403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f7942d2fb7381ee1735a4c972ef45c89b6521902e6eba024d4791dfd069def`  
		Last Modified: Thu, 31 Oct 2019 22:42:16 GMT  
		Size: 35.2 KB (35198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdce94e690d563311eb8b102b49e94a01b2a4c965daa9e33d5e59168dc4327e0`  
		Last Modified: Thu, 31 Oct 2019 22:42:16 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96a89ada1c32e30a1998945a8785c18bcdce55dcfe2b666bb587d432255cb11`  
		Last Modified: Thu, 31 Oct 2019 22:42:16 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441c8b285da3534c6705c81b056f0421dc29aff21e3b8e891572ee58969b23c4`  
		Last Modified: Fri, 01 Nov 2019 00:51:57 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3369e8993485be78046aa93778ceb9f0ac9a9cd1460c56dd0a39b5612a2bf0db`  
		Last Modified: Fri, 01 Nov 2019 00:51:58 GMT  
		Size: 2.7 MB (2675614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aedf06151273427f8c9155f17ce3804e486f188c768a9b1395a8e808091bfa59`  
		Last Modified: Fri, 01 Nov 2019 00:51:58 GMT  
		Size: 5.3 MB (5282727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb0173982fa974e75dbc470008149e563eb935f7027577971b32bf9790721d4`  
		Last Modified: Fri, 01 Nov 2019 00:51:57 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ff79f67ba8dbf80063a12f5296a984d5fe453bf212e7aa4562c6e9b2109d01`  
		Last Modified: Fri, 01 Nov 2019 00:51:55 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6085923db4441f085ae2476ca6fa391e1df060ca33644fb82a401201a757959f`  
		Last Modified: Fri, 01 Nov 2019 00:51:55 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50380edb4431c149b589a7bff3db64481717f9197cc57e99ea9cd2e278dab9b6`  
		Last Modified: Fri, 01 Nov 2019 00:52:21 GMT  
		Size: 104.6 MB (104617931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e667dd7db0918baac9e775b56ad7dbb1ec2806eee8f7415812d13f0dd700ed0`  
		Last Modified: Fri, 01 Nov 2019 00:51:55 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:545348b868a6ab6133facf259e76520240f6e7a6f4cdf4e53b38215cc9929476`  
		Last Modified: Fri, 01 Nov 2019 00:51:55 GMT  
		Size: 4.0 KB (4003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2` - linux; s390x

```console
$ docker pull mongo@sha256:76cdaab6ec75306255226b0ba785dd113c2f264320382e88368ae1157f93ddbc
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.5 MB (143531232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0000651cfa9056c242a341ec396f1b03a548a1d8486b039d3b6fd5d010751ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 31 Oct 2019 22:41:56 GMT
ADD file:6e6c5c69d7791dc0b62c8d03fc0c5051c6291e08dfc4e11abbdc333bc6f44359 in / 
# Thu, 31 Oct 2019 22:41:58 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:41:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:42:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:42:01 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 23:16:28 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Thu, 31 Oct 2019 23:16:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 31 Oct 2019 23:16:46 GMT
ENV GOSU_VERSION=1.11
# Thu, 31 Oct 2019 23:16:46 GMT
ENV JSYAML_VERSION=3.13.0
# Thu, 31 Oct 2019 23:17:14 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 31 Oct 2019 23:17:15 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 31 Oct 2019 23:17:15 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Thu, 31 Oct 2019 23:17:18 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 31 Oct 2019 23:17:18 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 31 Oct 2019 23:17:18 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 31 Oct 2019 23:17:18 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 31 Oct 2019 23:17:19 GMT
ENV MONGO_MAJOR=4.2
# Thu, 31 Oct 2019 23:17:19 GMT
ENV MONGO_VERSION=4.2.1
# Thu, 31 Oct 2019 23:17:21 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Thu, 31 Oct 2019 23:18:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Thu, 31 Oct 2019 23:18:06 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Thu, 31 Oct 2019 23:18:06 GMT
VOLUME [/data/db /data/configdb]
# Thu, 31 Oct 2019 23:18:07 GMT
COPY file:021686a669d0d1d1cbb99d6ca84ff8de10577b78ea985b8cdab9d75b347a3bd0 in /usr/local/bin/ 
# Thu, 31 Oct 2019 23:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 31 Oct 2019 23:18:08 GMT
EXPOSE 27017
# Thu, 31 Oct 2019 23:18:08 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:617b55fd1ba95b3ed68226101c9b2568ed00a9b7c50959230d2124648f3a47d2`  
		Last Modified: Thu, 31 Oct 2019 22:43:47 GMT  
		Size: 25.4 MB (25364650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee6ed80b799b3b7d7d66e31ba7e61be1f8d02732bccb1a22d1f14c65f9cea21`  
		Last Modified: Thu, 31 Oct 2019 22:43:42 GMT  
		Size: 36.2 KB (36173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc71634b6bba51b68da661aedfd0876ba93b197653cc94323ca050369bef0bc`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 841.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e017bfda3869ce68902d01d6dfb0fe74964f8c598ea31bc77825772e58a122b`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43ce05cccebf9f7a410bbace7582d3f6a8a6eb8f969e738365ff52fa41bef56`  
		Last Modified: Thu, 31 Oct 2019 23:18:26 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232ad1433592ae3e49689f9a399155d8cd4cb66e85d3e9a3371f64c5d3767ef5`  
		Last Modified: Thu, 31 Oct 2019 23:18:27 GMT  
		Size: 2.7 MB (2714202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfb83020b47608042582b07eac59bfe53f87d076f429e2030150fce7671fcfc`  
		Last Modified: Thu, 31 Oct 2019 23:18:28 GMT  
		Size: 5.7 MB (5684577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e67294f8ac41b2fbbb98389025f6a2934cd3e85f08b50641d96ce6fd42c5d4`  
		Last Modified: Thu, 31 Oct 2019 23:18:25 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10477e3f19872878bbd97b9b1d529a9cda966b6dab49c609ca17a815f56eaf03`  
		Last Modified: Thu, 31 Oct 2019 23:18:24 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd80e3c144d231663b9fc4f19de43fe431596d85adb3fd80db6e1965f649b99`  
		Last Modified: Thu, 31 Oct 2019 23:18:23 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390cef7a4233b0430f858343c7ffa603238382f6b3d57400fba4bc37dc1fc338`  
		Last Modified: Thu, 31 Oct 2019 23:18:49 GMT  
		Size: 109.7 MB (109722811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ab2a7a00460c93578481306a6e5212441ae6f399678d3a0938105339ff3659`  
		Last Modified: Thu, 31 Oct 2019 23:18:24 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729e6c5603fe8d82346fcc9450f163fdd06d4f77ad73e59fca74447aa971f9ba`  
		Last Modified: Thu, 31 Oct 2019 23:18:23 GMT  
		Size: 4.0 KB (4005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2` - windows version 10.0.14393.3384; amd64

```console
$ docker pull mongo@sha256:37ed0ce402c453d82362c8674a95a84ccdc02c9864bfa4fc8170d49d42584a92
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5816058219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fb916a127f9cd60ef9757a818d2c965590bd5303ed4476b1c5a8445ac0b6e2a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 15:47:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 23:35:26 GMT
ENV MONGO_VERSION=4.2.1
# Wed, 11 Dec 2019 23:35:27 GMT
ENV MONGO_DOWNLOAD_URL=https://downloads.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.1-signed.msi
# Wed, 11 Dec 2019 23:35:28 GMT
ENV MONGO_DOWNLOAD_SHA256=0bd9f5361d21cf358156e8e18aae3f4bc0298e9949b4b988c4b15b52913f91d6
# Wed, 11 Dec 2019 23:44:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Dec 2019 23:44:48 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Dec 2019 23:44:50 GMT
EXPOSE 27017
# Wed, 11 Dec 2019 23:44:52 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d23dffb4f7b6ebd1cceaac955d664d79467da76c4749d2a37d98556996d8bb0a`  
		Last Modified: Wed, 11 Dec 2019 18:01:38 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c30838129c9ab8ebc7cfc1437e4655ad2fcbf99b7c2a4f618f0dadeb02ee9b1`  
		Last Modified: Thu, 12 Dec 2019 00:08:43 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e12474c86cd0cf6cec9ffc98ee72da8f5c5ef236665b487ed4590f3083cb5d`  
		Last Modified: Thu, 12 Dec 2019 00:08:43 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de05e906a577fa8f95e8df9641ed2d7b042e8ab039218c711f9be88e153f43c4`  
		Last Modified: Thu, 12 Dec 2019 00:08:40 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0735cfc26b92c99aa40bf6c1feb6c344f5d7113c006c50441f5304fe92fd8285`  
		Last Modified: Thu, 12 Dec 2019 00:09:03 GMT  
		Size: 93.3 MB (93345990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77636ccac26ca06e73af52744671d5c6ae3db8960b110a60b0e95ed0231a9619`  
		Last Modified: Thu, 12 Dec 2019 00:08:41 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e83b06286df83053a894432b81bf6c78acc9a1000308697438915c8072f4210`  
		Last Modified: Thu, 12 Dec 2019 00:08:40 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262bd20abcdfdee728fa18bff25d7071edeb206e56c11f9b4a4080018ca2db1f`  
		Last Modified: Thu, 12 Dec 2019 00:08:40 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2` - windows version 10.0.17134.1184; amd64

```console
$ docker pull mongo@sha256:672798fb05567fe529909cf3f81422c76d5fe1a2bdbd1974abd9aa238b639f36
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2809636910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:def4de6e07cdaff0556a068451bdd6043d77ee91d167288d24f922343dab649d`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 12 Apr 2018 09:20:54 GMT
RUN Apply image 1803-RTM-amd64
# Wed, 04 Dec 2019 15:21:18 GMT
RUN Install update 1803-amd64
# Wed, 11 Dec 2019 15:36:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 23:45:17 GMT
ENV MONGO_VERSION=4.2.1
# Wed, 11 Dec 2019 23:45:19 GMT
ENV MONGO_DOWNLOAD_URL=https://downloads.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.1-signed.msi
# Wed, 11 Dec 2019 23:45:20 GMT
ENV MONGO_DOWNLOAD_SHA256=0bd9f5361d21cf358156e8e18aae3f4bc0298e9949b4b988c4b15b52913f91d6
# Thu, 12 Dec 2019 00:03:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 12 Dec 2019 00:03:17 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 12 Dec 2019 00:03:18 GMT
EXPOSE 27017
# Thu, 12 Dec 2019 00:03:20 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:d9e8b01179bfc94a5bdb1810fbd76b999aa52016001ace2d3a4c4bc7065a9601`  
		Last Modified: Tue, 18 Sep 2018 22:43:55 GMT  
		Size: 1.7 GB (1659688273 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d117323cd539488e5ef3bef575a41fa714d83119b0da1896607d96ec2a5e3b52`  
		Size: 696.9 MB (696873564 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:70c803815d644f3772896add8df055dfd33f5934921ca0c57efc290d42454abf`  
		Last Modified: Wed, 11 Dec 2019 18:00:43 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48cbbbce208b5a8e143d43012de06b33cd12dc212fae3e3f6cf28b1acd900861`  
		Last Modified: Thu, 12 Dec 2019 00:09:45 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f72bd77f828256b25eb7375c46fdec577565bc53d89a05fa8a100796450f599`  
		Last Modified: Thu, 12 Dec 2019 00:09:45 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d00e37fa3cf44154da5932563d6cfcff58333ffd56b34c2933a9b14f273b96`  
		Last Modified: Thu, 12 Dec 2019 00:09:42 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e5c13eeee73b3c63164fa7984e8859a050bb173cb69c2b162e7d93845778b5f`  
		Last Modified: Thu, 12 Dec 2019 00:10:40 GMT  
		Size: 453.1 MB (453066744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de21f5bd53ce10a88ff8e77419719b9a2283c1a3f88706ebc56116df5d13e82e`  
		Last Modified: Thu, 12 Dec 2019 00:09:42 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aecef79094cae66ab1003365b8a64bce825e973f8fc6fdaac26462fb31363a15`  
		Last Modified: Thu, 12 Dec 2019 00:09:43 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c1b6171741d09ad84e50e1a007624e0807534f6adc039d848e5915d26bcdfa9`  
		Last Modified: Thu, 12 Dec 2019 00:09:43 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.2.2`

**does not exist** (yet?)

## `mongo:4.2.2-bionic`

**does not exist** (yet?)

## `mongo:4.2.2-windowsservercore`

**does not exist** (yet?)

## `mongo:4.2.2-windowsservercore-1809`

**does not exist** (yet?)

## `mongo:4.2.2-windowsservercore-ltsc2016`

**does not exist** (yet?)

## `mongo:4.2-bionic`

```console
$ docker pull mongo@sha256:e7fb2214ca6898ea12017aaf0c7a45657a9d0e7abac1d7931b9451d2bd236f57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `mongo:4.2-bionic` - linux; amd64

```console
$ docker pull mongo@sha256:52c3314bee611f91d37b9b1bc0cc2755b1388f2de5b396b441f3fe94bef6c56c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.3 MB (147285849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:965553e202a44592bc26d8c076eafef996a6dfc0de5bb2c1cf1795cd3b3a7373`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 31 Oct 2019 22:20:35 GMT
ADD file:a48a5dc1b9dbfc632f6cf86fe27b770b63f07a115c98c4465dc184e303a4efa1 in / 
# Thu, 31 Oct 2019 22:20:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:20:36 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:20:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:20:37 GMT
CMD ["/bin/bash"]
# Fri, 01 Nov 2019 00:34:46 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 01 Nov 2019 00:34:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Nov 2019 00:34:56 GMT
ENV GOSU_VERSION=1.11
# Fri, 01 Nov 2019 00:34:56 GMT
ENV JSYAML_VERSION=3.13.0
# Fri, 01 Nov 2019 00:35:07 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 01 Nov 2019 00:35:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Nov 2019 00:35:09 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 01 Nov 2019 00:35:10 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 01 Nov 2019 00:35:10 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 01 Nov 2019 00:35:10 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 01 Nov 2019 00:35:10 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 01 Nov 2019 00:35:10 GMT
ENV MONGO_MAJOR=4.2
# Fri, 01 Nov 2019 00:35:11 GMT
ENV MONGO_VERSION=4.2.1
# Fri, 01 Nov 2019 00:35:11 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 01 Nov 2019 00:35:29 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 01 Nov 2019 00:35:29 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 01 Nov 2019 00:35:30 GMT
VOLUME [/data/db /data/configdb]
# Fri, 01 Nov 2019 00:35:30 GMT
COPY file:021686a669d0d1d1cbb99d6ca84ff8de10577b78ea985b8cdab9d75b347a3bd0 in /usr/local/bin/ 
# Fri, 01 Nov 2019 00:35:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Nov 2019 00:35:30 GMT
EXPOSE 27017
# Fri, 01 Nov 2019 00:35:30 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7ddbc47eeb70dc7f08e410a6667948b87ff3883024eb41478b44ef9a81bf400c`  
		Last Modified: Wed, 30 Oct 2019 00:25:34 GMT  
		Size: 26.7 MB (26688847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1bbdc448b7263673926b8fe2e88491e5083a8b4b06ddfabf311f2fc5f27e2ff`  
		Last Modified: Thu, 31 Oct 2019 22:21:39 GMT  
		Size: 35.4 KB (35362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3b70e3904492c753652606df4726430426f42ea56e06ea924d6fea7ae162a1`  
		Last Modified: Thu, 31 Oct 2019 22:21:39 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45d437916d5781043432f2d72608049dcf74ddbd27daa01a25fa63c8f1b9adc4`  
		Last Modified: Thu, 31 Oct 2019 22:21:39 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e119fb0e0a556b13af304b430ee02ab7dae340974ed1c56c071f8b76ba94fce8`  
		Last Modified: Fri, 01 Nov 2019 00:37:26 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f0b9bae1ea1da827453099df499d277582fee378b02632492f5960b3199f45`  
		Last Modified: Fri, 01 Nov 2019 00:37:27 GMT  
		Size: 3.0 MB (2981726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e7c2967f1132938ce99899a660345acb7d81a2722d03be593c501f2d5a0fb5`  
		Last Modified: Fri, 01 Nov 2019 00:37:28 GMT  
		Size: 5.8 MB (5763200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a945568374aab4d5559c42c26f5e91d0077eaa2fc6f4ac2de12681665847c1`  
		Last Modified: Fri, 01 Nov 2019 00:37:25 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93333bc225a750104af3ea7a4dee020f14d95b1f7e9f3d3bbd4629a0d38cbeb8`  
		Last Modified: Fri, 01 Nov 2019 00:37:25 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c10bd6c9bdce8efa69364bade1114e6089a95a8c9b652fad7f4e5e169f882a`  
		Last Modified: Fri, 01 Nov 2019 00:37:24 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4e3538e99cfab06dca9314aa7ee1d77d09973875de8c9505159544571ca423`  
		Last Modified: Fri, 01 Nov 2019 00:37:50 GMT  
		Size: 111.8 MB (111807903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1164b51d180a68eda4b69db7227a8ef9d79924dba229c255fb45a45e7704bdbd`  
		Last Modified: Fri, 01 Nov 2019 00:37:24 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a715a7d71f27cafd081768bdaeddc9538ab8060043ae9d59e20cb067fcf98b5e`  
		Last Modified: Fri, 01 Nov 2019 00:37:25 GMT  
		Size: 4.0 KB (4007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2-bionic` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:922dfe530d2a4bad26786c20f5ab9667bf8096c5378615ee1fb3327e1e45ba46
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136338781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f09d4aa5ffaafb22631c9c99c5038d690874b461d69736e308b6d3f5c9bbd57b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 31 Oct 2019 22:40:37 GMT
ADD file:4c6cab77271e86386e8f3d4ecf06c17a3e9339481bea878a706d2c5dc4a0addd in / 
# Thu, 31 Oct 2019 22:40:40 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:40:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:40:43 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:40:44 GMT
CMD ["/bin/bash"]
# Fri, 01 Nov 2019 00:48:13 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 01 Nov 2019 00:48:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Nov 2019 00:48:29 GMT
ENV GOSU_VERSION=1.11
# Fri, 01 Nov 2019 00:48:30 GMT
ENV JSYAML_VERSION=3.13.0
# Fri, 01 Nov 2019 00:48:54 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 01 Nov 2019 00:48:57 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Nov 2019 00:48:57 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 01 Nov 2019 00:49:00 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 01 Nov 2019 00:49:00 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 01 Nov 2019 00:49:01 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 01 Nov 2019 00:49:02 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 01 Nov 2019 00:49:03 GMT
ENV MONGO_MAJOR=4.2
# Fri, 01 Nov 2019 00:49:04 GMT
ENV MONGO_VERSION=4.2.1
# Fri, 01 Nov 2019 00:49:06 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 01 Nov 2019 00:49:30 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 01 Nov 2019 00:49:34 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 01 Nov 2019 00:49:35 GMT
VOLUME [/data/db /data/configdb]
# Fri, 01 Nov 2019 00:49:35 GMT
COPY file:021686a669d0d1d1cbb99d6ca84ff8de10577b78ea985b8cdab9d75b347a3bd0 in /usr/local/bin/ 
# Fri, 01 Nov 2019 00:49:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Nov 2019 00:49:37 GMT
EXPOSE 27017
# Fri, 01 Nov 2019 00:49:39 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:6531af3558948c8839fd7cc7eb7062aa86bfae891870ccaafd554ac65c97971b`  
		Last Modified: Thu, 31 Oct 2019 22:42:23 GMT  
		Size: 23.7 MB (23718403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f7942d2fb7381ee1735a4c972ef45c89b6521902e6eba024d4791dfd069def`  
		Last Modified: Thu, 31 Oct 2019 22:42:16 GMT  
		Size: 35.2 KB (35198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdce94e690d563311eb8b102b49e94a01b2a4c965daa9e33d5e59168dc4327e0`  
		Last Modified: Thu, 31 Oct 2019 22:42:16 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96a89ada1c32e30a1998945a8785c18bcdce55dcfe2b666bb587d432255cb11`  
		Last Modified: Thu, 31 Oct 2019 22:42:16 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441c8b285da3534c6705c81b056f0421dc29aff21e3b8e891572ee58969b23c4`  
		Last Modified: Fri, 01 Nov 2019 00:51:57 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3369e8993485be78046aa93778ceb9f0ac9a9cd1460c56dd0a39b5612a2bf0db`  
		Last Modified: Fri, 01 Nov 2019 00:51:58 GMT  
		Size: 2.7 MB (2675614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aedf06151273427f8c9155f17ce3804e486f188c768a9b1395a8e808091bfa59`  
		Last Modified: Fri, 01 Nov 2019 00:51:58 GMT  
		Size: 5.3 MB (5282727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb0173982fa974e75dbc470008149e563eb935f7027577971b32bf9790721d4`  
		Last Modified: Fri, 01 Nov 2019 00:51:57 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ff79f67ba8dbf80063a12f5296a984d5fe453bf212e7aa4562c6e9b2109d01`  
		Last Modified: Fri, 01 Nov 2019 00:51:55 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6085923db4441f085ae2476ca6fa391e1df060ca33644fb82a401201a757959f`  
		Last Modified: Fri, 01 Nov 2019 00:51:55 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50380edb4431c149b589a7bff3db64481717f9197cc57e99ea9cd2e278dab9b6`  
		Last Modified: Fri, 01 Nov 2019 00:52:21 GMT  
		Size: 104.6 MB (104617931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e667dd7db0918baac9e775b56ad7dbb1ec2806eee8f7415812d13f0dd700ed0`  
		Last Modified: Fri, 01 Nov 2019 00:51:55 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:545348b868a6ab6133facf259e76520240f6e7a6f4cdf4e53b38215cc9929476`  
		Last Modified: Fri, 01 Nov 2019 00:51:55 GMT  
		Size: 4.0 KB (4003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2-bionic` - linux; s390x

```console
$ docker pull mongo@sha256:76cdaab6ec75306255226b0ba785dd113c2f264320382e88368ae1157f93ddbc
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.5 MB (143531232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0000651cfa9056c242a341ec396f1b03a548a1d8486b039d3b6fd5d010751ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 31 Oct 2019 22:41:56 GMT
ADD file:6e6c5c69d7791dc0b62c8d03fc0c5051c6291e08dfc4e11abbdc333bc6f44359 in / 
# Thu, 31 Oct 2019 22:41:58 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:41:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:42:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:42:01 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 23:16:28 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Thu, 31 Oct 2019 23:16:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 31 Oct 2019 23:16:46 GMT
ENV GOSU_VERSION=1.11
# Thu, 31 Oct 2019 23:16:46 GMT
ENV JSYAML_VERSION=3.13.0
# Thu, 31 Oct 2019 23:17:14 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 31 Oct 2019 23:17:15 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 31 Oct 2019 23:17:15 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Thu, 31 Oct 2019 23:17:18 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 31 Oct 2019 23:17:18 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 31 Oct 2019 23:17:18 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 31 Oct 2019 23:17:18 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 31 Oct 2019 23:17:19 GMT
ENV MONGO_MAJOR=4.2
# Thu, 31 Oct 2019 23:17:19 GMT
ENV MONGO_VERSION=4.2.1
# Thu, 31 Oct 2019 23:17:21 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Thu, 31 Oct 2019 23:18:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Thu, 31 Oct 2019 23:18:06 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Thu, 31 Oct 2019 23:18:06 GMT
VOLUME [/data/db /data/configdb]
# Thu, 31 Oct 2019 23:18:07 GMT
COPY file:021686a669d0d1d1cbb99d6ca84ff8de10577b78ea985b8cdab9d75b347a3bd0 in /usr/local/bin/ 
# Thu, 31 Oct 2019 23:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 31 Oct 2019 23:18:08 GMT
EXPOSE 27017
# Thu, 31 Oct 2019 23:18:08 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:617b55fd1ba95b3ed68226101c9b2568ed00a9b7c50959230d2124648f3a47d2`  
		Last Modified: Thu, 31 Oct 2019 22:43:47 GMT  
		Size: 25.4 MB (25364650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee6ed80b799b3b7d7d66e31ba7e61be1f8d02732bccb1a22d1f14c65f9cea21`  
		Last Modified: Thu, 31 Oct 2019 22:43:42 GMT  
		Size: 36.2 KB (36173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc71634b6bba51b68da661aedfd0876ba93b197653cc94323ca050369bef0bc`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 841.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e017bfda3869ce68902d01d6dfb0fe74964f8c598ea31bc77825772e58a122b`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43ce05cccebf9f7a410bbace7582d3f6a8a6eb8f969e738365ff52fa41bef56`  
		Last Modified: Thu, 31 Oct 2019 23:18:26 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232ad1433592ae3e49689f9a399155d8cd4cb66e85d3e9a3371f64c5d3767ef5`  
		Last Modified: Thu, 31 Oct 2019 23:18:27 GMT  
		Size: 2.7 MB (2714202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfb83020b47608042582b07eac59bfe53f87d076f429e2030150fce7671fcfc`  
		Last Modified: Thu, 31 Oct 2019 23:18:28 GMT  
		Size: 5.7 MB (5684577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e67294f8ac41b2fbbb98389025f6a2934cd3e85f08b50641d96ce6fd42c5d4`  
		Last Modified: Thu, 31 Oct 2019 23:18:25 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10477e3f19872878bbd97b9b1d529a9cda966b6dab49c609ca17a815f56eaf03`  
		Last Modified: Thu, 31 Oct 2019 23:18:24 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd80e3c144d231663b9fc4f19de43fe431596d85adb3fd80db6e1965f649b99`  
		Last Modified: Thu, 31 Oct 2019 23:18:23 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390cef7a4233b0430f858343c7ffa603238382f6b3d57400fba4bc37dc1fc338`  
		Last Modified: Thu, 31 Oct 2019 23:18:49 GMT  
		Size: 109.7 MB (109722811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ab2a7a00460c93578481306a6e5212441ae6f399678d3a0938105339ff3659`  
		Last Modified: Thu, 31 Oct 2019 23:18:24 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729e6c5603fe8d82346fcc9450f163fdd06d4f77ad73e59fca74447aa971f9ba`  
		Last Modified: Thu, 31 Oct 2019 23:18:23 GMT  
		Size: 4.0 KB (4005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.2-windowsservercore`

```console
$ docker pull mongo@sha256:c310176382896f4a10beb26fbcfdd25844d3ce06c0267a7a470b1f4f7e60576e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3384; amd64
	-	windows version 10.0.17134.1184; amd64

### `mongo:4.2-windowsservercore` - windows version 10.0.14393.3384; amd64

```console
$ docker pull mongo@sha256:37ed0ce402c453d82362c8674a95a84ccdc02c9864bfa4fc8170d49d42584a92
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5816058219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fb916a127f9cd60ef9757a818d2c965590bd5303ed4476b1c5a8445ac0b6e2a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 15:47:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 23:35:26 GMT
ENV MONGO_VERSION=4.2.1
# Wed, 11 Dec 2019 23:35:27 GMT
ENV MONGO_DOWNLOAD_URL=https://downloads.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.1-signed.msi
# Wed, 11 Dec 2019 23:35:28 GMT
ENV MONGO_DOWNLOAD_SHA256=0bd9f5361d21cf358156e8e18aae3f4bc0298e9949b4b988c4b15b52913f91d6
# Wed, 11 Dec 2019 23:44:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Dec 2019 23:44:48 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Dec 2019 23:44:50 GMT
EXPOSE 27017
# Wed, 11 Dec 2019 23:44:52 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d23dffb4f7b6ebd1cceaac955d664d79467da76c4749d2a37d98556996d8bb0a`  
		Last Modified: Wed, 11 Dec 2019 18:01:38 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c30838129c9ab8ebc7cfc1437e4655ad2fcbf99b7c2a4f618f0dadeb02ee9b1`  
		Last Modified: Thu, 12 Dec 2019 00:08:43 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e12474c86cd0cf6cec9ffc98ee72da8f5c5ef236665b487ed4590f3083cb5d`  
		Last Modified: Thu, 12 Dec 2019 00:08:43 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de05e906a577fa8f95e8df9641ed2d7b042e8ab039218c711f9be88e153f43c4`  
		Last Modified: Thu, 12 Dec 2019 00:08:40 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0735cfc26b92c99aa40bf6c1feb6c344f5d7113c006c50441f5304fe92fd8285`  
		Last Modified: Thu, 12 Dec 2019 00:09:03 GMT  
		Size: 93.3 MB (93345990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77636ccac26ca06e73af52744671d5c6ae3db8960b110a60b0e95ed0231a9619`  
		Last Modified: Thu, 12 Dec 2019 00:08:41 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e83b06286df83053a894432b81bf6c78acc9a1000308697438915c8072f4210`  
		Last Modified: Thu, 12 Dec 2019 00:08:40 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262bd20abcdfdee728fa18bff25d7071edeb206e56c11f9b4a4080018ca2db1f`  
		Last Modified: Thu, 12 Dec 2019 00:08:40 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2-windowsservercore` - windows version 10.0.17134.1184; amd64

```console
$ docker pull mongo@sha256:672798fb05567fe529909cf3f81422c76d5fe1a2bdbd1974abd9aa238b639f36
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2809636910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:def4de6e07cdaff0556a068451bdd6043d77ee91d167288d24f922343dab649d`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 12 Apr 2018 09:20:54 GMT
RUN Apply image 1803-RTM-amd64
# Wed, 04 Dec 2019 15:21:18 GMT
RUN Install update 1803-amd64
# Wed, 11 Dec 2019 15:36:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 23:45:17 GMT
ENV MONGO_VERSION=4.2.1
# Wed, 11 Dec 2019 23:45:19 GMT
ENV MONGO_DOWNLOAD_URL=https://downloads.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.1-signed.msi
# Wed, 11 Dec 2019 23:45:20 GMT
ENV MONGO_DOWNLOAD_SHA256=0bd9f5361d21cf358156e8e18aae3f4bc0298e9949b4b988c4b15b52913f91d6
# Thu, 12 Dec 2019 00:03:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 12 Dec 2019 00:03:17 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 12 Dec 2019 00:03:18 GMT
EXPOSE 27017
# Thu, 12 Dec 2019 00:03:20 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:d9e8b01179bfc94a5bdb1810fbd76b999aa52016001ace2d3a4c4bc7065a9601`  
		Last Modified: Tue, 18 Sep 2018 22:43:55 GMT  
		Size: 1.7 GB (1659688273 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d117323cd539488e5ef3bef575a41fa714d83119b0da1896607d96ec2a5e3b52`  
		Size: 696.9 MB (696873564 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:70c803815d644f3772896add8df055dfd33f5934921ca0c57efc290d42454abf`  
		Last Modified: Wed, 11 Dec 2019 18:00:43 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48cbbbce208b5a8e143d43012de06b33cd12dc212fae3e3f6cf28b1acd900861`  
		Last Modified: Thu, 12 Dec 2019 00:09:45 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f72bd77f828256b25eb7375c46fdec577565bc53d89a05fa8a100796450f599`  
		Last Modified: Thu, 12 Dec 2019 00:09:45 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d00e37fa3cf44154da5932563d6cfcff58333ffd56b34c2933a9b14f273b96`  
		Last Modified: Thu, 12 Dec 2019 00:09:42 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e5c13eeee73b3c63164fa7984e8859a050bb173cb69c2b162e7d93845778b5f`  
		Last Modified: Thu, 12 Dec 2019 00:10:40 GMT  
		Size: 453.1 MB (453066744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de21f5bd53ce10a88ff8e77419719b9a2283c1a3f88706ebc56116df5d13e82e`  
		Last Modified: Thu, 12 Dec 2019 00:09:42 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aecef79094cae66ab1003365b8a64bce825e973f8fc6fdaac26462fb31363a15`  
		Last Modified: Thu, 12 Dec 2019 00:09:43 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c1b6171741d09ad84e50e1a007624e0807534f6adc039d848e5915d26bcdfa9`  
		Last Modified: Thu, 12 Dec 2019 00:09:43 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.2-windowsservercore-1809`

```console
$ docker pull mongo@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:

## `mongo:4.2-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:db78a7411279c77330a0e1cbc4bdf6db701b37e68a3071b4ae0a8186818828f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3384; amd64

### `mongo:4.2-windowsservercore-ltsc2016` - windows version 10.0.14393.3384; amd64

```console
$ docker pull mongo@sha256:37ed0ce402c453d82362c8674a95a84ccdc02c9864bfa4fc8170d49d42584a92
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5816058219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fb916a127f9cd60ef9757a818d2c965590bd5303ed4476b1c5a8445ac0b6e2a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 15:47:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 23:35:26 GMT
ENV MONGO_VERSION=4.2.1
# Wed, 11 Dec 2019 23:35:27 GMT
ENV MONGO_DOWNLOAD_URL=https://downloads.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.1-signed.msi
# Wed, 11 Dec 2019 23:35:28 GMT
ENV MONGO_DOWNLOAD_SHA256=0bd9f5361d21cf358156e8e18aae3f4bc0298e9949b4b988c4b15b52913f91d6
# Wed, 11 Dec 2019 23:44:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Dec 2019 23:44:48 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Dec 2019 23:44:50 GMT
EXPOSE 27017
# Wed, 11 Dec 2019 23:44:52 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d23dffb4f7b6ebd1cceaac955d664d79467da76c4749d2a37d98556996d8bb0a`  
		Last Modified: Wed, 11 Dec 2019 18:01:38 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c30838129c9ab8ebc7cfc1437e4655ad2fcbf99b7c2a4f618f0dadeb02ee9b1`  
		Last Modified: Thu, 12 Dec 2019 00:08:43 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e12474c86cd0cf6cec9ffc98ee72da8f5c5ef236665b487ed4590f3083cb5d`  
		Last Modified: Thu, 12 Dec 2019 00:08:43 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de05e906a577fa8f95e8df9641ed2d7b042e8ab039218c711f9be88e153f43c4`  
		Last Modified: Thu, 12 Dec 2019 00:08:40 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0735cfc26b92c99aa40bf6c1feb6c344f5d7113c006c50441f5304fe92fd8285`  
		Last Modified: Thu, 12 Dec 2019 00:09:03 GMT  
		Size: 93.3 MB (93345990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77636ccac26ca06e73af52744671d5c6ae3db8960b110a60b0e95ed0231a9619`  
		Last Modified: Thu, 12 Dec 2019 00:08:41 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e83b06286df83053a894432b81bf6c78acc9a1000308697438915c8072f4210`  
		Last Modified: Thu, 12 Dec 2019 00:08:40 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262bd20abcdfdee728fa18bff25d7071edeb206e56c11f9b4a4080018ca2db1f`  
		Last Modified: Thu, 12 Dec 2019 00:08:40 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4-bionic`

```console
$ docker pull mongo@sha256:e7fb2214ca6898ea12017aaf0c7a45657a9d0e7abac1d7931b9451d2bd236f57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `mongo:4-bionic` - linux; amd64

```console
$ docker pull mongo@sha256:52c3314bee611f91d37b9b1bc0cc2755b1388f2de5b396b441f3fe94bef6c56c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.3 MB (147285849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:965553e202a44592bc26d8c076eafef996a6dfc0de5bb2c1cf1795cd3b3a7373`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 31 Oct 2019 22:20:35 GMT
ADD file:a48a5dc1b9dbfc632f6cf86fe27b770b63f07a115c98c4465dc184e303a4efa1 in / 
# Thu, 31 Oct 2019 22:20:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:20:36 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:20:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:20:37 GMT
CMD ["/bin/bash"]
# Fri, 01 Nov 2019 00:34:46 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 01 Nov 2019 00:34:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Nov 2019 00:34:56 GMT
ENV GOSU_VERSION=1.11
# Fri, 01 Nov 2019 00:34:56 GMT
ENV JSYAML_VERSION=3.13.0
# Fri, 01 Nov 2019 00:35:07 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 01 Nov 2019 00:35:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Nov 2019 00:35:09 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 01 Nov 2019 00:35:10 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 01 Nov 2019 00:35:10 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 01 Nov 2019 00:35:10 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 01 Nov 2019 00:35:10 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 01 Nov 2019 00:35:10 GMT
ENV MONGO_MAJOR=4.2
# Fri, 01 Nov 2019 00:35:11 GMT
ENV MONGO_VERSION=4.2.1
# Fri, 01 Nov 2019 00:35:11 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 01 Nov 2019 00:35:29 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 01 Nov 2019 00:35:29 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 01 Nov 2019 00:35:30 GMT
VOLUME [/data/db /data/configdb]
# Fri, 01 Nov 2019 00:35:30 GMT
COPY file:021686a669d0d1d1cbb99d6ca84ff8de10577b78ea985b8cdab9d75b347a3bd0 in /usr/local/bin/ 
# Fri, 01 Nov 2019 00:35:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Nov 2019 00:35:30 GMT
EXPOSE 27017
# Fri, 01 Nov 2019 00:35:30 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7ddbc47eeb70dc7f08e410a6667948b87ff3883024eb41478b44ef9a81bf400c`  
		Last Modified: Wed, 30 Oct 2019 00:25:34 GMT  
		Size: 26.7 MB (26688847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1bbdc448b7263673926b8fe2e88491e5083a8b4b06ddfabf311f2fc5f27e2ff`  
		Last Modified: Thu, 31 Oct 2019 22:21:39 GMT  
		Size: 35.4 KB (35362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3b70e3904492c753652606df4726430426f42ea56e06ea924d6fea7ae162a1`  
		Last Modified: Thu, 31 Oct 2019 22:21:39 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45d437916d5781043432f2d72608049dcf74ddbd27daa01a25fa63c8f1b9adc4`  
		Last Modified: Thu, 31 Oct 2019 22:21:39 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e119fb0e0a556b13af304b430ee02ab7dae340974ed1c56c071f8b76ba94fce8`  
		Last Modified: Fri, 01 Nov 2019 00:37:26 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f0b9bae1ea1da827453099df499d277582fee378b02632492f5960b3199f45`  
		Last Modified: Fri, 01 Nov 2019 00:37:27 GMT  
		Size: 3.0 MB (2981726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e7c2967f1132938ce99899a660345acb7d81a2722d03be593c501f2d5a0fb5`  
		Last Modified: Fri, 01 Nov 2019 00:37:28 GMT  
		Size: 5.8 MB (5763200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a945568374aab4d5559c42c26f5e91d0077eaa2fc6f4ac2de12681665847c1`  
		Last Modified: Fri, 01 Nov 2019 00:37:25 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93333bc225a750104af3ea7a4dee020f14d95b1f7e9f3d3bbd4629a0d38cbeb8`  
		Last Modified: Fri, 01 Nov 2019 00:37:25 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c10bd6c9bdce8efa69364bade1114e6089a95a8c9b652fad7f4e5e169f882a`  
		Last Modified: Fri, 01 Nov 2019 00:37:24 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4e3538e99cfab06dca9314aa7ee1d77d09973875de8c9505159544571ca423`  
		Last Modified: Fri, 01 Nov 2019 00:37:50 GMT  
		Size: 111.8 MB (111807903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1164b51d180a68eda4b69db7227a8ef9d79924dba229c255fb45a45e7704bdbd`  
		Last Modified: Fri, 01 Nov 2019 00:37:24 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a715a7d71f27cafd081768bdaeddc9538ab8060043ae9d59e20cb067fcf98b5e`  
		Last Modified: Fri, 01 Nov 2019 00:37:25 GMT  
		Size: 4.0 KB (4007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-bionic` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:922dfe530d2a4bad26786c20f5ab9667bf8096c5378615ee1fb3327e1e45ba46
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136338781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f09d4aa5ffaafb22631c9c99c5038d690874b461d69736e308b6d3f5c9bbd57b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 31 Oct 2019 22:40:37 GMT
ADD file:4c6cab77271e86386e8f3d4ecf06c17a3e9339481bea878a706d2c5dc4a0addd in / 
# Thu, 31 Oct 2019 22:40:40 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:40:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:40:43 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:40:44 GMT
CMD ["/bin/bash"]
# Fri, 01 Nov 2019 00:48:13 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 01 Nov 2019 00:48:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Nov 2019 00:48:29 GMT
ENV GOSU_VERSION=1.11
# Fri, 01 Nov 2019 00:48:30 GMT
ENV JSYAML_VERSION=3.13.0
# Fri, 01 Nov 2019 00:48:54 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 01 Nov 2019 00:48:57 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Nov 2019 00:48:57 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 01 Nov 2019 00:49:00 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 01 Nov 2019 00:49:00 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 01 Nov 2019 00:49:01 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 01 Nov 2019 00:49:02 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 01 Nov 2019 00:49:03 GMT
ENV MONGO_MAJOR=4.2
# Fri, 01 Nov 2019 00:49:04 GMT
ENV MONGO_VERSION=4.2.1
# Fri, 01 Nov 2019 00:49:06 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 01 Nov 2019 00:49:30 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 01 Nov 2019 00:49:34 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 01 Nov 2019 00:49:35 GMT
VOLUME [/data/db /data/configdb]
# Fri, 01 Nov 2019 00:49:35 GMT
COPY file:021686a669d0d1d1cbb99d6ca84ff8de10577b78ea985b8cdab9d75b347a3bd0 in /usr/local/bin/ 
# Fri, 01 Nov 2019 00:49:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Nov 2019 00:49:37 GMT
EXPOSE 27017
# Fri, 01 Nov 2019 00:49:39 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:6531af3558948c8839fd7cc7eb7062aa86bfae891870ccaafd554ac65c97971b`  
		Last Modified: Thu, 31 Oct 2019 22:42:23 GMT  
		Size: 23.7 MB (23718403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f7942d2fb7381ee1735a4c972ef45c89b6521902e6eba024d4791dfd069def`  
		Last Modified: Thu, 31 Oct 2019 22:42:16 GMT  
		Size: 35.2 KB (35198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdce94e690d563311eb8b102b49e94a01b2a4c965daa9e33d5e59168dc4327e0`  
		Last Modified: Thu, 31 Oct 2019 22:42:16 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96a89ada1c32e30a1998945a8785c18bcdce55dcfe2b666bb587d432255cb11`  
		Last Modified: Thu, 31 Oct 2019 22:42:16 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441c8b285da3534c6705c81b056f0421dc29aff21e3b8e891572ee58969b23c4`  
		Last Modified: Fri, 01 Nov 2019 00:51:57 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3369e8993485be78046aa93778ceb9f0ac9a9cd1460c56dd0a39b5612a2bf0db`  
		Last Modified: Fri, 01 Nov 2019 00:51:58 GMT  
		Size: 2.7 MB (2675614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aedf06151273427f8c9155f17ce3804e486f188c768a9b1395a8e808091bfa59`  
		Last Modified: Fri, 01 Nov 2019 00:51:58 GMT  
		Size: 5.3 MB (5282727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb0173982fa974e75dbc470008149e563eb935f7027577971b32bf9790721d4`  
		Last Modified: Fri, 01 Nov 2019 00:51:57 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ff79f67ba8dbf80063a12f5296a984d5fe453bf212e7aa4562c6e9b2109d01`  
		Last Modified: Fri, 01 Nov 2019 00:51:55 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6085923db4441f085ae2476ca6fa391e1df060ca33644fb82a401201a757959f`  
		Last Modified: Fri, 01 Nov 2019 00:51:55 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50380edb4431c149b589a7bff3db64481717f9197cc57e99ea9cd2e278dab9b6`  
		Last Modified: Fri, 01 Nov 2019 00:52:21 GMT  
		Size: 104.6 MB (104617931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e667dd7db0918baac9e775b56ad7dbb1ec2806eee8f7415812d13f0dd700ed0`  
		Last Modified: Fri, 01 Nov 2019 00:51:55 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:545348b868a6ab6133facf259e76520240f6e7a6f4cdf4e53b38215cc9929476`  
		Last Modified: Fri, 01 Nov 2019 00:51:55 GMT  
		Size: 4.0 KB (4003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-bionic` - linux; s390x

```console
$ docker pull mongo@sha256:76cdaab6ec75306255226b0ba785dd113c2f264320382e88368ae1157f93ddbc
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.5 MB (143531232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0000651cfa9056c242a341ec396f1b03a548a1d8486b039d3b6fd5d010751ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 31 Oct 2019 22:41:56 GMT
ADD file:6e6c5c69d7791dc0b62c8d03fc0c5051c6291e08dfc4e11abbdc333bc6f44359 in / 
# Thu, 31 Oct 2019 22:41:58 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:41:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:42:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:42:01 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 23:16:28 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Thu, 31 Oct 2019 23:16:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 31 Oct 2019 23:16:46 GMT
ENV GOSU_VERSION=1.11
# Thu, 31 Oct 2019 23:16:46 GMT
ENV JSYAML_VERSION=3.13.0
# Thu, 31 Oct 2019 23:17:14 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 31 Oct 2019 23:17:15 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 31 Oct 2019 23:17:15 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Thu, 31 Oct 2019 23:17:18 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 31 Oct 2019 23:17:18 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 31 Oct 2019 23:17:18 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 31 Oct 2019 23:17:18 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 31 Oct 2019 23:17:19 GMT
ENV MONGO_MAJOR=4.2
# Thu, 31 Oct 2019 23:17:19 GMT
ENV MONGO_VERSION=4.2.1
# Thu, 31 Oct 2019 23:17:21 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Thu, 31 Oct 2019 23:18:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Thu, 31 Oct 2019 23:18:06 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Thu, 31 Oct 2019 23:18:06 GMT
VOLUME [/data/db /data/configdb]
# Thu, 31 Oct 2019 23:18:07 GMT
COPY file:021686a669d0d1d1cbb99d6ca84ff8de10577b78ea985b8cdab9d75b347a3bd0 in /usr/local/bin/ 
# Thu, 31 Oct 2019 23:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 31 Oct 2019 23:18:08 GMT
EXPOSE 27017
# Thu, 31 Oct 2019 23:18:08 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:617b55fd1ba95b3ed68226101c9b2568ed00a9b7c50959230d2124648f3a47d2`  
		Last Modified: Thu, 31 Oct 2019 22:43:47 GMT  
		Size: 25.4 MB (25364650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee6ed80b799b3b7d7d66e31ba7e61be1f8d02732bccb1a22d1f14c65f9cea21`  
		Last Modified: Thu, 31 Oct 2019 22:43:42 GMT  
		Size: 36.2 KB (36173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc71634b6bba51b68da661aedfd0876ba93b197653cc94323ca050369bef0bc`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 841.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e017bfda3869ce68902d01d6dfb0fe74964f8c598ea31bc77825772e58a122b`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43ce05cccebf9f7a410bbace7582d3f6a8a6eb8f969e738365ff52fa41bef56`  
		Last Modified: Thu, 31 Oct 2019 23:18:26 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232ad1433592ae3e49689f9a399155d8cd4cb66e85d3e9a3371f64c5d3767ef5`  
		Last Modified: Thu, 31 Oct 2019 23:18:27 GMT  
		Size: 2.7 MB (2714202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfb83020b47608042582b07eac59bfe53f87d076f429e2030150fce7671fcfc`  
		Last Modified: Thu, 31 Oct 2019 23:18:28 GMT  
		Size: 5.7 MB (5684577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e67294f8ac41b2fbbb98389025f6a2934cd3e85f08b50641d96ce6fd42c5d4`  
		Last Modified: Thu, 31 Oct 2019 23:18:25 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10477e3f19872878bbd97b9b1d529a9cda966b6dab49c609ca17a815f56eaf03`  
		Last Modified: Thu, 31 Oct 2019 23:18:24 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd80e3c144d231663b9fc4f19de43fe431596d85adb3fd80db6e1965f649b99`  
		Last Modified: Thu, 31 Oct 2019 23:18:23 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390cef7a4233b0430f858343c7ffa603238382f6b3d57400fba4bc37dc1fc338`  
		Last Modified: Thu, 31 Oct 2019 23:18:49 GMT  
		Size: 109.7 MB (109722811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ab2a7a00460c93578481306a6e5212441ae6f399678d3a0938105339ff3659`  
		Last Modified: Thu, 31 Oct 2019 23:18:24 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729e6c5603fe8d82346fcc9450f163fdd06d4f77ad73e59fca74447aa971f9ba`  
		Last Modified: Thu, 31 Oct 2019 23:18:23 GMT  
		Size: 4.0 KB (4005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4-windowsservercore`

```console
$ docker pull mongo@sha256:c310176382896f4a10beb26fbcfdd25844d3ce06c0267a7a470b1f4f7e60576e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3384; amd64
	-	windows version 10.0.17134.1184; amd64

### `mongo:4-windowsservercore` - windows version 10.0.14393.3384; amd64

```console
$ docker pull mongo@sha256:37ed0ce402c453d82362c8674a95a84ccdc02c9864bfa4fc8170d49d42584a92
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5816058219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fb916a127f9cd60ef9757a818d2c965590bd5303ed4476b1c5a8445ac0b6e2a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 15:47:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 23:35:26 GMT
ENV MONGO_VERSION=4.2.1
# Wed, 11 Dec 2019 23:35:27 GMT
ENV MONGO_DOWNLOAD_URL=https://downloads.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.1-signed.msi
# Wed, 11 Dec 2019 23:35:28 GMT
ENV MONGO_DOWNLOAD_SHA256=0bd9f5361d21cf358156e8e18aae3f4bc0298e9949b4b988c4b15b52913f91d6
# Wed, 11 Dec 2019 23:44:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Dec 2019 23:44:48 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Dec 2019 23:44:50 GMT
EXPOSE 27017
# Wed, 11 Dec 2019 23:44:52 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d23dffb4f7b6ebd1cceaac955d664d79467da76c4749d2a37d98556996d8bb0a`  
		Last Modified: Wed, 11 Dec 2019 18:01:38 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c30838129c9ab8ebc7cfc1437e4655ad2fcbf99b7c2a4f618f0dadeb02ee9b1`  
		Last Modified: Thu, 12 Dec 2019 00:08:43 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e12474c86cd0cf6cec9ffc98ee72da8f5c5ef236665b487ed4590f3083cb5d`  
		Last Modified: Thu, 12 Dec 2019 00:08:43 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de05e906a577fa8f95e8df9641ed2d7b042e8ab039218c711f9be88e153f43c4`  
		Last Modified: Thu, 12 Dec 2019 00:08:40 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0735cfc26b92c99aa40bf6c1feb6c344f5d7113c006c50441f5304fe92fd8285`  
		Last Modified: Thu, 12 Dec 2019 00:09:03 GMT  
		Size: 93.3 MB (93345990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77636ccac26ca06e73af52744671d5c6ae3db8960b110a60b0e95ed0231a9619`  
		Last Modified: Thu, 12 Dec 2019 00:08:41 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e83b06286df83053a894432b81bf6c78acc9a1000308697438915c8072f4210`  
		Last Modified: Thu, 12 Dec 2019 00:08:40 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262bd20abcdfdee728fa18bff25d7071edeb206e56c11f9b4a4080018ca2db1f`  
		Last Modified: Thu, 12 Dec 2019 00:08:40 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-windowsservercore` - windows version 10.0.17134.1184; amd64

```console
$ docker pull mongo@sha256:672798fb05567fe529909cf3f81422c76d5fe1a2bdbd1974abd9aa238b639f36
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2809636910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:def4de6e07cdaff0556a068451bdd6043d77ee91d167288d24f922343dab649d`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 12 Apr 2018 09:20:54 GMT
RUN Apply image 1803-RTM-amd64
# Wed, 04 Dec 2019 15:21:18 GMT
RUN Install update 1803-amd64
# Wed, 11 Dec 2019 15:36:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 23:45:17 GMT
ENV MONGO_VERSION=4.2.1
# Wed, 11 Dec 2019 23:45:19 GMT
ENV MONGO_DOWNLOAD_URL=https://downloads.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.1-signed.msi
# Wed, 11 Dec 2019 23:45:20 GMT
ENV MONGO_DOWNLOAD_SHA256=0bd9f5361d21cf358156e8e18aae3f4bc0298e9949b4b988c4b15b52913f91d6
# Thu, 12 Dec 2019 00:03:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 12 Dec 2019 00:03:17 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 12 Dec 2019 00:03:18 GMT
EXPOSE 27017
# Thu, 12 Dec 2019 00:03:20 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:d9e8b01179bfc94a5bdb1810fbd76b999aa52016001ace2d3a4c4bc7065a9601`  
		Last Modified: Tue, 18 Sep 2018 22:43:55 GMT  
		Size: 1.7 GB (1659688273 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d117323cd539488e5ef3bef575a41fa714d83119b0da1896607d96ec2a5e3b52`  
		Size: 696.9 MB (696873564 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:70c803815d644f3772896add8df055dfd33f5934921ca0c57efc290d42454abf`  
		Last Modified: Wed, 11 Dec 2019 18:00:43 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48cbbbce208b5a8e143d43012de06b33cd12dc212fae3e3f6cf28b1acd900861`  
		Last Modified: Thu, 12 Dec 2019 00:09:45 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f72bd77f828256b25eb7375c46fdec577565bc53d89a05fa8a100796450f599`  
		Last Modified: Thu, 12 Dec 2019 00:09:45 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d00e37fa3cf44154da5932563d6cfcff58333ffd56b34c2933a9b14f273b96`  
		Last Modified: Thu, 12 Dec 2019 00:09:42 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e5c13eeee73b3c63164fa7984e8859a050bb173cb69c2b162e7d93845778b5f`  
		Last Modified: Thu, 12 Dec 2019 00:10:40 GMT  
		Size: 453.1 MB (453066744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de21f5bd53ce10a88ff8e77419719b9a2283c1a3f88706ebc56116df5d13e82e`  
		Last Modified: Thu, 12 Dec 2019 00:09:42 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aecef79094cae66ab1003365b8a64bce825e973f8fc6fdaac26462fb31363a15`  
		Last Modified: Thu, 12 Dec 2019 00:09:43 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c1b6171741d09ad84e50e1a007624e0807534f6adc039d848e5915d26bcdfa9`  
		Last Modified: Thu, 12 Dec 2019 00:09:43 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4-windowsservercore-1809`

```console
$ docker pull mongo@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:

## `mongo:4-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:db78a7411279c77330a0e1cbc4bdf6db701b37e68a3071b4ae0a8186818828f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3384; amd64

### `mongo:4-windowsservercore-ltsc2016` - windows version 10.0.14393.3384; amd64

```console
$ docker pull mongo@sha256:37ed0ce402c453d82362c8674a95a84ccdc02c9864bfa4fc8170d49d42584a92
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5816058219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fb916a127f9cd60ef9757a818d2c965590bd5303ed4476b1c5a8445ac0b6e2a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 15:47:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 23:35:26 GMT
ENV MONGO_VERSION=4.2.1
# Wed, 11 Dec 2019 23:35:27 GMT
ENV MONGO_DOWNLOAD_URL=https://downloads.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.1-signed.msi
# Wed, 11 Dec 2019 23:35:28 GMT
ENV MONGO_DOWNLOAD_SHA256=0bd9f5361d21cf358156e8e18aae3f4bc0298e9949b4b988c4b15b52913f91d6
# Wed, 11 Dec 2019 23:44:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Dec 2019 23:44:48 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Dec 2019 23:44:50 GMT
EXPOSE 27017
# Wed, 11 Dec 2019 23:44:52 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d23dffb4f7b6ebd1cceaac955d664d79467da76c4749d2a37d98556996d8bb0a`  
		Last Modified: Wed, 11 Dec 2019 18:01:38 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c30838129c9ab8ebc7cfc1437e4655ad2fcbf99b7c2a4f618f0dadeb02ee9b1`  
		Last Modified: Thu, 12 Dec 2019 00:08:43 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e12474c86cd0cf6cec9ffc98ee72da8f5c5ef236665b487ed4590f3083cb5d`  
		Last Modified: Thu, 12 Dec 2019 00:08:43 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de05e906a577fa8f95e8df9641ed2d7b042e8ab039218c711f9be88e153f43c4`  
		Last Modified: Thu, 12 Dec 2019 00:08:40 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0735cfc26b92c99aa40bf6c1feb6c344f5d7113c006c50441f5304fe92fd8285`  
		Last Modified: Thu, 12 Dec 2019 00:09:03 GMT  
		Size: 93.3 MB (93345990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77636ccac26ca06e73af52744671d5c6ae3db8960b110a60b0e95ed0231a9619`  
		Last Modified: Thu, 12 Dec 2019 00:08:41 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e83b06286df83053a894432b81bf6c78acc9a1000308697438915c8072f4210`  
		Last Modified: Thu, 12 Dec 2019 00:08:40 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262bd20abcdfdee728fa18bff25d7071edeb206e56c11f9b4a4080018ca2db1f`  
		Last Modified: Thu, 12 Dec 2019 00:08:40 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:bionic`

```console
$ docker pull mongo@sha256:e7fb2214ca6898ea12017aaf0c7a45657a9d0e7abac1d7931b9451d2bd236f57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `mongo:bionic` - linux; amd64

```console
$ docker pull mongo@sha256:52c3314bee611f91d37b9b1bc0cc2755b1388f2de5b396b441f3fe94bef6c56c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.3 MB (147285849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:965553e202a44592bc26d8c076eafef996a6dfc0de5bb2c1cf1795cd3b3a7373`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 31 Oct 2019 22:20:35 GMT
ADD file:a48a5dc1b9dbfc632f6cf86fe27b770b63f07a115c98c4465dc184e303a4efa1 in / 
# Thu, 31 Oct 2019 22:20:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:20:36 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:20:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:20:37 GMT
CMD ["/bin/bash"]
# Fri, 01 Nov 2019 00:34:46 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 01 Nov 2019 00:34:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Nov 2019 00:34:56 GMT
ENV GOSU_VERSION=1.11
# Fri, 01 Nov 2019 00:34:56 GMT
ENV JSYAML_VERSION=3.13.0
# Fri, 01 Nov 2019 00:35:07 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 01 Nov 2019 00:35:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Nov 2019 00:35:09 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 01 Nov 2019 00:35:10 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 01 Nov 2019 00:35:10 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 01 Nov 2019 00:35:10 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 01 Nov 2019 00:35:10 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 01 Nov 2019 00:35:10 GMT
ENV MONGO_MAJOR=4.2
# Fri, 01 Nov 2019 00:35:11 GMT
ENV MONGO_VERSION=4.2.1
# Fri, 01 Nov 2019 00:35:11 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 01 Nov 2019 00:35:29 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 01 Nov 2019 00:35:29 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 01 Nov 2019 00:35:30 GMT
VOLUME [/data/db /data/configdb]
# Fri, 01 Nov 2019 00:35:30 GMT
COPY file:021686a669d0d1d1cbb99d6ca84ff8de10577b78ea985b8cdab9d75b347a3bd0 in /usr/local/bin/ 
# Fri, 01 Nov 2019 00:35:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Nov 2019 00:35:30 GMT
EXPOSE 27017
# Fri, 01 Nov 2019 00:35:30 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7ddbc47eeb70dc7f08e410a6667948b87ff3883024eb41478b44ef9a81bf400c`  
		Last Modified: Wed, 30 Oct 2019 00:25:34 GMT  
		Size: 26.7 MB (26688847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1bbdc448b7263673926b8fe2e88491e5083a8b4b06ddfabf311f2fc5f27e2ff`  
		Last Modified: Thu, 31 Oct 2019 22:21:39 GMT  
		Size: 35.4 KB (35362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3b70e3904492c753652606df4726430426f42ea56e06ea924d6fea7ae162a1`  
		Last Modified: Thu, 31 Oct 2019 22:21:39 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45d437916d5781043432f2d72608049dcf74ddbd27daa01a25fa63c8f1b9adc4`  
		Last Modified: Thu, 31 Oct 2019 22:21:39 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e119fb0e0a556b13af304b430ee02ab7dae340974ed1c56c071f8b76ba94fce8`  
		Last Modified: Fri, 01 Nov 2019 00:37:26 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f0b9bae1ea1da827453099df499d277582fee378b02632492f5960b3199f45`  
		Last Modified: Fri, 01 Nov 2019 00:37:27 GMT  
		Size: 3.0 MB (2981726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e7c2967f1132938ce99899a660345acb7d81a2722d03be593c501f2d5a0fb5`  
		Last Modified: Fri, 01 Nov 2019 00:37:28 GMT  
		Size: 5.8 MB (5763200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a945568374aab4d5559c42c26f5e91d0077eaa2fc6f4ac2de12681665847c1`  
		Last Modified: Fri, 01 Nov 2019 00:37:25 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93333bc225a750104af3ea7a4dee020f14d95b1f7e9f3d3bbd4629a0d38cbeb8`  
		Last Modified: Fri, 01 Nov 2019 00:37:25 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c10bd6c9bdce8efa69364bade1114e6089a95a8c9b652fad7f4e5e169f882a`  
		Last Modified: Fri, 01 Nov 2019 00:37:24 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4e3538e99cfab06dca9314aa7ee1d77d09973875de8c9505159544571ca423`  
		Last Modified: Fri, 01 Nov 2019 00:37:50 GMT  
		Size: 111.8 MB (111807903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1164b51d180a68eda4b69db7227a8ef9d79924dba229c255fb45a45e7704bdbd`  
		Last Modified: Fri, 01 Nov 2019 00:37:24 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a715a7d71f27cafd081768bdaeddc9538ab8060043ae9d59e20cb067fcf98b5e`  
		Last Modified: Fri, 01 Nov 2019 00:37:25 GMT  
		Size: 4.0 KB (4007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:bionic` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:922dfe530d2a4bad26786c20f5ab9667bf8096c5378615ee1fb3327e1e45ba46
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136338781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f09d4aa5ffaafb22631c9c99c5038d690874b461d69736e308b6d3f5c9bbd57b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 31 Oct 2019 22:40:37 GMT
ADD file:4c6cab77271e86386e8f3d4ecf06c17a3e9339481bea878a706d2c5dc4a0addd in / 
# Thu, 31 Oct 2019 22:40:40 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:40:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:40:43 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:40:44 GMT
CMD ["/bin/bash"]
# Fri, 01 Nov 2019 00:48:13 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 01 Nov 2019 00:48:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Nov 2019 00:48:29 GMT
ENV GOSU_VERSION=1.11
# Fri, 01 Nov 2019 00:48:30 GMT
ENV JSYAML_VERSION=3.13.0
# Fri, 01 Nov 2019 00:48:54 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 01 Nov 2019 00:48:57 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Nov 2019 00:48:57 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 01 Nov 2019 00:49:00 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 01 Nov 2019 00:49:00 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 01 Nov 2019 00:49:01 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 01 Nov 2019 00:49:02 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 01 Nov 2019 00:49:03 GMT
ENV MONGO_MAJOR=4.2
# Fri, 01 Nov 2019 00:49:04 GMT
ENV MONGO_VERSION=4.2.1
# Fri, 01 Nov 2019 00:49:06 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 01 Nov 2019 00:49:30 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 01 Nov 2019 00:49:34 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 01 Nov 2019 00:49:35 GMT
VOLUME [/data/db /data/configdb]
# Fri, 01 Nov 2019 00:49:35 GMT
COPY file:021686a669d0d1d1cbb99d6ca84ff8de10577b78ea985b8cdab9d75b347a3bd0 in /usr/local/bin/ 
# Fri, 01 Nov 2019 00:49:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Nov 2019 00:49:37 GMT
EXPOSE 27017
# Fri, 01 Nov 2019 00:49:39 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:6531af3558948c8839fd7cc7eb7062aa86bfae891870ccaafd554ac65c97971b`  
		Last Modified: Thu, 31 Oct 2019 22:42:23 GMT  
		Size: 23.7 MB (23718403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f7942d2fb7381ee1735a4c972ef45c89b6521902e6eba024d4791dfd069def`  
		Last Modified: Thu, 31 Oct 2019 22:42:16 GMT  
		Size: 35.2 KB (35198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdce94e690d563311eb8b102b49e94a01b2a4c965daa9e33d5e59168dc4327e0`  
		Last Modified: Thu, 31 Oct 2019 22:42:16 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96a89ada1c32e30a1998945a8785c18bcdce55dcfe2b666bb587d432255cb11`  
		Last Modified: Thu, 31 Oct 2019 22:42:16 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441c8b285da3534c6705c81b056f0421dc29aff21e3b8e891572ee58969b23c4`  
		Last Modified: Fri, 01 Nov 2019 00:51:57 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3369e8993485be78046aa93778ceb9f0ac9a9cd1460c56dd0a39b5612a2bf0db`  
		Last Modified: Fri, 01 Nov 2019 00:51:58 GMT  
		Size: 2.7 MB (2675614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aedf06151273427f8c9155f17ce3804e486f188c768a9b1395a8e808091bfa59`  
		Last Modified: Fri, 01 Nov 2019 00:51:58 GMT  
		Size: 5.3 MB (5282727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb0173982fa974e75dbc470008149e563eb935f7027577971b32bf9790721d4`  
		Last Modified: Fri, 01 Nov 2019 00:51:57 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ff79f67ba8dbf80063a12f5296a984d5fe453bf212e7aa4562c6e9b2109d01`  
		Last Modified: Fri, 01 Nov 2019 00:51:55 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6085923db4441f085ae2476ca6fa391e1df060ca33644fb82a401201a757959f`  
		Last Modified: Fri, 01 Nov 2019 00:51:55 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50380edb4431c149b589a7bff3db64481717f9197cc57e99ea9cd2e278dab9b6`  
		Last Modified: Fri, 01 Nov 2019 00:52:21 GMT  
		Size: 104.6 MB (104617931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e667dd7db0918baac9e775b56ad7dbb1ec2806eee8f7415812d13f0dd700ed0`  
		Last Modified: Fri, 01 Nov 2019 00:51:55 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:545348b868a6ab6133facf259e76520240f6e7a6f4cdf4e53b38215cc9929476`  
		Last Modified: Fri, 01 Nov 2019 00:51:55 GMT  
		Size: 4.0 KB (4003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:bionic` - linux; s390x

```console
$ docker pull mongo@sha256:76cdaab6ec75306255226b0ba785dd113c2f264320382e88368ae1157f93ddbc
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.5 MB (143531232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0000651cfa9056c242a341ec396f1b03a548a1d8486b039d3b6fd5d010751ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 31 Oct 2019 22:41:56 GMT
ADD file:6e6c5c69d7791dc0b62c8d03fc0c5051c6291e08dfc4e11abbdc333bc6f44359 in / 
# Thu, 31 Oct 2019 22:41:58 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:41:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:42:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:42:01 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 23:16:28 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Thu, 31 Oct 2019 23:16:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 31 Oct 2019 23:16:46 GMT
ENV GOSU_VERSION=1.11
# Thu, 31 Oct 2019 23:16:46 GMT
ENV JSYAML_VERSION=3.13.0
# Thu, 31 Oct 2019 23:17:14 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 31 Oct 2019 23:17:15 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 31 Oct 2019 23:17:15 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Thu, 31 Oct 2019 23:17:18 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 31 Oct 2019 23:17:18 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 31 Oct 2019 23:17:18 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 31 Oct 2019 23:17:18 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 31 Oct 2019 23:17:19 GMT
ENV MONGO_MAJOR=4.2
# Thu, 31 Oct 2019 23:17:19 GMT
ENV MONGO_VERSION=4.2.1
# Thu, 31 Oct 2019 23:17:21 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Thu, 31 Oct 2019 23:18:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Thu, 31 Oct 2019 23:18:06 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Thu, 31 Oct 2019 23:18:06 GMT
VOLUME [/data/db /data/configdb]
# Thu, 31 Oct 2019 23:18:07 GMT
COPY file:021686a669d0d1d1cbb99d6ca84ff8de10577b78ea985b8cdab9d75b347a3bd0 in /usr/local/bin/ 
# Thu, 31 Oct 2019 23:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 31 Oct 2019 23:18:08 GMT
EXPOSE 27017
# Thu, 31 Oct 2019 23:18:08 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:617b55fd1ba95b3ed68226101c9b2568ed00a9b7c50959230d2124648f3a47d2`  
		Last Modified: Thu, 31 Oct 2019 22:43:47 GMT  
		Size: 25.4 MB (25364650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee6ed80b799b3b7d7d66e31ba7e61be1f8d02732bccb1a22d1f14c65f9cea21`  
		Last Modified: Thu, 31 Oct 2019 22:43:42 GMT  
		Size: 36.2 KB (36173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc71634b6bba51b68da661aedfd0876ba93b197653cc94323ca050369bef0bc`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 841.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e017bfda3869ce68902d01d6dfb0fe74964f8c598ea31bc77825772e58a122b`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43ce05cccebf9f7a410bbace7582d3f6a8a6eb8f969e738365ff52fa41bef56`  
		Last Modified: Thu, 31 Oct 2019 23:18:26 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232ad1433592ae3e49689f9a399155d8cd4cb66e85d3e9a3371f64c5d3767ef5`  
		Last Modified: Thu, 31 Oct 2019 23:18:27 GMT  
		Size: 2.7 MB (2714202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfb83020b47608042582b07eac59bfe53f87d076f429e2030150fce7671fcfc`  
		Last Modified: Thu, 31 Oct 2019 23:18:28 GMT  
		Size: 5.7 MB (5684577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e67294f8ac41b2fbbb98389025f6a2934cd3e85f08b50641d96ce6fd42c5d4`  
		Last Modified: Thu, 31 Oct 2019 23:18:25 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10477e3f19872878bbd97b9b1d529a9cda966b6dab49c609ca17a815f56eaf03`  
		Last Modified: Thu, 31 Oct 2019 23:18:24 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd80e3c144d231663b9fc4f19de43fe431596d85adb3fd80db6e1965f649b99`  
		Last Modified: Thu, 31 Oct 2019 23:18:23 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390cef7a4233b0430f858343c7ffa603238382f6b3d57400fba4bc37dc1fc338`  
		Last Modified: Thu, 31 Oct 2019 23:18:49 GMT  
		Size: 109.7 MB (109722811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ab2a7a00460c93578481306a6e5212441ae6f399678d3a0938105339ff3659`  
		Last Modified: Thu, 31 Oct 2019 23:18:24 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729e6c5603fe8d82346fcc9450f163fdd06d4f77ad73e59fca74447aa971f9ba`  
		Last Modified: Thu, 31 Oct 2019 23:18:23 GMT  
		Size: 4.0 KB (4005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:latest`

```console
$ docker pull mongo@sha256:6ca49afbcb2b44aedf53f5f27b20c99813f500981b6d62193aa770e8340461cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x
	-	windows version 10.0.14393.3384; amd64
	-	windows version 10.0.17134.1184; amd64

### `mongo:latest` - linux; amd64

```console
$ docker pull mongo@sha256:52c3314bee611f91d37b9b1bc0cc2755b1388f2de5b396b441f3fe94bef6c56c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.3 MB (147285849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:965553e202a44592bc26d8c076eafef996a6dfc0de5bb2c1cf1795cd3b3a7373`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 31 Oct 2019 22:20:35 GMT
ADD file:a48a5dc1b9dbfc632f6cf86fe27b770b63f07a115c98c4465dc184e303a4efa1 in / 
# Thu, 31 Oct 2019 22:20:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:20:36 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:20:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:20:37 GMT
CMD ["/bin/bash"]
# Fri, 01 Nov 2019 00:34:46 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 01 Nov 2019 00:34:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Nov 2019 00:34:56 GMT
ENV GOSU_VERSION=1.11
# Fri, 01 Nov 2019 00:34:56 GMT
ENV JSYAML_VERSION=3.13.0
# Fri, 01 Nov 2019 00:35:07 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 01 Nov 2019 00:35:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Nov 2019 00:35:09 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 01 Nov 2019 00:35:10 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 01 Nov 2019 00:35:10 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 01 Nov 2019 00:35:10 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 01 Nov 2019 00:35:10 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 01 Nov 2019 00:35:10 GMT
ENV MONGO_MAJOR=4.2
# Fri, 01 Nov 2019 00:35:11 GMT
ENV MONGO_VERSION=4.2.1
# Fri, 01 Nov 2019 00:35:11 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 01 Nov 2019 00:35:29 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 01 Nov 2019 00:35:29 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 01 Nov 2019 00:35:30 GMT
VOLUME [/data/db /data/configdb]
# Fri, 01 Nov 2019 00:35:30 GMT
COPY file:021686a669d0d1d1cbb99d6ca84ff8de10577b78ea985b8cdab9d75b347a3bd0 in /usr/local/bin/ 
# Fri, 01 Nov 2019 00:35:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Nov 2019 00:35:30 GMT
EXPOSE 27017
# Fri, 01 Nov 2019 00:35:30 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7ddbc47eeb70dc7f08e410a6667948b87ff3883024eb41478b44ef9a81bf400c`  
		Last Modified: Wed, 30 Oct 2019 00:25:34 GMT  
		Size: 26.7 MB (26688847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1bbdc448b7263673926b8fe2e88491e5083a8b4b06ddfabf311f2fc5f27e2ff`  
		Last Modified: Thu, 31 Oct 2019 22:21:39 GMT  
		Size: 35.4 KB (35362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3b70e3904492c753652606df4726430426f42ea56e06ea924d6fea7ae162a1`  
		Last Modified: Thu, 31 Oct 2019 22:21:39 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45d437916d5781043432f2d72608049dcf74ddbd27daa01a25fa63c8f1b9adc4`  
		Last Modified: Thu, 31 Oct 2019 22:21:39 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e119fb0e0a556b13af304b430ee02ab7dae340974ed1c56c071f8b76ba94fce8`  
		Last Modified: Fri, 01 Nov 2019 00:37:26 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f0b9bae1ea1da827453099df499d277582fee378b02632492f5960b3199f45`  
		Last Modified: Fri, 01 Nov 2019 00:37:27 GMT  
		Size: 3.0 MB (2981726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e7c2967f1132938ce99899a660345acb7d81a2722d03be593c501f2d5a0fb5`  
		Last Modified: Fri, 01 Nov 2019 00:37:28 GMT  
		Size: 5.8 MB (5763200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a945568374aab4d5559c42c26f5e91d0077eaa2fc6f4ac2de12681665847c1`  
		Last Modified: Fri, 01 Nov 2019 00:37:25 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93333bc225a750104af3ea7a4dee020f14d95b1f7e9f3d3bbd4629a0d38cbeb8`  
		Last Modified: Fri, 01 Nov 2019 00:37:25 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c10bd6c9bdce8efa69364bade1114e6089a95a8c9b652fad7f4e5e169f882a`  
		Last Modified: Fri, 01 Nov 2019 00:37:24 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4e3538e99cfab06dca9314aa7ee1d77d09973875de8c9505159544571ca423`  
		Last Modified: Fri, 01 Nov 2019 00:37:50 GMT  
		Size: 111.8 MB (111807903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1164b51d180a68eda4b69db7227a8ef9d79924dba229c255fb45a45e7704bdbd`  
		Last Modified: Fri, 01 Nov 2019 00:37:24 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a715a7d71f27cafd081768bdaeddc9538ab8060043ae9d59e20cb067fcf98b5e`  
		Last Modified: Fri, 01 Nov 2019 00:37:25 GMT  
		Size: 4.0 KB (4007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:922dfe530d2a4bad26786c20f5ab9667bf8096c5378615ee1fb3327e1e45ba46
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136338781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f09d4aa5ffaafb22631c9c99c5038d690874b461d69736e308b6d3f5c9bbd57b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 31 Oct 2019 22:40:37 GMT
ADD file:4c6cab77271e86386e8f3d4ecf06c17a3e9339481bea878a706d2c5dc4a0addd in / 
# Thu, 31 Oct 2019 22:40:40 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:40:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:40:43 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:40:44 GMT
CMD ["/bin/bash"]
# Fri, 01 Nov 2019 00:48:13 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Fri, 01 Nov 2019 00:48:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Nov 2019 00:48:29 GMT
ENV GOSU_VERSION=1.11
# Fri, 01 Nov 2019 00:48:30 GMT
ENV JSYAML_VERSION=3.13.0
# Fri, 01 Nov 2019 00:48:54 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 01 Nov 2019 00:48:57 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Nov 2019 00:48:57 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Fri, 01 Nov 2019 00:49:00 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Fri, 01 Nov 2019 00:49:00 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 01 Nov 2019 00:49:01 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 01 Nov 2019 00:49:02 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 01 Nov 2019 00:49:03 GMT
ENV MONGO_MAJOR=4.2
# Fri, 01 Nov 2019 00:49:04 GMT
ENV MONGO_VERSION=4.2.1
# Fri, 01 Nov 2019 00:49:06 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Fri, 01 Nov 2019 00:49:30 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Fri, 01 Nov 2019 00:49:34 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Fri, 01 Nov 2019 00:49:35 GMT
VOLUME [/data/db /data/configdb]
# Fri, 01 Nov 2019 00:49:35 GMT
COPY file:021686a669d0d1d1cbb99d6ca84ff8de10577b78ea985b8cdab9d75b347a3bd0 in /usr/local/bin/ 
# Fri, 01 Nov 2019 00:49:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Nov 2019 00:49:37 GMT
EXPOSE 27017
# Fri, 01 Nov 2019 00:49:39 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:6531af3558948c8839fd7cc7eb7062aa86bfae891870ccaafd554ac65c97971b`  
		Last Modified: Thu, 31 Oct 2019 22:42:23 GMT  
		Size: 23.7 MB (23718403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f7942d2fb7381ee1735a4c972ef45c89b6521902e6eba024d4791dfd069def`  
		Last Modified: Thu, 31 Oct 2019 22:42:16 GMT  
		Size: 35.2 KB (35198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdce94e690d563311eb8b102b49e94a01b2a4c965daa9e33d5e59168dc4327e0`  
		Last Modified: Thu, 31 Oct 2019 22:42:16 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96a89ada1c32e30a1998945a8785c18bcdce55dcfe2b666bb587d432255cb11`  
		Last Modified: Thu, 31 Oct 2019 22:42:16 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441c8b285da3534c6705c81b056f0421dc29aff21e3b8e891572ee58969b23c4`  
		Last Modified: Fri, 01 Nov 2019 00:51:57 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3369e8993485be78046aa93778ceb9f0ac9a9cd1460c56dd0a39b5612a2bf0db`  
		Last Modified: Fri, 01 Nov 2019 00:51:58 GMT  
		Size: 2.7 MB (2675614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aedf06151273427f8c9155f17ce3804e486f188c768a9b1395a8e808091bfa59`  
		Last Modified: Fri, 01 Nov 2019 00:51:58 GMT  
		Size: 5.3 MB (5282727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb0173982fa974e75dbc470008149e563eb935f7027577971b32bf9790721d4`  
		Last Modified: Fri, 01 Nov 2019 00:51:57 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ff79f67ba8dbf80063a12f5296a984d5fe453bf212e7aa4562c6e9b2109d01`  
		Last Modified: Fri, 01 Nov 2019 00:51:55 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6085923db4441f085ae2476ca6fa391e1df060ca33644fb82a401201a757959f`  
		Last Modified: Fri, 01 Nov 2019 00:51:55 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50380edb4431c149b589a7bff3db64481717f9197cc57e99ea9cd2e278dab9b6`  
		Last Modified: Fri, 01 Nov 2019 00:52:21 GMT  
		Size: 104.6 MB (104617931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e667dd7db0918baac9e775b56ad7dbb1ec2806eee8f7415812d13f0dd700ed0`  
		Last Modified: Fri, 01 Nov 2019 00:51:55 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:545348b868a6ab6133facf259e76520240f6e7a6f4cdf4e53b38215cc9929476`  
		Last Modified: Fri, 01 Nov 2019 00:51:55 GMT  
		Size: 4.0 KB (4003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - linux; s390x

```console
$ docker pull mongo@sha256:76cdaab6ec75306255226b0ba785dd113c2f264320382e88368ae1157f93ddbc
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.5 MB (143531232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0000651cfa9056c242a341ec396f1b03a548a1d8486b039d3b6fd5d010751ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 31 Oct 2019 22:41:56 GMT
ADD file:6e6c5c69d7791dc0b62c8d03fc0c5051c6291e08dfc4e11abbdc333bc6f44359 in / 
# Thu, 31 Oct 2019 22:41:58 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 31 Oct 2019 22:41:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 31 Oct 2019 22:42:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 31 Oct 2019 22:42:01 GMT
CMD ["/bin/bash"]
# Thu, 31 Oct 2019 23:16:28 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Thu, 31 Oct 2019 23:16:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 31 Oct 2019 23:16:46 GMT
ENV GOSU_VERSION=1.11
# Thu, 31 Oct 2019 23:16:46 GMT
ENV JSYAML_VERSION=3.13.0
# Thu, 31 Oct 2019 23:17:14 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 31 Oct 2019 23:17:15 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 31 Oct 2019 23:17:15 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Thu, 31 Oct 2019 23:17:18 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 31 Oct 2019 23:17:18 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 31 Oct 2019 23:17:18 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 31 Oct 2019 23:17:18 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 31 Oct 2019 23:17:19 GMT
ENV MONGO_MAJOR=4.2
# Thu, 31 Oct 2019 23:17:19 GMT
ENV MONGO_VERSION=4.2.1
# Thu, 31 Oct 2019 23:17:21 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Thu, 31 Oct 2019 23:18:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Thu, 31 Oct 2019 23:18:06 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Thu, 31 Oct 2019 23:18:06 GMT
VOLUME [/data/db /data/configdb]
# Thu, 31 Oct 2019 23:18:07 GMT
COPY file:021686a669d0d1d1cbb99d6ca84ff8de10577b78ea985b8cdab9d75b347a3bd0 in /usr/local/bin/ 
# Thu, 31 Oct 2019 23:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 31 Oct 2019 23:18:08 GMT
EXPOSE 27017
# Thu, 31 Oct 2019 23:18:08 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:617b55fd1ba95b3ed68226101c9b2568ed00a9b7c50959230d2124648f3a47d2`  
		Last Modified: Thu, 31 Oct 2019 22:43:47 GMT  
		Size: 25.4 MB (25364650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee6ed80b799b3b7d7d66e31ba7e61be1f8d02732bccb1a22d1f14c65f9cea21`  
		Last Modified: Thu, 31 Oct 2019 22:43:42 GMT  
		Size: 36.2 KB (36173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc71634b6bba51b68da661aedfd0876ba93b197653cc94323ca050369bef0bc`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 841.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e017bfda3869ce68902d01d6dfb0fe74964f8c598ea31bc77825772e58a122b`  
		Last Modified: Thu, 31 Oct 2019 22:43:43 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43ce05cccebf9f7a410bbace7582d3f6a8a6eb8f969e738365ff52fa41bef56`  
		Last Modified: Thu, 31 Oct 2019 23:18:26 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232ad1433592ae3e49689f9a399155d8cd4cb66e85d3e9a3371f64c5d3767ef5`  
		Last Modified: Thu, 31 Oct 2019 23:18:27 GMT  
		Size: 2.7 MB (2714202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfb83020b47608042582b07eac59bfe53f87d076f429e2030150fce7671fcfc`  
		Last Modified: Thu, 31 Oct 2019 23:18:28 GMT  
		Size: 5.7 MB (5684577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e67294f8ac41b2fbbb98389025f6a2934cd3e85f08b50641d96ce6fd42c5d4`  
		Last Modified: Thu, 31 Oct 2019 23:18:25 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10477e3f19872878bbd97b9b1d529a9cda966b6dab49c609ca17a815f56eaf03`  
		Last Modified: Thu, 31 Oct 2019 23:18:24 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd80e3c144d231663b9fc4f19de43fe431596d85adb3fd80db6e1965f649b99`  
		Last Modified: Thu, 31 Oct 2019 23:18:23 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390cef7a4233b0430f858343c7ffa603238382f6b3d57400fba4bc37dc1fc338`  
		Last Modified: Thu, 31 Oct 2019 23:18:49 GMT  
		Size: 109.7 MB (109722811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ab2a7a00460c93578481306a6e5212441ae6f399678d3a0938105339ff3659`  
		Last Modified: Thu, 31 Oct 2019 23:18:24 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729e6c5603fe8d82346fcc9450f163fdd06d4f77ad73e59fca74447aa971f9ba`  
		Last Modified: Thu, 31 Oct 2019 23:18:23 GMT  
		Size: 4.0 KB (4005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.14393.3384; amd64

```console
$ docker pull mongo@sha256:37ed0ce402c453d82362c8674a95a84ccdc02c9864bfa4fc8170d49d42584a92
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5816058219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fb916a127f9cd60ef9757a818d2c965590bd5303ed4476b1c5a8445ac0b6e2a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 15:47:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 23:35:26 GMT
ENV MONGO_VERSION=4.2.1
# Wed, 11 Dec 2019 23:35:27 GMT
ENV MONGO_DOWNLOAD_URL=https://downloads.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.1-signed.msi
# Wed, 11 Dec 2019 23:35:28 GMT
ENV MONGO_DOWNLOAD_SHA256=0bd9f5361d21cf358156e8e18aae3f4bc0298e9949b4b988c4b15b52913f91d6
# Wed, 11 Dec 2019 23:44:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Dec 2019 23:44:48 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Dec 2019 23:44:50 GMT
EXPOSE 27017
# Wed, 11 Dec 2019 23:44:52 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d23dffb4f7b6ebd1cceaac955d664d79467da76c4749d2a37d98556996d8bb0a`  
		Last Modified: Wed, 11 Dec 2019 18:01:38 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c30838129c9ab8ebc7cfc1437e4655ad2fcbf99b7c2a4f618f0dadeb02ee9b1`  
		Last Modified: Thu, 12 Dec 2019 00:08:43 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e12474c86cd0cf6cec9ffc98ee72da8f5c5ef236665b487ed4590f3083cb5d`  
		Last Modified: Thu, 12 Dec 2019 00:08:43 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de05e906a577fa8f95e8df9641ed2d7b042e8ab039218c711f9be88e153f43c4`  
		Last Modified: Thu, 12 Dec 2019 00:08:40 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0735cfc26b92c99aa40bf6c1feb6c344f5d7113c006c50441f5304fe92fd8285`  
		Last Modified: Thu, 12 Dec 2019 00:09:03 GMT  
		Size: 93.3 MB (93345990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77636ccac26ca06e73af52744671d5c6ae3db8960b110a60b0e95ed0231a9619`  
		Last Modified: Thu, 12 Dec 2019 00:08:41 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e83b06286df83053a894432b81bf6c78acc9a1000308697438915c8072f4210`  
		Last Modified: Thu, 12 Dec 2019 00:08:40 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262bd20abcdfdee728fa18bff25d7071edeb206e56c11f9b4a4080018ca2db1f`  
		Last Modified: Thu, 12 Dec 2019 00:08:40 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.17134.1184; amd64

```console
$ docker pull mongo@sha256:672798fb05567fe529909cf3f81422c76d5fe1a2bdbd1974abd9aa238b639f36
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2809636910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:def4de6e07cdaff0556a068451bdd6043d77ee91d167288d24f922343dab649d`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 12 Apr 2018 09:20:54 GMT
RUN Apply image 1803-RTM-amd64
# Wed, 04 Dec 2019 15:21:18 GMT
RUN Install update 1803-amd64
# Wed, 11 Dec 2019 15:36:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 23:45:17 GMT
ENV MONGO_VERSION=4.2.1
# Wed, 11 Dec 2019 23:45:19 GMT
ENV MONGO_DOWNLOAD_URL=https://downloads.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.1-signed.msi
# Wed, 11 Dec 2019 23:45:20 GMT
ENV MONGO_DOWNLOAD_SHA256=0bd9f5361d21cf358156e8e18aae3f4bc0298e9949b4b988c4b15b52913f91d6
# Thu, 12 Dec 2019 00:03:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 12 Dec 2019 00:03:17 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 12 Dec 2019 00:03:18 GMT
EXPOSE 27017
# Thu, 12 Dec 2019 00:03:20 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:d9e8b01179bfc94a5bdb1810fbd76b999aa52016001ace2d3a4c4bc7065a9601`  
		Last Modified: Tue, 18 Sep 2018 22:43:55 GMT  
		Size: 1.7 GB (1659688273 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d117323cd539488e5ef3bef575a41fa714d83119b0da1896607d96ec2a5e3b52`  
		Size: 696.9 MB (696873564 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:70c803815d644f3772896add8df055dfd33f5934921ca0c57efc290d42454abf`  
		Last Modified: Wed, 11 Dec 2019 18:00:43 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48cbbbce208b5a8e143d43012de06b33cd12dc212fae3e3f6cf28b1acd900861`  
		Last Modified: Thu, 12 Dec 2019 00:09:45 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f72bd77f828256b25eb7375c46fdec577565bc53d89a05fa8a100796450f599`  
		Last Modified: Thu, 12 Dec 2019 00:09:45 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d00e37fa3cf44154da5932563d6cfcff58333ffd56b34c2933a9b14f273b96`  
		Last Modified: Thu, 12 Dec 2019 00:09:42 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e5c13eeee73b3c63164fa7984e8859a050bb173cb69c2b162e7d93845778b5f`  
		Last Modified: Thu, 12 Dec 2019 00:10:40 GMT  
		Size: 453.1 MB (453066744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de21f5bd53ce10a88ff8e77419719b9a2283c1a3f88706ebc56116df5d13e82e`  
		Last Modified: Thu, 12 Dec 2019 00:09:42 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aecef79094cae66ab1003365b8a64bce825e973f8fc6fdaac26462fb31363a15`  
		Last Modified: Thu, 12 Dec 2019 00:09:43 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c1b6171741d09ad84e50e1a007624e0807534f6adc039d848e5915d26bcdfa9`  
		Last Modified: Thu, 12 Dec 2019 00:09:43 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:windowsservercore`

```console
$ docker pull mongo@sha256:c310176382896f4a10beb26fbcfdd25844d3ce06c0267a7a470b1f4f7e60576e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3384; amd64
	-	windows version 10.0.17134.1184; amd64

### `mongo:windowsservercore` - windows version 10.0.14393.3384; amd64

```console
$ docker pull mongo@sha256:37ed0ce402c453d82362c8674a95a84ccdc02c9864bfa4fc8170d49d42584a92
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5816058219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fb916a127f9cd60ef9757a818d2c965590bd5303ed4476b1c5a8445ac0b6e2a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 15:47:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 23:35:26 GMT
ENV MONGO_VERSION=4.2.1
# Wed, 11 Dec 2019 23:35:27 GMT
ENV MONGO_DOWNLOAD_URL=https://downloads.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.1-signed.msi
# Wed, 11 Dec 2019 23:35:28 GMT
ENV MONGO_DOWNLOAD_SHA256=0bd9f5361d21cf358156e8e18aae3f4bc0298e9949b4b988c4b15b52913f91d6
# Wed, 11 Dec 2019 23:44:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Dec 2019 23:44:48 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Dec 2019 23:44:50 GMT
EXPOSE 27017
# Wed, 11 Dec 2019 23:44:52 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d23dffb4f7b6ebd1cceaac955d664d79467da76c4749d2a37d98556996d8bb0a`  
		Last Modified: Wed, 11 Dec 2019 18:01:38 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c30838129c9ab8ebc7cfc1437e4655ad2fcbf99b7c2a4f618f0dadeb02ee9b1`  
		Last Modified: Thu, 12 Dec 2019 00:08:43 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e12474c86cd0cf6cec9ffc98ee72da8f5c5ef236665b487ed4590f3083cb5d`  
		Last Modified: Thu, 12 Dec 2019 00:08:43 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de05e906a577fa8f95e8df9641ed2d7b042e8ab039218c711f9be88e153f43c4`  
		Last Modified: Thu, 12 Dec 2019 00:08:40 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0735cfc26b92c99aa40bf6c1feb6c344f5d7113c006c50441f5304fe92fd8285`  
		Last Modified: Thu, 12 Dec 2019 00:09:03 GMT  
		Size: 93.3 MB (93345990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77636ccac26ca06e73af52744671d5c6ae3db8960b110a60b0e95ed0231a9619`  
		Last Modified: Thu, 12 Dec 2019 00:08:41 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e83b06286df83053a894432b81bf6c78acc9a1000308697438915c8072f4210`  
		Last Modified: Thu, 12 Dec 2019 00:08:40 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262bd20abcdfdee728fa18bff25d7071edeb206e56c11f9b4a4080018ca2db1f`  
		Last Modified: Thu, 12 Dec 2019 00:08:40 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:windowsservercore` - windows version 10.0.17134.1184; amd64

```console
$ docker pull mongo@sha256:672798fb05567fe529909cf3f81422c76d5fe1a2bdbd1974abd9aa238b639f36
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2809636910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:def4de6e07cdaff0556a068451bdd6043d77ee91d167288d24f922343dab649d`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 12 Apr 2018 09:20:54 GMT
RUN Apply image 1803-RTM-amd64
# Wed, 04 Dec 2019 15:21:18 GMT
RUN Install update 1803-amd64
# Wed, 11 Dec 2019 15:36:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 23:45:17 GMT
ENV MONGO_VERSION=4.2.1
# Wed, 11 Dec 2019 23:45:19 GMT
ENV MONGO_DOWNLOAD_URL=https://downloads.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.1-signed.msi
# Wed, 11 Dec 2019 23:45:20 GMT
ENV MONGO_DOWNLOAD_SHA256=0bd9f5361d21cf358156e8e18aae3f4bc0298e9949b4b988c4b15b52913f91d6
# Thu, 12 Dec 2019 00:03:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 12 Dec 2019 00:03:17 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 12 Dec 2019 00:03:18 GMT
EXPOSE 27017
# Thu, 12 Dec 2019 00:03:20 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:d9e8b01179bfc94a5bdb1810fbd76b999aa52016001ace2d3a4c4bc7065a9601`  
		Last Modified: Tue, 18 Sep 2018 22:43:55 GMT  
		Size: 1.7 GB (1659688273 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d117323cd539488e5ef3bef575a41fa714d83119b0da1896607d96ec2a5e3b52`  
		Size: 696.9 MB (696873564 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:70c803815d644f3772896add8df055dfd33f5934921ca0c57efc290d42454abf`  
		Last Modified: Wed, 11 Dec 2019 18:00:43 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48cbbbce208b5a8e143d43012de06b33cd12dc212fae3e3f6cf28b1acd900861`  
		Last Modified: Thu, 12 Dec 2019 00:09:45 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f72bd77f828256b25eb7375c46fdec577565bc53d89a05fa8a100796450f599`  
		Last Modified: Thu, 12 Dec 2019 00:09:45 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d00e37fa3cf44154da5932563d6cfcff58333ffd56b34c2933a9b14f273b96`  
		Last Modified: Thu, 12 Dec 2019 00:09:42 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e5c13eeee73b3c63164fa7984e8859a050bb173cb69c2b162e7d93845778b5f`  
		Last Modified: Thu, 12 Dec 2019 00:10:40 GMT  
		Size: 453.1 MB (453066744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de21f5bd53ce10a88ff8e77419719b9a2283c1a3f88706ebc56116df5d13e82e`  
		Last Modified: Thu, 12 Dec 2019 00:09:42 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aecef79094cae66ab1003365b8a64bce825e973f8fc6fdaac26462fb31363a15`  
		Last Modified: Thu, 12 Dec 2019 00:09:43 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c1b6171741d09ad84e50e1a007624e0807534f6adc039d848e5915d26bcdfa9`  
		Last Modified: Thu, 12 Dec 2019 00:09:43 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:windowsservercore-1809`

```console
$ docker pull mongo@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:

## `mongo:windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:db78a7411279c77330a0e1cbc4bdf6db701b37e68a3071b4ae0a8186818828f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3384; amd64

### `mongo:windowsservercore-ltsc2016` - windows version 10.0.14393.3384; amd64

```console
$ docker pull mongo@sha256:37ed0ce402c453d82362c8674a95a84ccdc02c9864bfa4fc8170d49d42584a92
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5816058219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fb916a127f9cd60ef9757a818d2c965590bd5303ed4476b1c5a8445ac0b6e2a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 15:47:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2019 23:35:26 GMT
ENV MONGO_VERSION=4.2.1
# Wed, 11 Dec 2019 23:35:27 GMT
ENV MONGO_DOWNLOAD_URL=https://downloads.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.1-signed.msi
# Wed, 11 Dec 2019 23:35:28 GMT
ENV MONGO_DOWNLOAD_SHA256=0bd9f5361d21cf358156e8e18aae3f4bc0298e9949b4b988c4b15b52913f91d6
# Wed, 11 Dec 2019 23:44:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Dec 2019 23:44:48 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Dec 2019 23:44:50 GMT
EXPOSE 27017
# Wed, 11 Dec 2019 23:44:52 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d23dffb4f7b6ebd1cceaac955d664d79467da76c4749d2a37d98556996d8bb0a`  
		Last Modified: Wed, 11 Dec 2019 18:01:38 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c30838129c9ab8ebc7cfc1437e4655ad2fcbf99b7c2a4f618f0dadeb02ee9b1`  
		Last Modified: Thu, 12 Dec 2019 00:08:43 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e12474c86cd0cf6cec9ffc98ee72da8f5c5ef236665b487ed4590f3083cb5d`  
		Last Modified: Thu, 12 Dec 2019 00:08:43 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de05e906a577fa8f95e8df9641ed2d7b042e8ab039218c711f9be88e153f43c4`  
		Last Modified: Thu, 12 Dec 2019 00:08:40 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0735cfc26b92c99aa40bf6c1feb6c344f5d7113c006c50441f5304fe92fd8285`  
		Last Modified: Thu, 12 Dec 2019 00:09:03 GMT  
		Size: 93.3 MB (93345990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77636ccac26ca06e73af52744671d5c6ae3db8960b110a60b0e95ed0231a9619`  
		Last Modified: Thu, 12 Dec 2019 00:08:41 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e83b06286df83053a894432b81bf6c78acc9a1000308697438915c8072f4210`  
		Last Modified: Thu, 12 Dec 2019 00:08:40 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262bd20abcdfdee728fa18bff25d7071edeb206e56c11f9b4a4080018ca2db1f`  
		Last Modified: Thu, 12 Dec 2019 00:08:40 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
