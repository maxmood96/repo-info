## `mongo:8-noble`

```console
$ docker pull mongo@sha256:feff3f93d46512c1f404e441f1886b72db60ebebf65f441a086d57f01dc10bcf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:8-noble` - linux; amd64

```console
$ docker pull mongo@sha256:40432390b0ad3bbbd134bc96003dccba2eb8e70411cc6937d41e649095749d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.1 MB (301066652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a328705c9f53cb7554ebf3c01d53578130d4c68cca7c15bb079822729c8236`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 30 Sep 2025 14:32:28 GMT
ARG RELEASE
# Tue, 30 Sep 2025 14:32:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 14:32:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 14:32:28 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 14:32:30 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Tue, 30 Sep 2025 14:32:31 GMT
CMD ["/bin/bash"]
# Mon, 06 Oct 2025 23:08:34 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Mon, 06 Oct 2025 23:08:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Oct 2025 23:08:34 GMT
ENV GOSU_VERSION=1.19
# Mon, 06 Oct 2025 23:08:34 GMT
ENV JSYAML_VERSION=3.13.1
# Mon, 06 Oct 2025 23:08:34 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Mon, 06 Oct 2025 23:08:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 06 Oct 2025 23:08:34 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 06 Oct 2025 23:08:34 GMT
ARG MONGO_PACKAGE=mongodb-org
# Mon, 06 Oct 2025 23:08:34 GMT
ARG MONGO_REPO=repo.mongodb.org
# Mon, 06 Oct 2025 23:08:34 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Mon, 06 Oct 2025 23:08:34 GMT
ENV MONGO_MAJOR=8.0
# Mon, 06 Oct 2025 23:08:34 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Mon, 06 Oct 2025 23:08:34 GMT
ENV MONGO_VERSION=8.0.15
# Mon, 06 Oct 2025 23:08:34 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Mon, 06 Oct 2025 23:08:34 GMT
VOLUME [/data/db /data/configdb]
# Mon, 06 Oct 2025 23:08:34 GMT
ENV HOME=/data/db
# Mon, 06 Oct 2025 23:08:34 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Mon, 06 Oct 2025 23:08:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 Oct 2025 23:08:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 Oct 2025 23:08:34 GMT
EXPOSE map[27017/tcp:{}]
# Mon, 06 Oct 2025 23:08:34 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7cf1772c39ac7c44d4c0b687a2f662b78806bddbd857d470be379313837b89c`  
		Last Modified: Wed, 08 Oct 2025 00:12:18 GMT  
		Size: 1.2 KB (1215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0aa04a4a04a79052fd89ed8e07d27c73e5a6a130564a4e228fc3bae5f402671`  
		Last Modified: Wed, 08 Oct 2025 00:12:18 GMT  
		Size: 3.9 MB (3913300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c689879ab953c6c0c0db6e8093acb39a7b5548538be4cbda5908366687fbfa1d`  
		Last Modified: Wed, 08 Oct 2025 00:12:18 GMT  
		Size: 933.7 KB (933717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8f5e3438759325281fd2490384724879fc663998c0c08fff46129b4e927f7e`  
		Last Modified: Wed, 08 Oct 2025 00:12:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b286d17d79fb8cc6192efb4fc9b7d6884a1e2f48257992eb793cda0aa40575`  
		Last Modified: Wed, 08 Oct 2025 00:12:18 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8375b6da4a30168d5d123ef0af37bd632871953a0dca4e0b018505366aa29e`  
		Last Modified: Wed, 08 Oct 2025 01:11:07 GMT  
		Size: 266.5 MB (266490025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd6e43de3c442231d1472011f3195eddfaf1d91e4569568543e1f21ae0d87b1`  
		Last Modified: Wed, 08 Oct 2025 00:12:18 GMT  
		Size: 5.0 KB (5005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:8-noble` - unknown; unknown

```console
$ docker pull mongo@sha256:15453ea7b1a39f55a2f68e31ce22c5ca278c2783a0b1150a048d27c6279e8d56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2695149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b948720f096b468839291afcfccab170ff1dd8c36a835828dca8c17733bf08`

```dockerfile
```

-	Layers:
	-	`sha256:6245d60c44be86c16345e68bafb807a13c8b111e94736a5cb6aa6e48bea62f5c`  
		Last Modified: Wed, 08 Oct 2025 04:08:12 GMT  
		Size: 2.7 MB (2666310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5544f31f2f974cf7fd00033e71983ee74a087847388d9a561b5f36a286bc6319`  
		Last Modified: Wed, 08 Oct 2025 04:08:13 GMT  
		Size: 28.8 KB (28839 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:8-noble` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:c72b1f51340e0cc4ef0ea11616a47321d10e991f93ea23e50ce7b4ef3f3f3af5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.5 MB (288466505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd3f49b8f71422ad5b77146df99b1e9261a84f7d6ac1a30caf7588692807349`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 30 Sep 2025 14:36:10 GMT
ARG RELEASE
# Tue, 30 Sep 2025 14:36:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 Sep 2025 14:36:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 Sep 2025 14:36:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 30 Sep 2025 14:36:15 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 30 Sep 2025 14:36:15 GMT
CMD ["/bin/bash"]
# Mon, 06 Oct 2025 23:08:34 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Mon, 06 Oct 2025 23:08:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 06 Oct 2025 23:08:34 GMT
ENV GOSU_VERSION=1.19
# Mon, 06 Oct 2025 23:08:34 GMT
ENV JSYAML_VERSION=3.13.1
# Mon, 06 Oct 2025 23:08:34 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Mon, 06 Oct 2025 23:08:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 06 Oct 2025 23:08:34 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 06 Oct 2025 23:08:34 GMT
ARG MONGO_PACKAGE=mongodb-org
# Mon, 06 Oct 2025 23:08:34 GMT
ARG MONGO_REPO=repo.mongodb.org
# Mon, 06 Oct 2025 23:08:34 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Mon, 06 Oct 2025 23:08:34 GMT
ENV MONGO_MAJOR=8.0
# Mon, 06 Oct 2025 23:08:34 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Mon, 06 Oct 2025 23:08:34 GMT
ENV MONGO_VERSION=8.0.15
# Mon, 06 Oct 2025 23:08:34 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Mon, 06 Oct 2025 23:08:34 GMT
VOLUME [/data/db /data/configdb]
# Mon, 06 Oct 2025 23:08:34 GMT
ENV HOME=/data/db
# Mon, 06 Oct 2025 23:08:34 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Mon, 06 Oct 2025 23:08:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 06 Oct 2025 23:08:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 06 Oct 2025 23:08:34 GMT
EXPOSE map[27017/tcp:{}]
# Mon, 06 Oct 2025 23:08:34 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ef24267ccaa91fffa8fc03c39f7b1832cb9e863dfcb1654dbe250b8f93983e`  
		Last Modified: Wed, 08 Oct 2025 00:46:00 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03acc555cf4b7af7481ccd464618d3703439737884a754dec56859970fad170`  
		Last Modified: Wed, 08 Oct 2025 00:45:59 GMT  
		Size: 3.7 MB (3709744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af1a93e517a7c45340baa8f36ffcb6f3c66332179569e2aefa55d1ebda4eae2`  
		Last Modified: Wed, 08 Oct 2025 00:45:59 GMT  
		Size: 886.0 KB (885985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1f2e33c26e6a83022415ba47a9f5de160f7481ca35528885814b63214a59a6`  
		Last Modified: Wed, 08 Oct 2025 00:46:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ab4f7a55e1aface5a22db42837a818c2b32501434fb726b914f10388e4bc66`  
		Last Modified: Wed, 08 Oct 2025 00:45:59 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014090b2fefdb97b2096a450b475c91fdb0d2a654fe392e23efaa40381165c66`  
		Last Modified: Wed, 08 Oct 2025 01:12:49 GMT  
		Size: 255.0 MB (255002598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3f670c85ef5e74dedb008d8eac6e3a10b69682ccf44f854356de164f076e48`  
		Last Modified: Wed, 08 Oct 2025 00:45:59 GMT  
		Size: 5.0 KB (5004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:8-noble` - unknown; unknown

```console
$ docker pull mongo@sha256:d4978b5dce0dc0ccc3738a441462e8a77f41acb8f0dc57d9d3499d72e468d575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2696512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5628c46fd60262ad44a4641c8c670ac7a0f81ea9ac653945da3532fbc042c27`

```dockerfile
```

-	Layers:
	-	`sha256:bb137b53e3669fac0b2fd5b94692c232996c1b04517eddd730e444750f8bd1c9`  
		Last Modified: Wed, 08 Oct 2025 04:08:17 GMT  
		Size: 2.7 MB (2667446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3eb91e7bec2b960807d2bc1e70d443ef6de9090aa38b582a0e7f9cef98216271`  
		Last Modified: Wed, 08 Oct 2025 04:08:17 GMT  
		Size: 29.1 KB (29066 bytes)  
		MIME: application/vnd.in-toto+json
