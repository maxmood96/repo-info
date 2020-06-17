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
