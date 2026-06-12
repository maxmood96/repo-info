## `mongo:noble`

```console
$ docker pull mongo@sha256:060d95983e8c81fb270588865606e9a5c3bb8371ebb3e96057d57f577382c49a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:noble` - linux; amd64

```console
$ docker pull mongo@sha256:6c7889031d2ff57f7dd3711398587d1c8b05a68439aab02dd880ed1e0691cfbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.6 MB (338632309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e9809b5a1bf31577123d6704296cb5881617cf226251ef9afe4f6f1719b818`
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
# Fri, 12 Jun 2026 19:08:51 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Fri, 12 Jun 2026 19:08:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jun 2026 19:09:04 GMT
ENV GOSU_VERSION=1.19
# Fri, 12 Jun 2026 19:09:04 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 12 Jun 2026 19:09:04 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Fri, 12 Jun 2026 19:09:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 12 Jun 2026 19:09:04 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 12 Jun 2026 19:09:04 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 12 Jun 2026 19:09:04 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 12 Jun 2026 19:09:04 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 12 Jun 2026 19:09:04 GMT
ENV MONGO_MAJOR=8.2
# Fri, 12 Jun 2026 19:09:04 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/$MONGO_PACKAGE/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/$MONGO_PACKAGE.list" # buildkit
# Fri, 12 Jun 2026 19:09:04 GMT
ENV MONGO_VERSION=8.2.11
# Fri, 12 Jun 2026 19:09:21 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Fri, 12 Jun 2026 19:09:21 GMT
VOLUME [/data/db /data/configdb]
# Fri, 12 Jun 2026 19:09:21 GMT
ENV HOME=/data/db
# Fri, 12 Jun 2026 19:09:21 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Fri, 12 Jun 2026 19:09:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Jun 2026 19:09:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2026 19:09:21 GMT
EXPOSE map[27017/tcp:{}]
# Fri, 12 Jun 2026 19:09:21 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e8c2375bc5e9dfd10897eee880e13d2bffb9e7082d60e85afdda725546d93b`  
		Last Modified: Fri, 12 Jun 2026 19:09:56 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a96a9518c5e48545e5bd6b3f4f204d22864e411274dad47538c43e85b16eb8`  
		Last Modified: Fri, 12 Jun 2026 19:09:56 GMT  
		Size: 3.9 MB (3918150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f963550fd6abab08e5b836606b84e1e98117971726f41cf30694d0851c46eb`  
		Last Modified: Fri, 12 Jun 2026 19:09:55 GMT  
		Size: 933.9 KB (933877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b21dc82064b04e9e5ca5b3611d369182107c2c0d43cd00cd5df179c4b1b9ab`  
		Last Modified: Fri, 12 Jun 2026 19:09:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a675cf1444f83fd5a9b79755b69bb620e73d149ce06cf09b9244c4626542a3a1`  
		Last Modified: Fri, 12 Jun 2026 19:09:57 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12382c3b403995631c7c237d30809996a5f2e06ad6df4e93bd1663886e97e995`  
		Last Modified: Fri, 12 Jun 2026 19:10:03 GMT  
		Size: 304.0 MB (304040876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deec6ab29319f52dc41d5d1addb04ff1b35a4368413d6818d8b22d49813ccc11`  
		Last Modified: Fri, 12 Jun 2026 19:09:57 GMT  
		Size: 5.0 KB (5001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:noble` - unknown; unknown

```console
$ docker pull mongo@sha256:57c472f94b814eac43510afbddb1c2efb7ff7a1a3c19580dac885b1fcfc60034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2689198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65c287ac020eea1cdd4b186b6b3486067cc4018c4cad2d853d8fe519cf7ed712`

```dockerfile
```

-	Layers:
	-	`sha256:abae127182622c05e1c684bdd1fdd152ff0e0aae036e8c1abcf70cb99ee631ef`  
		Last Modified: Fri, 12 Jun 2026 19:09:56 GMT  
		Size: 2.7 MB (2660457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3955da3112c5b814f954b72475a392438be8449c4c1299d8503e879f1a60cc6`  
		Last Modified: Fri, 12 Jun 2026 19:09:56 GMT  
		Size: 28.7 KB (28741 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:noble` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:8af30bfe6621044afae354c9be2f6110dcecf8d2338861d4d50fa42206cc7ecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.1 MB (323111506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54152f5bb8950cb6bdb6c8c0658eb299128338f685afa467c0d8186fe245010`
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
# Fri, 12 Jun 2026 19:08:45 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Fri, 12 Jun 2026 19:08:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jun 2026 19:09:01 GMT
ENV GOSU_VERSION=1.19
# Fri, 12 Jun 2026 19:09:01 GMT
ENV JSYAML_VERSION=3.13.1
# Fri, 12 Jun 2026 19:09:01 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Fri, 12 Jun 2026 19:09:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 12 Jun 2026 19:09:01 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 12 Jun 2026 19:09:01 GMT
ARG MONGO_PACKAGE=mongodb-org
# Fri, 12 Jun 2026 19:09:01 GMT
ARG MONGO_REPO=repo.mongodb.org
# Fri, 12 Jun 2026 19:09:01 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Fri, 12 Jun 2026 19:09:01 GMT
ENV MONGO_MAJOR=8.2
# Fri, 12 Jun 2026 19:09:01 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/$MONGO_PACKAGE/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/$MONGO_PACKAGE.list" # buildkit
# Fri, 12 Jun 2026 19:09:01 GMT
ENV MONGO_VERSION=8.2.11
# Fri, 12 Jun 2026 19:09:21 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Fri, 12 Jun 2026 19:09:21 GMT
VOLUME [/data/db /data/configdb]
# Fri, 12 Jun 2026 19:09:21 GMT
ENV HOME=/data/db
# Fri, 12 Jun 2026 19:09:21 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Fri, 12 Jun 2026 19:09:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 12 Jun 2026 19:09:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Jun 2026 19:09:21 GMT
EXPOSE map[27017/tcp:{}]
# Fri, 12 Jun 2026 19:09:21 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b77ccde538ad884da2252e5915899e285b1f3af2ba49bb1b410e68155bb8ae4`  
		Last Modified: Fri, 12 Jun 2026 19:09:56 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c07ef21bab6601bfa52e9fb636b64a551b94d107ae92a7ff1801f7d0f4232e9`  
		Last Modified: Fri, 12 Jun 2026 19:09:56 GMT  
		Size: 3.7 MB (3713228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deff5935811e7925bfaa1a16278ff34fe0762905d5524f0c6eb74c64bc9a2841`  
		Last Modified: Fri, 12 Jun 2026 19:09:56 GMT  
		Size: 886.2 KB (886235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2830fe8a9e3dde8a27c0bcf6b34b1ae031a9aecb8629751ba88e599b8cec656`  
		Last Modified: Fri, 12 Jun 2026 19:09:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7adb90dbb4c6cd2bd4e9445095351bad78880bffc6ca7e67cbed3c9d60105666`  
		Last Modified: Fri, 12 Jun 2026 19:09:57 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c076c0599234fa1ffbda0472cb09ab801626baf0ca397dbcfe9240fb3886e8a`  
		Last Modified: Fri, 12 Jun 2026 19:10:04 GMT  
		Size: 289.6 MB (289629035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b7a15996065ad8e56e4e3dc5b0bc0ba14e094e3efa38734c7d1541c7baa456`  
		Last Modified: Fri, 12 Jun 2026 19:09:57 GMT  
		Size: 5.0 KB (5003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:noble` - unknown; unknown

```console
$ docker pull mongo@sha256:d18a3cb1cae69b67dedcdc09fafd6d2b0142e261d9f46c6660cfa51ce21f02b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2690561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1fb65f14e5986526534df087a37ad26b4a0f6a24c3054c05096ba2bc94c6a3a`

```dockerfile
```

-	Layers:
	-	`sha256:86fb79536def63d3de583a0cc77d133b0654ba16db67bb3c5c1ef4f73e7733de`  
		Last Modified: Fri, 12 Jun 2026 19:09:56 GMT  
		Size: 2.7 MB (2661593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0a1081b6a8d689e0bf995bc38057273043e236bab179ca45cc235e7abd2b1b6`  
		Last Modified: Fri, 12 Jun 2026 19:09:56 GMT  
		Size: 29.0 KB (28968 bytes)  
		MIME: application/vnd.in-toto+json
