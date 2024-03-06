## `mongo:5-focal`

```console
$ docker pull mongo@sha256:3aa6245ce2fdb3eac1cb99c518c33295a412d16388ffdf842a58624cf10219d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:5-focal` - linux; amd64

```console
$ docker pull mongo@sha256:d1b8a7b77424347397653ab8ff500c66b1e9979b4cebf826951d37b0d3966721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.7 MB (263722413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2070962e76e18a7a91ee3b8f031f82c9d1bbb6dbf35cbee794b0f05efee13644`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 16 Feb 2024 21:32:49 GMT
ARG RELEASE
# Fri, 16 Feb 2024 21:32:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 21:32:52 GMT
ADD file:a25798f31219000d6a82d2c9258743926b1a400530d12dbb1eadf2c2519f9888 in / 
# Fri, 16 Feb 2024 21:32:52 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 23:27:08 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Thu, 29 Feb 2024 23:27:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 23:27:08 GMT
ENV GOSU_VERSION=1.17
# Thu, 29 Feb 2024 23:27:08 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 29 Feb 2024 23:27:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-5.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 29 Feb 2024 23:27:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Feb 2024 23:27:08 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 29 Feb 2024 23:27:08 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 29 Feb 2024 23:27:08 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 29 Feb 2024 23:27:08 GMT
ENV MONGO_MAJOR=5.0
# Thu, 29 Feb 2024 23:27:08 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Thu, 29 Feb 2024 23:27:08 GMT
ENV MONGO_VERSION=5.0.25
# Thu, 29 Feb 2024 23:27:08 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Thu, 29 Feb 2024 23:27:08 GMT
VOLUME [/data/db /data/configdb]
# Thu, 29 Feb 2024 23:27:08 GMT
ENV HOME=/data/db
# Thu, 29 Feb 2024 23:27:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 Feb 2024 23:27:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Feb 2024 23:27:08 GMT
EXPOSE map[27017/tcp:{}]
# Thu, 29 Feb 2024 23:27:08 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:17d0386c2fff30a5b92652bbef2b84639dba9b9f17bdbb819c8d10badd827fdb`  
		Last Modified: Fri, 16 Feb 2024 21:40:52 GMT  
		Size: 27.5 MB (27514312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:915bad942312c536ce19926b70ec95f2416f5e2227a8467c7a7a95c03a45e053`  
		Last Modified: Wed, 06 Mar 2024 02:57:01 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7edeb543901f169cbb925e7a4e40a6b462c14094008fe463b4eacc066fbdd60`  
		Last Modified: Wed, 06 Mar 2024 02:57:02 GMT  
		Size: 3.1 MB (3076203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd854cd7b098d3e9d40f16754e2501a634f7c2dcf9565d68eff6b9b0f8e3a894`  
		Last Modified: Wed, 06 Mar 2024 02:57:02 GMT  
		Size: 1.1 MB (1091335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b376b6debcb97be7e5a62de07846cf9673e4da53bb52f97252e26349bded1fda`  
		Last Modified: Wed, 06 Mar 2024 02:56:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0f340988bc529a30fed23e3c2e6cfc3e938d90d023be365ee8b1ade410a840`  
		Last Modified: Wed, 06 Mar 2024 02:57:02 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a001dec272780e29072f082a9d52303554dc3119d1e518fe35532545da4df584`  
		Last Modified: Wed, 06 Mar 2024 02:57:06 GMT  
		Size: 232.0 MB (232033405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b0e72590abb741ff677074bbf5deac10b75625ef2a6a8fa12b6b878e128c0f`  
		Last Modified: Wed, 06 Mar 2024 02:57:03 GMT  
		Size: 5.0 KB (4998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:5-focal` - unknown; unknown

```console
$ docker pull mongo@sha256:75ad2fc9d4edf6f4a2f4196137251a82d3cd0c48989a5271c44f9b263ca14c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3025614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071dcedc30702b836204ab0b80ef6c5fcaa56a87c5d8490dd82ea0b934709a11`

```dockerfile
```

-	Layers:
	-	`sha256:813fc64d3dd33c07e59e95b93e0edbf7aa11fee06fd5a8216d06965f6d93af6a`  
		Last Modified: Wed, 06 Mar 2024 02:57:02 GMT  
		Size: 3.0 MB (2998782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1be923897f704d1a6570fc48b21411b303125c672cda9d38dff744f8034d4e60`  
		Last Modified: Wed, 06 Mar 2024 02:57:02 GMT  
		Size: 26.8 KB (26832 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:5-focal` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:540cbf85c2b602a6ffe80dda92f6fbc85db39695fe06ff6bf028a9f5fbd426ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.1 MB (256126542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16470b7e9a71d98b9354d17869304520c350ecd4de30751040fe93884211941e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 16 Feb 2024 19:15:01 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:15:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:15:06 GMT
ADD file:a8303c80b47ec165c276111aa6f98ee877e4da60ddafa00b7547032a3de7935d in / 
# Fri, 16 Feb 2024 19:15:06 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 23:27:08 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Thu, 29 Feb 2024 23:27:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 23:27:08 GMT
ENV GOSU_VERSION=1.17
# Thu, 29 Feb 2024 23:27:08 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 29 Feb 2024 23:27:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-5.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 29 Feb 2024 23:27:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Feb 2024 23:27:08 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 29 Feb 2024 23:27:08 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 29 Feb 2024 23:27:08 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 29 Feb 2024 23:27:08 GMT
ENV MONGO_MAJOR=5.0
# Thu, 29 Feb 2024 23:27:08 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Thu, 29 Feb 2024 23:27:08 GMT
ENV MONGO_VERSION=5.0.25
# Thu, 29 Feb 2024 23:27:08 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Thu, 29 Feb 2024 23:27:08 GMT
VOLUME [/data/db /data/configdb]
# Thu, 29 Feb 2024 23:27:08 GMT
ENV HOME=/data/db
# Thu, 29 Feb 2024 23:27:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 Feb 2024 23:27:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Feb 2024 23:27:08 GMT
EXPOSE map[27017/tcp:{}]
# Thu, 29 Feb 2024 23:27:08 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:6aae4cfdd5a10a8b0554e75c4c14ae38022a0c8f08dc5d769a735c705670cab7`  
		Last Modified: Fri, 16 Feb 2024 21:40:59 GMT  
		Size: 26.0 MB (25974391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b819790bf6c5d972784a5f81e9609e790c0c8374ad9148d6db4183189adb696`  
		Last Modified: Wed, 06 Mar 2024 17:25:30 GMT  
		Size: 1.8 KB (1799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7c87e20203f1f413df42b60f86241f3ec9cc2a05b6c4a072c0b20400c75e8c`  
		Last Modified: Wed, 06 Mar 2024 17:25:30 GMT  
		Size: 2.9 MB (2929622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814732339515debd2ecb1fec71e25823c95b1c15e6022f17111665a4d2d9e8ae`  
		Last Modified: Wed, 06 Mar 2024 17:25:30 GMT  
		Size: 1.0 MB (1023700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6151bf224fa05f14d8cfcfd4e90014758ee44f9d82fe3f404b828a348231ca3b`  
		Last Modified: Wed, 06 Mar 2024 17:25:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d461762ba8ab71f2ee8480484eb8fe31744d1fa75910a642e6ee577dcec4f4`  
		Last Modified: Wed, 06 Mar 2024 17:25:31 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754ad922ae051eb3553a38ad7a74e581a47512bec9efadadf3bec1b95be51aac`  
		Last Modified: Wed, 06 Mar 2024 17:25:37 GMT  
		Size: 226.2 MB (226191656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d06cbb3f864ee31e996ae734d2a6080d6e573094c1d4d4232ad95296f2166d`  
		Last Modified: Wed, 06 Mar 2024 17:25:31 GMT  
		Size: 5.0 KB (4998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:5-focal` - unknown; unknown

```console
$ docker pull mongo@sha256:07bc737cd34004697ee2c553455a607c5fbdc58b30bb51f3bd8070d8706acc81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3025700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:354e832c81844797d8173ae52b2411c90a99af15d175db4217e2066c218f7c53`

```dockerfile
```

-	Layers:
	-	`sha256:ee5b92a59e29fedca14add7e8679a6df8699f0469eeac3aac1d63f74f136892c`  
		Last Modified: Wed, 06 Mar 2024 17:25:30 GMT  
		Size: 3.0 MB (2999015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cb5092f0f18a7d4808adca747b8b10e0ff5802f21ea5bb67047e55e54461495`  
		Last Modified: Wed, 06 Mar 2024 17:25:30 GMT  
		Size: 26.7 KB (26685 bytes)  
		MIME: application/vnd.in-toto+json
