<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clickhouse`

-	[`clickhouse:25.3`](#clickhouse253)
-	[`clickhouse:25.3-jammy`](#clickhouse253-jammy)
-	[`clickhouse:25.3.7`](#clickhouse2537)
-	[`clickhouse:25.3.7-jammy`](#clickhouse2537-jammy)
-	[`clickhouse:25.3.7.194`](#clickhouse2537194)
-	[`clickhouse:25.3.7.194-jammy`](#clickhouse2537194-jammy)
-	[`clickhouse:25.7`](#clickhouse257)
-	[`clickhouse:25.7-jammy`](#clickhouse257-jammy)
-	[`clickhouse:25.7.8`](#clickhouse2578)
-	[`clickhouse:25.7.8-jammy`](#clickhouse2578-jammy)
-	[`clickhouse:25.7.8.71`](#clickhouse257871)
-	[`clickhouse:25.7.8.71-jammy`](#clickhouse257871-jammy)
-	[`clickhouse:25.8`](#clickhouse258)
-	[`clickhouse:25.8-jammy`](#clickhouse258-jammy)
-	[`clickhouse:25.8.10`](#clickhouse25810)
-	[`clickhouse:25.8.10-jammy`](#clickhouse25810-jammy)
-	[`clickhouse:25.8.10.7`](#clickhouse258107)
-	[`clickhouse:25.8.10.7-jammy`](#clickhouse258107-jammy)
-	[`clickhouse:25.9`](#clickhouse259)
-	[`clickhouse:25.9-jammy`](#clickhouse259-jammy)
-	[`clickhouse:25.9.4`](#clickhouse2594)
-	[`clickhouse:25.9.4-jammy`](#clickhouse2594-jammy)
-	[`clickhouse:25.9.4.58`](#clickhouse259458)
-	[`clickhouse:25.9.4.58-jammy`](#clickhouse259458-jammy)
-	[`clickhouse:jammy`](#clickhousejammy)
-	[`clickhouse:latest`](#clickhouselatest)
-	[`clickhouse:lts`](#clickhouselts)
-	[`clickhouse:lts-jammy`](#clickhouselts-jammy)

## `clickhouse:25.3`

```console
$ docker pull clickhouse@sha256:e4fd5d9c36120b531ee62f3c550525d214cbaafe40181d207f5ecad1142d7650
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:e3fb656126491239d39ea97b91a562f221ca9167774475fb304d69885773a9d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.5 MB (205502138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d0e165e2f132d96906ab0b36c9f0193d2599234560e5a8f3468eb68193f86d3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 16 Oct 2025 16:06:54 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 16 Oct 2025 16:06:54 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
ARG REPO_CHANNEL=stable
# Thu, 16 Oct 2025 16:06:54 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 16 Oct 2025 16:06:54 GMT
ARG VERSION=25.3.7.194
# Thu, 16 Oct 2025 16:06:54 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.7.194 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.7.194 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.7.194 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
ENV LANG=en_US.UTF-8
# Thu, 16 Oct 2025 16:06:54 GMT
ENV TZ=UTC
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.7.194 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 16 Oct 2025 16:06:54 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 16 Oct 2025 16:06:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 16 Oct 2025 16:06:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4201bedd3b8f4da93c07aee6fa701d1c014f1c5fdc9038d4c9fc54d3fed3fd16`  
		Last Modified: Thu, 16 Oct 2025 18:54:16 GMT  
		Size: 7.2 MB (7151577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20b311e6ac5989423d05f047ee00c9bc6462aa971d874c5e0a966c9a31fcc03`  
		Last Modified: Thu, 16 Oct 2025 19:11:04 GMT  
		Size: 167.9 MB (167943491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1389958a7c4e44693b1136e775ff65b33a4e6fc8999a8d45c9ced4ba73a29b`  
		Last Modified: Thu, 16 Oct 2025 18:54:15 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dd9b6984c1652bd62ab70663ae49d76634bab8b7798c83a8681ea5ad6bbc36`  
		Last Modified: Thu, 16 Oct 2025 18:54:16 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735c0026b584ea438f8112ca05d62547105bf0aea59faf5bede6eeb7f0c89b7b`  
		Last Modified: Thu, 16 Oct 2025 18:54:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a6c0f3cdd16775f141e60465fe3fc079324e7475e94e4554a0f5eb624373eb`  
		Last Modified: Thu, 16 Oct 2025 18:54:15 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0388478724d63084d17671a04f1a784f3172e8d947c415834ae56cd6a9c3ea39`  
		Last Modified: Thu, 16 Oct 2025 18:54:15 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f69c8958d0cb8ecb41651e54d4dae645e8fc91a98496c92d56c3cc43cde2ac31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad7ddab7e37c5f9fa97a2b0f392be221f9962a239a6957782aadfcaa3a30b9a`

```dockerfile
```

-	Layers:
	-	`sha256:620f540e54216c95542ee6d03fc3f97c65c4f1ae04ddbb860bd9db29b0cce518`  
		Last Modified: Thu, 16 Oct 2025 21:49:20 GMT  
		Size: 25.3 KB (25274 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4ab19fe31703cc6c6646b7c42b9496fd2d6c4412e98e604c9d0ca37305f89607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (192984036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17752078ced3c015a86b8e789ef633a00e0347222c3a268caba3564b7fbebfb`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 16 Oct 2025 16:06:54 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 16 Oct 2025 16:06:54 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
ARG REPO_CHANNEL=stable
# Thu, 16 Oct 2025 16:06:54 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 16 Oct 2025 16:06:54 GMT
ARG VERSION=25.3.7.194
# Thu, 16 Oct 2025 16:06:54 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.7.194 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.7.194 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.7.194 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
ENV LANG=en_US.UTF-8
# Thu, 16 Oct 2025 16:06:54 GMT
ENV TZ=UTC
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.7.194 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 16 Oct 2025 16:06:54 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 16 Oct 2025 16:06:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 16 Oct 2025 16:06:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82537f702d38bef03492d1fc7bc9a15b15911182131d228b0fb39109e5bc3e53`  
		Last Modified: Thu, 16 Oct 2025 18:54:14 GMT  
		Size: 7.1 MB (7127250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe969a13317c5499c4d9f6c2ebbf88eac62c37d993df0002164b38b840306be`  
		Last Modified: Thu, 16 Oct 2025 18:55:00 GMT  
		Size: 157.6 MB (157603435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa762f1f7a11ed6e49ae25702c163396439725b27d727cf4d4c744f1e255b633`  
		Last Modified: Thu, 16 Oct 2025 18:54:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cbace4950e6ae8dc79f450c7b858c8753f4f94da5084c90582a8922916e64b`  
		Last Modified: Thu, 16 Oct 2025 18:54:13 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e6befd2db4b3f3139835f321a9f87074650287eac9742af2685b6fe54c8110`  
		Last Modified: Thu, 16 Oct 2025 18:54:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d6b9620edc1e68084fb4bc2eff805a4f72038aad5fed5ebda6135cf259803f`  
		Last Modified: Thu, 16 Oct 2025 18:54:13 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a966db524229a385c17f7ed623a63c2858dde005faab2c7a545e05d057742be`  
		Last Modified: Thu, 16 Oct 2025 18:54:13 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8cf3656994b42d6ab1f0cbdc5d5e49e9c4081cb76395efd3fd5ef35edf72ac86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f55141ed97091926b245679eec0d674dbf23f9573e097f1d182ade60d5a5cdb`

```dockerfile
```

-	Layers:
	-	`sha256:ec6ec35284eed9b262bcab8c510ff0aa5a33eb26663221514e3c8fc53c32a82b`  
		Last Modified: Thu, 16 Oct 2025 21:49:24 GMT  
		Size: 25.5 KB (25462 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3-jammy`

```console
$ docker pull clickhouse@sha256:e4fd5d9c36120b531ee62f3c550525d214cbaafe40181d207f5ecad1142d7650
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:e3fb656126491239d39ea97b91a562f221ca9167774475fb304d69885773a9d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.5 MB (205502138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d0e165e2f132d96906ab0b36c9f0193d2599234560e5a8f3468eb68193f86d3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 16 Oct 2025 16:06:54 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 16 Oct 2025 16:06:54 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
ARG REPO_CHANNEL=stable
# Thu, 16 Oct 2025 16:06:54 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 16 Oct 2025 16:06:54 GMT
ARG VERSION=25.3.7.194
# Thu, 16 Oct 2025 16:06:54 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.7.194 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.7.194 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.7.194 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
ENV LANG=en_US.UTF-8
# Thu, 16 Oct 2025 16:06:54 GMT
ENV TZ=UTC
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.7.194 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 16 Oct 2025 16:06:54 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 16 Oct 2025 16:06:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 16 Oct 2025 16:06:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4201bedd3b8f4da93c07aee6fa701d1c014f1c5fdc9038d4c9fc54d3fed3fd16`  
		Last Modified: Thu, 16 Oct 2025 18:54:16 GMT  
		Size: 7.2 MB (7151577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20b311e6ac5989423d05f047ee00c9bc6462aa971d874c5e0a966c9a31fcc03`  
		Last Modified: Thu, 16 Oct 2025 19:11:04 GMT  
		Size: 167.9 MB (167943491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1389958a7c4e44693b1136e775ff65b33a4e6fc8999a8d45c9ced4ba73a29b`  
		Last Modified: Thu, 16 Oct 2025 18:54:15 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dd9b6984c1652bd62ab70663ae49d76634bab8b7798c83a8681ea5ad6bbc36`  
		Last Modified: Thu, 16 Oct 2025 18:54:16 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735c0026b584ea438f8112ca05d62547105bf0aea59faf5bede6eeb7f0c89b7b`  
		Last Modified: Thu, 16 Oct 2025 18:54:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a6c0f3cdd16775f141e60465fe3fc079324e7475e94e4554a0f5eb624373eb`  
		Last Modified: Thu, 16 Oct 2025 18:54:15 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0388478724d63084d17671a04f1a784f3172e8d947c415834ae56cd6a9c3ea39`  
		Last Modified: Thu, 16 Oct 2025 18:54:15 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f69c8958d0cb8ecb41651e54d4dae645e8fc91a98496c92d56c3cc43cde2ac31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad7ddab7e37c5f9fa97a2b0f392be221f9962a239a6957782aadfcaa3a30b9a`

```dockerfile
```

-	Layers:
	-	`sha256:620f540e54216c95542ee6d03fc3f97c65c4f1ae04ddbb860bd9db29b0cce518`  
		Last Modified: Thu, 16 Oct 2025 21:49:20 GMT  
		Size: 25.3 KB (25274 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4ab19fe31703cc6c6646b7c42b9496fd2d6c4412e98e604c9d0ca37305f89607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (192984036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17752078ced3c015a86b8e789ef633a00e0347222c3a268caba3564b7fbebfb`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 16 Oct 2025 16:06:54 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 16 Oct 2025 16:06:54 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
ARG REPO_CHANNEL=stable
# Thu, 16 Oct 2025 16:06:54 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 16 Oct 2025 16:06:54 GMT
ARG VERSION=25.3.7.194
# Thu, 16 Oct 2025 16:06:54 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.7.194 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.7.194 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.7.194 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
ENV LANG=en_US.UTF-8
# Thu, 16 Oct 2025 16:06:54 GMT
ENV TZ=UTC
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.7.194 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 16 Oct 2025 16:06:54 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 16 Oct 2025 16:06:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 16 Oct 2025 16:06:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82537f702d38bef03492d1fc7bc9a15b15911182131d228b0fb39109e5bc3e53`  
		Last Modified: Thu, 16 Oct 2025 18:54:14 GMT  
		Size: 7.1 MB (7127250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe969a13317c5499c4d9f6c2ebbf88eac62c37d993df0002164b38b840306be`  
		Last Modified: Thu, 16 Oct 2025 18:55:00 GMT  
		Size: 157.6 MB (157603435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa762f1f7a11ed6e49ae25702c163396439725b27d727cf4d4c744f1e255b633`  
		Last Modified: Thu, 16 Oct 2025 18:54:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cbace4950e6ae8dc79f450c7b858c8753f4f94da5084c90582a8922916e64b`  
		Last Modified: Thu, 16 Oct 2025 18:54:13 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e6befd2db4b3f3139835f321a9f87074650287eac9742af2685b6fe54c8110`  
		Last Modified: Thu, 16 Oct 2025 18:54:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d6b9620edc1e68084fb4bc2eff805a4f72038aad5fed5ebda6135cf259803f`  
		Last Modified: Thu, 16 Oct 2025 18:54:13 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a966db524229a385c17f7ed623a63c2858dde005faab2c7a545e05d057742be`  
		Last Modified: Thu, 16 Oct 2025 18:54:13 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8cf3656994b42d6ab1f0cbdc5d5e49e9c4081cb76395efd3fd5ef35edf72ac86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f55141ed97091926b245679eec0d674dbf23f9573e097f1d182ade60d5a5cdb`

```dockerfile
```

-	Layers:
	-	`sha256:ec6ec35284eed9b262bcab8c510ff0aa5a33eb26663221514e3c8fc53c32a82b`  
		Last Modified: Thu, 16 Oct 2025 21:49:24 GMT  
		Size: 25.5 KB (25462 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.7`

```console
$ docker pull clickhouse@sha256:e4fd5d9c36120b531ee62f3c550525d214cbaafe40181d207f5ecad1142d7650
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.7` - linux; amd64

```console
$ docker pull clickhouse@sha256:e3fb656126491239d39ea97b91a562f221ca9167774475fb304d69885773a9d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.5 MB (205502138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d0e165e2f132d96906ab0b36c9f0193d2599234560e5a8f3468eb68193f86d3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 16 Oct 2025 16:06:54 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 16 Oct 2025 16:06:54 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
ARG REPO_CHANNEL=stable
# Thu, 16 Oct 2025 16:06:54 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 16 Oct 2025 16:06:54 GMT
ARG VERSION=25.3.7.194
# Thu, 16 Oct 2025 16:06:54 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.7.194 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.7.194 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.7.194 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
ENV LANG=en_US.UTF-8
# Thu, 16 Oct 2025 16:06:54 GMT
ENV TZ=UTC
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.7.194 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 16 Oct 2025 16:06:54 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 16 Oct 2025 16:06:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 16 Oct 2025 16:06:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4201bedd3b8f4da93c07aee6fa701d1c014f1c5fdc9038d4c9fc54d3fed3fd16`  
		Last Modified: Thu, 16 Oct 2025 18:54:16 GMT  
		Size: 7.2 MB (7151577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20b311e6ac5989423d05f047ee00c9bc6462aa971d874c5e0a966c9a31fcc03`  
		Last Modified: Thu, 16 Oct 2025 19:11:04 GMT  
		Size: 167.9 MB (167943491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1389958a7c4e44693b1136e775ff65b33a4e6fc8999a8d45c9ced4ba73a29b`  
		Last Modified: Thu, 16 Oct 2025 18:54:15 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dd9b6984c1652bd62ab70663ae49d76634bab8b7798c83a8681ea5ad6bbc36`  
		Last Modified: Thu, 16 Oct 2025 18:54:16 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735c0026b584ea438f8112ca05d62547105bf0aea59faf5bede6eeb7f0c89b7b`  
		Last Modified: Thu, 16 Oct 2025 18:54:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a6c0f3cdd16775f141e60465fe3fc079324e7475e94e4554a0f5eb624373eb`  
		Last Modified: Thu, 16 Oct 2025 18:54:15 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0388478724d63084d17671a04f1a784f3172e8d947c415834ae56cd6a9c3ea39`  
		Last Modified: Thu, 16 Oct 2025 18:54:15 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f69c8958d0cb8ecb41651e54d4dae645e8fc91a98496c92d56c3cc43cde2ac31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad7ddab7e37c5f9fa97a2b0f392be221f9962a239a6957782aadfcaa3a30b9a`

```dockerfile
```

-	Layers:
	-	`sha256:620f540e54216c95542ee6d03fc3f97c65c4f1ae04ddbb860bd9db29b0cce518`  
		Last Modified: Thu, 16 Oct 2025 21:49:20 GMT  
		Size: 25.3 KB (25274 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.7` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4ab19fe31703cc6c6646b7c42b9496fd2d6c4412e98e604c9d0ca37305f89607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (192984036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17752078ced3c015a86b8e789ef633a00e0347222c3a268caba3564b7fbebfb`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 16 Oct 2025 16:06:54 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 16 Oct 2025 16:06:54 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
ARG REPO_CHANNEL=stable
# Thu, 16 Oct 2025 16:06:54 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 16 Oct 2025 16:06:54 GMT
ARG VERSION=25.3.7.194
# Thu, 16 Oct 2025 16:06:54 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.7.194 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.7.194 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.7.194 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
ENV LANG=en_US.UTF-8
# Thu, 16 Oct 2025 16:06:54 GMT
ENV TZ=UTC
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.7.194 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 16 Oct 2025 16:06:54 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 16 Oct 2025 16:06:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 16 Oct 2025 16:06:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82537f702d38bef03492d1fc7bc9a15b15911182131d228b0fb39109e5bc3e53`  
		Last Modified: Thu, 16 Oct 2025 18:54:14 GMT  
		Size: 7.1 MB (7127250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe969a13317c5499c4d9f6c2ebbf88eac62c37d993df0002164b38b840306be`  
		Last Modified: Thu, 16 Oct 2025 18:55:00 GMT  
		Size: 157.6 MB (157603435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa762f1f7a11ed6e49ae25702c163396439725b27d727cf4d4c744f1e255b633`  
		Last Modified: Thu, 16 Oct 2025 18:54:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cbace4950e6ae8dc79f450c7b858c8753f4f94da5084c90582a8922916e64b`  
		Last Modified: Thu, 16 Oct 2025 18:54:13 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e6befd2db4b3f3139835f321a9f87074650287eac9742af2685b6fe54c8110`  
		Last Modified: Thu, 16 Oct 2025 18:54:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d6b9620edc1e68084fb4bc2eff805a4f72038aad5fed5ebda6135cf259803f`  
		Last Modified: Thu, 16 Oct 2025 18:54:13 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a966db524229a385c17f7ed623a63c2858dde005faab2c7a545e05d057742be`  
		Last Modified: Thu, 16 Oct 2025 18:54:13 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8cf3656994b42d6ab1f0cbdc5d5e49e9c4081cb76395efd3fd5ef35edf72ac86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f55141ed97091926b245679eec0d674dbf23f9573e097f1d182ade60d5a5cdb`

```dockerfile
```

-	Layers:
	-	`sha256:ec6ec35284eed9b262bcab8c510ff0aa5a33eb26663221514e3c8fc53c32a82b`  
		Last Modified: Thu, 16 Oct 2025 21:49:24 GMT  
		Size: 25.5 KB (25462 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.7-jammy`

```console
$ docker pull clickhouse@sha256:e4fd5d9c36120b531ee62f3c550525d214cbaafe40181d207f5ecad1142d7650
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.7-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:e3fb656126491239d39ea97b91a562f221ca9167774475fb304d69885773a9d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.5 MB (205502138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d0e165e2f132d96906ab0b36c9f0193d2599234560e5a8f3468eb68193f86d3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 16 Oct 2025 16:06:54 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 16 Oct 2025 16:06:54 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
ARG REPO_CHANNEL=stable
# Thu, 16 Oct 2025 16:06:54 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 16 Oct 2025 16:06:54 GMT
ARG VERSION=25.3.7.194
# Thu, 16 Oct 2025 16:06:54 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.7.194 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.7.194 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.7.194 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
ENV LANG=en_US.UTF-8
# Thu, 16 Oct 2025 16:06:54 GMT
ENV TZ=UTC
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.7.194 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 16 Oct 2025 16:06:54 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 16 Oct 2025 16:06:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 16 Oct 2025 16:06:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4201bedd3b8f4da93c07aee6fa701d1c014f1c5fdc9038d4c9fc54d3fed3fd16`  
		Last Modified: Thu, 16 Oct 2025 18:54:16 GMT  
		Size: 7.2 MB (7151577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20b311e6ac5989423d05f047ee00c9bc6462aa971d874c5e0a966c9a31fcc03`  
		Last Modified: Thu, 16 Oct 2025 19:11:04 GMT  
		Size: 167.9 MB (167943491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1389958a7c4e44693b1136e775ff65b33a4e6fc8999a8d45c9ced4ba73a29b`  
		Last Modified: Thu, 16 Oct 2025 18:54:15 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dd9b6984c1652bd62ab70663ae49d76634bab8b7798c83a8681ea5ad6bbc36`  
		Last Modified: Thu, 16 Oct 2025 18:54:16 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735c0026b584ea438f8112ca05d62547105bf0aea59faf5bede6eeb7f0c89b7b`  
		Last Modified: Thu, 16 Oct 2025 18:54:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a6c0f3cdd16775f141e60465fe3fc079324e7475e94e4554a0f5eb624373eb`  
		Last Modified: Thu, 16 Oct 2025 18:54:15 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0388478724d63084d17671a04f1a784f3172e8d947c415834ae56cd6a9c3ea39`  
		Last Modified: Thu, 16 Oct 2025 18:54:15 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.7-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f69c8958d0cb8ecb41651e54d4dae645e8fc91a98496c92d56c3cc43cde2ac31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad7ddab7e37c5f9fa97a2b0f392be221f9962a239a6957782aadfcaa3a30b9a`

```dockerfile
```

-	Layers:
	-	`sha256:620f540e54216c95542ee6d03fc3f97c65c4f1ae04ddbb860bd9db29b0cce518`  
		Last Modified: Thu, 16 Oct 2025 21:49:20 GMT  
		Size: 25.3 KB (25274 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.7-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4ab19fe31703cc6c6646b7c42b9496fd2d6c4412e98e604c9d0ca37305f89607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (192984036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17752078ced3c015a86b8e789ef633a00e0347222c3a268caba3564b7fbebfb`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 16 Oct 2025 16:06:54 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 16 Oct 2025 16:06:54 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
ARG REPO_CHANNEL=stable
# Thu, 16 Oct 2025 16:06:54 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 16 Oct 2025 16:06:54 GMT
ARG VERSION=25.3.7.194
# Thu, 16 Oct 2025 16:06:54 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.7.194 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.7.194 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.7.194 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
ENV LANG=en_US.UTF-8
# Thu, 16 Oct 2025 16:06:54 GMT
ENV TZ=UTC
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.7.194 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 16 Oct 2025 16:06:54 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 16 Oct 2025 16:06:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 16 Oct 2025 16:06:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82537f702d38bef03492d1fc7bc9a15b15911182131d228b0fb39109e5bc3e53`  
		Last Modified: Thu, 16 Oct 2025 18:54:14 GMT  
		Size: 7.1 MB (7127250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe969a13317c5499c4d9f6c2ebbf88eac62c37d993df0002164b38b840306be`  
		Last Modified: Thu, 16 Oct 2025 18:55:00 GMT  
		Size: 157.6 MB (157603435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa762f1f7a11ed6e49ae25702c163396439725b27d727cf4d4c744f1e255b633`  
		Last Modified: Thu, 16 Oct 2025 18:54:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cbace4950e6ae8dc79f450c7b858c8753f4f94da5084c90582a8922916e64b`  
		Last Modified: Thu, 16 Oct 2025 18:54:13 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e6befd2db4b3f3139835f321a9f87074650287eac9742af2685b6fe54c8110`  
		Last Modified: Thu, 16 Oct 2025 18:54:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d6b9620edc1e68084fb4bc2eff805a4f72038aad5fed5ebda6135cf259803f`  
		Last Modified: Thu, 16 Oct 2025 18:54:13 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a966db524229a385c17f7ed623a63c2858dde005faab2c7a545e05d057742be`  
		Last Modified: Thu, 16 Oct 2025 18:54:13 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.7-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8cf3656994b42d6ab1f0cbdc5d5e49e9c4081cb76395efd3fd5ef35edf72ac86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f55141ed97091926b245679eec0d674dbf23f9573e097f1d182ade60d5a5cdb`

```dockerfile
```

-	Layers:
	-	`sha256:ec6ec35284eed9b262bcab8c510ff0aa5a33eb26663221514e3c8fc53c32a82b`  
		Last Modified: Thu, 16 Oct 2025 21:49:24 GMT  
		Size: 25.5 KB (25462 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.7.194`

```console
$ docker pull clickhouse@sha256:e4fd5d9c36120b531ee62f3c550525d214cbaafe40181d207f5ecad1142d7650
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.7.194` - linux; amd64

```console
$ docker pull clickhouse@sha256:e3fb656126491239d39ea97b91a562f221ca9167774475fb304d69885773a9d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.5 MB (205502138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d0e165e2f132d96906ab0b36c9f0193d2599234560e5a8f3468eb68193f86d3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 16 Oct 2025 16:06:54 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 16 Oct 2025 16:06:54 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
ARG REPO_CHANNEL=stable
# Thu, 16 Oct 2025 16:06:54 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 16 Oct 2025 16:06:54 GMT
ARG VERSION=25.3.7.194
# Thu, 16 Oct 2025 16:06:54 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.7.194 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.7.194 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.7.194 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
ENV LANG=en_US.UTF-8
# Thu, 16 Oct 2025 16:06:54 GMT
ENV TZ=UTC
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.7.194 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 16 Oct 2025 16:06:54 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 16 Oct 2025 16:06:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 16 Oct 2025 16:06:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4201bedd3b8f4da93c07aee6fa701d1c014f1c5fdc9038d4c9fc54d3fed3fd16`  
		Last Modified: Thu, 16 Oct 2025 18:54:16 GMT  
		Size: 7.2 MB (7151577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20b311e6ac5989423d05f047ee00c9bc6462aa971d874c5e0a966c9a31fcc03`  
		Last Modified: Thu, 16 Oct 2025 19:11:04 GMT  
		Size: 167.9 MB (167943491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1389958a7c4e44693b1136e775ff65b33a4e6fc8999a8d45c9ced4ba73a29b`  
		Last Modified: Thu, 16 Oct 2025 18:54:15 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dd9b6984c1652bd62ab70663ae49d76634bab8b7798c83a8681ea5ad6bbc36`  
		Last Modified: Thu, 16 Oct 2025 18:54:16 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735c0026b584ea438f8112ca05d62547105bf0aea59faf5bede6eeb7f0c89b7b`  
		Last Modified: Thu, 16 Oct 2025 18:54:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a6c0f3cdd16775f141e60465fe3fc079324e7475e94e4554a0f5eb624373eb`  
		Last Modified: Thu, 16 Oct 2025 18:54:15 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0388478724d63084d17671a04f1a784f3172e8d947c415834ae56cd6a9c3ea39`  
		Last Modified: Thu, 16 Oct 2025 18:54:15 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.7.194` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f69c8958d0cb8ecb41651e54d4dae645e8fc91a98496c92d56c3cc43cde2ac31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad7ddab7e37c5f9fa97a2b0f392be221f9962a239a6957782aadfcaa3a30b9a`

```dockerfile
```

-	Layers:
	-	`sha256:620f540e54216c95542ee6d03fc3f97c65c4f1ae04ddbb860bd9db29b0cce518`  
		Last Modified: Thu, 16 Oct 2025 21:49:20 GMT  
		Size: 25.3 KB (25274 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.7.194` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4ab19fe31703cc6c6646b7c42b9496fd2d6c4412e98e604c9d0ca37305f89607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (192984036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17752078ced3c015a86b8e789ef633a00e0347222c3a268caba3564b7fbebfb`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 16 Oct 2025 16:06:54 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 16 Oct 2025 16:06:54 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
ARG REPO_CHANNEL=stable
# Thu, 16 Oct 2025 16:06:54 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 16 Oct 2025 16:06:54 GMT
ARG VERSION=25.3.7.194
# Thu, 16 Oct 2025 16:06:54 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.7.194 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.7.194 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.7.194 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
ENV LANG=en_US.UTF-8
# Thu, 16 Oct 2025 16:06:54 GMT
ENV TZ=UTC
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.7.194 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 16 Oct 2025 16:06:54 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 16 Oct 2025 16:06:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 16 Oct 2025 16:06:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82537f702d38bef03492d1fc7bc9a15b15911182131d228b0fb39109e5bc3e53`  
		Last Modified: Thu, 16 Oct 2025 18:54:14 GMT  
		Size: 7.1 MB (7127250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe969a13317c5499c4d9f6c2ebbf88eac62c37d993df0002164b38b840306be`  
		Last Modified: Thu, 16 Oct 2025 18:55:00 GMT  
		Size: 157.6 MB (157603435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa762f1f7a11ed6e49ae25702c163396439725b27d727cf4d4c744f1e255b633`  
		Last Modified: Thu, 16 Oct 2025 18:54:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cbace4950e6ae8dc79f450c7b858c8753f4f94da5084c90582a8922916e64b`  
		Last Modified: Thu, 16 Oct 2025 18:54:13 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e6befd2db4b3f3139835f321a9f87074650287eac9742af2685b6fe54c8110`  
		Last Modified: Thu, 16 Oct 2025 18:54:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d6b9620edc1e68084fb4bc2eff805a4f72038aad5fed5ebda6135cf259803f`  
		Last Modified: Thu, 16 Oct 2025 18:54:13 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a966db524229a385c17f7ed623a63c2858dde005faab2c7a545e05d057742be`  
		Last Modified: Thu, 16 Oct 2025 18:54:13 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.7.194` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8cf3656994b42d6ab1f0cbdc5d5e49e9c4081cb76395efd3fd5ef35edf72ac86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f55141ed97091926b245679eec0d674dbf23f9573e097f1d182ade60d5a5cdb`

```dockerfile
```

-	Layers:
	-	`sha256:ec6ec35284eed9b262bcab8c510ff0aa5a33eb26663221514e3c8fc53c32a82b`  
		Last Modified: Thu, 16 Oct 2025 21:49:24 GMT  
		Size: 25.5 KB (25462 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.7.194-jammy`

```console
$ docker pull clickhouse@sha256:e4fd5d9c36120b531ee62f3c550525d214cbaafe40181d207f5ecad1142d7650
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.7.194-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:e3fb656126491239d39ea97b91a562f221ca9167774475fb304d69885773a9d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.5 MB (205502138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d0e165e2f132d96906ab0b36c9f0193d2599234560e5a8f3468eb68193f86d3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 16 Oct 2025 16:06:54 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 16 Oct 2025 16:06:54 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
ARG REPO_CHANNEL=stable
# Thu, 16 Oct 2025 16:06:54 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 16 Oct 2025 16:06:54 GMT
ARG VERSION=25.3.7.194
# Thu, 16 Oct 2025 16:06:54 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.7.194 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.7.194 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.7.194 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
ENV LANG=en_US.UTF-8
# Thu, 16 Oct 2025 16:06:54 GMT
ENV TZ=UTC
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.7.194 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 16 Oct 2025 16:06:54 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 16 Oct 2025 16:06:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 16 Oct 2025 16:06:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4201bedd3b8f4da93c07aee6fa701d1c014f1c5fdc9038d4c9fc54d3fed3fd16`  
		Last Modified: Thu, 16 Oct 2025 18:54:16 GMT  
		Size: 7.2 MB (7151577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20b311e6ac5989423d05f047ee00c9bc6462aa971d874c5e0a966c9a31fcc03`  
		Last Modified: Thu, 16 Oct 2025 19:11:04 GMT  
		Size: 167.9 MB (167943491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1389958a7c4e44693b1136e775ff65b33a4e6fc8999a8d45c9ced4ba73a29b`  
		Last Modified: Thu, 16 Oct 2025 18:54:15 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dd9b6984c1652bd62ab70663ae49d76634bab8b7798c83a8681ea5ad6bbc36`  
		Last Modified: Thu, 16 Oct 2025 18:54:16 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735c0026b584ea438f8112ca05d62547105bf0aea59faf5bede6eeb7f0c89b7b`  
		Last Modified: Thu, 16 Oct 2025 18:54:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a6c0f3cdd16775f141e60465fe3fc079324e7475e94e4554a0f5eb624373eb`  
		Last Modified: Thu, 16 Oct 2025 18:54:15 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0388478724d63084d17671a04f1a784f3172e8d947c415834ae56cd6a9c3ea39`  
		Last Modified: Thu, 16 Oct 2025 18:54:15 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.7.194-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f69c8958d0cb8ecb41651e54d4dae645e8fc91a98496c92d56c3cc43cde2ac31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad7ddab7e37c5f9fa97a2b0f392be221f9962a239a6957782aadfcaa3a30b9a`

```dockerfile
```

-	Layers:
	-	`sha256:620f540e54216c95542ee6d03fc3f97c65c4f1ae04ddbb860bd9db29b0cce518`  
		Last Modified: Thu, 16 Oct 2025 21:49:20 GMT  
		Size: 25.3 KB (25274 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.7.194-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4ab19fe31703cc6c6646b7c42b9496fd2d6c4412e98e604c9d0ca37305f89607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (192984036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17752078ced3c015a86b8e789ef633a00e0347222c3a268caba3564b7fbebfb`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 16 Oct 2025 16:06:54 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 16 Oct 2025 16:06:54 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
ARG REPO_CHANNEL=stable
# Thu, 16 Oct 2025 16:06:54 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 16 Oct 2025 16:06:54 GMT
ARG VERSION=25.3.7.194
# Thu, 16 Oct 2025 16:06:54 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.7.194 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.7.194 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.7.194 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
ENV LANG=en_US.UTF-8
# Thu, 16 Oct 2025 16:06:54 GMT
ENV TZ=UTC
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.7.194 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 16 Oct 2025 16:06:54 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 16 Oct 2025 16:06:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 16 Oct 2025 16:06:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82537f702d38bef03492d1fc7bc9a15b15911182131d228b0fb39109e5bc3e53`  
		Last Modified: Thu, 16 Oct 2025 18:54:14 GMT  
		Size: 7.1 MB (7127250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe969a13317c5499c4d9f6c2ebbf88eac62c37d993df0002164b38b840306be`  
		Last Modified: Thu, 16 Oct 2025 18:55:00 GMT  
		Size: 157.6 MB (157603435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa762f1f7a11ed6e49ae25702c163396439725b27d727cf4d4c744f1e255b633`  
		Last Modified: Thu, 16 Oct 2025 18:54:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cbace4950e6ae8dc79f450c7b858c8753f4f94da5084c90582a8922916e64b`  
		Last Modified: Thu, 16 Oct 2025 18:54:13 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e6befd2db4b3f3139835f321a9f87074650287eac9742af2685b6fe54c8110`  
		Last Modified: Thu, 16 Oct 2025 18:54:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d6b9620edc1e68084fb4bc2eff805a4f72038aad5fed5ebda6135cf259803f`  
		Last Modified: Thu, 16 Oct 2025 18:54:13 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a966db524229a385c17f7ed623a63c2858dde005faab2c7a545e05d057742be`  
		Last Modified: Thu, 16 Oct 2025 18:54:13 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.7.194-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8cf3656994b42d6ab1f0cbdc5d5e49e9c4081cb76395efd3fd5ef35edf72ac86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f55141ed97091926b245679eec0d674dbf23f9573e097f1d182ade60d5a5cdb`

```dockerfile
```

-	Layers:
	-	`sha256:ec6ec35284eed9b262bcab8c510ff0aa5a33eb26663221514e3c8fc53c32a82b`  
		Last Modified: Thu, 16 Oct 2025 21:49:24 GMT  
		Size: 25.5 KB (25462 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.7`

```console
$ docker pull clickhouse@sha256:96fab997c08759c52195bc9ac9059a9f3b92cdd1f90dc952888256987b303ab3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.7` - linux; amd64

```console
$ docker pull clickhouse@sha256:f09acbe73568c90b64c1655b096e7739bb1407cbeb969cf8c039c4c30c3ebbca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.0 MB (221956924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025c3823ab1cd6d5af6d33bd6079d3fcb22c24a89c081d6b0c7f2352d2e910c0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 16 Oct 2025 16:06:54 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 16 Oct 2025 16:06:54 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
ARG REPO_CHANNEL=stable
# Thu, 16 Oct 2025 16:06:54 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 16 Oct 2025 16:06:54 GMT
ARG VERSION=25.7.8.71
# Thu, 16 Oct 2025 16:06:54 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.8.71 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.8.71 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.8.71 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
ENV LANG=en_US.UTF-8
# Thu, 16 Oct 2025 16:06:54 GMT
ENV TZ=UTC
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.8.71 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 16 Oct 2025 16:06:54 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 16 Oct 2025 16:06:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 16 Oct 2025 16:06:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7822052672b76ac2453a86fad01735f8c5f52ac1e874ba452b112cfc263cfd18`  
		Last Modified: Thu, 16 Oct 2025 18:53:14 GMT  
		Size: 7.6 MB (7598419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a761d06a6b266c6afbab0c22d5338ccb4cf19fb77f1a21d902aec5e2f2e6c6c1`  
		Last Modified: Thu, 16 Oct 2025 18:53:50 GMT  
		Size: 184.0 MB (183951662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d05f659f3ca72f37f46b6309b2a324fa3d96e88f34d92c07aa82bfdfc79962e`  
		Last Modified: Thu, 16 Oct 2025 18:53:14 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b5a967c79ce3cb41bc4e7d4c7eabaf802e45f103096b5a67c528b54dff9d1aa`  
		Last Modified: Thu, 16 Oct 2025 18:53:14 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0542bf24761eea9f94a2c2e1c4a5430d14b1406d7495e80c714626ab14234863`  
		Last Modified: Thu, 16 Oct 2025 18:53:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632d93909e65c7234abde86ea1f9e5631295c741fecdcb62738ed3f9d93a38aa`  
		Last Modified: Thu, 16 Oct 2025 18:53:14 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9663a44466508c32bf34b7862dfc667ed7d02312b48ad9ac0967a3e55a42c64e`  
		Last Modified: Thu, 16 Oct 2025 18:53:14 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:003a59f49cf4ca8c5a200e9c4b373cdb84a3ab10282547738d1a0ed55885346a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd74a84030e0326efbafe2d861d2229f677a536f20cc788f13a37a1e1c3cd98`

```dockerfile
```

-	Layers:
	-	`sha256:fbb88c3ac9e704a4487b1c7b6cad6b4a8c92cdc2d13a690d56a67a1401052a7c`  
		Last Modified: Thu, 16 Oct 2025 21:49:38 GMT  
		Size: 25.5 KB (25461 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.7` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:ec7a092fc3f5b1aa5be0c7f613b483db4dac61cba2687d1e80e83d6050e76ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.9 MB (207932780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6ce372f742631d92e894d4823869df3a1abbbe4e9fdb9da706a12ec0573396f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 16 Oct 2025 16:06:54 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 16 Oct 2025 16:06:54 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
ARG REPO_CHANNEL=stable
# Thu, 16 Oct 2025 16:06:54 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 16 Oct 2025 16:06:54 GMT
ARG VERSION=25.7.8.71
# Thu, 16 Oct 2025 16:06:54 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.8.71 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.8.71 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.8.71 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
ENV LANG=en_US.UTF-8
# Thu, 16 Oct 2025 16:06:54 GMT
ENV TZ=UTC
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.8.71 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 16 Oct 2025 16:06:54 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 16 Oct 2025 16:06:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 16 Oct 2025 16:06:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842d5f71add3462bbc7c1ce16dc942e42b86e6c490409d5e991df8de5fb3603f`  
		Last Modified: Thu, 16 Oct 2025 18:54:15 GMT  
		Size: 7.6 MB (7576754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7f9190289fc1e12edba35673c10cf935ed01de15e516dcc77766a20096052e`  
		Last Modified: Thu, 16 Oct 2025 21:50:07 GMT  
		Size: 172.1 MB (172102892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac106452ef670c779af11ce2a7a64bcb58bc1ecfbab1b8889772cbdecbdf59a`  
		Last Modified: Thu, 16 Oct 2025 18:54:13 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a1a08829fd7e38a68bf67a81eeca3e12f781e448c68363c1b7e91e585d8af9`  
		Last Modified: Thu, 16 Oct 2025 18:54:13 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709484672aeff06b6aa3adc8eb0a3a72ff4ec25c06c862a465eebde8af848f42`  
		Last Modified: Thu, 16 Oct 2025 18:54:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a1b9dc478441ec2500fdae3044a0faea06565a7e12b62a5745f142c6f1ab24`  
		Last Modified: Thu, 16 Oct 2025 18:54:14 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89f200c9fa1f8827fc73e090375b44f3810f6f4e013069f820cf51864176773`  
		Last Modified: Thu, 16 Oct 2025 18:54:14 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5434cf9abad6e2d8390cb54a3d245ca27c4d2af06c4975fe8cd917956a432286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d684efdca1960f0e09a3e0d50d7bbf69822c3dff63adb7faecb105ea06371fa5`

```dockerfile
```

-	Layers:
	-	`sha256:e94144569a80c2726b2bab54438a398bea0e589313368b1dbb6af72306b19815`  
		Last Modified: Thu, 16 Oct 2025 21:49:42 GMT  
		Size: 25.6 KB (25649 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.7-jammy`

```console
$ docker pull clickhouse@sha256:96fab997c08759c52195bc9ac9059a9f3b92cdd1f90dc952888256987b303ab3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.7-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:f09acbe73568c90b64c1655b096e7739bb1407cbeb969cf8c039c4c30c3ebbca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.0 MB (221956924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025c3823ab1cd6d5af6d33bd6079d3fcb22c24a89c081d6b0c7f2352d2e910c0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 16 Oct 2025 16:06:54 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 16 Oct 2025 16:06:54 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
ARG REPO_CHANNEL=stable
# Thu, 16 Oct 2025 16:06:54 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 16 Oct 2025 16:06:54 GMT
ARG VERSION=25.7.8.71
# Thu, 16 Oct 2025 16:06:54 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.8.71 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.8.71 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.8.71 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
ENV LANG=en_US.UTF-8
# Thu, 16 Oct 2025 16:06:54 GMT
ENV TZ=UTC
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.8.71 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 16 Oct 2025 16:06:54 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 16 Oct 2025 16:06:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 16 Oct 2025 16:06:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7822052672b76ac2453a86fad01735f8c5f52ac1e874ba452b112cfc263cfd18`  
		Last Modified: Thu, 16 Oct 2025 18:53:14 GMT  
		Size: 7.6 MB (7598419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a761d06a6b266c6afbab0c22d5338ccb4cf19fb77f1a21d902aec5e2f2e6c6c1`  
		Last Modified: Thu, 16 Oct 2025 18:53:50 GMT  
		Size: 184.0 MB (183951662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d05f659f3ca72f37f46b6309b2a324fa3d96e88f34d92c07aa82bfdfc79962e`  
		Last Modified: Thu, 16 Oct 2025 18:53:14 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b5a967c79ce3cb41bc4e7d4c7eabaf802e45f103096b5a67c528b54dff9d1aa`  
		Last Modified: Thu, 16 Oct 2025 18:53:14 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0542bf24761eea9f94a2c2e1c4a5430d14b1406d7495e80c714626ab14234863`  
		Last Modified: Thu, 16 Oct 2025 18:53:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632d93909e65c7234abde86ea1f9e5631295c741fecdcb62738ed3f9d93a38aa`  
		Last Modified: Thu, 16 Oct 2025 18:53:14 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9663a44466508c32bf34b7862dfc667ed7d02312b48ad9ac0967a3e55a42c64e`  
		Last Modified: Thu, 16 Oct 2025 18:53:14 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:003a59f49cf4ca8c5a200e9c4b373cdb84a3ab10282547738d1a0ed55885346a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd74a84030e0326efbafe2d861d2229f677a536f20cc788f13a37a1e1c3cd98`

```dockerfile
```

-	Layers:
	-	`sha256:fbb88c3ac9e704a4487b1c7b6cad6b4a8c92cdc2d13a690d56a67a1401052a7c`  
		Last Modified: Thu, 16 Oct 2025 21:49:38 GMT  
		Size: 25.5 KB (25461 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.7-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:ec7a092fc3f5b1aa5be0c7f613b483db4dac61cba2687d1e80e83d6050e76ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.9 MB (207932780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6ce372f742631d92e894d4823869df3a1abbbe4e9fdb9da706a12ec0573396f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 16 Oct 2025 16:06:54 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 16 Oct 2025 16:06:54 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
ARG REPO_CHANNEL=stable
# Thu, 16 Oct 2025 16:06:54 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 16 Oct 2025 16:06:54 GMT
ARG VERSION=25.7.8.71
# Thu, 16 Oct 2025 16:06:54 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.8.71 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.8.71 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.8.71 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
ENV LANG=en_US.UTF-8
# Thu, 16 Oct 2025 16:06:54 GMT
ENV TZ=UTC
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.8.71 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 16 Oct 2025 16:06:54 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 16 Oct 2025 16:06:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 16 Oct 2025 16:06:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842d5f71add3462bbc7c1ce16dc942e42b86e6c490409d5e991df8de5fb3603f`  
		Last Modified: Thu, 16 Oct 2025 18:54:15 GMT  
		Size: 7.6 MB (7576754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7f9190289fc1e12edba35673c10cf935ed01de15e516dcc77766a20096052e`  
		Last Modified: Thu, 16 Oct 2025 21:50:07 GMT  
		Size: 172.1 MB (172102892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac106452ef670c779af11ce2a7a64bcb58bc1ecfbab1b8889772cbdecbdf59a`  
		Last Modified: Thu, 16 Oct 2025 18:54:13 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a1a08829fd7e38a68bf67a81eeca3e12f781e448c68363c1b7e91e585d8af9`  
		Last Modified: Thu, 16 Oct 2025 18:54:13 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709484672aeff06b6aa3adc8eb0a3a72ff4ec25c06c862a465eebde8af848f42`  
		Last Modified: Thu, 16 Oct 2025 18:54:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a1b9dc478441ec2500fdae3044a0faea06565a7e12b62a5745f142c6f1ab24`  
		Last Modified: Thu, 16 Oct 2025 18:54:14 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89f200c9fa1f8827fc73e090375b44f3810f6f4e013069f820cf51864176773`  
		Last Modified: Thu, 16 Oct 2025 18:54:14 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5434cf9abad6e2d8390cb54a3d245ca27c4d2af06c4975fe8cd917956a432286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d684efdca1960f0e09a3e0d50d7bbf69822c3dff63adb7faecb105ea06371fa5`

```dockerfile
```

-	Layers:
	-	`sha256:e94144569a80c2726b2bab54438a398bea0e589313368b1dbb6af72306b19815`  
		Last Modified: Thu, 16 Oct 2025 21:49:42 GMT  
		Size: 25.6 KB (25649 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.7.8`

```console
$ docker pull clickhouse@sha256:96fab997c08759c52195bc9ac9059a9f3b92cdd1f90dc952888256987b303ab3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.7.8` - linux; amd64

```console
$ docker pull clickhouse@sha256:f09acbe73568c90b64c1655b096e7739bb1407cbeb969cf8c039c4c30c3ebbca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.0 MB (221956924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025c3823ab1cd6d5af6d33bd6079d3fcb22c24a89c081d6b0c7f2352d2e910c0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 16 Oct 2025 16:06:54 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 16 Oct 2025 16:06:54 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
ARG REPO_CHANNEL=stable
# Thu, 16 Oct 2025 16:06:54 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 16 Oct 2025 16:06:54 GMT
ARG VERSION=25.7.8.71
# Thu, 16 Oct 2025 16:06:54 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.8.71 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.8.71 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.8.71 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
ENV LANG=en_US.UTF-8
# Thu, 16 Oct 2025 16:06:54 GMT
ENV TZ=UTC
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.8.71 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 16 Oct 2025 16:06:54 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 16 Oct 2025 16:06:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 16 Oct 2025 16:06:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7822052672b76ac2453a86fad01735f8c5f52ac1e874ba452b112cfc263cfd18`  
		Last Modified: Thu, 16 Oct 2025 18:53:14 GMT  
		Size: 7.6 MB (7598419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a761d06a6b266c6afbab0c22d5338ccb4cf19fb77f1a21d902aec5e2f2e6c6c1`  
		Last Modified: Thu, 16 Oct 2025 18:53:50 GMT  
		Size: 184.0 MB (183951662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d05f659f3ca72f37f46b6309b2a324fa3d96e88f34d92c07aa82bfdfc79962e`  
		Last Modified: Thu, 16 Oct 2025 18:53:14 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b5a967c79ce3cb41bc4e7d4c7eabaf802e45f103096b5a67c528b54dff9d1aa`  
		Last Modified: Thu, 16 Oct 2025 18:53:14 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0542bf24761eea9f94a2c2e1c4a5430d14b1406d7495e80c714626ab14234863`  
		Last Modified: Thu, 16 Oct 2025 18:53:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632d93909e65c7234abde86ea1f9e5631295c741fecdcb62738ed3f9d93a38aa`  
		Last Modified: Thu, 16 Oct 2025 18:53:14 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9663a44466508c32bf34b7862dfc667ed7d02312b48ad9ac0967a3e55a42c64e`  
		Last Modified: Thu, 16 Oct 2025 18:53:14 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:003a59f49cf4ca8c5a200e9c4b373cdb84a3ab10282547738d1a0ed55885346a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd74a84030e0326efbafe2d861d2229f677a536f20cc788f13a37a1e1c3cd98`

```dockerfile
```

-	Layers:
	-	`sha256:fbb88c3ac9e704a4487b1c7b6cad6b4a8c92cdc2d13a690d56a67a1401052a7c`  
		Last Modified: Thu, 16 Oct 2025 21:49:38 GMT  
		Size: 25.5 KB (25461 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.7.8` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:ec7a092fc3f5b1aa5be0c7f613b483db4dac61cba2687d1e80e83d6050e76ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.9 MB (207932780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6ce372f742631d92e894d4823869df3a1abbbe4e9fdb9da706a12ec0573396f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 16 Oct 2025 16:06:54 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 16 Oct 2025 16:06:54 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
ARG REPO_CHANNEL=stable
# Thu, 16 Oct 2025 16:06:54 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 16 Oct 2025 16:06:54 GMT
ARG VERSION=25.7.8.71
# Thu, 16 Oct 2025 16:06:54 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.8.71 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.8.71 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.8.71 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
ENV LANG=en_US.UTF-8
# Thu, 16 Oct 2025 16:06:54 GMT
ENV TZ=UTC
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.8.71 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 16 Oct 2025 16:06:54 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 16 Oct 2025 16:06:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 16 Oct 2025 16:06:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842d5f71add3462bbc7c1ce16dc942e42b86e6c490409d5e991df8de5fb3603f`  
		Last Modified: Thu, 16 Oct 2025 18:54:15 GMT  
		Size: 7.6 MB (7576754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7f9190289fc1e12edba35673c10cf935ed01de15e516dcc77766a20096052e`  
		Last Modified: Thu, 16 Oct 2025 21:50:07 GMT  
		Size: 172.1 MB (172102892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac106452ef670c779af11ce2a7a64bcb58bc1ecfbab1b8889772cbdecbdf59a`  
		Last Modified: Thu, 16 Oct 2025 18:54:13 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a1a08829fd7e38a68bf67a81eeca3e12f781e448c68363c1b7e91e585d8af9`  
		Last Modified: Thu, 16 Oct 2025 18:54:13 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709484672aeff06b6aa3adc8eb0a3a72ff4ec25c06c862a465eebde8af848f42`  
		Last Modified: Thu, 16 Oct 2025 18:54:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a1b9dc478441ec2500fdae3044a0faea06565a7e12b62a5745f142c6f1ab24`  
		Last Modified: Thu, 16 Oct 2025 18:54:14 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89f200c9fa1f8827fc73e090375b44f3810f6f4e013069f820cf51864176773`  
		Last Modified: Thu, 16 Oct 2025 18:54:14 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5434cf9abad6e2d8390cb54a3d245ca27c4d2af06c4975fe8cd917956a432286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d684efdca1960f0e09a3e0d50d7bbf69822c3dff63adb7faecb105ea06371fa5`

```dockerfile
```

-	Layers:
	-	`sha256:e94144569a80c2726b2bab54438a398bea0e589313368b1dbb6af72306b19815`  
		Last Modified: Thu, 16 Oct 2025 21:49:42 GMT  
		Size: 25.6 KB (25649 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.7.8-jammy`

```console
$ docker pull clickhouse@sha256:96fab997c08759c52195bc9ac9059a9f3b92cdd1f90dc952888256987b303ab3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.7.8-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:f09acbe73568c90b64c1655b096e7739bb1407cbeb969cf8c039c4c30c3ebbca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.0 MB (221956924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025c3823ab1cd6d5af6d33bd6079d3fcb22c24a89c081d6b0c7f2352d2e910c0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 16 Oct 2025 16:06:54 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 16 Oct 2025 16:06:54 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
ARG REPO_CHANNEL=stable
# Thu, 16 Oct 2025 16:06:54 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 16 Oct 2025 16:06:54 GMT
ARG VERSION=25.7.8.71
# Thu, 16 Oct 2025 16:06:54 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.8.71 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.8.71 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.8.71 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
ENV LANG=en_US.UTF-8
# Thu, 16 Oct 2025 16:06:54 GMT
ENV TZ=UTC
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.8.71 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 16 Oct 2025 16:06:54 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 16 Oct 2025 16:06:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 16 Oct 2025 16:06:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7822052672b76ac2453a86fad01735f8c5f52ac1e874ba452b112cfc263cfd18`  
		Last Modified: Thu, 16 Oct 2025 18:53:14 GMT  
		Size: 7.6 MB (7598419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a761d06a6b266c6afbab0c22d5338ccb4cf19fb77f1a21d902aec5e2f2e6c6c1`  
		Last Modified: Thu, 16 Oct 2025 18:53:50 GMT  
		Size: 184.0 MB (183951662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d05f659f3ca72f37f46b6309b2a324fa3d96e88f34d92c07aa82bfdfc79962e`  
		Last Modified: Thu, 16 Oct 2025 18:53:14 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b5a967c79ce3cb41bc4e7d4c7eabaf802e45f103096b5a67c528b54dff9d1aa`  
		Last Modified: Thu, 16 Oct 2025 18:53:14 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0542bf24761eea9f94a2c2e1c4a5430d14b1406d7495e80c714626ab14234863`  
		Last Modified: Thu, 16 Oct 2025 18:53:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632d93909e65c7234abde86ea1f9e5631295c741fecdcb62738ed3f9d93a38aa`  
		Last Modified: Thu, 16 Oct 2025 18:53:14 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9663a44466508c32bf34b7862dfc667ed7d02312b48ad9ac0967a3e55a42c64e`  
		Last Modified: Thu, 16 Oct 2025 18:53:14 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:003a59f49cf4ca8c5a200e9c4b373cdb84a3ab10282547738d1a0ed55885346a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd74a84030e0326efbafe2d861d2229f677a536f20cc788f13a37a1e1c3cd98`

```dockerfile
```

-	Layers:
	-	`sha256:fbb88c3ac9e704a4487b1c7b6cad6b4a8c92cdc2d13a690d56a67a1401052a7c`  
		Last Modified: Thu, 16 Oct 2025 21:49:38 GMT  
		Size: 25.5 KB (25461 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.7.8-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:ec7a092fc3f5b1aa5be0c7f613b483db4dac61cba2687d1e80e83d6050e76ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.9 MB (207932780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6ce372f742631d92e894d4823869df3a1abbbe4e9fdb9da706a12ec0573396f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 16 Oct 2025 16:06:54 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 16 Oct 2025 16:06:54 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
ARG REPO_CHANNEL=stable
# Thu, 16 Oct 2025 16:06:54 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 16 Oct 2025 16:06:54 GMT
ARG VERSION=25.7.8.71
# Thu, 16 Oct 2025 16:06:54 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.8.71 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.8.71 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.8.71 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
ENV LANG=en_US.UTF-8
# Thu, 16 Oct 2025 16:06:54 GMT
ENV TZ=UTC
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.8.71 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 16 Oct 2025 16:06:54 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 16 Oct 2025 16:06:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 16 Oct 2025 16:06:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842d5f71add3462bbc7c1ce16dc942e42b86e6c490409d5e991df8de5fb3603f`  
		Last Modified: Thu, 16 Oct 2025 18:54:15 GMT  
		Size: 7.6 MB (7576754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7f9190289fc1e12edba35673c10cf935ed01de15e516dcc77766a20096052e`  
		Last Modified: Thu, 16 Oct 2025 21:50:07 GMT  
		Size: 172.1 MB (172102892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac106452ef670c779af11ce2a7a64bcb58bc1ecfbab1b8889772cbdecbdf59a`  
		Last Modified: Thu, 16 Oct 2025 18:54:13 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a1a08829fd7e38a68bf67a81eeca3e12f781e448c68363c1b7e91e585d8af9`  
		Last Modified: Thu, 16 Oct 2025 18:54:13 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709484672aeff06b6aa3adc8eb0a3a72ff4ec25c06c862a465eebde8af848f42`  
		Last Modified: Thu, 16 Oct 2025 18:54:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a1b9dc478441ec2500fdae3044a0faea06565a7e12b62a5745f142c6f1ab24`  
		Last Modified: Thu, 16 Oct 2025 18:54:14 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89f200c9fa1f8827fc73e090375b44f3810f6f4e013069f820cf51864176773`  
		Last Modified: Thu, 16 Oct 2025 18:54:14 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5434cf9abad6e2d8390cb54a3d245ca27c4d2af06c4975fe8cd917956a432286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d684efdca1960f0e09a3e0d50d7bbf69822c3dff63adb7faecb105ea06371fa5`

```dockerfile
```

-	Layers:
	-	`sha256:e94144569a80c2726b2bab54438a398bea0e589313368b1dbb6af72306b19815`  
		Last Modified: Thu, 16 Oct 2025 21:49:42 GMT  
		Size: 25.6 KB (25649 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.7.8.71`

```console
$ docker pull clickhouse@sha256:96fab997c08759c52195bc9ac9059a9f3b92cdd1f90dc952888256987b303ab3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.7.8.71` - linux; amd64

```console
$ docker pull clickhouse@sha256:f09acbe73568c90b64c1655b096e7739bb1407cbeb969cf8c039c4c30c3ebbca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.0 MB (221956924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025c3823ab1cd6d5af6d33bd6079d3fcb22c24a89c081d6b0c7f2352d2e910c0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 16 Oct 2025 16:06:54 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 16 Oct 2025 16:06:54 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
ARG REPO_CHANNEL=stable
# Thu, 16 Oct 2025 16:06:54 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 16 Oct 2025 16:06:54 GMT
ARG VERSION=25.7.8.71
# Thu, 16 Oct 2025 16:06:54 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.8.71 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.8.71 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.8.71 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
ENV LANG=en_US.UTF-8
# Thu, 16 Oct 2025 16:06:54 GMT
ENV TZ=UTC
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.8.71 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 16 Oct 2025 16:06:54 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 16 Oct 2025 16:06:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 16 Oct 2025 16:06:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7822052672b76ac2453a86fad01735f8c5f52ac1e874ba452b112cfc263cfd18`  
		Last Modified: Thu, 16 Oct 2025 18:53:14 GMT  
		Size: 7.6 MB (7598419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a761d06a6b266c6afbab0c22d5338ccb4cf19fb77f1a21d902aec5e2f2e6c6c1`  
		Last Modified: Thu, 16 Oct 2025 18:53:50 GMT  
		Size: 184.0 MB (183951662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d05f659f3ca72f37f46b6309b2a324fa3d96e88f34d92c07aa82bfdfc79962e`  
		Last Modified: Thu, 16 Oct 2025 18:53:14 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b5a967c79ce3cb41bc4e7d4c7eabaf802e45f103096b5a67c528b54dff9d1aa`  
		Last Modified: Thu, 16 Oct 2025 18:53:14 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0542bf24761eea9f94a2c2e1c4a5430d14b1406d7495e80c714626ab14234863`  
		Last Modified: Thu, 16 Oct 2025 18:53:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632d93909e65c7234abde86ea1f9e5631295c741fecdcb62738ed3f9d93a38aa`  
		Last Modified: Thu, 16 Oct 2025 18:53:14 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9663a44466508c32bf34b7862dfc667ed7d02312b48ad9ac0967a3e55a42c64e`  
		Last Modified: Thu, 16 Oct 2025 18:53:14 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.8.71` - unknown; unknown

```console
$ docker pull clickhouse@sha256:003a59f49cf4ca8c5a200e9c4b373cdb84a3ab10282547738d1a0ed55885346a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd74a84030e0326efbafe2d861d2229f677a536f20cc788f13a37a1e1c3cd98`

```dockerfile
```

-	Layers:
	-	`sha256:fbb88c3ac9e704a4487b1c7b6cad6b4a8c92cdc2d13a690d56a67a1401052a7c`  
		Last Modified: Thu, 16 Oct 2025 21:49:38 GMT  
		Size: 25.5 KB (25461 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.7.8.71` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:ec7a092fc3f5b1aa5be0c7f613b483db4dac61cba2687d1e80e83d6050e76ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.9 MB (207932780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6ce372f742631d92e894d4823869df3a1abbbe4e9fdb9da706a12ec0573396f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 16 Oct 2025 16:06:54 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 16 Oct 2025 16:06:54 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
ARG REPO_CHANNEL=stable
# Thu, 16 Oct 2025 16:06:54 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 16 Oct 2025 16:06:54 GMT
ARG VERSION=25.7.8.71
# Thu, 16 Oct 2025 16:06:54 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.8.71 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.8.71 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.8.71 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
ENV LANG=en_US.UTF-8
# Thu, 16 Oct 2025 16:06:54 GMT
ENV TZ=UTC
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.8.71 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 16 Oct 2025 16:06:54 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 16 Oct 2025 16:06:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 16 Oct 2025 16:06:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842d5f71add3462bbc7c1ce16dc942e42b86e6c490409d5e991df8de5fb3603f`  
		Last Modified: Thu, 16 Oct 2025 18:54:15 GMT  
		Size: 7.6 MB (7576754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7f9190289fc1e12edba35673c10cf935ed01de15e516dcc77766a20096052e`  
		Last Modified: Thu, 16 Oct 2025 21:50:07 GMT  
		Size: 172.1 MB (172102892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac106452ef670c779af11ce2a7a64bcb58bc1ecfbab1b8889772cbdecbdf59a`  
		Last Modified: Thu, 16 Oct 2025 18:54:13 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a1a08829fd7e38a68bf67a81eeca3e12f781e448c68363c1b7e91e585d8af9`  
		Last Modified: Thu, 16 Oct 2025 18:54:13 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709484672aeff06b6aa3adc8eb0a3a72ff4ec25c06c862a465eebde8af848f42`  
		Last Modified: Thu, 16 Oct 2025 18:54:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a1b9dc478441ec2500fdae3044a0faea06565a7e12b62a5745f142c6f1ab24`  
		Last Modified: Thu, 16 Oct 2025 18:54:14 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89f200c9fa1f8827fc73e090375b44f3810f6f4e013069f820cf51864176773`  
		Last Modified: Thu, 16 Oct 2025 18:54:14 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.8.71` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5434cf9abad6e2d8390cb54a3d245ca27c4d2af06c4975fe8cd917956a432286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d684efdca1960f0e09a3e0d50d7bbf69822c3dff63adb7faecb105ea06371fa5`

```dockerfile
```

-	Layers:
	-	`sha256:e94144569a80c2726b2bab54438a398bea0e589313368b1dbb6af72306b19815`  
		Last Modified: Thu, 16 Oct 2025 21:49:42 GMT  
		Size: 25.6 KB (25649 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.7.8.71-jammy`

```console
$ docker pull clickhouse@sha256:96fab997c08759c52195bc9ac9059a9f3b92cdd1f90dc952888256987b303ab3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.7.8.71-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:f09acbe73568c90b64c1655b096e7739bb1407cbeb969cf8c039c4c30c3ebbca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.0 MB (221956924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025c3823ab1cd6d5af6d33bd6079d3fcb22c24a89c081d6b0c7f2352d2e910c0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 16 Oct 2025 16:06:54 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 16 Oct 2025 16:06:54 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
ARG REPO_CHANNEL=stable
# Thu, 16 Oct 2025 16:06:54 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 16 Oct 2025 16:06:54 GMT
ARG VERSION=25.7.8.71
# Thu, 16 Oct 2025 16:06:54 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.8.71 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.8.71 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.8.71 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
ENV LANG=en_US.UTF-8
# Thu, 16 Oct 2025 16:06:54 GMT
ENV TZ=UTC
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.8.71 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 16 Oct 2025 16:06:54 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 16 Oct 2025 16:06:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 16 Oct 2025 16:06:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7822052672b76ac2453a86fad01735f8c5f52ac1e874ba452b112cfc263cfd18`  
		Last Modified: Thu, 16 Oct 2025 18:53:14 GMT  
		Size: 7.6 MB (7598419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a761d06a6b266c6afbab0c22d5338ccb4cf19fb77f1a21d902aec5e2f2e6c6c1`  
		Last Modified: Thu, 16 Oct 2025 18:53:50 GMT  
		Size: 184.0 MB (183951662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d05f659f3ca72f37f46b6309b2a324fa3d96e88f34d92c07aa82bfdfc79962e`  
		Last Modified: Thu, 16 Oct 2025 18:53:14 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b5a967c79ce3cb41bc4e7d4c7eabaf802e45f103096b5a67c528b54dff9d1aa`  
		Last Modified: Thu, 16 Oct 2025 18:53:14 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0542bf24761eea9f94a2c2e1c4a5430d14b1406d7495e80c714626ab14234863`  
		Last Modified: Thu, 16 Oct 2025 18:53:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632d93909e65c7234abde86ea1f9e5631295c741fecdcb62738ed3f9d93a38aa`  
		Last Modified: Thu, 16 Oct 2025 18:53:14 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9663a44466508c32bf34b7862dfc667ed7d02312b48ad9ac0967a3e55a42c64e`  
		Last Modified: Thu, 16 Oct 2025 18:53:14 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.8.71-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:003a59f49cf4ca8c5a200e9c4b373cdb84a3ab10282547738d1a0ed55885346a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd74a84030e0326efbafe2d861d2229f677a536f20cc788f13a37a1e1c3cd98`

```dockerfile
```

-	Layers:
	-	`sha256:fbb88c3ac9e704a4487b1c7b6cad6b4a8c92cdc2d13a690d56a67a1401052a7c`  
		Last Modified: Thu, 16 Oct 2025 21:49:38 GMT  
		Size: 25.5 KB (25461 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.7.8.71-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:ec7a092fc3f5b1aa5be0c7f613b483db4dac61cba2687d1e80e83d6050e76ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.9 MB (207932780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6ce372f742631d92e894d4823869df3a1abbbe4e9fdb9da706a12ec0573396f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 16 Oct 2025 16:06:54 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 16 Oct 2025 16:06:54 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
ARG REPO_CHANNEL=stable
# Thu, 16 Oct 2025 16:06:54 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 16 Oct 2025 16:06:54 GMT
ARG VERSION=25.7.8.71
# Thu, 16 Oct 2025 16:06:54 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.8.71 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.8.71 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.8.71 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
ENV LANG=en_US.UTF-8
# Thu, 16 Oct 2025 16:06:54 GMT
ENV TZ=UTC
# Thu, 16 Oct 2025 16:06:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.8.71 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 16 Oct 2025 16:06:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 16 Oct 2025 16:06:54 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 16 Oct 2025 16:06:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 16 Oct 2025 16:06:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842d5f71add3462bbc7c1ce16dc942e42b86e6c490409d5e991df8de5fb3603f`  
		Last Modified: Thu, 16 Oct 2025 18:54:15 GMT  
		Size: 7.6 MB (7576754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7f9190289fc1e12edba35673c10cf935ed01de15e516dcc77766a20096052e`  
		Last Modified: Thu, 16 Oct 2025 21:50:07 GMT  
		Size: 172.1 MB (172102892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac106452ef670c779af11ce2a7a64bcb58bc1ecfbab1b8889772cbdecbdf59a`  
		Last Modified: Thu, 16 Oct 2025 18:54:13 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a1a08829fd7e38a68bf67a81eeca3e12f781e448c68363c1b7e91e585d8af9`  
		Last Modified: Thu, 16 Oct 2025 18:54:13 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709484672aeff06b6aa3adc8eb0a3a72ff4ec25c06c862a465eebde8af848f42`  
		Last Modified: Thu, 16 Oct 2025 18:54:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a1b9dc478441ec2500fdae3044a0faea06565a7e12b62a5745f142c6f1ab24`  
		Last Modified: Thu, 16 Oct 2025 18:54:14 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89f200c9fa1f8827fc73e090375b44f3810f6f4e013069f820cf51864176773`  
		Last Modified: Thu, 16 Oct 2025 18:54:14 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.8.71-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5434cf9abad6e2d8390cb54a3d245ca27c4d2af06c4975fe8cd917956a432286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d684efdca1960f0e09a3e0d50d7bbf69822c3dff63adb7faecb105ea06371fa5`

```dockerfile
```

-	Layers:
	-	`sha256:e94144569a80c2726b2bab54438a398bea0e589313368b1dbb6af72306b19815`  
		Last Modified: Thu, 16 Oct 2025 21:49:42 GMT  
		Size: 25.6 KB (25649 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8`

```console
$ docker pull clickhouse@sha256:3ad7dba29b919c092ccdcbc615b154947ee650b98db766f0b02d010876911332
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8` - linux; amd64

```console
$ docker pull clickhouse@sha256:014ce3c7fb6e10da19a42c0eb61995b05f65af48d7492a29d2dc2731c6733c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227813563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36230d3191dfe2429e3ca84290a3205fece0c511fac0c1b24fb08a95ce66389a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 09 Oct 2025 16:08:11 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 09 Oct 2025 16:08:11 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ARG REPO_CHANNEL=stable
# Thu, 09 Oct 2025 16:08:11 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 09 Oct 2025 16:08:11 GMT
ARG VERSION=25.8.10.7
# Thu, 09 Oct 2025 16:08:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Oct 2025 16:08:11 GMT
ENV TZ=UTC
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 09 Oct 2025 16:08:11 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 09 Oct 2025 16:08:11 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 09 Oct 2025 16:08:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbf784615546088a9911e2e6670b12bb2add7f11c869084f50f43701472019a`  
		Last Modified: Thu, 09 Oct 2025 18:04:09 GMT  
		Size: 7.6 MB (7598394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f763341119f8e483bffb29e2067fcce227d7cd93d9af59e70d24620311625033`  
		Last Modified: Thu, 09 Oct 2025 18:50:04 GMT  
		Size: 189.8 MB (189808325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2195d16840bfd88c5050cdbd49f3c79cb23cea6fd82c57e53161b92f14330340`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f28b765b4124de3928ce25e6fdfadebc679ab186b753270194ebd384b24795`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc13c07dc3b1e7e4a22527e28a0adea995540d847256c197657c2d4e2ee4856`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109b8a5c3d24e5d248127a8a9090bf7ba3a3528858793c0670cf4320318637cb`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202891ea53457fd16b78e2c09483a2c30bbcf05a7c9d5b2660e1ea0f9703e42e`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f61f7a88a9cc5bf543e509c175c766faaa2c91bf67bfa430604ab6dd26566077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbdf48d096588bf66f39110ea1fa67d75ea2d3afe30bc4561509b26076da889e`

```dockerfile
```

-	Layers:
	-	`sha256:0c6033682af199025495d6f753aee1c3f90090f3f577fce9da3921f261ea9b51`  
		Last Modified: Thu, 09 Oct 2025 18:49:35 GMT  
		Size: 26.1 KB (26077 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:984c68e62c33767896b89a40a512651046ddb49c395de36617d3065d9d53e83d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.6 MB (212621178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30bd20aebbd2224437c2203ebba4b664b536234bd0127f2963f74d7c4046334`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 09 Oct 2025 16:08:11 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 09 Oct 2025 16:08:11 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ARG REPO_CHANNEL=stable
# Thu, 09 Oct 2025 16:08:11 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 09 Oct 2025 16:08:11 GMT
ARG VERSION=25.8.10.7
# Thu, 09 Oct 2025 16:08:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Oct 2025 16:08:11 GMT
ENV TZ=UTC
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 09 Oct 2025 16:08:11 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 09 Oct 2025 16:08:11 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 09 Oct 2025 16:08:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1153d40948259afc0f2c882331af600a3c3eb3d680f0105a07342bc0d60245`  
		Last Modified: Thu, 09 Oct 2025 18:49:48 GMT  
		Size: 7.6 MB (7576753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf275d0555ec5fca1465a172f1d0f251796fa4f951c45863ee6c2efb21ac066`  
		Last Modified: Thu, 09 Oct 2025 18:49:58 GMT  
		Size: 176.8 MB (176791297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44250edf6e172027a8a7e70ec848942d44e04a45bf505d6f1a5cb5a2ee4c40c`  
		Last Modified: Thu, 09 Oct 2025 18:18:07 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2b4e32c07938d944c59bf2745534bbc75ae74d70c1dc2328059fddb0007520`  
		Last Modified: Thu, 09 Oct 2025 18:18:18 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243bd52d3cccaf7499339160160d3adbb5b5f0146d65b50ef0e2cbb8ce33be90`  
		Last Modified: Thu, 09 Oct 2025 18:18:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cee2da3dd6928562361b1adef7b38f62c05b53eb7651545f8ed7c02b39e2084`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d05804c22b94a1271693b697e0dfd4eb247ac50f9ba72001a9f069033cf0ee5`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3f570dc1ce728a238ca567f82481c0df2f9566081a2405e26db566018a746824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11fa3a06888b684dee3cc392f2a56b6a32a4af4e66e9280d6171e735a00e7c01`

```dockerfile
```

-	Layers:
	-	`sha256:d3c9f2a0afde4bc153c70eabf341024743f43f3f54346643c00867383cacac14`  
		Last Modified: Thu, 09 Oct 2025 18:49:40 GMT  
		Size: 26.3 KB (26288 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8-jammy`

```console
$ docker pull clickhouse@sha256:3ad7dba29b919c092ccdcbc615b154947ee650b98db766f0b02d010876911332
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:014ce3c7fb6e10da19a42c0eb61995b05f65af48d7492a29d2dc2731c6733c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227813563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36230d3191dfe2429e3ca84290a3205fece0c511fac0c1b24fb08a95ce66389a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 09 Oct 2025 16:08:11 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 09 Oct 2025 16:08:11 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ARG REPO_CHANNEL=stable
# Thu, 09 Oct 2025 16:08:11 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 09 Oct 2025 16:08:11 GMT
ARG VERSION=25.8.10.7
# Thu, 09 Oct 2025 16:08:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Oct 2025 16:08:11 GMT
ENV TZ=UTC
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 09 Oct 2025 16:08:11 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 09 Oct 2025 16:08:11 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 09 Oct 2025 16:08:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbf784615546088a9911e2e6670b12bb2add7f11c869084f50f43701472019a`  
		Last Modified: Thu, 09 Oct 2025 18:04:09 GMT  
		Size: 7.6 MB (7598394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f763341119f8e483bffb29e2067fcce227d7cd93d9af59e70d24620311625033`  
		Last Modified: Thu, 09 Oct 2025 18:50:04 GMT  
		Size: 189.8 MB (189808325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2195d16840bfd88c5050cdbd49f3c79cb23cea6fd82c57e53161b92f14330340`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f28b765b4124de3928ce25e6fdfadebc679ab186b753270194ebd384b24795`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc13c07dc3b1e7e4a22527e28a0adea995540d847256c197657c2d4e2ee4856`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109b8a5c3d24e5d248127a8a9090bf7ba3a3528858793c0670cf4320318637cb`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202891ea53457fd16b78e2c09483a2c30bbcf05a7c9d5b2660e1ea0f9703e42e`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f61f7a88a9cc5bf543e509c175c766faaa2c91bf67bfa430604ab6dd26566077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbdf48d096588bf66f39110ea1fa67d75ea2d3afe30bc4561509b26076da889e`

```dockerfile
```

-	Layers:
	-	`sha256:0c6033682af199025495d6f753aee1c3f90090f3f577fce9da3921f261ea9b51`  
		Last Modified: Thu, 09 Oct 2025 18:49:35 GMT  
		Size: 26.1 KB (26077 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:984c68e62c33767896b89a40a512651046ddb49c395de36617d3065d9d53e83d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.6 MB (212621178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30bd20aebbd2224437c2203ebba4b664b536234bd0127f2963f74d7c4046334`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 09 Oct 2025 16:08:11 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 09 Oct 2025 16:08:11 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ARG REPO_CHANNEL=stable
# Thu, 09 Oct 2025 16:08:11 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 09 Oct 2025 16:08:11 GMT
ARG VERSION=25.8.10.7
# Thu, 09 Oct 2025 16:08:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Oct 2025 16:08:11 GMT
ENV TZ=UTC
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 09 Oct 2025 16:08:11 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 09 Oct 2025 16:08:11 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 09 Oct 2025 16:08:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1153d40948259afc0f2c882331af600a3c3eb3d680f0105a07342bc0d60245`  
		Last Modified: Thu, 09 Oct 2025 18:49:48 GMT  
		Size: 7.6 MB (7576753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf275d0555ec5fca1465a172f1d0f251796fa4f951c45863ee6c2efb21ac066`  
		Last Modified: Thu, 09 Oct 2025 18:49:58 GMT  
		Size: 176.8 MB (176791297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44250edf6e172027a8a7e70ec848942d44e04a45bf505d6f1a5cb5a2ee4c40c`  
		Last Modified: Thu, 09 Oct 2025 18:18:07 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2b4e32c07938d944c59bf2745534bbc75ae74d70c1dc2328059fddb0007520`  
		Last Modified: Thu, 09 Oct 2025 18:18:18 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243bd52d3cccaf7499339160160d3adbb5b5f0146d65b50ef0e2cbb8ce33be90`  
		Last Modified: Thu, 09 Oct 2025 18:18:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cee2da3dd6928562361b1adef7b38f62c05b53eb7651545f8ed7c02b39e2084`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d05804c22b94a1271693b697e0dfd4eb247ac50f9ba72001a9f069033cf0ee5`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3f570dc1ce728a238ca567f82481c0df2f9566081a2405e26db566018a746824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11fa3a06888b684dee3cc392f2a56b6a32a4af4e66e9280d6171e735a00e7c01`

```dockerfile
```

-	Layers:
	-	`sha256:d3c9f2a0afde4bc153c70eabf341024743f43f3f54346643c00867383cacac14`  
		Last Modified: Thu, 09 Oct 2025 18:49:40 GMT  
		Size: 26.3 KB (26288 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.10`

```console
$ docker pull clickhouse@sha256:3ad7dba29b919c092ccdcbc615b154947ee650b98db766f0b02d010876911332
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.10` - linux; amd64

```console
$ docker pull clickhouse@sha256:014ce3c7fb6e10da19a42c0eb61995b05f65af48d7492a29d2dc2731c6733c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227813563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36230d3191dfe2429e3ca84290a3205fece0c511fac0c1b24fb08a95ce66389a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 09 Oct 2025 16:08:11 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 09 Oct 2025 16:08:11 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ARG REPO_CHANNEL=stable
# Thu, 09 Oct 2025 16:08:11 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 09 Oct 2025 16:08:11 GMT
ARG VERSION=25.8.10.7
# Thu, 09 Oct 2025 16:08:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Oct 2025 16:08:11 GMT
ENV TZ=UTC
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 09 Oct 2025 16:08:11 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 09 Oct 2025 16:08:11 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 09 Oct 2025 16:08:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbf784615546088a9911e2e6670b12bb2add7f11c869084f50f43701472019a`  
		Last Modified: Thu, 09 Oct 2025 18:04:09 GMT  
		Size: 7.6 MB (7598394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f763341119f8e483bffb29e2067fcce227d7cd93d9af59e70d24620311625033`  
		Last Modified: Thu, 09 Oct 2025 18:50:04 GMT  
		Size: 189.8 MB (189808325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2195d16840bfd88c5050cdbd49f3c79cb23cea6fd82c57e53161b92f14330340`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f28b765b4124de3928ce25e6fdfadebc679ab186b753270194ebd384b24795`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc13c07dc3b1e7e4a22527e28a0adea995540d847256c197657c2d4e2ee4856`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109b8a5c3d24e5d248127a8a9090bf7ba3a3528858793c0670cf4320318637cb`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202891ea53457fd16b78e2c09483a2c30bbcf05a7c9d5b2660e1ea0f9703e42e`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.10` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f61f7a88a9cc5bf543e509c175c766faaa2c91bf67bfa430604ab6dd26566077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbdf48d096588bf66f39110ea1fa67d75ea2d3afe30bc4561509b26076da889e`

```dockerfile
```

-	Layers:
	-	`sha256:0c6033682af199025495d6f753aee1c3f90090f3f577fce9da3921f261ea9b51`  
		Last Modified: Thu, 09 Oct 2025 18:49:35 GMT  
		Size: 26.1 KB (26077 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.10` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:984c68e62c33767896b89a40a512651046ddb49c395de36617d3065d9d53e83d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.6 MB (212621178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30bd20aebbd2224437c2203ebba4b664b536234bd0127f2963f74d7c4046334`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 09 Oct 2025 16:08:11 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 09 Oct 2025 16:08:11 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ARG REPO_CHANNEL=stable
# Thu, 09 Oct 2025 16:08:11 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 09 Oct 2025 16:08:11 GMT
ARG VERSION=25.8.10.7
# Thu, 09 Oct 2025 16:08:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Oct 2025 16:08:11 GMT
ENV TZ=UTC
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 09 Oct 2025 16:08:11 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 09 Oct 2025 16:08:11 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 09 Oct 2025 16:08:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1153d40948259afc0f2c882331af600a3c3eb3d680f0105a07342bc0d60245`  
		Last Modified: Thu, 09 Oct 2025 18:49:48 GMT  
		Size: 7.6 MB (7576753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf275d0555ec5fca1465a172f1d0f251796fa4f951c45863ee6c2efb21ac066`  
		Last Modified: Thu, 09 Oct 2025 18:49:58 GMT  
		Size: 176.8 MB (176791297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44250edf6e172027a8a7e70ec848942d44e04a45bf505d6f1a5cb5a2ee4c40c`  
		Last Modified: Thu, 09 Oct 2025 18:18:07 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2b4e32c07938d944c59bf2745534bbc75ae74d70c1dc2328059fddb0007520`  
		Last Modified: Thu, 09 Oct 2025 18:18:18 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243bd52d3cccaf7499339160160d3adbb5b5f0146d65b50ef0e2cbb8ce33be90`  
		Last Modified: Thu, 09 Oct 2025 18:18:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cee2da3dd6928562361b1adef7b38f62c05b53eb7651545f8ed7c02b39e2084`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d05804c22b94a1271693b697e0dfd4eb247ac50f9ba72001a9f069033cf0ee5`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.10` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3f570dc1ce728a238ca567f82481c0df2f9566081a2405e26db566018a746824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11fa3a06888b684dee3cc392f2a56b6a32a4af4e66e9280d6171e735a00e7c01`

```dockerfile
```

-	Layers:
	-	`sha256:d3c9f2a0afde4bc153c70eabf341024743f43f3f54346643c00867383cacac14`  
		Last Modified: Thu, 09 Oct 2025 18:49:40 GMT  
		Size: 26.3 KB (26288 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.10-jammy`

```console
$ docker pull clickhouse@sha256:3ad7dba29b919c092ccdcbc615b154947ee650b98db766f0b02d010876911332
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.10-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:014ce3c7fb6e10da19a42c0eb61995b05f65af48d7492a29d2dc2731c6733c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227813563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36230d3191dfe2429e3ca84290a3205fece0c511fac0c1b24fb08a95ce66389a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 09 Oct 2025 16:08:11 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 09 Oct 2025 16:08:11 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ARG REPO_CHANNEL=stable
# Thu, 09 Oct 2025 16:08:11 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 09 Oct 2025 16:08:11 GMT
ARG VERSION=25.8.10.7
# Thu, 09 Oct 2025 16:08:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Oct 2025 16:08:11 GMT
ENV TZ=UTC
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 09 Oct 2025 16:08:11 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 09 Oct 2025 16:08:11 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 09 Oct 2025 16:08:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbf784615546088a9911e2e6670b12bb2add7f11c869084f50f43701472019a`  
		Last Modified: Thu, 09 Oct 2025 18:04:09 GMT  
		Size: 7.6 MB (7598394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f763341119f8e483bffb29e2067fcce227d7cd93d9af59e70d24620311625033`  
		Last Modified: Thu, 09 Oct 2025 18:50:04 GMT  
		Size: 189.8 MB (189808325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2195d16840bfd88c5050cdbd49f3c79cb23cea6fd82c57e53161b92f14330340`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f28b765b4124de3928ce25e6fdfadebc679ab186b753270194ebd384b24795`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc13c07dc3b1e7e4a22527e28a0adea995540d847256c197657c2d4e2ee4856`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109b8a5c3d24e5d248127a8a9090bf7ba3a3528858793c0670cf4320318637cb`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202891ea53457fd16b78e2c09483a2c30bbcf05a7c9d5b2660e1ea0f9703e42e`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.10-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f61f7a88a9cc5bf543e509c175c766faaa2c91bf67bfa430604ab6dd26566077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbdf48d096588bf66f39110ea1fa67d75ea2d3afe30bc4561509b26076da889e`

```dockerfile
```

-	Layers:
	-	`sha256:0c6033682af199025495d6f753aee1c3f90090f3f577fce9da3921f261ea9b51`  
		Last Modified: Thu, 09 Oct 2025 18:49:35 GMT  
		Size: 26.1 KB (26077 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.10-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:984c68e62c33767896b89a40a512651046ddb49c395de36617d3065d9d53e83d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.6 MB (212621178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30bd20aebbd2224437c2203ebba4b664b536234bd0127f2963f74d7c4046334`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 09 Oct 2025 16:08:11 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 09 Oct 2025 16:08:11 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ARG REPO_CHANNEL=stable
# Thu, 09 Oct 2025 16:08:11 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 09 Oct 2025 16:08:11 GMT
ARG VERSION=25.8.10.7
# Thu, 09 Oct 2025 16:08:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Oct 2025 16:08:11 GMT
ENV TZ=UTC
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 09 Oct 2025 16:08:11 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 09 Oct 2025 16:08:11 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 09 Oct 2025 16:08:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1153d40948259afc0f2c882331af600a3c3eb3d680f0105a07342bc0d60245`  
		Last Modified: Thu, 09 Oct 2025 18:49:48 GMT  
		Size: 7.6 MB (7576753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf275d0555ec5fca1465a172f1d0f251796fa4f951c45863ee6c2efb21ac066`  
		Last Modified: Thu, 09 Oct 2025 18:49:58 GMT  
		Size: 176.8 MB (176791297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44250edf6e172027a8a7e70ec848942d44e04a45bf505d6f1a5cb5a2ee4c40c`  
		Last Modified: Thu, 09 Oct 2025 18:18:07 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2b4e32c07938d944c59bf2745534bbc75ae74d70c1dc2328059fddb0007520`  
		Last Modified: Thu, 09 Oct 2025 18:18:18 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243bd52d3cccaf7499339160160d3adbb5b5f0146d65b50ef0e2cbb8ce33be90`  
		Last Modified: Thu, 09 Oct 2025 18:18:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cee2da3dd6928562361b1adef7b38f62c05b53eb7651545f8ed7c02b39e2084`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d05804c22b94a1271693b697e0dfd4eb247ac50f9ba72001a9f069033cf0ee5`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.10-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3f570dc1ce728a238ca567f82481c0df2f9566081a2405e26db566018a746824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11fa3a06888b684dee3cc392f2a56b6a32a4af4e66e9280d6171e735a00e7c01`

```dockerfile
```

-	Layers:
	-	`sha256:d3c9f2a0afde4bc153c70eabf341024743f43f3f54346643c00867383cacac14`  
		Last Modified: Thu, 09 Oct 2025 18:49:40 GMT  
		Size: 26.3 KB (26288 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.10.7`

```console
$ docker pull clickhouse@sha256:3ad7dba29b919c092ccdcbc615b154947ee650b98db766f0b02d010876911332
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.10.7` - linux; amd64

```console
$ docker pull clickhouse@sha256:014ce3c7fb6e10da19a42c0eb61995b05f65af48d7492a29d2dc2731c6733c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227813563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36230d3191dfe2429e3ca84290a3205fece0c511fac0c1b24fb08a95ce66389a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 09 Oct 2025 16:08:11 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 09 Oct 2025 16:08:11 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ARG REPO_CHANNEL=stable
# Thu, 09 Oct 2025 16:08:11 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 09 Oct 2025 16:08:11 GMT
ARG VERSION=25.8.10.7
# Thu, 09 Oct 2025 16:08:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Oct 2025 16:08:11 GMT
ENV TZ=UTC
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 09 Oct 2025 16:08:11 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 09 Oct 2025 16:08:11 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 09 Oct 2025 16:08:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbf784615546088a9911e2e6670b12bb2add7f11c869084f50f43701472019a`  
		Last Modified: Thu, 09 Oct 2025 18:04:09 GMT  
		Size: 7.6 MB (7598394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f763341119f8e483bffb29e2067fcce227d7cd93d9af59e70d24620311625033`  
		Last Modified: Thu, 09 Oct 2025 18:50:04 GMT  
		Size: 189.8 MB (189808325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2195d16840bfd88c5050cdbd49f3c79cb23cea6fd82c57e53161b92f14330340`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f28b765b4124de3928ce25e6fdfadebc679ab186b753270194ebd384b24795`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc13c07dc3b1e7e4a22527e28a0adea995540d847256c197657c2d4e2ee4856`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109b8a5c3d24e5d248127a8a9090bf7ba3a3528858793c0670cf4320318637cb`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202891ea53457fd16b78e2c09483a2c30bbcf05a7c9d5b2660e1ea0f9703e42e`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.10.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f61f7a88a9cc5bf543e509c175c766faaa2c91bf67bfa430604ab6dd26566077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbdf48d096588bf66f39110ea1fa67d75ea2d3afe30bc4561509b26076da889e`

```dockerfile
```

-	Layers:
	-	`sha256:0c6033682af199025495d6f753aee1c3f90090f3f577fce9da3921f261ea9b51`  
		Last Modified: Thu, 09 Oct 2025 18:49:35 GMT  
		Size: 26.1 KB (26077 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.10.7` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:984c68e62c33767896b89a40a512651046ddb49c395de36617d3065d9d53e83d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.6 MB (212621178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30bd20aebbd2224437c2203ebba4b664b536234bd0127f2963f74d7c4046334`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 09 Oct 2025 16:08:11 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 09 Oct 2025 16:08:11 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ARG REPO_CHANNEL=stable
# Thu, 09 Oct 2025 16:08:11 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 09 Oct 2025 16:08:11 GMT
ARG VERSION=25.8.10.7
# Thu, 09 Oct 2025 16:08:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Oct 2025 16:08:11 GMT
ENV TZ=UTC
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 09 Oct 2025 16:08:11 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 09 Oct 2025 16:08:11 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 09 Oct 2025 16:08:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1153d40948259afc0f2c882331af600a3c3eb3d680f0105a07342bc0d60245`  
		Last Modified: Thu, 09 Oct 2025 18:49:48 GMT  
		Size: 7.6 MB (7576753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf275d0555ec5fca1465a172f1d0f251796fa4f951c45863ee6c2efb21ac066`  
		Last Modified: Thu, 09 Oct 2025 18:49:58 GMT  
		Size: 176.8 MB (176791297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44250edf6e172027a8a7e70ec848942d44e04a45bf505d6f1a5cb5a2ee4c40c`  
		Last Modified: Thu, 09 Oct 2025 18:18:07 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2b4e32c07938d944c59bf2745534bbc75ae74d70c1dc2328059fddb0007520`  
		Last Modified: Thu, 09 Oct 2025 18:18:18 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243bd52d3cccaf7499339160160d3adbb5b5f0146d65b50ef0e2cbb8ce33be90`  
		Last Modified: Thu, 09 Oct 2025 18:18:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cee2da3dd6928562361b1adef7b38f62c05b53eb7651545f8ed7c02b39e2084`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d05804c22b94a1271693b697e0dfd4eb247ac50f9ba72001a9f069033cf0ee5`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.10.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3f570dc1ce728a238ca567f82481c0df2f9566081a2405e26db566018a746824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11fa3a06888b684dee3cc392f2a56b6a32a4af4e66e9280d6171e735a00e7c01`

```dockerfile
```

-	Layers:
	-	`sha256:d3c9f2a0afde4bc153c70eabf341024743f43f3f54346643c00867383cacac14`  
		Last Modified: Thu, 09 Oct 2025 18:49:40 GMT  
		Size: 26.3 KB (26288 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.10.7-jammy`

```console
$ docker pull clickhouse@sha256:3ad7dba29b919c092ccdcbc615b154947ee650b98db766f0b02d010876911332
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.10.7-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:014ce3c7fb6e10da19a42c0eb61995b05f65af48d7492a29d2dc2731c6733c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227813563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36230d3191dfe2429e3ca84290a3205fece0c511fac0c1b24fb08a95ce66389a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 09 Oct 2025 16:08:11 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 09 Oct 2025 16:08:11 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ARG REPO_CHANNEL=stable
# Thu, 09 Oct 2025 16:08:11 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 09 Oct 2025 16:08:11 GMT
ARG VERSION=25.8.10.7
# Thu, 09 Oct 2025 16:08:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Oct 2025 16:08:11 GMT
ENV TZ=UTC
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 09 Oct 2025 16:08:11 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 09 Oct 2025 16:08:11 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 09 Oct 2025 16:08:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbf784615546088a9911e2e6670b12bb2add7f11c869084f50f43701472019a`  
		Last Modified: Thu, 09 Oct 2025 18:04:09 GMT  
		Size: 7.6 MB (7598394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f763341119f8e483bffb29e2067fcce227d7cd93d9af59e70d24620311625033`  
		Last Modified: Thu, 09 Oct 2025 18:50:04 GMT  
		Size: 189.8 MB (189808325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2195d16840bfd88c5050cdbd49f3c79cb23cea6fd82c57e53161b92f14330340`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f28b765b4124de3928ce25e6fdfadebc679ab186b753270194ebd384b24795`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc13c07dc3b1e7e4a22527e28a0adea995540d847256c197657c2d4e2ee4856`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109b8a5c3d24e5d248127a8a9090bf7ba3a3528858793c0670cf4320318637cb`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202891ea53457fd16b78e2c09483a2c30bbcf05a7c9d5b2660e1ea0f9703e42e`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.10.7-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f61f7a88a9cc5bf543e509c175c766faaa2c91bf67bfa430604ab6dd26566077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbdf48d096588bf66f39110ea1fa67d75ea2d3afe30bc4561509b26076da889e`

```dockerfile
```

-	Layers:
	-	`sha256:0c6033682af199025495d6f753aee1c3f90090f3f577fce9da3921f261ea9b51`  
		Last Modified: Thu, 09 Oct 2025 18:49:35 GMT  
		Size: 26.1 KB (26077 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.10.7-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:984c68e62c33767896b89a40a512651046ddb49c395de36617d3065d9d53e83d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.6 MB (212621178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30bd20aebbd2224437c2203ebba4b664b536234bd0127f2963f74d7c4046334`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 09 Oct 2025 16:08:11 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 09 Oct 2025 16:08:11 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ARG REPO_CHANNEL=stable
# Thu, 09 Oct 2025 16:08:11 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 09 Oct 2025 16:08:11 GMT
ARG VERSION=25.8.10.7
# Thu, 09 Oct 2025 16:08:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Oct 2025 16:08:11 GMT
ENV TZ=UTC
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 09 Oct 2025 16:08:11 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 09 Oct 2025 16:08:11 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 09 Oct 2025 16:08:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1153d40948259afc0f2c882331af600a3c3eb3d680f0105a07342bc0d60245`  
		Last Modified: Thu, 09 Oct 2025 18:49:48 GMT  
		Size: 7.6 MB (7576753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf275d0555ec5fca1465a172f1d0f251796fa4f951c45863ee6c2efb21ac066`  
		Last Modified: Thu, 09 Oct 2025 18:49:58 GMT  
		Size: 176.8 MB (176791297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44250edf6e172027a8a7e70ec848942d44e04a45bf505d6f1a5cb5a2ee4c40c`  
		Last Modified: Thu, 09 Oct 2025 18:18:07 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2b4e32c07938d944c59bf2745534bbc75ae74d70c1dc2328059fddb0007520`  
		Last Modified: Thu, 09 Oct 2025 18:18:18 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243bd52d3cccaf7499339160160d3adbb5b5f0146d65b50ef0e2cbb8ce33be90`  
		Last Modified: Thu, 09 Oct 2025 18:18:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cee2da3dd6928562361b1adef7b38f62c05b53eb7651545f8ed7c02b39e2084`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d05804c22b94a1271693b697e0dfd4eb247ac50f9ba72001a9f069033cf0ee5`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.10.7-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3f570dc1ce728a238ca567f82481c0df2f9566081a2405e26db566018a746824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11fa3a06888b684dee3cc392f2a56b6a32a4af4e66e9280d6171e735a00e7c01`

```dockerfile
```

-	Layers:
	-	`sha256:d3c9f2a0afde4bc153c70eabf341024743f43f3f54346643c00867383cacac14`  
		Last Modified: Thu, 09 Oct 2025 18:49:40 GMT  
		Size: 26.3 KB (26288 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.9`

```console
$ docker pull clickhouse@sha256:314fccc9ac7d95d42e2c8acd352554c7dbbf18272b51e00745a05da8e5b253d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.9` - linux; amd64

```console
$ docker pull clickhouse@sha256:5625912305fbc1f15b3d3f2583b6c762ea6e55234be9e7453facdaf71854045e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.8 MB (228833641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d61b4231cd63c90d1a1d1182e7225fd8b7cc8bf9ae1b887b907027efbac11a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 23 Oct 2025 16:06:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 23 Oct 2025 16:06:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
ARG REPO_CHANNEL=stable
# Thu, 23 Oct 2025 16:06:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 23 Oct 2025 16:06:50 GMT
ARG VERSION=25.9.4.58
# Thu, 23 Oct 2025 16:06:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
ENV LANG=en_US.UTF-8
# Thu, 23 Oct 2025 16:06:50 GMT
ENV TZ=UTC
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 23 Oct 2025 16:06:50 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 23 Oct 2025 16:06:50 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 23 Oct 2025 16:06:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:448c320ee0ed6369efabdcd6e80936019eeed85a13fb4e3481675029a1abef27`  
		Last Modified: Thu, 23 Oct 2025 23:28:27 GMT  
		Size: 7.6 MB (7598389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2263f88f7716a380550c6778749c9a44d41f29f768b2792302aa28c1a22e403`  
		Last Modified: Fri, 24 Oct 2025 00:49:58 GMT  
		Size: 190.8 MB (190828405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61452f93f2c196dbdf99950843c9cfccbcf99bb0e2e02c549eac9aa45a1ee27`  
		Last Modified: Thu, 23 Oct 2025 23:28:26 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23083dff4142aa95c1af480f64c7016930c4d4334412e754b13fdc90d34a5bb4`  
		Last Modified: Thu, 23 Oct 2025 23:28:26 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b60e85f50a3310c9644e0f4ef8ac7ca6399ac79bdc8b354f9a4b7fd4c85e26`  
		Last Modified: Thu, 23 Oct 2025 23:28:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d232c9f1aacee2e91a2dad24d85208d8cb3d9b9d4f4cf84b8805b9e0867184b`  
		Last Modified: Thu, 23 Oct 2025 23:28:26 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0458b551cbb0bebf370eeed7a4b45fb35f2a58d43071bd9f59c43b3e6753996`  
		Last Modified: Thu, 23 Oct 2025 23:28:26 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9` - unknown; unknown

```console
$ docker pull clickhouse@sha256:817d7b611e78bc559333bd8d75344334090e61f28621c714915ec0faef12019a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:623b41d0d0bc8627005a2cea9e9911e98523b7e5bfc0c2ff597f4ea9e852dcdb`

```dockerfile
```

-	Layers:
	-	`sha256:91da8fef60fa485696e72b09a8649f7c6a2f510c0d95c4fbebc5be8c87071166`  
		Last Modified: Fri, 24 Oct 2025 00:49:25 GMT  
		Size: 26.1 KB (26071 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.9` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:7617a68234240ab5063f7040b050882cb89ed7ba7f2f23fee27005ddf5742c3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214122062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157073ed1af7b6df6aa4d62bbee55990144981e8b2a8be520fd3ea59758aa2c6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 23 Oct 2025 16:06:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 23 Oct 2025 16:06:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
ARG REPO_CHANNEL=stable
# Thu, 23 Oct 2025 16:06:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 23 Oct 2025 16:06:50 GMT
ARG VERSION=25.9.4.58
# Thu, 23 Oct 2025 16:06:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
ENV LANG=en_US.UTF-8
# Thu, 23 Oct 2025 16:06:50 GMT
ENV TZ=UTC
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 23 Oct 2025 16:06:50 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 23 Oct 2025 16:06:50 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 23 Oct 2025 16:06:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51dd8ef4596e241d8da0b34e2429acfbd000eb915cfdf673912ea44c90a0e5d3`  
		Last Modified: Thu, 23 Oct 2025 21:27:16 GMT  
		Size: 7.6 MB (7576738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04df4dc5f8980801074e5484109b1670c9da98e4a322fa4325a88b1e780e62c6`  
		Last Modified: Thu, 23 Oct 2025 21:49:54 GMT  
		Size: 178.3 MB (178292196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4338714d7e65f209c56e194a18f88f02c1000565a7fef4aa4a5ebd26c0dd6c`  
		Last Modified: Thu, 23 Oct 2025 21:27:15 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5288159d8914a691a503723d40cb4a6132c77e1709c70aa636f52d093f30b8`  
		Last Modified: Thu, 23 Oct 2025 21:27:15 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39947de51651e74c4d02f0929ea799a32a86e474dac339c314b841d667eff2f`  
		Last Modified: Thu, 23 Oct 2025 21:27:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7ad64f931385c578056a088c2b1e1deb0ebc99913af56e39de25c31d8d72ff`  
		Last Modified: Thu, 23 Oct 2025 21:27:16 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b984804c5d0ae90d01cddb5a92e5b8a4cedf46d3959c4ad9a5a426fecdd30d8`  
		Last Modified: Thu, 23 Oct 2025 21:27:15 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9645d0ed6d160bd7c3b9e789d847cf7e7e062c54b2face2e04cdbac20d9143ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:216484c23ff0507e301a25fa2e62b2dc760afbeac4a3b21bc62abcb73dc0ae07`

```dockerfile
```

-	Layers:
	-	`sha256:ece05afee5ab01587a237add3de9abd28f441770e00551740eee672f5b147dbb`  
		Last Modified: Thu, 23 Oct 2025 21:49:26 GMT  
		Size: 26.3 KB (26283 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.9-jammy`

```console
$ docker pull clickhouse@sha256:314fccc9ac7d95d42e2c8acd352554c7dbbf18272b51e00745a05da8e5b253d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.9-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:5625912305fbc1f15b3d3f2583b6c762ea6e55234be9e7453facdaf71854045e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.8 MB (228833641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d61b4231cd63c90d1a1d1182e7225fd8b7cc8bf9ae1b887b907027efbac11a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 23 Oct 2025 16:06:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 23 Oct 2025 16:06:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
ARG REPO_CHANNEL=stable
# Thu, 23 Oct 2025 16:06:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 23 Oct 2025 16:06:50 GMT
ARG VERSION=25.9.4.58
# Thu, 23 Oct 2025 16:06:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
ENV LANG=en_US.UTF-8
# Thu, 23 Oct 2025 16:06:50 GMT
ENV TZ=UTC
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 23 Oct 2025 16:06:50 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 23 Oct 2025 16:06:50 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 23 Oct 2025 16:06:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:448c320ee0ed6369efabdcd6e80936019eeed85a13fb4e3481675029a1abef27`  
		Last Modified: Thu, 23 Oct 2025 23:28:27 GMT  
		Size: 7.6 MB (7598389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2263f88f7716a380550c6778749c9a44d41f29f768b2792302aa28c1a22e403`  
		Last Modified: Fri, 24 Oct 2025 00:49:58 GMT  
		Size: 190.8 MB (190828405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61452f93f2c196dbdf99950843c9cfccbcf99bb0e2e02c549eac9aa45a1ee27`  
		Last Modified: Thu, 23 Oct 2025 23:28:26 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23083dff4142aa95c1af480f64c7016930c4d4334412e754b13fdc90d34a5bb4`  
		Last Modified: Thu, 23 Oct 2025 23:28:26 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b60e85f50a3310c9644e0f4ef8ac7ca6399ac79bdc8b354f9a4b7fd4c85e26`  
		Last Modified: Thu, 23 Oct 2025 23:28:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d232c9f1aacee2e91a2dad24d85208d8cb3d9b9d4f4cf84b8805b9e0867184b`  
		Last Modified: Thu, 23 Oct 2025 23:28:26 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0458b551cbb0bebf370eeed7a4b45fb35f2a58d43071bd9f59c43b3e6753996`  
		Last Modified: Thu, 23 Oct 2025 23:28:26 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:817d7b611e78bc559333bd8d75344334090e61f28621c714915ec0faef12019a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:623b41d0d0bc8627005a2cea9e9911e98523b7e5bfc0c2ff597f4ea9e852dcdb`

```dockerfile
```

-	Layers:
	-	`sha256:91da8fef60fa485696e72b09a8649f7c6a2f510c0d95c4fbebc5be8c87071166`  
		Last Modified: Fri, 24 Oct 2025 00:49:25 GMT  
		Size: 26.1 KB (26071 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.9-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:7617a68234240ab5063f7040b050882cb89ed7ba7f2f23fee27005ddf5742c3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214122062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157073ed1af7b6df6aa4d62bbee55990144981e8b2a8be520fd3ea59758aa2c6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 23 Oct 2025 16:06:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 23 Oct 2025 16:06:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
ARG REPO_CHANNEL=stable
# Thu, 23 Oct 2025 16:06:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 23 Oct 2025 16:06:50 GMT
ARG VERSION=25.9.4.58
# Thu, 23 Oct 2025 16:06:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
ENV LANG=en_US.UTF-8
# Thu, 23 Oct 2025 16:06:50 GMT
ENV TZ=UTC
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 23 Oct 2025 16:06:50 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 23 Oct 2025 16:06:50 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 23 Oct 2025 16:06:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51dd8ef4596e241d8da0b34e2429acfbd000eb915cfdf673912ea44c90a0e5d3`  
		Last Modified: Thu, 23 Oct 2025 21:27:16 GMT  
		Size: 7.6 MB (7576738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04df4dc5f8980801074e5484109b1670c9da98e4a322fa4325a88b1e780e62c6`  
		Last Modified: Thu, 23 Oct 2025 21:49:54 GMT  
		Size: 178.3 MB (178292196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4338714d7e65f209c56e194a18f88f02c1000565a7fef4aa4a5ebd26c0dd6c`  
		Last Modified: Thu, 23 Oct 2025 21:27:15 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5288159d8914a691a503723d40cb4a6132c77e1709c70aa636f52d093f30b8`  
		Last Modified: Thu, 23 Oct 2025 21:27:15 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39947de51651e74c4d02f0929ea799a32a86e474dac339c314b841d667eff2f`  
		Last Modified: Thu, 23 Oct 2025 21:27:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7ad64f931385c578056a088c2b1e1deb0ebc99913af56e39de25c31d8d72ff`  
		Last Modified: Thu, 23 Oct 2025 21:27:16 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b984804c5d0ae90d01cddb5a92e5b8a4cedf46d3959c4ad9a5a426fecdd30d8`  
		Last Modified: Thu, 23 Oct 2025 21:27:15 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9645d0ed6d160bd7c3b9e789d847cf7e7e062c54b2face2e04cdbac20d9143ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:216484c23ff0507e301a25fa2e62b2dc760afbeac4a3b21bc62abcb73dc0ae07`

```dockerfile
```

-	Layers:
	-	`sha256:ece05afee5ab01587a237add3de9abd28f441770e00551740eee672f5b147dbb`  
		Last Modified: Thu, 23 Oct 2025 21:49:26 GMT  
		Size: 26.3 KB (26283 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.9.4`

```console
$ docker pull clickhouse@sha256:314fccc9ac7d95d42e2c8acd352554c7dbbf18272b51e00745a05da8e5b253d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.9.4` - linux; amd64

```console
$ docker pull clickhouse@sha256:5625912305fbc1f15b3d3f2583b6c762ea6e55234be9e7453facdaf71854045e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.8 MB (228833641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d61b4231cd63c90d1a1d1182e7225fd8b7cc8bf9ae1b887b907027efbac11a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 23 Oct 2025 16:06:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 23 Oct 2025 16:06:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
ARG REPO_CHANNEL=stable
# Thu, 23 Oct 2025 16:06:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 23 Oct 2025 16:06:50 GMT
ARG VERSION=25.9.4.58
# Thu, 23 Oct 2025 16:06:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
ENV LANG=en_US.UTF-8
# Thu, 23 Oct 2025 16:06:50 GMT
ENV TZ=UTC
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 23 Oct 2025 16:06:50 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 23 Oct 2025 16:06:50 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 23 Oct 2025 16:06:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:448c320ee0ed6369efabdcd6e80936019eeed85a13fb4e3481675029a1abef27`  
		Last Modified: Thu, 23 Oct 2025 23:28:27 GMT  
		Size: 7.6 MB (7598389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2263f88f7716a380550c6778749c9a44d41f29f768b2792302aa28c1a22e403`  
		Last Modified: Fri, 24 Oct 2025 00:49:58 GMT  
		Size: 190.8 MB (190828405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61452f93f2c196dbdf99950843c9cfccbcf99bb0e2e02c549eac9aa45a1ee27`  
		Last Modified: Thu, 23 Oct 2025 23:28:26 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23083dff4142aa95c1af480f64c7016930c4d4334412e754b13fdc90d34a5bb4`  
		Last Modified: Thu, 23 Oct 2025 23:28:26 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b60e85f50a3310c9644e0f4ef8ac7ca6399ac79bdc8b354f9a4b7fd4c85e26`  
		Last Modified: Thu, 23 Oct 2025 23:28:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d232c9f1aacee2e91a2dad24d85208d8cb3d9b9d4f4cf84b8805b9e0867184b`  
		Last Modified: Thu, 23 Oct 2025 23:28:26 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0458b551cbb0bebf370eeed7a4b45fb35f2a58d43071bd9f59c43b3e6753996`  
		Last Modified: Thu, 23 Oct 2025 23:28:26 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:817d7b611e78bc559333bd8d75344334090e61f28621c714915ec0faef12019a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:623b41d0d0bc8627005a2cea9e9911e98523b7e5bfc0c2ff597f4ea9e852dcdb`

```dockerfile
```

-	Layers:
	-	`sha256:91da8fef60fa485696e72b09a8649f7c6a2f510c0d95c4fbebc5be8c87071166`  
		Last Modified: Fri, 24 Oct 2025 00:49:25 GMT  
		Size: 26.1 KB (26071 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.9.4` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:7617a68234240ab5063f7040b050882cb89ed7ba7f2f23fee27005ddf5742c3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214122062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157073ed1af7b6df6aa4d62bbee55990144981e8b2a8be520fd3ea59758aa2c6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 23 Oct 2025 16:06:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 23 Oct 2025 16:06:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
ARG REPO_CHANNEL=stable
# Thu, 23 Oct 2025 16:06:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 23 Oct 2025 16:06:50 GMT
ARG VERSION=25.9.4.58
# Thu, 23 Oct 2025 16:06:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
ENV LANG=en_US.UTF-8
# Thu, 23 Oct 2025 16:06:50 GMT
ENV TZ=UTC
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 23 Oct 2025 16:06:50 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 23 Oct 2025 16:06:50 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 23 Oct 2025 16:06:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51dd8ef4596e241d8da0b34e2429acfbd000eb915cfdf673912ea44c90a0e5d3`  
		Last Modified: Thu, 23 Oct 2025 21:27:16 GMT  
		Size: 7.6 MB (7576738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04df4dc5f8980801074e5484109b1670c9da98e4a322fa4325a88b1e780e62c6`  
		Last Modified: Thu, 23 Oct 2025 21:49:54 GMT  
		Size: 178.3 MB (178292196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4338714d7e65f209c56e194a18f88f02c1000565a7fef4aa4a5ebd26c0dd6c`  
		Last Modified: Thu, 23 Oct 2025 21:27:15 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5288159d8914a691a503723d40cb4a6132c77e1709c70aa636f52d093f30b8`  
		Last Modified: Thu, 23 Oct 2025 21:27:15 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39947de51651e74c4d02f0929ea799a32a86e474dac339c314b841d667eff2f`  
		Last Modified: Thu, 23 Oct 2025 21:27:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7ad64f931385c578056a088c2b1e1deb0ebc99913af56e39de25c31d8d72ff`  
		Last Modified: Thu, 23 Oct 2025 21:27:16 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b984804c5d0ae90d01cddb5a92e5b8a4cedf46d3959c4ad9a5a426fecdd30d8`  
		Last Modified: Thu, 23 Oct 2025 21:27:15 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9645d0ed6d160bd7c3b9e789d847cf7e7e062c54b2face2e04cdbac20d9143ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:216484c23ff0507e301a25fa2e62b2dc760afbeac4a3b21bc62abcb73dc0ae07`

```dockerfile
```

-	Layers:
	-	`sha256:ece05afee5ab01587a237add3de9abd28f441770e00551740eee672f5b147dbb`  
		Last Modified: Thu, 23 Oct 2025 21:49:26 GMT  
		Size: 26.3 KB (26283 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.9.4-jammy`

```console
$ docker pull clickhouse@sha256:314fccc9ac7d95d42e2c8acd352554c7dbbf18272b51e00745a05da8e5b253d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.9.4-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:5625912305fbc1f15b3d3f2583b6c762ea6e55234be9e7453facdaf71854045e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.8 MB (228833641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d61b4231cd63c90d1a1d1182e7225fd8b7cc8bf9ae1b887b907027efbac11a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 23 Oct 2025 16:06:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 23 Oct 2025 16:06:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
ARG REPO_CHANNEL=stable
# Thu, 23 Oct 2025 16:06:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 23 Oct 2025 16:06:50 GMT
ARG VERSION=25.9.4.58
# Thu, 23 Oct 2025 16:06:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
ENV LANG=en_US.UTF-8
# Thu, 23 Oct 2025 16:06:50 GMT
ENV TZ=UTC
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 23 Oct 2025 16:06:50 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 23 Oct 2025 16:06:50 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 23 Oct 2025 16:06:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:448c320ee0ed6369efabdcd6e80936019eeed85a13fb4e3481675029a1abef27`  
		Last Modified: Thu, 23 Oct 2025 23:28:27 GMT  
		Size: 7.6 MB (7598389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2263f88f7716a380550c6778749c9a44d41f29f768b2792302aa28c1a22e403`  
		Last Modified: Fri, 24 Oct 2025 00:49:58 GMT  
		Size: 190.8 MB (190828405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61452f93f2c196dbdf99950843c9cfccbcf99bb0e2e02c549eac9aa45a1ee27`  
		Last Modified: Thu, 23 Oct 2025 23:28:26 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23083dff4142aa95c1af480f64c7016930c4d4334412e754b13fdc90d34a5bb4`  
		Last Modified: Thu, 23 Oct 2025 23:28:26 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b60e85f50a3310c9644e0f4ef8ac7ca6399ac79bdc8b354f9a4b7fd4c85e26`  
		Last Modified: Thu, 23 Oct 2025 23:28:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d232c9f1aacee2e91a2dad24d85208d8cb3d9b9d4f4cf84b8805b9e0867184b`  
		Last Modified: Thu, 23 Oct 2025 23:28:26 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0458b551cbb0bebf370eeed7a4b45fb35f2a58d43071bd9f59c43b3e6753996`  
		Last Modified: Thu, 23 Oct 2025 23:28:26 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:817d7b611e78bc559333bd8d75344334090e61f28621c714915ec0faef12019a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:623b41d0d0bc8627005a2cea9e9911e98523b7e5bfc0c2ff597f4ea9e852dcdb`

```dockerfile
```

-	Layers:
	-	`sha256:91da8fef60fa485696e72b09a8649f7c6a2f510c0d95c4fbebc5be8c87071166`  
		Last Modified: Fri, 24 Oct 2025 00:49:25 GMT  
		Size: 26.1 KB (26071 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.9.4-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:7617a68234240ab5063f7040b050882cb89ed7ba7f2f23fee27005ddf5742c3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214122062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157073ed1af7b6df6aa4d62bbee55990144981e8b2a8be520fd3ea59758aa2c6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 23 Oct 2025 16:06:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 23 Oct 2025 16:06:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
ARG REPO_CHANNEL=stable
# Thu, 23 Oct 2025 16:06:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 23 Oct 2025 16:06:50 GMT
ARG VERSION=25.9.4.58
# Thu, 23 Oct 2025 16:06:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
ENV LANG=en_US.UTF-8
# Thu, 23 Oct 2025 16:06:50 GMT
ENV TZ=UTC
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 23 Oct 2025 16:06:50 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 23 Oct 2025 16:06:50 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 23 Oct 2025 16:06:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51dd8ef4596e241d8da0b34e2429acfbd000eb915cfdf673912ea44c90a0e5d3`  
		Last Modified: Thu, 23 Oct 2025 21:27:16 GMT  
		Size: 7.6 MB (7576738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04df4dc5f8980801074e5484109b1670c9da98e4a322fa4325a88b1e780e62c6`  
		Last Modified: Thu, 23 Oct 2025 21:49:54 GMT  
		Size: 178.3 MB (178292196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4338714d7e65f209c56e194a18f88f02c1000565a7fef4aa4a5ebd26c0dd6c`  
		Last Modified: Thu, 23 Oct 2025 21:27:15 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5288159d8914a691a503723d40cb4a6132c77e1709c70aa636f52d093f30b8`  
		Last Modified: Thu, 23 Oct 2025 21:27:15 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39947de51651e74c4d02f0929ea799a32a86e474dac339c314b841d667eff2f`  
		Last Modified: Thu, 23 Oct 2025 21:27:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7ad64f931385c578056a088c2b1e1deb0ebc99913af56e39de25c31d8d72ff`  
		Last Modified: Thu, 23 Oct 2025 21:27:16 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b984804c5d0ae90d01cddb5a92e5b8a4cedf46d3959c4ad9a5a426fecdd30d8`  
		Last Modified: Thu, 23 Oct 2025 21:27:15 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9645d0ed6d160bd7c3b9e789d847cf7e7e062c54b2face2e04cdbac20d9143ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:216484c23ff0507e301a25fa2e62b2dc760afbeac4a3b21bc62abcb73dc0ae07`

```dockerfile
```

-	Layers:
	-	`sha256:ece05afee5ab01587a237add3de9abd28f441770e00551740eee672f5b147dbb`  
		Last Modified: Thu, 23 Oct 2025 21:49:26 GMT  
		Size: 26.3 KB (26283 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.9.4.58`

```console
$ docker pull clickhouse@sha256:314fccc9ac7d95d42e2c8acd352554c7dbbf18272b51e00745a05da8e5b253d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.9.4.58` - linux; amd64

```console
$ docker pull clickhouse@sha256:5625912305fbc1f15b3d3f2583b6c762ea6e55234be9e7453facdaf71854045e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.8 MB (228833641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d61b4231cd63c90d1a1d1182e7225fd8b7cc8bf9ae1b887b907027efbac11a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 23 Oct 2025 16:06:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 23 Oct 2025 16:06:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
ARG REPO_CHANNEL=stable
# Thu, 23 Oct 2025 16:06:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 23 Oct 2025 16:06:50 GMT
ARG VERSION=25.9.4.58
# Thu, 23 Oct 2025 16:06:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
ENV LANG=en_US.UTF-8
# Thu, 23 Oct 2025 16:06:50 GMT
ENV TZ=UTC
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 23 Oct 2025 16:06:50 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 23 Oct 2025 16:06:50 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 23 Oct 2025 16:06:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:448c320ee0ed6369efabdcd6e80936019eeed85a13fb4e3481675029a1abef27`  
		Last Modified: Thu, 23 Oct 2025 23:28:27 GMT  
		Size: 7.6 MB (7598389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2263f88f7716a380550c6778749c9a44d41f29f768b2792302aa28c1a22e403`  
		Last Modified: Fri, 24 Oct 2025 00:49:58 GMT  
		Size: 190.8 MB (190828405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61452f93f2c196dbdf99950843c9cfccbcf99bb0e2e02c549eac9aa45a1ee27`  
		Last Modified: Thu, 23 Oct 2025 23:28:26 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23083dff4142aa95c1af480f64c7016930c4d4334412e754b13fdc90d34a5bb4`  
		Last Modified: Thu, 23 Oct 2025 23:28:26 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b60e85f50a3310c9644e0f4ef8ac7ca6399ac79bdc8b354f9a4b7fd4c85e26`  
		Last Modified: Thu, 23 Oct 2025 23:28:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d232c9f1aacee2e91a2dad24d85208d8cb3d9b9d4f4cf84b8805b9e0867184b`  
		Last Modified: Thu, 23 Oct 2025 23:28:26 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0458b551cbb0bebf370eeed7a4b45fb35f2a58d43071bd9f59c43b3e6753996`  
		Last Modified: Thu, 23 Oct 2025 23:28:26 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9.4.58` - unknown; unknown

```console
$ docker pull clickhouse@sha256:817d7b611e78bc559333bd8d75344334090e61f28621c714915ec0faef12019a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:623b41d0d0bc8627005a2cea9e9911e98523b7e5bfc0c2ff597f4ea9e852dcdb`

```dockerfile
```

-	Layers:
	-	`sha256:91da8fef60fa485696e72b09a8649f7c6a2f510c0d95c4fbebc5be8c87071166`  
		Last Modified: Fri, 24 Oct 2025 00:49:25 GMT  
		Size: 26.1 KB (26071 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.9.4.58` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:7617a68234240ab5063f7040b050882cb89ed7ba7f2f23fee27005ddf5742c3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214122062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157073ed1af7b6df6aa4d62bbee55990144981e8b2a8be520fd3ea59758aa2c6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 23 Oct 2025 16:06:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 23 Oct 2025 16:06:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
ARG REPO_CHANNEL=stable
# Thu, 23 Oct 2025 16:06:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 23 Oct 2025 16:06:50 GMT
ARG VERSION=25.9.4.58
# Thu, 23 Oct 2025 16:06:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
ENV LANG=en_US.UTF-8
# Thu, 23 Oct 2025 16:06:50 GMT
ENV TZ=UTC
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 23 Oct 2025 16:06:50 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 23 Oct 2025 16:06:50 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 23 Oct 2025 16:06:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51dd8ef4596e241d8da0b34e2429acfbd000eb915cfdf673912ea44c90a0e5d3`  
		Last Modified: Thu, 23 Oct 2025 21:27:16 GMT  
		Size: 7.6 MB (7576738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04df4dc5f8980801074e5484109b1670c9da98e4a322fa4325a88b1e780e62c6`  
		Last Modified: Thu, 23 Oct 2025 21:49:54 GMT  
		Size: 178.3 MB (178292196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4338714d7e65f209c56e194a18f88f02c1000565a7fef4aa4a5ebd26c0dd6c`  
		Last Modified: Thu, 23 Oct 2025 21:27:15 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5288159d8914a691a503723d40cb4a6132c77e1709c70aa636f52d093f30b8`  
		Last Modified: Thu, 23 Oct 2025 21:27:15 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39947de51651e74c4d02f0929ea799a32a86e474dac339c314b841d667eff2f`  
		Last Modified: Thu, 23 Oct 2025 21:27:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7ad64f931385c578056a088c2b1e1deb0ebc99913af56e39de25c31d8d72ff`  
		Last Modified: Thu, 23 Oct 2025 21:27:16 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b984804c5d0ae90d01cddb5a92e5b8a4cedf46d3959c4ad9a5a426fecdd30d8`  
		Last Modified: Thu, 23 Oct 2025 21:27:15 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9.4.58` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9645d0ed6d160bd7c3b9e789d847cf7e7e062c54b2face2e04cdbac20d9143ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:216484c23ff0507e301a25fa2e62b2dc760afbeac4a3b21bc62abcb73dc0ae07`

```dockerfile
```

-	Layers:
	-	`sha256:ece05afee5ab01587a237add3de9abd28f441770e00551740eee672f5b147dbb`  
		Last Modified: Thu, 23 Oct 2025 21:49:26 GMT  
		Size: 26.3 KB (26283 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.9.4.58-jammy`

```console
$ docker pull clickhouse@sha256:314fccc9ac7d95d42e2c8acd352554c7dbbf18272b51e00745a05da8e5b253d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.9.4.58-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:5625912305fbc1f15b3d3f2583b6c762ea6e55234be9e7453facdaf71854045e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.8 MB (228833641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d61b4231cd63c90d1a1d1182e7225fd8b7cc8bf9ae1b887b907027efbac11a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 23 Oct 2025 16:06:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 23 Oct 2025 16:06:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
ARG REPO_CHANNEL=stable
# Thu, 23 Oct 2025 16:06:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 23 Oct 2025 16:06:50 GMT
ARG VERSION=25.9.4.58
# Thu, 23 Oct 2025 16:06:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
ENV LANG=en_US.UTF-8
# Thu, 23 Oct 2025 16:06:50 GMT
ENV TZ=UTC
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 23 Oct 2025 16:06:50 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 23 Oct 2025 16:06:50 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 23 Oct 2025 16:06:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:448c320ee0ed6369efabdcd6e80936019eeed85a13fb4e3481675029a1abef27`  
		Last Modified: Thu, 23 Oct 2025 23:28:27 GMT  
		Size: 7.6 MB (7598389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2263f88f7716a380550c6778749c9a44d41f29f768b2792302aa28c1a22e403`  
		Last Modified: Fri, 24 Oct 2025 00:49:58 GMT  
		Size: 190.8 MB (190828405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61452f93f2c196dbdf99950843c9cfccbcf99bb0e2e02c549eac9aa45a1ee27`  
		Last Modified: Thu, 23 Oct 2025 23:28:26 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23083dff4142aa95c1af480f64c7016930c4d4334412e754b13fdc90d34a5bb4`  
		Last Modified: Thu, 23 Oct 2025 23:28:26 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b60e85f50a3310c9644e0f4ef8ac7ca6399ac79bdc8b354f9a4b7fd4c85e26`  
		Last Modified: Thu, 23 Oct 2025 23:28:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d232c9f1aacee2e91a2dad24d85208d8cb3d9b9d4f4cf84b8805b9e0867184b`  
		Last Modified: Thu, 23 Oct 2025 23:28:26 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0458b551cbb0bebf370eeed7a4b45fb35f2a58d43071bd9f59c43b3e6753996`  
		Last Modified: Thu, 23 Oct 2025 23:28:26 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9.4.58-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:817d7b611e78bc559333bd8d75344334090e61f28621c714915ec0faef12019a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:623b41d0d0bc8627005a2cea9e9911e98523b7e5bfc0c2ff597f4ea9e852dcdb`

```dockerfile
```

-	Layers:
	-	`sha256:91da8fef60fa485696e72b09a8649f7c6a2f510c0d95c4fbebc5be8c87071166`  
		Last Modified: Fri, 24 Oct 2025 00:49:25 GMT  
		Size: 26.1 KB (26071 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.9.4.58-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:7617a68234240ab5063f7040b050882cb89ed7ba7f2f23fee27005ddf5742c3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214122062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157073ed1af7b6df6aa4d62bbee55990144981e8b2a8be520fd3ea59758aa2c6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 23 Oct 2025 16:06:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 23 Oct 2025 16:06:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
ARG REPO_CHANNEL=stable
# Thu, 23 Oct 2025 16:06:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 23 Oct 2025 16:06:50 GMT
ARG VERSION=25.9.4.58
# Thu, 23 Oct 2025 16:06:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
ENV LANG=en_US.UTF-8
# Thu, 23 Oct 2025 16:06:50 GMT
ENV TZ=UTC
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 23 Oct 2025 16:06:50 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 23 Oct 2025 16:06:50 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 23 Oct 2025 16:06:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51dd8ef4596e241d8da0b34e2429acfbd000eb915cfdf673912ea44c90a0e5d3`  
		Last Modified: Thu, 23 Oct 2025 21:27:16 GMT  
		Size: 7.6 MB (7576738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04df4dc5f8980801074e5484109b1670c9da98e4a322fa4325a88b1e780e62c6`  
		Last Modified: Thu, 23 Oct 2025 21:49:54 GMT  
		Size: 178.3 MB (178292196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4338714d7e65f209c56e194a18f88f02c1000565a7fef4aa4a5ebd26c0dd6c`  
		Last Modified: Thu, 23 Oct 2025 21:27:15 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5288159d8914a691a503723d40cb4a6132c77e1709c70aa636f52d093f30b8`  
		Last Modified: Thu, 23 Oct 2025 21:27:15 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39947de51651e74c4d02f0929ea799a32a86e474dac339c314b841d667eff2f`  
		Last Modified: Thu, 23 Oct 2025 21:27:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7ad64f931385c578056a088c2b1e1deb0ebc99913af56e39de25c31d8d72ff`  
		Last Modified: Thu, 23 Oct 2025 21:27:16 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b984804c5d0ae90d01cddb5a92e5b8a4cedf46d3959c4ad9a5a426fecdd30d8`  
		Last Modified: Thu, 23 Oct 2025 21:27:15 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9.4.58-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9645d0ed6d160bd7c3b9e789d847cf7e7e062c54b2face2e04cdbac20d9143ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:216484c23ff0507e301a25fa2e62b2dc760afbeac4a3b21bc62abcb73dc0ae07`

```dockerfile
```

-	Layers:
	-	`sha256:ece05afee5ab01587a237add3de9abd28f441770e00551740eee672f5b147dbb`  
		Last Modified: Thu, 23 Oct 2025 21:49:26 GMT  
		Size: 26.3 KB (26283 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:jammy`

```console
$ docker pull clickhouse@sha256:314fccc9ac7d95d42e2c8acd352554c7dbbf18272b51e00745a05da8e5b253d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:5625912305fbc1f15b3d3f2583b6c762ea6e55234be9e7453facdaf71854045e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.8 MB (228833641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d61b4231cd63c90d1a1d1182e7225fd8b7cc8bf9ae1b887b907027efbac11a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 23 Oct 2025 16:06:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 23 Oct 2025 16:06:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
ARG REPO_CHANNEL=stable
# Thu, 23 Oct 2025 16:06:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 23 Oct 2025 16:06:50 GMT
ARG VERSION=25.9.4.58
# Thu, 23 Oct 2025 16:06:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
ENV LANG=en_US.UTF-8
# Thu, 23 Oct 2025 16:06:50 GMT
ENV TZ=UTC
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 23 Oct 2025 16:06:50 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 23 Oct 2025 16:06:50 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 23 Oct 2025 16:06:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:448c320ee0ed6369efabdcd6e80936019eeed85a13fb4e3481675029a1abef27`  
		Last Modified: Thu, 23 Oct 2025 23:28:27 GMT  
		Size: 7.6 MB (7598389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2263f88f7716a380550c6778749c9a44d41f29f768b2792302aa28c1a22e403`  
		Last Modified: Fri, 24 Oct 2025 00:49:58 GMT  
		Size: 190.8 MB (190828405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61452f93f2c196dbdf99950843c9cfccbcf99bb0e2e02c549eac9aa45a1ee27`  
		Last Modified: Thu, 23 Oct 2025 23:28:26 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23083dff4142aa95c1af480f64c7016930c4d4334412e754b13fdc90d34a5bb4`  
		Last Modified: Thu, 23 Oct 2025 23:28:26 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b60e85f50a3310c9644e0f4ef8ac7ca6399ac79bdc8b354f9a4b7fd4c85e26`  
		Last Modified: Thu, 23 Oct 2025 23:28:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d232c9f1aacee2e91a2dad24d85208d8cb3d9b9d4f4cf84b8805b9e0867184b`  
		Last Modified: Thu, 23 Oct 2025 23:28:26 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0458b551cbb0bebf370eeed7a4b45fb35f2a58d43071bd9f59c43b3e6753996`  
		Last Modified: Thu, 23 Oct 2025 23:28:26 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:817d7b611e78bc559333bd8d75344334090e61f28621c714915ec0faef12019a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:623b41d0d0bc8627005a2cea9e9911e98523b7e5bfc0c2ff597f4ea9e852dcdb`

```dockerfile
```

-	Layers:
	-	`sha256:91da8fef60fa485696e72b09a8649f7c6a2f510c0d95c4fbebc5be8c87071166`  
		Last Modified: Fri, 24 Oct 2025 00:49:25 GMT  
		Size: 26.1 KB (26071 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:7617a68234240ab5063f7040b050882cb89ed7ba7f2f23fee27005ddf5742c3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214122062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157073ed1af7b6df6aa4d62bbee55990144981e8b2a8be520fd3ea59758aa2c6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 23 Oct 2025 16:06:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 23 Oct 2025 16:06:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
ARG REPO_CHANNEL=stable
# Thu, 23 Oct 2025 16:06:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 23 Oct 2025 16:06:50 GMT
ARG VERSION=25.9.4.58
# Thu, 23 Oct 2025 16:06:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
ENV LANG=en_US.UTF-8
# Thu, 23 Oct 2025 16:06:50 GMT
ENV TZ=UTC
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 23 Oct 2025 16:06:50 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 23 Oct 2025 16:06:50 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 23 Oct 2025 16:06:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51dd8ef4596e241d8da0b34e2429acfbd000eb915cfdf673912ea44c90a0e5d3`  
		Last Modified: Thu, 23 Oct 2025 21:27:16 GMT  
		Size: 7.6 MB (7576738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04df4dc5f8980801074e5484109b1670c9da98e4a322fa4325a88b1e780e62c6`  
		Last Modified: Thu, 23 Oct 2025 21:49:54 GMT  
		Size: 178.3 MB (178292196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4338714d7e65f209c56e194a18f88f02c1000565a7fef4aa4a5ebd26c0dd6c`  
		Last Modified: Thu, 23 Oct 2025 21:27:15 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5288159d8914a691a503723d40cb4a6132c77e1709c70aa636f52d093f30b8`  
		Last Modified: Thu, 23 Oct 2025 21:27:15 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39947de51651e74c4d02f0929ea799a32a86e474dac339c314b841d667eff2f`  
		Last Modified: Thu, 23 Oct 2025 21:27:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7ad64f931385c578056a088c2b1e1deb0ebc99913af56e39de25c31d8d72ff`  
		Last Modified: Thu, 23 Oct 2025 21:27:16 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b984804c5d0ae90d01cddb5a92e5b8a4cedf46d3959c4ad9a5a426fecdd30d8`  
		Last Modified: Thu, 23 Oct 2025 21:27:15 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9645d0ed6d160bd7c3b9e789d847cf7e7e062c54b2face2e04cdbac20d9143ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:216484c23ff0507e301a25fa2e62b2dc760afbeac4a3b21bc62abcb73dc0ae07`

```dockerfile
```

-	Layers:
	-	`sha256:ece05afee5ab01587a237add3de9abd28f441770e00551740eee672f5b147dbb`  
		Last Modified: Thu, 23 Oct 2025 21:49:26 GMT  
		Size: 26.3 KB (26283 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:314fccc9ac7d95d42e2c8acd352554c7dbbf18272b51e00745a05da8e5b253d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

```console
$ docker pull clickhouse@sha256:5625912305fbc1f15b3d3f2583b6c762ea6e55234be9e7453facdaf71854045e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.8 MB (228833641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d61b4231cd63c90d1a1d1182e7225fd8b7cc8bf9ae1b887b907027efbac11a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 23 Oct 2025 16:06:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 23 Oct 2025 16:06:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
ARG REPO_CHANNEL=stable
# Thu, 23 Oct 2025 16:06:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 23 Oct 2025 16:06:50 GMT
ARG VERSION=25.9.4.58
# Thu, 23 Oct 2025 16:06:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
ENV LANG=en_US.UTF-8
# Thu, 23 Oct 2025 16:06:50 GMT
ENV TZ=UTC
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 23 Oct 2025 16:06:50 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 23 Oct 2025 16:06:50 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 23 Oct 2025 16:06:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:448c320ee0ed6369efabdcd6e80936019eeed85a13fb4e3481675029a1abef27`  
		Last Modified: Thu, 23 Oct 2025 23:28:27 GMT  
		Size: 7.6 MB (7598389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2263f88f7716a380550c6778749c9a44d41f29f768b2792302aa28c1a22e403`  
		Last Modified: Fri, 24 Oct 2025 00:49:58 GMT  
		Size: 190.8 MB (190828405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61452f93f2c196dbdf99950843c9cfccbcf99bb0e2e02c549eac9aa45a1ee27`  
		Last Modified: Thu, 23 Oct 2025 23:28:26 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23083dff4142aa95c1af480f64c7016930c4d4334412e754b13fdc90d34a5bb4`  
		Last Modified: Thu, 23 Oct 2025 23:28:26 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b60e85f50a3310c9644e0f4ef8ac7ca6399ac79bdc8b354f9a4b7fd4c85e26`  
		Last Modified: Thu, 23 Oct 2025 23:28:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d232c9f1aacee2e91a2dad24d85208d8cb3d9b9d4f4cf84b8805b9e0867184b`  
		Last Modified: Thu, 23 Oct 2025 23:28:26 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0458b551cbb0bebf370eeed7a4b45fb35f2a58d43071bd9f59c43b3e6753996`  
		Last Modified: Thu, 23 Oct 2025 23:28:26 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:817d7b611e78bc559333bd8d75344334090e61f28621c714915ec0faef12019a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:623b41d0d0bc8627005a2cea9e9911e98523b7e5bfc0c2ff597f4ea9e852dcdb`

```dockerfile
```

-	Layers:
	-	`sha256:91da8fef60fa485696e72b09a8649f7c6a2f510c0d95c4fbebc5be8c87071166`  
		Last Modified: Fri, 24 Oct 2025 00:49:25 GMT  
		Size: 26.1 KB (26071 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:7617a68234240ab5063f7040b050882cb89ed7ba7f2f23fee27005ddf5742c3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214122062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157073ed1af7b6df6aa4d62bbee55990144981e8b2a8be520fd3ea59758aa2c6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 23 Oct 2025 16:06:50 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 23 Oct 2025 16:06:50 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
ARG REPO_CHANNEL=stable
# Thu, 23 Oct 2025 16:06:50 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 23 Oct 2025 16:06:50 GMT
ARG VERSION=25.9.4.58
# Thu, 23 Oct 2025 16:06:50 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
ENV LANG=en_US.UTF-8
# Thu, 23 Oct 2025 16:06:50 GMT
ENV TZ=UTC
# Thu, 23 Oct 2025 16:06:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.4.58 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 23 Oct 2025 16:06:50 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 23 Oct 2025 16:06:50 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 23 Oct 2025 16:06:50 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 23 Oct 2025 16:06:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51dd8ef4596e241d8da0b34e2429acfbd000eb915cfdf673912ea44c90a0e5d3`  
		Last Modified: Thu, 23 Oct 2025 21:27:16 GMT  
		Size: 7.6 MB (7576738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04df4dc5f8980801074e5484109b1670c9da98e4a322fa4325a88b1e780e62c6`  
		Last Modified: Thu, 23 Oct 2025 21:49:54 GMT  
		Size: 178.3 MB (178292196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4338714d7e65f209c56e194a18f88f02c1000565a7fef4aa4a5ebd26c0dd6c`  
		Last Modified: Thu, 23 Oct 2025 21:27:15 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5288159d8914a691a503723d40cb4a6132c77e1709c70aa636f52d093f30b8`  
		Last Modified: Thu, 23 Oct 2025 21:27:15 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39947de51651e74c4d02f0929ea799a32a86e474dac339c314b841d667eff2f`  
		Last Modified: Thu, 23 Oct 2025 21:27:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7ad64f931385c578056a088c2b1e1deb0ebc99913af56e39de25c31d8d72ff`  
		Last Modified: Thu, 23 Oct 2025 21:27:16 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b984804c5d0ae90d01cddb5a92e5b8a4cedf46d3959c4ad9a5a426fecdd30d8`  
		Last Modified: Thu, 23 Oct 2025 21:27:15 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9645d0ed6d160bd7c3b9e789d847cf7e7e062c54b2face2e04cdbac20d9143ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:216484c23ff0507e301a25fa2e62b2dc760afbeac4a3b21bc62abcb73dc0ae07`

```dockerfile
```

-	Layers:
	-	`sha256:ece05afee5ab01587a237add3de9abd28f441770e00551740eee672f5b147dbb`  
		Last Modified: Thu, 23 Oct 2025 21:49:26 GMT  
		Size: 26.3 KB (26283 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts`

```console
$ docker pull clickhouse@sha256:3ad7dba29b919c092ccdcbc615b154947ee650b98db766f0b02d010876911332
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts` - linux; amd64

```console
$ docker pull clickhouse@sha256:014ce3c7fb6e10da19a42c0eb61995b05f65af48d7492a29d2dc2731c6733c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227813563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36230d3191dfe2429e3ca84290a3205fece0c511fac0c1b24fb08a95ce66389a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 09 Oct 2025 16:08:11 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 09 Oct 2025 16:08:11 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ARG REPO_CHANNEL=stable
# Thu, 09 Oct 2025 16:08:11 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 09 Oct 2025 16:08:11 GMT
ARG VERSION=25.8.10.7
# Thu, 09 Oct 2025 16:08:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Oct 2025 16:08:11 GMT
ENV TZ=UTC
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 09 Oct 2025 16:08:11 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 09 Oct 2025 16:08:11 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 09 Oct 2025 16:08:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbf784615546088a9911e2e6670b12bb2add7f11c869084f50f43701472019a`  
		Last Modified: Thu, 09 Oct 2025 18:04:09 GMT  
		Size: 7.6 MB (7598394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f763341119f8e483bffb29e2067fcce227d7cd93d9af59e70d24620311625033`  
		Last Modified: Thu, 09 Oct 2025 18:50:04 GMT  
		Size: 189.8 MB (189808325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2195d16840bfd88c5050cdbd49f3c79cb23cea6fd82c57e53161b92f14330340`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f28b765b4124de3928ce25e6fdfadebc679ab186b753270194ebd384b24795`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc13c07dc3b1e7e4a22527e28a0adea995540d847256c197657c2d4e2ee4856`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109b8a5c3d24e5d248127a8a9090bf7ba3a3528858793c0670cf4320318637cb`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202891ea53457fd16b78e2c09483a2c30bbcf05a7c9d5b2660e1ea0f9703e42e`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f61f7a88a9cc5bf543e509c175c766faaa2c91bf67bfa430604ab6dd26566077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbdf48d096588bf66f39110ea1fa67d75ea2d3afe30bc4561509b26076da889e`

```dockerfile
```

-	Layers:
	-	`sha256:0c6033682af199025495d6f753aee1c3f90090f3f577fce9da3921f261ea9b51`  
		Last Modified: Thu, 09 Oct 2025 18:49:35 GMT  
		Size: 26.1 KB (26077 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:984c68e62c33767896b89a40a512651046ddb49c395de36617d3065d9d53e83d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.6 MB (212621178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30bd20aebbd2224437c2203ebba4b664b536234bd0127f2963f74d7c4046334`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 09 Oct 2025 16:08:11 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 09 Oct 2025 16:08:11 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ARG REPO_CHANNEL=stable
# Thu, 09 Oct 2025 16:08:11 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 09 Oct 2025 16:08:11 GMT
ARG VERSION=25.8.10.7
# Thu, 09 Oct 2025 16:08:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Oct 2025 16:08:11 GMT
ENV TZ=UTC
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 09 Oct 2025 16:08:11 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 09 Oct 2025 16:08:11 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 09 Oct 2025 16:08:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1153d40948259afc0f2c882331af600a3c3eb3d680f0105a07342bc0d60245`  
		Last Modified: Thu, 09 Oct 2025 18:49:48 GMT  
		Size: 7.6 MB (7576753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf275d0555ec5fca1465a172f1d0f251796fa4f951c45863ee6c2efb21ac066`  
		Last Modified: Thu, 09 Oct 2025 18:49:58 GMT  
		Size: 176.8 MB (176791297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44250edf6e172027a8a7e70ec848942d44e04a45bf505d6f1a5cb5a2ee4c40c`  
		Last Modified: Thu, 09 Oct 2025 18:18:07 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2b4e32c07938d944c59bf2745534bbc75ae74d70c1dc2328059fddb0007520`  
		Last Modified: Thu, 09 Oct 2025 18:18:18 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243bd52d3cccaf7499339160160d3adbb5b5f0146d65b50ef0e2cbb8ce33be90`  
		Last Modified: Thu, 09 Oct 2025 18:18:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cee2da3dd6928562361b1adef7b38f62c05b53eb7651545f8ed7c02b39e2084`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d05804c22b94a1271693b697e0dfd4eb247ac50f9ba72001a9f069033cf0ee5`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3f570dc1ce728a238ca567f82481c0df2f9566081a2405e26db566018a746824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11fa3a06888b684dee3cc392f2a56b6a32a4af4e66e9280d6171e735a00e7c01`

```dockerfile
```

-	Layers:
	-	`sha256:d3c9f2a0afde4bc153c70eabf341024743f43f3f54346643c00867383cacac14`  
		Last Modified: Thu, 09 Oct 2025 18:49:40 GMT  
		Size: 26.3 KB (26288 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts-jammy`

```console
$ docker pull clickhouse@sha256:3ad7dba29b919c092ccdcbc615b154947ee650b98db766f0b02d010876911332
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:014ce3c7fb6e10da19a42c0eb61995b05f65af48d7492a29d2dc2731c6733c92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227813563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36230d3191dfe2429e3ca84290a3205fece0c511fac0c1b24fb08a95ce66389a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 09 Oct 2025 16:08:11 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 09 Oct 2025 16:08:11 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ARG REPO_CHANNEL=stable
# Thu, 09 Oct 2025 16:08:11 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 09 Oct 2025 16:08:11 GMT
ARG VERSION=25.8.10.7
# Thu, 09 Oct 2025 16:08:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Oct 2025 16:08:11 GMT
ENV TZ=UTC
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 09 Oct 2025 16:08:11 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 09 Oct 2025 16:08:11 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 09 Oct 2025 16:08:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbf784615546088a9911e2e6670b12bb2add7f11c869084f50f43701472019a`  
		Last Modified: Thu, 09 Oct 2025 18:04:09 GMT  
		Size: 7.6 MB (7598394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f763341119f8e483bffb29e2067fcce227d7cd93d9af59e70d24620311625033`  
		Last Modified: Thu, 09 Oct 2025 18:50:04 GMT  
		Size: 189.8 MB (189808325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2195d16840bfd88c5050cdbd49f3c79cb23cea6fd82c57e53161b92f14330340`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f28b765b4124de3928ce25e6fdfadebc679ab186b753270194ebd384b24795`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc13c07dc3b1e7e4a22527e28a0adea995540d847256c197657c2d4e2ee4856`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109b8a5c3d24e5d248127a8a9090bf7ba3a3528858793c0670cf4320318637cb`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202891ea53457fd16b78e2c09483a2c30bbcf05a7c9d5b2660e1ea0f9703e42e`  
		Last Modified: Thu, 09 Oct 2025 18:05:04 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f61f7a88a9cc5bf543e509c175c766faaa2c91bf67bfa430604ab6dd26566077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbdf48d096588bf66f39110ea1fa67d75ea2d3afe30bc4561509b26076da889e`

```dockerfile
```

-	Layers:
	-	`sha256:0c6033682af199025495d6f753aee1c3f90090f3f577fce9da3921f261ea9b51`  
		Last Modified: Thu, 09 Oct 2025 18:49:35 GMT  
		Size: 26.1 KB (26077 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:984c68e62c33767896b89a40a512651046ddb49c395de36617d3065d9d53e83d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.6 MB (212621178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30bd20aebbd2224437c2203ebba4b664b536234bd0127f2963f74d7c4046334`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 09 Oct 2025 16:08:11 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 09 Oct 2025 16:08:11 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ARG REPO_CHANNEL=stable
# Thu, 09 Oct 2025 16:08:11 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 09 Oct 2025 16:08:11 GMT
ARG VERSION=25.8.10.7
# Thu, 09 Oct 2025 16:08:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Oct 2025 16:08:11 GMT
ENV TZ=UTC
# Thu, 09 Oct 2025 16:08:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.10.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 09 Oct 2025 16:08:11 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 09 Oct 2025 16:08:11 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 09 Oct 2025 16:08:11 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 09 Oct 2025 16:08:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1153d40948259afc0f2c882331af600a3c3eb3d680f0105a07342bc0d60245`  
		Last Modified: Thu, 09 Oct 2025 18:49:48 GMT  
		Size: 7.6 MB (7576753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf275d0555ec5fca1465a172f1d0f251796fa4f951c45863ee6c2efb21ac066`  
		Last Modified: Thu, 09 Oct 2025 18:49:58 GMT  
		Size: 176.8 MB (176791297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44250edf6e172027a8a7e70ec848942d44e04a45bf505d6f1a5cb5a2ee4c40c`  
		Last Modified: Thu, 09 Oct 2025 18:18:07 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2b4e32c07938d944c59bf2745534bbc75ae74d70c1dc2328059fddb0007520`  
		Last Modified: Thu, 09 Oct 2025 18:18:18 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243bd52d3cccaf7499339160160d3adbb5b5f0146d65b50ef0e2cbb8ce33be90`  
		Last Modified: Thu, 09 Oct 2025 18:18:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cee2da3dd6928562361b1adef7b38f62c05b53eb7651545f8ed7c02b39e2084`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d05804c22b94a1271693b697e0dfd4eb247ac50f9ba72001a9f069033cf0ee5`  
		Last Modified: Thu, 09 Oct 2025 18:02:04 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3f570dc1ce728a238ca567f82481c0df2f9566081a2405e26db566018a746824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11fa3a06888b684dee3cc392f2a56b6a32a4af4e66e9280d6171e735a00e7c01`

```dockerfile
```

-	Layers:
	-	`sha256:d3c9f2a0afde4bc153c70eabf341024743f43f3f54346643c00867383cacac14`  
		Last Modified: Thu, 09 Oct 2025 18:49:40 GMT  
		Size: 26.3 KB (26288 bytes)  
		MIME: application/vnd.in-toto+json
