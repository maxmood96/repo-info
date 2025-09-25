<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clickhouse`

-	[`clickhouse:25.3`](#clickhouse253)
-	[`clickhouse:25.3-jammy`](#clickhouse253-jammy)
-	[`clickhouse:25.3.6`](#clickhouse2536)
-	[`clickhouse:25.3.6-jammy`](#clickhouse2536-jammy)
-	[`clickhouse:25.3.6.56`](#clickhouse253656)
-	[`clickhouse:25.3.6.56-jammy`](#clickhouse253656-jammy)
-	[`clickhouse:25.6`](#clickhouse256)
-	[`clickhouse:25.6-jammy`](#clickhouse256-jammy)
-	[`clickhouse:25.6.12`](#clickhouse25612)
-	[`clickhouse:25.6.12-jammy`](#clickhouse25612-jammy)
-	[`clickhouse:25.6.12.10`](#clickhouse2561210)
-	[`clickhouse:25.6.12.10-jammy`](#clickhouse2561210-jammy)
-	[`clickhouse:25.7`](#clickhouse257)
-	[`clickhouse:25.7-jammy`](#clickhouse257-jammy)
-	[`clickhouse:25.7.7`](#clickhouse2577)
-	[`clickhouse:25.7.7-jammy`](#clickhouse2577-jammy)
-	[`clickhouse:25.7.7.68`](#clickhouse257768)
-	[`clickhouse:25.7.7.68-jammy`](#clickhouse257768-jammy)
-	[`clickhouse:25.8`](#clickhouse258)
-	[`clickhouse:25.8-jammy`](#clickhouse258-jammy)
-	[`clickhouse:25.8.7`](#clickhouse2587)
-	[`clickhouse:25.8.7-jammy`](#clickhouse2587-jammy)
-	[`clickhouse:25.8.7.3`](#clickhouse25873)
-	[`clickhouse:25.8.7.3-jammy`](#clickhouse25873-jammy)
-	[`clickhouse:jammy`](#clickhousejammy)
-	[`clickhouse:latest`](#clickhouselatest)
-	[`clickhouse:lts`](#clickhouselts)
-	[`clickhouse:lts-jammy`](#clickhouselts-jammy)

## `clickhouse:25.3`

```console
$ docker pull clickhouse@sha256:5b7a561f01ffef2778b62a98ad3240597c9b1221054b4d823e887a357fca199d
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
$ docker pull clickhouse@sha256:d892e915e75c821583672c3d6b896fd7b2f717f458baf44bb362e49c65f1309b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192914616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e58685f5bdad3ba0bc7c8de0469d6b6350387638f0ad3518c7884e93f149081`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:17 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:19 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 17:21:19 GMT
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
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53bc80260a87d75c26106a8275097885b20843146fe1e6fd837e6af8a5771e9`  
		Last Modified: Tue, 02 Sep 2025 01:21:51 GMT  
		Size: 7.1 MB (7127944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90841967e872576c42e5dbade007e13c3f6bbb85568b8f46a497eb3f8a79ac7c`  
		Last Modified: Tue, 02 Sep 2025 03:49:34 GMT  
		Size: 157.6 MB (157554955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b9912743e22819a39e458cd6a730c7b339aef5ae6dd062c9581c0a0864f9f8`  
		Last Modified: Tue, 02 Sep 2025 00:18:09 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1213c0adac33fc6f8efee9d181b43d6051f12d9d0d5244fe6d539a6943c57d41`  
		Last Modified: Tue, 02 Sep 2025 00:18:12 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580eb6bfefd035d79b25f94ea56f4f3b900f25188fe3646390a360b5e80e0339`  
		Last Modified: Tue, 02 Sep 2025 00:18:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6f506816a234fa7168b5864702486c71eb36cb721f2c4eece208a8b057913e`  
		Last Modified: Tue, 02 Sep 2025 00:18:12 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6ed03564cfdcb75cbaa37f1f375a2fed1b6773e070d7f2abd20a3bc3f35784`  
		Last Modified: Tue, 02 Sep 2025 00:18:13 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:7cd2f404c27c665053aed069feb733b79e882fde09a25bff13117d287f586b28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69efeac22341fe15c4f4eae6fd9d0e2bc4eac00d04ea26ac6f0e94f405f18e6c`

```dockerfile
```

-	Layers:
	-	`sha256:88f4c4fd85cb13450eae1a2293511e3b55f142d5e0c8c060e85251e12547649b`  
		Last Modified: Tue, 02 Sep 2025 03:49:18 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3-jammy`

```console
$ docker pull clickhouse@sha256:5b7a561f01ffef2778b62a98ad3240597c9b1221054b4d823e887a357fca199d
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
$ docker pull clickhouse@sha256:d892e915e75c821583672c3d6b896fd7b2f717f458baf44bb362e49c65f1309b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192914616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e58685f5bdad3ba0bc7c8de0469d6b6350387638f0ad3518c7884e93f149081`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:17 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:19 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 17:21:19 GMT
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
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53bc80260a87d75c26106a8275097885b20843146fe1e6fd837e6af8a5771e9`  
		Last Modified: Tue, 02 Sep 2025 01:21:51 GMT  
		Size: 7.1 MB (7127944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90841967e872576c42e5dbade007e13c3f6bbb85568b8f46a497eb3f8a79ac7c`  
		Last Modified: Tue, 02 Sep 2025 03:49:34 GMT  
		Size: 157.6 MB (157554955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b9912743e22819a39e458cd6a730c7b339aef5ae6dd062c9581c0a0864f9f8`  
		Last Modified: Tue, 02 Sep 2025 00:18:09 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1213c0adac33fc6f8efee9d181b43d6051f12d9d0d5244fe6d539a6943c57d41`  
		Last Modified: Tue, 02 Sep 2025 00:18:12 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580eb6bfefd035d79b25f94ea56f4f3b900f25188fe3646390a360b5e80e0339`  
		Last Modified: Tue, 02 Sep 2025 00:18:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6f506816a234fa7168b5864702486c71eb36cb721f2c4eece208a8b057913e`  
		Last Modified: Tue, 02 Sep 2025 00:18:12 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6ed03564cfdcb75cbaa37f1f375a2fed1b6773e070d7f2abd20a3bc3f35784`  
		Last Modified: Tue, 02 Sep 2025 00:18:13 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:7cd2f404c27c665053aed069feb733b79e882fde09a25bff13117d287f586b28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69efeac22341fe15c4f4eae6fd9d0e2bc4eac00d04ea26ac6f0e94f405f18e6c`

```dockerfile
```

-	Layers:
	-	`sha256:88f4c4fd85cb13450eae1a2293511e3b55f142d5e0c8c060e85251e12547649b`  
		Last Modified: Tue, 02 Sep 2025 03:49:18 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.6`

```console
$ docker pull clickhouse@sha256:5b7a561f01ffef2778b62a98ad3240597c9b1221054b4d823e887a357fca199d
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
$ docker pull clickhouse@sha256:d892e915e75c821583672c3d6b896fd7b2f717f458baf44bb362e49c65f1309b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192914616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e58685f5bdad3ba0bc7c8de0469d6b6350387638f0ad3518c7884e93f149081`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:17 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:19 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 17:21:19 GMT
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
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53bc80260a87d75c26106a8275097885b20843146fe1e6fd837e6af8a5771e9`  
		Last Modified: Tue, 02 Sep 2025 01:21:51 GMT  
		Size: 7.1 MB (7127944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90841967e872576c42e5dbade007e13c3f6bbb85568b8f46a497eb3f8a79ac7c`  
		Last Modified: Tue, 02 Sep 2025 03:49:34 GMT  
		Size: 157.6 MB (157554955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b9912743e22819a39e458cd6a730c7b339aef5ae6dd062c9581c0a0864f9f8`  
		Last Modified: Tue, 02 Sep 2025 00:18:09 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1213c0adac33fc6f8efee9d181b43d6051f12d9d0d5244fe6d539a6943c57d41`  
		Last Modified: Tue, 02 Sep 2025 00:18:12 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580eb6bfefd035d79b25f94ea56f4f3b900f25188fe3646390a360b5e80e0339`  
		Last Modified: Tue, 02 Sep 2025 00:18:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6f506816a234fa7168b5864702486c71eb36cb721f2c4eece208a8b057913e`  
		Last Modified: Tue, 02 Sep 2025 00:18:12 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6ed03564cfdcb75cbaa37f1f375a2fed1b6773e070d7f2abd20a3bc3f35784`  
		Last Modified: Tue, 02 Sep 2025 00:18:13 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.6` - unknown; unknown

```console
$ docker pull clickhouse@sha256:7cd2f404c27c665053aed069feb733b79e882fde09a25bff13117d287f586b28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69efeac22341fe15c4f4eae6fd9d0e2bc4eac00d04ea26ac6f0e94f405f18e6c`

```dockerfile
```

-	Layers:
	-	`sha256:88f4c4fd85cb13450eae1a2293511e3b55f142d5e0c8c060e85251e12547649b`  
		Last Modified: Tue, 02 Sep 2025 03:49:18 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.6-jammy`

```console
$ docker pull clickhouse@sha256:5b7a561f01ffef2778b62a98ad3240597c9b1221054b4d823e887a357fca199d
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
$ docker pull clickhouse@sha256:d892e915e75c821583672c3d6b896fd7b2f717f458baf44bb362e49c65f1309b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192914616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e58685f5bdad3ba0bc7c8de0469d6b6350387638f0ad3518c7884e93f149081`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:17 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:19 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 17:21:19 GMT
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
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53bc80260a87d75c26106a8275097885b20843146fe1e6fd837e6af8a5771e9`  
		Last Modified: Tue, 02 Sep 2025 01:21:51 GMT  
		Size: 7.1 MB (7127944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90841967e872576c42e5dbade007e13c3f6bbb85568b8f46a497eb3f8a79ac7c`  
		Last Modified: Tue, 02 Sep 2025 03:49:34 GMT  
		Size: 157.6 MB (157554955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b9912743e22819a39e458cd6a730c7b339aef5ae6dd062c9581c0a0864f9f8`  
		Last Modified: Tue, 02 Sep 2025 00:18:09 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1213c0adac33fc6f8efee9d181b43d6051f12d9d0d5244fe6d539a6943c57d41`  
		Last Modified: Tue, 02 Sep 2025 00:18:12 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580eb6bfefd035d79b25f94ea56f4f3b900f25188fe3646390a360b5e80e0339`  
		Last Modified: Tue, 02 Sep 2025 00:18:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6f506816a234fa7168b5864702486c71eb36cb721f2c4eece208a8b057913e`  
		Last Modified: Tue, 02 Sep 2025 00:18:12 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6ed03564cfdcb75cbaa37f1f375a2fed1b6773e070d7f2abd20a3bc3f35784`  
		Last Modified: Tue, 02 Sep 2025 00:18:13 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.6-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:7cd2f404c27c665053aed069feb733b79e882fde09a25bff13117d287f586b28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69efeac22341fe15c4f4eae6fd9d0e2bc4eac00d04ea26ac6f0e94f405f18e6c`

```dockerfile
```

-	Layers:
	-	`sha256:88f4c4fd85cb13450eae1a2293511e3b55f142d5e0c8c060e85251e12547649b`  
		Last Modified: Tue, 02 Sep 2025 03:49:18 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.6.56`

```console
$ docker pull clickhouse@sha256:5b7a561f01ffef2778b62a98ad3240597c9b1221054b4d823e887a357fca199d
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
$ docker pull clickhouse@sha256:d892e915e75c821583672c3d6b896fd7b2f717f458baf44bb362e49c65f1309b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192914616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e58685f5bdad3ba0bc7c8de0469d6b6350387638f0ad3518c7884e93f149081`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:17 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:19 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 17:21:19 GMT
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
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53bc80260a87d75c26106a8275097885b20843146fe1e6fd837e6af8a5771e9`  
		Last Modified: Tue, 02 Sep 2025 01:21:51 GMT  
		Size: 7.1 MB (7127944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90841967e872576c42e5dbade007e13c3f6bbb85568b8f46a497eb3f8a79ac7c`  
		Last Modified: Tue, 02 Sep 2025 03:49:34 GMT  
		Size: 157.6 MB (157554955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b9912743e22819a39e458cd6a730c7b339aef5ae6dd062c9581c0a0864f9f8`  
		Last Modified: Tue, 02 Sep 2025 00:18:09 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1213c0adac33fc6f8efee9d181b43d6051f12d9d0d5244fe6d539a6943c57d41`  
		Last Modified: Tue, 02 Sep 2025 00:18:12 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580eb6bfefd035d79b25f94ea56f4f3b900f25188fe3646390a360b5e80e0339`  
		Last Modified: Tue, 02 Sep 2025 00:18:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6f506816a234fa7168b5864702486c71eb36cb721f2c4eece208a8b057913e`  
		Last Modified: Tue, 02 Sep 2025 00:18:12 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6ed03564cfdcb75cbaa37f1f375a2fed1b6773e070d7f2abd20a3bc3f35784`  
		Last Modified: Tue, 02 Sep 2025 00:18:13 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.6.56` - unknown; unknown

```console
$ docker pull clickhouse@sha256:7cd2f404c27c665053aed069feb733b79e882fde09a25bff13117d287f586b28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69efeac22341fe15c4f4eae6fd9d0e2bc4eac00d04ea26ac6f0e94f405f18e6c`

```dockerfile
```

-	Layers:
	-	`sha256:88f4c4fd85cb13450eae1a2293511e3b55f142d5e0c8c060e85251e12547649b`  
		Last Modified: Tue, 02 Sep 2025 03:49:18 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.6.56-jammy`

```console
$ docker pull clickhouse@sha256:5b7a561f01ffef2778b62a98ad3240597c9b1221054b4d823e887a357fca199d
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
$ docker pull clickhouse@sha256:d892e915e75c821583672c3d6b896fd7b2f717f458baf44bb362e49c65f1309b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192914616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e58685f5bdad3ba0bc7c8de0469d6b6350387638f0ad3518c7884e93f149081`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:17 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:19 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 17:21:19 GMT
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
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53bc80260a87d75c26106a8275097885b20843146fe1e6fd837e6af8a5771e9`  
		Last Modified: Tue, 02 Sep 2025 01:21:51 GMT  
		Size: 7.1 MB (7127944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90841967e872576c42e5dbade007e13c3f6bbb85568b8f46a497eb3f8a79ac7c`  
		Last Modified: Tue, 02 Sep 2025 03:49:34 GMT  
		Size: 157.6 MB (157554955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b9912743e22819a39e458cd6a730c7b339aef5ae6dd062c9581c0a0864f9f8`  
		Last Modified: Tue, 02 Sep 2025 00:18:09 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1213c0adac33fc6f8efee9d181b43d6051f12d9d0d5244fe6d539a6943c57d41`  
		Last Modified: Tue, 02 Sep 2025 00:18:12 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580eb6bfefd035d79b25f94ea56f4f3b900f25188fe3646390a360b5e80e0339`  
		Last Modified: Tue, 02 Sep 2025 00:18:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6f506816a234fa7168b5864702486c71eb36cb721f2c4eece208a8b057913e`  
		Last Modified: Tue, 02 Sep 2025 00:18:12 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6ed03564cfdcb75cbaa37f1f375a2fed1b6773e070d7f2abd20a3bc3f35784`  
		Last Modified: Tue, 02 Sep 2025 00:18:13 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.6.56-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:7cd2f404c27c665053aed069feb733b79e882fde09a25bff13117d287f586b28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69efeac22341fe15c4f4eae6fd9d0e2bc4eac00d04ea26ac6f0e94f405f18e6c`

```dockerfile
```

-	Layers:
	-	`sha256:88f4c4fd85cb13450eae1a2293511e3b55f142d5e0c8c060e85251e12547649b`  
		Last Modified: Tue, 02 Sep 2025 03:49:18 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.6`

```console
$ docker pull clickhouse@sha256:60eeec959f0200d08f889381049340a676c1adb3f04e0a9d2078c975bbfdba6b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6` - linux; amd64

```console
$ docker pull clickhouse@sha256:e6e9df30da3b21e48f4059d0f60e98e4e9e88ef02b380789c5147597e71c0af6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212107087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4289aa0834f0ca8d2260d14f874b9ed19df7aa3baa1df830c493238eb91b62f`
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
# Thu, 18 Sep 2025 16:06:29 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 18 Sep 2025 16:06:29 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
ARG REPO_CHANNEL=stable
# Thu, 18 Sep 2025 16:06:29 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 18 Sep 2025 16:06:29 GMT
ARG VERSION=25.6.12.10
# Thu, 18 Sep 2025 16:06:29 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 16:06:29 GMT
ENV TZ=UTC
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 18 Sep 2025 16:06:29 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 18 Sep 2025 16:06:29 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 18 Sep 2025 16:06:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce6346c3366f193d14d4e8075d749fa6fae7c27cf17debba55c640de6de214e`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 7.2 MB (7151606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ed3e49c1e9f332aa2ca092062811bf88d39810972fcce313242544cad8a449`  
		Last Modified: Thu, 18 Sep 2025 21:49:49 GMT  
		Size: 174.5 MB (174548520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9502f88569554c8eef0d2b14a41bcfc4aad686c6672551a8db9f65f26af39f42`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bda514c12021b1f0e31c16cb0dd1c52bed5b03ea6629c3c232d2089d8cbef01`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b920a490da86c608609246454fb43df932f8558930408cec43a07cf2b6113a6`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b8785a807e8cc35a1c11672027702e500999c329bcb4d5b4cac504c54a448f`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e65c3600304b8a467921d36fa5e5346eb0396162dfb403b6f88110053e9174`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6` - unknown; unknown

```console
$ docker pull clickhouse@sha256:269cb78b9eee5a609ab20b2c5977bd75a17443f7c5d7b0540af5b056c141d1b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5ae60f6c19fae6eafefbeada71100b27b9293432fd6455e2da034bf1b8f55fb`

```dockerfile
```

-	Layers:
	-	`sha256:7b8b5f589470f5c47cadc70cdca67e4d73826144c94f1a56156022cace97d8ed`  
		Last Modified: Thu, 18 Sep 2025 21:49:23 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.6` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a64881b9ebed6e6817340fbe4bd7b10e41b5d2b126198607bf48565da31ef74f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198248017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b01f720a485edead0f837a5326d1d523025d2c2f5593dc1b07700cfb1376cb`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:17 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:19 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 17:21:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 16:06:29 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 18 Sep 2025 16:06:29 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
ARG REPO_CHANNEL=stable
# Thu, 18 Sep 2025 16:06:29 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 18 Sep 2025 16:06:29 GMT
ARG VERSION=25.6.12.10
# Thu, 18 Sep 2025 16:06:29 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 16:06:29 GMT
ENV TZ=UTC
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 18 Sep 2025 16:06:29 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 18 Sep 2025 16:06:29 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 18 Sep 2025 16:06:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d37946de2e062811d095b0851034dd7289ca2d346a4320b1f07939da4a691c0`  
		Last Modified: Thu, 18 Sep 2025 19:00:50 GMT  
		Size: 7.1 MB (7127987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55694d503755d703110a934ed8514d5ea03c4d08f9dc863d0dff9ee5994c7cfe`  
		Last Modified: Thu, 18 Sep 2025 19:10:32 GMT  
		Size: 162.9 MB (162888535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d8861c84fae76283c0f8531174991d71f5eaf1338217e9ef74c0ba6dea2324`  
		Last Modified: Thu, 18 Sep 2025 19:00:50 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed161be40290000908e4604fea1c2e58b8e33925362d9682b15c6349c8c3ed98`  
		Last Modified: Thu, 18 Sep 2025 19:00:50 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8024951b043b8e61654ffd32eddef2fee22cb34097c8917ac52b9520c5c8f700`  
		Last Modified: Thu, 18 Sep 2025 19:00:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed761be0922bae1061927a6a5c2e71c10f04a90fb7f31d9ba320f7d09d7e09d8`  
		Last Modified: Thu, 18 Sep 2025 19:00:50 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276533c3360217c4db197789d1f9ab39ce7f06bbf6fee13d95fa9e59302a132c`  
		Last Modified: Thu, 18 Sep 2025 19:00:50 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d1c722b5a1d3fa58e22d40921adaa088a66eca679baa4e841624a912d8a41ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9f2091310b49816e97f1aa793b15b39e0594b517e9dc8c48bbaa3b36e5f0880`

```dockerfile
```

-	Layers:
	-	`sha256:886593947163388ddaa74c1285f7810ac544e089905e2759397f3a090af99360`  
		Last Modified: Thu, 18 Sep 2025 21:49:26 GMT  
		Size: 25.5 KB (25465 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.6-jammy`

```console
$ docker pull clickhouse@sha256:60eeec959f0200d08f889381049340a676c1adb3f04e0a9d2078c975bbfdba6b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:e6e9df30da3b21e48f4059d0f60e98e4e9e88ef02b380789c5147597e71c0af6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212107087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4289aa0834f0ca8d2260d14f874b9ed19df7aa3baa1df830c493238eb91b62f`
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
# Thu, 18 Sep 2025 16:06:29 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 18 Sep 2025 16:06:29 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
ARG REPO_CHANNEL=stable
# Thu, 18 Sep 2025 16:06:29 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 18 Sep 2025 16:06:29 GMT
ARG VERSION=25.6.12.10
# Thu, 18 Sep 2025 16:06:29 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 16:06:29 GMT
ENV TZ=UTC
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 18 Sep 2025 16:06:29 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 18 Sep 2025 16:06:29 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 18 Sep 2025 16:06:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce6346c3366f193d14d4e8075d749fa6fae7c27cf17debba55c640de6de214e`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 7.2 MB (7151606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ed3e49c1e9f332aa2ca092062811bf88d39810972fcce313242544cad8a449`  
		Last Modified: Thu, 18 Sep 2025 21:49:49 GMT  
		Size: 174.5 MB (174548520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9502f88569554c8eef0d2b14a41bcfc4aad686c6672551a8db9f65f26af39f42`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bda514c12021b1f0e31c16cb0dd1c52bed5b03ea6629c3c232d2089d8cbef01`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b920a490da86c608609246454fb43df932f8558930408cec43a07cf2b6113a6`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b8785a807e8cc35a1c11672027702e500999c329bcb4d5b4cac504c54a448f`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e65c3600304b8a467921d36fa5e5346eb0396162dfb403b6f88110053e9174`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:269cb78b9eee5a609ab20b2c5977bd75a17443f7c5d7b0540af5b056c141d1b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5ae60f6c19fae6eafefbeada71100b27b9293432fd6455e2da034bf1b8f55fb`

```dockerfile
```

-	Layers:
	-	`sha256:7b8b5f589470f5c47cadc70cdca67e4d73826144c94f1a56156022cace97d8ed`  
		Last Modified: Thu, 18 Sep 2025 21:49:23 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.6-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a64881b9ebed6e6817340fbe4bd7b10e41b5d2b126198607bf48565da31ef74f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198248017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b01f720a485edead0f837a5326d1d523025d2c2f5593dc1b07700cfb1376cb`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:17 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:19 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 17:21:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 16:06:29 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 18 Sep 2025 16:06:29 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
ARG REPO_CHANNEL=stable
# Thu, 18 Sep 2025 16:06:29 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 18 Sep 2025 16:06:29 GMT
ARG VERSION=25.6.12.10
# Thu, 18 Sep 2025 16:06:29 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 16:06:29 GMT
ENV TZ=UTC
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 18 Sep 2025 16:06:29 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 18 Sep 2025 16:06:29 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 18 Sep 2025 16:06:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d37946de2e062811d095b0851034dd7289ca2d346a4320b1f07939da4a691c0`  
		Last Modified: Thu, 18 Sep 2025 19:00:50 GMT  
		Size: 7.1 MB (7127987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55694d503755d703110a934ed8514d5ea03c4d08f9dc863d0dff9ee5994c7cfe`  
		Last Modified: Thu, 18 Sep 2025 19:10:32 GMT  
		Size: 162.9 MB (162888535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d8861c84fae76283c0f8531174991d71f5eaf1338217e9ef74c0ba6dea2324`  
		Last Modified: Thu, 18 Sep 2025 19:00:50 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed161be40290000908e4604fea1c2e58b8e33925362d9682b15c6349c8c3ed98`  
		Last Modified: Thu, 18 Sep 2025 19:00:50 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8024951b043b8e61654ffd32eddef2fee22cb34097c8917ac52b9520c5c8f700`  
		Last Modified: Thu, 18 Sep 2025 19:00:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed761be0922bae1061927a6a5c2e71c10f04a90fb7f31d9ba320f7d09d7e09d8`  
		Last Modified: Thu, 18 Sep 2025 19:00:50 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276533c3360217c4db197789d1f9ab39ce7f06bbf6fee13d95fa9e59302a132c`  
		Last Modified: Thu, 18 Sep 2025 19:00:50 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d1c722b5a1d3fa58e22d40921adaa088a66eca679baa4e841624a912d8a41ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9f2091310b49816e97f1aa793b15b39e0594b517e9dc8c48bbaa3b36e5f0880`

```dockerfile
```

-	Layers:
	-	`sha256:886593947163388ddaa74c1285f7810ac544e089905e2759397f3a090af99360`  
		Last Modified: Thu, 18 Sep 2025 21:49:26 GMT  
		Size: 25.5 KB (25465 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.6.12`

```console
$ docker pull clickhouse@sha256:60eeec959f0200d08f889381049340a676c1adb3f04e0a9d2078c975bbfdba6b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6.12` - linux; amd64

```console
$ docker pull clickhouse@sha256:e6e9df30da3b21e48f4059d0f60e98e4e9e88ef02b380789c5147597e71c0af6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212107087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4289aa0834f0ca8d2260d14f874b9ed19df7aa3baa1df830c493238eb91b62f`
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
# Thu, 18 Sep 2025 16:06:29 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 18 Sep 2025 16:06:29 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
ARG REPO_CHANNEL=stable
# Thu, 18 Sep 2025 16:06:29 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 18 Sep 2025 16:06:29 GMT
ARG VERSION=25.6.12.10
# Thu, 18 Sep 2025 16:06:29 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 16:06:29 GMT
ENV TZ=UTC
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 18 Sep 2025 16:06:29 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 18 Sep 2025 16:06:29 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 18 Sep 2025 16:06:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce6346c3366f193d14d4e8075d749fa6fae7c27cf17debba55c640de6de214e`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 7.2 MB (7151606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ed3e49c1e9f332aa2ca092062811bf88d39810972fcce313242544cad8a449`  
		Last Modified: Thu, 18 Sep 2025 21:49:49 GMT  
		Size: 174.5 MB (174548520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9502f88569554c8eef0d2b14a41bcfc4aad686c6672551a8db9f65f26af39f42`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bda514c12021b1f0e31c16cb0dd1c52bed5b03ea6629c3c232d2089d8cbef01`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b920a490da86c608609246454fb43df932f8558930408cec43a07cf2b6113a6`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b8785a807e8cc35a1c11672027702e500999c329bcb4d5b4cac504c54a448f`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e65c3600304b8a467921d36fa5e5346eb0396162dfb403b6f88110053e9174`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.12` - unknown; unknown

```console
$ docker pull clickhouse@sha256:269cb78b9eee5a609ab20b2c5977bd75a17443f7c5d7b0540af5b056c141d1b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5ae60f6c19fae6eafefbeada71100b27b9293432fd6455e2da034bf1b8f55fb`

```dockerfile
```

-	Layers:
	-	`sha256:7b8b5f589470f5c47cadc70cdca67e4d73826144c94f1a56156022cace97d8ed`  
		Last Modified: Thu, 18 Sep 2025 21:49:23 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.6.12` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a64881b9ebed6e6817340fbe4bd7b10e41b5d2b126198607bf48565da31ef74f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198248017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b01f720a485edead0f837a5326d1d523025d2c2f5593dc1b07700cfb1376cb`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:17 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:19 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 17:21:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 16:06:29 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 18 Sep 2025 16:06:29 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
ARG REPO_CHANNEL=stable
# Thu, 18 Sep 2025 16:06:29 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 18 Sep 2025 16:06:29 GMT
ARG VERSION=25.6.12.10
# Thu, 18 Sep 2025 16:06:29 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 16:06:29 GMT
ENV TZ=UTC
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 18 Sep 2025 16:06:29 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 18 Sep 2025 16:06:29 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 18 Sep 2025 16:06:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d37946de2e062811d095b0851034dd7289ca2d346a4320b1f07939da4a691c0`  
		Last Modified: Thu, 18 Sep 2025 19:00:50 GMT  
		Size: 7.1 MB (7127987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55694d503755d703110a934ed8514d5ea03c4d08f9dc863d0dff9ee5994c7cfe`  
		Last Modified: Thu, 18 Sep 2025 19:10:32 GMT  
		Size: 162.9 MB (162888535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d8861c84fae76283c0f8531174991d71f5eaf1338217e9ef74c0ba6dea2324`  
		Last Modified: Thu, 18 Sep 2025 19:00:50 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed161be40290000908e4604fea1c2e58b8e33925362d9682b15c6349c8c3ed98`  
		Last Modified: Thu, 18 Sep 2025 19:00:50 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8024951b043b8e61654ffd32eddef2fee22cb34097c8917ac52b9520c5c8f700`  
		Last Modified: Thu, 18 Sep 2025 19:00:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed761be0922bae1061927a6a5c2e71c10f04a90fb7f31d9ba320f7d09d7e09d8`  
		Last Modified: Thu, 18 Sep 2025 19:00:50 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276533c3360217c4db197789d1f9ab39ce7f06bbf6fee13d95fa9e59302a132c`  
		Last Modified: Thu, 18 Sep 2025 19:00:50 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.12` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d1c722b5a1d3fa58e22d40921adaa088a66eca679baa4e841624a912d8a41ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9f2091310b49816e97f1aa793b15b39e0594b517e9dc8c48bbaa3b36e5f0880`

```dockerfile
```

-	Layers:
	-	`sha256:886593947163388ddaa74c1285f7810ac544e089905e2759397f3a090af99360`  
		Last Modified: Thu, 18 Sep 2025 21:49:26 GMT  
		Size: 25.5 KB (25465 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.6.12-jammy`

```console
$ docker pull clickhouse@sha256:60eeec959f0200d08f889381049340a676c1adb3f04e0a9d2078c975bbfdba6b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6.12-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:e6e9df30da3b21e48f4059d0f60e98e4e9e88ef02b380789c5147597e71c0af6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212107087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4289aa0834f0ca8d2260d14f874b9ed19df7aa3baa1df830c493238eb91b62f`
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
# Thu, 18 Sep 2025 16:06:29 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 18 Sep 2025 16:06:29 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
ARG REPO_CHANNEL=stable
# Thu, 18 Sep 2025 16:06:29 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 18 Sep 2025 16:06:29 GMT
ARG VERSION=25.6.12.10
# Thu, 18 Sep 2025 16:06:29 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 16:06:29 GMT
ENV TZ=UTC
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 18 Sep 2025 16:06:29 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 18 Sep 2025 16:06:29 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 18 Sep 2025 16:06:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce6346c3366f193d14d4e8075d749fa6fae7c27cf17debba55c640de6de214e`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 7.2 MB (7151606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ed3e49c1e9f332aa2ca092062811bf88d39810972fcce313242544cad8a449`  
		Last Modified: Thu, 18 Sep 2025 21:49:49 GMT  
		Size: 174.5 MB (174548520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9502f88569554c8eef0d2b14a41bcfc4aad686c6672551a8db9f65f26af39f42`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bda514c12021b1f0e31c16cb0dd1c52bed5b03ea6629c3c232d2089d8cbef01`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b920a490da86c608609246454fb43df932f8558930408cec43a07cf2b6113a6`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b8785a807e8cc35a1c11672027702e500999c329bcb4d5b4cac504c54a448f`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e65c3600304b8a467921d36fa5e5346eb0396162dfb403b6f88110053e9174`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.12-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:269cb78b9eee5a609ab20b2c5977bd75a17443f7c5d7b0540af5b056c141d1b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5ae60f6c19fae6eafefbeada71100b27b9293432fd6455e2da034bf1b8f55fb`

```dockerfile
```

-	Layers:
	-	`sha256:7b8b5f589470f5c47cadc70cdca67e4d73826144c94f1a56156022cace97d8ed`  
		Last Modified: Thu, 18 Sep 2025 21:49:23 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.6.12-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a64881b9ebed6e6817340fbe4bd7b10e41b5d2b126198607bf48565da31ef74f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198248017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b01f720a485edead0f837a5326d1d523025d2c2f5593dc1b07700cfb1376cb`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:17 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:19 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 17:21:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 16:06:29 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 18 Sep 2025 16:06:29 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
ARG REPO_CHANNEL=stable
# Thu, 18 Sep 2025 16:06:29 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 18 Sep 2025 16:06:29 GMT
ARG VERSION=25.6.12.10
# Thu, 18 Sep 2025 16:06:29 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 16:06:29 GMT
ENV TZ=UTC
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 18 Sep 2025 16:06:29 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 18 Sep 2025 16:06:29 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 18 Sep 2025 16:06:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d37946de2e062811d095b0851034dd7289ca2d346a4320b1f07939da4a691c0`  
		Last Modified: Thu, 18 Sep 2025 19:00:50 GMT  
		Size: 7.1 MB (7127987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55694d503755d703110a934ed8514d5ea03c4d08f9dc863d0dff9ee5994c7cfe`  
		Last Modified: Thu, 18 Sep 2025 19:10:32 GMT  
		Size: 162.9 MB (162888535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d8861c84fae76283c0f8531174991d71f5eaf1338217e9ef74c0ba6dea2324`  
		Last Modified: Thu, 18 Sep 2025 19:00:50 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed161be40290000908e4604fea1c2e58b8e33925362d9682b15c6349c8c3ed98`  
		Last Modified: Thu, 18 Sep 2025 19:00:50 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8024951b043b8e61654ffd32eddef2fee22cb34097c8917ac52b9520c5c8f700`  
		Last Modified: Thu, 18 Sep 2025 19:00:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed761be0922bae1061927a6a5c2e71c10f04a90fb7f31d9ba320f7d09d7e09d8`  
		Last Modified: Thu, 18 Sep 2025 19:00:50 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276533c3360217c4db197789d1f9ab39ce7f06bbf6fee13d95fa9e59302a132c`  
		Last Modified: Thu, 18 Sep 2025 19:00:50 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.12-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d1c722b5a1d3fa58e22d40921adaa088a66eca679baa4e841624a912d8a41ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9f2091310b49816e97f1aa793b15b39e0594b517e9dc8c48bbaa3b36e5f0880`

```dockerfile
```

-	Layers:
	-	`sha256:886593947163388ddaa74c1285f7810ac544e089905e2759397f3a090af99360`  
		Last Modified: Thu, 18 Sep 2025 21:49:26 GMT  
		Size: 25.5 KB (25465 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.6.12.10`

```console
$ docker pull clickhouse@sha256:60eeec959f0200d08f889381049340a676c1adb3f04e0a9d2078c975bbfdba6b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6.12.10` - linux; amd64

```console
$ docker pull clickhouse@sha256:e6e9df30da3b21e48f4059d0f60e98e4e9e88ef02b380789c5147597e71c0af6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212107087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4289aa0834f0ca8d2260d14f874b9ed19df7aa3baa1df830c493238eb91b62f`
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
# Thu, 18 Sep 2025 16:06:29 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 18 Sep 2025 16:06:29 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
ARG REPO_CHANNEL=stable
# Thu, 18 Sep 2025 16:06:29 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 18 Sep 2025 16:06:29 GMT
ARG VERSION=25.6.12.10
# Thu, 18 Sep 2025 16:06:29 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 16:06:29 GMT
ENV TZ=UTC
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 18 Sep 2025 16:06:29 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 18 Sep 2025 16:06:29 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 18 Sep 2025 16:06:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce6346c3366f193d14d4e8075d749fa6fae7c27cf17debba55c640de6de214e`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 7.2 MB (7151606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ed3e49c1e9f332aa2ca092062811bf88d39810972fcce313242544cad8a449`  
		Last Modified: Thu, 18 Sep 2025 21:49:49 GMT  
		Size: 174.5 MB (174548520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9502f88569554c8eef0d2b14a41bcfc4aad686c6672551a8db9f65f26af39f42`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bda514c12021b1f0e31c16cb0dd1c52bed5b03ea6629c3c232d2089d8cbef01`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b920a490da86c608609246454fb43df932f8558930408cec43a07cf2b6113a6`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b8785a807e8cc35a1c11672027702e500999c329bcb4d5b4cac504c54a448f`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e65c3600304b8a467921d36fa5e5346eb0396162dfb403b6f88110053e9174`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.12.10` - unknown; unknown

```console
$ docker pull clickhouse@sha256:269cb78b9eee5a609ab20b2c5977bd75a17443f7c5d7b0540af5b056c141d1b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5ae60f6c19fae6eafefbeada71100b27b9293432fd6455e2da034bf1b8f55fb`

```dockerfile
```

-	Layers:
	-	`sha256:7b8b5f589470f5c47cadc70cdca67e4d73826144c94f1a56156022cace97d8ed`  
		Last Modified: Thu, 18 Sep 2025 21:49:23 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.6.12.10` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a64881b9ebed6e6817340fbe4bd7b10e41b5d2b126198607bf48565da31ef74f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198248017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b01f720a485edead0f837a5326d1d523025d2c2f5593dc1b07700cfb1376cb`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:17 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:19 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 17:21:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 16:06:29 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 18 Sep 2025 16:06:29 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
ARG REPO_CHANNEL=stable
# Thu, 18 Sep 2025 16:06:29 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 18 Sep 2025 16:06:29 GMT
ARG VERSION=25.6.12.10
# Thu, 18 Sep 2025 16:06:29 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 16:06:29 GMT
ENV TZ=UTC
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 18 Sep 2025 16:06:29 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 18 Sep 2025 16:06:29 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 18 Sep 2025 16:06:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d37946de2e062811d095b0851034dd7289ca2d346a4320b1f07939da4a691c0`  
		Last Modified: Thu, 18 Sep 2025 19:00:50 GMT  
		Size: 7.1 MB (7127987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55694d503755d703110a934ed8514d5ea03c4d08f9dc863d0dff9ee5994c7cfe`  
		Last Modified: Thu, 18 Sep 2025 19:10:32 GMT  
		Size: 162.9 MB (162888535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d8861c84fae76283c0f8531174991d71f5eaf1338217e9ef74c0ba6dea2324`  
		Last Modified: Thu, 18 Sep 2025 19:00:50 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed161be40290000908e4604fea1c2e58b8e33925362d9682b15c6349c8c3ed98`  
		Last Modified: Thu, 18 Sep 2025 19:00:50 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8024951b043b8e61654ffd32eddef2fee22cb34097c8917ac52b9520c5c8f700`  
		Last Modified: Thu, 18 Sep 2025 19:00:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed761be0922bae1061927a6a5c2e71c10f04a90fb7f31d9ba320f7d09d7e09d8`  
		Last Modified: Thu, 18 Sep 2025 19:00:50 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276533c3360217c4db197789d1f9ab39ce7f06bbf6fee13d95fa9e59302a132c`  
		Last Modified: Thu, 18 Sep 2025 19:00:50 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.12.10` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d1c722b5a1d3fa58e22d40921adaa088a66eca679baa4e841624a912d8a41ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9f2091310b49816e97f1aa793b15b39e0594b517e9dc8c48bbaa3b36e5f0880`

```dockerfile
```

-	Layers:
	-	`sha256:886593947163388ddaa74c1285f7810ac544e089905e2759397f3a090af99360`  
		Last Modified: Thu, 18 Sep 2025 21:49:26 GMT  
		Size: 25.5 KB (25465 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.6.12.10-jammy`

```console
$ docker pull clickhouse@sha256:60eeec959f0200d08f889381049340a676c1adb3f04e0a9d2078c975bbfdba6b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6.12.10-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:e6e9df30da3b21e48f4059d0f60e98e4e9e88ef02b380789c5147597e71c0af6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212107087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4289aa0834f0ca8d2260d14f874b9ed19df7aa3baa1df830c493238eb91b62f`
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
# Thu, 18 Sep 2025 16:06:29 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 18 Sep 2025 16:06:29 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
ARG REPO_CHANNEL=stable
# Thu, 18 Sep 2025 16:06:29 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 18 Sep 2025 16:06:29 GMT
ARG VERSION=25.6.12.10
# Thu, 18 Sep 2025 16:06:29 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 16:06:29 GMT
ENV TZ=UTC
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 18 Sep 2025 16:06:29 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 18 Sep 2025 16:06:29 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 18 Sep 2025 16:06:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce6346c3366f193d14d4e8075d749fa6fae7c27cf17debba55c640de6de214e`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 7.2 MB (7151606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ed3e49c1e9f332aa2ca092062811bf88d39810972fcce313242544cad8a449`  
		Last Modified: Thu, 18 Sep 2025 21:49:49 GMT  
		Size: 174.5 MB (174548520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9502f88569554c8eef0d2b14a41bcfc4aad686c6672551a8db9f65f26af39f42`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bda514c12021b1f0e31c16cb0dd1c52bed5b03ea6629c3c232d2089d8cbef01`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b920a490da86c608609246454fb43df932f8558930408cec43a07cf2b6113a6`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b8785a807e8cc35a1c11672027702e500999c329bcb4d5b4cac504c54a448f`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e65c3600304b8a467921d36fa5e5346eb0396162dfb403b6f88110053e9174`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.12.10-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:269cb78b9eee5a609ab20b2c5977bd75a17443f7c5d7b0540af5b056c141d1b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5ae60f6c19fae6eafefbeada71100b27b9293432fd6455e2da034bf1b8f55fb`

```dockerfile
```

-	Layers:
	-	`sha256:7b8b5f589470f5c47cadc70cdca67e4d73826144c94f1a56156022cace97d8ed`  
		Last Modified: Thu, 18 Sep 2025 21:49:23 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.6.12.10-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a64881b9ebed6e6817340fbe4bd7b10e41b5d2b126198607bf48565da31ef74f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198248017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b01f720a485edead0f837a5326d1d523025d2c2f5593dc1b07700cfb1376cb`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:17 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:19 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 17:21:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 16:06:29 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 18 Sep 2025 16:06:29 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
ARG REPO_CHANNEL=stable
# Thu, 18 Sep 2025 16:06:29 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 18 Sep 2025 16:06:29 GMT
ARG VERSION=25.6.12.10
# Thu, 18 Sep 2025 16:06:29 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 16:06:29 GMT
ENV TZ=UTC
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 18 Sep 2025 16:06:29 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 18 Sep 2025 16:06:29 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 18 Sep 2025 16:06:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d37946de2e062811d095b0851034dd7289ca2d346a4320b1f07939da4a691c0`  
		Last Modified: Thu, 18 Sep 2025 19:00:50 GMT  
		Size: 7.1 MB (7127987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55694d503755d703110a934ed8514d5ea03c4d08f9dc863d0dff9ee5994c7cfe`  
		Last Modified: Thu, 18 Sep 2025 19:10:32 GMT  
		Size: 162.9 MB (162888535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d8861c84fae76283c0f8531174991d71f5eaf1338217e9ef74c0ba6dea2324`  
		Last Modified: Thu, 18 Sep 2025 19:00:50 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed161be40290000908e4604fea1c2e58b8e33925362d9682b15c6349c8c3ed98`  
		Last Modified: Thu, 18 Sep 2025 19:00:50 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8024951b043b8e61654ffd32eddef2fee22cb34097c8917ac52b9520c5c8f700`  
		Last Modified: Thu, 18 Sep 2025 19:00:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed761be0922bae1061927a6a5c2e71c10f04a90fb7f31d9ba320f7d09d7e09d8`  
		Last Modified: Thu, 18 Sep 2025 19:00:50 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276533c3360217c4db197789d1f9ab39ce7f06bbf6fee13d95fa9e59302a132c`  
		Last Modified: Thu, 18 Sep 2025 19:00:50 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.12.10-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d1c722b5a1d3fa58e22d40921adaa088a66eca679baa4e841624a912d8a41ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9f2091310b49816e97f1aa793b15b39e0594b517e9dc8c48bbaa3b36e5f0880`

```dockerfile
```

-	Layers:
	-	`sha256:886593947163388ddaa74c1285f7810ac544e089905e2759397f3a090af99360`  
		Last Modified: Thu, 18 Sep 2025 21:49:26 GMT  
		Size: 25.5 KB (25465 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.7`

```console
$ docker pull clickhouse@sha256:09ed91ad70e952664c6bd0162149865681d42ab0d75db30e8b35256adb72963b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.7` - linux; amd64

```console
$ docker pull clickhouse@sha256:6bb0972af794c51cd257cec37ff8fb2bc0585972398596bfe043dd74fc47c7ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221873228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45c844005318524dcde3dc199412ccc2b5987b7c6a398bb62356d055dfe63705`
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
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.7.7.68
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fcdcbe58c9000f60fbbd97b9c476d599cc9fb9a5b78995b368361badcb1194e`  
		Last Modified: Thu, 25 Sep 2025 17:40:26 GMT  
		Size: 7.6 MB (7598481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0302f8ab0fa5c939b2444dd3b6169eda23d4dabef613fb0f4040607f16bd52a4`  
		Last Modified: Thu, 25 Sep 2025 18:50:02 GMT  
		Size: 183.9 MB (183867788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ed5371ab3e6289a59f3ba06e5ace31e101319cb4d0d80222540350f6d24426`  
		Last Modified: Thu, 25 Sep 2025 17:40:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b6c29ab3bd6eaefe7b6bb7cb0afd19b324b662f8cf01574c7a9d48e129ac57`  
		Last Modified: Thu, 25 Sep 2025 17:40:25 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a663001f0e3ee3ded89f4dcea562b36ae70f5efabeeb84e4204ffd818f407c87`  
		Last Modified: Thu, 25 Sep 2025 17:40:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2278ee103d75b0f3fff12c113541676a7bd3b6b95e772ff65f3e60eced55b3b`  
		Last Modified: Thu, 25 Sep 2025 17:40:26 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1048cb093d408574524c2db35d765ccd67612b5a3199772c288aa09df4d96c76`  
		Last Modified: Thu, 25 Sep 2025 17:40:26 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:de370f920364dd41bb6de3629a2af4a6b0778b13dae8987a092b7a3cb2585b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee0b70ac8fe94c416eadc25a56dc6a1fc660887f6e47cd37ae26c97dfb36f53`

```dockerfile
```

-	Layers:
	-	`sha256:65340b8583184dd5fe44f052d3bf95890b4e2f552792c19f59382ce9240c7aec`  
		Last Modified: Thu, 25 Sep 2025 18:49:27 GMT  
		Size: 25.5 KB (25460 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.7` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:6746518814e510b28bd7dd517195f648529da869ed42524ed7f5e92349dfbc54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.8 MB (207787017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e40eb8fcf90dc30bd981d04f1906aa9ab03f7cfdca8042011520a76b5a16d8f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:17 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:19 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 17:21:19 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.7.7.68
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b243d4603c9fb10873c5c8071c63750ba2ef471941549af64a0e9b750990555`  
		Last Modified: Thu, 25 Sep 2025 17:40:02 GMT  
		Size: 7.6 MB (7577255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829ddc07aee5da355b3e9f621bb5a1ab52f8e89bb194c0562e178b1302ea61a3`  
		Last Modified: Thu, 25 Sep 2025 18:49:56 GMT  
		Size: 172.0 MB (171978270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d97c4d247a31661f8a3e325ec93579864a9387514d044966fb94fc8f5a9704`  
		Last Modified: Thu, 25 Sep 2025 17:40:01 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9a1cbed902526a98c24edac85a7de58184d45cac51ea3462c88858d01f743b`  
		Last Modified: Thu, 25 Sep 2025 17:40:02 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bc58932d6fbb2946acfc63f25b647cb8ecf9173c9dcbfcab667c30f9021467`  
		Last Modified: Thu, 25 Sep 2025 17:40:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40145640226783b4fa4a000af6670d5264b7b371c41c3ee485ca08cb5f8f3ec`  
		Last Modified: Thu, 25 Sep 2025 17:40:01 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043e525e1c360f6690a8c4760e474ee33537cf3a4ed3bf0355fc35bad848f9c1`  
		Last Modified: Thu, 25 Sep 2025 17:40:01 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0f526c3cd32aa9a095e13ee8090d39c575580da66df75b5c32b06c5f7db1c08a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7df6fe6d09b8c911d4fa679713ab237bd52cf501548efab0c820f717941615a4`

```dockerfile
```

-	Layers:
	-	`sha256:a07f926872d4924a19972bb2d6ecb84f3ffb6a2d398a06be76cf9f6af60d627e`  
		Last Modified: Thu, 25 Sep 2025 18:49:30 GMT  
		Size: 25.6 KB (25649 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.7-jammy`

```console
$ docker pull clickhouse@sha256:09ed91ad70e952664c6bd0162149865681d42ab0d75db30e8b35256adb72963b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.7-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:6bb0972af794c51cd257cec37ff8fb2bc0585972398596bfe043dd74fc47c7ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221873228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45c844005318524dcde3dc199412ccc2b5987b7c6a398bb62356d055dfe63705`
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
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.7.7.68
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fcdcbe58c9000f60fbbd97b9c476d599cc9fb9a5b78995b368361badcb1194e`  
		Last Modified: Thu, 25 Sep 2025 17:40:26 GMT  
		Size: 7.6 MB (7598481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0302f8ab0fa5c939b2444dd3b6169eda23d4dabef613fb0f4040607f16bd52a4`  
		Last Modified: Thu, 25 Sep 2025 18:50:02 GMT  
		Size: 183.9 MB (183867788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ed5371ab3e6289a59f3ba06e5ace31e101319cb4d0d80222540350f6d24426`  
		Last Modified: Thu, 25 Sep 2025 17:40:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b6c29ab3bd6eaefe7b6bb7cb0afd19b324b662f8cf01574c7a9d48e129ac57`  
		Last Modified: Thu, 25 Sep 2025 17:40:25 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a663001f0e3ee3ded89f4dcea562b36ae70f5efabeeb84e4204ffd818f407c87`  
		Last Modified: Thu, 25 Sep 2025 17:40:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2278ee103d75b0f3fff12c113541676a7bd3b6b95e772ff65f3e60eced55b3b`  
		Last Modified: Thu, 25 Sep 2025 17:40:26 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1048cb093d408574524c2db35d765ccd67612b5a3199772c288aa09df4d96c76`  
		Last Modified: Thu, 25 Sep 2025 17:40:26 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:de370f920364dd41bb6de3629a2af4a6b0778b13dae8987a092b7a3cb2585b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee0b70ac8fe94c416eadc25a56dc6a1fc660887f6e47cd37ae26c97dfb36f53`

```dockerfile
```

-	Layers:
	-	`sha256:65340b8583184dd5fe44f052d3bf95890b4e2f552792c19f59382ce9240c7aec`  
		Last Modified: Thu, 25 Sep 2025 18:49:27 GMT  
		Size: 25.5 KB (25460 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.7-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:6746518814e510b28bd7dd517195f648529da869ed42524ed7f5e92349dfbc54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.8 MB (207787017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e40eb8fcf90dc30bd981d04f1906aa9ab03f7cfdca8042011520a76b5a16d8f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:17 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:19 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 17:21:19 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.7.7.68
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b243d4603c9fb10873c5c8071c63750ba2ef471941549af64a0e9b750990555`  
		Last Modified: Thu, 25 Sep 2025 17:40:02 GMT  
		Size: 7.6 MB (7577255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829ddc07aee5da355b3e9f621bb5a1ab52f8e89bb194c0562e178b1302ea61a3`  
		Last Modified: Thu, 25 Sep 2025 18:49:56 GMT  
		Size: 172.0 MB (171978270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d97c4d247a31661f8a3e325ec93579864a9387514d044966fb94fc8f5a9704`  
		Last Modified: Thu, 25 Sep 2025 17:40:01 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9a1cbed902526a98c24edac85a7de58184d45cac51ea3462c88858d01f743b`  
		Last Modified: Thu, 25 Sep 2025 17:40:02 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bc58932d6fbb2946acfc63f25b647cb8ecf9173c9dcbfcab667c30f9021467`  
		Last Modified: Thu, 25 Sep 2025 17:40:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40145640226783b4fa4a000af6670d5264b7b371c41c3ee485ca08cb5f8f3ec`  
		Last Modified: Thu, 25 Sep 2025 17:40:01 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043e525e1c360f6690a8c4760e474ee33537cf3a4ed3bf0355fc35bad848f9c1`  
		Last Modified: Thu, 25 Sep 2025 17:40:01 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0f526c3cd32aa9a095e13ee8090d39c575580da66df75b5c32b06c5f7db1c08a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7df6fe6d09b8c911d4fa679713ab237bd52cf501548efab0c820f717941615a4`

```dockerfile
```

-	Layers:
	-	`sha256:a07f926872d4924a19972bb2d6ecb84f3ffb6a2d398a06be76cf9f6af60d627e`  
		Last Modified: Thu, 25 Sep 2025 18:49:30 GMT  
		Size: 25.6 KB (25649 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.7.7`

```console
$ docker pull clickhouse@sha256:09ed91ad70e952664c6bd0162149865681d42ab0d75db30e8b35256adb72963b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.7.7` - linux; amd64

```console
$ docker pull clickhouse@sha256:6bb0972af794c51cd257cec37ff8fb2bc0585972398596bfe043dd74fc47c7ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221873228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45c844005318524dcde3dc199412ccc2b5987b7c6a398bb62356d055dfe63705`
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
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.7.7.68
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fcdcbe58c9000f60fbbd97b9c476d599cc9fb9a5b78995b368361badcb1194e`  
		Last Modified: Thu, 25 Sep 2025 17:40:26 GMT  
		Size: 7.6 MB (7598481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0302f8ab0fa5c939b2444dd3b6169eda23d4dabef613fb0f4040607f16bd52a4`  
		Last Modified: Thu, 25 Sep 2025 18:50:02 GMT  
		Size: 183.9 MB (183867788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ed5371ab3e6289a59f3ba06e5ace31e101319cb4d0d80222540350f6d24426`  
		Last Modified: Thu, 25 Sep 2025 17:40:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b6c29ab3bd6eaefe7b6bb7cb0afd19b324b662f8cf01574c7a9d48e129ac57`  
		Last Modified: Thu, 25 Sep 2025 17:40:25 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a663001f0e3ee3ded89f4dcea562b36ae70f5efabeeb84e4204ffd818f407c87`  
		Last Modified: Thu, 25 Sep 2025 17:40:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2278ee103d75b0f3fff12c113541676a7bd3b6b95e772ff65f3e60eced55b3b`  
		Last Modified: Thu, 25 Sep 2025 17:40:26 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1048cb093d408574524c2db35d765ccd67612b5a3199772c288aa09df4d96c76`  
		Last Modified: Thu, 25 Sep 2025 17:40:26 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:de370f920364dd41bb6de3629a2af4a6b0778b13dae8987a092b7a3cb2585b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee0b70ac8fe94c416eadc25a56dc6a1fc660887f6e47cd37ae26c97dfb36f53`

```dockerfile
```

-	Layers:
	-	`sha256:65340b8583184dd5fe44f052d3bf95890b4e2f552792c19f59382ce9240c7aec`  
		Last Modified: Thu, 25 Sep 2025 18:49:27 GMT  
		Size: 25.5 KB (25460 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.7.7` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:6746518814e510b28bd7dd517195f648529da869ed42524ed7f5e92349dfbc54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.8 MB (207787017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e40eb8fcf90dc30bd981d04f1906aa9ab03f7cfdca8042011520a76b5a16d8f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:17 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:19 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 17:21:19 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.7.7.68
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b243d4603c9fb10873c5c8071c63750ba2ef471941549af64a0e9b750990555`  
		Last Modified: Thu, 25 Sep 2025 17:40:02 GMT  
		Size: 7.6 MB (7577255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829ddc07aee5da355b3e9f621bb5a1ab52f8e89bb194c0562e178b1302ea61a3`  
		Last Modified: Thu, 25 Sep 2025 18:49:56 GMT  
		Size: 172.0 MB (171978270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d97c4d247a31661f8a3e325ec93579864a9387514d044966fb94fc8f5a9704`  
		Last Modified: Thu, 25 Sep 2025 17:40:01 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9a1cbed902526a98c24edac85a7de58184d45cac51ea3462c88858d01f743b`  
		Last Modified: Thu, 25 Sep 2025 17:40:02 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bc58932d6fbb2946acfc63f25b647cb8ecf9173c9dcbfcab667c30f9021467`  
		Last Modified: Thu, 25 Sep 2025 17:40:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40145640226783b4fa4a000af6670d5264b7b371c41c3ee485ca08cb5f8f3ec`  
		Last Modified: Thu, 25 Sep 2025 17:40:01 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043e525e1c360f6690a8c4760e474ee33537cf3a4ed3bf0355fc35bad848f9c1`  
		Last Modified: Thu, 25 Sep 2025 17:40:01 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0f526c3cd32aa9a095e13ee8090d39c575580da66df75b5c32b06c5f7db1c08a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7df6fe6d09b8c911d4fa679713ab237bd52cf501548efab0c820f717941615a4`

```dockerfile
```

-	Layers:
	-	`sha256:a07f926872d4924a19972bb2d6ecb84f3ffb6a2d398a06be76cf9f6af60d627e`  
		Last Modified: Thu, 25 Sep 2025 18:49:30 GMT  
		Size: 25.6 KB (25649 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.7.7-jammy`

```console
$ docker pull clickhouse@sha256:09ed91ad70e952664c6bd0162149865681d42ab0d75db30e8b35256adb72963b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.7.7-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:6bb0972af794c51cd257cec37ff8fb2bc0585972398596bfe043dd74fc47c7ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221873228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45c844005318524dcde3dc199412ccc2b5987b7c6a398bb62356d055dfe63705`
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
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.7.7.68
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fcdcbe58c9000f60fbbd97b9c476d599cc9fb9a5b78995b368361badcb1194e`  
		Last Modified: Thu, 25 Sep 2025 17:40:26 GMT  
		Size: 7.6 MB (7598481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0302f8ab0fa5c939b2444dd3b6169eda23d4dabef613fb0f4040607f16bd52a4`  
		Last Modified: Thu, 25 Sep 2025 18:50:02 GMT  
		Size: 183.9 MB (183867788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ed5371ab3e6289a59f3ba06e5ace31e101319cb4d0d80222540350f6d24426`  
		Last Modified: Thu, 25 Sep 2025 17:40:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b6c29ab3bd6eaefe7b6bb7cb0afd19b324b662f8cf01574c7a9d48e129ac57`  
		Last Modified: Thu, 25 Sep 2025 17:40:25 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a663001f0e3ee3ded89f4dcea562b36ae70f5efabeeb84e4204ffd818f407c87`  
		Last Modified: Thu, 25 Sep 2025 17:40:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2278ee103d75b0f3fff12c113541676a7bd3b6b95e772ff65f3e60eced55b3b`  
		Last Modified: Thu, 25 Sep 2025 17:40:26 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1048cb093d408574524c2db35d765ccd67612b5a3199772c288aa09df4d96c76`  
		Last Modified: Thu, 25 Sep 2025 17:40:26 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.7-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:de370f920364dd41bb6de3629a2af4a6b0778b13dae8987a092b7a3cb2585b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee0b70ac8fe94c416eadc25a56dc6a1fc660887f6e47cd37ae26c97dfb36f53`

```dockerfile
```

-	Layers:
	-	`sha256:65340b8583184dd5fe44f052d3bf95890b4e2f552792c19f59382ce9240c7aec`  
		Last Modified: Thu, 25 Sep 2025 18:49:27 GMT  
		Size: 25.5 KB (25460 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.7.7-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:6746518814e510b28bd7dd517195f648529da869ed42524ed7f5e92349dfbc54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.8 MB (207787017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e40eb8fcf90dc30bd981d04f1906aa9ab03f7cfdca8042011520a76b5a16d8f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:17 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:19 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 17:21:19 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.7.7.68
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b243d4603c9fb10873c5c8071c63750ba2ef471941549af64a0e9b750990555`  
		Last Modified: Thu, 25 Sep 2025 17:40:02 GMT  
		Size: 7.6 MB (7577255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829ddc07aee5da355b3e9f621bb5a1ab52f8e89bb194c0562e178b1302ea61a3`  
		Last Modified: Thu, 25 Sep 2025 18:49:56 GMT  
		Size: 172.0 MB (171978270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d97c4d247a31661f8a3e325ec93579864a9387514d044966fb94fc8f5a9704`  
		Last Modified: Thu, 25 Sep 2025 17:40:01 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9a1cbed902526a98c24edac85a7de58184d45cac51ea3462c88858d01f743b`  
		Last Modified: Thu, 25 Sep 2025 17:40:02 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bc58932d6fbb2946acfc63f25b647cb8ecf9173c9dcbfcab667c30f9021467`  
		Last Modified: Thu, 25 Sep 2025 17:40:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40145640226783b4fa4a000af6670d5264b7b371c41c3ee485ca08cb5f8f3ec`  
		Last Modified: Thu, 25 Sep 2025 17:40:01 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043e525e1c360f6690a8c4760e474ee33537cf3a4ed3bf0355fc35bad848f9c1`  
		Last Modified: Thu, 25 Sep 2025 17:40:01 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.7-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0f526c3cd32aa9a095e13ee8090d39c575580da66df75b5c32b06c5f7db1c08a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7df6fe6d09b8c911d4fa679713ab237bd52cf501548efab0c820f717941615a4`

```dockerfile
```

-	Layers:
	-	`sha256:a07f926872d4924a19972bb2d6ecb84f3ffb6a2d398a06be76cf9f6af60d627e`  
		Last Modified: Thu, 25 Sep 2025 18:49:30 GMT  
		Size: 25.6 KB (25649 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.7.7.68`

```console
$ docker pull clickhouse@sha256:09ed91ad70e952664c6bd0162149865681d42ab0d75db30e8b35256adb72963b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.7.7.68` - linux; amd64

```console
$ docker pull clickhouse@sha256:6bb0972af794c51cd257cec37ff8fb2bc0585972398596bfe043dd74fc47c7ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221873228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45c844005318524dcde3dc199412ccc2b5987b7c6a398bb62356d055dfe63705`
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
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.7.7.68
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fcdcbe58c9000f60fbbd97b9c476d599cc9fb9a5b78995b368361badcb1194e`  
		Last Modified: Thu, 25 Sep 2025 17:40:26 GMT  
		Size: 7.6 MB (7598481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0302f8ab0fa5c939b2444dd3b6169eda23d4dabef613fb0f4040607f16bd52a4`  
		Last Modified: Thu, 25 Sep 2025 18:50:02 GMT  
		Size: 183.9 MB (183867788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ed5371ab3e6289a59f3ba06e5ace31e101319cb4d0d80222540350f6d24426`  
		Last Modified: Thu, 25 Sep 2025 17:40:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b6c29ab3bd6eaefe7b6bb7cb0afd19b324b662f8cf01574c7a9d48e129ac57`  
		Last Modified: Thu, 25 Sep 2025 17:40:25 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a663001f0e3ee3ded89f4dcea562b36ae70f5efabeeb84e4204ffd818f407c87`  
		Last Modified: Thu, 25 Sep 2025 17:40:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2278ee103d75b0f3fff12c113541676a7bd3b6b95e772ff65f3e60eced55b3b`  
		Last Modified: Thu, 25 Sep 2025 17:40:26 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1048cb093d408574524c2db35d765ccd67612b5a3199772c288aa09df4d96c76`  
		Last Modified: Thu, 25 Sep 2025 17:40:26 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.7.68` - unknown; unknown

```console
$ docker pull clickhouse@sha256:de370f920364dd41bb6de3629a2af4a6b0778b13dae8987a092b7a3cb2585b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee0b70ac8fe94c416eadc25a56dc6a1fc660887f6e47cd37ae26c97dfb36f53`

```dockerfile
```

-	Layers:
	-	`sha256:65340b8583184dd5fe44f052d3bf95890b4e2f552792c19f59382ce9240c7aec`  
		Last Modified: Thu, 25 Sep 2025 18:49:27 GMT  
		Size: 25.5 KB (25460 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.7.7.68` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:6746518814e510b28bd7dd517195f648529da869ed42524ed7f5e92349dfbc54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.8 MB (207787017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e40eb8fcf90dc30bd981d04f1906aa9ab03f7cfdca8042011520a76b5a16d8f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:17 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:19 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 17:21:19 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.7.7.68
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b243d4603c9fb10873c5c8071c63750ba2ef471941549af64a0e9b750990555`  
		Last Modified: Thu, 25 Sep 2025 17:40:02 GMT  
		Size: 7.6 MB (7577255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829ddc07aee5da355b3e9f621bb5a1ab52f8e89bb194c0562e178b1302ea61a3`  
		Last Modified: Thu, 25 Sep 2025 18:49:56 GMT  
		Size: 172.0 MB (171978270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d97c4d247a31661f8a3e325ec93579864a9387514d044966fb94fc8f5a9704`  
		Last Modified: Thu, 25 Sep 2025 17:40:01 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9a1cbed902526a98c24edac85a7de58184d45cac51ea3462c88858d01f743b`  
		Last Modified: Thu, 25 Sep 2025 17:40:02 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bc58932d6fbb2946acfc63f25b647cb8ecf9173c9dcbfcab667c30f9021467`  
		Last Modified: Thu, 25 Sep 2025 17:40:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40145640226783b4fa4a000af6670d5264b7b371c41c3ee485ca08cb5f8f3ec`  
		Last Modified: Thu, 25 Sep 2025 17:40:01 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043e525e1c360f6690a8c4760e474ee33537cf3a4ed3bf0355fc35bad848f9c1`  
		Last Modified: Thu, 25 Sep 2025 17:40:01 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.7.68` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0f526c3cd32aa9a095e13ee8090d39c575580da66df75b5c32b06c5f7db1c08a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7df6fe6d09b8c911d4fa679713ab237bd52cf501548efab0c820f717941615a4`

```dockerfile
```

-	Layers:
	-	`sha256:a07f926872d4924a19972bb2d6ecb84f3ffb6a2d398a06be76cf9f6af60d627e`  
		Last Modified: Thu, 25 Sep 2025 18:49:30 GMT  
		Size: 25.6 KB (25649 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.7.7.68-jammy`

```console
$ docker pull clickhouse@sha256:09ed91ad70e952664c6bd0162149865681d42ab0d75db30e8b35256adb72963b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.7.7.68-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:6bb0972af794c51cd257cec37ff8fb2bc0585972398596bfe043dd74fc47c7ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221873228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45c844005318524dcde3dc199412ccc2b5987b7c6a398bb62356d055dfe63705`
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
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.7.7.68
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fcdcbe58c9000f60fbbd97b9c476d599cc9fb9a5b78995b368361badcb1194e`  
		Last Modified: Thu, 25 Sep 2025 17:40:26 GMT  
		Size: 7.6 MB (7598481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0302f8ab0fa5c939b2444dd3b6169eda23d4dabef613fb0f4040607f16bd52a4`  
		Last Modified: Thu, 25 Sep 2025 18:50:02 GMT  
		Size: 183.9 MB (183867788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ed5371ab3e6289a59f3ba06e5ace31e101319cb4d0d80222540350f6d24426`  
		Last Modified: Thu, 25 Sep 2025 17:40:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b6c29ab3bd6eaefe7b6bb7cb0afd19b324b662f8cf01574c7a9d48e129ac57`  
		Last Modified: Thu, 25 Sep 2025 17:40:25 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a663001f0e3ee3ded89f4dcea562b36ae70f5efabeeb84e4204ffd818f407c87`  
		Last Modified: Thu, 25 Sep 2025 17:40:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2278ee103d75b0f3fff12c113541676a7bd3b6b95e772ff65f3e60eced55b3b`  
		Last Modified: Thu, 25 Sep 2025 17:40:26 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1048cb093d408574524c2db35d765ccd67612b5a3199772c288aa09df4d96c76`  
		Last Modified: Thu, 25 Sep 2025 17:40:26 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.7.68-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:de370f920364dd41bb6de3629a2af4a6b0778b13dae8987a092b7a3cb2585b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee0b70ac8fe94c416eadc25a56dc6a1fc660887f6e47cd37ae26c97dfb36f53`

```dockerfile
```

-	Layers:
	-	`sha256:65340b8583184dd5fe44f052d3bf95890b4e2f552792c19f59382ce9240c7aec`  
		Last Modified: Thu, 25 Sep 2025 18:49:27 GMT  
		Size: 25.5 KB (25460 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.7.7.68-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:6746518814e510b28bd7dd517195f648529da869ed42524ed7f5e92349dfbc54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.8 MB (207787017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e40eb8fcf90dc30bd981d04f1906aa9ab03f7cfdca8042011520a76b5a16d8f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:17 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:19 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 17:21:19 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.7.7.68
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b243d4603c9fb10873c5c8071c63750ba2ef471941549af64a0e9b750990555`  
		Last Modified: Thu, 25 Sep 2025 17:40:02 GMT  
		Size: 7.6 MB (7577255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829ddc07aee5da355b3e9f621bb5a1ab52f8e89bb194c0562e178b1302ea61a3`  
		Last Modified: Thu, 25 Sep 2025 18:49:56 GMT  
		Size: 172.0 MB (171978270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d97c4d247a31661f8a3e325ec93579864a9387514d044966fb94fc8f5a9704`  
		Last Modified: Thu, 25 Sep 2025 17:40:01 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9a1cbed902526a98c24edac85a7de58184d45cac51ea3462c88858d01f743b`  
		Last Modified: Thu, 25 Sep 2025 17:40:02 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bc58932d6fbb2946acfc63f25b647cb8ecf9173c9dcbfcab667c30f9021467`  
		Last Modified: Thu, 25 Sep 2025 17:40:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40145640226783b4fa4a000af6670d5264b7b371c41c3ee485ca08cb5f8f3ec`  
		Last Modified: Thu, 25 Sep 2025 17:40:01 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043e525e1c360f6690a8c4760e474ee33537cf3a4ed3bf0355fc35bad848f9c1`  
		Last Modified: Thu, 25 Sep 2025 17:40:01 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.7.68-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0f526c3cd32aa9a095e13ee8090d39c575580da66df75b5c32b06c5f7db1c08a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7df6fe6d09b8c911d4fa679713ab237bd52cf501548efab0c820f717941615a4`

```dockerfile
```

-	Layers:
	-	`sha256:a07f926872d4924a19972bb2d6ecb84f3ffb6a2d398a06be76cf9f6af60d627e`  
		Last Modified: Thu, 25 Sep 2025 18:49:30 GMT  
		Size: 25.6 KB (25649 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8`

```console
$ docker pull clickhouse@sha256:217e9643d44076676669a12ec4c8aa6e43c33a68e24c5400358cfbf98174568f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8` - linux; amd64

```console
$ docker pull clickhouse@sha256:af3aef7502fa1c8a5598030c3efd562cc9d1c2f7098d05d5bdf998f2b841bac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227759917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:407e4509f562e8b0351a5f719f3f0cf025f6cb227639ba3410be5f1a579e3de6`
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
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580422714323634b611a3fb8e44e73f8afecca28874ed636a4da68d011d04a33`  
		Last Modified: Thu, 25 Sep 2025 17:39:46 GMT  
		Size: 7.6 MB (7598477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acdb8ce9ea1d3e217a551662c8d886f0e4e75c384b8d756c20afca3133128d5`  
		Last Modified: Thu, 25 Sep 2025 17:39:58 GMT  
		Size: 189.8 MB (189754480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b93ce6e1cd16537660e7a840cefd7288af66f50e29520da80812db8a96f859f`  
		Last Modified: Thu, 25 Sep 2025 17:39:44 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4a142b373583cac3d6ff628ab96cc5ce62dcc20634182cc35ffe189f5ecbd6`  
		Last Modified: Thu, 25 Sep 2025 17:39:45 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e853a8448be63a282281b7d3532179b999e06c71f71193ace44ca7663e7ac7f3`  
		Last Modified: Thu, 25 Sep 2025 17:39:44 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bb954bdec7066f13486a0ee79ae48235e89cb9541bc29e1df89d91321fd145`  
		Last Modified: Thu, 25 Sep 2025 17:39:45 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a09584ea34ca452b5835dbfa91afae8b438ec674592e458a5591be2bb02594c`  
		Last Modified: Thu, 25 Sep 2025 17:39:46 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:78442cad9b27dabbdd92a482c474550fdd5495a71428c3c78692bb8d987b1ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cca2e460a8c84fb617d84a2f865422b2d5f4876871eccdb119782d3d04f41a8`

```dockerfile
```

-	Layers:
	-	`sha256:e77fe48b80219b8db20edf27d679ad5f5e267f5698627fccfc280d4d982be475`  
		Last Modified: Thu, 25 Sep 2025 18:49:46 GMT  
		Size: 26.7 KB (26671 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:cbb5add2832e1d452312b2c77bd5a68e8cf808177eccfc32fc473cc7de1fc330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212485993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d623b7b3b9bc0b020a0ae2eacddb5e9abf59a2e4c35edb4fcb44dcb2ad4e76`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:17 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:19 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 17:21:19 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1b04584cd6f09afaec0004bdd62a59044c994531e926d76408bb5410b3db73`  
		Last Modified: Thu, 25 Sep 2025 17:39:05 GMT  
		Size: 7.6 MB (7577256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d24ae17e68eaeb435578ea2a5dffb42d7583313ba4bb8c1025b168d9b26f946`  
		Last Modified: Thu, 25 Sep 2025 17:39:55 GMT  
		Size: 176.7 MB (176677246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6469e1f2f367bbb723894875fa831da3ce2afb6f9274d10ffff94eb6c54f2306`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4efd299d81e2e52296288bc512546b1d40e1acf7511269a7bb7acbe69e8f094`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6764477384e76a92e9d7bf6f5ace44f0100ae89d363c543363f8dd2baa64b751`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a55eeddab67d88ebc34168bf1125738b99a1e4e27b642c3cec836de7c6f2dd6`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233b658515568da00a5c6b8cfb7273f1f8bcdfd6c94f71f6582f6547a7fff3d3`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ee9717135a59b2d5c616a27f57cff095a38a92132426a14e3899f5d147c742be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b8f960e6f48c4f4d6760bd939c49a61b2cd0c568d550441e026dd77e1bd0dc`

```dockerfile
```

-	Layers:
	-	`sha256:83660230c78a1f467c12d7ee78f111edf66589c53fed4593422435572363ec20`  
		Last Modified: Thu, 25 Sep 2025 18:49:49 GMT  
		Size: 26.9 KB (26906 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8-jammy`

```console
$ docker pull clickhouse@sha256:217e9643d44076676669a12ec4c8aa6e43c33a68e24c5400358cfbf98174568f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:af3aef7502fa1c8a5598030c3efd562cc9d1c2f7098d05d5bdf998f2b841bac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227759917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:407e4509f562e8b0351a5f719f3f0cf025f6cb227639ba3410be5f1a579e3de6`
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
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580422714323634b611a3fb8e44e73f8afecca28874ed636a4da68d011d04a33`  
		Last Modified: Thu, 25 Sep 2025 17:39:46 GMT  
		Size: 7.6 MB (7598477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acdb8ce9ea1d3e217a551662c8d886f0e4e75c384b8d756c20afca3133128d5`  
		Last Modified: Thu, 25 Sep 2025 17:39:58 GMT  
		Size: 189.8 MB (189754480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b93ce6e1cd16537660e7a840cefd7288af66f50e29520da80812db8a96f859f`  
		Last Modified: Thu, 25 Sep 2025 17:39:44 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4a142b373583cac3d6ff628ab96cc5ce62dcc20634182cc35ffe189f5ecbd6`  
		Last Modified: Thu, 25 Sep 2025 17:39:45 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e853a8448be63a282281b7d3532179b999e06c71f71193ace44ca7663e7ac7f3`  
		Last Modified: Thu, 25 Sep 2025 17:39:44 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bb954bdec7066f13486a0ee79ae48235e89cb9541bc29e1df89d91321fd145`  
		Last Modified: Thu, 25 Sep 2025 17:39:45 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a09584ea34ca452b5835dbfa91afae8b438ec674592e458a5591be2bb02594c`  
		Last Modified: Thu, 25 Sep 2025 17:39:46 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:78442cad9b27dabbdd92a482c474550fdd5495a71428c3c78692bb8d987b1ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cca2e460a8c84fb617d84a2f865422b2d5f4876871eccdb119782d3d04f41a8`

```dockerfile
```

-	Layers:
	-	`sha256:e77fe48b80219b8db20edf27d679ad5f5e267f5698627fccfc280d4d982be475`  
		Last Modified: Thu, 25 Sep 2025 18:49:46 GMT  
		Size: 26.7 KB (26671 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:cbb5add2832e1d452312b2c77bd5a68e8cf808177eccfc32fc473cc7de1fc330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212485993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d623b7b3b9bc0b020a0ae2eacddb5e9abf59a2e4c35edb4fcb44dcb2ad4e76`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:17 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:19 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 17:21:19 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1b04584cd6f09afaec0004bdd62a59044c994531e926d76408bb5410b3db73`  
		Last Modified: Thu, 25 Sep 2025 17:39:05 GMT  
		Size: 7.6 MB (7577256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d24ae17e68eaeb435578ea2a5dffb42d7583313ba4bb8c1025b168d9b26f946`  
		Last Modified: Thu, 25 Sep 2025 17:39:55 GMT  
		Size: 176.7 MB (176677246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6469e1f2f367bbb723894875fa831da3ce2afb6f9274d10ffff94eb6c54f2306`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4efd299d81e2e52296288bc512546b1d40e1acf7511269a7bb7acbe69e8f094`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6764477384e76a92e9d7bf6f5ace44f0100ae89d363c543363f8dd2baa64b751`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a55eeddab67d88ebc34168bf1125738b99a1e4e27b642c3cec836de7c6f2dd6`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233b658515568da00a5c6b8cfb7273f1f8bcdfd6c94f71f6582f6547a7fff3d3`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ee9717135a59b2d5c616a27f57cff095a38a92132426a14e3899f5d147c742be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b8f960e6f48c4f4d6760bd939c49a61b2cd0c568d550441e026dd77e1bd0dc`

```dockerfile
```

-	Layers:
	-	`sha256:83660230c78a1f467c12d7ee78f111edf66589c53fed4593422435572363ec20`  
		Last Modified: Thu, 25 Sep 2025 18:49:49 GMT  
		Size: 26.9 KB (26906 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.7`

```console
$ docker pull clickhouse@sha256:217e9643d44076676669a12ec4c8aa6e43c33a68e24c5400358cfbf98174568f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.7` - linux; amd64

```console
$ docker pull clickhouse@sha256:af3aef7502fa1c8a5598030c3efd562cc9d1c2f7098d05d5bdf998f2b841bac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227759917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:407e4509f562e8b0351a5f719f3f0cf025f6cb227639ba3410be5f1a579e3de6`
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
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580422714323634b611a3fb8e44e73f8afecca28874ed636a4da68d011d04a33`  
		Last Modified: Thu, 25 Sep 2025 17:39:46 GMT  
		Size: 7.6 MB (7598477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acdb8ce9ea1d3e217a551662c8d886f0e4e75c384b8d756c20afca3133128d5`  
		Last Modified: Thu, 25 Sep 2025 17:39:58 GMT  
		Size: 189.8 MB (189754480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b93ce6e1cd16537660e7a840cefd7288af66f50e29520da80812db8a96f859f`  
		Last Modified: Thu, 25 Sep 2025 17:39:44 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4a142b373583cac3d6ff628ab96cc5ce62dcc20634182cc35ffe189f5ecbd6`  
		Last Modified: Thu, 25 Sep 2025 17:39:45 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e853a8448be63a282281b7d3532179b999e06c71f71193ace44ca7663e7ac7f3`  
		Last Modified: Thu, 25 Sep 2025 17:39:44 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bb954bdec7066f13486a0ee79ae48235e89cb9541bc29e1df89d91321fd145`  
		Last Modified: Thu, 25 Sep 2025 17:39:45 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a09584ea34ca452b5835dbfa91afae8b438ec674592e458a5591be2bb02594c`  
		Last Modified: Thu, 25 Sep 2025 17:39:46 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:78442cad9b27dabbdd92a482c474550fdd5495a71428c3c78692bb8d987b1ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cca2e460a8c84fb617d84a2f865422b2d5f4876871eccdb119782d3d04f41a8`

```dockerfile
```

-	Layers:
	-	`sha256:e77fe48b80219b8db20edf27d679ad5f5e267f5698627fccfc280d4d982be475`  
		Last Modified: Thu, 25 Sep 2025 18:49:46 GMT  
		Size: 26.7 KB (26671 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.7` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:cbb5add2832e1d452312b2c77bd5a68e8cf808177eccfc32fc473cc7de1fc330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212485993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d623b7b3b9bc0b020a0ae2eacddb5e9abf59a2e4c35edb4fcb44dcb2ad4e76`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:17 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:19 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 17:21:19 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1b04584cd6f09afaec0004bdd62a59044c994531e926d76408bb5410b3db73`  
		Last Modified: Thu, 25 Sep 2025 17:39:05 GMT  
		Size: 7.6 MB (7577256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d24ae17e68eaeb435578ea2a5dffb42d7583313ba4bb8c1025b168d9b26f946`  
		Last Modified: Thu, 25 Sep 2025 17:39:55 GMT  
		Size: 176.7 MB (176677246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6469e1f2f367bbb723894875fa831da3ce2afb6f9274d10ffff94eb6c54f2306`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4efd299d81e2e52296288bc512546b1d40e1acf7511269a7bb7acbe69e8f094`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6764477384e76a92e9d7bf6f5ace44f0100ae89d363c543363f8dd2baa64b751`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a55eeddab67d88ebc34168bf1125738b99a1e4e27b642c3cec836de7c6f2dd6`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233b658515568da00a5c6b8cfb7273f1f8bcdfd6c94f71f6582f6547a7fff3d3`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ee9717135a59b2d5c616a27f57cff095a38a92132426a14e3899f5d147c742be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b8f960e6f48c4f4d6760bd939c49a61b2cd0c568d550441e026dd77e1bd0dc`

```dockerfile
```

-	Layers:
	-	`sha256:83660230c78a1f467c12d7ee78f111edf66589c53fed4593422435572363ec20`  
		Last Modified: Thu, 25 Sep 2025 18:49:49 GMT  
		Size: 26.9 KB (26906 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.7-jammy`

```console
$ docker pull clickhouse@sha256:217e9643d44076676669a12ec4c8aa6e43c33a68e24c5400358cfbf98174568f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.7-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:af3aef7502fa1c8a5598030c3efd562cc9d1c2f7098d05d5bdf998f2b841bac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227759917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:407e4509f562e8b0351a5f719f3f0cf025f6cb227639ba3410be5f1a579e3de6`
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
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580422714323634b611a3fb8e44e73f8afecca28874ed636a4da68d011d04a33`  
		Last Modified: Thu, 25 Sep 2025 17:39:46 GMT  
		Size: 7.6 MB (7598477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acdb8ce9ea1d3e217a551662c8d886f0e4e75c384b8d756c20afca3133128d5`  
		Last Modified: Thu, 25 Sep 2025 17:39:58 GMT  
		Size: 189.8 MB (189754480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b93ce6e1cd16537660e7a840cefd7288af66f50e29520da80812db8a96f859f`  
		Last Modified: Thu, 25 Sep 2025 17:39:44 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4a142b373583cac3d6ff628ab96cc5ce62dcc20634182cc35ffe189f5ecbd6`  
		Last Modified: Thu, 25 Sep 2025 17:39:45 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e853a8448be63a282281b7d3532179b999e06c71f71193ace44ca7663e7ac7f3`  
		Last Modified: Thu, 25 Sep 2025 17:39:44 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bb954bdec7066f13486a0ee79ae48235e89cb9541bc29e1df89d91321fd145`  
		Last Modified: Thu, 25 Sep 2025 17:39:45 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a09584ea34ca452b5835dbfa91afae8b438ec674592e458a5591be2bb02594c`  
		Last Modified: Thu, 25 Sep 2025 17:39:46 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.7-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:78442cad9b27dabbdd92a482c474550fdd5495a71428c3c78692bb8d987b1ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cca2e460a8c84fb617d84a2f865422b2d5f4876871eccdb119782d3d04f41a8`

```dockerfile
```

-	Layers:
	-	`sha256:e77fe48b80219b8db20edf27d679ad5f5e267f5698627fccfc280d4d982be475`  
		Last Modified: Thu, 25 Sep 2025 18:49:46 GMT  
		Size: 26.7 KB (26671 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.7-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:cbb5add2832e1d452312b2c77bd5a68e8cf808177eccfc32fc473cc7de1fc330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212485993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d623b7b3b9bc0b020a0ae2eacddb5e9abf59a2e4c35edb4fcb44dcb2ad4e76`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:17 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:19 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 17:21:19 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1b04584cd6f09afaec0004bdd62a59044c994531e926d76408bb5410b3db73`  
		Last Modified: Thu, 25 Sep 2025 17:39:05 GMT  
		Size: 7.6 MB (7577256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d24ae17e68eaeb435578ea2a5dffb42d7583313ba4bb8c1025b168d9b26f946`  
		Last Modified: Thu, 25 Sep 2025 17:39:55 GMT  
		Size: 176.7 MB (176677246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6469e1f2f367bbb723894875fa831da3ce2afb6f9274d10ffff94eb6c54f2306`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4efd299d81e2e52296288bc512546b1d40e1acf7511269a7bb7acbe69e8f094`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6764477384e76a92e9d7bf6f5ace44f0100ae89d363c543363f8dd2baa64b751`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a55eeddab67d88ebc34168bf1125738b99a1e4e27b642c3cec836de7c6f2dd6`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233b658515568da00a5c6b8cfb7273f1f8bcdfd6c94f71f6582f6547a7fff3d3`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.7-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ee9717135a59b2d5c616a27f57cff095a38a92132426a14e3899f5d147c742be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b8f960e6f48c4f4d6760bd939c49a61b2cd0c568d550441e026dd77e1bd0dc`

```dockerfile
```

-	Layers:
	-	`sha256:83660230c78a1f467c12d7ee78f111edf66589c53fed4593422435572363ec20`  
		Last Modified: Thu, 25 Sep 2025 18:49:49 GMT  
		Size: 26.9 KB (26906 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.7.3`

```console
$ docker pull clickhouse@sha256:217e9643d44076676669a12ec4c8aa6e43c33a68e24c5400358cfbf98174568f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.7.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:af3aef7502fa1c8a5598030c3efd562cc9d1c2f7098d05d5bdf998f2b841bac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227759917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:407e4509f562e8b0351a5f719f3f0cf025f6cb227639ba3410be5f1a579e3de6`
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
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580422714323634b611a3fb8e44e73f8afecca28874ed636a4da68d011d04a33`  
		Last Modified: Thu, 25 Sep 2025 17:39:46 GMT  
		Size: 7.6 MB (7598477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acdb8ce9ea1d3e217a551662c8d886f0e4e75c384b8d756c20afca3133128d5`  
		Last Modified: Thu, 25 Sep 2025 17:39:58 GMT  
		Size: 189.8 MB (189754480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b93ce6e1cd16537660e7a840cefd7288af66f50e29520da80812db8a96f859f`  
		Last Modified: Thu, 25 Sep 2025 17:39:44 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4a142b373583cac3d6ff628ab96cc5ce62dcc20634182cc35ffe189f5ecbd6`  
		Last Modified: Thu, 25 Sep 2025 17:39:45 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e853a8448be63a282281b7d3532179b999e06c71f71193ace44ca7663e7ac7f3`  
		Last Modified: Thu, 25 Sep 2025 17:39:44 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bb954bdec7066f13486a0ee79ae48235e89cb9541bc29e1df89d91321fd145`  
		Last Modified: Thu, 25 Sep 2025 17:39:45 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a09584ea34ca452b5835dbfa91afae8b438ec674592e458a5591be2bb02594c`  
		Last Modified: Thu, 25 Sep 2025 17:39:46 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.7.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:78442cad9b27dabbdd92a482c474550fdd5495a71428c3c78692bb8d987b1ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cca2e460a8c84fb617d84a2f865422b2d5f4876871eccdb119782d3d04f41a8`

```dockerfile
```

-	Layers:
	-	`sha256:e77fe48b80219b8db20edf27d679ad5f5e267f5698627fccfc280d4d982be475`  
		Last Modified: Thu, 25 Sep 2025 18:49:46 GMT  
		Size: 26.7 KB (26671 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.7.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:cbb5add2832e1d452312b2c77bd5a68e8cf808177eccfc32fc473cc7de1fc330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212485993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d623b7b3b9bc0b020a0ae2eacddb5e9abf59a2e4c35edb4fcb44dcb2ad4e76`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:17 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:19 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 17:21:19 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1b04584cd6f09afaec0004bdd62a59044c994531e926d76408bb5410b3db73`  
		Last Modified: Thu, 25 Sep 2025 17:39:05 GMT  
		Size: 7.6 MB (7577256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d24ae17e68eaeb435578ea2a5dffb42d7583313ba4bb8c1025b168d9b26f946`  
		Last Modified: Thu, 25 Sep 2025 17:39:55 GMT  
		Size: 176.7 MB (176677246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6469e1f2f367bbb723894875fa831da3ce2afb6f9274d10ffff94eb6c54f2306`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4efd299d81e2e52296288bc512546b1d40e1acf7511269a7bb7acbe69e8f094`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6764477384e76a92e9d7bf6f5ace44f0100ae89d363c543363f8dd2baa64b751`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a55eeddab67d88ebc34168bf1125738b99a1e4e27b642c3cec836de7c6f2dd6`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233b658515568da00a5c6b8cfb7273f1f8bcdfd6c94f71f6582f6547a7fff3d3`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.7.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ee9717135a59b2d5c616a27f57cff095a38a92132426a14e3899f5d147c742be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b8f960e6f48c4f4d6760bd939c49a61b2cd0c568d550441e026dd77e1bd0dc`

```dockerfile
```

-	Layers:
	-	`sha256:83660230c78a1f467c12d7ee78f111edf66589c53fed4593422435572363ec20`  
		Last Modified: Thu, 25 Sep 2025 18:49:49 GMT  
		Size: 26.9 KB (26906 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.7.3-jammy`

```console
$ docker pull clickhouse@sha256:217e9643d44076676669a12ec4c8aa6e43c33a68e24c5400358cfbf98174568f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.7.3-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:af3aef7502fa1c8a5598030c3efd562cc9d1c2f7098d05d5bdf998f2b841bac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227759917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:407e4509f562e8b0351a5f719f3f0cf025f6cb227639ba3410be5f1a579e3de6`
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
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580422714323634b611a3fb8e44e73f8afecca28874ed636a4da68d011d04a33`  
		Last Modified: Thu, 25 Sep 2025 17:39:46 GMT  
		Size: 7.6 MB (7598477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acdb8ce9ea1d3e217a551662c8d886f0e4e75c384b8d756c20afca3133128d5`  
		Last Modified: Thu, 25 Sep 2025 17:39:58 GMT  
		Size: 189.8 MB (189754480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b93ce6e1cd16537660e7a840cefd7288af66f50e29520da80812db8a96f859f`  
		Last Modified: Thu, 25 Sep 2025 17:39:44 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4a142b373583cac3d6ff628ab96cc5ce62dcc20634182cc35ffe189f5ecbd6`  
		Last Modified: Thu, 25 Sep 2025 17:39:45 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e853a8448be63a282281b7d3532179b999e06c71f71193ace44ca7663e7ac7f3`  
		Last Modified: Thu, 25 Sep 2025 17:39:44 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bb954bdec7066f13486a0ee79ae48235e89cb9541bc29e1df89d91321fd145`  
		Last Modified: Thu, 25 Sep 2025 17:39:45 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a09584ea34ca452b5835dbfa91afae8b438ec674592e458a5591be2bb02594c`  
		Last Modified: Thu, 25 Sep 2025 17:39:46 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.7.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:78442cad9b27dabbdd92a482c474550fdd5495a71428c3c78692bb8d987b1ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cca2e460a8c84fb617d84a2f865422b2d5f4876871eccdb119782d3d04f41a8`

```dockerfile
```

-	Layers:
	-	`sha256:e77fe48b80219b8db20edf27d679ad5f5e267f5698627fccfc280d4d982be475`  
		Last Modified: Thu, 25 Sep 2025 18:49:46 GMT  
		Size: 26.7 KB (26671 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.7.3-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:cbb5add2832e1d452312b2c77bd5a68e8cf808177eccfc32fc473cc7de1fc330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212485993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d623b7b3b9bc0b020a0ae2eacddb5e9abf59a2e4c35edb4fcb44dcb2ad4e76`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:17 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:19 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 17:21:19 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1b04584cd6f09afaec0004bdd62a59044c994531e926d76408bb5410b3db73`  
		Last Modified: Thu, 25 Sep 2025 17:39:05 GMT  
		Size: 7.6 MB (7577256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d24ae17e68eaeb435578ea2a5dffb42d7583313ba4bb8c1025b168d9b26f946`  
		Last Modified: Thu, 25 Sep 2025 17:39:55 GMT  
		Size: 176.7 MB (176677246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6469e1f2f367bbb723894875fa831da3ce2afb6f9274d10ffff94eb6c54f2306`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4efd299d81e2e52296288bc512546b1d40e1acf7511269a7bb7acbe69e8f094`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6764477384e76a92e9d7bf6f5ace44f0100ae89d363c543363f8dd2baa64b751`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a55eeddab67d88ebc34168bf1125738b99a1e4e27b642c3cec836de7c6f2dd6`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233b658515568da00a5c6b8cfb7273f1f8bcdfd6c94f71f6582f6547a7fff3d3`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.7.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ee9717135a59b2d5c616a27f57cff095a38a92132426a14e3899f5d147c742be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b8f960e6f48c4f4d6760bd939c49a61b2cd0c568d550441e026dd77e1bd0dc`

```dockerfile
```

-	Layers:
	-	`sha256:83660230c78a1f467c12d7ee78f111edf66589c53fed4593422435572363ec20`  
		Last Modified: Thu, 25 Sep 2025 18:49:49 GMT  
		Size: 26.9 KB (26906 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:jammy`

```console
$ docker pull clickhouse@sha256:217e9643d44076676669a12ec4c8aa6e43c33a68e24c5400358cfbf98174568f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:af3aef7502fa1c8a5598030c3efd562cc9d1c2f7098d05d5bdf998f2b841bac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227759917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:407e4509f562e8b0351a5f719f3f0cf025f6cb227639ba3410be5f1a579e3de6`
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
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580422714323634b611a3fb8e44e73f8afecca28874ed636a4da68d011d04a33`  
		Last Modified: Thu, 25 Sep 2025 17:39:46 GMT  
		Size: 7.6 MB (7598477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acdb8ce9ea1d3e217a551662c8d886f0e4e75c384b8d756c20afca3133128d5`  
		Last Modified: Thu, 25 Sep 2025 17:39:58 GMT  
		Size: 189.8 MB (189754480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b93ce6e1cd16537660e7a840cefd7288af66f50e29520da80812db8a96f859f`  
		Last Modified: Thu, 25 Sep 2025 17:39:44 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4a142b373583cac3d6ff628ab96cc5ce62dcc20634182cc35ffe189f5ecbd6`  
		Last Modified: Thu, 25 Sep 2025 17:39:45 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e853a8448be63a282281b7d3532179b999e06c71f71193ace44ca7663e7ac7f3`  
		Last Modified: Thu, 25 Sep 2025 17:39:44 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bb954bdec7066f13486a0ee79ae48235e89cb9541bc29e1df89d91321fd145`  
		Last Modified: Thu, 25 Sep 2025 17:39:45 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a09584ea34ca452b5835dbfa91afae8b438ec674592e458a5591be2bb02594c`  
		Last Modified: Thu, 25 Sep 2025 17:39:46 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:78442cad9b27dabbdd92a482c474550fdd5495a71428c3c78692bb8d987b1ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cca2e460a8c84fb617d84a2f865422b2d5f4876871eccdb119782d3d04f41a8`

```dockerfile
```

-	Layers:
	-	`sha256:e77fe48b80219b8db20edf27d679ad5f5e267f5698627fccfc280d4d982be475`  
		Last Modified: Thu, 25 Sep 2025 18:49:46 GMT  
		Size: 26.7 KB (26671 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:cbb5add2832e1d452312b2c77bd5a68e8cf808177eccfc32fc473cc7de1fc330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212485993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d623b7b3b9bc0b020a0ae2eacddb5e9abf59a2e4c35edb4fcb44dcb2ad4e76`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:17 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:19 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 17:21:19 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1b04584cd6f09afaec0004bdd62a59044c994531e926d76408bb5410b3db73`  
		Last Modified: Thu, 25 Sep 2025 17:39:05 GMT  
		Size: 7.6 MB (7577256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d24ae17e68eaeb435578ea2a5dffb42d7583313ba4bb8c1025b168d9b26f946`  
		Last Modified: Thu, 25 Sep 2025 17:39:55 GMT  
		Size: 176.7 MB (176677246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6469e1f2f367bbb723894875fa831da3ce2afb6f9274d10ffff94eb6c54f2306`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4efd299d81e2e52296288bc512546b1d40e1acf7511269a7bb7acbe69e8f094`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6764477384e76a92e9d7bf6f5ace44f0100ae89d363c543363f8dd2baa64b751`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a55eeddab67d88ebc34168bf1125738b99a1e4e27b642c3cec836de7c6f2dd6`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233b658515568da00a5c6b8cfb7273f1f8bcdfd6c94f71f6582f6547a7fff3d3`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ee9717135a59b2d5c616a27f57cff095a38a92132426a14e3899f5d147c742be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b8f960e6f48c4f4d6760bd939c49a61b2cd0c568d550441e026dd77e1bd0dc`

```dockerfile
```

-	Layers:
	-	`sha256:83660230c78a1f467c12d7ee78f111edf66589c53fed4593422435572363ec20`  
		Last Modified: Thu, 25 Sep 2025 18:49:49 GMT  
		Size: 26.9 KB (26906 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:217e9643d44076676669a12ec4c8aa6e43c33a68e24c5400358cfbf98174568f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

```console
$ docker pull clickhouse@sha256:af3aef7502fa1c8a5598030c3efd562cc9d1c2f7098d05d5bdf998f2b841bac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227759917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:407e4509f562e8b0351a5f719f3f0cf025f6cb227639ba3410be5f1a579e3de6`
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
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580422714323634b611a3fb8e44e73f8afecca28874ed636a4da68d011d04a33`  
		Last Modified: Thu, 25 Sep 2025 17:39:46 GMT  
		Size: 7.6 MB (7598477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acdb8ce9ea1d3e217a551662c8d886f0e4e75c384b8d756c20afca3133128d5`  
		Last Modified: Thu, 25 Sep 2025 17:39:58 GMT  
		Size: 189.8 MB (189754480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b93ce6e1cd16537660e7a840cefd7288af66f50e29520da80812db8a96f859f`  
		Last Modified: Thu, 25 Sep 2025 17:39:44 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4a142b373583cac3d6ff628ab96cc5ce62dcc20634182cc35ffe189f5ecbd6`  
		Last Modified: Thu, 25 Sep 2025 17:39:45 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e853a8448be63a282281b7d3532179b999e06c71f71193ace44ca7663e7ac7f3`  
		Last Modified: Thu, 25 Sep 2025 17:39:44 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bb954bdec7066f13486a0ee79ae48235e89cb9541bc29e1df89d91321fd145`  
		Last Modified: Thu, 25 Sep 2025 17:39:45 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a09584ea34ca452b5835dbfa91afae8b438ec674592e458a5591be2bb02594c`  
		Last Modified: Thu, 25 Sep 2025 17:39:46 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:78442cad9b27dabbdd92a482c474550fdd5495a71428c3c78692bb8d987b1ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cca2e460a8c84fb617d84a2f865422b2d5f4876871eccdb119782d3d04f41a8`

```dockerfile
```

-	Layers:
	-	`sha256:e77fe48b80219b8db20edf27d679ad5f5e267f5698627fccfc280d4d982be475`  
		Last Modified: Thu, 25 Sep 2025 18:49:46 GMT  
		Size: 26.7 KB (26671 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:cbb5add2832e1d452312b2c77bd5a68e8cf808177eccfc32fc473cc7de1fc330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212485993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d623b7b3b9bc0b020a0ae2eacddb5e9abf59a2e4c35edb4fcb44dcb2ad4e76`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:17 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:19 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 17:21:19 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1b04584cd6f09afaec0004bdd62a59044c994531e926d76408bb5410b3db73`  
		Last Modified: Thu, 25 Sep 2025 17:39:05 GMT  
		Size: 7.6 MB (7577256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d24ae17e68eaeb435578ea2a5dffb42d7583313ba4bb8c1025b168d9b26f946`  
		Last Modified: Thu, 25 Sep 2025 17:39:55 GMT  
		Size: 176.7 MB (176677246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6469e1f2f367bbb723894875fa831da3ce2afb6f9274d10ffff94eb6c54f2306`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4efd299d81e2e52296288bc512546b1d40e1acf7511269a7bb7acbe69e8f094`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6764477384e76a92e9d7bf6f5ace44f0100ae89d363c543363f8dd2baa64b751`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a55eeddab67d88ebc34168bf1125738b99a1e4e27b642c3cec836de7c6f2dd6`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233b658515568da00a5c6b8cfb7273f1f8bcdfd6c94f71f6582f6547a7fff3d3`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ee9717135a59b2d5c616a27f57cff095a38a92132426a14e3899f5d147c742be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b8f960e6f48c4f4d6760bd939c49a61b2cd0c568d550441e026dd77e1bd0dc`

```dockerfile
```

-	Layers:
	-	`sha256:83660230c78a1f467c12d7ee78f111edf66589c53fed4593422435572363ec20`  
		Last Modified: Thu, 25 Sep 2025 18:49:49 GMT  
		Size: 26.9 KB (26906 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts`

```console
$ docker pull clickhouse@sha256:217e9643d44076676669a12ec4c8aa6e43c33a68e24c5400358cfbf98174568f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts` - linux; amd64

```console
$ docker pull clickhouse@sha256:af3aef7502fa1c8a5598030c3efd562cc9d1c2f7098d05d5bdf998f2b841bac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227759917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:407e4509f562e8b0351a5f719f3f0cf025f6cb227639ba3410be5f1a579e3de6`
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
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580422714323634b611a3fb8e44e73f8afecca28874ed636a4da68d011d04a33`  
		Last Modified: Thu, 25 Sep 2025 17:39:46 GMT  
		Size: 7.6 MB (7598477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acdb8ce9ea1d3e217a551662c8d886f0e4e75c384b8d756c20afca3133128d5`  
		Last Modified: Thu, 25 Sep 2025 17:39:58 GMT  
		Size: 189.8 MB (189754480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b93ce6e1cd16537660e7a840cefd7288af66f50e29520da80812db8a96f859f`  
		Last Modified: Thu, 25 Sep 2025 17:39:44 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4a142b373583cac3d6ff628ab96cc5ce62dcc20634182cc35ffe189f5ecbd6`  
		Last Modified: Thu, 25 Sep 2025 17:39:45 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e853a8448be63a282281b7d3532179b999e06c71f71193ace44ca7663e7ac7f3`  
		Last Modified: Thu, 25 Sep 2025 17:39:44 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bb954bdec7066f13486a0ee79ae48235e89cb9541bc29e1df89d91321fd145`  
		Last Modified: Thu, 25 Sep 2025 17:39:45 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a09584ea34ca452b5835dbfa91afae8b438ec674592e458a5591be2bb02594c`  
		Last Modified: Thu, 25 Sep 2025 17:39:46 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:78442cad9b27dabbdd92a482c474550fdd5495a71428c3c78692bb8d987b1ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cca2e460a8c84fb617d84a2f865422b2d5f4876871eccdb119782d3d04f41a8`

```dockerfile
```

-	Layers:
	-	`sha256:e77fe48b80219b8db20edf27d679ad5f5e267f5698627fccfc280d4d982be475`  
		Last Modified: Thu, 25 Sep 2025 18:49:46 GMT  
		Size: 26.7 KB (26671 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:cbb5add2832e1d452312b2c77bd5a68e8cf808177eccfc32fc473cc7de1fc330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212485993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d623b7b3b9bc0b020a0ae2eacddb5e9abf59a2e4c35edb4fcb44dcb2ad4e76`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:17 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:19 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 17:21:19 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1b04584cd6f09afaec0004bdd62a59044c994531e926d76408bb5410b3db73`  
		Last Modified: Thu, 25 Sep 2025 17:39:05 GMT  
		Size: 7.6 MB (7577256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d24ae17e68eaeb435578ea2a5dffb42d7583313ba4bb8c1025b168d9b26f946`  
		Last Modified: Thu, 25 Sep 2025 17:39:55 GMT  
		Size: 176.7 MB (176677246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6469e1f2f367bbb723894875fa831da3ce2afb6f9274d10ffff94eb6c54f2306`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4efd299d81e2e52296288bc512546b1d40e1acf7511269a7bb7acbe69e8f094`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6764477384e76a92e9d7bf6f5ace44f0100ae89d363c543363f8dd2baa64b751`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a55eeddab67d88ebc34168bf1125738b99a1e4e27b642c3cec836de7c6f2dd6`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233b658515568da00a5c6b8cfb7273f1f8bcdfd6c94f71f6582f6547a7fff3d3`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ee9717135a59b2d5c616a27f57cff095a38a92132426a14e3899f5d147c742be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b8f960e6f48c4f4d6760bd939c49a61b2cd0c568d550441e026dd77e1bd0dc`

```dockerfile
```

-	Layers:
	-	`sha256:83660230c78a1f467c12d7ee78f111edf66589c53fed4593422435572363ec20`  
		Last Modified: Thu, 25 Sep 2025 18:49:49 GMT  
		Size: 26.9 KB (26906 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts-jammy`

```console
$ docker pull clickhouse@sha256:217e9643d44076676669a12ec4c8aa6e43c33a68e24c5400358cfbf98174568f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:af3aef7502fa1c8a5598030c3efd562cc9d1c2f7098d05d5bdf998f2b841bac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227759917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:407e4509f562e8b0351a5f719f3f0cf025f6cb227639ba3410be5f1a579e3de6`
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
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580422714323634b611a3fb8e44e73f8afecca28874ed636a4da68d011d04a33`  
		Last Modified: Thu, 25 Sep 2025 17:39:46 GMT  
		Size: 7.6 MB (7598477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acdb8ce9ea1d3e217a551662c8d886f0e4e75c384b8d756c20afca3133128d5`  
		Last Modified: Thu, 25 Sep 2025 17:39:58 GMT  
		Size: 189.8 MB (189754480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b93ce6e1cd16537660e7a840cefd7288af66f50e29520da80812db8a96f859f`  
		Last Modified: Thu, 25 Sep 2025 17:39:44 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4a142b373583cac3d6ff628ab96cc5ce62dcc20634182cc35ffe189f5ecbd6`  
		Last Modified: Thu, 25 Sep 2025 17:39:45 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e853a8448be63a282281b7d3532179b999e06c71f71193ace44ca7663e7ac7f3`  
		Last Modified: Thu, 25 Sep 2025 17:39:44 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bb954bdec7066f13486a0ee79ae48235e89cb9541bc29e1df89d91321fd145`  
		Last Modified: Thu, 25 Sep 2025 17:39:45 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a09584ea34ca452b5835dbfa91afae8b438ec674592e458a5591be2bb02594c`  
		Last Modified: Thu, 25 Sep 2025 17:39:46 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:78442cad9b27dabbdd92a482c474550fdd5495a71428c3c78692bb8d987b1ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cca2e460a8c84fb617d84a2f865422b2d5f4876871eccdb119782d3d04f41a8`

```dockerfile
```

-	Layers:
	-	`sha256:e77fe48b80219b8db20edf27d679ad5f5e267f5698627fccfc280d4d982be475`  
		Last Modified: Thu, 25 Sep 2025 18:49:46 GMT  
		Size: 26.7 KB (26671 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:cbb5add2832e1d452312b2c77bd5a68e8cf808177eccfc32fc473cc7de1fc330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212485993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d623b7b3b9bc0b020a0ae2eacddb5e9abf59a2e4c35edb4fcb44dcb2ad4e76`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:17 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:19 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 17:21:19 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1b04584cd6f09afaec0004bdd62a59044c994531e926d76408bb5410b3db73`  
		Last Modified: Thu, 25 Sep 2025 17:39:05 GMT  
		Size: 7.6 MB (7577256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d24ae17e68eaeb435578ea2a5dffb42d7583313ba4bb8c1025b168d9b26f946`  
		Last Modified: Thu, 25 Sep 2025 17:39:55 GMT  
		Size: 176.7 MB (176677246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6469e1f2f367bbb723894875fa831da3ce2afb6f9274d10ffff94eb6c54f2306`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4efd299d81e2e52296288bc512546b1d40e1acf7511269a7bb7acbe69e8f094`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6764477384e76a92e9d7bf6f5ace44f0100ae89d363c543363f8dd2baa64b751`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a55eeddab67d88ebc34168bf1125738b99a1e4e27b642c3cec836de7c6f2dd6`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233b658515568da00a5c6b8cfb7273f1f8bcdfd6c94f71f6582f6547a7fff3d3`  
		Last Modified: Thu, 25 Sep 2025 17:39:04 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ee9717135a59b2d5c616a27f57cff095a38a92132426a14e3899f5d147c742be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b8f960e6f48c4f4d6760bd939c49a61b2cd0c568d550441e026dd77e1bd0dc`

```dockerfile
```

-	Layers:
	-	`sha256:83660230c78a1f467c12d7ee78f111edf66589c53fed4593422435572363ec20`  
		Last Modified: Thu, 25 Sep 2025 18:49:49 GMT  
		Size: 26.9 KB (26906 bytes)  
		MIME: application/vnd.in-toto+json
