<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mongo`

-	[`mongo:3`](#mongo3)
-	[`mongo:3.6`](#mongo36)
-	[`mongo:3.6.18`](#mongo3618)
-	[`mongo:3.6.18-windowsservercore`](#mongo3618-windowsservercore)
-	[`mongo:3.6.18-windowsservercore-1809`](#mongo3618-windowsservercore-1809)
-	[`mongo:3.6.18-windowsservercore-ltsc2016`](#mongo3618-windowsservercore-ltsc2016)
-	[`mongo:3.6.18-xenial`](#mongo3618-xenial)
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
-	[`mongo:4.0.19`](#mongo4019)
-	[`mongo:4.0.19-windowsservercore`](#mongo4019-windowsservercore)
-	[`mongo:4.0.19-windowsservercore-1809`](#mongo4019-windowsservercore-1809)
-	[`mongo:4.0.19-windowsservercore-ltsc2016`](#mongo4019-windowsservercore-ltsc2016)
-	[`mongo:4.0.19-xenial`](#mongo4019-xenial)
-	[`mongo:4.0-windowsservercore`](#mongo40-windowsservercore)
-	[`mongo:4.0-windowsservercore-1809`](#mongo40-windowsservercore-1809)
-	[`mongo:4.0-windowsservercore-ltsc2016`](#mongo40-windowsservercore-ltsc2016)
-	[`mongo:4.0-xenial`](#mongo40-xenial)
-	[`mongo:4.2`](#mongo42)
-	[`mongo:4.2.8`](#mongo428)
-	[`mongo:4.2.8-bionic`](#mongo428-bionic)
-	[`mongo:4.2.8-windowsservercore`](#mongo428-windowsservercore)
-	[`mongo:4.2.8-windowsservercore-1809`](#mongo428-windowsservercore-1809)
-	[`mongo:4.2.8-windowsservercore-ltsc2016`](#mongo428-windowsservercore-ltsc2016)
-	[`mongo:4.2-bionic`](#mongo42-bionic)
-	[`mongo:4.2-windowsservercore`](#mongo42-windowsservercore)
-	[`mongo:4.2-windowsservercore-1809`](#mongo42-windowsservercore-1809)
-	[`mongo:4.2-windowsservercore-ltsc2016`](#mongo42-windowsservercore-ltsc2016)
-	[`mongo:4.4.0-rc9`](#mongo440-rc9)
-	[`mongo:4.4.0-rc9-bionic`](#mongo440-rc9-bionic)
-	[`mongo:4.4.0-rc9-windowsservercore`](#mongo440-rc9-windowsservercore)
-	[`mongo:4.4.0-rc9-windowsservercore-1809`](#mongo440-rc9-windowsservercore-1809)
-	[`mongo:4.4.0-rc9-windowsservercore-ltsc2016`](#mongo440-rc9-windowsservercore-ltsc2016)
-	[`mongo:4.4-rc`](#mongo44-rc)
-	[`mongo:4.4-rc-bionic`](#mongo44-rc-bionic)
-	[`mongo:4.4-rc-windowsservercore`](#mongo44-rc-windowsservercore)
-	[`mongo:4.4-rc-windowsservercore-1809`](#mongo44-rc-windowsservercore-1809)
-	[`mongo:4.4-rc-windowsservercore-ltsc2016`](#mongo44-rc-windowsservercore-ltsc2016)
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
$ docker pull mongo@sha256:c063422622bb64e5689a795614d9309bc5d31034231008be0e66e02c347a98b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.14393.3750; amd64
	-	windows version 10.0.17763.1282; amd64

### `mongo:3` - linux; amd64

```console
$ docker pull mongo@sha256:5252e05bdca8bed4a4c537b00b15501109c341215eba935cbf969940de5fb3df
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165909480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ed1f113d4af0590a51b16321cc54e0a7cface8f0ee6b14a557b3329342fcfa3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:21:26 GMT
ADD file:52af30f80ba214985a59cb0ef7073c64f8514d58396c0de48f8d7056dec2a58a in / 
# Wed, 17 Jun 2020 01:21:27 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 01:21:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:21:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:21:29 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 05:14:46 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 05:14:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 05:14:55 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 05:14:55 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 05:15:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 05:15:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 05:15:12 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Wed, 17 Jun 2020 05:15:13 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 05:15:13 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 05:15:13 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 05:15:14 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 05:15:14 GMT
ENV MONGO_MAJOR=3.6
# Wed, 17 Jun 2020 05:15:14 GMT
ENV MONGO_VERSION=3.6.18
# Wed, 17 Jun 2020 05:15:15 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 05:15:31 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 05:15:32 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 05:15:32 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 05:15:32 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 05:15:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 05:15:33 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 05:15:33 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:b5e173e44934e01d8d2674bc8b1da00f761c4fe796e0fb2bee1bd1129d2e4ae1`  
		Last Modified: Fri, 15 May 2020 13:20:22 GMT  
		Size: 44.3 MB (44320272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29047100b0407dff554ea80b8005380d62b13a66d7fe2e2adb07b9c091b9f2c0`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 531.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15743a713c2a4033877dab08fb3989280f8c856234227158a4011811c7991372`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6bc9e2987763aa991b7dfd742be04c7b3bb04448982ffe88e58d55c93b76d4`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0742b611831efaa04736014a0196f9d038c2f66141cbae2be6191b487207f2`  
		Last Modified: Wed, 17 Jun 2020 05:17:42 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac88a40bfb757f3fd79fee2a4efdc269db4922c6c3e5bdd058b44b94d4b45a9`  
		Last Modified: Wed, 17 Jun 2020 05:17:42 GMT  
		Size: 2.9 MB (2904013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2a2c44348f93f163d89525024baa1ec80c4ea18b092a08ebb545c348e7d270`  
		Last Modified: Wed, 17 Jun 2020 05:17:42 GMT  
		Size: 1.3 MB (1305044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1c4d1da9278aa467bc18ef66e8714710039f1523ac7fe674d1e5713f162e35`  
		Last Modified: Wed, 17 Jun 2020 05:17:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fa54925dd579adcec5e2abda6b41c1ff268e7ba11a95e74ec09be18bdbc31d9`  
		Last Modified: Wed, 17 Jun 2020 05:17:41 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4b5a734c7f081c2694b37792fc6c36e2a9386f5f1b5d33c57c2b6169abca26`  
		Last Modified: Wed, 17 Jun 2020 05:17:41 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2022710a010f4e1f8a32b253836e9efd416e8dc196bbb3adcf25c30dce90a2f7`  
		Last Modified: Wed, 17 Jun 2020 05:18:00 GMT  
		Size: 117.4 MB (117370162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed0635abd18e3ba799fe897ed8ccb8b9157f10b2a8faf2671a6381703d6eee3`  
		Last Modified: Wed, 17 Jun 2020 05:17:41 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd93e12da51bd497ffebf33e89d26b8827b2608720b88ff32b72cc8174547be`  
		Last Modified: Wed, 17 Jun 2020 05:17:41 GMT  
		Size: 4.0 KB (3953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:a14f1e7d0c8e74bca064fd79a7aa34a432a2f0cf2e61d4d33b352ce1a31e98d0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155250052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae20f80998fd08f33fc5181399f89cd067ac9d35d86b3a6063e6786fad946072`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:44:20 GMT
ADD file:e359a3b06531f763adba716802e252fa49b2e6126f0d3dae1451fc94f5617a13 in / 
# Wed, 17 Jun 2020 01:44:24 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 01:44:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:44:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:44:29 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:22:26 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 03:22:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:22:45 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:22:45 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 03:23:17 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:23:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:23:20 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Wed, 17 Jun 2020 03:23:22 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:23:23 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 03:23:24 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:23:25 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:23:25 GMT
ENV MONGO_MAJOR=3.6
# Wed, 17 Jun 2020 03:23:26 GMT
ENV MONGO_VERSION=3.6.18
# Wed, 17 Jun 2020 03:23:29 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 03:23:53 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 03:24:01 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 03:24:02 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 03:24:05 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:24:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:24:11 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 03:24:20 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:13340090a20bfb81868e7119dc439546fe30dcfccce42509f0fb4d998a1d1fee`  
		Last Modified: Fri, 15 May 2020 16:25:35 GMT  
		Size: 40.0 MB (40003935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75eea8c54eb3d5e45521f4ba5c57ede8436f58690cb8a37da90cfcda5efc25f7`  
		Last Modified: Wed, 17 Jun 2020 01:45:48 GMT  
		Size: 470.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857f69e728f2821d6dce88bd1c73ebda9481628a80b563e677ec423b08fdba87`  
		Last Modified: Wed, 17 Jun 2020 01:45:48 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8b20459bfc0dfbc19d643cff0a457a117336e167bb8051554fb88aee48feff`  
		Last Modified: Wed, 17 Jun 2020 01:45:48 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270afc1f069e440415e7f2ce6ea17182e6af8d92e4c8f67842fc4f54413d3b2e`  
		Last Modified: Wed, 17 Jun 2020 03:30:03 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aca9f74e6ca082c5da190f0f58ac30d4822b0ffd568394e5ffec26bb1fd6a07`  
		Last Modified: Wed, 17 Jun 2020 03:30:02 GMT  
		Size: 2.4 MB (2431869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f567c330a76a757a4b3ad26abdef55c652ebb1e0e70b77b935d3afe42d59a499`  
		Last Modified: Wed, 17 Jun 2020 03:30:03 GMT  
		Size: 1.2 MB (1232045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8e0ba58951fc1e9fa054b24cbd1cdab213c985e279cc76f8bf95465d62c50c`  
		Last Modified: Wed, 17 Jun 2020 03:30:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6273f1d75581a230d9c91081a565493238adf9a52da319953a73a76b5e1151`  
		Last Modified: Wed, 17 Jun 2020 03:30:00 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f3ee35ed8257ac4b1418f6edd3afef970462f931e9b9380a4f575c8c21149f`  
		Last Modified: Wed, 17 Jun 2020 03:30:00 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:273a73ba7a8d6fa9adfa346c96a6a9394e0af69ff18311c8afbca3ea60d5e7c4`  
		Last Modified: Wed, 17 Jun 2020 03:30:27 GMT  
		Size: 111.6 MB (111572207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab45023f72bd29157d7c5781691d982672ab51058905e1ce6a98173ebff45983`  
		Last Modified: Wed, 17 Jun 2020 03:30:00 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71e9c207cf6d3e2bf05e2d8139808a1e142a315d7067547c18467e3e2dc7b14`  
		Last Modified: Wed, 17 Jun 2020 03:30:00 GMT  
		Size: 4.0 KB (3954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3` - windows version 10.0.14393.3750; amd64

```console
$ docker pull mongo@sha256:36a967b2327cfa45e973b881bd4a7934f06ebdd8363c6cf0b69ce7a45a321237
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5827645797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5257e6147460e9d6d88072bf34645b0726d3a4ac5ec84fad7b78b32ba0cd4d4e`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 01 Jun 2020 18:53:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Jun 2020 12:52:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Jun 2020 18:12:21 GMT
ENV MONGO_VERSION=3.6.18
# Wed, 10 Jun 2020 18:12:22 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.18-signed.msi
# Wed, 10 Jun 2020 18:12:23 GMT
ENV MONGO_DOWNLOAD_SHA256=d6a17f96adcda714f523a4b119419b8bf93269542acee70e2b5e899d6d93efdc
# Wed, 10 Jun 2020 18:25:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 10 Jun 2020 18:25:54 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 10 Jun 2020 18:25:56 GMT
EXPOSE 27017
# Wed, 10 Jun 2020 18:25:57 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:375fbabb84945635805b46a02a17ac15a3177bcaae7404cfab5f1ceb0460cb60`  
		Size: 1.7 GB (1664011795 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:30efe9163d37226b077b25cd93b088cebd2ddbaadf173d143b9fe0ddecaeae53`  
		Last Modified: Wed, 10 Jun 2020 15:34:41 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7fc06f25a20433529cc677026660803d286db9e3f8a055137e0fb4adf012f30`  
		Last Modified: Wed, 10 Jun 2020 20:26:03 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba0430b99800ae303becc127d856e491cee47840694a93137ff4b541ec3dd20`  
		Last Modified: Wed, 10 Jun 2020 20:26:02 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df886cb63add8ca65718c352acc3fb8eb0fe36b91664cf0656c582179826898`  
		Last Modified: Wed, 10 Jun 2020 20:26:01 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a205b8dfbf1b2ef64f36fecadd0bdd0a24da03ec7dd0d5c067973d40ea3c899`  
		Last Modified: Wed, 10 Jun 2020 20:26:21 GMT  
		Size: 93.6 MB (93640049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5abb4100f96204b1734a5f4ddffe022067cb3e48d70ed5079fc4a2e012da1185`  
		Last Modified: Wed, 10 Jun 2020 20:25:59 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ecb46291fd9c779f2b145d5c49b5b9e9ff15565e32d19a059a4662e24db90ae`  
		Last Modified: Wed, 10 Jun 2020 20:26:00 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc42606f221bf05aec5c472b015b8eb5e07704d8c498dbca5058adbd2eef885`  
		Last Modified: Wed, 10 Jun 2020 20:26:00 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3` - windows version 10.0.17763.1282; amd64

```console
$ docker pull mongo@sha256:92da2a1d4772d0b93fc197b68d6598b900d911a2084e0c2eda1b6ec816e6c0a2
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2386924383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a90a68509d82192dc4f3cd1515d0842e50b5b7b604bcd15c45aca2a662980f6`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Wed, 10 Jun 2020 12:43:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Jun 2020 18:26:07 GMT
ENV MONGO_VERSION=3.6.18
# Wed, 10 Jun 2020 18:26:08 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.18-signed.msi
# Wed, 10 Jun 2020 18:26:08 GMT
ENV MONGO_DOWNLOAD_SHA256=d6a17f96adcda714f523a4b119419b8bf93269542acee70e2b5e899d6d93efdc
# Wed, 10 Jun 2020 18:40:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 10 Jun 2020 18:40:02 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 10 Jun 2020 18:40:03 GMT
EXPOSE 27017
# Wed, 10 Jun 2020 18:40:04 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b11029314f3c794dc51e43c915b3e62f6b44aeb96f84b8b92f453e61cf7a2cb3`  
		Last Modified: Wed, 10 Jun 2020 15:34:12 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:637403b20232ba07d564c2a0530b1f5b8513e13afeae1720fa945dca7a4345ce`  
		Last Modified: Wed, 10 Jun 2020 20:26:38 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734ddb1043b8b11997a958386f728fdd820942a38c9d43e325e22d43e7a1c209`  
		Last Modified: Wed, 10 Jun 2020 20:26:38 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ae9516d42c6b1c8190c4da03bc21fd92905429da8fe9c022512026413d0865`  
		Last Modified: Wed, 10 Jun 2020 20:26:35 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13a450568155c9a15f52f40f17ae307bb34726b6eb47ff8c1fa2a16b6a4f040`  
		Last Modified: Wed, 10 Jun 2020 20:26:57 GMT  
		Size: 93.0 MB (93002199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0bb5eaf61d4fa06f97b072f70d10cf84b1ba68111389e690c2d6c39bc26ddc5`  
		Last Modified: Wed, 10 Jun 2020 20:26:35 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd32776d415229410f3e7acd3749e28a532e0f5f03553a9d93021571253e3934`  
		Last Modified: Wed, 10 Jun 2020 20:26:35 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6333cf051585d01194811d9da3d43c32f4b55307ce87de32482f391f6158037b`  
		Last Modified: Wed, 10 Jun 2020 20:26:35 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.6`

```console
$ docker pull mongo@sha256:c063422622bb64e5689a795614d9309bc5d31034231008be0e66e02c347a98b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.14393.3750; amd64
	-	windows version 10.0.17763.1282; amd64

### `mongo:3.6` - linux; amd64

```console
$ docker pull mongo@sha256:5252e05bdca8bed4a4c537b00b15501109c341215eba935cbf969940de5fb3df
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165909480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ed1f113d4af0590a51b16321cc54e0a7cface8f0ee6b14a557b3329342fcfa3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:21:26 GMT
ADD file:52af30f80ba214985a59cb0ef7073c64f8514d58396c0de48f8d7056dec2a58a in / 
# Wed, 17 Jun 2020 01:21:27 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 01:21:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:21:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:21:29 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 05:14:46 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 05:14:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 05:14:55 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 05:14:55 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 05:15:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 05:15:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 05:15:12 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Wed, 17 Jun 2020 05:15:13 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 05:15:13 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 05:15:13 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 05:15:14 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 05:15:14 GMT
ENV MONGO_MAJOR=3.6
# Wed, 17 Jun 2020 05:15:14 GMT
ENV MONGO_VERSION=3.6.18
# Wed, 17 Jun 2020 05:15:15 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 05:15:31 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 05:15:32 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 05:15:32 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 05:15:32 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 05:15:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 05:15:33 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 05:15:33 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:b5e173e44934e01d8d2674bc8b1da00f761c4fe796e0fb2bee1bd1129d2e4ae1`  
		Last Modified: Fri, 15 May 2020 13:20:22 GMT  
		Size: 44.3 MB (44320272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29047100b0407dff554ea80b8005380d62b13a66d7fe2e2adb07b9c091b9f2c0`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 531.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15743a713c2a4033877dab08fb3989280f8c856234227158a4011811c7991372`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6bc9e2987763aa991b7dfd742be04c7b3bb04448982ffe88e58d55c93b76d4`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0742b611831efaa04736014a0196f9d038c2f66141cbae2be6191b487207f2`  
		Last Modified: Wed, 17 Jun 2020 05:17:42 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac88a40bfb757f3fd79fee2a4efdc269db4922c6c3e5bdd058b44b94d4b45a9`  
		Last Modified: Wed, 17 Jun 2020 05:17:42 GMT  
		Size: 2.9 MB (2904013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2a2c44348f93f163d89525024baa1ec80c4ea18b092a08ebb545c348e7d270`  
		Last Modified: Wed, 17 Jun 2020 05:17:42 GMT  
		Size: 1.3 MB (1305044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1c4d1da9278aa467bc18ef66e8714710039f1523ac7fe674d1e5713f162e35`  
		Last Modified: Wed, 17 Jun 2020 05:17:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fa54925dd579adcec5e2abda6b41c1ff268e7ba11a95e74ec09be18bdbc31d9`  
		Last Modified: Wed, 17 Jun 2020 05:17:41 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4b5a734c7f081c2694b37792fc6c36e2a9386f5f1b5d33c57c2b6169abca26`  
		Last Modified: Wed, 17 Jun 2020 05:17:41 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2022710a010f4e1f8a32b253836e9efd416e8dc196bbb3adcf25c30dce90a2f7`  
		Last Modified: Wed, 17 Jun 2020 05:18:00 GMT  
		Size: 117.4 MB (117370162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed0635abd18e3ba799fe897ed8ccb8b9157f10b2a8faf2671a6381703d6eee3`  
		Last Modified: Wed, 17 Jun 2020 05:17:41 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd93e12da51bd497ffebf33e89d26b8827b2608720b88ff32b72cc8174547be`  
		Last Modified: Wed, 17 Jun 2020 05:17:41 GMT  
		Size: 4.0 KB (3953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3.6` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:a14f1e7d0c8e74bca064fd79a7aa34a432a2f0cf2e61d4d33b352ce1a31e98d0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155250052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae20f80998fd08f33fc5181399f89cd067ac9d35d86b3a6063e6786fad946072`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:44:20 GMT
ADD file:e359a3b06531f763adba716802e252fa49b2e6126f0d3dae1451fc94f5617a13 in / 
# Wed, 17 Jun 2020 01:44:24 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 01:44:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:44:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:44:29 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:22:26 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 03:22:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:22:45 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:22:45 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 03:23:17 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:23:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:23:20 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Wed, 17 Jun 2020 03:23:22 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:23:23 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 03:23:24 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:23:25 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:23:25 GMT
ENV MONGO_MAJOR=3.6
# Wed, 17 Jun 2020 03:23:26 GMT
ENV MONGO_VERSION=3.6.18
# Wed, 17 Jun 2020 03:23:29 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 03:23:53 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 03:24:01 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 03:24:02 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 03:24:05 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:24:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:24:11 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 03:24:20 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:13340090a20bfb81868e7119dc439546fe30dcfccce42509f0fb4d998a1d1fee`  
		Last Modified: Fri, 15 May 2020 16:25:35 GMT  
		Size: 40.0 MB (40003935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75eea8c54eb3d5e45521f4ba5c57ede8436f58690cb8a37da90cfcda5efc25f7`  
		Last Modified: Wed, 17 Jun 2020 01:45:48 GMT  
		Size: 470.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857f69e728f2821d6dce88bd1c73ebda9481628a80b563e677ec423b08fdba87`  
		Last Modified: Wed, 17 Jun 2020 01:45:48 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8b20459bfc0dfbc19d643cff0a457a117336e167bb8051554fb88aee48feff`  
		Last Modified: Wed, 17 Jun 2020 01:45:48 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270afc1f069e440415e7f2ce6ea17182e6af8d92e4c8f67842fc4f54413d3b2e`  
		Last Modified: Wed, 17 Jun 2020 03:30:03 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aca9f74e6ca082c5da190f0f58ac30d4822b0ffd568394e5ffec26bb1fd6a07`  
		Last Modified: Wed, 17 Jun 2020 03:30:02 GMT  
		Size: 2.4 MB (2431869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f567c330a76a757a4b3ad26abdef55c652ebb1e0e70b77b935d3afe42d59a499`  
		Last Modified: Wed, 17 Jun 2020 03:30:03 GMT  
		Size: 1.2 MB (1232045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8e0ba58951fc1e9fa054b24cbd1cdab213c985e279cc76f8bf95465d62c50c`  
		Last Modified: Wed, 17 Jun 2020 03:30:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6273f1d75581a230d9c91081a565493238adf9a52da319953a73a76b5e1151`  
		Last Modified: Wed, 17 Jun 2020 03:30:00 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f3ee35ed8257ac4b1418f6edd3afef970462f931e9b9380a4f575c8c21149f`  
		Last Modified: Wed, 17 Jun 2020 03:30:00 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:273a73ba7a8d6fa9adfa346c96a6a9394e0af69ff18311c8afbca3ea60d5e7c4`  
		Last Modified: Wed, 17 Jun 2020 03:30:27 GMT  
		Size: 111.6 MB (111572207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab45023f72bd29157d7c5781691d982672ab51058905e1ce6a98173ebff45983`  
		Last Modified: Wed, 17 Jun 2020 03:30:00 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71e9c207cf6d3e2bf05e2d8139808a1e142a315d7067547c18467e3e2dc7b14`  
		Last Modified: Wed, 17 Jun 2020 03:30:00 GMT  
		Size: 4.0 KB (3954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3.6` - windows version 10.0.14393.3750; amd64

```console
$ docker pull mongo@sha256:36a967b2327cfa45e973b881bd4a7934f06ebdd8363c6cf0b69ce7a45a321237
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5827645797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5257e6147460e9d6d88072bf34645b0726d3a4ac5ec84fad7b78b32ba0cd4d4e`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 01 Jun 2020 18:53:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Jun 2020 12:52:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Jun 2020 18:12:21 GMT
ENV MONGO_VERSION=3.6.18
# Wed, 10 Jun 2020 18:12:22 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.18-signed.msi
# Wed, 10 Jun 2020 18:12:23 GMT
ENV MONGO_DOWNLOAD_SHA256=d6a17f96adcda714f523a4b119419b8bf93269542acee70e2b5e899d6d93efdc
# Wed, 10 Jun 2020 18:25:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 10 Jun 2020 18:25:54 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 10 Jun 2020 18:25:56 GMT
EXPOSE 27017
# Wed, 10 Jun 2020 18:25:57 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:375fbabb84945635805b46a02a17ac15a3177bcaae7404cfab5f1ceb0460cb60`  
		Size: 1.7 GB (1664011795 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:30efe9163d37226b077b25cd93b088cebd2ddbaadf173d143b9fe0ddecaeae53`  
		Last Modified: Wed, 10 Jun 2020 15:34:41 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7fc06f25a20433529cc677026660803d286db9e3f8a055137e0fb4adf012f30`  
		Last Modified: Wed, 10 Jun 2020 20:26:03 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba0430b99800ae303becc127d856e491cee47840694a93137ff4b541ec3dd20`  
		Last Modified: Wed, 10 Jun 2020 20:26:02 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df886cb63add8ca65718c352acc3fb8eb0fe36b91664cf0656c582179826898`  
		Last Modified: Wed, 10 Jun 2020 20:26:01 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a205b8dfbf1b2ef64f36fecadd0bdd0a24da03ec7dd0d5c067973d40ea3c899`  
		Last Modified: Wed, 10 Jun 2020 20:26:21 GMT  
		Size: 93.6 MB (93640049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5abb4100f96204b1734a5f4ddffe022067cb3e48d70ed5079fc4a2e012da1185`  
		Last Modified: Wed, 10 Jun 2020 20:25:59 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ecb46291fd9c779f2b145d5c49b5b9e9ff15565e32d19a059a4662e24db90ae`  
		Last Modified: Wed, 10 Jun 2020 20:26:00 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc42606f221bf05aec5c472b015b8eb5e07704d8c498dbca5058adbd2eef885`  
		Last Modified: Wed, 10 Jun 2020 20:26:00 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3.6` - windows version 10.0.17763.1282; amd64

```console
$ docker pull mongo@sha256:92da2a1d4772d0b93fc197b68d6598b900d911a2084e0c2eda1b6ec816e6c0a2
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2386924383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a90a68509d82192dc4f3cd1515d0842e50b5b7b604bcd15c45aca2a662980f6`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Wed, 10 Jun 2020 12:43:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Jun 2020 18:26:07 GMT
ENV MONGO_VERSION=3.6.18
# Wed, 10 Jun 2020 18:26:08 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.18-signed.msi
# Wed, 10 Jun 2020 18:26:08 GMT
ENV MONGO_DOWNLOAD_SHA256=d6a17f96adcda714f523a4b119419b8bf93269542acee70e2b5e899d6d93efdc
# Wed, 10 Jun 2020 18:40:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 10 Jun 2020 18:40:02 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 10 Jun 2020 18:40:03 GMT
EXPOSE 27017
# Wed, 10 Jun 2020 18:40:04 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b11029314f3c794dc51e43c915b3e62f6b44aeb96f84b8b92f453e61cf7a2cb3`  
		Last Modified: Wed, 10 Jun 2020 15:34:12 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:637403b20232ba07d564c2a0530b1f5b8513e13afeae1720fa945dca7a4345ce`  
		Last Modified: Wed, 10 Jun 2020 20:26:38 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734ddb1043b8b11997a958386f728fdd820942a38c9d43e325e22d43e7a1c209`  
		Last Modified: Wed, 10 Jun 2020 20:26:38 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ae9516d42c6b1c8190c4da03bc21fd92905429da8fe9c022512026413d0865`  
		Last Modified: Wed, 10 Jun 2020 20:26:35 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13a450568155c9a15f52f40f17ae307bb34726b6eb47ff8c1fa2a16b6a4f040`  
		Last Modified: Wed, 10 Jun 2020 20:26:57 GMT  
		Size: 93.0 MB (93002199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0bb5eaf61d4fa06f97b072f70d10cf84b1ba68111389e690c2d6c39bc26ddc5`  
		Last Modified: Wed, 10 Jun 2020 20:26:35 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd32776d415229410f3e7acd3749e28a532e0f5f03553a9d93021571253e3934`  
		Last Modified: Wed, 10 Jun 2020 20:26:35 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6333cf051585d01194811d9da3d43c32f4b55307ce87de32482f391f6158037b`  
		Last Modified: Wed, 10 Jun 2020 20:26:35 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.6.18`

```console
$ docker pull mongo@sha256:c063422622bb64e5689a795614d9309bc5d31034231008be0e66e02c347a98b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.14393.3750; amd64
	-	windows version 10.0.17763.1282; amd64

### `mongo:3.6.18` - linux; amd64

```console
$ docker pull mongo@sha256:5252e05bdca8bed4a4c537b00b15501109c341215eba935cbf969940de5fb3df
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165909480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ed1f113d4af0590a51b16321cc54e0a7cface8f0ee6b14a557b3329342fcfa3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:21:26 GMT
ADD file:52af30f80ba214985a59cb0ef7073c64f8514d58396c0de48f8d7056dec2a58a in / 
# Wed, 17 Jun 2020 01:21:27 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 01:21:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:21:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:21:29 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 05:14:46 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 05:14:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 05:14:55 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 05:14:55 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 05:15:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 05:15:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 05:15:12 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Wed, 17 Jun 2020 05:15:13 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 05:15:13 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 05:15:13 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 05:15:14 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 05:15:14 GMT
ENV MONGO_MAJOR=3.6
# Wed, 17 Jun 2020 05:15:14 GMT
ENV MONGO_VERSION=3.6.18
# Wed, 17 Jun 2020 05:15:15 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 05:15:31 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 05:15:32 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 05:15:32 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 05:15:32 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 05:15:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 05:15:33 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 05:15:33 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:b5e173e44934e01d8d2674bc8b1da00f761c4fe796e0fb2bee1bd1129d2e4ae1`  
		Last Modified: Fri, 15 May 2020 13:20:22 GMT  
		Size: 44.3 MB (44320272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29047100b0407dff554ea80b8005380d62b13a66d7fe2e2adb07b9c091b9f2c0`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 531.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15743a713c2a4033877dab08fb3989280f8c856234227158a4011811c7991372`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6bc9e2987763aa991b7dfd742be04c7b3bb04448982ffe88e58d55c93b76d4`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0742b611831efaa04736014a0196f9d038c2f66141cbae2be6191b487207f2`  
		Last Modified: Wed, 17 Jun 2020 05:17:42 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac88a40bfb757f3fd79fee2a4efdc269db4922c6c3e5bdd058b44b94d4b45a9`  
		Last Modified: Wed, 17 Jun 2020 05:17:42 GMT  
		Size: 2.9 MB (2904013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2a2c44348f93f163d89525024baa1ec80c4ea18b092a08ebb545c348e7d270`  
		Last Modified: Wed, 17 Jun 2020 05:17:42 GMT  
		Size: 1.3 MB (1305044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1c4d1da9278aa467bc18ef66e8714710039f1523ac7fe674d1e5713f162e35`  
		Last Modified: Wed, 17 Jun 2020 05:17:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fa54925dd579adcec5e2abda6b41c1ff268e7ba11a95e74ec09be18bdbc31d9`  
		Last Modified: Wed, 17 Jun 2020 05:17:41 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4b5a734c7f081c2694b37792fc6c36e2a9386f5f1b5d33c57c2b6169abca26`  
		Last Modified: Wed, 17 Jun 2020 05:17:41 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2022710a010f4e1f8a32b253836e9efd416e8dc196bbb3adcf25c30dce90a2f7`  
		Last Modified: Wed, 17 Jun 2020 05:18:00 GMT  
		Size: 117.4 MB (117370162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed0635abd18e3ba799fe897ed8ccb8b9157f10b2a8faf2671a6381703d6eee3`  
		Last Modified: Wed, 17 Jun 2020 05:17:41 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd93e12da51bd497ffebf33e89d26b8827b2608720b88ff32b72cc8174547be`  
		Last Modified: Wed, 17 Jun 2020 05:17:41 GMT  
		Size: 4.0 KB (3953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3.6.18` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:a14f1e7d0c8e74bca064fd79a7aa34a432a2f0cf2e61d4d33b352ce1a31e98d0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155250052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae20f80998fd08f33fc5181399f89cd067ac9d35d86b3a6063e6786fad946072`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:44:20 GMT
ADD file:e359a3b06531f763adba716802e252fa49b2e6126f0d3dae1451fc94f5617a13 in / 
# Wed, 17 Jun 2020 01:44:24 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 01:44:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:44:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:44:29 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:22:26 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 03:22:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:22:45 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:22:45 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 03:23:17 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:23:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:23:20 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Wed, 17 Jun 2020 03:23:22 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:23:23 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 03:23:24 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:23:25 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:23:25 GMT
ENV MONGO_MAJOR=3.6
# Wed, 17 Jun 2020 03:23:26 GMT
ENV MONGO_VERSION=3.6.18
# Wed, 17 Jun 2020 03:23:29 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 03:23:53 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 03:24:01 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 03:24:02 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 03:24:05 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:24:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:24:11 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 03:24:20 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:13340090a20bfb81868e7119dc439546fe30dcfccce42509f0fb4d998a1d1fee`  
		Last Modified: Fri, 15 May 2020 16:25:35 GMT  
		Size: 40.0 MB (40003935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75eea8c54eb3d5e45521f4ba5c57ede8436f58690cb8a37da90cfcda5efc25f7`  
		Last Modified: Wed, 17 Jun 2020 01:45:48 GMT  
		Size: 470.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857f69e728f2821d6dce88bd1c73ebda9481628a80b563e677ec423b08fdba87`  
		Last Modified: Wed, 17 Jun 2020 01:45:48 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8b20459bfc0dfbc19d643cff0a457a117336e167bb8051554fb88aee48feff`  
		Last Modified: Wed, 17 Jun 2020 01:45:48 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270afc1f069e440415e7f2ce6ea17182e6af8d92e4c8f67842fc4f54413d3b2e`  
		Last Modified: Wed, 17 Jun 2020 03:30:03 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aca9f74e6ca082c5da190f0f58ac30d4822b0ffd568394e5ffec26bb1fd6a07`  
		Last Modified: Wed, 17 Jun 2020 03:30:02 GMT  
		Size: 2.4 MB (2431869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f567c330a76a757a4b3ad26abdef55c652ebb1e0e70b77b935d3afe42d59a499`  
		Last Modified: Wed, 17 Jun 2020 03:30:03 GMT  
		Size: 1.2 MB (1232045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8e0ba58951fc1e9fa054b24cbd1cdab213c985e279cc76f8bf95465d62c50c`  
		Last Modified: Wed, 17 Jun 2020 03:30:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6273f1d75581a230d9c91081a565493238adf9a52da319953a73a76b5e1151`  
		Last Modified: Wed, 17 Jun 2020 03:30:00 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f3ee35ed8257ac4b1418f6edd3afef970462f931e9b9380a4f575c8c21149f`  
		Last Modified: Wed, 17 Jun 2020 03:30:00 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:273a73ba7a8d6fa9adfa346c96a6a9394e0af69ff18311c8afbca3ea60d5e7c4`  
		Last Modified: Wed, 17 Jun 2020 03:30:27 GMT  
		Size: 111.6 MB (111572207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab45023f72bd29157d7c5781691d982672ab51058905e1ce6a98173ebff45983`  
		Last Modified: Wed, 17 Jun 2020 03:30:00 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71e9c207cf6d3e2bf05e2d8139808a1e142a315d7067547c18467e3e2dc7b14`  
		Last Modified: Wed, 17 Jun 2020 03:30:00 GMT  
		Size: 4.0 KB (3954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3.6.18` - windows version 10.0.14393.3750; amd64

```console
$ docker pull mongo@sha256:36a967b2327cfa45e973b881bd4a7934f06ebdd8363c6cf0b69ce7a45a321237
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5827645797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5257e6147460e9d6d88072bf34645b0726d3a4ac5ec84fad7b78b32ba0cd4d4e`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 01 Jun 2020 18:53:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Jun 2020 12:52:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Jun 2020 18:12:21 GMT
ENV MONGO_VERSION=3.6.18
# Wed, 10 Jun 2020 18:12:22 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.18-signed.msi
# Wed, 10 Jun 2020 18:12:23 GMT
ENV MONGO_DOWNLOAD_SHA256=d6a17f96adcda714f523a4b119419b8bf93269542acee70e2b5e899d6d93efdc
# Wed, 10 Jun 2020 18:25:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 10 Jun 2020 18:25:54 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 10 Jun 2020 18:25:56 GMT
EXPOSE 27017
# Wed, 10 Jun 2020 18:25:57 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:375fbabb84945635805b46a02a17ac15a3177bcaae7404cfab5f1ceb0460cb60`  
		Size: 1.7 GB (1664011795 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:30efe9163d37226b077b25cd93b088cebd2ddbaadf173d143b9fe0ddecaeae53`  
		Last Modified: Wed, 10 Jun 2020 15:34:41 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7fc06f25a20433529cc677026660803d286db9e3f8a055137e0fb4adf012f30`  
		Last Modified: Wed, 10 Jun 2020 20:26:03 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba0430b99800ae303becc127d856e491cee47840694a93137ff4b541ec3dd20`  
		Last Modified: Wed, 10 Jun 2020 20:26:02 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df886cb63add8ca65718c352acc3fb8eb0fe36b91664cf0656c582179826898`  
		Last Modified: Wed, 10 Jun 2020 20:26:01 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a205b8dfbf1b2ef64f36fecadd0bdd0a24da03ec7dd0d5c067973d40ea3c899`  
		Last Modified: Wed, 10 Jun 2020 20:26:21 GMT  
		Size: 93.6 MB (93640049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5abb4100f96204b1734a5f4ddffe022067cb3e48d70ed5079fc4a2e012da1185`  
		Last Modified: Wed, 10 Jun 2020 20:25:59 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ecb46291fd9c779f2b145d5c49b5b9e9ff15565e32d19a059a4662e24db90ae`  
		Last Modified: Wed, 10 Jun 2020 20:26:00 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc42606f221bf05aec5c472b015b8eb5e07704d8c498dbca5058adbd2eef885`  
		Last Modified: Wed, 10 Jun 2020 20:26:00 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3.6.18` - windows version 10.0.17763.1282; amd64

```console
$ docker pull mongo@sha256:92da2a1d4772d0b93fc197b68d6598b900d911a2084e0c2eda1b6ec816e6c0a2
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2386924383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a90a68509d82192dc4f3cd1515d0842e50b5b7b604bcd15c45aca2a662980f6`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Wed, 10 Jun 2020 12:43:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Jun 2020 18:26:07 GMT
ENV MONGO_VERSION=3.6.18
# Wed, 10 Jun 2020 18:26:08 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.18-signed.msi
# Wed, 10 Jun 2020 18:26:08 GMT
ENV MONGO_DOWNLOAD_SHA256=d6a17f96adcda714f523a4b119419b8bf93269542acee70e2b5e899d6d93efdc
# Wed, 10 Jun 2020 18:40:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 10 Jun 2020 18:40:02 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 10 Jun 2020 18:40:03 GMT
EXPOSE 27017
# Wed, 10 Jun 2020 18:40:04 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b11029314f3c794dc51e43c915b3e62f6b44aeb96f84b8b92f453e61cf7a2cb3`  
		Last Modified: Wed, 10 Jun 2020 15:34:12 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:637403b20232ba07d564c2a0530b1f5b8513e13afeae1720fa945dca7a4345ce`  
		Last Modified: Wed, 10 Jun 2020 20:26:38 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734ddb1043b8b11997a958386f728fdd820942a38c9d43e325e22d43e7a1c209`  
		Last Modified: Wed, 10 Jun 2020 20:26:38 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ae9516d42c6b1c8190c4da03bc21fd92905429da8fe9c022512026413d0865`  
		Last Modified: Wed, 10 Jun 2020 20:26:35 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13a450568155c9a15f52f40f17ae307bb34726b6eb47ff8c1fa2a16b6a4f040`  
		Last Modified: Wed, 10 Jun 2020 20:26:57 GMT  
		Size: 93.0 MB (93002199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0bb5eaf61d4fa06f97b072f70d10cf84b1ba68111389e690c2d6c39bc26ddc5`  
		Last Modified: Wed, 10 Jun 2020 20:26:35 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd32776d415229410f3e7acd3749e28a532e0f5f03553a9d93021571253e3934`  
		Last Modified: Wed, 10 Jun 2020 20:26:35 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6333cf051585d01194811d9da3d43c32f4b55307ce87de32482f391f6158037b`  
		Last Modified: Wed, 10 Jun 2020 20:26:35 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.6.18-windowsservercore`

```console
$ docker pull mongo@sha256:bbdbeee49f3b69d6ecb3874572ad67e790cd49ac36c8f98533e9b99b922c74f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3750; amd64
	-	windows version 10.0.17763.1282; amd64

### `mongo:3.6.18-windowsservercore` - windows version 10.0.14393.3750; amd64

```console
$ docker pull mongo@sha256:36a967b2327cfa45e973b881bd4a7934f06ebdd8363c6cf0b69ce7a45a321237
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5827645797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5257e6147460e9d6d88072bf34645b0726d3a4ac5ec84fad7b78b32ba0cd4d4e`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 01 Jun 2020 18:53:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Jun 2020 12:52:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Jun 2020 18:12:21 GMT
ENV MONGO_VERSION=3.6.18
# Wed, 10 Jun 2020 18:12:22 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.18-signed.msi
# Wed, 10 Jun 2020 18:12:23 GMT
ENV MONGO_DOWNLOAD_SHA256=d6a17f96adcda714f523a4b119419b8bf93269542acee70e2b5e899d6d93efdc
# Wed, 10 Jun 2020 18:25:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 10 Jun 2020 18:25:54 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 10 Jun 2020 18:25:56 GMT
EXPOSE 27017
# Wed, 10 Jun 2020 18:25:57 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:375fbabb84945635805b46a02a17ac15a3177bcaae7404cfab5f1ceb0460cb60`  
		Size: 1.7 GB (1664011795 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:30efe9163d37226b077b25cd93b088cebd2ddbaadf173d143b9fe0ddecaeae53`  
		Last Modified: Wed, 10 Jun 2020 15:34:41 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7fc06f25a20433529cc677026660803d286db9e3f8a055137e0fb4adf012f30`  
		Last Modified: Wed, 10 Jun 2020 20:26:03 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba0430b99800ae303becc127d856e491cee47840694a93137ff4b541ec3dd20`  
		Last Modified: Wed, 10 Jun 2020 20:26:02 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df886cb63add8ca65718c352acc3fb8eb0fe36b91664cf0656c582179826898`  
		Last Modified: Wed, 10 Jun 2020 20:26:01 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a205b8dfbf1b2ef64f36fecadd0bdd0a24da03ec7dd0d5c067973d40ea3c899`  
		Last Modified: Wed, 10 Jun 2020 20:26:21 GMT  
		Size: 93.6 MB (93640049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5abb4100f96204b1734a5f4ddffe022067cb3e48d70ed5079fc4a2e012da1185`  
		Last Modified: Wed, 10 Jun 2020 20:25:59 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ecb46291fd9c779f2b145d5c49b5b9e9ff15565e32d19a059a4662e24db90ae`  
		Last Modified: Wed, 10 Jun 2020 20:26:00 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc42606f221bf05aec5c472b015b8eb5e07704d8c498dbca5058adbd2eef885`  
		Last Modified: Wed, 10 Jun 2020 20:26:00 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3.6.18-windowsservercore` - windows version 10.0.17763.1282; amd64

```console
$ docker pull mongo@sha256:92da2a1d4772d0b93fc197b68d6598b900d911a2084e0c2eda1b6ec816e6c0a2
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2386924383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a90a68509d82192dc4f3cd1515d0842e50b5b7b604bcd15c45aca2a662980f6`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Wed, 10 Jun 2020 12:43:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Jun 2020 18:26:07 GMT
ENV MONGO_VERSION=3.6.18
# Wed, 10 Jun 2020 18:26:08 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.18-signed.msi
# Wed, 10 Jun 2020 18:26:08 GMT
ENV MONGO_DOWNLOAD_SHA256=d6a17f96adcda714f523a4b119419b8bf93269542acee70e2b5e899d6d93efdc
# Wed, 10 Jun 2020 18:40:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 10 Jun 2020 18:40:02 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 10 Jun 2020 18:40:03 GMT
EXPOSE 27017
# Wed, 10 Jun 2020 18:40:04 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b11029314f3c794dc51e43c915b3e62f6b44aeb96f84b8b92f453e61cf7a2cb3`  
		Last Modified: Wed, 10 Jun 2020 15:34:12 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:637403b20232ba07d564c2a0530b1f5b8513e13afeae1720fa945dca7a4345ce`  
		Last Modified: Wed, 10 Jun 2020 20:26:38 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734ddb1043b8b11997a958386f728fdd820942a38c9d43e325e22d43e7a1c209`  
		Last Modified: Wed, 10 Jun 2020 20:26:38 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ae9516d42c6b1c8190c4da03bc21fd92905429da8fe9c022512026413d0865`  
		Last Modified: Wed, 10 Jun 2020 20:26:35 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13a450568155c9a15f52f40f17ae307bb34726b6eb47ff8c1fa2a16b6a4f040`  
		Last Modified: Wed, 10 Jun 2020 20:26:57 GMT  
		Size: 93.0 MB (93002199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0bb5eaf61d4fa06f97b072f70d10cf84b1ba68111389e690c2d6c39bc26ddc5`  
		Last Modified: Wed, 10 Jun 2020 20:26:35 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd32776d415229410f3e7acd3749e28a532e0f5f03553a9d93021571253e3934`  
		Last Modified: Wed, 10 Jun 2020 20:26:35 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6333cf051585d01194811d9da3d43c32f4b55307ce87de32482f391f6158037b`  
		Last Modified: Wed, 10 Jun 2020 20:26:35 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.6.18-windowsservercore-1809`

```console
$ docker pull mongo@sha256:168f93ffc37589489ff16a458b124925235e7342353261bbac8aaacf84e9cff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1282; amd64

### `mongo:3.6.18-windowsservercore-1809` - windows version 10.0.17763.1282; amd64

```console
$ docker pull mongo@sha256:92da2a1d4772d0b93fc197b68d6598b900d911a2084e0c2eda1b6ec816e6c0a2
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2386924383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a90a68509d82192dc4f3cd1515d0842e50b5b7b604bcd15c45aca2a662980f6`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Wed, 10 Jun 2020 12:43:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Jun 2020 18:26:07 GMT
ENV MONGO_VERSION=3.6.18
# Wed, 10 Jun 2020 18:26:08 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.18-signed.msi
# Wed, 10 Jun 2020 18:26:08 GMT
ENV MONGO_DOWNLOAD_SHA256=d6a17f96adcda714f523a4b119419b8bf93269542acee70e2b5e899d6d93efdc
# Wed, 10 Jun 2020 18:40:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 10 Jun 2020 18:40:02 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 10 Jun 2020 18:40:03 GMT
EXPOSE 27017
# Wed, 10 Jun 2020 18:40:04 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b11029314f3c794dc51e43c915b3e62f6b44aeb96f84b8b92f453e61cf7a2cb3`  
		Last Modified: Wed, 10 Jun 2020 15:34:12 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:637403b20232ba07d564c2a0530b1f5b8513e13afeae1720fa945dca7a4345ce`  
		Last Modified: Wed, 10 Jun 2020 20:26:38 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734ddb1043b8b11997a958386f728fdd820942a38c9d43e325e22d43e7a1c209`  
		Last Modified: Wed, 10 Jun 2020 20:26:38 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ae9516d42c6b1c8190c4da03bc21fd92905429da8fe9c022512026413d0865`  
		Last Modified: Wed, 10 Jun 2020 20:26:35 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13a450568155c9a15f52f40f17ae307bb34726b6eb47ff8c1fa2a16b6a4f040`  
		Last Modified: Wed, 10 Jun 2020 20:26:57 GMT  
		Size: 93.0 MB (93002199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0bb5eaf61d4fa06f97b072f70d10cf84b1ba68111389e690c2d6c39bc26ddc5`  
		Last Modified: Wed, 10 Jun 2020 20:26:35 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd32776d415229410f3e7acd3749e28a532e0f5f03553a9d93021571253e3934`  
		Last Modified: Wed, 10 Jun 2020 20:26:35 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6333cf051585d01194811d9da3d43c32f4b55307ce87de32482f391f6158037b`  
		Last Modified: Wed, 10 Jun 2020 20:26:35 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.6.18-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:52630676efc96befa6e39413412ef130f145cdf478f6e886a6e8cc088ef1deb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3750; amd64

### `mongo:3.6.18-windowsservercore-ltsc2016` - windows version 10.0.14393.3750; amd64

```console
$ docker pull mongo@sha256:36a967b2327cfa45e973b881bd4a7934f06ebdd8363c6cf0b69ce7a45a321237
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5827645797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5257e6147460e9d6d88072bf34645b0726d3a4ac5ec84fad7b78b32ba0cd4d4e`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 01 Jun 2020 18:53:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Jun 2020 12:52:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Jun 2020 18:12:21 GMT
ENV MONGO_VERSION=3.6.18
# Wed, 10 Jun 2020 18:12:22 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.18-signed.msi
# Wed, 10 Jun 2020 18:12:23 GMT
ENV MONGO_DOWNLOAD_SHA256=d6a17f96adcda714f523a4b119419b8bf93269542acee70e2b5e899d6d93efdc
# Wed, 10 Jun 2020 18:25:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 10 Jun 2020 18:25:54 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 10 Jun 2020 18:25:56 GMT
EXPOSE 27017
# Wed, 10 Jun 2020 18:25:57 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:375fbabb84945635805b46a02a17ac15a3177bcaae7404cfab5f1ceb0460cb60`  
		Size: 1.7 GB (1664011795 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:30efe9163d37226b077b25cd93b088cebd2ddbaadf173d143b9fe0ddecaeae53`  
		Last Modified: Wed, 10 Jun 2020 15:34:41 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7fc06f25a20433529cc677026660803d286db9e3f8a055137e0fb4adf012f30`  
		Last Modified: Wed, 10 Jun 2020 20:26:03 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba0430b99800ae303becc127d856e491cee47840694a93137ff4b541ec3dd20`  
		Last Modified: Wed, 10 Jun 2020 20:26:02 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df886cb63add8ca65718c352acc3fb8eb0fe36b91664cf0656c582179826898`  
		Last Modified: Wed, 10 Jun 2020 20:26:01 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a205b8dfbf1b2ef64f36fecadd0bdd0a24da03ec7dd0d5c067973d40ea3c899`  
		Last Modified: Wed, 10 Jun 2020 20:26:21 GMT  
		Size: 93.6 MB (93640049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5abb4100f96204b1734a5f4ddffe022067cb3e48d70ed5079fc4a2e012da1185`  
		Last Modified: Wed, 10 Jun 2020 20:25:59 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ecb46291fd9c779f2b145d5c49b5b9e9ff15565e32d19a059a4662e24db90ae`  
		Last Modified: Wed, 10 Jun 2020 20:26:00 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc42606f221bf05aec5c472b015b8eb5e07704d8c498dbca5058adbd2eef885`  
		Last Modified: Wed, 10 Jun 2020 20:26:00 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.6.18-xenial`

```console
$ docker pull mongo@sha256:b7e0595148ec6eca2820718e205f17fb34b91a8aa51643a814b1a9721d3415c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:3.6.18-xenial` - linux; amd64

```console
$ docker pull mongo@sha256:5252e05bdca8bed4a4c537b00b15501109c341215eba935cbf969940de5fb3df
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165909480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ed1f113d4af0590a51b16321cc54e0a7cface8f0ee6b14a557b3329342fcfa3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:21:26 GMT
ADD file:52af30f80ba214985a59cb0ef7073c64f8514d58396c0de48f8d7056dec2a58a in / 
# Wed, 17 Jun 2020 01:21:27 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 01:21:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:21:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:21:29 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 05:14:46 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 05:14:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 05:14:55 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 05:14:55 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 05:15:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 05:15:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 05:15:12 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Wed, 17 Jun 2020 05:15:13 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 05:15:13 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 05:15:13 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 05:15:14 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 05:15:14 GMT
ENV MONGO_MAJOR=3.6
# Wed, 17 Jun 2020 05:15:14 GMT
ENV MONGO_VERSION=3.6.18
# Wed, 17 Jun 2020 05:15:15 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 05:15:31 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 05:15:32 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 05:15:32 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 05:15:32 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 05:15:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 05:15:33 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 05:15:33 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:b5e173e44934e01d8d2674bc8b1da00f761c4fe796e0fb2bee1bd1129d2e4ae1`  
		Last Modified: Fri, 15 May 2020 13:20:22 GMT  
		Size: 44.3 MB (44320272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29047100b0407dff554ea80b8005380d62b13a66d7fe2e2adb07b9c091b9f2c0`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 531.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15743a713c2a4033877dab08fb3989280f8c856234227158a4011811c7991372`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6bc9e2987763aa991b7dfd742be04c7b3bb04448982ffe88e58d55c93b76d4`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0742b611831efaa04736014a0196f9d038c2f66141cbae2be6191b487207f2`  
		Last Modified: Wed, 17 Jun 2020 05:17:42 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac88a40bfb757f3fd79fee2a4efdc269db4922c6c3e5bdd058b44b94d4b45a9`  
		Last Modified: Wed, 17 Jun 2020 05:17:42 GMT  
		Size: 2.9 MB (2904013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2a2c44348f93f163d89525024baa1ec80c4ea18b092a08ebb545c348e7d270`  
		Last Modified: Wed, 17 Jun 2020 05:17:42 GMT  
		Size: 1.3 MB (1305044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1c4d1da9278aa467bc18ef66e8714710039f1523ac7fe674d1e5713f162e35`  
		Last Modified: Wed, 17 Jun 2020 05:17:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fa54925dd579adcec5e2abda6b41c1ff268e7ba11a95e74ec09be18bdbc31d9`  
		Last Modified: Wed, 17 Jun 2020 05:17:41 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4b5a734c7f081c2694b37792fc6c36e2a9386f5f1b5d33c57c2b6169abca26`  
		Last Modified: Wed, 17 Jun 2020 05:17:41 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2022710a010f4e1f8a32b253836e9efd416e8dc196bbb3adcf25c30dce90a2f7`  
		Last Modified: Wed, 17 Jun 2020 05:18:00 GMT  
		Size: 117.4 MB (117370162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed0635abd18e3ba799fe897ed8ccb8b9157f10b2a8faf2671a6381703d6eee3`  
		Last Modified: Wed, 17 Jun 2020 05:17:41 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd93e12da51bd497ffebf33e89d26b8827b2608720b88ff32b72cc8174547be`  
		Last Modified: Wed, 17 Jun 2020 05:17:41 GMT  
		Size: 4.0 KB (3953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3.6.18-xenial` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:a14f1e7d0c8e74bca064fd79a7aa34a432a2f0cf2e61d4d33b352ce1a31e98d0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155250052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae20f80998fd08f33fc5181399f89cd067ac9d35d86b3a6063e6786fad946072`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:44:20 GMT
ADD file:e359a3b06531f763adba716802e252fa49b2e6126f0d3dae1451fc94f5617a13 in / 
# Wed, 17 Jun 2020 01:44:24 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 01:44:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:44:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:44:29 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:22:26 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 03:22:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:22:45 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:22:45 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 03:23:17 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:23:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:23:20 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Wed, 17 Jun 2020 03:23:22 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:23:23 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 03:23:24 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:23:25 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:23:25 GMT
ENV MONGO_MAJOR=3.6
# Wed, 17 Jun 2020 03:23:26 GMT
ENV MONGO_VERSION=3.6.18
# Wed, 17 Jun 2020 03:23:29 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 03:23:53 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 03:24:01 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 03:24:02 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 03:24:05 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:24:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:24:11 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 03:24:20 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:13340090a20bfb81868e7119dc439546fe30dcfccce42509f0fb4d998a1d1fee`  
		Last Modified: Fri, 15 May 2020 16:25:35 GMT  
		Size: 40.0 MB (40003935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75eea8c54eb3d5e45521f4ba5c57ede8436f58690cb8a37da90cfcda5efc25f7`  
		Last Modified: Wed, 17 Jun 2020 01:45:48 GMT  
		Size: 470.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857f69e728f2821d6dce88bd1c73ebda9481628a80b563e677ec423b08fdba87`  
		Last Modified: Wed, 17 Jun 2020 01:45:48 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8b20459bfc0dfbc19d643cff0a457a117336e167bb8051554fb88aee48feff`  
		Last Modified: Wed, 17 Jun 2020 01:45:48 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270afc1f069e440415e7f2ce6ea17182e6af8d92e4c8f67842fc4f54413d3b2e`  
		Last Modified: Wed, 17 Jun 2020 03:30:03 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aca9f74e6ca082c5da190f0f58ac30d4822b0ffd568394e5ffec26bb1fd6a07`  
		Last Modified: Wed, 17 Jun 2020 03:30:02 GMT  
		Size: 2.4 MB (2431869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f567c330a76a757a4b3ad26abdef55c652ebb1e0e70b77b935d3afe42d59a499`  
		Last Modified: Wed, 17 Jun 2020 03:30:03 GMT  
		Size: 1.2 MB (1232045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8e0ba58951fc1e9fa054b24cbd1cdab213c985e279cc76f8bf95465d62c50c`  
		Last Modified: Wed, 17 Jun 2020 03:30:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6273f1d75581a230d9c91081a565493238adf9a52da319953a73a76b5e1151`  
		Last Modified: Wed, 17 Jun 2020 03:30:00 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f3ee35ed8257ac4b1418f6edd3afef970462f931e9b9380a4f575c8c21149f`  
		Last Modified: Wed, 17 Jun 2020 03:30:00 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:273a73ba7a8d6fa9adfa346c96a6a9394e0af69ff18311c8afbca3ea60d5e7c4`  
		Last Modified: Wed, 17 Jun 2020 03:30:27 GMT  
		Size: 111.6 MB (111572207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab45023f72bd29157d7c5781691d982672ab51058905e1ce6a98173ebff45983`  
		Last Modified: Wed, 17 Jun 2020 03:30:00 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71e9c207cf6d3e2bf05e2d8139808a1e142a315d7067547c18467e3e2dc7b14`  
		Last Modified: Wed, 17 Jun 2020 03:30:00 GMT  
		Size: 4.0 KB (3954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.6-windowsservercore`

```console
$ docker pull mongo@sha256:bbdbeee49f3b69d6ecb3874572ad67e790cd49ac36c8f98533e9b99b922c74f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3750; amd64
	-	windows version 10.0.17763.1282; amd64

### `mongo:3.6-windowsservercore` - windows version 10.0.14393.3750; amd64

```console
$ docker pull mongo@sha256:36a967b2327cfa45e973b881bd4a7934f06ebdd8363c6cf0b69ce7a45a321237
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5827645797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5257e6147460e9d6d88072bf34645b0726d3a4ac5ec84fad7b78b32ba0cd4d4e`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 01 Jun 2020 18:53:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Jun 2020 12:52:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Jun 2020 18:12:21 GMT
ENV MONGO_VERSION=3.6.18
# Wed, 10 Jun 2020 18:12:22 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.18-signed.msi
# Wed, 10 Jun 2020 18:12:23 GMT
ENV MONGO_DOWNLOAD_SHA256=d6a17f96adcda714f523a4b119419b8bf93269542acee70e2b5e899d6d93efdc
# Wed, 10 Jun 2020 18:25:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 10 Jun 2020 18:25:54 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 10 Jun 2020 18:25:56 GMT
EXPOSE 27017
# Wed, 10 Jun 2020 18:25:57 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:375fbabb84945635805b46a02a17ac15a3177bcaae7404cfab5f1ceb0460cb60`  
		Size: 1.7 GB (1664011795 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:30efe9163d37226b077b25cd93b088cebd2ddbaadf173d143b9fe0ddecaeae53`  
		Last Modified: Wed, 10 Jun 2020 15:34:41 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7fc06f25a20433529cc677026660803d286db9e3f8a055137e0fb4adf012f30`  
		Last Modified: Wed, 10 Jun 2020 20:26:03 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba0430b99800ae303becc127d856e491cee47840694a93137ff4b541ec3dd20`  
		Last Modified: Wed, 10 Jun 2020 20:26:02 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df886cb63add8ca65718c352acc3fb8eb0fe36b91664cf0656c582179826898`  
		Last Modified: Wed, 10 Jun 2020 20:26:01 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a205b8dfbf1b2ef64f36fecadd0bdd0a24da03ec7dd0d5c067973d40ea3c899`  
		Last Modified: Wed, 10 Jun 2020 20:26:21 GMT  
		Size: 93.6 MB (93640049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5abb4100f96204b1734a5f4ddffe022067cb3e48d70ed5079fc4a2e012da1185`  
		Last Modified: Wed, 10 Jun 2020 20:25:59 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ecb46291fd9c779f2b145d5c49b5b9e9ff15565e32d19a059a4662e24db90ae`  
		Last Modified: Wed, 10 Jun 2020 20:26:00 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc42606f221bf05aec5c472b015b8eb5e07704d8c498dbca5058adbd2eef885`  
		Last Modified: Wed, 10 Jun 2020 20:26:00 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3.6-windowsservercore` - windows version 10.0.17763.1282; amd64

```console
$ docker pull mongo@sha256:92da2a1d4772d0b93fc197b68d6598b900d911a2084e0c2eda1b6ec816e6c0a2
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2386924383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a90a68509d82192dc4f3cd1515d0842e50b5b7b604bcd15c45aca2a662980f6`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Wed, 10 Jun 2020 12:43:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Jun 2020 18:26:07 GMT
ENV MONGO_VERSION=3.6.18
# Wed, 10 Jun 2020 18:26:08 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.18-signed.msi
# Wed, 10 Jun 2020 18:26:08 GMT
ENV MONGO_DOWNLOAD_SHA256=d6a17f96adcda714f523a4b119419b8bf93269542acee70e2b5e899d6d93efdc
# Wed, 10 Jun 2020 18:40:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 10 Jun 2020 18:40:02 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 10 Jun 2020 18:40:03 GMT
EXPOSE 27017
# Wed, 10 Jun 2020 18:40:04 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b11029314f3c794dc51e43c915b3e62f6b44aeb96f84b8b92f453e61cf7a2cb3`  
		Last Modified: Wed, 10 Jun 2020 15:34:12 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:637403b20232ba07d564c2a0530b1f5b8513e13afeae1720fa945dca7a4345ce`  
		Last Modified: Wed, 10 Jun 2020 20:26:38 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734ddb1043b8b11997a958386f728fdd820942a38c9d43e325e22d43e7a1c209`  
		Last Modified: Wed, 10 Jun 2020 20:26:38 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ae9516d42c6b1c8190c4da03bc21fd92905429da8fe9c022512026413d0865`  
		Last Modified: Wed, 10 Jun 2020 20:26:35 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13a450568155c9a15f52f40f17ae307bb34726b6eb47ff8c1fa2a16b6a4f040`  
		Last Modified: Wed, 10 Jun 2020 20:26:57 GMT  
		Size: 93.0 MB (93002199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0bb5eaf61d4fa06f97b072f70d10cf84b1ba68111389e690c2d6c39bc26ddc5`  
		Last Modified: Wed, 10 Jun 2020 20:26:35 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd32776d415229410f3e7acd3749e28a532e0f5f03553a9d93021571253e3934`  
		Last Modified: Wed, 10 Jun 2020 20:26:35 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6333cf051585d01194811d9da3d43c32f4b55307ce87de32482f391f6158037b`  
		Last Modified: Wed, 10 Jun 2020 20:26:35 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.6-windowsservercore-1809`

```console
$ docker pull mongo@sha256:168f93ffc37589489ff16a458b124925235e7342353261bbac8aaacf84e9cff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1282; amd64

### `mongo:3.6-windowsservercore-1809` - windows version 10.0.17763.1282; amd64

```console
$ docker pull mongo@sha256:92da2a1d4772d0b93fc197b68d6598b900d911a2084e0c2eda1b6ec816e6c0a2
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2386924383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a90a68509d82192dc4f3cd1515d0842e50b5b7b604bcd15c45aca2a662980f6`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Wed, 10 Jun 2020 12:43:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Jun 2020 18:26:07 GMT
ENV MONGO_VERSION=3.6.18
# Wed, 10 Jun 2020 18:26:08 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.18-signed.msi
# Wed, 10 Jun 2020 18:26:08 GMT
ENV MONGO_DOWNLOAD_SHA256=d6a17f96adcda714f523a4b119419b8bf93269542acee70e2b5e899d6d93efdc
# Wed, 10 Jun 2020 18:40:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 10 Jun 2020 18:40:02 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 10 Jun 2020 18:40:03 GMT
EXPOSE 27017
# Wed, 10 Jun 2020 18:40:04 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b11029314f3c794dc51e43c915b3e62f6b44aeb96f84b8b92f453e61cf7a2cb3`  
		Last Modified: Wed, 10 Jun 2020 15:34:12 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:637403b20232ba07d564c2a0530b1f5b8513e13afeae1720fa945dca7a4345ce`  
		Last Modified: Wed, 10 Jun 2020 20:26:38 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734ddb1043b8b11997a958386f728fdd820942a38c9d43e325e22d43e7a1c209`  
		Last Modified: Wed, 10 Jun 2020 20:26:38 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ae9516d42c6b1c8190c4da03bc21fd92905429da8fe9c022512026413d0865`  
		Last Modified: Wed, 10 Jun 2020 20:26:35 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13a450568155c9a15f52f40f17ae307bb34726b6eb47ff8c1fa2a16b6a4f040`  
		Last Modified: Wed, 10 Jun 2020 20:26:57 GMT  
		Size: 93.0 MB (93002199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0bb5eaf61d4fa06f97b072f70d10cf84b1ba68111389e690c2d6c39bc26ddc5`  
		Last Modified: Wed, 10 Jun 2020 20:26:35 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd32776d415229410f3e7acd3749e28a532e0f5f03553a9d93021571253e3934`  
		Last Modified: Wed, 10 Jun 2020 20:26:35 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6333cf051585d01194811d9da3d43c32f4b55307ce87de32482f391f6158037b`  
		Last Modified: Wed, 10 Jun 2020 20:26:35 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.6-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:52630676efc96befa6e39413412ef130f145cdf478f6e886a6e8cc088ef1deb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3750; amd64

### `mongo:3.6-windowsservercore-ltsc2016` - windows version 10.0.14393.3750; amd64

```console
$ docker pull mongo@sha256:36a967b2327cfa45e973b881bd4a7934f06ebdd8363c6cf0b69ce7a45a321237
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5827645797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5257e6147460e9d6d88072bf34645b0726d3a4ac5ec84fad7b78b32ba0cd4d4e`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 01 Jun 2020 18:53:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Jun 2020 12:52:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Jun 2020 18:12:21 GMT
ENV MONGO_VERSION=3.6.18
# Wed, 10 Jun 2020 18:12:22 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.18-signed.msi
# Wed, 10 Jun 2020 18:12:23 GMT
ENV MONGO_DOWNLOAD_SHA256=d6a17f96adcda714f523a4b119419b8bf93269542acee70e2b5e899d6d93efdc
# Wed, 10 Jun 2020 18:25:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 10 Jun 2020 18:25:54 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 10 Jun 2020 18:25:56 GMT
EXPOSE 27017
# Wed, 10 Jun 2020 18:25:57 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:375fbabb84945635805b46a02a17ac15a3177bcaae7404cfab5f1ceb0460cb60`  
		Size: 1.7 GB (1664011795 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:30efe9163d37226b077b25cd93b088cebd2ddbaadf173d143b9fe0ddecaeae53`  
		Last Modified: Wed, 10 Jun 2020 15:34:41 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7fc06f25a20433529cc677026660803d286db9e3f8a055137e0fb4adf012f30`  
		Last Modified: Wed, 10 Jun 2020 20:26:03 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba0430b99800ae303becc127d856e491cee47840694a93137ff4b541ec3dd20`  
		Last Modified: Wed, 10 Jun 2020 20:26:02 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df886cb63add8ca65718c352acc3fb8eb0fe36b91664cf0656c582179826898`  
		Last Modified: Wed, 10 Jun 2020 20:26:01 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a205b8dfbf1b2ef64f36fecadd0bdd0a24da03ec7dd0d5c067973d40ea3c899`  
		Last Modified: Wed, 10 Jun 2020 20:26:21 GMT  
		Size: 93.6 MB (93640049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5abb4100f96204b1734a5f4ddffe022067cb3e48d70ed5079fc4a2e012da1185`  
		Last Modified: Wed, 10 Jun 2020 20:25:59 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ecb46291fd9c779f2b145d5c49b5b9e9ff15565e32d19a059a4662e24db90ae`  
		Last Modified: Wed, 10 Jun 2020 20:26:00 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc42606f221bf05aec5c472b015b8eb5e07704d8c498dbca5058adbd2eef885`  
		Last Modified: Wed, 10 Jun 2020 20:26:00 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3.6-xenial`

```console
$ docker pull mongo@sha256:b7e0595148ec6eca2820718e205f17fb34b91a8aa51643a814b1a9721d3415c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:3.6-xenial` - linux; amd64

```console
$ docker pull mongo@sha256:5252e05bdca8bed4a4c537b00b15501109c341215eba935cbf969940de5fb3df
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165909480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ed1f113d4af0590a51b16321cc54e0a7cface8f0ee6b14a557b3329342fcfa3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:21:26 GMT
ADD file:52af30f80ba214985a59cb0ef7073c64f8514d58396c0de48f8d7056dec2a58a in / 
# Wed, 17 Jun 2020 01:21:27 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 01:21:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:21:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:21:29 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 05:14:46 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 05:14:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 05:14:55 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 05:14:55 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 05:15:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 05:15:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 05:15:12 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Wed, 17 Jun 2020 05:15:13 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 05:15:13 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 05:15:13 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 05:15:14 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 05:15:14 GMT
ENV MONGO_MAJOR=3.6
# Wed, 17 Jun 2020 05:15:14 GMT
ENV MONGO_VERSION=3.6.18
# Wed, 17 Jun 2020 05:15:15 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 05:15:31 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 05:15:32 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 05:15:32 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 05:15:32 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 05:15:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 05:15:33 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 05:15:33 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:b5e173e44934e01d8d2674bc8b1da00f761c4fe796e0fb2bee1bd1129d2e4ae1`  
		Last Modified: Fri, 15 May 2020 13:20:22 GMT  
		Size: 44.3 MB (44320272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29047100b0407dff554ea80b8005380d62b13a66d7fe2e2adb07b9c091b9f2c0`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 531.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15743a713c2a4033877dab08fb3989280f8c856234227158a4011811c7991372`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6bc9e2987763aa991b7dfd742be04c7b3bb04448982ffe88e58d55c93b76d4`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0742b611831efaa04736014a0196f9d038c2f66141cbae2be6191b487207f2`  
		Last Modified: Wed, 17 Jun 2020 05:17:42 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac88a40bfb757f3fd79fee2a4efdc269db4922c6c3e5bdd058b44b94d4b45a9`  
		Last Modified: Wed, 17 Jun 2020 05:17:42 GMT  
		Size: 2.9 MB (2904013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2a2c44348f93f163d89525024baa1ec80c4ea18b092a08ebb545c348e7d270`  
		Last Modified: Wed, 17 Jun 2020 05:17:42 GMT  
		Size: 1.3 MB (1305044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1c4d1da9278aa467bc18ef66e8714710039f1523ac7fe674d1e5713f162e35`  
		Last Modified: Wed, 17 Jun 2020 05:17:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fa54925dd579adcec5e2abda6b41c1ff268e7ba11a95e74ec09be18bdbc31d9`  
		Last Modified: Wed, 17 Jun 2020 05:17:41 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4b5a734c7f081c2694b37792fc6c36e2a9386f5f1b5d33c57c2b6169abca26`  
		Last Modified: Wed, 17 Jun 2020 05:17:41 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2022710a010f4e1f8a32b253836e9efd416e8dc196bbb3adcf25c30dce90a2f7`  
		Last Modified: Wed, 17 Jun 2020 05:18:00 GMT  
		Size: 117.4 MB (117370162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed0635abd18e3ba799fe897ed8ccb8b9157f10b2a8faf2671a6381703d6eee3`  
		Last Modified: Wed, 17 Jun 2020 05:17:41 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd93e12da51bd497ffebf33e89d26b8827b2608720b88ff32b72cc8174547be`  
		Last Modified: Wed, 17 Jun 2020 05:17:41 GMT  
		Size: 4.0 KB (3953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3.6-xenial` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:a14f1e7d0c8e74bca064fd79a7aa34a432a2f0cf2e61d4d33b352ce1a31e98d0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155250052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae20f80998fd08f33fc5181399f89cd067ac9d35d86b3a6063e6786fad946072`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:44:20 GMT
ADD file:e359a3b06531f763adba716802e252fa49b2e6126f0d3dae1451fc94f5617a13 in / 
# Wed, 17 Jun 2020 01:44:24 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 01:44:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:44:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:44:29 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:22:26 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 03:22:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:22:45 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:22:45 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 03:23:17 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:23:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:23:20 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Wed, 17 Jun 2020 03:23:22 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:23:23 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 03:23:24 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:23:25 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:23:25 GMT
ENV MONGO_MAJOR=3.6
# Wed, 17 Jun 2020 03:23:26 GMT
ENV MONGO_VERSION=3.6.18
# Wed, 17 Jun 2020 03:23:29 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 03:23:53 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 03:24:01 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 03:24:02 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 03:24:05 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:24:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:24:11 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 03:24:20 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:13340090a20bfb81868e7119dc439546fe30dcfccce42509f0fb4d998a1d1fee`  
		Last Modified: Fri, 15 May 2020 16:25:35 GMT  
		Size: 40.0 MB (40003935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75eea8c54eb3d5e45521f4ba5c57ede8436f58690cb8a37da90cfcda5efc25f7`  
		Last Modified: Wed, 17 Jun 2020 01:45:48 GMT  
		Size: 470.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857f69e728f2821d6dce88bd1c73ebda9481628a80b563e677ec423b08fdba87`  
		Last Modified: Wed, 17 Jun 2020 01:45:48 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8b20459bfc0dfbc19d643cff0a457a117336e167bb8051554fb88aee48feff`  
		Last Modified: Wed, 17 Jun 2020 01:45:48 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270afc1f069e440415e7f2ce6ea17182e6af8d92e4c8f67842fc4f54413d3b2e`  
		Last Modified: Wed, 17 Jun 2020 03:30:03 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aca9f74e6ca082c5da190f0f58ac30d4822b0ffd568394e5ffec26bb1fd6a07`  
		Last Modified: Wed, 17 Jun 2020 03:30:02 GMT  
		Size: 2.4 MB (2431869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f567c330a76a757a4b3ad26abdef55c652ebb1e0e70b77b935d3afe42d59a499`  
		Last Modified: Wed, 17 Jun 2020 03:30:03 GMT  
		Size: 1.2 MB (1232045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8e0ba58951fc1e9fa054b24cbd1cdab213c985e279cc76f8bf95465d62c50c`  
		Last Modified: Wed, 17 Jun 2020 03:30:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6273f1d75581a230d9c91081a565493238adf9a52da319953a73a76b5e1151`  
		Last Modified: Wed, 17 Jun 2020 03:30:00 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f3ee35ed8257ac4b1418f6edd3afef970462f931e9b9380a4f575c8c21149f`  
		Last Modified: Wed, 17 Jun 2020 03:30:00 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:273a73ba7a8d6fa9adfa346c96a6a9394e0af69ff18311c8afbca3ea60d5e7c4`  
		Last Modified: Wed, 17 Jun 2020 03:30:27 GMT  
		Size: 111.6 MB (111572207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab45023f72bd29157d7c5781691d982672ab51058905e1ce6a98173ebff45983`  
		Last Modified: Wed, 17 Jun 2020 03:30:00 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71e9c207cf6d3e2bf05e2d8139808a1e142a315d7067547c18467e3e2dc7b14`  
		Last Modified: Wed, 17 Jun 2020 03:30:00 GMT  
		Size: 4.0 KB (3954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3-windowsservercore`

```console
$ docker pull mongo@sha256:bbdbeee49f3b69d6ecb3874572ad67e790cd49ac36c8f98533e9b99b922c74f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3750; amd64
	-	windows version 10.0.17763.1282; amd64

### `mongo:3-windowsservercore` - windows version 10.0.14393.3750; amd64

```console
$ docker pull mongo@sha256:36a967b2327cfa45e973b881bd4a7934f06ebdd8363c6cf0b69ce7a45a321237
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5827645797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5257e6147460e9d6d88072bf34645b0726d3a4ac5ec84fad7b78b32ba0cd4d4e`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 01 Jun 2020 18:53:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Jun 2020 12:52:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Jun 2020 18:12:21 GMT
ENV MONGO_VERSION=3.6.18
# Wed, 10 Jun 2020 18:12:22 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.18-signed.msi
# Wed, 10 Jun 2020 18:12:23 GMT
ENV MONGO_DOWNLOAD_SHA256=d6a17f96adcda714f523a4b119419b8bf93269542acee70e2b5e899d6d93efdc
# Wed, 10 Jun 2020 18:25:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 10 Jun 2020 18:25:54 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 10 Jun 2020 18:25:56 GMT
EXPOSE 27017
# Wed, 10 Jun 2020 18:25:57 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:375fbabb84945635805b46a02a17ac15a3177bcaae7404cfab5f1ceb0460cb60`  
		Size: 1.7 GB (1664011795 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:30efe9163d37226b077b25cd93b088cebd2ddbaadf173d143b9fe0ddecaeae53`  
		Last Modified: Wed, 10 Jun 2020 15:34:41 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7fc06f25a20433529cc677026660803d286db9e3f8a055137e0fb4adf012f30`  
		Last Modified: Wed, 10 Jun 2020 20:26:03 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba0430b99800ae303becc127d856e491cee47840694a93137ff4b541ec3dd20`  
		Last Modified: Wed, 10 Jun 2020 20:26:02 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df886cb63add8ca65718c352acc3fb8eb0fe36b91664cf0656c582179826898`  
		Last Modified: Wed, 10 Jun 2020 20:26:01 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a205b8dfbf1b2ef64f36fecadd0bdd0a24da03ec7dd0d5c067973d40ea3c899`  
		Last Modified: Wed, 10 Jun 2020 20:26:21 GMT  
		Size: 93.6 MB (93640049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5abb4100f96204b1734a5f4ddffe022067cb3e48d70ed5079fc4a2e012da1185`  
		Last Modified: Wed, 10 Jun 2020 20:25:59 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ecb46291fd9c779f2b145d5c49b5b9e9ff15565e32d19a059a4662e24db90ae`  
		Last Modified: Wed, 10 Jun 2020 20:26:00 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc42606f221bf05aec5c472b015b8eb5e07704d8c498dbca5058adbd2eef885`  
		Last Modified: Wed, 10 Jun 2020 20:26:00 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3-windowsservercore` - windows version 10.0.17763.1282; amd64

```console
$ docker pull mongo@sha256:92da2a1d4772d0b93fc197b68d6598b900d911a2084e0c2eda1b6ec816e6c0a2
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2386924383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a90a68509d82192dc4f3cd1515d0842e50b5b7b604bcd15c45aca2a662980f6`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Wed, 10 Jun 2020 12:43:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Jun 2020 18:26:07 GMT
ENV MONGO_VERSION=3.6.18
# Wed, 10 Jun 2020 18:26:08 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.18-signed.msi
# Wed, 10 Jun 2020 18:26:08 GMT
ENV MONGO_DOWNLOAD_SHA256=d6a17f96adcda714f523a4b119419b8bf93269542acee70e2b5e899d6d93efdc
# Wed, 10 Jun 2020 18:40:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 10 Jun 2020 18:40:02 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 10 Jun 2020 18:40:03 GMT
EXPOSE 27017
# Wed, 10 Jun 2020 18:40:04 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b11029314f3c794dc51e43c915b3e62f6b44aeb96f84b8b92f453e61cf7a2cb3`  
		Last Modified: Wed, 10 Jun 2020 15:34:12 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:637403b20232ba07d564c2a0530b1f5b8513e13afeae1720fa945dca7a4345ce`  
		Last Modified: Wed, 10 Jun 2020 20:26:38 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734ddb1043b8b11997a958386f728fdd820942a38c9d43e325e22d43e7a1c209`  
		Last Modified: Wed, 10 Jun 2020 20:26:38 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ae9516d42c6b1c8190c4da03bc21fd92905429da8fe9c022512026413d0865`  
		Last Modified: Wed, 10 Jun 2020 20:26:35 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13a450568155c9a15f52f40f17ae307bb34726b6eb47ff8c1fa2a16b6a4f040`  
		Last Modified: Wed, 10 Jun 2020 20:26:57 GMT  
		Size: 93.0 MB (93002199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0bb5eaf61d4fa06f97b072f70d10cf84b1ba68111389e690c2d6c39bc26ddc5`  
		Last Modified: Wed, 10 Jun 2020 20:26:35 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd32776d415229410f3e7acd3749e28a532e0f5f03553a9d93021571253e3934`  
		Last Modified: Wed, 10 Jun 2020 20:26:35 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6333cf051585d01194811d9da3d43c32f4b55307ce87de32482f391f6158037b`  
		Last Modified: Wed, 10 Jun 2020 20:26:35 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3-windowsservercore-1809`

```console
$ docker pull mongo@sha256:168f93ffc37589489ff16a458b124925235e7342353261bbac8aaacf84e9cff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1282; amd64

### `mongo:3-windowsservercore-1809` - windows version 10.0.17763.1282; amd64

```console
$ docker pull mongo@sha256:92da2a1d4772d0b93fc197b68d6598b900d911a2084e0c2eda1b6ec816e6c0a2
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2386924383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a90a68509d82192dc4f3cd1515d0842e50b5b7b604bcd15c45aca2a662980f6`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Wed, 10 Jun 2020 12:43:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Jun 2020 18:26:07 GMT
ENV MONGO_VERSION=3.6.18
# Wed, 10 Jun 2020 18:26:08 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.18-signed.msi
# Wed, 10 Jun 2020 18:26:08 GMT
ENV MONGO_DOWNLOAD_SHA256=d6a17f96adcda714f523a4b119419b8bf93269542acee70e2b5e899d6d93efdc
# Wed, 10 Jun 2020 18:40:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 10 Jun 2020 18:40:02 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 10 Jun 2020 18:40:03 GMT
EXPOSE 27017
# Wed, 10 Jun 2020 18:40:04 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b11029314f3c794dc51e43c915b3e62f6b44aeb96f84b8b92f453e61cf7a2cb3`  
		Last Modified: Wed, 10 Jun 2020 15:34:12 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:637403b20232ba07d564c2a0530b1f5b8513e13afeae1720fa945dca7a4345ce`  
		Last Modified: Wed, 10 Jun 2020 20:26:38 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734ddb1043b8b11997a958386f728fdd820942a38c9d43e325e22d43e7a1c209`  
		Last Modified: Wed, 10 Jun 2020 20:26:38 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ae9516d42c6b1c8190c4da03bc21fd92905429da8fe9c022512026413d0865`  
		Last Modified: Wed, 10 Jun 2020 20:26:35 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13a450568155c9a15f52f40f17ae307bb34726b6eb47ff8c1fa2a16b6a4f040`  
		Last Modified: Wed, 10 Jun 2020 20:26:57 GMT  
		Size: 93.0 MB (93002199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0bb5eaf61d4fa06f97b072f70d10cf84b1ba68111389e690c2d6c39bc26ddc5`  
		Last Modified: Wed, 10 Jun 2020 20:26:35 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd32776d415229410f3e7acd3749e28a532e0f5f03553a9d93021571253e3934`  
		Last Modified: Wed, 10 Jun 2020 20:26:35 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6333cf051585d01194811d9da3d43c32f4b55307ce87de32482f391f6158037b`  
		Last Modified: Wed, 10 Jun 2020 20:26:35 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:52630676efc96befa6e39413412ef130f145cdf478f6e886a6e8cc088ef1deb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3750; amd64

### `mongo:3-windowsservercore-ltsc2016` - windows version 10.0.14393.3750; amd64

```console
$ docker pull mongo@sha256:36a967b2327cfa45e973b881bd4a7934f06ebdd8363c6cf0b69ce7a45a321237
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5827645797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5257e6147460e9d6d88072bf34645b0726d3a4ac5ec84fad7b78b32ba0cd4d4e`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 01 Jun 2020 18:53:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Jun 2020 12:52:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Jun 2020 18:12:21 GMT
ENV MONGO_VERSION=3.6.18
# Wed, 10 Jun 2020 18:12:22 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.18-signed.msi
# Wed, 10 Jun 2020 18:12:23 GMT
ENV MONGO_DOWNLOAD_SHA256=d6a17f96adcda714f523a4b119419b8bf93269542acee70e2b5e899d6d93efdc
# Wed, 10 Jun 2020 18:25:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 10 Jun 2020 18:25:54 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 10 Jun 2020 18:25:56 GMT
EXPOSE 27017
# Wed, 10 Jun 2020 18:25:57 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:375fbabb84945635805b46a02a17ac15a3177bcaae7404cfab5f1ceb0460cb60`  
		Size: 1.7 GB (1664011795 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:30efe9163d37226b077b25cd93b088cebd2ddbaadf173d143b9fe0ddecaeae53`  
		Last Modified: Wed, 10 Jun 2020 15:34:41 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7fc06f25a20433529cc677026660803d286db9e3f8a055137e0fb4adf012f30`  
		Last Modified: Wed, 10 Jun 2020 20:26:03 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba0430b99800ae303becc127d856e491cee47840694a93137ff4b541ec3dd20`  
		Last Modified: Wed, 10 Jun 2020 20:26:02 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df886cb63add8ca65718c352acc3fb8eb0fe36b91664cf0656c582179826898`  
		Last Modified: Wed, 10 Jun 2020 20:26:01 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a205b8dfbf1b2ef64f36fecadd0bdd0a24da03ec7dd0d5c067973d40ea3c899`  
		Last Modified: Wed, 10 Jun 2020 20:26:21 GMT  
		Size: 93.6 MB (93640049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5abb4100f96204b1734a5f4ddffe022067cb3e48d70ed5079fc4a2e012da1185`  
		Last Modified: Wed, 10 Jun 2020 20:25:59 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ecb46291fd9c779f2b145d5c49b5b9e9ff15565e32d19a059a4662e24db90ae`  
		Last Modified: Wed, 10 Jun 2020 20:26:00 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc42606f221bf05aec5c472b015b8eb5e07704d8c498dbca5058adbd2eef885`  
		Last Modified: Wed, 10 Jun 2020 20:26:00 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:3-xenial`

```console
$ docker pull mongo@sha256:b7e0595148ec6eca2820718e205f17fb34b91a8aa51643a814b1a9721d3415c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:3-xenial` - linux; amd64

```console
$ docker pull mongo@sha256:5252e05bdca8bed4a4c537b00b15501109c341215eba935cbf969940de5fb3df
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165909480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ed1f113d4af0590a51b16321cc54e0a7cface8f0ee6b14a557b3329342fcfa3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:21:26 GMT
ADD file:52af30f80ba214985a59cb0ef7073c64f8514d58396c0de48f8d7056dec2a58a in / 
# Wed, 17 Jun 2020 01:21:27 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 01:21:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:21:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:21:29 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 05:14:46 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 05:14:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 05:14:55 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 05:14:55 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 05:15:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 05:15:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 05:15:12 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Wed, 17 Jun 2020 05:15:13 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 05:15:13 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 05:15:13 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 05:15:14 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 05:15:14 GMT
ENV MONGO_MAJOR=3.6
# Wed, 17 Jun 2020 05:15:14 GMT
ENV MONGO_VERSION=3.6.18
# Wed, 17 Jun 2020 05:15:15 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 05:15:31 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 05:15:32 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 05:15:32 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 05:15:32 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 05:15:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 05:15:33 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 05:15:33 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:b5e173e44934e01d8d2674bc8b1da00f761c4fe796e0fb2bee1bd1129d2e4ae1`  
		Last Modified: Fri, 15 May 2020 13:20:22 GMT  
		Size: 44.3 MB (44320272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29047100b0407dff554ea80b8005380d62b13a66d7fe2e2adb07b9c091b9f2c0`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 531.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15743a713c2a4033877dab08fb3989280f8c856234227158a4011811c7991372`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6bc9e2987763aa991b7dfd742be04c7b3bb04448982ffe88e58d55c93b76d4`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0742b611831efaa04736014a0196f9d038c2f66141cbae2be6191b487207f2`  
		Last Modified: Wed, 17 Jun 2020 05:17:42 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac88a40bfb757f3fd79fee2a4efdc269db4922c6c3e5bdd058b44b94d4b45a9`  
		Last Modified: Wed, 17 Jun 2020 05:17:42 GMT  
		Size: 2.9 MB (2904013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2a2c44348f93f163d89525024baa1ec80c4ea18b092a08ebb545c348e7d270`  
		Last Modified: Wed, 17 Jun 2020 05:17:42 GMT  
		Size: 1.3 MB (1305044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1c4d1da9278aa467bc18ef66e8714710039f1523ac7fe674d1e5713f162e35`  
		Last Modified: Wed, 17 Jun 2020 05:17:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fa54925dd579adcec5e2abda6b41c1ff268e7ba11a95e74ec09be18bdbc31d9`  
		Last Modified: Wed, 17 Jun 2020 05:17:41 GMT  
		Size: 2.0 KB (1999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4b5a734c7f081c2694b37792fc6c36e2a9386f5f1b5d33c57c2b6169abca26`  
		Last Modified: Wed, 17 Jun 2020 05:17:41 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2022710a010f4e1f8a32b253836e9efd416e8dc196bbb3adcf25c30dce90a2f7`  
		Last Modified: Wed, 17 Jun 2020 05:18:00 GMT  
		Size: 117.4 MB (117370162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed0635abd18e3ba799fe897ed8ccb8b9157f10b2a8faf2671a6381703d6eee3`  
		Last Modified: Wed, 17 Jun 2020 05:17:41 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd93e12da51bd497ffebf33e89d26b8827b2608720b88ff32b72cc8174547be`  
		Last Modified: Wed, 17 Jun 2020 05:17:41 GMT  
		Size: 4.0 KB (3953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3-xenial` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:a14f1e7d0c8e74bca064fd79a7aa34a432a2f0cf2e61d4d33b352ce1a31e98d0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155250052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae20f80998fd08f33fc5181399f89cd067ac9d35d86b3a6063e6786fad946072`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:44:20 GMT
ADD file:e359a3b06531f763adba716802e252fa49b2e6126f0d3dae1451fc94f5617a13 in / 
# Wed, 17 Jun 2020 01:44:24 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 01:44:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:44:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:44:29 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:22:26 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 03:22:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:22:45 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:22:45 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 03:23:17 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:23:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:23:20 GMT
ENV GPG_KEYS=2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Wed, 17 Jun 2020 03:23:22 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:23:23 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 03:23:24 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:23:25 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:23:25 GMT
ENV MONGO_MAJOR=3.6
# Wed, 17 Jun 2020 03:23:26 GMT
ENV MONGO_VERSION=3.6.18
# Wed, 17 Jun 2020 03:23:29 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 03:23:53 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 03:24:01 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 03:24:02 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 03:24:05 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:24:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:24:11 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 03:24:20 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:13340090a20bfb81868e7119dc439546fe30dcfccce42509f0fb4d998a1d1fee`  
		Last Modified: Fri, 15 May 2020 16:25:35 GMT  
		Size: 40.0 MB (40003935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75eea8c54eb3d5e45521f4ba5c57ede8436f58690cb8a37da90cfcda5efc25f7`  
		Last Modified: Wed, 17 Jun 2020 01:45:48 GMT  
		Size: 470.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857f69e728f2821d6dce88bd1c73ebda9481628a80b563e677ec423b08fdba87`  
		Last Modified: Wed, 17 Jun 2020 01:45:48 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8b20459bfc0dfbc19d643cff0a457a117336e167bb8051554fb88aee48feff`  
		Last Modified: Wed, 17 Jun 2020 01:45:48 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270afc1f069e440415e7f2ce6ea17182e6af8d92e4c8f67842fc4f54413d3b2e`  
		Last Modified: Wed, 17 Jun 2020 03:30:03 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aca9f74e6ca082c5da190f0f58ac30d4822b0ffd568394e5ffec26bb1fd6a07`  
		Last Modified: Wed, 17 Jun 2020 03:30:02 GMT  
		Size: 2.4 MB (2431869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f567c330a76a757a4b3ad26abdef55c652ebb1e0e70b77b935d3afe42d59a499`  
		Last Modified: Wed, 17 Jun 2020 03:30:03 GMT  
		Size: 1.2 MB (1232045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8e0ba58951fc1e9fa054b24cbd1cdab213c985e279cc76f8bf95465d62c50c`  
		Last Modified: Wed, 17 Jun 2020 03:30:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6273f1d75581a230d9c91081a565493238adf9a52da319953a73a76b5e1151`  
		Last Modified: Wed, 17 Jun 2020 03:30:00 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f3ee35ed8257ac4b1418f6edd3afef970462f931e9b9380a4f575c8c21149f`  
		Last Modified: Wed, 17 Jun 2020 03:30:00 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:273a73ba7a8d6fa9adfa346c96a6a9394e0af69ff18311c8afbca3ea60d5e7c4`  
		Last Modified: Wed, 17 Jun 2020 03:30:27 GMT  
		Size: 111.6 MB (111572207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab45023f72bd29157d7c5781691d982672ab51058905e1ce6a98173ebff45983`  
		Last Modified: Wed, 17 Jun 2020 03:30:00 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71e9c207cf6d3e2bf05e2d8139808a1e142a315d7067547c18467e3e2dc7b14`  
		Last Modified: Wed, 17 Jun 2020 03:30:00 GMT  
		Size: 4.0 KB (3954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4`

```console
$ docker pull mongo@sha256:29805e9a6fc2a233b9b633c7b0f382a43df3f119522b82366a72abecb302a793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x
	-	windows version 10.0.14393.3750; amd64
	-	windows version 10.0.17763.1282; amd64

### `mongo:4` - linux; amd64

```console
$ docker pull mongo@sha256:ed04fcf28fccf1bb2c295074775a24ddd007e14ca522ae97a56983f269cad163
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164652387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2cc1f48aed02a160b0447fd28b75952ed1d2df8c66693733d4954483734e44`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:20:29 GMT
ADD file:1e8d02626176dc8141df3c0a1365774ce73d79934654fe24a4b1e7f173108232 in / 
# Wed, 17 Jun 2020 01:20:30 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:20:31 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:20:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:20:32 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 05:16:06 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 05:16:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 05:16:16 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 05:16:16 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 05:16:30 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 05:16:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 05:16:33 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Wed, 17 Jun 2020 05:16:34 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 05:16:34 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 05:16:34 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 05:16:34 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 05:16:34 GMT
ENV MONGO_MAJOR=4.2
# Wed, 17 Jun 2020 05:16:35 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 17 Jun 2020 05:16:35 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 05:16:53 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 05:16:54 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 05:16:54 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 05:16:54 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 05:16:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 05:16:55 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 05:16:55 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:d7c3167c320d7a820935f54cf4290890ea19567da496ecf774e8773b35d5f065`  
		Last Modified: Wed, 27 May 2020 12:21:15 GMT  
		Size: 26.7 MB (26688718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:131f805ec7fd68d45a887e2ef82de61de0247b4eb934ab03b7c933650e854baa`  
		Last Modified: Wed, 17 Jun 2020 01:21:41 GMT  
		Size: 35.4 KB (35369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322ed380e680a77f30528ba013e3a802a7b44948a0609c7d1d732dd46a9a310d`  
		Last Modified: Wed, 17 Jun 2020 01:21:41 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac240b130982ad1c3ba3188abbf18ba4e54bdd9e504ce2d5c2eff6d3e86b8dd`  
		Last Modified: Wed, 17 Jun 2020 01:21:41 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5704a01b59ff4d100b5bcc0244090cb5b369649b41a468a82cb5015afdc4f9d`  
		Last Modified: Wed, 17 Jun 2020 05:18:30 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e396e2a1e6820b238c82087b900e4f03e1304b30ee16a5341b0c6a2a9eec20e`  
		Last Modified: Wed, 17 Jun 2020 05:18:29 GMT  
		Size: 3.0 MB (2973543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:914fffcb1cc543f9e16861fe6d80fdaad26ea9c69ba952c73cb3db44a9cfc545`  
		Last Modified: Wed, 17 Jun 2020 05:18:30 GMT  
		Size: 5.8 MB (5823974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692bd0d35810fbf133d67af4f0ae0c627fb731b875d5370d3dfaa3f1a06392fa`  
		Last Modified: Wed, 17 Jun 2020 05:18:29 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122d231765e47cbdd1b934b3ee55ffa291b76b17e4134be5b6e9837c52053c9e`  
		Last Modified: Wed, 17 Jun 2020 05:18:28 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9c497305ce2ee80e9d80fb69dcf2766f51b6b23e093fbf9d0d837b14376810`  
		Last Modified: Wed, 17 Jun 2020 05:18:28 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e3ca7a65fcd8d5d002ae04e06a5d7b900020097dec64e04923b9fa25d7d633`  
		Last Modified: Wed, 17 Jun 2020 05:18:46 GMT  
		Size: 129.1 MB (129122023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70e0d9672b4cbcef6ddbaa3fae90fb8181aeb83b59cac8f4910d69f7c359f96`  
		Last Modified: Wed, 17 Jun 2020 05:18:28 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc04aade5db18c8ca826bfaef542aa9b48f2b3045dfe7a4fa0d4f11714d37a1`  
		Last Modified: Wed, 17 Jun 2020 05:18:28 GMT  
		Size: 4.0 KB (3955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:cdec0bd28e60bc06892f9972803753d57fdc3d4bcff657b694ba7f35b80d3d02
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154677642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f84af28ce3aa3b7b04964d7f7ee9eb0ae10e3c19e684ad29ceeca55c605f2924`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:42:33 GMT
ADD file:7dc8819fd3d4b84ad19fb836e5bfda64a5ffefc371166f70d4d41dff6b22d450 in / 
# Wed, 17 Jun 2020 01:42:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:42:41 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:42:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:42:45 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:26:00 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 03:26:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:26:24 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:26:25 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 03:27:01 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:27:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:27:06 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Wed, 17 Jun 2020 03:27:10 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:27:12 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 03:27:13 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:27:16 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:27:19 GMT
ENV MONGO_MAJOR=4.2
# Wed, 17 Jun 2020 03:27:20 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 17 Jun 2020 03:27:23 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 03:27:58 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 03:28:02 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 03:28:04 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 03:28:05 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:28:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:28:08 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 03:28:09 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:2e8bea8b22f8f5a4fd5aa85019945dd8ae04f283a4ba2a7aeb4536fe2f1d1ec2`  
		Last Modified: Tue, 26 May 2020 16:25:25 GMT  
		Size: 23.7 MB (23721687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc90876b9c9a7343ae432eaec7c8dc8859c1e84b6193da8d386815fde165a70e`  
		Last Modified: Wed, 17 Jun 2020 01:44:48 GMT  
		Size: 35.2 KB (35192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bfc658a5210a9f0c9cfcda5f504e720da9268e9f3f3bf48e3a9a7af360c959`  
		Last Modified: Wed, 17 Jun 2020 01:44:49 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef0f1b06b2142ff2bf35cc565f019ed9e4efe0d8f332825167538c2337bac8a`  
		Last Modified: Wed, 17 Jun 2020 01:44:49 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79f4068e2fc9c5ce913c3640637c35584b72816ca9485c4bf5af0a22994d0f6`  
		Last Modified: Wed, 17 Jun 2020 03:31:11 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5678c55b212ca2ce4ea7b4092838653b706277000f57d7a18526f3df6cba283`  
		Last Modified: Wed, 17 Jun 2020 03:31:11 GMT  
		Size: 2.7 MB (2665976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509de0ccfb79a34de230a6fef2cfc900bdb35f1f7f583fc957b7c23b46439d4f`  
		Last Modified: Wed, 17 Jun 2020 03:31:12 GMT  
		Size: 5.3 MB (5345550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5493b54160873a149e08eedf09e74628680b1d5e8826b90672f04c88c30ccb`  
		Last Modified: Wed, 17 Jun 2020 03:31:10 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe2b58fe1082de604f779b26f7bac0f685326b5584f5a43457f1d51effdca86`  
		Last Modified: Wed, 17 Jun 2020 03:31:09 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52cb618aa3e851b5a35792b706fd4e70901c2e3fd1faa3fcf12d719ac3d8ff1`  
		Last Modified: Wed, 17 Jun 2020 03:31:08 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8985f89f29dd85eccbd8da50a080817fa846f7b7baee89e54e83f79559fff4b`  
		Last Modified: Wed, 17 Jun 2020 03:31:35 GMT  
		Size: 122.9 MB (122900361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f01ca57315b3f1a9469f85034d0f072b2d67b5ee9d3c9d2e14e3487df4db4d`  
		Last Modified: Wed, 17 Jun 2020 03:31:08 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f414fc1b8d9a096289a531b03096d4af7478a1c627842175a15974cb041c879`  
		Last Modified: Wed, 17 Jun 2020 03:31:08 GMT  
		Size: 4.0 KB (3950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4` - linux; s390x

```console
$ docker pull mongo@sha256:e1c13c3ee8ae7031fdaa1e4cb645de3279a46ccf47511a9fb4b82c90d5c831f5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160598470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddfb01efb7ddfe0ac3ea40d0ded51ac1742d89e522b72b9ca43ec82ac2a642b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:41:48 GMT
ADD file:8708e93980b416070ba0bb024a7858748129059a85d2c771a4489c31710a9df1 in / 
# Wed, 17 Jun 2020 01:41:51 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:41:52 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:41:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:41:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:24:26 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 03:24:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:24:35 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:24:35 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 03:24:46 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:24:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:24:47 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Wed, 17 Jun 2020 03:24:48 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:24:48 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 03:24:48 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:24:48 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:24:48 GMT
ENV MONGO_MAJOR=4.2
# Wed, 17 Jun 2020 03:24:49 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 17 Jun 2020 03:24:49 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 03:25:14 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 03:25:18 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 03:25:18 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 03:25:19 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:25:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:25:19 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 03:25:19 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f3c26641772baa3348c0cce190edb38690a41f1824570c5c65cc363b42e5a5b5`  
		Last Modified: Sat, 30 May 2020 09:30:29 GMT  
		Size: 25.4 MB (25365846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf76fcee55454304ffbf9e321dda388a7e8de8a3916f854e1e588bc6c19b088`  
		Last Modified: Wed, 17 Jun 2020 01:42:56 GMT  
		Size: 36.2 KB (36165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5173e4f9f1868daa26021e1e701a000b0aadb2b611a487d089e7de4b728a7424`  
		Last Modified: Wed, 17 Jun 2020 01:42:56 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13da9fe451bd0f377d042d4bebef4ffd19163113e3e66dcd718fe187149a0dbd`  
		Last Modified: Wed, 17 Jun 2020 01:42:57 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d8fc9b1e9007ca5666c42ff8398a5227869b151fea1562c5e3cfb2188640e6`  
		Last Modified: Wed, 17 Jun 2020 03:28:52 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a889c8302a90f8884ff21edb649cf8dc1771453aca39505e61f29e053a1b64`  
		Last Modified: Wed, 17 Jun 2020 03:28:51 GMT  
		Size: 2.7 MB (2704483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:582fe8ee181790ce5fdadeef1c1cd7af40de0e8d2cb2e307fa05aed8d23a82b7`  
		Last Modified: Wed, 17 Jun 2020 03:28:50 GMT  
		Size: 5.7 MB (5745080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6096f1fa9fe7ad82ea015203f2410ac8b0831d0617db029aed54c698f84a2eaf`  
		Last Modified: Wed, 17 Jun 2020 03:28:50 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2bddaa2c78c2b5ac010b9af305db894e7bb616461499b863fe6af05c42bb502`  
		Last Modified: Wed, 17 Jun 2020 03:28:48 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b0ea0902452b7fe6fc59cc6001683eb80ddf80ba9fa1a59f83a576855317e12`  
		Last Modified: Wed, 17 Jun 2020 03:28:48 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507e67f4e596fea4d40f10e6ca9132a57d472a59bef2ce47ae79b92eb029ca7a`  
		Last Modified: Wed, 17 Jun 2020 03:29:02 GMT  
		Size: 126.7 MB (126738040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf93b294dbde6159d09390ee7231284abcaad59049a9d10eaebfc46619d4ad3`  
		Last Modified: Wed, 17 Jun 2020 03:28:48 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e514b21a3b45674ce414ecd79bf6adc339e8ea02fc1a80956ece983f3192be`  
		Last Modified: Wed, 17 Jun 2020 03:29:03 GMT  
		Size: 4.0 KB (3953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4` - windows version 10.0.14393.3750; amd64

```console
$ docker pull mongo@sha256:af38590235375eb1218ddd651e660f1a6e6e6a882842e7b428f2d55d46cc937a
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6193023222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aaf2b53fe9e096da5ab6f4ae0e34caf7cf3de0a336bd9576cee60752c37c17b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 01 Jun 2020 18:53:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Jun 2020 12:52:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 17 Jun 2020 00:50:43 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 17 Jun 2020 00:50:44 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 17 Jun 2020 00:50:45 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 17 Jun 2020 01:08:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 17 Jun 2020 01:08:52 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 17 Jun 2020 01:08:53 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 01:08:54 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:375fbabb84945635805b46a02a17ac15a3177bcaae7404cfab5f1ceb0460cb60`  
		Size: 1.7 GB (1664011795 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:30efe9163d37226b077b25cd93b088cebd2ddbaadf173d143b9fe0ddecaeae53`  
		Last Modified: Wed, 10 Jun 2020 15:34:41 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b60479ef88c8a931aeeffaa74d289fbbf204229adb6a20c54d51456f70bb75`  
		Last Modified: Wed, 17 Jun 2020 01:32:04 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52bb592e6eb6512ccf1127b0311263697d559599357972414f4b776277bd628f`  
		Last Modified: Wed, 17 Jun 2020 01:32:04 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e57b55cda98f10b8c536232f9fd5fbc19c778c4043edc4fea012972832bb4570`  
		Last Modified: Wed, 17 Jun 2020 01:32:01 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eaad7a52f6dc4a311c3e724f9b5fe27f7af849fa6229fe21fc0490976fcb607`  
		Last Modified: Wed, 17 Jun 2020 01:32:57 GMT  
		Size: 459.0 MB (459017760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187b8e518ef05e3f4e7348e0ca7fef3e05414c63661223d63d83a36367ff9605`  
		Last Modified: Wed, 17 Jun 2020 01:32:01 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58773855217e4f81876fd21fd13a61d94d0f5a191e7025ce2bf26469077e330c`  
		Last Modified: Wed, 17 Jun 2020 01:32:01 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e25f1762a4dcad6fd6709c2602e0d459a0efb6aea6e10e16cb78796c27e496d`  
		Last Modified: Wed, 17 Jun 2020 01:32:01 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4` - windows version 10.0.17763.1282; amd64

```console
$ docker pull mongo@sha256:a332d0d55bcb861ab664609d4ee8b7a3c7481e800fa5ad62009c671c1673af0b
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2752054828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86c12ab59b3d8850d880c02f06724769d7955a42bb4c5b10fd9a16cb6ad19f7`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Wed, 10 Jun 2020 12:43:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 17 Jun 2020 01:09:02 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 17 Jun 2020 01:09:03 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 17 Jun 2020 01:09:04 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 17 Jun 2020 01:28:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 17 Jun 2020 01:28:16 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 17 Jun 2020 01:28:18 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 01:28:19 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b11029314f3c794dc51e43c915b3e62f6b44aeb96f84b8b92f453e61cf7a2cb3`  
		Last Modified: Wed, 10 Jun 2020 15:34:12 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f51df57f2cb6ccc03b57cbd044ee4a49d9383489feb3872da465ba8b6bffa89`  
		Last Modified: Wed, 17 Jun 2020 01:33:19 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84353c49610a99480bfb74a8769e7446bbd898b8644c25d2b8c645c7a2e90e0e`  
		Last Modified: Wed, 17 Jun 2020 01:33:18 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c19d206596ed0cd1b7da30ba6e637be1d4c31dc398ca6f4d30d583593e31705`  
		Last Modified: Wed, 17 Jun 2020 01:33:16 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90fa0f2b93199d15d0678aa8a13db7d1470a5ce7ddb94ec8fa93a75156cce44`  
		Last Modified: Wed, 17 Jun 2020 01:34:14 GMT  
		Size: 458.1 MB (458132610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:369180762b76f75c56ed85ad59e938011c514ad32b51a43cbb6d5fcce885b5d1`  
		Last Modified: Wed, 17 Jun 2020 01:33:16 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f9c110c11f811446f2204714562c02b6eefeeb1cae671aa73af5e4cc7dfbd0`  
		Last Modified: Wed, 17 Jun 2020 01:33:16 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c7a275e52c9eafb08caf7a861ef21a725b77ee54c1b867ddb4b4da99814dd7`  
		Last Modified: Wed, 17 Jun 2020 01:33:16 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.0`

```console
$ docker pull mongo@sha256:f9abc51175e73c807bd146689c563980e12a1f797aba153d13961e91e5a45c11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.14393.3750; amd64
	-	windows version 10.0.17763.1282; amd64

### `mongo:4.0` - linux; amd64

```console
$ docker pull mongo@sha256:7e87b7e743c943be2520b0475da0ada3b254e6bf9817a3d1e97777ea575c40b6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.8 MB (153792832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e541b5559917be313d87d6b879d85e429dc6aec5df3b3e4ddc3d150660b9a45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:21:26 GMT
ADD file:52af30f80ba214985a59cb0ef7073c64f8514d58396c0de48f8d7056dec2a58a in / 
# Wed, 17 Jun 2020 01:21:27 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 01:21:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:21:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:21:29 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 05:14:46 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 05:14:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 05:14:55 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 05:14:55 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 05:15:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 05:15:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 05:15:40 GMT
ENV GPG_KEYS=9DA31620334BD75D9DCB49F368818C72E52529D4
# Wed, 17 Jun 2020 05:15:41 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 05:15:41 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 05:15:41 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 05:15:41 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 05:15:41 GMT
ENV MONGO_MAJOR=4.0
# Wed, 17 Jun 2020 05:15:41 GMT
ENV MONGO_VERSION=4.0.19
# Wed, 17 Jun 2020 05:15:42 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 05:15:59 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 05:16:00 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 05:16:00 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 05:16:00 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 05:16:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 05:16:01 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 05:16:01 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:b5e173e44934e01d8d2674bc8b1da00f761c4fe796e0fb2bee1bd1129d2e4ae1`  
		Last Modified: Fri, 15 May 2020 13:20:22 GMT  
		Size: 44.3 MB (44320272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29047100b0407dff554ea80b8005380d62b13a66d7fe2e2adb07b9c091b9f2c0`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 531.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15743a713c2a4033877dab08fb3989280f8c856234227158a4011811c7991372`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6bc9e2987763aa991b7dfd742be04c7b3bb04448982ffe88e58d55c93b76d4`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0742b611831efaa04736014a0196f9d038c2f66141cbae2be6191b487207f2`  
		Last Modified: Wed, 17 Jun 2020 05:17:42 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac88a40bfb757f3fd79fee2a4efdc269db4922c6c3e5bdd058b44b94d4b45a9`  
		Last Modified: Wed, 17 Jun 2020 05:17:42 GMT  
		Size: 2.9 MB (2904013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2a2c44348f93f163d89525024baa1ec80c4ea18b092a08ebb545c348e7d270`  
		Last Modified: Wed, 17 Jun 2020 05:17:42 GMT  
		Size: 1.3 MB (1305044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1c4d1da9278aa467bc18ef66e8714710039f1523ac7fe674d1e5713f162e35`  
		Last Modified: Wed, 17 Jun 2020 05:17:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f710eae0da44706cdd69fb6df1b0b3c65539a2359f36e8ad614993f2e60ecff`  
		Last Modified: Wed, 17 Jun 2020 05:18:05 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca24f3ca70c39253780feea5588acd8b8010b7f559515fa6153a547afb370d8f`  
		Last Modified: Wed, 17 Jun 2020 05:18:05 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c5ae9ffe7bc3613be27b4e795c3aba5ac34c39f3ea309373238bb76a28056f3`  
		Last Modified: Wed, 17 Jun 2020 05:18:22 GMT  
		Size: 105.3 MB (105254085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71541f27ccb019a43dae7fcc9929d489102490704b1c79bf4289d6c88c8d2e83`  
		Last Modified: Wed, 17 Jun 2020 05:18:06 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf2098794726bab4c816a3a21cd0ce0434456e797560b578dcd59bac416551f`  
		Last Modified: Wed, 17 Jun 2020 05:18:05 GMT  
		Size: 4.0 KB (3955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:2ceebfb3ba9dd87bee897485561b8c7b82065c0281127ab5f4782f38c2481d9c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.4 MB (143363263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cebd15eb77de47468757b975d4a261739eb155ba1e116c7dfe1bfa01bda91a22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:44:20 GMT
ADD file:e359a3b06531f763adba716802e252fa49b2e6126f0d3dae1451fc94f5617a13 in / 
# Wed, 17 Jun 2020 01:44:24 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 01:44:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:44:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:44:29 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:22:26 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 03:22:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:22:45 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:22:45 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 03:23:17 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:23:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:24:39 GMT
ENV GPG_KEYS=9DA31620334BD75D9DCB49F368818C72E52529D4
# Wed, 17 Jun 2020 03:24:42 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:24:43 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 03:24:44 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:24:45 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:24:46 GMT
ENV MONGO_MAJOR=4.0
# Wed, 17 Jun 2020 03:24:47 GMT
ENV MONGO_VERSION=4.0.19
# Wed, 17 Jun 2020 03:24:49 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 03:25:33 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 03:25:36 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 03:25:38 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 03:25:39 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:25:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:25:41 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 03:25:43 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:13340090a20bfb81868e7119dc439546fe30dcfccce42509f0fb4d998a1d1fee`  
		Last Modified: Fri, 15 May 2020 16:25:35 GMT  
		Size: 40.0 MB (40003935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75eea8c54eb3d5e45521f4ba5c57ede8436f58690cb8a37da90cfcda5efc25f7`  
		Last Modified: Wed, 17 Jun 2020 01:45:48 GMT  
		Size: 470.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857f69e728f2821d6dce88bd1c73ebda9481628a80b563e677ec423b08fdba87`  
		Last Modified: Wed, 17 Jun 2020 01:45:48 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8b20459bfc0dfbc19d643cff0a457a117336e167bb8051554fb88aee48feff`  
		Last Modified: Wed, 17 Jun 2020 01:45:48 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270afc1f069e440415e7f2ce6ea17182e6af8d92e4c8f67842fc4f54413d3b2e`  
		Last Modified: Wed, 17 Jun 2020 03:30:03 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aca9f74e6ca082c5da190f0f58ac30d4822b0ffd568394e5ffec26bb1fd6a07`  
		Last Modified: Wed, 17 Jun 2020 03:30:02 GMT  
		Size: 2.4 MB (2431869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f567c330a76a757a4b3ad26abdef55c652ebb1e0e70b77b935d3afe42d59a499`  
		Last Modified: Wed, 17 Jun 2020 03:30:03 GMT  
		Size: 1.2 MB (1232045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8e0ba58951fc1e9fa054b24cbd1cdab213c985e279cc76f8bf95465d62c50c`  
		Last Modified: Wed, 17 Jun 2020 03:30:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c1fdd5271b26ffe0d62b29b25121931dcdbe6ebb7ea49ba6b24fd99e266112a`  
		Last Modified: Wed, 17 Jun 2020 03:30:36 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd7739bdf8cd161542061f5bc73b8a6756dd8a561f9b8209a6d091aa4fcc503`  
		Last Modified: Wed, 17 Jun 2020 03:30:36 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac0483829d143872abb4f5eb93398b84d81da48055989fac0d4a17d73360ee5b`  
		Last Modified: Wed, 17 Jun 2020 03:31:01 GMT  
		Size: 99.7 MB (99685983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbaee99aa1bb5266c3f49a40599712f23081844d6f9f1242a95e952fc787ed19`  
		Last Modified: Wed, 17 Jun 2020 03:30:36 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6839344713a90022b7a568a420d74d75dab8bc2e7bf09a66fdb6c56ce063795e`  
		Last Modified: Wed, 17 Jun 2020 03:30:36 GMT  
		Size: 4.0 KB (3956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0` - windows version 10.0.14393.3750; amd64

```console
$ docker pull mongo@sha256:1a3468a39b95b542655927d7e0a04353366dc703ded677e6c22451360c87bac9
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6183054924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c053b22eb0ec81f93e0935c743ad67ebefcb1a5799d222cabaf3c11a513caffc`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 01 Jun 2020 18:53:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Jun 2020 12:52:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 17 Jun 2020 00:14:52 GMT
ENV MONGO_VERSION=4.0.19
# Wed, 17 Jun 2020 00:14:53 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.19-signed.msi
# Wed, 17 Jun 2020 00:14:54 GMT
ENV MONGO_DOWNLOAD_SHA256=fcdadb2d83e21551da2e8302f6cdab69ac840d4b1cca2cb353853c5d81aebac6
# Wed, 17 Jun 2020 00:32:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 17 Jun 2020 00:32:17 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 17 Jun 2020 00:32:18 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 00:32:20 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:375fbabb84945635805b46a02a17ac15a3177bcaae7404cfab5f1ceb0460cb60`  
		Size: 1.7 GB (1664011795 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:30efe9163d37226b077b25cd93b088cebd2ddbaadf173d143b9fe0ddecaeae53`  
		Last Modified: Wed, 10 Jun 2020 15:34:41 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:816499e8d3b97fdb4d8e47ee9d0d1f281a3b1eeb8850ff030523cff88380321e`  
		Last Modified: Wed, 17 Jun 2020 01:29:35 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26a589c682f9703eb3d409e2032c7919de1aefc19a3cb393b0c064eaef6f0be`  
		Last Modified: Wed, 17 Jun 2020 01:29:35 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d73871c04674ed1c797392fe5bec4228f05654ebf5a6a58435036fb1abe2ee`  
		Last Modified: Wed, 17 Jun 2020 01:29:32 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726d3ce65aa1b227ef614b059b137963db5ee0a8bc95a4a730d085a97fe6bc33`  
		Last Modified: Wed, 17 Jun 2020 01:30:29 GMT  
		Size: 449.0 MB (449049166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad0ff8e9f21a3c1e912d9eeeeb97ee2d5c553ee879ec5f5cccd0a184698a8a7`  
		Last Modified: Wed, 17 Jun 2020 01:29:31 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305f20c2735d1ba169d52da0302e523ab3b2c09d047ff177d330c3b6a1bd6026`  
		Last Modified: Wed, 17 Jun 2020 01:29:32 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78f51b73ffa29728a6caf389cb3cb091a7706b2ea1f1013eeace11097778c12`  
		Last Modified: Wed, 17 Jun 2020 01:29:31 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0` - windows version 10.0.17763.1282; amd64

```console
$ docker pull mongo@sha256:eb7fd8e0a8c3db95868d8e17bab4ac26092180248fc0b068cd15bc286cb2d083
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2742131599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:737ee931c2d9a8f5de2d151517486894b4a41d3b3339fbb6c2a6e0c65bedeccb`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Wed, 10 Jun 2020 12:43:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 17 Jun 2020 00:32:25 GMT
ENV MONGO_VERSION=4.0.19
# Wed, 17 Jun 2020 00:32:26 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.19-signed.msi
# Wed, 17 Jun 2020 00:32:27 GMT
ENV MONGO_DOWNLOAD_SHA256=fcdadb2d83e21551da2e8302f6cdab69ac840d4b1cca2cb353853c5d81aebac6
# Wed, 17 Jun 2020 00:50:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 17 Jun 2020 00:50:35 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 17 Jun 2020 00:50:36 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 00:50:38 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b11029314f3c794dc51e43c915b3e62f6b44aeb96f84b8b92f453e61cf7a2cb3`  
		Last Modified: Wed, 10 Jun 2020 15:34:12 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a707c5dc762ba141d7a8cfbec6295f374527707f6eaf5c98abb2e978cfdd69c`  
		Last Modified: Wed, 17 Jun 2020 01:30:44 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8348966f83fe75692293e65cfde9e25e61e57e47a99fde23ecd73642b2ff5b`  
		Last Modified: Wed, 17 Jun 2020 01:30:44 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:887dfff9dc52cbfb40b678f03ca01f03f8ac6c6d2d6ff0b5975d3a124bd1dc01`  
		Last Modified: Wed, 17 Jun 2020 01:30:42 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4de8a718850e42fbd3d5b80d7812a66349a84429e6723b9737fbdf391b6698c`  
		Last Modified: Wed, 17 Jun 2020 01:31:41 GMT  
		Size: 448.2 MB (448209541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111da423a065bc6ecad62ce7b9f223431a830dc2e9b4cb1648197242d7588792`  
		Last Modified: Wed, 17 Jun 2020 01:30:42 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03a5bc7d4fd2ff019705f4be25c3f277871730c361ca588a58adff3b8e908cd2`  
		Last Modified: Wed, 17 Jun 2020 01:30:42 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80595cd8b92d2c1a9701d89839040895c7da7b2a27ecc9acc28d2784b311c1f2`  
		Last Modified: Wed, 17 Jun 2020 01:30:42 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.0.19`

```console
$ docker pull mongo@sha256:f9abc51175e73c807bd146689c563980e12a1f797aba153d13961e91e5a45c11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.14393.3750; amd64
	-	windows version 10.0.17763.1282; amd64

### `mongo:4.0.19` - linux; amd64

```console
$ docker pull mongo@sha256:7e87b7e743c943be2520b0475da0ada3b254e6bf9817a3d1e97777ea575c40b6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.8 MB (153792832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e541b5559917be313d87d6b879d85e429dc6aec5df3b3e4ddc3d150660b9a45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:21:26 GMT
ADD file:52af30f80ba214985a59cb0ef7073c64f8514d58396c0de48f8d7056dec2a58a in / 
# Wed, 17 Jun 2020 01:21:27 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 01:21:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:21:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:21:29 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 05:14:46 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 05:14:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 05:14:55 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 05:14:55 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 05:15:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 05:15:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 05:15:40 GMT
ENV GPG_KEYS=9DA31620334BD75D9DCB49F368818C72E52529D4
# Wed, 17 Jun 2020 05:15:41 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 05:15:41 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 05:15:41 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 05:15:41 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 05:15:41 GMT
ENV MONGO_MAJOR=4.0
# Wed, 17 Jun 2020 05:15:41 GMT
ENV MONGO_VERSION=4.0.19
# Wed, 17 Jun 2020 05:15:42 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 05:15:59 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 05:16:00 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 05:16:00 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 05:16:00 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 05:16:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 05:16:01 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 05:16:01 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:b5e173e44934e01d8d2674bc8b1da00f761c4fe796e0fb2bee1bd1129d2e4ae1`  
		Last Modified: Fri, 15 May 2020 13:20:22 GMT  
		Size: 44.3 MB (44320272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29047100b0407dff554ea80b8005380d62b13a66d7fe2e2adb07b9c091b9f2c0`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 531.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15743a713c2a4033877dab08fb3989280f8c856234227158a4011811c7991372`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6bc9e2987763aa991b7dfd742be04c7b3bb04448982ffe88e58d55c93b76d4`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0742b611831efaa04736014a0196f9d038c2f66141cbae2be6191b487207f2`  
		Last Modified: Wed, 17 Jun 2020 05:17:42 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac88a40bfb757f3fd79fee2a4efdc269db4922c6c3e5bdd058b44b94d4b45a9`  
		Last Modified: Wed, 17 Jun 2020 05:17:42 GMT  
		Size: 2.9 MB (2904013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2a2c44348f93f163d89525024baa1ec80c4ea18b092a08ebb545c348e7d270`  
		Last Modified: Wed, 17 Jun 2020 05:17:42 GMT  
		Size: 1.3 MB (1305044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1c4d1da9278aa467bc18ef66e8714710039f1523ac7fe674d1e5713f162e35`  
		Last Modified: Wed, 17 Jun 2020 05:17:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f710eae0da44706cdd69fb6df1b0b3c65539a2359f36e8ad614993f2e60ecff`  
		Last Modified: Wed, 17 Jun 2020 05:18:05 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca24f3ca70c39253780feea5588acd8b8010b7f559515fa6153a547afb370d8f`  
		Last Modified: Wed, 17 Jun 2020 05:18:05 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c5ae9ffe7bc3613be27b4e795c3aba5ac34c39f3ea309373238bb76a28056f3`  
		Last Modified: Wed, 17 Jun 2020 05:18:22 GMT  
		Size: 105.3 MB (105254085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71541f27ccb019a43dae7fcc9929d489102490704b1c79bf4289d6c88c8d2e83`  
		Last Modified: Wed, 17 Jun 2020 05:18:06 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf2098794726bab4c816a3a21cd0ce0434456e797560b578dcd59bac416551f`  
		Last Modified: Wed, 17 Jun 2020 05:18:05 GMT  
		Size: 4.0 KB (3955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0.19` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:2ceebfb3ba9dd87bee897485561b8c7b82065c0281127ab5f4782f38c2481d9c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.4 MB (143363263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cebd15eb77de47468757b975d4a261739eb155ba1e116c7dfe1bfa01bda91a22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:44:20 GMT
ADD file:e359a3b06531f763adba716802e252fa49b2e6126f0d3dae1451fc94f5617a13 in / 
# Wed, 17 Jun 2020 01:44:24 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 01:44:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:44:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:44:29 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:22:26 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 03:22:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:22:45 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:22:45 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 03:23:17 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:23:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:24:39 GMT
ENV GPG_KEYS=9DA31620334BD75D9DCB49F368818C72E52529D4
# Wed, 17 Jun 2020 03:24:42 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:24:43 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 03:24:44 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:24:45 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:24:46 GMT
ENV MONGO_MAJOR=4.0
# Wed, 17 Jun 2020 03:24:47 GMT
ENV MONGO_VERSION=4.0.19
# Wed, 17 Jun 2020 03:24:49 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 03:25:33 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 03:25:36 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 03:25:38 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 03:25:39 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:25:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:25:41 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 03:25:43 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:13340090a20bfb81868e7119dc439546fe30dcfccce42509f0fb4d998a1d1fee`  
		Last Modified: Fri, 15 May 2020 16:25:35 GMT  
		Size: 40.0 MB (40003935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75eea8c54eb3d5e45521f4ba5c57ede8436f58690cb8a37da90cfcda5efc25f7`  
		Last Modified: Wed, 17 Jun 2020 01:45:48 GMT  
		Size: 470.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857f69e728f2821d6dce88bd1c73ebda9481628a80b563e677ec423b08fdba87`  
		Last Modified: Wed, 17 Jun 2020 01:45:48 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8b20459bfc0dfbc19d643cff0a457a117336e167bb8051554fb88aee48feff`  
		Last Modified: Wed, 17 Jun 2020 01:45:48 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270afc1f069e440415e7f2ce6ea17182e6af8d92e4c8f67842fc4f54413d3b2e`  
		Last Modified: Wed, 17 Jun 2020 03:30:03 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aca9f74e6ca082c5da190f0f58ac30d4822b0ffd568394e5ffec26bb1fd6a07`  
		Last Modified: Wed, 17 Jun 2020 03:30:02 GMT  
		Size: 2.4 MB (2431869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f567c330a76a757a4b3ad26abdef55c652ebb1e0e70b77b935d3afe42d59a499`  
		Last Modified: Wed, 17 Jun 2020 03:30:03 GMT  
		Size: 1.2 MB (1232045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8e0ba58951fc1e9fa054b24cbd1cdab213c985e279cc76f8bf95465d62c50c`  
		Last Modified: Wed, 17 Jun 2020 03:30:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c1fdd5271b26ffe0d62b29b25121931dcdbe6ebb7ea49ba6b24fd99e266112a`  
		Last Modified: Wed, 17 Jun 2020 03:30:36 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd7739bdf8cd161542061f5bc73b8a6756dd8a561f9b8209a6d091aa4fcc503`  
		Last Modified: Wed, 17 Jun 2020 03:30:36 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac0483829d143872abb4f5eb93398b84d81da48055989fac0d4a17d73360ee5b`  
		Last Modified: Wed, 17 Jun 2020 03:31:01 GMT  
		Size: 99.7 MB (99685983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbaee99aa1bb5266c3f49a40599712f23081844d6f9f1242a95e952fc787ed19`  
		Last Modified: Wed, 17 Jun 2020 03:30:36 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6839344713a90022b7a568a420d74d75dab8bc2e7bf09a66fdb6c56ce063795e`  
		Last Modified: Wed, 17 Jun 2020 03:30:36 GMT  
		Size: 4.0 KB (3956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0.19` - windows version 10.0.14393.3750; amd64

```console
$ docker pull mongo@sha256:1a3468a39b95b542655927d7e0a04353366dc703ded677e6c22451360c87bac9
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6183054924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c053b22eb0ec81f93e0935c743ad67ebefcb1a5799d222cabaf3c11a513caffc`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 01 Jun 2020 18:53:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Jun 2020 12:52:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 17 Jun 2020 00:14:52 GMT
ENV MONGO_VERSION=4.0.19
# Wed, 17 Jun 2020 00:14:53 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.19-signed.msi
# Wed, 17 Jun 2020 00:14:54 GMT
ENV MONGO_DOWNLOAD_SHA256=fcdadb2d83e21551da2e8302f6cdab69ac840d4b1cca2cb353853c5d81aebac6
# Wed, 17 Jun 2020 00:32:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 17 Jun 2020 00:32:17 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 17 Jun 2020 00:32:18 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 00:32:20 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:375fbabb84945635805b46a02a17ac15a3177bcaae7404cfab5f1ceb0460cb60`  
		Size: 1.7 GB (1664011795 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:30efe9163d37226b077b25cd93b088cebd2ddbaadf173d143b9fe0ddecaeae53`  
		Last Modified: Wed, 10 Jun 2020 15:34:41 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:816499e8d3b97fdb4d8e47ee9d0d1f281a3b1eeb8850ff030523cff88380321e`  
		Last Modified: Wed, 17 Jun 2020 01:29:35 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26a589c682f9703eb3d409e2032c7919de1aefc19a3cb393b0c064eaef6f0be`  
		Last Modified: Wed, 17 Jun 2020 01:29:35 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d73871c04674ed1c797392fe5bec4228f05654ebf5a6a58435036fb1abe2ee`  
		Last Modified: Wed, 17 Jun 2020 01:29:32 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726d3ce65aa1b227ef614b059b137963db5ee0a8bc95a4a730d085a97fe6bc33`  
		Last Modified: Wed, 17 Jun 2020 01:30:29 GMT  
		Size: 449.0 MB (449049166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad0ff8e9f21a3c1e912d9eeeeb97ee2d5c553ee879ec5f5cccd0a184698a8a7`  
		Last Modified: Wed, 17 Jun 2020 01:29:31 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305f20c2735d1ba169d52da0302e523ab3b2c09d047ff177d330c3b6a1bd6026`  
		Last Modified: Wed, 17 Jun 2020 01:29:32 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78f51b73ffa29728a6caf389cb3cb091a7706b2ea1f1013eeace11097778c12`  
		Last Modified: Wed, 17 Jun 2020 01:29:31 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0.19` - windows version 10.0.17763.1282; amd64

```console
$ docker pull mongo@sha256:eb7fd8e0a8c3db95868d8e17bab4ac26092180248fc0b068cd15bc286cb2d083
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2742131599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:737ee931c2d9a8f5de2d151517486894b4a41d3b3339fbb6c2a6e0c65bedeccb`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Wed, 10 Jun 2020 12:43:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 17 Jun 2020 00:32:25 GMT
ENV MONGO_VERSION=4.0.19
# Wed, 17 Jun 2020 00:32:26 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.19-signed.msi
# Wed, 17 Jun 2020 00:32:27 GMT
ENV MONGO_DOWNLOAD_SHA256=fcdadb2d83e21551da2e8302f6cdab69ac840d4b1cca2cb353853c5d81aebac6
# Wed, 17 Jun 2020 00:50:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 17 Jun 2020 00:50:35 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 17 Jun 2020 00:50:36 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 00:50:38 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b11029314f3c794dc51e43c915b3e62f6b44aeb96f84b8b92f453e61cf7a2cb3`  
		Last Modified: Wed, 10 Jun 2020 15:34:12 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a707c5dc762ba141d7a8cfbec6295f374527707f6eaf5c98abb2e978cfdd69c`  
		Last Modified: Wed, 17 Jun 2020 01:30:44 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8348966f83fe75692293e65cfde9e25e61e57e47a99fde23ecd73642b2ff5b`  
		Last Modified: Wed, 17 Jun 2020 01:30:44 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:887dfff9dc52cbfb40b678f03ca01f03f8ac6c6d2d6ff0b5975d3a124bd1dc01`  
		Last Modified: Wed, 17 Jun 2020 01:30:42 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4de8a718850e42fbd3d5b80d7812a66349a84429e6723b9737fbdf391b6698c`  
		Last Modified: Wed, 17 Jun 2020 01:31:41 GMT  
		Size: 448.2 MB (448209541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111da423a065bc6ecad62ce7b9f223431a830dc2e9b4cb1648197242d7588792`  
		Last Modified: Wed, 17 Jun 2020 01:30:42 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03a5bc7d4fd2ff019705f4be25c3f277871730c361ca588a58adff3b8e908cd2`  
		Last Modified: Wed, 17 Jun 2020 01:30:42 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80595cd8b92d2c1a9701d89839040895c7da7b2a27ecc9acc28d2784b311c1f2`  
		Last Modified: Wed, 17 Jun 2020 01:30:42 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.0.19-windowsservercore`

```console
$ docker pull mongo@sha256:228832407c9cfccf7c1c7820b2c8df88413ac75638d8db733fd8e94706097a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3750; amd64
	-	windows version 10.0.17763.1282; amd64

### `mongo:4.0.19-windowsservercore` - windows version 10.0.14393.3750; amd64

```console
$ docker pull mongo@sha256:1a3468a39b95b542655927d7e0a04353366dc703ded677e6c22451360c87bac9
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6183054924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c053b22eb0ec81f93e0935c743ad67ebefcb1a5799d222cabaf3c11a513caffc`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 01 Jun 2020 18:53:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Jun 2020 12:52:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 17 Jun 2020 00:14:52 GMT
ENV MONGO_VERSION=4.0.19
# Wed, 17 Jun 2020 00:14:53 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.19-signed.msi
# Wed, 17 Jun 2020 00:14:54 GMT
ENV MONGO_DOWNLOAD_SHA256=fcdadb2d83e21551da2e8302f6cdab69ac840d4b1cca2cb353853c5d81aebac6
# Wed, 17 Jun 2020 00:32:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 17 Jun 2020 00:32:17 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 17 Jun 2020 00:32:18 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 00:32:20 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:375fbabb84945635805b46a02a17ac15a3177bcaae7404cfab5f1ceb0460cb60`  
		Size: 1.7 GB (1664011795 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:30efe9163d37226b077b25cd93b088cebd2ddbaadf173d143b9fe0ddecaeae53`  
		Last Modified: Wed, 10 Jun 2020 15:34:41 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:816499e8d3b97fdb4d8e47ee9d0d1f281a3b1eeb8850ff030523cff88380321e`  
		Last Modified: Wed, 17 Jun 2020 01:29:35 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26a589c682f9703eb3d409e2032c7919de1aefc19a3cb393b0c064eaef6f0be`  
		Last Modified: Wed, 17 Jun 2020 01:29:35 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d73871c04674ed1c797392fe5bec4228f05654ebf5a6a58435036fb1abe2ee`  
		Last Modified: Wed, 17 Jun 2020 01:29:32 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726d3ce65aa1b227ef614b059b137963db5ee0a8bc95a4a730d085a97fe6bc33`  
		Last Modified: Wed, 17 Jun 2020 01:30:29 GMT  
		Size: 449.0 MB (449049166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad0ff8e9f21a3c1e912d9eeeeb97ee2d5c553ee879ec5f5cccd0a184698a8a7`  
		Last Modified: Wed, 17 Jun 2020 01:29:31 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305f20c2735d1ba169d52da0302e523ab3b2c09d047ff177d330c3b6a1bd6026`  
		Last Modified: Wed, 17 Jun 2020 01:29:32 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78f51b73ffa29728a6caf389cb3cb091a7706b2ea1f1013eeace11097778c12`  
		Last Modified: Wed, 17 Jun 2020 01:29:31 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0.19-windowsservercore` - windows version 10.0.17763.1282; amd64

```console
$ docker pull mongo@sha256:eb7fd8e0a8c3db95868d8e17bab4ac26092180248fc0b068cd15bc286cb2d083
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2742131599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:737ee931c2d9a8f5de2d151517486894b4a41d3b3339fbb6c2a6e0c65bedeccb`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Wed, 10 Jun 2020 12:43:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 17 Jun 2020 00:32:25 GMT
ENV MONGO_VERSION=4.0.19
# Wed, 17 Jun 2020 00:32:26 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.19-signed.msi
# Wed, 17 Jun 2020 00:32:27 GMT
ENV MONGO_DOWNLOAD_SHA256=fcdadb2d83e21551da2e8302f6cdab69ac840d4b1cca2cb353853c5d81aebac6
# Wed, 17 Jun 2020 00:50:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 17 Jun 2020 00:50:35 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 17 Jun 2020 00:50:36 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 00:50:38 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b11029314f3c794dc51e43c915b3e62f6b44aeb96f84b8b92f453e61cf7a2cb3`  
		Last Modified: Wed, 10 Jun 2020 15:34:12 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a707c5dc762ba141d7a8cfbec6295f374527707f6eaf5c98abb2e978cfdd69c`  
		Last Modified: Wed, 17 Jun 2020 01:30:44 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8348966f83fe75692293e65cfde9e25e61e57e47a99fde23ecd73642b2ff5b`  
		Last Modified: Wed, 17 Jun 2020 01:30:44 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:887dfff9dc52cbfb40b678f03ca01f03f8ac6c6d2d6ff0b5975d3a124bd1dc01`  
		Last Modified: Wed, 17 Jun 2020 01:30:42 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4de8a718850e42fbd3d5b80d7812a66349a84429e6723b9737fbdf391b6698c`  
		Last Modified: Wed, 17 Jun 2020 01:31:41 GMT  
		Size: 448.2 MB (448209541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111da423a065bc6ecad62ce7b9f223431a830dc2e9b4cb1648197242d7588792`  
		Last Modified: Wed, 17 Jun 2020 01:30:42 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03a5bc7d4fd2ff019705f4be25c3f277871730c361ca588a58adff3b8e908cd2`  
		Last Modified: Wed, 17 Jun 2020 01:30:42 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80595cd8b92d2c1a9701d89839040895c7da7b2a27ecc9acc28d2784b311c1f2`  
		Last Modified: Wed, 17 Jun 2020 01:30:42 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.0.19-windowsservercore-1809`

```console
$ docker pull mongo@sha256:758f3d74b248ca29c188aa7afe6af40107e685b039e4182fedca012d4e981702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1282; amd64

### `mongo:4.0.19-windowsservercore-1809` - windows version 10.0.17763.1282; amd64

```console
$ docker pull mongo@sha256:eb7fd8e0a8c3db95868d8e17bab4ac26092180248fc0b068cd15bc286cb2d083
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2742131599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:737ee931c2d9a8f5de2d151517486894b4a41d3b3339fbb6c2a6e0c65bedeccb`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Wed, 10 Jun 2020 12:43:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 17 Jun 2020 00:32:25 GMT
ENV MONGO_VERSION=4.0.19
# Wed, 17 Jun 2020 00:32:26 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.19-signed.msi
# Wed, 17 Jun 2020 00:32:27 GMT
ENV MONGO_DOWNLOAD_SHA256=fcdadb2d83e21551da2e8302f6cdab69ac840d4b1cca2cb353853c5d81aebac6
# Wed, 17 Jun 2020 00:50:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 17 Jun 2020 00:50:35 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 17 Jun 2020 00:50:36 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 00:50:38 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b11029314f3c794dc51e43c915b3e62f6b44aeb96f84b8b92f453e61cf7a2cb3`  
		Last Modified: Wed, 10 Jun 2020 15:34:12 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a707c5dc762ba141d7a8cfbec6295f374527707f6eaf5c98abb2e978cfdd69c`  
		Last Modified: Wed, 17 Jun 2020 01:30:44 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8348966f83fe75692293e65cfde9e25e61e57e47a99fde23ecd73642b2ff5b`  
		Last Modified: Wed, 17 Jun 2020 01:30:44 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:887dfff9dc52cbfb40b678f03ca01f03f8ac6c6d2d6ff0b5975d3a124bd1dc01`  
		Last Modified: Wed, 17 Jun 2020 01:30:42 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4de8a718850e42fbd3d5b80d7812a66349a84429e6723b9737fbdf391b6698c`  
		Last Modified: Wed, 17 Jun 2020 01:31:41 GMT  
		Size: 448.2 MB (448209541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111da423a065bc6ecad62ce7b9f223431a830dc2e9b4cb1648197242d7588792`  
		Last Modified: Wed, 17 Jun 2020 01:30:42 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03a5bc7d4fd2ff019705f4be25c3f277871730c361ca588a58adff3b8e908cd2`  
		Last Modified: Wed, 17 Jun 2020 01:30:42 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80595cd8b92d2c1a9701d89839040895c7da7b2a27ecc9acc28d2784b311c1f2`  
		Last Modified: Wed, 17 Jun 2020 01:30:42 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.0.19-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:bdf25441c3ae280bf10aa80c445d6eb90f76a8e2d288bfa13d2798aca90c85b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3750; amd64

### `mongo:4.0.19-windowsservercore-ltsc2016` - windows version 10.0.14393.3750; amd64

```console
$ docker pull mongo@sha256:1a3468a39b95b542655927d7e0a04353366dc703ded677e6c22451360c87bac9
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6183054924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c053b22eb0ec81f93e0935c743ad67ebefcb1a5799d222cabaf3c11a513caffc`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 01 Jun 2020 18:53:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Jun 2020 12:52:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 17 Jun 2020 00:14:52 GMT
ENV MONGO_VERSION=4.0.19
# Wed, 17 Jun 2020 00:14:53 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.19-signed.msi
# Wed, 17 Jun 2020 00:14:54 GMT
ENV MONGO_DOWNLOAD_SHA256=fcdadb2d83e21551da2e8302f6cdab69ac840d4b1cca2cb353853c5d81aebac6
# Wed, 17 Jun 2020 00:32:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 17 Jun 2020 00:32:17 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 17 Jun 2020 00:32:18 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 00:32:20 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:375fbabb84945635805b46a02a17ac15a3177bcaae7404cfab5f1ceb0460cb60`  
		Size: 1.7 GB (1664011795 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:30efe9163d37226b077b25cd93b088cebd2ddbaadf173d143b9fe0ddecaeae53`  
		Last Modified: Wed, 10 Jun 2020 15:34:41 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:816499e8d3b97fdb4d8e47ee9d0d1f281a3b1eeb8850ff030523cff88380321e`  
		Last Modified: Wed, 17 Jun 2020 01:29:35 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26a589c682f9703eb3d409e2032c7919de1aefc19a3cb393b0c064eaef6f0be`  
		Last Modified: Wed, 17 Jun 2020 01:29:35 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d73871c04674ed1c797392fe5bec4228f05654ebf5a6a58435036fb1abe2ee`  
		Last Modified: Wed, 17 Jun 2020 01:29:32 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726d3ce65aa1b227ef614b059b137963db5ee0a8bc95a4a730d085a97fe6bc33`  
		Last Modified: Wed, 17 Jun 2020 01:30:29 GMT  
		Size: 449.0 MB (449049166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad0ff8e9f21a3c1e912d9eeeeb97ee2d5c553ee879ec5f5cccd0a184698a8a7`  
		Last Modified: Wed, 17 Jun 2020 01:29:31 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305f20c2735d1ba169d52da0302e523ab3b2c09d047ff177d330c3b6a1bd6026`  
		Last Modified: Wed, 17 Jun 2020 01:29:32 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78f51b73ffa29728a6caf389cb3cb091a7706b2ea1f1013eeace11097778c12`  
		Last Modified: Wed, 17 Jun 2020 01:29:31 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.0.19-xenial`

```console
$ docker pull mongo@sha256:bc35602421ae30f947a73d2c7e188840fc2137d5216f68ed63a5671acd988d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:4.0.19-xenial` - linux; amd64

```console
$ docker pull mongo@sha256:7e87b7e743c943be2520b0475da0ada3b254e6bf9817a3d1e97777ea575c40b6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.8 MB (153792832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e541b5559917be313d87d6b879d85e429dc6aec5df3b3e4ddc3d150660b9a45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:21:26 GMT
ADD file:52af30f80ba214985a59cb0ef7073c64f8514d58396c0de48f8d7056dec2a58a in / 
# Wed, 17 Jun 2020 01:21:27 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 01:21:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:21:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:21:29 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 05:14:46 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 05:14:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 05:14:55 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 05:14:55 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 05:15:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 05:15:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 05:15:40 GMT
ENV GPG_KEYS=9DA31620334BD75D9DCB49F368818C72E52529D4
# Wed, 17 Jun 2020 05:15:41 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 05:15:41 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 05:15:41 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 05:15:41 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 05:15:41 GMT
ENV MONGO_MAJOR=4.0
# Wed, 17 Jun 2020 05:15:41 GMT
ENV MONGO_VERSION=4.0.19
# Wed, 17 Jun 2020 05:15:42 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 05:15:59 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 05:16:00 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 05:16:00 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 05:16:00 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 05:16:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 05:16:01 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 05:16:01 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:b5e173e44934e01d8d2674bc8b1da00f761c4fe796e0fb2bee1bd1129d2e4ae1`  
		Last Modified: Fri, 15 May 2020 13:20:22 GMT  
		Size: 44.3 MB (44320272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29047100b0407dff554ea80b8005380d62b13a66d7fe2e2adb07b9c091b9f2c0`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 531.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15743a713c2a4033877dab08fb3989280f8c856234227158a4011811c7991372`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6bc9e2987763aa991b7dfd742be04c7b3bb04448982ffe88e58d55c93b76d4`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0742b611831efaa04736014a0196f9d038c2f66141cbae2be6191b487207f2`  
		Last Modified: Wed, 17 Jun 2020 05:17:42 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac88a40bfb757f3fd79fee2a4efdc269db4922c6c3e5bdd058b44b94d4b45a9`  
		Last Modified: Wed, 17 Jun 2020 05:17:42 GMT  
		Size: 2.9 MB (2904013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2a2c44348f93f163d89525024baa1ec80c4ea18b092a08ebb545c348e7d270`  
		Last Modified: Wed, 17 Jun 2020 05:17:42 GMT  
		Size: 1.3 MB (1305044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1c4d1da9278aa467bc18ef66e8714710039f1523ac7fe674d1e5713f162e35`  
		Last Modified: Wed, 17 Jun 2020 05:17:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f710eae0da44706cdd69fb6df1b0b3c65539a2359f36e8ad614993f2e60ecff`  
		Last Modified: Wed, 17 Jun 2020 05:18:05 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca24f3ca70c39253780feea5588acd8b8010b7f559515fa6153a547afb370d8f`  
		Last Modified: Wed, 17 Jun 2020 05:18:05 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c5ae9ffe7bc3613be27b4e795c3aba5ac34c39f3ea309373238bb76a28056f3`  
		Last Modified: Wed, 17 Jun 2020 05:18:22 GMT  
		Size: 105.3 MB (105254085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71541f27ccb019a43dae7fcc9929d489102490704b1c79bf4289d6c88c8d2e83`  
		Last Modified: Wed, 17 Jun 2020 05:18:06 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf2098794726bab4c816a3a21cd0ce0434456e797560b578dcd59bac416551f`  
		Last Modified: Wed, 17 Jun 2020 05:18:05 GMT  
		Size: 4.0 KB (3955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0.19-xenial` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:2ceebfb3ba9dd87bee897485561b8c7b82065c0281127ab5f4782f38c2481d9c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.4 MB (143363263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cebd15eb77de47468757b975d4a261739eb155ba1e116c7dfe1bfa01bda91a22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:44:20 GMT
ADD file:e359a3b06531f763adba716802e252fa49b2e6126f0d3dae1451fc94f5617a13 in / 
# Wed, 17 Jun 2020 01:44:24 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 01:44:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:44:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:44:29 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:22:26 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 03:22:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:22:45 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:22:45 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 03:23:17 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:23:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:24:39 GMT
ENV GPG_KEYS=9DA31620334BD75D9DCB49F368818C72E52529D4
# Wed, 17 Jun 2020 03:24:42 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:24:43 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 03:24:44 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:24:45 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:24:46 GMT
ENV MONGO_MAJOR=4.0
# Wed, 17 Jun 2020 03:24:47 GMT
ENV MONGO_VERSION=4.0.19
# Wed, 17 Jun 2020 03:24:49 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 03:25:33 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 03:25:36 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 03:25:38 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 03:25:39 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:25:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:25:41 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 03:25:43 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:13340090a20bfb81868e7119dc439546fe30dcfccce42509f0fb4d998a1d1fee`  
		Last Modified: Fri, 15 May 2020 16:25:35 GMT  
		Size: 40.0 MB (40003935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75eea8c54eb3d5e45521f4ba5c57ede8436f58690cb8a37da90cfcda5efc25f7`  
		Last Modified: Wed, 17 Jun 2020 01:45:48 GMT  
		Size: 470.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857f69e728f2821d6dce88bd1c73ebda9481628a80b563e677ec423b08fdba87`  
		Last Modified: Wed, 17 Jun 2020 01:45:48 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8b20459bfc0dfbc19d643cff0a457a117336e167bb8051554fb88aee48feff`  
		Last Modified: Wed, 17 Jun 2020 01:45:48 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270afc1f069e440415e7f2ce6ea17182e6af8d92e4c8f67842fc4f54413d3b2e`  
		Last Modified: Wed, 17 Jun 2020 03:30:03 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aca9f74e6ca082c5da190f0f58ac30d4822b0ffd568394e5ffec26bb1fd6a07`  
		Last Modified: Wed, 17 Jun 2020 03:30:02 GMT  
		Size: 2.4 MB (2431869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f567c330a76a757a4b3ad26abdef55c652ebb1e0e70b77b935d3afe42d59a499`  
		Last Modified: Wed, 17 Jun 2020 03:30:03 GMT  
		Size: 1.2 MB (1232045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8e0ba58951fc1e9fa054b24cbd1cdab213c985e279cc76f8bf95465d62c50c`  
		Last Modified: Wed, 17 Jun 2020 03:30:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c1fdd5271b26ffe0d62b29b25121931dcdbe6ebb7ea49ba6b24fd99e266112a`  
		Last Modified: Wed, 17 Jun 2020 03:30:36 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd7739bdf8cd161542061f5bc73b8a6756dd8a561f9b8209a6d091aa4fcc503`  
		Last Modified: Wed, 17 Jun 2020 03:30:36 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac0483829d143872abb4f5eb93398b84d81da48055989fac0d4a17d73360ee5b`  
		Last Modified: Wed, 17 Jun 2020 03:31:01 GMT  
		Size: 99.7 MB (99685983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbaee99aa1bb5266c3f49a40599712f23081844d6f9f1242a95e952fc787ed19`  
		Last Modified: Wed, 17 Jun 2020 03:30:36 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6839344713a90022b7a568a420d74d75dab8bc2e7bf09a66fdb6c56ce063795e`  
		Last Modified: Wed, 17 Jun 2020 03:30:36 GMT  
		Size: 4.0 KB (3956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.0-windowsservercore`

```console
$ docker pull mongo@sha256:228832407c9cfccf7c1c7820b2c8df88413ac75638d8db733fd8e94706097a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3750; amd64
	-	windows version 10.0.17763.1282; amd64

### `mongo:4.0-windowsservercore` - windows version 10.0.14393.3750; amd64

```console
$ docker pull mongo@sha256:1a3468a39b95b542655927d7e0a04353366dc703ded677e6c22451360c87bac9
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6183054924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c053b22eb0ec81f93e0935c743ad67ebefcb1a5799d222cabaf3c11a513caffc`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 01 Jun 2020 18:53:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Jun 2020 12:52:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 17 Jun 2020 00:14:52 GMT
ENV MONGO_VERSION=4.0.19
# Wed, 17 Jun 2020 00:14:53 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.19-signed.msi
# Wed, 17 Jun 2020 00:14:54 GMT
ENV MONGO_DOWNLOAD_SHA256=fcdadb2d83e21551da2e8302f6cdab69ac840d4b1cca2cb353853c5d81aebac6
# Wed, 17 Jun 2020 00:32:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 17 Jun 2020 00:32:17 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 17 Jun 2020 00:32:18 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 00:32:20 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:375fbabb84945635805b46a02a17ac15a3177bcaae7404cfab5f1ceb0460cb60`  
		Size: 1.7 GB (1664011795 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:30efe9163d37226b077b25cd93b088cebd2ddbaadf173d143b9fe0ddecaeae53`  
		Last Modified: Wed, 10 Jun 2020 15:34:41 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:816499e8d3b97fdb4d8e47ee9d0d1f281a3b1eeb8850ff030523cff88380321e`  
		Last Modified: Wed, 17 Jun 2020 01:29:35 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26a589c682f9703eb3d409e2032c7919de1aefc19a3cb393b0c064eaef6f0be`  
		Last Modified: Wed, 17 Jun 2020 01:29:35 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d73871c04674ed1c797392fe5bec4228f05654ebf5a6a58435036fb1abe2ee`  
		Last Modified: Wed, 17 Jun 2020 01:29:32 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726d3ce65aa1b227ef614b059b137963db5ee0a8bc95a4a730d085a97fe6bc33`  
		Last Modified: Wed, 17 Jun 2020 01:30:29 GMT  
		Size: 449.0 MB (449049166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad0ff8e9f21a3c1e912d9eeeeb97ee2d5c553ee879ec5f5cccd0a184698a8a7`  
		Last Modified: Wed, 17 Jun 2020 01:29:31 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305f20c2735d1ba169d52da0302e523ab3b2c09d047ff177d330c3b6a1bd6026`  
		Last Modified: Wed, 17 Jun 2020 01:29:32 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78f51b73ffa29728a6caf389cb3cb091a7706b2ea1f1013eeace11097778c12`  
		Last Modified: Wed, 17 Jun 2020 01:29:31 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0-windowsservercore` - windows version 10.0.17763.1282; amd64

```console
$ docker pull mongo@sha256:eb7fd8e0a8c3db95868d8e17bab4ac26092180248fc0b068cd15bc286cb2d083
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2742131599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:737ee931c2d9a8f5de2d151517486894b4a41d3b3339fbb6c2a6e0c65bedeccb`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Wed, 10 Jun 2020 12:43:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 17 Jun 2020 00:32:25 GMT
ENV MONGO_VERSION=4.0.19
# Wed, 17 Jun 2020 00:32:26 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.19-signed.msi
# Wed, 17 Jun 2020 00:32:27 GMT
ENV MONGO_DOWNLOAD_SHA256=fcdadb2d83e21551da2e8302f6cdab69ac840d4b1cca2cb353853c5d81aebac6
# Wed, 17 Jun 2020 00:50:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 17 Jun 2020 00:50:35 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 17 Jun 2020 00:50:36 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 00:50:38 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b11029314f3c794dc51e43c915b3e62f6b44aeb96f84b8b92f453e61cf7a2cb3`  
		Last Modified: Wed, 10 Jun 2020 15:34:12 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a707c5dc762ba141d7a8cfbec6295f374527707f6eaf5c98abb2e978cfdd69c`  
		Last Modified: Wed, 17 Jun 2020 01:30:44 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8348966f83fe75692293e65cfde9e25e61e57e47a99fde23ecd73642b2ff5b`  
		Last Modified: Wed, 17 Jun 2020 01:30:44 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:887dfff9dc52cbfb40b678f03ca01f03f8ac6c6d2d6ff0b5975d3a124bd1dc01`  
		Last Modified: Wed, 17 Jun 2020 01:30:42 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4de8a718850e42fbd3d5b80d7812a66349a84429e6723b9737fbdf391b6698c`  
		Last Modified: Wed, 17 Jun 2020 01:31:41 GMT  
		Size: 448.2 MB (448209541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111da423a065bc6ecad62ce7b9f223431a830dc2e9b4cb1648197242d7588792`  
		Last Modified: Wed, 17 Jun 2020 01:30:42 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03a5bc7d4fd2ff019705f4be25c3f277871730c361ca588a58adff3b8e908cd2`  
		Last Modified: Wed, 17 Jun 2020 01:30:42 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80595cd8b92d2c1a9701d89839040895c7da7b2a27ecc9acc28d2784b311c1f2`  
		Last Modified: Wed, 17 Jun 2020 01:30:42 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.0-windowsservercore-1809`

```console
$ docker pull mongo@sha256:758f3d74b248ca29c188aa7afe6af40107e685b039e4182fedca012d4e981702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1282; amd64

### `mongo:4.0-windowsservercore-1809` - windows version 10.0.17763.1282; amd64

```console
$ docker pull mongo@sha256:eb7fd8e0a8c3db95868d8e17bab4ac26092180248fc0b068cd15bc286cb2d083
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2742131599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:737ee931c2d9a8f5de2d151517486894b4a41d3b3339fbb6c2a6e0c65bedeccb`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Wed, 10 Jun 2020 12:43:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 17 Jun 2020 00:32:25 GMT
ENV MONGO_VERSION=4.0.19
# Wed, 17 Jun 2020 00:32:26 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.19-signed.msi
# Wed, 17 Jun 2020 00:32:27 GMT
ENV MONGO_DOWNLOAD_SHA256=fcdadb2d83e21551da2e8302f6cdab69ac840d4b1cca2cb353853c5d81aebac6
# Wed, 17 Jun 2020 00:50:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 17 Jun 2020 00:50:35 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 17 Jun 2020 00:50:36 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 00:50:38 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b11029314f3c794dc51e43c915b3e62f6b44aeb96f84b8b92f453e61cf7a2cb3`  
		Last Modified: Wed, 10 Jun 2020 15:34:12 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a707c5dc762ba141d7a8cfbec6295f374527707f6eaf5c98abb2e978cfdd69c`  
		Last Modified: Wed, 17 Jun 2020 01:30:44 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8348966f83fe75692293e65cfde9e25e61e57e47a99fde23ecd73642b2ff5b`  
		Last Modified: Wed, 17 Jun 2020 01:30:44 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:887dfff9dc52cbfb40b678f03ca01f03f8ac6c6d2d6ff0b5975d3a124bd1dc01`  
		Last Modified: Wed, 17 Jun 2020 01:30:42 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4de8a718850e42fbd3d5b80d7812a66349a84429e6723b9737fbdf391b6698c`  
		Last Modified: Wed, 17 Jun 2020 01:31:41 GMT  
		Size: 448.2 MB (448209541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111da423a065bc6ecad62ce7b9f223431a830dc2e9b4cb1648197242d7588792`  
		Last Modified: Wed, 17 Jun 2020 01:30:42 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03a5bc7d4fd2ff019705f4be25c3f277871730c361ca588a58adff3b8e908cd2`  
		Last Modified: Wed, 17 Jun 2020 01:30:42 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80595cd8b92d2c1a9701d89839040895c7da7b2a27ecc9acc28d2784b311c1f2`  
		Last Modified: Wed, 17 Jun 2020 01:30:42 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.0-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:bdf25441c3ae280bf10aa80c445d6eb90f76a8e2d288bfa13d2798aca90c85b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3750; amd64

### `mongo:4.0-windowsservercore-ltsc2016` - windows version 10.0.14393.3750; amd64

```console
$ docker pull mongo@sha256:1a3468a39b95b542655927d7e0a04353366dc703ded677e6c22451360c87bac9
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6183054924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c053b22eb0ec81f93e0935c743ad67ebefcb1a5799d222cabaf3c11a513caffc`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 01 Jun 2020 18:53:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Jun 2020 12:52:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 17 Jun 2020 00:14:52 GMT
ENV MONGO_VERSION=4.0.19
# Wed, 17 Jun 2020 00:14:53 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-4.0.19-signed.msi
# Wed, 17 Jun 2020 00:14:54 GMT
ENV MONGO_DOWNLOAD_SHA256=fcdadb2d83e21551da2e8302f6cdab69ac840d4b1cca2cb353853c5d81aebac6
# Wed, 17 Jun 2020 00:32:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 17 Jun 2020 00:32:17 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 17 Jun 2020 00:32:18 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 00:32:20 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:375fbabb84945635805b46a02a17ac15a3177bcaae7404cfab5f1ceb0460cb60`  
		Size: 1.7 GB (1664011795 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:30efe9163d37226b077b25cd93b088cebd2ddbaadf173d143b9fe0ddecaeae53`  
		Last Modified: Wed, 10 Jun 2020 15:34:41 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:816499e8d3b97fdb4d8e47ee9d0d1f281a3b1eeb8850ff030523cff88380321e`  
		Last Modified: Wed, 17 Jun 2020 01:29:35 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26a589c682f9703eb3d409e2032c7919de1aefc19a3cb393b0c064eaef6f0be`  
		Last Modified: Wed, 17 Jun 2020 01:29:35 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d73871c04674ed1c797392fe5bec4228f05654ebf5a6a58435036fb1abe2ee`  
		Last Modified: Wed, 17 Jun 2020 01:29:32 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726d3ce65aa1b227ef614b059b137963db5ee0a8bc95a4a730d085a97fe6bc33`  
		Last Modified: Wed, 17 Jun 2020 01:30:29 GMT  
		Size: 449.0 MB (449049166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad0ff8e9f21a3c1e912d9eeeeb97ee2d5c553ee879ec5f5cccd0a184698a8a7`  
		Last Modified: Wed, 17 Jun 2020 01:29:31 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:305f20c2735d1ba169d52da0302e523ab3b2c09d047ff177d330c3b6a1bd6026`  
		Last Modified: Wed, 17 Jun 2020 01:29:32 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78f51b73ffa29728a6caf389cb3cb091a7706b2ea1f1013eeace11097778c12`  
		Last Modified: Wed, 17 Jun 2020 01:29:31 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.0-xenial`

```console
$ docker pull mongo@sha256:bc35602421ae30f947a73d2c7e188840fc2137d5216f68ed63a5671acd988d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `mongo:4.0-xenial` - linux; amd64

```console
$ docker pull mongo@sha256:7e87b7e743c943be2520b0475da0ada3b254e6bf9817a3d1e97777ea575c40b6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.8 MB (153792832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e541b5559917be313d87d6b879d85e429dc6aec5df3b3e4ddc3d150660b9a45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:21:26 GMT
ADD file:52af30f80ba214985a59cb0ef7073c64f8514d58396c0de48f8d7056dec2a58a in / 
# Wed, 17 Jun 2020 01:21:27 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 01:21:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:21:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:21:29 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 05:14:46 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 05:14:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 05:14:55 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 05:14:55 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 05:15:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 05:15:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 05:15:40 GMT
ENV GPG_KEYS=9DA31620334BD75D9DCB49F368818C72E52529D4
# Wed, 17 Jun 2020 05:15:41 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 05:15:41 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 05:15:41 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 05:15:41 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 05:15:41 GMT
ENV MONGO_MAJOR=4.0
# Wed, 17 Jun 2020 05:15:41 GMT
ENV MONGO_VERSION=4.0.19
# Wed, 17 Jun 2020 05:15:42 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 05:15:59 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 05:16:00 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 05:16:00 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 05:16:00 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 05:16:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 05:16:01 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 05:16:01 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:b5e173e44934e01d8d2674bc8b1da00f761c4fe796e0fb2bee1bd1129d2e4ae1`  
		Last Modified: Fri, 15 May 2020 13:20:22 GMT  
		Size: 44.3 MB (44320272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29047100b0407dff554ea80b8005380d62b13a66d7fe2e2adb07b9c091b9f2c0`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 531.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15743a713c2a4033877dab08fb3989280f8c856234227158a4011811c7991372`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6bc9e2987763aa991b7dfd742be04c7b3bb04448982ffe88e58d55c93b76d4`  
		Last Modified: Wed, 17 Jun 2020 01:22:21 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0742b611831efaa04736014a0196f9d038c2f66141cbae2be6191b487207f2`  
		Last Modified: Wed, 17 Jun 2020 05:17:42 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac88a40bfb757f3fd79fee2a4efdc269db4922c6c3e5bdd058b44b94d4b45a9`  
		Last Modified: Wed, 17 Jun 2020 05:17:42 GMT  
		Size: 2.9 MB (2904013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2a2c44348f93f163d89525024baa1ec80c4ea18b092a08ebb545c348e7d270`  
		Last Modified: Wed, 17 Jun 2020 05:17:42 GMT  
		Size: 1.3 MB (1305044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1c4d1da9278aa467bc18ef66e8714710039f1523ac7fe674d1e5713f162e35`  
		Last Modified: Wed, 17 Jun 2020 05:17:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f710eae0da44706cdd69fb6df1b0b3c65539a2359f36e8ad614993f2e60ecff`  
		Last Modified: Wed, 17 Jun 2020 05:18:05 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca24f3ca70c39253780feea5588acd8b8010b7f559515fa6153a547afb370d8f`  
		Last Modified: Wed, 17 Jun 2020 05:18:05 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c5ae9ffe7bc3613be27b4e795c3aba5ac34c39f3ea309373238bb76a28056f3`  
		Last Modified: Wed, 17 Jun 2020 05:18:22 GMT  
		Size: 105.3 MB (105254085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71541f27ccb019a43dae7fcc9929d489102490704b1c79bf4289d6c88c8d2e83`  
		Last Modified: Wed, 17 Jun 2020 05:18:06 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf2098794726bab4c816a3a21cd0ce0434456e797560b578dcd59bac416551f`  
		Last Modified: Wed, 17 Jun 2020 05:18:05 GMT  
		Size: 4.0 KB (3955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.0-xenial` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:2ceebfb3ba9dd87bee897485561b8c7b82065c0281127ab5f4782f38c2481d9c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.4 MB (143363263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cebd15eb77de47468757b975d4a261739eb155ba1e116c7dfe1bfa01bda91a22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:44:20 GMT
ADD file:e359a3b06531f763adba716802e252fa49b2e6126f0d3dae1451fc94f5617a13 in / 
# Wed, 17 Jun 2020 01:44:24 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 01:44:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:44:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:44:29 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:22:26 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 03:22:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:22:45 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:22:45 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 03:23:17 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:23:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:24:39 GMT
ENV GPG_KEYS=9DA31620334BD75D9DCB49F368818C72E52529D4
# Wed, 17 Jun 2020 03:24:42 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:24:43 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 03:24:44 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:24:45 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:24:46 GMT
ENV MONGO_MAJOR=4.0
# Wed, 17 Jun 2020 03:24:47 GMT
ENV MONGO_VERSION=4.0.19
# Wed, 17 Jun 2020 03:24:49 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu xenial/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 03:25:33 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 03:25:36 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 03:25:38 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 03:25:39 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:25:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:25:41 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 03:25:43 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:13340090a20bfb81868e7119dc439546fe30dcfccce42509f0fb4d998a1d1fee`  
		Last Modified: Fri, 15 May 2020 16:25:35 GMT  
		Size: 40.0 MB (40003935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75eea8c54eb3d5e45521f4ba5c57ede8436f58690cb8a37da90cfcda5efc25f7`  
		Last Modified: Wed, 17 Jun 2020 01:45:48 GMT  
		Size: 470.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857f69e728f2821d6dce88bd1c73ebda9481628a80b563e677ec423b08fdba87`  
		Last Modified: Wed, 17 Jun 2020 01:45:48 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8b20459bfc0dfbc19d643cff0a457a117336e167bb8051554fb88aee48feff`  
		Last Modified: Wed, 17 Jun 2020 01:45:48 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270afc1f069e440415e7f2ce6ea17182e6af8d92e4c8f67842fc4f54413d3b2e`  
		Last Modified: Wed, 17 Jun 2020 03:30:03 GMT  
		Size: 2.0 KB (1992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aca9f74e6ca082c5da190f0f58ac30d4822b0ffd568394e5ffec26bb1fd6a07`  
		Last Modified: Wed, 17 Jun 2020 03:30:02 GMT  
		Size: 2.4 MB (2431869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f567c330a76a757a4b3ad26abdef55c652ebb1e0e70b77b935d3afe42d59a499`  
		Last Modified: Wed, 17 Jun 2020 03:30:03 GMT  
		Size: 1.2 MB (1232045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8e0ba58951fc1e9fa054b24cbd1cdab213c985e279cc76f8bf95465d62c50c`  
		Last Modified: Wed, 17 Jun 2020 03:30:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c1fdd5271b26ffe0d62b29b25121931dcdbe6ebb7ea49ba6b24fd99e266112a`  
		Last Modified: Wed, 17 Jun 2020 03:30:36 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd7739bdf8cd161542061f5bc73b8a6756dd8a561f9b8209a6d091aa4fcc503`  
		Last Modified: Wed, 17 Jun 2020 03:30:36 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac0483829d143872abb4f5eb93398b84d81da48055989fac0d4a17d73360ee5b`  
		Last Modified: Wed, 17 Jun 2020 03:31:01 GMT  
		Size: 99.7 MB (99685983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbaee99aa1bb5266c3f49a40599712f23081844d6f9f1242a95e952fc787ed19`  
		Last Modified: Wed, 17 Jun 2020 03:30:36 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6839344713a90022b7a568a420d74d75dab8bc2e7bf09a66fdb6c56ce063795e`  
		Last Modified: Wed, 17 Jun 2020 03:30:36 GMT  
		Size: 4.0 KB (3956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.2`

```console
$ docker pull mongo@sha256:29805e9a6fc2a233b9b633c7b0f382a43df3f119522b82366a72abecb302a793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x
	-	windows version 10.0.14393.3750; amd64
	-	windows version 10.0.17763.1282; amd64

### `mongo:4.2` - linux; amd64

```console
$ docker pull mongo@sha256:ed04fcf28fccf1bb2c295074775a24ddd007e14ca522ae97a56983f269cad163
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164652387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2cc1f48aed02a160b0447fd28b75952ed1d2df8c66693733d4954483734e44`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:20:29 GMT
ADD file:1e8d02626176dc8141df3c0a1365774ce73d79934654fe24a4b1e7f173108232 in / 
# Wed, 17 Jun 2020 01:20:30 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:20:31 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:20:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:20:32 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 05:16:06 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 05:16:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 05:16:16 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 05:16:16 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 05:16:30 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 05:16:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 05:16:33 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Wed, 17 Jun 2020 05:16:34 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 05:16:34 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 05:16:34 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 05:16:34 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 05:16:34 GMT
ENV MONGO_MAJOR=4.2
# Wed, 17 Jun 2020 05:16:35 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 17 Jun 2020 05:16:35 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 05:16:53 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 05:16:54 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 05:16:54 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 05:16:54 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 05:16:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 05:16:55 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 05:16:55 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:d7c3167c320d7a820935f54cf4290890ea19567da496ecf774e8773b35d5f065`  
		Last Modified: Wed, 27 May 2020 12:21:15 GMT  
		Size: 26.7 MB (26688718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:131f805ec7fd68d45a887e2ef82de61de0247b4eb934ab03b7c933650e854baa`  
		Last Modified: Wed, 17 Jun 2020 01:21:41 GMT  
		Size: 35.4 KB (35369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322ed380e680a77f30528ba013e3a802a7b44948a0609c7d1d732dd46a9a310d`  
		Last Modified: Wed, 17 Jun 2020 01:21:41 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac240b130982ad1c3ba3188abbf18ba4e54bdd9e504ce2d5c2eff6d3e86b8dd`  
		Last Modified: Wed, 17 Jun 2020 01:21:41 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5704a01b59ff4d100b5bcc0244090cb5b369649b41a468a82cb5015afdc4f9d`  
		Last Modified: Wed, 17 Jun 2020 05:18:30 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e396e2a1e6820b238c82087b900e4f03e1304b30ee16a5341b0c6a2a9eec20e`  
		Last Modified: Wed, 17 Jun 2020 05:18:29 GMT  
		Size: 3.0 MB (2973543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:914fffcb1cc543f9e16861fe6d80fdaad26ea9c69ba952c73cb3db44a9cfc545`  
		Last Modified: Wed, 17 Jun 2020 05:18:30 GMT  
		Size: 5.8 MB (5823974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692bd0d35810fbf133d67af4f0ae0c627fb731b875d5370d3dfaa3f1a06392fa`  
		Last Modified: Wed, 17 Jun 2020 05:18:29 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122d231765e47cbdd1b934b3ee55ffa291b76b17e4134be5b6e9837c52053c9e`  
		Last Modified: Wed, 17 Jun 2020 05:18:28 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9c497305ce2ee80e9d80fb69dcf2766f51b6b23e093fbf9d0d837b14376810`  
		Last Modified: Wed, 17 Jun 2020 05:18:28 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e3ca7a65fcd8d5d002ae04e06a5d7b900020097dec64e04923b9fa25d7d633`  
		Last Modified: Wed, 17 Jun 2020 05:18:46 GMT  
		Size: 129.1 MB (129122023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70e0d9672b4cbcef6ddbaa3fae90fb8181aeb83b59cac8f4910d69f7c359f96`  
		Last Modified: Wed, 17 Jun 2020 05:18:28 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc04aade5db18c8ca826bfaef542aa9b48f2b3045dfe7a4fa0d4f11714d37a1`  
		Last Modified: Wed, 17 Jun 2020 05:18:28 GMT  
		Size: 4.0 KB (3955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:cdec0bd28e60bc06892f9972803753d57fdc3d4bcff657b694ba7f35b80d3d02
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154677642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f84af28ce3aa3b7b04964d7f7ee9eb0ae10e3c19e684ad29ceeca55c605f2924`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:42:33 GMT
ADD file:7dc8819fd3d4b84ad19fb836e5bfda64a5ffefc371166f70d4d41dff6b22d450 in / 
# Wed, 17 Jun 2020 01:42:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:42:41 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:42:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:42:45 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:26:00 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 03:26:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:26:24 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:26:25 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 03:27:01 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:27:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:27:06 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Wed, 17 Jun 2020 03:27:10 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:27:12 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 03:27:13 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:27:16 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:27:19 GMT
ENV MONGO_MAJOR=4.2
# Wed, 17 Jun 2020 03:27:20 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 17 Jun 2020 03:27:23 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 03:27:58 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 03:28:02 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 03:28:04 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 03:28:05 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:28:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:28:08 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 03:28:09 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:2e8bea8b22f8f5a4fd5aa85019945dd8ae04f283a4ba2a7aeb4536fe2f1d1ec2`  
		Last Modified: Tue, 26 May 2020 16:25:25 GMT  
		Size: 23.7 MB (23721687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc90876b9c9a7343ae432eaec7c8dc8859c1e84b6193da8d386815fde165a70e`  
		Last Modified: Wed, 17 Jun 2020 01:44:48 GMT  
		Size: 35.2 KB (35192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bfc658a5210a9f0c9cfcda5f504e720da9268e9f3f3bf48e3a9a7af360c959`  
		Last Modified: Wed, 17 Jun 2020 01:44:49 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef0f1b06b2142ff2bf35cc565f019ed9e4efe0d8f332825167538c2337bac8a`  
		Last Modified: Wed, 17 Jun 2020 01:44:49 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79f4068e2fc9c5ce913c3640637c35584b72816ca9485c4bf5af0a22994d0f6`  
		Last Modified: Wed, 17 Jun 2020 03:31:11 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5678c55b212ca2ce4ea7b4092838653b706277000f57d7a18526f3df6cba283`  
		Last Modified: Wed, 17 Jun 2020 03:31:11 GMT  
		Size: 2.7 MB (2665976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509de0ccfb79a34de230a6fef2cfc900bdb35f1f7f583fc957b7c23b46439d4f`  
		Last Modified: Wed, 17 Jun 2020 03:31:12 GMT  
		Size: 5.3 MB (5345550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5493b54160873a149e08eedf09e74628680b1d5e8826b90672f04c88c30ccb`  
		Last Modified: Wed, 17 Jun 2020 03:31:10 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe2b58fe1082de604f779b26f7bac0f685326b5584f5a43457f1d51effdca86`  
		Last Modified: Wed, 17 Jun 2020 03:31:09 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52cb618aa3e851b5a35792b706fd4e70901c2e3fd1faa3fcf12d719ac3d8ff1`  
		Last Modified: Wed, 17 Jun 2020 03:31:08 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8985f89f29dd85eccbd8da50a080817fa846f7b7baee89e54e83f79559fff4b`  
		Last Modified: Wed, 17 Jun 2020 03:31:35 GMT  
		Size: 122.9 MB (122900361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f01ca57315b3f1a9469f85034d0f072b2d67b5ee9d3c9d2e14e3487df4db4d`  
		Last Modified: Wed, 17 Jun 2020 03:31:08 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f414fc1b8d9a096289a531b03096d4af7478a1c627842175a15974cb041c879`  
		Last Modified: Wed, 17 Jun 2020 03:31:08 GMT  
		Size: 4.0 KB (3950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2` - linux; s390x

```console
$ docker pull mongo@sha256:e1c13c3ee8ae7031fdaa1e4cb645de3279a46ccf47511a9fb4b82c90d5c831f5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160598470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddfb01efb7ddfe0ac3ea40d0ded51ac1742d89e522b72b9ca43ec82ac2a642b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:41:48 GMT
ADD file:8708e93980b416070ba0bb024a7858748129059a85d2c771a4489c31710a9df1 in / 
# Wed, 17 Jun 2020 01:41:51 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:41:52 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:41:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:41:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:24:26 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 03:24:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:24:35 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:24:35 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 03:24:46 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:24:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:24:47 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Wed, 17 Jun 2020 03:24:48 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:24:48 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 03:24:48 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:24:48 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:24:48 GMT
ENV MONGO_MAJOR=4.2
# Wed, 17 Jun 2020 03:24:49 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 17 Jun 2020 03:24:49 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 03:25:14 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 03:25:18 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 03:25:18 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 03:25:19 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:25:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:25:19 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 03:25:19 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f3c26641772baa3348c0cce190edb38690a41f1824570c5c65cc363b42e5a5b5`  
		Last Modified: Sat, 30 May 2020 09:30:29 GMT  
		Size: 25.4 MB (25365846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf76fcee55454304ffbf9e321dda388a7e8de8a3916f854e1e588bc6c19b088`  
		Last Modified: Wed, 17 Jun 2020 01:42:56 GMT  
		Size: 36.2 KB (36165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5173e4f9f1868daa26021e1e701a000b0aadb2b611a487d089e7de4b728a7424`  
		Last Modified: Wed, 17 Jun 2020 01:42:56 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13da9fe451bd0f377d042d4bebef4ffd19163113e3e66dcd718fe187149a0dbd`  
		Last Modified: Wed, 17 Jun 2020 01:42:57 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d8fc9b1e9007ca5666c42ff8398a5227869b151fea1562c5e3cfb2188640e6`  
		Last Modified: Wed, 17 Jun 2020 03:28:52 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a889c8302a90f8884ff21edb649cf8dc1771453aca39505e61f29e053a1b64`  
		Last Modified: Wed, 17 Jun 2020 03:28:51 GMT  
		Size: 2.7 MB (2704483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:582fe8ee181790ce5fdadeef1c1cd7af40de0e8d2cb2e307fa05aed8d23a82b7`  
		Last Modified: Wed, 17 Jun 2020 03:28:50 GMT  
		Size: 5.7 MB (5745080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6096f1fa9fe7ad82ea015203f2410ac8b0831d0617db029aed54c698f84a2eaf`  
		Last Modified: Wed, 17 Jun 2020 03:28:50 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2bddaa2c78c2b5ac010b9af305db894e7bb616461499b863fe6af05c42bb502`  
		Last Modified: Wed, 17 Jun 2020 03:28:48 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b0ea0902452b7fe6fc59cc6001683eb80ddf80ba9fa1a59f83a576855317e12`  
		Last Modified: Wed, 17 Jun 2020 03:28:48 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507e67f4e596fea4d40f10e6ca9132a57d472a59bef2ce47ae79b92eb029ca7a`  
		Last Modified: Wed, 17 Jun 2020 03:29:02 GMT  
		Size: 126.7 MB (126738040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf93b294dbde6159d09390ee7231284abcaad59049a9d10eaebfc46619d4ad3`  
		Last Modified: Wed, 17 Jun 2020 03:28:48 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e514b21a3b45674ce414ecd79bf6adc339e8ea02fc1a80956ece983f3192be`  
		Last Modified: Wed, 17 Jun 2020 03:29:03 GMT  
		Size: 4.0 KB (3953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2` - windows version 10.0.14393.3750; amd64

```console
$ docker pull mongo@sha256:af38590235375eb1218ddd651e660f1a6e6e6a882842e7b428f2d55d46cc937a
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6193023222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aaf2b53fe9e096da5ab6f4ae0e34caf7cf3de0a336bd9576cee60752c37c17b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 01 Jun 2020 18:53:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Jun 2020 12:52:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 17 Jun 2020 00:50:43 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 17 Jun 2020 00:50:44 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 17 Jun 2020 00:50:45 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 17 Jun 2020 01:08:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 17 Jun 2020 01:08:52 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 17 Jun 2020 01:08:53 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 01:08:54 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:375fbabb84945635805b46a02a17ac15a3177bcaae7404cfab5f1ceb0460cb60`  
		Size: 1.7 GB (1664011795 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:30efe9163d37226b077b25cd93b088cebd2ddbaadf173d143b9fe0ddecaeae53`  
		Last Modified: Wed, 10 Jun 2020 15:34:41 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b60479ef88c8a931aeeffaa74d289fbbf204229adb6a20c54d51456f70bb75`  
		Last Modified: Wed, 17 Jun 2020 01:32:04 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52bb592e6eb6512ccf1127b0311263697d559599357972414f4b776277bd628f`  
		Last Modified: Wed, 17 Jun 2020 01:32:04 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e57b55cda98f10b8c536232f9fd5fbc19c778c4043edc4fea012972832bb4570`  
		Last Modified: Wed, 17 Jun 2020 01:32:01 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eaad7a52f6dc4a311c3e724f9b5fe27f7af849fa6229fe21fc0490976fcb607`  
		Last Modified: Wed, 17 Jun 2020 01:32:57 GMT  
		Size: 459.0 MB (459017760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187b8e518ef05e3f4e7348e0ca7fef3e05414c63661223d63d83a36367ff9605`  
		Last Modified: Wed, 17 Jun 2020 01:32:01 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58773855217e4f81876fd21fd13a61d94d0f5a191e7025ce2bf26469077e330c`  
		Last Modified: Wed, 17 Jun 2020 01:32:01 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e25f1762a4dcad6fd6709c2602e0d459a0efb6aea6e10e16cb78796c27e496d`  
		Last Modified: Wed, 17 Jun 2020 01:32:01 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2` - windows version 10.0.17763.1282; amd64

```console
$ docker pull mongo@sha256:a332d0d55bcb861ab664609d4ee8b7a3c7481e800fa5ad62009c671c1673af0b
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2752054828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86c12ab59b3d8850d880c02f06724769d7955a42bb4c5b10fd9a16cb6ad19f7`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Wed, 10 Jun 2020 12:43:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 17 Jun 2020 01:09:02 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 17 Jun 2020 01:09:03 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 17 Jun 2020 01:09:04 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 17 Jun 2020 01:28:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 17 Jun 2020 01:28:16 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 17 Jun 2020 01:28:18 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 01:28:19 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b11029314f3c794dc51e43c915b3e62f6b44aeb96f84b8b92f453e61cf7a2cb3`  
		Last Modified: Wed, 10 Jun 2020 15:34:12 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f51df57f2cb6ccc03b57cbd044ee4a49d9383489feb3872da465ba8b6bffa89`  
		Last Modified: Wed, 17 Jun 2020 01:33:19 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84353c49610a99480bfb74a8769e7446bbd898b8644c25d2b8c645c7a2e90e0e`  
		Last Modified: Wed, 17 Jun 2020 01:33:18 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c19d206596ed0cd1b7da30ba6e637be1d4c31dc398ca6f4d30d583593e31705`  
		Last Modified: Wed, 17 Jun 2020 01:33:16 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90fa0f2b93199d15d0678aa8a13db7d1470a5ce7ddb94ec8fa93a75156cce44`  
		Last Modified: Wed, 17 Jun 2020 01:34:14 GMT  
		Size: 458.1 MB (458132610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:369180762b76f75c56ed85ad59e938011c514ad32b51a43cbb6d5fcce885b5d1`  
		Last Modified: Wed, 17 Jun 2020 01:33:16 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f9c110c11f811446f2204714562c02b6eefeeb1cae671aa73af5e4cc7dfbd0`  
		Last Modified: Wed, 17 Jun 2020 01:33:16 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c7a275e52c9eafb08caf7a861ef21a725b77ee54c1b867ddb4b4da99814dd7`  
		Last Modified: Wed, 17 Jun 2020 01:33:16 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.2.8`

```console
$ docker pull mongo@sha256:29805e9a6fc2a233b9b633c7b0f382a43df3f119522b82366a72abecb302a793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x
	-	windows version 10.0.14393.3750; amd64
	-	windows version 10.0.17763.1282; amd64

### `mongo:4.2.8` - linux; amd64

```console
$ docker pull mongo@sha256:ed04fcf28fccf1bb2c295074775a24ddd007e14ca522ae97a56983f269cad163
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164652387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2cc1f48aed02a160b0447fd28b75952ed1d2df8c66693733d4954483734e44`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:20:29 GMT
ADD file:1e8d02626176dc8141df3c0a1365774ce73d79934654fe24a4b1e7f173108232 in / 
# Wed, 17 Jun 2020 01:20:30 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:20:31 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:20:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:20:32 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 05:16:06 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 05:16:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 05:16:16 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 05:16:16 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 05:16:30 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 05:16:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 05:16:33 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Wed, 17 Jun 2020 05:16:34 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 05:16:34 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 05:16:34 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 05:16:34 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 05:16:34 GMT
ENV MONGO_MAJOR=4.2
# Wed, 17 Jun 2020 05:16:35 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 17 Jun 2020 05:16:35 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 05:16:53 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 05:16:54 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 05:16:54 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 05:16:54 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 05:16:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 05:16:55 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 05:16:55 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:d7c3167c320d7a820935f54cf4290890ea19567da496ecf774e8773b35d5f065`  
		Last Modified: Wed, 27 May 2020 12:21:15 GMT  
		Size: 26.7 MB (26688718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:131f805ec7fd68d45a887e2ef82de61de0247b4eb934ab03b7c933650e854baa`  
		Last Modified: Wed, 17 Jun 2020 01:21:41 GMT  
		Size: 35.4 KB (35369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322ed380e680a77f30528ba013e3a802a7b44948a0609c7d1d732dd46a9a310d`  
		Last Modified: Wed, 17 Jun 2020 01:21:41 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac240b130982ad1c3ba3188abbf18ba4e54bdd9e504ce2d5c2eff6d3e86b8dd`  
		Last Modified: Wed, 17 Jun 2020 01:21:41 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5704a01b59ff4d100b5bcc0244090cb5b369649b41a468a82cb5015afdc4f9d`  
		Last Modified: Wed, 17 Jun 2020 05:18:30 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e396e2a1e6820b238c82087b900e4f03e1304b30ee16a5341b0c6a2a9eec20e`  
		Last Modified: Wed, 17 Jun 2020 05:18:29 GMT  
		Size: 3.0 MB (2973543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:914fffcb1cc543f9e16861fe6d80fdaad26ea9c69ba952c73cb3db44a9cfc545`  
		Last Modified: Wed, 17 Jun 2020 05:18:30 GMT  
		Size: 5.8 MB (5823974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692bd0d35810fbf133d67af4f0ae0c627fb731b875d5370d3dfaa3f1a06392fa`  
		Last Modified: Wed, 17 Jun 2020 05:18:29 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122d231765e47cbdd1b934b3ee55ffa291b76b17e4134be5b6e9837c52053c9e`  
		Last Modified: Wed, 17 Jun 2020 05:18:28 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9c497305ce2ee80e9d80fb69dcf2766f51b6b23e093fbf9d0d837b14376810`  
		Last Modified: Wed, 17 Jun 2020 05:18:28 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e3ca7a65fcd8d5d002ae04e06a5d7b900020097dec64e04923b9fa25d7d633`  
		Last Modified: Wed, 17 Jun 2020 05:18:46 GMT  
		Size: 129.1 MB (129122023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70e0d9672b4cbcef6ddbaa3fae90fb8181aeb83b59cac8f4910d69f7c359f96`  
		Last Modified: Wed, 17 Jun 2020 05:18:28 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc04aade5db18c8ca826bfaef542aa9b48f2b3045dfe7a4fa0d4f11714d37a1`  
		Last Modified: Wed, 17 Jun 2020 05:18:28 GMT  
		Size: 4.0 KB (3955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2.8` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:cdec0bd28e60bc06892f9972803753d57fdc3d4bcff657b694ba7f35b80d3d02
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154677642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f84af28ce3aa3b7b04964d7f7ee9eb0ae10e3c19e684ad29ceeca55c605f2924`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:42:33 GMT
ADD file:7dc8819fd3d4b84ad19fb836e5bfda64a5ffefc371166f70d4d41dff6b22d450 in / 
# Wed, 17 Jun 2020 01:42:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:42:41 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:42:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:42:45 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:26:00 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 03:26:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:26:24 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:26:25 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 03:27:01 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:27:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:27:06 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Wed, 17 Jun 2020 03:27:10 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:27:12 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 03:27:13 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:27:16 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:27:19 GMT
ENV MONGO_MAJOR=4.2
# Wed, 17 Jun 2020 03:27:20 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 17 Jun 2020 03:27:23 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 03:27:58 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 03:28:02 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 03:28:04 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 03:28:05 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:28:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:28:08 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 03:28:09 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:2e8bea8b22f8f5a4fd5aa85019945dd8ae04f283a4ba2a7aeb4536fe2f1d1ec2`  
		Last Modified: Tue, 26 May 2020 16:25:25 GMT  
		Size: 23.7 MB (23721687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc90876b9c9a7343ae432eaec7c8dc8859c1e84b6193da8d386815fde165a70e`  
		Last Modified: Wed, 17 Jun 2020 01:44:48 GMT  
		Size: 35.2 KB (35192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bfc658a5210a9f0c9cfcda5f504e720da9268e9f3f3bf48e3a9a7af360c959`  
		Last Modified: Wed, 17 Jun 2020 01:44:49 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef0f1b06b2142ff2bf35cc565f019ed9e4efe0d8f332825167538c2337bac8a`  
		Last Modified: Wed, 17 Jun 2020 01:44:49 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79f4068e2fc9c5ce913c3640637c35584b72816ca9485c4bf5af0a22994d0f6`  
		Last Modified: Wed, 17 Jun 2020 03:31:11 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5678c55b212ca2ce4ea7b4092838653b706277000f57d7a18526f3df6cba283`  
		Last Modified: Wed, 17 Jun 2020 03:31:11 GMT  
		Size: 2.7 MB (2665976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509de0ccfb79a34de230a6fef2cfc900bdb35f1f7f583fc957b7c23b46439d4f`  
		Last Modified: Wed, 17 Jun 2020 03:31:12 GMT  
		Size: 5.3 MB (5345550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5493b54160873a149e08eedf09e74628680b1d5e8826b90672f04c88c30ccb`  
		Last Modified: Wed, 17 Jun 2020 03:31:10 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe2b58fe1082de604f779b26f7bac0f685326b5584f5a43457f1d51effdca86`  
		Last Modified: Wed, 17 Jun 2020 03:31:09 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52cb618aa3e851b5a35792b706fd4e70901c2e3fd1faa3fcf12d719ac3d8ff1`  
		Last Modified: Wed, 17 Jun 2020 03:31:08 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8985f89f29dd85eccbd8da50a080817fa846f7b7baee89e54e83f79559fff4b`  
		Last Modified: Wed, 17 Jun 2020 03:31:35 GMT  
		Size: 122.9 MB (122900361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f01ca57315b3f1a9469f85034d0f072b2d67b5ee9d3c9d2e14e3487df4db4d`  
		Last Modified: Wed, 17 Jun 2020 03:31:08 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f414fc1b8d9a096289a531b03096d4af7478a1c627842175a15974cb041c879`  
		Last Modified: Wed, 17 Jun 2020 03:31:08 GMT  
		Size: 4.0 KB (3950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2.8` - linux; s390x

```console
$ docker pull mongo@sha256:e1c13c3ee8ae7031fdaa1e4cb645de3279a46ccf47511a9fb4b82c90d5c831f5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160598470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddfb01efb7ddfe0ac3ea40d0ded51ac1742d89e522b72b9ca43ec82ac2a642b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:41:48 GMT
ADD file:8708e93980b416070ba0bb024a7858748129059a85d2c771a4489c31710a9df1 in / 
# Wed, 17 Jun 2020 01:41:51 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:41:52 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:41:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:41:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:24:26 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 03:24:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:24:35 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:24:35 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 03:24:46 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:24:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:24:47 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Wed, 17 Jun 2020 03:24:48 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:24:48 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 03:24:48 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:24:48 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:24:48 GMT
ENV MONGO_MAJOR=4.2
# Wed, 17 Jun 2020 03:24:49 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 17 Jun 2020 03:24:49 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 03:25:14 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 03:25:18 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 03:25:18 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 03:25:19 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:25:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:25:19 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 03:25:19 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f3c26641772baa3348c0cce190edb38690a41f1824570c5c65cc363b42e5a5b5`  
		Last Modified: Sat, 30 May 2020 09:30:29 GMT  
		Size: 25.4 MB (25365846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf76fcee55454304ffbf9e321dda388a7e8de8a3916f854e1e588bc6c19b088`  
		Last Modified: Wed, 17 Jun 2020 01:42:56 GMT  
		Size: 36.2 KB (36165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5173e4f9f1868daa26021e1e701a000b0aadb2b611a487d089e7de4b728a7424`  
		Last Modified: Wed, 17 Jun 2020 01:42:56 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13da9fe451bd0f377d042d4bebef4ffd19163113e3e66dcd718fe187149a0dbd`  
		Last Modified: Wed, 17 Jun 2020 01:42:57 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d8fc9b1e9007ca5666c42ff8398a5227869b151fea1562c5e3cfb2188640e6`  
		Last Modified: Wed, 17 Jun 2020 03:28:52 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a889c8302a90f8884ff21edb649cf8dc1771453aca39505e61f29e053a1b64`  
		Last Modified: Wed, 17 Jun 2020 03:28:51 GMT  
		Size: 2.7 MB (2704483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:582fe8ee181790ce5fdadeef1c1cd7af40de0e8d2cb2e307fa05aed8d23a82b7`  
		Last Modified: Wed, 17 Jun 2020 03:28:50 GMT  
		Size: 5.7 MB (5745080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6096f1fa9fe7ad82ea015203f2410ac8b0831d0617db029aed54c698f84a2eaf`  
		Last Modified: Wed, 17 Jun 2020 03:28:50 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2bddaa2c78c2b5ac010b9af305db894e7bb616461499b863fe6af05c42bb502`  
		Last Modified: Wed, 17 Jun 2020 03:28:48 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b0ea0902452b7fe6fc59cc6001683eb80ddf80ba9fa1a59f83a576855317e12`  
		Last Modified: Wed, 17 Jun 2020 03:28:48 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507e67f4e596fea4d40f10e6ca9132a57d472a59bef2ce47ae79b92eb029ca7a`  
		Last Modified: Wed, 17 Jun 2020 03:29:02 GMT  
		Size: 126.7 MB (126738040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf93b294dbde6159d09390ee7231284abcaad59049a9d10eaebfc46619d4ad3`  
		Last Modified: Wed, 17 Jun 2020 03:28:48 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e514b21a3b45674ce414ecd79bf6adc339e8ea02fc1a80956ece983f3192be`  
		Last Modified: Wed, 17 Jun 2020 03:29:03 GMT  
		Size: 4.0 KB (3953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2.8` - windows version 10.0.14393.3750; amd64

```console
$ docker pull mongo@sha256:af38590235375eb1218ddd651e660f1a6e6e6a882842e7b428f2d55d46cc937a
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6193023222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aaf2b53fe9e096da5ab6f4ae0e34caf7cf3de0a336bd9576cee60752c37c17b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 01 Jun 2020 18:53:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Jun 2020 12:52:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 17 Jun 2020 00:50:43 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 17 Jun 2020 00:50:44 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 17 Jun 2020 00:50:45 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 17 Jun 2020 01:08:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 17 Jun 2020 01:08:52 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 17 Jun 2020 01:08:53 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 01:08:54 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:375fbabb84945635805b46a02a17ac15a3177bcaae7404cfab5f1ceb0460cb60`  
		Size: 1.7 GB (1664011795 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:30efe9163d37226b077b25cd93b088cebd2ddbaadf173d143b9fe0ddecaeae53`  
		Last Modified: Wed, 10 Jun 2020 15:34:41 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b60479ef88c8a931aeeffaa74d289fbbf204229adb6a20c54d51456f70bb75`  
		Last Modified: Wed, 17 Jun 2020 01:32:04 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52bb592e6eb6512ccf1127b0311263697d559599357972414f4b776277bd628f`  
		Last Modified: Wed, 17 Jun 2020 01:32:04 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e57b55cda98f10b8c536232f9fd5fbc19c778c4043edc4fea012972832bb4570`  
		Last Modified: Wed, 17 Jun 2020 01:32:01 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eaad7a52f6dc4a311c3e724f9b5fe27f7af849fa6229fe21fc0490976fcb607`  
		Last Modified: Wed, 17 Jun 2020 01:32:57 GMT  
		Size: 459.0 MB (459017760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187b8e518ef05e3f4e7348e0ca7fef3e05414c63661223d63d83a36367ff9605`  
		Last Modified: Wed, 17 Jun 2020 01:32:01 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58773855217e4f81876fd21fd13a61d94d0f5a191e7025ce2bf26469077e330c`  
		Last Modified: Wed, 17 Jun 2020 01:32:01 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e25f1762a4dcad6fd6709c2602e0d459a0efb6aea6e10e16cb78796c27e496d`  
		Last Modified: Wed, 17 Jun 2020 01:32:01 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2.8` - windows version 10.0.17763.1282; amd64

```console
$ docker pull mongo@sha256:a332d0d55bcb861ab664609d4ee8b7a3c7481e800fa5ad62009c671c1673af0b
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2752054828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86c12ab59b3d8850d880c02f06724769d7955a42bb4c5b10fd9a16cb6ad19f7`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Wed, 10 Jun 2020 12:43:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 17 Jun 2020 01:09:02 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 17 Jun 2020 01:09:03 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 17 Jun 2020 01:09:04 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 17 Jun 2020 01:28:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 17 Jun 2020 01:28:16 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 17 Jun 2020 01:28:18 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 01:28:19 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b11029314f3c794dc51e43c915b3e62f6b44aeb96f84b8b92f453e61cf7a2cb3`  
		Last Modified: Wed, 10 Jun 2020 15:34:12 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f51df57f2cb6ccc03b57cbd044ee4a49d9383489feb3872da465ba8b6bffa89`  
		Last Modified: Wed, 17 Jun 2020 01:33:19 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84353c49610a99480bfb74a8769e7446bbd898b8644c25d2b8c645c7a2e90e0e`  
		Last Modified: Wed, 17 Jun 2020 01:33:18 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c19d206596ed0cd1b7da30ba6e637be1d4c31dc398ca6f4d30d583593e31705`  
		Last Modified: Wed, 17 Jun 2020 01:33:16 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90fa0f2b93199d15d0678aa8a13db7d1470a5ce7ddb94ec8fa93a75156cce44`  
		Last Modified: Wed, 17 Jun 2020 01:34:14 GMT  
		Size: 458.1 MB (458132610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:369180762b76f75c56ed85ad59e938011c514ad32b51a43cbb6d5fcce885b5d1`  
		Last Modified: Wed, 17 Jun 2020 01:33:16 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f9c110c11f811446f2204714562c02b6eefeeb1cae671aa73af5e4cc7dfbd0`  
		Last Modified: Wed, 17 Jun 2020 01:33:16 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c7a275e52c9eafb08caf7a861ef21a725b77ee54c1b867ddb4b4da99814dd7`  
		Last Modified: Wed, 17 Jun 2020 01:33:16 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.2.8-bionic`

```console
$ docker pull mongo@sha256:6bf46291247789c85932f35b2e824158e0f04771fb551aea10e3e7e86c349326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `mongo:4.2.8-bionic` - linux; amd64

```console
$ docker pull mongo@sha256:ed04fcf28fccf1bb2c295074775a24ddd007e14ca522ae97a56983f269cad163
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164652387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2cc1f48aed02a160b0447fd28b75952ed1d2df8c66693733d4954483734e44`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:20:29 GMT
ADD file:1e8d02626176dc8141df3c0a1365774ce73d79934654fe24a4b1e7f173108232 in / 
# Wed, 17 Jun 2020 01:20:30 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:20:31 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:20:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:20:32 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 05:16:06 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 05:16:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 05:16:16 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 05:16:16 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 05:16:30 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 05:16:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 05:16:33 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Wed, 17 Jun 2020 05:16:34 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 05:16:34 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 05:16:34 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 05:16:34 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 05:16:34 GMT
ENV MONGO_MAJOR=4.2
# Wed, 17 Jun 2020 05:16:35 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 17 Jun 2020 05:16:35 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 05:16:53 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 05:16:54 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 05:16:54 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 05:16:54 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 05:16:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 05:16:55 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 05:16:55 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:d7c3167c320d7a820935f54cf4290890ea19567da496ecf774e8773b35d5f065`  
		Last Modified: Wed, 27 May 2020 12:21:15 GMT  
		Size: 26.7 MB (26688718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:131f805ec7fd68d45a887e2ef82de61de0247b4eb934ab03b7c933650e854baa`  
		Last Modified: Wed, 17 Jun 2020 01:21:41 GMT  
		Size: 35.4 KB (35369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322ed380e680a77f30528ba013e3a802a7b44948a0609c7d1d732dd46a9a310d`  
		Last Modified: Wed, 17 Jun 2020 01:21:41 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac240b130982ad1c3ba3188abbf18ba4e54bdd9e504ce2d5c2eff6d3e86b8dd`  
		Last Modified: Wed, 17 Jun 2020 01:21:41 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5704a01b59ff4d100b5bcc0244090cb5b369649b41a468a82cb5015afdc4f9d`  
		Last Modified: Wed, 17 Jun 2020 05:18:30 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e396e2a1e6820b238c82087b900e4f03e1304b30ee16a5341b0c6a2a9eec20e`  
		Last Modified: Wed, 17 Jun 2020 05:18:29 GMT  
		Size: 3.0 MB (2973543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:914fffcb1cc543f9e16861fe6d80fdaad26ea9c69ba952c73cb3db44a9cfc545`  
		Last Modified: Wed, 17 Jun 2020 05:18:30 GMT  
		Size: 5.8 MB (5823974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692bd0d35810fbf133d67af4f0ae0c627fb731b875d5370d3dfaa3f1a06392fa`  
		Last Modified: Wed, 17 Jun 2020 05:18:29 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122d231765e47cbdd1b934b3ee55ffa291b76b17e4134be5b6e9837c52053c9e`  
		Last Modified: Wed, 17 Jun 2020 05:18:28 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9c497305ce2ee80e9d80fb69dcf2766f51b6b23e093fbf9d0d837b14376810`  
		Last Modified: Wed, 17 Jun 2020 05:18:28 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e3ca7a65fcd8d5d002ae04e06a5d7b900020097dec64e04923b9fa25d7d633`  
		Last Modified: Wed, 17 Jun 2020 05:18:46 GMT  
		Size: 129.1 MB (129122023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70e0d9672b4cbcef6ddbaa3fae90fb8181aeb83b59cac8f4910d69f7c359f96`  
		Last Modified: Wed, 17 Jun 2020 05:18:28 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc04aade5db18c8ca826bfaef542aa9b48f2b3045dfe7a4fa0d4f11714d37a1`  
		Last Modified: Wed, 17 Jun 2020 05:18:28 GMT  
		Size: 4.0 KB (3955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2.8-bionic` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:cdec0bd28e60bc06892f9972803753d57fdc3d4bcff657b694ba7f35b80d3d02
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154677642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f84af28ce3aa3b7b04964d7f7ee9eb0ae10e3c19e684ad29ceeca55c605f2924`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:42:33 GMT
ADD file:7dc8819fd3d4b84ad19fb836e5bfda64a5ffefc371166f70d4d41dff6b22d450 in / 
# Wed, 17 Jun 2020 01:42:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:42:41 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:42:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:42:45 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:26:00 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 03:26:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:26:24 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:26:25 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 03:27:01 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:27:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:27:06 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Wed, 17 Jun 2020 03:27:10 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:27:12 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 03:27:13 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:27:16 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:27:19 GMT
ENV MONGO_MAJOR=4.2
# Wed, 17 Jun 2020 03:27:20 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 17 Jun 2020 03:27:23 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 03:27:58 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 03:28:02 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 03:28:04 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 03:28:05 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:28:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:28:08 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 03:28:09 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:2e8bea8b22f8f5a4fd5aa85019945dd8ae04f283a4ba2a7aeb4536fe2f1d1ec2`  
		Last Modified: Tue, 26 May 2020 16:25:25 GMT  
		Size: 23.7 MB (23721687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc90876b9c9a7343ae432eaec7c8dc8859c1e84b6193da8d386815fde165a70e`  
		Last Modified: Wed, 17 Jun 2020 01:44:48 GMT  
		Size: 35.2 KB (35192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bfc658a5210a9f0c9cfcda5f504e720da9268e9f3f3bf48e3a9a7af360c959`  
		Last Modified: Wed, 17 Jun 2020 01:44:49 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef0f1b06b2142ff2bf35cc565f019ed9e4efe0d8f332825167538c2337bac8a`  
		Last Modified: Wed, 17 Jun 2020 01:44:49 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79f4068e2fc9c5ce913c3640637c35584b72816ca9485c4bf5af0a22994d0f6`  
		Last Modified: Wed, 17 Jun 2020 03:31:11 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5678c55b212ca2ce4ea7b4092838653b706277000f57d7a18526f3df6cba283`  
		Last Modified: Wed, 17 Jun 2020 03:31:11 GMT  
		Size: 2.7 MB (2665976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509de0ccfb79a34de230a6fef2cfc900bdb35f1f7f583fc957b7c23b46439d4f`  
		Last Modified: Wed, 17 Jun 2020 03:31:12 GMT  
		Size: 5.3 MB (5345550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5493b54160873a149e08eedf09e74628680b1d5e8826b90672f04c88c30ccb`  
		Last Modified: Wed, 17 Jun 2020 03:31:10 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe2b58fe1082de604f779b26f7bac0f685326b5584f5a43457f1d51effdca86`  
		Last Modified: Wed, 17 Jun 2020 03:31:09 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52cb618aa3e851b5a35792b706fd4e70901c2e3fd1faa3fcf12d719ac3d8ff1`  
		Last Modified: Wed, 17 Jun 2020 03:31:08 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8985f89f29dd85eccbd8da50a080817fa846f7b7baee89e54e83f79559fff4b`  
		Last Modified: Wed, 17 Jun 2020 03:31:35 GMT  
		Size: 122.9 MB (122900361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f01ca57315b3f1a9469f85034d0f072b2d67b5ee9d3c9d2e14e3487df4db4d`  
		Last Modified: Wed, 17 Jun 2020 03:31:08 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f414fc1b8d9a096289a531b03096d4af7478a1c627842175a15974cb041c879`  
		Last Modified: Wed, 17 Jun 2020 03:31:08 GMT  
		Size: 4.0 KB (3950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2.8-bionic` - linux; s390x

```console
$ docker pull mongo@sha256:e1c13c3ee8ae7031fdaa1e4cb645de3279a46ccf47511a9fb4b82c90d5c831f5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160598470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddfb01efb7ddfe0ac3ea40d0ded51ac1742d89e522b72b9ca43ec82ac2a642b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:41:48 GMT
ADD file:8708e93980b416070ba0bb024a7858748129059a85d2c771a4489c31710a9df1 in / 
# Wed, 17 Jun 2020 01:41:51 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:41:52 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:41:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:41:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:24:26 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 03:24:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:24:35 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:24:35 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 03:24:46 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:24:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:24:47 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Wed, 17 Jun 2020 03:24:48 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:24:48 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 03:24:48 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:24:48 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:24:48 GMT
ENV MONGO_MAJOR=4.2
# Wed, 17 Jun 2020 03:24:49 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 17 Jun 2020 03:24:49 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 03:25:14 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 03:25:18 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 03:25:18 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 03:25:19 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:25:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:25:19 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 03:25:19 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f3c26641772baa3348c0cce190edb38690a41f1824570c5c65cc363b42e5a5b5`  
		Last Modified: Sat, 30 May 2020 09:30:29 GMT  
		Size: 25.4 MB (25365846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf76fcee55454304ffbf9e321dda388a7e8de8a3916f854e1e588bc6c19b088`  
		Last Modified: Wed, 17 Jun 2020 01:42:56 GMT  
		Size: 36.2 KB (36165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5173e4f9f1868daa26021e1e701a000b0aadb2b611a487d089e7de4b728a7424`  
		Last Modified: Wed, 17 Jun 2020 01:42:56 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13da9fe451bd0f377d042d4bebef4ffd19163113e3e66dcd718fe187149a0dbd`  
		Last Modified: Wed, 17 Jun 2020 01:42:57 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d8fc9b1e9007ca5666c42ff8398a5227869b151fea1562c5e3cfb2188640e6`  
		Last Modified: Wed, 17 Jun 2020 03:28:52 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a889c8302a90f8884ff21edb649cf8dc1771453aca39505e61f29e053a1b64`  
		Last Modified: Wed, 17 Jun 2020 03:28:51 GMT  
		Size: 2.7 MB (2704483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:582fe8ee181790ce5fdadeef1c1cd7af40de0e8d2cb2e307fa05aed8d23a82b7`  
		Last Modified: Wed, 17 Jun 2020 03:28:50 GMT  
		Size: 5.7 MB (5745080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6096f1fa9fe7ad82ea015203f2410ac8b0831d0617db029aed54c698f84a2eaf`  
		Last Modified: Wed, 17 Jun 2020 03:28:50 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2bddaa2c78c2b5ac010b9af305db894e7bb616461499b863fe6af05c42bb502`  
		Last Modified: Wed, 17 Jun 2020 03:28:48 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b0ea0902452b7fe6fc59cc6001683eb80ddf80ba9fa1a59f83a576855317e12`  
		Last Modified: Wed, 17 Jun 2020 03:28:48 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507e67f4e596fea4d40f10e6ca9132a57d472a59bef2ce47ae79b92eb029ca7a`  
		Last Modified: Wed, 17 Jun 2020 03:29:02 GMT  
		Size: 126.7 MB (126738040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf93b294dbde6159d09390ee7231284abcaad59049a9d10eaebfc46619d4ad3`  
		Last Modified: Wed, 17 Jun 2020 03:28:48 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e514b21a3b45674ce414ecd79bf6adc339e8ea02fc1a80956ece983f3192be`  
		Last Modified: Wed, 17 Jun 2020 03:29:03 GMT  
		Size: 4.0 KB (3953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.2.8-windowsservercore`

```console
$ docker pull mongo@sha256:3dfacb1c248e30392bcfaba258677f7a057a4ea96b2a37de4839a01081742a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3750; amd64
	-	windows version 10.0.17763.1282; amd64

### `mongo:4.2.8-windowsservercore` - windows version 10.0.14393.3750; amd64

```console
$ docker pull mongo@sha256:af38590235375eb1218ddd651e660f1a6e6e6a882842e7b428f2d55d46cc937a
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6193023222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aaf2b53fe9e096da5ab6f4ae0e34caf7cf3de0a336bd9576cee60752c37c17b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 01 Jun 2020 18:53:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Jun 2020 12:52:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 17 Jun 2020 00:50:43 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 17 Jun 2020 00:50:44 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 17 Jun 2020 00:50:45 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 17 Jun 2020 01:08:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 17 Jun 2020 01:08:52 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 17 Jun 2020 01:08:53 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 01:08:54 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:375fbabb84945635805b46a02a17ac15a3177bcaae7404cfab5f1ceb0460cb60`  
		Size: 1.7 GB (1664011795 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:30efe9163d37226b077b25cd93b088cebd2ddbaadf173d143b9fe0ddecaeae53`  
		Last Modified: Wed, 10 Jun 2020 15:34:41 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b60479ef88c8a931aeeffaa74d289fbbf204229adb6a20c54d51456f70bb75`  
		Last Modified: Wed, 17 Jun 2020 01:32:04 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52bb592e6eb6512ccf1127b0311263697d559599357972414f4b776277bd628f`  
		Last Modified: Wed, 17 Jun 2020 01:32:04 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e57b55cda98f10b8c536232f9fd5fbc19c778c4043edc4fea012972832bb4570`  
		Last Modified: Wed, 17 Jun 2020 01:32:01 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eaad7a52f6dc4a311c3e724f9b5fe27f7af849fa6229fe21fc0490976fcb607`  
		Last Modified: Wed, 17 Jun 2020 01:32:57 GMT  
		Size: 459.0 MB (459017760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187b8e518ef05e3f4e7348e0ca7fef3e05414c63661223d63d83a36367ff9605`  
		Last Modified: Wed, 17 Jun 2020 01:32:01 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58773855217e4f81876fd21fd13a61d94d0f5a191e7025ce2bf26469077e330c`  
		Last Modified: Wed, 17 Jun 2020 01:32:01 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e25f1762a4dcad6fd6709c2602e0d459a0efb6aea6e10e16cb78796c27e496d`  
		Last Modified: Wed, 17 Jun 2020 01:32:01 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2.8-windowsservercore` - windows version 10.0.17763.1282; amd64

```console
$ docker pull mongo@sha256:a332d0d55bcb861ab664609d4ee8b7a3c7481e800fa5ad62009c671c1673af0b
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2752054828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86c12ab59b3d8850d880c02f06724769d7955a42bb4c5b10fd9a16cb6ad19f7`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Wed, 10 Jun 2020 12:43:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 17 Jun 2020 01:09:02 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 17 Jun 2020 01:09:03 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 17 Jun 2020 01:09:04 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 17 Jun 2020 01:28:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 17 Jun 2020 01:28:16 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 17 Jun 2020 01:28:18 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 01:28:19 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b11029314f3c794dc51e43c915b3e62f6b44aeb96f84b8b92f453e61cf7a2cb3`  
		Last Modified: Wed, 10 Jun 2020 15:34:12 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f51df57f2cb6ccc03b57cbd044ee4a49d9383489feb3872da465ba8b6bffa89`  
		Last Modified: Wed, 17 Jun 2020 01:33:19 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84353c49610a99480bfb74a8769e7446bbd898b8644c25d2b8c645c7a2e90e0e`  
		Last Modified: Wed, 17 Jun 2020 01:33:18 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c19d206596ed0cd1b7da30ba6e637be1d4c31dc398ca6f4d30d583593e31705`  
		Last Modified: Wed, 17 Jun 2020 01:33:16 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90fa0f2b93199d15d0678aa8a13db7d1470a5ce7ddb94ec8fa93a75156cce44`  
		Last Modified: Wed, 17 Jun 2020 01:34:14 GMT  
		Size: 458.1 MB (458132610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:369180762b76f75c56ed85ad59e938011c514ad32b51a43cbb6d5fcce885b5d1`  
		Last Modified: Wed, 17 Jun 2020 01:33:16 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f9c110c11f811446f2204714562c02b6eefeeb1cae671aa73af5e4cc7dfbd0`  
		Last Modified: Wed, 17 Jun 2020 01:33:16 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c7a275e52c9eafb08caf7a861ef21a725b77ee54c1b867ddb4b4da99814dd7`  
		Last Modified: Wed, 17 Jun 2020 01:33:16 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.2.8-windowsservercore-1809`

```console
$ docker pull mongo@sha256:bc2bc28a30754135707bfc25dd73c4aceb4ae89c943a243433b0b3f321f640fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1282; amd64

### `mongo:4.2.8-windowsservercore-1809` - windows version 10.0.17763.1282; amd64

```console
$ docker pull mongo@sha256:a332d0d55bcb861ab664609d4ee8b7a3c7481e800fa5ad62009c671c1673af0b
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2752054828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86c12ab59b3d8850d880c02f06724769d7955a42bb4c5b10fd9a16cb6ad19f7`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Wed, 10 Jun 2020 12:43:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 17 Jun 2020 01:09:02 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 17 Jun 2020 01:09:03 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 17 Jun 2020 01:09:04 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 17 Jun 2020 01:28:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 17 Jun 2020 01:28:16 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 17 Jun 2020 01:28:18 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 01:28:19 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b11029314f3c794dc51e43c915b3e62f6b44aeb96f84b8b92f453e61cf7a2cb3`  
		Last Modified: Wed, 10 Jun 2020 15:34:12 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f51df57f2cb6ccc03b57cbd044ee4a49d9383489feb3872da465ba8b6bffa89`  
		Last Modified: Wed, 17 Jun 2020 01:33:19 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84353c49610a99480bfb74a8769e7446bbd898b8644c25d2b8c645c7a2e90e0e`  
		Last Modified: Wed, 17 Jun 2020 01:33:18 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c19d206596ed0cd1b7da30ba6e637be1d4c31dc398ca6f4d30d583593e31705`  
		Last Modified: Wed, 17 Jun 2020 01:33:16 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90fa0f2b93199d15d0678aa8a13db7d1470a5ce7ddb94ec8fa93a75156cce44`  
		Last Modified: Wed, 17 Jun 2020 01:34:14 GMT  
		Size: 458.1 MB (458132610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:369180762b76f75c56ed85ad59e938011c514ad32b51a43cbb6d5fcce885b5d1`  
		Last Modified: Wed, 17 Jun 2020 01:33:16 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f9c110c11f811446f2204714562c02b6eefeeb1cae671aa73af5e4cc7dfbd0`  
		Last Modified: Wed, 17 Jun 2020 01:33:16 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c7a275e52c9eafb08caf7a861ef21a725b77ee54c1b867ddb4b4da99814dd7`  
		Last Modified: Wed, 17 Jun 2020 01:33:16 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.2.8-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:9b6e497bdcaa3a451d4296f944c0a13ac07344a7879cb41fb387ae288308fc61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3750; amd64

### `mongo:4.2.8-windowsservercore-ltsc2016` - windows version 10.0.14393.3750; amd64

```console
$ docker pull mongo@sha256:af38590235375eb1218ddd651e660f1a6e6e6a882842e7b428f2d55d46cc937a
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6193023222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aaf2b53fe9e096da5ab6f4ae0e34caf7cf3de0a336bd9576cee60752c37c17b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 01 Jun 2020 18:53:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Jun 2020 12:52:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 17 Jun 2020 00:50:43 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 17 Jun 2020 00:50:44 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 17 Jun 2020 00:50:45 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 17 Jun 2020 01:08:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 17 Jun 2020 01:08:52 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 17 Jun 2020 01:08:53 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 01:08:54 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:375fbabb84945635805b46a02a17ac15a3177bcaae7404cfab5f1ceb0460cb60`  
		Size: 1.7 GB (1664011795 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:30efe9163d37226b077b25cd93b088cebd2ddbaadf173d143b9fe0ddecaeae53`  
		Last Modified: Wed, 10 Jun 2020 15:34:41 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b60479ef88c8a931aeeffaa74d289fbbf204229adb6a20c54d51456f70bb75`  
		Last Modified: Wed, 17 Jun 2020 01:32:04 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52bb592e6eb6512ccf1127b0311263697d559599357972414f4b776277bd628f`  
		Last Modified: Wed, 17 Jun 2020 01:32:04 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e57b55cda98f10b8c536232f9fd5fbc19c778c4043edc4fea012972832bb4570`  
		Last Modified: Wed, 17 Jun 2020 01:32:01 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eaad7a52f6dc4a311c3e724f9b5fe27f7af849fa6229fe21fc0490976fcb607`  
		Last Modified: Wed, 17 Jun 2020 01:32:57 GMT  
		Size: 459.0 MB (459017760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187b8e518ef05e3f4e7348e0ca7fef3e05414c63661223d63d83a36367ff9605`  
		Last Modified: Wed, 17 Jun 2020 01:32:01 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58773855217e4f81876fd21fd13a61d94d0f5a191e7025ce2bf26469077e330c`  
		Last Modified: Wed, 17 Jun 2020 01:32:01 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e25f1762a4dcad6fd6709c2602e0d459a0efb6aea6e10e16cb78796c27e496d`  
		Last Modified: Wed, 17 Jun 2020 01:32:01 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.2-bionic`

```console
$ docker pull mongo@sha256:6bf46291247789c85932f35b2e824158e0f04771fb551aea10e3e7e86c349326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `mongo:4.2-bionic` - linux; amd64

```console
$ docker pull mongo@sha256:ed04fcf28fccf1bb2c295074775a24ddd007e14ca522ae97a56983f269cad163
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164652387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2cc1f48aed02a160b0447fd28b75952ed1d2df8c66693733d4954483734e44`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:20:29 GMT
ADD file:1e8d02626176dc8141df3c0a1365774ce73d79934654fe24a4b1e7f173108232 in / 
# Wed, 17 Jun 2020 01:20:30 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:20:31 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:20:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:20:32 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 05:16:06 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 05:16:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 05:16:16 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 05:16:16 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 05:16:30 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 05:16:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 05:16:33 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Wed, 17 Jun 2020 05:16:34 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 05:16:34 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 05:16:34 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 05:16:34 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 05:16:34 GMT
ENV MONGO_MAJOR=4.2
# Wed, 17 Jun 2020 05:16:35 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 17 Jun 2020 05:16:35 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 05:16:53 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 05:16:54 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 05:16:54 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 05:16:54 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 05:16:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 05:16:55 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 05:16:55 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:d7c3167c320d7a820935f54cf4290890ea19567da496ecf774e8773b35d5f065`  
		Last Modified: Wed, 27 May 2020 12:21:15 GMT  
		Size: 26.7 MB (26688718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:131f805ec7fd68d45a887e2ef82de61de0247b4eb934ab03b7c933650e854baa`  
		Last Modified: Wed, 17 Jun 2020 01:21:41 GMT  
		Size: 35.4 KB (35369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322ed380e680a77f30528ba013e3a802a7b44948a0609c7d1d732dd46a9a310d`  
		Last Modified: Wed, 17 Jun 2020 01:21:41 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac240b130982ad1c3ba3188abbf18ba4e54bdd9e504ce2d5c2eff6d3e86b8dd`  
		Last Modified: Wed, 17 Jun 2020 01:21:41 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5704a01b59ff4d100b5bcc0244090cb5b369649b41a468a82cb5015afdc4f9d`  
		Last Modified: Wed, 17 Jun 2020 05:18:30 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e396e2a1e6820b238c82087b900e4f03e1304b30ee16a5341b0c6a2a9eec20e`  
		Last Modified: Wed, 17 Jun 2020 05:18:29 GMT  
		Size: 3.0 MB (2973543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:914fffcb1cc543f9e16861fe6d80fdaad26ea9c69ba952c73cb3db44a9cfc545`  
		Last Modified: Wed, 17 Jun 2020 05:18:30 GMT  
		Size: 5.8 MB (5823974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692bd0d35810fbf133d67af4f0ae0c627fb731b875d5370d3dfaa3f1a06392fa`  
		Last Modified: Wed, 17 Jun 2020 05:18:29 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122d231765e47cbdd1b934b3ee55ffa291b76b17e4134be5b6e9837c52053c9e`  
		Last Modified: Wed, 17 Jun 2020 05:18:28 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9c497305ce2ee80e9d80fb69dcf2766f51b6b23e093fbf9d0d837b14376810`  
		Last Modified: Wed, 17 Jun 2020 05:18:28 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e3ca7a65fcd8d5d002ae04e06a5d7b900020097dec64e04923b9fa25d7d633`  
		Last Modified: Wed, 17 Jun 2020 05:18:46 GMT  
		Size: 129.1 MB (129122023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70e0d9672b4cbcef6ddbaa3fae90fb8181aeb83b59cac8f4910d69f7c359f96`  
		Last Modified: Wed, 17 Jun 2020 05:18:28 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc04aade5db18c8ca826bfaef542aa9b48f2b3045dfe7a4fa0d4f11714d37a1`  
		Last Modified: Wed, 17 Jun 2020 05:18:28 GMT  
		Size: 4.0 KB (3955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2-bionic` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:cdec0bd28e60bc06892f9972803753d57fdc3d4bcff657b694ba7f35b80d3d02
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154677642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f84af28ce3aa3b7b04964d7f7ee9eb0ae10e3c19e684ad29ceeca55c605f2924`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:42:33 GMT
ADD file:7dc8819fd3d4b84ad19fb836e5bfda64a5ffefc371166f70d4d41dff6b22d450 in / 
# Wed, 17 Jun 2020 01:42:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:42:41 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:42:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:42:45 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:26:00 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 03:26:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:26:24 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:26:25 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 03:27:01 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:27:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:27:06 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Wed, 17 Jun 2020 03:27:10 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:27:12 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 03:27:13 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:27:16 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:27:19 GMT
ENV MONGO_MAJOR=4.2
# Wed, 17 Jun 2020 03:27:20 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 17 Jun 2020 03:27:23 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 03:27:58 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 03:28:02 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 03:28:04 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 03:28:05 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:28:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:28:08 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 03:28:09 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:2e8bea8b22f8f5a4fd5aa85019945dd8ae04f283a4ba2a7aeb4536fe2f1d1ec2`  
		Last Modified: Tue, 26 May 2020 16:25:25 GMT  
		Size: 23.7 MB (23721687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc90876b9c9a7343ae432eaec7c8dc8859c1e84b6193da8d386815fde165a70e`  
		Last Modified: Wed, 17 Jun 2020 01:44:48 GMT  
		Size: 35.2 KB (35192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bfc658a5210a9f0c9cfcda5f504e720da9268e9f3f3bf48e3a9a7af360c959`  
		Last Modified: Wed, 17 Jun 2020 01:44:49 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef0f1b06b2142ff2bf35cc565f019ed9e4efe0d8f332825167538c2337bac8a`  
		Last Modified: Wed, 17 Jun 2020 01:44:49 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79f4068e2fc9c5ce913c3640637c35584b72816ca9485c4bf5af0a22994d0f6`  
		Last Modified: Wed, 17 Jun 2020 03:31:11 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5678c55b212ca2ce4ea7b4092838653b706277000f57d7a18526f3df6cba283`  
		Last Modified: Wed, 17 Jun 2020 03:31:11 GMT  
		Size: 2.7 MB (2665976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509de0ccfb79a34de230a6fef2cfc900bdb35f1f7f583fc957b7c23b46439d4f`  
		Last Modified: Wed, 17 Jun 2020 03:31:12 GMT  
		Size: 5.3 MB (5345550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5493b54160873a149e08eedf09e74628680b1d5e8826b90672f04c88c30ccb`  
		Last Modified: Wed, 17 Jun 2020 03:31:10 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe2b58fe1082de604f779b26f7bac0f685326b5584f5a43457f1d51effdca86`  
		Last Modified: Wed, 17 Jun 2020 03:31:09 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52cb618aa3e851b5a35792b706fd4e70901c2e3fd1faa3fcf12d719ac3d8ff1`  
		Last Modified: Wed, 17 Jun 2020 03:31:08 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8985f89f29dd85eccbd8da50a080817fa846f7b7baee89e54e83f79559fff4b`  
		Last Modified: Wed, 17 Jun 2020 03:31:35 GMT  
		Size: 122.9 MB (122900361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f01ca57315b3f1a9469f85034d0f072b2d67b5ee9d3c9d2e14e3487df4db4d`  
		Last Modified: Wed, 17 Jun 2020 03:31:08 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f414fc1b8d9a096289a531b03096d4af7478a1c627842175a15974cb041c879`  
		Last Modified: Wed, 17 Jun 2020 03:31:08 GMT  
		Size: 4.0 KB (3950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2-bionic` - linux; s390x

```console
$ docker pull mongo@sha256:e1c13c3ee8ae7031fdaa1e4cb645de3279a46ccf47511a9fb4b82c90d5c831f5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160598470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddfb01efb7ddfe0ac3ea40d0ded51ac1742d89e522b72b9ca43ec82ac2a642b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:41:48 GMT
ADD file:8708e93980b416070ba0bb024a7858748129059a85d2c771a4489c31710a9df1 in / 
# Wed, 17 Jun 2020 01:41:51 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:41:52 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:41:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:41:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:24:26 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 03:24:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:24:35 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:24:35 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 03:24:46 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:24:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:24:47 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Wed, 17 Jun 2020 03:24:48 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:24:48 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 03:24:48 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:24:48 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:24:48 GMT
ENV MONGO_MAJOR=4.2
# Wed, 17 Jun 2020 03:24:49 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 17 Jun 2020 03:24:49 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 03:25:14 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 03:25:18 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 03:25:18 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 03:25:19 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:25:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:25:19 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 03:25:19 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f3c26641772baa3348c0cce190edb38690a41f1824570c5c65cc363b42e5a5b5`  
		Last Modified: Sat, 30 May 2020 09:30:29 GMT  
		Size: 25.4 MB (25365846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf76fcee55454304ffbf9e321dda388a7e8de8a3916f854e1e588bc6c19b088`  
		Last Modified: Wed, 17 Jun 2020 01:42:56 GMT  
		Size: 36.2 KB (36165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5173e4f9f1868daa26021e1e701a000b0aadb2b611a487d089e7de4b728a7424`  
		Last Modified: Wed, 17 Jun 2020 01:42:56 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13da9fe451bd0f377d042d4bebef4ffd19163113e3e66dcd718fe187149a0dbd`  
		Last Modified: Wed, 17 Jun 2020 01:42:57 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d8fc9b1e9007ca5666c42ff8398a5227869b151fea1562c5e3cfb2188640e6`  
		Last Modified: Wed, 17 Jun 2020 03:28:52 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a889c8302a90f8884ff21edb649cf8dc1771453aca39505e61f29e053a1b64`  
		Last Modified: Wed, 17 Jun 2020 03:28:51 GMT  
		Size: 2.7 MB (2704483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:582fe8ee181790ce5fdadeef1c1cd7af40de0e8d2cb2e307fa05aed8d23a82b7`  
		Last Modified: Wed, 17 Jun 2020 03:28:50 GMT  
		Size: 5.7 MB (5745080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6096f1fa9fe7ad82ea015203f2410ac8b0831d0617db029aed54c698f84a2eaf`  
		Last Modified: Wed, 17 Jun 2020 03:28:50 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2bddaa2c78c2b5ac010b9af305db894e7bb616461499b863fe6af05c42bb502`  
		Last Modified: Wed, 17 Jun 2020 03:28:48 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b0ea0902452b7fe6fc59cc6001683eb80ddf80ba9fa1a59f83a576855317e12`  
		Last Modified: Wed, 17 Jun 2020 03:28:48 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507e67f4e596fea4d40f10e6ca9132a57d472a59bef2ce47ae79b92eb029ca7a`  
		Last Modified: Wed, 17 Jun 2020 03:29:02 GMT  
		Size: 126.7 MB (126738040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf93b294dbde6159d09390ee7231284abcaad59049a9d10eaebfc46619d4ad3`  
		Last Modified: Wed, 17 Jun 2020 03:28:48 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e514b21a3b45674ce414ecd79bf6adc339e8ea02fc1a80956ece983f3192be`  
		Last Modified: Wed, 17 Jun 2020 03:29:03 GMT  
		Size: 4.0 KB (3953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.2-windowsservercore`

```console
$ docker pull mongo@sha256:3dfacb1c248e30392bcfaba258677f7a057a4ea96b2a37de4839a01081742a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3750; amd64
	-	windows version 10.0.17763.1282; amd64

### `mongo:4.2-windowsservercore` - windows version 10.0.14393.3750; amd64

```console
$ docker pull mongo@sha256:af38590235375eb1218ddd651e660f1a6e6e6a882842e7b428f2d55d46cc937a
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6193023222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aaf2b53fe9e096da5ab6f4ae0e34caf7cf3de0a336bd9576cee60752c37c17b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 01 Jun 2020 18:53:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Jun 2020 12:52:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 17 Jun 2020 00:50:43 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 17 Jun 2020 00:50:44 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 17 Jun 2020 00:50:45 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 17 Jun 2020 01:08:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 17 Jun 2020 01:08:52 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 17 Jun 2020 01:08:53 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 01:08:54 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:375fbabb84945635805b46a02a17ac15a3177bcaae7404cfab5f1ceb0460cb60`  
		Size: 1.7 GB (1664011795 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:30efe9163d37226b077b25cd93b088cebd2ddbaadf173d143b9fe0ddecaeae53`  
		Last Modified: Wed, 10 Jun 2020 15:34:41 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b60479ef88c8a931aeeffaa74d289fbbf204229adb6a20c54d51456f70bb75`  
		Last Modified: Wed, 17 Jun 2020 01:32:04 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52bb592e6eb6512ccf1127b0311263697d559599357972414f4b776277bd628f`  
		Last Modified: Wed, 17 Jun 2020 01:32:04 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e57b55cda98f10b8c536232f9fd5fbc19c778c4043edc4fea012972832bb4570`  
		Last Modified: Wed, 17 Jun 2020 01:32:01 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eaad7a52f6dc4a311c3e724f9b5fe27f7af849fa6229fe21fc0490976fcb607`  
		Last Modified: Wed, 17 Jun 2020 01:32:57 GMT  
		Size: 459.0 MB (459017760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187b8e518ef05e3f4e7348e0ca7fef3e05414c63661223d63d83a36367ff9605`  
		Last Modified: Wed, 17 Jun 2020 01:32:01 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58773855217e4f81876fd21fd13a61d94d0f5a191e7025ce2bf26469077e330c`  
		Last Modified: Wed, 17 Jun 2020 01:32:01 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e25f1762a4dcad6fd6709c2602e0d459a0efb6aea6e10e16cb78796c27e496d`  
		Last Modified: Wed, 17 Jun 2020 01:32:01 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.2-windowsservercore` - windows version 10.0.17763.1282; amd64

```console
$ docker pull mongo@sha256:a332d0d55bcb861ab664609d4ee8b7a3c7481e800fa5ad62009c671c1673af0b
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2752054828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86c12ab59b3d8850d880c02f06724769d7955a42bb4c5b10fd9a16cb6ad19f7`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Wed, 10 Jun 2020 12:43:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 17 Jun 2020 01:09:02 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 17 Jun 2020 01:09:03 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 17 Jun 2020 01:09:04 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 17 Jun 2020 01:28:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 17 Jun 2020 01:28:16 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 17 Jun 2020 01:28:18 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 01:28:19 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b11029314f3c794dc51e43c915b3e62f6b44aeb96f84b8b92f453e61cf7a2cb3`  
		Last Modified: Wed, 10 Jun 2020 15:34:12 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f51df57f2cb6ccc03b57cbd044ee4a49d9383489feb3872da465ba8b6bffa89`  
		Last Modified: Wed, 17 Jun 2020 01:33:19 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84353c49610a99480bfb74a8769e7446bbd898b8644c25d2b8c645c7a2e90e0e`  
		Last Modified: Wed, 17 Jun 2020 01:33:18 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c19d206596ed0cd1b7da30ba6e637be1d4c31dc398ca6f4d30d583593e31705`  
		Last Modified: Wed, 17 Jun 2020 01:33:16 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90fa0f2b93199d15d0678aa8a13db7d1470a5ce7ddb94ec8fa93a75156cce44`  
		Last Modified: Wed, 17 Jun 2020 01:34:14 GMT  
		Size: 458.1 MB (458132610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:369180762b76f75c56ed85ad59e938011c514ad32b51a43cbb6d5fcce885b5d1`  
		Last Modified: Wed, 17 Jun 2020 01:33:16 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f9c110c11f811446f2204714562c02b6eefeeb1cae671aa73af5e4cc7dfbd0`  
		Last Modified: Wed, 17 Jun 2020 01:33:16 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c7a275e52c9eafb08caf7a861ef21a725b77ee54c1b867ddb4b4da99814dd7`  
		Last Modified: Wed, 17 Jun 2020 01:33:16 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.2-windowsservercore-1809`

```console
$ docker pull mongo@sha256:bc2bc28a30754135707bfc25dd73c4aceb4ae89c943a243433b0b3f321f640fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1282; amd64

### `mongo:4.2-windowsservercore-1809` - windows version 10.0.17763.1282; amd64

```console
$ docker pull mongo@sha256:a332d0d55bcb861ab664609d4ee8b7a3c7481e800fa5ad62009c671c1673af0b
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2752054828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86c12ab59b3d8850d880c02f06724769d7955a42bb4c5b10fd9a16cb6ad19f7`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Wed, 10 Jun 2020 12:43:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 17 Jun 2020 01:09:02 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 17 Jun 2020 01:09:03 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 17 Jun 2020 01:09:04 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 17 Jun 2020 01:28:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 17 Jun 2020 01:28:16 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 17 Jun 2020 01:28:18 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 01:28:19 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b11029314f3c794dc51e43c915b3e62f6b44aeb96f84b8b92f453e61cf7a2cb3`  
		Last Modified: Wed, 10 Jun 2020 15:34:12 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f51df57f2cb6ccc03b57cbd044ee4a49d9383489feb3872da465ba8b6bffa89`  
		Last Modified: Wed, 17 Jun 2020 01:33:19 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84353c49610a99480bfb74a8769e7446bbd898b8644c25d2b8c645c7a2e90e0e`  
		Last Modified: Wed, 17 Jun 2020 01:33:18 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c19d206596ed0cd1b7da30ba6e637be1d4c31dc398ca6f4d30d583593e31705`  
		Last Modified: Wed, 17 Jun 2020 01:33:16 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90fa0f2b93199d15d0678aa8a13db7d1470a5ce7ddb94ec8fa93a75156cce44`  
		Last Modified: Wed, 17 Jun 2020 01:34:14 GMT  
		Size: 458.1 MB (458132610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:369180762b76f75c56ed85ad59e938011c514ad32b51a43cbb6d5fcce885b5d1`  
		Last Modified: Wed, 17 Jun 2020 01:33:16 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f9c110c11f811446f2204714562c02b6eefeeb1cae671aa73af5e4cc7dfbd0`  
		Last Modified: Wed, 17 Jun 2020 01:33:16 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c7a275e52c9eafb08caf7a861ef21a725b77ee54c1b867ddb4b4da99814dd7`  
		Last Modified: Wed, 17 Jun 2020 01:33:16 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.2-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:9b6e497bdcaa3a451d4296f944c0a13ac07344a7879cb41fb387ae288308fc61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3750; amd64

### `mongo:4.2-windowsservercore-ltsc2016` - windows version 10.0.14393.3750; amd64

```console
$ docker pull mongo@sha256:af38590235375eb1218ddd651e660f1a6e6e6a882842e7b428f2d55d46cc937a
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6193023222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aaf2b53fe9e096da5ab6f4ae0e34caf7cf3de0a336bd9576cee60752c37c17b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 01 Jun 2020 18:53:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Jun 2020 12:52:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 17 Jun 2020 00:50:43 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 17 Jun 2020 00:50:44 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 17 Jun 2020 00:50:45 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 17 Jun 2020 01:08:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 17 Jun 2020 01:08:52 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 17 Jun 2020 01:08:53 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 01:08:54 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:375fbabb84945635805b46a02a17ac15a3177bcaae7404cfab5f1ceb0460cb60`  
		Size: 1.7 GB (1664011795 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:30efe9163d37226b077b25cd93b088cebd2ddbaadf173d143b9fe0ddecaeae53`  
		Last Modified: Wed, 10 Jun 2020 15:34:41 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b60479ef88c8a931aeeffaa74d289fbbf204229adb6a20c54d51456f70bb75`  
		Last Modified: Wed, 17 Jun 2020 01:32:04 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52bb592e6eb6512ccf1127b0311263697d559599357972414f4b776277bd628f`  
		Last Modified: Wed, 17 Jun 2020 01:32:04 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e57b55cda98f10b8c536232f9fd5fbc19c778c4043edc4fea012972832bb4570`  
		Last Modified: Wed, 17 Jun 2020 01:32:01 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eaad7a52f6dc4a311c3e724f9b5fe27f7af849fa6229fe21fc0490976fcb607`  
		Last Modified: Wed, 17 Jun 2020 01:32:57 GMT  
		Size: 459.0 MB (459017760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187b8e518ef05e3f4e7348e0ca7fef3e05414c63661223d63d83a36367ff9605`  
		Last Modified: Wed, 17 Jun 2020 01:32:01 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58773855217e4f81876fd21fd13a61d94d0f5a191e7025ce2bf26469077e330c`  
		Last Modified: Wed, 17 Jun 2020 01:32:01 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e25f1762a4dcad6fd6709c2602e0d459a0efb6aea6e10e16cb78796c27e496d`  
		Last Modified: Wed, 17 Jun 2020 01:32:01 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.4.0-rc9`

```console
$ docker pull mongo@sha256:d253a81dc8c13b3fe94b2b1b8fd1c763c8dd19503702df6ce3e02a6bcff84a09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x
	-	windows version 10.0.14393.3750; amd64
	-	windows version 10.0.17763.1282; amd64

### `mongo:4.4.0-rc9` - linux; amd64

```console
$ docker pull mongo@sha256:08a7438918614c7cb939c947bc471e687ac2e8485a7f1d6cb29f98d43650eb81
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.7 MB (177701947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ece36a7d4fb83f0867b7fe3de0923e2e70d0d8f8886191993685962fbf19bd4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:20:29 GMT
ADD file:1e8d02626176dc8141df3c0a1365774ce73d79934654fe24a4b1e7f173108232 in / 
# Wed, 17 Jun 2020 01:20:30 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:20:31 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:20:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:20:32 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 05:16:06 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 05:16:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 05:16:16 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 05:16:16 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 05:16:30 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 05:16:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 05:17:00 GMT
ENV GPG_KEYS=99DC630F00A2F97F27C6A02A253612A09571B484 20691EEC35216C63CAF66CE1656408E390CFB1F5 E162F504A20CDF15827F718D4B7C549A058F8B6B 9DA31620334BD75D9DCB49F368818C72E52529D4 2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Wed, 17 Jun 2020 05:17:01 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 05:17:01 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 05:17:01 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 05:17:02 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 05:17:02 GMT
ENV MONGO_MAJOR=testing
# Wed, 17 Jun 2020 05:17:02 GMT
ENV MONGO_VERSION=4.4.0~rc9
# Wed, 17 Jun 2020 05:17:03 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 05:17:23 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 05:17:26 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 05:17:26 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 05:17:26 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 05:17:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 05:17:27 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 05:17:27 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:d7c3167c320d7a820935f54cf4290890ea19567da496ecf774e8773b35d5f065`  
		Last Modified: Wed, 27 May 2020 12:21:15 GMT  
		Size: 26.7 MB (26688718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:131f805ec7fd68d45a887e2ef82de61de0247b4eb934ab03b7c933650e854baa`  
		Last Modified: Wed, 17 Jun 2020 01:21:41 GMT  
		Size: 35.4 KB (35369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322ed380e680a77f30528ba013e3a802a7b44948a0609c7d1d732dd46a9a310d`  
		Last Modified: Wed, 17 Jun 2020 01:21:41 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac240b130982ad1c3ba3188abbf18ba4e54bdd9e504ce2d5c2eff6d3e86b8dd`  
		Last Modified: Wed, 17 Jun 2020 01:21:41 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5704a01b59ff4d100b5bcc0244090cb5b369649b41a468a82cb5015afdc4f9d`  
		Last Modified: Wed, 17 Jun 2020 05:18:30 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e396e2a1e6820b238c82087b900e4f03e1304b30ee16a5341b0c6a2a9eec20e`  
		Last Modified: Wed, 17 Jun 2020 05:18:29 GMT  
		Size: 3.0 MB (2973543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:914fffcb1cc543f9e16861fe6d80fdaad26ea9c69ba952c73cb3db44a9cfc545`  
		Last Modified: Wed, 17 Jun 2020 05:18:30 GMT  
		Size: 5.8 MB (5823974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692bd0d35810fbf133d67af4f0ae0c627fb731b875d5370d3dfaa3f1a06392fa`  
		Last Modified: Wed, 17 Jun 2020 05:18:29 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ae4de9714c056e86d9925b9efc4d6be680aa04cfb1fd1dfd58bdb93dadffc5`  
		Last Modified: Wed, 17 Jun 2020 05:18:52 GMT  
		Size: 6.3 KB (6252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27913ee473ed41f8d48e523eac423b4627c2665aa164447d132f16dc2fbc65d`  
		Last Modified: Wed, 17 Jun 2020 05:18:52 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9274dbb221bc53f997714e90d3d95a7eed3786847bb400dddffa1e1fdf1f1e`  
		Last Modified: Wed, 17 Jun 2020 05:19:14 GMT  
		Size: 142.2 MB (142166762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c46635cb88709e9bad2966b953bb001762cebcd352bdc838d942364dbd55b8d`  
		Last Modified: Wed, 17 Jun 2020 05:18:52 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8bfa6aa4decd3c6d67bf9fe6d4762e1557c1e30c52e71884ce3476b05f614f`  
		Last Modified: Wed, 17 Jun 2020 05:18:52 GMT  
		Size: 4.0 KB (3950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.4.0-rc9` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:536a31542b7d3f9ba2dd78dcc7a53e83d4a37c2796ab4bbaecdd28a7a126eb5d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.7 MB (167661341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5a682f2ee63f45ab3382088349f51c0af8b9d20952a766d219656ec9ddf42c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:42:33 GMT
ADD file:7dc8819fd3d4b84ad19fb836e5bfda64a5ffefc371166f70d4d41dff6b22d450 in / 
# Wed, 17 Jun 2020 01:42:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:42:41 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:42:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:42:45 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:26:00 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 03:26:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:26:24 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:26:25 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 03:27:01 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:27:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:28:31 GMT
ENV GPG_KEYS=99DC630F00A2F97F27C6A02A253612A09571B484 20691EEC35216C63CAF66CE1656408E390CFB1F5 E162F504A20CDF15827F718D4B7C549A058F8B6B 9DA31620334BD75D9DCB49F368818C72E52529D4 2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Wed, 17 Jun 2020 03:28:34 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:28:36 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 03:28:39 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:28:41 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:28:42 GMT
ENV MONGO_MAJOR=testing
# Wed, 17 Jun 2020 03:28:43 GMT
ENV MONGO_VERSION=4.4.0~rc9
# Wed, 17 Jun 2020 03:28:46 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 03:29:24 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 03:29:27 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 03:29:28 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 03:29:29 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:29:31 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 03:29:33 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:2e8bea8b22f8f5a4fd5aa85019945dd8ae04f283a4ba2a7aeb4536fe2f1d1ec2`  
		Last Modified: Tue, 26 May 2020 16:25:25 GMT  
		Size: 23.7 MB (23721687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc90876b9c9a7343ae432eaec7c8dc8859c1e84b6193da8d386815fde165a70e`  
		Last Modified: Wed, 17 Jun 2020 01:44:48 GMT  
		Size: 35.2 KB (35192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bfc658a5210a9f0c9cfcda5f504e720da9268e9f3f3bf48e3a9a7af360c959`  
		Last Modified: Wed, 17 Jun 2020 01:44:49 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef0f1b06b2142ff2bf35cc565f019ed9e4efe0d8f332825167538c2337bac8a`  
		Last Modified: Wed, 17 Jun 2020 01:44:49 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79f4068e2fc9c5ce913c3640637c35584b72816ca9485c4bf5af0a22994d0f6`  
		Last Modified: Wed, 17 Jun 2020 03:31:11 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5678c55b212ca2ce4ea7b4092838653b706277000f57d7a18526f3df6cba283`  
		Last Modified: Wed, 17 Jun 2020 03:31:11 GMT  
		Size: 2.7 MB (2665976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509de0ccfb79a34de230a6fef2cfc900bdb35f1f7f583fc957b7c23b46439d4f`  
		Last Modified: Wed, 17 Jun 2020 03:31:12 GMT  
		Size: 5.3 MB (5345550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5493b54160873a149e08eedf09e74628680b1d5e8826b90672f04c88c30ccb`  
		Last Modified: Wed, 17 Jun 2020 03:31:10 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deafc22fb839309e0ff73d69148b1061567442476c00078e55fd8f2ca6fcd5c8`  
		Last Modified: Wed, 17 Jun 2020 03:31:47 GMT  
		Size: 6.3 KB (6253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6774a6455e0eda434f9817370afa1a8a0ae837302f9816494275f66238012ae2`  
		Last Modified: Wed, 17 Jun 2020 03:31:47 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7bd711f5ff0470496bfd97c7937c82ec2b9d5fa4ee3ded334f2a51d237ddbf`  
		Last Modified: Wed, 17 Jun 2020 03:32:25 GMT  
		Size: 135.9 MB (135879240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8898fe6b89326089621a29a76f81a23cc42d9fe5f809a53b67466040c474420`  
		Last Modified: Wed, 17 Jun 2020 03:31:47 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b178145b3f3d3bad498dbb2534db4a93ff08031a2d2d8b5b47fdf9d7e6fa45c6`  
		Last Modified: Wed, 17 Jun 2020 03:31:47 GMT  
		Size: 4.0 KB (3952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.4.0-rc9` - linux; s390x

```console
$ docker pull mongo@sha256:54151c9e8490a5ba1f294fb021b5fb2566dce18f481ac5ffae4d4311b2028d0b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.7 MB (172657780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1164e632ad52e2cf5eacf9312a565830950785edf24dbfac0186e9a12f174ee8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:41:48 GMT
ADD file:8708e93980b416070ba0bb024a7858748129059a85d2c771a4489c31710a9df1 in / 
# Wed, 17 Jun 2020 01:41:51 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:41:52 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:41:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:41:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:24:26 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 03:24:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:24:35 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:24:35 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 03:24:46 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:24:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:25:33 GMT
ENV GPG_KEYS=99DC630F00A2F97F27C6A02A253612A09571B484 20691EEC35216C63CAF66CE1656408E390CFB1F5 E162F504A20CDF15827F718D4B7C549A058F8B6B 9DA31620334BD75D9DCB49F368818C72E52529D4 2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Wed, 17 Jun 2020 03:25:34 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:25:34 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 03:25:34 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:25:34 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:25:35 GMT
ENV MONGO_MAJOR=testing
# Wed, 17 Jun 2020 03:25:35 GMT
ENV MONGO_VERSION=4.4.0~rc9
# Wed, 17 Jun 2020 03:25:35 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 03:28:23 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 03:28:28 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 03:28:29 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 03:28:29 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:28:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:28:29 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 03:28:30 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f3c26641772baa3348c0cce190edb38690a41f1824570c5c65cc363b42e5a5b5`  
		Last Modified: Sat, 30 May 2020 09:30:29 GMT  
		Size: 25.4 MB (25365846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf76fcee55454304ffbf9e321dda388a7e8de8a3916f854e1e588bc6c19b088`  
		Last Modified: Wed, 17 Jun 2020 01:42:56 GMT  
		Size: 36.2 KB (36165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5173e4f9f1868daa26021e1e701a000b0aadb2b611a487d089e7de4b728a7424`  
		Last Modified: Wed, 17 Jun 2020 01:42:56 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13da9fe451bd0f377d042d4bebef4ffd19163113e3e66dcd718fe187149a0dbd`  
		Last Modified: Wed, 17 Jun 2020 01:42:57 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d8fc9b1e9007ca5666c42ff8398a5227869b151fea1562c5e3cfb2188640e6`  
		Last Modified: Wed, 17 Jun 2020 03:28:52 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a889c8302a90f8884ff21edb649cf8dc1771453aca39505e61f29e053a1b64`  
		Last Modified: Wed, 17 Jun 2020 03:28:51 GMT  
		Size: 2.7 MB (2704483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:582fe8ee181790ce5fdadeef1c1cd7af40de0e8d2cb2e307fa05aed8d23a82b7`  
		Last Modified: Wed, 17 Jun 2020 03:28:50 GMT  
		Size: 5.7 MB (5745080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6096f1fa9fe7ad82ea015203f2410ac8b0831d0617db029aed54c698f84a2eaf`  
		Last Modified: Wed, 17 Jun 2020 03:28:50 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce8677aae44e31d383f2709bd3cc41ba2aeb459d07e6e05442802c8fe09b36c`  
		Last Modified: Wed, 17 Jun 2020 03:29:11 GMT  
		Size: 6.2 KB (6248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63fd6a4cab24edcfbee6d202c0a9e3ed0923dac53271f99942f0a7ab84ec83e7`  
		Last Modified: Wed, 17 Jun 2020 03:29:10 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3652237c6732d7d65cced49e7409ba137ea2273d6bd1c26028d3d2af7d56fddd`  
		Last Modified: Wed, 17 Jun 2020 03:29:28 GMT  
		Size: 138.8 MB (138792530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a223e5df98ceffef359a0bd07fe9327cf5f384a2ad7563899be68aa25a5006d5`  
		Last Modified: Wed, 17 Jun 2020 03:29:10 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddeaa0784e1dcec5ff0f75d4e2a824607e6bceca061e67fcdfd15ddc3249017b`  
		Last Modified: Wed, 17 Jun 2020 03:29:41 GMT  
		Size: 4.0 KB (3953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.4.0-rc9` - windows version 10.0.14393.3750; amd64

```console
$ docker pull mongo@sha256:215f1361466e6995d5a57effb6c461d42d7d7cfb19c4bae176999db59440ace6
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5784920267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec81dd11cfe596c69cd23bb0a3e6562beb0f5ea0e32111cffd56de47adef954`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 01 Jun 2020 18:53:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Jun 2020 12:52:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jun 2020 19:16:43 GMT
ENV MONGO_VERSION=4.4.0-rc9
# Thu, 11 Jun 2020 19:16:44 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.0-rc9-signed.msi
# Thu, 11 Jun 2020 19:16:45 GMT
ENV MONGO_DOWNLOAD_SHA256=efa1d75f19d03500deb895fcc67c8afd1ae4ebd347821673f3a54ba7af8ea63c
# Thu, 11 Jun 2020 19:30:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 11 Jun 2020 19:30:28 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 11 Jun 2020 19:30:30 GMT
EXPOSE 27017
# Thu, 11 Jun 2020 19:30:31 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:375fbabb84945635805b46a02a17ac15a3177bcaae7404cfab5f1ceb0460cb60`  
		Size: 1.7 GB (1664011795 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:30efe9163d37226b077b25cd93b088cebd2ddbaadf173d143b9fe0ddecaeae53`  
		Last Modified: Wed, 10 Jun 2020 15:34:41 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f722bab4d6f564851060c094083c229bc7e58ad34bb63f63adf236f9b42161`  
		Last Modified: Thu, 11 Jun 2020 19:50:23 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c119bfdf019d71f020a808c4f5bcc3f141c37923eb4df84b35c0d64d24255f5`  
		Last Modified: Thu, 11 Jun 2020 19:50:23 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88dd5ed82ce663bb0dd49f1ba28274c0dd50b21500e838a693bc6df493013993`  
		Last Modified: Thu, 11 Jun 2020 19:50:21 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319d5363e64c1103acb8013122be273969f0339da0b37ff3c524c4e93f184f92`  
		Last Modified: Thu, 11 Jun 2020 19:50:30 GMT  
		Size: 50.9 MB (50914489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3598bb59158e998723a319fc5452a711979f68fc439064076339b6acbf6509`  
		Last Modified: Thu, 11 Jun 2020 19:50:21 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a419ffdf45ea371482995436d267f646e75ab9d8eb38a9739a567c985054fb9c`  
		Last Modified: Thu, 11 Jun 2020 19:50:21 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca4bbbef218f58984237b6a3ac496ded351fdb00850abcaaf1bf39c4a586ddb`  
		Last Modified: Thu, 11 Jun 2020 19:50:21 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.4.0-rc9` - windows version 10.0.17763.1282; amd64

```console
$ docker pull mongo@sha256:f205b8f1adaba4f302e4e08dfd199917ddfd027e22957dd466befddf99e6bfd9
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2706264212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2caf8fbd3bef0c6654b37c79bf354076d15dd8e6d83641a5b6cd129a982772ec`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Wed, 10 Jun 2020 12:43:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jun 2020 19:30:44 GMT
ENV MONGO_VERSION=4.4.0-rc9
# Thu, 11 Jun 2020 19:30:44 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.0-rc9-signed.msi
# Thu, 11 Jun 2020 19:30:45 GMT
ENV MONGO_DOWNLOAD_SHA256=efa1d75f19d03500deb895fcc67c8afd1ae4ebd347821673f3a54ba7af8ea63c
# Thu, 11 Jun 2020 19:49:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 11 Jun 2020 19:49:08 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 11 Jun 2020 19:49:09 GMT
EXPOSE 27017
# Thu, 11 Jun 2020 19:49:11 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b11029314f3c794dc51e43c915b3e62f6b44aeb96f84b8b92f453e61cf7a2cb3`  
		Last Modified: Wed, 10 Jun 2020 15:34:12 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599f6162438ec450553183469d80b7b2ae5da8231df1f927ab76bfddc4b3c0ce`  
		Last Modified: Thu, 11 Jun 2020 19:50:44 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e2f3d8d745162590cfa721fb659aaf0b0401d1247e77cf43ffae2c49cbce4fd`  
		Last Modified: Thu, 11 Jun 2020 19:50:44 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6066806f7a19d5d3b2f0bea4f42c11ea2f6d2ad1a29b05df6a23b5cba7e0c61`  
		Last Modified: Thu, 11 Jun 2020 19:50:42 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d062a956e06d65c5441f637a66d90250482f6d8f3c6685efb18c8d2503b915f3`  
		Last Modified: Thu, 11 Jun 2020 19:51:26 GMT  
		Size: 412.3 MB (412341899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be01ca6b29df6c87708fb4aadf7c0d4e9ec8644f2623cfde90f1446d78847513`  
		Last Modified: Thu, 11 Jun 2020 19:50:42 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1352273101d55a8a68733057ad6497baa7b56ff90b264ade51f9b97f7c92c4`  
		Last Modified: Thu, 11 Jun 2020 19:50:41 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7706c8ce70f1e3c1bb44ced94ca6e668ad9de0a05e89d689d8fed82cb6d02499`  
		Last Modified: Thu, 11 Jun 2020 19:50:41 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.4.0-rc9-bionic`

```console
$ docker pull mongo@sha256:c86ca7d3826a4a113dfa60ee1a5b215be979d4241bd01411f765fb58931637a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `mongo:4.4.0-rc9-bionic` - linux; amd64

```console
$ docker pull mongo@sha256:08a7438918614c7cb939c947bc471e687ac2e8485a7f1d6cb29f98d43650eb81
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.7 MB (177701947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ece36a7d4fb83f0867b7fe3de0923e2e70d0d8f8886191993685962fbf19bd4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:20:29 GMT
ADD file:1e8d02626176dc8141df3c0a1365774ce73d79934654fe24a4b1e7f173108232 in / 
# Wed, 17 Jun 2020 01:20:30 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:20:31 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:20:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:20:32 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 05:16:06 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 05:16:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 05:16:16 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 05:16:16 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 05:16:30 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 05:16:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 05:17:00 GMT
ENV GPG_KEYS=99DC630F00A2F97F27C6A02A253612A09571B484 20691EEC35216C63CAF66CE1656408E390CFB1F5 E162F504A20CDF15827F718D4B7C549A058F8B6B 9DA31620334BD75D9DCB49F368818C72E52529D4 2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Wed, 17 Jun 2020 05:17:01 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 05:17:01 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 05:17:01 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 05:17:02 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 05:17:02 GMT
ENV MONGO_MAJOR=testing
# Wed, 17 Jun 2020 05:17:02 GMT
ENV MONGO_VERSION=4.4.0~rc9
# Wed, 17 Jun 2020 05:17:03 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 05:17:23 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 05:17:26 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 05:17:26 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 05:17:26 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 05:17:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 05:17:27 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 05:17:27 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:d7c3167c320d7a820935f54cf4290890ea19567da496ecf774e8773b35d5f065`  
		Last Modified: Wed, 27 May 2020 12:21:15 GMT  
		Size: 26.7 MB (26688718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:131f805ec7fd68d45a887e2ef82de61de0247b4eb934ab03b7c933650e854baa`  
		Last Modified: Wed, 17 Jun 2020 01:21:41 GMT  
		Size: 35.4 KB (35369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322ed380e680a77f30528ba013e3a802a7b44948a0609c7d1d732dd46a9a310d`  
		Last Modified: Wed, 17 Jun 2020 01:21:41 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac240b130982ad1c3ba3188abbf18ba4e54bdd9e504ce2d5c2eff6d3e86b8dd`  
		Last Modified: Wed, 17 Jun 2020 01:21:41 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5704a01b59ff4d100b5bcc0244090cb5b369649b41a468a82cb5015afdc4f9d`  
		Last Modified: Wed, 17 Jun 2020 05:18:30 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e396e2a1e6820b238c82087b900e4f03e1304b30ee16a5341b0c6a2a9eec20e`  
		Last Modified: Wed, 17 Jun 2020 05:18:29 GMT  
		Size: 3.0 MB (2973543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:914fffcb1cc543f9e16861fe6d80fdaad26ea9c69ba952c73cb3db44a9cfc545`  
		Last Modified: Wed, 17 Jun 2020 05:18:30 GMT  
		Size: 5.8 MB (5823974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692bd0d35810fbf133d67af4f0ae0c627fb731b875d5370d3dfaa3f1a06392fa`  
		Last Modified: Wed, 17 Jun 2020 05:18:29 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ae4de9714c056e86d9925b9efc4d6be680aa04cfb1fd1dfd58bdb93dadffc5`  
		Last Modified: Wed, 17 Jun 2020 05:18:52 GMT  
		Size: 6.3 KB (6252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27913ee473ed41f8d48e523eac423b4627c2665aa164447d132f16dc2fbc65d`  
		Last Modified: Wed, 17 Jun 2020 05:18:52 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9274dbb221bc53f997714e90d3d95a7eed3786847bb400dddffa1e1fdf1f1e`  
		Last Modified: Wed, 17 Jun 2020 05:19:14 GMT  
		Size: 142.2 MB (142166762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c46635cb88709e9bad2966b953bb001762cebcd352bdc838d942364dbd55b8d`  
		Last Modified: Wed, 17 Jun 2020 05:18:52 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8bfa6aa4decd3c6d67bf9fe6d4762e1557c1e30c52e71884ce3476b05f614f`  
		Last Modified: Wed, 17 Jun 2020 05:18:52 GMT  
		Size: 4.0 KB (3950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.4.0-rc9-bionic` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:536a31542b7d3f9ba2dd78dcc7a53e83d4a37c2796ab4bbaecdd28a7a126eb5d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.7 MB (167661341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5a682f2ee63f45ab3382088349f51c0af8b9d20952a766d219656ec9ddf42c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:42:33 GMT
ADD file:7dc8819fd3d4b84ad19fb836e5bfda64a5ffefc371166f70d4d41dff6b22d450 in / 
# Wed, 17 Jun 2020 01:42:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:42:41 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:42:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:42:45 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:26:00 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 03:26:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:26:24 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:26:25 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 03:27:01 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:27:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:28:31 GMT
ENV GPG_KEYS=99DC630F00A2F97F27C6A02A253612A09571B484 20691EEC35216C63CAF66CE1656408E390CFB1F5 E162F504A20CDF15827F718D4B7C549A058F8B6B 9DA31620334BD75D9DCB49F368818C72E52529D4 2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Wed, 17 Jun 2020 03:28:34 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:28:36 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 03:28:39 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:28:41 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:28:42 GMT
ENV MONGO_MAJOR=testing
# Wed, 17 Jun 2020 03:28:43 GMT
ENV MONGO_VERSION=4.4.0~rc9
# Wed, 17 Jun 2020 03:28:46 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 03:29:24 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 03:29:27 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 03:29:28 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 03:29:29 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:29:31 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 03:29:33 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:2e8bea8b22f8f5a4fd5aa85019945dd8ae04f283a4ba2a7aeb4536fe2f1d1ec2`  
		Last Modified: Tue, 26 May 2020 16:25:25 GMT  
		Size: 23.7 MB (23721687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc90876b9c9a7343ae432eaec7c8dc8859c1e84b6193da8d386815fde165a70e`  
		Last Modified: Wed, 17 Jun 2020 01:44:48 GMT  
		Size: 35.2 KB (35192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bfc658a5210a9f0c9cfcda5f504e720da9268e9f3f3bf48e3a9a7af360c959`  
		Last Modified: Wed, 17 Jun 2020 01:44:49 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef0f1b06b2142ff2bf35cc565f019ed9e4efe0d8f332825167538c2337bac8a`  
		Last Modified: Wed, 17 Jun 2020 01:44:49 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79f4068e2fc9c5ce913c3640637c35584b72816ca9485c4bf5af0a22994d0f6`  
		Last Modified: Wed, 17 Jun 2020 03:31:11 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5678c55b212ca2ce4ea7b4092838653b706277000f57d7a18526f3df6cba283`  
		Last Modified: Wed, 17 Jun 2020 03:31:11 GMT  
		Size: 2.7 MB (2665976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509de0ccfb79a34de230a6fef2cfc900bdb35f1f7f583fc957b7c23b46439d4f`  
		Last Modified: Wed, 17 Jun 2020 03:31:12 GMT  
		Size: 5.3 MB (5345550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5493b54160873a149e08eedf09e74628680b1d5e8826b90672f04c88c30ccb`  
		Last Modified: Wed, 17 Jun 2020 03:31:10 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deafc22fb839309e0ff73d69148b1061567442476c00078e55fd8f2ca6fcd5c8`  
		Last Modified: Wed, 17 Jun 2020 03:31:47 GMT  
		Size: 6.3 KB (6253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6774a6455e0eda434f9817370afa1a8a0ae837302f9816494275f66238012ae2`  
		Last Modified: Wed, 17 Jun 2020 03:31:47 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7bd711f5ff0470496bfd97c7937c82ec2b9d5fa4ee3ded334f2a51d237ddbf`  
		Last Modified: Wed, 17 Jun 2020 03:32:25 GMT  
		Size: 135.9 MB (135879240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8898fe6b89326089621a29a76f81a23cc42d9fe5f809a53b67466040c474420`  
		Last Modified: Wed, 17 Jun 2020 03:31:47 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b178145b3f3d3bad498dbb2534db4a93ff08031a2d2d8b5b47fdf9d7e6fa45c6`  
		Last Modified: Wed, 17 Jun 2020 03:31:47 GMT  
		Size: 4.0 KB (3952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.4.0-rc9-bionic` - linux; s390x

```console
$ docker pull mongo@sha256:54151c9e8490a5ba1f294fb021b5fb2566dce18f481ac5ffae4d4311b2028d0b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.7 MB (172657780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1164e632ad52e2cf5eacf9312a565830950785edf24dbfac0186e9a12f174ee8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:41:48 GMT
ADD file:8708e93980b416070ba0bb024a7858748129059a85d2c771a4489c31710a9df1 in / 
# Wed, 17 Jun 2020 01:41:51 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:41:52 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:41:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:41:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:24:26 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 03:24:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:24:35 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:24:35 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 03:24:46 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:24:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:25:33 GMT
ENV GPG_KEYS=99DC630F00A2F97F27C6A02A253612A09571B484 20691EEC35216C63CAF66CE1656408E390CFB1F5 E162F504A20CDF15827F718D4B7C549A058F8B6B 9DA31620334BD75D9DCB49F368818C72E52529D4 2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Wed, 17 Jun 2020 03:25:34 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:25:34 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 03:25:34 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:25:34 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:25:35 GMT
ENV MONGO_MAJOR=testing
# Wed, 17 Jun 2020 03:25:35 GMT
ENV MONGO_VERSION=4.4.0~rc9
# Wed, 17 Jun 2020 03:25:35 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 03:28:23 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 03:28:28 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 03:28:29 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 03:28:29 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:28:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:28:29 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 03:28:30 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f3c26641772baa3348c0cce190edb38690a41f1824570c5c65cc363b42e5a5b5`  
		Last Modified: Sat, 30 May 2020 09:30:29 GMT  
		Size: 25.4 MB (25365846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf76fcee55454304ffbf9e321dda388a7e8de8a3916f854e1e588bc6c19b088`  
		Last Modified: Wed, 17 Jun 2020 01:42:56 GMT  
		Size: 36.2 KB (36165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5173e4f9f1868daa26021e1e701a000b0aadb2b611a487d089e7de4b728a7424`  
		Last Modified: Wed, 17 Jun 2020 01:42:56 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13da9fe451bd0f377d042d4bebef4ffd19163113e3e66dcd718fe187149a0dbd`  
		Last Modified: Wed, 17 Jun 2020 01:42:57 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d8fc9b1e9007ca5666c42ff8398a5227869b151fea1562c5e3cfb2188640e6`  
		Last Modified: Wed, 17 Jun 2020 03:28:52 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a889c8302a90f8884ff21edb649cf8dc1771453aca39505e61f29e053a1b64`  
		Last Modified: Wed, 17 Jun 2020 03:28:51 GMT  
		Size: 2.7 MB (2704483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:582fe8ee181790ce5fdadeef1c1cd7af40de0e8d2cb2e307fa05aed8d23a82b7`  
		Last Modified: Wed, 17 Jun 2020 03:28:50 GMT  
		Size: 5.7 MB (5745080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6096f1fa9fe7ad82ea015203f2410ac8b0831d0617db029aed54c698f84a2eaf`  
		Last Modified: Wed, 17 Jun 2020 03:28:50 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce8677aae44e31d383f2709bd3cc41ba2aeb459d07e6e05442802c8fe09b36c`  
		Last Modified: Wed, 17 Jun 2020 03:29:11 GMT  
		Size: 6.2 KB (6248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63fd6a4cab24edcfbee6d202c0a9e3ed0923dac53271f99942f0a7ab84ec83e7`  
		Last Modified: Wed, 17 Jun 2020 03:29:10 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3652237c6732d7d65cced49e7409ba137ea2273d6bd1c26028d3d2af7d56fddd`  
		Last Modified: Wed, 17 Jun 2020 03:29:28 GMT  
		Size: 138.8 MB (138792530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a223e5df98ceffef359a0bd07fe9327cf5f384a2ad7563899be68aa25a5006d5`  
		Last Modified: Wed, 17 Jun 2020 03:29:10 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddeaa0784e1dcec5ff0f75d4e2a824607e6bceca061e67fcdfd15ddc3249017b`  
		Last Modified: Wed, 17 Jun 2020 03:29:41 GMT  
		Size: 4.0 KB (3953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.4.0-rc9-windowsservercore`

```console
$ docker pull mongo@sha256:617152623d4f74d44e069e0d6b0d95dc9f0bd58d80aba3eba9c1c465ff03cbed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3750; amd64
	-	windows version 10.0.17763.1282; amd64

### `mongo:4.4.0-rc9-windowsservercore` - windows version 10.0.14393.3750; amd64

```console
$ docker pull mongo@sha256:215f1361466e6995d5a57effb6c461d42d7d7cfb19c4bae176999db59440ace6
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5784920267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec81dd11cfe596c69cd23bb0a3e6562beb0f5ea0e32111cffd56de47adef954`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 01 Jun 2020 18:53:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Jun 2020 12:52:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jun 2020 19:16:43 GMT
ENV MONGO_VERSION=4.4.0-rc9
# Thu, 11 Jun 2020 19:16:44 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.0-rc9-signed.msi
# Thu, 11 Jun 2020 19:16:45 GMT
ENV MONGO_DOWNLOAD_SHA256=efa1d75f19d03500deb895fcc67c8afd1ae4ebd347821673f3a54ba7af8ea63c
# Thu, 11 Jun 2020 19:30:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 11 Jun 2020 19:30:28 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 11 Jun 2020 19:30:30 GMT
EXPOSE 27017
# Thu, 11 Jun 2020 19:30:31 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:375fbabb84945635805b46a02a17ac15a3177bcaae7404cfab5f1ceb0460cb60`  
		Size: 1.7 GB (1664011795 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:30efe9163d37226b077b25cd93b088cebd2ddbaadf173d143b9fe0ddecaeae53`  
		Last Modified: Wed, 10 Jun 2020 15:34:41 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f722bab4d6f564851060c094083c229bc7e58ad34bb63f63adf236f9b42161`  
		Last Modified: Thu, 11 Jun 2020 19:50:23 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c119bfdf019d71f020a808c4f5bcc3f141c37923eb4df84b35c0d64d24255f5`  
		Last Modified: Thu, 11 Jun 2020 19:50:23 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88dd5ed82ce663bb0dd49f1ba28274c0dd50b21500e838a693bc6df493013993`  
		Last Modified: Thu, 11 Jun 2020 19:50:21 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319d5363e64c1103acb8013122be273969f0339da0b37ff3c524c4e93f184f92`  
		Last Modified: Thu, 11 Jun 2020 19:50:30 GMT  
		Size: 50.9 MB (50914489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3598bb59158e998723a319fc5452a711979f68fc439064076339b6acbf6509`  
		Last Modified: Thu, 11 Jun 2020 19:50:21 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a419ffdf45ea371482995436d267f646e75ab9d8eb38a9739a567c985054fb9c`  
		Last Modified: Thu, 11 Jun 2020 19:50:21 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca4bbbef218f58984237b6a3ac496ded351fdb00850abcaaf1bf39c4a586ddb`  
		Last Modified: Thu, 11 Jun 2020 19:50:21 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.4.0-rc9-windowsservercore` - windows version 10.0.17763.1282; amd64

```console
$ docker pull mongo@sha256:f205b8f1adaba4f302e4e08dfd199917ddfd027e22957dd466befddf99e6bfd9
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2706264212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2caf8fbd3bef0c6654b37c79bf354076d15dd8e6d83641a5b6cd129a982772ec`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Wed, 10 Jun 2020 12:43:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jun 2020 19:30:44 GMT
ENV MONGO_VERSION=4.4.0-rc9
# Thu, 11 Jun 2020 19:30:44 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.0-rc9-signed.msi
# Thu, 11 Jun 2020 19:30:45 GMT
ENV MONGO_DOWNLOAD_SHA256=efa1d75f19d03500deb895fcc67c8afd1ae4ebd347821673f3a54ba7af8ea63c
# Thu, 11 Jun 2020 19:49:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 11 Jun 2020 19:49:08 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 11 Jun 2020 19:49:09 GMT
EXPOSE 27017
# Thu, 11 Jun 2020 19:49:11 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b11029314f3c794dc51e43c915b3e62f6b44aeb96f84b8b92f453e61cf7a2cb3`  
		Last Modified: Wed, 10 Jun 2020 15:34:12 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599f6162438ec450553183469d80b7b2ae5da8231df1f927ab76bfddc4b3c0ce`  
		Last Modified: Thu, 11 Jun 2020 19:50:44 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e2f3d8d745162590cfa721fb659aaf0b0401d1247e77cf43ffae2c49cbce4fd`  
		Last Modified: Thu, 11 Jun 2020 19:50:44 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6066806f7a19d5d3b2f0bea4f42c11ea2f6d2ad1a29b05df6a23b5cba7e0c61`  
		Last Modified: Thu, 11 Jun 2020 19:50:42 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d062a956e06d65c5441f637a66d90250482f6d8f3c6685efb18c8d2503b915f3`  
		Last Modified: Thu, 11 Jun 2020 19:51:26 GMT  
		Size: 412.3 MB (412341899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be01ca6b29df6c87708fb4aadf7c0d4e9ec8644f2623cfde90f1446d78847513`  
		Last Modified: Thu, 11 Jun 2020 19:50:42 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1352273101d55a8a68733057ad6497baa7b56ff90b264ade51f9b97f7c92c4`  
		Last Modified: Thu, 11 Jun 2020 19:50:41 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7706c8ce70f1e3c1bb44ced94ca6e668ad9de0a05e89d689d8fed82cb6d02499`  
		Last Modified: Thu, 11 Jun 2020 19:50:41 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.4.0-rc9-windowsservercore-1809`

```console
$ docker pull mongo@sha256:c95ca3410e9bd64e03a9e52df6e500e5a2f49b561f1f8564be65040af575399d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1282; amd64

### `mongo:4.4.0-rc9-windowsservercore-1809` - windows version 10.0.17763.1282; amd64

```console
$ docker pull mongo@sha256:f205b8f1adaba4f302e4e08dfd199917ddfd027e22957dd466befddf99e6bfd9
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2706264212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2caf8fbd3bef0c6654b37c79bf354076d15dd8e6d83641a5b6cd129a982772ec`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Wed, 10 Jun 2020 12:43:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jun 2020 19:30:44 GMT
ENV MONGO_VERSION=4.4.0-rc9
# Thu, 11 Jun 2020 19:30:44 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.0-rc9-signed.msi
# Thu, 11 Jun 2020 19:30:45 GMT
ENV MONGO_DOWNLOAD_SHA256=efa1d75f19d03500deb895fcc67c8afd1ae4ebd347821673f3a54ba7af8ea63c
# Thu, 11 Jun 2020 19:49:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 11 Jun 2020 19:49:08 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 11 Jun 2020 19:49:09 GMT
EXPOSE 27017
# Thu, 11 Jun 2020 19:49:11 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b11029314f3c794dc51e43c915b3e62f6b44aeb96f84b8b92f453e61cf7a2cb3`  
		Last Modified: Wed, 10 Jun 2020 15:34:12 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599f6162438ec450553183469d80b7b2ae5da8231df1f927ab76bfddc4b3c0ce`  
		Last Modified: Thu, 11 Jun 2020 19:50:44 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e2f3d8d745162590cfa721fb659aaf0b0401d1247e77cf43ffae2c49cbce4fd`  
		Last Modified: Thu, 11 Jun 2020 19:50:44 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6066806f7a19d5d3b2f0bea4f42c11ea2f6d2ad1a29b05df6a23b5cba7e0c61`  
		Last Modified: Thu, 11 Jun 2020 19:50:42 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d062a956e06d65c5441f637a66d90250482f6d8f3c6685efb18c8d2503b915f3`  
		Last Modified: Thu, 11 Jun 2020 19:51:26 GMT  
		Size: 412.3 MB (412341899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be01ca6b29df6c87708fb4aadf7c0d4e9ec8644f2623cfde90f1446d78847513`  
		Last Modified: Thu, 11 Jun 2020 19:50:42 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1352273101d55a8a68733057ad6497baa7b56ff90b264ade51f9b97f7c92c4`  
		Last Modified: Thu, 11 Jun 2020 19:50:41 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7706c8ce70f1e3c1bb44ced94ca6e668ad9de0a05e89d689d8fed82cb6d02499`  
		Last Modified: Thu, 11 Jun 2020 19:50:41 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.4.0-rc9-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:5afd912fc4b63c5845eb6538190be33bd2b62f848f1d4761ef82a65c7b798948
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3750; amd64

### `mongo:4.4.0-rc9-windowsservercore-ltsc2016` - windows version 10.0.14393.3750; amd64

```console
$ docker pull mongo@sha256:215f1361466e6995d5a57effb6c461d42d7d7cfb19c4bae176999db59440ace6
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5784920267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec81dd11cfe596c69cd23bb0a3e6562beb0f5ea0e32111cffd56de47adef954`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 01 Jun 2020 18:53:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Jun 2020 12:52:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jun 2020 19:16:43 GMT
ENV MONGO_VERSION=4.4.0-rc9
# Thu, 11 Jun 2020 19:16:44 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.0-rc9-signed.msi
# Thu, 11 Jun 2020 19:16:45 GMT
ENV MONGO_DOWNLOAD_SHA256=efa1d75f19d03500deb895fcc67c8afd1ae4ebd347821673f3a54ba7af8ea63c
# Thu, 11 Jun 2020 19:30:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 11 Jun 2020 19:30:28 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 11 Jun 2020 19:30:30 GMT
EXPOSE 27017
# Thu, 11 Jun 2020 19:30:31 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:375fbabb84945635805b46a02a17ac15a3177bcaae7404cfab5f1ceb0460cb60`  
		Size: 1.7 GB (1664011795 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:30efe9163d37226b077b25cd93b088cebd2ddbaadf173d143b9fe0ddecaeae53`  
		Last Modified: Wed, 10 Jun 2020 15:34:41 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f722bab4d6f564851060c094083c229bc7e58ad34bb63f63adf236f9b42161`  
		Last Modified: Thu, 11 Jun 2020 19:50:23 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c119bfdf019d71f020a808c4f5bcc3f141c37923eb4df84b35c0d64d24255f5`  
		Last Modified: Thu, 11 Jun 2020 19:50:23 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88dd5ed82ce663bb0dd49f1ba28274c0dd50b21500e838a693bc6df493013993`  
		Last Modified: Thu, 11 Jun 2020 19:50:21 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319d5363e64c1103acb8013122be273969f0339da0b37ff3c524c4e93f184f92`  
		Last Modified: Thu, 11 Jun 2020 19:50:30 GMT  
		Size: 50.9 MB (50914489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3598bb59158e998723a319fc5452a711979f68fc439064076339b6acbf6509`  
		Last Modified: Thu, 11 Jun 2020 19:50:21 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a419ffdf45ea371482995436d267f646e75ab9d8eb38a9739a567c985054fb9c`  
		Last Modified: Thu, 11 Jun 2020 19:50:21 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca4bbbef218f58984237b6a3ac496ded351fdb00850abcaaf1bf39c4a586ddb`  
		Last Modified: Thu, 11 Jun 2020 19:50:21 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.4-rc`

```console
$ docker pull mongo@sha256:d253a81dc8c13b3fe94b2b1b8fd1c763c8dd19503702df6ce3e02a6bcff84a09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x
	-	windows version 10.0.14393.3750; amd64
	-	windows version 10.0.17763.1282; amd64

### `mongo:4.4-rc` - linux; amd64

```console
$ docker pull mongo@sha256:08a7438918614c7cb939c947bc471e687ac2e8485a7f1d6cb29f98d43650eb81
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.7 MB (177701947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ece36a7d4fb83f0867b7fe3de0923e2e70d0d8f8886191993685962fbf19bd4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:20:29 GMT
ADD file:1e8d02626176dc8141df3c0a1365774ce73d79934654fe24a4b1e7f173108232 in / 
# Wed, 17 Jun 2020 01:20:30 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:20:31 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:20:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:20:32 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 05:16:06 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 05:16:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 05:16:16 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 05:16:16 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 05:16:30 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 05:16:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 05:17:00 GMT
ENV GPG_KEYS=99DC630F00A2F97F27C6A02A253612A09571B484 20691EEC35216C63CAF66CE1656408E390CFB1F5 E162F504A20CDF15827F718D4B7C549A058F8B6B 9DA31620334BD75D9DCB49F368818C72E52529D4 2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Wed, 17 Jun 2020 05:17:01 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 05:17:01 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 05:17:01 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 05:17:02 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 05:17:02 GMT
ENV MONGO_MAJOR=testing
# Wed, 17 Jun 2020 05:17:02 GMT
ENV MONGO_VERSION=4.4.0~rc9
# Wed, 17 Jun 2020 05:17:03 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 05:17:23 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 05:17:26 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 05:17:26 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 05:17:26 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 05:17:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 05:17:27 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 05:17:27 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:d7c3167c320d7a820935f54cf4290890ea19567da496ecf774e8773b35d5f065`  
		Last Modified: Wed, 27 May 2020 12:21:15 GMT  
		Size: 26.7 MB (26688718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:131f805ec7fd68d45a887e2ef82de61de0247b4eb934ab03b7c933650e854baa`  
		Last Modified: Wed, 17 Jun 2020 01:21:41 GMT  
		Size: 35.4 KB (35369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322ed380e680a77f30528ba013e3a802a7b44948a0609c7d1d732dd46a9a310d`  
		Last Modified: Wed, 17 Jun 2020 01:21:41 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac240b130982ad1c3ba3188abbf18ba4e54bdd9e504ce2d5c2eff6d3e86b8dd`  
		Last Modified: Wed, 17 Jun 2020 01:21:41 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5704a01b59ff4d100b5bcc0244090cb5b369649b41a468a82cb5015afdc4f9d`  
		Last Modified: Wed, 17 Jun 2020 05:18:30 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e396e2a1e6820b238c82087b900e4f03e1304b30ee16a5341b0c6a2a9eec20e`  
		Last Modified: Wed, 17 Jun 2020 05:18:29 GMT  
		Size: 3.0 MB (2973543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:914fffcb1cc543f9e16861fe6d80fdaad26ea9c69ba952c73cb3db44a9cfc545`  
		Last Modified: Wed, 17 Jun 2020 05:18:30 GMT  
		Size: 5.8 MB (5823974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692bd0d35810fbf133d67af4f0ae0c627fb731b875d5370d3dfaa3f1a06392fa`  
		Last Modified: Wed, 17 Jun 2020 05:18:29 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ae4de9714c056e86d9925b9efc4d6be680aa04cfb1fd1dfd58bdb93dadffc5`  
		Last Modified: Wed, 17 Jun 2020 05:18:52 GMT  
		Size: 6.3 KB (6252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27913ee473ed41f8d48e523eac423b4627c2665aa164447d132f16dc2fbc65d`  
		Last Modified: Wed, 17 Jun 2020 05:18:52 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9274dbb221bc53f997714e90d3d95a7eed3786847bb400dddffa1e1fdf1f1e`  
		Last Modified: Wed, 17 Jun 2020 05:19:14 GMT  
		Size: 142.2 MB (142166762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c46635cb88709e9bad2966b953bb001762cebcd352bdc838d942364dbd55b8d`  
		Last Modified: Wed, 17 Jun 2020 05:18:52 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8bfa6aa4decd3c6d67bf9fe6d4762e1557c1e30c52e71884ce3476b05f614f`  
		Last Modified: Wed, 17 Jun 2020 05:18:52 GMT  
		Size: 4.0 KB (3950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.4-rc` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:536a31542b7d3f9ba2dd78dcc7a53e83d4a37c2796ab4bbaecdd28a7a126eb5d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.7 MB (167661341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5a682f2ee63f45ab3382088349f51c0af8b9d20952a766d219656ec9ddf42c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:42:33 GMT
ADD file:7dc8819fd3d4b84ad19fb836e5bfda64a5ffefc371166f70d4d41dff6b22d450 in / 
# Wed, 17 Jun 2020 01:42:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:42:41 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:42:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:42:45 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:26:00 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 03:26:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:26:24 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:26:25 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 03:27:01 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:27:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:28:31 GMT
ENV GPG_KEYS=99DC630F00A2F97F27C6A02A253612A09571B484 20691EEC35216C63CAF66CE1656408E390CFB1F5 E162F504A20CDF15827F718D4B7C549A058F8B6B 9DA31620334BD75D9DCB49F368818C72E52529D4 2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Wed, 17 Jun 2020 03:28:34 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:28:36 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 03:28:39 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:28:41 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:28:42 GMT
ENV MONGO_MAJOR=testing
# Wed, 17 Jun 2020 03:28:43 GMT
ENV MONGO_VERSION=4.4.0~rc9
# Wed, 17 Jun 2020 03:28:46 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 03:29:24 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 03:29:27 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 03:29:28 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 03:29:29 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:29:31 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 03:29:33 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:2e8bea8b22f8f5a4fd5aa85019945dd8ae04f283a4ba2a7aeb4536fe2f1d1ec2`  
		Last Modified: Tue, 26 May 2020 16:25:25 GMT  
		Size: 23.7 MB (23721687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc90876b9c9a7343ae432eaec7c8dc8859c1e84b6193da8d386815fde165a70e`  
		Last Modified: Wed, 17 Jun 2020 01:44:48 GMT  
		Size: 35.2 KB (35192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bfc658a5210a9f0c9cfcda5f504e720da9268e9f3f3bf48e3a9a7af360c959`  
		Last Modified: Wed, 17 Jun 2020 01:44:49 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef0f1b06b2142ff2bf35cc565f019ed9e4efe0d8f332825167538c2337bac8a`  
		Last Modified: Wed, 17 Jun 2020 01:44:49 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79f4068e2fc9c5ce913c3640637c35584b72816ca9485c4bf5af0a22994d0f6`  
		Last Modified: Wed, 17 Jun 2020 03:31:11 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5678c55b212ca2ce4ea7b4092838653b706277000f57d7a18526f3df6cba283`  
		Last Modified: Wed, 17 Jun 2020 03:31:11 GMT  
		Size: 2.7 MB (2665976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509de0ccfb79a34de230a6fef2cfc900bdb35f1f7f583fc957b7c23b46439d4f`  
		Last Modified: Wed, 17 Jun 2020 03:31:12 GMT  
		Size: 5.3 MB (5345550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5493b54160873a149e08eedf09e74628680b1d5e8826b90672f04c88c30ccb`  
		Last Modified: Wed, 17 Jun 2020 03:31:10 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deafc22fb839309e0ff73d69148b1061567442476c00078e55fd8f2ca6fcd5c8`  
		Last Modified: Wed, 17 Jun 2020 03:31:47 GMT  
		Size: 6.3 KB (6253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6774a6455e0eda434f9817370afa1a8a0ae837302f9816494275f66238012ae2`  
		Last Modified: Wed, 17 Jun 2020 03:31:47 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7bd711f5ff0470496bfd97c7937c82ec2b9d5fa4ee3ded334f2a51d237ddbf`  
		Last Modified: Wed, 17 Jun 2020 03:32:25 GMT  
		Size: 135.9 MB (135879240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8898fe6b89326089621a29a76f81a23cc42d9fe5f809a53b67466040c474420`  
		Last Modified: Wed, 17 Jun 2020 03:31:47 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b178145b3f3d3bad498dbb2534db4a93ff08031a2d2d8b5b47fdf9d7e6fa45c6`  
		Last Modified: Wed, 17 Jun 2020 03:31:47 GMT  
		Size: 4.0 KB (3952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.4-rc` - linux; s390x

```console
$ docker pull mongo@sha256:54151c9e8490a5ba1f294fb021b5fb2566dce18f481ac5ffae4d4311b2028d0b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.7 MB (172657780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1164e632ad52e2cf5eacf9312a565830950785edf24dbfac0186e9a12f174ee8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:41:48 GMT
ADD file:8708e93980b416070ba0bb024a7858748129059a85d2c771a4489c31710a9df1 in / 
# Wed, 17 Jun 2020 01:41:51 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:41:52 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:41:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:41:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:24:26 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 03:24:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:24:35 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:24:35 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 03:24:46 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:24:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:25:33 GMT
ENV GPG_KEYS=99DC630F00A2F97F27C6A02A253612A09571B484 20691EEC35216C63CAF66CE1656408E390CFB1F5 E162F504A20CDF15827F718D4B7C549A058F8B6B 9DA31620334BD75D9DCB49F368818C72E52529D4 2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Wed, 17 Jun 2020 03:25:34 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:25:34 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 03:25:34 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:25:34 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:25:35 GMT
ENV MONGO_MAJOR=testing
# Wed, 17 Jun 2020 03:25:35 GMT
ENV MONGO_VERSION=4.4.0~rc9
# Wed, 17 Jun 2020 03:25:35 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 03:28:23 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 03:28:28 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 03:28:29 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 03:28:29 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:28:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:28:29 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 03:28:30 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f3c26641772baa3348c0cce190edb38690a41f1824570c5c65cc363b42e5a5b5`  
		Last Modified: Sat, 30 May 2020 09:30:29 GMT  
		Size: 25.4 MB (25365846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf76fcee55454304ffbf9e321dda388a7e8de8a3916f854e1e588bc6c19b088`  
		Last Modified: Wed, 17 Jun 2020 01:42:56 GMT  
		Size: 36.2 KB (36165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5173e4f9f1868daa26021e1e701a000b0aadb2b611a487d089e7de4b728a7424`  
		Last Modified: Wed, 17 Jun 2020 01:42:56 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13da9fe451bd0f377d042d4bebef4ffd19163113e3e66dcd718fe187149a0dbd`  
		Last Modified: Wed, 17 Jun 2020 01:42:57 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d8fc9b1e9007ca5666c42ff8398a5227869b151fea1562c5e3cfb2188640e6`  
		Last Modified: Wed, 17 Jun 2020 03:28:52 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a889c8302a90f8884ff21edb649cf8dc1771453aca39505e61f29e053a1b64`  
		Last Modified: Wed, 17 Jun 2020 03:28:51 GMT  
		Size: 2.7 MB (2704483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:582fe8ee181790ce5fdadeef1c1cd7af40de0e8d2cb2e307fa05aed8d23a82b7`  
		Last Modified: Wed, 17 Jun 2020 03:28:50 GMT  
		Size: 5.7 MB (5745080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6096f1fa9fe7ad82ea015203f2410ac8b0831d0617db029aed54c698f84a2eaf`  
		Last Modified: Wed, 17 Jun 2020 03:28:50 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce8677aae44e31d383f2709bd3cc41ba2aeb459d07e6e05442802c8fe09b36c`  
		Last Modified: Wed, 17 Jun 2020 03:29:11 GMT  
		Size: 6.2 KB (6248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63fd6a4cab24edcfbee6d202c0a9e3ed0923dac53271f99942f0a7ab84ec83e7`  
		Last Modified: Wed, 17 Jun 2020 03:29:10 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3652237c6732d7d65cced49e7409ba137ea2273d6bd1c26028d3d2af7d56fddd`  
		Last Modified: Wed, 17 Jun 2020 03:29:28 GMT  
		Size: 138.8 MB (138792530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a223e5df98ceffef359a0bd07fe9327cf5f384a2ad7563899be68aa25a5006d5`  
		Last Modified: Wed, 17 Jun 2020 03:29:10 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddeaa0784e1dcec5ff0f75d4e2a824607e6bceca061e67fcdfd15ddc3249017b`  
		Last Modified: Wed, 17 Jun 2020 03:29:41 GMT  
		Size: 4.0 KB (3953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.4-rc` - windows version 10.0.14393.3750; amd64

```console
$ docker pull mongo@sha256:215f1361466e6995d5a57effb6c461d42d7d7cfb19c4bae176999db59440ace6
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5784920267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec81dd11cfe596c69cd23bb0a3e6562beb0f5ea0e32111cffd56de47adef954`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 01 Jun 2020 18:53:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Jun 2020 12:52:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jun 2020 19:16:43 GMT
ENV MONGO_VERSION=4.4.0-rc9
# Thu, 11 Jun 2020 19:16:44 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.0-rc9-signed.msi
# Thu, 11 Jun 2020 19:16:45 GMT
ENV MONGO_DOWNLOAD_SHA256=efa1d75f19d03500deb895fcc67c8afd1ae4ebd347821673f3a54ba7af8ea63c
# Thu, 11 Jun 2020 19:30:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 11 Jun 2020 19:30:28 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 11 Jun 2020 19:30:30 GMT
EXPOSE 27017
# Thu, 11 Jun 2020 19:30:31 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:375fbabb84945635805b46a02a17ac15a3177bcaae7404cfab5f1ceb0460cb60`  
		Size: 1.7 GB (1664011795 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:30efe9163d37226b077b25cd93b088cebd2ddbaadf173d143b9fe0ddecaeae53`  
		Last Modified: Wed, 10 Jun 2020 15:34:41 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f722bab4d6f564851060c094083c229bc7e58ad34bb63f63adf236f9b42161`  
		Last Modified: Thu, 11 Jun 2020 19:50:23 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c119bfdf019d71f020a808c4f5bcc3f141c37923eb4df84b35c0d64d24255f5`  
		Last Modified: Thu, 11 Jun 2020 19:50:23 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88dd5ed82ce663bb0dd49f1ba28274c0dd50b21500e838a693bc6df493013993`  
		Last Modified: Thu, 11 Jun 2020 19:50:21 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319d5363e64c1103acb8013122be273969f0339da0b37ff3c524c4e93f184f92`  
		Last Modified: Thu, 11 Jun 2020 19:50:30 GMT  
		Size: 50.9 MB (50914489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3598bb59158e998723a319fc5452a711979f68fc439064076339b6acbf6509`  
		Last Modified: Thu, 11 Jun 2020 19:50:21 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a419ffdf45ea371482995436d267f646e75ab9d8eb38a9739a567c985054fb9c`  
		Last Modified: Thu, 11 Jun 2020 19:50:21 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca4bbbef218f58984237b6a3ac496ded351fdb00850abcaaf1bf39c4a586ddb`  
		Last Modified: Thu, 11 Jun 2020 19:50:21 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.4-rc` - windows version 10.0.17763.1282; amd64

```console
$ docker pull mongo@sha256:f205b8f1adaba4f302e4e08dfd199917ddfd027e22957dd466befddf99e6bfd9
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2706264212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2caf8fbd3bef0c6654b37c79bf354076d15dd8e6d83641a5b6cd129a982772ec`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Wed, 10 Jun 2020 12:43:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jun 2020 19:30:44 GMT
ENV MONGO_VERSION=4.4.0-rc9
# Thu, 11 Jun 2020 19:30:44 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.0-rc9-signed.msi
# Thu, 11 Jun 2020 19:30:45 GMT
ENV MONGO_DOWNLOAD_SHA256=efa1d75f19d03500deb895fcc67c8afd1ae4ebd347821673f3a54ba7af8ea63c
# Thu, 11 Jun 2020 19:49:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 11 Jun 2020 19:49:08 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 11 Jun 2020 19:49:09 GMT
EXPOSE 27017
# Thu, 11 Jun 2020 19:49:11 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b11029314f3c794dc51e43c915b3e62f6b44aeb96f84b8b92f453e61cf7a2cb3`  
		Last Modified: Wed, 10 Jun 2020 15:34:12 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599f6162438ec450553183469d80b7b2ae5da8231df1f927ab76bfddc4b3c0ce`  
		Last Modified: Thu, 11 Jun 2020 19:50:44 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e2f3d8d745162590cfa721fb659aaf0b0401d1247e77cf43ffae2c49cbce4fd`  
		Last Modified: Thu, 11 Jun 2020 19:50:44 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6066806f7a19d5d3b2f0bea4f42c11ea2f6d2ad1a29b05df6a23b5cba7e0c61`  
		Last Modified: Thu, 11 Jun 2020 19:50:42 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d062a956e06d65c5441f637a66d90250482f6d8f3c6685efb18c8d2503b915f3`  
		Last Modified: Thu, 11 Jun 2020 19:51:26 GMT  
		Size: 412.3 MB (412341899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be01ca6b29df6c87708fb4aadf7c0d4e9ec8644f2623cfde90f1446d78847513`  
		Last Modified: Thu, 11 Jun 2020 19:50:42 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1352273101d55a8a68733057ad6497baa7b56ff90b264ade51f9b97f7c92c4`  
		Last Modified: Thu, 11 Jun 2020 19:50:41 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7706c8ce70f1e3c1bb44ced94ca6e668ad9de0a05e89d689d8fed82cb6d02499`  
		Last Modified: Thu, 11 Jun 2020 19:50:41 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.4-rc-bionic`

```console
$ docker pull mongo@sha256:c86ca7d3826a4a113dfa60ee1a5b215be979d4241bd01411f765fb58931637a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `mongo:4.4-rc-bionic` - linux; amd64

```console
$ docker pull mongo@sha256:08a7438918614c7cb939c947bc471e687ac2e8485a7f1d6cb29f98d43650eb81
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.7 MB (177701947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ece36a7d4fb83f0867b7fe3de0923e2e70d0d8f8886191993685962fbf19bd4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:20:29 GMT
ADD file:1e8d02626176dc8141df3c0a1365774ce73d79934654fe24a4b1e7f173108232 in / 
# Wed, 17 Jun 2020 01:20:30 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:20:31 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:20:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:20:32 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 05:16:06 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 05:16:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 05:16:16 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 05:16:16 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 05:16:30 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 05:16:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 05:17:00 GMT
ENV GPG_KEYS=99DC630F00A2F97F27C6A02A253612A09571B484 20691EEC35216C63CAF66CE1656408E390CFB1F5 E162F504A20CDF15827F718D4B7C549A058F8B6B 9DA31620334BD75D9DCB49F368818C72E52529D4 2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Wed, 17 Jun 2020 05:17:01 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 05:17:01 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 05:17:01 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 05:17:02 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 05:17:02 GMT
ENV MONGO_MAJOR=testing
# Wed, 17 Jun 2020 05:17:02 GMT
ENV MONGO_VERSION=4.4.0~rc9
# Wed, 17 Jun 2020 05:17:03 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 05:17:23 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 05:17:26 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 05:17:26 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 05:17:26 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 05:17:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 05:17:27 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 05:17:27 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:d7c3167c320d7a820935f54cf4290890ea19567da496ecf774e8773b35d5f065`  
		Last Modified: Wed, 27 May 2020 12:21:15 GMT  
		Size: 26.7 MB (26688718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:131f805ec7fd68d45a887e2ef82de61de0247b4eb934ab03b7c933650e854baa`  
		Last Modified: Wed, 17 Jun 2020 01:21:41 GMT  
		Size: 35.4 KB (35369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322ed380e680a77f30528ba013e3a802a7b44948a0609c7d1d732dd46a9a310d`  
		Last Modified: Wed, 17 Jun 2020 01:21:41 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac240b130982ad1c3ba3188abbf18ba4e54bdd9e504ce2d5c2eff6d3e86b8dd`  
		Last Modified: Wed, 17 Jun 2020 01:21:41 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5704a01b59ff4d100b5bcc0244090cb5b369649b41a468a82cb5015afdc4f9d`  
		Last Modified: Wed, 17 Jun 2020 05:18:30 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e396e2a1e6820b238c82087b900e4f03e1304b30ee16a5341b0c6a2a9eec20e`  
		Last Modified: Wed, 17 Jun 2020 05:18:29 GMT  
		Size: 3.0 MB (2973543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:914fffcb1cc543f9e16861fe6d80fdaad26ea9c69ba952c73cb3db44a9cfc545`  
		Last Modified: Wed, 17 Jun 2020 05:18:30 GMT  
		Size: 5.8 MB (5823974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692bd0d35810fbf133d67af4f0ae0c627fb731b875d5370d3dfaa3f1a06392fa`  
		Last Modified: Wed, 17 Jun 2020 05:18:29 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ae4de9714c056e86d9925b9efc4d6be680aa04cfb1fd1dfd58bdb93dadffc5`  
		Last Modified: Wed, 17 Jun 2020 05:18:52 GMT  
		Size: 6.3 KB (6252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27913ee473ed41f8d48e523eac423b4627c2665aa164447d132f16dc2fbc65d`  
		Last Modified: Wed, 17 Jun 2020 05:18:52 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9274dbb221bc53f997714e90d3d95a7eed3786847bb400dddffa1e1fdf1f1e`  
		Last Modified: Wed, 17 Jun 2020 05:19:14 GMT  
		Size: 142.2 MB (142166762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c46635cb88709e9bad2966b953bb001762cebcd352bdc838d942364dbd55b8d`  
		Last Modified: Wed, 17 Jun 2020 05:18:52 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8bfa6aa4decd3c6d67bf9fe6d4762e1557c1e30c52e71884ce3476b05f614f`  
		Last Modified: Wed, 17 Jun 2020 05:18:52 GMT  
		Size: 4.0 KB (3950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.4-rc-bionic` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:536a31542b7d3f9ba2dd78dcc7a53e83d4a37c2796ab4bbaecdd28a7a126eb5d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.7 MB (167661341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5a682f2ee63f45ab3382088349f51c0af8b9d20952a766d219656ec9ddf42c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:42:33 GMT
ADD file:7dc8819fd3d4b84ad19fb836e5bfda64a5ffefc371166f70d4d41dff6b22d450 in / 
# Wed, 17 Jun 2020 01:42:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:42:41 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:42:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:42:45 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:26:00 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 03:26:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:26:24 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:26:25 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 03:27:01 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:27:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:28:31 GMT
ENV GPG_KEYS=99DC630F00A2F97F27C6A02A253612A09571B484 20691EEC35216C63CAF66CE1656408E390CFB1F5 E162F504A20CDF15827F718D4B7C549A058F8B6B 9DA31620334BD75D9DCB49F368818C72E52529D4 2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Wed, 17 Jun 2020 03:28:34 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:28:36 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 03:28:39 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:28:41 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:28:42 GMT
ENV MONGO_MAJOR=testing
# Wed, 17 Jun 2020 03:28:43 GMT
ENV MONGO_VERSION=4.4.0~rc9
# Wed, 17 Jun 2020 03:28:46 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 03:29:24 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 03:29:27 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 03:29:28 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 03:29:29 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:29:31 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 03:29:33 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:2e8bea8b22f8f5a4fd5aa85019945dd8ae04f283a4ba2a7aeb4536fe2f1d1ec2`  
		Last Modified: Tue, 26 May 2020 16:25:25 GMT  
		Size: 23.7 MB (23721687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc90876b9c9a7343ae432eaec7c8dc8859c1e84b6193da8d386815fde165a70e`  
		Last Modified: Wed, 17 Jun 2020 01:44:48 GMT  
		Size: 35.2 KB (35192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bfc658a5210a9f0c9cfcda5f504e720da9268e9f3f3bf48e3a9a7af360c959`  
		Last Modified: Wed, 17 Jun 2020 01:44:49 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef0f1b06b2142ff2bf35cc565f019ed9e4efe0d8f332825167538c2337bac8a`  
		Last Modified: Wed, 17 Jun 2020 01:44:49 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79f4068e2fc9c5ce913c3640637c35584b72816ca9485c4bf5af0a22994d0f6`  
		Last Modified: Wed, 17 Jun 2020 03:31:11 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5678c55b212ca2ce4ea7b4092838653b706277000f57d7a18526f3df6cba283`  
		Last Modified: Wed, 17 Jun 2020 03:31:11 GMT  
		Size: 2.7 MB (2665976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509de0ccfb79a34de230a6fef2cfc900bdb35f1f7f583fc957b7c23b46439d4f`  
		Last Modified: Wed, 17 Jun 2020 03:31:12 GMT  
		Size: 5.3 MB (5345550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5493b54160873a149e08eedf09e74628680b1d5e8826b90672f04c88c30ccb`  
		Last Modified: Wed, 17 Jun 2020 03:31:10 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deafc22fb839309e0ff73d69148b1061567442476c00078e55fd8f2ca6fcd5c8`  
		Last Modified: Wed, 17 Jun 2020 03:31:47 GMT  
		Size: 6.3 KB (6253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6774a6455e0eda434f9817370afa1a8a0ae837302f9816494275f66238012ae2`  
		Last Modified: Wed, 17 Jun 2020 03:31:47 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7bd711f5ff0470496bfd97c7937c82ec2b9d5fa4ee3ded334f2a51d237ddbf`  
		Last Modified: Wed, 17 Jun 2020 03:32:25 GMT  
		Size: 135.9 MB (135879240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8898fe6b89326089621a29a76f81a23cc42d9fe5f809a53b67466040c474420`  
		Last Modified: Wed, 17 Jun 2020 03:31:47 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b178145b3f3d3bad498dbb2534db4a93ff08031a2d2d8b5b47fdf9d7e6fa45c6`  
		Last Modified: Wed, 17 Jun 2020 03:31:47 GMT  
		Size: 4.0 KB (3952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.4-rc-bionic` - linux; s390x

```console
$ docker pull mongo@sha256:54151c9e8490a5ba1f294fb021b5fb2566dce18f481ac5ffae4d4311b2028d0b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.7 MB (172657780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1164e632ad52e2cf5eacf9312a565830950785edf24dbfac0186e9a12f174ee8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:41:48 GMT
ADD file:8708e93980b416070ba0bb024a7858748129059a85d2c771a4489c31710a9df1 in / 
# Wed, 17 Jun 2020 01:41:51 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:41:52 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:41:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:41:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:24:26 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 03:24:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:24:35 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:24:35 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 03:24:46 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:24:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:25:33 GMT
ENV GPG_KEYS=99DC630F00A2F97F27C6A02A253612A09571B484 20691EEC35216C63CAF66CE1656408E390CFB1F5 E162F504A20CDF15827F718D4B7C549A058F8B6B 9DA31620334BD75D9DCB49F368818C72E52529D4 2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
# Wed, 17 Jun 2020 03:25:34 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:25:34 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 03:25:34 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:25:34 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:25:35 GMT
ENV MONGO_MAJOR=testing
# Wed, 17 Jun 2020 03:25:35 GMT
ENV MONGO_VERSION=4.4.0~rc9
# Wed, 17 Jun 2020 03:25:35 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 03:28:23 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 03:28:28 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 03:28:29 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 03:28:29 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:28:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:28:29 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 03:28:30 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f3c26641772baa3348c0cce190edb38690a41f1824570c5c65cc363b42e5a5b5`  
		Last Modified: Sat, 30 May 2020 09:30:29 GMT  
		Size: 25.4 MB (25365846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf76fcee55454304ffbf9e321dda388a7e8de8a3916f854e1e588bc6c19b088`  
		Last Modified: Wed, 17 Jun 2020 01:42:56 GMT  
		Size: 36.2 KB (36165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5173e4f9f1868daa26021e1e701a000b0aadb2b611a487d089e7de4b728a7424`  
		Last Modified: Wed, 17 Jun 2020 01:42:56 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13da9fe451bd0f377d042d4bebef4ffd19163113e3e66dcd718fe187149a0dbd`  
		Last Modified: Wed, 17 Jun 2020 01:42:57 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d8fc9b1e9007ca5666c42ff8398a5227869b151fea1562c5e3cfb2188640e6`  
		Last Modified: Wed, 17 Jun 2020 03:28:52 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a889c8302a90f8884ff21edb649cf8dc1771453aca39505e61f29e053a1b64`  
		Last Modified: Wed, 17 Jun 2020 03:28:51 GMT  
		Size: 2.7 MB (2704483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:582fe8ee181790ce5fdadeef1c1cd7af40de0e8d2cb2e307fa05aed8d23a82b7`  
		Last Modified: Wed, 17 Jun 2020 03:28:50 GMT  
		Size: 5.7 MB (5745080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6096f1fa9fe7ad82ea015203f2410ac8b0831d0617db029aed54c698f84a2eaf`  
		Last Modified: Wed, 17 Jun 2020 03:28:50 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce8677aae44e31d383f2709bd3cc41ba2aeb459d07e6e05442802c8fe09b36c`  
		Last Modified: Wed, 17 Jun 2020 03:29:11 GMT  
		Size: 6.2 KB (6248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63fd6a4cab24edcfbee6d202c0a9e3ed0923dac53271f99942f0a7ab84ec83e7`  
		Last Modified: Wed, 17 Jun 2020 03:29:10 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3652237c6732d7d65cced49e7409ba137ea2273d6bd1c26028d3d2af7d56fddd`  
		Last Modified: Wed, 17 Jun 2020 03:29:28 GMT  
		Size: 138.8 MB (138792530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a223e5df98ceffef359a0bd07fe9327cf5f384a2ad7563899be68aa25a5006d5`  
		Last Modified: Wed, 17 Jun 2020 03:29:10 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddeaa0784e1dcec5ff0f75d4e2a824607e6bceca061e67fcdfd15ddc3249017b`  
		Last Modified: Wed, 17 Jun 2020 03:29:41 GMT  
		Size: 4.0 KB (3953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.4-rc-windowsservercore`

```console
$ docker pull mongo@sha256:617152623d4f74d44e069e0d6b0d95dc9f0bd58d80aba3eba9c1c465ff03cbed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3750; amd64
	-	windows version 10.0.17763.1282; amd64

### `mongo:4.4-rc-windowsservercore` - windows version 10.0.14393.3750; amd64

```console
$ docker pull mongo@sha256:215f1361466e6995d5a57effb6c461d42d7d7cfb19c4bae176999db59440ace6
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5784920267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec81dd11cfe596c69cd23bb0a3e6562beb0f5ea0e32111cffd56de47adef954`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 01 Jun 2020 18:53:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Jun 2020 12:52:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jun 2020 19:16:43 GMT
ENV MONGO_VERSION=4.4.0-rc9
# Thu, 11 Jun 2020 19:16:44 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.0-rc9-signed.msi
# Thu, 11 Jun 2020 19:16:45 GMT
ENV MONGO_DOWNLOAD_SHA256=efa1d75f19d03500deb895fcc67c8afd1ae4ebd347821673f3a54ba7af8ea63c
# Thu, 11 Jun 2020 19:30:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 11 Jun 2020 19:30:28 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 11 Jun 2020 19:30:30 GMT
EXPOSE 27017
# Thu, 11 Jun 2020 19:30:31 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:375fbabb84945635805b46a02a17ac15a3177bcaae7404cfab5f1ceb0460cb60`  
		Size: 1.7 GB (1664011795 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:30efe9163d37226b077b25cd93b088cebd2ddbaadf173d143b9fe0ddecaeae53`  
		Last Modified: Wed, 10 Jun 2020 15:34:41 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f722bab4d6f564851060c094083c229bc7e58ad34bb63f63adf236f9b42161`  
		Last Modified: Thu, 11 Jun 2020 19:50:23 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c119bfdf019d71f020a808c4f5bcc3f141c37923eb4df84b35c0d64d24255f5`  
		Last Modified: Thu, 11 Jun 2020 19:50:23 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88dd5ed82ce663bb0dd49f1ba28274c0dd50b21500e838a693bc6df493013993`  
		Last Modified: Thu, 11 Jun 2020 19:50:21 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319d5363e64c1103acb8013122be273969f0339da0b37ff3c524c4e93f184f92`  
		Last Modified: Thu, 11 Jun 2020 19:50:30 GMT  
		Size: 50.9 MB (50914489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3598bb59158e998723a319fc5452a711979f68fc439064076339b6acbf6509`  
		Last Modified: Thu, 11 Jun 2020 19:50:21 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a419ffdf45ea371482995436d267f646e75ab9d8eb38a9739a567c985054fb9c`  
		Last Modified: Thu, 11 Jun 2020 19:50:21 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca4bbbef218f58984237b6a3ac496ded351fdb00850abcaaf1bf39c4a586ddb`  
		Last Modified: Thu, 11 Jun 2020 19:50:21 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4.4-rc-windowsservercore` - windows version 10.0.17763.1282; amd64

```console
$ docker pull mongo@sha256:f205b8f1adaba4f302e4e08dfd199917ddfd027e22957dd466befddf99e6bfd9
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2706264212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2caf8fbd3bef0c6654b37c79bf354076d15dd8e6d83641a5b6cd129a982772ec`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Wed, 10 Jun 2020 12:43:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jun 2020 19:30:44 GMT
ENV MONGO_VERSION=4.4.0-rc9
# Thu, 11 Jun 2020 19:30:44 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.0-rc9-signed.msi
# Thu, 11 Jun 2020 19:30:45 GMT
ENV MONGO_DOWNLOAD_SHA256=efa1d75f19d03500deb895fcc67c8afd1ae4ebd347821673f3a54ba7af8ea63c
# Thu, 11 Jun 2020 19:49:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 11 Jun 2020 19:49:08 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 11 Jun 2020 19:49:09 GMT
EXPOSE 27017
# Thu, 11 Jun 2020 19:49:11 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b11029314f3c794dc51e43c915b3e62f6b44aeb96f84b8b92f453e61cf7a2cb3`  
		Last Modified: Wed, 10 Jun 2020 15:34:12 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599f6162438ec450553183469d80b7b2ae5da8231df1f927ab76bfddc4b3c0ce`  
		Last Modified: Thu, 11 Jun 2020 19:50:44 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e2f3d8d745162590cfa721fb659aaf0b0401d1247e77cf43ffae2c49cbce4fd`  
		Last Modified: Thu, 11 Jun 2020 19:50:44 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6066806f7a19d5d3b2f0bea4f42c11ea2f6d2ad1a29b05df6a23b5cba7e0c61`  
		Last Modified: Thu, 11 Jun 2020 19:50:42 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d062a956e06d65c5441f637a66d90250482f6d8f3c6685efb18c8d2503b915f3`  
		Last Modified: Thu, 11 Jun 2020 19:51:26 GMT  
		Size: 412.3 MB (412341899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be01ca6b29df6c87708fb4aadf7c0d4e9ec8644f2623cfde90f1446d78847513`  
		Last Modified: Thu, 11 Jun 2020 19:50:42 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1352273101d55a8a68733057ad6497baa7b56ff90b264ade51f9b97f7c92c4`  
		Last Modified: Thu, 11 Jun 2020 19:50:41 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7706c8ce70f1e3c1bb44ced94ca6e668ad9de0a05e89d689d8fed82cb6d02499`  
		Last Modified: Thu, 11 Jun 2020 19:50:41 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.4-rc-windowsservercore-1809`

```console
$ docker pull mongo@sha256:c95ca3410e9bd64e03a9e52df6e500e5a2f49b561f1f8564be65040af575399d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1282; amd64

### `mongo:4.4-rc-windowsservercore-1809` - windows version 10.0.17763.1282; amd64

```console
$ docker pull mongo@sha256:f205b8f1adaba4f302e4e08dfd199917ddfd027e22957dd466befddf99e6bfd9
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2706264212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2caf8fbd3bef0c6654b37c79bf354076d15dd8e6d83641a5b6cd129a982772ec`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Wed, 10 Jun 2020 12:43:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jun 2020 19:30:44 GMT
ENV MONGO_VERSION=4.4.0-rc9
# Thu, 11 Jun 2020 19:30:44 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.0-rc9-signed.msi
# Thu, 11 Jun 2020 19:30:45 GMT
ENV MONGO_DOWNLOAD_SHA256=efa1d75f19d03500deb895fcc67c8afd1ae4ebd347821673f3a54ba7af8ea63c
# Thu, 11 Jun 2020 19:49:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 11 Jun 2020 19:49:08 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 11 Jun 2020 19:49:09 GMT
EXPOSE 27017
# Thu, 11 Jun 2020 19:49:11 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b11029314f3c794dc51e43c915b3e62f6b44aeb96f84b8b92f453e61cf7a2cb3`  
		Last Modified: Wed, 10 Jun 2020 15:34:12 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599f6162438ec450553183469d80b7b2ae5da8231df1f927ab76bfddc4b3c0ce`  
		Last Modified: Thu, 11 Jun 2020 19:50:44 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e2f3d8d745162590cfa721fb659aaf0b0401d1247e77cf43ffae2c49cbce4fd`  
		Last Modified: Thu, 11 Jun 2020 19:50:44 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6066806f7a19d5d3b2f0bea4f42c11ea2f6d2ad1a29b05df6a23b5cba7e0c61`  
		Last Modified: Thu, 11 Jun 2020 19:50:42 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d062a956e06d65c5441f637a66d90250482f6d8f3c6685efb18c8d2503b915f3`  
		Last Modified: Thu, 11 Jun 2020 19:51:26 GMT  
		Size: 412.3 MB (412341899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be01ca6b29df6c87708fb4aadf7c0d4e9ec8644f2623cfde90f1446d78847513`  
		Last Modified: Thu, 11 Jun 2020 19:50:42 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1352273101d55a8a68733057ad6497baa7b56ff90b264ade51f9b97f7c92c4`  
		Last Modified: Thu, 11 Jun 2020 19:50:41 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7706c8ce70f1e3c1bb44ced94ca6e668ad9de0a05e89d689d8fed82cb6d02499`  
		Last Modified: Thu, 11 Jun 2020 19:50:41 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4.4-rc-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:5afd912fc4b63c5845eb6538190be33bd2b62f848f1d4761ef82a65c7b798948
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3750; amd64

### `mongo:4.4-rc-windowsservercore-ltsc2016` - windows version 10.0.14393.3750; amd64

```console
$ docker pull mongo@sha256:215f1361466e6995d5a57effb6c461d42d7d7cfb19c4bae176999db59440ace6
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5784920267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec81dd11cfe596c69cd23bb0a3e6562beb0f5ea0e32111cffd56de47adef954`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 01 Jun 2020 18:53:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Jun 2020 12:52:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jun 2020 19:16:43 GMT
ENV MONGO_VERSION=4.4.0-rc9
# Thu, 11 Jun 2020 19:16:44 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.0-rc9-signed.msi
# Thu, 11 Jun 2020 19:16:45 GMT
ENV MONGO_DOWNLOAD_SHA256=efa1d75f19d03500deb895fcc67c8afd1ae4ebd347821673f3a54ba7af8ea63c
# Thu, 11 Jun 2020 19:30:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 11 Jun 2020 19:30:28 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 11 Jun 2020 19:30:30 GMT
EXPOSE 27017
# Thu, 11 Jun 2020 19:30:31 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:375fbabb84945635805b46a02a17ac15a3177bcaae7404cfab5f1ceb0460cb60`  
		Size: 1.7 GB (1664011795 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:30efe9163d37226b077b25cd93b088cebd2ddbaadf173d143b9fe0ddecaeae53`  
		Last Modified: Wed, 10 Jun 2020 15:34:41 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f722bab4d6f564851060c094083c229bc7e58ad34bb63f63adf236f9b42161`  
		Last Modified: Thu, 11 Jun 2020 19:50:23 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c119bfdf019d71f020a808c4f5bcc3f141c37923eb4df84b35c0d64d24255f5`  
		Last Modified: Thu, 11 Jun 2020 19:50:23 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88dd5ed82ce663bb0dd49f1ba28274c0dd50b21500e838a693bc6df493013993`  
		Last Modified: Thu, 11 Jun 2020 19:50:21 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319d5363e64c1103acb8013122be273969f0339da0b37ff3c524c4e93f184f92`  
		Last Modified: Thu, 11 Jun 2020 19:50:30 GMT  
		Size: 50.9 MB (50914489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3598bb59158e998723a319fc5452a711979f68fc439064076339b6acbf6509`  
		Last Modified: Thu, 11 Jun 2020 19:50:21 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a419ffdf45ea371482995436d267f646e75ab9d8eb38a9739a567c985054fb9c`  
		Last Modified: Thu, 11 Jun 2020 19:50:21 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca4bbbef218f58984237b6a3ac496ded351fdb00850abcaaf1bf39c4a586ddb`  
		Last Modified: Thu, 11 Jun 2020 19:50:21 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4-bionic`

```console
$ docker pull mongo@sha256:6bf46291247789c85932f35b2e824158e0f04771fb551aea10e3e7e86c349326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `mongo:4-bionic` - linux; amd64

```console
$ docker pull mongo@sha256:ed04fcf28fccf1bb2c295074775a24ddd007e14ca522ae97a56983f269cad163
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164652387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2cc1f48aed02a160b0447fd28b75952ed1d2df8c66693733d4954483734e44`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:20:29 GMT
ADD file:1e8d02626176dc8141df3c0a1365774ce73d79934654fe24a4b1e7f173108232 in / 
# Wed, 17 Jun 2020 01:20:30 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:20:31 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:20:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:20:32 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 05:16:06 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 05:16:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 05:16:16 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 05:16:16 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 05:16:30 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 05:16:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 05:16:33 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Wed, 17 Jun 2020 05:16:34 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 05:16:34 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 05:16:34 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 05:16:34 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 05:16:34 GMT
ENV MONGO_MAJOR=4.2
# Wed, 17 Jun 2020 05:16:35 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 17 Jun 2020 05:16:35 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 05:16:53 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 05:16:54 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 05:16:54 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 05:16:54 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 05:16:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 05:16:55 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 05:16:55 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:d7c3167c320d7a820935f54cf4290890ea19567da496ecf774e8773b35d5f065`  
		Last Modified: Wed, 27 May 2020 12:21:15 GMT  
		Size: 26.7 MB (26688718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:131f805ec7fd68d45a887e2ef82de61de0247b4eb934ab03b7c933650e854baa`  
		Last Modified: Wed, 17 Jun 2020 01:21:41 GMT  
		Size: 35.4 KB (35369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322ed380e680a77f30528ba013e3a802a7b44948a0609c7d1d732dd46a9a310d`  
		Last Modified: Wed, 17 Jun 2020 01:21:41 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac240b130982ad1c3ba3188abbf18ba4e54bdd9e504ce2d5c2eff6d3e86b8dd`  
		Last Modified: Wed, 17 Jun 2020 01:21:41 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5704a01b59ff4d100b5bcc0244090cb5b369649b41a468a82cb5015afdc4f9d`  
		Last Modified: Wed, 17 Jun 2020 05:18:30 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e396e2a1e6820b238c82087b900e4f03e1304b30ee16a5341b0c6a2a9eec20e`  
		Last Modified: Wed, 17 Jun 2020 05:18:29 GMT  
		Size: 3.0 MB (2973543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:914fffcb1cc543f9e16861fe6d80fdaad26ea9c69ba952c73cb3db44a9cfc545`  
		Last Modified: Wed, 17 Jun 2020 05:18:30 GMT  
		Size: 5.8 MB (5823974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692bd0d35810fbf133d67af4f0ae0c627fb731b875d5370d3dfaa3f1a06392fa`  
		Last Modified: Wed, 17 Jun 2020 05:18:29 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122d231765e47cbdd1b934b3ee55ffa291b76b17e4134be5b6e9837c52053c9e`  
		Last Modified: Wed, 17 Jun 2020 05:18:28 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9c497305ce2ee80e9d80fb69dcf2766f51b6b23e093fbf9d0d837b14376810`  
		Last Modified: Wed, 17 Jun 2020 05:18:28 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e3ca7a65fcd8d5d002ae04e06a5d7b900020097dec64e04923b9fa25d7d633`  
		Last Modified: Wed, 17 Jun 2020 05:18:46 GMT  
		Size: 129.1 MB (129122023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70e0d9672b4cbcef6ddbaa3fae90fb8181aeb83b59cac8f4910d69f7c359f96`  
		Last Modified: Wed, 17 Jun 2020 05:18:28 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc04aade5db18c8ca826bfaef542aa9b48f2b3045dfe7a4fa0d4f11714d37a1`  
		Last Modified: Wed, 17 Jun 2020 05:18:28 GMT  
		Size: 4.0 KB (3955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-bionic` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:cdec0bd28e60bc06892f9972803753d57fdc3d4bcff657b694ba7f35b80d3d02
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154677642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f84af28ce3aa3b7b04964d7f7ee9eb0ae10e3c19e684ad29ceeca55c605f2924`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:42:33 GMT
ADD file:7dc8819fd3d4b84ad19fb836e5bfda64a5ffefc371166f70d4d41dff6b22d450 in / 
# Wed, 17 Jun 2020 01:42:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:42:41 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:42:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:42:45 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:26:00 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 03:26:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:26:24 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:26:25 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 03:27:01 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:27:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:27:06 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Wed, 17 Jun 2020 03:27:10 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:27:12 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 03:27:13 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:27:16 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:27:19 GMT
ENV MONGO_MAJOR=4.2
# Wed, 17 Jun 2020 03:27:20 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 17 Jun 2020 03:27:23 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 03:27:58 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 03:28:02 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 03:28:04 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 03:28:05 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:28:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:28:08 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 03:28:09 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:2e8bea8b22f8f5a4fd5aa85019945dd8ae04f283a4ba2a7aeb4536fe2f1d1ec2`  
		Last Modified: Tue, 26 May 2020 16:25:25 GMT  
		Size: 23.7 MB (23721687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc90876b9c9a7343ae432eaec7c8dc8859c1e84b6193da8d386815fde165a70e`  
		Last Modified: Wed, 17 Jun 2020 01:44:48 GMT  
		Size: 35.2 KB (35192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bfc658a5210a9f0c9cfcda5f504e720da9268e9f3f3bf48e3a9a7af360c959`  
		Last Modified: Wed, 17 Jun 2020 01:44:49 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef0f1b06b2142ff2bf35cc565f019ed9e4efe0d8f332825167538c2337bac8a`  
		Last Modified: Wed, 17 Jun 2020 01:44:49 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79f4068e2fc9c5ce913c3640637c35584b72816ca9485c4bf5af0a22994d0f6`  
		Last Modified: Wed, 17 Jun 2020 03:31:11 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5678c55b212ca2ce4ea7b4092838653b706277000f57d7a18526f3df6cba283`  
		Last Modified: Wed, 17 Jun 2020 03:31:11 GMT  
		Size: 2.7 MB (2665976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509de0ccfb79a34de230a6fef2cfc900bdb35f1f7f583fc957b7c23b46439d4f`  
		Last Modified: Wed, 17 Jun 2020 03:31:12 GMT  
		Size: 5.3 MB (5345550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5493b54160873a149e08eedf09e74628680b1d5e8826b90672f04c88c30ccb`  
		Last Modified: Wed, 17 Jun 2020 03:31:10 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe2b58fe1082de604f779b26f7bac0f685326b5584f5a43457f1d51effdca86`  
		Last Modified: Wed, 17 Jun 2020 03:31:09 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52cb618aa3e851b5a35792b706fd4e70901c2e3fd1faa3fcf12d719ac3d8ff1`  
		Last Modified: Wed, 17 Jun 2020 03:31:08 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8985f89f29dd85eccbd8da50a080817fa846f7b7baee89e54e83f79559fff4b`  
		Last Modified: Wed, 17 Jun 2020 03:31:35 GMT  
		Size: 122.9 MB (122900361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f01ca57315b3f1a9469f85034d0f072b2d67b5ee9d3c9d2e14e3487df4db4d`  
		Last Modified: Wed, 17 Jun 2020 03:31:08 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f414fc1b8d9a096289a531b03096d4af7478a1c627842175a15974cb041c879`  
		Last Modified: Wed, 17 Jun 2020 03:31:08 GMT  
		Size: 4.0 KB (3950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-bionic` - linux; s390x

```console
$ docker pull mongo@sha256:e1c13c3ee8ae7031fdaa1e4cb645de3279a46ccf47511a9fb4b82c90d5c831f5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160598470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddfb01efb7ddfe0ac3ea40d0ded51ac1742d89e522b72b9ca43ec82ac2a642b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:41:48 GMT
ADD file:8708e93980b416070ba0bb024a7858748129059a85d2c771a4489c31710a9df1 in / 
# Wed, 17 Jun 2020 01:41:51 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:41:52 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:41:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:41:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:24:26 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 03:24:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:24:35 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:24:35 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 03:24:46 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:24:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:24:47 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Wed, 17 Jun 2020 03:24:48 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:24:48 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 03:24:48 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:24:48 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:24:48 GMT
ENV MONGO_MAJOR=4.2
# Wed, 17 Jun 2020 03:24:49 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 17 Jun 2020 03:24:49 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 03:25:14 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 03:25:18 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 03:25:18 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 03:25:19 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:25:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:25:19 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 03:25:19 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f3c26641772baa3348c0cce190edb38690a41f1824570c5c65cc363b42e5a5b5`  
		Last Modified: Sat, 30 May 2020 09:30:29 GMT  
		Size: 25.4 MB (25365846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf76fcee55454304ffbf9e321dda388a7e8de8a3916f854e1e588bc6c19b088`  
		Last Modified: Wed, 17 Jun 2020 01:42:56 GMT  
		Size: 36.2 KB (36165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5173e4f9f1868daa26021e1e701a000b0aadb2b611a487d089e7de4b728a7424`  
		Last Modified: Wed, 17 Jun 2020 01:42:56 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13da9fe451bd0f377d042d4bebef4ffd19163113e3e66dcd718fe187149a0dbd`  
		Last Modified: Wed, 17 Jun 2020 01:42:57 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d8fc9b1e9007ca5666c42ff8398a5227869b151fea1562c5e3cfb2188640e6`  
		Last Modified: Wed, 17 Jun 2020 03:28:52 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a889c8302a90f8884ff21edb649cf8dc1771453aca39505e61f29e053a1b64`  
		Last Modified: Wed, 17 Jun 2020 03:28:51 GMT  
		Size: 2.7 MB (2704483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:582fe8ee181790ce5fdadeef1c1cd7af40de0e8d2cb2e307fa05aed8d23a82b7`  
		Last Modified: Wed, 17 Jun 2020 03:28:50 GMT  
		Size: 5.7 MB (5745080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6096f1fa9fe7ad82ea015203f2410ac8b0831d0617db029aed54c698f84a2eaf`  
		Last Modified: Wed, 17 Jun 2020 03:28:50 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2bddaa2c78c2b5ac010b9af305db894e7bb616461499b863fe6af05c42bb502`  
		Last Modified: Wed, 17 Jun 2020 03:28:48 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b0ea0902452b7fe6fc59cc6001683eb80ddf80ba9fa1a59f83a576855317e12`  
		Last Modified: Wed, 17 Jun 2020 03:28:48 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507e67f4e596fea4d40f10e6ca9132a57d472a59bef2ce47ae79b92eb029ca7a`  
		Last Modified: Wed, 17 Jun 2020 03:29:02 GMT  
		Size: 126.7 MB (126738040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf93b294dbde6159d09390ee7231284abcaad59049a9d10eaebfc46619d4ad3`  
		Last Modified: Wed, 17 Jun 2020 03:28:48 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e514b21a3b45674ce414ecd79bf6adc339e8ea02fc1a80956ece983f3192be`  
		Last Modified: Wed, 17 Jun 2020 03:29:03 GMT  
		Size: 4.0 KB (3953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4-windowsservercore`

```console
$ docker pull mongo@sha256:3dfacb1c248e30392bcfaba258677f7a057a4ea96b2a37de4839a01081742a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3750; amd64
	-	windows version 10.0.17763.1282; amd64

### `mongo:4-windowsservercore` - windows version 10.0.14393.3750; amd64

```console
$ docker pull mongo@sha256:af38590235375eb1218ddd651e660f1a6e6e6a882842e7b428f2d55d46cc937a
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6193023222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aaf2b53fe9e096da5ab6f4ae0e34caf7cf3de0a336bd9576cee60752c37c17b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 01 Jun 2020 18:53:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Jun 2020 12:52:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 17 Jun 2020 00:50:43 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 17 Jun 2020 00:50:44 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 17 Jun 2020 00:50:45 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 17 Jun 2020 01:08:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 17 Jun 2020 01:08:52 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 17 Jun 2020 01:08:53 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 01:08:54 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:375fbabb84945635805b46a02a17ac15a3177bcaae7404cfab5f1ceb0460cb60`  
		Size: 1.7 GB (1664011795 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:30efe9163d37226b077b25cd93b088cebd2ddbaadf173d143b9fe0ddecaeae53`  
		Last Modified: Wed, 10 Jun 2020 15:34:41 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b60479ef88c8a931aeeffaa74d289fbbf204229adb6a20c54d51456f70bb75`  
		Last Modified: Wed, 17 Jun 2020 01:32:04 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52bb592e6eb6512ccf1127b0311263697d559599357972414f4b776277bd628f`  
		Last Modified: Wed, 17 Jun 2020 01:32:04 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e57b55cda98f10b8c536232f9fd5fbc19c778c4043edc4fea012972832bb4570`  
		Last Modified: Wed, 17 Jun 2020 01:32:01 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eaad7a52f6dc4a311c3e724f9b5fe27f7af849fa6229fe21fc0490976fcb607`  
		Last Modified: Wed, 17 Jun 2020 01:32:57 GMT  
		Size: 459.0 MB (459017760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187b8e518ef05e3f4e7348e0ca7fef3e05414c63661223d63d83a36367ff9605`  
		Last Modified: Wed, 17 Jun 2020 01:32:01 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58773855217e4f81876fd21fd13a61d94d0f5a191e7025ce2bf26469077e330c`  
		Last Modified: Wed, 17 Jun 2020 01:32:01 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e25f1762a4dcad6fd6709c2602e0d459a0efb6aea6e10e16cb78796c27e496d`  
		Last Modified: Wed, 17 Jun 2020 01:32:01 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-windowsservercore` - windows version 10.0.17763.1282; amd64

```console
$ docker pull mongo@sha256:a332d0d55bcb861ab664609d4ee8b7a3c7481e800fa5ad62009c671c1673af0b
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2752054828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86c12ab59b3d8850d880c02f06724769d7955a42bb4c5b10fd9a16cb6ad19f7`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Wed, 10 Jun 2020 12:43:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 17 Jun 2020 01:09:02 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 17 Jun 2020 01:09:03 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 17 Jun 2020 01:09:04 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 17 Jun 2020 01:28:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 17 Jun 2020 01:28:16 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 17 Jun 2020 01:28:18 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 01:28:19 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b11029314f3c794dc51e43c915b3e62f6b44aeb96f84b8b92f453e61cf7a2cb3`  
		Last Modified: Wed, 10 Jun 2020 15:34:12 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f51df57f2cb6ccc03b57cbd044ee4a49d9383489feb3872da465ba8b6bffa89`  
		Last Modified: Wed, 17 Jun 2020 01:33:19 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84353c49610a99480bfb74a8769e7446bbd898b8644c25d2b8c645c7a2e90e0e`  
		Last Modified: Wed, 17 Jun 2020 01:33:18 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c19d206596ed0cd1b7da30ba6e637be1d4c31dc398ca6f4d30d583593e31705`  
		Last Modified: Wed, 17 Jun 2020 01:33:16 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90fa0f2b93199d15d0678aa8a13db7d1470a5ce7ddb94ec8fa93a75156cce44`  
		Last Modified: Wed, 17 Jun 2020 01:34:14 GMT  
		Size: 458.1 MB (458132610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:369180762b76f75c56ed85ad59e938011c514ad32b51a43cbb6d5fcce885b5d1`  
		Last Modified: Wed, 17 Jun 2020 01:33:16 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f9c110c11f811446f2204714562c02b6eefeeb1cae671aa73af5e4cc7dfbd0`  
		Last Modified: Wed, 17 Jun 2020 01:33:16 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c7a275e52c9eafb08caf7a861ef21a725b77ee54c1b867ddb4b4da99814dd7`  
		Last Modified: Wed, 17 Jun 2020 01:33:16 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4-windowsservercore-1809`

```console
$ docker pull mongo@sha256:bc2bc28a30754135707bfc25dd73c4aceb4ae89c943a243433b0b3f321f640fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1282; amd64

### `mongo:4-windowsservercore-1809` - windows version 10.0.17763.1282; amd64

```console
$ docker pull mongo@sha256:a332d0d55bcb861ab664609d4ee8b7a3c7481e800fa5ad62009c671c1673af0b
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2752054828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86c12ab59b3d8850d880c02f06724769d7955a42bb4c5b10fd9a16cb6ad19f7`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Wed, 10 Jun 2020 12:43:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 17 Jun 2020 01:09:02 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 17 Jun 2020 01:09:03 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 17 Jun 2020 01:09:04 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 17 Jun 2020 01:28:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 17 Jun 2020 01:28:16 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 17 Jun 2020 01:28:18 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 01:28:19 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b11029314f3c794dc51e43c915b3e62f6b44aeb96f84b8b92f453e61cf7a2cb3`  
		Last Modified: Wed, 10 Jun 2020 15:34:12 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f51df57f2cb6ccc03b57cbd044ee4a49d9383489feb3872da465ba8b6bffa89`  
		Last Modified: Wed, 17 Jun 2020 01:33:19 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84353c49610a99480bfb74a8769e7446bbd898b8644c25d2b8c645c7a2e90e0e`  
		Last Modified: Wed, 17 Jun 2020 01:33:18 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c19d206596ed0cd1b7da30ba6e637be1d4c31dc398ca6f4d30d583593e31705`  
		Last Modified: Wed, 17 Jun 2020 01:33:16 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90fa0f2b93199d15d0678aa8a13db7d1470a5ce7ddb94ec8fa93a75156cce44`  
		Last Modified: Wed, 17 Jun 2020 01:34:14 GMT  
		Size: 458.1 MB (458132610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:369180762b76f75c56ed85ad59e938011c514ad32b51a43cbb6d5fcce885b5d1`  
		Last Modified: Wed, 17 Jun 2020 01:33:16 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f9c110c11f811446f2204714562c02b6eefeeb1cae671aa73af5e4cc7dfbd0`  
		Last Modified: Wed, 17 Jun 2020 01:33:16 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c7a275e52c9eafb08caf7a861ef21a725b77ee54c1b867ddb4b4da99814dd7`  
		Last Modified: Wed, 17 Jun 2020 01:33:16 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:4-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:9b6e497bdcaa3a451d4296f944c0a13ac07344a7879cb41fb387ae288308fc61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3750; amd64

### `mongo:4-windowsservercore-ltsc2016` - windows version 10.0.14393.3750; amd64

```console
$ docker pull mongo@sha256:af38590235375eb1218ddd651e660f1a6e6e6a882842e7b428f2d55d46cc937a
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6193023222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aaf2b53fe9e096da5ab6f4ae0e34caf7cf3de0a336bd9576cee60752c37c17b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 01 Jun 2020 18:53:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Jun 2020 12:52:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 17 Jun 2020 00:50:43 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 17 Jun 2020 00:50:44 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 17 Jun 2020 00:50:45 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 17 Jun 2020 01:08:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 17 Jun 2020 01:08:52 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 17 Jun 2020 01:08:53 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 01:08:54 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:375fbabb84945635805b46a02a17ac15a3177bcaae7404cfab5f1ceb0460cb60`  
		Size: 1.7 GB (1664011795 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:30efe9163d37226b077b25cd93b088cebd2ddbaadf173d143b9fe0ddecaeae53`  
		Last Modified: Wed, 10 Jun 2020 15:34:41 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b60479ef88c8a931aeeffaa74d289fbbf204229adb6a20c54d51456f70bb75`  
		Last Modified: Wed, 17 Jun 2020 01:32:04 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52bb592e6eb6512ccf1127b0311263697d559599357972414f4b776277bd628f`  
		Last Modified: Wed, 17 Jun 2020 01:32:04 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e57b55cda98f10b8c536232f9fd5fbc19c778c4043edc4fea012972832bb4570`  
		Last Modified: Wed, 17 Jun 2020 01:32:01 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eaad7a52f6dc4a311c3e724f9b5fe27f7af849fa6229fe21fc0490976fcb607`  
		Last Modified: Wed, 17 Jun 2020 01:32:57 GMT  
		Size: 459.0 MB (459017760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187b8e518ef05e3f4e7348e0ca7fef3e05414c63661223d63d83a36367ff9605`  
		Last Modified: Wed, 17 Jun 2020 01:32:01 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58773855217e4f81876fd21fd13a61d94d0f5a191e7025ce2bf26469077e330c`  
		Last Modified: Wed, 17 Jun 2020 01:32:01 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e25f1762a4dcad6fd6709c2602e0d459a0efb6aea6e10e16cb78796c27e496d`  
		Last Modified: Wed, 17 Jun 2020 01:32:01 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:bionic`

```console
$ docker pull mongo@sha256:6bf46291247789c85932f35b2e824158e0f04771fb551aea10e3e7e86c349326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `mongo:bionic` - linux; amd64

```console
$ docker pull mongo@sha256:ed04fcf28fccf1bb2c295074775a24ddd007e14ca522ae97a56983f269cad163
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164652387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2cc1f48aed02a160b0447fd28b75952ed1d2df8c66693733d4954483734e44`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:20:29 GMT
ADD file:1e8d02626176dc8141df3c0a1365774ce73d79934654fe24a4b1e7f173108232 in / 
# Wed, 17 Jun 2020 01:20:30 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:20:31 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:20:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:20:32 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 05:16:06 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 05:16:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 05:16:16 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 05:16:16 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 05:16:30 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 05:16:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 05:16:33 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Wed, 17 Jun 2020 05:16:34 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 05:16:34 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 05:16:34 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 05:16:34 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 05:16:34 GMT
ENV MONGO_MAJOR=4.2
# Wed, 17 Jun 2020 05:16:35 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 17 Jun 2020 05:16:35 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 05:16:53 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 05:16:54 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 05:16:54 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 05:16:54 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 05:16:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 05:16:55 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 05:16:55 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:d7c3167c320d7a820935f54cf4290890ea19567da496ecf774e8773b35d5f065`  
		Last Modified: Wed, 27 May 2020 12:21:15 GMT  
		Size: 26.7 MB (26688718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:131f805ec7fd68d45a887e2ef82de61de0247b4eb934ab03b7c933650e854baa`  
		Last Modified: Wed, 17 Jun 2020 01:21:41 GMT  
		Size: 35.4 KB (35369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322ed380e680a77f30528ba013e3a802a7b44948a0609c7d1d732dd46a9a310d`  
		Last Modified: Wed, 17 Jun 2020 01:21:41 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac240b130982ad1c3ba3188abbf18ba4e54bdd9e504ce2d5c2eff6d3e86b8dd`  
		Last Modified: Wed, 17 Jun 2020 01:21:41 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5704a01b59ff4d100b5bcc0244090cb5b369649b41a468a82cb5015afdc4f9d`  
		Last Modified: Wed, 17 Jun 2020 05:18:30 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e396e2a1e6820b238c82087b900e4f03e1304b30ee16a5341b0c6a2a9eec20e`  
		Last Modified: Wed, 17 Jun 2020 05:18:29 GMT  
		Size: 3.0 MB (2973543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:914fffcb1cc543f9e16861fe6d80fdaad26ea9c69ba952c73cb3db44a9cfc545`  
		Last Modified: Wed, 17 Jun 2020 05:18:30 GMT  
		Size: 5.8 MB (5823974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692bd0d35810fbf133d67af4f0ae0c627fb731b875d5370d3dfaa3f1a06392fa`  
		Last Modified: Wed, 17 Jun 2020 05:18:29 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122d231765e47cbdd1b934b3ee55ffa291b76b17e4134be5b6e9837c52053c9e`  
		Last Modified: Wed, 17 Jun 2020 05:18:28 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9c497305ce2ee80e9d80fb69dcf2766f51b6b23e093fbf9d0d837b14376810`  
		Last Modified: Wed, 17 Jun 2020 05:18:28 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e3ca7a65fcd8d5d002ae04e06a5d7b900020097dec64e04923b9fa25d7d633`  
		Last Modified: Wed, 17 Jun 2020 05:18:46 GMT  
		Size: 129.1 MB (129122023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70e0d9672b4cbcef6ddbaa3fae90fb8181aeb83b59cac8f4910d69f7c359f96`  
		Last Modified: Wed, 17 Jun 2020 05:18:28 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc04aade5db18c8ca826bfaef542aa9b48f2b3045dfe7a4fa0d4f11714d37a1`  
		Last Modified: Wed, 17 Jun 2020 05:18:28 GMT  
		Size: 4.0 KB (3955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:bionic` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:cdec0bd28e60bc06892f9972803753d57fdc3d4bcff657b694ba7f35b80d3d02
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154677642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f84af28ce3aa3b7b04964d7f7ee9eb0ae10e3c19e684ad29ceeca55c605f2924`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:42:33 GMT
ADD file:7dc8819fd3d4b84ad19fb836e5bfda64a5ffefc371166f70d4d41dff6b22d450 in / 
# Wed, 17 Jun 2020 01:42:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:42:41 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:42:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:42:45 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:26:00 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 03:26:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:26:24 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:26:25 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 03:27:01 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:27:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:27:06 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Wed, 17 Jun 2020 03:27:10 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:27:12 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 03:27:13 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:27:16 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:27:19 GMT
ENV MONGO_MAJOR=4.2
# Wed, 17 Jun 2020 03:27:20 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 17 Jun 2020 03:27:23 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 03:27:58 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 03:28:02 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 03:28:04 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 03:28:05 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:28:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:28:08 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 03:28:09 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:2e8bea8b22f8f5a4fd5aa85019945dd8ae04f283a4ba2a7aeb4536fe2f1d1ec2`  
		Last Modified: Tue, 26 May 2020 16:25:25 GMT  
		Size: 23.7 MB (23721687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc90876b9c9a7343ae432eaec7c8dc8859c1e84b6193da8d386815fde165a70e`  
		Last Modified: Wed, 17 Jun 2020 01:44:48 GMT  
		Size: 35.2 KB (35192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bfc658a5210a9f0c9cfcda5f504e720da9268e9f3f3bf48e3a9a7af360c959`  
		Last Modified: Wed, 17 Jun 2020 01:44:49 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef0f1b06b2142ff2bf35cc565f019ed9e4efe0d8f332825167538c2337bac8a`  
		Last Modified: Wed, 17 Jun 2020 01:44:49 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79f4068e2fc9c5ce913c3640637c35584b72816ca9485c4bf5af0a22994d0f6`  
		Last Modified: Wed, 17 Jun 2020 03:31:11 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5678c55b212ca2ce4ea7b4092838653b706277000f57d7a18526f3df6cba283`  
		Last Modified: Wed, 17 Jun 2020 03:31:11 GMT  
		Size: 2.7 MB (2665976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509de0ccfb79a34de230a6fef2cfc900bdb35f1f7f583fc957b7c23b46439d4f`  
		Last Modified: Wed, 17 Jun 2020 03:31:12 GMT  
		Size: 5.3 MB (5345550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5493b54160873a149e08eedf09e74628680b1d5e8826b90672f04c88c30ccb`  
		Last Modified: Wed, 17 Jun 2020 03:31:10 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe2b58fe1082de604f779b26f7bac0f685326b5584f5a43457f1d51effdca86`  
		Last Modified: Wed, 17 Jun 2020 03:31:09 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52cb618aa3e851b5a35792b706fd4e70901c2e3fd1faa3fcf12d719ac3d8ff1`  
		Last Modified: Wed, 17 Jun 2020 03:31:08 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8985f89f29dd85eccbd8da50a080817fa846f7b7baee89e54e83f79559fff4b`  
		Last Modified: Wed, 17 Jun 2020 03:31:35 GMT  
		Size: 122.9 MB (122900361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f01ca57315b3f1a9469f85034d0f072b2d67b5ee9d3c9d2e14e3487df4db4d`  
		Last Modified: Wed, 17 Jun 2020 03:31:08 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f414fc1b8d9a096289a531b03096d4af7478a1c627842175a15974cb041c879`  
		Last Modified: Wed, 17 Jun 2020 03:31:08 GMT  
		Size: 4.0 KB (3950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:bionic` - linux; s390x

```console
$ docker pull mongo@sha256:e1c13c3ee8ae7031fdaa1e4cb645de3279a46ccf47511a9fb4b82c90d5c831f5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160598470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddfb01efb7ddfe0ac3ea40d0ded51ac1742d89e522b72b9ca43ec82ac2a642b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:41:48 GMT
ADD file:8708e93980b416070ba0bb024a7858748129059a85d2c771a4489c31710a9df1 in / 
# Wed, 17 Jun 2020 01:41:51 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:41:52 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:41:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:41:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:24:26 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 03:24:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:24:35 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:24:35 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 03:24:46 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:24:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:24:47 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Wed, 17 Jun 2020 03:24:48 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:24:48 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 03:24:48 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:24:48 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:24:48 GMT
ENV MONGO_MAJOR=4.2
# Wed, 17 Jun 2020 03:24:49 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 17 Jun 2020 03:24:49 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 03:25:14 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 03:25:18 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 03:25:18 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 03:25:19 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:25:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:25:19 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 03:25:19 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f3c26641772baa3348c0cce190edb38690a41f1824570c5c65cc363b42e5a5b5`  
		Last Modified: Sat, 30 May 2020 09:30:29 GMT  
		Size: 25.4 MB (25365846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf76fcee55454304ffbf9e321dda388a7e8de8a3916f854e1e588bc6c19b088`  
		Last Modified: Wed, 17 Jun 2020 01:42:56 GMT  
		Size: 36.2 KB (36165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5173e4f9f1868daa26021e1e701a000b0aadb2b611a487d089e7de4b728a7424`  
		Last Modified: Wed, 17 Jun 2020 01:42:56 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13da9fe451bd0f377d042d4bebef4ffd19163113e3e66dcd718fe187149a0dbd`  
		Last Modified: Wed, 17 Jun 2020 01:42:57 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d8fc9b1e9007ca5666c42ff8398a5227869b151fea1562c5e3cfb2188640e6`  
		Last Modified: Wed, 17 Jun 2020 03:28:52 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a889c8302a90f8884ff21edb649cf8dc1771453aca39505e61f29e053a1b64`  
		Last Modified: Wed, 17 Jun 2020 03:28:51 GMT  
		Size: 2.7 MB (2704483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:582fe8ee181790ce5fdadeef1c1cd7af40de0e8d2cb2e307fa05aed8d23a82b7`  
		Last Modified: Wed, 17 Jun 2020 03:28:50 GMT  
		Size: 5.7 MB (5745080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6096f1fa9fe7ad82ea015203f2410ac8b0831d0617db029aed54c698f84a2eaf`  
		Last Modified: Wed, 17 Jun 2020 03:28:50 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2bddaa2c78c2b5ac010b9af305db894e7bb616461499b863fe6af05c42bb502`  
		Last Modified: Wed, 17 Jun 2020 03:28:48 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b0ea0902452b7fe6fc59cc6001683eb80ddf80ba9fa1a59f83a576855317e12`  
		Last Modified: Wed, 17 Jun 2020 03:28:48 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507e67f4e596fea4d40f10e6ca9132a57d472a59bef2ce47ae79b92eb029ca7a`  
		Last Modified: Wed, 17 Jun 2020 03:29:02 GMT  
		Size: 126.7 MB (126738040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf93b294dbde6159d09390ee7231284abcaad59049a9d10eaebfc46619d4ad3`  
		Last Modified: Wed, 17 Jun 2020 03:28:48 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e514b21a3b45674ce414ecd79bf6adc339e8ea02fc1a80956ece983f3192be`  
		Last Modified: Wed, 17 Jun 2020 03:29:03 GMT  
		Size: 4.0 KB (3953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:latest`

```console
$ docker pull mongo@sha256:29805e9a6fc2a233b9b633c7b0f382a43df3f119522b82366a72abecb302a793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x
	-	windows version 10.0.14393.3750; amd64
	-	windows version 10.0.17763.1282; amd64

### `mongo:latest` - linux; amd64

```console
$ docker pull mongo@sha256:ed04fcf28fccf1bb2c295074775a24ddd007e14ca522ae97a56983f269cad163
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164652387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2cc1f48aed02a160b0447fd28b75952ed1d2df8c66693733d4954483734e44`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:20:29 GMT
ADD file:1e8d02626176dc8141df3c0a1365774ce73d79934654fe24a4b1e7f173108232 in / 
# Wed, 17 Jun 2020 01:20:30 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:20:31 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:20:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:20:32 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 05:16:06 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 05:16:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 05:16:16 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 05:16:16 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 05:16:30 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 05:16:32 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 05:16:33 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Wed, 17 Jun 2020 05:16:34 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 05:16:34 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 05:16:34 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 05:16:34 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 05:16:34 GMT
ENV MONGO_MAJOR=4.2
# Wed, 17 Jun 2020 05:16:35 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 17 Jun 2020 05:16:35 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 05:16:53 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 05:16:54 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 05:16:54 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 05:16:54 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 05:16:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 05:16:55 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 05:16:55 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:d7c3167c320d7a820935f54cf4290890ea19567da496ecf774e8773b35d5f065`  
		Last Modified: Wed, 27 May 2020 12:21:15 GMT  
		Size: 26.7 MB (26688718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:131f805ec7fd68d45a887e2ef82de61de0247b4eb934ab03b7c933650e854baa`  
		Last Modified: Wed, 17 Jun 2020 01:21:41 GMT  
		Size: 35.4 KB (35369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322ed380e680a77f30528ba013e3a802a7b44948a0609c7d1d732dd46a9a310d`  
		Last Modified: Wed, 17 Jun 2020 01:21:41 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac240b130982ad1c3ba3188abbf18ba4e54bdd9e504ce2d5c2eff6d3e86b8dd`  
		Last Modified: Wed, 17 Jun 2020 01:21:41 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5704a01b59ff4d100b5bcc0244090cb5b369649b41a468a82cb5015afdc4f9d`  
		Last Modified: Wed, 17 Jun 2020 05:18:30 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e396e2a1e6820b238c82087b900e4f03e1304b30ee16a5341b0c6a2a9eec20e`  
		Last Modified: Wed, 17 Jun 2020 05:18:29 GMT  
		Size: 3.0 MB (2973543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:914fffcb1cc543f9e16861fe6d80fdaad26ea9c69ba952c73cb3db44a9cfc545`  
		Last Modified: Wed, 17 Jun 2020 05:18:30 GMT  
		Size: 5.8 MB (5823974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692bd0d35810fbf133d67af4f0ae0c627fb731b875d5370d3dfaa3f1a06392fa`  
		Last Modified: Wed, 17 Jun 2020 05:18:29 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122d231765e47cbdd1b934b3ee55ffa291b76b17e4134be5b6e9837c52053c9e`  
		Last Modified: Wed, 17 Jun 2020 05:18:28 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9c497305ce2ee80e9d80fb69dcf2766f51b6b23e093fbf9d0d837b14376810`  
		Last Modified: Wed, 17 Jun 2020 05:18:28 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e3ca7a65fcd8d5d002ae04e06a5d7b900020097dec64e04923b9fa25d7d633`  
		Last Modified: Wed, 17 Jun 2020 05:18:46 GMT  
		Size: 129.1 MB (129122023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70e0d9672b4cbcef6ddbaa3fae90fb8181aeb83b59cac8f4910d69f7c359f96`  
		Last Modified: Wed, 17 Jun 2020 05:18:28 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc04aade5db18c8ca826bfaef542aa9b48f2b3045dfe7a4fa0d4f11714d37a1`  
		Last Modified: Wed, 17 Jun 2020 05:18:28 GMT  
		Size: 4.0 KB (3955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:cdec0bd28e60bc06892f9972803753d57fdc3d4bcff657b694ba7f35b80d3d02
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.7 MB (154677642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f84af28ce3aa3b7b04964d7f7ee9eb0ae10e3c19e684ad29ceeca55c605f2924`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:42:33 GMT
ADD file:7dc8819fd3d4b84ad19fb836e5bfda64a5ffefc371166f70d4d41dff6b22d450 in / 
# Wed, 17 Jun 2020 01:42:37 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:42:41 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:42:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:42:45 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:26:00 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 03:26:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:26:24 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:26:25 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 03:27:01 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:27:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:27:06 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Wed, 17 Jun 2020 03:27:10 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:27:12 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 03:27:13 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:27:16 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:27:19 GMT
ENV MONGO_MAJOR=4.2
# Wed, 17 Jun 2020 03:27:20 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 17 Jun 2020 03:27:23 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 03:27:58 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 03:28:02 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 03:28:04 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 03:28:05 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:28:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:28:08 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 03:28:09 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:2e8bea8b22f8f5a4fd5aa85019945dd8ae04f283a4ba2a7aeb4536fe2f1d1ec2`  
		Last Modified: Tue, 26 May 2020 16:25:25 GMT  
		Size: 23.7 MB (23721687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc90876b9c9a7343ae432eaec7c8dc8859c1e84b6193da8d386815fde165a70e`  
		Last Modified: Wed, 17 Jun 2020 01:44:48 GMT  
		Size: 35.2 KB (35192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bfc658a5210a9f0c9cfcda5f504e720da9268e9f3f3bf48e3a9a7af360c959`  
		Last Modified: Wed, 17 Jun 2020 01:44:49 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef0f1b06b2142ff2bf35cc565f019ed9e4efe0d8f332825167538c2337bac8a`  
		Last Modified: Wed, 17 Jun 2020 01:44:49 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79f4068e2fc9c5ce913c3640637c35584b72816ca9485c4bf5af0a22994d0f6`  
		Last Modified: Wed, 17 Jun 2020 03:31:11 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5678c55b212ca2ce4ea7b4092838653b706277000f57d7a18526f3df6cba283`  
		Last Modified: Wed, 17 Jun 2020 03:31:11 GMT  
		Size: 2.7 MB (2665976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509de0ccfb79a34de230a6fef2cfc900bdb35f1f7f583fc957b7c23b46439d4f`  
		Last Modified: Wed, 17 Jun 2020 03:31:12 GMT  
		Size: 5.3 MB (5345550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5493b54160873a149e08eedf09e74628680b1d5e8826b90672f04c88c30ccb`  
		Last Modified: Wed, 17 Jun 2020 03:31:10 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe2b58fe1082de604f779b26f7bac0f685326b5584f5a43457f1d51effdca86`  
		Last Modified: Wed, 17 Jun 2020 03:31:09 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52cb618aa3e851b5a35792b706fd4e70901c2e3fd1faa3fcf12d719ac3d8ff1`  
		Last Modified: Wed, 17 Jun 2020 03:31:08 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8985f89f29dd85eccbd8da50a080817fa846f7b7baee89e54e83f79559fff4b`  
		Last Modified: Wed, 17 Jun 2020 03:31:35 GMT  
		Size: 122.9 MB (122900361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f01ca57315b3f1a9469f85034d0f072b2d67b5ee9d3c9d2e14e3487df4db4d`  
		Last Modified: Wed, 17 Jun 2020 03:31:08 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f414fc1b8d9a096289a531b03096d4af7478a1c627842175a15974cb041c879`  
		Last Modified: Wed, 17 Jun 2020 03:31:08 GMT  
		Size: 4.0 KB (3950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - linux; s390x

```console
$ docker pull mongo@sha256:e1c13c3ee8ae7031fdaa1e4cb645de3279a46ccf47511a9fb4b82c90d5c831f5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160598470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddfb01efb7ddfe0ac3ea40d0ded51ac1742d89e522b72b9ca43ec82ac2a642b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 17 Jun 2020 01:41:48 GMT
ADD file:8708e93980b416070ba0bb024a7858748129059a85d2c771a4489c31710a9df1 in / 
# Wed, 17 Jun 2020 01:41:51 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 17 Jun 2020 01:41:52 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 17 Jun 2020 01:41:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 17 Jun 2020 01:41:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2020 03:24:26 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Wed, 17 Jun 2020 03:24:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jun 2020 03:24:35 GMT
ENV GOSU_VERSION=1.12
# Wed, 17 Jun 2020 03:24:35 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 17 Jun 2020 03:24:46 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 17 Jun 2020 03:24:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Jun 2020 03:24:47 GMT
ENV GPG_KEYS=E162F504A20CDF15827F718D4B7C549A058F8B6B
# Wed, 17 Jun 2020 03:24:48 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Wed, 17 Jun 2020 03:24:48 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 17 Jun 2020 03:24:48 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:24:48 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 17 Jun 2020 03:24:48 GMT
ENV MONGO_MAJOR=4.2
# Wed, 17 Jun 2020 03:24:49 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 17 Jun 2020 03:24:49 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Wed, 17 Jun 2020 03:25:14 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Wed, 17 Jun 2020 03:25:18 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Wed, 17 Jun 2020 03:25:18 GMT
VOLUME [/data/db /data/configdb]
# Wed, 17 Jun 2020 03:25:19 GMT
COPY file:c3beae20a29d6d69ecab76830068690f9c4f9d77d82eb60160db72670df64615 in /usr/local/bin/ 
# Wed, 17 Jun 2020 03:25:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jun 2020 03:25:19 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 03:25:19 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f3c26641772baa3348c0cce190edb38690a41f1824570c5c65cc363b42e5a5b5`  
		Last Modified: Sat, 30 May 2020 09:30:29 GMT  
		Size: 25.4 MB (25365846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf76fcee55454304ffbf9e321dda388a7e8de8a3916f854e1e588bc6c19b088`  
		Last Modified: Wed, 17 Jun 2020 01:42:56 GMT  
		Size: 36.2 KB (36165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5173e4f9f1868daa26021e1e701a000b0aadb2b611a487d089e7de4b728a7424`  
		Last Modified: Wed, 17 Jun 2020 01:42:56 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13da9fe451bd0f377d042d4bebef4ffd19163113e3e66dcd718fe187149a0dbd`  
		Last Modified: Wed, 17 Jun 2020 01:42:57 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d8fc9b1e9007ca5666c42ff8398a5227869b151fea1562c5e3cfb2188640e6`  
		Last Modified: Wed, 17 Jun 2020 03:28:52 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a889c8302a90f8884ff21edb649cf8dc1771453aca39505e61f29e053a1b64`  
		Last Modified: Wed, 17 Jun 2020 03:28:51 GMT  
		Size: 2.7 MB (2704483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:582fe8ee181790ce5fdadeef1c1cd7af40de0e8d2cb2e307fa05aed8d23a82b7`  
		Last Modified: Wed, 17 Jun 2020 03:28:50 GMT  
		Size: 5.7 MB (5745080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6096f1fa9fe7ad82ea015203f2410ac8b0831d0617db029aed54c698f84a2eaf`  
		Last Modified: Wed, 17 Jun 2020 03:28:50 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2bddaa2c78c2b5ac010b9af305db894e7bb616461499b863fe6af05c42bb502`  
		Last Modified: Wed, 17 Jun 2020 03:28:48 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b0ea0902452b7fe6fc59cc6001683eb80ddf80ba9fa1a59f83a576855317e12`  
		Last Modified: Wed, 17 Jun 2020 03:28:48 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507e67f4e596fea4d40f10e6ca9132a57d472a59bef2ce47ae79b92eb029ca7a`  
		Last Modified: Wed, 17 Jun 2020 03:29:02 GMT  
		Size: 126.7 MB (126738040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf93b294dbde6159d09390ee7231284abcaad59049a9d10eaebfc46619d4ad3`  
		Last Modified: Wed, 17 Jun 2020 03:28:48 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e514b21a3b45674ce414ecd79bf6adc339e8ea02fc1a80956ece983f3192be`  
		Last Modified: Wed, 17 Jun 2020 03:29:03 GMT  
		Size: 4.0 KB (3953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.14393.3750; amd64

```console
$ docker pull mongo@sha256:af38590235375eb1218ddd651e660f1a6e6e6a882842e7b428f2d55d46cc937a
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6193023222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aaf2b53fe9e096da5ab6f4ae0e34caf7cf3de0a336bd9576cee60752c37c17b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 01 Jun 2020 18:53:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Jun 2020 12:52:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 17 Jun 2020 00:50:43 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 17 Jun 2020 00:50:44 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 17 Jun 2020 00:50:45 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 17 Jun 2020 01:08:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 17 Jun 2020 01:08:52 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 17 Jun 2020 01:08:53 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 01:08:54 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:375fbabb84945635805b46a02a17ac15a3177bcaae7404cfab5f1ceb0460cb60`  
		Size: 1.7 GB (1664011795 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:30efe9163d37226b077b25cd93b088cebd2ddbaadf173d143b9fe0ddecaeae53`  
		Last Modified: Wed, 10 Jun 2020 15:34:41 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b60479ef88c8a931aeeffaa74d289fbbf204229adb6a20c54d51456f70bb75`  
		Last Modified: Wed, 17 Jun 2020 01:32:04 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52bb592e6eb6512ccf1127b0311263697d559599357972414f4b776277bd628f`  
		Last Modified: Wed, 17 Jun 2020 01:32:04 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e57b55cda98f10b8c536232f9fd5fbc19c778c4043edc4fea012972832bb4570`  
		Last Modified: Wed, 17 Jun 2020 01:32:01 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eaad7a52f6dc4a311c3e724f9b5fe27f7af849fa6229fe21fc0490976fcb607`  
		Last Modified: Wed, 17 Jun 2020 01:32:57 GMT  
		Size: 459.0 MB (459017760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187b8e518ef05e3f4e7348e0ca7fef3e05414c63661223d63d83a36367ff9605`  
		Last Modified: Wed, 17 Jun 2020 01:32:01 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58773855217e4f81876fd21fd13a61d94d0f5a191e7025ce2bf26469077e330c`  
		Last Modified: Wed, 17 Jun 2020 01:32:01 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e25f1762a4dcad6fd6709c2602e0d459a0efb6aea6e10e16cb78796c27e496d`  
		Last Modified: Wed, 17 Jun 2020 01:32:01 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:latest` - windows version 10.0.17763.1282; amd64

```console
$ docker pull mongo@sha256:a332d0d55bcb861ab664609d4ee8b7a3c7481e800fa5ad62009c671c1673af0b
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2752054828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86c12ab59b3d8850d880c02f06724769d7955a42bb4c5b10fd9a16cb6ad19f7`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Wed, 10 Jun 2020 12:43:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 17 Jun 2020 01:09:02 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 17 Jun 2020 01:09:03 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 17 Jun 2020 01:09:04 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 17 Jun 2020 01:28:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 17 Jun 2020 01:28:16 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 17 Jun 2020 01:28:18 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 01:28:19 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b11029314f3c794dc51e43c915b3e62f6b44aeb96f84b8b92f453e61cf7a2cb3`  
		Last Modified: Wed, 10 Jun 2020 15:34:12 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f51df57f2cb6ccc03b57cbd044ee4a49d9383489feb3872da465ba8b6bffa89`  
		Last Modified: Wed, 17 Jun 2020 01:33:19 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84353c49610a99480bfb74a8769e7446bbd898b8644c25d2b8c645c7a2e90e0e`  
		Last Modified: Wed, 17 Jun 2020 01:33:18 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c19d206596ed0cd1b7da30ba6e637be1d4c31dc398ca6f4d30d583593e31705`  
		Last Modified: Wed, 17 Jun 2020 01:33:16 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90fa0f2b93199d15d0678aa8a13db7d1470a5ce7ddb94ec8fa93a75156cce44`  
		Last Modified: Wed, 17 Jun 2020 01:34:14 GMT  
		Size: 458.1 MB (458132610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:369180762b76f75c56ed85ad59e938011c514ad32b51a43cbb6d5fcce885b5d1`  
		Last Modified: Wed, 17 Jun 2020 01:33:16 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f9c110c11f811446f2204714562c02b6eefeeb1cae671aa73af5e4cc7dfbd0`  
		Last Modified: Wed, 17 Jun 2020 01:33:16 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c7a275e52c9eafb08caf7a861ef21a725b77ee54c1b867ddb4b4da99814dd7`  
		Last Modified: Wed, 17 Jun 2020 01:33:16 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:windowsservercore`

```console
$ docker pull mongo@sha256:3dfacb1c248e30392bcfaba258677f7a057a4ea96b2a37de4839a01081742a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3750; amd64
	-	windows version 10.0.17763.1282; amd64

### `mongo:windowsservercore` - windows version 10.0.14393.3750; amd64

```console
$ docker pull mongo@sha256:af38590235375eb1218ddd651e660f1a6e6e6a882842e7b428f2d55d46cc937a
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6193023222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aaf2b53fe9e096da5ab6f4ae0e34caf7cf3de0a336bd9576cee60752c37c17b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 01 Jun 2020 18:53:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Jun 2020 12:52:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 17 Jun 2020 00:50:43 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 17 Jun 2020 00:50:44 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 17 Jun 2020 00:50:45 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 17 Jun 2020 01:08:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 17 Jun 2020 01:08:52 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 17 Jun 2020 01:08:53 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 01:08:54 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:375fbabb84945635805b46a02a17ac15a3177bcaae7404cfab5f1ceb0460cb60`  
		Size: 1.7 GB (1664011795 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:30efe9163d37226b077b25cd93b088cebd2ddbaadf173d143b9fe0ddecaeae53`  
		Last Modified: Wed, 10 Jun 2020 15:34:41 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b60479ef88c8a931aeeffaa74d289fbbf204229adb6a20c54d51456f70bb75`  
		Last Modified: Wed, 17 Jun 2020 01:32:04 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52bb592e6eb6512ccf1127b0311263697d559599357972414f4b776277bd628f`  
		Last Modified: Wed, 17 Jun 2020 01:32:04 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e57b55cda98f10b8c536232f9fd5fbc19c778c4043edc4fea012972832bb4570`  
		Last Modified: Wed, 17 Jun 2020 01:32:01 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eaad7a52f6dc4a311c3e724f9b5fe27f7af849fa6229fe21fc0490976fcb607`  
		Last Modified: Wed, 17 Jun 2020 01:32:57 GMT  
		Size: 459.0 MB (459017760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187b8e518ef05e3f4e7348e0ca7fef3e05414c63661223d63d83a36367ff9605`  
		Last Modified: Wed, 17 Jun 2020 01:32:01 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58773855217e4f81876fd21fd13a61d94d0f5a191e7025ce2bf26469077e330c`  
		Last Modified: Wed, 17 Jun 2020 01:32:01 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e25f1762a4dcad6fd6709c2602e0d459a0efb6aea6e10e16cb78796c27e496d`  
		Last Modified: Wed, 17 Jun 2020 01:32:01 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:windowsservercore` - windows version 10.0.17763.1282; amd64

```console
$ docker pull mongo@sha256:a332d0d55bcb861ab664609d4ee8b7a3c7481e800fa5ad62009c671c1673af0b
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2752054828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86c12ab59b3d8850d880c02f06724769d7955a42bb4c5b10fd9a16cb6ad19f7`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Wed, 10 Jun 2020 12:43:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 17 Jun 2020 01:09:02 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 17 Jun 2020 01:09:03 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 17 Jun 2020 01:09:04 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 17 Jun 2020 01:28:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 17 Jun 2020 01:28:16 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 17 Jun 2020 01:28:18 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 01:28:19 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b11029314f3c794dc51e43c915b3e62f6b44aeb96f84b8b92f453e61cf7a2cb3`  
		Last Modified: Wed, 10 Jun 2020 15:34:12 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f51df57f2cb6ccc03b57cbd044ee4a49d9383489feb3872da465ba8b6bffa89`  
		Last Modified: Wed, 17 Jun 2020 01:33:19 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84353c49610a99480bfb74a8769e7446bbd898b8644c25d2b8c645c7a2e90e0e`  
		Last Modified: Wed, 17 Jun 2020 01:33:18 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c19d206596ed0cd1b7da30ba6e637be1d4c31dc398ca6f4d30d583593e31705`  
		Last Modified: Wed, 17 Jun 2020 01:33:16 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90fa0f2b93199d15d0678aa8a13db7d1470a5ce7ddb94ec8fa93a75156cce44`  
		Last Modified: Wed, 17 Jun 2020 01:34:14 GMT  
		Size: 458.1 MB (458132610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:369180762b76f75c56ed85ad59e938011c514ad32b51a43cbb6d5fcce885b5d1`  
		Last Modified: Wed, 17 Jun 2020 01:33:16 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f9c110c11f811446f2204714562c02b6eefeeb1cae671aa73af5e4cc7dfbd0`  
		Last Modified: Wed, 17 Jun 2020 01:33:16 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c7a275e52c9eafb08caf7a861ef21a725b77ee54c1b867ddb4b4da99814dd7`  
		Last Modified: Wed, 17 Jun 2020 01:33:16 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:windowsservercore-1809`

```console
$ docker pull mongo@sha256:bc2bc28a30754135707bfc25dd73c4aceb4ae89c943a243433b0b3f321f640fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1282; amd64

### `mongo:windowsservercore-1809` - windows version 10.0.17763.1282; amd64

```console
$ docker pull mongo@sha256:a332d0d55bcb861ab664609d4ee8b7a3c7481e800fa5ad62009c671c1673af0b
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2752054828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86c12ab59b3d8850d880c02f06724769d7955a42bb4c5b10fd9a16cb6ad19f7`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Jun 2020 01:48:42 GMT
RUN Install update 1809-amd64
# Wed, 10 Jun 2020 12:43:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 17 Jun 2020 01:09:02 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 17 Jun 2020 01:09:03 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 17 Jun 2020 01:09:04 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 17 Jun 2020 01:28:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 17 Jun 2020 01:28:16 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 17 Jun 2020 01:28:18 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 01:28:19 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:666079ee04606f07f4a27dd98526f5049ef8fed93e347d8b4c447b0d5060c77d`  
		Size: 575.6 MB (575581379 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b11029314f3c794dc51e43c915b3e62f6b44aeb96f84b8b92f453e61cf7a2cb3`  
		Last Modified: Wed, 10 Jun 2020 15:34:12 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f51df57f2cb6ccc03b57cbd044ee4a49d9383489feb3872da465ba8b6bffa89`  
		Last Modified: Wed, 17 Jun 2020 01:33:19 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84353c49610a99480bfb74a8769e7446bbd898b8644c25d2b8c645c7a2e90e0e`  
		Last Modified: Wed, 17 Jun 2020 01:33:18 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c19d206596ed0cd1b7da30ba6e637be1d4c31dc398ca6f4d30d583593e31705`  
		Last Modified: Wed, 17 Jun 2020 01:33:16 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90fa0f2b93199d15d0678aa8a13db7d1470a5ce7ddb94ec8fa93a75156cce44`  
		Last Modified: Wed, 17 Jun 2020 01:34:14 GMT  
		Size: 458.1 MB (458132610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:369180762b76f75c56ed85ad59e938011c514ad32b51a43cbb6d5fcce885b5d1`  
		Last Modified: Wed, 17 Jun 2020 01:33:16 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f9c110c11f811446f2204714562c02b6eefeeb1cae671aa73af5e4cc7dfbd0`  
		Last Modified: Wed, 17 Jun 2020 01:33:16 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c7a275e52c9eafb08caf7a861ef21a725b77ee54c1b867ddb4b4da99814dd7`  
		Last Modified: Wed, 17 Jun 2020 01:33:16 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mongo:windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:9b6e497bdcaa3a451d4296f944c0a13ac07344a7879cb41fb387ae288308fc61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3750; amd64

### `mongo:windowsservercore-ltsc2016` - windows version 10.0.14393.3750; amd64

```console
$ docker pull mongo@sha256:af38590235375eb1218ddd651e660f1a6e6e6a882842e7b428f2d55d46cc937a
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6193023222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aaf2b53fe9e096da5ab6f4ae0e34caf7cf3de0a336bd9576cee60752c37c17b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 01 Jun 2020 18:53:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Jun 2020 12:52:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 17 Jun 2020 00:50:43 GMT
ENV MONGO_VERSION=4.2.8
# Wed, 17 Jun 2020 00:50:44 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.8-signed.msi
# Wed, 17 Jun 2020 00:50:45 GMT
ENV MONGO_DOWNLOAD_SHA256=166c5cd99132d72969a67446e494da6287710a34f3f75ee9fb798a2945c0f502
# Wed, 17 Jun 2020 01:08:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 17 Jun 2020 01:08:52 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 17 Jun 2020 01:08:53 GMT
EXPOSE 27017
# Wed, 17 Jun 2020 01:08:54 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:375fbabb84945635805b46a02a17ac15a3177bcaae7404cfab5f1ceb0460cb60`  
		Size: 1.7 GB (1664011795 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:30efe9163d37226b077b25cd93b088cebd2ddbaadf173d143b9fe0ddecaeae53`  
		Last Modified: Wed, 10 Jun 2020 15:34:41 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b60479ef88c8a931aeeffaa74d289fbbf204229adb6a20c54d51456f70bb75`  
		Last Modified: Wed, 17 Jun 2020 01:32:04 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52bb592e6eb6512ccf1127b0311263697d559599357972414f4b776277bd628f`  
		Last Modified: Wed, 17 Jun 2020 01:32:04 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e57b55cda98f10b8c536232f9fd5fbc19c778c4043edc4fea012972832bb4570`  
		Last Modified: Wed, 17 Jun 2020 01:32:01 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eaad7a52f6dc4a311c3e724f9b5fe27f7af849fa6229fe21fc0490976fcb607`  
		Last Modified: Wed, 17 Jun 2020 01:32:57 GMT  
		Size: 459.0 MB (459017760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187b8e518ef05e3f4e7348e0ca7fef3e05414c63661223d63d83a36367ff9605`  
		Last Modified: Wed, 17 Jun 2020 01:32:01 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58773855217e4f81876fd21fd13a61d94d0f5a191e7025ce2bf26469077e330c`  
		Last Modified: Wed, 17 Jun 2020 01:32:01 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e25f1762a4dcad6fd6709c2602e0d459a0efb6aea6e10e16cb78796c27e496d`  
		Last Modified: Wed, 17 Jun 2020 01:32:01 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
