## `mongo:5-focal`

```console
$ docker pull mongo@sha256:6a86d408d50cc7bb45bc616ebe226d275663fd06daf71c104bdfbc8e69b42f38
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mongo:5-focal` - linux; amd64

```console
$ docker pull mongo@sha256:f4a1073bd8807edae53fd43e433886731983ebdbbdceda6dd3561a789f9f8c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.3 MB (265273211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80cfe23a003e3b810828a8011ee1ab1486fbdc120e7b288984aa198a3e789ff2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 13 Dec 2023 10:27:43 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:27:45 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Wed, 13 Dec 2023 10:27:45 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:04:56 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Thu, 18 Jan 2024 17:04:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Jan 2024 17:04:56 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:04:56 GMT
ENV JSYAML_VERSION=3.13.1
# Thu, 18 Jan 2024 17:04:56 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:04:56 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Jan 2024 17:04:56 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:04:56 GMT
ARG MONGO_PACKAGE=mongodb-org
# Thu, 18 Jan 2024 17:04:56 GMT
ARG MONGO_REPO=repo.mongodb.org
# Thu, 18 Jan 2024 17:04:56 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Thu, 18 Jan 2024 17:04:56 GMT
ENV MONGO_MAJOR=5.0
# Thu, 18 Jan 2024 17:04:56 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Thu, 18 Jan 2024 17:04:56 GMT
ENV MONGO_VERSION=5.0.24
# Thu, 18 Jan 2024 17:04:56 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Thu, 18 Jan 2024 17:04:56 GMT
VOLUME [/data/db /data/configdb]
# Thu, 18 Jan 2024 17:04:56 GMT
ENV HOME=/data/db
# Thu, 18 Jan 2024 17:04:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:04:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:04:56 GMT
EXPOSE map[27017/tcp:{}]
# Thu, 18 Jan 2024 17:04:56 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:527f5363b98e562da03d2e0bbf86fd7c34f487bffd9b27a3cf0a9afea2f0ee1f`  
		Last Modified: Wed, 13 Dec 2023 10:48:59 GMT  
		Size: 27.5 MB (27512774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfa7a2267f1955648cc79cbb390a82c224445edb1c581e54d2a1ee110899998`  
		Last Modified: Thu, 18 Jan 2024 23:59:14 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b5b0d5071fafbd2b60feec199d8fc3be3f25f802633dd932675b0c6fa6a68e7`  
		Last Modified: Thu, 18 Jan 2024 23:59:13 GMT  
		Size: 8.4 MB (8373254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29cc04619cf630455f4e9cd22e53f03be8994efc9bb3a1851f9763dafa14506`  
		Last Modified: Thu, 18 Jan 2024 23:59:13 GMT  
		Size: 1.1 MB (1100514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41279fccacc72a08e2327d59728438eaf2550c4c4bdc57847d35fa78479c3f37`  
		Last Modified: Thu, 18 Jan 2024 23:59:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5fc86c58b14e2d4d1baed932e1acd04201bb70cab006f84cbe2631e55b6b7af`  
		Last Modified: Thu, 18 Jan 2024 23:59:14 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c63a8580732c2037453e6254b12cee2d8d3c9d13188a06ba952c6b7e7bf356df`  
		Last Modified: Thu, 18 Jan 2024 23:59:14 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba6a83088d0d039a00a904274ad1844758f7ceb5fd0dd538bbbaf358e57b07c`  
		Last Modified: Thu, 18 Jan 2024 23:59:18 GMT  
		Size: 228.3 MB (228278124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bff0621f8e80a0a70c74032a17ecaf055162c69b918b1771c025934eb547d6`  
		Last Modified: Thu, 18 Jan 2024 23:59:15 GMT  
		Size: 5.0 KB (4994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:5-focal` - unknown; unknown

```console
$ docker pull mongo@sha256:51de6c1f458eece3f1fce5fac3a86cde8fa3e109ec9cead490c4579d2f94af06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2759662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd5162903bf1cd6e6eb192126bbbaada248cd5ac7d5b591cd3f1360a9e0a473`

```dockerfile
```

-	Layers:
	-	`sha256:3c84a48fc3d15de68de684dc5f6126ab9423491c52c4b6d8e40ba6e37d596d90`  
		Last Modified: Thu, 18 Jan 2024 23:59:13 GMT  
		Size: 2.7 MB (2731043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25c37dbb64ae9d1599b079f8f1b8fdf05fa524cd766661df0bd0b2e43266e8f7`  
		Last Modified: Thu, 18 Jan 2024 23:59:13 GMT  
		Size: 28.6 KB (28619 bytes)  
		MIME: application/vnd.in-toto+json

### `mongo:5-focal` - linux; arm64 variant v8

```console
$ docker pull mongo@sha256:f29251851db04402dfb330e9d0ca2a9e0106af05da8babd07c26f1217522a873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.6 MB (257628295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1b6c748921e1ce0d853d2133c2cc8bb915bff20a3f31dc668f1e61e3fcea505`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mongod"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
CMD ["/bin/bash"]
# Tue, 19 Dec 2023 19:08:50 GMT
RUN set -eux; 	groupadd --gid 999 --system mongodb; 	useradd --uid 999 --system --gid mongodb --home-dir /data/db mongodb; 	mkdir -p /data/db /data/configdb; 	chown -R mongodb:mongodb /data/db /data/configdb # buildkit
# Tue, 19 Dec 2023 19:08:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		gnupg 		jq 		numactl 		procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Dec 2023 19:08:50 GMT
ENV GOSU_VERSION=1.16
# Tue, 19 Dec 2023 19:08:50 GMT
ENV JSYAML_VERSION=3.13.1
# Tue, 19 Dec 2023 19:08:50 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		mkdir -p /opt/js-yaml/; 	wget -O /opt/js-yaml/js-yaml.js "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/dist/js-yaml.js"; 	wget -O /opt/js-yaml/package.json "https://github.com/nodeca/js-yaml/raw/${JSYAML_VERSION}/package.json"; 	ln -s /opt/js-yaml/js-yaml.js /js-yaml.js; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 19 Dec 2023 19:08:50 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 19 Dec 2023 19:08:50 GMT
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	set -- 'F5679A222C647C87527C2F8CB00A0BD1E2C63C11'; 	for key; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$@" > /etc/apt/keyrings/mongodb.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 Dec 2023 19:08:50 GMT
ARG MONGO_PACKAGE=mongodb-org
# Tue, 19 Dec 2023 19:08:50 GMT
ARG MONGO_REPO=repo.mongodb.org
# Tue, 19 Dec 2023 19:08:50 GMT
ENV MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
# Tue, 19 Dec 2023 19:08:50 GMT
ENV MONGO_MAJOR=5.0
# Tue, 19 Dec 2023 19:08:50 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN echo "deb [ signed-by=/etc/apt/keyrings/mongodb.gpg ] http://$MONGO_REPO/apt/ubuntu focal/${MONGO_PACKAGE%-unstable}/$MONGO_MAJOR multiverse" | tee "/etc/apt/sources.list.d/${MONGO_PACKAGE%-unstable}.list" # buildkit
# Tue, 19 Dec 2023 19:08:50 GMT
ENV MONGO_VERSION=5.0.23
# Tue, 19 Dec 2023 19:08:50 GMT
# ARGS: MONGO_PACKAGE=mongodb-org MONGO_REPO=repo.mongodb.org
RUN set -x 	&& export DEBIAN_FRONTEND=noninteractive 	&& apt-get update 	&& apt-get install -y 		${MONGO_PACKAGE}=$MONGO_VERSION 		${MONGO_PACKAGE}-server=$MONGO_VERSION 		${MONGO_PACKAGE}-shell=$MONGO_VERSION 		${MONGO_PACKAGE}-mongos=$MONGO_VERSION 		${MONGO_PACKAGE}-tools=$MONGO_VERSION 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mongodb 	&& mv /etc/mongod.conf /etc/mongod.conf.orig # buildkit
# Tue, 19 Dec 2023 19:08:50 GMT
VOLUME [/data/db /data/configdb]
# Tue, 19 Dec 2023 19:08:50 GMT
ENV HOME=/data/db
# Tue, 19 Dec 2023 19:08:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Dec 2023 19:08:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Dec 2023 19:08:50 GMT
EXPOSE map[27017/tcp:{}]
# Tue, 19 Dec 2023 19:08:50 GMT
CMD ["mongod"]
```

-	Layers:
	-	`sha256:d519a3a2a796a075e4e40e5c4a1513aa8db8f8fdf009662bf6858f0149143b28`  
		Last Modified: Wed, 13 Dec 2023 10:49:05 GMT  
		Size: 26.0 MB (25974768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352ba6b7451f9d95719ad43508919c914407cf286d0b7fb6e1ee9a02cd51b045`  
		Last Modified: Mon, 18 Dec 2023 19:51:47 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ded41913893fb2c19b7f6cb4b21f0e12639a543c69be1d62dbe3afdf3fbc42`  
		Last Modified: Mon, 18 Dec 2023 19:51:48 GMT  
		Size: 8.2 MB (8200494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ab25682bfe74e5ec2f8feaf928bbba54d7139f2c30e2ee063f5b347f288996`  
		Last Modified: Wed, 20 Dec 2023 22:10:12 GMT  
		Size: 1.0 MB (1032196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb81d91cc097017e7f7b40df750f78372e32354fd7495c225c4ffbbd8eab22f8`  
		Last Modified: Wed, 20 Dec 2023 22:10:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7d67ca0832893ab9fbc7dd6f775ad4bc9f05d962d08fc72973c4ae3a1e016e`  
		Last Modified: Wed, 20 Dec 2023 22:10:11 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02064cf3c6fe875ad2084c98199038705142a2cf41985be7d5c586b2266b9cb9`  
		Last Modified: Wed, 20 Dec 2023 22:10:11 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc920ef7a447e0a1730c44bd9bca9a83260291722e33aa01aab7952d61f7d8f`  
		Last Modified: Wed, 20 Dec 2023 22:10:19 GMT  
		Size: 222.4 MB (222412291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff07ac66c2fa6aa1599cc32d5d2720bb0c7fbafd9dca8ea5fbac67f292a2cc2f`  
		Last Modified: Wed, 20 Dec 2023 22:10:12 GMT  
		Size: 5.0 KB (4996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mongo:5-focal` - unknown; unknown

```console
$ docker pull mongo@sha256:78e5573c91b1bf1a40fdf549bbf3bc695bf41e3226b16574bef9dbfe6731a321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2759346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94440a32067fa87da13e41ef3bc7c90e7854398d438bb2b2488a8594eb0e7460`

```dockerfile
```

-	Layers:
	-	`sha256:9bc62583dabb65ff721f53967b376951d9306df13eb16e82ec377706c1a1e976`  
		Last Modified: Wed, 20 Dec 2023 22:10:12 GMT  
		Size: 2.7 MB (2730874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f78886e1c50d0fd719c5c4c0de051432ebbfa70959002a8e961b5027fb9cc06`  
		Last Modified: Wed, 20 Dec 2023 22:10:11 GMT  
		Size: 28.5 KB (28472 bytes)  
		MIME: application/vnd.in-toto+json
