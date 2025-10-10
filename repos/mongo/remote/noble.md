## `mongo:noble`

```console
$ docker pull mongo@sha256:953b234598fd8c6d07e0b8dfeac379c7457df43750ff448da260863706debe71
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:noble` - linux; amd64

```console
$ docker pull mongo@sha256:c05e8144b31de7e147b6a6c3dcefd97b19621bb5b42748da4214a12c0d9fd8e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.7 MB (298662631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9196ab1f1e1083d834e668b1e5ed49aca5b8012904f6a5922d0a50161646092`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
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
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f211690369e7048c17cdce8d087b0ccc8ac4091ba3229cbcbffc00715cd500a`  
		Last Modified: Thu, 09 Oct 2025 21:21:12 GMT  
		Size: 1.2 KB (1215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e20d020ae6f39f5211c80e8cbd297171bcc404bc8625af256177eb1d7d4b389f`  
		Last Modified: Thu, 09 Oct 2025 21:21:12 GMT  
		Size: 1.5 MB (1509186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c61448294a5ec2bc3a71d590f91000403f4aae18417a42a041a591fa81af93f5`  
		Last Modified: Thu, 09 Oct 2025 21:21:13 GMT  
		Size: 933.7 KB (933708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b397d908326d9210dbbca5555c1fd71a6786dabbc28ba72bbc719217985f3c`  
		Last Modified: Thu, 09 Oct 2025 21:21:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92a15b39d954733288938d0536e362728e588a4154776763fe14049c47dd456`  
		Last Modified: Thu, 09 Oct 2025 21:21:12 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c9ec5e75886c14594a14c94f821317c6b99e4794815ac89df2a08ba2c09dde1`  
		Last Modified: Thu, 09 Oct 2025 22:19:01 GMT  
		Size: 266.5 MB (266489992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92ad19150f36bde23d3514e3a6203d8ff40c4efbf2abdd37705e5d39a6a1b96`  
		Last Modified: Thu, 09 Oct 2025 21:21:12 GMT  
		Size: 5.0 KB (5001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:noble` - unknown; unknown

```console
$ docker pull mongo@sha256:7f5dd507e9dbb192a58b26149e67729473e1e8cc20059b4f4686a4c6cbd3f4e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2695150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9967b466b2e2060437f87b9248c6e1b7ca15e5260132d10c24d2ba41f1fc76`

```dockerfile
```

-	Layers:
	-	`sha256:cd6b9b36bcea3422187c1decb8f3f10a7e1a0a298c5f27f589463ed7a45c9090`  
		Last Modified: Fri, 10 Oct 2025 01:07:37 GMT  
		Size: 2.7 MB (2666310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0ec5a731ff3108a8f26fc688eac58de9a3a748fef09c0cd027b58051c1bc45b`  
		Last Modified: Fri, 10 Oct 2025 01:07:38 GMT  
		Size: 28.8 KB (28840 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:noble` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:01c18639b1a43ea4f5b711a74bc5a15014604db639de0b814d8be7cb8639eea1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286251691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63645998e0f4a0c98df36f3fab7384760713a93aced2626f14cb5f2a6969afe0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
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
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0164b2cc357eb24c2a87e6db133b2e2d3b765e9b4ddaabd0642ce8115b9e39`  
		Last Modified: Thu, 09 Oct 2025 21:22:22 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14bdb55a4ac2d75a64df5af79d1c17e3c6d353a2769a11666e835b12c8036852`  
		Last Modified: Thu, 09 Oct 2025 21:22:22 GMT  
		Size: 1.5 MB (1494455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eeee0fb9876183abf49fa4727e0e187a3ddb460ea961ccaff30303842eda67a`  
		Last Modified: Thu, 09 Oct 2025 21:22:22 GMT  
		Size: 886.2 KB (886153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f19012efbdb2b0a8cb6a777a9fd211ab6e1043c4ae0213a7d4cebc973a3bde7c`  
		Last Modified: Thu, 09 Oct 2025 21:22:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc89647002980a1361eaa988b9bd2f5234a0da5efd9d7a0e3c4f563dd7247370`  
		Last Modified: Thu, 09 Oct 2025 21:22:22 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f8af00d4552264760acc76406f7532f91954d6803a3f5611a09323c319d6d87`  
		Last Modified: Thu, 09 Oct 2025 22:18:33 GMT  
		Size: 255.0 MB (255002770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb403185da21177b51c85823655adee544c06352d19e9224645898914bc64fbd`  
		Last Modified: Thu, 09 Oct 2025 21:22:22 GMT  
		Size: 5.0 KB (5002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:noble` - unknown; unknown

```console
$ docker pull mongo@sha256:55a72986802c974ed72ae15b6a9b342d277caba63c21d7a00accf5c484a9748c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2696513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d378c5e2b0cc2555360b49c07d9b62e3d7686418a8bb06508f27f7da46f409f1`

```dockerfile
```

-	Layers:
	-	`sha256:bd831753c922992162b66ea4a321427e8395f8fc7487639991dfc956bd3a1436`  
		Last Modified: Fri, 10 Oct 2025 00:26:58 GMT  
		Size: 2.7 MB (2667446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d280d404ff1a2115e102abe44e18a124e9c513c31ae2b0db589257d9230923b`  
		Last Modified: Fri, 10 Oct 2025 00:26:56 GMT  
		Size: 29.1 KB (29067 bytes)  
		MIME: application/vnd.in-toto+json
