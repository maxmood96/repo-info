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
-	[`clickhouse:25.5.10`](#clickhouse25510)
-	[`clickhouse:25.5.10-jammy`](#clickhouse25510-jammy)
-	[`clickhouse:25.5.10.95`](#clickhouse2551095)
-	[`clickhouse:25.5.10.95-jammy`](#clickhouse2551095-jammy)
-	[`clickhouse:25.6`](#clickhouse256)
-	[`clickhouse:25.6-jammy`](#clickhouse256-jammy)
-	[`clickhouse:25.6.8`](#clickhouse2568)
-	[`clickhouse:25.6.8-jammy`](#clickhouse2568-jammy)
-	[`clickhouse:25.6.8.10`](#clickhouse256810)
-	[`clickhouse:25.6.8.10-jammy`](#clickhouse256810-jammy)
-	[`clickhouse:25.7`](#clickhouse257)
-	[`clickhouse:25.7-jammy`](#clickhouse257-jammy)
-	[`clickhouse:25.7.5`](#clickhouse2575)
-	[`clickhouse:25.7.5-jammy`](#clickhouse2575-jammy)
-	[`clickhouse:25.7.5.34`](#clickhouse257534)
-	[`clickhouse:25.7.5.34-jammy`](#clickhouse257534-jammy)
-	[`clickhouse:jammy`](#clickhousejammy)
-	[`clickhouse:latest`](#clickhouselatest)
-	[`clickhouse:lts`](#clickhouselts)
-	[`clickhouse:lts-jammy`](#clickhouselts-jammy)

## `clickhouse:25.3`

```console
$ docker pull clickhouse@sha256:897f6727996c2c6bf768e44b56627dc3fcf2215daa0aecee3d49f5c1d34f0349
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:79c0f0ba61b5a5f7284a10e9f671ccfeab8e445cca58929d14d9b5c30de86d20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.4 MB (205432385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db22b7ed486ee977ad64ddca75012fb3118be31681443b2941bb0c0809c3fb5`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.3.6.56
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28b8b64bfc3c006da3dbdc8315726047223dc83bf809ec568a01a6282bb7c6d`  
		Last Modified: Mon, 01 Sep 2025 23:09:02 GMT  
		Size: 7.2 MB (7151643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3063f406083ccf1f853493cc1903b17828299758cc838c0ae3ff5a1ab038e53a`  
		Last Modified: Tue, 02 Sep 2025 00:49:44 GMT  
		Size: 167.9 MB (167873557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068524848a39bc20273deb9c815010922e604f57cae4d762fe4a110be010b7cc`  
		Last Modified: Mon, 01 Sep 2025 23:09:01 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bbfcd3b5b7985fa5315ff6a50d0e8302ff1ef18dc6ebe4087c197fd26b8483`  
		Last Modified: Mon, 01 Sep 2025 23:09:02 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce48062e0dad3ffc672b574bd49b5254c21bc836e2cd928d35697d45107fa99`  
		Last Modified: Mon, 01 Sep 2025 23:09:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a239040b253b9101ca6a52d9fdf17f703d4d539ea63f832e9295ac84a2eeecb0`  
		Last Modified: Mon, 01 Sep 2025 23:09:03 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ef3f7692f6964082a0ebad321915d0eab0f8f6e4c8c320b008376823e6fd63`  
		Last Modified: Mon, 01 Sep 2025 23:09:03 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:50a83551816610e25f1c81d2c2b78c69e6ab1bffca8651469526761dce29669a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:759649216f9edd7c53fc693d5297c37eb1089638406f26eb7694ea6961951a21`

```dockerfile
```

-	Layers:
	-	`sha256:c307d95fe108fe4572dfab6fbe5f75fa0d6ac491733f5cb90e7aaaab019461b2`  
		Last Modified: Tue, 02 Sep 2025 00:49:19 GMT  
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
$ docker pull clickhouse@sha256:897f6727996c2c6bf768e44b56627dc3fcf2215daa0aecee3d49f5c1d34f0349
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:79c0f0ba61b5a5f7284a10e9f671ccfeab8e445cca58929d14d9b5c30de86d20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.4 MB (205432385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db22b7ed486ee977ad64ddca75012fb3118be31681443b2941bb0c0809c3fb5`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.3.6.56
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28b8b64bfc3c006da3dbdc8315726047223dc83bf809ec568a01a6282bb7c6d`  
		Last Modified: Mon, 01 Sep 2025 23:09:02 GMT  
		Size: 7.2 MB (7151643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3063f406083ccf1f853493cc1903b17828299758cc838c0ae3ff5a1ab038e53a`  
		Last Modified: Tue, 02 Sep 2025 00:49:44 GMT  
		Size: 167.9 MB (167873557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068524848a39bc20273deb9c815010922e604f57cae4d762fe4a110be010b7cc`  
		Last Modified: Mon, 01 Sep 2025 23:09:01 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bbfcd3b5b7985fa5315ff6a50d0e8302ff1ef18dc6ebe4087c197fd26b8483`  
		Last Modified: Mon, 01 Sep 2025 23:09:02 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce48062e0dad3ffc672b574bd49b5254c21bc836e2cd928d35697d45107fa99`  
		Last Modified: Mon, 01 Sep 2025 23:09:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a239040b253b9101ca6a52d9fdf17f703d4d539ea63f832e9295ac84a2eeecb0`  
		Last Modified: Mon, 01 Sep 2025 23:09:03 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ef3f7692f6964082a0ebad321915d0eab0f8f6e4c8c320b008376823e6fd63`  
		Last Modified: Mon, 01 Sep 2025 23:09:03 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:50a83551816610e25f1c81d2c2b78c69e6ab1bffca8651469526761dce29669a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:759649216f9edd7c53fc693d5297c37eb1089638406f26eb7694ea6961951a21`

```dockerfile
```

-	Layers:
	-	`sha256:c307d95fe108fe4572dfab6fbe5f75fa0d6ac491733f5cb90e7aaaab019461b2`  
		Last Modified: Tue, 02 Sep 2025 00:49:19 GMT  
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
$ docker pull clickhouse@sha256:897f6727996c2c6bf768e44b56627dc3fcf2215daa0aecee3d49f5c1d34f0349
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.6` - linux; amd64

```console
$ docker pull clickhouse@sha256:79c0f0ba61b5a5f7284a10e9f671ccfeab8e445cca58929d14d9b5c30de86d20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.4 MB (205432385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db22b7ed486ee977ad64ddca75012fb3118be31681443b2941bb0c0809c3fb5`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.3.6.56
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28b8b64bfc3c006da3dbdc8315726047223dc83bf809ec568a01a6282bb7c6d`  
		Last Modified: Mon, 01 Sep 2025 23:09:02 GMT  
		Size: 7.2 MB (7151643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3063f406083ccf1f853493cc1903b17828299758cc838c0ae3ff5a1ab038e53a`  
		Last Modified: Tue, 02 Sep 2025 00:49:44 GMT  
		Size: 167.9 MB (167873557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068524848a39bc20273deb9c815010922e604f57cae4d762fe4a110be010b7cc`  
		Last Modified: Mon, 01 Sep 2025 23:09:01 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bbfcd3b5b7985fa5315ff6a50d0e8302ff1ef18dc6ebe4087c197fd26b8483`  
		Last Modified: Mon, 01 Sep 2025 23:09:02 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce48062e0dad3ffc672b574bd49b5254c21bc836e2cd928d35697d45107fa99`  
		Last Modified: Mon, 01 Sep 2025 23:09:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a239040b253b9101ca6a52d9fdf17f703d4d539ea63f832e9295ac84a2eeecb0`  
		Last Modified: Mon, 01 Sep 2025 23:09:03 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ef3f7692f6964082a0ebad321915d0eab0f8f6e4c8c320b008376823e6fd63`  
		Last Modified: Mon, 01 Sep 2025 23:09:03 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.6` - unknown; unknown

```console
$ docker pull clickhouse@sha256:50a83551816610e25f1c81d2c2b78c69e6ab1bffca8651469526761dce29669a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:759649216f9edd7c53fc693d5297c37eb1089638406f26eb7694ea6961951a21`

```dockerfile
```

-	Layers:
	-	`sha256:c307d95fe108fe4572dfab6fbe5f75fa0d6ac491733f5cb90e7aaaab019461b2`  
		Last Modified: Tue, 02 Sep 2025 00:49:19 GMT  
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
$ docker pull clickhouse@sha256:897f6727996c2c6bf768e44b56627dc3fcf2215daa0aecee3d49f5c1d34f0349
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.6-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:79c0f0ba61b5a5f7284a10e9f671ccfeab8e445cca58929d14d9b5c30de86d20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.4 MB (205432385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db22b7ed486ee977ad64ddca75012fb3118be31681443b2941bb0c0809c3fb5`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.3.6.56
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28b8b64bfc3c006da3dbdc8315726047223dc83bf809ec568a01a6282bb7c6d`  
		Last Modified: Mon, 01 Sep 2025 23:09:02 GMT  
		Size: 7.2 MB (7151643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3063f406083ccf1f853493cc1903b17828299758cc838c0ae3ff5a1ab038e53a`  
		Last Modified: Tue, 02 Sep 2025 00:49:44 GMT  
		Size: 167.9 MB (167873557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068524848a39bc20273deb9c815010922e604f57cae4d762fe4a110be010b7cc`  
		Last Modified: Mon, 01 Sep 2025 23:09:01 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bbfcd3b5b7985fa5315ff6a50d0e8302ff1ef18dc6ebe4087c197fd26b8483`  
		Last Modified: Mon, 01 Sep 2025 23:09:02 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce48062e0dad3ffc672b574bd49b5254c21bc836e2cd928d35697d45107fa99`  
		Last Modified: Mon, 01 Sep 2025 23:09:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a239040b253b9101ca6a52d9fdf17f703d4d539ea63f832e9295ac84a2eeecb0`  
		Last Modified: Mon, 01 Sep 2025 23:09:03 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ef3f7692f6964082a0ebad321915d0eab0f8f6e4c8c320b008376823e6fd63`  
		Last Modified: Mon, 01 Sep 2025 23:09:03 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.6-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:50a83551816610e25f1c81d2c2b78c69e6ab1bffca8651469526761dce29669a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:759649216f9edd7c53fc693d5297c37eb1089638406f26eb7694ea6961951a21`

```dockerfile
```

-	Layers:
	-	`sha256:c307d95fe108fe4572dfab6fbe5f75fa0d6ac491733f5cb90e7aaaab019461b2`  
		Last Modified: Tue, 02 Sep 2025 00:49:19 GMT  
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
$ docker pull clickhouse@sha256:897f6727996c2c6bf768e44b56627dc3fcf2215daa0aecee3d49f5c1d34f0349
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.6.56` - linux; amd64

```console
$ docker pull clickhouse@sha256:79c0f0ba61b5a5f7284a10e9f671ccfeab8e445cca58929d14d9b5c30de86d20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.4 MB (205432385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db22b7ed486ee977ad64ddca75012fb3118be31681443b2941bb0c0809c3fb5`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.3.6.56
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28b8b64bfc3c006da3dbdc8315726047223dc83bf809ec568a01a6282bb7c6d`  
		Last Modified: Mon, 01 Sep 2025 23:09:02 GMT  
		Size: 7.2 MB (7151643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3063f406083ccf1f853493cc1903b17828299758cc838c0ae3ff5a1ab038e53a`  
		Last Modified: Tue, 02 Sep 2025 00:49:44 GMT  
		Size: 167.9 MB (167873557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068524848a39bc20273deb9c815010922e604f57cae4d762fe4a110be010b7cc`  
		Last Modified: Mon, 01 Sep 2025 23:09:01 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bbfcd3b5b7985fa5315ff6a50d0e8302ff1ef18dc6ebe4087c197fd26b8483`  
		Last Modified: Mon, 01 Sep 2025 23:09:02 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce48062e0dad3ffc672b574bd49b5254c21bc836e2cd928d35697d45107fa99`  
		Last Modified: Mon, 01 Sep 2025 23:09:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a239040b253b9101ca6a52d9fdf17f703d4d539ea63f832e9295ac84a2eeecb0`  
		Last Modified: Mon, 01 Sep 2025 23:09:03 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ef3f7692f6964082a0ebad321915d0eab0f8f6e4c8c320b008376823e6fd63`  
		Last Modified: Mon, 01 Sep 2025 23:09:03 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.6.56` - unknown; unknown

```console
$ docker pull clickhouse@sha256:50a83551816610e25f1c81d2c2b78c69e6ab1bffca8651469526761dce29669a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:759649216f9edd7c53fc693d5297c37eb1089638406f26eb7694ea6961951a21`

```dockerfile
```

-	Layers:
	-	`sha256:c307d95fe108fe4572dfab6fbe5f75fa0d6ac491733f5cb90e7aaaab019461b2`  
		Last Modified: Tue, 02 Sep 2025 00:49:19 GMT  
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
$ docker pull clickhouse@sha256:897f6727996c2c6bf768e44b56627dc3fcf2215daa0aecee3d49f5c1d34f0349
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.6.56-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:79c0f0ba61b5a5f7284a10e9f671ccfeab8e445cca58929d14d9b5c30de86d20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.4 MB (205432385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db22b7ed486ee977ad64ddca75012fb3118be31681443b2941bb0c0809c3fb5`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.3.6.56
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28b8b64bfc3c006da3dbdc8315726047223dc83bf809ec568a01a6282bb7c6d`  
		Last Modified: Mon, 01 Sep 2025 23:09:02 GMT  
		Size: 7.2 MB (7151643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3063f406083ccf1f853493cc1903b17828299758cc838c0ae3ff5a1ab038e53a`  
		Last Modified: Tue, 02 Sep 2025 00:49:44 GMT  
		Size: 167.9 MB (167873557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068524848a39bc20273deb9c815010922e604f57cae4d762fe4a110be010b7cc`  
		Last Modified: Mon, 01 Sep 2025 23:09:01 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bbfcd3b5b7985fa5315ff6a50d0e8302ff1ef18dc6ebe4087c197fd26b8483`  
		Last Modified: Mon, 01 Sep 2025 23:09:02 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce48062e0dad3ffc672b574bd49b5254c21bc836e2cd928d35697d45107fa99`  
		Last Modified: Mon, 01 Sep 2025 23:09:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a239040b253b9101ca6a52d9fdf17f703d4d539ea63f832e9295ac84a2eeecb0`  
		Last Modified: Mon, 01 Sep 2025 23:09:03 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ef3f7692f6964082a0ebad321915d0eab0f8f6e4c8c320b008376823e6fd63`  
		Last Modified: Mon, 01 Sep 2025 23:09:03 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.6.56-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:50a83551816610e25f1c81d2c2b78c69e6ab1bffca8651469526761dce29669a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:759649216f9edd7c53fc693d5297c37eb1089638406f26eb7694ea6961951a21`

```dockerfile
```

-	Layers:
	-	`sha256:c307d95fe108fe4572dfab6fbe5f75fa0d6ac491733f5cb90e7aaaab019461b2`  
		Last Modified: Tue, 02 Sep 2025 00:49:19 GMT  
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
$ docker pull clickhouse@sha256:b93adc6519069a204509994d8fa336210978db3e13b802aa8e76300e119bd5c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.5` - linux; amd64

```console
$ docker pull clickhouse@sha256:0bcc7571acc111dc646795308c563a8ae1c515eca493afc073965e3256f74319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.0 MB (204986560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606ae98f43065a2b44e4d2dceeb6d6b826ba84c64a0b299ebd9f6ccc40f17cf7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.5.10.95
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.10.95 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.10.95 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.10.95 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.10.95 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55cf0ba34be6db4777a231c0021aa8f4d71bbe843c34b02b74a63a068d46c4d3`  
		Last Modified: Tue, 02 Sep 2025 00:23:20 GMT  
		Size: 7.2 MB (7151654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff1f795cfbafdb8baaee45f86adc610731535a6e73ee9e846db8ca63499f1ff`  
		Last Modified: Tue, 02 Sep 2025 00:23:35 GMT  
		Size: 167.4 MB (167427721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9406dfd3e626d72613c8a7a61474c697f49593a2bafd5ed0192b79970ce84b8`  
		Last Modified: Mon, 01 Sep 2025 23:08:45 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ffcf3470b7ec3a16c31c07da8b7d8117b3715b1e2159febb52114cf0f3a80c`  
		Last Modified: Mon, 01 Sep 2025 23:08:46 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e4e1aa8421c773d6c73d7ca7d8bebb82a7de26fa7557f0914e4d4da37d19cb`  
		Last Modified: Mon, 01 Sep 2025 23:08:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf5fcca0bcdf3bc097caab8ebdf399b36896c47018186fc134c35ab991bac68`  
		Last Modified: Mon, 01 Sep 2025 23:08:46 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abeb20da8a289cf66af3ba78811293087cda44cf2305731651f0163dbabfee1c`  
		Last Modified: Mon, 01 Sep 2025 23:08:46 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e8b4f2e09e73b131756019ef152910198e08aadfbbe6b230012a64d2495f5899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe5152f3cc8f97e5d29a8f9ddc4a2ce1ce9e7705d56497985d51b2cfdf1b23b3`

```dockerfile
```

-	Layers:
	-	`sha256:aa2751fdbe76e2b05c6a940c7d8fadb2fd30ad0669df5661a904323821c7fd46`  
		Last Modified: Tue, 02 Sep 2025 00:49:28 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.5` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:2aee723b18fbe336a1bf1d9ab2b20b79499fd6144cf4fee27b87a274ea859b84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.6 MB (191565944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc66f11b25b46fdc6c766aafd37179f3f554e250a97d1d5e6ee7eee1faf95785`
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
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.5.10.95
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.10.95 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.10.95 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.10.95 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.10.95 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cda0881a36768df1ff70dd0327fe11cd1aa5d03a1be3ba0e2d9410b07e34909`  
		Last Modified: Thu, 28 Aug 2025 17:56:34 GMT  
		Size: 7.1 MB (7127896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9629893a8564e09e1d2efd18112b9d8a06f652980d286204f2233a8992b7f601`  
		Last Modified: Thu, 28 Aug 2025 18:49:46 GMT  
		Size: 156.2 MB (156208554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4a7b3234e3ce0f08fb27eb691ad8851495c26484911aaffc3d6420f880721c`  
		Last Modified: Thu, 28 Aug 2025 17:56:34 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f137fd7d9a39b75f0576b240ff5f8e78cad9f1796057f238469c4daef7380e`  
		Last Modified: Thu, 28 Aug 2025 17:56:34 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b68064c1d0669b9938b9e43194779e4cfe5f51274c63157f63aa5e0a884e8ea`  
		Last Modified: Thu, 28 Aug 2025 17:56:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bb59adf0cea953d4f7fe1a401ab8749b62212de52595b0a8c05697a3cc8f5c`  
		Last Modified: Thu, 28 Aug 2025 17:56:34 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25de0bd605f637f97f26e7c1e156ad7d87872d33ad6875086b3749b2618f7d2`  
		Last Modified: Thu, 28 Aug 2025 17:56:34 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9231bc0e5d908927a823c47e105ba2724cfd6ad295a8d9fdc9b1a0095f7c4683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1788c965f09fae3c194e16707229cff179de3101abc1c08bd681a886702917c`

```dockerfile
```

-	Layers:
	-	`sha256:05ec36e6194fdc0b3f2e09bd111e7300749f94b89ffc8df1a5f909d06ac4cab0`  
		Last Modified: Thu, 28 Aug 2025 18:49:27 GMT  
		Size: 25.5 KB (25465 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.5-jammy`

```console
$ docker pull clickhouse@sha256:b93adc6519069a204509994d8fa336210978db3e13b802aa8e76300e119bd5c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.5-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:0bcc7571acc111dc646795308c563a8ae1c515eca493afc073965e3256f74319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.0 MB (204986560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606ae98f43065a2b44e4d2dceeb6d6b826ba84c64a0b299ebd9f6ccc40f17cf7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.5.10.95
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.10.95 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.10.95 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.10.95 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.10.95 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55cf0ba34be6db4777a231c0021aa8f4d71bbe843c34b02b74a63a068d46c4d3`  
		Last Modified: Tue, 02 Sep 2025 00:23:20 GMT  
		Size: 7.2 MB (7151654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff1f795cfbafdb8baaee45f86adc610731535a6e73ee9e846db8ca63499f1ff`  
		Last Modified: Tue, 02 Sep 2025 00:23:35 GMT  
		Size: 167.4 MB (167427721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9406dfd3e626d72613c8a7a61474c697f49593a2bafd5ed0192b79970ce84b8`  
		Last Modified: Mon, 01 Sep 2025 23:08:45 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ffcf3470b7ec3a16c31c07da8b7d8117b3715b1e2159febb52114cf0f3a80c`  
		Last Modified: Mon, 01 Sep 2025 23:08:46 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e4e1aa8421c773d6c73d7ca7d8bebb82a7de26fa7557f0914e4d4da37d19cb`  
		Last Modified: Mon, 01 Sep 2025 23:08:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf5fcca0bcdf3bc097caab8ebdf399b36896c47018186fc134c35ab991bac68`  
		Last Modified: Mon, 01 Sep 2025 23:08:46 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abeb20da8a289cf66af3ba78811293087cda44cf2305731651f0163dbabfee1c`  
		Last Modified: Mon, 01 Sep 2025 23:08:46 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e8b4f2e09e73b131756019ef152910198e08aadfbbe6b230012a64d2495f5899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe5152f3cc8f97e5d29a8f9ddc4a2ce1ce9e7705d56497985d51b2cfdf1b23b3`

```dockerfile
```

-	Layers:
	-	`sha256:aa2751fdbe76e2b05c6a940c7d8fadb2fd30ad0669df5661a904323821c7fd46`  
		Last Modified: Tue, 02 Sep 2025 00:49:28 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.5-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:2aee723b18fbe336a1bf1d9ab2b20b79499fd6144cf4fee27b87a274ea859b84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.6 MB (191565944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc66f11b25b46fdc6c766aafd37179f3f554e250a97d1d5e6ee7eee1faf95785`
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
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.5.10.95
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.10.95 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.10.95 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.10.95 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.10.95 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cda0881a36768df1ff70dd0327fe11cd1aa5d03a1be3ba0e2d9410b07e34909`  
		Last Modified: Thu, 28 Aug 2025 17:56:34 GMT  
		Size: 7.1 MB (7127896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9629893a8564e09e1d2efd18112b9d8a06f652980d286204f2233a8992b7f601`  
		Last Modified: Thu, 28 Aug 2025 18:49:46 GMT  
		Size: 156.2 MB (156208554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4a7b3234e3ce0f08fb27eb691ad8851495c26484911aaffc3d6420f880721c`  
		Last Modified: Thu, 28 Aug 2025 17:56:34 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f137fd7d9a39b75f0576b240ff5f8e78cad9f1796057f238469c4daef7380e`  
		Last Modified: Thu, 28 Aug 2025 17:56:34 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b68064c1d0669b9938b9e43194779e4cfe5f51274c63157f63aa5e0a884e8ea`  
		Last Modified: Thu, 28 Aug 2025 17:56:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bb59adf0cea953d4f7fe1a401ab8749b62212de52595b0a8c05697a3cc8f5c`  
		Last Modified: Thu, 28 Aug 2025 17:56:34 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25de0bd605f637f97f26e7c1e156ad7d87872d33ad6875086b3749b2618f7d2`  
		Last Modified: Thu, 28 Aug 2025 17:56:34 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9231bc0e5d908927a823c47e105ba2724cfd6ad295a8d9fdc9b1a0095f7c4683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1788c965f09fae3c194e16707229cff179de3101abc1c08bd681a886702917c`

```dockerfile
```

-	Layers:
	-	`sha256:05ec36e6194fdc0b3f2e09bd111e7300749f94b89ffc8df1a5f909d06ac4cab0`  
		Last Modified: Thu, 28 Aug 2025 18:49:27 GMT  
		Size: 25.5 KB (25465 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.5.10`

```console
$ docker pull clickhouse@sha256:b93adc6519069a204509994d8fa336210978db3e13b802aa8e76300e119bd5c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.5.10` - linux; amd64

```console
$ docker pull clickhouse@sha256:0bcc7571acc111dc646795308c563a8ae1c515eca493afc073965e3256f74319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.0 MB (204986560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606ae98f43065a2b44e4d2dceeb6d6b826ba84c64a0b299ebd9f6ccc40f17cf7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.5.10.95
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.10.95 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.10.95 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.10.95 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.10.95 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55cf0ba34be6db4777a231c0021aa8f4d71bbe843c34b02b74a63a068d46c4d3`  
		Last Modified: Tue, 02 Sep 2025 00:23:20 GMT  
		Size: 7.2 MB (7151654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff1f795cfbafdb8baaee45f86adc610731535a6e73ee9e846db8ca63499f1ff`  
		Last Modified: Tue, 02 Sep 2025 00:23:35 GMT  
		Size: 167.4 MB (167427721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9406dfd3e626d72613c8a7a61474c697f49593a2bafd5ed0192b79970ce84b8`  
		Last Modified: Mon, 01 Sep 2025 23:08:45 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ffcf3470b7ec3a16c31c07da8b7d8117b3715b1e2159febb52114cf0f3a80c`  
		Last Modified: Mon, 01 Sep 2025 23:08:46 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e4e1aa8421c773d6c73d7ca7d8bebb82a7de26fa7557f0914e4d4da37d19cb`  
		Last Modified: Mon, 01 Sep 2025 23:08:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf5fcca0bcdf3bc097caab8ebdf399b36896c47018186fc134c35ab991bac68`  
		Last Modified: Mon, 01 Sep 2025 23:08:46 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abeb20da8a289cf66af3ba78811293087cda44cf2305731651f0163dbabfee1c`  
		Last Modified: Mon, 01 Sep 2025 23:08:46 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5.10` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e8b4f2e09e73b131756019ef152910198e08aadfbbe6b230012a64d2495f5899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe5152f3cc8f97e5d29a8f9ddc4a2ce1ce9e7705d56497985d51b2cfdf1b23b3`

```dockerfile
```

-	Layers:
	-	`sha256:aa2751fdbe76e2b05c6a940c7d8fadb2fd30ad0669df5661a904323821c7fd46`  
		Last Modified: Tue, 02 Sep 2025 00:49:28 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.5.10` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:2aee723b18fbe336a1bf1d9ab2b20b79499fd6144cf4fee27b87a274ea859b84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.6 MB (191565944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc66f11b25b46fdc6c766aafd37179f3f554e250a97d1d5e6ee7eee1faf95785`
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
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.5.10.95
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.10.95 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.10.95 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.10.95 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.10.95 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cda0881a36768df1ff70dd0327fe11cd1aa5d03a1be3ba0e2d9410b07e34909`  
		Last Modified: Thu, 28 Aug 2025 17:56:34 GMT  
		Size: 7.1 MB (7127896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9629893a8564e09e1d2efd18112b9d8a06f652980d286204f2233a8992b7f601`  
		Last Modified: Thu, 28 Aug 2025 18:49:46 GMT  
		Size: 156.2 MB (156208554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4a7b3234e3ce0f08fb27eb691ad8851495c26484911aaffc3d6420f880721c`  
		Last Modified: Thu, 28 Aug 2025 17:56:34 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f137fd7d9a39b75f0576b240ff5f8e78cad9f1796057f238469c4daef7380e`  
		Last Modified: Thu, 28 Aug 2025 17:56:34 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b68064c1d0669b9938b9e43194779e4cfe5f51274c63157f63aa5e0a884e8ea`  
		Last Modified: Thu, 28 Aug 2025 17:56:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bb59adf0cea953d4f7fe1a401ab8749b62212de52595b0a8c05697a3cc8f5c`  
		Last Modified: Thu, 28 Aug 2025 17:56:34 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25de0bd605f637f97f26e7c1e156ad7d87872d33ad6875086b3749b2618f7d2`  
		Last Modified: Thu, 28 Aug 2025 17:56:34 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5.10` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9231bc0e5d908927a823c47e105ba2724cfd6ad295a8d9fdc9b1a0095f7c4683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1788c965f09fae3c194e16707229cff179de3101abc1c08bd681a886702917c`

```dockerfile
```

-	Layers:
	-	`sha256:05ec36e6194fdc0b3f2e09bd111e7300749f94b89ffc8df1a5f909d06ac4cab0`  
		Last Modified: Thu, 28 Aug 2025 18:49:27 GMT  
		Size: 25.5 KB (25465 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.5.10-jammy`

```console
$ docker pull clickhouse@sha256:b93adc6519069a204509994d8fa336210978db3e13b802aa8e76300e119bd5c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.5.10-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:0bcc7571acc111dc646795308c563a8ae1c515eca493afc073965e3256f74319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.0 MB (204986560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606ae98f43065a2b44e4d2dceeb6d6b826ba84c64a0b299ebd9f6ccc40f17cf7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.5.10.95
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.10.95 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.10.95 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.10.95 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.10.95 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55cf0ba34be6db4777a231c0021aa8f4d71bbe843c34b02b74a63a068d46c4d3`  
		Last Modified: Tue, 02 Sep 2025 00:23:20 GMT  
		Size: 7.2 MB (7151654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff1f795cfbafdb8baaee45f86adc610731535a6e73ee9e846db8ca63499f1ff`  
		Last Modified: Tue, 02 Sep 2025 00:23:35 GMT  
		Size: 167.4 MB (167427721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9406dfd3e626d72613c8a7a61474c697f49593a2bafd5ed0192b79970ce84b8`  
		Last Modified: Mon, 01 Sep 2025 23:08:45 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ffcf3470b7ec3a16c31c07da8b7d8117b3715b1e2159febb52114cf0f3a80c`  
		Last Modified: Mon, 01 Sep 2025 23:08:46 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e4e1aa8421c773d6c73d7ca7d8bebb82a7de26fa7557f0914e4d4da37d19cb`  
		Last Modified: Mon, 01 Sep 2025 23:08:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf5fcca0bcdf3bc097caab8ebdf399b36896c47018186fc134c35ab991bac68`  
		Last Modified: Mon, 01 Sep 2025 23:08:46 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abeb20da8a289cf66af3ba78811293087cda44cf2305731651f0163dbabfee1c`  
		Last Modified: Mon, 01 Sep 2025 23:08:46 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5.10-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e8b4f2e09e73b131756019ef152910198e08aadfbbe6b230012a64d2495f5899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe5152f3cc8f97e5d29a8f9ddc4a2ce1ce9e7705d56497985d51b2cfdf1b23b3`

```dockerfile
```

-	Layers:
	-	`sha256:aa2751fdbe76e2b05c6a940c7d8fadb2fd30ad0669df5661a904323821c7fd46`  
		Last Modified: Tue, 02 Sep 2025 00:49:28 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.5.10-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:2aee723b18fbe336a1bf1d9ab2b20b79499fd6144cf4fee27b87a274ea859b84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.6 MB (191565944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc66f11b25b46fdc6c766aafd37179f3f554e250a97d1d5e6ee7eee1faf95785`
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
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.5.10.95
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.10.95 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.10.95 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.10.95 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.10.95 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cda0881a36768df1ff70dd0327fe11cd1aa5d03a1be3ba0e2d9410b07e34909`  
		Last Modified: Thu, 28 Aug 2025 17:56:34 GMT  
		Size: 7.1 MB (7127896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9629893a8564e09e1d2efd18112b9d8a06f652980d286204f2233a8992b7f601`  
		Last Modified: Thu, 28 Aug 2025 18:49:46 GMT  
		Size: 156.2 MB (156208554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4a7b3234e3ce0f08fb27eb691ad8851495c26484911aaffc3d6420f880721c`  
		Last Modified: Thu, 28 Aug 2025 17:56:34 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f137fd7d9a39b75f0576b240ff5f8e78cad9f1796057f238469c4daef7380e`  
		Last Modified: Thu, 28 Aug 2025 17:56:34 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b68064c1d0669b9938b9e43194779e4cfe5f51274c63157f63aa5e0a884e8ea`  
		Last Modified: Thu, 28 Aug 2025 17:56:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bb59adf0cea953d4f7fe1a401ab8749b62212de52595b0a8c05697a3cc8f5c`  
		Last Modified: Thu, 28 Aug 2025 17:56:34 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25de0bd605f637f97f26e7c1e156ad7d87872d33ad6875086b3749b2618f7d2`  
		Last Modified: Thu, 28 Aug 2025 17:56:34 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5.10-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9231bc0e5d908927a823c47e105ba2724cfd6ad295a8d9fdc9b1a0095f7c4683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1788c965f09fae3c194e16707229cff179de3101abc1c08bd681a886702917c`

```dockerfile
```

-	Layers:
	-	`sha256:05ec36e6194fdc0b3f2e09bd111e7300749f94b89ffc8df1a5f909d06ac4cab0`  
		Last Modified: Thu, 28 Aug 2025 18:49:27 GMT  
		Size: 25.5 KB (25465 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.5.10.95`

```console
$ docker pull clickhouse@sha256:b93adc6519069a204509994d8fa336210978db3e13b802aa8e76300e119bd5c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.5.10.95` - linux; amd64

```console
$ docker pull clickhouse@sha256:0bcc7571acc111dc646795308c563a8ae1c515eca493afc073965e3256f74319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.0 MB (204986560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606ae98f43065a2b44e4d2dceeb6d6b826ba84c64a0b299ebd9f6ccc40f17cf7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.5.10.95
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.10.95 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.10.95 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.10.95 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.10.95 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55cf0ba34be6db4777a231c0021aa8f4d71bbe843c34b02b74a63a068d46c4d3`  
		Last Modified: Tue, 02 Sep 2025 00:23:20 GMT  
		Size: 7.2 MB (7151654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff1f795cfbafdb8baaee45f86adc610731535a6e73ee9e846db8ca63499f1ff`  
		Last Modified: Tue, 02 Sep 2025 00:23:35 GMT  
		Size: 167.4 MB (167427721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9406dfd3e626d72613c8a7a61474c697f49593a2bafd5ed0192b79970ce84b8`  
		Last Modified: Mon, 01 Sep 2025 23:08:45 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ffcf3470b7ec3a16c31c07da8b7d8117b3715b1e2159febb52114cf0f3a80c`  
		Last Modified: Mon, 01 Sep 2025 23:08:46 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e4e1aa8421c773d6c73d7ca7d8bebb82a7de26fa7557f0914e4d4da37d19cb`  
		Last Modified: Mon, 01 Sep 2025 23:08:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf5fcca0bcdf3bc097caab8ebdf399b36896c47018186fc134c35ab991bac68`  
		Last Modified: Mon, 01 Sep 2025 23:08:46 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abeb20da8a289cf66af3ba78811293087cda44cf2305731651f0163dbabfee1c`  
		Last Modified: Mon, 01 Sep 2025 23:08:46 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5.10.95` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e8b4f2e09e73b131756019ef152910198e08aadfbbe6b230012a64d2495f5899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe5152f3cc8f97e5d29a8f9ddc4a2ce1ce9e7705d56497985d51b2cfdf1b23b3`

```dockerfile
```

-	Layers:
	-	`sha256:aa2751fdbe76e2b05c6a940c7d8fadb2fd30ad0669df5661a904323821c7fd46`  
		Last Modified: Tue, 02 Sep 2025 00:49:28 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.5.10.95` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:2aee723b18fbe336a1bf1d9ab2b20b79499fd6144cf4fee27b87a274ea859b84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.6 MB (191565944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc66f11b25b46fdc6c766aafd37179f3f554e250a97d1d5e6ee7eee1faf95785`
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
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.5.10.95
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.10.95 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.10.95 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.10.95 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.10.95 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cda0881a36768df1ff70dd0327fe11cd1aa5d03a1be3ba0e2d9410b07e34909`  
		Last Modified: Thu, 28 Aug 2025 17:56:34 GMT  
		Size: 7.1 MB (7127896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9629893a8564e09e1d2efd18112b9d8a06f652980d286204f2233a8992b7f601`  
		Last Modified: Thu, 28 Aug 2025 18:49:46 GMT  
		Size: 156.2 MB (156208554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4a7b3234e3ce0f08fb27eb691ad8851495c26484911aaffc3d6420f880721c`  
		Last Modified: Thu, 28 Aug 2025 17:56:34 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f137fd7d9a39b75f0576b240ff5f8e78cad9f1796057f238469c4daef7380e`  
		Last Modified: Thu, 28 Aug 2025 17:56:34 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b68064c1d0669b9938b9e43194779e4cfe5f51274c63157f63aa5e0a884e8ea`  
		Last Modified: Thu, 28 Aug 2025 17:56:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bb59adf0cea953d4f7fe1a401ab8749b62212de52595b0a8c05697a3cc8f5c`  
		Last Modified: Thu, 28 Aug 2025 17:56:34 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25de0bd605f637f97f26e7c1e156ad7d87872d33ad6875086b3749b2618f7d2`  
		Last Modified: Thu, 28 Aug 2025 17:56:34 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5.10.95` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9231bc0e5d908927a823c47e105ba2724cfd6ad295a8d9fdc9b1a0095f7c4683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1788c965f09fae3c194e16707229cff179de3101abc1c08bd681a886702917c`

```dockerfile
```

-	Layers:
	-	`sha256:05ec36e6194fdc0b3f2e09bd111e7300749f94b89ffc8df1a5f909d06ac4cab0`  
		Last Modified: Thu, 28 Aug 2025 18:49:27 GMT  
		Size: 25.5 KB (25465 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.5.10.95-jammy`

```console
$ docker pull clickhouse@sha256:b93adc6519069a204509994d8fa336210978db3e13b802aa8e76300e119bd5c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.5.10.95-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:0bcc7571acc111dc646795308c563a8ae1c515eca493afc073965e3256f74319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.0 MB (204986560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606ae98f43065a2b44e4d2dceeb6d6b826ba84c64a0b299ebd9f6ccc40f17cf7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.5.10.95
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.10.95 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.10.95 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.10.95 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.10.95 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55cf0ba34be6db4777a231c0021aa8f4d71bbe843c34b02b74a63a068d46c4d3`  
		Last Modified: Tue, 02 Sep 2025 00:23:20 GMT  
		Size: 7.2 MB (7151654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff1f795cfbafdb8baaee45f86adc610731535a6e73ee9e846db8ca63499f1ff`  
		Last Modified: Tue, 02 Sep 2025 00:23:35 GMT  
		Size: 167.4 MB (167427721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9406dfd3e626d72613c8a7a61474c697f49593a2bafd5ed0192b79970ce84b8`  
		Last Modified: Mon, 01 Sep 2025 23:08:45 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ffcf3470b7ec3a16c31c07da8b7d8117b3715b1e2159febb52114cf0f3a80c`  
		Last Modified: Mon, 01 Sep 2025 23:08:46 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e4e1aa8421c773d6c73d7ca7d8bebb82a7de26fa7557f0914e4d4da37d19cb`  
		Last Modified: Mon, 01 Sep 2025 23:08:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf5fcca0bcdf3bc097caab8ebdf399b36896c47018186fc134c35ab991bac68`  
		Last Modified: Mon, 01 Sep 2025 23:08:46 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abeb20da8a289cf66af3ba78811293087cda44cf2305731651f0163dbabfee1c`  
		Last Modified: Mon, 01 Sep 2025 23:08:46 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5.10.95-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e8b4f2e09e73b131756019ef152910198e08aadfbbe6b230012a64d2495f5899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe5152f3cc8f97e5d29a8f9ddc4a2ce1ce9e7705d56497985d51b2cfdf1b23b3`

```dockerfile
```

-	Layers:
	-	`sha256:aa2751fdbe76e2b05c6a940c7d8fadb2fd30ad0669df5661a904323821c7fd46`  
		Last Modified: Tue, 02 Sep 2025 00:49:28 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.5.10.95-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:2aee723b18fbe336a1bf1d9ab2b20b79499fd6144cf4fee27b87a274ea859b84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.6 MB (191565944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc66f11b25b46fdc6c766aafd37179f3f554e250a97d1d5e6ee7eee1faf95785`
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
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.5.10.95
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.10.95 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.10.95 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.10.95 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.10.95 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cda0881a36768df1ff70dd0327fe11cd1aa5d03a1be3ba0e2d9410b07e34909`  
		Last Modified: Thu, 28 Aug 2025 17:56:34 GMT  
		Size: 7.1 MB (7127896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9629893a8564e09e1d2efd18112b9d8a06f652980d286204f2233a8992b7f601`  
		Last Modified: Thu, 28 Aug 2025 18:49:46 GMT  
		Size: 156.2 MB (156208554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4a7b3234e3ce0f08fb27eb691ad8851495c26484911aaffc3d6420f880721c`  
		Last Modified: Thu, 28 Aug 2025 17:56:34 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f137fd7d9a39b75f0576b240ff5f8e78cad9f1796057f238469c4daef7380e`  
		Last Modified: Thu, 28 Aug 2025 17:56:34 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b68064c1d0669b9938b9e43194779e4cfe5f51274c63157f63aa5e0a884e8ea`  
		Last Modified: Thu, 28 Aug 2025 17:56:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bb59adf0cea953d4f7fe1a401ab8749b62212de52595b0a8c05697a3cc8f5c`  
		Last Modified: Thu, 28 Aug 2025 17:56:34 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25de0bd605f637f97f26e7c1e156ad7d87872d33ad6875086b3749b2618f7d2`  
		Last Modified: Thu, 28 Aug 2025 17:56:34 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5.10.95-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9231bc0e5d908927a823c47e105ba2724cfd6ad295a8d9fdc9b1a0095f7c4683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1788c965f09fae3c194e16707229cff179de3101abc1c08bd681a886702917c`

```dockerfile
```

-	Layers:
	-	`sha256:05ec36e6194fdc0b3f2e09bd111e7300749f94b89ffc8df1a5f909d06ac4cab0`  
		Last Modified: Thu, 28 Aug 2025 18:49:27 GMT  
		Size: 25.5 KB (25465 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.6`

```console
$ docker pull clickhouse@sha256:dd12b46a9f78b9de1bc8296914ce75e982bb4a9e3c50e43fb8beca44aed2329f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6` - linux; amd64

```console
$ docker pull clickhouse@sha256:c28e9483a2c4837f2fe2839694622bedd89372147708e9a75060ef43c70ddf61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.0 MB (212029043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0ee6d87a35f31e2b499f7a980b1a97da096d72dd306a0e47e366fa14224edd1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.6.8.10
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4bd7829c7f2dd175984dc7ab80e67eb4a8a3684b68e4fab9f52bf0ee529000`  
		Last Modified: Mon, 01 Sep 2025 23:08:38 GMT  
		Size: 7.2 MB (7151613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae58093d8c482079a30ad8cd2a0c9782c4c15249a4a3e66a009f30ccfa5d911`  
		Last Modified: Tue, 02 Sep 2025 00:50:00 GMT  
		Size: 174.5 MB (174470475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1cf8dbbb7996eeb806f2976b0050939cf2091ded83566a62e5ab1d0dad4c5f`  
		Last Modified: Mon, 01 Sep 2025 23:08:37 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2a4820998a7dacf99068afa4331d4c8b4d5d44d16bf030897619496712877c`  
		Last Modified: Mon, 01 Sep 2025 23:08:37 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b1646140461586c78576529bab1b3695efb7d0eea52c1efcbdcdcd9d4da5b7`  
		Last Modified: Mon, 01 Sep 2025 23:08:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf0c400e1876b4d90cca5c40ffe6405e7bc3bd9d6db3a08a2dc20bf15b84fcf`  
		Last Modified: Mon, 01 Sep 2025 23:08:37 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9be2b31810852d75d7917675b61ceca91b90820e8c9b79e67057d4687c4e9f3`  
		Last Modified: Mon, 01 Sep 2025 23:08:37 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6` - unknown; unknown

```console
$ docker pull clickhouse@sha256:dfcfaeb3c5a15c8f9122c8a525bd9cdf1e37e2f6025bbac372835d2d806ecd24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c509aef850e305e4836a2d13d45ab0dc8acd6a59c39ca3d80436c5c13d5cf36`

```dockerfile
```

-	Layers:
	-	`sha256:dd186f6a3a8fa8784c227fb474cd37ee50c6e0e816a3ac3d2eb4a61f892d64b0`  
		Last Modified: Tue, 02 Sep 2025 00:49:37 GMT  
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
$ docker pull clickhouse@sha256:dd12b46a9f78b9de1bc8296914ce75e982bb4a9e3c50e43fb8beca44aed2329f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:c28e9483a2c4837f2fe2839694622bedd89372147708e9a75060ef43c70ddf61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.0 MB (212029043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0ee6d87a35f31e2b499f7a980b1a97da096d72dd306a0e47e366fa14224edd1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.6.8.10
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4bd7829c7f2dd175984dc7ab80e67eb4a8a3684b68e4fab9f52bf0ee529000`  
		Last Modified: Mon, 01 Sep 2025 23:08:38 GMT  
		Size: 7.2 MB (7151613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae58093d8c482079a30ad8cd2a0c9782c4c15249a4a3e66a009f30ccfa5d911`  
		Last Modified: Tue, 02 Sep 2025 00:50:00 GMT  
		Size: 174.5 MB (174470475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1cf8dbbb7996eeb806f2976b0050939cf2091ded83566a62e5ab1d0dad4c5f`  
		Last Modified: Mon, 01 Sep 2025 23:08:37 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2a4820998a7dacf99068afa4331d4c8b4d5d44d16bf030897619496712877c`  
		Last Modified: Mon, 01 Sep 2025 23:08:37 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b1646140461586c78576529bab1b3695efb7d0eea52c1efcbdcdcd9d4da5b7`  
		Last Modified: Mon, 01 Sep 2025 23:08:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf0c400e1876b4d90cca5c40ffe6405e7bc3bd9d6db3a08a2dc20bf15b84fcf`  
		Last Modified: Mon, 01 Sep 2025 23:08:37 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9be2b31810852d75d7917675b61ceca91b90820e8c9b79e67057d4687c4e9f3`  
		Last Modified: Mon, 01 Sep 2025 23:08:37 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:dfcfaeb3c5a15c8f9122c8a525bd9cdf1e37e2f6025bbac372835d2d806ecd24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c509aef850e305e4836a2d13d45ab0dc8acd6a59c39ca3d80436c5c13d5cf36`

```dockerfile
```

-	Layers:
	-	`sha256:dd186f6a3a8fa8784c227fb474cd37ee50c6e0e816a3ac3d2eb4a61f892d64b0`  
		Last Modified: Tue, 02 Sep 2025 00:49:37 GMT  
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
$ docker pull clickhouse@sha256:dd12b46a9f78b9de1bc8296914ce75e982bb4a9e3c50e43fb8beca44aed2329f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6.8` - linux; amd64

```console
$ docker pull clickhouse@sha256:c28e9483a2c4837f2fe2839694622bedd89372147708e9a75060ef43c70ddf61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.0 MB (212029043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0ee6d87a35f31e2b499f7a980b1a97da096d72dd306a0e47e366fa14224edd1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.6.8.10
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4bd7829c7f2dd175984dc7ab80e67eb4a8a3684b68e4fab9f52bf0ee529000`  
		Last Modified: Mon, 01 Sep 2025 23:08:38 GMT  
		Size: 7.2 MB (7151613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae58093d8c482079a30ad8cd2a0c9782c4c15249a4a3e66a009f30ccfa5d911`  
		Last Modified: Tue, 02 Sep 2025 00:50:00 GMT  
		Size: 174.5 MB (174470475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1cf8dbbb7996eeb806f2976b0050939cf2091ded83566a62e5ab1d0dad4c5f`  
		Last Modified: Mon, 01 Sep 2025 23:08:37 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2a4820998a7dacf99068afa4331d4c8b4d5d44d16bf030897619496712877c`  
		Last Modified: Mon, 01 Sep 2025 23:08:37 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b1646140461586c78576529bab1b3695efb7d0eea52c1efcbdcdcd9d4da5b7`  
		Last Modified: Mon, 01 Sep 2025 23:08:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf0c400e1876b4d90cca5c40ffe6405e7bc3bd9d6db3a08a2dc20bf15b84fcf`  
		Last Modified: Mon, 01 Sep 2025 23:08:37 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9be2b31810852d75d7917675b61ceca91b90820e8c9b79e67057d4687c4e9f3`  
		Last Modified: Mon, 01 Sep 2025 23:08:37 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:dfcfaeb3c5a15c8f9122c8a525bd9cdf1e37e2f6025bbac372835d2d806ecd24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c509aef850e305e4836a2d13d45ab0dc8acd6a59c39ca3d80436c5c13d5cf36`

```dockerfile
```

-	Layers:
	-	`sha256:dd186f6a3a8fa8784c227fb474cd37ee50c6e0e816a3ac3d2eb4a61f892d64b0`  
		Last Modified: Tue, 02 Sep 2025 00:49:37 GMT  
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
$ docker pull clickhouse@sha256:dd12b46a9f78b9de1bc8296914ce75e982bb4a9e3c50e43fb8beca44aed2329f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6.8-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:c28e9483a2c4837f2fe2839694622bedd89372147708e9a75060ef43c70ddf61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.0 MB (212029043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0ee6d87a35f31e2b499f7a980b1a97da096d72dd306a0e47e366fa14224edd1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.6.8.10
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4bd7829c7f2dd175984dc7ab80e67eb4a8a3684b68e4fab9f52bf0ee529000`  
		Last Modified: Mon, 01 Sep 2025 23:08:38 GMT  
		Size: 7.2 MB (7151613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae58093d8c482079a30ad8cd2a0c9782c4c15249a4a3e66a009f30ccfa5d911`  
		Last Modified: Tue, 02 Sep 2025 00:50:00 GMT  
		Size: 174.5 MB (174470475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1cf8dbbb7996eeb806f2976b0050939cf2091ded83566a62e5ab1d0dad4c5f`  
		Last Modified: Mon, 01 Sep 2025 23:08:37 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2a4820998a7dacf99068afa4331d4c8b4d5d44d16bf030897619496712877c`  
		Last Modified: Mon, 01 Sep 2025 23:08:37 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b1646140461586c78576529bab1b3695efb7d0eea52c1efcbdcdcd9d4da5b7`  
		Last Modified: Mon, 01 Sep 2025 23:08:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf0c400e1876b4d90cca5c40ffe6405e7bc3bd9d6db3a08a2dc20bf15b84fcf`  
		Last Modified: Mon, 01 Sep 2025 23:08:37 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9be2b31810852d75d7917675b61ceca91b90820e8c9b79e67057d4687c4e9f3`  
		Last Modified: Mon, 01 Sep 2025 23:08:37 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:dfcfaeb3c5a15c8f9122c8a525bd9cdf1e37e2f6025bbac372835d2d806ecd24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c509aef850e305e4836a2d13d45ab0dc8acd6a59c39ca3d80436c5c13d5cf36`

```dockerfile
```

-	Layers:
	-	`sha256:dd186f6a3a8fa8784c227fb474cd37ee50c6e0e816a3ac3d2eb4a61f892d64b0`  
		Last Modified: Tue, 02 Sep 2025 00:49:37 GMT  
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
$ docker pull clickhouse@sha256:dd12b46a9f78b9de1bc8296914ce75e982bb4a9e3c50e43fb8beca44aed2329f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6.8.10` - linux; amd64

```console
$ docker pull clickhouse@sha256:c28e9483a2c4837f2fe2839694622bedd89372147708e9a75060ef43c70ddf61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.0 MB (212029043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0ee6d87a35f31e2b499f7a980b1a97da096d72dd306a0e47e366fa14224edd1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.6.8.10
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4bd7829c7f2dd175984dc7ab80e67eb4a8a3684b68e4fab9f52bf0ee529000`  
		Last Modified: Mon, 01 Sep 2025 23:08:38 GMT  
		Size: 7.2 MB (7151613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae58093d8c482079a30ad8cd2a0c9782c4c15249a4a3e66a009f30ccfa5d911`  
		Last Modified: Tue, 02 Sep 2025 00:50:00 GMT  
		Size: 174.5 MB (174470475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1cf8dbbb7996eeb806f2976b0050939cf2091ded83566a62e5ab1d0dad4c5f`  
		Last Modified: Mon, 01 Sep 2025 23:08:37 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2a4820998a7dacf99068afa4331d4c8b4d5d44d16bf030897619496712877c`  
		Last Modified: Mon, 01 Sep 2025 23:08:37 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b1646140461586c78576529bab1b3695efb7d0eea52c1efcbdcdcd9d4da5b7`  
		Last Modified: Mon, 01 Sep 2025 23:08:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf0c400e1876b4d90cca5c40ffe6405e7bc3bd9d6db3a08a2dc20bf15b84fcf`  
		Last Modified: Mon, 01 Sep 2025 23:08:37 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9be2b31810852d75d7917675b61ceca91b90820e8c9b79e67057d4687c4e9f3`  
		Last Modified: Mon, 01 Sep 2025 23:08:37 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.8.10` - unknown; unknown

```console
$ docker pull clickhouse@sha256:dfcfaeb3c5a15c8f9122c8a525bd9cdf1e37e2f6025bbac372835d2d806ecd24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c509aef850e305e4836a2d13d45ab0dc8acd6a59c39ca3d80436c5c13d5cf36`

```dockerfile
```

-	Layers:
	-	`sha256:dd186f6a3a8fa8784c227fb474cd37ee50c6e0e816a3ac3d2eb4a61f892d64b0`  
		Last Modified: Tue, 02 Sep 2025 00:49:37 GMT  
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
$ docker pull clickhouse@sha256:dd12b46a9f78b9de1bc8296914ce75e982bb4a9e3c50e43fb8beca44aed2329f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6.8.10-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:c28e9483a2c4837f2fe2839694622bedd89372147708e9a75060ef43c70ddf61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.0 MB (212029043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0ee6d87a35f31e2b499f7a980b1a97da096d72dd306a0e47e366fa14224edd1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.6.8.10
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.8.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4bd7829c7f2dd175984dc7ab80e67eb4a8a3684b68e4fab9f52bf0ee529000`  
		Last Modified: Mon, 01 Sep 2025 23:08:38 GMT  
		Size: 7.2 MB (7151613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae58093d8c482079a30ad8cd2a0c9782c4c15249a4a3e66a009f30ccfa5d911`  
		Last Modified: Tue, 02 Sep 2025 00:50:00 GMT  
		Size: 174.5 MB (174470475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1cf8dbbb7996eeb806f2976b0050939cf2091ded83566a62e5ab1d0dad4c5f`  
		Last Modified: Mon, 01 Sep 2025 23:08:37 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2a4820998a7dacf99068afa4331d4c8b4d5d44d16bf030897619496712877c`  
		Last Modified: Mon, 01 Sep 2025 23:08:37 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b1646140461586c78576529bab1b3695efb7d0eea52c1efcbdcdcd9d4da5b7`  
		Last Modified: Mon, 01 Sep 2025 23:08:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf0c400e1876b4d90cca5c40ffe6405e7bc3bd9d6db3a08a2dc20bf15b84fcf`  
		Last Modified: Mon, 01 Sep 2025 23:08:37 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9be2b31810852d75d7917675b61ceca91b90820e8c9b79e67057d4687c4e9f3`  
		Last Modified: Mon, 01 Sep 2025 23:08:37 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.8.10-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:dfcfaeb3c5a15c8f9122c8a525bd9cdf1e37e2f6025bbac372835d2d806ecd24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c509aef850e305e4836a2d13d45ab0dc8acd6a59c39ca3d80436c5c13d5cf36`

```dockerfile
```

-	Layers:
	-	`sha256:dd186f6a3a8fa8784c227fb474cd37ee50c6e0e816a3ac3d2eb4a61f892d64b0`  
		Last Modified: Tue, 02 Sep 2025 00:49:37 GMT  
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
$ docker pull clickhouse@sha256:1508289214b29246fd35a488d405dea6165b952ab2adf1b0be001bc1cdc42583
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.7` - linux; amd64

```console
$ docker pull clickhouse@sha256:f5667c6b06d142244823009828ba9c547f26c7951f3e300abde0d70cc3977c4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.8 MB (221797576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2319e022e1159e0362f694dae9d62c6303f5412b24bbda06d8d3a1f26f87a0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.7.5.34
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0acf31bcca6e9d020dc3cd6cf1a2cf27bdbed95f073afb7c89a998dbef961881`  
		Last Modified: Mon, 01 Sep 2025 23:08:51 GMT  
		Size: 7.6 MB (7598441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3acf2cfb5f58d29d4ed6f0f157dc9e27446f2217744760f800761fbe09f5c75d`  
		Last Modified: Tue, 02 Sep 2025 00:49:59 GMT  
		Size: 183.8 MB (183792178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e433084271857428ea3902ea62c02c1aed622e54938c7323ec2413507c61596`  
		Last Modified: Mon, 01 Sep 2025 23:08:51 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef32936b35234483f20ea9f67542299ebaab52cae3e5a5248295bd75e3885a1`  
		Last Modified: Mon, 01 Sep 2025 23:08:51 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b9fc87ee27c0bb8ea9548795698247b9d25a399ba76225803fce45aff2ea6d`  
		Last Modified: Mon, 01 Sep 2025 23:08:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882143b2addcc1efd237c25fc818844571236a7f37a43213a702b662e3ee8674`  
		Last Modified: Mon, 01 Sep 2025 23:08:53 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85737f8b0e50d3dc6e877a7784ebb8cb187102db8d56f857a0dd231883cc56a2`  
		Last Modified: Mon, 01 Sep 2025 23:08:54 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3eb2216cf2b9cf5ef7b00f546c313dcee62890da74a8a2325e026a7508485f9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48d49fe7937afdf335fc473758bd0c6dcecd7a36bfe265dcfade8c232bc3082`

```dockerfile
```

-	Layers:
	-	`sha256:87e6d65a8eda12e0b8069b19788123dd91da9fcf4b213e89d6880962f825a54f`  
		Last Modified: Tue, 02 Sep 2025 00:49:47 GMT  
		Size: 26.1 KB (26070 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.7` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:ca208d9b17099544c4b0d1625319f7cde591f2c63ad765374b8b33997fa936fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207741903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d171afdf1c548ab261c07c93896a196012d7095ce64d654081d1dcf05f2b735`
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
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.7.5.34
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78dfb031d96f0d6e0220d56775bfbe34690e364e89a1bb14a2448fb489fecde`  
		Last Modified: Thu, 28 Aug 2025 17:54:42 GMT  
		Size: 7.6 MB (7577285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe87a91d8723e8bac5bd512c577a4c35923579f053a75af56940a02b604fb775`  
		Last Modified: Thu, 28 Aug 2025 18:40:41 GMT  
		Size: 171.9 MB (171935346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c03d31bb76761e17be10afee6782ff6e78947fa79e295a8d2a3f1f626f841df`  
		Last Modified: Thu, 28 Aug 2025 17:54:41 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77512bf52bfcb5eae03b1e48b59afc8648a9363715a23b2813fcb846dcbc7e5`  
		Last Modified: Thu, 28 Aug 2025 17:54:42 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da12be5d638ee43e262a6162d62702ff8c4f95b6fea366fa9c2d95afb33d7001`  
		Last Modified: Thu, 28 Aug 2025 17:54:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c4efa96760bea1a09199c43903851b8b4c5c8d3bab838dabde5c67c1ac2b2d`  
		Last Modified: Thu, 28 Aug 2025 17:54:42 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3887264c85bbf58061466aad9577404039f58fd7580be096f0bb288e8b480483`  
		Last Modified: Thu, 28 Aug 2025 17:54:42 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9a407fe3edc84eff68792592deeab655212a6d441a9e18ca188792fdd4b46670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e4d81eb5d7b91693ffa4c17eedae9eb13ee61e12c007a3885826783a8f38363`

```dockerfile
```

-	Layers:
	-	`sha256:664cdd35be364a4d5bb090d74f01626feadc11ec4e3c4358d0a9cea8963324e4`  
		Last Modified: Thu, 28 Aug 2025 18:49:41 GMT  
		Size: 26.3 KB (26283 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.7-jammy`

```console
$ docker pull clickhouse@sha256:1508289214b29246fd35a488d405dea6165b952ab2adf1b0be001bc1cdc42583
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.7-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:f5667c6b06d142244823009828ba9c547f26c7951f3e300abde0d70cc3977c4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.8 MB (221797576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2319e022e1159e0362f694dae9d62c6303f5412b24bbda06d8d3a1f26f87a0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.7.5.34
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0acf31bcca6e9d020dc3cd6cf1a2cf27bdbed95f073afb7c89a998dbef961881`  
		Last Modified: Mon, 01 Sep 2025 23:08:51 GMT  
		Size: 7.6 MB (7598441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3acf2cfb5f58d29d4ed6f0f157dc9e27446f2217744760f800761fbe09f5c75d`  
		Last Modified: Tue, 02 Sep 2025 00:49:59 GMT  
		Size: 183.8 MB (183792178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e433084271857428ea3902ea62c02c1aed622e54938c7323ec2413507c61596`  
		Last Modified: Mon, 01 Sep 2025 23:08:51 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef32936b35234483f20ea9f67542299ebaab52cae3e5a5248295bd75e3885a1`  
		Last Modified: Mon, 01 Sep 2025 23:08:51 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b9fc87ee27c0bb8ea9548795698247b9d25a399ba76225803fce45aff2ea6d`  
		Last Modified: Mon, 01 Sep 2025 23:08:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882143b2addcc1efd237c25fc818844571236a7f37a43213a702b662e3ee8674`  
		Last Modified: Mon, 01 Sep 2025 23:08:53 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85737f8b0e50d3dc6e877a7784ebb8cb187102db8d56f857a0dd231883cc56a2`  
		Last Modified: Mon, 01 Sep 2025 23:08:54 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3eb2216cf2b9cf5ef7b00f546c313dcee62890da74a8a2325e026a7508485f9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48d49fe7937afdf335fc473758bd0c6dcecd7a36bfe265dcfade8c232bc3082`

```dockerfile
```

-	Layers:
	-	`sha256:87e6d65a8eda12e0b8069b19788123dd91da9fcf4b213e89d6880962f825a54f`  
		Last Modified: Tue, 02 Sep 2025 00:49:47 GMT  
		Size: 26.1 KB (26070 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.7-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:ca208d9b17099544c4b0d1625319f7cde591f2c63ad765374b8b33997fa936fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207741903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d171afdf1c548ab261c07c93896a196012d7095ce64d654081d1dcf05f2b735`
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
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.7.5.34
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78dfb031d96f0d6e0220d56775bfbe34690e364e89a1bb14a2448fb489fecde`  
		Last Modified: Thu, 28 Aug 2025 17:54:42 GMT  
		Size: 7.6 MB (7577285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe87a91d8723e8bac5bd512c577a4c35923579f053a75af56940a02b604fb775`  
		Last Modified: Thu, 28 Aug 2025 18:40:41 GMT  
		Size: 171.9 MB (171935346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c03d31bb76761e17be10afee6782ff6e78947fa79e295a8d2a3f1f626f841df`  
		Last Modified: Thu, 28 Aug 2025 17:54:41 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77512bf52bfcb5eae03b1e48b59afc8648a9363715a23b2813fcb846dcbc7e5`  
		Last Modified: Thu, 28 Aug 2025 17:54:42 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da12be5d638ee43e262a6162d62702ff8c4f95b6fea366fa9c2d95afb33d7001`  
		Last Modified: Thu, 28 Aug 2025 17:54:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c4efa96760bea1a09199c43903851b8b4c5c8d3bab838dabde5c67c1ac2b2d`  
		Last Modified: Thu, 28 Aug 2025 17:54:42 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3887264c85bbf58061466aad9577404039f58fd7580be096f0bb288e8b480483`  
		Last Modified: Thu, 28 Aug 2025 17:54:42 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9a407fe3edc84eff68792592deeab655212a6d441a9e18ca188792fdd4b46670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e4d81eb5d7b91693ffa4c17eedae9eb13ee61e12c007a3885826783a8f38363`

```dockerfile
```

-	Layers:
	-	`sha256:664cdd35be364a4d5bb090d74f01626feadc11ec4e3c4358d0a9cea8963324e4`  
		Last Modified: Thu, 28 Aug 2025 18:49:41 GMT  
		Size: 26.3 KB (26283 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.7.5`

```console
$ docker pull clickhouse@sha256:1508289214b29246fd35a488d405dea6165b952ab2adf1b0be001bc1cdc42583
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.7.5` - linux; amd64

```console
$ docker pull clickhouse@sha256:f5667c6b06d142244823009828ba9c547f26c7951f3e300abde0d70cc3977c4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.8 MB (221797576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2319e022e1159e0362f694dae9d62c6303f5412b24bbda06d8d3a1f26f87a0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.7.5.34
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0acf31bcca6e9d020dc3cd6cf1a2cf27bdbed95f073afb7c89a998dbef961881`  
		Last Modified: Mon, 01 Sep 2025 23:08:51 GMT  
		Size: 7.6 MB (7598441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3acf2cfb5f58d29d4ed6f0f157dc9e27446f2217744760f800761fbe09f5c75d`  
		Last Modified: Tue, 02 Sep 2025 00:49:59 GMT  
		Size: 183.8 MB (183792178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e433084271857428ea3902ea62c02c1aed622e54938c7323ec2413507c61596`  
		Last Modified: Mon, 01 Sep 2025 23:08:51 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef32936b35234483f20ea9f67542299ebaab52cae3e5a5248295bd75e3885a1`  
		Last Modified: Mon, 01 Sep 2025 23:08:51 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b9fc87ee27c0bb8ea9548795698247b9d25a399ba76225803fce45aff2ea6d`  
		Last Modified: Mon, 01 Sep 2025 23:08:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882143b2addcc1efd237c25fc818844571236a7f37a43213a702b662e3ee8674`  
		Last Modified: Mon, 01 Sep 2025 23:08:53 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85737f8b0e50d3dc6e877a7784ebb8cb187102db8d56f857a0dd231883cc56a2`  
		Last Modified: Mon, 01 Sep 2025 23:08:54 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.5` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3eb2216cf2b9cf5ef7b00f546c313dcee62890da74a8a2325e026a7508485f9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48d49fe7937afdf335fc473758bd0c6dcecd7a36bfe265dcfade8c232bc3082`

```dockerfile
```

-	Layers:
	-	`sha256:87e6d65a8eda12e0b8069b19788123dd91da9fcf4b213e89d6880962f825a54f`  
		Last Modified: Tue, 02 Sep 2025 00:49:47 GMT  
		Size: 26.1 KB (26070 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.7.5` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:ca208d9b17099544c4b0d1625319f7cde591f2c63ad765374b8b33997fa936fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207741903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d171afdf1c548ab261c07c93896a196012d7095ce64d654081d1dcf05f2b735`
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
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.7.5.34
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78dfb031d96f0d6e0220d56775bfbe34690e364e89a1bb14a2448fb489fecde`  
		Last Modified: Thu, 28 Aug 2025 17:54:42 GMT  
		Size: 7.6 MB (7577285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe87a91d8723e8bac5bd512c577a4c35923579f053a75af56940a02b604fb775`  
		Last Modified: Thu, 28 Aug 2025 18:40:41 GMT  
		Size: 171.9 MB (171935346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c03d31bb76761e17be10afee6782ff6e78947fa79e295a8d2a3f1f626f841df`  
		Last Modified: Thu, 28 Aug 2025 17:54:41 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77512bf52bfcb5eae03b1e48b59afc8648a9363715a23b2813fcb846dcbc7e5`  
		Last Modified: Thu, 28 Aug 2025 17:54:42 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da12be5d638ee43e262a6162d62702ff8c4f95b6fea366fa9c2d95afb33d7001`  
		Last Modified: Thu, 28 Aug 2025 17:54:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c4efa96760bea1a09199c43903851b8b4c5c8d3bab838dabde5c67c1ac2b2d`  
		Last Modified: Thu, 28 Aug 2025 17:54:42 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3887264c85bbf58061466aad9577404039f58fd7580be096f0bb288e8b480483`  
		Last Modified: Thu, 28 Aug 2025 17:54:42 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.5` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9a407fe3edc84eff68792592deeab655212a6d441a9e18ca188792fdd4b46670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e4d81eb5d7b91693ffa4c17eedae9eb13ee61e12c007a3885826783a8f38363`

```dockerfile
```

-	Layers:
	-	`sha256:664cdd35be364a4d5bb090d74f01626feadc11ec4e3c4358d0a9cea8963324e4`  
		Last Modified: Thu, 28 Aug 2025 18:49:41 GMT  
		Size: 26.3 KB (26283 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.7.5-jammy`

```console
$ docker pull clickhouse@sha256:1508289214b29246fd35a488d405dea6165b952ab2adf1b0be001bc1cdc42583
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.7.5-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:f5667c6b06d142244823009828ba9c547f26c7951f3e300abde0d70cc3977c4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.8 MB (221797576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2319e022e1159e0362f694dae9d62c6303f5412b24bbda06d8d3a1f26f87a0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.7.5.34
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0acf31bcca6e9d020dc3cd6cf1a2cf27bdbed95f073afb7c89a998dbef961881`  
		Last Modified: Mon, 01 Sep 2025 23:08:51 GMT  
		Size: 7.6 MB (7598441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3acf2cfb5f58d29d4ed6f0f157dc9e27446f2217744760f800761fbe09f5c75d`  
		Last Modified: Tue, 02 Sep 2025 00:49:59 GMT  
		Size: 183.8 MB (183792178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e433084271857428ea3902ea62c02c1aed622e54938c7323ec2413507c61596`  
		Last Modified: Mon, 01 Sep 2025 23:08:51 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef32936b35234483f20ea9f67542299ebaab52cae3e5a5248295bd75e3885a1`  
		Last Modified: Mon, 01 Sep 2025 23:08:51 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b9fc87ee27c0bb8ea9548795698247b9d25a399ba76225803fce45aff2ea6d`  
		Last Modified: Mon, 01 Sep 2025 23:08:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882143b2addcc1efd237c25fc818844571236a7f37a43213a702b662e3ee8674`  
		Last Modified: Mon, 01 Sep 2025 23:08:53 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85737f8b0e50d3dc6e877a7784ebb8cb187102db8d56f857a0dd231883cc56a2`  
		Last Modified: Mon, 01 Sep 2025 23:08:54 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.5-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3eb2216cf2b9cf5ef7b00f546c313dcee62890da74a8a2325e026a7508485f9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48d49fe7937afdf335fc473758bd0c6dcecd7a36bfe265dcfade8c232bc3082`

```dockerfile
```

-	Layers:
	-	`sha256:87e6d65a8eda12e0b8069b19788123dd91da9fcf4b213e89d6880962f825a54f`  
		Last Modified: Tue, 02 Sep 2025 00:49:47 GMT  
		Size: 26.1 KB (26070 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.7.5-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:ca208d9b17099544c4b0d1625319f7cde591f2c63ad765374b8b33997fa936fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207741903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d171afdf1c548ab261c07c93896a196012d7095ce64d654081d1dcf05f2b735`
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
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.7.5.34
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78dfb031d96f0d6e0220d56775bfbe34690e364e89a1bb14a2448fb489fecde`  
		Last Modified: Thu, 28 Aug 2025 17:54:42 GMT  
		Size: 7.6 MB (7577285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe87a91d8723e8bac5bd512c577a4c35923579f053a75af56940a02b604fb775`  
		Last Modified: Thu, 28 Aug 2025 18:40:41 GMT  
		Size: 171.9 MB (171935346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c03d31bb76761e17be10afee6782ff6e78947fa79e295a8d2a3f1f626f841df`  
		Last Modified: Thu, 28 Aug 2025 17:54:41 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77512bf52bfcb5eae03b1e48b59afc8648a9363715a23b2813fcb846dcbc7e5`  
		Last Modified: Thu, 28 Aug 2025 17:54:42 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da12be5d638ee43e262a6162d62702ff8c4f95b6fea366fa9c2d95afb33d7001`  
		Last Modified: Thu, 28 Aug 2025 17:54:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c4efa96760bea1a09199c43903851b8b4c5c8d3bab838dabde5c67c1ac2b2d`  
		Last Modified: Thu, 28 Aug 2025 17:54:42 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3887264c85bbf58061466aad9577404039f58fd7580be096f0bb288e8b480483`  
		Last Modified: Thu, 28 Aug 2025 17:54:42 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.5-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9a407fe3edc84eff68792592deeab655212a6d441a9e18ca188792fdd4b46670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e4d81eb5d7b91693ffa4c17eedae9eb13ee61e12c007a3885826783a8f38363`

```dockerfile
```

-	Layers:
	-	`sha256:664cdd35be364a4d5bb090d74f01626feadc11ec4e3c4358d0a9cea8963324e4`  
		Last Modified: Thu, 28 Aug 2025 18:49:41 GMT  
		Size: 26.3 KB (26283 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.7.5.34`

```console
$ docker pull clickhouse@sha256:1508289214b29246fd35a488d405dea6165b952ab2adf1b0be001bc1cdc42583
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.7.5.34` - linux; amd64

```console
$ docker pull clickhouse@sha256:f5667c6b06d142244823009828ba9c547f26c7951f3e300abde0d70cc3977c4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.8 MB (221797576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2319e022e1159e0362f694dae9d62c6303f5412b24bbda06d8d3a1f26f87a0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.7.5.34
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0acf31bcca6e9d020dc3cd6cf1a2cf27bdbed95f073afb7c89a998dbef961881`  
		Last Modified: Mon, 01 Sep 2025 23:08:51 GMT  
		Size: 7.6 MB (7598441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3acf2cfb5f58d29d4ed6f0f157dc9e27446f2217744760f800761fbe09f5c75d`  
		Last Modified: Tue, 02 Sep 2025 00:49:59 GMT  
		Size: 183.8 MB (183792178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e433084271857428ea3902ea62c02c1aed622e54938c7323ec2413507c61596`  
		Last Modified: Mon, 01 Sep 2025 23:08:51 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef32936b35234483f20ea9f67542299ebaab52cae3e5a5248295bd75e3885a1`  
		Last Modified: Mon, 01 Sep 2025 23:08:51 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b9fc87ee27c0bb8ea9548795698247b9d25a399ba76225803fce45aff2ea6d`  
		Last Modified: Mon, 01 Sep 2025 23:08:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882143b2addcc1efd237c25fc818844571236a7f37a43213a702b662e3ee8674`  
		Last Modified: Mon, 01 Sep 2025 23:08:53 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85737f8b0e50d3dc6e877a7784ebb8cb187102db8d56f857a0dd231883cc56a2`  
		Last Modified: Mon, 01 Sep 2025 23:08:54 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.5.34` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3eb2216cf2b9cf5ef7b00f546c313dcee62890da74a8a2325e026a7508485f9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48d49fe7937afdf335fc473758bd0c6dcecd7a36bfe265dcfade8c232bc3082`

```dockerfile
```

-	Layers:
	-	`sha256:87e6d65a8eda12e0b8069b19788123dd91da9fcf4b213e89d6880962f825a54f`  
		Last Modified: Tue, 02 Sep 2025 00:49:47 GMT  
		Size: 26.1 KB (26070 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.7.5.34` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:ca208d9b17099544c4b0d1625319f7cde591f2c63ad765374b8b33997fa936fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207741903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d171afdf1c548ab261c07c93896a196012d7095ce64d654081d1dcf05f2b735`
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
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.7.5.34
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78dfb031d96f0d6e0220d56775bfbe34690e364e89a1bb14a2448fb489fecde`  
		Last Modified: Thu, 28 Aug 2025 17:54:42 GMT  
		Size: 7.6 MB (7577285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe87a91d8723e8bac5bd512c577a4c35923579f053a75af56940a02b604fb775`  
		Last Modified: Thu, 28 Aug 2025 18:40:41 GMT  
		Size: 171.9 MB (171935346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c03d31bb76761e17be10afee6782ff6e78947fa79e295a8d2a3f1f626f841df`  
		Last Modified: Thu, 28 Aug 2025 17:54:41 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77512bf52bfcb5eae03b1e48b59afc8648a9363715a23b2813fcb846dcbc7e5`  
		Last Modified: Thu, 28 Aug 2025 17:54:42 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da12be5d638ee43e262a6162d62702ff8c4f95b6fea366fa9c2d95afb33d7001`  
		Last Modified: Thu, 28 Aug 2025 17:54:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c4efa96760bea1a09199c43903851b8b4c5c8d3bab838dabde5c67c1ac2b2d`  
		Last Modified: Thu, 28 Aug 2025 17:54:42 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3887264c85bbf58061466aad9577404039f58fd7580be096f0bb288e8b480483`  
		Last Modified: Thu, 28 Aug 2025 17:54:42 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.5.34` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9a407fe3edc84eff68792592deeab655212a6d441a9e18ca188792fdd4b46670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e4d81eb5d7b91693ffa4c17eedae9eb13ee61e12c007a3885826783a8f38363`

```dockerfile
```

-	Layers:
	-	`sha256:664cdd35be364a4d5bb090d74f01626feadc11ec4e3c4358d0a9cea8963324e4`  
		Last Modified: Thu, 28 Aug 2025 18:49:41 GMT  
		Size: 26.3 KB (26283 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.7.5.34-jammy`

```console
$ docker pull clickhouse@sha256:1508289214b29246fd35a488d405dea6165b952ab2adf1b0be001bc1cdc42583
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.7.5.34-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:f5667c6b06d142244823009828ba9c547f26c7951f3e300abde0d70cc3977c4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.8 MB (221797576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2319e022e1159e0362f694dae9d62c6303f5412b24bbda06d8d3a1f26f87a0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.7.5.34
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0acf31bcca6e9d020dc3cd6cf1a2cf27bdbed95f073afb7c89a998dbef961881`  
		Last Modified: Mon, 01 Sep 2025 23:08:51 GMT  
		Size: 7.6 MB (7598441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3acf2cfb5f58d29d4ed6f0f157dc9e27446f2217744760f800761fbe09f5c75d`  
		Last Modified: Tue, 02 Sep 2025 00:49:59 GMT  
		Size: 183.8 MB (183792178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e433084271857428ea3902ea62c02c1aed622e54938c7323ec2413507c61596`  
		Last Modified: Mon, 01 Sep 2025 23:08:51 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef32936b35234483f20ea9f67542299ebaab52cae3e5a5248295bd75e3885a1`  
		Last Modified: Mon, 01 Sep 2025 23:08:51 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b9fc87ee27c0bb8ea9548795698247b9d25a399ba76225803fce45aff2ea6d`  
		Last Modified: Mon, 01 Sep 2025 23:08:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882143b2addcc1efd237c25fc818844571236a7f37a43213a702b662e3ee8674`  
		Last Modified: Mon, 01 Sep 2025 23:08:53 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85737f8b0e50d3dc6e877a7784ebb8cb187102db8d56f857a0dd231883cc56a2`  
		Last Modified: Mon, 01 Sep 2025 23:08:54 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.5.34-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3eb2216cf2b9cf5ef7b00f546c313dcee62890da74a8a2325e026a7508485f9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48d49fe7937afdf335fc473758bd0c6dcecd7a36bfe265dcfade8c232bc3082`

```dockerfile
```

-	Layers:
	-	`sha256:87e6d65a8eda12e0b8069b19788123dd91da9fcf4b213e89d6880962f825a54f`  
		Last Modified: Tue, 02 Sep 2025 00:49:47 GMT  
		Size: 26.1 KB (26070 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.7.5.34-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:ca208d9b17099544c4b0d1625319f7cde591f2c63ad765374b8b33997fa936fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207741903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d171afdf1c548ab261c07c93896a196012d7095ce64d654081d1dcf05f2b735`
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
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.7.5.34
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78dfb031d96f0d6e0220d56775bfbe34690e364e89a1bb14a2448fb489fecde`  
		Last Modified: Thu, 28 Aug 2025 17:54:42 GMT  
		Size: 7.6 MB (7577285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe87a91d8723e8bac5bd512c577a4c35923579f053a75af56940a02b604fb775`  
		Last Modified: Thu, 28 Aug 2025 18:40:41 GMT  
		Size: 171.9 MB (171935346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c03d31bb76761e17be10afee6782ff6e78947fa79e295a8d2a3f1f626f841df`  
		Last Modified: Thu, 28 Aug 2025 17:54:41 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77512bf52bfcb5eae03b1e48b59afc8648a9363715a23b2813fcb846dcbc7e5`  
		Last Modified: Thu, 28 Aug 2025 17:54:42 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da12be5d638ee43e262a6162d62702ff8c4f95b6fea366fa9c2d95afb33d7001`  
		Last Modified: Thu, 28 Aug 2025 17:54:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c4efa96760bea1a09199c43903851b8b4c5c8d3bab838dabde5c67c1ac2b2d`  
		Last Modified: Thu, 28 Aug 2025 17:54:42 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3887264c85bbf58061466aad9577404039f58fd7580be096f0bb288e8b480483`  
		Last Modified: Thu, 28 Aug 2025 17:54:42 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.5.34-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9a407fe3edc84eff68792592deeab655212a6d441a9e18ca188792fdd4b46670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e4d81eb5d7b91693ffa4c17eedae9eb13ee61e12c007a3885826783a8f38363`

```dockerfile
```

-	Layers:
	-	`sha256:664cdd35be364a4d5bb090d74f01626feadc11ec4e3c4358d0a9cea8963324e4`  
		Last Modified: Thu, 28 Aug 2025 18:49:41 GMT  
		Size: 26.3 KB (26283 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:jammy`

```console
$ docker pull clickhouse@sha256:1508289214b29246fd35a488d405dea6165b952ab2adf1b0be001bc1cdc42583
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:f5667c6b06d142244823009828ba9c547f26c7951f3e300abde0d70cc3977c4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.8 MB (221797576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2319e022e1159e0362f694dae9d62c6303f5412b24bbda06d8d3a1f26f87a0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.7.5.34
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0acf31bcca6e9d020dc3cd6cf1a2cf27bdbed95f073afb7c89a998dbef961881`  
		Last Modified: Mon, 01 Sep 2025 23:08:51 GMT  
		Size: 7.6 MB (7598441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3acf2cfb5f58d29d4ed6f0f157dc9e27446f2217744760f800761fbe09f5c75d`  
		Last Modified: Tue, 02 Sep 2025 00:49:59 GMT  
		Size: 183.8 MB (183792178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e433084271857428ea3902ea62c02c1aed622e54938c7323ec2413507c61596`  
		Last Modified: Mon, 01 Sep 2025 23:08:51 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef32936b35234483f20ea9f67542299ebaab52cae3e5a5248295bd75e3885a1`  
		Last Modified: Mon, 01 Sep 2025 23:08:51 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b9fc87ee27c0bb8ea9548795698247b9d25a399ba76225803fce45aff2ea6d`  
		Last Modified: Mon, 01 Sep 2025 23:08:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882143b2addcc1efd237c25fc818844571236a7f37a43213a702b662e3ee8674`  
		Last Modified: Mon, 01 Sep 2025 23:08:53 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85737f8b0e50d3dc6e877a7784ebb8cb187102db8d56f857a0dd231883cc56a2`  
		Last Modified: Mon, 01 Sep 2025 23:08:54 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3eb2216cf2b9cf5ef7b00f546c313dcee62890da74a8a2325e026a7508485f9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48d49fe7937afdf335fc473758bd0c6dcecd7a36bfe265dcfade8c232bc3082`

```dockerfile
```

-	Layers:
	-	`sha256:87e6d65a8eda12e0b8069b19788123dd91da9fcf4b213e89d6880962f825a54f`  
		Last Modified: Tue, 02 Sep 2025 00:49:47 GMT  
		Size: 26.1 KB (26070 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:ca208d9b17099544c4b0d1625319f7cde591f2c63ad765374b8b33997fa936fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207741903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d171afdf1c548ab261c07c93896a196012d7095ce64d654081d1dcf05f2b735`
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
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.7.5.34
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78dfb031d96f0d6e0220d56775bfbe34690e364e89a1bb14a2448fb489fecde`  
		Last Modified: Thu, 28 Aug 2025 17:54:42 GMT  
		Size: 7.6 MB (7577285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe87a91d8723e8bac5bd512c577a4c35923579f053a75af56940a02b604fb775`  
		Last Modified: Thu, 28 Aug 2025 18:40:41 GMT  
		Size: 171.9 MB (171935346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c03d31bb76761e17be10afee6782ff6e78947fa79e295a8d2a3f1f626f841df`  
		Last Modified: Thu, 28 Aug 2025 17:54:41 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77512bf52bfcb5eae03b1e48b59afc8648a9363715a23b2813fcb846dcbc7e5`  
		Last Modified: Thu, 28 Aug 2025 17:54:42 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da12be5d638ee43e262a6162d62702ff8c4f95b6fea366fa9c2d95afb33d7001`  
		Last Modified: Thu, 28 Aug 2025 17:54:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c4efa96760bea1a09199c43903851b8b4c5c8d3bab838dabde5c67c1ac2b2d`  
		Last Modified: Thu, 28 Aug 2025 17:54:42 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3887264c85bbf58061466aad9577404039f58fd7580be096f0bb288e8b480483`  
		Last Modified: Thu, 28 Aug 2025 17:54:42 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9a407fe3edc84eff68792592deeab655212a6d441a9e18ca188792fdd4b46670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e4d81eb5d7b91693ffa4c17eedae9eb13ee61e12c007a3885826783a8f38363`

```dockerfile
```

-	Layers:
	-	`sha256:664cdd35be364a4d5bb090d74f01626feadc11ec4e3c4358d0a9cea8963324e4`  
		Last Modified: Thu, 28 Aug 2025 18:49:41 GMT  
		Size: 26.3 KB (26283 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:1508289214b29246fd35a488d405dea6165b952ab2adf1b0be001bc1cdc42583
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

```console
$ docker pull clickhouse@sha256:f5667c6b06d142244823009828ba9c547f26c7951f3e300abde0d70cc3977c4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.8 MB (221797576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2319e022e1159e0362f694dae9d62c6303f5412b24bbda06d8d3a1f26f87a0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.7.5.34
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0acf31bcca6e9d020dc3cd6cf1a2cf27bdbed95f073afb7c89a998dbef961881`  
		Last Modified: Mon, 01 Sep 2025 23:08:51 GMT  
		Size: 7.6 MB (7598441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3acf2cfb5f58d29d4ed6f0f157dc9e27446f2217744760f800761fbe09f5c75d`  
		Last Modified: Tue, 02 Sep 2025 00:49:59 GMT  
		Size: 183.8 MB (183792178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e433084271857428ea3902ea62c02c1aed622e54938c7323ec2413507c61596`  
		Last Modified: Mon, 01 Sep 2025 23:08:51 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef32936b35234483f20ea9f67542299ebaab52cae3e5a5248295bd75e3885a1`  
		Last Modified: Mon, 01 Sep 2025 23:08:51 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b9fc87ee27c0bb8ea9548795698247b9d25a399ba76225803fce45aff2ea6d`  
		Last Modified: Mon, 01 Sep 2025 23:08:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882143b2addcc1efd237c25fc818844571236a7f37a43213a702b662e3ee8674`  
		Last Modified: Mon, 01 Sep 2025 23:08:53 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85737f8b0e50d3dc6e877a7784ebb8cb187102db8d56f857a0dd231883cc56a2`  
		Last Modified: Mon, 01 Sep 2025 23:08:54 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3eb2216cf2b9cf5ef7b00f546c313dcee62890da74a8a2325e026a7508485f9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48d49fe7937afdf335fc473758bd0c6dcecd7a36bfe265dcfade8c232bc3082`

```dockerfile
```

-	Layers:
	-	`sha256:87e6d65a8eda12e0b8069b19788123dd91da9fcf4b213e89d6880962f825a54f`  
		Last Modified: Tue, 02 Sep 2025 00:49:47 GMT  
		Size: 26.1 KB (26070 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:ca208d9b17099544c4b0d1625319f7cde591f2c63ad765374b8b33997fa936fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207741903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d171afdf1c548ab261c07c93896a196012d7095ce64d654081d1dcf05f2b735`
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
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.7.5.34
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.5.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78dfb031d96f0d6e0220d56775bfbe34690e364e89a1bb14a2448fb489fecde`  
		Last Modified: Thu, 28 Aug 2025 17:54:42 GMT  
		Size: 7.6 MB (7577285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe87a91d8723e8bac5bd512c577a4c35923579f053a75af56940a02b604fb775`  
		Last Modified: Thu, 28 Aug 2025 18:40:41 GMT  
		Size: 171.9 MB (171935346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c03d31bb76761e17be10afee6782ff6e78947fa79e295a8d2a3f1f626f841df`  
		Last Modified: Thu, 28 Aug 2025 17:54:41 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77512bf52bfcb5eae03b1e48b59afc8648a9363715a23b2813fcb846dcbc7e5`  
		Last Modified: Thu, 28 Aug 2025 17:54:42 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da12be5d638ee43e262a6162d62702ff8c4f95b6fea366fa9c2d95afb33d7001`  
		Last Modified: Thu, 28 Aug 2025 17:54:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c4efa96760bea1a09199c43903851b8b4c5c8d3bab838dabde5c67c1ac2b2d`  
		Last Modified: Thu, 28 Aug 2025 17:54:42 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3887264c85bbf58061466aad9577404039f58fd7580be096f0bb288e8b480483`  
		Last Modified: Thu, 28 Aug 2025 17:54:42 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9a407fe3edc84eff68792592deeab655212a6d441a9e18ca188792fdd4b46670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e4d81eb5d7b91693ffa4c17eedae9eb13ee61e12c007a3885826783a8f38363`

```dockerfile
```

-	Layers:
	-	`sha256:664cdd35be364a4d5bb090d74f01626feadc11ec4e3c4358d0a9cea8963324e4`  
		Last Modified: Thu, 28 Aug 2025 18:49:41 GMT  
		Size: 26.3 KB (26283 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts`

```console
$ docker pull clickhouse@sha256:897f6727996c2c6bf768e44b56627dc3fcf2215daa0aecee3d49f5c1d34f0349
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts` - linux; amd64

```console
$ docker pull clickhouse@sha256:79c0f0ba61b5a5f7284a10e9f671ccfeab8e445cca58929d14d9b5c30de86d20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.4 MB (205432385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db22b7ed486ee977ad64ddca75012fb3118be31681443b2941bb0c0809c3fb5`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.3.6.56
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28b8b64bfc3c006da3dbdc8315726047223dc83bf809ec568a01a6282bb7c6d`  
		Last Modified: Mon, 01 Sep 2025 23:09:02 GMT  
		Size: 7.2 MB (7151643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3063f406083ccf1f853493cc1903b17828299758cc838c0ae3ff5a1ab038e53a`  
		Last Modified: Tue, 02 Sep 2025 00:49:44 GMT  
		Size: 167.9 MB (167873557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068524848a39bc20273deb9c815010922e604f57cae4d762fe4a110be010b7cc`  
		Last Modified: Mon, 01 Sep 2025 23:09:01 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bbfcd3b5b7985fa5315ff6a50d0e8302ff1ef18dc6ebe4087c197fd26b8483`  
		Last Modified: Mon, 01 Sep 2025 23:09:02 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce48062e0dad3ffc672b574bd49b5254c21bc836e2cd928d35697d45107fa99`  
		Last Modified: Mon, 01 Sep 2025 23:09:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a239040b253b9101ca6a52d9fdf17f703d4d539ea63f832e9295ac84a2eeecb0`  
		Last Modified: Mon, 01 Sep 2025 23:09:03 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ef3f7692f6964082a0ebad321915d0eab0f8f6e4c8c320b008376823e6fd63`  
		Last Modified: Mon, 01 Sep 2025 23:09:03 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:50a83551816610e25f1c81d2c2b78c69e6ab1bffca8651469526761dce29669a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:759649216f9edd7c53fc693d5297c37eb1089638406f26eb7694ea6961951a21`

```dockerfile
```

-	Layers:
	-	`sha256:c307d95fe108fe4572dfab6fbe5f75fa0d6ac491733f5cb90e7aaaab019461b2`  
		Last Modified: Tue, 02 Sep 2025 00:49:19 GMT  
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
$ docker pull clickhouse@sha256:897f6727996c2c6bf768e44b56627dc3fcf2215daa0aecee3d49f5c1d34f0349
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:79c0f0ba61b5a5f7284a10e9f671ccfeab8e445cca58929d14d9b5c30de86d20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.4 MB (205432385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db22b7ed486ee977ad64ddca75012fb3118be31681443b2941bb0c0809c3fb5`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.3.6.56
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28b8b64bfc3c006da3dbdc8315726047223dc83bf809ec568a01a6282bb7c6d`  
		Last Modified: Mon, 01 Sep 2025 23:09:02 GMT  
		Size: 7.2 MB (7151643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3063f406083ccf1f853493cc1903b17828299758cc838c0ae3ff5a1ab038e53a`  
		Last Modified: Tue, 02 Sep 2025 00:49:44 GMT  
		Size: 167.9 MB (167873557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068524848a39bc20273deb9c815010922e604f57cae4d762fe4a110be010b7cc`  
		Last Modified: Mon, 01 Sep 2025 23:09:01 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bbfcd3b5b7985fa5315ff6a50d0e8302ff1ef18dc6ebe4087c197fd26b8483`  
		Last Modified: Mon, 01 Sep 2025 23:09:02 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce48062e0dad3ffc672b574bd49b5254c21bc836e2cd928d35697d45107fa99`  
		Last Modified: Mon, 01 Sep 2025 23:09:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a239040b253b9101ca6a52d9fdf17f703d4d539ea63f832e9295ac84a2eeecb0`  
		Last Modified: Mon, 01 Sep 2025 23:09:03 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ef3f7692f6964082a0ebad321915d0eab0f8f6e4c8c320b008376823e6fd63`  
		Last Modified: Mon, 01 Sep 2025 23:09:03 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:50a83551816610e25f1c81d2c2b78c69e6ab1bffca8651469526761dce29669a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:759649216f9edd7c53fc693d5297c37eb1089638406f26eb7694ea6961951a21`

```dockerfile
```

-	Layers:
	-	`sha256:c307d95fe108fe4572dfab6fbe5f75fa0d6ac491733f5cb90e7aaaab019461b2`  
		Last Modified: Tue, 02 Sep 2025 00:49:19 GMT  
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
