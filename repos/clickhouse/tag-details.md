<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clickhouse`

-	[`clickhouse:25.3`](#clickhouse253)
-	[`clickhouse:25.3-jammy`](#clickhouse253-jammy)
-	[`clickhouse:25.3.6`](#clickhouse2536)
-	[`clickhouse:25.3.6-jammy`](#clickhouse2536-jammy)
-	[`clickhouse:25.3.6.56`](#clickhouse253656)
-	[`clickhouse:25.3.6.56-jammy`](#clickhouse253656-jammy)
-	[`clickhouse:25.5`](#clickhouse255)
-	[`clickhouse:25.5-jammy`](#clickhouse255-jammy)
-	[`clickhouse:25.5.9`](#clickhouse2559)
-	[`clickhouse:25.5.9-jammy`](#clickhouse2559-jammy)
-	[`clickhouse:25.5.9.14`](#clickhouse255914)
-	[`clickhouse:25.5.9.14-jammy`](#clickhouse255914-jammy)
-	[`clickhouse:25.6`](#clickhouse256)
-	[`clickhouse:25.6-jammy`](#clickhouse256-jammy)
-	[`clickhouse:25.6.8`](#clickhouse2568)
-	[`clickhouse:25.6.8-jammy`](#clickhouse2568-jammy)
-	[`clickhouse:25.6.8.10`](#clickhouse256810)
-	[`clickhouse:25.6.8.10-jammy`](#clickhouse256810-jammy)
-	[`clickhouse:25.7`](#clickhouse257)
-	[`clickhouse:25.7-jammy`](#clickhouse257-jammy)
-	[`clickhouse:25.7.4`](#clickhouse2574)
-	[`clickhouse:25.7.4-jammy`](#clickhouse2574-jammy)
-	[`clickhouse:25.7.4.11`](#clickhouse257411)
-	[`clickhouse:25.7.4.11-jammy`](#clickhouse257411-jammy)
-	[`clickhouse:jammy`](#clickhousejammy)
-	[`clickhouse:latest`](#clickhouselatest)
-	[`clickhouse:lts`](#clickhouselts)
-	[`clickhouse:lts-jammy`](#clickhouselts-jammy)

## `clickhouse:25.3`

```console
$ docker pull clickhouse@sha256:b2026b4defbdd247c6978d9f77c887340b2aa5d036a4856089ddaa49f95d5e28
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:636ce3aa345c93482ba2f51d9737721e89a96f44ff0fd913ff400b18d50bd125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.4 MB (205432539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0861ca60e97c4a4911b5ab03e22d521e79beaf99aeba2542fca8a4ae16f5fab7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:32:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:32:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:32:14 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 30 Jul 2025 05:32:14 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:05:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 07 Aug 2025 16:05:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPO_CHANNEL=stable
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 07 Aug 2025 16:05:41 GMT
ARG VERSION=25.3.6.56
# Thu, 07 Aug 2025 16:05:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 16:05:41 GMT
ENV TZ=UTC
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 07 Aug 2025 16:05:41 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 07 Aug 2025 16:05:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 07 Aug 2025 16:05:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137c85da229929a08f72e0cfa17aaec9403f65a3da5881d8597fbcc91cbdd1f2`  
		Last Modified: Tue, 12 Aug 2025 17:24:15 GMT  
		Size: 7.2 MB (7151687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f0f4d76285565776b73c89d420a55567190d02146e95bb55b2a043b6113a8e`  
		Last Modified: Tue, 12 Aug 2025 18:49:54 GMT  
		Size: 167.9 MB (167873615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ef3061e624958aab31c4e5978a0f61eeda5c05c194bd11c4b704d446fa1097`  
		Last Modified: Tue, 12 Aug 2025 17:24:11 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1b24d7e886d2fbd34ded6bb6650b314782d91b5b74b7b208959f51a09b95b1`  
		Last Modified: Tue, 12 Aug 2025 17:24:12 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384bebcfcced27c8cc253e9a927dadea48eccc047b126656c50f40eb610959c6`  
		Last Modified: Tue, 12 Aug 2025 17:24:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55573752dbede5172c8eedea40d806a0622935e82410289e57b4b9394f4f147`  
		Last Modified: Tue, 12 Aug 2025 17:24:12 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb76cd2113121f91e3ab02f114cf6252db5f9292d55c9407f5cc537cf6ba237`  
		Last Modified: Tue, 12 Aug 2025 17:24:13 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:82eb1fb6bde6c4de016b438a56cb7bd716aaa4629cb957b74e3c93cfe06eb9e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4596f7361fd8a3e99e4345bb0763c6f63d502e4254aaa3c4fe5706b3c9f27f25`

```dockerfile
```

-	Layers:
	-	`sha256:4fad8a220e2457601f329591a0485ba91179ff6374b02e0696775d095f5c25f2`  
		Last Modified: Tue, 12 Aug 2025 18:49:21 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:cf502240469bccc854c9b3fc67e5ca54ec37a3f5ef6df20056f0f8323d42b3db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192912365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7be4817e5d79d7aedd4983a60758916bd520dd58e258225fb62ec07bc1bed9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:14 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:17 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 30 Jul 2025 05:34:17 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:05:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 07 Aug 2025 16:05:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPO_CHANNEL=stable
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 07 Aug 2025 16:05:41 GMT
ARG VERSION=25.3.6.56
# Thu, 07 Aug 2025 16:05:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 16:05:41 GMT
ENV TZ=UTC
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 07 Aug 2025 16:05:41 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 07 Aug 2025 16:05:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 07 Aug 2025 16:05:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e6e0b617b9c63d680a3dee014408e3c901d247257c08f588eb01fd8ab0b0cf`  
		Last Modified: Tue, 12 Aug 2025 17:35:42 GMT  
		Size: 7.1 MB (7127960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa41208f438b689eaf456b07fbfecabf48676b2b7cef271faca1a76e41f0a463`  
		Last Modified: Tue, 12 Aug 2025 18:49:50 GMT  
		Size: 157.6 MB (157554909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa40645d38b2be7a1826a8c5ce4f1672e59b4119987c880641938a181bd9ed83`  
		Last Modified: Tue, 12 Aug 2025 17:35:41 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7826c6a09a2f6eec6e397f6a19aad16112f8387aa6f876f40771f63b54fb2fa`  
		Last Modified: Tue, 12 Aug 2025 17:35:42 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a378edc92a579bbd440d0c7e6b2aa53b121a721e0da76a3d251ba47ad3dd4aa`  
		Last Modified: Tue, 12 Aug 2025 17:35:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9dd5e8c5fe95a063fd9c0b05940f9c20ad696c10e01033a27283229ecc5780`  
		Last Modified: Tue, 12 Aug 2025 17:35:41 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbf8d069153cecb84f87a8a394bf119304fb4b4e8fda23b32c4d191b44c8b55`  
		Last Modified: Tue, 12 Aug 2025 17:35:42 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a71c6061a09f252dac7c36c94adc81c75a467329095ed90329b2bcddadb37a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f25d0f988a9bcd5c1eff72678102496338ffcec6798ffacadbc579eac789164a`

```dockerfile
```

-	Layers:
	-	`sha256:4586c050a3d62b4912f0aff1149618f3e8e444bbc8955c0a08f13d942d02f7d7`  
		Last Modified: Tue, 12 Aug 2025 18:49:25 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3-jammy`

```console
$ docker pull clickhouse@sha256:b2026b4defbdd247c6978d9f77c887340b2aa5d036a4856089ddaa49f95d5e28
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:636ce3aa345c93482ba2f51d9737721e89a96f44ff0fd913ff400b18d50bd125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.4 MB (205432539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0861ca60e97c4a4911b5ab03e22d521e79beaf99aeba2542fca8a4ae16f5fab7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:32:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:32:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:32:14 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 30 Jul 2025 05:32:14 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:05:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 07 Aug 2025 16:05:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPO_CHANNEL=stable
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 07 Aug 2025 16:05:41 GMT
ARG VERSION=25.3.6.56
# Thu, 07 Aug 2025 16:05:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 16:05:41 GMT
ENV TZ=UTC
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 07 Aug 2025 16:05:41 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 07 Aug 2025 16:05:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 07 Aug 2025 16:05:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137c85da229929a08f72e0cfa17aaec9403f65a3da5881d8597fbcc91cbdd1f2`  
		Last Modified: Tue, 12 Aug 2025 17:24:15 GMT  
		Size: 7.2 MB (7151687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f0f4d76285565776b73c89d420a55567190d02146e95bb55b2a043b6113a8e`  
		Last Modified: Tue, 12 Aug 2025 18:49:54 GMT  
		Size: 167.9 MB (167873615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ef3061e624958aab31c4e5978a0f61eeda5c05c194bd11c4b704d446fa1097`  
		Last Modified: Tue, 12 Aug 2025 17:24:11 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1b24d7e886d2fbd34ded6bb6650b314782d91b5b74b7b208959f51a09b95b1`  
		Last Modified: Tue, 12 Aug 2025 17:24:12 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384bebcfcced27c8cc253e9a927dadea48eccc047b126656c50f40eb610959c6`  
		Last Modified: Tue, 12 Aug 2025 17:24:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55573752dbede5172c8eedea40d806a0622935e82410289e57b4b9394f4f147`  
		Last Modified: Tue, 12 Aug 2025 17:24:12 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb76cd2113121f91e3ab02f114cf6252db5f9292d55c9407f5cc537cf6ba237`  
		Last Modified: Tue, 12 Aug 2025 17:24:13 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:82eb1fb6bde6c4de016b438a56cb7bd716aaa4629cb957b74e3c93cfe06eb9e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4596f7361fd8a3e99e4345bb0763c6f63d502e4254aaa3c4fe5706b3c9f27f25`

```dockerfile
```

-	Layers:
	-	`sha256:4fad8a220e2457601f329591a0485ba91179ff6374b02e0696775d095f5c25f2`  
		Last Modified: Tue, 12 Aug 2025 18:49:21 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:cf502240469bccc854c9b3fc67e5ca54ec37a3f5ef6df20056f0f8323d42b3db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192912365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7be4817e5d79d7aedd4983a60758916bd520dd58e258225fb62ec07bc1bed9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:14 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:17 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 30 Jul 2025 05:34:17 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:05:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 07 Aug 2025 16:05:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPO_CHANNEL=stable
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 07 Aug 2025 16:05:41 GMT
ARG VERSION=25.3.6.56
# Thu, 07 Aug 2025 16:05:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 16:05:41 GMT
ENV TZ=UTC
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 07 Aug 2025 16:05:41 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 07 Aug 2025 16:05:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 07 Aug 2025 16:05:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e6e0b617b9c63d680a3dee014408e3c901d247257c08f588eb01fd8ab0b0cf`  
		Last Modified: Tue, 12 Aug 2025 17:35:42 GMT  
		Size: 7.1 MB (7127960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa41208f438b689eaf456b07fbfecabf48676b2b7cef271faca1a76e41f0a463`  
		Last Modified: Tue, 12 Aug 2025 18:49:50 GMT  
		Size: 157.6 MB (157554909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa40645d38b2be7a1826a8c5ce4f1672e59b4119987c880641938a181bd9ed83`  
		Last Modified: Tue, 12 Aug 2025 17:35:41 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7826c6a09a2f6eec6e397f6a19aad16112f8387aa6f876f40771f63b54fb2fa`  
		Last Modified: Tue, 12 Aug 2025 17:35:42 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a378edc92a579bbd440d0c7e6b2aa53b121a721e0da76a3d251ba47ad3dd4aa`  
		Last Modified: Tue, 12 Aug 2025 17:35:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9dd5e8c5fe95a063fd9c0b05940f9c20ad696c10e01033a27283229ecc5780`  
		Last Modified: Tue, 12 Aug 2025 17:35:41 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbf8d069153cecb84f87a8a394bf119304fb4b4e8fda23b32c4d191b44c8b55`  
		Last Modified: Tue, 12 Aug 2025 17:35:42 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a71c6061a09f252dac7c36c94adc81c75a467329095ed90329b2bcddadb37a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f25d0f988a9bcd5c1eff72678102496338ffcec6798ffacadbc579eac789164a`

```dockerfile
```

-	Layers:
	-	`sha256:4586c050a3d62b4912f0aff1149618f3e8e444bbc8955c0a08f13d942d02f7d7`  
		Last Modified: Tue, 12 Aug 2025 18:49:25 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.6`

```console
$ docker pull clickhouse@sha256:b2026b4defbdd247c6978d9f77c887340b2aa5d036a4856089ddaa49f95d5e28
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.6` - linux; amd64

```console
$ docker pull clickhouse@sha256:636ce3aa345c93482ba2f51d9737721e89a96f44ff0fd913ff400b18d50bd125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.4 MB (205432539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0861ca60e97c4a4911b5ab03e22d521e79beaf99aeba2542fca8a4ae16f5fab7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:32:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:32:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:32:14 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 30 Jul 2025 05:32:14 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:05:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 07 Aug 2025 16:05:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPO_CHANNEL=stable
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 07 Aug 2025 16:05:41 GMT
ARG VERSION=25.3.6.56
# Thu, 07 Aug 2025 16:05:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 16:05:41 GMT
ENV TZ=UTC
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 07 Aug 2025 16:05:41 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 07 Aug 2025 16:05:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 07 Aug 2025 16:05:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137c85da229929a08f72e0cfa17aaec9403f65a3da5881d8597fbcc91cbdd1f2`  
		Last Modified: Tue, 12 Aug 2025 17:24:15 GMT  
		Size: 7.2 MB (7151687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f0f4d76285565776b73c89d420a55567190d02146e95bb55b2a043b6113a8e`  
		Last Modified: Tue, 12 Aug 2025 18:49:54 GMT  
		Size: 167.9 MB (167873615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ef3061e624958aab31c4e5978a0f61eeda5c05c194bd11c4b704d446fa1097`  
		Last Modified: Tue, 12 Aug 2025 17:24:11 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1b24d7e886d2fbd34ded6bb6650b314782d91b5b74b7b208959f51a09b95b1`  
		Last Modified: Tue, 12 Aug 2025 17:24:12 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384bebcfcced27c8cc253e9a927dadea48eccc047b126656c50f40eb610959c6`  
		Last Modified: Tue, 12 Aug 2025 17:24:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55573752dbede5172c8eedea40d806a0622935e82410289e57b4b9394f4f147`  
		Last Modified: Tue, 12 Aug 2025 17:24:12 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb76cd2113121f91e3ab02f114cf6252db5f9292d55c9407f5cc537cf6ba237`  
		Last Modified: Tue, 12 Aug 2025 17:24:13 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.6` - unknown; unknown

```console
$ docker pull clickhouse@sha256:82eb1fb6bde6c4de016b438a56cb7bd716aaa4629cb957b74e3c93cfe06eb9e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4596f7361fd8a3e99e4345bb0763c6f63d502e4254aaa3c4fe5706b3c9f27f25`

```dockerfile
```

-	Layers:
	-	`sha256:4fad8a220e2457601f329591a0485ba91179ff6374b02e0696775d095f5c25f2`  
		Last Modified: Tue, 12 Aug 2025 18:49:21 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.6` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:cf502240469bccc854c9b3fc67e5ca54ec37a3f5ef6df20056f0f8323d42b3db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192912365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7be4817e5d79d7aedd4983a60758916bd520dd58e258225fb62ec07bc1bed9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:14 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:17 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 30 Jul 2025 05:34:17 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:05:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 07 Aug 2025 16:05:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPO_CHANNEL=stable
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 07 Aug 2025 16:05:41 GMT
ARG VERSION=25.3.6.56
# Thu, 07 Aug 2025 16:05:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 16:05:41 GMT
ENV TZ=UTC
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 07 Aug 2025 16:05:41 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 07 Aug 2025 16:05:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 07 Aug 2025 16:05:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e6e0b617b9c63d680a3dee014408e3c901d247257c08f588eb01fd8ab0b0cf`  
		Last Modified: Tue, 12 Aug 2025 17:35:42 GMT  
		Size: 7.1 MB (7127960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa41208f438b689eaf456b07fbfecabf48676b2b7cef271faca1a76e41f0a463`  
		Last Modified: Tue, 12 Aug 2025 18:49:50 GMT  
		Size: 157.6 MB (157554909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa40645d38b2be7a1826a8c5ce4f1672e59b4119987c880641938a181bd9ed83`  
		Last Modified: Tue, 12 Aug 2025 17:35:41 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7826c6a09a2f6eec6e397f6a19aad16112f8387aa6f876f40771f63b54fb2fa`  
		Last Modified: Tue, 12 Aug 2025 17:35:42 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a378edc92a579bbd440d0c7e6b2aa53b121a721e0da76a3d251ba47ad3dd4aa`  
		Last Modified: Tue, 12 Aug 2025 17:35:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9dd5e8c5fe95a063fd9c0b05940f9c20ad696c10e01033a27283229ecc5780`  
		Last Modified: Tue, 12 Aug 2025 17:35:41 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbf8d069153cecb84f87a8a394bf119304fb4b4e8fda23b32c4d191b44c8b55`  
		Last Modified: Tue, 12 Aug 2025 17:35:42 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.6` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a71c6061a09f252dac7c36c94adc81c75a467329095ed90329b2bcddadb37a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f25d0f988a9bcd5c1eff72678102496338ffcec6798ffacadbc579eac789164a`

```dockerfile
```

-	Layers:
	-	`sha256:4586c050a3d62b4912f0aff1149618f3e8e444bbc8955c0a08f13d942d02f7d7`  
		Last Modified: Tue, 12 Aug 2025 18:49:25 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.6-jammy`

```console
$ docker pull clickhouse@sha256:b2026b4defbdd247c6978d9f77c887340b2aa5d036a4856089ddaa49f95d5e28
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.6-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:636ce3aa345c93482ba2f51d9737721e89a96f44ff0fd913ff400b18d50bd125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.4 MB (205432539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0861ca60e97c4a4911b5ab03e22d521e79beaf99aeba2542fca8a4ae16f5fab7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:32:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:32:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:32:14 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 30 Jul 2025 05:32:14 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:05:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 07 Aug 2025 16:05:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPO_CHANNEL=stable
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 07 Aug 2025 16:05:41 GMT
ARG VERSION=25.3.6.56
# Thu, 07 Aug 2025 16:05:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 16:05:41 GMT
ENV TZ=UTC
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 07 Aug 2025 16:05:41 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 07 Aug 2025 16:05:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 07 Aug 2025 16:05:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137c85da229929a08f72e0cfa17aaec9403f65a3da5881d8597fbcc91cbdd1f2`  
		Last Modified: Tue, 12 Aug 2025 17:24:15 GMT  
		Size: 7.2 MB (7151687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f0f4d76285565776b73c89d420a55567190d02146e95bb55b2a043b6113a8e`  
		Last Modified: Tue, 12 Aug 2025 18:49:54 GMT  
		Size: 167.9 MB (167873615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ef3061e624958aab31c4e5978a0f61eeda5c05c194bd11c4b704d446fa1097`  
		Last Modified: Tue, 12 Aug 2025 17:24:11 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1b24d7e886d2fbd34ded6bb6650b314782d91b5b74b7b208959f51a09b95b1`  
		Last Modified: Tue, 12 Aug 2025 17:24:12 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384bebcfcced27c8cc253e9a927dadea48eccc047b126656c50f40eb610959c6`  
		Last Modified: Tue, 12 Aug 2025 17:24:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55573752dbede5172c8eedea40d806a0622935e82410289e57b4b9394f4f147`  
		Last Modified: Tue, 12 Aug 2025 17:24:12 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb76cd2113121f91e3ab02f114cf6252db5f9292d55c9407f5cc537cf6ba237`  
		Last Modified: Tue, 12 Aug 2025 17:24:13 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.6-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:82eb1fb6bde6c4de016b438a56cb7bd716aaa4629cb957b74e3c93cfe06eb9e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4596f7361fd8a3e99e4345bb0763c6f63d502e4254aaa3c4fe5706b3c9f27f25`

```dockerfile
```

-	Layers:
	-	`sha256:4fad8a220e2457601f329591a0485ba91179ff6374b02e0696775d095f5c25f2`  
		Last Modified: Tue, 12 Aug 2025 18:49:21 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.6-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:cf502240469bccc854c9b3fc67e5ca54ec37a3f5ef6df20056f0f8323d42b3db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192912365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7be4817e5d79d7aedd4983a60758916bd520dd58e258225fb62ec07bc1bed9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:14 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:17 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 30 Jul 2025 05:34:17 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:05:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 07 Aug 2025 16:05:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPO_CHANNEL=stable
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 07 Aug 2025 16:05:41 GMT
ARG VERSION=25.3.6.56
# Thu, 07 Aug 2025 16:05:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 16:05:41 GMT
ENV TZ=UTC
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 07 Aug 2025 16:05:41 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 07 Aug 2025 16:05:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 07 Aug 2025 16:05:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e6e0b617b9c63d680a3dee014408e3c901d247257c08f588eb01fd8ab0b0cf`  
		Last Modified: Tue, 12 Aug 2025 17:35:42 GMT  
		Size: 7.1 MB (7127960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa41208f438b689eaf456b07fbfecabf48676b2b7cef271faca1a76e41f0a463`  
		Last Modified: Tue, 12 Aug 2025 18:49:50 GMT  
		Size: 157.6 MB (157554909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa40645d38b2be7a1826a8c5ce4f1672e59b4119987c880641938a181bd9ed83`  
		Last Modified: Tue, 12 Aug 2025 17:35:41 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7826c6a09a2f6eec6e397f6a19aad16112f8387aa6f876f40771f63b54fb2fa`  
		Last Modified: Tue, 12 Aug 2025 17:35:42 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a378edc92a579bbd440d0c7e6b2aa53b121a721e0da76a3d251ba47ad3dd4aa`  
		Last Modified: Tue, 12 Aug 2025 17:35:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9dd5e8c5fe95a063fd9c0b05940f9c20ad696c10e01033a27283229ecc5780`  
		Last Modified: Tue, 12 Aug 2025 17:35:41 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbf8d069153cecb84f87a8a394bf119304fb4b4e8fda23b32c4d191b44c8b55`  
		Last Modified: Tue, 12 Aug 2025 17:35:42 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.6-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a71c6061a09f252dac7c36c94adc81c75a467329095ed90329b2bcddadb37a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f25d0f988a9bcd5c1eff72678102496338ffcec6798ffacadbc579eac789164a`

```dockerfile
```

-	Layers:
	-	`sha256:4586c050a3d62b4912f0aff1149618f3e8e444bbc8955c0a08f13d942d02f7d7`  
		Last Modified: Tue, 12 Aug 2025 18:49:25 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.6.56`

```console
$ docker pull clickhouse@sha256:b2026b4defbdd247c6978d9f77c887340b2aa5d036a4856089ddaa49f95d5e28
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.6.56` - linux; amd64

```console
$ docker pull clickhouse@sha256:636ce3aa345c93482ba2f51d9737721e89a96f44ff0fd913ff400b18d50bd125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.4 MB (205432539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0861ca60e97c4a4911b5ab03e22d521e79beaf99aeba2542fca8a4ae16f5fab7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:32:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:32:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:32:14 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 30 Jul 2025 05:32:14 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:05:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 07 Aug 2025 16:05:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPO_CHANNEL=stable
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 07 Aug 2025 16:05:41 GMT
ARG VERSION=25.3.6.56
# Thu, 07 Aug 2025 16:05:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 16:05:41 GMT
ENV TZ=UTC
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 07 Aug 2025 16:05:41 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 07 Aug 2025 16:05:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 07 Aug 2025 16:05:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137c85da229929a08f72e0cfa17aaec9403f65a3da5881d8597fbcc91cbdd1f2`  
		Last Modified: Tue, 12 Aug 2025 17:24:15 GMT  
		Size: 7.2 MB (7151687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f0f4d76285565776b73c89d420a55567190d02146e95bb55b2a043b6113a8e`  
		Last Modified: Tue, 12 Aug 2025 18:49:54 GMT  
		Size: 167.9 MB (167873615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ef3061e624958aab31c4e5978a0f61eeda5c05c194bd11c4b704d446fa1097`  
		Last Modified: Tue, 12 Aug 2025 17:24:11 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1b24d7e886d2fbd34ded6bb6650b314782d91b5b74b7b208959f51a09b95b1`  
		Last Modified: Tue, 12 Aug 2025 17:24:12 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384bebcfcced27c8cc253e9a927dadea48eccc047b126656c50f40eb610959c6`  
		Last Modified: Tue, 12 Aug 2025 17:24:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55573752dbede5172c8eedea40d806a0622935e82410289e57b4b9394f4f147`  
		Last Modified: Tue, 12 Aug 2025 17:24:12 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb76cd2113121f91e3ab02f114cf6252db5f9292d55c9407f5cc537cf6ba237`  
		Last Modified: Tue, 12 Aug 2025 17:24:13 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.6.56` - unknown; unknown

```console
$ docker pull clickhouse@sha256:82eb1fb6bde6c4de016b438a56cb7bd716aaa4629cb957b74e3c93cfe06eb9e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4596f7361fd8a3e99e4345bb0763c6f63d502e4254aaa3c4fe5706b3c9f27f25`

```dockerfile
```

-	Layers:
	-	`sha256:4fad8a220e2457601f329591a0485ba91179ff6374b02e0696775d095f5c25f2`  
		Last Modified: Tue, 12 Aug 2025 18:49:21 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.6.56` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:cf502240469bccc854c9b3fc67e5ca54ec37a3f5ef6df20056f0f8323d42b3db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192912365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7be4817e5d79d7aedd4983a60758916bd520dd58e258225fb62ec07bc1bed9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:14 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:17 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 30 Jul 2025 05:34:17 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:05:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 07 Aug 2025 16:05:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPO_CHANNEL=stable
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 07 Aug 2025 16:05:41 GMT
ARG VERSION=25.3.6.56
# Thu, 07 Aug 2025 16:05:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 16:05:41 GMT
ENV TZ=UTC
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 07 Aug 2025 16:05:41 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 07 Aug 2025 16:05:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 07 Aug 2025 16:05:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e6e0b617b9c63d680a3dee014408e3c901d247257c08f588eb01fd8ab0b0cf`  
		Last Modified: Tue, 12 Aug 2025 17:35:42 GMT  
		Size: 7.1 MB (7127960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa41208f438b689eaf456b07fbfecabf48676b2b7cef271faca1a76e41f0a463`  
		Last Modified: Tue, 12 Aug 2025 18:49:50 GMT  
		Size: 157.6 MB (157554909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa40645d38b2be7a1826a8c5ce4f1672e59b4119987c880641938a181bd9ed83`  
		Last Modified: Tue, 12 Aug 2025 17:35:41 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7826c6a09a2f6eec6e397f6a19aad16112f8387aa6f876f40771f63b54fb2fa`  
		Last Modified: Tue, 12 Aug 2025 17:35:42 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a378edc92a579bbd440d0c7e6b2aa53b121a721e0da76a3d251ba47ad3dd4aa`  
		Last Modified: Tue, 12 Aug 2025 17:35:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9dd5e8c5fe95a063fd9c0b05940f9c20ad696c10e01033a27283229ecc5780`  
		Last Modified: Tue, 12 Aug 2025 17:35:41 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbf8d069153cecb84f87a8a394bf119304fb4b4e8fda23b32c4d191b44c8b55`  
		Last Modified: Tue, 12 Aug 2025 17:35:42 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.6.56` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a71c6061a09f252dac7c36c94adc81c75a467329095ed90329b2bcddadb37a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f25d0f988a9bcd5c1eff72678102496338ffcec6798ffacadbc579eac789164a`

```dockerfile
```

-	Layers:
	-	`sha256:4586c050a3d62b4912f0aff1149618f3e8e444bbc8955c0a08f13d942d02f7d7`  
		Last Modified: Tue, 12 Aug 2025 18:49:25 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.6.56-jammy`

```console
$ docker pull clickhouse@sha256:b2026b4defbdd247c6978d9f77c887340b2aa5d036a4856089ddaa49f95d5e28
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.6.56-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:636ce3aa345c93482ba2f51d9737721e89a96f44ff0fd913ff400b18d50bd125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.4 MB (205432539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0861ca60e97c4a4911b5ab03e22d521e79beaf99aeba2542fca8a4ae16f5fab7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:32:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:32:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:32:14 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 30 Jul 2025 05:32:14 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:05:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 07 Aug 2025 16:05:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPO_CHANNEL=stable
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 07 Aug 2025 16:05:41 GMT
ARG VERSION=25.3.6.56
# Thu, 07 Aug 2025 16:05:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 16:05:41 GMT
ENV TZ=UTC
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 07 Aug 2025 16:05:41 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 07 Aug 2025 16:05:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 07 Aug 2025 16:05:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137c85da229929a08f72e0cfa17aaec9403f65a3da5881d8597fbcc91cbdd1f2`  
		Last Modified: Tue, 12 Aug 2025 17:24:15 GMT  
		Size: 7.2 MB (7151687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f0f4d76285565776b73c89d420a55567190d02146e95bb55b2a043b6113a8e`  
		Last Modified: Tue, 12 Aug 2025 18:49:54 GMT  
		Size: 167.9 MB (167873615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ef3061e624958aab31c4e5978a0f61eeda5c05c194bd11c4b704d446fa1097`  
		Last Modified: Tue, 12 Aug 2025 17:24:11 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1b24d7e886d2fbd34ded6bb6650b314782d91b5b74b7b208959f51a09b95b1`  
		Last Modified: Tue, 12 Aug 2025 17:24:12 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384bebcfcced27c8cc253e9a927dadea48eccc047b126656c50f40eb610959c6`  
		Last Modified: Tue, 12 Aug 2025 17:24:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55573752dbede5172c8eedea40d806a0622935e82410289e57b4b9394f4f147`  
		Last Modified: Tue, 12 Aug 2025 17:24:12 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb76cd2113121f91e3ab02f114cf6252db5f9292d55c9407f5cc537cf6ba237`  
		Last Modified: Tue, 12 Aug 2025 17:24:13 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.6.56-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:82eb1fb6bde6c4de016b438a56cb7bd716aaa4629cb957b74e3c93cfe06eb9e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4596f7361fd8a3e99e4345bb0763c6f63d502e4254aaa3c4fe5706b3c9f27f25`

```dockerfile
```

-	Layers:
	-	`sha256:4fad8a220e2457601f329591a0485ba91179ff6374b02e0696775d095f5c25f2`  
		Last Modified: Tue, 12 Aug 2025 18:49:21 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.6.56-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:cf502240469bccc854c9b3fc67e5ca54ec37a3f5ef6df20056f0f8323d42b3db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192912365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7be4817e5d79d7aedd4983a60758916bd520dd58e258225fb62ec07bc1bed9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:14 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:17 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 30 Jul 2025 05:34:17 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:05:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 07 Aug 2025 16:05:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPO_CHANNEL=stable
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 07 Aug 2025 16:05:41 GMT
ARG VERSION=25.3.6.56
# Thu, 07 Aug 2025 16:05:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 16:05:41 GMT
ENV TZ=UTC
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 07 Aug 2025 16:05:41 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 07 Aug 2025 16:05:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 07 Aug 2025 16:05:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e6e0b617b9c63d680a3dee014408e3c901d247257c08f588eb01fd8ab0b0cf`  
		Last Modified: Tue, 12 Aug 2025 17:35:42 GMT  
		Size: 7.1 MB (7127960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa41208f438b689eaf456b07fbfecabf48676b2b7cef271faca1a76e41f0a463`  
		Last Modified: Tue, 12 Aug 2025 18:49:50 GMT  
		Size: 157.6 MB (157554909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa40645d38b2be7a1826a8c5ce4f1672e59b4119987c880641938a181bd9ed83`  
		Last Modified: Tue, 12 Aug 2025 17:35:41 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7826c6a09a2f6eec6e397f6a19aad16112f8387aa6f876f40771f63b54fb2fa`  
		Last Modified: Tue, 12 Aug 2025 17:35:42 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a378edc92a579bbd440d0c7e6b2aa53b121a721e0da76a3d251ba47ad3dd4aa`  
		Last Modified: Tue, 12 Aug 2025 17:35:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9dd5e8c5fe95a063fd9c0b05940f9c20ad696c10e01033a27283229ecc5780`  
		Last Modified: Tue, 12 Aug 2025 17:35:41 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbf8d069153cecb84f87a8a394bf119304fb4b4e8fda23b32c4d191b44c8b55`  
		Last Modified: Tue, 12 Aug 2025 17:35:42 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.6.56-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a71c6061a09f252dac7c36c94adc81c75a467329095ed90329b2bcddadb37a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f25d0f988a9bcd5c1eff72678102496338ffcec6798ffacadbc579eac789164a`

```dockerfile
```

-	Layers:
	-	`sha256:4586c050a3d62b4912f0aff1149618f3e8e444bbc8955c0a08f13d942d02f7d7`  
		Last Modified: Tue, 12 Aug 2025 18:49:25 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.5`

```console
$ docker pull clickhouse@sha256:aa33165e8a355b7fc32f0421aa33d1cf7e1e391335cb8df8332bd9f6e61be717
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.5` - linux; amd64

```console
$ docker pull clickhouse@sha256:fcd146e8a584be4c58af56ca9b6df508111cbb6caebc0d087587d69ba85e6ad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.0 MB (204952936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9efe53ebf4e1526effa500c4aeaef5790353e995172cdc471d8b95020523307`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:32:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:32:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:32:14 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 30 Jul 2025 05:32:14 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:05:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 07 Aug 2025 16:05:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPO_CHANNEL=stable
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 07 Aug 2025 16:05:41 GMT
ARG VERSION=25.5.9.14
# Thu, 07 Aug 2025 16:05:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 16:05:41 GMT
ENV TZ=UTC
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 07 Aug 2025 16:05:41 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 07 Aug 2025 16:05:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 07 Aug 2025 16:05:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b9ee61a845dbae0fb9c2be83817c1fef9fdbe656a675d4c3a45ad31caa256e`  
		Last Modified: Tue, 12 Aug 2025 17:24:40 GMT  
		Size: 7.2 MB (7151648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b382013c2004f9941d2cfd53020818cc542430be926f1f1188b5db2681887c3f`  
		Last Modified: Tue, 12 Aug 2025 18:50:01 GMT  
		Size: 167.4 MB (167394048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701852115368ba480bdf3f8b92da2ff3d2ca8d511551d33211b8b8ad276db0eb`  
		Last Modified: Tue, 12 Aug 2025 17:24:38 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03832b1d1e55486dc5e79eb8cece00555cf9e86fa7c2e182df9a227cf2e5eda`  
		Last Modified: Tue, 12 Aug 2025 17:24:38 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1083cebbed573dcdd9de448e98f3da859f47997512c71ab4596f2c6a4696fa2c`  
		Last Modified: Tue, 12 Aug 2025 17:24:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31363e68ca5300eb3c35bb07ba939d784cc4e4ba4f8b84920b2cb1dc48015c6b`  
		Last Modified: Tue, 12 Aug 2025 17:24:37 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70448358dc119c655fa38f5e22c49655e57eb515fc8ef17f7caea18b9faeaf0`  
		Last Modified: Tue, 12 Aug 2025 17:24:35 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5` - unknown; unknown

```console
$ docker pull clickhouse@sha256:cebdbde77a09fd2799e6ff4963e97cb40ec05c6aa9b6c7c95ed1da59507fa6a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb16fc5560be91659aa190a6cd3426c491ab55461671bc61909595d5f9cf8e76`

```dockerfile
```

-	Layers:
	-	`sha256:b50e7f1869cf9aff770aa8381576ddf5a4fcb85fc192850ed9d6f7675dfd9f65`  
		Last Modified: Tue, 12 Aug 2025 18:49:39 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.5` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:53b41d88ea9d8c9345a26cc9604b85409a9bd43bfa6e9b7d9804ebd842b9ebae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191528363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c74adbb573fbcfa3c142b959e1fc98c2bdca4951dc63091f8bc05338a3011590`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:14 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:17 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 30 Jul 2025 05:34:17 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:05:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 07 Aug 2025 16:05:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPO_CHANNEL=stable
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 07 Aug 2025 16:05:41 GMT
ARG VERSION=25.5.9.14
# Thu, 07 Aug 2025 16:05:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 16:05:41 GMT
ENV TZ=UTC
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 07 Aug 2025 16:05:41 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 07 Aug 2025 16:05:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 07 Aug 2025 16:05:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2109e05b2e0a5ed21bc73d18e4913a59a775cb95dbc302d5e75d1b4069ce035`  
		Last Modified: Tue, 12 Aug 2025 17:28:05 GMT  
		Size: 7.1 MB (7127934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816ceb2897c432e74a1fbd8de8bb239fc71db09e261dbcedfe04a5c7aeb560e8`  
		Last Modified: Tue, 12 Aug 2025 18:50:10 GMT  
		Size: 156.2 MB (156170934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbd2dd0282ad0ab9f4bf2bc5ee913cb71c2600fe8d3a0f77e3f4e0581280776`  
		Last Modified: Tue, 12 Aug 2025 17:33:47 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d33cf61a11bde6ba163196c8d1bd7a73bb156839d7c7180a0e0513792692e0`  
		Last Modified: Tue, 12 Aug 2025 17:33:48 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd8fdcfbeb1e09ed940fdafc1177863ea564a51b77444ca141b75ffd59d6197`  
		Last Modified: Tue, 12 Aug 2025 17:33:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9477559cc66b1ef0303195d9203e70cf2201b6d7d1620b6bde440498f2586a`  
		Last Modified: Tue, 12 Aug 2025 17:33:49 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aeac7f94bd19fd174b2dbec2e9a6b3dab6594cfd73a7f5dd9390b3ae9a6c8f6`  
		Last Modified: Tue, 12 Aug 2025 17:33:49 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5b744977b1dc83561ecf02f51df8a3615ebd94f2248f923ab7c64e2e897adb70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec3c0ee9ae65c09480f2ecdaa7bf8edd29219f3de72456984bfccf66fa123989`

```dockerfile
```

-	Layers:
	-	`sha256:886831c6f00e976567f807bff495034ae607a4aac9f44b2609d1654046c6a8b9`  
		Last Modified: Tue, 12 Aug 2025 18:49:42 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.5-jammy`

```console
$ docker pull clickhouse@sha256:aa33165e8a355b7fc32f0421aa33d1cf7e1e391335cb8df8332bd9f6e61be717
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.5-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:fcd146e8a584be4c58af56ca9b6df508111cbb6caebc0d087587d69ba85e6ad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.0 MB (204952936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9efe53ebf4e1526effa500c4aeaef5790353e995172cdc471d8b95020523307`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:32:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:32:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:32:14 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 30 Jul 2025 05:32:14 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:05:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 07 Aug 2025 16:05:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPO_CHANNEL=stable
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 07 Aug 2025 16:05:41 GMT
ARG VERSION=25.5.9.14
# Thu, 07 Aug 2025 16:05:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 16:05:41 GMT
ENV TZ=UTC
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 07 Aug 2025 16:05:41 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 07 Aug 2025 16:05:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 07 Aug 2025 16:05:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b9ee61a845dbae0fb9c2be83817c1fef9fdbe656a675d4c3a45ad31caa256e`  
		Last Modified: Tue, 12 Aug 2025 17:24:40 GMT  
		Size: 7.2 MB (7151648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b382013c2004f9941d2cfd53020818cc542430be926f1f1188b5db2681887c3f`  
		Last Modified: Tue, 12 Aug 2025 18:50:01 GMT  
		Size: 167.4 MB (167394048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701852115368ba480bdf3f8b92da2ff3d2ca8d511551d33211b8b8ad276db0eb`  
		Last Modified: Tue, 12 Aug 2025 17:24:38 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03832b1d1e55486dc5e79eb8cece00555cf9e86fa7c2e182df9a227cf2e5eda`  
		Last Modified: Tue, 12 Aug 2025 17:24:38 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1083cebbed573dcdd9de448e98f3da859f47997512c71ab4596f2c6a4696fa2c`  
		Last Modified: Tue, 12 Aug 2025 17:24:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31363e68ca5300eb3c35bb07ba939d784cc4e4ba4f8b84920b2cb1dc48015c6b`  
		Last Modified: Tue, 12 Aug 2025 17:24:37 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70448358dc119c655fa38f5e22c49655e57eb515fc8ef17f7caea18b9faeaf0`  
		Last Modified: Tue, 12 Aug 2025 17:24:35 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:cebdbde77a09fd2799e6ff4963e97cb40ec05c6aa9b6c7c95ed1da59507fa6a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb16fc5560be91659aa190a6cd3426c491ab55461671bc61909595d5f9cf8e76`

```dockerfile
```

-	Layers:
	-	`sha256:b50e7f1869cf9aff770aa8381576ddf5a4fcb85fc192850ed9d6f7675dfd9f65`  
		Last Modified: Tue, 12 Aug 2025 18:49:39 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.5-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:53b41d88ea9d8c9345a26cc9604b85409a9bd43bfa6e9b7d9804ebd842b9ebae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191528363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c74adbb573fbcfa3c142b959e1fc98c2bdca4951dc63091f8bc05338a3011590`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:14 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:17 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 30 Jul 2025 05:34:17 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:05:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 07 Aug 2025 16:05:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPO_CHANNEL=stable
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 07 Aug 2025 16:05:41 GMT
ARG VERSION=25.5.9.14
# Thu, 07 Aug 2025 16:05:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 16:05:41 GMT
ENV TZ=UTC
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 07 Aug 2025 16:05:41 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 07 Aug 2025 16:05:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 07 Aug 2025 16:05:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2109e05b2e0a5ed21bc73d18e4913a59a775cb95dbc302d5e75d1b4069ce035`  
		Last Modified: Tue, 12 Aug 2025 17:28:05 GMT  
		Size: 7.1 MB (7127934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816ceb2897c432e74a1fbd8de8bb239fc71db09e261dbcedfe04a5c7aeb560e8`  
		Last Modified: Tue, 12 Aug 2025 18:50:10 GMT  
		Size: 156.2 MB (156170934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbd2dd0282ad0ab9f4bf2bc5ee913cb71c2600fe8d3a0f77e3f4e0581280776`  
		Last Modified: Tue, 12 Aug 2025 17:33:47 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d33cf61a11bde6ba163196c8d1bd7a73bb156839d7c7180a0e0513792692e0`  
		Last Modified: Tue, 12 Aug 2025 17:33:48 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd8fdcfbeb1e09ed940fdafc1177863ea564a51b77444ca141b75ffd59d6197`  
		Last Modified: Tue, 12 Aug 2025 17:33:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9477559cc66b1ef0303195d9203e70cf2201b6d7d1620b6bde440498f2586a`  
		Last Modified: Tue, 12 Aug 2025 17:33:49 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aeac7f94bd19fd174b2dbec2e9a6b3dab6594cfd73a7f5dd9390b3ae9a6c8f6`  
		Last Modified: Tue, 12 Aug 2025 17:33:49 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5b744977b1dc83561ecf02f51df8a3615ebd94f2248f923ab7c64e2e897adb70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec3c0ee9ae65c09480f2ecdaa7bf8edd29219f3de72456984bfccf66fa123989`

```dockerfile
```

-	Layers:
	-	`sha256:886831c6f00e976567f807bff495034ae607a4aac9f44b2609d1654046c6a8b9`  
		Last Modified: Tue, 12 Aug 2025 18:49:42 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.5.9`

```console
$ docker pull clickhouse@sha256:aa33165e8a355b7fc32f0421aa33d1cf7e1e391335cb8df8332bd9f6e61be717
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.5.9` - linux; amd64

```console
$ docker pull clickhouse@sha256:fcd146e8a584be4c58af56ca9b6df508111cbb6caebc0d087587d69ba85e6ad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.0 MB (204952936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9efe53ebf4e1526effa500c4aeaef5790353e995172cdc471d8b95020523307`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:32:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:32:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:32:14 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 30 Jul 2025 05:32:14 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:05:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 07 Aug 2025 16:05:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPO_CHANNEL=stable
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 07 Aug 2025 16:05:41 GMT
ARG VERSION=25.5.9.14
# Thu, 07 Aug 2025 16:05:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 16:05:41 GMT
ENV TZ=UTC
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 07 Aug 2025 16:05:41 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 07 Aug 2025 16:05:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 07 Aug 2025 16:05:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b9ee61a845dbae0fb9c2be83817c1fef9fdbe656a675d4c3a45ad31caa256e`  
		Last Modified: Tue, 12 Aug 2025 17:24:40 GMT  
		Size: 7.2 MB (7151648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b382013c2004f9941d2cfd53020818cc542430be926f1f1188b5db2681887c3f`  
		Last Modified: Tue, 12 Aug 2025 18:50:01 GMT  
		Size: 167.4 MB (167394048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701852115368ba480bdf3f8b92da2ff3d2ca8d511551d33211b8b8ad276db0eb`  
		Last Modified: Tue, 12 Aug 2025 17:24:38 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03832b1d1e55486dc5e79eb8cece00555cf9e86fa7c2e182df9a227cf2e5eda`  
		Last Modified: Tue, 12 Aug 2025 17:24:38 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1083cebbed573dcdd9de448e98f3da859f47997512c71ab4596f2c6a4696fa2c`  
		Last Modified: Tue, 12 Aug 2025 17:24:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31363e68ca5300eb3c35bb07ba939d784cc4e4ba4f8b84920b2cb1dc48015c6b`  
		Last Modified: Tue, 12 Aug 2025 17:24:37 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70448358dc119c655fa38f5e22c49655e57eb515fc8ef17f7caea18b9faeaf0`  
		Last Modified: Tue, 12 Aug 2025 17:24:35 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5.9` - unknown; unknown

```console
$ docker pull clickhouse@sha256:cebdbde77a09fd2799e6ff4963e97cb40ec05c6aa9b6c7c95ed1da59507fa6a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb16fc5560be91659aa190a6cd3426c491ab55461671bc61909595d5f9cf8e76`

```dockerfile
```

-	Layers:
	-	`sha256:b50e7f1869cf9aff770aa8381576ddf5a4fcb85fc192850ed9d6f7675dfd9f65`  
		Last Modified: Tue, 12 Aug 2025 18:49:39 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.5.9` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:53b41d88ea9d8c9345a26cc9604b85409a9bd43bfa6e9b7d9804ebd842b9ebae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191528363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c74adbb573fbcfa3c142b959e1fc98c2bdca4951dc63091f8bc05338a3011590`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:14 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:17 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 30 Jul 2025 05:34:17 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:05:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 07 Aug 2025 16:05:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPO_CHANNEL=stable
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 07 Aug 2025 16:05:41 GMT
ARG VERSION=25.5.9.14
# Thu, 07 Aug 2025 16:05:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 16:05:41 GMT
ENV TZ=UTC
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 07 Aug 2025 16:05:41 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 07 Aug 2025 16:05:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 07 Aug 2025 16:05:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2109e05b2e0a5ed21bc73d18e4913a59a775cb95dbc302d5e75d1b4069ce035`  
		Last Modified: Tue, 12 Aug 2025 17:28:05 GMT  
		Size: 7.1 MB (7127934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816ceb2897c432e74a1fbd8de8bb239fc71db09e261dbcedfe04a5c7aeb560e8`  
		Last Modified: Tue, 12 Aug 2025 18:50:10 GMT  
		Size: 156.2 MB (156170934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbd2dd0282ad0ab9f4bf2bc5ee913cb71c2600fe8d3a0f77e3f4e0581280776`  
		Last Modified: Tue, 12 Aug 2025 17:33:47 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d33cf61a11bde6ba163196c8d1bd7a73bb156839d7c7180a0e0513792692e0`  
		Last Modified: Tue, 12 Aug 2025 17:33:48 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd8fdcfbeb1e09ed940fdafc1177863ea564a51b77444ca141b75ffd59d6197`  
		Last Modified: Tue, 12 Aug 2025 17:33:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9477559cc66b1ef0303195d9203e70cf2201b6d7d1620b6bde440498f2586a`  
		Last Modified: Tue, 12 Aug 2025 17:33:49 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aeac7f94bd19fd174b2dbec2e9a6b3dab6594cfd73a7f5dd9390b3ae9a6c8f6`  
		Last Modified: Tue, 12 Aug 2025 17:33:49 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5.9` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5b744977b1dc83561ecf02f51df8a3615ebd94f2248f923ab7c64e2e897adb70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec3c0ee9ae65c09480f2ecdaa7bf8edd29219f3de72456984bfccf66fa123989`

```dockerfile
```

-	Layers:
	-	`sha256:886831c6f00e976567f807bff495034ae607a4aac9f44b2609d1654046c6a8b9`  
		Last Modified: Tue, 12 Aug 2025 18:49:42 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.5.9-jammy`

```console
$ docker pull clickhouse@sha256:aa33165e8a355b7fc32f0421aa33d1cf7e1e391335cb8df8332bd9f6e61be717
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.5.9-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:fcd146e8a584be4c58af56ca9b6df508111cbb6caebc0d087587d69ba85e6ad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.0 MB (204952936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9efe53ebf4e1526effa500c4aeaef5790353e995172cdc471d8b95020523307`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:32:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:32:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:32:14 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 30 Jul 2025 05:32:14 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:05:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 07 Aug 2025 16:05:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPO_CHANNEL=stable
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 07 Aug 2025 16:05:41 GMT
ARG VERSION=25.5.9.14
# Thu, 07 Aug 2025 16:05:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 16:05:41 GMT
ENV TZ=UTC
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 07 Aug 2025 16:05:41 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 07 Aug 2025 16:05:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 07 Aug 2025 16:05:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b9ee61a845dbae0fb9c2be83817c1fef9fdbe656a675d4c3a45ad31caa256e`  
		Last Modified: Tue, 12 Aug 2025 17:24:40 GMT  
		Size: 7.2 MB (7151648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b382013c2004f9941d2cfd53020818cc542430be926f1f1188b5db2681887c3f`  
		Last Modified: Tue, 12 Aug 2025 18:50:01 GMT  
		Size: 167.4 MB (167394048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701852115368ba480bdf3f8b92da2ff3d2ca8d511551d33211b8b8ad276db0eb`  
		Last Modified: Tue, 12 Aug 2025 17:24:38 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03832b1d1e55486dc5e79eb8cece00555cf9e86fa7c2e182df9a227cf2e5eda`  
		Last Modified: Tue, 12 Aug 2025 17:24:38 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1083cebbed573dcdd9de448e98f3da859f47997512c71ab4596f2c6a4696fa2c`  
		Last Modified: Tue, 12 Aug 2025 17:24:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31363e68ca5300eb3c35bb07ba939d784cc4e4ba4f8b84920b2cb1dc48015c6b`  
		Last Modified: Tue, 12 Aug 2025 17:24:37 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70448358dc119c655fa38f5e22c49655e57eb515fc8ef17f7caea18b9faeaf0`  
		Last Modified: Tue, 12 Aug 2025 17:24:35 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5.9-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:cebdbde77a09fd2799e6ff4963e97cb40ec05c6aa9b6c7c95ed1da59507fa6a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb16fc5560be91659aa190a6cd3426c491ab55461671bc61909595d5f9cf8e76`

```dockerfile
```

-	Layers:
	-	`sha256:b50e7f1869cf9aff770aa8381576ddf5a4fcb85fc192850ed9d6f7675dfd9f65`  
		Last Modified: Tue, 12 Aug 2025 18:49:39 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.5.9-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:53b41d88ea9d8c9345a26cc9604b85409a9bd43bfa6e9b7d9804ebd842b9ebae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191528363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c74adbb573fbcfa3c142b959e1fc98c2bdca4951dc63091f8bc05338a3011590`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:14 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:17 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 30 Jul 2025 05:34:17 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:05:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 07 Aug 2025 16:05:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPO_CHANNEL=stable
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 07 Aug 2025 16:05:41 GMT
ARG VERSION=25.5.9.14
# Thu, 07 Aug 2025 16:05:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 16:05:41 GMT
ENV TZ=UTC
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 07 Aug 2025 16:05:41 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 07 Aug 2025 16:05:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 07 Aug 2025 16:05:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2109e05b2e0a5ed21bc73d18e4913a59a775cb95dbc302d5e75d1b4069ce035`  
		Last Modified: Tue, 12 Aug 2025 17:28:05 GMT  
		Size: 7.1 MB (7127934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816ceb2897c432e74a1fbd8de8bb239fc71db09e261dbcedfe04a5c7aeb560e8`  
		Last Modified: Tue, 12 Aug 2025 18:50:10 GMT  
		Size: 156.2 MB (156170934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbd2dd0282ad0ab9f4bf2bc5ee913cb71c2600fe8d3a0f77e3f4e0581280776`  
		Last Modified: Tue, 12 Aug 2025 17:33:47 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d33cf61a11bde6ba163196c8d1bd7a73bb156839d7c7180a0e0513792692e0`  
		Last Modified: Tue, 12 Aug 2025 17:33:48 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd8fdcfbeb1e09ed940fdafc1177863ea564a51b77444ca141b75ffd59d6197`  
		Last Modified: Tue, 12 Aug 2025 17:33:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9477559cc66b1ef0303195d9203e70cf2201b6d7d1620b6bde440498f2586a`  
		Last Modified: Tue, 12 Aug 2025 17:33:49 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aeac7f94bd19fd174b2dbec2e9a6b3dab6594cfd73a7f5dd9390b3ae9a6c8f6`  
		Last Modified: Tue, 12 Aug 2025 17:33:49 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5.9-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5b744977b1dc83561ecf02f51df8a3615ebd94f2248f923ab7c64e2e897adb70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec3c0ee9ae65c09480f2ecdaa7bf8edd29219f3de72456984bfccf66fa123989`

```dockerfile
```

-	Layers:
	-	`sha256:886831c6f00e976567f807bff495034ae607a4aac9f44b2609d1654046c6a8b9`  
		Last Modified: Tue, 12 Aug 2025 18:49:42 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.5.9.14`

```console
$ docker pull clickhouse@sha256:aa33165e8a355b7fc32f0421aa33d1cf7e1e391335cb8df8332bd9f6e61be717
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.5.9.14` - linux; amd64

```console
$ docker pull clickhouse@sha256:fcd146e8a584be4c58af56ca9b6df508111cbb6caebc0d087587d69ba85e6ad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.0 MB (204952936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9efe53ebf4e1526effa500c4aeaef5790353e995172cdc471d8b95020523307`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:32:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:32:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:32:14 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 30 Jul 2025 05:32:14 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:05:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 07 Aug 2025 16:05:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPO_CHANNEL=stable
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 07 Aug 2025 16:05:41 GMT
ARG VERSION=25.5.9.14
# Thu, 07 Aug 2025 16:05:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 16:05:41 GMT
ENV TZ=UTC
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 07 Aug 2025 16:05:41 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 07 Aug 2025 16:05:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 07 Aug 2025 16:05:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b9ee61a845dbae0fb9c2be83817c1fef9fdbe656a675d4c3a45ad31caa256e`  
		Last Modified: Tue, 12 Aug 2025 17:24:40 GMT  
		Size: 7.2 MB (7151648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b382013c2004f9941d2cfd53020818cc542430be926f1f1188b5db2681887c3f`  
		Last Modified: Tue, 12 Aug 2025 18:50:01 GMT  
		Size: 167.4 MB (167394048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701852115368ba480bdf3f8b92da2ff3d2ca8d511551d33211b8b8ad276db0eb`  
		Last Modified: Tue, 12 Aug 2025 17:24:38 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03832b1d1e55486dc5e79eb8cece00555cf9e86fa7c2e182df9a227cf2e5eda`  
		Last Modified: Tue, 12 Aug 2025 17:24:38 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1083cebbed573dcdd9de448e98f3da859f47997512c71ab4596f2c6a4696fa2c`  
		Last Modified: Tue, 12 Aug 2025 17:24:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31363e68ca5300eb3c35bb07ba939d784cc4e4ba4f8b84920b2cb1dc48015c6b`  
		Last Modified: Tue, 12 Aug 2025 17:24:37 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70448358dc119c655fa38f5e22c49655e57eb515fc8ef17f7caea18b9faeaf0`  
		Last Modified: Tue, 12 Aug 2025 17:24:35 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5.9.14` - unknown; unknown

```console
$ docker pull clickhouse@sha256:cebdbde77a09fd2799e6ff4963e97cb40ec05c6aa9b6c7c95ed1da59507fa6a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb16fc5560be91659aa190a6cd3426c491ab55461671bc61909595d5f9cf8e76`

```dockerfile
```

-	Layers:
	-	`sha256:b50e7f1869cf9aff770aa8381576ddf5a4fcb85fc192850ed9d6f7675dfd9f65`  
		Last Modified: Tue, 12 Aug 2025 18:49:39 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.5.9.14` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:53b41d88ea9d8c9345a26cc9604b85409a9bd43bfa6e9b7d9804ebd842b9ebae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191528363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c74adbb573fbcfa3c142b959e1fc98c2bdca4951dc63091f8bc05338a3011590`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:14 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:17 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 30 Jul 2025 05:34:17 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:05:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 07 Aug 2025 16:05:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPO_CHANNEL=stable
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 07 Aug 2025 16:05:41 GMT
ARG VERSION=25.5.9.14
# Thu, 07 Aug 2025 16:05:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 16:05:41 GMT
ENV TZ=UTC
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 07 Aug 2025 16:05:41 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 07 Aug 2025 16:05:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 07 Aug 2025 16:05:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2109e05b2e0a5ed21bc73d18e4913a59a775cb95dbc302d5e75d1b4069ce035`  
		Last Modified: Tue, 12 Aug 2025 17:28:05 GMT  
		Size: 7.1 MB (7127934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816ceb2897c432e74a1fbd8de8bb239fc71db09e261dbcedfe04a5c7aeb560e8`  
		Last Modified: Tue, 12 Aug 2025 18:50:10 GMT  
		Size: 156.2 MB (156170934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbd2dd0282ad0ab9f4bf2bc5ee913cb71c2600fe8d3a0f77e3f4e0581280776`  
		Last Modified: Tue, 12 Aug 2025 17:33:47 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d33cf61a11bde6ba163196c8d1bd7a73bb156839d7c7180a0e0513792692e0`  
		Last Modified: Tue, 12 Aug 2025 17:33:48 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd8fdcfbeb1e09ed940fdafc1177863ea564a51b77444ca141b75ffd59d6197`  
		Last Modified: Tue, 12 Aug 2025 17:33:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9477559cc66b1ef0303195d9203e70cf2201b6d7d1620b6bde440498f2586a`  
		Last Modified: Tue, 12 Aug 2025 17:33:49 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aeac7f94bd19fd174b2dbec2e9a6b3dab6594cfd73a7f5dd9390b3ae9a6c8f6`  
		Last Modified: Tue, 12 Aug 2025 17:33:49 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5.9.14` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5b744977b1dc83561ecf02f51df8a3615ebd94f2248f923ab7c64e2e897adb70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec3c0ee9ae65c09480f2ecdaa7bf8edd29219f3de72456984bfccf66fa123989`

```dockerfile
```

-	Layers:
	-	`sha256:886831c6f00e976567f807bff495034ae607a4aac9f44b2609d1654046c6a8b9`  
		Last Modified: Tue, 12 Aug 2025 18:49:42 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.5.9.14-jammy`

```console
$ docker pull clickhouse@sha256:aa33165e8a355b7fc32f0421aa33d1cf7e1e391335cb8df8332bd9f6e61be717
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.5.9.14-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:fcd146e8a584be4c58af56ca9b6df508111cbb6caebc0d087587d69ba85e6ad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.0 MB (204952936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9efe53ebf4e1526effa500c4aeaef5790353e995172cdc471d8b95020523307`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:32:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:32:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:32:14 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 30 Jul 2025 05:32:14 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:05:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 07 Aug 2025 16:05:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPO_CHANNEL=stable
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 07 Aug 2025 16:05:41 GMT
ARG VERSION=25.5.9.14
# Thu, 07 Aug 2025 16:05:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 16:05:41 GMT
ENV TZ=UTC
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 07 Aug 2025 16:05:41 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 07 Aug 2025 16:05:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 07 Aug 2025 16:05:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b9ee61a845dbae0fb9c2be83817c1fef9fdbe656a675d4c3a45ad31caa256e`  
		Last Modified: Tue, 12 Aug 2025 17:24:40 GMT  
		Size: 7.2 MB (7151648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b382013c2004f9941d2cfd53020818cc542430be926f1f1188b5db2681887c3f`  
		Last Modified: Tue, 12 Aug 2025 18:50:01 GMT  
		Size: 167.4 MB (167394048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701852115368ba480bdf3f8b92da2ff3d2ca8d511551d33211b8b8ad276db0eb`  
		Last Modified: Tue, 12 Aug 2025 17:24:38 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03832b1d1e55486dc5e79eb8cece00555cf9e86fa7c2e182df9a227cf2e5eda`  
		Last Modified: Tue, 12 Aug 2025 17:24:38 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1083cebbed573dcdd9de448e98f3da859f47997512c71ab4596f2c6a4696fa2c`  
		Last Modified: Tue, 12 Aug 2025 17:24:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31363e68ca5300eb3c35bb07ba939d784cc4e4ba4f8b84920b2cb1dc48015c6b`  
		Last Modified: Tue, 12 Aug 2025 17:24:37 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70448358dc119c655fa38f5e22c49655e57eb515fc8ef17f7caea18b9faeaf0`  
		Last Modified: Tue, 12 Aug 2025 17:24:35 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5.9.14-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:cebdbde77a09fd2799e6ff4963e97cb40ec05c6aa9b6c7c95ed1da59507fa6a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb16fc5560be91659aa190a6cd3426c491ab55461671bc61909595d5f9cf8e76`

```dockerfile
```

-	Layers:
	-	`sha256:b50e7f1869cf9aff770aa8381576ddf5a4fcb85fc192850ed9d6f7675dfd9f65`  
		Last Modified: Tue, 12 Aug 2025 18:49:39 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.5.9.14-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:53b41d88ea9d8c9345a26cc9604b85409a9bd43bfa6e9b7d9804ebd842b9ebae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191528363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c74adbb573fbcfa3c142b959e1fc98c2bdca4951dc63091f8bc05338a3011590`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:14 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:17 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 30 Jul 2025 05:34:17 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:05:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 07 Aug 2025 16:05:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPO_CHANNEL=stable
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 07 Aug 2025 16:05:41 GMT
ARG VERSION=25.5.9.14
# Thu, 07 Aug 2025 16:05:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 16:05:41 GMT
ENV TZ=UTC
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.9.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 07 Aug 2025 16:05:41 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 07 Aug 2025 16:05:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 07 Aug 2025 16:05:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2109e05b2e0a5ed21bc73d18e4913a59a775cb95dbc302d5e75d1b4069ce035`  
		Last Modified: Tue, 12 Aug 2025 17:28:05 GMT  
		Size: 7.1 MB (7127934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816ceb2897c432e74a1fbd8de8bb239fc71db09e261dbcedfe04a5c7aeb560e8`  
		Last Modified: Tue, 12 Aug 2025 18:50:10 GMT  
		Size: 156.2 MB (156170934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbd2dd0282ad0ab9f4bf2bc5ee913cb71c2600fe8d3a0f77e3f4e0581280776`  
		Last Modified: Tue, 12 Aug 2025 17:33:47 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d33cf61a11bde6ba163196c8d1bd7a73bb156839d7c7180a0e0513792692e0`  
		Last Modified: Tue, 12 Aug 2025 17:33:48 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd8fdcfbeb1e09ed940fdafc1177863ea564a51b77444ca141b75ffd59d6197`  
		Last Modified: Tue, 12 Aug 2025 17:33:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9477559cc66b1ef0303195d9203e70cf2201b6d7d1620b6bde440498f2586a`  
		Last Modified: Tue, 12 Aug 2025 17:33:49 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aeac7f94bd19fd174b2dbec2e9a6b3dab6594cfd73a7f5dd9390b3ae9a6c8f6`  
		Last Modified: Tue, 12 Aug 2025 17:33:49 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5.9.14-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5b744977b1dc83561ecf02f51df8a3615ebd94f2248f923ab7c64e2e897adb70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec3c0ee9ae65c09480f2ecdaa7bf8edd29219f3de72456984bfccf66fa123989`

```dockerfile
```

-	Layers:
	-	`sha256:886831c6f00e976567f807bff495034ae607a4aac9f44b2609d1654046c6a8b9`  
		Last Modified: Tue, 12 Aug 2025 18:49:42 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.6`

```console
$ docker pull clickhouse@sha256:01b5ca12efa0e75a6f9e188e0594371896996a64037ff2e1aac9a47bae36e4cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6` - linux; amd64

```console
$ docker pull clickhouse@sha256:ea43cfeef1b5c26689618c9dc4c1b0472d9014f5315f1336b33c191e1615ae92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.0 MB (212029095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b66f1510ef6105508130530c0c8f229859b84d734b3b091242e7f8b611e6fa19`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:32:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:32:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:32:14 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 30 Jul 2025 05:32:14 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:05:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 07 Aug 2025 16:05:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPO_CHANNEL=stable
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 07 Aug 2025 16:05:41 GMT
ARG VERSION=25.6.8.10
# Thu, 07 Aug 2025 16:05:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 16:05:41 GMT
ENV TZ=UTC
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 07 Aug 2025 16:05:41 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 07 Aug 2025 16:05:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 07 Aug 2025 16:05:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853c7cf0e26d1540f1ff0c62234c4fce2e87bf6ebcc719b773abe9f618919737`  
		Last Modified: Tue, 12 Aug 2025 18:49:59 GMT  
		Size: 7.2 MB (7151655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8927f5c76c95f6a45dad9c7ac0dbaea0a3fe648efc312e9801f30747b334347d`  
		Last Modified: Tue, 12 Aug 2025 20:31:30 GMT  
		Size: 174.5 MB (174470426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b20567c032a671ce85d1e527537669d385e361614692f562809dd2b55c962d`  
		Last Modified: Tue, 12 Aug 2025 18:25:26 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa3b5d467aeb0d60855d98a58e5eae0961f9acc8976e944af98f9e1c17f32d5`  
		Last Modified: Tue, 12 Aug 2025 18:25:28 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7e10b171f6c1e534825b3534111ebc08814ce81d1ec24ee73fd513dfc6f1c9`  
		Last Modified: Tue, 12 Aug 2025 18:25:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6bb59aeadca638cfa51bdb968e74be3b5e03079f92b4abd9eb1643452eee413`  
		Last Modified: Tue, 12 Aug 2025 18:25:36 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a329dbb55525918fd38ca283960935fc6ccf7b98c80f684afa31e551fc0f04`  
		Last Modified: Tue, 12 Aug 2025 18:25:39 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8966d3b7e72809b5426a5a95a176f82c9d0f4a134f69a6bf181aa429b4f4261f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89deb4fd058297e30d1c2e3af96834fb1c5f4d7e2394cb5790dc624cfa525791`

```dockerfile
```

-	Layers:
	-	`sha256:b10da922cecc5604859ea609897e61c1da2efe7fe7dad07e829788ecf3333eb0`  
		Last Modified: Tue, 12 Aug 2025 18:49:48 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.6` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:0b74f1b21ea10506c37d99a393f2fb8d2217be0754668f937ff174cd6ce32721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198190135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c262ba65a9006129bb34883a053893f6209e82cd725624475f3be8825a434197`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:14 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:17 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 30 Jul 2025 05:34:17 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:05:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 07 Aug 2025 16:05:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPO_CHANNEL=stable
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 07 Aug 2025 16:05:41 GMT
ARG VERSION=25.6.8.10
# Thu, 07 Aug 2025 16:05:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 16:05:41 GMT
ENV TZ=UTC
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 07 Aug 2025 16:05:41 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 07 Aug 2025 16:05:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 07 Aug 2025 16:05:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2109e05b2e0a5ed21bc73d18e4913a59a775cb95dbc302d5e75d1b4069ce035`  
		Last Modified: Tue, 12 Aug 2025 17:28:05 GMT  
		Size: 7.1 MB (7127934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d717407919e10480fd40f3f851ba1a34d3b9fdb46eeb5c299e89b4b45a0ad2ef`  
		Last Modified: Tue, 12 Aug 2025 18:50:18 GMT  
		Size: 162.8 MB (162832928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3901e30537f72745a974d62147e776a154374a731e040f87784eaa9efc66e3`  
		Last Modified: Tue, 12 Aug 2025 17:28:00 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b189a014543df0bb857990a1655f4befd8a16ef04d5117d6b2ef4a3553e51e0`  
		Last Modified: Tue, 12 Aug 2025 17:28:01 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7201364d51d03488cfe058d3171882ac1f4b4ea4fd4f2a3e828a5cbf76481a49`  
		Last Modified: Tue, 12 Aug 2025 17:28:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fec77ba4eed10357772a1e52a1266ee2818030d03c9a6925e854af39aa9c901`  
		Last Modified: Tue, 12 Aug 2025 17:28:01 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3cb8e11d3eb79c137f7f16799d0ffa050bf46b9872e495bebaa382e1adb4cd`  
		Last Modified: Tue, 12 Aug 2025 17:28:00 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6` - unknown; unknown

```console
$ docker pull clickhouse@sha256:be9a127f10f6c754d1debcec49fbcbd3ceae9286d59802eafa0305916ef51151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:252619c2109277bf19856f9c9b3e9ff5eacb81cce6a311cf94046396250b2455`

```dockerfile
```

-	Layers:
	-	`sha256:0e1895c3d91af475ad1002d688f244cfef94a8d3bacb6c1fd7545d2e31e16f4d`  
		Last Modified: Tue, 12 Aug 2025 18:49:51 GMT  
		Size: 25.4 KB (25450 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.6-jammy`

```console
$ docker pull clickhouse@sha256:01b5ca12efa0e75a6f9e188e0594371896996a64037ff2e1aac9a47bae36e4cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:ea43cfeef1b5c26689618c9dc4c1b0472d9014f5315f1336b33c191e1615ae92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.0 MB (212029095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b66f1510ef6105508130530c0c8f229859b84d734b3b091242e7f8b611e6fa19`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:32:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:32:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:32:14 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 30 Jul 2025 05:32:14 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:05:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 07 Aug 2025 16:05:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPO_CHANNEL=stable
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 07 Aug 2025 16:05:41 GMT
ARG VERSION=25.6.8.10
# Thu, 07 Aug 2025 16:05:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 16:05:41 GMT
ENV TZ=UTC
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 07 Aug 2025 16:05:41 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 07 Aug 2025 16:05:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 07 Aug 2025 16:05:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853c7cf0e26d1540f1ff0c62234c4fce2e87bf6ebcc719b773abe9f618919737`  
		Last Modified: Tue, 12 Aug 2025 18:49:59 GMT  
		Size: 7.2 MB (7151655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8927f5c76c95f6a45dad9c7ac0dbaea0a3fe648efc312e9801f30747b334347d`  
		Last Modified: Tue, 12 Aug 2025 20:31:30 GMT  
		Size: 174.5 MB (174470426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b20567c032a671ce85d1e527537669d385e361614692f562809dd2b55c962d`  
		Last Modified: Tue, 12 Aug 2025 18:25:26 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa3b5d467aeb0d60855d98a58e5eae0961f9acc8976e944af98f9e1c17f32d5`  
		Last Modified: Tue, 12 Aug 2025 18:25:28 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7e10b171f6c1e534825b3534111ebc08814ce81d1ec24ee73fd513dfc6f1c9`  
		Last Modified: Tue, 12 Aug 2025 18:25:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6bb59aeadca638cfa51bdb968e74be3b5e03079f92b4abd9eb1643452eee413`  
		Last Modified: Tue, 12 Aug 2025 18:25:36 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a329dbb55525918fd38ca283960935fc6ccf7b98c80f684afa31e551fc0f04`  
		Last Modified: Tue, 12 Aug 2025 18:25:39 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8966d3b7e72809b5426a5a95a176f82c9d0f4a134f69a6bf181aa429b4f4261f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89deb4fd058297e30d1c2e3af96834fb1c5f4d7e2394cb5790dc624cfa525791`

```dockerfile
```

-	Layers:
	-	`sha256:b10da922cecc5604859ea609897e61c1da2efe7fe7dad07e829788ecf3333eb0`  
		Last Modified: Tue, 12 Aug 2025 18:49:48 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.6-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:0b74f1b21ea10506c37d99a393f2fb8d2217be0754668f937ff174cd6ce32721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198190135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c262ba65a9006129bb34883a053893f6209e82cd725624475f3be8825a434197`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:14 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:17 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 30 Jul 2025 05:34:17 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:05:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 07 Aug 2025 16:05:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPO_CHANNEL=stable
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 07 Aug 2025 16:05:41 GMT
ARG VERSION=25.6.8.10
# Thu, 07 Aug 2025 16:05:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 16:05:41 GMT
ENV TZ=UTC
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 07 Aug 2025 16:05:41 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 07 Aug 2025 16:05:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 07 Aug 2025 16:05:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2109e05b2e0a5ed21bc73d18e4913a59a775cb95dbc302d5e75d1b4069ce035`  
		Last Modified: Tue, 12 Aug 2025 17:28:05 GMT  
		Size: 7.1 MB (7127934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d717407919e10480fd40f3f851ba1a34d3b9fdb46eeb5c299e89b4b45a0ad2ef`  
		Last Modified: Tue, 12 Aug 2025 18:50:18 GMT  
		Size: 162.8 MB (162832928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3901e30537f72745a974d62147e776a154374a731e040f87784eaa9efc66e3`  
		Last Modified: Tue, 12 Aug 2025 17:28:00 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b189a014543df0bb857990a1655f4befd8a16ef04d5117d6b2ef4a3553e51e0`  
		Last Modified: Tue, 12 Aug 2025 17:28:01 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7201364d51d03488cfe058d3171882ac1f4b4ea4fd4f2a3e828a5cbf76481a49`  
		Last Modified: Tue, 12 Aug 2025 17:28:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fec77ba4eed10357772a1e52a1266ee2818030d03c9a6925e854af39aa9c901`  
		Last Modified: Tue, 12 Aug 2025 17:28:01 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3cb8e11d3eb79c137f7f16799d0ffa050bf46b9872e495bebaa382e1adb4cd`  
		Last Modified: Tue, 12 Aug 2025 17:28:00 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:be9a127f10f6c754d1debcec49fbcbd3ceae9286d59802eafa0305916ef51151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:252619c2109277bf19856f9c9b3e9ff5eacb81cce6a311cf94046396250b2455`

```dockerfile
```

-	Layers:
	-	`sha256:0e1895c3d91af475ad1002d688f244cfef94a8d3bacb6c1fd7545d2e31e16f4d`  
		Last Modified: Tue, 12 Aug 2025 18:49:51 GMT  
		Size: 25.4 KB (25450 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.6.8`

```console
$ docker pull clickhouse@sha256:01b5ca12efa0e75a6f9e188e0594371896996a64037ff2e1aac9a47bae36e4cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6.8` - linux; amd64

```console
$ docker pull clickhouse@sha256:ea43cfeef1b5c26689618c9dc4c1b0472d9014f5315f1336b33c191e1615ae92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.0 MB (212029095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b66f1510ef6105508130530c0c8f229859b84d734b3b091242e7f8b611e6fa19`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:32:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:32:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:32:14 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 30 Jul 2025 05:32:14 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:05:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 07 Aug 2025 16:05:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPO_CHANNEL=stable
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 07 Aug 2025 16:05:41 GMT
ARG VERSION=25.6.8.10
# Thu, 07 Aug 2025 16:05:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 16:05:41 GMT
ENV TZ=UTC
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 07 Aug 2025 16:05:41 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 07 Aug 2025 16:05:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 07 Aug 2025 16:05:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853c7cf0e26d1540f1ff0c62234c4fce2e87bf6ebcc719b773abe9f618919737`  
		Last Modified: Tue, 12 Aug 2025 18:49:59 GMT  
		Size: 7.2 MB (7151655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8927f5c76c95f6a45dad9c7ac0dbaea0a3fe648efc312e9801f30747b334347d`  
		Last Modified: Tue, 12 Aug 2025 20:31:30 GMT  
		Size: 174.5 MB (174470426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b20567c032a671ce85d1e527537669d385e361614692f562809dd2b55c962d`  
		Last Modified: Tue, 12 Aug 2025 18:25:26 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa3b5d467aeb0d60855d98a58e5eae0961f9acc8976e944af98f9e1c17f32d5`  
		Last Modified: Tue, 12 Aug 2025 18:25:28 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7e10b171f6c1e534825b3534111ebc08814ce81d1ec24ee73fd513dfc6f1c9`  
		Last Modified: Tue, 12 Aug 2025 18:25:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6bb59aeadca638cfa51bdb968e74be3b5e03079f92b4abd9eb1643452eee413`  
		Last Modified: Tue, 12 Aug 2025 18:25:36 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a329dbb55525918fd38ca283960935fc6ccf7b98c80f684afa31e551fc0f04`  
		Last Modified: Tue, 12 Aug 2025 18:25:39 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8966d3b7e72809b5426a5a95a176f82c9d0f4a134f69a6bf181aa429b4f4261f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89deb4fd058297e30d1c2e3af96834fb1c5f4d7e2394cb5790dc624cfa525791`

```dockerfile
```

-	Layers:
	-	`sha256:b10da922cecc5604859ea609897e61c1da2efe7fe7dad07e829788ecf3333eb0`  
		Last Modified: Tue, 12 Aug 2025 18:49:48 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.6.8` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:0b74f1b21ea10506c37d99a393f2fb8d2217be0754668f937ff174cd6ce32721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198190135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c262ba65a9006129bb34883a053893f6209e82cd725624475f3be8825a434197`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:14 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:17 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 30 Jul 2025 05:34:17 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:05:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 07 Aug 2025 16:05:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPO_CHANNEL=stable
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 07 Aug 2025 16:05:41 GMT
ARG VERSION=25.6.8.10
# Thu, 07 Aug 2025 16:05:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 16:05:41 GMT
ENV TZ=UTC
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 07 Aug 2025 16:05:41 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 07 Aug 2025 16:05:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 07 Aug 2025 16:05:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2109e05b2e0a5ed21bc73d18e4913a59a775cb95dbc302d5e75d1b4069ce035`  
		Last Modified: Tue, 12 Aug 2025 17:28:05 GMT  
		Size: 7.1 MB (7127934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d717407919e10480fd40f3f851ba1a34d3b9fdb46eeb5c299e89b4b45a0ad2ef`  
		Last Modified: Tue, 12 Aug 2025 18:50:18 GMT  
		Size: 162.8 MB (162832928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3901e30537f72745a974d62147e776a154374a731e040f87784eaa9efc66e3`  
		Last Modified: Tue, 12 Aug 2025 17:28:00 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b189a014543df0bb857990a1655f4befd8a16ef04d5117d6b2ef4a3553e51e0`  
		Last Modified: Tue, 12 Aug 2025 17:28:01 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7201364d51d03488cfe058d3171882ac1f4b4ea4fd4f2a3e828a5cbf76481a49`  
		Last Modified: Tue, 12 Aug 2025 17:28:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fec77ba4eed10357772a1e52a1266ee2818030d03c9a6925e854af39aa9c901`  
		Last Modified: Tue, 12 Aug 2025 17:28:01 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3cb8e11d3eb79c137f7f16799d0ffa050bf46b9872e495bebaa382e1adb4cd`  
		Last Modified: Tue, 12 Aug 2025 17:28:00 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:be9a127f10f6c754d1debcec49fbcbd3ceae9286d59802eafa0305916ef51151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:252619c2109277bf19856f9c9b3e9ff5eacb81cce6a311cf94046396250b2455`

```dockerfile
```

-	Layers:
	-	`sha256:0e1895c3d91af475ad1002d688f244cfef94a8d3bacb6c1fd7545d2e31e16f4d`  
		Last Modified: Tue, 12 Aug 2025 18:49:51 GMT  
		Size: 25.4 KB (25450 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.6.8-jammy`

```console
$ docker pull clickhouse@sha256:01b5ca12efa0e75a6f9e188e0594371896996a64037ff2e1aac9a47bae36e4cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6.8-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:ea43cfeef1b5c26689618c9dc4c1b0472d9014f5315f1336b33c191e1615ae92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.0 MB (212029095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b66f1510ef6105508130530c0c8f229859b84d734b3b091242e7f8b611e6fa19`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:32:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:32:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:32:14 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 30 Jul 2025 05:32:14 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:05:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 07 Aug 2025 16:05:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPO_CHANNEL=stable
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 07 Aug 2025 16:05:41 GMT
ARG VERSION=25.6.8.10
# Thu, 07 Aug 2025 16:05:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 16:05:41 GMT
ENV TZ=UTC
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 07 Aug 2025 16:05:41 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 07 Aug 2025 16:05:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 07 Aug 2025 16:05:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853c7cf0e26d1540f1ff0c62234c4fce2e87bf6ebcc719b773abe9f618919737`  
		Last Modified: Tue, 12 Aug 2025 18:49:59 GMT  
		Size: 7.2 MB (7151655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8927f5c76c95f6a45dad9c7ac0dbaea0a3fe648efc312e9801f30747b334347d`  
		Last Modified: Tue, 12 Aug 2025 20:31:30 GMT  
		Size: 174.5 MB (174470426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b20567c032a671ce85d1e527537669d385e361614692f562809dd2b55c962d`  
		Last Modified: Tue, 12 Aug 2025 18:25:26 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa3b5d467aeb0d60855d98a58e5eae0961f9acc8976e944af98f9e1c17f32d5`  
		Last Modified: Tue, 12 Aug 2025 18:25:28 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7e10b171f6c1e534825b3534111ebc08814ce81d1ec24ee73fd513dfc6f1c9`  
		Last Modified: Tue, 12 Aug 2025 18:25:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6bb59aeadca638cfa51bdb968e74be3b5e03079f92b4abd9eb1643452eee413`  
		Last Modified: Tue, 12 Aug 2025 18:25:36 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a329dbb55525918fd38ca283960935fc6ccf7b98c80f684afa31e551fc0f04`  
		Last Modified: Tue, 12 Aug 2025 18:25:39 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8966d3b7e72809b5426a5a95a176f82c9d0f4a134f69a6bf181aa429b4f4261f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89deb4fd058297e30d1c2e3af96834fb1c5f4d7e2394cb5790dc624cfa525791`

```dockerfile
```

-	Layers:
	-	`sha256:b10da922cecc5604859ea609897e61c1da2efe7fe7dad07e829788ecf3333eb0`  
		Last Modified: Tue, 12 Aug 2025 18:49:48 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.6.8-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:0b74f1b21ea10506c37d99a393f2fb8d2217be0754668f937ff174cd6ce32721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198190135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c262ba65a9006129bb34883a053893f6209e82cd725624475f3be8825a434197`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:14 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:17 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 30 Jul 2025 05:34:17 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:05:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 07 Aug 2025 16:05:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPO_CHANNEL=stable
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 07 Aug 2025 16:05:41 GMT
ARG VERSION=25.6.8.10
# Thu, 07 Aug 2025 16:05:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 16:05:41 GMT
ENV TZ=UTC
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 07 Aug 2025 16:05:41 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 07 Aug 2025 16:05:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 07 Aug 2025 16:05:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2109e05b2e0a5ed21bc73d18e4913a59a775cb95dbc302d5e75d1b4069ce035`  
		Last Modified: Tue, 12 Aug 2025 17:28:05 GMT  
		Size: 7.1 MB (7127934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d717407919e10480fd40f3f851ba1a34d3b9fdb46eeb5c299e89b4b45a0ad2ef`  
		Last Modified: Tue, 12 Aug 2025 18:50:18 GMT  
		Size: 162.8 MB (162832928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3901e30537f72745a974d62147e776a154374a731e040f87784eaa9efc66e3`  
		Last Modified: Tue, 12 Aug 2025 17:28:00 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b189a014543df0bb857990a1655f4befd8a16ef04d5117d6b2ef4a3553e51e0`  
		Last Modified: Tue, 12 Aug 2025 17:28:01 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7201364d51d03488cfe058d3171882ac1f4b4ea4fd4f2a3e828a5cbf76481a49`  
		Last Modified: Tue, 12 Aug 2025 17:28:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fec77ba4eed10357772a1e52a1266ee2818030d03c9a6925e854af39aa9c901`  
		Last Modified: Tue, 12 Aug 2025 17:28:01 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3cb8e11d3eb79c137f7f16799d0ffa050bf46b9872e495bebaa382e1adb4cd`  
		Last Modified: Tue, 12 Aug 2025 17:28:00 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:be9a127f10f6c754d1debcec49fbcbd3ceae9286d59802eafa0305916ef51151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:252619c2109277bf19856f9c9b3e9ff5eacb81cce6a311cf94046396250b2455`

```dockerfile
```

-	Layers:
	-	`sha256:0e1895c3d91af475ad1002d688f244cfef94a8d3bacb6c1fd7545d2e31e16f4d`  
		Last Modified: Tue, 12 Aug 2025 18:49:51 GMT  
		Size: 25.4 KB (25450 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.6.8.10`

```console
$ docker pull clickhouse@sha256:01b5ca12efa0e75a6f9e188e0594371896996a64037ff2e1aac9a47bae36e4cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6.8.10` - linux; amd64

```console
$ docker pull clickhouse@sha256:ea43cfeef1b5c26689618c9dc4c1b0472d9014f5315f1336b33c191e1615ae92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.0 MB (212029095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b66f1510ef6105508130530c0c8f229859b84d734b3b091242e7f8b611e6fa19`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:32:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:32:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:32:14 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 30 Jul 2025 05:32:14 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:05:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 07 Aug 2025 16:05:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPO_CHANNEL=stable
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 07 Aug 2025 16:05:41 GMT
ARG VERSION=25.6.8.10
# Thu, 07 Aug 2025 16:05:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 16:05:41 GMT
ENV TZ=UTC
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 07 Aug 2025 16:05:41 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 07 Aug 2025 16:05:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 07 Aug 2025 16:05:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853c7cf0e26d1540f1ff0c62234c4fce2e87bf6ebcc719b773abe9f618919737`  
		Last Modified: Tue, 12 Aug 2025 18:49:59 GMT  
		Size: 7.2 MB (7151655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8927f5c76c95f6a45dad9c7ac0dbaea0a3fe648efc312e9801f30747b334347d`  
		Last Modified: Tue, 12 Aug 2025 20:31:30 GMT  
		Size: 174.5 MB (174470426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b20567c032a671ce85d1e527537669d385e361614692f562809dd2b55c962d`  
		Last Modified: Tue, 12 Aug 2025 18:25:26 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa3b5d467aeb0d60855d98a58e5eae0961f9acc8976e944af98f9e1c17f32d5`  
		Last Modified: Tue, 12 Aug 2025 18:25:28 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7e10b171f6c1e534825b3534111ebc08814ce81d1ec24ee73fd513dfc6f1c9`  
		Last Modified: Tue, 12 Aug 2025 18:25:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6bb59aeadca638cfa51bdb968e74be3b5e03079f92b4abd9eb1643452eee413`  
		Last Modified: Tue, 12 Aug 2025 18:25:36 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a329dbb55525918fd38ca283960935fc6ccf7b98c80f684afa31e551fc0f04`  
		Last Modified: Tue, 12 Aug 2025 18:25:39 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.8.10` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8966d3b7e72809b5426a5a95a176f82c9d0f4a134f69a6bf181aa429b4f4261f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89deb4fd058297e30d1c2e3af96834fb1c5f4d7e2394cb5790dc624cfa525791`

```dockerfile
```

-	Layers:
	-	`sha256:b10da922cecc5604859ea609897e61c1da2efe7fe7dad07e829788ecf3333eb0`  
		Last Modified: Tue, 12 Aug 2025 18:49:48 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.6.8.10` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:0b74f1b21ea10506c37d99a393f2fb8d2217be0754668f937ff174cd6ce32721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198190135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c262ba65a9006129bb34883a053893f6209e82cd725624475f3be8825a434197`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:14 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:17 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 30 Jul 2025 05:34:17 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:05:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 07 Aug 2025 16:05:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPO_CHANNEL=stable
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 07 Aug 2025 16:05:41 GMT
ARG VERSION=25.6.8.10
# Thu, 07 Aug 2025 16:05:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 16:05:41 GMT
ENV TZ=UTC
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 07 Aug 2025 16:05:41 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 07 Aug 2025 16:05:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 07 Aug 2025 16:05:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2109e05b2e0a5ed21bc73d18e4913a59a775cb95dbc302d5e75d1b4069ce035`  
		Last Modified: Tue, 12 Aug 2025 17:28:05 GMT  
		Size: 7.1 MB (7127934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d717407919e10480fd40f3f851ba1a34d3b9fdb46eeb5c299e89b4b45a0ad2ef`  
		Last Modified: Tue, 12 Aug 2025 18:50:18 GMT  
		Size: 162.8 MB (162832928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3901e30537f72745a974d62147e776a154374a731e040f87784eaa9efc66e3`  
		Last Modified: Tue, 12 Aug 2025 17:28:00 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b189a014543df0bb857990a1655f4befd8a16ef04d5117d6b2ef4a3553e51e0`  
		Last Modified: Tue, 12 Aug 2025 17:28:01 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7201364d51d03488cfe058d3171882ac1f4b4ea4fd4f2a3e828a5cbf76481a49`  
		Last Modified: Tue, 12 Aug 2025 17:28:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fec77ba4eed10357772a1e52a1266ee2818030d03c9a6925e854af39aa9c901`  
		Last Modified: Tue, 12 Aug 2025 17:28:01 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3cb8e11d3eb79c137f7f16799d0ffa050bf46b9872e495bebaa382e1adb4cd`  
		Last Modified: Tue, 12 Aug 2025 17:28:00 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.8.10` - unknown; unknown

```console
$ docker pull clickhouse@sha256:be9a127f10f6c754d1debcec49fbcbd3ceae9286d59802eafa0305916ef51151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:252619c2109277bf19856f9c9b3e9ff5eacb81cce6a311cf94046396250b2455`

```dockerfile
```

-	Layers:
	-	`sha256:0e1895c3d91af475ad1002d688f244cfef94a8d3bacb6c1fd7545d2e31e16f4d`  
		Last Modified: Tue, 12 Aug 2025 18:49:51 GMT  
		Size: 25.4 KB (25450 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.6.8.10-jammy`

```console
$ docker pull clickhouse@sha256:01b5ca12efa0e75a6f9e188e0594371896996a64037ff2e1aac9a47bae36e4cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6.8.10-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:ea43cfeef1b5c26689618c9dc4c1b0472d9014f5315f1336b33c191e1615ae92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.0 MB (212029095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b66f1510ef6105508130530c0c8f229859b84d734b3b091242e7f8b611e6fa19`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:32:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:32:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:32:14 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 30 Jul 2025 05:32:14 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:05:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 07 Aug 2025 16:05:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPO_CHANNEL=stable
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 07 Aug 2025 16:05:41 GMT
ARG VERSION=25.6.8.10
# Thu, 07 Aug 2025 16:05:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 16:05:41 GMT
ENV TZ=UTC
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 07 Aug 2025 16:05:41 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 07 Aug 2025 16:05:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 07 Aug 2025 16:05:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853c7cf0e26d1540f1ff0c62234c4fce2e87bf6ebcc719b773abe9f618919737`  
		Last Modified: Tue, 12 Aug 2025 18:49:59 GMT  
		Size: 7.2 MB (7151655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8927f5c76c95f6a45dad9c7ac0dbaea0a3fe648efc312e9801f30747b334347d`  
		Last Modified: Tue, 12 Aug 2025 20:31:30 GMT  
		Size: 174.5 MB (174470426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b20567c032a671ce85d1e527537669d385e361614692f562809dd2b55c962d`  
		Last Modified: Tue, 12 Aug 2025 18:25:26 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa3b5d467aeb0d60855d98a58e5eae0961f9acc8976e944af98f9e1c17f32d5`  
		Last Modified: Tue, 12 Aug 2025 18:25:28 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7e10b171f6c1e534825b3534111ebc08814ce81d1ec24ee73fd513dfc6f1c9`  
		Last Modified: Tue, 12 Aug 2025 18:25:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6bb59aeadca638cfa51bdb968e74be3b5e03079f92b4abd9eb1643452eee413`  
		Last Modified: Tue, 12 Aug 2025 18:25:36 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a329dbb55525918fd38ca283960935fc6ccf7b98c80f684afa31e551fc0f04`  
		Last Modified: Tue, 12 Aug 2025 18:25:39 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.8.10-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8966d3b7e72809b5426a5a95a176f82c9d0f4a134f69a6bf181aa429b4f4261f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89deb4fd058297e30d1c2e3af96834fb1c5f4d7e2394cb5790dc624cfa525791`

```dockerfile
```

-	Layers:
	-	`sha256:b10da922cecc5604859ea609897e61c1da2efe7fe7dad07e829788ecf3333eb0`  
		Last Modified: Tue, 12 Aug 2025 18:49:48 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.6.8.10-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:0b74f1b21ea10506c37d99a393f2fb8d2217be0754668f937ff174cd6ce32721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198190135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c262ba65a9006129bb34883a053893f6209e82cd725624475f3be8825a434197`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:14 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:17 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 30 Jul 2025 05:34:17 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:05:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 07 Aug 2025 16:05:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPO_CHANNEL=stable
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 07 Aug 2025 16:05:41 GMT
ARG VERSION=25.6.8.10
# Thu, 07 Aug 2025 16:05:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 16:05:41 GMT
ENV TZ=UTC
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 07 Aug 2025 16:05:41 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 07 Aug 2025 16:05:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 07 Aug 2025 16:05:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2109e05b2e0a5ed21bc73d18e4913a59a775cb95dbc302d5e75d1b4069ce035`  
		Last Modified: Tue, 12 Aug 2025 17:28:05 GMT  
		Size: 7.1 MB (7127934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d717407919e10480fd40f3f851ba1a34d3b9fdb46eeb5c299e89b4b45a0ad2ef`  
		Last Modified: Tue, 12 Aug 2025 18:50:18 GMT  
		Size: 162.8 MB (162832928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3901e30537f72745a974d62147e776a154374a731e040f87784eaa9efc66e3`  
		Last Modified: Tue, 12 Aug 2025 17:28:00 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b189a014543df0bb857990a1655f4befd8a16ef04d5117d6b2ef4a3553e51e0`  
		Last Modified: Tue, 12 Aug 2025 17:28:01 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7201364d51d03488cfe058d3171882ac1f4b4ea4fd4f2a3e828a5cbf76481a49`  
		Last Modified: Tue, 12 Aug 2025 17:28:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fec77ba4eed10357772a1e52a1266ee2818030d03c9a6925e854af39aa9c901`  
		Last Modified: Tue, 12 Aug 2025 17:28:01 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3cb8e11d3eb79c137f7f16799d0ffa050bf46b9872e495bebaa382e1adb4cd`  
		Last Modified: Tue, 12 Aug 2025 17:28:00 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.8.10-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:be9a127f10f6c754d1debcec49fbcbd3ceae9286d59802eafa0305916ef51151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:252619c2109277bf19856f9c9b3e9ff5eacb81cce6a311cf94046396250b2455`

```dockerfile
```

-	Layers:
	-	`sha256:0e1895c3d91af475ad1002d688f244cfef94a8d3bacb6c1fd7545d2e31e16f4d`  
		Last Modified: Tue, 12 Aug 2025 18:49:51 GMT  
		Size: 25.4 KB (25450 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.7`

```console
$ docker pull clickhouse@sha256:cb508b298560ec995d8ae212df1a9f2a45b6fe52a808d16a649f46c38f32e22c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.7` - linux; amd64

```console
$ docker pull clickhouse@sha256:c4bf9ef5c0ba0e82ef2469983af6bee00fcabcde75396f730a077f6fe9e20917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.8 MB (221779604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577e072221ce4b820d7c599d3833d401ca56cbdad732cc02216cab04517d5714`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:32:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:32:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:32:14 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 30 Jul 2025 05:32:14 GMT
CMD ["/bin/bash"]
# Thu, 14 Aug 2025 16:05:39 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 14 Aug 2025 16:05:39 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
ARG REPO_CHANNEL=stable
# Thu, 14 Aug 2025 16:05:39 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 14 Aug 2025 16:05:39 GMT
ARG VERSION=25.7.4.11
# Thu, 14 Aug 2025 16:05:39 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
ENV LANG=en_US.UTF-8
# Thu, 14 Aug 2025 16:05:39 GMT
ENV TZ=UTC
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 14 Aug 2025 16:05:39 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 14 Aug 2025 16:05:39 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 14 Aug 2025 16:05:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2b1ff853e348471606bdabae3dbeca582dc076f0a12400b20b6a0d3eec0e20`  
		Last Modified: Thu, 14 Aug 2025 17:28:33 GMT  
		Size: 7.6 MB (7598470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a491a1d2b5ea4b1ff196b10523f89bde73de85e3634f19dc9d8c9f235c56dbeb`  
		Last Modified: Thu, 14 Aug 2025 18:50:16 GMT  
		Size: 183.8 MB (183774118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7690c20a34e22cf7d5173eee36489a7d9217387d1b6425d41f530d64164fb9c9`  
		Last Modified: Thu, 14 Aug 2025 17:28:31 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d9a2267bb087200f032b91d07eb2993af87cbdc6ea6f1c23e058999f25670d`  
		Last Modified: Thu, 14 Aug 2025 17:28:31 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d41a2fb8dc49d5b2e8f8f7e6592acdd26dd09c2d1ec46a7da5ab63c08e0679`  
		Last Modified: Thu, 14 Aug 2025 17:28:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093a89a665149b53a3d981455e0fdc995ac2ee38effda627a80fb755c12f8342`  
		Last Modified: Thu, 14 Aug 2025 17:28:31 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8761ecfbd3d5f4577d0427f6692f8727b32e79416868416c486be5473b9e8b`  
		Last Modified: Thu, 14 Aug 2025 17:28:31 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:681562d9ba1813dbbc603309b2d6892e801600f8bebbc79ff4abeff3a76ac79f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3142b6d3fda75b3d9985523564a3d7d40e45991fb5e5e637c3a73a07c95b8ae4`

```dockerfile
```

-	Layers:
	-	`sha256:755fe53608bf0f85d4cd957d4b130cde780dfc04405d767175281a3629b995ca`  
		Last Modified: Thu, 14 Aug 2025 18:49:26 GMT  
		Size: 26.1 KB (26071 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.7` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:0ff9072c4eaa42f21cef806de9ebaa7a611cefc1ae5060d1600e698aadd436eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207720588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f02b4897b9ec9012e2e5140263f7bee3daf48ad52467d391d758751e237421`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:14 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:17 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 30 Jul 2025 05:34:17 GMT
CMD ["/bin/bash"]
# Thu, 14 Aug 2025 16:05:39 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 14 Aug 2025 16:05:39 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
ARG REPO_CHANNEL=stable
# Thu, 14 Aug 2025 16:05:39 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 14 Aug 2025 16:05:39 GMT
ARG VERSION=25.7.4.11
# Thu, 14 Aug 2025 16:05:39 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
ENV LANG=en_US.UTF-8
# Thu, 14 Aug 2025 16:05:39 GMT
ENV TZ=UTC
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 14 Aug 2025 16:05:39 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 14 Aug 2025 16:05:39 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 14 Aug 2025 16:05:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2c5ada98534882e286e4969587be2e4169319891948356df0691eb0dfc0cf1`  
		Last Modified: Thu, 14 Aug 2025 19:36:00 GMT  
		Size: 7.6 MB (7577276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbee40376ed8c772055142ca3b88c92c6dd5ebef0998e194467a07421d00c50`  
		Last Modified: Thu, 14 Aug 2025 20:08:40 GMT  
		Size: 171.9 MB (171914045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f81e9e8e167fab92ae391f856bd24fc60139efb08bdeb826e973c8ee943371`  
		Last Modified: Thu, 14 Aug 2025 19:35:59 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235e71c5f6c35d9286578d8aab323a9ec1f8e1f1158046dfbc794f8104b43b88`  
		Last Modified: Thu, 14 Aug 2025 19:35:59 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32870a365cd24f6d24b0980a8aaf87d05b8d49cddef394c6aee47fc7edf8211d`  
		Last Modified: Thu, 14 Aug 2025 19:35:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa70480277eda6c1ceb38bbd7b8d599ef8b289c0003d5d9a56fe12efc50e371`  
		Last Modified: Thu, 14 Aug 2025 19:35:59 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29505d9e8a9f4453402a96cb19faa4e3d8fdf5d01bf90488f762982948bd6aa5`  
		Last Modified: Thu, 14 Aug 2025 19:35:59 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d0a2627faf4952f98bb6ee0128e3df446b6a462dee024cf9e01b8e28b9cbd016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f8825679b8cb20134bd947613df5f8eecf19664db4a2931fc22b3f461625af8`

```dockerfile
```

-	Layers:
	-	`sha256:525f392b97e6c32e62cd61b273c27ee18766b1ed8b182fe0f3694c990ba14bc3`  
		Last Modified: Thu, 14 Aug 2025 21:49:28 GMT  
		Size: 26.3 KB (26283 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.7-jammy`

```console
$ docker pull clickhouse@sha256:cb508b298560ec995d8ae212df1a9f2a45b6fe52a808d16a649f46c38f32e22c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.7-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:c4bf9ef5c0ba0e82ef2469983af6bee00fcabcde75396f730a077f6fe9e20917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.8 MB (221779604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577e072221ce4b820d7c599d3833d401ca56cbdad732cc02216cab04517d5714`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:32:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:32:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:32:14 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 30 Jul 2025 05:32:14 GMT
CMD ["/bin/bash"]
# Thu, 14 Aug 2025 16:05:39 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 14 Aug 2025 16:05:39 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
ARG REPO_CHANNEL=stable
# Thu, 14 Aug 2025 16:05:39 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 14 Aug 2025 16:05:39 GMT
ARG VERSION=25.7.4.11
# Thu, 14 Aug 2025 16:05:39 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
ENV LANG=en_US.UTF-8
# Thu, 14 Aug 2025 16:05:39 GMT
ENV TZ=UTC
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 14 Aug 2025 16:05:39 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 14 Aug 2025 16:05:39 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 14 Aug 2025 16:05:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2b1ff853e348471606bdabae3dbeca582dc076f0a12400b20b6a0d3eec0e20`  
		Last Modified: Thu, 14 Aug 2025 17:28:33 GMT  
		Size: 7.6 MB (7598470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a491a1d2b5ea4b1ff196b10523f89bde73de85e3634f19dc9d8c9f235c56dbeb`  
		Last Modified: Thu, 14 Aug 2025 18:50:16 GMT  
		Size: 183.8 MB (183774118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7690c20a34e22cf7d5173eee36489a7d9217387d1b6425d41f530d64164fb9c9`  
		Last Modified: Thu, 14 Aug 2025 17:28:31 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d9a2267bb087200f032b91d07eb2993af87cbdc6ea6f1c23e058999f25670d`  
		Last Modified: Thu, 14 Aug 2025 17:28:31 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d41a2fb8dc49d5b2e8f8f7e6592acdd26dd09c2d1ec46a7da5ab63c08e0679`  
		Last Modified: Thu, 14 Aug 2025 17:28:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093a89a665149b53a3d981455e0fdc995ac2ee38effda627a80fb755c12f8342`  
		Last Modified: Thu, 14 Aug 2025 17:28:31 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8761ecfbd3d5f4577d0427f6692f8727b32e79416868416c486be5473b9e8b`  
		Last Modified: Thu, 14 Aug 2025 17:28:31 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:681562d9ba1813dbbc603309b2d6892e801600f8bebbc79ff4abeff3a76ac79f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3142b6d3fda75b3d9985523564a3d7d40e45991fb5e5e637c3a73a07c95b8ae4`

```dockerfile
```

-	Layers:
	-	`sha256:755fe53608bf0f85d4cd957d4b130cde780dfc04405d767175281a3629b995ca`  
		Last Modified: Thu, 14 Aug 2025 18:49:26 GMT  
		Size: 26.1 KB (26071 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.7-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:0ff9072c4eaa42f21cef806de9ebaa7a611cefc1ae5060d1600e698aadd436eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207720588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f02b4897b9ec9012e2e5140263f7bee3daf48ad52467d391d758751e237421`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:14 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:17 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 30 Jul 2025 05:34:17 GMT
CMD ["/bin/bash"]
# Thu, 14 Aug 2025 16:05:39 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 14 Aug 2025 16:05:39 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
ARG REPO_CHANNEL=stable
# Thu, 14 Aug 2025 16:05:39 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 14 Aug 2025 16:05:39 GMT
ARG VERSION=25.7.4.11
# Thu, 14 Aug 2025 16:05:39 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
ENV LANG=en_US.UTF-8
# Thu, 14 Aug 2025 16:05:39 GMT
ENV TZ=UTC
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 14 Aug 2025 16:05:39 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 14 Aug 2025 16:05:39 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 14 Aug 2025 16:05:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2c5ada98534882e286e4969587be2e4169319891948356df0691eb0dfc0cf1`  
		Last Modified: Thu, 14 Aug 2025 19:36:00 GMT  
		Size: 7.6 MB (7577276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbee40376ed8c772055142ca3b88c92c6dd5ebef0998e194467a07421d00c50`  
		Last Modified: Thu, 14 Aug 2025 20:08:40 GMT  
		Size: 171.9 MB (171914045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f81e9e8e167fab92ae391f856bd24fc60139efb08bdeb826e973c8ee943371`  
		Last Modified: Thu, 14 Aug 2025 19:35:59 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235e71c5f6c35d9286578d8aab323a9ec1f8e1f1158046dfbc794f8104b43b88`  
		Last Modified: Thu, 14 Aug 2025 19:35:59 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32870a365cd24f6d24b0980a8aaf87d05b8d49cddef394c6aee47fc7edf8211d`  
		Last Modified: Thu, 14 Aug 2025 19:35:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa70480277eda6c1ceb38bbd7b8d599ef8b289c0003d5d9a56fe12efc50e371`  
		Last Modified: Thu, 14 Aug 2025 19:35:59 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29505d9e8a9f4453402a96cb19faa4e3d8fdf5d01bf90488f762982948bd6aa5`  
		Last Modified: Thu, 14 Aug 2025 19:35:59 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d0a2627faf4952f98bb6ee0128e3df446b6a462dee024cf9e01b8e28b9cbd016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f8825679b8cb20134bd947613df5f8eecf19664db4a2931fc22b3f461625af8`

```dockerfile
```

-	Layers:
	-	`sha256:525f392b97e6c32e62cd61b273c27ee18766b1ed8b182fe0f3694c990ba14bc3`  
		Last Modified: Thu, 14 Aug 2025 21:49:28 GMT  
		Size: 26.3 KB (26283 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.7.4`

```console
$ docker pull clickhouse@sha256:cb508b298560ec995d8ae212df1a9f2a45b6fe52a808d16a649f46c38f32e22c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.7.4` - linux; amd64

```console
$ docker pull clickhouse@sha256:c4bf9ef5c0ba0e82ef2469983af6bee00fcabcde75396f730a077f6fe9e20917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.8 MB (221779604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577e072221ce4b820d7c599d3833d401ca56cbdad732cc02216cab04517d5714`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:32:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:32:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:32:14 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 30 Jul 2025 05:32:14 GMT
CMD ["/bin/bash"]
# Thu, 14 Aug 2025 16:05:39 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 14 Aug 2025 16:05:39 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
ARG REPO_CHANNEL=stable
# Thu, 14 Aug 2025 16:05:39 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 14 Aug 2025 16:05:39 GMT
ARG VERSION=25.7.4.11
# Thu, 14 Aug 2025 16:05:39 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
ENV LANG=en_US.UTF-8
# Thu, 14 Aug 2025 16:05:39 GMT
ENV TZ=UTC
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 14 Aug 2025 16:05:39 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 14 Aug 2025 16:05:39 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 14 Aug 2025 16:05:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2b1ff853e348471606bdabae3dbeca582dc076f0a12400b20b6a0d3eec0e20`  
		Last Modified: Thu, 14 Aug 2025 17:28:33 GMT  
		Size: 7.6 MB (7598470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a491a1d2b5ea4b1ff196b10523f89bde73de85e3634f19dc9d8c9f235c56dbeb`  
		Last Modified: Thu, 14 Aug 2025 18:50:16 GMT  
		Size: 183.8 MB (183774118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7690c20a34e22cf7d5173eee36489a7d9217387d1b6425d41f530d64164fb9c9`  
		Last Modified: Thu, 14 Aug 2025 17:28:31 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d9a2267bb087200f032b91d07eb2993af87cbdc6ea6f1c23e058999f25670d`  
		Last Modified: Thu, 14 Aug 2025 17:28:31 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d41a2fb8dc49d5b2e8f8f7e6592acdd26dd09c2d1ec46a7da5ab63c08e0679`  
		Last Modified: Thu, 14 Aug 2025 17:28:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093a89a665149b53a3d981455e0fdc995ac2ee38effda627a80fb755c12f8342`  
		Last Modified: Thu, 14 Aug 2025 17:28:31 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8761ecfbd3d5f4577d0427f6692f8727b32e79416868416c486be5473b9e8b`  
		Last Modified: Thu, 14 Aug 2025 17:28:31 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:681562d9ba1813dbbc603309b2d6892e801600f8bebbc79ff4abeff3a76ac79f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3142b6d3fda75b3d9985523564a3d7d40e45991fb5e5e637c3a73a07c95b8ae4`

```dockerfile
```

-	Layers:
	-	`sha256:755fe53608bf0f85d4cd957d4b130cde780dfc04405d767175281a3629b995ca`  
		Last Modified: Thu, 14 Aug 2025 18:49:26 GMT  
		Size: 26.1 KB (26071 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.7.4` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:0ff9072c4eaa42f21cef806de9ebaa7a611cefc1ae5060d1600e698aadd436eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207720588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f02b4897b9ec9012e2e5140263f7bee3daf48ad52467d391d758751e237421`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:14 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:17 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 30 Jul 2025 05:34:17 GMT
CMD ["/bin/bash"]
# Thu, 14 Aug 2025 16:05:39 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 14 Aug 2025 16:05:39 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
ARG REPO_CHANNEL=stable
# Thu, 14 Aug 2025 16:05:39 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 14 Aug 2025 16:05:39 GMT
ARG VERSION=25.7.4.11
# Thu, 14 Aug 2025 16:05:39 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
ENV LANG=en_US.UTF-8
# Thu, 14 Aug 2025 16:05:39 GMT
ENV TZ=UTC
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 14 Aug 2025 16:05:39 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 14 Aug 2025 16:05:39 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 14 Aug 2025 16:05:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2c5ada98534882e286e4969587be2e4169319891948356df0691eb0dfc0cf1`  
		Last Modified: Thu, 14 Aug 2025 19:36:00 GMT  
		Size: 7.6 MB (7577276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbee40376ed8c772055142ca3b88c92c6dd5ebef0998e194467a07421d00c50`  
		Last Modified: Thu, 14 Aug 2025 20:08:40 GMT  
		Size: 171.9 MB (171914045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f81e9e8e167fab92ae391f856bd24fc60139efb08bdeb826e973c8ee943371`  
		Last Modified: Thu, 14 Aug 2025 19:35:59 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235e71c5f6c35d9286578d8aab323a9ec1f8e1f1158046dfbc794f8104b43b88`  
		Last Modified: Thu, 14 Aug 2025 19:35:59 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32870a365cd24f6d24b0980a8aaf87d05b8d49cddef394c6aee47fc7edf8211d`  
		Last Modified: Thu, 14 Aug 2025 19:35:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa70480277eda6c1ceb38bbd7b8d599ef8b289c0003d5d9a56fe12efc50e371`  
		Last Modified: Thu, 14 Aug 2025 19:35:59 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29505d9e8a9f4453402a96cb19faa4e3d8fdf5d01bf90488f762982948bd6aa5`  
		Last Modified: Thu, 14 Aug 2025 19:35:59 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d0a2627faf4952f98bb6ee0128e3df446b6a462dee024cf9e01b8e28b9cbd016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f8825679b8cb20134bd947613df5f8eecf19664db4a2931fc22b3f461625af8`

```dockerfile
```

-	Layers:
	-	`sha256:525f392b97e6c32e62cd61b273c27ee18766b1ed8b182fe0f3694c990ba14bc3`  
		Last Modified: Thu, 14 Aug 2025 21:49:28 GMT  
		Size: 26.3 KB (26283 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.7.4-jammy`

```console
$ docker pull clickhouse@sha256:cb508b298560ec995d8ae212df1a9f2a45b6fe52a808d16a649f46c38f32e22c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.7.4-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:c4bf9ef5c0ba0e82ef2469983af6bee00fcabcde75396f730a077f6fe9e20917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.8 MB (221779604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577e072221ce4b820d7c599d3833d401ca56cbdad732cc02216cab04517d5714`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:32:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:32:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:32:14 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 30 Jul 2025 05:32:14 GMT
CMD ["/bin/bash"]
# Thu, 14 Aug 2025 16:05:39 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 14 Aug 2025 16:05:39 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
ARG REPO_CHANNEL=stable
# Thu, 14 Aug 2025 16:05:39 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 14 Aug 2025 16:05:39 GMT
ARG VERSION=25.7.4.11
# Thu, 14 Aug 2025 16:05:39 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
ENV LANG=en_US.UTF-8
# Thu, 14 Aug 2025 16:05:39 GMT
ENV TZ=UTC
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 14 Aug 2025 16:05:39 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 14 Aug 2025 16:05:39 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 14 Aug 2025 16:05:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2b1ff853e348471606bdabae3dbeca582dc076f0a12400b20b6a0d3eec0e20`  
		Last Modified: Thu, 14 Aug 2025 17:28:33 GMT  
		Size: 7.6 MB (7598470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a491a1d2b5ea4b1ff196b10523f89bde73de85e3634f19dc9d8c9f235c56dbeb`  
		Last Modified: Thu, 14 Aug 2025 18:50:16 GMT  
		Size: 183.8 MB (183774118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7690c20a34e22cf7d5173eee36489a7d9217387d1b6425d41f530d64164fb9c9`  
		Last Modified: Thu, 14 Aug 2025 17:28:31 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d9a2267bb087200f032b91d07eb2993af87cbdc6ea6f1c23e058999f25670d`  
		Last Modified: Thu, 14 Aug 2025 17:28:31 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d41a2fb8dc49d5b2e8f8f7e6592acdd26dd09c2d1ec46a7da5ab63c08e0679`  
		Last Modified: Thu, 14 Aug 2025 17:28:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093a89a665149b53a3d981455e0fdc995ac2ee38effda627a80fb755c12f8342`  
		Last Modified: Thu, 14 Aug 2025 17:28:31 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8761ecfbd3d5f4577d0427f6692f8727b32e79416868416c486be5473b9e8b`  
		Last Modified: Thu, 14 Aug 2025 17:28:31 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:681562d9ba1813dbbc603309b2d6892e801600f8bebbc79ff4abeff3a76ac79f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3142b6d3fda75b3d9985523564a3d7d40e45991fb5e5e637c3a73a07c95b8ae4`

```dockerfile
```

-	Layers:
	-	`sha256:755fe53608bf0f85d4cd957d4b130cde780dfc04405d767175281a3629b995ca`  
		Last Modified: Thu, 14 Aug 2025 18:49:26 GMT  
		Size: 26.1 KB (26071 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.7.4-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:0ff9072c4eaa42f21cef806de9ebaa7a611cefc1ae5060d1600e698aadd436eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207720588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f02b4897b9ec9012e2e5140263f7bee3daf48ad52467d391d758751e237421`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:14 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:17 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 30 Jul 2025 05:34:17 GMT
CMD ["/bin/bash"]
# Thu, 14 Aug 2025 16:05:39 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 14 Aug 2025 16:05:39 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
ARG REPO_CHANNEL=stable
# Thu, 14 Aug 2025 16:05:39 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 14 Aug 2025 16:05:39 GMT
ARG VERSION=25.7.4.11
# Thu, 14 Aug 2025 16:05:39 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
ENV LANG=en_US.UTF-8
# Thu, 14 Aug 2025 16:05:39 GMT
ENV TZ=UTC
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 14 Aug 2025 16:05:39 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 14 Aug 2025 16:05:39 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 14 Aug 2025 16:05:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2c5ada98534882e286e4969587be2e4169319891948356df0691eb0dfc0cf1`  
		Last Modified: Thu, 14 Aug 2025 19:36:00 GMT  
		Size: 7.6 MB (7577276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbee40376ed8c772055142ca3b88c92c6dd5ebef0998e194467a07421d00c50`  
		Last Modified: Thu, 14 Aug 2025 20:08:40 GMT  
		Size: 171.9 MB (171914045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f81e9e8e167fab92ae391f856bd24fc60139efb08bdeb826e973c8ee943371`  
		Last Modified: Thu, 14 Aug 2025 19:35:59 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235e71c5f6c35d9286578d8aab323a9ec1f8e1f1158046dfbc794f8104b43b88`  
		Last Modified: Thu, 14 Aug 2025 19:35:59 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32870a365cd24f6d24b0980a8aaf87d05b8d49cddef394c6aee47fc7edf8211d`  
		Last Modified: Thu, 14 Aug 2025 19:35:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa70480277eda6c1ceb38bbd7b8d599ef8b289c0003d5d9a56fe12efc50e371`  
		Last Modified: Thu, 14 Aug 2025 19:35:59 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29505d9e8a9f4453402a96cb19faa4e3d8fdf5d01bf90488f762982948bd6aa5`  
		Last Modified: Thu, 14 Aug 2025 19:35:59 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d0a2627faf4952f98bb6ee0128e3df446b6a462dee024cf9e01b8e28b9cbd016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f8825679b8cb20134bd947613df5f8eecf19664db4a2931fc22b3f461625af8`

```dockerfile
```

-	Layers:
	-	`sha256:525f392b97e6c32e62cd61b273c27ee18766b1ed8b182fe0f3694c990ba14bc3`  
		Last Modified: Thu, 14 Aug 2025 21:49:28 GMT  
		Size: 26.3 KB (26283 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.7.4.11`

```console
$ docker pull clickhouse@sha256:cb508b298560ec995d8ae212df1a9f2a45b6fe52a808d16a649f46c38f32e22c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.7.4.11` - linux; amd64

```console
$ docker pull clickhouse@sha256:c4bf9ef5c0ba0e82ef2469983af6bee00fcabcde75396f730a077f6fe9e20917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.8 MB (221779604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577e072221ce4b820d7c599d3833d401ca56cbdad732cc02216cab04517d5714`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:32:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:32:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:32:14 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 30 Jul 2025 05:32:14 GMT
CMD ["/bin/bash"]
# Thu, 14 Aug 2025 16:05:39 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 14 Aug 2025 16:05:39 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
ARG REPO_CHANNEL=stable
# Thu, 14 Aug 2025 16:05:39 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 14 Aug 2025 16:05:39 GMT
ARG VERSION=25.7.4.11
# Thu, 14 Aug 2025 16:05:39 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
ENV LANG=en_US.UTF-8
# Thu, 14 Aug 2025 16:05:39 GMT
ENV TZ=UTC
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 14 Aug 2025 16:05:39 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 14 Aug 2025 16:05:39 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 14 Aug 2025 16:05:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2b1ff853e348471606bdabae3dbeca582dc076f0a12400b20b6a0d3eec0e20`  
		Last Modified: Thu, 14 Aug 2025 17:28:33 GMT  
		Size: 7.6 MB (7598470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a491a1d2b5ea4b1ff196b10523f89bde73de85e3634f19dc9d8c9f235c56dbeb`  
		Last Modified: Thu, 14 Aug 2025 18:50:16 GMT  
		Size: 183.8 MB (183774118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7690c20a34e22cf7d5173eee36489a7d9217387d1b6425d41f530d64164fb9c9`  
		Last Modified: Thu, 14 Aug 2025 17:28:31 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d9a2267bb087200f032b91d07eb2993af87cbdc6ea6f1c23e058999f25670d`  
		Last Modified: Thu, 14 Aug 2025 17:28:31 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d41a2fb8dc49d5b2e8f8f7e6592acdd26dd09c2d1ec46a7da5ab63c08e0679`  
		Last Modified: Thu, 14 Aug 2025 17:28:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093a89a665149b53a3d981455e0fdc995ac2ee38effda627a80fb755c12f8342`  
		Last Modified: Thu, 14 Aug 2025 17:28:31 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8761ecfbd3d5f4577d0427f6692f8727b32e79416868416c486be5473b9e8b`  
		Last Modified: Thu, 14 Aug 2025 17:28:31 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.4.11` - unknown; unknown

```console
$ docker pull clickhouse@sha256:681562d9ba1813dbbc603309b2d6892e801600f8bebbc79ff4abeff3a76ac79f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3142b6d3fda75b3d9985523564a3d7d40e45991fb5e5e637c3a73a07c95b8ae4`

```dockerfile
```

-	Layers:
	-	`sha256:755fe53608bf0f85d4cd957d4b130cde780dfc04405d767175281a3629b995ca`  
		Last Modified: Thu, 14 Aug 2025 18:49:26 GMT  
		Size: 26.1 KB (26071 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.7.4.11` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:0ff9072c4eaa42f21cef806de9ebaa7a611cefc1ae5060d1600e698aadd436eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207720588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f02b4897b9ec9012e2e5140263f7bee3daf48ad52467d391d758751e237421`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:14 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:17 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 30 Jul 2025 05:34:17 GMT
CMD ["/bin/bash"]
# Thu, 14 Aug 2025 16:05:39 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 14 Aug 2025 16:05:39 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
ARG REPO_CHANNEL=stable
# Thu, 14 Aug 2025 16:05:39 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 14 Aug 2025 16:05:39 GMT
ARG VERSION=25.7.4.11
# Thu, 14 Aug 2025 16:05:39 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
ENV LANG=en_US.UTF-8
# Thu, 14 Aug 2025 16:05:39 GMT
ENV TZ=UTC
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 14 Aug 2025 16:05:39 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 14 Aug 2025 16:05:39 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 14 Aug 2025 16:05:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2c5ada98534882e286e4969587be2e4169319891948356df0691eb0dfc0cf1`  
		Last Modified: Thu, 14 Aug 2025 19:36:00 GMT  
		Size: 7.6 MB (7577276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbee40376ed8c772055142ca3b88c92c6dd5ebef0998e194467a07421d00c50`  
		Last Modified: Thu, 14 Aug 2025 20:08:40 GMT  
		Size: 171.9 MB (171914045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f81e9e8e167fab92ae391f856bd24fc60139efb08bdeb826e973c8ee943371`  
		Last Modified: Thu, 14 Aug 2025 19:35:59 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235e71c5f6c35d9286578d8aab323a9ec1f8e1f1158046dfbc794f8104b43b88`  
		Last Modified: Thu, 14 Aug 2025 19:35:59 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32870a365cd24f6d24b0980a8aaf87d05b8d49cddef394c6aee47fc7edf8211d`  
		Last Modified: Thu, 14 Aug 2025 19:35:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa70480277eda6c1ceb38bbd7b8d599ef8b289c0003d5d9a56fe12efc50e371`  
		Last Modified: Thu, 14 Aug 2025 19:35:59 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29505d9e8a9f4453402a96cb19faa4e3d8fdf5d01bf90488f762982948bd6aa5`  
		Last Modified: Thu, 14 Aug 2025 19:35:59 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.4.11` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d0a2627faf4952f98bb6ee0128e3df446b6a462dee024cf9e01b8e28b9cbd016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f8825679b8cb20134bd947613df5f8eecf19664db4a2931fc22b3f461625af8`

```dockerfile
```

-	Layers:
	-	`sha256:525f392b97e6c32e62cd61b273c27ee18766b1ed8b182fe0f3694c990ba14bc3`  
		Last Modified: Thu, 14 Aug 2025 21:49:28 GMT  
		Size: 26.3 KB (26283 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.7.4.11-jammy`

```console
$ docker pull clickhouse@sha256:cb508b298560ec995d8ae212df1a9f2a45b6fe52a808d16a649f46c38f32e22c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.7.4.11-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:c4bf9ef5c0ba0e82ef2469983af6bee00fcabcde75396f730a077f6fe9e20917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.8 MB (221779604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577e072221ce4b820d7c599d3833d401ca56cbdad732cc02216cab04517d5714`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:32:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:32:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:32:14 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 30 Jul 2025 05:32:14 GMT
CMD ["/bin/bash"]
# Thu, 14 Aug 2025 16:05:39 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 14 Aug 2025 16:05:39 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
ARG REPO_CHANNEL=stable
# Thu, 14 Aug 2025 16:05:39 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 14 Aug 2025 16:05:39 GMT
ARG VERSION=25.7.4.11
# Thu, 14 Aug 2025 16:05:39 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
ENV LANG=en_US.UTF-8
# Thu, 14 Aug 2025 16:05:39 GMT
ENV TZ=UTC
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 14 Aug 2025 16:05:39 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 14 Aug 2025 16:05:39 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 14 Aug 2025 16:05:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2b1ff853e348471606bdabae3dbeca582dc076f0a12400b20b6a0d3eec0e20`  
		Last Modified: Thu, 14 Aug 2025 17:28:33 GMT  
		Size: 7.6 MB (7598470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a491a1d2b5ea4b1ff196b10523f89bde73de85e3634f19dc9d8c9f235c56dbeb`  
		Last Modified: Thu, 14 Aug 2025 18:50:16 GMT  
		Size: 183.8 MB (183774118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7690c20a34e22cf7d5173eee36489a7d9217387d1b6425d41f530d64164fb9c9`  
		Last Modified: Thu, 14 Aug 2025 17:28:31 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d9a2267bb087200f032b91d07eb2993af87cbdc6ea6f1c23e058999f25670d`  
		Last Modified: Thu, 14 Aug 2025 17:28:31 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d41a2fb8dc49d5b2e8f8f7e6592acdd26dd09c2d1ec46a7da5ab63c08e0679`  
		Last Modified: Thu, 14 Aug 2025 17:28:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093a89a665149b53a3d981455e0fdc995ac2ee38effda627a80fb755c12f8342`  
		Last Modified: Thu, 14 Aug 2025 17:28:31 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8761ecfbd3d5f4577d0427f6692f8727b32e79416868416c486be5473b9e8b`  
		Last Modified: Thu, 14 Aug 2025 17:28:31 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.4.11-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:681562d9ba1813dbbc603309b2d6892e801600f8bebbc79ff4abeff3a76ac79f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3142b6d3fda75b3d9985523564a3d7d40e45991fb5e5e637c3a73a07c95b8ae4`

```dockerfile
```

-	Layers:
	-	`sha256:755fe53608bf0f85d4cd957d4b130cde780dfc04405d767175281a3629b995ca`  
		Last Modified: Thu, 14 Aug 2025 18:49:26 GMT  
		Size: 26.1 KB (26071 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.7.4.11-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:0ff9072c4eaa42f21cef806de9ebaa7a611cefc1ae5060d1600e698aadd436eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207720588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f02b4897b9ec9012e2e5140263f7bee3daf48ad52467d391d758751e237421`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:14 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:17 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 30 Jul 2025 05:34:17 GMT
CMD ["/bin/bash"]
# Thu, 14 Aug 2025 16:05:39 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 14 Aug 2025 16:05:39 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
ARG REPO_CHANNEL=stable
# Thu, 14 Aug 2025 16:05:39 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 14 Aug 2025 16:05:39 GMT
ARG VERSION=25.7.4.11
# Thu, 14 Aug 2025 16:05:39 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
ENV LANG=en_US.UTF-8
# Thu, 14 Aug 2025 16:05:39 GMT
ENV TZ=UTC
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 14 Aug 2025 16:05:39 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 14 Aug 2025 16:05:39 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 14 Aug 2025 16:05:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2c5ada98534882e286e4969587be2e4169319891948356df0691eb0dfc0cf1`  
		Last Modified: Thu, 14 Aug 2025 19:36:00 GMT  
		Size: 7.6 MB (7577276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbee40376ed8c772055142ca3b88c92c6dd5ebef0998e194467a07421d00c50`  
		Last Modified: Thu, 14 Aug 2025 20:08:40 GMT  
		Size: 171.9 MB (171914045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f81e9e8e167fab92ae391f856bd24fc60139efb08bdeb826e973c8ee943371`  
		Last Modified: Thu, 14 Aug 2025 19:35:59 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235e71c5f6c35d9286578d8aab323a9ec1f8e1f1158046dfbc794f8104b43b88`  
		Last Modified: Thu, 14 Aug 2025 19:35:59 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32870a365cd24f6d24b0980a8aaf87d05b8d49cddef394c6aee47fc7edf8211d`  
		Last Modified: Thu, 14 Aug 2025 19:35:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa70480277eda6c1ceb38bbd7b8d599ef8b289c0003d5d9a56fe12efc50e371`  
		Last Modified: Thu, 14 Aug 2025 19:35:59 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29505d9e8a9f4453402a96cb19faa4e3d8fdf5d01bf90488f762982948bd6aa5`  
		Last Modified: Thu, 14 Aug 2025 19:35:59 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.4.11-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d0a2627faf4952f98bb6ee0128e3df446b6a462dee024cf9e01b8e28b9cbd016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f8825679b8cb20134bd947613df5f8eecf19664db4a2931fc22b3f461625af8`

```dockerfile
```

-	Layers:
	-	`sha256:525f392b97e6c32e62cd61b273c27ee18766b1ed8b182fe0f3694c990ba14bc3`  
		Last Modified: Thu, 14 Aug 2025 21:49:28 GMT  
		Size: 26.3 KB (26283 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:jammy`

```console
$ docker pull clickhouse@sha256:cb508b298560ec995d8ae212df1a9f2a45b6fe52a808d16a649f46c38f32e22c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:c4bf9ef5c0ba0e82ef2469983af6bee00fcabcde75396f730a077f6fe9e20917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.8 MB (221779604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577e072221ce4b820d7c599d3833d401ca56cbdad732cc02216cab04517d5714`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:32:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:32:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:32:14 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 30 Jul 2025 05:32:14 GMT
CMD ["/bin/bash"]
# Thu, 14 Aug 2025 16:05:39 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 14 Aug 2025 16:05:39 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
ARG REPO_CHANNEL=stable
# Thu, 14 Aug 2025 16:05:39 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 14 Aug 2025 16:05:39 GMT
ARG VERSION=25.7.4.11
# Thu, 14 Aug 2025 16:05:39 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
ENV LANG=en_US.UTF-8
# Thu, 14 Aug 2025 16:05:39 GMT
ENV TZ=UTC
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 14 Aug 2025 16:05:39 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 14 Aug 2025 16:05:39 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 14 Aug 2025 16:05:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2b1ff853e348471606bdabae3dbeca582dc076f0a12400b20b6a0d3eec0e20`  
		Last Modified: Thu, 14 Aug 2025 17:28:33 GMT  
		Size: 7.6 MB (7598470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a491a1d2b5ea4b1ff196b10523f89bde73de85e3634f19dc9d8c9f235c56dbeb`  
		Last Modified: Thu, 14 Aug 2025 18:50:16 GMT  
		Size: 183.8 MB (183774118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7690c20a34e22cf7d5173eee36489a7d9217387d1b6425d41f530d64164fb9c9`  
		Last Modified: Thu, 14 Aug 2025 17:28:31 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d9a2267bb087200f032b91d07eb2993af87cbdc6ea6f1c23e058999f25670d`  
		Last Modified: Thu, 14 Aug 2025 17:28:31 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d41a2fb8dc49d5b2e8f8f7e6592acdd26dd09c2d1ec46a7da5ab63c08e0679`  
		Last Modified: Thu, 14 Aug 2025 17:28:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093a89a665149b53a3d981455e0fdc995ac2ee38effda627a80fb755c12f8342`  
		Last Modified: Thu, 14 Aug 2025 17:28:31 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8761ecfbd3d5f4577d0427f6692f8727b32e79416868416c486be5473b9e8b`  
		Last Modified: Thu, 14 Aug 2025 17:28:31 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:681562d9ba1813dbbc603309b2d6892e801600f8bebbc79ff4abeff3a76ac79f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3142b6d3fda75b3d9985523564a3d7d40e45991fb5e5e637c3a73a07c95b8ae4`

```dockerfile
```

-	Layers:
	-	`sha256:755fe53608bf0f85d4cd957d4b130cde780dfc04405d767175281a3629b995ca`  
		Last Modified: Thu, 14 Aug 2025 18:49:26 GMT  
		Size: 26.1 KB (26071 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:0ff9072c4eaa42f21cef806de9ebaa7a611cefc1ae5060d1600e698aadd436eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207720588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f02b4897b9ec9012e2e5140263f7bee3daf48ad52467d391d758751e237421`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:14 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:17 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 30 Jul 2025 05:34:17 GMT
CMD ["/bin/bash"]
# Thu, 14 Aug 2025 16:05:39 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 14 Aug 2025 16:05:39 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
ARG REPO_CHANNEL=stable
# Thu, 14 Aug 2025 16:05:39 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 14 Aug 2025 16:05:39 GMT
ARG VERSION=25.7.4.11
# Thu, 14 Aug 2025 16:05:39 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
ENV LANG=en_US.UTF-8
# Thu, 14 Aug 2025 16:05:39 GMT
ENV TZ=UTC
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 14 Aug 2025 16:05:39 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 14 Aug 2025 16:05:39 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 14 Aug 2025 16:05:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2c5ada98534882e286e4969587be2e4169319891948356df0691eb0dfc0cf1`  
		Last Modified: Thu, 14 Aug 2025 19:36:00 GMT  
		Size: 7.6 MB (7577276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbee40376ed8c772055142ca3b88c92c6dd5ebef0998e194467a07421d00c50`  
		Last Modified: Thu, 14 Aug 2025 20:08:40 GMT  
		Size: 171.9 MB (171914045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f81e9e8e167fab92ae391f856bd24fc60139efb08bdeb826e973c8ee943371`  
		Last Modified: Thu, 14 Aug 2025 19:35:59 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235e71c5f6c35d9286578d8aab323a9ec1f8e1f1158046dfbc794f8104b43b88`  
		Last Modified: Thu, 14 Aug 2025 19:35:59 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32870a365cd24f6d24b0980a8aaf87d05b8d49cddef394c6aee47fc7edf8211d`  
		Last Modified: Thu, 14 Aug 2025 19:35:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa70480277eda6c1ceb38bbd7b8d599ef8b289c0003d5d9a56fe12efc50e371`  
		Last Modified: Thu, 14 Aug 2025 19:35:59 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29505d9e8a9f4453402a96cb19faa4e3d8fdf5d01bf90488f762982948bd6aa5`  
		Last Modified: Thu, 14 Aug 2025 19:35:59 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d0a2627faf4952f98bb6ee0128e3df446b6a462dee024cf9e01b8e28b9cbd016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f8825679b8cb20134bd947613df5f8eecf19664db4a2931fc22b3f461625af8`

```dockerfile
```

-	Layers:
	-	`sha256:525f392b97e6c32e62cd61b273c27ee18766b1ed8b182fe0f3694c990ba14bc3`  
		Last Modified: Thu, 14 Aug 2025 21:49:28 GMT  
		Size: 26.3 KB (26283 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:cb508b298560ec995d8ae212df1a9f2a45b6fe52a808d16a649f46c38f32e22c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

```console
$ docker pull clickhouse@sha256:c4bf9ef5c0ba0e82ef2469983af6bee00fcabcde75396f730a077f6fe9e20917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.8 MB (221779604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577e072221ce4b820d7c599d3833d401ca56cbdad732cc02216cab04517d5714`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:32:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:32:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:32:14 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 30 Jul 2025 05:32:14 GMT
CMD ["/bin/bash"]
# Thu, 14 Aug 2025 16:05:39 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 14 Aug 2025 16:05:39 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
ARG REPO_CHANNEL=stable
# Thu, 14 Aug 2025 16:05:39 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 14 Aug 2025 16:05:39 GMT
ARG VERSION=25.7.4.11
# Thu, 14 Aug 2025 16:05:39 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
ENV LANG=en_US.UTF-8
# Thu, 14 Aug 2025 16:05:39 GMT
ENV TZ=UTC
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 14 Aug 2025 16:05:39 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 14 Aug 2025 16:05:39 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 14 Aug 2025 16:05:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2b1ff853e348471606bdabae3dbeca582dc076f0a12400b20b6a0d3eec0e20`  
		Last Modified: Thu, 14 Aug 2025 17:28:33 GMT  
		Size: 7.6 MB (7598470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a491a1d2b5ea4b1ff196b10523f89bde73de85e3634f19dc9d8c9f235c56dbeb`  
		Last Modified: Thu, 14 Aug 2025 18:50:16 GMT  
		Size: 183.8 MB (183774118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7690c20a34e22cf7d5173eee36489a7d9217387d1b6425d41f530d64164fb9c9`  
		Last Modified: Thu, 14 Aug 2025 17:28:31 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d9a2267bb087200f032b91d07eb2993af87cbdc6ea6f1c23e058999f25670d`  
		Last Modified: Thu, 14 Aug 2025 17:28:31 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d41a2fb8dc49d5b2e8f8f7e6592acdd26dd09c2d1ec46a7da5ab63c08e0679`  
		Last Modified: Thu, 14 Aug 2025 17:28:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093a89a665149b53a3d981455e0fdc995ac2ee38effda627a80fb755c12f8342`  
		Last Modified: Thu, 14 Aug 2025 17:28:31 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8761ecfbd3d5f4577d0427f6692f8727b32e79416868416c486be5473b9e8b`  
		Last Modified: Thu, 14 Aug 2025 17:28:31 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:681562d9ba1813dbbc603309b2d6892e801600f8bebbc79ff4abeff3a76ac79f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3142b6d3fda75b3d9985523564a3d7d40e45991fb5e5e637c3a73a07c95b8ae4`

```dockerfile
```

-	Layers:
	-	`sha256:755fe53608bf0f85d4cd957d4b130cde780dfc04405d767175281a3629b995ca`  
		Last Modified: Thu, 14 Aug 2025 18:49:26 GMT  
		Size: 26.1 KB (26071 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:0ff9072c4eaa42f21cef806de9ebaa7a611cefc1ae5060d1600e698aadd436eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207720588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f02b4897b9ec9012e2e5140263f7bee3daf48ad52467d391d758751e237421`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:14 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:17 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 30 Jul 2025 05:34:17 GMT
CMD ["/bin/bash"]
# Thu, 14 Aug 2025 16:05:39 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 14 Aug 2025 16:05:39 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
ARG REPO_CHANNEL=stable
# Thu, 14 Aug 2025 16:05:39 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 14 Aug 2025 16:05:39 GMT
ARG VERSION=25.7.4.11
# Thu, 14 Aug 2025 16:05:39 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
ENV LANG=en_US.UTF-8
# Thu, 14 Aug 2025 16:05:39 GMT
ENV TZ=UTC
# Thu, 14 Aug 2025 16:05:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.4.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 14 Aug 2025 16:05:39 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 14 Aug 2025 16:05:39 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 14 Aug 2025 16:05:39 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 14 Aug 2025 16:05:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2c5ada98534882e286e4969587be2e4169319891948356df0691eb0dfc0cf1`  
		Last Modified: Thu, 14 Aug 2025 19:36:00 GMT  
		Size: 7.6 MB (7577276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbee40376ed8c772055142ca3b88c92c6dd5ebef0998e194467a07421d00c50`  
		Last Modified: Thu, 14 Aug 2025 20:08:40 GMT  
		Size: 171.9 MB (171914045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f81e9e8e167fab92ae391f856bd24fc60139efb08bdeb826e973c8ee943371`  
		Last Modified: Thu, 14 Aug 2025 19:35:59 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235e71c5f6c35d9286578d8aab323a9ec1f8e1f1158046dfbc794f8104b43b88`  
		Last Modified: Thu, 14 Aug 2025 19:35:59 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32870a365cd24f6d24b0980a8aaf87d05b8d49cddef394c6aee47fc7edf8211d`  
		Last Modified: Thu, 14 Aug 2025 19:35:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa70480277eda6c1ceb38bbd7b8d599ef8b289c0003d5d9a56fe12efc50e371`  
		Last Modified: Thu, 14 Aug 2025 19:35:59 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29505d9e8a9f4453402a96cb19faa4e3d8fdf5d01bf90488f762982948bd6aa5`  
		Last Modified: Thu, 14 Aug 2025 19:35:59 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d0a2627faf4952f98bb6ee0128e3df446b6a462dee024cf9e01b8e28b9cbd016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f8825679b8cb20134bd947613df5f8eecf19664db4a2931fc22b3f461625af8`

```dockerfile
```

-	Layers:
	-	`sha256:525f392b97e6c32e62cd61b273c27ee18766b1ed8b182fe0f3694c990ba14bc3`  
		Last Modified: Thu, 14 Aug 2025 21:49:28 GMT  
		Size: 26.3 KB (26283 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts`

```console
$ docker pull clickhouse@sha256:b2026b4defbdd247c6978d9f77c887340b2aa5d036a4856089ddaa49f95d5e28
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts` - linux; amd64

```console
$ docker pull clickhouse@sha256:636ce3aa345c93482ba2f51d9737721e89a96f44ff0fd913ff400b18d50bd125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.4 MB (205432539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0861ca60e97c4a4911b5ab03e22d521e79beaf99aeba2542fca8a4ae16f5fab7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:32:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:32:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:32:14 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 30 Jul 2025 05:32:14 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:05:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 07 Aug 2025 16:05:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPO_CHANNEL=stable
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 07 Aug 2025 16:05:41 GMT
ARG VERSION=25.3.6.56
# Thu, 07 Aug 2025 16:05:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 16:05:41 GMT
ENV TZ=UTC
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 07 Aug 2025 16:05:41 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 07 Aug 2025 16:05:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 07 Aug 2025 16:05:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137c85da229929a08f72e0cfa17aaec9403f65a3da5881d8597fbcc91cbdd1f2`  
		Last Modified: Tue, 12 Aug 2025 17:24:15 GMT  
		Size: 7.2 MB (7151687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f0f4d76285565776b73c89d420a55567190d02146e95bb55b2a043b6113a8e`  
		Last Modified: Tue, 12 Aug 2025 18:49:54 GMT  
		Size: 167.9 MB (167873615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ef3061e624958aab31c4e5978a0f61eeda5c05c194bd11c4b704d446fa1097`  
		Last Modified: Tue, 12 Aug 2025 17:24:11 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1b24d7e886d2fbd34ded6bb6650b314782d91b5b74b7b208959f51a09b95b1`  
		Last Modified: Tue, 12 Aug 2025 17:24:12 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384bebcfcced27c8cc253e9a927dadea48eccc047b126656c50f40eb610959c6`  
		Last Modified: Tue, 12 Aug 2025 17:24:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55573752dbede5172c8eedea40d806a0622935e82410289e57b4b9394f4f147`  
		Last Modified: Tue, 12 Aug 2025 17:24:12 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb76cd2113121f91e3ab02f114cf6252db5f9292d55c9407f5cc537cf6ba237`  
		Last Modified: Tue, 12 Aug 2025 17:24:13 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:82eb1fb6bde6c4de016b438a56cb7bd716aaa4629cb957b74e3c93cfe06eb9e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4596f7361fd8a3e99e4345bb0763c6f63d502e4254aaa3c4fe5706b3c9f27f25`

```dockerfile
```

-	Layers:
	-	`sha256:4fad8a220e2457601f329591a0485ba91179ff6374b02e0696775d095f5c25f2`  
		Last Modified: Tue, 12 Aug 2025 18:49:21 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:cf502240469bccc854c9b3fc67e5ca54ec37a3f5ef6df20056f0f8323d42b3db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192912365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7be4817e5d79d7aedd4983a60758916bd520dd58e258225fb62ec07bc1bed9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:14 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:17 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 30 Jul 2025 05:34:17 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:05:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 07 Aug 2025 16:05:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPO_CHANNEL=stable
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 07 Aug 2025 16:05:41 GMT
ARG VERSION=25.3.6.56
# Thu, 07 Aug 2025 16:05:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 16:05:41 GMT
ENV TZ=UTC
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 07 Aug 2025 16:05:41 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 07 Aug 2025 16:05:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 07 Aug 2025 16:05:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e6e0b617b9c63d680a3dee014408e3c901d247257c08f588eb01fd8ab0b0cf`  
		Last Modified: Tue, 12 Aug 2025 17:35:42 GMT  
		Size: 7.1 MB (7127960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa41208f438b689eaf456b07fbfecabf48676b2b7cef271faca1a76e41f0a463`  
		Last Modified: Tue, 12 Aug 2025 18:49:50 GMT  
		Size: 157.6 MB (157554909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa40645d38b2be7a1826a8c5ce4f1672e59b4119987c880641938a181bd9ed83`  
		Last Modified: Tue, 12 Aug 2025 17:35:41 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7826c6a09a2f6eec6e397f6a19aad16112f8387aa6f876f40771f63b54fb2fa`  
		Last Modified: Tue, 12 Aug 2025 17:35:42 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a378edc92a579bbd440d0c7e6b2aa53b121a721e0da76a3d251ba47ad3dd4aa`  
		Last Modified: Tue, 12 Aug 2025 17:35:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9dd5e8c5fe95a063fd9c0b05940f9c20ad696c10e01033a27283229ecc5780`  
		Last Modified: Tue, 12 Aug 2025 17:35:41 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbf8d069153cecb84f87a8a394bf119304fb4b4e8fda23b32c4d191b44c8b55`  
		Last Modified: Tue, 12 Aug 2025 17:35:42 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a71c6061a09f252dac7c36c94adc81c75a467329095ed90329b2bcddadb37a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f25d0f988a9bcd5c1eff72678102496338ffcec6798ffacadbc579eac789164a`

```dockerfile
```

-	Layers:
	-	`sha256:4586c050a3d62b4912f0aff1149618f3e8e444bbc8955c0a08f13d942d02f7d7`  
		Last Modified: Tue, 12 Aug 2025 18:49:25 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts-jammy`

```console
$ docker pull clickhouse@sha256:b2026b4defbdd247c6978d9f77c887340b2aa5d036a4856089ddaa49f95d5e28
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:636ce3aa345c93482ba2f51d9737721e89a96f44ff0fd913ff400b18d50bd125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.4 MB (205432539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0861ca60e97c4a4911b5ab03e22d521e79beaf99aeba2542fca8a4ae16f5fab7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:32:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:32:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:32:14 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 30 Jul 2025 05:32:14 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:05:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 07 Aug 2025 16:05:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPO_CHANNEL=stable
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 07 Aug 2025 16:05:41 GMT
ARG VERSION=25.3.6.56
# Thu, 07 Aug 2025 16:05:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 16:05:41 GMT
ENV TZ=UTC
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 07 Aug 2025 16:05:41 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 07 Aug 2025 16:05:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 07 Aug 2025 16:05:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137c85da229929a08f72e0cfa17aaec9403f65a3da5881d8597fbcc91cbdd1f2`  
		Last Modified: Tue, 12 Aug 2025 17:24:15 GMT  
		Size: 7.2 MB (7151687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f0f4d76285565776b73c89d420a55567190d02146e95bb55b2a043b6113a8e`  
		Last Modified: Tue, 12 Aug 2025 18:49:54 GMT  
		Size: 167.9 MB (167873615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ef3061e624958aab31c4e5978a0f61eeda5c05c194bd11c4b704d446fa1097`  
		Last Modified: Tue, 12 Aug 2025 17:24:11 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1b24d7e886d2fbd34ded6bb6650b314782d91b5b74b7b208959f51a09b95b1`  
		Last Modified: Tue, 12 Aug 2025 17:24:12 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384bebcfcced27c8cc253e9a927dadea48eccc047b126656c50f40eb610959c6`  
		Last Modified: Tue, 12 Aug 2025 17:24:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55573752dbede5172c8eedea40d806a0622935e82410289e57b4b9394f4f147`  
		Last Modified: Tue, 12 Aug 2025 17:24:12 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb76cd2113121f91e3ab02f114cf6252db5f9292d55c9407f5cc537cf6ba237`  
		Last Modified: Tue, 12 Aug 2025 17:24:13 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:82eb1fb6bde6c4de016b438a56cb7bd716aaa4629cb957b74e3c93cfe06eb9e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4596f7361fd8a3e99e4345bb0763c6f63d502e4254aaa3c4fe5706b3c9f27f25`

```dockerfile
```

-	Layers:
	-	`sha256:4fad8a220e2457601f329591a0485ba91179ff6374b02e0696775d095f5c25f2`  
		Last Modified: Tue, 12 Aug 2025 18:49:21 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:cf502240469bccc854c9b3fc67e5ca54ec37a3f5ef6df20056f0f8323d42b3db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192912365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7be4817e5d79d7aedd4983a60758916bd520dd58e258225fb62ec07bc1bed9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:14 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:17 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 30 Jul 2025 05:34:17 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 16:05:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 07 Aug 2025 16:05:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPO_CHANNEL=stable
# Thu, 07 Aug 2025 16:05:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 07 Aug 2025 16:05:41 GMT
ARG VERSION=25.3.6.56
# Thu, 07 Aug 2025 16:05:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 16:05:41 GMT
ENV TZ=UTC
# Thu, 07 Aug 2025 16:05:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 Aug 2025 16:05:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 07 Aug 2025 16:05:41 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 07 Aug 2025 16:05:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 07 Aug 2025 16:05:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e6e0b617b9c63d680a3dee014408e3c901d247257c08f588eb01fd8ab0b0cf`  
		Last Modified: Tue, 12 Aug 2025 17:35:42 GMT  
		Size: 7.1 MB (7127960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa41208f438b689eaf456b07fbfecabf48676b2b7cef271faca1a76e41f0a463`  
		Last Modified: Tue, 12 Aug 2025 18:49:50 GMT  
		Size: 157.6 MB (157554909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa40645d38b2be7a1826a8c5ce4f1672e59b4119987c880641938a181bd9ed83`  
		Last Modified: Tue, 12 Aug 2025 17:35:41 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7826c6a09a2f6eec6e397f6a19aad16112f8387aa6f876f40771f63b54fb2fa`  
		Last Modified: Tue, 12 Aug 2025 17:35:42 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a378edc92a579bbd440d0c7e6b2aa53b121a721e0da76a3d251ba47ad3dd4aa`  
		Last Modified: Tue, 12 Aug 2025 17:35:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9dd5e8c5fe95a063fd9c0b05940f9c20ad696c10e01033a27283229ecc5780`  
		Last Modified: Tue, 12 Aug 2025 17:35:41 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbf8d069153cecb84f87a8a394bf119304fb4b4e8fda23b32c4d191b44c8b55`  
		Last Modified: Tue, 12 Aug 2025 17:35:42 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a71c6061a09f252dac7c36c94adc81c75a467329095ed90329b2bcddadb37a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f25d0f988a9bcd5c1eff72678102496338ffcec6798ffacadbc579eac789164a`

```dockerfile
```

-	Layers:
	-	`sha256:4586c050a3d62b4912f0aff1149618f3e8e444bbc8955c0a08f13d942d02f7d7`  
		Last Modified: Tue, 12 Aug 2025 18:49:25 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json
