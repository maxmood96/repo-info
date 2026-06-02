## `mongo:8-noble`

```console
$ docker pull mongo@sha256:007773db61cb1aa44e526fb7175fc582902e67d4e6cc5f13106445767d46c818
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:8-noble` - linux; amd64

```console
$ docker pull mongo@sha256:d4e395b33d3eaa727bee364f758d403b96330ec34028759fe9886301d0c6f8d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.2 MB (336158701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3019a18b4f601516939857e652f998a4accd1dfa3dce6ca9e2bdb560a239164`
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
# Tue, 02 Jun 2026 08:19:10 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Tue, 02 Jun 2026 08:19:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:19:24 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Jun 2026 08:19:24 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 02 Jun 2026 08:19:24 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Tue, 02 Jun 2026 08:19:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jun 2026 08:19:24 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 02 Jun 2026 08:19:24 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 02 Jun 2026 08:19:24 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 02 Jun 2026 08:19:24 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 02 Jun 2026 08:19:24 GMT
ENV MONGO_MAJOR=8.2
# Tue, 02 Jun 2026 08:19:24 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/$MONGO_PACKAGE/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/$MONGO_PACKAGE.list" # buildkit
# Tue, 02 Jun 2026 08:19:24 GMT
ENV MONGO_VERSION=8.2.9
# Tue, 02 Jun 2026 08:19:40 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Tue, 02 Jun 2026 08:19:40 GMT
VOLUME [/data/db /data/configdb]
# Tue, 02 Jun 2026 08:19:40 GMT
ENV HOME=/data/db
# Tue, 02 Jun 2026 08:19:40 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Tue, 02 Jun 2026 08:19:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jun 2026 08:19:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 08:19:40 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 02 Jun 2026 08:19:40 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d99f9ea545059709d07577fd23242abf5db122dbd49bc347165a97957704ba`  
		Last Modified: Tue, 02 Jun 2026 08:20:15 GMT  
		Size: 1.2 KB (1218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4a9b74b7e4f21f23ff43d94d99a8e6c817d799f2dc732d7527864fba624b1c`  
		Last Modified: Tue, 02 Jun 2026 08:20:15 GMT  
		Size: 1.5 MB (1510295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05428580398951537f8919271cec17854c882a2c216ecea2d9529bd984586f98`  
		Last Modified: Tue, 02 Jun 2026 08:20:15 GMT  
		Size: 933.8 KB (933812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d949d6af289994133fd438b23ffa1cb087040c841e35d939420d820d7dc2b3da`  
		Last Modified: Tue, 02 Jun 2026 08:20:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c3eec97d54ed4a3bbb3f96ca82dff6ef9c760d7f84e080240cfaabc4995d83`  
		Last Modified: Tue, 02 Jun 2026 08:20:17 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c810d0643d1e8c37844f707cd554bbae99c3fee3cc0d586c03b86be5c5d432`  
		Last Modified: Tue, 02 Jun 2026 08:20:24 GMT  
		Size: 304.0 MB (303975190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc0890f613c7dc2fca844290db7778ca7657dc593195a07362e4046c9adbfc0`  
		Last Modified: Tue, 02 Jun 2026 08:20:17 GMT  
		Size: 5.0 KB (5000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:8-noble` - unknown; unknown

```console
$ docker pull mongo@sha256:79f818c78e2424fb05cc6f850a99fa2809d9da3fe0d31595b7274cf377f7cda0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2689171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5a8cfe23453f354f5c175bc9d6d286ad0b58c58d169fe77d243e1cb87b90c82`

```dockerfile
```

-	Layers:
	-	`sha256:8d40861298688aab619447fa119277fdba42dd8c16584b07f445279b665a0b78`  
		Last Modified: Tue, 02 Jun 2026 08:20:15 GMT  
		Size: 2.7 MB (2660435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f50dddda872b0cab06027c15b6f582f2c535c2fd6647c5e3af7e5f6f795bb4c`  
		Last Modified: Tue, 02 Jun 2026 08:20:15 GMT  
		Size: 28.7 KB (28736 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:8-noble` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:5a85a3fad74929bad4da99a1680c66c111fbd45ebedb702a982d9ed9574e8da9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.8 MB (320835589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f09db935fe3ab8b9bd4b72a47872bf7ef2d0cd18914402ff0954f58b10671f49`
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
# Tue, 02 Jun 2026 08:19:39 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Tue, 02 Jun 2026 08:19:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:19:57 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Jun 2026 08:19:57 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 02 Jun 2026 08:19:57 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Tue, 02 Jun 2026 08:19:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jun 2026 08:19:57 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 02 Jun 2026 08:19:57 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 02 Jun 2026 08:19:57 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 02 Jun 2026 08:19:57 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 02 Jun 2026 08:19:57 GMT
ENV MONGO_MAJOR=8.2
# Tue, 02 Jun 2026 08:19:57 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/$MONGO_PACKAGE/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/$MONGO_PACKAGE.list" # buildkit
# Tue, 02 Jun 2026 08:19:57 GMT
ENV MONGO_VERSION=8.2.9
# Tue, 02 Jun 2026 08:20:17 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Tue, 02 Jun 2026 08:20:17 GMT
VOLUME [/data/db /data/configdb]
# Tue, 02 Jun 2026 08:20:17 GMT
ENV HOME=/data/db
# Tue, 02 Jun 2026 08:20:17 GMT
ENV GLIBC_TUNABLES=glibc.pthread.rseq=0
# Tue, 02 Jun 2026 08:20:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jun 2026 08:20:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jun 2026 08:20:17 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 02 Jun 2026 08:20:17 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6484ce70ec362d3cee863c26eaf7b90cc3ac30343022e2f3b75b710a46c0179a`  
		Last Modified: Tue, 02 Jun 2026 08:20:51 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef1c7c9baec3e2d84f96152822ad70eb29d2c125546383870858186eb807ac0`  
		Last Modified: Tue, 02 Jun 2026 08:20:51 GMT  
		Size: 1.5 MB (1495798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302ec5ea1e503d88cfe31022fdc3dee1af52451e044ec082fdce33a234f7913c`  
		Last Modified: Tue, 02 Jun 2026 08:20:51 GMT  
		Size: 886.1 KB (886105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:262c0ee705138b0d9a084ec8aed9fc507d8385501abedd9c5b9fd93f1b093fdf`  
		Last Modified: Tue, 02 Jun 2026 08:20:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba4c6e97e0c4c28df23405b0d9dbfbb5c4fa5dbfc14498ff046ea68ac4fe68fd`  
		Last Modified: Tue, 02 Jun 2026 08:20:53 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89457bafc1eecdf4af681ce5d34457d3264e32753d633f8136014825f0efae92`  
		Last Modified: Tue, 02 Jun 2026 08:21:00 GMT  
		Size: 289.6 MB (289570684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e5170ee26dc50df4be8ccabc424e1fff647c40fb736838ba8924ff787595d4`  
		Last Modified: Tue, 02 Jun 2026 08:20:53 GMT  
		Size: 5.0 KB (5002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:8-noble` - unknown; unknown

```console
$ docker pull mongo@sha256:6e815729a926e662c6d0d4b3fa3c6affef4692ab595fd47c15107dfcbf12ac8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2690534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92cfce67db22f7f7eb3c9eeb0a164fdc31a9cada4a943f6fd6905214449909d3`

```dockerfile
```

-	Layers:
	-	`sha256:a863bdb3e611d52144da071188970f4677726b28ad6fe241bb590b2d98e3c720`  
		Last Modified: Tue, 02 Jun 2026 08:20:51 GMT  
		Size: 2.7 MB (2661571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39221f895cfb8a565ecaf5b131666f91c983fba69d0c0b769d1634955a774569`  
		Last Modified: Tue, 02 Jun 2026 08:20:51 GMT  
		Size: 29.0 KB (28963 bytes)  
		MIME: application/vnd.in-toto+json
