## `mongo:7-jammy`

```console
$ docker pull mongo@sha256:88785f6f665ab817955ec1cb4f05b7b9c76947023086401413085cd1fff091a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:7-jammy` - linux; amd64

```console
$ docker pull mongo@sha256:d3d7c7fbbbb18f61baac3f8d13f0834c28a0e000cae444691def321d568abe47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.6 MB (283552228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d626061330ce6cccc8ffdf61bdfcd3f929080070a90e16a0f3cc460393c7d7d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:33:32 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Thu, 15 Jan 2026 22:33:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:33:52 GMT
ENV GOSU_VERSION=1.19
# Thu, 15 Jan 2026 22:33:52 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 15 Jan 2026 22:33:52 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Thu, 15 Jan 2026 22:33:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 15 Jan 2026 22:33:52 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:33:52 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 15 Jan 2026 22:33:52 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 15 Jan 2026 22:33:52 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 15 Jan 2026 22:33:52 GMT
ENV MONGO_MAJOR=7.0
# Thu, 15 Jan 2026 22:33:52 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Thu, 15 Jan 2026 22:33:52 GMT
ENV MONGO_VERSION=7.0.28
# Thu, 15 Jan 2026 22:34:11 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Thu, 15 Jan 2026 22:34:11 GMT
VOLUME [/data/db /data/configdb]
# Thu, 15 Jan 2026 22:34:11 GMT
ENV HOME=/data/db
# Thu, 15 Jan 2026 22:34:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 22:34:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:34:12 GMT
EXPOSE map[27017/tcp:{}]
# Thu, 15 Jan 2026 22:34:12 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc530503d63acdf0ebeb37699d232920962c96ae03820fc5a668c46a010f913f`  
		Last Modified: Thu, 15 Jan 2026 22:34:55 GMT  
		Size: 1.8 KB (1780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9863ceddd80002325c13476a79ac26473cd21f1d952e9bf72cb0480d765ba5f`  
		Last Modified: Thu, 15 Jan 2026 22:34:57 GMT  
		Size: 1.5 MB (1513849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053a896a950f60a295f98d5d291ac94b011e01d7a6ac819130f96303334be9dd`  
		Last Modified: Thu, 15 Jan 2026 22:34:56 GMT  
		Size: 898.1 KB (898144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b189090aa38fec755ea1a694b114f7b167fc4e330a7666b8e93b5ed4c57ca42d`  
		Last Modified: Thu, 15 Jan 2026 22:34:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49725ac362ad7d58ec7512376703259a9f58bf270f4abb666f8665ba7ae60f6f`  
		Last Modified: Thu, 15 Jan 2026 22:34:42 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ab68bcb301f43c41dff9f35fc1d315207bec711f61387487098aea65550a97`  
		Last Modified: Thu, 15 Jan 2026 22:34:47 GMT  
		Size: 251.6 MB (251596406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7407b56680a93c1b88f3d65b71499c386e4add38ba075254e78af9c46ba78e23`  
		Last Modified: Thu, 15 Jan 2026 22:34:58 GMT  
		Size: 5.0 KB (5002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:7-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:c900af4d7f5bcab7ffa1eaea126f023000e1fd79b02655898dba0367d95645e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3254460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7324a63bac8e8326d01b1244470cd5909581a11612fa26d5f1d30148413e93bd`

```dockerfile
```

-	Layers:
	-	`sha256:385147b9b3df4e42322fff9f9cffbad737d5498d845a9f64293778b2153e1981`  
		Last Modified: Thu, 15 Jan 2026 22:34:41 GMT  
		Size: 3.2 MB (3226518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0eabfbf68c0528177d78ed23b95749061041140692c0cc4d39a2590df3ecac3`  
		Last Modified: Thu, 15 Jan 2026 22:34:41 GMT  
		Size: 27.9 KB (27942 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:7-jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:9c4b531caba8a9764ce4d1bcb24a9d38517780c6617533a80c2d2cdd7a77a399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.4 MB (270352997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c028a038ba851eea2419e6224684652adb21f0f9edc34b7f128d0ae1d2c987`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:36:15 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Thu, 15 Jan 2026 22:36:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:36:40 GMT
ENV GOSU_VERSION=1.19
# Thu, 15 Jan 2026 22:36:40 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 15 Jan 2026 22:36:40 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Thu, 15 Jan 2026 22:36:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-7.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'E58830201F7DD82CD808AA84160D26BB1785BA38' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 15 Jan 2026 22:36:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:36:40 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 15 Jan 2026 22:36:40 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 15 Jan 2026 22:36:40 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 15 Jan 2026 22:36:40 GMT
ENV MONGO_MAJOR=7.0
# Thu, 15 Jan 2026 22:36:40 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Thu, 15 Jan 2026 22:36:40 GMT
ENV MONGO_VERSION=7.0.28
# Thu, 15 Jan 2026 22:37:00 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Thu, 15 Jan 2026 22:37:00 GMT
VOLUME [/data/db /data/configdb]
# Thu, 15 Jan 2026 22:37:00 GMT
ENV HOME=/data/db
# Thu, 15 Jan 2026 22:37:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 22:37:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jan 2026 22:37:00 GMT
EXPOSE map[27017/tcp:{}]
# Thu, 15 Jan 2026 22:37:00 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 11:16:52 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6342326cfb480d95f8229963424e669e8bc9511c927946f90c3414368adf87`  
		Last Modified: Thu, 15 Jan 2026 22:37:40 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c011418e0ec5641135cd20feba283f79ac31feabe3366c3d9cbee489dd3d39`  
		Last Modified: Thu, 15 Jan 2026 22:37:41 GMT  
		Size: 1.5 MB (1482371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a02f680d534a9c527057391f90df1eeeda494cc4a8ae65220daf05bb2592d0f`  
		Last Modified: Thu, 15 Jan 2026 22:37:29 GMT  
		Size: 850.5 KB (850458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95b4d4c57a367b9c90d30a71189e22e14b2b34afc23f7fc0aac6e1c376dfa29`  
		Last Modified: Thu, 15 Jan 2026 22:37:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6dbcc125dc3fbaa5084fd6bf4b37e4bc8418d50c811df4c40040507083b1b48`  
		Last Modified: Thu, 15 Jan 2026 22:37:40 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f22640b02e8ed8dc8853dab1e43c8f0567d4dd833547b1eb02925afef33afeca`  
		Last Modified: Thu, 15 Jan 2026 22:37:58 GMT  
		Size: 240.6 MB (240629504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e87ddfd65828f812b44b9e1ed882d8d2d125110d39f03113b4c4afbcca0377`  
		Last Modified: Thu, 15 Jan 2026 22:37:40 GMT  
		Size: 5.0 KB (5005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:7-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:79d6a31a420ab5c41d4f6e90695d68ba78f86a38edb7032a4a6aafa0f0b75d42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3254983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f12b7218750c30ed5bfbc87c99aba2d23b8438ddfb24a89f2c856829fe01e0f`

```dockerfile
```

-	Layers:
	-	`sha256:56a2e7643804772e88ab8883a9474b4305d8eab3fa3e8b7b28f7d9deb2466063`  
		Last Modified: Fri, 16 Jan 2026 00:29:48 GMT  
		Size: 3.2 MB (3226837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecc81bf188360fdcbd92434c811c05e6aa4211361c3b6c59ff3b2a075217110c`  
		Last Modified: Thu, 15 Jan 2026 22:37:29 GMT  
		Size: 28.1 KB (28146 bytes)  
		MIME: application/vnd.in-toto+json
