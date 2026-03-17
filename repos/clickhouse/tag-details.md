<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clickhouse`

-	[`clickhouse:25.12`](#clickhouse2512)
-	[`clickhouse:25.12-jammy`](#clickhouse2512-jammy)
-	[`clickhouse:25.12.8`](#clickhouse25128)
-	[`clickhouse:25.12.8-jammy`](#clickhouse25128-jammy)
-	[`clickhouse:25.12.8.9`](#clickhouse251289)
-	[`clickhouse:25.12.8.9-jammy`](#clickhouse251289-jammy)
-	[`clickhouse:25.3`](#clickhouse253)
-	[`clickhouse:25.3-jammy`](#clickhouse253-jammy)
-	[`clickhouse:25.3.14`](#clickhouse25314)
-	[`clickhouse:25.3.14-jammy`](#clickhouse25314-jammy)
-	[`clickhouse:25.3.14.14`](#clickhouse2531414)
-	[`clickhouse:25.3.14.14-jammy`](#clickhouse2531414-jammy)
-	[`clickhouse:25.8`](#clickhouse258)
-	[`clickhouse:25.8-jammy`](#clickhouse258-jammy)
-	[`clickhouse:25.8.18`](#clickhouse25818)
-	[`clickhouse:25.8.18-jammy`](#clickhouse25818-jammy)
-	[`clickhouse:25.8.18.1`](#clickhouse258181)
-	[`clickhouse:25.8.18.1-jammy`](#clickhouse258181-jammy)
-	[`clickhouse:26.1`](#clickhouse261)
-	[`clickhouse:26.1-jammy`](#clickhouse261-jammy)
-	[`clickhouse:26.1.4`](#clickhouse2614)
-	[`clickhouse:26.1.4-jammy`](#clickhouse2614-jammy)
-	[`clickhouse:26.1.4.35`](#clickhouse261435)
-	[`clickhouse:26.1.4.35-jammy`](#clickhouse261435-jammy)
-	[`clickhouse:26.2`](#clickhouse262)
-	[`clickhouse:26.2-jammy`](#clickhouse262-jammy)
-	[`clickhouse:26.2.4`](#clickhouse2624)
-	[`clickhouse:26.2.4-jammy`](#clickhouse2624-jammy)
-	[`clickhouse:26.2.4.23`](#clickhouse262423)
-	[`clickhouse:26.2.4.23-jammy`](#clickhouse262423-jammy)
-	[`clickhouse:jammy`](#clickhousejammy)
-	[`clickhouse:latest`](#clickhouselatest)
-	[`clickhouse:lts`](#clickhouselts)
-	[`clickhouse:lts-jammy`](#clickhouselts-jammy)

## `clickhouse:25.12`

```console
$ docker pull clickhouse@sha256:052b9c4466989070c56a5d16e60bf7743abc5b438d1c6bf7dd1a9c5b15e9b812
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.12` - linux; amd64

```console
$ docker pull clickhouse@sha256:fac0609179d0fa1093499519e286c2a13ed2ff8cc72bdfd5203c7ff849c2664e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246378430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:110e422d32d054790fe317c51beff171355faaf609442979b2adc949165a0405`
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
# Fri, 06 Mar 2026 18:18:09 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:09 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:09 GMT
ARG VERSION=25.12.8.9
# Fri, 06 Mar 2026 18:18:09 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:19:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:19:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:19:44 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:19:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:19:44 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:19:44 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:19:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22eaf4113aeb35a06fd46548b455b9b73b22b6d4d683b65ed58a5cbbeb012e3e`  
		Last Modified: Fri, 06 Mar 2026 18:19:04 GMT  
		Size: 7.6 MB (7598345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eaa12a3aadd71c346f315cdc572d9b848e1175c3d8ea2b0ac09ea124d9b2ebd`  
		Last Modified: Fri, 06 Mar 2026 18:20:14 GMT  
		Size: 208.4 MB (208372669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c291f511c5d1878ea81eb683aea2f353bb3a5a1bed516d82358820e7f36ba547`  
		Last Modified: Fri, 06 Mar 2026 18:20:09 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619cad1e3fe6dc81d8578912c7720ee86f9d77221c2698d2344350c7c1d6cd9c`  
		Last Modified: Fri, 06 Mar 2026 18:20:09 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62cc90988622b94efb394ef436315d0c6ca039b5f324ad95af99a9104c9ea128`  
		Last Modified: Fri, 06 Mar 2026 18:20:09 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2b0d9cb6bcfc39aca49338e07ae1048e033a959835ca8cb1da37bf18346cf1`  
		Last Modified: Fri, 06 Mar 2026 18:20:10 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7df23d46b224adba793c134a422475c5792f2c92c36e6a012be15e280784ec`  
		Last Modified: Fri, 06 Mar 2026 18:20:10 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12` - unknown; unknown

```console
$ docker pull clickhouse@sha256:054cd0f5581571d38c3a5089fe533b22c5977b4e79b47d2d3a4198147ddeca50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72db44c5b921c2a6b491b960920defdbc67b36419bf73068a1793c524a988fe1`

```dockerfile
```

-	Layers:
	-	`sha256:df14ab7180d67e046644843b7e13d5071293464d5470c7fa18d76af28b25446d`  
		Last Modified: Fri, 06 Mar 2026 18:20:09 GMT  
		Size: 25.4 KB (25426 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.12` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:e5a5c629ad6d9ffe898cb4b34c2b866b50cbd29da7a96cfd929a4e5001b28d80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228297213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f8baf51e92bc56c5fba203f387d58cab31a5029dd7b8deab8110340a0142c4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:46 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:46 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:46 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:46 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:46 GMT
ARG VERSION=25.12.8.9
# Tue, 17 Mar 2026 01:15:46 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:16:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:16:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:16:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:16:21 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:16:21 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:16:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:16:21 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:16:21 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:16:21 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:16:21 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:16:21 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:16:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381efad135058801adc987b93ccee75a2c9bcffddf19fbbb3524d6e7f213494b`  
		Last Modified: Tue, 17 Mar 2026 01:16:44 GMT  
		Size: 7.6 MB (7577332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e339810d2e03e4735b96812cf17632a10f940de183a48d57873031009bd28fc2`  
		Last Modified: Tue, 17 Mar 2026 01:16:47 GMT  
		Size: 192.5 MB (192460805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c889c6e3064f755c86fee8d49a38817156be15e0b7665b3f43d9229f901f990`  
		Last Modified: Tue, 17 Mar 2026 01:16:44 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22c8ce8b6dd3ac561aec5f3852d9c57ee0f363b99df84bddb35054a40f91da2`  
		Last Modified: Tue, 17 Mar 2026 01:16:43 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2d47d48a0b947ac75772c908b99edf66603988f810f6817cad744ac105a3f0`  
		Last Modified: Tue, 17 Mar 2026 01:16:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284e2bb6092cb005190569c97e90a9b97c2f668feb60563104d697d399cdbd27`  
		Last Modified: Tue, 17 Mar 2026 01:16:45 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4bf266dd106987e35f67847cb8e14b785af143c08056a7979e5f9a9a1bb4b48`  
		Last Modified: Tue, 17 Mar 2026 01:16:45 GMT  
		Size: 3.6 KB (3634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f6528acbd831c8503f74910943054bf4251084c857291e0b319bacf7e01c9d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:009230da7d18738fc695704a997e710e4ae31305b01cc7d54c9f8c56ba9d269a`

```dockerfile
```

-	Layers:
	-	`sha256:c6d448ea963df46f317f038c0d958fb0f2aa165355945a7d3267da49c5cdefbf`  
		Last Modified: Tue, 17 Mar 2026 01:16:43 GMT  
		Size: 25.6 KB (25614 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.12-jammy`

```console
$ docker pull clickhouse@sha256:052b9c4466989070c56a5d16e60bf7743abc5b438d1c6bf7dd1a9c5b15e9b812
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.12-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:fac0609179d0fa1093499519e286c2a13ed2ff8cc72bdfd5203c7ff849c2664e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246378430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:110e422d32d054790fe317c51beff171355faaf609442979b2adc949165a0405`
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
# Fri, 06 Mar 2026 18:18:09 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:09 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:09 GMT
ARG VERSION=25.12.8.9
# Fri, 06 Mar 2026 18:18:09 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:19:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:19:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:19:44 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:19:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:19:44 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:19:44 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:19:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22eaf4113aeb35a06fd46548b455b9b73b22b6d4d683b65ed58a5cbbeb012e3e`  
		Last Modified: Fri, 06 Mar 2026 18:19:04 GMT  
		Size: 7.6 MB (7598345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eaa12a3aadd71c346f315cdc572d9b848e1175c3d8ea2b0ac09ea124d9b2ebd`  
		Last Modified: Fri, 06 Mar 2026 18:20:14 GMT  
		Size: 208.4 MB (208372669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c291f511c5d1878ea81eb683aea2f353bb3a5a1bed516d82358820e7f36ba547`  
		Last Modified: Fri, 06 Mar 2026 18:20:09 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619cad1e3fe6dc81d8578912c7720ee86f9d77221c2698d2344350c7c1d6cd9c`  
		Last Modified: Fri, 06 Mar 2026 18:20:09 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62cc90988622b94efb394ef436315d0c6ca039b5f324ad95af99a9104c9ea128`  
		Last Modified: Fri, 06 Mar 2026 18:20:09 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2b0d9cb6bcfc39aca49338e07ae1048e033a959835ca8cb1da37bf18346cf1`  
		Last Modified: Fri, 06 Mar 2026 18:20:10 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7df23d46b224adba793c134a422475c5792f2c92c36e6a012be15e280784ec`  
		Last Modified: Fri, 06 Mar 2026 18:20:10 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:054cd0f5581571d38c3a5089fe533b22c5977b4e79b47d2d3a4198147ddeca50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72db44c5b921c2a6b491b960920defdbc67b36419bf73068a1793c524a988fe1`

```dockerfile
```

-	Layers:
	-	`sha256:df14ab7180d67e046644843b7e13d5071293464d5470c7fa18d76af28b25446d`  
		Last Modified: Fri, 06 Mar 2026 18:20:09 GMT  
		Size: 25.4 KB (25426 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.12-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:e5a5c629ad6d9ffe898cb4b34c2b866b50cbd29da7a96cfd929a4e5001b28d80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228297213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f8baf51e92bc56c5fba203f387d58cab31a5029dd7b8deab8110340a0142c4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:46 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:46 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:46 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:46 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:46 GMT
ARG VERSION=25.12.8.9
# Tue, 17 Mar 2026 01:15:46 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:16:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:16:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:16:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:16:21 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:16:21 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:16:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:16:21 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:16:21 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:16:21 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:16:21 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:16:21 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:16:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381efad135058801adc987b93ccee75a2c9bcffddf19fbbb3524d6e7f213494b`  
		Last Modified: Tue, 17 Mar 2026 01:16:44 GMT  
		Size: 7.6 MB (7577332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e339810d2e03e4735b96812cf17632a10f940de183a48d57873031009bd28fc2`  
		Last Modified: Tue, 17 Mar 2026 01:16:47 GMT  
		Size: 192.5 MB (192460805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c889c6e3064f755c86fee8d49a38817156be15e0b7665b3f43d9229f901f990`  
		Last Modified: Tue, 17 Mar 2026 01:16:44 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22c8ce8b6dd3ac561aec5f3852d9c57ee0f363b99df84bddb35054a40f91da2`  
		Last Modified: Tue, 17 Mar 2026 01:16:43 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2d47d48a0b947ac75772c908b99edf66603988f810f6817cad744ac105a3f0`  
		Last Modified: Tue, 17 Mar 2026 01:16:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284e2bb6092cb005190569c97e90a9b97c2f668feb60563104d697d399cdbd27`  
		Last Modified: Tue, 17 Mar 2026 01:16:45 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4bf266dd106987e35f67847cb8e14b785af143c08056a7979e5f9a9a1bb4b48`  
		Last Modified: Tue, 17 Mar 2026 01:16:45 GMT  
		Size: 3.6 KB (3634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f6528acbd831c8503f74910943054bf4251084c857291e0b319bacf7e01c9d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:009230da7d18738fc695704a997e710e4ae31305b01cc7d54c9f8c56ba9d269a`

```dockerfile
```

-	Layers:
	-	`sha256:c6d448ea963df46f317f038c0d958fb0f2aa165355945a7d3267da49c5cdefbf`  
		Last Modified: Tue, 17 Mar 2026 01:16:43 GMT  
		Size: 25.6 KB (25614 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.12.8`

```console
$ docker pull clickhouse@sha256:052b9c4466989070c56a5d16e60bf7743abc5b438d1c6bf7dd1a9c5b15e9b812
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.12.8` - linux; amd64

```console
$ docker pull clickhouse@sha256:fac0609179d0fa1093499519e286c2a13ed2ff8cc72bdfd5203c7ff849c2664e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246378430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:110e422d32d054790fe317c51beff171355faaf609442979b2adc949165a0405`
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
# Fri, 06 Mar 2026 18:18:09 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:09 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:09 GMT
ARG VERSION=25.12.8.9
# Fri, 06 Mar 2026 18:18:09 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:19:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:19:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:19:44 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:19:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:19:44 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:19:44 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:19:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22eaf4113aeb35a06fd46548b455b9b73b22b6d4d683b65ed58a5cbbeb012e3e`  
		Last Modified: Fri, 06 Mar 2026 18:19:04 GMT  
		Size: 7.6 MB (7598345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eaa12a3aadd71c346f315cdc572d9b848e1175c3d8ea2b0ac09ea124d9b2ebd`  
		Last Modified: Fri, 06 Mar 2026 18:20:14 GMT  
		Size: 208.4 MB (208372669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c291f511c5d1878ea81eb683aea2f353bb3a5a1bed516d82358820e7f36ba547`  
		Last Modified: Fri, 06 Mar 2026 18:20:09 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619cad1e3fe6dc81d8578912c7720ee86f9d77221c2698d2344350c7c1d6cd9c`  
		Last Modified: Fri, 06 Mar 2026 18:20:09 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62cc90988622b94efb394ef436315d0c6ca039b5f324ad95af99a9104c9ea128`  
		Last Modified: Fri, 06 Mar 2026 18:20:09 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2b0d9cb6bcfc39aca49338e07ae1048e033a959835ca8cb1da37bf18346cf1`  
		Last Modified: Fri, 06 Mar 2026 18:20:10 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7df23d46b224adba793c134a422475c5792f2c92c36e6a012be15e280784ec`  
		Last Modified: Fri, 06 Mar 2026 18:20:10 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:054cd0f5581571d38c3a5089fe533b22c5977b4e79b47d2d3a4198147ddeca50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72db44c5b921c2a6b491b960920defdbc67b36419bf73068a1793c524a988fe1`

```dockerfile
```

-	Layers:
	-	`sha256:df14ab7180d67e046644843b7e13d5071293464d5470c7fa18d76af28b25446d`  
		Last Modified: Fri, 06 Mar 2026 18:20:09 GMT  
		Size: 25.4 KB (25426 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.12.8` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:e5a5c629ad6d9ffe898cb4b34c2b866b50cbd29da7a96cfd929a4e5001b28d80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228297213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f8baf51e92bc56c5fba203f387d58cab31a5029dd7b8deab8110340a0142c4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:46 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:46 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:46 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:46 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:46 GMT
ARG VERSION=25.12.8.9
# Tue, 17 Mar 2026 01:15:46 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:16:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:16:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:16:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:16:21 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:16:21 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:16:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:16:21 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:16:21 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:16:21 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:16:21 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:16:21 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:16:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381efad135058801adc987b93ccee75a2c9bcffddf19fbbb3524d6e7f213494b`  
		Last Modified: Tue, 17 Mar 2026 01:16:44 GMT  
		Size: 7.6 MB (7577332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e339810d2e03e4735b96812cf17632a10f940de183a48d57873031009bd28fc2`  
		Last Modified: Tue, 17 Mar 2026 01:16:47 GMT  
		Size: 192.5 MB (192460805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c889c6e3064f755c86fee8d49a38817156be15e0b7665b3f43d9229f901f990`  
		Last Modified: Tue, 17 Mar 2026 01:16:44 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22c8ce8b6dd3ac561aec5f3852d9c57ee0f363b99df84bddb35054a40f91da2`  
		Last Modified: Tue, 17 Mar 2026 01:16:43 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2d47d48a0b947ac75772c908b99edf66603988f810f6817cad744ac105a3f0`  
		Last Modified: Tue, 17 Mar 2026 01:16:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284e2bb6092cb005190569c97e90a9b97c2f668feb60563104d697d399cdbd27`  
		Last Modified: Tue, 17 Mar 2026 01:16:45 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4bf266dd106987e35f67847cb8e14b785af143c08056a7979e5f9a9a1bb4b48`  
		Last Modified: Tue, 17 Mar 2026 01:16:45 GMT  
		Size: 3.6 KB (3634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f6528acbd831c8503f74910943054bf4251084c857291e0b319bacf7e01c9d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:009230da7d18738fc695704a997e710e4ae31305b01cc7d54c9f8c56ba9d269a`

```dockerfile
```

-	Layers:
	-	`sha256:c6d448ea963df46f317f038c0d958fb0f2aa165355945a7d3267da49c5cdefbf`  
		Last Modified: Tue, 17 Mar 2026 01:16:43 GMT  
		Size: 25.6 KB (25614 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.12.8-jammy`

```console
$ docker pull clickhouse@sha256:052b9c4466989070c56a5d16e60bf7743abc5b438d1c6bf7dd1a9c5b15e9b812
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.12.8-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:fac0609179d0fa1093499519e286c2a13ed2ff8cc72bdfd5203c7ff849c2664e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246378430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:110e422d32d054790fe317c51beff171355faaf609442979b2adc949165a0405`
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
# Fri, 06 Mar 2026 18:18:09 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:09 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:09 GMT
ARG VERSION=25.12.8.9
# Fri, 06 Mar 2026 18:18:09 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:19:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:19:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:19:44 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:19:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:19:44 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:19:44 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:19:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22eaf4113aeb35a06fd46548b455b9b73b22b6d4d683b65ed58a5cbbeb012e3e`  
		Last Modified: Fri, 06 Mar 2026 18:19:04 GMT  
		Size: 7.6 MB (7598345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eaa12a3aadd71c346f315cdc572d9b848e1175c3d8ea2b0ac09ea124d9b2ebd`  
		Last Modified: Fri, 06 Mar 2026 18:20:14 GMT  
		Size: 208.4 MB (208372669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c291f511c5d1878ea81eb683aea2f353bb3a5a1bed516d82358820e7f36ba547`  
		Last Modified: Fri, 06 Mar 2026 18:20:09 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619cad1e3fe6dc81d8578912c7720ee86f9d77221c2698d2344350c7c1d6cd9c`  
		Last Modified: Fri, 06 Mar 2026 18:20:09 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62cc90988622b94efb394ef436315d0c6ca039b5f324ad95af99a9104c9ea128`  
		Last Modified: Fri, 06 Mar 2026 18:20:09 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2b0d9cb6bcfc39aca49338e07ae1048e033a959835ca8cb1da37bf18346cf1`  
		Last Modified: Fri, 06 Mar 2026 18:20:10 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7df23d46b224adba793c134a422475c5792f2c92c36e6a012be15e280784ec`  
		Last Modified: Fri, 06 Mar 2026 18:20:10 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:054cd0f5581571d38c3a5089fe533b22c5977b4e79b47d2d3a4198147ddeca50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72db44c5b921c2a6b491b960920defdbc67b36419bf73068a1793c524a988fe1`

```dockerfile
```

-	Layers:
	-	`sha256:df14ab7180d67e046644843b7e13d5071293464d5470c7fa18d76af28b25446d`  
		Last Modified: Fri, 06 Mar 2026 18:20:09 GMT  
		Size: 25.4 KB (25426 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.12.8-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:e5a5c629ad6d9ffe898cb4b34c2b866b50cbd29da7a96cfd929a4e5001b28d80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228297213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f8baf51e92bc56c5fba203f387d58cab31a5029dd7b8deab8110340a0142c4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:46 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:46 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:46 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:46 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:46 GMT
ARG VERSION=25.12.8.9
# Tue, 17 Mar 2026 01:15:46 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:16:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:16:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:16:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:16:21 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:16:21 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:16:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:16:21 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:16:21 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:16:21 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:16:21 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:16:21 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:16:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381efad135058801adc987b93ccee75a2c9bcffddf19fbbb3524d6e7f213494b`  
		Last Modified: Tue, 17 Mar 2026 01:16:44 GMT  
		Size: 7.6 MB (7577332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e339810d2e03e4735b96812cf17632a10f940de183a48d57873031009bd28fc2`  
		Last Modified: Tue, 17 Mar 2026 01:16:47 GMT  
		Size: 192.5 MB (192460805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c889c6e3064f755c86fee8d49a38817156be15e0b7665b3f43d9229f901f990`  
		Last Modified: Tue, 17 Mar 2026 01:16:44 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22c8ce8b6dd3ac561aec5f3852d9c57ee0f363b99df84bddb35054a40f91da2`  
		Last Modified: Tue, 17 Mar 2026 01:16:43 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2d47d48a0b947ac75772c908b99edf66603988f810f6817cad744ac105a3f0`  
		Last Modified: Tue, 17 Mar 2026 01:16:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284e2bb6092cb005190569c97e90a9b97c2f668feb60563104d697d399cdbd27`  
		Last Modified: Tue, 17 Mar 2026 01:16:45 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4bf266dd106987e35f67847cb8e14b785af143c08056a7979e5f9a9a1bb4b48`  
		Last Modified: Tue, 17 Mar 2026 01:16:45 GMT  
		Size: 3.6 KB (3634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f6528acbd831c8503f74910943054bf4251084c857291e0b319bacf7e01c9d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:009230da7d18738fc695704a997e710e4ae31305b01cc7d54c9f8c56ba9d269a`

```dockerfile
```

-	Layers:
	-	`sha256:c6d448ea963df46f317f038c0d958fb0f2aa165355945a7d3267da49c5cdefbf`  
		Last Modified: Tue, 17 Mar 2026 01:16:43 GMT  
		Size: 25.6 KB (25614 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.12.8.9`

```console
$ docker pull clickhouse@sha256:052b9c4466989070c56a5d16e60bf7743abc5b438d1c6bf7dd1a9c5b15e9b812
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.12.8.9` - linux; amd64

```console
$ docker pull clickhouse@sha256:fac0609179d0fa1093499519e286c2a13ed2ff8cc72bdfd5203c7ff849c2664e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246378430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:110e422d32d054790fe317c51beff171355faaf609442979b2adc949165a0405`
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
# Fri, 06 Mar 2026 18:18:09 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:09 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:09 GMT
ARG VERSION=25.12.8.9
# Fri, 06 Mar 2026 18:18:09 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:19:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:19:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:19:44 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:19:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:19:44 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:19:44 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:19:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22eaf4113aeb35a06fd46548b455b9b73b22b6d4d683b65ed58a5cbbeb012e3e`  
		Last Modified: Fri, 06 Mar 2026 18:19:04 GMT  
		Size: 7.6 MB (7598345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eaa12a3aadd71c346f315cdc572d9b848e1175c3d8ea2b0ac09ea124d9b2ebd`  
		Last Modified: Fri, 06 Mar 2026 18:20:14 GMT  
		Size: 208.4 MB (208372669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c291f511c5d1878ea81eb683aea2f353bb3a5a1bed516d82358820e7f36ba547`  
		Last Modified: Fri, 06 Mar 2026 18:20:09 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619cad1e3fe6dc81d8578912c7720ee86f9d77221c2698d2344350c7c1d6cd9c`  
		Last Modified: Fri, 06 Mar 2026 18:20:09 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62cc90988622b94efb394ef436315d0c6ca039b5f324ad95af99a9104c9ea128`  
		Last Modified: Fri, 06 Mar 2026 18:20:09 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2b0d9cb6bcfc39aca49338e07ae1048e033a959835ca8cb1da37bf18346cf1`  
		Last Modified: Fri, 06 Mar 2026 18:20:10 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7df23d46b224adba793c134a422475c5792f2c92c36e6a012be15e280784ec`  
		Last Modified: Fri, 06 Mar 2026 18:20:10 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.8.9` - unknown; unknown

```console
$ docker pull clickhouse@sha256:054cd0f5581571d38c3a5089fe533b22c5977b4e79b47d2d3a4198147ddeca50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72db44c5b921c2a6b491b960920defdbc67b36419bf73068a1793c524a988fe1`

```dockerfile
```

-	Layers:
	-	`sha256:df14ab7180d67e046644843b7e13d5071293464d5470c7fa18d76af28b25446d`  
		Last Modified: Fri, 06 Mar 2026 18:20:09 GMT  
		Size: 25.4 KB (25426 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.12.8.9` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:e5a5c629ad6d9ffe898cb4b34c2b866b50cbd29da7a96cfd929a4e5001b28d80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228297213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f8baf51e92bc56c5fba203f387d58cab31a5029dd7b8deab8110340a0142c4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:46 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:46 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:46 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:46 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:46 GMT
ARG VERSION=25.12.8.9
# Tue, 17 Mar 2026 01:15:46 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:16:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:16:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:16:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:16:21 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:16:21 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:16:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:16:21 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:16:21 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:16:21 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:16:21 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:16:21 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:16:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381efad135058801adc987b93ccee75a2c9bcffddf19fbbb3524d6e7f213494b`  
		Last Modified: Tue, 17 Mar 2026 01:16:44 GMT  
		Size: 7.6 MB (7577332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e339810d2e03e4735b96812cf17632a10f940de183a48d57873031009bd28fc2`  
		Last Modified: Tue, 17 Mar 2026 01:16:47 GMT  
		Size: 192.5 MB (192460805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c889c6e3064f755c86fee8d49a38817156be15e0b7665b3f43d9229f901f990`  
		Last Modified: Tue, 17 Mar 2026 01:16:44 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22c8ce8b6dd3ac561aec5f3852d9c57ee0f363b99df84bddb35054a40f91da2`  
		Last Modified: Tue, 17 Mar 2026 01:16:43 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2d47d48a0b947ac75772c908b99edf66603988f810f6817cad744ac105a3f0`  
		Last Modified: Tue, 17 Mar 2026 01:16:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284e2bb6092cb005190569c97e90a9b97c2f668feb60563104d697d399cdbd27`  
		Last Modified: Tue, 17 Mar 2026 01:16:45 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4bf266dd106987e35f67847cb8e14b785af143c08056a7979e5f9a9a1bb4b48`  
		Last Modified: Tue, 17 Mar 2026 01:16:45 GMT  
		Size: 3.6 KB (3634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.8.9` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f6528acbd831c8503f74910943054bf4251084c857291e0b319bacf7e01c9d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:009230da7d18738fc695704a997e710e4ae31305b01cc7d54c9f8c56ba9d269a`

```dockerfile
```

-	Layers:
	-	`sha256:c6d448ea963df46f317f038c0d958fb0f2aa165355945a7d3267da49c5cdefbf`  
		Last Modified: Tue, 17 Mar 2026 01:16:43 GMT  
		Size: 25.6 KB (25614 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.12.8.9-jammy`

```console
$ docker pull clickhouse@sha256:052b9c4466989070c56a5d16e60bf7743abc5b438d1c6bf7dd1a9c5b15e9b812
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.12.8.9-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:fac0609179d0fa1093499519e286c2a13ed2ff8cc72bdfd5203c7ff849c2664e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246378430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:110e422d32d054790fe317c51beff171355faaf609442979b2adc949165a0405`
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
# Fri, 06 Mar 2026 18:18:09 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:09 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:09 GMT
ARG VERSION=25.12.8.9
# Fri, 06 Mar 2026 18:18:09 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:19:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:19:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:19:44 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:19:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:19:44 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:19:44 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:19:44 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:19:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22eaf4113aeb35a06fd46548b455b9b73b22b6d4d683b65ed58a5cbbeb012e3e`  
		Last Modified: Fri, 06 Mar 2026 18:19:04 GMT  
		Size: 7.6 MB (7598345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eaa12a3aadd71c346f315cdc572d9b848e1175c3d8ea2b0ac09ea124d9b2ebd`  
		Last Modified: Fri, 06 Mar 2026 18:20:14 GMT  
		Size: 208.4 MB (208372669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c291f511c5d1878ea81eb683aea2f353bb3a5a1bed516d82358820e7f36ba547`  
		Last Modified: Fri, 06 Mar 2026 18:20:09 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619cad1e3fe6dc81d8578912c7720ee86f9d77221c2698d2344350c7c1d6cd9c`  
		Last Modified: Fri, 06 Mar 2026 18:20:09 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62cc90988622b94efb394ef436315d0c6ca039b5f324ad95af99a9104c9ea128`  
		Last Modified: Fri, 06 Mar 2026 18:20:09 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2b0d9cb6bcfc39aca49338e07ae1048e033a959835ca8cb1da37bf18346cf1`  
		Last Modified: Fri, 06 Mar 2026 18:20:10 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7df23d46b224adba793c134a422475c5792f2c92c36e6a012be15e280784ec`  
		Last Modified: Fri, 06 Mar 2026 18:20:10 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.8.9-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:054cd0f5581571d38c3a5089fe533b22c5977b4e79b47d2d3a4198147ddeca50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72db44c5b921c2a6b491b960920defdbc67b36419bf73068a1793c524a988fe1`

```dockerfile
```

-	Layers:
	-	`sha256:df14ab7180d67e046644843b7e13d5071293464d5470c7fa18d76af28b25446d`  
		Last Modified: Fri, 06 Mar 2026 18:20:09 GMT  
		Size: 25.4 KB (25426 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.12.8.9-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:e5a5c629ad6d9ffe898cb4b34c2b866b50cbd29da7a96cfd929a4e5001b28d80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228297213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f8baf51e92bc56c5fba203f387d58cab31a5029dd7b8deab8110340a0142c4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:46 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:46 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:46 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:46 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:46 GMT
ARG VERSION=25.12.8.9
# Tue, 17 Mar 2026 01:15:46 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:16:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:16:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:16:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:16:21 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:16:21 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:16:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.8.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:16:21 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:16:21 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:16:21 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:16:21 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:16:21 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:16:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381efad135058801adc987b93ccee75a2c9bcffddf19fbbb3524d6e7f213494b`  
		Last Modified: Tue, 17 Mar 2026 01:16:44 GMT  
		Size: 7.6 MB (7577332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e339810d2e03e4735b96812cf17632a10f940de183a48d57873031009bd28fc2`  
		Last Modified: Tue, 17 Mar 2026 01:16:47 GMT  
		Size: 192.5 MB (192460805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c889c6e3064f755c86fee8d49a38817156be15e0b7665b3f43d9229f901f990`  
		Last Modified: Tue, 17 Mar 2026 01:16:44 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22c8ce8b6dd3ac561aec5f3852d9c57ee0f363b99df84bddb35054a40f91da2`  
		Last Modified: Tue, 17 Mar 2026 01:16:43 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2d47d48a0b947ac75772c908b99edf66603988f810f6817cad744ac105a3f0`  
		Last Modified: Tue, 17 Mar 2026 01:16:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284e2bb6092cb005190569c97e90a9b97c2f668feb60563104d697d399cdbd27`  
		Last Modified: Tue, 17 Mar 2026 01:16:45 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4bf266dd106987e35f67847cb8e14b785af143c08056a7979e5f9a9a1bb4b48`  
		Last Modified: Tue, 17 Mar 2026 01:16:45 GMT  
		Size: 3.6 KB (3634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.8.9-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f6528acbd831c8503f74910943054bf4251084c857291e0b319bacf7e01c9d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:009230da7d18738fc695704a997e710e4ae31305b01cc7d54c9f8c56ba9d269a`

```dockerfile
```

-	Layers:
	-	`sha256:c6d448ea963df46f317f038c0d958fb0f2aa165355945a7d3267da49c5cdefbf`  
		Last Modified: Tue, 17 Mar 2026 01:16:43 GMT  
		Size: 25.6 KB (25614 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3`

```console
$ docker pull clickhouse@sha256:b59cd7dc15fc4e07879149a3c3c06a0eccd14ccb8e80877756ecbf1a9cbeb74e
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
$ docker pull clickhouse@sha256:665f0d2d923456af1fb9fb7ce7d4ed6834592b747256d5aedc7a43fbbe135310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193810367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739f9cb8a27aff7bab921735652a16a7413e448d65fb87029fbd3ad9043bb020`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:23 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:23 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:23 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:23 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:23 GMT
ARG VERSION=25.3.14.14
# Tue, 17 Mar 2026 01:15:23 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:15:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:15:49 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:15:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:15:49 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:15:49 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:15:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3378707c4664419239f73413d0d64cc47512c8c4d2277b83766d0663fc56ee06`  
		Last Modified: Tue, 17 Mar 2026 01:16:06 GMT  
		Size: 7.1 MB (7128017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c23b4cfc6a6b13daa97de2f89e8b8bdf88f720b6844e6c4aa944112b18abdf1`  
		Last Modified: Tue, 17 Mar 2026 01:16:09 GMT  
		Size: 158.4 MB (158423075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d5949d99157b0c7b1f549b8906dcb08667b9b7be89944afb54a57c94302ea9`  
		Last Modified: Tue, 17 Mar 2026 01:16:06 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9487f671e7c9bd07d5037953db2a6beca888ce7783f207678d52239f0b054ab`  
		Last Modified: Tue, 17 Mar 2026 01:16:06 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80030bcef0d1515fd0bf3371bf1813444b6a7dd75363687403f34f7fbd689f47`  
		Last Modified: Tue, 17 Mar 2026 01:16:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19232562da027e1b978e40983a63aa4b932d406793b7bea774c62d0051567096`  
		Last Modified: Tue, 17 Mar 2026 01:16:07 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97e7c37ba3dfa013d3ddd63ce2968f8ff02d26b1001243b795a8390f27410b5`  
		Last Modified: Tue, 17 Mar 2026 01:16:07 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e34d019b82610f0133a441648010ad80682418c07c5ce43a142d4b564cafc969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b94f700e7376d22e3a7304430fc82280ecb6572ce8aa95b423a2ae06dbf1398`

```dockerfile
```

-	Layers:
	-	`sha256:1b7e4053e3be085fbadb553c8575a9fcfef9a7a592ba4d872b484863b71a5f3e`  
		Last Modified: Tue, 17 Mar 2026 01:16:06 GMT  
		Size: 25.4 KB (25423 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3-jammy`

```console
$ docker pull clickhouse@sha256:b59cd7dc15fc4e07879149a3c3c06a0eccd14ccb8e80877756ecbf1a9cbeb74e
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
$ docker pull clickhouse@sha256:665f0d2d923456af1fb9fb7ce7d4ed6834592b747256d5aedc7a43fbbe135310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193810367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739f9cb8a27aff7bab921735652a16a7413e448d65fb87029fbd3ad9043bb020`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:23 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:23 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:23 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:23 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:23 GMT
ARG VERSION=25.3.14.14
# Tue, 17 Mar 2026 01:15:23 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:15:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:15:49 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:15:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:15:49 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:15:49 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:15:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3378707c4664419239f73413d0d64cc47512c8c4d2277b83766d0663fc56ee06`  
		Last Modified: Tue, 17 Mar 2026 01:16:06 GMT  
		Size: 7.1 MB (7128017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c23b4cfc6a6b13daa97de2f89e8b8bdf88f720b6844e6c4aa944112b18abdf1`  
		Last Modified: Tue, 17 Mar 2026 01:16:09 GMT  
		Size: 158.4 MB (158423075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d5949d99157b0c7b1f549b8906dcb08667b9b7be89944afb54a57c94302ea9`  
		Last Modified: Tue, 17 Mar 2026 01:16:06 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9487f671e7c9bd07d5037953db2a6beca888ce7783f207678d52239f0b054ab`  
		Last Modified: Tue, 17 Mar 2026 01:16:06 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80030bcef0d1515fd0bf3371bf1813444b6a7dd75363687403f34f7fbd689f47`  
		Last Modified: Tue, 17 Mar 2026 01:16:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19232562da027e1b978e40983a63aa4b932d406793b7bea774c62d0051567096`  
		Last Modified: Tue, 17 Mar 2026 01:16:07 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97e7c37ba3dfa013d3ddd63ce2968f8ff02d26b1001243b795a8390f27410b5`  
		Last Modified: Tue, 17 Mar 2026 01:16:07 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e34d019b82610f0133a441648010ad80682418c07c5ce43a142d4b564cafc969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b94f700e7376d22e3a7304430fc82280ecb6572ce8aa95b423a2ae06dbf1398`

```dockerfile
```

-	Layers:
	-	`sha256:1b7e4053e3be085fbadb553c8575a9fcfef9a7a592ba4d872b484863b71a5f3e`  
		Last Modified: Tue, 17 Mar 2026 01:16:06 GMT  
		Size: 25.4 KB (25423 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.14`

```console
$ docker pull clickhouse@sha256:b59cd7dc15fc4e07879149a3c3c06a0eccd14ccb8e80877756ecbf1a9cbeb74e
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
$ docker pull clickhouse@sha256:665f0d2d923456af1fb9fb7ce7d4ed6834592b747256d5aedc7a43fbbe135310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193810367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739f9cb8a27aff7bab921735652a16a7413e448d65fb87029fbd3ad9043bb020`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:23 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:23 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:23 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:23 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:23 GMT
ARG VERSION=25.3.14.14
# Tue, 17 Mar 2026 01:15:23 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:15:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:15:49 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:15:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:15:49 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:15:49 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:15:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3378707c4664419239f73413d0d64cc47512c8c4d2277b83766d0663fc56ee06`  
		Last Modified: Tue, 17 Mar 2026 01:16:06 GMT  
		Size: 7.1 MB (7128017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c23b4cfc6a6b13daa97de2f89e8b8bdf88f720b6844e6c4aa944112b18abdf1`  
		Last Modified: Tue, 17 Mar 2026 01:16:09 GMT  
		Size: 158.4 MB (158423075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d5949d99157b0c7b1f549b8906dcb08667b9b7be89944afb54a57c94302ea9`  
		Last Modified: Tue, 17 Mar 2026 01:16:06 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9487f671e7c9bd07d5037953db2a6beca888ce7783f207678d52239f0b054ab`  
		Last Modified: Tue, 17 Mar 2026 01:16:06 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80030bcef0d1515fd0bf3371bf1813444b6a7dd75363687403f34f7fbd689f47`  
		Last Modified: Tue, 17 Mar 2026 01:16:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19232562da027e1b978e40983a63aa4b932d406793b7bea774c62d0051567096`  
		Last Modified: Tue, 17 Mar 2026 01:16:07 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97e7c37ba3dfa013d3ddd63ce2968f8ff02d26b1001243b795a8390f27410b5`  
		Last Modified: Tue, 17 Mar 2026 01:16:07 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.14` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e34d019b82610f0133a441648010ad80682418c07c5ce43a142d4b564cafc969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b94f700e7376d22e3a7304430fc82280ecb6572ce8aa95b423a2ae06dbf1398`

```dockerfile
```

-	Layers:
	-	`sha256:1b7e4053e3be085fbadb553c8575a9fcfef9a7a592ba4d872b484863b71a5f3e`  
		Last Modified: Tue, 17 Mar 2026 01:16:06 GMT  
		Size: 25.4 KB (25423 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.14-jammy`

```console
$ docker pull clickhouse@sha256:b59cd7dc15fc4e07879149a3c3c06a0eccd14ccb8e80877756ecbf1a9cbeb74e
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
$ docker pull clickhouse@sha256:665f0d2d923456af1fb9fb7ce7d4ed6834592b747256d5aedc7a43fbbe135310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193810367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739f9cb8a27aff7bab921735652a16a7413e448d65fb87029fbd3ad9043bb020`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:23 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:23 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:23 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:23 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:23 GMT
ARG VERSION=25.3.14.14
# Tue, 17 Mar 2026 01:15:23 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:15:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:15:49 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:15:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:15:49 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:15:49 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:15:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3378707c4664419239f73413d0d64cc47512c8c4d2277b83766d0663fc56ee06`  
		Last Modified: Tue, 17 Mar 2026 01:16:06 GMT  
		Size: 7.1 MB (7128017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c23b4cfc6a6b13daa97de2f89e8b8bdf88f720b6844e6c4aa944112b18abdf1`  
		Last Modified: Tue, 17 Mar 2026 01:16:09 GMT  
		Size: 158.4 MB (158423075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d5949d99157b0c7b1f549b8906dcb08667b9b7be89944afb54a57c94302ea9`  
		Last Modified: Tue, 17 Mar 2026 01:16:06 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9487f671e7c9bd07d5037953db2a6beca888ce7783f207678d52239f0b054ab`  
		Last Modified: Tue, 17 Mar 2026 01:16:06 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80030bcef0d1515fd0bf3371bf1813444b6a7dd75363687403f34f7fbd689f47`  
		Last Modified: Tue, 17 Mar 2026 01:16:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19232562da027e1b978e40983a63aa4b932d406793b7bea774c62d0051567096`  
		Last Modified: Tue, 17 Mar 2026 01:16:07 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97e7c37ba3dfa013d3ddd63ce2968f8ff02d26b1001243b795a8390f27410b5`  
		Last Modified: Tue, 17 Mar 2026 01:16:07 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.14-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e34d019b82610f0133a441648010ad80682418c07c5ce43a142d4b564cafc969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b94f700e7376d22e3a7304430fc82280ecb6572ce8aa95b423a2ae06dbf1398`

```dockerfile
```

-	Layers:
	-	`sha256:1b7e4053e3be085fbadb553c8575a9fcfef9a7a592ba4d872b484863b71a5f3e`  
		Last Modified: Tue, 17 Mar 2026 01:16:06 GMT  
		Size: 25.4 KB (25423 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.14.14`

```console
$ docker pull clickhouse@sha256:b59cd7dc15fc4e07879149a3c3c06a0eccd14ccb8e80877756ecbf1a9cbeb74e
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
$ docker pull clickhouse@sha256:665f0d2d923456af1fb9fb7ce7d4ed6834592b747256d5aedc7a43fbbe135310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193810367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739f9cb8a27aff7bab921735652a16a7413e448d65fb87029fbd3ad9043bb020`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:23 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:23 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:23 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:23 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:23 GMT
ARG VERSION=25.3.14.14
# Tue, 17 Mar 2026 01:15:23 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:15:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:15:49 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:15:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:15:49 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:15:49 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:15:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3378707c4664419239f73413d0d64cc47512c8c4d2277b83766d0663fc56ee06`  
		Last Modified: Tue, 17 Mar 2026 01:16:06 GMT  
		Size: 7.1 MB (7128017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c23b4cfc6a6b13daa97de2f89e8b8bdf88f720b6844e6c4aa944112b18abdf1`  
		Last Modified: Tue, 17 Mar 2026 01:16:09 GMT  
		Size: 158.4 MB (158423075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d5949d99157b0c7b1f549b8906dcb08667b9b7be89944afb54a57c94302ea9`  
		Last Modified: Tue, 17 Mar 2026 01:16:06 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9487f671e7c9bd07d5037953db2a6beca888ce7783f207678d52239f0b054ab`  
		Last Modified: Tue, 17 Mar 2026 01:16:06 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80030bcef0d1515fd0bf3371bf1813444b6a7dd75363687403f34f7fbd689f47`  
		Last Modified: Tue, 17 Mar 2026 01:16:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19232562da027e1b978e40983a63aa4b932d406793b7bea774c62d0051567096`  
		Last Modified: Tue, 17 Mar 2026 01:16:07 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97e7c37ba3dfa013d3ddd63ce2968f8ff02d26b1001243b795a8390f27410b5`  
		Last Modified: Tue, 17 Mar 2026 01:16:07 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.14.14` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e34d019b82610f0133a441648010ad80682418c07c5ce43a142d4b564cafc969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b94f700e7376d22e3a7304430fc82280ecb6572ce8aa95b423a2ae06dbf1398`

```dockerfile
```

-	Layers:
	-	`sha256:1b7e4053e3be085fbadb553c8575a9fcfef9a7a592ba4d872b484863b71a5f3e`  
		Last Modified: Tue, 17 Mar 2026 01:16:06 GMT  
		Size: 25.4 KB (25423 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.14.14-jammy`

```console
$ docker pull clickhouse@sha256:b59cd7dc15fc4e07879149a3c3c06a0eccd14ccb8e80877756ecbf1a9cbeb74e
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
$ docker pull clickhouse@sha256:665f0d2d923456af1fb9fb7ce7d4ed6834592b747256d5aedc7a43fbbe135310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193810367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739f9cb8a27aff7bab921735652a16a7413e448d65fb87029fbd3ad9043bb020`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:23 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:23 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:23 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:23 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:23 GMT
ARG VERSION=25.3.14.14
# Tue, 17 Mar 2026 01:15:23 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:15:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:15:49 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:15:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:15:49 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:15:49 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:15:49 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:15:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3378707c4664419239f73413d0d64cc47512c8c4d2277b83766d0663fc56ee06`  
		Last Modified: Tue, 17 Mar 2026 01:16:06 GMT  
		Size: 7.1 MB (7128017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c23b4cfc6a6b13daa97de2f89e8b8bdf88f720b6844e6c4aa944112b18abdf1`  
		Last Modified: Tue, 17 Mar 2026 01:16:09 GMT  
		Size: 158.4 MB (158423075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d5949d99157b0c7b1f549b8906dcb08667b9b7be89944afb54a57c94302ea9`  
		Last Modified: Tue, 17 Mar 2026 01:16:06 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9487f671e7c9bd07d5037953db2a6beca888ce7783f207678d52239f0b054ab`  
		Last Modified: Tue, 17 Mar 2026 01:16:06 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80030bcef0d1515fd0bf3371bf1813444b6a7dd75363687403f34f7fbd689f47`  
		Last Modified: Tue, 17 Mar 2026 01:16:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19232562da027e1b978e40983a63aa4b932d406793b7bea774c62d0051567096`  
		Last Modified: Tue, 17 Mar 2026 01:16:07 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97e7c37ba3dfa013d3ddd63ce2968f8ff02d26b1001243b795a8390f27410b5`  
		Last Modified: Tue, 17 Mar 2026 01:16:07 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.14.14-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e34d019b82610f0133a441648010ad80682418c07c5ce43a142d4b564cafc969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b94f700e7376d22e3a7304430fc82280ecb6572ce8aa95b423a2ae06dbf1398`

```dockerfile
```

-	Layers:
	-	`sha256:1b7e4053e3be085fbadb553c8575a9fcfef9a7a592ba4d872b484863b71a5f3e`  
		Last Modified: Tue, 17 Mar 2026 01:16:06 GMT  
		Size: 25.4 KB (25423 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8`

```console
$ docker pull clickhouse@sha256:3b6b075ed3ed9bc9bd231bc9a97eb37805c4248737f45c3a2d7e803b7892b03f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8` - linux; amd64

```console
$ docker pull clickhouse@sha256:51db9b19b7faacb227be96bb32f8fa41e77e291617771052643682a004aab6d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (228956961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b173876c47035abf1e353aeafae7f806ec2ece30749bcd55dd6fdc95d58970`
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
# Fri, 06 Mar 2026 18:18:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:33 GMT
ARG VERSION=25.8.18.1
# Fri, 06 Mar 2026 18:18:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:20:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:20:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:20:06 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:20:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:20:06 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:20:06 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:20:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf1cd52a322630e05ff2887999d6093183d6952c5afbc0c1f04cadda3151a63`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 7.6 MB (7598399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f15c8a78545882c5b5d20de07c3b2ce913b72c7618e71dc7406f47fd2ec77f3`  
		Last Modified: Fri, 06 Mar 2026 18:20:29 GMT  
		Size: 191.0 MB (190951174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14499c88faf4f3259b248f6ef835d54060e4f6446a9a7a4d77d2aeb560008c57`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4639d26d5fea888c1dc9315370cedc0227c9a9b5da6b9aaafb06bd416b0c0cf4`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e7e125ac0ce703736242bb82a395bb092a6dc1a71fa212843686348c9d6427`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f3b4d918f0a194272c136d63f8ea5c7fc91d732070e4c39ffe7492e4e5e825`  
		Last Modified: Fri, 06 Mar 2026 18:20:26 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4788a9bd7152d1a8751ed266ec4f19f881c953b4c2dd9ca17e719aacf9eea9e`  
		Last Modified: Fri, 06 Mar 2026 18:20:26 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3f871562ee569f41853247e03faa124152cbc02b26ad4af635e9f48869262511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907bce1944962a711dcb7b0a0e2bc3e0ef2209a91fec34bb4ef7528e812caf02`

```dockerfile
```

-	Layers:
	-	`sha256:6023ddd3ff61c0a42e800fb01b931ee54d710e507a9aa8b5fa7ead51695cc85a`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 26.0 KB (26034 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:48af527e13d25cc4eafe38faa62c7c16f4290dffefdb995220f37db57089c285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.9 MB (213852131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64554b1cdecae50f2e1a969f91c4f7d4796ca9828ba02b4698c036b3219a9545`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:40 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:40 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:40 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:40 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:40 GMT
ARG VERSION=25.8.18.1
# Tue, 17 Mar 2026 01:15:40 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:16:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:16:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:16:10 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:16:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:16:10 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:16:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:16:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624738f5fd92e7b367ade3723b173a32feb25a63a3b43c65b9c17f8b2556f391`  
		Last Modified: Tue, 17 Mar 2026 01:16:29 GMT  
		Size: 7.6 MB (7577383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345ce4ca8b8b3838829ae4173c40639b95d650c11e081e0215c83348a8365318`  
		Last Modified: Tue, 17 Mar 2026 01:16:32 GMT  
		Size: 178.0 MB (178015700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7387612f85f8dfa2149b3d338066e137bd01eecd6bc5dcdceda97d7f90678cb`  
		Last Modified: Tue, 17 Mar 2026 01:16:28 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4cec9b7d967bbb3b133fd7e8b8b1975429816982d1d3279a8c7e7aaef10bc9`  
		Last Modified: Tue, 17 Mar 2026 01:16:29 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284037406a24a7bbebec076c913f28e75c5e11ff502ef87ed70e1d14fbad4a00`  
		Last Modified: Tue, 17 Mar 2026 01:16:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad87031f83bb1367e0ba7889fa35749b0c76a4bf1171154bd5baa111f4e2b3d`  
		Last Modified: Tue, 17 Mar 2026 01:16:30 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2ae45d675d5b9b73537a5eadac12c0e86837a05dc14a287ca973e53fbd58b1`  
		Last Modified: Tue, 17 Mar 2026 01:16:30 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:36df80ae326769e4e214e790e6df6b722bef5915201d50061cd44349c482fd17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0d9829330d0bc51c1346d6969d2f634156ad6e6d512a5d0ee26ea1fc7afcfd`

```dockerfile
```

-	Layers:
	-	`sha256:87b465e3d96244b1a0315152911bb75af8d48146c0ecf3e620557b11f4fed01c`  
		Last Modified: Tue, 17 Mar 2026 01:16:28 GMT  
		Size: 26.2 KB (26245 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8-jammy`

```console
$ docker pull clickhouse@sha256:3b6b075ed3ed9bc9bd231bc9a97eb37805c4248737f45c3a2d7e803b7892b03f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:51db9b19b7faacb227be96bb32f8fa41e77e291617771052643682a004aab6d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (228956961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b173876c47035abf1e353aeafae7f806ec2ece30749bcd55dd6fdc95d58970`
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
# Fri, 06 Mar 2026 18:18:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:33 GMT
ARG VERSION=25.8.18.1
# Fri, 06 Mar 2026 18:18:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:20:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:20:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:20:06 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:20:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:20:06 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:20:06 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:20:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf1cd52a322630e05ff2887999d6093183d6952c5afbc0c1f04cadda3151a63`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 7.6 MB (7598399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f15c8a78545882c5b5d20de07c3b2ce913b72c7618e71dc7406f47fd2ec77f3`  
		Last Modified: Fri, 06 Mar 2026 18:20:29 GMT  
		Size: 191.0 MB (190951174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14499c88faf4f3259b248f6ef835d54060e4f6446a9a7a4d77d2aeb560008c57`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4639d26d5fea888c1dc9315370cedc0227c9a9b5da6b9aaafb06bd416b0c0cf4`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e7e125ac0ce703736242bb82a395bb092a6dc1a71fa212843686348c9d6427`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f3b4d918f0a194272c136d63f8ea5c7fc91d732070e4c39ffe7492e4e5e825`  
		Last Modified: Fri, 06 Mar 2026 18:20:26 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4788a9bd7152d1a8751ed266ec4f19f881c953b4c2dd9ca17e719aacf9eea9e`  
		Last Modified: Fri, 06 Mar 2026 18:20:26 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3f871562ee569f41853247e03faa124152cbc02b26ad4af635e9f48869262511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907bce1944962a711dcb7b0a0e2bc3e0ef2209a91fec34bb4ef7528e812caf02`

```dockerfile
```

-	Layers:
	-	`sha256:6023ddd3ff61c0a42e800fb01b931ee54d710e507a9aa8b5fa7ead51695cc85a`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 26.0 KB (26034 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:48af527e13d25cc4eafe38faa62c7c16f4290dffefdb995220f37db57089c285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.9 MB (213852131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64554b1cdecae50f2e1a969f91c4f7d4796ca9828ba02b4698c036b3219a9545`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:40 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:40 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:40 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:40 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:40 GMT
ARG VERSION=25.8.18.1
# Tue, 17 Mar 2026 01:15:40 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:16:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:16:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:16:10 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:16:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:16:10 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:16:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:16:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624738f5fd92e7b367ade3723b173a32feb25a63a3b43c65b9c17f8b2556f391`  
		Last Modified: Tue, 17 Mar 2026 01:16:29 GMT  
		Size: 7.6 MB (7577383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345ce4ca8b8b3838829ae4173c40639b95d650c11e081e0215c83348a8365318`  
		Last Modified: Tue, 17 Mar 2026 01:16:32 GMT  
		Size: 178.0 MB (178015700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7387612f85f8dfa2149b3d338066e137bd01eecd6bc5dcdceda97d7f90678cb`  
		Last Modified: Tue, 17 Mar 2026 01:16:28 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4cec9b7d967bbb3b133fd7e8b8b1975429816982d1d3279a8c7e7aaef10bc9`  
		Last Modified: Tue, 17 Mar 2026 01:16:29 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284037406a24a7bbebec076c913f28e75c5e11ff502ef87ed70e1d14fbad4a00`  
		Last Modified: Tue, 17 Mar 2026 01:16:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad87031f83bb1367e0ba7889fa35749b0c76a4bf1171154bd5baa111f4e2b3d`  
		Last Modified: Tue, 17 Mar 2026 01:16:30 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2ae45d675d5b9b73537a5eadac12c0e86837a05dc14a287ca973e53fbd58b1`  
		Last Modified: Tue, 17 Mar 2026 01:16:30 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:36df80ae326769e4e214e790e6df6b722bef5915201d50061cd44349c482fd17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0d9829330d0bc51c1346d6969d2f634156ad6e6d512a5d0ee26ea1fc7afcfd`

```dockerfile
```

-	Layers:
	-	`sha256:87b465e3d96244b1a0315152911bb75af8d48146c0ecf3e620557b11f4fed01c`  
		Last Modified: Tue, 17 Mar 2026 01:16:28 GMT  
		Size: 26.2 KB (26245 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.18`

```console
$ docker pull clickhouse@sha256:3b6b075ed3ed9bc9bd231bc9a97eb37805c4248737f45c3a2d7e803b7892b03f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.18` - linux; amd64

```console
$ docker pull clickhouse@sha256:51db9b19b7faacb227be96bb32f8fa41e77e291617771052643682a004aab6d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (228956961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b173876c47035abf1e353aeafae7f806ec2ece30749bcd55dd6fdc95d58970`
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
# Fri, 06 Mar 2026 18:18:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:33 GMT
ARG VERSION=25.8.18.1
# Fri, 06 Mar 2026 18:18:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:20:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:20:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:20:06 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:20:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:20:06 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:20:06 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:20:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf1cd52a322630e05ff2887999d6093183d6952c5afbc0c1f04cadda3151a63`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 7.6 MB (7598399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f15c8a78545882c5b5d20de07c3b2ce913b72c7618e71dc7406f47fd2ec77f3`  
		Last Modified: Fri, 06 Mar 2026 18:20:29 GMT  
		Size: 191.0 MB (190951174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14499c88faf4f3259b248f6ef835d54060e4f6446a9a7a4d77d2aeb560008c57`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4639d26d5fea888c1dc9315370cedc0227c9a9b5da6b9aaafb06bd416b0c0cf4`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e7e125ac0ce703736242bb82a395bb092a6dc1a71fa212843686348c9d6427`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f3b4d918f0a194272c136d63f8ea5c7fc91d732070e4c39ffe7492e4e5e825`  
		Last Modified: Fri, 06 Mar 2026 18:20:26 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4788a9bd7152d1a8751ed266ec4f19f881c953b4c2dd9ca17e719aacf9eea9e`  
		Last Modified: Fri, 06 Mar 2026 18:20:26 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.18` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3f871562ee569f41853247e03faa124152cbc02b26ad4af635e9f48869262511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907bce1944962a711dcb7b0a0e2bc3e0ef2209a91fec34bb4ef7528e812caf02`

```dockerfile
```

-	Layers:
	-	`sha256:6023ddd3ff61c0a42e800fb01b931ee54d710e507a9aa8b5fa7ead51695cc85a`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 26.0 KB (26034 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.18` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:48af527e13d25cc4eafe38faa62c7c16f4290dffefdb995220f37db57089c285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.9 MB (213852131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64554b1cdecae50f2e1a969f91c4f7d4796ca9828ba02b4698c036b3219a9545`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:40 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:40 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:40 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:40 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:40 GMT
ARG VERSION=25.8.18.1
# Tue, 17 Mar 2026 01:15:40 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:16:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:16:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:16:10 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:16:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:16:10 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:16:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:16:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624738f5fd92e7b367ade3723b173a32feb25a63a3b43c65b9c17f8b2556f391`  
		Last Modified: Tue, 17 Mar 2026 01:16:29 GMT  
		Size: 7.6 MB (7577383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345ce4ca8b8b3838829ae4173c40639b95d650c11e081e0215c83348a8365318`  
		Last Modified: Tue, 17 Mar 2026 01:16:32 GMT  
		Size: 178.0 MB (178015700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7387612f85f8dfa2149b3d338066e137bd01eecd6bc5dcdceda97d7f90678cb`  
		Last Modified: Tue, 17 Mar 2026 01:16:28 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4cec9b7d967bbb3b133fd7e8b8b1975429816982d1d3279a8c7e7aaef10bc9`  
		Last Modified: Tue, 17 Mar 2026 01:16:29 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284037406a24a7bbebec076c913f28e75c5e11ff502ef87ed70e1d14fbad4a00`  
		Last Modified: Tue, 17 Mar 2026 01:16:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad87031f83bb1367e0ba7889fa35749b0c76a4bf1171154bd5baa111f4e2b3d`  
		Last Modified: Tue, 17 Mar 2026 01:16:30 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2ae45d675d5b9b73537a5eadac12c0e86837a05dc14a287ca973e53fbd58b1`  
		Last Modified: Tue, 17 Mar 2026 01:16:30 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.18` - unknown; unknown

```console
$ docker pull clickhouse@sha256:36df80ae326769e4e214e790e6df6b722bef5915201d50061cd44349c482fd17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0d9829330d0bc51c1346d6969d2f634156ad6e6d512a5d0ee26ea1fc7afcfd`

```dockerfile
```

-	Layers:
	-	`sha256:87b465e3d96244b1a0315152911bb75af8d48146c0ecf3e620557b11f4fed01c`  
		Last Modified: Tue, 17 Mar 2026 01:16:28 GMT  
		Size: 26.2 KB (26245 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.18-jammy`

```console
$ docker pull clickhouse@sha256:3b6b075ed3ed9bc9bd231bc9a97eb37805c4248737f45c3a2d7e803b7892b03f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.18-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:51db9b19b7faacb227be96bb32f8fa41e77e291617771052643682a004aab6d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (228956961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b173876c47035abf1e353aeafae7f806ec2ece30749bcd55dd6fdc95d58970`
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
# Fri, 06 Mar 2026 18:18:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:33 GMT
ARG VERSION=25.8.18.1
# Fri, 06 Mar 2026 18:18:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:20:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:20:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:20:06 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:20:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:20:06 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:20:06 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:20:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf1cd52a322630e05ff2887999d6093183d6952c5afbc0c1f04cadda3151a63`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 7.6 MB (7598399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f15c8a78545882c5b5d20de07c3b2ce913b72c7618e71dc7406f47fd2ec77f3`  
		Last Modified: Fri, 06 Mar 2026 18:20:29 GMT  
		Size: 191.0 MB (190951174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14499c88faf4f3259b248f6ef835d54060e4f6446a9a7a4d77d2aeb560008c57`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4639d26d5fea888c1dc9315370cedc0227c9a9b5da6b9aaafb06bd416b0c0cf4`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e7e125ac0ce703736242bb82a395bb092a6dc1a71fa212843686348c9d6427`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f3b4d918f0a194272c136d63f8ea5c7fc91d732070e4c39ffe7492e4e5e825`  
		Last Modified: Fri, 06 Mar 2026 18:20:26 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4788a9bd7152d1a8751ed266ec4f19f881c953b4c2dd9ca17e719aacf9eea9e`  
		Last Modified: Fri, 06 Mar 2026 18:20:26 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.18-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3f871562ee569f41853247e03faa124152cbc02b26ad4af635e9f48869262511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907bce1944962a711dcb7b0a0e2bc3e0ef2209a91fec34bb4ef7528e812caf02`

```dockerfile
```

-	Layers:
	-	`sha256:6023ddd3ff61c0a42e800fb01b931ee54d710e507a9aa8b5fa7ead51695cc85a`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 26.0 KB (26034 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.18-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:48af527e13d25cc4eafe38faa62c7c16f4290dffefdb995220f37db57089c285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.9 MB (213852131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64554b1cdecae50f2e1a969f91c4f7d4796ca9828ba02b4698c036b3219a9545`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:40 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:40 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:40 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:40 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:40 GMT
ARG VERSION=25.8.18.1
# Tue, 17 Mar 2026 01:15:40 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:16:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:16:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:16:10 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:16:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:16:10 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:16:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:16:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624738f5fd92e7b367ade3723b173a32feb25a63a3b43c65b9c17f8b2556f391`  
		Last Modified: Tue, 17 Mar 2026 01:16:29 GMT  
		Size: 7.6 MB (7577383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345ce4ca8b8b3838829ae4173c40639b95d650c11e081e0215c83348a8365318`  
		Last Modified: Tue, 17 Mar 2026 01:16:32 GMT  
		Size: 178.0 MB (178015700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7387612f85f8dfa2149b3d338066e137bd01eecd6bc5dcdceda97d7f90678cb`  
		Last Modified: Tue, 17 Mar 2026 01:16:28 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4cec9b7d967bbb3b133fd7e8b8b1975429816982d1d3279a8c7e7aaef10bc9`  
		Last Modified: Tue, 17 Mar 2026 01:16:29 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284037406a24a7bbebec076c913f28e75c5e11ff502ef87ed70e1d14fbad4a00`  
		Last Modified: Tue, 17 Mar 2026 01:16:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad87031f83bb1367e0ba7889fa35749b0c76a4bf1171154bd5baa111f4e2b3d`  
		Last Modified: Tue, 17 Mar 2026 01:16:30 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2ae45d675d5b9b73537a5eadac12c0e86837a05dc14a287ca973e53fbd58b1`  
		Last Modified: Tue, 17 Mar 2026 01:16:30 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.18-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:36df80ae326769e4e214e790e6df6b722bef5915201d50061cd44349c482fd17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0d9829330d0bc51c1346d6969d2f634156ad6e6d512a5d0ee26ea1fc7afcfd`

```dockerfile
```

-	Layers:
	-	`sha256:87b465e3d96244b1a0315152911bb75af8d48146c0ecf3e620557b11f4fed01c`  
		Last Modified: Tue, 17 Mar 2026 01:16:28 GMT  
		Size: 26.2 KB (26245 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.18.1`

```console
$ docker pull clickhouse@sha256:3b6b075ed3ed9bc9bd231bc9a97eb37805c4248737f45c3a2d7e803b7892b03f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.18.1` - linux; amd64

```console
$ docker pull clickhouse@sha256:51db9b19b7faacb227be96bb32f8fa41e77e291617771052643682a004aab6d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (228956961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b173876c47035abf1e353aeafae7f806ec2ece30749bcd55dd6fdc95d58970`
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
# Fri, 06 Mar 2026 18:18:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:33 GMT
ARG VERSION=25.8.18.1
# Fri, 06 Mar 2026 18:18:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:20:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:20:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:20:06 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:20:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:20:06 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:20:06 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:20:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf1cd52a322630e05ff2887999d6093183d6952c5afbc0c1f04cadda3151a63`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 7.6 MB (7598399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f15c8a78545882c5b5d20de07c3b2ce913b72c7618e71dc7406f47fd2ec77f3`  
		Last Modified: Fri, 06 Mar 2026 18:20:29 GMT  
		Size: 191.0 MB (190951174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14499c88faf4f3259b248f6ef835d54060e4f6446a9a7a4d77d2aeb560008c57`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4639d26d5fea888c1dc9315370cedc0227c9a9b5da6b9aaafb06bd416b0c0cf4`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e7e125ac0ce703736242bb82a395bb092a6dc1a71fa212843686348c9d6427`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f3b4d918f0a194272c136d63f8ea5c7fc91d732070e4c39ffe7492e4e5e825`  
		Last Modified: Fri, 06 Mar 2026 18:20:26 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4788a9bd7152d1a8751ed266ec4f19f881c953b4c2dd9ca17e719aacf9eea9e`  
		Last Modified: Fri, 06 Mar 2026 18:20:26 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.18.1` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3f871562ee569f41853247e03faa124152cbc02b26ad4af635e9f48869262511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907bce1944962a711dcb7b0a0e2bc3e0ef2209a91fec34bb4ef7528e812caf02`

```dockerfile
```

-	Layers:
	-	`sha256:6023ddd3ff61c0a42e800fb01b931ee54d710e507a9aa8b5fa7ead51695cc85a`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 26.0 KB (26034 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.18.1` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:48af527e13d25cc4eafe38faa62c7c16f4290dffefdb995220f37db57089c285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.9 MB (213852131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64554b1cdecae50f2e1a969f91c4f7d4796ca9828ba02b4698c036b3219a9545`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:40 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:40 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:40 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:40 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:40 GMT
ARG VERSION=25.8.18.1
# Tue, 17 Mar 2026 01:15:40 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:16:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:16:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:16:10 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:16:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:16:10 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:16:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:16:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624738f5fd92e7b367ade3723b173a32feb25a63a3b43c65b9c17f8b2556f391`  
		Last Modified: Tue, 17 Mar 2026 01:16:29 GMT  
		Size: 7.6 MB (7577383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345ce4ca8b8b3838829ae4173c40639b95d650c11e081e0215c83348a8365318`  
		Last Modified: Tue, 17 Mar 2026 01:16:32 GMT  
		Size: 178.0 MB (178015700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7387612f85f8dfa2149b3d338066e137bd01eecd6bc5dcdceda97d7f90678cb`  
		Last Modified: Tue, 17 Mar 2026 01:16:28 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4cec9b7d967bbb3b133fd7e8b8b1975429816982d1d3279a8c7e7aaef10bc9`  
		Last Modified: Tue, 17 Mar 2026 01:16:29 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284037406a24a7bbebec076c913f28e75c5e11ff502ef87ed70e1d14fbad4a00`  
		Last Modified: Tue, 17 Mar 2026 01:16:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad87031f83bb1367e0ba7889fa35749b0c76a4bf1171154bd5baa111f4e2b3d`  
		Last Modified: Tue, 17 Mar 2026 01:16:30 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2ae45d675d5b9b73537a5eadac12c0e86837a05dc14a287ca973e53fbd58b1`  
		Last Modified: Tue, 17 Mar 2026 01:16:30 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.18.1` - unknown; unknown

```console
$ docker pull clickhouse@sha256:36df80ae326769e4e214e790e6df6b722bef5915201d50061cd44349c482fd17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0d9829330d0bc51c1346d6969d2f634156ad6e6d512a5d0ee26ea1fc7afcfd`

```dockerfile
```

-	Layers:
	-	`sha256:87b465e3d96244b1a0315152911bb75af8d48146c0ecf3e620557b11f4fed01c`  
		Last Modified: Tue, 17 Mar 2026 01:16:28 GMT  
		Size: 26.2 KB (26245 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.18.1-jammy`

```console
$ docker pull clickhouse@sha256:3b6b075ed3ed9bc9bd231bc9a97eb37805c4248737f45c3a2d7e803b7892b03f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.18.1-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:51db9b19b7faacb227be96bb32f8fa41e77e291617771052643682a004aab6d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (228956961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b173876c47035abf1e353aeafae7f806ec2ece30749bcd55dd6fdc95d58970`
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
# Fri, 06 Mar 2026 18:18:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:33 GMT
ARG VERSION=25.8.18.1
# Fri, 06 Mar 2026 18:18:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:20:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:20:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:20:06 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:20:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:20:06 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:20:06 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:20:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf1cd52a322630e05ff2887999d6093183d6952c5afbc0c1f04cadda3151a63`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 7.6 MB (7598399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f15c8a78545882c5b5d20de07c3b2ce913b72c7618e71dc7406f47fd2ec77f3`  
		Last Modified: Fri, 06 Mar 2026 18:20:29 GMT  
		Size: 191.0 MB (190951174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14499c88faf4f3259b248f6ef835d54060e4f6446a9a7a4d77d2aeb560008c57`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4639d26d5fea888c1dc9315370cedc0227c9a9b5da6b9aaafb06bd416b0c0cf4`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e7e125ac0ce703736242bb82a395bb092a6dc1a71fa212843686348c9d6427`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f3b4d918f0a194272c136d63f8ea5c7fc91d732070e4c39ffe7492e4e5e825`  
		Last Modified: Fri, 06 Mar 2026 18:20:26 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4788a9bd7152d1a8751ed266ec4f19f881c953b4c2dd9ca17e719aacf9eea9e`  
		Last Modified: Fri, 06 Mar 2026 18:20:26 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.18.1-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3f871562ee569f41853247e03faa124152cbc02b26ad4af635e9f48869262511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907bce1944962a711dcb7b0a0e2bc3e0ef2209a91fec34bb4ef7528e812caf02`

```dockerfile
```

-	Layers:
	-	`sha256:6023ddd3ff61c0a42e800fb01b931ee54d710e507a9aa8b5fa7ead51695cc85a`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 26.0 KB (26034 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.18.1-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:48af527e13d25cc4eafe38faa62c7c16f4290dffefdb995220f37db57089c285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.9 MB (213852131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64554b1cdecae50f2e1a969f91c4f7d4796ca9828ba02b4698c036b3219a9545`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:40 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:40 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:40 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:40 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:40 GMT
ARG VERSION=25.8.18.1
# Tue, 17 Mar 2026 01:15:40 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:16:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:16:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:16:10 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:16:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:16:10 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:16:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:16:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624738f5fd92e7b367ade3723b173a32feb25a63a3b43c65b9c17f8b2556f391`  
		Last Modified: Tue, 17 Mar 2026 01:16:29 GMT  
		Size: 7.6 MB (7577383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345ce4ca8b8b3838829ae4173c40639b95d650c11e081e0215c83348a8365318`  
		Last Modified: Tue, 17 Mar 2026 01:16:32 GMT  
		Size: 178.0 MB (178015700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7387612f85f8dfa2149b3d338066e137bd01eecd6bc5dcdceda97d7f90678cb`  
		Last Modified: Tue, 17 Mar 2026 01:16:28 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4cec9b7d967bbb3b133fd7e8b8b1975429816982d1d3279a8c7e7aaef10bc9`  
		Last Modified: Tue, 17 Mar 2026 01:16:29 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284037406a24a7bbebec076c913f28e75c5e11ff502ef87ed70e1d14fbad4a00`  
		Last Modified: Tue, 17 Mar 2026 01:16:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad87031f83bb1367e0ba7889fa35749b0c76a4bf1171154bd5baa111f4e2b3d`  
		Last Modified: Tue, 17 Mar 2026 01:16:30 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2ae45d675d5b9b73537a5eadac12c0e86837a05dc14a287ca973e53fbd58b1`  
		Last Modified: Tue, 17 Mar 2026 01:16:30 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.18.1-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:36df80ae326769e4e214e790e6df6b722bef5915201d50061cd44349c482fd17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0d9829330d0bc51c1346d6969d2f634156ad6e6d512a5d0ee26ea1fc7afcfd`

```dockerfile
```

-	Layers:
	-	`sha256:87b465e3d96244b1a0315152911bb75af8d48146c0ecf3e620557b11f4fed01c`  
		Last Modified: Tue, 17 Mar 2026 01:16:28 GMT  
		Size: 26.2 KB (26245 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1`

```console
$ docker pull clickhouse@sha256:e963c19fff30164a740c669a92af1bb7000b75f312762ffc626e53bfbf1ce3c9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1` - linux; amd64

```console
$ docker pull clickhouse@sha256:7a5fb226f81ff050cd0e717e4b0fe12270742e616905d2243ed419f7aa6d8e81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (246001744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccae8563d00171c05b6b46aac39d24bcb38e9c08f28eb1ae90291e4ecc1f3fff`
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
# Fri, 06 Mar 2026 18:18:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:33 GMT
ARG VERSION=26.1.4.35
# Fri, 06 Mar 2026 18:18:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:18:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:18:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:19:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:19:00 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:19:00 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:19:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:19:01 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:19:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:19:01 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:19:01 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:19:01 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:19:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf1cd52a322630e05ff2887999d6093183d6952c5afbc0c1f04cadda3151a63`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 7.6 MB (7598399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fef26d9d2fca551739567e01ef730c91fa91edf0c8ef1f2ed9f72735dfc7bea`  
		Last Modified: Fri, 06 Mar 2026 18:19:27 GMT  
		Size: 208.0 MB (207995930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011531cdbf3f055c3088541a8b344b155ce558ecc075259c1ce7c4df54a7cbc2`  
		Last Modified: Fri, 06 Mar 2026 18:19:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da1132809fcc99ea72c0b0cb364d991bcc4585804ff5607f8a625ed10cd5860`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5674fe75400fe75f63fc10b32e1a627b74d84c50f4db3e339f6c8ad23a2126`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29e0614378578fd665364c6a2e71e0952c32566c8ebc2f2a23093666f41d160`  
		Last Modified: Fri, 06 Mar 2026 18:19:24 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f114ba2f50295f78252fb4289608de328d11683d258383cf8121bcdd1f90861f`  
		Last Modified: Fri, 06 Mar 2026 18:19:24 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f9e3292979f8379b1996be583504c5d74d1ed6ba66ed3ca5a118895c1c8c01fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b33d5972c27b9d8d24ad3ffbca659262785fb0ad2182daafdbaf9b24655fe4eb`

```dockerfile
```

-	Layers:
	-	`sha256:1b2f58f0c29777bd0357a391cc09801c7129374079468f633a030a2850a45f7e`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 25.4 KB (25418 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:dfb15848187627df8c5cbde28c2bf9708b8eb80028c34d4a7d3d9e9955476261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228246926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c782508554b248a41a6d2fbb3dde7d64bde8ee120e8309d59368bfc163edf3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:25 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:25 GMT
ARG VERSION=26.1.4.35
# Tue, 17 Mar 2026 01:15:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:15:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:15:59 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:15:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:15:59 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:15:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:15:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6584dfb8e761d2835ed68cdc836e2caedfdd354cb02cce2a2beb546c773cd3ce`  
		Last Modified: Tue, 17 Mar 2026 01:16:19 GMT  
		Size: 7.6 MB (7577385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7debbd2fc19a0083e840610be32e23f2b10ead488e5a70937f2ba838cd90c961`  
		Last Modified: Tue, 17 Mar 2026 01:16:23 GMT  
		Size: 192.4 MB (192410468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7510a8afb0f61af1a5515d7e63c866a19877474052fefebdcdbcd4f77dd55f38`  
		Last Modified: Tue, 17 Mar 2026 01:16:19 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e75ec6f7eb02a26d013dd2847b9331ec80273f3e51783cc88e16b5347fb588c`  
		Last Modified: Tue, 17 Mar 2026 01:16:19 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad770cf2515a681a5c431f760d32a45233948add498a917de393218707359004`  
		Last Modified: Tue, 17 Mar 2026 01:16:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fff4834048bf7c50f0a8494a01fda8d6ed8be6d3b2460ca210751dfce6d2b8b`  
		Last Modified: Tue, 17 Mar 2026 01:16:20 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcef26757561469ac2de381b099e8827f9a0a91257c6de403ffce19fba43d49`  
		Last Modified: Tue, 17 Mar 2026 01:16:21 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1` - unknown; unknown

```console
$ docker pull clickhouse@sha256:30040edcfe86febe2b72ff22affbb093cca9b1df31fe6bed4e203a1110f7204e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd5ced716c0c43d6d3bee423fffbfa224ef2eea5fc59669300f81f7a10ba5355`

```dockerfile
```

-	Layers:
	-	`sha256:5b85ed9433df0c1edceeb1fc5b52fa675833b4971b9bbf2f166dd6be63d5b3b4`  
		Last Modified: Tue, 17 Mar 2026 01:16:19 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1-jammy`

```console
$ docker pull clickhouse@sha256:e963c19fff30164a740c669a92af1bb7000b75f312762ffc626e53bfbf1ce3c9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:7a5fb226f81ff050cd0e717e4b0fe12270742e616905d2243ed419f7aa6d8e81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (246001744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccae8563d00171c05b6b46aac39d24bcb38e9c08f28eb1ae90291e4ecc1f3fff`
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
# Fri, 06 Mar 2026 18:18:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:33 GMT
ARG VERSION=26.1.4.35
# Fri, 06 Mar 2026 18:18:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:18:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:18:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:19:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:19:00 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:19:00 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:19:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:19:01 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:19:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:19:01 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:19:01 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:19:01 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:19:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf1cd52a322630e05ff2887999d6093183d6952c5afbc0c1f04cadda3151a63`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 7.6 MB (7598399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fef26d9d2fca551739567e01ef730c91fa91edf0c8ef1f2ed9f72735dfc7bea`  
		Last Modified: Fri, 06 Mar 2026 18:19:27 GMT  
		Size: 208.0 MB (207995930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011531cdbf3f055c3088541a8b344b155ce558ecc075259c1ce7c4df54a7cbc2`  
		Last Modified: Fri, 06 Mar 2026 18:19:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da1132809fcc99ea72c0b0cb364d991bcc4585804ff5607f8a625ed10cd5860`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5674fe75400fe75f63fc10b32e1a627b74d84c50f4db3e339f6c8ad23a2126`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29e0614378578fd665364c6a2e71e0952c32566c8ebc2f2a23093666f41d160`  
		Last Modified: Fri, 06 Mar 2026 18:19:24 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f114ba2f50295f78252fb4289608de328d11683d258383cf8121bcdd1f90861f`  
		Last Modified: Fri, 06 Mar 2026 18:19:24 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f9e3292979f8379b1996be583504c5d74d1ed6ba66ed3ca5a118895c1c8c01fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b33d5972c27b9d8d24ad3ffbca659262785fb0ad2182daafdbaf9b24655fe4eb`

```dockerfile
```

-	Layers:
	-	`sha256:1b2f58f0c29777bd0357a391cc09801c7129374079468f633a030a2850a45f7e`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 25.4 KB (25418 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:dfb15848187627df8c5cbde28c2bf9708b8eb80028c34d4a7d3d9e9955476261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228246926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c782508554b248a41a6d2fbb3dde7d64bde8ee120e8309d59368bfc163edf3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:25 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:25 GMT
ARG VERSION=26.1.4.35
# Tue, 17 Mar 2026 01:15:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:15:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:15:59 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:15:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:15:59 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:15:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:15:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6584dfb8e761d2835ed68cdc836e2caedfdd354cb02cce2a2beb546c773cd3ce`  
		Last Modified: Tue, 17 Mar 2026 01:16:19 GMT  
		Size: 7.6 MB (7577385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7debbd2fc19a0083e840610be32e23f2b10ead488e5a70937f2ba838cd90c961`  
		Last Modified: Tue, 17 Mar 2026 01:16:23 GMT  
		Size: 192.4 MB (192410468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7510a8afb0f61af1a5515d7e63c866a19877474052fefebdcdbcd4f77dd55f38`  
		Last Modified: Tue, 17 Mar 2026 01:16:19 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e75ec6f7eb02a26d013dd2847b9331ec80273f3e51783cc88e16b5347fb588c`  
		Last Modified: Tue, 17 Mar 2026 01:16:19 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad770cf2515a681a5c431f760d32a45233948add498a917de393218707359004`  
		Last Modified: Tue, 17 Mar 2026 01:16:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fff4834048bf7c50f0a8494a01fda8d6ed8be6d3b2460ca210751dfce6d2b8b`  
		Last Modified: Tue, 17 Mar 2026 01:16:20 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcef26757561469ac2de381b099e8827f9a0a91257c6de403ffce19fba43d49`  
		Last Modified: Tue, 17 Mar 2026 01:16:21 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:30040edcfe86febe2b72ff22affbb093cca9b1df31fe6bed4e203a1110f7204e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd5ced716c0c43d6d3bee423fffbfa224ef2eea5fc59669300f81f7a10ba5355`

```dockerfile
```

-	Layers:
	-	`sha256:5b85ed9433df0c1edceeb1fc5b52fa675833b4971b9bbf2f166dd6be63d5b3b4`  
		Last Modified: Tue, 17 Mar 2026 01:16:19 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1.4`

```console
$ docker pull clickhouse@sha256:e963c19fff30164a740c669a92af1bb7000b75f312762ffc626e53bfbf1ce3c9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1.4` - linux; amd64

```console
$ docker pull clickhouse@sha256:7a5fb226f81ff050cd0e717e4b0fe12270742e616905d2243ed419f7aa6d8e81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (246001744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccae8563d00171c05b6b46aac39d24bcb38e9c08f28eb1ae90291e4ecc1f3fff`
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
# Fri, 06 Mar 2026 18:18:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:33 GMT
ARG VERSION=26.1.4.35
# Fri, 06 Mar 2026 18:18:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:18:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:18:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:19:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:19:00 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:19:00 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:19:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:19:01 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:19:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:19:01 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:19:01 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:19:01 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:19:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf1cd52a322630e05ff2887999d6093183d6952c5afbc0c1f04cadda3151a63`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 7.6 MB (7598399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fef26d9d2fca551739567e01ef730c91fa91edf0c8ef1f2ed9f72735dfc7bea`  
		Last Modified: Fri, 06 Mar 2026 18:19:27 GMT  
		Size: 208.0 MB (207995930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011531cdbf3f055c3088541a8b344b155ce558ecc075259c1ce7c4df54a7cbc2`  
		Last Modified: Fri, 06 Mar 2026 18:19:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da1132809fcc99ea72c0b0cb364d991bcc4585804ff5607f8a625ed10cd5860`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5674fe75400fe75f63fc10b32e1a627b74d84c50f4db3e339f6c8ad23a2126`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29e0614378578fd665364c6a2e71e0952c32566c8ebc2f2a23093666f41d160`  
		Last Modified: Fri, 06 Mar 2026 18:19:24 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f114ba2f50295f78252fb4289608de328d11683d258383cf8121bcdd1f90861f`  
		Last Modified: Fri, 06 Mar 2026 18:19:24 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f9e3292979f8379b1996be583504c5d74d1ed6ba66ed3ca5a118895c1c8c01fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b33d5972c27b9d8d24ad3ffbca659262785fb0ad2182daafdbaf9b24655fe4eb`

```dockerfile
```

-	Layers:
	-	`sha256:1b2f58f0c29777bd0357a391cc09801c7129374079468f633a030a2850a45f7e`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 25.4 KB (25418 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1.4` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:dfb15848187627df8c5cbde28c2bf9708b8eb80028c34d4a7d3d9e9955476261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228246926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c782508554b248a41a6d2fbb3dde7d64bde8ee120e8309d59368bfc163edf3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:25 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:25 GMT
ARG VERSION=26.1.4.35
# Tue, 17 Mar 2026 01:15:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:15:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:15:59 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:15:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:15:59 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:15:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:15:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6584dfb8e761d2835ed68cdc836e2caedfdd354cb02cce2a2beb546c773cd3ce`  
		Last Modified: Tue, 17 Mar 2026 01:16:19 GMT  
		Size: 7.6 MB (7577385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7debbd2fc19a0083e840610be32e23f2b10ead488e5a70937f2ba838cd90c961`  
		Last Modified: Tue, 17 Mar 2026 01:16:23 GMT  
		Size: 192.4 MB (192410468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7510a8afb0f61af1a5515d7e63c866a19877474052fefebdcdbcd4f77dd55f38`  
		Last Modified: Tue, 17 Mar 2026 01:16:19 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e75ec6f7eb02a26d013dd2847b9331ec80273f3e51783cc88e16b5347fb588c`  
		Last Modified: Tue, 17 Mar 2026 01:16:19 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad770cf2515a681a5c431f760d32a45233948add498a917de393218707359004`  
		Last Modified: Tue, 17 Mar 2026 01:16:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fff4834048bf7c50f0a8494a01fda8d6ed8be6d3b2460ca210751dfce6d2b8b`  
		Last Modified: Tue, 17 Mar 2026 01:16:20 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcef26757561469ac2de381b099e8827f9a0a91257c6de403ffce19fba43d49`  
		Last Modified: Tue, 17 Mar 2026 01:16:21 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:30040edcfe86febe2b72ff22affbb093cca9b1df31fe6bed4e203a1110f7204e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd5ced716c0c43d6d3bee423fffbfa224ef2eea5fc59669300f81f7a10ba5355`

```dockerfile
```

-	Layers:
	-	`sha256:5b85ed9433df0c1edceeb1fc5b52fa675833b4971b9bbf2f166dd6be63d5b3b4`  
		Last Modified: Tue, 17 Mar 2026 01:16:19 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1.4-jammy`

```console
$ docker pull clickhouse@sha256:e963c19fff30164a740c669a92af1bb7000b75f312762ffc626e53bfbf1ce3c9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1.4-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:7a5fb226f81ff050cd0e717e4b0fe12270742e616905d2243ed419f7aa6d8e81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (246001744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccae8563d00171c05b6b46aac39d24bcb38e9c08f28eb1ae90291e4ecc1f3fff`
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
# Fri, 06 Mar 2026 18:18:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:33 GMT
ARG VERSION=26.1.4.35
# Fri, 06 Mar 2026 18:18:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:18:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:18:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:19:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:19:00 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:19:00 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:19:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:19:01 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:19:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:19:01 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:19:01 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:19:01 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:19:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf1cd52a322630e05ff2887999d6093183d6952c5afbc0c1f04cadda3151a63`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 7.6 MB (7598399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fef26d9d2fca551739567e01ef730c91fa91edf0c8ef1f2ed9f72735dfc7bea`  
		Last Modified: Fri, 06 Mar 2026 18:19:27 GMT  
		Size: 208.0 MB (207995930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011531cdbf3f055c3088541a8b344b155ce558ecc075259c1ce7c4df54a7cbc2`  
		Last Modified: Fri, 06 Mar 2026 18:19:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da1132809fcc99ea72c0b0cb364d991bcc4585804ff5607f8a625ed10cd5860`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5674fe75400fe75f63fc10b32e1a627b74d84c50f4db3e339f6c8ad23a2126`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29e0614378578fd665364c6a2e71e0952c32566c8ebc2f2a23093666f41d160`  
		Last Modified: Fri, 06 Mar 2026 18:19:24 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f114ba2f50295f78252fb4289608de328d11683d258383cf8121bcdd1f90861f`  
		Last Modified: Fri, 06 Mar 2026 18:19:24 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f9e3292979f8379b1996be583504c5d74d1ed6ba66ed3ca5a118895c1c8c01fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b33d5972c27b9d8d24ad3ffbca659262785fb0ad2182daafdbaf9b24655fe4eb`

```dockerfile
```

-	Layers:
	-	`sha256:1b2f58f0c29777bd0357a391cc09801c7129374079468f633a030a2850a45f7e`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 25.4 KB (25418 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1.4-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:dfb15848187627df8c5cbde28c2bf9708b8eb80028c34d4a7d3d9e9955476261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228246926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c782508554b248a41a6d2fbb3dde7d64bde8ee120e8309d59368bfc163edf3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:25 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:25 GMT
ARG VERSION=26.1.4.35
# Tue, 17 Mar 2026 01:15:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:15:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:15:59 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:15:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:15:59 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:15:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:15:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6584dfb8e761d2835ed68cdc836e2caedfdd354cb02cce2a2beb546c773cd3ce`  
		Last Modified: Tue, 17 Mar 2026 01:16:19 GMT  
		Size: 7.6 MB (7577385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7debbd2fc19a0083e840610be32e23f2b10ead488e5a70937f2ba838cd90c961`  
		Last Modified: Tue, 17 Mar 2026 01:16:23 GMT  
		Size: 192.4 MB (192410468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7510a8afb0f61af1a5515d7e63c866a19877474052fefebdcdbcd4f77dd55f38`  
		Last Modified: Tue, 17 Mar 2026 01:16:19 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e75ec6f7eb02a26d013dd2847b9331ec80273f3e51783cc88e16b5347fb588c`  
		Last Modified: Tue, 17 Mar 2026 01:16:19 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad770cf2515a681a5c431f760d32a45233948add498a917de393218707359004`  
		Last Modified: Tue, 17 Mar 2026 01:16:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fff4834048bf7c50f0a8494a01fda8d6ed8be6d3b2460ca210751dfce6d2b8b`  
		Last Modified: Tue, 17 Mar 2026 01:16:20 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcef26757561469ac2de381b099e8827f9a0a91257c6de403ffce19fba43d49`  
		Last Modified: Tue, 17 Mar 2026 01:16:21 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:30040edcfe86febe2b72ff22affbb093cca9b1df31fe6bed4e203a1110f7204e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd5ced716c0c43d6d3bee423fffbfa224ef2eea5fc59669300f81f7a10ba5355`

```dockerfile
```

-	Layers:
	-	`sha256:5b85ed9433df0c1edceeb1fc5b52fa675833b4971b9bbf2f166dd6be63d5b3b4`  
		Last Modified: Tue, 17 Mar 2026 01:16:19 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1.4.35`

```console
$ docker pull clickhouse@sha256:e963c19fff30164a740c669a92af1bb7000b75f312762ffc626e53bfbf1ce3c9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1.4.35` - linux; amd64

```console
$ docker pull clickhouse@sha256:7a5fb226f81ff050cd0e717e4b0fe12270742e616905d2243ed419f7aa6d8e81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (246001744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccae8563d00171c05b6b46aac39d24bcb38e9c08f28eb1ae90291e4ecc1f3fff`
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
# Fri, 06 Mar 2026 18:18:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:33 GMT
ARG VERSION=26.1.4.35
# Fri, 06 Mar 2026 18:18:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:18:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:18:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:19:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:19:00 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:19:00 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:19:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:19:01 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:19:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:19:01 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:19:01 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:19:01 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:19:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf1cd52a322630e05ff2887999d6093183d6952c5afbc0c1f04cadda3151a63`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 7.6 MB (7598399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fef26d9d2fca551739567e01ef730c91fa91edf0c8ef1f2ed9f72735dfc7bea`  
		Last Modified: Fri, 06 Mar 2026 18:19:27 GMT  
		Size: 208.0 MB (207995930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011531cdbf3f055c3088541a8b344b155ce558ecc075259c1ce7c4df54a7cbc2`  
		Last Modified: Fri, 06 Mar 2026 18:19:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da1132809fcc99ea72c0b0cb364d991bcc4585804ff5607f8a625ed10cd5860`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5674fe75400fe75f63fc10b32e1a627b74d84c50f4db3e339f6c8ad23a2126`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29e0614378578fd665364c6a2e71e0952c32566c8ebc2f2a23093666f41d160`  
		Last Modified: Fri, 06 Mar 2026 18:19:24 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f114ba2f50295f78252fb4289608de328d11683d258383cf8121bcdd1f90861f`  
		Last Modified: Fri, 06 Mar 2026 18:19:24 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.4.35` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f9e3292979f8379b1996be583504c5d74d1ed6ba66ed3ca5a118895c1c8c01fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b33d5972c27b9d8d24ad3ffbca659262785fb0ad2182daafdbaf9b24655fe4eb`

```dockerfile
```

-	Layers:
	-	`sha256:1b2f58f0c29777bd0357a391cc09801c7129374079468f633a030a2850a45f7e`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 25.4 KB (25418 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1.4.35` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:dfb15848187627df8c5cbde28c2bf9708b8eb80028c34d4a7d3d9e9955476261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228246926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c782508554b248a41a6d2fbb3dde7d64bde8ee120e8309d59368bfc163edf3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:25 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:25 GMT
ARG VERSION=26.1.4.35
# Tue, 17 Mar 2026 01:15:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:15:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:15:59 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:15:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:15:59 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:15:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:15:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6584dfb8e761d2835ed68cdc836e2caedfdd354cb02cce2a2beb546c773cd3ce`  
		Last Modified: Tue, 17 Mar 2026 01:16:19 GMT  
		Size: 7.6 MB (7577385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7debbd2fc19a0083e840610be32e23f2b10ead488e5a70937f2ba838cd90c961`  
		Last Modified: Tue, 17 Mar 2026 01:16:23 GMT  
		Size: 192.4 MB (192410468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7510a8afb0f61af1a5515d7e63c866a19877474052fefebdcdbcd4f77dd55f38`  
		Last Modified: Tue, 17 Mar 2026 01:16:19 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e75ec6f7eb02a26d013dd2847b9331ec80273f3e51783cc88e16b5347fb588c`  
		Last Modified: Tue, 17 Mar 2026 01:16:19 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad770cf2515a681a5c431f760d32a45233948add498a917de393218707359004`  
		Last Modified: Tue, 17 Mar 2026 01:16:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fff4834048bf7c50f0a8494a01fda8d6ed8be6d3b2460ca210751dfce6d2b8b`  
		Last Modified: Tue, 17 Mar 2026 01:16:20 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcef26757561469ac2de381b099e8827f9a0a91257c6de403ffce19fba43d49`  
		Last Modified: Tue, 17 Mar 2026 01:16:21 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.4.35` - unknown; unknown

```console
$ docker pull clickhouse@sha256:30040edcfe86febe2b72ff22affbb093cca9b1df31fe6bed4e203a1110f7204e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd5ced716c0c43d6d3bee423fffbfa224ef2eea5fc59669300f81f7a10ba5355`

```dockerfile
```

-	Layers:
	-	`sha256:5b85ed9433df0c1edceeb1fc5b52fa675833b4971b9bbf2f166dd6be63d5b3b4`  
		Last Modified: Tue, 17 Mar 2026 01:16:19 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1.4.35-jammy`

```console
$ docker pull clickhouse@sha256:e963c19fff30164a740c669a92af1bb7000b75f312762ffc626e53bfbf1ce3c9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1.4.35-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:7a5fb226f81ff050cd0e717e4b0fe12270742e616905d2243ed419f7aa6d8e81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (246001744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccae8563d00171c05b6b46aac39d24bcb38e9c08f28eb1ae90291e4ecc1f3fff`
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
# Fri, 06 Mar 2026 18:18:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:33 GMT
ARG VERSION=26.1.4.35
# Fri, 06 Mar 2026 18:18:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:18:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:18:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:19:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:19:00 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:19:00 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:19:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:19:01 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:19:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:19:01 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:19:01 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:19:01 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:19:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf1cd52a322630e05ff2887999d6093183d6952c5afbc0c1f04cadda3151a63`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 7.6 MB (7598399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fef26d9d2fca551739567e01ef730c91fa91edf0c8ef1f2ed9f72735dfc7bea`  
		Last Modified: Fri, 06 Mar 2026 18:19:27 GMT  
		Size: 208.0 MB (207995930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011531cdbf3f055c3088541a8b344b155ce558ecc075259c1ce7c4df54a7cbc2`  
		Last Modified: Fri, 06 Mar 2026 18:19:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da1132809fcc99ea72c0b0cb364d991bcc4585804ff5607f8a625ed10cd5860`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5674fe75400fe75f63fc10b32e1a627b74d84c50f4db3e339f6c8ad23a2126`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29e0614378578fd665364c6a2e71e0952c32566c8ebc2f2a23093666f41d160`  
		Last Modified: Fri, 06 Mar 2026 18:19:24 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f114ba2f50295f78252fb4289608de328d11683d258383cf8121bcdd1f90861f`  
		Last Modified: Fri, 06 Mar 2026 18:19:24 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.4.35-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f9e3292979f8379b1996be583504c5d74d1ed6ba66ed3ca5a118895c1c8c01fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b33d5972c27b9d8d24ad3ffbca659262785fb0ad2182daafdbaf9b24655fe4eb`

```dockerfile
```

-	Layers:
	-	`sha256:1b2f58f0c29777bd0357a391cc09801c7129374079468f633a030a2850a45f7e`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 25.4 KB (25418 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1.4.35-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:dfb15848187627df8c5cbde28c2bf9708b8eb80028c34d4a7d3d9e9955476261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228246926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c782508554b248a41a6d2fbb3dde7d64bde8ee120e8309d59368bfc163edf3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:25 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:25 GMT
ARG VERSION=26.1.4.35
# Tue, 17 Mar 2026 01:15:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:15:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:15:59 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:15:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.4.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:15:59 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:15:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:15:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6584dfb8e761d2835ed68cdc836e2caedfdd354cb02cce2a2beb546c773cd3ce`  
		Last Modified: Tue, 17 Mar 2026 01:16:19 GMT  
		Size: 7.6 MB (7577385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7debbd2fc19a0083e840610be32e23f2b10ead488e5a70937f2ba838cd90c961`  
		Last Modified: Tue, 17 Mar 2026 01:16:23 GMT  
		Size: 192.4 MB (192410468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7510a8afb0f61af1a5515d7e63c866a19877474052fefebdcdbcd4f77dd55f38`  
		Last Modified: Tue, 17 Mar 2026 01:16:19 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e75ec6f7eb02a26d013dd2847b9331ec80273f3e51783cc88e16b5347fb588c`  
		Last Modified: Tue, 17 Mar 2026 01:16:19 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad770cf2515a681a5c431f760d32a45233948add498a917de393218707359004`  
		Last Modified: Tue, 17 Mar 2026 01:16:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fff4834048bf7c50f0a8494a01fda8d6ed8be6d3b2460ca210751dfce6d2b8b`  
		Last Modified: Tue, 17 Mar 2026 01:16:20 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcef26757561469ac2de381b099e8827f9a0a91257c6de403ffce19fba43d49`  
		Last Modified: Tue, 17 Mar 2026 01:16:21 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.4.35-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:30040edcfe86febe2b72ff22affbb093cca9b1df31fe6bed4e203a1110f7204e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd5ced716c0c43d6d3bee423fffbfa224ef2eea5fc59669300f81f7a10ba5355`

```dockerfile
```

-	Layers:
	-	`sha256:5b85ed9433df0c1edceeb1fc5b52fa675833b4971b9bbf2f166dd6be63d5b3b4`  
		Last Modified: Tue, 17 Mar 2026 01:16:19 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2`

```console
$ docker pull clickhouse@sha256:5f8d57082e288c5e3fd541de7ac611f5ab4420fc61f014bb83a936f03e23b99f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2` - linux; amd64

```console
$ docker pull clickhouse@sha256:8bb7216daa1b1e60a43f1d026a51fe7db0c0af3e89ed13708e1da55a2c7fbda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.6 MB (253565469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11cf87e6eeb307bfcd986fdc250c2d0d3a111d19a93823e872a68e4f78ed4ab1`
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
# Fri, 06 Mar 2026 18:18:09 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:09 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:09 GMT
ARG VERSION=26.2.4.23
# Fri, 06 Mar 2026 18:18:09 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:18:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:18:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:18:38 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:18:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:18:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:18:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:18:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22eaf4113aeb35a06fd46548b455b9b73b22b6d4d683b65ed58a5cbbeb012e3e`  
		Last Modified: Fri, 06 Mar 2026 18:19:04 GMT  
		Size: 7.6 MB (7598345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d5e0a067d5092ab00d8523814b7a1177d9a19cc4ffdad496b9af464eafddd4`  
		Last Modified: Fri, 06 Mar 2026 18:19:08 GMT  
		Size: 215.6 MB (215559707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6181f8036f56b33269a32e5f31ca4f53cc6b79c61c49d64c0bd6cee2c2657835`  
		Last Modified: Fri, 06 Mar 2026 18:19:03 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3bb9a19dfb24c1d97efb9ab4526da77b22e4063ee862113871cfd7d02167193`  
		Last Modified: Fri, 06 Mar 2026 18:19:04 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98deebd5cfcd03fe40014d9bb9131fb4dff19698aacd22879fa18ca72acd2c68`  
		Last Modified: Fri, 06 Mar 2026 18:19:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652bc65f3110d56d313c28ceab6c30c81b11a7fe01abf8afedde793ca05fd327`  
		Last Modified: Fri, 06 Mar 2026 18:19:05 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf83d8b9d8887336121e3163af3d3bb1b137d9a8c30647843dbed5ad939970a0`  
		Last Modified: Fri, 06 Mar 2026 18:19:05 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:159a51c6df9cfe13192db6a453e6766b15cdd35c8537c2664e5f2bf4c56cc2a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4c93a1bc7c8559efe5282cfc66f7980e39eb7d946fb13a67591086228181c9`

```dockerfile
```

-	Layers:
	-	`sha256:f2effedc5d26987e9737e26f67009bff95effe72a9af0dabae2617850e6c0d11`  
		Last Modified: Fri, 06 Mar 2026 18:19:03 GMT  
		Size: 26.0 KB (26027 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:6d0c52bd6b57c9fd047315f093b81d285026b8c7242f64970c73308bb5b798de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237156340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:153abe2b156d323d7d30e5b705cad5cb7fe92839f5eb7c00575a586df7a0dd65`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:25 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:25 GMT
ARG VERSION=26.2.4.23
# Tue, 17 Mar 2026 01:15:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:15:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:15:58 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:15:58 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:15:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:15:59 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:15:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:15:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a317af7a5f124f732179e605341776219201524bb83c2f8fdfb4b8202d81323`  
		Last Modified: Tue, 17 Mar 2026 01:16:21 GMT  
		Size: 7.6 MB (7577366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140bde1e18277c0b794fe7439e37d4eecfdb491f050f5a3cf20988748546533a`  
		Last Modified: Tue, 17 Mar 2026 01:16:24 GMT  
		Size: 201.3 MB (201319899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b59afba237f3cc12ef717f5997f167c4e97a644a89067c3aee1ae79c630bb6`  
		Last Modified: Tue, 17 Mar 2026 01:16:20 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a11aa3d7ce29a9729165c1fb0d50b7d4af4ef42d2e6d5c57e95923b6aef962`  
		Last Modified: Tue, 17 Mar 2026 01:16:21 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477c7a02a0dd0bbc4c7ef240b36b92d5c4972f240821458e5c718f56a6b22d7f`  
		Last Modified: Tue, 17 Mar 2026 01:16:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72fe6e453a9256df711de6e06c0dd7afc2a0c6e2956aa903677edb3c64f4e591`  
		Last Modified: Tue, 17 Mar 2026 01:16:22 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcef26757561469ac2de381b099e8827f9a0a91257c6de403ffce19fba43d49`  
		Last Modified: Tue, 17 Mar 2026 01:16:21 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:248eae08d3dd2d5cacf083729b5b66e360375eb1a82c7657d03e0451da5bc940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55443238ddeb66f4a95ee470f66f47930afb5cd05a961f94b39ba2aae946eb7d`

```dockerfile
```

-	Layers:
	-	`sha256:2ee2edc47ecd9600978cc00bd3ab1b85f3a41fb8a1832fde9ced084cf8257d7f`  
		Last Modified: Tue, 17 Mar 2026 01:16:20 GMT  
		Size: 26.2 KB (26237 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2-jammy`

```console
$ docker pull clickhouse@sha256:5f8d57082e288c5e3fd541de7ac611f5ab4420fc61f014bb83a936f03e23b99f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:8bb7216daa1b1e60a43f1d026a51fe7db0c0af3e89ed13708e1da55a2c7fbda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.6 MB (253565469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11cf87e6eeb307bfcd986fdc250c2d0d3a111d19a93823e872a68e4f78ed4ab1`
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
# Fri, 06 Mar 2026 18:18:09 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:09 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:09 GMT
ARG VERSION=26.2.4.23
# Fri, 06 Mar 2026 18:18:09 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:18:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:18:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:18:38 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:18:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:18:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:18:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:18:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22eaf4113aeb35a06fd46548b455b9b73b22b6d4d683b65ed58a5cbbeb012e3e`  
		Last Modified: Fri, 06 Mar 2026 18:19:04 GMT  
		Size: 7.6 MB (7598345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d5e0a067d5092ab00d8523814b7a1177d9a19cc4ffdad496b9af464eafddd4`  
		Last Modified: Fri, 06 Mar 2026 18:19:08 GMT  
		Size: 215.6 MB (215559707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6181f8036f56b33269a32e5f31ca4f53cc6b79c61c49d64c0bd6cee2c2657835`  
		Last Modified: Fri, 06 Mar 2026 18:19:03 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3bb9a19dfb24c1d97efb9ab4526da77b22e4063ee862113871cfd7d02167193`  
		Last Modified: Fri, 06 Mar 2026 18:19:04 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98deebd5cfcd03fe40014d9bb9131fb4dff19698aacd22879fa18ca72acd2c68`  
		Last Modified: Fri, 06 Mar 2026 18:19:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652bc65f3110d56d313c28ceab6c30c81b11a7fe01abf8afedde793ca05fd327`  
		Last Modified: Fri, 06 Mar 2026 18:19:05 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf83d8b9d8887336121e3163af3d3bb1b137d9a8c30647843dbed5ad939970a0`  
		Last Modified: Fri, 06 Mar 2026 18:19:05 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:159a51c6df9cfe13192db6a453e6766b15cdd35c8537c2664e5f2bf4c56cc2a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4c93a1bc7c8559efe5282cfc66f7980e39eb7d946fb13a67591086228181c9`

```dockerfile
```

-	Layers:
	-	`sha256:f2effedc5d26987e9737e26f67009bff95effe72a9af0dabae2617850e6c0d11`  
		Last Modified: Fri, 06 Mar 2026 18:19:03 GMT  
		Size: 26.0 KB (26027 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:6d0c52bd6b57c9fd047315f093b81d285026b8c7242f64970c73308bb5b798de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237156340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:153abe2b156d323d7d30e5b705cad5cb7fe92839f5eb7c00575a586df7a0dd65`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:25 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:25 GMT
ARG VERSION=26.2.4.23
# Tue, 17 Mar 2026 01:15:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:15:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:15:58 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:15:58 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:15:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:15:59 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:15:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:15:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a317af7a5f124f732179e605341776219201524bb83c2f8fdfb4b8202d81323`  
		Last Modified: Tue, 17 Mar 2026 01:16:21 GMT  
		Size: 7.6 MB (7577366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140bde1e18277c0b794fe7439e37d4eecfdb491f050f5a3cf20988748546533a`  
		Last Modified: Tue, 17 Mar 2026 01:16:24 GMT  
		Size: 201.3 MB (201319899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b59afba237f3cc12ef717f5997f167c4e97a644a89067c3aee1ae79c630bb6`  
		Last Modified: Tue, 17 Mar 2026 01:16:20 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a11aa3d7ce29a9729165c1fb0d50b7d4af4ef42d2e6d5c57e95923b6aef962`  
		Last Modified: Tue, 17 Mar 2026 01:16:21 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477c7a02a0dd0bbc4c7ef240b36b92d5c4972f240821458e5c718f56a6b22d7f`  
		Last Modified: Tue, 17 Mar 2026 01:16:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72fe6e453a9256df711de6e06c0dd7afc2a0c6e2956aa903677edb3c64f4e591`  
		Last Modified: Tue, 17 Mar 2026 01:16:22 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcef26757561469ac2de381b099e8827f9a0a91257c6de403ffce19fba43d49`  
		Last Modified: Tue, 17 Mar 2026 01:16:21 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:248eae08d3dd2d5cacf083729b5b66e360375eb1a82c7657d03e0451da5bc940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55443238ddeb66f4a95ee470f66f47930afb5cd05a961f94b39ba2aae946eb7d`

```dockerfile
```

-	Layers:
	-	`sha256:2ee2edc47ecd9600978cc00bd3ab1b85f3a41fb8a1832fde9ced084cf8257d7f`  
		Last Modified: Tue, 17 Mar 2026 01:16:20 GMT  
		Size: 26.2 KB (26237 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2.4`

```console
$ docker pull clickhouse@sha256:5f8d57082e288c5e3fd541de7ac611f5ab4420fc61f014bb83a936f03e23b99f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2.4` - linux; amd64

```console
$ docker pull clickhouse@sha256:8bb7216daa1b1e60a43f1d026a51fe7db0c0af3e89ed13708e1da55a2c7fbda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.6 MB (253565469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11cf87e6eeb307bfcd986fdc250c2d0d3a111d19a93823e872a68e4f78ed4ab1`
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
# Fri, 06 Mar 2026 18:18:09 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:09 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:09 GMT
ARG VERSION=26.2.4.23
# Fri, 06 Mar 2026 18:18:09 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:18:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:18:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:18:38 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:18:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:18:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:18:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:18:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22eaf4113aeb35a06fd46548b455b9b73b22b6d4d683b65ed58a5cbbeb012e3e`  
		Last Modified: Fri, 06 Mar 2026 18:19:04 GMT  
		Size: 7.6 MB (7598345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d5e0a067d5092ab00d8523814b7a1177d9a19cc4ffdad496b9af464eafddd4`  
		Last Modified: Fri, 06 Mar 2026 18:19:08 GMT  
		Size: 215.6 MB (215559707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6181f8036f56b33269a32e5f31ca4f53cc6b79c61c49d64c0bd6cee2c2657835`  
		Last Modified: Fri, 06 Mar 2026 18:19:03 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3bb9a19dfb24c1d97efb9ab4526da77b22e4063ee862113871cfd7d02167193`  
		Last Modified: Fri, 06 Mar 2026 18:19:04 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98deebd5cfcd03fe40014d9bb9131fb4dff19698aacd22879fa18ca72acd2c68`  
		Last Modified: Fri, 06 Mar 2026 18:19:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652bc65f3110d56d313c28ceab6c30c81b11a7fe01abf8afedde793ca05fd327`  
		Last Modified: Fri, 06 Mar 2026 18:19:05 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf83d8b9d8887336121e3163af3d3bb1b137d9a8c30647843dbed5ad939970a0`  
		Last Modified: Fri, 06 Mar 2026 18:19:05 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:159a51c6df9cfe13192db6a453e6766b15cdd35c8537c2664e5f2bf4c56cc2a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4c93a1bc7c8559efe5282cfc66f7980e39eb7d946fb13a67591086228181c9`

```dockerfile
```

-	Layers:
	-	`sha256:f2effedc5d26987e9737e26f67009bff95effe72a9af0dabae2617850e6c0d11`  
		Last Modified: Fri, 06 Mar 2026 18:19:03 GMT  
		Size: 26.0 KB (26027 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2.4` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:6d0c52bd6b57c9fd047315f093b81d285026b8c7242f64970c73308bb5b798de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237156340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:153abe2b156d323d7d30e5b705cad5cb7fe92839f5eb7c00575a586df7a0dd65`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:25 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:25 GMT
ARG VERSION=26.2.4.23
# Tue, 17 Mar 2026 01:15:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:15:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:15:58 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:15:58 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:15:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:15:59 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:15:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:15:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a317af7a5f124f732179e605341776219201524bb83c2f8fdfb4b8202d81323`  
		Last Modified: Tue, 17 Mar 2026 01:16:21 GMT  
		Size: 7.6 MB (7577366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140bde1e18277c0b794fe7439e37d4eecfdb491f050f5a3cf20988748546533a`  
		Last Modified: Tue, 17 Mar 2026 01:16:24 GMT  
		Size: 201.3 MB (201319899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b59afba237f3cc12ef717f5997f167c4e97a644a89067c3aee1ae79c630bb6`  
		Last Modified: Tue, 17 Mar 2026 01:16:20 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a11aa3d7ce29a9729165c1fb0d50b7d4af4ef42d2e6d5c57e95923b6aef962`  
		Last Modified: Tue, 17 Mar 2026 01:16:21 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477c7a02a0dd0bbc4c7ef240b36b92d5c4972f240821458e5c718f56a6b22d7f`  
		Last Modified: Tue, 17 Mar 2026 01:16:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72fe6e453a9256df711de6e06c0dd7afc2a0c6e2956aa903677edb3c64f4e591`  
		Last Modified: Tue, 17 Mar 2026 01:16:22 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcef26757561469ac2de381b099e8827f9a0a91257c6de403ffce19fba43d49`  
		Last Modified: Tue, 17 Mar 2026 01:16:21 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:248eae08d3dd2d5cacf083729b5b66e360375eb1a82c7657d03e0451da5bc940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55443238ddeb66f4a95ee470f66f47930afb5cd05a961f94b39ba2aae946eb7d`

```dockerfile
```

-	Layers:
	-	`sha256:2ee2edc47ecd9600978cc00bd3ab1b85f3a41fb8a1832fde9ced084cf8257d7f`  
		Last Modified: Tue, 17 Mar 2026 01:16:20 GMT  
		Size: 26.2 KB (26237 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2.4-jammy`

```console
$ docker pull clickhouse@sha256:5f8d57082e288c5e3fd541de7ac611f5ab4420fc61f014bb83a936f03e23b99f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2.4-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:8bb7216daa1b1e60a43f1d026a51fe7db0c0af3e89ed13708e1da55a2c7fbda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.6 MB (253565469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11cf87e6eeb307bfcd986fdc250c2d0d3a111d19a93823e872a68e4f78ed4ab1`
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
# Fri, 06 Mar 2026 18:18:09 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:09 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:09 GMT
ARG VERSION=26.2.4.23
# Fri, 06 Mar 2026 18:18:09 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:18:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:18:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:18:38 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:18:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:18:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:18:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:18:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22eaf4113aeb35a06fd46548b455b9b73b22b6d4d683b65ed58a5cbbeb012e3e`  
		Last Modified: Fri, 06 Mar 2026 18:19:04 GMT  
		Size: 7.6 MB (7598345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d5e0a067d5092ab00d8523814b7a1177d9a19cc4ffdad496b9af464eafddd4`  
		Last Modified: Fri, 06 Mar 2026 18:19:08 GMT  
		Size: 215.6 MB (215559707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6181f8036f56b33269a32e5f31ca4f53cc6b79c61c49d64c0bd6cee2c2657835`  
		Last Modified: Fri, 06 Mar 2026 18:19:03 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3bb9a19dfb24c1d97efb9ab4526da77b22e4063ee862113871cfd7d02167193`  
		Last Modified: Fri, 06 Mar 2026 18:19:04 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98deebd5cfcd03fe40014d9bb9131fb4dff19698aacd22879fa18ca72acd2c68`  
		Last Modified: Fri, 06 Mar 2026 18:19:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652bc65f3110d56d313c28ceab6c30c81b11a7fe01abf8afedde793ca05fd327`  
		Last Modified: Fri, 06 Mar 2026 18:19:05 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf83d8b9d8887336121e3163af3d3bb1b137d9a8c30647843dbed5ad939970a0`  
		Last Modified: Fri, 06 Mar 2026 18:19:05 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:159a51c6df9cfe13192db6a453e6766b15cdd35c8537c2664e5f2bf4c56cc2a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4c93a1bc7c8559efe5282cfc66f7980e39eb7d946fb13a67591086228181c9`

```dockerfile
```

-	Layers:
	-	`sha256:f2effedc5d26987e9737e26f67009bff95effe72a9af0dabae2617850e6c0d11`  
		Last Modified: Fri, 06 Mar 2026 18:19:03 GMT  
		Size: 26.0 KB (26027 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2.4-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:6d0c52bd6b57c9fd047315f093b81d285026b8c7242f64970c73308bb5b798de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237156340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:153abe2b156d323d7d30e5b705cad5cb7fe92839f5eb7c00575a586df7a0dd65`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:25 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:25 GMT
ARG VERSION=26.2.4.23
# Tue, 17 Mar 2026 01:15:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:15:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:15:58 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:15:58 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:15:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:15:59 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:15:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:15:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a317af7a5f124f732179e605341776219201524bb83c2f8fdfb4b8202d81323`  
		Last Modified: Tue, 17 Mar 2026 01:16:21 GMT  
		Size: 7.6 MB (7577366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140bde1e18277c0b794fe7439e37d4eecfdb491f050f5a3cf20988748546533a`  
		Last Modified: Tue, 17 Mar 2026 01:16:24 GMT  
		Size: 201.3 MB (201319899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b59afba237f3cc12ef717f5997f167c4e97a644a89067c3aee1ae79c630bb6`  
		Last Modified: Tue, 17 Mar 2026 01:16:20 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a11aa3d7ce29a9729165c1fb0d50b7d4af4ef42d2e6d5c57e95923b6aef962`  
		Last Modified: Tue, 17 Mar 2026 01:16:21 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477c7a02a0dd0bbc4c7ef240b36b92d5c4972f240821458e5c718f56a6b22d7f`  
		Last Modified: Tue, 17 Mar 2026 01:16:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72fe6e453a9256df711de6e06c0dd7afc2a0c6e2956aa903677edb3c64f4e591`  
		Last Modified: Tue, 17 Mar 2026 01:16:22 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcef26757561469ac2de381b099e8827f9a0a91257c6de403ffce19fba43d49`  
		Last Modified: Tue, 17 Mar 2026 01:16:21 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:248eae08d3dd2d5cacf083729b5b66e360375eb1a82c7657d03e0451da5bc940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55443238ddeb66f4a95ee470f66f47930afb5cd05a961f94b39ba2aae946eb7d`

```dockerfile
```

-	Layers:
	-	`sha256:2ee2edc47ecd9600978cc00bd3ab1b85f3a41fb8a1832fde9ced084cf8257d7f`  
		Last Modified: Tue, 17 Mar 2026 01:16:20 GMT  
		Size: 26.2 KB (26237 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2.4.23`

```console
$ docker pull clickhouse@sha256:5f8d57082e288c5e3fd541de7ac611f5ab4420fc61f014bb83a936f03e23b99f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2.4.23` - linux; amd64

```console
$ docker pull clickhouse@sha256:8bb7216daa1b1e60a43f1d026a51fe7db0c0af3e89ed13708e1da55a2c7fbda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.6 MB (253565469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11cf87e6eeb307bfcd986fdc250c2d0d3a111d19a93823e872a68e4f78ed4ab1`
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
# Fri, 06 Mar 2026 18:18:09 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:09 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:09 GMT
ARG VERSION=26.2.4.23
# Fri, 06 Mar 2026 18:18:09 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:18:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:18:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:18:38 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:18:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:18:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:18:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:18:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22eaf4113aeb35a06fd46548b455b9b73b22b6d4d683b65ed58a5cbbeb012e3e`  
		Last Modified: Fri, 06 Mar 2026 18:19:04 GMT  
		Size: 7.6 MB (7598345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d5e0a067d5092ab00d8523814b7a1177d9a19cc4ffdad496b9af464eafddd4`  
		Last Modified: Fri, 06 Mar 2026 18:19:08 GMT  
		Size: 215.6 MB (215559707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6181f8036f56b33269a32e5f31ca4f53cc6b79c61c49d64c0bd6cee2c2657835`  
		Last Modified: Fri, 06 Mar 2026 18:19:03 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3bb9a19dfb24c1d97efb9ab4526da77b22e4063ee862113871cfd7d02167193`  
		Last Modified: Fri, 06 Mar 2026 18:19:04 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98deebd5cfcd03fe40014d9bb9131fb4dff19698aacd22879fa18ca72acd2c68`  
		Last Modified: Fri, 06 Mar 2026 18:19:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652bc65f3110d56d313c28ceab6c30c81b11a7fe01abf8afedde793ca05fd327`  
		Last Modified: Fri, 06 Mar 2026 18:19:05 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf83d8b9d8887336121e3163af3d3bb1b137d9a8c30647843dbed5ad939970a0`  
		Last Modified: Fri, 06 Mar 2026 18:19:05 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.4.23` - unknown; unknown

```console
$ docker pull clickhouse@sha256:159a51c6df9cfe13192db6a453e6766b15cdd35c8537c2664e5f2bf4c56cc2a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4c93a1bc7c8559efe5282cfc66f7980e39eb7d946fb13a67591086228181c9`

```dockerfile
```

-	Layers:
	-	`sha256:f2effedc5d26987e9737e26f67009bff95effe72a9af0dabae2617850e6c0d11`  
		Last Modified: Fri, 06 Mar 2026 18:19:03 GMT  
		Size: 26.0 KB (26027 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2.4.23` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:6d0c52bd6b57c9fd047315f093b81d285026b8c7242f64970c73308bb5b798de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237156340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:153abe2b156d323d7d30e5b705cad5cb7fe92839f5eb7c00575a586df7a0dd65`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:25 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:25 GMT
ARG VERSION=26.2.4.23
# Tue, 17 Mar 2026 01:15:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:15:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:15:58 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:15:58 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:15:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:15:59 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:15:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:15:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a317af7a5f124f732179e605341776219201524bb83c2f8fdfb4b8202d81323`  
		Last Modified: Tue, 17 Mar 2026 01:16:21 GMT  
		Size: 7.6 MB (7577366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140bde1e18277c0b794fe7439e37d4eecfdb491f050f5a3cf20988748546533a`  
		Last Modified: Tue, 17 Mar 2026 01:16:24 GMT  
		Size: 201.3 MB (201319899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b59afba237f3cc12ef717f5997f167c4e97a644a89067c3aee1ae79c630bb6`  
		Last Modified: Tue, 17 Mar 2026 01:16:20 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a11aa3d7ce29a9729165c1fb0d50b7d4af4ef42d2e6d5c57e95923b6aef962`  
		Last Modified: Tue, 17 Mar 2026 01:16:21 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477c7a02a0dd0bbc4c7ef240b36b92d5c4972f240821458e5c718f56a6b22d7f`  
		Last Modified: Tue, 17 Mar 2026 01:16:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72fe6e453a9256df711de6e06c0dd7afc2a0c6e2956aa903677edb3c64f4e591`  
		Last Modified: Tue, 17 Mar 2026 01:16:22 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcef26757561469ac2de381b099e8827f9a0a91257c6de403ffce19fba43d49`  
		Last Modified: Tue, 17 Mar 2026 01:16:21 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.4.23` - unknown; unknown

```console
$ docker pull clickhouse@sha256:248eae08d3dd2d5cacf083729b5b66e360375eb1a82c7657d03e0451da5bc940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55443238ddeb66f4a95ee470f66f47930afb5cd05a961f94b39ba2aae946eb7d`

```dockerfile
```

-	Layers:
	-	`sha256:2ee2edc47ecd9600978cc00bd3ab1b85f3a41fb8a1832fde9ced084cf8257d7f`  
		Last Modified: Tue, 17 Mar 2026 01:16:20 GMT  
		Size: 26.2 KB (26237 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2.4.23-jammy`

```console
$ docker pull clickhouse@sha256:5f8d57082e288c5e3fd541de7ac611f5ab4420fc61f014bb83a936f03e23b99f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2.4.23-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:8bb7216daa1b1e60a43f1d026a51fe7db0c0af3e89ed13708e1da55a2c7fbda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.6 MB (253565469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11cf87e6eeb307bfcd986fdc250c2d0d3a111d19a93823e872a68e4f78ed4ab1`
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
# Fri, 06 Mar 2026 18:18:09 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:09 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:09 GMT
ARG VERSION=26.2.4.23
# Fri, 06 Mar 2026 18:18:09 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:18:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:18:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:18:38 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:18:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:18:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:18:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:18:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22eaf4113aeb35a06fd46548b455b9b73b22b6d4d683b65ed58a5cbbeb012e3e`  
		Last Modified: Fri, 06 Mar 2026 18:19:04 GMT  
		Size: 7.6 MB (7598345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d5e0a067d5092ab00d8523814b7a1177d9a19cc4ffdad496b9af464eafddd4`  
		Last Modified: Fri, 06 Mar 2026 18:19:08 GMT  
		Size: 215.6 MB (215559707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6181f8036f56b33269a32e5f31ca4f53cc6b79c61c49d64c0bd6cee2c2657835`  
		Last Modified: Fri, 06 Mar 2026 18:19:03 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3bb9a19dfb24c1d97efb9ab4526da77b22e4063ee862113871cfd7d02167193`  
		Last Modified: Fri, 06 Mar 2026 18:19:04 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98deebd5cfcd03fe40014d9bb9131fb4dff19698aacd22879fa18ca72acd2c68`  
		Last Modified: Fri, 06 Mar 2026 18:19:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652bc65f3110d56d313c28ceab6c30c81b11a7fe01abf8afedde793ca05fd327`  
		Last Modified: Fri, 06 Mar 2026 18:19:05 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf83d8b9d8887336121e3163af3d3bb1b137d9a8c30647843dbed5ad939970a0`  
		Last Modified: Fri, 06 Mar 2026 18:19:05 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.4.23-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:159a51c6df9cfe13192db6a453e6766b15cdd35c8537c2664e5f2bf4c56cc2a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4c93a1bc7c8559efe5282cfc66f7980e39eb7d946fb13a67591086228181c9`

```dockerfile
```

-	Layers:
	-	`sha256:f2effedc5d26987e9737e26f67009bff95effe72a9af0dabae2617850e6c0d11`  
		Last Modified: Fri, 06 Mar 2026 18:19:03 GMT  
		Size: 26.0 KB (26027 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2.4.23-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:6d0c52bd6b57c9fd047315f093b81d285026b8c7242f64970c73308bb5b798de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237156340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:153abe2b156d323d7d30e5b705cad5cb7fe92839f5eb7c00575a586df7a0dd65`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:25 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:25 GMT
ARG VERSION=26.2.4.23
# Tue, 17 Mar 2026 01:15:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:15:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:15:58 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:15:58 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:15:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:15:59 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:15:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:15:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a317af7a5f124f732179e605341776219201524bb83c2f8fdfb4b8202d81323`  
		Last Modified: Tue, 17 Mar 2026 01:16:21 GMT  
		Size: 7.6 MB (7577366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140bde1e18277c0b794fe7439e37d4eecfdb491f050f5a3cf20988748546533a`  
		Last Modified: Tue, 17 Mar 2026 01:16:24 GMT  
		Size: 201.3 MB (201319899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b59afba237f3cc12ef717f5997f167c4e97a644a89067c3aee1ae79c630bb6`  
		Last Modified: Tue, 17 Mar 2026 01:16:20 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a11aa3d7ce29a9729165c1fb0d50b7d4af4ef42d2e6d5c57e95923b6aef962`  
		Last Modified: Tue, 17 Mar 2026 01:16:21 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477c7a02a0dd0bbc4c7ef240b36b92d5c4972f240821458e5c718f56a6b22d7f`  
		Last Modified: Tue, 17 Mar 2026 01:16:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72fe6e453a9256df711de6e06c0dd7afc2a0c6e2956aa903677edb3c64f4e591`  
		Last Modified: Tue, 17 Mar 2026 01:16:22 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcef26757561469ac2de381b099e8827f9a0a91257c6de403ffce19fba43d49`  
		Last Modified: Tue, 17 Mar 2026 01:16:21 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.4.23-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:248eae08d3dd2d5cacf083729b5b66e360375eb1a82c7657d03e0451da5bc940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55443238ddeb66f4a95ee470f66f47930afb5cd05a961f94b39ba2aae946eb7d`

```dockerfile
```

-	Layers:
	-	`sha256:2ee2edc47ecd9600978cc00bd3ab1b85f3a41fb8a1832fde9ced084cf8257d7f`  
		Last Modified: Tue, 17 Mar 2026 01:16:20 GMT  
		Size: 26.2 KB (26237 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:jammy`

```console
$ docker pull clickhouse@sha256:5f8d57082e288c5e3fd541de7ac611f5ab4420fc61f014bb83a936f03e23b99f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:8bb7216daa1b1e60a43f1d026a51fe7db0c0af3e89ed13708e1da55a2c7fbda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.6 MB (253565469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11cf87e6eeb307bfcd986fdc250c2d0d3a111d19a93823e872a68e4f78ed4ab1`
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
# Fri, 06 Mar 2026 18:18:09 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:09 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:09 GMT
ARG VERSION=26.2.4.23
# Fri, 06 Mar 2026 18:18:09 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:18:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:18:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:18:38 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:18:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:18:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:18:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:18:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22eaf4113aeb35a06fd46548b455b9b73b22b6d4d683b65ed58a5cbbeb012e3e`  
		Last Modified: Fri, 06 Mar 2026 18:19:04 GMT  
		Size: 7.6 MB (7598345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d5e0a067d5092ab00d8523814b7a1177d9a19cc4ffdad496b9af464eafddd4`  
		Last Modified: Fri, 06 Mar 2026 18:19:08 GMT  
		Size: 215.6 MB (215559707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6181f8036f56b33269a32e5f31ca4f53cc6b79c61c49d64c0bd6cee2c2657835`  
		Last Modified: Fri, 06 Mar 2026 18:19:03 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3bb9a19dfb24c1d97efb9ab4526da77b22e4063ee862113871cfd7d02167193`  
		Last Modified: Fri, 06 Mar 2026 18:19:04 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98deebd5cfcd03fe40014d9bb9131fb4dff19698aacd22879fa18ca72acd2c68`  
		Last Modified: Fri, 06 Mar 2026 18:19:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652bc65f3110d56d313c28ceab6c30c81b11a7fe01abf8afedde793ca05fd327`  
		Last Modified: Fri, 06 Mar 2026 18:19:05 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf83d8b9d8887336121e3163af3d3bb1b137d9a8c30647843dbed5ad939970a0`  
		Last Modified: Fri, 06 Mar 2026 18:19:05 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:159a51c6df9cfe13192db6a453e6766b15cdd35c8537c2664e5f2bf4c56cc2a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4c93a1bc7c8559efe5282cfc66f7980e39eb7d946fb13a67591086228181c9`

```dockerfile
```

-	Layers:
	-	`sha256:f2effedc5d26987e9737e26f67009bff95effe72a9af0dabae2617850e6c0d11`  
		Last Modified: Fri, 06 Mar 2026 18:19:03 GMT  
		Size: 26.0 KB (26027 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:6d0c52bd6b57c9fd047315f093b81d285026b8c7242f64970c73308bb5b798de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237156340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:153abe2b156d323d7d30e5b705cad5cb7fe92839f5eb7c00575a586df7a0dd65`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:25 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:25 GMT
ARG VERSION=26.2.4.23
# Tue, 17 Mar 2026 01:15:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:15:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:15:58 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:15:58 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:15:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:15:59 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:15:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:15:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a317af7a5f124f732179e605341776219201524bb83c2f8fdfb4b8202d81323`  
		Last Modified: Tue, 17 Mar 2026 01:16:21 GMT  
		Size: 7.6 MB (7577366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140bde1e18277c0b794fe7439e37d4eecfdb491f050f5a3cf20988748546533a`  
		Last Modified: Tue, 17 Mar 2026 01:16:24 GMT  
		Size: 201.3 MB (201319899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b59afba237f3cc12ef717f5997f167c4e97a644a89067c3aee1ae79c630bb6`  
		Last Modified: Tue, 17 Mar 2026 01:16:20 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a11aa3d7ce29a9729165c1fb0d50b7d4af4ef42d2e6d5c57e95923b6aef962`  
		Last Modified: Tue, 17 Mar 2026 01:16:21 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477c7a02a0dd0bbc4c7ef240b36b92d5c4972f240821458e5c718f56a6b22d7f`  
		Last Modified: Tue, 17 Mar 2026 01:16:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72fe6e453a9256df711de6e06c0dd7afc2a0c6e2956aa903677edb3c64f4e591`  
		Last Modified: Tue, 17 Mar 2026 01:16:22 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcef26757561469ac2de381b099e8827f9a0a91257c6de403ffce19fba43d49`  
		Last Modified: Tue, 17 Mar 2026 01:16:21 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:248eae08d3dd2d5cacf083729b5b66e360375eb1a82c7657d03e0451da5bc940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55443238ddeb66f4a95ee470f66f47930afb5cd05a961f94b39ba2aae946eb7d`

```dockerfile
```

-	Layers:
	-	`sha256:2ee2edc47ecd9600978cc00bd3ab1b85f3a41fb8a1832fde9ced084cf8257d7f`  
		Last Modified: Tue, 17 Mar 2026 01:16:20 GMT  
		Size: 26.2 KB (26237 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:5f8d57082e288c5e3fd541de7ac611f5ab4420fc61f014bb83a936f03e23b99f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

```console
$ docker pull clickhouse@sha256:8bb7216daa1b1e60a43f1d026a51fe7db0c0af3e89ed13708e1da55a2c7fbda2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.6 MB (253565469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11cf87e6eeb307bfcd986fdc250c2d0d3a111d19a93823e872a68e4f78ed4ab1`
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
# Fri, 06 Mar 2026 18:18:09 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:09 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:09 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:09 GMT
ARG VERSION=26.2.4.23
# Fri, 06 Mar 2026 18:18:09 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:18:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:18:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:18:38 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:18:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:18:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:18:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:18:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:18:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22eaf4113aeb35a06fd46548b455b9b73b22b6d4d683b65ed58a5cbbeb012e3e`  
		Last Modified: Fri, 06 Mar 2026 18:19:04 GMT  
		Size: 7.6 MB (7598345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d5e0a067d5092ab00d8523814b7a1177d9a19cc4ffdad496b9af464eafddd4`  
		Last Modified: Fri, 06 Mar 2026 18:19:08 GMT  
		Size: 215.6 MB (215559707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6181f8036f56b33269a32e5f31ca4f53cc6b79c61c49d64c0bd6cee2c2657835`  
		Last Modified: Fri, 06 Mar 2026 18:19:03 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3bb9a19dfb24c1d97efb9ab4526da77b22e4063ee862113871cfd7d02167193`  
		Last Modified: Fri, 06 Mar 2026 18:19:04 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98deebd5cfcd03fe40014d9bb9131fb4dff19698aacd22879fa18ca72acd2c68`  
		Last Modified: Fri, 06 Mar 2026 18:19:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652bc65f3110d56d313c28ceab6c30c81b11a7fe01abf8afedde793ca05fd327`  
		Last Modified: Fri, 06 Mar 2026 18:19:05 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf83d8b9d8887336121e3163af3d3bb1b137d9a8c30647843dbed5ad939970a0`  
		Last Modified: Fri, 06 Mar 2026 18:19:05 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:159a51c6df9cfe13192db6a453e6766b15cdd35c8537c2664e5f2bf4c56cc2a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df4c93a1bc7c8559efe5282cfc66f7980e39eb7d946fb13a67591086228181c9`

```dockerfile
```

-	Layers:
	-	`sha256:f2effedc5d26987e9737e26f67009bff95effe72a9af0dabae2617850e6c0d11`  
		Last Modified: Fri, 06 Mar 2026 18:19:03 GMT  
		Size: 26.0 KB (26027 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:6d0c52bd6b57c9fd047315f093b81d285026b8c7242f64970c73308bb5b798de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237156340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:153abe2b156d323d7d30e5b705cad5cb7fe92839f5eb7c00575a586df7a0dd65`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:25 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:25 GMT
ARG VERSION=26.2.4.23
# Tue, 17 Mar 2026 01:15:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:15:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:15:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:15:58 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:15:58 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:15:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.4.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:15:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:15:59 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:15:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:15:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a317af7a5f124f732179e605341776219201524bb83c2f8fdfb4b8202d81323`  
		Last Modified: Tue, 17 Mar 2026 01:16:21 GMT  
		Size: 7.6 MB (7577366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140bde1e18277c0b794fe7439e37d4eecfdb491f050f5a3cf20988748546533a`  
		Last Modified: Tue, 17 Mar 2026 01:16:24 GMT  
		Size: 201.3 MB (201319899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b59afba237f3cc12ef717f5997f167c4e97a644a89067c3aee1ae79c630bb6`  
		Last Modified: Tue, 17 Mar 2026 01:16:20 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a11aa3d7ce29a9729165c1fb0d50b7d4af4ef42d2e6d5c57e95923b6aef962`  
		Last Modified: Tue, 17 Mar 2026 01:16:21 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477c7a02a0dd0bbc4c7ef240b36b92d5c4972f240821458e5c718f56a6b22d7f`  
		Last Modified: Tue, 17 Mar 2026 01:16:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72fe6e453a9256df711de6e06c0dd7afc2a0c6e2956aa903677edb3c64f4e591`  
		Last Modified: Tue, 17 Mar 2026 01:16:22 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcef26757561469ac2de381b099e8827f9a0a91257c6de403ffce19fba43d49`  
		Last Modified: Tue, 17 Mar 2026 01:16:21 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:248eae08d3dd2d5cacf083729b5b66e360375eb1a82c7657d03e0451da5bc940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55443238ddeb66f4a95ee470f66f47930afb5cd05a961f94b39ba2aae946eb7d`

```dockerfile
```

-	Layers:
	-	`sha256:2ee2edc47ecd9600978cc00bd3ab1b85f3a41fb8a1832fde9ced084cf8257d7f`  
		Last Modified: Tue, 17 Mar 2026 01:16:20 GMT  
		Size: 26.2 KB (26237 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts`

```console
$ docker pull clickhouse@sha256:3b6b075ed3ed9bc9bd231bc9a97eb37805c4248737f45c3a2d7e803b7892b03f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts` - linux; amd64

```console
$ docker pull clickhouse@sha256:51db9b19b7faacb227be96bb32f8fa41e77e291617771052643682a004aab6d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (228956961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b173876c47035abf1e353aeafae7f806ec2ece30749bcd55dd6fdc95d58970`
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
# Fri, 06 Mar 2026 18:18:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:33 GMT
ARG VERSION=25.8.18.1
# Fri, 06 Mar 2026 18:18:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:20:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:20:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:20:06 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:20:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:20:06 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:20:06 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:20:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf1cd52a322630e05ff2887999d6093183d6952c5afbc0c1f04cadda3151a63`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 7.6 MB (7598399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f15c8a78545882c5b5d20de07c3b2ce913b72c7618e71dc7406f47fd2ec77f3`  
		Last Modified: Fri, 06 Mar 2026 18:20:29 GMT  
		Size: 191.0 MB (190951174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14499c88faf4f3259b248f6ef835d54060e4f6446a9a7a4d77d2aeb560008c57`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4639d26d5fea888c1dc9315370cedc0227c9a9b5da6b9aaafb06bd416b0c0cf4`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e7e125ac0ce703736242bb82a395bb092a6dc1a71fa212843686348c9d6427`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f3b4d918f0a194272c136d63f8ea5c7fc91d732070e4c39ffe7492e4e5e825`  
		Last Modified: Fri, 06 Mar 2026 18:20:26 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4788a9bd7152d1a8751ed266ec4f19f881c953b4c2dd9ca17e719aacf9eea9e`  
		Last Modified: Fri, 06 Mar 2026 18:20:26 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3f871562ee569f41853247e03faa124152cbc02b26ad4af635e9f48869262511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907bce1944962a711dcb7b0a0e2bc3e0ef2209a91fec34bb4ef7528e812caf02`

```dockerfile
```

-	Layers:
	-	`sha256:6023ddd3ff61c0a42e800fb01b931ee54d710e507a9aa8b5fa7ead51695cc85a`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 26.0 KB (26034 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:48af527e13d25cc4eafe38faa62c7c16f4290dffefdb995220f37db57089c285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.9 MB (213852131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64554b1cdecae50f2e1a969f91c4f7d4796ca9828ba02b4698c036b3219a9545`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:40 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:40 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:40 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:40 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:40 GMT
ARG VERSION=25.8.18.1
# Tue, 17 Mar 2026 01:15:40 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:16:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:16:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:16:10 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:16:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:16:10 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:16:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:16:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624738f5fd92e7b367ade3723b173a32feb25a63a3b43c65b9c17f8b2556f391`  
		Last Modified: Tue, 17 Mar 2026 01:16:29 GMT  
		Size: 7.6 MB (7577383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345ce4ca8b8b3838829ae4173c40639b95d650c11e081e0215c83348a8365318`  
		Last Modified: Tue, 17 Mar 2026 01:16:32 GMT  
		Size: 178.0 MB (178015700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7387612f85f8dfa2149b3d338066e137bd01eecd6bc5dcdceda97d7f90678cb`  
		Last Modified: Tue, 17 Mar 2026 01:16:28 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4cec9b7d967bbb3b133fd7e8b8b1975429816982d1d3279a8c7e7aaef10bc9`  
		Last Modified: Tue, 17 Mar 2026 01:16:29 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284037406a24a7bbebec076c913f28e75c5e11ff502ef87ed70e1d14fbad4a00`  
		Last Modified: Tue, 17 Mar 2026 01:16:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad87031f83bb1367e0ba7889fa35749b0c76a4bf1171154bd5baa111f4e2b3d`  
		Last Modified: Tue, 17 Mar 2026 01:16:30 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2ae45d675d5b9b73537a5eadac12c0e86837a05dc14a287ca973e53fbd58b1`  
		Last Modified: Tue, 17 Mar 2026 01:16:30 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:36df80ae326769e4e214e790e6df6b722bef5915201d50061cd44349c482fd17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0d9829330d0bc51c1346d6969d2f634156ad6e6d512a5d0ee26ea1fc7afcfd`

```dockerfile
```

-	Layers:
	-	`sha256:87b465e3d96244b1a0315152911bb75af8d48146c0ecf3e620557b11f4fed01c`  
		Last Modified: Tue, 17 Mar 2026 01:16:28 GMT  
		Size: 26.2 KB (26245 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts-jammy`

```console
$ docker pull clickhouse@sha256:3b6b075ed3ed9bc9bd231bc9a97eb37805c4248737f45c3a2d7e803b7892b03f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:51db9b19b7faacb227be96bb32f8fa41e77e291617771052643682a004aab6d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (228956961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b173876c47035abf1e353aeafae7f806ec2ece30749bcd55dd6fdc95d58970`
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
# Fri, 06 Mar 2026 18:18:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 06 Mar 2026 18:18:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 06 Mar 2026 18:18:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPO_CHANNEL=stable
# Fri, 06 Mar 2026 18:18:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 06 Mar 2026 18:18:33 GMT
ARG VERSION=25.8.18.1
# Fri, 06 Mar 2026 18:18:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 06 Mar 2026 18:20:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:20:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
ENV LANG=en_US.UTF-8
# Fri, 06 Mar 2026 18:20:06 GMT
ENV TZ=UTC
# Fri, 06 Mar 2026 18:20:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 06 Mar 2026 18:20:06 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 06 Mar 2026 18:20:06 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 06 Mar 2026 18:20:06 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 06 Mar 2026 18:20:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf1cd52a322630e05ff2887999d6093183d6952c5afbc0c1f04cadda3151a63`  
		Last Modified: Fri, 06 Mar 2026 18:19:23 GMT  
		Size: 7.6 MB (7598399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f15c8a78545882c5b5d20de07c3b2ce913b72c7618e71dc7406f47fd2ec77f3`  
		Last Modified: Fri, 06 Mar 2026 18:20:29 GMT  
		Size: 191.0 MB (190951174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14499c88faf4f3259b248f6ef835d54060e4f6446a9a7a4d77d2aeb560008c57`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4639d26d5fea888c1dc9315370cedc0227c9a9b5da6b9aaafb06bd416b0c0cf4`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e7e125ac0ce703736242bb82a395bb092a6dc1a71fa212843686348c9d6427`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f3b4d918f0a194272c136d63f8ea5c7fc91d732070e4c39ffe7492e4e5e825`  
		Last Modified: Fri, 06 Mar 2026 18:20:26 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4788a9bd7152d1a8751ed266ec4f19f881c953b4c2dd9ca17e719aacf9eea9e`  
		Last Modified: Fri, 06 Mar 2026 18:20:26 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3f871562ee569f41853247e03faa124152cbc02b26ad4af635e9f48869262511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907bce1944962a711dcb7b0a0e2bc3e0ef2209a91fec34bb4ef7528e812caf02`

```dockerfile
```

-	Layers:
	-	`sha256:6023ddd3ff61c0a42e800fb01b931ee54d710e507a9aa8b5fa7ead51695cc85a`  
		Last Modified: Fri, 06 Mar 2026 18:20:25 GMT  
		Size: 26.0 KB (26034 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:48af527e13d25cc4eafe38faa62c7c16f4290dffefdb995220f37db57089c285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.9 MB (213852131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64554b1cdecae50f2e1a969f91c4f7d4796ca9828ba02b4698c036b3219a9545`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:40 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Mar 2026 01:15:40 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Mar 2026 01:15:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Mar 2026 01:15:40 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Mar 2026 01:15:40 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Mar 2026 01:15:40 GMT
ARG VERSION=25.8.18.1
# Tue, 17 Mar 2026 01:15:40 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Mar 2026 01:16:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:16:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Mar 2026 01:16:10 GMT
ENV TZ=UTC
# Tue, 17 Mar 2026 01:16:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.18.1 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:16:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Mar 2026 01:16:10 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Mar 2026 01:16:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Mar 2026 01:16:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624738f5fd92e7b367ade3723b173a32feb25a63a3b43c65b9c17f8b2556f391`  
		Last Modified: Tue, 17 Mar 2026 01:16:29 GMT  
		Size: 7.6 MB (7577383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345ce4ca8b8b3838829ae4173c40639b95d650c11e081e0215c83348a8365318`  
		Last Modified: Tue, 17 Mar 2026 01:16:32 GMT  
		Size: 178.0 MB (178015700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7387612f85f8dfa2149b3d338066e137bd01eecd6bc5dcdceda97d7f90678cb`  
		Last Modified: Tue, 17 Mar 2026 01:16:28 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4cec9b7d967bbb3b133fd7e8b8b1975429816982d1d3279a8c7e7aaef10bc9`  
		Last Modified: Tue, 17 Mar 2026 01:16:29 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284037406a24a7bbebec076c913f28e75c5e11ff502ef87ed70e1d14fbad4a00`  
		Last Modified: Tue, 17 Mar 2026 01:16:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad87031f83bb1367e0ba7889fa35749b0c76a4bf1171154bd5baa111f4e2b3d`  
		Last Modified: Tue, 17 Mar 2026 01:16:30 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2ae45d675d5b9b73537a5eadac12c0e86837a05dc14a287ca973e53fbd58b1`  
		Last Modified: Tue, 17 Mar 2026 01:16:30 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:36df80ae326769e4e214e790e6df6b722bef5915201d50061cd44349c482fd17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0d9829330d0bc51c1346d6969d2f634156ad6e6d512a5d0ee26ea1fc7afcfd`

```dockerfile
```

-	Layers:
	-	`sha256:87b465e3d96244b1a0315152911bb75af8d48146c0ecf3e620557b11f4fed01c`  
		Last Modified: Tue, 17 Mar 2026 01:16:28 GMT  
		Size: 26.2 KB (26245 bytes)  
		MIME: application/vnd.in-toto+json
