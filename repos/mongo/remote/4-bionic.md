## `mongo:4-bionic`

```console
$ docker pull mongo@sha256:c310271a26008121e3d92e1c5aec224cfe2d349f886ee34614ccaff1ecf54f64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `mongo:4-bionic` - linux; amd64

```console
$ docker pull mongo@sha256:ebb6b8403c1f47069b099f1ba75778d41e15a5d8eed3db6f435733333e403a2d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.7 MB (175677269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07630e791de3ceb87d39543799438e118753246d19dcfd6529bd4d27ff1b83bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 23 Apr 2021 22:21:22 GMT
ADD file:d7fa3c26651f9204a5629287a1a9a6e7dc6a0bc6eb499e82c433c0c8f67ff46b in / 
# Fri, 23 Apr 2021 22:21:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:21:24 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:21:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:21:25 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 00:41:08 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Sat, 24 Apr 2021 00:41:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:41:18 GMT
ENV GOSU_VERSION=1.12
# Sat, 24 Apr 2021 00:41:18 GMT
ENV JSYAML_VERSION=3.13.1
# Sat, 24 Apr 2021 00:41:28 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 24 Apr 2021 00:41:29 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 24 Apr 2021 00:41:58 GMT
ENV GPG_KEYS=20691EEC35216C63CAF66CE1656408E390CFB1F5
# Sat, 24 Apr 2021 00:41:59 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Sat, 24 Apr 2021 00:42:00 GMT
ARG MONGO_PACKAGE=mongodb-org
# Sat, 24 Apr 2021 00:42:00 GMT
ARG MONGO_REPO=repo.mongodb.org
# Sat, 24 Apr 2021 00:42:00 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Sat, 24 Apr 2021 00:42:00 GMT
ENV MONGO_MAJOR=4.4
# Tue, 11 May 2021 00:11:00 GMT
ENV MONGO_VERSION=4.4.6
# Tue, 11 May 2021 00:11:02 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Tue, 11 May 2021 00:11:45 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Tue, 11 May 2021 00:11:48 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Tue, 11 May 2021 00:11:48 GMT
VOLUME [/data/db /data/configdb]
# Tue, 11 May 2021 00:11:49 GMT
COPY file:1dd28550b0c6cd4baae08342a3beff8f6014f7551c63d060630b98bd44e1f706 in /usr/local/bin/ 
# Tue, 11 May 2021 00:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 May 2021 00:11:49 GMT
EXPOSE 27017
# Tue, 11 May 2021 00:11:50 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:01bf7da0a88c9e37ae418d17c0aeed0621524848d80ccb9e38c67e7ab8e11928`  
		Last Modified: Fri, 16 Apr 2021 15:20:23 GMT  
		Size: 26.7 MB (26697009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b4a5f15c7a0722b4f22e61b5387317eaf2602c27ffb2bceac9a25f19fbd156`  
		Last Modified: Fri, 23 Apr 2021 22:22:45 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ffbe87baa135002dddb7a7460082c5d6a352186e1be9464c5f31db81378824`  
		Last Modified: Fri, 23 Apr 2021 22:22:45 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d5e5c7eab9e07a520aed11bed2b4b7c44c3ec3df6e389bc458cb25c18582ad`  
		Last Modified: Sat, 24 Apr 2021 00:43:52 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43798cf18b45dce7601f8c40514229531dd9f36d588b6d69b29fe7400aa80640`  
		Last Modified: Sat, 24 Apr 2021 00:43:51 GMT  
		Size: 3.0 MB (2978981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67349a81f4351858274518ff0d80ad12763635a544d8483bdfc9a9d33882be7d`  
		Last Modified: Sat, 24 Apr 2021 00:43:52 GMT  
		Size: 5.8 MB (5829871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:590845b1f17c5e6f8c9aef645fc7a87e9d5bf7b95a9cb3b37ccd407f7d956818`  
		Last Modified: Sat, 24 Apr 2021 00:43:50 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f2ff17242ce7e307fbd191a597f210061566606443ff6632ca685d394cb9acf`  
		Last Modified: Sat, 24 Apr 2021 00:44:16 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f11b2ce05942f19ca819aa8c130575b0850153384fba7f489fd1a62ec0d94e7`  
		Last Modified: Tue, 11 May 2021 00:12:27 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91532386f4ec7af743bc43ddbab8410d9d2fee68ce63bca3aa397c04e29b9091`  
		Last Modified: Tue, 11 May 2021 00:12:51 GMT  
		Size: 140.2 MB (140162019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:705ef0ab262e766f32008195b4e3719f5444b83e3218dbab09f5cfa7098322ea`  
		Last Modified: Tue, 11 May 2021 00:12:27 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6238126b609f01bb47ddd8598f331bb5cb7653f2d9798eb2f14d48061d8e279`  
		Last Modified: Tue, 11 May 2021 00:12:27 GMT  
		Size: 4.5 KB (4477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-bionic` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:c740f5fce802628d8837ad78d443dda66eecc3db7e8143943c5494a86fe57d7c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.1 MB (168069821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0033abba7a987dc06e45c2bec726aed64206b619a9da1b59498555d43512cc24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 27 May 2021 12:29:48 GMT
ADD file:813209ca97a54f1f092727aea57fe5652a037b9c167df8bfccd9262415f8553f in / 
# Thu, 27 May 2021 12:29:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 27 May 2021 12:29:50 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 27 May 2021 12:29:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 27 May 2021 12:29:51 GMT
CMD ["/bin/bash"]
# Thu, 10 Jun 2021 20:41:07 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Thu, 10 Jun 2021 20:41:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 10 Jun 2021 20:41:16 GMT
ENV GOSU_VERSION=1.12
# Thu, 10 Jun 2021 20:41:16 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 10 Jun 2021 20:41:29 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 10 Jun 2021 20:41:30 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 10 Jun 2021 20:41:31 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '20691EEC35216C63CAF66CE1656408E390CFB1F5'; 	for key; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export "$@" > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 10 Jun 2021 20:41:31 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 10 Jun 2021 20:41:31 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 10 Jun 2021 20:41:32 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 10 Jun 2021 20:41:32 GMT
ENV MONGO_MAJOR=4.4
# Thu, 10 Jun 2021 20:41:32 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Thu, 10 Jun 2021 20:41:33 GMT
ENV MONGO_VERSION=4.4.6
# Thu, 10 Jun 2021 20:41:53 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Thu, 10 Jun 2021 20:41:54 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Thu, 10 Jun 2021 20:41:54 GMT
VOLUME [/data/db /data/configdb]
# Thu, 10 Jun 2021 20:41:55 GMT
COPY file:1dd28550b0c6cd4baae08342a3beff8f6014f7551c63d060630b98bd44e1f706 in /usr/local/bin/ 
# Thu, 10 Jun 2021 20:41:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Jun 2021 20:41:55 GMT
EXPOSE 27017
# Thu, 10 Jun 2021 20:41:55 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:ed6dc9c66f7cc607969a6f995c83956f1e614ec5dd42205a2ea544f8f6260a34`  
		Last Modified: Thu, 13 May 2021 00:25:09 GMT  
		Size: 23.7 MB (23703340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c11899c85b166cc1ed1af82b5f8bda57b93fa119405e47bb96f45bbbd93533`  
		Last Modified: Thu, 27 May 2021 12:31:40 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86ebe93eb4a196c3d45c24bb95176c57287e87aed340cf757e873a861aed2540`  
		Last Modified: Thu, 27 May 2021 12:31:40 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39aaa4477be69e542f97742562aae792bf43c417f60d541c8314e5883ff03bc9`  
		Last Modified: Thu, 10 Jun 2021 20:44:40 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e646d519ec5ded7db3b57dd834a5a6e5cc816e992f357f8e151fb8604689e23e`  
		Last Modified: Thu, 10 Jun 2021 20:44:40 GMT  
		Size: 2.7 MB (2668978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab123adc4a7a214364c8739f02249d0718679ba5d32471ad885b57852b7969c`  
		Last Modified: Thu, 10 Jun 2021 20:44:40 GMT  
		Size: 5.3 MB (5347068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c0f20e463788ba641b21c5733701dfd4782a8cd4e6c2ef93d0794316d3076a`  
		Last Modified: Thu, 10 Jun 2021 20:44:39 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff9d1fb24321e627086c56799a49292a628b1c7ea326f70eea26b68f1d67d31`  
		Last Modified: Thu, 10 Jun 2021 20:44:36 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f72b3a3c05c4ab28e627e2ff1e77a7c953cd1a1bdfa76b453776e0fd19c3b46`  
		Last Modified: Thu, 10 Jun 2021 20:44:36 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6967469c70cb1ae3af218cade46ceaa805cb7e3057850f631ba7b9297cc4ba96`  
		Last Modified: Thu, 10 Jun 2021 20:44:55 GMT  
		Size: 136.3 MB (136341060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1265aeb257785dcc8d6ed979283446b00c01ba0b64b51c4933d9ad2319f20e3d`  
		Last Modified: Thu, 10 Jun 2021 20:44:37 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:656d6f04d9418b2445f9f3563d241fbefd2435f5c62efb8f02667ed865d8600c`  
		Last Modified: Thu, 10 Jun 2021 20:44:37 GMT  
		Size: 4.5 KB (4471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-bionic` - linux; s390x

```console
$ docker pull mongo@sha256:b56aae7c12e687b3e3f3b911b3728e16ce2207a0238139f757bba418ddef45e3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169474401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3771054b9187f4b4a0943d8e4564a6afd9d52da3bdf84ef34146ea14509126f8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 19 May 2021 23:28:29 GMT
ADD file:718406af36d25bc30b425ddad4eaa810e4f8cfe92388955edc07fd5ec9816dcc in / 
# Wed, 19 May 2021 23:28:36 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 23:28:38 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 May 2021 23:28:40 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 23:28:40 GMT
CMD ["/bin/bash"]
# Thu, 10 Jun 2021 20:41:44 GMT
RUN groupadd -r mongodb && useradd -r -g mongodb mongodb
# Thu, 10 Jun 2021 20:42:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 	; 	if ! command -v ps > /dev/null; then 		apt-get install -y --no-install-recommends procps; 	fi; 	rm -rf /var/lib/apt/lists/*
# Thu, 10 Jun 2021 20:42:03 GMT
ENV GOSU_VERSION=1.12
# Thu, 10 Jun 2021 20:42:03 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 10 Jun 2021 20:42:21 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	if ! command -v gpg > /dev/null; then 		apt-get install -y --no-install-recommends gnupg dirmngr; 		savedAptMark="$savedAptMark gnupg dirmngr"; 	elif gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends gnupg-curl; 	fi; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 		wget -O /js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 10 Jun 2021 20:42:23 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 10 Jun 2021 20:42:26 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- '20691EEC35216C63CAF66CE1656408E390CFB1F5'; 	for key; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --export "$@" > /etc/apt/trusted.gpg.d/mongodb.gpg; 	command -v gpgconf && gpgconf --kill all || :; 	rm -r "$GNUPGHOME"; 	apt-key list
# Thu, 10 Jun 2021 20:42:27 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 10 Jun 2021 20:42:28 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 10 Jun 2021 20:42:28 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 10 Jun 2021 20:42:29 GMT
ENV MONGO_MAJOR=4.4
# Thu, 10 Jun 2021 20:42:31 GMT
RUN echo "deb http://$MONGO_REPO/apt/ubuntu bionic/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list"
# Thu, 10 Jun 2021 20:42:31 GMT
ENV MONGO_VERSION=4.4.6
# Thu, 10 Jun 2021 20:43:17 GMT
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& ln -s /bin/true /usr/local/bin/systemctl 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -f /usr/local/bin/systemctl 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig
# Thu, 10 Jun 2021 20:43:28 GMT
RUN mkdir -p /data/db /data/configdb 	&& chown -R mongodb:mongodb /data/db /data/configdb
# Thu, 10 Jun 2021 20:43:29 GMT
VOLUME [/data/db /data/configdb]
# Thu, 10 Jun 2021 20:43:30 GMT
COPY file:1dd28550b0c6cd4baae08342a3beff8f6014f7551c63d060630b98bd44e1f706 in /usr/local/bin/ 
# Thu, 10 Jun 2021 20:43:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 10 Jun 2021 20:43:31 GMT
EXPOSE 27017
# Thu, 10 Jun 2021 20:43:32 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:3d5e421eb08da6bcb06173fcdd4e739a0fc77d7b26f72680342d8db9aedebf05`  
		Last Modified: Wed, 19 May 2021 23:30:36 GMT  
		Size: 25.4 MB (25352550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b74c33ee4c205747bbbc098fc12afc14cab69dd5b2186b8bf7ee58f516631b`  
		Last Modified: Wed, 19 May 2021 23:30:32 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb318177ecfab6a1f7a7c8290c83d4d680cf1110f5b4d80fd059793e3b64708`  
		Last Modified: Wed, 19 May 2021 23:30:32 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e6595cbe72b974f8aafef387a4f7d5fb790d80893125b3a2e45a651a013599`  
		Last Modified: Thu, 10 Jun 2021 20:43:59 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bacf862d594fd09099ab7d5f8649e8253f4c24328ec0ad6b48fc1c3caf13136`  
		Last Modified: Thu, 10 Jun 2021 20:43:58 GMT  
		Size: 2.7 MB (2708372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4673cb5055737335c1e65c15d667592d1a2fc6f8ddd6a7a41c6e449f2f9ccb29`  
		Last Modified: Thu, 10 Jun 2021 20:43:59 GMT  
		Size: 5.7 MB (5747491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:247939de1194baece6b926aede4388220608f654c69900ac04ff0cd7e418cb1d`  
		Last Modified: Thu, 10 Jun 2021 20:43:58 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36592447e0d27843fce2e478128be877dc4cc0c32a90a38fc4ab269e2b4ac57c`  
		Last Modified: Thu, 10 Jun 2021 20:43:56 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c22aae6ac6e6baf8ebfe0eae614751c111255bcd7ff38c007f9519c39b1ce47`  
		Last Modified: Thu, 10 Jun 2021 20:43:56 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9340e459b4ce83fff9b2c7d8dc421213035d71652688cacf0b6587be41544794`  
		Last Modified: Thu, 10 Jun 2021 20:44:15 GMT  
		Size: 135.7 MB (135656602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5fcfc89899b02657c93dde8623b024ad8f24f08ca08fb001e2313b338a39232`  
		Last Modified: Thu, 10 Jun 2021 20:43:56 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c952310b693edd8f7af0947447f69298c5c0bd0e567e4a20333661b9ed93bd49`  
		Last Modified: Thu, 10 Jun 2021 20:43:57 GMT  
		Size: 4.5 KB (4472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
