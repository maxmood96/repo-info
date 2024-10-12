## `mongo:8-noble`

```console
$ docker pull mongo@sha256:ff5997833c8c29b69ebe571e4b69989f57b320f3852a0b2ce0b7a17845f05157
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:8-noble` - linux; amd64

```console
$ docker pull mongo@sha256:0c23e8ede37de87b97c628d65c9e042140b3ef8e080d7367e60cf041f135e4c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.4 MB (274430281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:543980b7d80b4fc7ae92f74883e37c4281fbc62d3993095d0748ef7cc1cd378c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 09 Oct 2024 22:01:30 GMT
ARG RELEASE
# Wed, 09 Oct 2024 22:01:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 22:01:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 22:01:30 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 09 Oct 2024 22:01:30 GMT
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
# Wed, 09 Oct 2024 22:01:30 GMT
CMD ["/bin/bash"]
# Wed, 09 Oct 2024 22:01:30 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Wed, 09 Oct 2024 22:01:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Oct 2024 22:01:30 GMT
ENV GOSU_VERSION=1.17
# Wed, 09 Oct 2024 22:01:30 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 09 Oct 2024 22:01:30 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Wed, 09 Oct 2024 22:01:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 09 Oct 2024 22:01:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 09 Oct 2024 22:01:30 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 09 Oct 2024 22:01:30 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 09 Oct 2024 22:01:30 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 09 Oct 2024 22:01:30 GMT
ENV MONGO_MAJOR=8.0
# Wed, 09 Oct 2024 22:01:30 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Wed, 09 Oct 2024 22:01:30 GMT
ENV MONGO_VERSION=8.0.1
# Wed, 09 Oct 2024 22:01:30 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Wed, 09 Oct 2024 22:01:30 GMT
VOLUME [/data/db /data/configdb]
# Wed, 09 Oct 2024 22:01:30 GMT
ENV HOME=/data/db
# Wed, 09 Oct 2024 22:01:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Oct 2024 22:01:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Oct 2024 22:01:30 GMT
EXPOSE map[27017/tcp:{}]
# Wed, 09 Oct 2024 22:01:30 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:d1fbec07a2e50e73803e0c9ea0fc8f9fb48ad1215583bb1bbb8852660f52abeb`  
		Last Modified: Thu, 10 Oct 2024 08:59:45 GMT  
		Size: 29.8 MB (29750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72522092030e51ccbcac24474e3401f3ca0842e2ded4a92d650c414152bae17`  
		Last Modified: Sat, 12 Oct 2024 00:01:11 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0191e8f9f6a572b735680f864474fa7a57e59b4f59da418cc0de26fb6e67e55`  
		Last Modified: Sat, 12 Oct 2024 00:01:11 GMT  
		Size: 1.8 MB (1820121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d0a6a297c24e784cbdd4c2a04a4d8a4eb469ff5760c1ed28820e3069fc95fe`  
		Last Modified: Sat, 12 Oct 2024 00:01:11 GMT  
		Size: 1.1 MB (1129760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68eb28142e2ffae2c1ccf11f6e539b443d2f262ae08c2c513f123a277234f03b`  
		Last Modified: Sat, 12 Oct 2024 00:01:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48bd3f436015a92c9315a8c758947592b52fb84efb504e4a3a8553409a77464a`  
		Last Modified: Sat, 12 Oct 2024 00:01:11 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f1d8ba746b92ab6d09fc39d675bd293cdb5c95f2d2dfd80392a0e91b3c4c073`  
		Last Modified: Sat, 12 Oct 2024 00:01:15 GMT  
		Size: 241.7 MB (241723355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72d84281986bd2cbf978b6ae4888cc4c4a12b9b0ea24303678cabd1f18d291b`  
		Last Modified: Sat, 12 Oct 2024 00:01:11 GMT  
		Size: 5.0 KB (4998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:8-noble` - unknown; unknown

```console
$ docker pull mongo@sha256:d8a8ef0561462b68bf1edf54159c9920e01e280a7ac746ee2da5a69528c4e7bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2509100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3809fe6d15c4547b0bdbd8972a96fb8fdb488fec2c35fddcb39b3fec90f3de`

```dockerfile
```

-	Layers:
	-	`sha256:47766aa07e17e52845675d9b8d8355e107a572fda10509dc6a4625a8d4b83325`  
		Last Modified: Sat, 12 Oct 2024 00:01:11 GMT  
		Size: 2.5 MB (2480744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba556acbb551b9ae43dfe1ccb47904309c97ecd41196486762a8c839a10b47e7`  
		Last Modified: Sat, 12 Oct 2024 00:01:11 GMT  
		Size: 28.4 KB (28356 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:8-noble` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:80f8ddecb066e57ff82eaa071c047b717e9d18593de9e164809523eaf20963ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.7 MB (263689500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c29529edd9a983d3c26252ac9d1b1384273c136d86d69da651405cf6478188`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 09 Oct 2024 22:01:30 GMT
ARG RELEASE
# Wed, 09 Oct 2024 22:01:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 09 Oct 2024 22:01:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 09 Oct 2024 22:01:30 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 09 Oct 2024 22:01:30 GMT
ADD file:b618f3f3cddb65c88794a06b33f6df2350e72e9bc020bcaf987a41fcbeea7557 in / 
# Wed, 09 Oct 2024 22:01:30 GMT
CMD ["/bin/bash"]
# Wed, 09 Oct 2024 22:01:30 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Wed, 09 Oct 2024 22:01:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Oct 2024 22:01:30 GMT
ENV GOSU_VERSION=1.17
# Wed, 09 Oct 2024 22:01:30 GMT
ENV JSYAML_VERSION=3.13.1
# Wed, 09 Oct 2024 22:01:30 GMT
ENV JSYAML_CHECKSUM=662e32319bdd378e91f67578e56a34954b0a2e33aca11d70ab9f4826af24b941
# Wed, 09 Oct 2024 22:01:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.tgz https://registry.npmjs.org/js-yaml/-/js-yaml-${JSYAML_VERSION}.tgz; 	echo "$JSYAML_CHECKSUM */opt/js-yaml/js-yaml.tgz" | sha256sum -c -; 	tar -xz --strip-components=1 -f /opt/js-yaml/js-yaml.tgz -C /opt/js-yaml package/dist/js-yaml.js package/package.json; 	rm /opt/js-yaml/js-yaml.tgz; 	ln -s /opt/js-yaml/dist/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-8.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '4B0752C1BCA238C0B4EE14DC41DE058A4E7DCA05' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 09 Oct 2024 22:01:30 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 09 Oct 2024 22:01:30 GMT
ARG MONGO_PACKAGE=mongodb-org
# Wed, 09 Oct 2024 22:01:30 GMT
ARG MONGO_REPO=repo.mongodb.org
# Wed, 09 Oct 2024 22:01:30 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Wed, 09 Oct 2024 22:01:30 GMT
ENV MONGO_MAJOR=8.0
# Wed, 09 Oct 2024 22:01:30 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu noble/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Wed, 09 Oct 2024 22:01:30 GMT
ENV MONGO_VERSION=8.0.1
# Wed, 09 Oct 2024 22:01:30 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Wed, 09 Oct 2024 22:01:30 GMT
VOLUME [/data/db /data/configdb]
# Wed, 09 Oct 2024 22:01:30 GMT
ENV HOME=/data/db
# Wed, 09 Oct 2024 22:01:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 09 Oct 2024 22:01:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Oct 2024 22:01:30 GMT
EXPOSE map[27017/tcp:{}]
# Wed, 09 Oct 2024 22:01:30 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:0741829382faee1dada646b49acf3f4349f0c757e16139b7bb1874c6339d996e`  
		Last Modified: Thu, 10 Oct 2024 08:59:51 GMT  
		Size: 28.9 MB (28885616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc141ec2689bead7bcea68bb94bff9809d06a85c0847afffc21eb0b0f19075c`  
		Last Modified: Sat, 12 Oct 2024 01:53:58 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da623327110a4be8b745e02bd2121eae311bb5f8482366e5b3b1312fb4e9813`  
		Last Modified: Sat, 12 Oct 2024 01:53:58 GMT  
		Size: 1.8 MB (1817444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a914b33c5b17a1cf1b030109b90d978260fd9eb7f53c320872d333382da026`  
		Last Modified: Sat, 12 Oct 2024 01:53:58 GMT  
		Size: 1.1 MB (1059966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f86d5fa421f23732d814d765abe49c2a458f0440b40eec14438505133e66e1`  
		Last Modified: Sat, 12 Oct 2024 01:53:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd70949cc7ad1f41cf63210756c9805c3f0e3266cc4d56de6f64480e03f6ce2`  
		Last Modified: Sat, 12 Oct 2024 01:53:59 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8471eac24553e3f6c77125c6f579a9da7571164ae1bed77e7ae72f24199797c9`  
		Last Modified: Sat, 12 Oct 2024 01:54:04 GMT  
		Size: 231.9 MB (231919890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee2bad1f5bc7bbf78c553e2cbf71ea8c24e06e8fb85c0d77c13fee877e62702`  
		Last Modified: Sat, 12 Oct 2024 01:53:59 GMT  
		Size: 5.0 KB (4993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:8-noble` - unknown; unknown

```console
$ docker pull mongo@sha256:5a77da9bfd1ac93755957e13d49ee25ae1e27c11ae88e4f3a3ed9ffa6d1947b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2510457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c823b35e2e188b476aae5899918fdd5fac7fcc6e439193a80aa7de4ebfb5593`

```dockerfile
```

-	Layers:
	-	`sha256:8222a16d47213ae75179461a660dae56e22074487fff343972d4e8511e052976`  
		Last Modified: Sat, 12 Oct 2024 01:53:58 GMT  
		Size: 2.5 MB (2481880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81d475e63d113ded516a592d2c441f49ba7071ce3d31013354debe3daa2289a2`  
		Last Modified: Sat, 12 Oct 2024 01:53:58 GMT  
		Size: 28.6 KB (28577 bytes)  
		MIME: application/vnd.in-toto+json
