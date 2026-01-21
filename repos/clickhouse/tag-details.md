<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clickhouse`

-	[`clickhouse:25.10`](#clickhouse2510)
-	[`clickhouse:25.10-jammy`](#clickhouse2510-jammy)
-	[`clickhouse:25.10.4`](#clickhouse25104)
-	[`clickhouse:25.10.4-jammy`](#clickhouse25104-jammy)
-	[`clickhouse:25.10.4.104`](#clickhouse25104104)
-	[`clickhouse:25.10.4.104-jammy`](#clickhouse25104104-jammy)
-	[`clickhouse:25.11`](#clickhouse2511)
-	[`clickhouse:25.11-jammy`](#clickhouse2511-jammy)
-	[`clickhouse:25.11.6`](#clickhouse25116)
-	[`clickhouse:25.11.6-jammy`](#clickhouse25116-jammy)
-	[`clickhouse:25.11.6.11`](#clickhouse2511611)
-	[`clickhouse:25.11.6.11-jammy`](#clickhouse2511611-jammy)
-	[`clickhouse:25.12`](#clickhouse2512)
-	[`clickhouse:25.12-jammy`](#clickhouse2512-jammy)
-	[`clickhouse:25.12.3`](#clickhouse25123)
-	[`clickhouse:25.12.3-jammy`](#clickhouse25123-jammy)
-	[`clickhouse:25.12.3.21`](#clickhouse2512321)
-	[`clickhouse:25.12.3.21-jammy`](#clickhouse2512321-jammy)
-	[`clickhouse:25.3`](#clickhouse253)
-	[`clickhouse:25.3-jammy`](#clickhouse253-jammy)
-	[`clickhouse:25.3.12`](#clickhouse25312)
-	[`clickhouse:25.3.12-jammy`](#clickhouse25312-jammy)
-	[`clickhouse:25.3.12.8`](#clickhouse253128)
-	[`clickhouse:25.3.12.8-jammy`](#clickhouse253128-jammy)
-	[`clickhouse:25.8`](#clickhouse258)
-	[`clickhouse:25.8-jammy`](#clickhouse258-jammy)
-	[`clickhouse:25.8.14`](#clickhouse25814)
-	[`clickhouse:25.8.14-jammy`](#clickhouse25814-jammy)
-	[`clickhouse:25.8.14.17`](#clickhouse2581417)
-	[`clickhouse:25.8.14.17-jammy`](#clickhouse2581417-jammy)
-	[`clickhouse:jammy`](#clickhousejammy)
-	[`clickhouse:latest`](#clickhouselatest)
-	[`clickhouse:lts`](#clickhouselts)
-	[`clickhouse:lts-jammy`](#clickhouselts-jammy)

## `clickhouse:25.10`

```console
$ docker pull clickhouse@sha256:086f579e00316898ae20d8e8715bf00808dbf2ce9837925a419e9e1180d714cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.10` - linux; amd64

```console
$ docker pull clickhouse@sha256:6351431b7a6d088338be94bb6de4d308967b22a8da675426886c52f2f306edc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232890009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a0c922ca38e4a7b68f4a326f37f70ceece050a340a5b5aedfb417a320562aa`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:11:03 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:11:03 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:11:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:11:03 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:11:03 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:11:03 GMT
ARG VERSION=25.10.4.104
# Thu, 15 Jan 2026 22:11:03 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:32 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:32 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:32 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:32 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:32 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:32 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84a88e93a2661e1955318d2d4e150adba0e71973ab69884c788e9f50a712566`  
		Last Modified: Thu, 15 Jan 2026 22:11:54 GMT  
		Size: 7.6 MB (7598528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41deee8cfc0abb003e290ead3e49eb6f75e5685576d868a81e6ae2620275288a`  
		Last Modified: Thu, 15 Jan 2026 22:11:58 GMT  
		Size: 194.9 MB (194884790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af95a0672eff800e1145b064cf20096c77aceea3dfef6536a54f98899b2792c`  
		Last Modified: Thu, 15 Jan 2026 22:12:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:213c76d05277e05718814ad1d00294b3e588cccf96a3790dc6f49df0ce8d124b`  
		Last Modified: Thu, 15 Jan 2026 22:11:54 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54f0395f34317f7ad1f9a08531c513711cf9517c8b8d3cf3e5a2b0211afeebc`  
		Last Modified: Thu, 15 Jan 2026 22:11:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c537afa2b7617e943adde0d1aef466850666ecc73dc74f1b37c5f2caea75e512`  
		Last Modified: Thu, 15 Jan 2026 22:12:03 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a107612acdbe4343f75d95d9df17579058dfc5ce32d77cc968f1f75a8a23b7d`  
		Last Modified: Thu, 15 Jan 2026 22:11:55 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.10` - unknown; unknown

```console
$ docker pull clickhouse@sha256:bd90098b4d3b3a99b9c5e7842ea8f72ce2d4c84575b5718bdce9d8862ea30441
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e923b4a8c5016cf635df9a263a927955011987e3c3adc1853116a47947c1d05d`

```dockerfile
```

-	Layers:
	-	`sha256:49331d210556f75aa1ad1a66f5e33d661c588196c4d8e6694a5f8306fee932fe`  
		Last Modified: Thu, 15 Jan 2026 22:11:54 GMT  
		Size: 25.5 KB (25452 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.10` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:e4fa6a5cd85593bdb06deed9438e89373cbd49446e0039fa88e4b87085e0f650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.5 MB (217459432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cf05d48df12b284032694b827a4df9fa0c97d56ce6dc2953a74c546418c74fc`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:11:06 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:11:06 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:11:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:11:06 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:11:06 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:11:06 GMT
ARG VERSION=25.10.4.104
# Thu, 15 Jan 2026 22:11:06 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:38 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:38 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3519a8c1ec0913fb5fa0eeb4b5fccb2669056546a3b109bd3663df3533b296`  
		Last Modified: Thu, 15 Jan 2026 22:11:57 GMT  
		Size: 7.6 MB (7576713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27efb3ef0e9a9ac9cd9a4dcdfc078d62c65115c8bb713836fc028743f2e1300`  
		Last Modified: Thu, 15 Jan 2026 22:12:01 GMT  
		Size: 181.6 MB (181629194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f28bb06c96fd935a3ae0716ec2bbe06e7e615843375517e2ce0f98e9526b3a`  
		Last Modified: Thu, 15 Jan 2026 22:11:56 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222a1eba957828637391343d4faace482565ee2a71ed3125a3865e512265f570`  
		Last Modified: Thu, 15 Jan 2026 22:11:57 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da24271c02ef1d51851e13c9180fe586b6499a684a5d0b762e793f67c7b348a`  
		Last Modified: Thu, 15 Jan 2026 22:12:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6515e87788f5d23701783ad75195cafbba3632dbcc1032a2b8f60f18fdc549bb`  
		Last Modified: Thu, 15 Jan 2026 22:12:09 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3244abe62f85257e177d08d47c2e4236baa09085aea013091a941b491608635`  
		Last Modified: Thu, 15 Jan 2026 22:11:58 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.10` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c47700b9f2be48f8c6fc37dc41dc96763c84831bd64c7ca204fe7ad24fed8aed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c184eb0a6e361404cb592bd3a36a9135f21a013b9304e4b6ed8f9de64dedee6`

```dockerfile
```

-	Layers:
	-	`sha256:ac408b16a9d6b7328b0feac3a13b0d946f11bed1bc991fe0cb04f965d59ae5da`  
		Last Modified: Thu, 15 Jan 2026 22:50:16 GMT  
		Size: 25.6 KB (25640 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.10-jammy`

```console
$ docker pull clickhouse@sha256:086f579e00316898ae20d8e8715bf00808dbf2ce9837925a419e9e1180d714cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.10-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:6351431b7a6d088338be94bb6de4d308967b22a8da675426886c52f2f306edc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232890009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a0c922ca38e4a7b68f4a326f37f70ceece050a340a5b5aedfb417a320562aa`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:11:03 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:11:03 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:11:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:11:03 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:11:03 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:11:03 GMT
ARG VERSION=25.10.4.104
# Thu, 15 Jan 2026 22:11:03 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:32 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:32 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:32 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:32 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:32 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:32 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84a88e93a2661e1955318d2d4e150adba0e71973ab69884c788e9f50a712566`  
		Last Modified: Thu, 15 Jan 2026 22:11:54 GMT  
		Size: 7.6 MB (7598528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41deee8cfc0abb003e290ead3e49eb6f75e5685576d868a81e6ae2620275288a`  
		Last Modified: Thu, 15 Jan 2026 22:11:58 GMT  
		Size: 194.9 MB (194884790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af95a0672eff800e1145b064cf20096c77aceea3dfef6536a54f98899b2792c`  
		Last Modified: Thu, 15 Jan 2026 22:12:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:213c76d05277e05718814ad1d00294b3e588cccf96a3790dc6f49df0ce8d124b`  
		Last Modified: Thu, 15 Jan 2026 22:11:54 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54f0395f34317f7ad1f9a08531c513711cf9517c8b8d3cf3e5a2b0211afeebc`  
		Last Modified: Thu, 15 Jan 2026 22:11:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c537afa2b7617e943adde0d1aef466850666ecc73dc74f1b37c5f2caea75e512`  
		Last Modified: Thu, 15 Jan 2026 22:12:03 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a107612acdbe4343f75d95d9df17579058dfc5ce32d77cc968f1f75a8a23b7d`  
		Last Modified: Thu, 15 Jan 2026 22:11:55 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.10-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:bd90098b4d3b3a99b9c5e7842ea8f72ce2d4c84575b5718bdce9d8862ea30441
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e923b4a8c5016cf635df9a263a927955011987e3c3adc1853116a47947c1d05d`

```dockerfile
```

-	Layers:
	-	`sha256:49331d210556f75aa1ad1a66f5e33d661c588196c4d8e6694a5f8306fee932fe`  
		Last Modified: Thu, 15 Jan 2026 22:11:54 GMT  
		Size: 25.5 KB (25452 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.10-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:e4fa6a5cd85593bdb06deed9438e89373cbd49446e0039fa88e4b87085e0f650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.5 MB (217459432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cf05d48df12b284032694b827a4df9fa0c97d56ce6dc2953a74c546418c74fc`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:11:06 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:11:06 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:11:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:11:06 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:11:06 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:11:06 GMT
ARG VERSION=25.10.4.104
# Thu, 15 Jan 2026 22:11:06 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:38 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:38 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3519a8c1ec0913fb5fa0eeb4b5fccb2669056546a3b109bd3663df3533b296`  
		Last Modified: Thu, 15 Jan 2026 22:11:57 GMT  
		Size: 7.6 MB (7576713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27efb3ef0e9a9ac9cd9a4dcdfc078d62c65115c8bb713836fc028743f2e1300`  
		Last Modified: Thu, 15 Jan 2026 22:12:01 GMT  
		Size: 181.6 MB (181629194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f28bb06c96fd935a3ae0716ec2bbe06e7e615843375517e2ce0f98e9526b3a`  
		Last Modified: Thu, 15 Jan 2026 22:11:56 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222a1eba957828637391343d4faace482565ee2a71ed3125a3865e512265f570`  
		Last Modified: Thu, 15 Jan 2026 22:11:57 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da24271c02ef1d51851e13c9180fe586b6499a684a5d0b762e793f67c7b348a`  
		Last Modified: Thu, 15 Jan 2026 22:12:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6515e87788f5d23701783ad75195cafbba3632dbcc1032a2b8f60f18fdc549bb`  
		Last Modified: Thu, 15 Jan 2026 22:12:09 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3244abe62f85257e177d08d47c2e4236baa09085aea013091a941b491608635`  
		Last Modified: Thu, 15 Jan 2026 22:11:58 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.10-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c47700b9f2be48f8c6fc37dc41dc96763c84831bd64c7ca204fe7ad24fed8aed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c184eb0a6e361404cb592bd3a36a9135f21a013b9304e4b6ed8f9de64dedee6`

```dockerfile
```

-	Layers:
	-	`sha256:ac408b16a9d6b7328b0feac3a13b0d946f11bed1bc991fe0cb04f965d59ae5da`  
		Last Modified: Thu, 15 Jan 2026 22:50:16 GMT  
		Size: 25.6 KB (25640 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.10.4`

```console
$ docker pull clickhouse@sha256:086f579e00316898ae20d8e8715bf00808dbf2ce9837925a419e9e1180d714cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.10.4` - linux; amd64

```console
$ docker pull clickhouse@sha256:6351431b7a6d088338be94bb6de4d308967b22a8da675426886c52f2f306edc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232890009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a0c922ca38e4a7b68f4a326f37f70ceece050a340a5b5aedfb417a320562aa`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:11:03 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:11:03 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:11:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:11:03 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:11:03 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:11:03 GMT
ARG VERSION=25.10.4.104
# Thu, 15 Jan 2026 22:11:03 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:32 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:32 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:32 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:32 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:32 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:32 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84a88e93a2661e1955318d2d4e150adba0e71973ab69884c788e9f50a712566`  
		Last Modified: Thu, 15 Jan 2026 22:11:54 GMT  
		Size: 7.6 MB (7598528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41deee8cfc0abb003e290ead3e49eb6f75e5685576d868a81e6ae2620275288a`  
		Last Modified: Thu, 15 Jan 2026 22:11:58 GMT  
		Size: 194.9 MB (194884790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af95a0672eff800e1145b064cf20096c77aceea3dfef6536a54f98899b2792c`  
		Last Modified: Thu, 15 Jan 2026 22:12:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:213c76d05277e05718814ad1d00294b3e588cccf96a3790dc6f49df0ce8d124b`  
		Last Modified: Thu, 15 Jan 2026 22:11:54 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54f0395f34317f7ad1f9a08531c513711cf9517c8b8d3cf3e5a2b0211afeebc`  
		Last Modified: Thu, 15 Jan 2026 22:11:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c537afa2b7617e943adde0d1aef466850666ecc73dc74f1b37c5f2caea75e512`  
		Last Modified: Thu, 15 Jan 2026 22:12:03 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a107612acdbe4343f75d95d9df17579058dfc5ce32d77cc968f1f75a8a23b7d`  
		Last Modified: Thu, 15 Jan 2026 22:11:55 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.10.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:bd90098b4d3b3a99b9c5e7842ea8f72ce2d4c84575b5718bdce9d8862ea30441
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e923b4a8c5016cf635df9a263a927955011987e3c3adc1853116a47947c1d05d`

```dockerfile
```

-	Layers:
	-	`sha256:49331d210556f75aa1ad1a66f5e33d661c588196c4d8e6694a5f8306fee932fe`  
		Last Modified: Thu, 15 Jan 2026 22:11:54 GMT  
		Size: 25.5 KB (25452 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.10.4` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:e4fa6a5cd85593bdb06deed9438e89373cbd49446e0039fa88e4b87085e0f650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.5 MB (217459432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cf05d48df12b284032694b827a4df9fa0c97d56ce6dc2953a74c546418c74fc`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:11:06 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:11:06 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:11:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:11:06 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:11:06 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:11:06 GMT
ARG VERSION=25.10.4.104
# Thu, 15 Jan 2026 22:11:06 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:38 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:38 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3519a8c1ec0913fb5fa0eeb4b5fccb2669056546a3b109bd3663df3533b296`  
		Last Modified: Thu, 15 Jan 2026 22:11:57 GMT  
		Size: 7.6 MB (7576713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27efb3ef0e9a9ac9cd9a4dcdfc078d62c65115c8bb713836fc028743f2e1300`  
		Last Modified: Thu, 15 Jan 2026 22:12:01 GMT  
		Size: 181.6 MB (181629194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f28bb06c96fd935a3ae0716ec2bbe06e7e615843375517e2ce0f98e9526b3a`  
		Last Modified: Thu, 15 Jan 2026 22:11:56 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222a1eba957828637391343d4faace482565ee2a71ed3125a3865e512265f570`  
		Last Modified: Thu, 15 Jan 2026 22:11:57 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da24271c02ef1d51851e13c9180fe586b6499a684a5d0b762e793f67c7b348a`  
		Last Modified: Thu, 15 Jan 2026 22:12:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6515e87788f5d23701783ad75195cafbba3632dbcc1032a2b8f60f18fdc549bb`  
		Last Modified: Thu, 15 Jan 2026 22:12:09 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3244abe62f85257e177d08d47c2e4236baa09085aea013091a941b491608635`  
		Last Modified: Thu, 15 Jan 2026 22:11:58 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.10.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c47700b9f2be48f8c6fc37dc41dc96763c84831bd64c7ca204fe7ad24fed8aed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c184eb0a6e361404cb592bd3a36a9135f21a013b9304e4b6ed8f9de64dedee6`

```dockerfile
```

-	Layers:
	-	`sha256:ac408b16a9d6b7328b0feac3a13b0d946f11bed1bc991fe0cb04f965d59ae5da`  
		Last Modified: Thu, 15 Jan 2026 22:50:16 GMT  
		Size: 25.6 KB (25640 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.10.4-jammy`

```console
$ docker pull clickhouse@sha256:086f579e00316898ae20d8e8715bf00808dbf2ce9837925a419e9e1180d714cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.10.4-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:6351431b7a6d088338be94bb6de4d308967b22a8da675426886c52f2f306edc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232890009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a0c922ca38e4a7b68f4a326f37f70ceece050a340a5b5aedfb417a320562aa`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:11:03 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:11:03 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:11:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:11:03 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:11:03 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:11:03 GMT
ARG VERSION=25.10.4.104
# Thu, 15 Jan 2026 22:11:03 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:32 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:32 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:32 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:32 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:32 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:32 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84a88e93a2661e1955318d2d4e150adba0e71973ab69884c788e9f50a712566`  
		Last Modified: Thu, 15 Jan 2026 22:11:54 GMT  
		Size: 7.6 MB (7598528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41deee8cfc0abb003e290ead3e49eb6f75e5685576d868a81e6ae2620275288a`  
		Last Modified: Thu, 15 Jan 2026 22:11:58 GMT  
		Size: 194.9 MB (194884790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af95a0672eff800e1145b064cf20096c77aceea3dfef6536a54f98899b2792c`  
		Last Modified: Thu, 15 Jan 2026 22:12:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:213c76d05277e05718814ad1d00294b3e588cccf96a3790dc6f49df0ce8d124b`  
		Last Modified: Thu, 15 Jan 2026 22:11:54 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54f0395f34317f7ad1f9a08531c513711cf9517c8b8d3cf3e5a2b0211afeebc`  
		Last Modified: Thu, 15 Jan 2026 22:11:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c537afa2b7617e943adde0d1aef466850666ecc73dc74f1b37c5f2caea75e512`  
		Last Modified: Thu, 15 Jan 2026 22:12:03 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a107612acdbe4343f75d95d9df17579058dfc5ce32d77cc968f1f75a8a23b7d`  
		Last Modified: Thu, 15 Jan 2026 22:11:55 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.10.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:bd90098b4d3b3a99b9c5e7842ea8f72ce2d4c84575b5718bdce9d8862ea30441
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e923b4a8c5016cf635df9a263a927955011987e3c3adc1853116a47947c1d05d`

```dockerfile
```

-	Layers:
	-	`sha256:49331d210556f75aa1ad1a66f5e33d661c588196c4d8e6694a5f8306fee932fe`  
		Last Modified: Thu, 15 Jan 2026 22:11:54 GMT  
		Size: 25.5 KB (25452 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.10.4-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:e4fa6a5cd85593bdb06deed9438e89373cbd49446e0039fa88e4b87085e0f650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.5 MB (217459432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cf05d48df12b284032694b827a4df9fa0c97d56ce6dc2953a74c546418c74fc`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:11:06 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:11:06 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:11:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:11:06 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:11:06 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:11:06 GMT
ARG VERSION=25.10.4.104
# Thu, 15 Jan 2026 22:11:06 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:38 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:38 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3519a8c1ec0913fb5fa0eeb4b5fccb2669056546a3b109bd3663df3533b296`  
		Last Modified: Thu, 15 Jan 2026 22:11:57 GMT  
		Size: 7.6 MB (7576713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27efb3ef0e9a9ac9cd9a4dcdfc078d62c65115c8bb713836fc028743f2e1300`  
		Last Modified: Thu, 15 Jan 2026 22:12:01 GMT  
		Size: 181.6 MB (181629194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f28bb06c96fd935a3ae0716ec2bbe06e7e615843375517e2ce0f98e9526b3a`  
		Last Modified: Thu, 15 Jan 2026 22:11:56 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222a1eba957828637391343d4faace482565ee2a71ed3125a3865e512265f570`  
		Last Modified: Thu, 15 Jan 2026 22:11:57 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da24271c02ef1d51851e13c9180fe586b6499a684a5d0b762e793f67c7b348a`  
		Last Modified: Thu, 15 Jan 2026 22:12:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6515e87788f5d23701783ad75195cafbba3632dbcc1032a2b8f60f18fdc549bb`  
		Last Modified: Thu, 15 Jan 2026 22:12:09 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3244abe62f85257e177d08d47c2e4236baa09085aea013091a941b491608635`  
		Last Modified: Thu, 15 Jan 2026 22:11:58 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.10.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c47700b9f2be48f8c6fc37dc41dc96763c84831bd64c7ca204fe7ad24fed8aed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c184eb0a6e361404cb592bd3a36a9135f21a013b9304e4b6ed8f9de64dedee6`

```dockerfile
```

-	Layers:
	-	`sha256:ac408b16a9d6b7328b0feac3a13b0d946f11bed1bc991fe0cb04f965d59ae5da`  
		Last Modified: Thu, 15 Jan 2026 22:50:16 GMT  
		Size: 25.6 KB (25640 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.10.4.104`

```console
$ docker pull clickhouse@sha256:086f579e00316898ae20d8e8715bf00808dbf2ce9837925a419e9e1180d714cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.10.4.104` - linux; amd64

```console
$ docker pull clickhouse@sha256:6351431b7a6d088338be94bb6de4d308967b22a8da675426886c52f2f306edc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232890009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a0c922ca38e4a7b68f4a326f37f70ceece050a340a5b5aedfb417a320562aa`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:11:03 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:11:03 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:11:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:11:03 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:11:03 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:11:03 GMT
ARG VERSION=25.10.4.104
# Thu, 15 Jan 2026 22:11:03 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:32 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:32 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:32 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:32 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:32 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:32 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84a88e93a2661e1955318d2d4e150adba0e71973ab69884c788e9f50a712566`  
		Last Modified: Thu, 15 Jan 2026 22:11:54 GMT  
		Size: 7.6 MB (7598528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41deee8cfc0abb003e290ead3e49eb6f75e5685576d868a81e6ae2620275288a`  
		Last Modified: Thu, 15 Jan 2026 22:11:58 GMT  
		Size: 194.9 MB (194884790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af95a0672eff800e1145b064cf20096c77aceea3dfef6536a54f98899b2792c`  
		Last Modified: Thu, 15 Jan 2026 22:12:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:213c76d05277e05718814ad1d00294b3e588cccf96a3790dc6f49df0ce8d124b`  
		Last Modified: Thu, 15 Jan 2026 22:11:54 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54f0395f34317f7ad1f9a08531c513711cf9517c8b8d3cf3e5a2b0211afeebc`  
		Last Modified: Thu, 15 Jan 2026 22:11:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c537afa2b7617e943adde0d1aef466850666ecc73dc74f1b37c5f2caea75e512`  
		Last Modified: Thu, 15 Jan 2026 22:12:03 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a107612acdbe4343f75d95d9df17579058dfc5ce32d77cc968f1f75a8a23b7d`  
		Last Modified: Thu, 15 Jan 2026 22:11:55 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.10.4.104` - unknown; unknown

```console
$ docker pull clickhouse@sha256:bd90098b4d3b3a99b9c5e7842ea8f72ce2d4c84575b5718bdce9d8862ea30441
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e923b4a8c5016cf635df9a263a927955011987e3c3adc1853116a47947c1d05d`

```dockerfile
```

-	Layers:
	-	`sha256:49331d210556f75aa1ad1a66f5e33d661c588196c4d8e6694a5f8306fee932fe`  
		Last Modified: Thu, 15 Jan 2026 22:11:54 GMT  
		Size: 25.5 KB (25452 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.10.4.104` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:e4fa6a5cd85593bdb06deed9438e89373cbd49446e0039fa88e4b87085e0f650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.5 MB (217459432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cf05d48df12b284032694b827a4df9fa0c97d56ce6dc2953a74c546418c74fc`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:11:06 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:11:06 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:11:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:11:06 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:11:06 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:11:06 GMT
ARG VERSION=25.10.4.104
# Thu, 15 Jan 2026 22:11:06 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:38 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:38 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3519a8c1ec0913fb5fa0eeb4b5fccb2669056546a3b109bd3663df3533b296`  
		Last Modified: Thu, 15 Jan 2026 22:11:57 GMT  
		Size: 7.6 MB (7576713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27efb3ef0e9a9ac9cd9a4dcdfc078d62c65115c8bb713836fc028743f2e1300`  
		Last Modified: Thu, 15 Jan 2026 22:12:01 GMT  
		Size: 181.6 MB (181629194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f28bb06c96fd935a3ae0716ec2bbe06e7e615843375517e2ce0f98e9526b3a`  
		Last Modified: Thu, 15 Jan 2026 22:11:56 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222a1eba957828637391343d4faace482565ee2a71ed3125a3865e512265f570`  
		Last Modified: Thu, 15 Jan 2026 22:11:57 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da24271c02ef1d51851e13c9180fe586b6499a684a5d0b762e793f67c7b348a`  
		Last Modified: Thu, 15 Jan 2026 22:12:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6515e87788f5d23701783ad75195cafbba3632dbcc1032a2b8f60f18fdc549bb`  
		Last Modified: Thu, 15 Jan 2026 22:12:09 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3244abe62f85257e177d08d47c2e4236baa09085aea013091a941b491608635`  
		Last Modified: Thu, 15 Jan 2026 22:11:58 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.10.4.104` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c47700b9f2be48f8c6fc37dc41dc96763c84831bd64c7ca204fe7ad24fed8aed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c184eb0a6e361404cb592bd3a36a9135f21a013b9304e4b6ed8f9de64dedee6`

```dockerfile
```

-	Layers:
	-	`sha256:ac408b16a9d6b7328b0feac3a13b0d946f11bed1bc991fe0cb04f965d59ae5da`  
		Last Modified: Thu, 15 Jan 2026 22:50:16 GMT  
		Size: 25.6 KB (25640 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.10.4.104-jammy`

```console
$ docker pull clickhouse@sha256:086f579e00316898ae20d8e8715bf00808dbf2ce9837925a419e9e1180d714cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.10.4.104-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:6351431b7a6d088338be94bb6de4d308967b22a8da675426886c52f2f306edc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232890009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a0c922ca38e4a7b68f4a326f37f70ceece050a340a5b5aedfb417a320562aa`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:11:03 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:11:03 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:11:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:11:03 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:11:03 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:11:03 GMT
ARG VERSION=25.10.4.104
# Thu, 15 Jan 2026 22:11:03 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:32 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:32 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:32 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:32 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:32 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:32 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84a88e93a2661e1955318d2d4e150adba0e71973ab69884c788e9f50a712566`  
		Last Modified: Thu, 15 Jan 2026 22:11:54 GMT  
		Size: 7.6 MB (7598528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41deee8cfc0abb003e290ead3e49eb6f75e5685576d868a81e6ae2620275288a`  
		Last Modified: Thu, 15 Jan 2026 22:11:58 GMT  
		Size: 194.9 MB (194884790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af95a0672eff800e1145b064cf20096c77aceea3dfef6536a54f98899b2792c`  
		Last Modified: Thu, 15 Jan 2026 22:12:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:213c76d05277e05718814ad1d00294b3e588cccf96a3790dc6f49df0ce8d124b`  
		Last Modified: Thu, 15 Jan 2026 22:11:54 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54f0395f34317f7ad1f9a08531c513711cf9517c8b8d3cf3e5a2b0211afeebc`  
		Last Modified: Thu, 15 Jan 2026 22:11:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c537afa2b7617e943adde0d1aef466850666ecc73dc74f1b37c5f2caea75e512`  
		Last Modified: Thu, 15 Jan 2026 22:12:03 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a107612acdbe4343f75d95d9df17579058dfc5ce32d77cc968f1f75a8a23b7d`  
		Last Modified: Thu, 15 Jan 2026 22:11:55 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.10.4.104-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:bd90098b4d3b3a99b9c5e7842ea8f72ce2d4c84575b5718bdce9d8862ea30441
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e923b4a8c5016cf635df9a263a927955011987e3c3adc1853116a47947c1d05d`

```dockerfile
```

-	Layers:
	-	`sha256:49331d210556f75aa1ad1a66f5e33d661c588196c4d8e6694a5f8306fee932fe`  
		Last Modified: Thu, 15 Jan 2026 22:11:54 GMT  
		Size: 25.5 KB (25452 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.10.4.104-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:e4fa6a5cd85593bdb06deed9438e89373cbd49446e0039fa88e4b87085e0f650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.5 MB (217459432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cf05d48df12b284032694b827a4df9fa0c97d56ce6dc2953a74c546418c74fc`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:11:06 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:11:06 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:11:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:11:06 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:11:06 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:11:06 GMT
ARG VERSION=25.10.4.104
# Thu, 15 Jan 2026 22:11:06 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:38 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:38 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3519a8c1ec0913fb5fa0eeb4b5fccb2669056546a3b109bd3663df3533b296`  
		Last Modified: Thu, 15 Jan 2026 22:11:57 GMT  
		Size: 7.6 MB (7576713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27efb3ef0e9a9ac9cd9a4dcdfc078d62c65115c8bb713836fc028743f2e1300`  
		Last Modified: Thu, 15 Jan 2026 22:12:01 GMT  
		Size: 181.6 MB (181629194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f28bb06c96fd935a3ae0716ec2bbe06e7e615843375517e2ce0f98e9526b3a`  
		Last Modified: Thu, 15 Jan 2026 22:11:56 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222a1eba957828637391343d4faace482565ee2a71ed3125a3865e512265f570`  
		Last Modified: Thu, 15 Jan 2026 22:11:57 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da24271c02ef1d51851e13c9180fe586b6499a684a5d0b762e793f67c7b348a`  
		Last Modified: Thu, 15 Jan 2026 22:12:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6515e87788f5d23701783ad75195cafbba3632dbcc1032a2b8f60f18fdc549bb`  
		Last Modified: Thu, 15 Jan 2026 22:12:09 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3244abe62f85257e177d08d47c2e4236baa09085aea013091a941b491608635`  
		Last Modified: Thu, 15 Jan 2026 22:11:58 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.10.4.104-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c47700b9f2be48f8c6fc37dc41dc96763c84831bd64c7ca204fe7ad24fed8aed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c184eb0a6e361404cb592bd3a36a9135f21a013b9304e4b6ed8f9de64dedee6`

```dockerfile
```

-	Layers:
	-	`sha256:ac408b16a9d6b7328b0feac3a13b0d946f11bed1bc991fe0cb04f965d59ae5da`  
		Last Modified: Thu, 15 Jan 2026 22:50:16 GMT  
		Size: 25.6 KB (25640 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.11`

```console
$ docker pull clickhouse@sha256:fe51f09c96de0fa32353b438cd2639918fce9815ec9c52abdf9442ccb56a87ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.11` - linux; amd64

```console
$ docker pull clickhouse@sha256:6f524c1dceb2206acdf5e3067085095cfffaa754db7da471a7fe9aa363e53265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233899732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f3afe3e073ea24b0f91e2d3c02e4dd9882737a9528138353e7664f0d4c27ff7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:11:01 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:11:01 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:11:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:11:01 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:11:01 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:11:01 GMT
ARG VERSION=25.11.6.11
# Thu, 15 Jan 2026 22:11:01 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:28 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:28 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:28 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43de62778e5f89fcedecccb57537032f4b7d24902ec476f190941649d59f854a`  
		Last Modified: Thu, 15 Jan 2026 22:11:47 GMT  
		Size: 7.6 MB (7598588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb01ce10fdd3f8b3013bcd4fc5ec5519337cb49c225575e53c89494cfd6645e9`  
		Last Modified: Thu, 15 Jan 2026 22:11:51 GMT  
		Size: 195.9 MB (195894428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90fcd2878134591d0c92333f033854ddec31947de16862c220ddca54f6d4959`  
		Last Modified: Thu, 15 Jan 2026 22:11:57 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d349d2529ea1f2f1b8ffcddd9898d4118831b2ba1d38fe6bf109e9dd45e61e`  
		Last Modified: Thu, 15 Jan 2026 22:11:57 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca3142d616260a664cb9a2217a099a008c767a4ff8e352ac3b3b54b6a46ddd1`  
		Last Modified: Thu, 15 Jan 2026 22:11:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb91135e39af2c577558c88e49395c42c25a4eaedc9436f7abe00a2f68864f5`  
		Last Modified: Thu, 15 Jan 2026 22:11:57 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6bcd43c36c173a620e1d8a3d38e3eaad53c66ce20d579e820dc78a28401ead4`  
		Last Modified: Thu, 15 Jan 2026 22:11:49 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11` - unknown; unknown

```console
$ docker pull clickhouse@sha256:729560ad96c63e3746263143c9c95af51ffbbdcd224790976d22f90ea9881d09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee7f5e3f8e9a763e8e6cb6628bfb32a8f63de9dbb5e587e57a54d37a1babcb0`

```dockerfile
```

-	Layers:
	-	`sha256:f658efda0460c87d55a2513ef2c5d3d65369e846e6fb5e54ad272e8cb865e6b6`  
		Last Modified: Thu, 15 Jan 2026 22:11:47 GMT  
		Size: 25.4 KB (25437 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.11` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:d0b3ddbb14896b0c5aa9d37eb47c961f6d01784079304695e9a0d0f38c71faad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218812859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83b5a12626164c8b79d232db35f971f00662f65fb6f9952017d0cafb4a2e2fc9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:45 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:10:45 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:10:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:10:45 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:10:45 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:10:45 GMT
ARG VERSION=25.11.6.11
# Thu, 15 Jan 2026 22:10:45 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:12 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:12 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:12 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:12 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:12 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:12 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58c0e2e48a79c168e033531dabf556b1e47099b22fd56e0b45f0f2ef6f28b08`  
		Last Modified: Thu, 15 Jan 2026 22:11:43 GMT  
		Size: 7.6 MB (7576719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d893b56b1c473b5c0d4b1c6196089be507fe43c780af3073232a6aa08bd04f`  
		Last Modified: Thu, 15 Jan 2026 22:11:35 GMT  
		Size: 183.0 MB (182982599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2661e7ce812997c7780c086340d1df97c6a0f032412e86621ae5434693cf82`  
		Last Modified: Thu, 15 Jan 2026 22:11:30 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bee16393b746a37d141ffb5bda5a7bd168c66d1b94903f1013aae7c01069837`  
		Last Modified: Thu, 15 Jan 2026 22:11:42 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1199758e5ed3cb9f07a9318f51921e579e53ba1294502aefda55f41e3cdcacc`  
		Last Modified: Thu, 15 Jan 2026 22:11:42 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337187f36558c25a1f7310cceae48470a16ca813ef02131e34f0d48f016bc672`  
		Last Modified: Thu, 15 Jan 2026 22:11:42 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05fca4bd1478ce07af6e595b1ea1c177d3fcfc6fbf9844a850a0e6fc306fd03`  
		Last Modified: Thu, 15 Jan 2026 22:11:42 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a6f08525268a061e4989945673f0488cc08f243f0491f26929942eb60f3e8bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7734594116b65091ff58e787079ff1a687a0ab10b6fdc1eff21abfa576d6f0`

```dockerfile
```

-	Layers:
	-	`sha256:e4aea2fda2f70573a05ac2ecf2256737a45d9383e9eaad00e2f13a83f0f5a072`  
		Last Modified: Thu, 15 Jan 2026 22:50:33 GMT  
		Size: 25.6 KB (25625 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.11-jammy`

```console
$ docker pull clickhouse@sha256:fe51f09c96de0fa32353b438cd2639918fce9815ec9c52abdf9442ccb56a87ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.11-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:6f524c1dceb2206acdf5e3067085095cfffaa754db7da471a7fe9aa363e53265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233899732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f3afe3e073ea24b0f91e2d3c02e4dd9882737a9528138353e7664f0d4c27ff7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:11:01 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:11:01 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:11:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:11:01 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:11:01 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:11:01 GMT
ARG VERSION=25.11.6.11
# Thu, 15 Jan 2026 22:11:01 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:28 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:28 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:28 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43de62778e5f89fcedecccb57537032f4b7d24902ec476f190941649d59f854a`  
		Last Modified: Thu, 15 Jan 2026 22:11:47 GMT  
		Size: 7.6 MB (7598588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb01ce10fdd3f8b3013bcd4fc5ec5519337cb49c225575e53c89494cfd6645e9`  
		Last Modified: Thu, 15 Jan 2026 22:11:51 GMT  
		Size: 195.9 MB (195894428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90fcd2878134591d0c92333f033854ddec31947de16862c220ddca54f6d4959`  
		Last Modified: Thu, 15 Jan 2026 22:11:57 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d349d2529ea1f2f1b8ffcddd9898d4118831b2ba1d38fe6bf109e9dd45e61e`  
		Last Modified: Thu, 15 Jan 2026 22:11:57 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca3142d616260a664cb9a2217a099a008c767a4ff8e352ac3b3b54b6a46ddd1`  
		Last Modified: Thu, 15 Jan 2026 22:11:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb91135e39af2c577558c88e49395c42c25a4eaedc9436f7abe00a2f68864f5`  
		Last Modified: Thu, 15 Jan 2026 22:11:57 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6bcd43c36c173a620e1d8a3d38e3eaad53c66ce20d579e820dc78a28401ead4`  
		Last Modified: Thu, 15 Jan 2026 22:11:49 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:729560ad96c63e3746263143c9c95af51ffbbdcd224790976d22f90ea9881d09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee7f5e3f8e9a763e8e6cb6628bfb32a8f63de9dbb5e587e57a54d37a1babcb0`

```dockerfile
```

-	Layers:
	-	`sha256:f658efda0460c87d55a2513ef2c5d3d65369e846e6fb5e54ad272e8cb865e6b6`  
		Last Modified: Thu, 15 Jan 2026 22:11:47 GMT  
		Size: 25.4 KB (25437 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.11-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:d0b3ddbb14896b0c5aa9d37eb47c961f6d01784079304695e9a0d0f38c71faad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218812859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83b5a12626164c8b79d232db35f971f00662f65fb6f9952017d0cafb4a2e2fc9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:45 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:10:45 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:10:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:10:45 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:10:45 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:10:45 GMT
ARG VERSION=25.11.6.11
# Thu, 15 Jan 2026 22:10:45 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:12 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:12 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:12 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:12 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:12 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:12 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58c0e2e48a79c168e033531dabf556b1e47099b22fd56e0b45f0f2ef6f28b08`  
		Last Modified: Thu, 15 Jan 2026 22:11:43 GMT  
		Size: 7.6 MB (7576719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d893b56b1c473b5c0d4b1c6196089be507fe43c780af3073232a6aa08bd04f`  
		Last Modified: Thu, 15 Jan 2026 22:11:35 GMT  
		Size: 183.0 MB (182982599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2661e7ce812997c7780c086340d1df97c6a0f032412e86621ae5434693cf82`  
		Last Modified: Thu, 15 Jan 2026 22:11:30 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bee16393b746a37d141ffb5bda5a7bd168c66d1b94903f1013aae7c01069837`  
		Last Modified: Thu, 15 Jan 2026 22:11:42 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1199758e5ed3cb9f07a9318f51921e579e53ba1294502aefda55f41e3cdcacc`  
		Last Modified: Thu, 15 Jan 2026 22:11:42 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337187f36558c25a1f7310cceae48470a16ca813ef02131e34f0d48f016bc672`  
		Last Modified: Thu, 15 Jan 2026 22:11:42 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05fca4bd1478ce07af6e595b1ea1c177d3fcfc6fbf9844a850a0e6fc306fd03`  
		Last Modified: Thu, 15 Jan 2026 22:11:42 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a6f08525268a061e4989945673f0488cc08f243f0491f26929942eb60f3e8bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7734594116b65091ff58e787079ff1a687a0ab10b6fdc1eff21abfa576d6f0`

```dockerfile
```

-	Layers:
	-	`sha256:e4aea2fda2f70573a05ac2ecf2256737a45d9383e9eaad00e2f13a83f0f5a072`  
		Last Modified: Thu, 15 Jan 2026 22:50:33 GMT  
		Size: 25.6 KB (25625 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.11.6`

```console
$ docker pull clickhouse@sha256:fe51f09c96de0fa32353b438cd2639918fce9815ec9c52abdf9442ccb56a87ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.11.6` - linux; amd64

```console
$ docker pull clickhouse@sha256:6f524c1dceb2206acdf5e3067085095cfffaa754db7da471a7fe9aa363e53265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233899732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f3afe3e073ea24b0f91e2d3c02e4dd9882737a9528138353e7664f0d4c27ff7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:11:01 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:11:01 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:11:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:11:01 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:11:01 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:11:01 GMT
ARG VERSION=25.11.6.11
# Thu, 15 Jan 2026 22:11:01 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:28 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:28 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:28 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43de62778e5f89fcedecccb57537032f4b7d24902ec476f190941649d59f854a`  
		Last Modified: Thu, 15 Jan 2026 22:11:47 GMT  
		Size: 7.6 MB (7598588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb01ce10fdd3f8b3013bcd4fc5ec5519337cb49c225575e53c89494cfd6645e9`  
		Last Modified: Thu, 15 Jan 2026 22:11:51 GMT  
		Size: 195.9 MB (195894428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90fcd2878134591d0c92333f033854ddec31947de16862c220ddca54f6d4959`  
		Last Modified: Thu, 15 Jan 2026 22:11:57 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d349d2529ea1f2f1b8ffcddd9898d4118831b2ba1d38fe6bf109e9dd45e61e`  
		Last Modified: Thu, 15 Jan 2026 22:11:57 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca3142d616260a664cb9a2217a099a008c767a4ff8e352ac3b3b54b6a46ddd1`  
		Last Modified: Thu, 15 Jan 2026 22:11:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb91135e39af2c577558c88e49395c42c25a4eaedc9436f7abe00a2f68864f5`  
		Last Modified: Thu, 15 Jan 2026 22:11:57 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6bcd43c36c173a620e1d8a3d38e3eaad53c66ce20d579e820dc78a28401ead4`  
		Last Modified: Thu, 15 Jan 2026 22:11:49 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.6` - unknown; unknown

```console
$ docker pull clickhouse@sha256:729560ad96c63e3746263143c9c95af51ffbbdcd224790976d22f90ea9881d09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee7f5e3f8e9a763e8e6cb6628bfb32a8f63de9dbb5e587e57a54d37a1babcb0`

```dockerfile
```

-	Layers:
	-	`sha256:f658efda0460c87d55a2513ef2c5d3d65369e846e6fb5e54ad272e8cb865e6b6`  
		Last Modified: Thu, 15 Jan 2026 22:11:47 GMT  
		Size: 25.4 KB (25437 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.11.6` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:d0b3ddbb14896b0c5aa9d37eb47c961f6d01784079304695e9a0d0f38c71faad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218812859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83b5a12626164c8b79d232db35f971f00662f65fb6f9952017d0cafb4a2e2fc9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:45 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:10:45 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:10:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:10:45 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:10:45 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:10:45 GMT
ARG VERSION=25.11.6.11
# Thu, 15 Jan 2026 22:10:45 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:12 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:12 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:12 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:12 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:12 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:12 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58c0e2e48a79c168e033531dabf556b1e47099b22fd56e0b45f0f2ef6f28b08`  
		Last Modified: Thu, 15 Jan 2026 22:11:43 GMT  
		Size: 7.6 MB (7576719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d893b56b1c473b5c0d4b1c6196089be507fe43c780af3073232a6aa08bd04f`  
		Last Modified: Thu, 15 Jan 2026 22:11:35 GMT  
		Size: 183.0 MB (182982599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2661e7ce812997c7780c086340d1df97c6a0f032412e86621ae5434693cf82`  
		Last Modified: Thu, 15 Jan 2026 22:11:30 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bee16393b746a37d141ffb5bda5a7bd168c66d1b94903f1013aae7c01069837`  
		Last Modified: Thu, 15 Jan 2026 22:11:42 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1199758e5ed3cb9f07a9318f51921e579e53ba1294502aefda55f41e3cdcacc`  
		Last Modified: Thu, 15 Jan 2026 22:11:42 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337187f36558c25a1f7310cceae48470a16ca813ef02131e34f0d48f016bc672`  
		Last Modified: Thu, 15 Jan 2026 22:11:42 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05fca4bd1478ce07af6e595b1ea1c177d3fcfc6fbf9844a850a0e6fc306fd03`  
		Last Modified: Thu, 15 Jan 2026 22:11:42 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.6` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a6f08525268a061e4989945673f0488cc08f243f0491f26929942eb60f3e8bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7734594116b65091ff58e787079ff1a687a0ab10b6fdc1eff21abfa576d6f0`

```dockerfile
```

-	Layers:
	-	`sha256:e4aea2fda2f70573a05ac2ecf2256737a45d9383e9eaad00e2f13a83f0f5a072`  
		Last Modified: Thu, 15 Jan 2026 22:50:33 GMT  
		Size: 25.6 KB (25625 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.11.6-jammy`

```console
$ docker pull clickhouse@sha256:fe51f09c96de0fa32353b438cd2639918fce9815ec9c52abdf9442ccb56a87ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.11.6-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:6f524c1dceb2206acdf5e3067085095cfffaa754db7da471a7fe9aa363e53265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233899732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f3afe3e073ea24b0f91e2d3c02e4dd9882737a9528138353e7664f0d4c27ff7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:11:01 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:11:01 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:11:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:11:01 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:11:01 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:11:01 GMT
ARG VERSION=25.11.6.11
# Thu, 15 Jan 2026 22:11:01 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:28 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:28 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:28 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43de62778e5f89fcedecccb57537032f4b7d24902ec476f190941649d59f854a`  
		Last Modified: Thu, 15 Jan 2026 22:11:47 GMT  
		Size: 7.6 MB (7598588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb01ce10fdd3f8b3013bcd4fc5ec5519337cb49c225575e53c89494cfd6645e9`  
		Last Modified: Thu, 15 Jan 2026 22:11:51 GMT  
		Size: 195.9 MB (195894428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90fcd2878134591d0c92333f033854ddec31947de16862c220ddca54f6d4959`  
		Last Modified: Thu, 15 Jan 2026 22:11:57 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d349d2529ea1f2f1b8ffcddd9898d4118831b2ba1d38fe6bf109e9dd45e61e`  
		Last Modified: Thu, 15 Jan 2026 22:11:57 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca3142d616260a664cb9a2217a099a008c767a4ff8e352ac3b3b54b6a46ddd1`  
		Last Modified: Thu, 15 Jan 2026 22:11:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb91135e39af2c577558c88e49395c42c25a4eaedc9436f7abe00a2f68864f5`  
		Last Modified: Thu, 15 Jan 2026 22:11:57 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6bcd43c36c173a620e1d8a3d38e3eaad53c66ce20d579e820dc78a28401ead4`  
		Last Modified: Thu, 15 Jan 2026 22:11:49 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.6-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:729560ad96c63e3746263143c9c95af51ffbbdcd224790976d22f90ea9881d09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee7f5e3f8e9a763e8e6cb6628bfb32a8f63de9dbb5e587e57a54d37a1babcb0`

```dockerfile
```

-	Layers:
	-	`sha256:f658efda0460c87d55a2513ef2c5d3d65369e846e6fb5e54ad272e8cb865e6b6`  
		Last Modified: Thu, 15 Jan 2026 22:11:47 GMT  
		Size: 25.4 KB (25437 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.11.6-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:d0b3ddbb14896b0c5aa9d37eb47c961f6d01784079304695e9a0d0f38c71faad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218812859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83b5a12626164c8b79d232db35f971f00662f65fb6f9952017d0cafb4a2e2fc9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:45 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:10:45 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:10:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:10:45 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:10:45 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:10:45 GMT
ARG VERSION=25.11.6.11
# Thu, 15 Jan 2026 22:10:45 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:12 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:12 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:12 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:12 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:12 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:12 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58c0e2e48a79c168e033531dabf556b1e47099b22fd56e0b45f0f2ef6f28b08`  
		Last Modified: Thu, 15 Jan 2026 22:11:43 GMT  
		Size: 7.6 MB (7576719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d893b56b1c473b5c0d4b1c6196089be507fe43c780af3073232a6aa08bd04f`  
		Last Modified: Thu, 15 Jan 2026 22:11:35 GMT  
		Size: 183.0 MB (182982599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2661e7ce812997c7780c086340d1df97c6a0f032412e86621ae5434693cf82`  
		Last Modified: Thu, 15 Jan 2026 22:11:30 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bee16393b746a37d141ffb5bda5a7bd168c66d1b94903f1013aae7c01069837`  
		Last Modified: Thu, 15 Jan 2026 22:11:42 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1199758e5ed3cb9f07a9318f51921e579e53ba1294502aefda55f41e3cdcacc`  
		Last Modified: Thu, 15 Jan 2026 22:11:42 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337187f36558c25a1f7310cceae48470a16ca813ef02131e34f0d48f016bc672`  
		Last Modified: Thu, 15 Jan 2026 22:11:42 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05fca4bd1478ce07af6e595b1ea1c177d3fcfc6fbf9844a850a0e6fc306fd03`  
		Last Modified: Thu, 15 Jan 2026 22:11:42 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.6-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a6f08525268a061e4989945673f0488cc08f243f0491f26929942eb60f3e8bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7734594116b65091ff58e787079ff1a687a0ab10b6fdc1eff21abfa576d6f0`

```dockerfile
```

-	Layers:
	-	`sha256:e4aea2fda2f70573a05ac2ecf2256737a45d9383e9eaad00e2f13a83f0f5a072`  
		Last Modified: Thu, 15 Jan 2026 22:50:33 GMT  
		Size: 25.6 KB (25625 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.11.6.11`

```console
$ docker pull clickhouse@sha256:fe51f09c96de0fa32353b438cd2639918fce9815ec9c52abdf9442ccb56a87ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.11.6.11` - linux; amd64

```console
$ docker pull clickhouse@sha256:6f524c1dceb2206acdf5e3067085095cfffaa754db7da471a7fe9aa363e53265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233899732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f3afe3e073ea24b0f91e2d3c02e4dd9882737a9528138353e7664f0d4c27ff7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:11:01 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:11:01 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:11:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:11:01 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:11:01 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:11:01 GMT
ARG VERSION=25.11.6.11
# Thu, 15 Jan 2026 22:11:01 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:28 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:28 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:28 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43de62778e5f89fcedecccb57537032f4b7d24902ec476f190941649d59f854a`  
		Last Modified: Thu, 15 Jan 2026 22:11:47 GMT  
		Size: 7.6 MB (7598588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb01ce10fdd3f8b3013bcd4fc5ec5519337cb49c225575e53c89494cfd6645e9`  
		Last Modified: Thu, 15 Jan 2026 22:11:51 GMT  
		Size: 195.9 MB (195894428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90fcd2878134591d0c92333f033854ddec31947de16862c220ddca54f6d4959`  
		Last Modified: Thu, 15 Jan 2026 22:11:57 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d349d2529ea1f2f1b8ffcddd9898d4118831b2ba1d38fe6bf109e9dd45e61e`  
		Last Modified: Thu, 15 Jan 2026 22:11:57 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca3142d616260a664cb9a2217a099a008c767a4ff8e352ac3b3b54b6a46ddd1`  
		Last Modified: Thu, 15 Jan 2026 22:11:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb91135e39af2c577558c88e49395c42c25a4eaedc9436f7abe00a2f68864f5`  
		Last Modified: Thu, 15 Jan 2026 22:11:57 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6bcd43c36c173a620e1d8a3d38e3eaad53c66ce20d579e820dc78a28401ead4`  
		Last Modified: Thu, 15 Jan 2026 22:11:49 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.6.11` - unknown; unknown

```console
$ docker pull clickhouse@sha256:729560ad96c63e3746263143c9c95af51ffbbdcd224790976d22f90ea9881d09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee7f5e3f8e9a763e8e6cb6628bfb32a8f63de9dbb5e587e57a54d37a1babcb0`

```dockerfile
```

-	Layers:
	-	`sha256:f658efda0460c87d55a2513ef2c5d3d65369e846e6fb5e54ad272e8cb865e6b6`  
		Last Modified: Thu, 15 Jan 2026 22:11:47 GMT  
		Size: 25.4 KB (25437 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.11.6.11` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:d0b3ddbb14896b0c5aa9d37eb47c961f6d01784079304695e9a0d0f38c71faad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218812859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83b5a12626164c8b79d232db35f971f00662f65fb6f9952017d0cafb4a2e2fc9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:45 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:10:45 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:10:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:10:45 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:10:45 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:10:45 GMT
ARG VERSION=25.11.6.11
# Thu, 15 Jan 2026 22:10:45 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:12 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:12 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:12 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:12 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:12 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:12 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58c0e2e48a79c168e033531dabf556b1e47099b22fd56e0b45f0f2ef6f28b08`  
		Last Modified: Thu, 15 Jan 2026 22:11:43 GMT  
		Size: 7.6 MB (7576719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d893b56b1c473b5c0d4b1c6196089be507fe43c780af3073232a6aa08bd04f`  
		Last Modified: Thu, 15 Jan 2026 22:11:35 GMT  
		Size: 183.0 MB (182982599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2661e7ce812997c7780c086340d1df97c6a0f032412e86621ae5434693cf82`  
		Last Modified: Thu, 15 Jan 2026 22:11:30 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bee16393b746a37d141ffb5bda5a7bd168c66d1b94903f1013aae7c01069837`  
		Last Modified: Thu, 15 Jan 2026 22:11:42 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1199758e5ed3cb9f07a9318f51921e579e53ba1294502aefda55f41e3cdcacc`  
		Last Modified: Thu, 15 Jan 2026 22:11:42 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337187f36558c25a1f7310cceae48470a16ca813ef02131e34f0d48f016bc672`  
		Last Modified: Thu, 15 Jan 2026 22:11:42 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05fca4bd1478ce07af6e595b1ea1c177d3fcfc6fbf9844a850a0e6fc306fd03`  
		Last Modified: Thu, 15 Jan 2026 22:11:42 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.6.11` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a6f08525268a061e4989945673f0488cc08f243f0491f26929942eb60f3e8bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7734594116b65091ff58e787079ff1a687a0ab10b6fdc1eff21abfa576d6f0`

```dockerfile
```

-	Layers:
	-	`sha256:e4aea2fda2f70573a05ac2ecf2256737a45d9383e9eaad00e2f13a83f0f5a072`  
		Last Modified: Thu, 15 Jan 2026 22:50:33 GMT  
		Size: 25.6 KB (25625 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.11.6.11-jammy`

```console
$ docker pull clickhouse@sha256:fe51f09c96de0fa32353b438cd2639918fce9815ec9c52abdf9442ccb56a87ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.11.6.11-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:6f524c1dceb2206acdf5e3067085095cfffaa754db7da471a7fe9aa363e53265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233899732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f3afe3e073ea24b0f91e2d3c02e4dd9882737a9528138353e7664f0d4c27ff7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:11:01 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:11:01 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:11:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:11:01 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:11:01 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:11:01 GMT
ARG VERSION=25.11.6.11
# Thu, 15 Jan 2026 22:11:01 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:28 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:28 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:28 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43de62778e5f89fcedecccb57537032f4b7d24902ec476f190941649d59f854a`  
		Last Modified: Thu, 15 Jan 2026 22:11:47 GMT  
		Size: 7.6 MB (7598588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb01ce10fdd3f8b3013bcd4fc5ec5519337cb49c225575e53c89494cfd6645e9`  
		Last Modified: Thu, 15 Jan 2026 22:11:51 GMT  
		Size: 195.9 MB (195894428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90fcd2878134591d0c92333f033854ddec31947de16862c220ddca54f6d4959`  
		Last Modified: Thu, 15 Jan 2026 22:11:57 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d349d2529ea1f2f1b8ffcddd9898d4118831b2ba1d38fe6bf109e9dd45e61e`  
		Last Modified: Thu, 15 Jan 2026 22:11:57 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca3142d616260a664cb9a2217a099a008c767a4ff8e352ac3b3b54b6a46ddd1`  
		Last Modified: Thu, 15 Jan 2026 22:11:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb91135e39af2c577558c88e49395c42c25a4eaedc9436f7abe00a2f68864f5`  
		Last Modified: Thu, 15 Jan 2026 22:11:57 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6bcd43c36c173a620e1d8a3d38e3eaad53c66ce20d579e820dc78a28401ead4`  
		Last Modified: Thu, 15 Jan 2026 22:11:49 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.6.11-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:729560ad96c63e3746263143c9c95af51ffbbdcd224790976d22f90ea9881d09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee7f5e3f8e9a763e8e6cb6628bfb32a8f63de9dbb5e587e57a54d37a1babcb0`

```dockerfile
```

-	Layers:
	-	`sha256:f658efda0460c87d55a2513ef2c5d3d65369e846e6fb5e54ad272e8cb865e6b6`  
		Last Modified: Thu, 15 Jan 2026 22:11:47 GMT  
		Size: 25.4 KB (25437 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.11.6.11-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:d0b3ddbb14896b0c5aa9d37eb47c961f6d01784079304695e9a0d0f38c71faad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218812859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83b5a12626164c8b79d232db35f971f00662f65fb6f9952017d0cafb4a2e2fc9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:45 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:10:45 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:10:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:10:45 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:10:45 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:10:45 GMT
ARG VERSION=25.11.6.11
# Thu, 15 Jan 2026 22:10:45 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:12 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:12 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:12 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:12 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:12 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:12 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58c0e2e48a79c168e033531dabf556b1e47099b22fd56e0b45f0f2ef6f28b08`  
		Last Modified: Thu, 15 Jan 2026 22:11:43 GMT  
		Size: 7.6 MB (7576719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d893b56b1c473b5c0d4b1c6196089be507fe43c780af3073232a6aa08bd04f`  
		Last Modified: Thu, 15 Jan 2026 22:11:35 GMT  
		Size: 183.0 MB (182982599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2661e7ce812997c7780c086340d1df97c6a0f032412e86621ae5434693cf82`  
		Last Modified: Thu, 15 Jan 2026 22:11:30 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bee16393b746a37d141ffb5bda5a7bd168c66d1b94903f1013aae7c01069837`  
		Last Modified: Thu, 15 Jan 2026 22:11:42 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1199758e5ed3cb9f07a9318f51921e579e53ba1294502aefda55f41e3cdcacc`  
		Last Modified: Thu, 15 Jan 2026 22:11:42 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337187f36558c25a1f7310cceae48470a16ca813ef02131e34f0d48f016bc672`  
		Last Modified: Thu, 15 Jan 2026 22:11:42 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05fca4bd1478ce07af6e595b1ea1c177d3fcfc6fbf9844a850a0e6fc306fd03`  
		Last Modified: Thu, 15 Jan 2026 22:11:42 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.6.11-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a6f08525268a061e4989945673f0488cc08f243f0491f26929942eb60f3e8bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7734594116b65091ff58e787079ff1a687a0ab10b6fdc1eff21abfa576d6f0`

```dockerfile
```

-	Layers:
	-	`sha256:e4aea2fda2f70573a05ac2ecf2256737a45d9383e9eaad00e2f13a83f0f5a072`  
		Last Modified: Thu, 15 Jan 2026 22:50:33 GMT  
		Size: 25.6 KB (25625 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.12`

```console
$ docker pull clickhouse@sha256:9c348b2bd082bf71b8401397bb79f75e6698f3de0f1552f2742dab4e6909377e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.12` - linux; amd64

```console
$ docker pull clickhouse@sha256:e87ff5cc4db0ee4bd74404347ba9caa3e3ab5ef325db02aa1ba773f0f823ea81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246322771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852801b390c937417eee197f95cae6c5575ef31f3bc676501e5733f2732fa92a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:45 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:10:45 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:10:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:10:45 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:10:45 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:10:45 GMT
ARG VERSION=25.12.3.21
# Thu, 15 Jan 2026 22:10:45 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:15 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:15 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:15 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:16 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:16 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:16 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83cb5d9b0d9196f8fbe14025ad18475a55f20d4a27d7ec251d3790d05808e146`  
		Last Modified: Thu, 15 Jan 2026 22:11:49 GMT  
		Size: 7.6 MB (7598550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab75fa925b2df2acd4af08b5acff65f28cd8bdfeb13b687340aaa11fc602623`  
		Last Modified: Thu, 15 Jan 2026 22:52:15 GMT  
		Size: 208.3 MB (208317501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed06808047e10a168d67bf3d37fd53b16619284a18291d24e0e035551b64bba3`  
		Last Modified: Thu, 15 Jan 2026 22:11:37 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88194bfab547d36d32697803376d16fa6f50a5706e11835d6b2e5149249e3fd4`  
		Last Modified: Thu, 15 Jan 2026 22:11:38 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9694b94933bd348b79a326e9e90b99c980c93497916c9afea0517e9e59510dbd`  
		Last Modified: Thu, 15 Jan 2026 22:11:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c40bd2e7d92e7c7db010275427785be0871517f608b23e3062d094e4f11009`  
		Last Modified: Thu, 15 Jan 2026 22:11:39 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05fca4bd1478ce07af6e595b1ea1c177d3fcfc6fbf9844a850a0e6fc306fd03`  
		Last Modified: Thu, 15 Jan 2026 22:11:42 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8deb39a713f008acdec3251678de02eb74fdfffabbb7e17040b103fd78983a21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73dda45360c6471ea6f661c4f5ae30a7ffc26ae55624a1ad6d5cac45ff451818`

```dockerfile
```

-	Layers:
	-	`sha256:ed29f8b17477a4026a6b1c15b5babe8cec498591f0abd7fc02b73306b0839930`  
		Last Modified: Thu, 15 Jan 2026 22:50:48 GMT  
		Size: 26.0 KB (26047 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.12` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:30190af3158d8b3b3a48f60bdabfc40f26b446d16f28529014262d88e5dd2b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228224093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b161afcc2f6dd175ca36bc983f0bb75365d90b91db4bfcbc023a9c93ed07e9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:34 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:10:34 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:10:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:10:34 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:10:34 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:10:34 GMT
ARG VERSION=25.12.3.21
# Thu, 15 Jan 2026 22:10:34 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:04 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:04 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3df312c201c41d963c5bdc407650a174e7712d5b8aff75c83b0c6e2755b1208`  
		Last Modified: Thu, 15 Jan 2026 22:11:26 GMT  
		Size: 7.6 MB (7576689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bb9a92d4b2fd9436589e7c5649592d95edac119b4ab6a8460c0700e67ffa37`  
		Last Modified: Thu, 15 Jan 2026 22:11:29 GMT  
		Size: 192.4 MB (192393858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ccbc4119e8834350abf692cba0442fb6e8b1ae37944efd9240f68e493868a07`  
		Last Modified: Thu, 15 Jan 2026 22:11:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5438f0c9f26c70a44ea1b4bc005c852e7919abc5eede23dd3a7b6f26015d11`  
		Last Modified: Thu, 15 Jan 2026 22:11:26 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7f0fe7586dc17cf8a7c98584015cc914819093423666de59fbdd09517f7018`  
		Last Modified: Thu, 15 Jan 2026 22:28:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da9049ed0141a54a80279b382c924b58ddfd2bdd4b30df9481610ecbb1ca834`  
		Last Modified: Thu, 15 Jan 2026 22:11:36 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aaec0e1cac56fdd17db6b0d9f73eafdf93fd7ecbc8a724f365da206621940c5`  
		Last Modified: Thu, 15 Jan 2026 22:11:28 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12` - unknown; unknown

```console
$ docker pull clickhouse@sha256:72d6bc00b24890fcefc779de396dd7bf35973955caff366e6957e679fd5f6f34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66aeb9bbe2041bbf2c5fdaca3c3705af0cfc09ea38f7e9eeb469af9a7e3ee66b`

```dockerfile
```

-	Layers:
	-	`sha256:166252afa9942cdc70c9de156ab1064cca9eeee6a864d1fa47f76f812f2431b3`  
		Last Modified: Thu, 15 Jan 2026 22:11:26 GMT  
		Size: 26.3 KB (26258 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.12-jammy`

```console
$ docker pull clickhouse@sha256:9c348b2bd082bf71b8401397bb79f75e6698f3de0f1552f2742dab4e6909377e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.12-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:e87ff5cc4db0ee4bd74404347ba9caa3e3ab5ef325db02aa1ba773f0f823ea81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246322771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852801b390c937417eee197f95cae6c5575ef31f3bc676501e5733f2732fa92a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:45 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:10:45 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:10:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:10:45 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:10:45 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:10:45 GMT
ARG VERSION=25.12.3.21
# Thu, 15 Jan 2026 22:10:45 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:15 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:15 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:15 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:16 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:16 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:16 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83cb5d9b0d9196f8fbe14025ad18475a55f20d4a27d7ec251d3790d05808e146`  
		Last Modified: Thu, 15 Jan 2026 22:11:49 GMT  
		Size: 7.6 MB (7598550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab75fa925b2df2acd4af08b5acff65f28cd8bdfeb13b687340aaa11fc602623`  
		Last Modified: Thu, 15 Jan 2026 22:52:15 GMT  
		Size: 208.3 MB (208317501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed06808047e10a168d67bf3d37fd53b16619284a18291d24e0e035551b64bba3`  
		Last Modified: Thu, 15 Jan 2026 22:11:37 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88194bfab547d36d32697803376d16fa6f50a5706e11835d6b2e5149249e3fd4`  
		Last Modified: Thu, 15 Jan 2026 22:11:38 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9694b94933bd348b79a326e9e90b99c980c93497916c9afea0517e9e59510dbd`  
		Last Modified: Thu, 15 Jan 2026 22:11:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c40bd2e7d92e7c7db010275427785be0871517f608b23e3062d094e4f11009`  
		Last Modified: Thu, 15 Jan 2026 22:11:39 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05fca4bd1478ce07af6e595b1ea1c177d3fcfc6fbf9844a850a0e6fc306fd03`  
		Last Modified: Thu, 15 Jan 2026 22:11:42 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8deb39a713f008acdec3251678de02eb74fdfffabbb7e17040b103fd78983a21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73dda45360c6471ea6f661c4f5ae30a7ffc26ae55624a1ad6d5cac45ff451818`

```dockerfile
```

-	Layers:
	-	`sha256:ed29f8b17477a4026a6b1c15b5babe8cec498591f0abd7fc02b73306b0839930`  
		Last Modified: Thu, 15 Jan 2026 22:50:48 GMT  
		Size: 26.0 KB (26047 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.12-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:30190af3158d8b3b3a48f60bdabfc40f26b446d16f28529014262d88e5dd2b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228224093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b161afcc2f6dd175ca36bc983f0bb75365d90b91db4bfcbc023a9c93ed07e9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:34 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:10:34 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:10:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:10:34 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:10:34 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:10:34 GMT
ARG VERSION=25.12.3.21
# Thu, 15 Jan 2026 22:10:34 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:04 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:04 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3df312c201c41d963c5bdc407650a174e7712d5b8aff75c83b0c6e2755b1208`  
		Last Modified: Thu, 15 Jan 2026 22:11:26 GMT  
		Size: 7.6 MB (7576689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bb9a92d4b2fd9436589e7c5649592d95edac119b4ab6a8460c0700e67ffa37`  
		Last Modified: Thu, 15 Jan 2026 22:11:29 GMT  
		Size: 192.4 MB (192393858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ccbc4119e8834350abf692cba0442fb6e8b1ae37944efd9240f68e493868a07`  
		Last Modified: Thu, 15 Jan 2026 22:11:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5438f0c9f26c70a44ea1b4bc005c852e7919abc5eede23dd3a7b6f26015d11`  
		Last Modified: Thu, 15 Jan 2026 22:11:26 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7f0fe7586dc17cf8a7c98584015cc914819093423666de59fbdd09517f7018`  
		Last Modified: Thu, 15 Jan 2026 22:28:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da9049ed0141a54a80279b382c924b58ddfd2bdd4b30df9481610ecbb1ca834`  
		Last Modified: Thu, 15 Jan 2026 22:11:36 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aaec0e1cac56fdd17db6b0d9f73eafdf93fd7ecbc8a724f365da206621940c5`  
		Last Modified: Thu, 15 Jan 2026 22:11:28 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:72d6bc00b24890fcefc779de396dd7bf35973955caff366e6957e679fd5f6f34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66aeb9bbe2041bbf2c5fdaca3c3705af0cfc09ea38f7e9eeb469af9a7e3ee66b`

```dockerfile
```

-	Layers:
	-	`sha256:166252afa9942cdc70c9de156ab1064cca9eeee6a864d1fa47f76f812f2431b3`  
		Last Modified: Thu, 15 Jan 2026 22:11:26 GMT  
		Size: 26.3 KB (26258 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.12.3`

```console
$ docker pull clickhouse@sha256:9c348b2bd082bf71b8401397bb79f75e6698f3de0f1552f2742dab4e6909377e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.12.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:e87ff5cc4db0ee4bd74404347ba9caa3e3ab5ef325db02aa1ba773f0f823ea81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246322771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852801b390c937417eee197f95cae6c5575ef31f3bc676501e5733f2732fa92a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:45 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:10:45 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:10:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:10:45 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:10:45 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:10:45 GMT
ARG VERSION=25.12.3.21
# Thu, 15 Jan 2026 22:10:45 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:15 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:15 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:15 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:16 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:16 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:16 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83cb5d9b0d9196f8fbe14025ad18475a55f20d4a27d7ec251d3790d05808e146`  
		Last Modified: Thu, 15 Jan 2026 22:11:49 GMT  
		Size: 7.6 MB (7598550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab75fa925b2df2acd4af08b5acff65f28cd8bdfeb13b687340aaa11fc602623`  
		Last Modified: Thu, 15 Jan 2026 22:52:15 GMT  
		Size: 208.3 MB (208317501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed06808047e10a168d67bf3d37fd53b16619284a18291d24e0e035551b64bba3`  
		Last Modified: Thu, 15 Jan 2026 22:11:37 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88194bfab547d36d32697803376d16fa6f50a5706e11835d6b2e5149249e3fd4`  
		Last Modified: Thu, 15 Jan 2026 22:11:38 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9694b94933bd348b79a326e9e90b99c980c93497916c9afea0517e9e59510dbd`  
		Last Modified: Thu, 15 Jan 2026 22:11:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c40bd2e7d92e7c7db010275427785be0871517f608b23e3062d094e4f11009`  
		Last Modified: Thu, 15 Jan 2026 22:11:39 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05fca4bd1478ce07af6e595b1ea1c177d3fcfc6fbf9844a850a0e6fc306fd03`  
		Last Modified: Thu, 15 Jan 2026 22:11:42 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8deb39a713f008acdec3251678de02eb74fdfffabbb7e17040b103fd78983a21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73dda45360c6471ea6f661c4f5ae30a7ffc26ae55624a1ad6d5cac45ff451818`

```dockerfile
```

-	Layers:
	-	`sha256:ed29f8b17477a4026a6b1c15b5babe8cec498591f0abd7fc02b73306b0839930`  
		Last Modified: Thu, 15 Jan 2026 22:50:48 GMT  
		Size: 26.0 KB (26047 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.12.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:30190af3158d8b3b3a48f60bdabfc40f26b446d16f28529014262d88e5dd2b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228224093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b161afcc2f6dd175ca36bc983f0bb75365d90b91db4bfcbc023a9c93ed07e9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:34 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:10:34 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:10:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:10:34 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:10:34 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:10:34 GMT
ARG VERSION=25.12.3.21
# Thu, 15 Jan 2026 22:10:34 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:04 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:04 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3df312c201c41d963c5bdc407650a174e7712d5b8aff75c83b0c6e2755b1208`  
		Last Modified: Thu, 15 Jan 2026 22:11:26 GMT  
		Size: 7.6 MB (7576689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bb9a92d4b2fd9436589e7c5649592d95edac119b4ab6a8460c0700e67ffa37`  
		Last Modified: Thu, 15 Jan 2026 22:11:29 GMT  
		Size: 192.4 MB (192393858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ccbc4119e8834350abf692cba0442fb6e8b1ae37944efd9240f68e493868a07`  
		Last Modified: Thu, 15 Jan 2026 22:11:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5438f0c9f26c70a44ea1b4bc005c852e7919abc5eede23dd3a7b6f26015d11`  
		Last Modified: Thu, 15 Jan 2026 22:11:26 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7f0fe7586dc17cf8a7c98584015cc914819093423666de59fbdd09517f7018`  
		Last Modified: Thu, 15 Jan 2026 22:28:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da9049ed0141a54a80279b382c924b58ddfd2bdd4b30df9481610ecbb1ca834`  
		Last Modified: Thu, 15 Jan 2026 22:11:36 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aaec0e1cac56fdd17db6b0d9f73eafdf93fd7ecbc8a724f365da206621940c5`  
		Last Modified: Thu, 15 Jan 2026 22:11:28 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:72d6bc00b24890fcefc779de396dd7bf35973955caff366e6957e679fd5f6f34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66aeb9bbe2041bbf2c5fdaca3c3705af0cfc09ea38f7e9eeb469af9a7e3ee66b`

```dockerfile
```

-	Layers:
	-	`sha256:166252afa9942cdc70c9de156ab1064cca9eeee6a864d1fa47f76f812f2431b3`  
		Last Modified: Thu, 15 Jan 2026 22:11:26 GMT  
		Size: 26.3 KB (26258 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.12.3-jammy`

```console
$ docker pull clickhouse@sha256:9c348b2bd082bf71b8401397bb79f75e6698f3de0f1552f2742dab4e6909377e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.12.3-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:e87ff5cc4db0ee4bd74404347ba9caa3e3ab5ef325db02aa1ba773f0f823ea81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246322771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852801b390c937417eee197f95cae6c5575ef31f3bc676501e5733f2732fa92a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:45 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:10:45 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:10:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:10:45 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:10:45 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:10:45 GMT
ARG VERSION=25.12.3.21
# Thu, 15 Jan 2026 22:10:45 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:15 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:15 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:15 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:16 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:16 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:16 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83cb5d9b0d9196f8fbe14025ad18475a55f20d4a27d7ec251d3790d05808e146`  
		Last Modified: Thu, 15 Jan 2026 22:11:49 GMT  
		Size: 7.6 MB (7598550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab75fa925b2df2acd4af08b5acff65f28cd8bdfeb13b687340aaa11fc602623`  
		Last Modified: Thu, 15 Jan 2026 22:52:15 GMT  
		Size: 208.3 MB (208317501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed06808047e10a168d67bf3d37fd53b16619284a18291d24e0e035551b64bba3`  
		Last Modified: Thu, 15 Jan 2026 22:11:37 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88194bfab547d36d32697803376d16fa6f50a5706e11835d6b2e5149249e3fd4`  
		Last Modified: Thu, 15 Jan 2026 22:11:38 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9694b94933bd348b79a326e9e90b99c980c93497916c9afea0517e9e59510dbd`  
		Last Modified: Thu, 15 Jan 2026 22:11:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c40bd2e7d92e7c7db010275427785be0871517f608b23e3062d094e4f11009`  
		Last Modified: Thu, 15 Jan 2026 22:11:39 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05fca4bd1478ce07af6e595b1ea1c177d3fcfc6fbf9844a850a0e6fc306fd03`  
		Last Modified: Thu, 15 Jan 2026 22:11:42 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8deb39a713f008acdec3251678de02eb74fdfffabbb7e17040b103fd78983a21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73dda45360c6471ea6f661c4f5ae30a7ffc26ae55624a1ad6d5cac45ff451818`

```dockerfile
```

-	Layers:
	-	`sha256:ed29f8b17477a4026a6b1c15b5babe8cec498591f0abd7fc02b73306b0839930`  
		Last Modified: Thu, 15 Jan 2026 22:50:48 GMT  
		Size: 26.0 KB (26047 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.12.3-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:30190af3158d8b3b3a48f60bdabfc40f26b446d16f28529014262d88e5dd2b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228224093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b161afcc2f6dd175ca36bc983f0bb75365d90b91db4bfcbc023a9c93ed07e9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:34 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:10:34 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:10:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:10:34 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:10:34 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:10:34 GMT
ARG VERSION=25.12.3.21
# Thu, 15 Jan 2026 22:10:34 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:04 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:04 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3df312c201c41d963c5bdc407650a174e7712d5b8aff75c83b0c6e2755b1208`  
		Last Modified: Thu, 15 Jan 2026 22:11:26 GMT  
		Size: 7.6 MB (7576689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bb9a92d4b2fd9436589e7c5649592d95edac119b4ab6a8460c0700e67ffa37`  
		Last Modified: Thu, 15 Jan 2026 22:11:29 GMT  
		Size: 192.4 MB (192393858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ccbc4119e8834350abf692cba0442fb6e8b1ae37944efd9240f68e493868a07`  
		Last Modified: Thu, 15 Jan 2026 22:11:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5438f0c9f26c70a44ea1b4bc005c852e7919abc5eede23dd3a7b6f26015d11`  
		Last Modified: Thu, 15 Jan 2026 22:11:26 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7f0fe7586dc17cf8a7c98584015cc914819093423666de59fbdd09517f7018`  
		Last Modified: Thu, 15 Jan 2026 22:28:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da9049ed0141a54a80279b382c924b58ddfd2bdd4b30df9481610ecbb1ca834`  
		Last Modified: Thu, 15 Jan 2026 22:11:36 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aaec0e1cac56fdd17db6b0d9f73eafdf93fd7ecbc8a724f365da206621940c5`  
		Last Modified: Thu, 15 Jan 2026 22:11:28 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:72d6bc00b24890fcefc779de396dd7bf35973955caff366e6957e679fd5f6f34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66aeb9bbe2041bbf2c5fdaca3c3705af0cfc09ea38f7e9eeb469af9a7e3ee66b`

```dockerfile
```

-	Layers:
	-	`sha256:166252afa9942cdc70c9de156ab1064cca9eeee6a864d1fa47f76f812f2431b3`  
		Last Modified: Thu, 15 Jan 2026 22:11:26 GMT  
		Size: 26.3 KB (26258 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.12.3.21`

```console
$ docker pull clickhouse@sha256:9c348b2bd082bf71b8401397bb79f75e6698f3de0f1552f2742dab4e6909377e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.12.3.21` - linux; amd64

```console
$ docker pull clickhouse@sha256:e87ff5cc4db0ee4bd74404347ba9caa3e3ab5ef325db02aa1ba773f0f823ea81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246322771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852801b390c937417eee197f95cae6c5575ef31f3bc676501e5733f2732fa92a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:45 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:10:45 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:10:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:10:45 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:10:45 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:10:45 GMT
ARG VERSION=25.12.3.21
# Thu, 15 Jan 2026 22:10:45 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:15 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:15 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:15 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:16 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:16 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:16 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83cb5d9b0d9196f8fbe14025ad18475a55f20d4a27d7ec251d3790d05808e146`  
		Last Modified: Thu, 15 Jan 2026 22:11:49 GMT  
		Size: 7.6 MB (7598550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab75fa925b2df2acd4af08b5acff65f28cd8bdfeb13b687340aaa11fc602623`  
		Last Modified: Thu, 15 Jan 2026 22:52:15 GMT  
		Size: 208.3 MB (208317501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed06808047e10a168d67bf3d37fd53b16619284a18291d24e0e035551b64bba3`  
		Last Modified: Thu, 15 Jan 2026 22:11:37 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88194bfab547d36d32697803376d16fa6f50a5706e11835d6b2e5149249e3fd4`  
		Last Modified: Thu, 15 Jan 2026 22:11:38 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9694b94933bd348b79a326e9e90b99c980c93497916c9afea0517e9e59510dbd`  
		Last Modified: Thu, 15 Jan 2026 22:11:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c40bd2e7d92e7c7db010275427785be0871517f608b23e3062d094e4f11009`  
		Last Modified: Thu, 15 Jan 2026 22:11:39 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05fca4bd1478ce07af6e595b1ea1c177d3fcfc6fbf9844a850a0e6fc306fd03`  
		Last Modified: Thu, 15 Jan 2026 22:11:42 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.3.21` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8deb39a713f008acdec3251678de02eb74fdfffabbb7e17040b103fd78983a21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73dda45360c6471ea6f661c4f5ae30a7ffc26ae55624a1ad6d5cac45ff451818`

```dockerfile
```

-	Layers:
	-	`sha256:ed29f8b17477a4026a6b1c15b5babe8cec498591f0abd7fc02b73306b0839930`  
		Last Modified: Thu, 15 Jan 2026 22:50:48 GMT  
		Size: 26.0 KB (26047 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.12.3.21` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:30190af3158d8b3b3a48f60bdabfc40f26b446d16f28529014262d88e5dd2b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228224093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b161afcc2f6dd175ca36bc983f0bb75365d90b91db4bfcbc023a9c93ed07e9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:34 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:10:34 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:10:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:10:34 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:10:34 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:10:34 GMT
ARG VERSION=25.12.3.21
# Thu, 15 Jan 2026 22:10:34 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:04 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:04 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3df312c201c41d963c5bdc407650a174e7712d5b8aff75c83b0c6e2755b1208`  
		Last Modified: Thu, 15 Jan 2026 22:11:26 GMT  
		Size: 7.6 MB (7576689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bb9a92d4b2fd9436589e7c5649592d95edac119b4ab6a8460c0700e67ffa37`  
		Last Modified: Thu, 15 Jan 2026 22:11:29 GMT  
		Size: 192.4 MB (192393858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ccbc4119e8834350abf692cba0442fb6e8b1ae37944efd9240f68e493868a07`  
		Last Modified: Thu, 15 Jan 2026 22:11:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5438f0c9f26c70a44ea1b4bc005c852e7919abc5eede23dd3a7b6f26015d11`  
		Last Modified: Thu, 15 Jan 2026 22:11:26 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7f0fe7586dc17cf8a7c98584015cc914819093423666de59fbdd09517f7018`  
		Last Modified: Thu, 15 Jan 2026 22:28:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da9049ed0141a54a80279b382c924b58ddfd2bdd4b30df9481610ecbb1ca834`  
		Last Modified: Thu, 15 Jan 2026 22:11:36 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aaec0e1cac56fdd17db6b0d9f73eafdf93fd7ecbc8a724f365da206621940c5`  
		Last Modified: Thu, 15 Jan 2026 22:11:28 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.3.21` - unknown; unknown

```console
$ docker pull clickhouse@sha256:72d6bc00b24890fcefc779de396dd7bf35973955caff366e6957e679fd5f6f34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66aeb9bbe2041bbf2c5fdaca3c3705af0cfc09ea38f7e9eeb469af9a7e3ee66b`

```dockerfile
```

-	Layers:
	-	`sha256:166252afa9942cdc70c9de156ab1064cca9eeee6a864d1fa47f76f812f2431b3`  
		Last Modified: Thu, 15 Jan 2026 22:11:26 GMT  
		Size: 26.3 KB (26258 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.12.3.21-jammy`

```console
$ docker pull clickhouse@sha256:9c348b2bd082bf71b8401397bb79f75e6698f3de0f1552f2742dab4e6909377e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.12.3.21-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:e87ff5cc4db0ee4bd74404347ba9caa3e3ab5ef325db02aa1ba773f0f823ea81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246322771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852801b390c937417eee197f95cae6c5575ef31f3bc676501e5733f2732fa92a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:45 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:10:45 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:10:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:10:45 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:10:45 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:10:45 GMT
ARG VERSION=25.12.3.21
# Thu, 15 Jan 2026 22:10:45 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:15 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:15 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:15 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:16 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:16 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:16 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83cb5d9b0d9196f8fbe14025ad18475a55f20d4a27d7ec251d3790d05808e146`  
		Last Modified: Thu, 15 Jan 2026 22:11:49 GMT  
		Size: 7.6 MB (7598550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab75fa925b2df2acd4af08b5acff65f28cd8bdfeb13b687340aaa11fc602623`  
		Last Modified: Thu, 15 Jan 2026 22:52:15 GMT  
		Size: 208.3 MB (208317501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed06808047e10a168d67bf3d37fd53b16619284a18291d24e0e035551b64bba3`  
		Last Modified: Thu, 15 Jan 2026 22:11:37 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88194bfab547d36d32697803376d16fa6f50a5706e11835d6b2e5149249e3fd4`  
		Last Modified: Thu, 15 Jan 2026 22:11:38 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9694b94933bd348b79a326e9e90b99c980c93497916c9afea0517e9e59510dbd`  
		Last Modified: Thu, 15 Jan 2026 22:11:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c40bd2e7d92e7c7db010275427785be0871517f608b23e3062d094e4f11009`  
		Last Modified: Thu, 15 Jan 2026 22:11:39 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05fca4bd1478ce07af6e595b1ea1c177d3fcfc6fbf9844a850a0e6fc306fd03`  
		Last Modified: Thu, 15 Jan 2026 22:11:42 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.3.21-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8deb39a713f008acdec3251678de02eb74fdfffabbb7e17040b103fd78983a21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73dda45360c6471ea6f661c4f5ae30a7ffc26ae55624a1ad6d5cac45ff451818`

```dockerfile
```

-	Layers:
	-	`sha256:ed29f8b17477a4026a6b1c15b5babe8cec498591f0abd7fc02b73306b0839930`  
		Last Modified: Thu, 15 Jan 2026 22:50:48 GMT  
		Size: 26.0 KB (26047 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.12.3.21-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:30190af3158d8b3b3a48f60bdabfc40f26b446d16f28529014262d88e5dd2b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228224093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b161afcc2f6dd175ca36bc983f0bb75365d90b91db4bfcbc023a9c93ed07e9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:34 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:10:34 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:10:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:10:34 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:10:34 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:10:34 GMT
ARG VERSION=25.12.3.21
# Thu, 15 Jan 2026 22:10:34 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:04 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:04 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3df312c201c41d963c5bdc407650a174e7712d5b8aff75c83b0c6e2755b1208`  
		Last Modified: Thu, 15 Jan 2026 22:11:26 GMT  
		Size: 7.6 MB (7576689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bb9a92d4b2fd9436589e7c5649592d95edac119b4ab6a8460c0700e67ffa37`  
		Last Modified: Thu, 15 Jan 2026 22:11:29 GMT  
		Size: 192.4 MB (192393858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ccbc4119e8834350abf692cba0442fb6e8b1ae37944efd9240f68e493868a07`  
		Last Modified: Thu, 15 Jan 2026 22:11:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5438f0c9f26c70a44ea1b4bc005c852e7919abc5eede23dd3a7b6f26015d11`  
		Last Modified: Thu, 15 Jan 2026 22:11:26 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7f0fe7586dc17cf8a7c98584015cc914819093423666de59fbdd09517f7018`  
		Last Modified: Thu, 15 Jan 2026 22:28:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da9049ed0141a54a80279b382c924b58ddfd2bdd4b30df9481610ecbb1ca834`  
		Last Modified: Thu, 15 Jan 2026 22:11:36 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aaec0e1cac56fdd17db6b0d9f73eafdf93fd7ecbc8a724f365da206621940c5`  
		Last Modified: Thu, 15 Jan 2026 22:11:28 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.3.21-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:72d6bc00b24890fcefc779de396dd7bf35973955caff366e6957e679fd5f6f34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66aeb9bbe2041bbf2c5fdaca3c3705af0cfc09ea38f7e9eeb469af9a7e3ee66b`

```dockerfile
```

-	Layers:
	-	`sha256:166252afa9942cdc70c9de156ab1064cca9eeee6a864d1fa47f76f812f2431b3`  
		Last Modified: Thu, 15 Jan 2026 22:11:26 GMT  
		Size: 26.3 KB (26258 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3`

```console
$ docker pull clickhouse@sha256:a574ad6b0b18c31c0aa4909d53e5c800dac8b7e2bad7d69ff793739e254094f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:1efdcef132d1f724415c04fcba729eacb5bb51c724ee7e3137e5eb68b4d9a188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206311712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2770432550fe4dcd6aabc4d0897ad28a763ee9c988b0ba2d334eaaf0c7c3ca`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:11:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:11:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:11:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:11:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:11:04 GMT
ARG VERSION=25.3.12.8
# Thu, 15 Jan 2026 22:11:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:35 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:35 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:35 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:35 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:35 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:35 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c60245cd567fe38ecb66f864fedf11b7b73e8137e54dab5cbbc37520211fb17`  
		Last Modified: Thu, 15 Jan 2026 22:12:04 GMT  
		Size: 7.2 MB (7151747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2dbd93ad11b640a2ae6bca9a6bf2847d6e81c34e0bde9bec71fe0d42eae7e92`  
		Last Modified: Thu, 15 Jan 2026 22:11:57 GMT  
		Size: 168.8 MB (168753057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f857a0eb0acfbaab0f33771d2634dad02ce3f7d5806307aa8a90c5067d31be65`  
		Last Modified: Thu, 15 Jan 2026 22:11:53 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14de14d6278befda78d6625d6d87e962fdcd83c3b63a0574e0614c4ab70941bb`  
		Last Modified: Thu, 15 Jan 2026 22:12:04 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a435df05db1d0cfc47f660a6b47258bd86797236e0d55f14dbad7432cd26d7f`  
		Last Modified: Thu, 15 Jan 2026 22:11:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ebd9662282ce5aa6186d5bbcec1b12e34b40cd5d578a7b713cee35037a38d3`  
		Last Modified: Thu, 15 Jan 2026 22:11:55 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e119f653fd51b67f1c5dac43c8e608b88fd1e1e6e842315c608a3c92e93d37`  
		Last Modified: Thu, 15 Jan 2026 22:12:06 GMT  
		Size: 3.8 KB (3831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:08cb3e01087209916b8ab647ec3de34558c51e6d8ec073dbf79cbec6ec1b167c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ee30ad9d4b53c7dff5f53e1aa997fa2f1879e809ae5a860ce0d995abd95d3d`

```dockerfile
```

-	Layers:
	-	`sha256:f45b511eaadbd492fe5d812e7f6fde50739f431e7b6050012da20f21fde6b91c`  
		Last Modified: Thu, 15 Jan 2026 22:51:06 GMT  
		Size: 25.2 KB (25224 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:5f5c2b562ec4c76ab2a17fc65935ae85cab877e13662db4a033e5dd5b5485443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193787940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c692e26abe18a2d083b71fae51b141711775df388a8db3dedddde787254a452`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:11:19 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:11:19 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:11:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:11:19 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:11:19 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:11:19 GMT
ARG VERSION=25.3.12.8
# Thu, 15 Jan 2026 22:11:19 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:47 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:47 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:47 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1557193fc59b224a71057a138d93e110901f9c757256a8820b8df754fa580a73`  
		Last Modified: Thu, 15 Jan 2026 22:12:13 GMT  
		Size: 7.1 MB (7127206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6172235b917dbd2521b63ef97099190547db23f3cd7c79e7da5c71284ed9e0d`  
		Last Modified: Thu, 15 Jan 2026 22:12:07 GMT  
		Size: 158.4 MB (158406987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb488937be61ffe4ccd5545af47450e4a37c4e2d863a5e105253270d726a1af8`  
		Last Modified: Thu, 15 Jan 2026 22:12:03 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4882f3bebb796783656df7adce4108253ddde7523b4b22d6f8377d5584e15da8`  
		Last Modified: Thu, 15 Jan 2026 22:12:04 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae4b6c185d934cffdc8303b7a0971a113c359329aa1a39942f204e8de16bfb5`  
		Last Modified: Thu, 15 Jan 2026 22:12:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff3f187f8ad4ccc172afede208182e6c01c4d1379294c0177da9f1f906f3508`  
		Last Modified: Thu, 15 Jan 2026 22:12:05 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3797727e93a6d098e923f8e9b1e62c9e4d625bc668e942b539abfa8f8e34595d`  
		Last Modified: Thu, 15 Jan 2026 22:12:13 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:bf2bf261870df0edda083d3831694ccb664b9cb600854ead1970ee266013cc08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08eb210af1576173c939267162b0bedf0715b2a5243d9b08c58abfc02c19a3a5`

```dockerfile
```

-	Layers:
	-	`sha256:66b9ef8dd19a91807b8570a41ee1e451fe191b757eb2e0ad615cec8f783d3399`  
		Last Modified: Thu, 15 Jan 2026 22:12:03 GMT  
		Size: 25.4 KB (25412 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3-jammy`

```console
$ docker pull clickhouse@sha256:a574ad6b0b18c31c0aa4909d53e5c800dac8b7e2bad7d69ff793739e254094f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:1efdcef132d1f724415c04fcba729eacb5bb51c724ee7e3137e5eb68b4d9a188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206311712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2770432550fe4dcd6aabc4d0897ad28a763ee9c988b0ba2d334eaaf0c7c3ca`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:11:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:11:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:11:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:11:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:11:04 GMT
ARG VERSION=25.3.12.8
# Thu, 15 Jan 2026 22:11:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:35 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:35 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:35 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:35 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:35 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:35 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c60245cd567fe38ecb66f864fedf11b7b73e8137e54dab5cbbc37520211fb17`  
		Last Modified: Thu, 15 Jan 2026 22:12:04 GMT  
		Size: 7.2 MB (7151747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2dbd93ad11b640a2ae6bca9a6bf2847d6e81c34e0bde9bec71fe0d42eae7e92`  
		Last Modified: Thu, 15 Jan 2026 22:11:57 GMT  
		Size: 168.8 MB (168753057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f857a0eb0acfbaab0f33771d2634dad02ce3f7d5806307aa8a90c5067d31be65`  
		Last Modified: Thu, 15 Jan 2026 22:11:53 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14de14d6278befda78d6625d6d87e962fdcd83c3b63a0574e0614c4ab70941bb`  
		Last Modified: Thu, 15 Jan 2026 22:12:04 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a435df05db1d0cfc47f660a6b47258bd86797236e0d55f14dbad7432cd26d7f`  
		Last Modified: Thu, 15 Jan 2026 22:11:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ebd9662282ce5aa6186d5bbcec1b12e34b40cd5d578a7b713cee35037a38d3`  
		Last Modified: Thu, 15 Jan 2026 22:11:55 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e119f653fd51b67f1c5dac43c8e608b88fd1e1e6e842315c608a3c92e93d37`  
		Last Modified: Thu, 15 Jan 2026 22:12:06 GMT  
		Size: 3.8 KB (3831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:08cb3e01087209916b8ab647ec3de34558c51e6d8ec073dbf79cbec6ec1b167c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ee30ad9d4b53c7dff5f53e1aa997fa2f1879e809ae5a860ce0d995abd95d3d`

```dockerfile
```

-	Layers:
	-	`sha256:f45b511eaadbd492fe5d812e7f6fde50739f431e7b6050012da20f21fde6b91c`  
		Last Modified: Thu, 15 Jan 2026 22:51:06 GMT  
		Size: 25.2 KB (25224 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:5f5c2b562ec4c76ab2a17fc65935ae85cab877e13662db4a033e5dd5b5485443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193787940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c692e26abe18a2d083b71fae51b141711775df388a8db3dedddde787254a452`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:11:19 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:11:19 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:11:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:11:19 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:11:19 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:11:19 GMT
ARG VERSION=25.3.12.8
# Thu, 15 Jan 2026 22:11:19 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:47 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:47 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:47 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1557193fc59b224a71057a138d93e110901f9c757256a8820b8df754fa580a73`  
		Last Modified: Thu, 15 Jan 2026 22:12:13 GMT  
		Size: 7.1 MB (7127206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6172235b917dbd2521b63ef97099190547db23f3cd7c79e7da5c71284ed9e0d`  
		Last Modified: Thu, 15 Jan 2026 22:12:07 GMT  
		Size: 158.4 MB (158406987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb488937be61ffe4ccd5545af47450e4a37c4e2d863a5e105253270d726a1af8`  
		Last Modified: Thu, 15 Jan 2026 22:12:03 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4882f3bebb796783656df7adce4108253ddde7523b4b22d6f8377d5584e15da8`  
		Last Modified: Thu, 15 Jan 2026 22:12:04 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae4b6c185d934cffdc8303b7a0971a113c359329aa1a39942f204e8de16bfb5`  
		Last Modified: Thu, 15 Jan 2026 22:12:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff3f187f8ad4ccc172afede208182e6c01c4d1379294c0177da9f1f906f3508`  
		Last Modified: Thu, 15 Jan 2026 22:12:05 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3797727e93a6d098e923f8e9b1e62c9e4d625bc668e942b539abfa8f8e34595d`  
		Last Modified: Thu, 15 Jan 2026 22:12:13 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:bf2bf261870df0edda083d3831694ccb664b9cb600854ead1970ee266013cc08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08eb210af1576173c939267162b0bedf0715b2a5243d9b08c58abfc02c19a3a5`

```dockerfile
```

-	Layers:
	-	`sha256:66b9ef8dd19a91807b8570a41ee1e451fe191b757eb2e0ad615cec8f783d3399`  
		Last Modified: Thu, 15 Jan 2026 22:12:03 GMT  
		Size: 25.4 KB (25412 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.12`

```console
$ docker pull clickhouse@sha256:a574ad6b0b18c31c0aa4909d53e5c800dac8b7e2bad7d69ff793739e254094f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.12` - linux; amd64

```console
$ docker pull clickhouse@sha256:1efdcef132d1f724415c04fcba729eacb5bb51c724ee7e3137e5eb68b4d9a188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206311712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2770432550fe4dcd6aabc4d0897ad28a763ee9c988b0ba2d334eaaf0c7c3ca`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:11:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:11:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:11:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:11:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:11:04 GMT
ARG VERSION=25.3.12.8
# Thu, 15 Jan 2026 22:11:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:35 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:35 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:35 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:35 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:35 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:35 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c60245cd567fe38ecb66f864fedf11b7b73e8137e54dab5cbbc37520211fb17`  
		Last Modified: Thu, 15 Jan 2026 22:12:04 GMT  
		Size: 7.2 MB (7151747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2dbd93ad11b640a2ae6bca9a6bf2847d6e81c34e0bde9bec71fe0d42eae7e92`  
		Last Modified: Thu, 15 Jan 2026 22:11:57 GMT  
		Size: 168.8 MB (168753057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f857a0eb0acfbaab0f33771d2634dad02ce3f7d5806307aa8a90c5067d31be65`  
		Last Modified: Thu, 15 Jan 2026 22:11:53 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14de14d6278befda78d6625d6d87e962fdcd83c3b63a0574e0614c4ab70941bb`  
		Last Modified: Thu, 15 Jan 2026 22:12:04 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a435df05db1d0cfc47f660a6b47258bd86797236e0d55f14dbad7432cd26d7f`  
		Last Modified: Thu, 15 Jan 2026 22:11:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ebd9662282ce5aa6186d5bbcec1b12e34b40cd5d578a7b713cee35037a38d3`  
		Last Modified: Thu, 15 Jan 2026 22:11:55 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e119f653fd51b67f1c5dac43c8e608b88fd1e1e6e842315c608a3c92e93d37`  
		Last Modified: Thu, 15 Jan 2026 22:12:06 GMT  
		Size: 3.8 KB (3831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.12` - unknown; unknown

```console
$ docker pull clickhouse@sha256:08cb3e01087209916b8ab647ec3de34558c51e6d8ec073dbf79cbec6ec1b167c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ee30ad9d4b53c7dff5f53e1aa997fa2f1879e809ae5a860ce0d995abd95d3d`

```dockerfile
```

-	Layers:
	-	`sha256:f45b511eaadbd492fe5d812e7f6fde50739f431e7b6050012da20f21fde6b91c`  
		Last Modified: Thu, 15 Jan 2026 22:51:06 GMT  
		Size: 25.2 KB (25224 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.12` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:5f5c2b562ec4c76ab2a17fc65935ae85cab877e13662db4a033e5dd5b5485443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193787940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c692e26abe18a2d083b71fae51b141711775df388a8db3dedddde787254a452`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:11:19 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:11:19 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:11:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:11:19 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:11:19 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:11:19 GMT
ARG VERSION=25.3.12.8
# Thu, 15 Jan 2026 22:11:19 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:47 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:47 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:47 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1557193fc59b224a71057a138d93e110901f9c757256a8820b8df754fa580a73`  
		Last Modified: Thu, 15 Jan 2026 22:12:13 GMT  
		Size: 7.1 MB (7127206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6172235b917dbd2521b63ef97099190547db23f3cd7c79e7da5c71284ed9e0d`  
		Last Modified: Thu, 15 Jan 2026 22:12:07 GMT  
		Size: 158.4 MB (158406987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb488937be61ffe4ccd5545af47450e4a37c4e2d863a5e105253270d726a1af8`  
		Last Modified: Thu, 15 Jan 2026 22:12:03 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4882f3bebb796783656df7adce4108253ddde7523b4b22d6f8377d5584e15da8`  
		Last Modified: Thu, 15 Jan 2026 22:12:04 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae4b6c185d934cffdc8303b7a0971a113c359329aa1a39942f204e8de16bfb5`  
		Last Modified: Thu, 15 Jan 2026 22:12:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff3f187f8ad4ccc172afede208182e6c01c4d1379294c0177da9f1f906f3508`  
		Last Modified: Thu, 15 Jan 2026 22:12:05 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3797727e93a6d098e923f8e9b1e62c9e4d625bc668e942b539abfa8f8e34595d`  
		Last Modified: Thu, 15 Jan 2026 22:12:13 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.12` - unknown; unknown

```console
$ docker pull clickhouse@sha256:bf2bf261870df0edda083d3831694ccb664b9cb600854ead1970ee266013cc08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08eb210af1576173c939267162b0bedf0715b2a5243d9b08c58abfc02c19a3a5`

```dockerfile
```

-	Layers:
	-	`sha256:66b9ef8dd19a91807b8570a41ee1e451fe191b757eb2e0ad615cec8f783d3399`  
		Last Modified: Thu, 15 Jan 2026 22:12:03 GMT  
		Size: 25.4 KB (25412 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.12-jammy`

```console
$ docker pull clickhouse@sha256:a574ad6b0b18c31c0aa4909d53e5c800dac8b7e2bad7d69ff793739e254094f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.12-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:1efdcef132d1f724415c04fcba729eacb5bb51c724ee7e3137e5eb68b4d9a188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206311712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2770432550fe4dcd6aabc4d0897ad28a763ee9c988b0ba2d334eaaf0c7c3ca`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:11:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:11:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:11:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:11:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:11:04 GMT
ARG VERSION=25.3.12.8
# Thu, 15 Jan 2026 22:11:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:35 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:35 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:35 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:35 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:35 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:35 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c60245cd567fe38ecb66f864fedf11b7b73e8137e54dab5cbbc37520211fb17`  
		Last Modified: Thu, 15 Jan 2026 22:12:04 GMT  
		Size: 7.2 MB (7151747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2dbd93ad11b640a2ae6bca9a6bf2847d6e81c34e0bde9bec71fe0d42eae7e92`  
		Last Modified: Thu, 15 Jan 2026 22:11:57 GMT  
		Size: 168.8 MB (168753057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f857a0eb0acfbaab0f33771d2634dad02ce3f7d5806307aa8a90c5067d31be65`  
		Last Modified: Thu, 15 Jan 2026 22:11:53 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14de14d6278befda78d6625d6d87e962fdcd83c3b63a0574e0614c4ab70941bb`  
		Last Modified: Thu, 15 Jan 2026 22:12:04 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a435df05db1d0cfc47f660a6b47258bd86797236e0d55f14dbad7432cd26d7f`  
		Last Modified: Thu, 15 Jan 2026 22:11:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ebd9662282ce5aa6186d5bbcec1b12e34b40cd5d578a7b713cee35037a38d3`  
		Last Modified: Thu, 15 Jan 2026 22:11:55 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e119f653fd51b67f1c5dac43c8e608b88fd1e1e6e842315c608a3c92e93d37`  
		Last Modified: Thu, 15 Jan 2026 22:12:06 GMT  
		Size: 3.8 KB (3831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.12-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:08cb3e01087209916b8ab647ec3de34558c51e6d8ec073dbf79cbec6ec1b167c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ee30ad9d4b53c7dff5f53e1aa997fa2f1879e809ae5a860ce0d995abd95d3d`

```dockerfile
```

-	Layers:
	-	`sha256:f45b511eaadbd492fe5d812e7f6fde50739f431e7b6050012da20f21fde6b91c`  
		Last Modified: Thu, 15 Jan 2026 22:51:06 GMT  
		Size: 25.2 KB (25224 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.12-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:5f5c2b562ec4c76ab2a17fc65935ae85cab877e13662db4a033e5dd5b5485443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193787940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c692e26abe18a2d083b71fae51b141711775df388a8db3dedddde787254a452`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:11:19 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:11:19 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:11:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:11:19 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:11:19 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:11:19 GMT
ARG VERSION=25.3.12.8
# Thu, 15 Jan 2026 22:11:19 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:47 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:47 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:47 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1557193fc59b224a71057a138d93e110901f9c757256a8820b8df754fa580a73`  
		Last Modified: Thu, 15 Jan 2026 22:12:13 GMT  
		Size: 7.1 MB (7127206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6172235b917dbd2521b63ef97099190547db23f3cd7c79e7da5c71284ed9e0d`  
		Last Modified: Thu, 15 Jan 2026 22:12:07 GMT  
		Size: 158.4 MB (158406987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb488937be61ffe4ccd5545af47450e4a37c4e2d863a5e105253270d726a1af8`  
		Last Modified: Thu, 15 Jan 2026 22:12:03 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4882f3bebb796783656df7adce4108253ddde7523b4b22d6f8377d5584e15da8`  
		Last Modified: Thu, 15 Jan 2026 22:12:04 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae4b6c185d934cffdc8303b7a0971a113c359329aa1a39942f204e8de16bfb5`  
		Last Modified: Thu, 15 Jan 2026 22:12:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff3f187f8ad4ccc172afede208182e6c01c4d1379294c0177da9f1f906f3508`  
		Last Modified: Thu, 15 Jan 2026 22:12:05 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3797727e93a6d098e923f8e9b1e62c9e4d625bc668e942b539abfa8f8e34595d`  
		Last Modified: Thu, 15 Jan 2026 22:12:13 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.12-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:bf2bf261870df0edda083d3831694ccb664b9cb600854ead1970ee266013cc08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08eb210af1576173c939267162b0bedf0715b2a5243d9b08c58abfc02c19a3a5`

```dockerfile
```

-	Layers:
	-	`sha256:66b9ef8dd19a91807b8570a41ee1e451fe191b757eb2e0ad615cec8f783d3399`  
		Last Modified: Thu, 15 Jan 2026 22:12:03 GMT  
		Size: 25.4 KB (25412 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.12.8`

```console
$ docker pull clickhouse@sha256:a574ad6b0b18c31c0aa4909d53e5c800dac8b7e2bad7d69ff793739e254094f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.12.8` - linux; amd64

```console
$ docker pull clickhouse@sha256:1efdcef132d1f724415c04fcba729eacb5bb51c724ee7e3137e5eb68b4d9a188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206311712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2770432550fe4dcd6aabc4d0897ad28a763ee9c988b0ba2d334eaaf0c7c3ca`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:11:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:11:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:11:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:11:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:11:04 GMT
ARG VERSION=25.3.12.8
# Thu, 15 Jan 2026 22:11:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:35 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:35 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:35 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:35 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:35 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:35 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c60245cd567fe38ecb66f864fedf11b7b73e8137e54dab5cbbc37520211fb17`  
		Last Modified: Thu, 15 Jan 2026 22:12:04 GMT  
		Size: 7.2 MB (7151747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2dbd93ad11b640a2ae6bca9a6bf2847d6e81c34e0bde9bec71fe0d42eae7e92`  
		Last Modified: Thu, 15 Jan 2026 22:11:57 GMT  
		Size: 168.8 MB (168753057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f857a0eb0acfbaab0f33771d2634dad02ce3f7d5806307aa8a90c5067d31be65`  
		Last Modified: Thu, 15 Jan 2026 22:11:53 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14de14d6278befda78d6625d6d87e962fdcd83c3b63a0574e0614c4ab70941bb`  
		Last Modified: Thu, 15 Jan 2026 22:12:04 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a435df05db1d0cfc47f660a6b47258bd86797236e0d55f14dbad7432cd26d7f`  
		Last Modified: Thu, 15 Jan 2026 22:11:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ebd9662282ce5aa6186d5bbcec1b12e34b40cd5d578a7b713cee35037a38d3`  
		Last Modified: Thu, 15 Jan 2026 22:11:55 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e119f653fd51b67f1c5dac43c8e608b88fd1e1e6e842315c608a3c92e93d37`  
		Last Modified: Thu, 15 Jan 2026 22:12:06 GMT  
		Size: 3.8 KB (3831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.12.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:08cb3e01087209916b8ab647ec3de34558c51e6d8ec073dbf79cbec6ec1b167c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ee30ad9d4b53c7dff5f53e1aa997fa2f1879e809ae5a860ce0d995abd95d3d`

```dockerfile
```

-	Layers:
	-	`sha256:f45b511eaadbd492fe5d812e7f6fde50739f431e7b6050012da20f21fde6b91c`  
		Last Modified: Thu, 15 Jan 2026 22:51:06 GMT  
		Size: 25.2 KB (25224 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.12.8` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:5f5c2b562ec4c76ab2a17fc65935ae85cab877e13662db4a033e5dd5b5485443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193787940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c692e26abe18a2d083b71fae51b141711775df388a8db3dedddde787254a452`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:11:19 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:11:19 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:11:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:11:19 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:11:19 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:11:19 GMT
ARG VERSION=25.3.12.8
# Thu, 15 Jan 2026 22:11:19 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:47 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:47 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:47 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1557193fc59b224a71057a138d93e110901f9c757256a8820b8df754fa580a73`  
		Last Modified: Thu, 15 Jan 2026 22:12:13 GMT  
		Size: 7.1 MB (7127206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6172235b917dbd2521b63ef97099190547db23f3cd7c79e7da5c71284ed9e0d`  
		Last Modified: Thu, 15 Jan 2026 22:12:07 GMT  
		Size: 158.4 MB (158406987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb488937be61ffe4ccd5545af47450e4a37c4e2d863a5e105253270d726a1af8`  
		Last Modified: Thu, 15 Jan 2026 22:12:03 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4882f3bebb796783656df7adce4108253ddde7523b4b22d6f8377d5584e15da8`  
		Last Modified: Thu, 15 Jan 2026 22:12:04 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae4b6c185d934cffdc8303b7a0971a113c359329aa1a39942f204e8de16bfb5`  
		Last Modified: Thu, 15 Jan 2026 22:12:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff3f187f8ad4ccc172afede208182e6c01c4d1379294c0177da9f1f906f3508`  
		Last Modified: Thu, 15 Jan 2026 22:12:05 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3797727e93a6d098e923f8e9b1e62c9e4d625bc668e942b539abfa8f8e34595d`  
		Last Modified: Thu, 15 Jan 2026 22:12:13 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.12.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:bf2bf261870df0edda083d3831694ccb664b9cb600854ead1970ee266013cc08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08eb210af1576173c939267162b0bedf0715b2a5243d9b08c58abfc02c19a3a5`

```dockerfile
```

-	Layers:
	-	`sha256:66b9ef8dd19a91807b8570a41ee1e451fe191b757eb2e0ad615cec8f783d3399`  
		Last Modified: Thu, 15 Jan 2026 22:12:03 GMT  
		Size: 25.4 KB (25412 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.12.8-jammy`

```console
$ docker pull clickhouse@sha256:a574ad6b0b18c31c0aa4909d53e5c800dac8b7e2bad7d69ff793739e254094f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.12.8-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:1efdcef132d1f724415c04fcba729eacb5bb51c724ee7e3137e5eb68b4d9a188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206311712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2770432550fe4dcd6aabc4d0897ad28a763ee9c988b0ba2d334eaaf0c7c3ca`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:11:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:11:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:11:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:11:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:11:04 GMT
ARG VERSION=25.3.12.8
# Thu, 15 Jan 2026 22:11:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:35 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:35 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:35 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:35 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:35 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:35 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c60245cd567fe38ecb66f864fedf11b7b73e8137e54dab5cbbc37520211fb17`  
		Last Modified: Thu, 15 Jan 2026 22:12:04 GMT  
		Size: 7.2 MB (7151747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2dbd93ad11b640a2ae6bca9a6bf2847d6e81c34e0bde9bec71fe0d42eae7e92`  
		Last Modified: Thu, 15 Jan 2026 22:11:57 GMT  
		Size: 168.8 MB (168753057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f857a0eb0acfbaab0f33771d2634dad02ce3f7d5806307aa8a90c5067d31be65`  
		Last Modified: Thu, 15 Jan 2026 22:11:53 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14de14d6278befda78d6625d6d87e962fdcd83c3b63a0574e0614c4ab70941bb`  
		Last Modified: Thu, 15 Jan 2026 22:12:04 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a435df05db1d0cfc47f660a6b47258bd86797236e0d55f14dbad7432cd26d7f`  
		Last Modified: Thu, 15 Jan 2026 22:11:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ebd9662282ce5aa6186d5bbcec1b12e34b40cd5d578a7b713cee35037a38d3`  
		Last Modified: Thu, 15 Jan 2026 22:11:55 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e119f653fd51b67f1c5dac43c8e608b88fd1e1e6e842315c608a3c92e93d37`  
		Last Modified: Thu, 15 Jan 2026 22:12:06 GMT  
		Size: 3.8 KB (3831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.12.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:08cb3e01087209916b8ab647ec3de34558c51e6d8ec073dbf79cbec6ec1b167c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ee30ad9d4b53c7dff5f53e1aa997fa2f1879e809ae5a860ce0d995abd95d3d`

```dockerfile
```

-	Layers:
	-	`sha256:f45b511eaadbd492fe5d812e7f6fde50739f431e7b6050012da20f21fde6b91c`  
		Last Modified: Thu, 15 Jan 2026 22:51:06 GMT  
		Size: 25.2 KB (25224 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.12.8-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:5f5c2b562ec4c76ab2a17fc65935ae85cab877e13662db4a033e5dd5b5485443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193787940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c692e26abe18a2d083b71fae51b141711775df388a8db3dedddde787254a452`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:11:19 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:11:19 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:11:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:11:19 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:11:19 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:11:19 GMT
ARG VERSION=25.3.12.8
# Thu, 15 Jan 2026 22:11:19 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:47 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:47 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:47 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1557193fc59b224a71057a138d93e110901f9c757256a8820b8df754fa580a73`  
		Last Modified: Thu, 15 Jan 2026 22:12:13 GMT  
		Size: 7.1 MB (7127206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6172235b917dbd2521b63ef97099190547db23f3cd7c79e7da5c71284ed9e0d`  
		Last Modified: Thu, 15 Jan 2026 22:12:07 GMT  
		Size: 158.4 MB (158406987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb488937be61ffe4ccd5545af47450e4a37c4e2d863a5e105253270d726a1af8`  
		Last Modified: Thu, 15 Jan 2026 22:12:03 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4882f3bebb796783656df7adce4108253ddde7523b4b22d6f8377d5584e15da8`  
		Last Modified: Thu, 15 Jan 2026 22:12:04 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae4b6c185d934cffdc8303b7a0971a113c359329aa1a39942f204e8de16bfb5`  
		Last Modified: Thu, 15 Jan 2026 22:12:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff3f187f8ad4ccc172afede208182e6c01c4d1379294c0177da9f1f906f3508`  
		Last Modified: Thu, 15 Jan 2026 22:12:05 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3797727e93a6d098e923f8e9b1e62c9e4d625bc668e942b539abfa8f8e34595d`  
		Last Modified: Thu, 15 Jan 2026 22:12:13 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.12.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:bf2bf261870df0edda083d3831694ccb664b9cb600854ead1970ee266013cc08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08eb210af1576173c939267162b0bedf0715b2a5243d9b08c58abfc02c19a3a5`

```dockerfile
```

-	Layers:
	-	`sha256:66b9ef8dd19a91807b8570a41ee1e451fe191b757eb2e0ad615cec8f783d3399`  
		Last Modified: Thu, 15 Jan 2026 22:12:03 GMT  
		Size: 25.4 KB (25412 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8`

```console
$ docker pull clickhouse@sha256:4bca955e2c69ac02266f3f49a875cd66f309fb3ccc047ef43142d99217cbcec5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8` - linux; amd64

```console
$ docker pull clickhouse@sha256:137c2814b0f9386acb01501cf8b8aee782cea88c67eaf7b0574a8ebd3a42a11c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228927881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:405c6aee9d117ca376bb20a9133443568308ccb1a427c57446a734a6b85dba7f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:11:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:11:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:11:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:11:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:11:04 GMT
ARG VERSION=25.8.14.17
# Thu, 15 Jan 2026 22:11:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:38 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:38 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ef9b857503b896202db7ec6ef5737188d91b89ab5cc14511bef40e8153ec33`  
		Last Modified: Thu, 15 Jan 2026 22:12:01 GMT  
		Size: 7.6 MB (7598572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7717e9dd1378290bdcd675fcf0bf16665dbd8f50fd27de108a0e8452e589ebc1`  
		Last Modified: Thu, 15 Jan 2026 22:12:04 GMT  
		Size: 190.9 MB (190922617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b378e4471da99ac876409cc2c5f4f9665b84b269f04e94d09dd8f13c7f938b`  
		Last Modified: Thu, 15 Jan 2026 22:12:11 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e3057aefd02678456881131f1425134307d5f38db9064c5647e37ded35840e`  
		Last Modified: Thu, 15 Jan 2026 22:12:00 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da24271c02ef1d51851e13c9180fe586b6499a684a5d0b762e793f67c7b348a`  
		Last Modified: Thu, 15 Jan 2026 22:12:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af0ff00bd76836cc516373a39fbe657144cb050655d1788129ccab203a20da1`  
		Last Modified: Thu, 15 Jan 2026 22:12:11 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb344d98f2089982fb2ceed745a809d9165351e7393aff31d18102de4587c4b`  
		Last Modified: Thu, 15 Jan 2026 22:12:11 GMT  
		Size: 3.6 KB (3609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2bbdafdc831d87bdae33f1ed22e11e834cac9924e6c04c0a75d621f38ea4e156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9141f11eb4c178adb3e2f395e698e843d228a644523ea02f223d637f065531b5`

```dockerfile
```

-	Layers:
	-	`sha256:f2322c19f09a252e05c2666313c5773ae0ec3e6e6bf9979ba3b80cfc0d891fb8`  
		Last Modified: Thu, 15 Jan 2026 22:51:25 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4745062273cd45217a1b1f92f587882d45bee1b698643a6a0d69eef03e6f0fc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213827477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5614231090cb07c25f883f615d8d387e4ad171fd0fea854a81d62a702e181f48`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:11:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:11:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:11:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:11:13 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:11:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:11:13 GMT
ARG VERSION=25.8.14.17
# Thu, 15 Jan 2026 22:11:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:39 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:39 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:40 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:40 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:40 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:40 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297714d85bd1bd0b198fca6dace9d682bdfb99e6e582716cc4a402ea5135fbbf`  
		Last Modified: Thu, 15 Jan 2026 22:12:08 GMT  
		Size: 7.6 MB (7576661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195a3a53e2e0eb5312aabf39c28c7bc006ed22839691070a10ac4e6f85b781a2`  
		Last Modified: Thu, 15 Jan 2026 22:52:05 GMT  
		Size: 178.0 MB (177997293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ae2aaba775f3813680fd84a18107bf25d1cbd69a62aca86efc63a87de10377`  
		Last Modified: Thu, 15 Jan 2026 22:12:07 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178625e79308f5b24a28acea16bfc338aa97911935ad1038cd260a830c4b21eb`  
		Last Modified: Thu, 15 Jan 2026 22:11:58 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696ec49e708558d4523f56fb769ab640f6d7876636d963e16ae9fd1fd6b3cdf8`  
		Last Modified: Thu, 15 Jan 2026 22:12:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0534458f051ddf2bdc3544ffd719e1dc98eb9543380c6886465d64fa25a60be0`  
		Last Modified: Thu, 15 Jan 2026 22:12:00 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a6c12a019e979f88d574e4305b919081b1e6f2700eced0a594cab9e9207ee3`  
		Last Modified: Thu, 15 Jan 2026 22:12:00 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b49ec4e7cacbb4063ef4b014c20533cc848fad443c3cbddbe2000e2beac58ab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46895b10a1450d21a3af70c5a280e46f4a205d3c43f89d780ddceab33d56520`

```dockerfile
```

-	Layers:
	-	`sha256:6d7fd1fc6025d9d3cdc3f1111b5502b5712170dd438f110ab07d697f387be06a`  
		Last Modified: Thu, 15 Jan 2026 22:51:29 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8-jammy`

```console
$ docker pull clickhouse@sha256:4bca955e2c69ac02266f3f49a875cd66f309fb3ccc047ef43142d99217cbcec5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:137c2814b0f9386acb01501cf8b8aee782cea88c67eaf7b0574a8ebd3a42a11c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228927881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:405c6aee9d117ca376bb20a9133443568308ccb1a427c57446a734a6b85dba7f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:11:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:11:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:11:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:11:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:11:04 GMT
ARG VERSION=25.8.14.17
# Thu, 15 Jan 2026 22:11:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:38 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:38 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ef9b857503b896202db7ec6ef5737188d91b89ab5cc14511bef40e8153ec33`  
		Last Modified: Thu, 15 Jan 2026 22:12:01 GMT  
		Size: 7.6 MB (7598572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7717e9dd1378290bdcd675fcf0bf16665dbd8f50fd27de108a0e8452e589ebc1`  
		Last Modified: Thu, 15 Jan 2026 22:12:04 GMT  
		Size: 190.9 MB (190922617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b378e4471da99ac876409cc2c5f4f9665b84b269f04e94d09dd8f13c7f938b`  
		Last Modified: Thu, 15 Jan 2026 22:12:11 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e3057aefd02678456881131f1425134307d5f38db9064c5647e37ded35840e`  
		Last Modified: Thu, 15 Jan 2026 22:12:00 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da24271c02ef1d51851e13c9180fe586b6499a684a5d0b762e793f67c7b348a`  
		Last Modified: Thu, 15 Jan 2026 22:12:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af0ff00bd76836cc516373a39fbe657144cb050655d1788129ccab203a20da1`  
		Last Modified: Thu, 15 Jan 2026 22:12:11 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb344d98f2089982fb2ceed745a809d9165351e7393aff31d18102de4587c4b`  
		Last Modified: Thu, 15 Jan 2026 22:12:11 GMT  
		Size: 3.6 KB (3609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2bbdafdc831d87bdae33f1ed22e11e834cac9924e6c04c0a75d621f38ea4e156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9141f11eb4c178adb3e2f395e698e843d228a644523ea02f223d637f065531b5`

```dockerfile
```

-	Layers:
	-	`sha256:f2322c19f09a252e05c2666313c5773ae0ec3e6e6bf9979ba3b80cfc0d891fb8`  
		Last Modified: Thu, 15 Jan 2026 22:51:25 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4745062273cd45217a1b1f92f587882d45bee1b698643a6a0d69eef03e6f0fc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213827477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5614231090cb07c25f883f615d8d387e4ad171fd0fea854a81d62a702e181f48`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:11:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:11:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:11:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:11:13 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:11:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:11:13 GMT
ARG VERSION=25.8.14.17
# Thu, 15 Jan 2026 22:11:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:39 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:39 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:40 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:40 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:40 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:40 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297714d85bd1bd0b198fca6dace9d682bdfb99e6e582716cc4a402ea5135fbbf`  
		Last Modified: Thu, 15 Jan 2026 22:12:08 GMT  
		Size: 7.6 MB (7576661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195a3a53e2e0eb5312aabf39c28c7bc006ed22839691070a10ac4e6f85b781a2`  
		Last Modified: Thu, 15 Jan 2026 22:52:05 GMT  
		Size: 178.0 MB (177997293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ae2aaba775f3813680fd84a18107bf25d1cbd69a62aca86efc63a87de10377`  
		Last Modified: Thu, 15 Jan 2026 22:12:07 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178625e79308f5b24a28acea16bfc338aa97911935ad1038cd260a830c4b21eb`  
		Last Modified: Thu, 15 Jan 2026 22:11:58 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696ec49e708558d4523f56fb769ab640f6d7876636d963e16ae9fd1fd6b3cdf8`  
		Last Modified: Thu, 15 Jan 2026 22:12:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0534458f051ddf2bdc3544ffd719e1dc98eb9543380c6886465d64fa25a60be0`  
		Last Modified: Thu, 15 Jan 2026 22:12:00 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a6c12a019e979f88d574e4305b919081b1e6f2700eced0a594cab9e9207ee3`  
		Last Modified: Thu, 15 Jan 2026 22:12:00 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b49ec4e7cacbb4063ef4b014c20533cc848fad443c3cbddbe2000e2beac58ab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46895b10a1450d21a3af70c5a280e46f4a205d3c43f89d780ddceab33d56520`

```dockerfile
```

-	Layers:
	-	`sha256:6d7fd1fc6025d9d3cdc3f1111b5502b5712170dd438f110ab07d697f387be06a`  
		Last Modified: Thu, 15 Jan 2026 22:51:29 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.14`

```console
$ docker pull clickhouse@sha256:4bca955e2c69ac02266f3f49a875cd66f309fb3ccc047ef43142d99217cbcec5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.14` - linux; amd64

```console
$ docker pull clickhouse@sha256:137c2814b0f9386acb01501cf8b8aee782cea88c67eaf7b0574a8ebd3a42a11c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228927881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:405c6aee9d117ca376bb20a9133443568308ccb1a427c57446a734a6b85dba7f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:11:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:11:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:11:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:11:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:11:04 GMT
ARG VERSION=25.8.14.17
# Thu, 15 Jan 2026 22:11:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:38 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:38 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ef9b857503b896202db7ec6ef5737188d91b89ab5cc14511bef40e8153ec33`  
		Last Modified: Thu, 15 Jan 2026 22:12:01 GMT  
		Size: 7.6 MB (7598572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7717e9dd1378290bdcd675fcf0bf16665dbd8f50fd27de108a0e8452e589ebc1`  
		Last Modified: Thu, 15 Jan 2026 22:12:04 GMT  
		Size: 190.9 MB (190922617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b378e4471da99ac876409cc2c5f4f9665b84b269f04e94d09dd8f13c7f938b`  
		Last Modified: Thu, 15 Jan 2026 22:12:11 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e3057aefd02678456881131f1425134307d5f38db9064c5647e37ded35840e`  
		Last Modified: Thu, 15 Jan 2026 22:12:00 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da24271c02ef1d51851e13c9180fe586b6499a684a5d0b762e793f67c7b348a`  
		Last Modified: Thu, 15 Jan 2026 22:12:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af0ff00bd76836cc516373a39fbe657144cb050655d1788129ccab203a20da1`  
		Last Modified: Thu, 15 Jan 2026 22:12:11 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb344d98f2089982fb2ceed745a809d9165351e7393aff31d18102de4587c4b`  
		Last Modified: Thu, 15 Jan 2026 22:12:11 GMT  
		Size: 3.6 KB (3609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.14` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2bbdafdc831d87bdae33f1ed22e11e834cac9924e6c04c0a75d621f38ea4e156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9141f11eb4c178adb3e2f395e698e843d228a644523ea02f223d637f065531b5`

```dockerfile
```

-	Layers:
	-	`sha256:f2322c19f09a252e05c2666313c5773ae0ec3e6e6bf9979ba3b80cfc0d891fb8`  
		Last Modified: Thu, 15 Jan 2026 22:51:25 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.14` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4745062273cd45217a1b1f92f587882d45bee1b698643a6a0d69eef03e6f0fc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213827477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5614231090cb07c25f883f615d8d387e4ad171fd0fea854a81d62a702e181f48`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:11:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:11:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:11:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:11:13 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:11:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:11:13 GMT
ARG VERSION=25.8.14.17
# Thu, 15 Jan 2026 22:11:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:39 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:39 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:40 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:40 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:40 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:40 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297714d85bd1bd0b198fca6dace9d682bdfb99e6e582716cc4a402ea5135fbbf`  
		Last Modified: Thu, 15 Jan 2026 22:12:08 GMT  
		Size: 7.6 MB (7576661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195a3a53e2e0eb5312aabf39c28c7bc006ed22839691070a10ac4e6f85b781a2`  
		Last Modified: Thu, 15 Jan 2026 22:52:05 GMT  
		Size: 178.0 MB (177997293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ae2aaba775f3813680fd84a18107bf25d1cbd69a62aca86efc63a87de10377`  
		Last Modified: Thu, 15 Jan 2026 22:12:07 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178625e79308f5b24a28acea16bfc338aa97911935ad1038cd260a830c4b21eb`  
		Last Modified: Thu, 15 Jan 2026 22:11:58 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696ec49e708558d4523f56fb769ab640f6d7876636d963e16ae9fd1fd6b3cdf8`  
		Last Modified: Thu, 15 Jan 2026 22:12:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0534458f051ddf2bdc3544ffd719e1dc98eb9543380c6886465d64fa25a60be0`  
		Last Modified: Thu, 15 Jan 2026 22:12:00 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a6c12a019e979f88d574e4305b919081b1e6f2700eced0a594cab9e9207ee3`  
		Last Modified: Thu, 15 Jan 2026 22:12:00 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.14` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b49ec4e7cacbb4063ef4b014c20533cc848fad443c3cbddbe2000e2beac58ab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46895b10a1450d21a3af70c5a280e46f4a205d3c43f89d780ddceab33d56520`

```dockerfile
```

-	Layers:
	-	`sha256:6d7fd1fc6025d9d3cdc3f1111b5502b5712170dd438f110ab07d697f387be06a`  
		Last Modified: Thu, 15 Jan 2026 22:51:29 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.14-jammy`

```console
$ docker pull clickhouse@sha256:4bca955e2c69ac02266f3f49a875cd66f309fb3ccc047ef43142d99217cbcec5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.14-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:137c2814b0f9386acb01501cf8b8aee782cea88c67eaf7b0574a8ebd3a42a11c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228927881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:405c6aee9d117ca376bb20a9133443568308ccb1a427c57446a734a6b85dba7f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:11:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:11:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:11:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:11:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:11:04 GMT
ARG VERSION=25.8.14.17
# Thu, 15 Jan 2026 22:11:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:38 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:38 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ef9b857503b896202db7ec6ef5737188d91b89ab5cc14511bef40e8153ec33`  
		Last Modified: Thu, 15 Jan 2026 22:12:01 GMT  
		Size: 7.6 MB (7598572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7717e9dd1378290bdcd675fcf0bf16665dbd8f50fd27de108a0e8452e589ebc1`  
		Last Modified: Thu, 15 Jan 2026 22:12:04 GMT  
		Size: 190.9 MB (190922617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b378e4471da99ac876409cc2c5f4f9665b84b269f04e94d09dd8f13c7f938b`  
		Last Modified: Thu, 15 Jan 2026 22:12:11 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e3057aefd02678456881131f1425134307d5f38db9064c5647e37ded35840e`  
		Last Modified: Thu, 15 Jan 2026 22:12:00 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da24271c02ef1d51851e13c9180fe586b6499a684a5d0b762e793f67c7b348a`  
		Last Modified: Thu, 15 Jan 2026 22:12:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af0ff00bd76836cc516373a39fbe657144cb050655d1788129ccab203a20da1`  
		Last Modified: Thu, 15 Jan 2026 22:12:11 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb344d98f2089982fb2ceed745a809d9165351e7393aff31d18102de4587c4b`  
		Last Modified: Thu, 15 Jan 2026 22:12:11 GMT  
		Size: 3.6 KB (3609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.14-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2bbdafdc831d87bdae33f1ed22e11e834cac9924e6c04c0a75d621f38ea4e156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9141f11eb4c178adb3e2f395e698e843d228a644523ea02f223d637f065531b5`

```dockerfile
```

-	Layers:
	-	`sha256:f2322c19f09a252e05c2666313c5773ae0ec3e6e6bf9979ba3b80cfc0d891fb8`  
		Last Modified: Thu, 15 Jan 2026 22:51:25 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.14-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4745062273cd45217a1b1f92f587882d45bee1b698643a6a0d69eef03e6f0fc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213827477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5614231090cb07c25f883f615d8d387e4ad171fd0fea854a81d62a702e181f48`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:11:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:11:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:11:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:11:13 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:11:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:11:13 GMT
ARG VERSION=25.8.14.17
# Thu, 15 Jan 2026 22:11:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:39 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:39 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:40 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:40 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:40 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:40 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297714d85bd1bd0b198fca6dace9d682bdfb99e6e582716cc4a402ea5135fbbf`  
		Last Modified: Thu, 15 Jan 2026 22:12:08 GMT  
		Size: 7.6 MB (7576661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195a3a53e2e0eb5312aabf39c28c7bc006ed22839691070a10ac4e6f85b781a2`  
		Last Modified: Thu, 15 Jan 2026 22:52:05 GMT  
		Size: 178.0 MB (177997293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ae2aaba775f3813680fd84a18107bf25d1cbd69a62aca86efc63a87de10377`  
		Last Modified: Thu, 15 Jan 2026 22:12:07 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178625e79308f5b24a28acea16bfc338aa97911935ad1038cd260a830c4b21eb`  
		Last Modified: Thu, 15 Jan 2026 22:11:58 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696ec49e708558d4523f56fb769ab640f6d7876636d963e16ae9fd1fd6b3cdf8`  
		Last Modified: Thu, 15 Jan 2026 22:12:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0534458f051ddf2bdc3544ffd719e1dc98eb9543380c6886465d64fa25a60be0`  
		Last Modified: Thu, 15 Jan 2026 22:12:00 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a6c12a019e979f88d574e4305b919081b1e6f2700eced0a594cab9e9207ee3`  
		Last Modified: Thu, 15 Jan 2026 22:12:00 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.14-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b49ec4e7cacbb4063ef4b014c20533cc848fad443c3cbddbe2000e2beac58ab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46895b10a1450d21a3af70c5a280e46f4a205d3c43f89d780ddceab33d56520`

```dockerfile
```

-	Layers:
	-	`sha256:6d7fd1fc6025d9d3cdc3f1111b5502b5712170dd438f110ab07d697f387be06a`  
		Last Modified: Thu, 15 Jan 2026 22:51:29 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.14.17`

```console
$ docker pull clickhouse@sha256:4bca955e2c69ac02266f3f49a875cd66f309fb3ccc047ef43142d99217cbcec5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.14.17` - linux; amd64

```console
$ docker pull clickhouse@sha256:137c2814b0f9386acb01501cf8b8aee782cea88c67eaf7b0574a8ebd3a42a11c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228927881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:405c6aee9d117ca376bb20a9133443568308ccb1a427c57446a734a6b85dba7f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:11:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:11:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:11:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:11:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:11:04 GMT
ARG VERSION=25.8.14.17
# Thu, 15 Jan 2026 22:11:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:38 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:38 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ef9b857503b896202db7ec6ef5737188d91b89ab5cc14511bef40e8153ec33`  
		Last Modified: Thu, 15 Jan 2026 22:12:01 GMT  
		Size: 7.6 MB (7598572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7717e9dd1378290bdcd675fcf0bf16665dbd8f50fd27de108a0e8452e589ebc1`  
		Last Modified: Thu, 15 Jan 2026 22:12:04 GMT  
		Size: 190.9 MB (190922617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b378e4471da99ac876409cc2c5f4f9665b84b269f04e94d09dd8f13c7f938b`  
		Last Modified: Thu, 15 Jan 2026 22:12:11 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e3057aefd02678456881131f1425134307d5f38db9064c5647e37ded35840e`  
		Last Modified: Thu, 15 Jan 2026 22:12:00 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da24271c02ef1d51851e13c9180fe586b6499a684a5d0b762e793f67c7b348a`  
		Last Modified: Thu, 15 Jan 2026 22:12:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af0ff00bd76836cc516373a39fbe657144cb050655d1788129ccab203a20da1`  
		Last Modified: Thu, 15 Jan 2026 22:12:11 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb344d98f2089982fb2ceed745a809d9165351e7393aff31d18102de4587c4b`  
		Last Modified: Thu, 15 Jan 2026 22:12:11 GMT  
		Size: 3.6 KB (3609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.14.17` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2bbdafdc831d87bdae33f1ed22e11e834cac9924e6c04c0a75d621f38ea4e156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9141f11eb4c178adb3e2f395e698e843d228a644523ea02f223d637f065531b5`

```dockerfile
```

-	Layers:
	-	`sha256:f2322c19f09a252e05c2666313c5773ae0ec3e6e6bf9979ba3b80cfc0d891fb8`  
		Last Modified: Thu, 15 Jan 2026 22:51:25 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.14.17` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4745062273cd45217a1b1f92f587882d45bee1b698643a6a0d69eef03e6f0fc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213827477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5614231090cb07c25f883f615d8d387e4ad171fd0fea854a81d62a702e181f48`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:11:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:11:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:11:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:11:13 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:11:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:11:13 GMT
ARG VERSION=25.8.14.17
# Thu, 15 Jan 2026 22:11:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:39 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:39 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:40 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:40 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:40 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:40 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297714d85bd1bd0b198fca6dace9d682bdfb99e6e582716cc4a402ea5135fbbf`  
		Last Modified: Thu, 15 Jan 2026 22:12:08 GMT  
		Size: 7.6 MB (7576661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195a3a53e2e0eb5312aabf39c28c7bc006ed22839691070a10ac4e6f85b781a2`  
		Last Modified: Thu, 15 Jan 2026 22:52:05 GMT  
		Size: 178.0 MB (177997293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ae2aaba775f3813680fd84a18107bf25d1cbd69a62aca86efc63a87de10377`  
		Last Modified: Thu, 15 Jan 2026 22:12:07 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178625e79308f5b24a28acea16bfc338aa97911935ad1038cd260a830c4b21eb`  
		Last Modified: Thu, 15 Jan 2026 22:11:58 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696ec49e708558d4523f56fb769ab640f6d7876636d963e16ae9fd1fd6b3cdf8`  
		Last Modified: Thu, 15 Jan 2026 22:12:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0534458f051ddf2bdc3544ffd719e1dc98eb9543380c6886465d64fa25a60be0`  
		Last Modified: Thu, 15 Jan 2026 22:12:00 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a6c12a019e979f88d574e4305b919081b1e6f2700eced0a594cab9e9207ee3`  
		Last Modified: Thu, 15 Jan 2026 22:12:00 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.14.17` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b49ec4e7cacbb4063ef4b014c20533cc848fad443c3cbddbe2000e2beac58ab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46895b10a1450d21a3af70c5a280e46f4a205d3c43f89d780ddceab33d56520`

```dockerfile
```

-	Layers:
	-	`sha256:6d7fd1fc6025d9d3cdc3f1111b5502b5712170dd438f110ab07d697f387be06a`  
		Last Modified: Thu, 15 Jan 2026 22:51:29 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.14.17-jammy`

```console
$ docker pull clickhouse@sha256:4bca955e2c69ac02266f3f49a875cd66f309fb3ccc047ef43142d99217cbcec5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.14.17-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:137c2814b0f9386acb01501cf8b8aee782cea88c67eaf7b0574a8ebd3a42a11c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228927881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:405c6aee9d117ca376bb20a9133443568308ccb1a427c57446a734a6b85dba7f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:11:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:11:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:11:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:11:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:11:04 GMT
ARG VERSION=25.8.14.17
# Thu, 15 Jan 2026 22:11:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:38 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:38 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ef9b857503b896202db7ec6ef5737188d91b89ab5cc14511bef40e8153ec33`  
		Last Modified: Thu, 15 Jan 2026 22:12:01 GMT  
		Size: 7.6 MB (7598572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7717e9dd1378290bdcd675fcf0bf16665dbd8f50fd27de108a0e8452e589ebc1`  
		Last Modified: Thu, 15 Jan 2026 22:12:04 GMT  
		Size: 190.9 MB (190922617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b378e4471da99ac876409cc2c5f4f9665b84b269f04e94d09dd8f13c7f938b`  
		Last Modified: Thu, 15 Jan 2026 22:12:11 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e3057aefd02678456881131f1425134307d5f38db9064c5647e37ded35840e`  
		Last Modified: Thu, 15 Jan 2026 22:12:00 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da24271c02ef1d51851e13c9180fe586b6499a684a5d0b762e793f67c7b348a`  
		Last Modified: Thu, 15 Jan 2026 22:12:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af0ff00bd76836cc516373a39fbe657144cb050655d1788129ccab203a20da1`  
		Last Modified: Thu, 15 Jan 2026 22:12:11 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb344d98f2089982fb2ceed745a809d9165351e7393aff31d18102de4587c4b`  
		Last Modified: Thu, 15 Jan 2026 22:12:11 GMT  
		Size: 3.6 KB (3609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.14.17-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2bbdafdc831d87bdae33f1ed22e11e834cac9924e6c04c0a75d621f38ea4e156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9141f11eb4c178adb3e2f395e698e843d228a644523ea02f223d637f065531b5`

```dockerfile
```

-	Layers:
	-	`sha256:f2322c19f09a252e05c2666313c5773ae0ec3e6e6bf9979ba3b80cfc0d891fb8`  
		Last Modified: Thu, 15 Jan 2026 22:51:25 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.14.17-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4745062273cd45217a1b1f92f587882d45bee1b698643a6a0d69eef03e6f0fc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213827477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5614231090cb07c25f883f615d8d387e4ad171fd0fea854a81d62a702e181f48`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:11:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:11:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:11:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:11:13 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:11:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:11:13 GMT
ARG VERSION=25.8.14.17
# Thu, 15 Jan 2026 22:11:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:39 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:39 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:40 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:40 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:40 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:40 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297714d85bd1bd0b198fca6dace9d682bdfb99e6e582716cc4a402ea5135fbbf`  
		Last Modified: Thu, 15 Jan 2026 22:12:08 GMT  
		Size: 7.6 MB (7576661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195a3a53e2e0eb5312aabf39c28c7bc006ed22839691070a10ac4e6f85b781a2`  
		Last Modified: Thu, 15 Jan 2026 22:52:05 GMT  
		Size: 178.0 MB (177997293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ae2aaba775f3813680fd84a18107bf25d1cbd69a62aca86efc63a87de10377`  
		Last Modified: Thu, 15 Jan 2026 22:12:07 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178625e79308f5b24a28acea16bfc338aa97911935ad1038cd260a830c4b21eb`  
		Last Modified: Thu, 15 Jan 2026 22:11:58 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696ec49e708558d4523f56fb769ab640f6d7876636d963e16ae9fd1fd6b3cdf8`  
		Last Modified: Thu, 15 Jan 2026 22:12:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0534458f051ddf2bdc3544ffd719e1dc98eb9543380c6886465d64fa25a60be0`  
		Last Modified: Thu, 15 Jan 2026 22:12:00 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a6c12a019e979f88d574e4305b919081b1e6f2700eced0a594cab9e9207ee3`  
		Last Modified: Thu, 15 Jan 2026 22:12:00 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.14.17-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b49ec4e7cacbb4063ef4b014c20533cc848fad443c3cbddbe2000e2beac58ab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46895b10a1450d21a3af70c5a280e46f4a205d3c43f89d780ddceab33d56520`

```dockerfile
```

-	Layers:
	-	`sha256:6d7fd1fc6025d9d3cdc3f1111b5502b5712170dd438f110ab07d697f387be06a`  
		Last Modified: Thu, 15 Jan 2026 22:51:29 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:jammy`

```console
$ docker pull clickhouse@sha256:9c348b2bd082bf71b8401397bb79f75e6698f3de0f1552f2742dab4e6909377e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:e87ff5cc4db0ee4bd74404347ba9caa3e3ab5ef325db02aa1ba773f0f823ea81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246322771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852801b390c937417eee197f95cae6c5575ef31f3bc676501e5733f2732fa92a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:45 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:10:45 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:10:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:10:45 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:10:45 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:10:45 GMT
ARG VERSION=25.12.3.21
# Thu, 15 Jan 2026 22:10:45 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:15 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:15 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:15 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:16 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:16 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:16 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83cb5d9b0d9196f8fbe14025ad18475a55f20d4a27d7ec251d3790d05808e146`  
		Last Modified: Thu, 15 Jan 2026 22:11:49 GMT  
		Size: 7.6 MB (7598550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab75fa925b2df2acd4af08b5acff65f28cd8bdfeb13b687340aaa11fc602623`  
		Last Modified: Thu, 15 Jan 2026 22:52:15 GMT  
		Size: 208.3 MB (208317501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed06808047e10a168d67bf3d37fd53b16619284a18291d24e0e035551b64bba3`  
		Last Modified: Thu, 15 Jan 2026 22:11:37 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88194bfab547d36d32697803376d16fa6f50a5706e11835d6b2e5149249e3fd4`  
		Last Modified: Thu, 15 Jan 2026 22:11:38 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9694b94933bd348b79a326e9e90b99c980c93497916c9afea0517e9e59510dbd`  
		Last Modified: Thu, 15 Jan 2026 22:11:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c40bd2e7d92e7c7db010275427785be0871517f608b23e3062d094e4f11009`  
		Last Modified: Thu, 15 Jan 2026 22:11:39 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05fca4bd1478ce07af6e595b1ea1c177d3fcfc6fbf9844a850a0e6fc306fd03`  
		Last Modified: Thu, 15 Jan 2026 22:11:42 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8deb39a713f008acdec3251678de02eb74fdfffabbb7e17040b103fd78983a21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73dda45360c6471ea6f661c4f5ae30a7ffc26ae55624a1ad6d5cac45ff451818`

```dockerfile
```

-	Layers:
	-	`sha256:ed29f8b17477a4026a6b1c15b5babe8cec498591f0abd7fc02b73306b0839930`  
		Last Modified: Thu, 15 Jan 2026 22:50:48 GMT  
		Size: 26.0 KB (26047 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:30190af3158d8b3b3a48f60bdabfc40f26b446d16f28529014262d88e5dd2b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228224093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b161afcc2f6dd175ca36bc983f0bb75365d90b91db4bfcbc023a9c93ed07e9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:34 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:10:34 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:10:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:10:34 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:10:34 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:10:34 GMT
ARG VERSION=25.12.3.21
# Thu, 15 Jan 2026 22:10:34 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:04 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:04 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3df312c201c41d963c5bdc407650a174e7712d5b8aff75c83b0c6e2755b1208`  
		Last Modified: Thu, 15 Jan 2026 22:11:26 GMT  
		Size: 7.6 MB (7576689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bb9a92d4b2fd9436589e7c5649592d95edac119b4ab6a8460c0700e67ffa37`  
		Last Modified: Thu, 15 Jan 2026 22:11:29 GMT  
		Size: 192.4 MB (192393858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ccbc4119e8834350abf692cba0442fb6e8b1ae37944efd9240f68e493868a07`  
		Last Modified: Thu, 15 Jan 2026 22:11:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5438f0c9f26c70a44ea1b4bc005c852e7919abc5eede23dd3a7b6f26015d11`  
		Last Modified: Thu, 15 Jan 2026 22:11:26 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7f0fe7586dc17cf8a7c98584015cc914819093423666de59fbdd09517f7018`  
		Last Modified: Thu, 15 Jan 2026 22:28:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da9049ed0141a54a80279b382c924b58ddfd2bdd4b30df9481610ecbb1ca834`  
		Last Modified: Thu, 15 Jan 2026 22:11:36 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aaec0e1cac56fdd17db6b0d9f73eafdf93fd7ecbc8a724f365da206621940c5`  
		Last Modified: Thu, 15 Jan 2026 22:11:28 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:72d6bc00b24890fcefc779de396dd7bf35973955caff366e6957e679fd5f6f34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66aeb9bbe2041bbf2c5fdaca3c3705af0cfc09ea38f7e9eeb469af9a7e3ee66b`

```dockerfile
```

-	Layers:
	-	`sha256:166252afa9942cdc70c9de156ab1064cca9eeee6a864d1fa47f76f812f2431b3`  
		Last Modified: Thu, 15 Jan 2026 22:11:26 GMT  
		Size: 26.3 KB (26258 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:9c348b2bd082bf71b8401397bb79f75e6698f3de0f1552f2742dab4e6909377e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

```console
$ docker pull clickhouse@sha256:e87ff5cc4db0ee4bd74404347ba9caa3e3ab5ef325db02aa1ba773f0f823ea81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246322771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852801b390c937417eee197f95cae6c5575ef31f3bc676501e5733f2732fa92a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:45 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:10:45 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:10:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:10:45 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:10:45 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:10:45 GMT
ARG VERSION=25.12.3.21
# Thu, 15 Jan 2026 22:10:45 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:15 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:15 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:15 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:16 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:16 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:16 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83cb5d9b0d9196f8fbe14025ad18475a55f20d4a27d7ec251d3790d05808e146`  
		Last Modified: Thu, 15 Jan 2026 22:11:49 GMT  
		Size: 7.6 MB (7598550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab75fa925b2df2acd4af08b5acff65f28cd8bdfeb13b687340aaa11fc602623`  
		Last Modified: Thu, 15 Jan 2026 22:52:15 GMT  
		Size: 208.3 MB (208317501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed06808047e10a168d67bf3d37fd53b16619284a18291d24e0e035551b64bba3`  
		Last Modified: Thu, 15 Jan 2026 22:11:37 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88194bfab547d36d32697803376d16fa6f50a5706e11835d6b2e5149249e3fd4`  
		Last Modified: Thu, 15 Jan 2026 22:11:38 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9694b94933bd348b79a326e9e90b99c980c93497916c9afea0517e9e59510dbd`  
		Last Modified: Thu, 15 Jan 2026 22:11:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c40bd2e7d92e7c7db010275427785be0871517f608b23e3062d094e4f11009`  
		Last Modified: Thu, 15 Jan 2026 22:11:39 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05fca4bd1478ce07af6e595b1ea1c177d3fcfc6fbf9844a850a0e6fc306fd03`  
		Last Modified: Thu, 15 Jan 2026 22:11:42 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8deb39a713f008acdec3251678de02eb74fdfffabbb7e17040b103fd78983a21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73dda45360c6471ea6f661c4f5ae30a7ffc26ae55624a1ad6d5cac45ff451818`

```dockerfile
```

-	Layers:
	-	`sha256:ed29f8b17477a4026a6b1c15b5babe8cec498591f0abd7fc02b73306b0839930`  
		Last Modified: Thu, 15 Jan 2026 22:50:48 GMT  
		Size: 26.0 KB (26047 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:30190af3158d8b3b3a48f60bdabfc40f26b446d16f28529014262d88e5dd2b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228224093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b161afcc2f6dd175ca36bc983f0bb75365d90b91db4bfcbc023a9c93ed07e9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:34 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:10:34 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:10:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:10:34 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:10:34 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:10:34 GMT
ARG VERSION=25.12.3.21
# Thu, 15 Jan 2026 22:10:34 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:04 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.3.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:04 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3df312c201c41d963c5bdc407650a174e7712d5b8aff75c83b0c6e2755b1208`  
		Last Modified: Thu, 15 Jan 2026 22:11:26 GMT  
		Size: 7.6 MB (7576689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49bb9a92d4b2fd9436589e7c5649592d95edac119b4ab6a8460c0700e67ffa37`  
		Last Modified: Thu, 15 Jan 2026 22:11:29 GMT  
		Size: 192.4 MB (192393858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ccbc4119e8834350abf692cba0442fb6e8b1ae37944efd9240f68e493868a07`  
		Last Modified: Thu, 15 Jan 2026 22:11:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5438f0c9f26c70a44ea1b4bc005c852e7919abc5eede23dd3a7b6f26015d11`  
		Last Modified: Thu, 15 Jan 2026 22:11:26 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7f0fe7586dc17cf8a7c98584015cc914819093423666de59fbdd09517f7018`  
		Last Modified: Thu, 15 Jan 2026 22:28:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da9049ed0141a54a80279b382c924b58ddfd2bdd4b30df9481610ecbb1ca834`  
		Last Modified: Thu, 15 Jan 2026 22:11:36 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aaec0e1cac56fdd17db6b0d9f73eafdf93fd7ecbc8a724f365da206621940c5`  
		Last Modified: Thu, 15 Jan 2026 22:11:28 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:72d6bc00b24890fcefc779de396dd7bf35973955caff366e6957e679fd5f6f34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66aeb9bbe2041bbf2c5fdaca3c3705af0cfc09ea38f7e9eeb469af9a7e3ee66b`

```dockerfile
```

-	Layers:
	-	`sha256:166252afa9942cdc70c9de156ab1064cca9eeee6a864d1fa47f76f812f2431b3`  
		Last Modified: Thu, 15 Jan 2026 22:11:26 GMT  
		Size: 26.3 KB (26258 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts`

```console
$ docker pull clickhouse@sha256:4bca955e2c69ac02266f3f49a875cd66f309fb3ccc047ef43142d99217cbcec5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts` - linux; amd64

```console
$ docker pull clickhouse@sha256:137c2814b0f9386acb01501cf8b8aee782cea88c67eaf7b0574a8ebd3a42a11c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228927881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:405c6aee9d117ca376bb20a9133443568308ccb1a427c57446a734a6b85dba7f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:11:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:11:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:11:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:11:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:11:04 GMT
ARG VERSION=25.8.14.17
# Thu, 15 Jan 2026 22:11:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:38 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:38 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ef9b857503b896202db7ec6ef5737188d91b89ab5cc14511bef40e8153ec33`  
		Last Modified: Thu, 15 Jan 2026 22:12:01 GMT  
		Size: 7.6 MB (7598572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7717e9dd1378290bdcd675fcf0bf16665dbd8f50fd27de108a0e8452e589ebc1`  
		Last Modified: Thu, 15 Jan 2026 22:12:04 GMT  
		Size: 190.9 MB (190922617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b378e4471da99ac876409cc2c5f4f9665b84b269f04e94d09dd8f13c7f938b`  
		Last Modified: Thu, 15 Jan 2026 22:12:11 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e3057aefd02678456881131f1425134307d5f38db9064c5647e37ded35840e`  
		Last Modified: Thu, 15 Jan 2026 22:12:00 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da24271c02ef1d51851e13c9180fe586b6499a684a5d0b762e793f67c7b348a`  
		Last Modified: Thu, 15 Jan 2026 22:12:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af0ff00bd76836cc516373a39fbe657144cb050655d1788129ccab203a20da1`  
		Last Modified: Thu, 15 Jan 2026 22:12:11 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb344d98f2089982fb2ceed745a809d9165351e7393aff31d18102de4587c4b`  
		Last Modified: Thu, 15 Jan 2026 22:12:11 GMT  
		Size: 3.6 KB (3609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2bbdafdc831d87bdae33f1ed22e11e834cac9924e6c04c0a75d621f38ea4e156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9141f11eb4c178adb3e2f395e698e843d228a644523ea02f223d637f065531b5`

```dockerfile
```

-	Layers:
	-	`sha256:f2322c19f09a252e05c2666313c5773ae0ec3e6e6bf9979ba3b80cfc0d891fb8`  
		Last Modified: Thu, 15 Jan 2026 22:51:25 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4745062273cd45217a1b1f92f587882d45bee1b698643a6a0d69eef03e6f0fc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213827477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5614231090cb07c25f883f615d8d387e4ad171fd0fea854a81d62a702e181f48`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:11:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:11:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:11:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:11:13 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:11:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:11:13 GMT
ARG VERSION=25.8.14.17
# Thu, 15 Jan 2026 22:11:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:39 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:39 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:40 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:40 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:40 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:40 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297714d85bd1bd0b198fca6dace9d682bdfb99e6e582716cc4a402ea5135fbbf`  
		Last Modified: Thu, 15 Jan 2026 22:12:08 GMT  
		Size: 7.6 MB (7576661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195a3a53e2e0eb5312aabf39c28c7bc006ed22839691070a10ac4e6f85b781a2`  
		Last Modified: Thu, 15 Jan 2026 22:52:05 GMT  
		Size: 178.0 MB (177997293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ae2aaba775f3813680fd84a18107bf25d1cbd69a62aca86efc63a87de10377`  
		Last Modified: Thu, 15 Jan 2026 22:12:07 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178625e79308f5b24a28acea16bfc338aa97911935ad1038cd260a830c4b21eb`  
		Last Modified: Thu, 15 Jan 2026 22:11:58 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696ec49e708558d4523f56fb769ab640f6d7876636d963e16ae9fd1fd6b3cdf8`  
		Last Modified: Thu, 15 Jan 2026 22:12:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0534458f051ddf2bdc3544ffd719e1dc98eb9543380c6886465d64fa25a60be0`  
		Last Modified: Thu, 15 Jan 2026 22:12:00 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a6c12a019e979f88d574e4305b919081b1e6f2700eced0a594cab9e9207ee3`  
		Last Modified: Thu, 15 Jan 2026 22:12:00 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b49ec4e7cacbb4063ef4b014c20533cc848fad443c3cbddbe2000e2beac58ab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46895b10a1450d21a3af70c5a280e46f4a205d3c43f89d780ddceab33d56520`

```dockerfile
```

-	Layers:
	-	`sha256:6d7fd1fc6025d9d3cdc3f1111b5502b5712170dd438f110ab07d697f387be06a`  
		Last Modified: Thu, 15 Jan 2026 22:51:29 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts-jammy`

```console
$ docker pull clickhouse@sha256:4bca955e2c69ac02266f3f49a875cd66f309fb3ccc047ef43142d99217cbcec5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:137c2814b0f9386acb01501cf8b8aee782cea88c67eaf7b0574a8ebd3a42a11c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228927881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:405c6aee9d117ca376bb20a9133443568308ccb1a427c57446a734a6b85dba7f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:11:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:11:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:11:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:11:04 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:11:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:11:04 GMT
ARG VERSION=25.8.14.17
# Thu, 15 Jan 2026 22:11:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:38 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:38 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ef9b857503b896202db7ec6ef5737188d91b89ab5cc14511bef40e8153ec33`  
		Last Modified: Thu, 15 Jan 2026 22:12:01 GMT  
		Size: 7.6 MB (7598572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7717e9dd1378290bdcd675fcf0bf16665dbd8f50fd27de108a0e8452e589ebc1`  
		Last Modified: Thu, 15 Jan 2026 22:12:04 GMT  
		Size: 190.9 MB (190922617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b378e4471da99ac876409cc2c5f4f9665b84b269f04e94d09dd8f13c7f938b`  
		Last Modified: Thu, 15 Jan 2026 22:12:11 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e3057aefd02678456881131f1425134307d5f38db9064c5647e37ded35840e`  
		Last Modified: Thu, 15 Jan 2026 22:12:00 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da24271c02ef1d51851e13c9180fe586b6499a684a5d0b762e793f67c7b348a`  
		Last Modified: Thu, 15 Jan 2026 22:12:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af0ff00bd76836cc516373a39fbe657144cb050655d1788129ccab203a20da1`  
		Last Modified: Thu, 15 Jan 2026 22:12:11 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb344d98f2089982fb2ceed745a809d9165351e7393aff31d18102de4587c4b`  
		Last Modified: Thu, 15 Jan 2026 22:12:11 GMT  
		Size: 3.6 KB (3609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2bbdafdc831d87bdae33f1ed22e11e834cac9924e6c04c0a75d621f38ea4e156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9141f11eb4c178adb3e2f395e698e843d228a644523ea02f223d637f065531b5`

```dockerfile
```

-	Layers:
	-	`sha256:f2322c19f09a252e05c2666313c5773ae0ec3e6e6bf9979ba3b80cfc0d891fb8`  
		Last Modified: Thu, 15 Jan 2026 22:51:25 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4745062273cd45217a1b1f92f587882d45bee1b698643a6a0d69eef03e6f0fc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213827477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5614231090cb07c25f883f615d8d387e4ad171fd0fea854a81d62a702e181f48`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:11:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 15 Jan 2026 22:11:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 15 Jan 2026 22:11:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 15 Jan 2026 22:11:13 GMT
ARG REPO_CHANNEL=stable
# Thu, 15 Jan 2026 22:11:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 15 Jan 2026 22:11:13 GMT
ARG VERSION=25.8.14.17
# Thu, 15 Jan 2026 22:11:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 15 Jan 2026 22:11:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 15 Jan 2026 22:11:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 15 Jan 2026 22:11:39 GMT
ENV LANG=en_US.UTF-8
# Thu, 15 Jan 2026 22:11:39 GMT
ENV TZ=UTC
# Thu, 15 Jan 2026 22:11:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Jan 2026 22:11:40 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 15 Jan 2026 22:11:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 15 Jan 2026 22:11:40 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 15 Jan 2026 22:11:40 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 15 Jan 2026 22:11:40 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 15 Jan 2026 22:11:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297714d85bd1bd0b198fca6dace9d682bdfb99e6e582716cc4a402ea5135fbbf`  
		Last Modified: Thu, 15 Jan 2026 22:12:08 GMT  
		Size: 7.6 MB (7576661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195a3a53e2e0eb5312aabf39c28c7bc006ed22839691070a10ac4e6f85b781a2`  
		Last Modified: Thu, 15 Jan 2026 22:52:05 GMT  
		Size: 178.0 MB (177997293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ae2aaba775f3813680fd84a18107bf25d1cbd69a62aca86efc63a87de10377`  
		Last Modified: Thu, 15 Jan 2026 22:12:07 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178625e79308f5b24a28acea16bfc338aa97911935ad1038cd260a830c4b21eb`  
		Last Modified: Thu, 15 Jan 2026 22:11:58 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696ec49e708558d4523f56fb769ab640f6d7876636d963e16ae9fd1fd6b3cdf8`  
		Last Modified: Thu, 15 Jan 2026 22:12:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0534458f051ddf2bdc3544ffd719e1dc98eb9543380c6886465d64fa25a60be0`  
		Last Modified: Thu, 15 Jan 2026 22:12:00 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a6c12a019e979f88d574e4305b919081b1e6f2700eced0a594cab9e9207ee3`  
		Last Modified: Thu, 15 Jan 2026 22:12:00 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b49ec4e7cacbb4063ef4b014c20533cc848fad443c3cbddbe2000e2beac58ab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46895b10a1450d21a3af70c5a280e46f4a205d3c43f89d780ddceab33d56520`

```dockerfile
```

-	Layers:
	-	`sha256:6d7fd1fc6025d9d3cdc3f1111b5502b5712170dd438f110ab07d697f387be06a`  
		Last Modified: Thu, 15 Jan 2026 22:51:29 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json
