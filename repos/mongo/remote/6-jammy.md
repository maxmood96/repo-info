## `mongo:6-jammy`

```console
$ docker pull mongo@sha256:d17a54d779084049638a5c82ae7ab1d4663c03b6c81b4c6a062a15846046f438
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:6-jammy` - linux; amd64

```console
$ docker pull mongo@sha256:f3dedbe2ebd1d6a88bf316cdd58c19737c59050ce720007cac868c5b2b4cb94e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (245963050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97eb2e5e80a77e90277e6a2bc96e0d4c37b04941151f81f1707296c465720d30`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 27 Feb 2024 18:52:57 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:52:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:52:58 GMT
ADD file:21c2e8d95909bec6f4acdaf4aed55b44ee13603681f93b152e423e3e6a4a207b in / 
# Tue, 27 Feb 2024 18:52:59 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 23:30:03 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Thu, 29 Feb 2024 23:30:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 23:30:03 GMT
ENV GOSU_VERSION=1.17
# Thu, 29 Feb 2024 23:30:03 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 29 Feb 2024 23:30:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-6.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '39BD841E4BE5FB195A65400E6A26B1AE64C3C388' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 29 Feb 2024 23:30:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Feb 2024 23:30:03 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 29 Feb 2024 23:30:03 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 29 Feb 2024 23:30:03 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 29 Feb 2024 23:30:03 GMT
ENV MONGO_MAJOR=6.0
# Thu, 29 Feb 2024 23:30:03 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Thu, 29 Feb 2024 23:30:03 GMT
ENV MONGO_VERSION=6.0.14
# Thu, 29 Feb 2024 23:30:03 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Thu, 29 Feb 2024 23:30:03 GMT
VOLUME [/data/db /data/configdb]
# Thu, 29 Feb 2024 23:30:03 GMT
ENV HOME=/data/db
# Thu, 29 Feb 2024 23:30:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 Feb 2024 23:30:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Feb 2024 23:30:03 GMT
EXPOSE map[27017/tcp:{}]
# Thu, 29 Feb 2024 23:30:03 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:bccd10f490ab0f3fba61b193d1b80af91b17ca9bdca9768a16ed05ce16552fcb`  
		Last Modified: Tue, 27 Feb 2024 19:00:05 GMT  
		Size: 29.5 MB (29538961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e2e7362ed26224892d570c60f07c795676f809097055683a74cf1e70e4629b`  
		Last Modified: Wed, 06 Mar 2024 02:56:42 GMT  
		Size: 1.8 KB (1773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a146171a4972808593036b8a5d2c48b7a971cb461eb0599adfd633fbb15cce46`  
		Last Modified: Wed, 06 Mar 2024 02:56:42 GMT  
		Size: 1.5 MB (1500325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871a3fb69ddd128a5b9c910c9c7d5803df2edeba9a390953e839f5baade8bd17`  
		Last Modified: Wed, 06 Mar 2024 02:56:42 GMT  
		Size: 1.1 MB (1094196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52217215350e963cbf1d7a2cde71fcd10b735515a1d470b2cc376eccd9935601`  
		Last Modified: Wed, 06 Mar 2024 02:56:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba4f4058dcadcc780a86d9df6a05b45b559de8b087ff864ed4b366cbc48230d1`  
		Last Modified: Wed, 06 Mar 2024 02:56:42 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94183542a5f17b915ec5ce8f9fce49553907ae98bb8e41334dac04327631805`  
		Last Modified: Wed, 06 Mar 2024 02:56:46 GMT  
		Size: 213.8 MB (213822417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d8743e4c94cb7a5cfe2eab49bff528944e2eb9407e808062cbc62475c8ac0b`  
		Last Modified: Wed, 06 Mar 2024 02:56:43 GMT  
		Size: 5.0 KB (4999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:6-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:cd86ff3c99956b06f5e5a7da55a07858ddd7a2239250f2b8a603b0b4d677fa1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3026446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26110f157199308b4f4105ace853a2fff83e3e3b623961b9aefb1cbb125a511c`

```dockerfile
```

-	Layers:
	-	`sha256:3b9f3ece1666cc5553112fb6c37e1d82902124e756cbf010fc524802afeeb107`  
		Last Modified: Wed, 06 Mar 2024 02:56:42 GMT  
		Size: 3.0 MB (2999293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fe3289301dce362530e8faca02ea908ded6511a1905f936584cbfed68e7414d`  
		Last Modified: Wed, 06 Mar 2024 02:56:42 GMT  
		Size: 27.2 KB (27153 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:6-jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:dd0ce03345a9b19534b80bb5b31745206603f71970e36ae3db9c805a3783f56a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.8 MB (238827038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02f97eb80d32ea85744da4fcac4faa72693f6159da08de7243f921b13a2b6119`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Tue, 27 Feb 2024 18:53:22 GMT
ARG RELEASE
# Tue, 27 Feb 2024 18:53:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Feb 2024 18:53:22 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 27 Feb 2024 18:53:25 GMT
ADD file:07cdbabf782942af04487c9da03de50a611a51e69d8bac1f593acb73a3ba3a46 in / 
# Tue, 27 Feb 2024 18:53:25 GMT
CMD ["/bin/bash"]
# Thu, 29 Feb 2024 23:30:03 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Thu, 29 Feb 2024 23:30:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Feb 2024 23:30:03 GMT
ENV GOSU_VERSION=1.17
# Thu, 29 Feb 2024 23:30:03 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 29 Feb 2024 23:30:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-6.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '39BD841E4BE5FB195A65400E6A26B1AE64C3C388' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 29 Feb 2024 23:30:03 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Feb 2024 23:30:03 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 29 Feb 2024 23:30:03 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 29 Feb 2024 23:30:03 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 29 Feb 2024 23:30:03 GMT
ENV MONGO_MAJOR=6.0
# Thu, 29 Feb 2024 23:30:03 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Thu, 29 Feb 2024 23:30:03 GMT
ENV MONGO_VERSION=6.0.14
# Thu, 29 Feb 2024 23:30:03 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Thu, 29 Feb 2024 23:30:03 GMT
VOLUME [/data/db /data/configdb]
# Thu, 29 Feb 2024 23:30:03 GMT
ENV HOME=/data/db
# Thu, 29 Feb 2024 23:30:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 29 Feb 2024 23:30:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 29 Feb 2024 23:30:03 GMT
EXPOSE map[27017/tcp:{}]
# Thu, 29 Feb 2024 23:30:03 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:f4bb4e8dca02be491b4f72d2ef2127a64ce49c48d0d9c0a0fcaffa625067679d`  
		Last Modified: Tue, 27 Feb 2024 19:00:12 GMT  
		Size: 27.4 MB (27358724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4bd89af55c0e4a026246b31bb0ead738f1dec86ed74f6cd61588112089ffdf`  
		Last Modified: Fri, 15 Mar 2024 19:53:26 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5eac8f7306550dc8afd92ed23b6cf11dd6ce96e577a15565b3b5af29aa2503f`  
		Last Modified: Fri, 15 Mar 2024 19:53:26 GMT  
		Size: 1.5 MB (1465421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e397ca005a6f111a24e03c392871ea41733419c985dffd7f69d293373569f9`  
		Last Modified: Fri, 15 Mar 2024 20:00:56 GMT  
		Size: 1.0 MB (1026957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a115e1752e9ce88f6e778a86c62fa35394a4d4738b1a8847999d5dbf863f24bd`  
		Last Modified: Fri, 15 Mar 2024 20:00:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4aaf32209720c4e4add95a385c7743adc3a1b2453e8bc0cd02edbbb58f07a2d`  
		Last Modified: Fri, 15 Mar 2024 20:00:56 GMT  
		Size: 263.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ab459181a1729b01f9439350f2261dada5809532b5a697037c230beabf7363`  
		Last Modified: Fri, 15 Mar 2024 20:01:02 GMT  
		Size: 209.0 MB (208968779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7aeaac799c0c0f5df4ddeb3e136f5463f180ebd4f41ae173ec8205065a865a5`  
		Last Modified: Fri, 15 Mar 2024 20:00:57 GMT  
		Size: 5.0 KB (4993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:6-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:35b014fb7fd8256e643e6ce5059e77bfea6a393f63138e62a64be532fef05943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3026553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77696f19cc3763456e27f598d74b683cf4b00f5aa08ea4f219b412d70583bc76`

```dockerfile
```

-	Layers:
	-	`sha256:2cc179e18d254857a05e217cf5398b2d36759ff700ed9775c3e9eaecefc3efc0`  
		Last Modified: Fri, 15 Mar 2024 20:00:56 GMT  
		Size: 3.0 MB (2999546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fcf1cd93752d798c04f90140b5e3789e9179afe27d415a84a25cf1d6dca294e`  
		Last Modified: Fri, 15 Mar 2024 20:00:56 GMT  
		Size: 27.0 KB (27007 bytes)  
		MIME: application/vnd.in-toto+json
