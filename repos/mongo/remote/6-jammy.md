## `mongo:6-jammy`

```console
$ docker pull mongo@sha256:fc601b8dd26f6348f70becd8888dff1dd08253f4c3e67dcebddfeffdcb768ccf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:6-jammy` - linux; amd64

```console
$ docker pull mongo@sha256:f06a25c6a55b98171b65672afbd6c96127d2b66c82c5357dc9275c483cf81ba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.4 MB (252415780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a9f5cd13295c4df8da0c26b0a0adb70b15aac6727dec193d18d82baa1549872`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 18 Apr 2024 10:01:32 GMT
ARG RELEASE
# Thu, 18 Apr 2024 10:01:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Apr 2024 10:01:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Apr 2024 10:01:32 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Apr 2024 10:01:32 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Thu, 18 Apr 2024 10:01:32 GMT
CMD ["/bin/bash"]
# Thu, 18 Apr 2024 10:01:32 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Thu, 18 Apr 2024 10:01:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Apr 2024 10:01:32 GMT
ENV GOSU_VERSION=1.17
# Thu, 18 Apr 2024 10:01:32 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 18 Apr 2024 10:01:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-6.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '39BD841E4BE5FB195A65400E6A26B1AE64C3C388' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Apr 2024 10:01:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Apr 2024 10:01:32 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 18 Apr 2024 10:01:32 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 18 Apr 2024 10:01:32 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 18 Apr 2024 10:01:32 GMT
ENV MONGO_MAJOR=6.0
# Thu, 18 Apr 2024 10:01:32 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Thu, 18 Apr 2024 10:01:32 GMT
ENV MONGO_VERSION=6.0.15
# Thu, 18 Apr 2024 10:01:32 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Thu, 18 Apr 2024 10:01:32 GMT
VOLUME [/data/db /data/configdb]
# Thu, 18 Apr 2024 10:01:32 GMT
ENV HOME=/data/db
# Thu, 18 Apr 2024 10:01:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 10:01:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Apr 2024 10:01:32 GMT
EXPOSE map[27017/tcp:{}]
# Thu, 18 Apr 2024 10:01:32 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed43470d34557ca6b9e1bef37e531e72352ae7a368f25379e2faf1372a06f3ac`  
		Last Modified: Wed, 05 Jun 2024 02:22:03 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d06bb5e0759e36d84e4556a4be54f3849d74fc8f8a7a2c65b42d45539a92a733`  
		Last Modified: Wed, 05 Jun 2024 02:22:03 GMT  
		Size: 1.5 MB (1500799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1744a61682a80c21e787d65cd107554ac44869d0dfe405e18f10bc6f684b4935`  
		Last Modified: Wed, 05 Jun 2024 02:22:03 GMT  
		Size: 1.1 MB (1094635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf90a833dd2f0fefe16fe7dee7b1f922c6d7f8ff3e237a0e6946aade8a2ca9ad`  
		Last Modified: Wed, 05 Jun 2024 02:22:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b87df9d851826428fc613b2853478b2a7c727e1b61529614cf81134f6a9d6945`  
		Last Modified: Wed, 05 Jun 2024 02:22:04 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f578d2a329fcbc1f0abe4a592ed22f087091d30c617db47dd00f18c1cc482e`  
		Last Modified: Wed, 05 Jun 2024 02:22:07 GMT  
		Size: 220.3 MB (220279430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555a62b8f2fd99ed71b5c30f577486fe63e5f9539d32ec8d340c2641e2efccdd`  
		Last Modified: Wed, 05 Jun 2024 02:22:04 GMT  
		Size: 5.0 KB (4999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:6-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:d5e8e202420dfd9dcf3c86f63e377a930ec947e49c864e744299b71bcc810990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3027509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c45383e9323d6f51cd78e183a071dc53aa664bebca6413db10248a70959bfeef`

```dockerfile
```

-	Layers:
	-	`sha256:182cfbcfe37755785a6e398f5850abf1f9457952df7e5f1cc4f412b7b4acc3e6`  
		Last Modified: Wed, 05 Jun 2024 02:22:03 GMT  
		Size: 3.0 MB (3000512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f937dd1253df0b6af1eeb94307f153bb5ab958fe48b9ac00bf89ed7cc2fcdba`  
		Last Modified: Wed, 05 Jun 2024 02:22:03 GMT  
		Size: 27.0 KB (26997 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:6-jammy` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:8c4c9e3e664ab5e95b9410f1c80d477923a88f5eec94f97f1e47e93e8dbdd5f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.3 MB (245331039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e37825a4a656122482302627c8811b8da65d2661b7d2585e9290b79bb01b5593`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Thu, 18 Apr 2024 10:01:32 GMT
ARG RELEASE
# Thu, 18 Apr 2024 10:01:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Apr 2024 10:01:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Apr 2024 10:01:32 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Apr 2024 10:01:32 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Thu, 18 Apr 2024 10:01:32 GMT
CMD ["/bin/bash"]
# Thu, 18 Apr 2024 10:01:32 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Thu, 18 Apr 2024 10:01:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Apr 2024 10:01:32 GMT
ENV GOSU_VERSION=1.17
# Thu, 18 Apr 2024 10:01:32 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 18 Apr 2024 10:01:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		export GNUPGHOME="$(mktemp -d)"; 	wget -O KEYS 'https://pgp.mongodb.com/server-6.0.asc'; 	gpg --batch --import KEYS; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export --armor '39BD841E4BE5FB195A65400E6A26B1AE64C3C388' > /etc/apt/keyrings/mongodb.asc; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" KEYS; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Apr 2024 10:01:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Apr 2024 10:01:32 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 18 Apr 2024 10:01:32 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 18 Apr 2024 10:01:32 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 18 Apr 2024 10:01:32 GMT
ENV MONGO_MAJOR=6.0
# Thu, 18 Apr 2024 10:01:32 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.asc ] http://$MONGO_REPO/apt/ubuntu jammy/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Thu, 18 Apr 2024 10:01:32 GMT
ENV MONGO_VERSION=6.0.15
# Thu, 18 Apr 2024 10:01:32 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 		${MONGO_PACKAGE}-database=$MONGO_VERSION 		${MONGO_PACKAGE}-database-tools-extra=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Thu, 18 Apr 2024 10:01:32 GMT
VOLUME [/data/db /data/configdb]
# Thu, 18 Apr 2024 10:01:32 GMT
ENV HOME=/data/db
# Thu, 18 Apr 2024 10:01:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 10:01:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Apr 2024 10:01:32 GMT
EXPOSE map[27017/tcp:{}]
# Thu, 18 Apr 2024 10:01:32 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f33a3006c470fcf35e360ed94e30a65c5fe9f95ce0cf0c9ab2243273d4df519`  
		Last Modified: Wed, 05 Jun 2024 16:22:58 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eedf0c2fd07791b0a7c85eaf3c323cc949fdc8675f41c70a6bfff588bab98d26`  
		Last Modified: Wed, 05 Jun 2024 16:22:58 GMT  
		Size: 1.5 MB (1467355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126b0aa21c63b92202a1b2a4c83889ae6fa7dc17252a9538cbc30ff96abd3071`  
		Last Modified: Wed, 05 Jun 2024 16:26:40 GMT  
		Size: 1.0 MB (1028921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e915518433afe84b0c2d934d6225ad5cf09ebc2f5c0e716fa428d4d71f8c6a`  
		Last Modified: Wed, 05 Jun 2024 16:26:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed0dc05706b8b3ebc798520adaa711d857503df34ebad4e5ac8eab039d568bb`  
		Last Modified: Wed, 05 Jun 2024 16:26:40 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:defa63f59e94cb014c5f870c882e09a12699621b57c31ff54da87ddb1591d7d5`  
		Last Modified: Wed, 05 Jun 2024 16:26:46 GMT  
		Size: 215.5 MB (215465815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0155a0d755ee3fc7ff86ff8d94f36ab59b06dd93f0b11490d31cfaa6528a77`  
		Last Modified: Wed, 05 Jun 2024 16:26:41 GMT  
		Size: 5.0 KB (5000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:6-jammy` - unknown; unknown

```console
$ docker pull mongo@sha256:58788cfe18072dce6e89e1161ab86a758e85dca7de0561b6fccd5b1d90b8e12a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3028151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:647c3cc3ec98aa9678105e2005fb960047d3403f54b1c18040971be1dc7d3736`

```dockerfile
```

-	Layers:
	-	`sha256:21dc916c91dc096f513c75afb6b70a3d48def2db4a96df037a6a3aefed22a087`  
		Last Modified: Wed, 05 Jun 2024 16:26:40 GMT  
		Size: 3.0 MB (3000830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c5eedc0cf396e02e0ecdfeb8042f104c2872d2a718be8afd9196ddcca0e0c1b`  
		Last Modified: Wed, 05 Jun 2024 16:26:40 GMT  
		Size: 27.3 KB (27321 bytes)  
		MIME: application/vnd.in-toto+json
