<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clickhouse`

-	[`clickhouse:25.3`](#clickhouse253)
-	[`clickhouse:25.3-jammy`](#clickhouse253-jammy)
-	[`clickhouse:25.3.8`](#clickhouse2538)
-	[`clickhouse:25.3.8-jammy`](#clickhouse2538-jammy)
-	[`clickhouse:25.3.8.23`](#clickhouse253823)
-	[`clickhouse:25.3.8.23-jammy`](#clickhouse253823-jammy)
-	[`clickhouse:25.7`](#clickhouse257)
-	[`clickhouse:25.7-jammy`](#clickhouse257-jammy)
-	[`clickhouse:25.7.8`](#clickhouse2578)
-	[`clickhouse:25.7.8-jammy`](#clickhouse2578-jammy)
-	[`clickhouse:25.7.8.71`](#clickhouse257871)
-	[`clickhouse:25.7.8.71-jammy`](#clickhouse257871-jammy)
-	[`clickhouse:25.8`](#clickhouse258)
-	[`clickhouse:25.8-jammy`](#clickhouse258-jammy)
-	[`clickhouse:25.8.11`](#clickhouse25811)
-	[`clickhouse:25.8.11-jammy`](#clickhouse25811-jammy)
-	[`clickhouse:25.8.11.66`](#clickhouse2581166)
-	[`clickhouse:25.8.11.66-jammy`](#clickhouse2581166-jammy)
-	[`clickhouse:25.9`](#clickhouse259)
-	[`clickhouse:25.9-jammy`](#clickhouse259-jammy)
-	[`clickhouse:25.9.5`](#clickhouse2595)
-	[`clickhouse:25.9.5-jammy`](#clickhouse2595-jammy)
-	[`clickhouse:25.9.5.21`](#clickhouse259521)
-	[`clickhouse:25.9.5.21-jammy`](#clickhouse259521-jammy)
-	[`clickhouse:jammy`](#clickhousejammy)
-	[`clickhouse:latest`](#clickhouselatest)
-	[`clickhouse:lts`](#clickhouselts)
-	[`clickhouse:lts-jammy`](#clickhouselts-jammy)

## `clickhouse:25.3`

```console
$ docker pull clickhouse@sha256:75596f94a3db6ab6cc46ea4c9b94d7f03e1b36785a7e66bc16b7c07b589a6e32
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
$ docker pull clickhouse@sha256:4aed478be3bb7097bdc1debd209b178ecf42c37d7210d4e9648631b2579a94b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (192983547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01d35bbed0c2650693ae9c9d44da2e89dc8b42aba620b35d6de0c43ea3e01810`
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
# Thu, 30 Oct 2025 21:21:49 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 21:21:49 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 21:21:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 21:21:49 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 21:21:49 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 21:21:49 GMT
ARG VERSION=25.3.8.23
# Thu, 30 Oct 2025 21:21:49 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 21:22:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 21:22:16 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 21:22:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 21:22:16 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 21:22:16 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 21:22:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3307f657683d186c6205717bfb85eb558ca87cc25b5ec9e9e0f2a3afab8238ae`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 7.1 MB (7127222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53827a5efe698f075c2a8f84f9e910521f6c849d4e663f8bcda6c1d682998277`  
		Last Modified: Thu, 30 Oct 2025 21:49:52 GMT  
		Size: 157.6 MB (157602973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c75edbbc000a53843b7b15ecb1d209d70d5d24a28598e3ca4b43e07e2115257`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe72d435c20e30ef6acfa667b15604b77c558491fc9f904b620510017cde658`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6a66cb23d300a47ce566678ece81a979d365580649b98d8c909fff1cda80e2`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83f337947838d1b535c45aeb37402ed7a290dcfca3e3858494873cc04ab3e63`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314c2d04e787243b12ffabf5f69c468c59cd5a03651b8956fe2db0894f3d63d1`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 3.8 KB (3832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fa760c382c19e3ad290a49a7f9fcbc3da22211dbfaa1e668571cd3ffdd30a3c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea58f8008ecdd3d85019881850a1558ac37f38e694fe5712d42af495973d636`

```dockerfile
```

-	Layers:
	-	`sha256:0ae0b038ca2f160b52a976b7eaeccfa1cc67911433863762494a512c80ae316f`  
		Last Modified: Thu, 30 Oct 2025 21:49:22 GMT  
		Size: 25.4 KB (25407 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3-jammy`

```console
$ docker pull clickhouse@sha256:75596f94a3db6ab6cc46ea4c9b94d7f03e1b36785a7e66bc16b7c07b589a6e32
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
$ docker pull clickhouse@sha256:4aed478be3bb7097bdc1debd209b178ecf42c37d7210d4e9648631b2579a94b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (192983547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01d35bbed0c2650693ae9c9d44da2e89dc8b42aba620b35d6de0c43ea3e01810`
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
# Thu, 30 Oct 2025 21:21:49 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 21:21:49 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 21:21:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 21:21:49 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 21:21:49 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 21:21:49 GMT
ARG VERSION=25.3.8.23
# Thu, 30 Oct 2025 21:21:49 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 21:22:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 21:22:16 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 21:22:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 21:22:16 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 21:22:16 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 21:22:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3307f657683d186c6205717bfb85eb558ca87cc25b5ec9e9e0f2a3afab8238ae`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 7.1 MB (7127222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53827a5efe698f075c2a8f84f9e910521f6c849d4e663f8bcda6c1d682998277`  
		Last Modified: Thu, 30 Oct 2025 21:49:52 GMT  
		Size: 157.6 MB (157602973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c75edbbc000a53843b7b15ecb1d209d70d5d24a28598e3ca4b43e07e2115257`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe72d435c20e30ef6acfa667b15604b77c558491fc9f904b620510017cde658`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6a66cb23d300a47ce566678ece81a979d365580649b98d8c909fff1cda80e2`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83f337947838d1b535c45aeb37402ed7a290dcfca3e3858494873cc04ab3e63`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314c2d04e787243b12ffabf5f69c468c59cd5a03651b8956fe2db0894f3d63d1`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 3.8 KB (3832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fa760c382c19e3ad290a49a7f9fcbc3da22211dbfaa1e668571cd3ffdd30a3c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea58f8008ecdd3d85019881850a1558ac37f38e694fe5712d42af495973d636`

```dockerfile
```

-	Layers:
	-	`sha256:0ae0b038ca2f160b52a976b7eaeccfa1cc67911433863762494a512c80ae316f`  
		Last Modified: Thu, 30 Oct 2025 21:49:22 GMT  
		Size: 25.4 KB (25407 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.8`

```console
$ docker pull clickhouse@sha256:a8548516c02d91b78380d0c1a225fca03508d113ef24c72100075dc8e669dcc7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.8` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4aed478be3bb7097bdc1debd209b178ecf42c37d7210d4e9648631b2579a94b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (192983547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01d35bbed0c2650693ae9c9d44da2e89dc8b42aba620b35d6de0c43ea3e01810`
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
# Thu, 30 Oct 2025 21:21:49 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 21:21:49 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 21:21:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 21:21:49 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 21:21:49 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 21:21:49 GMT
ARG VERSION=25.3.8.23
# Thu, 30 Oct 2025 21:21:49 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 21:22:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 21:22:16 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 21:22:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 21:22:16 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 21:22:16 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 21:22:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3307f657683d186c6205717bfb85eb558ca87cc25b5ec9e9e0f2a3afab8238ae`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 7.1 MB (7127222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53827a5efe698f075c2a8f84f9e910521f6c849d4e663f8bcda6c1d682998277`  
		Last Modified: Thu, 30 Oct 2025 21:49:52 GMT  
		Size: 157.6 MB (157602973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c75edbbc000a53843b7b15ecb1d209d70d5d24a28598e3ca4b43e07e2115257`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe72d435c20e30ef6acfa667b15604b77c558491fc9f904b620510017cde658`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6a66cb23d300a47ce566678ece81a979d365580649b98d8c909fff1cda80e2`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83f337947838d1b535c45aeb37402ed7a290dcfca3e3858494873cc04ab3e63`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314c2d04e787243b12ffabf5f69c468c59cd5a03651b8956fe2db0894f3d63d1`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 3.8 KB (3832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fa760c382c19e3ad290a49a7f9fcbc3da22211dbfaa1e668571cd3ffdd30a3c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea58f8008ecdd3d85019881850a1558ac37f38e694fe5712d42af495973d636`

```dockerfile
```

-	Layers:
	-	`sha256:0ae0b038ca2f160b52a976b7eaeccfa1cc67911433863762494a512c80ae316f`  
		Last Modified: Thu, 30 Oct 2025 21:49:22 GMT  
		Size: 25.4 KB (25407 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.8-jammy`

```console
$ docker pull clickhouse@sha256:a8548516c02d91b78380d0c1a225fca03508d113ef24c72100075dc8e669dcc7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.8-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4aed478be3bb7097bdc1debd209b178ecf42c37d7210d4e9648631b2579a94b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (192983547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01d35bbed0c2650693ae9c9d44da2e89dc8b42aba620b35d6de0c43ea3e01810`
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
# Thu, 30 Oct 2025 21:21:49 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 21:21:49 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 21:21:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 21:21:49 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 21:21:49 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 21:21:49 GMT
ARG VERSION=25.3.8.23
# Thu, 30 Oct 2025 21:21:49 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 21:22:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 21:22:16 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 21:22:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 21:22:16 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 21:22:16 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 21:22:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3307f657683d186c6205717bfb85eb558ca87cc25b5ec9e9e0f2a3afab8238ae`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 7.1 MB (7127222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53827a5efe698f075c2a8f84f9e910521f6c849d4e663f8bcda6c1d682998277`  
		Last Modified: Thu, 30 Oct 2025 21:49:52 GMT  
		Size: 157.6 MB (157602973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c75edbbc000a53843b7b15ecb1d209d70d5d24a28598e3ca4b43e07e2115257`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe72d435c20e30ef6acfa667b15604b77c558491fc9f904b620510017cde658`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6a66cb23d300a47ce566678ece81a979d365580649b98d8c909fff1cda80e2`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83f337947838d1b535c45aeb37402ed7a290dcfca3e3858494873cc04ab3e63`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314c2d04e787243b12ffabf5f69c468c59cd5a03651b8956fe2db0894f3d63d1`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 3.8 KB (3832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fa760c382c19e3ad290a49a7f9fcbc3da22211dbfaa1e668571cd3ffdd30a3c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea58f8008ecdd3d85019881850a1558ac37f38e694fe5712d42af495973d636`

```dockerfile
```

-	Layers:
	-	`sha256:0ae0b038ca2f160b52a976b7eaeccfa1cc67911433863762494a512c80ae316f`  
		Last Modified: Thu, 30 Oct 2025 21:49:22 GMT  
		Size: 25.4 KB (25407 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.8.23`

```console
$ docker pull clickhouse@sha256:a8548516c02d91b78380d0c1a225fca03508d113ef24c72100075dc8e669dcc7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.8.23` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4aed478be3bb7097bdc1debd209b178ecf42c37d7210d4e9648631b2579a94b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (192983547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01d35bbed0c2650693ae9c9d44da2e89dc8b42aba620b35d6de0c43ea3e01810`
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
# Thu, 30 Oct 2025 21:21:49 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 21:21:49 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 21:21:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 21:21:49 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 21:21:49 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 21:21:49 GMT
ARG VERSION=25.3.8.23
# Thu, 30 Oct 2025 21:21:49 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 21:22:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 21:22:16 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 21:22:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 21:22:16 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 21:22:16 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 21:22:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3307f657683d186c6205717bfb85eb558ca87cc25b5ec9e9e0f2a3afab8238ae`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 7.1 MB (7127222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53827a5efe698f075c2a8f84f9e910521f6c849d4e663f8bcda6c1d682998277`  
		Last Modified: Thu, 30 Oct 2025 21:49:52 GMT  
		Size: 157.6 MB (157602973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c75edbbc000a53843b7b15ecb1d209d70d5d24a28598e3ca4b43e07e2115257`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe72d435c20e30ef6acfa667b15604b77c558491fc9f904b620510017cde658`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6a66cb23d300a47ce566678ece81a979d365580649b98d8c909fff1cda80e2`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83f337947838d1b535c45aeb37402ed7a290dcfca3e3858494873cc04ab3e63`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314c2d04e787243b12ffabf5f69c468c59cd5a03651b8956fe2db0894f3d63d1`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 3.8 KB (3832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.8.23` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fa760c382c19e3ad290a49a7f9fcbc3da22211dbfaa1e668571cd3ffdd30a3c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea58f8008ecdd3d85019881850a1558ac37f38e694fe5712d42af495973d636`

```dockerfile
```

-	Layers:
	-	`sha256:0ae0b038ca2f160b52a976b7eaeccfa1cc67911433863762494a512c80ae316f`  
		Last Modified: Thu, 30 Oct 2025 21:49:22 GMT  
		Size: 25.4 KB (25407 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.8.23-jammy`

```console
$ docker pull clickhouse@sha256:a8548516c02d91b78380d0c1a225fca03508d113ef24c72100075dc8e669dcc7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.8.23-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4aed478be3bb7097bdc1debd209b178ecf42c37d7210d4e9648631b2579a94b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (192983547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01d35bbed0c2650693ae9c9d44da2e89dc8b42aba620b35d6de0c43ea3e01810`
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
# Thu, 30 Oct 2025 21:21:49 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 21:21:49 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 21:21:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 21:21:49 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 21:21:49 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 21:21:49 GMT
ARG VERSION=25.3.8.23
# Thu, 30 Oct 2025 21:21:49 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 21:22:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 21:22:16 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 21:22:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 21:22:16 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 21:22:16 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 21:22:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3307f657683d186c6205717bfb85eb558ca87cc25b5ec9e9e0f2a3afab8238ae`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 7.1 MB (7127222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53827a5efe698f075c2a8f84f9e910521f6c849d4e663f8bcda6c1d682998277`  
		Last Modified: Thu, 30 Oct 2025 21:49:52 GMT  
		Size: 157.6 MB (157602973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c75edbbc000a53843b7b15ecb1d209d70d5d24a28598e3ca4b43e07e2115257`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe72d435c20e30ef6acfa667b15604b77c558491fc9f904b620510017cde658`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6a66cb23d300a47ce566678ece81a979d365580649b98d8c909fff1cda80e2`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83f337947838d1b535c45aeb37402ed7a290dcfca3e3858494873cc04ab3e63`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314c2d04e787243b12ffabf5f69c468c59cd5a03651b8956fe2db0894f3d63d1`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 3.8 KB (3832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.8.23-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fa760c382c19e3ad290a49a7f9fcbc3da22211dbfaa1e668571cd3ffdd30a3c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea58f8008ecdd3d85019881850a1558ac37f38e694fe5712d42af495973d636`

```dockerfile
```

-	Layers:
	-	`sha256:0ae0b038ca2f160b52a976b7eaeccfa1cc67911433863762494a512c80ae316f`  
		Last Modified: Thu, 30 Oct 2025 21:49:22 GMT  
		Size: 25.4 KB (25407 bytes)  
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
$ docker pull clickhouse@sha256:e4177e94d974c4d344d85c6ca7c4707f3dd3f1a72f5a446ff505fc4d76179381
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
$ docker pull clickhouse@sha256:a5656778631ee59482d9821f008c2f43704a533bb78ce9fabe3f9e735055b882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.6 MB (212645310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636cee591520bd679efa5bdfc5ccbbe8955c161e8ce6052107b9f0192bb2d962`
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
# Thu, 30 Oct 2025 21:21:43 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 21:21:43 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 21:21:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 21:21:43 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 21:21:43 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 21:21:43 GMT
ARG VERSION=25.8.11.66
# Thu, 30 Oct 2025 21:21:43 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 21:22:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 21:22:12 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 21:22:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 21:22:12 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 21:22:12 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 21:22:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce7ce10c9eeca1dd1885578ad8f3f6291f3732bdf5a50a8a6535af67a72e81f`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 7.6 MB (7576689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee964fa2145e136ca73e4c3796c405f427a709e6070f3f4802f8e19f6723677`  
		Last Modified: Thu, 30 Oct 2025 21:50:09 GMT  
		Size: 176.8 MB (176815492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd59e47ba03552bfa2a66ef28e55b44868ad4666ae67b5fe3e408e5c5a79ca85`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9616189aee41fb2150e3b2e7df745964d4e966fb63f6a7a431d6d848dfc358`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e163c00ab90daa2465b1046a4d0b95388778dc70b143011610dca4fb7590de31`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47157a68ab31f8dfb08a2352278276b514a9773b046ac4dca1504822e01e8856`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dda603cdd01780ad677c4f16ef238ba487aa146cd3f5d06542f066c10b93575`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:557ba9743467f6d9ecfb1670d9fb813858720e1ed9612956f837ce4eb5cf0dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30079417e65d20ad6f0ad236690d7babc98d5d1128642255422497d2ca46316f`

```dockerfile
```

-	Layers:
	-	`sha256:cdecb34f64c1ba351dec1bcc4a2182fa4b916423bfa5f3853e9f82069f25386a`  
		Last Modified: Thu, 30 Oct 2025 21:49:42 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8-jammy`

```console
$ docker pull clickhouse@sha256:e4177e94d974c4d344d85c6ca7c4707f3dd3f1a72f5a446ff505fc4d76179381
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
$ docker pull clickhouse@sha256:a5656778631ee59482d9821f008c2f43704a533bb78ce9fabe3f9e735055b882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.6 MB (212645310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636cee591520bd679efa5bdfc5ccbbe8955c161e8ce6052107b9f0192bb2d962`
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
# Thu, 30 Oct 2025 21:21:43 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 21:21:43 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 21:21:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 21:21:43 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 21:21:43 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 21:21:43 GMT
ARG VERSION=25.8.11.66
# Thu, 30 Oct 2025 21:21:43 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 21:22:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 21:22:12 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 21:22:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 21:22:12 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 21:22:12 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 21:22:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce7ce10c9eeca1dd1885578ad8f3f6291f3732bdf5a50a8a6535af67a72e81f`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 7.6 MB (7576689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee964fa2145e136ca73e4c3796c405f427a709e6070f3f4802f8e19f6723677`  
		Last Modified: Thu, 30 Oct 2025 21:50:09 GMT  
		Size: 176.8 MB (176815492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd59e47ba03552bfa2a66ef28e55b44868ad4666ae67b5fe3e408e5c5a79ca85`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9616189aee41fb2150e3b2e7df745964d4e966fb63f6a7a431d6d848dfc358`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e163c00ab90daa2465b1046a4d0b95388778dc70b143011610dca4fb7590de31`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47157a68ab31f8dfb08a2352278276b514a9773b046ac4dca1504822e01e8856`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dda603cdd01780ad677c4f16ef238ba487aa146cd3f5d06542f066c10b93575`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:557ba9743467f6d9ecfb1670d9fb813858720e1ed9612956f837ce4eb5cf0dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30079417e65d20ad6f0ad236690d7babc98d5d1128642255422497d2ca46316f`

```dockerfile
```

-	Layers:
	-	`sha256:cdecb34f64c1ba351dec1bcc4a2182fa4b916423bfa5f3853e9f82069f25386a`  
		Last Modified: Thu, 30 Oct 2025 21:49:42 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.11`

```console
$ docker pull clickhouse@sha256:5adb648f43e8d1e48394b5c5b45fe4ccda19861208abb9ea6520933447bc40a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.11` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a5656778631ee59482d9821f008c2f43704a533bb78ce9fabe3f9e735055b882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.6 MB (212645310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636cee591520bd679efa5bdfc5ccbbe8955c161e8ce6052107b9f0192bb2d962`
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
# Thu, 30 Oct 2025 21:21:43 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 21:21:43 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 21:21:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 21:21:43 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 21:21:43 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 21:21:43 GMT
ARG VERSION=25.8.11.66
# Thu, 30 Oct 2025 21:21:43 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 21:22:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 21:22:12 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 21:22:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 21:22:12 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 21:22:12 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 21:22:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce7ce10c9eeca1dd1885578ad8f3f6291f3732bdf5a50a8a6535af67a72e81f`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 7.6 MB (7576689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee964fa2145e136ca73e4c3796c405f427a709e6070f3f4802f8e19f6723677`  
		Last Modified: Thu, 30 Oct 2025 21:50:09 GMT  
		Size: 176.8 MB (176815492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd59e47ba03552bfa2a66ef28e55b44868ad4666ae67b5fe3e408e5c5a79ca85`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9616189aee41fb2150e3b2e7df745964d4e966fb63f6a7a431d6d848dfc358`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e163c00ab90daa2465b1046a4d0b95388778dc70b143011610dca4fb7590de31`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47157a68ab31f8dfb08a2352278276b514a9773b046ac4dca1504822e01e8856`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dda603cdd01780ad677c4f16ef238ba487aa146cd3f5d06542f066c10b93575`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.11` - unknown; unknown

```console
$ docker pull clickhouse@sha256:557ba9743467f6d9ecfb1670d9fb813858720e1ed9612956f837ce4eb5cf0dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30079417e65d20ad6f0ad236690d7babc98d5d1128642255422497d2ca46316f`

```dockerfile
```

-	Layers:
	-	`sha256:cdecb34f64c1ba351dec1bcc4a2182fa4b916423bfa5f3853e9f82069f25386a`  
		Last Modified: Thu, 30 Oct 2025 21:49:42 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.11-jammy`

```console
$ docker pull clickhouse@sha256:5adb648f43e8d1e48394b5c5b45fe4ccda19861208abb9ea6520933447bc40a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.11-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a5656778631ee59482d9821f008c2f43704a533bb78ce9fabe3f9e735055b882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.6 MB (212645310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636cee591520bd679efa5bdfc5ccbbe8955c161e8ce6052107b9f0192bb2d962`
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
# Thu, 30 Oct 2025 21:21:43 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 21:21:43 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 21:21:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 21:21:43 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 21:21:43 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 21:21:43 GMT
ARG VERSION=25.8.11.66
# Thu, 30 Oct 2025 21:21:43 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 21:22:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 21:22:12 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 21:22:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 21:22:12 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 21:22:12 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 21:22:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce7ce10c9eeca1dd1885578ad8f3f6291f3732bdf5a50a8a6535af67a72e81f`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 7.6 MB (7576689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee964fa2145e136ca73e4c3796c405f427a709e6070f3f4802f8e19f6723677`  
		Last Modified: Thu, 30 Oct 2025 21:50:09 GMT  
		Size: 176.8 MB (176815492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd59e47ba03552bfa2a66ef28e55b44868ad4666ae67b5fe3e408e5c5a79ca85`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9616189aee41fb2150e3b2e7df745964d4e966fb63f6a7a431d6d848dfc358`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e163c00ab90daa2465b1046a4d0b95388778dc70b143011610dca4fb7590de31`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47157a68ab31f8dfb08a2352278276b514a9773b046ac4dca1504822e01e8856`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dda603cdd01780ad677c4f16ef238ba487aa146cd3f5d06542f066c10b93575`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.11-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:557ba9743467f6d9ecfb1670d9fb813858720e1ed9612956f837ce4eb5cf0dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30079417e65d20ad6f0ad236690d7babc98d5d1128642255422497d2ca46316f`

```dockerfile
```

-	Layers:
	-	`sha256:cdecb34f64c1ba351dec1bcc4a2182fa4b916423bfa5f3853e9f82069f25386a`  
		Last Modified: Thu, 30 Oct 2025 21:49:42 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.11.66`

```console
$ docker pull clickhouse@sha256:5adb648f43e8d1e48394b5c5b45fe4ccda19861208abb9ea6520933447bc40a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.11.66` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a5656778631ee59482d9821f008c2f43704a533bb78ce9fabe3f9e735055b882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.6 MB (212645310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636cee591520bd679efa5bdfc5ccbbe8955c161e8ce6052107b9f0192bb2d962`
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
# Thu, 30 Oct 2025 21:21:43 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 21:21:43 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 21:21:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 21:21:43 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 21:21:43 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 21:21:43 GMT
ARG VERSION=25.8.11.66
# Thu, 30 Oct 2025 21:21:43 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 21:22:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 21:22:12 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 21:22:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 21:22:12 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 21:22:12 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 21:22:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce7ce10c9eeca1dd1885578ad8f3f6291f3732bdf5a50a8a6535af67a72e81f`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 7.6 MB (7576689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee964fa2145e136ca73e4c3796c405f427a709e6070f3f4802f8e19f6723677`  
		Last Modified: Thu, 30 Oct 2025 21:50:09 GMT  
		Size: 176.8 MB (176815492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd59e47ba03552bfa2a66ef28e55b44868ad4666ae67b5fe3e408e5c5a79ca85`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9616189aee41fb2150e3b2e7df745964d4e966fb63f6a7a431d6d848dfc358`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e163c00ab90daa2465b1046a4d0b95388778dc70b143011610dca4fb7590de31`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47157a68ab31f8dfb08a2352278276b514a9773b046ac4dca1504822e01e8856`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dda603cdd01780ad677c4f16ef238ba487aa146cd3f5d06542f066c10b93575`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.11.66` - unknown; unknown

```console
$ docker pull clickhouse@sha256:557ba9743467f6d9ecfb1670d9fb813858720e1ed9612956f837ce4eb5cf0dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30079417e65d20ad6f0ad236690d7babc98d5d1128642255422497d2ca46316f`

```dockerfile
```

-	Layers:
	-	`sha256:cdecb34f64c1ba351dec1bcc4a2182fa4b916423bfa5f3853e9f82069f25386a`  
		Last Modified: Thu, 30 Oct 2025 21:49:42 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.11.66-jammy`

```console
$ docker pull clickhouse@sha256:5adb648f43e8d1e48394b5c5b45fe4ccda19861208abb9ea6520933447bc40a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.11.66-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a5656778631ee59482d9821f008c2f43704a533bb78ce9fabe3f9e735055b882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.6 MB (212645310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636cee591520bd679efa5bdfc5ccbbe8955c161e8ce6052107b9f0192bb2d962`
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
# Thu, 30 Oct 2025 21:21:43 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 21:21:43 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 21:21:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 21:21:43 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 21:21:43 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 21:21:43 GMT
ARG VERSION=25.8.11.66
# Thu, 30 Oct 2025 21:21:43 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 21:22:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 21:22:12 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 21:22:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 21:22:12 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 21:22:12 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 21:22:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce7ce10c9eeca1dd1885578ad8f3f6291f3732bdf5a50a8a6535af67a72e81f`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 7.6 MB (7576689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee964fa2145e136ca73e4c3796c405f427a709e6070f3f4802f8e19f6723677`  
		Last Modified: Thu, 30 Oct 2025 21:50:09 GMT  
		Size: 176.8 MB (176815492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd59e47ba03552bfa2a66ef28e55b44868ad4666ae67b5fe3e408e5c5a79ca85`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9616189aee41fb2150e3b2e7df745964d4e966fb63f6a7a431d6d848dfc358`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e163c00ab90daa2465b1046a4d0b95388778dc70b143011610dca4fb7590de31`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47157a68ab31f8dfb08a2352278276b514a9773b046ac4dca1504822e01e8856`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dda603cdd01780ad677c4f16ef238ba487aa146cd3f5d06542f066c10b93575`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.11.66-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:557ba9743467f6d9ecfb1670d9fb813858720e1ed9612956f837ce4eb5cf0dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30079417e65d20ad6f0ad236690d7babc98d5d1128642255422497d2ca46316f`

```dockerfile
```

-	Layers:
	-	`sha256:cdecb34f64c1ba351dec1bcc4a2182fa4b916423bfa5f3853e9f82069f25386a`  
		Last Modified: Thu, 30 Oct 2025 21:49:42 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.9`

```console
$ docker pull clickhouse@sha256:31de21589d0d2a7641492d645b53535efc35751fd36ca43929031cd012293af5
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
$ docker pull clickhouse@sha256:4c561844d47154da2cf18bf6fc308a9c1470ebd0b1557577abda7d8663dbd839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214126824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99fd8eaba170a8cabde920b8dff74572a18fef475f1da56cf9c2855f6e4dbaf7`
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
# Thu, 30 Oct 2025 21:20:39 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 21:20:39 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 21:20:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 21:20:39 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 21:20:39 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 21:20:39 GMT
ARG VERSION=25.9.5.21
# Thu, 30 Oct 2025 21:20:39 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 21:21:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:21:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:21:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 21:21:07 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 21:21:07 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 21:21:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 21:21:07 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 21:21:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 21:21:08 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 21:21:08 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 21:21:08 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 21:21:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f2b54dec56f899e3541e6378d03e8cd182afe4eb4890b954deb8802842f910`  
		Last Modified: Thu, 30 Oct 2025 21:21:52 GMT  
		Size: 7.6 MB (7576733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb3ffe7f678bcd6c880170754623c76b9248b55906cf055baf12b61fd5eef4ed`  
		Last Modified: Thu, 30 Oct 2025 21:50:23 GMT  
		Size: 178.3 MB (178296962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd97dc583a1c5bacf4be0631e5360f470d7b445747bdf2c1e39ab7c59092afb7`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75ac0b36c361fd8685c0f0c00ac426d3f75d0735f1fd9f3c71b4738dbf41f8d`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b892c789c4c82a60a77df538ce28170f3c71c1c7381ab0c590c490d13f6fef7`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6da2b828b97d18e73c18a5c0b0811f1e365e04a58484841e5d282a130d9f34`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9dec9f0e0da6fcc5341e51c7153a7fb55efedbb4ee320a25539daf55c8e011`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9` - unknown; unknown

```console
$ docker pull clickhouse@sha256:312f09886ff78060a641456578037587fbae0fae26fb8970a86de595d351c709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a11d90d516ff1db5e847298e0bfda6cfe9477e57b25a8aaa5279ad2323fec60`

```dockerfile
```

-	Layers:
	-	`sha256:7c0633f1e88444ed45b99f3525f54cbe9baf7c926eb1cf5c8f5abfc8e32886a2`  
		Last Modified: Thu, 30 Oct 2025 21:49:57 GMT  
		Size: 26.2 KB (26240 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.9-jammy`

```console
$ docker pull clickhouse@sha256:31de21589d0d2a7641492d645b53535efc35751fd36ca43929031cd012293af5
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
$ docker pull clickhouse@sha256:4c561844d47154da2cf18bf6fc308a9c1470ebd0b1557577abda7d8663dbd839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214126824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99fd8eaba170a8cabde920b8dff74572a18fef475f1da56cf9c2855f6e4dbaf7`
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
# Thu, 30 Oct 2025 21:20:39 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 21:20:39 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 21:20:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 21:20:39 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 21:20:39 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 21:20:39 GMT
ARG VERSION=25.9.5.21
# Thu, 30 Oct 2025 21:20:39 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 21:21:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:21:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:21:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 21:21:07 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 21:21:07 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 21:21:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 21:21:07 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 21:21:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 21:21:08 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 21:21:08 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 21:21:08 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 21:21:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f2b54dec56f899e3541e6378d03e8cd182afe4eb4890b954deb8802842f910`  
		Last Modified: Thu, 30 Oct 2025 21:21:52 GMT  
		Size: 7.6 MB (7576733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb3ffe7f678bcd6c880170754623c76b9248b55906cf055baf12b61fd5eef4ed`  
		Last Modified: Thu, 30 Oct 2025 21:50:23 GMT  
		Size: 178.3 MB (178296962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd97dc583a1c5bacf4be0631e5360f470d7b445747bdf2c1e39ab7c59092afb7`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75ac0b36c361fd8685c0f0c00ac426d3f75d0735f1fd9f3c71b4738dbf41f8d`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b892c789c4c82a60a77df538ce28170f3c71c1c7381ab0c590c490d13f6fef7`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6da2b828b97d18e73c18a5c0b0811f1e365e04a58484841e5d282a130d9f34`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9dec9f0e0da6fcc5341e51c7153a7fb55efedbb4ee320a25539daf55c8e011`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:312f09886ff78060a641456578037587fbae0fae26fb8970a86de595d351c709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a11d90d516ff1db5e847298e0bfda6cfe9477e57b25a8aaa5279ad2323fec60`

```dockerfile
```

-	Layers:
	-	`sha256:7c0633f1e88444ed45b99f3525f54cbe9baf7c926eb1cf5c8f5abfc8e32886a2`  
		Last Modified: Thu, 30 Oct 2025 21:49:57 GMT  
		Size: 26.2 KB (26240 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.9.5`

```console
$ docker pull clickhouse@sha256:b280ec59f7f45e7fe849ae37ea577658775e7d356ce52d68d65d5daf8e3de1e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.9.5` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4c561844d47154da2cf18bf6fc308a9c1470ebd0b1557577abda7d8663dbd839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214126824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99fd8eaba170a8cabde920b8dff74572a18fef475f1da56cf9c2855f6e4dbaf7`
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
# Thu, 30 Oct 2025 21:20:39 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 21:20:39 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 21:20:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 21:20:39 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 21:20:39 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 21:20:39 GMT
ARG VERSION=25.9.5.21
# Thu, 30 Oct 2025 21:20:39 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 21:21:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:21:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:21:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 21:21:07 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 21:21:07 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 21:21:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 21:21:07 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 21:21:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 21:21:08 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 21:21:08 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 21:21:08 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 21:21:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f2b54dec56f899e3541e6378d03e8cd182afe4eb4890b954deb8802842f910`  
		Last Modified: Thu, 30 Oct 2025 21:21:52 GMT  
		Size: 7.6 MB (7576733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb3ffe7f678bcd6c880170754623c76b9248b55906cf055baf12b61fd5eef4ed`  
		Last Modified: Thu, 30 Oct 2025 21:50:23 GMT  
		Size: 178.3 MB (178296962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd97dc583a1c5bacf4be0631e5360f470d7b445747bdf2c1e39ab7c59092afb7`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75ac0b36c361fd8685c0f0c00ac426d3f75d0735f1fd9f3c71b4738dbf41f8d`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b892c789c4c82a60a77df538ce28170f3c71c1c7381ab0c590c490d13f6fef7`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6da2b828b97d18e73c18a5c0b0811f1e365e04a58484841e5d282a130d9f34`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9dec9f0e0da6fcc5341e51c7153a7fb55efedbb4ee320a25539daf55c8e011`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9.5` - unknown; unknown

```console
$ docker pull clickhouse@sha256:312f09886ff78060a641456578037587fbae0fae26fb8970a86de595d351c709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a11d90d516ff1db5e847298e0bfda6cfe9477e57b25a8aaa5279ad2323fec60`

```dockerfile
```

-	Layers:
	-	`sha256:7c0633f1e88444ed45b99f3525f54cbe9baf7c926eb1cf5c8f5abfc8e32886a2`  
		Last Modified: Thu, 30 Oct 2025 21:49:57 GMT  
		Size: 26.2 KB (26240 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.9.5-jammy`

```console
$ docker pull clickhouse@sha256:b280ec59f7f45e7fe849ae37ea577658775e7d356ce52d68d65d5daf8e3de1e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.9.5-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4c561844d47154da2cf18bf6fc308a9c1470ebd0b1557577abda7d8663dbd839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214126824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99fd8eaba170a8cabde920b8dff74572a18fef475f1da56cf9c2855f6e4dbaf7`
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
# Thu, 30 Oct 2025 21:20:39 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 21:20:39 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 21:20:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 21:20:39 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 21:20:39 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 21:20:39 GMT
ARG VERSION=25.9.5.21
# Thu, 30 Oct 2025 21:20:39 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 21:21:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:21:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:21:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 21:21:07 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 21:21:07 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 21:21:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 21:21:07 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 21:21:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 21:21:08 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 21:21:08 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 21:21:08 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 21:21:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f2b54dec56f899e3541e6378d03e8cd182afe4eb4890b954deb8802842f910`  
		Last Modified: Thu, 30 Oct 2025 21:21:52 GMT  
		Size: 7.6 MB (7576733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb3ffe7f678bcd6c880170754623c76b9248b55906cf055baf12b61fd5eef4ed`  
		Last Modified: Thu, 30 Oct 2025 21:50:23 GMT  
		Size: 178.3 MB (178296962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd97dc583a1c5bacf4be0631e5360f470d7b445747bdf2c1e39ab7c59092afb7`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75ac0b36c361fd8685c0f0c00ac426d3f75d0735f1fd9f3c71b4738dbf41f8d`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b892c789c4c82a60a77df538ce28170f3c71c1c7381ab0c590c490d13f6fef7`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6da2b828b97d18e73c18a5c0b0811f1e365e04a58484841e5d282a130d9f34`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9dec9f0e0da6fcc5341e51c7153a7fb55efedbb4ee320a25539daf55c8e011`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9.5-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:312f09886ff78060a641456578037587fbae0fae26fb8970a86de595d351c709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a11d90d516ff1db5e847298e0bfda6cfe9477e57b25a8aaa5279ad2323fec60`

```dockerfile
```

-	Layers:
	-	`sha256:7c0633f1e88444ed45b99f3525f54cbe9baf7c926eb1cf5c8f5abfc8e32886a2`  
		Last Modified: Thu, 30 Oct 2025 21:49:57 GMT  
		Size: 26.2 KB (26240 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.9.5.21`

```console
$ docker pull clickhouse@sha256:b280ec59f7f45e7fe849ae37ea577658775e7d356ce52d68d65d5daf8e3de1e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.9.5.21` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4c561844d47154da2cf18bf6fc308a9c1470ebd0b1557577abda7d8663dbd839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214126824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99fd8eaba170a8cabde920b8dff74572a18fef475f1da56cf9c2855f6e4dbaf7`
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
# Thu, 30 Oct 2025 21:20:39 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 21:20:39 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 21:20:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 21:20:39 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 21:20:39 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 21:20:39 GMT
ARG VERSION=25.9.5.21
# Thu, 30 Oct 2025 21:20:39 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 21:21:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:21:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:21:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 21:21:07 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 21:21:07 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 21:21:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 21:21:07 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 21:21:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 21:21:08 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 21:21:08 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 21:21:08 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 21:21:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f2b54dec56f899e3541e6378d03e8cd182afe4eb4890b954deb8802842f910`  
		Last Modified: Thu, 30 Oct 2025 21:21:52 GMT  
		Size: 7.6 MB (7576733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb3ffe7f678bcd6c880170754623c76b9248b55906cf055baf12b61fd5eef4ed`  
		Last Modified: Thu, 30 Oct 2025 21:50:23 GMT  
		Size: 178.3 MB (178296962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd97dc583a1c5bacf4be0631e5360f470d7b445747bdf2c1e39ab7c59092afb7`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75ac0b36c361fd8685c0f0c00ac426d3f75d0735f1fd9f3c71b4738dbf41f8d`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b892c789c4c82a60a77df538ce28170f3c71c1c7381ab0c590c490d13f6fef7`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6da2b828b97d18e73c18a5c0b0811f1e365e04a58484841e5d282a130d9f34`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9dec9f0e0da6fcc5341e51c7153a7fb55efedbb4ee320a25539daf55c8e011`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9.5.21` - unknown; unknown

```console
$ docker pull clickhouse@sha256:312f09886ff78060a641456578037587fbae0fae26fb8970a86de595d351c709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a11d90d516ff1db5e847298e0bfda6cfe9477e57b25a8aaa5279ad2323fec60`

```dockerfile
```

-	Layers:
	-	`sha256:7c0633f1e88444ed45b99f3525f54cbe9baf7c926eb1cf5c8f5abfc8e32886a2`  
		Last Modified: Thu, 30 Oct 2025 21:49:57 GMT  
		Size: 26.2 KB (26240 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.9.5.21-jammy`

```console
$ docker pull clickhouse@sha256:b280ec59f7f45e7fe849ae37ea577658775e7d356ce52d68d65d5daf8e3de1e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.9.5.21-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4c561844d47154da2cf18bf6fc308a9c1470ebd0b1557577abda7d8663dbd839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214126824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99fd8eaba170a8cabde920b8dff74572a18fef475f1da56cf9c2855f6e4dbaf7`
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
# Thu, 30 Oct 2025 21:20:39 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 21:20:39 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 21:20:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 21:20:39 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 21:20:39 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 21:20:39 GMT
ARG VERSION=25.9.5.21
# Thu, 30 Oct 2025 21:20:39 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 21:21:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:21:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:21:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 21:21:07 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 21:21:07 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 21:21:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 21:21:07 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 21:21:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 21:21:08 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 21:21:08 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 21:21:08 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 21:21:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f2b54dec56f899e3541e6378d03e8cd182afe4eb4890b954deb8802842f910`  
		Last Modified: Thu, 30 Oct 2025 21:21:52 GMT  
		Size: 7.6 MB (7576733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb3ffe7f678bcd6c880170754623c76b9248b55906cf055baf12b61fd5eef4ed`  
		Last Modified: Thu, 30 Oct 2025 21:50:23 GMT  
		Size: 178.3 MB (178296962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd97dc583a1c5bacf4be0631e5360f470d7b445747bdf2c1e39ab7c59092afb7`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75ac0b36c361fd8685c0f0c00ac426d3f75d0735f1fd9f3c71b4738dbf41f8d`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b892c789c4c82a60a77df538ce28170f3c71c1c7381ab0c590c490d13f6fef7`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6da2b828b97d18e73c18a5c0b0811f1e365e04a58484841e5d282a130d9f34`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9dec9f0e0da6fcc5341e51c7153a7fb55efedbb4ee320a25539daf55c8e011`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9.5.21-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:312f09886ff78060a641456578037587fbae0fae26fb8970a86de595d351c709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a11d90d516ff1db5e847298e0bfda6cfe9477e57b25a8aaa5279ad2323fec60`

```dockerfile
```

-	Layers:
	-	`sha256:7c0633f1e88444ed45b99f3525f54cbe9baf7c926eb1cf5c8f5abfc8e32886a2`  
		Last Modified: Thu, 30 Oct 2025 21:49:57 GMT  
		Size: 26.2 KB (26240 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:jammy`

```console
$ docker pull clickhouse@sha256:31de21589d0d2a7641492d645b53535efc35751fd36ca43929031cd012293af5
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
$ docker pull clickhouse@sha256:4c561844d47154da2cf18bf6fc308a9c1470ebd0b1557577abda7d8663dbd839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214126824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99fd8eaba170a8cabde920b8dff74572a18fef475f1da56cf9c2855f6e4dbaf7`
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
# Thu, 30 Oct 2025 21:20:39 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 21:20:39 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 21:20:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 21:20:39 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 21:20:39 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 21:20:39 GMT
ARG VERSION=25.9.5.21
# Thu, 30 Oct 2025 21:20:39 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 21:21:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:21:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:21:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 21:21:07 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 21:21:07 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 21:21:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 21:21:07 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 21:21:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 21:21:08 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 21:21:08 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 21:21:08 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 21:21:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f2b54dec56f899e3541e6378d03e8cd182afe4eb4890b954deb8802842f910`  
		Last Modified: Thu, 30 Oct 2025 21:21:52 GMT  
		Size: 7.6 MB (7576733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb3ffe7f678bcd6c880170754623c76b9248b55906cf055baf12b61fd5eef4ed`  
		Last Modified: Thu, 30 Oct 2025 21:50:23 GMT  
		Size: 178.3 MB (178296962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd97dc583a1c5bacf4be0631e5360f470d7b445747bdf2c1e39ab7c59092afb7`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75ac0b36c361fd8685c0f0c00ac426d3f75d0735f1fd9f3c71b4738dbf41f8d`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b892c789c4c82a60a77df538ce28170f3c71c1c7381ab0c590c490d13f6fef7`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6da2b828b97d18e73c18a5c0b0811f1e365e04a58484841e5d282a130d9f34`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9dec9f0e0da6fcc5341e51c7153a7fb55efedbb4ee320a25539daf55c8e011`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:312f09886ff78060a641456578037587fbae0fae26fb8970a86de595d351c709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a11d90d516ff1db5e847298e0bfda6cfe9477e57b25a8aaa5279ad2323fec60`

```dockerfile
```

-	Layers:
	-	`sha256:7c0633f1e88444ed45b99f3525f54cbe9baf7c926eb1cf5c8f5abfc8e32886a2`  
		Last Modified: Thu, 30 Oct 2025 21:49:57 GMT  
		Size: 26.2 KB (26240 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:31de21589d0d2a7641492d645b53535efc35751fd36ca43929031cd012293af5
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
$ docker pull clickhouse@sha256:4c561844d47154da2cf18bf6fc308a9c1470ebd0b1557577abda7d8663dbd839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214126824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99fd8eaba170a8cabde920b8dff74572a18fef475f1da56cf9c2855f6e4dbaf7`
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
# Thu, 30 Oct 2025 21:20:39 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 21:20:39 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 21:20:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 21:20:39 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 21:20:39 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 21:20:39 GMT
ARG VERSION=25.9.5.21
# Thu, 30 Oct 2025 21:20:39 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 21:21:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:21:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:21:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 21:21:07 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 21:21:07 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 21:21:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 21:21:07 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 21:21:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 21:21:08 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 21:21:08 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 21:21:08 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 21:21:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f2b54dec56f899e3541e6378d03e8cd182afe4eb4890b954deb8802842f910`  
		Last Modified: Thu, 30 Oct 2025 21:21:52 GMT  
		Size: 7.6 MB (7576733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb3ffe7f678bcd6c880170754623c76b9248b55906cf055baf12b61fd5eef4ed`  
		Last Modified: Thu, 30 Oct 2025 21:50:23 GMT  
		Size: 178.3 MB (178296962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd97dc583a1c5bacf4be0631e5360f470d7b445747bdf2c1e39ab7c59092afb7`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75ac0b36c361fd8685c0f0c00ac426d3f75d0735f1fd9f3c71b4738dbf41f8d`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b892c789c4c82a60a77df538ce28170f3c71c1c7381ab0c590c490d13f6fef7`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6da2b828b97d18e73c18a5c0b0811f1e365e04a58484841e5d282a130d9f34`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9dec9f0e0da6fcc5341e51c7153a7fb55efedbb4ee320a25539daf55c8e011`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:312f09886ff78060a641456578037587fbae0fae26fb8970a86de595d351c709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a11d90d516ff1db5e847298e0bfda6cfe9477e57b25a8aaa5279ad2323fec60`

```dockerfile
```

-	Layers:
	-	`sha256:7c0633f1e88444ed45b99f3525f54cbe9baf7c926eb1cf5c8f5abfc8e32886a2`  
		Last Modified: Thu, 30 Oct 2025 21:49:57 GMT  
		Size: 26.2 KB (26240 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts`

```console
$ docker pull clickhouse@sha256:e4177e94d974c4d344d85c6ca7c4707f3dd3f1a72f5a446ff505fc4d76179381
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
$ docker pull clickhouse@sha256:a5656778631ee59482d9821f008c2f43704a533bb78ce9fabe3f9e735055b882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.6 MB (212645310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636cee591520bd679efa5bdfc5ccbbe8955c161e8ce6052107b9f0192bb2d962`
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
# Thu, 30 Oct 2025 21:21:43 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 21:21:43 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 21:21:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 21:21:43 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 21:21:43 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 21:21:43 GMT
ARG VERSION=25.8.11.66
# Thu, 30 Oct 2025 21:21:43 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 21:22:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 21:22:12 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 21:22:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 21:22:12 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 21:22:12 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 21:22:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce7ce10c9eeca1dd1885578ad8f3f6291f3732bdf5a50a8a6535af67a72e81f`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 7.6 MB (7576689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee964fa2145e136ca73e4c3796c405f427a709e6070f3f4802f8e19f6723677`  
		Last Modified: Thu, 30 Oct 2025 21:50:09 GMT  
		Size: 176.8 MB (176815492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd59e47ba03552bfa2a66ef28e55b44868ad4666ae67b5fe3e408e5c5a79ca85`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9616189aee41fb2150e3b2e7df745964d4e966fb63f6a7a431d6d848dfc358`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e163c00ab90daa2465b1046a4d0b95388778dc70b143011610dca4fb7590de31`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47157a68ab31f8dfb08a2352278276b514a9773b046ac4dca1504822e01e8856`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dda603cdd01780ad677c4f16ef238ba487aa146cd3f5d06542f066c10b93575`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:557ba9743467f6d9ecfb1670d9fb813858720e1ed9612956f837ce4eb5cf0dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30079417e65d20ad6f0ad236690d7babc98d5d1128642255422497d2ca46316f`

```dockerfile
```

-	Layers:
	-	`sha256:cdecb34f64c1ba351dec1bcc4a2182fa4b916423bfa5f3853e9f82069f25386a`  
		Last Modified: Thu, 30 Oct 2025 21:49:42 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts-jammy`

```console
$ docker pull clickhouse@sha256:e4177e94d974c4d344d85c6ca7c4707f3dd3f1a72f5a446ff505fc4d76179381
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
$ docker pull clickhouse@sha256:a5656778631ee59482d9821f008c2f43704a533bb78ce9fabe3f9e735055b882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.6 MB (212645310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636cee591520bd679efa5bdfc5ccbbe8955c161e8ce6052107b9f0192bb2d962`
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
# Thu, 30 Oct 2025 21:21:43 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 21:21:43 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 21:21:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 21:21:43 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 21:21:43 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 21:21:43 GMT
ARG VERSION=25.8.11.66
# Thu, 30 Oct 2025 21:21:43 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 21:22:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 21:22:12 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 21:22:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 21:22:12 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 21:22:12 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 21:22:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce7ce10c9eeca1dd1885578ad8f3f6291f3732bdf5a50a8a6535af67a72e81f`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 7.6 MB (7576689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee964fa2145e136ca73e4c3796c405f427a709e6070f3f4802f8e19f6723677`  
		Last Modified: Thu, 30 Oct 2025 21:50:09 GMT  
		Size: 176.8 MB (176815492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd59e47ba03552bfa2a66ef28e55b44868ad4666ae67b5fe3e408e5c5a79ca85`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9616189aee41fb2150e3b2e7df745964d4e966fb63f6a7a431d6d848dfc358`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e163c00ab90daa2465b1046a4d0b95388778dc70b143011610dca4fb7590de31`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47157a68ab31f8dfb08a2352278276b514a9773b046ac4dca1504822e01e8856`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dda603cdd01780ad677c4f16ef238ba487aa146cd3f5d06542f066c10b93575`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:557ba9743467f6d9ecfb1670d9fb813858720e1ed9612956f837ce4eb5cf0dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30079417e65d20ad6f0ad236690d7babc98d5d1128642255422497d2ca46316f`

```dockerfile
```

-	Layers:
	-	`sha256:cdecb34f64c1ba351dec1bcc4a2182fa4b916423bfa5f3853e9f82069f25386a`  
		Last Modified: Thu, 30 Oct 2025 21:49:42 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json
