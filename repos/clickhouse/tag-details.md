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
-	[`clickhouse:25.6.11`](#clickhouse25611)
-	[`clickhouse:25.6.11-jammy`](#clickhouse25611-jammy)
-	[`clickhouse:25.6.11.18`](#clickhouse2561118)
-	[`clickhouse:25.6.11.18-jammy`](#clickhouse2561118-jammy)
-	[`clickhouse:25.7`](#clickhouse257)
-	[`clickhouse:25.7-jammy`](#clickhouse257-jammy)
-	[`clickhouse:25.7.6`](#clickhouse2576)
-	[`clickhouse:25.7.6-jammy`](#clickhouse2576-jammy)
-	[`clickhouse:25.7.6.21`](#clickhouse257621)
-	[`clickhouse:25.7.6.21-jammy`](#clickhouse257621-jammy)
-	[`clickhouse:25.8`](#clickhouse258)
-	[`clickhouse:25.8-jammy`](#clickhouse258-jammy)
-	[`clickhouse:25.8.2`](#clickhouse2582)
-	[`clickhouse:25.8.2-jammy`](#clickhouse2582-jammy)
-	[`clickhouse:25.8.2.29`](#clickhouse258229)
-	[`clickhouse:25.8.2.29-jammy`](#clickhouse258229-jammy)
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
$ docker pull clickhouse@sha256:281b753b54e8a2e1a9f414cbf9e42942b909ce1a320d7878e67c75933a148873
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6` - linux; amd64

```console
$ docker pull clickhouse@sha256:86c0359552e3173897b257bfcc53c55c0b6bc67c8bc9c5b42b8e64cce3e1077f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212100500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90b4f73fbc026a78d369fca3e5dd1bf5c3746e2febfbe392906a9c4e79ff9658`
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
# Thu, 11 Sep 2025 16:06:16 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 11 Sep 2025 16:06:16 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
ARG REPO_CHANNEL=stable
# Thu, 11 Sep 2025 16:06:16 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 11 Sep 2025 16:06:16 GMT
ARG VERSION=25.6.11.18
# Thu, 11 Sep 2025 16:06:16 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.11.18 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.11.18 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.11.18 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
ENV LANG=en_US.UTF-8
# Thu, 11 Sep 2025 16:06:16 GMT
ENV TZ=UTC
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.11.18 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 11 Sep 2025 16:06:16 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 11 Sep 2025 16:06:16 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 11 Sep 2025 16:06:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a707e2e9b26f157e0b1557495ac76013f4e78afb134ae5db452ef58b92732e93`  
		Last Modified: Thu, 11 Sep 2025 17:08:40 GMT  
		Size: 7.2 MB (7151688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8eb7060d1713fd42abc775326d0f6a8d435021f9077468d1724b4d4986202a1`  
		Last Modified: Thu, 11 Sep 2025 17:09:04 GMT  
		Size: 174.5 MB (174541854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1ab06edb17ba4e359aca485b338177b14fa1b7eb6dbf5fe7685b6718ed527f`  
		Last Modified: Thu, 11 Sep 2025 17:08:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2d07ba3cdab0e48051b636e3aa8d46a2944849fe547c32dc44ac4ac3d909b5`  
		Last Modified: Thu, 11 Sep 2025 17:08:38 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c4f56b05470e299062787fd7e253636f954ce1c32a261ce9fe34ba2932b61c`  
		Last Modified: Thu, 11 Sep 2025 17:08:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814b4f01dd7c6055b42f84b266f822f30c7b2ac0823ecf1ff43081cf2097743d`  
		Last Modified: Thu, 11 Sep 2025 17:08:37 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43dca555fc1d752f31f9c89d8d07c0bdd88b4732a7633fa088d6b79e4cc732db`  
		Last Modified: Thu, 11 Sep 2025 17:08:36 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e460c5372596daddfdaedcc5214245a714528a5930d0a7ad8c3f6fae36f7bc6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38e08aa45f80f37ce92fd96da9dda5b05905acd302a805720e456e72f0fed8a4`

```dockerfile
```

-	Layers:
	-	`sha256:6cff905352150aa1a659e355bd68f6a89159ac65bf02aa39948be691c433d599`  
		Last Modified: Thu, 11 Sep 2025 18:49:29 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.6` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:26cc159ddc450657a3e087b554eec9ff4b939d0be8e3570a52254bbb44cf6f3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.3 MB (198250239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9cfe31b94df0c045639c24ad8a4422b00a50b2246b53ceb9ed62843dd3ec95f`
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
# Thu, 11 Sep 2025 16:06:16 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 11 Sep 2025 16:06:16 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
ARG REPO_CHANNEL=stable
# Thu, 11 Sep 2025 16:06:16 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 11 Sep 2025 16:06:16 GMT
ARG VERSION=25.6.11.18
# Thu, 11 Sep 2025 16:06:16 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.11.18 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.11.18 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.11.18 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
ENV LANG=en_US.UTF-8
# Thu, 11 Sep 2025 16:06:16 GMT
ENV TZ=UTC
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.11.18 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 11 Sep 2025 16:06:16 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 11 Sep 2025 16:06:16 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 11 Sep 2025 16:06:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b6fc097e987cf080907725bee128816b79b5a91a6b2b279d16330178a1eedd`  
		Last Modified: Thu, 11 Sep 2025 17:08:11 GMT  
		Size: 7.1 MB (7127935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05eb04471900ac0874de5cf8a175405ec0109764d939baa04063af0fa42f8251`  
		Last Modified: Thu, 11 Sep 2025 17:08:22 GMT  
		Size: 162.9 MB (162890812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64dfbefe8c2cd54ac5c0df1827a4d9d668cb0298b7b62cb7caed215b61afb0c7`  
		Last Modified: Thu, 11 Sep 2025 17:08:11 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93843183b381cae40511d60d204acacc5850a76191e293f7379e8a456a7d97e8`  
		Last Modified: Thu, 11 Sep 2025 17:08:13 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb23dc55bbdc2e9458c319211cc31031df4b80e7c1f47531f406662e71099b9b`  
		Last Modified: Thu, 11 Sep 2025 17:08:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0121aabd0230a749e00c9642b021ab472b5dd9f8531909ca17cfcf8d01a0b7`  
		Last Modified: Thu, 11 Sep 2025 17:08:12 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07bfe3aa67e0578f9cd348b39e4eaf4e69b4e49879f09d0fdfdf34ec53056d9c`  
		Last Modified: Thu, 11 Sep 2025 17:08:12 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6` - unknown; unknown

```console
$ docker pull clickhouse@sha256:7e5d5e22499af31003d7d87e027fb3ca40f689eaee1c9c6dc46075417f47dc9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09447d8d4bfa07595b1bb6d3fed04fdb7853099cdcf3536045dd835b2aada0f1`

```dockerfile
```

-	Layers:
	-	`sha256:3d5cb526dec856b5f18234d5b0f47ce3c251078414ef0d87a0ba472e26b16f62`  
		Last Modified: Thu, 11 Sep 2025 18:49:32 GMT  
		Size: 25.5 KB (25465 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.6-jammy`

```console
$ docker pull clickhouse@sha256:281b753b54e8a2e1a9f414cbf9e42942b909ce1a320d7878e67c75933a148873
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:86c0359552e3173897b257bfcc53c55c0b6bc67c8bc9c5b42b8e64cce3e1077f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212100500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90b4f73fbc026a78d369fca3e5dd1bf5c3746e2febfbe392906a9c4e79ff9658`
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
# Thu, 11 Sep 2025 16:06:16 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 11 Sep 2025 16:06:16 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
ARG REPO_CHANNEL=stable
# Thu, 11 Sep 2025 16:06:16 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 11 Sep 2025 16:06:16 GMT
ARG VERSION=25.6.11.18
# Thu, 11 Sep 2025 16:06:16 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.11.18 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.11.18 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.11.18 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
ENV LANG=en_US.UTF-8
# Thu, 11 Sep 2025 16:06:16 GMT
ENV TZ=UTC
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.11.18 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 11 Sep 2025 16:06:16 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 11 Sep 2025 16:06:16 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 11 Sep 2025 16:06:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a707e2e9b26f157e0b1557495ac76013f4e78afb134ae5db452ef58b92732e93`  
		Last Modified: Thu, 11 Sep 2025 17:08:40 GMT  
		Size: 7.2 MB (7151688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8eb7060d1713fd42abc775326d0f6a8d435021f9077468d1724b4d4986202a1`  
		Last Modified: Thu, 11 Sep 2025 17:09:04 GMT  
		Size: 174.5 MB (174541854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1ab06edb17ba4e359aca485b338177b14fa1b7eb6dbf5fe7685b6718ed527f`  
		Last Modified: Thu, 11 Sep 2025 17:08:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2d07ba3cdab0e48051b636e3aa8d46a2944849fe547c32dc44ac4ac3d909b5`  
		Last Modified: Thu, 11 Sep 2025 17:08:38 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c4f56b05470e299062787fd7e253636f954ce1c32a261ce9fe34ba2932b61c`  
		Last Modified: Thu, 11 Sep 2025 17:08:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814b4f01dd7c6055b42f84b266f822f30c7b2ac0823ecf1ff43081cf2097743d`  
		Last Modified: Thu, 11 Sep 2025 17:08:37 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43dca555fc1d752f31f9c89d8d07c0bdd88b4732a7633fa088d6b79e4cc732db`  
		Last Modified: Thu, 11 Sep 2025 17:08:36 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e460c5372596daddfdaedcc5214245a714528a5930d0a7ad8c3f6fae36f7bc6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38e08aa45f80f37ce92fd96da9dda5b05905acd302a805720e456e72f0fed8a4`

```dockerfile
```

-	Layers:
	-	`sha256:6cff905352150aa1a659e355bd68f6a89159ac65bf02aa39948be691c433d599`  
		Last Modified: Thu, 11 Sep 2025 18:49:29 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.6-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:26cc159ddc450657a3e087b554eec9ff4b939d0be8e3570a52254bbb44cf6f3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.3 MB (198250239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9cfe31b94df0c045639c24ad8a4422b00a50b2246b53ceb9ed62843dd3ec95f`
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
# Thu, 11 Sep 2025 16:06:16 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 11 Sep 2025 16:06:16 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
ARG REPO_CHANNEL=stable
# Thu, 11 Sep 2025 16:06:16 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 11 Sep 2025 16:06:16 GMT
ARG VERSION=25.6.11.18
# Thu, 11 Sep 2025 16:06:16 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.11.18 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.11.18 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.11.18 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
ENV LANG=en_US.UTF-8
# Thu, 11 Sep 2025 16:06:16 GMT
ENV TZ=UTC
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.11.18 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 11 Sep 2025 16:06:16 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 11 Sep 2025 16:06:16 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 11 Sep 2025 16:06:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b6fc097e987cf080907725bee128816b79b5a91a6b2b279d16330178a1eedd`  
		Last Modified: Thu, 11 Sep 2025 17:08:11 GMT  
		Size: 7.1 MB (7127935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05eb04471900ac0874de5cf8a175405ec0109764d939baa04063af0fa42f8251`  
		Last Modified: Thu, 11 Sep 2025 17:08:22 GMT  
		Size: 162.9 MB (162890812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64dfbefe8c2cd54ac5c0df1827a4d9d668cb0298b7b62cb7caed215b61afb0c7`  
		Last Modified: Thu, 11 Sep 2025 17:08:11 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93843183b381cae40511d60d204acacc5850a76191e293f7379e8a456a7d97e8`  
		Last Modified: Thu, 11 Sep 2025 17:08:13 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb23dc55bbdc2e9458c319211cc31031df4b80e7c1f47531f406662e71099b9b`  
		Last Modified: Thu, 11 Sep 2025 17:08:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0121aabd0230a749e00c9642b021ab472b5dd9f8531909ca17cfcf8d01a0b7`  
		Last Modified: Thu, 11 Sep 2025 17:08:12 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07bfe3aa67e0578f9cd348b39e4eaf4e69b4e49879f09d0fdfdf34ec53056d9c`  
		Last Modified: Thu, 11 Sep 2025 17:08:12 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:7e5d5e22499af31003d7d87e027fb3ca40f689eaee1c9c6dc46075417f47dc9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09447d8d4bfa07595b1bb6d3fed04fdb7853099cdcf3536045dd835b2aada0f1`

```dockerfile
```

-	Layers:
	-	`sha256:3d5cb526dec856b5f18234d5b0f47ce3c251078414ef0d87a0ba472e26b16f62`  
		Last Modified: Thu, 11 Sep 2025 18:49:32 GMT  
		Size: 25.5 KB (25465 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.6.11`

```console
$ docker pull clickhouse@sha256:281b753b54e8a2e1a9f414cbf9e42942b909ce1a320d7878e67c75933a148873
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6.11` - linux; amd64

```console
$ docker pull clickhouse@sha256:86c0359552e3173897b257bfcc53c55c0b6bc67c8bc9c5b42b8e64cce3e1077f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212100500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90b4f73fbc026a78d369fca3e5dd1bf5c3746e2febfbe392906a9c4e79ff9658`
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
# Thu, 11 Sep 2025 16:06:16 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 11 Sep 2025 16:06:16 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
ARG REPO_CHANNEL=stable
# Thu, 11 Sep 2025 16:06:16 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 11 Sep 2025 16:06:16 GMT
ARG VERSION=25.6.11.18
# Thu, 11 Sep 2025 16:06:16 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.11.18 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.11.18 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.11.18 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
ENV LANG=en_US.UTF-8
# Thu, 11 Sep 2025 16:06:16 GMT
ENV TZ=UTC
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.11.18 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 11 Sep 2025 16:06:16 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 11 Sep 2025 16:06:16 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 11 Sep 2025 16:06:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a707e2e9b26f157e0b1557495ac76013f4e78afb134ae5db452ef58b92732e93`  
		Last Modified: Thu, 11 Sep 2025 17:08:40 GMT  
		Size: 7.2 MB (7151688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8eb7060d1713fd42abc775326d0f6a8d435021f9077468d1724b4d4986202a1`  
		Last Modified: Thu, 11 Sep 2025 17:09:04 GMT  
		Size: 174.5 MB (174541854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1ab06edb17ba4e359aca485b338177b14fa1b7eb6dbf5fe7685b6718ed527f`  
		Last Modified: Thu, 11 Sep 2025 17:08:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2d07ba3cdab0e48051b636e3aa8d46a2944849fe547c32dc44ac4ac3d909b5`  
		Last Modified: Thu, 11 Sep 2025 17:08:38 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c4f56b05470e299062787fd7e253636f954ce1c32a261ce9fe34ba2932b61c`  
		Last Modified: Thu, 11 Sep 2025 17:08:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814b4f01dd7c6055b42f84b266f822f30c7b2ac0823ecf1ff43081cf2097743d`  
		Last Modified: Thu, 11 Sep 2025 17:08:37 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43dca555fc1d752f31f9c89d8d07c0bdd88b4732a7633fa088d6b79e4cc732db`  
		Last Modified: Thu, 11 Sep 2025 17:08:36 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.11` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e460c5372596daddfdaedcc5214245a714528a5930d0a7ad8c3f6fae36f7bc6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38e08aa45f80f37ce92fd96da9dda5b05905acd302a805720e456e72f0fed8a4`

```dockerfile
```

-	Layers:
	-	`sha256:6cff905352150aa1a659e355bd68f6a89159ac65bf02aa39948be691c433d599`  
		Last Modified: Thu, 11 Sep 2025 18:49:29 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.6.11` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:26cc159ddc450657a3e087b554eec9ff4b939d0be8e3570a52254bbb44cf6f3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.3 MB (198250239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9cfe31b94df0c045639c24ad8a4422b00a50b2246b53ceb9ed62843dd3ec95f`
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
# Thu, 11 Sep 2025 16:06:16 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 11 Sep 2025 16:06:16 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
ARG REPO_CHANNEL=stable
# Thu, 11 Sep 2025 16:06:16 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 11 Sep 2025 16:06:16 GMT
ARG VERSION=25.6.11.18
# Thu, 11 Sep 2025 16:06:16 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.11.18 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.11.18 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.11.18 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
ENV LANG=en_US.UTF-8
# Thu, 11 Sep 2025 16:06:16 GMT
ENV TZ=UTC
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.11.18 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 11 Sep 2025 16:06:16 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 11 Sep 2025 16:06:16 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 11 Sep 2025 16:06:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b6fc097e987cf080907725bee128816b79b5a91a6b2b279d16330178a1eedd`  
		Last Modified: Thu, 11 Sep 2025 17:08:11 GMT  
		Size: 7.1 MB (7127935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05eb04471900ac0874de5cf8a175405ec0109764d939baa04063af0fa42f8251`  
		Last Modified: Thu, 11 Sep 2025 17:08:22 GMT  
		Size: 162.9 MB (162890812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64dfbefe8c2cd54ac5c0df1827a4d9d668cb0298b7b62cb7caed215b61afb0c7`  
		Last Modified: Thu, 11 Sep 2025 17:08:11 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93843183b381cae40511d60d204acacc5850a76191e293f7379e8a456a7d97e8`  
		Last Modified: Thu, 11 Sep 2025 17:08:13 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb23dc55bbdc2e9458c319211cc31031df4b80e7c1f47531f406662e71099b9b`  
		Last Modified: Thu, 11 Sep 2025 17:08:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0121aabd0230a749e00c9642b021ab472b5dd9f8531909ca17cfcf8d01a0b7`  
		Last Modified: Thu, 11 Sep 2025 17:08:12 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07bfe3aa67e0578f9cd348b39e4eaf4e69b4e49879f09d0fdfdf34ec53056d9c`  
		Last Modified: Thu, 11 Sep 2025 17:08:12 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.11` - unknown; unknown

```console
$ docker pull clickhouse@sha256:7e5d5e22499af31003d7d87e027fb3ca40f689eaee1c9c6dc46075417f47dc9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09447d8d4bfa07595b1bb6d3fed04fdb7853099cdcf3536045dd835b2aada0f1`

```dockerfile
```

-	Layers:
	-	`sha256:3d5cb526dec856b5f18234d5b0f47ce3c251078414ef0d87a0ba472e26b16f62`  
		Last Modified: Thu, 11 Sep 2025 18:49:32 GMT  
		Size: 25.5 KB (25465 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.6.11-jammy`

```console
$ docker pull clickhouse@sha256:281b753b54e8a2e1a9f414cbf9e42942b909ce1a320d7878e67c75933a148873
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6.11-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:86c0359552e3173897b257bfcc53c55c0b6bc67c8bc9c5b42b8e64cce3e1077f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212100500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90b4f73fbc026a78d369fca3e5dd1bf5c3746e2febfbe392906a9c4e79ff9658`
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
# Thu, 11 Sep 2025 16:06:16 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 11 Sep 2025 16:06:16 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
ARG REPO_CHANNEL=stable
# Thu, 11 Sep 2025 16:06:16 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 11 Sep 2025 16:06:16 GMT
ARG VERSION=25.6.11.18
# Thu, 11 Sep 2025 16:06:16 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.11.18 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.11.18 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.11.18 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
ENV LANG=en_US.UTF-8
# Thu, 11 Sep 2025 16:06:16 GMT
ENV TZ=UTC
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.11.18 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 11 Sep 2025 16:06:16 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 11 Sep 2025 16:06:16 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 11 Sep 2025 16:06:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a707e2e9b26f157e0b1557495ac76013f4e78afb134ae5db452ef58b92732e93`  
		Last Modified: Thu, 11 Sep 2025 17:08:40 GMT  
		Size: 7.2 MB (7151688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8eb7060d1713fd42abc775326d0f6a8d435021f9077468d1724b4d4986202a1`  
		Last Modified: Thu, 11 Sep 2025 17:09:04 GMT  
		Size: 174.5 MB (174541854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1ab06edb17ba4e359aca485b338177b14fa1b7eb6dbf5fe7685b6718ed527f`  
		Last Modified: Thu, 11 Sep 2025 17:08:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2d07ba3cdab0e48051b636e3aa8d46a2944849fe547c32dc44ac4ac3d909b5`  
		Last Modified: Thu, 11 Sep 2025 17:08:38 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c4f56b05470e299062787fd7e253636f954ce1c32a261ce9fe34ba2932b61c`  
		Last Modified: Thu, 11 Sep 2025 17:08:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814b4f01dd7c6055b42f84b266f822f30c7b2ac0823ecf1ff43081cf2097743d`  
		Last Modified: Thu, 11 Sep 2025 17:08:37 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43dca555fc1d752f31f9c89d8d07c0bdd88b4732a7633fa088d6b79e4cc732db`  
		Last Modified: Thu, 11 Sep 2025 17:08:36 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.11-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e460c5372596daddfdaedcc5214245a714528a5930d0a7ad8c3f6fae36f7bc6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38e08aa45f80f37ce92fd96da9dda5b05905acd302a805720e456e72f0fed8a4`

```dockerfile
```

-	Layers:
	-	`sha256:6cff905352150aa1a659e355bd68f6a89159ac65bf02aa39948be691c433d599`  
		Last Modified: Thu, 11 Sep 2025 18:49:29 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.6.11-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:26cc159ddc450657a3e087b554eec9ff4b939d0be8e3570a52254bbb44cf6f3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.3 MB (198250239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9cfe31b94df0c045639c24ad8a4422b00a50b2246b53ceb9ed62843dd3ec95f`
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
# Thu, 11 Sep 2025 16:06:16 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 11 Sep 2025 16:06:16 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
ARG REPO_CHANNEL=stable
# Thu, 11 Sep 2025 16:06:16 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 11 Sep 2025 16:06:16 GMT
ARG VERSION=25.6.11.18
# Thu, 11 Sep 2025 16:06:16 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.11.18 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.11.18 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.11.18 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
ENV LANG=en_US.UTF-8
# Thu, 11 Sep 2025 16:06:16 GMT
ENV TZ=UTC
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.11.18 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 11 Sep 2025 16:06:16 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 11 Sep 2025 16:06:16 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 11 Sep 2025 16:06:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b6fc097e987cf080907725bee128816b79b5a91a6b2b279d16330178a1eedd`  
		Last Modified: Thu, 11 Sep 2025 17:08:11 GMT  
		Size: 7.1 MB (7127935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05eb04471900ac0874de5cf8a175405ec0109764d939baa04063af0fa42f8251`  
		Last Modified: Thu, 11 Sep 2025 17:08:22 GMT  
		Size: 162.9 MB (162890812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64dfbefe8c2cd54ac5c0df1827a4d9d668cb0298b7b62cb7caed215b61afb0c7`  
		Last Modified: Thu, 11 Sep 2025 17:08:11 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93843183b381cae40511d60d204acacc5850a76191e293f7379e8a456a7d97e8`  
		Last Modified: Thu, 11 Sep 2025 17:08:13 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb23dc55bbdc2e9458c319211cc31031df4b80e7c1f47531f406662e71099b9b`  
		Last Modified: Thu, 11 Sep 2025 17:08:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0121aabd0230a749e00c9642b021ab472b5dd9f8531909ca17cfcf8d01a0b7`  
		Last Modified: Thu, 11 Sep 2025 17:08:12 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07bfe3aa67e0578f9cd348b39e4eaf4e69b4e49879f09d0fdfdf34ec53056d9c`  
		Last Modified: Thu, 11 Sep 2025 17:08:12 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.11-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:7e5d5e22499af31003d7d87e027fb3ca40f689eaee1c9c6dc46075417f47dc9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09447d8d4bfa07595b1bb6d3fed04fdb7853099cdcf3536045dd835b2aada0f1`

```dockerfile
```

-	Layers:
	-	`sha256:3d5cb526dec856b5f18234d5b0f47ce3c251078414ef0d87a0ba472e26b16f62`  
		Last Modified: Thu, 11 Sep 2025 18:49:32 GMT  
		Size: 25.5 KB (25465 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.6.11.18`

```console
$ docker pull clickhouse@sha256:281b753b54e8a2e1a9f414cbf9e42942b909ce1a320d7878e67c75933a148873
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6.11.18` - linux; amd64

```console
$ docker pull clickhouse@sha256:86c0359552e3173897b257bfcc53c55c0b6bc67c8bc9c5b42b8e64cce3e1077f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212100500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90b4f73fbc026a78d369fca3e5dd1bf5c3746e2febfbe392906a9c4e79ff9658`
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
# Thu, 11 Sep 2025 16:06:16 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 11 Sep 2025 16:06:16 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
ARG REPO_CHANNEL=stable
# Thu, 11 Sep 2025 16:06:16 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 11 Sep 2025 16:06:16 GMT
ARG VERSION=25.6.11.18
# Thu, 11 Sep 2025 16:06:16 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.11.18 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.11.18 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.11.18 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
ENV LANG=en_US.UTF-8
# Thu, 11 Sep 2025 16:06:16 GMT
ENV TZ=UTC
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.11.18 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 11 Sep 2025 16:06:16 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 11 Sep 2025 16:06:16 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 11 Sep 2025 16:06:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a707e2e9b26f157e0b1557495ac76013f4e78afb134ae5db452ef58b92732e93`  
		Last Modified: Thu, 11 Sep 2025 17:08:40 GMT  
		Size: 7.2 MB (7151688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8eb7060d1713fd42abc775326d0f6a8d435021f9077468d1724b4d4986202a1`  
		Last Modified: Thu, 11 Sep 2025 17:09:04 GMT  
		Size: 174.5 MB (174541854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1ab06edb17ba4e359aca485b338177b14fa1b7eb6dbf5fe7685b6718ed527f`  
		Last Modified: Thu, 11 Sep 2025 17:08:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2d07ba3cdab0e48051b636e3aa8d46a2944849fe547c32dc44ac4ac3d909b5`  
		Last Modified: Thu, 11 Sep 2025 17:08:38 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c4f56b05470e299062787fd7e253636f954ce1c32a261ce9fe34ba2932b61c`  
		Last Modified: Thu, 11 Sep 2025 17:08:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814b4f01dd7c6055b42f84b266f822f30c7b2ac0823ecf1ff43081cf2097743d`  
		Last Modified: Thu, 11 Sep 2025 17:08:37 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43dca555fc1d752f31f9c89d8d07c0bdd88b4732a7633fa088d6b79e4cc732db`  
		Last Modified: Thu, 11 Sep 2025 17:08:36 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.11.18` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e460c5372596daddfdaedcc5214245a714528a5930d0a7ad8c3f6fae36f7bc6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38e08aa45f80f37ce92fd96da9dda5b05905acd302a805720e456e72f0fed8a4`

```dockerfile
```

-	Layers:
	-	`sha256:6cff905352150aa1a659e355bd68f6a89159ac65bf02aa39948be691c433d599`  
		Last Modified: Thu, 11 Sep 2025 18:49:29 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.6.11.18` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:26cc159ddc450657a3e087b554eec9ff4b939d0be8e3570a52254bbb44cf6f3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.3 MB (198250239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9cfe31b94df0c045639c24ad8a4422b00a50b2246b53ceb9ed62843dd3ec95f`
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
# Thu, 11 Sep 2025 16:06:16 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 11 Sep 2025 16:06:16 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
ARG REPO_CHANNEL=stable
# Thu, 11 Sep 2025 16:06:16 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 11 Sep 2025 16:06:16 GMT
ARG VERSION=25.6.11.18
# Thu, 11 Sep 2025 16:06:16 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.11.18 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.11.18 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.11.18 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
ENV LANG=en_US.UTF-8
# Thu, 11 Sep 2025 16:06:16 GMT
ENV TZ=UTC
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.11.18 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 11 Sep 2025 16:06:16 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 11 Sep 2025 16:06:16 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 11 Sep 2025 16:06:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b6fc097e987cf080907725bee128816b79b5a91a6b2b279d16330178a1eedd`  
		Last Modified: Thu, 11 Sep 2025 17:08:11 GMT  
		Size: 7.1 MB (7127935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05eb04471900ac0874de5cf8a175405ec0109764d939baa04063af0fa42f8251`  
		Last Modified: Thu, 11 Sep 2025 17:08:22 GMT  
		Size: 162.9 MB (162890812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64dfbefe8c2cd54ac5c0df1827a4d9d668cb0298b7b62cb7caed215b61afb0c7`  
		Last Modified: Thu, 11 Sep 2025 17:08:11 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93843183b381cae40511d60d204acacc5850a76191e293f7379e8a456a7d97e8`  
		Last Modified: Thu, 11 Sep 2025 17:08:13 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb23dc55bbdc2e9458c319211cc31031df4b80e7c1f47531f406662e71099b9b`  
		Last Modified: Thu, 11 Sep 2025 17:08:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0121aabd0230a749e00c9642b021ab472b5dd9f8531909ca17cfcf8d01a0b7`  
		Last Modified: Thu, 11 Sep 2025 17:08:12 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07bfe3aa67e0578f9cd348b39e4eaf4e69b4e49879f09d0fdfdf34ec53056d9c`  
		Last Modified: Thu, 11 Sep 2025 17:08:12 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.11.18` - unknown; unknown

```console
$ docker pull clickhouse@sha256:7e5d5e22499af31003d7d87e027fb3ca40f689eaee1c9c6dc46075417f47dc9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09447d8d4bfa07595b1bb6d3fed04fdb7853099cdcf3536045dd835b2aada0f1`

```dockerfile
```

-	Layers:
	-	`sha256:3d5cb526dec856b5f18234d5b0f47ce3c251078414ef0d87a0ba472e26b16f62`  
		Last Modified: Thu, 11 Sep 2025 18:49:32 GMT  
		Size: 25.5 KB (25465 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.6.11.18-jammy`

```console
$ docker pull clickhouse@sha256:281b753b54e8a2e1a9f414cbf9e42942b909ce1a320d7878e67c75933a148873
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6.11.18-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:86c0359552e3173897b257bfcc53c55c0b6bc67c8bc9c5b42b8e64cce3e1077f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212100500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90b4f73fbc026a78d369fca3e5dd1bf5c3746e2febfbe392906a9c4e79ff9658`
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
# Thu, 11 Sep 2025 16:06:16 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 11 Sep 2025 16:06:16 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
ARG REPO_CHANNEL=stable
# Thu, 11 Sep 2025 16:06:16 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 11 Sep 2025 16:06:16 GMT
ARG VERSION=25.6.11.18
# Thu, 11 Sep 2025 16:06:16 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.11.18 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.11.18 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.11.18 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
ENV LANG=en_US.UTF-8
# Thu, 11 Sep 2025 16:06:16 GMT
ENV TZ=UTC
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.11.18 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 11 Sep 2025 16:06:16 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 11 Sep 2025 16:06:16 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 11 Sep 2025 16:06:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a707e2e9b26f157e0b1557495ac76013f4e78afb134ae5db452ef58b92732e93`  
		Last Modified: Thu, 11 Sep 2025 17:08:40 GMT  
		Size: 7.2 MB (7151688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8eb7060d1713fd42abc775326d0f6a8d435021f9077468d1724b4d4986202a1`  
		Last Modified: Thu, 11 Sep 2025 17:09:04 GMT  
		Size: 174.5 MB (174541854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1ab06edb17ba4e359aca485b338177b14fa1b7eb6dbf5fe7685b6718ed527f`  
		Last Modified: Thu, 11 Sep 2025 17:08:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2d07ba3cdab0e48051b636e3aa8d46a2944849fe547c32dc44ac4ac3d909b5`  
		Last Modified: Thu, 11 Sep 2025 17:08:38 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c4f56b05470e299062787fd7e253636f954ce1c32a261ce9fe34ba2932b61c`  
		Last Modified: Thu, 11 Sep 2025 17:08:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814b4f01dd7c6055b42f84b266f822f30c7b2ac0823ecf1ff43081cf2097743d`  
		Last Modified: Thu, 11 Sep 2025 17:08:37 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43dca555fc1d752f31f9c89d8d07c0bdd88b4732a7633fa088d6b79e4cc732db`  
		Last Modified: Thu, 11 Sep 2025 17:08:36 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.11.18-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e460c5372596daddfdaedcc5214245a714528a5930d0a7ad8c3f6fae36f7bc6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38e08aa45f80f37ce92fd96da9dda5b05905acd302a805720e456e72f0fed8a4`

```dockerfile
```

-	Layers:
	-	`sha256:6cff905352150aa1a659e355bd68f6a89159ac65bf02aa39948be691c433d599`  
		Last Modified: Thu, 11 Sep 2025 18:49:29 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.6.11.18-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:26cc159ddc450657a3e087b554eec9ff4b939d0be8e3570a52254bbb44cf6f3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.3 MB (198250239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9cfe31b94df0c045639c24ad8a4422b00a50b2246b53ceb9ed62843dd3ec95f`
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
# Thu, 11 Sep 2025 16:06:16 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 11 Sep 2025 16:06:16 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
ARG REPO_CHANNEL=stable
# Thu, 11 Sep 2025 16:06:16 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 11 Sep 2025 16:06:16 GMT
ARG VERSION=25.6.11.18
# Thu, 11 Sep 2025 16:06:16 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.11.18 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.11.18 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.11.18 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
ENV LANG=en_US.UTF-8
# Thu, 11 Sep 2025 16:06:16 GMT
ENV TZ=UTC
# Thu, 11 Sep 2025 16:06:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.11.18 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Sep 2025 16:06:16 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 11 Sep 2025 16:06:16 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 11 Sep 2025 16:06:16 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 11 Sep 2025 16:06:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b6fc097e987cf080907725bee128816b79b5a91a6b2b279d16330178a1eedd`  
		Last Modified: Thu, 11 Sep 2025 17:08:11 GMT  
		Size: 7.1 MB (7127935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05eb04471900ac0874de5cf8a175405ec0109764d939baa04063af0fa42f8251`  
		Last Modified: Thu, 11 Sep 2025 17:08:22 GMT  
		Size: 162.9 MB (162890812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64dfbefe8c2cd54ac5c0df1827a4d9d668cb0298b7b62cb7caed215b61afb0c7`  
		Last Modified: Thu, 11 Sep 2025 17:08:11 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93843183b381cae40511d60d204acacc5850a76191e293f7379e8a456a7d97e8`  
		Last Modified: Thu, 11 Sep 2025 17:08:13 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb23dc55bbdc2e9458c319211cc31031df4b80e7c1f47531f406662e71099b9b`  
		Last Modified: Thu, 11 Sep 2025 17:08:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0121aabd0230a749e00c9642b021ab472b5dd9f8531909ca17cfcf8d01a0b7`  
		Last Modified: Thu, 11 Sep 2025 17:08:12 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07bfe3aa67e0578f9cd348b39e4eaf4e69b4e49879f09d0fdfdf34ec53056d9c`  
		Last Modified: Thu, 11 Sep 2025 17:08:12 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.11.18-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:7e5d5e22499af31003d7d87e027fb3ca40f689eaee1c9c6dc46075417f47dc9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09447d8d4bfa07595b1bb6d3fed04fdb7853099cdcf3536045dd835b2aada0f1`

```dockerfile
```

-	Layers:
	-	`sha256:3d5cb526dec856b5f18234d5b0f47ce3c251078414ef0d87a0ba472e26b16f62`  
		Last Modified: Thu, 11 Sep 2025 18:49:32 GMT  
		Size: 25.5 KB (25465 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.7`

```console
$ docker pull clickhouse@sha256:12551fca18bdf55c41573b436544973fd2e0d60309785755b71ca91839287d2f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.7` - linux; amd64

```console
$ docker pull clickhouse@sha256:0752ca83e0b3927b5f06b7b3b8a64ad6a5d9ccdc0c4e6f96770673cf83fea4e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.8 MB (221796998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e162390f7fd5af13d6a33fc69d01a5427c8130f91dbd36c3b881c8df185cc0c9`
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
# Thu, 04 Sep 2025 16:06:14 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 04 Sep 2025 16:06:14 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPO_CHANNEL=stable
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 04 Sep 2025 16:06:14 GMT
ARG VERSION=25.7.6.21
# Thu, 04 Sep 2025 16:06:14 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.6.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.6.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.6.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ENV LANG=en_US.UTF-8
# Thu, 04 Sep 2025 16:06:14 GMT
ENV TZ=UTC
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.6.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 04 Sep 2025 16:06:14 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 04 Sep 2025 16:06:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 04 Sep 2025 16:06:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d752dc6ed017f8a4bb8fc51a041aca7d5cd301611e489f4089d61379b94c20b`  
		Last Modified: Thu, 04 Sep 2025 17:26:45 GMT  
		Size: 7.6 MB (7598401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd98d78b4780afa930349b33780a56d5a5f7eee353e01f49e8f25b65fee968c`  
		Last Modified: Thu, 04 Sep 2025 18:50:02 GMT  
		Size: 183.8 MB (183791638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75707ca058257ce00db4c480da77c89f9781007c10cdd3d6ef1dd73e3f0e27e0`  
		Last Modified: Thu, 04 Sep 2025 17:26:45 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce56de849374b01d936eb85221cea81094f25d1adcb15faa7dc95c0f249ee85`  
		Last Modified: Thu, 04 Sep 2025 17:26:45 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81bd442da0d627487ad7428cf72526736bb5dacc3f91f2129ecdd84609e06b8d`  
		Last Modified: Thu, 04 Sep 2025 17:26:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51683e7c1d1b02514b5505121423b718454c63321b46395ff3f6af2acff34fa0`  
		Last Modified: Thu, 04 Sep 2025 17:26:45 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9903689e54dd6be962b6bd1d722a3a56a6857f0be66c8fa2a5a1e5bad2ee1e`  
		Last Modified: Thu, 04 Sep 2025 17:26:45 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d270bf37d427a10ca4878620861020b86ff261a623a09706aeb93a3002a4c9b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d22cd1af9445d319fe7009543c5508cec527553a4f25aba906a6ef4c764121`

```dockerfile
```

-	Layers:
	-	`sha256:417cfc00dc992bb38d39854d4488c82c221e99eabfaa4dc881be36de08ceece8`  
		Last Modified: Thu, 04 Sep 2025 18:49:40 GMT  
		Size: 25.5 KB (25461 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.7` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:8f5141ddfbcddd9b2b18d976e22911cd6997c9f7540225091477d4a8918a1b1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207733746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d3c3be91ad6c4bf8e676d26282156a94c94eb202d8de4c907eeeb87dbdf76f3`
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
# Thu, 04 Sep 2025 16:06:14 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 04 Sep 2025 16:06:14 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPO_CHANNEL=stable
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 04 Sep 2025 16:06:14 GMT
ARG VERSION=25.7.6.21
# Thu, 04 Sep 2025 16:06:14 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.6.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.6.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.6.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ENV LANG=en_US.UTF-8
# Thu, 04 Sep 2025 16:06:14 GMT
ENV TZ=UTC
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.6.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 04 Sep 2025 16:06:14 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 04 Sep 2025 16:06:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 04 Sep 2025 16:06:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4964c07b6117590bc4d7e7628fe632efb50202bcaf314ab922822d753cd5576e`  
		Last Modified: Thu, 04 Sep 2025 18:49:52 GMT  
		Size: 7.6 MB (7577345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebfd06d77ed6429c8ce0d9965dab8d09142ef78e1021d233e660afe2dbb42eb`  
		Last Modified: Thu, 04 Sep 2025 18:50:07 GMT  
		Size: 171.9 MB (171924908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c813c1438de87ce7c0473b5ed3398708c17daf620b35c411a463b956bbb87d3`  
		Last Modified: Thu, 04 Sep 2025 17:34:48 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecb3c78d4709777c3b190d0a877d0d4b9e9a8aea07c8500ac936a050df34a27`  
		Last Modified: Thu, 04 Sep 2025 17:34:51 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533d652372090cab3995f4bf8477026501a1d48ee7fd06fc62de15cae7257308`  
		Last Modified: Thu, 04 Sep 2025 17:34:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03764a811a2428d883597cbd8587aac4c833bc3268273289502dcdeb3cddbfc7`  
		Last Modified: Thu, 04 Sep 2025 17:34:58 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a75478794a90302bd11523ab11582c1038afb89d5dc97d119c2089fdf3cd4bd`  
		Last Modified: Thu, 04 Sep 2025 17:35:01 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ab29857128a7d703c7f4c7b9282d2ffdf22004a21c37ab2bb1e0570f61fa8e5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6644179fc1a3b92f7b8a3d7c97f6009776724f2e406f754a1c924887370c586f`

```dockerfile
```

-	Layers:
	-	`sha256:e84186197c316a091f45076a876f3b4427389bb214f1aeb5c5afc4eee0044247`  
		Last Modified: Thu, 04 Sep 2025 18:49:43 GMT  
		Size: 25.6 KB (25649 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.7-jammy`

```console
$ docker pull clickhouse@sha256:12551fca18bdf55c41573b436544973fd2e0d60309785755b71ca91839287d2f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.7-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:0752ca83e0b3927b5f06b7b3b8a64ad6a5d9ccdc0c4e6f96770673cf83fea4e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.8 MB (221796998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e162390f7fd5af13d6a33fc69d01a5427c8130f91dbd36c3b881c8df185cc0c9`
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
# Thu, 04 Sep 2025 16:06:14 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 04 Sep 2025 16:06:14 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPO_CHANNEL=stable
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 04 Sep 2025 16:06:14 GMT
ARG VERSION=25.7.6.21
# Thu, 04 Sep 2025 16:06:14 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.6.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.6.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.6.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ENV LANG=en_US.UTF-8
# Thu, 04 Sep 2025 16:06:14 GMT
ENV TZ=UTC
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.6.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 04 Sep 2025 16:06:14 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 04 Sep 2025 16:06:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 04 Sep 2025 16:06:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d752dc6ed017f8a4bb8fc51a041aca7d5cd301611e489f4089d61379b94c20b`  
		Last Modified: Thu, 04 Sep 2025 17:26:45 GMT  
		Size: 7.6 MB (7598401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd98d78b4780afa930349b33780a56d5a5f7eee353e01f49e8f25b65fee968c`  
		Last Modified: Thu, 04 Sep 2025 18:50:02 GMT  
		Size: 183.8 MB (183791638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75707ca058257ce00db4c480da77c89f9781007c10cdd3d6ef1dd73e3f0e27e0`  
		Last Modified: Thu, 04 Sep 2025 17:26:45 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce56de849374b01d936eb85221cea81094f25d1adcb15faa7dc95c0f249ee85`  
		Last Modified: Thu, 04 Sep 2025 17:26:45 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81bd442da0d627487ad7428cf72526736bb5dacc3f91f2129ecdd84609e06b8d`  
		Last Modified: Thu, 04 Sep 2025 17:26:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51683e7c1d1b02514b5505121423b718454c63321b46395ff3f6af2acff34fa0`  
		Last Modified: Thu, 04 Sep 2025 17:26:45 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9903689e54dd6be962b6bd1d722a3a56a6857f0be66c8fa2a5a1e5bad2ee1e`  
		Last Modified: Thu, 04 Sep 2025 17:26:45 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d270bf37d427a10ca4878620861020b86ff261a623a09706aeb93a3002a4c9b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d22cd1af9445d319fe7009543c5508cec527553a4f25aba906a6ef4c764121`

```dockerfile
```

-	Layers:
	-	`sha256:417cfc00dc992bb38d39854d4488c82c221e99eabfaa4dc881be36de08ceece8`  
		Last Modified: Thu, 04 Sep 2025 18:49:40 GMT  
		Size: 25.5 KB (25461 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.7-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:8f5141ddfbcddd9b2b18d976e22911cd6997c9f7540225091477d4a8918a1b1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207733746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d3c3be91ad6c4bf8e676d26282156a94c94eb202d8de4c907eeeb87dbdf76f3`
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
# Thu, 04 Sep 2025 16:06:14 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 04 Sep 2025 16:06:14 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPO_CHANNEL=stable
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 04 Sep 2025 16:06:14 GMT
ARG VERSION=25.7.6.21
# Thu, 04 Sep 2025 16:06:14 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.6.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.6.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.6.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ENV LANG=en_US.UTF-8
# Thu, 04 Sep 2025 16:06:14 GMT
ENV TZ=UTC
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.6.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 04 Sep 2025 16:06:14 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 04 Sep 2025 16:06:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 04 Sep 2025 16:06:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4964c07b6117590bc4d7e7628fe632efb50202bcaf314ab922822d753cd5576e`  
		Last Modified: Thu, 04 Sep 2025 18:49:52 GMT  
		Size: 7.6 MB (7577345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebfd06d77ed6429c8ce0d9965dab8d09142ef78e1021d233e660afe2dbb42eb`  
		Last Modified: Thu, 04 Sep 2025 18:50:07 GMT  
		Size: 171.9 MB (171924908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c813c1438de87ce7c0473b5ed3398708c17daf620b35c411a463b956bbb87d3`  
		Last Modified: Thu, 04 Sep 2025 17:34:48 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecb3c78d4709777c3b190d0a877d0d4b9e9a8aea07c8500ac936a050df34a27`  
		Last Modified: Thu, 04 Sep 2025 17:34:51 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533d652372090cab3995f4bf8477026501a1d48ee7fd06fc62de15cae7257308`  
		Last Modified: Thu, 04 Sep 2025 17:34:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03764a811a2428d883597cbd8587aac4c833bc3268273289502dcdeb3cddbfc7`  
		Last Modified: Thu, 04 Sep 2025 17:34:58 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a75478794a90302bd11523ab11582c1038afb89d5dc97d119c2089fdf3cd4bd`  
		Last Modified: Thu, 04 Sep 2025 17:35:01 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ab29857128a7d703c7f4c7b9282d2ffdf22004a21c37ab2bb1e0570f61fa8e5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6644179fc1a3b92f7b8a3d7c97f6009776724f2e406f754a1c924887370c586f`

```dockerfile
```

-	Layers:
	-	`sha256:e84186197c316a091f45076a876f3b4427389bb214f1aeb5c5afc4eee0044247`  
		Last Modified: Thu, 04 Sep 2025 18:49:43 GMT  
		Size: 25.6 KB (25649 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.7.6`

```console
$ docker pull clickhouse@sha256:12551fca18bdf55c41573b436544973fd2e0d60309785755b71ca91839287d2f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.7.6` - linux; amd64

```console
$ docker pull clickhouse@sha256:0752ca83e0b3927b5f06b7b3b8a64ad6a5d9ccdc0c4e6f96770673cf83fea4e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.8 MB (221796998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e162390f7fd5af13d6a33fc69d01a5427c8130f91dbd36c3b881c8df185cc0c9`
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
# Thu, 04 Sep 2025 16:06:14 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 04 Sep 2025 16:06:14 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPO_CHANNEL=stable
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 04 Sep 2025 16:06:14 GMT
ARG VERSION=25.7.6.21
# Thu, 04 Sep 2025 16:06:14 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.6.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.6.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.6.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ENV LANG=en_US.UTF-8
# Thu, 04 Sep 2025 16:06:14 GMT
ENV TZ=UTC
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.6.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 04 Sep 2025 16:06:14 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 04 Sep 2025 16:06:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 04 Sep 2025 16:06:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d752dc6ed017f8a4bb8fc51a041aca7d5cd301611e489f4089d61379b94c20b`  
		Last Modified: Thu, 04 Sep 2025 17:26:45 GMT  
		Size: 7.6 MB (7598401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd98d78b4780afa930349b33780a56d5a5f7eee353e01f49e8f25b65fee968c`  
		Last Modified: Thu, 04 Sep 2025 18:50:02 GMT  
		Size: 183.8 MB (183791638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75707ca058257ce00db4c480da77c89f9781007c10cdd3d6ef1dd73e3f0e27e0`  
		Last Modified: Thu, 04 Sep 2025 17:26:45 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce56de849374b01d936eb85221cea81094f25d1adcb15faa7dc95c0f249ee85`  
		Last Modified: Thu, 04 Sep 2025 17:26:45 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81bd442da0d627487ad7428cf72526736bb5dacc3f91f2129ecdd84609e06b8d`  
		Last Modified: Thu, 04 Sep 2025 17:26:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51683e7c1d1b02514b5505121423b718454c63321b46395ff3f6af2acff34fa0`  
		Last Modified: Thu, 04 Sep 2025 17:26:45 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9903689e54dd6be962b6bd1d722a3a56a6857f0be66c8fa2a5a1e5bad2ee1e`  
		Last Modified: Thu, 04 Sep 2025 17:26:45 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.6` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d270bf37d427a10ca4878620861020b86ff261a623a09706aeb93a3002a4c9b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d22cd1af9445d319fe7009543c5508cec527553a4f25aba906a6ef4c764121`

```dockerfile
```

-	Layers:
	-	`sha256:417cfc00dc992bb38d39854d4488c82c221e99eabfaa4dc881be36de08ceece8`  
		Last Modified: Thu, 04 Sep 2025 18:49:40 GMT  
		Size: 25.5 KB (25461 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.7.6` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:8f5141ddfbcddd9b2b18d976e22911cd6997c9f7540225091477d4a8918a1b1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207733746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d3c3be91ad6c4bf8e676d26282156a94c94eb202d8de4c907eeeb87dbdf76f3`
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
# Thu, 04 Sep 2025 16:06:14 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 04 Sep 2025 16:06:14 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPO_CHANNEL=stable
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 04 Sep 2025 16:06:14 GMT
ARG VERSION=25.7.6.21
# Thu, 04 Sep 2025 16:06:14 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.6.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.6.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.6.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ENV LANG=en_US.UTF-8
# Thu, 04 Sep 2025 16:06:14 GMT
ENV TZ=UTC
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.6.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 04 Sep 2025 16:06:14 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 04 Sep 2025 16:06:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 04 Sep 2025 16:06:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4964c07b6117590bc4d7e7628fe632efb50202bcaf314ab922822d753cd5576e`  
		Last Modified: Thu, 04 Sep 2025 18:49:52 GMT  
		Size: 7.6 MB (7577345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebfd06d77ed6429c8ce0d9965dab8d09142ef78e1021d233e660afe2dbb42eb`  
		Last Modified: Thu, 04 Sep 2025 18:50:07 GMT  
		Size: 171.9 MB (171924908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c813c1438de87ce7c0473b5ed3398708c17daf620b35c411a463b956bbb87d3`  
		Last Modified: Thu, 04 Sep 2025 17:34:48 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecb3c78d4709777c3b190d0a877d0d4b9e9a8aea07c8500ac936a050df34a27`  
		Last Modified: Thu, 04 Sep 2025 17:34:51 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533d652372090cab3995f4bf8477026501a1d48ee7fd06fc62de15cae7257308`  
		Last Modified: Thu, 04 Sep 2025 17:34:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03764a811a2428d883597cbd8587aac4c833bc3268273289502dcdeb3cddbfc7`  
		Last Modified: Thu, 04 Sep 2025 17:34:58 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a75478794a90302bd11523ab11582c1038afb89d5dc97d119c2089fdf3cd4bd`  
		Last Modified: Thu, 04 Sep 2025 17:35:01 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.6` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ab29857128a7d703c7f4c7b9282d2ffdf22004a21c37ab2bb1e0570f61fa8e5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6644179fc1a3b92f7b8a3d7c97f6009776724f2e406f754a1c924887370c586f`

```dockerfile
```

-	Layers:
	-	`sha256:e84186197c316a091f45076a876f3b4427389bb214f1aeb5c5afc4eee0044247`  
		Last Modified: Thu, 04 Sep 2025 18:49:43 GMT  
		Size: 25.6 KB (25649 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.7.6-jammy`

```console
$ docker pull clickhouse@sha256:12551fca18bdf55c41573b436544973fd2e0d60309785755b71ca91839287d2f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.7.6-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:0752ca83e0b3927b5f06b7b3b8a64ad6a5d9ccdc0c4e6f96770673cf83fea4e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.8 MB (221796998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e162390f7fd5af13d6a33fc69d01a5427c8130f91dbd36c3b881c8df185cc0c9`
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
# Thu, 04 Sep 2025 16:06:14 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 04 Sep 2025 16:06:14 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPO_CHANNEL=stable
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 04 Sep 2025 16:06:14 GMT
ARG VERSION=25.7.6.21
# Thu, 04 Sep 2025 16:06:14 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.6.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.6.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.6.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ENV LANG=en_US.UTF-8
# Thu, 04 Sep 2025 16:06:14 GMT
ENV TZ=UTC
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.6.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 04 Sep 2025 16:06:14 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 04 Sep 2025 16:06:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 04 Sep 2025 16:06:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d752dc6ed017f8a4bb8fc51a041aca7d5cd301611e489f4089d61379b94c20b`  
		Last Modified: Thu, 04 Sep 2025 17:26:45 GMT  
		Size: 7.6 MB (7598401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd98d78b4780afa930349b33780a56d5a5f7eee353e01f49e8f25b65fee968c`  
		Last Modified: Thu, 04 Sep 2025 18:50:02 GMT  
		Size: 183.8 MB (183791638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75707ca058257ce00db4c480da77c89f9781007c10cdd3d6ef1dd73e3f0e27e0`  
		Last Modified: Thu, 04 Sep 2025 17:26:45 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce56de849374b01d936eb85221cea81094f25d1adcb15faa7dc95c0f249ee85`  
		Last Modified: Thu, 04 Sep 2025 17:26:45 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81bd442da0d627487ad7428cf72526736bb5dacc3f91f2129ecdd84609e06b8d`  
		Last Modified: Thu, 04 Sep 2025 17:26:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51683e7c1d1b02514b5505121423b718454c63321b46395ff3f6af2acff34fa0`  
		Last Modified: Thu, 04 Sep 2025 17:26:45 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9903689e54dd6be962b6bd1d722a3a56a6857f0be66c8fa2a5a1e5bad2ee1e`  
		Last Modified: Thu, 04 Sep 2025 17:26:45 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.6-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d270bf37d427a10ca4878620861020b86ff261a623a09706aeb93a3002a4c9b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d22cd1af9445d319fe7009543c5508cec527553a4f25aba906a6ef4c764121`

```dockerfile
```

-	Layers:
	-	`sha256:417cfc00dc992bb38d39854d4488c82c221e99eabfaa4dc881be36de08ceece8`  
		Last Modified: Thu, 04 Sep 2025 18:49:40 GMT  
		Size: 25.5 KB (25461 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.7.6-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:8f5141ddfbcddd9b2b18d976e22911cd6997c9f7540225091477d4a8918a1b1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207733746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d3c3be91ad6c4bf8e676d26282156a94c94eb202d8de4c907eeeb87dbdf76f3`
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
# Thu, 04 Sep 2025 16:06:14 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 04 Sep 2025 16:06:14 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPO_CHANNEL=stable
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 04 Sep 2025 16:06:14 GMT
ARG VERSION=25.7.6.21
# Thu, 04 Sep 2025 16:06:14 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.6.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.6.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.6.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ENV LANG=en_US.UTF-8
# Thu, 04 Sep 2025 16:06:14 GMT
ENV TZ=UTC
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.6.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 04 Sep 2025 16:06:14 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 04 Sep 2025 16:06:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 04 Sep 2025 16:06:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4964c07b6117590bc4d7e7628fe632efb50202bcaf314ab922822d753cd5576e`  
		Last Modified: Thu, 04 Sep 2025 18:49:52 GMT  
		Size: 7.6 MB (7577345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebfd06d77ed6429c8ce0d9965dab8d09142ef78e1021d233e660afe2dbb42eb`  
		Last Modified: Thu, 04 Sep 2025 18:50:07 GMT  
		Size: 171.9 MB (171924908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c813c1438de87ce7c0473b5ed3398708c17daf620b35c411a463b956bbb87d3`  
		Last Modified: Thu, 04 Sep 2025 17:34:48 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecb3c78d4709777c3b190d0a877d0d4b9e9a8aea07c8500ac936a050df34a27`  
		Last Modified: Thu, 04 Sep 2025 17:34:51 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533d652372090cab3995f4bf8477026501a1d48ee7fd06fc62de15cae7257308`  
		Last Modified: Thu, 04 Sep 2025 17:34:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03764a811a2428d883597cbd8587aac4c833bc3268273289502dcdeb3cddbfc7`  
		Last Modified: Thu, 04 Sep 2025 17:34:58 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a75478794a90302bd11523ab11582c1038afb89d5dc97d119c2089fdf3cd4bd`  
		Last Modified: Thu, 04 Sep 2025 17:35:01 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.6-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ab29857128a7d703c7f4c7b9282d2ffdf22004a21c37ab2bb1e0570f61fa8e5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6644179fc1a3b92f7b8a3d7c97f6009776724f2e406f754a1c924887370c586f`

```dockerfile
```

-	Layers:
	-	`sha256:e84186197c316a091f45076a876f3b4427389bb214f1aeb5c5afc4eee0044247`  
		Last Modified: Thu, 04 Sep 2025 18:49:43 GMT  
		Size: 25.6 KB (25649 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.7.6.21`

```console
$ docker pull clickhouse@sha256:12551fca18bdf55c41573b436544973fd2e0d60309785755b71ca91839287d2f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.7.6.21` - linux; amd64

```console
$ docker pull clickhouse@sha256:0752ca83e0b3927b5f06b7b3b8a64ad6a5d9ccdc0c4e6f96770673cf83fea4e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.8 MB (221796998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e162390f7fd5af13d6a33fc69d01a5427c8130f91dbd36c3b881c8df185cc0c9`
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
# Thu, 04 Sep 2025 16:06:14 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 04 Sep 2025 16:06:14 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPO_CHANNEL=stable
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 04 Sep 2025 16:06:14 GMT
ARG VERSION=25.7.6.21
# Thu, 04 Sep 2025 16:06:14 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.6.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.6.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.6.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ENV LANG=en_US.UTF-8
# Thu, 04 Sep 2025 16:06:14 GMT
ENV TZ=UTC
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.6.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 04 Sep 2025 16:06:14 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 04 Sep 2025 16:06:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 04 Sep 2025 16:06:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d752dc6ed017f8a4bb8fc51a041aca7d5cd301611e489f4089d61379b94c20b`  
		Last Modified: Thu, 04 Sep 2025 17:26:45 GMT  
		Size: 7.6 MB (7598401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd98d78b4780afa930349b33780a56d5a5f7eee353e01f49e8f25b65fee968c`  
		Last Modified: Thu, 04 Sep 2025 18:50:02 GMT  
		Size: 183.8 MB (183791638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75707ca058257ce00db4c480da77c89f9781007c10cdd3d6ef1dd73e3f0e27e0`  
		Last Modified: Thu, 04 Sep 2025 17:26:45 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce56de849374b01d936eb85221cea81094f25d1adcb15faa7dc95c0f249ee85`  
		Last Modified: Thu, 04 Sep 2025 17:26:45 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81bd442da0d627487ad7428cf72526736bb5dacc3f91f2129ecdd84609e06b8d`  
		Last Modified: Thu, 04 Sep 2025 17:26:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51683e7c1d1b02514b5505121423b718454c63321b46395ff3f6af2acff34fa0`  
		Last Modified: Thu, 04 Sep 2025 17:26:45 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9903689e54dd6be962b6bd1d722a3a56a6857f0be66c8fa2a5a1e5bad2ee1e`  
		Last Modified: Thu, 04 Sep 2025 17:26:45 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.6.21` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d270bf37d427a10ca4878620861020b86ff261a623a09706aeb93a3002a4c9b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d22cd1af9445d319fe7009543c5508cec527553a4f25aba906a6ef4c764121`

```dockerfile
```

-	Layers:
	-	`sha256:417cfc00dc992bb38d39854d4488c82c221e99eabfaa4dc881be36de08ceece8`  
		Last Modified: Thu, 04 Sep 2025 18:49:40 GMT  
		Size: 25.5 KB (25461 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.7.6.21` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:8f5141ddfbcddd9b2b18d976e22911cd6997c9f7540225091477d4a8918a1b1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207733746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d3c3be91ad6c4bf8e676d26282156a94c94eb202d8de4c907eeeb87dbdf76f3`
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
# Thu, 04 Sep 2025 16:06:14 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 04 Sep 2025 16:06:14 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPO_CHANNEL=stable
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 04 Sep 2025 16:06:14 GMT
ARG VERSION=25.7.6.21
# Thu, 04 Sep 2025 16:06:14 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.6.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.6.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.6.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ENV LANG=en_US.UTF-8
# Thu, 04 Sep 2025 16:06:14 GMT
ENV TZ=UTC
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.6.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 04 Sep 2025 16:06:14 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 04 Sep 2025 16:06:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 04 Sep 2025 16:06:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4964c07b6117590bc4d7e7628fe632efb50202bcaf314ab922822d753cd5576e`  
		Last Modified: Thu, 04 Sep 2025 18:49:52 GMT  
		Size: 7.6 MB (7577345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebfd06d77ed6429c8ce0d9965dab8d09142ef78e1021d233e660afe2dbb42eb`  
		Last Modified: Thu, 04 Sep 2025 18:50:07 GMT  
		Size: 171.9 MB (171924908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c813c1438de87ce7c0473b5ed3398708c17daf620b35c411a463b956bbb87d3`  
		Last Modified: Thu, 04 Sep 2025 17:34:48 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecb3c78d4709777c3b190d0a877d0d4b9e9a8aea07c8500ac936a050df34a27`  
		Last Modified: Thu, 04 Sep 2025 17:34:51 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533d652372090cab3995f4bf8477026501a1d48ee7fd06fc62de15cae7257308`  
		Last Modified: Thu, 04 Sep 2025 17:34:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03764a811a2428d883597cbd8587aac4c833bc3268273289502dcdeb3cddbfc7`  
		Last Modified: Thu, 04 Sep 2025 17:34:58 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a75478794a90302bd11523ab11582c1038afb89d5dc97d119c2089fdf3cd4bd`  
		Last Modified: Thu, 04 Sep 2025 17:35:01 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.6.21` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ab29857128a7d703c7f4c7b9282d2ffdf22004a21c37ab2bb1e0570f61fa8e5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6644179fc1a3b92f7b8a3d7c97f6009776724f2e406f754a1c924887370c586f`

```dockerfile
```

-	Layers:
	-	`sha256:e84186197c316a091f45076a876f3b4427389bb214f1aeb5c5afc4eee0044247`  
		Last Modified: Thu, 04 Sep 2025 18:49:43 GMT  
		Size: 25.6 KB (25649 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.7.6.21-jammy`

```console
$ docker pull clickhouse@sha256:12551fca18bdf55c41573b436544973fd2e0d60309785755b71ca91839287d2f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.7.6.21-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:0752ca83e0b3927b5f06b7b3b8a64ad6a5d9ccdc0c4e6f96770673cf83fea4e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.8 MB (221796998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e162390f7fd5af13d6a33fc69d01a5427c8130f91dbd36c3b881c8df185cc0c9`
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
# Thu, 04 Sep 2025 16:06:14 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 04 Sep 2025 16:06:14 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPO_CHANNEL=stable
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 04 Sep 2025 16:06:14 GMT
ARG VERSION=25.7.6.21
# Thu, 04 Sep 2025 16:06:14 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.6.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.6.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.6.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ENV LANG=en_US.UTF-8
# Thu, 04 Sep 2025 16:06:14 GMT
ENV TZ=UTC
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.6.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 04 Sep 2025 16:06:14 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 04 Sep 2025 16:06:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 04 Sep 2025 16:06:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d752dc6ed017f8a4bb8fc51a041aca7d5cd301611e489f4089d61379b94c20b`  
		Last Modified: Thu, 04 Sep 2025 17:26:45 GMT  
		Size: 7.6 MB (7598401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd98d78b4780afa930349b33780a56d5a5f7eee353e01f49e8f25b65fee968c`  
		Last Modified: Thu, 04 Sep 2025 18:50:02 GMT  
		Size: 183.8 MB (183791638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75707ca058257ce00db4c480da77c89f9781007c10cdd3d6ef1dd73e3f0e27e0`  
		Last Modified: Thu, 04 Sep 2025 17:26:45 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce56de849374b01d936eb85221cea81094f25d1adcb15faa7dc95c0f249ee85`  
		Last Modified: Thu, 04 Sep 2025 17:26:45 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81bd442da0d627487ad7428cf72526736bb5dacc3f91f2129ecdd84609e06b8d`  
		Last Modified: Thu, 04 Sep 2025 17:26:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51683e7c1d1b02514b5505121423b718454c63321b46395ff3f6af2acff34fa0`  
		Last Modified: Thu, 04 Sep 2025 17:26:45 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9903689e54dd6be962b6bd1d722a3a56a6857f0be66c8fa2a5a1e5bad2ee1e`  
		Last Modified: Thu, 04 Sep 2025 17:26:45 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.6.21-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d270bf37d427a10ca4878620861020b86ff261a623a09706aeb93a3002a4c9b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d22cd1af9445d319fe7009543c5508cec527553a4f25aba906a6ef4c764121`

```dockerfile
```

-	Layers:
	-	`sha256:417cfc00dc992bb38d39854d4488c82c221e99eabfaa4dc881be36de08ceece8`  
		Last Modified: Thu, 04 Sep 2025 18:49:40 GMT  
		Size: 25.5 KB (25461 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.7.6.21-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:8f5141ddfbcddd9b2b18d976e22911cd6997c9f7540225091477d4a8918a1b1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207733746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d3c3be91ad6c4bf8e676d26282156a94c94eb202d8de4c907eeeb87dbdf76f3`
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
# Thu, 04 Sep 2025 16:06:14 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 04 Sep 2025 16:06:14 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPO_CHANNEL=stable
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 04 Sep 2025 16:06:14 GMT
ARG VERSION=25.7.6.21
# Thu, 04 Sep 2025 16:06:14 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.6.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.6.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.6.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ENV LANG=en_US.UTF-8
# Thu, 04 Sep 2025 16:06:14 GMT
ENV TZ=UTC
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.6.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 04 Sep 2025 16:06:14 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 04 Sep 2025 16:06:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 04 Sep 2025 16:06:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4964c07b6117590bc4d7e7628fe632efb50202bcaf314ab922822d753cd5576e`  
		Last Modified: Thu, 04 Sep 2025 18:49:52 GMT  
		Size: 7.6 MB (7577345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebfd06d77ed6429c8ce0d9965dab8d09142ef78e1021d233e660afe2dbb42eb`  
		Last Modified: Thu, 04 Sep 2025 18:50:07 GMT  
		Size: 171.9 MB (171924908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c813c1438de87ce7c0473b5ed3398708c17daf620b35c411a463b956bbb87d3`  
		Last Modified: Thu, 04 Sep 2025 17:34:48 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecb3c78d4709777c3b190d0a877d0d4b9e9a8aea07c8500ac936a050df34a27`  
		Last Modified: Thu, 04 Sep 2025 17:34:51 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533d652372090cab3995f4bf8477026501a1d48ee7fd06fc62de15cae7257308`  
		Last Modified: Thu, 04 Sep 2025 17:34:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03764a811a2428d883597cbd8587aac4c833bc3268273289502dcdeb3cddbfc7`  
		Last Modified: Thu, 04 Sep 2025 17:34:58 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a75478794a90302bd11523ab11582c1038afb89d5dc97d119c2089fdf3cd4bd`  
		Last Modified: Thu, 04 Sep 2025 17:35:01 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.6.21-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ab29857128a7d703c7f4c7b9282d2ffdf22004a21c37ab2bb1e0570f61fa8e5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6644179fc1a3b92f7b8a3d7c97f6009776724f2e406f754a1c924887370c586f`

```dockerfile
```

-	Layers:
	-	`sha256:e84186197c316a091f45076a876f3b4427389bb214f1aeb5c5afc4eee0044247`  
		Last Modified: Thu, 04 Sep 2025 18:49:43 GMT  
		Size: 25.6 KB (25649 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8`

```console
$ docker pull clickhouse@sha256:30e6b08a3371f0837a88ecc90568e9bc22e1316f75250f4c102cf2bcd28afa8e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8` - linux; amd64

```console
$ docker pull clickhouse@sha256:70374eab8db97e716c0c803b8e426526567a852ea46c4fbbaffa20aadb6bddda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.6 MB (227646811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2712c652b4c632d10c2b1e7525a9e55cb75a477d208a03d0d5f4a69e3b880170`
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
# Thu, 04 Sep 2025 16:06:14 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 04 Sep 2025 16:06:14 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPO_CHANNEL=stable
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 04 Sep 2025 16:06:14 GMT
ARG VERSION=25.8.2.29
# Thu, 04 Sep 2025 16:06:14 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ENV LANG=en_US.UTF-8
# Thu, 04 Sep 2025 16:06:14 GMT
ENV TZ=UTC
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 04 Sep 2025 16:06:14 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 04 Sep 2025 16:06:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 04 Sep 2025 16:06:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2674d38b8300b858879b0e7bc2f778d915ea4988dee3908123e8a5ae14c2185`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 7.6 MB (7598429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0716cebfee9c18bfbac80c646f5717ca53f7d6b70451c5a30ecf6539e91fac6`  
		Last Modified: Thu, 04 Sep 2025 18:31:08 GMT  
		Size: 189.6 MB (189641425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc9e8dce7ae686e1f14c0590e855c6cccba74ec64742505427ed9c077c0b3a0`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff903e1c3fca299ee3267558f234215acd3c6359130611bd3b914ce39fec2e94`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ca8d80efc007ad421b2edbebd579205d26e5b24dd9368b1a7fcbee2936d1c6`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450458a8fa14ce6ea48552cbac580e000b33f200bfe5d5f74dda19dc36b33d04`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb98d5afe64ab4f4c464946cf3e840f85923798e29c22c321e892d435a10e39f`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9d73c85ac5c80ce6e5ae0e4577c706687576573e83c738b24d63675c0d3bb7c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d975838095cb1936f50f2b0a3f7b35936b3c1d3750d873626de144db9f345ae`

```dockerfile
```

-	Layers:
	-	`sha256:05a206c5ac24002577f1380ef90af02fc64eef6eb74e89df0f0241de04709f67`  
		Last Modified: Thu, 04 Sep 2025 18:49:53 GMT  
		Size: 26.7 KB (26683 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:faf446bacfba09029ad4542899d4e96e43d67da7681bf3afae1ca56a732a5849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212396721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571824efb148de6116d9ad9d75469041a29601827f6aecdb256f4eb1829a0a6e`
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
# Thu, 04 Sep 2025 16:06:14 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 04 Sep 2025 16:06:14 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPO_CHANNEL=stable
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 04 Sep 2025 16:06:14 GMT
ARG VERSION=25.8.2.29
# Thu, 04 Sep 2025 16:06:14 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ENV LANG=en_US.UTF-8
# Thu, 04 Sep 2025 16:06:14 GMT
ENV TZ=UTC
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 04 Sep 2025 16:06:14 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 04 Sep 2025 16:06:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 04 Sep 2025 16:06:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5ec0191b4ea618855356e7f5642643723d508ce4a081599087506aacec3635`  
		Last Modified: Thu, 04 Sep 2025 18:31:02 GMT  
		Size: 7.6 MB (7577271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f0b5998b053fb76c44f29c05b0c890cfb16d3f6ac26332f4a077d04aec0b23`  
		Last Modified: Thu, 04 Sep 2025 18:31:25 GMT  
		Size: 176.6 MB (176587956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d1d145fe1a57c3893100205acdcb0271fb6878db7926ebf738da1e11098159`  
		Last Modified: Thu, 04 Sep 2025 18:08:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a0dffe6609b09c327f4d70e0e75f9c2472241217ceb9fa245b44fb1444744c`  
		Last Modified: Thu, 04 Sep 2025 18:08:13 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62bf014b26c1ca3ff8c228697c11b42ff86e6f550d5882953aee5780be4f56f3`  
		Last Modified: Thu, 04 Sep 2025 18:08:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beaa6239d0f79e1cc6dd43bd5cc8fb93810c186a1bcfa7a60f6d296b96d68a9c`  
		Last Modified: Thu, 04 Sep 2025 18:08:13 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b011b7349796e6a7547c09f02b5433ba94731e3f0b01e606efb62fe91d30095b`  
		Last Modified: Thu, 04 Sep 2025 18:08:12 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:398e24d59bf5b944d28318e7d7bf46be33dcae00865dcc851fd58ff95c419a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7860a7857bb8fb6e4b9b353fcf34d84322eb24d2c539304ea4496b7937932c4d`

```dockerfile
```

-	Layers:
	-	`sha256:f22151502df928d19d2a8d8f234da857a6d78c6de4b76b4ffc06ed4e76ff80c3`  
		Last Modified: Thu, 04 Sep 2025 18:49:57 GMT  
		Size: 26.9 KB (26919 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8-jammy`

```console
$ docker pull clickhouse@sha256:30e6b08a3371f0837a88ecc90568e9bc22e1316f75250f4c102cf2bcd28afa8e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:70374eab8db97e716c0c803b8e426526567a852ea46c4fbbaffa20aadb6bddda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.6 MB (227646811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2712c652b4c632d10c2b1e7525a9e55cb75a477d208a03d0d5f4a69e3b880170`
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
# Thu, 04 Sep 2025 16:06:14 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 04 Sep 2025 16:06:14 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPO_CHANNEL=stable
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 04 Sep 2025 16:06:14 GMT
ARG VERSION=25.8.2.29
# Thu, 04 Sep 2025 16:06:14 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ENV LANG=en_US.UTF-8
# Thu, 04 Sep 2025 16:06:14 GMT
ENV TZ=UTC
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 04 Sep 2025 16:06:14 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 04 Sep 2025 16:06:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 04 Sep 2025 16:06:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2674d38b8300b858879b0e7bc2f778d915ea4988dee3908123e8a5ae14c2185`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 7.6 MB (7598429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0716cebfee9c18bfbac80c646f5717ca53f7d6b70451c5a30ecf6539e91fac6`  
		Last Modified: Thu, 04 Sep 2025 18:31:08 GMT  
		Size: 189.6 MB (189641425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc9e8dce7ae686e1f14c0590e855c6cccba74ec64742505427ed9c077c0b3a0`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff903e1c3fca299ee3267558f234215acd3c6359130611bd3b914ce39fec2e94`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ca8d80efc007ad421b2edbebd579205d26e5b24dd9368b1a7fcbee2936d1c6`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450458a8fa14ce6ea48552cbac580e000b33f200bfe5d5f74dda19dc36b33d04`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb98d5afe64ab4f4c464946cf3e840f85923798e29c22c321e892d435a10e39f`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9d73c85ac5c80ce6e5ae0e4577c706687576573e83c738b24d63675c0d3bb7c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d975838095cb1936f50f2b0a3f7b35936b3c1d3750d873626de144db9f345ae`

```dockerfile
```

-	Layers:
	-	`sha256:05a206c5ac24002577f1380ef90af02fc64eef6eb74e89df0f0241de04709f67`  
		Last Modified: Thu, 04 Sep 2025 18:49:53 GMT  
		Size: 26.7 KB (26683 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:faf446bacfba09029ad4542899d4e96e43d67da7681bf3afae1ca56a732a5849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212396721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571824efb148de6116d9ad9d75469041a29601827f6aecdb256f4eb1829a0a6e`
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
# Thu, 04 Sep 2025 16:06:14 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 04 Sep 2025 16:06:14 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPO_CHANNEL=stable
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 04 Sep 2025 16:06:14 GMT
ARG VERSION=25.8.2.29
# Thu, 04 Sep 2025 16:06:14 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ENV LANG=en_US.UTF-8
# Thu, 04 Sep 2025 16:06:14 GMT
ENV TZ=UTC
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 04 Sep 2025 16:06:14 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 04 Sep 2025 16:06:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 04 Sep 2025 16:06:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5ec0191b4ea618855356e7f5642643723d508ce4a081599087506aacec3635`  
		Last Modified: Thu, 04 Sep 2025 18:31:02 GMT  
		Size: 7.6 MB (7577271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f0b5998b053fb76c44f29c05b0c890cfb16d3f6ac26332f4a077d04aec0b23`  
		Last Modified: Thu, 04 Sep 2025 18:31:25 GMT  
		Size: 176.6 MB (176587956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d1d145fe1a57c3893100205acdcb0271fb6878db7926ebf738da1e11098159`  
		Last Modified: Thu, 04 Sep 2025 18:08:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a0dffe6609b09c327f4d70e0e75f9c2472241217ceb9fa245b44fb1444744c`  
		Last Modified: Thu, 04 Sep 2025 18:08:13 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62bf014b26c1ca3ff8c228697c11b42ff86e6f550d5882953aee5780be4f56f3`  
		Last Modified: Thu, 04 Sep 2025 18:08:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beaa6239d0f79e1cc6dd43bd5cc8fb93810c186a1bcfa7a60f6d296b96d68a9c`  
		Last Modified: Thu, 04 Sep 2025 18:08:13 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b011b7349796e6a7547c09f02b5433ba94731e3f0b01e606efb62fe91d30095b`  
		Last Modified: Thu, 04 Sep 2025 18:08:12 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:398e24d59bf5b944d28318e7d7bf46be33dcae00865dcc851fd58ff95c419a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7860a7857bb8fb6e4b9b353fcf34d84322eb24d2c539304ea4496b7937932c4d`

```dockerfile
```

-	Layers:
	-	`sha256:f22151502df928d19d2a8d8f234da857a6d78c6de4b76b4ffc06ed4e76ff80c3`  
		Last Modified: Thu, 04 Sep 2025 18:49:57 GMT  
		Size: 26.9 KB (26919 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.2`

```console
$ docker pull clickhouse@sha256:30e6b08a3371f0837a88ecc90568e9bc22e1316f75250f4c102cf2bcd28afa8e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.2` - linux; amd64

```console
$ docker pull clickhouse@sha256:70374eab8db97e716c0c803b8e426526567a852ea46c4fbbaffa20aadb6bddda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.6 MB (227646811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2712c652b4c632d10c2b1e7525a9e55cb75a477d208a03d0d5f4a69e3b880170`
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
# Thu, 04 Sep 2025 16:06:14 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 04 Sep 2025 16:06:14 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPO_CHANNEL=stable
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 04 Sep 2025 16:06:14 GMT
ARG VERSION=25.8.2.29
# Thu, 04 Sep 2025 16:06:14 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ENV LANG=en_US.UTF-8
# Thu, 04 Sep 2025 16:06:14 GMT
ENV TZ=UTC
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 04 Sep 2025 16:06:14 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 04 Sep 2025 16:06:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 04 Sep 2025 16:06:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2674d38b8300b858879b0e7bc2f778d915ea4988dee3908123e8a5ae14c2185`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 7.6 MB (7598429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0716cebfee9c18bfbac80c646f5717ca53f7d6b70451c5a30ecf6539e91fac6`  
		Last Modified: Thu, 04 Sep 2025 18:31:08 GMT  
		Size: 189.6 MB (189641425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc9e8dce7ae686e1f14c0590e855c6cccba74ec64742505427ed9c077c0b3a0`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff903e1c3fca299ee3267558f234215acd3c6359130611bd3b914ce39fec2e94`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ca8d80efc007ad421b2edbebd579205d26e5b24dd9368b1a7fcbee2936d1c6`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450458a8fa14ce6ea48552cbac580e000b33f200bfe5d5f74dda19dc36b33d04`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb98d5afe64ab4f4c464946cf3e840f85923798e29c22c321e892d435a10e39f`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9d73c85ac5c80ce6e5ae0e4577c706687576573e83c738b24d63675c0d3bb7c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d975838095cb1936f50f2b0a3f7b35936b3c1d3750d873626de144db9f345ae`

```dockerfile
```

-	Layers:
	-	`sha256:05a206c5ac24002577f1380ef90af02fc64eef6eb74e89df0f0241de04709f67`  
		Last Modified: Thu, 04 Sep 2025 18:49:53 GMT  
		Size: 26.7 KB (26683 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.2` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:faf446bacfba09029ad4542899d4e96e43d67da7681bf3afae1ca56a732a5849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212396721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571824efb148de6116d9ad9d75469041a29601827f6aecdb256f4eb1829a0a6e`
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
# Thu, 04 Sep 2025 16:06:14 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 04 Sep 2025 16:06:14 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPO_CHANNEL=stable
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 04 Sep 2025 16:06:14 GMT
ARG VERSION=25.8.2.29
# Thu, 04 Sep 2025 16:06:14 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ENV LANG=en_US.UTF-8
# Thu, 04 Sep 2025 16:06:14 GMT
ENV TZ=UTC
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 04 Sep 2025 16:06:14 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 04 Sep 2025 16:06:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 04 Sep 2025 16:06:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5ec0191b4ea618855356e7f5642643723d508ce4a081599087506aacec3635`  
		Last Modified: Thu, 04 Sep 2025 18:31:02 GMT  
		Size: 7.6 MB (7577271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f0b5998b053fb76c44f29c05b0c890cfb16d3f6ac26332f4a077d04aec0b23`  
		Last Modified: Thu, 04 Sep 2025 18:31:25 GMT  
		Size: 176.6 MB (176587956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d1d145fe1a57c3893100205acdcb0271fb6878db7926ebf738da1e11098159`  
		Last Modified: Thu, 04 Sep 2025 18:08:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a0dffe6609b09c327f4d70e0e75f9c2472241217ceb9fa245b44fb1444744c`  
		Last Modified: Thu, 04 Sep 2025 18:08:13 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62bf014b26c1ca3ff8c228697c11b42ff86e6f550d5882953aee5780be4f56f3`  
		Last Modified: Thu, 04 Sep 2025 18:08:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beaa6239d0f79e1cc6dd43bd5cc8fb93810c186a1bcfa7a60f6d296b96d68a9c`  
		Last Modified: Thu, 04 Sep 2025 18:08:13 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b011b7349796e6a7547c09f02b5433ba94731e3f0b01e606efb62fe91d30095b`  
		Last Modified: Thu, 04 Sep 2025 18:08:12 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:398e24d59bf5b944d28318e7d7bf46be33dcae00865dcc851fd58ff95c419a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7860a7857bb8fb6e4b9b353fcf34d84322eb24d2c539304ea4496b7937932c4d`

```dockerfile
```

-	Layers:
	-	`sha256:f22151502df928d19d2a8d8f234da857a6d78c6de4b76b4ffc06ed4e76ff80c3`  
		Last Modified: Thu, 04 Sep 2025 18:49:57 GMT  
		Size: 26.9 KB (26919 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.2-jammy`

```console
$ docker pull clickhouse@sha256:30e6b08a3371f0837a88ecc90568e9bc22e1316f75250f4c102cf2bcd28afa8e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.2-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:70374eab8db97e716c0c803b8e426526567a852ea46c4fbbaffa20aadb6bddda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.6 MB (227646811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2712c652b4c632d10c2b1e7525a9e55cb75a477d208a03d0d5f4a69e3b880170`
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
# Thu, 04 Sep 2025 16:06:14 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 04 Sep 2025 16:06:14 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPO_CHANNEL=stable
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 04 Sep 2025 16:06:14 GMT
ARG VERSION=25.8.2.29
# Thu, 04 Sep 2025 16:06:14 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ENV LANG=en_US.UTF-8
# Thu, 04 Sep 2025 16:06:14 GMT
ENV TZ=UTC
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 04 Sep 2025 16:06:14 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 04 Sep 2025 16:06:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 04 Sep 2025 16:06:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2674d38b8300b858879b0e7bc2f778d915ea4988dee3908123e8a5ae14c2185`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 7.6 MB (7598429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0716cebfee9c18bfbac80c646f5717ca53f7d6b70451c5a30ecf6539e91fac6`  
		Last Modified: Thu, 04 Sep 2025 18:31:08 GMT  
		Size: 189.6 MB (189641425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc9e8dce7ae686e1f14c0590e855c6cccba74ec64742505427ed9c077c0b3a0`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff903e1c3fca299ee3267558f234215acd3c6359130611bd3b914ce39fec2e94`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ca8d80efc007ad421b2edbebd579205d26e5b24dd9368b1a7fcbee2936d1c6`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450458a8fa14ce6ea48552cbac580e000b33f200bfe5d5f74dda19dc36b33d04`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb98d5afe64ab4f4c464946cf3e840f85923798e29c22c321e892d435a10e39f`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9d73c85ac5c80ce6e5ae0e4577c706687576573e83c738b24d63675c0d3bb7c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d975838095cb1936f50f2b0a3f7b35936b3c1d3750d873626de144db9f345ae`

```dockerfile
```

-	Layers:
	-	`sha256:05a206c5ac24002577f1380ef90af02fc64eef6eb74e89df0f0241de04709f67`  
		Last Modified: Thu, 04 Sep 2025 18:49:53 GMT  
		Size: 26.7 KB (26683 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.2-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:faf446bacfba09029ad4542899d4e96e43d67da7681bf3afae1ca56a732a5849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212396721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571824efb148de6116d9ad9d75469041a29601827f6aecdb256f4eb1829a0a6e`
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
# Thu, 04 Sep 2025 16:06:14 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 04 Sep 2025 16:06:14 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPO_CHANNEL=stable
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 04 Sep 2025 16:06:14 GMT
ARG VERSION=25.8.2.29
# Thu, 04 Sep 2025 16:06:14 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ENV LANG=en_US.UTF-8
# Thu, 04 Sep 2025 16:06:14 GMT
ENV TZ=UTC
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 04 Sep 2025 16:06:14 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 04 Sep 2025 16:06:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 04 Sep 2025 16:06:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5ec0191b4ea618855356e7f5642643723d508ce4a081599087506aacec3635`  
		Last Modified: Thu, 04 Sep 2025 18:31:02 GMT  
		Size: 7.6 MB (7577271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f0b5998b053fb76c44f29c05b0c890cfb16d3f6ac26332f4a077d04aec0b23`  
		Last Modified: Thu, 04 Sep 2025 18:31:25 GMT  
		Size: 176.6 MB (176587956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d1d145fe1a57c3893100205acdcb0271fb6878db7926ebf738da1e11098159`  
		Last Modified: Thu, 04 Sep 2025 18:08:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a0dffe6609b09c327f4d70e0e75f9c2472241217ceb9fa245b44fb1444744c`  
		Last Modified: Thu, 04 Sep 2025 18:08:13 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62bf014b26c1ca3ff8c228697c11b42ff86e6f550d5882953aee5780be4f56f3`  
		Last Modified: Thu, 04 Sep 2025 18:08:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beaa6239d0f79e1cc6dd43bd5cc8fb93810c186a1bcfa7a60f6d296b96d68a9c`  
		Last Modified: Thu, 04 Sep 2025 18:08:13 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b011b7349796e6a7547c09f02b5433ba94731e3f0b01e606efb62fe91d30095b`  
		Last Modified: Thu, 04 Sep 2025 18:08:12 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:398e24d59bf5b944d28318e7d7bf46be33dcae00865dcc851fd58ff95c419a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7860a7857bb8fb6e4b9b353fcf34d84322eb24d2c539304ea4496b7937932c4d`

```dockerfile
```

-	Layers:
	-	`sha256:f22151502df928d19d2a8d8f234da857a6d78c6de4b76b4ffc06ed4e76ff80c3`  
		Last Modified: Thu, 04 Sep 2025 18:49:57 GMT  
		Size: 26.9 KB (26919 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.2.29`

```console
$ docker pull clickhouse@sha256:30e6b08a3371f0837a88ecc90568e9bc22e1316f75250f4c102cf2bcd28afa8e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.2.29` - linux; amd64

```console
$ docker pull clickhouse@sha256:70374eab8db97e716c0c803b8e426526567a852ea46c4fbbaffa20aadb6bddda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.6 MB (227646811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2712c652b4c632d10c2b1e7525a9e55cb75a477d208a03d0d5f4a69e3b880170`
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
# Thu, 04 Sep 2025 16:06:14 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 04 Sep 2025 16:06:14 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPO_CHANNEL=stable
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 04 Sep 2025 16:06:14 GMT
ARG VERSION=25.8.2.29
# Thu, 04 Sep 2025 16:06:14 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ENV LANG=en_US.UTF-8
# Thu, 04 Sep 2025 16:06:14 GMT
ENV TZ=UTC
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 04 Sep 2025 16:06:14 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 04 Sep 2025 16:06:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 04 Sep 2025 16:06:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2674d38b8300b858879b0e7bc2f778d915ea4988dee3908123e8a5ae14c2185`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 7.6 MB (7598429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0716cebfee9c18bfbac80c646f5717ca53f7d6b70451c5a30ecf6539e91fac6`  
		Last Modified: Thu, 04 Sep 2025 18:31:08 GMT  
		Size: 189.6 MB (189641425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc9e8dce7ae686e1f14c0590e855c6cccba74ec64742505427ed9c077c0b3a0`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff903e1c3fca299ee3267558f234215acd3c6359130611bd3b914ce39fec2e94`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ca8d80efc007ad421b2edbebd579205d26e5b24dd9368b1a7fcbee2936d1c6`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450458a8fa14ce6ea48552cbac580e000b33f200bfe5d5f74dda19dc36b33d04`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb98d5afe64ab4f4c464946cf3e840f85923798e29c22c321e892d435a10e39f`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.2.29` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9d73c85ac5c80ce6e5ae0e4577c706687576573e83c738b24d63675c0d3bb7c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d975838095cb1936f50f2b0a3f7b35936b3c1d3750d873626de144db9f345ae`

```dockerfile
```

-	Layers:
	-	`sha256:05a206c5ac24002577f1380ef90af02fc64eef6eb74e89df0f0241de04709f67`  
		Last Modified: Thu, 04 Sep 2025 18:49:53 GMT  
		Size: 26.7 KB (26683 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.2.29` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:faf446bacfba09029ad4542899d4e96e43d67da7681bf3afae1ca56a732a5849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212396721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571824efb148de6116d9ad9d75469041a29601827f6aecdb256f4eb1829a0a6e`
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
# Thu, 04 Sep 2025 16:06:14 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 04 Sep 2025 16:06:14 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPO_CHANNEL=stable
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 04 Sep 2025 16:06:14 GMT
ARG VERSION=25.8.2.29
# Thu, 04 Sep 2025 16:06:14 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ENV LANG=en_US.UTF-8
# Thu, 04 Sep 2025 16:06:14 GMT
ENV TZ=UTC
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 04 Sep 2025 16:06:14 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 04 Sep 2025 16:06:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 04 Sep 2025 16:06:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5ec0191b4ea618855356e7f5642643723d508ce4a081599087506aacec3635`  
		Last Modified: Thu, 04 Sep 2025 18:31:02 GMT  
		Size: 7.6 MB (7577271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f0b5998b053fb76c44f29c05b0c890cfb16d3f6ac26332f4a077d04aec0b23`  
		Last Modified: Thu, 04 Sep 2025 18:31:25 GMT  
		Size: 176.6 MB (176587956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d1d145fe1a57c3893100205acdcb0271fb6878db7926ebf738da1e11098159`  
		Last Modified: Thu, 04 Sep 2025 18:08:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a0dffe6609b09c327f4d70e0e75f9c2472241217ceb9fa245b44fb1444744c`  
		Last Modified: Thu, 04 Sep 2025 18:08:13 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62bf014b26c1ca3ff8c228697c11b42ff86e6f550d5882953aee5780be4f56f3`  
		Last Modified: Thu, 04 Sep 2025 18:08:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beaa6239d0f79e1cc6dd43bd5cc8fb93810c186a1bcfa7a60f6d296b96d68a9c`  
		Last Modified: Thu, 04 Sep 2025 18:08:13 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b011b7349796e6a7547c09f02b5433ba94731e3f0b01e606efb62fe91d30095b`  
		Last Modified: Thu, 04 Sep 2025 18:08:12 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.2.29` - unknown; unknown

```console
$ docker pull clickhouse@sha256:398e24d59bf5b944d28318e7d7bf46be33dcae00865dcc851fd58ff95c419a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7860a7857bb8fb6e4b9b353fcf34d84322eb24d2c539304ea4496b7937932c4d`

```dockerfile
```

-	Layers:
	-	`sha256:f22151502df928d19d2a8d8f234da857a6d78c6de4b76b4ffc06ed4e76ff80c3`  
		Last Modified: Thu, 04 Sep 2025 18:49:57 GMT  
		Size: 26.9 KB (26919 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.2.29-jammy`

```console
$ docker pull clickhouse@sha256:30e6b08a3371f0837a88ecc90568e9bc22e1316f75250f4c102cf2bcd28afa8e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.2.29-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:70374eab8db97e716c0c803b8e426526567a852ea46c4fbbaffa20aadb6bddda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.6 MB (227646811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2712c652b4c632d10c2b1e7525a9e55cb75a477d208a03d0d5f4a69e3b880170`
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
# Thu, 04 Sep 2025 16:06:14 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 04 Sep 2025 16:06:14 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPO_CHANNEL=stable
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 04 Sep 2025 16:06:14 GMT
ARG VERSION=25.8.2.29
# Thu, 04 Sep 2025 16:06:14 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ENV LANG=en_US.UTF-8
# Thu, 04 Sep 2025 16:06:14 GMT
ENV TZ=UTC
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 04 Sep 2025 16:06:14 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 04 Sep 2025 16:06:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 04 Sep 2025 16:06:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2674d38b8300b858879b0e7bc2f778d915ea4988dee3908123e8a5ae14c2185`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 7.6 MB (7598429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0716cebfee9c18bfbac80c646f5717ca53f7d6b70451c5a30ecf6539e91fac6`  
		Last Modified: Thu, 04 Sep 2025 18:31:08 GMT  
		Size: 189.6 MB (189641425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc9e8dce7ae686e1f14c0590e855c6cccba74ec64742505427ed9c077c0b3a0`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff903e1c3fca299ee3267558f234215acd3c6359130611bd3b914ce39fec2e94`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ca8d80efc007ad421b2edbebd579205d26e5b24dd9368b1a7fcbee2936d1c6`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450458a8fa14ce6ea48552cbac580e000b33f200bfe5d5f74dda19dc36b33d04`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb98d5afe64ab4f4c464946cf3e840f85923798e29c22c321e892d435a10e39f`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.2.29-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9d73c85ac5c80ce6e5ae0e4577c706687576573e83c738b24d63675c0d3bb7c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d975838095cb1936f50f2b0a3f7b35936b3c1d3750d873626de144db9f345ae`

```dockerfile
```

-	Layers:
	-	`sha256:05a206c5ac24002577f1380ef90af02fc64eef6eb74e89df0f0241de04709f67`  
		Last Modified: Thu, 04 Sep 2025 18:49:53 GMT  
		Size: 26.7 KB (26683 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.2.29-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:faf446bacfba09029ad4542899d4e96e43d67da7681bf3afae1ca56a732a5849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212396721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571824efb148de6116d9ad9d75469041a29601827f6aecdb256f4eb1829a0a6e`
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
# Thu, 04 Sep 2025 16:06:14 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 04 Sep 2025 16:06:14 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPO_CHANNEL=stable
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 04 Sep 2025 16:06:14 GMT
ARG VERSION=25.8.2.29
# Thu, 04 Sep 2025 16:06:14 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ENV LANG=en_US.UTF-8
# Thu, 04 Sep 2025 16:06:14 GMT
ENV TZ=UTC
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 04 Sep 2025 16:06:14 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 04 Sep 2025 16:06:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 04 Sep 2025 16:06:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5ec0191b4ea618855356e7f5642643723d508ce4a081599087506aacec3635`  
		Last Modified: Thu, 04 Sep 2025 18:31:02 GMT  
		Size: 7.6 MB (7577271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f0b5998b053fb76c44f29c05b0c890cfb16d3f6ac26332f4a077d04aec0b23`  
		Last Modified: Thu, 04 Sep 2025 18:31:25 GMT  
		Size: 176.6 MB (176587956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d1d145fe1a57c3893100205acdcb0271fb6878db7926ebf738da1e11098159`  
		Last Modified: Thu, 04 Sep 2025 18:08:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a0dffe6609b09c327f4d70e0e75f9c2472241217ceb9fa245b44fb1444744c`  
		Last Modified: Thu, 04 Sep 2025 18:08:13 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62bf014b26c1ca3ff8c228697c11b42ff86e6f550d5882953aee5780be4f56f3`  
		Last Modified: Thu, 04 Sep 2025 18:08:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beaa6239d0f79e1cc6dd43bd5cc8fb93810c186a1bcfa7a60f6d296b96d68a9c`  
		Last Modified: Thu, 04 Sep 2025 18:08:13 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b011b7349796e6a7547c09f02b5433ba94731e3f0b01e606efb62fe91d30095b`  
		Last Modified: Thu, 04 Sep 2025 18:08:12 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.2.29-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:398e24d59bf5b944d28318e7d7bf46be33dcae00865dcc851fd58ff95c419a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7860a7857bb8fb6e4b9b353fcf34d84322eb24d2c539304ea4496b7937932c4d`

```dockerfile
```

-	Layers:
	-	`sha256:f22151502df928d19d2a8d8f234da857a6d78c6de4b76b4ffc06ed4e76ff80c3`  
		Last Modified: Thu, 04 Sep 2025 18:49:57 GMT  
		Size: 26.9 KB (26919 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:jammy`

```console
$ docker pull clickhouse@sha256:30e6b08a3371f0837a88ecc90568e9bc22e1316f75250f4c102cf2bcd28afa8e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:70374eab8db97e716c0c803b8e426526567a852ea46c4fbbaffa20aadb6bddda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.6 MB (227646811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2712c652b4c632d10c2b1e7525a9e55cb75a477d208a03d0d5f4a69e3b880170`
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
# Thu, 04 Sep 2025 16:06:14 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 04 Sep 2025 16:06:14 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPO_CHANNEL=stable
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 04 Sep 2025 16:06:14 GMT
ARG VERSION=25.8.2.29
# Thu, 04 Sep 2025 16:06:14 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ENV LANG=en_US.UTF-8
# Thu, 04 Sep 2025 16:06:14 GMT
ENV TZ=UTC
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 04 Sep 2025 16:06:14 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 04 Sep 2025 16:06:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 04 Sep 2025 16:06:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2674d38b8300b858879b0e7bc2f778d915ea4988dee3908123e8a5ae14c2185`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 7.6 MB (7598429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0716cebfee9c18bfbac80c646f5717ca53f7d6b70451c5a30ecf6539e91fac6`  
		Last Modified: Thu, 04 Sep 2025 18:31:08 GMT  
		Size: 189.6 MB (189641425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc9e8dce7ae686e1f14c0590e855c6cccba74ec64742505427ed9c077c0b3a0`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff903e1c3fca299ee3267558f234215acd3c6359130611bd3b914ce39fec2e94`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ca8d80efc007ad421b2edbebd579205d26e5b24dd9368b1a7fcbee2936d1c6`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450458a8fa14ce6ea48552cbac580e000b33f200bfe5d5f74dda19dc36b33d04`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb98d5afe64ab4f4c464946cf3e840f85923798e29c22c321e892d435a10e39f`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9d73c85ac5c80ce6e5ae0e4577c706687576573e83c738b24d63675c0d3bb7c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d975838095cb1936f50f2b0a3f7b35936b3c1d3750d873626de144db9f345ae`

```dockerfile
```

-	Layers:
	-	`sha256:05a206c5ac24002577f1380ef90af02fc64eef6eb74e89df0f0241de04709f67`  
		Last Modified: Thu, 04 Sep 2025 18:49:53 GMT  
		Size: 26.7 KB (26683 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:faf446bacfba09029ad4542899d4e96e43d67da7681bf3afae1ca56a732a5849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212396721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571824efb148de6116d9ad9d75469041a29601827f6aecdb256f4eb1829a0a6e`
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
# Thu, 04 Sep 2025 16:06:14 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 04 Sep 2025 16:06:14 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPO_CHANNEL=stable
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 04 Sep 2025 16:06:14 GMT
ARG VERSION=25.8.2.29
# Thu, 04 Sep 2025 16:06:14 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ENV LANG=en_US.UTF-8
# Thu, 04 Sep 2025 16:06:14 GMT
ENV TZ=UTC
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 04 Sep 2025 16:06:14 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 04 Sep 2025 16:06:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 04 Sep 2025 16:06:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5ec0191b4ea618855356e7f5642643723d508ce4a081599087506aacec3635`  
		Last Modified: Thu, 04 Sep 2025 18:31:02 GMT  
		Size: 7.6 MB (7577271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f0b5998b053fb76c44f29c05b0c890cfb16d3f6ac26332f4a077d04aec0b23`  
		Last Modified: Thu, 04 Sep 2025 18:31:25 GMT  
		Size: 176.6 MB (176587956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d1d145fe1a57c3893100205acdcb0271fb6878db7926ebf738da1e11098159`  
		Last Modified: Thu, 04 Sep 2025 18:08:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a0dffe6609b09c327f4d70e0e75f9c2472241217ceb9fa245b44fb1444744c`  
		Last Modified: Thu, 04 Sep 2025 18:08:13 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62bf014b26c1ca3ff8c228697c11b42ff86e6f550d5882953aee5780be4f56f3`  
		Last Modified: Thu, 04 Sep 2025 18:08:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beaa6239d0f79e1cc6dd43bd5cc8fb93810c186a1bcfa7a60f6d296b96d68a9c`  
		Last Modified: Thu, 04 Sep 2025 18:08:13 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b011b7349796e6a7547c09f02b5433ba94731e3f0b01e606efb62fe91d30095b`  
		Last Modified: Thu, 04 Sep 2025 18:08:12 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:398e24d59bf5b944d28318e7d7bf46be33dcae00865dcc851fd58ff95c419a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7860a7857bb8fb6e4b9b353fcf34d84322eb24d2c539304ea4496b7937932c4d`

```dockerfile
```

-	Layers:
	-	`sha256:f22151502df928d19d2a8d8f234da857a6d78c6de4b76b4ffc06ed4e76ff80c3`  
		Last Modified: Thu, 04 Sep 2025 18:49:57 GMT  
		Size: 26.9 KB (26919 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:30e6b08a3371f0837a88ecc90568e9bc22e1316f75250f4c102cf2bcd28afa8e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

```console
$ docker pull clickhouse@sha256:70374eab8db97e716c0c803b8e426526567a852ea46c4fbbaffa20aadb6bddda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.6 MB (227646811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2712c652b4c632d10c2b1e7525a9e55cb75a477d208a03d0d5f4a69e3b880170`
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
# Thu, 04 Sep 2025 16:06:14 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 04 Sep 2025 16:06:14 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPO_CHANNEL=stable
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 04 Sep 2025 16:06:14 GMT
ARG VERSION=25.8.2.29
# Thu, 04 Sep 2025 16:06:14 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ENV LANG=en_US.UTF-8
# Thu, 04 Sep 2025 16:06:14 GMT
ENV TZ=UTC
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 04 Sep 2025 16:06:14 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 04 Sep 2025 16:06:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 04 Sep 2025 16:06:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2674d38b8300b858879b0e7bc2f778d915ea4988dee3908123e8a5ae14c2185`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 7.6 MB (7598429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0716cebfee9c18bfbac80c646f5717ca53f7d6b70451c5a30ecf6539e91fac6`  
		Last Modified: Thu, 04 Sep 2025 18:31:08 GMT  
		Size: 189.6 MB (189641425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc9e8dce7ae686e1f14c0590e855c6cccba74ec64742505427ed9c077c0b3a0`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff903e1c3fca299ee3267558f234215acd3c6359130611bd3b914ce39fec2e94`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ca8d80efc007ad421b2edbebd579205d26e5b24dd9368b1a7fcbee2936d1c6`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450458a8fa14ce6ea48552cbac580e000b33f200bfe5d5f74dda19dc36b33d04`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb98d5afe64ab4f4c464946cf3e840f85923798e29c22c321e892d435a10e39f`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9d73c85ac5c80ce6e5ae0e4577c706687576573e83c738b24d63675c0d3bb7c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d975838095cb1936f50f2b0a3f7b35936b3c1d3750d873626de144db9f345ae`

```dockerfile
```

-	Layers:
	-	`sha256:05a206c5ac24002577f1380ef90af02fc64eef6eb74e89df0f0241de04709f67`  
		Last Modified: Thu, 04 Sep 2025 18:49:53 GMT  
		Size: 26.7 KB (26683 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:faf446bacfba09029ad4542899d4e96e43d67da7681bf3afae1ca56a732a5849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212396721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571824efb148de6116d9ad9d75469041a29601827f6aecdb256f4eb1829a0a6e`
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
# Thu, 04 Sep 2025 16:06:14 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 04 Sep 2025 16:06:14 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPO_CHANNEL=stable
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 04 Sep 2025 16:06:14 GMT
ARG VERSION=25.8.2.29
# Thu, 04 Sep 2025 16:06:14 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ENV LANG=en_US.UTF-8
# Thu, 04 Sep 2025 16:06:14 GMT
ENV TZ=UTC
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 04 Sep 2025 16:06:14 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 04 Sep 2025 16:06:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 04 Sep 2025 16:06:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5ec0191b4ea618855356e7f5642643723d508ce4a081599087506aacec3635`  
		Last Modified: Thu, 04 Sep 2025 18:31:02 GMT  
		Size: 7.6 MB (7577271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f0b5998b053fb76c44f29c05b0c890cfb16d3f6ac26332f4a077d04aec0b23`  
		Last Modified: Thu, 04 Sep 2025 18:31:25 GMT  
		Size: 176.6 MB (176587956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d1d145fe1a57c3893100205acdcb0271fb6878db7926ebf738da1e11098159`  
		Last Modified: Thu, 04 Sep 2025 18:08:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a0dffe6609b09c327f4d70e0e75f9c2472241217ceb9fa245b44fb1444744c`  
		Last Modified: Thu, 04 Sep 2025 18:08:13 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62bf014b26c1ca3ff8c228697c11b42ff86e6f550d5882953aee5780be4f56f3`  
		Last Modified: Thu, 04 Sep 2025 18:08:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beaa6239d0f79e1cc6dd43bd5cc8fb93810c186a1bcfa7a60f6d296b96d68a9c`  
		Last Modified: Thu, 04 Sep 2025 18:08:13 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b011b7349796e6a7547c09f02b5433ba94731e3f0b01e606efb62fe91d30095b`  
		Last Modified: Thu, 04 Sep 2025 18:08:12 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:398e24d59bf5b944d28318e7d7bf46be33dcae00865dcc851fd58ff95c419a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7860a7857bb8fb6e4b9b353fcf34d84322eb24d2c539304ea4496b7937932c4d`

```dockerfile
```

-	Layers:
	-	`sha256:f22151502df928d19d2a8d8f234da857a6d78c6de4b76b4ffc06ed4e76ff80c3`  
		Last Modified: Thu, 04 Sep 2025 18:49:57 GMT  
		Size: 26.9 KB (26919 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts`

```console
$ docker pull clickhouse@sha256:30e6b08a3371f0837a88ecc90568e9bc22e1316f75250f4c102cf2bcd28afa8e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts` - linux; amd64

```console
$ docker pull clickhouse@sha256:70374eab8db97e716c0c803b8e426526567a852ea46c4fbbaffa20aadb6bddda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.6 MB (227646811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2712c652b4c632d10c2b1e7525a9e55cb75a477d208a03d0d5f4a69e3b880170`
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
# Thu, 04 Sep 2025 16:06:14 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 04 Sep 2025 16:06:14 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPO_CHANNEL=stable
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 04 Sep 2025 16:06:14 GMT
ARG VERSION=25.8.2.29
# Thu, 04 Sep 2025 16:06:14 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ENV LANG=en_US.UTF-8
# Thu, 04 Sep 2025 16:06:14 GMT
ENV TZ=UTC
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 04 Sep 2025 16:06:14 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 04 Sep 2025 16:06:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 04 Sep 2025 16:06:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2674d38b8300b858879b0e7bc2f778d915ea4988dee3908123e8a5ae14c2185`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 7.6 MB (7598429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0716cebfee9c18bfbac80c646f5717ca53f7d6b70451c5a30ecf6539e91fac6`  
		Last Modified: Thu, 04 Sep 2025 18:31:08 GMT  
		Size: 189.6 MB (189641425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc9e8dce7ae686e1f14c0590e855c6cccba74ec64742505427ed9c077c0b3a0`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff903e1c3fca299ee3267558f234215acd3c6359130611bd3b914ce39fec2e94`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ca8d80efc007ad421b2edbebd579205d26e5b24dd9368b1a7fcbee2936d1c6`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450458a8fa14ce6ea48552cbac580e000b33f200bfe5d5f74dda19dc36b33d04`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb98d5afe64ab4f4c464946cf3e840f85923798e29c22c321e892d435a10e39f`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9d73c85ac5c80ce6e5ae0e4577c706687576573e83c738b24d63675c0d3bb7c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d975838095cb1936f50f2b0a3f7b35936b3c1d3750d873626de144db9f345ae`

```dockerfile
```

-	Layers:
	-	`sha256:05a206c5ac24002577f1380ef90af02fc64eef6eb74e89df0f0241de04709f67`  
		Last Modified: Thu, 04 Sep 2025 18:49:53 GMT  
		Size: 26.7 KB (26683 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:faf446bacfba09029ad4542899d4e96e43d67da7681bf3afae1ca56a732a5849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212396721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571824efb148de6116d9ad9d75469041a29601827f6aecdb256f4eb1829a0a6e`
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
# Thu, 04 Sep 2025 16:06:14 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 04 Sep 2025 16:06:14 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPO_CHANNEL=stable
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 04 Sep 2025 16:06:14 GMT
ARG VERSION=25.8.2.29
# Thu, 04 Sep 2025 16:06:14 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ENV LANG=en_US.UTF-8
# Thu, 04 Sep 2025 16:06:14 GMT
ENV TZ=UTC
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 04 Sep 2025 16:06:14 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 04 Sep 2025 16:06:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 04 Sep 2025 16:06:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5ec0191b4ea618855356e7f5642643723d508ce4a081599087506aacec3635`  
		Last Modified: Thu, 04 Sep 2025 18:31:02 GMT  
		Size: 7.6 MB (7577271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f0b5998b053fb76c44f29c05b0c890cfb16d3f6ac26332f4a077d04aec0b23`  
		Last Modified: Thu, 04 Sep 2025 18:31:25 GMT  
		Size: 176.6 MB (176587956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d1d145fe1a57c3893100205acdcb0271fb6878db7926ebf738da1e11098159`  
		Last Modified: Thu, 04 Sep 2025 18:08:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a0dffe6609b09c327f4d70e0e75f9c2472241217ceb9fa245b44fb1444744c`  
		Last Modified: Thu, 04 Sep 2025 18:08:13 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62bf014b26c1ca3ff8c228697c11b42ff86e6f550d5882953aee5780be4f56f3`  
		Last Modified: Thu, 04 Sep 2025 18:08:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beaa6239d0f79e1cc6dd43bd5cc8fb93810c186a1bcfa7a60f6d296b96d68a9c`  
		Last Modified: Thu, 04 Sep 2025 18:08:13 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b011b7349796e6a7547c09f02b5433ba94731e3f0b01e606efb62fe91d30095b`  
		Last Modified: Thu, 04 Sep 2025 18:08:12 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:398e24d59bf5b944d28318e7d7bf46be33dcae00865dcc851fd58ff95c419a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7860a7857bb8fb6e4b9b353fcf34d84322eb24d2c539304ea4496b7937932c4d`

```dockerfile
```

-	Layers:
	-	`sha256:f22151502df928d19d2a8d8f234da857a6d78c6de4b76b4ffc06ed4e76ff80c3`  
		Last Modified: Thu, 04 Sep 2025 18:49:57 GMT  
		Size: 26.9 KB (26919 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts-jammy`

```console
$ docker pull clickhouse@sha256:30e6b08a3371f0837a88ecc90568e9bc22e1316f75250f4c102cf2bcd28afa8e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:70374eab8db97e716c0c803b8e426526567a852ea46c4fbbaffa20aadb6bddda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.6 MB (227646811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2712c652b4c632d10c2b1e7525a9e55cb75a477d208a03d0d5f4a69e3b880170`
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
# Thu, 04 Sep 2025 16:06:14 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 04 Sep 2025 16:06:14 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPO_CHANNEL=stable
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 04 Sep 2025 16:06:14 GMT
ARG VERSION=25.8.2.29
# Thu, 04 Sep 2025 16:06:14 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ENV LANG=en_US.UTF-8
# Thu, 04 Sep 2025 16:06:14 GMT
ENV TZ=UTC
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 04 Sep 2025 16:06:14 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 04 Sep 2025 16:06:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 04 Sep 2025 16:06:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2674d38b8300b858879b0e7bc2f778d915ea4988dee3908123e8a5ae14c2185`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 7.6 MB (7598429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0716cebfee9c18bfbac80c646f5717ca53f7d6b70451c5a30ecf6539e91fac6`  
		Last Modified: Thu, 04 Sep 2025 18:31:08 GMT  
		Size: 189.6 MB (189641425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc9e8dce7ae686e1f14c0590e855c6cccba74ec64742505427ed9c077c0b3a0`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff903e1c3fca299ee3267558f234215acd3c6359130611bd3b914ce39fec2e94`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ca8d80efc007ad421b2edbebd579205d26e5b24dd9368b1a7fcbee2936d1c6`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450458a8fa14ce6ea48552cbac580e000b33f200bfe5d5f74dda19dc36b33d04`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb98d5afe64ab4f4c464946cf3e840f85923798e29c22c321e892d435a10e39f`  
		Last Modified: Thu, 04 Sep 2025 17:26:44 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9d73c85ac5c80ce6e5ae0e4577c706687576573e83c738b24d63675c0d3bb7c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d975838095cb1936f50f2b0a3f7b35936b3c1d3750d873626de144db9f345ae`

```dockerfile
```

-	Layers:
	-	`sha256:05a206c5ac24002577f1380ef90af02fc64eef6eb74e89df0f0241de04709f67`  
		Last Modified: Thu, 04 Sep 2025 18:49:53 GMT  
		Size: 26.7 KB (26683 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:faf446bacfba09029ad4542899d4e96e43d67da7681bf3afae1ca56a732a5849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212396721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571824efb148de6116d9ad9d75469041a29601827f6aecdb256f4eb1829a0a6e`
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
# Thu, 04 Sep 2025 16:06:14 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 04 Sep 2025 16:06:14 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPO_CHANNEL=stable
# Thu, 04 Sep 2025 16:06:14 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 04 Sep 2025 16:06:14 GMT
ARG VERSION=25.8.2.29
# Thu, 04 Sep 2025 16:06:14 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
ENV LANG=en_US.UTF-8
# Thu, 04 Sep 2025 16:06:14 GMT
ENV TZ=UTC
# Thu, 04 Sep 2025 16:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.2.29 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 04 Sep 2025 16:06:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 04 Sep 2025 16:06:14 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 04 Sep 2025 16:06:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 04 Sep 2025 16:06:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5ec0191b4ea618855356e7f5642643723d508ce4a081599087506aacec3635`  
		Last Modified: Thu, 04 Sep 2025 18:31:02 GMT  
		Size: 7.6 MB (7577271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f0b5998b053fb76c44f29c05b0c890cfb16d3f6ac26332f4a077d04aec0b23`  
		Last Modified: Thu, 04 Sep 2025 18:31:25 GMT  
		Size: 176.6 MB (176587956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d1d145fe1a57c3893100205acdcb0271fb6878db7926ebf738da1e11098159`  
		Last Modified: Thu, 04 Sep 2025 18:08:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a0dffe6609b09c327f4d70e0e75f9c2472241217ceb9fa245b44fb1444744c`  
		Last Modified: Thu, 04 Sep 2025 18:08:13 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62bf014b26c1ca3ff8c228697c11b42ff86e6f550d5882953aee5780be4f56f3`  
		Last Modified: Thu, 04 Sep 2025 18:08:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beaa6239d0f79e1cc6dd43bd5cc8fb93810c186a1bcfa7a60f6d296b96d68a9c`  
		Last Modified: Thu, 04 Sep 2025 18:08:13 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b011b7349796e6a7547c09f02b5433ba94731e3f0b01e606efb62fe91d30095b`  
		Last Modified: Thu, 04 Sep 2025 18:08:12 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:398e24d59bf5b944d28318e7d7bf46be33dcae00865dcc851fd58ff95c419a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7860a7857bb8fb6e4b9b353fcf34d84322eb24d2c539304ea4496b7937932c4d`

```dockerfile
```

-	Layers:
	-	`sha256:f22151502df928d19d2a8d8f234da857a6d78c6de4b76b4ffc06ed4e76ff80c3`  
		Last Modified: Thu, 04 Sep 2025 18:49:57 GMT  
		Size: 26.9 KB (26919 bytes)  
		MIME: application/vnd.in-toto+json
