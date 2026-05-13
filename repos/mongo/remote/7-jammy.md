## `mongo:7-jammy`

```console
$ docker pull mongo@sha256:9d68114c8c7877bdae70a329d4b8846a96b045d5d9146616c82779a249569b36
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:7-jammy` - linux; amd64

```console
$ docker pull mongo@sha256:62a4bb399b36c7eb8477d855ca59d0424957dbffb446644fbec16862fce04243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.2 MB (293211798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2937b1eeb5264b3cd6ae8af2ccefeeccd8861887103b13e2a0d86b096501d2ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 13 May 2026 18:12:19 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Wed, 13 May 2026 18:12:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 18:12:34 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:12:34 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 13 May 2026 18:12:34 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Wed, 13 May 2026 18:12:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:12:34 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 13 May 2026 18:12:34 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 13 May 2026 18:12:34 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 13 May 2026 18:12:34 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 13 May 2026 18:12:34 GMT
ENV MONGO_MAJOR=7.0
# Wed, 13 May 2026 18:12:35 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/$MONGO_PACKAGE/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/$MONGO_PACKAGE.list" # buildkit
# Wed, 13 May 2026 18:12:35 GMT
ENV MONGO_VERSION=7.0.34
# Wed, 13 May 2026 18:12:55 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Wed, 13 May 2026 18:12:55 GMT
VOLUME [/data/db /data/configdb]
# Wed, 13 May 2026 18:12:55 GMT
ENV HOME=/data/db
# Wed, 13 May 2026 18:12:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:12:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:12:55 GMT
EXPOSE map[27017/tcp:{}]
# Wed, 13 May 2026 18:12:55 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dc8ec2173950d5bb4bfc1f8da08d991e4853652a8df964f0c6690c7dfce9301`  
		Last Modified: Wed, 13 May 2026 18:13:30 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1a009e3865cdd50b273f68aa62aafdb029cbff1ed2023150ac575b6519890f`  
		Last Modified: Wed, 13 May 2026 18:13:30 GMT  
		Size: 1.5 MB (1514464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c310f449ffa680f96ea5c2bc9f070e91183c3bc21d50c7241534a68ebc97e117`  
		Last Modified: Wed, 13 May 2026 18:13:30 GMT  
		Size: 898.1 KB (898098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179dd76f067a986405d6a0b702f4d7b4150da418f4286cbdaabfb9239458033c`  
		Last Modified: Wed, 13 May 2026 18:13:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b56365ab4b3627387217fe10fa81b57a56e61083231774d567627709e0e46bf1`  
		Last Modified: Wed, 13 May 2026 18:13:31 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae92f27baaaa98065fa7b3da4ea800ad00729b19399f16a581937ea681c32779`  
		Last Modified: Wed, 13 May 2026 18:13:36 GMT  
		Size: 261.1 MB (261055565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f5407448ec087f4094db03d0292d4565a422e1bc54910ec5d9b701d8b4bdc2`  
		Last Modified: Wed, 13 May 2026 18:13:31 GMT  
		Size: 5.0 KB (5003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:7-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:187f4f96ae932917677ef4acfc36a3058e5734bf7b89f190581510c171b358cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3245887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57230b5bb4c2da3ad2da98c051f3083b6d397e0b5382eb04b8f1f9c72976f63`

```dockerfile
```

-	Layers:
	-	`sha256:69581c3cf7d08b64a5a993b652340c1fc62e122c7760cff53d901b4bb847fb1f`  
		Last Modified: Wed, 13 May 2026 18:13:30 GMT  
		Size: 3.2 MB (3218000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23202f1cee89f1f056d78bf3120a1fa8a54b585651656bb444f9561d3a8bbe7c`  
		Last Modified: Wed, 13 May 2026 18:13:30 GMT  
		Size: 27.9 KB (27887 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:7-jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:8c2c45081a548a9cd241fa4254d105310011a6af87a215ae1e7817660129ad05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.3 MB (279292672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:875c0e3e96310b771fc20c2e83934cd9b8dcac62fd26b9f26646911282d231d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 13 May 2026 18:03:09 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Wed, 13 May 2026 18:03:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 18:03:30 GMT
ENV GOSU_VERSION=1.19
# Wed, 13 May 2026 18:03:30 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 13 May 2026 18:03:30 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Wed, 13 May 2026 18:03:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 13 May 2026 18:03:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 13 May 2026 18:03:30 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 13 May 2026 18:03:30 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 13 May 2026 18:03:30 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 13 May 2026 18:03:30 GMT
ENV MONGO_MAJOR=7.0
# Wed, 13 May 2026 18:03:30 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/$MONGO_PACKAGE/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/$MONGO_PACKAGE.list" # buildkit
# Wed, 13 May 2026 18:03:30 GMT
ENV MONGO_VERSION=7.0.34
# Wed, 13 May 2026 18:03:52 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Wed, 13 May 2026 18:03:52 GMT
VOLUME [/data/db /data/configdb]
# Wed, 13 May 2026 18:03:52 GMT
ENV HOME=/data/db
# Wed, 13 May 2026 18:03:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 18:03:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 18:03:52 GMT
EXPOSE map[27017/tcp:{}]
# Wed, 13 May 2026 18:03:52 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2df88669eec97626acc8197a5a155facff181d8bd114dc4bb2d4a617a8ae65`  
		Last Modified: Wed, 13 May 2026 18:04:23 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8605f19742e1f3752a11f04d925ec6bd6475e9290630808153772cd4f693421b`  
		Last Modified: Wed, 13 May 2026 18:04:23 GMT  
		Size: 1.5 MB (1485332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d4d8f066f038d01e7bd5dd0f40a8f753ee4beaeb21bb59c5b0d3dd30d15ee8`  
		Last Modified: Wed, 13 May 2026 18:04:23 GMT  
		Size: 850.6 KB (850559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7a48d5331b7d2c67a1570767592cc708d9f1bcd6c8f0adc8ce78a57d19a2e1`  
		Last Modified: Wed, 13 May 2026 18:04:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf207fa55a59a9d01d1bb102024172650bf2cd2f1f123b90a67f6c252e5739c0`  
		Last Modified: Wed, 13 May 2026 18:04:24 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f12bf68b404556ea743f2f6952c06063fd265907c7ee3a7deda0805cdcabd9`  
		Last Modified: Wed, 13 May 2026 18:04:32 GMT  
		Size: 249.3 MB (249343067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01b17404453c4314ff599eb3e7ef31ba029984cef5d316e623e8d34a0bfebf6`  
		Last Modified: Wed, 13 May 2026 18:04:25 GMT  
		Size: 5.0 KB (5004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:7-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:a378b1ea207efa0d8a2131e1b36af4dce263c8bcb496c3b1fc3070c8e269af2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3246409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d0a9312f08cf2622fbe2047027451985e1d06a8e39425583c4c5da3d4bd7bea`

```dockerfile
```

-	Layers:
	-	`sha256:9494f04d125b5e87b122f866fe6a88331e76670c7315fa6446855511e54d86bf`  
		Last Modified: Wed, 13 May 2026 18:04:23 GMT  
		Size: 3.2 MB (3218319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41c4c9b6d7707612b61ca728310f289de1f6de65621f165f158ce9ee27f05501`  
		Last Modified: Wed, 13 May 2026 18:04:23 GMT  
		Size: 28.1 KB (28090 bytes)  
		MIME: application/vnd.in-toto+json
