<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clickhouse`

-	[`clickhouse:25.8`](#clickhouse258)
-	[`clickhouse:25.8-jammy`](#clickhouse258-jammy)
-	[`clickhouse:25.8.20`](#clickhouse25820)
-	[`clickhouse:25.8.20-jammy`](#clickhouse25820-jammy)
-	[`clickhouse:25.8.20.4`](#clickhouse258204)
-	[`clickhouse:25.8.20.4-jammy`](#clickhouse258204-jammy)
-	[`clickhouse:26.1`](#clickhouse261)
-	[`clickhouse:26.1-jammy`](#clickhouse261-jammy)
-	[`clickhouse:26.1.6`](#clickhouse2616)
-	[`clickhouse:26.1.6-jammy`](#clickhouse2616-jammy)
-	[`clickhouse:26.1.6.6`](#clickhouse26166)
-	[`clickhouse:26.1.6.6-jammy`](#clickhouse26166-jammy)
-	[`clickhouse:26.2`](#clickhouse262)
-	[`clickhouse:26.2-jammy`](#clickhouse262-jammy)
-	[`clickhouse:26.2.5`](#clickhouse2625)
-	[`clickhouse:26.2.5-jammy`](#clickhouse2625-jammy)
-	[`clickhouse:26.2.5.45`](#clickhouse262545)
-	[`clickhouse:26.2.5.45-jammy`](#clickhouse262545-jammy)
-	[`clickhouse:26.3`](#clickhouse263)
-	[`clickhouse:26.3-jammy`](#clickhouse263-jammy)
-	[`clickhouse:26.3.1`](#clickhouse2631)
-	[`clickhouse:26.3.1-jammy`](#clickhouse2631-jammy)
-	[`clickhouse:26.3.1.896`](#clickhouse2631896)
-	[`clickhouse:26.3.1.896-jammy`](#clickhouse2631896-jammy)
-	[`clickhouse:jammy`](#clickhousejammy)
-	[`clickhouse:latest`](#clickhouselatest)
-	[`clickhouse:lts`](#clickhouselts)
-	[`clickhouse:lts-jammy`](#clickhouselts-jammy)

## `clickhouse:25.8`

```console
$ docker pull clickhouse@sha256:af9eeec63d54a753f6ac672dcc18bba7638a5f8e28a4452dd600c3443bd72cd4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8` - linux; amd64

```console
$ docker pull clickhouse@sha256:739d1bcb96bcbf5a68bb9990eeac0f28a25eaca3dc705a6cc456621e7b25bee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229197199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e84eefaf1a197c4a1f7303bc361c9509188d2b70879a0fa5e4bca65c816a46e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:48 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:48 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:48 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:48 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:48 GMT
ARG VERSION=25.8.20.4
# Wed, 01 Apr 2026 20:05:48 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:06:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:06:16 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:06:16 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:06:16 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:06:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:06:16 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:06:16 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:06:16 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:06:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50810b101a74fa3ade6095362caa2fe053ff0ab41235a6458748fa98f15fae32`  
		Last Modified: Wed, 01 Apr 2026 20:06:39 GMT  
		Size: 7.6 MB (7598285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04b88720ec4b7622e25ab385c5fd4934b04e690af79ed82239acedee15dfb4c`  
		Last Modified: Wed, 01 Apr 2026 20:06:43 GMT  
		Size: 191.0 MB (190992472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8931aa010689625eb5ff9ee4669d6a1fabd2fd6384b09a7fc5f92d0cea6a346`  
		Last Modified: Wed, 01 Apr 2026 20:06:39 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d4b94c9b182f8d7c80d6cd85252eddd39c375812e2258e5ff3db4478ed3611`  
		Last Modified: Wed, 01 Apr 2026 20:06:39 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5624661f82ba20fc04de3037e5682a4900bf184c5126b80b43f0f51e69f62e00`  
		Last Modified: Wed, 01 Apr 2026 20:06:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85561baa6c19e21395b1c93aa8b940c843900913ee316d6c47ad89a7f0718507`  
		Last Modified: Wed, 01 Apr 2026 20:06:40 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab291619b83b80963aa183c137c9abe3bc4658d68dd7320a95e3b0fa2ab51df`  
		Last Modified: Wed, 01 Apr 2026 20:06:41 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:db97e7e60e9a02b405ab5222aedb6ff10ae68f266fef30fd6087f43c412b28f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da4e2ebba9604f890c29711e1912dbc93237688239955b5e9c3cb4ce1acb5dfc`

```dockerfile
```

-	Layers:
	-	`sha256:e58f2b299ecbeefe5e6e8729f95ac8d1e785b4b06c99a07045b6fe113991cf31`  
		Last Modified: Wed, 01 Apr 2026 20:06:38 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:32be4c1dd2614fc495e7ffd44b0dee0af86a03ac04022047b9308db6b4f9cca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214130600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85dda075ad0db4aa4f9d508e9cb07a9ab93c27e76c2af592d26539e8526e34e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:50 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:50 GMT
ARG VERSION=25.8.20.4
# Wed, 01 Apr 2026 20:05:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:06:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:06:24 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:06:24 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:06:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:06:24 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:06:25 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:06:25 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:06:25 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:06:25 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:06:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f75f23fcc33b72895cf555ffa4070d4da76c889bf0e91213288d9786d71c7d`  
		Last Modified: Wed, 01 Apr 2026 20:06:44 GMT  
		Size: 7.6 MB (7577469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9025cdce507e2847915b78e6e5691e47972b6b7922fe9dbe4884e8cb9dd6f592`  
		Last Modified: Wed, 01 Apr 2026 20:06:48 GMT  
		Size: 178.1 MB (178076161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7067b5c9fc843b965e3dbe1527487410fa933c0f179da54cdb3839c57ada6713`  
		Last Modified: Wed, 01 Apr 2026 20:06:43 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff48e89dfe0d91604906fb0ecc92d5b160074ca8dff51b3a91d8e13dd60e603`  
		Last Modified: Wed, 01 Apr 2026 20:06:43 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530d203f48f62d7f71b0b2ebc2703addefa8d8104165ef4befe569d717941c99`  
		Last Modified: Wed, 01 Apr 2026 20:06:45 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60747abf839f79255fce2a173ba79cc3e8a57de0b4e663df71d0075bad13534c`  
		Last Modified: Wed, 01 Apr 2026 20:06:45 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab291619b83b80963aa183c137c9abe3bc4658d68dd7320a95e3b0fa2ab51df`  
		Last Modified: Wed, 01 Apr 2026 20:06:41 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4b3f7d6a3653f62c6dcf6125d71a2a38fef913c9398e51c2e95ec34fd6f4cf65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86adc5e8c864e3e1604b5907c5d6b96e95a5ceacd37de053af543e1a19853b0d`

```dockerfile
```

-	Layers:
	-	`sha256:15242b9690a6158beb09abb1748ac27fb03bbc8cc82b8fdca7434bb3471b2925`  
		Last Modified: Wed, 01 Apr 2026 20:06:43 GMT  
		Size: 25.6 KB (25610 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8-jammy`

```console
$ docker pull clickhouse@sha256:af9eeec63d54a753f6ac672dcc18bba7638a5f8e28a4452dd600c3443bd72cd4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:739d1bcb96bcbf5a68bb9990eeac0f28a25eaca3dc705a6cc456621e7b25bee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229197199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e84eefaf1a197c4a1f7303bc361c9509188d2b70879a0fa5e4bca65c816a46e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:48 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:48 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:48 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:48 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:48 GMT
ARG VERSION=25.8.20.4
# Wed, 01 Apr 2026 20:05:48 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:06:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:06:16 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:06:16 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:06:16 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:06:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:06:16 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:06:16 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:06:16 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:06:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50810b101a74fa3ade6095362caa2fe053ff0ab41235a6458748fa98f15fae32`  
		Last Modified: Wed, 01 Apr 2026 20:06:39 GMT  
		Size: 7.6 MB (7598285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04b88720ec4b7622e25ab385c5fd4934b04e690af79ed82239acedee15dfb4c`  
		Last Modified: Wed, 01 Apr 2026 20:06:43 GMT  
		Size: 191.0 MB (190992472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8931aa010689625eb5ff9ee4669d6a1fabd2fd6384b09a7fc5f92d0cea6a346`  
		Last Modified: Wed, 01 Apr 2026 20:06:39 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d4b94c9b182f8d7c80d6cd85252eddd39c375812e2258e5ff3db4478ed3611`  
		Last Modified: Wed, 01 Apr 2026 20:06:39 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5624661f82ba20fc04de3037e5682a4900bf184c5126b80b43f0f51e69f62e00`  
		Last Modified: Wed, 01 Apr 2026 20:06:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85561baa6c19e21395b1c93aa8b940c843900913ee316d6c47ad89a7f0718507`  
		Last Modified: Wed, 01 Apr 2026 20:06:40 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab291619b83b80963aa183c137c9abe3bc4658d68dd7320a95e3b0fa2ab51df`  
		Last Modified: Wed, 01 Apr 2026 20:06:41 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:db97e7e60e9a02b405ab5222aedb6ff10ae68f266fef30fd6087f43c412b28f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da4e2ebba9604f890c29711e1912dbc93237688239955b5e9c3cb4ce1acb5dfc`

```dockerfile
```

-	Layers:
	-	`sha256:e58f2b299ecbeefe5e6e8729f95ac8d1e785b4b06c99a07045b6fe113991cf31`  
		Last Modified: Wed, 01 Apr 2026 20:06:38 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:32be4c1dd2614fc495e7ffd44b0dee0af86a03ac04022047b9308db6b4f9cca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214130600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85dda075ad0db4aa4f9d508e9cb07a9ab93c27e76c2af592d26539e8526e34e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:50 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:50 GMT
ARG VERSION=25.8.20.4
# Wed, 01 Apr 2026 20:05:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:06:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:06:24 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:06:24 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:06:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:06:24 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:06:25 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:06:25 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:06:25 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:06:25 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:06:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f75f23fcc33b72895cf555ffa4070d4da76c889bf0e91213288d9786d71c7d`  
		Last Modified: Wed, 01 Apr 2026 20:06:44 GMT  
		Size: 7.6 MB (7577469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9025cdce507e2847915b78e6e5691e47972b6b7922fe9dbe4884e8cb9dd6f592`  
		Last Modified: Wed, 01 Apr 2026 20:06:48 GMT  
		Size: 178.1 MB (178076161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7067b5c9fc843b965e3dbe1527487410fa933c0f179da54cdb3839c57ada6713`  
		Last Modified: Wed, 01 Apr 2026 20:06:43 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff48e89dfe0d91604906fb0ecc92d5b160074ca8dff51b3a91d8e13dd60e603`  
		Last Modified: Wed, 01 Apr 2026 20:06:43 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530d203f48f62d7f71b0b2ebc2703addefa8d8104165ef4befe569d717941c99`  
		Last Modified: Wed, 01 Apr 2026 20:06:45 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60747abf839f79255fce2a173ba79cc3e8a57de0b4e663df71d0075bad13534c`  
		Last Modified: Wed, 01 Apr 2026 20:06:45 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab291619b83b80963aa183c137c9abe3bc4658d68dd7320a95e3b0fa2ab51df`  
		Last Modified: Wed, 01 Apr 2026 20:06:41 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4b3f7d6a3653f62c6dcf6125d71a2a38fef913c9398e51c2e95ec34fd6f4cf65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86adc5e8c864e3e1604b5907c5d6b96e95a5ceacd37de053af543e1a19853b0d`

```dockerfile
```

-	Layers:
	-	`sha256:15242b9690a6158beb09abb1748ac27fb03bbc8cc82b8fdca7434bb3471b2925`  
		Last Modified: Wed, 01 Apr 2026 20:06:43 GMT  
		Size: 25.6 KB (25610 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.20`

```console
$ docker pull clickhouse@sha256:af9eeec63d54a753f6ac672dcc18bba7638a5f8e28a4452dd600c3443bd72cd4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.20` - linux; amd64

```console
$ docker pull clickhouse@sha256:739d1bcb96bcbf5a68bb9990eeac0f28a25eaca3dc705a6cc456621e7b25bee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229197199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e84eefaf1a197c4a1f7303bc361c9509188d2b70879a0fa5e4bca65c816a46e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:48 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:48 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:48 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:48 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:48 GMT
ARG VERSION=25.8.20.4
# Wed, 01 Apr 2026 20:05:48 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:06:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:06:16 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:06:16 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:06:16 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:06:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:06:16 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:06:16 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:06:16 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:06:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50810b101a74fa3ade6095362caa2fe053ff0ab41235a6458748fa98f15fae32`  
		Last Modified: Wed, 01 Apr 2026 20:06:39 GMT  
		Size: 7.6 MB (7598285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04b88720ec4b7622e25ab385c5fd4934b04e690af79ed82239acedee15dfb4c`  
		Last Modified: Wed, 01 Apr 2026 20:06:43 GMT  
		Size: 191.0 MB (190992472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8931aa010689625eb5ff9ee4669d6a1fabd2fd6384b09a7fc5f92d0cea6a346`  
		Last Modified: Wed, 01 Apr 2026 20:06:39 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d4b94c9b182f8d7c80d6cd85252eddd39c375812e2258e5ff3db4478ed3611`  
		Last Modified: Wed, 01 Apr 2026 20:06:39 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5624661f82ba20fc04de3037e5682a4900bf184c5126b80b43f0f51e69f62e00`  
		Last Modified: Wed, 01 Apr 2026 20:06:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85561baa6c19e21395b1c93aa8b940c843900913ee316d6c47ad89a7f0718507`  
		Last Modified: Wed, 01 Apr 2026 20:06:40 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab291619b83b80963aa183c137c9abe3bc4658d68dd7320a95e3b0fa2ab51df`  
		Last Modified: Wed, 01 Apr 2026 20:06:41 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.20` - unknown; unknown

```console
$ docker pull clickhouse@sha256:db97e7e60e9a02b405ab5222aedb6ff10ae68f266fef30fd6087f43c412b28f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da4e2ebba9604f890c29711e1912dbc93237688239955b5e9c3cb4ce1acb5dfc`

```dockerfile
```

-	Layers:
	-	`sha256:e58f2b299ecbeefe5e6e8729f95ac8d1e785b4b06c99a07045b6fe113991cf31`  
		Last Modified: Wed, 01 Apr 2026 20:06:38 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.20` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:32be4c1dd2614fc495e7ffd44b0dee0af86a03ac04022047b9308db6b4f9cca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214130600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85dda075ad0db4aa4f9d508e9cb07a9ab93c27e76c2af592d26539e8526e34e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:50 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:50 GMT
ARG VERSION=25.8.20.4
# Wed, 01 Apr 2026 20:05:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:06:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:06:24 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:06:24 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:06:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:06:24 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:06:25 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:06:25 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:06:25 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:06:25 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:06:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f75f23fcc33b72895cf555ffa4070d4da76c889bf0e91213288d9786d71c7d`  
		Last Modified: Wed, 01 Apr 2026 20:06:44 GMT  
		Size: 7.6 MB (7577469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9025cdce507e2847915b78e6e5691e47972b6b7922fe9dbe4884e8cb9dd6f592`  
		Last Modified: Wed, 01 Apr 2026 20:06:48 GMT  
		Size: 178.1 MB (178076161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7067b5c9fc843b965e3dbe1527487410fa933c0f179da54cdb3839c57ada6713`  
		Last Modified: Wed, 01 Apr 2026 20:06:43 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff48e89dfe0d91604906fb0ecc92d5b160074ca8dff51b3a91d8e13dd60e603`  
		Last Modified: Wed, 01 Apr 2026 20:06:43 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530d203f48f62d7f71b0b2ebc2703addefa8d8104165ef4befe569d717941c99`  
		Last Modified: Wed, 01 Apr 2026 20:06:45 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60747abf839f79255fce2a173ba79cc3e8a57de0b4e663df71d0075bad13534c`  
		Last Modified: Wed, 01 Apr 2026 20:06:45 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab291619b83b80963aa183c137c9abe3bc4658d68dd7320a95e3b0fa2ab51df`  
		Last Modified: Wed, 01 Apr 2026 20:06:41 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.20` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4b3f7d6a3653f62c6dcf6125d71a2a38fef913c9398e51c2e95ec34fd6f4cf65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86adc5e8c864e3e1604b5907c5d6b96e95a5ceacd37de053af543e1a19853b0d`

```dockerfile
```

-	Layers:
	-	`sha256:15242b9690a6158beb09abb1748ac27fb03bbc8cc82b8fdca7434bb3471b2925`  
		Last Modified: Wed, 01 Apr 2026 20:06:43 GMT  
		Size: 25.6 KB (25610 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.20-jammy`

```console
$ docker pull clickhouse@sha256:af9eeec63d54a753f6ac672dcc18bba7638a5f8e28a4452dd600c3443bd72cd4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.20-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:739d1bcb96bcbf5a68bb9990eeac0f28a25eaca3dc705a6cc456621e7b25bee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229197199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e84eefaf1a197c4a1f7303bc361c9509188d2b70879a0fa5e4bca65c816a46e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:48 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:48 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:48 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:48 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:48 GMT
ARG VERSION=25.8.20.4
# Wed, 01 Apr 2026 20:05:48 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:06:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:06:16 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:06:16 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:06:16 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:06:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:06:16 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:06:16 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:06:16 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:06:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50810b101a74fa3ade6095362caa2fe053ff0ab41235a6458748fa98f15fae32`  
		Last Modified: Wed, 01 Apr 2026 20:06:39 GMT  
		Size: 7.6 MB (7598285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04b88720ec4b7622e25ab385c5fd4934b04e690af79ed82239acedee15dfb4c`  
		Last Modified: Wed, 01 Apr 2026 20:06:43 GMT  
		Size: 191.0 MB (190992472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8931aa010689625eb5ff9ee4669d6a1fabd2fd6384b09a7fc5f92d0cea6a346`  
		Last Modified: Wed, 01 Apr 2026 20:06:39 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d4b94c9b182f8d7c80d6cd85252eddd39c375812e2258e5ff3db4478ed3611`  
		Last Modified: Wed, 01 Apr 2026 20:06:39 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5624661f82ba20fc04de3037e5682a4900bf184c5126b80b43f0f51e69f62e00`  
		Last Modified: Wed, 01 Apr 2026 20:06:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85561baa6c19e21395b1c93aa8b940c843900913ee316d6c47ad89a7f0718507`  
		Last Modified: Wed, 01 Apr 2026 20:06:40 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab291619b83b80963aa183c137c9abe3bc4658d68dd7320a95e3b0fa2ab51df`  
		Last Modified: Wed, 01 Apr 2026 20:06:41 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.20-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:db97e7e60e9a02b405ab5222aedb6ff10ae68f266fef30fd6087f43c412b28f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da4e2ebba9604f890c29711e1912dbc93237688239955b5e9c3cb4ce1acb5dfc`

```dockerfile
```

-	Layers:
	-	`sha256:e58f2b299ecbeefe5e6e8729f95ac8d1e785b4b06c99a07045b6fe113991cf31`  
		Last Modified: Wed, 01 Apr 2026 20:06:38 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.20-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:32be4c1dd2614fc495e7ffd44b0dee0af86a03ac04022047b9308db6b4f9cca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214130600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85dda075ad0db4aa4f9d508e9cb07a9ab93c27e76c2af592d26539e8526e34e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:50 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:50 GMT
ARG VERSION=25.8.20.4
# Wed, 01 Apr 2026 20:05:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:06:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:06:24 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:06:24 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:06:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:06:24 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:06:25 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:06:25 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:06:25 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:06:25 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:06:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f75f23fcc33b72895cf555ffa4070d4da76c889bf0e91213288d9786d71c7d`  
		Last Modified: Wed, 01 Apr 2026 20:06:44 GMT  
		Size: 7.6 MB (7577469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9025cdce507e2847915b78e6e5691e47972b6b7922fe9dbe4884e8cb9dd6f592`  
		Last Modified: Wed, 01 Apr 2026 20:06:48 GMT  
		Size: 178.1 MB (178076161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7067b5c9fc843b965e3dbe1527487410fa933c0f179da54cdb3839c57ada6713`  
		Last Modified: Wed, 01 Apr 2026 20:06:43 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff48e89dfe0d91604906fb0ecc92d5b160074ca8dff51b3a91d8e13dd60e603`  
		Last Modified: Wed, 01 Apr 2026 20:06:43 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530d203f48f62d7f71b0b2ebc2703addefa8d8104165ef4befe569d717941c99`  
		Last Modified: Wed, 01 Apr 2026 20:06:45 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60747abf839f79255fce2a173ba79cc3e8a57de0b4e663df71d0075bad13534c`  
		Last Modified: Wed, 01 Apr 2026 20:06:45 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab291619b83b80963aa183c137c9abe3bc4658d68dd7320a95e3b0fa2ab51df`  
		Last Modified: Wed, 01 Apr 2026 20:06:41 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.20-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4b3f7d6a3653f62c6dcf6125d71a2a38fef913c9398e51c2e95ec34fd6f4cf65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86adc5e8c864e3e1604b5907c5d6b96e95a5ceacd37de053af543e1a19853b0d`

```dockerfile
```

-	Layers:
	-	`sha256:15242b9690a6158beb09abb1748ac27fb03bbc8cc82b8fdca7434bb3471b2925`  
		Last Modified: Wed, 01 Apr 2026 20:06:43 GMT  
		Size: 25.6 KB (25610 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.20.4`

```console
$ docker pull clickhouse@sha256:af9eeec63d54a753f6ac672dcc18bba7638a5f8e28a4452dd600c3443bd72cd4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.20.4` - linux; amd64

```console
$ docker pull clickhouse@sha256:739d1bcb96bcbf5a68bb9990eeac0f28a25eaca3dc705a6cc456621e7b25bee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229197199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e84eefaf1a197c4a1f7303bc361c9509188d2b70879a0fa5e4bca65c816a46e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:48 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:48 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:48 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:48 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:48 GMT
ARG VERSION=25.8.20.4
# Wed, 01 Apr 2026 20:05:48 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:06:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:06:16 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:06:16 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:06:16 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:06:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:06:16 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:06:16 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:06:16 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:06:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50810b101a74fa3ade6095362caa2fe053ff0ab41235a6458748fa98f15fae32`  
		Last Modified: Wed, 01 Apr 2026 20:06:39 GMT  
		Size: 7.6 MB (7598285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04b88720ec4b7622e25ab385c5fd4934b04e690af79ed82239acedee15dfb4c`  
		Last Modified: Wed, 01 Apr 2026 20:06:43 GMT  
		Size: 191.0 MB (190992472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8931aa010689625eb5ff9ee4669d6a1fabd2fd6384b09a7fc5f92d0cea6a346`  
		Last Modified: Wed, 01 Apr 2026 20:06:39 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d4b94c9b182f8d7c80d6cd85252eddd39c375812e2258e5ff3db4478ed3611`  
		Last Modified: Wed, 01 Apr 2026 20:06:39 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5624661f82ba20fc04de3037e5682a4900bf184c5126b80b43f0f51e69f62e00`  
		Last Modified: Wed, 01 Apr 2026 20:06:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85561baa6c19e21395b1c93aa8b940c843900913ee316d6c47ad89a7f0718507`  
		Last Modified: Wed, 01 Apr 2026 20:06:40 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab291619b83b80963aa183c137c9abe3bc4658d68dd7320a95e3b0fa2ab51df`  
		Last Modified: Wed, 01 Apr 2026 20:06:41 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.20.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:db97e7e60e9a02b405ab5222aedb6ff10ae68f266fef30fd6087f43c412b28f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da4e2ebba9604f890c29711e1912dbc93237688239955b5e9c3cb4ce1acb5dfc`

```dockerfile
```

-	Layers:
	-	`sha256:e58f2b299ecbeefe5e6e8729f95ac8d1e785b4b06c99a07045b6fe113991cf31`  
		Last Modified: Wed, 01 Apr 2026 20:06:38 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.20.4` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:32be4c1dd2614fc495e7ffd44b0dee0af86a03ac04022047b9308db6b4f9cca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214130600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85dda075ad0db4aa4f9d508e9cb07a9ab93c27e76c2af592d26539e8526e34e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:50 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:50 GMT
ARG VERSION=25.8.20.4
# Wed, 01 Apr 2026 20:05:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:06:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:06:24 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:06:24 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:06:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:06:24 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:06:25 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:06:25 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:06:25 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:06:25 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:06:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f75f23fcc33b72895cf555ffa4070d4da76c889bf0e91213288d9786d71c7d`  
		Last Modified: Wed, 01 Apr 2026 20:06:44 GMT  
		Size: 7.6 MB (7577469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9025cdce507e2847915b78e6e5691e47972b6b7922fe9dbe4884e8cb9dd6f592`  
		Last Modified: Wed, 01 Apr 2026 20:06:48 GMT  
		Size: 178.1 MB (178076161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7067b5c9fc843b965e3dbe1527487410fa933c0f179da54cdb3839c57ada6713`  
		Last Modified: Wed, 01 Apr 2026 20:06:43 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff48e89dfe0d91604906fb0ecc92d5b160074ca8dff51b3a91d8e13dd60e603`  
		Last Modified: Wed, 01 Apr 2026 20:06:43 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530d203f48f62d7f71b0b2ebc2703addefa8d8104165ef4befe569d717941c99`  
		Last Modified: Wed, 01 Apr 2026 20:06:45 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60747abf839f79255fce2a173ba79cc3e8a57de0b4e663df71d0075bad13534c`  
		Last Modified: Wed, 01 Apr 2026 20:06:45 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab291619b83b80963aa183c137c9abe3bc4658d68dd7320a95e3b0fa2ab51df`  
		Last Modified: Wed, 01 Apr 2026 20:06:41 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.20.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4b3f7d6a3653f62c6dcf6125d71a2a38fef913c9398e51c2e95ec34fd6f4cf65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86adc5e8c864e3e1604b5907c5d6b96e95a5ceacd37de053af543e1a19853b0d`

```dockerfile
```

-	Layers:
	-	`sha256:15242b9690a6158beb09abb1748ac27fb03bbc8cc82b8fdca7434bb3471b2925`  
		Last Modified: Wed, 01 Apr 2026 20:06:43 GMT  
		Size: 25.6 KB (25610 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.20.4-jammy`

```console
$ docker pull clickhouse@sha256:af9eeec63d54a753f6ac672dcc18bba7638a5f8e28a4452dd600c3443bd72cd4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.20.4-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:739d1bcb96bcbf5a68bb9990eeac0f28a25eaca3dc705a6cc456621e7b25bee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229197199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e84eefaf1a197c4a1f7303bc361c9509188d2b70879a0fa5e4bca65c816a46e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:48 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:48 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:48 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:48 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:48 GMT
ARG VERSION=25.8.20.4
# Wed, 01 Apr 2026 20:05:48 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:06:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:06:16 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:06:16 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:06:16 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:06:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:06:16 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:06:16 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:06:16 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:06:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50810b101a74fa3ade6095362caa2fe053ff0ab41235a6458748fa98f15fae32`  
		Last Modified: Wed, 01 Apr 2026 20:06:39 GMT  
		Size: 7.6 MB (7598285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04b88720ec4b7622e25ab385c5fd4934b04e690af79ed82239acedee15dfb4c`  
		Last Modified: Wed, 01 Apr 2026 20:06:43 GMT  
		Size: 191.0 MB (190992472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8931aa010689625eb5ff9ee4669d6a1fabd2fd6384b09a7fc5f92d0cea6a346`  
		Last Modified: Wed, 01 Apr 2026 20:06:39 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d4b94c9b182f8d7c80d6cd85252eddd39c375812e2258e5ff3db4478ed3611`  
		Last Modified: Wed, 01 Apr 2026 20:06:39 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5624661f82ba20fc04de3037e5682a4900bf184c5126b80b43f0f51e69f62e00`  
		Last Modified: Wed, 01 Apr 2026 20:06:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85561baa6c19e21395b1c93aa8b940c843900913ee316d6c47ad89a7f0718507`  
		Last Modified: Wed, 01 Apr 2026 20:06:40 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab291619b83b80963aa183c137c9abe3bc4658d68dd7320a95e3b0fa2ab51df`  
		Last Modified: Wed, 01 Apr 2026 20:06:41 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.20.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:db97e7e60e9a02b405ab5222aedb6ff10ae68f266fef30fd6087f43c412b28f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da4e2ebba9604f890c29711e1912dbc93237688239955b5e9c3cb4ce1acb5dfc`

```dockerfile
```

-	Layers:
	-	`sha256:e58f2b299ecbeefe5e6e8729f95ac8d1e785b4b06c99a07045b6fe113991cf31`  
		Last Modified: Wed, 01 Apr 2026 20:06:38 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.20.4-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:32be4c1dd2614fc495e7ffd44b0dee0af86a03ac04022047b9308db6b4f9cca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214130600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85dda075ad0db4aa4f9d508e9cb07a9ab93c27e76c2af592d26539e8526e34e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:50 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:50 GMT
ARG VERSION=25.8.20.4
# Wed, 01 Apr 2026 20:05:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:06:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:06:24 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:06:24 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:06:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:06:24 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:06:25 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:06:25 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:06:25 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:06:25 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:06:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f75f23fcc33b72895cf555ffa4070d4da76c889bf0e91213288d9786d71c7d`  
		Last Modified: Wed, 01 Apr 2026 20:06:44 GMT  
		Size: 7.6 MB (7577469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9025cdce507e2847915b78e6e5691e47972b6b7922fe9dbe4884e8cb9dd6f592`  
		Last Modified: Wed, 01 Apr 2026 20:06:48 GMT  
		Size: 178.1 MB (178076161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7067b5c9fc843b965e3dbe1527487410fa933c0f179da54cdb3839c57ada6713`  
		Last Modified: Wed, 01 Apr 2026 20:06:43 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff48e89dfe0d91604906fb0ecc92d5b160074ca8dff51b3a91d8e13dd60e603`  
		Last Modified: Wed, 01 Apr 2026 20:06:43 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530d203f48f62d7f71b0b2ebc2703addefa8d8104165ef4befe569d717941c99`  
		Last Modified: Wed, 01 Apr 2026 20:06:45 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60747abf839f79255fce2a173ba79cc3e8a57de0b4e663df71d0075bad13534c`  
		Last Modified: Wed, 01 Apr 2026 20:06:45 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab291619b83b80963aa183c137c9abe3bc4658d68dd7320a95e3b0fa2ab51df`  
		Last Modified: Wed, 01 Apr 2026 20:06:41 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.20.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4b3f7d6a3653f62c6dcf6125d71a2a38fef913c9398e51c2e95ec34fd6f4cf65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86adc5e8c864e3e1604b5907c5d6b96e95a5ceacd37de053af543e1a19853b0d`

```dockerfile
```

-	Layers:
	-	`sha256:15242b9690a6158beb09abb1748ac27fb03bbc8cc82b8fdca7434bb3471b2925`  
		Last Modified: Wed, 01 Apr 2026 20:06:43 GMT  
		Size: 25.6 KB (25610 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1`

```console
$ docker pull clickhouse@sha256:5d5aa8d6e8b904ad22735039f18c43248f439763904fa83535ddeeb5e6d6f96c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1` - linux; amd64

```console
$ docker pull clickhouse@sha256:52200268014aeeeba10f4d02c42f7798a066d8065a4fecb8aea6e556b2257e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246290745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad3ba111ac19acdfab4a979220da70b803e7a4e3ed3088ff82d648b94a8478c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:18 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:18 GMT
ARG VERSION=26.1.6.6
# Wed, 01 Apr 2026 20:05:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:05:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:05:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:05:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:05:49 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:05:49 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:05:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:05:49 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:05:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:05:49 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:05:49 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:05:49 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:05:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e34ce9febdccc444a1fea7a6bede340f193f9e11b6c35d5598f03d1443df60c`  
		Last Modified: Wed, 01 Apr 2026 20:06:15 GMT  
		Size: 7.6 MB (7598372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c5917217ecfff511dc88aee17c1202a88418fcea042d2a1fed61bae4fdb041`  
		Last Modified: Wed, 01 Apr 2026 20:06:21 GMT  
		Size: 208.1 MB (208085910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c771c9bb4fd6100cefe1ac7b33e8e49ce3bbe8d93bc18f961ed3407cc7e83c`  
		Last Modified: Wed, 01 Apr 2026 20:06:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f20df3ab129314d8ce88530fadccfa3e914ba5cdda4b7d2fe406a0860509b8e`  
		Last Modified: Wed, 01 Apr 2026 20:06:15 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9ac4f42e04c2fb9132dfcd34ba8e63aeedccd9b6220a42b55080281ace3f86`  
		Last Modified: Wed, 01 Apr 2026 20:06:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b55806d8b1db79619afd1aa445b17a45e87d1ea6ad15ea2a7159dbb847c729`  
		Last Modified: Wed, 01 Apr 2026 20:06:16 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45561826e56e9196a428ea93727947135407e4c3e32bafe0e31c115cdb6002cf`  
		Last Modified: Wed, 01 Apr 2026 20:06:17 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1` - unknown; unknown

```console
$ docker pull clickhouse@sha256:7898c25a1af9f318583a40f666e26bbb95a9a6d2c506108e6776039a333ce79d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8139abb2e57b413abf1bab2a428b6f42dfb6406ce0e2e5c5fc71daec28029b1`

```dockerfile
```

-	Layers:
	-	`sha256:d9c2de4925ec0f5d901e4e18513a86db55d04e29951d914bf9fa835131b2d03b`  
		Last Modified: Wed, 01 Apr 2026 20:06:14 GMT  
		Size: 25.4 KB (25406 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:25c8c04ddb836b9063c7d63b21afd2dd058aae2817e9448741044685aaa4308d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228491258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a9a0615f81a6830c833d49ddd263ee61266e96c65e96f96a94d1d3eebebe723`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:35 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:35 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:35 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:35 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:35 GMT
ARG VERSION=26.1.6.6
# Wed, 01 Apr 2026 20:05:35 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:06:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:06:11 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:06:11 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:06:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:06:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:06:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:06:11 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:06:11 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:06:11 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:06:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ada8fdaeb998316b2548d1fc1b09087cc8000738d528d392d161a224cdb3797`  
		Last Modified: Wed, 01 Apr 2026 20:06:31 GMT  
		Size: 7.6 MB (7577433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c5eba9aefc3b25f55d620303971e46131e25b70049fbd0de58c47e5fa15350`  
		Last Modified: Wed, 01 Apr 2026 20:06:35 GMT  
		Size: 192.4 MB (192436835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0a36959eb8a87ed21ae6aef06322de0f477621655bdb871979d192d81a285b`  
		Last Modified: Wed, 01 Apr 2026 20:06:31 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:857f2a50cd1dbcd91b08f2c5df1df86bf01e2ef98b84a57f6ca73c2fe5068f1b`  
		Last Modified: Wed, 01 Apr 2026 20:06:31 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed81fdc7d0828b9daa83c0964f1f1c53470aa55346d398ba81af961b995fb564`  
		Last Modified: Wed, 01 Apr 2026 20:06:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6916b718c7c0811fd3570b9e1e97237a18f05d4b97facc9032f528de98fd2b6`  
		Last Modified: Wed, 01 Apr 2026 20:06:32 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890b8be52c1a68fbccbceaa8f973ac48811716d744dc7d294e5c9ba46734db3c`  
		Last Modified: Wed, 01 Apr 2026 20:06:34 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3a40f5f1f0ad9a2a97c80910bc984889921cae3a166925c4f0fd6af26fcfd1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02014b7969bad6ee8a9e8674a1c43937083bfaf85ab74bf3abbb811ffd94272f`

```dockerfile
```

-	Layers:
	-	`sha256:bbeabefee9e25dd54d6f8380cf6562c47f0cf6d121f9944d7898675a65c2ea8b`  
		Last Modified: Wed, 01 Apr 2026 20:06:31 GMT  
		Size: 25.6 KB (25595 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1-jammy`

```console
$ docker pull clickhouse@sha256:5d5aa8d6e8b904ad22735039f18c43248f439763904fa83535ddeeb5e6d6f96c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:52200268014aeeeba10f4d02c42f7798a066d8065a4fecb8aea6e556b2257e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246290745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad3ba111ac19acdfab4a979220da70b803e7a4e3ed3088ff82d648b94a8478c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:18 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:18 GMT
ARG VERSION=26.1.6.6
# Wed, 01 Apr 2026 20:05:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:05:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:05:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:05:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:05:49 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:05:49 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:05:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:05:49 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:05:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:05:49 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:05:49 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:05:49 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:05:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e34ce9febdccc444a1fea7a6bede340f193f9e11b6c35d5598f03d1443df60c`  
		Last Modified: Wed, 01 Apr 2026 20:06:15 GMT  
		Size: 7.6 MB (7598372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c5917217ecfff511dc88aee17c1202a88418fcea042d2a1fed61bae4fdb041`  
		Last Modified: Wed, 01 Apr 2026 20:06:21 GMT  
		Size: 208.1 MB (208085910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c771c9bb4fd6100cefe1ac7b33e8e49ce3bbe8d93bc18f961ed3407cc7e83c`  
		Last Modified: Wed, 01 Apr 2026 20:06:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f20df3ab129314d8ce88530fadccfa3e914ba5cdda4b7d2fe406a0860509b8e`  
		Last Modified: Wed, 01 Apr 2026 20:06:15 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9ac4f42e04c2fb9132dfcd34ba8e63aeedccd9b6220a42b55080281ace3f86`  
		Last Modified: Wed, 01 Apr 2026 20:06:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b55806d8b1db79619afd1aa445b17a45e87d1ea6ad15ea2a7159dbb847c729`  
		Last Modified: Wed, 01 Apr 2026 20:06:16 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45561826e56e9196a428ea93727947135407e4c3e32bafe0e31c115cdb6002cf`  
		Last Modified: Wed, 01 Apr 2026 20:06:17 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:7898c25a1af9f318583a40f666e26bbb95a9a6d2c506108e6776039a333ce79d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8139abb2e57b413abf1bab2a428b6f42dfb6406ce0e2e5c5fc71daec28029b1`

```dockerfile
```

-	Layers:
	-	`sha256:d9c2de4925ec0f5d901e4e18513a86db55d04e29951d914bf9fa835131b2d03b`  
		Last Modified: Wed, 01 Apr 2026 20:06:14 GMT  
		Size: 25.4 KB (25406 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:25c8c04ddb836b9063c7d63b21afd2dd058aae2817e9448741044685aaa4308d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228491258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a9a0615f81a6830c833d49ddd263ee61266e96c65e96f96a94d1d3eebebe723`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:35 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:35 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:35 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:35 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:35 GMT
ARG VERSION=26.1.6.6
# Wed, 01 Apr 2026 20:05:35 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:06:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:06:11 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:06:11 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:06:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:06:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:06:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:06:11 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:06:11 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:06:11 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:06:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ada8fdaeb998316b2548d1fc1b09087cc8000738d528d392d161a224cdb3797`  
		Last Modified: Wed, 01 Apr 2026 20:06:31 GMT  
		Size: 7.6 MB (7577433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c5eba9aefc3b25f55d620303971e46131e25b70049fbd0de58c47e5fa15350`  
		Last Modified: Wed, 01 Apr 2026 20:06:35 GMT  
		Size: 192.4 MB (192436835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0a36959eb8a87ed21ae6aef06322de0f477621655bdb871979d192d81a285b`  
		Last Modified: Wed, 01 Apr 2026 20:06:31 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:857f2a50cd1dbcd91b08f2c5df1df86bf01e2ef98b84a57f6ca73c2fe5068f1b`  
		Last Modified: Wed, 01 Apr 2026 20:06:31 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed81fdc7d0828b9daa83c0964f1f1c53470aa55346d398ba81af961b995fb564`  
		Last Modified: Wed, 01 Apr 2026 20:06:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6916b718c7c0811fd3570b9e1e97237a18f05d4b97facc9032f528de98fd2b6`  
		Last Modified: Wed, 01 Apr 2026 20:06:32 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890b8be52c1a68fbccbceaa8f973ac48811716d744dc7d294e5c9ba46734db3c`  
		Last Modified: Wed, 01 Apr 2026 20:06:34 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3a40f5f1f0ad9a2a97c80910bc984889921cae3a166925c4f0fd6af26fcfd1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02014b7969bad6ee8a9e8674a1c43937083bfaf85ab74bf3abbb811ffd94272f`

```dockerfile
```

-	Layers:
	-	`sha256:bbeabefee9e25dd54d6f8380cf6562c47f0cf6d121f9944d7898675a65c2ea8b`  
		Last Modified: Wed, 01 Apr 2026 20:06:31 GMT  
		Size: 25.6 KB (25595 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1.6`

```console
$ docker pull clickhouse@sha256:5d5aa8d6e8b904ad22735039f18c43248f439763904fa83535ddeeb5e6d6f96c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1.6` - linux; amd64

```console
$ docker pull clickhouse@sha256:52200268014aeeeba10f4d02c42f7798a066d8065a4fecb8aea6e556b2257e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246290745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad3ba111ac19acdfab4a979220da70b803e7a4e3ed3088ff82d648b94a8478c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:18 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:18 GMT
ARG VERSION=26.1.6.6
# Wed, 01 Apr 2026 20:05:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:05:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:05:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:05:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:05:49 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:05:49 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:05:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:05:49 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:05:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:05:49 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:05:49 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:05:49 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:05:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e34ce9febdccc444a1fea7a6bede340f193f9e11b6c35d5598f03d1443df60c`  
		Last Modified: Wed, 01 Apr 2026 20:06:15 GMT  
		Size: 7.6 MB (7598372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c5917217ecfff511dc88aee17c1202a88418fcea042d2a1fed61bae4fdb041`  
		Last Modified: Wed, 01 Apr 2026 20:06:21 GMT  
		Size: 208.1 MB (208085910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c771c9bb4fd6100cefe1ac7b33e8e49ce3bbe8d93bc18f961ed3407cc7e83c`  
		Last Modified: Wed, 01 Apr 2026 20:06:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f20df3ab129314d8ce88530fadccfa3e914ba5cdda4b7d2fe406a0860509b8e`  
		Last Modified: Wed, 01 Apr 2026 20:06:15 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9ac4f42e04c2fb9132dfcd34ba8e63aeedccd9b6220a42b55080281ace3f86`  
		Last Modified: Wed, 01 Apr 2026 20:06:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b55806d8b1db79619afd1aa445b17a45e87d1ea6ad15ea2a7159dbb847c729`  
		Last Modified: Wed, 01 Apr 2026 20:06:16 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45561826e56e9196a428ea93727947135407e4c3e32bafe0e31c115cdb6002cf`  
		Last Modified: Wed, 01 Apr 2026 20:06:17 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.6` - unknown; unknown

```console
$ docker pull clickhouse@sha256:7898c25a1af9f318583a40f666e26bbb95a9a6d2c506108e6776039a333ce79d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8139abb2e57b413abf1bab2a428b6f42dfb6406ce0e2e5c5fc71daec28029b1`

```dockerfile
```

-	Layers:
	-	`sha256:d9c2de4925ec0f5d901e4e18513a86db55d04e29951d914bf9fa835131b2d03b`  
		Last Modified: Wed, 01 Apr 2026 20:06:14 GMT  
		Size: 25.4 KB (25406 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1.6` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:25c8c04ddb836b9063c7d63b21afd2dd058aae2817e9448741044685aaa4308d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228491258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a9a0615f81a6830c833d49ddd263ee61266e96c65e96f96a94d1d3eebebe723`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:35 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:35 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:35 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:35 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:35 GMT
ARG VERSION=26.1.6.6
# Wed, 01 Apr 2026 20:05:35 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:06:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:06:11 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:06:11 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:06:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:06:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:06:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:06:11 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:06:11 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:06:11 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:06:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ada8fdaeb998316b2548d1fc1b09087cc8000738d528d392d161a224cdb3797`  
		Last Modified: Wed, 01 Apr 2026 20:06:31 GMT  
		Size: 7.6 MB (7577433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c5eba9aefc3b25f55d620303971e46131e25b70049fbd0de58c47e5fa15350`  
		Last Modified: Wed, 01 Apr 2026 20:06:35 GMT  
		Size: 192.4 MB (192436835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0a36959eb8a87ed21ae6aef06322de0f477621655bdb871979d192d81a285b`  
		Last Modified: Wed, 01 Apr 2026 20:06:31 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:857f2a50cd1dbcd91b08f2c5df1df86bf01e2ef98b84a57f6ca73c2fe5068f1b`  
		Last Modified: Wed, 01 Apr 2026 20:06:31 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed81fdc7d0828b9daa83c0964f1f1c53470aa55346d398ba81af961b995fb564`  
		Last Modified: Wed, 01 Apr 2026 20:06:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6916b718c7c0811fd3570b9e1e97237a18f05d4b97facc9032f528de98fd2b6`  
		Last Modified: Wed, 01 Apr 2026 20:06:32 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890b8be52c1a68fbccbceaa8f973ac48811716d744dc7d294e5c9ba46734db3c`  
		Last Modified: Wed, 01 Apr 2026 20:06:34 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.6` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3a40f5f1f0ad9a2a97c80910bc984889921cae3a166925c4f0fd6af26fcfd1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02014b7969bad6ee8a9e8674a1c43937083bfaf85ab74bf3abbb811ffd94272f`

```dockerfile
```

-	Layers:
	-	`sha256:bbeabefee9e25dd54d6f8380cf6562c47f0cf6d121f9944d7898675a65c2ea8b`  
		Last Modified: Wed, 01 Apr 2026 20:06:31 GMT  
		Size: 25.6 KB (25595 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1.6-jammy`

```console
$ docker pull clickhouse@sha256:5d5aa8d6e8b904ad22735039f18c43248f439763904fa83535ddeeb5e6d6f96c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1.6-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:52200268014aeeeba10f4d02c42f7798a066d8065a4fecb8aea6e556b2257e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246290745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad3ba111ac19acdfab4a979220da70b803e7a4e3ed3088ff82d648b94a8478c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:18 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:18 GMT
ARG VERSION=26.1.6.6
# Wed, 01 Apr 2026 20:05:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:05:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:05:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:05:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:05:49 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:05:49 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:05:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:05:49 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:05:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:05:49 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:05:49 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:05:49 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:05:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e34ce9febdccc444a1fea7a6bede340f193f9e11b6c35d5598f03d1443df60c`  
		Last Modified: Wed, 01 Apr 2026 20:06:15 GMT  
		Size: 7.6 MB (7598372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c5917217ecfff511dc88aee17c1202a88418fcea042d2a1fed61bae4fdb041`  
		Last Modified: Wed, 01 Apr 2026 20:06:21 GMT  
		Size: 208.1 MB (208085910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c771c9bb4fd6100cefe1ac7b33e8e49ce3bbe8d93bc18f961ed3407cc7e83c`  
		Last Modified: Wed, 01 Apr 2026 20:06:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f20df3ab129314d8ce88530fadccfa3e914ba5cdda4b7d2fe406a0860509b8e`  
		Last Modified: Wed, 01 Apr 2026 20:06:15 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9ac4f42e04c2fb9132dfcd34ba8e63aeedccd9b6220a42b55080281ace3f86`  
		Last Modified: Wed, 01 Apr 2026 20:06:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b55806d8b1db79619afd1aa445b17a45e87d1ea6ad15ea2a7159dbb847c729`  
		Last Modified: Wed, 01 Apr 2026 20:06:16 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45561826e56e9196a428ea93727947135407e4c3e32bafe0e31c115cdb6002cf`  
		Last Modified: Wed, 01 Apr 2026 20:06:17 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.6-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:7898c25a1af9f318583a40f666e26bbb95a9a6d2c506108e6776039a333ce79d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8139abb2e57b413abf1bab2a428b6f42dfb6406ce0e2e5c5fc71daec28029b1`

```dockerfile
```

-	Layers:
	-	`sha256:d9c2de4925ec0f5d901e4e18513a86db55d04e29951d914bf9fa835131b2d03b`  
		Last Modified: Wed, 01 Apr 2026 20:06:14 GMT  
		Size: 25.4 KB (25406 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1.6-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:25c8c04ddb836b9063c7d63b21afd2dd058aae2817e9448741044685aaa4308d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228491258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a9a0615f81a6830c833d49ddd263ee61266e96c65e96f96a94d1d3eebebe723`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:35 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:35 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:35 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:35 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:35 GMT
ARG VERSION=26.1.6.6
# Wed, 01 Apr 2026 20:05:35 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:06:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:06:11 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:06:11 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:06:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:06:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:06:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:06:11 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:06:11 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:06:11 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:06:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ada8fdaeb998316b2548d1fc1b09087cc8000738d528d392d161a224cdb3797`  
		Last Modified: Wed, 01 Apr 2026 20:06:31 GMT  
		Size: 7.6 MB (7577433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c5eba9aefc3b25f55d620303971e46131e25b70049fbd0de58c47e5fa15350`  
		Last Modified: Wed, 01 Apr 2026 20:06:35 GMT  
		Size: 192.4 MB (192436835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0a36959eb8a87ed21ae6aef06322de0f477621655bdb871979d192d81a285b`  
		Last Modified: Wed, 01 Apr 2026 20:06:31 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:857f2a50cd1dbcd91b08f2c5df1df86bf01e2ef98b84a57f6ca73c2fe5068f1b`  
		Last Modified: Wed, 01 Apr 2026 20:06:31 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed81fdc7d0828b9daa83c0964f1f1c53470aa55346d398ba81af961b995fb564`  
		Last Modified: Wed, 01 Apr 2026 20:06:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6916b718c7c0811fd3570b9e1e97237a18f05d4b97facc9032f528de98fd2b6`  
		Last Modified: Wed, 01 Apr 2026 20:06:32 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890b8be52c1a68fbccbceaa8f973ac48811716d744dc7d294e5c9ba46734db3c`  
		Last Modified: Wed, 01 Apr 2026 20:06:34 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.6-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3a40f5f1f0ad9a2a97c80910bc984889921cae3a166925c4f0fd6af26fcfd1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02014b7969bad6ee8a9e8674a1c43937083bfaf85ab74bf3abbb811ffd94272f`

```dockerfile
```

-	Layers:
	-	`sha256:bbeabefee9e25dd54d6f8380cf6562c47f0cf6d121f9944d7898675a65c2ea8b`  
		Last Modified: Wed, 01 Apr 2026 20:06:31 GMT  
		Size: 25.6 KB (25595 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1.6.6`

```console
$ docker pull clickhouse@sha256:5d5aa8d6e8b904ad22735039f18c43248f439763904fa83535ddeeb5e6d6f96c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1.6.6` - linux; amd64

```console
$ docker pull clickhouse@sha256:52200268014aeeeba10f4d02c42f7798a066d8065a4fecb8aea6e556b2257e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246290745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad3ba111ac19acdfab4a979220da70b803e7a4e3ed3088ff82d648b94a8478c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:18 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:18 GMT
ARG VERSION=26.1.6.6
# Wed, 01 Apr 2026 20:05:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:05:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:05:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:05:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:05:49 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:05:49 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:05:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:05:49 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:05:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:05:49 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:05:49 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:05:49 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:05:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e34ce9febdccc444a1fea7a6bede340f193f9e11b6c35d5598f03d1443df60c`  
		Last Modified: Wed, 01 Apr 2026 20:06:15 GMT  
		Size: 7.6 MB (7598372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c5917217ecfff511dc88aee17c1202a88418fcea042d2a1fed61bae4fdb041`  
		Last Modified: Wed, 01 Apr 2026 20:06:21 GMT  
		Size: 208.1 MB (208085910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c771c9bb4fd6100cefe1ac7b33e8e49ce3bbe8d93bc18f961ed3407cc7e83c`  
		Last Modified: Wed, 01 Apr 2026 20:06:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f20df3ab129314d8ce88530fadccfa3e914ba5cdda4b7d2fe406a0860509b8e`  
		Last Modified: Wed, 01 Apr 2026 20:06:15 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9ac4f42e04c2fb9132dfcd34ba8e63aeedccd9b6220a42b55080281ace3f86`  
		Last Modified: Wed, 01 Apr 2026 20:06:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b55806d8b1db79619afd1aa445b17a45e87d1ea6ad15ea2a7159dbb847c729`  
		Last Modified: Wed, 01 Apr 2026 20:06:16 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45561826e56e9196a428ea93727947135407e4c3e32bafe0e31c115cdb6002cf`  
		Last Modified: Wed, 01 Apr 2026 20:06:17 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.6.6` - unknown; unknown

```console
$ docker pull clickhouse@sha256:7898c25a1af9f318583a40f666e26bbb95a9a6d2c506108e6776039a333ce79d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8139abb2e57b413abf1bab2a428b6f42dfb6406ce0e2e5c5fc71daec28029b1`

```dockerfile
```

-	Layers:
	-	`sha256:d9c2de4925ec0f5d901e4e18513a86db55d04e29951d914bf9fa835131b2d03b`  
		Last Modified: Wed, 01 Apr 2026 20:06:14 GMT  
		Size: 25.4 KB (25406 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1.6.6` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:25c8c04ddb836b9063c7d63b21afd2dd058aae2817e9448741044685aaa4308d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228491258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a9a0615f81a6830c833d49ddd263ee61266e96c65e96f96a94d1d3eebebe723`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:35 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:35 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:35 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:35 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:35 GMT
ARG VERSION=26.1.6.6
# Wed, 01 Apr 2026 20:05:35 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:06:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:06:11 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:06:11 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:06:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:06:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:06:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:06:11 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:06:11 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:06:11 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:06:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ada8fdaeb998316b2548d1fc1b09087cc8000738d528d392d161a224cdb3797`  
		Last Modified: Wed, 01 Apr 2026 20:06:31 GMT  
		Size: 7.6 MB (7577433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c5eba9aefc3b25f55d620303971e46131e25b70049fbd0de58c47e5fa15350`  
		Last Modified: Wed, 01 Apr 2026 20:06:35 GMT  
		Size: 192.4 MB (192436835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0a36959eb8a87ed21ae6aef06322de0f477621655bdb871979d192d81a285b`  
		Last Modified: Wed, 01 Apr 2026 20:06:31 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:857f2a50cd1dbcd91b08f2c5df1df86bf01e2ef98b84a57f6ca73c2fe5068f1b`  
		Last Modified: Wed, 01 Apr 2026 20:06:31 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed81fdc7d0828b9daa83c0964f1f1c53470aa55346d398ba81af961b995fb564`  
		Last Modified: Wed, 01 Apr 2026 20:06:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6916b718c7c0811fd3570b9e1e97237a18f05d4b97facc9032f528de98fd2b6`  
		Last Modified: Wed, 01 Apr 2026 20:06:32 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890b8be52c1a68fbccbceaa8f973ac48811716d744dc7d294e5c9ba46734db3c`  
		Last Modified: Wed, 01 Apr 2026 20:06:34 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.6.6` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3a40f5f1f0ad9a2a97c80910bc984889921cae3a166925c4f0fd6af26fcfd1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02014b7969bad6ee8a9e8674a1c43937083bfaf85ab74bf3abbb811ffd94272f`

```dockerfile
```

-	Layers:
	-	`sha256:bbeabefee9e25dd54d6f8380cf6562c47f0cf6d121f9944d7898675a65c2ea8b`  
		Last Modified: Wed, 01 Apr 2026 20:06:31 GMT  
		Size: 25.6 KB (25595 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1.6.6-jammy`

```console
$ docker pull clickhouse@sha256:5d5aa8d6e8b904ad22735039f18c43248f439763904fa83535ddeeb5e6d6f96c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1.6.6-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:52200268014aeeeba10f4d02c42f7798a066d8065a4fecb8aea6e556b2257e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246290745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad3ba111ac19acdfab4a979220da70b803e7a4e3ed3088ff82d648b94a8478c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:18 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:18 GMT
ARG VERSION=26.1.6.6
# Wed, 01 Apr 2026 20:05:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:05:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:05:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:05:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:05:49 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:05:49 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:05:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:05:49 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:05:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:05:49 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:05:49 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:05:49 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:05:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e34ce9febdccc444a1fea7a6bede340f193f9e11b6c35d5598f03d1443df60c`  
		Last Modified: Wed, 01 Apr 2026 20:06:15 GMT  
		Size: 7.6 MB (7598372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c5917217ecfff511dc88aee17c1202a88418fcea042d2a1fed61bae4fdb041`  
		Last Modified: Wed, 01 Apr 2026 20:06:21 GMT  
		Size: 208.1 MB (208085910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c771c9bb4fd6100cefe1ac7b33e8e49ce3bbe8d93bc18f961ed3407cc7e83c`  
		Last Modified: Wed, 01 Apr 2026 20:06:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f20df3ab129314d8ce88530fadccfa3e914ba5cdda4b7d2fe406a0860509b8e`  
		Last Modified: Wed, 01 Apr 2026 20:06:15 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9ac4f42e04c2fb9132dfcd34ba8e63aeedccd9b6220a42b55080281ace3f86`  
		Last Modified: Wed, 01 Apr 2026 20:06:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b55806d8b1db79619afd1aa445b17a45e87d1ea6ad15ea2a7159dbb847c729`  
		Last Modified: Wed, 01 Apr 2026 20:06:16 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45561826e56e9196a428ea93727947135407e4c3e32bafe0e31c115cdb6002cf`  
		Last Modified: Wed, 01 Apr 2026 20:06:17 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.6.6-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:7898c25a1af9f318583a40f666e26bbb95a9a6d2c506108e6776039a333ce79d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8139abb2e57b413abf1bab2a428b6f42dfb6406ce0e2e5c5fc71daec28029b1`

```dockerfile
```

-	Layers:
	-	`sha256:d9c2de4925ec0f5d901e4e18513a86db55d04e29951d914bf9fa835131b2d03b`  
		Last Modified: Wed, 01 Apr 2026 20:06:14 GMT  
		Size: 25.4 KB (25406 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1.6.6-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:25c8c04ddb836b9063c7d63b21afd2dd058aae2817e9448741044685aaa4308d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228491258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a9a0615f81a6830c833d49ddd263ee61266e96c65e96f96a94d1d3eebebe723`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:35 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:35 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:35 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:35 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:35 GMT
ARG VERSION=26.1.6.6
# Wed, 01 Apr 2026 20:05:35 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:06:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:06:11 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:06:11 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:06:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:06:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:06:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:06:11 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:06:11 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:06:11 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:06:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ada8fdaeb998316b2548d1fc1b09087cc8000738d528d392d161a224cdb3797`  
		Last Modified: Wed, 01 Apr 2026 20:06:31 GMT  
		Size: 7.6 MB (7577433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c5eba9aefc3b25f55d620303971e46131e25b70049fbd0de58c47e5fa15350`  
		Last Modified: Wed, 01 Apr 2026 20:06:35 GMT  
		Size: 192.4 MB (192436835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0a36959eb8a87ed21ae6aef06322de0f477621655bdb871979d192d81a285b`  
		Last Modified: Wed, 01 Apr 2026 20:06:31 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:857f2a50cd1dbcd91b08f2c5df1df86bf01e2ef98b84a57f6ca73c2fe5068f1b`  
		Last Modified: Wed, 01 Apr 2026 20:06:31 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed81fdc7d0828b9daa83c0964f1f1c53470aa55346d398ba81af961b995fb564`  
		Last Modified: Wed, 01 Apr 2026 20:06:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6916b718c7c0811fd3570b9e1e97237a18f05d4b97facc9032f528de98fd2b6`  
		Last Modified: Wed, 01 Apr 2026 20:06:32 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890b8be52c1a68fbccbceaa8f973ac48811716d744dc7d294e5c9ba46734db3c`  
		Last Modified: Wed, 01 Apr 2026 20:06:34 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.6.6-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3a40f5f1f0ad9a2a97c80910bc984889921cae3a166925c4f0fd6af26fcfd1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02014b7969bad6ee8a9e8674a1c43937083bfaf85ab74bf3abbb811ffd94272f`

```dockerfile
```

-	Layers:
	-	`sha256:bbeabefee9e25dd54d6f8380cf6562c47f0cf6d121f9944d7898675a65c2ea8b`  
		Last Modified: Wed, 01 Apr 2026 20:06:31 GMT  
		Size: 25.6 KB (25595 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2`

```console
$ docker pull clickhouse@sha256:d3df4d7098d4a5650bf2ffb1a1408bc1425342df0094cbc01596a9501b388aff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2` - linux; amd64

```console
$ docker pull clickhouse@sha256:ea63c739b09b95a8d90b29f25426354215e1b07e6e98f6308d795ba305f2879f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 MB (253794379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc8ee1009de3ada8852cdcd46f6254a04f7dda0d91ac7a0e01aeec8f8cc0dfc2`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:38 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:38 GMT
ARG VERSION=26.2.5.45
# Wed, 01 Apr 2026 20:05:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:06:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:06:10 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:06:10 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:06:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:06:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:06:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:06:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:06:10 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:06:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:06:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3eabbc6107496a280043886f453df5eceb33ac7f2e14d288f464662ba538439`  
		Last Modified: Wed, 01 Apr 2026 20:06:33 GMT  
		Size: 7.6 MB (7598297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8fc49c988efd239ffb8ac89c2fde7fb971f08ea8fb2076038ffe87c61b985be`  
		Last Modified: Wed, 01 Apr 2026 20:06:42 GMT  
		Size: 215.6 MB (215589621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c777d79148d1de9927711cd62b491541472f1f074499fd19501d7165fe4b631`  
		Last Modified: Wed, 01 Apr 2026 20:06:33 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68670e33f930064a0b454e9e0dab8617febd320e8608d2ecce66b867e44fd146`  
		Last Modified: Wed, 01 Apr 2026 20:06:33 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6429b25036a2564c44f8224fe28776b80b5245064b3223445ace1bbc8b07c46`  
		Last Modified: Wed, 01 Apr 2026 20:06:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2cf3dd4a0a8b0328e10e741acc2833947f7b5d9d012c09496f530014b7d4f18`  
		Last Modified: Wed, 01 Apr 2026 20:06:35 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c1e3aa512ad7fc1864c7fcd59671914db2f15fe1487ff74284b0c065b0dce5`  
		Last Modified: Wed, 01 Apr 2026 20:06:35 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ad715097a25358655af64fbb391b231179d72b7cfd0dead7bf300efa20b2f5c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9236e337797a0c898178b2affec0418c0aa00dfa858e1c1b1d5e5b93921151f`

```dockerfile
```

-	Layers:
	-	`sha256:bfb43cf63463580bf743698bc946653acba9ff0c03794e4bb9f4dda1f4d38f1d`  
		Last Modified: Wed, 01 Apr 2026 20:06:33 GMT  
		Size: 25.4 KB (25418 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:c38cd9680ad7ef125c694543088d5ec62c32a873a8e3061d389caf5a86f20dc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.4 MB (237416609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:338f8c65b8be93d07b893993f32119313a494118b3ca4c3d89522a9ae253306c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:34 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:34 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:34 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:34 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:34 GMT
ARG VERSION=26.2.5.45
# Wed, 01 Apr 2026 20:05:34 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:06:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:06:04 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:06:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:06:04 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:06:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:06:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6b8526c1014d4afabbcbf93a359a21a5bdbf1f3e9da82df30d4cac3b38a090`  
		Last Modified: Wed, 01 Apr 2026 20:06:31 GMT  
		Size: 7.6 MB (7577440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d88b145795608f7eb95ba88ab3a74298d2b2af5e712eb2b56bede93de0d71f7`  
		Last Modified: Wed, 01 Apr 2026 20:06:31 GMT  
		Size: 201.4 MB (201362179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54370e74a6c297ea48114087bb043d22f9a8707a542dc8202e1f6d2cef570385`  
		Last Modified: Wed, 01 Apr 2026 20:06:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c8603370b11a223c2230a410d3d0c37cfa20ce1b3771b125e1f433949b98bd`  
		Last Modified: Wed, 01 Apr 2026 20:06:26 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5a0a67309f515d5a11f570805fedc9e58feb41d9b49723f2d7d5a22150d9bd`  
		Last Modified: Wed, 01 Apr 2026 20:06:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f517bc964c55e5026682beab4f5e04a5ae07ad7abef3033be3689ea38a52c3`  
		Last Modified: Wed, 01 Apr 2026 20:06:27 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9949ec1fe18126d6086f1a1e77a2b859323dad2ef3476ffc70e03c08b9a377`  
		Last Modified: Wed, 01 Apr 2026 20:06:29 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0067e8f689df819eeb4e43d73adfafd480774dac826f0cb1bb3af5ed946fd82d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28953af04ba974e321e1081c2f068c088347782e0cd98d0f57c68ef3b16b5d8`

```dockerfile
```

-	Layers:
	-	`sha256:31be783c2baceb2fe4558f3cf5fede49fe43671575c71576adeb7507ad114e70`  
		Last Modified: Wed, 01 Apr 2026 20:06:26 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2-jammy`

```console
$ docker pull clickhouse@sha256:d3df4d7098d4a5650bf2ffb1a1408bc1425342df0094cbc01596a9501b388aff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:ea63c739b09b95a8d90b29f25426354215e1b07e6e98f6308d795ba305f2879f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 MB (253794379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc8ee1009de3ada8852cdcd46f6254a04f7dda0d91ac7a0e01aeec8f8cc0dfc2`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:38 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:38 GMT
ARG VERSION=26.2.5.45
# Wed, 01 Apr 2026 20:05:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:06:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:06:10 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:06:10 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:06:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:06:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:06:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:06:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:06:10 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:06:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:06:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3eabbc6107496a280043886f453df5eceb33ac7f2e14d288f464662ba538439`  
		Last Modified: Wed, 01 Apr 2026 20:06:33 GMT  
		Size: 7.6 MB (7598297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8fc49c988efd239ffb8ac89c2fde7fb971f08ea8fb2076038ffe87c61b985be`  
		Last Modified: Wed, 01 Apr 2026 20:06:42 GMT  
		Size: 215.6 MB (215589621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c777d79148d1de9927711cd62b491541472f1f074499fd19501d7165fe4b631`  
		Last Modified: Wed, 01 Apr 2026 20:06:33 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68670e33f930064a0b454e9e0dab8617febd320e8608d2ecce66b867e44fd146`  
		Last Modified: Wed, 01 Apr 2026 20:06:33 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6429b25036a2564c44f8224fe28776b80b5245064b3223445ace1bbc8b07c46`  
		Last Modified: Wed, 01 Apr 2026 20:06:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2cf3dd4a0a8b0328e10e741acc2833947f7b5d9d012c09496f530014b7d4f18`  
		Last Modified: Wed, 01 Apr 2026 20:06:35 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c1e3aa512ad7fc1864c7fcd59671914db2f15fe1487ff74284b0c065b0dce5`  
		Last Modified: Wed, 01 Apr 2026 20:06:35 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ad715097a25358655af64fbb391b231179d72b7cfd0dead7bf300efa20b2f5c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9236e337797a0c898178b2affec0418c0aa00dfa858e1c1b1d5e5b93921151f`

```dockerfile
```

-	Layers:
	-	`sha256:bfb43cf63463580bf743698bc946653acba9ff0c03794e4bb9f4dda1f4d38f1d`  
		Last Modified: Wed, 01 Apr 2026 20:06:33 GMT  
		Size: 25.4 KB (25418 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:c38cd9680ad7ef125c694543088d5ec62c32a873a8e3061d389caf5a86f20dc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.4 MB (237416609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:338f8c65b8be93d07b893993f32119313a494118b3ca4c3d89522a9ae253306c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:34 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:34 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:34 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:34 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:34 GMT
ARG VERSION=26.2.5.45
# Wed, 01 Apr 2026 20:05:34 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:06:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:06:04 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:06:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:06:04 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:06:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:06:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6b8526c1014d4afabbcbf93a359a21a5bdbf1f3e9da82df30d4cac3b38a090`  
		Last Modified: Wed, 01 Apr 2026 20:06:31 GMT  
		Size: 7.6 MB (7577440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d88b145795608f7eb95ba88ab3a74298d2b2af5e712eb2b56bede93de0d71f7`  
		Last Modified: Wed, 01 Apr 2026 20:06:31 GMT  
		Size: 201.4 MB (201362179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54370e74a6c297ea48114087bb043d22f9a8707a542dc8202e1f6d2cef570385`  
		Last Modified: Wed, 01 Apr 2026 20:06:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c8603370b11a223c2230a410d3d0c37cfa20ce1b3771b125e1f433949b98bd`  
		Last Modified: Wed, 01 Apr 2026 20:06:26 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5a0a67309f515d5a11f570805fedc9e58feb41d9b49723f2d7d5a22150d9bd`  
		Last Modified: Wed, 01 Apr 2026 20:06:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f517bc964c55e5026682beab4f5e04a5ae07ad7abef3033be3689ea38a52c3`  
		Last Modified: Wed, 01 Apr 2026 20:06:27 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9949ec1fe18126d6086f1a1e77a2b859323dad2ef3476ffc70e03c08b9a377`  
		Last Modified: Wed, 01 Apr 2026 20:06:29 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0067e8f689df819eeb4e43d73adfafd480774dac826f0cb1bb3af5ed946fd82d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28953af04ba974e321e1081c2f068c088347782e0cd98d0f57c68ef3b16b5d8`

```dockerfile
```

-	Layers:
	-	`sha256:31be783c2baceb2fe4558f3cf5fede49fe43671575c71576adeb7507ad114e70`  
		Last Modified: Wed, 01 Apr 2026 20:06:26 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2.5`

```console
$ docker pull clickhouse@sha256:d3df4d7098d4a5650bf2ffb1a1408bc1425342df0094cbc01596a9501b388aff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2.5` - linux; amd64

```console
$ docker pull clickhouse@sha256:ea63c739b09b95a8d90b29f25426354215e1b07e6e98f6308d795ba305f2879f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 MB (253794379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc8ee1009de3ada8852cdcd46f6254a04f7dda0d91ac7a0e01aeec8f8cc0dfc2`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:38 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:38 GMT
ARG VERSION=26.2.5.45
# Wed, 01 Apr 2026 20:05:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:06:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:06:10 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:06:10 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:06:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:06:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:06:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:06:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:06:10 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:06:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:06:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3eabbc6107496a280043886f453df5eceb33ac7f2e14d288f464662ba538439`  
		Last Modified: Wed, 01 Apr 2026 20:06:33 GMT  
		Size: 7.6 MB (7598297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8fc49c988efd239ffb8ac89c2fde7fb971f08ea8fb2076038ffe87c61b985be`  
		Last Modified: Wed, 01 Apr 2026 20:06:42 GMT  
		Size: 215.6 MB (215589621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c777d79148d1de9927711cd62b491541472f1f074499fd19501d7165fe4b631`  
		Last Modified: Wed, 01 Apr 2026 20:06:33 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68670e33f930064a0b454e9e0dab8617febd320e8608d2ecce66b867e44fd146`  
		Last Modified: Wed, 01 Apr 2026 20:06:33 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6429b25036a2564c44f8224fe28776b80b5245064b3223445ace1bbc8b07c46`  
		Last Modified: Wed, 01 Apr 2026 20:06:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2cf3dd4a0a8b0328e10e741acc2833947f7b5d9d012c09496f530014b7d4f18`  
		Last Modified: Wed, 01 Apr 2026 20:06:35 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c1e3aa512ad7fc1864c7fcd59671914db2f15fe1487ff74284b0c065b0dce5`  
		Last Modified: Wed, 01 Apr 2026 20:06:35 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.5` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ad715097a25358655af64fbb391b231179d72b7cfd0dead7bf300efa20b2f5c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9236e337797a0c898178b2affec0418c0aa00dfa858e1c1b1d5e5b93921151f`

```dockerfile
```

-	Layers:
	-	`sha256:bfb43cf63463580bf743698bc946653acba9ff0c03794e4bb9f4dda1f4d38f1d`  
		Last Modified: Wed, 01 Apr 2026 20:06:33 GMT  
		Size: 25.4 KB (25418 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2.5` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:c38cd9680ad7ef125c694543088d5ec62c32a873a8e3061d389caf5a86f20dc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.4 MB (237416609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:338f8c65b8be93d07b893993f32119313a494118b3ca4c3d89522a9ae253306c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:34 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:34 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:34 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:34 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:34 GMT
ARG VERSION=26.2.5.45
# Wed, 01 Apr 2026 20:05:34 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:06:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:06:04 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:06:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:06:04 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:06:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:06:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6b8526c1014d4afabbcbf93a359a21a5bdbf1f3e9da82df30d4cac3b38a090`  
		Last Modified: Wed, 01 Apr 2026 20:06:31 GMT  
		Size: 7.6 MB (7577440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d88b145795608f7eb95ba88ab3a74298d2b2af5e712eb2b56bede93de0d71f7`  
		Last Modified: Wed, 01 Apr 2026 20:06:31 GMT  
		Size: 201.4 MB (201362179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54370e74a6c297ea48114087bb043d22f9a8707a542dc8202e1f6d2cef570385`  
		Last Modified: Wed, 01 Apr 2026 20:06:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c8603370b11a223c2230a410d3d0c37cfa20ce1b3771b125e1f433949b98bd`  
		Last Modified: Wed, 01 Apr 2026 20:06:26 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5a0a67309f515d5a11f570805fedc9e58feb41d9b49723f2d7d5a22150d9bd`  
		Last Modified: Wed, 01 Apr 2026 20:06:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f517bc964c55e5026682beab4f5e04a5ae07ad7abef3033be3689ea38a52c3`  
		Last Modified: Wed, 01 Apr 2026 20:06:27 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9949ec1fe18126d6086f1a1e77a2b859323dad2ef3476ffc70e03c08b9a377`  
		Last Modified: Wed, 01 Apr 2026 20:06:29 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.5` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0067e8f689df819eeb4e43d73adfafd480774dac826f0cb1bb3af5ed946fd82d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28953af04ba974e321e1081c2f068c088347782e0cd98d0f57c68ef3b16b5d8`

```dockerfile
```

-	Layers:
	-	`sha256:31be783c2baceb2fe4558f3cf5fede49fe43671575c71576adeb7507ad114e70`  
		Last Modified: Wed, 01 Apr 2026 20:06:26 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2.5-jammy`

```console
$ docker pull clickhouse@sha256:d3df4d7098d4a5650bf2ffb1a1408bc1425342df0094cbc01596a9501b388aff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2.5-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:ea63c739b09b95a8d90b29f25426354215e1b07e6e98f6308d795ba305f2879f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 MB (253794379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc8ee1009de3ada8852cdcd46f6254a04f7dda0d91ac7a0e01aeec8f8cc0dfc2`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:38 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:38 GMT
ARG VERSION=26.2.5.45
# Wed, 01 Apr 2026 20:05:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:06:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:06:10 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:06:10 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:06:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:06:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:06:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:06:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:06:10 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:06:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:06:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3eabbc6107496a280043886f453df5eceb33ac7f2e14d288f464662ba538439`  
		Last Modified: Wed, 01 Apr 2026 20:06:33 GMT  
		Size: 7.6 MB (7598297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8fc49c988efd239ffb8ac89c2fde7fb971f08ea8fb2076038ffe87c61b985be`  
		Last Modified: Wed, 01 Apr 2026 20:06:42 GMT  
		Size: 215.6 MB (215589621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c777d79148d1de9927711cd62b491541472f1f074499fd19501d7165fe4b631`  
		Last Modified: Wed, 01 Apr 2026 20:06:33 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68670e33f930064a0b454e9e0dab8617febd320e8608d2ecce66b867e44fd146`  
		Last Modified: Wed, 01 Apr 2026 20:06:33 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6429b25036a2564c44f8224fe28776b80b5245064b3223445ace1bbc8b07c46`  
		Last Modified: Wed, 01 Apr 2026 20:06:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2cf3dd4a0a8b0328e10e741acc2833947f7b5d9d012c09496f530014b7d4f18`  
		Last Modified: Wed, 01 Apr 2026 20:06:35 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c1e3aa512ad7fc1864c7fcd59671914db2f15fe1487ff74284b0c065b0dce5`  
		Last Modified: Wed, 01 Apr 2026 20:06:35 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.5-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ad715097a25358655af64fbb391b231179d72b7cfd0dead7bf300efa20b2f5c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9236e337797a0c898178b2affec0418c0aa00dfa858e1c1b1d5e5b93921151f`

```dockerfile
```

-	Layers:
	-	`sha256:bfb43cf63463580bf743698bc946653acba9ff0c03794e4bb9f4dda1f4d38f1d`  
		Last Modified: Wed, 01 Apr 2026 20:06:33 GMT  
		Size: 25.4 KB (25418 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2.5-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:c38cd9680ad7ef125c694543088d5ec62c32a873a8e3061d389caf5a86f20dc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.4 MB (237416609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:338f8c65b8be93d07b893993f32119313a494118b3ca4c3d89522a9ae253306c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:34 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:34 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:34 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:34 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:34 GMT
ARG VERSION=26.2.5.45
# Wed, 01 Apr 2026 20:05:34 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:06:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:06:04 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:06:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:06:04 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:06:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:06:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6b8526c1014d4afabbcbf93a359a21a5bdbf1f3e9da82df30d4cac3b38a090`  
		Last Modified: Wed, 01 Apr 2026 20:06:31 GMT  
		Size: 7.6 MB (7577440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d88b145795608f7eb95ba88ab3a74298d2b2af5e712eb2b56bede93de0d71f7`  
		Last Modified: Wed, 01 Apr 2026 20:06:31 GMT  
		Size: 201.4 MB (201362179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54370e74a6c297ea48114087bb043d22f9a8707a542dc8202e1f6d2cef570385`  
		Last Modified: Wed, 01 Apr 2026 20:06:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c8603370b11a223c2230a410d3d0c37cfa20ce1b3771b125e1f433949b98bd`  
		Last Modified: Wed, 01 Apr 2026 20:06:26 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5a0a67309f515d5a11f570805fedc9e58feb41d9b49723f2d7d5a22150d9bd`  
		Last Modified: Wed, 01 Apr 2026 20:06:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f517bc964c55e5026682beab4f5e04a5ae07ad7abef3033be3689ea38a52c3`  
		Last Modified: Wed, 01 Apr 2026 20:06:27 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9949ec1fe18126d6086f1a1e77a2b859323dad2ef3476ffc70e03c08b9a377`  
		Last Modified: Wed, 01 Apr 2026 20:06:29 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.5-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0067e8f689df819eeb4e43d73adfafd480774dac826f0cb1bb3af5ed946fd82d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28953af04ba974e321e1081c2f068c088347782e0cd98d0f57c68ef3b16b5d8`

```dockerfile
```

-	Layers:
	-	`sha256:31be783c2baceb2fe4558f3cf5fede49fe43671575c71576adeb7507ad114e70`  
		Last Modified: Wed, 01 Apr 2026 20:06:26 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2.5.45`

```console
$ docker pull clickhouse@sha256:d3df4d7098d4a5650bf2ffb1a1408bc1425342df0094cbc01596a9501b388aff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2.5.45` - linux; amd64

```console
$ docker pull clickhouse@sha256:ea63c739b09b95a8d90b29f25426354215e1b07e6e98f6308d795ba305f2879f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 MB (253794379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc8ee1009de3ada8852cdcd46f6254a04f7dda0d91ac7a0e01aeec8f8cc0dfc2`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:38 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:38 GMT
ARG VERSION=26.2.5.45
# Wed, 01 Apr 2026 20:05:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:06:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:06:10 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:06:10 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:06:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:06:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:06:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:06:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:06:10 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:06:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:06:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3eabbc6107496a280043886f453df5eceb33ac7f2e14d288f464662ba538439`  
		Last Modified: Wed, 01 Apr 2026 20:06:33 GMT  
		Size: 7.6 MB (7598297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8fc49c988efd239ffb8ac89c2fde7fb971f08ea8fb2076038ffe87c61b985be`  
		Last Modified: Wed, 01 Apr 2026 20:06:42 GMT  
		Size: 215.6 MB (215589621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c777d79148d1de9927711cd62b491541472f1f074499fd19501d7165fe4b631`  
		Last Modified: Wed, 01 Apr 2026 20:06:33 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68670e33f930064a0b454e9e0dab8617febd320e8608d2ecce66b867e44fd146`  
		Last Modified: Wed, 01 Apr 2026 20:06:33 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6429b25036a2564c44f8224fe28776b80b5245064b3223445ace1bbc8b07c46`  
		Last Modified: Wed, 01 Apr 2026 20:06:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2cf3dd4a0a8b0328e10e741acc2833947f7b5d9d012c09496f530014b7d4f18`  
		Last Modified: Wed, 01 Apr 2026 20:06:35 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c1e3aa512ad7fc1864c7fcd59671914db2f15fe1487ff74284b0c065b0dce5`  
		Last Modified: Wed, 01 Apr 2026 20:06:35 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.5.45` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ad715097a25358655af64fbb391b231179d72b7cfd0dead7bf300efa20b2f5c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9236e337797a0c898178b2affec0418c0aa00dfa858e1c1b1d5e5b93921151f`

```dockerfile
```

-	Layers:
	-	`sha256:bfb43cf63463580bf743698bc946653acba9ff0c03794e4bb9f4dda1f4d38f1d`  
		Last Modified: Wed, 01 Apr 2026 20:06:33 GMT  
		Size: 25.4 KB (25418 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2.5.45` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:c38cd9680ad7ef125c694543088d5ec62c32a873a8e3061d389caf5a86f20dc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.4 MB (237416609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:338f8c65b8be93d07b893993f32119313a494118b3ca4c3d89522a9ae253306c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:34 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:34 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:34 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:34 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:34 GMT
ARG VERSION=26.2.5.45
# Wed, 01 Apr 2026 20:05:34 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:06:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:06:04 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:06:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:06:04 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:06:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:06:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6b8526c1014d4afabbcbf93a359a21a5bdbf1f3e9da82df30d4cac3b38a090`  
		Last Modified: Wed, 01 Apr 2026 20:06:31 GMT  
		Size: 7.6 MB (7577440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d88b145795608f7eb95ba88ab3a74298d2b2af5e712eb2b56bede93de0d71f7`  
		Last Modified: Wed, 01 Apr 2026 20:06:31 GMT  
		Size: 201.4 MB (201362179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54370e74a6c297ea48114087bb043d22f9a8707a542dc8202e1f6d2cef570385`  
		Last Modified: Wed, 01 Apr 2026 20:06:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c8603370b11a223c2230a410d3d0c37cfa20ce1b3771b125e1f433949b98bd`  
		Last Modified: Wed, 01 Apr 2026 20:06:26 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5a0a67309f515d5a11f570805fedc9e58feb41d9b49723f2d7d5a22150d9bd`  
		Last Modified: Wed, 01 Apr 2026 20:06:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f517bc964c55e5026682beab4f5e04a5ae07ad7abef3033be3689ea38a52c3`  
		Last Modified: Wed, 01 Apr 2026 20:06:27 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9949ec1fe18126d6086f1a1e77a2b859323dad2ef3476ffc70e03c08b9a377`  
		Last Modified: Wed, 01 Apr 2026 20:06:29 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.5.45` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0067e8f689df819eeb4e43d73adfafd480774dac826f0cb1bb3af5ed946fd82d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28953af04ba974e321e1081c2f068c088347782e0cd98d0f57c68ef3b16b5d8`

```dockerfile
```

-	Layers:
	-	`sha256:31be783c2baceb2fe4558f3cf5fede49fe43671575c71576adeb7507ad114e70`  
		Last Modified: Wed, 01 Apr 2026 20:06:26 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2.5.45-jammy`

```console
$ docker pull clickhouse@sha256:d3df4d7098d4a5650bf2ffb1a1408bc1425342df0094cbc01596a9501b388aff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2.5.45-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:ea63c739b09b95a8d90b29f25426354215e1b07e6e98f6308d795ba305f2879f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 MB (253794379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc8ee1009de3ada8852cdcd46f6254a04f7dda0d91ac7a0e01aeec8f8cc0dfc2`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:38 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:38 GMT
ARG VERSION=26.2.5.45
# Wed, 01 Apr 2026 20:05:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:06:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:06:10 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:06:10 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:06:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:06:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:06:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:06:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:06:10 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:06:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:06:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3eabbc6107496a280043886f453df5eceb33ac7f2e14d288f464662ba538439`  
		Last Modified: Wed, 01 Apr 2026 20:06:33 GMT  
		Size: 7.6 MB (7598297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8fc49c988efd239ffb8ac89c2fde7fb971f08ea8fb2076038ffe87c61b985be`  
		Last Modified: Wed, 01 Apr 2026 20:06:42 GMT  
		Size: 215.6 MB (215589621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c777d79148d1de9927711cd62b491541472f1f074499fd19501d7165fe4b631`  
		Last Modified: Wed, 01 Apr 2026 20:06:33 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68670e33f930064a0b454e9e0dab8617febd320e8608d2ecce66b867e44fd146`  
		Last Modified: Wed, 01 Apr 2026 20:06:33 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6429b25036a2564c44f8224fe28776b80b5245064b3223445ace1bbc8b07c46`  
		Last Modified: Wed, 01 Apr 2026 20:06:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2cf3dd4a0a8b0328e10e741acc2833947f7b5d9d012c09496f530014b7d4f18`  
		Last Modified: Wed, 01 Apr 2026 20:06:35 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c1e3aa512ad7fc1864c7fcd59671914db2f15fe1487ff74284b0c065b0dce5`  
		Last Modified: Wed, 01 Apr 2026 20:06:35 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.5.45-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ad715097a25358655af64fbb391b231179d72b7cfd0dead7bf300efa20b2f5c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9236e337797a0c898178b2affec0418c0aa00dfa858e1c1b1d5e5b93921151f`

```dockerfile
```

-	Layers:
	-	`sha256:bfb43cf63463580bf743698bc946653acba9ff0c03794e4bb9f4dda1f4d38f1d`  
		Last Modified: Wed, 01 Apr 2026 20:06:33 GMT  
		Size: 25.4 KB (25418 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2.5.45-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:c38cd9680ad7ef125c694543088d5ec62c32a873a8e3061d389caf5a86f20dc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.4 MB (237416609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:338f8c65b8be93d07b893993f32119313a494118b3ca4c3d89522a9ae253306c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:34 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:34 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:34 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:34 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:34 GMT
ARG VERSION=26.2.5.45
# Wed, 01 Apr 2026 20:05:34 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:06:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:06:04 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:06:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:06:04 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:06:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:06:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6b8526c1014d4afabbcbf93a359a21a5bdbf1f3e9da82df30d4cac3b38a090`  
		Last Modified: Wed, 01 Apr 2026 20:06:31 GMT  
		Size: 7.6 MB (7577440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d88b145795608f7eb95ba88ab3a74298d2b2af5e712eb2b56bede93de0d71f7`  
		Last Modified: Wed, 01 Apr 2026 20:06:31 GMT  
		Size: 201.4 MB (201362179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54370e74a6c297ea48114087bb043d22f9a8707a542dc8202e1f6d2cef570385`  
		Last Modified: Wed, 01 Apr 2026 20:06:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c8603370b11a223c2230a410d3d0c37cfa20ce1b3771b125e1f433949b98bd`  
		Last Modified: Wed, 01 Apr 2026 20:06:26 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5a0a67309f515d5a11f570805fedc9e58feb41d9b49723f2d7d5a22150d9bd`  
		Last Modified: Wed, 01 Apr 2026 20:06:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f517bc964c55e5026682beab4f5e04a5ae07ad7abef3033be3689ea38a52c3`  
		Last Modified: Wed, 01 Apr 2026 20:06:27 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9949ec1fe18126d6086f1a1e77a2b859323dad2ef3476ffc70e03c08b9a377`  
		Last Modified: Wed, 01 Apr 2026 20:06:29 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.5.45-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0067e8f689df819eeb4e43d73adfafd480774dac826f0cb1bb3af5ed946fd82d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28953af04ba974e321e1081c2f068c088347782e0cd98d0f57c68ef3b16b5d8`

```dockerfile
```

-	Layers:
	-	`sha256:31be783c2baceb2fe4558f3cf5fede49fe43671575c71576adeb7507ad114e70`  
		Last Modified: Wed, 01 Apr 2026 20:06:26 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3`

```console
$ docker pull clickhouse@sha256:61a86a946f7e24107e1456651dc5da9154f2997722110aa83f0b847e174fde26
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:0fd0732bef5efc5999dfcf6356cc97beb21d76eeb92c3b91cb22b29b2a19b7a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.2 MB (262228036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41318e73cfbae6b1a89e7c6a9b3e64378ba9cc097b2092f348183cfd39299b15`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:27 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:27 GMT
ARG VERSION=26.3.1.896
# Wed, 01 Apr 2026 20:05:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:05:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:05:56 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:05:56 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:05:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:05:57 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:05:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:05:57 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:05:57 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:05:57 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:05:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534ad254b48275e47a53a047d04eac1b9ced7d8484e6358f8caa1876a7af4f77`  
		Last Modified: Wed, 01 Apr 2026 20:06:19 GMT  
		Size: 7.6 MB (7598315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47fd016e96bd289b13add3a240233fe68a1e1cc6691ef37542db855095a3c85`  
		Last Modified: Wed, 01 Apr 2026 20:06:25 GMT  
		Size: 224.0 MB (224023254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3acf289b9f31eb827cbc2b51b579cd5ea21b56735f0e735a5f5be59510752c4a`  
		Last Modified: Wed, 01 Apr 2026 20:06:24 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad5fa83c1077ae117a57fd36920e82f8cfe0458321eefb8a4f1307f5e6d2b84`  
		Last Modified: Wed, 01 Apr 2026 20:06:19 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d049147650bccf304c14b8108133d3e09e2a712232a823779a6c3e95ee00fc5d`  
		Last Modified: Wed, 01 Apr 2026 20:06:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cbd9b471e501348876c82ac4f9aa7c6f68ece17902c638cd736a34b4057a3c`  
		Last Modified: Wed, 01 Apr 2026 20:06:21 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45561826e56e9196a428ea93727947135407e4c3e32bafe0e31c115cdb6002cf`  
		Last Modified: Wed, 01 Apr 2026 20:06:17 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f1a3e9017fb0238f8dec720083a4c5354cd59f3389f8463ebde14de26fcbb24a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2728e55ad7a87bed0b0aed80f79112fb2ee20b8562187fff2d4d2cd54b28e82d`

```dockerfile
```

-	Layers:
	-	`sha256:72586ffb7c07af8397e8b35c6e1ecb529997218fd39db8b0211471a5f66eb048`  
		Last Modified: Wed, 01 Apr 2026 20:06:19 GMT  
		Size: 26.7 KB (26651 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:b049f1894852c6f88038c8672984754261cf2f265f3c9cddfbfa980ae1dc0166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244464397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd3e32e853c72ba0dbff4072a2b945852dedf837a2da6a84be74fe1fbc00e094`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:34 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:34 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:34 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:34 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:34 GMT
ARG VERSION=26.3.1.896
# Wed, 01 Apr 2026 20:05:34 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:06:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:06:04 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:06:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:06:04 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:06:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:06:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c91c9bb03f5c1be062449acdf2e31b868f28566ebdf3d2dc66e522880010a2`  
		Last Modified: Wed, 01 Apr 2026 20:06:27 GMT  
		Size: 7.6 MB (7577453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460842314d3242e865bc24647f0e2ba5f5fb6c279a11d4f56634d75925f72104`  
		Last Modified: Wed, 01 Apr 2026 20:06:30 GMT  
		Size: 208.4 MB (208409957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54370e74a6c297ea48114087bb043d22f9a8707a542dc8202e1f6d2cef570385`  
		Last Modified: Wed, 01 Apr 2026 20:06:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c8603370b11a223c2230a410d3d0c37cfa20ce1b3771b125e1f433949b98bd`  
		Last Modified: Wed, 01 Apr 2026 20:06:26 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5a0a67309f515d5a11f570805fedc9e58feb41d9b49723f2d7d5a22150d9bd`  
		Last Modified: Wed, 01 Apr 2026 20:06:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a48ac8a84f790732886aa96d0d703decf93fd80706f8385f80d90fb5bd7d68`  
		Last Modified: Wed, 01 Apr 2026 20:06:28 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204362d0086811f274a089d895ec551087a54bb78adee7efe7025904f946b562`  
		Last Modified: Wed, 01 Apr 2026 20:06:28 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4179cae6a9b44859cc8bed139f805476637f01dad9267dc9ed962f8a9960fb50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b18502d1ffb802e9a7265897e5df2ffa8e6b67287f7dfb8049352b875a47515a`

```dockerfile
```

-	Layers:
	-	`sha256:b51f0249c540ffed3fda88182372c2ede4549bd4e79ceca3324f30c8a0974ea0`  
		Last Modified: Wed, 01 Apr 2026 20:06:26 GMT  
		Size: 26.9 KB (26887 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3-jammy`

```console
$ docker pull clickhouse@sha256:61a86a946f7e24107e1456651dc5da9154f2997722110aa83f0b847e174fde26
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:0fd0732bef5efc5999dfcf6356cc97beb21d76eeb92c3b91cb22b29b2a19b7a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.2 MB (262228036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41318e73cfbae6b1a89e7c6a9b3e64378ba9cc097b2092f348183cfd39299b15`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:27 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:27 GMT
ARG VERSION=26.3.1.896
# Wed, 01 Apr 2026 20:05:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:05:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:05:56 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:05:56 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:05:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:05:57 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:05:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:05:57 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:05:57 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:05:57 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:05:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534ad254b48275e47a53a047d04eac1b9ced7d8484e6358f8caa1876a7af4f77`  
		Last Modified: Wed, 01 Apr 2026 20:06:19 GMT  
		Size: 7.6 MB (7598315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47fd016e96bd289b13add3a240233fe68a1e1cc6691ef37542db855095a3c85`  
		Last Modified: Wed, 01 Apr 2026 20:06:25 GMT  
		Size: 224.0 MB (224023254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3acf289b9f31eb827cbc2b51b579cd5ea21b56735f0e735a5f5be59510752c4a`  
		Last Modified: Wed, 01 Apr 2026 20:06:24 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad5fa83c1077ae117a57fd36920e82f8cfe0458321eefb8a4f1307f5e6d2b84`  
		Last Modified: Wed, 01 Apr 2026 20:06:19 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d049147650bccf304c14b8108133d3e09e2a712232a823779a6c3e95ee00fc5d`  
		Last Modified: Wed, 01 Apr 2026 20:06:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cbd9b471e501348876c82ac4f9aa7c6f68ece17902c638cd736a34b4057a3c`  
		Last Modified: Wed, 01 Apr 2026 20:06:21 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45561826e56e9196a428ea93727947135407e4c3e32bafe0e31c115cdb6002cf`  
		Last Modified: Wed, 01 Apr 2026 20:06:17 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f1a3e9017fb0238f8dec720083a4c5354cd59f3389f8463ebde14de26fcbb24a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2728e55ad7a87bed0b0aed80f79112fb2ee20b8562187fff2d4d2cd54b28e82d`

```dockerfile
```

-	Layers:
	-	`sha256:72586ffb7c07af8397e8b35c6e1ecb529997218fd39db8b0211471a5f66eb048`  
		Last Modified: Wed, 01 Apr 2026 20:06:19 GMT  
		Size: 26.7 KB (26651 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:b049f1894852c6f88038c8672984754261cf2f265f3c9cddfbfa980ae1dc0166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244464397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd3e32e853c72ba0dbff4072a2b945852dedf837a2da6a84be74fe1fbc00e094`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:34 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:34 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:34 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:34 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:34 GMT
ARG VERSION=26.3.1.896
# Wed, 01 Apr 2026 20:05:34 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:06:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:06:04 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:06:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:06:04 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:06:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:06:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c91c9bb03f5c1be062449acdf2e31b868f28566ebdf3d2dc66e522880010a2`  
		Last Modified: Wed, 01 Apr 2026 20:06:27 GMT  
		Size: 7.6 MB (7577453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460842314d3242e865bc24647f0e2ba5f5fb6c279a11d4f56634d75925f72104`  
		Last Modified: Wed, 01 Apr 2026 20:06:30 GMT  
		Size: 208.4 MB (208409957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54370e74a6c297ea48114087bb043d22f9a8707a542dc8202e1f6d2cef570385`  
		Last Modified: Wed, 01 Apr 2026 20:06:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c8603370b11a223c2230a410d3d0c37cfa20ce1b3771b125e1f433949b98bd`  
		Last Modified: Wed, 01 Apr 2026 20:06:26 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5a0a67309f515d5a11f570805fedc9e58feb41d9b49723f2d7d5a22150d9bd`  
		Last Modified: Wed, 01 Apr 2026 20:06:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a48ac8a84f790732886aa96d0d703decf93fd80706f8385f80d90fb5bd7d68`  
		Last Modified: Wed, 01 Apr 2026 20:06:28 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204362d0086811f274a089d895ec551087a54bb78adee7efe7025904f946b562`  
		Last Modified: Wed, 01 Apr 2026 20:06:28 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4179cae6a9b44859cc8bed139f805476637f01dad9267dc9ed962f8a9960fb50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b18502d1ffb802e9a7265897e5df2ffa8e6b67287f7dfb8049352b875a47515a`

```dockerfile
```

-	Layers:
	-	`sha256:b51f0249c540ffed3fda88182372c2ede4549bd4e79ceca3324f30c8a0974ea0`  
		Last Modified: Wed, 01 Apr 2026 20:06:26 GMT  
		Size: 26.9 KB (26887 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3.1`

```console
$ docker pull clickhouse@sha256:61a86a946f7e24107e1456651dc5da9154f2997722110aa83f0b847e174fde26
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3.1` - linux; amd64

```console
$ docker pull clickhouse@sha256:0fd0732bef5efc5999dfcf6356cc97beb21d76eeb92c3b91cb22b29b2a19b7a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.2 MB (262228036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41318e73cfbae6b1a89e7c6a9b3e64378ba9cc097b2092f348183cfd39299b15`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:27 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:27 GMT
ARG VERSION=26.3.1.896
# Wed, 01 Apr 2026 20:05:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:05:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:05:56 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:05:56 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:05:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:05:57 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:05:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:05:57 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:05:57 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:05:57 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:05:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534ad254b48275e47a53a047d04eac1b9ced7d8484e6358f8caa1876a7af4f77`  
		Last Modified: Wed, 01 Apr 2026 20:06:19 GMT  
		Size: 7.6 MB (7598315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47fd016e96bd289b13add3a240233fe68a1e1cc6691ef37542db855095a3c85`  
		Last Modified: Wed, 01 Apr 2026 20:06:25 GMT  
		Size: 224.0 MB (224023254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3acf289b9f31eb827cbc2b51b579cd5ea21b56735f0e735a5f5be59510752c4a`  
		Last Modified: Wed, 01 Apr 2026 20:06:24 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad5fa83c1077ae117a57fd36920e82f8cfe0458321eefb8a4f1307f5e6d2b84`  
		Last Modified: Wed, 01 Apr 2026 20:06:19 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d049147650bccf304c14b8108133d3e09e2a712232a823779a6c3e95ee00fc5d`  
		Last Modified: Wed, 01 Apr 2026 20:06:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cbd9b471e501348876c82ac4f9aa7c6f68ece17902c638cd736a34b4057a3c`  
		Last Modified: Wed, 01 Apr 2026 20:06:21 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45561826e56e9196a428ea93727947135407e4c3e32bafe0e31c115cdb6002cf`  
		Last Modified: Wed, 01 Apr 2026 20:06:17 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.1` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f1a3e9017fb0238f8dec720083a4c5354cd59f3389f8463ebde14de26fcbb24a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2728e55ad7a87bed0b0aed80f79112fb2ee20b8562187fff2d4d2cd54b28e82d`

```dockerfile
```

-	Layers:
	-	`sha256:72586ffb7c07af8397e8b35c6e1ecb529997218fd39db8b0211471a5f66eb048`  
		Last Modified: Wed, 01 Apr 2026 20:06:19 GMT  
		Size: 26.7 KB (26651 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3.1` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:b049f1894852c6f88038c8672984754261cf2f265f3c9cddfbfa980ae1dc0166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244464397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd3e32e853c72ba0dbff4072a2b945852dedf837a2da6a84be74fe1fbc00e094`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:34 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:34 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:34 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:34 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:34 GMT
ARG VERSION=26.3.1.896
# Wed, 01 Apr 2026 20:05:34 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:06:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:06:04 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:06:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:06:04 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:06:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:06:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c91c9bb03f5c1be062449acdf2e31b868f28566ebdf3d2dc66e522880010a2`  
		Last Modified: Wed, 01 Apr 2026 20:06:27 GMT  
		Size: 7.6 MB (7577453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460842314d3242e865bc24647f0e2ba5f5fb6c279a11d4f56634d75925f72104`  
		Last Modified: Wed, 01 Apr 2026 20:06:30 GMT  
		Size: 208.4 MB (208409957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54370e74a6c297ea48114087bb043d22f9a8707a542dc8202e1f6d2cef570385`  
		Last Modified: Wed, 01 Apr 2026 20:06:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c8603370b11a223c2230a410d3d0c37cfa20ce1b3771b125e1f433949b98bd`  
		Last Modified: Wed, 01 Apr 2026 20:06:26 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5a0a67309f515d5a11f570805fedc9e58feb41d9b49723f2d7d5a22150d9bd`  
		Last Modified: Wed, 01 Apr 2026 20:06:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a48ac8a84f790732886aa96d0d703decf93fd80706f8385f80d90fb5bd7d68`  
		Last Modified: Wed, 01 Apr 2026 20:06:28 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204362d0086811f274a089d895ec551087a54bb78adee7efe7025904f946b562`  
		Last Modified: Wed, 01 Apr 2026 20:06:28 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.1` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4179cae6a9b44859cc8bed139f805476637f01dad9267dc9ed962f8a9960fb50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b18502d1ffb802e9a7265897e5df2ffa8e6b67287f7dfb8049352b875a47515a`

```dockerfile
```

-	Layers:
	-	`sha256:b51f0249c540ffed3fda88182372c2ede4549bd4e79ceca3324f30c8a0974ea0`  
		Last Modified: Wed, 01 Apr 2026 20:06:26 GMT  
		Size: 26.9 KB (26887 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3.1-jammy`

```console
$ docker pull clickhouse@sha256:61a86a946f7e24107e1456651dc5da9154f2997722110aa83f0b847e174fde26
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3.1-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:0fd0732bef5efc5999dfcf6356cc97beb21d76eeb92c3b91cb22b29b2a19b7a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.2 MB (262228036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41318e73cfbae6b1a89e7c6a9b3e64378ba9cc097b2092f348183cfd39299b15`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:27 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:27 GMT
ARG VERSION=26.3.1.896
# Wed, 01 Apr 2026 20:05:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:05:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:05:56 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:05:56 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:05:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:05:57 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:05:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:05:57 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:05:57 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:05:57 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:05:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534ad254b48275e47a53a047d04eac1b9ced7d8484e6358f8caa1876a7af4f77`  
		Last Modified: Wed, 01 Apr 2026 20:06:19 GMT  
		Size: 7.6 MB (7598315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47fd016e96bd289b13add3a240233fe68a1e1cc6691ef37542db855095a3c85`  
		Last Modified: Wed, 01 Apr 2026 20:06:25 GMT  
		Size: 224.0 MB (224023254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3acf289b9f31eb827cbc2b51b579cd5ea21b56735f0e735a5f5be59510752c4a`  
		Last Modified: Wed, 01 Apr 2026 20:06:24 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad5fa83c1077ae117a57fd36920e82f8cfe0458321eefb8a4f1307f5e6d2b84`  
		Last Modified: Wed, 01 Apr 2026 20:06:19 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d049147650bccf304c14b8108133d3e09e2a712232a823779a6c3e95ee00fc5d`  
		Last Modified: Wed, 01 Apr 2026 20:06:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cbd9b471e501348876c82ac4f9aa7c6f68ece17902c638cd736a34b4057a3c`  
		Last Modified: Wed, 01 Apr 2026 20:06:21 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45561826e56e9196a428ea93727947135407e4c3e32bafe0e31c115cdb6002cf`  
		Last Modified: Wed, 01 Apr 2026 20:06:17 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.1-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f1a3e9017fb0238f8dec720083a4c5354cd59f3389f8463ebde14de26fcbb24a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2728e55ad7a87bed0b0aed80f79112fb2ee20b8562187fff2d4d2cd54b28e82d`

```dockerfile
```

-	Layers:
	-	`sha256:72586ffb7c07af8397e8b35c6e1ecb529997218fd39db8b0211471a5f66eb048`  
		Last Modified: Wed, 01 Apr 2026 20:06:19 GMT  
		Size: 26.7 KB (26651 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3.1-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:b049f1894852c6f88038c8672984754261cf2f265f3c9cddfbfa980ae1dc0166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244464397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd3e32e853c72ba0dbff4072a2b945852dedf837a2da6a84be74fe1fbc00e094`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:34 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:34 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:34 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:34 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:34 GMT
ARG VERSION=26.3.1.896
# Wed, 01 Apr 2026 20:05:34 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:06:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:06:04 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:06:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:06:04 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:06:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:06:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c91c9bb03f5c1be062449acdf2e31b868f28566ebdf3d2dc66e522880010a2`  
		Last Modified: Wed, 01 Apr 2026 20:06:27 GMT  
		Size: 7.6 MB (7577453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460842314d3242e865bc24647f0e2ba5f5fb6c279a11d4f56634d75925f72104`  
		Last Modified: Wed, 01 Apr 2026 20:06:30 GMT  
		Size: 208.4 MB (208409957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54370e74a6c297ea48114087bb043d22f9a8707a542dc8202e1f6d2cef570385`  
		Last Modified: Wed, 01 Apr 2026 20:06:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c8603370b11a223c2230a410d3d0c37cfa20ce1b3771b125e1f433949b98bd`  
		Last Modified: Wed, 01 Apr 2026 20:06:26 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5a0a67309f515d5a11f570805fedc9e58feb41d9b49723f2d7d5a22150d9bd`  
		Last Modified: Wed, 01 Apr 2026 20:06:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a48ac8a84f790732886aa96d0d703decf93fd80706f8385f80d90fb5bd7d68`  
		Last Modified: Wed, 01 Apr 2026 20:06:28 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204362d0086811f274a089d895ec551087a54bb78adee7efe7025904f946b562`  
		Last Modified: Wed, 01 Apr 2026 20:06:28 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.1-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4179cae6a9b44859cc8bed139f805476637f01dad9267dc9ed962f8a9960fb50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b18502d1ffb802e9a7265897e5df2ffa8e6b67287f7dfb8049352b875a47515a`

```dockerfile
```

-	Layers:
	-	`sha256:b51f0249c540ffed3fda88182372c2ede4549bd4e79ceca3324f30c8a0974ea0`  
		Last Modified: Wed, 01 Apr 2026 20:06:26 GMT  
		Size: 26.9 KB (26887 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3.1.896`

```console
$ docker pull clickhouse@sha256:61a86a946f7e24107e1456651dc5da9154f2997722110aa83f0b847e174fde26
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3.1.896` - linux; amd64

```console
$ docker pull clickhouse@sha256:0fd0732bef5efc5999dfcf6356cc97beb21d76eeb92c3b91cb22b29b2a19b7a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.2 MB (262228036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41318e73cfbae6b1a89e7c6a9b3e64378ba9cc097b2092f348183cfd39299b15`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:27 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:27 GMT
ARG VERSION=26.3.1.896
# Wed, 01 Apr 2026 20:05:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:05:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:05:56 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:05:56 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:05:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:05:57 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:05:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:05:57 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:05:57 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:05:57 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:05:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534ad254b48275e47a53a047d04eac1b9ced7d8484e6358f8caa1876a7af4f77`  
		Last Modified: Wed, 01 Apr 2026 20:06:19 GMT  
		Size: 7.6 MB (7598315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47fd016e96bd289b13add3a240233fe68a1e1cc6691ef37542db855095a3c85`  
		Last Modified: Wed, 01 Apr 2026 20:06:25 GMT  
		Size: 224.0 MB (224023254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3acf289b9f31eb827cbc2b51b579cd5ea21b56735f0e735a5f5be59510752c4a`  
		Last Modified: Wed, 01 Apr 2026 20:06:24 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad5fa83c1077ae117a57fd36920e82f8cfe0458321eefb8a4f1307f5e6d2b84`  
		Last Modified: Wed, 01 Apr 2026 20:06:19 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d049147650bccf304c14b8108133d3e09e2a712232a823779a6c3e95ee00fc5d`  
		Last Modified: Wed, 01 Apr 2026 20:06:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cbd9b471e501348876c82ac4f9aa7c6f68ece17902c638cd736a34b4057a3c`  
		Last Modified: Wed, 01 Apr 2026 20:06:21 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45561826e56e9196a428ea93727947135407e4c3e32bafe0e31c115cdb6002cf`  
		Last Modified: Wed, 01 Apr 2026 20:06:17 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.1.896` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f1a3e9017fb0238f8dec720083a4c5354cd59f3389f8463ebde14de26fcbb24a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2728e55ad7a87bed0b0aed80f79112fb2ee20b8562187fff2d4d2cd54b28e82d`

```dockerfile
```

-	Layers:
	-	`sha256:72586ffb7c07af8397e8b35c6e1ecb529997218fd39db8b0211471a5f66eb048`  
		Last Modified: Wed, 01 Apr 2026 20:06:19 GMT  
		Size: 26.7 KB (26651 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3.1.896` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:b049f1894852c6f88038c8672984754261cf2f265f3c9cddfbfa980ae1dc0166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244464397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd3e32e853c72ba0dbff4072a2b945852dedf837a2da6a84be74fe1fbc00e094`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:34 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:34 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:34 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:34 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:34 GMT
ARG VERSION=26.3.1.896
# Wed, 01 Apr 2026 20:05:34 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:06:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:06:04 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:06:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:06:04 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:06:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:06:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c91c9bb03f5c1be062449acdf2e31b868f28566ebdf3d2dc66e522880010a2`  
		Last Modified: Wed, 01 Apr 2026 20:06:27 GMT  
		Size: 7.6 MB (7577453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460842314d3242e865bc24647f0e2ba5f5fb6c279a11d4f56634d75925f72104`  
		Last Modified: Wed, 01 Apr 2026 20:06:30 GMT  
		Size: 208.4 MB (208409957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54370e74a6c297ea48114087bb043d22f9a8707a542dc8202e1f6d2cef570385`  
		Last Modified: Wed, 01 Apr 2026 20:06:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c8603370b11a223c2230a410d3d0c37cfa20ce1b3771b125e1f433949b98bd`  
		Last Modified: Wed, 01 Apr 2026 20:06:26 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5a0a67309f515d5a11f570805fedc9e58feb41d9b49723f2d7d5a22150d9bd`  
		Last Modified: Wed, 01 Apr 2026 20:06:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a48ac8a84f790732886aa96d0d703decf93fd80706f8385f80d90fb5bd7d68`  
		Last Modified: Wed, 01 Apr 2026 20:06:28 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204362d0086811f274a089d895ec551087a54bb78adee7efe7025904f946b562`  
		Last Modified: Wed, 01 Apr 2026 20:06:28 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.1.896` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4179cae6a9b44859cc8bed139f805476637f01dad9267dc9ed962f8a9960fb50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b18502d1ffb802e9a7265897e5df2ffa8e6b67287f7dfb8049352b875a47515a`

```dockerfile
```

-	Layers:
	-	`sha256:b51f0249c540ffed3fda88182372c2ede4549bd4e79ceca3324f30c8a0974ea0`  
		Last Modified: Wed, 01 Apr 2026 20:06:26 GMT  
		Size: 26.9 KB (26887 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3.1.896-jammy`

```console
$ docker pull clickhouse@sha256:61a86a946f7e24107e1456651dc5da9154f2997722110aa83f0b847e174fde26
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3.1.896-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:0fd0732bef5efc5999dfcf6356cc97beb21d76eeb92c3b91cb22b29b2a19b7a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.2 MB (262228036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41318e73cfbae6b1a89e7c6a9b3e64378ba9cc097b2092f348183cfd39299b15`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:27 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:27 GMT
ARG VERSION=26.3.1.896
# Wed, 01 Apr 2026 20:05:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:05:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:05:56 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:05:56 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:05:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:05:57 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:05:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:05:57 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:05:57 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:05:57 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:05:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534ad254b48275e47a53a047d04eac1b9ced7d8484e6358f8caa1876a7af4f77`  
		Last Modified: Wed, 01 Apr 2026 20:06:19 GMT  
		Size: 7.6 MB (7598315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47fd016e96bd289b13add3a240233fe68a1e1cc6691ef37542db855095a3c85`  
		Last Modified: Wed, 01 Apr 2026 20:06:25 GMT  
		Size: 224.0 MB (224023254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3acf289b9f31eb827cbc2b51b579cd5ea21b56735f0e735a5f5be59510752c4a`  
		Last Modified: Wed, 01 Apr 2026 20:06:24 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad5fa83c1077ae117a57fd36920e82f8cfe0458321eefb8a4f1307f5e6d2b84`  
		Last Modified: Wed, 01 Apr 2026 20:06:19 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d049147650bccf304c14b8108133d3e09e2a712232a823779a6c3e95ee00fc5d`  
		Last Modified: Wed, 01 Apr 2026 20:06:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cbd9b471e501348876c82ac4f9aa7c6f68ece17902c638cd736a34b4057a3c`  
		Last Modified: Wed, 01 Apr 2026 20:06:21 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45561826e56e9196a428ea93727947135407e4c3e32bafe0e31c115cdb6002cf`  
		Last Modified: Wed, 01 Apr 2026 20:06:17 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.1.896-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f1a3e9017fb0238f8dec720083a4c5354cd59f3389f8463ebde14de26fcbb24a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2728e55ad7a87bed0b0aed80f79112fb2ee20b8562187fff2d4d2cd54b28e82d`

```dockerfile
```

-	Layers:
	-	`sha256:72586ffb7c07af8397e8b35c6e1ecb529997218fd39db8b0211471a5f66eb048`  
		Last Modified: Wed, 01 Apr 2026 20:06:19 GMT  
		Size: 26.7 KB (26651 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3.1.896-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:b049f1894852c6f88038c8672984754261cf2f265f3c9cddfbfa980ae1dc0166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244464397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd3e32e853c72ba0dbff4072a2b945852dedf837a2da6a84be74fe1fbc00e094`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:34 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:34 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:34 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:34 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:34 GMT
ARG VERSION=26.3.1.896
# Wed, 01 Apr 2026 20:05:34 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:06:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:06:04 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:06:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:06:04 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:06:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:06:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c91c9bb03f5c1be062449acdf2e31b868f28566ebdf3d2dc66e522880010a2`  
		Last Modified: Wed, 01 Apr 2026 20:06:27 GMT  
		Size: 7.6 MB (7577453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460842314d3242e865bc24647f0e2ba5f5fb6c279a11d4f56634d75925f72104`  
		Last Modified: Wed, 01 Apr 2026 20:06:30 GMT  
		Size: 208.4 MB (208409957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54370e74a6c297ea48114087bb043d22f9a8707a542dc8202e1f6d2cef570385`  
		Last Modified: Wed, 01 Apr 2026 20:06:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c8603370b11a223c2230a410d3d0c37cfa20ce1b3771b125e1f433949b98bd`  
		Last Modified: Wed, 01 Apr 2026 20:06:26 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5a0a67309f515d5a11f570805fedc9e58feb41d9b49723f2d7d5a22150d9bd`  
		Last Modified: Wed, 01 Apr 2026 20:06:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a48ac8a84f790732886aa96d0d703decf93fd80706f8385f80d90fb5bd7d68`  
		Last Modified: Wed, 01 Apr 2026 20:06:28 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204362d0086811f274a089d895ec551087a54bb78adee7efe7025904f946b562`  
		Last Modified: Wed, 01 Apr 2026 20:06:28 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.1.896-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4179cae6a9b44859cc8bed139f805476637f01dad9267dc9ed962f8a9960fb50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b18502d1ffb802e9a7265897e5df2ffa8e6b67287f7dfb8049352b875a47515a`

```dockerfile
```

-	Layers:
	-	`sha256:b51f0249c540ffed3fda88182372c2ede4549bd4e79ceca3324f30c8a0974ea0`  
		Last Modified: Wed, 01 Apr 2026 20:06:26 GMT  
		Size: 26.9 KB (26887 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:jammy`

```console
$ docker pull clickhouse@sha256:61a86a946f7e24107e1456651dc5da9154f2997722110aa83f0b847e174fde26
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:0fd0732bef5efc5999dfcf6356cc97beb21d76eeb92c3b91cb22b29b2a19b7a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.2 MB (262228036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41318e73cfbae6b1a89e7c6a9b3e64378ba9cc097b2092f348183cfd39299b15`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:27 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:27 GMT
ARG VERSION=26.3.1.896
# Wed, 01 Apr 2026 20:05:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:05:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:05:56 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:05:56 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:05:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:05:57 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:05:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:05:57 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:05:57 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:05:57 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:05:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534ad254b48275e47a53a047d04eac1b9ced7d8484e6358f8caa1876a7af4f77`  
		Last Modified: Wed, 01 Apr 2026 20:06:19 GMT  
		Size: 7.6 MB (7598315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47fd016e96bd289b13add3a240233fe68a1e1cc6691ef37542db855095a3c85`  
		Last Modified: Wed, 01 Apr 2026 20:06:25 GMT  
		Size: 224.0 MB (224023254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3acf289b9f31eb827cbc2b51b579cd5ea21b56735f0e735a5f5be59510752c4a`  
		Last Modified: Wed, 01 Apr 2026 20:06:24 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad5fa83c1077ae117a57fd36920e82f8cfe0458321eefb8a4f1307f5e6d2b84`  
		Last Modified: Wed, 01 Apr 2026 20:06:19 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d049147650bccf304c14b8108133d3e09e2a712232a823779a6c3e95ee00fc5d`  
		Last Modified: Wed, 01 Apr 2026 20:06:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cbd9b471e501348876c82ac4f9aa7c6f68ece17902c638cd736a34b4057a3c`  
		Last Modified: Wed, 01 Apr 2026 20:06:21 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45561826e56e9196a428ea93727947135407e4c3e32bafe0e31c115cdb6002cf`  
		Last Modified: Wed, 01 Apr 2026 20:06:17 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f1a3e9017fb0238f8dec720083a4c5354cd59f3389f8463ebde14de26fcbb24a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2728e55ad7a87bed0b0aed80f79112fb2ee20b8562187fff2d4d2cd54b28e82d`

```dockerfile
```

-	Layers:
	-	`sha256:72586ffb7c07af8397e8b35c6e1ecb529997218fd39db8b0211471a5f66eb048`  
		Last Modified: Wed, 01 Apr 2026 20:06:19 GMT  
		Size: 26.7 KB (26651 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:b049f1894852c6f88038c8672984754261cf2f265f3c9cddfbfa980ae1dc0166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244464397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd3e32e853c72ba0dbff4072a2b945852dedf837a2da6a84be74fe1fbc00e094`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:34 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:34 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:34 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:34 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:34 GMT
ARG VERSION=26.3.1.896
# Wed, 01 Apr 2026 20:05:34 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:06:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:06:04 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:06:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:06:04 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:06:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:06:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c91c9bb03f5c1be062449acdf2e31b868f28566ebdf3d2dc66e522880010a2`  
		Last Modified: Wed, 01 Apr 2026 20:06:27 GMT  
		Size: 7.6 MB (7577453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460842314d3242e865bc24647f0e2ba5f5fb6c279a11d4f56634d75925f72104`  
		Last Modified: Wed, 01 Apr 2026 20:06:30 GMT  
		Size: 208.4 MB (208409957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54370e74a6c297ea48114087bb043d22f9a8707a542dc8202e1f6d2cef570385`  
		Last Modified: Wed, 01 Apr 2026 20:06:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c8603370b11a223c2230a410d3d0c37cfa20ce1b3771b125e1f433949b98bd`  
		Last Modified: Wed, 01 Apr 2026 20:06:26 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5a0a67309f515d5a11f570805fedc9e58feb41d9b49723f2d7d5a22150d9bd`  
		Last Modified: Wed, 01 Apr 2026 20:06:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a48ac8a84f790732886aa96d0d703decf93fd80706f8385f80d90fb5bd7d68`  
		Last Modified: Wed, 01 Apr 2026 20:06:28 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204362d0086811f274a089d895ec551087a54bb78adee7efe7025904f946b562`  
		Last Modified: Wed, 01 Apr 2026 20:06:28 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4179cae6a9b44859cc8bed139f805476637f01dad9267dc9ed962f8a9960fb50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b18502d1ffb802e9a7265897e5df2ffa8e6b67287f7dfb8049352b875a47515a`

```dockerfile
```

-	Layers:
	-	`sha256:b51f0249c540ffed3fda88182372c2ede4549bd4e79ceca3324f30c8a0974ea0`  
		Last Modified: Wed, 01 Apr 2026 20:06:26 GMT  
		Size: 26.9 KB (26887 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:61a86a946f7e24107e1456651dc5da9154f2997722110aa83f0b847e174fde26
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

```console
$ docker pull clickhouse@sha256:0fd0732bef5efc5999dfcf6356cc97beb21d76eeb92c3b91cb22b29b2a19b7a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.2 MB (262228036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41318e73cfbae6b1a89e7c6a9b3e64378ba9cc097b2092f348183cfd39299b15`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:27 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:27 GMT
ARG VERSION=26.3.1.896
# Wed, 01 Apr 2026 20:05:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:05:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:05:56 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:05:56 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:05:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:05:57 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:05:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:05:57 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:05:57 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:05:57 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:05:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534ad254b48275e47a53a047d04eac1b9ced7d8484e6358f8caa1876a7af4f77`  
		Last Modified: Wed, 01 Apr 2026 20:06:19 GMT  
		Size: 7.6 MB (7598315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47fd016e96bd289b13add3a240233fe68a1e1cc6691ef37542db855095a3c85`  
		Last Modified: Wed, 01 Apr 2026 20:06:25 GMT  
		Size: 224.0 MB (224023254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3acf289b9f31eb827cbc2b51b579cd5ea21b56735f0e735a5f5be59510752c4a`  
		Last Modified: Wed, 01 Apr 2026 20:06:24 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad5fa83c1077ae117a57fd36920e82f8cfe0458321eefb8a4f1307f5e6d2b84`  
		Last Modified: Wed, 01 Apr 2026 20:06:19 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d049147650bccf304c14b8108133d3e09e2a712232a823779a6c3e95ee00fc5d`  
		Last Modified: Wed, 01 Apr 2026 20:06:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cbd9b471e501348876c82ac4f9aa7c6f68ece17902c638cd736a34b4057a3c`  
		Last Modified: Wed, 01 Apr 2026 20:06:21 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45561826e56e9196a428ea93727947135407e4c3e32bafe0e31c115cdb6002cf`  
		Last Modified: Wed, 01 Apr 2026 20:06:17 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f1a3e9017fb0238f8dec720083a4c5354cd59f3389f8463ebde14de26fcbb24a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2728e55ad7a87bed0b0aed80f79112fb2ee20b8562187fff2d4d2cd54b28e82d`

```dockerfile
```

-	Layers:
	-	`sha256:72586ffb7c07af8397e8b35c6e1ecb529997218fd39db8b0211471a5f66eb048`  
		Last Modified: Wed, 01 Apr 2026 20:06:19 GMT  
		Size: 26.7 KB (26651 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:b049f1894852c6f88038c8672984754261cf2f265f3c9cddfbfa980ae1dc0166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244464397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd3e32e853c72ba0dbff4072a2b945852dedf837a2da6a84be74fe1fbc00e094`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:34 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:34 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:34 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:34 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:34 GMT
ARG VERSION=26.3.1.896
# Wed, 01 Apr 2026 20:05:34 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:06:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:06:04 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:06:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:06:04 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:06:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:06:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c91c9bb03f5c1be062449acdf2e31b868f28566ebdf3d2dc66e522880010a2`  
		Last Modified: Wed, 01 Apr 2026 20:06:27 GMT  
		Size: 7.6 MB (7577453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460842314d3242e865bc24647f0e2ba5f5fb6c279a11d4f56634d75925f72104`  
		Last Modified: Wed, 01 Apr 2026 20:06:30 GMT  
		Size: 208.4 MB (208409957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54370e74a6c297ea48114087bb043d22f9a8707a542dc8202e1f6d2cef570385`  
		Last Modified: Wed, 01 Apr 2026 20:06:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c8603370b11a223c2230a410d3d0c37cfa20ce1b3771b125e1f433949b98bd`  
		Last Modified: Wed, 01 Apr 2026 20:06:26 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5a0a67309f515d5a11f570805fedc9e58feb41d9b49723f2d7d5a22150d9bd`  
		Last Modified: Wed, 01 Apr 2026 20:06:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a48ac8a84f790732886aa96d0d703decf93fd80706f8385f80d90fb5bd7d68`  
		Last Modified: Wed, 01 Apr 2026 20:06:28 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204362d0086811f274a089d895ec551087a54bb78adee7efe7025904f946b562`  
		Last Modified: Wed, 01 Apr 2026 20:06:28 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4179cae6a9b44859cc8bed139f805476637f01dad9267dc9ed962f8a9960fb50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b18502d1ffb802e9a7265897e5df2ffa8e6b67287f7dfb8049352b875a47515a`

```dockerfile
```

-	Layers:
	-	`sha256:b51f0249c540ffed3fda88182372c2ede4549bd4e79ceca3324f30c8a0974ea0`  
		Last Modified: Wed, 01 Apr 2026 20:06:26 GMT  
		Size: 26.9 KB (26887 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts`

```console
$ docker pull clickhouse@sha256:61a86a946f7e24107e1456651dc5da9154f2997722110aa83f0b847e174fde26
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts` - linux; amd64

```console
$ docker pull clickhouse@sha256:0fd0732bef5efc5999dfcf6356cc97beb21d76eeb92c3b91cb22b29b2a19b7a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.2 MB (262228036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41318e73cfbae6b1a89e7c6a9b3e64378ba9cc097b2092f348183cfd39299b15`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:27 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:27 GMT
ARG VERSION=26.3.1.896
# Wed, 01 Apr 2026 20:05:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:05:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:05:56 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:05:56 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:05:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:05:57 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:05:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:05:57 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:05:57 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:05:57 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:05:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534ad254b48275e47a53a047d04eac1b9ced7d8484e6358f8caa1876a7af4f77`  
		Last Modified: Wed, 01 Apr 2026 20:06:19 GMT  
		Size: 7.6 MB (7598315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47fd016e96bd289b13add3a240233fe68a1e1cc6691ef37542db855095a3c85`  
		Last Modified: Wed, 01 Apr 2026 20:06:25 GMT  
		Size: 224.0 MB (224023254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3acf289b9f31eb827cbc2b51b579cd5ea21b56735f0e735a5f5be59510752c4a`  
		Last Modified: Wed, 01 Apr 2026 20:06:24 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad5fa83c1077ae117a57fd36920e82f8cfe0458321eefb8a4f1307f5e6d2b84`  
		Last Modified: Wed, 01 Apr 2026 20:06:19 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d049147650bccf304c14b8108133d3e09e2a712232a823779a6c3e95ee00fc5d`  
		Last Modified: Wed, 01 Apr 2026 20:06:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cbd9b471e501348876c82ac4f9aa7c6f68ece17902c638cd736a34b4057a3c`  
		Last Modified: Wed, 01 Apr 2026 20:06:21 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45561826e56e9196a428ea93727947135407e4c3e32bafe0e31c115cdb6002cf`  
		Last Modified: Wed, 01 Apr 2026 20:06:17 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f1a3e9017fb0238f8dec720083a4c5354cd59f3389f8463ebde14de26fcbb24a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2728e55ad7a87bed0b0aed80f79112fb2ee20b8562187fff2d4d2cd54b28e82d`

```dockerfile
```

-	Layers:
	-	`sha256:72586ffb7c07af8397e8b35c6e1ecb529997218fd39db8b0211471a5f66eb048`  
		Last Modified: Wed, 01 Apr 2026 20:06:19 GMT  
		Size: 26.7 KB (26651 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:b049f1894852c6f88038c8672984754261cf2f265f3c9cddfbfa980ae1dc0166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244464397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd3e32e853c72ba0dbff4072a2b945852dedf837a2da6a84be74fe1fbc00e094`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:34 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:34 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:34 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:34 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:34 GMT
ARG VERSION=26.3.1.896
# Wed, 01 Apr 2026 20:05:34 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:06:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:06:04 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:06:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:06:04 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:06:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:06:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c91c9bb03f5c1be062449acdf2e31b868f28566ebdf3d2dc66e522880010a2`  
		Last Modified: Wed, 01 Apr 2026 20:06:27 GMT  
		Size: 7.6 MB (7577453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460842314d3242e865bc24647f0e2ba5f5fb6c279a11d4f56634d75925f72104`  
		Last Modified: Wed, 01 Apr 2026 20:06:30 GMT  
		Size: 208.4 MB (208409957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54370e74a6c297ea48114087bb043d22f9a8707a542dc8202e1f6d2cef570385`  
		Last Modified: Wed, 01 Apr 2026 20:06:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c8603370b11a223c2230a410d3d0c37cfa20ce1b3771b125e1f433949b98bd`  
		Last Modified: Wed, 01 Apr 2026 20:06:26 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5a0a67309f515d5a11f570805fedc9e58feb41d9b49723f2d7d5a22150d9bd`  
		Last Modified: Wed, 01 Apr 2026 20:06:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a48ac8a84f790732886aa96d0d703decf93fd80706f8385f80d90fb5bd7d68`  
		Last Modified: Wed, 01 Apr 2026 20:06:28 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204362d0086811f274a089d895ec551087a54bb78adee7efe7025904f946b562`  
		Last Modified: Wed, 01 Apr 2026 20:06:28 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4179cae6a9b44859cc8bed139f805476637f01dad9267dc9ed962f8a9960fb50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b18502d1ffb802e9a7265897e5df2ffa8e6b67287f7dfb8049352b875a47515a`

```dockerfile
```

-	Layers:
	-	`sha256:b51f0249c540ffed3fda88182372c2ede4549bd4e79ceca3324f30c8a0974ea0`  
		Last Modified: Wed, 01 Apr 2026 20:06:26 GMT  
		Size: 26.9 KB (26887 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts-jammy`

```console
$ docker pull clickhouse@sha256:61a86a946f7e24107e1456651dc5da9154f2997722110aa83f0b847e174fde26
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:0fd0732bef5efc5999dfcf6356cc97beb21d76eeb92c3b91cb22b29b2a19b7a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.2 MB (262228036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41318e73cfbae6b1a89e7c6a9b3e64378ba9cc097b2092f348183cfd39299b15`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:27 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:27 GMT
ARG VERSION=26.3.1.896
# Wed, 01 Apr 2026 20:05:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:05:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:05:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:05:56 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:05:56 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:05:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:05:57 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:05:57 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:05:57 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:05:57 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:05:57 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:05:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534ad254b48275e47a53a047d04eac1b9ced7d8484e6358f8caa1876a7af4f77`  
		Last Modified: Wed, 01 Apr 2026 20:06:19 GMT  
		Size: 7.6 MB (7598315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47fd016e96bd289b13add3a240233fe68a1e1cc6691ef37542db855095a3c85`  
		Last Modified: Wed, 01 Apr 2026 20:06:25 GMT  
		Size: 224.0 MB (224023254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3acf289b9f31eb827cbc2b51b579cd5ea21b56735f0e735a5f5be59510752c4a`  
		Last Modified: Wed, 01 Apr 2026 20:06:24 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad5fa83c1077ae117a57fd36920e82f8cfe0458321eefb8a4f1307f5e6d2b84`  
		Last Modified: Wed, 01 Apr 2026 20:06:19 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d049147650bccf304c14b8108133d3e09e2a712232a823779a6c3e95ee00fc5d`  
		Last Modified: Wed, 01 Apr 2026 20:06:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cbd9b471e501348876c82ac4f9aa7c6f68ece17902c638cd736a34b4057a3c`  
		Last Modified: Wed, 01 Apr 2026 20:06:21 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45561826e56e9196a428ea93727947135407e4c3e32bafe0e31c115cdb6002cf`  
		Last Modified: Wed, 01 Apr 2026 20:06:17 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f1a3e9017fb0238f8dec720083a4c5354cd59f3389f8463ebde14de26fcbb24a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2728e55ad7a87bed0b0aed80f79112fb2ee20b8562187fff2d4d2cd54b28e82d`

```dockerfile
```

-	Layers:
	-	`sha256:72586ffb7c07af8397e8b35c6e1ecb529997218fd39db8b0211471a5f66eb048`  
		Last Modified: Wed, 01 Apr 2026 20:06:19 GMT  
		Size: 26.7 KB (26651 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:b049f1894852c6f88038c8672984754261cf2f265f3c9cddfbfa980ae1dc0166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244464397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd3e32e853c72ba0dbff4072a2b945852dedf837a2da6a84be74fe1fbc00e094`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:05:34 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 01 Apr 2026 20:05:34 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 01 Apr 2026 20:05:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 01 Apr 2026 20:05:34 GMT
ARG REPO_CHANNEL=stable
# Wed, 01 Apr 2026 20:05:34 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 01 Apr 2026 20:05:34 GMT
ARG VERSION=26.3.1.896
# Wed, 01 Apr 2026 20:05:34 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 01 Apr 2026 20:06:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:06:04 GMT
ENV TZ=UTC
# Wed, 01 Apr 2026 20:06:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:06:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 01 Apr 2026 20:06:04 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 01 Apr 2026 20:06:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 01 Apr 2026 20:06:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c91c9bb03f5c1be062449acdf2e31b868f28566ebdf3d2dc66e522880010a2`  
		Last Modified: Wed, 01 Apr 2026 20:06:27 GMT  
		Size: 7.6 MB (7577453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460842314d3242e865bc24647f0e2ba5f5fb6c279a11d4f56634d75925f72104`  
		Last Modified: Wed, 01 Apr 2026 20:06:30 GMT  
		Size: 208.4 MB (208409957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54370e74a6c297ea48114087bb043d22f9a8707a542dc8202e1f6d2cef570385`  
		Last Modified: Wed, 01 Apr 2026 20:06:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c8603370b11a223c2230a410d3d0c37cfa20ce1b3771b125e1f433949b98bd`  
		Last Modified: Wed, 01 Apr 2026 20:06:26 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5a0a67309f515d5a11f570805fedc9e58feb41d9b49723f2d7d5a22150d9bd`  
		Last Modified: Wed, 01 Apr 2026 20:06:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a48ac8a84f790732886aa96d0d703decf93fd80706f8385f80d90fb5bd7d68`  
		Last Modified: Wed, 01 Apr 2026 20:06:28 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204362d0086811f274a089d895ec551087a54bb78adee7efe7025904f946b562`  
		Last Modified: Wed, 01 Apr 2026 20:06:28 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4179cae6a9b44859cc8bed139f805476637f01dad9267dc9ed962f8a9960fb50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b18502d1ffb802e9a7265897e5df2ffa8e6b67287f7dfb8049352b875a47515a`

```dockerfile
```

-	Layers:
	-	`sha256:b51f0249c540ffed3fda88182372c2ede4549bd4e79ceca3324f30c8a0974ea0`  
		Last Modified: Wed, 01 Apr 2026 20:06:26 GMT  
		Size: 26.9 KB (26887 bytes)  
		MIME: application/vnd.in-toto+json
