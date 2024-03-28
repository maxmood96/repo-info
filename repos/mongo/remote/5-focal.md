## `mongo:5-focal`

```console
$ docker pull mongo@sha256:b8859fcec6780d861c848eb6e58938fe84b0108f64719fce113dd5840e05eee7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:5-focal` - linux; amd64

```console
$ docker pull mongo@sha256:9a7b5a805a2752116763fdae97f945d57b71da092fad1505ec9256d5cf0aab4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.9 MB (266870726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f8ebaef09e71c4047294d57265af1ada011e530d9061fe0069588d4e7102cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 16 Feb 2024 21:32:49 GMT
ARG RELEASE
# Fri, 16 Feb 2024 21:32:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 21:32:52 GMT
ADD file:a25798f31219000d6a82d2c9258743926b1a400530d12dbb1eadf2c2519f9888 in / 
# Fri, 16 Feb 2024 21:32:52 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 22:01:21 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Tue, 26 Mar 2024 22:01:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 Mar 2024 22:01:21 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 22:01:21 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 26 Mar 2024 22:01:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-5.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 22:01:21 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 26 Mar 2024 22:01:21 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 26 Mar 2024 22:01:21 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 26 Mar 2024 22:01:21 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 26 Mar 2024 22:01:21 GMT
ENV MONGO_MAJOR=5.0
# Tue, 26 Mar 2024 22:01:21 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Tue, 26 Mar 2024 22:01:21 GMT
ENV MONGO_VERSION=5.0.26
# Tue, 26 Mar 2024 22:01:21 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Tue, 26 Mar 2024 22:01:21 GMT
VOLUME [/data/db /data/configdb]
# Tue, 26 Mar 2024 22:01:21 GMT
ENV HOME=/data/db
# Tue, 26 Mar 2024 22:01:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 22:01:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 22:01:21 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 26 Mar 2024 22:01:21 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:17d0386c2fff30a5b92652bbef2b84639dba9b9f17bdbb819c8d10badd827fdb`  
		Last Modified: Fri, 16 Feb 2024 21:40:52 GMT  
		Size: 27.5 MB (27514312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89edeba9996686fd9c6ff99c34371503e21f098d829e22ddb3e2cd261b063b06`  
		Last Modified: Wed, 27 Mar 2024 21:50:53 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4501537394b72b41345a29810df2a6f2597f825b2b43473bb095ec66554e0ad8`  
		Last Modified: Wed, 27 Mar 2024 21:50:54 GMT  
		Size: 3.1 MB (3076159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c40e9a1a9cc334fe0a43f03ecc397689c8d9ded235cbb0cee5bc24332795d1`  
		Last Modified: Wed, 27 Mar 2024 21:50:54 GMT  
		Size: 1.1 MB (1091347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd79ce9342f300e2328b1ad1139e84739dd7fd3c5b403feba5bd8180a62ed770`  
		Last Modified: Wed, 27 Mar 2024 21:50:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250404df8e2d9759fc341a4774e702c939b4d3fb2c230a22c6e99b720a6f3199`  
		Last Modified: Wed, 27 Mar 2024 21:50:54 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad816d0ced04e9d106662c2fd7240ff417d8a5ae0c298633083718a582d1563`  
		Last Modified: Wed, 27 Mar 2024 21:51:01 GMT  
		Size: 235.2 MB (235181750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1b05ec1990cfe2ca7724266a3501537cf1162097bb44d1dfb1c01e93240be7`  
		Last Modified: Wed, 27 Mar 2024 21:50:55 GMT  
		Size: 5.0 KB (4997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:5-focal` - unknown; unknown

```console
$ docker pull mongo@sha256:005621bd4cf2939112582ba095727f31b2d89d78c56a7eecc8fc4639f5fb964e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3026761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:950e9473d64d67ea6099e2a400ebf1b9910fbaf598060b8a95c17331b3651cdb`

```dockerfile
```

-	Layers:
	-	`sha256:529acc3ec40dd9e7941f57b22e44a081c12f284940adfed268fb503acb79963a`  
		Last Modified: Wed, 27 Mar 2024 21:50:53 GMT  
		Size: 3.0 MB (2999930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e2e3cca714186a14d21f5e63969e3ce457fd4a47b9ac50aba5b44f071c9ff8c`  
		Last Modified: Wed, 27 Mar 2024 21:50:53 GMT  
		Size: 26.8 KB (26831 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:5-focal` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:266172515130a995e07abae81b3392de4a9aef3a96496113222bebb54d53c9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.2 MB (259179777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0c88796ee19f131095dc4695ca21edfc967049cfb9309615a38cc08c9c749d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Fri, 16 Feb 2024 19:15:01 GMT
ARG RELEASE
# Fri, 16 Feb 2024 19:15:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 19:15:01 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 19:15:06 GMT
ADD file:a8303c80b47ec165c276111aa6f98ee877e4da60ddafa00b7547032a3de7935d in / 
# Fri, 16 Feb 2024 19:15:06 GMT
CMD ["/bin/bash"]
# Tue, 26 Mar 2024 22:01:21 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Tue, 26 Mar 2024 22:01:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 26 Mar 2024 22:01:21 GMT
ENV GOSU_VERSION=1.17
# Tue, 26 Mar 2024 22:01:21 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 26 Mar 2024 22:01:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-5.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 26 Mar 2024 22:01:21 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 26 Mar 2024 22:01:21 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 26 Mar 2024 22:01:21 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 26 Mar 2024 22:01:21 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 26 Mar 2024 22:01:21 GMT
ENV MONGO_MAJOR=5.0
# Tue, 26 Mar 2024 22:01:21 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Tue, 26 Mar 2024 22:01:21 GMT
ENV MONGO_VERSION=5.0.26
# Tue, 26 Mar 2024 22:01:21 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Tue, 26 Mar 2024 22:01:21 GMT
VOLUME [/data/db /data/configdb]
# Tue, 26 Mar 2024 22:01:21 GMT
ENV HOME=/data/db
# Tue, 26 Mar 2024 22:01:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Mar 2024 22:01:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Mar 2024 22:01:21 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 26 Mar 2024 22:01:21 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:6aae4cfdd5a10a8b0554e75c4c14ae38022a0c8f08dc5d769a735c705670cab7`  
		Last Modified: Fri, 16 Feb 2024 21:40:59 GMT  
		Size: 26.0 MB (25974391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07886f594025d7f95fc3f5d0228d02d9cc0d2e469c812b82c32017a5f83195b8`  
		Last Modified: Wed, 27 Mar 2024 21:54:08 GMT  
		Size: 1.8 KB (1801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4e0038c86cd2d6dd77126be867021216b7f86d6b20f7780ff35119e9178e29`  
		Last Modified: Wed, 27 Mar 2024 21:54:08 GMT  
		Size: 2.9 MB (2929567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b161945e091116183b7c7653a37e3a2fb8b6a97ac09d5d945b2c94ce11e8c3d`  
		Last Modified: Wed, 27 Mar 2024 21:54:09 GMT  
		Size: 1.0 MB (1023651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bced92f23deaeba26baced1cccbed7453230ce26c3da8ab686827399c5395c`  
		Last Modified: Wed, 27 Mar 2024 21:54:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e155b6681aecfe6d1967a601361d26398a2c9c00e4f2e9f90cbc89ba0fda52`  
		Last Modified: Wed, 27 Mar 2024 21:54:09 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572f802418d59c6487f417425059d27988a29b85ebae746a9e67365e0cfe904c`  
		Last Modified: Wed, 27 Mar 2024 21:54:14 GMT  
		Size: 229.2 MB (229244994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c792f7dbd9218fe78ad43752063029359e81db39701ffa49471cf95d02e5c81`  
		Last Modified: Wed, 27 Mar 2024 21:54:10 GMT  
		Size: 5.0 KB (4995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:5-focal` - unknown; unknown

```console
$ docker pull mongo@sha256:0817d9670b86af801217d3fbe597f6c693fe4dfda10918e96ad7ad792b17a4d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3026848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:706f78ee0ea8d9d86c0b7f83e234627de2ad4cff67d18052ff5b7223d0ed9861`

```dockerfile
```

-	Layers:
	-	`sha256:e14f44e31383d579507227c83b24c4e7893d196a6fa092ec3f5872d4eb8668ed`  
		Last Modified: Wed, 27 Mar 2024 21:54:09 GMT  
		Size: 3.0 MB (3000163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea32eec6b38096a7c4353ecb3d568f465c6eecabc049f7cac1e0ea04536b3091`  
		Last Modified: Wed, 27 Mar 2024 21:54:08 GMT  
		Size: 26.7 KB (26685 bytes)  
		MIME: application/vnd.in-toto+json
