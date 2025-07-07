<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clickhouse`

-	[`clickhouse:25.3`](#clickhouse253)
-	[`clickhouse:25.3-jammy`](#clickhouse253-jammy)
-	[`clickhouse:25.3.5`](#clickhouse2535)
-	[`clickhouse:25.3.5-jammy`](#clickhouse2535-jammy)
-	[`clickhouse:25.3.5.42`](#clickhouse253542)
-	[`clickhouse:25.3.5.42-jammy`](#clickhouse253542-jammy)
-	[`clickhouse:25.4`](#clickhouse254)
-	[`clickhouse:25.4-jammy`](#clickhouse254-jammy)
-	[`clickhouse:25.4.9`](#clickhouse2549)
-	[`clickhouse:25.4.9-jammy`](#clickhouse2549-jammy)
-	[`clickhouse:25.4.9.14`](#clickhouse254914)
-	[`clickhouse:25.4.9.14-jammy`](#clickhouse254914-jammy)
-	[`clickhouse:25.5`](#clickhouse255)
-	[`clickhouse:25.5-jammy`](#clickhouse255-jammy)
-	[`clickhouse:25.5.6`](#clickhouse2556)
-	[`clickhouse:25.5.6-jammy`](#clickhouse2556-jammy)
-	[`clickhouse:25.5.6.14`](#clickhouse255614)
-	[`clickhouse:25.5.6.14-jammy`](#clickhouse255614-jammy)
-	[`clickhouse:25.6`](#clickhouse256)
-	[`clickhouse:25.6-jammy`](#clickhouse256-jammy)
-	[`clickhouse:25.6.2`](#clickhouse2562)
-	[`clickhouse:25.6.2-jammy`](#clickhouse2562-jammy)
-	[`clickhouse:25.6.2.5`](#clickhouse25625)
-	[`clickhouse:25.6.2.5-jammy`](#clickhouse25625-jammy)
-	[`clickhouse:jammy`](#clickhousejammy)
-	[`clickhouse:latest`](#clickhouselatest)
-	[`clickhouse:lts`](#clickhouselts)
-	[`clickhouse:lts-jammy`](#clickhouselts-jammy)

## `clickhouse:25.3`

```console
$ docker pull clickhouse@sha256:49f5b75ec3a569dbe50acb66780a225d29ffcfc5a5cb877d93ceb95c34251293
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:d8f635befa70fa0c45be6225b696864a6451f017ba62bf5ddda48a21d9bd7590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.7 MB (204659623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b90fcaca844c127e836d31e01ea9dce94fa23be7bc355de01e364920525ad24`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:16:46 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:16:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:16:49 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 20 Jun 2025 10:16:49 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.3.4.190
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104c2bdaf2b02eb3f26b85e0576c00c4f907f93f8c62af3064e43dc094f41a07`  
		Last Modified: Wed, 02 Jul 2025 03:10:30 GMT  
		Size: 7.2 MB (7151669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da6ef7d3b065fdf197f3dd65f9ee2e30dc510766d8239aff2a15f4747fd574a`  
		Last Modified: Wed, 02 Jul 2025 06:49:57 GMT  
		Size: 167.1 MB (167102022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c25e9ac71c24467c144a76ce318f614889ce0daf9f5dc8790b4f4bf5fb0a1ef`  
		Last Modified: Wed, 02 Jul 2025 03:10:29 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a062209c921c121bb92b83347f0331bd2c20225c4e1cff78814308125b4ff6d`  
		Last Modified: Wed, 02 Jul 2025 03:10:29 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e0b859169434ef7e1b5790afbddec7cd2384d7191c9b30dd97b5d5f93c54a3`  
		Last Modified: Wed, 02 Jul 2025 03:10:29 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f31232c6e2f74deecbb80b4c8543e2130cb2d34df05909c3d61f26ce2f112701`  
		Last Modified: Wed, 02 Jul 2025 03:10:29 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58c58364d0572cde3bdf34909d49d86ac7e30fed6a6c7348c7f77b21dbbe451`  
		Last Modified: Wed, 02 Jul 2025 03:10:29 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3f303132522edab91cbc25281246c9b126e115a685f762959073e888a220d0b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b53e376f3cf83cb574547a6fb3a6d752a00260dafd114613457e6efc885f53e2`

```dockerfile
```

-	Layers:
	-	`sha256:d3998c26d9ddf10719a879795cb439d110fec37df8d10e93e3c06fd305568758`  
		Last Modified: Wed, 02 Jul 2025 06:49:21 GMT  
		Size: 25.9 KB (25886 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:2e3b4f19b5acf3c7ae8417327db75a8d0988bd9a4c4133957c38a0013a532f91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192180209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a32218ce2bb1c2ec06c6a083d3d00a8e3ce8f4a8a7b9306175f79c84546b7e74`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:18:35 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:18:37 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 20 Jun 2025 10:18:37 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.3.4.190
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc63836cf54edbe487093a98cd679c0d6119b7f2319ff0ee57e940dd07e42e41`  
		Last Modified: Wed, 02 Jul 2025 04:22:58 GMT  
		Size: 7.1 MB (7127871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384a3a362bc0e7cd77831dd0465f8c9b3e03db00e94fcde53215ee63e802393d`  
		Last Modified: Wed, 02 Jul 2025 06:55:20 GMT  
		Size: 156.8 MB (156822817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d838e3a1af3f6a54e2226427f97a6ed60055dd5561df51fecd68ba4e9db3d648`  
		Last Modified: Wed, 02 Jul 2025 04:25:19 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae087b18ef2b2730319ae27bbc891e4153b8fde973810ff505b55f807fa08a90`  
		Last Modified: Wed, 02 Jul 2025 04:25:19 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181d43a87b24f7ebf7be3aa404dca9b16cfc7a662196c71a790e215348c7430c`  
		Last Modified: Wed, 02 Jul 2025 04:25:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61a24c08f04ddd72200c608bccab06fc6539754f01bfbc26dc92c070cf2e837`  
		Last Modified: Wed, 02 Jul 2025 04:25:18 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad8c04c557de6398a13c0d503120d0ad9234f77003900b98dc39d6ad2d459d3`  
		Last Modified: Wed, 02 Jul 2025 04:25:19 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:365e00b7d353ec6ef40d35c38bc2095946f3f4cb8f2cbede5245e5b1916e6cb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d492a1d926298716d97409cb4f461c804ad2c8c81548f3e75ffdcd70917a5417`

```dockerfile
```

-	Layers:
	-	`sha256:b9b824397acbee3e0d51403b7b411531dde259e191c01b6d89a202c99e60e7b8`  
		Last Modified: Wed, 02 Jul 2025 06:49:25 GMT  
		Size: 26.1 KB (26098 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3-jammy`

```console
$ docker pull clickhouse@sha256:49f5b75ec3a569dbe50acb66780a225d29ffcfc5a5cb877d93ceb95c34251293
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:d8f635befa70fa0c45be6225b696864a6451f017ba62bf5ddda48a21d9bd7590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.7 MB (204659623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b90fcaca844c127e836d31e01ea9dce94fa23be7bc355de01e364920525ad24`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:16:46 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:16:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:16:49 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 20 Jun 2025 10:16:49 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.3.4.190
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104c2bdaf2b02eb3f26b85e0576c00c4f907f93f8c62af3064e43dc094f41a07`  
		Last Modified: Wed, 02 Jul 2025 03:10:30 GMT  
		Size: 7.2 MB (7151669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da6ef7d3b065fdf197f3dd65f9ee2e30dc510766d8239aff2a15f4747fd574a`  
		Last Modified: Wed, 02 Jul 2025 06:49:57 GMT  
		Size: 167.1 MB (167102022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c25e9ac71c24467c144a76ce318f614889ce0daf9f5dc8790b4f4bf5fb0a1ef`  
		Last Modified: Wed, 02 Jul 2025 03:10:29 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a062209c921c121bb92b83347f0331bd2c20225c4e1cff78814308125b4ff6d`  
		Last Modified: Wed, 02 Jul 2025 03:10:29 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e0b859169434ef7e1b5790afbddec7cd2384d7191c9b30dd97b5d5f93c54a3`  
		Last Modified: Wed, 02 Jul 2025 03:10:29 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f31232c6e2f74deecbb80b4c8543e2130cb2d34df05909c3d61f26ce2f112701`  
		Last Modified: Wed, 02 Jul 2025 03:10:29 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58c58364d0572cde3bdf34909d49d86ac7e30fed6a6c7348c7f77b21dbbe451`  
		Last Modified: Wed, 02 Jul 2025 03:10:29 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3f303132522edab91cbc25281246c9b126e115a685f762959073e888a220d0b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b53e376f3cf83cb574547a6fb3a6d752a00260dafd114613457e6efc885f53e2`

```dockerfile
```

-	Layers:
	-	`sha256:d3998c26d9ddf10719a879795cb439d110fec37df8d10e93e3c06fd305568758`  
		Last Modified: Wed, 02 Jul 2025 06:49:21 GMT  
		Size: 25.9 KB (25886 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:2e3b4f19b5acf3c7ae8417327db75a8d0988bd9a4c4133957c38a0013a532f91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192180209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a32218ce2bb1c2ec06c6a083d3d00a8e3ce8f4a8a7b9306175f79c84546b7e74`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:18:35 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:18:37 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 20 Jun 2025 10:18:37 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.3.4.190
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc63836cf54edbe487093a98cd679c0d6119b7f2319ff0ee57e940dd07e42e41`  
		Last Modified: Wed, 02 Jul 2025 04:22:58 GMT  
		Size: 7.1 MB (7127871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384a3a362bc0e7cd77831dd0465f8c9b3e03db00e94fcde53215ee63e802393d`  
		Last Modified: Wed, 02 Jul 2025 06:55:20 GMT  
		Size: 156.8 MB (156822817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d838e3a1af3f6a54e2226427f97a6ed60055dd5561df51fecd68ba4e9db3d648`  
		Last Modified: Wed, 02 Jul 2025 04:25:19 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae087b18ef2b2730319ae27bbc891e4153b8fde973810ff505b55f807fa08a90`  
		Last Modified: Wed, 02 Jul 2025 04:25:19 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181d43a87b24f7ebf7be3aa404dca9b16cfc7a662196c71a790e215348c7430c`  
		Last Modified: Wed, 02 Jul 2025 04:25:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61a24c08f04ddd72200c608bccab06fc6539754f01bfbc26dc92c070cf2e837`  
		Last Modified: Wed, 02 Jul 2025 04:25:18 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad8c04c557de6398a13c0d503120d0ad9234f77003900b98dc39d6ad2d459d3`  
		Last Modified: Wed, 02 Jul 2025 04:25:19 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:365e00b7d353ec6ef40d35c38bc2095946f3f4cb8f2cbede5245e5b1916e6cb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d492a1d926298716d97409cb4f461c804ad2c8c81548f3e75ffdcd70917a5417`

```dockerfile
```

-	Layers:
	-	`sha256:b9b824397acbee3e0d51403b7b411531dde259e191c01b6d89a202c99e60e7b8`  
		Last Modified: Wed, 02 Jul 2025 06:49:25 GMT  
		Size: 26.1 KB (26098 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.5`

**does not exist** (yet?)

## `clickhouse:25.3.5-jammy`

**does not exist** (yet?)

## `clickhouse:25.3.5.42`

**does not exist** (yet?)

## `clickhouse:25.3.5.42-jammy`

**does not exist** (yet?)

## `clickhouse:25.4`

```console
$ docker pull clickhouse@sha256:9f7382ff15311e69855cddacf510691cfa701c4506b5e2decbf0858019b92879
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.4` - linux; amd64

```console
$ docker pull clickhouse@sha256:dbaf5db133e1af7f3826b9e25cb26b334674827c73ecb58651a41a7444368591
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202675366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1d6022f34b2fa0b9215a3465928026b2e36d17ab59abaf85a344b08dc9a1038`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:16:46 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:16:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:16:49 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 20 Jun 2025 10:16:49 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.4.7.66
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679cbeb4a6117e4a89354385a22991056e1a8ba7a0faf362d2d54100fcbc2fee`  
		Last Modified: Wed, 02 Jul 2025 03:10:28 GMT  
		Size: 7.2 MB (7151652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638f678e2e0e3d2d72c7e27f1862113026358e303c3753b0470fe308f8c9c053`  
		Last Modified: Wed, 02 Jul 2025 06:55:20 GMT  
		Size: 165.1 MB (165117784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6df584021a4952c558982a48d242b0ae8b8c77a3ae299ffd724a99ae2798c0`  
		Last Modified: Wed, 02 Jul 2025 03:10:26 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1828df3cb32bfe1f9553f994c53189eda09f756781c27628c19c452a109f2920`  
		Last Modified: Wed, 02 Jul 2025 03:10:26 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f311fe84a2dce203104d8aada861287455280206949ffe889dc9092295f3c365`  
		Last Modified: Wed, 02 Jul 2025 03:10:27 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f1274a79351c464dbc2dad572b3d4f1ab867898021f80c1a3e0bf05d2702a5`  
		Last Modified: Wed, 02 Jul 2025 03:10:26 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7b9d5aca7a7a54ce2d46ced324e2d23289e6c06fd10d04208e316d30858fd0`  
		Last Modified: Wed, 02 Jul 2025 03:10:27 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:037e245f02e341d28caac2f95d27df37726a0c6f56801f3c44eba03970d900f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:603a1b6aae002a02454e13976842228e87ad9a3e612c36b8faa14590f6c97445`

```dockerfile
```

-	Layers:
	-	`sha256:e572c291236bda57040052d8ed47908cb0546fe3ecee642200233a94c88eb4a5`  
		Last Modified: Wed, 02 Jul 2025 06:49:33 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.4` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4df5f6d460629f59ecddbc46b6c5d27376ab771a5862bdfc06d47e55f59814ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (190022438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed8575b048f51c67ddc2099de63a17f427278f5e47f9a05820b46902cb1f774f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:18:35 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:18:37 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 20 Jun 2025 10:18:37 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.4.7.66
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc63836cf54edbe487093a98cd679c0d6119b7f2319ff0ee57e940dd07e42e41`  
		Last Modified: Wed, 02 Jul 2025 04:22:58 GMT  
		Size: 7.1 MB (7127871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc56d823391ab7401425406d6a855f2f2cdd7f1d1db4d3dc058408ff00bf234`  
		Last Modified: Wed, 02 Jul 2025 06:55:17 GMT  
		Size: 154.7 MB (154665047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5456f0cb6164326c4da32dd8d0a6f5f28bb968f776d9a10c51bc6abd056dbfb`  
		Last Modified: Wed, 02 Jul 2025 04:24:30 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3fb17302f69c5b90ea632ae93960b0ad9d1c38d339b7d154430b8423586e0e`  
		Last Modified: Wed, 02 Jul 2025 04:24:30 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17fdbf40b48cd6c97c56ebb802b16b40e9f35ca5b6c5d64fdb5589b8da2965cb`  
		Last Modified: Wed, 02 Jul 2025 04:24:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3653fc849d9eabf98bb14766b2bc9cf9d6c04174e0ab276a2ab6228267bf00`  
		Last Modified: Wed, 02 Jul 2025 04:24:30 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a97d1cccb811f1a7d8a3c0358285fc0eebe1df75da17e545a3424dddc95f576`  
		Last Modified: Wed, 02 Jul 2025 04:24:30 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5d4b443d8cf9443d407c3d98b04cd035cf7e8a0e33bc1aa39e2b0529591d0ada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40b38f79c376d97b0d59c6cebd35269a4b23e16c69e9e3880b02499eb89db977`

```dockerfile
```

-	Layers:
	-	`sha256:8aeda07879ed4c3fd2d2356645ca3aa30d6816091352b98674467d5c367efd2c`  
		Last Modified: Wed, 02 Jul 2025 06:49:36 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.4-jammy`

```console
$ docker pull clickhouse@sha256:9f7382ff15311e69855cddacf510691cfa701c4506b5e2decbf0858019b92879
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.4-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:dbaf5db133e1af7f3826b9e25cb26b334674827c73ecb58651a41a7444368591
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202675366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1d6022f34b2fa0b9215a3465928026b2e36d17ab59abaf85a344b08dc9a1038`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:16:46 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:16:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:16:49 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 20 Jun 2025 10:16:49 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.4.7.66
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679cbeb4a6117e4a89354385a22991056e1a8ba7a0faf362d2d54100fcbc2fee`  
		Last Modified: Wed, 02 Jul 2025 03:10:28 GMT  
		Size: 7.2 MB (7151652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638f678e2e0e3d2d72c7e27f1862113026358e303c3753b0470fe308f8c9c053`  
		Last Modified: Wed, 02 Jul 2025 06:55:20 GMT  
		Size: 165.1 MB (165117784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6df584021a4952c558982a48d242b0ae8b8c77a3ae299ffd724a99ae2798c0`  
		Last Modified: Wed, 02 Jul 2025 03:10:26 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1828df3cb32bfe1f9553f994c53189eda09f756781c27628c19c452a109f2920`  
		Last Modified: Wed, 02 Jul 2025 03:10:26 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f311fe84a2dce203104d8aada861287455280206949ffe889dc9092295f3c365`  
		Last Modified: Wed, 02 Jul 2025 03:10:27 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f1274a79351c464dbc2dad572b3d4f1ab867898021f80c1a3e0bf05d2702a5`  
		Last Modified: Wed, 02 Jul 2025 03:10:26 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7b9d5aca7a7a54ce2d46ced324e2d23289e6c06fd10d04208e316d30858fd0`  
		Last Modified: Wed, 02 Jul 2025 03:10:27 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:037e245f02e341d28caac2f95d27df37726a0c6f56801f3c44eba03970d900f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:603a1b6aae002a02454e13976842228e87ad9a3e612c36b8faa14590f6c97445`

```dockerfile
```

-	Layers:
	-	`sha256:e572c291236bda57040052d8ed47908cb0546fe3ecee642200233a94c88eb4a5`  
		Last Modified: Wed, 02 Jul 2025 06:49:33 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.4-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4df5f6d460629f59ecddbc46b6c5d27376ab771a5862bdfc06d47e55f59814ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (190022438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed8575b048f51c67ddc2099de63a17f427278f5e47f9a05820b46902cb1f774f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:18:35 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:18:37 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 20 Jun 2025 10:18:37 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.4.7.66
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc63836cf54edbe487093a98cd679c0d6119b7f2319ff0ee57e940dd07e42e41`  
		Last Modified: Wed, 02 Jul 2025 04:22:58 GMT  
		Size: 7.1 MB (7127871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc56d823391ab7401425406d6a855f2f2cdd7f1d1db4d3dc058408ff00bf234`  
		Last Modified: Wed, 02 Jul 2025 06:55:17 GMT  
		Size: 154.7 MB (154665047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5456f0cb6164326c4da32dd8d0a6f5f28bb968f776d9a10c51bc6abd056dbfb`  
		Last Modified: Wed, 02 Jul 2025 04:24:30 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3fb17302f69c5b90ea632ae93960b0ad9d1c38d339b7d154430b8423586e0e`  
		Last Modified: Wed, 02 Jul 2025 04:24:30 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17fdbf40b48cd6c97c56ebb802b16b40e9f35ca5b6c5d64fdb5589b8da2965cb`  
		Last Modified: Wed, 02 Jul 2025 04:24:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3653fc849d9eabf98bb14766b2bc9cf9d6c04174e0ab276a2ab6228267bf00`  
		Last Modified: Wed, 02 Jul 2025 04:24:30 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a97d1cccb811f1a7d8a3c0358285fc0eebe1df75da17e545a3424dddc95f576`  
		Last Modified: Wed, 02 Jul 2025 04:24:30 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5d4b443d8cf9443d407c3d98b04cd035cf7e8a0e33bc1aa39e2b0529591d0ada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40b38f79c376d97b0d59c6cebd35269a4b23e16c69e9e3880b02499eb89db977`

```dockerfile
```

-	Layers:
	-	`sha256:8aeda07879ed4c3fd2d2356645ca3aa30d6816091352b98674467d5c367efd2c`  
		Last Modified: Wed, 02 Jul 2025 06:49:36 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.4.9`

**does not exist** (yet?)

## `clickhouse:25.4.9-jammy`

**does not exist** (yet?)

## `clickhouse:25.4.9.14`

**does not exist** (yet?)

## `clickhouse:25.4.9.14-jammy`

**does not exist** (yet?)

## `clickhouse:25.5`

```console
$ docker pull clickhouse@sha256:87f5b48b54884fac7dd2511da0d73be3e5457a24e8f48034db2a1bf43fd23103
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.5` - linux; amd64

```console
$ docker pull clickhouse@sha256:a1cdf5c13e20cf6c25d07ebd0542be184d306bf47c63b5f2c905c91fa15b07f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.9 MB (204928019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2601588f28c0c97c59aa309d92d81a9e2edc9d32b6ef72738c6de77b60bc67`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:16:46 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:16:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:16:49 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 20 Jun 2025 10:16:49 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.5.4.38
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97a79a932a497dfa918b66405b817b11ee7a79f093d25b0579c7459112fe266`  
		Last Modified: Wed, 02 Jul 2025 03:10:30 GMT  
		Size: 7.2 MB (7151672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5dbe68f23b3832a2e956b62928ec382028a8f2e26533f4c2626668532ae09b`  
		Last Modified: Wed, 02 Jul 2025 06:55:53 GMT  
		Size: 167.4 MB (167370419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f46026909fa13a77dede5a0ff60e50931b169842a7112edc584252b021628c`  
		Last Modified: Wed, 02 Jul 2025 03:10:29 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c20239fe3d61636a3f7a35fff91af74f7a00eb482b71e6ac2c0e5195938c7df`  
		Last Modified: Wed, 02 Jul 2025 03:10:29 GMT  
		Size: 865.7 KB (865743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f5c4c3ba15641d32639dc4dc0f9990dab2bda5e3bf5eb906d7e22cfe7fb546`  
		Last Modified: Wed, 02 Jul 2025 03:10:29 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a8f8d1c6a21118b0a252d8d05cf8bd6fc2b749f4c3a4f5b48f43d865b35774`  
		Last Modified: Wed, 02 Jul 2025 03:10:29 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58c58364d0572cde3bdf34909d49d86ac7e30fed6a6c7348c7f77b21dbbe451`  
		Last Modified: Wed, 02 Jul 2025 03:10:29 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5` - unknown; unknown

```console
$ docker pull clickhouse@sha256:27b58218aaf3bfeeb602e62f35f382561dbedbcee0320bc8ac3c40cda28b900f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:254c7a38c77a3aeec579b746bf0440f0e72fc05e65d1d9f0ccc542d140cf3c80`

```dockerfile
```

-	Layers:
	-	`sha256:ca6167bc1f39edb7cd992f1cae97d5da45bc8b1458d7a4293ba79f4510052871`  
		Last Modified: Wed, 02 Jul 2025 06:49:44 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.5` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:db7e656cd93c7bd8823eee6fea2a265fd5a957982fc2c5bc86f8714faa728880
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191502401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:553ee03064c9f9156ea9cc69dba1f114a979fdbb6d419dfef5ca8df5dff004a1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:18:35 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:18:37 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 20 Jun 2025 10:18:37 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.5.4.38
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc63836cf54edbe487093a98cd679c0d6119b7f2319ff0ee57e940dd07e42e41`  
		Last Modified: Wed, 02 Jul 2025 04:22:58 GMT  
		Size: 7.1 MB (7127871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cd6f5afd1eb368e9f5c0418400b3573fc6c67d8cddc9c434f3a5a01024a6fa`  
		Last Modified: Wed, 02 Jul 2025 06:55:56 GMT  
		Size: 156.1 MB (156145015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9218969a47f9ff6e76f519dc409b6818f3d2096997b032940d7ae07fe6e69120`  
		Last Modified: Wed, 02 Jul 2025 04:23:42 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e89cff5fccf8976ceca44251a121f6e01238f7b795def4415a8fbb48844583b`  
		Last Modified: Wed, 02 Jul 2025 04:23:42 GMT  
		Size: 865.7 KB (865744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54c9a54cb5cf3057ac5d586afe9a917b179eb5487c8a7a0c0538ab0d3d4d2ea`  
		Last Modified: Wed, 02 Jul 2025 04:23:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d356d5dc2a32c7ffd02c3abd056c88d8438eb86be87dc75572195aad4f1726`  
		Last Modified: Wed, 02 Jul 2025 04:23:42 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13dd116c427645ddc85356eb6fc051489f146752219ee337eb62215b424a2180`  
		Last Modified: Wed, 02 Jul 2025 04:23:42 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4806e63b5df615f5bc668692d79a5dad2e071da7cde7fa0d54ea463f10602429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760c14ee3c7bf8fd063ca7c48236bc318f85ff3ddd8aaa23849a2fcaef396f1f`

```dockerfile
```

-	Layers:
	-	`sha256:a811fe2ec4a1ec1cd478ecaf5527fe7f79c9f76a5790139eaacb7cf53ed2708b`  
		Last Modified: Wed, 02 Jul 2025 06:49:48 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.5-jammy`

```console
$ docker pull clickhouse@sha256:87f5b48b54884fac7dd2511da0d73be3e5457a24e8f48034db2a1bf43fd23103
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.5-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:a1cdf5c13e20cf6c25d07ebd0542be184d306bf47c63b5f2c905c91fa15b07f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.9 MB (204928019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2601588f28c0c97c59aa309d92d81a9e2edc9d32b6ef72738c6de77b60bc67`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:16:46 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:16:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:16:49 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 20 Jun 2025 10:16:49 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.5.4.38
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97a79a932a497dfa918b66405b817b11ee7a79f093d25b0579c7459112fe266`  
		Last Modified: Wed, 02 Jul 2025 03:10:30 GMT  
		Size: 7.2 MB (7151672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5dbe68f23b3832a2e956b62928ec382028a8f2e26533f4c2626668532ae09b`  
		Last Modified: Wed, 02 Jul 2025 06:55:53 GMT  
		Size: 167.4 MB (167370419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f46026909fa13a77dede5a0ff60e50931b169842a7112edc584252b021628c`  
		Last Modified: Wed, 02 Jul 2025 03:10:29 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c20239fe3d61636a3f7a35fff91af74f7a00eb482b71e6ac2c0e5195938c7df`  
		Last Modified: Wed, 02 Jul 2025 03:10:29 GMT  
		Size: 865.7 KB (865743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f5c4c3ba15641d32639dc4dc0f9990dab2bda5e3bf5eb906d7e22cfe7fb546`  
		Last Modified: Wed, 02 Jul 2025 03:10:29 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a8f8d1c6a21118b0a252d8d05cf8bd6fc2b749f4c3a4f5b48f43d865b35774`  
		Last Modified: Wed, 02 Jul 2025 03:10:29 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58c58364d0572cde3bdf34909d49d86ac7e30fed6a6c7348c7f77b21dbbe451`  
		Last Modified: Wed, 02 Jul 2025 03:10:29 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:27b58218aaf3bfeeb602e62f35f382561dbedbcee0320bc8ac3c40cda28b900f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:254c7a38c77a3aeec579b746bf0440f0e72fc05e65d1d9f0ccc542d140cf3c80`

```dockerfile
```

-	Layers:
	-	`sha256:ca6167bc1f39edb7cd992f1cae97d5da45bc8b1458d7a4293ba79f4510052871`  
		Last Modified: Wed, 02 Jul 2025 06:49:44 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.5-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:db7e656cd93c7bd8823eee6fea2a265fd5a957982fc2c5bc86f8714faa728880
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191502401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:553ee03064c9f9156ea9cc69dba1f114a979fdbb6d419dfef5ca8df5dff004a1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:18:35 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:18:37 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 20 Jun 2025 10:18:37 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.5.4.38
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc63836cf54edbe487093a98cd679c0d6119b7f2319ff0ee57e940dd07e42e41`  
		Last Modified: Wed, 02 Jul 2025 04:22:58 GMT  
		Size: 7.1 MB (7127871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cd6f5afd1eb368e9f5c0418400b3573fc6c67d8cddc9c434f3a5a01024a6fa`  
		Last Modified: Wed, 02 Jul 2025 06:55:56 GMT  
		Size: 156.1 MB (156145015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9218969a47f9ff6e76f519dc409b6818f3d2096997b032940d7ae07fe6e69120`  
		Last Modified: Wed, 02 Jul 2025 04:23:42 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e89cff5fccf8976ceca44251a121f6e01238f7b795def4415a8fbb48844583b`  
		Last Modified: Wed, 02 Jul 2025 04:23:42 GMT  
		Size: 865.7 KB (865744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54c9a54cb5cf3057ac5d586afe9a917b179eb5487c8a7a0c0538ab0d3d4d2ea`  
		Last Modified: Wed, 02 Jul 2025 04:23:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d356d5dc2a32c7ffd02c3abd056c88d8438eb86be87dc75572195aad4f1726`  
		Last Modified: Wed, 02 Jul 2025 04:23:42 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13dd116c427645ddc85356eb6fc051489f146752219ee337eb62215b424a2180`  
		Last Modified: Wed, 02 Jul 2025 04:23:42 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4806e63b5df615f5bc668692d79a5dad2e071da7cde7fa0d54ea463f10602429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760c14ee3c7bf8fd063ca7c48236bc318f85ff3ddd8aaa23849a2fcaef396f1f`

```dockerfile
```

-	Layers:
	-	`sha256:a811fe2ec4a1ec1cd478ecaf5527fe7f79c9f76a5790139eaacb7cf53ed2708b`  
		Last Modified: Wed, 02 Jul 2025 06:49:48 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.5.6`

**does not exist** (yet?)

## `clickhouse:25.5.6-jammy`

**does not exist** (yet?)

## `clickhouse:25.5.6.14`

**does not exist** (yet?)

## `clickhouse:25.5.6.14-jammy`

**does not exist** (yet?)

## `clickhouse:25.6`

```console
$ docker pull clickhouse@sha256:0553b2a0694402f0ad9a61f38d138e8347386abfba6b6520985a20f50b6930ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6` - linux; amd64

```console
$ docker pull clickhouse@sha256:1e801f1a53f2d95fa271522d3239f1836a8e19a240821e131ff0cee70026154e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.9 MB (211943384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f1ff92a6840c80761849b6728ee9a4a3ffefeecdca2742ef00193bff9916bd`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:16:46 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:16:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:16:49 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 20 Jun 2025 10:16:49 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.6.1.3206
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a1637f5502c67b526e9bc3cfeca600dce96543f03eb27019d0041ee4174cc7`  
		Last Modified: Wed, 02 Jul 2025 03:10:43 GMT  
		Size: 7.2 MB (7151643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa28bfd8b50056b5cb978968d37138aeed27ff9237450ebfa71b0fb61ef3583`  
		Last Modified: Wed, 02 Jul 2025 06:50:25 GMT  
		Size: 174.4 MB (174386034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051903cc395d903139ee457befbc29ec3292b9746a5880577001d8c4de257e30`  
		Last Modified: Wed, 02 Jul 2025 03:10:36 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa7c59ac55a829d77855eac7696c4feab848a356c5609a0452e04697d9c41939`  
		Last Modified: Wed, 02 Jul 2025 03:10:37 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63680a0a115053afe7088b4e7a8f63d89e6bf2458e073040864c68dc1b401fb7`  
		Last Modified: Wed, 02 Jul 2025 03:10:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53eec9f329dbc0b30dcec8a6a8d8cdcc1c2fdadd3d17a8917c90e5add0d1546a`  
		Last Modified: Wed, 02 Jul 2025 03:10:37 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd515ee754790c9d877a364ae558e3c53d2c322d8c2ce1dd1303895e04502e8`  
		Last Modified: Wed, 02 Jul 2025 03:10:36 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4264499de9ed6e105c1d9d2da695116ed3ae862e7af8f1e29f8011567e7755a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e8ff95c3c91495333d522020f3e0b46e7b697e6b0e593945a0c7e187d87d49`

```dockerfile
```

-	Layers:
	-	`sha256:9af019c5e02bc1b165c74580c95a0a7dc7d713806ef0532b94b4a1fa46573cee`  
		Last Modified: Wed, 02 Jul 2025 06:49:57 GMT  
		Size: 25.9 KB (25898 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.6` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:afc053b21c7882e8430af51137b3d555803b37bc19e90829c5fb72f5942b09a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.1 MB (198102303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a33dd9eb106c51a34330fc7cb8cb501a384ff70889f3594b6378a8e5f3425d1e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:18:35 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:18:37 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 20 Jun 2025 10:18:37 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.6.1.3206
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc63836cf54edbe487093a98cd679c0d6119b7f2319ff0ee57e940dd07e42e41`  
		Last Modified: Wed, 02 Jul 2025 04:22:58 GMT  
		Size: 7.1 MB (7127871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcaba232407c2c036075d65c6cf23ba8e57397244608476c6fd9cdbe68b59923`  
		Last Modified: Wed, 02 Jul 2025 06:55:55 GMT  
		Size: 162.7 MB (162745144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab41f04a385f00e5aa91c7f41f9d0ea70b5253cc78569a4085c8399bd54119e9`  
		Last Modified: Wed, 02 Jul 2025 04:22:57 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7997c5b75b804ca7a178e2988ce5f56dc6f3299de5505f9964b6cce652780a`  
		Last Modified: Wed, 02 Jul 2025 04:22:58 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8eb5eb09651d8448bc9e67c85363d2f95808afc6367f5f4bb8387dee7ec7c6`  
		Last Modified: Wed, 02 Jul 2025 04:22:58 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3bde4de3adc75c664c94d71be5c4567c8def45782360f8a733627c0c4b1e32`  
		Last Modified: Wed, 02 Jul 2025 04:22:58 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb723e7d6c35e7ed89363082dbe7717806580bbc1fa3adf5328ce843c12989cc`  
		Last Modified: Wed, 02 Jul 2025 04:22:58 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6` - unknown; unknown

```console
$ docker pull clickhouse@sha256:7d82ea28300618e8e9dd2d7479e15496de959bc7930e422e21527ea49306dd30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3685195818abbf25b61b8eac618d6b01a227689310dae0c5e5f2ffbae1cdeda`

```dockerfile
```

-	Layers:
	-	`sha256:08cde2a5c470fbed02c4c7627b8854d21feaf803a6803846791f6d8b6f0a46fb`  
		Last Modified: Wed, 02 Jul 2025 06:50:00 GMT  
		Size: 26.1 KB (26111 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.6-jammy`

```console
$ docker pull clickhouse@sha256:0553b2a0694402f0ad9a61f38d138e8347386abfba6b6520985a20f50b6930ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:1e801f1a53f2d95fa271522d3239f1836a8e19a240821e131ff0cee70026154e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.9 MB (211943384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f1ff92a6840c80761849b6728ee9a4a3ffefeecdca2742ef00193bff9916bd`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:16:46 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:16:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:16:49 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 20 Jun 2025 10:16:49 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.6.1.3206
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a1637f5502c67b526e9bc3cfeca600dce96543f03eb27019d0041ee4174cc7`  
		Last Modified: Wed, 02 Jul 2025 03:10:43 GMT  
		Size: 7.2 MB (7151643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa28bfd8b50056b5cb978968d37138aeed27ff9237450ebfa71b0fb61ef3583`  
		Last Modified: Wed, 02 Jul 2025 06:50:25 GMT  
		Size: 174.4 MB (174386034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051903cc395d903139ee457befbc29ec3292b9746a5880577001d8c4de257e30`  
		Last Modified: Wed, 02 Jul 2025 03:10:36 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa7c59ac55a829d77855eac7696c4feab848a356c5609a0452e04697d9c41939`  
		Last Modified: Wed, 02 Jul 2025 03:10:37 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63680a0a115053afe7088b4e7a8f63d89e6bf2458e073040864c68dc1b401fb7`  
		Last Modified: Wed, 02 Jul 2025 03:10:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53eec9f329dbc0b30dcec8a6a8d8cdcc1c2fdadd3d17a8917c90e5add0d1546a`  
		Last Modified: Wed, 02 Jul 2025 03:10:37 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd515ee754790c9d877a364ae558e3c53d2c322d8c2ce1dd1303895e04502e8`  
		Last Modified: Wed, 02 Jul 2025 03:10:36 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4264499de9ed6e105c1d9d2da695116ed3ae862e7af8f1e29f8011567e7755a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e8ff95c3c91495333d522020f3e0b46e7b697e6b0e593945a0c7e187d87d49`

```dockerfile
```

-	Layers:
	-	`sha256:9af019c5e02bc1b165c74580c95a0a7dc7d713806ef0532b94b4a1fa46573cee`  
		Last Modified: Wed, 02 Jul 2025 06:49:57 GMT  
		Size: 25.9 KB (25898 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.6-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:afc053b21c7882e8430af51137b3d555803b37bc19e90829c5fb72f5942b09a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.1 MB (198102303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a33dd9eb106c51a34330fc7cb8cb501a384ff70889f3594b6378a8e5f3425d1e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:18:35 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:18:37 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 20 Jun 2025 10:18:37 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.6.1.3206
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc63836cf54edbe487093a98cd679c0d6119b7f2319ff0ee57e940dd07e42e41`  
		Last Modified: Wed, 02 Jul 2025 04:22:58 GMT  
		Size: 7.1 MB (7127871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcaba232407c2c036075d65c6cf23ba8e57397244608476c6fd9cdbe68b59923`  
		Last Modified: Wed, 02 Jul 2025 06:55:55 GMT  
		Size: 162.7 MB (162745144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab41f04a385f00e5aa91c7f41f9d0ea70b5253cc78569a4085c8399bd54119e9`  
		Last Modified: Wed, 02 Jul 2025 04:22:57 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7997c5b75b804ca7a178e2988ce5f56dc6f3299de5505f9964b6cce652780a`  
		Last Modified: Wed, 02 Jul 2025 04:22:58 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8eb5eb09651d8448bc9e67c85363d2f95808afc6367f5f4bb8387dee7ec7c6`  
		Last Modified: Wed, 02 Jul 2025 04:22:58 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3bde4de3adc75c664c94d71be5c4567c8def45782360f8a733627c0c4b1e32`  
		Last Modified: Wed, 02 Jul 2025 04:22:58 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb723e7d6c35e7ed89363082dbe7717806580bbc1fa3adf5328ce843c12989cc`  
		Last Modified: Wed, 02 Jul 2025 04:22:58 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:7d82ea28300618e8e9dd2d7479e15496de959bc7930e422e21527ea49306dd30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3685195818abbf25b61b8eac618d6b01a227689310dae0c5e5f2ffbae1cdeda`

```dockerfile
```

-	Layers:
	-	`sha256:08cde2a5c470fbed02c4c7627b8854d21feaf803a6803846791f6d8b6f0a46fb`  
		Last Modified: Wed, 02 Jul 2025 06:50:00 GMT  
		Size: 26.1 KB (26111 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.6.2`

**does not exist** (yet?)

## `clickhouse:25.6.2-jammy`

**does not exist** (yet?)

## `clickhouse:25.6.2.5`

**does not exist** (yet?)

## `clickhouse:25.6.2.5-jammy`

**does not exist** (yet?)

## `clickhouse:jammy`

```console
$ docker pull clickhouse@sha256:0553b2a0694402f0ad9a61f38d138e8347386abfba6b6520985a20f50b6930ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:1e801f1a53f2d95fa271522d3239f1836a8e19a240821e131ff0cee70026154e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.9 MB (211943384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f1ff92a6840c80761849b6728ee9a4a3ffefeecdca2742ef00193bff9916bd`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:16:46 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:16:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:16:49 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 20 Jun 2025 10:16:49 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.6.1.3206
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a1637f5502c67b526e9bc3cfeca600dce96543f03eb27019d0041ee4174cc7`  
		Last Modified: Wed, 02 Jul 2025 03:10:43 GMT  
		Size: 7.2 MB (7151643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa28bfd8b50056b5cb978968d37138aeed27ff9237450ebfa71b0fb61ef3583`  
		Last Modified: Wed, 02 Jul 2025 06:50:25 GMT  
		Size: 174.4 MB (174386034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051903cc395d903139ee457befbc29ec3292b9746a5880577001d8c4de257e30`  
		Last Modified: Wed, 02 Jul 2025 03:10:36 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa7c59ac55a829d77855eac7696c4feab848a356c5609a0452e04697d9c41939`  
		Last Modified: Wed, 02 Jul 2025 03:10:37 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63680a0a115053afe7088b4e7a8f63d89e6bf2458e073040864c68dc1b401fb7`  
		Last Modified: Wed, 02 Jul 2025 03:10:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53eec9f329dbc0b30dcec8a6a8d8cdcc1c2fdadd3d17a8917c90e5add0d1546a`  
		Last Modified: Wed, 02 Jul 2025 03:10:37 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd515ee754790c9d877a364ae558e3c53d2c322d8c2ce1dd1303895e04502e8`  
		Last Modified: Wed, 02 Jul 2025 03:10:36 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4264499de9ed6e105c1d9d2da695116ed3ae862e7af8f1e29f8011567e7755a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e8ff95c3c91495333d522020f3e0b46e7b697e6b0e593945a0c7e187d87d49`

```dockerfile
```

-	Layers:
	-	`sha256:9af019c5e02bc1b165c74580c95a0a7dc7d713806ef0532b94b4a1fa46573cee`  
		Last Modified: Wed, 02 Jul 2025 06:49:57 GMT  
		Size: 25.9 KB (25898 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:afc053b21c7882e8430af51137b3d555803b37bc19e90829c5fb72f5942b09a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.1 MB (198102303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a33dd9eb106c51a34330fc7cb8cb501a384ff70889f3594b6378a8e5f3425d1e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:18:35 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:18:37 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 20 Jun 2025 10:18:37 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.6.1.3206
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc63836cf54edbe487093a98cd679c0d6119b7f2319ff0ee57e940dd07e42e41`  
		Last Modified: Wed, 02 Jul 2025 04:22:58 GMT  
		Size: 7.1 MB (7127871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcaba232407c2c036075d65c6cf23ba8e57397244608476c6fd9cdbe68b59923`  
		Last Modified: Wed, 02 Jul 2025 06:55:55 GMT  
		Size: 162.7 MB (162745144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab41f04a385f00e5aa91c7f41f9d0ea70b5253cc78569a4085c8399bd54119e9`  
		Last Modified: Wed, 02 Jul 2025 04:22:57 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7997c5b75b804ca7a178e2988ce5f56dc6f3299de5505f9964b6cce652780a`  
		Last Modified: Wed, 02 Jul 2025 04:22:58 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8eb5eb09651d8448bc9e67c85363d2f95808afc6367f5f4bb8387dee7ec7c6`  
		Last Modified: Wed, 02 Jul 2025 04:22:58 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3bde4de3adc75c664c94d71be5c4567c8def45782360f8a733627c0c4b1e32`  
		Last Modified: Wed, 02 Jul 2025 04:22:58 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb723e7d6c35e7ed89363082dbe7717806580bbc1fa3adf5328ce843c12989cc`  
		Last Modified: Wed, 02 Jul 2025 04:22:58 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:7d82ea28300618e8e9dd2d7479e15496de959bc7930e422e21527ea49306dd30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3685195818abbf25b61b8eac618d6b01a227689310dae0c5e5f2ffbae1cdeda`

```dockerfile
```

-	Layers:
	-	`sha256:08cde2a5c470fbed02c4c7627b8854d21feaf803a6803846791f6d8b6f0a46fb`  
		Last Modified: Wed, 02 Jul 2025 06:50:00 GMT  
		Size: 26.1 KB (26111 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:0553b2a0694402f0ad9a61f38d138e8347386abfba6b6520985a20f50b6930ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

```console
$ docker pull clickhouse@sha256:1e801f1a53f2d95fa271522d3239f1836a8e19a240821e131ff0cee70026154e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.9 MB (211943384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f1ff92a6840c80761849b6728ee9a4a3ffefeecdca2742ef00193bff9916bd`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:16:46 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:16:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:16:49 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 20 Jun 2025 10:16:49 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.6.1.3206
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a1637f5502c67b526e9bc3cfeca600dce96543f03eb27019d0041ee4174cc7`  
		Last Modified: Wed, 02 Jul 2025 03:10:43 GMT  
		Size: 7.2 MB (7151643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa28bfd8b50056b5cb978968d37138aeed27ff9237450ebfa71b0fb61ef3583`  
		Last Modified: Wed, 02 Jul 2025 06:50:25 GMT  
		Size: 174.4 MB (174386034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051903cc395d903139ee457befbc29ec3292b9746a5880577001d8c4de257e30`  
		Last Modified: Wed, 02 Jul 2025 03:10:36 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa7c59ac55a829d77855eac7696c4feab848a356c5609a0452e04697d9c41939`  
		Last Modified: Wed, 02 Jul 2025 03:10:37 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63680a0a115053afe7088b4e7a8f63d89e6bf2458e073040864c68dc1b401fb7`  
		Last Modified: Wed, 02 Jul 2025 03:10:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53eec9f329dbc0b30dcec8a6a8d8cdcc1c2fdadd3d17a8917c90e5add0d1546a`  
		Last Modified: Wed, 02 Jul 2025 03:10:37 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd515ee754790c9d877a364ae558e3c53d2c322d8c2ce1dd1303895e04502e8`  
		Last Modified: Wed, 02 Jul 2025 03:10:36 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4264499de9ed6e105c1d9d2da695116ed3ae862e7af8f1e29f8011567e7755a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e8ff95c3c91495333d522020f3e0b46e7b697e6b0e593945a0c7e187d87d49`

```dockerfile
```

-	Layers:
	-	`sha256:9af019c5e02bc1b165c74580c95a0a7dc7d713806ef0532b94b4a1fa46573cee`  
		Last Modified: Wed, 02 Jul 2025 06:49:57 GMT  
		Size: 25.9 KB (25898 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:afc053b21c7882e8430af51137b3d555803b37bc19e90829c5fb72f5942b09a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.1 MB (198102303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a33dd9eb106c51a34330fc7cb8cb501a384ff70889f3594b6378a8e5f3425d1e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:18:35 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:18:37 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 20 Jun 2025 10:18:37 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.6.1.3206
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc63836cf54edbe487093a98cd679c0d6119b7f2319ff0ee57e940dd07e42e41`  
		Last Modified: Wed, 02 Jul 2025 04:22:58 GMT  
		Size: 7.1 MB (7127871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcaba232407c2c036075d65c6cf23ba8e57397244608476c6fd9cdbe68b59923`  
		Last Modified: Wed, 02 Jul 2025 06:55:55 GMT  
		Size: 162.7 MB (162745144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab41f04a385f00e5aa91c7f41f9d0ea70b5253cc78569a4085c8399bd54119e9`  
		Last Modified: Wed, 02 Jul 2025 04:22:57 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7997c5b75b804ca7a178e2988ce5f56dc6f3299de5505f9964b6cce652780a`  
		Last Modified: Wed, 02 Jul 2025 04:22:58 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8eb5eb09651d8448bc9e67c85363d2f95808afc6367f5f4bb8387dee7ec7c6`  
		Last Modified: Wed, 02 Jul 2025 04:22:58 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3bde4de3adc75c664c94d71be5c4567c8def45782360f8a733627c0c4b1e32`  
		Last Modified: Wed, 02 Jul 2025 04:22:58 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb723e7d6c35e7ed89363082dbe7717806580bbc1fa3adf5328ce843c12989cc`  
		Last Modified: Wed, 02 Jul 2025 04:22:58 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:7d82ea28300618e8e9dd2d7479e15496de959bc7930e422e21527ea49306dd30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3685195818abbf25b61b8eac618d6b01a227689310dae0c5e5f2ffbae1cdeda`

```dockerfile
```

-	Layers:
	-	`sha256:08cde2a5c470fbed02c4c7627b8854d21feaf803a6803846791f6d8b6f0a46fb`  
		Last Modified: Wed, 02 Jul 2025 06:50:00 GMT  
		Size: 26.1 KB (26111 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts`

```console
$ docker pull clickhouse@sha256:49f5b75ec3a569dbe50acb66780a225d29ffcfc5a5cb877d93ceb95c34251293
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts` - linux; amd64

```console
$ docker pull clickhouse@sha256:d8f635befa70fa0c45be6225b696864a6451f017ba62bf5ddda48a21d9bd7590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.7 MB (204659623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b90fcaca844c127e836d31e01ea9dce94fa23be7bc355de01e364920525ad24`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:16:46 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:16:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:16:49 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 20 Jun 2025 10:16:49 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.3.4.190
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104c2bdaf2b02eb3f26b85e0576c00c4f907f93f8c62af3064e43dc094f41a07`  
		Last Modified: Wed, 02 Jul 2025 03:10:30 GMT  
		Size: 7.2 MB (7151669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da6ef7d3b065fdf197f3dd65f9ee2e30dc510766d8239aff2a15f4747fd574a`  
		Last Modified: Wed, 02 Jul 2025 06:49:57 GMT  
		Size: 167.1 MB (167102022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c25e9ac71c24467c144a76ce318f614889ce0daf9f5dc8790b4f4bf5fb0a1ef`  
		Last Modified: Wed, 02 Jul 2025 03:10:29 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a062209c921c121bb92b83347f0331bd2c20225c4e1cff78814308125b4ff6d`  
		Last Modified: Wed, 02 Jul 2025 03:10:29 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e0b859169434ef7e1b5790afbddec7cd2384d7191c9b30dd97b5d5f93c54a3`  
		Last Modified: Wed, 02 Jul 2025 03:10:29 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f31232c6e2f74deecbb80b4c8543e2130cb2d34df05909c3d61f26ce2f112701`  
		Last Modified: Wed, 02 Jul 2025 03:10:29 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58c58364d0572cde3bdf34909d49d86ac7e30fed6a6c7348c7f77b21dbbe451`  
		Last Modified: Wed, 02 Jul 2025 03:10:29 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3f303132522edab91cbc25281246c9b126e115a685f762959073e888a220d0b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b53e376f3cf83cb574547a6fb3a6d752a00260dafd114613457e6efc885f53e2`

```dockerfile
```

-	Layers:
	-	`sha256:d3998c26d9ddf10719a879795cb439d110fec37df8d10e93e3c06fd305568758`  
		Last Modified: Wed, 02 Jul 2025 06:49:21 GMT  
		Size: 25.9 KB (25886 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:2e3b4f19b5acf3c7ae8417327db75a8d0988bd9a4c4133957c38a0013a532f91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192180209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a32218ce2bb1c2ec06c6a083d3d00a8e3ce8f4a8a7b9306175f79c84546b7e74`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:18:35 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:18:37 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 20 Jun 2025 10:18:37 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.3.4.190
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc63836cf54edbe487093a98cd679c0d6119b7f2319ff0ee57e940dd07e42e41`  
		Last Modified: Wed, 02 Jul 2025 04:22:58 GMT  
		Size: 7.1 MB (7127871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384a3a362bc0e7cd77831dd0465f8c9b3e03db00e94fcde53215ee63e802393d`  
		Last Modified: Wed, 02 Jul 2025 06:55:20 GMT  
		Size: 156.8 MB (156822817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d838e3a1af3f6a54e2226427f97a6ed60055dd5561df51fecd68ba4e9db3d648`  
		Last Modified: Wed, 02 Jul 2025 04:25:19 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae087b18ef2b2730319ae27bbc891e4153b8fde973810ff505b55f807fa08a90`  
		Last Modified: Wed, 02 Jul 2025 04:25:19 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181d43a87b24f7ebf7be3aa404dca9b16cfc7a662196c71a790e215348c7430c`  
		Last Modified: Wed, 02 Jul 2025 04:25:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61a24c08f04ddd72200c608bccab06fc6539754f01bfbc26dc92c070cf2e837`  
		Last Modified: Wed, 02 Jul 2025 04:25:18 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad8c04c557de6398a13c0d503120d0ad9234f77003900b98dc39d6ad2d459d3`  
		Last Modified: Wed, 02 Jul 2025 04:25:19 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:365e00b7d353ec6ef40d35c38bc2095946f3f4cb8f2cbede5245e5b1916e6cb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d492a1d926298716d97409cb4f461c804ad2c8c81548f3e75ffdcd70917a5417`

```dockerfile
```

-	Layers:
	-	`sha256:b9b824397acbee3e0d51403b7b411531dde259e191c01b6d89a202c99e60e7b8`  
		Last Modified: Wed, 02 Jul 2025 06:49:25 GMT  
		Size: 26.1 KB (26098 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts-jammy`

```console
$ docker pull clickhouse@sha256:49f5b75ec3a569dbe50acb66780a225d29ffcfc5a5cb877d93ceb95c34251293
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:d8f635befa70fa0c45be6225b696864a6451f017ba62bf5ddda48a21d9bd7590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.7 MB (204659623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b90fcaca844c127e836d31e01ea9dce94fa23be7bc355de01e364920525ad24`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:16:46 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:16:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:16:46 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:16:49 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 20 Jun 2025 10:16:49 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.3.4.190
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104c2bdaf2b02eb3f26b85e0576c00c4f907f93f8c62af3064e43dc094f41a07`  
		Last Modified: Wed, 02 Jul 2025 03:10:30 GMT  
		Size: 7.2 MB (7151669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da6ef7d3b065fdf197f3dd65f9ee2e30dc510766d8239aff2a15f4747fd574a`  
		Last Modified: Wed, 02 Jul 2025 06:49:57 GMT  
		Size: 167.1 MB (167102022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c25e9ac71c24467c144a76ce318f614889ce0daf9f5dc8790b4f4bf5fb0a1ef`  
		Last Modified: Wed, 02 Jul 2025 03:10:29 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a062209c921c121bb92b83347f0331bd2c20225c4e1cff78814308125b4ff6d`  
		Last Modified: Wed, 02 Jul 2025 03:10:29 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e0b859169434ef7e1b5790afbddec7cd2384d7191c9b30dd97b5d5f93c54a3`  
		Last Modified: Wed, 02 Jul 2025 03:10:29 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f31232c6e2f74deecbb80b4c8543e2130cb2d34df05909c3d61f26ce2f112701`  
		Last Modified: Wed, 02 Jul 2025 03:10:29 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58c58364d0572cde3bdf34909d49d86ac7e30fed6a6c7348c7f77b21dbbe451`  
		Last Modified: Wed, 02 Jul 2025 03:10:29 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3f303132522edab91cbc25281246c9b126e115a685f762959073e888a220d0b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b53e376f3cf83cb574547a6fb3a6d752a00260dafd114613457e6efc885f53e2`

```dockerfile
```

-	Layers:
	-	`sha256:d3998c26d9ddf10719a879795cb439d110fec37df8d10e93e3c06fd305568758`  
		Last Modified: Wed, 02 Jul 2025 06:49:21 GMT  
		Size: 25.9 KB (25886 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:2e3b4f19b5acf3c7ae8417327db75a8d0988bd9a4c4133957c38a0013a532f91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192180209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a32218ce2bb1c2ec06c6a083d3d00a8e3ce8f4a8a7b9306175f79c84546b7e74`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 20 Jun 2025 10:18:35 GMT
ARG RELEASE
# Fri, 20 Jun 2025 10:18:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Jun 2025 10:18:35 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 20 Jun 2025 10:18:37 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Fri, 20 Jun 2025 10:18:37 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.3.4.190
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc63836cf54edbe487093a98cd679c0d6119b7f2319ff0ee57e940dd07e42e41`  
		Last Modified: Wed, 02 Jul 2025 04:22:58 GMT  
		Size: 7.1 MB (7127871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384a3a362bc0e7cd77831dd0465f8c9b3e03db00e94fcde53215ee63e802393d`  
		Last Modified: Wed, 02 Jul 2025 06:55:20 GMT  
		Size: 156.8 MB (156822817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d838e3a1af3f6a54e2226427f97a6ed60055dd5561df51fecd68ba4e9db3d648`  
		Last Modified: Wed, 02 Jul 2025 04:25:19 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae087b18ef2b2730319ae27bbc891e4153b8fde973810ff505b55f807fa08a90`  
		Last Modified: Wed, 02 Jul 2025 04:25:19 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181d43a87b24f7ebf7be3aa404dca9b16cfc7a662196c71a790e215348c7430c`  
		Last Modified: Wed, 02 Jul 2025 04:25:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61a24c08f04ddd72200c608bccab06fc6539754f01bfbc26dc92c070cf2e837`  
		Last Modified: Wed, 02 Jul 2025 04:25:18 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad8c04c557de6398a13c0d503120d0ad9234f77003900b98dc39d6ad2d459d3`  
		Last Modified: Wed, 02 Jul 2025 04:25:19 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:365e00b7d353ec6ef40d35c38bc2095946f3f4cb8f2cbede5245e5b1916e6cb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d492a1d926298716d97409cb4f461c804ad2c8c81548f3e75ffdcd70917a5417`

```dockerfile
```

-	Layers:
	-	`sha256:b9b824397acbee3e0d51403b7b411531dde259e191c01b6d89a202c99e60e7b8`  
		Last Modified: Wed, 02 Jul 2025 06:49:25 GMT  
		Size: 26.1 KB (26098 bytes)  
		MIME: application/vnd.in-toto+json
