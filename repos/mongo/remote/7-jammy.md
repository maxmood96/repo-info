## `mongo:7-jammy`

```console
$ docker pull mongo@sha256:074c773cda61f791523e2a6a8536a4d1191595641dbcd723008a6d039719812e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:7-jammy` - linux; amd64

```console
$ docker pull mongo@sha256:2ed4a43fac59b57dafcb567745a3ded0f8d581d30e06db062922f48320a5df91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.8 MB (293807504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30dcf348e2baf03821819d979618dc179384e5d150c5cc8dc24443b9e0e1a191`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 18:09:58 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Tue, 17 Mar 2026 18:10:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 18:10:19 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 18:10:19 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 17 Mar 2026 18:10:19 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Tue, 17 Mar 2026 18:10:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 18:10:19 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 18:10:19 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 17 Mar 2026 18:10:19 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 17 Mar 2026 18:10:19 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 17 Mar 2026 18:10:19 GMT
ENV MONGO_MAJOR=7.0
# Tue, 17 Mar 2026 18:10:19 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Tue, 17 Mar 2026 18:10:19 GMT
ENV MONGO_VERSION=7.0.31
# Tue, 17 Mar 2026 18:10:40 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Tue, 17 Mar 2026 18:10:40 GMT
VOLUME [/data/db /data/configdb]
# Tue, 17 Mar 2026 18:10:40 GMT
ENV HOME=/data/db
# Tue, 17 Mar 2026 18:10:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 18:10:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 18:10:40 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 17 Mar 2026 18:10:40 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b1e87c2feac56f629a5371e78e81765e8599adfb5b4c19d94a954e571788d1`  
		Last Modified: Tue, 17 Mar 2026 18:11:13 GMT  
		Size: 1.8 KB (1780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e159ac627d773741622dfd48a941b0c0f5d5a68485f99bc9679d4a9f59ebde`  
		Last Modified: Tue, 17 Mar 2026 18:11:13 GMT  
		Size: 1.5 MB (1513763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919533137d609ca918394267f0473b1edb39c58065056e53257108e921cd0e2a`  
		Last Modified: Tue, 17 Mar 2026 18:11:13 GMT  
		Size: 898.0 KB (898049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a332d882040e0780c1b47bda328b3fbd6644bd3da67b5fb386e85a65feb49c73`  
		Last Modified: Tue, 17 Mar 2026 18:11:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3208b27941d70adb7bd6f3c2f013a7d7e53c3693159c4c51c69211152254d04`  
		Last Modified: Tue, 17 Mar 2026 18:11:14 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0d79bd4c2e6393a9425580b9c3b2091ccfa5c2b2d1c1e287cedd6a06726ccf`  
		Last Modified: Tue, 17 Mar 2026 18:11:20 GMT  
		Size: 261.9 MB (261850011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc54214ac6a5048b4826adb3dde246af48a77f934e29d6bb827a65af776e12c`  
		Last Modified: Tue, 17 Mar 2026 18:11:15 GMT  
		Size: 5.0 KB (5002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:7-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:190f6f6a9e5198efcd992e5732e2d7678414a28c4b85814ebcdb4d2125e4f2ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3246775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3262bac0616d8cb157e0752ccd325cd6d29ccb642a7fd9b6547d9c802fc44a77`

```dockerfile
```

-	Layers:
	-	`sha256:f3471e3684c2c14affed0aef134db8a76c397cefed09f399e44867eebecc8884`  
		Last Modified: Tue, 17 Mar 2026 18:11:13 GMT  
		Size: 3.2 MB (3218835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c899fefe3569b8c99c63e20a7bd3eb79d3939dd9f4c8ff509f33c47d962cc5b`  
		Last Modified: Tue, 17 Mar 2026 18:11:13 GMT  
		Size: 27.9 KB (27940 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:7-jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:f72875bd1481cfbb8f05429aa898250e5e3188cdafafa81e95d088d3cdf45fdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.8 MB (279806581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc8cea17166713cba43ac594733388a41f4a61f6bd1874484b37de00cc79deb9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 18:09:49 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Tue, 17 Mar 2026 18:09:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 18:10:14 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 18:10:14 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 17 Mar 2026 18:10:14 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Tue, 17 Mar 2026 18:10:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 18:10:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 18:10:14 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 17 Mar 2026 18:10:14 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 17 Mar 2026 18:10:14 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 17 Mar 2026 18:10:14 GMT
ENV MONGO_MAJOR=7.0
# Tue, 17 Mar 2026 18:10:14 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Tue, 17 Mar 2026 18:10:14 GMT
ENV MONGO_VERSION=7.0.31
# Tue, 17 Mar 2026 18:10:37 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Tue, 17 Mar 2026 18:10:37 GMT
VOLUME [/data/db /data/configdb]
# Tue, 17 Mar 2026 18:10:37 GMT
ENV HOME=/data/db
# Tue, 17 Mar 2026 18:10:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 18:10:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 18:10:37 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 17 Mar 2026 18:10:37 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc93ca5076135820dc756347411616e8913d62a962a2f01b5597c195338f5349`  
		Last Modified: Tue, 17 Mar 2026 18:11:07 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a32f73ce5a5fd510f7ab577b4d4bac79b677eb0b3f039b3b15c4330322ec65`  
		Last Modified: Tue, 17 Mar 2026 18:11:07 GMT  
		Size: 1.5 MB (1483230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5330d49b71d29d69e4c492088d774bedf2a93f617e1b02d8b870478d8366b0`  
		Last Modified: Tue, 17 Mar 2026 18:11:07 GMT  
		Size: 850.5 KB (850524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ebaa82763663d0e60c26956ba678f4f7751cf63a9419b760660737095a694c`  
		Last Modified: Tue, 17 Mar 2026 18:11:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ae5d930dd0e01b5d126962fb69babde0bbca45d63c5b45c731a79fe5c982f1`  
		Last Modified: Tue, 17 Mar 2026 18:11:08 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35003752e75ed6cd9a525374b4c5c53d5eac530af9fda4ea45b3f807f1bb7175`  
		Last Modified: Tue, 17 Mar 2026 18:11:13 GMT  
		Size: 250.1 MB (250076629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ac9bb295fbb525bc20974bbb8ea2c27ecc0b437ea1ce44666aded85ea782ef`  
		Last Modified: Tue, 17 Mar 2026 18:11:08 GMT  
		Size: 5.0 KB (5006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:7-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:ad5aaddbef8d3af4fc794c3cbe15bc108ca306382ec6052156893b0ad383defd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3247299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f29cb909d83e932647cdd7ff821a94f119b9eec33904a2cbcb01794753eb69f5`

```dockerfile
```

-	Layers:
	-	`sha256:5dfa936da0a0dd38488f387987e12a9fd63b0ae38fe118e755677420399403e8`  
		Last Modified: Tue, 17 Mar 2026 18:11:07 GMT  
		Size: 3.2 MB (3219154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb505c2f3e7037a322303bc43f8d001f957c746823e3e69ba32635b0f1e7e3a2`  
		Last Modified: Tue, 17 Mar 2026 18:11:07 GMT  
		Size: 28.1 KB (28145 bytes)  
		MIME: application/vnd.in-toto+json
