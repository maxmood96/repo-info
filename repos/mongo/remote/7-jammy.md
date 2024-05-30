## `mongo:7-jammy`

```console
$ docker pull mongo@sha256:63c7601604ae4fb5e9d2a8d2c486dc454cef815a4208e850fc08217f02ff74e8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:7-jammy` - linux; amd64

```console
$ docker pull mongo@sha256:26ba9dcdb9a225f9d7957e5c5a962af9d9ca403d0c5562e1590338bbae37cd10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.5 MB (265517019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f732130b5c39f4f56bd113026646151be7558acb36cf30b4347aeccd0249630`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:35 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:37 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Sat, 27 Apr 2024 13:18:37 GMT
CMD ["/bin/bash"]
# Thu, 23 May 2024 22:01:34 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Thu, 23 May 2024 22:01:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 23 May 2024 22:01:34 GMT
ENV GOSU_VERSION=1.17
# Thu, 23 May 2024 22:01:34 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 23 May 2024 22:01:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 23 May 2024 22:01:34 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 23 May 2024 22:01:34 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 23 May 2024 22:01:34 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 23 May 2024 22:01:34 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 23 May 2024 22:01:34 GMT
ENV MONGO_MAJOR=7.0
# Thu, 23 May 2024 22:01:34 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Thu, 23 May 2024 22:01:34 GMT
ENV MONGO_VERSION=7.0.11
# Thu, 23 May 2024 22:01:34 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Thu, 23 May 2024 22:01:34 GMT
VOLUME [/data/db /data/configdb]
# Thu, 23 May 2024 22:01:34 GMT
ENV HOME=/data/db
# Thu, 23 May 2024 22:01:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 22:01:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 22:01:34 GMT
EXPOSE map[27017/tcp:{}]
# Thu, 23 May 2024 22:01:34 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:a8b1c5f80c2d2a757adc963e3fe2dad0b4d229f83df3349fbb70e4d12dd48822`  
		Last Modified: Sat, 27 Apr 2024 14:45:30 GMT  
		Size: 29.5 MB (29533949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1f192fe0850dccc336d563146dfde7b09152317b45aae1313f54f6ad2d9a8a`  
		Last Modified: Wed, 29 May 2024 22:02:31 GMT  
		Size: 1.8 KB (1780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329c0ae4635854d289c95a4ad3c41b7dbe0cfcba90b5351607d938da96be168f`  
		Last Modified: Wed, 29 May 2024 22:02:31 GMT  
		Size: 1.5 MB (1500715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41d483e5ca38039e44082c628a83b0570d8d9edfe1be406cff1329ca26a4ba6`  
		Last Modified: Wed, 29 May 2024 22:02:31 GMT  
		Size: 1.1 MB (1094566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ce4a7bbe770e042832f483445224c24448decde12b286d4a2ee477e64274cc`  
		Last Modified: Wed, 29 May 2024 22:02:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57884d3aea6673fe871b179a44070e728ea0cfa25ad14c280edacd89f185736d`  
		Last Modified: Wed, 29 May 2024 22:02:32 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5117a1be0e20afe0967f00793e5f95b3453d72d9b2d8d9461a5e37c95965606c`  
		Last Modified: Wed, 29 May 2024 22:02:38 GMT  
		Size: 233.4 MB (233380626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a739f30e1d2f7bc2cb18440074edc3674a4dc6bff77d6bc749056aec6750f64`  
		Last Modified: Wed, 29 May 2024 22:02:33 GMT  
		Size: 5.0 KB (5000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:7-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:2248441a8f2cbdcb8b6f84b45216ae6d44bd184e1163758b93482409105e5d68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3028690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:533047f465bb0f46491a567a647b7846d6c1efbe3a60b37d510999bc9c34ddf6`

```dockerfile
```

-	Layers:
	-	`sha256:1270803922da793593179d45a03d8e652167ad72ba1fc3420a65254ed44f836d`  
		Last Modified: Wed, 29 May 2024 22:02:31 GMT  
		Size: 3.0 MB (3001103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a460778238823ee66d32c6a07dec27213ed41baf6ba802adb4fe7f340d7b23ec`  
		Last Modified: Wed, 29 May 2024 22:02:31 GMT  
		Size: 27.6 KB (27587 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:7-jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:8ff69162926750978451697274dc3c93eac609894b9cff7ed977e76e6bcabcbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.5 MB (256534333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c06ba83b1d2680952de1a543a44eb21131eab72c9a0f86e956d3d251cc9ba63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Sat, 27 Apr 2024 00:09:59 GMT
ARG RELEASE
# Sat, 27 Apr 2024 00:09:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 00:09:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 00:09:59 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 00:09:59 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 00:09:59 GMT
CMD ["/bin/bash"]
# Sat, 27 Apr 2024 00:09:59 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Sat, 27 Apr 2024 00:09:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 27 Apr 2024 00:09:59 GMT
ENV GOSU_VERSION=1.17
# Sat, 27 Apr 2024 00:09:59 GMT
ENV JSYAML_VERSION=3.13.1
# Sat, 27 Apr 2024 00:09:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sat, 27 Apr 2024 00:09:59 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sat, 27 Apr 2024 00:09:59 GMT
ARG MONGO_PACKAGE=mongodb-org
# Sat, 27 Apr 2024 00:09:59 GMT
ARG MONGO_REPO=repo.mongodb.org
# Sat, 27 Apr 2024 00:09:59 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Sat, 27 Apr 2024 00:09:59 GMT
ENV MONGO_MAJOR=7.0
# Sat, 27 Apr 2024 00:09:59 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Sat, 27 Apr 2024 00:09:59 GMT
ENV MONGO_VERSION=7.0.9
# Sat, 27 Apr 2024 00:09:59 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Sat, 27 Apr 2024 00:09:59 GMT
VOLUME [/data/db /data/configdb]
# Sat, 27 Apr 2024 00:09:59 GMT
ENV HOME=/data/db
# Sat, 27 Apr 2024 00:09:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 27 Apr 2024 00:09:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Apr 2024 00:09:59 GMT
EXPOSE map[27017/tcp:{}]
# Sat, 27 Apr 2024 00:09:59 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:d5a2ad729c09fbfdb259ae764f92188efc67a615ffde9bb34a46298d1edf3cd6`  
		Last Modified: Sat, 27 Apr 2024 14:45:36 GMT  
		Size: 27.4 MB (27360530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8997f1f9f9006d728589447abdb1409fa9e5a099131cd4e1e64cd6a6aebc75a4`  
		Last Modified: Mon, 06 May 2024 16:53:50 GMT  
		Size: 1.8 KB (1780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df3da78ba55adacc12f99125c8d02a8619ea246b5d158139419be8088a877bb`  
		Last Modified: Mon, 06 May 2024 16:53:50 GMT  
		Size: 1.5 MB (1466053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae663e18ef47982e6b53f9b575e1993c050751aec9bdb1efdaf18322d4316a9`  
		Last Modified: Mon, 06 May 2024 16:53:50 GMT  
		Size: 1.0 MB (1027591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f560100ad0dc25e76b51215a6b8410d2312fdfa4c0c9b4a85d89a11c59963da`  
		Last Modified: Mon, 06 May 2024 16:53:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84723abe3887e1bffb5b6b441daae3f4ed30cdebc4975696ff713fa9b6cf34b6`  
		Last Modified: Mon, 06 May 2024 16:53:51 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae2c767f2a3daaceda5366b368db9ac73a420d2e4d372371d37f830ce2a4b3f`  
		Last Modified: Mon, 06 May 2024 16:53:56 GMT  
		Size: 226.7 MB (226673006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e6b00d3f2175c4dc556796f1dd47dd441479d7e3b20e579299a5d277bbdf0b`  
		Last Modified: Mon, 06 May 2024 16:53:51 GMT  
		Size: 5.0 KB (4991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:7-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:c6861a6510dc88ba4663e64f330467346339fd0be14ec98634dba09cd806df94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3028938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3e2a7e7eeda0778c9cca6aceecc9135b929114e6ea1073c7a8ae579346af798`

```dockerfile
```

-	Layers:
	-	`sha256:a155ef00de76ad8d24d5eaffa82fd516c0b45b309aee74b30323ec3c87d06a0d`  
		Last Modified: Mon, 06 May 2024 16:53:50 GMT  
		Size: 3.0 MB (3001342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44175a6e7d7411c6049bf9731512e52d77fc3254ddc46efa7fcbfee4d7fcdf05`  
		Last Modified: Mon, 06 May 2024 16:53:50 GMT  
		Size: 27.6 KB (27596 bytes)  
		MIME: application/vnd.in-toto+json
