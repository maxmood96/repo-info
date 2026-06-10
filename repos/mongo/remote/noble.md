## `mongo:noble`

```console
$ docker pull mongo@sha256:439371de4ada674320d417898402ef37b904d48c16dbc3968e0e17ef3b8ba00e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:noble` - linux; amd64

```console
$ docker pull mongo@sha256:b042b95944294d6758569c1773e44f3e9280bdf289e2a3053f669e975d496ee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.6 MB (338632330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51f1b23e69e0f702a3ee70dc7d8ae522ec29fa13c5f53d386638de52c3a6adca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Wed, 10 Jun 2026 20:11:16 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Wed, 10 Jun 2026 20:11:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jun 2026 20:11:31 GMT
ENV GOSU_VERSION=1.19
# Wed, 10 Jun 2026 20:11:31 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 10 Jun 2026 20:11:31 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Wed, 10 Jun 2026 20:11:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 10 Jun 2026 20:11:31 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 10 Jun 2026 20:11:31 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 10 Jun 2026 20:11:31 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 10 Jun 2026 20:11:31 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 10 Jun 2026 20:11:31 GMT
ENV MONGO_MAJOR=8.2
# Wed, 10 Jun 2026 20:11:31 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/$MONGO_PACKAGE/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/$MONGO_PACKAGE.list" # buildkit
# Wed, 10 Jun 2026 20:11:31 GMT
ENV MONGO_VERSION=8.2.10
# Wed, 10 Jun 2026 20:11:51 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Wed, 10 Jun 2026 20:11:51 GMT
VOLUME [/data/db /data/configdb]
# Wed, 10 Jun 2026 20:11:51 GMT
ENV HOME=/data/db
# Wed, 10 Jun 2026 20:11:51 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Wed, 10 Jun 2026 20:11:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 20:11:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 20:11:51 GMT
EXPOSE map[27017/tcp:{}]
# Wed, 10 Jun 2026 20:11:51 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222c00b8608f2fe69e8dabb7b34efea2a8853aad3d2c4f48345b221b8598ae01`  
		Last Modified: Wed, 10 Jun 2026 20:12:26 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:668d28e62c9b0184f936c004133374ba7e63b3bc09aef8453ca7cd580a0f3c4e`  
		Last Modified: Wed, 10 Jun 2026 20:12:26 GMT  
		Size: 3.9 MB (3918222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f2397e91a36bc58f97a128fa220248fbce728a161273c0b023e50b526df96b`  
		Last Modified: Wed, 10 Jun 2026 20:12:26 GMT  
		Size: 933.9 KB (933903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c391ff3ec475d1f356b867852989af8755ab0715ee705e3aeb37fa048b7e79`  
		Last Modified: Wed, 10 Jun 2026 20:12:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c3c06c76fdd0bb2d53dc3824770f187ad353c5ecc408723341b10a57943903`  
		Last Modified: Wed, 10 Jun 2026 20:12:27 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb149f6b2a83bad2cda3cd5cea16837e52a64fbe8cb215427945126c72202a8`  
		Last Modified: Wed, 10 Jun 2026 20:12:36 GMT  
		Size: 304.0 MB (304040798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5438145c5cdc576d25455c2df10981990f41a1aedaf0c7ea11603981b4667872`  
		Last Modified: Wed, 10 Jun 2026 20:12:28 GMT  
		Size: 5.0 KB (5004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:noble` - unknown; unknown

```console
$ docker pull mongo@sha256:7c7ea1d0f15131160f9b3664ba4720c09176a72c7cc6cd242ccc7a48b1015350
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2689198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc370da3cd14e00414c913263e33e741bfa06c52a87d832a4aef8928ed02c178`

```dockerfile
```

-	Layers:
	-	`sha256:5df5d0ad4feb85ced446201aafa819a5771322351e27ff2b316209bdd11f3783`  
		Last Modified: Wed, 10 Jun 2026 20:12:26 GMT  
		Size: 2.7 MB (2660457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:677b0b3f2bd80f66542f90fd2978fe416c01d076962cd00bb7f50cde2bef8a20`  
		Last Modified: Wed, 10 Jun 2026 20:12:26 GMT  
		Size: 28.7 KB (28741 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:noble` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:b12cbf9a7768fc4533e2a5e1d4e2246076e8798177e0e23770728a329930f1de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.1 MB (323110266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e67f8ae3d72539713302f83caa192c2006688a4e111984c8466ee40bffde90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Wed, 10 Jun 2026 20:11:00 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Wed, 10 Jun 2026 20:11:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 10 Jun 2026 20:11:19 GMT
ENV GOSU_VERSION=1.19
# Wed, 10 Jun 2026 20:11:19 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 10 Jun 2026 20:11:19 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Wed, 10 Jun 2026 20:11:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 10 Jun 2026 20:11:19 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 10 Jun 2026 20:11:19 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 10 Jun 2026 20:11:19 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 10 Jun 2026 20:11:19 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 10 Jun 2026 20:11:19 GMT
ENV MONGO_MAJOR=8.2
# Wed, 10 Jun 2026 20:11:19 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/$MONGO_PACKAGE/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/$MONGO_PACKAGE.list" # buildkit
# Wed, 10 Jun 2026 20:11:19 GMT
ENV MONGO_VERSION=8.2.10
# Wed, 10 Jun 2026 20:11:40 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Wed, 10 Jun 2026 20:11:40 GMT
VOLUME [/data/db /data/configdb]
# Wed, 10 Jun 2026 20:11:40 GMT
ENV HOME=/data/db
# Wed, 10 Jun 2026 20:11:40 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Wed, 10 Jun 2026 20:11:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 20:11:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 20:11:40 GMT
EXPOSE map[27017/tcp:{}]
# Wed, 10 Jun 2026 20:11:40 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204f2cfc7f75781e97d17401f621ac22babc35529ba4513a8aa7dd161d9e13c2`  
		Last Modified: Wed, 10 Jun 2026 20:12:14 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5522b4b4826bd4fe221f1e9a086eebc448312eaa3c04f1b9c5c6dca50800ffb8`  
		Last Modified: Wed, 10 Jun 2026 20:12:14 GMT  
		Size: 3.7 MB (3713271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9879686bbc540914438a86da77374435b3f90b5b417161dad924c94ac724c2a3`  
		Last Modified: Wed, 10 Jun 2026 20:12:14 GMT  
		Size: 886.2 KB (886223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2342f3fd9f50524b417777744d2a09d05c0d0e59e0c61968b0fbf515e58b0381`  
		Last Modified: Wed, 10 Jun 2026 20:12:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f78cd883526298836a745910d54007a1f614ef3241c73a35ab50f28a211986`  
		Last Modified: Wed, 10 Jun 2026 20:12:15 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12472d32c6cfcbdeccef876e387b4dd365c617e324c78d383e1848c2bd8814a`  
		Last Modified: Wed, 10 Jun 2026 20:12:22 GMT  
		Size: 289.6 MB (289627765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1849bc3cfd35ffaa0340fc42202cf1a3ac7508847906423805641a2a5f2e80`  
		Last Modified: Wed, 10 Jun 2026 20:12:16 GMT  
		Size: 5.0 KB (5003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:noble` - unknown; unknown

```console
$ docker pull mongo@sha256:e196f6a4aff9906f8cd3385e48d8d97fea7de6ac22d95a2616e071d6bd0a3b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2690561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03a9d25ab536dd9735317707bdc9a20a990feadba58aacac38710d7e493c3369`

```dockerfile
```

-	Layers:
	-	`sha256:b5ddb8fc729cd03aa1ba07c6df20cc0a30d22538b12e19237232184ad0c8c183`  
		Last Modified: Wed, 10 Jun 2026 20:12:14 GMT  
		Size: 2.7 MB (2661593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c050d302ec8f9b8678c328508af59ce103514b7635e2ba89078687a77b8bad05`  
		Last Modified: Wed, 10 Jun 2026 20:12:14 GMT  
		Size: 29.0 KB (28968 bytes)  
		MIME: application/vnd.in-toto+json
