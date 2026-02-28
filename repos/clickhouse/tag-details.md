<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clickhouse`

-	[`clickhouse:25.11`](#clickhouse2511)
-	[`clickhouse:25.11-jammy`](#clickhouse2511-jammy)
-	[`clickhouse:25.11.9`](#clickhouse25119)
-	[`clickhouse:25.11.9-jammy`](#clickhouse25119-jammy)
-	[`clickhouse:25.11.9.34`](#clickhouse2511934)
-	[`clickhouse:25.11.9.34-jammy`](#clickhouse2511934-jammy)
-	[`clickhouse:25.12`](#clickhouse2512)
-	[`clickhouse:25.12-jammy`](#clickhouse2512-jammy)
-	[`clickhouse:25.12.7`](#clickhouse25127)
-	[`clickhouse:25.12.7-jammy`](#clickhouse25127-jammy)
-	[`clickhouse:25.12.7.21`](#clickhouse2512721)
-	[`clickhouse:25.12.7.21-jammy`](#clickhouse2512721-jammy)
-	[`clickhouse:25.3`](#clickhouse253)
-	[`clickhouse:25.3-jammy`](#clickhouse253-jammy)
-	[`clickhouse:25.3.14`](#clickhouse25314)
-	[`clickhouse:25.3.14-jammy`](#clickhouse25314-jammy)
-	[`clickhouse:25.3.14.14`](#clickhouse2531414)
-	[`clickhouse:25.3.14.14-jammy`](#clickhouse2531414-jammy)
-	[`clickhouse:25.8`](#clickhouse258)
-	[`clickhouse:25.8-jammy`](#clickhouse258-jammy)
-	[`clickhouse:25.8.16`](#clickhouse25816)
-	[`clickhouse:25.8.16-jammy`](#clickhouse25816-jammy)
-	[`clickhouse:25.8.16.34`](#clickhouse2581634)
-	[`clickhouse:25.8.16.34-jammy`](#clickhouse2581634-jammy)
-	[`clickhouse:26.1`](#clickhouse261)
-	[`clickhouse:26.1-jammy`](#clickhouse261-jammy)
-	[`clickhouse:26.1.3`](#clickhouse2613)
-	[`clickhouse:26.1.3-jammy`](#clickhouse2613-jammy)
-	[`clickhouse:26.1.3.52`](#clickhouse261352)
-	[`clickhouse:26.1.3.52-jammy`](#clickhouse261352-jammy)
-	[`clickhouse:jammy`](#clickhousejammy)
-	[`clickhouse:latest`](#clickhouselatest)
-	[`clickhouse:lts`](#clickhouselts)
-	[`clickhouse:lts-jammy`](#clickhouselts-jammy)

## `clickhouse:25.11`

```console
$ docker pull clickhouse@sha256:d0f71dc3b05893b2377fb33c82fa435e865e93865f4f6ca40ef2c2ae1106883f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.11` - linux; amd64

```console
$ docker pull clickhouse@sha256:69cde8aacd11527a6c1e8a311a30389fe0a78fe79d1b01c947ba8bf2bb2863b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233937404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d0dec1a3e9e01d5a665954d92ffe8378028ae544a487799dfeb88d21175b302`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 20 Feb 2026 18:56:02 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Feb 2026 18:56:02 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Feb 2026 18:56:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Feb 2026 18:56:02 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Feb 2026 18:56:02 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Feb 2026 18:56:02 GMT
ARG VERSION=25.11.9.34
# Fri, 20 Feb 2026 18:56:02 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Feb 2026 18:57:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.9.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:57:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.9.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:57:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.9.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Feb 2026 18:57:28 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Feb 2026 18:57:28 GMT
ENV TZ=UTC
# Fri, 20 Feb 2026 18:57:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.9.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Feb 2026 18:57:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Feb 2026 18:57:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Feb 2026 18:57:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Feb 2026 18:57:28 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Feb 2026 18:57:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Feb 2026 18:57:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6264629b10e9e86b9f3a55076a22cf04acd714130d22ca018783540fae2cea54`  
		Last Modified: Fri, 20 Feb 2026 18:56:49 GMT  
		Size: 7.6 MB (7598309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfc285133e340947ee6e7438899068df5a2213a33acca1231ab92df4ed6df43`  
		Last Modified: Fri, 20 Feb 2026 18:57:52 GMT  
		Size: 195.9 MB (195931680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c95762452ce9ec719051e189c2a20ae2875deb609402d47541fbc56ca79fb71`  
		Last Modified: Fri, 20 Feb 2026 18:57:47 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f77838964c13a3627be462112daf496650eb819e88148f87cb8ee6a211c7de34`  
		Last Modified: Fri, 20 Feb 2026 18:57:47 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12314fc3b24f761f8d8fbe8104e4b6fc14feba2e569ab51de0fc799dda5e99c8`  
		Last Modified: Fri, 20 Feb 2026 18:57:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ae543998e7cada9d1e88c4ce546c35e69e7afb1ce8bda93337822ecce32853`  
		Last Modified: Fri, 20 Feb 2026 18:57:48 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec38330e61a43af4b323386cb8f66622cfc795d055a9fcb45925703fb0ee499`  
		Last Modified: Fri, 20 Feb 2026 18:57:48 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11` - unknown; unknown

```console
$ docker pull clickhouse@sha256:410e5c77fcc35e9ced63de34cf69c008eb7c6d4772dcb92b6f6dd1f63cadcbbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2795aa4e3861cc85b22aeb3ee1cd8a06157dab720ff9f8f98d1f84b6f3e4554`

```dockerfile
```

-	Layers:
	-	`sha256:f69d02f14b4812898412ac294dc0dab2dc56794622e5884f95b2fe6f8b20fe21`  
		Last Modified: Fri, 20 Feb 2026 18:57:47 GMT  
		Size: 25.4 KB (25437 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.11` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:faa91d8bbe9c6ee8a82e563814793675d2ea507ef7f914ff2d9cfe3017e5cbe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218828329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2674f9a6e613b8267a7724d7526fe16e149dddcadee9d13456dc5562def3e43`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Fri, 20 Feb 2026 18:56:06 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Feb 2026 18:56:06 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Feb 2026 18:56:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Feb 2026 18:56:06 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Feb 2026 18:56:06 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Feb 2026 18:56:06 GMT
ARG VERSION=25.11.9.34
# Fri, 20 Feb 2026 18:56:06 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Feb 2026 18:57:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.9.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:57:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.9.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:57:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.9.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Feb 2026 18:57:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Feb 2026 18:57:32 GMT
ENV TZ=UTC
# Fri, 20 Feb 2026 18:57:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.9.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Feb 2026 18:57:32 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Feb 2026 18:57:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Feb 2026 18:57:32 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Feb 2026 18:57:32 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Feb 2026 18:57:32 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Feb 2026 18:57:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ddda68ab08dc984109a23de1a2466e333e45ed21633b824db1aa90595410ffd`  
		Last Modified: Fri, 20 Feb 2026 18:56:55 GMT  
		Size: 7.6 MB (7577563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605555697f58070013657afbc8682855063097608914b0cd5f6f878ce56f1073`  
		Last Modified: Fri, 20 Feb 2026 18:57:54 GMT  
		Size: 183.0 MB (182995773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4c95f52ffca5931405dcd68e38964d959dd72a0517252cfdb5aa369507c045`  
		Last Modified: Fri, 20 Feb 2026 18:57:50 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c3f60ff0b369d9319ab243cff5f1d988786c4ce5d69d3bb1c12353485d1b01`  
		Last Modified: Fri, 20 Feb 2026 18:57:50 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881cf1ccccbc524eea8008eb0b3b571fae69e2817d5730543bf7462af5218bd9`  
		Last Modified: Fri, 20 Feb 2026 18:57:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eda7848198b505e460c8e7335033d7a91b2949b1bdb3a03ec63cefbfb5815c7`  
		Last Modified: Fri, 20 Feb 2026 18:57:52 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92f82468ac7ae3788a577ef56dc4a961a9e5c27df04c5508fea7418b53f99f3`  
		Last Modified: Fri, 20 Feb 2026 18:57:52 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f91dc84ef4afd318ab2cf4b3ec55120d0f6e0048411820e4be4eeb819d3c269e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5a07dc724e6c7659a584b08655abb9ff7edacc7532e8a3952dc86e7652a7aa`

```dockerfile
```

-	Layers:
	-	`sha256:699ab0680de175f089dc279f322f8d199708e3d9fa5896fd93fbcfbec2a2c47b`  
		Last Modified: Fri, 20 Feb 2026 18:57:50 GMT  
		Size: 25.6 KB (25625 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.11-jammy`

```console
$ docker pull clickhouse@sha256:d0f71dc3b05893b2377fb33c82fa435e865e93865f4f6ca40ef2c2ae1106883f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.11-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:69cde8aacd11527a6c1e8a311a30389fe0a78fe79d1b01c947ba8bf2bb2863b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233937404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d0dec1a3e9e01d5a665954d92ffe8378028ae544a487799dfeb88d21175b302`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 20 Feb 2026 18:56:02 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Feb 2026 18:56:02 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Feb 2026 18:56:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Feb 2026 18:56:02 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Feb 2026 18:56:02 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Feb 2026 18:56:02 GMT
ARG VERSION=25.11.9.34
# Fri, 20 Feb 2026 18:56:02 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Feb 2026 18:57:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.9.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:57:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.9.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:57:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.9.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Feb 2026 18:57:28 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Feb 2026 18:57:28 GMT
ENV TZ=UTC
# Fri, 20 Feb 2026 18:57:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.9.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Feb 2026 18:57:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Feb 2026 18:57:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Feb 2026 18:57:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Feb 2026 18:57:28 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Feb 2026 18:57:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Feb 2026 18:57:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6264629b10e9e86b9f3a55076a22cf04acd714130d22ca018783540fae2cea54`  
		Last Modified: Fri, 20 Feb 2026 18:56:49 GMT  
		Size: 7.6 MB (7598309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfc285133e340947ee6e7438899068df5a2213a33acca1231ab92df4ed6df43`  
		Last Modified: Fri, 20 Feb 2026 18:57:52 GMT  
		Size: 195.9 MB (195931680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c95762452ce9ec719051e189c2a20ae2875deb609402d47541fbc56ca79fb71`  
		Last Modified: Fri, 20 Feb 2026 18:57:47 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f77838964c13a3627be462112daf496650eb819e88148f87cb8ee6a211c7de34`  
		Last Modified: Fri, 20 Feb 2026 18:57:47 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12314fc3b24f761f8d8fbe8104e4b6fc14feba2e569ab51de0fc799dda5e99c8`  
		Last Modified: Fri, 20 Feb 2026 18:57:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ae543998e7cada9d1e88c4ce546c35e69e7afb1ce8bda93337822ecce32853`  
		Last Modified: Fri, 20 Feb 2026 18:57:48 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec38330e61a43af4b323386cb8f66622cfc795d055a9fcb45925703fb0ee499`  
		Last Modified: Fri, 20 Feb 2026 18:57:48 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:410e5c77fcc35e9ced63de34cf69c008eb7c6d4772dcb92b6f6dd1f63cadcbbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2795aa4e3861cc85b22aeb3ee1cd8a06157dab720ff9f8f98d1f84b6f3e4554`

```dockerfile
```

-	Layers:
	-	`sha256:f69d02f14b4812898412ac294dc0dab2dc56794622e5884f95b2fe6f8b20fe21`  
		Last Modified: Fri, 20 Feb 2026 18:57:47 GMT  
		Size: 25.4 KB (25437 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.11-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:faa91d8bbe9c6ee8a82e563814793675d2ea507ef7f914ff2d9cfe3017e5cbe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218828329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2674f9a6e613b8267a7724d7526fe16e149dddcadee9d13456dc5562def3e43`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Fri, 20 Feb 2026 18:56:06 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Feb 2026 18:56:06 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Feb 2026 18:56:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Feb 2026 18:56:06 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Feb 2026 18:56:06 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Feb 2026 18:56:06 GMT
ARG VERSION=25.11.9.34
# Fri, 20 Feb 2026 18:56:06 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Feb 2026 18:57:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.9.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:57:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.9.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:57:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.9.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Feb 2026 18:57:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Feb 2026 18:57:32 GMT
ENV TZ=UTC
# Fri, 20 Feb 2026 18:57:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.9.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Feb 2026 18:57:32 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Feb 2026 18:57:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Feb 2026 18:57:32 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Feb 2026 18:57:32 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Feb 2026 18:57:32 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Feb 2026 18:57:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ddda68ab08dc984109a23de1a2466e333e45ed21633b824db1aa90595410ffd`  
		Last Modified: Fri, 20 Feb 2026 18:56:55 GMT  
		Size: 7.6 MB (7577563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605555697f58070013657afbc8682855063097608914b0cd5f6f878ce56f1073`  
		Last Modified: Fri, 20 Feb 2026 18:57:54 GMT  
		Size: 183.0 MB (182995773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4c95f52ffca5931405dcd68e38964d959dd72a0517252cfdb5aa369507c045`  
		Last Modified: Fri, 20 Feb 2026 18:57:50 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c3f60ff0b369d9319ab243cff5f1d988786c4ce5d69d3bb1c12353485d1b01`  
		Last Modified: Fri, 20 Feb 2026 18:57:50 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881cf1ccccbc524eea8008eb0b3b571fae69e2817d5730543bf7462af5218bd9`  
		Last Modified: Fri, 20 Feb 2026 18:57:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eda7848198b505e460c8e7335033d7a91b2949b1bdb3a03ec63cefbfb5815c7`  
		Last Modified: Fri, 20 Feb 2026 18:57:52 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92f82468ac7ae3788a577ef56dc4a961a9e5c27df04c5508fea7418b53f99f3`  
		Last Modified: Fri, 20 Feb 2026 18:57:52 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f91dc84ef4afd318ab2cf4b3ec55120d0f6e0048411820e4be4eeb819d3c269e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5a07dc724e6c7659a584b08655abb9ff7edacc7532e8a3952dc86e7652a7aa`

```dockerfile
```

-	Layers:
	-	`sha256:699ab0680de175f089dc279f322f8d199708e3d9fa5896fd93fbcfbec2a2c47b`  
		Last Modified: Fri, 20 Feb 2026 18:57:50 GMT  
		Size: 25.6 KB (25625 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.11.9`

```console
$ docker pull clickhouse@sha256:d0f71dc3b05893b2377fb33c82fa435e865e93865f4f6ca40ef2c2ae1106883f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.11.9` - linux; amd64

```console
$ docker pull clickhouse@sha256:69cde8aacd11527a6c1e8a311a30389fe0a78fe79d1b01c947ba8bf2bb2863b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233937404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d0dec1a3e9e01d5a665954d92ffe8378028ae544a487799dfeb88d21175b302`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 20 Feb 2026 18:56:02 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Feb 2026 18:56:02 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Feb 2026 18:56:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Feb 2026 18:56:02 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Feb 2026 18:56:02 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Feb 2026 18:56:02 GMT
ARG VERSION=25.11.9.34
# Fri, 20 Feb 2026 18:56:02 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Feb 2026 18:57:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.9.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:57:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.9.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:57:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.9.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Feb 2026 18:57:28 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Feb 2026 18:57:28 GMT
ENV TZ=UTC
# Fri, 20 Feb 2026 18:57:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.9.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Feb 2026 18:57:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Feb 2026 18:57:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Feb 2026 18:57:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Feb 2026 18:57:28 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Feb 2026 18:57:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Feb 2026 18:57:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6264629b10e9e86b9f3a55076a22cf04acd714130d22ca018783540fae2cea54`  
		Last Modified: Fri, 20 Feb 2026 18:56:49 GMT  
		Size: 7.6 MB (7598309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfc285133e340947ee6e7438899068df5a2213a33acca1231ab92df4ed6df43`  
		Last Modified: Fri, 20 Feb 2026 18:57:52 GMT  
		Size: 195.9 MB (195931680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c95762452ce9ec719051e189c2a20ae2875deb609402d47541fbc56ca79fb71`  
		Last Modified: Fri, 20 Feb 2026 18:57:47 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f77838964c13a3627be462112daf496650eb819e88148f87cb8ee6a211c7de34`  
		Last Modified: Fri, 20 Feb 2026 18:57:47 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12314fc3b24f761f8d8fbe8104e4b6fc14feba2e569ab51de0fc799dda5e99c8`  
		Last Modified: Fri, 20 Feb 2026 18:57:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ae543998e7cada9d1e88c4ce546c35e69e7afb1ce8bda93337822ecce32853`  
		Last Modified: Fri, 20 Feb 2026 18:57:48 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec38330e61a43af4b323386cb8f66622cfc795d055a9fcb45925703fb0ee499`  
		Last Modified: Fri, 20 Feb 2026 18:57:48 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.9` - unknown; unknown

```console
$ docker pull clickhouse@sha256:410e5c77fcc35e9ced63de34cf69c008eb7c6d4772dcb92b6f6dd1f63cadcbbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2795aa4e3861cc85b22aeb3ee1cd8a06157dab720ff9f8f98d1f84b6f3e4554`

```dockerfile
```

-	Layers:
	-	`sha256:f69d02f14b4812898412ac294dc0dab2dc56794622e5884f95b2fe6f8b20fe21`  
		Last Modified: Fri, 20 Feb 2026 18:57:47 GMT  
		Size: 25.4 KB (25437 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.11.9` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:faa91d8bbe9c6ee8a82e563814793675d2ea507ef7f914ff2d9cfe3017e5cbe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218828329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2674f9a6e613b8267a7724d7526fe16e149dddcadee9d13456dc5562def3e43`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Fri, 20 Feb 2026 18:56:06 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Feb 2026 18:56:06 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Feb 2026 18:56:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Feb 2026 18:56:06 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Feb 2026 18:56:06 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Feb 2026 18:56:06 GMT
ARG VERSION=25.11.9.34
# Fri, 20 Feb 2026 18:56:06 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Feb 2026 18:57:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.9.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:57:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.9.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:57:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.9.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Feb 2026 18:57:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Feb 2026 18:57:32 GMT
ENV TZ=UTC
# Fri, 20 Feb 2026 18:57:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.9.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Feb 2026 18:57:32 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Feb 2026 18:57:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Feb 2026 18:57:32 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Feb 2026 18:57:32 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Feb 2026 18:57:32 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Feb 2026 18:57:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ddda68ab08dc984109a23de1a2466e333e45ed21633b824db1aa90595410ffd`  
		Last Modified: Fri, 20 Feb 2026 18:56:55 GMT  
		Size: 7.6 MB (7577563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605555697f58070013657afbc8682855063097608914b0cd5f6f878ce56f1073`  
		Last Modified: Fri, 20 Feb 2026 18:57:54 GMT  
		Size: 183.0 MB (182995773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4c95f52ffca5931405dcd68e38964d959dd72a0517252cfdb5aa369507c045`  
		Last Modified: Fri, 20 Feb 2026 18:57:50 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c3f60ff0b369d9319ab243cff5f1d988786c4ce5d69d3bb1c12353485d1b01`  
		Last Modified: Fri, 20 Feb 2026 18:57:50 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881cf1ccccbc524eea8008eb0b3b571fae69e2817d5730543bf7462af5218bd9`  
		Last Modified: Fri, 20 Feb 2026 18:57:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eda7848198b505e460c8e7335033d7a91b2949b1bdb3a03ec63cefbfb5815c7`  
		Last Modified: Fri, 20 Feb 2026 18:57:52 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92f82468ac7ae3788a577ef56dc4a961a9e5c27df04c5508fea7418b53f99f3`  
		Last Modified: Fri, 20 Feb 2026 18:57:52 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.9` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f91dc84ef4afd318ab2cf4b3ec55120d0f6e0048411820e4be4eeb819d3c269e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5a07dc724e6c7659a584b08655abb9ff7edacc7532e8a3952dc86e7652a7aa`

```dockerfile
```

-	Layers:
	-	`sha256:699ab0680de175f089dc279f322f8d199708e3d9fa5896fd93fbcfbec2a2c47b`  
		Last Modified: Fri, 20 Feb 2026 18:57:50 GMT  
		Size: 25.6 KB (25625 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.11.9-jammy`

```console
$ docker pull clickhouse@sha256:d0f71dc3b05893b2377fb33c82fa435e865e93865f4f6ca40ef2c2ae1106883f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.11.9-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:69cde8aacd11527a6c1e8a311a30389fe0a78fe79d1b01c947ba8bf2bb2863b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233937404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d0dec1a3e9e01d5a665954d92ffe8378028ae544a487799dfeb88d21175b302`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 20 Feb 2026 18:56:02 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Feb 2026 18:56:02 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Feb 2026 18:56:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Feb 2026 18:56:02 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Feb 2026 18:56:02 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Feb 2026 18:56:02 GMT
ARG VERSION=25.11.9.34
# Fri, 20 Feb 2026 18:56:02 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Feb 2026 18:57:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.9.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:57:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.9.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:57:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.9.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Feb 2026 18:57:28 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Feb 2026 18:57:28 GMT
ENV TZ=UTC
# Fri, 20 Feb 2026 18:57:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.9.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Feb 2026 18:57:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Feb 2026 18:57:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Feb 2026 18:57:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Feb 2026 18:57:28 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Feb 2026 18:57:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Feb 2026 18:57:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6264629b10e9e86b9f3a55076a22cf04acd714130d22ca018783540fae2cea54`  
		Last Modified: Fri, 20 Feb 2026 18:56:49 GMT  
		Size: 7.6 MB (7598309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfc285133e340947ee6e7438899068df5a2213a33acca1231ab92df4ed6df43`  
		Last Modified: Fri, 20 Feb 2026 18:57:52 GMT  
		Size: 195.9 MB (195931680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c95762452ce9ec719051e189c2a20ae2875deb609402d47541fbc56ca79fb71`  
		Last Modified: Fri, 20 Feb 2026 18:57:47 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f77838964c13a3627be462112daf496650eb819e88148f87cb8ee6a211c7de34`  
		Last Modified: Fri, 20 Feb 2026 18:57:47 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12314fc3b24f761f8d8fbe8104e4b6fc14feba2e569ab51de0fc799dda5e99c8`  
		Last Modified: Fri, 20 Feb 2026 18:57:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ae543998e7cada9d1e88c4ce546c35e69e7afb1ce8bda93337822ecce32853`  
		Last Modified: Fri, 20 Feb 2026 18:57:48 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec38330e61a43af4b323386cb8f66622cfc795d055a9fcb45925703fb0ee499`  
		Last Modified: Fri, 20 Feb 2026 18:57:48 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.9-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:410e5c77fcc35e9ced63de34cf69c008eb7c6d4772dcb92b6f6dd1f63cadcbbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2795aa4e3861cc85b22aeb3ee1cd8a06157dab720ff9f8f98d1f84b6f3e4554`

```dockerfile
```

-	Layers:
	-	`sha256:f69d02f14b4812898412ac294dc0dab2dc56794622e5884f95b2fe6f8b20fe21`  
		Last Modified: Fri, 20 Feb 2026 18:57:47 GMT  
		Size: 25.4 KB (25437 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.11.9-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:faa91d8bbe9c6ee8a82e563814793675d2ea507ef7f914ff2d9cfe3017e5cbe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218828329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2674f9a6e613b8267a7724d7526fe16e149dddcadee9d13456dc5562def3e43`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Fri, 20 Feb 2026 18:56:06 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Feb 2026 18:56:06 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Feb 2026 18:56:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Feb 2026 18:56:06 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Feb 2026 18:56:06 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Feb 2026 18:56:06 GMT
ARG VERSION=25.11.9.34
# Fri, 20 Feb 2026 18:56:06 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Feb 2026 18:57:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.9.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:57:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.9.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:57:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.9.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Feb 2026 18:57:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Feb 2026 18:57:32 GMT
ENV TZ=UTC
# Fri, 20 Feb 2026 18:57:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.9.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Feb 2026 18:57:32 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Feb 2026 18:57:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Feb 2026 18:57:32 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Feb 2026 18:57:32 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Feb 2026 18:57:32 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Feb 2026 18:57:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ddda68ab08dc984109a23de1a2466e333e45ed21633b824db1aa90595410ffd`  
		Last Modified: Fri, 20 Feb 2026 18:56:55 GMT  
		Size: 7.6 MB (7577563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605555697f58070013657afbc8682855063097608914b0cd5f6f878ce56f1073`  
		Last Modified: Fri, 20 Feb 2026 18:57:54 GMT  
		Size: 183.0 MB (182995773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4c95f52ffca5931405dcd68e38964d959dd72a0517252cfdb5aa369507c045`  
		Last Modified: Fri, 20 Feb 2026 18:57:50 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c3f60ff0b369d9319ab243cff5f1d988786c4ce5d69d3bb1c12353485d1b01`  
		Last Modified: Fri, 20 Feb 2026 18:57:50 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881cf1ccccbc524eea8008eb0b3b571fae69e2817d5730543bf7462af5218bd9`  
		Last Modified: Fri, 20 Feb 2026 18:57:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eda7848198b505e460c8e7335033d7a91b2949b1bdb3a03ec63cefbfb5815c7`  
		Last Modified: Fri, 20 Feb 2026 18:57:52 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92f82468ac7ae3788a577ef56dc4a961a9e5c27df04c5508fea7418b53f99f3`  
		Last Modified: Fri, 20 Feb 2026 18:57:52 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.9-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f91dc84ef4afd318ab2cf4b3ec55120d0f6e0048411820e4be4eeb819d3c269e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5a07dc724e6c7659a584b08655abb9ff7edacc7532e8a3952dc86e7652a7aa`

```dockerfile
```

-	Layers:
	-	`sha256:699ab0680de175f089dc279f322f8d199708e3d9fa5896fd93fbcfbec2a2c47b`  
		Last Modified: Fri, 20 Feb 2026 18:57:50 GMT  
		Size: 25.6 KB (25625 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.11.9.34`

```console
$ docker pull clickhouse@sha256:d0f71dc3b05893b2377fb33c82fa435e865e93865f4f6ca40ef2c2ae1106883f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.11.9.34` - linux; amd64

```console
$ docker pull clickhouse@sha256:69cde8aacd11527a6c1e8a311a30389fe0a78fe79d1b01c947ba8bf2bb2863b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233937404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d0dec1a3e9e01d5a665954d92ffe8378028ae544a487799dfeb88d21175b302`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 20 Feb 2026 18:56:02 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Feb 2026 18:56:02 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Feb 2026 18:56:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Feb 2026 18:56:02 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Feb 2026 18:56:02 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Feb 2026 18:56:02 GMT
ARG VERSION=25.11.9.34
# Fri, 20 Feb 2026 18:56:02 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Feb 2026 18:57:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.9.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:57:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.9.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:57:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.9.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Feb 2026 18:57:28 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Feb 2026 18:57:28 GMT
ENV TZ=UTC
# Fri, 20 Feb 2026 18:57:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.9.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Feb 2026 18:57:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Feb 2026 18:57:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Feb 2026 18:57:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Feb 2026 18:57:28 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Feb 2026 18:57:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Feb 2026 18:57:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6264629b10e9e86b9f3a55076a22cf04acd714130d22ca018783540fae2cea54`  
		Last Modified: Fri, 20 Feb 2026 18:56:49 GMT  
		Size: 7.6 MB (7598309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfc285133e340947ee6e7438899068df5a2213a33acca1231ab92df4ed6df43`  
		Last Modified: Fri, 20 Feb 2026 18:57:52 GMT  
		Size: 195.9 MB (195931680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c95762452ce9ec719051e189c2a20ae2875deb609402d47541fbc56ca79fb71`  
		Last Modified: Fri, 20 Feb 2026 18:57:47 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f77838964c13a3627be462112daf496650eb819e88148f87cb8ee6a211c7de34`  
		Last Modified: Fri, 20 Feb 2026 18:57:47 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12314fc3b24f761f8d8fbe8104e4b6fc14feba2e569ab51de0fc799dda5e99c8`  
		Last Modified: Fri, 20 Feb 2026 18:57:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ae543998e7cada9d1e88c4ce546c35e69e7afb1ce8bda93337822ecce32853`  
		Last Modified: Fri, 20 Feb 2026 18:57:48 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec38330e61a43af4b323386cb8f66622cfc795d055a9fcb45925703fb0ee499`  
		Last Modified: Fri, 20 Feb 2026 18:57:48 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.9.34` - unknown; unknown

```console
$ docker pull clickhouse@sha256:410e5c77fcc35e9ced63de34cf69c008eb7c6d4772dcb92b6f6dd1f63cadcbbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2795aa4e3861cc85b22aeb3ee1cd8a06157dab720ff9f8f98d1f84b6f3e4554`

```dockerfile
```

-	Layers:
	-	`sha256:f69d02f14b4812898412ac294dc0dab2dc56794622e5884f95b2fe6f8b20fe21`  
		Last Modified: Fri, 20 Feb 2026 18:57:47 GMT  
		Size: 25.4 KB (25437 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.11.9.34` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:faa91d8bbe9c6ee8a82e563814793675d2ea507ef7f914ff2d9cfe3017e5cbe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218828329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2674f9a6e613b8267a7724d7526fe16e149dddcadee9d13456dc5562def3e43`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Fri, 20 Feb 2026 18:56:06 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Feb 2026 18:56:06 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Feb 2026 18:56:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Feb 2026 18:56:06 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Feb 2026 18:56:06 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Feb 2026 18:56:06 GMT
ARG VERSION=25.11.9.34
# Fri, 20 Feb 2026 18:56:06 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Feb 2026 18:57:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.9.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:57:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.9.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:57:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.9.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Feb 2026 18:57:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Feb 2026 18:57:32 GMT
ENV TZ=UTC
# Fri, 20 Feb 2026 18:57:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.9.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Feb 2026 18:57:32 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Feb 2026 18:57:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Feb 2026 18:57:32 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Feb 2026 18:57:32 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Feb 2026 18:57:32 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Feb 2026 18:57:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ddda68ab08dc984109a23de1a2466e333e45ed21633b824db1aa90595410ffd`  
		Last Modified: Fri, 20 Feb 2026 18:56:55 GMT  
		Size: 7.6 MB (7577563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605555697f58070013657afbc8682855063097608914b0cd5f6f878ce56f1073`  
		Last Modified: Fri, 20 Feb 2026 18:57:54 GMT  
		Size: 183.0 MB (182995773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4c95f52ffca5931405dcd68e38964d959dd72a0517252cfdb5aa369507c045`  
		Last Modified: Fri, 20 Feb 2026 18:57:50 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c3f60ff0b369d9319ab243cff5f1d988786c4ce5d69d3bb1c12353485d1b01`  
		Last Modified: Fri, 20 Feb 2026 18:57:50 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881cf1ccccbc524eea8008eb0b3b571fae69e2817d5730543bf7462af5218bd9`  
		Last Modified: Fri, 20 Feb 2026 18:57:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eda7848198b505e460c8e7335033d7a91b2949b1bdb3a03ec63cefbfb5815c7`  
		Last Modified: Fri, 20 Feb 2026 18:57:52 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92f82468ac7ae3788a577ef56dc4a961a9e5c27df04c5508fea7418b53f99f3`  
		Last Modified: Fri, 20 Feb 2026 18:57:52 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.9.34` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f91dc84ef4afd318ab2cf4b3ec55120d0f6e0048411820e4be4eeb819d3c269e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5a07dc724e6c7659a584b08655abb9ff7edacc7532e8a3952dc86e7652a7aa`

```dockerfile
```

-	Layers:
	-	`sha256:699ab0680de175f089dc279f322f8d199708e3d9fa5896fd93fbcfbec2a2c47b`  
		Last Modified: Fri, 20 Feb 2026 18:57:50 GMT  
		Size: 25.6 KB (25625 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.11.9.34-jammy`

```console
$ docker pull clickhouse@sha256:d0f71dc3b05893b2377fb33c82fa435e865e93865f4f6ca40ef2c2ae1106883f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.11.9.34-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:69cde8aacd11527a6c1e8a311a30389fe0a78fe79d1b01c947ba8bf2bb2863b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233937404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d0dec1a3e9e01d5a665954d92ffe8378028ae544a487799dfeb88d21175b302`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 20 Feb 2026 18:56:02 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Feb 2026 18:56:02 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Feb 2026 18:56:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Feb 2026 18:56:02 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Feb 2026 18:56:02 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Feb 2026 18:56:02 GMT
ARG VERSION=25.11.9.34
# Fri, 20 Feb 2026 18:56:02 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Feb 2026 18:57:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.9.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:57:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.9.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:57:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.9.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Feb 2026 18:57:28 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Feb 2026 18:57:28 GMT
ENV TZ=UTC
# Fri, 20 Feb 2026 18:57:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.9.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Feb 2026 18:57:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Feb 2026 18:57:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Feb 2026 18:57:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Feb 2026 18:57:28 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Feb 2026 18:57:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Feb 2026 18:57:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6264629b10e9e86b9f3a55076a22cf04acd714130d22ca018783540fae2cea54`  
		Last Modified: Fri, 20 Feb 2026 18:56:49 GMT  
		Size: 7.6 MB (7598309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfc285133e340947ee6e7438899068df5a2213a33acca1231ab92df4ed6df43`  
		Last Modified: Fri, 20 Feb 2026 18:57:52 GMT  
		Size: 195.9 MB (195931680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c95762452ce9ec719051e189c2a20ae2875deb609402d47541fbc56ca79fb71`  
		Last Modified: Fri, 20 Feb 2026 18:57:47 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f77838964c13a3627be462112daf496650eb819e88148f87cb8ee6a211c7de34`  
		Last Modified: Fri, 20 Feb 2026 18:57:47 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12314fc3b24f761f8d8fbe8104e4b6fc14feba2e569ab51de0fc799dda5e99c8`  
		Last Modified: Fri, 20 Feb 2026 18:57:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ae543998e7cada9d1e88c4ce546c35e69e7afb1ce8bda93337822ecce32853`  
		Last Modified: Fri, 20 Feb 2026 18:57:48 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec38330e61a43af4b323386cb8f66622cfc795d055a9fcb45925703fb0ee499`  
		Last Modified: Fri, 20 Feb 2026 18:57:48 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.9.34-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:410e5c77fcc35e9ced63de34cf69c008eb7c6d4772dcb92b6f6dd1f63cadcbbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2795aa4e3861cc85b22aeb3ee1cd8a06157dab720ff9f8f98d1f84b6f3e4554`

```dockerfile
```

-	Layers:
	-	`sha256:f69d02f14b4812898412ac294dc0dab2dc56794622e5884f95b2fe6f8b20fe21`  
		Last Modified: Fri, 20 Feb 2026 18:57:47 GMT  
		Size: 25.4 KB (25437 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.11.9.34-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:faa91d8bbe9c6ee8a82e563814793675d2ea507ef7f914ff2d9cfe3017e5cbe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218828329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2674f9a6e613b8267a7724d7526fe16e149dddcadee9d13456dc5562def3e43`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Fri, 20 Feb 2026 18:56:06 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Feb 2026 18:56:06 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Feb 2026 18:56:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Feb 2026 18:56:06 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Feb 2026 18:56:06 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Feb 2026 18:56:06 GMT
ARG VERSION=25.11.9.34
# Fri, 20 Feb 2026 18:56:06 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Feb 2026 18:57:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.9.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:57:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.9.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:57:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.9.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Feb 2026 18:57:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Feb 2026 18:57:32 GMT
ENV TZ=UTC
# Fri, 20 Feb 2026 18:57:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.9.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Feb 2026 18:57:32 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Feb 2026 18:57:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Feb 2026 18:57:32 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Feb 2026 18:57:32 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Feb 2026 18:57:32 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Feb 2026 18:57:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ddda68ab08dc984109a23de1a2466e333e45ed21633b824db1aa90595410ffd`  
		Last Modified: Fri, 20 Feb 2026 18:56:55 GMT  
		Size: 7.6 MB (7577563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605555697f58070013657afbc8682855063097608914b0cd5f6f878ce56f1073`  
		Last Modified: Fri, 20 Feb 2026 18:57:54 GMT  
		Size: 183.0 MB (182995773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4c95f52ffca5931405dcd68e38964d959dd72a0517252cfdb5aa369507c045`  
		Last Modified: Fri, 20 Feb 2026 18:57:50 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c3f60ff0b369d9319ab243cff5f1d988786c4ce5d69d3bb1c12353485d1b01`  
		Last Modified: Fri, 20 Feb 2026 18:57:50 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881cf1ccccbc524eea8008eb0b3b571fae69e2817d5730543bf7462af5218bd9`  
		Last Modified: Fri, 20 Feb 2026 18:57:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eda7848198b505e460c8e7335033d7a91b2949b1bdb3a03ec63cefbfb5815c7`  
		Last Modified: Fri, 20 Feb 2026 18:57:52 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92f82468ac7ae3788a577ef56dc4a961a9e5c27df04c5508fea7418b53f99f3`  
		Last Modified: Fri, 20 Feb 2026 18:57:52 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.9.34-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f91dc84ef4afd318ab2cf4b3ec55120d0f6e0048411820e4be4eeb819d3c269e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5a07dc724e6c7659a584b08655abb9ff7edacc7532e8a3952dc86e7652a7aa`

```dockerfile
```

-	Layers:
	-	`sha256:699ab0680de175f089dc279f322f8d199708e3d9fa5896fd93fbcfbec2a2c47b`  
		Last Modified: Fri, 20 Feb 2026 18:57:50 GMT  
		Size: 25.6 KB (25625 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.12`

```console
$ docker pull clickhouse@sha256:3774ff0f86beed192c067cd4dfa0f8591b1fd1a0b079082d512b7a166d6da5f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.12` - linux; amd64

```console
$ docker pull clickhouse@sha256:a0d96b2e9ce670d08ba8cc5f96bc45b8ccf56f521cd4e4d358d6ed9c0646ddc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246380284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74c146e38cf8a2fedb558cbb7476beec57300c9b2493e4ea4d18d95b786c11e4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 27 Feb 2026 22:27:55 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Feb 2026 22:27:55 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Feb 2026 22:27:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Feb 2026 22:27:55 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Feb 2026 22:27:55 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Feb 2026 22:27:55 GMT
ARG VERSION=25.12.7.21
# Fri, 27 Feb 2026 22:27:55 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Feb 2026 22:28:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.7.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Feb 2026 22:28:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.7.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Feb 2026 22:28:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.7.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Feb 2026 22:28:24 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Feb 2026 22:28:24 GMT
ENV TZ=UTC
# Fri, 27 Feb 2026 22:28:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.7.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Feb 2026 22:28:24 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Feb 2026 22:28:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Feb 2026 22:28:24 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Feb 2026 22:28:24 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Feb 2026 22:28:24 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Feb 2026 22:28:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8d099a96f70c076e1819201823630e441353c18bac1712345ab10eaa53c511`  
		Last Modified: Fri, 27 Feb 2026 22:28:50 GMT  
		Size: 7.6 MB (7598279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3dcbb76724f8f371a704e52113438bc40a6a0b9218c167ea4f0b8011189ed7`  
		Last Modified: Fri, 27 Feb 2026 22:28:54 GMT  
		Size: 208.4 MB (208374593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0545996ff9a927792111c49ce0e364252e2a09a52bb7968fd9e91253f1d601b`  
		Last Modified: Fri, 27 Feb 2026 22:28:50 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48b98ba68effe2b8ac999a5b8c9983069ea15fe925f6a0b9507099012530a81`  
		Last Modified: Fri, 27 Feb 2026 22:28:50 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b40507c558d02b06dbaae72c3c245992bda893a2b52bed0c55e5a19068bc15`  
		Last Modified: Fri, 27 Feb 2026 22:28:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf86ef885f1a57ec1e0aef70ab02355bd93897c099c39f9374c9df3337bd70ec`  
		Last Modified: Fri, 27 Feb 2026 22:28:51 GMT  
		Size: 358.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f239b1782b3ada59abf21104ab16ac616db4e2d64c53f8c3a8e5bc973e51dd`  
		Last Modified: Fri, 27 Feb 2026 22:28:52 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12` - unknown; unknown

```console
$ docker pull clickhouse@sha256:7e0d4fe993baca231998568186a262c3700f7f61bd51917e2a10c7794748867f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9539f192849f3ed422254283c0af6d0a2e9e0bc1847af10222fb17933c9654fc`

```dockerfile
```

-	Layers:
	-	`sha256:564966241615df78ff9d69b6157cc3f77af6dbbd69d3c294f7ee550c53bf0e3f`  
		Last Modified: Fri, 27 Feb 2026 22:28:50 GMT  
		Size: 25.4 KB (25436 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.12` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:cb916bcab99e2d63529b72b111d6d98b1e0e599f6b91921962dd32c1279e5e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228297479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6510ecd4564970437239226b557dba010fe2295c8ad99d031062cb3c4b50ad9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Fri, 27 Feb 2026 22:27:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Feb 2026 22:27:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Feb 2026 22:27:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Feb 2026 22:27:47 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Feb 2026 22:27:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Feb 2026 22:27:47 GMT
ARG VERSION=25.12.7.21
# Fri, 27 Feb 2026 22:27:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Feb 2026 22:28:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.7.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Feb 2026 22:28:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.7.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Feb 2026 22:28:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.7.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Feb 2026 22:28:17 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Feb 2026 22:28:17 GMT
ENV TZ=UTC
# Fri, 27 Feb 2026 22:28:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.7.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Feb 2026 22:28:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Feb 2026 22:28:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Feb 2026 22:28:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Feb 2026 22:28:17 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Feb 2026 22:28:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Feb 2026 22:28:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427265c7591907f60845f56adb5eb4dcd95f4be72e147ac7e960c8620bf4c84a`  
		Last Modified: Fri, 27 Feb 2026 22:28:40 GMT  
		Size: 7.6 MB (7577541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4560112e45d4357e88f9079d4da2f4a7f0091df3e41bbba7a68a708ca997d60`  
		Last Modified: Fri, 27 Feb 2026 22:28:43 GMT  
		Size: 192.5 MB (192464944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ea07032172a5db2a3c535157a269657bf91e016cd8ab9ffa4bbb938df06b37`  
		Last Modified: Fri, 27 Feb 2026 22:28:39 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9db8a1e198cfa2ab5153c13e6e0734d80407590b55f7ff03bf1e58690c3716`  
		Last Modified: Fri, 27 Feb 2026 22:28:39 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f72c6c37aca5cfc02307ca8b711e52b305feddc6589c24e3b49f8b58dc3b051`  
		Last Modified: Fri, 27 Feb 2026 22:28:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669821d7b0c1fdac2b4180a3a2b902a673c5013e5745d560306616119d53b2bd`  
		Last Modified: Fri, 27 Feb 2026 22:28:40 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891d2ce3f0310233a911c9f03e78097e849d5139a0a1c1a3ee328b6c7f09be1a`  
		Last Modified: Fri, 27 Feb 2026 22:28:41 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12` - unknown; unknown

```console
$ docker pull clickhouse@sha256:56054686c14d094737185f35d132bb7c8c7b110d8c2442b58ef071f6ff46a59c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10ad18e978faa91bbab35b8c146313ab77b4128d0d2efcd0955d75c0c9b12eb8`

```dockerfile
```

-	Layers:
	-	`sha256:4a42811e1eaee96429cd262b4b5726c56f02fc721a2f51fb08b61739db30b59b`  
		Last Modified: Fri, 27 Feb 2026 22:28:39 GMT  
		Size: 25.6 KB (25625 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.12-jammy`

```console
$ docker pull clickhouse@sha256:3774ff0f86beed192c067cd4dfa0f8591b1fd1a0b079082d512b7a166d6da5f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.12-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:a0d96b2e9ce670d08ba8cc5f96bc45b8ccf56f521cd4e4d358d6ed9c0646ddc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246380284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74c146e38cf8a2fedb558cbb7476beec57300c9b2493e4ea4d18d95b786c11e4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 27 Feb 2026 22:27:55 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Feb 2026 22:27:55 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Feb 2026 22:27:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Feb 2026 22:27:55 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Feb 2026 22:27:55 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Feb 2026 22:27:55 GMT
ARG VERSION=25.12.7.21
# Fri, 27 Feb 2026 22:27:55 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Feb 2026 22:28:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.7.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Feb 2026 22:28:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.7.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Feb 2026 22:28:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.7.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Feb 2026 22:28:24 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Feb 2026 22:28:24 GMT
ENV TZ=UTC
# Fri, 27 Feb 2026 22:28:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.7.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Feb 2026 22:28:24 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Feb 2026 22:28:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Feb 2026 22:28:24 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Feb 2026 22:28:24 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Feb 2026 22:28:24 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Feb 2026 22:28:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8d099a96f70c076e1819201823630e441353c18bac1712345ab10eaa53c511`  
		Last Modified: Fri, 27 Feb 2026 22:28:50 GMT  
		Size: 7.6 MB (7598279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3dcbb76724f8f371a704e52113438bc40a6a0b9218c167ea4f0b8011189ed7`  
		Last Modified: Fri, 27 Feb 2026 22:28:54 GMT  
		Size: 208.4 MB (208374593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0545996ff9a927792111c49ce0e364252e2a09a52bb7968fd9e91253f1d601b`  
		Last Modified: Fri, 27 Feb 2026 22:28:50 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48b98ba68effe2b8ac999a5b8c9983069ea15fe925f6a0b9507099012530a81`  
		Last Modified: Fri, 27 Feb 2026 22:28:50 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b40507c558d02b06dbaae72c3c245992bda893a2b52bed0c55e5a19068bc15`  
		Last Modified: Fri, 27 Feb 2026 22:28:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf86ef885f1a57ec1e0aef70ab02355bd93897c099c39f9374c9df3337bd70ec`  
		Last Modified: Fri, 27 Feb 2026 22:28:51 GMT  
		Size: 358.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f239b1782b3ada59abf21104ab16ac616db4e2d64c53f8c3a8e5bc973e51dd`  
		Last Modified: Fri, 27 Feb 2026 22:28:52 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:7e0d4fe993baca231998568186a262c3700f7f61bd51917e2a10c7794748867f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9539f192849f3ed422254283c0af6d0a2e9e0bc1847af10222fb17933c9654fc`

```dockerfile
```

-	Layers:
	-	`sha256:564966241615df78ff9d69b6157cc3f77af6dbbd69d3c294f7ee550c53bf0e3f`  
		Last Modified: Fri, 27 Feb 2026 22:28:50 GMT  
		Size: 25.4 KB (25436 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.12-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:cb916bcab99e2d63529b72b111d6d98b1e0e599f6b91921962dd32c1279e5e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228297479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6510ecd4564970437239226b557dba010fe2295c8ad99d031062cb3c4b50ad9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Fri, 27 Feb 2026 22:27:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Feb 2026 22:27:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Feb 2026 22:27:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Feb 2026 22:27:47 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Feb 2026 22:27:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Feb 2026 22:27:47 GMT
ARG VERSION=25.12.7.21
# Fri, 27 Feb 2026 22:27:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Feb 2026 22:28:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.7.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Feb 2026 22:28:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.7.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Feb 2026 22:28:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.7.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Feb 2026 22:28:17 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Feb 2026 22:28:17 GMT
ENV TZ=UTC
# Fri, 27 Feb 2026 22:28:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.7.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Feb 2026 22:28:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Feb 2026 22:28:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Feb 2026 22:28:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Feb 2026 22:28:17 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Feb 2026 22:28:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Feb 2026 22:28:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427265c7591907f60845f56adb5eb4dcd95f4be72e147ac7e960c8620bf4c84a`  
		Last Modified: Fri, 27 Feb 2026 22:28:40 GMT  
		Size: 7.6 MB (7577541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4560112e45d4357e88f9079d4da2f4a7f0091df3e41bbba7a68a708ca997d60`  
		Last Modified: Fri, 27 Feb 2026 22:28:43 GMT  
		Size: 192.5 MB (192464944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ea07032172a5db2a3c535157a269657bf91e016cd8ab9ffa4bbb938df06b37`  
		Last Modified: Fri, 27 Feb 2026 22:28:39 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9db8a1e198cfa2ab5153c13e6e0734d80407590b55f7ff03bf1e58690c3716`  
		Last Modified: Fri, 27 Feb 2026 22:28:39 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f72c6c37aca5cfc02307ca8b711e52b305feddc6589c24e3b49f8b58dc3b051`  
		Last Modified: Fri, 27 Feb 2026 22:28:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669821d7b0c1fdac2b4180a3a2b902a673c5013e5745d560306616119d53b2bd`  
		Last Modified: Fri, 27 Feb 2026 22:28:40 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891d2ce3f0310233a911c9f03e78097e849d5139a0a1c1a3ee328b6c7f09be1a`  
		Last Modified: Fri, 27 Feb 2026 22:28:41 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:56054686c14d094737185f35d132bb7c8c7b110d8c2442b58ef071f6ff46a59c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10ad18e978faa91bbab35b8c146313ab77b4128d0d2efcd0955d75c0c9b12eb8`

```dockerfile
```

-	Layers:
	-	`sha256:4a42811e1eaee96429cd262b4b5726c56f02fc721a2f51fb08b61739db30b59b`  
		Last Modified: Fri, 27 Feb 2026 22:28:39 GMT  
		Size: 25.6 KB (25625 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.12.7`

```console
$ docker pull clickhouse@sha256:3774ff0f86beed192c067cd4dfa0f8591b1fd1a0b079082d512b7a166d6da5f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.12.7` - linux; amd64

```console
$ docker pull clickhouse@sha256:a0d96b2e9ce670d08ba8cc5f96bc45b8ccf56f521cd4e4d358d6ed9c0646ddc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246380284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74c146e38cf8a2fedb558cbb7476beec57300c9b2493e4ea4d18d95b786c11e4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 27 Feb 2026 22:27:55 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Feb 2026 22:27:55 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Feb 2026 22:27:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Feb 2026 22:27:55 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Feb 2026 22:27:55 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Feb 2026 22:27:55 GMT
ARG VERSION=25.12.7.21
# Fri, 27 Feb 2026 22:27:55 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Feb 2026 22:28:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.7.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Feb 2026 22:28:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.7.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Feb 2026 22:28:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.7.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Feb 2026 22:28:24 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Feb 2026 22:28:24 GMT
ENV TZ=UTC
# Fri, 27 Feb 2026 22:28:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.7.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Feb 2026 22:28:24 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Feb 2026 22:28:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Feb 2026 22:28:24 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Feb 2026 22:28:24 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Feb 2026 22:28:24 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Feb 2026 22:28:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8d099a96f70c076e1819201823630e441353c18bac1712345ab10eaa53c511`  
		Last Modified: Fri, 27 Feb 2026 22:28:50 GMT  
		Size: 7.6 MB (7598279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3dcbb76724f8f371a704e52113438bc40a6a0b9218c167ea4f0b8011189ed7`  
		Last Modified: Fri, 27 Feb 2026 22:28:54 GMT  
		Size: 208.4 MB (208374593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0545996ff9a927792111c49ce0e364252e2a09a52bb7968fd9e91253f1d601b`  
		Last Modified: Fri, 27 Feb 2026 22:28:50 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48b98ba68effe2b8ac999a5b8c9983069ea15fe925f6a0b9507099012530a81`  
		Last Modified: Fri, 27 Feb 2026 22:28:50 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b40507c558d02b06dbaae72c3c245992bda893a2b52bed0c55e5a19068bc15`  
		Last Modified: Fri, 27 Feb 2026 22:28:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf86ef885f1a57ec1e0aef70ab02355bd93897c099c39f9374c9df3337bd70ec`  
		Last Modified: Fri, 27 Feb 2026 22:28:51 GMT  
		Size: 358.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f239b1782b3ada59abf21104ab16ac616db4e2d64c53f8c3a8e5bc973e51dd`  
		Last Modified: Fri, 27 Feb 2026 22:28:52 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:7e0d4fe993baca231998568186a262c3700f7f61bd51917e2a10c7794748867f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9539f192849f3ed422254283c0af6d0a2e9e0bc1847af10222fb17933c9654fc`

```dockerfile
```

-	Layers:
	-	`sha256:564966241615df78ff9d69b6157cc3f77af6dbbd69d3c294f7ee550c53bf0e3f`  
		Last Modified: Fri, 27 Feb 2026 22:28:50 GMT  
		Size: 25.4 KB (25436 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.12.7` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:cb916bcab99e2d63529b72b111d6d98b1e0e599f6b91921962dd32c1279e5e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228297479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6510ecd4564970437239226b557dba010fe2295c8ad99d031062cb3c4b50ad9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Fri, 27 Feb 2026 22:27:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Feb 2026 22:27:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Feb 2026 22:27:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Feb 2026 22:27:47 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Feb 2026 22:27:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Feb 2026 22:27:47 GMT
ARG VERSION=25.12.7.21
# Fri, 27 Feb 2026 22:27:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Feb 2026 22:28:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.7.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Feb 2026 22:28:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.7.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Feb 2026 22:28:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.7.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Feb 2026 22:28:17 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Feb 2026 22:28:17 GMT
ENV TZ=UTC
# Fri, 27 Feb 2026 22:28:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.7.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Feb 2026 22:28:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Feb 2026 22:28:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Feb 2026 22:28:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Feb 2026 22:28:17 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Feb 2026 22:28:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Feb 2026 22:28:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427265c7591907f60845f56adb5eb4dcd95f4be72e147ac7e960c8620bf4c84a`  
		Last Modified: Fri, 27 Feb 2026 22:28:40 GMT  
		Size: 7.6 MB (7577541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4560112e45d4357e88f9079d4da2f4a7f0091df3e41bbba7a68a708ca997d60`  
		Last Modified: Fri, 27 Feb 2026 22:28:43 GMT  
		Size: 192.5 MB (192464944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ea07032172a5db2a3c535157a269657bf91e016cd8ab9ffa4bbb938df06b37`  
		Last Modified: Fri, 27 Feb 2026 22:28:39 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9db8a1e198cfa2ab5153c13e6e0734d80407590b55f7ff03bf1e58690c3716`  
		Last Modified: Fri, 27 Feb 2026 22:28:39 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f72c6c37aca5cfc02307ca8b711e52b305feddc6589c24e3b49f8b58dc3b051`  
		Last Modified: Fri, 27 Feb 2026 22:28:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669821d7b0c1fdac2b4180a3a2b902a673c5013e5745d560306616119d53b2bd`  
		Last Modified: Fri, 27 Feb 2026 22:28:40 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891d2ce3f0310233a911c9f03e78097e849d5139a0a1c1a3ee328b6c7f09be1a`  
		Last Modified: Fri, 27 Feb 2026 22:28:41 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:56054686c14d094737185f35d132bb7c8c7b110d8c2442b58ef071f6ff46a59c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10ad18e978faa91bbab35b8c146313ab77b4128d0d2efcd0955d75c0c9b12eb8`

```dockerfile
```

-	Layers:
	-	`sha256:4a42811e1eaee96429cd262b4b5726c56f02fc721a2f51fb08b61739db30b59b`  
		Last Modified: Fri, 27 Feb 2026 22:28:39 GMT  
		Size: 25.6 KB (25625 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.12.7-jammy`

```console
$ docker pull clickhouse@sha256:3774ff0f86beed192c067cd4dfa0f8591b1fd1a0b079082d512b7a166d6da5f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.12.7-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:a0d96b2e9ce670d08ba8cc5f96bc45b8ccf56f521cd4e4d358d6ed9c0646ddc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246380284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74c146e38cf8a2fedb558cbb7476beec57300c9b2493e4ea4d18d95b786c11e4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 27 Feb 2026 22:27:55 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Feb 2026 22:27:55 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Feb 2026 22:27:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Feb 2026 22:27:55 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Feb 2026 22:27:55 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Feb 2026 22:27:55 GMT
ARG VERSION=25.12.7.21
# Fri, 27 Feb 2026 22:27:55 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Feb 2026 22:28:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.7.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Feb 2026 22:28:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.7.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Feb 2026 22:28:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.7.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Feb 2026 22:28:24 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Feb 2026 22:28:24 GMT
ENV TZ=UTC
# Fri, 27 Feb 2026 22:28:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.7.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Feb 2026 22:28:24 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Feb 2026 22:28:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Feb 2026 22:28:24 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Feb 2026 22:28:24 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Feb 2026 22:28:24 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Feb 2026 22:28:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8d099a96f70c076e1819201823630e441353c18bac1712345ab10eaa53c511`  
		Last Modified: Fri, 27 Feb 2026 22:28:50 GMT  
		Size: 7.6 MB (7598279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3dcbb76724f8f371a704e52113438bc40a6a0b9218c167ea4f0b8011189ed7`  
		Last Modified: Fri, 27 Feb 2026 22:28:54 GMT  
		Size: 208.4 MB (208374593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0545996ff9a927792111c49ce0e364252e2a09a52bb7968fd9e91253f1d601b`  
		Last Modified: Fri, 27 Feb 2026 22:28:50 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48b98ba68effe2b8ac999a5b8c9983069ea15fe925f6a0b9507099012530a81`  
		Last Modified: Fri, 27 Feb 2026 22:28:50 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b40507c558d02b06dbaae72c3c245992bda893a2b52bed0c55e5a19068bc15`  
		Last Modified: Fri, 27 Feb 2026 22:28:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf86ef885f1a57ec1e0aef70ab02355bd93897c099c39f9374c9df3337bd70ec`  
		Last Modified: Fri, 27 Feb 2026 22:28:51 GMT  
		Size: 358.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f239b1782b3ada59abf21104ab16ac616db4e2d64c53f8c3a8e5bc973e51dd`  
		Last Modified: Fri, 27 Feb 2026 22:28:52 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.7-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:7e0d4fe993baca231998568186a262c3700f7f61bd51917e2a10c7794748867f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9539f192849f3ed422254283c0af6d0a2e9e0bc1847af10222fb17933c9654fc`

```dockerfile
```

-	Layers:
	-	`sha256:564966241615df78ff9d69b6157cc3f77af6dbbd69d3c294f7ee550c53bf0e3f`  
		Last Modified: Fri, 27 Feb 2026 22:28:50 GMT  
		Size: 25.4 KB (25436 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.12.7-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:cb916bcab99e2d63529b72b111d6d98b1e0e599f6b91921962dd32c1279e5e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228297479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6510ecd4564970437239226b557dba010fe2295c8ad99d031062cb3c4b50ad9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Fri, 27 Feb 2026 22:27:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Feb 2026 22:27:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Feb 2026 22:27:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Feb 2026 22:27:47 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Feb 2026 22:27:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Feb 2026 22:27:47 GMT
ARG VERSION=25.12.7.21
# Fri, 27 Feb 2026 22:27:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Feb 2026 22:28:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.7.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Feb 2026 22:28:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.7.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Feb 2026 22:28:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.7.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Feb 2026 22:28:17 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Feb 2026 22:28:17 GMT
ENV TZ=UTC
# Fri, 27 Feb 2026 22:28:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.7.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Feb 2026 22:28:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Feb 2026 22:28:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Feb 2026 22:28:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Feb 2026 22:28:17 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Feb 2026 22:28:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Feb 2026 22:28:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427265c7591907f60845f56adb5eb4dcd95f4be72e147ac7e960c8620bf4c84a`  
		Last Modified: Fri, 27 Feb 2026 22:28:40 GMT  
		Size: 7.6 MB (7577541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4560112e45d4357e88f9079d4da2f4a7f0091df3e41bbba7a68a708ca997d60`  
		Last Modified: Fri, 27 Feb 2026 22:28:43 GMT  
		Size: 192.5 MB (192464944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ea07032172a5db2a3c535157a269657bf91e016cd8ab9ffa4bbb938df06b37`  
		Last Modified: Fri, 27 Feb 2026 22:28:39 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9db8a1e198cfa2ab5153c13e6e0734d80407590b55f7ff03bf1e58690c3716`  
		Last Modified: Fri, 27 Feb 2026 22:28:39 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f72c6c37aca5cfc02307ca8b711e52b305feddc6589c24e3b49f8b58dc3b051`  
		Last Modified: Fri, 27 Feb 2026 22:28:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669821d7b0c1fdac2b4180a3a2b902a673c5013e5745d560306616119d53b2bd`  
		Last Modified: Fri, 27 Feb 2026 22:28:40 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891d2ce3f0310233a911c9f03e78097e849d5139a0a1c1a3ee328b6c7f09be1a`  
		Last Modified: Fri, 27 Feb 2026 22:28:41 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.7-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:56054686c14d094737185f35d132bb7c8c7b110d8c2442b58ef071f6ff46a59c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10ad18e978faa91bbab35b8c146313ab77b4128d0d2efcd0955d75c0c9b12eb8`

```dockerfile
```

-	Layers:
	-	`sha256:4a42811e1eaee96429cd262b4b5726c56f02fc721a2f51fb08b61739db30b59b`  
		Last Modified: Fri, 27 Feb 2026 22:28:39 GMT  
		Size: 25.6 KB (25625 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.12.7.21`

```console
$ docker pull clickhouse@sha256:3774ff0f86beed192c067cd4dfa0f8591b1fd1a0b079082d512b7a166d6da5f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.12.7.21` - linux; amd64

```console
$ docker pull clickhouse@sha256:a0d96b2e9ce670d08ba8cc5f96bc45b8ccf56f521cd4e4d358d6ed9c0646ddc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246380284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74c146e38cf8a2fedb558cbb7476beec57300c9b2493e4ea4d18d95b786c11e4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 27 Feb 2026 22:27:55 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Feb 2026 22:27:55 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Feb 2026 22:27:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Feb 2026 22:27:55 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Feb 2026 22:27:55 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Feb 2026 22:27:55 GMT
ARG VERSION=25.12.7.21
# Fri, 27 Feb 2026 22:27:55 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Feb 2026 22:28:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.7.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Feb 2026 22:28:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.7.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Feb 2026 22:28:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.7.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Feb 2026 22:28:24 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Feb 2026 22:28:24 GMT
ENV TZ=UTC
# Fri, 27 Feb 2026 22:28:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.7.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Feb 2026 22:28:24 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Feb 2026 22:28:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Feb 2026 22:28:24 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Feb 2026 22:28:24 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Feb 2026 22:28:24 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Feb 2026 22:28:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8d099a96f70c076e1819201823630e441353c18bac1712345ab10eaa53c511`  
		Last Modified: Fri, 27 Feb 2026 22:28:50 GMT  
		Size: 7.6 MB (7598279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3dcbb76724f8f371a704e52113438bc40a6a0b9218c167ea4f0b8011189ed7`  
		Last Modified: Fri, 27 Feb 2026 22:28:54 GMT  
		Size: 208.4 MB (208374593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0545996ff9a927792111c49ce0e364252e2a09a52bb7968fd9e91253f1d601b`  
		Last Modified: Fri, 27 Feb 2026 22:28:50 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48b98ba68effe2b8ac999a5b8c9983069ea15fe925f6a0b9507099012530a81`  
		Last Modified: Fri, 27 Feb 2026 22:28:50 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b40507c558d02b06dbaae72c3c245992bda893a2b52bed0c55e5a19068bc15`  
		Last Modified: Fri, 27 Feb 2026 22:28:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf86ef885f1a57ec1e0aef70ab02355bd93897c099c39f9374c9df3337bd70ec`  
		Last Modified: Fri, 27 Feb 2026 22:28:51 GMT  
		Size: 358.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f239b1782b3ada59abf21104ab16ac616db4e2d64c53f8c3a8e5bc973e51dd`  
		Last Modified: Fri, 27 Feb 2026 22:28:52 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.7.21` - unknown; unknown

```console
$ docker pull clickhouse@sha256:7e0d4fe993baca231998568186a262c3700f7f61bd51917e2a10c7794748867f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9539f192849f3ed422254283c0af6d0a2e9e0bc1847af10222fb17933c9654fc`

```dockerfile
```

-	Layers:
	-	`sha256:564966241615df78ff9d69b6157cc3f77af6dbbd69d3c294f7ee550c53bf0e3f`  
		Last Modified: Fri, 27 Feb 2026 22:28:50 GMT  
		Size: 25.4 KB (25436 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.12.7.21` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:cb916bcab99e2d63529b72b111d6d98b1e0e599f6b91921962dd32c1279e5e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228297479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6510ecd4564970437239226b557dba010fe2295c8ad99d031062cb3c4b50ad9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Fri, 27 Feb 2026 22:27:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Feb 2026 22:27:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Feb 2026 22:27:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Feb 2026 22:27:47 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Feb 2026 22:27:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Feb 2026 22:27:47 GMT
ARG VERSION=25.12.7.21
# Fri, 27 Feb 2026 22:27:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Feb 2026 22:28:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.7.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Feb 2026 22:28:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.7.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Feb 2026 22:28:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.7.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Feb 2026 22:28:17 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Feb 2026 22:28:17 GMT
ENV TZ=UTC
# Fri, 27 Feb 2026 22:28:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.7.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Feb 2026 22:28:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Feb 2026 22:28:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Feb 2026 22:28:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Feb 2026 22:28:17 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Feb 2026 22:28:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Feb 2026 22:28:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427265c7591907f60845f56adb5eb4dcd95f4be72e147ac7e960c8620bf4c84a`  
		Last Modified: Fri, 27 Feb 2026 22:28:40 GMT  
		Size: 7.6 MB (7577541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4560112e45d4357e88f9079d4da2f4a7f0091df3e41bbba7a68a708ca997d60`  
		Last Modified: Fri, 27 Feb 2026 22:28:43 GMT  
		Size: 192.5 MB (192464944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ea07032172a5db2a3c535157a269657bf91e016cd8ab9ffa4bbb938df06b37`  
		Last Modified: Fri, 27 Feb 2026 22:28:39 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9db8a1e198cfa2ab5153c13e6e0734d80407590b55f7ff03bf1e58690c3716`  
		Last Modified: Fri, 27 Feb 2026 22:28:39 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f72c6c37aca5cfc02307ca8b711e52b305feddc6589c24e3b49f8b58dc3b051`  
		Last Modified: Fri, 27 Feb 2026 22:28:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669821d7b0c1fdac2b4180a3a2b902a673c5013e5745d560306616119d53b2bd`  
		Last Modified: Fri, 27 Feb 2026 22:28:40 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891d2ce3f0310233a911c9f03e78097e849d5139a0a1c1a3ee328b6c7f09be1a`  
		Last Modified: Fri, 27 Feb 2026 22:28:41 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.7.21` - unknown; unknown

```console
$ docker pull clickhouse@sha256:56054686c14d094737185f35d132bb7c8c7b110d8c2442b58ef071f6ff46a59c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10ad18e978faa91bbab35b8c146313ab77b4128d0d2efcd0955d75c0c9b12eb8`

```dockerfile
```

-	Layers:
	-	`sha256:4a42811e1eaee96429cd262b4b5726c56f02fc721a2f51fb08b61739db30b59b`  
		Last Modified: Fri, 27 Feb 2026 22:28:39 GMT  
		Size: 25.6 KB (25625 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.12.7.21-jammy`

```console
$ docker pull clickhouse@sha256:3774ff0f86beed192c067cd4dfa0f8591b1fd1a0b079082d512b7a166d6da5f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.12.7.21-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:a0d96b2e9ce670d08ba8cc5f96bc45b8ccf56f521cd4e4d358d6ed9c0646ddc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246380284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74c146e38cf8a2fedb558cbb7476beec57300c9b2493e4ea4d18d95b786c11e4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 27 Feb 2026 22:27:55 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Feb 2026 22:27:55 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Feb 2026 22:27:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Feb 2026 22:27:55 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Feb 2026 22:27:55 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Feb 2026 22:27:55 GMT
ARG VERSION=25.12.7.21
# Fri, 27 Feb 2026 22:27:55 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Feb 2026 22:28:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.7.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Feb 2026 22:28:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.7.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Feb 2026 22:28:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.7.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Feb 2026 22:28:24 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Feb 2026 22:28:24 GMT
ENV TZ=UTC
# Fri, 27 Feb 2026 22:28:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.7.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Feb 2026 22:28:24 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Feb 2026 22:28:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Feb 2026 22:28:24 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Feb 2026 22:28:24 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Feb 2026 22:28:24 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Feb 2026 22:28:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8d099a96f70c076e1819201823630e441353c18bac1712345ab10eaa53c511`  
		Last Modified: Fri, 27 Feb 2026 22:28:50 GMT  
		Size: 7.6 MB (7598279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3dcbb76724f8f371a704e52113438bc40a6a0b9218c167ea4f0b8011189ed7`  
		Last Modified: Fri, 27 Feb 2026 22:28:54 GMT  
		Size: 208.4 MB (208374593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0545996ff9a927792111c49ce0e364252e2a09a52bb7968fd9e91253f1d601b`  
		Last Modified: Fri, 27 Feb 2026 22:28:50 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48b98ba68effe2b8ac999a5b8c9983069ea15fe925f6a0b9507099012530a81`  
		Last Modified: Fri, 27 Feb 2026 22:28:50 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b40507c558d02b06dbaae72c3c245992bda893a2b52bed0c55e5a19068bc15`  
		Last Modified: Fri, 27 Feb 2026 22:28:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf86ef885f1a57ec1e0aef70ab02355bd93897c099c39f9374c9df3337bd70ec`  
		Last Modified: Fri, 27 Feb 2026 22:28:51 GMT  
		Size: 358.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f239b1782b3ada59abf21104ab16ac616db4e2d64c53f8c3a8e5bc973e51dd`  
		Last Modified: Fri, 27 Feb 2026 22:28:52 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.7.21-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:7e0d4fe993baca231998568186a262c3700f7f61bd51917e2a10c7794748867f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9539f192849f3ed422254283c0af6d0a2e9e0bc1847af10222fb17933c9654fc`

```dockerfile
```

-	Layers:
	-	`sha256:564966241615df78ff9d69b6157cc3f77af6dbbd69d3c294f7ee550c53bf0e3f`  
		Last Modified: Fri, 27 Feb 2026 22:28:50 GMT  
		Size: 25.4 KB (25436 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.12.7.21-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:cb916bcab99e2d63529b72b111d6d98b1e0e599f6b91921962dd32c1279e5e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228297479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6510ecd4564970437239226b557dba010fe2295c8ad99d031062cb3c4b50ad9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Fri, 27 Feb 2026 22:27:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Feb 2026 22:27:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Feb 2026 22:27:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Feb 2026 22:27:47 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Feb 2026 22:27:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Feb 2026 22:27:47 GMT
ARG VERSION=25.12.7.21
# Fri, 27 Feb 2026 22:27:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Feb 2026 22:28:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.7.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Feb 2026 22:28:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.7.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Feb 2026 22:28:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.7.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Feb 2026 22:28:17 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Feb 2026 22:28:17 GMT
ENV TZ=UTC
# Fri, 27 Feb 2026 22:28:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.7.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Feb 2026 22:28:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Feb 2026 22:28:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Feb 2026 22:28:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Feb 2026 22:28:17 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Feb 2026 22:28:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Feb 2026 22:28:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427265c7591907f60845f56adb5eb4dcd95f4be72e147ac7e960c8620bf4c84a`  
		Last Modified: Fri, 27 Feb 2026 22:28:40 GMT  
		Size: 7.6 MB (7577541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4560112e45d4357e88f9079d4da2f4a7f0091df3e41bbba7a68a708ca997d60`  
		Last Modified: Fri, 27 Feb 2026 22:28:43 GMT  
		Size: 192.5 MB (192464944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ea07032172a5db2a3c535157a269657bf91e016cd8ab9ffa4bbb938df06b37`  
		Last Modified: Fri, 27 Feb 2026 22:28:39 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9db8a1e198cfa2ab5153c13e6e0734d80407590b55f7ff03bf1e58690c3716`  
		Last Modified: Fri, 27 Feb 2026 22:28:39 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f72c6c37aca5cfc02307ca8b711e52b305feddc6589c24e3b49f8b58dc3b051`  
		Last Modified: Fri, 27 Feb 2026 22:28:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669821d7b0c1fdac2b4180a3a2b902a673c5013e5745d560306616119d53b2bd`  
		Last Modified: Fri, 27 Feb 2026 22:28:40 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891d2ce3f0310233a911c9f03e78097e849d5139a0a1c1a3ee328b6c7f09be1a`  
		Last Modified: Fri, 27 Feb 2026 22:28:41 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.7.21-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:56054686c14d094737185f35d132bb7c8c7b110d8c2442b58ef071f6ff46a59c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10ad18e978faa91bbab35b8c146313ab77b4128d0d2efcd0955d75c0c9b12eb8`

```dockerfile
```

-	Layers:
	-	`sha256:4a42811e1eaee96429cd262b4b5726c56f02fc721a2f51fb08b61739db30b59b`  
		Last Modified: Fri, 27 Feb 2026 22:28:39 GMT  
		Size: 25.6 KB (25625 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3`

```console
$ docker pull clickhouse@sha256:a161d2462162002de37ef285f97ee473ff6508e71ed81731086b45058f7971a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:68b993f2d07340a659657c85dbec8c0e6664c4763ed2e16677805ac01eba6c87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206336680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddae4d17c8b5b9c19686e4b059d576168ca5cfa47e7ac610e39ce0056dfd1005`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:12:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:12:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:12:18 GMT
ARG VERSION=25.3.14.14
# Tue, 17 Feb 2026 20:12:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:44 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:44 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:44 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea5956e9ce06105113f91334938df5dcf525a8bc3df1c2a16f57e7f2b6a425e`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 7.2 MB (7151509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd687d6ec6fb5e767ac2ca0cf6d3411821c2963f0640e0e7316bbb579e892f9c`  
		Last Modified: Tue, 17 Feb 2026 20:13:07 GMT  
		Size: 168.8 MB (168777561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbfc1879e0b9308f93961875da0ed4a1eeea8e8338923e92c8fd29dec9372c8`  
		Last Modified: Tue, 17 Feb 2026 20:13:02 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560b24731cae82462de66b7d68ab1508e053d735ee7d2bac36fff6a9289b78f0`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81dbbc20ed2fff54fd78c0590eaf506bffd7a5c803469fe9ac05e04dbdb7860d`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8413cb2badc60c87392ed27852cbeb3e4c2f9813d852f8ae754ee0a8ba0426bd`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2059c77eb3baaca966ebdda21ee54d6da774ddde0eb1e45ed10c5ea89e3542`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:190da4274705d84510bc8104aaae91dbf618e9cf2060d8d588b9b1df7a1991bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aafc7844525af3653222389e37e92e42b166fd754a24836b758e384ab815546d`

```dockerfile
```

-	Layers:
	-	`sha256:efc0464d0f6bea6c6a6592de9a192f7ea548342e2624f968db4bf76d272f23ff`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 25.2 KB (25235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:485453bc6aa4103654609fcce1b5a83f178933e16b3b172b1e12d734a5cbda45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193806497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:616e0f6b5e42d7886179a3dfb40e0fd3da2b1eb6b6f1a113cb70ef9ea73ebd66`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:33 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:33 GMT
ARG VERSION=25.3.14.14
# Tue, 17 Feb 2026 20:11:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:11:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:11:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:00 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:00 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59885813d2f331b43b4d1b4a603417ed9d9a5cbc416424ae6b095157475d29b8`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 7.1 MB (7128067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9daf47d8683bb463fc285f6fa2c0389a2631e55679b3ae463e2ab577942d4883`  
		Last Modified: Tue, 17 Feb 2026 20:12:26 GMT  
		Size: 158.4 MB (158423249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a7d7c1ac561fd5f9a2a2d52cd577d5a4947992fe513cb6eb9eb94786fd16de`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac72554f2c42ff26b6ee6b1bb296f8ad25875544d0f7f6a53d3e6c33c2574089`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 865.7 KB (865743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471715e89c512d9a8ae44d90031fe06f801f3aa194634227cdd295803c805172`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88a679bec67c5fc1629125025793f282530a3fbfe4632cc065265a71a0490b2`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3610c5656cde1e3bdb996350e08bcaf439884c976546b048f90e380470c279f1`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 3.8 KB (3833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c7570325bce91d940a46b84cefce0ee0dcfef171bbdb74f61141cb965f42e73c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907a078740daa561978d8bd3f2180da51d1a7d0ee6e73d20bc77d43d00114e07`

```dockerfile
```

-	Layers:
	-	`sha256:29e9f9a0d1bd0b8f9de203da15c5c54b93f793c82362c853130c14729f32fb1c`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3-jammy`

```console
$ docker pull clickhouse@sha256:a161d2462162002de37ef285f97ee473ff6508e71ed81731086b45058f7971a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:68b993f2d07340a659657c85dbec8c0e6664c4763ed2e16677805ac01eba6c87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206336680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddae4d17c8b5b9c19686e4b059d576168ca5cfa47e7ac610e39ce0056dfd1005`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:12:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:12:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:12:18 GMT
ARG VERSION=25.3.14.14
# Tue, 17 Feb 2026 20:12:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:44 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:44 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:44 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea5956e9ce06105113f91334938df5dcf525a8bc3df1c2a16f57e7f2b6a425e`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 7.2 MB (7151509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd687d6ec6fb5e767ac2ca0cf6d3411821c2963f0640e0e7316bbb579e892f9c`  
		Last Modified: Tue, 17 Feb 2026 20:13:07 GMT  
		Size: 168.8 MB (168777561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbfc1879e0b9308f93961875da0ed4a1eeea8e8338923e92c8fd29dec9372c8`  
		Last Modified: Tue, 17 Feb 2026 20:13:02 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560b24731cae82462de66b7d68ab1508e053d735ee7d2bac36fff6a9289b78f0`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81dbbc20ed2fff54fd78c0590eaf506bffd7a5c803469fe9ac05e04dbdb7860d`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8413cb2badc60c87392ed27852cbeb3e4c2f9813d852f8ae754ee0a8ba0426bd`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2059c77eb3baaca966ebdda21ee54d6da774ddde0eb1e45ed10c5ea89e3542`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:190da4274705d84510bc8104aaae91dbf618e9cf2060d8d588b9b1df7a1991bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aafc7844525af3653222389e37e92e42b166fd754a24836b758e384ab815546d`

```dockerfile
```

-	Layers:
	-	`sha256:efc0464d0f6bea6c6a6592de9a192f7ea548342e2624f968db4bf76d272f23ff`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 25.2 KB (25235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:485453bc6aa4103654609fcce1b5a83f178933e16b3b172b1e12d734a5cbda45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193806497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:616e0f6b5e42d7886179a3dfb40e0fd3da2b1eb6b6f1a113cb70ef9ea73ebd66`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:33 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:33 GMT
ARG VERSION=25.3.14.14
# Tue, 17 Feb 2026 20:11:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:11:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:11:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:00 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:00 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59885813d2f331b43b4d1b4a603417ed9d9a5cbc416424ae6b095157475d29b8`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 7.1 MB (7128067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9daf47d8683bb463fc285f6fa2c0389a2631e55679b3ae463e2ab577942d4883`  
		Last Modified: Tue, 17 Feb 2026 20:12:26 GMT  
		Size: 158.4 MB (158423249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a7d7c1ac561fd5f9a2a2d52cd577d5a4947992fe513cb6eb9eb94786fd16de`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac72554f2c42ff26b6ee6b1bb296f8ad25875544d0f7f6a53d3e6c33c2574089`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 865.7 KB (865743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471715e89c512d9a8ae44d90031fe06f801f3aa194634227cdd295803c805172`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88a679bec67c5fc1629125025793f282530a3fbfe4632cc065265a71a0490b2`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3610c5656cde1e3bdb996350e08bcaf439884c976546b048f90e380470c279f1`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 3.8 KB (3833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c7570325bce91d940a46b84cefce0ee0dcfef171bbdb74f61141cb965f42e73c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907a078740daa561978d8bd3f2180da51d1a7d0ee6e73d20bc77d43d00114e07`

```dockerfile
```

-	Layers:
	-	`sha256:29e9f9a0d1bd0b8f9de203da15c5c54b93f793c82362c853130c14729f32fb1c`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.14`

```console
$ docker pull clickhouse@sha256:a161d2462162002de37ef285f97ee473ff6508e71ed81731086b45058f7971a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.14` - linux; amd64

```console
$ docker pull clickhouse@sha256:68b993f2d07340a659657c85dbec8c0e6664c4763ed2e16677805ac01eba6c87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206336680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddae4d17c8b5b9c19686e4b059d576168ca5cfa47e7ac610e39ce0056dfd1005`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:12:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:12:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:12:18 GMT
ARG VERSION=25.3.14.14
# Tue, 17 Feb 2026 20:12:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:44 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:44 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:44 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea5956e9ce06105113f91334938df5dcf525a8bc3df1c2a16f57e7f2b6a425e`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 7.2 MB (7151509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd687d6ec6fb5e767ac2ca0cf6d3411821c2963f0640e0e7316bbb579e892f9c`  
		Last Modified: Tue, 17 Feb 2026 20:13:07 GMT  
		Size: 168.8 MB (168777561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbfc1879e0b9308f93961875da0ed4a1eeea8e8338923e92c8fd29dec9372c8`  
		Last Modified: Tue, 17 Feb 2026 20:13:02 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560b24731cae82462de66b7d68ab1508e053d735ee7d2bac36fff6a9289b78f0`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81dbbc20ed2fff54fd78c0590eaf506bffd7a5c803469fe9ac05e04dbdb7860d`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8413cb2badc60c87392ed27852cbeb3e4c2f9813d852f8ae754ee0a8ba0426bd`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2059c77eb3baaca966ebdda21ee54d6da774ddde0eb1e45ed10c5ea89e3542`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.14` - unknown; unknown

```console
$ docker pull clickhouse@sha256:190da4274705d84510bc8104aaae91dbf618e9cf2060d8d588b9b1df7a1991bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aafc7844525af3653222389e37e92e42b166fd754a24836b758e384ab815546d`

```dockerfile
```

-	Layers:
	-	`sha256:efc0464d0f6bea6c6a6592de9a192f7ea548342e2624f968db4bf76d272f23ff`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 25.2 KB (25235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.14` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:485453bc6aa4103654609fcce1b5a83f178933e16b3b172b1e12d734a5cbda45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193806497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:616e0f6b5e42d7886179a3dfb40e0fd3da2b1eb6b6f1a113cb70ef9ea73ebd66`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:33 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:33 GMT
ARG VERSION=25.3.14.14
# Tue, 17 Feb 2026 20:11:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:11:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:11:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:00 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:00 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59885813d2f331b43b4d1b4a603417ed9d9a5cbc416424ae6b095157475d29b8`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 7.1 MB (7128067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9daf47d8683bb463fc285f6fa2c0389a2631e55679b3ae463e2ab577942d4883`  
		Last Modified: Tue, 17 Feb 2026 20:12:26 GMT  
		Size: 158.4 MB (158423249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a7d7c1ac561fd5f9a2a2d52cd577d5a4947992fe513cb6eb9eb94786fd16de`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac72554f2c42ff26b6ee6b1bb296f8ad25875544d0f7f6a53d3e6c33c2574089`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 865.7 KB (865743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471715e89c512d9a8ae44d90031fe06f801f3aa194634227cdd295803c805172`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88a679bec67c5fc1629125025793f282530a3fbfe4632cc065265a71a0490b2`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3610c5656cde1e3bdb996350e08bcaf439884c976546b048f90e380470c279f1`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 3.8 KB (3833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.14` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c7570325bce91d940a46b84cefce0ee0dcfef171bbdb74f61141cb965f42e73c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907a078740daa561978d8bd3f2180da51d1a7d0ee6e73d20bc77d43d00114e07`

```dockerfile
```

-	Layers:
	-	`sha256:29e9f9a0d1bd0b8f9de203da15c5c54b93f793c82362c853130c14729f32fb1c`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.14-jammy`

```console
$ docker pull clickhouse@sha256:a161d2462162002de37ef285f97ee473ff6508e71ed81731086b45058f7971a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.14-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:68b993f2d07340a659657c85dbec8c0e6664c4763ed2e16677805ac01eba6c87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206336680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddae4d17c8b5b9c19686e4b059d576168ca5cfa47e7ac610e39ce0056dfd1005`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:12:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:12:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:12:18 GMT
ARG VERSION=25.3.14.14
# Tue, 17 Feb 2026 20:12:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:44 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:44 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:44 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea5956e9ce06105113f91334938df5dcf525a8bc3df1c2a16f57e7f2b6a425e`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 7.2 MB (7151509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd687d6ec6fb5e767ac2ca0cf6d3411821c2963f0640e0e7316bbb579e892f9c`  
		Last Modified: Tue, 17 Feb 2026 20:13:07 GMT  
		Size: 168.8 MB (168777561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbfc1879e0b9308f93961875da0ed4a1eeea8e8338923e92c8fd29dec9372c8`  
		Last Modified: Tue, 17 Feb 2026 20:13:02 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560b24731cae82462de66b7d68ab1508e053d735ee7d2bac36fff6a9289b78f0`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81dbbc20ed2fff54fd78c0590eaf506bffd7a5c803469fe9ac05e04dbdb7860d`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8413cb2badc60c87392ed27852cbeb3e4c2f9813d852f8ae754ee0a8ba0426bd`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2059c77eb3baaca966ebdda21ee54d6da774ddde0eb1e45ed10c5ea89e3542`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.14-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:190da4274705d84510bc8104aaae91dbf618e9cf2060d8d588b9b1df7a1991bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aafc7844525af3653222389e37e92e42b166fd754a24836b758e384ab815546d`

```dockerfile
```

-	Layers:
	-	`sha256:efc0464d0f6bea6c6a6592de9a192f7ea548342e2624f968db4bf76d272f23ff`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 25.2 KB (25235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.14-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:485453bc6aa4103654609fcce1b5a83f178933e16b3b172b1e12d734a5cbda45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193806497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:616e0f6b5e42d7886179a3dfb40e0fd3da2b1eb6b6f1a113cb70ef9ea73ebd66`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:33 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:33 GMT
ARG VERSION=25.3.14.14
# Tue, 17 Feb 2026 20:11:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:11:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:11:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:00 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:00 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59885813d2f331b43b4d1b4a603417ed9d9a5cbc416424ae6b095157475d29b8`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 7.1 MB (7128067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9daf47d8683bb463fc285f6fa2c0389a2631e55679b3ae463e2ab577942d4883`  
		Last Modified: Tue, 17 Feb 2026 20:12:26 GMT  
		Size: 158.4 MB (158423249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a7d7c1ac561fd5f9a2a2d52cd577d5a4947992fe513cb6eb9eb94786fd16de`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac72554f2c42ff26b6ee6b1bb296f8ad25875544d0f7f6a53d3e6c33c2574089`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 865.7 KB (865743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471715e89c512d9a8ae44d90031fe06f801f3aa194634227cdd295803c805172`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88a679bec67c5fc1629125025793f282530a3fbfe4632cc065265a71a0490b2`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3610c5656cde1e3bdb996350e08bcaf439884c976546b048f90e380470c279f1`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 3.8 KB (3833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.14-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c7570325bce91d940a46b84cefce0ee0dcfef171bbdb74f61141cb965f42e73c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907a078740daa561978d8bd3f2180da51d1a7d0ee6e73d20bc77d43d00114e07`

```dockerfile
```

-	Layers:
	-	`sha256:29e9f9a0d1bd0b8f9de203da15c5c54b93f793c82362c853130c14729f32fb1c`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.14.14`

```console
$ docker pull clickhouse@sha256:a161d2462162002de37ef285f97ee473ff6508e71ed81731086b45058f7971a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.14.14` - linux; amd64

```console
$ docker pull clickhouse@sha256:68b993f2d07340a659657c85dbec8c0e6664c4763ed2e16677805ac01eba6c87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206336680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddae4d17c8b5b9c19686e4b059d576168ca5cfa47e7ac610e39ce0056dfd1005`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:12:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:12:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:12:18 GMT
ARG VERSION=25.3.14.14
# Tue, 17 Feb 2026 20:12:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:44 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:44 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:44 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea5956e9ce06105113f91334938df5dcf525a8bc3df1c2a16f57e7f2b6a425e`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 7.2 MB (7151509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd687d6ec6fb5e767ac2ca0cf6d3411821c2963f0640e0e7316bbb579e892f9c`  
		Last Modified: Tue, 17 Feb 2026 20:13:07 GMT  
		Size: 168.8 MB (168777561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbfc1879e0b9308f93961875da0ed4a1eeea8e8338923e92c8fd29dec9372c8`  
		Last Modified: Tue, 17 Feb 2026 20:13:02 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560b24731cae82462de66b7d68ab1508e053d735ee7d2bac36fff6a9289b78f0`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81dbbc20ed2fff54fd78c0590eaf506bffd7a5c803469fe9ac05e04dbdb7860d`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8413cb2badc60c87392ed27852cbeb3e4c2f9813d852f8ae754ee0a8ba0426bd`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2059c77eb3baaca966ebdda21ee54d6da774ddde0eb1e45ed10c5ea89e3542`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.14.14` - unknown; unknown

```console
$ docker pull clickhouse@sha256:190da4274705d84510bc8104aaae91dbf618e9cf2060d8d588b9b1df7a1991bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aafc7844525af3653222389e37e92e42b166fd754a24836b758e384ab815546d`

```dockerfile
```

-	Layers:
	-	`sha256:efc0464d0f6bea6c6a6592de9a192f7ea548342e2624f968db4bf76d272f23ff`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 25.2 KB (25235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.14.14` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:485453bc6aa4103654609fcce1b5a83f178933e16b3b172b1e12d734a5cbda45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193806497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:616e0f6b5e42d7886179a3dfb40e0fd3da2b1eb6b6f1a113cb70ef9ea73ebd66`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:33 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:33 GMT
ARG VERSION=25.3.14.14
# Tue, 17 Feb 2026 20:11:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:11:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:11:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:00 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:00 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59885813d2f331b43b4d1b4a603417ed9d9a5cbc416424ae6b095157475d29b8`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 7.1 MB (7128067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9daf47d8683bb463fc285f6fa2c0389a2631e55679b3ae463e2ab577942d4883`  
		Last Modified: Tue, 17 Feb 2026 20:12:26 GMT  
		Size: 158.4 MB (158423249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a7d7c1ac561fd5f9a2a2d52cd577d5a4947992fe513cb6eb9eb94786fd16de`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac72554f2c42ff26b6ee6b1bb296f8ad25875544d0f7f6a53d3e6c33c2574089`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 865.7 KB (865743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471715e89c512d9a8ae44d90031fe06f801f3aa194634227cdd295803c805172`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88a679bec67c5fc1629125025793f282530a3fbfe4632cc065265a71a0490b2`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3610c5656cde1e3bdb996350e08bcaf439884c976546b048f90e380470c279f1`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 3.8 KB (3833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.14.14` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c7570325bce91d940a46b84cefce0ee0dcfef171bbdb74f61141cb965f42e73c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907a078740daa561978d8bd3f2180da51d1a7d0ee6e73d20bc77d43d00114e07`

```dockerfile
```

-	Layers:
	-	`sha256:29e9f9a0d1bd0b8f9de203da15c5c54b93f793c82362c853130c14729f32fb1c`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.14.14-jammy`

```console
$ docker pull clickhouse@sha256:a161d2462162002de37ef285f97ee473ff6508e71ed81731086b45058f7971a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.14.14-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:68b993f2d07340a659657c85dbec8c0e6664c4763ed2e16677805ac01eba6c87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206336680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddae4d17c8b5b9c19686e4b059d576168ca5cfa47e7ac610e39ce0056dfd1005`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:12:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:12:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:12:18 GMT
ARG VERSION=25.3.14.14
# Tue, 17 Feb 2026 20:12:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:44 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:44 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:44 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea5956e9ce06105113f91334938df5dcf525a8bc3df1c2a16f57e7f2b6a425e`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 7.2 MB (7151509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd687d6ec6fb5e767ac2ca0cf6d3411821c2963f0640e0e7316bbb579e892f9c`  
		Last Modified: Tue, 17 Feb 2026 20:13:07 GMT  
		Size: 168.8 MB (168777561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbfc1879e0b9308f93961875da0ed4a1eeea8e8338923e92c8fd29dec9372c8`  
		Last Modified: Tue, 17 Feb 2026 20:13:02 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560b24731cae82462de66b7d68ab1508e053d735ee7d2bac36fff6a9289b78f0`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81dbbc20ed2fff54fd78c0590eaf506bffd7a5c803469fe9ac05e04dbdb7860d`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8413cb2badc60c87392ed27852cbeb3e4c2f9813d852f8ae754ee0a8ba0426bd`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2059c77eb3baaca966ebdda21ee54d6da774ddde0eb1e45ed10c5ea89e3542`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.14.14-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:190da4274705d84510bc8104aaae91dbf618e9cf2060d8d588b9b1df7a1991bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aafc7844525af3653222389e37e92e42b166fd754a24836b758e384ab815546d`

```dockerfile
```

-	Layers:
	-	`sha256:efc0464d0f6bea6c6a6592de9a192f7ea548342e2624f968db4bf76d272f23ff`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 25.2 KB (25235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.14.14-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:485453bc6aa4103654609fcce1b5a83f178933e16b3b172b1e12d734a5cbda45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193806497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:616e0f6b5e42d7886179a3dfb40e0fd3da2b1eb6b6f1a113cb70ef9ea73ebd66`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:33 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:33 GMT
ARG VERSION=25.3.14.14
# Tue, 17 Feb 2026 20:11:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:11:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:11:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:00 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:00 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59885813d2f331b43b4d1b4a603417ed9d9a5cbc416424ae6b095157475d29b8`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 7.1 MB (7128067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9daf47d8683bb463fc285f6fa2c0389a2631e55679b3ae463e2ab577942d4883`  
		Last Modified: Tue, 17 Feb 2026 20:12:26 GMT  
		Size: 158.4 MB (158423249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a7d7c1ac561fd5f9a2a2d52cd577d5a4947992fe513cb6eb9eb94786fd16de`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac72554f2c42ff26b6ee6b1bb296f8ad25875544d0f7f6a53d3e6c33c2574089`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 865.7 KB (865743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471715e89c512d9a8ae44d90031fe06f801f3aa194634227cdd295803c805172`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88a679bec67c5fc1629125025793f282530a3fbfe4632cc065265a71a0490b2`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3610c5656cde1e3bdb996350e08bcaf439884c976546b048f90e380470c279f1`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 3.8 KB (3833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.14.14-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c7570325bce91d940a46b84cefce0ee0dcfef171bbdb74f61141cb965f42e73c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907a078740daa561978d8bd3f2180da51d1a7d0ee6e73d20bc77d43d00114e07`

```dockerfile
```

-	Layers:
	-	`sha256:29e9f9a0d1bd0b8f9de203da15c5c54b93f793c82362c853130c14729f32fb1c`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8`

```console
$ docker pull clickhouse@sha256:cb8ea3c339aa84c1d75e0c9fc08f372e0398576caa3d787e7f27b9bbca483d3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8` - linux; amd64

```console
$ docker pull clickhouse@sha256:0ec0e053c41857406923f72d00580eac2b61fe11aff754672a9ed03f172c02c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228945044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5381324c8bcc3410608a9c899346d8806971bcef1a1a5fad7b59b6418415de5`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:26 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:12:26 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:12:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:12:26 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:12:26 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:12:26 GMT
ARG VERSION=25.8.16.34
# Tue, 17 Feb 2026 20:12:26 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:53 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:53 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:53 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820dee958d69ceaceb4ea57bc08fb7179f6c7e0987acf3a83c3fb4d05fecc5f2`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 7.6 MB (7598324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258567d60460abdf8fc0d705b07cfb5c2cf9c109302d7d2c766667ce48775f4c`  
		Last Modified: Tue, 17 Feb 2026 20:13:16 GMT  
		Size: 190.9 MB (190939334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e88afd8fd9b9d7dc8563b7db8a2a6351683c3b3e457879c7f4c041b98bff53e`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53900b96e71ca59796a1577140c2aea52ebe99495fc78ab718f66f89ce11fda`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b306d071c1343d8dc0c6d88a9a96ca5aa60bd057563577ae76fd30fbf89e8a3f`  
		Last Modified: Tue, 17 Feb 2026 20:13:13 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c6fbf6e82586a7efc880a4aa52b6e2c210259ad18c01db546ba7da838bd3af`  
		Last Modified: Tue, 17 Feb 2026 20:13:14 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9009d2f669d7bd059ba402b69f6770efd463c0a1f88b6c0a81fce2aa343e61b`  
		Last Modified: Tue, 17 Feb 2026 20:13:14 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0f00e22ef556b57f9002953ccb230258a724d206ddecc96ddef872a1715c4cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b864971555410cf3c7ecd8e15f929470ad3e6751db3fb535b698bb37a50e09a9`

```dockerfile
```

-	Layers:
	-	`sha256:b03ea5c9cfa2f868003976091441edbc705a684639b36b3607bd13f9e0fa5a85`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:2bc2d567de72e07f96d39d437aa8ad8c85de7d62d947633c5197d97d05e3603b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213848446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6a020363e23f68ae53ea85f8d5889d92a049d464d3eac58db615f3903fd82d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:49 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:49 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:49 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:49 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:49 GMT
ARG VERSION=25.8.16.34
# Tue, 17 Feb 2026 20:11:49 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:18 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:18 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e105b5258b6287684da632f28c009bead56d72476c38c18b71037e43e8e9b7c`  
		Last Modified: Tue, 17 Feb 2026 20:12:39 GMT  
		Size: 7.6 MB (7577435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494d420eedbfb97f76c475c4139188424ad202fa0e076dcced2c2495768b59ac`  
		Last Modified: Tue, 17 Feb 2026 20:12:41 GMT  
		Size: 178.0 MB (178016046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c477e7fcc96d3a9fe18cfd60a3109816b4a377d41bfdb46d3e0a3438fd193976`  
		Last Modified: Tue, 17 Feb 2026 20:12:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56a0a0e8730d6ac8153fd30fc3f7dc73e6e5160fa253c8ffa137dbdb06914b4`  
		Last Modified: Tue, 17 Feb 2026 20:12:37 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55e4b063f018d389136b40b857059bb4e1bb4f5af6046376bb9edfcad0241ff`  
		Last Modified: Tue, 17 Feb 2026 20:12:38 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ac4fd6f889704ea3b167cbbc7b274f8178ae69d00df70debe3e214aa936b13`  
		Last Modified: Tue, 17 Feb 2026 20:12:38 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff96f921752d4141c565ccca7e44ec7c882d09ac1601be61a0997273ce77657c`  
		Last Modified: Tue, 17 Feb 2026 20:12:40 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e40bf21f69748ff21ecb45294a3d5abada6026f07908ff61c72014db1bb06598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8a041960efb6f4644dde88a255c026fc5cac64f703efced83f24300b69ce680`

```dockerfile
```

-	Layers:
	-	`sha256:d61611774bdc1996895d1e9b295614f62dae75e1c939a7fb15d6abaa66d5a746`  
		Last Modified: Tue, 17 Feb 2026 20:12:37 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8-jammy`

```console
$ docker pull clickhouse@sha256:cb8ea3c339aa84c1d75e0c9fc08f372e0398576caa3d787e7f27b9bbca483d3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:0ec0e053c41857406923f72d00580eac2b61fe11aff754672a9ed03f172c02c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228945044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5381324c8bcc3410608a9c899346d8806971bcef1a1a5fad7b59b6418415de5`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:26 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:12:26 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:12:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:12:26 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:12:26 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:12:26 GMT
ARG VERSION=25.8.16.34
# Tue, 17 Feb 2026 20:12:26 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:53 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:53 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:53 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820dee958d69ceaceb4ea57bc08fb7179f6c7e0987acf3a83c3fb4d05fecc5f2`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 7.6 MB (7598324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258567d60460abdf8fc0d705b07cfb5c2cf9c109302d7d2c766667ce48775f4c`  
		Last Modified: Tue, 17 Feb 2026 20:13:16 GMT  
		Size: 190.9 MB (190939334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e88afd8fd9b9d7dc8563b7db8a2a6351683c3b3e457879c7f4c041b98bff53e`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53900b96e71ca59796a1577140c2aea52ebe99495fc78ab718f66f89ce11fda`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b306d071c1343d8dc0c6d88a9a96ca5aa60bd057563577ae76fd30fbf89e8a3f`  
		Last Modified: Tue, 17 Feb 2026 20:13:13 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c6fbf6e82586a7efc880a4aa52b6e2c210259ad18c01db546ba7da838bd3af`  
		Last Modified: Tue, 17 Feb 2026 20:13:14 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9009d2f669d7bd059ba402b69f6770efd463c0a1f88b6c0a81fce2aa343e61b`  
		Last Modified: Tue, 17 Feb 2026 20:13:14 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0f00e22ef556b57f9002953ccb230258a724d206ddecc96ddef872a1715c4cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b864971555410cf3c7ecd8e15f929470ad3e6751db3fb535b698bb37a50e09a9`

```dockerfile
```

-	Layers:
	-	`sha256:b03ea5c9cfa2f868003976091441edbc705a684639b36b3607bd13f9e0fa5a85`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:2bc2d567de72e07f96d39d437aa8ad8c85de7d62d947633c5197d97d05e3603b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213848446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6a020363e23f68ae53ea85f8d5889d92a049d464d3eac58db615f3903fd82d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:49 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:49 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:49 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:49 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:49 GMT
ARG VERSION=25.8.16.34
# Tue, 17 Feb 2026 20:11:49 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:18 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:18 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e105b5258b6287684da632f28c009bead56d72476c38c18b71037e43e8e9b7c`  
		Last Modified: Tue, 17 Feb 2026 20:12:39 GMT  
		Size: 7.6 MB (7577435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494d420eedbfb97f76c475c4139188424ad202fa0e076dcced2c2495768b59ac`  
		Last Modified: Tue, 17 Feb 2026 20:12:41 GMT  
		Size: 178.0 MB (178016046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c477e7fcc96d3a9fe18cfd60a3109816b4a377d41bfdb46d3e0a3438fd193976`  
		Last Modified: Tue, 17 Feb 2026 20:12:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56a0a0e8730d6ac8153fd30fc3f7dc73e6e5160fa253c8ffa137dbdb06914b4`  
		Last Modified: Tue, 17 Feb 2026 20:12:37 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55e4b063f018d389136b40b857059bb4e1bb4f5af6046376bb9edfcad0241ff`  
		Last Modified: Tue, 17 Feb 2026 20:12:38 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ac4fd6f889704ea3b167cbbc7b274f8178ae69d00df70debe3e214aa936b13`  
		Last Modified: Tue, 17 Feb 2026 20:12:38 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff96f921752d4141c565ccca7e44ec7c882d09ac1601be61a0997273ce77657c`  
		Last Modified: Tue, 17 Feb 2026 20:12:40 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e40bf21f69748ff21ecb45294a3d5abada6026f07908ff61c72014db1bb06598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8a041960efb6f4644dde88a255c026fc5cac64f703efced83f24300b69ce680`

```dockerfile
```

-	Layers:
	-	`sha256:d61611774bdc1996895d1e9b295614f62dae75e1c939a7fb15d6abaa66d5a746`  
		Last Modified: Tue, 17 Feb 2026 20:12:37 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.16`

```console
$ docker pull clickhouse@sha256:cb8ea3c339aa84c1d75e0c9fc08f372e0398576caa3d787e7f27b9bbca483d3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.16` - linux; amd64

```console
$ docker pull clickhouse@sha256:0ec0e053c41857406923f72d00580eac2b61fe11aff754672a9ed03f172c02c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228945044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5381324c8bcc3410608a9c899346d8806971bcef1a1a5fad7b59b6418415de5`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:26 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:12:26 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:12:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:12:26 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:12:26 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:12:26 GMT
ARG VERSION=25.8.16.34
# Tue, 17 Feb 2026 20:12:26 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:53 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:53 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:53 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820dee958d69ceaceb4ea57bc08fb7179f6c7e0987acf3a83c3fb4d05fecc5f2`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 7.6 MB (7598324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258567d60460abdf8fc0d705b07cfb5c2cf9c109302d7d2c766667ce48775f4c`  
		Last Modified: Tue, 17 Feb 2026 20:13:16 GMT  
		Size: 190.9 MB (190939334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e88afd8fd9b9d7dc8563b7db8a2a6351683c3b3e457879c7f4c041b98bff53e`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53900b96e71ca59796a1577140c2aea52ebe99495fc78ab718f66f89ce11fda`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b306d071c1343d8dc0c6d88a9a96ca5aa60bd057563577ae76fd30fbf89e8a3f`  
		Last Modified: Tue, 17 Feb 2026 20:13:13 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c6fbf6e82586a7efc880a4aa52b6e2c210259ad18c01db546ba7da838bd3af`  
		Last Modified: Tue, 17 Feb 2026 20:13:14 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9009d2f669d7bd059ba402b69f6770efd463c0a1f88b6c0a81fce2aa343e61b`  
		Last Modified: Tue, 17 Feb 2026 20:13:14 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.16` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0f00e22ef556b57f9002953ccb230258a724d206ddecc96ddef872a1715c4cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b864971555410cf3c7ecd8e15f929470ad3e6751db3fb535b698bb37a50e09a9`

```dockerfile
```

-	Layers:
	-	`sha256:b03ea5c9cfa2f868003976091441edbc705a684639b36b3607bd13f9e0fa5a85`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.16` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:2bc2d567de72e07f96d39d437aa8ad8c85de7d62d947633c5197d97d05e3603b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213848446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6a020363e23f68ae53ea85f8d5889d92a049d464d3eac58db615f3903fd82d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:49 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:49 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:49 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:49 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:49 GMT
ARG VERSION=25.8.16.34
# Tue, 17 Feb 2026 20:11:49 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:18 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:18 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e105b5258b6287684da632f28c009bead56d72476c38c18b71037e43e8e9b7c`  
		Last Modified: Tue, 17 Feb 2026 20:12:39 GMT  
		Size: 7.6 MB (7577435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494d420eedbfb97f76c475c4139188424ad202fa0e076dcced2c2495768b59ac`  
		Last Modified: Tue, 17 Feb 2026 20:12:41 GMT  
		Size: 178.0 MB (178016046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c477e7fcc96d3a9fe18cfd60a3109816b4a377d41bfdb46d3e0a3438fd193976`  
		Last Modified: Tue, 17 Feb 2026 20:12:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56a0a0e8730d6ac8153fd30fc3f7dc73e6e5160fa253c8ffa137dbdb06914b4`  
		Last Modified: Tue, 17 Feb 2026 20:12:37 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55e4b063f018d389136b40b857059bb4e1bb4f5af6046376bb9edfcad0241ff`  
		Last Modified: Tue, 17 Feb 2026 20:12:38 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ac4fd6f889704ea3b167cbbc7b274f8178ae69d00df70debe3e214aa936b13`  
		Last Modified: Tue, 17 Feb 2026 20:12:38 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff96f921752d4141c565ccca7e44ec7c882d09ac1601be61a0997273ce77657c`  
		Last Modified: Tue, 17 Feb 2026 20:12:40 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.16` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e40bf21f69748ff21ecb45294a3d5abada6026f07908ff61c72014db1bb06598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8a041960efb6f4644dde88a255c026fc5cac64f703efced83f24300b69ce680`

```dockerfile
```

-	Layers:
	-	`sha256:d61611774bdc1996895d1e9b295614f62dae75e1c939a7fb15d6abaa66d5a746`  
		Last Modified: Tue, 17 Feb 2026 20:12:37 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.16-jammy`

```console
$ docker pull clickhouse@sha256:cb8ea3c339aa84c1d75e0c9fc08f372e0398576caa3d787e7f27b9bbca483d3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.16-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:0ec0e053c41857406923f72d00580eac2b61fe11aff754672a9ed03f172c02c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228945044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5381324c8bcc3410608a9c899346d8806971bcef1a1a5fad7b59b6418415de5`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:26 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:12:26 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:12:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:12:26 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:12:26 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:12:26 GMT
ARG VERSION=25.8.16.34
# Tue, 17 Feb 2026 20:12:26 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:53 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:53 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:53 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820dee958d69ceaceb4ea57bc08fb7179f6c7e0987acf3a83c3fb4d05fecc5f2`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 7.6 MB (7598324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258567d60460abdf8fc0d705b07cfb5c2cf9c109302d7d2c766667ce48775f4c`  
		Last Modified: Tue, 17 Feb 2026 20:13:16 GMT  
		Size: 190.9 MB (190939334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e88afd8fd9b9d7dc8563b7db8a2a6351683c3b3e457879c7f4c041b98bff53e`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53900b96e71ca59796a1577140c2aea52ebe99495fc78ab718f66f89ce11fda`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b306d071c1343d8dc0c6d88a9a96ca5aa60bd057563577ae76fd30fbf89e8a3f`  
		Last Modified: Tue, 17 Feb 2026 20:13:13 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c6fbf6e82586a7efc880a4aa52b6e2c210259ad18c01db546ba7da838bd3af`  
		Last Modified: Tue, 17 Feb 2026 20:13:14 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9009d2f669d7bd059ba402b69f6770efd463c0a1f88b6c0a81fce2aa343e61b`  
		Last Modified: Tue, 17 Feb 2026 20:13:14 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.16-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0f00e22ef556b57f9002953ccb230258a724d206ddecc96ddef872a1715c4cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b864971555410cf3c7ecd8e15f929470ad3e6751db3fb535b698bb37a50e09a9`

```dockerfile
```

-	Layers:
	-	`sha256:b03ea5c9cfa2f868003976091441edbc705a684639b36b3607bd13f9e0fa5a85`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.16-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:2bc2d567de72e07f96d39d437aa8ad8c85de7d62d947633c5197d97d05e3603b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213848446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6a020363e23f68ae53ea85f8d5889d92a049d464d3eac58db615f3903fd82d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:49 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:49 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:49 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:49 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:49 GMT
ARG VERSION=25.8.16.34
# Tue, 17 Feb 2026 20:11:49 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:18 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:18 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e105b5258b6287684da632f28c009bead56d72476c38c18b71037e43e8e9b7c`  
		Last Modified: Tue, 17 Feb 2026 20:12:39 GMT  
		Size: 7.6 MB (7577435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494d420eedbfb97f76c475c4139188424ad202fa0e076dcced2c2495768b59ac`  
		Last Modified: Tue, 17 Feb 2026 20:12:41 GMT  
		Size: 178.0 MB (178016046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c477e7fcc96d3a9fe18cfd60a3109816b4a377d41bfdb46d3e0a3438fd193976`  
		Last Modified: Tue, 17 Feb 2026 20:12:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56a0a0e8730d6ac8153fd30fc3f7dc73e6e5160fa253c8ffa137dbdb06914b4`  
		Last Modified: Tue, 17 Feb 2026 20:12:37 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55e4b063f018d389136b40b857059bb4e1bb4f5af6046376bb9edfcad0241ff`  
		Last Modified: Tue, 17 Feb 2026 20:12:38 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ac4fd6f889704ea3b167cbbc7b274f8178ae69d00df70debe3e214aa936b13`  
		Last Modified: Tue, 17 Feb 2026 20:12:38 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff96f921752d4141c565ccca7e44ec7c882d09ac1601be61a0997273ce77657c`  
		Last Modified: Tue, 17 Feb 2026 20:12:40 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.16-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e40bf21f69748ff21ecb45294a3d5abada6026f07908ff61c72014db1bb06598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8a041960efb6f4644dde88a255c026fc5cac64f703efced83f24300b69ce680`

```dockerfile
```

-	Layers:
	-	`sha256:d61611774bdc1996895d1e9b295614f62dae75e1c939a7fb15d6abaa66d5a746`  
		Last Modified: Tue, 17 Feb 2026 20:12:37 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.16.34`

```console
$ docker pull clickhouse@sha256:cb8ea3c339aa84c1d75e0c9fc08f372e0398576caa3d787e7f27b9bbca483d3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.16.34` - linux; amd64

```console
$ docker pull clickhouse@sha256:0ec0e053c41857406923f72d00580eac2b61fe11aff754672a9ed03f172c02c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228945044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5381324c8bcc3410608a9c899346d8806971bcef1a1a5fad7b59b6418415de5`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:26 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:12:26 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:12:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:12:26 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:12:26 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:12:26 GMT
ARG VERSION=25.8.16.34
# Tue, 17 Feb 2026 20:12:26 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:53 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:53 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:53 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820dee958d69ceaceb4ea57bc08fb7179f6c7e0987acf3a83c3fb4d05fecc5f2`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 7.6 MB (7598324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258567d60460abdf8fc0d705b07cfb5c2cf9c109302d7d2c766667ce48775f4c`  
		Last Modified: Tue, 17 Feb 2026 20:13:16 GMT  
		Size: 190.9 MB (190939334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e88afd8fd9b9d7dc8563b7db8a2a6351683c3b3e457879c7f4c041b98bff53e`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53900b96e71ca59796a1577140c2aea52ebe99495fc78ab718f66f89ce11fda`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b306d071c1343d8dc0c6d88a9a96ca5aa60bd057563577ae76fd30fbf89e8a3f`  
		Last Modified: Tue, 17 Feb 2026 20:13:13 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c6fbf6e82586a7efc880a4aa52b6e2c210259ad18c01db546ba7da838bd3af`  
		Last Modified: Tue, 17 Feb 2026 20:13:14 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9009d2f669d7bd059ba402b69f6770efd463c0a1f88b6c0a81fce2aa343e61b`  
		Last Modified: Tue, 17 Feb 2026 20:13:14 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.16.34` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0f00e22ef556b57f9002953ccb230258a724d206ddecc96ddef872a1715c4cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b864971555410cf3c7ecd8e15f929470ad3e6751db3fb535b698bb37a50e09a9`

```dockerfile
```

-	Layers:
	-	`sha256:b03ea5c9cfa2f868003976091441edbc705a684639b36b3607bd13f9e0fa5a85`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.16.34` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:2bc2d567de72e07f96d39d437aa8ad8c85de7d62d947633c5197d97d05e3603b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213848446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6a020363e23f68ae53ea85f8d5889d92a049d464d3eac58db615f3903fd82d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:49 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:49 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:49 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:49 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:49 GMT
ARG VERSION=25.8.16.34
# Tue, 17 Feb 2026 20:11:49 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:18 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:18 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e105b5258b6287684da632f28c009bead56d72476c38c18b71037e43e8e9b7c`  
		Last Modified: Tue, 17 Feb 2026 20:12:39 GMT  
		Size: 7.6 MB (7577435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494d420eedbfb97f76c475c4139188424ad202fa0e076dcced2c2495768b59ac`  
		Last Modified: Tue, 17 Feb 2026 20:12:41 GMT  
		Size: 178.0 MB (178016046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c477e7fcc96d3a9fe18cfd60a3109816b4a377d41bfdb46d3e0a3438fd193976`  
		Last Modified: Tue, 17 Feb 2026 20:12:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56a0a0e8730d6ac8153fd30fc3f7dc73e6e5160fa253c8ffa137dbdb06914b4`  
		Last Modified: Tue, 17 Feb 2026 20:12:37 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55e4b063f018d389136b40b857059bb4e1bb4f5af6046376bb9edfcad0241ff`  
		Last Modified: Tue, 17 Feb 2026 20:12:38 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ac4fd6f889704ea3b167cbbc7b274f8178ae69d00df70debe3e214aa936b13`  
		Last Modified: Tue, 17 Feb 2026 20:12:38 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff96f921752d4141c565ccca7e44ec7c882d09ac1601be61a0997273ce77657c`  
		Last Modified: Tue, 17 Feb 2026 20:12:40 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.16.34` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e40bf21f69748ff21ecb45294a3d5abada6026f07908ff61c72014db1bb06598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8a041960efb6f4644dde88a255c026fc5cac64f703efced83f24300b69ce680`

```dockerfile
```

-	Layers:
	-	`sha256:d61611774bdc1996895d1e9b295614f62dae75e1c939a7fb15d6abaa66d5a746`  
		Last Modified: Tue, 17 Feb 2026 20:12:37 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.16.34-jammy`

```console
$ docker pull clickhouse@sha256:cb8ea3c339aa84c1d75e0c9fc08f372e0398576caa3d787e7f27b9bbca483d3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.16.34-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:0ec0e053c41857406923f72d00580eac2b61fe11aff754672a9ed03f172c02c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228945044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5381324c8bcc3410608a9c899346d8806971bcef1a1a5fad7b59b6418415de5`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:26 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:12:26 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:12:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:12:26 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:12:26 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:12:26 GMT
ARG VERSION=25.8.16.34
# Tue, 17 Feb 2026 20:12:26 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:53 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:53 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:53 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820dee958d69ceaceb4ea57bc08fb7179f6c7e0987acf3a83c3fb4d05fecc5f2`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 7.6 MB (7598324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258567d60460abdf8fc0d705b07cfb5c2cf9c109302d7d2c766667ce48775f4c`  
		Last Modified: Tue, 17 Feb 2026 20:13:16 GMT  
		Size: 190.9 MB (190939334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e88afd8fd9b9d7dc8563b7db8a2a6351683c3b3e457879c7f4c041b98bff53e`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53900b96e71ca59796a1577140c2aea52ebe99495fc78ab718f66f89ce11fda`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b306d071c1343d8dc0c6d88a9a96ca5aa60bd057563577ae76fd30fbf89e8a3f`  
		Last Modified: Tue, 17 Feb 2026 20:13:13 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c6fbf6e82586a7efc880a4aa52b6e2c210259ad18c01db546ba7da838bd3af`  
		Last Modified: Tue, 17 Feb 2026 20:13:14 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9009d2f669d7bd059ba402b69f6770efd463c0a1f88b6c0a81fce2aa343e61b`  
		Last Modified: Tue, 17 Feb 2026 20:13:14 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.16.34-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0f00e22ef556b57f9002953ccb230258a724d206ddecc96ddef872a1715c4cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b864971555410cf3c7ecd8e15f929470ad3e6751db3fb535b698bb37a50e09a9`

```dockerfile
```

-	Layers:
	-	`sha256:b03ea5c9cfa2f868003976091441edbc705a684639b36b3607bd13f9e0fa5a85`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.16.34-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:2bc2d567de72e07f96d39d437aa8ad8c85de7d62d947633c5197d97d05e3603b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213848446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6a020363e23f68ae53ea85f8d5889d92a049d464d3eac58db615f3903fd82d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:49 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:49 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:49 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:49 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:49 GMT
ARG VERSION=25.8.16.34
# Tue, 17 Feb 2026 20:11:49 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:18 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:18 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e105b5258b6287684da632f28c009bead56d72476c38c18b71037e43e8e9b7c`  
		Last Modified: Tue, 17 Feb 2026 20:12:39 GMT  
		Size: 7.6 MB (7577435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494d420eedbfb97f76c475c4139188424ad202fa0e076dcced2c2495768b59ac`  
		Last Modified: Tue, 17 Feb 2026 20:12:41 GMT  
		Size: 178.0 MB (178016046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c477e7fcc96d3a9fe18cfd60a3109816b4a377d41bfdb46d3e0a3438fd193976`  
		Last Modified: Tue, 17 Feb 2026 20:12:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56a0a0e8730d6ac8153fd30fc3f7dc73e6e5160fa253c8ffa137dbdb06914b4`  
		Last Modified: Tue, 17 Feb 2026 20:12:37 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55e4b063f018d389136b40b857059bb4e1bb4f5af6046376bb9edfcad0241ff`  
		Last Modified: Tue, 17 Feb 2026 20:12:38 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ac4fd6f889704ea3b167cbbc7b274f8178ae69d00df70debe3e214aa936b13`  
		Last Modified: Tue, 17 Feb 2026 20:12:38 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff96f921752d4141c565ccca7e44ec7c882d09ac1601be61a0997273ce77657c`  
		Last Modified: Tue, 17 Feb 2026 20:12:40 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.16.34-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e40bf21f69748ff21ecb45294a3d5abada6026f07908ff61c72014db1bb06598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8a041960efb6f4644dde88a255c026fc5cac64f703efced83f24300b69ce680`

```dockerfile
```

-	Layers:
	-	`sha256:d61611774bdc1996895d1e9b295614f62dae75e1c939a7fb15d6abaa66d5a746`  
		Last Modified: Tue, 17 Feb 2026 20:12:37 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1`

```console
$ docker pull clickhouse@sha256:9f5b8b6dc95a25ef0129364f57b58ba621c76d6e551b4acd3b3f7d4d07fccaec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1` - linux; amd64

```console
$ docker pull clickhouse@sha256:326a3eca32eb99b3ccc9060c986d1a1224ccf7c100267d6be9afd91101b2f2a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (246010815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8c12f754b92a416f907484e935779f5f778ab7840b980c3937026b337e43e1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 20 Feb 2026 18:56:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Feb 2026 18:56:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Feb 2026 18:56:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Feb 2026 18:56:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Feb 2026 18:56:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Feb 2026 18:56:04 GMT
ARG VERSION=26.1.3.52
# Fri, 20 Feb 2026 18:56:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Feb 2026 18:56:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:56:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Feb 2026 18:56:35 GMT
ENV TZ=UTC
# Fri, 20 Feb 2026 18:56:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Feb 2026 18:56:35 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Feb 2026 18:56:35 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Feb 2026 18:56:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5034c143169a9ba01dd52c520d8113e75c347d9bfcda66d60c09c2a7a6531c39`  
		Last Modified: Fri, 20 Feb 2026 18:56:59 GMT  
		Size: 7.6 MB (7598331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1145cc277ba96ce39c3f4525c888b1be3a8da6c8c96ccd98e306146fad16afdc`  
		Last Modified: Fri, 20 Feb 2026 18:57:03 GMT  
		Size: 208.0 MB (208005070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b476bac4fb9d16cf0ebb80d913c0e6b758b7831ca00680e1a1af8367d66abd97`  
		Last Modified: Fri, 20 Feb 2026 18:56:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93015ce7d4331c21cf738d4ff889c7061d10dd88481965e8b2c2d777bb0aaac9`  
		Last Modified: Fri, 20 Feb 2026 18:56:58 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6dea9a16d676ac8b2f04a0e4b2c1fcc669e8439f07afca92112de02173b9733`  
		Last Modified: Fri, 20 Feb 2026 18:56:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954a25eea9d780f60c30dea1ce2c102f62345da96141fc377fbda846c994d071`  
		Last Modified: Fri, 20 Feb 2026 18:57:00 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83276a6ada13df074d0c737bd36861bd08e765b2284abb31e54e37b8f8de7c8b`  
		Last Modified: Fri, 20 Feb 2026 18:56:51 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f07f33f7d20fdc08fdf65ae7e9b62f6e946331082daed4bd440ae1f180e4625d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c518a0ba598b5762bb4826580257f12b55dc0b92000fab2c18f7436ede414171`

```dockerfile
```

-	Layers:
	-	`sha256:7bf60e3a6a48827be391e6b8c3ef6174877e55410603e110494fb540180fcf27`  
		Last Modified: Fri, 20 Feb 2026 18:56:58 GMT  
		Size: 26.0 KB (26028 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:be365b3a81b62d7d3f21c68e51c62c3870ea37f7c9fcc94cf099919af7f0fc15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228214491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80f7ffeb89eeffa280e608c7798a22bbef8d54fc8ea4a3af02dbe91a2e2d657b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Fri, 20 Feb 2026 18:56:06 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Feb 2026 18:56:06 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Feb 2026 18:56:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Feb 2026 18:56:06 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Feb 2026 18:56:06 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Feb 2026 18:56:06 GMT
ARG VERSION=26.1.3.52
# Fri, 20 Feb 2026 18:56:06 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Feb 2026 18:56:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:56:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Feb 2026 18:56:35 GMT
ENV TZ=UTC
# Fri, 20 Feb 2026 18:56:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Feb 2026 18:56:35 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Feb 2026 18:56:35 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Feb 2026 18:56:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ddda68ab08dc984109a23de1a2466e333e45ed21633b824db1aa90595410ffd`  
		Last Modified: Fri, 20 Feb 2026 18:56:55 GMT  
		Size: 7.6 MB (7577563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ec5baf43f2c14fd49b5df0cdc87f99fbbcd832212a492750feff736a5e5106`  
		Last Modified: Fri, 20 Feb 2026 18:56:59 GMT  
		Size: 192.4 MB (192381932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad9a04319b22315f9b9acde116065a30bc6a7f3892535799846fd320800a5c1`  
		Last Modified: Fri, 20 Feb 2026 18:56:55 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4c78b264d0d65b227b08e5711cb6d7947d2b2d8d1c801395a47d6ba78b464b`  
		Last Modified: Fri, 20 Feb 2026 18:56:55 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6dea9a16d676ac8b2f04a0e4b2c1fcc669e8439f07afca92112de02173b9733`  
		Last Modified: Fri, 20 Feb 2026 18:56:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e540ae5bc62cff0e6735ea5cd710e794eb0d9e59add1c8d1a1ef6fc30b76fd`  
		Last Modified: Fri, 20 Feb 2026 18:56:56 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8712bf0ecbbbe42456fa5f461add3c00f5153e81f95d0bc75d6351724aafdb`  
		Last Modified: Fri, 20 Feb 2026 18:56:56 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5944b0c47919209a5352044d8030c590d410be81753a240eb7453c7ead479842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65e5cc5faf34e95c7e8bccb3491878f2c51ad549370b4673f38e1842dd6c3b6e`

```dockerfile
```

-	Layers:
	-	`sha256:be0f32a0c65a008a58d760580d930bf3450bc62730ba56cab6fc2e6f0c498237`  
		Last Modified: Fri, 20 Feb 2026 18:56:55 GMT  
		Size: 26.2 KB (26238 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1-jammy`

```console
$ docker pull clickhouse@sha256:9f5b8b6dc95a25ef0129364f57b58ba621c76d6e551b4acd3b3f7d4d07fccaec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:326a3eca32eb99b3ccc9060c986d1a1224ccf7c100267d6be9afd91101b2f2a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (246010815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8c12f754b92a416f907484e935779f5f778ab7840b980c3937026b337e43e1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 20 Feb 2026 18:56:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Feb 2026 18:56:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Feb 2026 18:56:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Feb 2026 18:56:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Feb 2026 18:56:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Feb 2026 18:56:04 GMT
ARG VERSION=26.1.3.52
# Fri, 20 Feb 2026 18:56:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Feb 2026 18:56:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:56:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Feb 2026 18:56:35 GMT
ENV TZ=UTC
# Fri, 20 Feb 2026 18:56:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Feb 2026 18:56:35 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Feb 2026 18:56:35 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Feb 2026 18:56:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5034c143169a9ba01dd52c520d8113e75c347d9bfcda66d60c09c2a7a6531c39`  
		Last Modified: Fri, 20 Feb 2026 18:56:59 GMT  
		Size: 7.6 MB (7598331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1145cc277ba96ce39c3f4525c888b1be3a8da6c8c96ccd98e306146fad16afdc`  
		Last Modified: Fri, 20 Feb 2026 18:57:03 GMT  
		Size: 208.0 MB (208005070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b476bac4fb9d16cf0ebb80d913c0e6b758b7831ca00680e1a1af8367d66abd97`  
		Last Modified: Fri, 20 Feb 2026 18:56:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93015ce7d4331c21cf738d4ff889c7061d10dd88481965e8b2c2d777bb0aaac9`  
		Last Modified: Fri, 20 Feb 2026 18:56:58 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6dea9a16d676ac8b2f04a0e4b2c1fcc669e8439f07afca92112de02173b9733`  
		Last Modified: Fri, 20 Feb 2026 18:56:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954a25eea9d780f60c30dea1ce2c102f62345da96141fc377fbda846c994d071`  
		Last Modified: Fri, 20 Feb 2026 18:57:00 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83276a6ada13df074d0c737bd36861bd08e765b2284abb31e54e37b8f8de7c8b`  
		Last Modified: Fri, 20 Feb 2026 18:56:51 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f07f33f7d20fdc08fdf65ae7e9b62f6e946331082daed4bd440ae1f180e4625d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c518a0ba598b5762bb4826580257f12b55dc0b92000fab2c18f7436ede414171`

```dockerfile
```

-	Layers:
	-	`sha256:7bf60e3a6a48827be391e6b8c3ef6174877e55410603e110494fb540180fcf27`  
		Last Modified: Fri, 20 Feb 2026 18:56:58 GMT  
		Size: 26.0 KB (26028 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:be365b3a81b62d7d3f21c68e51c62c3870ea37f7c9fcc94cf099919af7f0fc15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228214491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80f7ffeb89eeffa280e608c7798a22bbef8d54fc8ea4a3af02dbe91a2e2d657b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Fri, 20 Feb 2026 18:56:06 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Feb 2026 18:56:06 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Feb 2026 18:56:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Feb 2026 18:56:06 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Feb 2026 18:56:06 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Feb 2026 18:56:06 GMT
ARG VERSION=26.1.3.52
# Fri, 20 Feb 2026 18:56:06 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Feb 2026 18:56:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:56:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Feb 2026 18:56:35 GMT
ENV TZ=UTC
# Fri, 20 Feb 2026 18:56:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Feb 2026 18:56:35 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Feb 2026 18:56:35 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Feb 2026 18:56:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ddda68ab08dc984109a23de1a2466e333e45ed21633b824db1aa90595410ffd`  
		Last Modified: Fri, 20 Feb 2026 18:56:55 GMT  
		Size: 7.6 MB (7577563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ec5baf43f2c14fd49b5df0cdc87f99fbbcd832212a492750feff736a5e5106`  
		Last Modified: Fri, 20 Feb 2026 18:56:59 GMT  
		Size: 192.4 MB (192381932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad9a04319b22315f9b9acde116065a30bc6a7f3892535799846fd320800a5c1`  
		Last Modified: Fri, 20 Feb 2026 18:56:55 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4c78b264d0d65b227b08e5711cb6d7947d2b2d8d1c801395a47d6ba78b464b`  
		Last Modified: Fri, 20 Feb 2026 18:56:55 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6dea9a16d676ac8b2f04a0e4b2c1fcc669e8439f07afca92112de02173b9733`  
		Last Modified: Fri, 20 Feb 2026 18:56:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e540ae5bc62cff0e6735ea5cd710e794eb0d9e59add1c8d1a1ef6fc30b76fd`  
		Last Modified: Fri, 20 Feb 2026 18:56:56 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8712bf0ecbbbe42456fa5f461add3c00f5153e81f95d0bc75d6351724aafdb`  
		Last Modified: Fri, 20 Feb 2026 18:56:56 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5944b0c47919209a5352044d8030c590d410be81753a240eb7453c7ead479842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65e5cc5faf34e95c7e8bccb3491878f2c51ad549370b4673f38e1842dd6c3b6e`

```dockerfile
```

-	Layers:
	-	`sha256:be0f32a0c65a008a58d760580d930bf3450bc62730ba56cab6fc2e6f0c498237`  
		Last Modified: Fri, 20 Feb 2026 18:56:55 GMT  
		Size: 26.2 KB (26238 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1.3`

```console
$ docker pull clickhouse@sha256:9f5b8b6dc95a25ef0129364f57b58ba621c76d6e551b4acd3b3f7d4d07fccaec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:326a3eca32eb99b3ccc9060c986d1a1224ccf7c100267d6be9afd91101b2f2a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (246010815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8c12f754b92a416f907484e935779f5f778ab7840b980c3937026b337e43e1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 20 Feb 2026 18:56:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Feb 2026 18:56:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Feb 2026 18:56:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Feb 2026 18:56:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Feb 2026 18:56:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Feb 2026 18:56:04 GMT
ARG VERSION=26.1.3.52
# Fri, 20 Feb 2026 18:56:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Feb 2026 18:56:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:56:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Feb 2026 18:56:35 GMT
ENV TZ=UTC
# Fri, 20 Feb 2026 18:56:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Feb 2026 18:56:35 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Feb 2026 18:56:35 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Feb 2026 18:56:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5034c143169a9ba01dd52c520d8113e75c347d9bfcda66d60c09c2a7a6531c39`  
		Last Modified: Fri, 20 Feb 2026 18:56:59 GMT  
		Size: 7.6 MB (7598331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1145cc277ba96ce39c3f4525c888b1be3a8da6c8c96ccd98e306146fad16afdc`  
		Last Modified: Fri, 20 Feb 2026 18:57:03 GMT  
		Size: 208.0 MB (208005070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b476bac4fb9d16cf0ebb80d913c0e6b758b7831ca00680e1a1af8367d66abd97`  
		Last Modified: Fri, 20 Feb 2026 18:56:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93015ce7d4331c21cf738d4ff889c7061d10dd88481965e8b2c2d777bb0aaac9`  
		Last Modified: Fri, 20 Feb 2026 18:56:58 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6dea9a16d676ac8b2f04a0e4b2c1fcc669e8439f07afca92112de02173b9733`  
		Last Modified: Fri, 20 Feb 2026 18:56:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954a25eea9d780f60c30dea1ce2c102f62345da96141fc377fbda846c994d071`  
		Last Modified: Fri, 20 Feb 2026 18:57:00 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83276a6ada13df074d0c737bd36861bd08e765b2284abb31e54e37b8f8de7c8b`  
		Last Modified: Fri, 20 Feb 2026 18:56:51 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f07f33f7d20fdc08fdf65ae7e9b62f6e946331082daed4bd440ae1f180e4625d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c518a0ba598b5762bb4826580257f12b55dc0b92000fab2c18f7436ede414171`

```dockerfile
```

-	Layers:
	-	`sha256:7bf60e3a6a48827be391e6b8c3ef6174877e55410603e110494fb540180fcf27`  
		Last Modified: Fri, 20 Feb 2026 18:56:58 GMT  
		Size: 26.0 KB (26028 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:be365b3a81b62d7d3f21c68e51c62c3870ea37f7c9fcc94cf099919af7f0fc15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228214491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80f7ffeb89eeffa280e608c7798a22bbef8d54fc8ea4a3af02dbe91a2e2d657b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Fri, 20 Feb 2026 18:56:06 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Feb 2026 18:56:06 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Feb 2026 18:56:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Feb 2026 18:56:06 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Feb 2026 18:56:06 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Feb 2026 18:56:06 GMT
ARG VERSION=26.1.3.52
# Fri, 20 Feb 2026 18:56:06 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Feb 2026 18:56:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:56:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Feb 2026 18:56:35 GMT
ENV TZ=UTC
# Fri, 20 Feb 2026 18:56:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Feb 2026 18:56:35 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Feb 2026 18:56:35 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Feb 2026 18:56:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ddda68ab08dc984109a23de1a2466e333e45ed21633b824db1aa90595410ffd`  
		Last Modified: Fri, 20 Feb 2026 18:56:55 GMT  
		Size: 7.6 MB (7577563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ec5baf43f2c14fd49b5df0cdc87f99fbbcd832212a492750feff736a5e5106`  
		Last Modified: Fri, 20 Feb 2026 18:56:59 GMT  
		Size: 192.4 MB (192381932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad9a04319b22315f9b9acde116065a30bc6a7f3892535799846fd320800a5c1`  
		Last Modified: Fri, 20 Feb 2026 18:56:55 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4c78b264d0d65b227b08e5711cb6d7947d2b2d8d1c801395a47d6ba78b464b`  
		Last Modified: Fri, 20 Feb 2026 18:56:55 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6dea9a16d676ac8b2f04a0e4b2c1fcc669e8439f07afca92112de02173b9733`  
		Last Modified: Fri, 20 Feb 2026 18:56:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e540ae5bc62cff0e6735ea5cd710e794eb0d9e59add1c8d1a1ef6fc30b76fd`  
		Last Modified: Fri, 20 Feb 2026 18:56:56 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8712bf0ecbbbe42456fa5f461add3c00f5153e81f95d0bc75d6351724aafdb`  
		Last Modified: Fri, 20 Feb 2026 18:56:56 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5944b0c47919209a5352044d8030c590d410be81753a240eb7453c7ead479842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65e5cc5faf34e95c7e8bccb3491878f2c51ad549370b4673f38e1842dd6c3b6e`

```dockerfile
```

-	Layers:
	-	`sha256:be0f32a0c65a008a58d760580d930bf3450bc62730ba56cab6fc2e6f0c498237`  
		Last Modified: Fri, 20 Feb 2026 18:56:55 GMT  
		Size: 26.2 KB (26238 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1.3-jammy`

```console
$ docker pull clickhouse@sha256:9f5b8b6dc95a25ef0129364f57b58ba621c76d6e551b4acd3b3f7d4d07fccaec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1.3-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:326a3eca32eb99b3ccc9060c986d1a1224ccf7c100267d6be9afd91101b2f2a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (246010815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8c12f754b92a416f907484e935779f5f778ab7840b980c3937026b337e43e1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 20 Feb 2026 18:56:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Feb 2026 18:56:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Feb 2026 18:56:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Feb 2026 18:56:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Feb 2026 18:56:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Feb 2026 18:56:04 GMT
ARG VERSION=26.1.3.52
# Fri, 20 Feb 2026 18:56:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Feb 2026 18:56:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:56:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Feb 2026 18:56:35 GMT
ENV TZ=UTC
# Fri, 20 Feb 2026 18:56:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Feb 2026 18:56:35 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Feb 2026 18:56:35 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Feb 2026 18:56:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5034c143169a9ba01dd52c520d8113e75c347d9bfcda66d60c09c2a7a6531c39`  
		Last Modified: Fri, 20 Feb 2026 18:56:59 GMT  
		Size: 7.6 MB (7598331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1145cc277ba96ce39c3f4525c888b1be3a8da6c8c96ccd98e306146fad16afdc`  
		Last Modified: Fri, 20 Feb 2026 18:57:03 GMT  
		Size: 208.0 MB (208005070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b476bac4fb9d16cf0ebb80d913c0e6b758b7831ca00680e1a1af8367d66abd97`  
		Last Modified: Fri, 20 Feb 2026 18:56:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93015ce7d4331c21cf738d4ff889c7061d10dd88481965e8b2c2d777bb0aaac9`  
		Last Modified: Fri, 20 Feb 2026 18:56:58 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6dea9a16d676ac8b2f04a0e4b2c1fcc669e8439f07afca92112de02173b9733`  
		Last Modified: Fri, 20 Feb 2026 18:56:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954a25eea9d780f60c30dea1ce2c102f62345da96141fc377fbda846c994d071`  
		Last Modified: Fri, 20 Feb 2026 18:57:00 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83276a6ada13df074d0c737bd36861bd08e765b2284abb31e54e37b8f8de7c8b`  
		Last Modified: Fri, 20 Feb 2026 18:56:51 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f07f33f7d20fdc08fdf65ae7e9b62f6e946331082daed4bd440ae1f180e4625d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c518a0ba598b5762bb4826580257f12b55dc0b92000fab2c18f7436ede414171`

```dockerfile
```

-	Layers:
	-	`sha256:7bf60e3a6a48827be391e6b8c3ef6174877e55410603e110494fb540180fcf27`  
		Last Modified: Fri, 20 Feb 2026 18:56:58 GMT  
		Size: 26.0 KB (26028 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1.3-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:be365b3a81b62d7d3f21c68e51c62c3870ea37f7c9fcc94cf099919af7f0fc15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228214491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80f7ffeb89eeffa280e608c7798a22bbef8d54fc8ea4a3af02dbe91a2e2d657b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Fri, 20 Feb 2026 18:56:06 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Feb 2026 18:56:06 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Feb 2026 18:56:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Feb 2026 18:56:06 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Feb 2026 18:56:06 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Feb 2026 18:56:06 GMT
ARG VERSION=26.1.3.52
# Fri, 20 Feb 2026 18:56:06 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Feb 2026 18:56:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:56:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Feb 2026 18:56:35 GMT
ENV TZ=UTC
# Fri, 20 Feb 2026 18:56:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Feb 2026 18:56:35 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Feb 2026 18:56:35 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Feb 2026 18:56:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ddda68ab08dc984109a23de1a2466e333e45ed21633b824db1aa90595410ffd`  
		Last Modified: Fri, 20 Feb 2026 18:56:55 GMT  
		Size: 7.6 MB (7577563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ec5baf43f2c14fd49b5df0cdc87f99fbbcd832212a492750feff736a5e5106`  
		Last Modified: Fri, 20 Feb 2026 18:56:59 GMT  
		Size: 192.4 MB (192381932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad9a04319b22315f9b9acde116065a30bc6a7f3892535799846fd320800a5c1`  
		Last Modified: Fri, 20 Feb 2026 18:56:55 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4c78b264d0d65b227b08e5711cb6d7947d2b2d8d1c801395a47d6ba78b464b`  
		Last Modified: Fri, 20 Feb 2026 18:56:55 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6dea9a16d676ac8b2f04a0e4b2c1fcc669e8439f07afca92112de02173b9733`  
		Last Modified: Fri, 20 Feb 2026 18:56:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e540ae5bc62cff0e6735ea5cd710e794eb0d9e59add1c8d1a1ef6fc30b76fd`  
		Last Modified: Fri, 20 Feb 2026 18:56:56 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8712bf0ecbbbe42456fa5f461add3c00f5153e81f95d0bc75d6351724aafdb`  
		Last Modified: Fri, 20 Feb 2026 18:56:56 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5944b0c47919209a5352044d8030c590d410be81753a240eb7453c7ead479842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65e5cc5faf34e95c7e8bccb3491878f2c51ad549370b4673f38e1842dd6c3b6e`

```dockerfile
```

-	Layers:
	-	`sha256:be0f32a0c65a008a58d760580d930bf3450bc62730ba56cab6fc2e6f0c498237`  
		Last Modified: Fri, 20 Feb 2026 18:56:55 GMT  
		Size: 26.2 KB (26238 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1.3.52`

```console
$ docker pull clickhouse@sha256:9f5b8b6dc95a25ef0129364f57b58ba621c76d6e551b4acd3b3f7d4d07fccaec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1.3.52` - linux; amd64

```console
$ docker pull clickhouse@sha256:326a3eca32eb99b3ccc9060c986d1a1224ccf7c100267d6be9afd91101b2f2a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (246010815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8c12f754b92a416f907484e935779f5f778ab7840b980c3937026b337e43e1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 20 Feb 2026 18:56:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Feb 2026 18:56:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Feb 2026 18:56:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Feb 2026 18:56:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Feb 2026 18:56:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Feb 2026 18:56:04 GMT
ARG VERSION=26.1.3.52
# Fri, 20 Feb 2026 18:56:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Feb 2026 18:56:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:56:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Feb 2026 18:56:35 GMT
ENV TZ=UTC
# Fri, 20 Feb 2026 18:56:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Feb 2026 18:56:35 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Feb 2026 18:56:35 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Feb 2026 18:56:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5034c143169a9ba01dd52c520d8113e75c347d9bfcda66d60c09c2a7a6531c39`  
		Last Modified: Fri, 20 Feb 2026 18:56:59 GMT  
		Size: 7.6 MB (7598331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1145cc277ba96ce39c3f4525c888b1be3a8da6c8c96ccd98e306146fad16afdc`  
		Last Modified: Fri, 20 Feb 2026 18:57:03 GMT  
		Size: 208.0 MB (208005070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b476bac4fb9d16cf0ebb80d913c0e6b758b7831ca00680e1a1af8367d66abd97`  
		Last Modified: Fri, 20 Feb 2026 18:56:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93015ce7d4331c21cf738d4ff889c7061d10dd88481965e8b2c2d777bb0aaac9`  
		Last Modified: Fri, 20 Feb 2026 18:56:58 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6dea9a16d676ac8b2f04a0e4b2c1fcc669e8439f07afca92112de02173b9733`  
		Last Modified: Fri, 20 Feb 2026 18:56:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954a25eea9d780f60c30dea1ce2c102f62345da96141fc377fbda846c994d071`  
		Last Modified: Fri, 20 Feb 2026 18:57:00 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83276a6ada13df074d0c737bd36861bd08e765b2284abb31e54e37b8f8de7c8b`  
		Last Modified: Fri, 20 Feb 2026 18:56:51 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.3.52` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f07f33f7d20fdc08fdf65ae7e9b62f6e946331082daed4bd440ae1f180e4625d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c518a0ba598b5762bb4826580257f12b55dc0b92000fab2c18f7436ede414171`

```dockerfile
```

-	Layers:
	-	`sha256:7bf60e3a6a48827be391e6b8c3ef6174877e55410603e110494fb540180fcf27`  
		Last Modified: Fri, 20 Feb 2026 18:56:58 GMT  
		Size: 26.0 KB (26028 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1.3.52` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:be365b3a81b62d7d3f21c68e51c62c3870ea37f7c9fcc94cf099919af7f0fc15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228214491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80f7ffeb89eeffa280e608c7798a22bbef8d54fc8ea4a3af02dbe91a2e2d657b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Fri, 20 Feb 2026 18:56:06 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Feb 2026 18:56:06 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Feb 2026 18:56:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Feb 2026 18:56:06 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Feb 2026 18:56:06 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Feb 2026 18:56:06 GMT
ARG VERSION=26.1.3.52
# Fri, 20 Feb 2026 18:56:06 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Feb 2026 18:56:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:56:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Feb 2026 18:56:35 GMT
ENV TZ=UTC
# Fri, 20 Feb 2026 18:56:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Feb 2026 18:56:35 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Feb 2026 18:56:35 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Feb 2026 18:56:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ddda68ab08dc984109a23de1a2466e333e45ed21633b824db1aa90595410ffd`  
		Last Modified: Fri, 20 Feb 2026 18:56:55 GMT  
		Size: 7.6 MB (7577563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ec5baf43f2c14fd49b5df0cdc87f99fbbcd832212a492750feff736a5e5106`  
		Last Modified: Fri, 20 Feb 2026 18:56:59 GMT  
		Size: 192.4 MB (192381932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad9a04319b22315f9b9acde116065a30bc6a7f3892535799846fd320800a5c1`  
		Last Modified: Fri, 20 Feb 2026 18:56:55 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4c78b264d0d65b227b08e5711cb6d7947d2b2d8d1c801395a47d6ba78b464b`  
		Last Modified: Fri, 20 Feb 2026 18:56:55 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6dea9a16d676ac8b2f04a0e4b2c1fcc669e8439f07afca92112de02173b9733`  
		Last Modified: Fri, 20 Feb 2026 18:56:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e540ae5bc62cff0e6735ea5cd710e794eb0d9e59add1c8d1a1ef6fc30b76fd`  
		Last Modified: Fri, 20 Feb 2026 18:56:56 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8712bf0ecbbbe42456fa5f461add3c00f5153e81f95d0bc75d6351724aafdb`  
		Last Modified: Fri, 20 Feb 2026 18:56:56 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.3.52` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5944b0c47919209a5352044d8030c590d410be81753a240eb7453c7ead479842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65e5cc5faf34e95c7e8bccb3491878f2c51ad549370b4673f38e1842dd6c3b6e`

```dockerfile
```

-	Layers:
	-	`sha256:be0f32a0c65a008a58d760580d930bf3450bc62730ba56cab6fc2e6f0c498237`  
		Last Modified: Fri, 20 Feb 2026 18:56:55 GMT  
		Size: 26.2 KB (26238 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1.3.52-jammy`

```console
$ docker pull clickhouse@sha256:9f5b8b6dc95a25ef0129364f57b58ba621c76d6e551b4acd3b3f7d4d07fccaec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1.3.52-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:326a3eca32eb99b3ccc9060c986d1a1224ccf7c100267d6be9afd91101b2f2a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (246010815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8c12f754b92a416f907484e935779f5f778ab7840b980c3937026b337e43e1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 20 Feb 2026 18:56:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Feb 2026 18:56:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Feb 2026 18:56:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Feb 2026 18:56:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Feb 2026 18:56:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Feb 2026 18:56:04 GMT
ARG VERSION=26.1.3.52
# Fri, 20 Feb 2026 18:56:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Feb 2026 18:56:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:56:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Feb 2026 18:56:35 GMT
ENV TZ=UTC
# Fri, 20 Feb 2026 18:56:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Feb 2026 18:56:35 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Feb 2026 18:56:35 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Feb 2026 18:56:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5034c143169a9ba01dd52c520d8113e75c347d9bfcda66d60c09c2a7a6531c39`  
		Last Modified: Fri, 20 Feb 2026 18:56:59 GMT  
		Size: 7.6 MB (7598331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1145cc277ba96ce39c3f4525c888b1be3a8da6c8c96ccd98e306146fad16afdc`  
		Last Modified: Fri, 20 Feb 2026 18:57:03 GMT  
		Size: 208.0 MB (208005070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b476bac4fb9d16cf0ebb80d913c0e6b758b7831ca00680e1a1af8367d66abd97`  
		Last Modified: Fri, 20 Feb 2026 18:56:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93015ce7d4331c21cf738d4ff889c7061d10dd88481965e8b2c2d777bb0aaac9`  
		Last Modified: Fri, 20 Feb 2026 18:56:58 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6dea9a16d676ac8b2f04a0e4b2c1fcc669e8439f07afca92112de02173b9733`  
		Last Modified: Fri, 20 Feb 2026 18:56:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954a25eea9d780f60c30dea1ce2c102f62345da96141fc377fbda846c994d071`  
		Last Modified: Fri, 20 Feb 2026 18:57:00 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83276a6ada13df074d0c737bd36861bd08e765b2284abb31e54e37b8f8de7c8b`  
		Last Modified: Fri, 20 Feb 2026 18:56:51 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.3.52-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f07f33f7d20fdc08fdf65ae7e9b62f6e946331082daed4bd440ae1f180e4625d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c518a0ba598b5762bb4826580257f12b55dc0b92000fab2c18f7436ede414171`

```dockerfile
```

-	Layers:
	-	`sha256:7bf60e3a6a48827be391e6b8c3ef6174877e55410603e110494fb540180fcf27`  
		Last Modified: Fri, 20 Feb 2026 18:56:58 GMT  
		Size: 26.0 KB (26028 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1.3.52-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:be365b3a81b62d7d3f21c68e51c62c3870ea37f7c9fcc94cf099919af7f0fc15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228214491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80f7ffeb89eeffa280e608c7798a22bbef8d54fc8ea4a3af02dbe91a2e2d657b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Fri, 20 Feb 2026 18:56:06 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Feb 2026 18:56:06 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Feb 2026 18:56:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Feb 2026 18:56:06 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Feb 2026 18:56:06 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Feb 2026 18:56:06 GMT
ARG VERSION=26.1.3.52
# Fri, 20 Feb 2026 18:56:06 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Feb 2026 18:56:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:56:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Feb 2026 18:56:35 GMT
ENV TZ=UTC
# Fri, 20 Feb 2026 18:56:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Feb 2026 18:56:35 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Feb 2026 18:56:35 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Feb 2026 18:56:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ddda68ab08dc984109a23de1a2466e333e45ed21633b824db1aa90595410ffd`  
		Last Modified: Fri, 20 Feb 2026 18:56:55 GMT  
		Size: 7.6 MB (7577563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ec5baf43f2c14fd49b5df0cdc87f99fbbcd832212a492750feff736a5e5106`  
		Last Modified: Fri, 20 Feb 2026 18:56:59 GMT  
		Size: 192.4 MB (192381932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad9a04319b22315f9b9acde116065a30bc6a7f3892535799846fd320800a5c1`  
		Last Modified: Fri, 20 Feb 2026 18:56:55 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4c78b264d0d65b227b08e5711cb6d7947d2b2d8d1c801395a47d6ba78b464b`  
		Last Modified: Fri, 20 Feb 2026 18:56:55 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6dea9a16d676ac8b2f04a0e4b2c1fcc669e8439f07afca92112de02173b9733`  
		Last Modified: Fri, 20 Feb 2026 18:56:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e540ae5bc62cff0e6735ea5cd710e794eb0d9e59add1c8d1a1ef6fc30b76fd`  
		Last Modified: Fri, 20 Feb 2026 18:56:56 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8712bf0ecbbbe42456fa5f461add3c00f5153e81f95d0bc75d6351724aafdb`  
		Last Modified: Fri, 20 Feb 2026 18:56:56 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.3.52-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5944b0c47919209a5352044d8030c590d410be81753a240eb7453c7ead479842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65e5cc5faf34e95c7e8bccb3491878f2c51ad549370b4673f38e1842dd6c3b6e`

```dockerfile
```

-	Layers:
	-	`sha256:be0f32a0c65a008a58d760580d930bf3450bc62730ba56cab6fc2e6f0c498237`  
		Last Modified: Fri, 20 Feb 2026 18:56:55 GMT  
		Size: 26.2 KB (26238 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:jammy`

```console
$ docker pull clickhouse@sha256:9f5b8b6dc95a25ef0129364f57b58ba621c76d6e551b4acd3b3f7d4d07fccaec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:326a3eca32eb99b3ccc9060c986d1a1224ccf7c100267d6be9afd91101b2f2a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (246010815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8c12f754b92a416f907484e935779f5f778ab7840b980c3937026b337e43e1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 20 Feb 2026 18:56:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Feb 2026 18:56:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Feb 2026 18:56:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Feb 2026 18:56:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Feb 2026 18:56:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Feb 2026 18:56:04 GMT
ARG VERSION=26.1.3.52
# Fri, 20 Feb 2026 18:56:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Feb 2026 18:56:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:56:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Feb 2026 18:56:35 GMT
ENV TZ=UTC
# Fri, 20 Feb 2026 18:56:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Feb 2026 18:56:35 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Feb 2026 18:56:35 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Feb 2026 18:56:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5034c143169a9ba01dd52c520d8113e75c347d9bfcda66d60c09c2a7a6531c39`  
		Last Modified: Fri, 20 Feb 2026 18:56:59 GMT  
		Size: 7.6 MB (7598331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1145cc277ba96ce39c3f4525c888b1be3a8da6c8c96ccd98e306146fad16afdc`  
		Last Modified: Fri, 20 Feb 2026 18:57:03 GMT  
		Size: 208.0 MB (208005070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b476bac4fb9d16cf0ebb80d913c0e6b758b7831ca00680e1a1af8367d66abd97`  
		Last Modified: Fri, 20 Feb 2026 18:56:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93015ce7d4331c21cf738d4ff889c7061d10dd88481965e8b2c2d777bb0aaac9`  
		Last Modified: Fri, 20 Feb 2026 18:56:58 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6dea9a16d676ac8b2f04a0e4b2c1fcc669e8439f07afca92112de02173b9733`  
		Last Modified: Fri, 20 Feb 2026 18:56:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954a25eea9d780f60c30dea1ce2c102f62345da96141fc377fbda846c994d071`  
		Last Modified: Fri, 20 Feb 2026 18:57:00 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83276a6ada13df074d0c737bd36861bd08e765b2284abb31e54e37b8f8de7c8b`  
		Last Modified: Fri, 20 Feb 2026 18:56:51 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f07f33f7d20fdc08fdf65ae7e9b62f6e946331082daed4bd440ae1f180e4625d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c518a0ba598b5762bb4826580257f12b55dc0b92000fab2c18f7436ede414171`

```dockerfile
```

-	Layers:
	-	`sha256:7bf60e3a6a48827be391e6b8c3ef6174877e55410603e110494fb540180fcf27`  
		Last Modified: Fri, 20 Feb 2026 18:56:58 GMT  
		Size: 26.0 KB (26028 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:be365b3a81b62d7d3f21c68e51c62c3870ea37f7c9fcc94cf099919af7f0fc15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228214491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80f7ffeb89eeffa280e608c7798a22bbef8d54fc8ea4a3af02dbe91a2e2d657b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Fri, 20 Feb 2026 18:56:06 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Feb 2026 18:56:06 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Feb 2026 18:56:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Feb 2026 18:56:06 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Feb 2026 18:56:06 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Feb 2026 18:56:06 GMT
ARG VERSION=26.1.3.52
# Fri, 20 Feb 2026 18:56:06 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Feb 2026 18:56:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:56:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Feb 2026 18:56:35 GMT
ENV TZ=UTC
# Fri, 20 Feb 2026 18:56:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Feb 2026 18:56:35 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Feb 2026 18:56:35 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Feb 2026 18:56:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ddda68ab08dc984109a23de1a2466e333e45ed21633b824db1aa90595410ffd`  
		Last Modified: Fri, 20 Feb 2026 18:56:55 GMT  
		Size: 7.6 MB (7577563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ec5baf43f2c14fd49b5df0cdc87f99fbbcd832212a492750feff736a5e5106`  
		Last Modified: Fri, 20 Feb 2026 18:56:59 GMT  
		Size: 192.4 MB (192381932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad9a04319b22315f9b9acde116065a30bc6a7f3892535799846fd320800a5c1`  
		Last Modified: Fri, 20 Feb 2026 18:56:55 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4c78b264d0d65b227b08e5711cb6d7947d2b2d8d1c801395a47d6ba78b464b`  
		Last Modified: Fri, 20 Feb 2026 18:56:55 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6dea9a16d676ac8b2f04a0e4b2c1fcc669e8439f07afca92112de02173b9733`  
		Last Modified: Fri, 20 Feb 2026 18:56:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e540ae5bc62cff0e6735ea5cd710e794eb0d9e59add1c8d1a1ef6fc30b76fd`  
		Last Modified: Fri, 20 Feb 2026 18:56:56 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8712bf0ecbbbe42456fa5f461add3c00f5153e81f95d0bc75d6351724aafdb`  
		Last Modified: Fri, 20 Feb 2026 18:56:56 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5944b0c47919209a5352044d8030c590d410be81753a240eb7453c7ead479842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65e5cc5faf34e95c7e8bccb3491878f2c51ad549370b4673f38e1842dd6c3b6e`

```dockerfile
```

-	Layers:
	-	`sha256:be0f32a0c65a008a58d760580d930bf3450bc62730ba56cab6fc2e6f0c498237`  
		Last Modified: Fri, 20 Feb 2026 18:56:55 GMT  
		Size: 26.2 KB (26238 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:9f5b8b6dc95a25ef0129364f57b58ba621c76d6e551b4acd3b3f7d4d07fccaec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

```console
$ docker pull clickhouse@sha256:326a3eca32eb99b3ccc9060c986d1a1224ccf7c100267d6be9afd91101b2f2a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (246010815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8c12f754b92a416f907484e935779f5f778ab7840b980c3937026b337e43e1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Fri, 20 Feb 2026 18:56:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Feb 2026 18:56:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Feb 2026 18:56:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Feb 2026 18:56:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Feb 2026 18:56:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Feb 2026 18:56:04 GMT
ARG VERSION=26.1.3.52
# Fri, 20 Feb 2026 18:56:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Feb 2026 18:56:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:56:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Feb 2026 18:56:35 GMT
ENV TZ=UTC
# Fri, 20 Feb 2026 18:56:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Feb 2026 18:56:35 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Feb 2026 18:56:35 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Feb 2026 18:56:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5034c143169a9ba01dd52c520d8113e75c347d9bfcda66d60c09c2a7a6531c39`  
		Last Modified: Fri, 20 Feb 2026 18:56:59 GMT  
		Size: 7.6 MB (7598331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1145cc277ba96ce39c3f4525c888b1be3a8da6c8c96ccd98e306146fad16afdc`  
		Last Modified: Fri, 20 Feb 2026 18:57:03 GMT  
		Size: 208.0 MB (208005070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b476bac4fb9d16cf0ebb80d913c0e6b758b7831ca00680e1a1af8367d66abd97`  
		Last Modified: Fri, 20 Feb 2026 18:56:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93015ce7d4331c21cf738d4ff889c7061d10dd88481965e8b2c2d777bb0aaac9`  
		Last Modified: Fri, 20 Feb 2026 18:56:58 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6dea9a16d676ac8b2f04a0e4b2c1fcc669e8439f07afca92112de02173b9733`  
		Last Modified: Fri, 20 Feb 2026 18:56:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954a25eea9d780f60c30dea1ce2c102f62345da96141fc377fbda846c994d071`  
		Last Modified: Fri, 20 Feb 2026 18:57:00 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83276a6ada13df074d0c737bd36861bd08e765b2284abb31e54e37b8f8de7c8b`  
		Last Modified: Fri, 20 Feb 2026 18:56:51 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f07f33f7d20fdc08fdf65ae7e9b62f6e946331082daed4bd440ae1f180e4625d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c518a0ba598b5762bb4826580257f12b55dc0b92000fab2c18f7436ede414171`

```dockerfile
```

-	Layers:
	-	`sha256:7bf60e3a6a48827be391e6b8c3ef6174877e55410603e110494fb540180fcf27`  
		Last Modified: Fri, 20 Feb 2026 18:56:58 GMT  
		Size: 26.0 KB (26028 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:be365b3a81b62d7d3f21c68e51c62c3870ea37f7c9fcc94cf099919af7f0fc15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228214491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80f7ffeb89eeffa280e608c7798a22bbef8d54fc8ea4a3af02dbe91a2e2d657b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Fri, 20 Feb 2026 18:56:06 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Feb 2026 18:56:06 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Feb 2026 18:56:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Feb 2026 18:56:06 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Feb 2026 18:56:06 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Feb 2026 18:56:06 GMT
ARG VERSION=26.1.3.52
# Fri, 20 Feb 2026 18:56:06 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Feb 2026 18:56:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:56:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Feb 2026 18:56:35 GMT
ENV TZ=UTC
# Fri, 20 Feb 2026 18:56:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Feb 2026 18:56:35 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Feb 2026 18:56:35 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Feb 2026 18:56:35 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Feb 2026 18:56:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ddda68ab08dc984109a23de1a2466e333e45ed21633b824db1aa90595410ffd`  
		Last Modified: Fri, 20 Feb 2026 18:56:55 GMT  
		Size: 7.6 MB (7577563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ec5baf43f2c14fd49b5df0cdc87f99fbbcd832212a492750feff736a5e5106`  
		Last Modified: Fri, 20 Feb 2026 18:56:59 GMT  
		Size: 192.4 MB (192381932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad9a04319b22315f9b9acde116065a30bc6a7f3892535799846fd320800a5c1`  
		Last Modified: Fri, 20 Feb 2026 18:56:55 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4c78b264d0d65b227b08e5711cb6d7947d2b2d8d1c801395a47d6ba78b464b`  
		Last Modified: Fri, 20 Feb 2026 18:56:55 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6dea9a16d676ac8b2f04a0e4b2c1fcc669e8439f07afca92112de02173b9733`  
		Last Modified: Fri, 20 Feb 2026 18:56:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e540ae5bc62cff0e6735ea5cd710e794eb0d9e59add1c8d1a1ef6fc30b76fd`  
		Last Modified: Fri, 20 Feb 2026 18:56:56 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8712bf0ecbbbe42456fa5f461add3c00f5153e81f95d0bc75d6351724aafdb`  
		Last Modified: Fri, 20 Feb 2026 18:56:56 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5944b0c47919209a5352044d8030c590d410be81753a240eb7453c7ead479842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65e5cc5faf34e95c7e8bccb3491878f2c51ad549370b4673f38e1842dd6c3b6e`

```dockerfile
```

-	Layers:
	-	`sha256:be0f32a0c65a008a58d760580d930bf3450bc62730ba56cab6fc2e6f0c498237`  
		Last Modified: Fri, 20 Feb 2026 18:56:55 GMT  
		Size: 26.2 KB (26238 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts`

```console
$ docker pull clickhouse@sha256:cb8ea3c339aa84c1d75e0c9fc08f372e0398576caa3d787e7f27b9bbca483d3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts` - linux; amd64

```console
$ docker pull clickhouse@sha256:0ec0e053c41857406923f72d00580eac2b61fe11aff754672a9ed03f172c02c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228945044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5381324c8bcc3410608a9c899346d8806971bcef1a1a5fad7b59b6418415de5`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:26 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:12:26 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:12:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:12:26 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:12:26 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:12:26 GMT
ARG VERSION=25.8.16.34
# Tue, 17 Feb 2026 20:12:26 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:53 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:53 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:53 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820dee958d69ceaceb4ea57bc08fb7179f6c7e0987acf3a83c3fb4d05fecc5f2`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 7.6 MB (7598324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258567d60460abdf8fc0d705b07cfb5c2cf9c109302d7d2c766667ce48775f4c`  
		Last Modified: Tue, 17 Feb 2026 20:13:16 GMT  
		Size: 190.9 MB (190939334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e88afd8fd9b9d7dc8563b7db8a2a6351683c3b3e457879c7f4c041b98bff53e`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53900b96e71ca59796a1577140c2aea52ebe99495fc78ab718f66f89ce11fda`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b306d071c1343d8dc0c6d88a9a96ca5aa60bd057563577ae76fd30fbf89e8a3f`  
		Last Modified: Tue, 17 Feb 2026 20:13:13 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c6fbf6e82586a7efc880a4aa52b6e2c210259ad18c01db546ba7da838bd3af`  
		Last Modified: Tue, 17 Feb 2026 20:13:14 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9009d2f669d7bd059ba402b69f6770efd463c0a1f88b6c0a81fce2aa343e61b`  
		Last Modified: Tue, 17 Feb 2026 20:13:14 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0f00e22ef556b57f9002953ccb230258a724d206ddecc96ddef872a1715c4cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b864971555410cf3c7ecd8e15f929470ad3e6751db3fb535b698bb37a50e09a9`

```dockerfile
```

-	Layers:
	-	`sha256:b03ea5c9cfa2f868003976091441edbc705a684639b36b3607bd13f9e0fa5a85`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:2bc2d567de72e07f96d39d437aa8ad8c85de7d62d947633c5197d97d05e3603b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213848446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6a020363e23f68ae53ea85f8d5889d92a049d464d3eac58db615f3903fd82d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:49 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:49 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:49 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:49 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:49 GMT
ARG VERSION=25.8.16.34
# Tue, 17 Feb 2026 20:11:49 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:18 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:18 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e105b5258b6287684da632f28c009bead56d72476c38c18b71037e43e8e9b7c`  
		Last Modified: Tue, 17 Feb 2026 20:12:39 GMT  
		Size: 7.6 MB (7577435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494d420eedbfb97f76c475c4139188424ad202fa0e076dcced2c2495768b59ac`  
		Last Modified: Tue, 17 Feb 2026 20:12:41 GMT  
		Size: 178.0 MB (178016046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c477e7fcc96d3a9fe18cfd60a3109816b4a377d41bfdb46d3e0a3438fd193976`  
		Last Modified: Tue, 17 Feb 2026 20:12:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56a0a0e8730d6ac8153fd30fc3f7dc73e6e5160fa253c8ffa137dbdb06914b4`  
		Last Modified: Tue, 17 Feb 2026 20:12:37 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55e4b063f018d389136b40b857059bb4e1bb4f5af6046376bb9edfcad0241ff`  
		Last Modified: Tue, 17 Feb 2026 20:12:38 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ac4fd6f889704ea3b167cbbc7b274f8178ae69d00df70debe3e214aa936b13`  
		Last Modified: Tue, 17 Feb 2026 20:12:38 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff96f921752d4141c565ccca7e44ec7c882d09ac1601be61a0997273ce77657c`  
		Last Modified: Tue, 17 Feb 2026 20:12:40 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e40bf21f69748ff21ecb45294a3d5abada6026f07908ff61c72014db1bb06598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8a041960efb6f4644dde88a255c026fc5cac64f703efced83f24300b69ce680`

```dockerfile
```

-	Layers:
	-	`sha256:d61611774bdc1996895d1e9b295614f62dae75e1c939a7fb15d6abaa66d5a746`  
		Last Modified: Tue, 17 Feb 2026 20:12:37 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts-jammy`

```console
$ docker pull clickhouse@sha256:cb8ea3c339aa84c1d75e0c9fc08f372e0398576caa3d787e7f27b9bbca483d3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:0ec0e053c41857406923f72d00580eac2b61fe11aff754672a9ed03f172c02c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228945044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5381324c8bcc3410608a9c899346d8806971bcef1a1a5fad7b59b6418415de5`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:26 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:12:26 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:12:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:12:26 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:12:26 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:12:26 GMT
ARG VERSION=25.8.16.34
# Tue, 17 Feb 2026 20:12:26 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:53 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:53 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:53 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820dee958d69ceaceb4ea57bc08fb7179f6c7e0987acf3a83c3fb4d05fecc5f2`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 7.6 MB (7598324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258567d60460abdf8fc0d705b07cfb5c2cf9c109302d7d2c766667ce48775f4c`  
		Last Modified: Tue, 17 Feb 2026 20:13:16 GMT  
		Size: 190.9 MB (190939334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e88afd8fd9b9d7dc8563b7db8a2a6351683c3b3e457879c7f4c041b98bff53e`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53900b96e71ca59796a1577140c2aea52ebe99495fc78ab718f66f89ce11fda`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b306d071c1343d8dc0c6d88a9a96ca5aa60bd057563577ae76fd30fbf89e8a3f`  
		Last Modified: Tue, 17 Feb 2026 20:13:13 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c6fbf6e82586a7efc880a4aa52b6e2c210259ad18c01db546ba7da838bd3af`  
		Last Modified: Tue, 17 Feb 2026 20:13:14 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9009d2f669d7bd059ba402b69f6770efd463c0a1f88b6c0a81fce2aa343e61b`  
		Last Modified: Tue, 17 Feb 2026 20:13:14 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0f00e22ef556b57f9002953ccb230258a724d206ddecc96ddef872a1715c4cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b864971555410cf3c7ecd8e15f929470ad3e6751db3fb535b698bb37a50e09a9`

```dockerfile
```

-	Layers:
	-	`sha256:b03ea5c9cfa2f868003976091441edbc705a684639b36b3607bd13f9e0fa5a85`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:2bc2d567de72e07f96d39d437aa8ad8c85de7d62d947633c5197d97d05e3603b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213848446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6a020363e23f68ae53ea85f8d5889d92a049d464d3eac58db615f3903fd82d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:49 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:49 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:49 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:49 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:49 GMT
ARG VERSION=25.8.16.34
# Tue, 17 Feb 2026 20:11:49 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:18 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:18 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e105b5258b6287684da632f28c009bead56d72476c38c18b71037e43e8e9b7c`  
		Last Modified: Tue, 17 Feb 2026 20:12:39 GMT  
		Size: 7.6 MB (7577435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494d420eedbfb97f76c475c4139188424ad202fa0e076dcced2c2495768b59ac`  
		Last Modified: Tue, 17 Feb 2026 20:12:41 GMT  
		Size: 178.0 MB (178016046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c477e7fcc96d3a9fe18cfd60a3109816b4a377d41bfdb46d3e0a3438fd193976`  
		Last Modified: Tue, 17 Feb 2026 20:12:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56a0a0e8730d6ac8153fd30fc3f7dc73e6e5160fa253c8ffa137dbdb06914b4`  
		Last Modified: Tue, 17 Feb 2026 20:12:37 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55e4b063f018d389136b40b857059bb4e1bb4f5af6046376bb9edfcad0241ff`  
		Last Modified: Tue, 17 Feb 2026 20:12:38 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ac4fd6f889704ea3b167cbbc7b274f8178ae69d00df70debe3e214aa936b13`  
		Last Modified: Tue, 17 Feb 2026 20:12:38 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff96f921752d4141c565ccca7e44ec7c882d09ac1601be61a0997273ce77657c`  
		Last Modified: Tue, 17 Feb 2026 20:12:40 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e40bf21f69748ff21ecb45294a3d5abada6026f07908ff61c72014db1bb06598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8a041960efb6f4644dde88a255c026fc5cac64f703efced83f24300b69ce680`

```dockerfile
```

-	Layers:
	-	`sha256:d61611774bdc1996895d1e9b295614f62dae75e1c939a7fb15d6abaa66d5a746`  
		Last Modified: Tue, 17 Feb 2026 20:12:37 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json
