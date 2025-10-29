## `mongo:8-noble`

```console
$ docker pull mongo@sha256:9f98cd2c05abfef5c4fdfa8ea668b09ab9a7c23226d6b84cabfed035f01403c9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:8-noble` - linux; amd64

```console
$ docker pull mongo@sha256:86ef52c3f024205afe0496bee9100b04c00bd9e025e16697f6c0b425b289b840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.5 MB (323525808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b59ba0909632de13b5bcaa71a9f2d3ec0576e43323d30155b00a71b638541f`
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
# Tue, 28 Oct 2025 19:05:36 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Tue, 28 Oct 2025 19:05:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Oct 2025 19:05:57 GMT
ENV GOSU_VERSION=1.19
# Tue, 28 Oct 2025 19:05:57 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 28 Oct 2025 19:05:57 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Tue, 28 Oct 2025 19:05:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 28 Oct 2025 19:05:57 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 28 Oct 2025 19:05:57 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 28 Oct 2025 19:05:57 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 28 Oct 2025 19:05:57 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 28 Oct 2025 19:05:57 GMT
ENV MONGO_MAJOR=8.2
# Tue, 28 Oct 2025 19:05:57 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Tue, 28 Oct 2025 19:05:57 GMT
ENV MONGO_VERSION=8.2.1
# Tue, 28 Oct 2025 19:06:16 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Tue, 28 Oct 2025 19:06:16 GMT
VOLUME [/data/db /data/configdb]
# Tue, 28 Oct 2025 19:06:16 GMT
ENV HOME=/data/db
# Tue, 28 Oct 2025 19:06:16 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Tue, 28 Oct 2025 19:06:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 28 Oct 2025 19:06:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Oct 2025 19:06:16 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 28 Oct 2025 19:06:16 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34baad99576288ad2cfe5cf1b6f55b5f5dde6e1f4279f44c5251e1577fa51bcb`  
		Last Modified: Tue, 28 Oct 2025 19:07:19 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d6f7cf8e15d823ddddea522da5b09154872761bcbf1e87e3fe29df11dc1a773`  
		Last Modified: Tue, 28 Oct 2025 19:07:20 GMT  
		Size: 1.5 MB (1509316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90aba9940a7678e05211d629056a7ec525441c4e3cfc0d4cd5fd41f010482b8`  
		Last Modified: Tue, 28 Oct 2025 19:07:20 GMT  
		Size: 933.7 KB (933717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3652024acdb07dbadca1c12566fe621197fa5e4e05ced3c9a5aa6597407b26`  
		Last Modified: Tue, 28 Oct 2025 19:07:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74522aa03d0090b332dc0849dc7a35afc5457b91af0b6503923beb09640d03ca`  
		Last Modified: Tue, 28 Oct 2025 19:07:19 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8dccf1f4c1ddd75101d8ad0443c692ba045bd03a54fed3d1aa85be1775f0d1`  
		Last Modified: Tue, 28 Oct 2025 20:14:02 GMT  
		Size: 291.4 MB (291353028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ada45c862e44f23ec93ac1b2584641d96f49a45b6c48778a14c52726f696de`  
		Last Modified: Tue, 28 Oct 2025 19:07:20 GMT  
		Size: 5.0 KB (5002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:8-noble` - unknown; unknown

```console
$ docker pull mongo@sha256:b3dc807672e136ef11533a0a99bdd16ccdf214ec67ed26b88189950e021ff829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2695084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5584c341777c07dfc9044391b3bb114cad4ec3949b295763ac9f42d587917d2d`

```dockerfile
```

-	Layers:
	-	`sha256:08908a091c3bf1886a50d27e5d0533ba133828b76af0f5357995b1a48de84ce8`  
		Last Modified: Tue, 28 Oct 2025 22:08:17 GMT  
		Size: 2.7 MB (2666292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:876c470fe37e381258ef82fb1f5ab5d9ba36d585c066459283a68a161fef4721`  
		Last Modified: Tue, 28 Oct 2025 22:08:18 GMT  
		Size: 28.8 KB (28792 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:8-noble` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:8d40402af138bac7952bf43d83da34f89be47683a522724f9a996a979098f6c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.5 MB (309500636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d659cebf5e942f7fe81bfdcfcc32dafe271be1e688a6612706c3986af87bb6c`
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
# Tue, 28 Oct 2025 19:05:42 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Tue, 28 Oct 2025 19:05:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Oct 2025 19:06:02 GMT
ENV GOSU_VERSION=1.19
# Tue, 28 Oct 2025 19:06:02 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 28 Oct 2025 19:06:02 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Tue, 28 Oct 2025 19:06:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 28 Oct 2025 19:06:02 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 28 Oct 2025 19:06:02 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 28 Oct 2025 19:06:02 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 28 Oct 2025 19:06:02 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 28 Oct 2025 19:06:02 GMT
ENV MONGO_MAJOR=8.2
# Tue, 28 Oct 2025 19:06:02 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Tue, 28 Oct 2025 19:06:02 GMT
ENV MONGO_VERSION=8.2.1
# Tue, 28 Oct 2025 19:06:20 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Tue, 28 Oct 2025 19:06:20 GMT
VOLUME [/data/db /data/configdb]
# Tue, 28 Oct 2025 19:06:20 GMT
ENV HOME=/data/db
# Tue, 28 Oct 2025 19:06:20 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Tue, 28 Oct 2025 19:06:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 28 Oct 2025 19:06:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Oct 2025 19:06:20 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 28 Oct 2025 19:06:20 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a637dbfff7e5048c95cc9654b60b6870b3660530c6dfb42ef8b4e332709b0aa7`  
		Last Modified: Tue, 28 Oct 2025 19:07:18 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9047ace63cacb058263605a6c1675a47bc7b2acdab6736ba2376342b570f7c`  
		Last Modified: Tue, 28 Oct 2025 19:07:19 GMT  
		Size: 1.5 MB (1494407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02cd4cf700214e8fa3f0926cdb1c9e0f33448ca977f44b8eb8694aabccd95318`  
		Last Modified: Tue, 28 Oct 2025 19:07:18 GMT  
		Size: 886.2 KB (886152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb5d357a0251725bf789d8161edca1d6060c6d0e5b05b6626d0b9564ab764fd`  
		Last Modified: Tue, 28 Oct 2025 19:07:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007bf0024f67b18914f7c0526c62657e3f11d7b8f8e0c6549bc47921f7d770a5`  
		Last Modified: Tue, 28 Oct 2025 19:07:18 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67fd8af3998d13d2a4f4445fc216efab3f455b5159e712952a345e9286232eb5`  
		Last Modified: Tue, 28 Oct 2025 21:05:05 GMT  
		Size: 278.3 MB (278251764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d702312e81096cdff4461194b04ca6b2bc6f9c1fdd13571f23f4c31714e1f23d`  
		Last Modified: Tue, 28 Oct 2025 19:07:18 GMT  
		Size: 5.0 KB (5003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:8-noble` - unknown; unknown

```console
$ docker pull mongo@sha256:2f6ceaa8fe6024ad13032d5eb2343d7233f0f100d4243c0cd761aff123e65081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2696447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f651d6408c03816be1068b89ba5e4f3ee9529699b8301806e9827294929f2b99`

```dockerfile
```

-	Layers:
	-	`sha256:7a8d4a7e2da5bf8fbed91ad6e56a5d9187d060b71c57c26c286dd9e828f50862`  
		Last Modified: Tue, 28 Oct 2025 22:08:21 GMT  
		Size: 2.7 MB (2667428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:421976a0d5f1116fba482780b595677d6f0a0ba758be678564849146f5d0a9b1`  
		Last Modified: Tue, 28 Oct 2025 22:08:22 GMT  
		Size: 29.0 KB (29019 bytes)  
		MIME: application/vnd.in-toto+json
